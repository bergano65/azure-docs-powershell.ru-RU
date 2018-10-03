---
title: Критически важные изменения в Microsoft Azure PowerShell 6.0.0
description: Это руководство по миграции содержит список критических изменений, внесенных в выпуск Azure PowerShell версии 6.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/01/2018
ms.openlocfilehash: 227bec0f7eb24b0941e9e21d37524b290c4b83a5
ms.sourcegitcommit: 19dffee617477001f98d43e39a50ce1fad087b74
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2018
ms.locfileid: "47178516"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-600"></a><span data-ttu-id="b375f-103">Критически важные изменения в Microsoft Azure PowerShell 6.0.0</span><span class="sxs-lookup"><span data-stu-id="b375f-103">Breaking changes for Microsoft Azure PowerShell 6.0.0</span></span>

<span data-ttu-id="b375f-104">Этот документ предназначен для уведомления о критических изменениях и является руководством по миграции для пользователей командлетов Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b375f-104">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span> <span data-ttu-id="b375f-105">В каждом разделе описана причина критического изменения и самый простой путь миграции.</span><span class="sxs-lookup"><span data-stu-id="b375f-105">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span> <span data-ttu-id="b375f-106">Подробное описание см. в запросах на вытягивание для каждого изменения.</span><span class="sxs-lookup"><span data-stu-id="b375f-106">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="b375f-107">Оглавление</span><span class="sxs-lookup"><span data-stu-id="b375f-107">Table of Contents</span></span>

