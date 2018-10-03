---
title: Установка Azure PowerShell в ОС macOS или Linux
description: Инструкции по установке Azure PowerShell в ОС macOS или Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: f014d62e898da195a38052db6b7e37a2cd96dfdd
ms.sourcegitcommit: 3a02e0c85c83de873981dd392500bc82c1cf9286
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/24/2018
ms.locfileid: "46560122"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a><span data-ttu-id="4881f-103">Установка Azure PowerShell в ОС macOS или Linux</span><span class="sxs-lookup"><span data-stu-id="4881f-103">Install Azure PowerShell on macOS or Linux</span></span>

<span data-ttu-id="4881f-104">Для платформ, отличных от Windows, доступна альтернатива Azure PowerShell — PowerShell Core версии 6.</span><span class="sxs-lookup"><span data-stu-id="4881f-104">For non-Windows platforms, it's possible to run Azure PowerShell in PowerShell Core v6.</span></span> <span data-ttu-id="4881f-105">Эта версия PowerShell предназначена для всех платформ, поддерживающих .NET Core.</span><span class="sxs-lookup"><span data-stu-id="4881f-105">This version of PowerShell is built for use on any platform that supports .NET Core.</span></span> <span data-ttu-id="4881f-106">Для работы с этими платформами доступна версия Azure PowerShell для .NET Standard.</span><span class="sxs-lookup"><span data-stu-id="4881f-106">To work with these platforms, there's a .NET Standard version of Azure PowerShell available.</span></span>

> [!NOTE]
> <span data-ttu-id="4881f-107">Сейчас PowerShell Core версии 6 и Azure PowerShell для .NET Core реализованы в бета-версии.</span><span class="sxs-lookup"><span data-stu-id="4881f-107">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Core are still in beta.</span></span>
> <span data-ttu-id="4881f-108">Поддержка этих продуктов ограничена.</span><span class="sxs-lookup"><span data-stu-id="4881f-108">Support for these products is limited.</span></span> <span data-ttu-id="4881f-109">Если у вас возникнут проблемы или вы обнаружите ошибки, сообщите об этом через сайт GitHub.</span><span class="sxs-lookup"><span data-stu-id="4881f-109">If you have problems or discover bugs, please file an issue on GitHub.</span></span>
>
> * [<span data-ttu-id="4881f-110">Проблемы, связанные с PowerShell Core версии 6</span><span class="sxs-lookup"><span data-stu-id="4881f-110">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="4881f-111">Проблемы, связанные с Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="4881f-111">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a><span data-ttu-id="4881f-112">Установка PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="4881f-112">Install PowerShell Core</span></span>

<span data-ttu-id="4881f-113">Инструкции по установке PowerShell Core отличаются для macOS и большинства дистрибутивов Linux.</span><span class="sxs-lookup"><span data-stu-id="4881f-113">The installation instructions for PowerShell Core are different for macOS and most Linux distributions.</span></span>
<span data-ttu-id="4881f-114">Подробные инструкции можно найти в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="4881f-114">Detailed instructions can be found in the following articles:</span></span>

* [<span data-ttu-id="4881f-115">Установка PowerShell Core в macOS</span><span class="sxs-lookup"><span data-stu-id="4881f-115">Install PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [<span data-ttu-id="4881f-116">Установка PowerShell Core в Linux</span><span class="sxs-lookup"><span data-stu-id="4881f-116">Install PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a><span data-ttu-id="4881f-117">Установка Azure PowerShell для .NET Core</span><span class="sxs-lookup"><span data-stu-id="4881f-117">Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="4881f-118">В PowerShell Core уже входит модуль PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="4881f-118">PowerShell Core comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="4881f-119">Для установки модулей в PowerShell требуется более высокий уровень привилегий, поэтому вы должны запустить сеанс как суперпользователь.</span><span class="sxs-lookup"><span data-stu-id="4881f-119">Installation of modules in PowerShell requires elevated privileges, so you'll need to start your session as superuser:</span></span>

```bash
sudo pwsh
```

<span data-ttu-id="4881f-120">Чтобы установить Azure PowerShell, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="4881f-120">To install Azure PowerShell, run the following command:</span></span>

```powershell
Install-Module Az
```

> [!IMPORTANT]
> <span data-ttu-id="4881f-121">Модуль `AzureRM`, описанный в других статьях, не предназначен для .NET Core и не будет работать с PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="4881f-121">The `AzureRM` module detailed in other articles is not built for .NET Core and will not work with PowerShell Core.</span></span> <span data-ttu-id="4881f-122">Модули `Az` содержат псевдонимы команд для всех командлетов `AzureRM`, поэтому можно пользоваться всей документацией для `AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="4881f-122">The `Az` modules contain command aliases for all `AzureRM` cmdlets, so all of the documentation for `AzureRM` applies.</span></span>

<span data-ttu-id="4881f-123">По умолчанию коллекция PowerShell не используется как доверенный репозиторий для PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="4881f-123">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="4881f-124">При первом использовании PSGallery отображается следующее сообщение:</span><span class="sxs-lookup"><span data-stu-id="4881f-124">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="4881f-125">Ответьте `Yes` или `Yes to All`, чтобы продолжить установку.</span><span class="sxs-lookup"><span data-stu-id="4881f-125">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

## <a name="sign-in"></a><span data-ttu-id="4881f-126">Вход</span><span class="sxs-lookup"><span data-stu-id="4881f-126">Sign in</span></span>

<span data-ttu-id="4881f-127">Чтобы приступить к работе с Azure PowerShell, вам нужно загрузить `Az` в текущий сеанс PowerShell. Для этого воспользуйтесь командлетом [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), после чего войдите в систему с помощью своих учетных данных Azure.</span><span class="sxs-lookup"><span data-stu-id="4881f-127">To start working with Azure PowerShell, you need to load `Az` into your PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span> <span data-ttu-id="4881f-128">Для импорта модуля более высокий уровень привилегий __не__ требуется.</span><span class="sxs-lookup"><span data-stu-id="4881f-128">Importing a module does __not__ require elevated privileges.</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module Az
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="4881f-129">Эти действия нужно повторять для каждого нового сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4881f-129">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="4881f-130">Чтобы автоматически импортировать модуль `Az`, необходимо настроить профиль PowerShell. Подробнее об этом рассказывается [здесь](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="4881f-130">Automatically importing the `Az` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="4881f-131">В macOS и Linux работа с профилем выполняется с использованием переменной среды `$Profile`.</span><span class="sxs-lookup"><span data-stu-id="4881f-131">On macOS and Linux, you should work with your profile through the `$Profile` environment variable.</span></span> <span data-ttu-id="4881f-132">Чтобы узнать, как повторно использовать свои данные для входа в Azure в разных сеансах, см. статью [Использование учетных данных пользователя в разных сеансах PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="4881f-132">To learn how to persist your Azure sign-in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="4881f-133">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="4881f-133">Next Steps</span></span>

<span data-ttu-id="4881f-134">Дополнительные сведения об использовании Azure PowerShell см. в статье [Начало работы с Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="4881f-134">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
