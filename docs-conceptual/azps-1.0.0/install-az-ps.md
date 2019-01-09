---
title: Установка Azure PowerShell с помощью PowerShellGet
description: Инструкции по установке Azure PowerShell с помощью PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 828fa8cb2aabac893c566fb146d00af04b16b479
ms.sourcegitcommit: 6685809f054203bd733c84f68acc69e53e5cca8c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/02/2019
ms.locfileid: "53982932"
---
# <a name="install-the-azure-powershell-module"></a><span data-ttu-id="e0e60-103">Установка модуля Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="e0e60-103">Install the Azure PowerShell module</span></span>

<span data-ttu-id="e0e60-104">В этой статье рассказывается, как установить модули Azure PowerShell с помощью PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="e0e60-104">This article tells you how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="e0e60-105">Эти инструкции применимы для платформ Windows, macOS и Linux.</span><span class="sxs-lookup"><span data-stu-id="e0e60-105">These instructions work on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="e0e60-106">В данный момент другие методы установки не поддерживаются для модуля Az.</span><span class="sxs-lookup"><span data-stu-id="e0e60-106">For the Az module, currently no other installation methods are supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0e60-107">Требования</span><span class="sxs-lookup"><span data-stu-id="e0e60-107">Requirements</span></span>

<span data-ttu-id="e0e60-108">Azure PowerShell работает с PowerShell 6.x на любой платформе или с PowerShell 5.x на Windows 7 или более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="e0e60-108">Azure PowerShell works with PowerShell 5.x on Windows 7 or higher, or PowerShell 6.x on any platform.</span></span>
<span data-ttu-id="e0e60-109">Чтобы узнать вашу версию PowerShell, выполните приведенную ниже команду:</span><span class="sxs-lookup"><span data-stu-id="e0e60-109">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="e0e60-110">Если вы используете старую версию или вам нужно установить PowerShell, см. статью [Установка разных версий PowerShell](/powershell/scripting/setup/installing-powershell).</span><span class="sxs-lookup"><span data-stu-id="e0e60-110">If you have an outdated version or need to install PowerShell, see [Installing various versions of PowerShell](/powershell/scripting/setup/installing-powershell).</span></span> <span data-ttu-id="e0e60-111">На этой странице вы найдете ссылки на сведения по установке для своей платформы.</span><span class="sxs-lookup"><span data-stu-id="e0e60-111">Install information for your platform is linked from that page.</span></span>

