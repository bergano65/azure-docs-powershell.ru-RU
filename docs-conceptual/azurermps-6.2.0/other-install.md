---
title: Другие способы установки Azure PowerShell
description: Как установить Azure PowerShell с помощью пакета MSI или установщика веб-платформы.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 0919583d9cb05a75fae3b812eed84109be8b28aa
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323328"
---
# <a name="other-installation-methods"></a><span data-ttu-id="c47e0-103">Другие методы установки</span><span class="sxs-lookup"><span data-stu-id="c47e0-103">Other installation methods</span></span>

<span data-ttu-id="c47e0-104">В этой статье описывается, как установить Azure PowerShell с использованием MSI или установщика веб-платформы (WebPI).</span><span class="sxs-lookup"><span data-stu-id="c47e0-104">This article explains how to install Azure PowerShell using an MSI or Web Platform Installer (WebPI).</span></span> <span data-ttu-id="c47e0-105">Вы также можете запустить Azure PowerShell в контейнере Docker.</span><span class="sxs-lookup"><span data-stu-id="c47e0-105">You can also run Azure PowerShell from inside of a Docker container.</span></span> <span data-ttu-id="c47e0-106">Используйте эти способы установки только в том случае, если это необходимо для вашей системы.</span><span class="sxs-lookup"><span data-stu-id="c47e0-106">Use these installation methods only if they're necessary for your system.</span></span> <span data-ttu-id="c47e0-107">Стандартный вариант — установка Azure PowerShell через PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="c47e0-107">The canonical way to install Azure PowerShell is through PowerShellGet.</span></span> <span data-ttu-id="c47e0-108">Инструкции по установке Azure PowerShell с помощью PowerShellGet см. в [этой статье](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="c47e0-108">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-azurerm-ps.md).</span></span>

