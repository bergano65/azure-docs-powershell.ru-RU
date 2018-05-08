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
ms.date: 05/17/2017
ms.openlocfilehash: 0c1500a8748a3aa4546c6ce1e8d16a635b056edb
ms.sourcegitcommit: b256bf48e15ee98865de0fae50e7b81878b03a54
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2017
---
# <a name="install-and-configure-azure-powershell"></a><span data-ttu-id="3c00c-103">Установка и настройка Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="3c00c-103">Install and configure Azure PowerShell</span></span>

<span data-ttu-id="3c00c-104">Предпочтительный способ установки Azure PowerShell— из коллекции PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3c00c-104">Installing Azure PowerShell from the PowerShell Gallery is the preferred method of installation.</span></span>

## <a name="step-1-install-powershellget"></a><span data-ttu-id="3c00c-105">Шаг 1. Установка PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="3c00c-105">Step 1: Install PowerShellGet</span></span>

<span data-ttu-id="3c00c-106">Чтобы установить элементы из коллекции PowerShell, требуется модуль PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="3c00c-106">Installing items from the PowerShell Gallery requires the PowerShellGet module.</span></span> <span data-ttu-id="3c00c-107">Убедитесь, что в системе установлена соответствующая версия PowerShellGet и что выполнены другие требования к системе.</span><span class="sxs-lookup"><span data-stu-id="3c00c-107">Make sure you have the appropriate version of PowerShellGet and other system requirements.</span></span> <span data-ttu-id="3c00c-108">Выполните следующую команду, чтобы определить наличие PowerShellGet в вашей системе:</span><span class="sxs-lookup"><span data-stu-id="3c00c-108">Run the following command to see if you have PowerShellGet installed on your system.</span></span>

```powershell
Get-Module PowerShellGet -list | Select-Object Name,Version,Path
```

<span data-ttu-id="3c00c-109">Должен отобразиться результат, аналогичный следующему:</span><span class="sxs-lookup"><span data-stu-id="3c00c-109">You should see something similar to the following output:</span></span>

```
Name          Version Path
----          ------- ----
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="3c00c-110">Если у вас не установлен PowerShellGet, перейдите к разделу [Как получить PowerShellGet](#how-to-get-powershellget) этой статьи.</span><span class="sxs-lookup"><span data-stu-id="3c00c-110">If you do not have PowerShellGet installed, see the [How to get PowerShellGet](#how-to-get-powershellget) section of this article.</span></span>

> [!NOTE]
> <span data-ttu-id="3c00c-111">Чтобы использовать PowerShellGet, необходимо иметь политику выполнения, которая позволяет запускать сценарии.</span><span class="sxs-lookup"><span data-stu-id="3c00c-111">Using PowerShellGet requires an Execution Policy that allows you to run scripts.</span></span> <span data-ttu-id="3c00c-112">Дополнительные сведения о политике выполнения PowerShell см. в [этой статье](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.core/about/about_execution_policies).</span><span class="sxs-lookup"><span data-stu-id="3c00c-112">For more information about PowerShell's Execution Policy, see [About Execution Policies](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.core/about/about_execution_policies).</span></span>

## <a name="step-2-install-azure-powershell"></a><span data-ttu-id="3c00c-113">Шаг 2. Установка Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="3c00c-113">Step 2: Install Azure PowerShell</span></span>

<span data-ttu-id="3c00c-114">Для установки Azure PowerShell из коллекции PowerShell требуются повышенные привилегии.</span><span class="sxs-lookup"><span data-stu-id="3c00c-114">Installing Azure PowerShell from the PowerShell Gallery requires elevated privileges.</span></span> <span data-ttu-id="3c00c-115">Выполните следующую команду в сеансе PowerShell с повышенными правами:</span><span class="sxs-lookup"><span data-stu-id="3c00c-115">Run the following command from an elevated PowerShell session:</span></span>

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module AzureRM
```

<span data-ttu-id="3c00c-116">По умолчанию коллекция PowerShell не настроена как доверенное хранилище для PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="3c00c-116">By default, the PowerShell gallery is not configured as a Trusted repository for PowerShellGet.</span></span> <span data-ttu-id="3c00c-117">При первом использовании PSGallery отображается следующее сообщение:</span><span class="sxs-lookup"><span data-stu-id="3c00c-117">The first time you use the PSGallery you see the following prompt:</span></span>

