---
title: Заметки о выпуске Azure PowerShell
description: Узнайте обо всех последних обновлениях модулей Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/25/2019
ms.openlocfilehash: b879d970d3237098e481dba0419ee65efa8d51cd
ms.sourcegitcommit: f0f09eee03ef9dd7fe07432252a3dc8ca93e3a7b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "71319312"
---
## <a name="270---september-2019"></a><span data-ttu-id="ad5c1-103">2.7.0 — сентябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-103">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="ad5c1-104">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ad5c1-104">Az.ApiManagement</span></span>
* <span data-ttu-id="ad5c1-105">В справочной документации по командлету Set-AzApiManagementPolicy обновлено описание параметра -Format.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-105">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="ad5c1-106">Из справочной документации удалены ссылки на нерекомендуемый командлет Update-AzApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-106">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="ad5c1-107">Вместо него следует использовать командлет Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-107">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ad5c1-108">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ad5c1-108">Az.Automation</span></span>
* <span data-ttu-id="ad5c1-109">В справочной документации по командлету Register-AzAutomationDscNode исправлена опечатка в примере.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-109">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="ad5c1-110">Добавлено уточнение об ограничениях ОС для командлета Register-AzAutomationDSCNode.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-110">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="ad5c1-111">Исправлено исключение пустой ссылки для параметра -Wait в командлете Start-AzAutomationRunbook.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-111">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad5c1-112">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad5c1-112">Az.Compute</span></span>
* <span data-ttu-id="ad5c1-113">Добавлен параметр UploadSizeInBytes для командлета New-AzDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-113">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="ad5c1-114">Добавлен добавочный параметр для командлета New-AzSnapshotConfig.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-114">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="ad5c1-115">Для виртуальной машины добавлены такие функции с низким приоритетом:</span><span class="sxs-lookup"><span data-stu-id="ad5c1-115">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="ad5c1-116">Для командлета New-AzVMConfig добавлены параметры MaxPrice, EvictionPolicy и Priority.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-116">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="ad5c1-117">Для командлетов New-AzVmssConfig, Update-AzVM и Update-AzVmss добавлен параметр MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-117">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="ad5c1-118">Для командлета Get-AzAvailabilitySet устранена проблема со ссылкой на виртуальную машину, когда в нем перечисляются все группы доступности в подписке.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-118">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="ad5c1-119">Исправлено исключение NULL для командлета Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-119">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="ad5c1-120">Исправлен метод поиска VHD для относительной конечной позиции.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-120">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="ad5c1-121">Устранена проблема с UltraSSD для командлетов New-AzVM и Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-121">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ad5c1-122">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ad5c1-122">Az.DataFactory</span></span>
* <span data-ttu-id="ad5c1-123">Добавлены 3 новые команды для ADF версии 2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription и Get-AzDataFactoryV2TriggerSubscriptionStatus.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-123">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="ad5c1-124">Пакет SDK ADF для .NET обновлен до версии 4.1.3.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-124">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="ad5c1-125">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ad5c1-125">Az.HDInsight</span></span>
* <span data-ttu-id="ad5c1-126">Укажите критические изменения.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-126">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ad5c1-127">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ad5c1-127">Az.IotHub</span></span>
* <span data-ttu-id="ad5c1-128">Добавлена поддержка для вызова отработки отказа для IotHub в георегион аварийного восстановления.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-128">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="ad5c1-129">Добавлена поддержка для управления обогащением сообщений для IotHub.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-129">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="ad5c1-130">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="ad5c1-130">New cmdlets are:</span></span>
    - <span data-ttu-id="ad5c1-131">Add-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="ad5c1-131">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="ad5c1-132">Get-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="ad5c1-132">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="ad5c1-133">Remove-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="ad5c1-133">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="ad5c1-134">Set-AzIotHubMessageEnrichment.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-134">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ad5c1-135">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ad5c1-135">Az.Monitor</span></span>
* <span data-ttu-id="ad5c1-136">Указание на самую последнюю версию пакета SDK для монитора, т. е. 0.24.1-preview:</span><span class="sxs-lookup"><span data-stu-id="ad5c1-136">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="ad5c1-137">В командлеты метрик добавлены некритические изменения, т. е. перечисление единиц поддерживает несколько новых значений.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-137">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="ad5c1-138">Эти командлеты доступны только для чтения, поэтому входные данные командлетов не будут изменены.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-138">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="ad5c1-139">Актуальная версия API запросов **ActionGroups** — **2019-06-01**. До этого была версия **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-139">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="ad5c1-140">Тесты сценария обновлены в соответствии с этим изменением.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-140">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="ad5c1-141">В конструкторы классов **EmailReceiver** и **WebhookReceiver** добавлен один новый обязательный аргумент — логическое значение с именем **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-141">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="ad5c1-142">Сейчас для него установлено значение **false**, чтобы скрыть это критическое изменение от командлетов.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-142">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="ad5c1-143">**Примечание**. Это временное изменение, которое должно быть подтверждено командой оповещения.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-143">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="ad5c1-144">Порядок аргументов для конструктора класса **Source** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-144">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="ad5c1-145">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-145">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="ad5c1-146">Порядок аргументов для конструктора класса **AlertingAction** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-146">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="ad5c1-147">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-147">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="ad5c1-148">Добавлена поддержка критериев динамического порога для оповещения метрики версии 2:</span><span class="sxs-lookup"><span data-stu-id="ad5c1-148">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="ad5c1-149">New-AzMetricAlertRuleV2Criteria: теперь также позволяет создавать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-149">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="ad5c1-150">Add-AzMetricAlertRuleV2: теперь также позволяет принимать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-150">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="ad5c1-151">Добавлены усовершенствования в командлетах запланированных правил запросов (SQR).</span><span class="sxs-lookup"><span data-stu-id="ad5c1-151">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="ad5c1-152">Командлеты будут принимать параметр Location в обоих форматах: расположение (например, eastus) или отображаемое имя расположения (например, "восточная часть США").</span><span class="sxs-lookup"><span data-stu-id="ad5c1-152">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="ad5c1-153">Параметр Enabled проиллюстрирован в файлах справки надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-153">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="ad5c1-154">Добавлены примеры для необязательного параметра ActionGroup.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-154">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="ad5c1-155">Все файлы справки улучшены.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-155">Overall improved help files</span></span>
* <span data-ttu-id="ad5c1-156">Исправлена ошибка в определении типа области для командлета Set-AzActionRule.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-156">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ad5c1-157">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad5c1-157">Az.Network</span></span>
* <span data-ttu-id="ad5c1-158">Исправлен неправильный пример в справочной документации по командлету New-AzApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-158">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="ad5c1-159">В справочную документацию по командлету Get-AzNetworkWatcherPacketCapture добавлено примечание, посвященное извлечению всех свойств для записи пакетов.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-159">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="ad5c1-160">В справочной документации по командлету Test-AzNetworkWatcherIPFlow исправлен пример: теперь он правильно перечисляет сетевые карты.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-160">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="ad5c1-161">Улучшен анализ облачных исключений для отображения дополнительных сведений (при их наличии).</span><span class="sxs-lookup"><span data-stu-id="ad5c1-161">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="ad5c1-162">Улучшен анализ облачных исключений для обработки дополнительного типа исключения SDK.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-162">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="ad5c1-163">Исправлено неправильное сопоставление моделей правил безопасности.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-163">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="ad5c1-164">Добавлены свойства сетевого интерфейса для компонента частного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-164">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="ad5c1-165">Для интерфейса PSNetworkInterface добавлено свойство PrivateEndpoint с типом PSResourceId.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-165">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="ad5c1-166">В PSNetworkInterfaceIPConfiguration добавлено свойство PrivateLinkConnectionProperties с типом PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-166">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="ad5c1-167">Добавлен новый класс модели: PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-167">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="ad5c1-168">Добавлен новый тип ApplicationRuleProtocolType "mssql" для ресурса Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-168">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="ad5c1-169">Поддержка многоканального подключения в Виртуальной глобальной сети:</span><span class="sxs-lookup"><span data-stu-id="ad5c1-169">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="ad5c1-170">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="ad5c1-170">New cmdlets</span></span>
        - <span data-ttu-id="ad5c1-171">New-AzVpnSiteLink;</span><span class="sxs-lookup"><span data-stu-id="ad5c1-171">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="ad5c1-172">New-AzVpnSiteLinkConnection;</span><span class="sxs-lookup"><span data-stu-id="ad5c1-172">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="ad5c1-173">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="ad5c1-173">Updated cmdlet:</span></span>
        - <span data-ttu-id="ad5c1-174">New-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="ad5c1-174">New-VpnSite</span></span>
        - <span data-ttu-id="ad5c1-175">Update-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="ad5c1-175">Update-VpnSite</span></span>
        - <span data-ttu-id="ad5c1-176">New-VpnConnection;</span><span class="sxs-lookup"><span data-stu-id="ad5c1-176">New-VpnConnection</span></span>
        - <span data-ttu-id="ad5c1-177">Update-VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-177">Update-VpnConnection</span></span>
* <span data-ttu-id="ad5c1-178">Исправлены документы с некоторыми примерами PowerShell для использования командлетов AZ вместо командлетов AzureRM.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-178">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ad5c1-179">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ad5c1-179">Az.RecoveryServices</span></span>
* <span data-ttu-id="ad5c1-180">Для объекта AzureVMpolicy добавлен новый атрибут — ProtectedItemsCount.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-180">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="ad5c1-181">Добавлены тесты для политики виртуальной машины и восстановления исходной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-181">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad5c1-182">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad5c1-182">Az.Resources</span></span>
* <span data-ttu-id="ad5c1-183">Исправлена ошибка, при которой не удавалось вызвать командлет New-AzRoleAssignment без параметра Scope.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-183">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ad5c1-184">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ad5c1-184">Az.ServiceFabric</span></span>
* <span data-ttu-id="ad5c1-185">Исправлена опечатка в примере в справочной документации по командлету Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-185">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="ad5c1-186">Добавлены новые командлеты для управления приложениями и службами:</span><span class="sxs-lookup"><span data-stu-id="ad5c1-186">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="ad5c1-187">New-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="ad5c1-187">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="ad5c1-188">New-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="ad5c1-188">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="ad5c1-189">New-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="ad5c1-189">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="ad5c1-190">New-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="ad5c1-190">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="ad5c1-191">Update-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="ad5c1-191">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="ad5c1-192">Get-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="ad5c1-192">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="ad5c1-193">Get-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="ad5c1-193">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="ad5c1-194">Get-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="ad5c1-194">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="ad5c1-195">Get-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="ad5c1-195">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="ad5c1-196">Remove-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="ad5c1-196">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="ad5c1-197">Remove-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="ad5c1-197">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="ad5c1-198">Remove-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="ad5c1-198">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="ad5c1-199">Remove-AzServiceFabricServic.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-199">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="ad5c1-200">Пакет SDK для Service Fabric обновлен до версии 1.2.0, в которой используется версия API 2019-03-01 поставщика ресурсов Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-200">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="ad5c1-201">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="ad5c1-201">Az.SignalR</span></span>
* <span data-ttu-id="ad5c1-202">Добавлены командлеты Update, Restart, CheckNameAvailability и GetUsage.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-202">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad5c1-203">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad5c1-203">Az.Sql</span></span>
* <span data-ttu-id="ad5c1-204">Обновлен пример в справочной документации по командлету Get-AzSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-204">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="ad5c1-205">Добавлен пример виртуального ядра для командлета создания эластичного пула (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="ad5c1-205">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="ad5c1-206">Удалена проверка свойства EmailAddresses и того, что свойство EmailAdmins правильное в случае, если свойство EmailAddresses пустое в командлетах Set-AzSqlServerAdvancedThreatProtectionPolicy и Set-AzSqlDatabaseAdvancedThreatProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-206">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="ad5c1-207">Теперь, если существует несколько параметров диагностики, включающих категорию аудита, параметры аудита сервера и базы данных удаляются.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-207">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="ad5c1-208">Исправлена проверка адресов электронной почты в нескольких командлетах оценки уязвимостей SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting и Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="ad5c1-208">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ad5c1-209">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ad5c1-209">Az.Storage</span></span>
* <span data-ttu-id="ad5c1-210">Обновлен пример в справочной документации по командлету Get-AzStorageAccountKey.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-210">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="ad5c1-211">Теперь при отправке и загрузке файла Azure в конечном файле сохраняются свойства SMB исходного файла (атрибуты файла, время создания файла, время последней записи файла).</span><span class="sxs-lookup"><span data-stu-id="ad5c1-211">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="ad5c1-212">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ad5c1-212">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="ad5c1-213">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ad5c1-213">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="ad5c1-214">Исправлена операция отправки блочного BLOB-объекта, в которой происходили сбои свойств и метаданных в контейнере с включенной ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-214">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="ad5c1-215">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ad5c1-215">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="ad5c1-216">Добавлена поддержка управления общими папками Azure в API плоскости управления с помощью таких командлетов:</span><span class="sxs-lookup"><span data-stu-id="ad5c1-216">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="ad5c1-217">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="ad5c1-217">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="ad5c1-218">Get-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="ad5c1-218">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="ad5c1-219">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="ad5c1-219">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="ad5c1-220">Remove-AzRmStorageShare.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-220">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ad5c1-221">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ad5c1-221">Az.Websites</span></span>
* <span data-ttu-id="ad5c1-222">Устранена проблема, из-за которой теги webapp удалялись при переносе приложения в новый ASP.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-222">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="ad5c1-223">Теперь командлет Publish-AzureWebapp работает в Linux и Windows.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-223">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="ad5c1-224">Обновлен пример в справочной документации по командлету Get-AzWebAppPublishingProfile.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-224">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="ad5c1-225">2.6.0 — август 2019 г.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-225">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="ad5c1-226">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="ad5c1-226">General</span></span>
* <span data-ttu-id="ad5c1-227">Исправлены опечатки в модулях.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-227">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ad5c1-228">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ad5c1-228">Az.Accounts</span></span>
* <span data-ttu-id="ad5c1-229">Добавлена поддержка назначаемого пользователем удостоверения MSI при проверке подлинности в Функциях Azure (№ 9479).</span><span class="sxs-lookup"><span data-stu-id="ad5c1-229">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="ad5c1-230">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="ad5c1-230">Az.Aks</span></span>
* <span data-ttu-id="ad5c1-231">Устранена проблема с выходными данными для Get-AzAks.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-231">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="ad5c1-232">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9847.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-232">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="ad5c1-233">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ad5c1-233">Az.ApiManagement</span></span>
* <span data-ttu-id="ad5c1-234">исправлена проблема https://github.com/Azure/azure-powershell/issues/9351.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-234">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="ad5c1-235">Обновлена версия NuGet для .NET, которая не накладывает ограничений на productId, apiId, groupId и userId.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-235">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="ad5c1-236">**Get-AzApiManagementProduct**. Добавлена поддержка запросов к продуктам с помощью API.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-236">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="ad5c1-237">**New-AzApiManagementApiRevision**. Устранена проблема, из-за которой не задавался параметр ApiRevisionDescription при создании новой редакции API https://github.com/Azure/azure-powershell/issues/9752.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-237">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="ad5c1-238">Исправлено написание имени модели c PsApiManagementOAuth2AuthrozationServer на PsApiManagementOAuth2AuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-238">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="ad5c1-239">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ad5c1-239">Az.Batch</span></span>
* <span data-ttu-id="ad5c1-240">Исправлена опечатка в написании Windows со строчной буквы в справочных сообщениях и документации.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-240">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ad5c1-241">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ad5c1-241">Az.Cdn</span></span>
* <span data-ttu-id="ad5c1-242">Исправлена опечатка во вспомогательном приложении модуля CDN.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-242">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad5c1-243">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad5c1-243">Az.Compute</span></span>
* <span data-ttu-id="ad5c1-244">Добавлен параметр VmssId в новый командлет Add New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-244">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="ad5c1-245">Добавлены параметры TerminateScheduledEvents и TerminateScheduledEventNotBeforeTimeoutInMinutes в New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-245">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="ad5c1-246">Добавлено свойство HyperVGeneration в объект образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-246">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="ad5c1-247">Добавлены компоненты Host и HostGroup.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-247">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="ad5c1-248">Новые командлеты:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="ad5c1-248">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="ad5c1-249">Параметр HostId добавлен в New-AzVMConfig и New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-249">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="ad5c1-250">Исправлен пример в документации по Invoke-AzVMRunCommand, в котором теперь используется правильное имя параметра.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-250">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="ad5c1-251">Исправлено описание VolumeType в справочной документации по Set-AzVMDiskEncryptionExtension и Set-AzVmssDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-251">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ad5c1-252">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ad5c1-252">Az.DataFactory</span></span>
* <span data-ttu-id="ad5c1-253">Исправлена опечатка в написании Windows со строчной буквы в документации по New-AzDataFactoryEncryptValue.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-253">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="ad5c1-254">Пакет SDK ADF для .NET обновлен до версии 4.1.2.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-254">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="ad5c1-255">Добавлены параметры DataProxyIntegrationRuntimeName, DataProxyStagingLinkedServiceName и DataProxyStagingPath в командлет Set-AzureRmDataFactoryV2IntegrationRuntime, что позволяет настраивать локальную среду выполнения интеграции в качестве прокси-сервера для Azure-SSIS Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-255">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="ad5c1-256">Обновлены PSTriggerRun для отображения активированных конвейеров, сообщений и свойств и PSActivityRun для отображения типа действия.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-256">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ad5c1-257">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ad5c1-257">Az.DataLakeStore</span></span>
* <span data-ttu-id="ad5c1-258">Устранена проблема, при которой Get-DataLakeStoreDeletedItem переставал отвечать на запросы при возникновении ошибок или удаленных исключений.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-258">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ad5c1-259">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ad5c1-259">Az.EventHub</span></span>
* <span data-ttu-id="ad5c1-260">Исправлена проблема № 9658: опечатка в написании параметра VirtualNteworkRule у Set-AzEventHubNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-260">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="ad5c1-261">Исправлена проблема № 9558: в Set-AzEventHubNamespace используется PATCH вместо PUT.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-261">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="ad5c1-262">В командлет Set-AzEventHubNamespace добавлен параметр EnableKafka.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-262">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="ad5c1-263">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-263">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="ad5c1-264">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="ad5c1-264">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="ad5c1-265">Исправлено написание Azure со строчной буквы.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-265">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ad5c1-266">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ad5c1-266">Az.Monitor</span></span>
* <span data-ttu-id="ad5c1-267">Исправлены неправильные имена параметров в справочной документации.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-267">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ad5c1-268">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad5c1-268">Az.Network</span></span>
* <span data-ttu-id="ad5c1-269">Обновлен New-AzPrivateLinkServiceIpConfig.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-269">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="ad5c1-270">Параметр PublicIpAddress объявлен нерекомендуемым, так как он не используется на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-270">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="ad5c1-271">Добавлен необязательный параметр Primary, указывающий, является ли текущая IP-конфигурация основной.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-271">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="ad5c1-272">Улучшена обработка исключений из-за ошибок запроса от пакета SDK. Устранена проблема, при которой исключения пакета SDK не обрабатывались правильно, из-за чего не отображались основные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-272">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="ad5c1-273">Настроена логика проверки для префикса IPv6 IP-адреса для проверки правильности длины префикса IPv6.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-273">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="ad5c1-274">Обновлен Get-AzVirtualNetworkSubnetConfig: добавлен набор параметров для получения по идентификатору ресурса подсети.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-274">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="ad5c1-275">Обновлено описание параметра Location для AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-275">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ad5c1-276">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ad5c1-276">Az.OperationalInsights</span></span>
* <span data-ttu-id="ad5c1-277">Обновлена документация по New-AzOperationalInsightsLinuxSyslogDataSource.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-277">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="ad5c1-278">Добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-278">Added example</span></span>
    - <span data-ttu-id="ad5c1-279">Обновлено описание параметра -Name.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-279">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="ad5c1-280">Добавлен пример для New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="ad5c1-280">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="ad5c1-281">Изменено описание параметра -Name для New-AzOperationalInsightsWindowsEventDataSource.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-281">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ad5c1-282">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ad5c1-282">Az.RecoveryServices</span></span>
