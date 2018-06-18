---
title: Установка Azure PowerShell с помощью PowerShellGet
description: Инструкции по установке Azure PowerShell с помощью PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/31/2018
ms.openlocfilehash: 9b7046157e32a5c8473210e9840f9ae1b2f45902
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323107"
---
# <a name="install-azure-powershell-with-powershellget"></a><span data-ttu-id="304a8-103">Установка Azure PowerShell с помощью PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="304a8-103">Install Azure PowerShell with PowerShellGet</span></span>

<span data-ttu-id="304a8-104">В этой статье содержатся инструкции по установке модулей Azure PowerShell в среде Windows с помощью PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="304a8-104">This article explains the steps to install the Azure PowerShell modules in a Windows environment using PowerShellGet.</span></span>  <span data-ttu-id="304a8-105">Это предпочтительный способ установки Azure PowerShell, но если вы хотите использовать для установки пакет MSI или установщик веб-платформы, см. раздел [Другие способы установки](other-install.md).</span><span class="sxs-lookup"><span data-stu-id="304a8-105">This is the preferred way to install Azure PowerShell, but if you would rather install with the Web Platform Installer or MSI package, see [Other installation methods](other-install.md).</span></span>

<span data-ttu-id="304a8-106">Если вы хотите использовать Azure PowerShell в macOS или Linux, ознакомьтесь со следующей статьей: [Установка и настройка Azure PowerShell в macOS и Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="304a8-106">If you want to use Azure PowerShell on macOS or Linux, see the following article: [Install and configure Azure PowerShell on macOS and Linux](install-azurermps-maclinux.md).</span></span>

## <a name="system-requirements"></a><span data-ttu-id="304a8-107">Требования к системе</span><span class="sxs-lookup"><span data-stu-id="304a8-107">System requirements</span></span>

<span data-ttu-id="304a8-108">Для работы с Azure PowerShell версии 6.1.0 требуется PowerShell версии 5.0 (или выше).</span><span class="sxs-lookup"><span data-stu-id="304a8-108">Azure PowerShell version 6.1.0 requires version 5.0 (or higher) of PowerShell.</span></span> <span data-ttu-id="304a8-109">Сведения об обновлении до версии PowerShell 5.0 см. в разделе [Обновление существующей версии Windows PowerShell](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="304a8-109">For information on upgrading to PowerShell 5.0, see [Upgrading existing Windows PowerShell](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span></span>

<span data-ttu-id="304a8-110">PowerShellGet автоматически входит в состав PowerShell 5.0.</span><span class="sxs-lookup"><span data-stu-id="304a8-110">PowerShellGet is automatically included as part of PowerShell 5.0.</span></span>

## <a name="install-or-update-the-azure-powershell-module"></a><span data-ttu-id="304a8-111">Установка или обновление модуля Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="304a8-111">Install or update the Azure PowerShell module</span></span>

<span data-ttu-id="304a8-112">Для установки Azure PowerShell из коллекции PowerShell требуются повышенные права.</span><span class="sxs-lookup"><span data-stu-id="304a8-112">Installing Azure PowerShell from the PowerShell Gallery requires elevated privileges.</span></span> <span data-ttu-id="304a8-113">Выполните следующую команду PowerShell с повышенными правами:</span><span class="sxs-lookup"><span data-stu-id="304a8-113">Run the following command from an elevated PowerShell session:</span></span>

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

> [!IMPORTANT]
> <span data-ttu-id="304a8-114">В результате использования этой команды любая существующая в вашей системе версия модуля Azure PowerShell будет обновлена.</span><span class="sxs-lookup"><span data-stu-id="304a8-114">This command will update any existing installation of Azure PowerShell on your system.</span></span> <span data-ttu-id="304a8-115">Если необходимо установить несколько версий, перейдите в раздел часто задаваемых вопросов и найдите ответ на вопрос [Можно ли установить несколько версий Azure PowerShell?](#multiple-versions).</span><span class="sxs-lookup"><span data-stu-id="304a8-115">If you need to have more than one version installed, see the FAQ answer for [Can I install multiple versions of Azure PowerShell?](#multiple-versions)</span></span>

<span data-ttu-id="304a8-116">По умолчанию коллекция PowerShell не настроена как доверенный репозиторий для PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="304a8-116">By default, the PowerShell gallery is not configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="304a8-117">При первом использовании PSGallery отображается следующее сообщение:</span><span class="sxs-lookup"><span data-stu-id="304a8-117">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="304a8-118">Ответьте "Да" или "Да для всех", чтобы продолжить установку.</span><span class="sxs-lookup"><span data-stu-id="304a8-118">Answer 'Yes' or 'Yes to All' to continue with the installation.</span></span>

> [!NOTE]
> <span data-ttu-id="304a8-119">Если установленная версия NuGet предшествует версии 2.8.5.201, вам будет предложено скачать и установить последнюю версию NuGet.</span><span class="sxs-lookup"><span data-stu-id="304a8-119">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="304a8-120">Модуль AzureRM — это набор командлетов для работы с Azure Resource Manager. </span><span class="sxs-lookup"><span data-stu-id="304a8-120">The AzureRM module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="304a8-121">При установке модуля AzureRM любой модуль Azure PowerShell, который ранее не был установлен, скачивается из коллекции PowerShell.</span><span class="sxs-lookup"><span data-stu-id="304a8-121">When you install the AzureRM module, any Azure PowerShell module not previously installed is downloaded from the PowerShell Gallery.</span></span>

## <a name="load-the-azure-powershell-module"></a><span data-ttu-id="304a8-122">Загрузка модуля Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="304a8-122">Load the Azure PowerShell module</span></span>

<span data-ttu-id="304a8-123">После установки модуля его необходимо загрузить в сеанс PowerShell.</span><span class="sxs-lookup"><span data-stu-id="304a8-123">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="304a8-124">Это необходимо сделать в обычном (без повышенных привилегий) сеансе PowerShell.</span><span class="sxs-lookup"><span data-stu-id="304a8-124">You should do this in a normal (non-elevated) PowerShell session.</span></span> <span data-ttu-id="304a8-125">Модули можно загрузить с помощью командлета `Import-Module` следующим образом:</span><span class="sxs-lookup"><span data-stu-id="304a8-125">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module -Name AzureRM
```

## <a name="reporting-issues-and-feedback"></a><span data-ttu-id="304a8-126">Создание отчетов о проблемах и обратная связь</span><span class="sxs-lookup"><span data-stu-id="304a8-126">Reporting issues and feedback</span></span>

<span data-ttu-id="304a8-127">При возникновении каких-либо ошибок в работе средства [сообщите о проблеме на сайте GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="304a8-127">If you encounter any bugs with the tool, please [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span> <span data-ttu-id="304a8-128">Чтобы отправить отзыв из командной строки, используйте командлет `Send-Feedback`.</span><span class="sxs-lookup"><span data-stu-id="304a8-128">To provide feedback from the command line, use the `Send-Feedback` cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="304a8-129">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="304a8-129">Next Steps</span></span>

<span data-ttu-id="304a8-130">Дополнительные сведения об использовании Azure PowerShell см. в следующей статье:</span><span class="sxs-lookup"><span data-stu-id="304a8-130">For more information about using Azure PowerShell, see the following articles:</span></span>

* <span data-ttu-id="304a8-131">[Getting started with Azure PowerShell](get-started-azureps.md) (Приступая к работе с Azure PowerShell)</span><span class="sxs-lookup"><span data-stu-id="304a8-131">[Get started with Azure PowerShell](get-started-azureps.md)</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="304a8-132">Часто задаваемые вопросы</span><span class="sxs-lookup"><span data-stu-id="304a8-132">Frequently asked questions</span></span>

### <a id="helpmechoose"></a><span data-ttu-id="304a8-133">Как проверить версию Azure PowerShell?</span><span class="sxs-lookup"><span data-stu-id="304a8-133">How do I check the version of Azure PowerShell?</span></span>

<span data-ttu-id="304a8-134">Хотя мы советуем выполнить обновление до последней версии как можно скорее, поддерживается несколько версий Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="304a8-134">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are supported.</span></span> <span data-ttu-id="304a8-135">Чтобы определить, какая версия Azure PowerShell установлена, выполните в командной строке команду `Get-Module AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="304a8-135">To determine the version of Azure PowerShell you have installed, run `Get-Module AzureRM` from your command line.</span></span>

```powershell
Get-Module AzureRM -ListAvailable | Select-Object -Property Name,Version,Path
```

### <a name="can-i-use-azure-powershell-for-azure-classic-deployments"></a><span data-ttu-id="304a8-136">Можно ли использовать Azure PowerShell для классических развертываний Azure?</span><span class="sxs-lookup"><span data-stu-id="304a8-136">Can I use Azure PowerShell for Azure Classic deployments?</span></span>

<span data-ttu-id="304a8-137">При наличии экземпляров, развернутых с помощью классической модели, вы можете установить Azure PowerShell для управления службами.</span><span class="sxs-lookup"><span data-stu-id="304a8-137">If you have deployments that use the classic deployment model you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="304a8-138">Дополнительные сведения см. в статье об [установке модуля управления службами Azure PowerShell](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="304a8-138">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span> <span data-ttu-id="304a8-139">Модули Azure и AzureRM имеют общие зависимости.</span><span class="sxs-lookup"><span data-stu-id="304a8-139">The Azure and AzureRM modules share common dependencies.</span></span> <span data-ttu-id="304a8-140">При использовании обоих модулей (Azure и AzureRM) необходимо установить одинаковую версию каждого пакета.</span><span class="sxs-lookup"><span data-stu-id="304a8-140">If you use both the Azure and AzureRM modules, you should install the same version of each package.</span></span>

### <a name="a-namemultiple-versionscan-i-install-multiple-versions-of-azure-powershell"></a><span data-ttu-id="304a8-141"><a name="multiple-versions"/>Можно ли установить несколько версий Azure PowerShell?</span><span class="sxs-lookup"><span data-stu-id="304a8-141"><a name="multiple-versions"/>Can I install multiple versions of Azure PowerShell?</span></span>

<span data-ttu-id="304a8-142">Установка с помощью PowerShellGet — единственный способ, поддерживающий установку нескольких версий.</span><span class="sxs-lookup"><span data-stu-id="304a8-142">PowerShellGet the only method of installation that supports multiple versions.</span></span> <span data-ttu-id="304a8-143">Для установки нескольких версий необходимо добавить параметр `-RequiredVersion` в командлет `Install-Module`.</span><span class="sxs-lookup"><span data-stu-id="304a8-143">To install multiple versions, you can add the `-RequiredVersion` parameter to the `Install-Module` cmdlet.</span></span> <span data-ttu-id="304a8-144">Ниже показан пример для установки версий 6.1.0 и 1.2.9:</span><span class="sxs-lookup"><span data-stu-id="304a8-144">For example, to install both versions 6.1.0 and 1.2.9:</span></span>

```powershell
Install-Module -Name AzureRM -RequiredVersion 6.1.0
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

<span data-ttu-id="304a8-145">В сеанс PowerShell можно загрузить только одну версию модуля.</span><span class="sxs-lookup"><span data-stu-id="304a8-145">Only one version of the module can be loaded in a PowerShell session.</span></span> <span data-ttu-id="304a8-146">Необходимо открыть новое окно PowerShell и с помощью команды `Import-Module` импортировать определенную версию модуля Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="304a8-146">You must open a new PowerShell window and use `Import-Module` to import a specific version of the Azure PowerShell module.</span></span>

```powershell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

> [!NOTE]
> <span data-ttu-id="304a8-147">Версии 2.1.0 и 1.2.6 — это первые версии модуля, предназначенные для установки и использования без удаления предыдущей версии.</span><span class="sxs-lookup"><span data-stu-id="304a8-147">Version 2.1.0 and version 1.2.6 are the first module versions designed to be installed and used side by side.</span></span> <span data-ttu-id="304a8-148">Если загрузить более раннюю версию модуля Azure PowerShell, то загрузится несовместимая версия модуля **AzureRM.Profile**.</span><span class="sxs-lookup"><span data-stu-id="304a8-148">When loading an earlier version of the Azure PowerShell, incompatible versions of the **AzureRM.Profile** module are loaded.</span></span> <span data-ttu-id="304a8-149">Это приведет к тому, что командлеты будут запрашивать выполнить вход при каждом выполнении командлета.</span><span class="sxs-lookup"><span data-stu-id="304a8-149">This results in the cmdlets prompting you to log in whenever you execute a cmdlet.</span></span>
