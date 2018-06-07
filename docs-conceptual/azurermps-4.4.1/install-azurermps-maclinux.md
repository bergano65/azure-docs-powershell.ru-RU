---
title: Установка и настройка Azure PowerShell в macOS и Linux | Документация Майкрософт
description: Как установить и настроить Azure PowerShell для первого использования в macOS и Linux.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/12/2018
ms.openlocfilehash: 18f07d3eebcce74988a02b78f2cc85f7663ed225
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/06/2018
ms.locfileid: "34821910"
---
# <a name="install-and-configure-azure-powershell-on-macos-and-linux"></a><span data-ttu-id="e3d2a-103">Установка и настройка Azure PowerShell в macOS и Linux</span><span class="sxs-lookup"><span data-stu-id="e3d2a-103">Install and configure Azure PowerShell on macOS and Linux</span></span>

<span data-ttu-id="e3d2a-104">Теперь можно установить PowerShell Core версии 6 и Azure PowerShell на платформах, отличных от Windows.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-104">It is now possible to install PowerShell Core v6 and Azure PowerShell on non-Windows platforms.</span></span>
<span data-ttu-id="e3d2a-105">Процесс установки Azure PowerShell в macOS и Linux не отличается от процесса установки в Windows, но сначала нужно установить PowerShell Core версии 6.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-105">The process of installing Azure PowerShell on macOS and Linux is not that different from Windows, however, you must first install PowerShell Core v6.</span></span>

> [!NOTE]