* <span data-ttu-id="ad5c1-283">Обновлен Get-AzRecoveryServicesBackupJobDetail.md.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-283">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad5c1-284">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad5c1-284">Az.Resources</span></span>
* <span data-ttu-id="ad5c1-285">Добавлена поддержка новой версии API 2019-05-10 для Microsoft.Resource.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-285">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="ad5c1-286">Добавлена поддержка copy.count = 0 для переменных, ресурсов и свойств.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-286">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="ad5c1-287">Ресурсы, у которых condition = false или copy.count = 0, будут удаляться в полном режиме.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-287">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="ad5c1-288">В справочную документацию добавлен пример назначения политики на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-288">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ad5c1-289">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ad5c1-289">Az.ServiceBus</span></span>
* <span data-ttu-id="ad5c1-290">Исправлена проблема № 9658: опечатка в написании параметра VirtualNetworkRule В Set-AzServiceBusNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-290">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="ad5c1-291">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-291">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="ad5c1-292">Добавлена новая команда Test-AzServiceBusNameAvailability для проверки доступности имени для очереди и раздела.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-292">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="ad5c1-293">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ad5c1-293">Az.ServiceFabric</span></span>
* <span data-ttu-id="ad5c1-294">Устранены ошибки командлета для добавления типа узла:</span><span class="sxs-lookup"><span data-stu-id="ad5c1-294">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="ad5c1-295">ошибка NullReferenceException, возникавшая, если у группы ресурсов были другие VMSS, не связанные с кластером Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-295">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="ad5c1-296">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8681.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-296">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="ad5c1-297">Исправлена ошибка, из-за которой командлет завершился сбоем, если virtualNetwork находилась не в той группе ресурсов, к которой относится кластер.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-297">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="ad5c1-298">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8407.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-298">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="ad5c1-299">Командлет Add-AzServiceFabricApplicationCertificate объявлен нерекомендуемым.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-299">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad5c1-300">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad5c1-300">Az.Sql</span></span>
* <span data-ttu-id="ad5c1-301">Обновление документации по старым командлетам аудита.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-301">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ad5c1-302">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ad5c1-302">Az.Storage</span></span>
* <span data-ttu-id="ad5c1-303">Обновлена справка по Get/Close-AzStorageFileHandle: в примеры добавлены сценарии использования командлетов и обновлено описание параметров.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-303">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="ad5c1-304">Добавлена поддержка StandardBlobTier в операции отправки BLOB-объекта и копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-304">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="ad5c1-305">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ad5c1-305">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="ad5c1-306">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="ad5c1-306">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="ad5c1-307">Добавлена поддержка приоритета восстановления в операцию копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-307">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="ad5c1-308">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="ad5c1-308">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ad5c1-309">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ad5c1-309">Az.Websites</span></span>
* <span data-ttu-id="ad5c1-310">Добавлены уточнение для параметра -AppSettings в Set-AzWebApp и Set-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-310">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="ad5c1-311">2.5.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-311">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ad5c1-312">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ad5c1-312">Az.Accounts</span></span>
* <span data-ttu-id="ad5c1-313">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-313">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="ad5c1-314">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="ad5c1-314">Az.ApplicationInsights</span></span>
* <span data-ttu-id="ad5c1-315">Исправлена опечатка в примере в документации по Remove-AzApplicationInsightsApiKey.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-315">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="ad5c1-316">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ad5c1-316">Az.Automation</span></span>
* <span data-ttu-id="ad5c1-317">Исправлена опечатка в строке ресурса.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-317">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="ad5c1-318">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ad5c1-318">Az.CognitiveServices</span></span>
* <span data-ttu-id="ad5c1-319">Добавлена поддержка NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-319">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad5c1-320">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad5c1-320">Az.Compute</span></span>
* <span data-ttu-id="ad5c1-321">Добавлены недостающие свойства (ComputerName, OsName, OsVersion и HyperVGeneration) для объекта представления экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-321">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="ad5c1-322">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ad5c1-322">Az.ContainerRegistry</span></span>
* <span data-ttu-id="ad5c1-323">Исправлена опечатка в Remove-AzContainerRegistryReplication для параметра репликации.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-323">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="ad5c1-324">См. подробнее: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-324">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ad5c1-325">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ad5c1-325">Az.DataFactory</span></span>
* <span data-ttu-id="ad5c1-326">Пакет SDK для ADF .NET обновлен до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-326">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="ad5c1-327">Исправлена опечатка в документации по Get-AzDataFactoryV2PipelineRun.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-327">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ad5c1-328">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ad5c1-328">Az.EventHub</span></span>
* <span data-ttu-id="ad5c1-329">Добавлен новый командлет для создания маркера SAS: New-AzEventHubAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-329">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="ad5c1-330">Добавлена проверка и сообщение об ошибке для случаев, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="ad5c1-330">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ad5c1-331">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ad5c1-331">Az.KeyVault</span></span>
* <span data-ttu-id="ad5c1-332">Добавлена поддержка для настройки параметра KeySize в политиках сертификатов.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-332">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ad5c1-333">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ad5c1-333">Az.LogicApp</span></span>
* <span data-ttu-id="ad5c1-334">Get-AzIntegrationAccountMap теперь надлежащим образом выводит все типы сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-334">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="ad5c1-335">Добавлен новый параметр MapType для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-335">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="ad5c1-336">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="ad5c1-336">Az.ManagedServices</span></span>
* <span data-ttu-id="ad5c1-337">Добавлена поддержка API версии 2019-06-01 (общедоступная).</span><span class="sxs-lookup"><span data-stu-id="ad5c1-337">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ad5c1-338">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad5c1-338">Az.Network</span></span>
* <span data-ttu-id="ad5c1-339">Добавлена поддержка частной конечной точки и службы приватного канала.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-339">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="ad5c1-340">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="ad5c1-340">New cmdlets</span></span>
        - <span data-ttu-id="ad5c1-341">Set-AzPrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-341">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="ad5c1-342">Set-AzPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-342">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="ad5c1-343">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-343">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ad5c1-344">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-344">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ad5c1-345">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-345">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ad5c1-346">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-346">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ad5c1-347">Test-AzPrivateLinkServiceVisibility.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-347">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="ad5c1-348">Get-AzAutoApprovedPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-348">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="ad5c1-349">Обновлены следующие команды для функции: Флаг PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies в подсети в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-349">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="ad5c1-350">Обновлены командлеты New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-350">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="ad5c1-351">Добавлен необязательный параметр -PrivateEndpointNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к частной конечной точке в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-351">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="ad5c1-352">Добавлен необязательный параметр -PrivateLinkServiceNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к службе приватного канала в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-352">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="ad5c1-353">Параметр ServiceName командлета AzPrivateLinkService был переименован на Name с псевдонимом ServiceName для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-353">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="ad5c1-354">Включен протокол ICMP для настройки правил безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-354">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="ad5c1-355">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="ad5c1-355">Updated cmdlets</span></span>
        - <span data-ttu-id="ad5c1-356">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-356">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="ad5c1-357">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-357">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="ad5c1-358">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-358">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="ad5c1-359">Добавлен ConnectionProtocolType (Ikev1/Ikev2) в качестве настраиваемого параметра для командлета New-AzVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-359">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="ad5c1-360">Добавлен PrivateIpAddressVersion в LoadBalancerFrontendIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-360">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="ad5c1-361">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="ad5c1-361">Updated cmdlet:</span></span>
        - <span data-ttu-id="ad5c1-362">New-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-362">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="ad5c1-363">Add-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-363">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="ad5c1-364">Set-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-364">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="ad5c1-365">Команда New-AzApplicationGatewayProbeConfig Шлюза приложений обновлена для поддержки настраиваемого порта в зонде.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-365">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="ad5c1-366">Обновлен командлет New-AzApplicationGatewayProbeConfig: добавлен необязательный параметр Port, который используется при проверке внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-366">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="ad5c1-367">Этот параметр применяется к номерам SKU Standard_V2 и WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-367">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ad5c1-368">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ad5c1-368">Az.OperationalInsights</span></span>