```
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): Y
```

<span data-ttu-id="3c00c-118">Ответьте "Да" или "Да для всех", чтобы продолжить установку.</span><span class="sxs-lookup"><span data-stu-id="3c00c-118">Answer 'Yes' or 'Yes to All' to continue with the installation.</span></span>

> [!NOTE]
> <span data-ttu-id="3c00c-119">Если установленная версия NuGet предшествует версии 2.8.5.201, то вам будет предложено скачать и установить последнюю версию NuGet.</span><span class="sxs-lookup"><span data-stu-id="3c00c-119">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="3c00c-120">Модуль AzureRM — это модуль свертки для командлетов Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="3c00c-120">The AzureRM module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="3c00c-121">При установке модуля AzureRM любой модуль Azure PowerShell, который ранее не был установлен, скачивается из коллекции PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3c00c-121">When you install the AzureRM module, any Azure PowerShell module not previously installed is downloaded and from the PowerShell Gallery.</span></span>

<span data-ttu-id="3c00c-122">Если у вас установлена предыдущая версия Azure PowerShell, то может появляться сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="3c00c-122">If you have a previous version of Azure PowerShell installed you may receive an error.</span></span> <span data-ttu-id="3c00c-123">Для устранения этой проблемы см. раздел [Обновление Azure PowerShell до новой версии](#update-azps) далее в этой статье.</span><span class="sxs-lookup"><span data-stu-id="3c00c-123">To resolve this issue, see the [Updating to a new version of Azure PowerShell](#update-azps) section of this article.</span></span>

## <a name="step-3-load-the-azurerm-module"></a><span data-ttu-id="3c00c-124">Шаг 3. Загрузка модуля AzureRM</span><span class="sxs-lookup"><span data-stu-id="3c00c-124">Step 3: Load the AzureRM module</span></span>
<span data-ttu-id="3c00c-125">После установки модуля его необходимо загрузить в сеанс PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3c00c-125">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="3c00c-126">Это необходимо сделать в обычном (без повышенных привилегий) сеансе PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3c00c-126">You should do this in a normal (non-elevated) PowerShell session.</span></span> <span data-ttu-id="3c00c-127">Модули можно загрузить с помощью командлета `Import-Module` следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3c00c-127">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module AzureRM
```

## <a name="next-steps"></a><span data-ttu-id="3c00c-128">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="3c00c-128">Next Steps</span></span>

<span data-ttu-id="3c00c-129">Дополнительные сведения об использовании Azure PowerShell см. в следующей статье:</span><span class="sxs-lookup"><span data-stu-id="3c00c-129">For more information about using Azure PowerShell, see the following articles:</span></span>

* <span data-ttu-id="3c00c-130">[Getting started with Azure PowerShell](get-started-azureps.md) (Приступая к работе с Azure PowerShell)</span><span class="sxs-lookup"><span data-stu-id="3c00c-130">[Get started with Azure PowerShell](get-started-azureps.md)</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="3c00c-131">Часто задаваемые вопросы</span><span class="sxs-lookup"><span data-stu-id="3c00c-131">Frequently asked questions</span></span>

### <a name="how-to-get-powershellget"></a><span data-ttu-id="3c00c-132">Как получить PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="3c00c-132">How to get PowerShellGet</span></span>

|<span data-ttu-id="3c00c-133">Версия ОС</span><span class="sxs-lookup"><span data-stu-id="3c00c-133">OS Version</span></span>|<span data-ttu-id="3c00c-134">Инструкции по установке</span><span class="sxs-lookup"><span data-stu-id="3c00c-134">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="3c00c-135">Используется Windows 10 или Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3c00c-135">I have Windows 10 or Windows Server 2016</span></span>|<span data-ttu-id="3c00c-136">Встроены в Windows Management Framework (WMF) 5.0, которая входит в состав ОС</span><span class="sxs-lookup"><span data-stu-id="3c00c-136">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="3c00c-137">Необходимо выполнить обновление до версии PowerShell 5</span><span class="sxs-lookup"><span data-stu-id="3c00c-137">I want to upgrade to PowerShell 5</span></span>|[<span data-ttu-id="3c00c-138">Установите последнюю версию WMF</span><span class="sxs-lookup"><span data-stu-id="3c00c-138">Install the latest version of WMF</span></span>](https://www.microsoft.com/en-us/download/details.aspx?id=54616)|
|<span data-ttu-id="3c00c-139">Используется версия Windows с PowerShell 3 или PowerShell 4</span><span class="sxs-lookup"><span data-stu-id="3c00c-139">I am running on a version of Windows with PowerShell 3 or PowerShell 4</span></span>|[<span data-ttu-id="3c00c-140">Скачайте модули PackageManagement</span><span class="sxs-lookup"><span data-stu-id="3c00c-140">Get the PackageManagement modules</span></span>](http://go.microsoft.com/fwlink/?LinkID=746217)|

<a id="helpmechoose"></a>
### <a name="checking-the-version-of-azure-powershell"></a><span data-ttu-id="3c00c-141">Проверка версии Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="3c00c-141">Checking the version of Azure PowerShell</span></span>

<span data-ttu-id="3c00c-142">Хотя мы советуем выполнить обновление до последней версии как можно раньше, несколько версий Azure PowerShell все еще поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="3c00c-142">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are support.</span></span> <span data-ttu-id="3c00c-143">Чтобы определить, какая версия Azure PowerShell установлена, выполните в командной строке команду `Get-Module AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="3c00c-143">To determine the version of Azure PowerShell you have installed, run `Get-Module AzureRM` from your command line.</span></span>

```powershell
Get-Module AzureRM -list | Select-Object Name,Version,Path
```

### <a name="support-for-classic-deployment-methods"></a><span data-ttu-id="3c00c-144">Поддержка классических методов развертывания</span><span class="sxs-lookup"><span data-stu-id="3c00c-144">Support for classic deployment methods</span></span>

<span data-ttu-id="3c00c-145">При наличии экземпляров, развернутых с помощью классической модели, вы можете установить Azure PowerShell для управления службами.</span><span class="sxs-lookup"><span data-stu-id="3c00c-145">If you have deployments that use the classic deployment model you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="3c00c-146">Дополнительные сведения см. в статье об [установке модуля управления службами Azure PowerShell](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="3c00c-146">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span> <span data-ttu-id="3c00c-147">Модули Azure и AzureRM имеют общие зависимости.</span><span class="sxs-lookup"><span data-stu-id="3c00c-147">The Azure and AzureRM modules share common dependencies.</span></span> <span data-ttu-id="3c00c-148">При использовании обоих модулей (Azure и AzureRM) необходимо установить одинаковую версию каждого пакета.</span><span class="sxs-lookup"><span data-stu-id="3c00c-148">If you use both the Azure and AzureRM modules, you should install the same version of each package.</span></span>

### <a id="update-azps"></a><span data-ttu-id="3c00c-149">Обновление Azure PowerShell до новой версии</span><span class="sxs-lookup"><span data-stu-id="3c00c-149">Updating to a new version of Azure PowerShell</span></span>

<span data-ttu-id="3c00c-150">Если у вас установлена предыдущая версия Azure PowerShell, включающая модуль управления службами, то может появляться следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="3c00c-150">If you have a previous version of Azure PowerShell installed that includes the Service Management module, you may receive the following error:</span></span>

```
PackageManagement\Install-Package : A command with name 'Get-AzureStorageContainerAcl' is already
available on this system. This module 'Azure.Storage' may override the existing commands. If you
still want to install this module 'Azure.Storage', use -AllowClobber parameter.

At C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PSModule.psm1:1772 char:21
+ ...          $null = PackageManagement\Install-Package @PSBoundParameters
+                      ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : InvalidOperation: (Microsoft.Power....InstallPackage:InstallPackage) [Install-Package], Exception
    + FullyQualifiedErrorId : CommandAlreadyAvailable,Validate-ModuleCommandAlreadyAvailable,Microsoft.PowerShell.PackageManagement.Cmdlets.InstallPackage
```

<span data-ttu-id="3c00c-151">Как указано в сообщении об ошибке, для установки модуля необходимо использовать параметр -AllowClobber.</span><span class="sxs-lookup"><span data-stu-id="3c00c-151">As the error message states, you need to use the -AllowClobber parameter to install the module.</span></span> <span data-ttu-id="3c00c-152">Используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="3c00c-152">Use the following command:</span></span>

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module AzureRM -AllowClobber
```

<span data-ttu-id="3c00c-153">Дополнительные сведения см. в статье, посвященной командлету [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).</span><span class="sxs-lookup"><span data-stu-id="3c00c-153">For more information, see the help topic for [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).</span></span>

### <a name="installing-module-versions-side-by-side"></a><span data-ttu-id="3c00c-154">Установка версий модуля без замены</span><span class="sxs-lookup"><span data-stu-id="3c00c-154">Installing module versions side by side</span></span>

<span data-ttu-id="3c00c-155">Метод установки PowerShellGet — это единственный метод, поддерживающий установку нескольких версий.</span><span class="sxs-lookup"><span data-stu-id="3c00c-155">The PowerShellGet method of installation is the only method that supports the installation of multiple versions.</span></span> <span data-ttu-id="3c00c-156">Например, вы можете использовать скрипты, написанные с помощью предыдущих версий Azure PowerShell, которые вы не можете обновить из-за отсутствия времени или ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3c00c-156">For example, you may have scripts written using a previous version of Azure PowerShell that you don't have the time or resources to updated.</span></span> <span data-ttu-id="3c00c-157">Чтобы установить несколько версий Azure PowerShell, выполните следующие команды:</span><span class="sxs-lookup"><span data-stu-id="3c00c-157">The following commands illustrate how to install multiple versions of Azure PowerShell:</span></span>

```powershell
Install-Module -Name AzureRM -RequiredVersion 3.7.0
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

<span data-ttu-id="3c00c-158">В сеанс PowerShell можно загрузить только одну версию модуля.</span><span class="sxs-lookup"><span data-stu-id="3c00c-158">Only one version of the module can be loaded in a PowerShell session.</span></span> <span data-ttu-id="3c00c-159">Необходимо открыть новое окно PowerShell и с помощью команды `Import-Module` импортировать определенную версию командлетов AzureRM:</span><span class="sxs-lookup"><span data-stu-id="3c00c-159">You must open a new PowerShell window and use `Import-Module` to import a specific version of the AzureRM cmdlets:</span></span>

```powershell
Import-Module AzureRM -RequiredVersion 1.2.9
```

> [!NOTE]
> <span data-ttu-id="3c00c-160">Версии 2.1.0 и 1.2.6 — это первые версии модуля, предназначенные для установки и использования без удаления предыдущей версии.</span><span class="sxs-lookup"><span data-stu-id="3c00c-160">Version 2.1.0 and version 1.2.6 are the first module versions designed to be installed and used side by side.</span></span> <span data-ttu-id="3c00c-161">Если загрузить более раннюю версию модуля Azure PowerShell, то загрузится несовместимая версия модуля **AzureRM.Profile**.</span><span class="sxs-lookup"><span data-stu-id="3c00c-161">When loading an earlier version of the Azure PowerShell, incompatible versions of the **AzureRM.Profile** module are loaded.</span></span> <span data-ttu-id="3c00c-162">Это приведет к тому, что командлеты будут запрашивать выполнить вход при каждом выполнении командлета.</span><span class="sxs-lookup"><span data-stu-id="3c00c-162">This results in the cmdlets prompting you to log in whenever you execute a cmdlet.</span></span>

### <a name="other-installation-methods"></a><span data-ttu-id="3c00c-163">Другие методы установки</span><span class="sxs-lookup"><span data-stu-id="3c00c-163">Other installation methods</span></span>

<span data-ttu-id="3c00c-164">Сведения об установке с помощью установщика веб-платформы или пакета MSI см. статье [Other installation methods](other-install.md) (Другие методы установки).</span><span class="sxs-lookup"><span data-stu-id="3c00c-164">For information about installing using the Web Platform Installer or the MSI Package, see [Other installation methods](other-install.md)</span></span>
