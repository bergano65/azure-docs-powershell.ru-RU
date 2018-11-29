---
title: Установка Azure PowerShell в ОС macOS или Linux
description: Инструкции по установке Azure PowerShell в ОС macOS или Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/05/2018
ms.openlocfilehash: f60ea1c608be4b1c8319d53303713ba039276abc
ms.sourcegitcommit: 558436c824d9b59731aa9b963cdc8df4dea932e7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/29/2018
ms.locfileid: "52588117"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a><span data-ttu-id="67ee0-103">Установка Azure PowerShell в ОС macOS или Linux</span><span class="sxs-lookup"><span data-stu-id="67ee0-103">Install Azure PowerShell on macOS or Linux</span></span>

<span data-ttu-id="67ee0-104">Для платформ, отличных от Windows, доступна альтернатива Azure PowerShell — PowerShell Core версии 6.</span><span class="sxs-lookup"><span data-stu-id="67ee0-104">For non-Windows platforms, it's possible to run Azure PowerShell in PowerShell Core v6.</span></span> <span data-ttu-id="67ee0-105">Эта версия PowerShell предназначена для всех платформ, поддерживающих .NET Core.</span><span class="sxs-lookup"><span data-stu-id="67ee0-105">This version of PowerShell is built for use on any platform that supports .NET Core.</span></span> <span data-ttu-id="67ee0-106">Для работы с этими платформами доступна версия Azure PowerShell для .NET Standard.</span><span class="sxs-lookup"><span data-stu-id="67ee0-106">To work with these platforms, there's a .NET Standard version of Azure PowerShell available.</span></span>

