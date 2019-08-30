---
ms.openlocfilehash: f89d13d6bbedaea29b62287942d8c7a509abe32b
ms.sourcegitcommit: abca342d8687ca638679c049792d0cef6045837d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2019
ms.locfileid: "70052640"
---
## <a name="260---august-2019"></a><span data-ttu-id="8ccb3-101">2.6.0 — август 2019 г.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-101">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="8ccb3-102">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="8ccb3-102">General</span></span>
* <span data-ttu-id="8ccb3-103">Исправлены опечатки в модулях.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-103">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8ccb3-104">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ccb3-104">Az.Accounts</span></span>
* <span data-ttu-id="8ccb3-105">Добавлена поддержка назначаемого пользователем удостоверения MSI при проверке подлинности в Функциях Azure (№ 9479).</span><span class="sxs-lookup"><span data-stu-id="8ccb3-105">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="8ccb3-106">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="8ccb3-106">Az.Aks</span></span>
* <span data-ttu-id="8ccb3-107">Устранена проблема с выходными данными для Get-AzAks.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-107">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="8ccb3-108">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9847.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-108">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="8ccb3-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8ccb3-109">Az.ApiManagement</span></span>
* <span data-ttu-id="8ccb3-110">исправлена проблема https://github.com/Azure/azure-powershell/issues/9351.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-110">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="8ccb3-111">Обновлена версия NuGet для .NET, которая не накладывает ограничений на productId, apiId, groupId и userId.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-111">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="8ccb3-112">**Get-AzApiManagementProduct**. Добавлена поддержка запросов к продуктам с помощью API.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-112">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="8ccb3-113">**New-AzApiManagementApiRevision**. Устранена проблема, из-за которой не задавался параметр ApiRevisionDescription при создании новой редакции API https://github.com/Azure/azure-powershell/issues/9752.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-113">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="8ccb3-114">Исправлено написание имени модели c PsApiManagementOAuth2AuthrozationServer на PsApiManagementOAuth2AuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-114">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="8ccb3-115">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8ccb3-115">Az.Batch</span></span>
* <span data-ttu-id="8ccb3-116">Исправлена опечатка в написании Windows со строчной буквы в справочных сообщениях и документации.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-116">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8ccb3-117">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8ccb3-117">Az.Cdn</span></span>
* <span data-ttu-id="8ccb3-118">Исправлена опечатка во вспомогательном приложении модуля CDN.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-118">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ccb3-119">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ccb3-119">Az.Compute</span></span>
* <span data-ttu-id="8ccb3-120">Добавлен параметр VmssId в новый командлет Add New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-120">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="8ccb3-121">Добавлены параметры TerminateScheduledEvents и TerminateScheduledEventNotBeforeTimeoutInMinutes в New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-121">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="8ccb3-122">Добавлено свойство HyperVGeneration в объект образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-122">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="8ccb3-123">Добавлены компоненты Host и HostGroup.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-123">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="8ccb3-124">Новые командлеты:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="8ccb3-124">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="8ccb3-125">Параметр HostId добавлен в New-AzVMConfig и New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-125">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="8ccb3-126">Исправлен пример в документации по Invoke-AzVMRunCommand, в котором теперь используется правильное имя параметра.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-126">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="8ccb3-127">Исправлено описание VolumeType в справочной документации по Set-AzVMDiskEncryptionExtension и Set-AzVmssDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-127">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8ccb3-128">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8ccb3-128">Az.DataFactory</span></span>
* <span data-ttu-id="8ccb3-129">Исправлена опечатка в написании Windows со строчной буквы в документации по New-AzDataFactoryEncryptValue.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-129">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="8ccb3-130">Пакет SDK ADF для .NET обновлен до версии 4.1.2.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-130">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="8ccb3-131">Добавлены параметры DataProxyIntegrationRuntimeName, DataProxyStagingLinkedServiceName и DataProxyStagingPath в командлет Set-AzureRmDataFactoryV2IntegrationRuntime, что позволяет настраивать локальную среду выполнения интеграции в качестве прокси-сервера для Azure-SSIS Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-131">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="8ccb3-132">Обновлены PSTriggerRun для отображения активированных конвейеров, сообщений и свойств и PSActivityRun для отображения типа действия.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-132">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8ccb3-133">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8ccb3-133">Az.DataLakeStore</span></span>
* <span data-ttu-id="8ccb3-134">Устранена проблема, при которой Get-DataLakeStoreDeletedItem переставал отвечать на запросы при возникновении ошибок или удаленных исключений.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-134">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8ccb3-135">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8ccb3-135">Az.EventHub</span></span>
* <span data-ttu-id="8ccb3-136">Исправлена проблема № 9658: опечатка в написании параметра VirtualNteworkRule у Set-AzEventHubNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-136">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="8ccb3-137">Исправлена проблема № 9558: в Set-AzEventHubNamespace используется PATCH вместо PUT.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-137">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="8ccb3-138">В командлет Set-AzEventHubNamespace добавлен параметр EnableKafka.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-138">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="8ccb3-139">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-139">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="8ccb3-140">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="8ccb3-140">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="8ccb3-141">Исправлено написание Azure со строчной буквы.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-141">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8ccb3-142">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8ccb3-142">Az.Monitor</span></span>
* <span data-ttu-id="8ccb3-143">Исправлены неправильные имена параметров в справочной документации.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-143">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ccb3-144">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ccb3-144">Az.Network</span></span>
* <span data-ttu-id="8ccb3-145">Обновлен New-AzPrivateLinkServiceIpConfig.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-145">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="8ccb3-146">Параметр PublicIpAddress объявлен нерекомендуемым, так как он не используется на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-146">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="8ccb3-147">Добавлен необязательный параметр Primary, указывающий, является ли текущая IP-конфигурация основной.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-147">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="8ccb3-148">Улучшена обработка исключений из-за ошибок запроса от пакета SDK. Устранена проблема, при которой исключения пакета SDK не обрабатывались правильно, из-за чего не отображались основные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-148">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="8ccb3-149">Настроена логика проверки для префикса IPv6 IP-адреса для проверки правильности длины префикса IPv6.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-149">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="8ccb3-150">Обновлен Get-AzVirtualNetworkSubnetConfig: добавлен набор параметров для получения по идентификатору ресурса подсети.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-150">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="8ccb3-151">Обновлено описание параметра Location для AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-151">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8ccb3-152">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8ccb3-152">Az.OperationalInsights</span></span>
* <span data-ttu-id="8ccb3-153">Обновлена документация по New-AzOperationalInsightsLinuxSyslogDataSource.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-153">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="8ccb3-154">Добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-154">Added example</span></span>
    - <span data-ttu-id="8ccb3-155">Обновлено описание параметра -Name.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-155">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="8ccb3-156">Добавлен пример для New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="8ccb3-156">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="8ccb3-157">Изменено описание параметра -Name для New-AzOperationalInsightsWindowsEventDataSource.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-157">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8ccb3-158">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8ccb3-158">Az.RecoveryServices</span></span>
* <span data-ttu-id="8ccb3-159">Обновлен Get-AzRecoveryServicesBackupJobDetail.md.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-159">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ccb3-160">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ccb3-160">Az.Resources</span></span>
* <span data-ttu-id="8ccb3-161">Добавлена поддержка новой версии API 2019-05-10 для Microsoft.Resource.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-161">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="8ccb3-162">Добавлена поддержка copy.count = 0 для переменных, ресурсов и свойств.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-162">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="8ccb3-163">Ресурсы, у которых condition = false или copy.count = 0, будут удаляться в полном режиме.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-163">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="8ccb3-164">В справочную документацию добавлен пример назначения политики на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-164">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8ccb3-165">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8ccb3-165">Az.ServiceBus</span></span>
* <span data-ttu-id="8ccb3-166">Исправлена проблема № 9658: опечатка в написании параметра VirtualNetworkRule В Set-AzServiceBusNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-166">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="8ccb3-167">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-167">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="8ccb3-168">Добавлена новая команда Test-AzServiceBusNameAvailability для проверки доступности имени для очереди и раздела.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-168">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="8ccb3-169">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8ccb3-169">Az.ServiceFabric</span></span>
* <span data-ttu-id="8ccb3-170">Устранены ошибки командлета для добавления типа узла:</span><span class="sxs-lookup"><span data-stu-id="8ccb3-170">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="8ccb3-171">ошибка NullReferenceException, возникавшая, если у группы ресурсов были другие VMSS, не связанные с кластером Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-171">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="8ccb3-172">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8681.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-172">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="8ccb3-173">Исправлена ошибка, из-за которой командлет завершился сбоем, если virtualNetwork находилась не в той группе ресурсов, к которой относится кластер.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-173">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="8ccb3-174">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8407.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-174">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="8ccb3-175">Командлет Add-AzServiceFabricApplicationCertificate объявлен нерекомендуемым.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-175">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ccb3-176">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ccb3-176">Az.Sql</span></span>
* <span data-ttu-id="8ccb3-177">Обновление документации по старым командлетам аудита.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-177">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8ccb3-178">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8ccb3-178">Az.Storage</span></span>
* <span data-ttu-id="8ccb3-179">Обновлена справка по Get/Close-AzStorageFileHandle: в примеры добавлены сценарии использования командлетов и обновлено описание параметров.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-179">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="8ccb3-180">Добавлена поддержка StandardBlobTier в операции отправки BLOB-объекта и копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-180">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="8ccb3-181">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8ccb3-181">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="8ccb3-182">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="8ccb3-182">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="8ccb3-183">Добавлена поддержка приоритета восстановления в операцию копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-183">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="8ccb3-184">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="8ccb3-184">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8ccb3-185">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8ccb3-185">Az.Websites</span></span>
* <span data-ttu-id="8ccb3-186">Добавлены уточнение для параметра -AppSettings в Set-AzWebApp и Set-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-186">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="8ccb3-187">2.5.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-187">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8ccb3-188">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ccb3-188">Az.Accounts</span></span>
* <span data-ttu-id="8ccb3-189">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-189">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="8ccb3-190">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="8ccb3-190">Az.ApplicationInsights</span></span>
* <span data-ttu-id="8ccb3-191">Исправлена опечатка в примере в документации по Remove-AzApplicationInsightsApiKey.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-191">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="8ccb3-192">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8ccb3-192">Az.Automation</span></span>
* <span data-ttu-id="8ccb3-193">Исправлена опечатка в строке ресурса.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-193">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="8ccb3-194">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8ccb3-194">Az.CognitiveServices</span></span>
* <span data-ttu-id="8ccb3-195">Добавлена поддержка NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-195">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ccb3-196">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ccb3-196">Az.Compute</span></span>
* <span data-ttu-id="8ccb3-197">Добавлены недостающие свойства (ComputerName, OsName, OsVersion и HyperVGeneration) для объекта представления экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-197">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="8ccb3-198">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8ccb3-198">Az.ContainerRegistry</span></span>
* <span data-ttu-id="8ccb3-199">Исправлена опечатка в Remove-AzContainerRegistryReplication для параметра репликации.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-199">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="8ccb3-200">См. подробнее: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-200">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8ccb3-201">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8ccb3-201">Az.DataFactory</span></span>
* <span data-ttu-id="8ccb3-202">Пакет SDK для ADF .NET обновлен до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-202">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="8ccb3-203">Исправлена опечатка в документации по Get-AzDataFactoryV2PipelineRun.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-203">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8ccb3-204">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8ccb3-204">Az.EventHub</span></span>
* <span data-ttu-id="8ccb3-205">Добавлен новый командлет для создания маркера SAS: New-AzEventHubAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-205">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="8ccb3-206">Добавлена проверка и сообщение об ошибке для случаев, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="8ccb3-206">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8ccb3-207">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8ccb3-207">Az.KeyVault</span></span>
* <span data-ttu-id="8ccb3-208">Добавлена поддержка для настройки параметра KeySize в политиках сертификатов.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-208">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8ccb3-209">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8ccb3-209">Az.LogicApp</span></span>
* <span data-ttu-id="8ccb3-210">Get-AzIntegrationAccountMap теперь надлежащим образом выводит все типы сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-210">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="8ccb3-211">Добавлен новый параметр MapType для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-211">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="8ccb3-212">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="8ccb3-212">Az.ManagedServices</span></span>
* <span data-ttu-id="8ccb3-213">Добавлена поддержка API версии 2019-06-01 (общедоступная).</span><span class="sxs-lookup"><span data-stu-id="8ccb3-213">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ccb3-214">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ccb3-214">Az.Network</span></span>
* <span data-ttu-id="8ccb3-215">Добавлена поддержка частной конечной точки и службы приватного канала.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-215">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="8ccb3-216">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="8ccb3-216">New cmdlets</span></span>
        - <span data-ttu-id="8ccb3-217">Set-AzPrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-217">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="8ccb3-218">Set-AzPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-218">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="8ccb3-219">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-219">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8ccb3-220">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-220">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8ccb3-221">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-221">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8ccb3-222">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-222">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8ccb3-223">Test-AzPrivateLinkServiceVisibility.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-223">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="8ccb3-224">Get-AzAutoApprovedPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-224">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="8ccb3-225">Обновлены следующие команды для функции: Флаг PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies в подсети в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-225">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="8ccb3-226">Обновлены командлеты New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-226">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="8ccb3-227">Добавлен необязательный параметр -PrivateEndpointNetworkPoliciesFlag, который указывает, что включение или отключение приводят к применению политик сети на частной конечной точке в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-227">Added optional parameter -PrivateEndpointNetworkPoliciesFlag to indicate that enable or disable apply network policies on pivate endpoint in this subnet.</span></span>
        - <span data-ttu-id="8ccb3-228">Добавлен необязательный параметр -PrivateLinkServiceNetworkPoliciesFlag, который указывает, что включение или отключение приводят к применению политик сети в службе приватного канала в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-228">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag to indicate that enable or disable apply network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="8ccb3-229">Параметр ServiceName командлета AzPrivateLinkService был переименован на Name с псевдонимом ServiceName для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-229">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="8ccb3-230">Включен протокол ICMP для настройки правил безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-230">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="8ccb3-231">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="8ccb3-231">Updated cmdlets</span></span>
        - <span data-ttu-id="8ccb3-232">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-232">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="8ccb3-233">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-233">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="8ccb3-234">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-234">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="8ccb3-235">Добавлен ConnectionProtocolType (Ikev1/Ikev2) в качестве настраиваемого параметра для командлета New-AzVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-235">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="8ccb3-236">Добавлен PrivateIpAddressVersion в LoadBalancerFrontendIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-236">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="8ccb3-237">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="8ccb3-237">Updated cmdlet:</span></span>
        - <span data-ttu-id="8ccb3-238">New-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-238">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="8ccb3-239">Add-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-239">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="8ccb3-240">Set-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-240">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="8ccb3-241">Команда New-AzApplicationGatewayProbeConfig Шлюза приложений обновлена для поддержки настраиваемого порта в зонде.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-241">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="8ccb3-242">Обновлен командлет New-AzApplicationGatewayProbeConfig: добавлен необязательный параметр Port, который используется при проверке внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-242">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="8ccb3-243">Этот параметр применяется к номерам SKU Standard_V2 и WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-243">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8ccb3-244">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8ccb3-244">Az.OperationalInsights</span></span>
