---
title: Установка и настройка Azure PowerShell | Документация Майкрософт
description: Как установить и настроить Azure PowerShell для первого использования.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/27/2018
ms.openlocfilehash: 0df1208db69fedcb61ca7e3e8fcf5d05dfef5379
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/23/2018
---
# <a name="install-and-configure-azure-powershell"></a><span data-ttu-id="41231-103">Установка и настройка Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="41231-103">Install and configure Azure PowerShell</span></span>

<span data-ttu-id="41231-104">В этой статье описывается порядок установки модулей Azure PowerShell в среде Windows.</span><span class="sxs-lookup"><span data-stu-id="41231-104">This article explains the steps to install the Azure PowerShell modules in a Windows environment.</span></span>
<span data-ttu-id="41231-105">Если вы хотите использовать Azure PowerShell в macOS или Linux, ознакомьтесь со следующей статьей: [Установка и настройка Azure PowerShell в macOS и Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="41231-105">If you want to use Azure PowerShell on macOS or Linux, see the following article: [Install and configure Azure PowerShell on macOS and Linux](install-azurermps-maclinux.md).</span></span>

## <a name="system-requirements"></a><span data-ttu-id="41231-106">Требования к системе</span><span class="sxs-lookup"><span data-stu-id="41231-106">System requirements</span></span>

<span data-ttu-id="41231-107">Для работы с Azure PowerShell версии 6.0.0 требуется версия PowerShell 5.0 и выше.</span><span class="sxs-lookup"><span data-stu-id="41231-107">Azure PowerShell version 6.0.0 requires version 5.0 (or higher) of PowerShell.</span></span> <span data-ttu-id="41231-108">Для работы с предыдущими версиями Azure PowerShell требуется _по крайней мере_ версия PowerShell 3.0 (для выполнения любого командлета). Сведения об обновлении до версии PowerShell 5.0 см. в [этой таблице](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="41231-108">Previous versions of Azure PowerShell required _at least_ version 3.0 of PowerShell to run any cmdlet.For information on upgrading to PowerShell 5.0, please see [this table](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span></span>

## <a name="step-1-install-powershellget"></a><span data-ttu-id="41231-109">Шаг 1. Проверка установленной версии PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="41231-109">Step 1: Install PowerShellGet</span></span>

<span data-ttu-id="41231-110">Azure PowerShell рекомендуется устанавливать из коллекции PowerShell.</span><span class="sxs-lookup"><span data-stu-id="41231-110">Installing Azure PowerShell from the PowerShell Gallery is the preferred method of installation.</span></span>

<span data-ttu-id="41231-111">Чтобы установить элементы из коллекции PowerShell, требуется модуль PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="41231-111">Installing items from the PowerShell Gallery requires the PowerShellGet module.</span></span> <span data-ttu-id="41231-112">Убедитесь, что в системе установлена необходимая версия PowerShellGet и что выполнены другие требования к системе.</span><span class="sxs-lookup"><span data-stu-id="41231-112">Make sure you have the appropriate version of PowerShellGet and other system requirements.</span></span> <span data-ttu-id="41231-113">Выполните следующую команду, чтобы определить наличие PowerShellGet в вашей системе:</span><span class="sxs-lookup"><span data-stu-id="41231-113">Run the following command to see if you have PowerShellGet installed on your system.</span></span>

```powershell
Get-Module -Name PowerShellGet -ListAvailable | Select-Object -Property Name,Version,Path
```

<span data-ttu-id="41231-114">Должен отобразиться результат, аналогичный следующему:</span><span class="sxs-lookup"><span data-stu-id="41231-114">You should see something similar to the following output:</span></span>

```Output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="41231-115">Необходимо установить версию PowerShellGet 1.1.2.0 или более позднюю.</span><span class="sxs-lookup"><span data-stu-id="41231-115">You need PowerShellGet version 1.1.2.0 or higher.</span></span> <span data-ttu-id="41231-116">Для обновления PowerShellGet используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="41231-116">To update PowerShellGet, use the following command:</span></span>

```powershell
Install-Module PowerShellGet -Force
```

<span data-ttu-id="41231-117">Если у вас не установлен PowerShellGet, перейдите к разделу [Как установить PowerShellGet](#how-to-get-powershellget) этой статьи.</span><span class="sxs-lookup"><span data-stu-id="41231-117">If you do not have PowerShellGet installed, see the [How to get PowerShellGet](#how-to-get-powershellget) section of this article.</span></span>

> [!NOTE]
> <span data-ttu-id="41231-118">Чтобы использовать PowerShellGet, необходимо иметь политику выполнения, которая позволяет запускать сценарии.</span><span class="sxs-lookup"><span data-stu-id="41231-118">Using PowerShellGet requires an Execution Policy that allows you to run scripts.</span></span> <span data-ttu-id="41231-119">Дополнительные сведения о политике выполнения PowerShell см. в [этой статье](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span><span class="sxs-lookup"><span data-stu-id="41231-119">For more information about PowerShell's Execution Policy, see [About Execution Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span></span>

## <a name="step-2-install-azure-powershell"></a><span data-ttu-id="41231-120">Шаг 2. Установка Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="41231-120">Step 2: Install Azure PowerShell</span></span>

<span data-ttu-id="41231-121">Для установки Azure PowerShell из коллекции PowerShell требуются повышенные привилегии.</span><span class="sxs-lookup"><span data-stu-id="41231-121">Installing Azure PowerShell from the PowerShell Gallery requires elevated privileges.</span></span> <span data-ttu-id="41231-122">Выполните следующую команду PowerShell с повышенными правами:</span><span class="sxs-lookup"><span data-stu-id="41231-122">Run the following command from an elevated PowerShell session:</span></span>

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

<span data-ttu-id="41231-123">По умолчанию коллекция PowerShell не настроена как доверенное хранилище для PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="41231-123">By default, the PowerShell gallery is not configured as a Trusted repository for PowerShellGet.</span></span> <span data-ttu-id="41231-124">При первом использовании PSGallery отображается следующее сообщение:</span><span class="sxs-lookup"><span data-stu-id="41231-124">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): Y
```

<span data-ttu-id="41231-125">Ответьте "Да" или "Да для всех", чтобы продолжить установку.</span><span class="sxs-lookup"><span data-stu-id="41231-125">Answer 'Yes' or 'Yes to All' to continue with the installation.</span></span>

> [!NOTE]
> <span data-ttu-id="41231-126">Если установленная версия NuGet предшествует версии 2.8.5.201, вам будет предложено скачать и установить последнюю версию NuGet.</span><span class="sxs-lookup"><span data-stu-id="41231-126">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="41231-127">Модуль AzureRM — это набор командлетов для работы с Azure Resource Manager. </span><span class="sxs-lookup"><span data-stu-id="41231-127">The AzureRM module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="41231-128">При установке модуля AzureRM любой модуль Azure PowerShell, который ранее не был установлен, скачивается из коллекции PowerShell.</span><span class="sxs-lookup"><span data-stu-id="41231-128">When you install the AzureRM module, any Azure PowerShell module not previously installed is downloaded and from the PowerShell Gallery.</span></span>

<span data-ttu-id="41231-129">Если у вас установлена предыдущая версия Azure PowerShell, то может появляться сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="41231-129">If you have a previous version of Azure PowerShell installed you may receive an error.</span></span> <span data-ttu-id="41231-130">Для устранения этой проблемы см. раздел [Обновление Azure PowerShell до новой версии](#update-azps) далее в этой статье.</span><span class="sxs-lookup"><span data-stu-id="41231-130">To resolve this issue, see the [Updating to a new version of Azure PowerShell](#update-azps) section of this article.</span></span>

## <a name="step-3-load-the-azurerm-module"></a><span data-ttu-id="41231-131">Шаг 3. Загрузка модуля AzureRM</span><span class="sxs-lookup"><span data-stu-id="41231-131">Step 3: Load the AzureRM module</span></span>
<span data-ttu-id="41231-132">После установки модуля его необходимо загрузить в сеанс PowerShell.</span><span class="sxs-lookup"><span data-stu-id="41231-132">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="41231-133">Это необходимо сделать в обычном (без повышенных привилегий) сеансе PowerShell.</span><span class="sxs-lookup"><span data-stu-id="41231-133">You should do this in a normal (non-elevated) PowerShell session.</span></span> <span data-ttu-id="41231-134">Модули можно загрузить с помощью командлета `Import-Module` следующим образом:</span><span class="sxs-lookup"><span data-stu-id="41231-134">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module -Name AzureRM
```

## <a name="next-steps"></a><span data-ttu-id="41231-135">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="41231-135">Next Steps</span></span>

<span data-ttu-id="41231-136">Дополнительные сведения об использовании Azure PowerShell см. в следующей статье:</span><span class="sxs-lookup"><span data-stu-id="41231-136">For more information about using Azure PowerShell, see the following articles:</span></span>

* <span data-ttu-id="41231-137">[Getting started with Azure PowerShell](get-started-azureps.md) (Приступая к работе с Azure PowerShell)</span><span class="sxs-lookup"><span data-stu-id="41231-137">[Get started with Azure PowerShell](get-started-azureps.md)</span></span>

## <a name="reporting-issues-and-feedback"></a><span data-ttu-id="41231-138">Создание отчетов о проблемах и обратная связь</span><span class="sxs-lookup"><span data-stu-id="41231-138">Reporting issues and feedback</span></span>

<span data-ttu-id="41231-139">При появлении ошибок в средстве сообщите о проблеме в разделе [Проблемы](https://github.com/Azure/azure-powershell/issues) репозитория GitHub.</span><span class="sxs-lookup"><span data-stu-id="41231-139">If you encounter any bugs with the tool, file an issue in the [Issues](https://github.com/Azure/azure-powershell/issues) section of our GitHub repo.</span></span> <span data-ttu-id="41231-140">Чтобы отправить отзыв из командной строки, используйте командлет `Send-Feedback`.</span><span class="sxs-lookup"><span data-stu-id="41231-140">To provide feedback from the command line, use the `Send-Feedback` cmdlet.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="41231-141">Часто задаваемые вопросы</span><span class="sxs-lookup"><span data-stu-id="41231-141">Frequently asked questions</span></span>

### <a name="how-to-get-powershellget"></a><span data-ttu-id="41231-142">Как установить PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="41231-142">How to get PowerShellGet</span></span>

|<span data-ttu-id="41231-143">Сценарий</span><span class="sxs-lookup"><span data-stu-id="41231-143">Scenario</span></span>|<span data-ttu-id="41231-144">Инструкции по установке</span><span class="sxs-lookup"><span data-stu-id="41231-144">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="41231-145">Windows 10</span><span class="sxs-lookup"><span data-stu-id="41231-145">Windows 10</span></span><br/><span data-ttu-id="41231-146">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="41231-146">Windows Server 2016</span></span>|<span data-ttu-id="41231-147">Встроен в пакет Windows Management Framework (WMF) 5.0, который входит в состав ОС</span><span class="sxs-lookup"><span data-stu-id="41231-147">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="41231-148">Обновление до PowerShell 5.0</span><span class="sxs-lookup"><span data-stu-id="41231-148">I want to upgrade to PowerShell 5</span></span>|<ol><li>[<span data-ttu-id="41231-149">Установите последнюю версию WMF</span><span class="sxs-lookup"><span data-stu-id="41231-149">Install the latest version of WMF</span></span>](https://www.microsoft.com/en-us/download/details.aspx?id=54616)</li><li><span data-ttu-id="41231-150">Выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="41231-150">Run the following command:</span></span><br/>```Install-Module PowerShellGet -Force```</li></ol>|
|<span data-ttu-id="41231-151">Используется версия Windows с PowerShell 3 или PowerShell 4</span><span class="sxs-lookup"><span data-stu-id="41231-151">I am running on a version of Windows with PowerShell 3 or PowerShell 4</span></span>|<ol><span data-ttu-id="41231-152"><il>[Получите модули PackageManagement:](http://go.microsoft.com/fwlink/?LinkID=746217)</il></span><span class="sxs-lookup"><span data-stu-id="41231-152"><il>[Get the PackageManagement modules](http://go.microsoft.com/fwlink/?LinkID=746217)</il></span></span><li><span data-ttu-id="41231-153">Выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="41231-153">Run the following command:</span></span><br/>```Install-Module PowerShellGet -Force```</li></ol>|

<a id="helpmechoose"></a>
### <a name="checking-the-version-of-azure-powershell"></a><span data-ttu-id="41231-154">Проверка версии Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="41231-154">Checking the version of Azure PowerShell</span></span>

<span data-ttu-id="41231-155">Хотя мы советуем выполнить обновление до последней версии как можно скорее, поддерживается несколько версий Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="41231-155">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are supported.</span></span> <span data-ttu-id="41231-156">Чтобы определить, какая версия Azure PowerShell установлена, выполните в командной строке команду `Get-Module AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="41231-156">To determine the version of Azure PowerShell you have installed, run `Get-Module AzureRM` from your command line.</span></span>

```powershell
Get-Module AzureRM -ListAvailable | Select-Object -Property Name,Version,Path
```

### <a name="support-for-classic-deployment-methods"></a><span data-ttu-id="41231-157">Поддержка классических методов развертывания</span><span class="sxs-lookup"><span data-stu-id="41231-157">Support for classic deployment methods</span></span>

<span data-ttu-id="41231-158">При наличии экземпляров, развернутых с помощью классической модели, вы можете установить Azure PowerShell для управления службами.</span><span class="sxs-lookup"><span data-stu-id="41231-158">If you have deployments that use the classic deployment model you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="41231-159">Дополнительные сведения см. в статье об [установке модуля управления службами Azure PowerShell](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="41231-159">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span> <span data-ttu-id="41231-160">Модули Azure и AzureRM имеют общие зависимости.</span><span class="sxs-lookup"><span data-stu-id="41231-160">The Azure and AzureRM modules share common dependencies.</span></span> <span data-ttu-id="41231-161">При использовании обоих модулей (Azure и AzureRM) необходимо установить одинаковую версию каждого пакета.</span><span class="sxs-lookup"><span data-stu-id="41231-161">If you use both the Azure and AzureRM modules, you should install the same version of each package.</span></span>

### <a id="update-azps"></a><span data-ttu-id="41231-162">Обновление Azure PowerShell до новой версии</span><span class="sxs-lookup"><span data-stu-id="41231-162">Updating to a new version of Azure PowerShell</span></span>

<span data-ttu-id="41231-163">Если у вас установлена предыдущая версия Azure PowerShell, включающая модуль управления службами, то может появляться следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="41231-163">If you have a previous version of Azure PowerShell installed that includes the Service Management module, you may receive the following error:</span></span>

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

<span data-ttu-id="41231-164">Как указано в сообщении об ошибке, для установки модуля необходимо использовать параметр -AllowClobber.</span><span class="sxs-lookup"><span data-stu-id="41231-164">As the error message states, you need to use the -AllowClobber parameter to install the module.</span></span> <span data-ttu-id="41231-165">Используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="41231-165">Use the following command:</span></span>

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

<span data-ttu-id="41231-166">Дополнительные сведения см. в статье, посвященной командлету [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).</span><span class="sxs-lookup"><span data-stu-id="41231-166">For more information, see the help topic for [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).</span></span>

### <a name="installing-module-versions-side-by-side"></a><span data-ttu-id="41231-167">Установка версий модуля без замены</span><span class="sxs-lookup"><span data-stu-id="41231-167">Installing module versions side by side</span></span>

<span data-ttu-id="41231-168">Метод установки PowerShellGet — это единственный метод, поддерживающий установку нескольких версий.</span><span class="sxs-lookup"><span data-stu-id="41231-168">The PowerShellGet method of installation is the only method that supports the installation of multiple versions.</span></span> <span data-ttu-id="41231-169">Например, вы можете использовать скрипты, написанные с помощью предыдущих версий Azure PowerShell, которые вы не можете обновить из-за отсутствия времени или ресурсов.</span><span class="sxs-lookup"><span data-stu-id="41231-169">For example, you may have scripts written using a previous version of Azure PowerShell that you don't have the time or resources to updated.</span></span> <span data-ttu-id="41231-170">Чтобы установить несколько версий Azure PowerShell, выполните следующие команды:</span><span class="sxs-lookup"><span data-stu-id="41231-170">The following commands illustrate how to install multiple versions of Azure PowerShell:</span></span>

```powershell
Install-Module -Name AzureRM -RequiredVersion 3.7.0
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

<span data-ttu-id="41231-171">В сеанс PowerShell можно загрузить только одну версию модуля.</span><span class="sxs-lookup"><span data-stu-id="41231-171">Only one version of the module can be loaded in a PowerShell session.</span></span> <span data-ttu-id="41231-172">Необходимо открыть новое окно PowerShell и с помощью команды `Import-Module` импортировать определенную версию командлетов AzureRM:</span><span class="sxs-lookup"><span data-stu-id="41231-172">You must open a new PowerShell window and use `Import-Module` to import a specific version of the AzureRM cmdlets:</span></span>

```powershell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

> [!NOTE]
> <span data-ttu-id="41231-173">Версии 2.1.0 и 1.2.6 — это первые версии модуля, предназначенные для установки и использования без удаления предыдущей версии.</span><span class="sxs-lookup"><span data-stu-id="41231-173">Version 2.1.0 and version 1.2.6 are the first module versions designed to be installed and used side by side.</span></span> <span data-ttu-id="41231-174">Если загрузить более раннюю версию модуля Azure PowerShell, то загрузится несовместимая версия модуля **AzureRM.Profile**.</span><span class="sxs-lookup"><span data-stu-id="41231-174">When loading an earlier version of the Azure PowerShell, incompatible versions of the **AzureRM.Profile** module are loaded.</span></span> <span data-ttu-id="41231-175">Это приведет к тому, что командлеты будут запрашивать выполнить вход при каждом выполнении командлета.</span><span class="sxs-lookup"><span data-stu-id="41231-175">This results in the cmdlets prompting you to log in whenever you execute a cmdlet.</span></span>

### <a name="other-installation-methods"></a><span data-ttu-id="41231-176">Другие методы установки</span><span class="sxs-lookup"><span data-stu-id="41231-176">Other installation methods</span></span>

<span data-ttu-id="41231-177">Сведения об установке с помощью установщика веб-платформы или пакета MSI см. статье [Other installation methods](other-install.md) (Другие методы установки).</span><span class="sxs-lookup"><span data-stu-id="41231-177">For information about installing using the Web Platform Installer or the MSI Package, see [Other installation methods](other-install.md)</span></span>
