---
title: Другие методы установки Azure PowerShell | Документация Майкрософт
description: Как установить Azure PowerShell с помощью пакета MSI или установщика веб-платформы.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/06/2017
ms.openlocfilehash: 8b7d9631581046800c772d7bc6f654bb6a9eb483
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/23/2018
---
# <a name="other-installation-methods"></a><span data-ttu-id="0df20-103">Другие методы установки</span><span class="sxs-lookup"><span data-stu-id="0df20-103">Other installation methods</span></span>

<span data-ttu-id="0df20-104">Azure PowerShell можно установить разными способами.</span><span class="sxs-lookup"><span data-stu-id="0df20-104">Azure PowerShell has multiple installation methods.</span></span> <span data-ttu-id="0df20-105">Предпочтительным является использование PowerShellGet с коллекцией PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0df20-105">Using PowerShellGet with the PowerShell Gallery is the preferred method.</span></span> <span data-ttu-id="0df20-106">Azure PowerShell можно установить в Windows с помощью установщика веб-платформы (WebPI) или с помощью MSI-файла из GitHub.</span><span class="sxs-lookup"><span data-stu-id="0df20-106">Azure PowerShell can be installed on Windows using the Web Platform Installer (WebPI) or by using the MSI file available from GitHub.</span></span> <span data-ttu-id="0df20-107">Также можно установить Azure PowerShell в контейнер Docker.</span><span class="sxs-lookup"><span data-stu-id="0df20-107">Azure PowerShell can also be installed in a Docker container.</span></span>

## <a name="install-on-windows-using-the-web-platform-installer"></a><span data-ttu-id="0df20-108">Установка в Windows с помощью установщика веб-платформы</span><span class="sxs-lookup"><span data-stu-id="0df20-108">Install on Windows using the Web Platform Installer</span></span>