* <span data-ttu-id="8ccb3-245">Обновленная версия по умолчанию для сохраненных операций поиска имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-245">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="8ccb3-246">Исправлены ошибки при обработке регулярных выражений со значениями NULL в журналах.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-246">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8ccb3-247">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8ccb3-247">Az.RecoveryServices</span></span>
* <span data-ttu-id="8ccb3-248">Обновлен файл Get-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-248">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="8ccb3-249">Обновлен файл Get-AzRecoveryServicesBackupContainer.md.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-249">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="8ccb3-250">Обновлен файл Get-AzRecoveryServicesVault.md.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-250">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="8ccb3-251">Обновлен файл Wait-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-251">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="8ccb3-252">Обновлен файл Set-AzRecoveryServicesVaultContext.md.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-252">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="8ccb3-253">Обновлен файл Get-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-253">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="8ccb3-254">Обновлен файл Get-AzRecoveryServicesBackupRecoveryPoint.md.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-254">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="8ccb3-255">Обновлен файл Restore-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-255">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="8ccb3-256">Обновлен вызов службы для отмены регистрации контейнера в общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-256">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="8ccb3-257">Обновлен файл Set-AzRecoveryServicesAsrAlertSetting.md.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-257">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ccb3-258">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ccb3-258">Az.Resources</span></span>
- <span data-ttu-id="8ccb3-259">Удален отсутствующий командлет, который упоминается в документации по New-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-259">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="8ccb3-260">Обновлены командлеты политик для использования новой версии API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-260">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8ccb3-261">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8ccb3-261">Az.ServiceBus</span></span>
* <span data-ttu-id="8ccb3-262">Добавлен новый командлет для создания маркера SAS: New-AzServiceBusAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-262">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="8ccb3-263">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="8ccb3-263">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ccb3-264">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ccb3-264">Az.Sql</span></span>
* <span data-ttu-id="8ccb3-265">Исправлены отсутствующие примеры для командлета Set-AzSqlDatabaseSecondary.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-265">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="8ccb3-266">Исправлены заданные повторяющиеся проверки для оценки наличия уязвимостей без указания адресов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-266">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="8ccb3-267">Исправлена незначительная опечатка в сообщении предупреждения.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-267">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8ccb3-268">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8ccb3-268">Az.Storage</span></span>
* <span data-ttu-id="8ccb3-269">Обновлен пример в справочной документации для использования командлетом Get-AzStorageAccount правильного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-269">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="8ccb3-270">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="8ccb3-270">Az.StorageSync</span></span>
* <span data-ttu-id="8ccb3-271">Добавлен командлет Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-271">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="8ccb3-272">Исправлена проблема № 9551, связанная с TierFilesOlderThanDays.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-272">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8ccb3-273">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8ccb3-273">Az.Websites</span></span>
* <span data-ttu-id="8ccb3-274">Исправлена ошибка, при которой некоторые свойства SiteConfig не возвращались Get-AzWebApp и Set-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-274">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="8ccb3-275">Добавлен новый параметр Location в Get-AzDeletedWebApp и Restore-AzDeletedWebApp.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-275">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="8ccb3-276">Исправлена ошибка, которая возникала при клонировании слотов веб-приложений с помощью командлета New-AzWebApp-IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-276">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="8ccb3-277">2.4.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-277">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8ccb3-278">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ccb3-278">Az.Accounts</span></span>
* <span data-ttu-id="8ccb3-279">Добавлена поддержка командлетов профиля.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-279">Add support for profile cmdlets</span></span>
* <span data-ttu-id="8ccb3-280">Добавлена поддержка сред и плоскостей данных в созданных командлетах.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-280">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="8ccb3-281">Исправлена ошибка, когда в командлетах плоскости данных в Windows PowerShell в некоторых случаях использовалась неправильная конечная точка.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-281">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="8ccb3-282">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="8ccb3-282">Az.Advisor</span></span>
* <span data-ttu-id="8ccb3-283">Выпущена общедоступная версия Az.Advisor.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-283">GA release of Az.Advisor</span></span>
* <span data-ttu-id="8ccb3-284">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-284">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="8ccb3-285">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8ccb3-285">Az.ApiManagement</span></span>
* <span data-ttu-id="8ccb3-286">исправлена проблема https://github.com/Azure/azure-powershell/issues/8671.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-286">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="8ccb3-287">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="8ccb3-287">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="8ccb3-288">Добавлена поддержка запрашивания подписок по пользователю и продукту.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-288">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="8ccb3-289">Добавлена поддержка создания запросов с использованием области "/", "/apis", "/apis/echo-api".</span><span class="sxs-lookup"><span data-stu-id="8ccb3-289">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="8ccb3-290">Исправлены проблемы https://github.com/Azure/azure-powershell/issues/9307 и https://github.com/Azure/azure-powershell/issues/8432.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-290">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="8ccb3-291">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="8ccb3-291">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="8ccb3-292">Добавлена поддержка указания ApiVersion и ApiVersionSetId при импорте API-интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-292">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8ccb3-293">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8ccb3-293">Az.Automation</span></span>
* <span data-ttu-id="8ccb3-294">Исправлена ошибка командлета Set-AzAutomationConnectionFieldValue при обработке строкового значения.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-294">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ccb3-295">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ccb3-295">Az.Compute</span></span>
* <span data-ttu-id="8ccb3-296">В New AzImageConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-296">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8ccb3-297">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8ccb3-297">Az.DataFactory</span></span>
* <span data-ttu-id="8ccb3-298">Обновление выходных данных командлетов ADF, предназначенных для получения числа выполнений действий, конвейеров и триггеров, для поддержки канала Select-Object.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-298">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8ccb3-299">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8ccb3-299">Az.EventGrid</span></span>
* <span data-ttu-id="8ccb3-300">Исправлена опечатка в документации по командлету New-AzEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-300">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8ccb3-301">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8ccb3-301">Az.IotHub</span></span>
* <span data-ttu-id="8ccb3-302">Добавлена поддержка повторного создания ключей политики авторизации.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-302">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ccb3-303">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ccb3-303">Az.Network</span></span>
* <span data-ttu-id="8ccb3-304">К тегам общедоступного IP-адреса добавлен тег RoutingPreference.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-304">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="8ccb3-305">Улучшены примеры для справочной документации по командлету Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-305">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8ccb3-306">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8ccb3-306">Az.PolicyInsights</span></span>
* <span data-ttu-id="8ccb3-307">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-307">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="8ccb3-308">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9446.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-308">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8ccb3-309">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8ccb3-309">Az.OperationalInsights</span></span>
* <span data-ttu-id="8ccb3-310">Исправленная модель источника данных CustomLog возвращена в командлет Get-AzOperationalInsightsDataSource.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-310">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8ccb3-311">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8ccb3-311">Az.RecoveryServices</span></span>
* <span data-ttu-id="8ccb3-312">Выпущено исправление для команды get-policy для виртуальных машин IaaS.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-312">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ccb3-313">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ccb3-313">Az.Resources</span></span>
    - <span data-ttu-id="8ccb3-314">Исправлен текст справки по параметру Get-AzPolicyState -Top.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-314">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="8ccb3-315">Добавлена поддержка разбиения по страницам на стороне клиента для Get-AzPolicyAlias.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-315">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="8ccb3-316">Добавлены новые параметры для Set-AzPolicyAssignment, -PolicyParameters и -PolicyParametersObject.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-316">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="8ccb3-317">Добавлен ряд обновлений документов и примеров для командлетов политик.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-317">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8ccb3-318">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8ccb3-318">Az.ServiceBus</span></span>
* <span data-ttu-id="8ccb3-319">Исправление ошибки № 4938: командлет New-AzureRmServiceBusQueue возвращает ответ BadRequest (Недопустимый запрос) при задании значения MaxSizeInMegabytes.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-319">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ccb3-320">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ccb3-320">Az.Sql</span></span>
* <span data-ttu-id="8ccb3-321">Из выпуска предварительной версии в выпуск общедоступной версии добавлены командлеты группы отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-321">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="8ccb3-322">Поддержка аудита Azure SQL Server и баз данных с помощью новых командлетов:</span><span class="sxs-lookup"><span data-stu-id="8ccb3-322">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="8ccb3-323">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="8ccb3-323">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="8ccb3-324">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="8ccb3-324">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="8ccb3-325">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="8ccb3-325">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="8ccb3-326">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="8ccb3-326">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="8ccb3-327">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="8ccb3-327">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="8ccb3-328">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="8ccb3-328">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="8ccb3-329">Из параметров оценки уязвимостей удалены ограничения, касающиеся электронной почты.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-329">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8ccb3-330">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8ccb3-330">Az.Storage</span></span>
* <span data-ttu-id="8ccb3-331">Два параметра в указанном ниже командлете — -IndexDocument и -ErrorDocument404Path, — которые ранее были обязательными, стали необязательными:</span><span class="sxs-lookup"><span data-stu-id="8ccb3-331">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="8ccb3-332">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="8ccb3-332">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="8ccb3-333">Обновлена справка по командлету Get-AzStorageBlobContent: добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-333">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="8ccb3-334">При сбое выполнения командлета с ошибкой StorageException отображаются дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-334">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="8ccb3-335">Добавлена поддержка создания или обновления учетной записи хранения с использованием проверки подлинности AAD DS для службы "Файлы Azure".</span><span class="sxs-lookup"><span data-stu-id="8ccb3-335">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="8ccb3-336">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8ccb3-336">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="8ccb3-337">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8ccb3-337">Set-AzStorageAccount</span></span>
* <span data-ttu-id="8ccb3-338">Добавлена поддержка перечисления или закрытия дескрипторов файлов для общей папки, каталога файлов или файла:</span><span class="sxs-lookup"><span data-stu-id="8ccb3-338">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="8ccb3-339">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="8ccb3-339">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="8ccb3-340">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="8ccb3-340">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="8ccb3-341">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="8ccb3-341">Az.StorageSync</span></span>
* <span data-ttu-id="8ccb3-342">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-342">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="8ccb3-343">2.3.2 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-343">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8ccb3-344">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ccb3-344">Az.Accounts</span></span>
* <span data-ttu-id="8ccb3-345">Исправлена ошибка, связанная с использованием неправильного URL-адреса для вызовов функций.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-345">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="8ccb3-346">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8983.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-346">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="8ccb3-347">Устранена проблема с псевдонимами из AzureRM для командлетов Az.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-347">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="8ccb3-348">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-348">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="8ccb3-349">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-349">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ccb3-350">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ccb3-350">Az.Compute</span></span>
* <span data-ttu-id="8ccb3-351">Простые наборы параметров New-AzVm и New-AzVmss теперь принимают параметр ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-351">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="8ccb3-352">Исправлена опечатка в справочной документации по New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-352">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="8ccb3-353">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="8ccb3-353">Az.Dns</span></span>
* <span data-ttu-id="8ccb3-354">Исправлена опечатка в справочных примерах по использованию Set-AzDnsZone.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-354">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8ccb3-355">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8ccb3-355">Az.EventGrid</span></span>
* <span data-ttu-id="8ccb3-356">Обновлен для использования API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-356">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="8ccb3-357">Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="8ccb3-357">New cmdlets:</span></span>
    - <span data-ttu-id="8ccb3-358">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="8ccb3-358">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="8ccb3-359">Создает домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-359">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="8ccb3-360">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="8ccb3-360">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="8ccb3-361">Возвращает сведения о домене Сетки событий или список всех доменов Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-361">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="8ccb3-362">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="8ccb3-362">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="8ccb3-363">Удаляет домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-363">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="8ccb3-364">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="8ccb3-364">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="8ccb3-365">Повторно создает ключ общего доступа для домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-365">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="8ccb3-366">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="8ccb3-366">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="8ccb3-367">Возвращает ключи общего доступа, используемые для публикации событий в домене Сетки событий.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-367">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="8ccb3-368">New-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="8ccb3-368">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="8ccb3-369">Создает раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-369">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="8ccb3-370">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="8ccb3-370">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="8ccb3-371">Возвращает сведения о разделе домена Сетки событий или список всех разделов определенного домена Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-371">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="8ccb3-372">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="8ccb3-372">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="8ccb3-373">Удаляет раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-373">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="8ccb3-374">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="8ccb3-374">Updated cmdlets:</span></span>
    - <span data-ttu-id="8ccb3-375">New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="8ccb3-375">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="8ccb3-376">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для нового домена Сетки событий и раздела домена Сетки событий и позволяющие создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-376">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="8ccb3-377">Добавляют новые обязательные параметры для указания имени нового домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-377">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="8ccb3-378">Добавляют новые наборы параметров для доменов и разделов домена и позволяют повторно использовать существующие параметры (например, EndPointType, SubjectBeginsWith и т. д.).</span><span class="sxs-lookup"><span data-stu-id="8ccb3-378">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="8ccb3-379">Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="8ccb3-379">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="8ccb3-380">срока действия подписки на событие;</span><span class="sxs-lookup"><span data-stu-id="8ccb3-380">Event subscription expiration date,</span></span>
            - <span data-ttu-id="8ccb3-381">параметров расширенной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-381">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="8ccb3-382">Добавляют новое перечисление для ServiceBusQueue в качестве места назначения.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-382">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="8ccb3-383">Запрещают использование значение All в параметре -IncludedEventType и заменяют его следующим:</span><span class="sxs-lookup"><span data-stu-id="8ccb3-383">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="8ccb3-384">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="8ccb3-384">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="8ccb3-385">Добавляют новые необязательные параметры (Top, ODataQuery и NextLink) для поддержки разбиения на страницы и фильтрации результатов.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-385">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="8ccb3-386">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="8ccb3-386">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="8ccb3-387">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для домена Сетки событий и раздела домена Сетки событий и позволяющие удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-387">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="8ccb3-388">Добавляют новые обязательные параметры для указания имени домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-388">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8ccb3-389">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8ccb3-389">Az.FrontDoor</span></span>
