---
ms.openlocfilehash: 77cb28e47d8dddcf3936edff23f794de3b78442b
ms.sourcegitcommit: b02cbcd00748a4a9a4790a5fba229ce53c3bf973
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/09/2019
ms.locfileid: "68861194"
---
## <a name="250---july-2019"></a><span data-ttu-id="3d158-101">2.5.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="3d158-101">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3d158-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3d158-102">Az.Accounts</span></span>
* <span data-ttu-id="3d158-103">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3d158-103">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="3d158-104">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="3d158-104">Az.ApplicationInsights</span></span>
* <span data-ttu-id="3d158-105">Исправлена опечатка в примере в документации по Remove-AzApplicationInsightsApiKey.</span><span class="sxs-lookup"><span data-stu-id="3d158-105">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="3d158-106">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3d158-106">Az.Automation</span></span>
* <span data-ttu-id="3d158-107">Исправлена опечатка в строке ресурса.</span><span class="sxs-lookup"><span data-stu-id="3d158-107">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="3d158-108">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3d158-108">Az.CognitiveServices</span></span>
* <span data-ttu-id="3d158-109">Добавлена поддержка NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="3d158-109">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3d158-110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3d158-110">Az.Compute</span></span>
* <span data-ttu-id="3d158-111">Добавлены недостающие свойства (ComputerName, OsName, OsVersion и HyperVGeneration) для объекта представления экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3d158-111">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="3d158-112">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="3d158-112">Az.ContainerRegistry</span></span>
* <span data-ttu-id="3d158-113">Исправлена опечатка в Remove-AzContainerRegistryReplication для параметра репликации.</span><span class="sxs-lookup"><span data-stu-id="3d158-113">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="3d158-114">См. подробнее: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="3d158-114">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3d158-115">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3d158-115">Az.DataFactory</span></span>
* <span data-ttu-id="3d158-116">Пакет SDK для ADF .NET обновлен до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="3d158-116">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="3d158-117">Исправлена опечатка в документации по Get-AzDataFactoryV2PipelineRun.</span><span class="sxs-lookup"><span data-stu-id="3d158-117">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="3d158-118">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="3d158-118">Az.EventHub</span></span>
* <span data-ttu-id="3d158-119">Добавлен новый командлет для создания маркера SAS: New-AzEventHubAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="3d158-119">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="3d158-120">Добавлена проверка и сообщение об ошибке для случаев, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="3d158-120">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="3d158-121">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3d158-121">Az.KeyVault</span></span>
* <span data-ttu-id="3d158-122">Добавлена поддержка для настройки параметра KeySize в политиках сертификатов.</span><span class="sxs-lookup"><span data-stu-id="3d158-122">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="3d158-123">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="3d158-123">Az.LogicApp</span></span>
* <span data-ttu-id="3d158-124">Get-AzIntegrationAccountMap теперь надлежащим образом выводит все типы сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="3d158-124">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="3d158-125">Добавлен новый параметр MapType для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="3d158-125">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="3d158-126">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="3d158-126">Az.ManagedServices</span></span>
* <span data-ttu-id="3d158-127">Добавлена поддержка API версии 2019-06-01 (общедоступная).</span><span class="sxs-lookup"><span data-stu-id="3d158-127">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3d158-128">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3d158-128">Az.Network</span></span>
* <span data-ttu-id="3d158-129">Добавлена поддержка частной конечной точки и службы приватного канала.</span><span class="sxs-lookup"><span data-stu-id="3d158-129">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="3d158-130">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="3d158-130">New cmdlets</span></span>
        - <span data-ttu-id="3d158-131">Set-AzPrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="3d158-131">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="3d158-132">Set-AzPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="3d158-132">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="3d158-133">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="3d158-133">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="3d158-134">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="3d158-134">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="3d158-135">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="3d158-135">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="3d158-136">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="3d158-136">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="3d158-137">Test-AzPrivateLinkServiceVisibility.</span><span class="sxs-lookup"><span data-stu-id="3d158-137">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="3d158-138">Get-AzAutoApprovedPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="3d158-138">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="3d158-139">Обновлены следующие команды для функции: Флаг PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies в подсети в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="3d158-139">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="3d158-140">Обновлены командлеты New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig.</span><span class="sxs-lookup"><span data-stu-id="3d158-140">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="3d158-141">Добавлен необязательный параметр -PrivateEndpointNetworkPoliciesFlag, который указывает, что включение или отключение приводят к применению политик сети на частной конечной точке в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="3d158-141">Added optional parameter -PrivateEndpointNetworkPoliciesFlag to indicate that enable or disable apply network policies on pivate endpoint in this subnet.</span></span>
        - <span data-ttu-id="3d158-142">Добавлен необязательный параметр -PrivateLinkServiceNetworkPoliciesFlag, который указывает, что включение или отключение приводят к применению политик сети в службе приватного канала в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="3d158-142">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag to indicate that enable or disable apply network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="3d158-143">Параметр ServiceName командлета AzPrivateLinkService был переименован на Name с псевдонимом ServiceName для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="3d158-143">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="3d158-144">Включен протокол ICMP для настройки правил безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="3d158-144">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="3d158-145">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="3d158-145">Updated cmdlets</span></span>
        - <span data-ttu-id="3d158-146">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="3d158-146">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="3d158-147">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="3d158-147">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="3d158-148">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="3d158-148">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="3d158-149">Добавлен ConnectionProtocolType (Ikev1/Ikev2) в качестве настраиваемого параметра для командлета New-AzVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="3d158-149">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="3d158-150">Добавлен PrivateIpAddressVersion в LoadBalancerFrontendIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="3d158-150">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="3d158-151">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="3d158-151">Updated cmdlet:</span></span>
        - <span data-ttu-id="3d158-152">New-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="3d158-152">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="3d158-153">Add-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="3d158-153">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="3d158-154">Set-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="3d158-154">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="3d158-155">Команда New-AzApplicationGatewayProbeConfig Шлюза приложений обновлена для поддержки настраиваемого порта в зонде.</span><span class="sxs-lookup"><span data-stu-id="3d158-155">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="3d158-156">Обновлен командлет New-AzApplicationGatewayProbeConfig: добавлен необязательный параметр Port, который используется при проверке внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="3d158-156">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="3d158-157">Этот параметр применяется к номерам SKU Standard_V2 и WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="3d158-157">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="3d158-158">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3d158-158">Az.OperationalInsights</span></span>
* <span data-ttu-id="3d158-159">Обновленная версия по умолчанию для сохраненных операций поиска имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="3d158-159">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="3d158-160">Исправлены ошибки при обработке регулярных выражений со значениями NULL в журналах.</span><span class="sxs-lookup"><span data-stu-id="3d158-160">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3d158-161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3d158-161">Az.RecoveryServices</span></span>
* <span data-ttu-id="3d158-162">Обновлен файл Get-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="3d158-162">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="3d158-163">Обновлен файл Get-AzRecoveryServicesBackupContainer.md.</span><span class="sxs-lookup"><span data-stu-id="3d158-163">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="3d158-164">Обновлен файл Get-AzRecoveryServicesVault.md.</span><span class="sxs-lookup"><span data-stu-id="3d158-164">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="3d158-165">Обновлен файл Wait-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="3d158-165">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="3d158-166">Обновлен файл Set-AzRecoveryServicesVaultContext.md.</span><span class="sxs-lookup"><span data-stu-id="3d158-166">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="3d158-167">Обновлен файл Get-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="3d158-167">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="3d158-168">Обновлен файл Get-AzRecoveryServicesBackupRecoveryPoint.md.</span><span class="sxs-lookup"><span data-stu-id="3d158-168">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="3d158-169">Обновлен файл Restore-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="3d158-169">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="3d158-170">Обновлен вызов службы для отмены регистрации контейнера в общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="3d158-170">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="3d158-171">Обновлен файл Set-AzRecoveryServicesAsrAlertSetting.md.</span><span class="sxs-lookup"><span data-stu-id="3d158-171">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="3d158-172">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3d158-172">Az.Resources</span></span>
- <span data-ttu-id="3d158-173">Удален отсутствующий командлет, который упоминается в документации по New-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="3d158-173">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="3d158-174">Обновлены командлеты политик для использования новой версии API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="3d158-174">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="3d158-175">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3d158-175">Az.ServiceBus</span></span>
* <span data-ttu-id="3d158-176">Добавлен новый командлет для создания маркера SAS: New-AzServiceBusAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="3d158-176">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="3d158-177">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="3d158-177">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="3d158-178">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3d158-178">Az.Sql</span></span>
* <span data-ttu-id="3d158-179">Исправлены отсутствующие примеры для командлета Set-AzSqlDatabaseSecondary.</span><span class="sxs-lookup"><span data-stu-id="3d158-179">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="3d158-180">Исправлены заданные повторяющиеся проверки для оценки наличия уязвимостей без указания адресов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="3d158-180">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="3d158-181">Исправлена незначительная опечатка в сообщении предупреждения.</span><span class="sxs-lookup"><span data-stu-id="3d158-181">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3d158-182">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3d158-182">Az.Storage</span></span>
* <span data-ttu-id="3d158-183">Обновлен пример в справочной документации для использования командлетом Get-AzStorageAccount правильного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="3d158-183">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="3d158-184">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="3d158-184">Az.StorageSync</span></span>
* <span data-ttu-id="3d158-185">Добавлен командлет Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="3d158-185">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="3d158-186">Исправлена проблема № 9551, связанная с TierFilesOlderThanDays.</span><span class="sxs-lookup"><span data-stu-id="3d158-186">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3d158-187">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3d158-187">Az.Websites</span></span>
* <span data-ttu-id="3d158-188">Исправлена ошибка, при которой некоторые свойства SiteConfig не возвращались Get-AzWebApp и Set-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="3d158-188">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="3d158-189">Добавлен новый параметр Location в Get-AzDeletedWebApp и Restore-AzDeletedWebApp.</span><span class="sxs-lookup"><span data-stu-id="3d158-189">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="3d158-190">Исправлена ошибка, которая возникала при клонировании слотов веб-приложений с помощью командлета New-AzWebApp-IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="3d158-190">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="3d158-191">2.4.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="3d158-191">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3d158-192">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3d158-192">Az.Accounts</span></span>
* <span data-ttu-id="3d158-193">Добавлена поддержка командлетов профиля.</span><span class="sxs-lookup"><span data-stu-id="3d158-193">Add support for profile cmdlets</span></span>
* <span data-ttu-id="3d158-194">Добавлена поддержка сред и плоскостей данных в созданных командлетах.</span><span class="sxs-lookup"><span data-stu-id="3d158-194">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="3d158-195">Исправлена ошибка, когда в командлетах плоскости данных в Windows PowerShell в некоторых случаях использовалась неправильная конечная точка.</span><span class="sxs-lookup"><span data-stu-id="3d158-195">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="3d158-196">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="3d158-196">Az.Advisor</span></span>
* <span data-ttu-id="3d158-197">Выпущена общедоступная версия Az.Advisor.</span><span class="sxs-lookup"><span data-stu-id="3d158-197">GA release of Az.Advisor</span></span>
* <span data-ttu-id="3d158-198">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="3d158-198">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="3d158-199">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3d158-199">Az.ApiManagement</span></span>
* <span data-ttu-id="3d158-200">исправлена проблема https://github.com/Azure/azure-powershell/issues/8671.</span><span class="sxs-lookup"><span data-stu-id="3d158-200">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="3d158-201">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="3d158-201">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="3d158-202">Добавлена поддержка запрашивания подписок по пользователю и продукту.</span><span class="sxs-lookup"><span data-stu-id="3d158-202">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="3d158-203">Добавлена поддержка создания запросов с использованием области "/", "/apis", "/apis/echo-api".</span><span class="sxs-lookup"><span data-stu-id="3d158-203">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="3d158-204">Исправлены проблемы https://github.com/Azure/azure-powershell/issues/9307 и https://github.com/Azure/azure-powershell/issues/8432.</span><span class="sxs-lookup"><span data-stu-id="3d158-204">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="3d158-205">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="3d158-205">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="3d158-206">Добавлена поддержка указания ApiVersion и ApiVersionSetId при импорте API-интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="3d158-206">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3d158-207">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3d158-207">Az.Automation</span></span>
* <span data-ttu-id="3d158-208">Исправлена ошибка командлета Set-AzAutomationConnectionFieldValue при обработке строкового значения.</span><span class="sxs-lookup"><span data-stu-id="3d158-208">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3d158-209">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3d158-209">Az.Compute</span></span>
* <span data-ttu-id="3d158-210">В New AzImageConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="3d158-210">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3d158-211">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3d158-211">Az.DataFactory</span></span>
* <span data-ttu-id="3d158-212">Обновление выходных данных командлетов ADF, предназначенных для получения числа выполнений действий, конвейеров и триггеров, для поддержки канала Select-Object.</span><span class="sxs-lookup"><span data-stu-id="3d158-212">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="3d158-213">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="3d158-213">Az.EventGrid</span></span>
* <span data-ttu-id="3d158-214">Исправлена опечатка в документации по командлету New-AzEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="3d158-214">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3d158-215">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3d158-215">Az.IotHub</span></span>
* <span data-ttu-id="3d158-216">Добавлена поддержка повторного создания ключей политики авторизации.</span><span class="sxs-lookup"><span data-stu-id="3d158-216">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3d158-217">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3d158-217">Az.Network</span></span>
* <span data-ttu-id="3d158-218">К тегам общедоступного IP-адреса добавлен тег RoutingPreference.</span><span class="sxs-lookup"><span data-stu-id="3d158-218">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="3d158-219">Улучшены примеры для справочной документации по командлету Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="3d158-219">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="3d158-220">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="3d158-220">Az.PolicyInsights</span></span>
* <span data-ttu-id="3d158-221">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="3d158-221">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="3d158-222">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9446.</span><span class="sxs-lookup"><span data-stu-id="3d158-222">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="3d158-223">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3d158-223">Az.OperationalInsights</span></span>
* <span data-ttu-id="3d158-224">Исправленная модель источника данных CustomLog возвращена в командлет Get-AzOperationalInsightsDataSource.</span><span class="sxs-lookup"><span data-stu-id="3d158-224">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3d158-225">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3d158-225">Az.RecoveryServices</span></span>
* <span data-ttu-id="3d158-226">Выпущено исправление для команды get-policy для виртуальных машин IaaS.</span><span class="sxs-lookup"><span data-stu-id="3d158-226">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="3d158-227">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3d158-227">Az.Resources</span></span>
    - <span data-ttu-id="3d158-228">Исправлен текст справки по параметру Get-AzPolicyState -Top.</span><span class="sxs-lookup"><span data-stu-id="3d158-228">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="3d158-229">Добавлена поддержка разбиения по страницам на стороне клиента для Get-AzPolicyAlias.</span><span class="sxs-lookup"><span data-stu-id="3d158-229">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="3d158-230">Добавлены новые параметры для Set-AzPolicyAssignment, -PolicyParameters и -PolicyParametersObject.</span><span class="sxs-lookup"><span data-stu-id="3d158-230">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="3d158-231">Добавлен ряд обновлений документов и примеров для командлетов политик.</span><span class="sxs-lookup"><span data-stu-id="3d158-231">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="3d158-232">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3d158-232">Az.ServiceBus</span></span>
