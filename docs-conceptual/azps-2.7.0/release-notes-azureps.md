---
ms.openlocfilehash: 96e6d7bc0cc29adc1c0e49ba344d27349454c214
ms.sourcegitcommit: 92722d603b60dc769660e7517da60110133d9959
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/24/2019
ms.locfileid: "71226445"
---
## <a name="270---september-2019"></a><span data-ttu-id="dd594-101">2.7.0 — сентябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="dd594-101">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="dd594-102">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="dd594-102">Az.ApiManagement</span></span>
* <span data-ttu-id="dd594-103">В справочной документации по командлету Set-AzApiManagementPolicy обновлено описание параметра -Format.</span><span class="sxs-lookup"><span data-stu-id="dd594-103">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="dd594-104">Из справочной документации удалены ссылки на нерекомендуемый командлет Update-AzApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="dd594-104">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="dd594-105">Вместо него следует использовать командлет Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="dd594-105">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="dd594-106">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dd594-106">Az.Automation</span></span>
* <span data-ttu-id="dd594-107">В справочной документации по командлету Register-AzAutomationDscNode исправлена опечатка в примере.</span><span class="sxs-lookup"><span data-stu-id="dd594-107">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="dd594-108">Добавлено уточнение об ограничениях ОС для командлета Register-AzAutomationDSCNode.</span><span class="sxs-lookup"><span data-stu-id="dd594-108">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="dd594-109">Исправлено исключение пустой ссылки для параметра -Wait в командлете Start-AzAutomationRunbook.</span><span class="sxs-lookup"><span data-stu-id="dd594-109">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dd594-110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd594-110">Az.Compute</span></span>
* <span data-ttu-id="dd594-111">Добавлен параметр UploadSizeInBytes для командлета New-AzDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="dd594-111">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="dd594-112">Добавлен добавочный параметр для командлета New-AzSnapshotConfig.</span><span class="sxs-lookup"><span data-stu-id="dd594-112">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="dd594-113">Для виртуальной машины добавлены такие функции с низким приоритетом:</span><span class="sxs-lookup"><span data-stu-id="dd594-113">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="dd594-114">Для командлета New-AzVMConfig добавлены параметры MaxPrice, EvictionPolicy и Priority.</span><span class="sxs-lookup"><span data-stu-id="dd594-114">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="dd594-115">Для командлетов New-AzVmssConfig, Update-AzVM и Update-AzVmss добавлен параметр MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="dd594-115">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="dd594-116">Для командлета Get-AzAvailabilitySet устранена проблема со ссылкой на виртуальную машину, когда в нем перечисляются все группы доступности в подписке.</span><span class="sxs-lookup"><span data-stu-id="dd594-116">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="dd594-117">Исправлено исключение NULL для командлета Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="dd594-117">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="dd594-118">Исправлен метод поиска VHD для относительной конечной позиции.</span><span class="sxs-lookup"><span data-stu-id="dd594-118">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="dd594-119">Устранена проблема с UltraSSD для командлетов New-AzVM и Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="dd594-119">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dd594-120">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dd594-120">Az.DataFactory</span></span>
* <span data-ttu-id="dd594-121">Добавлены 3 новые команды для ADF версии 2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription и Get-AzDataFactoryV2TriggerSubscriptionStatus.</span><span class="sxs-lookup"><span data-stu-id="dd594-121">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="dd594-122">Пакет SDK ADF для .NET обновлен до версии 4.1.3.</span><span class="sxs-lookup"><span data-stu-id="dd594-122">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="dd594-123">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="dd594-123">Az.HDInsight</span></span>
* <span data-ttu-id="dd594-124">Укажите критические изменения.</span><span class="sxs-lookup"><span data-stu-id="dd594-124">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="dd594-125">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="dd594-125">Az.IotHub</span></span>
* <span data-ttu-id="dd594-126">Добавлена поддержка для вызова отработки отказа для IotHub в георегион аварийного восстановления.</span><span class="sxs-lookup"><span data-stu-id="dd594-126">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="dd594-127">Добавлена поддержка для управления обогащением сообщений для IotHub.</span><span class="sxs-lookup"><span data-stu-id="dd594-127">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="dd594-128">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="dd594-128">New cmdlets are:</span></span>
    - <span data-ttu-id="dd594-129">Add-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="dd594-129">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="dd594-130">Get-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="dd594-130">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="dd594-131">Remove-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="dd594-131">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="dd594-132">Set-AzIotHubMessageEnrichment.</span><span class="sxs-lookup"><span data-stu-id="dd594-132">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="dd594-133">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dd594-133">Az.Monitor</span></span>
* <span data-ttu-id="dd594-134">Указание на самую последнюю версию пакета SDK для монитора, т. е. 0.24.1-preview:</span><span class="sxs-lookup"><span data-stu-id="dd594-134">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="dd594-135">В командлеты метрик добавлены некритические изменения, т. е. перечисление единиц поддерживает несколько новых значений.</span><span class="sxs-lookup"><span data-stu-id="dd594-135">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="dd594-136">Эти командлеты доступны только для чтения, поэтому входные данные командлетов не будут изменены.</span><span class="sxs-lookup"><span data-stu-id="dd594-136">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="dd594-137">Актуальная версия API запросов **ActionGroups** — **2019-06-01**. До этого была версия **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="dd594-137">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="dd594-138">Тесты сценария обновлены в соответствии с этим изменением.</span><span class="sxs-lookup"><span data-stu-id="dd594-138">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="dd594-139">В конструкторы классов **EmailReceiver** и **WebhookReceiver** добавлен один новый обязательный аргумент — логическое значение с именем **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="dd594-139">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="dd594-140">В настоящее время для него установлено значение false, чтобы скрыть это критическое изменение от командлетов.</span><span class="sxs-lookup"><span data-stu-id="dd594-140">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="dd594-141">**Примечание**. Это временное изменение, которое должно быть подтверждено командой оповещения.</span><span class="sxs-lookup"><span data-stu-id="dd594-141">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="dd594-142">Порядок аргументов для конструктора класса **Source** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="dd594-142">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="dd594-143">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="dd594-143">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="dd594-144">Порядок аргументов для конструктора класса **AlertingAction** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="dd594-144">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="dd594-145">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="dd594-145">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="dd594-146">Добавлена поддержка критериев динамического порога для оповещения метрики версии 2:</span><span class="sxs-lookup"><span data-stu-id="dd594-146">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="dd594-147">New-AzMetricAlertRuleV2Criteria: теперь также позволяет создавать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="dd594-147">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="dd594-148">Add-AzMetricAlertRuleV2: теперь также позволяет принимать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="dd594-148">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="dd594-149">Добавлены усовершенствования в командлетах запланированных правил запросов (SQR).</span><span class="sxs-lookup"><span data-stu-id="dd594-149">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="dd594-150">Командлеты будут принимать параметр Location в обоих форматах: расположение (например, eastus) или отображаемое имя расположения (например, "восточная часть США").</span><span class="sxs-lookup"><span data-stu-id="dd594-150">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="dd594-151">Параметр Enabled проиллюстрирован в файлах справки надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="dd594-151">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="dd594-152">Добавлены примеры для необязательного параметра ActionGroup.</span><span class="sxs-lookup"><span data-stu-id="dd594-152">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="dd594-153">Все файлы справки улучшены.</span><span class="sxs-lookup"><span data-stu-id="dd594-153">Overall improved help files</span></span>
* <span data-ttu-id="dd594-154">Исправлена ошибка в определении типа области для командлета Set-AzActionRule.</span><span class="sxs-lookup"><span data-stu-id="dd594-154">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dd594-155">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dd594-155">Az.Network</span></span>
* <span data-ttu-id="dd594-156">Исправлен неправильный пример в справочной документации по командлету New-AzApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="dd594-156">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="dd594-157">В справочную документацию по командлету Get-AzNetworkWatcherPacketCapture добавлено примечание, посвященное извлечению всех свойств для записи пакетов.</span><span class="sxs-lookup"><span data-stu-id="dd594-157">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="dd594-158">В справочной документации по командлету Test-AzNetworkWatcherIPFlow исправлен пример: теперь он правильно перечисляет сетевые карты.</span><span class="sxs-lookup"><span data-stu-id="dd594-158">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="dd594-159">Улучшен анализ облачных исключений для отображения дополнительных сведений (при их наличии).</span><span class="sxs-lookup"><span data-stu-id="dd594-159">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="dd594-160">Улучшен анализ облачных исключений для обработки дополнительного типа исключения SDK.</span><span class="sxs-lookup"><span data-stu-id="dd594-160">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="dd594-161">Исправлено неправильное сопоставление моделей правил безопасности.</span><span class="sxs-lookup"><span data-stu-id="dd594-161">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="dd594-162">Добавлены свойства сетевого интерфейса для компонента частного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="dd594-162">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="dd594-163">Для интерфейса PSNetworkInterface добавлено свойство PrivateEndpoint с типом PSResourceId.</span><span class="sxs-lookup"><span data-stu-id="dd594-163">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="dd594-164">В PSNetworkInterfaceIPConfiguration добавлено свойство PrivateLinkConnectionProperties с типом PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="dd594-164">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="dd594-165">Добавлен новый класс модели: PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="dd594-165">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="dd594-166">Добавлен новый тип ApplicationRuleProtocolType "mssql" для ресурса Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="dd594-166">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="dd594-167">Поддержка многоканального подключения в Виртуальной глобальной сети:</span><span class="sxs-lookup"><span data-stu-id="dd594-167">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="dd594-168">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="dd594-168">New cmdlets</span></span>
        - <span data-ttu-id="dd594-169">New-AzVpnSiteLink;</span><span class="sxs-lookup"><span data-stu-id="dd594-169">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="dd594-170">New-AzVpnSiteLinkConnection;</span><span class="sxs-lookup"><span data-stu-id="dd594-170">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="dd594-171">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="dd594-171">Updated cmdlet:</span></span>
        - <span data-ttu-id="dd594-172">New-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="dd594-172">New-VpnSite</span></span>
        - <span data-ttu-id="dd594-173">Update-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="dd594-173">Update-VpnSite</span></span>
        - <span data-ttu-id="dd594-174">New-VpnConnection;</span><span class="sxs-lookup"><span data-stu-id="dd594-174">New-VpnConnection</span></span>
        - <span data-ttu-id="dd594-175">Update-VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="dd594-175">Update-VpnConnection</span></span>
