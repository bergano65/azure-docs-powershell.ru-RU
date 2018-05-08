# <a name="table-of-contents"></a><span data-ttu-id="b9188-101">Оглавление</span><span class="sxs-lookup"><span data-stu-id="b9188-101">Table of Contents</span></span>
1. [<span data-ttu-id="b9188-102">Удаление параметров Force</span><span class="sxs-lookup"><span data-stu-id="b9188-102">Removal of Force parameters</span></span>](#removal-of-force-parameters)
2. [<span data-ttu-id="b9188-103">Изменение параметров Tag</span><span class="sxs-lookup"><span data-stu-id="b9188-103">Change of Tag parameters</span></span>](#change-of-tag-parameters)
3. [<span data-ttu-id="b9188-104">Критические изменения в командлетах Storage</span><span class="sxs-lookup"><span data-stu-id="b9188-104">Breaking changes to Storage cmdlets</span></span>](#breaking-changes-to-storage-cmdlets)
4. [<span data-ttu-id="b9188-105">Критические изменения в командлетах AD</span><span class="sxs-lookup"><span data-stu-id="b9188-105">Breaking changes to AD cmdlets</span></span>](#breaking-changes-to-ad-cmdlets)

## <a name="removal-of-force-parameters"></a><span data-ttu-id="b9188-106">Удаление параметров Force</span><span class="sxs-lookup"><span data-stu-id="b9188-106">Removal of Force parameters</span></span>

<span data-ttu-id="b9188-107">В этом выпуске мы удалили все устаревшие параметры `Force` из командлетов и соответствующие предупреждения о том, что параметры будут удалены в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="b9188-107">This release, we removed all Obsolete `Force` parameters from cmdlets and the corresponding warnings that the parameter would be removed in a future release.</span></span>

<span data-ttu-id="b9188-108">Это изменение затрагивает следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="b9188-108">The following cmdlets are affected by this change:</span></span>

<span data-ttu-id="b9188-109">**ApiManagement**</span><span class="sxs-lookup"><span data-stu-id="b9188-109">**ApiManagement**</span></span>
- <span data-ttu-id="b9188-110">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="b9188-110">Remove-AzureRmApiManagement</span></span>
- <span data-ttu-id="b9188-111">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="b9188-111">Remove-AzureRmApiManagementApi</span></span>
- <span data-ttu-id="b9188-112">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="b9188-112">Remove-AzureRmApiManagementGroup</span></span>
- <span data-ttu-id="b9188-113">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="b9188-113">Remove-AzureRmApiManagementLogger</span></span>
- <span data-ttu-id="b9188-114">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="b9188-114">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>
- <span data-ttu-id="b9188-115">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="b9188-115">Remove-AzureRmApiManagementOperation</span></span>
- <span data-ttu-id="b9188-116">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="b9188-116">Remove-AzureRmApiManagementPolicy</span></span>
- <span data-ttu-id="b9188-117">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="b9188-117">Remove-AzureRmApiManagementProduct</span></span>
- <span data-ttu-id="b9188-118">Remove-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="b9188-118">Remove-AzureRmApiManagementProperty</span></span>
- <span data-ttu-id="b9188-119">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="b9188-119">Remove-AzureRmApiManagementSubscription</span></span>
- <span data-ttu-id="b9188-120">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="b9188-120">Remove-AzureRmApiManagementUser</span></span>

<span data-ttu-id="b9188-121">**Автоматизация**</span><span class="sxs-lookup"><span data-stu-id="b9188-121">**Automation**</span></span>
- <span data-ttu-id="b9188-122">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="b9188-122">Remove-AzureRmAutomationCertificate</span></span>
- <span data-ttu-id="b9188-123">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="b9188-123">Remove-AzureRmAutomationCredential</span></span>
- <span data-ttu-id="b9188-124">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="b9188-124">Remove-AzureRmAutomationVariable</span></span>
- <span data-ttu-id="b9188-125">Remove-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="b9188-125">Remove-AzureRmAutomationWebhook</span></span>

<span data-ttu-id="b9188-126">**Пакетная служба**</span><span class="sxs-lookup"><span data-stu-id="b9188-126">**Batch**</span></span>
- <span data-ttu-id="b9188-127">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="b9188-127">Remove-AzureBatchCertificate</span></span>
- <span data-ttu-id="b9188-128">Remove-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="b9188-128">Remove-AzureBatchComputeNode</span></span>
- <span data-ttu-id="b9188-129">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="b9188-129">Remove-AzureBatchComputeNodeUser</span></span>

<span data-ttu-id="b9188-130">**DataFactories**</span><span class="sxs-lookup"><span data-stu-id="b9188-130">**DataFactories**</span></span>
- <span data-ttu-id="b9188-131">Resume-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="b9188-131">Resume-AzureRmDataFactoryPipeline</span></span>
- <span data-ttu-id="b9188-132">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="b9188-132">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>
- <span data-ttu-id="b9188-133">Suspend-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="b9188-133">Suspend-AzureRmDataFactoryPipeline</span></span>

<span data-ttu-id="b9188-134">**DataLakeStore**</span><span class="sxs-lookup"><span data-stu-id="b9188-134">**DataLakeStore**</span></span>
- <span data-ttu-id="b9188-135">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b9188-135">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>
- <span data-ttu-id="b9188-136">Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="b9188-136">Set-AzureRmDataLakeStoreItemAcl</span></span>
- <span data-ttu-id="b9188-137">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b9188-137">Set-AzureRmDataLakeStoreItemAclEntry</span></span>
- <span data-ttu-id="b9188-138">Set-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="b9188-138">Set-AzureRmDataLakeStoreItemOwner</span></span>

<span data-ttu-id="b9188-139">**OperationalInsights**</span><span class="sxs-lookup"><span data-stu-id="b9188-139">**OperationalInsights**</span></span>
- <span data-ttu-id="b9188-140">Remove-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="b9188-140">Remove-AzureRmOperationalInsightsSavedSearch</span></span>

<span data-ttu-id="b9188-141">**Профиль**</span><span class="sxs-lookup"><span data-stu-id="b9188-141">**Profile**</span></span>
- <span data-ttu-id="b9188-142">Remove-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="b9188-142">Remove-AzureRmEnvironment</span></span>

<span data-ttu-id="b9188-143">**Кэш Redis**</span><span class="sxs-lookup"><span data-stu-id="b9188-143">**RedisCache**</span></span>
- <span data-ttu-id="b9188-144">Remove-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="b9188-144">Remove-AzureRmRedisCacheDiagnostics</span></span>

<span data-ttu-id="b9188-145">**Ресурсы**</span><span class="sxs-lookup"><span data-stu-id="b9188-145">**Resources**</span></span>
- <span data-ttu-id="b9188-146">Register-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="b9188-146">Register-AzureRmProviderFeature</span></span>
- <span data-ttu-id="b9188-147">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="b9188-147">Register-AzureRmResourceProvider</span></span>
- <span data-ttu-id="b9188-148">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b9188-148">Remove-AzureRmADServicePrincipal</span></span>
- <span data-ttu-id="b9188-149">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b9188-149">Remove-AzureRmPolicyAssignment</span></span>
- <span data-ttu-id="b9188-150">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b9188-150">Remove-AzureRmResourceGroupDeployment</span></span>
- <span data-ttu-id="b9188-151">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="b9188-151">Remove-AzureRmRoleAssignment</span></span>
- <span data-ttu-id="b9188-152">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b9188-152">Stop-AzureRmResourceGroupDeployment</span></span>
- <span data-ttu-id="b9188-153">Unregister-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="b9188-153">Unregister-AzureRmResourceProvider</span></span>

<span data-ttu-id="b9188-154">**Хранилище**</span><span class="sxs-lookup"><span data-stu-id="b9188-154">**Storage**</span></span>
- <span data-ttu-id="b9188-155">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b9188-155">Remove-AzureStorageContainerStoredAccessPolicy</span></span>
- <span data-ttu-id="b9188-156">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b9188-156">Remove-AzureStorageQueueStoredAccessPolicy</span></span>
- <span data-ttu-id="b9188-157">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b9188-157">Remove-AzureStorageShareStoredAccessPolicy</span></span>
- <span data-ttu-id="b9188-158">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b9188-158">Remove-AzureStorageTableStoredAccessPolicy</span></span>

<span data-ttu-id="b9188-159">**StreamAnalytics**</span><span class="sxs-lookup"><span data-stu-id="b9188-159">**StreamAnalytics**</span></span>
- <span data-ttu-id="b9188-160">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="b9188-160">Remove-AzureRmStreamAnalyticsFunction</span></span>
- <span data-ttu-id="b9188-161">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="b9188-161">Remove-AzureRmStreamAnalyticsInput</span></span>
- <span data-ttu-id="b9188-162">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="b9188-162">Remove-AzureRmStreamAnalyticsJob</span></span>
- <span data-ttu-id="b9188-163">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="b9188-163">Remove-AzureRmStreamAnalyticsOutput</span></span>

<span data-ttu-id="b9188-164">**Tag**</span><span class="sxs-lookup"><span data-stu-id="b9188-164">**Tag**</span></span>
- <span data-ttu-id="b9188-165">Remove-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="b9188-165">Remove-AzureRmTag</span></span>

<br>

<span data-ttu-id="b9188-166">Если в вашем скрипте используется любой указанный выше командлет, можно применить критическое изменение, просто удалив параметр `Force`.</span><span class="sxs-lookup"><span data-stu-id="b9188-166">If you have a script that uses any of the above cmdlets, the breaking change can be fixed by simply removing the `Force` parameter.</span></span>

```powershell
# Old
New-AzureRmResourceGroup -Name $resourceGroupName -Location $location -Force

# New
New-AzureRmResourceGroup -Name $resourceGroupName -Location $location
```

<br>

## <a name="change-of-tag-parameters"></a><span data-ttu-id="b9188-167">Изменение параметров Tag</span><span class="sxs-lookup"><span data-stu-id="b9188-167">Change of Tag parameters</span></span>

<span data-ttu-id="b9188-168">В этом выпуске имя параметра `Tags` изменено на `Tag`, а тип изменен с `Hashtable[]` на `Hashtable`, что преобразовало формат пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="b9188-168">This release, the `Tags` parameter name was changed to `Tag`, and the type was changed from `Hashtable[]` to `Hashtable`, changing the format of the key-value pairings.</span></span>

<span data-ttu-id="b9188-169">Ранее каждая запись в `Hashtable[]` представляла одну пара "ключ-значение":</span><span class="sxs-lookup"><span data-stu-id="b9188-169">Previously, each entry in the `Hashtable[]` represented a single key-value pairing:</span></span>

```powershell
$tags = @{ Name = "test1"; Value = "testval1" }, @{ Name = "test2", Value = "testval2" }
$tags[0].Name  # Key for the first entry, "test1"
$tags[0].Value # Value for the first entry, "testval1"
$tags[1].Name  # Key for the second entry, "test2"
$tags[1].Value # Value for the second entry, "testval2"
```

<span data-ttu-id="b9188-170">Теперь `Name` и `Value` больше не нужны. Это позволяет создавать пары "ключ-значение", назначив `Key = "Value"` в `Hashtable`:</span><span class="sxs-lookup"><span data-stu-id="b9188-170">Now, `Name` and `Value` are no longer necessary, allowing for key-value pairings to be created by assigning `Key = "Value"` in the `Hashtable`:</span></span>

```powershell
$tag = @{ test1 = "testval1"; test2 = "testval2" }
$tag["test1"] # Gets the value associated with the key "test1"
$tag["test2"] # Gets the value associated with the key "test2"
```

<span data-ttu-id="b9188-171">Это изменение затрагивает следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="b9188-171">The following cmdlets are affected by this change:</span></span>

<span data-ttu-id="b9188-172">**Пакетная служба**</span><span class="sxs-lookup"><span data-stu-id="b9188-172">**Batch**</span></span>
- <span data-ttu-id="b9188-173">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="b9188-173">Get-AzureRmBatchAccount</span></span>
- <span data-ttu-id="b9188-174">New-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="b9188-174">New-AzureRmBatchAccount</span></span>
- <span data-ttu-id="b9188-175">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="b9188-175">Set-AzureRmBatchAccount</span></span>

<span data-ttu-id="b9188-176">**Среда выполнения приложений**</span><span class="sxs-lookup"><span data-stu-id="b9188-176">**Compute**</span></span>
- <span data-ttu-id="b9188-177">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b9188-177">New-AzureRmVM</span></span>
- <span data-ttu-id="b9188-178">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b9188-178">Update-AzureRmVM</span></span>

<span data-ttu-id="b9188-179">**DataLakeAnalytics**</span><span class="sxs-lookup"><span data-stu-id="b9188-179">**DataLakeAnalytics**</span></span>
- <span data-ttu-id="b9188-180">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="b9188-180">New-AzureRmDataLakeAnalyticsAccount</span></span>
- <span data-ttu-id="b9188-181">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="b9188-181">Set-AzureRmDataLakeAnalyticsAccount</span></span>

<span data-ttu-id="b9188-182">**DataLakeStore**</span><span class="sxs-lookup"><span data-stu-id="b9188-182">**DataLakeStore**</span></span>
- <span data-ttu-id="b9188-183">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="b9188-183">New-AzureRmDataLakeStoreAccount</span></span>
- <span data-ttu-id="b9188-184">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="b9188-184">Set-AzureRmDataLakeStoreAccount</span></span>

<span data-ttu-id="b9188-185">**Dns**</span><span class="sxs-lookup"><span data-stu-id="b9188-185">**Dns**</span></span>
- <span data-ttu-id="b9188-186">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="b9188-186">New-AzureRmDnsZone</span></span>
- <span data-ttu-id="b9188-187">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="b9188-187">Set-AzureRmDnsZone</span></span>

<span data-ttu-id="b9188-188">**Хранилище ключей**</span><span class="sxs-lookup"><span data-stu-id="b9188-188">**KeyVault**</span></span>
- <span data-ttu-id="b9188-189">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="b9188-189">Get-AzureRmKeyVault</span></span>
- <span data-ttu-id="b9188-190">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="b9188-190">New-AzureRmKeyVault</span></span>

<span data-ttu-id="b9188-191">**Сеть**</span><span class="sxs-lookup"><span data-stu-id="b9188-191">**Network**</span></span>
- <span data-ttu-id="b9188-192">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9188-192">New-AzureRmApplicationGateway</span></span>
- <span data-ttu-id="b9188-193">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b9188-193">New-AzureRmExpressRouteCircuit</span></span>
- <span data-ttu-id="b9188-194">New-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b9188-194">New-AzureRmLoadBalancer</span></span>
- <span data-ttu-id="b9188-195">New-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b9188-195">New-AzureRmLocalNetworkGateway</span></span>
- <span data-ttu-id="b9188-196">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b9188-196">New-AzureRmNetworkInterface</span></span>
- <span data-ttu-id="b9188-197">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b9188-197">New-AzureRmNetworkSecurityGroup</span></span>
- <span data-ttu-id="b9188-198">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b9188-198">New-AzureRmPublicIpAddress</span></span>
- <span data-ttu-id="b9188-199">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="b9188-199">New-AzureRmRouteTable</span></span>
- <span data-ttu-id="b9188-200">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b9188-200">New-AzureRmVirtualNetwork</span></span>
- <span data-ttu-id="b9188-201">New-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b9188-201">New-AzureRmVirtualNetworkGateway</span></span>
- <span data-ttu-id="b9188-202">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b9188-202">New-AzureRmVirtualNetworkGatewayConnection</span></span>
- <span data-ttu-id="b9188-203">New-AzureRmVirtualNetworkPeering.</span><span class="sxs-lookup"><span data-stu-id="b9188-203">New-AzureRmVirtualNetworkPeering</span></span>

<span data-ttu-id="b9188-204">**Ресурсы**</span><span class="sxs-lookup"><span data-stu-id="b9188-204">**Resources**</span></span>
- <span data-ttu-id="b9188-205">Find-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b9188-205">Find-AzureRmResource</span></span>
- <span data-ttu-id="b9188-206">Find-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b9188-206">Find-AzureRmResourceGroup</span></span>
- <span data-ttu-id="b9188-207">New-AzureRmResource;</span><span class="sxs-lookup"><span data-stu-id="b9188-207">New-AzureRmResource</span></span>
- <span data-ttu-id="b9188-208">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b9188-208">New-AzureRmResourceGroup</span></span>
- <span data-ttu-id="b9188-209">Set-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="b9188-209">Set-AzureRmResource</span></span>
- <span data-ttu-id="b9188-210">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b9188-210">Set-AzureRmResourceGroup</span></span>

<span data-ttu-id="b9188-211">**SQL**</span><span class="sxs-lookup"><span data-stu-id="b9188-211">**SQL**</span></span>
- <span data-ttu-id="b9188-212">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b9188-212">New-AzureRmSqlDatabase</span></span>
- <span data-ttu-id="b9188-213">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="b9188-213">New-AzureRmSqlDatabaseCopy</span></span>
- <span data-ttu-id="b9188-214">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b9188-214">New-AzureRmSqlDatabaseSecondary</span></span>
- <span data-ttu-id="b9188-215">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="b9188-215">New-AzureRmSqlElasticPool</span></span>
- <span data-ttu-id="b9188-216">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="b9188-216">New-AzureRmSqlServer</span></span>
- <span data-ttu-id="b9188-217">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b9188-217">Set-AzureRmSqlDatabase</span></span>
- <span data-ttu-id="b9188-218">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="b9188-218">Set-AzureRmSqlElasticPool</span></span>
- <span data-ttu-id="b9188-219">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="b9188-219">Set-AzureRmSqlServer</span></span>

<span data-ttu-id="b9188-220">**Хранилище**</span><span class="sxs-lookup"><span data-stu-id="b9188-220">**Storage**</span></span>
- <span data-ttu-id="b9188-221">New-AzureRmStorageAccount;</span><span class="sxs-lookup"><span data-stu-id="b9188-221">New-AzureRmStorageAccount</span></span>
- <span data-ttu-id="b9188-222">Set-AzureRmStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="b9188-222">Set-AzureRmStorageAccount</span></span>

<span data-ttu-id="b9188-223">**TrafficManager**</span><span class="sxs-lookup"><span data-stu-id="b9188-223">**TrafficManager**</span></span>
- <span data-ttu-id="b9188-224">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b9188-224">New-AzureRmTrafficManagerProfile</span></span>

<br>

<span data-ttu-id="b9188-225">Если в вашем скрипте используется любой указанный выше командлет, можно применить критическое изменение, изменив параметр `Tags` на `Tag`, а также преобразовав `Tag` в новый формат.</span><span class="sxs-lookup"><span data-stu-id="b9188-225">If you have a script that uses any of the above cmdlets, the breaking change can be fixed by changing the `Tags` parameter to `Tag`, as well as changing the `Tag` to the new format.</span></span>

```powershell
# Old
New-AzureRmResourceGroup -Name $resourceGroupName -Location -location -Tags @{ Name = "testtag"; Value = "testval" }

# New
New-AzureRmResourceGroup -Name $resourceGroupName -Location -location -Tag @{ testtag = "testval" }
```

<br>

## <a name="breaking-changes-to-storage-cmdlets"></a><span data-ttu-id="b9188-226">Критические изменения в командлетах Storage</span><span class="sxs-lookup"><span data-stu-id="b9188-226">Breaking changes to Storage cmdlets</span></span>

<span data-ttu-id="b9188-227">В этом выпуске затронуты следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="b9188-227">The following cmdlets were affected this release:</span></span>

<span data-ttu-id="b9188-228">**Get-AzureRmStorageAccountKey**</span><span class="sxs-lookup"><span data-stu-id="b9188-228">**Get-AzureRmStorageAccountKey**</span></span>
- <span data-ttu-id="b9188-229">Командлет возвращает список ключей, а не объект со свойствами для каждого ключа</span><span class="sxs-lookup"><span data-stu-id="b9188-229">The cmdlet now returns a list of keys, rather than an object with properties for each key</span></span>

```powershell
# Old
$key = (Get-AzureRmStorageAccountKey -ResourceGroupName $resourceGroupName -Name $accountName).Key1

# New
$key = (Get-AzureRmStorageAccountKey -ResourceGroupName $resourceGroupName -Name $accountName)[0].Value
```

<span data-ttu-id="b9188-230">**New-AzureRmStorageAccountKey**</span><span class="sxs-lookup"><span data-stu-id="b9188-230">**New-AzureRmStorageAccountKey**</span></span>
- <span data-ttu-id="b9188-231">Поле `StorageAccountRegenerateKeyResponse` в выходных данных командлета переименовано в `StorageAccountListKeysResults`, которое теперь является списком ключей, а не объектом со свойствами для каждого ключа.</span><span class="sxs-lookup"><span data-stu-id="b9188-231">`StorageAccountRegenerateKeyResponse` field in output of this cmdlet is renamed to `StorageAccountListKeysResults`, which is now a list of keys rather than an object with properties for each key</span></span>

```powershell
# Old
$key = (New-AzureRmStorageAccountKey -ResourceGroupName $resourceGroupName -Name $accountName).StorageAccountKeys.Key1

# New
$key = (New-AzureRmStorageAccountKey -ResourceGroupName $resourceGroupName -Name $accountName).Keys[0].Value
```

<span data-ttu-id="b9188-232">**New/Get/Set-AzureRmStorageAccount**</span><span class="sxs-lookup"><span data-stu-id="b9188-232">**New/Get/Set-AzureRmStorageAccount**</span></span>
- <span data-ttu-id="b9188-233">Поле `AccountType` в выходных данных этого командлета переименовано в `Sku.Name`.</span><span class="sxs-lookup"><span data-stu-id="b9188-233">`AccountType` field in output of this cmdlet is renamed to `Sku.Name`</span></span>
- <span data-ttu-id="b9188-234">Тип выходных данных первичных и вторичных конечных точек для больших двоичных объектов, таблиц, очередей и файлов изменен с `Uri` на `String`.</span><span class="sxs-lookup"><span data-stu-id="b9188-234">Output type for PrimaryEndpoints/Secondary endpoints blob/table/queue/file changed from `Uri` to `String`</span></span>

```powershell
# Old
$accountType = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).AccountType

# New
$accountType = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).Sku.Name
```

```powershell
# Old 
$blobEndpoint = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).PrimaryEndpoints.Blob.ToString()
$blobEndpoint = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).PrimaryEndpoints.Blob.AbsolutePath

# New
$blobEndpoint = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).PrimaryEndpoints.Blob.ToString()
$blobEndpoint = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).PrimaryEndpoints.Blob
```

<br>

## <a name="breaking-changes-to-ad-cmdlets"></a><span data-ttu-id="b9188-235">Критические изменения в командлетах AD</span><span class="sxs-lookup"><span data-stu-id="b9188-235">Breaking changes to AD cmdlets</span></span>

<span data-ttu-id="b9188-236">В этом выпуске затронуты следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="b9188-236">The following cmdlets were affected this release:</span></span>

<span data-ttu-id="b9188-237">**Get-AzureRMADServicePrincipal**</span><span class="sxs-lookup"><span data-stu-id="b9188-237">**Get-AzureRMADServicePrincipal**</span></span>
- <span data-ttu-id="b9188-238">Поле `ServicePrincipalName` в выходных данных этого командлета переименовано в `ServicePrincipalNames` и теперь является коллекцией.</span><span class="sxs-lookup"><span data-stu-id="b9188-238">`ServicePrincipalName` field in output of this cmdlet is renamed to `ServicePrincipalNames` and is now a collection.</span></span> <span data-ttu-id="b9188-239">Теперь `ApplicationId` отображается также как одно из имен субъекта-службы с identifierUri.</span><span class="sxs-lookup"><span data-stu-id="b9188-239">It now displays `ApplicationId` also as one of the SPN, along with the identifierUri.</span></span>

```powershell
# Old
$servicePrincipals = Get-AzureRmADServicePrincipal -SearchString $displayName
$spn = $servicePrincipals[0].ServicePrincipalName

# New
$servicePrincipals = Get-AzureRmADServicePrincipal -SearchString $displayName
$spn = $servicePrincipals[0].ServicePrincipalNames[0]
```

<span data-ttu-id="b9188-240">**Get-AzureRmADApplication**</span><span class="sxs-lookup"><span data-stu-id="b9188-240">**Get-AzureRmADApplication**</span></span>
- <span data-ttu-id="b9188-241">Параметр `ApplicationObjectId` переименован в `ObjectId`.</span><span class="sxs-lookup"><span data-stu-id="b9188-241">Parameter `ApplicationObjectId` is renamed to `ObjectId`.</span></span>
- <span data-ttu-id="b9188-242">В выходных данных этого командлета поле `ApplicationObjectId` переименовано в `ObjectId`.</span><span class="sxs-lookup"><span data-stu-id="b9188-242">In output of this cmdlet, `ApplicationObjectId` is renamed to `ObjectId`.</span></span>

```powershell
# Old
$app = Get-AzureRmADApplication -ApplicationObjectId $applicationObjectId
$objectId = $app.ApplicationObjectId

# New
$app = Get-AzureRmADApplication -ObjectId $objectId
$objectId = $app.ObjectId
```

<span data-ttu-id="b9188-243">**Remove-AzureRmADApplication**</span><span class="sxs-lookup"><span data-stu-id="b9188-243">**Remove-AzureRmADApplication**</span></span>
- <span data-ttu-id="b9188-244">Параметр `ApplicationObjectId` переименован в `ObjectId`.</span><span class="sxs-lookup"><span data-stu-id="b9188-244">Parameter `ApplicationObjectId` is renamed to `ObjectId`.</span></span>

```powershell
# Old
$app = Remove-AzureRmADApplication -ApplicationObjectId $applicationObjectId -Force

# New
$app = Remove-AzureRmADApplication -ObjectId $objectId -Force
```

<span data-ttu-id="b9188-245">**New-AzureRmADApplication**</span><span class="sxs-lookup"><span data-stu-id="b9188-245">**New-AzureRmADApplication**</span></span>
- <span data-ttu-id="b9188-246">В выходных данных этого командлета поле `ApplicationObjectId` переименовано в `ObjectId`.</span><span class="sxs-lookup"><span data-stu-id="b9188-246">In output of this cmdlet, `ApplicationObjectId` is renamed to `ObjectId`.</span></span>
- <span data-ttu-id="b9188-247">Удалены параметры `KeyValue`, `KeyUsage` и `KeyType`.</span><span class="sxs-lookup"><span data-stu-id="b9188-247">`KeyValue`, `KeyUsage`, `KeyType` parameters are removed.</span></span>

```powershell
# Old
$app = New-AzureRmADApplication -DisplayName $displayName -HomePage $homePage -IdentifierUris $identifierUris -KeyValue $kv -KeyType $kt -KeyUsage $ku
$id = $app.ApplicationObjectId

# New
$app = New-AzureRmADApplication -DisplayName $displayName -HomePage $homePage -IdentifierUris $identifierUris
$id = $app.ObjectId
New-AzureRmADAppCredential -ObjectId $id -Password $kv
```

<span data-ttu-id="b9188-248">**Get-AzureRmADGroup**</span><span class="sxs-lookup"><span data-stu-id="b9188-248">**Get-AzureRmADGroup**</span></span>
- <span data-ttu-id="b9188-249">Поле `Mail` удалено из выходных данных.</span><span class="sxs-lookup"><span data-stu-id="b9188-249">`Mail` field is removed from the output.</span></span>

<span data-ttu-id="b9188-250">**Get-AzureRmADUser**</span><span class="sxs-lookup"><span data-stu-id="b9188-250">**Get-AzureRmADUser**</span></span>
- <span data-ttu-id="b9188-251">Поле `Mail` удалено из выходных данных.</span><span class="sxs-lookup"><span data-stu-id="b9188-251">`Mail` field is removed from the output.</span></span>

<span data-ttu-id="b9188-252">**New-AzureRmADServicePrincipal**</span><span class="sxs-lookup"><span data-stu-id="b9188-252">**New-AzureRmADServicePrincipal**</span></span>
- <span data-ttu-id="b9188-253">Удален параметр `DisableAccount`.</span><span class="sxs-lookup"><span data-stu-id="b9188-253">Removed `DisableAccount` parameter.</span></span>

```powershell
# Old
$servicePrincipal = New-AzureRmADServicePrincipal -DisplayName $displayName -Password $password -DisableAccount true

# New
$servicePrincipal = New-AzureRmADServicePrincipal -DisplayName $displayName -Password $password
Remove-AzureRmADServicePrincipal -ObjectId $servicePrincipal.ObjectId
```