<span data-ttu-id="c47e0-109">Сведения об установке в средах Linux или macOS см. в [этом разделе](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="c47e0-109">To install on Linux or macOS environments, see [Install Azure PowerShell on macOS or Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-or-update-on-windows-using-the-web-platform-installer"></a><span data-ttu-id="c47e0-110">Установка или обновление в Windows с помощью установщика веб-платформы</span><span class="sxs-lookup"><span data-stu-id="c47e0-110">Install or update on Windows using the Web Platform Installer</span></span>

<span data-ttu-id="c47e0-111">Установка последней версии Azure PowerShell из WebPI выполняется также, как и установка предыдущих версий.</span><span class="sxs-lookup"><span data-stu-id="c47e0-111">Installing the latest Azure PowerShell from WebPI is the same as it was for previous versions.</span></span>
<span data-ttu-id="c47e0-112">Скачайте [пакет Azure PowerShell WebPI](http://aka.ms/webpi-azps) и запустите установку.</span><span class="sxs-lookup"><span data-stu-id="c47e0-112">Download the [Azure PowerShell WebPI package](http://aka.ms/webpi-azps) and start the install.</span></span>

> [!NOTE]
> <span data-ttu-id="c47e0-113">Если вы ранее установили модули Azure из коллекции PowerShell, то установщик автоматически удаляет их.</span><span class="sxs-lookup"><span data-stu-id="c47e0-113">If you have previously installed Azure modules from the PowerShell Gallery, the installer automatically removes them.</span></span> <span data-ttu-id="c47e0-114">Это облегчает использование среды за счет установки только одной версии Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c47e0-114">This simplifies your environment by ensuring that only one version of Azure PowerShell is installed.</span></span> <span data-ttu-id="c47e0-115">Но в некоторых сценариях может потребоваться установить несколько версий одновременно.</span><span class="sxs-lookup"><span data-stu-id="c47e0-115">However, there are scenarios where you may need multiple versions installed at the same time.</span></span>
>
> <span data-ttu-id="c47e0-116">Модули из коллекции PowerShell устанавливают модули в папку `$env:ProgramFiles\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="c47e0-116">PowerShell Gallery modules install modules in `$env:ProgramFiles\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="c47e0-117">А установщик WebPI устанавливает модули Azure в другую папку: `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.</span><span class="sxs-lookup"><span data-stu-id="c47e0-117">In contrast, the WebPI installer installs the Azure modules in `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.</span></span>
>
> <span data-ttu-id="c47e0-118">Если во время установки возникла ошибка, вы можете вручную удалить папки `Azure*` в папке `$env:ProgramFiles\WindowsPowerShell\Modules` и повторить попытку установки.</span><span class="sxs-lookup"><span data-stu-id="c47e0-118">If an error occurs during install, you can manually remove the `Azure*` folders in your `$env:ProgramFiles\WindowsPowerShell\Modules` folder, and try the installation again.</span></span>

<span data-ttu-id="c47e0-119">По завершении установки ваш параметр `$env:PSModulePath` должен включать каталоги, содержащие командлеты Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c47e0-119">Once the installation completes, your `$env:PSModulePath` setting should include the directories containing the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="c47e0-120">Используйте следующую команду, чтобы проверить, правильно ли установлена среда Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c47e0-120">The following command can be used to verify that the Azure PowerShell is installed properly:</span></span>

```powershell
# To make sure the Azure PowerShell module is available after you install
Get-Module -ListAvailable Azure* | Select-Object Name, Version, Path
```

> [!NOTE]
> <span data-ttu-id="c47e0-121">При установке с помощью WebPI может возникать известная проблема.</span><span class="sxs-lookup"><span data-stu-id="c47e0-121">There is a known issue that can occur when installing from WebPI.</span></span> <span data-ttu-id="c47e0-122">Если из-за установки обновлений системы или других компонентов потребуется перезагрузка компьютера, это может привести к исключению из `$env:PSModulePath` пути установки Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c47e0-122">If your computer requires a restart due to system updates or other installations, it may cause updates to `$env:PSModulePath` to fail to include the path where Azure PowerShell is installed.</span></span>

<span data-ttu-id="c47e0-123">При попытке загрузки или выполнения командлетов после установки может появиться следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="c47e0-123">When attempting to load or execute cmdlets after installation, you can receive the following error message:</span></span>

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

<span data-ttu-id="c47e0-124">Эту ошибку можно исправить при перезагрузке компьютера или импорте модуля, используя полный путь.</span><span class="sxs-lookup"><span data-stu-id="c47e0-124">This error can be corrected by restarting the machine or importing the module using the fully qualified path.</span></span>

```powershell
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="c47e0-125">Установка или обновление в Windows с помощью пакета MSI</span><span class="sxs-lookup"><span data-stu-id="c47e0-125">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="c47e0-126">Azure PowerShell можно установить с помощью MSI-файла из [GitHub](https://aka.ms/azps-release).</span><span class="sxs-lookup"><span data-stu-id="c47e0-126">Azure PowerShell can be installed using the MSI file available from [GitHub](https://aka.ms/azps-release).</span></span> <span data-ttu-id="c47e0-127">Если вы устанавливали предыдущие версии модулей Azure, то установщик автоматически удаляет их.</span><span class="sxs-lookup"><span data-stu-id="c47e0-127">If you have installed previous versions of Azure modules, the installer automatically removes them.</span></span> <span data-ttu-id="c47e0-128">Пакет MSI устанавливает модули в папку `$env:ProgramFiles\WindowsPowerShell\Modules`, но не создает папки для определенных версий.</span><span class="sxs-lookup"><span data-stu-id="c47e0-128">The MSI package installs modules in `$env:ProgramFiles\WindowsPowerShell\Modules` but does not create version-specific folders.</span></span>

## <a name="run-in-a-docker-container"></a><span data-ttu-id="c47e0-129">Запуск в контейнере Docker</span><span class="sxs-lookup"><span data-stu-id="c47e0-129">Run in a Docker container</span></span>

<span data-ttu-id="c47e0-130">Мы поддерживаем набор образов Docker, предварительно настроенный с помощью Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c47e0-130">We maintain a set of Docker images preconfigured with Azure PowerShell.</span></span> <span data-ttu-id="c47e0-131">Доступны контейнеры двух типов: в одних используется стандартная версия PowerShell в среде Windows, а в других — версия PowerShell Core в среде Windows или Linux.</span><span class="sxs-lookup"><span data-stu-id="c47e0-131">There are two types of containers available: Those running traditional PowerShell on Windows, and a container running PowerShell Core on either Windows or Linux.</span></span>

| <span data-ttu-id="c47e0-132">Среда</span><span class="sxs-lookup"><span data-stu-id="c47e0-132">Environment</span></span> | <span data-ttu-id="c47e0-133">Образ Docker</span><span class="sxs-lookup"><span data-stu-id="c47e0-133">Docker image</span></span> |
|-------------|--------------|
| <span data-ttu-id="c47e0-134">PowerShell в среде Windows</span><span class="sxs-lookup"><span data-stu-id="c47e0-134">PowerShell on Windows</span></span> | [<span data-ttu-id="c47e0-135">azuresdk/azure-powershell</span><span class="sxs-lookup"><span data-stu-id="c47e0-135">azuresdk/azure-powershell</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| <span data-ttu-id="c47e0-136">PowerShell Core в среде Windows</span><span class="sxs-lookup"><span data-stu-id="c47e0-136">PowerShell Core on Windows</span></span> | [<span data-ttu-id="c47e0-137">azuresdk/azure-powershell-core:nanoserver</span><span class="sxs-lookup"><span data-stu-id="c47e0-137">azuresdk/azure-powershell-core:nanoserver</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| <span data-ttu-id="c47e0-138">PowerShell Core в среде Linux</span><span class="sxs-lookup"><span data-stu-id="c47e0-138">PowerShell Core on Linux</span></span> | [<span data-ttu-id="c47e0-139">azuresdk/azure-powershell-core:latest</span><span class="sxs-lookup"><span data-stu-id="c47e0-139">azuresdk/azure-powershell-core:latest</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

<span data-ttu-id="c47e0-140">Для запуска любого из этих контейнеров используйте `docker run -it $ImageName`, чтобы получить интерактивный терминал.</span><span class="sxs-lookup"><span data-stu-id="c47e0-140">To run any of these containers, you use `docker run -it $ImageName` to get an interactive terminal.</span></span> <span data-ttu-id="c47e0-141">Например, чтобы запустить контейнер с PowerShell Core в среде Linux, используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="c47e0-141">For example, to run the PowerShell Core on Linux container, use:</span></span>

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> <span data-ttu-id="c47e0-142">Чтобы запустить контейнер Windows в Docker, в качестве ОС узла должна использоваться ОС Windows, а Docker необходимо настроить для запуска контейнеров Windows.</span><span class="sxs-lookup"><span data-stu-id="c47e0-142">To run a Windows container in Docker, your host OS must be Windows and Docker must be set to run Windows containers.</span></span> <span data-ttu-id="c47e0-143">Дополнительные сведения о переключении между средами Windows и Linux в Docker см. в документации по Docker [о переключении между контейнерами Windows и Linux](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span><span class="sxs-lookup"><span data-stu-id="c47e0-143">To learn about switching between Windows and Linux environments in Docker, see the Docker documentation [Switch between Windows and Linux containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span></span>