* <span data-ttu-id="8ccb3-390">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="8ccb3-390">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="8ccb3-391">Добавляет поддержку преобразований и новое значение оператора автозавершения (RegEx).</span><span class="sxs-lookup"><span data-stu-id="8ccb3-391">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="8ccb3-392">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="8ccb3-392">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="8ccb3-393">Добавляет новые значения автозавершения.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-393">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ccb3-394">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ccb3-394">Az.Network</span></span>
* <span data-ttu-id="8ccb3-395">Добавляет поддержку ресурса шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-395">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="8ccb3-396">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="8ccb3-396">New cmdlets</span></span>
        - <span data-ttu-id="8ccb3-397">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="8ccb3-397">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="8ccb3-398">Добавляет AvailablePrivateEndpointType.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-398">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="8ccb3-399">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="8ccb3-399">New cmdlets</span></span> 
        - <span data-ttu-id="8ccb3-400">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="8ccb3-400">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="8ccb3-401">Добавляет PrivatePrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-401">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="8ccb3-402">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="8ccb3-402">New cmdlets</span></span> 
        - <span data-ttu-id="8ccb3-403">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8ccb3-403">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="8ccb3-404">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8ccb3-404">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="8ccb3-405">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8ccb3-405">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="8ccb3-406">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="8ccb3-406">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="8ccb3-407">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8ccb3-407">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="8ccb3-408">Добавляет PrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-408">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="8ccb3-409">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="8ccb3-409">New cmdlets</span></span>
        - <span data-ttu-id="8ccb3-410">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8ccb3-410">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="8ccb3-411">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8ccb3-411">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="8ccb3-412">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8ccb3-412">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="8ccb3-413">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="8ccb3-413">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="8ccb3-414">Обновлены следующие команды для функции: флаг UseLocalAzureIpAddress для VPN-подключения.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-414">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="8ccb3-415">Обновлен командлет New-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-415">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="8ccb3-416">Обновлен командлет Set-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-416">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="8ccb3-417">В пиринг ExpressRoute добавлено поле только для чтения PeeredConnections.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-417">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="8ccb3-418">В ExpressRoute добавлено поле только для чтения GlobalReachEnabled.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-418">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="8ccb3-419">Добавлен атрибут в рамках критического изменения, отменяющего статус устаревшего поля AllowGlobalReach в модели ExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-419">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="8ccb3-420">Исправлена проблема, связанная с ошибкой 8756, при использовании TargetListenerID с командлетами AzApplicationGatewayRedirectConfiguration.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-420">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="8ccb3-421">Исправлена ошибка в New-AzApplicationGatewayPathRuleConfig, не позволявшая задавать набор правил повторного создания.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-421">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="8ccb3-422">Исправлено отображение VirtualNetworkTaps в NetworkInterfaceIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-422">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="8ccb3-423">Исправлены командлеты Cortex Get для отображения всех частей.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-423">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="8ccb3-424">Исправлено создание ссылок VirtualHub для ExpressRouteGateways и VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-424">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="8ccb3-425">В AzureFirewall и NatGateway добавлена поддержка Зон доступности.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-425">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="8ccb3-426">Добавлен командлет Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-426">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="8ccb3-427">Добавлена поддержка нескольких общедоступных IP-адресов для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-427">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="8ccb3-428">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="8ccb3-428">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="8ccb3-429">Добавлен параметр -PublicIpAddress, который принимает один или несколько объектов общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-429">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="8ccb3-430">Добавлен параметр -VirtualNetwork, который принимает объект виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-430">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="8ccb3-431">Добавлены методы AddPublicIpAddress и RemovePublicIpAddress для объекта брандмауэра. Они принимают объект общедоступного IP-адреса в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-431">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="8ccb3-432">Не рекомендуется использовать параметры -PublicIpName и -VirtualNetworkName.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-432">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="8ccb3-433">Обновлены следующие команды для функции: В параметрах проверки подлинности AAD VPN-клиента задан ресурс шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-433">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="8ccb3-434">Обновлен командлет New-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-434">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="8ccb3-435">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-435">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="8ccb3-436">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр-переключатель RemoveAadAuthentication для удаления в шлюзе параметров проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-436">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8ccb3-437">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8ccb3-437">Az.OperationalInsights</span></span>
* <span data-ttu-id="8ccb3-438">Добавлена поддержка SKU **pergb2018** в команде New-AzureRmOperationalInsightsWorkspace.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-438">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ccb3-439">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ccb3-439">Az.Resources</span></span>
* <span data-ttu-id="8ccb3-440">Поддержка дополнительных вариантов экспорта шаблона.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-440">Support for additional Template Export options</span></span>
    - <span data-ttu-id="8ccb3-441">В Export-AzResourceGroup добавлен параметр -SkipResourceNameParameterization.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-441">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="8ccb3-442">В Export-AzResourceGroup добавлен параметр -SkipAllParameterization.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-442">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="8ccb3-443">В Export-AzResourceGroup добавлен параметр -Resource для фильтрации экспортированных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-443">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8ccb3-444">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8ccb3-444">Az.ServiceFabric</span></span>
* <span data-ttu-id="8ccb3-445">Исправлена ошибка, связанная с получением иногда неправильных отпечатков при добавлении сертификата ByExistingKeyVault.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-445">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ccb3-446">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ccb3-446">Az.Sql</span></span>
* <span data-ttu-id="8ccb3-447">Исправлен суффикс конечной точки хранилища службы "Расширенная защита от угроз Azure".</span><span class="sxs-lookup"><span data-stu-id="8ccb3-447">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="8ccb3-448">Исправлена ошибка, связанная с возможностью пакета "Расширенная защита данных" переопределять политику службы "Расширенная защита от угроз".</span><span class="sxs-lookup"><span data-stu-id="8ccb3-448">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="8ccb3-449">Новые командлеты для Management.Sql позволяют клиентам добавлять ключи TDE и задавать средство защиты TDE для управляемых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-449">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="8ccb3-450">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8ccb3-450">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="8ccb3-451">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8ccb3-451">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="8ccb3-452">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8ccb3-452">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="8ccb3-453">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="8ccb3-453">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="8ccb3-454">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="8ccb3-454">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8ccb3-455">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8ccb3-455">Az.Storage</span></span>
* <span data-ttu-id="8ccb3-456">Поддержка класса Kind в FileStorage и значения Premium_ZRS в SkuName при создании учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-456">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="8ccb3-457">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8ccb3-457">New-AzStorageAccount</span></span>
* <span data-ttu-id="8ccb3-458">Уточнено описание командлета неизменности BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-458">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="8ccb3-459">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="8ccb3-459">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8ccb3-460">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8ccb3-460">Az.Websites</span></span>
* <span data-ttu-id="8ccb3-461">Оптимизирует Get-AzWebAppCertificate для фильтрации по группе ресурсов на сервере, а не в клиенте.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-461">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="8ccb3-462">Добавляет параметр-переключатель - UseDisasterRecovery в Get AzWebAppSnapshot.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-462">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="8ccb3-463">2.2.0 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-463">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="8ccb3-464">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8ccb3-464">Az.Cdn</span></span>
* <span data-ttu-id="8ccb3-465">Обновлены командлеты для поддержки функции rulesEngine на основе API версии 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-465">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ccb3-466">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ccb3-466">Az.Compute</span></span>
* <span data-ttu-id="8ccb3-467">Добавлен параметр `NoWait`, который запускает операцию и немедленно возвращает значение еще до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-467">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="8ccb3-468">Обновлены командлеты:   Export-AzLogAnalyticRequestRateByInterval; Export-AzLogAnalyticThrottledRequest; Remove-AzVM; Remove-AzVMAccessExtension; Remove-AzVMAEMExtension; Remove-AzVMChefExtension; Remove-AzVMCustomScriptExtension; Remove-AzVMDiagnosticsExtension; Remove-AzVMDiskEncryptionExtension; Remove-AzVMDscExtension; Remove-AzVMSqlServerExtension; Restart-AzVM; Set-AzVM; Set-AzVMAccessExtension; Set-AzVMADDomainExtension; Set-AzVMAEMExtension; Set-AzVMBginfoExtension; Set-AzVMChefExtension; Set-AzVMCustomScriptExtension; Set-AzVMDiagnosticsExtension; Set-AzVMDscExtension; Set-AzVMExtension; Start-AzVM; Stop-AzVM; Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-468">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8ccb3-469">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8ccb3-469">Az.EventHub</span></span>
* <span data-ttu-id="8ccb3-470">Исправлена ошибка № 9231. Командлет Get-AzEventHubNamespace не возвращал теги.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-470">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="8ccb3-471">Исправлена ошибка № 9230. Командлет Get-AzEventHubNamespace возвращал значение ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-471">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ccb3-472">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ccb3-472">Az.Network</span></span>
* <span data-ttu-id="8ccb3-473">Обновлены параметры ResourceId и InputObject для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-473">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="8ccb3-474">Добавлены псевдонимы для параметров ResourceId и InputObject.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-474">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8ccb3-475">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8ccb3-475">Az.PolicyInsights</span></span>
* <span data-ttu-id="8ccb3-476">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyEvent.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-476">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8ccb3-477">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8ccb3-477">Az.RecoveryServices</span></span>
* <span data-ttu-id="8ccb3-478">Минимальный срок хранения политики IaaSVM изменился с 1 до 7 дней.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-478">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8ccb3-479">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8ccb3-479">Az.ServiceBus</span></span>
* <span data-ttu-id="8ccb3-480">Исправлена ошибка № 9182. Командлет Get-AzServiceBusNamespace возвращал ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-480">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8ccb3-481">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8ccb3-481">Az.ServiceFabric</span></span>
* <span data-ttu-id="8ccb3-482">Исправлена опечатка в сообщении об ошибке для командлета Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-482">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="8ccb3-483">Исправлен отсутствующей символ в командных строках Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-483">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ccb3-484">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ccb3-484">Az.Sql</span></span>
* <span data-ttu-id="8ccb3-485">Для командлета New-AzureSqlInstance добавлен параметр DnsZonePartner, обеспечивающий поддержку AutoDr для Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-485">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="8ccb3-486">Командлет Get-AzSqlDatabaseSecureConnectionPolicy объявлен неподдерживаемым.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-486">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="8ccb3-487">Командлеты обнаружения угроз переименованы в командлеты Расширенной защиты от угроз.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-487">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="8ccb3-488">Параметры -StorageSizeInGB и -LicenseType командлета New-AzSqlInstance теперь необязательны.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-488">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8ccb3-489">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8ccb3-489">Az.Websites</span></span>
* <span data-ttu-id="8ccb3-490">Исправлены проблемы, когда удалялись теги при использовании Set-AzWebApp и Set-AzWebAppSlot со свойством -WebApp.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-490">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="8ccb3-491">2.1.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-491">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="8ccb3-492">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8ccb3-492">Az.ApiManagement</span></span>
* <span data-ttu-id="8ccb3-493">Созданы командлеты для управления диагностикой в глобальной области и в области API.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-493">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="8ccb3-494">**Get-AzApiManagementDiagnostic** — получение диагностики, заданной глобально или на уровне области API.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-494">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="8ccb3-495">**New-AzApiManagementDiagnostic** — создание диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-495">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="8ccb3-496">**New-AzApiManagementHttpMessageDiagnostic** — создание параметра диагностики, для которого регистрируются заголовки и размер байтов тела.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-496">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="8ccb3-497">**New-AzApiManagementPipelineDiagnosticSetting** — создание параметров диагностики для сообщений HTTP, поступающих в шлюз или исходящих из него.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-497">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="8ccb3-498">**New-AzApiManagementSamplingSetting** — создание параметра выборки для запросов и ответов касательно диагностики.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-498">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="8ccb3-499">**Remove-AzApiManagementDiagnostic** — удаление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-499">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="8ccb3-500">**Set-AzApiManagementDiagnostic** — обновление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-500">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="8ccb3-501">Созданы командлеты для управления кэшем в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-501">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="8ccb3-502">**Get-AzApiManagementCache** — получение сведений о кэше, указанном идентификатором, или обо всех кэшах.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-502">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="8ccb3-503">**New-AzApiManagementCache** — создание кэша по умолчанию или кэша в определенном регионе Azure.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-503">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="8ccb3-504">**Remove-AzApiManagementCache** — удаление кэша.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-504">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="8ccb3-505">**Update-AzApiManagementCache** — обновление кэша.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-505">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="8ccb3-506">Созданы командлеты для управления схемой API.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-506">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="8ccb3-507">**New-AzApiManagementSchema** — создание схемы для API.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-507">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="8ccb3-508">**Get-AzApiManagementSchema** — получение схем, настроенных в API.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-508">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="8ccb3-509">**Remove-AzApiManagementSchema** — удаление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-509">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="8ccb3-510">**Set-AzApiManagementSchema** — обновление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-510">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="8ccb3-511">Создан командлет для создания токена пользователя.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-511">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="8ccb3-512">**New-AzApiManagementUserToken** — создание токена пользователя, по умолчанию действительного в течение 8 часов. С помощью этого командлета можно создавать токен для пользователя GIT.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-512">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="8ccb3-513">Создан командлет для получения состояния сети.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-513">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="8ccb3-514">**Get-AzApiManagementNetworkStatus** — получение состояния сети ресурсов, от которых зависит служба "Управление API".</span><span class="sxs-lookup"><span data-stu-id="8ccb3-514">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="8ccb3-515">Это полезно при развертывании службы ApiManagement в виртуальной сети и проверке того, не нарушена ли какая-либо из зависимостей.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-515">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="8ccb3-516">Обновлен командлет **New-AzApiManagement** для управления службой ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-516">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="8ccb3-517">Добавлена поддержка нового SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-517">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="8ccb3-518">Добавлена поддержка для включения флага EnableClientCertificate в SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-518">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="8ccb3-519">Новый командлет **New-AzApiManagementSslSetting** позволяет настраивать параметр TLS/SSL для сервера (Backend) и внешнего интерфейса (Frontend).</span><span class="sxs-lookup"><span data-stu-id="8ccb3-519">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="8ccb3-520">Его также можно использовать для настройки Ciphers как 3DES, в ServerProtocols как Http2 для внешнего интерфейса (Frontend) службы ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-520">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="8ccb3-521">Добавлена поддержка настройки имени узла DeveloperPortal в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-521">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="8ccb3-522">Обновлен командлет **Get-AzApiManagementSsoToken** для извлечения объекта PsApiManagement в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-522">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="8ccb3-523">Обновлен командлет для отображения встроенных сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-523">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="8ccb3-524">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Код ошибки: ValidationError. Сообщение об ошибке: "Некоторые поля содержат неправильные значения". Сведения об ошибке: [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="8ccb3-524">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="8ccb3-525">Обновлен командлет **Export-AzApiManagementApi** для экспортирования программных интерфейсов в формате OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-525">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="8ccb3-526">Обновлен командлет **Import-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="8ccb3-526">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="8ccb3-527">Для импортирования API из спецификации документа OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-527">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="8ccb3-528">Для переопределения свойства PsApiManagementSchema, указанного в любом документе (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="8ccb3-528">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="8ccb3-529">Для переопределения свойства ServiceUrl, указанного в любом документе.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-529">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="8ccb3-530">Обновлен командлет **Get-AzApiManagementPolicy** для возврата политики в формате, экранированном не для XML, с использованием rawxml.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-530">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="8ccb3-531">Обновлен командлет **Set-AzApiManagementPolicy**. Он принимает политику в формате, экранированном не для XML, с использованием rawxml и в формате, экранированном для XML, с использованием XML.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-531">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="8ccb3-532">Обновлен командлет **New-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="8ccb3-532">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="8ccb3-533">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-533">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="8ccb3-534">Для создания API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-534">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="8ccb3-535">Для клонирования API с использованием значений SourceApiId и SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-535">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="8ccb3-536">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-536">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="8ccb3-537">Обновлен командлет **Set-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="8ccb3-537">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="8ccb3-538">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-538">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="8ccb3-539">Для обновления API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-539">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="8ccb3-540">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-540">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="8ccb3-541">Обновлен командлет **New-AzApiManagementRevision**:</span><span class="sxs-lookup"><span data-stu-id="8ccb3-541">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="8ccb3-542">Для клонирования (копирования тегов, продуктов, операций и политик) существующей редакции с использованием SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-542">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="8ccb3-543">Новая редакция предполагает родительский идентификатор ApiId.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-543">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="8ccb3-544">Для предоставления ApiRevisionDescription.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-544">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="8ccb3-545">Для переопределения значения ServiceUrl при клонировании API.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-545">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="8ccb3-546">Обновлен командлет **New-AzApiManagementIdentityProvider**:</span><span class="sxs-lookup"><span data-stu-id="8ccb3-546">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="8ccb3-547">Для настройки AAD или AADB2C с Authority.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-547">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="8ccb3-548">Для установки политик SignupPolicy, SigninPolicy, ProfileEditingPolicy и PasswordResetPolicy.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-548">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="8ccb3-549">Обновлен командлет **New-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-549">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="8ccb3-550">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-550">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="8ccb3-551">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-551">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="8ccb3-552">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-552">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="8ccb3-553">Обновлен командлет **Set-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-553">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="8ccb3-554">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-554">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="8ccb3-555">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-555">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="8ccb3-556">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-556">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="8ccb3-557">Следующие командлеты обновлены, чтобы принимать значение ResourceId в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-557">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="8ccb3-558">New-AzApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-558">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="8ccb3-559">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="8ccb3-559">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="8ccb3-560">Get-AzApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-560">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="8ccb3-561">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="8ccb3-561">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="8ccb3-562">Get-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-562">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="8ccb3-563">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="8ccb3-563">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="8ccb3-564">Get-AzApiManagementAuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-564">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="8ccb3-565">Get-AzApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-565">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="8ccb3-566">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="8ccb3-566">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="8ccb3-567">Get-AzApiManagementCertificate.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-567">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="8ccb3-568">Remove-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-568">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="8ccb3-569">Remove-AzApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-569">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8ccb3-570">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8ccb3-570">Az.Automation</span></span>
* <span data-ttu-id="8ccb3-571">Обновлен командлет Get-AzAutomationJobOutputRecord для обработки значений в формате JSON и в виде текстовой записи.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-571">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="8ccb3-572">исправлена проблема https://github.com/Azure/azure-powershell/issues/7977.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-572">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="8ccb3-573">исправлена проблема https://github.com/Azure/azure-powershell/issues/8600.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-573">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="8ccb3-574">Поведение командлета Start-AzAutomationDscCompilationJob изменено так, чтобы сразу же запустить задание, а не ждать его завершения.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-574">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="8ccb3-575">исправлена проблема https://github.com/Azure/azure-powershell/issues/8347.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-575">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="8ccb3-576">Исправлен командлет Get-AzAutomationDscNode, возвращающий все узлы при использовании -Name.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-576">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="8ccb3-577">Теперь он возвращает только соответствующий узел.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-577">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ccb3-578">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ccb3-578">Az.Compute</span></span>
* <span data-ttu-id="8ccb3-579">Добавлены параметры ProtectFromScaleIn и ProtectFromScaleSetAction для командлета Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-579">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="8ccb3-580">Командлет New-AzVM с простым набором параметров теперь по умолчанию использует доступное расположение, если регион "восточная часть США" не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-580">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8ccb3-581">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8ccb3-581">Az.DataLakeStore</span></span>
* <span data-ttu-id="8ccb3-582">Обновлен пакет SDK ADLS для использования httpclient. В инфраструктуру Azure интегрирована проверка плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-582">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8ccb3-583">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8ccb3-583">Az.Monitor</span></span>
* <span data-ttu-id="8ccb3-584">Исправлены неправильные имена параметров в справочных примерах.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-584">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ccb3-585">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ccb3-585">Az.Network</span></span>
* <span data-ttu-id="8ccb3-586">Добавлен флаг DisableBgpRoutePropagation для выходных данных действующей таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-586">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="8ccb3-587">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="8ccb3-587">Updated cmdlet:</span></span>
        - <span data-ttu-id="8ccb3-588">Get-AzEffectiveRouteTable.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-588">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="8ccb3-589">Исправлен двойной дефис в документации New-AzApplicationGatewayTrustedRootCertificate.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-589">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ccb3-590">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ccb3-590">Az.Resources</span></span>