* <span data-ttu-id="3d158-233">Исправление ошибки № 4938: командлет New-AzureRmServiceBusQueue возвращает ответ BadRequest (Недопустимый запрос) при задании значения MaxSizeInMegabytes.</span><span class="sxs-lookup"><span data-stu-id="3d158-233">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="3d158-234">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3d158-234">Az.Sql</span></span>
* <span data-ttu-id="3d158-235">Из выпуска предварительной версии в выпуск общедоступной версии добавлены командлеты группы отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="3d158-235">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="3d158-236">Поддержка аудита Azure SQL Server и баз данных с помощью новых командлетов:</span><span class="sxs-lookup"><span data-stu-id="3d158-236">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="3d158-237">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="3d158-237">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="3d158-238">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="3d158-238">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="3d158-239">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="3d158-239">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="3d158-240">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="3d158-240">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="3d158-241">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="3d158-241">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="3d158-242">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="3d158-242">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="3d158-243">Из параметров оценки уязвимостей удалены ограничения, касающиеся электронной почты.</span><span class="sxs-lookup"><span data-stu-id="3d158-243">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3d158-244">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3d158-244">Az.Storage</span></span>
* <span data-ttu-id="3d158-245">Два параметра в указанном ниже командлете — -IndexDocument и -ErrorDocument404Path, — которые ранее были обязательными, стали необязательными:</span><span class="sxs-lookup"><span data-stu-id="3d158-245">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="3d158-246">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="3d158-246">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="3d158-247">Обновлена справка по командлету Get-AzStorageBlobContent: добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="3d158-247">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="3d158-248">При сбое выполнения командлета с ошибкой StorageException отображаются дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="3d158-248">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="3d158-249">Добавлена поддержка создания или обновления учетной записи хранения с использованием проверки подлинности AAD DS для службы "Файлы Azure".</span><span class="sxs-lookup"><span data-stu-id="3d158-249">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="3d158-250">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3d158-250">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="3d158-251">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3d158-251">Set-AzStorageAccount</span></span>
* <span data-ttu-id="3d158-252">Добавлена поддержка перечисления или закрытия дескрипторов файлов для общей папки, каталога файлов или файла:</span><span class="sxs-lookup"><span data-stu-id="3d158-252">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="3d158-253">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="3d158-253">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="3d158-254">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="3d158-254">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="3d158-255">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="3d158-255">Az.StorageSync</span></span>
* <span data-ttu-id="3d158-256">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="3d158-256">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="3d158-257">2.3.2 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="3d158-257">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3d158-258">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3d158-258">Az.Accounts</span></span>
* <span data-ttu-id="3d158-259">Исправлена ошибка, связанная с использованием неправильного URL-адреса для вызовов функций.</span><span class="sxs-lookup"><span data-stu-id="3d158-259">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="3d158-260">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8983.</span><span class="sxs-lookup"><span data-stu-id="3d158-260">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="3d158-261">Устранена проблема с псевдонимами из AzureRM для командлетов Az.</span><span class="sxs-lookup"><span data-stu-id="3d158-261">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="3d158-262">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="3d158-262">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="3d158-263">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest.</span><span class="sxs-lookup"><span data-stu-id="3d158-263">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3d158-264">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3d158-264">Az.Compute</span></span>
* <span data-ttu-id="3d158-265">Простые наборы параметров New-AzVm и New-AzVmss теперь принимают параметр ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="3d158-265">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="3d158-266">Исправлена опечатка в справочной документации по New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="3d158-266">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="3d158-267">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="3d158-267">Az.Dns</span></span>
* <span data-ttu-id="3d158-268">Исправлена опечатка в справочных примерах по использованию Set-AzDnsZone.</span><span class="sxs-lookup"><span data-stu-id="3d158-268">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="3d158-269">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="3d158-269">Az.EventGrid</span></span>
* <span data-ttu-id="3d158-270">Обновлен для использования API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="3d158-270">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="3d158-271">Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="3d158-271">New cmdlets:</span></span>
    - <span data-ttu-id="3d158-272">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="3d158-272">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="3d158-273">Создает домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="3d158-273">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="3d158-274">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="3d158-274">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="3d158-275">Возвращает сведения о домене Сетки событий или список всех доменов Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="3d158-275">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="3d158-276">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="3d158-276">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="3d158-277">Удаляет домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="3d158-277">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="3d158-278">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="3d158-278">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="3d158-279">Повторно создает ключ общего доступа для домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="3d158-279">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="3d158-280">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="3d158-280">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="3d158-281">Возвращает ключи общего доступа, используемые для публикации событий в домене Сетки событий.</span><span class="sxs-lookup"><span data-stu-id="3d158-281">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="3d158-282">New-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="3d158-282">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="3d158-283">Создает раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="3d158-283">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="3d158-284">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="3d158-284">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="3d158-285">Возвращает сведения о разделе домена Сетки событий или список всех разделов определенного домена Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="3d158-285">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="3d158-286">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="3d158-286">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="3d158-287">Удаляет раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="3d158-287">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="3d158-288">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="3d158-288">Updated cmdlets:</span></span>
    - <span data-ttu-id="3d158-289">New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="3d158-289">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="3d158-290">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для нового домена Сетки событий и раздела домена Сетки событий и позволяющие создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="3d158-290">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="3d158-291">Добавляют новые обязательные параметры для указания имени нового домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="3d158-291">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="3d158-292">Добавляют новые наборы параметров для доменов и разделов домена и позволяют повторно использовать существующие параметры (например, EndPointType, SubjectBeginsWith и т. д.).</span><span class="sxs-lookup"><span data-stu-id="3d158-292">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="3d158-293">Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="3d158-293">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="3d158-294">срока действия подписки на событие;</span><span class="sxs-lookup"><span data-stu-id="3d158-294">Event subscription expiration date,</span></span>
            - <span data-ttu-id="3d158-295">параметров расширенной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="3d158-295">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="3d158-296">Добавляют новое перечисление для ServiceBusQueue в качестве места назначения.</span><span class="sxs-lookup"><span data-stu-id="3d158-296">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="3d158-297">Запрещают использование значение All в параметре -IncludedEventType и заменяют его следующим:</span><span class="sxs-lookup"><span data-stu-id="3d158-297">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="3d158-298">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="3d158-298">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="3d158-299">Добавляют новые необязательные параметры (Top, ODataQuery и NextLink) для поддержки разбиения на страницы и фильтрации результатов.</span><span class="sxs-lookup"><span data-stu-id="3d158-299">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="3d158-300">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="3d158-300">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="3d158-301">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для домена Сетки событий и раздела домена Сетки событий и позволяющие удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="3d158-301">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="3d158-302">Добавляют новые обязательные параметры для указания имени домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="3d158-302">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="3d158-303">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="3d158-303">Az.FrontDoor</span></span>
* <span data-ttu-id="3d158-304">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="3d158-304">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="3d158-305">Добавляет поддержку преобразований и новое значение оператора автозавершения (RegEx).</span><span class="sxs-lookup"><span data-stu-id="3d158-305">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="3d158-306">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="3d158-306">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="3d158-307">Добавляет новые значения автозавершения.</span><span class="sxs-lookup"><span data-stu-id="3d158-307">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3d158-308">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3d158-308">Az.Network</span></span>
* <span data-ttu-id="3d158-309">Добавляет поддержку ресурса шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="3d158-309">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="3d158-310">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="3d158-310">New cmdlets</span></span>
        - <span data-ttu-id="3d158-311">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="3d158-311">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="3d158-312">Добавляет AvailablePrivateEndpointType.</span><span class="sxs-lookup"><span data-stu-id="3d158-312">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="3d158-313">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="3d158-313">New cmdlets</span></span> 
        - <span data-ttu-id="3d158-314">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="3d158-314">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="3d158-315">Добавляет PrivatePrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="3d158-315">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="3d158-316">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="3d158-316">New cmdlets</span></span> 
        - <span data-ttu-id="3d158-317">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="3d158-317">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="3d158-318">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="3d158-318">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="3d158-319">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="3d158-319">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="3d158-320">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3d158-320">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="3d158-321">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3d158-321">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="3d158-322">Добавляет PrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="3d158-322">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="3d158-323">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="3d158-323">New cmdlets</span></span>
        - <span data-ttu-id="3d158-324">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="3d158-324">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="3d158-325">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="3d158-325">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="3d158-326">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="3d158-326">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="3d158-327">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="3d158-327">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="3d158-328">Обновлены следующие команды для функции: флаг UseLocalAzureIpAddress для VPN-подключения.</span><span class="sxs-lookup"><span data-stu-id="3d158-328">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="3d158-329">Обновлен командлет New-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="3d158-329">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="3d158-330">Обновлен командлет Set-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="3d158-330">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="3d158-331">В пиринг ExpressRoute добавлено поле только для чтения PeeredConnections.</span><span class="sxs-lookup"><span data-stu-id="3d158-331">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="3d158-332">В ExpressRoute добавлено поле только для чтения GlobalReachEnabled.</span><span class="sxs-lookup"><span data-stu-id="3d158-332">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="3d158-333">Добавлен атрибут в рамках критического изменения, отменяющего статус устаревшего поля AllowGlobalReach в модели ExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="3d158-333">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="3d158-334">Исправлена проблема, связанная с ошибкой 8756, при использовании TargetListenerID с командлетами AzApplicationGatewayRedirectConfiguration.</span><span class="sxs-lookup"><span data-stu-id="3d158-334">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="3d158-335">Исправлена ошибка в New-AzApplicationGatewayPathRuleConfig, не позволявшая задавать набор правил повторного создания.</span><span class="sxs-lookup"><span data-stu-id="3d158-335">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="3d158-336">Исправлено отображение VirtualNetworkTaps в NetworkInterfaceIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="3d158-336">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="3d158-337">Исправлены командлеты Cortex Get для отображения всех частей.</span><span class="sxs-lookup"><span data-stu-id="3d158-337">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="3d158-338">Исправлено создание ссылок VirtualHub для ExpressRouteGateways и VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="3d158-338">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="3d158-339">В AzureFirewall и NatGateway добавлена поддержка Зон доступности.</span><span class="sxs-lookup"><span data-stu-id="3d158-339">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="3d158-340">Добавлен командлет Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="3d158-340">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="3d158-341">Добавлена поддержка нескольких общедоступных IP-адресов для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="3d158-341">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="3d158-342">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="3d158-342">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="3d158-343">Добавлен параметр -PublicIpAddress, который принимает один или несколько объектов общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="3d158-343">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="3d158-344">Добавлен параметр -VirtualNetwork, который принимает объект виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="3d158-344">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="3d158-345">Добавлены методы AddPublicIpAddress и RemovePublicIpAddress для объекта брандмауэра. Они принимают объект общедоступного IP-адреса в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="3d158-345">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="3d158-346">Не рекомендуется использовать параметры -PublicIpName и -VirtualNetworkName.</span><span class="sxs-lookup"><span data-stu-id="3d158-346">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="3d158-347">Обновлены следующие команды для функции: В параметрах проверки подлинности AAD VPN-клиента задан ресурс шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="3d158-347">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="3d158-348">Обновлен командлет New-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="3d158-348">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="3d158-349">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="3d158-349">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="3d158-350">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр-переключатель RemoveAadAuthentication для удаления в шлюзе параметров проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="3d158-350">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="3d158-351">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3d158-351">Az.OperationalInsights</span></span>
* <span data-ttu-id="3d158-352">Добавлена поддержка SKU **pergb2018** в команде New-AzureRmOperationalInsightsWorkspace.</span><span class="sxs-lookup"><span data-stu-id="3d158-352">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="3d158-353">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3d158-353">Az.Resources</span></span>
* <span data-ttu-id="3d158-354">Поддержка дополнительных вариантов экспорта шаблона.</span><span class="sxs-lookup"><span data-stu-id="3d158-354">Support for additional Template Export options</span></span>
    - <span data-ttu-id="3d158-355">В Export-AzResourceGroup добавлен параметр -SkipResourceNameParameterization.</span><span class="sxs-lookup"><span data-stu-id="3d158-355">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="3d158-356">В Export-AzResourceGroup добавлен параметр -SkipAllParameterization.</span><span class="sxs-lookup"><span data-stu-id="3d158-356">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="3d158-357">В Export-AzResourceGroup добавлен параметр -Resource для фильтрации экспортированных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3d158-357">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="3d158-358">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3d158-358">Az.ServiceFabric</span></span>