- [<span data-ttu-id="b375f-108">Общие критически важные изменения</span><span class="sxs-lookup"><span data-stu-id="b375f-108">General breaking changes</span></span>](#general-breaking-changes)
    - [<span data-ttu-id="b375f-109">Минимальная требуемая версия изменена на PowerShell 5.0</span><span class="sxs-lookup"><span data-stu-id="b375f-109">Minimum PowerShell version required bumped to 5.0</span></span>](#minimum-powershell-version-required-bumped-to-50)
    - [<span data-ttu-id="b375f-110">Автосохранение контекста включено по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b375f-110">Context autosaved enabled by default</span></span>](#context-autosave-enabled-by-default)
    - [<span data-ttu-id="b375f-111">Удаление псевдонимов Tags</span><span class="sxs-lookup"><span data-stu-id="b375f-111">Removal of Tags alias</span></span>](#removal-of-tags-alias)
- [<span data-ttu-id="b375f-112">Критически важные изменения в командлетах AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b375f-112">Breaking changes to AzureRM.Compute cmdlets</span></span>](#breaking-changes-to-azurermcompute-cmdlets)
- [<span data-ttu-id="b375f-113">Критически важные изменения в командлетах AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b375f-113">Breaking changes to AzureRM.DataLakeStore cmdlets</span></span>](#breaking-changes-to-azurermdatalakestore-cmdlets)
- [<span data-ttu-id="b375f-114">Критически важные изменения в командлетах AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="b375f-114">Breaking changes to AzureRM.Dns cmdlets</span></span>](#breaking-changes-to-azurermdns-cmdlets)
- [<span data-ttu-id="b375f-115">Критически важные изменения в командлетах AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="b375f-115">Breaking changes to AzureRM.Insights cmdlets</span></span>](#breaking-changes-to-azurerminsights-cmdlets)
- [<span data-ttu-id="b375f-116">Критически важные изменения в командлетах AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b375f-116">Breaking changes to AzureRM.KeyVault cmdlets</span></span>](#breaking-changes-to-azurermkeyvault-cmdlets)
- [<span data-ttu-id="b375f-117">Критически важные изменения в командлетах AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b375f-117">Breaking changes to AzureRM.Network cmdlets</span></span>](#breaking-changes-to-azurermnetwork-cmdlets)
- [<span data-ttu-id="b375f-118">Критически важные изменения в командлетах AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="b375f-118">Breaking changes to AzureRM.RedisCache cmdlets</span></span>](#breaking-changes-to-azurermrediscache-cmdlets)
- [<span data-ttu-id="b375f-119">Критически важные изменения в командлетах AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="b375f-119">Breaking changes to AzureRM.Resources cmdlets</span></span>](#breaking-changes-to-azurermresources-cmdlets)
- [<span data-ttu-id="b375f-120">Критически важные изменения в командлетах AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="b375f-120">Breaking changes to AzureRM.Storage cmdlets</span></span>](#breaking-changes-to-azurermstorage-cmdlets)
- [<span data-ttu-id="b375f-121">Удаленные модули</span><span class="sxs-lookup"><span data-stu-id="b375f-121">Removed modules</span></span>](#removed-modules)
    - [`AzureRM.ServerManagement`](#azurermservermanagement)
    - [`AzureRM.SiteRecovery`](#azurermsiterecovery)

## <a name="general-breaking-changes"></a><span data-ttu-id="b375f-122">Общие критически важные изменения</span><span class="sxs-lookup"><span data-stu-id="b375f-122">General breaking changes</span></span>

### <a name="minimum-powershell-version-required-bumped-to-50"></a><span data-ttu-id="b375f-123">Минимальная требуемая версия изменена на PowerShell 5.0</span><span class="sxs-lookup"><span data-stu-id="b375f-123">Minimum PowerShell version required bumped to 5.0</span></span>

<span data-ttu-id="b375f-124">Ранее для выполнения любого командлета требовалась версия _не ниже_ Azure PowerShell 3.0.</span><span class="sxs-lookup"><span data-stu-id="b375f-124">Previously, Azure PowerShell required _at least_ version 3.0 of PowerShell to run any cmdlet.</span></span> <span data-ttu-id="b375f-125">Со временем требуемая версия повысится до PowerShell 5.0.</span><span class="sxs-lookup"><span data-stu-id="b375f-125">Moving forward, this requirement will be raised to version 5.0 of PowerShell.</span></span> <span data-ttu-id="b375f-126">Сведения об обновлении до PowerShell 5.0 см. в [этой таблице](https://docs.microsoft.com/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="b375f-126">For information on upgrading to PowerShell 5.0, please see [this table](https://docs.microsoft.com/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span></span>

### <a name="context-autosave-enabled-by-default"></a><span data-ttu-id="b375f-127">Автосохранение контекста включено по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b375f-127">Context autosave enabled by default</span></span>

<span data-ttu-id="b375f-128">Автосохранение контекста подразумевает хранение учетных данных Azure, которые могут использоваться в новых или других сеансах PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b375f-128">Context autosave is the storage of Azure sign in information that can be used between new and different PowerShell sessions.</span></span> <span data-ttu-id="b375f-129">Дополнительные сведения об автосохранении контекста см. в [этом документе](https://docs.microsoft.com/powershell/azure/context-persistence).</span><span class="sxs-lookup"><span data-stu-id="b375f-129">For more information on context autosave, please see [this document](https://docs.microsoft.com/powershell/azure/context-persistence).</span></span>

<span data-ttu-id="b375f-130">Ранее эта функция была отключена по умолчанию, то есть сведения об аутентификации пользователей Azure не сохранялись между сеансами. Чтобы включить сохранение контекста пользователи выполняли командлет `Enable-AzureRmContextAutosave`.</span><span class="sxs-lookup"><span data-stu-id="b375f-130">Previously by default, context autosave was disabled, which meant the user's Azure authentication information was not stored between sessions until they ran the `Enable-AzureRmContextAutosave` cmdlet to turn on context persistence.</span></span> <span data-ttu-id="b375f-131">Со временем сохранение контекста будет включено по умолчанию, то есть контекст будет сохраняться при следующем входе в систему пользователей _без сохраненных настроек автосохранения контекста_.</span><span class="sxs-lookup"><span data-stu-id="b375f-131">Moving forward, context autosave will be enabled by default, which means that users _with no saved context autosave settings_ will have their context stored the next time they sign in.</span></span> <span data-ttu-id="b375f-132">Пользователи смогут отключить эту функцию с помощью командлета `Disable-AzureRmContextAutosave`.</span><span class="sxs-lookup"><span data-stu-id="b375f-132">Users can opt out of this functionality by using the `Disable-AzureRmContextAutosave` cmdlet.</span></span>

<span data-ttu-id="b375f-133">_Примечание_. Это изменение не повлияет на пользователей, которые ранее отключили автосохранение контекста или включили эту функцию и используют сохраненный контекст.</span><span class="sxs-lookup"><span data-stu-id="b375f-133">_Note_: users that previously disabled context autosave or users with context autosave enabled and existing contexts will not be affected by this change</span></span>

### <a name="removal-of-tags-alias"></a><span data-ttu-id="b375f-134">Удаление псевдонимов Tags</span><span class="sxs-lookup"><span data-stu-id="b375f-134">Removal of Tags alias</span></span>

<span data-ttu-id="b375f-135">Псевдоним `Tags` для параметра `Tag` удален во многих командлетах.</span><span class="sxs-lookup"><span data-stu-id="b375f-135">The alias `Tags` for the `Tag` parameter has been removed across numerous cmdlets.</span></span> <span data-ttu-id="b375f-136">Ниже приведен список модулей (и соответствующих командлетов), которых коснулось это изменение:</span><span class="sxs-lookup"><span data-stu-id="b375f-136">Below is a list of modules (and the corresponding cmdlets) affected by this:</span></span>

#### `AzureRM.ApiManagement`

- `New-AzureRmApiManagement`
- `New-AzureRmApiManagementProperty`
- `Set-AzureRmApiManagementProperty`

#### `AzureRM.Automation`
- `Set-AzureRmAutomationRunbook`

#### `AzureRM.Cdn`
- `New-AzureRmCdnEndpoint`
- `New-AzureRmCdnProfile`

#### `AzureRM.Compute`
- `New-AzureRmVM`
- `Update-AzureRmVM`

#### `AzureRM.DataFactories`
- `New-AzureRmDataFactories`

#### `AzureRM.DataLakeAnalytics`
- `New-AzureRmDataLakeAnalyticsAccount`

#### `AzureRM.DataLakeStore`
- `New-AzureRmDataLakeStoreAccount`
- `Set-AzureRmDataLakeStoreAccount`

#### `AzureRM.MachineLearning`
- `Update-AzureRmMlCommitmentPlan`

#### `AzureRM.Media`
- `Set-AzureRmMediaService`

#### `AzureRM.OperationalInsights`
- `New-AzureRmOperationalInsightsSavedSearch`
- `New-AzureRmOperationalInsightsWorkspace`
- `Set-AzureRmOperationalInsightsSavedSearch`
- `Set-AzureRmOperationalInsightsWorkspace`

## <a name="breaking-changes-to-azurermcompute-cmdlets"></a><span data-ttu-id="b375f-137">Критически важные изменения в командлетах AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b375f-137">Breaking changes to AzureRM.Compute cmdlets</span></span>

<span data-ttu-id="b375f-138">**Разное**</span><span class="sxs-lookup"><span data-stu-id="b375f-138">**Miscellaneous**</span></span>
- <span data-ttu-id="b375f-139">Свойство имени SKU, вложенное в типы `PSDisk` и `PSSnapshot`, изменено с `StandardLRS` и `PremiumLRS` на `Standard_LRS` и `Premium_LRS` соответственно.</span><span class="sxs-lookup"><span data-stu-id="b375f-139">The sku name property nested in types `PSDisk` and `PSSnapshot` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

```powershell
$disk = Get-AzureRmDisk -ResourceGroupName "MyResourceGroup" -DiskName "MyDiskName"
$disk.Sku.Name       # This will now return Standard_LRS or Premium_LRS

$snapshot = Get-AzureRmSnapshot -ResourceGroupName "MyResourceGroup" -SnapshotName "MySnapshotName"
$snapshot.Sku.Name   # This will now return Standard_LRS or Premium_LRS
```

- <span data-ttu-id="b375f-140">Свойство учетной записи хранения, вложенное в типы `PSVirtualMachine`, `PSVirtualMachineScaleSet` и `PSImage`, изменено с `StandardLRS` и `PremiumLRS` на `Standard_LRS` и `Premium_LRS` соответственно.</span><span class="sxs-lookup"><span data-stu-id="b375f-140">The storage account type property nested in types `PSVirtualMachine`, `PSVirtualMachineScaleSet` and `PSImage` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

```powershell
$vm = Get-AzureRmVM -ResourceGroupName "MyResourceGroup" -Name "MyVM"
$vm.StorageProfile.DataDisks[0].ManagedDisk.StorageAccountType   # This will now return Standard_LRS or Premium_LRS
```

<span data-ttu-id="b375f-141">**Add-AzureRmImageDataDisk**</span><span class="sxs-lookup"><span data-stu-id="b375f-141">**Add-AzureRmImageDataDisk**</span></span>
- <span data-ttu-id="b375f-142">Допустимые значения для параметра `StorageAccountType` изменены с `StandardLRS` и `PremiumLRS` на `Standard_LRS` и `Premium_LRS`соответственно.</span><span class="sxs-lookup"><span data-stu-id="b375f-142">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="b375f-143">**Add-AzureRmVMDataDisk**</span><span class="sxs-lookup"><span data-stu-id="b375f-143">**Add-AzureRmVMDataDisk**</span></span>
- <span data-ttu-id="b375f-144">Допустимые значения для параметра `StorageAccountType` изменены с `StandardLRS` и `PremiumLRS` на `Standard_LRS` и `Premium_LRS`соответственно.</span><span class="sxs-lookup"><span data-stu-id="b375f-144">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="b375f-145">**Add-AzureRmVmssDataDisk**</span><span class="sxs-lookup"><span data-stu-id="b375f-145">**Add-AzureRmVmssDataDisk**</span></span>
- <span data-ttu-id="b375f-146">Допустимые значения для параметра `StorageAccountType` изменены с `StandardLRS` и `PremiumLRS` на `Standard_LRS` и `Premium_LRS`соответственно.</span><span class="sxs-lookup"><span data-stu-id="b375f-146">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="b375f-147">**New-AzureRmAvailabilitySet**</span><span class="sxs-lookup"><span data-stu-id="b375f-147">**New-AzureRmAvailabilitySet**</span></span>
- <span data-ttu-id="b375f-148">Параметр `Managed` изменен на `Sku`.</span><span class="sxs-lookup"><span data-stu-id="b375f-148">The parameter `Managed` was removed in favor of `Sku`</span></span>

```powershell
# Old
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Managed

# New
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Sku "Aligned"
```

<span data-ttu-id="b375f-149">**New-AzureRmDiskConfig**</span><span class="sxs-lookup"><span data-stu-id="b375f-149">**New-AzureRmDiskConfig**</span></span>
- <span data-ttu-id="b375f-150">Допустимые значения для параметра `SkuName` изменены с `StandardLRS` и `PremiumLRS` на `Standard_LRS` и `Premium_LRS`соответственно.</span><span class="sxs-lookup"><span data-stu-id="b375f-150">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="b375f-151">**New-AzureRmDiskUpdateConfig**</span><span class="sxs-lookup"><span data-stu-id="b375f-151">**New-AzureRmDiskUpdateConfig**</span></span>
- <span data-ttu-id="b375f-152">Допустимые значения для параметра `SkuName` изменены с `StandardLRS` и `PremiumLRS` на `Standard_LRS` и `Premium_LRS`соответственно.</span><span class="sxs-lookup"><span data-stu-id="b375f-152">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="b375f-153">**New-AzureRmSnapshotConfig**</span><span class="sxs-lookup"><span data-stu-id="b375f-153">**New-AzureRmSnapshotConfig**</span></span>
- <span data-ttu-id="b375f-154">Допустимые значения для параметра `SkuName` изменены с `StandardLRS` и `PremiumLRS` на `Standard_LRS` и `Premium_LRS`соответственно.</span><span class="sxs-lookup"><span data-stu-id="b375f-154">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="b375f-155">**New-AzureRmSnapshotUpdateConfig**</span><span class="sxs-lookup"><span data-stu-id="b375f-155">**New-AzureRmSnapshotUpdateConfig**</span></span>
- <span data-ttu-id="b375f-156">Допустимые значения для параметра `SkuName` изменены с `StandardLRS` и `PremiumLRS` на `Standard_LRS` и `Premium_LRS`соответственно.</span><span class="sxs-lookup"><span data-stu-id="b375f-156">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="b375f-157">**Set-AzureRmImageOsDisk**</span><span class="sxs-lookup"><span data-stu-id="b375f-157">**Set-AzureRmImageOsDisk**</span></span>
- <span data-ttu-id="b375f-158">Допустимые значения для параметра `StorageAccountType` изменены с `StandardLRS` и `PremiumLRS` на `Standard_LRS` и `Premium_LRS`соответственно.</span><span class="sxs-lookup"><span data-stu-id="b375f-158">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="b375f-159">**Set-AzureRmVMAEMExtension**</span><span class="sxs-lookup"><span data-stu-id="b375f-159">**Set-AzureRmVMAEMExtension**</span></span>
- <span data-ttu-id="b375f-160">Удален параметр `DisableWAD`.</span><span class="sxs-lookup"><span data-stu-id="b375f-160">The parameter `DisableWAD` was removed</span></span>
    -  <span data-ttu-id="b375f-161">Система диагностики Microsoft Azure отключена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b375f-161">Windows Azure Diagnostics is disabled by default</span></span>

<span data-ttu-id="b375f-162">**Set-AzureRmVMDataDisk**</span><span class="sxs-lookup"><span data-stu-id="b375f-162">**Set-AzureRmVMDataDisk**</span></span>
- <span data-ttu-id="b375f-163">Допустимые значения для параметра `StorageAccountType` изменены с `StandardLRS` и `PremiumLRS` на `Standard_LRS` и `Premium_LRS`соответственно.</span><span class="sxs-lookup"><span data-stu-id="b375f-163">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="b375f-164">**Set-AzureRmVMOSDisk**</span><span class="sxs-lookup"><span data-stu-id="b375f-164">**Set-AzureRmVMOSDisk**</span></span>
- <span data-ttu-id="b375f-165">Допустимые значения для параметра `StorageAccountType` изменены с `StandardLRS` и `PremiumLRS` на `Standard_LRS` и `Premium_LRS`соответственно.</span><span class="sxs-lookup"><span data-stu-id="b375f-165">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="b375f-166">**Set-AzureRmVmssStorageProfile**</span><span class="sxs-lookup"><span data-stu-id="b375f-166">**Set-AzureRmVmssStorageProfile**</span></span>
- <span data-ttu-id="b375f-167">Допустимые значения для параметра `ManagedDisk` изменены с `StandardLRS` и `PremiumLRS` на `Standard_LRS` и `Premium_LRS`соответственно.</span><span class="sxs-lookup"><span data-stu-id="b375f-167">The accepted values for parameter `ManagedDisk` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="b375f-168">**Update-AzureRmVmss**</span><span class="sxs-lookup"><span data-stu-id="b375f-168">**Update-AzureRmVmss**</span></span>
- <span data-ttu-id="b375f-169">Допустимые значения для параметра `ManagedDiskStorageAccountType` изменены с `StandardLRS` и `PremiumLRS` на `Standard_LRS` и `Premium_LRS`соответственно.</span><span class="sxs-lookup"><span data-stu-id="b375f-169">The accepted values for parameter `ManagedDiskStorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

## <a name="breaking-changes-to-azurermdatalakestore-cmdlets"></a><span data-ttu-id="b375f-170">Критически важные изменения в командлетах AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b375f-170">Breaking changes to AzureRM.DataLakeStore cmdlets</span></span>

<span data-ttu-id="b375f-171">**Export-AzureRmDataLakeStoreItem**</span><span class="sxs-lookup"><span data-stu-id="b375f-171">**Export-AzureRmDataLakeStoreItem**</span></span>
- <span data-ttu-id="b375f-172">Удалены параметры `PerFileThreadCount` и `ConcurrentFileCount`.</span><span class="sxs-lookup"><span data-stu-id="b375f-172">Parameters `PerFileThreadCount` and `ConcurrentFileCount` were removed.</span></span> <span data-ttu-id="b375f-173">В дальнейшем используйте параметр `Concurrency`.</span><span class="sxs-lookup"><span data-stu-id="b375f-173">Please use the `Concurrency` parameter moving forward</span></span>

```powershell
# Old
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -Concurrency 160
```

<span data-ttu-id="b375f-174">**Import-AzureRmDataLakeStoreItem**</span><span class="sxs-lookup"><span data-stu-id="b375f-174">**Import-AzureRmDataLakeStoreItem**</span></span>
- <span data-ttu-id="b375f-175">Удалены параметры `PerFileThreadCount` и `ConcurrentFileCount`.</span><span class="sxs-lookup"><span data-stu-id="b375f-175">Parameters `PerFileThreadCount` and `ConcurrentFileCount` were removed.</span></span> <span data-ttu-id="b375f-176">В дальнейшем используйте параметр `Concurrency`.</span><span class="sxs-lookup"><span data-stu-id="b375f-176">Please use the `Concurrency` parameter moving forward</span></span>

```powershell
# Old
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -Concurrency 160
```

<span data-ttu-id="b375f-177">**Remove-AzureRmDataLakeStoreItem**</span><span class="sxs-lookup"><span data-stu-id="b375f-177">**Remove-AzureRmDataLakeStoreItem**</span></span>
- <span data-ttu-id="b375f-178">Удален параметр `Clean`.</span><span class="sxs-lookup"><span data-stu-id="b375f-178">Parameter `Clean` was removed</span></span>

```powershell
# Old
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse -Clean

# New
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse
```

## <a name="breaking-changes-to-azurermdns-cmdlets"></a><span data-ttu-id="b375f-179">Критически важные изменения в командлетах AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="b375f-179">Breaking changes to AzureRM.Dns cmdlets</span></span>

<span data-ttu-id="b375f-180">**New-AzureRmDnsRecordSet**</span><span class="sxs-lookup"><span data-stu-id="b375f-180">**New-AzureRmDnsRecordSet**</span></span>
- <span data-ttu-id="b375f-181">Удален параметр `Force`.</span><span class="sxs-lookup"><span data-stu-id="b375f-181">The parameter `Force` was removed</span></span>

<span data-ttu-id="b375f-182">**Remove-AzureRmDnsRecordSet**</span><span class="sxs-lookup"><span data-stu-id="b375f-182">**Remove-AzureRmDnsRecordSet**</span></span>
- <span data-ttu-id="b375f-183">Удален параметр `Force`.</span><span class="sxs-lookup"><span data-stu-id="b375f-183">The parameter `Force` was removed</span></span>

<span data-ttu-id="b375f-184">**Remove-AzureRmDnsZone**</span><span class="sxs-lookup"><span data-stu-id="b375f-184">**Remove-AzureRmDnsZone**</span></span>
- <span data-ttu-id="b375f-185">Удален параметр `Force`.</span><span class="sxs-lookup"><span data-stu-id="b375f-185">The parameter `Force` was removed</span></span>

## <a name="breaking-changes-to-azurerminsights-cmdlets"></a><span data-ttu-id="b375f-186">Критически важные изменения в командлетах AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="b375f-186">Breaking changes to AzureRM.Insights cmdlets</span></span>

<span data-ttu-id="b375f-187">**Add-AzureRmAutoscaleSetting**</span><span class="sxs-lookup"><span data-stu-id="b375f-187">**Add-AzureRmAutoscaleSetting**</span></span>
- <span data-ttu-id="b375f-188">Удалены псевдонимы параметра `AutoscaleProfiles` и `Notifications`.</span><span class="sxs-lookup"><span data-stu-id="b375f-188">The parameter aliases `AutoscaleProfiles` and `Notifications` were removed</span></span>

<span data-ttu-id="b375f-189">**Add-AzureRmLogProfile**</span><span class="sxs-lookup"><span data-stu-id="b375f-189">**Add-AzureRmLogProfile**</span></span>
- <span data-ttu-id="b375f-190">Удалены псевдонимы параметра `Categories` и `Locations`.</span><span class="sxs-lookup"><span data-stu-id="b375f-190">The parameter aliases `Categories` and `Locations` were removed</span></span>

<span data-ttu-id="b375f-191">**Add-AzureRmMetricAlertRule**</span><span class="sxs-lookup"><span data-stu-id="b375f-191">**Add-AzureRmMetricAlertRule**</span></span>
- <span data-ttu-id="b375f-192">Удален псевдоним параметра `Actions`.</span><span class="sxs-lookup"><span data-stu-id="b375f-192">The parameter alias `Actions` was removed</span></span>

<span data-ttu-id="b375f-193">**Add-AzureRmWebtestAlertRule**</span><span class="sxs-lookup"><span data-stu-id="b375f-193">**Add-AzureRmWebtestAlertRule**</span></span>
- <span data-ttu-id="b375f-194">Удален псевдоним параметра `Actions`.</span><span class="sxs-lookup"><span data-stu-id="b375f-194">The parameter alias `Actions` was removed</span></span>

<span data-ttu-id="b375f-195">**Get-AzureRmLog**</span><span class="sxs-lookup"><span data-stu-id="b375f-195">**Get-AzureRmLog**</span></span>
- <span data-ttu-id="b375f-196">Удалены псевдонимы параметра `MaxRecords` и `MaxEvents`.</span><span class="sxs-lookup"><span data-stu-id="b375f-196">The parameter aliases `MaxRecords` and `MaxEvents` were removed</span></span>

<span data-ttu-id="b375f-197">**Get-AzureRmMetricDefinition**</span><span class="sxs-lookup"><span data-stu-id="b375f-197">**Get-AzureRmMetricDefinition**</span></span>
- <span data-ttu-id="b375f-198">Удален псевдоним параметра `MetricNames`.</span><span class="sxs-lookup"><span data-stu-id="b375f-198">The parameter alias `MetricNames` was removed</span></span>

<span data-ttu-id="b375f-199">**New-AzureRmAlertRuleEmail**</span><span class="sxs-lookup"><span data-stu-id="b375f-199">**New-AzureRmAlertRuleEmail**</span></span>
- <span data-ttu-id="b375f-200">Удалены псевдонимы параметра `CustomEmails` и `SendToServiceOwners`.</span><span class="sxs-lookup"><span data-stu-id="b375f-200">The parameter aliases `CustomEmails` and `SendToServiceOwners` were removed</span></span>

<span data-ttu-id="b375f-201">**New-AzureRmAlertRuleWebhook**</span><span class="sxs-lookup"><span data-stu-id="b375f-201">**New-AzureRmAlertRuleWebhook**</span></span>
- <span data-ttu-id="b375f-202">Удален псевдоним параметра `Properties`.</span><span class="sxs-lookup"><span data-stu-id="b375f-202">The parameter alias `Properties` was removed</span></span>

<span data-ttu-id="b375f-203">**New-AzureRmAutoscaleNotification**</span><span class="sxs-lookup"><span data-stu-id="b375f-203">**New-AzureRmAutoscaleNotification**</span></span>
- <span data-ttu-id="b375f-204">Удалены псевдонимы параметра `CustomEmails`, `SendEmailToSubscriptionCoAdministrators` и `Webhooks`.</span><span class="sxs-lookup"><span data-stu-id="b375f-204">The parameter aliases `CustomEmails`, `SendEmailToSubscriptionCoAdministrators` and `Webhooks` were removed</span></span>

<span data-ttu-id="b375f-205">**New-AzureRmAutoscaleProfile**</span><span class="sxs-lookup"><span data-stu-id="b375f-205">**New-AzureRmAutoscaleProfile**</span></span>
- <span data-ttu-id="b375f-206">Удалены псевдонимы параметра `Rules`, `ScheduleDays`, `ScheduleHours` и `ScheduleMinutes`.</span><span class="sxs-lookup"><span data-stu-id="b375f-206">The parameter aliases `Rules`, `ScheduleDays`, `ScheduleHours` and `ScheduleMinutes` were removed</span></span>

<span data-ttu-id="b375f-207">**New-AzureRmAutoscaleWebhook**</span><span class="sxs-lookup"><span data-stu-id="b375f-207">**New-AzureRmAutoscaleWebhook**</span></span>
- <span data-ttu-id="b375f-208">Удален псевдоним параметра `Properties`.</span><span class="sxs-lookup"><span data-stu-id="b375f-208">The parameter alias `Properties` was removed</span></span>

## <a name="breaking-changes-to-azurermkeyvault-cmdlets"></a><span data-ttu-id="b375f-209">Критически важные изменения в командлетах AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b375f-209">Breaking changes to AzureRM.KeyVault cmdlets</span></span>

<span data-ttu-id="b375f-210">**Add-AzureKeyVaultCertificate**</span><span class="sxs-lookup"><span data-stu-id="b375f-210">**Add-AzureKeyVaultCertificate**</span></span>
- <span data-ttu-id="b375f-211">Параметр `CertificatePolicy` стал обязательным.</span><span class="sxs-lookup"><span data-stu-id="b375f-211">The `CertificatePolicy` parameter has become mandatory.</span></span>

<span data-ttu-id="b375f-212">**Set-AzureKeyVaultManagedStorageSasDefinition**</span><span class="sxs-lookup"><span data-stu-id="b375f-212">**Set-AzureKeyVaultManagedStorageSasDefinition**</span></span>
- <span data-ttu-id="b375f-213">Этот командлет больше не принимает отдельные параметры, из которых состоит маркер доступа. Вместо этого он изменяет такие явные параметры маркеров, как `Service` или `Permissions`, на универсальный параметр `TemplateUri`, который соответствуют примеру маркера доступа, определенному в другом месте (предположительно с помощью командлетов службы хранилища PowerShell или созданных вручную в соответствии с документацией службы хранилища.) В командлете сохранен параметр `ValidityPeriod`.</span><span class="sxs-lookup"><span data-stu-id="b375f-213">The cmdlet no longer accepts individual parameters that compose the access token; instead, the cmdlet replaces explicit token parameters, such as `Service` or `Permissions`, with a generic `TemplateUri` parameter, corresponding to a sample access token defined elsewhere (presumably using Storage PowerShell cmdlets, or composed manually according to the Storage documentation.) The cmdlet retains the `ValidityPeriod` parameter.</span></span>

<span data-ttu-id="b375f-214">Дополнительные сведения о создании общих маркеров доступа для службы хранилища Azure см. на страницах соответствующей документации.</span><span class="sxs-lookup"><span data-stu-id="b375f-214">For more information on composing shared access tokens for Azure Storage, please refer to the documentation pages, respectively:</span></span>
- <span data-ttu-id="b375f-215">[Constructing a Service SAS] (https://docs.microsoft.com/rest/api/storageservices/Constructing-a-Service-SAS) (Создание подписанного URL-адреса уровня службы)</span><span class="sxs-lookup"><span data-stu-id="b375f-215">[Constructing a Service SAS] (https://docs.microsoft.com/rest/api/storageservices/Constructing-a-Service-SAS)</span></span>
- <span data-ttu-id="b375f-216">[Создание подписанного URL-адреса уровня учетной записи] (https://docs.microsoft.com/rest/api/storageservices/constructing-an-account-sas)</span><span class="sxs-lookup"><span data-stu-id="b375f-216">[Constructing an Account SAS] (https://docs.microsoft.com/rest/api/storageservices/constructing-an-account-sas)</span></span>

```powershell
# Old
$sas = Set-AzureKeyVaultManagedStorageSasDefinition -VaultName myVault -Name myKey -Service Blob -Permissions 'rcw' -ValidityPeriod 180d

# New
$sctx=New-AzureStorageContext -StorageAccountName $sa.StorageAccountName -Protocol Https -StorageAccountKey Key1
$start=[System.DateTime]::Now.AddDays(-1)
$end=[System.DateTime]::Now.AddMonths(1)
$at=New-AzureStorageAccountSasToken -Service blob -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -StartTime $start -ExpiryTime $end -Context $sctx
$sas=Set-AzureKeyVaultManagedStorageSasDefinition -AccountName $sa.StorageAccountName -VaultName $kv.VaultName -Name accountsas -TemplateUri $at -SasType 'account' -ValidityPeriod ([System.Timespan]::FromDays(30))
```

<span data-ttu-id="b375f-217">**Set-AzureKeyVaultCertificateIssuer**</span><span class="sxs-lookup"><span data-stu-id="b375f-217">**Set-AzureKeyVaultCertificateIssuer**</span></span>
- <span data-ttu-id="b375f-218">Параметр `IssuerProvider` стал обязательным.</span><span class="sxs-lookup"><span data-stu-id="b375f-218">The `IssuerProvider` parameter has become mandatory.</span></span>

<span data-ttu-id="b375f-219">**Undo-AzureKeyVaultCertificateRemoval**</span><span class="sxs-lookup"><span data-stu-id="b375f-219">**Undo-AzureKeyVaultCertificateRemoval**</span></span>
- <span data-ttu-id="b375f-220">Выходной параметр этого командлета изменен с `CertificateBundle` на `PSKeyVaultCertificate`.</span><span class="sxs-lookup"><span data-stu-id="b375f-220">The output of this cmdlet has changed from `CertificateBundle` to `PSKeyVaultCertificate`.</span></span>

<span data-ttu-id="b375f-221">**Undo-AzureRmKeyVaultRemoval**</span><span class="sxs-lookup"><span data-stu-id="b375f-221">**Undo-AzureRmKeyVaultRemoval**</span></span>
- <span data-ttu-id="b375f-222">Параметр `ResourceGroupName` удален из набора параметров `InputObject`. Вместо этого значения извлекаются из свойства `ResourceId` параметра `InputObject`.</span><span class="sxs-lookup"><span data-stu-id="b375f-222">`ResourceGroupName` has been removed from the `InputObject` parameter set, and is instead obtained from the `InputObject` parameter's `ResourceId` property.</span></span>

<span data-ttu-id="b375f-223">**Set-AzureRmKeyVaultAccessPolicy**</span><span class="sxs-lookup"><span data-stu-id="b375f-223">**Set-AzureRmKeyVaultAccessPolicy**</span></span>
- <span data-ttu-id="b375f-224">Разрешение `all` удалено из `PermissionsToKeys`, `PermissionsToSecrets` и `PermissionsToCertificates`.</span><span class="sxs-lookup"><span data-stu-id="b375f-224">The `all` permission was removed from `PermissionsToKeys`, `PermissionsToSecrets`, and `PermissionsToCertificates`.</span></span>

<span data-ttu-id="b375f-225">**Общие сведения**</span><span class="sxs-lookup"><span data-stu-id="b375f-225">**General**</span></span>
- <span data-ttu-id="b375f-226">Свойство `ValueFromPipelineByPropertyName` удалено из всех командлетов, в которых включен запуск конвейера с использованием свойства `InputObject`.</span><span class="sxs-lookup"><span data-stu-id="b375f-226">The `ValueFromPipelineByPropertyName` property was removed from all cmdlets where piping by `InputObject` was enabled.</span></span>  <span data-ttu-id="b375f-227">Это коснулось следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="b375f-227">The cmdlets affected are:</span></span>
    - `Add-AzureKeyVaultCertificate`
    - `Add-AzureKeyVaultCertificateContact`
    - `Add-AzureKeyVaultKey`
    - `Backup-AzureKeyVaultKey`
    - `Backup-AzureKeyVaultSecret`
    - `Get-AzureKeyVaultCertficate`
    - `Get-AzureKeyVaultCertificateContact`
    - `Get-AzureKeyVaultCertificateIssuer`
    - `Get-AzureKeyVaultCertificateOperation`
    - `Get-AzureKeyVaultCertificatePolicy`
    - `Get-AzureKeyVaultKey`
    - `Get-AzureKeyVaultManagedStorageAccount`
    - `Get-AzureKeyVaultManagedStorageSasDefinition`
    - `Get-AzureKeyVaultSecret`
    - `Remove-AzureRmKeyVault`
    - `Remove-AzureRmKeyVaultAccessPolicy`
    - `Remove-AzureKeyVaultCertificate`
    - `Remove-AzureKeyVaultCertificateContact`
    - `Remove-AzureKeyVaultCertificateIssuer`
    - `Remove-AzureKeyVaultCertificateOperation`
    - `Remove-AzureKeyVaultKey`
    - `Remove-AzureKeyVaultManagedStorageAccount`
    - `Remove-AzureKeyVaultManagedStorageSasDefinition`
    - `Remove-AzureKeyVaultSecret`
    - `Restore-AzureKeyVaultKey`
    - `Restore-AzureKeyVaultSecret`
    - `Set-AzureRmKeyVaultAccessPolicy`
    - `Set-AzureKeyVaultCertificateAttribute`
    - `Set-AzureKeyVaultCertificateIssuer`
    - `Set-AzureKeyVaultCertificatePolicy`
    - `Set-AzureKeyVaultKeyAttribute`
    - `Set-AzureKeyVaultManagedStorageSasDefinition`
    - `Set-AzureKeyVaultSecret`
    - `Set-AzureKeyVaultSecretAttribute`
    - `Stop-AzureKeyVaultCertificateOperation`
    - `Undo-AzureKeyVaultCertificateRemoval`
    - `Undo-AzureKeyVaultKeyRemoval`
    - `Undo-AzureRmKeyVaultRemoval`
    - `Undo-AzureKeyVaultSecretRemoval`
    - `Update-AzureKeyVaultManagedStorageAccount`
    - `Update-AzureKeyVaultManagedStorageAccountKey`

- <span data-ttu-id="b375f-228">Уровни `ConfirmImpact` удалены из всех командлетов.</span><span class="sxs-lookup"><span data-stu-id="b375f-228">`ConfirmImpact` levels were removed from all cmdlets.</span></span>  <span data-ttu-id="b375f-229">Это коснулось следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="b375f-229">The cmdlets affected are:</span></span>
    - `Remove-AzureRmKeyVault`
    - `Remove-AzureKeyVaultCertificate`
    - `Remove-AzureKeyVaultCertificateIssuer`
    - `Remove-AzureKeyVaultCertificateOperation`
    - `Remove-AzureKeyVaultKey`
    - `Remove-AzureKeyVaultManagedStorageAccount`
    - `Remove-AzureKeyVaultManagedStorageSasDefinition`
    - `Remove-AzureKeyVaultSecret`
    - `Stop-AzureKeyVaultCertificateOperation`
    - `Update-AzureKeyVaultManagedStorageAccountKey`

- <span data-ttu-id="b375f-230">Обновлен параметр `IKeyVaultDataServiceClient`. Теперь все операции с сертификатами возвращают PSTypes вместо типов пакетов SDK.</span><span class="sxs-lookup"><span data-stu-id="b375f-230">The `IKeyVaultDataServiceClient` was updated so all Certificate operations return PSTypes instead of SDK types.</span></span> <span data-ttu-id="b375f-231">А именно:</span><span class="sxs-lookup"><span data-stu-id="b375f-231">This includes:</span></span>
    - `SetCertificateContacts`
    - `GetCertificateContacts`
    - `GetCertificate`
    - `GetDeletedCertificate`
    - `MergeCertificate`
    - `ImportCertificate`
    - `DeleteCertificate`
    - `RecoverCertificate`
    - `EnrollCertificate`
    - `UpdateCertificate`
    - `GetCertificateOperation`
    - `DeleteCertificateOperation`
    - `CancelCertificateOperation`
    - `GetCertificatePolicy`
    - `UpdateCertificatePolicy`
    - `GetCertificateIssuer`
    - `SetCertificateIssuer`
    - `DeleteCertificateIssuer`

## <a name="breaking-changes-to-azurermnetwork-cmdlets"></a><span data-ttu-id="b375f-232">Критически важные изменения в командлетах AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b375f-232">Breaking changes to AzureRM.Network cmdlets</span></span>


<span data-ttu-id="b375f-233">**Add-AzureRmApplicationGatewayBackendHttpSettings**</span><span class="sxs-lookup"><span data-stu-id="b375f-233">**Add-AzureRmApplicationGatewayBackendHttpSettings**</span></span>
- <span data-ttu-id="b375f-234">Удален параметр `ProbeEnabled`.</span><span class="sxs-lookup"><span data-stu-id="b375f-234">The parameter `ProbeEnabled` was removed</span></span>

<span data-ttu-id="b375f-235">**Add-AzureRmVirtualNetworkPeering**</span><span class="sxs-lookup"><span data-stu-id="b375f-235">**Add-AzureRmVirtualNetworkPeering**</span></span>
- <span data-ttu-id="b375f-236">Удален псевдоним параметра `AlloowGatewayTransit`.</span><span class="sxs-lookup"><span data-stu-id="b375f-236">The parameter alias `AlloowGatewayTransit` was removed</span></span>

<span data-ttu-id="b375f-237">**New-AzureRmApplicationGatewayBackendHttpSettings**</span><span class="sxs-lookup"><span data-stu-id="b375f-237">**New-AzureRmApplicationGatewayBackendHttpSettings**</span></span>
- <span data-ttu-id="b375f-238">Удален параметр `ProbeEnabled`.</span><span class="sxs-lookup"><span data-stu-id="b375f-238">The parameter `ProbeEnabled` was removed</span></span>

<span data-ttu-id="b375f-239">**Set-AzureRmApplicationGatewayBackendHttpSettings**</span><span class="sxs-lookup"><span data-stu-id="b375f-239">**Set-AzureRmApplicationGatewayBackendHttpSettings**</span></span>
- <span data-ttu-id="b375f-240">Удален параметр `ProbeEnabled`.</span><span class="sxs-lookup"><span data-stu-id="b375f-240">The parameter `ProbeEnabled` was removed</span></span>

## <a name="breaking-changes-to-azurermrediscache-cmdlets"></a><span data-ttu-id="b375f-241">Критически важные изменения в командлетах AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="b375f-241">Breaking changes to AzureRM.RedisCache cmdlets</span></span>

<span data-ttu-id="b375f-242">**New-AzureRmRedisCache**</span><span class="sxs-lookup"><span data-stu-id="b375f-242">**New-AzureRmRedisCache**</span></span>
- <span data-ttu-id="b375f-243">Параметры `Subnet` и `VirtualNetwork` заменены на `SubnetId`.</span><span class="sxs-lookup"><span data-stu-id="b375f-243">The parameters `Subnet` and `VirtualNetwork` were removed in favor of `SubnetId`</span></span>
- <span data-ttu-id="b375f-244">Удален параметр `RedisVersion`.</span><span class="sxs-lookup"><span data-stu-id="b375f-244">The parameter `RedisVersion` was removed</span></span>
- <span data-ttu-id="b375f-245">Параметр `MaxMemoryPolicy` заменен на `RedisConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="b375f-245">The parameter `MaxMemoryPolicy` was removed in favor of `RedisConfiguration`</span></span>

```powershell
# Old
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -MaxMemoryPolicy "allkeys-lru"

# New
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

<span data-ttu-id="b375f-246">**Set-AzureRmRedisCache**</span><span class="sxs-lookup"><span data-stu-id="b375f-246">**Set-AzureRmRedisCache**</span></span>
- <span data-ttu-id="b375f-247">Параметр `MaxMemoryPolicy` заменен на `RedisConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="b375f-247">The parameter `MaxMemoryPolicy` was removed in favor of `RedisConfiguration`</span></span>

```powershell
# Old
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -MaxMemoryPolicy "allkeys-lru"

# New
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

## <a name="breaking-changes-to-azurermresources-cmdlets"></a><span data-ttu-id="b375f-248">Критически важные изменения в командлетах AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="b375f-248">Breaking changes to AzureRM.Resources cmdlets</span></span>

<span data-ttu-id="b375f-249">**Find-AzureRmResource**</span><span class="sxs-lookup"><span data-stu-id="b375f-249">**Find-AzureRmResource**</span></span>
- <span data-ttu-id="b375f-250">Этот командлет удален и его функции переданы `Get-AzureRmResource`.</span><span class="sxs-lookup"><span data-stu-id="b375f-250">This cmdlet was removed and the functionality was moved into `Get-AzureRmResource`</span></span>

```powershell
# Old
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupNameContains "ResourceGroup"
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceNameContains "test"

# New
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupName "*ResourceGroup*"
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -Name "*test*"
```

<span data-ttu-id="b375f-251">**Find-AzureRmResourceGroup**</span><span class="sxs-lookup"><span data-stu-id="b375f-251">**Find-AzureRmResourceGroup**</span></span>
- <span data-ttu-id="b375f-252">Этот командлет удален и его функции переданы `Get-AzureRmResourceGroup`.</span><span class="sxs-lookup"><span data-stu-id="b375f-252">This cmdlet was removed and the functionality was moved into `Get-AzureRmResourceGroup`</span></span>

```powershell
# Old
Find-AzureRmResourceGroup
Find-AzureRmResourceGroup -Tag @{ "testtag" = $null }
Find-AzureRmResourceGroup -Tag @{ "testtag" = "testval" }

# New
Get-AzureRmResourceGroup
Get-AzureRmResourceGroup -Tag @{ "testtag" = $null }
Get-AzureRmResourceGroup -Tag @{ "testtag" = "testval" }
```

<span data-ttu-id="b375f-253">**Get-AzureRmRoleDefinition**</span><span class="sxs-lookup"><span data-stu-id="b375f-253">**Get-AzureRmRoleDefinition**</span></span>
- <span data-ttu-id="b375f-254">Удален параметр `AtScopeAndBelow`.</span><span class="sxs-lookup"><span data-stu-id="b375f-254">Parameter `AtScopeAndBelow` was removed.</span></span>

```powershell

# Old
Get-AzureRmRoleDefinition [other required parameters] -AtScopeAndBelow

# New
Get-AzureRmRoleDefinition [other required parameters]
```

## <a name="breaking-changes-to-azurermstorage-cmdlets"></a><span data-ttu-id="b375f-255">Критически важные изменения в командлетах AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="b375f-255">Breaking changes to AzureRM.Storage cmdlets</span></span>

<span data-ttu-id="b375f-256">**New-AzureRmStorageAccount**</span><span class="sxs-lookup"><span data-stu-id="b375f-256">**New-AzureRmStorageAccount**</span></span>
- <span data-ttu-id="b375f-257">Удален параметр `EnableEncryptionService`.</span><span class="sxs-lookup"><span data-stu-id="b375f-257">The parameter `EnableEncryptionService` was removed</span></span>

<span data-ttu-id="b375f-258">**Set-AzureRmStorageAccount**</span><span class="sxs-lookup"><span data-stu-id="b375f-258">**Set-AzureRmStorageAccount**</span></span>
- <span data-ttu-id="b375f-259">Удалены параметры `EnableEncryptionService` и `DisableEncryptionService`.</span><span class="sxs-lookup"><span data-stu-id="b375f-259">The parameters `EnableEncryptionService` and `DisableEncryptionService` were removed</span></span>

## <a name="removed-modules"></a><span data-ttu-id="b375f-260">Удаленные модули</span><span class="sxs-lookup"><span data-stu-id="b375f-260">Removed modules</span></span>

### `AzureRM.ServerManagement`

<span data-ttu-id="b375f-261">Использование службы "Средства управления серверами" (SMT) [прекращено в прошлом году](https://blogs.technet.microsoft.com/servermanagement/2017/05/17/smt-preview-service-is-being-retired-on-june-30-2017/). Поэтому соответствующий модуль для SMT `AzureRM.ServerManagement` удален из `AzureRM` и в дальнейшем не будет предоставляться.</span><span class="sxs-lookup"><span data-stu-id="b375f-261">The Server Management Tools service was [retired last year](https://blogs.technet.microsoft.com/servermanagement/2017/05/17/smt-preview-service-is-being-retired-on-june-30-2017/), and as a result, the corresponding module for SMT, `AzureRM.ServerManagement`, was removed from `AzureRM` and will stop shipping moving forward.</span></span>

### `AzureRM.SiteRecovery`

<span data-ttu-id="b375f-262">Модуль `AzureRM.SiteRecovery` изменится на `AzureRM.RecoveryServices.SiteRecovery` — функциональное супермножество модуля `AzureRM.SiteRecovery`, содержащее новый набор эквивалентных командлетов.</span><span class="sxs-lookup"><span data-stu-id="b375f-262">The `AzureRM.SiteRecovery` module is being superseded by `AzureRM.RecoveryServices.SiteRecovery`, which is a functional superset of the `AzureRM.SiteRecovery` module and includes a new set of equivalent cmdlets.</span></span> <span data-ttu-id="b375f-263">Полный список сопоставлений старых и новых командлетов см. ниже.</span><span class="sxs-lookup"><span data-stu-id="b375f-263">The full list of mappings from old to new cmdlets can be found below:</span></span>

| <span data-ttu-id="b375f-264">Нерекомендуемые командлеты</span><span class="sxs-lookup"><span data-stu-id="b375f-264">Deprecated cmdlet</span></span>                                        | <span data-ttu-id="b375f-265">Эквивалентные командлеты</span><span class="sxs-lookup"><span data-stu-id="b375f-265">Equivalent cmdlet</span></span>                                                | <span data-ttu-id="b375f-266">Псевдонимы</span><span class="sxs-lookup"><span data-stu-id="b375f-266">Aliases</span></span>                                  |
|----------------------------------------------------------|------------------------------------------------------------------|------------------------------------------|
| `Edit-AzureRmSiteRecoveryRecoveryPlan`                   | `Edit-AzureRmRecoveryServicesAsrRecoveryPlan`                    | `Edit-ASRRecoveryPlan`                   |
| `Get-AzureRmSiteRecoveryFabric`                          | `Get-AzureRmRecoveryServicesAsrFabric`                           | `Get-ASRFabric`                          |
| `Get-AzureRmSiteRecoveryJob`                             | `Get-AzureRmRecoveryServicesAsrJob`                              | `Get-ASRJob`                             |
| `Get-AzureRmSiteRecoveryNetwork`                         | `Get-AzureRmRecoveryServicesAsrNetwork`                          | `Get-ASRNetwork`                         |
| `Get-AzureRmSiteRecoveryNetworkMapping`                  | `Get-AzureRmRecoveryServicesAsrNetworkMapping`                   | `Get-ASRNetworkMapping`                  |
| `Get-AzureRmSiteRecoveryPolicy`                          | `Get-AzureRmRecoveryServicesAsrPolicy`                           | `Get-ASRPolicy`                          |
| `Get-AzureRmSiteRecoveryProtectableItem`                 | `Get-AzureRmRecoveryServicesAsrProtectableItem`                  | `Get-ASRProtectableItem`                 |
| `Get-AzureRmSiteRecoveryProtectionContainer`             | `Get-AzureRmRecoveryServicesAsrProtectionContainer`              | `Get-ASRProtectionContainer`             |
| `Get-AzureRmSiteRecoveryProtectionContainerMapping`      | `Get-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `Get-ASRProtectionContainerMapping`      |
| `Get-AzureRmSiteRecoveryProtectionEntity`                | `Get-AzureRmRecoveryServicesAsrProtectableItem`                  | `Get-ASRProtectableItem`                 |
| `Get-AzureRmSiteRecoveryRecoveryPlan`                    | `Get-AzureRmRecoveryServicesAsrRecoveryPlan`                     | `Get-ASRRecoveryPlan`                    |
| `Get-AzureRmSiteRecoveryRecoveryPoint`                   | `Get-AzureRmRecoveryServicesAsrRecoveryPoint`                    | `Get-ASRRecoveryPoint`                   |
| `Get-AzureRmSiteRecoveryReplicationProtectedItem`        | `Get-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Get-ASRReplicationProtectedItem`        |
| `Get-AzureRmSiteRecoveryServer`                          | `Get-AzureRmRecoveryServicesAsrServicesProvider`                 | `Get-ASRServicesProvider`                |
| `Get-AzureRmSiteRecoveryServicesProvider`                | `Get-AzureRmRecoveryServicesAsrServicesProvider`                 | `Get-ASRServicesProvider`                |
| `Get-AzureRmSiteRecoverySite`                            | `Get-AzureRmRecoveryServicesAsrFabric`                           | `Get-ASRFabric`                          |
| `Get-AzureRmSiteRecoveryStorageClassification`           | `Get-AzureRmRecoveryServicesAsrStorageClassification`            | `Get-ASRStorageClassification`           |
| `Get-AzureRmSiteRecoveryStorageClassificationMapping`    | `Get-AzureRmRecoveryServicesAsrStorageClassificationMapping`     | `Get-ASRStorageClassificationMapping`    |
| `Get-AzureRmSiteRecoveryVault`                           | `Get-AzureRmRecoveryServicesVault`                               |                                          |
| `Get-AzureRmSiteRecoveryVaultSettings`                   | `Get-AzureRmRecoveryServicesAsrVaultContext`                     |                                          |
| `Get-AzureRmSiteRecoveryVaultSettingsFile`               | `Get-AzureRmRecoveryServicesVaultSettingsFile`                   |                                          |
| `Get-AzureRmSiteRecoveryVM`                              | `Get-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Get-ASRReplicationProtectedItem`        |
| `Import-AzureRmSiteRecoveryVaultSettingsFile`            | `Import-AzureRmRecoveryServicesAsrVaultSettingsFile`             |                                          |
| `New-AzureRmSiteRecoveryFabric`                          | `New-AzureRmRecoveryServicesAsrFabric`                           | `New-ASRFabric`                          |
| `New-AzureRmSiteRecoveryNetworkMapping`                  | `New-AzureRmRecoveryServicesAsrNetworkMapping`                   | `New-ASRNetworkMapping`                  |
| `New-AzureRmSiteRecoveryPolicy`                          | `New-AzureRmRecoveryServicesAsrPolicy`                           | `New-ASRPolicy`                          |
| `New-AzureRmSiteRecoveryProtectionContainerMapping`      | `New-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `New-ASRProtectionContainerMapping`      |
| `New-AzureRmSiteRecoveryRecoveryPlan`                    | `New-AzureRmRecoveryServicesAsrRecoveryPlan`                     | `New-ASRRecoveryPlan`                    |
| `New-AzureRmSiteRecoveryReplicationProtectedItem`        | `New-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `New-ASRReplicationProtectedItem`        |
| `New-AzureRmSiteRecoverySite`                            | `New-AzureRmRecoveryServicesAsrFabric`                           | `New-ASRFabric`                          |
| `New-AzureRmSiteRecoveryStorageClassificationMapping`    | `New-AzureRmRecoveryServicesAsrStorageClassificationMapping`     | `New-ASRStorageClassificationMapping`    |
| `New-AzureRmSiteRecoveryVault`                           | `New-AzureRmRecoveryServicesVault`                               |                                          |
| `Remove-AzureRmSiteRecoveryFabric`                       | `Remove-AzureRmRecoveryServicesAsrFabric`                        | `Remove-ASRFabric`                       |
| `Remove-AzureRmSiteRecoveryNetworkMapping`               | `Remove-AzureRmRecoveryServicesAsrNetworkMapping`                | `Remove-ASRNetworkMapping`               |
| `Remove-AzureRmSiteRecoveryPolicy`                       | `Remove-AzureRmRecoveryServicesAsrPolicy`                        | `Remove-ASRPolicy`                       |
| `Remove-AzureRmSiteRecoveryProtectionContainerMapping`   | `Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping`    | `Remove-ASRProtectionContainerMapping`   |
| `Remove-AzureRmSiteRecoveryRecoveryPlan`                 | `Remove-AzureRmRecoveryServicesAsrRecoveryPlan`                  | `Remove-ASRRecoveryPlan`                 |
| `Remove-AzureRmSiteRecoveryReplicationProtectedItem`     | `Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem`      | `Remove-ASRReplicationProtectedItem`     |
| `Remove-AzureRmSiteRecoveryServer`                       | `Remove-AzureRmRecoveryServicesAsrServicesProvider`              |                                          |
| `Remove-AzureRmSiteRecoveryServicesProvider`             | `Remove-AzureRmRecoveryServicesAsrServicesProvider`              | `Remove-ASRServicesProvider`             |
| `Remove-AzureRmSiteRecoverySite`                         | `Remove-AzureRmRecoveryServicesAsrFabric`                        | `Remove-ASRFabric`                       |
| `Remove-AzureRmSiteRecoveryStorageClassificationMapping` | `Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping`  | `Remove-ASRStorageClassificationMapping` |
| `Remove-AzureRmSiteRecoveryVault`                        | `Remove-AzureRmRecoveryServicesVault`                            |                                          |
| `Restart-AzureRmSiteRecoveryJob`                         | `Restart-AzureRmRecoveryServicesAsrJob`                          | `Restart-ASRJob`                         |
| `Resume-AzureRmSiteRecoveryJob`                          | `Resume-AzureRmRecoveryServicesAsrJob`                           | `Resume-ASRJob`                          |
| `Set-AzureRmSiteRecoveryProtectionEntity`                | `New-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `New-ASRReplicationProtectedItem`        |
| `Set-AzureRmSiteRecoveryReplicationProtectedItem`        | `Set-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Set-ASRReplicationProtectedItem`        |
| `Set-AzureRmSiteRecoveryVaultSettings`                   | `Set-AzureRmRecoveryServicesAsrVaultContext`                     | `Set-ASRVaultContext`                    |
| `Set-AzureRmSiteRecoveryVM`                              | `Set-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Set-ASRReplicationProtectedItem`        |
| `Start-AzureRmSiteRecoveryApplyRecoveryPoint`            | `Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint`             | `Start-ASRApplyRecoveryPoint`            |
| `Start-AzureRmSiteRecoveryCommitFailoverJob`             | `Start-AzureRmRecoveryServicesAsrCommitFailoverJob`              | `Start-ASRCommitFailoverJob`             |
| `Start-AzureRmSiteRecoveryPlannedFailoverJob`            | `Start-AzureRmRecoveryServicesAsrPlannedFailoverJob`             | `Start-ASRPlannedFailoverJob`            |
| `Start-AzureRmSiteRecoveryPolicyAssociationJob`          | `New-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `New-ASRProtectionContainerMapping`      |
| `Start-AzureRmSiteRecoveryPolicyDissociationJob`         | `Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping`    | `Remove-ASRProtectionContainerMapping`   |
| `Start-AzureRmSiteRecoveryTestFailoverJob`               | `Start-AzureRmRecoveryServicesAsrTestFailoverJob`                | `Start-ASRTestFailoverJob`               |
| `Start-AzureRmSiteRecoveryUnplannedFailoverJob`          | `Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob`           | `Start-ASRUnplannedFailoverJob`          |
| `Stop-AzureRmSiteRecoveryJob`                            | `Stop-AzureRmRecoveryServicesAsrJob`                             | `Stop-ASRJob`                            |
| `Update-AzureRmSiteRecoveryPolicy`                       | `Update-AzureRmRecoveryServicesAsrPolicy`                        | `Update-ASRPolicy`                       |
| `Update-AzureRmSiteRecoveryProtectionDirection`          | `Update-AzureRmRecoveryServicesAsrProtectionDirection`           | `Update-ASRProtectionDirection`          |
| `Update-AzureRmSiteRecoveryRecoveryPlan`                 | `Update-AzureRmRecoveryServicesAsrRecoveryPlan`                  | `Update-ASRRecoveryPlan`                 |
| `Update-AzureRmSiteRecoveryServer`                       | `Update-AzureRmRecoveryServicesAsrServicesProvider`              | `Update-ASRServicesProvider`             |
| `Update-AzureRmSiteRecoveryServicesProvider`             | `Update-AzureRmRecoveryServicesAsrvCenter`                       | `Update-ASRvCenter`                      |