* <span data-ttu-id="ad5c1-369">Обновленная версия по умолчанию для сохраненных операций поиска имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-369">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="ad5c1-370">Исправлены ошибки при обработке регулярных выражений со значениями NULL в журналах.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-370">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ad5c1-371">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ad5c1-371">Az.RecoveryServices</span></span>
* <span data-ttu-id="ad5c1-372">Обновлен файл Get-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-372">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="ad5c1-373">Обновлен файл Get-AzRecoveryServicesBackupContainer.md.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-373">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="ad5c1-374">Обновлен файл Get-AzRecoveryServicesVault.md.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-374">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="ad5c1-375">Обновлен файл Wait-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-375">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="ad5c1-376">Обновлен файл Set-AzRecoveryServicesVaultContext.md.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-376">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="ad5c1-377">Обновлен файл Get-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-377">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="ad5c1-378">Обновлен файл Get-AzRecoveryServicesBackupRecoveryPoint.md.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-378">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="ad5c1-379">Обновлен файл Restore-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-379">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="ad5c1-380">Обновлен вызов службы для отмены регистрации контейнера в общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-380">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="ad5c1-381">Обновлен файл Set-AzRecoveryServicesAsrAlertSetting.md.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-381">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad5c1-382">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad5c1-382">Az.Resources</span></span>
- <span data-ttu-id="ad5c1-383">Удален отсутствующий командлет, который упоминается в документации по New-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-383">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="ad5c1-384">Обновлены командлеты политик для использования новой версии API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-384">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ad5c1-385">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ad5c1-385">Az.ServiceBus</span></span>
* <span data-ttu-id="ad5c1-386">Добавлен новый командлет для создания маркера SAS: New-AzServiceBusAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-386">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="ad5c1-387">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="ad5c1-387">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad5c1-388">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad5c1-388">Az.Sql</span></span>
* <span data-ttu-id="ad5c1-389">Исправлены отсутствующие примеры для командлета Set-AzSqlDatabaseSecondary.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-389">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="ad5c1-390">Исправлены заданные повторяющиеся проверки для оценки наличия уязвимостей без указания адресов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-390">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="ad5c1-391">Исправлена незначительная опечатка в сообщении предупреждения.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-391">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ad5c1-392">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ad5c1-392">Az.Storage</span></span>
* <span data-ttu-id="ad5c1-393">Обновлен пример в справочной документации для использования командлетом Get-AzStorageAccount правильного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-393">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="ad5c1-394">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="ad5c1-394">Az.StorageSync</span></span>
* <span data-ttu-id="ad5c1-395">Добавлен командлет Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-395">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="ad5c1-396">Исправлена проблема № 9551, связанная с TierFilesOlderThanDays.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-396">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ad5c1-397">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ad5c1-397">Az.Websites</span></span>
* <span data-ttu-id="ad5c1-398">Исправлена ошибка, при которой некоторые свойства SiteConfig не возвращались Get-AzWebApp и Set-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-398">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="ad5c1-399">Добавлен новый параметр Location в Get-AzDeletedWebApp и Restore-AzDeletedWebApp.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-399">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="ad5c1-400">Исправлена ошибка, которая возникала при клонировании слотов веб-приложений с помощью командлета New-AzWebApp-IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-400">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="ad5c1-401">2.4.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-401">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ad5c1-402">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ad5c1-402">Az.Accounts</span></span>
* <span data-ttu-id="ad5c1-403">Добавлена поддержка командлетов профиля.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-403">Add support for profile cmdlets</span></span>
* <span data-ttu-id="ad5c1-404">Добавлена поддержка сред и плоскостей данных в созданных командлетах.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-404">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="ad5c1-405">Исправлена ошибка, когда в командлетах плоскости данных в Windows PowerShell в некоторых случаях использовалась неправильная конечная точка.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-405">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="ad5c1-406">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="ad5c1-406">Az.Advisor</span></span>
* <span data-ttu-id="ad5c1-407">Выпущена общедоступная версия Az.Advisor.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-407">GA release of Az.Advisor</span></span>
* <span data-ttu-id="ad5c1-408">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-408">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="ad5c1-409">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ad5c1-409">Az.ApiManagement</span></span>
* <span data-ttu-id="ad5c1-410">исправлена проблема https://github.com/Azure/azure-powershell/issues/8671.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-410">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="ad5c1-411">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="ad5c1-411">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="ad5c1-412">Добавлена поддержка запрашивания подписок по пользователю и продукту.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-412">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="ad5c1-413">Добавлена поддержка создания запросов с использованием области "/", "/apis", "/apis/echo-api".</span><span class="sxs-lookup"><span data-stu-id="ad5c1-413">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="ad5c1-414">Исправлены проблемы https://github.com/Azure/azure-powershell/issues/9307 и https://github.com/Azure/azure-powershell/issues/8432.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-414">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="ad5c1-415">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="ad5c1-415">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="ad5c1-416">Добавлена поддержка указания ApiVersion и ApiVersionSetId при импорте API-интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-416">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ad5c1-417">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ad5c1-417">Az.Automation</span></span>
* <span data-ttu-id="ad5c1-418">Исправлена ошибка командлета Set-AzAutomationConnectionFieldValue при обработке строкового значения.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-418">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad5c1-419">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad5c1-419">Az.Compute</span></span>
* <span data-ttu-id="ad5c1-420">В New AzImageConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-420">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ad5c1-421">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ad5c1-421">Az.DataFactory</span></span>
* <span data-ttu-id="ad5c1-422">Обновление выходных данных командлетов ADF, предназначенных для получения числа выполнений действий, конвейеров и триггеров, для поддержки канала Select-Object.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-422">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ad5c1-423">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ad5c1-423">Az.EventGrid</span></span>
* <span data-ttu-id="ad5c1-424">Исправлена опечатка в документации по командлету New-AzEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-424">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ad5c1-425">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ad5c1-425">Az.IotHub</span></span>
* <span data-ttu-id="ad5c1-426">Добавлена поддержка повторного создания ключей политики авторизации.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-426">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ad5c1-427">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad5c1-427">Az.Network</span></span>
* <span data-ttu-id="ad5c1-428">К тегам общедоступного IP-адреса добавлен тег RoutingPreference.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-428">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="ad5c1-429">Улучшены примеры для справочной документации по командлету Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-429">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ad5c1-430">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ad5c1-430">Az.PolicyInsights</span></span>
* <span data-ttu-id="ad5c1-431">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-431">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="ad5c1-432">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9446.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-432">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ad5c1-433">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ad5c1-433">Az.OperationalInsights</span></span>
* <span data-ttu-id="ad5c1-434">Исправленная модель источника данных CustomLog возвращена в командлет Get-AzOperationalInsightsDataSource.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-434">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ad5c1-435">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ad5c1-435">Az.RecoveryServices</span></span>
* <span data-ttu-id="ad5c1-436">Выпущено исправление для команды get-policy для виртуальных машин IaaS.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-436">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad5c1-437">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad5c1-437">Az.Resources</span></span>
    - <span data-ttu-id="ad5c1-438">Исправлен текст справки по параметру Get-AzPolicyState -Top.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-438">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="ad5c1-439">Добавлена поддержка разбиения по страницам на стороне клиента для Get-AzPolicyAlias.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-439">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="ad5c1-440">Добавлены новые параметры для Set-AzPolicyAssignment, -PolicyParameters и -PolicyParametersObject.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-440">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="ad5c1-441">Добавлен ряд обновлений документов и примеров для командлетов политик.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-441">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ad5c1-442">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ad5c1-442">Az.ServiceBus</span></span>
* <span data-ttu-id="ad5c1-443">Исправление ошибки № 4938: командлет New-AzureRmServiceBusQueue возвращает ответ BadRequest (Недопустимый запрос) при задании значения MaxSizeInMegabytes.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-443">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad5c1-444">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad5c1-444">Az.Sql</span></span>
* <span data-ttu-id="ad5c1-445">Из выпуска предварительной версии в выпуск общедоступной версии добавлены командлеты группы отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-445">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="ad5c1-446">Поддержка аудита Azure SQL Server и баз данных с помощью новых командлетов:</span><span class="sxs-lookup"><span data-stu-id="ad5c1-446">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="ad5c1-447">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="ad5c1-447">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="ad5c1-448">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="ad5c1-448">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="ad5c1-449">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="ad5c1-449">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="ad5c1-450">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="ad5c1-450">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="ad5c1-451">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="ad5c1-451">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="ad5c1-452">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="ad5c1-452">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="ad5c1-453">Из параметров оценки уязвимостей удалены ограничения, касающиеся электронной почты.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-453">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ad5c1-454">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ad5c1-454">Az.Storage</span></span>
* <span data-ttu-id="ad5c1-455">Два параметра в указанном ниже командлете — -IndexDocument и -ErrorDocument404Path, — которые ранее были обязательными, стали необязательными:</span><span class="sxs-lookup"><span data-stu-id="ad5c1-455">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="ad5c1-456">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="ad5c1-456">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="ad5c1-457">Обновлена справка по командлету Get-AzStorageBlobContent: добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-457">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="ad5c1-458">При сбое выполнения командлета с ошибкой StorageException отображаются дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-458">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="ad5c1-459">Добавлена поддержка создания или обновления учетной записи хранения с использованием проверки подлинности AAD DS для службы "Файлы Azure".</span><span class="sxs-lookup"><span data-stu-id="ad5c1-459">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="ad5c1-460">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ad5c1-460">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="ad5c1-461">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ad5c1-461">Set-AzStorageAccount</span></span>
* <span data-ttu-id="ad5c1-462">Добавлена поддержка перечисления или закрытия дескрипторов файлов для общей папки, каталога файлов или файла:</span><span class="sxs-lookup"><span data-stu-id="ad5c1-462">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="ad5c1-463">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="ad5c1-463">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="ad5c1-464">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="ad5c1-464">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="ad5c1-465">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="ad5c1-465">Az.StorageSync</span></span>
* <span data-ttu-id="ad5c1-466">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-466">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="ad5c1-467">2.3.2 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-467">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ad5c1-468">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ad5c1-468">Az.Accounts</span></span>
* <span data-ttu-id="ad5c1-469">Исправлена ошибка, связанная с использованием неправильного URL-адреса для вызовов функций.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-469">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="ad5c1-470">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8983.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-470">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="ad5c1-471">Устранена проблема с псевдонимами из AzureRM для командлетов Az.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-471">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="ad5c1-472">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-472">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="ad5c1-473">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-473">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad5c1-474">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad5c1-474">Az.Compute</span></span>
* <span data-ttu-id="ad5c1-475">Простые наборы параметров New-AzVm и New-AzVmss теперь принимают параметр ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-475">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="ad5c1-476">Исправлена опечатка в справочной документации по New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-476">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="ad5c1-477">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="ad5c1-477">Az.Dns</span></span>
* <span data-ttu-id="ad5c1-478">Исправлена опечатка в справочных примерах по использованию Set-AzDnsZone.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-478">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ad5c1-479">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ad5c1-479">Az.EventGrid</span></span>
* <span data-ttu-id="ad5c1-480">Обновлен для использования API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-480">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="ad5c1-481">Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="ad5c1-481">New cmdlets:</span></span>
    - <span data-ttu-id="ad5c1-482">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="ad5c1-482">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="ad5c1-483">Создает домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-483">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="ad5c1-484">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="ad5c1-484">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="ad5c1-485">Возвращает сведения о домене Сетки событий или список всех доменов Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-485">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="ad5c1-486">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="ad5c1-486">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="ad5c1-487">Удаляет домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-487">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="ad5c1-488">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="ad5c1-488">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="ad5c1-489">Повторно создает ключ общего доступа для домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-489">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="ad5c1-490">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="ad5c1-490">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="ad5c1-491">Возвращает ключи общего доступа, используемые для публикации событий в домене Сетки событий.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-491">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="ad5c1-492">New-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="ad5c1-492">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="ad5c1-493">Создает раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-493">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="ad5c1-494">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="ad5c1-494">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="ad5c1-495">Возвращает сведения о разделе домена Сетки событий или список всех разделов определенного домена Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-495">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="ad5c1-496">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="ad5c1-496">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="ad5c1-497">Удаляет раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-497">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="ad5c1-498">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="ad5c1-498">Updated cmdlets:</span></span>
    - <span data-ttu-id="ad5c1-499">New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="ad5c1-499">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="ad5c1-500">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для нового домена Сетки событий и раздела домена Сетки событий и позволяющие создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-500">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="ad5c1-501">Добавляют новые обязательные параметры для указания имени нового домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-501">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="ad5c1-502">Добавляют новые наборы параметров для доменов и разделов домена и позволяют повторно использовать существующие параметры (например, EndPointType, SubjectBeginsWith и т. д.).</span><span class="sxs-lookup"><span data-stu-id="ad5c1-502">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="ad5c1-503">Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="ad5c1-503">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="ad5c1-504">срока действия подписки на событие;</span><span class="sxs-lookup"><span data-stu-id="ad5c1-504">Event subscription expiration date,</span></span>
            - <span data-ttu-id="ad5c1-505">параметров расширенной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-505">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="ad5c1-506">Добавляют новое перечисление для ServiceBusQueue в качестве места назначения.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-506">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="ad5c1-507">Запрещают использование значение All в параметре -IncludedEventType и заменяют его следующим:</span><span class="sxs-lookup"><span data-stu-id="ad5c1-507">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="ad5c1-508">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="ad5c1-508">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="ad5c1-509">Добавляют новые необязательные параметры (Top, ODataQuery и NextLink) для поддержки разбиения на страницы и фильтрации результатов.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-509">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="ad5c1-510">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="ad5c1-510">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="ad5c1-511">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для домена Сетки событий и раздела домена Сетки событий и позволяющие удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-511">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="ad5c1-512">Добавляют новые обязательные параметры для указания имени домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-512">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="ad5c1-513">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ad5c1-513">Az.FrontDoor</span></span>
* <span data-ttu-id="ad5c1-514">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="ad5c1-514">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="ad5c1-515">Добавляет поддержку преобразований и новое значение оператора автозавершения (RegEx).</span><span class="sxs-lookup"><span data-stu-id="ad5c1-515">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="ad5c1-516">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="ad5c1-516">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="ad5c1-517">Добавляет новые значения автозавершения.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-517">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ad5c1-518">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad5c1-518">Az.Network</span></span>
* <span data-ttu-id="ad5c1-519">Добавляет поддержку ресурса шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-519">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="ad5c1-520">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="ad5c1-520">New cmdlets</span></span>
        - <span data-ttu-id="ad5c1-521">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="ad5c1-521">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="ad5c1-522">Добавляет AvailablePrivateEndpointType.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-522">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="ad5c1-523">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="ad5c1-523">New cmdlets</span></span> 
        - <span data-ttu-id="ad5c1-524">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="ad5c1-524">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="ad5c1-525">Добавляет PrivatePrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-525">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="ad5c1-526">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="ad5c1-526">New cmdlets</span></span> 
        - <span data-ttu-id="ad5c1-527">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ad5c1-527">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="ad5c1-528">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ad5c1-528">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="ad5c1-529">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ad5c1-529">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="ad5c1-530">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ad5c1-530">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="ad5c1-531">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ad5c1-531">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="ad5c1-532">Добавляет PrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-532">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="ad5c1-533">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="ad5c1-533">New cmdlets</span></span>
        - <span data-ttu-id="ad5c1-534">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ad5c1-534">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="ad5c1-535">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ad5c1-535">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="ad5c1-536">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ad5c1-536">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="ad5c1-537">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="ad5c1-537">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="ad5c1-538">Обновлены следующие команды для функции: флаг UseLocalAzureIpAddress для VPN-подключения.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-538">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="ad5c1-539">Обновлен командлет New-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-539">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="ad5c1-540">Обновлен командлет Set-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-540">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="ad5c1-541">В пиринг ExpressRoute добавлено поле только для чтения PeeredConnections.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-541">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="ad5c1-542">В ExpressRoute добавлено поле только для чтения GlobalReachEnabled.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-542">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="ad5c1-543">Добавлен атрибут в рамках критического изменения, отменяющего статус устаревшего поля AllowGlobalReach в модели ExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-543">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="ad5c1-544">Исправлена проблема, связанная с ошибкой 8756, при использовании TargetListenerID с командлетами AzApplicationGatewayRedirectConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-544">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="ad5c1-545">Исправлена ошибка в New-AzApplicationGatewayPathRuleConfig, не позволявшая задавать набор правил повторного создания.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-545">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="ad5c1-546">Исправлено отображение VirtualNetworkTaps в NetworkInterfaceIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-546">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="ad5c1-547">Исправлены командлеты Cortex Get для отображения всех частей.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-547">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="ad5c1-548">Исправлено создание ссылок VirtualHub для ExpressRouteGateways и VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-548">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="ad5c1-549">В AzureFirewall и NatGateway добавлена поддержка Зон доступности.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-549">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="ad5c1-550">Добавлен командлет Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-550">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="ad5c1-551">Добавлена поддержка нескольких общедоступных IP-адресов для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-551">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="ad5c1-552">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="ad5c1-552">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="ad5c1-553">Добавлен параметр -PublicIpAddress, который принимает один или несколько объектов общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-553">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="ad5c1-554">Добавлен параметр -VirtualNetwork, который принимает объект виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-554">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="ad5c1-555">Добавлены методы AddPublicIpAddress и RemovePublicIpAddress для объекта брандмауэра. Они принимают объект общедоступного IP-адреса в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-555">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="ad5c1-556">Не рекомендуется использовать параметры -PublicIpName и -VirtualNetworkName.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-556">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="ad5c1-557">Обновлены следующие команды для функции: В параметрах проверки подлинности AAD VPN-клиента задан ресурс шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-557">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="ad5c1-558">Обновлен командлет New-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-558">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="ad5c1-559">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-559">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="ad5c1-560">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр-переключатель RemoveAadAuthentication для удаления в шлюзе параметров проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-560">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ad5c1-561">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ad5c1-561">Az.OperationalInsights</span></span>
* <span data-ttu-id="ad5c1-562">Добавлена поддержка SKU **pergb2018** в команде New-AzureRmOperationalInsightsWorkspace.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-562">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad5c1-563">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad5c1-563">Az.Resources</span></span>
* <span data-ttu-id="ad5c1-564">Поддержка дополнительных вариантов экспорта шаблона.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-564">Support for additional Template Export options</span></span>
    - <span data-ttu-id="ad5c1-565">В Export-AzResourceGroup добавлен параметр -SkipResourceNameParameterization.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-565">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="ad5c1-566">В Export-AzResourceGroup добавлен параметр -SkipAllParameterization.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-566">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="ad5c1-567">В Export-AzResourceGroup добавлен параметр -Resource для фильтрации экспортированных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-567">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ad5c1-568">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ad5c1-568">Az.ServiceFabric</span></span>