* <span data-ttu-id="3d158-359">Исправлена ошибка, связанная с получением иногда неправильных отпечатков при добавлении сертификата ByExistingKeyVault.</span><span class="sxs-lookup"><span data-stu-id="3d158-359">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="3d158-360">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3d158-360">Az.Sql</span></span>
* <span data-ttu-id="3d158-361">Исправлен суффикс конечной точки хранилища службы "Расширенная защита от угроз Azure".</span><span class="sxs-lookup"><span data-stu-id="3d158-361">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="3d158-362">Исправлена ошибка, связанная с возможностью пакета "Расширенная защита данных" переопределять политику службы "Расширенная защита от угроз".</span><span class="sxs-lookup"><span data-stu-id="3d158-362">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="3d158-363">Новые командлеты для Management.Sql позволяют клиентам добавлять ключи TDE и задавать средство защиты TDE для управляемых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="3d158-363">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="3d158-364">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3d158-364">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="3d158-365">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3d158-365">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="3d158-366">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3d158-366">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="3d158-367">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="3d158-367">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="3d158-368">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="3d158-368">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3d158-369">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3d158-369">Az.Storage</span></span>
* <span data-ttu-id="3d158-370">Поддержка класса Kind в FileStorage и значения Premium_ZRS в SkuName при создании учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="3d158-370">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="3d158-371">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3d158-371">New-AzStorageAccount</span></span>
* <span data-ttu-id="3d158-372">Уточнено описание командлета неизменности BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="3d158-372">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="3d158-373">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="3d158-373">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3d158-374">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3d158-374">Az.Websites</span></span>
* <span data-ttu-id="3d158-375">Оптимизирует Get-AzWebAppCertificate для фильтрации по группе ресурсов на сервере, а не в клиенте.</span><span class="sxs-lookup"><span data-stu-id="3d158-375">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="3d158-376">Добавляет параметр-переключатель - UseDisasterRecovery в Get AzWebAppSnapshot.</span><span class="sxs-lookup"><span data-stu-id="3d158-376">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="3d158-377">2.2.0 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="3d158-377">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="3d158-378">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="3d158-378">Az.Cdn</span></span>
* <span data-ttu-id="3d158-379">Обновлены командлеты для поддержки функции rulesEngine на основе API версии 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="3d158-379">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3d158-380">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3d158-380">Az.Compute</span></span>
* <span data-ttu-id="3d158-381">Добавлен параметр `NoWait`, который запускает операцию и немедленно возвращает значение еще до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="3d158-381">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="3d158-382">Обновлены командлеты:   Export-AzLogAnalyticRequestRateByInterval; Export-AzLogAnalyticThrottledRequest; Remove-AzVM; Remove-AzVMAccessExtension; Remove-AzVMAEMExtension; Remove-AzVMChefExtension; Remove-AzVMCustomScriptExtension; Remove-AzVMDiagnosticsExtension; Remove-AzVMDiskEncryptionExtension; Remove-AzVMDscExtension; Remove-AzVMSqlServerExtension; Restart-AzVM; Set-AzVM; Set-AzVMAccessExtension; Set-AzVMADDomainExtension; Set-AzVMAEMExtension; Set-AzVMBginfoExtension; Set-AzVMChefExtension; Set-AzVMCustomScriptExtension; Set-AzVMDiagnosticsExtension; Set-AzVMDscExtension; Set-AzVMExtension; Start-AzVM; Stop-AzVM; Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="3d158-382">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="3d158-383">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="3d158-383">Az.EventHub</span></span>
* <span data-ttu-id="3d158-384">Исправлена ошибка № 9231. Командлет Get-AzEventHubNamespace не возвращал теги.</span><span class="sxs-lookup"><span data-stu-id="3d158-384">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="3d158-385">Исправлена ошибка № 9230. Командлет Get-AzEventHubNamespace возвращал значение ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="3d158-385">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3d158-386">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3d158-386">Az.Network</span></span>
* <span data-ttu-id="3d158-387">Обновлены параметры ResourceId и InputObject для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="3d158-387">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="3d158-388">Добавлены псевдонимы для параметров ResourceId и InputObject.</span><span class="sxs-lookup"><span data-stu-id="3d158-388">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="3d158-389">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="3d158-389">Az.PolicyInsights</span></span>
* <span data-ttu-id="3d158-390">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyEvent.</span><span class="sxs-lookup"><span data-stu-id="3d158-390">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3d158-391">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3d158-391">Az.RecoveryServices</span></span>
* <span data-ttu-id="3d158-392">Минимальный срок хранения политики IaaSVM изменился с 1 до 7 дней.</span><span class="sxs-lookup"><span data-stu-id="3d158-392">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="3d158-393">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3d158-393">Az.ServiceBus</span></span>
* <span data-ttu-id="3d158-394">Исправлена ошибка № 9182. Командлет Get-AzServiceBusNamespace возвращал ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="3d158-394">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="3d158-395">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3d158-395">Az.ServiceFabric</span></span>
* <span data-ttu-id="3d158-396">Исправлена опечатка в сообщении об ошибке для командлета Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="3d158-396">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="3d158-397">Исправлен отсутствующей символ в командных строках Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="3d158-397">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="3d158-398">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3d158-398">Az.Sql</span></span>
* <span data-ttu-id="3d158-399">Для командлета New-AzureSqlInstance добавлен параметр DnsZonePartner, обеспечивающий поддержку AutoDr для Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="3d158-399">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="3d158-400">Командлет Get-AzSqlDatabaseSecureConnectionPolicy объявлен неподдерживаемым.</span><span class="sxs-lookup"><span data-stu-id="3d158-400">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="3d158-401">Командлеты обнаружения угроз переименованы в командлеты Расширенной защиты от угроз.</span><span class="sxs-lookup"><span data-stu-id="3d158-401">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="3d158-402">Параметры -StorageSizeInGB и -LicenseType командлета New-AzSqlInstance теперь необязательны.</span><span class="sxs-lookup"><span data-stu-id="3d158-402">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3d158-403">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3d158-403">Az.Websites</span></span>
* <span data-ttu-id="3d158-404">Исправлены проблемы, когда удалялись теги при использовании Set-AzWebApp и Set-AzWebAppSlot со свойством -WebApp.</span><span class="sxs-lookup"><span data-stu-id="3d158-404">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="3d158-405">2.1.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="3d158-405">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="3d158-406">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3d158-406">Az.ApiManagement</span></span>
* <span data-ttu-id="3d158-407">Созданы командлеты для управления диагностикой в глобальной области и в области API.</span><span class="sxs-lookup"><span data-stu-id="3d158-407">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="3d158-408">**Get-AzApiManagementDiagnostic** — получение диагностики, заданной глобально или на уровне области API.</span><span class="sxs-lookup"><span data-stu-id="3d158-408">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="3d158-409">**New-AzApiManagementDiagnostic** — создание диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="3d158-409">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="3d158-410">**New-AzApiManagementHttpMessageDiagnostic** — создание параметра диагностики, для которого регистрируются заголовки и размер байтов тела.</span><span class="sxs-lookup"><span data-stu-id="3d158-410">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="3d158-411">**New-AzApiManagementPipelineDiagnosticSetting** — создание параметров диагностики для сообщений HTTP, поступающих в шлюз или исходящих из него.</span><span class="sxs-lookup"><span data-stu-id="3d158-411">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="3d158-412">**New-AzApiManagementSamplingSetting** — создание параметра выборки для запросов и ответов касательно диагностики.</span><span class="sxs-lookup"><span data-stu-id="3d158-412">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="3d158-413">**Remove-AzApiManagementDiagnostic** — удаление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="3d158-413">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="3d158-414">**Set-AzApiManagementDiagnostic** — обновление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="3d158-414">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="3d158-415">Созданы командлеты для управления кэшем в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="3d158-415">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="3d158-416">**Get-AzApiManagementCache** — получение сведений о кэше, указанном идентификатором, или обо всех кэшах.</span><span class="sxs-lookup"><span data-stu-id="3d158-416">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="3d158-417">**New-AzApiManagementCache** — создание кэша по умолчанию или кэша в определенном регионе Azure.</span><span class="sxs-lookup"><span data-stu-id="3d158-417">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="3d158-418">**Remove-AzApiManagementCache** — удаление кэша.</span><span class="sxs-lookup"><span data-stu-id="3d158-418">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="3d158-419">**Update-AzApiManagementCache** — обновление кэша.</span><span class="sxs-lookup"><span data-stu-id="3d158-419">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="3d158-420">Созданы командлеты для управления схемой API.</span><span class="sxs-lookup"><span data-stu-id="3d158-420">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="3d158-421">**New-AzApiManagementSchema** — создание схемы для API.</span><span class="sxs-lookup"><span data-stu-id="3d158-421">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="3d158-422">**Get-AzApiManagementSchema** — получение схем, настроенных в API.</span><span class="sxs-lookup"><span data-stu-id="3d158-422">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="3d158-423">**Remove-AzApiManagementSchema** — удаление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="3d158-423">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="3d158-424">**Set-AzApiManagementSchema** — обновление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="3d158-424">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="3d158-425">Создан командлет для создания токена пользователя.</span><span class="sxs-lookup"><span data-stu-id="3d158-425">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="3d158-426">**New-AzApiManagementUserToken** — создание токена пользователя, по умолчанию действительного в течение 8 часов. С помощью этого командлета можно создавать токен для пользователя GIT.</span><span class="sxs-lookup"><span data-stu-id="3d158-426">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="3d158-427">Создан командлет для получения состояния сети.</span><span class="sxs-lookup"><span data-stu-id="3d158-427">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="3d158-428">**Get-AzApiManagementNetworkStatus** — получение состояния сети ресурсов, от которых зависит служба "Управление API".</span><span class="sxs-lookup"><span data-stu-id="3d158-428">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="3d158-429">Это полезно при развертывании службы ApiManagement в виртуальной сети и проверке того, не нарушена ли какая-либо из зависимостей.</span><span class="sxs-lookup"><span data-stu-id="3d158-429">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="3d158-430">Обновлен командлет **New-AzApiManagement** для управления службой ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="3d158-430">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="3d158-431">Добавлена поддержка нового SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="3d158-431">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="3d158-432">Добавлена поддержка для включения флага EnableClientCertificate в SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="3d158-432">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="3d158-433">Новый командлет **New-AzApiManagementSslSetting** позволяет настраивать параметр TLS/SSL для сервера (Backend) и внешнего интерфейса (Frontend).</span><span class="sxs-lookup"><span data-stu-id="3d158-433">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="3d158-434">Его также можно использовать для настройки Ciphers как 3DES, в ServerProtocols как Http2 для внешнего интерфейса (Frontend) службы ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="3d158-434">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="3d158-435">Добавлена поддержка настройки имени узла DeveloperPortal в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="3d158-435">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="3d158-436">Обновлен командлет **Get-AzApiManagementSsoToken** для извлечения объекта PsApiManagement в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="3d158-436">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="3d158-437">Обновлен командлет для отображения встроенных сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="3d158-437">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="3d158-438">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Код ошибки: ValidationError. Сообщение об ошибке: "Некоторые поля содержат неправильные значения". Сведения об ошибке: [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="3d158-438">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="3d158-439">Обновлен командлет **Export-AzApiManagementApi** для экспортирования программных интерфейсов в формате OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="3d158-439">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="3d158-440">Обновлен командлет **Import-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="3d158-440">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="3d158-441">Для импортирования API из спецификации документа OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="3d158-441">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="3d158-442">Для переопределения свойства PsApiManagementSchema, указанного в любом документе (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="3d158-442">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="3d158-443">Для переопределения свойства ServiceUrl, указанного в любом документе.</span><span class="sxs-lookup"><span data-stu-id="3d158-443">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="3d158-444">Обновлен командлет **Get-AzApiManagementPolicy** для возврата политики в формате, экранированном не для XML, с использованием rawxml.</span><span class="sxs-lookup"><span data-stu-id="3d158-444">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="3d158-445">Обновлен командлет **Set-AzApiManagementPolicy**. Он принимает политику в формате, экранированном не для XML, с использованием rawxml и в формате, экранированном для XML, с использованием XML.</span><span class="sxs-lookup"><span data-stu-id="3d158-445">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="3d158-446">Обновлен командлет **New-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="3d158-446">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="3d158-447">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="3d158-447">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="3d158-448">Для создания API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="3d158-448">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="3d158-449">Для клонирования API с использованием значений SourceApiId и SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="3d158-449">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="3d158-450">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="3d158-450">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="3d158-451">Обновлен командлет **Set-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="3d158-451">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="3d158-452">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="3d158-452">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="3d158-453">Для обновления API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="3d158-453">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="3d158-454">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="3d158-454">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="3d158-455">Обновлен командлет **New-AzApiManagementRevision**:</span><span class="sxs-lookup"><span data-stu-id="3d158-455">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="3d158-456">Для клонирования (копирования тегов, продуктов, операций и политик) существующей редакции с использованием SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="3d158-456">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="3d158-457">Новая редакция предполагает родительский идентификатор ApiId.</span><span class="sxs-lookup"><span data-stu-id="3d158-457">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="3d158-458">Для предоставления ApiRevisionDescription.</span><span class="sxs-lookup"><span data-stu-id="3d158-458">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="3d158-459">Для переопределения значения ServiceUrl при клонировании API.</span><span class="sxs-lookup"><span data-stu-id="3d158-459">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="3d158-460">Обновлен командлет **New-AzApiManagementIdentityProvider**:</span><span class="sxs-lookup"><span data-stu-id="3d158-460">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="3d158-461">Для настройки AAD или AADB2C с Authority.</span><span class="sxs-lookup"><span data-stu-id="3d158-461">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="3d158-462">Для установки политик SignupPolicy, SigninPolicy, ProfileEditingPolicy и PasswordResetPolicy.</span><span class="sxs-lookup"><span data-stu-id="3d158-462">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="3d158-463">Обновлен командлет **New-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="3d158-463">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="3d158-464">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="3d158-464">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="3d158-465">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="3d158-465">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="3d158-466">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="3d158-466">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="3d158-467">Обновлен командлет **Set-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="3d158-467">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="3d158-468">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="3d158-468">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="3d158-469">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="3d158-469">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="3d158-470">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="3d158-470">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="3d158-471">Следующие командлеты обновлены, чтобы принимать значение ResourceId в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="3d158-471">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="3d158-472">New-AzApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="3d158-472">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="3d158-473">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="3d158-473">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="3d158-474">Get-AzApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="3d158-474">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="3d158-475">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="3d158-475">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="3d158-476">Get-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="3d158-476">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="3d158-477">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="3d158-477">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="3d158-478">Get-AzApiManagementAuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="3d158-478">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="3d158-479">Get-AzApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="3d158-479">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="3d158-480">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="3d158-480">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="3d158-481">Get-AzApiManagementCertificate.</span><span class="sxs-lookup"><span data-stu-id="3d158-481">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="3d158-482">Remove-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="3d158-482">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="3d158-483">Remove-AzApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="3d158-483">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3d158-484">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3d158-484">Az.Automation</span></span>
* <span data-ttu-id="3d158-485">Обновлен командлет Get-AzAutomationJobOutputRecord для обработки значений в формате JSON и в виде текстовой записи.</span><span class="sxs-lookup"><span data-stu-id="3d158-485">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="3d158-486">исправлена проблема https://github.com/Azure/azure-powershell/issues/7977.</span><span class="sxs-lookup"><span data-stu-id="3d158-486">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="3d158-487">исправлена проблема https://github.com/Azure/azure-powershell/issues/8600.</span><span class="sxs-lookup"><span data-stu-id="3d158-487">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="3d158-488">Поведение командлета Start-AzAutomationDscCompilationJob изменено так, чтобы сразу же запустить задание, а не ждать его завершения.</span><span class="sxs-lookup"><span data-stu-id="3d158-488">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="3d158-489">исправлена проблема https://github.com/Azure/azure-powershell/issues/8347.</span><span class="sxs-lookup"><span data-stu-id="3d158-489">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="3d158-490">Исправлен командлет Get-AzAutomationDscNode, возвращающий все узлы при использовании -Name.</span><span class="sxs-lookup"><span data-stu-id="3d158-490">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="3d158-491">Теперь он возвращает только соответствующий узел.</span><span class="sxs-lookup"><span data-stu-id="3d158-491">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3d158-492">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3d158-492">Az.Compute</span></span>
* <span data-ttu-id="3d158-493">Добавлены параметры ProtectFromScaleIn и ProtectFromScaleSetAction для командлета Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="3d158-493">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="3d158-494">Командлет New-AzVM с простым набором параметров теперь по умолчанию использует доступное расположение, если регион "восточная часть США" не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3d158-494">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3d158-495">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3d158-495">Az.DataLakeStore</span></span>
* <span data-ttu-id="3d158-496">Обновлен пакет SDK ADLS для использования httpclient. В инфраструктуру Azure интегрирована проверка плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="3d158-496">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3d158-497">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3d158-497">Az.Monitor</span></span>
* <span data-ttu-id="3d158-498">Исправлены неправильные имена параметров в справочных примерах.</span><span class="sxs-lookup"><span data-stu-id="3d158-498">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3d158-499">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3d158-499">Az.Network</span></span>
* <span data-ttu-id="3d158-500">Добавлен флаг DisableBgpRoutePropagation для выходных данных действующей таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="3d158-500">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="3d158-501">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="3d158-501">Updated cmdlet:</span></span>
        - <span data-ttu-id="3d158-502">Get-AzEffectiveRouteTable.</span><span class="sxs-lookup"><span data-stu-id="3d158-502">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="3d158-503">Исправлен двойной дефис в документации New-AzApplicationGatewayTrustedRootCertificate.</span><span class="sxs-lookup"><span data-stu-id="3d158-503">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="3d158-504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3d158-504">Az.Resources</span></span>
* <span data-ttu-id="3d158-505">Добавлен новый командлет Get-AzureRmDenyAssignment для получения запрещающих назначений.</span><span class="sxs-lookup"><span data-stu-id="3d158-505">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="3d158-506">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3d158-506">Az.Sql</span></span>
* <span data-ttu-id="3d158-507">Командлеты Расширенной защиты от угроз переименованы на командлеты Расширенной защиты данных, и оценка уязвимости включена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3d158-507">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="3d158-508">2.0.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="3d158-508">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3d158-509">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3d158-509">Az.Accounts</span></span>
* <span data-ttu-id="3d158-510">Обновлена библиотека аутентификации для устранения проблем с ADFS при использовании аутентификации на основе имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="3d158-510">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="3d158-511">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3d158-511">Az.CognitiveServices</span></span>
* <span data-ttu-id="3d158-512">Отображается только заявление об отказе Bing для служб Поиска Bing.</span><span class="sxs-lookup"><span data-stu-id="3d158-512">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="3d158-513">Исправлена проблема с созданием учетной записи.</span><span class="sxs-lookup"><span data-stu-id="3d158-513">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3d158-514">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3d158-514">Az.Compute</span></span>
* <span data-ttu-id="3d158-515">Функция группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="3d158-515">Proximity placement group feature.</span></span>
    - <span data-ttu-id="3d158-516">Добавлены следующие новые командлеты:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="3d158-516">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="3d158-517">Новый параметр ProximityPlacementGroupId будет добавлен в следующие командлеты:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="3d158-517">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="3d158-518">В командлет New-AzGalleryImageVersion добавлен параметр StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="3d158-518">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="3d158-519">TargetRegion в командлете New-AzGalleryImageVersion может содержать StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="3d158-519">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="3d158-520">Параметр-переключатель SkipShutdown добавлен в командлеты Stop-AzVM и Stop-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="3d158-520">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="3d158-521">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="3d158-521">Breaking changes</span></span>
    - <span data-ttu-id="3d158-522">Командлет SET-AzVMBootDiagnostics изменен на Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="3d158-522">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="3d158-523">Командлет Export-AzLogAnalyticThrottledRequests изменен на Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="3d158-523">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="3d158-524">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="3d158-524">Az.DeploymentManager</span></span>
* <span data-ttu-id="3d158-525">Первая общедоступная версия командлетов диспетчера развертывания Azure</span><span class="sxs-lookup"><span data-stu-id="3d158-525">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="3d158-526">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="3d158-526">Az.Dns</span></span>
* <span data-ttu-id="3d158-527">Автоматическое делегирование DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="3d158-527">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="3d158-528">Командлет для создания зоны DNS принимает имя родительской зоны в качестве дополнительного необязательного параметра.</span><span class="sxs-lookup"><span data-stu-id="3d158-528">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="3d158-529">Он добавляет записи NS в родительской зоне для созданной дочерней зоны.</span><span class="sxs-lookup"><span data-stu-id="3d158-529">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="3d158-530">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="3d158-530">Az.FrontDoor</span></span>
* <span data-ttu-id="3d158-531">Первая общедоступная версия командлетов Azure FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="3d158-531">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="3d158-532">Переименованы командлеты WAF для включения Waf.</span><span class="sxs-lookup"><span data-stu-id="3d158-532">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="3d158-533">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="3d158-533">Az.HDInsight</span></span>
* <span data-ttu-id="3d158-534">Удалены два командлета:</span><span class="sxs-lookup"><span data-stu-id="3d158-534">Removed two cmdlets:</span></span>
    - <span data-ttu-id="3d158-535">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="3d158-535">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="3d158-536">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="3d158-536">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="3d158-537">Добавлен новый командлет Set-AzHDInsightGatewayCredential для замены Grant-AzHDInsightHttpServicesAccess.</span><span class="sxs-lookup"><span data-stu-id="3d158-537">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="3d158-538">Обновлен командлет Get-AzHDInsightJobOutput для различения ролей читателя и оператора HDInsight:</span><span class="sxs-lookup"><span data-stu-id="3d158-538">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="3d158-539">Пользователям с ролью читателя не нужно указывать параметр DefaultStorageAccountKey явным образом, иначе возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="3d158-539">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="3d158-540">На пользователей с ролью оператора HDInsight это не повлияет.</span><span class="sxs-lookup"><span data-stu-id="3d158-540">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3d158-541">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3d158-541">Az.Monitor</span></span>
* <span data-ttu-id="3d158-542">Новые командлеты для API SQR (запланированное правило запросов)</span><span class="sxs-lookup"><span data-stu-id="3d158-542">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="3d158-543">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="3d158-543">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="3d158-544">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="3d158-544">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="3d158-545">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="3d158-545">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="3d158-546">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="3d158-546">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="3d158-547">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="3d158-547">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="3d158-548">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="3d158-548">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="3d158-549">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="3d158-549">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="3d158-550">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="3d158-550">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="3d158-551">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="3d158-551">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="3d158-552">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="3d158-552">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="3d158-553">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="3d158-553">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="3d158-554">См. подробнее об [API SQR](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules).</span><span class="sxs-lookup"><span data-stu-id="3d158-554">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="3d158-555">Обновлен файл Az.Monitor.md для включения командлетов для правила генерации оповещений на основе метрик GenV2(не классическая версия).</span><span class="sxs-lookup"><span data-stu-id="3d158-555">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3d158-556">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3d158-556">Az.Network</span></span>
* <span data-ttu-id="3d158-557">Добавлена поддержка для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="3d158-557">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="3d158-558">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="3d158-558">New cmdlets</span></span>
        - <span data-ttu-id="3d158-559">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="3d158-559">New-AzNatGateway</span></span>
        - <span data-ttu-id="3d158-560">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="3d158-560">Get-AzNatGateway</span></span>
        - <span data-ttu-id="3d158-561">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="3d158-561">Set-AzNatGateway</span></span>
        - <span data-ttu-id="3d158-562">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="3d158-562">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="3d158-563">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="3d158-563">Updated cmdlets</span></span>
        - <span data-ttu-id="3d158-564">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="3d158-564">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="3d158-565">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="3d158-565">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="3d158-566">Обновлены следующие команды для функции: Настройка и удаление пользовательских маршрутов через шлюз в Бруклине.</span><span class="sxs-lookup"><span data-stu-id="3d158-566">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="3d158-567">Обновлен командлет New-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="3d158-567">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="3d158-568">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="3d158-568">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="3d158-569">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="3d158-569">Az.PolicyInsights</span></span>
* <span data-ttu-id="3d158-570">Добавлена поддержка сведений об оценке политики запросов.</span><span class="sxs-lookup"><span data-stu-id="3d158-570">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="3d158-571">Добавлен параметр -Expand в командлет Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="3d158-571">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="3d158-572">Добавлена поддержка -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="3d158-572">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3d158-573">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3d158-573">Az.RecoveryServices</span></span>
* <span data-ttu-id="3d158-574">Добавлена поддержка перекрестной подписки на Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="3d158-574">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="3d158-575">Добавлена возможность отмечать предстоящие критически важные изменения для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="3d158-575">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="3d158-576">Исправлены план восстановления и план действий для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="3d158-576">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="3d158-577">Исправлено сетевое сопоставление обновления Azure Site Recovery (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="3d158-577">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="3d158-578">Исправлено направление защиты обновления Azure Site Recovery для управляемых дисков (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="3d158-578">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="3d158-579">Добавлены другие незначительные исправления.</span><span class="sxs-lookup"><span data-stu-id="3d158-579">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="3d158-580">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="3d158-580">Az.Relay</span></span>
* <span data-ttu-id="3d158-581">Исправлены опечатки в сообщениях для клиентов.</span><span class="sxs-lookup"><span data-stu-id="3d158-581">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="3d158-582">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3d158-582">Az.ServiceBus</span></span>
* <span data-ttu-id="3d158-583">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="3d158-583">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3d158-584">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3d158-584">Az.Storage</span></span>
* <span data-ttu-id="3d158-585">Выполнено обновление клиентской библиотеки хранилища до версии 10.0.1 (пространство имен всех объектов из этого пакета SDK изменено с Microsoft.WindowsAzure.Storage. *на Microsoft.Azure.Storage*).</span><span class="sxs-lookup"><span data-stu-id="3d158-585">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="3d158-586">Выполнено обновление до Microsoft.Azure.Management.Storage версии 11.0.0 для включения поддержки нового API версии 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="3d158-586">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="3d158-587">Значение свойства Kind по умолчанию в учетной записи хранения изменено со Storage на StorageV2.</span><span class="sxs-lookup"><span data-stu-id="3d158-587">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="3d158-588">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3d158-588">New-AzStorageAccount</span></span>
* <span data-ttu-id="3d158-589">Изменено значение Sku.Name в выходных данных командлета учетной записи хранения в соответствии со значением Sku.Name во входных данных путем добавления _ (например, StandardLRS изменено на Standard_LRS).</span><span class="sxs-lookup"><span data-stu-id="3d158-589">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="3d158-590">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3d158-590">New-AzStorageAccount</span></span>
    - <span data-ttu-id="3d158-591">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3d158-591">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="3d158-592">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3d158-592">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3d158-593">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3d158-593">Az.Websites</span></span>
* <span data-ttu-id="3d158-594">Свойство Kind теперь будет задаваться объектам PSSite, возвращаемым командлетом Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="3d158-594">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="3d158-595">Get-AzWebApp\*Metrics и Get-AzAppServicePlanMetrics считаются нерекомендуемыми.</span><span class="sxs-lookup"><span data-stu-id="3d158-595">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="3d158-596">1.8.0 — апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="3d158-596">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="3d158-597">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="3d158-597">Highlights since the last major release</span></span>
* <span data-ttu-id="3d158-598">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="3d158-598">General availability of `Az` module</span></span>
* <span data-ttu-id="3d158-599">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="3d158-599">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="3d158-600">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="3d158-600">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="3d158-601">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="3d158-601">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="3d158-602">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="3d158-602">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="3d158-603">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="3d158-603">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="3d158-604">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="3d158-604">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="3d158-605">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3d158-605">Az.Accounts</span></span>
* <span data-ttu-id="3d158-606">Обновлен командлет Uninstall-AzureRm для правильного удаления модулей в Mac.</span><span class="sxs-lookup"><span data-stu-id="3d158-606">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="3d158-607">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="3d158-607">Az.Batch</span></span>
* <span data-ttu-id="3d158-608">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="3d158-608">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="3d158-609">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="3d158-609">Az.Cdn</span></span>
* <span data-ttu-id="3d158-610">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="3d158-610">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="3d158-611">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3d158-611">Az.CognitiveServices</span></span>
* <span data-ttu-id="3d158-612">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="3d158-612">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3d158-613">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3d158-613">Az.Compute</span></span>
* <span data-ttu-id="3d158-614">Устранена проблема с установкой AEM, если в идентификаторах ресурсов дисков группа ресурсов указана в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="3d158-614">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="3d158-615">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="3d158-615">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="3d158-616">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="3d158-616">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3d158-617">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3d158-617">Az.DataFactory</span></span>
* <span data-ttu-id="3d158-618">Добавлены свойства SsisProperties, если NodeCount не имеет значения NULL для управляемой среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="3d158-618">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3d158-619">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3d158-619">Az.DataLakeStore</span></span>
* <span data-ttu-id="3d158-620">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="3d158-620">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="3d158-621">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="3d158-621">Az.EventGrid</span></span>
* <span data-ttu-id="3d158-622">Обновлен текст справки для конечной точки, указывающий, что необходимо создать ресурсы, прежде чем использовать командлеты для создания или обновления подписки на события.</span><span class="sxs-lookup"><span data-stu-id="3d158-622">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="3d158-623">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="3d158-623">Az.EventHub</span></span>
* <span data-ttu-id="3d158-624">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="3d158-624">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="3d158-625">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="3d158-625">Az.HDInsight</span></span>
* <span data-ttu-id="3d158-626">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="3d158-626">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3d158-627">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3d158-627">Az.IotHub</span></span>
* <span data-ttu-id="3d158-628">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="3d158-628">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="3d158-629">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3d158-629">Az.KeyVault</span></span>
* <span data-ttu-id="3d158-630">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="3d158-630">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="3d158-631">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="3d158-631">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="3d158-632">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="3d158-632">Az.MachineLearning</span></span>
* <span data-ttu-id="3d158-633">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="3d158-633">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="3d158-634">Az.Media</span><span class="sxs-lookup"><span data-stu-id="3d158-634">Az.Media</span></span>
* <span data-ttu-id="3d158-635">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="3d158-635">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3d158-636">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3d158-636">Az.Monitor</span></span>
  * <span data-ttu-id="3d158-637">Добавлены новые командлеты для правила генерации оповещений на основе метрик GenV2 (не классических).</span><span class="sxs-lookup"><span data-stu-id="3d158-637">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="3d158-638">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="3d158-638">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="3d158-639">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="3d158-639">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="3d158-640">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="3d158-640">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="3d158-641">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="3d158-641">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="3d158-642">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="3d158-642">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="3d158-643">Обновлен пакет SDK Monitor до предварительной версии 0.22.0.</span><span class="sxs-lookup"><span data-stu-id="3d158-643">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3d158-644">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3d158-644">Az.Network</span></span>
* <span data-ttu-id="3d158-645">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="3d158-645">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="3d158-646">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="3d158-646">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="3d158-647">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="3d158-647">Az.NotificationHubs</span></span>
* <span data-ttu-id="3d158-648">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="3d158-648">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="3d158-649">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3d158-649">Az.OperationalInsights</span></span>
* <span data-ttu-id="3d158-650">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="3d158-650">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="3d158-651">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="3d158-651">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="3d158-652">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="3d158-652">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3d158-653">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3d158-653">Az.RecoveryServices</span></span>
* <span data-ttu-id="3d158-654">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="3d158-654">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="3d158-655">Обновлен табличный формат для SQL на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="3d158-655">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="3d158-656">Добавлен альтернативный метод для получения расположения в Общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="3d158-656">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="3d158-657">Обновлено значение ScheduleRunDays в объекте SchedulePolicy в соответствии с часовым поясом.</span><span class="sxs-lookup"><span data-stu-id="3d158-657">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="3d158-658">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="3d158-658">Az.RedisCache</span></span>
* <span data-ttu-id="3d158-659">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="3d158-659">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3d158-660">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3d158-660">Az.Resources</span></span>
* <span data-ttu-id="3d158-661">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="3d158-661">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="3d158-662">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3d158-662">Az.Sql</span></span>
* <span data-ttu-id="3d158-663">Заменена зависимость от пакета SDK монитора на обычный код.</span><span class="sxs-lookup"><span data-stu-id="3d158-663">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="3d158-664">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="3d158-664">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="3d158-665">Улучшен процесс классификации нескольких столбцов.</span><span class="sxs-lookup"><span data-stu-id="3d158-665">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="3d158-666">Добавлены свойства SKU (имя, семейство, производительность SKU) в отклике Get-AzSqlServerServiceObjective, а также по умолчанию задан табличный формат.</span><span class="sxs-lookup"><span data-stu-id="3d158-666">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="3d158-667">C помощью Get-AzSqlServerServiceObjective теперь можно получать список доступных целевых служб по расположению без необходимости заранее размещать сервер в регионе.</span><span class="sxs-lookup"><span data-stu-id="3d158-667">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="3d158-668">Поддерживается параметр часового пояса при создании Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="3d158-668">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="3d158-669">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="3d158-669">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3d158-670">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3d158-670">Az.Websites</span></span>
* <span data-ttu-id="3d158-671">Исправлены командлеты Set-AzWebApp и Set-AzWebAppSlot, которые теперь не удаляют теги при выполнении.</span><span class="sxs-lookup"><span data-stu-id="3d158-671">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="3d158-672">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="3d158-672">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="3d158-673">Обновлен пакет SDK веб-узлов.</span><span class="sxs-lookup"><span data-stu-id="3d158-673">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="3d158-674">Удалено свойство AdminSiteName из PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="3d158-674">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="3d158-675">1.7.0 —апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="3d158-675">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="3d158-676">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="3d158-676">Highlights since the last major release</span></span>
* <span data-ttu-id="3d158-677">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="3d158-677">General availability of `Az` module</span></span>
* <span data-ttu-id="3d158-678">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="3d158-678">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="3d158-679">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="3d158-679">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="3d158-680">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="3d158-680">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="3d158-681">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="3d158-681">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="3d158-682">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="3d158-682">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="3d158-683">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="3d158-683">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="3d158-684">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3d158-684">Az.Accounts</span></span>
* <span data-ttu-id="3d158-685">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметр AzureAnalysisServicesEndpointResourceId.</span><span class="sxs-lookup"><span data-stu-id="3d158-685">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="3d158-686">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3d158-686">Az.AnalysisServices</span></span>
* <span data-ttu-id="3d158-687">Использование ServiceClient в командлетах плоскости данных и удаление исходной логики проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="3d158-687">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="3d158-688">Add-AzureASAccount используется как оболочка для Connect-AzAccount во избежание критических изменений.</span><span class="sxs-lookup"><span data-stu-id="3d158-688">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3d158-689">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3d158-689">Az.Automation</span></span>
* <span data-ttu-id="3d158-690">Исправлена ошибка командлета New-AzAutomationSoftwareUpdateConfiguration, связанная с включением.</span><span class="sxs-lookup"><span data-stu-id="3d158-690">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="3d158-691">Теперь параметры IncludedKbNumber и IncludedPackageNameMask должны работать нормально.</span><span class="sxs-lookup"><span data-stu-id="3d158-691">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="3d158-692">Исправлена ошибка динамической группы управления обновлениями службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="3d158-692">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3d158-693">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3d158-693">Az.Compute</span></span>
* <span data-ttu-id="3d158-694">В командлеты New-AzDiskConfig и New-AzSnapshotConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="3d158-694">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="3d158-695">Теперь можно создавать виртуальные машину на основе образов из коллекции от других клиентов.</span><span class="sxs-lookup"><span data-stu-id="3d158-695">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="3d158-696">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="3d158-696">Az.ContainerInstance</span></span>
* <span data-ttu-id="3d158-697">Исправлена проблема в параметре -Command командлета New-AzContainerGroup, из-за которой в конце добавлялся пустой аргумент.</span><span class="sxs-lookup"><span data-stu-id="3d158-697">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3d158-698">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3d158-698">Az.DataFactory</span></span>
* <span data-ttu-id="3d158-699">Пакет SDK для ADF .NET обновлен до версии 3.0.2.</span><span class="sxs-lookup"><span data-stu-id="3d158-699">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="3d158-700">Командлет Set-AzDataFactoryV2 обновлен с помощью дополнительных параметров для настроек, связанных с RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="3d158-700">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3d158-701">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3d158-701">Az.Resources</span></span>
* <span data-ttu-id="3d158-702">Улучшена обработка поставщиков Get-AzResource при предоставлении параметров -ResourceId или -ResourceGroupName, -Name и -ResourceType.</span><span class="sxs-lookup"><span data-stu-id="3d158-702">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="3d158-703">Улучшена обработка ошибок в командлетах Test-AzDeployment и Test-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="3d158-703">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="3d158-704">Теперь ошибки, возникающие за пределами проверки развертывания, обрабатываются и включаются в выходные данные команды.</span><span class="sxs-lookup"><span data-stu-id="3d158-704">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="3d158-705">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="3d158-705">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="3d158-706">Добавлен параметр-переключатель -IgnoreDynamicParameters, с помощью которого можно настроить командлеты развертывания так, чтобы они пропускали запросы в сценариях скриптов и заданий.</span><span class="sxs-lookup"><span data-stu-id="3d158-706">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="3d158-707">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="3d158-707">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="3d158-708">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3d158-708">Az.Sql</span></span>
* <span data-ttu-id="3d158-709">Поддержка классификации данных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="3d158-709">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3d158-710">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3d158-710">Az.Storage</span></span>
* <span data-ttu-id="3d158-711">Подробные сообщения об ошибке передаются при создании контекста хранилища с помощью параметра -UseConnectedAccount, но без входа в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="3d158-711">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="3d158-712">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="3d158-712">New-AzStorageContext</span></span>
* <span data-ttu-id="3d158-713">Поддержка свойств службы управления BLOB-объектов в указанной учетной записи хранения с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="3d158-713">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="3d158-714">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="3d158-714">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="3d158-715">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="3d158-715">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="3d158-716">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="3d158-716">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="3d158-717">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="3d158-717">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="3d158-718">Поддержка параметра -AsJob в командлетах для отправки и скачивания больших двоичных объектов и файлов.</span><span class="sxs-lookup"><span data-stu-id="3d158-718">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="3d158-719">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="3d158-719">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="3d158-720">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="3d158-720">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="3d158-721">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="3d158-721">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="3d158-722">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="3d158-722">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="3d158-723">1.6.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="3d158-723">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="3d158-724">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="3d158-724">Highlights since the last major release</span></span>
* <span data-ttu-id="3d158-725">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="3d158-725">General availability of `Az` module</span></span>
* <span data-ttu-id="3d158-726">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="3d158-726">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="3d158-727">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="3d158-727">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="3d158-728">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="3d158-728">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="3d158-729">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="3d158-729">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="3d158-730">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="3d158-730">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="3d158-731">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="3d158-731">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3d158-732">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3d158-732">Az.Automation</span></span>
* <span data-ttu-id="3d158-733">В управление обновлениями службы автоматизации Azure внесены изменения для поддержки следующих новых функций:</span><span class="sxs-lookup"><span data-stu-id="3d158-733">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="3d158-734">динамическое группирование;</span><span class="sxs-lookup"><span data-stu-id="3d158-734">Dynamic grouping</span></span>
    * <span data-ttu-id="3d158-735">скрипты предварительного или последующего выполнения;</span><span class="sxs-lookup"><span data-stu-id="3d158-735">Pre-Post script</span></span>
    * <span data-ttu-id="3d158-736">параметр перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="3d158-736">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3d158-737">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3d158-737">Az.Compute</span></span>
* <span data-ttu-id="3d158-738">Устранена проблема, связанная с разрешением пути в Get-AzVmBootDiagnosticsData.</span><span class="sxs-lookup"><span data-stu-id="3d158-738">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="3d158-739">Обновление клиентской библиотеки вычислений до версии 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="3d158-739">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="3d158-740">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3d158-740">Az.KeyVault</span></span>
* <span data-ttu-id="3d158-741">Добавлена поддержка подстановочных знаков в командлетах KeyVault.</span><span class="sxs-lookup"><span data-stu-id="3d158-741">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3d158-742">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3d158-742">Az.Network</span></span>
* <span data-ttu-id="3d158-743">Добавлена поддержка анализа угроз для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="3d158-743">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="3d158-744">Добавлены настраиваемые правила и ресурс верхнего уровня для политики брандмауэра Шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="3d158-744">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3d158-745">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3d158-745">Az.RecoveryServices</span></span>
* <span data-ttu-id="3d158-746">В политику виртуальной машины Azure добавлен объект SnapshotRetentionInDays для поддержки мгновенного восстановления.</span><span class="sxs-lookup"><span data-stu-id="3d158-746">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="3d158-747">Добавлена поддержка канала для отмены регистрации контейнера.</span><span class="sxs-lookup"><span data-stu-id="3d158-747">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="3d158-748">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3d158-748">Az.Resources</span></span>
* <span data-ttu-id="3d158-749">Обновлена поддержка подстановочных знаков для Get-AzResource и Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="3d158-749">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="3d158-750">Обновлены учетные данные, используемые при общих вызовах к ARM.</span><span class="sxs-lookup"><span data-stu-id="3d158-750">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="3d158-751">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3d158-751">Az.Sql</span></span>
* <span data-ttu-id="3d158-752">Изменен тип параметра (ExcludeDetectionType) командлетов для обнаружения угроз с DetectionTypes на string[] для поддержки актуального состояния при добавлении новых типов обнаружения и для поддержки автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="3d158-752">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3d158-753">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3d158-753">Az.Storage</span></span>
* <span data-ttu-id="3d158-754">Поддержка получения, настройки и удаления политики управления в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="3d158-754">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="3d158-755">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="3d158-755">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="3d158-756">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="3d158-756">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="3d158-757">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="3d158-757">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="3d158-758">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="3d158-758">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="3d158-759">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="3d158-759">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="3d158-760">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="3d158-760">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3d158-761">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3d158-761">Az.Websites</span></span>
* <span data-ttu-id="3d158-762">Исправлена ошибка с шаблоном ARM, из-за которой прерывалось клонирование все слотов при использовании New-AzWebApp -IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="3d158-762">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="3d158-763">1.5.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="3d158-763">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3d158-764">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3d158-764">Az.Accounts</span></span>
* <span data-ttu-id="3d158-765">Добавлена команда Register-AzModule для поддержки созданных командлетов AutoRest.</span><span class="sxs-lookup"><span data-stu-id="3d158-765">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="3d158-766">Обновлены примеры для Connect AzAccount.</span><span class="sxs-lookup"><span data-stu-id="3d158-766">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3d158-767">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3d158-767">Az.Automation</span></span>
* <span data-ttu-id="3d158-768">Исправлена проблема с получением некоторых ежемесячных расписаний в нескольких командлетах службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="3d158-768">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="3d158-769">Исправлен командлет Get-AzAutomationDscNode, возвращающий только первые 20 узлов.</span><span class="sxs-lookup"><span data-stu-id="3d158-769">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="3d158-770">Теперь он возвращает все узлы.</span><span class="sxs-lookup"><span data-stu-id="3d158-770">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="3d158-771">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="3d158-771">Az.Cdn</span></span>
* <span data-ttu-id="3d158-772">Добавлены новые командлеты PowerShell для включения и отключения HTTPS для личного домена и отключены устаревшие командлеты.</span><span class="sxs-lookup"><span data-stu-id="3d158-772">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3d158-773">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3d158-773">Az.Compute</span></span>
* <span data-ttu-id="3d158-774">Добавлена поддержка подстановочных знаков в командлетах Get.</span><span class="sxs-lookup"><span data-stu-id="3d158-774">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3d158-775">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3d158-775">Az.DataFactory</span></span>
* <span data-ttu-id="3d158-776">Обновлен пакет SDK для ADF .NET до версии 3.0.1.</span><span class="sxs-lookup"><span data-stu-id="3d158-776">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="3d158-777">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="3d158-777">Az.LogicApp</span></span>
* <span data-ttu-id="3d158-778">Исправлена проблема с получением только первой страницы результатов при выполнении команды ListWorkflows.</span><span class="sxs-lookup"><span data-stu-id="3d158-778">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3d158-779">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3d158-779">Az.Network</span></span>
* <span data-ttu-id="3d158-780">Добавлена поддержка подстановочных знаков в командлетах Network.</span><span class="sxs-lookup"><span data-stu-id="3d158-780">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3d158-781">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3d158-781">Az.RecoveryServices</span></span>
* <span data-ttu-id="3d158-782">Добавлена поддержка SQL Server на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="3d158-782">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="3d158-783">Обновление пакета SDK</span><span class="sxs-lookup"><span data-stu-id="3d158-783">SDK Update</span></span>
* <span data-ttu-id="3d158-784">Удалена проверка VMappContainer в Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="3d158-784">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="3d158-785">Добавлены параметры Name и ServerName для Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="3d158-785">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="3d158-786">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3d158-786">Az.Resources</span></span>
* <span data-ttu-id="3d158-787">Добавлен параметр `-TemplateObject` в командлеты для развертывания.</span><span class="sxs-lookup"><span data-stu-id="3d158-787">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="3d158-788">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2933.</span><span class="sxs-lookup"><span data-stu-id="3d158-788">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="3d158-789">Устранена проблема с передачей в конвейер результата `Get-AzResource` для `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="3d158-789">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="3d158-790">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8240.</span><span class="sxs-lookup"><span data-stu-id="3d158-790">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="3d158-791">Устранена проблема с изменением типа данных JSON при выполнении `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="3d158-791">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="3d158-792">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7930.</span><span class="sxs-lookup"><span data-stu-id="3d158-792">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="3d158-793">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3d158-793">Az.Sql</span></span>
* <span data-ttu-id="3d158-794">Обновление AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="3d158-794">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="3d158-795">Исправлено поведение для пограничного случая при создании параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="3d158-795">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3d158-796">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3d158-796">Az.Storage</span></span>
* <span data-ttu-id="3d158-797">Включена поддержка Kind BlockBlobStorage при создании учетной записи хранения для New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="3d158-797">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="3d158-798">1.4.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="3d158-798">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="3d158-799">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3d158-799">Az.AnalysisServices</span></span>
* <span data-ttu-id="3d158-800">Командлет AddAzureASAccount устарел.</span><span class="sxs-lookup"><span data-stu-id="3d158-800">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3d158-801">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3d158-801">Az.Automation</span></span>
* <span data-ttu-id="3d158-802">Обновлена справка для командлета Import-AzAutomationDscNodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="3d158-802">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="3d158-803">Добавлена проверка имени конфигурации для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="3d158-803">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="3d158-804">Улучшена обработка ошибок для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="3d158-804">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="3d158-805">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3d158-805">Az.CognitiveServices</span></span>
* <span data-ttu-id="3d158-806">Добавлен параметр CustomSubdomainName — новый необязательный параметр для командлета New-AzCognitiveServicesAccount, который указывает поддомен для ресурса.</span><span class="sxs-lookup"><span data-stu-id="3d158-806">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3d158-807">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3d158-807">Az.Compute</span></span>
* <span data-ttu-id="3d158-808">Устранена проблема с идентификаторами наборов параметров.</span><span class="sxs-lookup"><span data-stu-id="3d158-808">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="3d158-809">Обновлен командлет Get-AzVMExtension для отображения списка всех установленных расширений, если не указан параметр Name.</span><span class="sxs-lookup"><span data-stu-id="3d158-809">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="3d158-810">Для командлета Update-AzImage добавлены параметры Tag и ResourceId.</span><span class="sxs-lookup"><span data-stu-id="3d158-810">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="3d158-811">Командлет Get-AzVmssVM, который выполняется без указания идентификатора экземпляра и с параметром InstanceView, может выводить виртуальные машины из VMSS с представлением экземпляра.</span><span class="sxs-lookup"><span data-stu-id="3d158-811">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3d158-812">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3d158-812">Az.DataLakeStore</span></span>
* <span data-ttu-id="3d158-813">Добавлены командлеты для перечисления и восстановления удаленного элемента ADL.</span><span class="sxs-lookup"><span data-stu-id="3d158-813">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="3d158-814">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="3d158-814">Az.EventHub</span></span>
* <span data-ttu-id="3d158-815">Добавлено новое логическое свойство SkipEmptyArchives для пропуска пустых архивов в классе CaptureDescription Eventhub.</span><span class="sxs-lookup"><span data-stu-id="3d158-815">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="3d158-816">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3d158-816">Az.KeyVault</span></span>
* <span data-ttu-id="3d158-817">Исправлена расстановка тегов для командлета Set-AzKeyVaultSecret.</span><span class="sxs-lookup"><span data-stu-id="3d158-817">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="3d158-818">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="3d158-818">Az.LogicApp</span></span>
* <span data-ttu-id="3d158-819">Добавлен SKU "Базовый" для учетных записей интеграции.</span><span class="sxs-lookup"><span data-stu-id="3d158-819">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="3d158-820">Добавлены типы сопоставлений Liquid, а также XSLT 2.0 и XSLT 3.0.</span><span class="sxs-lookup"><span data-stu-id="3d158-820">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="3d158-821">Новые командлеты для сборок учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="3d158-821">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="3d158-822">Get-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="3d158-822">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="3d158-823">New-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="3d158-823">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="3d158-824">Remove-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="3d158-824">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="3d158-825">Set-AzIntegrationAccountAssembly.</span><span class="sxs-lookup"><span data-stu-id="3d158-825">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="3d158-826">Новые командлеты для конфигурации пакета учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="3d158-826">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="3d158-827">Get-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="3d158-827">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="3d158-828">New-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="3d158-828">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="3d158-829">Remove-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="3d158-829">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="3d158-830">Set-AzIntegrationAccountBatchConfiguration.</span><span class="sxs-lookup"><span data-stu-id="3d158-830">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="3d158-831">Обновлен пакет SDK Logic Apps до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="3d158-831">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3d158-832">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3d158-832">Az.Monitor</span></span>
* <span data-ttu-id="3d158-833">Обновлена справка для командлета Get-AzMetric.</span><span class="sxs-lookup"><span data-stu-id="3d158-833">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3d158-834">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3d158-834">Az.Network</span></span>
* <span data-ttu-id="3d158-835">Обновлен пример справки для командлета Add-AzApplicationGatewayCustomError.</span><span class="sxs-lookup"><span data-stu-id="3d158-835">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="3d158-836">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3d158-836">Az.OperationalInsights</span></span>
* <span data-ttu-id="3d158-837">Дополнительная поддержка создания и получения источников данных ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="3d158-837">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="3d158-838">Добавлен новый тип ApplicationInsights для получения определенных или всех источников данных ApplicationInsights для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="3d158-838">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="3d158-839">Добавлен командлет New-AzOperationalInsightsApplicationInsightsDataSource для создания источника данных с использованием параметров указанного ресурса Application-Insightss: subscription Id, resourceGroupName и name.</span><span class="sxs-lookup"><span data-stu-id="3d158-839">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="3d158-840">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3d158-840">Az.Resources</span></span>
* <span data-ttu-id="3d158-841">исправлена проблема https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="3d158-841">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="3d158-842">исправлена проблема https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="3d158-842">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="3d158-843">исправлена проблема https://github.com/Azure/azure-powershell/issues/6219.</span><span class="sxs-lookup"><span data-stu-id="3d158-843">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="3d158-844">Исправлена ошибка, препятствующая повторному созданию KeyCredentials.</span><span class="sxs-lookup"><span data-stu-id="3d158-844">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="3d158-845">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3d158-845">Az.Sql</span></span>
* <span data-ttu-id="3d158-846">Добавлена поддержка уровня гипермасштабирования в базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="3d158-846">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="3d158-847">Исправлена ошибка, из-за которой восстановление могло завершиться со сбоем при указании ненужных свойств в запросе на восстановление.</span><span class="sxs-lookup"><span data-stu-id="3d158-847">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3d158-848">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3d158-848">Az.Websites</span></span>
* <span data-ttu-id="3d158-849">Исправлен пример для командлета Get-AzWebAppSlotMetrics.</span><span class="sxs-lookup"><span data-stu-id="3d158-849">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="3d158-850">1.3.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="3d158-850">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3d158-851">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3d158-851">Az.Accounts</span></span>
* <span data-ttu-id="3d158-852">Обновление до последней версии ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="3d158-852">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="3d158-853">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3d158-853">Az.AnalysisServices</span></span>
<span data-ttu-id="3d158-854">Общедоступная версия модуля Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="3d158-854">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3d158-855">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3d158-855">Az.Compute</span></span>
* <span data-ttu-id="3d158-856">Расширение AEM: добавлена поддержка дисков UltraSSD, P60, P70 и P80.</span><span class="sxs-lookup"><span data-stu-id="3d158-856">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="3d158-857">Обновлено описание справки для командлета Set-AzVMBootDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="3d158-857">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="3d158-858">Обновлено описание справки и пример для командлета Update-AzImage.</span><span class="sxs-lookup"><span data-stu-id="3d158-858">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3d158-859">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3d158-859">Az.RecoveryServices</span></span>
<span data-ttu-id="3d158-860">Общедоступная версия модуля Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="3d158-860">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3d158-861">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3d158-861">Az.Resources</span></span>
* <span data-ttu-id="3d158-862">Исправлена расстановка тегов для групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3d158-862">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="3d158-863">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="3d158-863">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="3d158-864">Исправлена проблема с игнорированием командлетом `Get-AzureRmRoleAssignment` параметра -ErrorAction.</span><span class="sxs-lookup"><span data-stu-id="3d158-864">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="3d158-865">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="3d158-865">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="3d158-866">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3d158-866">Az.Sql</span></span>
* <span data-ttu-id="3d158-867">Добавлен командлет Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="3d158-867">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="3d158-868">Исправлена проблема с появлением исключения NullRef при выполнении командлетов SQL, если не выполнен вход в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="3d158-868">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="3d158-869">Исправлено исключение NullRef в командлете Get-AzSqlCapability.</span><span class="sxs-lookup"><span data-stu-id="3d158-869">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="3d158-870">1.2.1 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="3d158-870">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3d158-871">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3d158-871">Az.Accounts</span></span>
* <span data-ttu-id="3d158-872">Выпуск с правильной версией службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="3d158-872">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="3d158-873">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3d158-873">Az.AnalysisServices</span></span>
* <span data-ttu-id="3d158-874">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="3d158-874">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3d158-875">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3d158-875">Az.RecoveryServices</span></span>
* <span data-ttu-id="3d158-876">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="3d158-876">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="3d158-877">1.2.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="3d158-877">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3d158-878">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3d158-878">Az.Accounts</span></span>
* <span data-ttu-id="3d158-879">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="3d158-879">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="3d158-880">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="3d158-880">Update incorrect online help URLs</span></span>
* <span data-ttu-id="3d158-881">Добавлено предупреждающее сообщение в PS Core для модуля Uninstall-AzureRm.</span><span class="sxs-lookup"><span data-stu-id="3d158-881">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="3d158-882">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="3d158-882">Az.Aks</span></span>
* <span data-ttu-id="3d158-883">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="3d158-883">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3d158-884">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3d158-884">Az.Automation</span></span>
* <span data-ttu-id="3d158-885">Добавлена поддержка для модулей runbook Python 2.</span><span class="sxs-lookup"><span data-stu-id="3d158-885">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="3d158-886">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="3d158-886">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="3d158-887">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="3d158-887">Az.Cdn</span></span>
* <span data-ttu-id="3d158-888">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="3d158-888">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3d158-889">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3d158-889">Az.Compute</span></span>
* <span data-ttu-id="3d158-890">Добавлен командлет Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="3d158-890">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="3d158-891">Добавлен параметр TempDisk к командлету Set-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="3d158-891">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="3d158-892">Исправлено предупреждающее сообщение командлета New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="3d158-892">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="3d158-893">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="3d158-893">Az.ContainerRegistry</span></span>
* <span data-ttu-id="3d158-894">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="3d158-894">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3d158-895">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3d158-895">Az.DataFactory</span></span>
* <span data-ttu-id="3d158-896">Пакет SDK ADF .Net обновлен до версии 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="3d158-896">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3d158-897">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3d158-897">Az.DataLakeStore</span></span>
* <span data-ttu-id="3d158-898">Исправлена проблема с конечной точкой ADLS при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="3d158-898">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="3d158-899">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7462.</span><span class="sxs-lookup"><span data-stu-id="3d158-899">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="3d158-900">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="3d158-900">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3d158-901">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3d158-901">Az.IotHub</span></span>
* <span data-ttu-id="3d158-902">Добавлен формат кодирования для командлета Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="3d158-902">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="3d158-903">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3d158-903">Az.KeyVault</span></span>
* <span data-ttu-id="3d158-904">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="3d158-904">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3d158-905">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3d158-905">Az.Network</span></span>
* <span data-ttu-id="3d158-906">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="3d158-906">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="3d158-907">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3d158-907">Az.Resources</span></span>
* <span data-ttu-id="3d158-908">Исправлены неправильные примеры в справочной документации по командлетам New-AzADAppCredential и New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="3d158-908">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="3d158-909">Исправлена проблема, при которой путь для параметра -TemplateFile не удавалось разрешить до выполнения командлетов развертывания групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3d158-909">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="3d158-910">Az.Resources: исправлена документация для значения по умолчанию -Mode командлета New-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="3d158-910">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="3d158-911">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/7522.</span><span class="sxs-lookup"><span data-stu-id="3d158-911">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="3d158-912">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/5747.</span><span class="sxs-lookup"><span data-stu-id="3d158-912">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="3d158-913">Исправлена проблема с форматированием объекта PSResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="3d158-913">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="3d158-914">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2123.</span><span class="sxs-lookup"><span data-stu-id="3d158-914">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="3d158-915">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3d158-915">Az.ServiceFabric</span></span>
* <span data-ttu-id="3d158-916">Исправлена проблема с появлением исключения в процессе отката при добавлении сертификата к модели VMSS: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="3d158-916">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="3d158-917">Исправлены некоторые сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="3d158-917">Fix some error messages.</span></span>
* <span data-ttu-id="3d158-918">Исправлена проблема с созданием кластера с шаблоном ARM по умолчанию для командлета New-AzServiceFabriCluster, который не работал с операцией миграции в Az.</span><span class="sxs-lookup"><span data-stu-id="3d158-918">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="3d158-919">Исправлена проблема с добавлением сертификата кластера или приложения: теперь они добавляются только в Масштабируемые наборы виртуальных машин, которые сопоставлены с кластером, путем проверки идентификатора кластера в расширении.</span><span class="sxs-lookup"><span data-stu-id="3d158-919">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="3d158-920">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="3d158-920">Az.SignalR</span></span>
* <span data-ttu-id="3d158-921">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="3d158-921">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="3d158-922">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3d158-922">Az.Sql</span></span>
* <span data-ttu-id="3d158-923">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="3d158-923">Update incorrect online help URLs</span></span>
* <span data-ttu-id="3d158-924">Обновлено описание параметра LicenseType с добавлением возможных значений.</span><span class="sxs-lookup"><span data-stu-id="3d158-924">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="3d158-925">Исправлена проблема с неправильным обновлением удостоверения управляемого экземпляра, если оно было единственным обновляемым свойством.</span><span class="sxs-lookup"><span data-stu-id="3d158-925">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="3d158-926">Поддержка пользовательских параметров сортировки в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="3d158-926">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3d158-927">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3d158-927">Az.Storage</span></span>
* <span data-ttu-id="3d158-928">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="3d158-928">Update incorrect online help URLs</span></span>
* <span data-ttu-id="3d158-929">Добавлен вывод подробных сообщений об ошибке при получении или установке классических свойств ведения журнала или метрик в учетной записи хранилища класса Premium, так как учетная запись хранилища класса Premium не поддерживает классические функции ведения журнала и метрик.</span><span class="sxs-lookup"><span data-stu-id="3d158-929">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="3d158-930">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="3d158-930">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="3d158-931">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="3d158-931">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="3d158-932">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="3d158-932">Az.TrafficManager</span></span>
* <span data-ttu-id="3d158-933">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="3d158-933">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3d158-934">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3d158-934">Az.Websites</span></span>
* <span data-ttu-id="3d158-935">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="3d158-935">Update incorrect online help URLs</span></span>
* <span data-ttu-id="3d158-936">Исправлена работа командлета New-AzWebAppSSLBinding: сертификат отправляется в правильную группу ресурсов и правильное расположение, если приложение размещено в ASE.</span><span class="sxs-lookup"><span data-stu-id="3d158-936">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="3d158-937">Исправлена работа командлета New-AzWebAppSSLBinding: теги не перезаписываются при привязке SSL-сертификата к приложению.</span><span class="sxs-lookup"><span data-stu-id="3d158-937">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="3d158-938">1.1.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="3d158-938">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3d158-939">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3d158-939">Az.Accounts</span></span>
* <span data-ttu-id="3d158-940">Добавление области "Local" в Enable-AzureRmAlias.</span><span class="sxs-lookup"><span data-stu-id="3d158-940">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3d158-941">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3d158-941">Az.Compute</span></span>
* <span data-ttu-id="3d158-942">Теперь имя не является обязательным в идентификаторе набора параметров для Restart/Start/Stop/Remove/Set-AzVM и Save-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="3d158-942">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="3d158-943">Обновлено описание идентификатора в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="3d158-943">Updated the description of ID in help files</span></span>
* <span data-ttu-id="3d158-944">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="3d158-944">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3d158-945">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3d158-945">Az.DataLakeStore</span></span>
* <span data-ttu-id="3d158-946">Обновление версии пакета SDK для плоскости данных до 1.1.14 для устранения найденных проблем.</span><span class="sxs-lookup"><span data-stu-id="3d158-946">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="3d158-947">Исправлена обработка отрицательного времени доступа и времени изменения для getfilestatus и liststatus, исправлен токен отмены для асинхронных методов.</span><span class="sxs-lookup"><span data-stu-id="3d158-947">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="3d158-948">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="3d158-948">Az.EventGrid</span></span>
* <span data-ttu-id="3d158-949">Обновление для использования API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="3d158-949">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="3d158-950">Обновлены указанные ниже командлеты для поддержки нового сценария в API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="3d158-950">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="3d158-951">New-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="3d158-951">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="3d158-952">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="3d158-952">Event Time-To-Live,</span></span>
        - <span data-ttu-id="3d158-953">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="3d158-953">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="3d158-954">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="3d158-954">Dead letter endpoint.</span></span>
    - <span data-ttu-id="3d158-955">Update-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="3d158-955">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="3d158-956">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="3d158-956">Event Time-To-Live,</span></span>
        - <span data-ttu-id="3d158-957">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="3d158-957">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="3d158-958">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="3d158-958">Dead letter endpoint.</span></span>
* <span data-ttu-id="3d158-959">Для параметра EndpointType добавлены новые значения перечисления (storageQueue и hybridConnection) в командлеты New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="3d158-959">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="3d158-960">Если ожидается, что создание или обновление подписки на событие повлечет за собой действия со стороны пользователя, выполняемые вручную, отображается предупреждение при создании или обновлении подписки события.</span><span class="sxs-lookup"><span data-stu-id="3d158-960">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3d158-961">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3d158-961">Az.IotHub</span></span>
* <span data-ttu-id="3d158-962">Пакет SDK Центра Интернета вещей обновлен до последней версии.</span><span class="sxs-lookup"><span data-stu-id="3d158-962">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="3d158-963">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="3d158-963">Az.LogicApp</span></span>
* <span data-ttu-id="3d158-964">Get-AzLogicApp позволяет перечислить все параметры без указанного имени.</span><span class="sxs-lookup"><span data-stu-id="3d158-964">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="3d158-965">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3d158-965">Az.Resources</span></span>
* <span data-ttu-id="3d158-966">Исправлена проблема с набором параметров при предоставлении параметров "-ODataQuery" и "-ResourceId" для "Get-AzResource".</span><span class="sxs-lookup"><span data-stu-id="3d158-966">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="3d158-967">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7875.</span><span class="sxs-lookup"><span data-stu-id="3d158-967">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="3d158-968">Исправлена обработка параметра -Custom в New/Set-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="3d158-968">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="3d158-969">Исправлена опечатка в документации по New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="3d158-969">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="3d158-970">Параметр "-MailNickname" стал обязательным для "New-AzADUser".</span><span class="sxs-lookup"><span data-stu-id="3d158-970">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="3d158-971">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8220.</span><span class="sxs-lookup"><span data-stu-id="3d158-971">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="3d158-972">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="3d158-972">Az.SignalR</span></span>
* <span data-ttu-id="3d158-973">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="3d158-973">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="3d158-974">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3d158-974">Az.Sql</span></span>
* <span data-ttu-id="3d158-975">Зависимость клиента управления хранением преобразована для общей реализации в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="3d158-975">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3d158-976">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3d158-976">Az.Storage</span></span>
* <span data-ttu-id="3d158-977">Установка параметра StorageAccountName для контекста хранилища в качестве реального имени учетной записи хранения, если она была создана с использованием токена Sas, OAuth или анонимного доступа.</span><span class="sxs-lookup"><span data-stu-id="3d158-977">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="3d158-978">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="3d158-978">New-AzStorageContext</span></span>
* <span data-ttu-id="3d158-979">Создание токена Sas большого двоичного объекта моментального снимка с параметром "-FullUri". Возвращаемый URI исправлен на URI моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="3d158-979">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="3d158-980">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="3d158-980">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3d158-981">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3d158-981">Az.Websites</span></span>
* <span data-ttu-id="3d158-982">Исправлена ошибка синтаксического анализа даты в "Get-AzDeletedWebApp".</span><span class="sxs-lookup"><span data-stu-id="3d158-982">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="3d158-983">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="3d158-983">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="3d158-984">1.0.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="3d158-984">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="3d158-985">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="3d158-985">General</span></span>

- <span data-ttu-id="3d158-986">Общедоступная версия модуля Az.</span><span class="sxs-lookup"><span data-stu-id="3d158-986">General Availability of Az Module</span></span>
- <span data-ttu-id="3d158-987">Справка в Интернете для каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="3d158-987">Online help for each module</span></span>
- <span data-ttu-id="3d158-988">Дополнительные сведения и стратегию развития см. в статье [Announcing New Module 'Az'](https://aka.ms/azps-announce) (Объявление о новом модуле Az)</span><span class="sxs-lookup"><span data-stu-id="3d158-988">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="3d158-989">Сведения о миграции с AzureRM см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="3d158-989">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="3d158-990">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3d158-990">Az.Accounts</span></span>
- <span data-ttu-id="3d158-991">Изменено с Az.Profile.</span><span class="sxs-lookup"><span data-stu-id="3d158-991">Changed from Az.Profile</span></span>
- <span data-ttu-id="3d158-992">Исправлены форматы таблиц для типов профиля и контекста.</span><span class="sxs-lookup"><span data-stu-id="3d158-992">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="3d158-993">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3d158-993">Az.ApiManagement</span></span>
- <span data-ttu-id="3d158-994">Исправления для #7002.</span><span class="sxs-lookup"><span data-stu-id="3d158-994">Fixes for #7002</span></span>
- <span data-ttu-id="3d158-995">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="3d158-995">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="3d158-996">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="3d158-996">Az.Batch</span></span>
- <span data-ttu-id="3d158-997">Добавлена возможность видеть, какая версия агента узла пакетной службы Azure работает в пуле на каждой виртуальной машине, с помощью нового свойства `NodeAgentInformation` в `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="3d158-997">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="3d158-998">Значение `Caching` по умолчанию для `PSDataDisk` теперь `ReadWrite` вместо `None`.</span><span class="sxs-lookup"><span data-stu-id="3d158-998">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="3d158-999">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="3d158-999">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="3d158-1000">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="3d158-1000">Az.Billing</span></span>
- <span data-ttu-id="3d158-1001">Объединены командлеты Billing, Consumption и UsageAggregates. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0).</span><span class="sxs-lookup"><span data-stu-id="3d158-1001">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="3d158-1002">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="3d158-1002">Az.CognitivServices</span></span>
- <span data-ttu-id="3d158-1003">Добавлены средства заполнения для SkuName и Typem, доступные в операции New-AzureRmCognitiveServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="3d158-1003">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="3d158-1004">Удален набор параметров GetSkusWithAccountParamSetName из Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="3d158-1004">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="3d158-1005">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="3d158-1005">Az.ContainerInstance</span></span>
- <span data-ttu-id="3d158-1006">Добавлена поддержка ManagedIdentity.</span><span class="sxs-lookup"><span data-stu-id="3d158-1006">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="3d158-1007">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="3d158-1007">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="3d158-1008">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="3d158-1008">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="3d158-1009">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3d158-1009">Az.DataLakeStore</span></span>
- <span data-ttu-id="3d158-1010">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="3d158-1010">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="3d158-1011">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3d158-1011">Az.Monitor</span></span>
- <span data-ttu-id="3d158-1012">"Az.Insights" переименован в "Az.Monitor" и внесены другие незначительные критические изменения. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="3d158-1012">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="3d158-1013">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3d158-1013">Az.KeyVault</span></span>
- <span data-ttu-id="3d158-1014">Из типов вывода удалено устаревшее свойство PurgeDisabled</span><span class="sxs-lookup"><span data-stu-id="3d158-1014">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="3d158-1015">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="3d158-1015">Az.MachineLearning</span></span>
- <span data-ttu-id="3d158-1016">Включены командлеты из модуля Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="3d158-1016">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="3d158-1017">Az.Media</span><span class="sxs-lookup"><span data-stu-id="3d158-1017">Az.Media</span></span>
- <span data-ttu-id="3d158-1018">Удаляет устаревший псевдоним Tags из New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="3d158-1018">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="3d158-1019">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3d158-1019">Az.Network</span></span>
<span data-ttu-id="3d158-1020">В шлюз приложений добавлена поддержка настройки RewriteRuleSets</span><span class="sxs-lookup"><span data-stu-id="3d158-1020">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="3d158-1021">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="3d158-1021">New cmdlets added:</span></span>
        - <span data-ttu-id="3d158-1022">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3d158-1022">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="3d158-1023">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3d158-1023">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="3d158-1024">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3d158-1024">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="3d158-1025">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3d158-1025">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="3d158-1026">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3d158-1026">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="3d158-1027">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="3d158-1027">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="3d158-1028">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="3d158-1028">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="3d158-1029">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="3d158-1029">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="3d158-1030">В следующие командлеты добавлен необязательный параметр -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3d158-1030">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="3d158-1031">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3d158-1031">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="3d158-1032">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="3d158-1032">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="3d158-1033">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="3d158-1033">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="3d158-1034">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3d158-1034">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="3d158-1035">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="3d158-1035">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="3d158-1036">New-AzureRmApplicationGatewayUrlPathMapConfig добавил с помощью идентификатора поддержку KeyVault для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="3d158-1036">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="3d158-1037">В следующие командлеты добавлен необязательный параметр -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="3d158-1037">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="3d158-1038">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3d158-1038">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="3d158-1039">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3d158-1039">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="3d158-1040">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3d158-1040">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="3d158-1041">В командлет New-AzApplicationGateway добавлен необязательный параметр -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="3d158-1041">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="3d158-1042">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="3d158-1042">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="3d158-1043">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3d158-1043">Az.OperationalInsights</span></span>
- <span data-ttu-id="3d158-1044">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="3d158-1044">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="3d158-1045">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="3d158-1045">Az.Profile</span></span>
- <span data-ttu-id="3d158-1046">Имя модуля изменено на Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="3d158-1046">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="3d158-1047">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3d158-1047">Az.RecoveryServices</span></span>
- <span data-ttu-id="3d158-1048">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="3d158-1048">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="3d158-1049">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3d158-1049">Az.Resources</span></span>
- <span data-ttu-id="3d158-1050">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="3d158-1050">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="3d158-1051">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3d158-1051">Az.ServiceFabric</span></span>
- <span data-ttu-id="3d158-1052">Поддержка спецификации сертификата по общему имени и отпечатку</span><span class="sxs-lookup"><span data-stu-id="3d158-1052">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="3d158-1053">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="3d158-1053">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="3d158-1054">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="3d158-1054">Az.SIgnalR</span></span>
- <span data-ttu-id="3d158-1055">Общедоступная версия командлетов PowerShell для SIgnalR</span><span class="sxs-lookup"><span data-stu-id="3d158-1055">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="3d158-1056">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3d158-1056">Az.Sql</span></span>
- <span data-ttu-id="3d158-1057">Добавлены новые типы обнаружения Data_Exfiltration и Unsafe_Action в командлеты обнаружения угроз</span><span class="sxs-lookup"><span data-stu-id="3d158-1057">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="3d158-1058">Примеры обновленной документации для командлетов аудита Sql</span><span class="sxs-lookup"><span data-stu-id="3d158-1058">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="3d158-1059">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="3d158-1059">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="3d158-1060">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3d158-1060">Az.Storage</span></span>
- <span data-ttu-id="3d158-1061">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="3d158-1061">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="3d158-1062">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3d158-1062">Az.Websites</span></span>
- <span data-ttu-id="3d158-1063">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="3d158-1063">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="3d158-1064">0.7.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="3d158-1064">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="3d158-1065">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="3d158-1065">General</span></span>

* <span data-ttu-id="3d158-1066">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="3d158-1066">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="3d158-1067">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3d158-1067">Az.Compute</span></span>

* <span data-ttu-id="3d158-1068">Добавлена поддержка UltraSSD и образов коллекции в простых наборах параметров для командлетов `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="3d158-1068">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="3d158-1069">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3d158-1069">Az.DataLakeStore</span></span>

* <span data-ttu-id="3d158-1070">Исправлено косую черту в конце домена учетной записи ADLS</span><span class="sxs-lookup"><span data-stu-id="3d158-1070">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="3d158-1071">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="3d158-1071">Az.FrontDoor</span></span>

* <span data-ttu-id="3d158-1072">Исправлены некоторые неработающие ссылки</span><span class="sxs-lookup"><span data-stu-id="3d158-1072">Fixed some broken links</span></span>
    - <span data-ttu-id="3d158-1073">В статьях New-AzureRmFrontDoor и Set-AzureRmFrontDoor исправлена ссылка на статью командлета New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="3d158-1073">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="3d158-1074">В статье New-AzureRmFrontDoorManagedRuleObject исправлена ссылка на статью командлета New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="3d158-1074">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="3d158-1075">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3d158-1075">Az.RecoveryServices</span></span>

* <span data-ttu-id="3d158-1076">Добавлены проверки на стороне клиента для операций восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="3d158-1076">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="3d158-1077">StorageAccountName и storageAccountResourceGroupName являются необязательными для восстановления afs.</span><span class="sxs-lookup"><span data-stu-id="3d158-1077">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="3d158-1078">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3d158-1078">Az.Resources</span></span>

* <span data-ttu-id="3d158-1079">Исправление для https://github.com/Azure/azure-powershell/issues/7679.</span><span class="sxs-lookup"><span data-stu-id="3d158-1079">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="3d158-1080">Обновите Get-AzureRmRoleAssignment, чтобы использовать область подписки, если она указана при запросе классических администраторов.</span><span class="sxs-lookup"><span data-stu-id="3d158-1080">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="3d158-1081">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3d158-1081">Az.Sql</span></span>

* <span data-ttu-id="3d158-1082">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="3d158-1082">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="3d158-1083">Устранена проблема с использованием Get-AzureRmSqlDatabaseVulnerabilityAssessment с .NET Core.</span><span class="sxs-lookup"><span data-stu-id="3d158-1083">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="3d158-1084">Изменена документация справочных сообщений, связанных с командлетами аудита SQL.</span><span class="sxs-lookup"><span data-stu-id="3d158-1084">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="3d158-1085">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3d158-1085">Az.Storage</span></span>

* <span data-ttu-id="3d158-1086">Добавлено -EnableHierarchicalNamespace к New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3d158-1086">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="3d158-1087">Устранена проблема, из-за которой командлет Copy File не может повторно использовать исходный контекст в пункте назначения, если не введен -DestContext</span><span class="sxs-lookup"><span data-stu-id="3d158-1087">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="3d158-1088">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="3d158-1088">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="3d158-1089">Поддержка статической конфигурации сайта</span><span class="sxs-lookup"><span data-stu-id="3d158-1089">Support Static Website configuration</span></span>
    - <span data-ttu-id="3d158-1090">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="3d158-1090">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="3d158-1091">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="3d158-1091">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="3d158-1092">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3d158-1092">Az.Websites</span></span>

* <span data-ttu-id="3d158-1093">Set-AzureRmWebApp и Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3d158-1093">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="3d158-1094">Добавлен новый параметр (-AzureStoragePath), который указывает путь службы хранилища Azure для подключения в приложениях-контейнерах Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="3d158-1094">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="3d158-1095">Используйте выходные данные нового командлета New-AzureRmWebAppAzureStoragePath в качестве параметра, чтобы задать пути к службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="3d158-1095">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="3d158-1096">0.6.1 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="3d158-1096">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="3d158-1097">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3d158-1097">Az.ApiManagement</span></span>
* <span data-ttu-id="3d158-1098">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="3d158-1098">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="3d158-1099">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3d158-1099">Az.Automation</span></span>
* <span data-ttu-id="3d158-1100">Командлеты службы автоматизации Azure на базе Swagger.</span><span class="sxs-lookup"><span data-stu-id="3d158-1100">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="3d158-1101">Добавлены командлеты для Управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="3d158-1101">Added Update Management cmdlets</span></span>
* <span data-ttu-id="3d158-1102">Добавлены командлеты для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="3d158-1102">Added Source Control cmdlets</span></span>
* <span data-ttu-id="3d158-1103">Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="3d158-1103">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="3d158-1104">Исправлена команда DSC для регистрации узла.</span><span class="sxs-lookup"><span data-stu-id="3d158-1104">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="3d158-1105">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3d158-1105">Az.Compute</span></span>
* <span data-ttu-id="3d158-1106">Исправлена проблема с удостоверением, назначаемым системой.</span><span class="sxs-lookup"><span data-stu-id="3d158-1106">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="3d158-1107">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="3d158-1107">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="3d158-1108">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="3d158-1108">Az.ContainerInstance</span></span>
* <span data-ttu-id="3d158-1109">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="3d158-1109">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="3d158-1110">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="3d158-1110">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="3d158-1111">Обновлено описание в примерах командлетов для Marketplace.</span><span class="sxs-lookup"><span data-stu-id="3d158-1111">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="3d158-1112">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3d158-1112">Az.Network</span></span>
* <span data-ttu-id="3d158-1113">Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="3d158-1113">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="3d158-1114">Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="3d158-1114">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="3d158-1115">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="3d158-1115">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="3d158-1116">Исправлены проблемы с использованием памяти в карте виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="3d158-1116">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="3d158-1117">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="3d158-1117">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="3d158-1118">Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="3d158-1118">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="3d158-1119">Параметры часового пояса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="3d158-1119">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="3d158-1120">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="3d158-1120">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="3d158-1121">Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="3d158-1121">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="3d158-1122">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="3d158-1122">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="3d158-1123">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="3d158-1123">Az.Relay</span></span>
* <span data-ttu-id="3d158-1124">Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.</span><span class="sxs-lookup"><span data-stu-id="3d158-1124">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="3d158-1125">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3d158-1125">Az.Resources</span></span>
* <span data-ttu-id="3d158-1126">Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.</span><span class="sxs-lookup"><span data-stu-id="3d158-1126">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="3d158-1127">Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.</span><span class="sxs-lookup"><span data-stu-id="3d158-1127">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="3d158-1128">Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.</span><span class="sxs-lookup"><span data-stu-id="3d158-1128">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="3d158-1129">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3d158-1129">Az.ServiceFabric</span></span>
* <span data-ttu-id="3d158-1130">Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.</span><span class="sxs-lookup"><span data-stu-id="3d158-1130">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="3d158-1131">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3d158-1131">Az.Sql</span></span>
* <span data-ttu-id="3d158-1132">Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="3d158-1132">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="3d158-1133">Get-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="3d158-1133">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="3d158-1134">New-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="3d158-1134">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="3d158-1135">Set-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="3d158-1135">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="3d158-1136">Remove-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="3d158-1136">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="3d158-1137">Get-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="3d158-1137">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="3d158-1138">New-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="3d158-1138">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="3d158-1139">Restore-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="3d158-1139">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="3d158-1140">Remove-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="3d158-1140">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="3d158-1141">Добавлено расширенное управление политиками аудита для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="3d158-1141">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="3d158-1142">Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="3d158-1142">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="3d158-1143">Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.</span><span class="sxs-lookup"><span data-stu-id="3d158-1143">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="3d158-1144">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="3d158-1144">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="3d158-1145">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="3d158-1145">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="3d158-1146">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="3d158-1146">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="3d158-1147">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="3d158-1147">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="3d158-1148">Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="3d158-1148">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="3d158-1149">0.5.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="3d158-1149">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="3d158-1150">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="3d158-1150">General</span></span>
* <span data-ttu-id="3d158-1151">Добавлены средства заполнения ресурсов для многих основных командлетов — они позволяют вам переключать существующие имена ресурсов при вызове командлетов в интерактивном режиме</span><span class="sxs-lookup"><span data-stu-id="3d158-1151">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="3d158-1152">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="3d158-1152">Az.Profile</span></span>
* <span data-ttu-id="3d158-1153">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3d158-1153">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="3d158-1154">В командлете Connect-AzAccount параметр TenantId переименован в Tenant и добавлен псевдоним для TenantId</span><span class="sxs-lookup"><span data-stu-id="3d158-1154">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="3d158-1155">Обновлено описание TenantId для командлета Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="3d158-1155">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="3d158-1156">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="3d158-1156">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="3d158-1157">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="3d158-1157">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="3d158-1158">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="3d158-1158">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="3d158-1159">Устранена проблема, при которой командлет Disconnect-AzAccount вызывал сбой при отсутствии подключения</span><span class="sxs-lookup"><span data-stu-id="3d158-1159">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="3d158-1160">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3d158-1160">Az.CognitiveServices</span></span>
* <span data-ttu-id="3d158-1161">Добавлена операция Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="3d158-1161">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3d158-1162">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3d158-1162">Az.Compute</span></span>
* <span data-ttu-id="3d158-1163">Добавлены командлеты Add-AzVmssVMDataDisk и Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="3d158-1163">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="3d158-1164">Get-AzVMImage отображает AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="3d158-1164">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="3d158-1165">Устранена проблема, при которой значения параметров SetAzVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="3d158-1165">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3d158-1166">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3d158-1166">Az.DataLakeStore</span></span>
* <span data-ttu-id="3d158-1167">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="3d158-1167">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="3d158-1168">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="3d158-1168">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="3d158-1169">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="3d158-1169">Az.Insights</span></span>
* <span data-ttu-id="3d158-1170">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="3d158-1170">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="3d158-1171">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="3d158-1171">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="3d158-1172">Исправлена проблема № 7513 [Insights], при которой для командлета Set-AzDiagnosticSetting требовалось явное указание категорий во время создания параметра</span><span class="sxs-lookup"><span data-stu-id="3d158-1172">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="3d158-1173">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="3d158-1173">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3d158-1174">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3d158-1174">Az.Network</span></span>
* <span data-ttu-id="3d158-1175">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="3d158-1175">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="3d158-1176">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="3d158-1176">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="3d158-1177">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="3d158-1177">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="3d158-1178">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="3d158-1178">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="3d158-1179">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="3d158-1179">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="3d158-1180">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="3d158-1180">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="3d158-1181">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="3d158-1181">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="3d158-1182">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="3d158-1182">Az.PolicyInsights</span></span>
* <span data-ttu-id="3d158-1183">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="3d158-1183">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="3d158-1184">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3d158-1184">Az.Resources</span></span>
* <span data-ttu-id="3d158-1185">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="3d158-1185">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="3d158-1186">Разрешено перечисление ресурсов с помощью параметра -ResourceId для командлета Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="3d158-1186">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="3d158-1187">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3d158-1187">Az.ServiceBus</span></span>
* <span data-ttu-id="3d158-1188">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="3d158-1188">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="3d158-1189">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3d158-1189">Az.ServiceFabric</span></span>
* <span data-ttu-id="3d158-1190">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="3d158-1190">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="3d158-1191">Исправлен командлет Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="3d158-1191">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="3d158-1192">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="3d158-1192">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="3d158-1193">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="3d158-1193">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="3d158-1194">Исправлен командлет Update-AzServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="3d158-1194">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="3d158-1195">0.4.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="3d158-1195">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="3d158-1196">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="3d158-1196">Az.Profile</span></span>
* <span data-ttu-id="3d158-1197">Устранена проблема с Get-AzSubscription в CloudShell</span><span class="sxs-lookup"><span data-stu-id="3d158-1197">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="3d158-1198">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3d158-1198">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3d158-1199">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3d158-1199">Az.Compute</span></span>
* <span data-ttu-id="3d158-1200">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzVm</span><span class="sxs-lookup"><span data-stu-id="3d158-1200">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="3d158-1201">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="3d158-1201">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3d158-1202">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3d158-1202">Az.DataLakeStore</span></span>
* <span data-ttu-id="3d158-1203">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="3d158-1203">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="3d158-1204">Get-AzDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3d158-1204">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="3d158-1205">Add-AzDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3d158-1205">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="3d158-1206">Set-AzDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3d158-1206">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="3d158-1207">Remove-AzDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3d158-1207">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3d158-1208">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3d158-1208">Az.Network</span></span>
* <span data-ttu-id="3d158-1209">Обновлен командлет Test-AzNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="3d158-1209">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="3d158-1210">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="3d158-1210">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3d158-1211">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3d158-1211">Az.Resources</span></span>
* <span data-ttu-id="3d158-1212">Устранена проблема, из-за которой командлет Get-AzRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), благодаря добавлению понятного исключения в сценарий.</span><span class="sxs-lookup"><span data-stu-id="3d158-1212">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="3d158-1213">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="3d158-1213">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="3d158-1214">0.3.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="3d158-1214">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="3d158-1215">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="3d158-1215">Azure.Storage</span></span>
* <span data-ttu-id="3d158-1216">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="3d158-1216">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="3d158-1217">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="3d158-1217">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="3d158-1218">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="3d158-1218">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="3d158-1219">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="3d158-1219">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="3d158-1220">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="3d158-1220">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="3d158-1221">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3d158-1221">Az.CognitiveServices</span></span>
* <span data-ttu-id="3d158-1222">Поддержка Get-AzCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="3d158-1222">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3d158-1223">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3d158-1223">Az.Compute</span></span>
* <span data-ttu-id="3d158-1224">Исправлена команда Get-AzVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов</span><span class="sxs-lookup"><span data-stu-id="3d158-1224">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="3d158-1225">Добавлен пример использования SimpleParameterSet в справку командлета New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="3d158-1225">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="3d158-1226">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="3d158-1226">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="3d158-1227">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="3d158-1227">Az.DataFactoryV2</span></span>
* <span data-ttu-id="3d158-1228">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="3d158-1228">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3d158-1229">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3d158-1229">Az.Network</span></span>
* <span data-ttu-id="3d158-1230">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="3d158-1230">Added NetworkProfile functionality.</span></span> <span data-ttu-id="3d158-1231">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="3d158-1231">new cmdlets added</span></span>
    - <span data-ttu-id="3d158-1232">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3d158-1232">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="3d158-1233">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3d158-1233">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="3d158-1234">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3d158-1234">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="3d158-1235">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3d158-1235">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="3d158-1236">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="3d158-1236">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="3d158-1237">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="3d158-1237">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="3d158-1238">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="3d158-1238">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="3d158-1239">Добавлены командлеты: New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="3d158-1239">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="3d158-1240">Добавлены командлеты: Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="3d158-1240">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="3d158-1241">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="3d158-1241">Az.RedisCache</span></span>
* <span data-ttu-id="3d158-1242">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="3d158-1242">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="3d158-1243">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="3d158-1243">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="3d158-1244">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3d158-1244">Az.Resources</span></span>
* <span data-ttu-id="3d158-1245">Добавлен отсутствующий параметр -Mode в командлет Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3d158-1245">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="3d158-1246">Исправлена ошибка командлета Get-AzProviderOperation для операций, когда Origin содержит User</span><span class="sxs-lookup"><span data-stu-id="3d158-1246">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="3d158-1247">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3d158-1247">Az.Sql</span></span>
* <span data-ttu-id="3d158-1248">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="3d158-1248">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3d158-1249">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3d158-1249">Az.Websites</span></span>
* <span data-ttu-id="3d158-1250">Новый командлет Get-AzWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="3d158-1250">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="3d158-1251">Новые командлеты New-AzWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows</span><span class="sxs-lookup"><span data-stu-id="3d158-1251">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="3d158-1252">0.2.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="3d158-1252">0.2.0 - September 2018</span></span>
 <span data-ttu-id="3d158-1253">Первый выпуск</span><span class="sxs-lookup"><span data-stu-id="3d158-1253">Initial Release</span></span>