<span data-ttu-id="e0e60-112">Если вы используете PowerShell 5.x на Windows, необходимо также установить .NET Framework 4.7.2.</span><span class="sxs-lookup"><span data-stu-id="e0e60-112">If you are using PowerShell 5.x on Windows, you also need .NET Framework 4.7.2 installed.</span></span> <span data-ttu-id="e0e60-113">Инструкции по обновлению или установке новой версии платформы .NET Framework см. в разделе [Руководство по установке](/dotnet/framework/install).</span><span class="sxs-lookup"><span data-stu-id="e0e60-113">For instructions on updating or installing a new version of .NET Framework, see the [.NET Framework installation guide](/dotnet/framework/install).</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="e0e60-114">Установка модуля Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="e0e60-114">Install the Azure PowerShell module</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="e0e60-115">Модули AzureRM и Az могут быть установлены одновременно.</span><span class="sxs-lookup"><span data-stu-id="e0e60-115">You can have both the AzureRM and Az modules installed at the same time.</span></span> <span data-ttu-id="e0e60-116">Если у вас установлены оба модуля, __не включайте псевдонимы__.</span><span class="sxs-lookup"><span data-stu-id="e0e60-116">If you have both modules installed, __don't enable aliases__.</span></span>
> <span data-ttu-id="e0e60-117">Включение псевдонимов приведет к конфликтам между командлетами AzureRM и псевдонимами команд Az с непредсказуемыми результатами.</span><span class="sxs-lookup"><span data-stu-id="e0e60-117">Enabling aliases will cause conflicts between AzureRM cmdlets and Az command aliases, and could cause unexpected behavior.</span></span>
> <span data-ttu-id="e0e60-118">Перед установкой модуля Az рекомендуется удалить AzureRM.</span><span class="sxs-lookup"><span data-stu-id="e0e60-118">It's recommended that before installing the Az module, you uninstall AzureRM.</span></span> <span data-ttu-id="e0e60-119">Удалить AzureRM или включить псевдонимы можно в любое время.</span><span class="sxs-lookup"><span data-stu-id="e0e60-119">You can always uninstall AzureRM or enable aliases at any time.</span></span> <span data-ttu-id="e0e60-120">Дополнительные сведения о псевдонимах команд AzureRM см. в статье [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md) (Миграция с AzureRM на Az для Azure PowerShell).</span><span class="sxs-lookup"><span data-stu-id="e0e60-120">To learn about the AzureRM command aliases, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
> <span data-ttu-id="e0e60-121">Инструкции по удалению см. в разделе [Uninstall the AzureRM module](uninstall-az-ps.md#uninstall-the-azurerm-module) (Удаление модуля AzureRM).</span><span class="sxs-lookup"><span data-stu-id="e0e60-121">For uninstall instructions, see [Uninstall the AzureRM module](uninstall-az-ps.md#uninstall-the-azurerm-module).</span></span> 

<span data-ttu-id="e0e60-122">Чтобы установить модули в глобальной области видимости, необходим более высокий уровень привилегий для установки модулей из коллекции PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e0e60-122">To install modules at a global scope, you need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="e0e60-123">Чтобы установить Azure PowerShell, выполните следующую команду в сеансе с более высоким уровнем привилегий ("Запуск от имени администратора" в Windows или с правами суперпользователя в macOS или Linux):</span><span class="sxs-lookup"><span data-stu-id="e0e60-123">To install Azure PowerShell, run the following command in an elevated session ("Run as Administrator" on Windows, or with superuser privileges on macOS or Linux):</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

<span data-ttu-id="e0e60-124">Если у вас нет доступа к привилегиям администратора, можно выполнить установку для текущего пользователя, добавив аргумент `-Scope`.</span><span class="sxs-lookup"><span data-stu-id="e0e60-124">If you don't have access to administrator privileges, you can install for the current user by adding the `-Scope` argument.</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="e0e60-125">По умолчанию коллекция PowerShell не используется как доверенный репозиторий для PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="e0e60-125">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="e0e60-126">При первом использовании PSGallery отображается следующее сообщение:</span><span class="sxs-lookup"><span data-stu-id="e0e60-126">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="e0e60-127">Ответьте `Yes` или `Yes to All`, чтобы продолжить установку.</span><span class="sxs-lookup"><span data-stu-id="e0e60-127">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="e0e60-128">Модуль Az — это общий модуль для командлетов Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e0e60-128">The Az module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="e0e60-129">Во время его установки скачиваются все доступные модули Azure Resource Manager и устанавливаются все соответствующие командлеты.</span><span class="sxs-lookup"><span data-stu-id="e0e60-129">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="e0e60-130">Вход</span><span class="sxs-lookup"><span data-stu-id="e0e60-130">Sign in</span></span>

<span data-ttu-id="e0e60-131">Чтобы начать работу с Azure PowerShell, выполните вход, используя данные своей учетной записи в Azure.</span><span class="sxs-lookup"><span data-stu-id="e0e60-131">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> <span data-ttu-id="e0e60-132">Если вы отключили автоматическую загрузку модулей, вам нужно вручную импортировать модуль с помощью `Import-Module Az`.</span><span class="sxs-lookup"><span data-stu-id="e0e60-132">If you've disabled module autoloading, you need to manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="e0e60-133">Из-за структуры модуля эта операция может занять несколько секунд.</span><span class="sxs-lookup"><span data-stu-id="e0e60-133">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="e0e60-134">Эти действия нужно повторять для каждого нового сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e0e60-134">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="e0e60-135">Чтобы узнать, как повторно использовать свои данные для входа в Azure в разных сеансах PowerShell, см. статью [Использование учетных данных пользователя в разных сеансах PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="e0e60-135">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="e0e60-136">Обновление модуля Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="e0e60-136">Update the Azure PowerShell module</span></span>

<span data-ttu-id="e0e60-137">Чтобы обновить версию Azure PowerShell, выполните команду [Update-Module](/powershell/module/powershellget/update-module).</span><span class="sxs-lookup"><span data-stu-id="e0e60-137">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="e0e60-138">Эта команда __не__ удаляет предыдущие версии.</span><span class="sxs-lookup"><span data-stu-id="e0e60-138">This command does __not__ uninstall older versions.</span></span>

```powershell-interactive
Update-Module -Name Az
```

<span data-ttu-id="e0e60-139">Сведения о том, как удалить из системы предыдущие версии Azure PowerShell, см. в статье [Uninstall the Azure PowerShell module](uninstall-az-ps.md) (Удаление модуля Azure PowerShell).</span><span class="sxs-lookup"><span data-stu-id="e0e60-139">To learn how to remove old versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="e0e60-140">Использование нескольких версий Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="e0e60-140">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="e0e60-141">Вы можете установить несколько версий Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e0e60-141">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="e0e60-142">Чтобы проверить наличие нескольких установленных версий Azure PowerShell, используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="e0e60-142">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

<span data-ttu-id="e0e60-143">Сведения о том, как удалить версию Azure PowerShell, см. в статье [Удаление модуля Azure PowerShell](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="e0e60-143">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

<span data-ttu-id="e0e60-144">Определенную версию модуля `Az` можно установить или загрузить с помощью аргумента `-RequiredVersion`.</span><span class="sxs-lookup"><span data-stu-id="e0e60-144">You can install or load a specific version of the `Az` module by using the `-RequiredVersion` argument:</span></span>

```powershell-interactive
# Install Az version 0.7.0
Install-Module -Name Az -RequiredVersion 0.7.0 
# Load Az version 0.7.0
Import-Module -Name Az -RequiredVersion 0.7.0
```

<span data-ttu-id="e0e60-145">Если у вас установлено несколько версий модуля, модуль автозагрузки и `Import-Module` загрузит последнюю версию по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e0e60-145">If you have more than one version of the module installed, module autoload and `Import-Module` load the latest version by default.</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="e0e60-146">Отзывы</span><span class="sxs-lookup"><span data-stu-id="e0e60-146">Provide feedback</span></span>

<span data-ttu-id="e0e60-147">Если вы нашли ошибку при работе с Azure Powershell, сообщите о ней [на сайте GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="e0e60-147">If you find a bug in Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="e0e60-148">Чтобы отправить отзыв из командной строки, используйте командлет [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="e0e60-148">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="e0e60-149">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="e0e60-149">Next Steps</span></span>

<span data-ttu-id="e0e60-150">Дополнительные сведения о модулях Azure PowerShell и их функциях см. в статье [Get Started with Azure PowerShell](get-started-azureps.md) (Начало работы с Azure PowerShell).</span><span class="sxs-lookup"><span data-stu-id="e0e60-150">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>
<span data-ttu-id="e0e60-151">Если вы знакомы с Azure PowerShell и вам необходимо мигрировать из AzureRM, см. статью [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md) (Миграция с AzureRM на Az).</span><span class="sxs-lookup"><span data-stu-id="e0e60-151">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
