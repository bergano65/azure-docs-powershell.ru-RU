---
title: "Установка и настройка Azure PowerShell в macOS и Linux | Документация Майкрософт"
description: "Как установить и настроить Azure PowerShell для первого использования в macOS и Linux."
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/06/2017
ms.openlocfilehash: 94b39c18acaca7a4b17b5207feed025442665acc
ms.sourcegitcommit: 202ec2df66c40a60f47ea06b30a6701ad444d229
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2017
---
# <a name="install-and-configure-azure-powershell-on-macos-and-linux"></a><span data-ttu-id="c294d-103">Установка и настройка Azure PowerShell в macOS и Linux</span><span class="sxs-lookup"><span data-stu-id="c294d-103">Install and configure Azure PowerShell on macOS and Linux</span></span>

<span data-ttu-id="c294d-104">Теперь можно установить PowerShell 6 (бета-версия) и Azure PowerShell на платформах, отличных от Windows.</span><span class="sxs-lookup"><span data-stu-id="c294d-104">It is now possible to install PowerShell 6 (beta) and Azure PowerShell on non-Windows platforms.</span></span>
<span data-ttu-id="c294d-105">Процесс установки Azure PowerShell в macOS и Linux не отличается от процесса установки в Windows, однако необходимо сначала установить PowerShell 6 (бета-версия).</span><span class="sxs-lookup"><span data-stu-id="c294d-105">The process of installing Azure PowerShell on macOS and Linux is not that different from Windows, however, you must first install PowerShell 6 (beta).</span></span>

> [!NOTE]

