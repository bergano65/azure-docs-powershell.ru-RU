---
title: Установка Azure PowerShell в ОС macOS или Linux
description: Инструкции по установке Azure PowerShell в ОС macOS или Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 17912c155255b6fdfd3cfb9242163b67d405dc03
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323175"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a><span data-ttu-id="9c8e8-103">Установка Azure PowerShell в ОС macOS или Linux</span><span class="sxs-lookup"><span data-stu-id="9c8e8-103">Install Azure PowerShell on macOS or Linux</span></span>

<span data-ttu-id="9c8e8-104">Теперь Azure PowerShell можно запускать на основе PowerShell Core версии 6 на платформах, отличных от Windows.</span><span class="sxs-lookup"><span data-stu-id="9c8e8-104">For non-Windows platforms, it's possible to run Azure PowerShell on top of PowerShell Core v6.</span></span> <span data-ttu-id="9c8e8-105">В отличие от стандартной версии Azure PowerShell, созданной на основе .NET Framework для Windows, эта версия создана специально для .NET Core и запустить ее можно на любой платформе, поддерживающей среду выполнения .NET Core.</span><span class="sxs-lookup"><span data-stu-id="9c8e8-105">Rather than the standard Azure PowerShell built on .NET Framework for Windows, this product is built for .NET Core and can run on any platform which supports the .Net Core runtime.</span></span>