* <span data-ttu-id="ad5c1-569">Исправлена ошибка, связанная с получением иногда неправильных отпечатков при добавлении сертификата ByExistingKeyVault.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-569">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad5c1-570">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad5c1-570">Az.Sql</span></span>
* <span data-ttu-id="ad5c1-571">Исправлен суффикс конечной точки хранилища службы "Расширенная защита от угроз Azure".</span><span class="sxs-lookup"><span data-stu-id="ad5c1-571">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="ad5c1-572">Исправлена ошибка, связанная с возможностью пакета "Расширенная защита данных" переопределять политику службы "Расширенная защита от угроз".</span><span class="sxs-lookup"><span data-stu-id="ad5c1-572">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="ad5c1-573">Новые командлеты для Management.Sql позволяют клиентам добавлять ключи TDE и задавать средство защиты TDE для управляемых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-573">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="ad5c1-574">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ad5c1-574">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="ad5c1-575">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ad5c1-575">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="ad5c1-576">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ad5c1-576">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="ad5c1-577">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="ad5c1-577">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="ad5c1-578">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="ad5c1-578">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ad5c1-579">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ad5c1-579">Az.Storage</span></span>
* <span data-ttu-id="ad5c1-580">Поддержка класса Kind в FileStorage и значения Premium_ZRS в SkuName при создании учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-580">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="ad5c1-581">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ad5c1-581">New-AzStorageAccount</span></span>
* <span data-ttu-id="ad5c1-582">Уточнено описание командлета неизменности BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-582">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="ad5c1-583">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ad5c1-583">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ad5c1-584">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ad5c1-584">Az.Websites</span></span>
* <span data-ttu-id="ad5c1-585">Оптимизирует Get-AzWebAppCertificate для фильтрации по группе ресурсов на сервере, а не в клиенте.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-585">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="ad5c1-586">Добавляет параметр-переключатель - UseDisasterRecovery в Get AzWebAppSnapshot.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-586">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="ad5c1-587">2.2.0 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-587">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="ad5c1-588">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ad5c1-588">Az.Cdn</span></span>
* <span data-ttu-id="ad5c1-589">Обновлены командлеты для поддержки функции rulesEngine на основе API версии 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-589">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad5c1-590">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad5c1-590">Az.Compute</span></span>
* <span data-ttu-id="ad5c1-591">Добавлен параметр `NoWait`, который запускает операцию и немедленно возвращает значение еще до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-591">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="ad5c1-592">Обновлены командлеты:   Export-AzLogAnalyticRequestRateByInterval; Export-AzLogAnalyticThrottledRequest; Remove-AzVM; Remove-AzVMAccessExtension; Remove-AzVMAEMExtension; Remove-AzVMChefExtension; Remove-AzVMCustomScriptExtension; Remove-AzVMDiagnosticsExtension; Remove-AzVMDiskEncryptionExtension; Remove-AzVMDscExtension; Remove-AzVMSqlServerExtension; Restart-AzVM; Set-AzVM; Set-AzVMAccessExtension; Set-AzVMADDomainExtension; Set-AzVMAEMExtension; Set-AzVMBginfoExtension; Set-AzVMChefExtension; Set-AzVMCustomScriptExtension; Set-AzVMDiagnosticsExtension; Set-AzVMDscExtension; Set-AzVMExtension; Start-AzVM; Stop-AzVM; Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-592">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ad5c1-593">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ad5c1-593">Az.EventHub</span></span>
* <span data-ttu-id="ad5c1-594">Исправлена ошибка № 9231. Командлет Get-AzEventHubNamespace не возвращал теги.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-594">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="ad5c1-595">Исправлена ошибка № 9230. Командлет Get-AzEventHubNamespace возвращал значение ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-595">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ad5c1-596">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad5c1-596">Az.Network</span></span>
* <span data-ttu-id="ad5c1-597">Обновлены параметры ResourceId и InputObject для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-597">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="ad5c1-598">Добавлены псевдонимы для параметров ResourceId и InputObject.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-598">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ad5c1-599">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ad5c1-599">Az.PolicyInsights</span></span>
* <span data-ttu-id="ad5c1-600">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyEvent.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-600">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ad5c1-601">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ad5c1-601">Az.RecoveryServices</span></span>
* <span data-ttu-id="ad5c1-602">Минимальный срок хранения политики IaaSVM изменился с 1 до 7 дней.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-602">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ad5c1-603">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ad5c1-603">Az.ServiceBus</span></span>
* <span data-ttu-id="ad5c1-604">Исправлена ошибка № 9182. Командлет Get-AzServiceBusNamespace возвращал ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-604">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ad5c1-605">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ad5c1-605">Az.ServiceFabric</span></span>
* <span data-ttu-id="ad5c1-606">Исправлена опечатка в сообщении об ошибке для командлета Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-606">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="ad5c1-607">Исправлен отсутствующей символ в командных строках Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-607">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad5c1-608">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad5c1-608">Az.Sql</span></span>
* <span data-ttu-id="ad5c1-609">Для командлета New-AzureSqlInstance добавлен параметр DnsZonePartner, обеспечивающий поддержку AutoDr для Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-609">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="ad5c1-610">Командлет Get-AzSqlDatabaseSecureConnectionPolicy объявлен неподдерживаемым.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-610">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="ad5c1-611">Командлеты обнаружения угроз переименованы в командлеты Расширенной защиты от угроз.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-611">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="ad5c1-612">Параметры -StorageSizeInGB и -LicenseType командлета New-AzSqlInstance теперь необязательны.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-612">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ad5c1-613">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ad5c1-613">Az.Websites</span></span>
* <span data-ttu-id="ad5c1-614">Исправлены проблемы, когда удалялись теги при использовании Set-AzWebApp и Set-AzWebAppSlot со свойством -WebApp.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-614">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="ad5c1-615">2.1.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-615">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="ad5c1-616">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ad5c1-616">Az.ApiManagement</span></span>
* <span data-ttu-id="ad5c1-617">Созданы командлеты для управления диагностикой в глобальной области и в области API.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-617">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="ad5c1-618">**Get-AzApiManagementDiagnostic** — получение диагностики, заданной глобально или на уровне области API.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-618">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="ad5c1-619">**New-AzApiManagementDiagnostic** — создание диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-619">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="ad5c1-620">**New-AzApiManagementHttpMessageDiagnostic** — создание параметра диагностики, для которого регистрируются заголовки и размер байтов тела.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-620">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="ad5c1-621">**New-AzApiManagementPipelineDiagnosticSetting** — создание параметров диагностики для сообщений HTTP, поступающих в шлюз или исходящих из него.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-621">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="ad5c1-622">**New-AzApiManagementSamplingSetting** — создание параметра выборки для запросов и ответов касательно диагностики.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-622">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="ad5c1-623">**Remove-AzApiManagementDiagnostic** — удаление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-623">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="ad5c1-624">**Set-AzApiManagementDiagnostic** — обновление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-624">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="ad5c1-625">Созданы командлеты для управления кэшем в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-625">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="ad5c1-626">**Get-AzApiManagementCache** — получение сведений о кэше, указанном идентификатором, или обо всех кэшах.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-626">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="ad5c1-627">**New-AzApiManagementCache** — создание кэша по умолчанию или кэша в определенном регионе Azure.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-627">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="ad5c1-628">**Remove-AzApiManagementCache** — удаление кэша.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-628">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="ad5c1-629">**Update-AzApiManagementCache** — обновление кэша.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-629">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="ad5c1-630">Созданы командлеты для управления схемой API.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-630">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="ad5c1-631">**New-AzApiManagementSchema** — создание схемы для API.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-631">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="ad5c1-632">**Get-AzApiManagementSchema** — получение схем, настроенных в API.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-632">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="ad5c1-633">**Remove-AzApiManagementSchema** — удаление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-633">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="ad5c1-634">**Set-AzApiManagementSchema** — обновление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-634">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="ad5c1-635">Создан командлет для создания токена пользователя.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-635">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="ad5c1-636">**New-AzApiManagementUserToken** — создание токена пользователя, по умолчанию действительного в течение 8 часов. С помощью этого командлета можно создавать токен для пользователя GIT.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-636">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="ad5c1-637">Создан командлет для получения состояния сети.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-637">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="ad5c1-638">**Get-AzApiManagementNetworkStatus** — получение состояния сети ресурсов, от которых зависит служба "Управление API".</span><span class="sxs-lookup"><span data-stu-id="ad5c1-638">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="ad5c1-639">Это полезно при развертывании службы ApiManagement в виртуальной сети и проверке того, не нарушена ли какая-либо из зависимостей.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-639">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="ad5c1-640">Обновлен командлет **New-AzApiManagement** для управления службой ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-640">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="ad5c1-641">Добавлена поддержка нового SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-641">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="ad5c1-642">Добавлена поддержка для включения флага EnableClientCertificate в SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-642">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="ad5c1-643">Новый командлет **New-AzApiManagementSslSetting** позволяет настраивать параметр TLS/SSL для сервера (Backend) и внешнего интерфейса (Frontend).</span><span class="sxs-lookup"><span data-stu-id="ad5c1-643">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="ad5c1-644">Его также можно использовать для настройки Ciphers как 3DES, в ServerProtocols как Http2 для внешнего интерфейса (Frontend) службы ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-644">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="ad5c1-645">Добавлена поддержка настройки имени узла DeveloperPortal в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-645">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="ad5c1-646">Обновлен командлет **Get-AzApiManagementSsoToken** для извлечения объекта PsApiManagement в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-646">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="ad5c1-647">Обновлен командлет для отображения встроенных сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-647">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="ad5c1-648">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Код ошибки: ValidationError. Сообщение об ошибке: "Некоторые поля содержат неправильные значения". Сведения об ошибке: [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="ad5c1-648">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="ad5c1-649">Обновлен командлет **Export-AzApiManagementApi** для экспортирования программных интерфейсов в формате OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-649">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="ad5c1-650">Обновлен командлет **Import-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="ad5c1-650">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="ad5c1-651">Для импортирования API из спецификации документа OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-651">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="ad5c1-652">Для переопределения свойства PsApiManagementSchema, указанного в любом документе (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="ad5c1-652">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="ad5c1-653">Для переопределения свойства ServiceUrl, указанного в любом документе.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-653">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="ad5c1-654">Обновлен командлет **Get-AzApiManagementPolicy** для возврата политики в формате, экранированном не для XML, с использованием rawxml.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-654">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="ad5c1-655">Обновлен командлет **Set-AzApiManagementPolicy**. Он принимает политику в формате, экранированном не для XML, с использованием rawxml и в формате, экранированном для XML, с использованием XML.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-655">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="ad5c1-656">Обновлен командлет **New-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="ad5c1-656">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="ad5c1-657">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-657">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="ad5c1-658">Для создания API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-658">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="ad5c1-659">Для клонирования API с использованием значений SourceApiId и SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-659">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="ad5c1-660">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-660">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="ad5c1-661">Обновлен командлет **Set-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="ad5c1-661">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="ad5c1-662">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-662">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="ad5c1-663">Для обновления API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-663">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="ad5c1-664">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-664">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="ad5c1-665">Обновлен командлет **New-AzApiManagementRevision**:</span><span class="sxs-lookup"><span data-stu-id="ad5c1-665">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="ad5c1-666">Для клонирования (копирования тегов, продуктов, операций и политик) существующей редакции с использованием SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-666">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="ad5c1-667">Новая редакция предполагает родительский идентификатор ApiId.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-667">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="ad5c1-668">Для предоставления ApiRevisionDescription.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-668">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="ad5c1-669">Для переопределения значения ServiceUrl при клонировании API.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-669">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="ad5c1-670">Обновлен командлет **New-AzApiManagementIdentityProvider**:</span><span class="sxs-lookup"><span data-stu-id="ad5c1-670">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="ad5c1-671">Для настройки AAD или AADB2C с Authority.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-671">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="ad5c1-672">Для установки политик SignupPolicy, SigninPolicy, ProfileEditingPolicy и PasswordResetPolicy.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-672">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="ad5c1-673">Обновлен командлет **New-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-673">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="ad5c1-674">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-674">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="ad5c1-675">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-675">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="ad5c1-676">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-676">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="ad5c1-677">Обновлен командлет **Set-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-677">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="ad5c1-678">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-678">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="ad5c1-679">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-679">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="ad5c1-680">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-680">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="ad5c1-681">Следующие командлеты обновлены, чтобы принимать значение ResourceId в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-681">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="ad5c1-682">New-AzApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-682">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="ad5c1-683">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="ad5c1-683">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="ad5c1-684">Get-AzApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-684">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="ad5c1-685">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="ad5c1-685">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="ad5c1-686">Get-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-686">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="ad5c1-687">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="ad5c1-687">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="ad5c1-688">Get-AzApiManagementAuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-688">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="ad5c1-689">Get-AzApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-689">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="ad5c1-690">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="ad5c1-690">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="ad5c1-691">Get-AzApiManagementCertificate.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-691">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="ad5c1-692">Remove-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-692">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="ad5c1-693">Remove-AzApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-693">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ad5c1-694">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ad5c1-694">Az.Automation</span></span>
* <span data-ttu-id="ad5c1-695">Обновлен командлет Get-AzAutomationJobOutputRecord для обработки значений в формате JSON и в виде текстовой записи.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-695">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="ad5c1-696">исправлена проблема https://github.com/Azure/azure-powershell/issues/7977.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-696">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="ad5c1-697">исправлена проблема https://github.com/Azure/azure-powershell/issues/8600.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-697">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="ad5c1-698">Поведение командлета Start-AzAutomationDscCompilationJob изменено так, чтобы сразу же запустить задание, а не ждать его завершения.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-698">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="ad5c1-699">исправлена проблема https://github.com/Azure/azure-powershell/issues/8347.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-699">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="ad5c1-700">Исправлен командлет Get-AzAutomationDscNode, возвращающий все узлы при использовании -Name.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-700">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="ad5c1-701">Теперь он возвращает только соответствующий узел.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-701">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad5c1-702">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad5c1-702">Az.Compute</span></span>
* <span data-ttu-id="ad5c1-703">Добавлены параметры ProtectFromScaleIn и ProtectFromScaleSetAction для командлета Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-703">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="ad5c1-704">Командлет New-AzVM с простым набором параметров теперь по умолчанию использует доступное расположение, если регион "восточная часть США" не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-704">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ad5c1-705">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ad5c1-705">Az.DataLakeStore</span></span>
* <span data-ttu-id="ad5c1-706">Обновлен пакет SDK ADLS для использования httpclient. В инфраструктуру Azure интегрирована проверка плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-706">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ad5c1-707">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ad5c1-707">Az.Monitor</span></span>
* <span data-ttu-id="ad5c1-708">Исправлены неправильные имена параметров в справочных примерах.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-708">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ad5c1-709">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad5c1-709">Az.Network</span></span>
* <span data-ttu-id="ad5c1-710">Добавлен флаг DisableBgpRoutePropagation для выходных данных действующей таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-710">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="ad5c1-711">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="ad5c1-711">Updated cmdlet:</span></span>
        - <span data-ttu-id="ad5c1-712">Get-AzEffectiveRouteTable.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-712">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="ad5c1-713">Исправлен двойной дефис в документации New-AzApplicationGatewayTrustedRootCertificate.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-713">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad5c1-714">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad5c1-714">Az.Resources</span></span>