> <span data-ttu-id="e3d2a-106">Сейчас PowerShell Core версии 6 и Azure PowerShell для .NET Core реализованы в бета-версии.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-106">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Core are still in beta.</span></span>
> <span data-ttu-id="e3d2a-107">Поддержка этих продуктов ограничена.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-107">Support for these products is limited.</span></span> <span data-ttu-id="e3d2a-108">Если у вас возникнут проблемы или вы обнаружите ошибки, отправьте сведения об этих проблемах на сайт GitHub.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-108">If you have problems or discover bugs, please file Issues in GitHub.</span></span>
>
> * [<span data-ttu-id="e3d2a-109">Проблемы, связанные с PowerShell Core версии 6</span><span class="sxs-lookup"><span data-stu-id="e3d2a-109">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="e3d2a-110">Проблемы, связанные с Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="e3d2a-110">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="step-1-install-powershell-core-v6"></a><span data-ttu-id="e3d2a-111">Шаг 1. Установка PowerShell Core версии 6</span><span class="sxs-lookup"><span data-stu-id="e3d2a-111">Step 1: Install PowerShell Core v6</span></span>

<span data-ttu-id="e3d2a-112">Процесс установки PowerShell Core версии 6 зависит от целевой операционной системы.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-112">The process of installing PowerShell Core v6 on varies depending on the target operating system.</span></span>
<span data-ttu-id="e3d2a-113">PowerShell Core версии 6 можно установить и в Windows, но эта статья посвящена macOS и Linux.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-113">While it is possible to install PowerShell Core v6 on Windows, this article focuses on macOS and Linux.</span></span> <span data-ttu-id="e3d2a-114">Если вы хотите использовать Azure PowerShell в Windows, ознакомьтесь с разделом [Установка](./install-azurerm-ps.md) статьи для Windows.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-114">If you want to use Azure PowerShell on Windows, see the [install](./install-azurerm-ps.md) article for Windows.</span></span>

<span data-ttu-id="e3d2a-115">Установка **PowerShell Core версии 6** в Linux или macOS зависит от дистрибутива Linux и версии ОС.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-115">Installing **PowerShell Core v6** on Linux or macOS varies depending on the Linux distribution and OS version.</span></span>
<span data-ttu-id="e3d2a-116">Подробные инструкции можно найти в следующей статье:</span><span class="sxs-lookup"><span data-stu-id="e3d2a-116">Detailed instructions can be found in the following article:</span></span>

- [<span data-ttu-id="e3d2a-117">Установка PowerShell Core в macOS и Linux</span><span class="sxs-lookup"><span data-stu-id="e3d2a-117">Installing PowerShell Core on macOS and Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos-and-linux)

## <a name="step-2-install-azure-powershell-for-net-core"></a><span data-ttu-id="e3d2a-118">Шаг 2. Установка Azure PowerShell для .NET Core</span><span class="sxs-lookup"><span data-stu-id="e3d2a-118">Step 2: Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="e3d2a-119">PowerShell Core версии 6 поставляется с установленным модулем PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-119">PowerShell Core v6 comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="e3d2a-120">Это позволяет легко установить любой модуль, опубликованный в коллекции PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-120">This makes it easy to install any module that is published to the PowerShell Gallery.</span></span> <span data-ttu-id="e3d2a-121">Чтобы установить Azure PowerShell, откройте новый сеанс PowerShell и выполните следующую команду.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-121">To install Azure PowerShell, open a new PowerShell session and run the following command:</span></span>

```powershell
Install-Module AzureRM.NetCore
```

## <a name="step-3-load-the-azurermnetcore-module"></a><span data-ttu-id="e3d2a-122">Шаг 3. Загрузка модуля AzureRM.Netcore</span><span class="sxs-lookup"><span data-stu-id="e3d2a-122">Step 3: Load the AzureRM.Netcore module</span></span>

<span data-ttu-id="e3d2a-123">После установки модуля его необходимо загрузить в сеанс PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-123">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="e3d2a-124">Модули можно загрузить с помощью командлета `Import-Module` следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e3d2a-124">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module AzureRM.Netcore
Import-Module AzureRM.Profile.Netcore
```

<span data-ttu-id="e3d2a-125">После завершения импорта можно проверить только что установленный модуль, попытавшись войти в Azure с помощью следующей команды.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-125">After the import completes, you can test your newly installed and module by attempting to sign into Azure using the following command:</span></span>

```powershell
Login-AzureRMAccount
```

<span data-ttu-id="e3d2a-126">Приведенная выше команда должна предложить перейти по адресу `https://aka.ms/devicelogin` и ввести предоставленный код.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-126">The above command should prompt you to go to `https://aka.ms/devicelogin` and enter the provided code.</span></span>

## <a name="available-cmdlets"></a><span data-ttu-id="e3d2a-127">Доступные командлеты</span><span class="sxs-lookup"><span data-stu-id="e3d2a-127">Available cmdlets</span></span>

<span data-ttu-id="e3d2a-128">Модули Azure PowerShell для .NET Standard еще находятся в разработке.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-128">The Azure PowerShell modules for .NET Standard are still in development.</span></span> <span data-ttu-id="e3d2a-129">Эти модули не обеспечивают полный набор командлетов, которые доступны в версии модулей для Windows.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-129">These modules do not provide the full set of cmdlets that are available for the Windows version of the modules.</span></span> <span data-ttu-id="e3d2a-130">В модулях AzureRM.Netcore реализованы следующие функции.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-130">The following functions are implemented in AzureRM.Netcore modules:</span></span>

* <span data-ttu-id="e3d2a-131">Управление учетными записями</span><span class="sxs-lookup"><span data-stu-id="e3d2a-131">Account management</span></span>
  - <span data-ttu-id="e3d2a-132">Вход с помощью учетной записи Майкрософт, рабочей или учебной учетной записи или субъекта-службы с помощью Microsoft Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-132">Login with Microsoft account, Organizational account, or Service Principal through Microsoft Azure Active Directory</span></span>
  - <span data-ttu-id="e3d2a-133">Сохранение учетных данных на диск с помощью командлета Save-AzureRmContext и загрузка сохраненных учетных данных с помощью командлета Import-AzureRmContext.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-133">Save Credentials to disk with Save-AzureRmContext and load saved credentials using Import-AzureRmContext</span></span>
* <span data-ttu-id="e3d2a-134">Среда</span><span class="sxs-lookup"><span data-stu-id="e3d2a-134">Environment</span></span>
  - <span data-ttu-id="e3d2a-135">Получение различных стандартных сред Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-135">Get the different out-of-box Microsoft Azure environments</span></span>
  - <span data-ttu-id="e3d2a-136">Добавление, настройка и удаление настроенных сред (например, сред Azure Stack или Windows Azure Pack).</span><span class="sxs-lookup"><span data-stu-id="e3d2a-136">Add/Set/Remove customized environments (like your Azure Stack or Windows Azure Pack environments)</span></span>
* <span data-ttu-id="e3d2a-137">Командлеты плоскости управления для служб Azure, использующих интерфейсы Resource Manager и интерфейсы управления службами.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-137">Management plane cmdlets for Azure services using Resource Manager and Service Management interfaces.</span></span>
  - <span data-ttu-id="e3d2a-138">Виртуальная машина</span><span class="sxs-lookup"><span data-stu-id="e3d2a-138">Virtual Machine</span></span>
  - <span data-ttu-id="e3d2a-139">Служба приложений (веб-сайты)</span><span class="sxs-lookup"><span data-stu-id="e3d2a-139">App Service (Websites)</span></span>
  - <span data-ttu-id="e3d2a-140">База данных SQL</span><span class="sxs-lookup"><span data-stu-id="e3d2a-140">SQL Database</span></span>
  - <span data-ttu-id="e3d2a-141">Служба хранилища</span><span class="sxs-lookup"><span data-stu-id="e3d2a-141">Storage</span></span>
  - <span data-ttu-id="e3d2a-142">Сеть</span><span class="sxs-lookup"><span data-stu-id="e3d2a-142">Network</span></span>

## <a name="next-steps"></a><span data-ttu-id="e3d2a-143">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="e3d2a-143">Next Steps</span></span>

<span data-ttu-id="e3d2a-144">Дополнительные сведения об использовании Azure PowerShell см. в статье [Начало работы с Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="e3d2a-144">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
