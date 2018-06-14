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
ms.openlocfilehash: 5bc3c9079cb4019bdb2255ab1f947e8ad35ae4cc
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2018
ms.locfileid: "34853463"
---
# <a name="release-notes"></a><span data-ttu-id="5f28d-103">Заметки о выпуске</span><span class="sxs-lookup"><span data-stu-id="5f28d-103">Release notes</span></span>

<span data-ttu-id="5f28d-104">Здесь приведен список изменений, внесенных в Azure PowerShell в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="5f28d-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="620---june-2018"></a><span data-ttu-id="5f28d-105">6.2.0 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="5f28d-105">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="5f28d-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="5f28d-106">AzureRM.Profile</span></span>
* <span data-ttu-id="5f28d-107">Исправлена ошибка с загрузкой Newtonsoft.Json версии 10.0.3 во время импорта модуля.</span><span class="sxs-lookup"><span data-stu-id="5f28d-107">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="5f28d-108">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="5f28d-108">AzureRM.Compute</span></span>
* <span data-ttu-id="5f28d-109">Функция обновления виртуальных машин VMSS.</span><span class="sxs-lookup"><span data-stu-id="5f28d-109">VMSS VM Update feature</span></span>
    - <span data-ttu-id="5f28d-110">Добавлены командлеты Update-AzureRmVmssVM и New-AzureRmVMDataDisk.</span><span class="sxs-lookup"><span data-stu-id="5f28d-110">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="5f28d-111">В командлет Add-AzureRmVMDataDisk добавлен параметр VirtualMachineScaleSetVM, который позволяет добавлять диски данных в виртуальные машины VMSS.</span><span class="sxs-lookup"><span data-stu-id="5f28d-111">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="5f28d-112">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="5f28d-112">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="5f28d-113">Пакет SDK для ADF .NET обновлен до версии 0.8.0-preview. Новая версия содержит такие изменения:</span><span class="sxs-lookup"><span data-stu-id="5f28d-113">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="5f28d-114">добавлена операция для настройки репозитория фабрики;</span><span class="sxs-lookup"><span data-stu-id="5f28d-114">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="5f28d-115">связанная служба QuickBooks LinkedService теперь предоставляет свойства consumerKey и consumerSecret;</span><span class="sxs-lookup"><span data-stu-id="5f28d-115">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="5f28d-116">тип нескольких моделей изменен с SecretBase на Object;</span><span class="sxs-lookup"><span data-stu-id="5f28d-116">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="5f28d-117">добавлен триггер событий BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="5f28d-117">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="5f28d-118">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5f28d-118">AzureRM.KeyVault</span></span>
