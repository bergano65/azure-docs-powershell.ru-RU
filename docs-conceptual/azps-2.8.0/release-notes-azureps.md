---
title: Заметки о выпуске Azure PowerShell
description: Узнайте обо всех последних обновлениях модулей Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: 83e6039153bcc2b8ccb7ceddfa91609f0d6c7b3f
ms.sourcegitcommit: b4ee3fbaaa2a329ea28308bd1902ae83a34db698
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2019
ms.locfileid: "72380186"
---
## <a name="280---october-2019"></a><span data-ttu-id="04529-103">2.8.0 — октябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="04529-103">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="04529-104">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="04529-104">General</span></span>
* <span data-ttu-id="04529-105">Выпуск Az.HealthcareApis 1.0.0</span><span class="sxs-lookup"><span data-stu-id="04529-105">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="04529-106">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="04529-106">Az.Accounts</span></span>
* <span data-ttu-id="04529-107">Обновление телеметрии и перезаписи URL-адресов для созданных модулей, исправление для модульных тестов Windows.</span><span class="sxs-lookup"><span data-stu-id="04529-107">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="04529-108">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="04529-108">Az.ApiManagement</span></span>
* <span data-ttu-id="04529-109">**Set-AzApiManagementApi** — в ApiVersionSet добавлена поддержка обновления API.</span><span class="sxs-lookup"><span data-stu-id="04529-109">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="04529-110">исправлена проблема https://github.com/Azure/azure-powershell/issues/10068.</span><span class="sxs-lookup"><span data-stu-id="04529-110">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="04529-111">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="04529-111">Az.Automation</span></span>
* <span data-ttu-id="04529-112">Исправлен командлет New-AzureAutomationSoftwareUpdateConfiguration для параметра перезагрузки Linux.</span><span class="sxs-lookup"><span data-stu-id="04529-112">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="04529-113">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="04529-113">Az.Batch</span></span>
* <span data-ttu-id="04529-114">Командлет **Get-AzBatchNodeAgentSku** объявлен устаревшим и будет заменен на **Get-AzBatchSupportImage** в версии 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="04529-114">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="04529-115">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="04529-115">Az.Compute</span></span>
* <span data-ttu-id="04529-116">В командлеты New-AzVM и New-AzVmss добавлены параметры Priority, EvictionPolicy и MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="04529-116">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="04529-117">Исправлены предупреждающее сообщение для командлетов Add-AzVMAdditionalUnattendContent и Add-AzVMSshPublicKey и справочная документация по ним.</span><span class="sxs-lookup"><span data-stu-id="04529-117">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="04529-118">Для Set-AzVMDiskEncryptionExtension исправлено исключение -skipVmBackup для виртуальных машин Linux с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="04529-118">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="04529-119">Исправлена ошибка при изменении параметров шифрования в Set-AzVMDiskEncryptionExtension, реализован двухэтапный сценарий.</span><span class="sxs-lookup"><span data-stu-id="04529-119">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="04529-120">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="04529-120">Az.DataFactory</span></span>
* <span data-ttu-id="04529-121">Добавлены команды CRUD для потока данных Фабрики данных Azure версии 2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow и Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="04529-121">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="04529-122">Добавлены команды действий для сеанса отладки потока данных Фабрики данных Azure версии 2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand и Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="04529-122">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="04529-123">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.2.0.</span><span class="sxs-lookup"><span data-stu-id="04529-123">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="04529-124">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="04529-124">Az.DataLakeStore</span></span>
* <span data-ttu-id="04529-125">Проверка учетной записи исправлена так, чтобы учетные записи, содержащие знак "-", можно было передавать без домена.</span><span class="sxs-lookup"><span data-stu-id="04529-125">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="04529-126">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="04529-126">Az.HealthcareApis</span></span>
* <span data-ttu-id="04529-127">Версия PowerShell обновлена до 1.0.0.</span><span class="sxs-lookup"><span data-stu-id="04529-127">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="04529-128">Версия пакета SDK обновлена до 1.0.2.</span><span class="sxs-lookup"><span data-stu-id="04529-128">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="04529-129">В тестах обновлены ссылки на новую версию пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="04529-129">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="04529-130">Вложенная выходная структура заменена на плоскую.</span><span class="sxs-lookup"><span data-stu-id="04529-130">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="04529-131">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="04529-131">Az.IotHub</span></span>
* <span data-ttu-id="04529-132">Добавлен новый источник маршрутизации DigitalTwinChangeEvents.</span><span class="sxs-lookup"><span data-stu-id="04529-132">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="04529-133">Исправлены незначительные ошибки: Get-AzIothub не возвращает subscriptionId.</span><span class="sxs-lookup"><span data-stu-id="04529-133">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="04529-134">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="04529-134">Az.Monitor</span></span>
* <span data-ttu-id="04529-135">Добавлены новые получатели групп действий: -ItsmReceiver, -VoiceReceiver, -ArmRoleReceiver, -AzureFunctionReceiver, -LogicAppReceiver, -AutomationRunbookReceiver, -AzureAppPushReceiver.</span><span class="sxs-lookup"><span data-stu-id="04529-135">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="04529-136">Для получателей включите общую схему оповещений.</span><span class="sxs-lookup"><span data-stu-id="04529-136">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="04529-137">Это не касается получателей SMS, push-уведомлений приложения Azure, ITSM и голосовых сообщений.</span><span class="sxs-lookup"><span data-stu-id="04529-137">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="04529-138">Веб-перехватчики теперь поддерживают аутентификацию Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="04529-138">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="04529-139">Az.Network</span><span class="sxs-lookup"><span data-stu-id="04529-139">Az.Network</span></span>
* <span data-ttu-id="04529-140">Добавлен новый командлет Get-AzAvailableServiceAlias, позволяющий получить псевдонимы для политик конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="04529-140">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="04529-141">В подключениях шлюза виртуальной сети появилась возможность добавлять селекторы трафика.</span><span class="sxs-lookup"><span data-stu-id="04529-141">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="04529-142">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="04529-142">New cmdlets added:</span></span>
        - <span data-ttu-id="04529-143">New-AzureRmTrafficSelectorPolicy.</span><span class="sxs-lookup"><span data-stu-id="04529-143">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="04529-144">В командлеты добавлены необязательные параметры -TrafficSelectorPolicies, -New-AzureRmVirtualNetworkGatewayConnection, -Set-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="04529-144">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="04529-145">В конфигурациях правил сетевой безопасности добавлена поддержка протоколов ESP и AH.</span><span class="sxs-lookup"><span data-stu-id="04529-145">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="04529-146">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="04529-146">Updated cmdlets:</span></span>
        - <span data-ttu-id="04529-147">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="04529-147">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="04529-148">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="04529-148">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="04529-149">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="04529-149">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="04529-150">Улучшена обработка исключений в командлетах Cortex.</span><span class="sxs-lookup"><span data-stu-id="04529-150">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="04529-151">Выпущены новые поколения и номера SKU VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="04529-151">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="04529-152">Представлены новые поколения VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="04529-152">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="04529-153">Представлены новые номера SKU VirtualNetworkGateways с высокой пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="04529-153">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="04529-154">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="04529-154">Az.RedisCache</span></span>
* <span data-ttu-id="04529-155">В справочную документацию по Set-AzRedisCache добавлены недостающие значения для параметра -Size.</span><span class="sxs-lookup"><span data-stu-id="04529-155">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="04529-156">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="04529-156">Az.Sql</span></span>
* <span data-ttu-id="04529-157">Добавлена возможность назначать администратора Active Directory в Управляемом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="04529-157">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="04529-158">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="04529-158">Az.Storage</span></span>
* <span data-ttu-id="04529-159">Клиентская библиотека службы хранилища Azure обновлена до версии 11.1.0.</span><span class="sxs-lookup"><span data-stu-id="04529-159">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="04529-160">NextPageLink теперь позволяет получить список контейнеров с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="04529-160">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="04529-161">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="04529-161">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="04529-162">NextPageLink теперь позволяет получить список учетных записей хранения из подписки.</span><span class="sxs-lookup"><span data-stu-id="04529-162">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="04529-163">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="04529-163">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="04529-164">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="04529-164">Az.StorageSync</span></span>
* <span data-ttu-id="04529-165">Исправлена проблема 9810 с Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="04529-165">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="04529-166">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="04529-166">Az.Websites</span></span>
* <span data-ttu-id="04529-167">Обновление плана службы приложений с помощью Set-AzWebApp приводило к сбою приложения.</span><span class="sxs-lookup"><span data-stu-id="04529-167">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="04529-168">2.7.0 — сентябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="04529-168">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="04529-169">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="04529-169">Az.ApiManagement</span></span>
* <span data-ttu-id="04529-170">В справочной документации по командлету Set-AzApiManagementPolicy обновлено описание параметра -Format.</span><span class="sxs-lookup"><span data-stu-id="04529-170">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="04529-171">Из справочной документации удалены ссылки на нерекомендуемый командлет Update-AzApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="04529-171">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="04529-172">Вместо него следует использовать командлет Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="04529-172">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="04529-173">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="04529-173">Az.Automation</span></span>
* <span data-ttu-id="04529-174">В справочной документации по командлету Register-AzAutomationDscNode исправлена опечатка в примере.</span><span class="sxs-lookup"><span data-stu-id="04529-174">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="04529-175">Добавлено уточнение об ограничениях ОС для командлета Register-AzAutomationDSCNode.</span><span class="sxs-lookup"><span data-stu-id="04529-175">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="04529-176">Исправлено исключение пустой ссылки для параметра -Wait в командлете Start-AzAutomationRunbook.</span><span class="sxs-lookup"><span data-stu-id="04529-176">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="04529-177">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="04529-177">Az.Compute</span></span>
* <span data-ttu-id="04529-178">Добавлен параметр UploadSizeInBytes для командлета New-AzDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="04529-178">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="04529-179">Добавлен добавочный параметр для командлета New-AzSnapshotConfig.</span><span class="sxs-lookup"><span data-stu-id="04529-179">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="04529-180">Для виртуальной машины добавлены такие функции с низким приоритетом:</span><span class="sxs-lookup"><span data-stu-id="04529-180">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="04529-181">Для командлета New-AzVMConfig добавлены параметры MaxPrice, EvictionPolicy и Priority.</span><span class="sxs-lookup"><span data-stu-id="04529-181">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="04529-182">Для командлетов New-AzVmssConfig, Update-AzVM и Update-AzVmss добавлен параметр MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="04529-182">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="04529-183">Для командлета Get-AzAvailabilitySet устранена проблема со ссылкой на виртуальную машину, когда в нем перечисляются все группы доступности в подписке.</span><span class="sxs-lookup"><span data-stu-id="04529-183">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="04529-184">Исправлено исключение NULL для командлета Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="04529-184">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="04529-185">Исправлен метод поиска VHD для относительной конечной позиции.</span><span class="sxs-lookup"><span data-stu-id="04529-185">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="04529-186">Устранена проблема с UltraSSD для командлетов New-AzVM и Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="04529-186">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="04529-187">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="04529-187">Az.DataFactory</span></span>
* <span data-ttu-id="04529-188">Добавлены 3 новые команды для ADF версии 2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription и Get-AzDataFactoryV2TriggerSubscriptionStatus.</span><span class="sxs-lookup"><span data-stu-id="04529-188">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="04529-189">Пакет SDK ADF для .NET обновлен до версии 4.1.3.</span><span class="sxs-lookup"><span data-stu-id="04529-189">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="04529-190">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="04529-190">Az.HDInsight</span></span>
* <span data-ttu-id="04529-191">Укажите критические изменения.</span><span class="sxs-lookup"><span data-stu-id="04529-191">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="04529-192">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="04529-192">Az.IotHub</span></span>
* <span data-ttu-id="04529-193">Добавлена поддержка для вызова отработки отказа для IotHub в георегион аварийного восстановления.</span><span class="sxs-lookup"><span data-stu-id="04529-193">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="04529-194">Добавлена поддержка для управления обогащением сообщений для IotHub.</span><span class="sxs-lookup"><span data-stu-id="04529-194">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="04529-195">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="04529-195">New cmdlets are:</span></span>
    - <span data-ttu-id="04529-196">Add-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="04529-196">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="04529-197">Get-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="04529-197">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="04529-198">Remove-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="04529-198">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="04529-199">Set-AzIotHubMessageEnrichment.</span><span class="sxs-lookup"><span data-stu-id="04529-199">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="04529-200">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="04529-200">Az.Monitor</span></span>
* <span data-ttu-id="04529-201">Указание на самую последнюю версию пакета SDK для монитора, т. е. 0.24.1-preview:</span><span class="sxs-lookup"><span data-stu-id="04529-201">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="04529-202">В командлеты метрик добавлены некритические изменения, т. е. перечисление единиц поддерживает несколько новых значений.</span><span class="sxs-lookup"><span data-stu-id="04529-202">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="04529-203">Эти командлеты доступны только для чтения, поэтому входные данные командлетов не будут изменены.</span><span class="sxs-lookup"><span data-stu-id="04529-203">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="04529-204">Актуальная версия API запросов **ActionGroups** — **2019-06-01**. До этого была версия **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="04529-204">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="04529-205">Тесты сценария обновлены в соответствии с этим изменением.</span><span class="sxs-lookup"><span data-stu-id="04529-205">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="04529-206">В конструкторы классов **EmailReceiver** и **WebhookReceiver** добавлен один новый обязательный аргумент — логическое значение с именем **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="04529-206">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="04529-207">Сейчас для него установлено значение **false**, чтобы скрыть это критическое изменение от командлетов.</span><span class="sxs-lookup"><span data-stu-id="04529-207">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="04529-208">**Примечание**. Это временное изменение, которое должно быть подтверждено командой оповещения.</span><span class="sxs-lookup"><span data-stu-id="04529-208">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="04529-209">Порядок аргументов для конструктора класса **Source** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="04529-209">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="04529-210">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="04529-210">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="04529-211">Порядок аргументов для конструктора класса **AlertingAction** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="04529-211">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="04529-212">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="04529-212">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="04529-213">Добавлена поддержка критериев динамического порога для оповещения метрики версии 2:</span><span class="sxs-lookup"><span data-stu-id="04529-213">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="04529-214">New-AzMetricAlertRuleV2Criteria: теперь также позволяет создавать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="04529-214">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="04529-215">Add-AzMetricAlertRuleV2: теперь также позволяет принимать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="04529-215">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="04529-216">Добавлены усовершенствования в командлетах запланированных правил запросов (SQR).</span><span class="sxs-lookup"><span data-stu-id="04529-216">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="04529-217">Командлеты будут принимать параметр Location в обоих форматах: расположение (например, eastus) или отображаемое имя расположения (например, "восточная часть США").</span><span class="sxs-lookup"><span data-stu-id="04529-217">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="04529-218">Параметр Enabled проиллюстрирован в файлах справки надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="04529-218">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="04529-219">Добавлены примеры для необязательного параметра ActionGroup.</span><span class="sxs-lookup"><span data-stu-id="04529-219">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="04529-220">Все файлы справки улучшены.</span><span class="sxs-lookup"><span data-stu-id="04529-220">Overall improved help files</span></span>
* <span data-ttu-id="04529-221">Исправлена ошибка в определении типа области для командлета Set-AzActionRule.</span><span class="sxs-lookup"><span data-stu-id="04529-221">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="04529-222">Az.Network</span><span class="sxs-lookup"><span data-stu-id="04529-222">Az.Network</span></span>
* <span data-ttu-id="04529-223">Исправлен неправильный пример в справочной документации по командлету New-AzApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="04529-223">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="04529-224">В справочную документацию по командлету Get-AzNetworkWatcherPacketCapture добавлено примечание, посвященное извлечению всех свойств для записи пакетов.</span><span class="sxs-lookup"><span data-stu-id="04529-224">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="04529-225">В справочной документации по командлету Test-AzNetworkWatcherIPFlow исправлен пример: теперь он правильно перечисляет сетевые карты.</span><span class="sxs-lookup"><span data-stu-id="04529-225">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="04529-226">Улучшен анализ облачных исключений для отображения дополнительных сведений (при их наличии).</span><span class="sxs-lookup"><span data-stu-id="04529-226">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="04529-227">Улучшен анализ облачных исключений для обработки дополнительного типа исключения SDK.</span><span class="sxs-lookup"><span data-stu-id="04529-227">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="04529-228">Исправлено неправильное сопоставление моделей правил безопасности.</span><span class="sxs-lookup"><span data-stu-id="04529-228">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="04529-229">Добавлены свойства сетевого интерфейса для компонента частного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="04529-229">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="04529-230">Для интерфейса PSNetworkInterface добавлено свойство PrivateEndpoint с типом PSResourceId.</span><span class="sxs-lookup"><span data-stu-id="04529-230">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="04529-231">В PSNetworkInterfaceIPConfiguration добавлено свойство PrivateLinkConnectionProperties с типом PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="04529-231">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="04529-232">Добавлен новый класс модели: PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="04529-232">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="04529-233">Добавлен новый тип ApplicationRuleProtocolType "mssql" для ресурса Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="04529-233">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="04529-234">Поддержка многоканального подключения в Виртуальной глобальной сети:</span><span class="sxs-lookup"><span data-stu-id="04529-234">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="04529-235">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="04529-235">New cmdlets</span></span>
        - <span data-ttu-id="04529-236">New-AzVpnSiteLink;</span><span class="sxs-lookup"><span data-stu-id="04529-236">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="04529-237">New-AzVpnSiteLinkConnection;</span><span class="sxs-lookup"><span data-stu-id="04529-237">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="04529-238">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="04529-238">Updated cmdlet:</span></span>
        - <span data-ttu-id="04529-239">New-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="04529-239">New-VpnSite</span></span>
        - <span data-ttu-id="04529-240">Update-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="04529-240">Update-VpnSite</span></span>
        - <span data-ttu-id="04529-241">New-VpnConnection;</span><span class="sxs-lookup"><span data-stu-id="04529-241">New-VpnConnection</span></span>
        - <span data-ttu-id="04529-242">Update-VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="04529-242">Update-VpnConnection</span></span>