* <span data-ttu-id="8ccb3-591">Добавлен новый командлет Get-AzureRmDenyAssignment для получения запрещающих назначений.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-591">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ccb3-592">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ccb3-592">Az.Sql</span></span>
* <span data-ttu-id="8ccb3-593">Командлеты Расширенной защиты от угроз переименованы на командлеты Расширенной защиты данных, и оценка уязвимости включена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-593">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="8ccb3-594">2.0.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-594">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8ccb3-595">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ccb3-595">Az.Accounts</span></span>
* <span data-ttu-id="8ccb3-596">Обновлена библиотека аутентификации для устранения проблем с ADFS при использовании аутентификации на основе имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-596">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8ccb3-597">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8ccb3-597">Az.CognitiveServices</span></span>
* <span data-ttu-id="8ccb3-598">Отображается только заявление об отказе Bing для служб Поиска Bing.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-598">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="8ccb3-599">Исправлена проблема с созданием учетной записи.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-599">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ccb3-600">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ccb3-600">Az.Compute</span></span>
* <span data-ttu-id="8ccb3-601">Функция группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-601">Proximity placement group feature.</span></span>
    - <span data-ttu-id="8ccb3-602">Добавлены следующие новые командлеты:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="8ccb3-602">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="8ccb3-603">Новый параметр ProximityPlacementGroupId будет добавлен в следующие командлеты:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="8ccb3-603">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="8ccb3-604">В командлет New-AzGalleryImageVersion добавлен параметр StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-604">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="8ccb3-605">TargetRegion в командлете New-AzGalleryImageVersion может содержать StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-605">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="8ccb3-606">Параметр-переключатель SkipShutdown добавлен в командлеты Stop-AzVM и Stop-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-606">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="8ccb3-607">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="8ccb3-607">Breaking changes</span></span>
    - <span data-ttu-id="8ccb3-608">Командлет SET-AzVMBootDiagnostics изменен на Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-608">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="8ccb3-609">Командлет Export-AzLogAnalyticThrottledRequests изменен на Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-609">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="8ccb3-610">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="8ccb3-610">Az.DeploymentManager</span></span>
* <span data-ttu-id="8ccb3-611">Первая общедоступная версия командлетов диспетчера развертывания Azure</span><span class="sxs-lookup"><span data-stu-id="8ccb3-611">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="8ccb3-612">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="8ccb3-612">Az.Dns</span></span>
* <span data-ttu-id="8ccb3-613">Автоматическое делегирование DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="8ccb3-613">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="8ccb3-614">Командлет для создания зоны DNS принимает имя родительской зоны в качестве дополнительного необязательного параметра.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-614">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="8ccb3-615">Он добавляет записи NS в родительской зоне для созданной дочерней зоны.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-615">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8ccb3-616">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8ccb3-616">Az.FrontDoor</span></span>
* <span data-ttu-id="8ccb3-617">Первая общедоступная версия командлетов Azure FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-617">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="8ccb3-618">Переименованы командлеты WAF для включения Waf.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-618">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="8ccb3-619">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8ccb3-619">Az.HDInsight</span></span>
* <span data-ttu-id="8ccb3-620">Удалены два командлета:</span><span class="sxs-lookup"><span data-stu-id="8ccb3-620">Removed two cmdlets:</span></span>
    - <span data-ttu-id="8ccb3-621">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="8ccb3-621">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="8ccb3-622">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="8ccb3-622">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="8ccb3-623">Добавлен новый командлет Set-AzHDInsightGatewayCredential для замены Grant-AzHDInsightHttpServicesAccess.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-623">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="8ccb3-624">Обновлен командлет Get-AzHDInsightJobOutput для различения ролей читателя и оператора HDInsight:</span><span class="sxs-lookup"><span data-stu-id="8ccb3-624">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="8ccb3-625">Пользователям с ролью читателя не нужно указывать параметр DefaultStorageAccountKey явным образом, иначе возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-625">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="8ccb3-626">На пользователей с ролью оператора HDInsight это не повлияет.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-626">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8ccb3-627">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8ccb3-627">Az.Monitor</span></span>
* <span data-ttu-id="8ccb3-628">Новые командлеты для API SQR (запланированное правило запросов)</span><span class="sxs-lookup"><span data-stu-id="8ccb3-628">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="8ccb3-629">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="8ccb3-629">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="8ccb3-630">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="8ccb3-630">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="8ccb3-631">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="8ccb3-631">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="8ccb3-632">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="8ccb3-632">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="8ccb3-633">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="8ccb3-633">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="8ccb3-634">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="8ccb3-634">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="8ccb3-635">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8ccb3-635">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8ccb3-636">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8ccb3-636">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8ccb3-637">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8ccb3-637">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8ccb3-638">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8ccb3-638">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8ccb3-639">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8ccb3-639">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8ccb3-640">См. подробнее об [API SQR](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules).</span><span class="sxs-lookup"><span data-stu-id="8ccb3-640">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="8ccb3-641">Обновлен файл Az.Monitor.md для включения командлетов для правила генерации оповещений на основе метрик GenV2(не классическая версия).</span><span class="sxs-lookup"><span data-stu-id="8ccb3-641">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ccb3-642">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ccb3-642">Az.Network</span></span>
* <span data-ttu-id="8ccb3-643">Добавлена поддержка для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-643">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="8ccb3-644">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="8ccb3-644">New cmdlets</span></span>
        - <span data-ttu-id="8ccb3-645">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="8ccb3-645">New-AzNatGateway</span></span>
        - <span data-ttu-id="8ccb3-646">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="8ccb3-646">Get-AzNatGateway</span></span>
        - <span data-ttu-id="8ccb3-647">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="8ccb3-647">Set-AzNatGateway</span></span>
        - <span data-ttu-id="8ccb3-648">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="8ccb3-648">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="8ccb3-649">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="8ccb3-649">Updated cmdlets</span></span>
        - <span data-ttu-id="8ccb3-650">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="8ccb3-650">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="8ccb3-651">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="8ccb3-651">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="8ccb3-652">Обновлены следующие команды для функции: Настройка и удаление пользовательских маршрутов через шлюз в Бруклине.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-652">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="8ccb3-653">Обновлен командлет New-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-653">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="8ccb3-654">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-654">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8ccb3-655">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8ccb3-655">Az.PolicyInsights</span></span>
