---
title: Удаление Azure PowerShell
description: Сведения о том, как полностью удалить Azure PowerShell.
ms.date: 12/13/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: fcec2c713d1967a5a70df9b13aa30d9ff4625e9d
ms.sourcegitcommit: 447276d46ffeeb37f0c07a570536665e36c5ddb8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/14/2019
ms.locfileid: "57882366"
---
# <a name="uninstall-the-azure-powershell-module"></a>Удаление модуля Azure PowerShell

Из этой статьи вы узнаете, как удалить предыдущую версию Azure PowerShell или полностью удалить этот модуль из системы. Если вы решили полностью удалить Azure PowerShell, отправьте нам отзыв с помощью командлета [Send-Feedback](/powershell/module/az.accounts/send-feedback).
Если вы обнаружите ошибку, пожалуйста, [сообщите о ней на сайте GitHub](https://github.com/azure/azure-powershell/issues).

## <a name="uninstall-the-az-module"></a>Удаление модуля Az

Чтобы удалить модули Az, используйте командлет [Uninstall-Module](/powershell/module/powershellget/uninstall-module). Учтите, что `Uninstall-Module` удаляет только один модуль. Чтобы полностью удалить Azure PowerShell, каждый модуль нужно удалять отдельно. Удаление может усложниться, если у вас установлено несколько версий Azure PowerShell.

Чтобы проверить, какие версии Azure PowerShell у вас установлены, используйте следующую команду:

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
0.7.0               Az                             PSGallery            Azure Resource Manager Module
1.0.0               Az                             PSGallery            Azure Resource Manager Module
```

Следующий скрипт запрашивает из коллекции PowerShell список зависимых подмодулей, а затем удаляет правильную версию каждого подмодуля. Необходимы права доступа администратора для запуска этого скрипта в области, отличающейся от `Process` или `CurrentUser`.

```powershell-interactive
function Uninstall-AllModules {
  param(
    [Parameter(Mandatory=$true)]
    [string]$TargetModule,

    [Parameter(Mandatory=$true)]
    [string]$Version,

    [switch]$Force,

    [switch]$WhatIf
  )
  
  $AllModules = @()
  
  'Creating list of dependencies...'
  $target = Find-Module $TargetModule -RequiredVersion $version
  $target.Dependencies | ForEach-Object {
    if ($_.requiredVersion) {
      $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$_.requiredVersion}
    }
    else { # Assume minimum version
      # Minimum version actually reports the installed dependency
      # which is used, not the actual "minimum dependency." Check to
      # see if the requested version was installed as a dependency earlier.
      $candidate = Get-InstalledModule $_.name -RequiredVersion $version
      if ($candidate) {
        $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$version}
      }
      else {
        Write-Warning ("Could not find uninstall candidate for {0}:{1} - module may require manual uninstall" -f $_.name,$version)
      }
    }
  }
  $AllModules += New-Object -TypeName psobject -Property @{name=$TargetModule; version=$Version}

  foreach ($module in $AllModules) {
    Write-Host ('Uninstalling {0} version {1}...' -f $module.name,$module.version)
    try {
      Uninstall-Module -Name $module.name -RequiredVersion $module.version -Force:$Force -ErrorAction Stop -WhatIf:$WhatIf
    } catch {
      Write-Host ("`t" + $_.Exception.Message)
    }
  }
}
```

Чтобы воспользоваться этой функцией, скопируйте и вставьте этот код в окно сеанса PowerShell. В примере ниже показано, как запустить функцию, чтобы удалить предыдущую версию Azure PowerShell.

```powershell-interactive
Uninstall-AllModules -TargetModule Az -Version 0.7.0 -Force
```

Во время выполнения скрипта в окне будут отображаться имя и версия каждого удаляемого подмодуля. Чтобы запустить скрипт для просмотра только удаляемых компонентов без удаления, используйте параметр `-WhatIf`.

```output
Creating list of dependencies...
Uninstalling Az.Profile version 0.7.0
Uninstalling Az.Aks version 0.7.0
Uninstalling Az.AnalysisServices version 0.7.0
...
```

Выполните эту команду для каждой версии Azure PowerShell, которую нужно удалить. Для удобства следующий скрипт удалит все версии Az, __за исключением__ последней.

```powershell-interactive
$versions = (Get-InstalledModule Az -AllVersions | Select-Object Version)
$versions[1..($versions.Length-1)]  | foreach { Uninstall-AllModules -TargetModule Az -Version ($_.Version) -Force }
```

## <a name="uninstall-the-azurerm-module"></a>Удаление модуля AzureRM

Если в вашей системе установлен модуль Az и вы хотите удалить AzureRM, существуют два простых метода, которые не требуют запуска сценария `Uninstall-AllModules`, описанного выше. Выбор метода зависит от того, как был установлен AzureRM.
Если вы этого не знаете, сперва проверьте действия по удалению MSI.

### <a name="uninstall-azure-powershell-msi"></a>Удаление Azure PowerShell MSI

Если вы установили модули AzureRM Azure PowerShell с помощью пакета MSI, удалять модуль нужно через систему Windows, а не PowerShell.

| платформа | Указания |
|----------|--------------|
| Windows 10 | "Пуск" > "Параметры" > "Приложения" |
| Windows 7 </br>Windows 8 | "Пуск" > "Панель управления" > "Программы" > "Удаление программы" |

В этом окне в списке программ вы должны увидеть модуль __Azure PowerShell__. Это программа, которую можно удалить.

### <a name="uninstall-from-powershell"></a>Удаление с помощью PowerShell

Если вы установили AzureRM из PowerShellGet, то можете удалить модули с помощью новой команды `Uninstall-AzureRM`. С вашего компьютера удалятся _все_ модули AzureRM, но для этого требуются права администратора.

```powershell-interactive
Uninstall-AzureRm
```

Если вам не удается запустить команду `Uninstall-AzureRM`, то вместо нее используйте скрипт `Uninstall-AllModules`, приведенный в этой статье.