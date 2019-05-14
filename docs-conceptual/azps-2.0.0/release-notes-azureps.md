---
ms.openlocfilehash: 3848f7fb8e298d137c747405f32a0776c1a8f029
ms.sourcegitcommit: accff0c2cd6035fcda2d917f6051a5b509eb6255
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/06/2019
ms.locfileid: "65048637"
---
## <a name="200---may-2019"></a><span data-ttu-id="12fb8-101">2.0.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="12fb8-101">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="12fb8-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="12fb8-102">Az.Accounts</span></span>
* <span data-ttu-id="12fb8-103">Обновлена библиотека аутентификации для устранения проблем с ADFS при использовании аутентификации на основе имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="12fb8-103">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="12fb8-104">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="12fb8-104">Az.CognitiveServices</span></span>
* <span data-ttu-id="12fb8-105">Отображается только заявление об отказе Bing для служб Поиска Bing.</span><span class="sxs-lookup"><span data-stu-id="12fb8-105">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="12fb8-106">Исправлена проблема с созданием учетной записи.</span><span class="sxs-lookup"><span data-stu-id="12fb8-106">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="12fb8-107">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="12fb8-107">Az.Compute</span></span>
* <span data-ttu-id="12fb8-108">Функция группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="12fb8-108">Proximity placement group feature.</span></span>
    - <span data-ttu-id="12fb8-109">Добавлены следующие новые командлеты:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="12fb8-109">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="12fb8-110">Новый параметр ProximityPlacementGroupId будет добавлен в следующие командлеты:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="12fb8-110">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="12fb8-111">В командлет New-AzGalleryImageVersion добавлен параметр StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="12fb8-111">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="12fb8-112">TargetRegion в командлете New-AzGalleryImageVersion может содержать StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="12fb8-112">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="12fb8-113">Параметр-переключатель SkipShutdown добавлен в командлеты Stop-AzVM и Stop-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="12fb8-113">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="12fb8-114">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="12fb8-114">Breaking changes</span></span>
    - <span data-ttu-id="12fb8-115">Командлет SET-AzVMBootDiagnostics изменен на Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="12fb8-115">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="12fb8-116">Командлет Export-AzLogAnalyticThrottledRequests изменен на Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="12fb8-116">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="12fb8-117">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="12fb8-117">Az.DeploymentManager</span></span>
* <span data-ttu-id="12fb8-118">Первая общедоступная версия командлетов диспетчера развертывания Azure</span><span class="sxs-lookup"><span data-stu-id="12fb8-118">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="12fb8-119">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="12fb8-119">Az.Dns</span></span>
* <span data-ttu-id="12fb8-120">Автоматическое делегирование DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="12fb8-120">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="12fb8-121">Командлет для создания зоны DNS принимает имя родительской зоны в качестве дополнительного необязательного параметра.</span><span class="sxs-lookup"><span data-stu-id="12fb8-121">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="12fb8-122">Он добавляет записи NS в родительской зоне для созданной дочерней зоны.</span><span class="sxs-lookup"><span data-stu-id="12fb8-122">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="12fb8-123">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="12fb8-123">Az.FrontDoor</span></span>
* <span data-ttu-id="12fb8-124">Первая общедоступная версия командлетов Azure FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="12fb8-124">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="12fb8-125">Переименованы командлеты WAF для включения Waf.</span><span class="sxs-lookup"><span data-stu-id="12fb8-125">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="12fb8-126">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="12fb8-126">Az.HDInsight</span></span>
* <span data-ttu-id="12fb8-127">Удалены два командлета:</span><span class="sxs-lookup"><span data-stu-id="12fb8-127">Removed two cmdlets:</span></span>
    - <span data-ttu-id="12fb8-128">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="12fb8-128">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="12fb8-129">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="12fb8-129">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="12fb8-130">Добавлен новый командлет Set-AzHDInsightGatewayCredential для замены Grant-AzHDInsightHttpServicesAccess.</span><span class="sxs-lookup"><span data-stu-id="12fb8-130">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="12fb8-131">Обновлен командлет Get-AzHDInsightJobOutput для различения ролей читателя и оператора HDInsight:</span><span class="sxs-lookup"><span data-stu-id="12fb8-131">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="12fb8-132">Пользователям с ролью читателя не нужно указывать параметр DefaultStorageAccountKey явным образом, иначе возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="12fb8-132">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="12fb8-133">На пользователей с ролью оператора HDInsight это не повлияет.</span><span class="sxs-lookup"><span data-stu-id="12fb8-133">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="12fb8-134">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="12fb8-134">Az.Monitor</span></span>
