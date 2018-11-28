---
title: Установка модуля Az для Azure PowerShell с помощью PowerShellGet
description: Сведения об установке Azure PowerShell с помощью PowerShellGet в Windows, macOS и Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/16/2018
ms.openlocfilehash: 32e96c6459c9db0c4b9eda0cc170c85ba99a22ca
ms.sourcegitcommit: 80a3da199954d0ab78765715fb49793e89a30f12
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/22/2018
ms.locfileid: "52260018"
---
# <a name="install-the-azure-powershell-az-module"></a><span data-ttu-id="5d917-103">Установка модуля Az для Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="5d917-103">Install the Azure PowerShell 'Az' module</span></span>

<span data-ttu-id="5d917-104">В этой статье рассказывается, как установить модули Azure PowerShell с помощью PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="5d917-104">This article tells you how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="5d917-105">Эти инструкции применимы для платформ Windows, macOS и Linux.</span><span class="sxs-lookup"><span data-stu-id="5d917-105">These instructions work on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="5d917-106">В предварительной версии модуля Az другие методы установки не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="5d917-106">For the preview release of Az, no other install methods are supported.</span></span> 

## <a name="requirements"></a><span data-ttu-id="5d917-107">Требования</span><span class="sxs-lookup"><span data-stu-id="5d917-107">Requirements</span></span>

<span data-ttu-id="5d917-108">Azure PowerShell работает с PowerShell 5.x в Windows, или PowerShell 6.x на любой платформе.</span><span class="sxs-lookup"><span data-stu-id="5d917-108">Azure PowerShell works with either PowerShell 5.x on Windows, or PowerShell 6.x on any platform.</span></span> <span data-ttu-id="5d917-109">Чтобы проверить установленную на своем компьютере версию PowerShell, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="5d917-109">To check the version of PowerShell running on your machine, run the following command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="5d917-110">Если вы используете старую версию или вам нужно установить PowerShell, см. статью [Установка разных версий PowerShell](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-powershell?view=powershell-6).</span><span class="sxs-lookup"><span data-stu-id="5d917-110">If you have an outdated version or need to install PowerShell, see [Installing various versions of PowerShell](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-powershell?view=powershell-6).</span></span> <span data-ttu-id="5d917-111">На этой странице вы найдете ссылки на сведения по установке для своей платформы.</span><span class="sxs-lookup"><span data-stu-id="5d917-111">Install information for your platform is linked from that page.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="5d917-112">Установка модуля Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="5d917-112">Install the Azure PowerShell module</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="5d917-113">Не рекомендуется одновременно устанавливать модули `AzureRM` и `Az` в системе.</span><span class="sxs-lookup"><span data-stu-id="5d917-113">You shouldn't have both the `AzureRM` and `Az` modules installed on a system at the same time.</span></span> <span data-ttu-id="5d917-114">Перед установкой модуля `Az` модуль `AzureRM` необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="5d917-114">In order to install the `Az` module, `AzureRM` must be uninstalled.</span></span> <span data-ttu-id="5d917-115">Соответствующие сведения см. в статье [об удалении модуля Azure PowerShell (AzureRM)](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="5d917-115">For instructions on how to do that, see [Uninstall the Azure PowerShell module (AzureRM)](uninstall-azurerm-ps.md).</span></span>

<span data-ttu-id="5d917-116">Чтобы установить модули в глобальной области видимости, необходим более высокий уровень привилегий для установки модулей из коллекции PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5d917-116">To install modules at a global scope, you need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="5d917-117">Чтобы установить Azure PowerShell, выполните следующую команду в сеансе с более высоким уровнем привилегий ("Запуск от имени администратора" в Windows или с правами суперпользователя в macOS или Linux):</span><span class="sxs-lookup"><span data-stu-id="5d917-117">To install Azure PowerShell, run the following command in an elevated session ("Run as Administrator" on Windows, or with superuser privileges on macOS or Linux):</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

<span data-ttu-id="5d917-118">Если у вас нет доступа к привилегиям администратора, можно выполнить установку для текущего пользователя, добавив аргумент `-Scope`.</span><span class="sxs-lookup"><span data-stu-id="5d917-118">If you don't have access to administrator privileges, you can install for the current user by adding the `-Scope` argument.</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="5d917-119">По умолчанию коллекция PowerShell не используется как доверенный репозиторий для PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="5d917-119">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="5d917-120">При первом использовании PSGallery отображается следующее сообщение:</span><span class="sxs-lookup"><span data-stu-id="5d917-120">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="5d917-121">Ответьте `Yes` или `Yes to All`, чтобы продолжить установку.</span><span class="sxs-lookup"><span data-stu-id="5d917-121">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="5d917-122">Модуль `Az` — это общий модуль для командлетов Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5d917-122">The `Az` module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="5d917-123">Во время его установки скачиваются все доступные модули Azure Resource Manager и устанавливаются все соответствующие командлеты.</span><span class="sxs-lookup"><span data-stu-id="5d917-123">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="5d917-124">Вход</span><span class="sxs-lookup"><span data-stu-id="5d917-124">Sign in</span></span>

