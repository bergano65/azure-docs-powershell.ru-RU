---
title: Установка Azure PowerShell в ОС Windows с помощью PowerShellGet
description: Инструкции по установке Azure PowerShell с помощью PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/15/2018
ms.openlocfilehash: a868a62bd7bb2f39775a3b7878e2c8484c50438d
ms.sourcegitcommit: 06f9206e025afa7207d4657c8f57c94ddb74817a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2018
ms.locfileid: "51211100"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a><span data-ttu-id="30655-103">Установка Azure PowerShell в ОС Windows с помощью PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="30655-103">Install Azure PowerShell on Windows with PowerShellGet</span></span>

<span data-ttu-id="30655-104">В этой статье содержатся инструкции по установке модулей Azure PowerShell в среде Windows с помощью PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="30655-104">This article explains the steps to install the Azure PowerShell modules in a Windows environment using PowerShellGet.</span></span> <span data-ttu-id="30655-105">PowerShellGet и управление модулями — это предпочтительный способ установки Azure PowerShell, но если вы хотите использовать для установки пакет MSI или установщик веб-платформы, см. статью о [других способах установки](other-install.md).</span><span class="sxs-lookup"><span data-stu-id="30655-105">PowerShellGet and module management is the preferred way to install Azure PowerShell but if you would rather install with the Web Platform Installer or MSI package, see [Other installation methods](other-install.md).</span></span>