* <span data-ttu-id="ad5c1-715">Добавлен новый командлет Get-AzureRmDenyAssignment для получения запрещающих назначений.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-715">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad5c1-716">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad5c1-716">Az.Sql</span></span>
* <span data-ttu-id="ad5c1-717">Командлеты Расширенной защиты от угроз переименованы на командлеты Расширенной защиты данных, и оценка уязвимости включена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-717">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="ad5c1-718">2.0.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-718">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ad5c1-719">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ad5c1-719">Az.Accounts</span></span>
* <span data-ttu-id="ad5c1-720">Обновлена библиотека аутентификации для устранения проблем с ADFS при использовании аутентификации на основе имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-720">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ad5c1-721">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ad5c1-721">Az.CognitiveServices</span></span>
* <span data-ttu-id="ad5c1-722">Отображается только заявление об отказе Bing для служб Поиска Bing.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-722">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="ad5c1-723">Исправлена проблема с созданием учетной записи.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-723">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad5c1-724">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad5c1-724">Az.Compute</span></span>
* <span data-ttu-id="ad5c1-725">Функция группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-725">Proximity placement group feature.</span></span>
    - <span data-ttu-id="ad5c1-726">Добавлены следующие новые командлеты:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="ad5c1-726">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="ad5c1-727">Новый параметр ProximityPlacementGroupId будет добавлен в следующие командлеты:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="ad5c1-727">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="ad5c1-728">В командлет New-AzGalleryImageVersion добавлен параметр StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-728">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="ad5c1-729">TargetRegion в командлете New-AzGalleryImageVersion может содержать StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-729">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="ad5c1-730">Параметр-переключатель SkipShutdown добавлен в командлеты Stop-AzVM и Stop-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-730">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="ad5c1-731">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="ad5c1-731">Breaking changes</span></span>
    - <span data-ttu-id="ad5c1-732">Командлет SET-AzVMBootDiagnostics изменен на Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-732">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="ad5c1-733">Командлет Export-AzLogAnalyticThrottledRequests изменен на Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-733">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="ad5c1-734">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="ad5c1-734">Az.DeploymentManager</span></span>
* <span data-ttu-id="ad5c1-735">Первая общедоступная версия командлетов диспетчера развертывания Azure</span><span class="sxs-lookup"><span data-stu-id="ad5c1-735">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="ad5c1-736">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="ad5c1-736">Az.Dns</span></span>
* <span data-ttu-id="ad5c1-737">Автоматическое делегирование DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="ad5c1-737">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="ad5c1-738">Командлет для создания зоны DNS принимает имя родительской зоны в качестве дополнительного необязательного параметра.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-738">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="ad5c1-739">Он добавляет записи NS в родительской зоне для созданной дочерней зоны.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-739">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="ad5c1-740">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ad5c1-740">Az.FrontDoor</span></span>
* <span data-ttu-id="ad5c1-741">Первая общедоступная версия командлетов Azure FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-741">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="ad5c1-742">Переименованы командлеты WAF для включения Waf.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-742">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="ad5c1-743">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ad5c1-743">Az.HDInsight</span></span>
* <span data-ttu-id="ad5c1-744">Удалены два командлета:</span><span class="sxs-lookup"><span data-stu-id="ad5c1-744">Removed two cmdlets:</span></span>
    - <span data-ttu-id="ad5c1-745">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="ad5c1-745">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="ad5c1-746">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="ad5c1-746">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="ad5c1-747">Добавлен новый командлет Set-AzHDInsightGatewayCredential для замены Grant-AzHDInsightHttpServicesAccess.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-747">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="ad5c1-748">Обновлен командлет Get-AzHDInsightJobOutput для различения ролей читателя и оператора HDInsight:</span><span class="sxs-lookup"><span data-stu-id="ad5c1-748">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="ad5c1-749">Пользователям с ролью читателя не нужно указывать параметр DefaultStorageAccountKey явным образом, иначе возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-749">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="ad5c1-750">На пользователей с ролью оператора HDInsight это не повлияет.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-750">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ad5c1-751">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ad5c1-751">Az.Monitor</span></span>
* <span data-ttu-id="ad5c1-752">Новые командлеты для API SQR (запланированное правило запросов)</span><span class="sxs-lookup"><span data-stu-id="ad5c1-752">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="ad5c1-753">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="ad5c1-753">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="ad5c1-754">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="ad5c1-754">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="ad5c1-755">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="ad5c1-755">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="ad5c1-756">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="ad5c1-756">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="ad5c1-757">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="ad5c1-757">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="ad5c1-758">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="ad5c1-758">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="ad5c1-759">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ad5c1-759">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ad5c1-760">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ad5c1-760">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ad5c1-761">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ad5c1-761">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ad5c1-762">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ad5c1-762">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ad5c1-763">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ad5c1-763">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ad5c1-764">См. подробнее об [API SQR](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules).</span><span class="sxs-lookup"><span data-stu-id="ad5c1-764">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="ad5c1-765">Обновлен файл Az.Monitor.md для включения командлетов для правила генерации оповещений на основе метрик GenV2(не классическая версия).</span><span class="sxs-lookup"><span data-stu-id="ad5c1-765">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ad5c1-766">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad5c1-766">Az.Network</span></span>
* <span data-ttu-id="ad5c1-767">Добавлена поддержка для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-767">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="ad5c1-768">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="ad5c1-768">New cmdlets</span></span>
        - <span data-ttu-id="ad5c1-769">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ad5c1-769">New-AzNatGateway</span></span>
        - <span data-ttu-id="ad5c1-770">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ad5c1-770">Get-AzNatGateway</span></span>
        - <span data-ttu-id="ad5c1-771">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ad5c1-771">Set-AzNatGateway</span></span>
        - <span data-ttu-id="ad5c1-772">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ad5c1-772">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="ad5c1-773">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="ad5c1-773">Updated cmdlets</span></span>
        - <span data-ttu-id="ad5c1-774">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="ad5c1-774">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="ad5c1-775">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="ad5c1-775">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="ad5c1-776">Обновлены следующие команды для функции: Настройка и удаление пользовательских маршрутов через шлюз в Бруклине.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-776">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="ad5c1-777">Обновлен командлет New-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-777">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="ad5c1-778">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-778">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ad5c1-779">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ad5c1-779">Az.PolicyInsights</span></span>
* <span data-ttu-id="ad5c1-780">Добавлена поддержка сведений об оценке политики запросов.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-780">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="ad5c1-781">Добавлен параметр -Expand в командлет Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-781">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="ad5c1-782">Добавлена поддержка -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-782">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ad5c1-783">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ad5c1-783">Az.RecoveryServices</span></span>
* <span data-ttu-id="ad5c1-784">Добавлена поддержка перекрестной подписки на Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-784">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="ad5c1-785">Добавлена возможность отмечать предстоящие критически важные изменения для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-785">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="ad5c1-786">Исправлены план восстановления и план действий для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-786">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="ad5c1-787">Исправлено сетевое сопоставление обновления Azure Site Recovery (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="ad5c1-787">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="ad5c1-788">Исправлено направление защиты обновления Azure Site Recovery для управляемых дисков (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="ad5c1-788">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="ad5c1-789">Добавлены другие незначительные исправления.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-789">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="ad5c1-790">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="ad5c1-790">Az.Relay</span></span>
* <span data-ttu-id="ad5c1-791">Исправлены опечатки в сообщениях для клиентов.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-791">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ad5c1-792">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ad5c1-792">Az.ServiceBus</span></span>
* <span data-ttu-id="ad5c1-793">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-793">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ad5c1-794">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ad5c1-794">Az.Storage</span></span>
* <span data-ttu-id="ad5c1-795">Выполнено обновление клиентской библиотеки хранилища до версии 10.0.1 (пространство имен всех объектов из этого пакета SDK изменено с Microsoft.WindowsAzure.Storage. *на Microsoft.Azure.Storage*).</span><span class="sxs-lookup"><span data-stu-id="ad5c1-795">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="ad5c1-796">Выполнено обновление до Microsoft.Azure.Management.Storage версии 11.0.0 для включения поддержки нового API версии 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-796">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="ad5c1-797">Значение свойства Kind по умолчанию в учетной записи хранения изменено со Storage на StorageV2.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-797">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="ad5c1-798">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ad5c1-798">New-AzStorageAccount</span></span>
* <span data-ttu-id="ad5c1-799">Изменено значение Sku.Name в выходных данных командлета учетной записи хранения в соответствии со значением Sku.Name во входных данных путем добавления _ (например, StandardLRS изменено на Standard_LRS).</span><span class="sxs-lookup"><span data-stu-id="ad5c1-799">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="ad5c1-800">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ad5c1-800">New-AzStorageAccount</span></span>
    - <span data-ttu-id="ad5c1-801">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ad5c1-801">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="ad5c1-802">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ad5c1-802">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ad5c1-803">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ad5c1-803">Az.Websites</span></span>
* <span data-ttu-id="ad5c1-804">Свойство Kind теперь будет задаваться объектам PSSite, возвращаемым командлетом Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-804">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="ad5c1-805">Get-AzWebApp\*Metrics и Get-AzAppServicePlanMetrics считаются нерекомендуемыми.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-805">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="ad5c1-806">1.8.0 — апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-806">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ad5c1-807">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="ad5c1-807">Highlights since the last major release</span></span>
* <span data-ttu-id="ad5c1-808">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-808">General availability of `Az` module</span></span>
* <span data-ttu-id="ad5c1-809">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="ad5c1-809">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="ad5c1-810">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="ad5c1-810">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="ad5c1-811">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-811">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="ad5c1-812">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-812">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ad5c1-813">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-813">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="ad5c1-814">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="ad5c1-814">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ad5c1-815">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ad5c1-815">Az.Accounts</span></span>
* <span data-ttu-id="ad5c1-816">Обновлен командлет Uninstall-AzureRm для правильного удаления модулей в Mac.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-816">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="ad5c1-817">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ad5c1-817">Az.Batch</span></span>
* <span data-ttu-id="ad5c1-818">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-818">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ad5c1-819">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ad5c1-819">Az.Cdn</span></span>
* <span data-ttu-id="ad5c1-820">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-820">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ad5c1-821">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ad5c1-821">Az.CognitiveServices</span></span>
* <span data-ttu-id="ad5c1-822">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-822">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad5c1-823">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad5c1-823">Az.Compute</span></span>
* <span data-ttu-id="ad5c1-824">Устранена проблема с установкой AEM, если в идентификаторах ресурсов дисков группа ресурсов указана в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-824">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="ad5c1-825">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-825">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ad5c1-826">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-826">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ad5c1-827">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ad5c1-827">Az.DataFactory</span></span>
* <span data-ttu-id="ad5c1-828">Добавлены свойства SsisProperties, если NodeCount не имеет значения NULL для управляемой среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-828">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ad5c1-829">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ad5c1-829">Az.DataLakeStore</span></span>
* <span data-ttu-id="ad5c1-830">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-830">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ad5c1-831">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ad5c1-831">Az.EventGrid</span></span>
* <span data-ttu-id="ad5c1-832">Обновлен текст справки для конечной точки, указывающий, что необходимо создать ресурсы, прежде чем использовать командлеты для создания или обновления подписки на события.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-832">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ad5c1-833">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ad5c1-833">Az.EventHub</span></span>
* <span data-ttu-id="ad5c1-834">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-834">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="ad5c1-835">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ad5c1-835">Az.HDInsight</span></span>
* <span data-ttu-id="ad5c1-836">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-836">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ad5c1-837">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ad5c1-837">Az.IotHub</span></span>
* <span data-ttu-id="ad5c1-838">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-838">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ad5c1-839">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ad5c1-839">Az.KeyVault</span></span>
* <span data-ttu-id="ad5c1-840">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-840">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ad5c1-841">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-841">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="ad5c1-842">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="ad5c1-842">Az.MachineLearning</span></span>
* <span data-ttu-id="ad5c1-843">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-843">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="ad5c1-844">Az.Media</span><span class="sxs-lookup"><span data-stu-id="ad5c1-844">Az.Media</span></span>
* <span data-ttu-id="ad5c1-845">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-845">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ad5c1-846">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ad5c1-846">Az.Monitor</span></span>
  * <span data-ttu-id="ad5c1-847">Добавлены новые командлеты для правила генерации оповещений на основе метрик GenV2 (не классических).</span><span class="sxs-lookup"><span data-stu-id="ad5c1-847">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="ad5c1-848">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="ad5c1-848">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="ad5c1-849">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="ad5c1-849">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="ad5c1-850">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="ad5c1-850">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="ad5c1-851">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="ad5c1-851">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="ad5c1-852">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="ad5c1-852">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="ad5c1-853">Обновлен пакет SDK Monitor до предварительной версии 0.22.0.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-853">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ad5c1-854">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad5c1-854">Az.Network</span></span>