* <span data-ttu-id="04529-243">Исправлены документы с некоторыми примерами PowerShell для использования командлетов AZ вместо командлетов AzureRM.</span><span class="sxs-lookup"><span data-stu-id="04529-243">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="04529-244">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="04529-244">Az.RecoveryServices</span></span>
* <span data-ttu-id="04529-245">Для объекта AzureVMpolicy добавлен новый атрибут — ProtectedItemsCount.</span><span class="sxs-lookup"><span data-stu-id="04529-245">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="04529-246">Добавлены тесты для политики виртуальной машины и восстановления исходной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="04529-246">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="04529-247">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="04529-247">Az.Resources</span></span>
* <span data-ttu-id="04529-248">Исправлена ошибка, при которой не удавалось вызвать командлет New-AzRoleAssignment без параметра Scope.</span><span class="sxs-lookup"><span data-stu-id="04529-248">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="04529-249">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="04529-249">Az.ServiceFabric</span></span>
* <span data-ttu-id="04529-250">Исправлена опечатка в примере в справочной документации по командлету Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="04529-250">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="04529-251">Добавлены новые командлеты для управления приложениями и службами:</span><span class="sxs-lookup"><span data-stu-id="04529-251">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="04529-252">New-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="04529-252">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="04529-253">New-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="04529-253">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="04529-254">New-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="04529-254">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="04529-255">New-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="04529-255">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="04529-256">Update-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="04529-256">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="04529-257">Get-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="04529-257">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="04529-258">Get-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="04529-258">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="04529-259">Get-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="04529-259">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="04529-260">Get-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="04529-260">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="04529-261">Remove-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="04529-261">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="04529-262">Remove-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="04529-262">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="04529-263">Remove-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="04529-263">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="04529-264">Remove-AzServiceFabricServic.</span><span class="sxs-lookup"><span data-stu-id="04529-264">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="04529-265">Пакет SDK для Service Fabric обновлен до версии 1.2.0, в которой используется версия API 2019-03-01 поставщика ресурсов Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="04529-265">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="04529-266">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="04529-266">Az.SignalR</span></span>
* <span data-ttu-id="04529-267">Добавлены командлеты Update, Restart, CheckNameAvailability и GetUsage.</span><span class="sxs-lookup"><span data-stu-id="04529-267">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="04529-268">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="04529-268">Az.Sql</span></span>
* <span data-ttu-id="04529-269">Обновлен пример в справочной документации по командлету Get-AzSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="04529-269">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="04529-270">Добавлен пример виртуального ядра для командлета создания эластичного пула (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="04529-270">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="04529-271">Удалена проверка свойства EmailAddresses и того, что свойство EmailAdmins правильное в случае, если свойство EmailAddresses пустое в командлетах Set-AzSqlServerAdvancedThreatProtectionPolicy и Set-AzSqlDatabaseAdvancedThreatProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="04529-271">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="04529-272">Теперь, если существует несколько параметров диагностики, включающих категорию аудита, параметры аудита сервера и базы данных удаляются.</span><span class="sxs-lookup"><span data-stu-id="04529-272">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="04529-273">Исправлена проверка адресов электронной почты в нескольких командлетах оценки уязвимостей SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting и Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="04529-273">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="04529-274">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="04529-274">Az.Storage</span></span>
* <span data-ttu-id="04529-275">Обновлен пример в справочной документации по командлету Get-AzStorageAccountKey.</span><span class="sxs-lookup"><span data-stu-id="04529-275">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="04529-276">Теперь при отправке и загрузке файла Azure в конечном файле сохраняются свойства SMB исходного файла (атрибуты файла, время создания файла, время последней записи файла).</span><span class="sxs-lookup"><span data-stu-id="04529-276">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="04529-277">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="04529-277">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="04529-278">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="04529-278">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="04529-279">Исправлена операция отправки блочного BLOB-объекта, в которой происходили сбои свойств и метаданных в контейнере с включенной ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="04529-279">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="04529-280">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="04529-280">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="04529-281">Добавлена поддержка управления общими папками Azure в API плоскости управления с помощью таких командлетов:</span><span class="sxs-lookup"><span data-stu-id="04529-281">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="04529-282">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="04529-282">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="04529-283">Get-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="04529-283">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="04529-284">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="04529-284">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="04529-285">Remove-AzRmStorageShare.</span><span class="sxs-lookup"><span data-stu-id="04529-285">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="04529-286">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="04529-286">Az.Websites</span></span>
* <span data-ttu-id="04529-287">Устранена проблема, из-за которой теги webapp удалялись при переносе приложения в новый ASP.</span><span class="sxs-lookup"><span data-stu-id="04529-287">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="04529-288">Теперь командлет Publish-AzureWebapp работает в Linux и Windows.</span><span class="sxs-lookup"><span data-stu-id="04529-288">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="04529-289">Обновлен пример в справочной документации по командлету Get-AzWebAppPublishingProfile.</span><span class="sxs-lookup"><span data-stu-id="04529-289">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="04529-290">2.6.0 — август 2019 г.</span><span class="sxs-lookup"><span data-stu-id="04529-290">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="04529-291">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="04529-291">General</span></span>
* <span data-ttu-id="04529-292">Исправлены опечатки в модулях.</span><span class="sxs-lookup"><span data-stu-id="04529-292">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="04529-293">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="04529-293">Az.Accounts</span></span>
* <span data-ttu-id="04529-294">Добавлена поддержка назначаемого пользователем удостоверения MSI при проверке подлинности в Функциях Azure (№ 9479).</span><span class="sxs-lookup"><span data-stu-id="04529-294">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="04529-295">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="04529-295">Az.Aks</span></span>
* <span data-ttu-id="04529-296">Устранена проблема с выходными данными для Get-AzAks.</span><span class="sxs-lookup"><span data-stu-id="04529-296">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="04529-297">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9847.</span><span class="sxs-lookup"><span data-stu-id="04529-297">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="04529-298">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="04529-298">Az.ApiManagement</span></span>
* <span data-ttu-id="04529-299">исправлена проблема https://github.com/Azure/azure-powershell/issues/9351.</span><span class="sxs-lookup"><span data-stu-id="04529-299">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="04529-300">Обновлена версия NuGet для .NET, которая не накладывает ограничений на productId, apiId, groupId и userId.</span><span class="sxs-lookup"><span data-stu-id="04529-300">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="04529-301">**Get-AzApiManagementProduct**. Добавлена поддержка запросов к продуктам с помощью API.</span><span class="sxs-lookup"><span data-stu-id="04529-301">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="04529-302">**New-AzApiManagementApiRevision**. Устранена проблема, из-за которой не задавался параметр ApiRevisionDescription при создании новой редакции API https://github.com/Azure/azure-powershell/issues/9752.</span><span class="sxs-lookup"><span data-stu-id="04529-302">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="04529-303">Исправлено написание имени модели c PsApiManagementOAuth2AuthrozationServer на PsApiManagementOAuth2AuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="04529-303">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="04529-304">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="04529-304">Az.Batch</span></span>
* <span data-ttu-id="04529-305">Исправлена опечатка в написании Windows со строчной буквы в справочных сообщениях и документации.</span><span class="sxs-lookup"><span data-stu-id="04529-305">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="04529-306">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="04529-306">Az.Cdn</span></span>
* <span data-ttu-id="04529-307">Исправлена опечатка во вспомогательном приложении модуля CDN.</span><span class="sxs-lookup"><span data-stu-id="04529-307">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="04529-308">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="04529-308">Az.Compute</span></span>
* <span data-ttu-id="04529-309">Добавлен параметр VmssId в новый командлет Add New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="04529-309">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="04529-310">Добавлены параметры TerminateScheduledEvents и TerminateScheduledEventNotBeforeTimeoutInMinutes в New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="04529-310">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="04529-311">Добавлено свойство HyperVGeneration в объект образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="04529-311">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="04529-312">Добавлены компоненты Host и HostGroup.</span><span class="sxs-lookup"><span data-stu-id="04529-312">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="04529-313">Новые командлеты:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="04529-313">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="04529-314">Параметр HostId добавлен в New-AzVMConfig и New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="04529-314">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="04529-315">Исправлен пример в документации по Invoke-AzVMRunCommand, в котором теперь используется правильное имя параметра.</span><span class="sxs-lookup"><span data-stu-id="04529-315">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="04529-316">Исправлено описание VolumeType в справочной документации по Set-AzVMDiskEncryptionExtension и Set-AzVmssDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="04529-316">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="04529-317">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="04529-317">Az.DataFactory</span></span>
* <span data-ttu-id="04529-318">Исправлена опечатка в написании Windows со строчной буквы в документации по New-AzDataFactoryEncryptValue.</span><span class="sxs-lookup"><span data-stu-id="04529-318">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="04529-319">Пакет SDK ADF для .NET обновлен до версии 4.1.2.</span><span class="sxs-lookup"><span data-stu-id="04529-319">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="04529-320">Добавлены параметры DataProxyIntegrationRuntimeName, DataProxyStagingLinkedServiceName и DataProxyStagingPath в командлет Set-AzureRmDataFactoryV2IntegrationRuntime, что позволяет настраивать локальную среду выполнения интеграции в качестве прокси-сервера для Azure-SSIS Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="04529-320">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="04529-321">Обновлены PSTriggerRun для отображения активированных конвейеров, сообщений и свойств и PSActivityRun для отображения типа действия.</span><span class="sxs-lookup"><span data-stu-id="04529-321">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="04529-322">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="04529-322">Az.DataLakeStore</span></span>
* <span data-ttu-id="04529-323">Устранена проблема, при которой Get-DataLakeStoreDeletedItem переставал отвечать на запросы при возникновении ошибок или удаленных исключений.</span><span class="sxs-lookup"><span data-stu-id="04529-323">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="04529-324">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="04529-324">Az.EventHub</span></span>
* <span data-ttu-id="04529-325">Исправлена проблема № 9658: опечатка в написании параметра VirtualNteworkRule у Set-AzEventHubNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="04529-325">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="04529-326">Исправлена проблема № 9558: в Set-AzEventHubNamespace используется PATCH вместо PUT.</span><span class="sxs-lookup"><span data-stu-id="04529-326">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="04529-327">В командлет Set-AzEventHubNamespace добавлен параметр EnableKafka.</span><span class="sxs-lookup"><span data-stu-id="04529-327">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="04529-328">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="04529-328">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="04529-329">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="04529-329">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="04529-330">Исправлено написание Azure со строчной буквы.</span><span class="sxs-lookup"><span data-stu-id="04529-330">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="04529-331">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="04529-331">Az.Monitor</span></span>
* <span data-ttu-id="04529-332">Исправлены неправильные имена параметров в справочной документации.</span><span class="sxs-lookup"><span data-stu-id="04529-332">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="04529-333">Az.Network</span><span class="sxs-lookup"><span data-stu-id="04529-333">Az.Network</span></span>
* <span data-ttu-id="04529-334">Обновлен New-AzPrivateLinkServiceIpConfig.</span><span class="sxs-lookup"><span data-stu-id="04529-334">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="04529-335">Параметр PublicIpAddress объявлен нерекомендуемым, так как он не используется на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="04529-335">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="04529-336">Добавлен необязательный параметр Primary, указывающий, является ли текущая IP-конфигурация основной.</span><span class="sxs-lookup"><span data-stu-id="04529-336">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="04529-337">Улучшена обработка исключений из-за ошибок запроса от пакета SDK. Устранена проблема, при которой исключения пакета SDK не обрабатывались правильно, из-за чего не отображались основные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="04529-337">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="04529-338">Настроена логика проверки для префикса IPv6 IP-адреса для проверки правильности длины префикса IPv6.</span><span class="sxs-lookup"><span data-stu-id="04529-338">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="04529-339">Обновлен Get-AzVirtualNetworkSubnetConfig: добавлен набор параметров для получения по идентификатору ресурса подсети.</span><span class="sxs-lookup"><span data-stu-id="04529-339">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="04529-340">Обновлено описание параметра Location для AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="04529-340">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="04529-341">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="04529-341">Az.OperationalInsights</span></span>
* <span data-ttu-id="04529-342">Обновлена документация по New-AzOperationalInsightsLinuxSyslogDataSource.</span><span class="sxs-lookup"><span data-stu-id="04529-342">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="04529-343">Добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="04529-343">Added example</span></span>
    - <span data-ttu-id="04529-344">Обновлено описание параметра -Name.</span><span class="sxs-lookup"><span data-stu-id="04529-344">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="04529-345">Добавлен пример для New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="04529-345">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="04529-346">Изменено описание параметра -Name для New-AzOperationalInsightsWindowsEventDataSource.</span><span class="sxs-lookup"><span data-stu-id="04529-346">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="04529-347">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="04529-347">Az.RecoveryServices</span></span>
* <span data-ttu-id="04529-348">Обновлен Get-AzRecoveryServicesBackupJobDetail.md.</span><span class="sxs-lookup"><span data-stu-id="04529-348">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="04529-349">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="04529-349">Az.Resources</span></span>
* <span data-ttu-id="04529-350">Добавлена поддержка новой версии API 2019-05-10 для Microsoft.Resource.</span><span class="sxs-lookup"><span data-stu-id="04529-350">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="04529-351">Добавлена поддержка copy.count = 0 для переменных, ресурсов и свойств.</span><span class="sxs-lookup"><span data-stu-id="04529-351">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="04529-352">Ресурсы, у которых condition = false или copy.count = 0, будут удаляться в полном режиме.</span><span class="sxs-lookup"><span data-stu-id="04529-352">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="04529-353">В справочную документацию добавлен пример назначения политики на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="04529-353">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="04529-354">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="04529-354">Az.ServiceBus</span></span>
* <span data-ttu-id="04529-355">Исправлена проблема № 9658: опечатка в написании параметра VirtualNetworkRule В Set-AzServiceBusNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="04529-355">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="04529-356">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="04529-356">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="04529-357">Добавлена новая команда Test-AzServiceBusNameAvailability для проверки доступности имени для очереди и раздела.</span><span class="sxs-lookup"><span data-stu-id="04529-357">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="04529-358">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="04529-358">Az.ServiceFabric</span></span>
* <span data-ttu-id="04529-359">Устранены ошибки командлета для добавления типа узла:</span><span class="sxs-lookup"><span data-stu-id="04529-359">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="04529-360">ошибка NullReferenceException, возникавшая, если у группы ресурсов были другие VMSS, не связанные с кластером Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="04529-360">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="04529-361">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8681.</span><span class="sxs-lookup"><span data-stu-id="04529-361">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="04529-362">Исправлена ошибка, из-за которой командлет завершился сбоем, если virtualNetwork находилась не в той группе ресурсов, к которой относится кластер.</span><span class="sxs-lookup"><span data-stu-id="04529-362">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="04529-363">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8407.</span><span class="sxs-lookup"><span data-stu-id="04529-363">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="04529-364">Командлет Add-AzServiceFabricApplicationCertificate объявлен нерекомендуемым.</span><span class="sxs-lookup"><span data-stu-id="04529-364">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="04529-365">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="04529-365">Az.Sql</span></span>
* <span data-ttu-id="04529-366">Обновление документации по старым командлетам аудита.</span><span class="sxs-lookup"><span data-stu-id="04529-366">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="04529-367">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="04529-367">Az.Storage</span></span>
* <span data-ttu-id="04529-368">Обновлена справка по Get/Close-AzStorageFileHandle: в примеры добавлены сценарии использования командлетов и обновлено описание параметров.</span><span class="sxs-lookup"><span data-stu-id="04529-368">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="04529-369">Добавлена поддержка StandardBlobTier в операции отправки BLOB-объекта и копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="04529-369">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="04529-370">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="04529-370">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="04529-371">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="04529-371">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="04529-372">Добавлена поддержка приоритета восстановления в операцию копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="04529-372">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="04529-373">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="04529-373">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="04529-374">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="04529-374">Az.Websites</span></span>
* <span data-ttu-id="04529-375">Добавлены уточнение для параметра -AppSettings в Set-AzWebApp и Set-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="04529-375">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="04529-376">2.5.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="04529-376">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="04529-377">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="04529-377">Az.Accounts</span></span>
* <span data-ttu-id="04529-378">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="04529-378">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="04529-379">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="04529-379">Az.ApplicationInsights</span></span>
* <span data-ttu-id="04529-380">Исправлена опечатка в примере в документации по Remove-AzApplicationInsightsApiKey.</span><span class="sxs-lookup"><span data-stu-id="04529-380">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="04529-381">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="04529-381">Az.Automation</span></span>
* <span data-ttu-id="04529-382">Исправлена опечатка в строке ресурса.</span><span class="sxs-lookup"><span data-stu-id="04529-382">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="04529-383">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="04529-383">Az.CognitiveServices</span></span>
* <span data-ttu-id="04529-384">Добавлена поддержка NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="04529-384">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="04529-385">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="04529-385">Az.Compute</span></span>
* <span data-ttu-id="04529-386">Добавлены недостающие свойства (ComputerName, OsName, OsVersion и HyperVGeneration) для объекта представления экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="04529-386">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="04529-387">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="04529-387">Az.ContainerRegistry</span></span>
* <span data-ttu-id="04529-388">Исправлена опечатка в Remove-AzContainerRegistryReplication для параметра репликации.</span><span class="sxs-lookup"><span data-stu-id="04529-388">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="04529-389">См. подробнее: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="04529-389">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="04529-390">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="04529-390">Az.DataFactory</span></span>
* <span data-ttu-id="04529-391">Пакет SDK для ADF .NET обновлен до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="04529-391">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="04529-392">Исправлена опечатка в документации по Get-AzDataFactoryV2PipelineRun.</span><span class="sxs-lookup"><span data-stu-id="04529-392">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="04529-393">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="04529-393">Az.EventHub</span></span>
* <span data-ttu-id="04529-394">Добавлен новый командлет для создания маркера SAS: New-AzEventHubAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="04529-394">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="04529-395">Добавлена проверка и сообщение об ошибке для случаев, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="04529-395">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="04529-396">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="04529-396">Az.KeyVault</span></span>
* <span data-ttu-id="04529-397">Добавлена поддержка для настройки параметра KeySize в политиках сертификатов.</span><span class="sxs-lookup"><span data-stu-id="04529-397">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="04529-398">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="04529-398">Az.LogicApp</span></span>
* <span data-ttu-id="04529-399">Get-AzIntegrationAccountMap теперь надлежащим образом выводит все типы сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="04529-399">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="04529-400">Добавлен новый параметр MapType для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="04529-400">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="04529-401">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="04529-401">Az.ManagedServices</span></span>
* <span data-ttu-id="04529-402">Добавлена поддержка API версии 2019-06-01 (общедоступная).</span><span class="sxs-lookup"><span data-stu-id="04529-402">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="04529-403">Az.Network</span><span class="sxs-lookup"><span data-stu-id="04529-403">Az.Network</span></span>
* <span data-ttu-id="04529-404">Добавлена поддержка частной конечной точки и службы приватного канала.</span><span class="sxs-lookup"><span data-stu-id="04529-404">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="04529-405">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="04529-405">New cmdlets</span></span>
        - <span data-ttu-id="04529-406">Set-AzPrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="04529-406">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="04529-407">Set-AzPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="04529-407">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="04529-408">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="04529-408">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="04529-409">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="04529-409">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="04529-410">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="04529-410">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="04529-411">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="04529-411">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="04529-412">Test-AzPrivateLinkServiceVisibility.</span><span class="sxs-lookup"><span data-stu-id="04529-412">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="04529-413">Get-AzAutoApprovedPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="04529-413">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="04529-414">Обновлены следующие команды для функции: Флаг PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies в подсети в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="04529-414">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="04529-415">Обновлены командлеты New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig.</span><span class="sxs-lookup"><span data-stu-id="04529-415">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="04529-416">Добавлен необязательный параметр -PrivateEndpointNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к частной конечной точке в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="04529-416">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="04529-417">Добавлен необязательный параметр -PrivateLinkServiceNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к службе приватного канала в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="04529-417">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="04529-418">Параметр ServiceName командлета AzPrivateLinkService был переименован на Name с псевдонимом ServiceName для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="04529-418">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="04529-419">Включен протокол ICMP для настройки правил безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="04529-419">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="04529-420">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="04529-420">Updated cmdlets</span></span>
        - <span data-ttu-id="04529-421">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="04529-421">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="04529-422">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="04529-422">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="04529-423">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="04529-423">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="04529-424">Добавлен ConnectionProtocolType (Ikev1/Ikev2) в качестве настраиваемого параметра для командлета New-AzVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="04529-424">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="04529-425">Добавлен PrivateIpAddressVersion в LoadBalancerFrontendIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="04529-425">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="04529-426">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="04529-426">Updated cmdlet:</span></span>
        - <span data-ttu-id="04529-427">New-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="04529-427">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="04529-428">Add-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="04529-428">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="04529-429">Set-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="04529-429">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="04529-430">Команда New-AzApplicationGatewayProbeConfig Шлюза приложений обновлена для поддержки настраиваемого порта в зонде.</span><span class="sxs-lookup"><span data-stu-id="04529-430">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="04529-431">Обновлен командлет New-AzApplicationGatewayProbeConfig: добавлен необязательный параметр Port, который используется при проверке внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="04529-431">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="04529-432">Этот параметр применяется к номерам SKU Standard_V2 и WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="04529-432">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="04529-433">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="04529-433">Az.OperationalInsights</span></span>
* <span data-ttu-id="04529-434">Обновленная версия по умолчанию для сохраненных операций поиска имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="04529-434">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="04529-435">Исправлены ошибки при обработке регулярных выражений со значениями NULL в журналах.</span><span class="sxs-lookup"><span data-stu-id="04529-435">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="04529-436">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="04529-436">Az.RecoveryServices</span></span>
* <span data-ttu-id="04529-437">Обновлен файл Get-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="04529-437">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="04529-438">Обновлен файл Get-AzRecoveryServicesBackupContainer.md.</span><span class="sxs-lookup"><span data-stu-id="04529-438">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="04529-439">Обновлен файл Get-AzRecoveryServicesVault.md.</span><span class="sxs-lookup"><span data-stu-id="04529-439">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="04529-440">Обновлен файл Wait-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="04529-440">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="04529-441">Обновлен файл Set-AzRecoveryServicesVaultContext.md.</span><span class="sxs-lookup"><span data-stu-id="04529-441">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="04529-442">Обновлен файл Get-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="04529-442">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="04529-443">Обновлен файл Get-AzRecoveryServicesBackupRecoveryPoint.md.</span><span class="sxs-lookup"><span data-stu-id="04529-443">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="04529-444">Обновлен файл Restore-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="04529-444">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="04529-445">Обновлен вызов службы для отмены регистрации контейнера в общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="04529-445">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="04529-446">Обновлен файл Set-AzRecoveryServicesAsrAlertSetting.md.</span><span class="sxs-lookup"><span data-stu-id="04529-446">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="04529-447">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="04529-447">Az.Resources</span></span>
- <span data-ttu-id="04529-448">Удален отсутствующий командлет, который упоминается в документации по New-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="04529-448">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="04529-449">Обновлены командлеты политик для использования новой версии API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="04529-449">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="04529-450">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="04529-450">Az.ServiceBus</span></span>
* <span data-ttu-id="04529-451">Добавлен новый командлет для создания маркера SAS: New-AzServiceBusAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="04529-451">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="04529-452">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="04529-452">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="04529-453">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="04529-453">Az.Sql</span></span>
* <span data-ttu-id="04529-454">Исправлены отсутствующие примеры для командлета Set-AzSqlDatabaseSecondary.</span><span class="sxs-lookup"><span data-stu-id="04529-454">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="04529-455">Исправлены заданные повторяющиеся проверки для оценки наличия уязвимостей без указания адресов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="04529-455">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="04529-456">Исправлена незначительная опечатка в сообщении предупреждения.</span><span class="sxs-lookup"><span data-stu-id="04529-456">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="04529-457">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="04529-457">Az.Storage</span></span>
* <span data-ttu-id="04529-458">Обновлен пример в справочной документации для использования командлетом Get-AzStorageAccount правильного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="04529-458">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="04529-459">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="04529-459">Az.StorageSync</span></span>
* <span data-ttu-id="04529-460">Добавлен командлет Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="04529-460">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="04529-461">Исправлена проблема № 9551, связанная с TierFilesOlderThanDays.</span><span class="sxs-lookup"><span data-stu-id="04529-461">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="04529-462">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="04529-462">Az.Websites</span></span>
* <span data-ttu-id="04529-463">Исправлена ошибка, при которой некоторые свойства SiteConfig не возвращались Get-AzWebApp и Set-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="04529-463">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="04529-464">Добавлен новый параметр Location в Get-AzDeletedWebApp и Restore-AzDeletedWebApp.</span><span class="sxs-lookup"><span data-stu-id="04529-464">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="04529-465">Исправлена ошибка, которая возникала при клонировании слотов веб-приложений с помощью командлета New-AzWebApp-IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="04529-465">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="04529-466">2.4.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="04529-466">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="04529-467">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="04529-467">Az.Accounts</span></span>
* <span data-ttu-id="04529-468">Добавлена поддержка командлетов профиля.</span><span class="sxs-lookup"><span data-stu-id="04529-468">Add support for profile cmdlets</span></span>
* <span data-ttu-id="04529-469">Добавлена поддержка сред и плоскостей данных в созданных командлетах.</span><span class="sxs-lookup"><span data-stu-id="04529-469">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="04529-470">Исправлена ошибка, когда в командлетах плоскости данных в Windows PowerShell в некоторых случаях использовалась неправильная конечная точка.</span><span class="sxs-lookup"><span data-stu-id="04529-470">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="04529-471">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="04529-471">Az.Advisor</span></span>
* <span data-ttu-id="04529-472">Выпущена общедоступная версия Az.Advisor.</span><span class="sxs-lookup"><span data-stu-id="04529-472">GA release of Az.Advisor</span></span>
* <span data-ttu-id="04529-473">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="04529-473">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="04529-474">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="04529-474">Az.ApiManagement</span></span>
* <span data-ttu-id="04529-475">исправлена проблема https://github.com/Azure/azure-powershell/issues/8671.</span><span class="sxs-lookup"><span data-stu-id="04529-475">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="04529-476">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="04529-476">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="04529-477">Добавлена поддержка запрашивания подписок по пользователю и продукту.</span><span class="sxs-lookup"><span data-stu-id="04529-477">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="04529-478">Добавлена поддержка создания запросов с использованием области "/", "/apis", "/apis/echo-api".</span><span class="sxs-lookup"><span data-stu-id="04529-478">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="04529-479">Исправлены проблемы https://github.com/Azure/azure-powershell/issues/9307 и https://github.com/Azure/azure-powershell/issues/8432.</span><span class="sxs-lookup"><span data-stu-id="04529-479">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="04529-480">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="04529-480">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="04529-481">Добавлена поддержка указания ApiVersion и ApiVersionSetId при импорте API-интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="04529-481">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="04529-482">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="04529-482">Az.Automation</span></span>
* <span data-ttu-id="04529-483">Исправлена ошибка командлета Set-AzAutomationConnectionFieldValue при обработке строкового значения.</span><span class="sxs-lookup"><span data-stu-id="04529-483">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="04529-484">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="04529-484">Az.Compute</span></span>
* <span data-ttu-id="04529-485">В New AzImageConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="04529-485">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="04529-486">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="04529-486">Az.DataFactory</span></span>
* <span data-ttu-id="04529-487">Обновление выходных данных командлетов ADF, предназначенных для получения числа выполнений действий, конвейеров и триггеров, для поддержки канала Select-Object.</span><span class="sxs-lookup"><span data-stu-id="04529-487">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="04529-488">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="04529-488">Az.EventGrid</span></span>
* <span data-ttu-id="04529-489">Исправлена опечатка в документации по командлету New-AzEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="04529-489">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="04529-490">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="04529-490">Az.IotHub</span></span>
* <span data-ttu-id="04529-491">Добавлена поддержка повторного создания ключей политики авторизации.</span><span class="sxs-lookup"><span data-stu-id="04529-491">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="04529-492">Az.Network</span><span class="sxs-lookup"><span data-stu-id="04529-492">Az.Network</span></span>
* <span data-ttu-id="04529-493">К тегам общедоступного IP-адреса добавлен тег RoutingPreference.</span><span class="sxs-lookup"><span data-stu-id="04529-493">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="04529-494">Улучшены примеры для справочной документации по командлету Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="04529-494">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="04529-495">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="04529-495">Az.PolicyInsights</span></span>
* <span data-ttu-id="04529-496">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="04529-496">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="04529-497">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9446.</span><span class="sxs-lookup"><span data-stu-id="04529-497">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="04529-498">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="04529-498">Az.OperationalInsights</span></span>
* <span data-ttu-id="04529-499">Исправленная модель источника данных CustomLog возвращена в командлет Get-AzOperationalInsightsDataSource.</span><span class="sxs-lookup"><span data-stu-id="04529-499">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="04529-500">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="04529-500">Az.RecoveryServices</span></span>
* <span data-ttu-id="04529-501">Выпущено исправление для команды get-policy для виртуальных машин IaaS.</span><span class="sxs-lookup"><span data-stu-id="04529-501">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="04529-502">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="04529-502">Az.Resources</span></span>
    - <span data-ttu-id="04529-503">Исправлен текст справки по параметру Get-AzPolicyState -Top.</span><span class="sxs-lookup"><span data-stu-id="04529-503">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="04529-504">Добавлена поддержка разбиения по страницам на стороне клиента для Get-AzPolicyAlias.</span><span class="sxs-lookup"><span data-stu-id="04529-504">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="04529-505">Добавлены новые параметры для Set-AzPolicyAssignment, -PolicyParameters и -PolicyParametersObject.</span><span class="sxs-lookup"><span data-stu-id="04529-505">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="04529-506">Добавлен ряд обновлений документов и примеров для командлетов политик.</span><span class="sxs-lookup"><span data-stu-id="04529-506">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="04529-507">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="04529-507">Az.ServiceBus</span></span>
* <span data-ttu-id="04529-508">Исправление ошибки № 4938: командлет New-AzureRmServiceBusQueue возвращает ответ BadRequest (Недопустимый запрос) при задании значения MaxSizeInMegabytes.</span><span class="sxs-lookup"><span data-stu-id="04529-508">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="04529-509">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="04529-509">Az.Sql</span></span>
* <span data-ttu-id="04529-510">Из выпуска предварительной версии в выпуск общедоступной версии добавлены командлеты группы отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="04529-510">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="04529-511">Поддержка аудита Azure SQL Server и баз данных с помощью новых командлетов:</span><span class="sxs-lookup"><span data-stu-id="04529-511">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="04529-512">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="04529-512">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="04529-513">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="04529-513">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="04529-514">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="04529-514">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="04529-515">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="04529-515">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="04529-516">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="04529-516">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="04529-517">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="04529-517">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="04529-518">Из параметров оценки уязвимостей удалены ограничения, касающиеся электронной почты.</span><span class="sxs-lookup"><span data-stu-id="04529-518">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="04529-519">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="04529-519">Az.Storage</span></span>
* <span data-ttu-id="04529-520">Два параметра в указанном ниже командлете — -IndexDocument и -ErrorDocument404Path, — которые ранее были обязательными, стали необязательными:</span><span class="sxs-lookup"><span data-stu-id="04529-520">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="04529-521">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="04529-521">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="04529-522">Обновлена справка по командлету Get-AzStorageBlobContent: добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="04529-522">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="04529-523">При сбое выполнения командлета с ошибкой StorageException отображаются дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="04529-523">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="04529-524">Добавлена поддержка создания или обновления учетной записи хранения с использованием проверки подлинности AAD DS для службы "Файлы Azure".</span><span class="sxs-lookup"><span data-stu-id="04529-524">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="04529-525">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="04529-525">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="04529-526">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="04529-526">Set-AzStorageAccount</span></span>
* <span data-ttu-id="04529-527">Добавлена поддержка перечисления или закрытия дескрипторов файлов для общей папки, каталога файлов или файла:</span><span class="sxs-lookup"><span data-stu-id="04529-527">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="04529-528">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="04529-528">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="04529-529">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="04529-529">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="04529-530">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="04529-530">Az.StorageSync</span></span>
* <span data-ttu-id="04529-531">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="04529-531">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="04529-532">2.3.2 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="04529-532">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="04529-533">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="04529-533">Az.Accounts</span></span>
* <span data-ttu-id="04529-534">Исправлена ошибка, связанная с использованием неправильного URL-адреса для вызовов функций.</span><span class="sxs-lookup"><span data-stu-id="04529-534">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="04529-535">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8983.</span><span class="sxs-lookup"><span data-stu-id="04529-535">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="04529-536">Устранена проблема с псевдонимами из AzureRM для командлетов Az.</span><span class="sxs-lookup"><span data-stu-id="04529-536">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="04529-537">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="04529-537">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="04529-538">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest.</span><span class="sxs-lookup"><span data-stu-id="04529-538">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="04529-539">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="04529-539">Az.Compute</span></span>
* <span data-ttu-id="04529-540">Простые наборы параметров New-AzVm и New-AzVmss теперь принимают параметр ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="04529-540">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="04529-541">Исправлена опечатка в справочной документации по New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="04529-541">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="04529-542">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="04529-542">Az.Dns</span></span>
* <span data-ttu-id="04529-543">Исправлена опечатка в справочных примерах по использованию Set-AzDnsZone.</span><span class="sxs-lookup"><span data-stu-id="04529-543">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="04529-544">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="04529-544">Az.EventGrid</span></span>
* <span data-ttu-id="04529-545">Обновлен для использования API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="04529-545">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="04529-546">Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="04529-546">New cmdlets:</span></span>
    - <span data-ttu-id="04529-547">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="04529-547">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="04529-548">Создает домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="04529-548">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="04529-549">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="04529-549">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="04529-550">Возвращает сведения о домене Сетки событий или список всех доменов Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="04529-550">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="04529-551">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="04529-551">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="04529-552">Удаляет домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="04529-552">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="04529-553">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="04529-553">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="04529-554">Повторно создает ключ общего доступа для домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="04529-554">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="04529-555">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="04529-555">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="04529-556">Возвращает ключи общего доступа, используемые для публикации событий в домене Сетки событий.</span><span class="sxs-lookup"><span data-stu-id="04529-556">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="04529-557">New-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="04529-557">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="04529-558">Создает раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="04529-558">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="04529-559">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="04529-559">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="04529-560">Возвращает сведения о разделе домена Сетки событий или список всех разделов определенного домена Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="04529-560">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="04529-561">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="04529-561">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="04529-562">Удаляет раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="04529-562">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="04529-563">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="04529-563">Updated cmdlets:</span></span>
    - <span data-ttu-id="04529-564">New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="04529-564">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="04529-565">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для нового домена Сетки событий и раздела домена Сетки событий и позволяющие создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="04529-565">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="04529-566">Добавляют новые обязательные параметры для указания имени нового домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="04529-566">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="04529-567">Добавляют новые наборы параметров для доменов и разделов домена и позволяют повторно использовать существующие параметры (например, EndPointType, SubjectBeginsWith и т. д.).</span><span class="sxs-lookup"><span data-stu-id="04529-567">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="04529-568">Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="04529-568">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="04529-569">срока действия подписки на событие;</span><span class="sxs-lookup"><span data-stu-id="04529-569">Event subscription expiration date,</span></span>
            - <span data-ttu-id="04529-570">параметров расширенной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="04529-570">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="04529-571">Добавляют новое перечисление для ServiceBusQueue в качестве места назначения.</span><span class="sxs-lookup"><span data-stu-id="04529-571">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="04529-572">Запрещают использование значение All в параметре -IncludedEventType и заменяют его следующим:</span><span class="sxs-lookup"><span data-stu-id="04529-572">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="04529-573">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="04529-573">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="04529-574">Добавляют новые необязательные параметры (Top, ODataQuery и NextLink) для поддержки разбиения на страницы и фильтрации результатов.</span><span class="sxs-lookup"><span data-stu-id="04529-574">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="04529-575">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="04529-575">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="04529-576">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для домена Сетки событий и раздела домена Сетки событий и позволяющие удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="04529-576">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="04529-577">Добавляют новые обязательные параметры для указания имени домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="04529-577">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="04529-578">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="04529-578">Az.FrontDoor</span></span>
* <span data-ttu-id="04529-579">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="04529-579">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="04529-580">Добавляет поддержку преобразований и новое значение оператора автозавершения (RegEx).</span><span class="sxs-lookup"><span data-stu-id="04529-580">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="04529-581">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="04529-581">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="04529-582">Добавляет новые значения автозавершения.</span><span class="sxs-lookup"><span data-stu-id="04529-582">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="04529-583">Az.Network</span><span class="sxs-lookup"><span data-stu-id="04529-583">Az.Network</span></span>
* <span data-ttu-id="04529-584">Добавляет поддержку ресурса шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="04529-584">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="04529-585">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="04529-585">New cmdlets</span></span>
        - <span data-ttu-id="04529-586">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="04529-586">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="04529-587">Добавляет AvailablePrivateEndpointType.</span><span class="sxs-lookup"><span data-stu-id="04529-587">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="04529-588">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="04529-588">New cmdlets</span></span> 
        - <span data-ttu-id="04529-589">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="04529-589">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="04529-590">Добавляет PrivatePrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="04529-590">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="04529-591">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="04529-591">New cmdlets</span></span> 
        - <span data-ttu-id="04529-592">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="04529-592">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="04529-593">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="04529-593">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="04529-594">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="04529-594">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="04529-595">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="04529-595">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="04529-596">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="04529-596">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="04529-597">Добавляет PrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="04529-597">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="04529-598">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="04529-598">New cmdlets</span></span>
        - <span data-ttu-id="04529-599">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="04529-599">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="04529-600">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="04529-600">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="04529-601">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="04529-601">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="04529-602">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="04529-602">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="04529-603">Обновлены следующие команды для функции: флаг UseLocalAzureIpAddress для VPN-подключения.</span><span class="sxs-lookup"><span data-stu-id="04529-603">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="04529-604">Обновлен командлет New-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="04529-604">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="04529-605">Обновлен командлет Set-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="04529-605">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="04529-606">В пиринг ExpressRoute добавлено поле только для чтения PeeredConnections.</span><span class="sxs-lookup"><span data-stu-id="04529-606">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="04529-607">В ExpressRoute добавлено поле только для чтения GlobalReachEnabled.</span><span class="sxs-lookup"><span data-stu-id="04529-607">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="04529-608">Добавлен атрибут в рамках критического изменения, отменяющего статус устаревшего поля AllowGlobalReach в модели ExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="04529-608">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="04529-609">Исправлена проблема, связанная с ошибкой 8756, при использовании TargetListenerID с командлетами AzApplicationGatewayRedirectConfiguration.</span><span class="sxs-lookup"><span data-stu-id="04529-609">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="04529-610">Исправлена ошибка в New-AzApplicationGatewayPathRuleConfig, не позволявшая задавать набор правил повторного создания.</span><span class="sxs-lookup"><span data-stu-id="04529-610">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="04529-611">Исправлено отображение VirtualNetworkTaps в NetworkInterfaceIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="04529-611">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="04529-612">Исправлены командлеты Cortex Get для отображения всех частей.</span><span class="sxs-lookup"><span data-stu-id="04529-612">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="04529-613">Исправлено создание ссылок VirtualHub для ExpressRouteGateways и VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="04529-613">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="04529-614">В AzureFirewall и NatGateway добавлена поддержка Зон доступности.</span><span class="sxs-lookup"><span data-stu-id="04529-614">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="04529-615">Добавлен командлет Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="04529-615">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="04529-616">Добавлена поддержка нескольких общедоступных IP-адресов для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="04529-616">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="04529-617">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="04529-617">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="04529-618">Добавлен параметр -PublicIpAddress, который принимает один или несколько объектов общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="04529-618">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="04529-619">Добавлен параметр -VirtualNetwork, который принимает объект виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="04529-619">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="04529-620">Добавлены методы AddPublicIpAddress и RemovePublicIpAddress для объекта брандмауэра. Они принимают объект общедоступного IP-адреса в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="04529-620">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="04529-621">Не рекомендуется использовать параметры -PublicIpName и -VirtualNetworkName.</span><span class="sxs-lookup"><span data-stu-id="04529-621">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="04529-622">Обновлены следующие команды для функции: В параметрах проверки подлинности AAD VPN-клиента задан ресурс шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="04529-622">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="04529-623">Обновлен командлет New-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="04529-623">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="04529-624">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="04529-624">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="04529-625">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр-переключатель RemoveAadAuthentication для удаления в шлюзе параметров проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="04529-625">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="04529-626">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="04529-626">Az.OperationalInsights</span></span>
* <span data-ttu-id="04529-627">Добавлена поддержка SKU **pergb2018** в команде New-AzureRmOperationalInsightsWorkspace.</span><span class="sxs-lookup"><span data-stu-id="04529-627">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="04529-628">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="04529-628">Az.Resources</span></span>
* <span data-ttu-id="04529-629">Поддержка дополнительных вариантов экспорта шаблона.</span><span class="sxs-lookup"><span data-stu-id="04529-629">Support for additional Template Export options</span></span>
    - <span data-ttu-id="04529-630">В Export-AzResourceGroup добавлен параметр -SkipResourceNameParameterization.</span><span class="sxs-lookup"><span data-stu-id="04529-630">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="04529-631">В Export-AzResourceGroup добавлен параметр -SkipAllParameterization.</span><span class="sxs-lookup"><span data-stu-id="04529-631">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="04529-632">В Export-AzResourceGroup добавлен параметр -Resource для фильтрации экспортированных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="04529-632">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="04529-633">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="04529-633">Az.ServiceFabric</span></span>
* <span data-ttu-id="04529-634">Исправлена ошибка, связанная с получением иногда неправильных отпечатков при добавлении сертификата ByExistingKeyVault.</span><span class="sxs-lookup"><span data-stu-id="04529-634">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="04529-635">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="04529-635">Az.Sql</span></span>
* <span data-ttu-id="04529-636">Исправлен суффикс конечной точки хранилища службы "Расширенная защита от угроз Azure".</span><span class="sxs-lookup"><span data-stu-id="04529-636">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="04529-637">Исправлена ошибка, связанная с возможностью пакета "Расширенная защита данных" переопределять политику службы "Расширенная защита от угроз".</span><span class="sxs-lookup"><span data-stu-id="04529-637">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="04529-638">Новые командлеты для Management.Sql позволяют клиентам добавлять ключи TDE и задавать средство защиты TDE для управляемых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="04529-638">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="04529-639">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="04529-639">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="04529-640">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="04529-640">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="04529-641">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="04529-641">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="04529-642">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="04529-642">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="04529-643">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="04529-643">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="04529-644">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="04529-644">Az.Storage</span></span>
* <span data-ttu-id="04529-645">Поддержка класса Kind в FileStorage и значения Premium_ZRS в SkuName при создании учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="04529-645">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="04529-646">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="04529-646">New-AzStorageAccount</span></span>
* <span data-ttu-id="04529-647">Уточнено описание командлета неизменности BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="04529-647">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="04529-648">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="04529-648">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="04529-649">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="04529-649">Az.Websites</span></span>
* <span data-ttu-id="04529-650">Оптимизирует Get-AzWebAppCertificate для фильтрации по группе ресурсов на сервере, а не в клиенте.</span><span class="sxs-lookup"><span data-stu-id="04529-650">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="04529-651">Добавляет параметр-переключатель - UseDisasterRecovery в Get AzWebAppSnapshot.</span><span class="sxs-lookup"><span data-stu-id="04529-651">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="04529-652">2.2.0 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="04529-652">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="04529-653">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="04529-653">Az.Cdn</span></span>
* <span data-ttu-id="04529-654">Обновлены командлеты для поддержки функции rulesEngine на основе API версии 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="04529-654">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="04529-655">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="04529-655">Az.Compute</span></span>
* <span data-ttu-id="04529-656">Добавлен параметр `NoWait`, который запускает операцию и немедленно возвращает значение еще до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="04529-656">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="04529-657">Обновлены командлеты:   Export-AzLogAnalyticRequestRateByInterval; Export-AzLogAnalyticThrottledRequest; Remove-AzVM; Remove-AzVMAccessExtension; Remove-AzVMAEMExtension; Remove-AzVMChefExtension; Remove-AzVMCustomScriptExtension; Remove-AzVMDiagnosticsExtension; Remove-AzVMDiskEncryptionExtension; Remove-AzVMDscExtension; Remove-AzVMSqlServerExtension; Restart-AzVM; Set-AzVM; Set-AzVMAccessExtension; Set-AzVMADDomainExtension; Set-AzVMAEMExtension; Set-AzVMBginfoExtension; Set-AzVMChefExtension; Set-AzVMCustomScriptExtension; Set-AzVMDiagnosticsExtension; Set-AzVMDscExtension; Set-AzVMExtension; Start-AzVM; Stop-AzVM; Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="04529-657">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="04529-658">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="04529-658">Az.EventHub</span></span>
* <span data-ttu-id="04529-659">Исправлена ошибка № 9231. Командлет Get-AzEventHubNamespace не возвращал теги.</span><span class="sxs-lookup"><span data-stu-id="04529-659">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="04529-660">Исправлена ошибка № 9230. Командлет Get-AzEventHubNamespace возвращал значение ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="04529-660">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="04529-661">Az.Network</span><span class="sxs-lookup"><span data-stu-id="04529-661">Az.Network</span></span>
* <span data-ttu-id="04529-662">Обновлены параметры ResourceId и InputObject для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="04529-662">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="04529-663">Добавлены псевдонимы для параметров ResourceId и InputObject.</span><span class="sxs-lookup"><span data-stu-id="04529-663">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="04529-664">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="04529-664">Az.PolicyInsights</span></span>
* <span data-ttu-id="04529-665">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyEvent.</span><span class="sxs-lookup"><span data-stu-id="04529-665">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="04529-666">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="04529-666">Az.RecoveryServices</span></span>
* <span data-ttu-id="04529-667">Минимальный срок хранения политики IaaSVM изменился с 1 до 7 дней.</span><span class="sxs-lookup"><span data-stu-id="04529-667">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="04529-668">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="04529-668">Az.ServiceBus</span></span>
* <span data-ttu-id="04529-669">Исправлена ошибка № 9182. Командлет Get-AzServiceBusNamespace возвращал ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="04529-669">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="04529-670">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="04529-670">Az.ServiceFabric</span></span>
* <span data-ttu-id="04529-671">Исправлена опечатка в сообщении об ошибке для командлета Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="04529-671">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="04529-672">Исправлен отсутствующей символ в командных строках Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="04529-672">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="04529-673">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="04529-673">Az.Sql</span></span>
* <span data-ttu-id="04529-674">Для командлета New-AzureSqlInstance добавлен параметр DnsZonePartner, обеспечивающий поддержку AutoDr для Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="04529-674">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="04529-675">Командлет Get-AzSqlDatabaseSecureConnectionPolicy объявлен неподдерживаемым.</span><span class="sxs-lookup"><span data-stu-id="04529-675">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="04529-676">Командлеты обнаружения угроз переименованы в командлеты Расширенной защиты от угроз.</span><span class="sxs-lookup"><span data-stu-id="04529-676">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="04529-677">Параметры -StorageSizeInGB и -LicenseType командлета New-AzSqlInstance теперь необязательны.</span><span class="sxs-lookup"><span data-stu-id="04529-677">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="04529-678">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="04529-678">Az.Websites</span></span>
* <span data-ttu-id="04529-679">Исправлены проблемы, когда удалялись теги при использовании Set-AzWebApp и Set-AzWebAppSlot со свойством -WebApp.</span><span class="sxs-lookup"><span data-stu-id="04529-679">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="04529-680">2.1.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="04529-680">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="04529-681">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="04529-681">Az.ApiManagement</span></span>
* <span data-ttu-id="04529-682">Созданы командлеты для управления диагностикой в глобальной области и в области API.</span><span class="sxs-lookup"><span data-stu-id="04529-682">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="04529-683">**Get-AzApiManagementDiagnostic** — получение диагностики, заданной глобально или на уровне области API.</span><span class="sxs-lookup"><span data-stu-id="04529-683">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="04529-684">**New-AzApiManagementDiagnostic** — создание диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="04529-684">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="04529-685">**New-AzApiManagementHttpMessageDiagnostic** — создание параметра диагностики, для которого регистрируются заголовки и размер байтов тела.</span><span class="sxs-lookup"><span data-stu-id="04529-685">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="04529-686">**New-AzApiManagementPipelineDiagnosticSetting** — создание параметров диагностики для сообщений HTTP, поступающих в шлюз или исходящих из него.</span><span class="sxs-lookup"><span data-stu-id="04529-686">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="04529-687">**New-AzApiManagementSamplingSetting** — создание параметра выборки для запросов и ответов касательно диагностики.</span><span class="sxs-lookup"><span data-stu-id="04529-687">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="04529-688">**Remove-AzApiManagementDiagnostic** — удаление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="04529-688">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="04529-689">**Set-AzApiManagementDiagnostic** — обновление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="04529-689">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="04529-690">Созданы командлеты для управления кэшем в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="04529-690">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="04529-691">**Get-AzApiManagementCache** — получение сведений о кэше, указанном идентификатором, или обо всех кэшах.</span><span class="sxs-lookup"><span data-stu-id="04529-691">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="04529-692">**New-AzApiManagementCache** — создание кэша по умолчанию или кэша в определенном регионе Azure.</span><span class="sxs-lookup"><span data-stu-id="04529-692">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="04529-693">**Remove-AzApiManagementCache** — удаление кэша.</span><span class="sxs-lookup"><span data-stu-id="04529-693">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="04529-694">**Update-AzApiManagementCache** — обновление кэша.</span><span class="sxs-lookup"><span data-stu-id="04529-694">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="04529-695">Созданы командлеты для управления схемой API.</span><span class="sxs-lookup"><span data-stu-id="04529-695">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="04529-696">**New-AzApiManagementSchema** — создание схемы для API.</span><span class="sxs-lookup"><span data-stu-id="04529-696">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="04529-697">**Get-AzApiManagementSchema** — получение схем, настроенных в API.</span><span class="sxs-lookup"><span data-stu-id="04529-697">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="04529-698">**Remove-AzApiManagementSchema** — удаление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="04529-698">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="04529-699">**Set-AzApiManagementSchema** — обновление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="04529-699">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="04529-700">Создан командлет для создания токена пользователя.</span><span class="sxs-lookup"><span data-stu-id="04529-700">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="04529-701">**New-AzApiManagementUserToken** — создание токена пользователя, по умолчанию действительного в течение 8 часов. С помощью этого командлета можно создавать токен для пользователя GIT.</span><span class="sxs-lookup"><span data-stu-id="04529-701">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="04529-702">Создан командлет для получения состояния сети.</span><span class="sxs-lookup"><span data-stu-id="04529-702">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="04529-703">**Get-AzApiManagementNetworkStatus** — получение состояния сети ресурсов, от которых зависит служба "Управление API".</span><span class="sxs-lookup"><span data-stu-id="04529-703">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="04529-704">Это полезно при развертывании службы ApiManagement в виртуальной сети и проверке того, не нарушена ли какая-либо из зависимостей.</span><span class="sxs-lookup"><span data-stu-id="04529-704">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="04529-705">Обновлен командлет **New-AzApiManagement** для управления службой ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="04529-705">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="04529-706">Добавлена поддержка нового SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="04529-706">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="04529-707">Добавлена поддержка для включения флага EnableClientCertificate в SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="04529-707">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="04529-708">Новый командлет **New-AzApiManagementSslSetting** позволяет настраивать параметр TLS/SSL для сервера (Backend) и внешнего интерфейса (Frontend).</span><span class="sxs-lookup"><span data-stu-id="04529-708">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="04529-709">Его также можно использовать для настройки Ciphers как 3DES, в ServerProtocols как Http2 для внешнего интерфейса (Frontend) службы ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="04529-709">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="04529-710">Добавлена поддержка настройки имени узла DeveloperPortal в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="04529-710">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="04529-711">Обновлен командлет **Get-AzApiManagementSsoToken** для извлечения объекта PsApiManagement в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="04529-711">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="04529-712">Обновлен командлет для отображения встроенных сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="04529-712">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="04529-713">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Код ошибки: ValidationError. Сообщение об ошибке: "Некоторые поля содержат неправильные значения". Сведения об ошибке: [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="04529-713">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="04529-714">Обновлен командлет **Export-AzApiManagementApi** для экспортирования программных интерфейсов в формате OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="04529-714">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="04529-715">Обновлен командлет **Import-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="04529-715">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="04529-716">Для импортирования API из спецификации документа OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="04529-716">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="04529-717">Для переопределения свойства PsApiManagementSchema, указанного в любом документе (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="04529-717">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="04529-718">Для переопределения свойства ServiceUrl, указанного в любом документе.</span><span class="sxs-lookup"><span data-stu-id="04529-718">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="04529-719">Обновлен командлет **Get-AzApiManagementPolicy** для возврата политики в формате, экранированном не для XML, с использованием rawxml.</span><span class="sxs-lookup"><span data-stu-id="04529-719">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="04529-720">Обновлен командлет **Set-AzApiManagementPolicy**. Он принимает политику в формате, экранированном не для XML, с использованием rawxml и в формате, экранированном для XML, с использованием XML.</span><span class="sxs-lookup"><span data-stu-id="04529-720">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="04529-721">Обновлен командлет **New-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="04529-721">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="04529-722">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="04529-722">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="04529-723">Для создания API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="04529-723">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="04529-724">Для клонирования API с использованием значений SourceApiId и SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="04529-724">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="04529-725">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="04529-725">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="04529-726">Обновлен командлет **Set-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="04529-726">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="04529-727">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="04529-727">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="04529-728">Для обновления API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="04529-728">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="04529-729">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="04529-729">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="04529-730">Обновлен командлет **New-AzApiManagementRevision**:</span><span class="sxs-lookup"><span data-stu-id="04529-730">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="04529-731">Для клонирования (копирования тегов, продуктов, операций и политик) существующей редакции с использованием SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="04529-731">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="04529-732">Новая редакция предполагает родительский идентификатор ApiId.</span><span class="sxs-lookup"><span data-stu-id="04529-732">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="04529-733">Для предоставления ApiRevisionDescription.</span><span class="sxs-lookup"><span data-stu-id="04529-733">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="04529-734">Для переопределения значения ServiceUrl при клонировании API.</span><span class="sxs-lookup"><span data-stu-id="04529-734">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="04529-735">Обновлен командлет **New-AzApiManagementIdentityProvider**:</span><span class="sxs-lookup"><span data-stu-id="04529-735">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="04529-736">Для настройки AAD или AADB2C с Authority.</span><span class="sxs-lookup"><span data-stu-id="04529-736">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="04529-737">Для установки политик SignupPolicy, SigninPolicy, ProfileEditingPolicy и PasswordResetPolicy.</span><span class="sxs-lookup"><span data-stu-id="04529-737">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="04529-738">Обновлен командлет **New-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="04529-738">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="04529-739">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="04529-739">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="04529-740">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="04529-740">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="04529-741">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="04529-741">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="04529-742">Обновлен командлет **Set-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="04529-742">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="04529-743">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="04529-743">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="04529-744">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="04529-744">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="04529-745">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="04529-745">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="04529-746">Следующие командлеты обновлены, чтобы принимать значение ResourceId в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="04529-746">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="04529-747">New-AzApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="04529-747">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="04529-748">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="04529-748">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="04529-749">Get-AzApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="04529-749">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="04529-750">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="04529-750">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="04529-751">Get-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="04529-751">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="04529-752">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="04529-752">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="04529-753">Get-AzApiManagementAuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="04529-753">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="04529-754">Get-AzApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="04529-754">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="04529-755">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="04529-755">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="04529-756">Get-AzApiManagementCertificate.</span><span class="sxs-lookup"><span data-stu-id="04529-756">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="04529-757">Remove-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="04529-757">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="04529-758">Remove-AzApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="04529-758">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="04529-759">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="04529-759">Az.Automation</span></span>
* <span data-ttu-id="04529-760">Обновлен командлет Get-AzAutomationJobOutputRecord для обработки значений в формате JSON и в виде текстовой записи.</span><span class="sxs-lookup"><span data-stu-id="04529-760">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="04529-761">исправлена проблема https://github.com/Azure/azure-powershell/issues/7977.</span><span class="sxs-lookup"><span data-stu-id="04529-761">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="04529-762">исправлена проблема https://github.com/Azure/azure-powershell/issues/8600.</span><span class="sxs-lookup"><span data-stu-id="04529-762">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="04529-763">Поведение командлета Start-AzAutomationDscCompilationJob изменено так, чтобы сразу же запустить задание, а не ждать его завершения.</span><span class="sxs-lookup"><span data-stu-id="04529-763">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="04529-764">исправлена проблема https://github.com/Azure/azure-powershell/issues/8347.</span><span class="sxs-lookup"><span data-stu-id="04529-764">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="04529-765">Исправлен командлет Get-AzAutomationDscNode, возвращающий все узлы при использовании -Name.</span><span class="sxs-lookup"><span data-stu-id="04529-765">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="04529-766">Теперь он возвращает только соответствующий узел.</span><span class="sxs-lookup"><span data-stu-id="04529-766">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="04529-767">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="04529-767">Az.Compute</span></span>
* <span data-ttu-id="04529-768">Добавлены параметры ProtectFromScaleIn и ProtectFromScaleSetAction для командлета Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="04529-768">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="04529-769">Командлет New-AzVM с простым набором параметров теперь по умолчанию использует доступное расположение, если регион "восточная часть США" не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="04529-769">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="04529-770">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="04529-770">Az.DataLakeStore</span></span>
* <span data-ttu-id="04529-771">Обновлен пакет SDK ADLS для использования httpclient. В инфраструктуру Azure интегрирована проверка плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="04529-771">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="04529-772">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="04529-772">Az.Monitor</span></span>
* <span data-ttu-id="04529-773">Исправлены неправильные имена параметров в справочных примерах.</span><span class="sxs-lookup"><span data-stu-id="04529-773">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="04529-774">Az.Network</span><span class="sxs-lookup"><span data-stu-id="04529-774">Az.Network</span></span>
* <span data-ttu-id="04529-775">Добавлен флаг DisableBgpRoutePropagation для выходных данных действующей таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="04529-775">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="04529-776">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="04529-776">Updated cmdlet:</span></span>
        - <span data-ttu-id="04529-777">Get-AzEffectiveRouteTable.</span><span class="sxs-lookup"><span data-stu-id="04529-777">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="04529-778">Исправлен двойной дефис в документации New-AzApplicationGatewayTrustedRootCertificate.</span><span class="sxs-lookup"><span data-stu-id="04529-778">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="04529-779">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="04529-779">Az.Resources</span></span>
* <span data-ttu-id="04529-780">Добавлен новый командлет Get-AzureRmDenyAssignment для получения запрещающих назначений.</span><span class="sxs-lookup"><span data-stu-id="04529-780">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="04529-781">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="04529-781">Az.Sql</span></span>
* <span data-ttu-id="04529-782">Командлеты Расширенной защиты от угроз переименованы на командлеты Расширенной защиты данных, и оценка уязвимости включена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="04529-782">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="04529-783">2.0.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="04529-783">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="04529-784">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="04529-784">Az.Accounts</span></span>
* <span data-ttu-id="04529-785">Обновлена библиотека аутентификации для устранения проблем с ADFS при использовании аутентификации на основе имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="04529-785">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="04529-786">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="04529-786">Az.CognitiveServices</span></span>
* <span data-ttu-id="04529-787">Отображается только заявление об отказе Bing для служб Поиска Bing.</span><span class="sxs-lookup"><span data-stu-id="04529-787">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="04529-788">Исправлена проблема с созданием учетной записи.</span><span class="sxs-lookup"><span data-stu-id="04529-788">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="04529-789">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="04529-789">Az.Compute</span></span>
* <span data-ttu-id="04529-790">Функция группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="04529-790">Proximity placement group feature.</span></span>
    - <span data-ttu-id="04529-791">Добавлены следующие новые командлеты:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="04529-791">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="04529-792">Новый параметр ProximityPlacementGroupId будет добавлен в следующие командлеты:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="04529-792">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="04529-793">В командлет New-AzGalleryImageVersion добавлен параметр StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="04529-793">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="04529-794">TargetRegion в командлете New-AzGalleryImageVersion может содержать StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="04529-794">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="04529-795">Параметр-переключатель SkipShutdown добавлен в командлеты Stop-AzVM и Stop-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="04529-795">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="04529-796">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="04529-796">Breaking changes</span></span>
    - <span data-ttu-id="04529-797">Командлет SET-AzVMBootDiagnostics изменен на Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="04529-797">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="04529-798">Командлет Export-AzLogAnalyticThrottledRequests изменен на Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="04529-798">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="04529-799">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="04529-799">Az.DeploymentManager</span></span>
* <span data-ttu-id="04529-800">Первая общедоступная версия командлетов диспетчера развертывания Azure</span><span class="sxs-lookup"><span data-stu-id="04529-800">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="04529-801">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="04529-801">Az.Dns</span></span>
* <span data-ttu-id="04529-802">Автоматическое делегирование DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="04529-802">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="04529-803">Командлет для создания зоны DNS принимает имя родительской зоны в качестве дополнительного необязательного параметра.</span><span class="sxs-lookup"><span data-stu-id="04529-803">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="04529-804">Он добавляет записи NS в родительской зоне для созданной дочерней зоны.</span><span class="sxs-lookup"><span data-stu-id="04529-804">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="04529-805">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="04529-805">Az.FrontDoor</span></span>
* <span data-ttu-id="04529-806">Первая общедоступная версия командлетов Azure FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="04529-806">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="04529-807">Переименованы командлеты WAF для включения Waf.</span><span class="sxs-lookup"><span data-stu-id="04529-807">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="04529-808">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="04529-808">Az.HDInsight</span></span>
* <span data-ttu-id="04529-809">Удалены два командлета:</span><span class="sxs-lookup"><span data-stu-id="04529-809">Removed two cmdlets:</span></span>
    - <span data-ttu-id="04529-810">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="04529-810">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="04529-811">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="04529-811">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="04529-812">Добавлен новый командлет Set-AzHDInsightGatewayCredential для замены Grant-AzHDInsightHttpServicesAccess.</span><span class="sxs-lookup"><span data-stu-id="04529-812">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="04529-813">Обновлен командлет Get-AzHDInsightJobOutput для различения ролей читателя и оператора HDInsight:</span><span class="sxs-lookup"><span data-stu-id="04529-813">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="04529-814">Пользователям с ролью читателя не нужно указывать параметр DefaultStorageAccountKey явным образом, иначе возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="04529-814">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="04529-815">На пользователей с ролью оператора HDInsight это не повлияет.</span><span class="sxs-lookup"><span data-stu-id="04529-815">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="04529-816">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="04529-816">Az.Monitor</span></span>
* <span data-ttu-id="04529-817">Новые командлеты для API SQR (запланированное правило запросов)</span><span class="sxs-lookup"><span data-stu-id="04529-817">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="04529-818">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="04529-818">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="04529-819">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="04529-819">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="04529-820">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="04529-820">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="04529-821">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="04529-821">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="04529-822">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="04529-822">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="04529-823">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="04529-823">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="04529-824">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="04529-824">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="04529-825">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="04529-825">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="04529-826">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="04529-826">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="04529-827">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="04529-827">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="04529-828">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="04529-828">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="04529-829">См. подробнее об [API SQR](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules).</span><span class="sxs-lookup"><span data-stu-id="04529-829">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="04529-830">Обновлен файл Az.Monitor.md для включения командлетов для правила генерации оповещений на основе метрик GenV2(не классическая версия).</span><span class="sxs-lookup"><span data-stu-id="04529-830">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="04529-831">Az.Network</span><span class="sxs-lookup"><span data-stu-id="04529-831">Az.Network</span></span>
* <span data-ttu-id="04529-832">Добавлена поддержка для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="04529-832">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="04529-833">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="04529-833">New cmdlets</span></span>
        - <span data-ttu-id="04529-834">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="04529-834">New-AzNatGateway</span></span>
        - <span data-ttu-id="04529-835">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="04529-835">Get-AzNatGateway</span></span>
        - <span data-ttu-id="04529-836">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="04529-836">Set-AzNatGateway</span></span>
        - <span data-ttu-id="04529-837">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="04529-837">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="04529-838">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="04529-838">Updated cmdlets</span></span>
        - <span data-ttu-id="04529-839">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="04529-839">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="04529-840">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="04529-840">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="04529-841">Обновлены следующие команды для функции: Настройка и удаление пользовательских маршрутов через шлюз в Бруклине.</span><span class="sxs-lookup"><span data-stu-id="04529-841">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="04529-842">Обновлен командлет New-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="04529-842">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="04529-843">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="04529-843">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="04529-844">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="04529-844">Az.PolicyInsights</span></span>
* <span data-ttu-id="04529-845">Добавлена поддержка сведений об оценке политики запросов.</span><span class="sxs-lookup"><span data-stu-id="04529-845">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="04529-846">Добавлен параметр -Expand в командлет Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="04529-846">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="04529-847">Добавлена поддержка -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="04529-847">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="04529-848">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="04529-848">Az.RecoveryServices</span></span>
* <span data-ttu-id="04529-849">Добавлена поддержка перекрестной подписки на Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="04529-849">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="04529-850">Добавлена возможность отмечать предстоящие критически важные изменения для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="04529-850">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="04529-851">Исправлены план восстановления и план действий для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="04529-851">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="04529-852">Исправлено сетевое сопоставление обновления Azure Site Recovery (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="04529-852">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="04529-853">Исправлено направление защиты обновления Azure Site Recovery для управляемых дисков (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="04529-853">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="04529-854">Добавлены другие незначительные исправления.</span><span class="sxs-lookup"><span data-stu-id="04529-854">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="04529-855">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="04529-855">Az.Relay</span></span>
* <span data-ttu-id="04529-856">Исправлены опечатки в сообщениях для клиентов.</span><span class="sxs-lookup"><span data-stu-id="04529-856">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="04529-857">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="04529-857">Az.ServiceBus</span></span>
* <span data-ttu-id="04529-858">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="04529-858">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="04529-859">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="04529-859">Az.Storage</span></span>
* <span data-ttu-id="04529-860">Выполнено обновление клиентской библиотеки хранилища до версии 10.0.1 (пространство имен всех объектов из этого пакета SDK изменено с Microsoft.WindowsAzure.Storage. *на Microsoft.Azure.Storage*).</span><span class="sxs-lookup"><span data-stu-id="04529-860">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="04529-861">Выполнено обновление до Microsoft.Azure.Management.Storage версии 11.0.0 для включения поддержки нового API версии 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="04529-861">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="04529-862">Значение свойства Kind по умолчанию в учетной записи хранения изменено со Storage на StorageV2.</span><span class="sxs-lookup"><span data-stu-id="04529-862">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="04529-863">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="04529-863">New-AzStorageAccount</span></span>
* <span data-ttu-id="04529-864">Изменено значение Sku.Name в выходных данных командлета учетной записи хранения в соответствии со значением Sku.Name во входных данных путем добавления _ (например, StandardLRS изменено на Standard_LRS).</span><span class="sxs-lookup"><span data-stu-id="04529-864">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="04529-865">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="04529-865">New-AzStorageAccount</span></span>
    - <span data-ttu-id="04529-866">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="04529-866">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="04529-867">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="04529-867">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="04529-868">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="04529-868">Az.Websites</span></span>
* <span data-ttu-id="04529-869">Свойство Kind теперь будет задаваться объектам PSSite, возвращаемым командлетом Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="04529-869">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="04529-870">Get-AzWebApp\*Metrics и Get-AzAppServicePlanMetrics считаются нерекомендуемыми.</span><span class="sxs-lookup"><span data-stu-id="04529-870">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="04529-871">1.8.0 — апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="04529-871">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="04529-872">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="04529-872">Highlights since the last major release</span></span>
* <span data-ttu-id="04529-873">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="04529-873">General availability of `Az` module</span></span>
* <span data-ttu-id="04529-874">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="04529-874">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="04529-875">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="04529-875">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="04529-876">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="04529-876">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="04529-877">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="04529-877">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="04529-878">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="04529-878">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="04529-879">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="04529-879">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="04529-880">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="04529-880">Az.Accounts</span></span>
* <span data-ttu-id="04529-881">Обновлен командлет Uninstall-AzureRm для правильного удаления модулей в Mac.</span><span class="sxs-lookup"><span data-stu-id="04529-881">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="04529-882">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="04529-882">Az.Batch</span></span>
* <span data-ttu-id="04529-883">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="04529-883">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="04529-884">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="04529-884">Az.Cdn</span></span>
* <span data-ttu-id="04529-885">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="04529-885">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="04529-886">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="04529-886">Az.CognitiveServices</span></span>
* <span data-ttu-id="04529-887">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="04529-887">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="04529-888">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="04529-888">Az.Compute</span></span>
* <span data-ttu-id="04529-889">Устранена проблема с установкой AEM, если в идентификаторах ресурсов дисков группа ресурсов указана в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="04529-889">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="04529-890">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="04529-890">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="04529-891">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="04529-891">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="04529-892">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="04529-892">Az.DataFactory</span></span>
* <span data-ttu-id="04529-893">Добавлены свойства SsisProperties, если NodeCount не имеет значения NULL для управляемой среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="04529-893">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="04529-894">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="04529-894">Az.DataLakeStore</span></span>
* <span data-ttu-id="04529-895">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="04529-895">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="04529-896">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="04529-896">Az.EventGrid</span></span>
* <span data-ttu-id="04529-897">Обновлен текст справки для конечной точки, указывающий, что необходимо создать ресурсы, прежде чем использовать командлеты для создания или обновления подписки на события.</span><span class="sxs-lookup"><span data-stu-id="04529-897">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="04529-898">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="04529-898">Az.EventHub</span></span>
* <span data-ttu-id="04529-899">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="04529-899">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="04529-900">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="04529-900">Az.HDInsight</span></span>
* <span data-ttu-id="04529-901">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="04529-901">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="04529-902">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="04529-902">Az.IotHub</span></span>
* <span data-ttu-id="04529-903">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="04529-903">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="04529-904">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="04529-904">Az.KeyVault</span></span>
* <span data-ttu-id="04529-905">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="04529-905">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="04529-906">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="04529-906">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="04529-907">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="04529-907">Az.MachineLearning</span></span>
* <span data-ttu-id="04529-908">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="04529-908">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="04529-909">Az.Media</span><span class="sxs-lookup"><span data-stu-id="04529-909">Az.Media</span></span>
* <span data-ttu-id="04529-910">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="04529-910">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="04529-911">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="04529-911">Az.Monitor</span></span>
  * <span data-ttu-id="04529-912">Добавлены новые командлеты для правила генерации оповещений на основе метрик GenV2 (не классических).</span><span class="sxs-lookup"><span data-stu-id="04529-912">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="04529-913">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="04529-913">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="04529-914">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="04529-914">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="04529-915">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="04529-915">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="04529-916">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="04529-916">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="04529-917">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="04529-917">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="04529-918">Обновлен пакет SDK Monitor до предварительной версии 0.22.0.</span><span class="sxs-lookup"><span data-stu-id="04529-918">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="04529-919">Az.Network</span><span class="sxs-lookup"><span data-stu-id="04529-919">Az.Network</span></span>
* <span data-ttu-id="04529-920">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="04529-920">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="04529-921">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="04529-921">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="04529-922">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="04529-922">Az.NotificationHubs</span></span>
* <span data-ttu-id="04529-923">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="04529-923">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="04529-924">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="04529-924">Az.OperationalInsights</span></span>
* <span data-ttu-id="04529-925">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="04529-925">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="04529-926">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="04529-926">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="04529-927">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="04529-927">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="04529-928">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="04529-928">Az.RecoveryServices</span></span>
* <span data-ttu-id="04529-929">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="04529-929">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="04529-930">Обновлен табличный формат для SQL на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="04529-930">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="04529-931">Добавлен альтернативный метод для получения расположения в Общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="04529-931">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="04529-932">Обновлено значение ScheduleRunDays в объекте SchedulePolicy в соответствии с часовым поясом.</span><span class="sxs-lookup"><span data-stu-id="04529-932">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="04529-933">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="04529-933">Az.RedisCache</span></span>
* <span data-ttu-id="04529-934">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="04529-934">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="04529-935">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="04529-935">Az.Resources</span></span>
* <span data-ttu-id="04529-936">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="04529-936">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="04529-937">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="04529-937">Az.Sql</span></span>
* <span data-ttu-id="04529-938">Заменена зависимость от пакета SDK монитора на обычный код.</span><span class="sxs-lookup"><span data-stu-id="04529-938">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="04529-939">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="04529-939">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="04529-940">Улучшен процесс классификации нескольких столбцов.</span><span class="sxs-lookup"><span data-stu-id="04529-940">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="04529-941">Добавлены свойства SKU (имя, семейство, производительность SKU) в отклике Get-AzSqlServerServiceObjective, а также по умолчанию задан табличный формат.</span><span class="sxs-lookup"><span data-stu-id="04529-941">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="04529-942">C помощью Get-AzSqlServerServiceObjective теперь можно получать список доступных целевых служб по расположению без необходимости заранее размещать сервер в регионе.</span><span class="sxs-lookup"><span data-stu-id="04529-942">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="04529-943">Поддерживается параметр часового пояса при создании Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="04529-943">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="04529-944">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="04529-944">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="04529-945">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="04529-945">Az.Websites</span></span>
* <span data-ttu-id="04529-946">Исправлены командлеты Set-AzWebApp и Set-AzWebAppSlot, которые теперь не удаляют теги при выполнении.</span><span class="sxs-lookup"><span data-stu-id="04529-946">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="04529-947">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="04529-947">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="04529-948">Обновлен пакет SDK веб-узлов.</span><span class="sxs-lookup"><span data-stu-id="04529-948">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="04529-949">Удалено свойство AdminSiteName из PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="04529-949">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="04529-950">1.7.0 —апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="04529-950">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="04529-951">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="04529-951">Highlights since the last major release</span></span>
* <span data-ttu-id="04529-952">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="04529-952">General availability of `Az` module</span></span>
* <span data-ttu-id="04529-953">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="04529-953">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="04529-954">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="04529-954">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="04529-955">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="04529-955">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="04529-956">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="04529-956">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="04529-957">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="04529-957">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="04529-958">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="04529-958">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="04529-959">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="04529-959">Az.Accounts</span></span>
* <span data-ttu-id="04529-960">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметр AzureAnalysisServicesEndpointResourceId.</span><span class="sxs-lookup"><span data-stu-id="04529-960">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="04529-961">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="04529-961">Az.AnalysisServices</span></span>
* <span data-ttu-id="04529-962">Использование ServiceClient в командлетах плоскости данных и удаление исходной логики проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="04529-962">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="04529-963">Add-AzureASAccount используется как оболочка для Connect-AzAccount во избежание критических изменений.</span><span class="sxs-lookup"><span data-stu-id="04529-963">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="04529-964">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="04529-964">Az.Automation</span></span>
* <span data-ttu-id="04529-965">Исправлена ошибка командлета New-AzAutomationSoftwareUpdateConfiguration, связанная с включением.</span><span class="sxs-lookup"><span data-stu-id="04529-965">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="04529-966">Теперь параметры IncludedKbNumber и IncludedPackageNameMask должны работать нормально.</span><span class="sxs-lookup"><span data-stu-id="04529-966">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="04529-967">Исправлена ошибка динамической группы управления обновлениями службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="04529-967">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="04529-968">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="04529-968">Az.Compute</span></span>
* <span data-ttu-id="04529-969">В командлеты New-AzDiskConfig и New-AzSnapshotConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="04529-969">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="04529-970">Теперь можно создавать виртуальные машину на основе образов из коллекции от других клиентов.</span><span class="sxs-lookup"><span data-stu-id="04529-970">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="04529-971">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="04529-971">Az.ContainerInstance</span></span>
* <span data-ttu-id="04529-972">Исправлена проблема в параметре -Command командлета New-AzContainerGroup, из-за которой в конце добавлялся пустой аргумент.</span><span class="sxs-lookup"><span data-stu-id="04529-972">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="04529-973">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="04529-973">Az.DataFactory</span></span>
* <span data-ttu-id="04529-974">Пакет SDK для ADF .NET обновлен до версии 3.0.2.</span><span class="sxs-lookup"><span data-stu-id="04529-974">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="04529-975">Командлет Set-AzDataFactoryV2 обновлен с помощью дополнительных параметров для настроек, связанных с RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="04529-975">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="04529-976">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="04529-976">Az.Resources</span></span>
* <span data-ttu-id="04529-977">Улучшена обработка поставщиков Get-AzResource при предоставлении параметров -ResourceId или -ResourceGroupName, -Name и -ResourceType.</span><span class="sxs-lookup"><span data-stu-id="04529-977">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="04529-978">Улучшена обработка ошибок в командлетах Test-AzDeployment и Test-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="04529-978">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="04529-979">Теперь ошибки, возникающие за пределами проверки развертывания, обрабатываются и включаются в выходные данные команды.</span><span class="sxs-lookup"><span data-stu-id="04529-979">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="04529-980">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="04529-980">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="04529-981">Добавлен параметр-переключатель -IgnoreDynamicParameters, с помощью которого можно настроить командлеты развертывания так, чтобы они пропускали запросы в сценариях скриптов и заданий.</span><span class="sxs-lookup"><span data-stu-id="04529-981">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="04529-982">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="04529-982">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="04529-983">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="04529-983">Az.Sql</span></span>
* <span data-ttu-id="04529-984">Поддержка классификации данных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="04529-984">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="04529-985">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="04529-985">Az.Storage</span></span>
* <span data-ttu-id="04529-986">Подробные сообщения об ошибке передаются при создании контекста хранилища с помощью параметра -UseConnectedAccount, но без входа в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="04529-986">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="04529-987">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="04529-987">New-AzStorageContext</span></span>
* <span data-ttu-id="04529-988">Поддержка свойств службы управления BLOB-объектов в указанной учетной записи хранения с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="04529-988">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="04529-989">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="04529-989">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="04529-990">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="04529-990">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="04529-991">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="04529-991">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="04529-992">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="04529-992">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="04529-993">Поддержка параметра -AsJob в командлетах для отправки и скачивания больших двоичных объектов и файлов.</span><span class="sxs-lookup"><span data-stu-id="04529-993">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="04529-994">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="04529-994">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="04529-995">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="04529-995">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="04529-996">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="04529-996">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="04529-997">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="04529-997">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="04529-998">1.6.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="04529-998">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="04529-999">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="04529-999">Highlights since the last major release</span></span>
* <span data-ttu-id="04529-1000">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="04529-1000">General availability of `Az` module</span></span>
* <span data-ttu-id="04529-1001">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="04529-1001">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="04529-1002">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="04529-1002">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="04529-1003">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="04529-1003">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="04529-1004">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="04529-1004">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="04529-1005">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="04529-1005">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="04529-1006">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="04529-1006">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="04529-1007">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="04529-1007">Az.Automation</span></span>
* <span data-ttu-id="04529-1008">В управление обновлениями службы автоматизации Azure внесены изменения для поддержки следующих новых функций:</span><span class="sxs-lookup"><span data-stu-id="04529-1008">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="04529-1009">динамическое группирование;</span><span class="sxs-lookup"><span data-stu-id="04529-1009">Dynamic grouping</span></span>
    * <span data-ttu-id="04529-1010">скрипты предварительного или последующего выполнения;</span><span class="sxs-lookup"><span data-stu-id="04529-1010">Pre-Post script</span></span>
    * <span data-ttu-id="04529-1011">параметр перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="04529-1011">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="04529-1012">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="04529-1012">Az.Compute</span></span>
* <span data-ttu-id="04529-1013">Устранена проблема, связанная с разрешением пути в Get-AzVmBootDiagnosticsData.</span><span class="sxs-lookup"><span data-stu-id="04529-1013">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="04529-1014">Обновление клиентской библиотеки вычислений до версии 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="04529-1014">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="04529-1015">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="04529-1015">Az.KeyVault</span></span>
* <span data-ttu-id="04529-1016">Добавлена поддержка подстановочных знаков в командлетах KeyVault.</span><span class="sxs-lookup"><span data-stu-id="04529-1016">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="04529-1017">Az.Network</span><span class="sxs-lookup"><span data-stu-id="04529-1017">Az.Network</span></span>
* <span data-ttu-id="04529-1018">Добавлена поддержка анализа угроз для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="04529-1018">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="04529-1019">Добавлены настраиваемые правила и ресурс верхнего уровня для политики брандмауэра Шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="04529-1019">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="04529-1020">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="04529-1020">Az.RecoveryServices</span></span>
* <span data-ttu-id="04529-1021">В политику виртуальной машины Azure добавлен объект SnapshotRetentionInDays для поддержки мгновенного восстановления.</span><span class="sxs-lookup"><span data-stu-id="04529-1021">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="04529-1022">Добавлена поддержка канала для отмены регистрации контейнера.</span><span class="sxs-lookup"><span data-stu-id="04529-1022">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="04529-1023">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="04529-1023">Az.Resources</span></span>
* <span data-ttu-id="04529-1024">Обновлена поддержка подстановочных знаков для Get-AzResource и Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="04529-1024">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="04529-1025">Обновлены учетные данные, используемые при общих вызовах к ARM.</span><span class="sxs-lookup"><span data-stu-id="04529-1025">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="04529-1026">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="04529-1026">Az.Sql</span></span>
* <span data-ttu-id="04529-1027">Изменен тип параметра (ExcludeDetectionType) командлетов для обнаружения угроз с DetectionTypes на string[] для поддержки актуального состояния при добавлении новых типов обнаружения и для поддержки автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="04529-1027">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="04529-1028">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="04529-1028">Az.Storage</span></span>
* <span data-ttu-id="04529-1029">Поддержка получения, настройки и удаления политики управления в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="04529-1029">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="04529-1030">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="04529-1030">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="04529-1031">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="04529-1031">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="04529-1032">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="04529-1032">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="04529-1033">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="04529-1033">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="04529-1034">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="04529-1034">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="04529-1035">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="04529-1035">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="04529-1036">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="04529-1036">Az.Websites</span></span>
* <span data-ttu-id="04529-1037">Исправлена ошибка с шаблоном ARM, из-за которой прерывалось клонирование все слотов при использовании New-AzWebApp -IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="04529-1037">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="04529-1038">1.5.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="04529-1038">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="04529-1039">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="04529-1039">Az.Accounts</span></span>
* <span data-ttu-id="04529-1040">Добавлена команда Register-AzModule для поддержки созданных командлетов AutoRest.</span><span class="sxs-lookup"><span data-stu-id="04529-1040">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="04529-1041">Обновлены примеры для Connect AzAccount.</span><span class="sxs-lookup"><span data-stu-id="04529-1041">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="04529-1042">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="04529-1042">Az.Automation</span></span>
* <span data-ttu-id="04529-1043">Исправлена проблема с получением некоторых ежемесячных расписаний в нескольких командлетах службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="04529-1043">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="04529-1044">Исправлен командлет Get-AzAutomationDscNode, возвращающий только первые 20 узлов.</span><span class="sxs-lookup"><span data-stu-id="04529-1044">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="04529-1045">Теперь он возвращает все узлы.</span><span class="sxs-lookup"><span data-stu-id="04529-1045">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="04529-1046">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="04529-1046">Az.Cdn</span></span>
* <span data-ttu-id="04529-1047">Добавлены новые командлеты PowerShell для включения и отключения HTTPS для личного домена и отключены устаревшие командлеты.</span><span class="sxs-lookup"><span data-stu-id="04529-1047">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="04529-1048">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="04529-1048">Az.Compute</span></span>
* <span data-ttu-id="04529-1049">Добавлена поддержка подстановочных знаков в командлетах Get.</span><span class="sxs-lookup"><span data-stu-id="04529-1049">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="04529-1050">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="04529-1050">Az.DataFactory</span></span>
* <span data-ttu-id="04529-1051">Обновлен пакет SDK для ADF .NET до версии 3.0.1.</span><span class="sxs-lookup"><span data-stu-id="04529-1051">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="04529-1052">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="04529-1052">Az.LogicApp</span></span>
* <span data-ttu-id="04529-1053">Исправлена проблема с получением только первой страницы результатов при выполнении команды ListWorkflows.</span><span class="sxs-lookup"><span data-stu-id="04529-1053">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="04529-1054">Az.Network</span><span class="sxs-lookup"><span data-stu-id="04529-1054">Az.Network</span></span>
* <span data-ttu-id="04529-1055">Добавлена поддержка подстановочных знаков в командлетах Network.</span><span class="sxs-lookup"><span data-stu-id="04529-1055">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="04529-1056">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="04529-1056">Az.RecoveryServices</span></span>
* <span data-ttu-id="04529-1057">Добавлена поддержка SQL Server на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="04529-1057">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="04529-1058">Обновление пакета SDK</span><span class="sxs-lookup"><span data-stu-id="04529-1058">SDK Update</span></span>
* <span data-ttu-id="04529-1059">Удалена проверка VMappContainer в Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="04529-1059">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="04529-1060">Добавлены параметры Name и ServerName для Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="04529-1060">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="04529-1061">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="04529-1061">Az.Resources</span></span>
* <span data-ttu-id="04529-1062">Добавлен параметр `-TemplateObject` в командлеты для развертывания.</span><span class="sxs-lookup"><span data-stu-id="04529-1062">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="04529-1063">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2933.</span><span class="sxs-lookup"><span data-stu-id="04529-1063">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="04529-1064">Устранена проблема с передачей в конвейер результата `Get-AzResource` для `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="04529-1064">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="04529-1065">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8240.</span><span class="sxs-lookup"><span data-stu-id="04529-1065">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="04529-1066">Устранена проблема с изменением типа данных JSON при выполнении `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="04529-1066">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="04529-1067">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7930.</span><span class="sxs-lookup"><span data-stu-id="04529-1067">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="04529-1068">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="04529-1068">Az.Sql</span></span>
* <span data-ttu-id="04529-1069">Обновление AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="04529-1069">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="04529-1070">Исправлено поведение для пограничного случая при создании параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="04529-1070">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="04529-1071">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="04529-1071">Az.Storage</span></span>
* <span data-ttu-id="04529-1072">Включена поддержка Kind BlockBlobStorage при создании учетной записи хранения для New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="04529-1072">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="04529-1073">1.4.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="04529-1073">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="04529-1074">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="04529-1074">Az.AnalysisServices</span></span>
* <span data-ttu-id="04529-1075">Командлет AddAzureASAccount устарел.</span><span class="sxs-lookup"><span data-stu-id="04529-1075">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="04529-1076">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="04529-1076">Az.Automation</span></span>
* <span data-ttu-id="04529-1077">Обновлена справка для командлета Import-AzAutomationDscNodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="04529-1077">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="04529-1078">Добавлена проверка имени конфигурации для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="04529-1078">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="04529-1079">Улучшена обработка ошибок для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="04529-1079">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="04529-1080">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="04529-1080">Az.CognitiveServices</span></span>
* <span data-ttu-id="04529-1081">Добавлен параметр CustomSubdomainName — новый необязательный параметр для командлета New-AzCognitiveServicesAccount, который указывает поддомен для ресурса.</span><span class="sxs-lookup"><span data-stu-id="04529-1081">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="04529-1082">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="04529-1082">Az.Compute</span></span>
* <span data-ttu-id="04529-1083">Устранена проблема с идентификаторами наборов параметров.</span><span class="sxs-lookup"><span data-stu-id="04529-1083">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="04529-1084">Обновлен командлет Get-AzVMExtension для отображения списка всех установленных расширений, если не указан параметр Name.</span><span class="sxs-lookup"><span data-stu-id="04529-1084">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="04529-1085">Для командлета Update-AzImage добавлены параметры Tag и ResourceId.</span><span class="sxs-lookup"><span data-stu-id="04529-1085">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="04529-1086">Командлет Get-AzVmssVM, который выполняется без указания идентификатора экземпляра и с параметром InstanceView, может выводить виртуальные машины из VMSS с представлением экземпляра.</span><span class="sxs-lookup"><span data-stu-id="04529-1086">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="04529-1087">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="04529-1087">Az.DataLakeStore</span></span>
* <span data-ttu-id="04529-1088">Добавлены командлеты для перечисления и восстановления удаленного элемента ADL.</span><span class="sxs-lookup"><span data-stu-id="04529-1088">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="04529-1089">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="04529-1089">Az.EventHub</span></span>
* <span data-ttu-id="04529-1090">Добавлено новое логическое свойство SkipEmptyArchives для пропуска пустых архивов в классе CaptureDescription Eventhub.</span><span class="sxs-lookup"><span data-stu-id="04529-1090">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="04529-1091">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="04529-1091">Az.KeyVault</span></span>
* <span data-ttu-id="04529-1092">Исправлена расстановка тегов для командлета Set-AzKeyVaultSecret.</span><span class="sxs-lookup"><span data-stu-id="04529-1092">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="04529-1093">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="04529-1093">Az.LogicApp</span></span>
* <span data-ttu-id="04529-1094">Добавлен SKU "Базовый" для учетных записей интеграции.</span><span class="sxs-lookup"><span data-stu-id="04529-1094">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="04529-1095">Добавлены типы сопоставлений Liquid, а также XSLT 2.0 и XSLT 3.0.</span><span class="sxs-lookup"><span data-stu-id="04529-1095">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="04529-1096">Новые командлеты для сборок учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="04529-1096">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="04529-1097">Get-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="04529-1097">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="04529-1098">New-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="04529-1098">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="04529-1099">Remove-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="04529-1099">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="04529-1100">Set-AzIntegrationAccountAssembly.</span><span class="sxs-lookup"><span data-stu-id="04529-1100">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="04529-1101">Новые командлеты для конфигурации пакета учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="04529-1101">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="04529-1102">Get-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="04529-1102">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="04529-1103">New-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="04529-1103">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="04529-1104">Remove-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="04529-1104">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="04529-1105">Set-AzIntegrationAccountBatchConfiguration.</span><span class="sxs-lookup"><span data-stu-id="04529-1105">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="04529-1106">Обновлен пакет SDK Logic Apps до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="04529-1106">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="04529-1107">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="04529-1107">Az.Monitor</span></span>
* <span data-ttu-id="04529-1108">Обновлена справка для командлета Get-AzMetric.</span><span class="sxs-lookup"><span data-stu-id="04529-1108">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="04529-1109">Az.Network</span><span class="sxs-lookup"><span data-stu-id="04529-1109">Az.Network</span></span>
* <span data-ttu-id="04529-1110">Обновлен пример справки для командлета Add-AzApplicationGatewayCustomError.</span><span class="sxs-lookup"><span data-stu-id="04529-1110">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="04529-1111">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="04529-1111">Az.OperationalInsights</span></span>
* <span data-ttu-id="04529-1112">Дополнительная поддержка создания и получения источников данных ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="04529-1112">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="04529-1113">Добавлен новый тип ApplicationInsights для получения определенных или всех источников данных ApplicationInsights для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="04529-1113">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="04529-1114">Добавлен командлет New-AzOperationalInsightsApplicationInsightsDataSource для создания источника данных с использованием параметров указанного ресурса Application-Insightss: subscription Id, resourceGroupName и name.</span><span class="sxs-lookup"><span data-stu-id="04529-1114">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="04529-1115">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="04529-1115">Az.Resources</span></span>
* <span data-ttu-id="04529-1116">исправлена проблема https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="04529-1116">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="04529-1117">исправлена проблема https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="04529-1117">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="04529-1118">исправлена проблема https://github.com/Azure/azure-powershell/issues/6219.</span><span class="sxs-lookup"><span data-stu-id="04529-1118">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="04529-1119">Исправлена ошибка, препятствующая повторному созданию KeyCredentials.</span><span class="sxs-lookup"><span data-stu-id="04529-1119">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="04529-1120">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="04529-1120">Az.Sql</span></span>
* <span data-ttu-id="04529-1121">Добавлена поддержка уровня гипермасштабирования в базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="04529-1121">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="04529-1122">Исправлена ошибка, из-за которой восстановление могло завершиться со сбоем при указании ненужных свойств в запросе на восстановление.</span><span class="sxs-lookup"><span data-stu-id="04529-1122">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="04529-1123">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="04529-1123">Az.Websites</span></span>
* <span data-ttu-id="04529-1124">Исправлен пример для командлета Get-AzWebAppSlotMetrics.</span><span class="sxs-lookup"><span data-stu-id="04529-1124">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="04529-1125">1.3.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="04529-1125">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="04529-1126">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="04529-1126">Az.Accounts</span></span>
* <span data-ttu-id="04529-1127">Обновление до последней версии ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="04529-1127">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="04529-1128">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="04529-1128">Az.AnalysisServices</span></span>
<span data-ttu-id="04529-1129">Общедоступная версия модуля Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="04529-1129">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="04529-1130">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="04529-1130">Az.Compute</span></span>
* <span data-ttu-id="04529-1131">Расширение AEM: добавлена поддержка дисков UltraSSD, P60, P70 и P80.</span><span class="sxs-lookup"><span data-stu-id="04529-1131">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="04529-1132">Обновлено описание справки для командлета Set-AzVMBootDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="04529-1132">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="04529-1133">Обновлено описание справки и пример для командлета Update-AzImage.</span><span class="sxs-lookup"><span data-stu-id="04529-1133">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="04529-1134">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="04529-1134">Az.RecoveryServices</span></span>
<span data-ttu-id="04529-1135">Общедоступная версия модуля Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="04529-1135">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="04529-1136">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="04529-1136">Az.Resources</span></span>
* <span data-ttu-id="04529-1137">Исправлена расстановка тегов для групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="04529-1137">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="04529-1138">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="04529-1138">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="04529-1139">Исправлена проблема с игнорированием командлетом `Get-AzureRmRoleAssignment` параметра -ErrorAction.</span><span class="sxs-lookup"><span data-stu-id="04529-1139">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="04529-1140">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="04529-1140">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="04529-1141">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="04529-1141">Az.Sql</span></span>
* <span data-ttu-id="04529-1142">Добавлен командлет Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="04529-1142">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="04529-1143">Исправлена проблема с появлением исключения NullRef при выполнении командлетов SQL, если не выполнен вход в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="04529-1143">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="04529-1144">Исправлено исключение NullRef в командлете Get-AzSqlCapability.</span><span class="sxs-lookup"><span data-stu-id="04529-1144">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="04529-1145">1.2.1 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="04529-1145">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="04529-1146">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="04529-1146">Az.Accounts</span></span>
* <span data-ttu-id="04529-1147">Выпуск с правильной версией службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="04529-1147">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="04529-1148">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="04529-1148">Az.AnalysisServices</span></span>
* <span data-ttu-id="04529-1149">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="04529-1149">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="04529-1150">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="04529-1150">Az.RecoveryServices</span></span>
* <span data-ttu-id="04529-1151">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="04529-1151">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="04529-1152">1.2.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="04529-1152">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="04529-1153">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="04529-1153">Az.Accounts</span></span>
* <span data-ttu-id="04529-1154">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="04529-1154">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="04529-1155">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="04529-1155">Update incorrect online help URLs</span></span>
* <span data-ttu-id="04529-1156">Добавлено предупреждающее сообщение в PS Core для модуля Uninstall-AzureRm.</span><span class="sxs-lookup"><span data-stu-id="04529-1156">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="04529-1157">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="04529-1157">Az.Aks</span></span>
* <span data-ttu-id="04529-1158">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="04529-1158">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="04529-1159">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="04529-1159">Az.Automation</span></span>
* <span data-ttu-id="04529-1160">Добавлена поддержка для модулей runbook Python 2.</span><span class="sxs-lookup"><span data-stu-id="04529-1160">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="04529-1161">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="04529-1161">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="04529-1162">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="04529-1162">Az.Cdn</span></span>
* <span data-ttu-id="04529-1163">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="04529-1163">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="04529-1164">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="04529-1164">Az.Compute</span></span>
* <span data-ttu-id="04529-1165">Добавлен командлет Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="04529-1165">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="04529-1166">Добавлен параметр TempDisk к командлету Set-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="04529-1166">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="04529-1167">Исправлено предупреждающее сообщение командлета New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="04529-1167">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="04529-1168">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="04529-1168">Az.ContainerRegistry</span></span>
* <span data-ttu-id="04529-1169">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="04529-1169">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="04529-1170">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="04529-1170">Az.DataFactory</span></span>
* <span data-ttu-id="04529-1171">Пакет SDK ADF .Net обновлен до версии 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="04529-1171">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="04529-1172">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="04529-1172">Az.DataLakeStore</span></span>
* <span data-ttu-id="04529-1173">Исправлена проблема с конечной точкой ADLS при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="04529-1173">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="04529-1174">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7462.</span><span class="sxs-lookup"><span data-stu-id="04529-1174">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="04529-1175">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="04529-1175">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="04529-1176">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="04529-1176">Az.IotHub</span></span>
* <span data-ttu-id="04529-1177">Добавлен формат кодирования для командлета Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="04529-1177">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="04529-1178">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="04529-1178">Az.KeyVault</span></span>
* <span data-ttu-id="04529-1179">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="04529-1179">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="04529-1180">Az.Network</span><span class="sxs-lookup"><span data-stu-id="04529-1180">Az.Network</span></span>
* <span data-ttu-id="04529-1181">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="04529-1181">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="04529-1182">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="04529-1182">Az.Resources</span></span>
* <span data-ttu-id="04529-1183">Исправлены неправильные примеры в справочной документации по командлетам New-AzADAppCredential и New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="04529-1183">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="04529-1184">Исправлена проблема, при которой путь для параметра -TemplateFile не удавалось разрешить до выполнения командлетов развертывания групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="04529-1184">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="04529-1185">Az.Resources: исправлена документация для значения по умолчанию -Mode командлета New-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="04529-1185">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="04529-1186">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/7522.</span><span class="sxs-lookup"><span data-stu-id="04529-1186">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="04529-1187">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/5747.</span><span class="sxs-lookup"><span data-stu-id="04529-1187">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="04529-1188">Исправлена проблема с форматированием объекта PSResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="04529-1188">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="04529-1189">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2123.</span><span class="sxs-lookup"><span data-stu-id="04529-1189">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="04529-1190">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="04529-1190">Az.ServiceFabric</span></span>
* <span data-ttu-id="04529-1191">Исправлена проблема с появлением исключения в процессе отката при добавлении сертификата к модели VMSS: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="04529-1191">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="04529-1192">Исправлены некоторые сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="04529-1192">Fix some error messages.</span></span>
* <span data-ttu-id="04529-1193">Исправлена проблема с созданием кластера с шаблоном ARM по умолчанию для командлета New-AzServiceFabriCluster, который не работал с операцией миграции в Az.</span><span class="sxs-lookup"><span data-stu-id="04529-1193">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="04529-1194">Исправлена проблема с добавлением сертификата кластера или приложения: теперь они добавляются только в Масштабируемые наборы виртуальных машин, которые сопоставлены с кластером, путем проверки идентификатора кластера в расширении.</span><span class="sxs-lookup"><span data-stu-id="04529-1194">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="04529-1195">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="04529-1195">Az.SignalR</span></span>
* <span data-ttu-id="04529-1196">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="04529-1196">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="04529-1197">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="04529-1197">Az.Sql</span></span>
* <span data-ttu-id="04529-1198">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="04529-1198">Update incorrect online help URLs</span></span>
* <span data-ttu-id="04529-1199">Обновлено описание параметра LicenseType с добавлением возможных значений.</span><span class="sxs-lookup"><span data-stu-id="04529-1199">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="04529-1200">Исправлена проблема с неправильным обновлением удостоверения управляемого экземпляра, если оно было единственным обновляемым свойством.</span><span class="sxs-lookup"><span data-stu-id="04529-1200">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="04529-1201">Поддержка пользовательских параметров сортировки в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="04529-1201">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="04529-1202">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="04529-1202">Az.Storage</span></span>
* <span data-ttu-id="04529-1203">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="04529-1203">Update incorrect online help URLs</span></span>
* <span data-ttu-id="04529-1204">Добавлен вывод подробных сообщений об ошибке при получении или установке классических свойств ведения журнала или метрик в учетной записи хранилища класса Premium, так как учетная запись хранилища класса Premium не поддерживает классические функции ведения журнала и метрик.</span><span class="sxs-lookup"><span data-stu-id="04529-1204">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="04529-1205">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="04529-1205">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="04529-1206">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="04529-1206">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="04529-1207">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="04529-1207">Az.TrafficManager</span></span>
* <span data-ttu-id="04529-1208">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="04529-1208">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="04529-1209">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="04529-1209">Az.Websites</span></span>
* <span data-ttu-id="04529-1210">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="04529-1210">Update incorrect online help URLs</span></span>
* <span data-ttu-id="04529-1211">Исправлена работа командлета New-AzWebAppSSLBinding: сертификат отправляется в правильную группу ресурсов и правильное расположение, если приложение размещено в ASE.</span><span class="sxs-lookup"><span data-stu-id="04529-1211">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="04529-1212">Исправлена работа командлета New-AzWebAppSSLBinding: теги не перезаписываются при привязке SSL-сертификата к приложению.</span><span class="sxs-lookup"><span data-stu-id="04529-1212">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="04529-1213">1.1.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="04529-1213">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="04529-1214">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="04529-1214">Az.Accounts</span></span>
* <span data-ttu-id="04529-1215">Добавление области "Local" в Enable-AzureRmAlias.</span><span class="sxs-lookup"><span data-stu-id="04529-1215">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="04529-1216">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="04529-1216">Az.Compute</span></span>
* <span data-ttu-id="04529-1217">Теперь имя не является обязательным в идентификаторе набора параметров для Restart/Start/Stop/Remove/Set-AzVM и Save-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="04529-1217">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="04529-1218">Обновлено описание идентификатора в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="04529-1218">Updated the description of ID in help files</span></span>
* <span data-ttu-id="04529-1219">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="04529-1219">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="04529-1220">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="04529-1220">Az.DataLakeStore</span></span>
* <span data-ttu-id="04529-1221">Обновление версии пакета SDK для плоскости данных до 1.1.14 для устранения найденных проблем.</span><span class="sxs-lookup"><span data-stu-id="04529-1221">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="04529-1222">Исправлена обработка отрицательного времени доступа и времени изменения для getfilestatus и liststatus, исправлен токен отмены для асинхронных методов.</span><span class="sxs-lookup"><span data-stu-id="04529-1222">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="04529-1223">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="04529-1223">Az.EventGrid</span></span>
* <span data-ttu-id="04529-1224">Обновление для использования API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="04529-1224">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="04529-1225">Обновлены указанные ниже командлеты для поддержки нового сценария в API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="04529-1225">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="04529-1226">New-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="04529-1226">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="04529-1227">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="04529-1227">Event Time-To-Live,</span></span>
        - <span data-ttu-id="04529-1228">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="04529-1228">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="04529-1229">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="04529-1229">Dead letter endpoint.</span></span>
    - <span data-ttu-id="04529-1230">Update-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="04529-1230">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="04529-1231">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="04529-1231">Event Time-To-Live,</span></span>
        - <span data-ttu-id="04529-1232">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="04529-1232">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="04529-1233">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="04529-1233">Dead letter endpoint.</span></span>
* <span data-ttu-id="04529-1234">Для параметра EndpointType добавлены новые значения перечисления (storageQueue и hybridConnection) в командлеты New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="04529-1234">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="04529-1235">Если ожидается, что создание или обновление подписки на событие повлечет за собой действия со стороны пользователя, выполняемые вручную, отображается предупреждение при создании или обновлении подписки события.</span><span class="sxs-lookup"><span data-stu-id="04529-1235">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="04529-1236">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="04529-1236">Az.IotHub</span></span>
* <span data-ttu-id="04529-1237">Пакет SDK Центра Интернета вещей обновлен до последней версии.</span><span class="sxs-lookup"><span data-stu-id="04529-1237">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="04529-1238">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="04529-1238">Az.LogicApp</span></span>
* <span data-ttu-id="04529-1239">Get-AzLogicApp позволяет перечислить все параметры без указанного имени.</span><span class="sxs-lookup"><span data-stu-id="04529-1239">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="04529-1240">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="04529-1240">Az.Resources</span></span>
* <span data-ttu-id="04529-1241">Исправлена проблема с набором параметров при предоставлении параметров "-ODataQuery" и "-ResourceId" для "Get-AzResource".</span><span class="sxs-lookup"><span data-stu-id="04529-1241">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="04529-1242">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7875.</span><span class="sxs-lookup"><span data-stu-id="04529-1242">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="04529-1243">Исправлена обработка параметра -Custom в New/Set-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="04529-1243">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="04529-1244">Исправлена опечатка в документации по New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="04529-1244">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="04529-1245">Параметр "-MailNickname" стал обязательным для "New-AzADUser".</span><span class="sxs-lookup"><span data-stu-id="04529-1245">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="04529-1246">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8220.</span><span class="sxs-lookup"><span data-stu-id="04529-1246">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="04529-1247">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="04529-1247">Az.SignalR</span></span>
* <span data-ttu-id="04529-1248">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="04529-1248">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="04529-1249">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="04529-1249">Az.Sql</span></span>
* <span data-ttu-id="04529-1250">Зависимость клиента управления хранением преобразована для общей реализации в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="04529-1250">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="04529-1251">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="04529-1251">Az.Storage</span></span>
* <span data-ttu-id="04529-1252">Установка параметра StorageAccountName для контекста хранилища в качестве реального имени учетной записи хранения, если она была создана с использованием токена Sas, OAuth или анонимного доступа.</span><span class="sxs-lookup"><span data-stu-id="04529-1252">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="04529-1253">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="04529-1253">New-AzStorageContext</span></span>
* <span data-ttu-id="04529-1254">Создание токена Sas большого двоичного объекта моментального снимка с параметром "-FullUri". Возвращаемый URI исправлен на URI моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="04529-1254">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="04529-1255">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="04529-1255">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="04529-1256">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="04529-1256">Az.Websites</span></span>
* <span data-ttu-id="04529-1257">Исправлена ошибка синтаксического анализа даты в "Get-AzDeletedWebApp".</span><span class="sxs-lookup"><span data-stu-id="04529-1257">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="04529-1258">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="04529-1258">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="04529-1259">1.0.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="04529-1259">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="04529-1260">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="04529-1260">General</span></span>

- <span data-ttu-id="04529-1261">Общедоступная версия модуля Az.</span><span class="sxs-lookup"><span data-stu-id="04529-1261">General Availability of Az Module</span></span>
- <span data-ttu-id="04529-1262">Справка в Интернете для каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="04529-1262">Online help for each module</span></span>
- <span data-ttu-id="04529-1263">Дополнительные сведения и стратегию развития см. в статье [Announcing New Module 'Az'](https://aka.ms/azps-announce) (Объявление о новом модуле Az)</span><span class="sxs-lookup"><span data-stu-id="04529-1263">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="04529-1264">Сведения о миграции с AzureRM см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="04529-1264">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="04529-1265">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="04529-1265">Az.Accounts</span></span>
- <span data-ttu-id="04529-1266">Изменено с Az.Profile.</span><span class="sxs-lookup"><span data-stu-id="04529-1266">Changed from Az.Profile</span></span>
- <span data-ttu-id="04529-1267">Исправлены форматы таблиц для типов профиля и контекста.</span><span class="sxs-lookup"><span data-stu-id="04529-1267">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="04529-1268">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="04529-1268">Az.ApiManagement</span></span>
- <span data-ttu-id="04529-1269">Исправления для #7002.</span><span class="sxs-lookup"><span data-stu-id="04529-1269">Fixes for #7002</span></span>
- <span data-ttu-id="04529-1270">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="04529-1270">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="04529-1271">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="04529-1271">Az.Batch</span></span>
- <span data-ttu-id="04529-1272">Добавлена возможность видеть, какая версия агента узла пакетной службы Azure работает в пуле на каждой виртуальной машине, с помощью нового свойства `NodeAgentInformation` в `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="04529-1272">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="04529-1273">Значение `Caching` по умолчанию для `PSDataDisk` теперь `ReadWrite` вместо `None`.</span><span class="sxs-lookup"><span data-stu-id="04529-1273">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="04529-1274">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="04529-1274">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="04529-1275">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="04529-1275">Az.Billing</span></span>
- <span data-ttu-id="04529-1276">Объединены командлеты Billing, Consumption и UsageAggregates. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0).</span><span class="sxs-lookup"><span data-stu-id="04529-1276">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="04529-1277">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="04529-1277">Az.CognitivServices</span></span>
- <span data-ttu-id="04529-1278">Добавлены средства заполнения для SkuName и Typem, доступные в операции New-AzureRmCognitiveServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="04529-1278">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="04529-1279">Удален набор параметров GetSkusWithAccountParamSetName из Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="04529-1279">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="04529-1280">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="04529-1280">Az.ContainerInstance</span></span>
- <span data-ttu-id="04529-1281">Добавлена поддержка ManagedIdentity.</span><span class="sxs-lookup"><span data-stu-id="04529-1281">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="04529-1282">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="04529-1282">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="04529-1283">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="04529-1283">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="04529-1284">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="04529-1284">Az.DataLakeStore</span></span>
- <span data-ttu-id="04529-1285">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="04529-1285">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="04529-1286">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="04529-1286">Az.Monitor</span></span>
- <span data-ttu-id="04529-1287">"Az.Insights" переименован в "Az.Monitor" и внесены другие незначительные критические изменения. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="04529-1287">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="04529-1288">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="04529-1288">Az.KeyVault</span></span>
- <span data-ttu-id="04529-1289">Из типов вывода удалено устаревшее свойство PurgeDisabled</span><span class="sxs-lookup"><span data-stu-id="04529-1289">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="04529-1290">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="04529-1290">Az.MachineLearning</span></span>
- <span data-ttu-id="04529-1291">Включены командлеты из модуля Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="04529-1291">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="04529-1292">Az.Media</span><span class="sxs-lookup"><span data-stu-id="04529-1292">Az.Media</span></span>
- <span data-ttu-id="04529-1293">Удаляет устаревший псевдоним Tags из New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="04529-1293">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="04529-1294">Az.Network</span><span class="sxs-lookup"><span data-stu-id="04529-1294">Az.Network</span></span>
<span data-ttu-id="04529-1295">В шлюз приложений добавлена поддержка настройки RewriteRuleSets</span><span class="sxs-lookup"><span data-stu-id="04529-1295">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="04529-1296">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="04529-1296">New cmdlets added:</span></span>
        - <span data-ttu-id="04529-1297">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="04529-1297">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="04529-1298">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="04529-1298">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="04529-1299">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="04529-1299">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="04529-1300">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="04529-1300">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="04529-1301">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="04529-1301">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="04529-1302">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="04529-1302">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="04529-1303">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="04529-1303">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="04529-1304">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="04529-1304">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="04529-1305">В следующие командлеты добавлен необязательный параметр -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="04529-1305">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="04529-1306">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="04529-1306">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="04529-1307">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="04529-1307">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="04529-1308">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="04529-1308">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="04529-1309">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="04529-1309">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="04529-1310">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="04529-1310">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="04529-1311">New-AzureRmApplicationGatewayUrlPathMapConfig добавил с помощью идентификатора поддержку KeyVault для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="04529-1311">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="04529-1312">В следующие командлеты добавлен необязательный параметр -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="04529-1312">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="04529-1313">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="04529-1313">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="04529-1314">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="04529-1314">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="04529-1315">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="04529-1315">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="04529-1316">В командлет New-AzApplicationGateway добавлен необязательный параметр -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="04529-1316">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="04529-1317">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="04529-1317">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="04529-1318">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="04529-1318">Az.OperationalInsights</span></span>
- <span data-ttu-id="04529-1319">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="04529-1319">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="04529-1320">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="04529-1320">Az.Profile</span></span>
- <span data-ttu-id="04529-1321">Имя модуля изменено на Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="04529-1321">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="04529-1322">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="04529-1322">Az.RecoveryServices</span></span>
- <span data-ttu-id="04529-1323">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="04529-1323">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="04529-1324">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="04529-1324">Az.Resources</span></span>
- <span data-ttu-id="04529-1325">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="04529-1325">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="04529-1326">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="04529-1326">Az.ServiceFabric</span></span>
- <span data-ttu-id="04529-1327">Поддержка спецификации сертификата по общему имени и отпечатку</span><span class="sxs-lookup"><span data-stu-id="04529-1327">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="04529-1328">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="04529-1328">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="04529-1329">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="04529-1329">Az.SIgnalR</span></span>
- <span data-ttu-id="04529-1330">Общедоступная версия командлетов PowerShell для SIgnalR</span><span class="sxs-lookup"><span data-stu-id="04529-1330">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="04529-1331">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="04529-1331">Az.Sql</span></span>
- <span data-ttu-id="04529-1332">Добавлены новые типы обнаружения Data_Exfiltration и Unsafe_Action в командлеты обнаружения угроз</span><span class="sxs-lookup"><span data-stu-id="04529-1332">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="04529-1333">Примеры обновленной документации для командлетов аудита Sql</span><span class="sxs-lookup"><span data-stu-id="04529-1333">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="04529-1334">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="04529-1334">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="04529-1335">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="04529-1335">Az.Storage</span></span>
- <span data-ttu-id="04529-1336">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="04529-1336">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="04529-1337">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="04529-1337">Az.Websites</span></span>
- <span data-ttu-id="04529-1338">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="04529-1338">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="04529-1339">0.7.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="04529-1339">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="04529-1340">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="04529-1340">General</span></span>

* <span data-ttu-id="04529-1341">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="04529-1341">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="04529-1342">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="04529-1342">Az.Compute</span></span>

* <span data-ttu-id="04529-1343">Добавлена поддержка UltraSSD и образов коллекции в простых наборах параметров для командлетов `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="04529-1343">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="04529-1344">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="04529-1344">Az.DataLakeStore</span></span>

* <span data-ttu-id="04529-1345">Исправлено косую черту в конце домена учетной записи ADLS</span><span class="sxs-lookup"><span data-stu-id="04529-1345">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="04529-1346">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="04529-1346">Az.FrontDoor</span></span>

* <span data-ttu-id="04529-1347">Исправлены некоторые неработающие ссылки</span><span class="sxs-lookup"><span data-stu-id="04529-1347">Fixed some broken links</span></span>
    - <span data-ttu-id="04529-1348">В статьях New-AzureRmFrontDoor и Set-AzureRmFrontDoor исправлена ссылка на статью командлета New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="04529-1348">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="04529-1349">В статье New-AzureRmFrontDoorManagedRuleObject исправлена ссылка на статью командлета New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="04529-1349">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="04529-1350">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="04529-1350">Az.RecoveryServices</span></span>

* <span data-ttu-id="04529-1351">Добавлены проверки на стороне клиента для операций восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="04529-1351">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="04529-1352">StorageAccountName и storageAccountResourceGroupName являются необязательными для восстановления afs.</span><span class="sxs-lookup"><span data-stu-id="04529-1352">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="04529-1353">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="04529-1353">Az.Resources</span></span>

* <span data-ttu-id="04529-1354">Исправление для https://github.com/Azure/azure-powershell/issues/7679.</span><span class="sxs-lookup"><span data-stu-id="04529-1354">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="04529-1355">Обновите Get-AzureRmRoleAssignment, чтобы использовать область подписки, если она указана при запросе классических администраторов.</span><span class="sxs-lookup"><span data-stu-id="04529-1355">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="04529-1356">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="04529-1356">Az.Sql</span></span>

* <span data-ttu-id="04529-1357">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="04529-1357">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="04529-1358">Устранена проблема с использованием Get-AzureRmSqlDatabaseVulnerabilityAssessment с .NET Core.</span><span class="sxs-lookup"><span data-stu-id="04529-1358">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="04529-1359">Изменена документация справочных сообщений, связанных с командлетами аудита SQL.</span><span class="sxs-lookup"><span data-stu-id="04529-1359">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="04529-1360">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="04529-1360">Az.Storage</span></span>

* <span data-ttu-id="04529-1361">Добавлено -EnableHierarchicalNamespace к New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="04529-1361">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="04529-1362">Устранена проблема, из-за которой командлет Copy File не может повторно использовать исходный контекст в пункте назначения, если не введен -DestContext</span><span class="sxs-lookup"><span data-stu-id="04529-1362">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="04529-1363">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="04529-1363">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="04529-1364">Поддержка статической конфигурации сайта</span><span class="sxs-lookup"><span data-stu-id="04529-1364">Support Static Website configuration</span></span>
    - <span data-ttu-id="04529-1365">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="04529-1365">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="04529-1366">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="04529-1366">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="04529-1367">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="04529-1367">Az.Websites</span></span>

* <span data-ttu-id="04529-1368">Set-AzureRmWebApp и Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="04529-1368">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="04529-1369">Добавлен новый параметр (-AzureStoragePath), который указывает путь службы хранилища Azure для подключения в приложениях-контейнерах Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="04529-1369">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="04529-1370">Используйте выходные данные нового командлета New-AzureRmWebAppAzureStoragePath в качестве параметра, чтобы задать пути к службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="04529-1370">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="04529-1371">0.6.1 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="04529-1371">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="04529-1372">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="04529-1372">Az.ApiManagement</span></span>
* <span data-ttu-id="04529-1373">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="04529-1373">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="04529-1374">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="04529-1374">Az.Automation</span></span>
* <span data-ttu-id="04529-1375">Командлеты службы автоматизации Azure на базе Swagger.</span><span class="sxs-lookup"><span data-stu-id="04529-1375">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="04529-1376">Добавлены командлеты для Управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="04529-1376">Added Update Management cmdlets</span></span>
* <span data-ttu-id="04529-1377">Добавлены командлеты для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="04529-1377">Added Source Control cmdlets</span></span>
* <span data-ttu-id="04529-1378">Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="04529-1378">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="04529-1379">Исправлена команда DSC для регистрации узла.</span><span class="sxs-lookup"><span data-stu-id="04529-1379">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="04529-1380">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="04529-1380">Az.Compute</span></span>
* <span data-ttu-id="04529-1381">Исправлена проблема с удостоверением, назначаемым системой.</span><span class="sxs-lookup"><span data-stu-id="04529-1381">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="04529-1382">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="04529-1382">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="04529-1383">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="04529-1383">Az.ContainerInstance</span></span>
* <span data-ttu-id="04529-1384">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="04529-1384">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="04529-1385">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="04529-1385">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="04529-1386">Обновлено описание в примерах командлетов для Marketplace.</span><span class="sxs-lookup"><span data-stu-id="04529-1386">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="04529-1387">Az.Network</span><span class="sxs-lookup"><span data-stu-id="04529-1387">Az.Network</span></span>
* <span data-ttu-id="04529-1388">Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="04529-1388">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="04529-1389">Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="04529-1389">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="04529-1390">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="04529-1390">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="04529-1391">Исправлены проблемы с использованием памяти в карте виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="04529-1391">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="04529-1392">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="04529-1392">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="04529-1393">Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="04529-1393">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="04529-1394">Параметры часового пояса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="04529-1394">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="04529-1395">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="04529-1395">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="04529-1396">Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="04529-1396">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="04529-1397">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="04529-1397">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="04529-1398">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="04529-1398">Az.Relay</span></span>
* <span data-ttu-id="04529-1399">Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.</span><span class="sxs-lookup"><span data-stu-id="04529-1399">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="04529-1400">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="04529-1400">Az.Resources</span></span>
* <span data-ttu-id="04529-1401">Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.</span><span class="sxs-lookup"><span data-stu-id="04529-1401">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="04529-1402">Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.</span><span class="sxs-lookup"><span data-stu-id="04529-1402">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="04529-1403">Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.</span><span class="sxs-lookup"><span data-stu-id="04529-1403">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="04529-1404">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="04529-1404">Az.ServiceFabric</span></span>
* <span data-ttu-id="04529-1405">Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.</span><span class="sxs-lookup"><span data-stu-id="04529-1405">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="04529-1406">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="04529-1406">Az.Sql</span></span>
* <span data-ttu-id="04529-1407">Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="04529-1407">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="04529-1408">Get-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="04529-1408">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="04529-1409">New-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="04529-1409">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="04529-1410">Set-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="04529-1410">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="04529-1411">Remove-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="04529-1411">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="04529-1412">Get-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="04529-1412">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="04529-1413">New-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="04529-1413">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="04529-1414">Restore-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="04529-1414">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="04529-1415">Remove-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="04529-1415">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="04529-1416">Добавлено расширенное управление политиками аудита для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="04529-1416">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="04529-1417">Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="04529-1417">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="04529-1418">Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.</span><span class="sxs-lookup"><span data-stu-id="04529-1418">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="04529-1419">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="04529-1419">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="04529-1420">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="04529-1420">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="04529-1421">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="04529-1421">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="04529-1422">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="04529-1422">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="04529-1423">Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="04529-1423">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="04529-1424">0.5.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="04529-1424">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="04529-1425">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="04529-1425">General</span></span>
* <span data-ttu-id="04529-1426">Добавлены средства заполнения ресурсов для многих основных командлетов — они позволяют вам переключать существующие имена ресурсов при вызове командлетов в интерактивном режиме</span><span class="sxs-lookup"><span data-stu-id="04529-1426">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="04529-1427">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="04529-1427">Az.Profile</span></span>
* <span data-ttu-id="04529-1428">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="04529-1428">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="04529-1429">В командлете Connect-AzAccount параметр TenantId переименован в Tenant и добавлен псевдоним для TenantId</span><span class="sxs-lookup"><span data-stu-id="04529-1429">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="04529-1430">Обновлено описание TenantId для командлета Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="04529-1430">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="04529-1431">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="04529-1431">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="04529-1432">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="04529-1432">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="04529-1433">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="04529-1433">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="04529-1434">Устранена проблема, при которой командлет Disconnect-AzAccount вызывал сбой при отсутствии подключения</span><span class="sxs-lookup"><span data-stu-id="04529-1434">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="04529-1435">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="04529-1435">Az.CognitiveServices</span></span>
* <span data-ttu-id="04529-1436">Добавлена операция Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="04529-1436">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="04529-1437">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="04529-1437">Az.Compute</span></span>
* <span data-ttu-id="04529-1438">Добавлены командлеты Add-AzVmssVMDataDisk и Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="04529-1438">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="04529-1439">Get-AzVMImage отображает AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="04529-1439">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="04529-1440">Устранена проблема, при которой значения параметров SetAzVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="04529-1440">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="04529-1441">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="04529-1441">Az.DataLakeStore</span></span>
* <span data-ttu-id="04529-1442">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="04529-1442">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="04529-1443">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="04529-1443">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="04529-1444">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="04529-1444">Az.Insights</span></span>
* <span data-ttu-id="04529-1445">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="04529-1445">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="04529-1446">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="04529-1446">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="04529-1447">Исправлена проблема № 7513 [Insights], при которой для командлета Set-AzDiagnosticSetting требовалось явное указание категорий во время создания параметра</span><span class="sxs-lookup"><span data-stu-id="04529-1447">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="04529-1448">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="04529-1448">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="04529-1449">Az.Network</span><span class="sxs-lookup"><span data-stu-id="04529-1449">Az.Network</span></span>
* <span data-ttu-id="04529-1450">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="04529-1450">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="04529-1451">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="04529-1451">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="04529-1452">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="04529-1452">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="04529-1453">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="04529-1453">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="04529-1454">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="04529-1454">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="04529-1455">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="04529-1455">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="04529-1456">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="04529-1456">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="04529-1457">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="04529-1457">Az.PolicyInsights</span></span>
* <span data-ttu-id="04529-1458">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="04529-1458">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="04529-1459">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="04529-1459">Az.Resources</span></span>
* <span data-ttu-id="04529-1460">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="04529-1460">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="04529-1461">Разрешено перечисление ресурсов с помощью параметра -ResourceId для командлета Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="04529-1461">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="04529-1462">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="04529-1462">Az.ServiceBus</span></span>
* <span data-ttu-id="04529-1463">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="04529-1463">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="04529-1464">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="04529-1464">Az.ServiceFabric</span></span>
* <span data-ttu-id="04529-1465">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="04529-1465">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="04529-1466">Исправлен командлет Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="04529-1466">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="04529-1467">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="04529-1467">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="04529-1468">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="04529-1468">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="04529-1469">Исправлен командлет Update-AzServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="04529-1469">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="04529-1470">0.4.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="04529-1470">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="04529-1471">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="04529-1471">Az.Profile</span></span>
* <span data-ttu-id="04529-1472">Устранена проблема с Get-AzSubscription в CloudShell</span><span class="sxs-lookup"><span data-stu-id="04529-1472">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="04529-1473">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="04529-1473">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="04529-1474">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="04529-1474">Az.Compute</span></span>
* <span data-ttu-id="04529-1475">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzVm</span><span class="sxs-lookup"><span data-stu-id="04529-1475">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="04529-1476">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="04529-1476">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="04529-1477">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="04529-1477">Az.DataLakeStore</span></span>
* <span data-ttu-id="04529-1478">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="04529-1478">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="04529-1479">Get-AzDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="04529-1479">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="04529-1480">Add-AzDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="04529-1480">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="04529-1481">Set-AzDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="04529-1481">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="04529-1482">Remove-AzDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="04529-1482">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="04529-1483">Az.Network</span><span class="sxs-lookup"><span data-stu-id="04529-1483">Az.Network</span></span>
* <span data-ttu-id="04529-1484">Обновлен командлет Test-AzNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="04529-1484">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="04529-1485">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="04529-1485">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="04529-1486">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="04529-1486">Az.Resources</span></span>
* <span data-ttu-id="04529-1487">Устранена проблема, из-за которой командлет Get-AzRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), благодаря добавлению понятного исключения в сценарий.</span><span class="sxs-lookup"><span data-stu-id="04529-1487">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="04529-1488">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="04529-1488">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="04529-1489">0.3.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="04529-1489">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="04529-1490">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="04529-1490">Azure.Storage</span></span>
* <span data-ttu-id="04529-1491">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="04529-1491">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="04529-1492">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="04529-1492">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="04529-1493">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="04529-1493">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="04529-1494">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="04529-1494">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="04529-1495">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="04529-1495">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="04529-1496">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="04529-1496">Az.CognitiveServices</span></span>
* <span data-ttu-id="04529-1497">Поддержка Get-AzCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="04529-1497">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="04529-1498">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="04529-1498">Az.Compute</span></span>
* <span data-ttu-id="04529-1499">Исправлена команда Get-AzVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов</span><span class="sxs-lookup"><span data-stu-id="04529-1499">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="04529-1500">Добавлен пример использования SimpleParameterSet в справку командлета New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="04529-1500">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="04529-1501">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="04529-1501">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="04529-1502">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="04529-1502">Az.DataFactoryV2</span></span>
* <span data-ttu-id="04529-1503">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="04529-1503">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="04529-1504">Az.Network</span><span class="sxs-lookup"><span data-stu-id="04529-1504">Az.Network</span></span>
* <span data-ttu-id="04529-1505">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="04529-1505">Added NetworkProfile functionality.</span></span> <span data-ttu-id="04529-1506">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="04529-1506">new cmdlets added</span></span>
    - <span data-ttu-id="04529-1507">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="04529-1507">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="04529-1508">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="04529-1508">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="04529-1509">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="04529-1509">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="04529-1510">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="04529-1510">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="04529-1511">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="04529-1511">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="04529-1512">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="04529-1512">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="04529-1513">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="04529-1513">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="04529-1514">Добавлены командлеты: New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="04529-1514">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="04529-1515">Добавлены командлеты: Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="04529-1515">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="04529-1516">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="04529-1516">Az.RedisCache</span></span>
* <span data-ttu-id="04529-1517">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="04529-1517">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="04529-1518">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="04529-1518">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="04529-1519">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="04529-1519">Az.Resources</span></span>
* <span data-ttu-id="04529-1520">Добавлен отсутствующий параметр -Mode в командлет Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="04529-1520">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="04529-1521">Исправлена ошибка командлета Get-AzProviderOperation для операций, когда Origin содержит User</span><span class="sxs-lookup"><span data-stu-id="04529-1521">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="04529-1522">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="04529-1522">Az.Sql</span></span>
* <span data-ttu-id="04529-1523">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="04529-1523">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="04529-1524">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="04529-1524">Az.Websites</span></span>
* <span data-ttu-id="04529-1525">Новый командлет Get-AzWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="04529-1525">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="04529-1526">Новые командлеты New-AzWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows</span><span class="sxs-lookup"><span data-stu-id="04529-1526">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="04529-1527">0.2.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="04529-1527">0.2.0 - September 2018</span></span>
 <span data-ttu-id="04529-1528">Первый выпуск</span><span class="sxs-lookup"><span data-stu-id="04529-1528">Initial Release</span></span>
