---
ms.openlocfilehash: 179d22fa065944695e4769f2698e3cabc7666b04
ms.sourcegitcommit: c6fd0e490fa0e33b8b768b679682a47d8faae1cf
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/16/2019
ms.locfileid: "54342153"
---
## <a name="110---january-2019"></a><span data-ttu-id="479fc-101">1.1.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="479fc-101">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="479fc-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="479fc-102">Az.Accounts</span></span>
* <span data-ttu-id="479fc-103">Добавление области "Local" в Enable-AzureRmAlias.</span><span class="sxs-lookup"><span data-stu-id="479fc-103">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="479fc-104">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="479fc-104">Az.Compute</span></span>
* <span data-ttu-id="479fc-105">Теперь имя не является обязательным в идентификаторе набора параметров для Restart/Start/Stop/Remove/Set-AzVM и Save-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="479fc-105">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="479fc-106">Обновлено описание идентификатора в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="479fc-106">Updated the description of ID in help files</span></span>
* <span data-ttu-id="479fc-107">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="479fc-107">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="479fc-108">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="479fc-108">Az.DataLakeStore</span></span>
* <span data-ttu-id="479fc-109">Обновление версии пакета SDK для плоскости данных до 1.1.14 для устранения найденных проблем.</span><span class="sxs-lookup"><span data-stu-id="479fc-109">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="479fc-110">Исправлена обработка отрицательного времени доступа и времени изменения для getfilestatus и liststatus, исправлен токен отмены для асинхронных методов.</span><span class="sxs-lookup"><span data-stu-id="479fc-110">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="479fc-111">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="479fc-111">Az.EventGrid</span></span>
* <span data-ttu-id="479fc-112">Обновление для использования API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="479fc-112">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="479fc-113">Обновлены указанные ниже командлеты для поддержки нового сценария в API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="479fc-113">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="479fc-114">New-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="479fc-114">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="479fc-115">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="479fc-115">Event Time-To-Live,</span></span>
        - <span data-ttu-id="479fc-116">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="479fc-116">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="479fc-117">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="479fc-117">Dead letter endpoint.</span></span>
    - <span data-ttu-id="479fc-118">Update-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="479fc-118">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="479fc-119">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="479fc-119">Event Time-To-Live,</span></span>
        - <span data-ttu-id="479fc-120">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="479fc-120">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="479fc-121">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="479fc-121">Dead letter endpoint.</span></span>
* <span data-ttu-id="479fc-122">Для параметра EndpointType добавлены новые значения перечисления (storageQueue и hybridConnection) в командлеты New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="479fc-122">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="479fc-123">Если ожидается, что создание или обновление подписки на событие повлечет за собой действия со стороны пользователя, выполняемые вручную, отображается предупреждение при создании или обновлении подписки события.</span><span class="sxs-lookup"><span data-stu-id="479fc-123">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="479fc-124">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="479fc-124">Az.IotHub</span></span>
* <span data-ttu-id="479fc-125">Пакет SDK Центра Интернета вещей обновлен до последней версии.</span><span class="sxs-lookup"><span data-stu-id="479fc-125">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="479fc-126">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="479fc-126">Az.LogicApp</span></span>
* <span data-ttu-id="479fc-127">Get-AzLogicApp позволяет перечислить все параметры без указанного имени.</span><span class="sxs-lookup"><span data-stu-id="479fc-127">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="479fc-128">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="479fc-128">Az.Resources</span></span>
* <span data-ttu-id="479fc-129">Исправлена проблема с набором параметров при предоставлении параметров "-ODataQuery" и "-ResourceId" для "Get-AzResource".</span><span class="sxs-lookup"><span data-stu-id="479fc-129">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="479fc-130">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7875.</span><span class="sxs-lookup"><span data-stu-id="479fc-130">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="479fc-131">Исправлена обработка параметра -Custom в New/Set-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="479fc-131">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="479fc-132">Исправлена опечатка в документации по New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="479fc-132">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="479fc-133">Параметр "-MailNickname" стал обязательным для "New-AzADUser".</span><span class="sxs-lookup"><span data-stu-id="479fc-133">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="479fc-134">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8220.</span><span class="sxs-lookup"><span data-stu-id="479fc-134">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="479fc-135">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="479fc-135">Az.SignalR</span></span>
* <span data-ttu-id="479fc-136">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="479fc-136">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="479fc-137">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="479fc-137">Az.Sql</span></span>
* <span data-ttu-id="479fc-138">Зависимость клиента управления хранением преобразована для общей реализации в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="479fc-138">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="479fc-139">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="479fc-139">Az.Storage</span></span>
* <span data-ttu-id="479fc-140">Установка параметра StorageAccountName для контекста хранилища в качестве реального имени учетной записи хранения, если она была создана с использованием токена Sas, OAuth или анонимного доступа.</span><span class="sxs-lookup"><span data-stu-id="479fc-140">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="479fc-141">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="479fc-141">New-AzStorageContext</span></span>
* <span data-ttu-id="479fc-142">Создание токена Sas большого двоичного объекта моментального снимка с параметром "-FullUri". Возвращаемый URI исправлен на URI моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="479fc-142">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="479fc-143">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="479fc-143">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="479fc-144">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="479fc-144">Az.Websites</span></span>
* <span data-ttu-id="479fc-145">Исправлена ошибка синтаксического анализа даты в "Get-AzDeletedWebApp".</span><span class="sxs-lookup"><span data-stu-id="479fc-145">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="479fc-146">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="479fc-146">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="479fc-147">1.0.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="479fc-147">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="479fc-148">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="479fc-148">General</span></span>

