## <a name="100---december-2018"></a><span data-ttu-id="439e5-101">1.0.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="439e5-101">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="439e5-102">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="439e5-102">General</span></span>

- <span data-ttu-id="439e5-103">Общедоступная версия модуля Az.</span><span class="sxs-lookup"><span data-stu-id="439e5-103">General Availability of Az Module</span></span>
- <span data-ttu-id="439e5-104">Справка в Интернете для каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="439e5-104">Online help for each module</span></span>
- <span data-ttu-id="439e5-105">Дополнительные сведения и стратегию развития см. в статье [Announcing New Module 'Az'](https://aka.ms/azps-announce) (Объявление о новом модуле Az)</span><span class="sxs-lookup"><span data-stu-id="439e5-105">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="439e5-106">Сведения о миграции с AzureRM см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="439e5-106">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="439e5-107">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="439e5-107">Az.Accounts</span></span>
- <span data-ttu-id="439e5-108">Изменено с Az.Profile.</span><span class="sxs-lookup"><span data-stu-id="439e5-108">Changed from Az.Profile</span></span>
- <span data-ttu-id="439e5-109">Исправлены форматы таблиц для типов профиля и контекста.</span><span class="sxs-lookup"><span data-stu-id="439e5-109">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="439e5-110">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="439e5-110">Az.ApiManagement</span></span>
- <span data-ttu-id="439e5-111">Исправления для #7002.</span><span class="sxs-lookup"><span data-stu-id="439e5-111">Fixes for #7002</span></span>
- <span data-ttu-id="439e5-112">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="439e5-112">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="439e5-113">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="439e5-113">Az.Batch</span></span>
- <span data-ttu-id="439e5-114">Добавлена возможность видеть, какая версия агента узла пакетной службы Azure работает в пуле на каждой виртуальной машине, с помощью нового свойства `NodeAgentInformation` в `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="439e5-114">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="439e5-115">Значение `Caching` по умолчанию для `PSDataDisk` теперь `ReadWrite` вместо `None`.</span><span class="sxs-lookup"><span data-stu-id="439e5-115">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="439e5-116">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="439e5-116">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="439e5-117">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="439e5-117">Az.Billing</span></span>
- <span data-ttu-id="439e5-118">Объединены командлеты Billing, Consumption и UsageAggregates. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0).</span><span class="sxs-lookup"><span data-stu-id="439e5-118">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="439e5-119">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="439e5-119">Az.CognitivServices</span></span>
- <span data-ttu-id="439e5-120">Добавлены средства заполнения для SkuName и Typem, доступные в операции New-AzureRmCognitiveServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="439e5-120">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="439e5-121">Удален набор параметров GetSkusWithAccountParamSetName из Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="439e5-121">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="439e5-122">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="439e5-122">Az.ContainerInstance</span></span>
- <span data-ttu-id="439e5-123">Добавлена поддержка ManagedIdentity.</span><span class="sxs-lookup"><span data-stu-id="439e5-123">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="439e5-124">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="439e5-124">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="439e5-125">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="439e5-125">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="439e5-126">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="439e5-126">Az.DataLakeStore</span></span>
- <span data-ttu-id="439e5-127">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="439e5-127">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="439e5-128">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="439e5-128">Az.Monitor</span></span>
- <span data-ttu-id="439e5-129">"Az.Insights" переименован в "Az.Monitor" и внесены другие незначительные критические изменения. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="439e5-129">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="439e5-130">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="439e5-130">Az.KeyVault</span></span>
- <span data-ttu-id="439e5-131">Из типов вывода удалено устаревшее свойство PurgeDisabled</span><span class="sxs-lookup"><span data-stu-id="439e5-131">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="439e5-132">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="439e5-132">Az.MachineLearning</span></span>
- <span data-ttu-id="439e5-133">Включены командлеты из модуля Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="439e5-133">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="439e5-134">Az.Media</span><span class="sxs-lookup"><span data-stu-id="439e5-134">Az.Media</span></span>
- <span data-ttu-id="439e5-135">Удаляет устаревший псевдоним Tags из New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="439e5-135">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="439e5-136">Az.Network</span><span class="sxs-lookup"><span data-stu-id="439e5-136">Az.Network</span></span>
<span data-ttu-id="439e5-137">В шлюз приложений добавлена поддержка настройки RewriteRuleSets</span><span class="sxs-lookup"><span data-stu-id="439e5-137">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="439e5-138">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="439e5-138">New cmdlets added:</span></span>
        - <span data-ttu-id="439e5-139">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="439e5-139">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="439e5-140">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="439e5-140">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="439e5-141">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="439e5-141">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="439e5-142">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="439e5-142">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="439e5-143">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="439e5-143">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="439e5-144">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="439e5-144">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="439e5-145">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="439e5-145">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="439e5-146">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="439e5-146">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="439e5-147">В следующие командлеты добавлен необязательный параметр -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="439e5-147">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="439e5-148">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="439e5-148">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="439e5-149">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="439e5-149">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="439e5-150">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="439e5-150">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="439e5-151">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="439e5-151">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="439e5-152">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="439e5-152">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="439e5-153">New-AzureRmApplicationGatewayUrlPathMapConfig добавил с помощью идентификатора поддержку KeyVault для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="439e5-153">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="439e5-154">В следующие командлеты добавлен необязательный параметр -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="439e5-154">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="439e5-155">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="439e5-155">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="439e5-156">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="439e5-156">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="439e5-157">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="439e5-157">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="439e5-158">В командлет New-AzApplicationGateway добавлен необязательный параметр -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="439e5-158">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="439e5-159">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="439e5-159">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="439e5-160">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="439e5-160">Az.OperationalInsights</span></span>
- <span data-ttu-id="439e5-161">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="439e5-161">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="439e5-162">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="439e5-162">Az.Profile</span></span>
- <span data-ttu-id="439e5-163">Имя модуля изменено на Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="439e5-163">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="439e5-164">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="439e5-164">Az.RecoveryServices</span></span>
- <span data-ttu-id="439e5-165">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="439e5-165">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="439e5-166">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="439e5-166">Az.Resources</span></span>
- <span data-ttu-id="439e5-167">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="439e5-167">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="439e5-168">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="439e5-168">Az.ServiceFabric</span></span>
- <span data-ttu-id="439e5-169">Поддержка спецификации сертификата по общему имени и отпечатку</span><span class="sxs-lookup"><span data-stu-id="439e5-169">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="439e5-170">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="439e5-170">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="439e5-171">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="439e5-171">Az.SIgnalR</span></span>
- <span data-ttu-id="439e5-172">Общедоступная версия командлетов PowerShell для SIgnalR</span><span class="sxs-lookup"><span data-stu-id="439e5-172">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="439e5-173">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="439e5-173">Az.Sql</span></span>
- <span data-ttu-id="439e5-174">Добавлены новые типы обнаружения Data_Exfiltration и Unsafe_Action в командлеты обнаружения угроз</span><span class="sxs-lookup"><span data-stu-id="439e5-174">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="439e5-175">Примеры обновленной документации для командлетов аудита Sql</span><span class="sxs-lookup"><span data-stu-id="439e5-175">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="439e5-176">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="439e5-176">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="439e5-177">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="439e5-177">Az.Storage</span></span>
- <span data-ttu-id="439e5-178">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="439e5-178">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="439e5-179">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="439e5-179">Az.Websites</span></span>
- <span data-ttu-id="439e5-180">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="439e5-180">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="439e5-181">0.7.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="439e5-181">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="439e5-182">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="439e5-182">General</span></span>

* <span data-ttu-id="439e5-183">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="439e5-183">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="439e5-184">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="439e5-184">Az.Compute</span></span>

* <span data-ttu-id="439e5-185">Добавлена поддержка UltraSSD и образов коллекции в простых наборах параметров для командлетов `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="439e5-185">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="439e5-186">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="439e5-186">Az.DataLakeStore</span></span>

* <span data-ttu-id="439e5-187">Исправлено косую черту в конце домена учетной записи ADLS</span><span class="sxs-lookup"><span data-stu-id="439e5-187">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="439e5-188">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="439e5-188">Az.FrontDoor</span></span>

* <span data-ttu-id="439e5-189">Исправлены некоторые неработающие ссылки</span><span class="sxs-lookup"><span data-stu-id="439e5-189">Fixed some broken links</span></span>
    - <span data-ttu-id="439e5-190">В статьях New-AzureRmFrontDoor и Set-AzureRmFrontDoor исправлена ссылка на статью командлета New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="439e5-190">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="439e5-191">В статье New-AzureRmFrontDoorManagedRuleObject исправлена ссылка на статью командлета New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="439e5-191">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="439e5-192">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="439e5-192">Az.RecoveryServices</span></span>

* <span data-ttu-id="439e5-193">Добавлены проверки на стороне клиента для операций восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="439e5-193">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="439e5-194">StorageAccountName и storageAccountResourceGroupName являются необязательными для восстановления afs.</span><span class="sxs-lookup"><span data-stu-id="439e5-194">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="439e5-195">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="439e5-195">Az.Resources</span></span>

* <span data-ttu-id="439e5-196">Исправление для https://github.com/Azure/azure-powershell/issues/7679.</span><span class="sxs-lookup"><span data-stu-id="439e5-196">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="439e5-197">Обновите Get-AzureRmRoleAssignment, чтобы использовать область подписки, если она указана при запросе классических администраторов.</span><span class="sxs-lookup"><span data-stu-id="439e5-197">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="439e5-198">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="439e5-198">Az.Sql</span></span>

* <span data-ttu-id="439e5-199">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="439e5-199">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="439e5-200">Устранена проблема с использованием Get-AzureRmSqlDatabaseVulnerabilityAssessment с .NET Core.</span><span class="sxs-lookup"><span data-stu-id="439e5-200">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="439e5-201">Изменена документация справочных сообщений, связанных с командлетами аудита SQL.</span><span class="sxs-lookup"><span data-stu-id="439e5-201">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="439e5-202">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="439e5-202">Az.Storage</span></span>

* <span data-ttu-id="439e5-203">Добавлено -EnableHierarchicalNamespace к New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="439e5-203">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="439e5-204">Устранена проблема, из-за которой командлет Copy File не может повторно использовать исходный контекст в пункте назначения, если не введен -DestContext</span><span class="sxs-lookup"><span data-stu-id="439e5-204">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="439e5-205">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="439e5-205">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="439e5-206">Поддержка статической конфигурации сайта</span><span class="sxs-lookup"><span data-stu-id="439e5-206">Support Static Website configuration</span></span>
    - <span data-ttu-id="439e5-207">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="439e5-207">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="439e5-208">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="439e5-208">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="439e5-209">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="439e5-209">Az.Websites</span></span>

* <span data-ttu-id="439e5-210">Set-AzureRmWebApp и Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="439e5-210">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="439e5-211">Добавлен новый параметр (-AzureStoragePath), который указывает путь службы хранилища Azure для подключения в приложениях-контейнерах Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="439e5-211">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="439e5-212">Используйте выходные данные нового командлета New-AzureRmWebAppAzureStoragePath в качестве параметра, чтобы задать пути к службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="439e5-212">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="439e5-213">0.6.1 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="439e5-213">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="439e5-214">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="439e5-214">Az.ApiManagement</span></span>
* <span data-ttu-id="439e5-215">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="439e5-215">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="439e5-216">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="439e5-216">Az.Automation</span></span>
* <span data-ttu-id="439e5-217">Командлеты службы автоматизации Azure на базе Swagger.</span><span class="sxs-lookup"><span data-stu-id="439e5-217">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="439e5-218">Добавлены командлеты для Управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="439e5-218">Added Update Management cmdlets</span></span>
* <span data-ttu-id="439e5-219">Добавлены командлеты для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="439e5-219">Added Source Control cmdlets</span></span>
* <span data-ttu-id="439e5-220">Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="439e5-220">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="439e5-221">Исправлена команда DSC для регистрации узла.</span><span class="sxs-lookup"><span data-stu-id="439e5-221">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="439e5-222">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="439e5-222">Az.Compute</span></span>
* <span data-ttu-id="439e5-223">Исправлена проблема с удостоверением, назначаемым системой.</span><span class="sxs-lookup"><span data-stu-id="439e5-223">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="439e5-224">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="439e5-224">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="439e5-225">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="439e5-225">Az.ContainerInstance</span></span>
* <span data-ttu-id="439e5-226">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="439e5-226">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="439e5-227">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="439e5-227">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="439e5-228">Обновлено описание в примерах командлетов для Marketplace.</span><span class="sxs-lookup"><span data-stu-id="439e5-228">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="439e5-229">Az.Network</span><span class="sxs-lookup"><span data-stu-id="439e5-229">Az.Network</span></span>
* <span data-ttu-id="439e5-230">Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="439e5-230">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="439e5-231">Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="439e5-231">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="439e5-232">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="439e5-232">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="439e5-233">Исправлены проблемы с использованием памяти в карте виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="439e5-233">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="439e5-234">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="439e5-234">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="439e5-235">Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="439e5-235">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="439e5-236">Параметры часового пояса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="439e5-236">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="439e5-237">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="439e5-237">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="439e5-238">Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="439e5-238">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="439e5-239">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="439e5-239">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="439e5-240">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="439e5-240">Az.Relay</span></span>
* <span data-ttu-id="439e5-241">Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.</span><span class="sxs-lookup"><span data-stu-id="439e5-241">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="439e5-242">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="439e5-242">Az.Resources</span></span>
* <span data-ttu-id="439e5-243">Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.</span><span class="sxs-lookup"><span data-stu-id="439e5-243">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="439e5-244">Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.</span><span class="sxs-lookup"><span data-stu-id="439e5-244">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="439e5-245">Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.</span><span class="sxs-lookup"><span data-stu-id="439e5-245">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="439e5-246">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="439e5-246">Az.ServiceFabric</span></span>
* <span data-ttu-id="439e5-247">Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.</span><span class="sxs-lookup"><span data-stu-id="439e5-247">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="439e5-248">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="439e5-248">Az.Sql</span></span>
* <span data-ttu-id="439e5-249">Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="439e5-249">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="439e5-250">Get-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="439e5-250">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="439e5-251">New-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="439e5-251">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="439e5-252">Set-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="439e5-252">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="439e5-253">Remove-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="439e5-253">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="439e5-254">Get-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="439e5-254">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="439e5-255">New-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="439e5-255">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="439e5-256">Restore-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="439e5-256">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="439e5-257">Remove-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="439e5-257">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="439e5-258">Добавлено расширенное управление политиками аудита для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="439e5-258">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="439e5-259">Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="439e5-259">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="439e5-260">Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.</span><span class="sxs-lookup"><span data-stu-id="439e5-260">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="439e5-261">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="439e5-261">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="439e5-262">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="439e5-262">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="439e5-263">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="439e5-263">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="439e5-264">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="439e5-264">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="439e5-265">Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="439e5-265">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="439e5-266">0.5.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="439e5-266">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="439e5-267">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="439e5-267">General</span></span>
* <span data-ttu-id="439e5-268">Добавлены средства заполнения ресурсов для многих основных командлетов — они позволяют вам переключать существующие имена ресурсов при вызове командлетов в интерактивном режиме</span><span class="sxs-lookup"><span data-stu-id="439e5-268">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="439e5-269">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="439e5-269">Az.Profile</span></span>
* <span data-ttu-id="439e5-270">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="439e5-270">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="439e5-271">В командлете Connect-AzAccount параметр TenantId переименован в Tenant и добавлен псевдоним для TenantId</span><span class="sxs-lookup"><span data-stu-id="439e5-271">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="439e5-272">Обновлено описание TenantId для командлета Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="439e5-272">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="439e5-273">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="439e5-273">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="439e5-274">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="439e5-274">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="439e5-275">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="439e5-275">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="439e5-276">Устранена проблема, при которой командлет Disconnect-AzAccount вызывал сбой при отсутствии подключения</span><span class="sxs-lookup"><span data-stu-id="439e5-276">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="439e5-277">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="439e5-277">Az.CognitiveServices</span></span>
* <span data-ttu-id="439e5-278">Добавлена операция Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="439e5-278">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="439e5-279">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="439e5-279">Az.Compute</span></span>
* <span data-ttu-id="439e5-280">Добавлены командлеты Add-AzVmssVMDataDisk и Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="439e5-280">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="439e5-281">Get-AzVMImage отображает AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="439e5-281">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="439e5-282">Устранена проблема, при которой значения параметров SetAzVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="439e5-282">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="439e5-283">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="439e5-283">Az.DataLakeStore</span></span>
* <span data-ttu-id="439e5-284">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="439e5-284">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="439e5-285">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="439e5-285">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="439e5-286">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="439e5-286">Az.Insights</span></span>
* <span data-ttu-id="439e5-287">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="439e5-287">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="439e5-288">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="439e5-288">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="439e5-289">Исправлена проблема № 7513 [Insights], при которой для командлета Set-AzDiagnosticSetting требовалось явное указание категорий во время создания параметра</span><span class="sxs-lookup"><span data-stu-id="439e5-289">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="439e5-290">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="439e5-290">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="439e5-291">Az.Network</span><span class="sxs-lookup"><span data-stu-id="439e5-291">Az.Network</span></span>
* <span data-ttu-id="439e5-292">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="439e5-292">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="439e5-293">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="439e5-293">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="439e5-294">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="439e5-294">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="439e5-295">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="439e5-295">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="439e5-296">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="439e5-296">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="439e5-297">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="439e5-297">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="439e5-298">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="439e5-298">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="439e5-299">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="439e5-299">Az.PolicyInsights</span></span>
* <span data-ttu-id="439e5-300">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="439e5-300">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="439e5-301">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="439e5-301">Az.Resources</span></span>
* <span data-ttu-id="439e5-302">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="439e5-302">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="439e5-303">Разрешено перечисление ресурсов с помощью параметра -ResourceId для командлета Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="439e5-303">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="439e5-304">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="439e5-304">Az.ServiceBus</span></span>
* <span data-ttu-id="439e5-305">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="439e5-305">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="439e5-306">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="439e5-306">Az.ServiceFabric</span></span>
* <span data-ttu-id="439e5-307">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="439e5-307">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="439e5-308">Исправлен командлет Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="439e5-308">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="439e5-309">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="439e5-309">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="439e5-310">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="439e5-310">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="439e5-311">Исправлен командлет Update-AzServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="439e5-311">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="439e5-312">0.4.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="439e5-312">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="439e5-313">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="439e5-313">Az.Profile</span></span>
* <span data-ttu-id="439e5-314">Устранена проблема с Get-AzSubscription в CloudShell</span><span class="sxs-lookup"><span data-stu-id="439e5-314">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="439e5-315">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="439e5-315">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="439e5-316">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="439e5-316">Az.Compute</span></span>
* <span data-ttu-id="439e5-317">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzVm</span><span class="sxs-lookup"><span data-stu-id="439e5-317">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="439e5-318">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="439e5-318">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="439e5-319">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="439e5-319">Az.DataLakeStore</span></span>
* <span data-ttu-id="439e5-320">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="439e5-320">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="439e5-321">Get-AzDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="439e5-321">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="439e5-322">Add-AzDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="439e5-322">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="439e5-323">Set-AzDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="439e5-323">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="439e5-324">Remove-AzDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="439e5-324">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="439e5-325">Az.Network</span><span class="sxs-lookup"><span data-stu-id="439e5-325">Az.Network</span></span>
* <span data-ttu-id="439e5-326">Обновлен командлет Test-AzNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="439e5-326">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="439e5-327">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="439e5-327">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="439e5-328">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="439e5-328">Az.Resources</span></span>
* <span data-ttu-id="439e5-329">Устранена проблема, из-за которой командлет Get-AzRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), благодаря добавлению понятного исключения в сценарий.</span><span class="sxs-lookup"><span data-stu-id="439e5-329">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="439e5-330">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="439e5-330">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="439e5-331">0.3.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="439e5-331">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="439e5-332">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="439e5-332">Azure.Storage</span></span>
* <span data-ttu-id="439e5-333">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="439e5-333">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="439e5-334">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="439e5-334">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="439e5-335">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="439e5-335">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="439e5-336">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="439e5-336">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="439e5-337">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="439e5-337">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="439e5-338">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="439e5-338">Az.CognitiveServices</span></span>
* <span data-ttu-id="439e5-339">Поддержка Get-AzCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="439e5-339">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="439e5-340">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="439e5-340">Az.Compute</span></span>
* <span data-ttu-id="439e5-341">Исправлена команда Get-AzVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов</span><span class="sxs-lookup"><span data-stu-id="439e5-341">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="439e5-342">Добавлен пример использования SimpleParameterSet в справку командлета New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="439e5-342">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="439e5-343">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="439e5-343">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="439e5-344">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="439e5-344">Az.DataFactoryV2</span></span>
* <span data-ttu-id="439e5-345">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="439e5-345">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="439e5-346">Az.Network</span><span class="sxs-lookup"><span data-stu-id="439e5-346">Az.Network</span></span>
* <span data-ttu-id="439e5-347">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="439e5-347">Added NetworkProfile functionality.</span></span> <span data-ttu-id="439e5-348">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="439e5-348">new cmdlets added</span></span>
    - <span data-ttu-id="439e5-349">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="439e5-349">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="439e5-350">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="439e5-350">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="439e5-351">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="439e5-351">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="439e5-352">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="439e5-352">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="439e5-353">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="439e5-353">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="439e5-354">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="439e5-354">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="439e5-355">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="439e5-355">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="439e5-356">Добавлены командлеты: New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="439e5-356">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="439e5-357">Добавлены командлеты: Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="439e5-357">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="439e5-358">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="439e5-358">Az.RedisCache</span></span>
* <span data-ttu-id="439e5-359">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="439e5-359">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="439e5-360">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="439e5-360">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="439e5-361">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="439e5-361">Az.Resources</span></span>
* <span data-ttu-id="439e5-362">Добавлен отсутствующий параметр -Mode в командлет Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="439e5-362">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="439e5-363">Исправлена ошибка командлета Get-AzProviderOperation для операций, когда Origin содержит User</span><span class="sxs-lookup"><span data-stu-id="439e5-363">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="439e5-364">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="439e5-364">Az.Sql</span></span>
* <span data-ttu-id="439e5-365">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="439e5-365">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="439e5-366">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="439e5-366">Az.Websites</span></span>
* <span data-ttu-id="439e5-367">Новый командлет Get-AzWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="439e5-367">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="439e5-368">Новые командлеты New-AzWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows</span><span class="sxs-lookup"><span data-stu-id="439e5-368">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="439e5-369">0.2.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="439e5-369">0.2.0 - September 2018</span></span>
 <span data-ttu-id="439e5-370">Первый выпуск</span><span class="sxs-lookup"><span data-stu-id="439e5-370">Initial Release</span></span>