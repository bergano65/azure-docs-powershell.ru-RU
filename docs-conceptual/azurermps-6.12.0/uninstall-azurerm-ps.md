---
title: Удаление Azure PowerShell
description: Сведения о том, как полностью удалить Azure PowerShell.
ms.date: 09/11/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 3543dbb692a41bd3b417bb3d771e67c52d57c340
ms.sourcegitcommit: ac4b53bb42a25aae013a9d8cd9ae98ada9397274
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/08/2018
ms.locfileid: "51274659"
---
# <a name="uninstall-the-azure-powershell-module"></a>Удаление модуля Azure PowerShell

Из этой статьи вы узнаете, как удалить предыдущую версию Azure PowerShell или полностью удалить этот модуль из системы. Если вы решили полностью удалить Azure PowerShell, отправьте нам отзыв с помощью командлета [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).
Если возникнет ошибка, мы будем признательны, если вы [сообщите о ней на GitHub](https://github.com/azure/azure-powershell/issues).

## <a name="uninstall-from-powershell"></a>Удаление с помощью PowerShell

Если вы установили Azure PowerShell с помощью PowerShellGet, для удаления можно использовать командлет [Uninstall-Module](/powershell/module/powershellget/uninstall-module). Учтите, что `Uninstall-Module` удаляет только один модуль. Чтобы полностью удалить Azure PowerShell, каждый модуль нужно удалять отдельно. Удаление может усложниться, если у вас установлено несколько версий Azure PowerShell.

Следующий скрипт запрашивает из коллекции PowerShell список зависимых подмодулей, а затем удаляет правильную версию каждого подмодуля.

```powershell-interactive
function Uninstall-AllModules {
  param(
    [Parameter(Mandatory=$true)]
    [string]$TargetModule,

    [Parameter(Mandatory=$true)]
    [string]$Version,

    [switch]$Force
  )

  $AllModules = @()

  'Creating list of dependencies...'
  $target = Find-Module $TargetModule -RequiredVersion $version
  $target.Dependencies | ForEach-Object {
    $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$_.requiredversion}
  }
  $AllModules += New-Object -TypeName psobject -Property @{name=$TargetModule; version=$Version}

  foreach ($module in $AllModules) {
    Write-Host ('Uninstalling {0} version {1}' -f $module.name,$module.version)
    try {
      Uninstall-Module -Name $module.name -RequiredVersion $module.version -Force:$Force -ErrorAction Stop
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

Во время выполнения скрипта в окне будут отображаться имя и версия каждого удаляемого подмодуля.

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

## <a name="uninstall-msi"></a>Удаление пакета MSI

Если вы установили Azure PowerShell с помощью пакета MSI, удалять модуль нужно через систему Windows, а не PowerShell.

| платформа | Указания |
|----------|--------------|
| Windows 10 | "Пуск" > "Параметры" > "Приложения" |
| Windows 7 </br>Windows 8 | "Пуск" > "Панель управления" > "Программы" > "Удаление программы" |

В этом окне в списке программ вы должны увидеть модуль Azure PowerShell, который нужно удалить.