* <span data-ttu-id="ad5c1-855">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-855">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ad5c1-856">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-856">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="ad5c1-857">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="ad5c1-857">Az.NotificationHubs</span></span>
* <span data-ttu-id="ad5c1-858">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-858">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ad5c1-859">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ad5c1-859">Az.OperationalInsights</span></span>
* <span data-ttu-id="ad5c1-860">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-860">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="ad5c1-861">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="ad5c1-861">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="ad5c1-862">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-862">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ad5c1-863">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ad5c1-863">Az.RecoveryServices</span></span>
* <span data-ttu-id="ad5c1-864">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-864">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ad5c1-865">Обновлен табличный формат для SQL на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-865">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="ad5c1-866">Добавлен альтернативный метод для получения расположения в Общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-866">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="ad5c1-867">Обновлено значение ScheduleRunDays в объекте SchedulePolicy в соответствии с часовым поясом.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-867">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="ad5c1-868">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ad5c1-868">Az.RedisCache</span></span>
* <span data-ttu-id="ad5c1-869">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-869">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad5c1-870">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad5c1-870">Az.Resources</span></span>
* <span data-ttu-id="ad5c1-871">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-871">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad5c1-872">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad5c1-872">Az.Sql</span></span>
* <span data-ttu-id="ad5c1-873">Заменена зависимость от пакета SDK монитора на обычный код.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-873">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="ad5c1-874">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-874">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ad5c1-875">Улучшен процесс классификации нескольких столбцов.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-875">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="ad5c1-876">Добавлены свойства SKU (имя, семейство, производительность SKU) в отклике Get-AzSqlServerServiceObjective, а также по умолчанию задан табличный формат.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-876">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="ad5c1-877">C помощью Get-AzSqlServerServiceObjective теперь можно получать список доступных целевых служб по расположению без необходимости заранее размещать сервер в регионе.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-877">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="ad5c1-878">Поддерживается параметр часового пояса при создании Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-878">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="ad5c1-879">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-879">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ad5c1-880">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ad5c1-880">Az.Websites</span></span>
* <span data-ttu-id="ad5c1-881">Исправлены командлеты Set-AzWebApp и Set-AzWebAppSlot, которые теперь не удаляют теги при выполнении.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-881">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="ad5c1-882">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-882">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ad5c1-883">Обновлен пакет SDK веб-узлов.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-883">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="ad5c1-884">Удалено свойство AdminSiteName из PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-884">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="ad5c1-885">1.7.0 —апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-885">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ad5c1-886">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="ad5c1-886">Highlights since the last major release</span></span>
* <span data-ttu-id="ad5c1-887">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-887">General availability of `Az` module</span></span>
* <span data-ttu-id="ad5c1-888">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="ad5c1-888">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="ad5c1-889">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="ad5c1-889">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="ad5c1-890">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-890">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="ad5c1-891">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-891">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ad5c1-892">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-892">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="ad5c1-893">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="ad5c1-893">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ad5c1-894">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ad5c1-894">Az.Accounts</span></span>
* <span data-ttu-id="ad5c1-895">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметр AzureAnalysisServicesEndpointResourceId.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-895">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="ad5c1-896">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ad5c1-896">Az.AnalysisServices</span></span>
* <span data-ttu-id="ad5c1-897">Использование ServiceClient в командлетах плоскости данных и удаление исходной логики проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-897">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="ad5c1-898">Add-AzureASAccount используется как оболочка для Connect-AzAccount во избежание критических изменений.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-898">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ad5c1-899">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ad5c1-899">Az.Automation</span></span>
* <span data-ttu-id="ad5c1-900">Исправлена ошибка командлета New-AzAutomationSoftwareUpdateConfiguration, связанная с включением.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-900">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="ad5c1-901">Теперь параметры IncludedKbNumber и IncludedPackageNameMask должны работать нормально.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-901">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="ad5c1-902">Исправлена ошибка динамической группы управления обновлениями службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-902">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad5c1-903">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad5c1-903">Az.Compute</span></span>
* <span data-ttu-id="ad5c1-904">В командлеты New-AzDiskConfig и New-AzSnapshotConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-904">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="ad5c1-905">Теперь можно создавать виртуальные машину на основе образов из коллекции от других клиентов.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-905">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="ad5c1-906">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ad5c1-906">Az.ContainerInstance</span></span>
* <span data-ttu-id="ad5c1-907">Исправлена проблема в параметре -Command командлета New-AzContainerGroup, из-за которой в конце добавлялся пустой аргумент.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-907">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ad5c1-908">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ad5c1-908">Az.DataFactory</span></span>
* <span data-ttu-id="ad5c1-909">Пакет SDK для ADF .NET обновлен до версии 3.0.2.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-909">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="ad5c1-910">Командлет Set-AzDataFactoryV2 обновлен с помощью дополнительных параметров для настроек, связанных с RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-910">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad5c1-911">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad5c1-911">Az.Resources</span></span>
* <span data-ttu-id="ad5c1-912">Улучшена обработка поставщиков Get-AzResource при предоставлении параметров -ResourceId или -ResourceGroupName, -Name и -ResourceType.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-912">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="ad5c1-913">Улучшена обработка ошибок в командлетах Test-AzDeployment и Test-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-913">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="ad5c1-914">Теперь ошибки, возникающие за пределами проверки развертывания, обрабатываются и включаются в выходные данные команды.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-914">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="ad5c1-915">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-915">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="ad5c1-916">Добавлен параметр-переключатель -IgnoreDynamicParameters, с помощью которого можно настроить командлеты развертывания так, чтобы они пропускали запросы в сценариях скриптов и заданий.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-916">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="ad5c1-917">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-917">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad5c1-918">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad5c1-918">Az.Sql</span></span>
* <span data-ttu-id="ad5c1-919">Поддержка классификации данных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-919">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ad5c1-920">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ad5c1-920">Az.Storage</span></span>
* <span data-ttu-id="ad5c1-921">Подробные сообщения об ошибке передаются при создании контекста хранилища с помощью параметра -UseConnectedAccount, но без входа в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-921">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="ad5c1-922">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="ad5c1-922">New-AzStorageContext</span></span>
* <span data-ttu-id="ad5c1-923">Поддержка свойств службы управления BLOB-объектов в указанной учетной записи хранения с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-923">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="ad5c1-924">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="ad5c1-924">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="ad5c1-925">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="ad5c1-925">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="ad5c1-926">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ad5c1-926">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="ad5c1-927">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ad5c1-927">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="ad5c1-928">Поддержка параметра -AsJob в командлетах для отправки и скачивания больших двоичных объектов и файлов.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-928">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="ad5c1-929">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ad5c1-929">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="ad5c1-930">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ad5c1-930">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="ad5c1-931">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ad5c1-931">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="ad5c1-932">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ad5c1-932">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="ad5c1-933">1.6.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-933">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ad5c1-934">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="ad5c1-934">Highlights since the last major release</span></span>
* <span data-ttu-id="ad5c1-935">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-935">General availability of `Az` module</span></span>
* <span data-ttu-id="ad5c1-936">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="ad5c1-936">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="ad5c1-937">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="ad5c1-937">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="ad5c1-938">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-938">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="ad5c1-939">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-939">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ad5c1-940">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-940">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="ad5c1-941">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="ad5c1-941">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ad5c1-942">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ad5c1-942">Az.Automation</span></span>
* <span data-ttu-id="ad5c1-943">В управление обновлениями службы автоматизации Azure внесены изменения для поддержки следующих новых функций:</span><span class="sxs-lookup"><span data-stu-id="ad5c1-943">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="ad5c1-944">динамическое группирование;</span><span class="sxs-lookup"><span data-stu-id="ad5c1-944">Dynamic grouping</span></span>
    * <span data-ttu-id="ad5c1-945">скрипты предварительного или последующего выполнения;</span><span class="sxs-lookup"><span data-stu-id="ad5c1-945">Pre-Post script</span></span>
    * <span data-ttu-id="ad5c1-946">параметр перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-946">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad5c1-947">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad5c1-947">Az.Compute</span></span>
* <span data-ttu-id="ad5c1-948">Устранена проблема, связанная с разрешением пути в Get-AzVmBootDiagnosticsData.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-948">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="ad5c1-949">Обновление клиентской библиотеки вычислений до версии 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-949">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ad5c1-950">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ad5c1-950">Az.KeyVault</span></span>
* <span data-ttu-id="ad5c1-951">Добавлена поддержка подстановочных знаков в командлетах KeyVault.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-951">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ad5c1-952">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad5c1-952">Az.Network</span></span>
* <span data-ttu-id="ad5c1-953">Добавлена поддержка анализа угроз для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-953">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="ad5c1-954">Добавлены настраиваемые правила и ресурс верхнего уровня для политики брандмауэра Шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-954">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ad5c1-955">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ad5c1-955">Az.RecoveryServices</span></span>
* <span data-ttu-id="ad5c1-956">В политику виртуальной машины Azure добавлен объект SnapshotRetentionInDays для поддержки мгновенного восстановления.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-956">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="ad5c1-957">Добавлена поддержка канала для отмены регистрации контейнера.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-957">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad5c1-958">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad5c1-958">Az.Resources</span></span>
* <span data-ttu-id="ad5c1-959">Обновлена поддержка подстановочных знаков для Get-AzResource и Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-959">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="ad5c1-960">Обновлены учетные данные, используемые при общих вызовах к ARM.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-960">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad5c1-961">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad5c1-961">Az.Sql</span></span>
* <span data-ttu-id="ad5c1-962">Изменен тип параметра (ExcludeDetectionType) командлетов для обнаружения угроз с DetectionTypes на string[] для поддержки актуального состояния при добавлении новых типов обнаружения и для поддержки автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-962">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ad5c1-963">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ad5c1-963">Az.Storage</span></span>
* <span data-ttu-id="ad5c1-964">Поддержка получения, настройки и удаления политики управления в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-964">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="ad5c1-965">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ad5c1-965">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="ad5c1-966">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ad5c1-966">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="ad5c1-967">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ad5c1-967">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="ad5c1-968">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="ad5c1-968">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="ad5c1-969">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="ad5c1-969">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="ad5c1-970">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="ad5c1-970">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ad5c1-971">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ad5c1-971">Az.Websites</span></span>
* <span data-ttu-id="ad5c1-972">Исправлена ошибка с шаблоном ARM, из-за которой прерывалось клонирование все слотов при использовании New-AzWebApp -IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-972">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="ad5c1-973">1.5.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-973">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ad5c1-974">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ad5c1-974">Az.Accounts</span></span>
* <span data-ttu-id="ad5c1-975">Добавлена команда Register-AzModule для поддержки созданных командлетов AutoRest.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-975">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="ad5c1-976">Обновлены примеры для Connect AzAccount.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-976">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ad5c1-977">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ad5c1-977">Az.Automation</span></span>
* <span data-ttu-id="ad5c1-978">Исправлена проблема с получением некоторых ежемесячных расписаний в нескольких командлетах службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-978">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="ad5c1-979">Исправлен командлет Get-AzAutomationDscNode, возвращающий только первые 20 узлов.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-979">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="ad5c1-980">Теперь он возвращает все узлы.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-980">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ad5c1-981">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ad5c1-981">Az.Cdn</span></span>
* <span data-ttu-id="ad5c1-982">Добавлены новые командлеты PowerShell для включения и отключения HTTPS для личного домена и отключены устаревшие командлеты.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-982">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad5c1-983">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad5c1-983">Az.Compute</span></span>
* <span data-ttu-id="ad5c1-984">Добавлена поддержка подстановочных знаков в командлетах Get.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-984">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ad5c1-985">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ad5c1-985">Az.DataFactory</span></span>
* <span data-ttu-id="ad5c1-986">Обновлен пакет SDK для ADF .NET до версии 3.0.1.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-986">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ad5c1-987">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ad5c1-987">Az.LogicApp</span></span>
* <span data-ttu-id="ad5c1-988">Исправлена проблема с получением только первой страницы результатов при выполнении команды ListWorkflows.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-988">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ad5c1-989">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad5c1-989">Az.Network</span></span>
* <span data-ttu-id="ad5c1-990">Добавлена поддержка подстановочных знаков в командлетах Network.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-990">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ad5c1-991">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ad5c1-991">Az.RecoveryServices</span></span>
* <span data-ttu-id="ad5c1-992">Добавлена поддержка SQL Server на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-992">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="ad5c1-993">Обновление пакета SDK</span><span class="sxs-lookup"><span data-stu-id="ad5c1-993">SDK Update</span></span>
* <span data-ttu-id="ad5c1-994">Удалена проверка VMappContainer в Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-994">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="ad5c1-995">Добавлены параметры Name и ServerName для Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-995">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad5c1-996">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad5c1-996">Az.Resources</span></span>
* <span data-ttu-id="ad5c1-997">Добавлен параметр `-TemplateObject` в командлеты для развертывания.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-997">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="ad5c1-998">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2933.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-998">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="ad5c1-999">Устранена проблема с передачей в конвейер результата `Get-AzResource` для `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-999">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="ad5c1-1000">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8240.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1000">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="ad5c1-1001">Устранена проблема с изменением типа данных JSON при выполнении `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1001">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="ad5c1-1002">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7930.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1002">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad5c1-1003">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1003">Az.Sql</span></span>
* <span data-ttu-id="ad5c1-1004">Обновление AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1004">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="ad5c1-1005">Исправлено поведение для пограничного случая при создании параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1005">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ad5c1-1006">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1006">Az.Storage</span></span>
* <span data-ttu-id="ad5c1-1007">Включена поддержка Kind BlockBlobStorage при создании учетной записи хранения для New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1007">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="ad5c1-1008">1.4.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1008">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="ad5c1-1009">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1009">Az.AnalysisServices</span></span>
* <span data-ttu-id="ad5c1-1010">Командлет AddAzureASAccount устарел.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1010">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ad5c1-1011">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1011">Az.Automation</span></span>
* <span data-ttu-id="ad5c1-1012">Обновлена справка для командлета Import-AzAutomationDscNodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1012">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="ad5c1-1013">Добавлена проверка имени конфигурации для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1013">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="ad5c1-1014">Улучшена обработка ошибок для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1014">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ad5c1-1015">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1015">Az.CognitiveServices</span></span>
* <span data-ttu-id="ad5c1-1016">Добавлен параметр CustomSubdomainName — новый необязательный параметр для командлета New-AzCognitiveServicesAccount, который указывает поддомен для ресурса.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1016">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad5c1-1017">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1017">Az.Compute</span></span>
* <span data-ttu-id="ad5c1-1018">Устранена проблема с идентификаторами наборов параметров.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1018">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="ad5c1-1019">Обновлен командлет Get-AzVMExtension для отображения списка всех установленных расширений, если не указан параметр Name.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1019">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="ad5c1-1020">Для командлета Update-AzImage добавлены параметры Tag и ResourceId.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1020">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="ad5c1-1021">Командлет Get-AzVmssVM, который выполняется без указания идентификатора экземпляра и с параметром InstanceView, может выводить виртуальные машины из VMSS с представлением экземпляра.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1021">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ad5c1-1022">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1022">Az.DataLakeStore</span></span>
* <span data-ttu-id="ad5c1-1023">Добавлены командлеты для перечисления и восстановления удаленного элемента ADL.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1023">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ad5c1-1024">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1024">Az.EventHub</span></span>
* <span data-ttu-id="ad5c1-1025">Добавлено новое логическое свойство SkipEmptyArchives для пропуска пустых архивов в классе CaptureDescription Eventhub.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1025">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="ad5c1-1026">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1026">Az.KeyVault</span></span>
* <span data-ttu-id="ad5c1-1027">Исправлена расстановка тегов для командлета Set-AzKeyVaultSecret.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1027">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ad5c1-1028">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1028">Az.LogicApp</span></span>
* <span data-ttu-id="ad5c1-1029">Добавлен SKU "Базовый" для учетных записей интеграции.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1029">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="ad5c1-1030">Добавлены типы сопоставлений Liquid, а также XSLT 2.0 и XSLT 3.0.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1030">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="ad5c1-1031">Новые командлеты для сборок учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1031">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="ad5c1-1032">Get-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1032">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="ad5c1-1033">New-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1033">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="ad5c1-1034">Remove-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1034">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="ad5c1-1035">Set-AzIntegrationAccountAssembly.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1035">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="ad5c1-1036">Новые командлеты для конфигурации пакета учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1036">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="ad5c1-1037">Get-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1037">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="ad5c1-1038">New-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1038">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="ad5c1-1039">Remove-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1039">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="ad5c1-1040">Set-AzIntegrationAccountBatchConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1040">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="ad5c1-1041">Обновлен пакет SDK Logic Apps до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1041">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ad5c1-1042">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1042">Az.Monitor</span></span>
* <span data-ttu-id="ad5c1-1043">Обновлена справка для командлета Get-AzMetric.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1043">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ad5c1-1044">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1044">Az.Network</span></span>
* <span data-ttu-id="ad5c1-1045">Обновлен пример справки для командлета Add-AzApplicationGatewayCustomError.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1045">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ad5c1-1046">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1046">Az.OperationalInsights</span></span>
* <span data-ttu-id="ad5c1-1047">Дополнительная поддержка создания и получения источников данных ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1047">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="ad5c1-1048">Добавлен новый тип ApplicationInsights для получения определенных или всех источников данных ApplicationInsights для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1048">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="ad5c1-1049">Добавлен командлет New-AzOperationalInsightsApplicationInsightsDataSource для создания источника данных с использованием параметров указанного ресурса Application-Insightss: subscription Id, resourceGroupName и name.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1049">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="ad5c1-1050">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1050">Az.Resources</span></span>
* <span data-ttu-id="ad5c1-1051">исправлена проблема https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1051">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="ad5c1-1052">исправлена проблема https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1052">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="ad5c1-1053">исправлена проблема https://github.com/Azure/azure-powershell/issues/6219.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1053">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="ad5c1-1054">Исправлена ошибка, препятствующая повторному созданию KeyCredentials.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1054">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad5c1-1055">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1055">Az.Sql</span></span>
* <span data-ttu-id="ad5c1-1056">Добавлена поддержка уровня гипермасштабирования в базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1056">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="ad5c1-1057">Исправлена ошибка, из-за которой восстановление могло завершиться со сбоем при указании ненужных свойств в запросе на восстановление.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1057">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ad5c1-1058">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1058">Az.Websites</span></span>
* <span data-ttu-id="ad5c1-1059">Исправлен пример для командлета Get-AzWebAppSlotMetrics.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1059">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="ad5c1-1060">1.3.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1060">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ad5c1-1061">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1061">Az.Accounts</span></span>
* <span data-ttu-id="ad5c1-1062">Обновление до последней версии ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1062">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="ad5c1-1063">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1063">Az.AnalysisServices</span></span>
<span data-ttu-id="ad5c1-1064">Общедоступная версия модуля Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1064">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad5c1-1065">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1065">Az.Compute</span></span>
* <span data-ttu-id="ad5c1-1066">Расширение AEM: добавлена поддержка дисков UltraSSD, P60, P70 и P80.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1066">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="ad5c1-1067">Обновлено описание справки для командлета Set-AzVMBootDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1067">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="ad5c1-1068">Обновлено описание справки и пример для командлета Update-AzImage.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1068">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ad5c1-1069">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1069">Az.RecoveryServices</span></span>
<span data-ttu-id="ad5c1-1070">Общедоступная версия модуля Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1070">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad5c1-1071">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1071">Az.Resources</span></span>
* <span data-ttu-id="ad5c1-1072">Исправлена расстановка тегов для групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1072">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="ad5c1-1073">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1073">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="ad5c1-1074">Исправлена проблема с игнорированием командлетом `Get-AzureRmRoleAssignment` параметра -ErrorAction.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1074">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="ad5c1-1075">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1075">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad5c1-1076">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1076">Az.Sql</span></span>
* <span data-ttu-id="ad5c1-1077">Добавлен командлет Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1077">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="ad5c1-1078">Исправлена проблема с появлением исключения NullRef при выполнении командлетов SQL, если не выполнен вход в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1078">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="ad5c1-1079">Исправлено исключение NullRef в командлете Get-AzSqlCapability.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1079">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="ad5c1-1080">1.2.1 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1080">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ad5c1-1081">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1081">Az.Accounts</span></span>
* <span data-ttu-id="ad5c1-1082">Выпуск с правильной версией службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1082">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="ad5c1-1083">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1083">Az.AnalysisServices</span></span>
* <span data-ttu-id="ad5c1-1084">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1084">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ad5c1-1085">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1085">Az.RecoveryServices</span></span>
* <span data-ttu-id="ad5c1-1086">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1086">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="ad5c1-1087">1.2.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1087">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ad5c1-1088">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1088">Az.Accounts</span></span>
* <span data-ttu-id="ad5c1-1089">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1089">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ad5c1-1090">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1090">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ad5c1-1091">Добавлено предупреждающее сообщение в PS Core для модуля Uninstall-AzureRm.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1091">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="ad5c1-1092">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1092">Az.Aks</span></span>
* <span data-ttu-id="ad5c1-1093">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1093">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ad5c1-1094">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1094">Az.Automation</span></span>
* <span data-ttu-id="ad5c1-1095">Добавлена поддержка для модулей runbook Python 2.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1095">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="ad5c1-1096">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1096">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ad5c1-1097">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1097">Az.Cdn</span></span>
* <span data-ttu-id="ad5c1-1098">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1098">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad5c1-1099">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1099">Az.Compute</span></span>
* <span data-ttu-id="ad5c1-1100">Добавлен командлет Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1100">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="ad5c1-1101">Добавлен параметр TempDisk к командлету Set-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1101">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="ad5c1-1102">Исправлено предупреждающее сообщение командлета New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1102">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="ad5c1-1103">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1103">Az.ContainerRegistry</span></span>
* <span data-ttu-id="ad5c1-1104">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1104">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ad5c1-1105">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1105">Az.DataFactory</span></span>
* <span data-ttu-id="ad5c1-1106">Пакет SDK ADF .Net обновлен до версии 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1106">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ad5c1-1107">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1107">Az.DataLakeStore</span></span>
* <span data-ttu-id="ad5c1-1108">Исправлена проблема с конечной точкой ADLS при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1108">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="ad5c1-1109">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7462.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1109">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="ad5c1-1110">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1110">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ad5c1-1111">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1111">Az.IotHub</span></span>
* <span data-ttu-id="ad5c1-1112">Добавлен формат кодирования для командлета Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1112">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ad5c1-1113">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1113">Az.KeyVault</span></span>
* <span data-ttu-id="ad5c1-1114">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1114">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ad5c1-1115">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1115">Az.Network</span></span>
* <span data-ttu-id="ad5c1-1116">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1116">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad5c1-1117">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1117">Az.Resources</span></span>
* <span data-ttu-id="ad5c1-1118">Исправлены неправильные примеры в справочной документации по командлетам New-AzADAppCredential и New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1118">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="ad5c1-1119">Исправлена проблема, при которой путь для параметра -TemplateFile не удавалось разрешить до выполнения командлетов развертывания групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1119">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="ad5c1-1120">Az.Resources: исправлена документация для значения по умолчанию -Mode командлета New-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1120">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="ad5c1-1121">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/7522.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1121">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="ad5c1-1122">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/5747.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1122">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="ad5c1-1123">Исправлена проблема с форматированием объекта PSResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1123">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="ad5c1-1124">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2123.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1124">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ad5c1-1125">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1125">Az.ServiceFabric</span></span>
* <span data-ttu-id="ad5c1-1126">Исправлена проблема с появлением исключения в процессе отката при добавлении сертификата к модели VMSS: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1126">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="ad5c1-1127">Исправлены некоторые сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1127">Fix some error messages.</span></span>
* <span data-ttu-id="ad5c1-1128">Исправлена проблема с созданием кластера с шаблоном ARM по умолчанию для командлета New-AzServiceFabriCluster, который не работал с операцией миграции в Az.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1128">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="ad5c1-1129">Исправлена проблема с добавлением сертификата кластера или приложения: теперь они добавляются только в Масштабируемые наборы виртуальных машин, которые сопоставлены с кластером, путем проверки идентификатора кластера в расширении.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1129">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="ad5c1-1130">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1130">Az.SignalR</span></span>
* <span data-ttu-id="ad5c1-1131">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1131">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad5c1-1132">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1132">Az.Sql</span></span>
* <span data-ttu-id="ad5c1-1133">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1133">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ad5c1-1134">Обновлено описание параметра LicenseType с добавлением возможных значений.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1134">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="ad5c1-1135">Исправлена проблема с неправильным обновлением удостоверения управляемого экземпляра, если оно было единственным обновляемым свойством.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1135">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="ad5c1-1136">Поддержка пользовательских параметров сортировки в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1136">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ad5c1-1137">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1137">Az.Storage</span></span>
* <span data-ttu-id="ad5c1-1138">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1138">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ad5c1-1139">Добавлен вывод подробных сообщений об ошибке при получении или установке классических свойств ведения журнала или метрик в учетной записи хранилища класса Premium, так как учетная запись хранилища класса Premium не поддерживает классические функции ведения журнала и метрик.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1139">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="ad5c1-1140">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1140">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="ad5c1-1141">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1141">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="ad5c1-1142">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1142">Az.TrafficManager</span></span>
* <span data-ttu-id="ad5c1-1143">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1143">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ad5c1-1144">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1144">Az.Websites</span></span>
* <span data-ttu-id="ad5c1-1145">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1145">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ad5c1-1146">Исправлена работа командлета New-AzWebAppSSLBinding: сертификат отправляется в правильную группу ресурсов и правильное расположение, если приложение размещено в ASE.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1146">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="ad5c1-1147">Исправлена работа командлета New-AzWebAppSSLBinding: теги не перезаписываются при привязке SSL-сертификата к приложению.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1147">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="ad5c1-1148">1.1.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1148">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ad5c1-1149">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1149">Az.Accounts</span></span>
* <span data-ttu-id="ad5c1-1150">Добавление области "Local" в Enable-AzureRmAlias.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1150">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad5c1-1151">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1151">Az.Compute</span></span>
* <span data-ttu-id="ad5c1-1152">Теперь имя не является обязательным в идентификаторе набора параметров для Restart/Start/Stop/Remove/Set-AzVM и Save-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1152">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="ad5c1-1153">Обновлено описание идентификатора в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1153">Updated the description of ID in help files</span></span>
* <span data-ttu-id="ad5c1-1154">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1154">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ad5c1-1155">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1155">Az.DataLakeStore</span></span>
* <span data-ttu-id="ad5c1-1156">Обновление версии пакета SDK для плоскости данных до 1.1.14 для устранения найденных проблем.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1156">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="ad5c1-1157">Исправлена обработка отрицательного времени доступа и времени изменения для getfilestatus и liststatus, исправлен токен отмены для асинхронных методов.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1157">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ad5c1-1158">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1158">Az.EventGrid</span></span>
* <span data-ttu-id="ad5c1-1159">Обновление для использования API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1159">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="ad5c1-1160">Обновлены указанные ниже командлеты для поддержки нового сценария в API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1160">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="ad5c1-1161">New-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1161">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="ad5c1-1162">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1162">Event Time-To-Live,</span></span>
        - <span data-ttu-id="ad5c1-1163">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1163">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="ad5c1-1164">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1164">Dead letter endpoint.</span></span>
    - <span data-ttu-id="ad5c1-1165">Update-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1165">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="ad5c1-1166">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1166">Event Time-To-Live,</span></span>
        - <span data-ttu-id="ad5c1-1167">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1167">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="ad5c1-1168">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1168">Dead letter endpoint.</span></span>