* <span data-ttu-id="dd594-176">Исправлены документы с некоторыми примерами PowerShell для использования командлетов AZ вместо командлетов AzureRM.</span><span class="sxs-lookup"><span data-stu-id="dd594-176">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dd594-177">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dd594-177">Az.RecoveryServices</span></span>
* <span data-ttu-id="dd594-178">Для объекта AzureVMpolicy добавлен новый атрибут — ProtectedItemsCount.</span><span class="sxs-lookup"><span data-stu-id="dd594-178">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="dd594-179">Добавлены тесты для политики виртуальной машины и восстановления исходной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="dd594-179">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="dd594-180">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd594-180">Az.Resources</span></span>
* <span data-ttu-id="dd594-181">Исправлена ошибка, при которой не удавалось вызвать командлет New-AzRoleAssignment без параметра Scope.</span><span class="sxs-lookup"><span data-stu-id="dd594-181">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="dd594-182">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dd594-182">Az.ServiceFabric</span></span>
* <span data-ttu-id="dd594-183">Исправлена опечатка в примере в справочной документации по командлету Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="dd594-183">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="dd594-184">Добавлены новые командлеты для управления приложениями и службами:</span><span class="sxs-lookup"><span data-stu-id="dd594-184">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="dd594-185">New-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="dd594-185">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="dd594-186">New-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="dd594-186">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="dd594-187">New-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="dd594-187">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="dd594-188">New-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="dd594-188">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="dd594-189">Update-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="dd594-189">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="dd594-190">Get-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="dd594-190">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="dd594-191">Get-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="dd594-191">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="dd594-192">Get-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="dd594-192">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="dd594-193">Get-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="dd594-193">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="dd594-194">Remove-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="dd594-194">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="dd594-195">Remove-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="dd594-195">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="dd594-196">Remove-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="dd594-196">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="dd594-197">Remove-AzServiceFabricServic.</span><span class="sxs-lookup"><span data-stu-id="dd594-197">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="dd594-198">Пакет SDK для Service Fabric обновлен до версии 1.2.0, в которой используется версия API 2019-03-01 поставщика ресурсов Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="dd594-198">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="dd594-199">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="dd594-199">Az.SignalR</span></span>
* <span data-ttu-id="dd594-200">Добавлены командлеты Update, Restart, CheckNameAvailability и GetUsage.</span><span class="sxs-lookup"><span data-stu-id="dd594-200">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="dd594-201">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd594-201">Az.Sql</span></span>
* <span data-ttu-id="dd594-202">Обновлен пример в справочной документации по командлету Get-AzSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="dd594-202">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="dd594-203">Добавлен пример виртуального ядра для командлета создания эластичного пула (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="dd594-203">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="dd594-204">Удалена проверка свойства EmailAddresses и того, что свойство EmailAdmins правильное в случае, если свойство EmailAddresses пустое в командлетах Set-AzSqlServerAdvancedThreatProtectionPolicy и Set-AzSqlDatabaseAdvancedThreatProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="dd594-204">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="dd594-205">Теперь, если существует несколько параметров диагностики, включающих категорию аудита, параметры аудита сервера и базы данных удаляются.</span><span class="sxs-lookup"><span data-stu-id="dd594-205">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="dd594-206">Исправлена проверка адресов электронной почты в нескольких командлетах оценки уязвимостей SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting и Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="dd594-206">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dd594-207">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dd594-207">Az.Storage</span></span>
* <span data-ttu-id="dd594-208">Обновлен пример в справочной документации по командлету Get-AzStorageAccountKey.</span><span class="sxs-lookup"><span data-stu-id="dd594-208">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="dd594-209">Теперь при отправке и загрузке файла Azure в конечном файле сохраняются свойства SMB исходного файла (атрибуты файла, время создания файла, время последней записи файла).</span><span class="sxs-lookup"><span data-stu-id="dd594-209">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="dd594-210">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="dd594-210">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="dd594-211">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="dd594-211">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="dd594-212">Исправлена операция отправки блочного BLOB-объекта, в которой происходили сбои свойств и метаданных в контейнере с включенной ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="dd594-212">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="dd594-213">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="dd594-213">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="dd594-214">Добавлена поддержка управления общими папками Azure в API плоскости управления с помощью таких командлетов:</span><span class="sxs-lookup"><span data-stu-id="dd594-214">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="dd594-215">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="dd594-215">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="dd594-216">Get-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="dd594-216">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="dd594-217">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="dd594-217">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="dd594-218">Remove-AzRmStorageShare.</span><span class="sxs-lookup"><span data-stu-id="dd594-218">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dd594-219">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dd594-219">Az.Websites</span></span>
* <span data-ttu-id="dd594-220">Устранена проблема, из-за которой теги webapp удалялись при переносе приложения в новый ASP.</span><span class="sxs-lookup"><span data-stu-id="dd594-220">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="dd594-221">Теперь командлет Publish-AzureWebapp работает в Linux и Windows.</span><span class="sxs-lookup"><span data-stu-id="dd594-221">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="dd594-222">Обновлен пример в справочной документации по командлету Get-AzWebAppPublishingProfile.</span><span class="sxs-lookup"><span data-stu-id="dd594-222">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="dd594-223">2.6.0 — август 2019 г.</span><span class="sxs-lookup"><span data-stu-id="dd594-223">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="dd594-224">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="dd594-224">General</span></span>
* <span data-ttu-id="dd594-225">Исправлены опечатки в модулях.</span><span class="sxs-lookup"><span data-stu-id="dd594-225">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="dd594-226">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dd594-226">Az.Accounts</span></span>
* <span data-ttu-id="dd594-227">Добавлена поддержка назначаемого пользователем удостоверения MSI при проверке подлинности в Функциях Azure (№ 9479).</span><span class="sxs-lookup"><span data-stu-id="dd594-227">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="dd594-228">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="dd594-228">Az.Aks</span></span>
* <span data-ttu-id="dd594-229">Устранена проблема с выходными данными для Get-AzAks.</span><span class="sxs-lookup"><span data-stu-id="dd594-229">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="dd594-230">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9847.</span><span class="sxs-lookup"><span data-stu-id="dd594-230">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="dd594-231">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="dd594-231">Az.ApiManagement</span></span>
* <span data-ttu-id="dd594-232">исправлена проблема https://github.com/Azure/azure-powershell/issues/9351.</span><span class="sxs-lookup"><span data-stu-id="dd594-232">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="dd594-233">Обновлена версия NuGet для .NET, которая не накладывает ограничений на productId, apiId, groupId и userId.</span><span class="sxs-lookup"><span data-stu-id="dd594-233">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="dd594-234">**Get-AzApiManagementProduct**. Добавлена поддержка запросов к продуктам с помощью API.</span><span class="sxs-lookup"><span data-stu-id="dd594-234">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="dd594-235">**New-AzApiManagementApiRevision**. Устранена проблема, из-за которой не задавался параметр ApiRevisionDescription при создании новой редакции API https://github.com/Azure/azure-powershell/issues/9752.</span><span class="sxs-lookup"><span data-stu-id="dd594-235">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="dd594-236">Исправлено написание имени модели c PsApiManagementOAuth2AuthrozationServer на PsApiManagementOAuth2AuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="dd594-236">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="dd594-237">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="dd594-237">Az.Batch</span></span>
* <span data-ttu-id="dd594-238">Исправлена опечатка в написании Windows со строчной буквы в справочных сообщениях и документации.</span><span class="sxs-lookup"><span data-stu-id="dd594-238">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="dd594-239">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="dd594-239">Az.Cdn</span></span>
* <span data-ttu-id="dd594-240">Исправлена опечатка во вспомогательном приложении модуля CDN.</span><span class="sxs-lookup"><span data-stu-id="dd594-240">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dd594-241">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd594-241">Az.Compute</span></span>
* <span data-ttu-id="dd594-242">Добавлен параметр VmssId в новый командлет Add New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="dd594-242">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="dd594-243">Добавлены параметры TerminateScheduledEvents и TerminateScheduledEventNotBeforeTimeoutInMinutes в New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="dd594-243">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="dd594-244">Добавлено свойство HyperVGeneration в объект образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="dd594-244">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="dd594-245">Добавлены компоненты Host и HostGroup.</span><span class="sxs-lookup"><span data-stu-id="dd594-245">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="dd594-246">Новые командлеты:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="dd594-246">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="dd594-247">Параметр HostId добавлен в New-AzVMConfig и New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="dd594-247">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="dd594-248">Исправлен пример в документации по Invoke-AzVMRunCommand, в котором теперь используется правильное имя параметра.</span><span class="sxs-lookup"><span data-stu-id="dd594-248">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="dd594-249">Исправлено описание VolumeType в справочной документации по Set-AzVMDiskEncryptionExtension и Set-AzVmssDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="dd594-249">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dd594-250">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dd594-250">Az.DataFactory</span></span>
* <span data-ttu-id="dd594-251">Исправлена опечатка в написании Windows со строчной буквы в документации по New-AzDataFactoryEncryptValue.</span><span class="sxs-lookup"><span data-stu-id="dd594-251">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="dd594-252">Пакет SDK ADF для .NET обновлен до версии 4.1.2.</span><span class="sxs-lookup"><span data-stu-id="dd594-252">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="dd594-253">Добавлены параметры DataProxyIntegrationRuntimeName, DataProxyStagingLinkedServiceName и DataProxyStagingPath в командлет Set-AzureRmDataFactoryV2IntegrationRuntime, что позволяет настраивать локальную среду выполнения интеграции в качестве прокси-сервера для Azure-SSIS Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="dd594-253">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="dd594-254">Обновлены PSTriggerRun для отображения активированных конвейеров, сообщений и свойств и PSActivityRun для отображения типа действия.</span><span class="sxs-lookup"><span data-stu-id="dd594-254">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="dd594-255">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dd594-255">Az.DataLakeStore</span></span>
* <span data-ttu-id="dd594-256">Устранена проблема, при которой Get-DataLakeStoreDeletedItem переставал отвечать на запросы при возникновении ошибок или удаленных исключений.</span><span class="sxs-lookup"><span data-stu-id="dd594-256">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="dd594-257">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="dd594-257">Az.EventHub</span></span>
* <span data-ttu-id="dd594-258">Исправлена проблема № 9658: опечатка в написании параметра VirtualNteworkRule у Set-AzEventHubNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="dd594-258">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="dd594-259">Исправлена проблема № 9558: в Set-AzEventHubNamespace используется PATCH вместо PUT.</span><span class="sxs-lookup"><span data-stu-id="dd594-259">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="dd594-260">В командлет Set-AzEventHubNamespace добавлен параметр EnableKafka.</span><span class="sxs-lookup"><span data-stu-id="dd594-260">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="dd594-261">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="dd594-261">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="dd594-262">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="dd594-262">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="dd594-263">Исправлено написание Azure со строчной буквы.</span><span class="sxs-lookup"><span data-stu-id="dd594-263">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="dd594-264">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dd594-264">Az.Monitor</span></span>
* <span data-ttu-id="dd594-265">Исправлены неправильные имена параметров в справочной документации.</span><span class="sxs-lookup"><span data-stu-id="dd594-265">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dd594-266">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dd594-266">Az.Network</span></span>
* <span data-ttu-id="dd594-267">Обновлен New-AzPrivateLinkServiceIpConfig.</span><span class="sxs-lookup"><span data-stu-id="dd594-267">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="dd594-268">Параметр PublicIpAddress объявлен нерекомендуемым, так как он не используется на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="dd594-268">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="dd594-269">Добавлен необязательный параметр Primary, указывающий, является ли текущая IP-конфигурация основной.</span><span class="sxs-lookup"><span data-stu-id="dd594-269">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="dd594-270">Улучшена обработка исключений из-за ошибок запроса от пакета SDK. Устранена проблема, при которой исключения пакета SDK не обрабатывались правильно, из-за чего не отображались основные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="dd594-270">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="dd594-271">Настроена логика проверки для префикса IPv6 IP-адреса для проверки правильности длины префикса IPv6.</span><span class="sxs-lookup"><span data-stu-id="dd594-271">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="dd594-272">Обновлен Get-AzVirtualNetworkSubnetConfig: добавлен набор параметров для получения по идентификатору ресурса подсети.</span><span class="sxs-lookup"><span data-stu-id="dd594-272">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="dd594-273">Обновлено описание параметра Location для AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="dd594-273">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="dd594-274">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="dd594-274">Az.OperationalInsights</span></span>
* <span data-ttu-id="dd594-275">Обновлена документация по New-AzOperationalInsightsLinuxSyslogDataSource.</span><span class="sxs-lookup"><span data-stu-id="dd594-275">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="dd594-276">Добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="dd594-276">Added example</span></span>
    - <span data-ttu-id="dd594-277">Обновлено описание параметра -Name.</span><span class="sxs-lookup"><span data-stu-id="dd594-277">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="dd594-278">Добавлен пример для New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="dd594-278">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="dd594-279">Изменено описание параметра -Name для New-AzOperationalInsightsWindowsEventDataSource.</span><span class="sxs-lookup"><span data-stu-id="dd594-279">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dd594-280">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dd594-280">Az.RecoveryServices</span></span>
* <span data-ttu-id="dd594-281">Обновлен Get-AzRecoveryServicesBackupJobDetail.md.</span><span class="sxs-lookup"><span data-stu-id="dd594-281">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="dd594-282">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd594-282">Az.Resources</span></span>
* <span data-ttu-id="dd594-283">Добавлена поддержка новой версии API 2019-05-10 для Microsoft.Resource.</span><span class="sxs-lookup"><span data-stu-id="dd594-283">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="dd594-284">Добавлена поддержка copy.count = 0 для переменных, ресурсов и свойств.</span><span class="sxs-lookup"><span data-stu-id="dd594-284">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="dd594-285">Ресурсы, у которых condition = false или copy.count = 0, будут удаляться в полном режиме.</span><span class="sxs-lookup"><span data-stu-id="dd594-285">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="dd594-286">В справочную документацию добавлен пример назначения политики на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="dd594-286">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="dd594-287">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="dd594-287">Az.ServiceBus</span></span>
* <span data-ttu-id="dd594-288">Исправлена проблема № 9658: опечатка в написании параметра VirtualNetworkRule В Set-AzServiceBusNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="dd594-288">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="dd594-289">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="dd594-289">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="dd594-290">Добавлена новая команда Test-AzServiceBusNameAvailability для проверки доступности имени для очереди и раздела.</span><span class="sxs-lookup"><span data-stu-id="dd594-290">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="dd594-291">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dd594-291">Az.ServiceFabric</span></span>
* <span data-ttu-id="dd594-292">Устранены ошибки командлета для добавления типа узла:</span><span class="sxs-lookup"><span data-stu-id="dd594-292">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="dd594-293">ошибка NullReferenceException, возникавшая, если у группы ресурсов были другие VMSS, не связанные с кластером Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="dd594-293">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="dd594-294">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8681.</span><span class="sxs-lookup"><span data-stu-id="dd594-294">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="dd594-295">Исправлена ошибка, из-за которой командлет завершился сбоем, если virtualNetwork находилась не в той группе ресурсов, к которой относится кластер.</span><span class="sxs-lookup"><span data-stu-id="dd594-295">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="dd594-296">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8407.</span><span class="sxs-lookup"><span data-stu-id="dd594-296">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="dd594-297">Командлет Add-AzServiceFabricApplicationCertificate объявлен нерекомендуемым.</span><span class="sxs-lookup"><span data-stu-id="dd594-297">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="dd594-298">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd594-298">Az.Sql</span></span>
* <span data-ttu-id="dd594-299">Обновление документации по старым командлетам аудита.</span><span class="sxs-lookup"><span data-stu-id="dd594-299">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dd594-300">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dd594-300">Az.Storage</span></span>
* <span data-ttu-id="dd594-301">Обновлена справка по Get/Close-AzStorageFileHandle: в примеры добавлены сценарии использования командлетов и обновлено описание параметров.</span><span class="sxs-lookup"><span data-stu-id="dd594-301">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="dd594-302">Добавлена поддержка StandardBlobTier в операции отправки BLOB-объекта и копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="dd594-302">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="dd594-303">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="dd594-303">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="dd594-304">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="dd594-304">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="dd594-305">Добавлена поддержка приоритета восстановления в операцию копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="dd594-305">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="dd594-306">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="dd594-306">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dd594-307">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dd594-307">Az.Websites</span></span>
* <span data-ttu-id="dd594-308">Добавлены уточнение для параметра -AppSettings в Set-AzWebApp и Set-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="dd594-308">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="dd594-309">2.5.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="dd594-309">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dd594-310">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dd594-310">Az.Accounts</span></span>
* <span data-ttu-id="dd594-311">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dd594-311">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="dd594-312">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="dd594-312">Az.ApplicationInsights</span></span>
* <span data-ttu-id="dd594-313">Исправлена опечатка в примере в документации по Remove-AzApplicationInsightsApiKey.</span><span class="sxs-lookup"><span data-stu-id="dd594-313">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="dd594-314">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dd594-314">Az.Automation</span></span>
* <span data-ttu-id="dd594-315">Исправлена опечатка в строке ресурса.</span><span class="sxs-lookup"><span data-stu-id="dd594-315">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="dd594-316">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="dd594-316">Az.CognitiveServices</span></span>
* <span data-ttu-id="dd594-317">Добавлена поддержка NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="dd594-317">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dd594-318">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd594-318">Az.Compute</span></span>
* <span data-ttu-id="dd594-319">Добавлены недостающие свойства (ComputerName, OsName, OsVersion и HyperVGeneration) для объекта представления экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="dd594-319">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="dd594-320">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="dd594-320">Az.ContainerRegistry</span></span>
* <span data-ttu-id="dd594-321">Исправлена опечатка в Remove-AzContainerRegistryReplication для параметра репликации.</span><span class="sxs-lookup"><span data-stu-id="dd594-321">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="dd594-322">См. подробнее: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="dd594-322">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dd594-323">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dd594-323">Az.DataFactory</span></span>
* <span data-ttu-id="dd594-324">Пакет SDK для ADF .NET обновлен до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="dd594-324">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="dd594-325">Исправлена опечатка в документации по Get-AzDataFactoryV2PipelineRun.</span><span class="sxs-lookup"><span data-stu-id="dd594-325">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="dd594-326">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="dd594-326">Az.EventHub</span></span>
* <span data-ttu-id="dd594-327">Добавлен новый командлет для создания маркера SAS: New-AzEventHubAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="dd594-327">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="dd594-328">Добавлена проверка и сообщение об ошибке для случаев, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="dd594-328">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="dd594-329">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dd594-329">Az.KeyVault</span></span>
* <span data-ttu-id="dd594-330">Добавлена поддержка для настройки параметра KeySize в политиках сертификатов.</span><span class="sxs-lookup"><span data-stu-id="dd594-330">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="dd594-331">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="dd594-331">Az.LogicApp</span></span>
* <span data-ttu-id="dd594-332">Get-AzIntegrationAccountMap теперь надлежащим образом выводит все типы сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="dd594-332">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="dd594-333">Добавлен новый параметр MapType для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="dd594-333">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="dd594-334">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="dd594-334">Az.ManagedServices</span></span>
* <span data-ttu-id="dd594-335">Добавлена поддержка API версии 2019-06-01 (общедоступная).</span><span class="sxs-lookup"><span data-stu-id="dd594-335">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dd594-336">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dd594-336">Az.Network</span></span>
* <span data-ttu-id="dd594-337">Добавлена поддержка частной конечной точки и службы приватного канала.</span><span class="sxs-lookup"><span data-stu-id="dd594-337">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="dd594-338">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="dd594-338">New cmdlets</span></span>
        - <span data-ttu-id="dd594-339">Set-AzPrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="dd594-339">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="dd594-340">Set-AzPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="dd594-340">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="dd594-341">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="dd594-341">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="dd594-342">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="dd594-342">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="dd594-343">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="dd594-343">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="dd594-344">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="dd594-344">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="dd594-345">Test-AzPrivateLinkServiceVisibility.</span><span class="sxs-lookup"><span data-stu-id="dd594-345">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="dd594-346">Get-AzAutoApprovedPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="dd594-346">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="dd594-347">Обновлены следующие команды для функции: Флаг PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies в подсети в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="dd594-347">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="dd594-348">Обновлены командлеты New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig.</span><span class="sxs-lookup"><span data-stu-id="dd594-348">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="dd594-349">Добавлен необязательный параметр -PrivateEndpointNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к частной конечной точке в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="dd594-349">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="dd594-350">Добавлен необязательный параметр -PrivateLinkServiceNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к службе приватного канала в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="dd594-350">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="dd594-351">Параметр ServiceName командлета AzPrivateLinkService был переименован на Name с псевдонимом ServiceName для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="dd594-351">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="dd594-352">Включен протокол ICMP для настройки правил безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="dd594-352">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="dd594-353">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="dd594-353">Updated cmdlets</span></span>
        - <span data-ttu-id="dd594-354">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="dd594-354">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="dd594-355">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="dd594-355">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="dd594-356">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="dd594-356">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="dd594-357">Добавлен ConnectionProtocolType (Ikev1/Ikev2) в качестве настраиваемого параметра для командлета New-AzVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="dd594-357">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="dd594-358">Добавлен PrivateIpAddressVersion в LoadBalancerFrontendIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="dd594-358">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="dd594-359">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="dd594-359">Updated cmdlet:</span></span>
        - <span data-ttu-id="dd594-360">New-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="dd594-360">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="dd594-361">Add-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="dd594-361">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="dd594-362">Set-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="dd594-362">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="dd594-363">Команда New-AzApplicationGatewayProbeConfig Шлюза приложений обновлена для поддержки настраиваемого порта в зонде.</span><span class="sxs-lookup"><span data-stu-id="dd594-363">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="dd594-364">Обновлен командлет New-AzApplicationGatewayProbeConfig: добавлен необязательный параметр Port, который используется при проверке внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="dd594-364">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="dd594-365">Этот параметр применяется к номерам SKU Standard_V2 и WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="dd594-365">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="dd594-366">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="dd594-366">Az.OperationalInsights</span></span>
* <span data-ttu-id="dd594-367">Обновленная версия по умолчанию для сохраненных операций поиска имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="dd594-367">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="dd594-368">Исправлены ошибки при обработке регулярных выражений со значениями NULL в журналах.</span><span class="sxs-lookup"><span data-stu-id="dd594-368">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dd594-369">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dd594-369">Az.RecoveryServices</span></span>
* <span data-ttu-id="dd594-370">Обновлен файл Get-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="dd594-370">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="dd594-371">Обновлен файл Get-AzRecoveryServicesBackupContainer.md.</span><span class="sxs-lookup"><span data-stu-id="dd594-371">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="dd594-372">Обновлен файл Get-AzRecoveryServicesVault.md.</span><span class="sxs-lookup"><span data-stu-id="dd594-372">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="dd594-373">Обновлен файл Wait-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="dd594-373">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="dd594-374">Обновлен файл Set-AzRecoveryServicesVaultContext.md.</span><span class="sxs-lookup"><span data-stu-id="dd594-374">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="dd594-375">Обновлен файл Get-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="dd594-375">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="dd594-376">Обновлен файл Get-AzRecoveryServicesBackupRecoveryPoint.md.</span><span class="sxs-lookup"><span data-stu-id="dd594-376">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="dd594-377">Обновлен файл Restore-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="dd594-377">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="dd594-378">Обновлен вызов службы для отмены регистрации контейнера в общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="dd594-378">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="dd594-379">Обновлен файл Set-AzRecoveryServicesAsrAlertSetting.md.</span><span class="sxs-lookup"><span data-stu-id="dd594-379">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="dd594-380">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd594-380">Az.Resources</span></span>
- <span data-ttu-id="dd594-381">Удален отсутствующий командлет, который упоминается в документации по New-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="dd594-381">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="dd594-382">Обновлены командлеты политик для использования новой версии API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="dd594-382">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="dd594-383">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="dd594-383">Az.ServiceBus</span></span>
* <span data-ttu-id="dd594-384">Добавлен новый командлет для создания маркера SAS: New-AzServiceBusAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="dd594-384">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="dd594-385">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="dd594-385">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="dd594-386">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd594-386">Az.Sql</span></span>
* <span data-ttu-id="dd594-387">Исправлены отсутствующие примеры для командлета Set-AzSqlDatabaseSecondary.</span><span class="sxs-lookup"><span data-stu-id="dd594-387">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="dd594-388">Исправлены заданные повторяющиеся проверки для оценки наличия уязвимостей без указания адресов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="dd594-388">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="dd594-389">Исправлена незначительная опечатка в сообщении предупреждения.</span><span class="sxs-lookup"><span data-stu-id="dd594-389">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dd594-390">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dd594-390">Az.Storage</span></span>
* <span data-ttu-id="dd594-391">Обновлен пример в справочной документации для использования командлетом Get-AzStorageAccount правильного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="dd594-391">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="dd594-392">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="dd594-392">Az.StorageSync</span></span>
* <span data-ttu-id="dd594-393">Добавлен командлет Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="dd594-393">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="dd594-394">Исправлена проблема № 9551, связанная с TierFilesOlderThanDays.</span><span class="sxs-lookup"><span data-stu-id="dd594-394">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dd594-395">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dd594-395">Az.Websites</span></span>
* <span data-ttu-id="dd594-396">Исправлена ошибка, при которой некоторые свойства SiteConfig не возвращались Get-AzWebApp и Set-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="dd594-396">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="dd594-397">Добавлен новый параметр Location в Get-AzDeletedWebApp и Restore-AzDeletedWebApp.</span><span class="sxs-lookup"><span data-stu-id="dd594-397">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="dd594-398">Исправлена ошибка, которая возникала при клонировании слотов веб-приложений с помощью командлета New-AzWebApp-IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="dd594-398">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="dd594-399">2.4.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="dd594-399">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dd594-400">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dd594-400">Az.Accounts</span></span>
* <span data-ttu-id="dd594-401">Добавлена поддержка командлетов профиля.</span><span class="sxs-lookup"><span data-stu-id="dd594-401">Add support for profile cmdlets</span></span>
* <span data-ttu-id="dd594-402">Добавлена поддержка сред и плоскостей данных в созданных командлетах.</span><span class="sxs-lookup"><span data-stu-id="dd594-402">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="dd594-403">Исправлена ошибка, когда в командлетах плоскости данных в Windows PowerShell в некоторых случаях использовалась неправильная конечная точка.</span><span class="sxs-lookup"><span data-stu-id="dd594-403">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="dd594-404">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="dd594-404">Az.Advisor</span></span>
* <span data-ttu-id="dd594-405">Выпущена общедоступная версия Az.Advisor.</span><span class="sxs-lookup"><span data-stu-id="dd594-405">GA release of Az.Advisor</span></span>
* <span data-ttu-id="dd594-406">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="dd594-406">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="dd594-407">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="dd594-407">Az.ApiManagement</span></span>
* <span data-ttu-id="dd594-408">исправлена проблема https://github.com/Azure/azure-powershell/issues/8671.</span><span class="sxs-lookup"><span data-stu-id="dd594-408">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="dd594-409">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="dd594-409">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="dd594-410">Добавлена поддержка запрашивания подписок по пользователю и продукту.</span><span class="sxs-lookup"><span data-stu-id="dd594-410">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="dd594-411">Добавлена поддержка создания запросов с использованием области "/", "/apis", "/apis/echo-api".</span><span class="sxs-lookup"><span data-stu-id="dd594-411">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="dd594-412">Исправлены проблемы https://github.com/Azure/azure-powershell/issues/9307 и https://github.com/Azure/azure-powershell/issues/8432.</span><span class="sxs-lookup"><span data-stu-id="dd594-412">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="dd594-413">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="dd594-413">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="dd594-414">Добавлена поддержка указания ApiVersion и ApiVersionSetId при импорте API-интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="dd594-414">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="dd594-415">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dd594-415">Az.Automation</span></span>
* <span data-ttu-id="dd594-416">Исправлена ошибка командлета Set-AzAutomationConnectionFieldValue при обработке строкового значения.</span><span class="sxs-lookup"><span data-stu-id="dd594-416">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dd594-417">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd594-417">Az.Compute</span></span>
* <span data-ttu-id="dd594-418">В New AzImageConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="dd594-418">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dd594-419">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dd594-419">Az.DataFactory</span></span>
* <span data-ttu-id="dd594-420">Обновление выходных данных командлетов ADF, предназначенных для получения числа выполнений действий, конвейеров и триггеров, для поддержки канала Select-Object.</span><span class="sxs-lookup"><span data-stu-id="dd594-420">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="dd594-421">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="dd594-421">Az.EventGrid</span></span>
* <span data-ttu-id="dd594-422">Исправлена опечатка в документации по командлету New-AzEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="dd594-422">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="dd594-423">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="dd594-423">Az.IotHub</span></span>
* <span data-ttu-id="dd594-424">Добавлена поддержка повторного создания ключей политики авторизации.</span><span class="sxs-lookup"><span data-stu-id="dd594-424">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dd594-425">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dd594-425">Az.Network</span></span>
* <span data-ttu-id="dd594-426">К тегам общедоступного IP-адреса добавлен тег RoutingPreference.</span><span class="sxs-lookup"><span data-stu-id="dd594-426">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="dd594-427">Улучшены примеры для справочной документации по командлету Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="dd594-427">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="dd594-428">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="dd594-428">Az.PolicyInsights</span></span>
* <span data-ttu-id="dd594-429">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="dd594-429">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="dd594-430">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9446.</span><span class="sxs-lookup"><span data-stu-id="dd594-430">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="dd594-431">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="dd594-431">Az.OperationalInsights</span></span>
* <span data-ttu-id="dd594-432">Исправленная модель источника данных CustomLog возвращена в командлет Get-AzOperationalInsightsDataSource.</span><span class="sxs-lookup"><span data-stu-id="dd594-432">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dd594-433">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dd594-433">Az.RecoveryServices</span></span>
* <span data-ttu-id="dd594-434">Выпущено исправление для команды get-policy для виртуальных машин IaaS.</span><span class="sxs-lookup"><span data-stu-id="dd594-434">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="dd594-435">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd594-435">Az.Resources</span></span>
    - <span data-ttu-id="dd594-436">Исправлен текст справки по параметру Get-AzPolicyState -Top.</span><span class="sxs-lookup"><span data-stu-id="dd594-436">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="dd594-437">Добавлена поддержка разбиения по страницам на стороне клиента для Get-AzPolicyAlias.</span><span class="sxs-lookup"><span data-stu-id="dd594-437">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="dd594-438">Добавлены новые параметры для Set-AzPolicyAssignment, -PolicyParameters и -PolicyParametersObject.</span><span class="sxs-lookup"><span data-stu-id="dd594-438">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="dd594-439">Добавлен ряд обновлений документов и примеров для командлетов политик.</span><span class="sxs-lookup"><span data-stu-id="dd594-439">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="dd594-440">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="dd594-440">Az.ServiceBus</span></span>
* <span data-ttu-id="dd594-441">Исправление ошибки № 4938: командлет New-AzureRmServiceBusQueue возвращает ответ BadRequest (Недопустимый запрос) при задании значения MaxSizeInMegabytes.</span><span class="sxs-lookup"><span data-stu-id="dd594-441">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="dd594-442">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd594-442">Az.Sql</span></span>
* <span data-ttu-id="dd594-443">Из выпуска предварительной версии в выпуск общедоступной версии добавлены командлеты группы отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="dd594-443">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="dd594-444">Поддержка аудита Azure SQL Server и баз данных с помощью новых командлетов:</span><span class="sxs-lookup"><span data-stu-id="dd594-444">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="dd594-445">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="dd594-445">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="dd594-446">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="dd594-446">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="dd594-447">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="dd594-447">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="dd594-448">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="dd594-448">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="dd594-449">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="dd594-449">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="dd594-450">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="dd594-450">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="dd594-451">Из параметров оценки уязвимостей удалены ограничения, касающиеся электронной почты.</span><span class="sxs-lookup"><span data-stu-id="dd594-451">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dd594-452">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dd594-452">Az.Storage</span></span>
* <span data-ttu-id="dd594-453">Два параметра в указанном ниже командлете — -IndexDocument и -ErrorDocument404Path, — которые ранее были обязательными, стали необязательными:</span><span class="sxs-lookup"><span data-stu-id="dd594-453">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="dd594-454">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="dd594-454">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="dd594-455">Обновлена справка по командлету Get-AzStorageBlobContent: добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="dd594-455">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="dd594-456">При сбое выполнения командлета с ошибкой StorageException отображаются дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="dd594-456">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="dd594-457">Добавлена поддержка создания или обновления учетной записи хранения с использованием проверки подлинности AAD DS для службы "Файлы Azure".</span><span class="sxs-lookup"><span data-stu-id="dd594-457">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="dd594-458">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dd594-458">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="dd594-459">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dd594-459">Set-AzStorageAccount</span></span>
* <span data-ttu-id="dd594-460">Добавлена поддержка перечисления или закрытия дескрипторов файлов для общей папки, каталога файлов или файла:</span><span class="sxs-lookup"><span data-stu-id="dd594-460">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="dd594-461">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="dd594-461">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="dd594-462">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="dd594-462">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="dd594-463">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="dd594-463">Az.StorageSync</span></span>
* <span data-ttu-id="dd594-464">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="dd594-464">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="dd594-465">2.3.2 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="dd594-465">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dd594-466">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dd594-466">Az.Accounts</span></span>
* <span data-ttu-id="dd594-467">Исправлена ошибка, связанная с использованием неправильного URL-адреса для вызовов функций.</span><span class="sxs-lookup"><span data-stu-id="dd594-467">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="dd594-468">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8983.</span><span class="sxs-lookup"><span data-stu-id="dd594-468">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="dd594-469">Устранена проблема с псевдонимами из AzureRM для командлетов Az.</span><span class="sxs-lookup"><span data-stu-id="dd594-469">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="dd594-470">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="dd594-470">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="dd594-471">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest.</span><span class="sxs-lookup"><span data-stu-id="dd594-471">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dd594-472">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd594-472">Az.Compute</span></span>
* <span data-ttu-id="dd594-473">Простые наборы параметров New-AzVm и New-AzVmss теперь принимают параметр ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="dd594-473">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="dd594-474">Исправлена опечатка в справочной документации по New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="dd594-474">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="dd594-475">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="dd594-475">Az.Dns</span></span>
* <span data-ttu-id="dd594-476">Исправлена опечатка в справочных примерах по использованию Set-AzDnsZone.</span><span class="sxs-lookup"><span data-stu-id="dd594-476">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="dd594-477">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="dd594-477">Az.EventGrid</span></span>
* <span data-ttu-id="dd594-478">Обновлен для использования API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="dd594-478">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="dd594-479">Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="dd594-479">New cmdlets:</span></span>
    - <span data-ttu-id="dd594-480">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="dd594-480">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="dd594-481">Создает домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="dd594-481">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="dd594-482">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="dd594-482">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="dd594-483">Возвращает сведения о домене Сетки событий или список всех доменов Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="dd594-483">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="dd594-484">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="dd594-484">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="dd594-485">Удаляет домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="dd594-485">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="dd594-486">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="dd594-486">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="dd594-487">Повторно создает ключ общего доступа для домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="dd594-487">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="dd594-488">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="dd594-488">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="dd594-489">Возвращает ключи общего доступа, используемые для публикации событий в домене Сетки событий.</span><span class="sxs-lookup"><span data-stu-id="dd594-489">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="dd594-490">New-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="dd594-490">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="dd594-491">Создает раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="dd594-491">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="dd594-492">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="dd594-492">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="dd594-493">Возвращает сведения о разделе домена Сетки событий или список всех разделов определенного домена Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="dd594-493">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="dd594-494">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="dd594-494">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="dd594-495">Удаляет раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="dd594-495">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="dd594-496">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="dd594-496">Updated cmdlets:</span></span>
    - <span data-ttu-id="dd594-497">New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="dd594-497">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="dd594-498">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для нового домена Сетки событий и раздела домена Сетки событий и позволяющие создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="dd594-498">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="dd594-499">Добавляют новые обязательные параметры для указания имени нового домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="dd594-499">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="dd594-500">Добавляют новые наборы параметров для доменов и разделов домена и позволяют повторно использовать существующие параметры (например, EndPointType, SubjectBeginsWith и т. д.).</span><span class="sxs-lookup"><span data-stu-id="dd594-500">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="dd594-501">Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="dd594-501">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="dd594-502">срока действия подписки на событие;</span><span class="sxs-lookup"><span data-stu-id="dd594-502">Event subscription expiration date,</span></span>
            - <span data-ttu-id="dd594-503">параметров расширенной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="dd594-503">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="dd594-504">Добавляют новое перечисление для ServiceBusQueue в качестве места назначения.</span><span class="sxs-lookup"><span data-stu-id="dd594-504">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="dd594-505">Запрещают использование значение All в параметре -IncludedEventType и заменяют его следующим:</span><span class="sxs-lookup"><span data-stu-id="dd594-505">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="dd594-506">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="dd594-506">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="dd594-507">Добавляют новые необязательные параметры (Top, ODataQuery и NextLink) для поддержки разбиения на страницы и фильтрации результатов.</span><span class="sxs-lookup"><span data-stu-id="dd594-507">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="dd594-508">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="dd594-508">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="dd594-509">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для домена Сетки событий и раздела домена Сетки событий и позволяющие удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="dd594-509">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="dd594-510">Добавляют новые обязательные параметры для указания имени домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="dd594-510">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="dd594-511">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="dd594-511">Az.FrontDoor</span></span>
* <span data-ttu-id="dd594-512">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="dd594-512">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="dd594-513">Добавляет поддержку преобразований и новое значение оператора автозавершения (RegEx).</span><span class="sxs-lookup"><span data-stu-id="dd594-513">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="dd594-514">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="dd594-514">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="dd594-515">Добавляет новые значения автозавершения.</span><span class="sxs-lookup"><span data-stu-id="dd594-515">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dd594-516">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dd594-516">Az.Network</span></span>
* <span data-ttu-id="dd594-517">Добавляет поддержку ресурса шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="dd594-517">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="dd594-518">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="dd594-518">New cmdlets</span></span>
        - <span data-ttu-id="dd594-519">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="dd594-519">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="dd594-520">Добавляет AvailablePrivateEndpointType.</span><span class="sxs-lookup"><span data-stu-id="dd594-520">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="dd594-521">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="dd594-521">New cmdlets</span></span> 
        - <span data-ttu-id="dd594-522">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="dd594-522">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="dd594-523">Добавляет PrivatePrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="dd594-523">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="dd594-524">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="dd594-524">New cmdlets</span></span> 
        - <span data-ttu-id="dd594-525">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="dd594-525">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="dd594-526">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="dd594-526">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="dd594-527">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="dd594-527">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="dd594-528">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="dd594-528">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="dd594-529">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dd594-529">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="dd594-530">Добавляет PrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="dd594-530">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="dd594-531">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="dd594-531">New cmdlets</span></span>
        - <span data-ttu-id="dd594-532">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="dd594-532">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="dd594-533">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="dd594-533">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="dd594-534">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="dd594-534">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="dd594-535">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="dd594-535">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="dd594-536">Обновлены следующие команды для функции: флаг UseLocalAzureIpAddress для VPN-подключения.</span><span class="sxs-lookup"><span data-stu-id="dd594-536">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="dd594-537">Обновлен командлет New-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="dd594-537">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="dd594-538">Обновлен командлет Set-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="dd594-538">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="dd594-539">В пиринг ExpressRoute добавлено поле только для чтения PeeredConnections.</span><span class="sxs-lookup"><span data-stu-id="dd594-539">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="dd594-540">В ExpressRoute добавлено поле только для чтения GlobalReachEnabled.</span><span class="sxs-lookup"><span data-stu-id="dd594-540">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="dd594-541">Добавлен атрибут в рамках критического изменения, отменяющего статус устаревшего поля AllowGlobalReach в модели ExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="dd594-541">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="dd594-542">Исправлена проблема, связанная с ошибкой 8756, при использовании TargetListenerID с командлетами AzApplicationGatewayRedirectConfiguration.</span><span class="sxs-lookup"><span data-stu-id="dd594-542">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="dd594-543">Исправлена ошибка в New-AzApplicationGatewayPathRuleConfig, не позволявшая задавать набор правил повторного создания.</span><span class="sxs-lookup"><span data-stu-id="dd594-543">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="dd594-544">Исправлено отображение VirtualNetworkTaps в NetworkInterfaceIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="dd594-544">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="dd594-545">Исправлены командлеты Cortex Get для отображения всех частей.</span><span class="sxs-lookup"><span data-stu-id="dd594-545">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="dd594-546">Исправлено создание ссылок VirtualHub для ExpressRouteGateways и VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="dd594-546">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="dd594-547">В AzureFirewall и NatGateway добавлена поддержка Зон доступности.</span><span class="sxs-lookup"><span data-stu-id="dd594-547">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="dd594-548">Добавлен командлет Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="dd594-548">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="dd594-549">Добавлена поддержка нескольких общедоступных IP-адресов для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="dd594-549">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="dd594-550">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="dd594-550">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="dd594-551">Добавлен параметр -PublicIpAddress, который принимает один или несколько объектов общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="dd594-551">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="dd594-552">Добавлен параметр -VirtualNetwork, который принимает объект виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="dd594-552">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="dd594-553">Добавлены методы AddPublicIpAddress и RemovePublicIpAddress для объекта брандмауэра. Они принимают объект общедоступного IP-адреса в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="dd594-553">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="dd594-554">Не рекомендуется использовать параметры -PublicIpName и -VirtualNetworkName.</span><span class="sxs-lookup"><span data-stu-id="dd594-554">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="dd594-555">Обновлены следующие команды для функции: В параметрах проверки подлинности AAD VPN-клиента задан ресурс шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="dd594-555">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="dd594-556">Обновлен командлет New-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="dd594-556">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="dd594-557">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="dd594-557">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="dd594-558">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр-переключатель RemoveAadAuthentication для удаления в шлюзе параметров проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="dd594-558">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="dd594-559">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="dd594-559">Az.OperationalInsights</span></span>
* <span data-ttu-id="dd594-560">Добавлена поддержка SKU **pergb2018** в команде New-AzureRmOperationalInsightsWorkspace.</span><span class="sxs-lookup"><span data-stu-id="dd594-560">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="dd594-561">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd594-561">Az.Resources</span></span>
* <span data-ttu-id="dd594-562">Поддержка дополнительных вариантов экспорта шаблона.</span><span class="sxs-lookup"><span data-stu-id="dd594-562">Support for additional Template Export options</span></span>
    - <span data-ttu-id="dd594-563">В Export-AzResourceGroup добавлен параметр -SkipResourceNameParameterization.</span><span class="sxs-lookup"><span data-stu-id="dd594-563">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="dd594-564">В Export-AzResourceGroup добавлен параметр -SkipAllParameterization.</span><span class="sxs-lookup"><span data-stu-id="dd594-564">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="dd594-565">В Export-AzResourceGroup добавлен параметр -Resource для фильтрации экспортированных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dd594-565">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="dd594-566">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dd594-566">Az.ServiceFabric</span></span>
* <span data-ttu-id="dd594-567">Исправлена ошибка, связанная с получением иногда неправильных отпечатков при добавлении сертификата ByExistingKeyVault.</span><span class="sxs-lookup"><span data-stu-id="dd594-567">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="dd594-568">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd594-568">Az.Sql</span></span>
* <span data-ttu-id="dd594-569">Исправлен суффикс конечной точки хранилища службы "Расширенная защита от угроз Azure".</span><span class="sxs-lookup"><span data-stu-id="dd594-569">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="dd594-570">Исправлена ошибка, связанная с возможностью пакета "Расширенная защита данных" переопределять политику службы "Расширенная защита от угроз".</span><span class="sxs-lookup"><span data-stu-id="dd594-570">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="dd594-571">Новые командлеты для Management.Sql позволяют клиентам добавлять ключи TDE и задавать средство защиты TDE для управляемых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="dd594-571">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="dd594-572">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="dd594-572">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="dd594-573">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="dd594-573">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="dd594-574">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="dd594-574">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="dd594-575">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="dd594-575">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="dd594-576">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="dd594-576">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dd594-577">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dd594-577">Az.Storage</span></span>
* <span data-ttu-id="dd594-578">Поддержка класса Kind в FileStorage и значения Premium_ZRS в SkuName при создании учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="dd594-578">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="dd594-579">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dd594-579">New-AzStorageAccount</span></span>
* <span data-ttu-id="dd594-580">Уточнено описание командлета неизменности BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="dd594-580">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="dd594-581">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="dd594-581">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dd594-582">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dd594-582">Az.Websites</span></span>
* <span data-ttu-id="dd594-583">Оптимизирует Get-AzWebAppCertificate для фильтрации по группе ресурсов на сервере, а не в клиенте.</span><span class="sxs-lookup"><span data-stu-id="dd594-583">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="dd594-584">Добавляет параметр-переключатель - UseDisasterRecovery в Get AzWebAppSnapshot.</span><span class="sxs-lookup"><span data-stu-id="dd594-584">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="dd594-585">2.2.0 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="dd594-585">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="dd594-586">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="dd594-586">Az.Cdn</span></span>
* <span data-ttu-id="dd594-587">Обновлены командлеты для поддержки функции rulesEngine на основе API версии 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="dd594-587">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dd594-588">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd594-588">Az.Compute</span></span>
* <span data-ttu-id="dd594-589">Добавлен параметр `NoWait`, который запускает операцию и немедленно возвращает значение еще до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="dd594-589">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="dd594-590">Обновлены командлеты:   Export-AzLogAnalyticRequestRateByInterval; Export-AzLogAnalyticThrottledRequest; Remove-AzVM; Remove-AzVMAccessExtension; Remove-AzVMAEMExtension; Remove-AzVMChefExtension; Remove-AzVMCustomScriptExtension; Remove-AzVMDiagnosticsExtension; Remove-AzVMDiskEncryptionExtension; Remove-AzVMDscExtension; Remove-AzVMSqlServerExtension; Restart-AzVM; Set-AzVM; Set-AzVMAccessExtension; Set-AzVMADDomainExtension; Set-AzVMAEMExtension; Set-AzVMBginfoExtension; Set-AzVMChefExtension; Set-AzVMCustomScriptExtension; Set-AzVMDiagnosticsExtension; Set-AzVMDscExtension; Set-AzVMExtension; Start-AzVM; Stop-AzVM; Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="dd594-590">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="dd594-591">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="dd594-591">Az.EventHub</span></span>
* <span data-ttu-id="dd594-592">Исправлена ошибка № 9231. Командлет Get-AzEventHubNamespace не возвращал теги.</span><span class="sxs-lookup"><span data-stu-id="dd594-592">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="dd594-593">Исправлена ошибка № 9230. Командлет Get-AzEventHubNamespace возвращал значение ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="dd594-593">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dd594-594">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dd594-594">Az.Network</span></span>
* <span data-ttu-id="dd594-595">Обновлены параметры ResourceId и InputObject для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="dd594-595">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="dd594-596">Добавлены псевдонимы для параметров ResourceId и InputObject.</span><span class="sxs-lookup"><span data-stu-id="dd594-596">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="dd594-597">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="dd594-597">Az.PolicyInsights</span></span>
* <span data-ttu-id="dd594-598">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyEvent.</span><span class="sxs-lookup"><span data-stu-id="dd594-598">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dd594-599">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dd594-599">Az.RecoveryServices</span></span>
* <span data-ttu-id="dd594-600">Минимальный срок хранения политики IaaSVM изменился с 1 до 7 дней.</span><span class="sxs-lookup"><span data-stu-id="dd594-600">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="dd594-601">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="dd594-601">Az.ServiceBus</span></span>
* <span data-ttu-id="dd594-602">Исправлена ошибка № 9182. Командлет Get-AzServiceBusNamespace возвращал ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="dd594-602">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="dd594-603">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dd594-603">Az.ServiceFabric</span></span>
* <span data-ttu-id="dd594-604">Исправлена опечатка в сообщении об ошибке для командлета Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="dd594-604">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="dd594-605">Исправлен отсутствующей символ в командных строках Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="dd594-605">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="dd594-606">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd594-606">Az.Sql</span></span>
* <span data-ttu-id="dd594-607">Для командлета New-AzureSqlInstance добавлен параметр DnsZonePartner, обеспечивающий поддержку AutoDr для Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="dd594-607">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="dd594-608">Командлет Get-AzSqlDatabaseSecureConnectionPolicy объявлен неподдерживаемым.</span><span class="sxs-lookup"><span data-stu-id="dd594-608">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="dd594-609">Командлеты обнаружения угроз переименованы в командлеты Расширенной защиты от угроз.</span><span class="sxs-lookup"><span data-stu-id="dd594-609">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="dd594-610">Параметры -StorageSizeInGB и -LicenseType командлета New-AzSqlInstance теперь необязательны.</span><span class="sxs-lookup"><span data-stu-id="dd594-610">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dd594-611">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dd594-611">Az.Websites</span></span>
* <span data-ttu-id="dd594-612">Исправлены проблемы, когда удалялись теги при использовании Set-AzWebApp и Set-AzWebAppSlot со свойством -WebApp.</span><span class="sxs-lookup"><span data-stu-id="dd594-612">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="dd594-613">2.1.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="dd594-613">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="dd594-614">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="dd594-614">Az.ApiManagement</span></span>
* <span data-ttu-id="dd594-615">Созданы командлеты для управления диагностикой в глобальной области и в области API.</span><span class="sxs-lookup"><span data-stu-id="dd594-615">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="dd594-616">**Get-AzApiManagementDiagnostic** — получение диагностики, заданной глобально или на уровне области API.</span><span class="sxs-lookup"><span data-stu-id="dd594-616">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="dd594-617">**New-AzApiManagementDiagnostic** — создание диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="dd594-617">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="dd594-618">**New-AzApiManagementHttpMessageDiagnostic** — создание параметра диагностики, для которого регистрируются заголовки и размер байтов тела.</span><span class="sxs-lookup"><span data-stu-id="dd594-618">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="dd594-619">**New-AzApiManagementPipelineDiagnosticSetting** — создание параметров диагностики для сообщений HTTP, поступающих в шлюз или исходящих из него.</span><span class="sxs-lookup"><span data-stu-id="dd594-619">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="dd594-620">**New-AzApiManagementSamplingSetting** — создание параметра выборки для запросов и ответов касательно диагностики.</span><span class="sxs-lookup"><span data-stu-id="dd594-620">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="dd594-621">**Remove-AzApiManagementDiagnostic** — удаление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="dd594-621">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="dd594-622">**Set-AzApiManagementDiagnostic** — обновление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="dd594-622">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="dd594-623">Созданы командлеты для управления кэшем в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="dd594-623">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="dd594-624">**Get-AzApiManagementCache** — получение сведений о кэше, указанном идентификатором, или обо всех кэшах.</span><span class="sxs-lookup"><span data-stu-id="dd594-624">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="dd594-625">**New-AzApiManagementCache** — создание кэша по умолчанию или кэша в определенном регионе Azure.</span><span class="sxs-lookup"><span data-stu-id="dd594-625">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="dd594-626">**Remove-AzApiManagementCache** — удаление кэша.</span><span class="sxs-lookup"><span data-stu-id="dd594-626">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="dd594-627">**Update-AzApiManagementCache** — обновление кэша.</span><span class="sxs-lookup"><span data-stu-id="dd594-627">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="dd594-628">Созданы командлеты для управления схемой API.</span><span class="sxs-lookup"><span data-stu-id="dd594-628">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="dd594-629">**New-AzApiManagementSchema** — создание схемы для API.</span><span class="sxs-lookup"><span data-stu-id="dd594-629">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="dd594-630">**Get-AzApiManagementSchema** — получение схем, настроенных в API.</span><span class="sxs-lookup"><span data-stu-id="dd594-630">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="dd594-631">**Remove-AzApiManagementSchema** — удаление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="dd594-631">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="dd594-632">**Set-AzApiManagementSchema** — обновление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="dd594-632">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="dd594-633">Создан командлет для создания токена пользователя.</span><span class="sxs-lookup"><span data-stu-id="dd594-633">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="dd594-634">**New-AzApiManagementUserToken** — создание токена пользователя, по умолчанию действительного в течение 8 часов. С помощью этого командлета можно создавать токен для пользователя GIT.</span><span class="sxs-lookup"><span data-stu-id="dd594-634">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="dd594-635">Создан командлет для получения состояния сети.</span><span class="sxs-lookup"><span data-stu-id="dd594-635">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="dd594-636">**Get-AzApiManagementNetworkStatus** — получение состояния сети ресурсов, от которых зависит служба "Управление API".</span><span class="sxs-lookup"><span data-stu-id="dd594-636">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="dd594-637">Это полезно при развертывании службы ApiManagement в виртуальной сети и проверке того, не нарушена ли какая-либо из зависимостей.</span><span class="sxs-lookup"><span data-stu-id="dd594-637">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="dd594-638">Обновлен командлет **New-AzApiManagement** для управления службой ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="dd594-638">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="dd594-639">Добавлена поддержка нового SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="dd594-639">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="dd594-640">Добавлена поддержка для включения флага EnableClientCertificate в SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="dd594-640">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="dd594-641">Новый командлет **New-AzApiManagementSslSetting** позволяет настраивать параметр TLS/SSL для сервера (Backend) и внешнего интерфейса (Frontend).</span><span class="sxs-lookup"><span data-stu-id="dd594-641">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="dd594-642">Его также можно использовать для настройки Ciphers как 3DES, в ServerProtocols как Http2 для внешнего интерфейса (Frontend) службы ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="dd594-642">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="dd594-643">Добавлена поддержка настройки имени узла DeveloperPortal в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="dd594-643">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="dd594-644">Обновлен командлет **Get-AzApiManagementSsoToken** для извлечения объекта PsApiManagement в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="dd594-644">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="dd594-645">Обновлен командлет для отображения встроенных сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="dd594-645">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="dd594-646">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Код ошибки: ValidationError. Сообщение об ошибке: "Некоторые поля содержат неправильные значения". Сведения об ошибке: [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="dd594-646">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="dd594-647">Обновлен командлет **Export-AzApiManagementApi** для экспортирования программных интерфейсов в формате OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="dd594-647">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="dd594-648">Обновлен командлет **Import-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="dd594-648">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="dd594-649">Для импортирования API из спецификации документа OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="dd594-649">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="dd594-650">Для переопределения свойства PsApiManagementSchema, указанного в любом документе (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="dd594-650">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="dd594-651">Для переопределения свойства ServiceUrl, указанного в любом документе.</span><span class="sxs-lookup"><span data-stu-id="dd594-651">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="dd594-652">Обновлен командлет **Get-AzApiManagementPolicy** для возврата политики в формате, экранированном не для XML, с использованием rawxml.</span><span class="sxs-lookup"><span data-stu-id="dd594-652">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="dd594-653">Обновлен командлет **Set-AzApiManagementPolicy**. Он принимает политику в формате, экранированном не для XML, с использованием rawxml и в формате, экранированном для XML, с использованием XML.</span><span class="sxs-lookup"><span data-stu-id="dd594-653">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="dd594-654">Обновлен командлет **New-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="dd594-654">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="dd594-655">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="dd594-655">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="dd594-656">Для создания API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="dd594-656">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="dd594-657">Для клонирования API с использованием значений SourceApiId и SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="dd594-657">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="dd594-658">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="dd594-658">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="dd594-659">Обновлен командлет **Set-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="dd594-659">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="dd594-660">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="dd594-660">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="dd594-661">Для обновления API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="dd594-661">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="dd594-662">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="dd594-662">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="dd594-663">Обновлен командлет **New-AzApiManagementRevision**:</span><span class="sxs-lookup"><span data-stu-id="dd594-663">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="dd594-664">Для клонирования (копирования тегов, продуктов, операций и политик) существующей редакции с использованием SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="dd594-664">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="dd594-665">Новая редакция предполагает родительский идентификатор ApiId.</span><span class="sxs-lookup"><span data-stu-id="dd594-665">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="dd594-666">Для предоставления ApiRevisionDescription.</span><span class="sxs-lookup"><span data-stu-id="dd594-666">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="dd594-667">Для переопределения значения ServiceUrl при клонировании API.</span><span class="sxs-lookup"><span data-stu-id="dd594-667">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="dd594-668">Обновлен командлет **New-AzApiManagementIdentityProvider**:</span><span class="sxs-lookup"><span data-stu-id="dd594-668">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="dd594-669">Для настройки AAD или AADB2C с Authority.</span><span class="sxs-lookup"><span data-stu-id="dd594-669">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="dd594-670">Для установки политик SignupPolicy, SigninPolicy, ProfileEditingPolicy и PasswordResetPolicy.</span><span class="sxs-lookup"><span data-stu-id="dd594-670">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="dd594-671">Обновлен командлет **New-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="dd594-671">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="dd594-672">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="dd594-672">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="dd594-673">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="dd594-673">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="dd594-674">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="dd594-674">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="dd594-675">Обновлен командлет **Set-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="dd594-675">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="dd594-676">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="dd594-676">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="dd594-677">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="dd594-677">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="dd594-678">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="dd594-678">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="dd594-679">Следующие командлеты обновлены, чтобы принимать значение ResourceId в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="dd594-679">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="dd594-680">New-AzApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="dd594-680">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="dd594-681">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="dd594-681">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="dd594-682">Get-AzApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="dd594-682">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="dd594-683">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="dd594-683">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="dd594-684">Get-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="dd594-684">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="dd594-685">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="dd594-685">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="dd594-686">Get-AzApiManagementAuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="dd594-686">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="dd594-687">Get-AzApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="dd594-687">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="dd594-688">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="dd594-688">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="dd594-689">Get-AzApiManagementCertificate.</span><span class="sxs-lookup"><span data-stu-id="dd594-689">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="dd594-690">Remove-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="dd594-690">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="dd594-691">Remove-AzApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="dd594-691">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="dd594-692">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dd594-692">Az.Automation</span></span>
* <span data-ttu-id="dd594-693">Обновлен командлет Get-AzAutomationJobOutputRecord для обработки значений в формате JSON и в виде текстовой записи.</span><span class="sxs-lookup"><span data-stu-id="dd594-693">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="dd594-694">исправлена проблема https://github.com/Azure/azure-powershell/issues/7977.</span><span class="sxs-lookup"><span data-stu-id="dd594-694">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="dd594-695">исправлена проблема https://github.com/Azure/azure-powershell/issues/8600.</span><span class="sxs-lookup"><span data-stu-id="dd594-695">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="dd594-696">Поведение командлета Start-AzAutomationDscCompilationJob изменено так, чтобы сразу же запустить задание, а не ждать его завершения.</span><span class="sxs-lookup"><span data-stu-id="dd594-696">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="dd594-697">исправлена проблема https://github.com/Azure/azure-powershell/issues/8347.</span><span class="sxs-lookup"><span data-stu-id="dd594-697">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="dd594-698">Исправлен командлет Get-AzAutomationDscNode, возвращающий все узлы при использовании -Name.</span><span class="sxs-lookup"><span data-stu-id="dd594-698">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="dd594-699">Теперь он возвращает только соответствующий узел.</span><span class="sxs-lookup"><span data-stu-id="dd594-699">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dd594-700">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd594-700">Az.Compute</span></span>
* <span data-ttu-id="dd594-701">Добавлены параметры ProtectFromScaleIn и ProtectFromScaleSetAction для командлета Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="dd594-701">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="dd594-702">Командлет New-AzVM с простым набором параметров теперь по умолчанию использует доступное расположение, если регион "восточная часть США" не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="dd594-702">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="dd594-703">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dd594-703">Az.DataLakeStore</span></span>
* <span data-ttu-id="dd594-704">Обновлен пакет SDK ADLS для использования httpclient. В инфраструктуру Azure интегрирована проверка плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="dd594-704">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="dd594-705">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dd594-705">Az.Monitor</span></span>
* <span data-ttu-id="dd594-706">Исправлены неправильные имена параметров в справочных примерах.</span><span class="sxs-lookup"><span data-stu-id="dd594-706">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dd594-707">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dd594-707">Az.Network</span></span>
* <span data-ttu-id="dd594-708">Добавлен флаг DisableBgpRoutePropagation для выходных данных действующей таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="dd594-708">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="dd594-709">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="dd594-709">Updated cmdlet:</span></span>
        - <span data-ttu-id="dd594-710">Get-AzEffectiveRouteTable.</span><span class="sxs-lookup"><span data-stu-id="dd594-710">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="dd594-711">Исправлен двойной дефис в документации New-AzApplicationGatewayTrustedRootCertificate.</span><span class="sxs-lookup"><span data-stu-id="dd594-711">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="dd594-712">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd594-712">Az.Resources</span></span>
* <span data-ttu-id="dd594-713">Добавлен новый командлет Get-AzureRmDenyAssignment для получения запрещающих назначений.</span><span class="sxs-lookup"><span data-stu-id="dd594-713">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="dd594-714">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd594-714">Az.Sql</span></span>
* <span data-ttu-id="dd594-715">Командлеты Расширенной защиты от угроз переименованы на командлеты Расширенной защиты данных, и оценка уязвимости включена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="dd594-715">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="dd594-716">2.0.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="dd594-716">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dd594-717">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dd594-717">Az.Accounts</span></span>
* <span data-ttu-id="dd594-718">Обновлена библиотека аутентификации для устранения проблем с ADFS при использовании аутентификации на основе имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="dd594-718">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="dd594-719">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="dd594-719">Az.CognitiveServices</span></span>
* <span data-ttu-id="dd594-720">Отображается только заявление об отказе Bing для служб Поиска Bing.</span><span class="sxs-lookup"><span data-stu-id="dd594-720">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="dd594-721">Исправлена проблема с созданием учетной записи.</span><span class="sxs-lookup"><span data-stu-id="dd594-721">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dd594-722">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd594-722">Az.Compute</span></span>
* <span data-ttu-id="dd594-723">Функция группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="dd594-723">Proximity placement group feature.</span></span>
    - <span data-ttu-id="dd594-724">Добавлены следующие новые командлеты:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="dd594-724">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="dd594-725">Новый параметр ProximityPlacementGroupId будет добавлен в следующие командлеты:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="dd594-725">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="dd594-726">В командлет New-AzGalleryImageVersion добавлен параметр StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="dd594-726">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="dd594-727">TargetRegion в командлете New-AzGalleryImageVersion может содержать StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="dd594-727">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="dd594-728">Параметр-переключатель SkipShutdown добавлен в командлеты Stop-AzVM и Stop-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="dd594-728">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="dd594-729">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="dd594-729">Breaking changes</span></span>
    - <span data-ttu-id="dd594-730">Командлет SET-AzVMBootDiagnostics изменен на Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="dd594-730">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="dd594-731">Командлет Export-AzLogAnalyticThrottledRequests изменен на Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="dd594-731">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="dd594-732">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="dd594-732">Az.DeploymentManager</span></span>
* <span data-ttu-id="dd594-733">Первая общедоступная версия командлетов диспетчера развертывания Azure</span><span class="sxs-lookup"><span data-stu-id="dd594-733">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="dd594-734">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="dd594-734">Az.Dns</span></span>
* <span data-ttu-id="dd594-735">Автоматическое делегирование DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="dd594-735">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="dd594-736">Командлет для создания зоны DNS принимает имя родительской зоны в качестве дополнительного необязательного параметра.</span><span class="sxs-lookup"><span data-stu-id="dd594-736">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="dd594-737">Он добавляет записи NS в родительской зоне для созданной дочерней зоны.</span><span class="sxs-lookup"><span data-stu-id="dd594-737">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="dd594-738">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="dd594-738">Az.FrontDoor</span></span>
* <span data-ttu-id="dd594-739">Первая общедоступная версия командлетов Azure FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="dd594-739">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="dd594-740">Переименованы командлеты WAF для включения Waf.</span><span class="sxs-lookup"><span data-stu-id="dd594-740">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="dd594-741">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="dd594-741">Az.HDInsight</span></span>
* <span data-ttu-id="dd594-742">Удалены два командлета:</span><span class="sxs-lookup"><span data-stu-id="dd594-742">Removed two cmdlets:</span></span>
    - <span data-ttu-id="dd594-743">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="dd594-743">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="dd594-744">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="dd594-744">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="dd594-745">Добавлен новый командлет Set-AzHDInsightGatewayCredential для замены Grant-AzHDInsightHttpServicesAccess.</span><span class="sxs-lookup"><span data-stu-id="dd594-745">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="dd594-746">Обновлен командлет Get-AzHDInsightJobOutput для различения ролей читателя и оператора HDInsight:</span><span class="sxs-lookup"><span data-stu-id="dd594-746">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="dd594-747">Пользователям с ролью читателя не нужно указывать параметр DefaultStorageAccountKey явным образом, иначе возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="dd594-747">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="dd594-748">На пользователей с ролью оператора HDInsight это не повлияет.</span><span class="sxs-lookup"><span data-stu-id="dd594-748">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="dd594-749">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dd594-749">Az.Monitor</span></span>
* <span data-ttu-id="dd594-750">Новые командлеты для API SQR (запланированное правило запросов)</span><span class="sxs-lookup"><span data-stu-id="dd594-750">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="dd594-751">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="dd594-751">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="dd594-752">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="dd594-752">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="dd594-753">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="dd594-753">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="dd594-754">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="dd594-754">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="dd594-755">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="dd594-755">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="dd594-756">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="dd594-756">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="dd594-757">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="dd594-757">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="dd594-758">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="dd594-758">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="dd594-759">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="dd594-759">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="dd594-760">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="dd594-760">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="dd594-761">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="dd594-761">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="dd594-762">См. подробнее об [API SQR](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules).</span><span class="sxs-lookup"><span data-stu-id="dd594-762">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="dd594-763">Обновлен файл Az.Monitor.md для включения командлетов для правила генерации оповещений на основе метрик GenV2(не классическая версия).</span><span class="sxs-lookup"><span data-stu-id="dd594-763">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dd594-764">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dd594-764">Az.Network</span></span>
* <span data-ttu-id="dd594-765">Добавлена поддержка для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="dd594-765">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="dd594-766">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="dd594-766">New cmdlets</span></span>
        - <span data-ttu-id="dd594-767">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="dd594-767">New-AzNatGateway</span></span>
        - <span data-ttu-id="dd594-768">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="dd594-768">Get-AzNatGateway</span></span>
        - <span data-ttu-id="dd594-769">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="dd594-769">Set-AzNatGateway</span></span>
        - <span data-ttu-id="dd594-770">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="dd594-770">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="dd594-771">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="dd594-771">Updated cmdlets</span></span>
        - <span data-ttu-id="dd594-772">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="dd594-772">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="dd594-773">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="dd594-773">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="dd594-774">Обновлены следующие команды для функции: Настройка и удаление пользовательских маршрутов через шлюз в Бруклине.</span><span class="sxs-lookup"><span data-stu-id="dd594-774">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="dd594-775">Обновлен командлет New-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="dd594-775">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="dd594-776">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="dd594-776">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="dd594-777">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="dd594-777">Az.PolicyInsights</span></span>
* <span data-ttu-id="dd594-778">Добавлена поддержка сведений об оценке политики запросов.</span><span class="sxs-lookup"><span data-stu-id="dd594-778">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="dd594-779">Добавлен параметр -Expand в командлет Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="dd594-779">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="dd594-780">Добавлена поддержка -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="dd594-780">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dd594-781">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dd594-781">Az.RecoveryServices</span></span>
* <span data-ttu-id="dd594-782">Добавлена поддержка перекрестной подписки на Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="dd594-782">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="dd594-783">Добавлена возможность отмечать предстоящие критически важные изменения для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="dd594-783">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="dd594-784">Исправлены план восстановления и план действий для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="dd594-784">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="dd594-785">Исправлено сетевое сопоставление обновления Azure Site Recovery (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="dd594-785">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="dd594-786">Исправлено направление защиты обновления Azure Site Recovery для управляемых дисков (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="dd594-786">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="dd594-787">Добавлены другие незначительные исправления.</span><span class="sxs-lookup"><span data-stu-id="dd594-787">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="dd594-788">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="dd594-788">Az.Relay</span></span>
* <span data-ttu-id="dd594-789">Исправлены опечатки в сообщениях для клиентов.</span><span class="sxs-lookup"><span data-stu-id="dd594-789">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="dd594-790">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="dd594-790">Az.ServiceBus</span></span>
* <span data-ttu-id="dd594-791">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="dd594-791">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dd594-792">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dd594-792">Az.Storage</span></span>
* <span data-ttu-id="dd594-793">Выполнено обновление клиентской библиотеки хранилища до версии 10.0.1 (пространство имен всех объектов из этого пакета SDK изменено с Microsoft.WindowsAzure.Storage. *на Microsoft.Azure.Storage*).</span><span class="sxs-lookup"><span data-stu-id="dd594-793">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="dd594-794">Выполнено обновление до Microsoft.Azure.Management.Storage версии 11.0.0 для включения поддержки нового API версии 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="dd594-794">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="dd594-795">Значение свойства Kind по умолчанию в учетной записи хранения изменено со Storage на StorageV2.</span><span class="sxs-lookup"><span data-stu-id="dd594-795">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="dd594-796">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dd594-796">New-AzStorageAccount</span></span>
* <span data-ttu-id="dd594-797">Изменено значение Sku.Name в выходных данных командлета учетной записи хранения в соответствии со значением Sku.Name во входных данных путем добавления _ (например, StandardLRS изменено на Standard_LRS).</span><span class="sxs-lookup"><span data-stu-id="dd594-797">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="dd594-798">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dd594-798">New-AzStorageAccount</span></span>
    - <span data-ttu-id="dd594-799">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dd594-799">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="dd594-800">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dd594-800">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dd594-801">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dd594-801">Az.Websites</span></span>
* <span data-ttu-id="dd594-802">Свойство Kind теперь будет задаваться объектам PSSite, возвращаемым командлетом Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="dd594-802">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="dd594-803">Get-AzWebApp\*Metrics и Get-AzAppServicePlanMetrics считаются нерекомендуемыми.</span><span class="sxs-lookup"><span data-stu-id="dd594-803">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="dd594-804">1.8.0 — апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="dd594-804">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="dd594-805">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="dd594-805">Highlights since the last major release</span></span>
* <span data-ttu-id="dd594-806">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="dd594-806">General availability of `Az` module</span></span>
* <span data-ttu-id="dd594-807">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="dd594-807">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="dd594-808">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="dd594-808">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="dd594-809">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="dd594-809">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="dd594-810">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="dd594-810">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="dd594-811">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="dd594-811">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="dd594-812">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="dd594-812">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="dd594-813">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dd594-813">Az.Accounts</span></span>
* <span data-ttu-id="dd594-814">Обновлен командлет Uninstall-AzureRm для правильного удаления модулей в Mac.</span><span class="sxs-lookup"><span data-stu-id="dd594-814">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="dd594-815">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="dd594-815">Az.Batch</span></span>
* <span data-ttu-id="dd594-816">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="dd594-816">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="dd594-817">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="dd594-817">Az.Cdn</span></span>
* <span data-ttu-id="dd594-818">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="dd594-818">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="dd594-819">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="dd594-819">Az.CognitiveServices</span></span>
* <span data-ttu-id="dd594-820">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="dd594-820">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dd594-821">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd594-821">Az.Compute</span></span>
* <span data-ttu-id="dd594-822">Устранена проблема с установкой AEM, если в идентификаторах ресурсов дисков группа ресурсов указана в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="dd594-822">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="dd594-823">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="dd594-823">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="dd594-824">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="dd594-824">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dd594-825">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dd594-825">Az.DataFactory</span></span>
* <span data-ttu-id="dd594-826">Добавлены свойства SsisProperties, если NodeCount не имеет значения NULL для управляемой среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="dd594-826">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="dd594-827">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dd594-827">Az.DataLakeStore</span></span>
* <span data-ttu-id="dd594-828">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="dd594-828">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="dd594-829">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="dd594-829">Az.EventGrid</span></span>
* <span data-ttu-id="dd594-830">Обновлен текст справки для конечной точки, указывающий, что необходимо создать ресурсы, прежде чем использовать командлеты для создания или обновления подписки на события.</span><span class="sxs-lookup"><span data-stu-id="dd594-830">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="dd594-831">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="dd594-831">Az.EventHub</span></span>
* <span data-ttu-id="dd594-832">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="dd594-832">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="dd594-833">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="dd594-833">Az.HDInsight</span></span>
* <span data-ttu-id="dd594-834">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="dd594-834">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="dd594-835">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="dd594-835">Az.IotHub</span></span>
* <span data-ttu-id="dd594-836">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="dd594-836">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="dd594-837">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dd594-837">Az.KeyVault</span></span>
* <span data-ttu-id="dd594-838">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="dd594-838">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="dd594-839">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="dd594-839">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="dd594-840">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="dd594-840">Az.MachineLearning</span></span>
* <span data-ttu-id="dd594-841">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="dd594-841">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="dd594-842">Az.Media</span><span class="sxs-lookup"><span data-stu-id="dd594-842">Az.Media</span></span>
* <span data-ttu-id="dd594-843">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="dd594-843">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="dd594-844">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dd594-844">Az.Monitor</span></span>
  * <span data-ttu-id="dd594-845">Добавлены новые командлеты для правила генерации оповещений на основе метрик GenV2 (не классических).</span><span class="sxs-lookup"><span data-stu-id="dd594-845">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="dd594-846">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="dd594-846">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="dd594-847">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="dd594-847">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="dd594-848">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="dd594-848">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="dd594-849">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="dd594-849">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="dd594-850">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="dd594-850">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="dd594-851">Обновлен пакет SDK Monitor до предварительной версии 0.22.0.</span><span class="sxs-lookup"><span data-stu-id="dd594-851">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dd594-852">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dd594-852">Az.Network</span></span>
* <span data-ttu-id="dd594-853">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="dd594-853">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="dd594-854">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="dd594-854">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="dd594-855">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="dd594-855">Az.NotificationHubs</span></span>
* <span data-ttu-id="dd594-856">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="dd594-856">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="dd594-857">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="dd594-857">Az.OperationalInsights</span></span>
* <span data-ttu-id="dd594-858">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="dd594-858">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="dd594-859">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="dd594-859">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="dd594-860">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="dd594-860">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dd594-861">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dd594-861">Az.RecoveryServices</span></span>
* <span data-ttu-id="dd594-862">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="dd594-862">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="dd594-863">Обновлен табличный формат для SQL на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="dd594-863">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="dd594-864">Добавлен альтернативный метод для получения расположения в Общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="dd594-864">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="dd594-865">Обновлено значение ScheduleRunDays в объекте SchedulePolicy в соответствии с часовым поясом.</span><span class="sxs-lookup"><span data-stu-id="dd594-865">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="dd594-866">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="dd594-866">Az.RedisCache</span></span>
* <span data-ttu-id="dd594-867">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="dd594-867">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="dd594-868">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd594-868">Az.Resources</span></span>
* <span data-ttu-id="dd594-869">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="dd594-869">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="dd594-870">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd594-870">Az.Sql</span></span>
* <span data-ttu-id="dd594-871">Заменена зависимость от пакета SDK монитора на обычный код.</span><span class="sxs-lookup"><span data-stu-id="dd594-871">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="dd594-872">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="dd594-872">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="dd594-873">Улучшен процесс классификации нескольких столбцов.</span><span class="sxs-lookup"><span data-stu-id="dd594-873">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="dd594-874">Добавлены свойства SKU (имя, семейство, производительность SKU) в отклике Get-AzSqlServerServiceObjective, а также по умолчанию задан табличный формат.</span><span class="sxs-lookup"><span data-stu-id="dd594-874">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="dd594-875">C помощью Get-AzSqlServerServiceObjective теперь можно получать список доступных целевых служб по расположению без необходимости заранее размещать сервер в регионе.</span><span class="sxs-lookup"><span data-stu-id="dd594-875">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="dd594-876">Поддерживается параметр часового пояса при создании Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="dd594-876">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="dd594-877">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="dd594-877">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dd594-878">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dd594-878">Az.Websites</span></span>
* <span data-ttu-id="dd594-879">Исправлены командлеты Set-AzWebApp и Set-AzWebAppSlot, которые теперь не удаляют теги при выполнении.</span><span class="sxs-lookup"><span data-stu-id="dd594-879">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="dd594-880">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="dd594-880">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="dd594-881">Обновлен пакет SDK веб-узлов.</span><span class="sxs-lookup"><span data-stu-id="dd594-881">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="dd594-882">Удалено свойство AdminSiteName из PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="dd594-882">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="dd594-883">1.7.0 —апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="dd594-883">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="dd594-884">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="dd594-884">Highlights since the last major release</span></span>
* <span data-ttu-id="dd594-885">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="dd594-885">General availability of `Az` module</span></span>
* <span data-ttu-id="dd594-886">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="dd594-886">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="dd594-887">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="dd594-887">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="dd594-888">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="dd594-888">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="dd594-889">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="dd594-889">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="dd594-890">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="dd594-890">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="dd594-891">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="dd594-891">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="dd594-892">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dd594-892">Az.Accounts</span></span>
* <span data-ttu-id="dd594-893">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметр AzureAnalysisServicesEndpointResourceId.</span><span class="sxs-lookup"><span data-stu-id="dd594-893">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="dd594-894">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="dd594-894">Az.AnalysisServices</span></span>
* <span data-ttu-id="dd594-895">Использование ServiceClient в командлетах плоскости данных и удаление исходной логики проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="dd594-895">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="dd594-896">Add-AzureASAccount используется как оболочка для Connect-AzAccount во избежание критических изменений.</span><span class="sxs-lookup"><span data-stu-id="dd594-896">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="dd594-897">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dd594-897">Az.Automation</span></span>
* <span data-ttu-id="dd594-898">Исправлена ошибка командлета New-AzAutomationSoftwareUpdateConfiguration, связанная с включением.</span><span class="sxs-lookup"><span data-stu-id="dd594-898">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="dd594-899">Теперь параметры IncludedKbNumber и IncludedPackageNameMask должны работать нормально.</span><span class="sxs-lookup"><span data-stu-id="dd594-899">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="dd594-900">Исправлена ошибка динамической группы управления обновлениями службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="dd594-900">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dd594-901">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd594-901">Az.Compute</span></span>
* <span data-ttu-id="dd594-902">В командлеты New-AzDiskConfig и New-AzSnapshotConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="dd594-902">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="dd594-903">Теперь можно создавать виртуальные машину на основе образов из коллекции от других клиентов.</span><span class="sxs-lookup"><span data-stu-id="dd594-903">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="dd594-904">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="dd594-904">Az.ContainerInstance</span></span>
* <span data-ttu-id="dd594-905">Исправлена проблема в параметре -Command командлета New-AzContainerGroup, из-за которой в конце добавлялся пустой аргумент.</span><span class="sxs-lookup"><span data-stu-id="dd594-905">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dd594-906">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dd594-906">Az.DataFactory</span></span>
* <span data-ttu-id="dd594-907">Пакет SDK для ADF .NET обновлен до версии 3.0.2.</span><span class="sxs-lookup"><span data-stu-id="dd594-907">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="dd594-908">Командлет Set-AzDataFactoryV2 обновлен с помощью дополнительных параметров для настроек, связанных с RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="dd594-908">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="dd594-909">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd594-909">Az.Resources</span></span>
* <span data-ttu-id="dd594-910">Улучшена обработка поставщиков Get-AzResource при предоставлении параметров -ResourceId или -ResourceGroupName, -Name и -ResourceType.</span><span class="sxs-lookup"><span data-stu-id="dd594-910">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="dd594-911">Улучшена обработка ошибок в командлетах Test-AzDeployment и Test-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="dd594-911">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="dd594-912">Теперь ошибки, возникающие за пределами проверки развертывания, обрабатываются и включаются в выходные данные команды.</span><span class="sxs-lookup"><span data-stu-id="dd594-912">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="dd594-913">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="dd594-913">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="dd594-914">Добавлен параметр-переключатель -IgnoreDynamicParameters, с помощью которого можно настроить командлеты развертывания так, чтобы они пропускали запросы в сценариях скриптов и заданий.</span><span class="sxs-lookup"><span data-stu-id="dd594-914">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="dd594-915">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="dd594-915">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="dd594-916">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd594-916">Az.Sql</span></span>
* <span data-ttu-id="dd594-917">Поддержка классификации данных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="dd594-917">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dd594-918">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dd594-918">Az.Storage</span></span>
* <span data-ttu-id="dd594-919">Подробные сообщения об ошибке передаются при создании контекста хранилища с помощью параметра -UseConnectedAccount, но без входа в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="dd594-919">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="dd594-920">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="dd594-920">New-AzStorageContext</span></span>
* <span data-ttu-id="dd594-921">Поддержка свойств службы управления BLOB-объектов в указанной учетной записи хранения с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="dd594-921">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="dd594-922">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="dd594-922">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="dd594-923">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="dd594-923">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="dd594-924">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="dd594-924">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="dd594-925">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="dd594-925">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="dd594-926">Поддержка параметра -AsJob в командлетах для отправки и скачивания больших двоичных объектов и файлов.</span><span class="sxs-lookup"><span data-stu-id="dd594-926">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="dd594-927">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="dd594-927">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="dd594-928">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="dd594-928">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="dd594-929">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="dd594-929">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="dd594-930">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="dd594-930">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="dd594-931">1.6.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="dd594-931">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="dd594-932">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="dd594-932">Highlights since the last major release</span></span>
* <span data-ttu-id="dd594-933">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="dd594-933">General availability of `Az` module</span></span>
* <span data-ttu-id="dd594-934">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="dd594-934">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="dd594-935">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="dd594-935">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="dd594-936">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="dd594-936">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="dd594-937">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="dd594-937">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="dd594-938">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="dd594-938">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="dd594-939">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="dd594-939">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="dd594-940">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dd594-940">Az.Automation</span></span>
* <span data-ttu-id="dd594-941">В управление обновлениями службы автоматизации Azure внесены изменения для поддержки следующих новых функций:</span><span class="sxs-lookup"><span data-stu-id="dd594-941">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="dd594-942">динамическое группирование;</span><span class="sxs-lookup"><span data-stu-id="dd594-942">Dynamic grouping</span></span>
    * <span data-ttu-id="dd594-943">скрипты предварительного или последующего выполнения;</span><span class="sxs-lookup"><span data-stu-id="dd594-943">Pre-Post script</span></span>
    * <span data-ttu-id="dd594-944">параметр перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="dd594-944">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dd594-945">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd594-945">Az.Compute</span></span>
* <span data-ttu-id="dd594-946">Устранена проблема, связанная с разрешением пути в Get-AzVmBootDiagnosticsData.</span><span class="sxs-lookup"><span data-stu-id="dd594-946">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="dd594-947">Обновление клиентской библиотеки вычислений до версии 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="dd594-947">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="dd594-948">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dd594-948">Az.KeyVault</span></span>
* <span data-ttu-id="dd594-949">Добавлена поддержка подстановочных знаков в командлетах KeyVault.</span><span class="sxs-lookup"><span data-stu-id="dd594-949">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dd594-950">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dd594-950">Az.Network</span></span>
* <span data-ttu-id="dd594-951">Добавлена поддержка анализа угроз для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="dd594-951">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="dd594-952">Добавлены настраиваемые правила и ресурс верхнего уровня для политики брандмауэра Шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="dd594-952">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dd594-953">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dd594-953">Az.RecoveryServices</span></span>
* <span data-ttu-id="dd594-954">В политику виртуальной машины Azure добавлен объект SnapshotRetentionInDays для поддержки мгновенного восстановления.</span><span class="sxs-lookup"><span data-stu-id="dd594-954">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="dd594-955">Добавлена поддержка канала для отмены регистрации контейнера.</span><span class="sxs-lookup"><span data-stu-id="dd594-955">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="dd594-956">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd594-956">Az.Resources</span></span>
* <span data-ttu-id="dd594-957">Обновлена поддержка подстановочных знаков для Get-AzResource и Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="dd594-957">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="dd594-958">Обновлены учетные данные, используемые при общих вызовах к ARM.</span><span class="sxs-lookup"><span data-stu-id="dd594-958">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="dd594-959">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd594-959">Az.Sql</span></span>
* <span data-ttu-id="dd594-960">Изменен тип параметра (ExcludeDetectionType) командлетов для обнаружения угроз с DetectionTypes на string[] для поддержки актуального состояния при добавлении новых типов обнаружения и для поддержки автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="dd594-960">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dd594-961">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dd594-961">Az.Storage</span></span>
* <span data-ttu-id="dd594-962">Поддержка получения, настройки и удаления политики управления в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="dd594-962">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="dd594-963">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="dd594-963">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="dd594-964">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="dd594-964">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="dd594-965">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="dd594-965">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="dd594-966">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="dd594-966">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="dd594-967">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="dd594-967">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="dd594-968">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="dd594-968">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dd594-969">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dd594-969">Az.Websites</span></span>
* <span data-ttu-id="dd594-970">Исправлена ошибка с шаблоном ARM, из-за которой прерывалось клонирование все слотов при использовании New-AzWebApp -IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="dd594-970">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="dd594-971">1.5.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="dd594-971">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dd594-972">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dd594-972">Az.Accounts</span></span>
* <span data-ttu-id="dd594-973">Добавлена команда Register-AzModule для поддержки созданных командлетов AutoRest.</span><span class="sxs-lookup"><span data-stu-id="dd594-973">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="dd594-974">Обновлены примеры для Connect AzAccount.</span><span class="sxs-lookup"><span data-stu-id="dd594-974">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="dd594-975">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dd594-975">Az.Automation</span></span>
* <span data-ttu-id="dd594-976">Исправлена проблема с получением некоторых ежемесячных расписаний в нескольких командлетах службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="dd594-976">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="dd594-977">Исправлен командлет Get-AzAutomationDscNode, возвращающий только первые 20 узлов.</span><span class="sxs-lookup"><span data-stu-id="dd594-977">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="dd594-978">Теперь он возвращает все узлы.</span><span class="sxs-lookup"><span data-stu-id="dd594-978">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="dd594-979">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="dd594-979">Az.Cdn</span></span>
* <span data-ttu-id="dd594-980">Добавлены новые командлеты PowerShell для включения и отключения HTTPS для личного домена и отключены устаревшие командлеты.</span><span class="sxs-lookup"><span data-stu-id="dd594-980">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dd594-981">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd594-981">Az.Compute</span></span>
* <span data-ttu-id="dd594-982">Добавлена поддержка подстановочных знаков в командлетах Get.</span><span class="sxs-lookup"><span data-stu-id="dd594-982">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dd594-983">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dd594-983">Az.DataFactory</span></span>
* <span data-ttu-id="dd594-984">Обновлен пакет SDK для ADF .NET до версии 3.0.1.</span><span class="sxs-lookup"><span data-stu-id="dd594-984">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="dd594-985">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="dd594-985">Az.LogicApp</span></span>
* <span data-ttu-id="dd594-986">Исправлена проблема с получением только первой страницы результатов при выполнении команды ListWorkflows.</span><span class="sxs-lookup"><span data-stu-id="dd594-986">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dd594-987">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dd594-987">Az.Network</span></span>
* <span data-ttu-id="dd594-988">Добавлена поддержка подстановочных знаков в командлетах Network.</span><span class="sxs-lookup"><span data-stu-id="dd594-988">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dd594-989">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dd594-989">Az.RecoveryServices</span></span>
* <span data-ttu-id="dd594-990">Добавлена поддержка SQL Server на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="dd594-990">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="dd594-991">Обновление пакета SDK</span><span class="sxs-lookup"><span data-stu-id="dd594-991">SDK Update</span></span>
* <span data-ttu-id="dd594-992">Удалена проверка VMappContainer в Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="dd594-992">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="dd594-993">Добавлены параметры Name и ServerName для Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="dd594-993">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="dd594-994">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd594-994">Az.Resources</span></span>
* <span data-ttu-id="dd594-995">Добавлен параметр `-TemplateObject` в командлеты для развертывания.</span><span class="sxs-lookup"><span data-stu-id="dd594-995">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="dd594-996">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2933.</span><span class="sxs-lookup"><span data-stu-id="dd594-996">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="dd594-997">Устранена проблема с передачей в конвейер результата `Get-AzResource` для `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="dd594-997">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="dd594-998">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8240.</span><span class="sxs-lookup"><span data-stu-id="dd594-998">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="dd594-999">Устранена проблема с изменением типа данных JSON при выполнении `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="dd594-999">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="dd594-1000">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7930.</span><span class="sxs-lookup"><span data-stu-id="dd594-1000">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="dd594-1001">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd594-1001">Az.Sql</span></span>
* <span data-ttu-id="dd594-1002">Обновление AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="dd594-1002">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="dd594-1003">Исправлено поведение для пограничного случая при создании параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="dd594-1003">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dd594-1004">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dd594-1004">Az.Storage</span></span>
* <span data-ttu-id="dd594-1005">Включена поддержка Kind BlockBlobStorage при создании учетной записи хранения для New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="dd594-1005">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="dd594-1006">1.4.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="dd594-1006">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="dd594-1007">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="dd594-1007">Az.AnalysisServices</span></span>
* <span data-ttu-id="dd594-1008">Командлет AddAzureASAccount устарел.</span><span class="sxs-lookup"><span data-stu-id="dd594-1008">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="dd594-1009">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dd594-1009">Az.Automation</span></span>
* <span data-ttu-id="dd594-1010">Обновлена справка для командлета Import-AzAutomationDscNodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="dd594-1010">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="dd594-1011">Добавлена проверка имени конфигурации для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="dd594-1011">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="dd594-1012">Улучшена обработка ошибок для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="dd594-1012">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="dd594-1013">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="dd594-1013">Az.CognitiveServices</span></span>
* <span data-ttu-id="dd594-1014">Добавлен параметр CustomSubdomainName — новый необязательный параметр для командлета New-AzCognitiveServicesAccount, который указывает поддомен для ресурса.</span><span class="sxs-lookup"><span data-stu-id="dd594-1014">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dd594-1015">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd594-1015">Az.Compute</span></span>
* <span data-ttu-id="dd594-1016">Устранена проблема с идентификаторами наборов параметров.</span><span class="sxs-lookup"><span data-stu-id="dd594-1016">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="dd594-1017">Обновлен командлет Get-AzVMExtension для отображения списка всех установленных расширений, если не указан параметр Name.</span><span class="sxs-lookup"><span data-stu-id="dd594-1017">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="dd594-1018">Для командлета Update-AzImage добавлены параметры Tag и ResourceId.</span><span class="sxs-lookup"><span data-stu-id="dd594-1018">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="dd594-1019">Командлет Get-AzVmssVM, который выполняется без указания идентификатора экземпляра и с параметром InstanceView, может выводить виртуальные машины из VMSS с представлением экземпляра.</span><span class="sxs-lookup"><span data-stu-id="dd594-1019">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="dd594-1020">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dd594-1020">Az.DataLakeStore</span></span>
* <span data-ttu-id="dd594-1021">Добавлены командлеты для перечисления и восстановления удаленного элемента ADL.</span><span class="sxs-lookup"><span data-stu-id="dd594-1021">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="dd594-1022">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="dd594-1022">Az.EventHub</span></span>
* <span data-ttu-id="dd594-1023">Добавлено новое логическое свойство SkipEmptyArchives для пропуска пустых архивов в классе CaptureDescription Eventhub.</span><span class="sxs-lookup"><span data-stu-id="dd594-1023">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="dd594-1024">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dd594-1024">Az.KeyVault</span></span>
* <span data-ttu-id="dd594-1025">Исправлена расстановка тегов для командлета Set-AzKeyVaultSecret.</span><span class="sxs-lookup"><span data-stu-id="dd594-1025">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="dd594-1026">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="dd594-1026">Az.LogicApp</span></span>
* <span data-ttu-id="dd594-1027">Добавлен SKU "Базовый" для учетных записей интеграции.</span><span class="sxs-lookup"><span data-stu-id="dd594-1027">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="dd594-1028">Добавлены типы сопоставлений Liquid, а также XSLT 2.0 и XSLT 3.0.</span><span class="sxs-lookup"><span data-stu-id="dd594-1028">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="dd594-1029">Новые командлеты для сборок учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="dd594-1029">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="dd594-1030">Get-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="dd594-1030">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="dd594-1031">New-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="dd594-1031">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="dd594-1032">Remove-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="dd594-1032">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="dd594-1033">Set-AzIntegrationAccountAssembly.</span><span class="sxs-lookup"><span data-stu-id="dd594-1033">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="dd594-1034">Новые командлеты для конфигурации пакета учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="dd594-1034">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="dd594-1035">Get-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="dd594-1035">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="dd594-1036">New-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="dd594-1036">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="dd594-1037">Remove-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="dd594-1037">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="dd594-1038">Set-AzIntegrationAccountBatchConfiguration.</span><span class="sxs-lookup"><span data-stu-id="dd594-1038">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="dd594-1039">Обновлен пакет SDK Logic Apps до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="dd594-1039">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="dd594-1040">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dd594-1040">Az.Monitor</span></span>
* <span data-ttu-id="dd594-1041">Обновлена справка для командлета Get-AzMetric.</span><span class="sxs-lookup"><span data-stu-id="dd594-1041">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dd594-1042">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dd594-1042">Az.Network</span></span>
* <span data-ttu-id="dd594-1043">Обновлен пример справки для командлета Add-AzApplicationGatewayCustomError.</span><span class="sxs-lookup"><span data-stu-id="dd594-1043">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="dd594-1044">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="dd594-1044">Az.OperationalInsights</span></span>
* <span data-ttu-id="dd594-1045">Дополнительная поддержка создания и получения источников данных ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="dd594-1045">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="dd594-1046">Добавлен новый тип ApplicationInsights для получения определенных или всех источников данных ApplicationInsights для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="dd594-1046">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="dd594-1047">Добавлен командлет New-AzOperationalInsightsApplicationInsightsDataSource для создания источника данных с использованием параметров указанного ресурса Application-Insightss: subscription Id, resourceGroupName и name.</span><span class="sxs-lookup"><span data-stu-id="dd594-1047">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="dd594-1048">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd594-1048">Az.Resources</span></span>
* <span data-ttu-id="dd594-1049">исправлена проблема https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="dd594-1049">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="dd594-1050">исправлена проблема https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="dd594-1050">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="dd594-1051">исправлена проблема https://github.com/Azure/azure-powershell/issues/6219.</span><span class="sxs-lookup"><span data-stu-id="dd594-1051">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="dd594-1052">Исправлена ошибка, препятствующая повторному созданию KeyCredentials.</span><span class="sxs-lookup"><span data-stu-id="dd594-1052">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="dd594-1053">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd594-1053">Az.Sql</span></span>
* <span data-ttu-id="dd594-1054">Добавлена поддержка уровня гипермасштабирования в базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="dd594-1054">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="dd594-1055">Исправлена ошибка, из-за которой восстановление могло завершиться со сбоем при указании ненужных свойств в запросе на восстановление.</span><span class="sxs-lookup"><span data-stu-id="dd594-1055">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dd594-1056">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dd594-1056">Az.Websites</span></span>
* <span data-ttu-id="dd594-1057">Исправлен пример для командлета Get-AzWebAppSlotMetrics.</span><span class="sxs-lookup"><span data-stu-id="dd594-1057">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="dd594-1058">1.3.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="dd594-1058">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dd594-1059">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dd594-1059">Az.Accounts</span></span>
* <span data-ttu-id="dd594-1060">Обновление до последней версии ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="dd594-1060">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="dd594-1061">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="dd594-1061">Az.AnalysisServices</span></span>
<span data-ttu-id="dd594-1062">Общедоступная версия модуля Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="dd594-1062">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dd594-1063">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd594-1063">Az.Compute</span></span>
* <span data-ttu-id="dd594-1064">Расширение AEM: добавлена поддержка дисков UltraSSD, P60, P70 и P80.</span><span class="sxs-lookup"><span data-stu-id="dd594-1064">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="dd594-1065">Обновлено описание справки для командлета Set-AzVMBootDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="dd594-1065">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="dd594-1066">Обновлено описание справки и пример для командлета Update-AzImage.</span><span class="sxs-lookup"><span data-stu-id="dd594-1066">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dd594-1067">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dd594-1067">Az.RecoveryServices</span></span>
<span data-ttu-id="dd594-1068">Общедоступная версия модуля Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="dd594-1068">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="dd594-1069">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd594-1069">Az.Resources</span></span>
* <span data-ttu-id="dd594-1070">Исправлена расстановка тегов для групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dd594-1070">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="dd594-1071">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="dd594-1071">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="dd594-1072">Исправлена проблема с игнорированием командлетом `Get-AzureRmRoleAssignment` параметра -ErrorAction.</span><span class="sxs-lookup"><span data-stu-id="dd594-1072">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="dd594-1073">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="dd594-1073">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="dd594-1074">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd594-1074">Az.Sql</span></span>
* <span data-ttu-id="dd594-1075">Добавлен командлет Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="dd594-1075">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="dd594-1076">Исправлена проблема с появлением исключения NullRef при выполнении командлетов SQL, если не выполнен вход в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="dd594-1076">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="dd594-1077">Исправлено исключение NullRef в командлете Get-AzSqlCapability.</span><span class="sxs-lookup"><span data-stu-id="dd594-1077">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="dd594-1078">1.2.1 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="dd594-1078">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dd594-1079">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dd594-1079">Az.Accounts</span></span>
* <span data-ttu-id="dd594-1080">Выпуск с правильной версией службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="dd594-1080">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="dd594-1081">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="dd594-1081">Az.AnalysisServices</span></span>
* <span data-ttu-id="dd594-1082">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="dd594-1082">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dd594-1083">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dd594-1083">Az.RecoveryServices</span></span>
* <span data-ttu-id="dd594-1084">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="dd594-1084">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="dd594-1085">1.2.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="dd594-1085">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dd594-1086">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dd594-1086">Az.Accounts</span></span>
* <span data-ttu-id="dd594-1087">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="dd594-1087">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="dd594-1088">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="dd594-1088">Update incorrect online help URLs</span></span>
* <span data-ttu-id="dd594-1089">Добавлено предупреждающее сообщение в PS Core для модуля Uninstall-AzureRm.</span><span class="sxs-lookup"><span data-stu-id="dd594-1089">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="dd594-1090">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="dd594-1090">Az.Aks</span></span>
* <span data-ttu-id="dd594-1091">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="dd594-1091">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="dd594-1092">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dd594-1092">Az.Automation</span></span>
* <span data-ttu-id="dd594-1093">Добавлена поддержка для модулей runbook Python 2.</span><span class="sxs-lookup"><span data-stu-id="dd594-1093">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="dd594-1094">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="dd594-1094">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="dd594-1095">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="dd594-1095">Az.Cdn</span></span>
* <span data-ttu-id="dd594-1096">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="dd594-1096">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dd594-1097">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd594-1097">Az.Compute</span></span>
* <span data-ttu-id="dd594-1098">Добавлен командлет Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="dd594-1098">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="dd594-1099">Добавлен параметр TempDisk к командлету Set-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="dd594-1099">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="dd594-1100">Исправлено предупреждающее сообщение командлета New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="dd594-1100">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="dd594-1101">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="dd594-1101">Az.ContainerRegistry</span></span>
* <span data-ttu-id="dd594-1102">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="dd594-1102">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dd594-1103">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dd594-1103">Az.DataFactory</span></span>
* <span data-ttu-id="dd594-1104">Пакет SDK ADF .Net обновлен до версии 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="dd594-1104">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="dd594-1105">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dd594-1105">Az.DataLakeStore</span></span>
* <span data-ttu-id="dd594-1106">Исправлена проблема с конечной точкой ADLS при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="dd594-1106">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="dd594-1107">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7462.</span><span class="sxs-lookup"><span data-stu-id="dd594-1107">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="dd594-1108">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="dd594-1108">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="dd594-1109">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="dd594-1109">Az.IotHub</span></span>
* <span data-ttu-id="dd594-1110">Добавлен формат кодирования для командлета Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="dd594-1110">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="dd594-1111">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dd594-1111">Az.KeyVault</span></span>
* <span data-ttu-id="dd594-1112">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="dd594-1112">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dd594-1113">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dd594-1113">Az.Network</span></span>
* <span data-ttu-id="dd594-1114">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="dd594-1114">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="dd594-1115">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd594-1115">Az.Resources</span></span>
* <span data-ttu-id="dd594-1116">Исправлены неправильные примеры в справочной документации по командлетам New-AzADAppCredential и New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="dd594-1116">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="dd594-1117">Исправлена проблема, при которой путь для параметра -TemplateFile не удавалось разрешить до выполнения командлетов развертывания групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dd594-1117">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="dd594-1118">Az.Resources: исправлена документация для значения по умолчанию -Mode командлета New-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="dd594-1118">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="dd594-1119">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/7522.</span><span class="sxs-lookup"><span data-stu-id="dd594-1119">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="dd594-1120">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/5747.</span><span class="sxs-lookup"><span data-stu-id="dd594-1120">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="dd594-1121">Исправлена проблема с форматированием объекта PSResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="dd594-1121">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="dd594-1122">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2123.</span><span class="sxs-lookup"><span data-stu-id="dd594-1122">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="dd594-1123">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dd594-1123">Az.ServiceFabric</span></span>
* <span data-ttu-id="dd594-1124">Исправлена проблема с появлением исключения в процессе отката при добавлении сертификата к модели VMSS: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="dd594-1124">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="dd594-1125">Исправлены некоторые сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="dd594-1125">Fix some error messages.</span></span>
* <span data-ttu-id="dd594-1126">Исправлена проблема с созданием кластера с шаблоном ARM по умолчанию для командлета New-AzServiceFabriCluster, который не работал с операцией миграции в Az.</span><span class="sxs-lookup"><span data-stu-id="dd594-1126">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="dd594-1127">Исправлена проблема с добавлением сертификата кластера или приложения: теперь они добавляются только в Масштабируемые наборы виртуальных машин, которые сопоставлены с кластером, путем проверки идентификатора кластера в расширении.</span><span class="sxs-lookup"><span data-stu-id="dd594-1127">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="dd594-1128">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="dd594-1128">Az.SignalR</span></span>
* <span data-ttu-id="dd594-1129">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="dd594-1129">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="dd594-1130">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd594-1130">Az.Sql</span></span>
* <span data-ttu-id="dd594-1131">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="dd594-1131">Update incorrect online help URLs</span></span>
* <span data-ttu-id="dd594-1132">Обновлено описание параметра LicenseType с добавлением возможных значений.</span><span class="sxs-lookup"><span data-stu-id="dd594-1132">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="dd594-1133">Исправлена проблема с неправильным обновлением удостоверения управляемого экземпляра, если оно было единственным обновляемым свойством.</span><span class="sxs-lookup"><span data-stu-id="dd594-1133">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="dd594-1134">Поддержка пользовательских параметров сортировки в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="dd594-1134">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dd594-1135">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dd594-1135">Az.Storage</span></span>
* <span data-ttu-id="dd594-1136">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="dd594-1136">Update incorrect online help URLs</span></span>
* <span data-ttu-id="dd594-1137">Добавлен вывод подробных сообщений об ошибке при получении или установке классических свойств ведения журнала или метрик в учетной записи хранилища класса Premium, так как учетная запись хранилища класса Premium не поддерживает классические функции ведения журнала и метрик.</span><span class="sxs-lookup"><span data-stu-id="dd594-1137">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="dd594-1138">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="dd594-1138">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="dd594-1139">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="dd594-1139">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="dd594-1140">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="dd594-1140">Az.TrafficManager</span></span>
* <span data-ttu-id="dd594-1141">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="dd594-1141">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dd594-1142">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dd594-1142">Az.Websites</span></span>
* <span data-ttu-id="dd594-1143">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="dd594-1143">Update incorrect online help URLs</span></span>
* <span data-ttu-id="dd594-1144">Исправлена работа командлета New-AzWebAppSSLBinding: сертификат отправляется в правильную группу ресурсов и правильное расположение, если приложение размещено в ASE.</span><span class="sxs-lookup"><span data-stu-id="dd594-1144">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="dd594-1145">Исправлена работа командлета New-AzWebAppSSLBinding: теги не перезаписываются при привязке SSL-сертификата к приложению.</span><span class="sxs-lookup"><span data-stu-id="dd594-1145">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="dd594-1146">1.1.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="dd594-1146">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dd594-1147">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dd594-1147">Az.Accounts</span></span>
* <span data-ttu-id="dd594-1148">Добавление области "Local" в Enable-AzureRmAlias.</span><span class="sxs-lookup"><span data-stu-id="dd594-1148">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dd594-1149">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd594-1149">Az.Compute</span></span>
* <span data-ttu-id="dd594-1150">Теперь имя не является обязательным в идентификаторе набора параметров для Restart/Start/Stop/Remove/Set-AzVM и Save-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="dd594-1150">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="dd594-1151">Обновлено описание идентификатора в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="dd594-1151">Updated the description of ID in help files</span></span>
* <span data-ttu-id="dd594-1152">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="dd594-1152">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="dd594-1153">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dd594-1153">Az.DataLakeStore</span></span>
* <span data-ttu-id="dd594-1154">Обновление версии пакета SDK для плоскости данных до 1.1.14 для устранения найденных проблем.</span><span class="sxs-lookup"><span data-stu-id="dd594-1154">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="dd594-1155">Исправлена обработка отрицательного времени доступа и времени изменения для getfilestatus и liststatus, исправлен токен отмены для асинхронных методов.</span><span class="sxs-lookup"><span data-stu-id="dd594-1155">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="dd594-1156">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="dd594-1156">Az.EventGrid</span></span>
* <span data-ttu-id="dd594-1157">Обновление для использования API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="dd594-1157">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="dd594-1158">Обновлены указанные ниже командлеты для поддержки нового сценария в API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="dd594-1158">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="dd594-1159">New-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="dd594-1159">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="dd594-1160">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="dd594-1160">Event Time-To-Live,</span></span>
        - <span data-ttu-id="dd594-1161">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="dd594-1161">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="dd594-1162">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="dd594-1162">Dead letter endpoint.</span></span>
    - <span data-ttu-id="dd594-1163">Update-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="dd594-1163">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="dd594-1164">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="dd594-1164">Event Time-To-Live,</span></span>
        - <span data-ttu-id="dd594-1165">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="dd594-1165">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="dd594-1166">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="dd594-1166">Dead letter endpoint.</span></span>
* <span data-ttu-id="dd594-1167">Для параметра EndpointType добавлены новые значения перечисления (storageQueue и hybridConnection) в командлеты New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="dd594-1167">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="dd594-1168">Если ожидается, что создание или обновление подписки на событие повлечет за собой действия со стороны пользователя, выполняемые вручную, отображается предупреждение при создании или обновлении подписки события.</span><span class="sxs-lookup"><span data-stu-id="dd594-1168">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="dd594-1169">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="dd594-1169">Az.IotHub</span></span>
* <span data-ttu-id="dd594-1170">Пакет SDK Центра Интернета вещей обновлен до последней версии.</span><span class="sxs-lookup"><span data-stu-id="dd594-1170">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="dd594-1171">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="dd594-1171">Az.LogicApp</span></span>
* <span data-ttu-id="dd594-1172">Get-AzLogicApp позволяет перечислить все параметры без указанного имени.</span><span class="sxs-lookup"><span data-stu-id="dd594-1172">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="dd594-1173">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd594-1173">Az.Resources</span></span>
* <span data-ttu-id="dd594-1174">Исправлена проблема с набором параметров при предоставлении параметров "-ODataQuery" и "-ResourceId" для "Get-AzResource".</span><span class="sxs-lookup"><span data-stu-id="dd594-1174">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="dd594-1175">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7875.</span><span class="sxs-lookup"><span data-stu-id="dd594-1175">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="dd594-1176">Исправлена обработка параметра -Custom в New/Set-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="dd594-1176">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="dd594-1177">Исправлена опечатка в документации по New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="dd594-1177">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="dd594-1178">Параметр "-MailNickname" стал обязательным для "New-AzADUser".</span><span class="sxs-lookup"><span data-stu-id="dd594-1178">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="dd594-1179">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8220.</span><span class="sxs-lookup"><span data-stu-id="dd594-1179">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="dd594-1180">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="dd594-1180">Az.SignalR</span></span>
* <span data-ttu-id="dd594-1181">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="dd594-1181">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="dd594-1182">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd594-1182">Az.Sql</span></span>
* <span data-ttu-id="dd594-1183">Зависимость клиента управления хранением преобразована для общей реализации в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="dd594-1183">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dd594-1184">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dd594-1184">Az.Storage</span></span>
* <span data-ttu-id="dd594-1185">Установка параметра StorageAccountName для контекста хранилища в качестве реального имени учетной записи хранения, если она была создана с использованием токена Sas, OAuth или анонимного доступа.</span><span class="sxs-lookup"><span data-stu-id="dd594-1185">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="dd594-1186">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="dd594-1186">New-AzStorageContext</span></span>
* <span data-ttu-id="dd594-1187">Создание токена Sas большого двоичного объекта моментального снимка с параметром "-FullUri". Возвращаемый URI исправлен на URI моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="dd594-1187">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="dd594-1188">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="dd594-1188">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dd594-1189">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dd594-1189">Az.Websites</span></span>
* <span data-ttu-id="dd594-1190">Исправлена ошибка синтаксического анализа даты в "Get-AzDeletedWebApp".</span><span class="sxs-lookup"><span data-stu-id="dd594-1190">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="dd594-1191">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="dd594-1191">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="dd594-1192">1.0.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="dd594-1192">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="dd594-1193">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="dd594-1193">General</span></span>

- <span data-ttu-id="dd594-1194">Общедоступная версия модуля Az.</span><span class="sxs-lookup"><span data-stu-id="dd594-1194">General Availability of Az Module</span></span>
- <span data-ttu-id="dd594-1195">Справка в Интернете для каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="dd594-1195">Online help for each module</span></span>
- <span data-ttu-id="dd594-1196">Дополнительные сведения и стратегию развития см. в статье [Announcing New Module 'Az'](https://aka.ms/azps-announce) (Объявление о новом модуле Az)</span><span class="sxs-lookup"><span data-stu-id="dd594-1196">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="dd594-1197">Сведения о миграции с AzureRM см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="dd594-1197">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="dd594-1198">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dd594-1198">Az.Accounts</span></span>
- <span data-ttu-id="dd594-1199">Изменено с Az.Profile.</span><span class="sxs-lookup"><span data-stu-id="dd594-1199">Changed from Az.Profile</span></span>
- <span data-ttu-id="dd594-1200">Исправлены форматы таблиц для типов профиля и контекста.</span><span class="sxs-lookup"><span data-stu-id="dd594-1200">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="dd594-1201">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="dd594-1201">Az.ApiManagement</span></span>
- <span data-ttu-id="dd594-1202">Исправления для #7002.</span><span class="sxs-lookup"><span data-stu-id="dd594-1202">Fixes for #7002</span></span>
- <span data-ttu-id="dd594-1203">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="dd594-1203">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="dd594-1204">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="dd594-1204">Az.Batch</span></span>
- <span data-ttu-id="dd594-1205">Добавлена возможность видеть, какая версия агента узла пакетной службы Azure работает в пуле на каждой виртуальной машине, с помощью нового свойства `NodeAgentInformation` в `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="dd594-1205">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="dd594-1206">Значение `Caching` по умолчанию для `PSDataDisk` теперь `ReadWrite` вместо `None`.</span><span class="sxs-lookup"><span data-stu-id="dd594-1206">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="dd594-1207">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="dd594-1207">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="dd594-1208">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="dd594-1208">Az.Billing</span></span>
- <span data-ttu-id="dd594-1209">Объединены командлеты Billing, Consumption и UsageAggregates. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0).</span><span class="sxs-lookup"><span data-stu-id="dd594-1209">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="dd594-1210">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="dd594-1210">Az.CognitivServices</span></span>
- <span data-ttu-id="dd594-1211">Добавлены средства заполнения для SkuName и Typem, доступные в операции New-AzureRmCognitiveServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="dd594-1211">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="dd594-1212">Удален набор параметров GetSkusWithAccountParamSetName из Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="dd594-1212">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="dd594-1213">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="dd594-1213">Az.ContainerInstance</span></span>
- <span data-ttu-id="dd594-1214">Добавлена поддержка ManagedIdentity.</span><span class="sxs-lookup"><span data-stu-id="dd594-1214">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="dd594-1215">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="dd594-1215">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="dd594-1216">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="dd594-1216">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="dd594-1217">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dd594-1217">Az.DataLakeStore</span></span>
- <span data-ttu-id="dd594-1218">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="dd594-1218">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="dd594-1219">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dd594-1219">Az.Monitor</span></span>
- <span data-ttu-id="dd594-1220">"Az.Insights" переименован в "Az.Monitor" и внесены другие незначительные критические изменения. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="dd594-1220">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="dd594-1221">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dd594-1221">Az.KeyVault</span></span>
- <span data-ttu-id="dd594-1222">Из типов вывода удалено устаревшее свойство PurgeDisabled</span><span class="sxs-lookup"><span data-stu-id="dd594-1222">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="dd594-1223">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="dd594-1223">Az.MachineLearning</span></span>
- <span data-ttu-id="dd594-1224">Включены командлеты из модуля Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="dd594-1224">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="dd594-1225">Az.Media</span><span class="sxs-lookup"><span data-stu-id="dd594-1225">Az.Media</span></span>
- <span data-ttu-id="dd594-1226">Удаляет устаревший псевдоним Tags из New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="dd594-1226">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="dd594-1227">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dd594-1227">Az.Network</span></span>
<span data-ttu-id="dd594-1228">В шлюз приложений добавлена поддержка настройки RewriteRuleSets</span><span class="sxs-lookup"><span data-stu-id="dd594-1228">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="dd594-1229">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="dd594-1229">New cmdlets added:</span></span>
        - <span data-ttu-id="dd594-1230">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="dd594-1230">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="dd594-1231">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="dd594-1231">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="dd594-1232">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="dd594-1232">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="dd594-1233">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="dd594-1233">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="dd594-1234">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="dd594-1234">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="dd594-1235">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="dd594-1235">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="dd594-1236">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="dd594-1236">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="dd594-1237">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="dd594-1237">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="dd594-1238">В следующие командлеты добавлен необязательный параметр -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="dd594-1238">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="dd594-1239">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dd594-1239">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="dd594-1240">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="dd594-1240">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="dd594-1241">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="dd594-1241">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="dd594-1242">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dd594-1242">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="dd594-1243">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="dd594-1243">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="dd594-1244">New-AzureRmApplicationGatewayUrlPathMapConfig добавил с помощью идентификатора поддержку KeyVault для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="dd594-1244">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="dd594-1245">В следующие командлеты добавлен необязательный параметр -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="dd594-1245">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="dd594-1246">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="dd594-1246">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="dd594-1247">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="dd594-1247">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="dd594-1248">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="dd594-1248">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="dd594-1249">В командлет New-AzApplicationGateway добавлен необязательный параметр -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="dd594-1249">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="dd594-1250">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="dd594-1250">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="dd594-1251">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="dd594-1251">Az.OperationalInsights</span></span>
- <span data-ttu-id="dd594-1252">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="dd594-1252">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="dd594-1253">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="dd594-1253">Az.Profile</span></span>
- <span data-ttu-id="dd594-1254">Имя модуля изменено на Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="dd594-1254">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="dd594-1255">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dd594-1255">Az.RecoveryServices</span></span>
- <span data-ttu-id="dd594-1256">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="dd594-1256">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="dd594-1257">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd594-1257">Az.Resources</span></span>
- <span data-ttu-id="dd594-1258">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="dd594-1258">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="dd594-1259">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dd594-1259">Az.ServiceFabric</span></span>
- <span data-ttu-id="dd594-1260">Поддержка спецификации сертификата по общему имени и отпечатку</span><span class="sxs-lookup"><span data-stu-id="dd594-1260">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="dd594-1261">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="dd594-1261">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="dd594-1262">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="dd594-1262">Az.SIgnalR</span></span>
- <span data-ttu-id="dd594-1263">Общедоступная версия командлетов PowerShell для SIgnalR</span><span class="sxs-lookup"><span data-stu-id="dd594-1263">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="dd594-1264">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd594-1264">Az.Sql</span></span>
- <span data-ttu-id="dd594-1265">Добавлены новые типы обнаружения Data_Exfiltration и Unsafe_Action в командлеты обнаружения угроз</span><span class="sxs-lookup"><span data-stu-id="dd594-1265">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="dd594-1266">Примеры обновленной документации для командлетов аудита Sql</span><span class="sxs-lookup"><span data-stu-id="dd594-1266">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="dd594-1267">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="dd594-1267">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="dd594-1268">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dd594-1268">Az.Storage</span></span>
- <span data-ttu-id="dd594-1269">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="dd594-1269">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="dd594-1270">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dd594-1270">Az.Websites</span></span>
- <span data-ttu-id="dd594-1271">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="dd594-1271">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="dd594-1272">0.7.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="dd594-1272">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="dd594-1273">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="dd594-1273">General</span></span>

* <span data-ttu-id="dd594-1274">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="dd594-1274">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="dd594-1275">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd594-1275">Az.Compute</span></span>

* <span data-ttu-id="dd594-1276">Добавлена поддержка UltraSSD и образов коллекции в простых наборах параметров для командлетов `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="dd594-1276">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="dd594-1277">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dd594-1277">Az.DataLakeStore</span></span>

* <span data-ttu-id="dd594-1278">Исправлено косую черту в конце домена учетной записи ADLS</span><span class="sxs-lookup"><span data-stu-id="dd594-1278">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="dd594-1279">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="dd594-1279">Az.FrontDoor</span></span>

* <span data-ttu-id="dd594-1280">Исправлены некоторые неработающие ссылки</span><span class="sxs-lookup"><span data-stu-id="dd594-1280">Fixed some broken links</span></span>
    - <span data-ttu-id="dd594-1281">В статьях New-AzureRmFrontDoor и Set-AzureRmFrontDoor исправлена ссылка на статью командлета New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="dd594-1281">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="dd594-1282">В статье New-AzureRmFrontDoorManagedRuleObject исправлена ссылка на статью командлета New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="dd594-1282">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="dd594-1283">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dd594-1283">Az.RecoveryServices</span></span>

* <span data-ttu-id="dd594-1284">Добавлены проверки на стороне клиента для операций восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="dd594-1284">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="dd594-1285">StorageAccountName и storageAccountResourceGroupName являются необязательными для восстановления afs.</span><span class="sxs-lookup"><span data-stu-id="dd594-1285">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="dd594-1286">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd594-1286">Az.Resources</span></span>

* <span data-ttu-id="dd594-1287">Исправление для https://github.com/Azure/azure-powershell/issues/7679.</span><span class="sxs-lookup"><span data-stu-id="dd594-1287">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="dd594-1288">Обновите Get-AzureRmRoleAssignment, чтобы использовать область подписки, если она указана при запросе классических администраторов.</span><span class="sxs-lookup"><span data-stu-id="dd594-1288">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="dd594-1289">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd594-1289">Az.Sql</span></span>

* <span data-ttu-id="dd594-1290">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="dd594-1290">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="dd594-1291">Устранена проблема с использованием Get-AzureRmSqlDatabaseVulnerabilityAssessment с .NET Core.</span><span class="sxs-lookup"><span data-stu-id="dd594-1291">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="dd594-1292">Изменена документация справочных сообщений, связанных с командлетами аудита SQL.</span><span class="sxs-lookup"><span data-stu-id="dd594-1292">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="dd594-1293">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dd594-1293">Az.Storage</span></span>

* <span data-ttu-id="dd594-1294">Добавлено -EnableHierarchicalNamespace к New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dd594-1294">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="dd594-1295">Устранена проблема, из-за которой командлет Copy File не может повторно использовать исходный контекст в пункте назначения, если не введен -DestContext</span><span class="sxs-lookup"><span data-stu-id="dd594-1295">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="dd594-1296">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="dd594-1296">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="dd594-1297">Поддержка статической конфигурации сайта</span><span class="sxs-lookup"><span data-stu-id="dd594-1297">Support Static Website configuration</span></span>
    - <span data-ttu-id="dd594-1298">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="dd594-1298">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="dd594-1299">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="dd594-1299">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="dd594-1300">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dd594-1300">Az.Websites</span></span>

* <span data-ttu-id="dd594-1301">Set-AzureRmWebApp и Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="dd594-1301">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="dd594-1302">Добавлен новый параметр (-AzureStoragePath), который указывает путь службы хранилища Azure для подключения в приложениях-контейнерах Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="dd594-1302">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="dd594-1303">Используйте выходные данные нового командлета New-AzureRmWebAppAzureStoragePath в качестве параметра, чтобы задать пути к службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="dd594-1303">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="dd594-1304">0.6.1 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="dd594-1304">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="dd594-1305">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="dd594-1305">Az.ApiManagement</span></span>
* <span data-ttu-id="dd594-1306">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="dd594-1306">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="dd594-1307">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dd594-1307">Az.Automation</span></span>
* <span data-ttu-id="dd594-1308">Командлеты службы автоматизации Azure на базе Swagger.</span><span class="sxs-lookup"><span data-stu-id="dd594-1308">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="dd594-1309">Добавлены командлеты для Управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="dd594-1309">Added Update Management cmdlets</span></span>
* <span data-ttu-id="dd594-1310">Добавлены командлеты для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="dd594-1310">Added Source Control cmdlets</span></span>
* <span data-ttu-id="dd594-1311">Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="dd594-1311">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="dd594-1312">Исправлена команда DSC для регистрации узла.</span><span class="sxs-lookup"><span data-stu-id="dd594-1312">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="dd594-1313">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd594-1313">Az.Compute</span></span>
* <span data-ttu-id="dd594-1314">Исправлена проблема с удостоверением, назначаемым системой.</span><span class="sxs-lookup"><span data-stu-id="dd594-1314">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="dd594-1315">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="dd594-1315">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="dd594-1316">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="dd594-1316">Az.ContainerInstance</span></span>
* <span data-ttu-id="dd594-1317">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="dd594-1317">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="dd594-1318">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="dd594-1318">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="dd594-1319">Обновлено описание в примерах командлетов для Marketplace.</span><span class="sxs-lookup"><span data-stu-id="dd594-1319">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="dd594-1320">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dd594-1320">Az.Network</span></span>
* <span data-ttu-id="dd594-1321">Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="dd594-1321">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="dd594-1322">Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="dd594-1322">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="dd594-1323">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="dd594-1323">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="dd594-1324">Исправлены проблемы с использованием памяти в карте виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="dd594-1324">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="dd594-1325">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="dd594-1325">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="dd594-1326">Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="dd594-1326">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="dd594-1327">Параметры часового пояса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="dd594-1327">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="dd594-1328">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="dd594-1328">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="dd594-1329">Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="dd594-1329">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="dd594-1330">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="dd594-1330">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="dd594-1331">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="dd594-1331">Az.Relay</span></span>
* <span data-ttu-id="dd594-1332">Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.</span><span class="sxs-lookup"><span data-stu-id="dd594-1332">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="dd594-1333">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd594-1333">Az.Resources</span></span>
* <span data-ttu-id="dd594-1334">Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.</span><span class="sxs-lookup"><span data-stu-id="dd594-1334">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="dd594-1335">Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.</span><span class="sxs-lookup"><span data-stu-id="dd594-1335">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="dd594-1336">Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.</span><span class="sxs-lookup"><span data-stu-id="dd594-1336">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="dd594-1337">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dd594-1337">Az.ServiceFabric</span></span>
* <span data-ttu-id="dd594-1338">Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.</span><span class="sxs-lookup"><span data-stu-id="dd594-1338">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="dd594-1339">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd594-1339">Az.Sql</span></span>
* <span data-ttu-id="dd594-1340">Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="dd594-1340">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="dd594-1341">Get-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="dd594-1341">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="dd594-1342">New-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="dd594-1342">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="dd594-1343">Set-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="dd594-1343">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="dd594-1344">Remove-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="dd594-1344">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="dd594-1345">Get-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="dd594-1345">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="dd594-1346">New-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="dd594-1346">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="dd594-1347">Restore-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="dd594-1347">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="dd594-1348">Remove-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="dd594-1348">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="dd594-1349">Добавлено расширенное управление политиками аудита для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="dd594-1349">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="dd594-1350">Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="dd594-1350">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="dd594-1351">Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.</span><span class="sxs-lookup"><span data-stu-id="dd594-1351">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="dd594-1352">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="dd594-1352">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="dd594-1353">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="dd594-1353">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="dd594-1354">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="dd594-1354">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="dd594-1355">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="dd594-1355">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="dd594-1356">Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="dd594-1356">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="dd594-1357">0.5.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="dd594-1357">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="dd594-1358">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="dd594-1358">General</span></span>
* <span data-ttu-id="dd594-1359">Добавлены средства заполнения ресурсов для многих основных командлетов — они позволяют вам переключать существующие имена ресурсов при вызове командлетов в интерактивном режиме</span><span class="sxs-lookup"><span data-stu-id="dd594-1359">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="dd594-1360">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="dd594-1360">Az.Profile</span></span>
* <span data-ttu-id="dd594-1361">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dd594-1361">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="dd594-1362">В командлете Connect-AzAccount параметр TenantId переименован в Tenant и добавлен псевдоним для TenantId</span><span class="sxs-lookup"><span data-stu-id="dd594-1362">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="dd594-1363">Обновлено описание TenantId для командлета Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="dd594-1363">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="dd594-1364">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="dd594-1364">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="dd594-1365">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="dd594-1365">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="dd594-1366">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="dd594-1366">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="dd594-1367">Устранена проблема, при которой командлет Disconnect-AzAccount вызывал сбой при отсутствии подключения</span><span class="sxs-lookup"><span data-stu-id="dd594-1367">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="dd594-1368">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="dd594-1368">Az.CognitiveServices</span></span>
* <span data-ttu-id="dd594-1369">Добавлена операция Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="dd594-1369">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dd594-1370">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd594-1370">Az.Compute</span></span>
* <span data-ttu-id="dd594-1371">Добавлены командлеты Add-AzVmssVMDataDisk и Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="dd594-1371">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="dd594-1372">Get-AzVMImage отображает AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="dd594-1372">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="dd594-1373">Устранена проблема, при которой значения параметров SetAzVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="dd594-1373">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="dd594-1374">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dd594-1374">Az.DataLakeStore</span></span>
* <span data-ttu-id="dd594-1375">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="dd594-1375">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="dd594-1376">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="dd594-1376">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="dd594-1377">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="dd594-1377">Az.Insights</span></span>
* <span data-ttu-id="dd594-1378">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="dd594-1378">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="dd594-1379">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="dd594-1379">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="dd594-1380">Исправлена проблема № 7513 [Insights], при которой для командлета Set-AzDiagnosticSetting требовалось явное указание категорий во время создания параметра</span><span class="sxs-lookup"><span data-stu-id="dd594-1380">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="dd594-1381">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="dd594-1381">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dd594-1382">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dd594-1382">Az.Network</span></span>
* <span data-ttu-id="dd594-1383">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="dd594-1383">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="dd594-1384">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="dd594-1384">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="dd594-1385">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="dd594-1385">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="dd594-1386">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="dd594-1386">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="dd594-1387">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="dd594-1387">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="dd594-1388">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="dd594-1388">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="dd594-1389">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="dd594-1389">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="dd594-1390">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="dd594-1390">Az.PolicyInsights</span></span>
* <span data-ttu-id="dd594-1391">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="dd594-1391">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="dd594-1392">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd594-1392">Az.Resources</span></span>
* <span data-ttu-id="dd594-1393">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="dd594-1393">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="dd594-1394">Разрешено перечисление ресурсов с помощью параметра -ResourceId для командлета Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="dd594-1394">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="dd594-1395">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="dd594-1395">Az.ServiceBus</span></span>
* <span data-ttu-id="dd594-1396">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="dd594-1396">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="dd594-1397">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dd594-1397">Az.ServiceFabric</span></span>
* <span data-ttu-id="dd594-1398">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="dd594-1398">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="dd594-1399">Исправлен командлет Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="dd594-1399">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="dd594-1400">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="dd594-1400">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="dd594-1401">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="dd594-1401">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="dd594-1402">Исправлен командлет Update-AzServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="dd594-1402">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="dd594-1403">0.4.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="dd594-1403">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="dd594-1404">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="dd594-1404">Az.Profile</span></span>
* <span data-ttu-id="dd594-1405">Устранена проблема с Get-AzSubscription в CloudShell</span><span class="sxs-lookup"><span data-stu-id="dd594-1405">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="dd594-1406">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="dd594-1406">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dd594-1407">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd594-1407">Az.Compute</span></span>
* <span data-ttu-id="dd594-1408">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzVm</span><span class="sxs-lookup"><span data-stu-id="dd594-1408">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="dd594-1409">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="dd594-1409">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="dd594-1410">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dd594-1410">Az.DataLakeStore</span></span>
* <span data-ttu-id="dd594-1411">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="dd594-1411">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="dd594-1412">Get-AzDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="dd594-1412">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="dd594-1413">Add-AzDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="dd594-1413">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="dd594-1414">Set-AzDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="dd594-1414">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="dd594-1415">Remove-AzDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="dd594-1415">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dd594-1416">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dd594-1416">Az.Network</span></span>
* <span data-ttu-id="dd594-1417">Обновлен командлет Test-AzNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="dd594-1417">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="dd594-1418">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="dd594-1418">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="dd594-1419">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd594-1419">Az.Resources</span></span>
* <span data-ttu-id="dd594-1420">Устранена проблема, из-за которой командлет Get-AzRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), благодаря добавлению понятного исключения в сценарий.</span><span class="sxs-lookup"><span data-stu-id="dd594-1420">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="dd594-1421">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="dd594-1421">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="dd594-1422">0.3.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="dd594-1422">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="dd594-1423">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="dd594-1423">Azure.Storage</span></span>
* <span data-ttu-id="dd594-1424">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="dd594-1424">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="dd594-1425">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="dd594-1425">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="dd594-1426">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="dd594-1426">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="dd594-1427">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="dd594-1427">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="dd594-1428">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="dd594-1428">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="dd594-1429">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="dd594-1429">Az.CognitiveServices</span></span>
* <span data-ttu-id="dd594-1430">Поддержка Get-AzCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="dd594-1430">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dd594-1431">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd594-1431">Az.Compute</span></span>
* <span data-ttu-id="dd594-1432">Исправлена команда Get-AzVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов</span><span class="sxs-lookup"><span data-stu-id="dd594-1432">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="dd594-1433">Добавлен пример использования SimpleParameterSet в справку командлета New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="dd594-1433">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="dd594-1434">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="dd594-1434">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="dd594-1435">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="dd594-1435">Az.DataFactoryV2</span></span>
* <span data-ttu-id="dd594-1436">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="dd594-1436">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dd594-1437">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dd594-1437">Az.Network</span></span>
* <span data-ttu-id="dd594-1438">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="dd594-1438">Added NetworkProfile functionality.</span></span> <span data-ttu-id="dd594-1439">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="dd594-1439">new cmdlets added</span></span>
    - <span data-ttu-id="dd594-1440">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="dd594-1440">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="dd594-1441">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="dd594-1441">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="dd594-1442">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="dd594-1442">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="dd594-1443">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="dd594-1443">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="dd594-1444">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="dd594-1444">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="dd594-1445">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="dd594-1445">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="dd594-1446">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="dd594-1446">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="dd594-1447">Добавлены командлеты: New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="dd594-1447">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="dd594-1448">Добавлены командлеты: Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="dd594-1448">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="dd594-1449">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="dd594-1449">Az.RedisCache</span></span>
* <span data-ttu-id="dd594-1450">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="dd594-1450">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="dd594-1451">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="dd594-1451">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="dd594-1452">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd594-1452">Az.Resources</span></span>
* <span data-ttu-id="dd594-1453">Добавлен отсутствующий параметр -Mode в командлет Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="dd594-1453">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="dd594-1454">Исправлена ошибка командлета Get-AzProviderOperation для операций, когда Origin содержит User</span><span class="sxs-lookup"><span data-stu-id="dd594-1454">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="dd594-1455">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd594-1455">Az.Sql</span></span>
* <span data-ttu-id="dd594-1456">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="dd594-1456">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dd594-1457">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dd594-1457">Az.Websites</span></span>
* <span data-ttu-id="dd594-1458">Новый командлет Get-AzWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="dd594-1458">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="dd594-1459">Новые командлеты New-AzWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows</span><span class="sxs-lookup"><span data-stu-id="dd594-1459">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="dd594-1460">0.2.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="dd594-1460">0.2.0 - September 2018</span></span>
 <span data-ttu-id="dd594-1461">Первый выпуск</span><span class="sxs-lookup"><span data-stu-id="dd594-1461">Initial Release</span></span>