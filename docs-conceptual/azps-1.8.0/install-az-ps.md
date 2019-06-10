---
title: Установка Azure PowerShell с помощью PowerShellGet
description: Инструкции по установке Azure PowerShell с помощью PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: d99265c7f156622d876d700106e2b06dd729e8b8
ms.sourcegitcommit: 020c69430358b13cbd99fedd5d56607c9b10047b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "66365746"
---
# <a name="install-the-azure-powershell-module"></a><span data-ttu-id="bdda7-103">Установка модуля Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="bdda7-103">Install the Azure PowerShell module</span></span>

<span data-ttu-id="bdda7-104">В этой статье рассказывается, как установить модули Azure PowerShell с помощью PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="bdda7-104">This article tells you how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="bdda7-105">Эти инструкции применимы для платформ Windows, macOS и Linux.</span><span class="sxs-lookup"><span data-stu-id="bdda7-105">These instructions work on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="bdda7-106">В данный момент другие методы установки не поддерживаются для модуля Az.</span><span class="sxs-lookup"><span data-stu-id="bdda7-106">For the Az module, currently no other installation methods are supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdda7-107">Требования</span><span class="sxs-lookup"><span data-stu-id="bdda7-107">Requirements</span></span>

<span data-ttu-id="bdda7-108">Azure PowerShell работает с PowerShell 5.1 или более поздней версии на платформе Windows или с PowerShell Core 6.x или более поздней версии на любых платформах.</span><span class="sxs-lookup"><span data-stu-id="bdda7-108">Azure PowerShell works with PowerShell 5.1 or higher on Windows, or PowerShell Core 6.x and later on all platforms.</span></span> <span data-ttu-id="bdda7-109">Если вы не уверены, установлена ли среда PowerShell, либо используете macOS или Linux, [установите последнюю версию PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core).</span><span class="sxs-lookup"><span data-stu-id="bdda7-109">If you aren't sure if you have PowerShell, or are on macOS or Linux, [install the latest version of PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core).</span></span>

<span data-ttu-id="bdda7-110">Чтобы узнать вашу версию PowerShell, выполните приведенную ниже команду:</span><span class="sxs-lookup"><span data-stu-id="bdda7-110">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="bdda7-111">Чтобы запустить Azure PowerShell в PowerShell 5.1 на платформе Windows, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="bdda7-111">To run Azure PowerShell in PowerShell 5.1 on Windows:</span></span>