- <span data-ttu-id="479fc-149">Общедоступная версия модуля Az.</span><span class="sxs-lookup"><span data-stu-id="479fc-149">General Availability of Az Module</span></span>
- <span data-ttu-id="479fc-150">Справка в Интернете для каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="479fc-150">Online help for each module</span></span>
- <span data-ttu-id="479fc-151">Дополнительные сведения и стратегию развития см. в статье [Announcing New Module 'Az'](https://aka.ms/azps-announce) (Объявление о новом модуле Az)</span><span class="sxs-lookup"><span data-stu-id="479fc-151">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="479fc-152">Сведения о миграции с AzureRM см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="479fc-152">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="479fc-153">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="479fc-153">Az.Accounts</span></span>
- <span data-ttu-id="479fc-154">Изменено с Az.Profile.</span><span class="sxs-lookup"><span data-stu-id="479fc-154">Changed from Az.Profile</span></span>
- <span data-ttu-id="479fc-155">Исправлены форматы таблиц для типов профиля и контекста.</span><span class="sxs-lookup"><span data-stu-id="479fc-155">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="479fc-156">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="479fc-156">Az.ApiManagement</span></span>
- <span data-ttu-id="479fc-157">Исправления для #7002.</span><span class="sxs-lookup"><span data-stu-id="479fc-157">Fixes for #7002</span></span>
- <span data-ttu-id="479fc-158">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="479fc-158">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="479fc-159">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="479fc-159">Az.Batch</span></span>
- <span data-ttu-id="479fc-160">Добавлена возможность видеть, какая версия агента узла пакетной службы Azure работает в пуле на каждой виртуальной машине, с помощью нового свойства `NodeAgentInformation` в `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="479fc-160">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="479fc-161">Значение `Caching` по умолчанию для `PSDataDisk` теперь `ReadWrite` вместо `None`.</span><span class="sxs-lookup"><span data-stu-id="479fc-161">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="479fc-162">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="479fc-162">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="479fc-163">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="479fc-163">Az.Billing</span></span>
- <span data-ttu-id="479fc-164">Объединены командлеты Billing, Consumption и UsageAggregates. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0).</span><span class="sxs-lookup"><span data-stu-id="479fc-164">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="479fc-165">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="479fc-165">Az.CognitivServices</span></span>
- <span data-ttu-id="479fc-166">Добавлены средства заполнения для SkuName и Typem, доступные в операции New-AzureRmCognitiveServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="479fc-166">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="479fc-167">Удален набор параметров GetSkusWithAccountParamSetName из Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="479fc-167">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="479fc-168">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="479fc-168">Az.ContainerInstance</span></span>
- <span data-ttu-id="479fc-169">Добавлена поддержка ManagedIdentity.</span><span class="sxs-lookup"><span data-stu-id="479fc-169">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="479fc-170">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="479fc-170">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="479fc-171">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="479fc-171">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="479fc-172">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="479fc-172">Az.DataLakeStore</span></span>
- <span data-ttu-id="479fc-173">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="479fc-173">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="479fc-174">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="479fc-174">Az.Monitor</span></span>
- <span data-ttu-id="479fc-175">"Az.Insights" переименован в "Az.Monitor" и внесены другие незначительные критические изменения. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="479fc-175">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="479fc-176">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="479fc-176">Az.KeyVault</span></span>
- <span data-ttu-id="479fc-177">Из типов вывода удалено устаревшее свойство PurgeDisabled</span><span class="sxs-lookup"><span data-stu-id="479fc-177">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="479fc-178">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="479fc-178">Az.MachineLearning</span></span>
- <span data-ttu-id="479fc-179">Включены командлеты из модуля Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="479fc-179">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="479fc-180">Az.Media</span><span class="sxs-lookup"><span data-stu-id="479fc-180">Az.Media</span></span>
- <span data-ttu-id="479fc-181">Удаляет устаревший псевдоним Tags из New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="479fc-181">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="479fc-182">Az.Network</span><span class="sxs-lookup"><span data-stu-id="479fc-182">Az.Network</span></span>
<span data-ttu-id="479fc-183">В шлюз приложений добавлена поддержка настройки RewriteRuleSets</span><span class="sxs-lookup"><span data-stu-id="479fc-183">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="479fc-184">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="479fc-184">New cmdlets added:</span></span>
        - <span data-ttu-id="479fc-185">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="479fc-185">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="479fc-186">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="479fc-186">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="479fc-187">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="479fc-187">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="479fc-188">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="479fc-188">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="479fc-189">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="479fc-189">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="479fc-190">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="479fc-190">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="479fc-191">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="479fc-191">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="479fc-192">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="479fc-192">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="479fc-193">В следующие командлеты добавлен необязательный параметр -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="479fc-193">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="479fc-194">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="479fc-194">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="479fc-195">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="479fc-195">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="479fc-196">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="479fc-196">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="479fc-197">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="479fc-197">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="479fc-198">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="479fc-198">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="479fc-199">New-AzureRmApplicationGatewayUrlPathMapConfig добавил с помощью идентификатора поддержку KeyVault для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="479fc-199">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="479fc-200">В следующие командлеты добавлен необязательный параметр -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="479fc-200">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="479fc-201">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="479fc-201">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="479fc-202">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="479fc-202">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="479fc-203">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="479fc-203">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="479fc-204">В командлет New-AzApplicationGateway добавлен необязательный параметр -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="479fc-204">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="479fc-205">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="479fc-205">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="479fc-206">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="479fc-206">Az.OperationalInsights</span></span>
- <span data-ttu-id="479fc-207">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="479fc-207">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="479fc-208">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="479fc-208">Az.Profile</span></span>
- <span data-ttu-id="479fc-209">Имя модуля изменено на Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="479fc-209">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="479fc-210">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="479fc-210">Az.RecoveryServices</span></span>
- <span data-ttu-id="479fc-211">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="479fc-211">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="479fc-212">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="479fc-212">Az.Resources</span></span>
- <span data-ttu-id="479fc-213">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="479fc-213">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="479fc-214">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="479fc-214">Az.ServiceFabric</span></span>
- <span data-ttu-id="479fc-215">Поддержка спецификации сертификата по общему имени и отпечатку</span><span class="sxs-lookup"><span data-stu-id="479fc-215">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="479fc-216">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="479fc-216">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="479fc-217">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="479fc-217">Az.SIgnalR</span></span>
- <span data-ttu-id="479fc-218">Общедоступная версия командлетов PowerShell для SIgnalR</span><span class="sxs-lookup"><span data-stu-id="479fc-218">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="479fc-219">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="479fc-219">Az.Sql</span></span>
- <span data-ttu-id="479fc-220">Добавлены новые типы обнаружения Data_Exfiltration и Unsafe_Action в командлеты обнаружения угроз</span><span class="sxs-lookup"><span data-stu-id="479fc-220">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="479fc-221">Примеры обновленной документации для командлетов аудита Sql</span><span class="sxs-lookup"><span data-stu-id="479fc-221">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="479fc-222">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="479fc-222">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="479fc-223">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="479fc-223">Az.Storage</span></span>
- <span data-ttu-id="479fc-224">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="479fc-224">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="479fc-225">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="479fc-225">Az.Websites</span></span>
- <span data-ttu-id="479fc-226">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="479fc-226">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="479fc-227">0.7.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="479fc-227">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="479fc-228">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="479fc-228">General</span></span>

* <span data-ttu-id="479fc-229">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="479fc-229">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="479fc-230">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="479fc-230">Az.Compute</span></span>

* <span data-ttu-id="479fc-231">Добавлена поддержка UltraSSD и образов коллекции в простых наборах параметров для командлетов `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="479fc-231">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="479fc-232">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="479fc-232">Az.DataLakeStore</span></span>

* <span data-ttu-id="479fc-233">Исправлено косую черту в конце домена учетной записи ADLS</span><span class="sxs-lookup"><span data-stu-id="479fc-233">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="479fc-234">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="479fc-234">Az.FrontDoor</span></span>

* <span data-ttu-id="479fc-235">Исправлены некоторые неработающие ссылки</span><span class="sxs-lookup"><span data-stu-id="479fc-235">Fixed some broken links</span></span>
    - <span data-ttu-id="479fc-236">В статьях New-AzureRmFrontDoor и Set-AzureRmFrontDoor исправлена ссылка на статью командлета New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="479fc-236">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="479fc-237">В статье New-AzureRmFrontDoorManagedRuleObject исправлена ссылка на статью командлета New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="479fc-237">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="479fc-238">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="479fc-238">Az.RecoveryServices</span></span>

* <span data-ttu-id="479fc-239">Добавлены проверки на стороне клиента для операций восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="479fc-239">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="479fc-240">StorageAccountName и storageAccountResourceGroupName являются необязательными для восстановления afs.</span><span class="sxs-lookup"><span data-stu-id="479fc-240">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="479fc-241">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="479fc-241">Az.Resources</span></span>

* <span data-ttu-id="479fc-242">Исправление для https://github.com/Azure/azure-powershell/issues/7679.</span><span class="sxs-lookup"><span data-stu-id="479fc-242">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="479fc-243">Обновите Get-AzureRmRoleAssignment, чтобы использовать область подписки, если она указана при запросе классических администраторов.</span><span class="sxs-lookup"><span data-stu-id="479fc-243">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="479fc-244">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="479fc-244">Az.Sql</span></span>

* <span data-ttu-id="479fc-245">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="479fc-245">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="479fc-246">Устранена проблема с использованием Get-AzureRmSqlDatabaseVulnerabilityAssessment с .NET Core.</span><span class="sxs-lookup"><span data-stu-id="479fc-246">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="479fc-247">Изменена документация справочных сообщений, связанных с командлетами аудита SQL.</span><span class="sxs-lookup"><span data-stu-id="479fc-247">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="479fc-248">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="479fc-248">Az.Storage</span></span>

* <span data-ttu-id="479fc-249">Добавлено -EnableHierarchicalNamespace к New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="479fc-249">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="479fc-250">Устранена проблема, из-за которой командлет Copy File не может повторно использовать исходный контекст в пункте назначения, если не введен -DestContext</span><span class="sxs-lookup"><span data-stu-id="479fc-250">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="479fc-251">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="479fc-251">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="479fc-252">Поддержка статической конфигурации сайта</span><span class="sxs-lookup"><span data-stu-id="479fc-252">Support Static Website configuration</span></span>
    - <span data-ttu-id="479fc-253">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="479fc-253">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="479fc-254">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="479fc-254">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="479fc-255">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="479fc-255">Az.Websites</span></span>

* <span data-ttu-id="479fc-256">Set-AzureRmWebApp и Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="479fc-256">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="479fc-257">Добавлен новый параметр (-AzureStoragePath), который указывает путь службы хранилища Azure для подключения в приложениях-контейнерах Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="479fc-257">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="479fc-258">Используйте выходные данные нового командлета New-AzureRmWebAppAzureStoragePath в качестве параметра, чтобы задать пути к службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="479fc-258">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="479fc-259">0.6.1 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="479fc-259">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="479fc-260">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="479fc-260">Az.ApiManagement</span></span>
* <span data-ttu-id="479fc-261">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="479fc-261">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="479fc-262">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="479fc-262">Az.Automation</span></span>
* <span data-ttu-id="479fc-263">Командлеты службы автоматизации Azure на базе Swagger.</span><span class="sxs-lookup"><span data-stu-id="479fc-263">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="479fc-264">Добавлены командлеты для Управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="479fc-264">Added Update Management cmdlets</span></span>
* <span data-ttu-id="479fc-265">Добавлены командлеты для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="479fc-265">Added Source Control cmdlets</span></span>
* <span data-ttu-id="479fc-266">Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="479fc-266">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="479fc-267">Исправлена команда DSC для регистрации узла.</span><span class="sxs-lookup"><span data-stu-id="479fc-267">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="479fc-268">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="479fc-268">Az.Compute</span></span>
* <span data-ttu-id="479fc-269">Исправлена проблема с удостоверением, назначаемым системой.</span><span class="sxs-lookup"><span data-stu-id="479fc-269">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="479fc-270">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="479fc-270">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="479fc-271">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="479fc-271">Az.ContainerInstance</span></span>
* <span data-ttu-id="479fc-272">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="479fc-272">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="479fc-273">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="479fc-273">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="479fc-274">Обновлено описание в примерах командлетов для Marketplace.</span><span class="sxs-lookup"><span data-stu-id="479fc-274">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="479fc-275">Az.Network</span><span class="sxs-lookup"><span data-stu-id="479fc-275">Az.Network</span></span>
* <span data-ttu-id="479fc-276">Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="479fc-276">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="479fc-277">Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="479fc-277">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="479fc-278">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="479fc-278">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="479fc-279">Исправлены проблемы с использованием памяти в карте виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="479fc-279">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="479fc-280">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="479fc-280">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="479fc-281">Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="479fc-281">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="479fc-282">Параметры часового пояса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="479fc-282">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="479fc-283">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="479fc-283">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="479fc-284">Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="479fc-284">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="479fc-285">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="479fc-285">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="479fc-286">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="479fc-286">Az.Relay</span></span>
* <span data-ttu-id="479fc-287">Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.</span><span class="sxs-lookup"><span data-stu-id="479fc-287">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="479fc-288">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="479fc-288">Az.Resources</span></span>
* <span data-ttu-id="479fc-289">Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.</span><span class="sxs-lookup"><span data-stu-id="479fc-289">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="479fc-290">Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.</span><span class="sxs-lookup"><span data-stu-id="479fc-290">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="479fc-291">Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.</span><span class="sxs-lookup"><span data-stu-id="479fc-291">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="479fc-292">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="479fc-292">Az.ServiceFabric</span></span>
* <span data-ttu-id="479fc-293">Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.</span><span class="sxs-lookup"><span data-stu-id="479fc-293">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="479fc-294">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="479fc-294">Az.Sql</span></span>
* <span data-ttu-id="479fc-295">Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="479fc-295">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="479fc-296">Get-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="479fc-296">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="479fc-297">New-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="479fc-297">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="479fc-298">Set-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="479fc-298">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="479fc-299">Remove-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="479fc-299">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="479fc-300">Get-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="479fc-300">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="479fc-301">New-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="479fc-301">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="479fc-302">Restore-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="479fc-302">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="479fc-303">Remove-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="479fc-303">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="479fc-304">Добавлено расширенное управление политиками аудита для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="479fc-304">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="479fc-305">Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="479fc-305">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="479fc-306">Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.</span><span class="sxs-lookup"><span data-stu-id="479fc-306">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="479fc-307">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="479fc-307">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="479fc-308">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="479fc-308">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="479fc-309">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="479fc-309">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="479fc-310">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="479fc-310">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="479fc-311">Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="479fc-311">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="479fc-312">0.5.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="479fc-312">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="479fc-313">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="479fc-313">General</span></span>
* <span data-ttu-id="479fc-314">Добавлены средства заполнения ресурсов для многих основных командлетов — они позволяют вам переключать существующие имена ресурсов при вызове командлетов в интерактивном режиме</span><span class="sxs-lookup"><span data-stu-id="479fc-314">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="479fc-315">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="479fc-315">Az.Profile</span></span>
* <span data-ttu-id="479fc-316">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="479fc-316">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="479fc-317">В командлете Connect-AzAccount параметр TenantId переименован в Tenant и добавлен псевдоним для TenantId</span><span class="sxs-lookup"><span data-stu-id="479fc-317">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="479fc-318">Обновлено описание TenantId для командлета Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="479fc-318">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="479fc-319">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="479fc-319">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="479fc-320">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="479fc-320">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="479fc-321">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="479fc-321">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="479fc-322">Устранена проблема, при которой командлет Disconnect-AzAccount вызывал сбой при отсутствии подключения</span><span class="sxs-lookup"><span data-stu-id="479fc-322">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="479fc-323">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="479fc-323">Az.CognitiveServices</span></span>
* <span data-ttu-id="479fc-324">Добавлена операция Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="479fc-324">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="479fc-325">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="479fc-325">Az.Compute</span></span>
* <span data-ttu-id="479fc-326">Добавлены командлеты Add-AzVmssVMDataDisk и Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="479fc-326">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="479fc-327">Get-AzVMImage отображает AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="479fc-327">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="479fc-328">Устранена проблема, при которой значения параметров SetAzVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="479fc-328">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="479fc-329">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="479fc-329">Az.DataLakeStore</span></span>
* <span data-ttu-id="479fc-330">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="479fc-330">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="479fc-331">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="479fc-331">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="479fc-332">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="479fc-332">Az.Insights</span></span>
* <span data-ttu-id="479fc-333">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="479fc-333">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="479fc-334">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="479fc-334">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="479fc-335">Исправлена проблема № 7513 [Insights], при которой для командлета Set-AzDiagnosticSetting требовалось явное указание категорий во время создания параметра</span><span class="sxs-lookup"><span data-stu-id="479fc-335">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="479fc-336">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="479fc-336">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="479fc-337">Az.Network</span><span class="sxs-lookup"><span data-stu-id="479fc-337">Az.Network</span></span>
* <span data-ttu-id="479fc-338">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="479fc-338">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="479fc-339">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="479fc-339">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="479fc-340">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="479fc-340">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="479fc-341">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="479fc-341">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="479fc-342">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="479fc-342">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="479fc-343">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="479fc-343">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="479fc-344">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="479fc-344">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="479fc-345">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="479fc-345">Az.PolicyInsights</span></span>
* <span data-ttu-id="479fc-346">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="479fc-346">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="479fc-347">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="479fc-347">Az.Resources</span></span>
* <span data-ttu-id="479fc-348">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="479fc-348">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="479fc-349">Разрешено перечисление ресурсов с помощью параметра -ResourceId для командлета Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="479fc-349">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="479fc-350">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="479fc-350">Az.ServiceBus</span></span>
* <span data-ttu-id="479fc-351">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="479fc-351">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="479fc-352">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="479fc-352">Az.ServiceFabric</span></span>
* <span data-ttu-id="479fc-353">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="479fc-353">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="479fc-354">Исправлен командлет Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="479fc-354">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="479fc-355">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="479fc-355">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="479fc-356">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="479fc-356">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="479fc-357">Исправлен командлет Update-AzServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="479fc-357">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="479fc-358">0.4.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="479fc-358">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="479fc-359">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="479fc-359">Az.Profile</span></span>
* <span data-ttu-id="479fc-360">Устранена проблема с Get-AzSubscription в CloudShell</span><span class="sxs-lookup"><span data-stu-id="479fc-360">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="479fc-361">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="479fc-361">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="479fc-362">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="479fc-362">Az.Compute</span></span>
* <span data-ttu-id="479fc-363">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzVm</span><span class="sxs-lookup"><span data-stu-id="479fc-363">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="479fc-364">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="479fc-364">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="479fc-365">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="479fc-365">Az.DataLakeStore</span></span>
* <span data-ttu-id="479fc-366">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="479fc-366">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="479fc-367">Get-AzDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="479fc-367">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="479fc-368">Add-AzDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="479fc-368">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="479fc-369">Set-AzDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="479fc-369">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="479fc-370">Remove-AzDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="479fc-370">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="479fc-371">Az.Network</span><span class="sxs-lookup"><span data-stu-id="479fc-371">Az.Network</span></span>
* <span data-ttu-id="479fc-372">Обновлен командлет Test-AzNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="479fc-372">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="479fc-373">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="479fc-373">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="479fc-374">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="479fc-374">Az.Resources</span></span>
* <span data-ttu-id="479fc-375">Устранена проблема, из-за которой командлет Get-AzRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), благодаря добавлению понятного исключения в сценарий.</span><span class="sxs-lookup"><span data-stu-id="479fc-375">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="479fc-376">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="479fc-376">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="479fc-377">0.3.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="479fc-377">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="479fc-378">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="479fc-378">Azure.Storage</span></span>
* <span data-ttu-id="479fc-379">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="479fc-379">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="479fc-380">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="479fc-380">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="479fc-381">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="479fc-381">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="479fc-382">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="479fc-382">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="479fc-383">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="479fc-383">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="479fc-384">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="479fc-384">Az.CognitiveServices</span></span>
* <span data-ttu-id="479fc-385">Поддержка Get-AzCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="479fc-385">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="479fc-386">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="479fc-386">Az.Compute</span></span>
* <span data-ttu-id="479fc-387">Исправлена команда Get-AzVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов</span><span class="sxs-lookup"><span data-stu-id="479fc-387">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="479fc-388">Добавлен пример использования SimpleParameterSet в справку командлета New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="479fc-388">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="479fc-389">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="479fc-389">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="479fc-390">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="479fc-390">Az.DataFactoryV2</span></span>
* <span data-ttu-id="479fc-391">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="479fc-391">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="479fc-392">Az.Network</span><span class="sxs-lookup"><span data-stu-id="479fc-392">Az.Network</span></span>
* <span data-ttu-id="479fc-393">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="479fc-393">Added NetworkProfile functionality.</span></span> <span data-ttu-id="479fc-394">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="479fc-394">new cmdlets added</span></span>
    - <span data-ttu-id="479fc-395">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="479fc-395">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="479fc-396">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="479fc-396">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="479fc-397">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="479fc-397">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="479fc-398">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="479fc-398">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="479fc-399">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="479fc-399">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="479fc-400">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="479fc-400">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="479fc-401">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="479fc-401">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="479fc-402">Добавлены командлеты: New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="479fc-402">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="479fc-403">Добавлены командлеты: Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="479fc-403">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="479fc-404">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="479fc-404">Az.RedisCache</span></span>
* <span data-ttu-id="479fc-405">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="479fc-405">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="479fc-406">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="479fc-406">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="479fc-407">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="479fc-407">Az.Resources</span></span>
* <span data-ttu-id="479fc-408">Добавлен отсутствующий параметр -Mode в командлет Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="479fc-408">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="479fc-409">Исправлена ошибка командлета Get-AzProviderOperation для операций, когда Origin содержит User</span><span class="sxs-lookup"><span data-stu-id="479fc-409">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="479fc-410">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="479fc-410">Az.Sql</span></span>
* <span data-ttu-id="479fc-411">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="479fc-411">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="479fc-412">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="479fc-412">Az.Websites</span></span>
* <span data-ttu-id="479fc-413">Новый командлет Get-AzWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="479fc-413">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="479fc-414">Новые командлеты New-AzWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows</span><span class="sxs-lookup"><span data-stu-id="479fc-414">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="479fc-415">0.2.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="479fc-415">0.2.0 - September 2018</span></span>
 <span data-ttu-id="479fc-416">Первый выпуск</span><span class="sxs-lookup"><span data-stu-id="479fc-416">Initial Release</span></span>