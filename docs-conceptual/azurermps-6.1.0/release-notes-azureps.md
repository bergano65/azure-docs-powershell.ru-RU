---
title: Журнал изменений Azure PowerShell | Документация Майкрософт
description: Это руководство содержит историю изменений Azure PowerShell, внесенных в новом выпуске.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 0b7902155c47f2e6355e9147c203867288caab81
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/23/2018
ms.locfileid: "34462139"
---
# <a name="release-notes"></a><span data-ttu-id="c4cf0-103">Заметки о выпуске</span><span class="sxs-lookup"><span data-stu-id="c4cf0-103">Release notes</span></span>

<span data-ttu-id="c4cf0-104">Здесь приведен список изменений, внесенных в Azure PowerShell в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="c4cf0-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="610---may-2018"></a><span data-ttu-id="c4cf0-105">6.1.0 — май 2018 г.</span><span class="sxs-lookup"><span data-stu-id="c4cf0-105">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="c4cf0-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c4cf0-106">AzureRM.Profile</span></span>
* <span data-ttu-id="c4cf0-107">Устранена проблема с выполнением Clear-AzureRmContext, при которой сохранялся пустой контекст с именем предыдущего контекста по умолчанию, что не позволяло пользователю создать новый контекст со старым именем.</span><span class="sxs-lookup"><span data-stu-id="c4cf0-107">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="c4cf0-108">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c4cf0-108">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="c4cf0-109">Включены операции связывания и отмены связи в автономной системе.</span><span class="sxs-lookup"><span data-stu-id="c4cf0-109">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="c4cf0-110">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c4cf0-110">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="c4cf0-111">Добавлена поддержка ApiVersions, ApiReleases и ApiRevisions.</span><span class="sxs-lookup"><span data-stu-id="c4cf0-111">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="c4cf0-112">Добавлена поддержка серверной части ServiceFabric.</span><span class="sxs-lookup"><span data-stu-id="c4cf0-112">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="c4cf0-113">Добавлена поддержка средства ведения журнала Application Insights.</span><span class="sxs-lookup"><span data-stu-id="c4cf0-113">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="c4cf0-114">Добавлена поддержка для распознавания номера SKU уровня "Базовый" как допустимого номера SKU службы управления API.</span><span class="sxs-lookup"><span data-stu-id="c4cf0-114">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="c4cf0-115">Добавлена поддержка установки сертификатов, выданных частным центром сертификации в качестве корневого или обычного ЦС.</span><span class="sxs-lookup"><span data-stu-id="c4cf0-115">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="c4cf0-116">Добавлена поддержка для приема пользовательских SSL-сертификатов с помощью KeyVault и нескольких имен узлов прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="c4cf0-116">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="c4cf0-117">Добавлена поддержка для удостоверения MSI.</span><span class="sxs-lookup"><span data-stu-id="c4cf0-117">Added support for MSI identity</span></span>
* <span data-ttu-id="c4cf0-118">Добавлена поддержка для принятия политик с помощью URL-адреса. Примечание. Указанные ниже командлеты в следующей версии будут отмечены как нерекомендуемые.</span><span class="sxs-lookup"><span data-stu-id="c4cf0-118">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="c4cf0-119">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="c4cf0-119">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="c4cf0-120">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4cf0-120">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="c4cf0-121">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="c4cf0-121">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="c4cf0-122">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="c4cf0-122">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="c4cf0-123">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="c4cf0-123">AzureRM.Batch</span></span>
* <span data-ttu-id="c4cf0-124">Выпущен новый командлет Get-AzureBatchPoolNodeCounts.</span><span class="sxs-lookup"><span data-stu-id="c4cf0-124">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="c4cf0-125">Выпущен новый командлет Start-AzureBatchComputeNodeServiceLogUpload.</span><span class="sxs-lookup"><span data-stu-id="c4cf0-125">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="c4cf0-126">AzureRM.Consumption:</span><span class="sxs-lookup"><span data-stu-id="c4cf0-126">AzureRM.Consumption</span></span>
* <span data-ttu-id="c4cf0-127">Добавлены новые параметры Expand, ResourceGroup, InstanceName, InstanceId, Tags и командлет высшего уровня Get-AzureRmConsumptionUsageDetail.</span><span class="sxs-lookup"><span data-stu-id="c4cf0-127">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="c4cf0-128">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c4cf0-128">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="c4cf0-129">Исправлен пример для Export-AzureRmDataLakeStoreChildItemProperties.</span><span class="sxs-lookup"><span data-stu-id="c4cf0-129">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="c4cf0-130">Исправлено исключение параметра NULL при использовании рекурсии в Set-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="c4cf0-130">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="c4cf0-131">Исправлены файлы справки для Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl и Remove-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="c4cf0-131">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="c4cf0-132">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c4cf0-132">AzureRM.Network</span></span>
* <span data-ttu-id="c4cf0-133">Пакет SDK для сети обновлен с предварительной версии 18.0.0 до предварительной версии 19.0.0.</span><span class="sxs-lookup"><span data-stu-id="c4cf0-133">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="c4cf0-134">Добавлен командлет для создания конфигурации протокола.</span><span class="sxs-lookup"><span data-stu-id="c4cf0-134">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="c4cf0-135">New-AzureRmNetworkWatcherProtocolConfiguration.</span><span class="sxs-lookup"><span data-stu-id="c4cf0-135">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="c4cf0-136">Добавлен командлет для добавления нового подключения канала к существующему каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c4cf0-136">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="c4cf0-137">Add-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="c4cf0-137">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="c4cf0-138">Добавлен командлет для удаления подключения канала к существующему каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c4cf0-138">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="c4cf0-139">Remove-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="c4cf0-139">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="c4cf0-140">Добавлен командлет для получения подключения канала.</span><span class="sxs-lookup"><span data-stu-id="c4cf0-140">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="c4cf0-141">Get-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="c4cf0-141">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="c4cf0-142">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c4cf0-142">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="c4cf0-143">Исправлена процедура аутентификации сервера с использованием созданных сертификатов (проблема № 5998).</span><span class="sxs-lookup"><span data-stu-id="c4cf0-143">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="c4cf0-144">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c4cf0-144">AzureRM.Sql</span></span>
* <span data-ttu-id="c4cf0-145">Обновлены командлеты аудита, которые теперь позволяют удалять AuditActions или AuditActionGroups.</span><span class="sxs-lookup"><span data-stu-id="c4cf0-145">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="c4cf0-146">Исправлена проблема с Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy, при которой установка новой гибкой политики хранения завершалась ошибкой с сообщением "Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span><span class="sxs-lookup"><span data-stu-id="c4cf0-146">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="c4cf0-147">Please submit request with the new flexible retention policy" (Настройка политики долгосрочного хранения с помощью хранилища и политики служб восстановления Azure больше не поддерживается. Отправьте запрос с использованием новой гибкой политики хранения).</span><span class="sxs-lookup"><span data-stu-id="c4cf0-147">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="c4cf0-148">Обновлены все командлеты, связанные со службой "База данных SQL Azure", с созданием эластичных пулов и обновлением. Теперь используются новые API баз данных с поддержкой свойства номеров SKU для обеспечения масштабируемости и связанных с уровнями возможностей.</span><span class="sxs-lookup"><span data-stu-id="c4cf0-148">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="c4cf0-149">Обновлены командлеты, в том числе:</span><span class="sxs-lookup"><span data-stu-id="c4cf0-149">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="c4cf0-150">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="c4cf0-150">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="c4cf0-151">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool;</span><span class="sxs-lookup"><span data-stu-id="c4cf0-151">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="c4cf0-152">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="c4cf0-152">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="c4cf0-153">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="c4cf0-153">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="c4cf0-154">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c4cf0-154">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="c4cf0-155">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="c4cf0-155">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="c4cf0-156">Обновлены параметры для Get-AzureRmTrafficManagerProfile. Теперь при использовании параметра -Name требуется параметр -ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="c4cf0-156">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>