* <span data-ttu-id="5f28d-119">В документацию добавлены примеры выходных данных.</span><span class="sxs-lookup"><span data-stu-id="5f28d-119">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="5f28d-120">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="5f28d-120">AzureRM.Network</span></span>
* <span data-ttu-id="5f28d-121">В командлеты Наблюдателя за сетями добавлены параметры Аналитики трафика.</span><span class="sxs-lookup"><span data-stu-id="5f28d-121">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="5f28d-122">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="5f28d-122">AzureRM.Resources</span></span>
* <span data-ttu-id="5f28d-123">Исправлена ошибка, когда командлет Get-AzureRmResource возвращает свойство Properties объектов PSResource.</span><span class="sxs-lookup"><span data-stu-id="5f28d-123">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="5f28d-124">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="5f28d-124">AzureRM.Scheduler</span></span>
* <span data-ttu-id="5f28d-125">Исправлена ошибка, когда обновление ServiceBusQueueJob не задает новые значения для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="5f28d-125">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="5f28d-126">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="5f28d-126">AzureRM.Sql</span></span>
* <span data-ttu-id="5f28d-127">В перечисленные ниже командлеты добавлен необязательный параметр LicenseType.</span><span class="sxs-lookup"><span data-stu-id="5f28d-127">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="5f28d-128">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="5f28d-128">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="5f28d-129">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool;</span><span class="sxs-lookup"><span data-stu-id="5f28d-129">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="5f28d-130">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="5f28d-130">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="5f28d-131">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="5f28d-131">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="5f28d-132">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5f28d-132">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="5f28d-133">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="5f28d-133">AzureRM.Websites</span></span>
* <span data-ttu-id="5f28d-134">Командлет New-AzureRMWebApp теперь использует общие алгоритмы из библиотеки Strategy.</span><span class="sxs-lookup"><span data-stu-id="5f28d-134">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="5f28d-135">6.1.0 — май 2018 г.</span><span class="sxs-lookup"><span data-stu-id="5f28d-135">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="5f28d-136">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="5f28d-136">AzureRM.Profile</span></span>
* <span data-ttu-id="5f28d-137">Устранена проблема с выполнением Clear-AzureRmContext, при которой сохранялся пустой контекст с именем предыдущего контекста по умолчанию, что не позволяло пользователю создать новый контекст со старым именем.</span><span class="sxs-lookup"><span data-stu-id="5f28d-137">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="5f28d-138">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="5f28d-138">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="5f28d-139">Включены операции связывания и отмены связи в автономной системе.</span><span class="sxs-lookup"><span data-stu-id="5f28d-139">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="5f28d-140">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5f28d-140">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="5f28d-141">Добавлена поддержка ApiVersions, ApiReleases и ApiRevisions.</span><span class="sxs-lookup"><span data-stu-id="5f28d-141">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="5f28d-142">Добавлена поддержка серверной части ServiceFabric.</span><span class="sxs-lookup"><span data-stu-id="5f28d-142">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="5f28d-143">Добавлена поддержка средства ведения журнала Application Insights.</span><span class="sxs-lookup"><span data-stu-id="5f28d-143">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="5f28d-144">Добавлена поддержка для распознавания номера SKU уровня "Базовый" как допустимого номера SKU службы управления API.</span><span class="sxs-lookup"><span data-stu-id="5f28d-144">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="5f28d-145">Добавлена поддержка установки сертификатов, выданных частным центром сертификации в качестве корневого или обычного ЦС.</span><span class="sxs-lookup"><span data-stu-id="5f28d-145">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="5f28d-146">Добавлена поддержка для приема пользовательских SSL-сертификатов с помощью KeyVault и нескольких имен узлов прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="5f28d-146">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="5f28d-147">Добавлена поддержка для удостоверения MSI.</span><span class="sxs-lookup"><span data-stu-id="5f28d-147">Added support for MSI identity</span></span>
* <span data-ttu-id="5f28d-148">Добавлена поддержка для принятия политик с помощью URL-адреса. Примечание. Указанные ниже командлеты в следующей версии будут отмечены как нерекомендуемые.</span><span class="sxs-lookup"><span data-stu-id="5f28d-148">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="5f28d-149">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="5f28d-149">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="5f28d-150">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="5f28d-150">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="5f28d-151">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="5f28d-151">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="5f28d-152">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="5f28d-152">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="5f28d-153">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="5f28d-153">AzureRM.Batch</span></span>
* <span data-ttu-id="5f28d-154">Выпущен новый командлет Get-AzureBatchPoolNodeCounts.</span><span class="sxs-lookup"><span data-stu-id="5f28d-154">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="5f28d-155">Выпущен новый командлет Start-AzureBatchComputeNodeServiceLogUpload.</span><span class="sxs-lookup"><span data-stu-id="5f28d-155">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="5f28d-156">AzureRM.Consumption:</span><span class="sxs-lookup"><span data-stu-id="5f28d-156">AzureRM.Consumption</span></span>
* <span data-ttu-id="5f28d-157">Добавлены новые параметры Expand, ResourceGroup, InstanceName, InstanceId, Tags и командлет высшего уровня Get-AzureRmConsumptionUsageDetail.</span><span class="sxs-lookup"><span data-stu-id="5f28d-157">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="5f28d-158">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5f28d-158">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="5f28d-159">Исправлен пример для Export-AzureRmDataLakeStoreChildItemProperties.</span><span class="sxs-lookup"><span data-stu-id="5f28d-159">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="5f28d-160">Исправлено исключение параметра NULL при использовании рекурсии в Set-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="5f28d-160">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="5f28d-161">Исправлены файлы справки для Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl и Remove-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="5f28d-161">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="5f28d-162">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="5f28d-162">AzureRM.Network</span></span>
* <span data-ttu-id="5f28d-163">Пакет SDK для сети обновлен с предварительной версии 18.0.0 до предварительной версии 19.0.0.</span><span class="sxs-lookup"><span data-stu-id="5f28d-163">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="5f28d-164">Добавлен командлет для создания конфигурации протокола.</span><span class="sxs-lookup"><span data-stu-id="5f28d-164">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="5f28d-165">New-AzureRmNetworkWatcherProtocolConfiguration.</span><span class="sxs-lookup"><span data-stu-id="5f28d-165">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="5f28d-166">Добавлен командлет для добавления нового подключения канала к существующему каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="5f28d-166">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="5f28d-167">Add-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="5f28d-167">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="5f28d-168">Добавлен командлет для удаления подключения канала к существующему каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="5f28d-168">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="5f28d-169">Remove-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="5f28d-169">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="5f28d-170">Добавлен командлет для получения подключения канала.</span><span class="sxs-lookup"><span data-stu-id="5f28d-170">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="5f28d-171">Get-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="5f28d-171">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="5f28d-172">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5f28d-172">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="5f28d-173">Исправлена процедура аутентификации сервера с использованием созданных сертификатов (проблема № 5998).</span><span class="sxs-lookup"><span data-stu-id="5f28d-173">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="5f28d-174">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="5f28d-174">AzureRM.Sql</span></span>
* <span data-ttu-id="5f28d-175">Обновлены командлеты аудита, которые теперь позволяют удалять AuditActions или AuditActionGroups.</span><span class="sxs-lookup"><span data-stu-id="5f28d-175">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="5f28d-176">Исправлена проблема с Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy, при которой установка новой гибкой политики хранения завершалась ошибкой с сообщением "Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span><span class="sxs-lookup"><span data-stu-id="5f28d-176">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="5f28d-177">Please submit request with the new flexible retention policy" (Настройка политики долгосрочного хранения с помощью хранилища и политики служб восстановления Azure больше не поддерживается. Отправьте запрос с использованием новой гибкой политики хранения).</span><span class="sxs-lookup"><span data-stu-id="5f28d-177">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="5f28d-178">Обновлены все командлеты, связанные со службой "База данных SQL Azure", с созданием эластичных пулов и обновлением. Теперь используются новые API баз данных с поддержкой свойства номеров SKU для обеспечения масштабируемости и связанных с уровнями возможностей.</span><span class="sxs-lookup"><span data-stu-id="5f28d-178">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="5f28d-179">Обновлены командлеты, в том числе:</span><span class="sxs-lookup"><span data-stu-id="5f28d-179">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="5f28d-180">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="5f28d-180">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="5f28d-181">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool;</span><span class="sxs-lookup"><span data-stu-id="5f28d-181">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="5f28d-182">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="5f28d-182">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="5f28d-183">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="5f28d-183">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="5f28d-184">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5f28d-184">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="5f28d-185">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="5f28d-185">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="5f28d-186">Обновлены параметры для Get-AzureRmTrafficManagerProfile. Теперь при использовании параметра -Name требуется параметр -ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="5f28d-186">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>