1. <span data-ttu-id="bdda7-112">При необходимости выполните обновление до [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="bdda7-112">Update to [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) if needed.</span></span> <span data-ttu-id="bdda7-113">Если вы используете Windows 10, среда PowerShell 5.1 уже установлена.</span><span class="sxs-lookup"><span data-stu-id="bdda7-113">If you're on Windows 10, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="bdda7-114">[Установите платформу .NET Framework версии 4.7.2 или более поздней](/dotnet/framework/install).</span><span class="sxs-lookup"><span data-stu-id="bdda7-114">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>

<span data-ttu-id="bdda7-115">При использовании PowerShell Core для Azure PowerShell нет дополнительных требований.</span><span class="sxs-lookup"><span data-stu-id="bdda7-115">There are no additional requirements for Azure PowerShell when using PowerShell Core.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="bdda7-116">Установка модуля Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="bdda7-116">Install the Azure PowerShell module</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="bdda7-117">Модули AzureRM и Az могут быть установлены одновременно.</span><span class="sxs-lookup"><span data-stu-id="bdda7-117">You can have both the AzureRM and Az modules installed at the same time.</span></span> <span data-ttu-id="bdda7-118">Если у вас установлены оба модуля, __не включайте псевдонимы__.</span><span class="sxs-lookup"><span data-stu-id="bdda7-118">If you have both modules installed, __don't enable aliases__.</span></span>
> <span data-ttu-id="bdda7-119">Включение псевдонимов приведет к конфликтам между командлетами AzureRM и псевдонимами команд Az с непредсказуемыми результатами.</span><span class="sxs-lookup"><span data-stu-id="bdda7-119">Enabling aliases will cause conflicts between AzureRM cmdlets and Az command aliases, and could cause unexpected behavior.</span></span>
> <span data-ttu-id="bdda7-120">Перед установкой модуля Az рекомендуется удалить AzureRM.</span><span class="sxs-lookup"><span data-stu-id="bdda7-120">It's recommended that before installing the Az module, you uninstall AzureRM.</span></span> <span data-ttu-id="bdda7-121">Удалить AzureRM или включить псевдонимы можно в любое время.</span><span class="sxs-lookup"><span data-stu-id="bdda7-121">You can always uninstall AzureRM or enable aliases at any time.</span></span> <span data-ttu-id="bdda7-122">Дополнительные сведения о псевдонимах команд AzureRM см. в статье [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md) (Миграция с AzureRM на Az для Azure PowerShell).</span><span class="sxs-lookup"><span data-stu-id="bdda7-122">To learn about the AzureRM command aliases, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
> <span data-ttu-id="bdda7-123">Инструкции по удалению см. в разделе [Uninstall the AzureRM module](uninstall-az-ps.md#uninstall-the-azurerm-module) (Удаление модуля AzureRM).</span><span class="sxs-lookup"><span data-stu-id="bdda7-123">For uninstall instructions, see [Uninstall the AzureRM module](uninstall-az-ps.md#uninstall-the-azurerm-module).</span></span> 

<span data-ttu-id="bdda7-124">Чтобы установить модули в глобальной области видимости, необходим более высокий уровень привилегий для установки модулей из коллекции PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bdda7-124">To install modules at a global scope, you need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="bdda7-125">Чтобы установить Azure PowerShell, выполните следующую команду в сеансе с более высоким уровнем привилегий ("Запуск от имени администратора" в Windows или с правами суперпользователя в macOS или Linux):</span><span class="sxs-lookup"><span data-stu-id="bdda7-125">To install Azure PowerShell, run the following command in an elevated session ("Run as Administrator" on Windows, or with superuser privileges on macOS or Linux):</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

<span data-ttu-id="bdda7-126">Если у вас нет доступа к привилегиям администратора, можно выполнить установку для текущего пользователя, добавив аргумент `-Scope`.</span><span class="sxs-lookup"><span data-stu-id="bdda7-126">If you don't have access to administrator privileges, you can install for the current user by adding the `-Scope` argument.</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="bdda7-127">По умолчанию коллекция PowerShell не используется как доверенный репозиторий для PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="bdda7-127">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="bdda7-128">При первом использовании PSGallery отображается следующее сообщение:</span><span class="sxs-lookup"><span data-stu-id="bdda7-128">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="bdda7-129">Ответьте `Yes` или `Yes to All`, чтобы продолжить установку.</span><span class="sxs-lookup"><span data-stu-id="bdda7-129">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="bdda7-130">Модуль Az — это общий модуль для командлетов Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bdda7-130">The Az module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="bdda7-131">Во время его установки скачиваются все доступные модули Azure Resource Manager и устанавливаются все соответствующие командлеты.</span><span class="sxs-lookup"><span data-stu-id="bdda7-131">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="bdda7-132">Вход</span><span class="sxs-lookup"><span data-stu-id="bdda7-132">Sign in</span></span>

<span data-ttu-id="bdda7-133">Чтобы начать работу с Azure PowerShell, выполните вход, используя данные своей учетной записи в Azure.</span><span class="sxs-lookup"><span data-stu-id="bdda7-133">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> <span data-ttu-id="bdda7-134">Если вы отключили автоматическую загрузку модулей, вам нужно вручную импортировать модуль с помощью `Import-Module Az`.</span><span class="sxs-lookup"><span data-stu-id="bdda7-134">If you've disabled module autoloading, you need to manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="bdda7-135">Из-за структуры модуля эта операция может занять несколько секунд.</span><span class="sxs-lookup"><span data-stu-id="bdda7-135">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="bdda7-136">Эти действия нужно повторять для каждого нового сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bdda7-136">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="bdda7-137">Чтобы узнать, как повторно использовать свои данные для входа в Azure в разных сеансах PowerShell, см. статью [Использование учетных данных пользователя в разных сеансах PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="bdda7-137">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="bdda7-138">Обновление модуля Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="bdda7-138">Update the Azure PowerShell module</span></span>

<span data-ttu-id="bdda7-139">Команда [Update-Module](/powershell/module/powershellget/update-module) не обновит установку надлежащим образом из-за способа упаковки модуля Az.</span><span class="sxs-lookup"><span data-stu-id="bdda7-139">Because of how the Az module is package, the [Update-Module](/powershell/module/powershellget/update-module) command won't update your installation correctly.</span></span> <span data-ttu-id="bdda7-140">С технической точки зрения Az является метамодулем, включающим все подмодули, содержащие командлеты, необходимые для взаимодействия со службами Azure.</span><span class="sxs-lookup"><span data-stu-id="bdda7-140">Az is technically a meta-module, encompassing all of the submodules that contain cmdlets to interact with Azure services.</span></span> <span data-ttu-id="bdda7-141">Это означает, что для обновления модуля Azure PowerShell его необходимо __переустановить__, а не просто __выполнить обновление__.</span><span class="sxs-lookup"><span data-stu-id="bdda7-141">That means that to update the Azure PowerShell module, you will need to __reinstall__, rather than just __update__.</span></span> <span data-ttu-id="bdda7-142">Эта процедура ничем не отличается от установки, но может потребоваться добавить аргумент `-Force`:</span><span class="sxs-lookup"><span data-stu-id="bdda7-142">This is done in the same way as installing, but you may need to add the `-Force` argument:</span></span>

```powershell
Install-Module -Name Az -AllowClobber -Force
```

<span data-ttu-id="bdda7-143">Хотя это может перезаписать установленные модули, в системе по-прежнему могут остаться более старые версии.</span><span class="sxs-lookup"><span data-stu-id="bdda7-143">Although this can overwrite installed modules, you may still have older versions left on your system.</span></span>
<span data-ttu-id="bdda7-144">Сведения о том, как удалить из системы предыдущие версии Azure PowerShell, см. в статье [Uninstall the Azure PowerShell module](uninstall-az-ps.md) (Удаление модуля Azure PowerShell).</span><span class="sxs-lookup"><span data-stu-id="bdda7-144">To learn how to remove old versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="bdda7-145">Использование нескольких версий Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="bdda7-145">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="bdda7-146">Вы можете установить несколько версий Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bdda7-146">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="bdda7-147">Чтобы проверить наличие нескольких установленных версий Azure PowerShell, используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="bdda7-147">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

<span data-ttu-id="bdda7-148">Сведения о том, как удалить версию Azure PowerShell, см. в статье [Удаление модуля Azure PowerShell](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="bdda7-148">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

<span data-ttu-id="bdda7-149">Определенную версию модуля `Az` можно установить или загрузить с помощью аргумента `-RequiredVersion`.</span><span class="sxs-lookup"><span data-stu-id="bdda7-149">You can install or load a specific version of the `Az` module by using the `-RequiredVersion` argument:</span></span>

```powershell-interactive
# Install Az version 0.7.0
Install-Module -Name Az -RequiredVersion 0.7.0 
# Load Az version 0.7.0
Import-Module -Name Az -RequiredVersion 0.7.0
```

<span data-ttu-id="bdda7-150">Если у вас установлено несколько версий модуля, модуль автозагрузки и `Import-Module` загрузит последнюю версию по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bdda7-150">If you have more than one version of the module installed, module autoload and `Import-Module` load the latest version by default.</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="bdda7-151">Отзывы</span><span class="sxs-lookup"><span data-stu-id="bdda7-151">Provide feedback</span></span>

<span data-ttu-id="bdda7-152">Если вы нашли ошибку при работе с Azure Powershell, сообщите о ней [на сайте GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="bdda7-152">If you find a bug in Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="bdda7-153">Чтобы отправить отзыв из командной строки, используйте командлет [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="bdda7-153">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="bdda7-154">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="bdda7-154">Next Steps</span></span>

<span data-ttu-id="bdda7-155">Дополнительные сведения о модулях Azure PowerShell и их функциях см. в статье [Get Started with Azure PowerShell](get-started-azureps.md) (Начало работы с Azure PowerShell).</span><span class="sxs-lookup"><span data-stu-id="bdda7-155">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>
<span data-ttu-id="bdda7-156">Если вы знакомы с Azure PowerShell и вам необходимо мигрировать из AzureRM, см. статью [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md) (Миграция с AzureRM на Az).</span><span class="sxs-lookup"><span data-stu-id="bdda7-156">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
