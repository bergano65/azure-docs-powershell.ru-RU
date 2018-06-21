---
title: Журнал изменений Azure PowerShell | Документация Майкрософт
description: Это руководство содержит историю изменений Azure PowerShell, внесенных в новом выпуске.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 8515a267e80e5d1f7bb97557efa72b9e86b7b45d
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/08/2018
ms.locfileid: "33912009"
---
# <a name="release-notes"></a><span data-ttu-id="08042-103">Заметки о выпуске</span><span class="sxs-lookup"><span data-stu-id="08042-103">Release notes</span></span>

<span data-ttu-id="08042-104">Здесь приведен список изменений, внесенных в Azure PowerShell в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="08042-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---

## <a name="600---may-2018"></a><span data-ttu-id="08042-105">6.0.0 — май 2018 г.</span><span class="sxs-lookup"><span data-stu-id="08042-105">6.0.0 - May 2018</span></span>

### <a name="general"></a><span data-ttu-id="08042-106">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="08042-106">General</span></span>
* <span data-ttu-id="08042-107">Минимальная версия зависимости от модулей повышена до PowerShell 5.0.</span><span class="sxs-lookup"><span data-stu-id="08042-107">Set minimum dependency of modules to PowerShell 5.0</span></span>

### <a name="azurestorage"></a><span data-ttu-id="08042-108">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="08042-108">Azure.Storage</span></span>
* <span data-ttu-id="08042-109">Добавлена поддержка имени контейнера хранилища BLOB-объектов:</span><span class="sxs-lookup"><span data-stu-id="08042-109">Support  as Storage blob container name</span></span>
    - <span data-ttu-id="08042-110">New-AzureStorageBlobContainer;</span><span class="sxs-lookup"><span data-stu-id="08042-110">New-AzureStorageBlobContainer</span></span>
    - <span data-ttu-id="08042-111">Remove-AzureStorageBlobContainer;</span><span class="sxs-lookup"><span data-stu-id="08042-111">Remove-AzureStorageBlobContainer</span></span>
    - <span data-ttu-id="08042-112">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="08042-112">Set-AzureStorageBlobContent</span></span>
    - <span data-ttu-id="08042-113">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="08042-113">Get-AzureStorageBlobContent</span></span>
* <span data-ttu-id="08042-114">Исправлена проблема, из-за которой в выходных данных командлетов службы хранилища, которые завершались ошибкой, отсутствовали подробные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="08042-114">Fix the issue that some Storage cmdlets failure output not contain detail failure information</span></span>

### <a name="azurermapimanagement"></a><span data-ttu-id="08042-115">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="08042-115">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="08042-116">Представлено много критически важных изменений.</span><span class="sxs-lookup"><span data-stu-id="08042-116">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="08042-117">Дополнительные сведения см. в руководстве по миграции.</span><span class="sxs-lookup"><span data-stu-id="08042-117">Please refer to the migration guide for more information</span></span>

### <a name="azurermautomation"></a><span data-ttu-id="08042-118">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="08042-118">AzureRM.Automation</span></span>
* <span data-ttu-id="08042-119">Из следующих командлетов удален нерекомендуемый псевдоним Tags:</span><span class="sxs-lookup"><span data-stu-id="08042-119">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="08042-120">Set-AzureRmAutomationRunbook.</span><span class="sxs-lookup"><span data-stu-id="08042-120">'Set-AzureRmAutomationRunbook'</span></span>

### <a name="azurermbatch"></a><span data-ttu-id="08042-121">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="08042-121">AzureRM.Batch</span></span>
* <span data-ttu-id="08042-122">В документации по New-AzureBatchPool удален нерекомендуемый пример.</span><span class="sxs-lookup"><span data-stu-id="08042-122">Updated New-AzureBatchPool documentation to remove deprecated example</span></span>

