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
ms.openlocfilehash: 3dae464a876aaebc4327ac5c834a3b3ac0eb95f6
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/06/2018
ms.locfileid: "34820431"
---
# <a name="install-and-configure-azure-powershell-on-macos-and-linux"></a><span data-ttu-id="ea411-103">Установка и настройка Azure PowerShell в macOS и Linux</span><span class="sxs-lookup"><span data-stu-id="ea411-103">Install and configure Azure PowerShell on macOS and Linux</span></span>

<span data-ttu-id="ea411-104">Теперь можно установить PowerShell Core версии 6 и Azure PowerShell на платформах, отличных от Windows.</span><span class="sxs-lookup"><span data-stu-id="ea411-104">It is now possible to install PowerShell Core v6 and Azure PowerShell on non-Windows platforms.</span></span>
<span data-ttu-id="ea411-105">Процесс установки Azure PowerShell в macOS и Linux не отличается от процесса установки в Windows, но сначала нужно установить PowerShell Core версии 6.</span><span class="sxs-lookup"><span data-stu-id="ea411-105">The process of installing Azure PowerShell on macOS and Linux is not that different from Windows, however, you must first install PowerShell Core v6.</span></span>

> [!NOTE]

> <span data-ttu-id="ea411-106">Сейчас PowerShell Core версии 6 и Azure PowerShell для .NET Core реализованы в бета-версии.</span><span class="sxs-lookup"><span data-stu-id="ea411-106">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Core are still in beta.</span></span>
> <span data-ttu-id="ea411-107">Поддержка этих продуктов ограничена.</span><span class="sxs-lookup"><span data-stu-id="ea411-107">Support for these products is limited.</span></span> <span data-ttu-id="ea411-108">Если у вас возникнут проблемы или вы обнаружите ошибки, отправьте сведения об этих проблемах на сайт GitHub.</span><span class="sxs-lookup"><span data-stu-id="ea411-108">If you have problems or discover bugs, please file Issues in GitHub.</span></span>
>
> * [<span data-ttu-id="ea411-109">Проблемы, связанные с PowerShell Core версии 6</span><span class="sxs-lookup"><span data-stu-id="ea411-109">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="ea411-110">Проблемы, связанные с Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="ea411-110">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="step-1-install-powershell-core-v6"></a><span data-ttu-id="ea411-111">Шаг 1. Установка PowerShell Core версии 6</span><span class="sxs-lookup"><span data-stu-id="ea411-111">Step 1: Install PowerShell Core v6</span></span>

<span data-ttu-id="ea411-112">Процесс установки PowerShell Core версии 6 зависит от целевой операционной системы.</span><span class="sxs-lookup"><span data-stu-id="ea411-112">The process of installing PowerShell Core v6 varies depending on the target operating system.</span></span>
<span data-ttu-id="ea411-113">PowerShell Core версии 6 можно установить и в Windows, но эта статья посвящена macOS и Linux.</span><span class="sxs-lookup"><span data-stu-id="ea411-113">While it is possible to install PowerShell Core v6 on Windows, this article focuses on macOS and Linux.</span></span> <span data-ttu-id="ea411-114">Если вы хотите использовать Azure PowerShell в Windows, ознакомьтесь с разделом [Установка](./install-azurerm-ps.md) статьи для Windows.</span><span class="sxs-lookup"><span data-stu-id="ea411-114">If you want to use Azure PowerShell on Windows, see the [install](./install-azurerm-ps.md) article for Windows.</span></span>

<span data-ttu-id="ea411-115">Установка **PowerShell Core версии 6** в Linux или macOS зависит от дистрибутива Linux и версии ОС.</span><span class="sxs-lookup"><span data-stu-id="ea411-115">Installing **PowerShell Core v6** on Linux or macOS varies depending on the Linux distribution and OS version.</span></span>
<span data-ttu-id="ea411-116">Подробные инструкции можно найти в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="ea411-116">Detailed instructions can be found in the following articles:</span></span>

- [<span data-ttu-id="ea411-117">Установка PowerShell Core в macOS</span><span class="sxs-lookup"><span data-stu-id="ea411-117">Installing PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
- [<span data-ttu-id="ea411-118">Установка PowerShell Core в Linux</span><span class="sxs-lookup"><span data-stu-id="ea411-118">Installing PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="step-2-install-azure-powershell-for-net-core"></a><span data-ttu-id="ea411-119">Шаг 2. Установка Azure PowerShell для .NET Core</span><span class="sxs-lookup"><span data-stu-id="ea411-119">Step 2: Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="ea411-120">PowerShell Core версии 6 поставляется с установленным модулем PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="ea411-120">PowerShell Core v6 comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="ea411-121">Это позволяет легко установить любой модуль, опубликованный в коллекции PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ea411-121">This makes it easy to install any module that is published to the PowerShell Gallery.</span></span> <span data-ttu-id="ea411-122">Чтобы установить Azure PowerShell, откройте новый сеанс PowerShell и выполните следующую команду.</span><span class="sxs-lookup"><span data-stu-id="ea411-122">To install Azure PowerShell, open a new PowerShell session and run the following command:</span></span>

```powershell
Install-Module AzureRM.NetCore
```

## <a name="step-3-load-the-azurermnetcore-module"></a><span data-ttu-id="ea411-123">Шаг 3. Загрузка модуля AzureRM.Netcore</span><span class="sxs-lookup"><span data-stu-id="ea411-123">Step 3: Load the AzureRM.Netcore module</span></span>

<span data-ttu-id="ea411-124">После установки модуля его необходимо загрузить в сеанс PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ea411-124">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="ea411-125">Модули можно загрузить с помощью командлета `Import-Module` следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ea411-125">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module AzureRM.Netcore
Import-Module AzureRM.Profile.Netcore
```

<span data-ttu-id="ea411-126">После завершения импорта можно проверить только что установленный модуль, попытавшись войти в Azure с помощью следующей команды.</span><span class="sxs-lookup"><span data-stu-id="ea411-126">After the import completes, you can test your newly installed and module by attempting to sign into Azure using the following command:</span></span>

```powershell
Connect-AzureRmAccount
```

<span data-ttu-id="ea411-127">Приведенная выше команда должна предложить перейти по адресу `https://aka.ms/devicelogin` и ввести предоставленный код.</span><span class="sxs-lookup"><span data-stu-id="ea411-127">The above command should prompt you to go to `https://aka.ms/devicelogin` and enter the provided code.</span></span>

## <a name="available-cmdlets"></a><span data-ttu-id="ea411-128">Доступные командлеты</span><span class="sxs-lookup"><span data-stu-id="ea411-128">Available cmdlets</span></span>

<span data-ttu-id="ea411-129">Модули Azure PowerShell для .NET Standard еще находятся в разработке.</span><span class="sxs-lookup"><span data-stu-id="ea411-129">The Azure PowerShell modules for .NET Standard are still in development.</span></span> <span data-ttu-id="ea411-130">Эти модули не обеспечивают полный набор командлетов, которые доступны в версии модулей для Windows.</span><span class="sxs-lookup"><span data-stu-id="ea411-130">These modules do not provide the full set of cmdlets that are available for the Windows version of the modules.</span></span> <span data-ttu-id="ea411-131">В модулях AzureRM.Netcore реализованы следующие функции.</span><span class="sxs-lookup"><span data-stu-id="ea411-131">The following functions are implemented in AzureRM.Netcore modules:</span></span>

* <span data-ttu-id="ea411-132">Управление учетными записями</span><span class="sxs-lookup"><span data-stu-id="ea411-132">Account management</span></span>
  - <span data-ttu-id="ea411-133">Вход с помощью учетной записи Майкрософт, рабочей или учебной учетной записи или субъекта-службы с помощью Microsoft Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ea411-133">Login with Microsoft account, Organizational account, or Service Principal through Microsoft Azure Active Directory</span></span>
  - <span data-ttu-id="ea411-134">Сохранение учетных данных на диск с помощью командлета Save-AzureRmContext и загрузка сохраненных учетных данных с помощью командлета Import-AzureRmContext.</span><span class="sxs-lookup"><span data-stu-id="ea411-134">Save Credentials to disk with Save-AzureRmContext and load saved credentials using Import-AzureRmContext</span></span>
* <span data-ttu-id="ea411-135">Среда</span><span class="sxs-lookup"><span data-stu-id="ea411-135">Environment</span></span>
  - <span data-ttu-id="ea411-136">Получение различных стандартных сред Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ea411-136">Get the different out-of-box Microsoft Azure environments</span></span>
  - <span data-ttu-id="ea411-137">Добавление, настройка и удаление настроенных сред (например, сред Azure Stack или Windows Azure Pack).</span><span class="sxs-lookup"><span data-stu-id="ea411-137">Add/Set/Remove customized environments (like your Azure Stack or Windows Azure Pack environments)</span></span>
* <span data-ttu-id="ea411-138">Командлеты плоскости управления для служб Azure, использующих интерфейсы Resource Manager и интерфейсы управления службами.</span><span class="sxs-lookup"><span data-stu-id="ea411-138">Management plane cmdlets for Azure services using Resource Manager and Service Management interfaces.</span></span>
  - <span data-ttu-id="ea411-139">Виртуальная машина</span><span class="sxs-lookup"><span data-stu-id="ea411-139">Virtual Machine</span></span>
  - <span data-ttu-id="ea411-140">Служба приложений (веб-сайты)</span><span class="sxs-lookup"><span data-stu-id="ea411-140">App Service (Websites)</span></span>
  - <span data-ttu-id="ea411-141">База данных SQL</span><span class="sxs-lookup"><span data-stu-id="ea411-141">SQL Database</span></span>
  - <span data-ttu-id="ea411-142">Служба хранилища</span><span class="sxs-lookup"><span data-stu-id="ea411-142">Storage</span></span>
  - <span data-ttu-id="ea411-143">Сеть</span><span class="sxs-lookup"><span data-stu-id="ea411-143">Network</span></span>

## <a name="next-steps"></a><span data-ttu-id="ea411-144">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="ea411-144">Next Steps</span></span>

<span data-ttu-id="ea411-145">Дополнительные сведения об использовании Azure PowerShell см. в статье [Начало работы с Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="ea411-145">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
