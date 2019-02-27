---
title: Удаление Azure PowerShell
description: Сведения о том, как полностью удалить Azure PowerShell.
ms.date: 11/30/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: a0afae1ba51fdb34425c91049e08d7388f434d7d
ms.sourcegitcommit: 0b5b0434fba7a752b0199256e04fa34f06aaf33a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/21/2019
ms.locfileid: "56464984"
---
# <a name="uninstall-the-azure-powershell-module"></a>Удаление модуля Azure PowerShell

Из этой статьи вы узнаете, как удалить предыдущую версию Azure PowerShell или полностью удалить этот модуль из системы. Если вы решили полностью удалить Azure PowerShell, отправьте нам отзыв с помощью командлета [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).
Если вы обнаружите ошибку, пожалуйста, [сообщите о ней на сайте GitHub](https://github.com/azure/azure-powershell/issues).


## <a name="uninstall-azure-powershell-msi"></a>Удаление Azure PowerShell MSI

Если вы установили Azure PowerShell с помощью пакета MSI, удалять модуль нужно через систему Windows, а не PowerShell.

| платформа | Указания |
|----------|--------------|
| Windows 10 | "Пуск" > "Параметры" > "Приложения" |
| Windows 7 </br>Windows 8 | "Пуск" > "Панель управления" > "Программы" > "Удаление программы" |

В этом окне в списке программ вы должны увидеть модуль __Azure PowerShell__. Это программа, которую можно удалить.

## <a name="uninstall-from-powershell"></a>Удаление с помощью PowerShell

Если вы установили Azure PowerShell с помощью PowerShellGet, для удаления можно использовать командлет [Uninstall-Module](/powershell/module/powershellget/uninstall-module). Учтите, что `Uninstall-Module` удаляет только один модуль. Чтобы полностью удалить Azure PowerShell, каждый модуль нужно удалять отдельно. Удаление может усложниться, если у вас установлено несколько версий Azure PowerShell.

Чтобы проверить, какие версии Azure PowerShell у вас установлены, используйте следующую команду:

```powershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions
```

```output
Version              Name                                Repository           Description
-------              ----                                ----------           -----------
6.11.0               AzureRM                             PSGallery            Azure Resource Manager Module
6.13.1               AzureRM                             PSGallery            Azure Resource Manager Module
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
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

Во время выполнения скрипта в окне будут отображаться имя и версия каждого удаляемого подмодуля. Чтобы запустить скрипт для просмотра только удаляемых компонентов без удаления, используйте параметр `-WhatIf`.

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

Выполните эту команду для каждой версии Azure PowerShell, которую нужно удалить. Для удобства следующий скрипт удалит все версии AzureRM __за исключением__ последней.

```powershell-interactive
$versions = (get-installedmodule AzureRM -AllVersions | Select-Object Version)
$versions[1..($versions.Length-1)]  | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```