### <a name="azurermcdn"></a><span data-ttu-id="08042-123">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="08042-123">AzureRM.Cdn</span></span>
* <span data-ttu-id="08042-124">Представлено много критически важных изменений.</span><span class="sxs-lookup"><span data-stu-id="08042-124">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="08042-125">Дополнительные сведения см. в руководстве по миграции.</span><span class="sxs-lookup"><span data-stu-id="08042-125">Please refer to the migration guide for more information</span></span>

### <a name="azurermcompute"></a><span data-ttu-id="08042-126">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="08042-126">AzureRM.Compute</span></span>
* <span data-ttu-id="08042-127">New-AzureRmVm и New-AzureRmVmss поддерживают подробные выходные данные параметров.</span><span class="sxs-lookup"><span data-stu-id="08042-127">'New-AzureRmVm' and 'New-AzureRmVmss' support verbose output of parameters</span></span>
* <span data-ttu-id="08042-128">New-AzureRmVm и New-AzureRmVmss (простой набор параметров) поддерживают назначение виртуальной машине определяемых пользователем и (или) определяемые системой удостоверений.</span><span class="sxs-lookup"><span data-stu-id="08042-128">'New-AzureRmVm' and 'New-AzureRmVmss' (simple parameter set) support assigning user defined and(or) system defined identities to the VM(s).</span></span>
* <span data-ttu-id="08042-129">В масштабируемый набор виртуальных машин добавлены функции Redeploy и PerformMaintenance.</span><span class="sxs-lookup"><span data-stu-id="08042-129">VMSS Redeploy and PerformMaintenance feature</span></span>
    -  <span data-ttu-id="08042-130">В Set-AzureRmVmss и Set-AzureRmVmssVM добавлены новые параметры-переключатели -Redeploy и -PerformMaintenance.</span><span class="sxs-lookup"><span data-stu-id="08042-130">Add new switch parameter -Redeploy and -PerformMaintenance to 'Set-AzureRmVmss' and 'Set-AzureRmVmssVM'</span></span>
* <span data-ttu-id="08042-131">В командлет Set-AzureRmVMOperatingSystem добавлен параметр-переключатель DisableVMAgent.</span><span class="sxs-lookup"><span data-stu-id="08042-131">Add DisableVMAgent switch parameter to 'Set-AzureRmVMOperatingSystem' cmdlet</span></span>
* <span data-ttu-id="08042-132">В New-AzureRmVm и New-AzureRmVmss (простой набор параметров) добавлена поддержка образа Win10.</span><span class="sxs-lookup"><span data-stu-id="08042-132">'New-AzureRmVm' and 'New-AzureRmVmss' (simple parameter set) support a 'Win10' image.</span></span>
* <span data-ttu-id="08042-133">Добавлен командлет Repair-AzureRmVmssServiceFabricUpdateDomain.</span><span class="sxs-lookup"><span data-stu-id="08042-133">'Repair-AzureRmVmssServiceFabricUpdateDomain' cmdlet is added.</span></span>
* <span data-ttu-id="08042-134">Представлено много критически важных изменений.</span><span class="sxs-lookup"><span data-stu-id="08042-134">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="08042-135">Дополнительные сведения см. в руководстве по миграции.</span><span class="sxs-lookup"><span data-stu-id="08042-135">Please refer to the migration guide for more details</span></span>
* <span data-ttu-id="08042-136">Для Set-AzureRmVmDiskEncryptionExtension параметры AAD стали необязательными.</span><span class="sxs-lookup"><span data-stu-id="08042-136">'Set-AzureRmVmDiskEncryptionExtension' makes AAD parameters optional</span></span>

### <a name="azurermdatafactories"></a><span data-ttu-id="08042-137">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="08042-137">AzureRM.DataFactories</span></span>
* <span data-ttu-id="08042-138">Из следующих командлетов удален нерекомендуемый псевдоним Tags:</span><span class="sxs-lookup"><span data-stu-id="08042-138">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="08042-139">New-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="08042-139">New-AzureRmDataFactory</span></span>

