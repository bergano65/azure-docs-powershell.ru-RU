---
title: Установка Azure PowerShell в ОС macOS или Linux
description: Инструкции по установке Azure PowerShell в ОС macOS или Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 936bb24eecb4077080e172bf0d29fe57ec652187
ms.sourcegitcommit: 797c18f93aaa495ef005993b2e202d7378588dfa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2018
ms.locfileid: "53594460"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a><span data-ttu-id="6b91d-103">Установка Azure PowerShell в ОС macOS или Linux</span><span class="sxs-lookup"><span data-stu-id="6b91d-103">Install Azure PowerShell on macOS or Linux</span></span>

<span data-ttu-id="6b91d-104">Для платформ, отличных от Windows, доступна альтернатива Azure PowerShell — PowerShell Core версии 6.</span><span class="sxs-lookup"><span data-stu-id="6b91d-104">For non-Windows platforms, it's possible to run Azure PowerShell in PowerShell Core v6.</span></span> <span data-ttu-id="6b91d-105">Эта версия PowerShell предназначена для всех платформ, поддерживающих .NET Core.</span><span class="sxs-lookup"><span data-stu-id="6b91d-105">This version of PowerShell is built for use on any platform that supports .NET Core.</span></span> <span data-ttu-id="6b91d-106">Для работы с этими платформами доступна особая версия Azure PowerShell — для .NET Core.</span><span class="sxs-lookup"><span data-stu-id="6b91d-106">To work with these platforms, there's a special .NET Core version of Azure PowerShell available.</span></span>

[!INCLUDE[az-replacing-azurerm.md](../includes/az-replacing-azurerm.md)]

## <a name="install-powershell-core"></a><span data-ttu-id="6b91d-107">Установка PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="6b91d-107">Install PowerShell Core</span></span>

<span data-ttu-id="6b91d-108">Инструкции по установке PowerShell Core отличаются для macOS и большинства дистрибутивов Linux.</span><span class="sxs-lookup"><span data-stu-id="6b91d-108">The installation instructions for PowerShell Core are different for macOS and most Linux distributions.</span></span>
<span data-ttu-id="6b91d-109">Подробные инструкции можно найти в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="6b91d-109">Detailed instructions can be found in the following articles:</span></span>