<span data-ttu-id="30655-106">Инструкции по установке Azure PowerShell на других платформах см. в статье [Установка Azure PowerShell в macOS или Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="30655-106">For instructions to install Azure PowerShell on other platforms, see [Install and configure Azure PowerShell on macOS and Linux](install-azurermps-maclinux.md).</span></span>

<span data-ttu-id="30655-107">Эта версия Azure PowerShell не поддерживает классическую модель развертывания Azure.</span><span class="sxs-lookup"><span data-stu-id="30655-107">The Azure classic deployment model is not supported by this version of Azure PowerShell.</span></span> <span data-ttu-id="30655-108">Если вам нужна поддержка классического развертывания, см. статью [Установка модуля управления службами Azure PowerShell](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="30655-108">For support for classic deployments, follow the instructions in [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>

## <a name="requirements"></a><span data-ttu-id="30655-109">Требования</span><span class="sxs-lookup"><span data-stu-id="30655-109">Requirements</span></span>

<span data-ttu-id="30655-110">Чтобы установить Azure PowerShell, требуется PowerShellGet начиная с версии 1.1.2.0.</span><span class="sxs-lookup"><span data-stu-id="30655-110">To install Azure PowerShell, you need PowerShellGet version 1.1.2.0 or higher.</span></span> <span data-ttu-id="30655-111">Чтобы проверить свою систему на наличие этого компонента, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="30655-111">To check if it is available on your system, run the following command:</span></span>

```powershell-interactive
Get-Module -Name PowerShellGet -ListAvailable | Select-Object -Property Name,Version,Path
```

<span data-ttu-id="30655-112">Должен отобразиться результат, аналогичный следующему:</span><span class="sxs-lookup"><span data-stu-id="30655-112">You should see something similar to the following output:</span></span>

```output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="30655-113">Чтобы обновить свою версию PowerShellGet, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="30655-113">If you need to update your installation of PowerShellGet, run the following command:</span></span>

```powershell-interactive
Install-Module PowerShellGet -Force
```

<span data-ttu-id="30655-114">Если компонент PowerShellGet не установлен, следуйте инструкциям для своей системы из таблицы ниже.</span><span class="sxs-lookup"><span data-stu-id="30655-114">If you don't have PowerShellGet installed, follow the instructions in the table below for your system.</span></span>

|<span data-ttu-id="30655-115">Сценарий</span><span class="sxs-lookup"><span data-stu-id="30655-115">Scenario</span></span>|<span data-ttu-id="30655-116">Инструкции по установке</span><span class="sxs-lookup"><span data-stu-id="30655-116">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="30655-117">Windows 10</span><span class="sxs-lookup"><span data-stu-id="30655-117">Windows 10</span></span><br/><span data-ttu-id="30655-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="30655-118">Windows Server 2016</span></span>|<span data-ttu-id="30655-119">Встроен в пакет Windows Management Framework (WMF) 5.0, который входит в состав ОС</span><span class="sxs-lookup"><span data-stu-id="30655-119">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="30655-120">Обновление до PowerShell 5</span><span class="sxs-lookup"><span data-stu-id="30655-120">Upgrade to PowerShell 5</span></span>| <ol><li>[<span data-ttu-id="30655-121">Установите последнюю версию WMF</span><span class="sxs-lookup"><span data-stu-id="30655-121">Install the latest version of WMF</span></span>](https://www.microsoft.com/en-us/download/details.aspx?id=54616)</li><li><span data-ttu-id="30655-122">Выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="30655-122">Run the following command:</span></span><br/>```Install-Module PowerShellGet -Force```</li></ol>|
|<span data-ttu-id="30655-123">Windows с PowerShell 3 или PowerShell 4</span><span class="sxs-lookup"><span data-stu-id="30655-123">Windows with PowerShell 3 or PowerShell 4</span></span>|<ol><span data-ttu-id="30655-124"><il>[Получите модули PackageManagement:](http://go.microsoft.com/fwlink/?LinkID=746217)</il></span><span class="sxs-lookup"><span data-stu-id="30655-124"><il>[Get the PackageManagement modules](http://go.microsoft.com/fwlink/?LinkID=746217)</il></span></span><li><span data-ttu-id="30655-125">Выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="30655-125">Run the following command:</span></span><br/>```Install-Module PowerShellGet -Force```</li></ol>|

> [!NOTE]
> <span data-ttu-id="30655-126">Чтобы использовать PowerShellGet, необходимо иметь политику выполнения, которая позволяет запускать сценарии.</span><span class="sxs-lookup"><span data-stu-id="30655-126">Using PowerShellGet requires an Execution Policy that allows you to run scripts.</span></span> <span data-ttu-id="30655-127">Дополнительные сведения о политике выполнения PowerShell см. в [этой статье](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span><span class="sxs-lookup"><span data-stu-id="30655-127">For more information about PowerShell's Execution Policy, see [About Execution Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span></span>
>
> [!IMPORTANT]
> <span data-ttu-id="30655-128">Для модуля AzureRM, описанном в этом документе, используется .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="30655-128">The module described in this document, AzureRM, uses .NET Framework.</span></span> <span data-ttu-id="30655-129">Из-за этого модуль несовместимым с PowerShell версии 6.0, для которой используется .NET Core.</span><span class="sxs-lookup"><span data-stu-id="30655-129">This makes it incompatible with PowerShell 6.0, which uses .NET Core.</span></span> <span data-ttu-id="30655-130">Если вы используете PowerShell 6.0, изучите [инструкции по установке для macOS и Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="30655-130">If you are using PowerShell 6.0, follow the [installation instructions for macOS and Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="30655-131">Установка модуля Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="30655-131">Install the Azure PowerShell module</span></span>

<span data-ttu-id="30655-132">Для установки модулей из коллекции PowerShell требуется более высокий уровень привилегий.</span><span class="sxs-lookup"><span data-stu-id="30655-132">You need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="30655-133">Чтобы установить Azure PowerShell, в сеансе с более высоким уровнем привилегий выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="30655-133">To install Azure PowerShell, run the following command in an elevated session:</span></span>

```powershell-interactive
Install-Module -Name AzureRM
```

> [!NOTE]
> <span data-ttu-id="30655-134">Если установленная версия NuGet предшествует версии 2.8.5.201, вам будет предложено скачать и установить последнюю версию NuGet.</span><span class="sxs-lookup"><span data-stu-id="30655-134">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="30655-135">По умолчанию коллекция PowerShell не используется как доверенный репозиторий для PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="30655-135">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="30655-136">При первом использовании PSGallery отображается следующее сообщение:</span><span class="sxs-lookup"><span data-stu-id="30655-136">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="30655-137">Ответьте `Yes` или `Yes to All`, чтобы продолжить установку.</span><span class="sxs-lookup"><span data-stu-id="30655-137">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="30655-138">Модуль `AzureRM` — это общий модуль для командлетов Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="30655-138">The `AzureRM` module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="30655-139">Во время его установки скачиваются все доступные модули Azure Resource Manager и устанавливаются все соответствующие командлеты.</span><span class="sxs-lookup"><span data-stu-id="30655-139">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="30655-140">Вход</span><span class="sxs-lookup"><span data-stu-id="30655-140">Sign in</span></span>

<span data-ttu-id="30655-141">Чтобы приступить к работе с Azure PowerShell, вам нужно загрузить `AzureRM` в текущий сеанс PowerShell. Для этого воспользуйтесь командлетом [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), после чего войдите в систему с помощью своих учетных данных Azure.</span><span class="sxs-lookup"><span data-stu-id="30655-141">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="30655-142">Эти действия нужно повторять для каждого нового сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="30655-142">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="30655-143">Чтобы автоматически импортировать модуль `AzureRM`, необходимо настроить профиль PowerShell. Подробнее об этом рассказывается [здесь](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="30655-143">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="30655-144">Чтобы узнать, как повторно использовать свои данные для входа в Azure в разных сеансах, см. статью [Использование учетных данных пользователя в разных сеансах PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="30655-144">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="30655-145">Обновление модуля Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="30655-145">Update the Azure PowerShell module</span></span>

<span data-ttu-id="30655-146">Чтобы обновить версию Azure PowerShell, выполните команду [Update-Module](/powershell/module/powershellget/update-module).</span><span class="sxs-lookup"><span data-stu-id="30655-146">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="30655-147">Эта команда __не__ удаляет предыдущие версии.</span><span class="sxs-lookup"><span data-stu-id="30655-147">This command does __not__ uninstall earlier versions.</span></span>

```powershell-interactive
Update-Module -Name AzureRM
```

<span data-ttu-id="30655-148">Сведения о том, как удалить из системы предыдущие версии Azure PowerShell, см. в статье [Удаление модуля Azure PowerShell](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="30655-148">If you want to remove older versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="30655-149">Использование нескольких версий Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="30655-149">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="30655-150">Вы можете установить несколько версий Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="30655-150">It's possible to install multiple versions of Azure PowerShell.</span></span> <span data-ttu-id="30655-151">Несколько версий могут понадобиться, если вы работаете с локальными ресурсами Azure Stack, пользуетесь версиями Windows, в которых невозможно обновить PowerShell до версии 5.0, или используете классическую модель развертывания Azure.</span><span class="sxs-lookup"><span data-stu-id="30655-151">You might need more than one version if you work with on-premises Azure Stack resources, run an older version of Windows that you can't update to PowerShell 5.0, or use the Azure classic deployment model.</span></span> <span data-ttu-id="30655-152">Чтобы установить более раннюю версию, при установке укажите аргумент `-RequiredVersion`.</span><span class="sxs-lookup"><span data-stu-id="30655-152">To install an older version, provide the `-RequiredVersion` argument when installing.</span></span>

```powershell-interactive
# Install version 1.2.9 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

<span data-ttu-id="30655-153">По умолчанию всегда загружается модуль Azure PowerShell последней версии.</span><span class="sxs-lookup"><span data-stu-id="30655-153">When loading the Azure PowerShell module the latest version is loaded by default.</span></span> <span data-ttu-id="30655-154">Чтобы загрузить другую версию, укажите аргумент `-RequiredVersion`.</span><span class="sxs-lookup"><span data-stu-id="30655-154">To load a different version, provide the `-RequiredVersion` argument.</span></span>

```powershell-interactive
# Load version 1.2.9 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

## <a name="provide-feedback"></a><span data-ttu-id="30655-155">Отзывы</span><span class="sxs-lookup"><span data-stu-id="30655-155">Provide feedback</span></span>

<span data-ttu-id="30655-156">Если вы нашли ошибку при работе с Azure Powershell, [сообщите о ней на сайте GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="30655-156">If you find a bug when using Azure Powershell, please [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="30655-157">Чтобы отправить отзыв из командной строки, используйте командлет [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="30655-157">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="30655-158">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="30655-158">Next Steps</span></span>

<span data-ttu-id="30655-159">Сведения о начале работы с Azure PowerShell см. в [этой статье](get-started-azureps.md). Она содержит более подробную информацию о модуле и его компонентах.</span><span class="sxs-lookup"><span data-stu-id="30655-159">To get started using Azure PowerShell, see [Get Started with Azure PowerShell](get-started-azureps.md) to learn more about the module and its features.</span></span>