### <a name="azurermdatafactoryv2"></a><span data-ttu-id="08042-140">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="08042-140">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="08042-141">Обновлен пакет .Net SDK для ADF до версии 0.7.0-preview, содержащий следующие изменения:</span><span class="sxs-lookup"><span data-stu-id="08042-141">Updated the ADF .Net SDK version to 0.7.0-preview containing following changes:</span></span>
    - <span data-ttu-id="08042-142">Для действия ExecuteSSISPackage добавлены параметры выполнения и свойство диспетчера подключений.</span><span class="sxs-lookup"><span data-stu-id="08042-142">Added execution parameters and connection managers property on ExecuteSSISPackage Activity</span></span>
    - <span data-ttu-id="08042-143">Обновлены связанные службы PostgreSql и MySql для использования всей строки подключения вместо параметров сервера, базы данных, схемы, имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="08042-143">Updated PostgreSql, MySql llinked service to use full connection string instead of server, database, schema, username and password</span></span>
    - <span data-ttu-id="08042-144">Из связанной службы DB2 удалена схема.</span><span class="sxs-lookup"><span data-stu-id="08042-144">Removed the schema from DB2 linked service</span></span>
    - <span data-ttu-id="08042-145">Из связанной службы Teradata удалено свойство схемы.</span><span class="sxs-lookup"><span data-stu-id="08042-145">Removed schema property from Teradata linked service</span></span>
    - <span data-ttu-id="08042-146">Для Responsys добавлены параметры LinkedService, Dataset, CopySource.</span><span class="sxs-lookup"><span data-stu-id="08042-146">Added LinkedService, Dataset, CopySource for Responsys</span></span>

### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="08042-147">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="08042-147">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="08042-148">Из следующих командлетов удален нерекомендуемый псевдоним Tags:</span><span class="sxs-lookup"><span data-stu-id="08042-148">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="08042-149">New-AzureRmDataLakeAnalyticsAccount;</span><span class="sxs-lookup"><span data-stu-id="08042-149">'New-AzureRmDataLakeAnalyticsAccount'</span></span>
    - <span data-ttu-id="08042-150">Set-AzureRmDataLakeAnalyticsAccount.</span><span class="sxs-lookup"><span data-stu-id="08042-150">'Set-AzureRmDataLakeAnalyticsAccount'</span></span>

### <a name="azurermdatalakestore"></a><span data-ttu-id="08042-151">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="08042-151">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="08042-152">Добавлена новая функция рекурсивного изменения списка ACL в командлеты Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAclEntry и Set-AzureRmDataLakeStoreItemAcl.</span><span class="sxs-lookup"><span data-stu-id="08042-152">Add new feature of recursive Acl Change to Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="08042-153">Добавлен новый командлет для получения сводки по содержимому в каталоге.</span><span class="sxs-lookup"><span data-stu-id="08042-153">Add new cmdlet for retrieving the content summary under a directory</span></span>
* <span data-ttu-id="08042-154">Добавлен новый командлет для получения дампа ACL и сведений об использовании диска.</span><span class="sxs-lookup"><span data-stu-id="08042-154">Add new cmdlet for retrieving the disk usage and Acl dump</span></span>
* <span data-ttu-id="08042-155">Исправлен тип возвращаемого значения Set-AzureRmDataLakeStoreItemAcl с логического на IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="08042-155">Correct return type of Set-AzureRmDataLakeStoreItemAcl bool to IEnumerable<DataLakeStoreItemAce></span></span>
* <span data-ttu-id="08042-156">Исправлен тип возвращаемого значения Set-AzureRmDataLakeStoreItemAclEntry с логического на IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="08042-156">Correct return type of Set-AzureRmDataLakeStoreItemAclEntry bool to IEnumerable<DataLakeStoreItemAce></span></span>
* <span data-ttu-id="08042-157">В командлеты Export-AzureRmDataLakeStoreItem, Import-AzureRmDataLakeStoreItem, Remove-AzureRmDataLakeStoreItem внесены критически важные изменения.</span><span class="sxs-lookup"><span data-stu-id="08042-157">Breaking changes in Export-AzureRmDataLakeStoreItem, Import-AzureRmDataLakeStoreItem, Remove-AzureRmDataLakeStoreItem</span></span>