> <span data-ttu-id="c294d-106">В настоящее время PowerShell 6 (бета-версия) и Azure PowerShell для .NET Core находятся на этапе бета-версии.</span><span class="sxs-lookup"><span data-stu-id="c294d-106">At this time, both PowerShell 6 (beta) and Azure PowerShell for .NET Core are still in beta.</span></span>
> <span data-ttu-id="c294d-107">Поддержка этих продуктов ограничена.</span><span class="sxs-lookup"><span data-stu-id="c294d-107">Support for these products is limited.</span></span> <span data-ttu-id="c294d-108">Если у вас возникнут проблемы или вы обнаружите ошибки, отправьте сведения об этих проблемах на сайт GitHub.</span><span class="sxs-lookup"><span data-stu-id="c294d-108">If you have problems or discover bugs, please file Issues in GitHub.</span></span>
>
> * [<span data-ttu-id="c294d-109">Проблемы, связанные с PowerShell 6 (бета-версия)</span><span class="sxs-lookup"><span data-stu-id="c294d-109">Issues for PowerShell 6 (beta)</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="c294d-110">Проблемы, связанные с Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="c294d-110">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="step-1-install-powershell-6-beta"></a><span data-ttu-id="c294d-111">Шаг 1. Установка PowerShell 6 (бета-версия)</span><span class="sxs-lookup"><span data-stu-id="c294d-111">Step 1: Install PowerShell 6 (beta)</span></span>

<span data-ttu-id="c294d-112">Процесс установки PowerShell 6 (бета-версия) зависит от целевой операционной системы.</span><span class="sxs-lookup"><span data-stu-id="c294d-112">The process of installing PowerShell 6 (beta) on varies depending on the target operating system.</span></span>
<span data-ttu-id="c294d-113">Хотя PowerShell 6 (бета-версия) можно установить в Windows, эта статья посвящена macOS и Linux.</span><span class="sxs-lookup"><span data-stu-id="c294d-113">While it is possible to install PowerShell 6 (beta) on Windows, this article focuses on macOS and Linux.</span></span> <span data-ttu-id="c294d-114">Если вы хотите использовать Azure PowerShell в Windows, ознакомьтесь с разделом [Установка](./install-azurerm-ps.md) статьи для Windows.</span><span class="sxs-lookup"><span data-stu-id="c294d-114">If you want to use Azure PowerShell on Windows, see the [install](./install-azurerm-ps.md) article for Windows.</span></span>

<span data-ttu-id="c294d-115">Чтобы установить **PowerShell 6** (бета-версия) в Linux или macOS, необходимо:</span><span class="sxs-lookup"><span data-stu-id="c294d-115">To install **PowerShell 6** (beta) on Linux or macOS, you need to:</span></span>

1. <span data-ttu-id="c294d-116">получить PowerShell для определенного типа и версии операционной системы из [GitHub](https://github.com/powershell/powershell#get-powershell);</span><span class="sxs-lookup"><span data-stu-id="c294d-116">Get PowerShell for the specific OS and version, from [GitHub](https://github.com/powershell/powershell#get-powershell)</span></span>
2. <span data-ttu-id="c294d-117">выполнить инструкции по установке.</span><span class="sxs-lookup"><span data-stu-id="c294d-117">Follow the installation instructions</span></span>
   - [<span data-ttu-id="c294d-118">Linux</span><span class="sxs-lookup"><span data-stu-id="c294d-118">Linux</span></span>](https://github.com/PowerShell/PowerShell/blob/master/docs/installation/linux.md)
   - [<span data-ttu-id="c294d-119">macOS</span><span class="sxs-lookup"><span data-stu-id="c294d-119">macOS</span></span>](https://github.com/PowerShell/PowerShell/blob/master/docs/installation/linux.md#macos-1012)

## <a name="step-2-install-azure-powershell-for-net-core"></a><span data-ttu-id="c294d-120">Шаг 2. Установка Azure PowerShell для .NET Core</span><span class="sxs-lookup"><span data-stu-id="c294d-120">Step 2: Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="c294d-121">PowerShell 6 (бета-версия) поставляется с установленным модулем PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="c294d-121">PowerShell 6 (beta) comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="c294d-122">Это позволяет легко установить любой модуль, опубликованный в коллекции PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c294d-122">This makes it easy to install any module that is published to the PowerShell Gallery.</span></span> <span data-ttu-id="c294d-123">Чтобы установить Azure PowerShell, откройте новый сеанс PowerShell и выполните следующую команду.</span><span class="sxs-lookup"><span data-stu-id="c294d-123">To install Azure PowerShell, open a new PowerShell session and run the following command:</span></span>

```powershell
Install-Module AzureRM.NetCore
```

## <a name="step-3-load-the-azurermnetcore-module"></a><span data-ttu-id="c294d-124">Шаг 3. Загрузка модуля AzureRM.Netcore</span><span class="sxs-lookup"><span data-stu-id="c294d-124">Step 3: Load the AzureRM.Netcore module</span></span>

<span data-ttu-id="c294d-125">После установки модуля его необходимо загрузить в сеанс PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c294d-125">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="c294d-126">Модули можно загрузить с помощью командлета `Import-Module` следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c294d-126">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module AzureRM.Netcore
```

<span data-ttu-id="c294d-127">После завершения импорта можно проверить только что установленный модуль, попытавшись войти в Azure с помощью следующей команды.</span><span class="sxs-lookup"><span data-stu-id="c294d-127">After the import completes, you can test your newly installed and module by attempting to sign into Azure using the following command:</span></span>

```powershell
Login-AzureRMAccount
```

<span data-ttu-id="c294d-128">Приведенная выше команда должна предложить перейти по адресу `https://aka.ms/devicelogin` и ввести предоставленный код.</span><span class="sxs-lookup"><span data-stu-id="c294d-128">The above command should prompt you to go to `https://aka.ms/devicelogin` and enter the provided code.</span></span>

## <a name="available-cmdlets"></a><span data-ttu-id="c294d-129">Доступные командлеты</span><span class="sxs-lookup"><span data-stu-id="c294d-129">Available cmdlets</span></span>

<span data-ttu-id="c294d-130">Модули Azure PowerShell для .NET Standard еще находятся в разработке.</span><span class="sxs-lookup"><span data-stu-id="c294d-130">The Azure PowerShell modules for .NET Standard are still in development.</span></span> <span data-ttu-id="c294d-131">Эти модули не обеспечивают полный набор командлетов, которые доступны в версии модулей для Windows.</span><span class="sxs-lookup"><span data-stu-id="c294d-131">These modules do not provide the full set of cmdlets that are available for the Windows version of the modules.</span></span> <span data-ttu-id="c294d-132">В модулях AzureRM.Netcore реализованы следующие функции.</span><span class="sxs-lookup"><span data-stu-id="c294d-132">The following functions are implemented in AzureRM.Netcore modules:</span></span>

* <span data-ttu-id="c294d-133">Управление учетными записями</span><span class="sxs-lookup"><span data-stu-id="c294d-133">Account management</span></span>
  - <span data-ttu-id="c294d-134">Вход с помощью учетной записи Майкрософт, рабочей или учебной учетной записи или субъекта-службы с помощью Microsoft Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c294d-134">Login with Microsoft account, Organizational account, or Service Principal through Microsoft Azure Active Directory</span></span>
  - <span data-ttu-id="c294d-135">Сохранение учетных данных на диск с помощью командлета Save-AzureRmContext и загрузка сохраненных учетных данных с помощью командлета Import-AzureRmContext.</span><span class="sxs-lookup"><span data-stu-id="c294d-135">Save Credentials to disk with Save-AzureRmContext and load saved credentials using Import-AzureRmContext</span></span>
* <span data-ttu-id="c294d-136">Среда</span><span class="sxs-lookup"><span data-stu-id="c294d-136">Environment</span></span>
  - <span data-ttu-id="c294d-137">Получение различных стандартных сред Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c294d-137">Get the different out-of-box Microsoft Azure environments</span></span>
  - <span data-ttu-id="c294d-138">Добавление, настройка и удаление настроенных сред (например, сред Azure Stack или Windows Azure Pack).</span><span class="sxs-lookup"><span data-stu-id="c294d-138">Add/Set/Remove customized environments (like your Azure Stack or Windows Azure Pack environments)</span></span>
* <span data-ttu-id="c294d-139">Командлеты плоскости управления для служб Azure, использующих интерфейсы Resource Manager и интерфейсы управления службами.</span><span class="sxs-lookup"><span data-stu-id="c294d-139">Management plane cmdlets for Azure services using Resource Manager and Service Management interfaces.</span></span>
  - <span data-ttu-id="c294d-140">Виртуальная машина</span><span class="sxs-lookup"><span data-stu-id="c294d-140">Virtual Machine</span></span>
  - <span data-ttu-id="c294d-141">Служба приложений (веб-сайты)</span><span class="sxs-lookup"><span data-stu-id="c294d-141">App Service (Websites)</span></span>
  - <span data-ttu-id="c294d-142">База данных SQL</span><span class="sxs-lookup"><span data-stu-id="c294d-142">SQL Database</span></span>
  - <span data-ttu-id="c294d-143">Хранилище</span><span class="sxs-lookup"><span data-stu-id="c294d-143">Storage</span></span>
  - <span data-ttu-id="c294d-144">Сеть</span><span class="sxs-lookup"><span data-stu-id="c294d-144">Network</span></span>

## <a name="next-steps"></a><span data-ttu-id="c294d-145">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="c294d-145">Next Steps</span></span>

<span data-ttu-id="c294d-146">Дополнительные сведения об использовании Azure PowerShell см. в статье [Начало работы с Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="c294d-146">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
