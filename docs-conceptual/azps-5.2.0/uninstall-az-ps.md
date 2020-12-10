---
title: Удаление Azure PowerShell
description: Сведения о том, как полностью удалить Azure PowerShell.
ms.date: 09/15/2020
ms.devlang: powershell
ms.topic: conceptual
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: ec4ecc9902f700e12ce6b22c32b4e07b13b4d4dc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "96856649"
---
# <a name="how-to-uninstall-azure-powershell-modules"></a>Как удалить модули Azure PowerShell

Из этой статьи вы узнаете, как удалить предыдущую версию Azure PowerShell или полностью удалить этот модуль из системы. Если вы решили полностью удалить Azure PowerShell, отправьте нам отзыв с помощью командлета [Send-Feedback](/powershell/module/az.accounts/send-feedback). Если возникнет ошибка, мы будем признательны, если вы [сообщите о ней на GitHub](https://github.com/azure/azure-powershell/issues), чтобы мы исправили ее.

## <a name="uninstall-the-az-module"></a>Удаление модуля Az

Если в вашей системе установлен модуль Az и вы хотите удалить его, это можно сделать одним из двух методов. Выбор метода зависит от того, как был установлен модуль Az. Если вы этого не знаете, сначала выполните инструкции по удалению для MSI.

### <a name="option-1-uninstall-the-az-powershell-module-from-msi"></a>Вариант 1. Удаление модуля Az PowerShell из MSI

Если вы установили модуль Az PowerShell с помощью пакета MSI, удалять модуль нужно через систему Windows, а не PowerShell.

|         Платформа         |                      Instructions                      |
| ------------------------ | ------------------------------------------------------ |
| Windows 10               | Пуск > Параметры > Приложения                                |
| Windows 7 </br>Windows 8 | Пуск > Панель управления > Программы > Удалить программу |

В этом окне в списке программ вы должны увидеть модуль **Azure PowerShell**. Это программа, которую можно удалить. Если этой программы нет в списке, значит, она установлена с помощью PowerShellGet. Следуйте приведенным ниже инструкциям.

### <a name="option-2-uninstall-the-az-powershell-module-from-powershellget"></a>Вариант 2. Удаление модуля Az PowerShell из PowerShellGet

Чтобы удалить модули Az, используйте командлет [Uninstall-Module](/powershell/module/powershellget/uninstall-module). Учтите, что `Uninstall-Module` удаляет только один модуль. Чтобы полностью удалить модуль Az PowerShell, каждый модуль нужно удалять отдельно. Удаление может усложниться, если у вас установлено несколько версий Azure PowerShell.

Чтобы проверить, какие версии модуля Az PowerShell у вас установлены, используйте следующую команду:

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
3.8.0               Az                             PSGallery            Microsoft Azure PowerShell
4.1.0               Az                             PSGallery            Microsoft Azure PowerShell
```

Следующий скрипт запрашивает из коллекции PowerShell список зависимых подмодулей, а затем удаляет правильную версию каждого подмодуля. Для запуска этого скрипта в области, отличающейся от **Процесс** или **Текущий пользователь**, требуются права доступа администратора.

```powershell-interactive
function Uninstall-AzModule {
  [CmdletBinding(SupportsShouldProcess)]
  param(
    [ValidateNotNullOrEmpty()]
    [ValidateSet('Az','AzureRM','Azure')]
    [string]$Name = 'Az',

    [Parameter(Mandatory)]
    [string]$Version,

    [switch]$AllowPrerelease
  )

  $Params = @{}

  if ($PSBoundParameters.AllowPrerelease) {
    $Params.AllowPrerelease = $true
  }

  $IsAdmin = ([Security.Principal.WindowsPrincipal] [Security.Principal.WindowsIdentity]::GetCurrent()).IsInRole([Security.Principal.WindowsBuiltInRole] 'Administrator')

  if (-not(Get-InstalledModule -Name $Name -RequiredVersion $Version -ErrorAction SilentlyContinue -OutVariable RootModule @Params)) {

    Write-Warning -Message "Uninstall aborted. $Name version $Version not found."

  } elseif (($RootModule.InstalledLocation -notlike "*$env:USERPROFILE*") -and ($IsAdmin -eq $false)) {

    Write-Warning -Message "Uninstall aborted. $Name version $Version exists in a system path. PowerShell must be run elevated as an admin to remove it."

  } elseif ((Get-Process -Name powershell, pwsh -OutVariable Sessions -ErrorAction SilentlyContinue).Count -gt 1) {

    Write-Warning -Message "Uninstall aborted. Please close all other PowerShell sessions before continuing. There are currently $($Sessions.Count) PowerShell sessions running."

  } else {
    Write-Verbose -Message 'Creating list of dependencies...'
    $target = Find-Module -Name $Name -RequiredVersion $Version @Params

    $AllModules = @([pscustomobject]@{
      Name = $Name
      Version = $Version
    })

    $AllModules += foreach ($dependency in $target.Dependencies) {
      switch ($dependency.keys) {
        {$_ -contains 'RequiredVersion'} {$UninstallVersion = $dependency.RequiredVersion; break}
        {$_ -contains 'MinimumVersion'} {$UninstallVersion = $dependency.MinimumVersion; break}
      }

      [pscustomobject]@{
        Name = $dependency.Name
        Version = $UninstallVersion
      }
    }

    [int]$i = 100 / $AllModules.Count

    foreach ($module in $AllModules) {
      Write-Progress -Activity 'Uninstallation in Progress' -Status "$i% Complete:" -PercentComplete $i
      $i++

      if (Get-InstalledModule -Name $module.Name -RequiredVersion $module.Version -ErrorAction SilentlyContinue @Params) {
        Write-Verbose -Message "Uninstalling $($module.Name) version $($module.Version)"

        Remove-Module -FullyQualifiedName @{ModuleName=$module.Name;ModuleVersion=$module.Version} -ErrorAction SilentlyContinue

        try {
          if ($PSCmdlet.ShouldProcess("$($module.Name) version $($module.Version)")) {
            Uninstall-Module -Name $module.Name -RequiredVersion $module.Version -Force -ErrorAction Stop @Params
          }
          $State = 'Uninstalled'
        } Catch {
          $State = 'Manual uninstall required'
          Write-Verbose -Message "$($module.Name) version: $($module.Version) may require manual uninstallation."
        }

      } else {
        $State = 'Not found'
        Write-Verbose -Message "$($module.Name) version: $($module.Version) not found."
      }

      if (-not $PSBoundParameters.WhatIf) {
        [pscustomobject]@{
          ModuleName = $module.Name
          Version = $module.Version
          State = $State
        }
      }

    }
  }
}
```

Чтобы воспользоваться этой функцией, скопируйте и вставьте этот код в окно сеанса PowerShell. В примере ниже показано, как выполнить функцию для удаления предыдущей версии модуля Az PowerShell и его подмодулей.

```powershell-interactive
Uninstall-AzModule -Name Az -Version 1.8.0
```

Во время выполнения скрипта в окне будут отображаться **имя**, **версия** и **состояние** каждого удаляемого подмодуля. Чтобы запустить скрипт только для просмотра удаляемых компонентов без их удаления, используйте параметр `-WhatIf`.

```output
ModuleName              Version  State
----------              -------  -----
Az.Accounts             1.5.1    Not found
Az.Aks                  1.0.1    Uninstalled
Az.AnalysisServices     1.1.0    Uninstalled
Az.ApiManagement        1.0.0    Uninstalled
Az.ApplicationInsights  1.0.0    Uninstalled
...
```

> [!IMPORTANT]
> Если скрипт не может сопоставить определенную зависимость с версией для удаления, _ни одна_ из версий этой зависимости не будет удалена. Это обусловлено тем, что на компьютере могут быть установлены другие версии целевого модуля, связанные с этими зависимостями.

Выполните следующий пример для каждой версии модуля Az PowerShell, которую нужно удалить.
Для удобства следующий скрипт удалит все версии Az, **кроме** последней.

```powershell-interactive
$Modules = Get-InstalledModule -Name Az -AllVersions |
    Sort-Object -Property Version -Descending |
        Select-Object -Skip 1
$Modules | ForEach-Object {Uninstall-AzModule -Name $_.Name -Version $_.Version}
```

## <a name="uninstall-the-azurerm-module"></a>Удаление модуля AzureRM

Если в вашей системе установлен модуль Az и вы хотите удалить AzureRM, это можно сделать одним из двух методов. Выбор метода зависит от того, как был установлен модуль AzureRM. Если вы этого не знаете, сначала выполните инструкции по удалению для MSI.

### <a name="option-1-uninstall-the-azurerm-powershell-module-from-msi"></a>Вариант 1. Удаление модуля AzureRM PowerShell из MSI

Если вы установили модуль AzureRM PowerShell с помощью пакета MSI, удалять модуль нужно через систему Windows, а не PowerShell.

|         Платформа         |                      Instructions                      |
| ------------------------ | ------------------------------------------------------ |
| Windows 10               | Пуск > Параметры > Приложения                                |
| Windows 7 </br>Windows 8 | Пуск > Панель управления > Программы > Удалить программу |

В этом окне в списке программ вы должны увидеть **Azure PowerShell** или **Microsoft Azure PowerShell — месяц год**. Это программа, которую можно удалить. Если этой программы нет в списке, значит, она установлена с помощью PowerShellGet. Следуйте приведенным ниже инструкциям.

### <a name="option-2-uninstall-the-azurerm-powershell-module-from-powershellget"></a>Вариант 2. Удаление модуля AzureRM PowerShell из PowerShellGet

Если вы установили AzureRM с помощью PowerShellGet, вы можете удалить модули с помощью командлета [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm), доступного в модуле `Az.Accounts`.

Чтобы использовать модуль `Az.Accounts`, необходимо установить модуль Az.  Одновременное использование модуля AzureRM и модуля Az не поддерживается. Но с помощью модуля Az можно немедленно удалить модуль AzureRM.  Вы можете установить модуль Az и пропустить предупреждение модуля AzureRM с помощью следующей команды (если модуль Az еще не установлен):

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

После установки модуля Az можно удалить _все_ модули AzureRM с компьютера с помощью приведенной ниже команды. Для ее выполнения требуются права администратора.

```powershell-interactive
Uninstall-AzureRm
```