### <a name="azurermdns"></a><span data-ttu-id="08042-158">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="08042-158">AzureRM.Dns</span></span>
* <span data-ttu-id="08042-159">Представлено много критически важных изменений.</span><span class="sxs-lookup"><span data-stu-id="08042-159">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="08042-160">Дополнительные сведения см. в руководстве по миграции.</span><span class="sxs-lookup"><span data-stu-id="08042-160">Please refer to the migration guide for more information</span></span>

### <a name="azurermeventhub"></a><span data-ttu-id="08042-161">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="08042-161">AzureRM.EventHub</span></span>
* <span data-ttu-id="08042-162">В справку добавлены отсутствующие ранее примеры для командлетов.</span><span class="sxs-lookup"><span data-stu-id="08042-162">Updated Help for cmdlets with missing examples</span></span>

### <a name="azurerminsights"></a><span data-ttu-id="08042-163">AzureRM.Insights;</span><span class="sxs-lookup"><span data-stu-id="08042-163">AzureRM.Insights</span></span>
* <span data-ttu-id="08042-164">Представлено много критически важных изменений.</span><span class="sxs-lookup"><span data-stu-id="08042-164">Introduced multiple breaking changes</span></span>
    - <span data-ttu-id="08042-165">Дополнительные сведения см. в руководстве по миграции.</span><span class="sxs-lookup"><span data-stu-id="08042-165">Please refer to the migration guide for more information</span></span>

### <a name="azurermiothub"></a><span data-ttu-id="08042-166">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="08042-166">AzureRM.IotHub</span></span>
* <span data-ttu-id="08042-167">Для IotHub включены теги и SKU "Базовый".</span><span class="sxs-lookup"><span data-stu-id="08042-167">Enable tags and Basic Sku to the IotHub</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="08042-168">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="08042-168">AzureRM.KeyVault</span></span>
* <span data-ttu-id="08042-169">Внесены критически важные изменения для поддержки конвейерного режима.</span><span class="sxs-lookup"><span data-stu-id="08042-169">Breaking changes to support piping scenarios</span></span>
* <span data-ttu-id="08042-170">Добавлены новые командлеты: Backup/Restore-AzureKeyVaultManagedStorageAccount, Backup/Restore-AzureKeyVaultCertificate, Undo-AzureKeyVaultManagedStorageSasDefinitionRemoval и Undo-AzureKeyVaultManagedStorageAccountRemoval.</span><span class="sxs-lookup"><span data-stu-id="08042-170">Added new cmdlets: Backup/Restore-AzureKeyVaultManagedStorageAccount, Backup/Restore-AzureKeyVaultCertificate, Undo-AzureKeyVaultManagedStorageSasDefinitionRemoval, and Undo-AzureKeyVaultManagedStorageAccountRemoval</span></span>

### <a name="azurermmachinelearning"></a><span data-ttu-id="08042-171">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="08042-171">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="08042-172">Из следующих командлетов удален нерекомендуемый псевдоним Tags:</span><span class="sxs-lookup"><span data-stu-id="08042-172">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="08042-173">Update-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="08042-173">Update-AzureRmMlCommitmentPlan</span></span>

### <a name="azurermmedia"></a><span data-ttu-id="08042-174">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="08042-174">AzureRM.Media</span></span>
* <span data-ttu-id="08042-175">Из следующих командлетов удален нерекомендуемый псевдоним Tags:</span><span class="sxs-lookup"><span data-stu-id="08042-175">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="08042-176">Set-AzureRmMediaService.</span><span class="sxs-lookup"><span data-stu-id="08042-176">'Set-AzureRmMediaService'</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="08042-177">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="08042-177">AzureRM.Network</span></span>
* <span data-ttu-id="08042-178">Добавлена поддержка ресурса плана защиты от атак DDoS.</span><span class="sxs-lookup"><span data-stu-id="08042-178">Add support for DDoS protection plan resource</span></span>
* <span data-ttu-id="08042-179">Представлено много критически важных изменений.</span><span class="sxs-lookup"><span data-stu-id="08042-179">Introduced multiple breaking changes</span></span>
    - <span data-ttu-id="08042-180">Дополнительные сведения см. в руководстве по миграции.</span><span class="sxs-lookup"><span data-stu-id="08042-180">Please refer to the migration guide for more information</span></span>

