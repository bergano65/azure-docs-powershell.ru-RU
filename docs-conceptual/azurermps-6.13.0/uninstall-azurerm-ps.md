---
title: Удаление Azure PowerShell
description: Сведения о том, как полностью удалить Azure PowerShell.
ms.date: 09/11/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: bf1f81b4929ec066eeb888da4ba1303430f026b4
ms.sourcegitcommit: 80a3da199954d0ab78765715fb49793e89a30f12
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/22/2018
ms.locfileid: "52259898"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="9bade-103">Удаление модуля Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="9bade-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="9bade-104">Из этой статьи вы узнаете, как удалить предыдущую версию Azure PowerShell или полностью удалить этот модуль из системы.</span><span class="sxs-lookup"><span data-stu-id="9bade-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="9bade-105">Если вы решили полностью удалить Azure PowerShell, отправьте нам отзыв с помощью командлета [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="9bade-105">If you've decided to completely uninstall the Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>
<span data-ttu-id="9bade-106">Если вы обнаружите ошибку, пожалуйста, [сообщите о ней на сайте GitHub](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="9bade-106">If you encounter a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues).</span></span>

## <a name="uninstall-from-powershell"></a><span data-ttu-id="9bade-107">Удаление с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="9bade-107">Uninstall from PowerShell</span></span>

<span data-ttu-id="9bade-108">Если вы установили Azure PowerShell с помощью PowerShellGet, для удаления можно использовать командлет [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="9bade-108">If you installed Azure PowerShell using PowerShellGet, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="9bade-109">Учтите, что `Uninstall-Module` удаляет только один модуль.</span><span class="sxs-lookup"><span data-stu-id="9bade-109">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="9bade-110">Чтобы полностью удалить Azure PowerShell, каждый модуль нужно удалять отдельно.</span><span class="sxs-lookup"><span data-stu-id="9bade-110">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="9bade-111">Удаление может усложниться, если у вас установлено несколько версий Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9bade-111">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="9bade-112">Следующий скрипт запрашивает из коллекции PowerShell список зависимых подмодулей,</span><span class="sxs-lookup"><span data-stu-id="9bade-112">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="9bade-113">а затем удаляет правильную версию каждого подмодуля.</span><span class="sxs-lookup"><span data-stu-id="9bade-113">Then, the script uninstalls the correct version of each submodule.</span></span>

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
    $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$_.minimumVersion}
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

<span data-ttu-id="9bade-114">Чтобы воспользоваться этой функцией, скопируйте и вставьте этот код в окно сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9bade-114">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="9bade-115">В примере ниже показано, как запустить функцию, чтобы удалить предыдущую версию Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9bade-115">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

<span data-ttu-id="9bade-116">Во время выполнения скрипта в окне будут отображаться имя и версия каждого удаляемого подмодуля.</span><span class="sxs-lookup"><span data-stu-id="9bade-116">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span>

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

<span data-ttu-id="9bade-117">Выполните эту команду для каждой версии Azure PowerShell, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="9bade-117">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="9bade-118">Для удобства следующий скрипт удалит все версии AzureRM __за исключением__ последней.</span><span class="sxs-lookup"><span data-stu-id="9bade-118">For convenience, the following script will uninstall all versions of AzureRM __except__ for the latest.</span></span>

```powershell-interactive
$versions = (get-installedmodule AzureRM -AllVersions | Select-Object Version)
$versions[1..($versions.Length-1)]  | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```

## <a name="uninstall-msi"></a><span data-ttu-id="9bade-119">Удаление пакета MSI</span><span class="sxs-lookup"><span data-stu-id="9bade-119">Uninstall MSI</span></span>

<span data-ttu-id="9bade-120">Если вы установили Azure PowerShell с помощью пакета MSI, удалять модуль нужно через систему Windows, а не PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9bade-120">If you installed Azure PowerShell using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="9bade-121">платформа</span><span class="sxs-lookup"><span data-stu-id="9bade-121">Platform</span></span> | <span data-ttu-id="9bade-122">Указания</span><span class="sxs-lookup"><span data-stu-id="9bade-122">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="9bade-123">Windows 10</span><span class="sxs-lookup"><span data-stu-id="9bade-123">Windows 10</span></span> | <span data-ttu-id="9bade-124">"Пуск" > "Параметры" > "Приложения"</span><span class="sxs-lookup"><span data-stu-id="9bade-124">Start > Settings > Apps</span></span> |
| <span data-ttu-id="9bade-125">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9bade-125">Windows 7</span></span> </br><span data-ttu-id="9bade-126">Windows 8</span><span class="sxs-lookup"><span data-stu-id="9bade-126">Windows 8</span></span> | <span data-ttu-id="9bade-127">"Пуск" > "Панель управления" > "Программы" > "Удаление программы"</span><span class="sxs-lookup"><span data-stu-id="9bade-127">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="9bade-128">В этом окне в списке программ вы должны увидеть модуль Azure PowerShell, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="9bade-128">Once on this screen you should see "Azure PowerShell" in the program listing, and can uninstall from there.</span></span>
