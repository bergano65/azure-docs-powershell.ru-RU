---
title: "Установка и настройка Azure PowerShell | Документация Майкрософт"
description: "Как установить и настроить Azure PowerShell для первого использования."
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/31/2017
ms.openlocfilehash: 0e560332c87fdcc8b7365f2271de24481003a4d6
ms.sourcegitcommit: 72f56597f0329d35779a3ea4ccea6293f0fd2502
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2018
---
# <a name="install-and-configure-azure-powershell"></a><span data-ttu-id="0d764-103">Установка и настройка Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="0d764-103">Install and configure Azure PowerShell</span></span>

<span data-ttu-id="0d764-104">В этой статье описывается порядок установки модулей Azure PowerShell в среде Windows.</span><span class="sxs-lookup"><span data-stu-id="0d764-104">This article explains the steps to install the Azure PowerShell modules in a Windows environment.</span></span>
<span data-ttu-id="0d764-105">Если вы хотите использовать Azure PowerShell в macOS или Linux, ознакомьтесь со следующей статьей: [Установка и настройка Azure PowerShell в macOS и Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="0d764-105">If you want to use Azure PowerShell on macOS or Linux, see the following article: [Install and configure Azure PowerShell on macOS and Linux](install-azurermps-maclinux.md).</span></span>

<span data-ttu-id="0d764-106">Предпочтительный способ установки Azure PowerShell— из коллекции PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0d764-106">Installing Azure PowerShell from the PowerShell Gallery is the preferred method of installation.</span></span>

## <a name="step-1-install-powershellget"></a><span data-ttu-id="0d764-107">Шаг 1. Установка PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="0d764-107">Step 1: Install PowerShellGet</span></span>

<span data-ttu-id="0d764-108">Чтобы установить элементы из коллекции PowerShell, требуется модуль PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="0d764-108">Installing items from the PowerShell Gallery requires the PowerShellGet module.</span></span> <span data-ttu-id="0d764-109">Убедитесь, что в системе установлена соответствующая версия PowerShellGet и что выполнены другие требования к системе.</span><span class="sxs-lookup"><span data-stu-id="0d764-109">Make sure you have the appropriate version of PowerShellGet and other system requirements.</span></span> <span data-ttu-id="0d764-110">Выполните следующую команду, чтобы определить наличие PowerShellGet в вашей системе:</span><span class="sxs-lookup"><span data-stu-id="0d764-110">Run the following command to see if you have PowerShellGet installed on your system.</span></span>

```powershell
Get-Module PowerShellGet -list | Select-Object Name,Version,Path
```

<span data-ttu-id="0d764-111">Должен отобразиться результат, аналогичный следующему:</span><span class="sxs-lookup"><span data-stu-id="0d764-111">You should see something similar to the following output:</span></span>

```Output
Name          Version Path
----          ------- ----
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="0d764-112">Если у вас не установлен PowerShellGet, перейдите к разделу [Как получить PowerShellGet](#how-to-get-powershellget) этой статьи.</span><span class="sxs-lookup"><span data-stu-id="0d764-112">If you do not have PowerShellGet installed, see the [How to get PowerShellGet](#how-to-get-powershellget) section of this article.</span></span>

> [!NOTE]
> <span data-ttu-id="0d764-113">Чтобы использовать PowerShellGet, необходимо иметь политику выполнения, которая позволяет запускать сценарии.</span><span class="sxs-lookup"><span data-stu-id="0d764-113">Using PowerShellGet requires an Execution Policy that allows you to run scripts.</span></span> <span data-ttu-id="0d764-114">Дополнительные сведения о политике выполнения PowerShell см. в [этой статье](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span><span class="sxs-lookup"><span data-stu-id="0d764-114">For more information about PowerShell's Execution Policy, see [About Execution Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span></span>

## <a name="step-2-install-azure-powershell"></a><span data-ttu-id="0d764-115">Шаг 2. Установка Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="0d764-115">Step 2: Install Azure PowerShell</span></span>

<span data-ttu-id="0d764-116">Для установки Azure PowerShell из коллекции PowerShell требуются повышенные привилегии.</span><span class="sxs-lookup"><span data-stu-id="0d764-116">Installing Azure PowerShell from the PowerShell Gallery requires elevated privileges.</span></span> <span data-ttu-id="0d764-117">Выполните следующую команду в сеансе PowerShell с повышенными правами:</span><span class="sxs-lookup"><span data-stu-id="0d764-117">Run the following command from an elevated PowerShell session:</span></span>

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module AzureRM -AllowClobber
```

<span data-ttu-id="0d764-118">По умолчанию коллекция PowerShell не настроена как доверенное хранилище для PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="0d764-118">By default, the PowerShell gallery is not configured as a Trusted repository for PowerShellGet.</span></span> <span data-ttu-id="0d764-119">При первом использовании PSGallery отображается следующее сообщение:</span><span class="sxs-lookup"><span data-stu-id="0d764-119">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): Y
```

<span data-ttu-id="0d764-120">Ответьте "Да" или "Да для всех", чтобы продолжить установку.</span><span class="sxs-lookup"><span data-stu-id="0d764-120">Answer 'Yes' or 'Yes to All' to continue with the installation.</span></span>

> [!NOTE]
> <span data-ttu-id="0d764-121">Если установленная версия NuGet предшествует версии 2.8.5.201, то вам будет предложено скачать и установить последнюю версию NuGet.</span><span class="sxs-lookup"><span data-stu-id="0d764-121">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="0d764-122">Модуль AzureRM — это модуль свертки для командлетов Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="0d764-122">The AzureRM module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="0d764-123">При установке модуля AzureRM любой модуль Azure PowerShell, который ранее не был установлен, скачивается из коллекции PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0d764-123">When you install the AzureRM module, any Azure PowerShell module not previously installed is downloaded and from the PowerShell Gallery.</span></span>

<span data-ttu-id="0d764-124">Если у вас установлена предыдущая версия Azure PowerShell, то может появляться сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="0d764-124">If you have a previous version of Azure PowerShell installed you may receive an error.</span></span> <span data-ttu-id="0d764-125">Для устранения этой проблемы см. раздел [Обновление Azure PowerShell до новой версии](#update-azps) далее в этой статье.</span><span class="sxs-lookup"><span data-stu-id="0d764-125">To resolve this issue, see the [Updating to a new version of Azure PowerShell](#update-azps) section of this article.</span></span>

## <a name="step-3-load-the-azurerm-module"></a><span data-ttu-id="0d764-126">Шаг 3. Загрузка модуля AzureRM</span><span class="sxs-lookup"><span data-stu-id="0d764-126">Step 3: Load the AzureRM module</span></span>
<span data-ttu-id="0d764-127">После установки модуля его необходимо загрузить в сеанс PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0d764-127">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="0d764-128">Это необходимо сделать в обычном (без повышенных привилегий) сеансе PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0d764-128">You should do this in a normal (non-elevated) PowerShell session.</span></span> <span data-ttu-id="0d764-129">Модули можно загрузить с помощью командлета `Import-Module` следующим образом:</span><span class="sxs-lookup"><span data-stu-id="0d764-129">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module AzureRM
```

