---
title: Установка и настройка Azure PowerShell | Документация Майкрософт
description: Как установить и настроить Azure PowerShell для первого использования.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/27/2018
ms.openlocfilehash: 5092440515f8c8fae8baefa6e3c5c856e48bb62c
ms.sourcegitcommit: ac4b53bb42a25aae013a9d8cd9ae98ada9397274
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/08/2018
ms.locfileid: "51275492"
---
# <a name="install-and-configure-azure-powershell"></a><span data-ttu-id="0a94d-103">Установка и настройка Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="0a94d-103">Install and configure Azure PowerShell</span></span>

<span data-ttu-id="0a94d-104">В этой статье описывается порядок установки модулей Azure PowerShell в среде Windows.</span><span class="sxs-lookup"><span data-stu-id="0a94d-104">This article explains the steps to install the Azure PowerShell modules in a Windows environment.</span></span>
<span data-ttu-id="0a94d-105">Если вы хотите использовать Azure PowerShell в macOS или Linux, ознакомьтесь со следующей статьей: [Установка и настройка Azure PowerShell в macOS и Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="0a94d-105">If you want to use Azure PowerShell on macOS or Linux, see the following article: [Install and configure Azure PowerShell on macOS and Linux](install-azurermps-maclinux.md).</span></span>

<span data-ttu-id="0a94d-106">Azure PowerShell рекомендуется устанавливать из коллекции PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0a94d-106">Installing Azure PowerShell from the PowerShell Gallery is the preferred method of installation.</span></span>

## <a name="step-1-install-powershellget"></a><span data-ttu-id="0a94d-107">Шаг 1. Проверка установленной версии PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="0a94d-107">Step 1: Install PowerShellGet</span></span>

<span data-ttu-id="0a94d-108">Чтобы установить элементы из коллекции PowerShell, требуется модуль PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="0a94d-108">Installing items from the PowerShell Gallery requires the PowerShellGet module.</span></span> <span data-ttu-id="0a94d-109">Убедитесь, что в системе установлена необходимая версия PowerShellGet и что выполнены другие требования к системе.</span><span class="sxs-lookup"><span data-stu-id="0a94d-109">Make sure you have the appropriate version of PowerShellGet and other system requirements.</span></span> <span data-ttu-id="0a94d-110">Выполните следующую команду, чтобы определить наличие PowerShellGet в вашей системе:</span><span class="sxs-lookup"><span data-stu-id="0a94d-110">Run the following command to see if you have PowerShellGet installed on your system.</span></span>

```powershell-interactive
Get-Module -Name PowerShellGet -ListAvailable | Select-Object -Property Name,Version,Path
```

<span data-ttu-id="0a94d-111">Должен отобразиться результат, аналогичный следующему:</span><span class="sxs-lookup"><span data-stu-id="0a94d-111">You should see something similar to the following output:</span></span>

```Output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="0a94d-112">Необходимо установить версию PowerShellGet 1.1.2.0 или более позднюю.</span><span class="sxs-lookup"><span data-stu-id="0a94d-112">You need PowerShellGet version 1.1.2.0 or higher.</span></span> <span data-ttu-id="0a94d-113">Для обновления PowerShellGet используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0a94d-113">To update PowerShellGet, use the following command:</span></span>

```powershell-interactive
Install-Module PowerShellGet -Force
```

<span data-ttu-id="0a94d-114">Если у вас не установлен PowerShellGet, перейдите к разделу [Как установить PowerShellGet](#how-to-get-powershellget) этой статьи.</span><span class="sxs-lookup"><span data-stu-id="0a94d-114">If you do not have PowerShellGet installed, see the [How to get PowerShellGet](#how-to-get-powershellget) section of this article.</span></span>

> [!NOTE]
> <span data-ttu-id="0a94d-115">Чтобы использовать PowerShellGet, необходимо иметь политику выполнения, которая позволяет запускать сценарии.</span><span class="sxs-lookup"><span data-stu-id="0a94d-115">Using PowerShellGet requires an Execution Policy that allows you to run scripts.</span></span> <span data-ttu-id="0a94d-116">Дополнительные сведения о политике выполнения PowerShell см. в [этой статье](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span><span class="sxs-lookup"><span data-stu-id="0a94d-116">For more information about PowerShell's Execution Policy, see [About Execution Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span></span>
>
> [!IMPORTANT]
> <span data-ttu-id="0a94d-117">Для модуля AzureRM, описанном в этом документе, используется .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="0a94d-117">The module described in this document, AzureRM, uses .NET Framework.</span></span> <span data-ttu-id="0a94d-118">Из-за этого модуль несовместимым с PowerShell версии 6.0, для которой используется .NET Core.</span><span class="sxs-lookup"><span data-stu-id="0a94d-118">This makes it incompatible with PowerShell 6.0, which uses .NET Core.</span></span> <span data-ttu-id="0a94d-119">Если вы используете PowerShell 6.0, изучите [инструкции по установке для macOS и Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="0a94d-119">If you are using PowerShell 6.0, follow the [installation instructions for macOS and Linux](install-azurermps-maclinux.md).</span></span>

## <a name="step-2-install-azure-powershell"></a><span data-ttu-id="0a94d-120">Шаг 2. Установка Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="0a94d-120">Step 2: Install Azure PowerShell</span></span>

<span data-ttu-id="0a94d-121">Для установки Azure PowerShell из коллекции PowerShell требуются повышенные привилегии.</span><span class="sxs-lookup"><span data-stu-id="0a94d-121">Installing Azure PowerShell from the PowerShell Gallery requires elevated privileges.</span></span> <span data-ttu-id="0a94d-122">Выполните следующую команду PowerShell с повышенными правами:</span><span class="sxs-lookup"><span data-stu-id="0a94d-122">Run the following command from an elevated PowerShell session:</span></span>

```powershell-interactive
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

<span data-ttu-id="0a94d-123">По умолчанию коллекция PowerShell не настроена как доверенное хранилище для PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="0a94d-123">By default, the PowerShell gallery is not configured as a Trusted repository for PowerShellGet.</span></span> <span data-ttu-id="0a94d-124">При первом использовании PSGallery отображается следующее сообщение:</span><span class="sxs-lookup"><span data-stu-id="0a94d-124">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): Y
```

<span data-ttu-id="0a94d-125">Ответьте "Да" или "Да для всех", чтобы продолжить установку.</span><span class="sxs-lookup"><span data-stu-id="0a94d-125">Answer 'Yes' or 'Yes to All' to continue with the installation.</span></span>

> [!NOTE]
> <span data-ttu-id="0a94d-126">Если установленная версия NuGet предшествует версии 2.8.5.201, вам будет предложено скачать и установить последнюю версию NuGet.</span><span class="sxs-lookup"><span data-stu-id="0a94d-126">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="0a94d-127">Модуль AzureRM — это набор командлетов для работы с Azure Resource Manager. </span><span class="sxs-lookup"><span data-stu-id="0a94d-127">The AzureRM module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="0a94d-128">При установке модуля AzureRM любой модуль Azure PowerShell, который ранее не был установлен, скачивается из коллекции PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0a94d-128">When you install the AzureRM module, any Azure PowerShell module not previously installed is downloaded and from the PowerShell Gallery.</span></span>

<span data-ttu-id="0a94d-129">Если у вас установлена предыдущая версия Azure PowerShell, то может появляться сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="0a94d-129">If you have a previous version of Azure PowerShell installed you may receive an error.</span></span> <span data-ttu-id="0a94d-130">Для устранения этой проблемы см. раздел [Обновление Azure PowerShell до новой версии](#update-azps) далее в этой статье.</span><span class="sxs-lookup"><span data-stu-id="0a94d-130">To resolve this issue, see the [Updating to a new version of Azure PowerShell](#update-azps) section of this article.</span></span>

## <a name="step-3-load-the-azurerm-module"></a><span data-ttu-id="0a94d-131">Шаг 3. Загрузка модуля AzureRM</span><span class="sxs-lookup"><span data-stu-id="0a94d-131">Step 3: Load the AzureRM module</span></span>

<span data-ttu-id="0a94d-132">После установки модуля его необходимо загрузить в сеанс PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0a94d-132">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="0a94d-133">Это необходимо сделать в обычном (без повышенных привилегий) сеансе PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0a94d-133">You should do this in a normal (non-elevated) PowerShell session.</span></span> <span data-ttu-id="0a94d-134">Модули можно загрузить с помощью командлета `Import-Module` следующим образом:</span><span class="sxs-lookup"><span data-stu-id="0a94d-134">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell-interactive
Import-Module -Name AzureRM
```