* <span data-ttu-id="ad5c1-1169">Для параметра EndpointType добавлены новые значения перечисления (storageQueue и hybridConnection) в командлеты New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1169">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="ad5c1-1170">Если ожидается, что создание или обновление подписки на событие повлечет за собой действия со стороны пользователя, выполняемые вручную, отображается предупреждение при создании или обновлении подписки события.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1170">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ad5c1-1171">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1171">Az.IotHub</span></span>
* <span data-ttu-id="ad5c1-1172">Пакет SDK Центра Интернета вещей обновлен до последней версии.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1172">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ad5c1-1173">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1173">Az.LogicApp</span></span>
* <span data-ttu-id="ad5c1-1174">Get-AzLogicApp позволяет перечислить все параметры без указанного имени.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1174">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad5c1-1175">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1175">Az.Resources</span></span>
* <span data-ttu-id="ad5c1-1176">Исправлена проблема с набором параметров при предоставлении параметров "-ODataQuery" и "-ResourceId" для "Get-AzResource".</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1176">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="ad5c1-1177">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7875.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1177">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="ad5c1-1178">Исправлена обработка параметра -Custom в New/Set-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1178">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="ad5c1-1179">Исправлена опечатка в документации по New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1179">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="ad5c1-1180">Параметр "-MailNickname" стал обязательным для "New-AzADUser".</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1180">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="ad5c1-1181">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8220.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1181">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="ad5c1-1182">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1182">Az.SignalR</span></span>
* <span data-ttu-id="ad5c1-1183">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1183">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad5c1-1184">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1184">Az.Sql</span></span>
* <span data-ttu-id="ad5c1-1185">Зависимость клиента управления хранением преобразована для общей реализации в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1185">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ad5c1-1186">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1186">Az.Storage</span></span>
* <span data-ttu-id="ad5c1-1187">Установка параметра StorageAccountName для контекста хранилища в качестве реального имени учетной записи хранения, если она была создана с использованием токена Sas, OAuth или анонимного доступа.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1187">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="ad5c1-1188">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1188">New-AzStorageContext</span></span>
* <span data-ttu-id="ad5c1-1189">Создание токена Sas большого двоичного объекта моментального снимка с параметром "-FullUri". Возвращаемый URI исправлен на URI моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1189">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="ad5c1-1190">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1190">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ad5c1-1191">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1191">Az.Websites</span></span>
* <span data-ttu-id="ad5c1-1192">Исправлена ошибка синтаксического анализа даты в "Get-AzDeletedWebApp".</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1192">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="ad5c1-1193">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1193">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="ad5c1-1194">1.0.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1194">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="ad5c1-1195">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1195">General</span></span>