### <a name="azurermnotificationhubs"></a><span data-ttu-id="08042-181">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="08042-181">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="08042-182">Представлено много критически важных изменений.</span><span class="sxs-lookup"><span data-stu-id="08042-182">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="08042-183">Дополнительные сведения см. в руководстве по миграции.</span><span class="sxs-lookup"><span data-stu-id="08042-183">Please refer to the migration guide for more information</span></span>

### <a name="azurermoperationalinsights"></a><span data-ttu-id="08042-184">AzureRM.OperationalInsights;</span><span class="sxs-lookup"><span data-stu-id="08042-184">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="08042-185">Представлено много критически важных изменений.</span><span class="sxs-lookup"><span data-stu-id="08042-185">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="08042-186">Дополнительные сведения см. в руководстве по миграции.</span><span class="sxs-lookup"><span data-stu-id="08042-186">Please refer to the migration guide for more information</span></span>

### <a name="azurermprofile"></a><span data-ttu-id="08042-187">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="08042-187">AzureRM.Profile</span></span>
* <span data-ttu-id="08042-188">Автосохранение контекста включено по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="08042-188">Enable context autosave by default</span></span>
* <span data-ttu-id="08042-189">В среде Azure для государственных организаций США добавлены свойства USGovernmentOperationalInsightsEndpoint и USGovernmentOperationalInsightsEndpointResourceId.</span><span class="sxs-lookup"><span data-stu-id="08042-189">Add USGovernmentOperationalInsightsEndpoint and USGovernmentOperationalInsightsEndpointResourceId properties to Azure environment for US Gov.</span></span>

### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="08042-190">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="08042-190">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="08042-191">Исправлен заголовок аутентификации в сценариях SiteRecovery.</span><span class="sxs-lookup"><span data-stu-id="08042-191">Fixed Authentication Header in SiteRecovery scenarios</span></span>

### <a name="azurermrediscache"></a><span data-ttu-id="08042-192">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="08042-192">AzureRM.RedisCache</span></span>
* <span data-ttu-id="08042-193">Представлено много критически важных изменений.</span><span class="sxs-lookup"><span data-stu-id="08042-193">Introduced multiple breaking changes</span></span>
    - <span data-ttu-id="08042-194">Дополнительные сведения см. в руководстве по миграции.</span><span class="sxs-lookup"><span data-stu-id="08042-194">Please refer to the migration guide for more information</span></span>