## <a name="next-steps"></a><span data-ttu-id="0a94d-135">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="0a94d-135">Next Steps</span></span>

<span data-ttu-id="0a94d-136">Дополнительные сведения об использовании Azure PowerShell см. в следующей статье:</span><span class="sxs-lookup"><span data-stu-id="0a94d-136">For more information about using Azure PowerShell, see the following articles:</span></span>

* <span data-ttu-id="0a94d-137">[Getting started with Azure PowerShell](get-started-azureps.md) (Приступая к работе с Azure PowerShell)</span><span class="sxs-lookup"><span data-stu-id="0a94d-137">[Get started with Azure PowerShell](get-started-azureps.md)</span></span>

## <a name="reporting-issues-and-feedback"></a><span data-ttu-id="0a94d-138">Создание отчетов о проблемах и обратная связь</span><span class="sxs-lookup"><span data-stu-id="0a94d-138">Reporting issues and feedback</span></span>

<span data-ttu-id="0a94d-139">При появлении ошибок в средстве сообщите о проблеме в разделе [Проблемы](https://github.com/Azure/azure-powershell/issues) репозитория GitHub.</span><span class="sxs-lookup"><span data-stu-id="0a94d-139">If you encounter any bugs with the tool, file an issue in the [Issues](https://github.com/Azure/azure-powershell/issues) section of our GitHub repo.</span></span> <span data-ttu-id="0a94d-140">Чтобы отправить отзыв из командной строки, используйте командлет `Send-Feedback`.</span><span class="sxs-lookup"><span data-stu-id="0a94d-140">To provide feedback from the command line, use the `Send-Feedback` cmdlet.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="0a94d-141">Часто задаваемые вопросы</span><span class="sxs-lookup"><span data-stu-id="0a94d-141">Frequently asked questions</span></span>

### <a name="how-to-get-powershellget"></a><span data-ttu-id="0a94d-142">Как установить PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="0a94d-142">How to get PowerShellGet</span></span>

|<span data-ttu-id="0a94d-143">Сценарий</span><span class="sxs-lookup"><span data-stu-id="0a94d-143">OS Version</span></span>|<span data-ttu-id="0a94d-144">Инструкции по установке</span><span class="sxs-lookup"><span data-stu-id="0a94d-144">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="0a94d-145">Используется Windows 10 или Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="0a94d-145">I have Windows 10 or Windows Server 2016</span></span>|<span data-ttu-id="0a94d-146">Встроены в Windows Management Framework (WMF) 5.0, которая входит в состав ОС</span><span class="sxs-lookup"><span data-stu-id="0a94d-146">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="0a94d-147">Обновление до PowerShell 5.0</span><span class="sxs-lookup"><span data-stu-id="0a94d-147">I want to upgrade to PowerShell 5</span></span>|[<span data-ttu-id="0a94d-148">Установите последнюю версию WMF</span><span class="sxs-lookup"><span data-stu-id="0a94d-148">Install the latest version of WMF</span></span>](https://www.microsoft.com/en-us/download/details.aspx?id=54616)|
|<span data-ttu-id="0a94d-149">Используется версия Windows с PowerShell 3 или PowerShell 4</span><span class="sxs-lookup"><span data-stu-id="0a94d-149">I am running on a version of Windows with PowerShell 3 or PowerShell 4</span></span>|[<span data-ttu-id="0a94d-150">Скачайте модули PackageManagement</span><span class="sxs-lookup"><span data-stu-id="0a94d-150">Get the PackageManagement modules</span></span>](http://go.microsoft.com/fwlink/?LinkID=746217)|

### <a name="div-idhelpmechoosechecking-the-version-of-azure-powershell"></a><div id="helpmechoose"/><span data-ttu-id="0a94d-151">Проверка версии Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="0a94d-151">Checking the version of Azure PowerShell</span></span>

<span data-ttu-id="0a94d-152">Хотя мы советуем выполнить обновление до последней версии как можно скорее, поддерживается несколько версий Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0a94d-152">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are supported.</span></span> <span data-ttu-id="0a94d-153">Чтобы определить, какая версия Azure PowerShell установлена, выполните в командной строке команду `Get-Module AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="0a94d-153">To determine the version of Azure PowerShell you have installed, run `Get-Module AzureRM` from your command line.</span></span>

```powershell-interactive
Get-Module AzureRM -ListAvailable | Select-Object -Property Name,Version,Path
```

### <a name="support-for-classic-deployment-methods"></a><span data-ttu-id="0a94d-154">Поддержка классических методов развертывания</span><span class="sxs-lookup"><span data-stu-id="0a94d-154">Support for classic deployment methods</span></span>

<span data-ttu-id="0a94d-155">При наличии экземпляров, развернутых с помощью классической модели, вы можете установить Azure PowerShell для управления службами.</span><span class="sxs-lookup"><span data-stu-id="0a94d-155">If you have deployments that use the classic deployment model you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="0a94d-156">Дополнительные сведения см. в статье об [установке модуля управления службами Azure PowerShell](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="0a94d-156">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span> <span data-ttu-id="0a94d-157">Модули Azure и AzureRM имеют общие зависимости.</span><span class="sxs-lookup"><span data-stu-id="0a94d-157">The Azure and AzureRM modules share common dependencies.</span></span> <span data-ttu-id="0a94d-158">При использовании обоих модулей (Azure и AzureRM) необходимо установить одинаковую версию каждого пакета.</span><span class="sxs-lookup"><span data-stu-id="0a94d-158">If you use both the Azure and AzureRM modules, you should install the same version of each package.</span></span>

### <a name="div-idupdate-azpsupdating-to-a-new-version-of-azure-powershell"></a><div id="update-azps"/><span data-ttu-id="0a94d-159">Обновление Azure PowerShell до новой версии</span><span class="sxs-lookup"><span data-stu-id="0a94d-159">Updating to a new version of Azure PowerShell</span></span>

<span data-ttu-id="0a94d-160">Если у вас установлена предыдущая версия Azure PowerShell, включающая модуль управления службами, то может появиться следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="0a94d-160">If you have a previous version of Azure PowerShell installed that includes the Service Management module, you may receive the following error:</span></span>

```Output
PackageManagement\Install-Package : A command with name 'Get-AzureStorageContainerAcl' is already
available on this system. This module 'Azure.Storage' may override the existing commands. If you
still want to install this module 'Azure.Storage', use -AllowClobber parameter.

At C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PSModule.psm1:1772 char:21
+ ...          $null = PackageManagement\Install-Package @PSBoundParameters
+                      ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : InvalidOperation: (Microsoft.Power....InstallPackage:InstallPackage) [Install-Package], Exception
    + FullyQualifiedErrorId : CommandAlreadyAvailable,Validate-ModuleCommandAlreadyAvailable,Microsoft.PowerShell.PackageManagement.Cmdlets.InstallPackage
```

<span data-ttu-id="0a94d-161">Как указано в сообщении об ошибке, для установки модуля необходимо использовать параметр -AllowClobber.</span><span class="sxs-lookup"><span data-stu-id="0a94d-161">As the error message states, you need to use the -AllowClobber parameter to install the module.</span></span> <span data-ttu-id="0a94d-162">Используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0a94d-162">Use the following command:</span></span>

```powershell-interactive
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

<span data-ttu-id="0a94d-163">Дополнительные сведения см. в статье, посвященной командлету [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).</span><span class="sxs-lookup"><span data-stu-id="0a94d-163">For more information, see the help topic for [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).</span></span>

### <a name="installing-module-versions-side-by-side"></a><span data-ttu-id="0a94d-164">Установка версий модуля без замены</span><span class="sxs-lookup"><span data-stu-id="0a94d-164">Installing module versions side by side</span></span>

<span data-ttu-id="0a94d-165">Метод установки PowerShellGet — это единственный метод, поддерживающий установку нескольких версий.</span><span class="sxs-lookup"><span data-stu-id="0a94d-165">The PowerShellGet method of installation is the only method that supports the installation of multiple versions.</span></span> <span data-ttu-id="0a94d-166">Например, вы можете использовать скрипты, написанные с помощью предыдущих версий Azure PowerShell, которые вы не можете обновить из-за отсутствия времени или ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0a94d-166">For example, you may have scripts written using a previous version of Azure PowerShell that you don't have the time or resources to updated.</span></span> <span data-ttu-id="0a94d-167">Чтобы установить несколько версий Azure PowerShell, выполните следующие команды:</span><span class="sxs-lookup"><span data-stu-id="0a94d-167">The following commands illustrate how to install multiple versions of Azure PowerShell:</span></span>

```powershell-interactive
Install-Module -Name AzureRM -RequiredVersion 3.7.0
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

<span data-ttu-id="0a94d-168">В сеанс PowerShell можно загрузить только одну версию модуля.</span><span class="sxs-lookup"><span data-stu-id="0a94d-168">Only one version of the module can be loaded in a PowerShell session.</span></span> <span data-ttu-id="0a94d-169">Необходимо открыть новое окно PowerShell и с помощью команды `Import-Module` импортировать определенную версию командлетов AzureRM:</span><span class="sxs-lookup"><span data-stu-id="0a94d-169">You must open a new PowerShell window and use `Import-Module` to import a specific version of the AzureRM cmdlets:</span></span>

```powershell-interactive
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

> [!NOTE]
> <span data-ttu-id="0a94d-170">Версии 2.1.0 и 1.2.6 — это первые версии модуля, предназначенные для установки и использования без удаления предыдущей версии.</span><span class="sxs-lookup"><span data-stu-id="0a94d-170">Version 2.1.0 and version 1.2.6 are the first module versions designed to be installed and used side by side.</span></span> <span data-ttu-id="0a94d-171">Если загрузить более раннюю версию модуля Azure PowerShell, то загрузится несовместимая версия модуля **AzureRM.Profile**.</span><span class="sxs-lookup"><span data-stu-id="0a94d-171">When loading an earlier version of the Azure PowerShell, incompatible versions of the **AzureRM.Profile** module are loaded.</span></span> <span data-ttu-id="0a94d-172">Это приведет к тому, что при каждом выполнении командлета будет отображаться запрос на вход.</span><span class="sxs-lookup"><span data-stu-id="0a94d-172">This results in the cmdlets prompting you to sign in whenever you execute a cmdlet.</span></span>

### <a name="other-installation-methods"></a><span data-ttu-id="0a94d-173">Другие методы установки</span><span class="sxs-lookup"><span data-stu-id="0a94d-173">Other installation methods</span></span>

<span data-ttu-id="0a94d-174">Сведения об установке с помощью установщика веб-платформы или пакета MSI см. статье [Other installation methods](other-install.md) (Другие методы установки).</span><span class="sxs-lookup"><span data-stu-id="0a94d-174">For information about installing using the Web Platform Installer or the MSI Package, see [Other installation methods](other-install.md)</span></span>