> [!NOTE]
> <span data-ttu-id="67ee0-107">В настоящее время Azure PowerShell для .NET Standard предлагается в режиме бета-версии.</span><span class="sxs-lookup"><span data-stu-id="67ee0-107">At this time, Azure PowerShell for .NET Standard is still in beta.</span></span>
> <span data-ttu-id="67ee0-108">Если у вас возникнут проблемы или вы обнаружите ошибки, сообщите об этом через сайт GitHub.</span><span class="sxs-lookup"><span data-stu-id="67ee0-108">If you have problems or discover bugs, please file an issue on GitHub.</span></span>
>
> * [<span data-ttu-id="67ee0-109">Проблемы, связанные с Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="67ee0-109">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a><span data-ttu-id="67ee0-110">Установка PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="67ee0-110">Install PowerShell Core</span></span>

<span data-ttu-id="67ee0-111">Инструкции по установке PowerShell Core отличаются для macOS и большинства дистрибутивов Linux.</span><span class="sxs-lookup"><span data-stu-id="67ee0-111">The installation instructions for PowerShell Core are different for macOS and most Linux distributions.</span></span>
<span data-ttu-id="67ee0-112">Подробные инструкции можно найти в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="67ee0-112">Detailed instructions can be found in the following articles:</span></span>

* [<span data-ttu-id="67ee0-113">Установка PowerShell Core в macOS</span><span class="sxs-lookup"><span data-stu-id="67ee0-113">Install PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [<span data-ttu-id="67ee0-114">Установка PowerShell Core в Linux</span><span class="sxs-lookup"><span data-stu-id="67ee0-114">Install PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-standard"></a><span data-ttu-id="67ee0-115">Установка Azure PowerShell для .NET Standard</span><span class="sxs-lookup"><span data-stu-id="67ee0-115">Install Azure PowerShell for .NET Standard</span></span>

> [!IMPORTANT]
> <span data-ttu-id="67ee0-116">Модуль `AzureRM`, описанный в других статьях, не работает с PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="67ee0-116">The `AzureRM` module detailed in other articles does not work with PowerShell Core.</span></span>
> <span data-ttu-id="67ee0-117">Чтобы получить функциональность Azure PowerShell в PowerShell Core, необходимо установить модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="67ee0-117">You must install the `Az` module to get Azure PowerShell functionality in PowerShell Core.</span></span>

<span data-ttu-id="67ee0-118">В PowerShell Core уже входит модуль PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="67ee0-118">PowerShell Core comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="67ee0-119">Запустите PowerShell с помощью команды:</span><span class="sxs-lookup"><span data-stu-id="67ee0-119">Start PowerShell with the command:</span></span>

```bash
pwsh
```

<span data-ttu-id="67ee0-120">Чтобы установить Azure PowerShell, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="67ee0-120">To install Azure PowerShell, run the following command:</span></span>

```powershell-interactive
Install-Module Az
```

> [!NOTE]
> <span data-ttu-id="67ee0-121">Если при попытке установить модуль возникает ошибка, связанная с разрешениями, возможно, для установки модулей вам нужно запустить PowerShell в режиме суперпользователя.</span><span class="sxs-lookup"><span data-stu-id="67ee0-121">If you encounter a permissions error when attempting to install the module, you may need to run PowerShell in superuser mode to install modules.</span></span>
>
> ```bash
> sudo pwsh
> ```

<span data-ttu-id="67ee0-122">По умолчанию коллекция PowerShell не используется как доверенный репозиторий для PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="67ee0-122">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="67ee0-123">При первом использовании PSGallery отображается следующее сообщение:</span><span class="sxs-lookup"><span data-stu-id="67ee0-123">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="67ee0-124">Ответьте `Yes` или `Yes to All`, чтобы продолжить установку.</span><span class="sxs-lookup"><span data-stu-id="67ee0-124">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

## <a name="enable-aliases"></a><span data-ttu-id="67ee0-125">Включение псевдонимов</span><span class="sxs-lookup"><span data-stu-id="67ee0-125">Enable aliases</span></span>

<span data-ttu-id="67ee0-126">Для совместимости с существующим модулем `AzureRM` новый модуль `Az` получил возможность создавать обратно совместимые псевдонимы для командлетов `AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="67ee0-126">For compatibility with the existing `AzureRM` module, the new `Az` module has the ability to create backwards compatible aliases for the `AzureRM` cmdlets.</span></span> <span data-ttu-id="67ee0-127">Перед первым использованием модуля настройте эти псевдонимы с помощью следующей команды:</span><span class="sxs-lookup"><span data-stu-id="67ee0-127">Before using the module for the first time, set up these aliases with the following command:</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module Az
# Enable AzureRM aliases for the user
Enable-AzureRmAlias -Scope CurrentUser
```

<span data-ttu-id="67ee0-128">Псевдонимы будут настроены только для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="67ee0-128">This sets up aliases for the current user only.</span></span> <span data-ttu-id="67ee0-129">Сведения о других значениях, которые можно указать в параметре `-Scope` при настройке псевдонимов, см. в справке командлета.</span><span class="sxs-lookup"><span data-stu-id="67ee0-129">Check the cmdlet help for other values that can be provided to `-Scope` to set up the aliases.</span></span>

> [!NOTE]
> <span data-ttu-id="67ee0-130">Если возникла ошибка, связанная с расположением пути, убедитесь, что этот путь существует в локальной файловой системе.</span><span class="sxs-lookup"><span data-stu-id="67ee0-130">If you encounter an error about a path location, make sure that it exists on your local system.</span></span> <span data-ttu-id="67ee0-131">В области `CurrentUser` это ошибку можно устранить, выполнив следующую команду в `bash`:</span><span class="sxs-lookup"><span data-stu-id="67ee0-131">For the `CurrentUser` scope, this error can be resolved by running the following command in `bash`:</span></span>
>
> ```bash
> mkdir -p $HOME/.config/powershell
> ```

## <a name="sign-in"></a><span data-ttu-id="67ee0-132">Вход</span><span class="sxs-lookup"><span data-stu-id="67ee0-132">Sign in</span></span>

<span data-ttu-id="67ee0-133">Чтобы приступить к работе с Azure PowerShell, вам нужно загрузить `Az` в текущий сеанс PowerShell. Для этого воспользуйтесь командлетом [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), после чего войдите в систему с помощью своих учетных данных Azure.</span><span class="sxs-lookup"><span data-stu-id="67ee0-133">To start working with Azure PowerShell, you need to load `Az` into your PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span> <span data-ttu-id="67ee0-134">Для импорта модуля более высокий уровень привилегий __не__ требуется.</span><span class="sxs-lookup"><span data-stu-id="67ee0-134">Importing a module does __not__ require elevated privileges.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module Az
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="67ee0-135">Эти действия нужно повторять для каждого нового сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="67ee0-135">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="67ee0-136">Чтобы автоматически импортировать модуль `Az`, необходимо настроить профиль PowerShell. Подробнее об этом рассказывается [здесь](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="67ee0-136">Automatically importing the `Az` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="67ee0-137">В macOS и Linux работа с профилем выполняется с использованием переменной среды `$Profile`.</span><span class="sxs-lookup"><span data-stu-id="67ee0-137">On macOS and Linux, you should work with your profile through the `$Profile` environment variable.</span></span> <span data-ttu-id="67ee0-138">Чтобы узнать, как повторно использовать свои данные для входа в Azure в разных сеансах, см. статью [Использование учетных данных пользователя в разных сеансах PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="67ee0-138">To learn how to persist your Azure sign-in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="67ee0-139">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="67ee0-139">Next Steps</span></span>

<span data-ttu-id="67ee0-140">Дополнительные сведения об использовании Azure PowerShell см. в статье [Начало работы с Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="67ee0-140">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