* <span data-ttu-id="8ccb3-656">Добавлена поддержка сведений об оценке политики запросов.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-656">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="8ccb3-657">Добавлен параметр -Expand в командлет Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-657">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="8ccb3-658">Добавлена поддержка -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-658">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8ccb3-659">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8ccb3-659">Az.RecoveryServices</span></span>
* <span data-ttu-id="8ccb3-660">Добавлена поддержка перекрестной подписки на Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-660">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="8ccb3-661">Добавлена возможность отмечать предстоящие критически важные изменения для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-661">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="8ccb3-662">Исправлены план восстановления и план действий для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-662">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="8ccb3-663">Исправлено сетевое сопоставление обновления Azure Site Recovery (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="8ccb3-663">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="8ccb3-664">Исправлено направление защиты обновления Azure Site Recovery для управляемых дисков (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="8ccb3-664">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="8ccb3-665">Добавлены другие незначительные исправления.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-665">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="8ccb3-666">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="8ccb3-666">Az.Relay</span></span>
* <span data-ttu-id="8ccb3-667">Исправлены опечатки в сообщениях для клиентов.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-667">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8ccb3-668">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8ccb3-668">Az.ServiceBus</span></span>
* <span data-ttu-id="8ccb3-669">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-669">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8ccb3-670">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8ccb3-670">Az.Storage</span></span>
* <span data-ttu-id="8ccb3-671">Выполнено обновление клиентской библиотеки хранилища до версии 10.0.1 (пространство имен всех объектов из этого пакета SDK изменено с Microsoft.WindowsAzure.Storage. *на Microsoft.Azure.Storage*).</span><span class="sxs-lookup"><span data-stu-id="8ccb3-671">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="8ccb3-672">Выполнено обновление до Microsoft.Azure.Management.Storage версии 11.0.0 для включения поддержки нового API версии 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-672">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="8ccb3-673">Значение свойства Kind по умолчанию в учетной записи хранения изменено со Storage на StorageV2.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-673">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="8ccb3-674">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8ccb3-674">New-AzStorageAccount</span></span>
* <span data-ttu-id="8ccb3-675">Изменено значение Sku.Name в выходных данных командлета учетной записи хранения в соответствии со значением Sku.Name во входных данных путем добавления _ (например, StandardLRS изменено на Standard_LRS).</span><span class="sxs-lookup"><span data-stu-id="8ccb3-675">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="8ccb3-676">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8ccb3-676">New-AzStorageAccount</span></span>
    - <span data-ttu-id="8ccb3-677">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8ccb3-677">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="8ccb3-678">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8ccb3-678">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8ccb3-679">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8ccb3-679">Az.Websites</span></span>
* <span data-ttu-id="8ccb3-680">Свойство Kind теперь будет задаваться объектам PSSite, возвращаемым командлетом Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-680">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="8ccb3-681">Get-AzWebApp\*Metrics и Get-AzAppServicePlanMetrics считаются нерекомендуемыми.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-681">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="8ccb3-682">1.8.0 — апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-682">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8ccb3-683">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="8ccb3-683">Highlights since the last major release</span></span>
* <span data-ttu-id="8ccb3-684">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-684">General availability of `Az` module</span></span>
* <span data-ttu-id="8ccb3-685">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="8ccb3-685">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="8ccb3-686">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="8ccb3-686">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="8ccb3-687">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-687">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="8ccb3-688">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-688">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8ccb3-689">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-689">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="8ccb3-690">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="8ccb3-690">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8ccb3-691">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ccb3-691">Az.Accounts</span></span>
* <span data-ttu-id="8ccb3-692">Обновлен командлет Uninstall-AzureRm для правильного удаления модулей в Mac.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-692">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="8ccb3-693">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8ccb3-693">Az.Batch</span></span>
* <span data-ttu-id="8ccb3-694">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-694">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8ccb3-695">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8ccb3-695">Az.Cdn</span></span>
* <span data-ttu-id="8ccb3-696">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-696">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8ccb3-697">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8ccb3-697">Az.CognitiveServices</span></span>
* <span data-ttu-id="8ccb3-698">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-698">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ccb3-699">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ccb3-699">Az.Compute</span></span>
* <span data-ttu-id="8ccb3-700">Устранена проблема с установкой AEM, если в идентификаторах ресурсов дисков группа ресурсов указана в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-700">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="8ccb3-701">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-701">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8ccb3-702">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-702">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8ccb3-703">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8ccb3-703">Az.DataFactory</span></span>
* <span data-ttu-id="8ccb3-704">Добавлены свойства SsisProperties, если NodeCount не имеет значения NULL для управляемой среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-704">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8ccb3-705">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8ccb3-705">Az.DataLakeStore</span></span>
* <span data-ttu-id="8ccb3-706">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-706">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8ccb3-707">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8ccb3-707">Az.EventGrid</span></span>
* <span data-ttu-id="8ccb3-708">Обновлен текст справки для конечной точки, указывающий, что необходимо создать ресурсы, прежде чем использовать командлеты для создания или обновления подписки на события.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-708">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8ccb3-709">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8ccb3-709">Az.EventHub</span></span>
* <span data-ttu-id="8ccb3-710">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-710">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="8ccb3-711">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8ccb3-711">Az.HDInsight</span></span>
* <span data-ttu-id="8ccb3-712">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-712">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8ccb3-713">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8ccb3-713">Az.IotHub</span></span>
* <span data-ttu-id="8ccb3-714">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-714">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8ccb3-715">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8ccb3-715">Az.KeyVault</span></span>
* <span data-ttu-id="8ccb3-716">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-716">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8ccb3-717">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-717">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="8ccb3-718">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="8ccb3-718">Az.MachineLearning</span></span>
* <span data-ttu-id="8ccb3-719">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-719">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="8ccb3-720">Az.Media</span><span class="sxs-lookup"><span data-stu-id="8ccb3-720">Az.Media</span></span>
* <span data-ttu-id="8ccb3-721">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-721">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8ccb3-722">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8ccb3-722">Az.Monitor</span></span>
  * <span data-ttu-id="8ccb3-723">Добавлены новые командлеты для правила генерации оповещений на основе метрик GenV2 (не классических).</span><span class="sxs-lookup"><span data-stu-id="8ccb3-723">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="8ccb3-724">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="8ccb3-724">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="8ccb3-725">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="8ccb3-725">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="8ccb3-726">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="8ccb3-726">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="8ccb3-727">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="8ccb3-727">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="8ccb3-728">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="8ccb3-728">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="8ccb3-729">Обновлен пакет SDK Monitor до предварительной версии 0.22.0.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-729">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ccb3-730">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ccb3-730">Az.Network</span></span>
* <span data-ttu-id="8ccb3-731">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-731">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8ccb3-732">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-732">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="8ccb3-733">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="8ccb3-733">Az.NotificationHubs</span></span>
* <span data-ttu-id="8ccb3-734">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-734">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8ccb3-735">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8ccb3-735">Az.OperationalInsights</span></span>
* <span data-ttu-id="8ccb3-736">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-736">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="8ccb3-737">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="8ccb3-737">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="8ccb3-738">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-738">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8ccb3-739">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8ccb3-739">Az.RecoveryServices</span></span>
* <span data-ttu-id="8ccb3-740">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-740">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8ccb3-741">Обновлен табличный формат для SQL на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-741">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="8ccb3-742">Добавлен альтернативный метод для получения расположения в Общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-742">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="8ccb3-743">Обновлено значение ScheduleRunDays в объекте SchedulePolicy в соответствии с часовым поясом.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-743">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="8ccb3-744">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8ccb3-744">Az.RedisCache</span></span>
* <span data-ttu-id="8ccb3-745">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-745">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ccb3-746">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ccb3-746">Az.Resources</span></span>
* <span data-ttu-id="8ccb3-747">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-747">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ccb3-748">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ccb3-748">Az.Sql</span></span>
* <span data-ttu-id="8ccb3-749">Заменена зависимость от пакета SDK монитора на обычный код.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-749">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="8ccb3-750">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-750">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8ccb3-751">Улучшен процесс классификации нескольких столбцов.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-751">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="8ccb3-752">Добавлены свойства SKU (имя, семейство, производительность SKU) в отклике Get-AzSqlServerServiceObjective, а также по умолчанию задан табличный формат.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-752">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="8ccb3-753">C помощью Get-AzSqlServerServiceObjective теперь можно получать список доступных целевых служб по расположению без необходимости заранее размещать сервер в регионе.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-753">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="8ccb3-754">Поддерживается параметр часового пояса при создании Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-754">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="8ccb3-755">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-755">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8ccb3-756">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8ccb3-756">Az.Websites</span></span>
* <span data-ttu-id="8ccb3-757">Исправлены командлеты Set-AzWebApp и Set-AzWebAppSlot, которые теперь не удаляют теги при выполнении.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-757">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="8ccb3-758">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-758">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8ccb3-759">Обновлен пакет SDK веб-узлов.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-759">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="8ccb3-760">Удалено свойство AdminSiteName из PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-760">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="8ccb3-761">1.7.0 —апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-761">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8ccb3-762">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="8ccb3-762">Highlights since the last major release</span></span>
* <span data-ttu-id="8ccb3-763">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-763">General availability of `Az` module</span></span>
* <span data-ttu-id="8ccb3-764">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="8ccb3-764">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="8ccb3-765">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="8ccb3-765">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="8ccb3-766">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-766">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="8ccb3-767">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-767">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8ccb3-768">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-768">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="8ccb3-769">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="8ccb3-769">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8ccb3-770">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ccb3-770">Az.Accounts</span></span>
* <span data-ttu-id="8ccb3-771">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметр AzureAnalysisServicesEndpointResourceId.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-771">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="8ccb3-772">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8ccb3-772">Az.AnalysisServices</span></span>
* <span data-ttu-id="8ccb3-773">Использование ServiceClient в командлетах плоскости данных и удаление исходной логики проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-773">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="8ccb3-774">Add-AzureASAccount используется как оболочка для Connect-AzAccount во избежание критических изменений.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-774">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8ccb3-775">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8ccb3-775">Az.Automation</span></span>
* <span data-ttu-id="8ccb3-776">Исправлена ошибка командлета New-AzAutomationSoftwareUpdateConfiguration, связанная с включением.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-776">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="8ccb3-777">Теперь параметры IncludedKbNumber и IncludedPackageNameMask должны работать нормально.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-777">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="8ccb3-778">Исправлена ошибка динамической группы управления обновлениями службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-778">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ccb3-779">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ccb3-779">Az.Compute</span></span>
* <span data-ttu-id="8ccb3-780">В командлеты New-AzDiskConfig и New-AzSnapshotConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-780">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="8ccb3-781">Теперь можно создавать виртуальные машину на основе образов из коллекции от других клиентов.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-781">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="8ccb3-782">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8ccb3-782">Az.ContainerInstance</span></span>
* <span data-ttu-id="8ccb3-783">Исправлена проблема в параметре -Command командлета New-AzContainerGroup, из-за которой в конце добавлялся пустой аргумент.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-783">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8ccb3-784">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8ccb3-784">Az.DataFactory</span></span>
* <span data-ttu-id="8ccb3-785">Пакет SDK для ADF .NET обновлен до версии 3.0.2.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-785">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="8ccb3-786">Командлет Set-AzDataFactoryV2 обновлен с помощью дополнительных параметров для настроек, связанных с RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-786">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ccb3-787">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ccb3-787">Az.Resources</span></span>
* <span data-ttu-id="8ccb3-788">Улучшена обработка поставщиков Get-AzResource при предоставлении параметров -ResourceId или -ResourceGroupName, -Name и -ResourceType.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-788">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="8ccb3-789">Улучшена обработка ошибок в командлетах Test-AzDeployment и Test-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-789">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="8ccb3-790">Теперь ошибки, возникающие за пределами проверки развертывания, обрабатываются и включаются в выходные данные команды.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-790">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="8ccb3-791">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-791">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="8ccb3-792">Добавлен параметр-переключатель -IgnoreDynamicParameters, с помощью которого можно настроить командлеты развертывания так, чтобы они пропускали запросы в сценариях скриптов и заданий.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-792">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="8ccb3-793">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-793">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ccb3-794">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ccb3-794">Az.Sql</span></span>
* <span data-ttu-id="8ccb3-795">Поддержка классификации данных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-795">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8ccb3-796">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8ccb3-796">Az.Storage</span></span>
* <span data-ttu-id="8ccb3-797">Подробные сообщения об ошибке передаются при создании контекста хранилища с помощью параметра -UseConnectedAccount, но без входа в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-797">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="8ccb3-798">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="8ccb3-798">New-AzStorageContext</span></span>
* <span data-ttu-id="8ccb3-799">Поддержка свойств службы управления BLOB-объектов в указанной учетной записи хранения с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-799">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="8ccb3-800">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="8ccb3-800">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="8ccb3-801">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="8ccb3-801">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="8ccb3-802">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8ccb3-802">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="8ccb3-803">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8ccb3-803">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="8ccb3-804">Поддержка параметра -AsJob в командлетах для отправки и скачивания больших двоичных объектов и файлов.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-804">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="8ccb3-805">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8ccb3-805">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="8ccb3-806">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8ccb3-806">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="8ccb3-807">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8ccb3-807">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="8ccb3-808">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8ccb3-808">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="8ccb3-809">1.6.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-809">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8ccb3-810">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="8ccb3-810">Highlights since the last major release</span></span>
* <span data-ttu-id="8ccb3-811">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-811">General availability of `Az` module</span></span>
* <span data-ttu-id="8ccb3-812">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="8ccb3-812">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="8ccb3-813">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="8ccb3-813">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="8ccb3-814">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-814">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="8ccb3-815">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-815">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8ccb3-816">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-816">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="8ccb3-817">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="8ccb3-817">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8ccb3-818">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8ccb3-818">Az.Automation</span></span>
* <span data-ttu-id="8ccb3-819">В управление обновлениями службы автоматизации Azure внесены изменения для поддержки следующих новых функций:</span><span class="sxs-lookup"><span data-stu-id="8ccb3-819">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="8ccb3-820">динамическое группирование;</span><span class="sxs-lookup"><span data-stu-id="8ccb3-820">Dynamic grouping</span></span>
    * <span data-ttu-id="8ccb3-821">скрипты предварительного или последующего выполнения;</span><span class="sxs-lookup"><span data-stu-id="8ccb3-821">Pre-Post script</span></span>
    * <span data-ttu-id="8ccb3-822">параметр перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-822">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ccb3-823">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ccb3-823">Az.Compute</span></span>