### <a name="azurermresources"></a><span data-ttu-id="08042-195">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="08042-195">AzureRM.Resources</span></span>
* <span data-ttu-id="08042-196">Удален устаревший параметр -AtScopeAndBelow из вызова Get-AzureRmRoledefinition.</span><span class="sxs-lookup"><span data-stu-id="08042-196">Remove obsolete parameter -AtScopeAndBelow from Get-AzureRmRoledefinition call</span></span>
* <span data-ttu-id="08042-197">В результаты Get-AzureRmRoleAssignment добавлены данные о назначениях для удаленных элементов USers, Groups и ServicePrincipals.</span><span class="sxs-lookup"><span data-stu-id="08042-197">Include assignments to deleted USers/Groups/ServicePrincipals in Get-AzureRmRoleAssignment result</span></span>
* <span data-ttu-id="08042-198">Добавлены средства заполнения вкладок для Scope и ResourceType.</span><span class="sxs-lookup"><span data-stu-id="08042-198">Add Tab completers for Scope and ResourceType</span></span>
* <span data-ttu-id="08042-199">Добавлен вспомогательный командлет для создания субъектов служб.</span><span class="sxs-lookup"><span data-stu-id="08042-199">Add convenience cmdlet for creating ServicePrincipals</span></span>
* <span data-ttu-id="08042-200">Функции Get - и -Find объединены в Get-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="08042-200">Merge Get- and Find- functionality in Get-AzureRmResource</span></span>
* <span data-ttu-id="08042-201">Добавлены командлеты Active Directory:</span><span class="sxs-lookup"><span data-stu-id="08042-201">Add AD Cmdlets:</span></span>
  - <span data-ttu-id="08042-202">Remove-AzureRmADGroupMember;</span><span class="sxs-lookup"><span data-stu-id="08042-202">Remove-AzureRmADGroupMember</span></span>
  - <span data-ttu-id="08042-203">Get-AzureRmADGroup;</span><span class="sxs-lookup"><span data-stu-id="08042-203">Get-AzureRmADGroup</span></span>
  - <span data-ttu-id="08042-204">New-AzureRmADGroup;</span><span class="sxs-lookup"><span data-stu-id="08042-204">New-AzureRmADGroup</span></span>
  - <span data-ttu-id="08042-205">Remove-AzureRmADGroup;</span><span class="sxs-lookup"><span data-stu-id="08042-205">Remove-AzureRmADGroup</span></span>
  - <span data-ttu-id="08042-206">Remove-AzureRmADUser;</span><span class="sxs-lookup"><span data-stu-id="08042-206">Remove-AzureRmADUser</span></span>
  - <span data-ttu-id="08042-207">Update-AzureRmADApplication;</span><span class="sxs-lookup"><span data-stu-id="08042-207">Update-AzureRmADApplication</span></span>
  - <span data-ttu-id="08042-208">Update-AzureRmADServicePrincipal;</span><span class="sxs-lookup"><span data-stu-id="08042-208">Update-AzureRmADServicePrincipal</span></span>
  - <span data-ttu-id="08042-209">Update-AzureRmADUser.</span><span class="sxs-lookup"><span data-stu-id="08042-209">Update-AzureRmADUser</span></span>

### <a name="azurermservicefabric"></a><span data-ttu-id="08042-210">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="08042-210">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="08042-211">Обновлен используемый по умолчанию SKU версии образа Linux.</span><span class="sxs-lookup"><span data-stu-id="08042-211">Update default Linux image version sku</span></span>
  - <span data-ttu-id="08042-212">NewAzureServiceFabricCluster.cs default UbuntuServer1604 Sku update</span><span class="sxs-lookup"><span data-stu-id="08042-212">NewAzureServiceFabricCluster.cs default UbuntuServer1604 Sku update</span></span>

### <a name="azurermstorage"></a><span data-ttu-id="08042-213">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="08042-213">AzureRM.Storage</span></span>
* <span data-ttu-id="08042-214">Представлено много критически важных изменений.</span><span class="sxs-lookup"><span data-stu-id="08042-214">Introduced multiple breaking changes</span></span>
    - <span data-ttu-id="08042-215">Дополнительные сведения см. в руководстве по миграции.</span><span class="sxs-lookup"><span data-stu-id="08042-215">Please refer to the migration guide for more information</span></span>

### <a name="azurermwebsites"></a><span data-ttu-id="08042-216">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="08042-216">AzureRM.Websites</span></span>
* <span data-ttu-id="08042-217">Пакет SDK для веб-сайтов обновлен до последней версии.</span><span class="sxs-lookup"><span data-stu-id="08042-217">Upgrade to latest version of the Websites SDK</span></span>
* <span data-ttu-id="08042-218">Для Set-AzureRmWebApp и Set-AzureRmWebAppSlot добавлены свойства -AssignIdentity и -Httpsonly.</span><span class="sxs-lookup"><span data-stu-id="08042-218">Added -AssignIdentity & -Httpsonly properties for Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
* <span data-ttu-id="08042-219">Добавлены два новых командлета: Get-AzureRmWebAppSnapshots и Restore-AzureRmWebAppSnapshot.</span><span class="sxs-lookup"><span data-stu-id="08042-219">Added two new cmdlets: Get-AzureRmWebAppSnapshots and Restore-AzureRmWebAppSnapshot</span></span>