<span data-ttu-id="5d917-125">Чтобы начать работу с Azure PowerShell, выполните вход, используя данные своей учетной записи в Azure.</span><span class="sxs-lookup"><span data-stu-id="5d917-125">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> <span data-ttu-id="5d917-126">Если вы отключили автоматическую загрузку модулей, вам нужно вручную импортировать модуль с помощью `Import-Module Az`.</span><span class="sxs-lookup"><span data-stu-id="5d917-126">If you've disabled module autoloading, you need to manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="5d917-127">Из-за структуры модуля эта операция может занять несколько секунд.</span><span class="sxs-lookup"><span data-stu-id="5d917-127">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="5d917-128">Эти действия нужно повторять для каждого нового сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5d917-128">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="5d917-129">Чтобы узнать, как повторно использовать свои данные для входа в Azure в разных сеансах PowerShell, см. статью [Использование учетных данных пользователя в разных сеансах PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="5d917-129">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="5d917-130">Обновление модуля Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="5d917-130">Update the Azure PowerShell module</span></span>

<span data-ttu-id="5d917-131">Чтобы обновить версию Azure PowerShell, выполните команду [Update-Module](/powershell/module/powershellget/update-module).</span><span class="sxs-lookup"><span data-stu-id="5d917-131">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="5d917-132">Эта команда __не__ удаляет предыдущие версии.</span><span class="sxs-lookup"><span data-stu-id="5d917-132">This command does __not__ uninstall earlier versions.</span></span>

```powershell-interactive
Update-Module -Name Az
```

<span data-ttu-id="5d917-133">Сведения о том, как удалить из системы предыдущие версии Azure PowerShell, см. в статье [Удаление модуля Azure PowerShell](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="5d917-133">If you want to remove older versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="5d917-134">Использование нескольких версий Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="5d917-134">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="5d917-135">Вы можете установить несколько версий Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5d917-135">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="5d917-136">Чтобы проверить наличие нескольких установленных версий Azure PowerShell, используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="5d917-136">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-Module -Name Az -List | select Name,Version
```

<span data-ttu-id="5d917-137">Сведения о том, как удалить версию Azure PowerShell, см. в статье [Удаление модуля Azure PowerShell](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="5d917-137">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

<span data-ttu-id="5d917-138">Вы можете загрузить определенную версию модуля `Az`, используя аргумент `-RequiredVersion` с командами `Install-Module` или `Import-Module`:</span><span class="sxs-lookup"><span data-stu-id="5d917-138">You can load a specific version of the `Az` module by using the `-RequiredVersion` argument with `Install-Module` and `Import-Module`:</span></span>

```powershell-interactive
Install-Module -Name Az -RequiredVersion 0.4.0
Import-Module -Name Az -RequiredVersion 0.4.0
```

<span data-ttu-id="5d917-139">Если у вас установлено несколько версий модуля, по умолчанию загружается последняя версия.</span><span class="sxs-lookup"><span data-stu-id="5d917-139">If you have more than one version of the module installed, the latest version is loaded by default.</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="5d917-140">Отзывы</span><span class="sxs-lookup"><span data-stu-id="5d917-140">Provide feedback</span></span>

<span data-ttu-id="5d917-141">Если вы нашли ошибку при работе с Azure Powershell, [сообщите о ней на сайте GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="5d917-141">If you find a bug when using Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="5d917-142">Чтобы отправить отзыв из командной строки, используйте командлет [Send-Feedback](/powershell/module/az.profile/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="5d917-142">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.profile/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="5d917-143">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="5d917-143">Next Steps</span></span>

<span data-ttu-id="5d917-144">Сведения о начале работы с Azure PowerShell см. в [этой статье](get-started-azureps.md). Она содержит более подробную информацию о модуле и его компонентах.</span><span class="sxs-lookup"><span data-stu-id="5d917-144">To get started using Azure PowerShell, see [Get Started with Azure PowerShell](get-started-azureps.md) to learn more about the module and its features.</span></span>