* <span data-ttu-id="8ccb3-824">Устранена проблема, связанная с разрешением пути в Get-AzVmBootDiagnosticsData.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-824">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="8ccb3-825">Обновление клиентской библиотеки вычислений до версии 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-825">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8ccb3-826">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8ccb3-826">Az.KeyVault</span></span>
* <span data-ttu-id="8ccb3-827">Добавлена поддержка подстановочных знаков в командлетах KeyVault.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-827">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ccb3-828">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ccb3-828">Az.Network</span></span>
* <span data-ttu-id="8ccb3-829">Добавлена поддержка анализа угроз для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-829">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="8ccb3-830">Добавлены настраиваемые правила и ресурс верхнего уровня для политики брандмауэра Шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-830">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8ccb3-831">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8ccb3-831">Az.RecoveryServices</span></span>
* <span data-ttu-id="8ccb3-832">В политику виртуальной машины Azure добавлен объект SnapshotRetentionInDays для поддержки мгновенного восстановления.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-832">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="8ccb3-833">Добавлена поддержка канала для отмены регистрации контейнера.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-833">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ccb3-834">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ccb3-834">Az.Resources</span></span>
* <span data-ttu-id="8ccb3-835">Обновлена поддержка подстановочных знаков для Get-AzResource и Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-835">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="8ccb3-836">Обновлены учетные данные, используемые при общих вызовах к ARM.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-836">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ccb3-837">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ccb3-837">Az.Sql</span></span>
* <span data-ttu-id="8ccb3-838">Изменен тип параметра (ExcludeDetectionType) командлетов для обнаружения угроз с DetectionTypes на string[] для поддержки актуального состояния при добавлении новых типов обнаружения и для поддержки автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-838">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8ccb3-839">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8ccb3-839">Az.Storage</span></span>
* <span data-ttu-id="8ccb3-840">Поддержка получения, настройки и удаления политики управления в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-840">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="8ccb3-841">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="8ccb3-841">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="8ccb3-842">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="8ccb3-842">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="8ccb3-843">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="8ccb3-843">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="8ccb3-844">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="8ccb3-844">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="8ccb3-845">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="8ccb3-845">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="8ccb3-846">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="8ccb3-846">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8ccb3-847">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8ccb3-847">Az.Websites</span></span>
* <span data-ttu-id="8ccb3-848">Исправлена ошибка с шаблоном ARM, из-за которой прерывалось клонирование все слотов при использовании New-AzWebApp -IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-848">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="8ccb3-849">1.5.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-849">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8ccb3-850">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ccb3-850">Az.Accounts</span></span>
* <span data-ttu-id="8ccb3-851">Добавлена команда Register-AzModule для поддержки созданных командлетов AutoRest.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-851">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="8ccb3-852">Обновлены примеры для Connect AzAccount.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-852">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8ccb3-853">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8ccb3-853">Az.Automation</span></span>
* <span data-ttu-id="8ccb3-854">Исправлена проблема с получением некоторых ежемесячных расписаний в нескольких командлетах службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-854">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="8ccb3-855">Исправлен командлет Get-AzAutomationDscNode, возвращающий только первые 20 узлов.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-855">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="8ccb3-856">Теперь он возвращает все узлы.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-856">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8ccb3-857">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8ccb3-857">Az.Cdn</span></span>
* <span data-ttu-id="8ccb3-858">Добавлены новые командлеты PowerShell для включения и отключения HTTPS для личного домена и отключены устаревшие командлеты.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-858">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ccb3-859">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ccb3-859">Az.Compute</span></span>
* <span data-ttu-id="8ccb3-860">Добавлена поддержка подстановочных знаков в командлетах Get.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-860">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8ccb3-861">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8ccb3-861">Az.DataFactory</span></span>
* <span data-ttu-id="8ccb3-862">Обновлен пакет SDK для ADF .NET до версии 3.0.1.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-862">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8ccb3-863">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8ccb3-863">Az.LogicApp</span></span>
* <span data-ttu-id="8ccb3-864">Исправлена проблема с получением только первой страницы результатов при выполнении команды ListWorkflows.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-864">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ccb3-865">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ccb3-865">Az.Network</span></span>
* <span data-ttu-id="8ccb3-866">Добавлена поддержка подстановочных знаков в командлетах Network.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-866">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8ccb3-867">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8ccb3-867">Az.RecoveryServices</span></span>
* <span data-ttu-id="8ccb3-868">Добавлена поддержка SQL Server на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-868">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="8ccb3-869">Обновление пакета SDK</span><span class="sxs-lookup"><span data-stu-id="8ccb3-869">SDK Update</span></span>
* <span data-ttu-id="8ccb3-870">Удалена проверка VMappContainer в Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-870">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="8ccb3-871">Добавлены параметры Name и ServerName для Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-871">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ccb3-872">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ccb3-872">Az.Resources</span></span>
* <span data-ttu-id="8ccb3-873">Добавлен параметр `-TemplateObject` в командлеты для развертывания.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-873">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="8ccb3-874">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2933.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-874">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="8ccb3-875">Устранена проблема с передачей в конвейер результата `Get-AzResource` для `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-875">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="8ccb3-876">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8240.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-876">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="8ccb3-877">Устранена проблема с изменением типа данных JSON при выполнении `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-877">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="8ccb3-878">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7930.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-878">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ccb3-879">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ccb3-879">Az.Sql</span></span>
* <span data-ttu-id="8ccb3-880">Обновление AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-880">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="8ccb3-881">Исправлено поведение для пограничного случая при создании параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-881">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8ccb3-882">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8ccb3-882">Az.Storage</span></span>
* <span data-ttu-id="8ccb3-883">Включена поддержка Kind BlockBlobStorage при создании учетной записи хранения для New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-883">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="8ccb3-884">1.4.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-884">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="8ccb3-885">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8ccb3-885">Az.AnalysisServices</span></span>
* <span data-ttu-id="8ccb3-886">Командлет AddAzureASAccount устарел.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-886">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8ccb3-887">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8ccb3-887">Az.Automation</span></span>
* <span data-ttu-id="8ccb3-888">Обновлена справка для командлета Import-AzAutomationDscNodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-888">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="8ccb3-889">Добавлена проверка имени конфигурации для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-889">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="8ccb3-890">Улучшена обработка ошибок для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-890">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8ccb3-891">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8ccb3-891">Az.CognitiveServices</span></span>
* <span data-ttu-id="8ccb3-892">Добавлен параметр CustomSubdomainName — новый необязательный параметр для командлета New-AzCognitiveServicesAccount, который указывает поддомен для ресурса.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-892">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ccb3-893">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ccb3-893">Az.Compute</span></span>
* <span data-ttu-id="8ccb3-894">Устранена проблема с идентификаторами наборов параметров.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-894">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="8ccb3-895">Обновлен командлет Get-AzVMExtension для отображения списка всех установленных расширений, если не указан параметр Name.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-895">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="8ccb3-896">Для командлета Update-AzImage добавлены параметры Tag и ResourceId.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-896">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="8ccb3-897">Командлет Get-AzVmssVM, который выполняется без указания идентификатора экземпляра и с параметром InstanceView, может выводить виртуальные машины из VMSS с представлением экземпляра.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-897">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8ccb3-898">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8ccb3-898">Az.DataLakeStore</span></span>
* <span data-ttu-id="8ccb3-899">Добавлены командлеты для перечисления и восстановления удаленного элемента ADL.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-899">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8ccb3-900">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8ccb3-900">Az.EventHub</span></span>
* <span data-ttu-id="8ccb3-901">Добавлено новое логическое свойство SkipEmptyArchives для пропуска пустых архивов в классе CaptureDescription Eventhub.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-901">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="8ccb3-902">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8ccb3-902">Az.KeyVault</span></span>
* <span data-ttu-id="8ccb3-903">Исправлена расстановка тегов для командлета Set-AzKeyVaultSecret.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-903">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8ccb3-904">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8ccb3-904">Az.LogicApp</span></span>
* <span data-ttu-id="8ccb3-905">Добавлен SKU "Базовый" для учетных записей интеграции.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-905">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="8ccb3-906">Добавлены типы сопоставлений Liquid, а также XSLT 2.0 и XSLT 3.0.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-906">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="8ccb3-907">Новые командлеты для сборок учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="8ccb3-907">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="8ccb3-908">Get-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="8ccb3-908">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="8ccb3-909">New-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="8ccb3-909">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="8ccb3-910">Remove-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="8ccb3-910">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="8ccb3-911">Set-AzIntegrationAccountAssembly.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-911">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="8ccb3-912">Новые командлеты для конфигурации пакета учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="8ccb3-912">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="8ccb3-913">Get-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="8ccb3-913">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="8ccb3-914">New-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="8ccb3-914">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="8ccb3-915">Remove-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="8ccb3-915">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="8ccb3-916">Set-AzIntegrationAccountBatchConfiguration.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-916">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="8ccb3-917">Обновлен пакет SDK Logic Apps до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-917">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8ccb3-918">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8ccb3-918">Az.Monitor</span></span>
* <span data-ttu-id="8ccb3-919">Обновлена справка для командлета Get-AzMetric.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-919">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ccb3-920">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ccb3-920">Az.Network</span></span>
* <span data-ttu-id="8ccb3-921">Обновлен пример справки для командлета Add-AzApplicationGatewayCustomError.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-921">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8ccb3-922">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8ccb3-922">Az.OperationalInsights</span></span>
* <span data-ttu-id="8ccb3-923">Дополнительная поддержка создания и получения источников данных ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-923">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="8ccb3-924">Добавлен новый тип ApplicationInsights для получения определенных или всех источников данных ApplicationInsights для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-924">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="8ccb3-925">Добавлен командлет New-AzOperationalInsightsApplicationInsightsDataSource для создания источника данных с использованием параметров указанного ресурса Application-Insightss: subscription Id, resourceGroupName и name.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-925">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="8ccb3-926">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ccb3-926">Az.Resources</span></span>
* <span data-ttu-id="8ccb3-927">исправлена проблема https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-927">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="8ccb3-928">исправлена проблема https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-928">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="8ccb3-929">исправлена проблема https://github.com/Azure/azure-powershell/issues/6219.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-929">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="8ccb3-930">Исправлена ошибка, препятствующая повторному созданию KeyCredentials.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-930">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ccb3-931">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ccb3-931">Az.Sql</span></span>
* <span data-ttu-id="8ccb3-932">Добавлена поддержка уровня гипермасштабирования в базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-932">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="8ccb3-933">Исправлена ошибка, из-за которой восстановление могло завершиться со сбоем при указании ненужных свойств в запросе на восстановление.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-933">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8ccb3-934">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8ccb3-934">Az.Websites</span></span>
* <span data-ttu-id="8ccb3-935">Исправлен пример для командлета Get-AzWebAppSlotMetrics.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-935">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="8ccb3-936">1.3.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-936">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8ccb3-937">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ccb3-937">Az.Accounts</span></span>
* <span data-ttu-id="8ccb3-938">Обновление до последней версии ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="8ccb3-938">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="8ccb3-939">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8ccb3-939">Az.AnalysisServices</span></span>
<span data-ttu-id="8ccb3-940">Общедоступная версия модуля Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-940">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ccb3-941">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ccb3-941">Az.Compute</span></span>
* <span data-ttu-id="8ccb3-942">Расширение AEM: добавлена поддержка дисков UltraSSD, P60, P70 и P80.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-942">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="8ccb3-943">Обновлено описание справки для командлета Set-AzVMBootDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-943">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="8ccb3-944">Обновлено описание справки и пример для командлета Update-AzImage.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-944">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8ccb3-945">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8ccb3-945">Az.RecoveryServices</span></span>
<span data-ttu-id="8ccb3-946">Общедоступная версия модуля Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-946">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ccb3-947">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ccb3-947">Az.Resources</span></span>
* <span data-ttu-id="8ccb3-948">Исправлена расстановка тегов для групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-948">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="8ccb3-949">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-949">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="8ccb3-950">Исправлена проблема с игнорированием командлетом `Get-AzureRmRoleAssignment` параметра -ErrorAction.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-950">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="8ccb3-951">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-951">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ccb3-952">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ccb3-952">Az.Sql</span></span>
* <span data-ttu-id="8ccb3-953">Добавлен командлет Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-953">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="8ccb3-954">Исправлена проблема с появлением исключения NullRef при выполнении командлетов SQL, если не выполнен вход в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-954">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="8ccb3-955">Исправлено исключение NullRef в командлете Get-AzSqlCapability.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-955">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="8ccb3-956">1.2.1 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-956">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8ccb3-957">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ccb3-957">Az.Accounts</span></span>
* <span data-ttu-id="8ccb3-958">Выпуск с правильной версией службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-958">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="8ccb3-959">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8ccb3-959">Az.AnalysisServices</span></span>
* <span data-ttu-id="8ccb3-960">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-960">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8ccb3-961">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8ccb3-961">Az.RecoveryServices</span></span>
* <span data-ttu-id="8ccb3-962">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-962">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="8ccb3-963">1.2.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-963">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8ccb3-964">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ccb3-964">Az.Accounts</span></span>
* <span data-ttu-id="8ccb3-965">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-965">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8ccb3-966">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-966">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8ccb3-967">Добавлено предупреждающее сообщение в PS Core для модуля Uninstall-AzureRm.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-967">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="8ccb3-968">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="8ccb3-968">Az.Aks</span></span>
* <span data-ttu-id="8ccb3-969">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-969">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8ccb3-970">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8ccb3-970">Az.Automation</span></span>
* <span data-ttu-id="8ccb3-971">Добавлена поддержка для модулей runbook Python 2.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-971">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="8ccb3-972">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-972">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8ccb3-973">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8ccb3-973">Az.Cdn</span></span>
* <span data-ttu-id="8ccb3-974">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-974">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ccb3-975">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ccb3-975">Az.Compute</span></span>
* <span data-ttu-id="8ccb3-976">Добавлен командлет Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-976">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="8ccb3-977">Добавлен параметр TempDisk к командлету Set-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-977">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="8ccb3-978">Исправлено предупреждающее сообщение командлета New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-978">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="8ccb3-979">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8ccb3-979">Az.ContainerRegistry</span></span>
* <span data-ttu-id="8ccb3-980">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-980">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8ccb3-981">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8ccb3-981">Az.DataFactory</span></span>
* <span data-ttu-id="8ccb3-982">Пакет SDK ADF .Net обновлен до версии 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-982">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8ccb3-983">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8ccb3-983">Az.DataLakeStore</span></span>
* <span data-ttu-id="8ccb3-984">Исправлена проблема с конечной точкой ADLS при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-984">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="8ccb3-985">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7462.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-985">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="8ccb3-986">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-986">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8ccb3-987">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8ccb3-987">Az.IotHub</span></span>
* <span data-ttu-id="8ccb3-988">Добавлен формат кодирования для командлета Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-988">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8ccb3-989">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8ccb3-989">Az.KeyVault</span></span>
* <span data-ttu-id="8ccb3-990">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-990">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ccb3-991">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ccb3-991">Az.Network</span></span>
* <span data-ttu-id="8ccb3-992">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-992">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ccb3-993">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ccb3-993">Az.Resources</span></span>
* <span data-ttu-id="8ccb3-994">Исправлены неправильные примеры в справочной документации по командлетам New-AzADAppCredential и New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-994">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="8ccb3-995">Исправлена проблема, при которой путь для параметра -TemplateFile не удавалось разрешить до выполнения командлетов развертывания групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-995">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="8ccb3-996">Az.Resources: исправлена документация для значения по умолчанию -Mode командлета New-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-996">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="8ccb3-997">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/7522.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-997">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="8ccb3-998">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/5747.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-998">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="8ccb3-999">Исправлена проблема с форматированием объекта PSResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-999">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="8ccb3-1000">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2123.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1000">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8ccb3-1001">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1001">Az.ServiceFabric</span></span>
* <span data-ttu-id="8ccb3-1002">Исправлена проблема с появлением исключения в процессе отката при добавлении сертификата к модели VMSS: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1002">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="8ccb3-1003">Исправлены некоторые сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1003">Fix some error messages.</span></span>
* <span data-ttu-id="8ccb3-1004">Исправлена проблема с созданием кластера с шаблоном ARM по умолчанию для командлета New-AzServiceFabriCluster, который не работал с операцией миграции в Az.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1004">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="8ccb3-1005">Исправлена проблема с добавлением сертификата кластера или приложения: теперь они добавляются только в Масштабируемые наборы виртуальных машин, которые сопоставлены с кластером, путем проверки идентификатора кластера в расширении.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1005">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="8ccb3-1006">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1006">Az.SignalR</span></span>
* <span data-ttu-id="8ccb3-1007">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1007">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ccb3-1008">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1008">Az.Sql</span></span>
* <span data-ttu-id="8ccb3-1009">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1009">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8ccb3-1010">Обновлено описание параметра LicenseType с добавлением возможных значений.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1010">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="8ccb3-1011">Исправлена проблема с неправильным обновлением удостоверения управляемого экземпляра, если оно было единственным обновляемым свойством.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1011">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="8ccb3-1012">Поддержка пользовательских параметров сортировки в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1012">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8ccb3-1013">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1013">Az.Storage</span></span>
* <span data-ttu-id="8ccb3-1014">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1014">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8ccb3-1015">Добавлен вывод подробных сообщений об ошибке при получении или установке классических свойств ведения журнала или метрик в учетной записи хранилища класса Premium, так как учетная запись хранилища класса Premium не поддерживает классические функции ведения журнала и метрик.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1015">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="8ccb3-1016">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1016">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="8ccb3-1017">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1017">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="8ccb3-1018">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1018">Az.TrafficManager</span></span>
* <span data-ttu-id="8ccb3-1019">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1019">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8ccb3-1020">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1020">Az.Websites</span></span>
* <span data-ttu-id="8ccb3-1021">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1021">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8ccb3-1022">Исправлена работа командлета New-AzWebAppSSLBinding: сертификат отправляется в правильную группу ресурсов и правильное расположение, если приложение размещено в ASE.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1022">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="8ccb3-1023">Исправлена работа командлета New-AzWebAppSSLBinding: теги не перезаписываются при привязке SSL-сертификата к приложению.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1023">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="8ccb3-1024">1.1.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1024">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8ccb3-1025">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1025">Az.Accounts</span></span>
* <span data-ttu-id="8ccb3-1026">Добавление области "Local" в Enable-AzureRmAlias.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1026">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ccb3-1027">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1027">Az.Compute</span></span>
* <span data-ttu-id="8ccb3-1028">Теперь имя не является обязательным в идентификаторе набора параметров для Restart/Start/Stop/Remove/Set-AzVM и Save-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1028">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="8ccb3-1029">Обновлено описание идентификатора в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1029">Updated the description of ID in help files</span></span>
* <span data-ttu-id="8ccb3-1030">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1030">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8ccb3-1031">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1031">Az.DataLakeStore</span></span>
* <span data-ttu-id="8ccb3-1032">Обновление версии пакета SDK для плоскости данных до 1.1.14 для устранения найденных проблем.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1032">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="8ccb3-1033">Исправлена обработка отрицательного времени доступа и времени изменения для getfilestatus и liststatus, исправлен токен отмены для асинхронных методов.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1033">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8ccb3-1034">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1034">Az.EventGrid</span></span>
* <span data-ttu-id="8ccb3-1035">Обновление для использования API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1035">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="8ccb3-1036">Обновлены указанные ниже командлеты для поддержки нового сценария в API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1036">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="8ccb3-1037">New-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1037">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="8ccb3-1038">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1038">Event Time-To-Live,</span></span>
        - <span data-ttu-id="8ccb3-1039">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1039">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="8ccb3-1040">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1040">Dead letter endpoint.</span></span>
    - <span data-ttu-id="8ccb3-1041">Update-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1041">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="8ccb3-1042">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1042">Event Time-To-Live,</span></span>
        - <span data-ttu-id="8ccb3-1043">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1043">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="8ccb3-1044">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1044">Dead letter endpoint.</span></span>