* <span data-ttu-id="12fb8-135">Новые командлеты для API SQR (запланированное правило запросов)</span><span class="sxs-lookup"><span data-stu-id="12fb8-135">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="12fb8-136">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="12fb8-136">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="12fb8-137">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="12fb8-137">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="12fb8-138">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="12fb8-138">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="12fb8-139">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="12fb8-139">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="12fb8-140">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="12fb8-140">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="12fb8-141">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="12fb8-141">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="12fb8-142">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="12fb8-142">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="12fb8-143">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="12fb8-143">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="12fb8-144">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="12fb8-144">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="12fb8-145">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="12fb8-145">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="12fb8-146">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="12fb8-146">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="12fb8-147">См. подробнее об [API SQR](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules).</span><span class="sxs-lookup"><span data-stu-id="12fb8-147">[More](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="12fb8-148">Обновлен файл Az.Monitor.md для включения командлетов для правила генерации оповещений на основе метрик GenV2(не классическая версия).</span><span class="sxs-lookup"><span data-stu-id="12fb8-148">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="12fb8-149">Az.Network</span><span class="sxs-lookup"><span data-stu-id="12fb8-149">Az.Network</span></span>
* <span data-ttu-id="12fb8-150">Добавлена поддержка для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="12fb8-150">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="12fb8-151">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="12fb8-151">New cmdlets</span></span>
        - <span data-ttu-id="12fb8-152">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="12fb8-152">New-AzNatGateway</span></span>
        - <span data-ttu-id="12fb8-153">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="12fb8-153">Get-AzNatGateway</span></span>
        - <span data-ttu-id="12fb8-154">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="12fb8-154">Set-AzNatGateway</span></span>
        - <span data-ttu-id="12fb8-155">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="12fb8-155">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="12fb8-156">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="12fb8-156">Updated cmdlets</span></span>
        - <span data-ttu-id="12fb8-157">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="12fb8-157">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="12fb8-158">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="12fb8-158">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="12fb8-159">Обновлены следующие команды для функции: Настройка и удаление пользовательских маршрутов через шлюз в Бруклине.</span><span class="sxs-lookup"><span data-stu-id="12fb8-159">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="12fb8-160">Обновлен командлет New-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="12fb8-160">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="12fb8-161">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="12fb8-161">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="12fb8-162">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="12fb8-162">Az.PolicyInsights</span></span>
* <span data-ttu-id="12fb8-163">Добавлена поддержка сведений об оценке политики запросов.</span><span class="sxs-lookup"><span data-stu-id="12fb8-163">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="12fb8-164">Добавлен параметр -Expand в командлет Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="12fb8-164">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="12fb8-165">Добавлена поддержка -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="12fb8-165">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="12fb8-166">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="12fb8-166">Az.RecoveryServices</span></span>
* <span data-ttu-id="12fb8-167">Добавлена поддержка перекрестной подписки на Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="12fb8-167">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="12fb8-168">Добавлена возможность отмечать предстоящие критически важные изменения для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="12fb8-168">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="12fb8-169">Исправлены план восстановления и план действий для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="12fb8-169">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="12fb8-170">Исправлено сетевое сопоставление обновления Azure Site Recovery (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="12fb8-170">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="12fb8-171">Исправлено направление защиты обновления Azure Site Recovery для управляемых дисков (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="12fb8-171">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="12fb8-172">Добавлены другие незначительные исправления.</span><span class="sxs-lookup"><span data-stu-id="12fb8-172">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="12fb8-173">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="12fb8-173">Az.Relay</span></span>
* <span data-ttu-id="12fb8-174">Исправлены опечатки в сообщениях для клиентов.</span><span class="sxs-lookup"><span data-stu-id="12fb8-174">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="12fb8-175">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="12fb8-175">Az.ServiceBus</span></span>
* <span data-ttu-id="12fb8-176">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="12fb8-176">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="12fb8-177">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="12fb8-177">Az.Storage</span></span>
* <span data-ttu-id="12fb8-178">Выполнено обновление клиентской библиотеки хранилища до версии 10.0.1 (пространство имен всех объектов из этого пакета SDK изменено с Microsoft.WindowsAzure.Storage. *на Microsoft.Azure.Storage*).</span><span class="sxs-lookup"><span data-stu-id="12fb8-178">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="12fb8-179">Выполнено обновление до Microsoft.Azure.Management.Storage версии 11.0.0 для включения поддержки нового API версии 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="12fb8-179">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="12fb8-180">Значение свойства Kind по умолчанию в учетной записи хранения изменено со Storage на StorageV2.</span><span class="sxs-lookup"><span data-stu-id="12fb8-180">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="12fb8-181">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="12fb8-181">New-AzStorageAccount</span></span>
* <span data-ttu-id="12fb8-182">Изменено значение Sku.Name в выходных данных командлета учетной записи хранения в соответствии со значением Sku.Name во входных данных путем добавления _ (например, StandardLRS изменено на Standard_LRS).</span><span class="sxs-lookup"><span data-stu-id="12fb8-182">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="12fb8-183">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="12fb8-183">New-AzStorageAccount</span></span>
    - <span data-ttu-id="12fb8-184">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="12fb8-184">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="12fb8-185">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="12fb8-185">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="12fb8-186">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="12fb8-186">Az.Websites</span></span>
* <span data-ttu-id="12fb8-187">Свойство Kind теперь будет задаваться объектам PSSite, возвращаемым командлетом Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="12fb8-187">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="12fb8-188">Get-AzWebApp\*Metrics и Get-AzAppServicePlanMetrics считаются нерекомендуемыми.</span><span class="sxs-lookup"><span data-stu-id="12fb8-188">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="12fb8-189">1.8.0 — апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="12fb8-189">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="12fb8-190">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="12fb8-190">Highlights since the last major release</span></span>
* <span data-ttu-id="12fb8-191">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="12fb8-191">General availability of `Az` module</span></span>
* <span data-ttu-id="12fb8-192">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="12fb8-192">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="12fb8-193">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="12fb8-193">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="12fb8-194">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="12fb8-194">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="12fb8-195">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="12fb8-195">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="12fb8-196">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="12fb8-196">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="12fb8-197">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="12fb8-197">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="12fb8-198">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="12fb8-198">Az.Accounts</span></span>
* <span data-ttu-id="12fb8-199">Обновлен командлет Uninstall-AzureRm для правильного удаления модулей в Mac.</span><span class="sxs-lookup"><span data-stu-id="12fb8-199">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="12fb8-200">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="12fb8-200">Az.Batch</span></span>
* <span data-ttu-id="12fb8-201">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="12fb8-201">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="12fb8-202">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="12fb8-202">Az.Cdn</span></span>
* <span data-ttu-id="12fb8-203">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="12fb8-203">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="12fb8-204">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="12fb8-204">Az.CognitiveServices</span></span>
* <span data-ttu-id="12fb8-205">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="12fb8-205">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="12fb8-206">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="12fb8-206">Az.Compute</span></span>
* <span data-ttu-id="12fb8-207">Устранена проблема с установкой AEM, если в идентификаторах ресурсов дисков группа ресурсов указана в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="12fb8-207">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="12fb8-208">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="12fb8-208">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="12fb8-209">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="12fb8-209">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="12fb8-210">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="12fb8-210">Az.DataFactory</span></span>
* <span data-ttu-id="12fb8-211">Добавлены свойства SsisProperties, если NodeCount не имеет значения NULL для управляемой среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="12fb8-211">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="12fb8-212">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="12fb8-212">Az.DataLakeStore</span></span>
* <span data-ttu-id="12fb8-213">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="12fb8-213">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="12fb8-214">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="12fb8-214">Az.EventGrid</span></span>
* <span data-ttu-id="12fb8-215">Обновлен текст справки для конечной точки, указывающий, что необходимо создать ресурсы, прежде чем использовать командлеты для создания или обновления подписки на события.</span><span class="sxs-lookup"><span data-stu-id="12fb8-215">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="12fb8-216">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="12fb8-216">Az.EventHub</span></span>
* <span data-ttu-id="12fb8-217">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="12fb8-217">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="12fb8-218">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="12fb8-218">Az.HDInsight</span></span>
* <span data-ttu-id="12fb8-219">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="12fb8-219">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="12fb8-220">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="12fb8-220">Az.IotHub</span></span>
* <span data-ttu-id="12fb8-221">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="12fb8-221">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="12fb8-222">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="12fb8-222">Az.KeyVault</span></span>
* <span data-ttu-id="12fb8-223">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="12fb8-223">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="12fb8-224">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="12fb8-224">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="12fb8-225">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="12fb8-225">Az.MachineLearning</span></span>
* <span data-ttu-id="12fb8-226">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="12fb8-226">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="12fb8-227">Az.Media</span><span class="sxs-lookup"><span data-stu-id="12fb8-227">Az.Media</span></span>
* <span data-ttu-id="12fb8-228">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="12fb8-228">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="12fb8-229">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="12fb8-229">Az.Monitor</span></span>
  * <span data-ttu-id="12fb8-230">Добавлены новые командлеты для правила генерации оповещений на основе метрик GenV2 (не классических).</span><span class="sxs-lookup"><span data-stu-id="12fb8-230">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="12fb8-231">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="12fb8-231">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="12fb8-232">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="12fb8-232">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="12fb8-233">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="12fb8-233">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="12fb8-234">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="12fb8-234">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="12fb8-235">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="12fb8-235">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="12fb8-236">Обновлен пакет SDK Monitor до предварительной версии 0.22.0.</span><span class="sxs-lookup"><span data-stu-id="12fb8-236">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="12fb8-237">Az.Network</span><span class="sxs-lookup"><span data-stu-id="12fb8-237">Az.Network</span></span>
* <span data-ttu-id="12fb8-238">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="12fb8-238">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="12fb8-239">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="12fb8-239">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="12fb8-240">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="12fb8-240">Az.NotificationHubs</span></span>
* <span data-ttu-id="12fb8-241">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="12fb8-241">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="12fb8-242">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="12fb8-242">Az.OperationalInsights</span></span>
* <span data-ttu-id="12fb8-243">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="12fb8-243">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="12fb8-244">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="12fb8-244">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="12fb8-245">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="12fb8-245">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="12fb8-246">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="12fb8-246">Az.RecoveryServices</span></span>
* <span data-ttu-id="12fb8-247">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="12fb8-247">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="12fb8-248">Обновлен табличный формат для SQL на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="12fb8-248">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="12fb8-249">Добавлен альтернативный метод для получения расположения в Общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="12fb8-249">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="12fb8-250">Обновлено значение ScheduleRunDays в объекте SchedulePolicy в соответствии с часовым поясом.</span><span class="sxs-lookup"><span data-stu-id="12fb8-250">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="12fb8-251">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="12fb8-251">Az.RedisCache</span></span>
* <span data-ttu-id="12fb8-252">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="12fb8-252">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="12fb8-253">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="12fb8-253">Az.Resources</span></span>
* <span data-ttu-id="12fb8-254">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="12fb8-254">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="12fb8-255">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="12fb8-255">Az.Sql</span></span>
* <span data-ttu-id="12fb8-256">Заменена зависимость от пакета SDK монитора на обычный код.</span><span class="sxs-lookup"><span data-stu-id="12fb8-256">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="12fb8-257">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="12fb8-257">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="12fb8-258">Улучшен процесс классификации нескольких столбцов.</span><span class="sxs-lookup"><span data-stu-id="12fb8-258">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="12fb8-259">Добавлены свойства SKU (имя, семейство, производительность SKU) в отклике Get-AzSqlServerServiceObjective, а также по умолчанию задан табличный формат.</span><span class="sxs-lookup"><span data-stu-id="12fb8-259">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="12fb8-260">C помощью Get-AzSqlServerServiceObjective теперь можно получать список доступных целевых служб по расположению без необходимости заранее размещать сервер в регионе.</span><span class="sxs-lookup"><span data-stu-id="12fb8-260">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="12fb8-261">Поддерживается параметр часового пояса при создании Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="12fb8-261">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="12fb8-262">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="12fb8-262">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="12fb8-263">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="12fb8-263">Az.Websites</span></span>
* <span data-ttu-id="12fb8-264">Исправлены командлеты Set-AzWebApp и Set-AzWebAppSlot, которые теперь не удаляют теги при выполнении.</span><span class="sxs-lookup"><span data-stu-id="12fb8-264">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="12fb8-265">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="12fb8-265">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="12fb8-266">Обновлен пакет SDK веб-узлов.</span><span class="sxs-lookup"><span data-stu-id="12fb8-266">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="12fb8-267">Удалено свойство AdminSiteName из PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="12fb8-267">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="12fb8-268">1.7.0 —апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="12fb8-268">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="12fb8-269">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="12fb8-269">Highlights since the last major release</span></span>
* <span data-ttu-id="12fb8-270">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="12fb8-270">General availability of `Az` module</span></span>
* <span data-ttu-id="12fb8-271">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="12fb8-271">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="12fb8-272">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="12fb8-272">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="12fb8-273">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="12fb8-273">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="12fb8-274">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="12fb8-274">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="12fb8-275">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="12fb8-275">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="12fb8-276">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="12fb8-276">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="12fb8-277">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="12fb8-277">Az.Accounts</span></span>
* <span data-ttu-id="12fb8-278">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметр AzureAnalysisServicesEndpointResourceId.</span><span class="sxs-lookup"><span data-stu-id="12fb8-278">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="12fb8-279">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="12fb8-279">Az.AnalysisServices</span></span>
* <span data-ttu-id="12fb8-280">Использование ServiceClient в командлетах плоскости данных и удаление исходной логики проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="12fb8-280">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="12fb8-281">Add-AzureASAccount используется как оболочка для Connect-AzAccount во избежание критических изменений.</span><span class="sxs-lookup"><span data-stu-id="12fb8-281">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="12fb8-282">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="12fb8-282">Az.Automation</span></span>
* <span data-ttu-id="12fb8-283">Исправлена ошибка командлета New-AzAutomationSoftwareUpdateConfiguration, связанная с включением.</span><span class="sxs-lookup"><span data-stu-id="12fb8-283">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="12fb8-284">Теперь параметры IncludedKbNumber и IncludedPackageNameMask должны работать нормально.</span><span class="sxs-lookup"><span data-stu-id="12fb8-284">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="12fb8-285">Исправлена ошибка динамической группы управления обновлениями службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="12fb8-285">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="12fb8-286">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="12fb8-286">Az.Compute</span></span>
* <span data-ttu-id="12fb8-287">В командлеты New-AzDiskConfig и New-AzSnapshotConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="12fb8-287">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="12fb8-288">Теперь можно создавать виртуальные машину на основе образов из коллекции от других клиентов.</span><span class="sxs-lookup"><span data-stu-id="12fb8-288">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="12fb8-289">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="12fb8-289">Az.ContainerInstance</span></span>
* <span data-ttu-id="12fb8-290">Исправлена проблема в параметре -Command командлета New-AzContainerGroup, из-за которой в конце добавлялся пустой аргумент.</span><span class="sxs-lookup"><span data-stu-id="12fb8-290">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="12fb8-291">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="12fb8-291">Az.DataFactory</span></span>
* <span data-ttu-id="12fb8-292">Пакет SDK для ADF .NET обновлен до версии 3.0.2.</span><span class="sxs-lookup"><span data-stu-id="12fb8-292">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="12fb8-293">Командлет Set-AzDataFactoryV2 обновлен с помощью дополнительных параметров для настроек, связанных с RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="12fb8-293">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="12fb8-294">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="12fb8-294">Az.Resources</span></span>
* <span data-ttu-id="12fb8-295">Улучшена обработка поставщиков Get-AzResource при предоставлении параметров -ResourceId или -ResourceGroupName, -Name и -ResourceType.</span><span class="sxs-lookup"><span data-stu-id="12fb8-295">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="12fb8-296">Улучшена обработка ошибок в командлетах Test-AzDeployment и Test-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="12fb8-296">Improve error handling for for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="12fb8-297">Теперь ошибки, возникающие за пределами проверки развертывания, обрабатываются и включаются в выходные данные команды.</span><span class="sxs-lookup"><span data-stu-id="12fb8-297">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="12fb8-298">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="12fb8-298">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="12fb8-299">Добавлен параметр-переключатель -IgnoreDynamicParameters, с помощью которого можно настроить командлеты развертывания так, чтобы они пропускали запросы в сценариях скриптов и заданий.</span><span class="sxs-lookup"><span data-stu-id="12fb8-299">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="12fb8-300">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="12fb8-300">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="12fb8-301">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="12fb8-301">Az.Sql</span></span>
* <span data-ttu-id="12fb8-302">Поддержка классификации данных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="12fb8-302">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="12fb8-303">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="12fb8-303">Az.Storage</span></span>
* <span data-ttu-id="12fb8-304">Подробные сообщения об ошибке передаются при создании контекста хранилища с помощью параметра -UseConnectedAccount, но без входа в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="12fb8-304">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="12fb8-305">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="12fb8-305">New-AzStorageContext</span></span>
* <span data-ttu-id="12fb8-306">Поддержка свойств службы управления BLOB-объектов в указанной учетной записи хранения с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="12fb8-306">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="12fb8-307">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="12fb8-307">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="12fb8-308">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="12fb8-308">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="12fb8-309">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="12fb8-309">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="12fb8-310">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="12fb8-310">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="12fb8-311">Поддержка параметра -AsJob в командлетах для отправки и скачивания больших двоичных объектов и файлов.</span><span class="sxs-lookup"><span data-stu-id="12fb8-311">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="12fb8-312">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="12fb8-312">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="12fb8-313">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="12fb8-313">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="12fb8-314">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="12fb8-314">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="12fb8-315">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="12fb8-315">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="12fb8-316">1.6.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="12fb8-316">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="12fb8-317">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="12fb8-317">Highlights since the last major release</span></span>
* <span data-ttu-id="12fb8-318">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="12fb8-318">General availability of `Az` module</span></span>
* <span data-ttu-id="12fb8-319">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="12fb8-319">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="12fb8-320">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="12fb8-320">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="12fb8-321">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="12fb8-321">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="12fb8-322">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="12fb8-322">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="12fb8-323">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="12fb8-323">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="12fb8-324">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="12fb8-324">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="12fb8-325">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="12fb8-325">Az.Automation</span></span>
* <span data-ttu-id="12fb8-326">В управление обновлениями службы автоматизации Azure внесены изменения для поддержки следующих новых функций:</span><span class="sxs-lookup"><span data-stu-id="12fb8-326">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="12fb8-327">динамическое группирование;</span><span class="sxs-lookup"><span data-stu-id="12fb8-327">Dynamic grouping</span></span>
    * <span data-ttu-id="12fb8-328">скрипты предварительного или последующего выполнения;</span><span class="sxs-lookup"><span data-stu-id="12fb8-328">Pre-Post script</span></span>
    * <span data-ttu-id="12fb8-329">параметр перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="12fb8-329">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="12fb8-330">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="12fb8-330">Az.Compute</span></span>
* <span data-ttu-id="12fb8-331">Устранена проблема, связанная с разрешением пути в Get-AzVmBootDiagnosticsData.</span><span class="sxs-lookup"><span data-stu-id="12fb8-331">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="12fb8-332">Обновление клиентской библиотеки вычислений до версии 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="12fb8-332">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="12fb8-333">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="12fb8-333">Az.KeyVault</span></span>
* <span data-ttu-id="12fb8-334">Добавлена поддержка подстановочных знаков в командлетах KeyVault.</span><span class="sxs-lookup"><span data-stu-id="12fb8-334">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="12fb8-335">Az.Network</span><span class="sxs-lookup"><span data-stu-id="12fb8-335">Az.Network</span></span>
* <span data-ttu-id="12fb8-336">Добавлена поддержка анализа угроз для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="12fb8-336">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="12fb8-337">Добавлены настраиваемые правила и ресурс верхнего уровня для политики брандмауэра Шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="12fb8-337">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="12fb8-338">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="12fb8-338">Az.RecoveryServices</span></span>
* <span data-ttu-id="12fb8-339">В политику виртуальной машины Azure добавлен объект SnapshotRetentionInDays для поддержки мгновенного восстановления.</span><span class="sxs-lookup"><span data-stu-id="12fb8-339">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="12fb8-340">Добавлена поддержка канала для отмены регистрации контейнера.</span><span class="sxs-lookup"><span data-stu-id="12fb8-340">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="12fb8-341">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="12fb8-341">Az.Resources</span></span>
* <span data-ttu-id="12fb8-342">Обновлена поддержка подстановочных знаков для Get-AzResource и Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="12fb8-342">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="12fb8-343">Обновлены учетные данные, используемые при общих вызовах к ARM.</span><span class="sxs-lookup"><span data-stu-id="12fb8-343">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="12fb8-344">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="12fb8-344">Az.Sql</span></span>
* <span data-ttu-id="12fb8-345">Изменен тип параметра (ExcludeDetectionType) командлетов для обнаружения угроз с DetectionTypes на string[] для поддержки актуального состояния при добавлении новых типов обнаружения и для поддержки автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="12fb8-345">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="12fb8-346">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="12fb8-346">Az.Storage</span></span>
* <span data-ttu-id="12fb8-347">Поддержка получения, настройки и удаления политики управления в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="12fb8-347">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="12fb8-348">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="12fb8-348">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="12fb8-349">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="12fb8-349">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="12fb8-350">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="12fb8-350">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="12fb8-351">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="12fb8-351">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="12fb8-352">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="12fb8-352">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="12fb8-353">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="12fb8-353">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="12fb8-354">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="12fb8-354">Az.Websites</span></span>
* <span data-ttu-id="12fb8-355">Исправлена ошибка с шаблоном ARM, из-за которой прерывалось клонирование все слотов при использовании New-AzWebApp -IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="12fb8-355">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="12fb8-356">1.5.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="12fb8-356">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="12fb8-357">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="12fb8-357">Az.Accounts</span></span>
* <span data-ttu-id="12fb8-358">Добавлена команда Register-AzModule для поддержки созданных командлетов AutoRest.</span><span class="sxs-lookup"><span data-stu-id="12fb8-358">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="12fb8-359">Обновлены примеры для Connect AzAccount.</span><span class="sxs-lookup"><span data-stu-id="12fb8-359">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="12fb8-360">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="12fb8-360">Az.Automation</span></span>
* <span data-ttu-id="12fb8-361">Исправлена проблема с получением некоторых ежемесячных расписаний в нескольких командлетах службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="12fb8-361">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="12fb8-362">Исправлен командлет Get-AzAutomationDscNode, возвращающий только первые 20 узлов.</span><span class="sxs-lookup"><span data-stu-id="12fb8-362">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="12fb8-363">Теперь он возвращает все узлы.</span><span class="sxs-lookup"><span data-stu-id="12fb8-363">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="12fb8-364">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="12fb8-364">Az.Cdn</span></span>
* <span data-ttu-id="12fb8-365">Добавлены новые командлеты PowerShell для включения и отключения HTTPS для личного домена и отключены устаревшие командлеты.</span><span class="sxs-lookup"><span data-stu-id="12fb8-365">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="12fb8-366">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="12fb8-366">Az.Compute</span></span>
* <span data-ttu-id="12fb8-367">Добавлена поддержка подстановочных знаков в командлетах Get.</span><span class="sxs-lookup"><span data-stu-id="12fb8-367">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="12fb8-368">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="12fb8-368">Az.DataFactory</span></span>
* <span data-ttu-id="12fb8-369">Обновлен пакет SDK для ADF .NET до версии 3.0.1.</span><span class="sxs-lookup"><span data-stu-id="12fb8-369">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="12fb8-370">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="12fb8-370">Az.LogicApp</span></span>
* <span data-ttu-id="12fb8-371">Исправлена проблема с получением только первой страницы результатов при выполнении команды ListWorkflows.</span><span class="sxs-lookup"><span data-stu-id="12fb8-371">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="12fb8-372">Az.Network</span><span class="sxs-lookup"><span data-stu-id="12fb8-372">Az.Network</span></span>
* <span data-ttu-id="12fb8-373">Добавлена поддержка подстановочных знаков в командлетах Network.</span><span class="sxs-lookup"><span data-stu-id="12fb8-373">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="12fb8-374">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="12fb8-374">Az.RecoveryServices</span></span>
* <span data-ttu-id="12fb8-375">Добавлена поддержка SQL Server на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="12fb8-375">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="12fb8-376">Обновление пакета SDK</span><span class="sxs-lookup"><span data-stu-id="12fb8-376">SDK Update</span></span>
* <span data-ttu-id="12fb8-377">Удалена проверка VMappContainer в Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="12fb8-377">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="12fb8-378">Добавлены параметры Name и ServerName для Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="12fb8-378">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="12fb8-379">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="12fb8-379">Az.Resources</span></span>
* <span data-ttu-id="12fb8-380">Добавлен параметр `-TemplateObject` в командлеты для развертывания.</span><span class="sxs-lookup"><span data-stu-id="12fb8-380">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="12fb8-381">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2933.</span><span class="sxs-lookup"><span data-stu-id="12fb8-381">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="12fb8-382">Устранена проблема с передачей в конвейер результата `Get-AzResource` для `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="12fb8-382">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="12fb8-383">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8240.</span><span class="sxs-lookup"><span data-stu-id="12fb8-383">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="12fb8-384">Устранена проблема с изменением типа данных JSON при выполнении `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="12fb8-384">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="12fb8-385">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7930.</span><span class="sxs-lookup"><span data-stu-id="12fb8-385">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="12fb8-386">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="12fb8-386">Az.Sql</span></span>
* <span data-ttu-id="12fb8-387">Обновление AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="12fb8-387">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="12fb8-388">Исправлено поведение для пограничного случая при создании параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="12fb8-388">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="12fb8-389">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="12fb8-389">Az.Storage</span></span>
* <span data-ttu-id="12fb8-390">Включена поддержка Kind BlockBlobStorage при создании учетной записи хранения для New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="12fb8-390">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="12fb8-391">1.4.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="12fb8-391">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="12fb8-392">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="12fb8-392">Az.AnalysisServices</span></span>
* <span data-ttu-id="12fb8-393">Командлет AddAzureASAccount устарел.</span><span class="sxs-lookup"><span data-stu-id="12fb8-393">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="12fb8-394">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="12fb8-394">Az.Automation</span></span>
* <span data-ttu-id="12fb8-395">Обновлена справка для командлета Import-AzAutomationDscNodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="12fb8-395">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="12fb8-396">Добавлена проверка имени конфигурации для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="12fb8-396">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="12fb8-397">Улучшена обработка ошибок для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="12fb8-397">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="12fb8-398">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="12fb8-398">Az.CognitiveServices</span></span>
* <span data-ttu-id="12fb8-399">Добавлен параметр CustomSubdomainName — новый необязательный параметр для командлета New-AzCognitiveServicesAccount, который указывает поддомен для ресурса.</span><span class="sxs-lookup"><span data-stu-id="12fb8-399">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="12fb8-400">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="12fb8-400">Az.Compute</span></span>
* <span data-ttu-id="12fb8-401">Устранена проблема с идентификаторами наборов параметров.</span><span class="sxs-lookup"><span data-stu-id="12fb8-401">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="12fb8-402">Обновлен командлет Get-AzVMExtension для отображения списка всех установленных расширений, если не указан параметр Name.</span><span class="sxs-lookup"><span data-stu-id="12fb8-402">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="12fb8-403">Для командлета Update-AzImage добавлены параметры Tag и ResourceId.</span><span class="sxs-lookup"><span data-stu-id="12fb8-403">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="12fb8-404">Командлет Get-AzVmssVM, который выполняется без указания идентификатора экземпляра и с параметром InstanceView, может выводить виртуальные машины из VMSS с представлением экземпляра.</span><span class="sxs-lookup"><span data-stu-id="12fb8-404">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="12fb8-405">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="12fb8-405">Az.DataLakeStore</span></span>
* <span data-ttu-id="12fb8-406">Добавлены командлеты для перечисления и восстановления удаленного элемента ADL.</span><span class="sxs-lookup"><span data-stu-id="12fb8-406">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="12fb8-407">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="12fb8-407">Az.EventHub</span></span>
* <span data-ttu-id="12fb8-408">Добавлено новое логическое свойство SkipEmptyArchives для пропуска пустых архивов в классе CaptureDescription Eventhub.</span><span class="sxs-lookup"><span data-stu-id="12fb8-408">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="12fb8-409">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="12fb8-409">Az.KeyVault</span></span>
* <span data-ttu-id="12fb8-410">Исправлена расстановка тегов для командлета Set-AzKeyVaultSecret.</span><span class="sxs-lookup"><span data-stu-id="12fb8-410">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="12fb8-411">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="12fb8-411">Az.LogicApp</span></span>
* <span data-ttu-id="12fb8-412">Добавлен SKU "Базовый" для учетных записей интеграции.</span><span class="sxs-lookup"><span data-stu-id="12fb8-412">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="12fb8-413">Добавлены типы сопоставлений Liquid, а также XSLT 2.0 и XSLT 3.0.</span><span class="sxs-lookup"><span data-stu-id="12fb8-413">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="12fb8-414">Новые командлеты для сборок учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="12fb8-414">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="12fb8-415">Get-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="12fb8-415">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="12fb8-416">New-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="12fb8-416">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="12fb8-417">Remove-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="12fb8-417">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="12fb8-418">Set-AzIntegrationAccountAssembly.</span><span class="sxs-lookup"><span data-stu-id="12fb8-418">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="12fb8-419">Новые командлеты для конфигурации пакета учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="12fb8-419">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="12fb8-420">Get-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="12fb8-420">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="12fb8-421">New-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="12fb8-421">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="12fb8-422">Remove-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="12fb8-422">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="12fb8-423">Set-AzIntegrationAccountBatchConfiguration.</span><span class="sxs-lookup"><span data-stu-id="12fb8-423">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="12fb8-424">Обновлен пакет SDK Logic Apps до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="12fb8-424">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="12fb8-425">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="12fb8-425">Az.Monitor</span></span>
* <span data-ttu-id="12fb8-426">Обновлена справка для командлета Get-AzMetric.</span><span class="sxs-lookup"><span data-stu-id="12fb8-426">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="12fb8-427">Az.Network</span><span class="sxs-lookup"><span data-stu-id="12fb8-427">Az.Network</span></span>
* <span data-ttu-id="12fb8-428">Обновлен пример справки для командлета Add-AzApplicationGatewayCustomError.</span><span class="sxs-lookup"><span data-stu-id="12fb8-428">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="12fb8-429">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="12fb8-429">Az.OperationalInsights</span></span>
* <span data-ttu-id="12fb8-430">Дополнительная поддержка создания и получения источников данных ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="12fb8-430">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="12fb8-431">Добавлен новый тип ApplicationInsights для получения определенных или всех источников данных ApplicationInsights для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="12fb8-431">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="12fb8-432">Добавлен командлет New-AzOperationalInsightsApplicationInsightsDataSource для создания источника данных с использованием параметров указанного ресурса Application-Insightss: subscription Id, resourceGroupName и name.</span><span class="sxs-lookup"><span data-stu-id="12fb8-432">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="12fb8-433">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="12fb8-433">Az.Resources</span></span>
* <span data-ttu-id="12fb8-434">исправлена проблема https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="12fb8-434">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="12fb8-435">исправлена проблема https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="12fb8-435">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="12fb8-436">исправлена проблема https://github.com/Azure/azure-powershell/issues/6219.</span><span class="sxs-lookup"><span data-stu-id="12fb8-436">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="12fb8-437">Исправлена ошибка, препятствующая повторному созданию KeyCredentials.</span><span class="sxs-lookup"><span data-stu-id="12fb8-437">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="12fb8-438">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="12fb8-438">Az.Sql</span></span>
* <span data-ttu-id="12fb8-439">Добавлена поддержка уровня гипермасштабирования в базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="12fb8-439">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="12fb8-440">Исправлена ошибка, из-за которой восстановление могло завершиться со сбоем при указании ненужных свойств в запросе на восстановление.</span><span class="sxs-lookup"><span data-stu-id="12fb8-440">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="12fb8-441">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="12fb8-441">Az.Websites</span></span>
* <span data-ttu-id="12fb8-442">Исправлен пример для командлета Get-AzWebAppSlotMetrics.</span><span class="sxs-lookup"><span data-stu-id="12fb8-442">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="12fb8-443">1.3.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="12fb8-443">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="12fb8-444">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="12fb8-444">Az.Accounts</span></span>
* <span data-ttu-id="12fb8-445">Обновление до последней версии ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="12fb8-445">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="12fb8-446">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="12fb8-446">Az.AnalysisServices</span></span>
<span data-ttu-id="12fb8-447">Общедоступная версия модуля Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="12fb8-447">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="12fb8-448">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="12fb8-448">Az.Compute</span></span>
* <span data-ttu-id="12fb8-449">Расширение AEM: добавлена поддержка дисков UltraSSD, P60, P70 и P80.</span><span class="sxs-lookup"><span data-stu-id="12fb8-449">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="12fb8-450">Обновлено описание справки для командлета Set-AzVMBootDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="12fb8-450">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="12fb8-451">Обновлено описание справки и пример для командлета Update-AzImage.</span><span class="sxs-lookup"><span data-stu-id="12fb8-451">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="12fb8-452">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="12fb8-452">Az.RecoveryServices</span></span>
<span data-ttu-id="12fb8-453">Общедоступная версия модуля Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="12fb8-453">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="12fb8-454">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="12fb8-454">Az.Resources</span></span>
* <span data-ttu-id="12fb8-455">Исправлена расстановка тегов для групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="12fb8-455">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="12fb8-456">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="12fb8-456">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="12fb8-457">Исправлена проблема с игнорированием командлетом `Get-AzureRmRoleAssignment` параметра -ErrorAction.</span><span class="sxs-lookup"><span data-stu-id="12fb8-457">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="12fb8-458">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="12fb8-458">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="12fb8-459">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="12fb8-459">Az.Sql</span></span>
* <span data-ttu-id="12fb8-460">Добавлен командлет Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="12fb8-460">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="12fb8-461">Исправлена проблема с появлением исключения NullRef при выполнении командлетов SQL, если не выполнен вход в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="12fb8-461">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="12fb8-462">Исправлено исключение NullRef в командлете Get-AzSqlCapability.</span><span class="sxs-lookup"><span data-stu-id="12fb8-462">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="12fb8-463">1.2.1 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="12fb8-463">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="12fb8-464">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="12fb8-464">Az.Accounts</span></span>
* <span data-ttu-id="12fb8-465">Выпуск с правильной версией службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="12fb8-465">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="12fb8-466">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="12fb8-466">Az.AnalysisServices</span></span>
* <span data-ttu-id="12fb8-467">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="12fb8-467">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="12fb8-468">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="12fb8-468">Az.RecoveryServices</span></span>
* <span data-ttu-id="12fb8-469">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="12fb8-469">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="12fb8-470">1.2.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="12fb8-470">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="12fb8-471">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="12fb8-471">Az.Accounts</span></span>
* <span data-ttu-id="12fb8-472">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="12fb8-472">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="12fb8-473">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="12fb8-473">Update incorrect online help URLs</span></span>
* <span data-ttu-id="12fb8-474">Добавлено предупреждающее сообщение в PS Core для модуля Uninstall-AzureRm.</span><span class="sxs-lookup"><span data-stu-id="12fb8-474">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="12fb8-475">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="12fb8-475">Az.Aks</span></span>
* <span data-ttu-id="12fb8-476">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="12fb8-476">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="12fb8-477">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="12fb8-477">Az.Automation</span></span>
* <span data-ttu-id="12fb8-478">Добавлена поддержка для модулей runbook Python 2.</span><span class="sxs-lookup"><span data-stu-id="12fb8-478">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="12fb8-479">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="12fb8-479">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="12fb8-480">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="12fb8-480">Az.Cdn</span></span>
* <span data-ttu-id="12fb8-481">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="12fb8-481">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="12fb8-482">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="12fb8-482">Az.Compute</span></span>
* <span data-ttu-id="12fb8-483">Добавлен командлет Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="12fb8-483">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="12fb8-484">Добавлен параметр TempDisk к командлету Set-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="12fb8-484">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="12fb8-485">Исправлено предупреждающее сообщение командлета New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="12fb8-485">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="12fb8-486">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="12fb8-486">Az.ContainerRegistry</span></span>
* <span data-ttu-id="12fb8-487">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="12fb8-487">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="12fb8-488">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="12fb8-488">Az.DataFactory</span></span>
* <span data-ttu-id="12fb8-489">Пакет SDK ADF .Net обновлен до версии 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="12fb8-489">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="12fb8-490">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="12fb8-490">Az.DataLakeStore</span></span>
* <span data-ttu-id="12fb8-491">Исправлена проблема с конечной точкой ADLS при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="12fb8-491">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="12fb8-492">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7462.</span><span class="sxs-lookup"><span data-stu-id="12fb8-492">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="12fb8-493">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="12fb8-493">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="12fb8-494">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="12fb8-494">Az.IotHub</span></span>
* <span data-ttu-id="12fb8-495">Добавлен формат кодирования для командлета Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="12fb8-495">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="12fb8-496">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="12fb8-496">Az.KeyVault</span></span>
* <span data-ttu-id="12fb8-497">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="12fb8-497">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="12fb8-498">Az.Network</span><span class="sxs-lookup"><span data-stu-id="12fb8-498">Az.Network</span></span>
* <span data-ttu-id="12fb8-499">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="12fb8-499">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="12fb8-500">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="12fb8-500">Az.Resources</span></span>
* <span data-ttu-id="12fb8-501">Исправлены неправильные примеры в справочной документации по командлетам New-AzADAppCredential и New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="12fb8-501">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="12fb8-502">Исправлена проблема, при которой путь для параметра -TemplateFile не удавалось разрешить до выполнения командлетов развертывания групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="12fb8-502">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="12fb8-503">Az.Resources: исправлена документация для значения по умолчанию -Mode командлета New-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="12fb8-503">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="12fb8-504">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/7522.</span><span class="sxs-lookup"><span data-stu-id="12fb8-504">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="12fb8-505">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/5747.</span><span class="sxs-lookup"><span data-stu-id="12fb8-505">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="12fb8-506">Исправлена проблема с форматированием объекта PSResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="12fb8-506">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="12fb8-507">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2123.</span><span class="sxs-lookup"><span data-stu-id="12fb8-507">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="12fb8-508">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="12fb8-508">Az.ServiceFabric</span></span>
* <span data-ttu-id="12fb8-509">Исправлена проблема с появлением исключения в процессе отката при добавлении сертификата к модели VMSS: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="12fb8-509">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="12fb8-510">Исправлены некоторые сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="12fb8-510">Fix some error messages.</span></span>
* <span data-ttu-id="12fb8-511">Исправлена проблема с созданием кластера с шаблоном ARM по умолчанию для командлета New-AzServiceFabriCluster, который не работал с операцией миграции в Az.</span><span class="sxs-lookup"><span data-stu-id="12fb8-511">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="12fb8-512">Исправлена проблема с добавлением сертификата кластера или приложения: теперь они добавляются только в Масштабируемые наборы виртуальных машин, которые сопоставлены с кластером, путем проверки идентификатора кластера в расширении.</span><span class="sxs-lookup"><span data-stu-id="12fb8-512">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="12fb8-513">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="12fb8-513">Az.SignalR</span></span>
* <span data-ttu-id="12fb8-514">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="12fb8-514">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="12fb8-515">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="12fb8-515">Az.Sql</span></span>
* <span data-ttu-id="12fb8-516">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="12fb8-516">Update incorrect online help URLs</span></span>
* <span data-ttu-id="12fb8-517">Обновлено описание параметра LicenseType с добавлением возможных значений.</span><span class="sxs-lookup"><span data-stu-id="12fb8-517">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="12fb8-518">Исправлена проблема с неправильным обновлением удостоверения управляемого экземпляра, если оно было единственным обновляемым свойством.</span><span class="sxs-lookup"><span data-stu-id="12fb8-518">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="12fb8-519">Поддержка пользовательских параметров сортировки в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="12fb8-519">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="12fb8-520">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="12fb8-520">Az.Storage</span></span>
* <span data-ttu-id="12fb8-521">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="12fb8-521">Update incorrect online help URLs</span></span>
* <span data-ttu-id="12fb8-522">Добавлен вывод подробных сообщений об ошибке при получении или установке классических свойств ведения журнала или метрик в учетной записи хранилища класса Premium, так как учетная запись хранилища класса Premium не поддерживает классические функции ведения журнала и метрик.</span><span class="sxs-lookup"><span data-stu-id="12fb8-522">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="12fb8-523">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="12fb8-523">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="12fb8-524">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="12fb8-524">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="12fb8-525">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="12fb8-525">Az.TrafficManager</span></span>
* <span data-ttu-id="12fb8-526">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="12fb8-526">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="12fb8-527">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="12fb8-527">Az.Websites</span></span>
* <span data-ttu-id="12fb8-528">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="12fb8-528">Update incorrect online help URLs</span></span>
* <span data-ttu-id="12fb8-529">Исправлена работа командлета New-AzWebAppSSLBinding: сертификат отправляется в правильную группу ресурсов и правильное расположение, если приложение размещено в ASE.</span><span class="sxs-lookup"><span data-stu-id="12fb8-529">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="12fb8-530">Исправлена работа командлета New-AzWebAppSSLBinding: теги не перезаписываются при привязке SSL-сертификата к приложению.</span><span class="sxs-lookup"><span data-stu-id="12fb8-530">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="12fb8-531">1.1.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="12fb8-531">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="12fb8-532">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="12fb8-532">Az.Accounts</span></span>
* <span data-ttu-id="12fb8-533">Добавление области "Local" в Enable-AzureRmAlias.</span><span class="sxs-lookup"><span data-stu-id="12fb8-533">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="12fb8-534">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="12fb8-534">Az.Compute</span></span>
* <span data-ttu-id="12fb8-535">Теперь имя не является обязательным в идентификаторе набора параметров для Restart/Start/Stop/Remove/Set-AzVM и Save-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="12fb8-535">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="12fb8-536">Обновлено описание идентификатора в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="12fb8-536">Updated the description of ID in help files</span></span>
* <span data-ttu-id="12fb8-537">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="12fb8-537">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="12fb8-538">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="12fb8-538">Az.DataLakeStore</span></span>
* <span data-ttu-id="12fb8-539">Обновление версии пакета SDK для плоскости данных до 1.1.14 для устранения найденных проблем.</span><span class="sxs-lookup"><span data-stu-id="12fb8-539">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="12fb8-540">Исправлена обработка отрицательного времени доступа и времени изменения для getfilestatus и liststatus, исправлен токен отмены для асинхронных методов.</span><span class="sxs-lookup"><span data-stu-id="12fb8-540">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="12fb8-541">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="12fb8-541">Az.EventGrid</span></span>
* <span data-ttu-id="12fb8-542">Обновление для использования API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="12fb8-542">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="12fb8-543">Обновлены указанные ниже командлеты для поддержки нового сценария в API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="12fb8-543">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="12fb8-544">New-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="12fb8-544">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="12fb8-545">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="12fb8-545">Event Time-To-Live,</span></span>
        - <span data-ttu-id="12fb8-546">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="12fb8-546">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="12fb8-547">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="12fb8-547">Dead letter endpoint.</span></span>
    - <span data-ttu-id="12fb8-548">Update-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="12fb8-548">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="12fb8-549">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="12fb8-549">Event Time-To-Live,</span></span>
        - <span data-ttu-id="12fb8-550">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="12fb8-550">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="12fb8-551">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="12fb8-551">Dead letter endpoint.</span></span>
* <span data-ttu-id="12fb8-552">Для параметра EndpointType добавлены новые значения перечисления (storageQueue и hybridConnection) в командлеты New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="12fb8-552">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="12fb8-553">Если ожидается, что создание или обновление подписки на событие повлечет за собой действия со стороны пользователя, выполняемые вручную, отображается предупреждение при создании или обновлении подписки события.</span><span class="sxs-lookup"><span data-stu-id="12fb8-553">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="12fb8-554">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="12fb8-554">Az.IotHub</span></span>
* <span data-ttu-id="12fb8-555">Пакет SDK Центра Интернета вещей обновлен до последней версии.</span><span class="sxs-lookup"><span data-stu-id="12fb8-555">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="12fb8-556">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="12fb8-556">Az.LogicApp</span></span>
* <span data-ttu-id="12fb8-557">Get-AzLogicApp позволяет перечислить все параметры без указанного имени.</span><span class="sxs-lookup"><span data-stu-id="12fb8-557">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="12fb8-558">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="12fb8-558">Az.Resources</span></span>
* <span data-ttu-id="12fb8-559">Исправлена проблема с набором параметров при предоставлении параметров "-ODataQuery" и "-ResourceId" для "Get-AzResource".</span><span class="sxs-lookup"><span data-stu-id="12fb8-559">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="12fb8-560">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7875.</span><span class="sxs-lookup"><span data-stu-id="12fb8-560">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="12fb8-561">Исправлена обработка параметра -Custom в New/Set-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="12fb8-561">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="12fb8-562">Исправлена опечатка в документации по New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="12fb8-562">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="12fb8-563">Параметр "-MailNickname" стал обязательным для "New-AzADUser".</span><span class="sxs-lookup"><span data-stu-id="12fb8-563">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="12fb8-564">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8220.</span><span class="sxs-lookup"><span data-stu-id="12fb8-564">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="12fb8-565">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="12fb8-565">Az.SignalR</span></span>
* <span data-ttu-id="12fb8-566">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="12fb8-566">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="12fb8-567">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="12fb8-567">Az.Sql</span></span>
* <span data-ttu-id="12fb8-568">Зависимость клиента управления хранением преобразована для общей реализации в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="12fb8-568">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="12fb8-569">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="12fb8-569">Az.Storage</span></span>
* <span data-ttu-id="12fb8-570">Установка параметра StorageAccountName для контекста хранилища в качестве реального имени учетной записи хранения, если она была создана с использованием токена Sas, OAuth или анонимного доступа.</span><span class="sxs-lookup"><span data-stu-id="12fb8-570">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="12fb8-571">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="12fb8-571">New-AzStorageContext</span></span>
* <span data-ttu-id="12fb8-572">Создание токена Sas большого двоичного объекта моментального снимка с параметром "-FullUri". Возвращаемый URI исправлен на URI моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="12fb8-572">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="12fb8-573">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="12fb8-573">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="12fb8-574">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="12fb8-574">Az.Websites</span></span>
* <span data-ttu-id="12fb8-575">Исправлена ошибка синтаксического анализа даты в "Get-AzDeletedWebApp".</span><span class="sxs-lookup"><span data-stu-id="12fb8-575">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="12fb8-576">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="12fb8-576">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="12fb8-577">1.0.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="12fb8-577">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="12fb8-578">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="12fb8-578">General</span></span>

- <span data-ttu-id="12fb8-579">Общедоступная версия модуля Az.</span><span class="sxs-lookup"><span data-stu-id="12fb8-579">General Availability of Az Module</span></span>
- <span data-ttu-id="12fb8-580">Справка в Интернете для каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="12fb8-580">Online help for each module</span></span>
- <span data-ttu-id="12fb8-581">Дополнительные сведения и стратегию развития см. в статье [Announcing New Module 'Az'](https://aka.ms/azps-announce) (Объявление о новом модуле Az)</span><span class="sxs-lookup"><span data-stu-id="12fb8-581">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="12fb8-582">Сведения о миграции с AzureRM см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="12fb8-582">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="12fb8-583">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="12fb8-583">Az.Accounts</span></span>
- <span data-ttu-id="12fb8-584">Изменено с Az.Profile.</span><span class="sxs-lookup"><span data-stu-id="12fb8-584">Changed from Az.Profile</span></span>
- <span data-ttu-id="12fb8-585">Исправлены форматы таблиц для типов профиля и контекста.</span><span class="sxs-lookup"><span data-stu-id="12fb8-585">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="12fb8-586">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="12fb8-586">Az.ApiManagement</span></span>
- <span data-ttu-id="12fb8-587">Исправления для #7002.</span><span class="sxs-lookup"><span data-stu-id="12fb8-587">Fixes for #7002</span></span>
- <span data-ttu-id="12fb8-588">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="12fb8-588">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="12fb8-589">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="12fb8-589">Az.Batch</span></span>
- <span data-ttu-id="12fb8-590">Добавлена возможность видеть, какая версия агента узла пакетной службы Azure работает в пуле на каждой виртуальной машине, с помощью нового свойства `NodeAgentInformation` в `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="12fb8-590">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="12fb8-591">Значение `Caching` по умолчанию для `PSDataDisk` теперь `ReadWrite` вместо `None`.</span><span class="sxs-lookup"><span data-stu-id="12fb8-591">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="12fb8-592">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="12fb8-592">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="12fb8-593">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="12fb8-593">Az.Billing</span></span>
- <span data-ttu-id="12fb8-594">Объединены командлеты Billing, Consumption и UsageAggregates. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0).</span><span class="sxs-lookup"><span data-stu-id="12fb8-594">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="12fb8-595">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="12fb8-595">Az.CognitivServices</span></span>
- <span data-ttu-id="12fb8-596">Добавлены средства заполнения для SkuName и Typem, доступные в операции New-AzureRmCognitiveServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="12fb8-596">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="12fb8-597">Удален набор параметров GetSkusWithAccountParamSetName из Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="12fb8-597">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="12fb8-598">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="12fb8-598">Az.ContainerInstance</span></span>
- <span data-ttu-id="12fb8-599">Добавлена поддержка ManagedIdentity.</span><span class="sxs-lookup"><span data-stu-id="12fb8-599">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="12fb8-600">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="12fb8-600">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="12fb8-601">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="12fb8-601">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="12fb8-602">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="12fb8-602">Az.DataLakeStore</span></span>
- <span data-ttu-id="12fb8-603">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="12fb8-603">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="12fb8-604">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="12fb8-604">Az.Monitor</span></span>
- <span data-ttu-id="12fb8-605">"Az.Insights" переименован в "Az.Monitor" и внесены другие незначительные критические изменения. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="12fb8-605">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="12fb8-606">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="12fb8-606">Az.KeyVault</span></span>
- <span data-ttu-id="12fb8-607">Из типов вывода удалено устаревшее свойство PurgeDisabled</span><span class="sxs-lookup"><span data-stu-id="12fb8-607">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="12fb8-608">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="12fb8-608">Az.MachineLearning</span></span>
- <span data-ttu-id="12fb8-609">Включены командлеты из модуля Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="12fb8-609">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="12fb8-610">Az.Media</span><span class="sxs-lookup"><span data-stu-id="12fb8-610">Az.Media</span></span>
- <span data-ttu-id="12fb8-611">Удаляет устаревший псевдоним Tags из New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="12fb8-611">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="12fb8-612">Az.Network</span><span class="sxs-lookup"><span data-stu-id="12fb8-612">Az.Network</span></span>
<span data-ttu-id="12fb8-613">В шлюз приложений добавлена поддержка настройки RewriteRuleSets</span><span class="sxs-lookup"><span data-stu-id="12fb8-613">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="12fb8-614">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="12fb8-614">New cmdlets added:</span></span>
        - <span data-ttu-id="12fb8-615">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="12fb8-615">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="12fb8-616">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="12fb8-616">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="12fb8-617">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="12fb8-617">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="12fb8-618">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="12fb8-618">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="12fb8-619">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="12fb8-619">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="12fb8-620">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="12fb8-620">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="12fb8-621">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="12fb8-621">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="12fb8-622">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="12fb8-622">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="12fb8-623">В следующие командлеты добавлен необязательный параметр -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="12fb8-623">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="12fb8-624">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="12fb8-624">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="12fb8-625">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="12fb8-625">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="12fb8-626">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="12fb8-626">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="12fb8-627">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="12fb8-627">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="12fb8-628">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="12fb8-628">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="12fb8-629">New-AzureRmApplicationGatewayUrlPathMapConfig добавил с помощью идентификатора поддержку KeyVault для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="12fb8-629">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="12fb8-630">В следующие командлеты добавлен необязательный параметр -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="12fb8-630">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="12fb8-631">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="12fb8-631">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="12fb8-632">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="12fb8-632">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="12fb8-633">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="12fb8-633">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="12fb8-634">В командлет New-AzApplicationGateway добавлен необязательный параметр -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="12fb8-634">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="12fb8-635">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="12fb8-635">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="12fb8-636">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="12fb8-636">Az.OperationalInsights</span></span>
- <span data-ttu-id="12fb8-637">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="12fb8-637">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="12fb8-638">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="12fb8-638">Az.Profile</span></span>
- <span data-ttu-id="12fb8-639">Имя модуля изменено на Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="12fb8-639">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="12fb8-640">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="12fb8-640">Az.RecoveryServices</span></span>
- <span data-ttu-id="12fb8-641">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="12fb8-641">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="12fb8-642">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="12fb8-642">Az.Resources</span></span>
- <span data-ttu-id="12fb8-643">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="12fb8-643">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="12fb8-644">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="12fb8-644">Az.ServiceFabric</span></span>
- <span data-ttu-id="12fb8-645">Поддержка спецификации сертификата по общему имени и отпечатку</span><span class="sxs-lookup"><span data-stu-id="12fb8-645">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="12fb8-646">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="12fb8-646">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="12fb8-647">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="12fb8-647">Az.SIgnalR</span></span>
- <span data-ttu-id="12fb8-648">Общедоступная версия командлетов PowerShell для SIgnalR</span><span class="sxs-lookup"><span data-stu-id="12fb8-648">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="12fb8-649">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="12fb8-649">Az.Sql</span></span>
- <span data-ttu-id="12fb8-650">Добавлены новые типы обнаружения Data_Exfiltration и Unsafe_Action в командлеты обнаружения угроз</span><span class="sxs-lookup"><span data-stu-id="12fb8-650">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="12fb8-651">Примеры обновленной документации для командлетов аудита Sql</span><span class="sxs-lookup"><span data-stu-id="12fb8-651">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="12fb8-652">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="12fb8-652">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="12fb8-653">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="12fb8-653">Az.Storage</span></span>
- <span data-ttu-id="12fb8-654">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="12fb8-654">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="12fb8-655">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="12fb8-655">Az.Websites</span></span>
- <span data-ttu-id="12fb8-656">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="12fb8-656">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="12fb8-657">0.7.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="12fb8-657">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="12fb8-658">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="12fb8-658">General</span></span>

* <span data-ttu-id="12fb8-659">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="12fb8-659">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="12fb8-660">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="12fb8-660">Az.Compute</span></span>

* <span data-ttu-id="12fb8-661">Добавлена поддержка UltraSSD и образов коллекции в простых наборах параметров для командлетов `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="12fb8-661">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="12fb8-662">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="12fb8-662">Az.DataLakeStore</span></span>

* <span data-ttu-id="12fb8-663">Исправлено косую черту в конце домена учетной записи ADLS</span><span class="sxs-lookup"><span data-stu-id="12fb8-663">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="12fb8-664">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="12fb8-664">Az.FrontDoor</span></span>

* <span data-ttu-id="12fb8-665">Исправлены некоторые неработающие ссылки</span><span class="sxs-lookup"><span data-stu-id="12fb8-665">Fixed some broken links</span></span>
    - <span data-ttu-id="12fb8-666">В статьях New-AzureRmFrontDoor и Set-AzureRmFrontDoor исправлена ссылка на статью командлета New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="12fb8-666">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="12fb8-667">В статье New-AzureRmFrontDoorManagedRuleObject исправлена ссылка на статью командлета New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="12fb8-667">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="12fb8-668">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="12fb8-668">Az.RecoveryServices</span></span>

* <span data-ttu-id="12fb8-669">Добавлены проверки на стороне клиента для операций восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="12fb8-669">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="12fb8-670">StorageAccountName и storageAccountResourceGroupName являются необязательными для восстановления afs.</span><span class="sxs-lookup"><span data-stu-id="12fb8-670">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="12fb8-671">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="12fb8-671">Az.Resources</span></span>

* <span data-ttu-id="12fb8-672">Исправление для https://github.com/Azure/azure-powershell/issues/7679.</span><span class="sxs-lookup"><span data-stu-id="12fb8-672">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="12fb8-673">Обновите Get-AzureRmRoleAssignment, чтобы использовать область подписки, если она указана при запросе классических администраторов.</span><span class="sxs-lookup"><span data-stu-id="12fb8-673">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="12fb8-674">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="12fb8-674">Az.Sql</span></span>

* <span data-ttu-id="12fb8-675">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="12fb8-675">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="12fb8-676">Устранена проблема с использованием Get-AzureRmSqlDatabaseVulnerabilityAssessment с .NET Core.</span><span class="sxs-lookup"><span data-stu-id="12fb8-676">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="12fb8-677">Изменена документация справочных сообщений, связанных с командлетами аудита SQL.</span><span class="sxs-lookup"><span data-stu-id="12fb8-677">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="12fb8-678">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="12fb8-678">Az.Storage</span></span>

* <span data-ttu-id="12fb8-679">Добавлено -EnableHierarchicalNamespace к New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="12fb8-679">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="12fb8-680">Устранена проблема, из-за которой командлет Copy File не может повторно использовать исходный контекст в пункте назначения, если не введен -DestContext</span><span class="sxs-lookup"><span data-stu-id="12fb8-680">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="12fb8-681">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="12fb8-681">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="12fb8-682">Поддержка статической конфигурации сайта</span><span class="sxs-lookup"><span data-stu-id="12fb8-682">Support Static Website configuration</span></span>
    - <span data-ttu-id="12fb8-683">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="12fb8-683">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="12fb8-684">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="12fb8-684">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="12fb8-685">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="12fb8-685">Az.Websites</span></span>

* <span data-ttu-id="12fb8-686">Set-AzureRmWebApp и Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="12fb8-686">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="12fb8-687">Добавлен новый параметр (-AzureStoragePath), который указывает путь службы хранилища Azure для подключения в приложениях-контейнерах Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="12fb8-687">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="12fb8-688">Используйте выходные данные нового командлета New-AzureRmWebAppAzureStoragePath в качестве параметра, чтобы задать пути к службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="12fb8-688">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="12fb8-689">0.6.1 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="12fb8-689">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="12fb8-690">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="12fb8-690">Az.ApiManagement</span></span>
* <span data-ttu-id="12fb8-691">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="12fb8-691">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="12fb8-692">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="12fb8-692">Az.Automation</span></span>
* <span data-ttu-id="12fb8-693">Командлеты службы автоматизации Azure на базе Swagger.</span><span class="sxs-lookup"><span data-stu-id="12fb8-693">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="12fb8-694">Добавлены командлеты для Управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="12fb8-694">Added Update Management cmdlets</span></span>
* <span data-ttu-id="12fb8-695">Добавлены командлеты для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="12fb8-695">Added Source Control cmdlets</span></span>
* <span data-ttu-id="12fb8-696">Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="12fb8-696">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="12fb8-697">Исправлена команда DSC для регистрации узла.</span><span class="sxs-lookup"><span data-stu-id="12fb8-697">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="12fb8-698">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="12fb8-698">Az.Compute</span></span>
* <span data-ttu-id="12fb8-699">Исправлена проблема с удостоверением, назначаемым системой.</span><span class="sxs-lookup"><span data-stu-id="12fb8-699">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="12fb8-700">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="12fb8-700">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="12fb8-701">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="12fb8-701">Az.ContainerInstance</span></span>
* <span data-ttu-id="12fb8-702">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="12fb8-702">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="12fb8-703">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="12fb8-703">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="12fb8-704">Обновлено описание в примерах командлетов для Marketplace.</span><span class="sxs-lookup"><span data-stu-id="12fb8-704">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="12fb8-705">Az.Network</span><span class="sxs-lookup"><span data-stu-id="12fb8-705">Az.Network</span></span>
* <span data-ttu-id="12fb8-706">Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="12fb8-706">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="12fb8-707">Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="12fb8-707">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="12fb8-708">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="12fb8-708">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="12fb8-709">Исправлены проблемы с использованием памяти в карте виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="12fb8-709">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="12fb8-710">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="12fb8-710">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="12fb8-711">Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="12fb8-711">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="12fb8-712">Параметры часового пояса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="12fb8-712">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="12fb8-713">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="12fb8-713">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="12fb8-714">Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="12fb8-714">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="12fb8-715">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="12fb8-715">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="12fb8-716">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="12fb8-716">Az.Relay</span></span>
* <span data-ttu-id="12fb8-717">Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.</span><span class="sxs-lookup"><span data-stu-id="12fb8-717">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="12fb8-718">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="12fb8-718">Az.Resources</span></span>
* <span data-ttu-id="12fb8-719">Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.</span><span class="sxs-lookup"><span data-stu-id="12fb8-719">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="12fb8-720">Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.</span><span class="sxs-lookup"><span data-stu-id="12fb8-720">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="12fb8-721">Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.</span><span class="sxs-lookup"><span data-stu-id="12fb8-721">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="12fb8-722">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="12fb8-722">Az.ServiceFabric</span></span>
* <span data-ttu-id="12fb8-723">Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.</span><span class="sxs-lookup"><span data-stu-id="12fb8-723">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="12fb8-724">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="12fb8-724">Az.Sql</span></span>
* <span data-ttu-id="12fb8-725">Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="12fb8-725">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="12fb8-726">Get-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="12fb8-726">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="12fb8-727">New-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="12fb8-727">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="12fb8-728">Set-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="12fb8-728">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="12fb8-729">Remove-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="12fb8-729">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="12fb8-730">Get-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="12fb8-730">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="12fb8-731">New-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="12fb8-731">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="12fb8-732">Restore-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="12fb8-732">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="12fb8-733">Remove-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="12fb8-733">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="12fb8-734">Добавлено расширенное управление политиками аудита для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="12fb8-734">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="12fb8-735">Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="12fb8-735">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="12fb8-736">Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.</span><span class="sxs-lookup"><span data-stu-id="12fb8-736">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="12fb8-737">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="12fb8-737">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="12fb8-738">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="12fb8-738">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="12fb8-739">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="12fb8-739">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="12fb8-740">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="12fb8-740">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="12fb8-741">Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="12fb8-741">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="12fb8-742">0.5.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="12fb8-742">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="12fb8-743">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="12fb8-743">General</span></span>
* <span data-ttu-id="12fb8-744">Добавлены средства заполнения ресурсов для многих основных командлетов — они позволяют вам переключать существующие имена ресурсов при вызове командлетов в интерактивном режиме</span><span class="sxs-lookup"><span data-stu-id="12fb8-744">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="12fb8-745">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="12fb8-745">Az.Profile</span></span>
* <span data-ttu-id="12fb8-746">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="12fb8-746">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="12fb8-747">В командлете Connect-AzAccount параметр TenantId переименован в Tenant и добавлен псевдоним для TenantId</span><span class="sxs-lookup"><span data-stu-id="12fb8-747">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="12fb8-748">Обновлено описание TenantId для командлета Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="12fb8-748">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="12fb8-749">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="12fb8-749">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="12fb8-750">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="12fb8-750">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="12fb8-751">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="12fb8-751">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="12fb8-752">Устранена проблема, при которой командлет Disconnect-AzAccount вызывал сбой при отсутствии подключения</span><span class="sxs-lookup"><span data-stu-id="12fb8-752">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="12fb8-753">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="12fb8-753">Az.CognitiveServices</span></span>
* <span data-ttu-id="12fb8-754">Добавлена операция Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="12fb8-754">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="12fb8-755">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="12fb8-755">Az.Compute</span></span>
* <span data-ttu-id="12fb8-756">Добавлены командлеты Add-AzVmssVMDataDisk и Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="12fb8-756">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="12fb8-757">Get-AzVMImage отображает AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="12fb8-757">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="12fb8-758">Устранена проблема, при которой значения параметров SetAzVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="12fb8-758">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="12fb8-759">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="12fb8-759">Az.DataLakeStore</span></span>
* <span data-ttu-id="12fb8-760">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="12fb8-760">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="12fb8-761">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="12fb8-761">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="12fb8-762">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="12fb8-762">Az.Insights</span></span>
* <span data-ttu-id="12fb8-763">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="12fb8-763">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="12fb8-764">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="12fb8-764">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="12fb8-765">Исправлена проблема № 7513 [Insights], при которой для командлета Set-AzDiagnosticSetting требовалось явное указание категорий во время создания параметра</span><span class="sxs-lookup"><span data-stu-id="12fb8-765">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="12fb8-766">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="12fb8-766">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="12fb8-767">Az.Network</span><span class="sxs-lookup"><span data-stu-id="12fb8-767">Az.Network</span></span>
* <span data-ttu-id="12fb8-768">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="12fb8-768">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="12fb8-769">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="12fb8-769">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="12fb8-770">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="12fb8-770">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="12fb8-771">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="12fb8-771">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="12fb8-772">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="12fb8-772">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="12fb8-773">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="12fb8-773">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="12fb8-774">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="12fb8-774">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="12fb8-775">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="12fb8-775">Az.PolicyInsights</span></span>
* <span data-ttu-id="12fb8-776">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="12fb8-776">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="12fb8-777">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="12fb8-777">Az.Resources</span></span>
* <span data-ttu-id="12fb8-778">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="12fb8-778">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="12fb8-779">Разрешено перечисление ресурсов с помощью параметра -ResourceId для командлета Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="12fb8-779">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="12fb8-780">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="12fb8-780">Az.ServiceBus</span></span>
* <span data-ttu-id="12fb8-781">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="12fb8-781">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="12fb8-782">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="12fb8-782">Az.ServiceFabric</span></span>
* <span data-ttu-id="12fb8-783">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="12fb8-783">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="12fb8-784">Исправлен командлет Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="12fb8-784">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="12fb8-785">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="12fb8-785">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="12fb8-786">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="12fb8-786">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="12fb8-787">Исправлен командлет Update-AzServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="12fb8-787">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="12fb8-788">0.4.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="12fb8-788">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="12fb8-789">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="12fb8-789">Az.Profile</span></span>
* <span data-ttu-id="12fb8-790">Устранена проблема с Get-AzSubscription в CloudShell</span><span class="sxs-lookup"><span data-stu-id="12fb8-790">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="12fb8-791">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="12fb8-791">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="12fb8-792">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="12fb8-792">Az.Compute</span></span>
* <span data-ttu-id="12fb8-793">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzVm</span><span class="sxs-lookup"><span data-stu-id="12fb8-793">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="12fb8-794">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="12fb8-794">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="12fb8-795">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="12fb8-795">Az.DataLakeStore</span></span>
* <span data-ttu-id="12fb8-796">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="12fb8-796">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="12fb8-797">Get-AzDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="12fb8-797">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="12fb8-798">Add-AzDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="12fb8-798">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="12fb8-799">Set-AzDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="12fb8-799">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="12fb8-800">Remove-AzDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="12fb8-800">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="12fb8-801">Az.Network</span><span class="sxs-lookup"><span data-stu-id="12fb8-801">Az.Network</span></span>
* <span data-ttu-id="12fb8-802">Обновлен командлет Test-AzNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="12fb8-802">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="12fb8-803">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="12fb8-803">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="12fb8-804">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="12fb8-804">Az.Resources</span></span>
* <span data-ttu-id="12fb8-805">Устранена проблема, из-за которой командлет Get-AzRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), благодаря добавлению понятного исключения в сценарий.</span><span class="sxs-lookup"><span data-stu-id="12fb8-805">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="12fb8-806">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="12fb8-806">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="12fb8-807">0.3.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="12fb8-807">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="12fb8-808">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="12fb8-808">Azure.Storage</span></span>
* <span data-ttu-id="12fb8-809">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="12fb8-809">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="12fb8-810">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="12fb8-810">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="12fb8-811">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="12fb8-811">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="12fb8-812">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="12fb8-812">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="12fb8-813">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="12fb8-813">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="12fb8-814">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="12fb8-814">Az.CognitiveServices</span></span>
* <span data-ttu-id="12fb8-815">Поддержка Get-AzCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="12fb8-815">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="12fb8-816">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="12fb8-816">Az.Compute</span></span>
* <span data-ttu-id="12fb8-817">Исправлена команда Get-AzVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов</span><span class="sxs-lookup"><span data-stu-id="12fb8-817">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="12fb8-818">Добавлен пример использования SimpleParameterSet в справку командлета New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="12fb8-818">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="12fb8-819">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="12fb8-819">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="12fb8-820">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="12fb8-820">Az.DataFactoryV2</span></span>
* <span data-ttu-id="12fb8-821">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="12fb8-821">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="12fb8-822">Az.Network</span><span class="sxs-lookup"><span data-stu-id="12fb8-822">Az.Network</span></span>
* <span data-ttu-id="12fb8-823">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="12fb8-823">Added NetworkProfile functionality.</span></span> <span data-ttu-id="12fb8-824">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="12fb8-824">new cmdlets added</span></span>
    - <span data-ttu-id="12fb8-825">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="12fb8-825">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="12fb8-826">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="12fb8-826">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="12fb8-827">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="12fb8-827">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="12fb8-828">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="12fb8-828">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="12fb8-829">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="12fb8-829">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="12fb8-830">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="12fb8-830">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="12fb8-831">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="12fb8-831">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="12fb8-832">Добавлены командлеты: New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="12fb8-832">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="12fb8-833">Добавлены командлеты: Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="12fb8-833">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="12fb8-834">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="12fb8-834">Az.RedisCache</span></span>
* <span data-ttu-id="12fb8-835">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="12fb8-835">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="12fb8-836">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="12fb8-836">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="12fb8-837">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="12fb8-837">Az.Resources</span></span>
* <span data-ttu-id="12fb8-838">Добавлен отсутствующий параметр -Mode в командлет Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="12fb8-838">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="12fb8-839">Исправлена ошибка командлета Get-AzProviderOperation для операций, когда Origin содержит User</span><span class="sxs-lookup"><span data-stu-id="12fb8-839">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="12fb8-840">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="12fb8-840">Az.Sql</span></span>
* <span data-ttu-id="12fb8-841">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="12fb8-841">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="12fb8-842">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="12fb8-842">Az.Websites</span></span>
* <span data-ttu-id="12fb8-843">Новый командлет Get-AzWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="12fb8-843">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="12fb8-844">Новые командлеты New-AzWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows</span><span class="sxs-lookup"><span data-stu-id="12fb8-844">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="12fb8-845">0.2.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="12fb8-845">0.2.0 - September 2018</span></span>
 <span data-ttu-id="12fb8-846">Первый выпуск</span><span class="sxs-lookup"><span data-stu-id="12fb8-846">Initial Release</span></span>