## <a name="next-steps"></a><span data-ttu-id="0d764-130">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="0d764-130">Next Steps</span></span>

<span data-ttu-id="0d764-131">Дополнительные сведения об использовании Azure PowerShell см. в следующей статье:</span><span class="sxs-lookup"><span data-stu-id="0d764-131">For more information about using Azure PowerShell, see the following articles:</span></span>

* <span data-ttu-id="0d764-132">[Getting started with Azure PowerShell](get-started-azureps.md) (Приступая к работе с Azure PowerShell)</span><span class="sxs-lookup"><span data-stu-id="0d764-132">[Get started with Azure PowerShell](get-started-azureps.md)</span></span>

## <a name="reporting-issues-and-feedback"></a><span data-ttu-id="0d764-133">Создание отчетов о проблемах и обратная связь</span><span class="sxs-lookup"><span data-stu-id="0d764-133">Reporting issues and feedback</span></span>

<span data-ttu-id="0d764-134">При появлении ошибок в средстве сообщите о проблеме в разделе [Проблемы](https://github.com/Azure/azure-powershell/issues) репозитория GitHub.</span><span class="sxs-lookup"><span data-stu-id="0d764-134">If you encounter any bugs with the tool, file an issue in the [Issues](https://github.com/Azure/azure-powershell/issues) section of our GitHub repo.</span></span> <span data-ttu-id="0d764-135">Чтобы отправить отзыв из командной строки, используйте командлет `Send-Feedback`.</span><span class="sxs-lookup"><span data-stu-id="0d764-135">To provide feedback from the command line, use the `Send-Feedback` cmdlet.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="0d764-136">Часто задаваемые вопросы</span><span class="sxs-lookup"><span data-stu-id="0d764-136">Frequently asked questions</span></span>

### <a name="how-to-get-powershellget"></a><span data-ttu-id="0d764-137">Как получить PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="0d764-137">How to get PowerShellGet</span></span>

|<span data-ttu-id="0d764-138">Версия ОС</span><span class="sxs-lookup"><span data-stu-id="0d764-138">OS Version</span></span>|<span data-ttu-id="0d764-139">Инструкции по установке</span><span class="sxs-lookup"><span data-stu-id="0d764-139">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="0d764-140">Используется Windows 10 или Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="0d764-140">I have Windows 10 or Windows Server 2016</span></span>|<span data-ttu-id="0d764-141">Встроены в Windows Management Framework (WMF) 5.0, которая входит в состав ОС</span><span class="sxs-lookup"><span data-stu-id="0d764-141">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="0d764-142">Необходимо выполнить обновление до версии PowerShell 5</span><span class="sxs-lookup"><span data-stu-id="0d764-142">I want to upgrade to PowerShell 5</span></span>|[<span data-ttu-id="0d764-143">Установите последнюю версию WMF</span><span class="sxs-lookup"><span data-stu-id="0d764-143">Install the latest version of WMF</span></span>](https://www.microsoft.com/en-us/download/details.aspx?id=54616)|
|<span data-ttu-id="0d764-144">Используется версия Windows с PowerShell 3 или PowerShell 4</span><span class="sxs-lookup"><span data-stu-id="0d764-144">I am running on a version of Windows with PowerShell 3 or PowerShell 4</span></span>|[<span data-ttu-id="0d764-145">Скачайте модули PackageManagement</span><span class="sxs-lookup"><span data-stu-id="0d764-145">Get the PackageManagement modules</span></span>](http://go.microsoft.com/fwlink/?LinkID=746217)|

<a id="helpmechoose"></a>
### <a name="checking-the-version-of-azure-powershell"></a><span data-ttu-id="0d764-146">Проверка версии Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="0d764-146">Checking the version of Azure PowerShell</span></span>

<span data-ttu-id="0d764-147">Хотя мы советуем выполнить обновление до последней версии как можно скорее, поддерживается несколько версий Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0d764-147">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are supported.</span></span> <span data-ttu-id="0d764-148">Чтобы определить, какая версия Azure PowerShell установлена, выполните в командной строке команду `Get-Module AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="0d764-148">To determine the version of Azure PowerShell you have installed, run `Get-Module AzureRM` from your command line.</span></span>

```powershell
Get-Module AzureRM -list | Select-Object Name,Version,Path
```

### <a name="support-for-classic-deployment-methods"></a><span data-ttu-id="0d764-149">Поддержка классических методов развертывания</span><span class="sxs-lookup"><span data-stu-id="0d764-149">Support for classic deployment methods</span></span>

<span data-ttu-id="0d764-150">При наличии экземпляров, развернутых с помощью классической модели, вы можете установить Azure PowerShell для управления службами.</span><span class="sxs-lookup"><span data-stu-id="0d764-150">If you have deployments that use the classic deployment model you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="0d764-151">Дополнительные сведения см. в статье об [установке модуля управления службами Azure PowerShell](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="0d764-151">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span> <span data-ttu-id="0d764-152">Модули Azure и AzureRM имеют общие зависимости.</span><span class="sxs-lookup"><span data-stu-id="0d764-152">The Azure and AzureRM modules share common dependencies.</span></span> <span data-ttu-id="0d764-153">При использовании обоих модулей (Azure и AzureRM) необходимо установить одинаковую версию каждого пакета.</span><span class="sxs-lookup"><span data-stu-id="0d764-153">If you use both the Azure and AzureRM modules, you should install the same version of each package.</span></span>

### <a id="update-azps"></a><span data-ttu-id="0d764-154">Обновление Azure PowerShell до новой версии</span><span class="sxs-lookup"><span data-stu-id="0d764-154">Updating to a new version of Azure PowerShell</span></span>

<span data-ttu-id="0d764-155">Если у вас установлена предыдущая версия Azure PowerShell, включающая модуль управления службами, то может появляться следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="0d764-155">If you have a previous version of Azure PowerShell installed that includes the Service Management module, you may receive the following error:</span></span>

```Output
PackageManagement\Install-Package : A command with name 'Get-AzureStorageContainerAcl' is already
available on this system. This module 'Azure.Storage' may override the existing commands. If you
still want to install this module 'Azure.Storage', use -AllowClobber parameter.

At C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PSModule.psm1:1772 char:21
+ ...          $null = PackageManagement\Install-Package @PSBoundParameters
+                      ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : InvalidOperation: (Microsoft.Power....InstallPackage:InstallPackage) [Install-Package], Exception
    + FullyQualifiedErrorId : CommandAlreadyAvailable,Validate-ModuleCommandAlreadyAvailable,Microsoft.PowerShell.PackageManagement.Cmdlets.InstallPackage
```

<span data-ttu-id="0d764-156">Как указано в сообщении об ошибке, для установки модуля необходимо использовать параметр -AllowClobber.</span><span class="sxs-lookup"><span data-stu-id="0d764-156">As the error message states, you need to use the -AllowClobber parameter to install the module.</span></span> <span data-ttu-id="0d764-157">Используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0d764-157">Use the following command:</span></span>

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module AzureRM -AllowClobber
```

<span data-ttu-id="0d764-158">Дополнительные сведения см. в статье, посвященной командлету [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).</span><span class="sxs-lookup"><span data-stu-id="0d764-158">For more information, see the help topic for [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).</span></span>

### <a name="installing-module-versions-side-by-side"></a><span data-ttu-id="0d764-159">Установка версий модуля без замены</span><span class="sxs-lookup"><span data-stu-id="0d764-159">Installing module versions side by side</span></span>

<span data-ttu-id="0d764-160">Метод установки PowerShellGet — это единственный метод, поддерживающий установку нескольких версий.</span><span class="sxs-lookup"><span data-stu-id="0d764-160">The PowerShellGet method of installation is the only method that supports the installation of multiple versions.</span></span> <span data-ttu-id="0d764-161">Например, вы можете использовать скрипты, написанные с помощью предыдущих версий Azure PowerShell, которые вы не можете обновить из-за отсутствия времени или ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0d764-161">For example, you may have scripts written using a previous version of Azure PowerShell that you don't have the time or resources to updated.</span></span> <span data-ttu-id="0d764-162">Чтобы установить несколько версий Azure PowerShell, выполните следующие команды:</span><span class="sxs-lookup"><span data-stu-id="0d764-162">The following commands illustrate how to install multiple versions of Azure PowerShell:</span></span>

```powershell
Install-Module -Name AzureRM -RequiredVersion 3.7.0
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

<span data-ttu-id="0d764-163">В сеанс PowerShell можно загрузить только одну версию модуля.</span><span class="sxs-lookup"><span data-stu-id="0d764-163">Only one version of the module can be loaded in a PowerShell session.</span></span> <span data-ttu-id="0d764-164">Необходимо открыть новое окно PowerShell и с помощью команды `Import-Module` импортировать определенную версию командлетов AzureRM:</span><span class="sxs-lookup"><span data-stu-id="0d764-164">You must open a new PowerShell window and use `Import-Module` to import a specific version of the AzureRM cmdlets:</span></span>

```powershell
Import-Module AzureRM -RequiredVersion 1.2.9
```

> [!NOTE]
> <span data-ttu-id="0d764-165">Версии 2.1.0 и 1.2.6 — это первые версии модуля, предназначенные для установки и использования без удаления предыдущей версии.</span><span class="sxs-lookup"><span data-stu-id="0d764-165">Version 2.1.0 and version 1.2.6 are the first module versions designed to be installed and used side by side.</span></span> <span data-ttu-id="0d764-166">Если загрузить более раннюю версию модуля Azure PowerShell, то загрузится несовместимая версия модуля **AzureRM.Profile**.</span><span class="sxs-lookup"><span data-stu-id="0d764-166">When loading an earlier version of the Azure PowerShell, incompatible versions of the **AzureRM.Profile** module are loaded.</span></span> <span data-ttu-id="0d764-167">Это приведет к тому, что командлеты будут запрашивать выполнить вход при каждом выполнении командлета.</span><span class="sxs-lookup"><span data-stu-id="0d764-167">This results in the cmdlets prompting you to log in whenever you execute a cmdlet.</span></span>

### <a name="other-installation-methods"></a><span data-ttu-id="0d764-168">Другие методы установки</span><span class="sxs-lookup"><span data-stu-id="0d764-168">Other installation methods</span></span>

<span data-ttu-id="0d764-169">Сведения об установке с помощью установщика веб-платформы или пакета MSI см. статье [Other installation methods](other-install.md) (Другие методы установки).</span><span class="sxs-lookup"><span data-stu-id="0d764-169">For information about installing using the Web Platform Installer or the MSI Package, see [Other installation methods](other-install.md)</span></span>