* [<span data-ttu-id="6b91d-110">Установка PowerShell Core в macOS</span><span class="sxs-lookup"><span data-stu-id="6b91d-110">Install PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [<span data-ttu-id="6b91d-111">Установка PowerShell Core в Linux</span><span class="sxs-lookup"><span data-stu-id="6b91d-111">Install PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a><span data-ttu-id="6b91d-112">Установка Azure PowerShell для .NET Core</span><span class="sxs-lookup"><span data-stu-id="6b91d-112">Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="6b91d-113">В PowerShell Core уже входит модуль PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="6b91d-113">PowerShell Core comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="6b91d-114">Для установки модулей в PowerShell требуется более высокий уровень привилегий, поэтому вы должны запустить сеанс как суперпользователь.</span><span class="sxs-lookup"><span data-stu-id="6b91d-114">Installation of modules in PowerShell requires elevated privileges, so you'll need to start your session as superuser:</span></span>

```bash
sudo pwsh
```

<span data-ttu-id="6b91d-115">Чтобы установить Azure PowerShell, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="6b91d-115">To install Azure PowerShell, run the following command:</span></span>

```powershell-interactive
Install-Module AzureRM.NetCore
```

> [!IMPORTANT]
> <span data-ttu-id="6b91d-116">Модуль `AzureRM`, описанный в других статьях, не предназначен для .NET Core и не будет работать с PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="6b91d-116">The `AzureRM` module detailed in other articles is not built for .NET Core and will not work with PowerShell Core.</span></span> <span data-ttu-id="6b91d-117">В обоих модулях, `AzureRM` и `AzureRM.NetCore`, используются одинаковые имена командлетов. Единственное отличие заключается в общем модуле и версии .NET, для которой они предназначены.</span><span class="sxs-lookup"><span data-stu-id="6b91d-117">Both `AzureRM` and `AzureRM.NetCore` use the same cmdlet names, so the only difference is the name of the rollup module and which .NET version they are built against.</span></span>

<span data-ttu-id="6b91d-118">По умолчанию коллекция PowerShell не используется как доверенный репозиторий для PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="6b91d-118">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="6b91d-119">При первом использовании PSGallery отображается следующее сообщение:</span><span class="sxs-lookup"><span data-stu-id="6b91d-119">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="6b91d-120">Ответьте `Yes` или `Yes to All`, чтобы продолжить установку.</span><span class="sxs-lookup"><span data-stu-id="6b91d-120">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

## <a name="sign-in"></a><span data-ttu-id="6b91d-121">Вход</span><span class="sxs-lookup"><span data-stu-id="6b91d-121">Sign in</span></span>

<span data-ttu-id="6b91d-122">Чтобы приступить к работе с Azure PowerShell, вам нужно загрузить `AzureRM.Netcore` в текущий сеанс PowerShell. Для этого воспользуйтесь командлетом [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), после чего войдите в систему с помощью своих учетных данных Azure.</span><span class="sxs-lookup"><span data-stu-id="6b91d-122">To start working with Azure PowerShell, you need to load `AzureRM.Netcore` into your PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span> <span data-ttu-id="6b91d-123">Для импорта модуля более высокий уровень привилегий __не__ требуется.</span><span class="sxs-lookup"><span data-stu-id="6b91d-123">Importing a module does __not__ require elevated privileges.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM.Netcore
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="6b91d-124">Эти действия нужно повторять для каждого нового сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6b91d-124">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="6b91d-125">Чтобы автоматически импортировать модуль `AzureRM`, необходимо настроить профиль PowerShell. Подробнее об этом рассказывается [здесь](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="6b91d-125">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="6b91d-126">В macOS и Linux работа с профилем выполняется с использованием переменной среды `$Profile`.</span><span class="sxs-lookup"><span data-stu-id="6b91d-126">On macOS and Linux, you should work with your profile through the `$Profile` environment variable.</span></span> <span data-ttu-id="6b91d-127">Чтобы узнать, как повторно использовать свои данные для входа в Azure в разных сеансах, см. статью [Использование учетных данных пользователя в разных сеансах PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="6b91d-127">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="available-cmdlets"></a><span data-ttu-id="6b91d-128">Доступные командлеты</span><span class="sxs-lookup"><span data-stu-id="6b91d-128">Available cmdlets</span></span>

<span data-ttu-id="6b91d-129">Модули Azure PowerShell для .NET Core еще находятся в разработке.</span><span class="sxs-lookup"><span data-stu-id="6b91d-129">The Azure PowerShell modules for .NET Core are still in development.</span></span> <span data-ttu-id="6b91d-130">Эти модули не обеспечивают полный набор командлетов, которые доступны в версии модулей для Windows.</span><span class="sxs-lookup"><span data-stu-id="6b91d-130">These modules do not provide the full set of cmdlets that are available for the Windows version of the modules.</span></span> <span data-ttu-id="6b91d-131">В модулях AzureRM.Netcore реализованы следующие функции.</span><span class="sxs-lookup"><span data-stu-id="6b91d-131">The following functions are implemented in AzureRM.Netcore modules:</span></span>

* <span data-ttu-id="6b91d-132">Управление учетными записями</span><span class="sxs-lookup"><span data-stu-id="6b91d-132">Account management</span></span>
  * <span data-ttu-id="6b91d-133">Вход с помощью учетной записи Майкрософт, рабочей или учебной учетной записи или субъекта-службы с помощью Microsoft Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6b91d-133">Sign in with Microsoft account, Organizational account, or Service Principal through Microsoft Azure Active Directory</span></span>
  * <span data-ttu-id="6b91d-134">Сохранение учетных данных на диск с помощью командлета Save-AzureRmContext и загрузка сохраненных учетных данных с помощью командлета Import-AzureRmContext.</span><span class="sxs-lookup"><span data-stu-id="6b91d-134">Save Credentials to disk with Save-AzureRmContext and load saved credentials using Import-AzureRmContext</span></span>
* <span data-ttu-id="6b91d-135">Среда</span><span class="sxs-lookup"><span data-stu-id="6b91d-135">Environment</span></span>
  * <span data-ttu-id="6b91d-136">Получение различных стандартных сред Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6b91d-136">Get the different out-of-box Microsoft Azure environments</span></span>
  * <span data-ttu-id="6b91d-137">Добавление, настройка и удаление настроенных сред (например, сред Azure Stack или Windows Azure Pack).</span><span class="sxs-lookup"><span data-stu-id="6b91d-137">Add/Set/Remove customized environments (like your Azure Stack or Windows Azure Pack environments)</span></span>
* <span data-ttu-id="6b91d-138">Командлеты плоскости управления для служб Azure, использующих интерфейсы Resource Manager и интерфейсы управления службами.</span><span class="sxs-lookup"><span data-stu-id="6b91d-138">Management plane cmdlets for Azure services using Resource Manager and Service Management interfaces.</span></span>
  * <span data-ttu-id="6b91d-139">Виртуальная машина</span><span class="sxs-lookup"><span data-stu-id="6b91d-139">Virtual Machine</span></span>
  * <span data-ttu-id="6b91d-140">Служба приложений (веб-сайты)</span><span class="sxs-lookup"><span data-stu-id="6b91d-140">App Service (Websites)</span></span>
  * <span data-ttu-id="6b91d-141">База данных SQL</span><span class="sxs-lookup"><span data-stu-id="6b91d-141">SQL Database</span></span>
  * <span data-ttu-id="6b91d-142">Хранилище</span><span class="sxs-lookup"><span data-stu-id="6b91d-142">Storage</span></span>
  * <span data-ttu-id="6b91d-143">Сеть</span><span class="sxs-lookup"><span data-stu-id="6b91d-143">Network</span></span>

## <a name="next-steps"></a><span data-ttu-id="6b91d-144">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="6b91d-144">Next Steps</span></span>

<span data-ttu-id="6b91d-145">Дополнительные сведения об использовании Azure PowerShell см. в статье [Начало работы с Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="6b91d-145">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