> [!NOTE]
> <span data-ttu-id="9c8e8-106">Сейчас PowerShell Core версии 6 и Azure PowerShell для .NET Core реализованы в бета-версии.</span><span class="sxs-lookup"><span data-stu-id="9c8e8-106">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Core are still in beta.</span></span>
> <span data-ttu-id="9c8e8-107">Поддержка этих продуктов ограничена.</span><span class="sxs-lookup"><span data-stu-id="9c8e8-107">Support for these products is limited.</span></span> <span data-ttu-id="9c8e8-108">Если у вас возникнут проблемы или вы обнаружите ошибки, сообщите об этом через сайт GitHub.</span><span class="sxs-lookup"><span data-stu-id="9c8e8-108">If you have problems or discover bugs, please file an issue on GitHub.</span></span>
>
> * [<span data-ttu-id="9c8e8-109">Проблемы, связанные с PowerShell Core версии 6</span><span class="sxs-lookup"><span data-stu-id="9c8e8-109">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="9c8e8-110">Проблемы, связанные с Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="9c8e8-110">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core-v6"></a><span data-ttu-id="9c8e8-111">Установка PowerShell Core версии 6</span><span class="sxs-lookup"><span data-stu-id="9c8e8-111">Install PowerShell Core v6</span></span>

<span data-ttu-id="9c8e8-112">Процедура установки PowerShell Core версии 6 в ОС Linux или macOS зависит от дистрибутива Linux и версии ОС.</span><span class="sxs-lookup"><span data-stu-id="9c8e8-112">Installing PowerShell Core v6 on Linux or macOS varies depending on the Linux distribution and OS version.</span></span>
<span data-ttu-id="9c8e8-113">Подробные инструкции можно найти в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="9c8e8-113">Detailed instructions can be found in the following articles:</span></span>

- [<span data-ttu-id="9c8e8-114">Установка PowerShell Core в macOS</span><span class="sxs-lookup"><span data-stu-id="9c8e8-114">Install PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
- [<span data-ttu-id="9c8e8-115">Установка PowerShell Core в Linux</span><span class="sxs-lookup"><span data-stu-id="9c8e8-115">Install PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a><span data-ttu-id="9c8e8-116">Установка Azure PowerShell для .NET Core</span><span class="sxs-lookup"><span data-stu-id="9c8e8-116">Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="9c8e8-117">PowerShell Core версии 6 поставляется с установленным модулем PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="9c8e8-117">PowerShell Core v6 comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="9c8e8-118">Это позволяет легко установить любой модуль, опубликованный в коллекции PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9c8e8-118">This makes it easy to install any module that is published to the PowerShell Gallery.</span></span> <span data-ttu-id="9c8e8-119">Чтобы установить Azure PowerShell, откройте новый сеанс PowerShell и выполните следующую команду.</span><span class="sxs-lookup"><span data-stu-id="9c8e8-119">To install Azure PowerShell, open a new PowerShell session and run the following command:</span></span>

```powershell
Install-Module AzureRM.NetCore
```

## <a name="load-the-azurermnetcore-module"></a><span data-ttu-id="9c8e8-120">Загрузка модуля AzureRM.Netcore</span><span class="sxs-lookup"><span data-stu-id="9c8e8-120">Load the AzureRM.Netcore module</span></span>

<span data-ttu-id="9c8e8-121">После установки модуля его необходимо загрузить в сеанс PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9c8e8-121">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="9c8e8-122">Модули можно загрузить с помощью командлета `Import-Module` следующим образом:</span><span class="sxs-lookup"><span data-stu-id="9c8e8-122">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module AzureRM.Netcore
Import-Module AzureRM.Profile.Netcore
```

<span data-ttu-id="9c8e8-123">После завершения импорта можно проверить только что установленный модуль, попытавшись войти в Azure с помощью следующей команды.</span><span class="sxs-lookup"><span data-stu-id="9c8e8-123">After the import completes, you can test your newly installed and module by attempting to sign into Azure using the following command:</span></span>

```powershell
Connect-AzureRmAccount
```

<span data-ttu-id="9c8e8-124">Приведенная выше команда должна предложить перейти по адресу `https://aka.ms/devicelogin` и ввести предоставленный код.</span><span class="sxs-lookup"><span data-stu-id="9c8e8-124">The above command should prompt you to go to `https://aka.ms/devicelogin` and enter the provided code.</span></span>

## <a name="available-cmdlets"></a><span data-ttu-id="9c8e8-125">Доступные командлеты</span><span class="sxs-lookup"><span data-stu-id="9c8e8-125">Available cmdlets</span></span>

<span data-ttu-id="9c8e8-126">Модули Azure PowerShell для .NET Standard еще находятся в разработке.</span><span class="sxs-lookup"><span data-stu-id="9c8e8-126">The Azure PowerShell modules for .NET Standard are still in development.</span></span> <span data-ttu-id="9c8e8-127">Эти модули не обеспечивают полный набор командлетов, которые доступны в версии модулей для Windows.</span><span class="sxs-lookup"><span data-stu-id="9c8e8-127">These modules do not provide the full set of cmdlets that are available for the Windows version of the modules.</span></span> <span data-ttu-id="9c8e8-128">В модулях AzureRM.Netcore реализованы следующие функции.</span><span class="sxs-lookup"><span data-stu-id="9c8e8-128">The following functions are implemented in AzureRM.Netcore modules:</span></span>

* <span data-ttu-id="9c8e8-129">Управление учетными записями</span><span class="sxs-lookup"><span data-stu-id="9c8e8-129">Account management</span></span>
  - <span data-ttu-id="9c8e8-130">Вход с помощью учетной записи Майкрософт, рабочей или учебной учетной записи или субъекта-службы с помощью Microsoft Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9c8e8-130">Login with Microsoft account, Organizational account, or Service Principal through Microsoft Azure Active Directory</span></span>
  - <span data-ttu-id="9c8e8-131">Сохранение учетных данных на диск с помощью командлета Save-AzureRmContext и загрузка сохраненных учетных данных с помощью командлета Import-AzureRmContext.</span><span class="sxs-lookup"><span data-stu-id="9c8e8-131">Save Credentials to disk with Save-AzureRmContext and load saved credentials using Import-AzureRmContext</span></span>
* <span data-ttu-id="9c8e8-132">Среда</span><span class="sxs-lookup"><span data-stu-id="9c8e8-132">Environment</span></span>
  - <span data-ttu-id="9c8e8-133">Получение различных стандартных сред Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9c8e8-133">Get the different out-of-box Microsoft Azure environments</span></span>
  - <span data-ttu-id="9c8e8-134">Добавление, настройка и удаление настроенных сред (например, сред Azure Stack или Windows Azure Pack).</span><span class="sxs-lookup"><span data-stu-id="9c8e8-134">Add/Set/Remove customized environments (like your Azure Stack or Windows Azure Pack environments)</span></span>
* <span data-ttu-id="9c8e8-135">Командлеты плоскости управления для служб Azure, использующих интерфейсы Resource Manager и интерфейсы управления службами.</span><span class="sxs-lookup"><span data-stu-id="9c8e8-135">Management plane cmdlets for Azure services using Resource Manager and Service Management interfaces.</span></span>
  - <span data-ttu-id="9c8e8-136">Виртуальная машина</span><span class="sxs-lookup"><span data-stu-id="9c8e8-136">Virtual Machine</span></span>
  - <span data-ttu-id="9c8e8-137">Служба приложений (веб-сайты)</span><span class="sxs-lookup"><span data-stu-id="9c8e8-137">App Service (Websites)</span></span>
  - <span data-ttu-id="9c8e8-138">База данных SQL</span><span class="sxs-lookup"><span data-stu-id="9c8e8-138">SQL Database</span></span>
  - <span data-ttu-id="9c8e8-139">Служба хранилища</span><span class="sxs-lookup"><span data-stu-id="9c8e8-139">Storage</span></span>
  - <span data-ttu-id="9c8e8-140">Сеть</span><span class="sxs-lookup"><span data-stu-id="9c8e8-140">Network</span></span>

## <a name="next-steps"></a><span data-ttu-id="9c8e8-141">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="9c8e8-141">Next Steps</span></span>

<span data-ttu-id="9c8e8-142">Дополнительные сведения об использовании Azure PowerShell см. в статье [Начало работы с Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="9c8e8-142">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
