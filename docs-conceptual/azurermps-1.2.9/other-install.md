---
title: Другие методы установки Azure PowerShell | Документация Майкрософт
description: Как установить Azure PowerShell с помощью пакета MSI или установщика веб-платформы.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/06/2017
ms.openlocfilehash: 7e59a5188dee3801a1305a693b2df8af63425eb5
ms.sourcegitcommit: 4afdba3cd7e1d348876ce59f3503fdcd258f79ab
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/15/2018
ms.locfileid: "51575082"
---
# <a name="other-installation-methods"></a><span data-ttu-id="4f026-103">Другие методы установки</span><span class="sxs-lookup"><span data-stu-id="4f026-103">Other installation methods</span></span>

<span data-ttu-id="4f026-104">Azure PowerShell можно установить разными способами.</span><span class="sxs-lookup"><span data-stu-id="4f026-104">Azure PowerShell has multiple installation methods.</span></span> <span data-ttu-id="4f026-105">Предпочтительным является использование PowerShellGet с коллекцией PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4f026-105">Using PowerShellGet with the PowerShell Gallery is the preferred method.</span></span> <span data-ttu-id="4f026-106">Azure PowerShell можно установить в Windows с помощью установщика веб-платформы (WebPI) или с помощью MSI-файла из GitHub.</span><span class="sxs-lookup"><span data-stu-id="4f026-106">Azure PowerShell can be installed on Windows using the Web Platform Installer (WebPI) or by using the MSI file available from GitHub.</span></span>
 
## <a name="install-on-windows-using-the-web-platform-installer"></a><span data-ttu-id="4f026-107">Установка в Windows с помощью установщика веб-платформы</span><span class="sxs-lookup"><span data-stu-id="4f026-107">Install on Windows using the Web Platform Installer</span></span>

<span data-ttu-id="4f026-108">Установка последней версии Azure PowerShell из WebPI выполняется также, как и установка предыдущих версий.</span><span class="sxs-lookup"><span data-stu-id="4f026-108">Installing the latest Azure PowerShell from WebPI is the same as it was for previous versions.</span></span>
<span data-ttu-id="4f026-109">Скачайте [пакет Azure PowerShell WebPI](http://aka.ms/webpi-azps) и запустите установку.</span><span class="sxs-lookup"><span data-stu-id="4f026-109">Download the [Azure PowerShell WebPI package](http://aka.ms/webpi-azps) and start the install.</span></span>

> [!NOTE]
> <span data-ttu-id="4f026-110">Если вы ранее установили модули Azure из коллекции PowerShell, то установщик автоматически удаляет их.</span><span class="sxs-lookup"><span data-stu-id="4f026-110">If you have previously installed Azure modules from the PowerShell Gallery, the installer automatically removes them.</span></span> <span data-ttu-id="4f026-111">Это облегчает использование среды за счет установки только одной версии Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4f026-111">This simplifies your environment by ensuring that only one version of Azure PowerShell is installed.</span></span> <span data-ttu-id="4f026-112">Но в некоторых сценариях может потребоваться установить несколько версий одновременно.</span><span class="sxs-lookup"><span data-stu-id="4f026-112">However, there are scenarios where you may need multiple versions installed at the same time.</span></span>
>
> <span data-ttu-id="4f026-113">Модули из коллекции PowerShell устанавливают модули в папку `$env:ProgramFiles\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="4f026-113">PowerShell Gallery modules install modules in `$env:ProgramFiles\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="4f026-114">А установщик WebPI устанавливает модули Azure в другую папку: `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.</span><span class="sxs-lookup"><span data-stu-id="4f026-114">In contrast, the WebPI installer installs the Azure modules in `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.</span></span>
>
> <span data-ttu-id="4f026-115">Если во время установки возникла ошибка, вы можете можно вручную удалить папки Azure\* в папке `$env:ProgramFiles\WindowsPowerShell\Modules` и повторить попытку установки.</span><span class="sxs-lookup"><span data-stu-id="4f026-115">If an error occurs during install, you can manually remove the Azure\* folders in your `$env:ProgramFiles\WindowsPowerShell\Modules` folder, and try the installation again.</span></span>

<span data-ttu-id="4f026-116">По завершении установки ваш параметр `$env:PSModulePath` должен включать каталоги, содержащие командлеты Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4f026-116">Once the installation completes, your `$env:PSModulePath` setting should include the directories containing the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="4f026-117">Используйте следующую команду, чтобы убедиться, что среда Azure PowerShell установлена правильно.</span><span class="sxs-lookup"><span data-stu-id="4f026-117">The following command can be used to verify that the Azure PowerShell is installed properly.</span></span>

```powershell-interactive
# To make sure the Azure PowerShell module is available after you install
Get-Module -ListAvailable Azure* | Select-Object Name, Version, Path
```

> [!NOTE]
> <span data-ttu-id="4f026-118">При установке с помощью WebPI может возникать известная проблема.</span><span class="sxs-lookup"><span data-stu-id="4f026-118">There is a known issue that can occur when installing from WebPI.</span></span> <span data-ttu-id="4f026-119">Если из-за установки обновлений системы или других компонентов потребуется перезагрузка компьютера, это может привести к исключению из `$env:PSModulePath` пути установки Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4f026-119">If your computer requires a restart due to system updates or other installations, it may cause updates to `$env:PSModulePath` to fail to include the path where Azure PowerShell is installed.</span></span>

<span data-ttu-id="4f026-120">При попытке загрузки или выполнения командлетов после установки может появиться следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="4f026-120">When attempting to load or execute cmdlets after installation, you can receive the following error message:</span></span>

```output
PS C:\> Login-AzureRmAccount
Login-AzureRmAccount : The term 'Login-AzureRmAccount' is not recognized as the name of a cmdlet,
function, script file, or operable program. Check the spelling of the name, or if a path was
included, verify that the path is correct and try again.
At line:1 char:1
+ Login-AzureRmAccount
+ ~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (Login-AzureRmAccount:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
```

<span data-ttu-id="4f026-121">Эту ошибку можно исправить при перезагрузке компьютера или импорте модуля, используя полный путь.</span><span class="sxs-lookup"><span data-stu-id="4f026-121">This error can be corrected by restarting the machine or importing the module using the fully qualified path.</span></span> <span data-ttu-id="4f026-122">Например: </span><span class="sxs-lookup"><span data-stu-id="4f026-122">For example:</span></span>

```powershell-interactive
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-on-windows-using-the-msi-package"></a><span data-ttu-id="4f026-123">Установка в Windows с помощью пакета MSI</span><span class="sxs-lookup"><span data-stu-id="4f026-123">Install on Windows using the MSI Package</span></span>

<span data-ttu-id="4f026-124">Azure PowerShell можно установить с помощью MSI-файла из [GitHub](https://github.com/Azure/azure-powershell/releases/latest).</span><span class="sxs-lookup"><span data-stu-id="4f026-124">Azure PowerShell can be installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/latest).</span></span> <span data-ttu-id="4f026-125">Если вы устанавливали предыдущие версии модулей Azure, то установщик автоматически удаляет их.</span><span class="sxs-lookup"><span data-stu-id="4f026-125">If you have installed previous versions of Azure modules, the installer automatically removes them.</span></span> <span data-ttu-id="4f026-126">Пакет MSI устанавливает модули в папку `$env:ProgramFiles\WindowsPowerShell\Modules`, но не создает папки для определенных версий.</span><span class="sxs-lookup"><span data-stu-id="4f026-126">The MSI package installs modules in `$env:ProgramFiles\WindowsPowerShell\Modules` but does not create version-specific folders.</span></span>

