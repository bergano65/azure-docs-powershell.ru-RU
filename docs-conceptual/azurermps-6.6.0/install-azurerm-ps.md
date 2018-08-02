---
title: Установка Azure PowerShell в ОС Windows с помощью PowerShellGet
description: Инструкции по установке Azure PowerShell с помощью PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/15/2018
ms.openlocfilehash: 50b05e5f25b6e3e1c815f6b26f1b53b84cd0b7da
ms.sourcegitcommit: fd11600079ee3844986552bccc4e274a231332b6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/02/2018
ms.locfileid: "39368081"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a><span data-ttu-id="2f67e-103">Установка Azure PowerShell в ОС Windows с помощью PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="2f67e-103">Install Azure PowerShell on Windows with PowerShellGet</span></span>

<span data-ttu-id="2f67e-104">В этой статье содержатся инструкции по установке модулей Azure PowerShell в среде Windows с помощью PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="2f67e-104">This article explains the steps to install the Azure PowerShell modules in a Windows environment using PowerShellGet.</span></span> <span data-ttu-id="2f67e-105">PowerShellGet и управление модулями — это предпочтительный способ установки Azure PowerShell, но если вы хотите использовать для установки пакет MSI или установщик веб-платформы, см. статью о [других способах установки](other-install.md).</span><span class="sxs-lookup"><span data-stu-id="2f67e-105">PowerShellGet and module management is the preferred way to install Azure PowerShell but if you would rather install with the Web Platform Installer or MSI package, see [Other installation methods](other-install.md).</span></span>

