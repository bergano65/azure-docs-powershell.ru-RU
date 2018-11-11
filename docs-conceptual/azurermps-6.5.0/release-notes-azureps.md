---
title: Журнал изменений Azure PowerShell | Документация Майкрософт
description: Это руководство содержит историю изменений Azure PowerShell, внесенных в новом выпуске.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: e9fa2d75c1c4e6ffaa2f7dd8e400f5b13dd4527d
ms.sourcegitcommit: 8b882d1c27d9e323447ff85f56d11bbf5e244d7f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2018
ms.locfileid: "39110489"
---
# <a name="release-notes"></a><span data-ttu-id="6b1f7-103">Заметки о выпуске</span><span class="sxs-lookup"><span data-stu-id="6b1f7-103">Release notes</span></span>

<span data-ttu-id="6b1f7-104">Здесь приведен список изменений, внесенных в Azure PowerShell в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="650---july-2018"></a><span data-ttu-id="6b1f7-105">6.5.0 — июль 2018 г.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-105">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="6b1f7-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6b1f7-106">AzureRM.Profile</span></span>
* <span data-ttu-id="6b1f7-107">Обновлена справка для командлета Get-AzureRmContextAutosaveSetting.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-107">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="6b1f7-108">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="6b1f7-108">Azure.Storage</span></span>
* <span data-ttu-id="6b1f7-109">Добавлена поддержка отправки BLOB-объекта или файла с помощью токена SAS, доступного только для записи.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-109">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="6b1f7-110">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6b1f7-110">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="6b1f7-111">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6b1f7-111">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="6b1f7-112">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6b1f7-112">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="6b1f7-113">Для AS добавлено обязательное свойство ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-113">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="6b1f7-114">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="6b1f7-114">AzureRM.Automation</span></span>
* <span data-ttu-id="6b1f7-115">Обновлена справка и добавлены примеры для командлета New-AzureRMAutomationSchedule.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-115">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6b1f7-116">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6b1f7-116">AzureRM.Compute</span></span>
* <span data-ttu-id="6b1f7-117">Добавлен параметр -Tag для командлета Update/New-AzureRmAvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-117">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="6b1f7-118">Добавлен пример для командлета Add-AzureRmVmssExtension.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-118">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="6b1f7-119">Добавлены примеры для командлета Remove-AzureRmVmssExtension.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-119">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="6b1f7-120">Обновлена справка для командлета Set-AzureRmVMAccessExtension.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-120">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="6b1f7-121">Изменен класс SimpleParameterSet для командлета New-AzureRmVmss: теперь для SinglePlacementGroup по умолчанию задается значение false, а также добавляется параметр-переключатель SinglePlacementGroup, который позволяет пользователю создать VMSS в одной группе размещения.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-121">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="6b1f7-122">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="6b1f7-122">AzureRM.EventHub</span></span>
* <span data-ttu-id="6b1f7-123">В класс PSEventHubDRConfigurationAttributes добавлено доступное только для чтения свойство PendingReplicationOperationsCount, которое показывает количество ожидающих репликации операций во время реплицирования.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-123">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="6b1f7-124">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6b1f7-124">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6b1f7-125">Обновлено сообщение об ошибке для командлета Set-AzureRmKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-125">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="6b1f7-126">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6b1f7-126">AzureRM.LogicApp</span></span>
* <span data-ttu-id="6b1f7-127">Исправлена ошибка "parameter set could not be resolved" (не удалось разрешить заданный параметр) в командлете New-AzureRmLogicApp.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-127">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="6b1f7-128">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6b1f7-128">AzureRM.Network</span></span>
* <span data-ttu-id="6b1f7-129">Включен пиринг между виртуальными сетями в нескольких клиентах для командлета Set/Add-AzureRmVirtualNetworkPeering.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-129">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="6b1f7-130">Для шлюза приложений обновлены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="6b1f7-130">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="6b1f7-131">New-AzureRmApplicationGateway: добавлены флаг EnableFIPS и поддержка зон.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-131">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="6b1f7-132">New-AzureRmApplicationGatewaySku: добавлены новые номера SKU Standard_v2 и WAF_v2.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-132">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="6b1f7-133">Set-AzureRmApplicationGatewaySku: добавлены новые номера SKU Standard_v2 и WAF_v2.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-133">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="6b1f7-134">Командлеты RouteTable пересозданы в последней версии генератора.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-134">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="6b1f7-135">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="6b1f7-135">AzureRM.Relay</span></span>
* <span data-ttu-id="6b1f7-136">Обновлены файлы Markdown, исправлена проблема с именем параметра в примере.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-136">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="6b1f7-137">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6b1f7-137">AzureRM.Resources</span></span>
* <span data-ttu-id="6b1f7-138">Обновлены командлеты Roleassignment и roledefinition:</span><span class="sxs-lookup"><span data-stu-id="6b1f7-138">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="6b1f7-139">Удалены лишние вызовы roledefinition, выполняемые в ходе разбиения на страницы.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-139">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="6b1f7-140">Исправлен командлет Get-AzureRmRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-140">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="6b1f7-141">Исправлена работа параметра -ExpandPrincipalGroups.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-141">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="6b1f7-142">Устранена проблема в командлете Get-AzureRmResource, заключающая в том, что в параметре -ResourceType учитывался регистр символов.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-142">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="6b1f7-143">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6b1f7-143">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="6b1f7-144">Добавлены параметры top и skip для командлетов list.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-144">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="6b1f7-145">Добавлены командлеты для перехода с пространства имен ценовой категории "Стандартный" на пространство ценовой категории "Премиум":</span><span class="sxs-lookup"><span data-stu-id="6b1f7-145">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="6b1f7-146">Start-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="6b1f7-146">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="6b1f7-147">Get-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="6b1f7-147">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="6b1f7-148">Complete-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="6b1f7-148">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="6b1f7-149">Stop-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="6b1f7-149">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="6b1f7-150">Remove-AzureRmServiceBusMigration.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-150">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="6b1f7-151">В класс PSServiceBusDRConfigurationAttributes добавлено доступное только для чтения свойство PendingReplicationOperationsCount, которое показывает количество ожидающих репликации операций во время реплицирования.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-151">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="6b1f7-152">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6b1f7-152">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="6b1f7-153">Обновлен пример для командлета New-AzureRmServiceFabricCluster.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-153">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="6b1f7-154">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6b1f7-154">AzureRM.Sql</span></span>
* <span data-ttu-id="6b1f7-155">Добавлены новые командлеты для Management.Sql, позволяющие клиентам добавлять сертификат TDE в экземпляр SQL Server или управляемый экземпляр:</span><span class="sxs-lookup"><span data-stu-id="6b1f7-155">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="6b1f7-156">Add-AzureRmSqlServerTransparentDataEncryptionCertificate;</span><span class="sxs-lookup"><span data-stu-id="6b1f7-156">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="6b1f7-157">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-157">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="6b1f7-158">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="6b1f7-158">AzureRM.Websites</span></span>
* <span data-ttu-id="6b1f7-159">`Set-AzureRmWebApp -AssignIdentity` и `Set-AzureRmWebAppSlot -AssignIdentity` при установленном значении false теперь будут удалять свойство Identity из объекта сайта. Также при этом будет удаляться тег предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-159">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="6b1f7-160">Обновлен пример для `Get-AzureRmWebAppMetrics` и `Get-AzureRmAppServicePlanMetrics`.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-160">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="6b1f7-161">`Set-AzureRmWebApp -PhpVersion` теперь поддерживает off как допустимую версию PHP.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-161">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="6b1f7-162">6.4.0 — июль 2018 г.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-162">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="6b1f7-163">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="6b1f7-163">General</span></span>
* <span data-ttu-id="6b1f7-164">Исправлено форматирование OutputType в файлах справки для большинства модулей.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-164">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="6b1f7-165">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6b1f7-165">AzureRM.Profile</span></span>
* <span data-ttu-id="6b1f7-166">В основные типы выходных данных добавлен атрибут Ps1Xml.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-166">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6b1f7-167">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6b1f7-167">AzureRM.Compute</span></span>
* <span data-ttu-id="6b1f7-168">Функция добавления тега IP-адреса для масштабируемого набора виртуальных машин (VMSS)</span><span class="sxs-lookup"><span data-stu-id="6b1f7-168">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="6b1f7-169">Добавлен командлет New-AzureRmVmssIpTagConfig.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-169">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="6b1f7-170">В New-AzureRmVmssIpConfig добавлен параметр IpTag.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-170">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="6b1f7-171">Функция автоматического отката ОС для VMSS</span><span class="sxs-lookup"><span data-stu-id="6b1f7-171">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="6b1f7-172">В New-AzureRmVmssConfig и Update-AzureRmVmss добавлены параметры DisableAutoRollback.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-172">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="6b1f7-173">Функция ведения журнала обновлений ОС для VMSS</span><span class="sxs-lookup"><span data-stu-id="6b1f7-173">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="6b1f7-174">В Get-AzureRmVmss добавлен параметр OSUpgradeHistory.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-174">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="6b1f7-175">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="6b1f7-175">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="6b1f7-176">Добавлена поддержка списков управления доступом к каталогу с использованием следующих команд:</span><span class="sxs-lookup"><span data-stu-id="6b1f7-176">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="6b1f7-177">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry;</span><span class="sxs-lookup"><span data-stu-id="6b1f7-177">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="6b1f7-178">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry;</span><span class="sxs-lookup"><span data-stu-id="6b1f7-178">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="6b1f7-179">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-179">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="6b1f7-180">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6b1f7-180">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="6b1f7-181">Добавлены поддержка отмены выполнения и отслеживание хода выполнения для Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl и Remove-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-181">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="6b1f7-182">Добавлена поддержка отмены выполнения для Export-AzureRmDataLakeStoreChildItemProperties.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-182">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="6b1f7-183">Исправлена очистка сообщений об отладке для командлетов, которые выполняют рекурсивные операции.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-183">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="6b1f7-184">Исправлено расположение тестовых данных для командлетов DataLake.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-184">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="6b1f7-185">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="6b1f7-185">AzureRM.EventHub</span></span>
* <span data-ttu-id="6b1f7-186">Для командлетов вывода списка операций Get-AzureRmEventHub и Get-AzureRmEventHubConsumerGroup добавлен необязательный параметр MaxCount.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-186">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="6b1f7-187">Исправлена проблема с командлетом New-AzureRmEventHub, из-за которой требовалось указать по крайней мере один параметр при создании концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-187">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="6b1f7-188">Добавлен набор параметров по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-188">Provided Default Parameter set.</span></span>
* <span data-ttu-id="6b1f7-189">Для командлета New-AzureRmEventHubKey добавлен необязательный параметр -KeyValue, который позволяет пользователю предоставить значение ключа.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-189">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="6b1f7-190">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6b1f7-190">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6b1f7-191">Исправлена ошибка, из-за которой при выполнении командлета Get-AzureRmKeyVault с параметром -Tag возвращались все ресурсы.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-191">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="6b1f7-192">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6b1f7-192">AzureRM.Network</span></span>
* <span data-ttu-id="6b1f7-193">Для параметра шлюзов виртуальной вести, избыточных между зонами, предоставлены новые номера SKU.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-193">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="6b1f7-194">Добавлены новые команды для функции поддержки партнерских API для ExpressRoute, развертываемых с помощью ARM:</span><span class="sxs-lookup"><span data-stu-id="6b1f7-194">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="6b1f7-195">добавлена команда Get-AzureRmExpressRouteCrossConnection;</span><span class="sxs-lookup"><span data-stu-id="6b1f7-195">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="6b1f7-196">добавлена команда Set-AzureRmExpressRouteCrossConnection;</span><span class="sxs-lookup"><span data-stu-id="6b1f7-196">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="6b1f7-197">добавлена команда Add-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="6b1f7-197">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="6b1f7-198">добавлена команда Get-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="6b1f7-198">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="6b1f7-199">добавлена команда Remove-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="6b1f7-199">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="6b1f7-200">добавлена команда Get-AzureRMExpressRouteCrossConnectionArpTable;</span><span class="sxs-lookup"><span data-stu-id="6b1f7-200">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="6b1f7-201">добавлена команда Get-AzureRMExpressRouteCrossConnectionRouteTable;</span><span class="sxs-lookup"><span data-stu-id="6b1f7-201">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="6b1f7-202">добавлена команда Get-AzureRMExpressRouteCrossConnectionRouteTableSummary.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-202">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="6b1f7-203">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="6b1f7-203">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="6b1f7-204">Добавлен командлет Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-204">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="6b1f7-205">Этот командлет принимает идентификатор виртуальной машины и проверяет, защищена ли виртуальная машина с помощью какого-либо хранилища в подписке.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-205">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="6b1f7-206">Если такое хранилище существует, командлет выводит данные о нем.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-206">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="6b1f7-207">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6b1f7-207">AzureRM.Resources</span></span>
* <span data-ttu-id="6b1f7-208">Обновлены командлеты Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="6b1f7-208">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="6b1f7-209">Добавлена поддержка вывода списка значений параметра -Scope на уровне группы управления.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-209">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="6b1f7-210">Добавлена поддержка для получения отдельных назначений со значениями -Scope на уровне группы управления.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-210">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="6b1f7-211">Для параметра управления добавлены параметры -Effective и -All.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-211">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="6b1f7-212">Обновлены командлеты Get/New/Remove/Set-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-212">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="6b1f7-213">Добавлен параметр -ManagementGroupName для применения операций к заданной группе управления.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-213">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="6b1f7-214">Добавлен параметр -SubscriptionId для применения операций к заданной подписке.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-214">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="6b1f7-215">Обновлены командлеты Get/New/Remove/Set-AzureRmPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-215">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="6b1f7-216">Добавлен параметр -ManagementGroupName для применения операций к заданной группе управления.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-216">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="6b1f7-217">Добавлен параметр -SubscriptionId для применения операций к заданной подписке.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-217">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="6b1f7-218">Добавлена поддержка ссылок на секрет KeyVault в параметрах при использовании TemplateParameterObject в New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-218">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="6b1f7-219">Устранена проблема, из-за которой параметр -EndDate игнорировался в New-AzureRmADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-219">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="6b1f7-220">Устранена проблема, из-за которой в Add-AzureRmADGroupMember использовался неверный URL-адрес для запроса.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-220">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="6b1f7-221">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6b1f7-221">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="6b1f7-222">Для командлета New-AzureRmServiceBusKey добавлен необязательный параметр -KeyValue, который позволяет пользователю предоставить значение ключа.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-222">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="6b1f7-223">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6b1f7-223">AzureRM.Sql</span></span>
* <span data-ttu-id="6b1f7-224">В справке по New-AzureRmSqlDatabaseRestorePoint добавлено описание определяемых пользователем точек восстановления для хранилища данных SQL.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-224">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="6b1f7-225">Обновлена документация по параметру -ComputeGeneration, используемого в нескольких командлетах.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-225">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="6b1f7-226">6.3.0 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-226">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="6b1f7-227">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6b1f7-227">AzureRM.Profile</span></span>
* <span data-ttu-id="6b1f7-228">Обновлены сообщения об ошибках для Enable-AzureRmContextAutoSave.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-228">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="6b1f7-229">Создание контекста для каждой подписки при выполнении Connect-AzureRmAccount без предыдущего контекста.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-229">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="6b1f7-230">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="6b1f7-230">Azure.Storage</span></span>
* <span data-ttu-id="6b1f7-231">В файлы справки добавлены дополнительные сведения о параметре -Permissions.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-231">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6b1f7-232">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6b1f7-232">AzureRM.Compute</span></span>
* <span data-ttu-id="6b1f7-233">Get-AzureRmVmDiskEncryptionStatus устраняет проблему, которая наблюдалась на виртуальных машинах без дисков данных.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-233">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="6b1f7-234">Обновлена версия клиентской библиотеки Compute для исправления следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="6b1f7-234">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="6b1f7-235">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="6b1f7-235">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="6b1f7-236">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="6b1f7-236">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="6b1f7-237">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="6b1f7-237">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="6b1f7-238">В следующих командлетах исправлено отображение неправильных значений operation ID и operation status:</span><span class="sxs-lookup"><span data-stu-id="6b1f7-238">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="6b1f7-239">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6b1f7-239">Start-AzureRmVM</span></span>
    - <span data-ttu-id="6b1f7-240">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6b1f7-240">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="6b1f7-241">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6b1f7-241">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="6b1f7-242">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6b1f7-242">Set-AzureRmVM</span></span>
    - <span data-ttu-id="6b1f7-243">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="6b1f7-243">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="6b1f7-244">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6b1f7-244">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="6b1f7-245">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="6b1f7-245">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="6b1f7-246">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="6b1f7-246">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="6b1f7-247">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6b1f7-247">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="6b1f7-248">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6b1f7-248">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="6b1f7-249">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6b1f7-249">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="6b1f7-250">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6b1f7-250">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="6b1f7-251">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="6b1f7-251">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="6b1f7-252">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="6b1f7-252">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="6b1f7-253">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="6b1f7-253">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="6b1f7-254">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="6b1f7-254">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="6b1f7-255">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="6b1f7-255">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="6b1f7-256">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="6b1f7-256">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="6b1f7-257">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="6b1f7-257">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="6b1f7-258">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6b1f7-258">AzureRM.EventGrid</span></span>