- <span data-ttu-id="ad5c1-1196">Общедоступная версия модуля Az.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1196">General Availability of Az Module</span></span>
- <span data-ttu-id="ad5c1-1197">Справка в Интернете для каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1197">Online help for each module</span></span>
- <span data-ttu-id="ad5c1-1198">Дополнительные сведения и стратегию развития см. в статье [Announcing New Module 'Az'](https://aka.ms/azps-announce) (Объявление о новом модуле Az)</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1198">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="ad5c1-1199">Сведения о миграции с AzureRM см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1199">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="ad5c1-1200">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1200">Az.Accounts</span></span>
- <span data-ttu-id="ad5c1-1201">Изменено с Az.Profile.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1201">Changed from Az.Profile</span></span>
- <span data-ttu-id="ad5c1-1202">Исправлены форматы таблиц для типов профиля и контекста.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1202">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="ad5c1-1203">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1203">Az.ApiManagement</span></span>
- <span data-ttu-id="ad5c1-1204">Исправления для #7002.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1204">Fixes for #7002</span></span>
- <span data-ttu-id="ad5c1-1205">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1205">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="ad5c1-1206">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1206">Az.Batch</span></span>
- <span data-ttu-id="ad5c1-1207">Добавлена возможность видеть, какая версия агента узла пакетной службы Azure работает в пуле на каждой виртуальной машине, с помощью нового свойства `NodeAgentInformation` в `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1207">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="ad5c1-1208">Значение `Caching` по умолчанию для `PSDataDisk` теперь `ReadWrite` вместо `None`.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1208">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="ad5c1-1209">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1209">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="ad5c1-1210">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1210">Az.Billing</span></span>
- <span data-ttu-id="ad5c1-1211">Объединены командлеты Billing, Consumption и UsageAggregates. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0).</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1211">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="ad5c1-1212">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1212">Az.CognitivServices</span></span>
- <span data-ttu-id="ad5c1-1213">Добавлены средства заполнения для SkuName и Typem, доступные в операции New-AzureRmCognitiveServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1213">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="ad5c1-1214">Удален набор параметров GetSkusWithAccountParamSetName из Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1214">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="ad5c1-1215">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1215">Az.ContainerInstance</span></span>
- <span data-ttu-id="ad5c1-1216">Добавлена поддержка ManagedIdentity.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1216">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="ad5c1-1217">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1217">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="ad5c1-1218">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1218">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="ad5c1-1219">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1219">Az.DataLakeStore</span></span>
- <span data-ttu-id="ad5c1-1220">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1220">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="ad5c1-1221">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1221">Az.Monitor</span></span>
- <span data-ttu-id="ad5c1-1222">"Az.Insights" переименован в "Az.Monitor" и внесены другие незначительные критические изменения. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1222">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="ad5c1-1223">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1223">Az.KeyVault</span></span>
- <span data-ttu-id="ad5c1-1224">Из типов вывода удалено устаревшее свойство PurgeDisabled</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1224">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="ad5c1-1225">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1225">Az.MachineLearning</span></span>
- <span data-ttu-id="ad5c1-1226">Включены командлеты из модуля Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1226">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="ad5c1-1227">Az.Media</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1227">Az.Media</span></span>
- <span data-ttu-id="ad5c1-1228">Удаляет устаревший псевдоним Tags из New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1228">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="ad5c1-1229">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1229">Az.Network</span></span>
<span data-ttu-id="ad5c1-1230">В шлюз приложений добавлена поддержка настройки RewriteRuleSets</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1230">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="ad5c1-1231">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1231">New cmdlets added:</span></span>
        - <span data-ttu-id="ad5c1-1232">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1232">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ad5c1-1233">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1233">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ad5c1-1234">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1234">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ad5c1-1235">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1235">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ad5c1-1236">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1236">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ad5c1-1237">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1237">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="ad5c1-1238">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1238">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="ad5c1-1239">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1239">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="ad5c1-1240">В следующие командлеты добавлен необязательный параметр -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1240">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="ad5c1-1241">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1241">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="ad5c1-1242">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1242">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="ad5c1-1243">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1243">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="ad5c1-1244">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1244">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="ad5c1-1245">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1245">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="ad5c1-1246">New-AzureRmApplicationGatewayUrlPathMapConfig добавил с помощью идентификатора поддержку KeyVault для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1246">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="ad5c1-1247">В следующие командлеты добавлен необязательный параметр -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1247">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="ad5c1-1248">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1248">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="ad5c1-1249">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1249">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="ad5c1-1250">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1250">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="ad5c1-1251">В командлет New-AzApplicationGateway добавлен необязательный параметр -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1251">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="ad5c1-1252">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1252">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="ad5c1-1253">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1253">Az.OperationalInsights</span></span>
- <span data-ttu-id="ad5c1-1254">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1254">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="ad5c1-1255">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1255">Az.Profile</span></span>
- <span data-ttu-id="ad5c1-1256">Имя модуля изменено на Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1256">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="ad5c1-1257">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1257">Az.RecoveryServices</span></span>
- <span data-ttu-id="ad5c1-1258">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1258">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="ad5c1-1259">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1259">Az.Resources</span></span>
- <span data-ttu-id="ad5c1-1260">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1260">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="ad5c1-1261">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1261">Az.ServiceFabric</span></span>
- <span data-ttu-id="ad5c1-1262">Поддержка спецификации сертификата по общему имени и отпечатку</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1262">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="ad5c1-1263">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1263">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="ad5c1-1264">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1264">Az.SIgnalR</span></span>
- <span data-ttu-id="ad5c1-1265">Общедоступная версия командлетов PowerShell для SIgnalR</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1265">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="ad5c1-1266">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1266">Az.Sql</span></span>
- <span data-ttu-id="ad5c1-1267">Добавлены новые типы обнаружения Data_Exfiltration и Unsafe_Action в командлеты обнаружения угроз</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1267">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="ad5c1-1268">Примеры обновленной документации для командлетов аудита Sql</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1268">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="ad5c1-1269">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1269">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="ad5c1-1270">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1270">Az.Storage</span></span>
- <span data-ttu-id="ad5c1-1271">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1271">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="ad5c1-1272">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1272">Az.Websites</span></span>
- <span data-ttu-id="ad5c1-1273">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1273">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="ad5c1-1274">0.7.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1274">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="ad5c1-1275">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1275">General</span></span>

* <span data-ttu-id="ad5c1-1276">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1276">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="ad5c1-1277">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1277">Az.Compute</span></span>

* <span data-ttu-id="ad5c1-1278">Добавлена поддержка UltraSSD и образов коллекции в простых наборах параметров для командлетов `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1278">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="ad5c1-1279">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1279">Az.DataLakeStore</span></span>

* <span data-ttu-id="ad5c1-1280">Исправлено косую черту в конце домена учетной записи ADLS</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1280">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="ad5c1-1281">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1281">Az.FrontDoor</span></span>

* <span data-ttu-id="ad5c1-1282">Исправлены некоторые неработающие ссылки</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1282">Fixed some broken links</span></span>
    - <span data-ttu-id="ad5c1-1283">В статьях New-AzureRmFrontDoor и Set-AzureRmFrontDoor исправлена ссылка на статью командлета New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1283">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="ad5c1-1284">В статье New-AzureRmFrontDoorManagedRuleObject исправлена ссылка на статью командлета New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1284">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="ad5c1-1285">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1285">Az.RecoveryServices</span></span>

* <span data-ttu-id="ad5c1-1286">Добавлены проверки на стороне клиента для операций восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1286">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="ad5c1-1287">StorageAccountName и storageAccountResourceGroupName являются необязательными для восстановления afs.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1287">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="ad5c1-1288">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1288">Az.Resources</span></span>

* <span data-ttu-id="ad5c1-1289">Исправление для https://github.com/Azure/azure-powershell/issues/7679.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1289">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="ad5c1-1290">Обновите Get-AzureRmRoleAssignment, чтобы использовать область подписки, если она указана при запросе классических администраторов.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1290">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="ad5c1-1291">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1291">Az.Sql</span></span>

* <span data-ttu-id="ad5c1-1292">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1292">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="ad5c1-1293">Устранена проблема с использованием Get-AzureRmSqlDatabaseVulnerabilityAssessment с .NET Core.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1293">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="ad5c1-1294">Изменена документация справочных сообщений, связанных с командлетами аудита SQL.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1294">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="ad5c1-1295">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1295">Az.Storage</span></span>

* <span data-ttu-id="ad5c1-1296">Добавлено -EnableHierarchicalNamespace к New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1296">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="ad5c1-1297">Устранена проблема, из-за которой командлет Copy File не может повторно использовать исходный контекст в пункте назначения, если не введен -DestContext</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1297">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="ad5c1-1298">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1298">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="ad5c1-1299">Поддержка статической конфигурации сайта</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1299">Support Static Website configuration</span></span>
    - <span data-ttu-id="ad5c1-1300">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1300">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="ad5c1-1301">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1301">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="ad5c1-1302">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1302">Az.Websites</span></span>

* <span data-ttu-id="ad5c1-1303">Set-AzureRmWebApp и Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1303">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="ad5c1-1304">Добавлен новый параметр (-AzureStoragePath), который указывает путь службы хранилища Azure для подключения в приложениях-контейнерах Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1304">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="ad5c1-1305">Используйте выходные данные нового командлета New-AzureRmWebAppAzureStoragePath в качестве параметра, чтобы задать пути к службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1305">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="ad5c1-1306">0.6.1 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1306">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="ad5c1-1307">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1307">Az.ApiManagement</span></span>
* <span data-ttu-id="ad5c1-1308">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1308">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="ad5c1-1309">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1309">Az.Automation</span></span>
* <span data-ttu-id="ad5c1-1310">Командлеты службы автоматизации Azure на базе Swagger.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1310">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="ad5c1-1311">Добавлены командлеты для Управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1311">Added Update Management cmdlets</span></span>
* <span data-ttu-id="ad5c1-1312">Добавлены командлеты для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1312">Added Source Control cmdlets</span></span>
* <span data-ttu-id="ad5c1-1313">Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1313">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="ad5c1-1314">Исправлена команда DSC для регистрации узла.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1314">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="ad5c1-1315">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1315">Az.Compute</span></span>
* <span data-ttu-id="ad5c1-1316">Исправлена проблема с удостоверением, назначаемым системой.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1316">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="ad5c1-1317">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1317">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="ad5c1-1318">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1318">Az.ContainerInstance</span></span>
* <span data-ttu-id="ad5c1-1319">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1319">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="ad5c1-1320">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1320">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="ad5c1-1321">Обновлено описание в примерах командлетов для Marketplace.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1321">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="ad5c1-1322">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1322">Az.Network</span></span>
* <span data-ttu-id="ad5c1-1323">Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1323">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="ad5c1-1324">Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1324">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="ad5c1-1325">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1325">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="ad5c1-1326">Исправлены проблемы с использованием памяти в карте виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1326">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="ad5c1-1327">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1327">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="ad5c1-1328">Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1328">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="ad5c1-1329">Параметры часового пояса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1329">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="ad5c1-1330">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1330">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="ad5c1-1331">Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1331">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="ad5c1-1332">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1332">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="ad5c1-1333">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1333">Az.Relay</span></span>
* <span data-ttu-id="ad5c1-1334">Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1334">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="ad5c1-1335">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1335">Az.Resources</span></span>
* <span data-ttu-id="ad5c1-1336">Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1336">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="ad5c1-1337">Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1337">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="ad5c1-1338">Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1338">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="ad5c1-1339">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1339">Az.ServiceFabric</span></span>
* <span data-ttu-id="ad5c1-1340">Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1340">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="ad5c1-1341">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1341">Az.Sql</span></span>
* <span data-ttu-id="ad5c1-1342">Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1342">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="ad5c1-1343">Get-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1343">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ad5c1-1344">New-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1344">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ad5c1-1345">Set-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1345">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ad5c1-1346">Remove-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1346">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ad5c1-1347">Get-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1347">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="ad5c1-1348">New-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1348">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="ad5c1-1349">Restore-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1349">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="ad5c1-1350">Remove-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1350">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="ad5c1-1351">Добавлено расширенное управление политиками аудита для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1351">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="ad5c1-1352">Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1352">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="ad5c1-1353">Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1353">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="ad5c1-1354">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1354">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="ad5c1-1355">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1355">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="ad5c1-1356">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1356">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="ad5c1-1357">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1357">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="ad5c1-1358">Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1358">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="ad5c1-1359">0.5.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1359">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ad5c1-1360">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1360">General</span></span>
* <span data-ttu-id="ad5c1-1361">Добавлены средства заполнения ресурсов для многих основных командлетов — они позволяют вам переключать существующие имена ресурсов при вызове командлетов в интерактивном режиме</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1361">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="ad5c1-1362">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1362">Az.Profile</span></span>
* <span data-ttu-id="ad5c1-1363">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1363">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="ad5c1-1364">В командлете Connect-AzAccount параметр TenantId переименован в Tenant и добавлен псевдоним для TenantId</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1364">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="ad5c1-1365">Обновлено описание TenantId для командлета Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1365">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="ad5c1-1366">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1366">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="ad5c1-1367">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1367">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="ad5c1-1368">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1368">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="ad5c1-1369">Устранена проблема, при которой командлет Disconnect-AzAccount вызывал сбой при отсутствии подключения</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1369">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="ad5c1-1370">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1370">Az.CognitiveServices</span></span>
* <span data-ttu-id="ad5c1-1371">Добавлена операция Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1371">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad5c1-1372">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1372">Az.Compute</span></span>
* <span data-ttu-id="ad5c1-1373">Добавлены командлеты Add-AzVmssVMDataDisk и Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1373">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="ad5c1-1374">Get-AzVMImage отображает AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1374">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="ad5c1-1375">Устранена проблема, при которой значения параметров SetAzVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1375">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ad5c1-1376">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1376">Az.DataLakeStore</span></span>
* <span data-ttu-id="ad5c1-1377">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1377">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="ad5c1-1378">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1378">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="ad5c1-1379">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1379">Az.Insights</span></span>
* <span data-ttu-id="ad5c1-1380">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1380">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="ad5c1-1381">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1381">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="ad5c1-1382">Исправлена проблема № 7513 [Insights], при которой для командлета Set-AzDiagnosticSetting требовалось явное указание категорий во время создания параметра</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1382">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="ad5c1-1383">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1383">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ad5c1-1384">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1384">Az.Network</span></span>
* <span data-ttu-id="ad5c1-1385">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1385">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="ad5c1-1386">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1386">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="ad5c1-1387">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1387">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="ad5c1-1388">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1388">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="ad5c1-1389">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1389">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="ad5c1-1390">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1390">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="ad5c1-1391">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1391">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ad5c1-1392">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1392">Az.PolicyInsights</span></span>
* <span data-ttu-id="ad5c1-1393">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1393">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad5c1-1394">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1394">Az.Resources</span></span>
* <span data-ttu-id="ad5c1-1395">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1395">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="ad5c1-1396">Разрешено перечисление ресурсов с помощью параметра -ResourceId для командлета Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1396">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ad5c1-1397">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1397">Az.ServiceBus</span></span>
* <span data-ttu-id="ad5c1-1398">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1398">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ad5c1-1399">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1399">Az.ServiceFabric</span></span>
* <span data-ttu-id="ad5c1-1400">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1400">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="ad5c1-1401">Исправлен командлет Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1401">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="ad5c1-1402">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1402">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="ad5c1-1403">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1403">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="ad5c1-1404">Исправлен командлет Update-AzServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1404">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="ad5c1-1405">0.4.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1405">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="ad5c1-1406">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1406">Az.Profile</span></span>
* <span data-ttu-id="ad5c1-1407">Устранена проблема с Get-AzSubscription в CloudShell</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1407">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="ad5c1-1408">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1408">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad5c1-1409">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1409">Az.Compute</span></span>
* <span data-ttu-id="ad5c1-1410">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzVm</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1410">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="ad5c1-1411">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1411">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ad5c1-1412">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1412">Az.DataLakeStore</span></span>
* <span data-ttu-id="ad5c1-1413">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1413">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="ad5c1-1414">Get-AzDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1414">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="ad5c1-1415">Add-AzDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1415">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="ad5c1-1416">Set-AzDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1416">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="ad5c1-1417">Remove-AzDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1417">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ad5c1-1418">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1418">Az.Network</span></span>
* <span data-ttu-id="ad5c1-1419">Обновлен командлет Test-AzNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1419">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="ad5c1-1420">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1420">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad5c1-1421">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1421">Az.Resources</span></span>
* <span data-ttu-id="ad5c1-1422">Устранена проблема, из-за которой командлет Get-AzRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), благодаря добавлению понятного исключения в сценарий.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1422">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="ad5c1-1423">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1423">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="ad5c1-1424">0.3.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1424">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="ad5c1-1425">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1425">Azure.Storage</span></span>
* <span data-ttu-id="ad5c1-1426">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1426">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="ad5c1-1427">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1427">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="ad5c1-1428">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1428">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="ad5c1-1429">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1429">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="ad5c1-1430">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1430">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="ad5c1-1431">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1431">Az.CognitiveServices</span></span>
* <span data-ttu-id="ad5c1-1432">Поддержка Get-AzCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1432">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ad5c1-1433">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1433">Az.Compute</span></span>
* <span data-ttu-id="ad5c1-1434">Исправлена команда Get-AzVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1434">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="ad5c1-1435">Добавлен пример использования SimpleParameterSet в справку командлета New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1435">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="ad5c1-1436">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1436">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="ad5c1-1437">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1437">Az.DataFactoryV2</span></span>
* <span data-ttu-id="ad5c1-1438">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1438">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ad5c1-1439">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1439">Az.Network</span></span>
* <span data-ttu-id="ad5c1-1440">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1440">Added NetworkProfile functionality.</span></span> <span data-ttu-id="ad5c1-1441">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1441">new cmdlets added</span></span>
    - <span data-ttu-id="ad5c1-1442">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1442">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="ad5c1-1443">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1443">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="ad5c1-1444">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1444">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="ad5c1-1445">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1445">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="ad5c1-1446">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1446">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="ad5c1-1447">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1447">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="ad5c1-1448">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1448">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="ad5c1-1449">Добавлены командлеты: New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1449">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="ad5c1-1450">Добавлены командлеты: Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1450">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="ad5c1-1451">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1451">Az.RedisCache</span></span>
* <span data-ttu-id="ad5c1-1452">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1452">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="ad5c1-1453">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1453">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="ad5c1-1454">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1454">Az.Resources</span></span>
* <span data-ttu-id="ad5c1-1455">Добавлен отсутствующий параметр -Mode в командлет Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1455">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="ad5c1-1456">Исправлена ошибка командлета Get-AzProviderOperation для операций, когда Origin содержит User</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1456">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="ad5c1-1457">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1457">Az.Sql</span></span>
* <span data-ttu-id="ad5c1-1458">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1458">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ad5c1-1459">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1459">Az.Websites</span></span>
* <span data-ttu-id="ad5c1-1460">Новый командлет Get-AzWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1460">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="ad5c1-1461">Новые командлеты New-AzWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1461">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="ad5c1-1462">0.2.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1462">0.2.0 - September 2018</span></span>
 <span data-ttu-id="ad5c1-1463">Первый выпуск</span><span class="sxs-lookup"><span data-stu-id="ad5c1-1463">Initial Release</span></span>