* <span data-ttu-id="8ccb3-1045">Для параметра EndpointType добавлены новые значения перечисления (storageQueue и hybridConnection) в командлеты New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1045">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="8ccb3-1046">Если ожидается, что создание или обновление подписки на событие повлечет за собой действия со стороны пользователя, выполняемые вручную, отображается предупреждение при создании или обновлении подписки события.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1046">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8ccb3-1047">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1047">Az.IotHub</span></span>
* <span data-ttu-id="8ccb3-1048">Пакет SDK Центра Интернета вещей обновлен до последней версии.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1048">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8ccb3-1049">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1049">Az.LogicApp</span></span>
* <span data-ttu-id="8ccb3-1050">Get-AzLogicApp позволяет перечислить все параметры без указанного имени.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1050">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ccb3-1051">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1051">Az.Resources</span></span>
* <span data-ttu-id="8ccb3-1052">Исправлена проблема с набором параметров при предоставлении параметров "-ODataQuery" и "-ResourceId" для "Get-AzResource".</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1052">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="8ccb3-1053">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7875.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1053">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="8ccb3-1054">Исправлена обработка параметра -Custom в New/Set-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1054">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="8ccb3-1055">Исправлена опечатка в документации по New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1055">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="8ccb3-1056">Параметр "-MailNickname" стал обязательным для "New-AzADUser".</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1056">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="8ccb3-1057">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8220.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1057">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="8ccb3-1058">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1058">Az.SignalR</span></span>
* <span data-ttu-id="8ccb3-1059">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1059">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ccb3-1060">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1060">Az.Sql</span></span>
* <span data-ttu-id="8ccb3-1061">Зависимость клиента управления хранением преобразована для общей реализации в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1061">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8ccb3-1062">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1062">Az.Storage</span></span>
* <span data-ttu-id="8ccb3-1063">Установка параметра StorageAccountName для контекста хранилища в качестве реального имени учетной записи хранения, если она была создана с использованием токена Sas, OAuth или анонимного доступа.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1063">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="8ccb3-1064">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1064">New-AzStorageContext</span></span>
* <span data-ttu-id="8ccb3-1065">Создание токена Sas большого двоичного объекта моментального снимка с параметром "-FullUri". Возвращаемый URI исправлен на URI моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1065">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="8ccb3-1066">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1066">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8ccb3-1067">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1067">Az.Websites</span></span>
* <span data-ttu-id="8ccb3-1068">Исправлена ошибка синтаксического анализа даты в "Get-AzDeletedWebApp".</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1068">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="8ccb3-1069">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1069">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="8ccb3-1070">1.0.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1070">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="8ccb3-1071">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1071">General</span></span>

