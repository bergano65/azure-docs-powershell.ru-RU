---
title: Удаление Azure PowerShell
description: Сведения о том, как полностью удалить Azure PowerShell.
ms.date: 06/20/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 8071d6fb0e2644bb00b3fcfe8a2595e2586c5d02
ms.sourcegitcommit: 3bdbb176753e285df39d21c27ca317c000482d85
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/03/2018
ms.locfileid: "37439573"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="f07b8-103">Удаление модуля Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="f07b8-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="f07b8-104">Из этой статьи вы узнаете, как удалить предыдущую версию Azure PowerShell или полностью удалить этот модуль из системы.</span><span class="sxs-lookup"><span data-stu-id="f07b8-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="f07b8-105">Если вы решили полностью удалить Azure PowerShell, отправьте нам отзыв с помощью командлета [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="f07b8-105">If you've decided to completely uninstall the Azure PowerShell, please give us some feedback through the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span> <span data-ttu-id="f07b8-106">Если возникнет ошибка, мы будем признательны, если вы [сообщите о ней на GitHub](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="f07b8-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues).</span></span>

# <a name="uninstall-msi"></a><span data-ttu-id="f07b8-107">Удаление пакета MSI</span><span class="sxs-lookup"><span data-stu-id="f07b8-107">Uninstall MSI</span></span>

<span data-ttu-id="f07b8-108">Если вы установили Azure PowerShell с помощью пакета MSI, удалять модуль нужно через систему Windows, а не PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f07b8-108">If you installed Azure PowerShell using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>
 
| <span data-ttu-id="f07b8-109">платформа</span><span class="sxs-lookup"><span data-stu-id="f07b8-109">Platform</span></span> | <span data-ttu-id="f07b8-110">Указания</span><span class="sxs-lookup"><span data-stu-id="f07b8-110">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="f07b8-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="f07b8-111">Windows 10</span></span> | <span data-ttu-id="f07b8-112">"Пуск" > "Параметры" > "Приложения"</span><span class="sxs-lookup"><span data-stu-id="f07b8-112">Start > Settings > Apps</span></span> |
| <span data-ttu-id="f07b8-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f07b8-113">Windows 7</span></span> </br><span data-ttu-id="f07b8-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f07b8-114">Windows 8</span></span> | <span data-ttu-id="f07b8-115">"Пуск" > "Панель управления" > "Программы" > "Удаление программы"</span><span class="sxs-lookup"><span data-stu-id="f07b8-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="f07b8-116">В этом окне в списке программ вы должны увидеть модуль Azure PowerShell, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="f07b8-116">Once on this screen you should see "Azure PowerShell" in the program listing, and can uninstall from there.</span></span>

# <a name="uninstall-from-powershell"></a><span data-ttu-id="f07b8-117">Удаление с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="f07b8-117">Uninstall from PowerShell</span></span>

<span data-ttu-id="f07b8-118">Если вы установили Azure PowerShell с помощью PowerShellGet, для удаления можно использовать командлет [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="f07b8-118">If you installed Azure PowerShell using PowerShellGet, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="f07b8-119">Учтите, что `Uninstall-Module` удаляет только один модуль.</span><span class="sxs-lookup"><span data-stu-id="f07b8-119">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="f07b8-120">Чтобы полностью удалить Azure PowerShell, каждый модуль нужно удалять отдельно.</span><span class="sxs-lookup"><span data-stu-id="f07b8-120">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="f07b8-121">Удаление может усложниться, если у вас установлено несколько версий Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f07b8-121">Uninstallation can be complicated if you have multiple versions of Azure PowerShell installed.</span></span>

<span data-ttu-id="f07b8-122">Ниже приведен скрипт, с помощью которого можно полностью удалить одну версию Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f07b8-122">The following script can be used to completely remove a single version of Azure PowerShell.</span></span> <span data-ttu-id="f07b8-123">Скрипт запрашивает из коллекции PowerShell список зависимых подмодулей,</span><span class="sxs-lookup"><span data-stu-id="f07b8-123">The script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="f07b8-124">а затем удаляет правильную версию каждого подмодуля.</span><span class="sxs-lookup"><span data-stu-id="f07b8-124">Then, the script uninstalls the correct version of each submodule.</span></span>

```powershell
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

<span data-ttu-id="f07b8-125">Чтобы воспользоваться этой функцией, скопируйте и вставьте этот код в окно сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f07b8-125">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="f07b8-126">В примере ниже показано, как запустить функцию, чтобы удалить предыдущую версию Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f07b8-126">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

<span data-ttu-id="f07b8-127">Во время выполнения скрипта в окне будут отображаться имя и версия каждого удаляемого подмодуля.</span><span class="sxs-lookup"><span data-stu-id="f07b8-127">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span>

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

<span data-ttu-id="f07b8-128">Выполните эту команду для каждой версии Azure PowerShell, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="f07b8-128">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span>