<span data-ttu-id="0df20-109">Установка последней версии Azure PowerShell из WebPI выполняется также, как и установка предыдущих версий.</span><span class="sxs-lookup"><span data-stu-id="0df20-109">Installing the latest Azure PowerShell from WebPI is the same as it was for previous versions.</span></span>
<span data-ttu-id="0df20-110">Скачайте [пакет Azure PowerShell WebPI](http://aka.ms/webpi-azps) и запустите установку.</span><span class="sxs-lookup"><span data-stu-id="0df20-110">Download the [Azure PowerShell WebPI package](http://aka.ms/webpi-azps) and start the install.</span></span>

> [!NOTE]
> <span data-ttu-id="0df20-111">Если вы ранее установили модули Azure из коллекции PowerShell, то установщик автоматически удаляет их.</span><span class="sxs-lookup"><span data-stu-id="0df20-111">If you have previously installed Azure modules from the PowerShell Gallery, the installer automatically removes them.</span></span> <span data-ttu-id="0df20-112">Это облегчает использование среды за счет установки только одной версии Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0df20-112">This simplifies your environment by ensuring that only one version of Azure PowerShell is installed.</span></span> <span data-ttu-id="0df20-113">Но в некоторых сценариях может потребоваться установить несколько версий одновременно.</span><span class="sxs-lookup"><span data-stu-id="0df20-113">However, there are scenarios where you may need multiple versions installed at the same time.</span></span>
>
> <span data-ttu-id="0df20-114">Модули из коллекции PowerShell устанавливают модули в папку `$env:ProgramFiles\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="0df20-114">PowerShell Gallery modules install modules in `$env:ProgramFiles\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="0df20-115">А установщик WebPI устанавливает модули Azure в другую папку: `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.</span><span class="sxs-lookup"><span data-stu-id="0df20-115">In contrast, the WebPI installer installs the Azure modules in `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.</span></span>
>
> <span data-ttu-id="0df20-116">Если во время установки возникла ошибка, вы можете можно вручную удалить папки Azure\* в каталоге `$env:ProgramFiles\WindowsPowerShell\Modules` и повторить попытку установки.</span><span class="sxs-lookup"><span data-stu-id="0df20-116">If an error occurs during install, you can manually remove the Azure\* folders in your `$env:ProgramFiles\WindowsPowerShell\Modules` folder, and try the installation again.</span></span>

<span data-ttu-id="0df20-117">По завершении установки ваш параметр `$env:PSModulePath` должен включать каталоги, содержащие командлеты Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0df20-117">Once the installation completes, your `$env:PSModulePath` setting should include the directories containing the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="0df20-118">Используйте следующую команду, чтобы убедиться, что среда Azure PowerShell установлена правильно.</span><span class="sxs-lookup"><span data-stu-id="0df20-118">The following command can be used to verify that the Azure PowerShell is installed properly.</span></span>

```powershell
# To make sure the Azure PowerShell module is available after you install
Get-Module -ListAvailable Azure* | Select-Object Name, Version, Path
```

> [!NOTE]
> <span data-ttu-id="0df20-119">При установке с помощью WebPI может возникать известная проблема.</span><span class="sxs-lookup"><span data-stu-id="0df20-119">There is a known issue that can occur when installing from WebPI.</span></span> <span data-ttu-id="0df20-120">Если из-за установки обновлений системы или других компонентов потребуется перезагрузка компьютера, это может привести к исключению из `$env:PSModulePath` пути установки Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0df20-120">If your computer requires a restart due to system updates or other installations, it may cause updates to `$env:PSModulePath` to fail to include the path where Azure PowerShell is installed.</span></span>

<span data-ttu-id="0df20-121">При попытке загрузки или выполнения командлетов после установки может появиться следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="0df20-121">When attempting to load or execute cmdlets after installation, you can receive the following error message:</span></span>

```
PS C:\> Connect-AzureRmAccount
Connect-AzureRmAccount : The term 'Connect-AzureRmAccount' is not recognized as the name of a cmdlet,
function, script file, or operable program. Check the spelling of the name, or if a path was
included, verify that the path is correct and try again.
At line:1 char:1
+ Connect-AzureRmAccount
+ ~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (Connect-AzureRmAccount:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
```

<span data-ttu-id="0df20-122">Эту ошибку можно исправить при перезагрузке компьютера или импорте модуля, используя полный путь.</span><span class="sxs-lookup"><span data-stu-id="0df20-122">This error can be corrected by restarting the machine or importing the module using the fully qualified path.</span></span> <span data-ttu-id="0df20-123">Например: </span><span class="sxs-lookup"><span data-stu-id="0df20-123">For example:</span></span>

```powershell
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-on-windows-using-the-msi-package"></a><span data-ttu-id="0df20-124">Установка в Windows с помощью пакета MSI</span><span class="sxs-lookup"><span data-stu-id="0df20-124">Install on Windows using the MSI Package</span></span>

<span data-ttu-id="0df20-125">Azure PowerShell можно установить с помощью MSI-файла из [GitHub](https://aka.ms/azps-release).</span><span class="sxs-lookup"><span data-stu-id="0df20-125">Azure PowerShell can be installed using the MSI file available from [GitHub](https://aka.ms/azps-release).</span></span> <span data-ttu-id="0df20-126">Если вы устанавливали предыдущие версии модулей Azure, то установщик автоматически удаляет их.</span><span class="sxs-lookup"><span data-stu-id="0df20-126">If you have installed previous versions of Azure modules, the installer automatically removes them.</span></span> <span data-ttu-id="0df20-127">Пакет MSI устанавливает модули в папку `$env:ProgramFiles\WindowsPowerShell\Modules`, но не создает папки для определенных версий.</span><span class="sxs-lookup"><span data-stu-id="0df20-127">The MSI package installs modules in `$env:ProgramFiles\WindowsPowerShell\Modules` but does not create version-specific folders.</span></span>

## <a name="install-in-a-docker-container"></a><span data-ttu-id="0df20-128">Установка в контейнер Docker</span><span class="sxs-lookup"><span data-stu-id="0df20-128">Install in a Docker container</span></span>

<span data-ttu-id="0df20-129">Мы поддерживаем образ Docker, предварительно настроенный с помощью Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0df20-129">We maintain a Docker image preconfigured with Azure PowerShell.</span></span>

<span data-ttu-id="0df20-130">Запустите контейнер с помощью команды `docker run`.</span><span class="sxs-lookup"><span data-stu-id="0df20-130">Run the container with `docker run`.</span></span>

```powershell
docker run azuresdk/azure-powershell
```

<span data-ttu-id="0df20-131">Кроме того, мы поддерживаем подмножество командлетов в виде контейнера PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="0df20-131">In addition, we maintain a subset of cmdlets as a PowerShell Core container.</span></span>

<span data-ttu-id="0df20-132">Для платформ Mac и Linux используйте образ `latest`.</span><span class="sxs-lookup"><span data-stu-id="0df20-132">For Mac/Linux, use the `latest` image.</span></span>

```bash
docker run azuresdk/azure-powershell-core:latest
```

<span data-ttu-id="0df20-133">Для платформы Windows используйте образ `nanoserver`.</span><span class="sxs-lookup"><span data-stu-id="0df20-133">For Windows, use the `nanoserver` image.</span></span>

```powershell
docker run azuresdk/azure-powershell-core:nanoserver
```

<span data-ttu-id="0df20-134">Azure PowerShell устанавливается в образ с помощью `Install-Module` из [коллекции PowerShell](https://www.powershellgallery.com/).</span><span class="sxs-lookup"><span data-stu-id="0df20-134">Azure PowerShell is installed on the image via `Install-Module` from the [PowerShell Gallery](https://www.powershellgallery.com/).</span></span>