- <span data-ttu-id="8ccb3-1072">Общедоступная версия модуля Az.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1072">General Availability of Az Module</span></span>
- <span data-ttu-id="8ccb3-1073">Справка в Интернете для каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1073">Online help for each module</span></span>
- <span data-ttu-id="8ccb3-1074">Дополнительные сведения и стратегию развития см. в статье [Announcing New Module 'Az'](https://aka.ms/azps-announce) (Объявление о новом модуле Az)</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1074">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="8ccb3-1075">Сведения о миграции с AzureRM см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1075">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="8ccb3-1076">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1076">Az.Accounts</span></span>
- <span data-ttu-id="8ccb3-1077">Изменено с Az.Profile.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1077">Changed from Az.Profile</span></span>
- <span data-ttu-id="8ccb3-1078">Исправлены форматы таблиц для типов профиля и контекста.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1078">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="8ccb3-1079">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1079">Az.ApiManagement</span></span>
- <span data-ttu-id="8ccb3-1080">Исправления для #7002.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1080">Fixes for #7002</span></span>
- <span data-ttu-id="8ccb3-1081">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1081">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="8ccb3-1082">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1082">Az.Batch</span></span>
- <span data-ttu-id="8ccb3-1083">Добавлена возможность видеть, какая версия агента узла пакетной службы Azure работает в пуле на каждой виртуальной машине, с помощью нового свойства `NodeAgentInformation` в `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1083">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="8ccb3-1084">Значение `Caching` по умолчанию для `PSDataDisk` теперь `ReadWrite` вместо `None`.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1084">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="8ccb3-1085">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1085">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="8ccb3-1086">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1086">Az.Billing</span></span>
- <span data-ttu-id="8ccb3-1087">Объединены командлеты Billing, Consumption и UsageAggregates. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0).</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1087">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="8ccb3-1088">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1088">Az.CognitivServices</span></span>
- <span data-ttu-id="8ccb3-1089">Добавлены средства заполнения для SkuName и Typem, доступные в операции New-AzureRmCognitiveServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1089">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="8ccb3-1090">Удален набор параметров GetSkusWithAccountParamSetName из Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1090">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="8ccb3-1091">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1091">Az.ContainerInstance</span></span>
- <span data-ttu-id="8ccb3-1092">Добавлена поддержка ManagedIdentity.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1092">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="8ccb3-1093">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1093">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="8ccb3-1094">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1094">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="8ccb3-1095">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1095">Az.DataLakeStore</span></span>
- <span data-ttu-id="8ccb3-1096">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1096">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="8ccb3-1097">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1097">Az.Monitor</span></span>
- <span data-ttu-id="8ccb3-1098">"Az.Insights" переименован в "Az.Monitor" и внесены другие незначительные критические изменения. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1098">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="8ccb3-1099">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1099">Az.KeyVault</span></span>
- <span data-ttu-id="8ccb3-1100">Из типов вывода удалено устаревшее свойство PurgeDisabled</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1100">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="8ccb3-1101">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1101">Az.MachineLearning</span></span>
- <span data-ttu-id="8ccb3-1102">Включены командлеты из модуля Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1102">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="8ccb3-1103">Az.Media</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1103">Az.Media</span></span>
- <span data-ttu-id="8ccb3-1104">Удаляет устаревший псевдоним Tags из New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1104">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="8ccb3-1105">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1105">Az.Network</span></span>
<span data-ttu-id="8ccb3-1106">В шлюз приложений добавлена поддержка настройки RewriteRuleSets</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1106">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="8ccb3-1107">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1107">New cmdlets added:</span></span>
        - <span data-ttu-id="8ccb3-1108">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1108">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8ccb3-1109">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1109">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8ccb3-1110">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1110">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8ccb3-1111">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1111">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8ccb3-1112">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1112">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8ccb3-1113">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1113">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="8ccb3-1114">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1114">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="8ccb3-1115">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1115">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="8ccb3-1116">В следующие командлеты добавлен необязательный параметр -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1116">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="8ccb3-1117">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1117">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="8ccb3-1118">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1118">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="8ccb3-1119">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1119">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="8ccb3-1120">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1120">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="8ccb3-1121">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1121">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="8ccb3-1122">New-AzureRmApplicationGatewayUrlPathMapConfig добавил с помощью идентификатора поддержку KeyVault для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1122">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="8ccb3-1123">В следующие командлеты добавлен необязательный параметр -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1123">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="8ccb3-1124">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1124">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="8ccb3-1125">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1125">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="8ccb3-1126">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1126">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="8ccb3-1127">В командлет New-AzApplicationGateway добавлен необязательный параметр -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1127">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="8ccb3-1128">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1128">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="8ccb3-1129">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1129">Az.OperationalInsights</span></span>
- <span data-ttu-id="8ccb3-1130">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1130">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="8ccb3-1131">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1131">Az.Profile</span></span>
- <span data-ttu-id="8ccb3-1132">Имя модуля изменено на Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1132">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="8ccb3-1133">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1133">Az.RecoveryServices</span></span>
- <span data-ttu-id="8ccb3-1134">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1134">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="8ccb3-1135">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1135">Az.Resources</span></span>
- <span data-ttu-id="8ccb3-1136">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1136">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="8ccb3-1137">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1137">Az.ServiceFabric</span></span>
- <span data-ttu-id="8ccb3-1138">Поддержка спецификации сертификата по общему имени и отпечатку</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1138">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="8ccb3-1139">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1139">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="8ccb3-1140">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1140">Az.SIgnalR</span></span>
- <span data-ttu-id="8ccb3-1141">Общедоступная версия командлетов PowerShell для SIgnalR</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1141">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="8ccb3-1142">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1142">Az.Sql</span></span>
- <span data-ttu-id="8ccb3-1143">Добавлены новые типы обнаружения Data_Exfiltration и Unsafe_Action в командлеты обнаружения угроз</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1143">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="8ccb3-1144">Примеры обновленной документации для командлетов аудита Sql</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1144">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="8ccb3-1145">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1145">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="8ccb3-1146">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1146">Az.Storage</span></span>
- <span data-ttu-id="8ccb3-1147">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1147">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="8ccb3-1148">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1148">Az.Websites</span></span>
- <span data-ttu-id="8ccb3-1149">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1149">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="8ccb3-1150">0.7.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1150">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="8ccb3-1151">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1151">General</span></span>

* <span data-ttu-id="8ccb3-1152">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1152">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="8ccb3-1153">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1153">Az.Compute</span></span>

* <span data-ttu-id="8ccb3-1154">Добавлена поддержка UltraSSD и образов коллекции в простых наборах параметров для командлетов `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1154">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="8ccb3-1155">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1155">Az.DataLakeStore</span></span>

* <span data-ttu-id="8ccb3-1156">Исправлено косую черту в конце домена учетной записи ADLS</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1156">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="8ccb3-1157">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1157">Az.FrontDoor</span></span>

* <span data-ttu-id="8ccb3-1158">Исправлены некоторые неработающие ссылки</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1158">Fixed some broken links</span></span>
    - <span data-ttu-id="8ccb3-1159">В статьях New-AzureRmFrontDoor и Set-AzureRmFrontDoor исправлена ссылка на статью командлета New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1159">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="8ccb3-1160">В статье New-AzureRmFrontDoorManagedRuleObject исправлена ссылка на статью командлета New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1160">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="8ccb3-1161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1161">Az.RecoveryServices</span></span>

* <span data-ttu-id="8ccb3-1162">Добавлены проверки на стороне клиента для операций восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1162">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="8ccb3-1163">StorageAccountName и storageAccountResourceGroupName являются необязательными для восстановления afs.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1163">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="8ccb3-1164">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1164">Az.Resources</span></span>

* <span data-ttu-id="8ccb3-1165">Исправление для https://github.com/Azure/azure-powershell/issues/7679.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1165">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="8ccb3-1166">Обновите Get-AzureRmRoleAssignment, чтобы использовать область подписки, если она указана при запросе классических администраторов.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1166">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="8ccb3-1167">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1167">Az.Sql</span></span>

* <span data-ttu-id="8ccb3-1168">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1168">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="8ccb3-1169">Устранена проблема с использованием Get-AzureRmSqlDatabaseVulnerabilityAssessment с .NET Core.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1169">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="8ccb3-1170">Изменена документация справочных сообщений, связанных с командлетами аудита SQL.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1170">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="8ccb3-1171">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1171">Az.Storage</span></span>

* <span data-ttu-id="8ccb3-1172">Добавлено -EnableHierarchicalNamespace к New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1172">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="8ccb3-1173">Устранена проблема, из-за которой командлет Copy File не может повторно использовать исходный контекст в пункте назначения, если не введен -DestContext</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1173">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="8ccb3-1174">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1174">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="8ccb3-1175">Поддержка статической конфигурации сайта</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1175">Support Static Website configuration</span></span>
    - <span data-ttu-id="8ccb3-1176">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1176">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="8ccb3-1177">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1177">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="8ccb3-1178">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1178">Az.Websites</span></span>

* <span data-ttu-id="8ccb3-1179">Set-AzureRmWebApp и Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1179">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="8ccb3-1180">Добавлен новый параметр (-AzureStoragePath), который указывает путь службы хранилища Azure для подключения в приложениях-контейнерах Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1180">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="8ccb3-1181">Используйте выходные данные нового командлета New-AzureRmWebAppAzureStoragePath в качестве параметра, чтобы задать пути к службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1181">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="8ccb3-1182">0.6.1 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1182">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="8ccb3-1183">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1183">Az.ApiManagement</span></span>
* <span data-ttu-id="8ccb3-1184">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1184">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="8ccb3-1185">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1185">Az.Automation</span></span>
* <span data-ttu-id="8ccb3-1186">Командлеты службы автоматизации Azure на базе Swagger.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1186">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="8ccb3-1187">Добавлены командлеты для Управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1187">Added Update Management cmdlets</span></span>
* <span data-ttu-id="8ccb3-1188">Добавлены командлеты для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1188">Added Source Control cmdlets</span></span>
* <span data-ttu-id="8ccb3-1189">Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1189">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="8ccb3-1190">Исправлена команда DSC для регистрации узла.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1190">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="8ccb3-1191">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1191">Az.Compute</span></span>
* <span data-ttu-id="8ccb3-1192">Исправлена проблема с удостоверением, назначаемым системой.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1192">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="8ccb3-1193">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1193">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="8ccb3-1194">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1194">Az.ContainerInstance</span></span>
* <span data-ttu-id="8ccb3-1195">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1195">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="8ccb3-1196">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1196">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="8ccb3-1197">Обновлено описание в примерах командлетов для Marketplace.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1197">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="8ccb3-1198">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1198">Az.Network</span></span>
* <span data-ttu-id="8ccb3-1199">Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1199">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="8ccb3-1200">Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1200">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="8ccb3-1201">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1201">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="8ccb3-1202">Исправлены проблемы с использованием памяти в карте виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1202">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="8ccb3-1203">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1203">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="8ccb3-1204">Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1204">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="8ccb3-1205">Параметры часового пояса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1205">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="8ccb3-1206">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1206">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="8ccb3-1207">Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1207">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="8ccb3-1208">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1208">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="8ccb3-1209">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1209">Az.Relay</span></span>
* <span data-ttu-id="8ccb3-1210">Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1210">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="8ccb3-1211">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1211">Az.Resources</span></span>
* <span data-ttu-id="8ccb3-1212">Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1212">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="8ccb3-1213">Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1213">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="8ccb3-1214">Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1214">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="8ccb3-1215">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1215">Az.ServiceFabric</span></span>
* <span data-ttu-id="8ccb3-1216">Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1216">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="8ccb3-1217">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1217">Az.Sql</span></span>
* <span data-ttu-id="8ccb3-1218">Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1218">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="8ccb3-1219">Get-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1219">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8ccb3-1220">New-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1220">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8ccb3-1221">Set-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1221">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8ccb3-1222">Remove-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1222">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8ccb3-1223">Get-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1223">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="8ccb3-1224">New-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1224">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="8ccb3-1225">Restore-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1225">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="8ccb3-1226">Remove-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1226">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="8ccb3-1227">Добавлено расширенное управление политиками аудита для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1227">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="8ccb3-1228">Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1228">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="8ccb3-1229">Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1229">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="8ccb3-1230">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1230">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="8ccb3-1231">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1231">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="8ccb3-1232">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1232">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="8ccb3-1233">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1233">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="8ccb3-1234">Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1234">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="8ccb3-1235">0.5.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1235">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="8ccb3-1236">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1236">General</span></span>
* <span data-ttu-id="8ccb3-1237">Добавлены средства заполнения ресурсов для многих основных командлетов — они позволяют вам переключать существующие имена ресурсов при вызове командлетов в интерактивном режиме</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1237">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="8ccb3-1238">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1238">Az.Profile</span></span>
* <span data-ttu-id="8ccb3-1239">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1239">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="8ccb3-1240">В командлете Connect-AzAccount параметр TenantId переименован в Tenant и добавлен псевдоним для TenantId</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1240">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="8ccb3-1241">Обновлено описание TenantId для командлета Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1241">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="8ccb3-1242">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1242">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="8ccb3-1243">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1243">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="8ccb3-1244">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1244">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="8ccb3-1245">Устранена проблема, при которой командлет Disconnect-AzAccount вызывал сбой при отсутствии подключения</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1245">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="8ccb3-1246">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1246">Az.CognitiveServices</span></span>
* <span data-ttu-id="8ccb3-1247">Добавлена операция Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1247">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ccb3-1248">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1248">Az.Compute</span></span>
* <span data-ttu-id="8ccb3-1249">Добавлены командлеты Add-AzVmssVMDataDisk и Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1249">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="8ccb3-1250">Get-AzVMImage отображает AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1250">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="8ccb3-1251">Устранена проблема, при которой значения параметров SetAzVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1251">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8ccb3-1252">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1252">Az.DataLakeStore</span></span>
* <span data-ttu-id="8ccb3-1253">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1253">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="8ccb3-1254">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1254">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="8ccb3-1255">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1255">Az.Insights</span></span>
* <span data-ttu-id="8ccb3-1256">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1256">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="8ccb3-1257">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1257">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="8ccb3-1258">Исправлена проблема № 7513 [Insights], при которой для командлета Set-AzDiagnosticSetting требовалось явное указание категорий во время создания параметра</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1258">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="8ccb3-1259">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1259">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ccb3-1260">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1260">Az.Network</span></span>
* <span data-ttu-id="8ccb3-1261">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1261">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="8ccb3-1262">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1262">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="8ccb3-1263">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1263">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="8ccb3-1264">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1264">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="8ccb3-1265">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1265">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="8ccb3-1266">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1266">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="8ccb3-1267">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1267">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8ccb3-1268">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1268">Az.PolicyInsights</span></span>
* <span data-ttu-id="8ccb3-1269">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1269">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ccb3-1270">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1270">Az.Resources</span></span>
* <span data-ttu-id="8ccb3-1271">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1271">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="8ccb3-1272">Разрешено перечисление ресурсов с помощью параметра -ResourceId для командлета Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1272">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8ccb3-1273">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1273">Az.ServiceBus</span></span>
* <span data-ttu-id="8ccb3-1274">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1274">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8ccb3-1275">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1275">Az.ServiceFabric</span></span>
* <span data-ttu-id="8ccb3-1276">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1276">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="8ccb3-1277">Исправлен командлет Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1277">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="8ccb3-1278">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1278">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="8ccb3-1279">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1279">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="8ccb3-1280">Исправлен командлет Update-AzServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1280">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="8ccb3-1281">0.4.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1281">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="8ccb3-1282">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1282">Az.Profile</span></span>
* <span data-ttu-id="8ccb3-1283">Устранена проблема с Get-AzSubscription в CloudShell</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1283">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="8ccb3-1284">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1284">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ccb3-1285">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1285">Az.Compute</span></span>
* <span data-ttu-id="8ccb3-1286">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzVm</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1286">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="8ccb3-1287">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1287">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8ccb3-1288">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1288">Az.DataLakeStore</span></span>
* <span data-ttu-id="8ccb3-1289">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1289">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="8ccb3-1290">Get-AzDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1290">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="8ccb3-1291">Add-AzDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1291">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="8ccb3-1292">Set-AzDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1292">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="8ccb3-1293">Remove-AzDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1293">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ccb3-1294">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1294">Az.Network</span></span>
* <span data-ttu-id="8ccb3-1295">Обновлен командлет Test-AzNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1295">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="8ccb3-1296">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1296">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ccb3-1297">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1297">Az.Resources</span></span>
* <span data-ttu-id="8ccb3-1298">Устранена проблема, из-за которой командлет Get-AzRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), благодаря добавлению понятного исключения в сценарий.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1298">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="8ccb3-1299">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1299">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="8ccb3-1300">0.3.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1300">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="8ccb3-1301">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1301">Azure.Storage</span></span>
* <span data-ttu-id="8ccb3-1302">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1302">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="8ccb3-1303">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1303">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="8ccb3-1304">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1304">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="8ccb3-1305">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1305">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="8ccb3-1306">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1306">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="8ccb3-1307">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1307">Az.CognitiveServices</span></span>
* <span data-ttu-id="8ccb3-1308">Поддержка Get-AzCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1308">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ccb3-1309">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1309">Az.Compute</span></span>
* <span data-ttu-id="8ccb3-1310">Исправлена команда Get-AzVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1310">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="8ccb3-1311">Добавлен пример использования SimpleParameterSet в справку командлета New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1311">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="8ccb3-1312">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1312">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="8ccb3-1313">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1313">Az.DataFactoryV2</span></span>
* <span data-ttu-id="8ccb3-1314">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1314">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ccb3-1315">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1315">Az.Network</span></span>
* <span data-ttu-id="8ccb3-1316">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1316">Added NetworkProfile functionality.</span></span> <span data-ttu-id="8ccb3-1317">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1317">new cmdlets added</span></span>
    - <span data-ttu-id="8ccb3-1318">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1318">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="8ccb3-1319">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1319">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="8ccb3-1320">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1320">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="8ccb3-1321">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1321">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="8ccb3-1322">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1322">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="8ccb3-1323">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1323">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="8ccb3-1324">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1324">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="8ccb3-1325">Добавлены командлеты: New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1325">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="8ccb3-1326">Добавлены командлеты: Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1326">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="8ccb3-1327">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1327">Az.RedisCache</span></span>
* <span data-ttu-id="8ccb3-1328">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1328">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="8ccb3-1329">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1329">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ccb3-1330">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1330">Az.Resources</span></span>
* <span data-ttu-id="8ccb3-1331">Добавлен отсутствующий параметр -Mode в командлет Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1331">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="8ccb3-1332">Исправлена ошибка командлета Get-AzProviderOperation для операций, когда Origin содержит User</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1332">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ccb3-1333">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1333">Az.Sql</span></span>
* <span data-ttu-id="8ccb3-1334">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1334">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8ccb3-1335">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1335">Az.Websites</span></span>
* <span data-ttu-id="8ccb3-1336">Новый командлет Get-AzWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1336">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="8ccb3-1337">Новые командлеты New-AzWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1337">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="8ccb3-1338">0.2.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1338">0.2.0 - September 2018</span></span>
 <span data-ttu-id="8ccb3-1339">Первый выпуск</span><span class="sxs-lookup"><span data-stu-id="8ccb3-1339">Initial Release</span></span>