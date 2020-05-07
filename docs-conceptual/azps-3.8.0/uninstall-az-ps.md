---
title: Удаление Azure PowerShell
description: Сведения о том, как полностью удалить Azure PowerShell.
ms.date: 10/22/2019
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 37f152fb43e23c361544db4a738d58911099da1f
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/05/2020
ms.locfileid: "81740530"
---
# <a name="uninstall-the-azure-powershell-module"></a>Удаление модуля Azure PowerShell

Из этой статьи вы узнаете, как удалить предыдущую версию Azure PowerShell или полностью удалить этот модуль из системы. Если вы решили полностью удалить Azure PowerShell, отправьте нам отзыв с помощью командлета [Send-Feedback](/powershell/module/az.accounts/send-feedback).
Если возникнет ошибка, мы будем признательны, если вы [сообщите о ней на GitHub](https://github.com/azure/azure-powershell/issues), чтобы мы исправили ее.

## <a name="uninstall-azure-powershell-from-msi"></a>Удаление Azure PowerShell из MSI

Если вы установили Azure PowerShell с помощью пакета MSI, удалять модуль нужно через систему Windows, а не PowerShell.

| Платформа | Instructions |
|----------|--------------|
| Windows 10 | Пуск > Параметры > Приложения |
| Windows 7 </br>Windows 8 | Пуск > Панель управления > Программы > Удалить программу |

В этом окне в списке программ вы должны увидеть модуль __Azure PowerShell__. Это программа, которую можно удалить. Если этой программы нет в списке, значит, она установлена с помощью PowerShellGet. Следуйте приведенным ниже инструкциям.

## <a name="uninstall-azure-powershell-from-powershell-get"></a>Удаление Azure PowerShell из PowerShellGet

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

<a name="uninstall-script"/>

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
    if ($_.PSObject.Properties.Name -contains 'requiredVersion') {
      $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$_.requiredVersion}
    }
    else { # Assume minimum version
      # Minimum version actually reports the installed dependency
      # which is used, not the actual "minimum dependency." Check to
      # see if the requested version was installed as a dependency earlier.
      $candidate = Get-InstalledModule $_.name -RequiredVersion $version -ErrorAction Ignore
      if ($candidate) {
        $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$version}
      }
      else {
        $availableModules = Get-InstalledModule $_.name -AllVersions
        Write-Warning ("Could not find uninstall candidate for {0}:{1} - module may require manual uninstall. Available versions are: {2}" -f $_.name,$version,($availableModules.Version -join ', '))
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

> [!NOTE]
> Если скрипт не может сопоставить определенную зависимость с версией для удаления, _ни одна_ из версий этой зависимости не будет удалена. Это обусловлено тем, что на компьютере могут быть установлены другие версии целевого модуля, связанные с этими зависимостями. В этом случае перечисляются доступные версии зависимости.
> После этого вы можете вручную удалить любые предыдущие версии с помощью `Uninstall-Module`.

Выполните эту команду для каждой версии Azure PowerShell, которую нужно удалить. Для удобства следующий скрипт удалит все версии Az, __за исключением__ последней.

```powershell-interactive
$versions = (Get-InstalledModule Az -AllVersions | Select-Object Version)
$versions[0..($versions.Length-2)]  | foreach { Uninstall-AllModules -TargetModule Az -Version ($_.Version) -Force }
```

## <a name="uninstall-the-azurerm-module"></a>Удаление модуля AzureRM

Если в вашей системе установлен модуль Az и вы хотите удалить AzureRM, существуют два метода, которые не требуют выполнения сценария `Uninstall-AllModules`, описанного выше. Выбор метода зависит от того, как был установлен модуль AzureRM.
Если вы этого не знаете, тогда сначала удалите MSI.

### <a name="uninstall-azure-powershell-msi"></a>Удаление Azure PowerShell MSI

Если вы установили модули AzureRM Azure PowerShell с помощью пакета MSI, удалять модуль нужно через систему Windows, а не PowerShell.

| Платформа | Instructions |
|----------|--------------|
| Windows 10 | Пуск > Параметры > Приложения |
| Windows 7 </br>Windows 8 | Пуск > Панель управления > Программы > Удалить программу |

В этом окне в списке программ вы должны увидеть __Azure PowerShell__ или __Microsoft Azure PowerShell — месяц год__. Это программа, которую можно удалить. Если этой программы нет в списке, значит, она установлена с помощью PowerShellGet. Следуйте приведенным ниже инструкциям.

### <a name="uninstall-from-powershell"></a>Удаление с помощью PowerShell

Если вы установили AzureRM с помощью PowerShellGet, то модули можно удалить с помощью команды [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm), доступной в модуле `Az.Accounts`. С вашего компьютера удалятся _все_ модули AzureRM, но для этого требуются права администратора.

```powershell-interactive
Uninstall-AzureRm
```
или диспетчер конфигурации служб
```powershell-interactive
Uninstall-Module AzureRm
```

Если вам не удается запустить команду `Uninstall-AzureRM`, используйте [скрипт `Uninstall-AllModules`](#uninstall-script), приведенный в этой статье, путем следующего вызова:

```powershell-interactive
$versions = (Get-InstalledModule AzureRM -AllVersions | Select-Object Version)
$versions | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```
или диспетчер конфигурации служб
```powershell-interactive
foreach ($module in (Get-Module -ListAvailable AzureRM*).Name |Get-Unique) {
   write-host "Removing Module $module"
   Uninstall-module $module
}
```
