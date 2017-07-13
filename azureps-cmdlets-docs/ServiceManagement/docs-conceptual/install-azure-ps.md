---
title: "<span data-ttu-id=\"1834a-101\">Установка и настройка модуля управления службами Azure PowerShell | Документация Майкрософт</span><span class=\"sxs-lookup\"><span data-stu-id=\"1834a-101\">Install and configure the Azure PowerShell Service Management module | Microsoft Docs</span></span>"
description: "<span data-ttu-id=\"1834a-102\">Как установить и настроить Azure PowerShell для первого использования.</span><span class=\"sxs-lookup\"><span data-stu-id=\"1834a-102\">How to install and configure Azure PowerShell for first time use.</span></span>"
services: azure
author: sdwheeler
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/06/2017
ms.openlocfilehash: c51c727c1cb022eca59f819c7f24d8e058c677da
ms.sourcegitcommit: 226527be7cb647acfe2ea9ab151185053ab3c6db
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/29/2017
---
# <span data-ttu-id="1834a-103">Установка модуля управления службами Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="1834a-103">Installing the Azure PowerShell Service Management module</span></span>
<a id="installing-the-azure-powershell-service-management-module" class="xliff"></a>

<span data-ttu-id="1834a-104">Предпочтительный способ установки Azure PowerShell — из [коллекции PowerShell](https://www.powershellgallery.com/).</span><span class="sxs-lookup"><span data-stu-id="1834a-104">Installing Azure PowerShell from the [PowerShell Gallery](https://www.powershellgallery.com/) is the preferred method of installation.</span></span>

## <span data-ttu-id="1834a-105">Шаг 1. Установка PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="1834a-105">Step 1: Install PowerShellGet</span></span>
<a id="step-1-install-powershellget" class="xliff"></a>

<span data-ttu-id="1834a-106">Чтобы установить элементы из коллекции PowerShell, требуется модуль PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="1834a-106">Installing items from the PowerShell Gallery requires the PowerShellGet module.</span></span> <span data-ttu-id="1834a-107">Убедитесь, что в системе установлена соответствующая версия PowerShellGet и что выполнены другие требования к системе.</span><span class="sxs-lookup"><span data-stu-id="1834a-107">Make sure you have the appropriate version of PowerShellGet and other system requirements.</span></span> <span data-ttu-id="1834a-108">Выполните следующую команду, чтобы определить наличие PowerShellGet в вашей системе:</span><span class="sxs-lookup"><span data-stu-id="1834a-108">Run the following command to see if you have PowerShellGet installed on your system.</span></span>

```powershell
Get-Module PowerShellGet -list | Select-Object Name,Version,Path
```

<span data-ttu-id="1834a-109">Должен отобразиться похожий результат:</span><span class="sxs-lookup"><span data-stu-id="1834a-109">You should see something similar to the following output:</span></span>

```
Name          Version Path
----          ------- ----
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="1834a-110">Если у вас не установлен PowerShellGet, перейдите к разделу [Как получить PowerShellGet](install-azurerm-ps.md#how-to-get-powershellget).</span><span class="sxs-lookup"><span data-stu-id="1834a-110">If you do not have PowerShellGet installed, see the [How to get PowerShellGet](install-azurerm-ps.md#how-to-get-powershellget).</span></span>

## <span data-ttu-id="1834a-111">Шаг 2. Установка Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="1834a-111">Step 2: Install Azure PowerShell</span></span>
<a id="step-2-install-azure-powershell" class="xliff"></a>

<span data-ttu-id="1834a-112">Войдите в консоль Windows PowerShell с правами администратора и выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="1834a-112">Run the following command from the Windows PowerShell console running as Administrator:</span></span>

```powershell
Install-Module Azure
```

<span data-ttu-id="1834a-113">Модуль Azure — это модуль свертки для командлетов Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="1834a-113">The Azure module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="1834a-114">При установке модуля AzureRM из коллекции PowerShell будут скачаны и установлены все модули Azure, которые ранее не были установлены.</span><span class="sxs-lookup"><span data-stu-id="1834a-114">When you install the AzureRM module, any other Azure modules that have not previously been installed will be downloaded and installed from the PowerShell Gallery.</span></span>

<span data-ttu-id="1834a-115">Модуль управления службой Azure использует те же зависимости, что и модули Azure PowerShell Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="1834a-115">The Azure Service Management module shares dependencies with the Azure PowerShell Resource Manager modules.</span></span> <span data-ttu-id="1834a-116">Если вы установили модули Azure PowerShell Resource Manager, необходимо добавить параметр `-AllowClobber` в команду установки.</span><span class="sxs-lookup"><span data-stu-id="1834a-116">If you have installed the Azure PowerShell Resource Manager modules, you will need to add the `-AllowClobber` parameter to the install command.</span></span> <span data-ttu-id="1834a-117">Таким образом все существующие общие зависимости будут обновлены.</span><span class="sxs-lookup"><span data-stu-id="1834a-117">This allows this existing shared dependencies to be updated.</span></span> <span data-ttu-id="1834a-118">Если этот параметр отсутствует, происходит сбой установки модуля.</span><span class="sxs-lookup"><span data-stu-id="1834a-118">Without this parameter, installation of the module fails.</span></span>

```powershell
Install-Module Azure -AllowClobber
```

<span data-ttu-id="1834a-119">После установки этого модуля вы можете импортировать модуль, выполнив следующую команду:</span><span class="sxs-lookup"><span data-stu-id="1834a-119">After you install this module, you can import the module by running the following command:</span></span>

```powershell
Import-Module Azure
```

## <span data-ttu-id="1834a-120">Использование командлетов</span><span class="sxs-lookup"><span data-stu-id="1834a-120">To use the cmdlets</span></span>
<a id="to-use-the-cmdlets" class="xliff"></a>

<span data-ttu-id="1834a-121">Чтобы начать работу с командлетами управления службами Azure, сначала войдите в свою учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="1834a-121">To start working with the Azure Service Management cmdlets, first log on to your Azure account.</span></span> <span data-ttu-id="1834a-122">Чтобы войти в учетную запись, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="1834a-122">To log on to your account, run the following command:</span></span>

```powershell
Add-AzureAccount
```

<span data-ttu-id="1834a-123">Когда вы войдете в Azure, Azure PowerShell создаст контекст для этого сеанса.</span><span class="sxs-lookup"><span data-stu-id="1834a-123">After logging into Azure, Azure PowerShell creates a context for the given session.</span></span> <span data-ttu-id="1834a-124">Этот контекст содержит среду Azure PowerShell, учетную запись, клиент и подписку, которые будут использоваться для всех командлетов в этом сеансе.</span><span class="sxs-lookup"><span data-stu-id="1834a-124">That context contains the Azure PowerShell environment, account, tenant, and subscription that will be used for all cmdlets within that session.</span></span> <span data-ttu-id="1834a-125">Теперь вы готовы использовать следующие модули.</span><span class="sxs-lookup"><span data-stu-id="1834a-125">Now you are ready to use the modules below.</span></span>

## <span data-ttu-id="1834a-126">Командлеты для управления службами Azure</span><span class="sxs-lookup"><span data-stu-id="1834a-126">Azure Service Management cmdlets</span></span>
<a id="azure-service-management-cmdlets" class="xliff"></a>

<span data-ttu-id="1834a-127">Модули Azure PowerShell часто обновляются.</span><span class="sxs-lookup"><span data-stu-id="1834a-127">Azure PowerShell modules are updated frequently.</span></span> <span data-ttu-id="1834a-128">Если вы заметили, что онлайн-справка по командлетам содержит командлеты и параметры, которых нет в вашем модуле, скачайте и установите последнюю версию модуля.</span><span class="sxs-lookup"><span data-stu-id="1834a-128">If you notice that the online cmdlet help includes cmdlets or parameters that are not in your module, download and install the latest version of the module.</span></span> <span data-ttu-id="1834a-129">Чтобы найти версию своего модуля, введите: `(Get-Module Azure).Version`.</span><span class="sxs-lookup"><span data-stu-id="1834a-129">To find the version of your module, type: `(Get-Module Azure).Version`.</span></span>

<span data-ttu-id="1834a-130">Примеры скриптов, с помощью которых можно автоматизировать некоторые распространенные задачи в Azure, см. в [центре скриптов Microsoft Azure](http://www.windowsazure.com/documentation/scripts/).</span><span class="sxs-lookup"><span data-stu-id="1834a-130">For sample scripts that can help you automate some of the common tasks in Azure, see the [Windows Azure Script Center](http://www.windowsazure.com/documentation/scripts/).</span></span>

<span data-ttu-id="1834a-131">Общие сведения об установке, обучении, использовании и настройке Windows PowerShell см. в статье, посвященной [работе со скриптами в Windows PowerShell](http://go.microsoft.com/fwlink/p/?linkid=320210).</span><span class="sxs-lookup"><span data-stu-id="1834a-131">For general information about installing, learning, using, and customizing Windows PowerShell, see [Scripting with Windows PowerShell](http://go.microsoft.com/fwlink/p/?linkid=320210).</span></span>