* <span data-ttu-id="6b1f7-259">Удалены условия проверки ValidateNotNullOrEmpty для SubjectBeginsWith/SubjectEndsWith в командлете Update-AzureRmEventGridSubscription, что позволяет при необходимости заменять эти параметры пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-259">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="6b1f7-260">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6b1f7-260">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6b1f7-261">Исправлена ошибка, когда при выполнении командлета Get-AzureRmKeyVault -Tag не возвращается ни один тег.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-261">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="6b1f7-262">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6b1f7-262">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="6b1f7-263">Общедоступный выпуск командлетов Policy Insights.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-263">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="6b1f7-264">Используется API версии 2018-04-04.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-264">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="6b1f7-265">К результатам Get-AzureRmPolicyStateSummary добавлено PolicyDefinitionReferenceId.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-265">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="6b1f7-266">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="6b1f7-266">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="6b1f7-267">Для командлетов RecoveryServices.Backup добавлен параметр -Vault.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-267">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="6b1f7-268">Передача этого параметра переопределяет командлет Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-268">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="6b1f7-269">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6b1f7-269">AzureRM.Sql</span></span>
* <span data-ttu-id="6b1f7-270">В файле справки обновлен пример для командлета Get-AzureRmSqlDatabaseExpanded.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-270">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="6b1f7-271">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6b1f7-271">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="6b1f7-272">Обновлен файл справки для командлета Add-AzureRmTrafficManagerEndpointConfig.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-272">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="6b1f7-273">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="6b1f7-273">AzureRM.Websites</span></span>
* <span data-ttu-id="6b1f7-274">Изменено действие командлета Set-AzureRmWebApp. Теперь он не перезаписывает AppSettings, если используется параметр -AssignIdentity.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-274">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="6b1f7-275">Командлет New-AzureRmWebAppSlot теперь учитывает дополнительный параметр AppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-275">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="6b1f7-276">6.2.1 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-276">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="6b1f7-277">AzureRM.OperationalInsights;</span><span class="sxs-lookup"><span data-stu-id="6b1f7-277">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="6b1f7-278">В обновленной модели PSWorkspace Network может использовать type в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-278">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="6b1f7-279">6.2.0 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-279">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="6b1f7-280">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6b1f7-280">AzureRM.Profile</span></span>
* <span data-ttu-id="6b1f7-281">Исправлена ошибка с загрузкой Newtonsoft.Json версии 10.0.3 во время импорта модуля.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-281">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6b1f7-282">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6b1f7-282">AzureRM.Compute</span></span>
* <span data-ttu-id="6b1f7-283">Функция обновления виртуальных машин VMSS.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-283">VMSS VM Update feature</span></span>
    - <span data-ttu-id="6b1f7-284">Добавлены командлеты Update-AzureRmVmssVM и New-AzureRmVMDataDisk.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-284">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="6b1f7-285">В командлет Add-AzureRmVMDataDisk добавлен параметр VirtualMachineScaleSetVM, который позволяет добавлять диски данных в виртуальные машины VMSS.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-285">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="6b1f7-286">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6b1f7-286">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="6b1f7-287">Пакет SDK для ADF .NET обновлен до версии 0.8.0-preview. Новая версия содержит такие изменения:</span><span class="sxs-lookup"><span data-stu-id="6b1f7-287">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="6b1f7-288">добавлена операция для настройки репозитория фабрики;</span><span class="sxs-lookup"><span data-stu-id="6b1f7-288">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="6b1f7-289">связанная служба QuickBooks LinkedService теперь предоставляет свойства consumerKey и consumerSecret;</span><span class="sxs-lookup"><span data-stu-id="6b1f7-289">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="6b1f7-290">тип нескольких моделей изменен с SecretBase на Object;</span><span class="sxs-lookup"><span data-stu-id="6b1f7-290">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="6b1f7-291">добавлен триггер событий BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-291">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="6b1f7-292">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6b1f7-292">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6b1f7-293">В документацию добавлены примеры выходных данных.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-293">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="6b1f7-294">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6b1f7-294">AzureRM.Network</span></span>