<span data-ttu-id="2f67e-106">Инструкции по установке Azure PowerShell на других платформах см. в статье [Установка Azure PowerShell в macOS или Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="2f67e-106">For instructions to install Azure PowerShell on other platforms, see [Install and configure Azure PowerShell on macOS and Linux](install-azurermps-maclinux.md).</span></span>

<span data-ttu-id="2f67e-107">Эта версия Azure PowerShell не поддерживает классическую модель развертывания Azure.</span><span class="sxs-lookup"><span data-stu-id="2f67e-107">The Azure classic deployment model is not supported by this version of Azure PowerShell.</span></span> <span data-ttu-id="2f67e-108">Если вам нужна поддержка классического развертывания, см. статью [Установка модуля управления службами Azure PowerShell](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="2f67e-108">For support for classic deployments, follow the instructions in [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>

## <a name="requirements"></a><span data-ttu-id="2f67e-109">Требования</span><span class="sxs-lookup"><span data-stu-id="2f67e-109">Requirements</span></span>

<span data-ttu-id="2f67e-110">Чтобы использовать Azure PowerShell версии 6.0 и выше, требуется установить PowerShell 5.0.</span><span class="sxs-lookup"><span data-stu-id="2f67e-110">Starting with Azure PowerShell version 6.0, Azure PowerShell requires PowerShell version 5.0.</span></span> <span data-ttu-id="2f67e-111">Чтобы проверить установленную на своем компьютере версию PowerShell, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="2f67e-111">To check the version of PowerShell running on your machine, run the following command:</span></span>

```powershell
$PSVersionTable.PSVersion
```

<span data-ttu-id="2f67e-112">Если у вас более старая версия, см. раздел [Обновление существующей версии Windows PowerShell](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="2f67e-112">If you have an outdated version, see [Upgrading existing Windows PowerShell](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2f67e-113">Для модуля AzureRM, описанном в этом документе, используется .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="2f67e-113">The module described in this document, AzureRM, uses .NET Framework.</span></span> <span data-ttu-id="2f67e-114">Из-за этого модуль несовместимым с PowerShell версии 6.0, для которой используется .NET Core.</span><span class="sxs-lookup"><span data-stu-id="2f67e-114">This makes it incompatible with PowerShell 6.0, which uses .NET Core.</span></span> <span data-ttu-id="2f67e-115">Если вы используете PowerShell 6.0, изучите [инструкции по установке для macOS и Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="2f67e-115">If you are using PowerShell 6.0, follow the [installation instructions for macOS and Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="2f67e-116">Установка модуля Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="2f67e-116">Install the Azure PowerShell module</span></span>

<span data-ttu-id="2f67e-117">Для установки модулей из коллекции PowerShell требуется более высокий уровень привилегий.</span><span class="sxs-lookup"><span data-stu-id="2f67e-117">You need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="2f67e-118">Чтобы установить Azure PowerShell, в сеансе с более высоким уровнем привилегий выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="2f67e-118">To install Azure PowerShell, run the following command in an elevated session:</span></span>

```powershell
Install-Module -Name AzureRM
```

> [!NOTE]
> <span data-ttu-id="2f67e-119">Если установленная версия NuGet предшествует версии 2.8.5.201, вам будет предложено скачать и установить последнюю версию NuGet.</span><span class="sxs-lookup"><span data-stu-id="2f67e-119">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="2f67e-120">По умолчанию коллекция PowerShell не используется как доверенный репозиторий для PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="2f67e-120">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="2f67e-121">При первом использовании PSGallery отображается следующее сообщение:</span><span class="sxs-lookup"><span data-stu-id="2f67e-121">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="2f67e-122">Ответьте `Yes` или `Yes to All`, чтобы продолжить установку.</span><span class="sxs-lookup"><span data-stu-id="2f67e-122">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="2f67e-123">Модуль `AzureRM` — это общий модуль для командлетов Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2f67e-123">The `AzureRM` module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="2f67e-124">Во время его установки скачиваются все доступные модули Azure Resource Manager и устанавливаются все соответствующие командлеты.</span><span class="sxs-lookup"><span data-stu-id="2f67e-124">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="2f67e-125">Вход</span><span class="sxs-lookup"><span data-stu-id="2f67e-125">Sign in</span></span>

<span data-ttu-id="2f67e-126">Чтобы приступить к работе с Azure PowerShell, вам нужно загрузить `AzureRM` в текущий сеанс PowerShell. Для этого воспользуйтесь командлетом [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), после чего войдите в систему с помощью своих учетных данных Azure.</span><span class="sxs-lookup"><span data-stu-id="2f67e-126">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="2f67e-127">Эти действия нужно повторять для каждого нового сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2f67e-127">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="2f67e-128">Чтобы автоматически импортировать модуль `AzureRM`, необходимо настроить профиль PowerShell. Подробнее об этом рассказывается [здесь](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="2f67e-128">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="2f67e-129">Чтобы узнать, как повторно использовать свои данные для входа в Azure в разных сеансах, см. статью [Использование учетных данных пользователя в разных сеансах PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="2f67e-129">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="2f67e-130">Обновление модуля Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="2f67e-130">Update the Azure PowerShell module</span></span>

<span data-ttu-id="2f67e-131">Чтобы обновить версию Azure PowerShell, выполните команду [Update-Module](/powershell/module/powershellget/update-module).</span><span class="sxs-lookup"><span data-stu-id="2f67e-131">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="2f67e-132">Эта команда __не__ удаляет предыдущие версии.</span><span class="sxs-lookup"><span data-stu-id="2f67e-132">This command does __not__ uninstall earlier versions.</span></span>

```powershell
Update-Module -Name AzureRM
```

<span data-ttu-id="2f67e-133">Сведения о том, как удалить из системы предыдущие версии Azure PowerShell, см. в статье [Удаление модуля Azure PowerShell](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="2f67e-133">If you want to remove older versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="2f67e-134">Использование нескольких версий Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="2f67e-134">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="2f67e-135">Вы можете установить несколько версий Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2f67e-135">It's possible to install multiple versions of Azure PowerShell.</span></span> <span data-ttu-id="2f67e-136">Несколько версий могут понадобиться, если вы работаете с локальными ресурсами Azure Stack, пользуетесь версиями Windows, в которых невозможно обновить PowerShell до версии 5.0, или используете классическую модель развертывания Azure.</span><span class="sxs-lookup"><span data-stu-id="2f67e-136">You might need more than one version if you work with on-premises Azure Stack resources, run an older version of Windows that you can't update to PowerShell 5.0, or use the Azure classic deployment model.</span></span> <span data-ttu-id="2f67e-137">Чтобы установить более раннюю версию, при установке укажите аргумент `-RequiredVersion`.</span><span class="sxs-lookup"><span data-stu-id="2f67e-137">To install an older version, provide the `-RequiredVersion` argument when installing.</span></span>

```powershell
# Install version 1.2.9 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

<span data-ttu-id="2f67e-138">По умолчанию всегда загружается модуль Azure PowerShell последней версии.</span><span class="sxs-lookup"><span data-stu-id="2f67e-138">When loading the Azure PowerShell module the latest version is loaded by default.</span></span> <span data-ttu-id="2f67e-139">Чтобы загрузить другую версию, укажите аргумент `-RequiredVersion`.</span><span class="sxs-lookup"><span data-stu-id="2f67e-139">To load a different version, provide the `-RequiredVersion` argument.</span></span>

```powershell
# Load version 1.2.9 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

## <a name="provide-feedback"></a><span data-ttu-id="2f67e-140">Отзывы</span><span class="sxs-lookup"><span data-stu-id="2f67e-140">Provide feedback</span></span>

<span data-ttu-id="2f67e-141">Если вы нашли ошибку при работе с Azure Powershell, [сообщите о ней на сайте GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="2f67e-141">If you find a bug when using Azure Powershell, please [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="2f67e-142">Чтобы отправить отзыв из командной строки, используйте командлет [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="2f67e-142">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="2f67e-143">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="2f67e-143">Next Steps</span></span>

<span data-ttu-id="2f67e-144">Сведения о начале работы с Azure PowerShell см. в [этой статье](get-started-azureps.md). Она содержит более подробную информацию о модуле и его компонентах.</span><span class="sxs-lookup"><span data-stu-id="2f67e-144">To get started using Azure PowerShell, see [Get Started with Azure PowerShell](get-started-azureps.md) to learn more about the module and its features.</span></span>