* <span data-ttu-id="6b1f7-295">В командлеты Наблюдателя за сетями добавлены параметры Аналитики трафика.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-295">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="6b1f7-296">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6b1f7-296">AzureRM.Resources</span></span>
* <span data-ttu-id="6b1f7-297">Исправлена ошибка, когда командлет Get-AzureRmResource возвращает свойство Properties объектов PSResource.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-297">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="6b1f7-298">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="6b1f7-298">AzureRM.Scheduler</span></span>
* <span data-ttu-id="6b1f7-299">Исправлена ошибка, когда обновление ServiceBusQueueJob не задает новые значения для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-299">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="6b1f7-300">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6b1f7-300">AzureRM.Sql</span></span>
* <span data-ttu-id="6b1f7-301">В перечисленные ниже командлеты добавлен необязательный параметр LicenseType.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-301">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="6b1f7-302">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="6b1f7-302">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="6b1f7-303">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool;</span><span class="sxs-lookup"><span data-stu-id="6b1f7-303">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="6b1f7-304">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="6b1f7-304">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="6b1f7-305">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="6b1f7-305">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="6b1f7-306">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6b1f7-306">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="6b1f7-307">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="6b1f7-307">AzureRM.Websites</span></span>
* <span data-ttu-id="6b1f7-308">Командлет New-AzureRMWebApp теперь использует общие алгоритмы из библиотеки Strategy.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-308">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="6b1f7-309">6.1.0 — май 2018 г.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-309">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="6b1f7-310">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6b1f7-310">AzureRM.Profile</span></span>
* <span data-ttu-id="6b1f7-311">Устранена проблема с выполнением Clear-AzureRmContext, при которой сохранялся пустой контекст с именем предыдущего контекста по умолчанию, что не позволяло пользователю создать новый контекст со старым именем.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-311">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="6b1f7-312">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6b1f7-312">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="6b1f7-313">Включены операции связывания и отмены связи в автономной системе.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-313">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="6b1f7-314">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6b1f7-314">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="6b1f7-315">Добавлена поддержка ApiVersions, ApiReleases и ApiRevisions.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-315">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="6b1f7-316">Добавлена поддержка серверной части ServiceFabric.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-316">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="6b1f7-317">Добавлена поддержка средства ведения журнала Application Insights.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-317">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="6b1f7-318">Добавлена поддержка для распознавания номера SKU уровня "Базовый" как допустимого номера SKU службы управления API.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-318">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="6b1f7-319">Добавлена поддержка установки сертификатов, выданных частным центром сертификации в качестве корневого или обычного ЦС.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-319">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="6b1f7-320">Добавлена поддержка для приема пользовательских SSL-сертификатов с помощью KeyVault и нескольких имен узлов прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-320">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="6b1f7-321">Добавлена поддержка для удостоверения MSI.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-321">Added support for MSI identity</span></span>
* <span data-ttu-id="6b1f7-322">Добавлена поддержка для принятия политик с помощью URL-адреса. Примечание. Указанные ниже командлеты в следующей версии будут отмечены как нерекомендуемые.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-322">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="6b1f7-323">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="6b1f7-323">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="6b1f7-324">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="6b1f7-324">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="6b1f7-325">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="6b1f7-325">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="6b1f7-326">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="6b1f7-326">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="6b1f7-327">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="6b1f7-327">AzureRM.Batch</span></span>
* <span data-ttu-id="6b1f7-328">Выпущен новый командлет Get-AzureBatchPoolNodeCounts.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-328">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="6b1f7-329">Выпущен новый командлет Start-AzureBatchComputeNodeServiceLogUpload.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-329">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="6b1f7-330">AzureRM.Consumption:</span><span class="sxs-lookup"><span data-stu-id="6b1f7-330">AzureRM.Consumption</span></span>
* <span data-ttu-id="6b1f7-331">Добавлены новые параметры Expand, ResourceGroup, InstanceName, InstanceId, Tags и командлет высшего уровня Get-AzureRmConsumptionUsageDetail.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-331">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="6b1f7-332">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6b1f7-332">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="6b1f7-333">Исправлен пример для Export-AzureRmDataLakeStoreChildItemProperties.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-333">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="6b1f7-334">Исправлено исключение параметра NULL при использовании рекурсии в Set-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-334">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="6b1f7-335">Исправлены файлы справки для Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl и Remove-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-335">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="6b1f7-336">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6b1f7-336">AzureRM.Network</span></span>
* <span data-ttu-id="6b1f7-337">Пакет SDK для сети обновлен с предварительной версии 18.0.0 до предварительной версии 19.0.0.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-337">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="6b1f7-338">Добавлен командлет для создания конфигурации протокола.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-338">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="6b1f7-339">New-AzureRmNetworkWatcherProtocolConfiguration.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-339">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="6b1f7-340">Добавлен командлет для добавления нового подключения канала к существующему каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-340">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="6b1f7-341">Add-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-341">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="6b1f7-342">Добавлен командлет для удаления подключения канала к существующему каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-342">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="6b1f7-343">Remove-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-343">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="6b1f7-344">Добавлен командлет для получения подключения канала.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-344">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="6b1f7-345">Get-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-345">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="6b1f7-346">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6b1f7-346">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="6b1f7-347">Исправлена процедура аутентификации сервера с использованием созданных сертификатов (проблема № 5998).</span><span class="sxs-lookup"><span data-stu-id="6b1f7-347">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="6b1f7-348">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6b1f7-348">AzureRM.Sql</span></span>
* <span data-ttu-id="6b1f7-349">Обновлены командлеты аудита, которые теперь позволяют удалять AuditActions или AuditActionGroups.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-349">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="6b1f7-350">Исправлена проблема с Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy, при которой установка новой гибкой политики хранения завершалась ошибкой с сообщением "Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-350">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="6b1f7-351">Please submit request with the new flexible retention policy" (Настройка политики долгосрочного хранения с помощью хранилища и политики служб восстановления Azure больше не поддерживается. Отправьте запрос с использованием новой гибкой политики хранения).</span><span class="sxs-lookup"><span data-stu-id="6b1f7-351">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="6b1f7-352">Обновлены все командлеты, связанные со службой "База данных SQL Azure", с созданием эластичных пулов и обновлением. Теперь используются новые API баз данных с поддержкой свойства номеров SKU для обеспечения масштабируемости и связанных с уровнями возможностей.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-352">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="6b1f7-353">Обновлены командлеты, в том числе:</span><span class="sxs-lookup"><span data-stu-id="6b1f7-353">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="6b1f7-354">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="6b1f7-354">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="6b1f7-355">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool;</span><span class="sxs-lookup"><span data-stu-id="6b1f7-355">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="6b1f7-356">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="6b1f7-356">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="6b1f7-357">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="6b1f7-357">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="6b1f7-358">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6b1f7-358">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="6b1f7-359">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6b1f7-359">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="6b1f7-360">Обновлены параметры для Get-AzureRmTrafficManagerProfile. Теперь при использовании параметра -Name требуется параметр -ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="6b1f7-360">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>