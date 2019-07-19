---
ms.openlocfilehash: f357a17f698d68c1a29dcb78f83671973fd6ecad
ms.sourcegitcommit: 0b644bfecf4224b2ea83520d1a6a956734d9fba4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/12/2019
ms.locfileid: "67863741"
---
## <a name="240---july-2019"></a><span data-ttu-id="f22d8-101">2.4.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f22d8-101">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f22d8-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f22d8-102">Az.Accounts</span></span>
* <span data-ttu-id="f22d8-103">Добавлена поддержка командлетов профиля.</span><span class="sxs-lookup"><span data-stu-id="f22d8-103">Add support for profile cmdlets</span></span>
* <span data-ttu-id="f22d8-104">Добавлена поддержка сред и плоскостей данных в созданных командлетах.</span><span class="sxs-lookup"><span data-stu-id="f22d8-104">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="f22d8-105">Исправлена ошибка, когда в командлетах плоскости данных в Windows PowerShell в некоторых случаях использовалась неправильная конечная точка.</span><span class="sxs-lookup"><span data-stu-id="f22d8-105">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="f22d8-106">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="f22d8-106">Az.Advisor</span></span>
* <span data-ttu-id="f22d8-107">Выпущена общедоступная версия Az.Advisor.</span><span class="sxs-lookup"><span data-stu-id="f22d8-107">GA release of Az.Advisor</span></span>
* <span data-ttu-id="f22d8-108">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="f22d8-108">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f22d8-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f22d8-109">Az.ApiManagement</span></span>
* <span data-ttu-id="f22d8-110">исправлена проблема https://github.com/Azure/azure-powershell/issues/8671.</span><span class="sxs-lookup"><span data-stu-id="f22d8-110">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="f22d8-111">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="f22d8-111">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="f22d8-112">Добавлена поддержка запрашивания подписок по пользователю и продукту.</span><span class="sxs-lookup"><span data-stu-id="f22d8-112">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="f22d8-113">Добавлена поддержка создания запросов с использованием области "/", "/apis", "/apis/echo-api".</span><span class="sxs-lookup"><span data-stu-id="f22d8-113">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="f22d8-114">Исправлены проблемы https://github.com/Azure/azure-powershell/issues/9307 и https://github.com/Azure/azure-powershell/issues/8432.</span><span class="sxs-lookup"><span data-stu-id="f22d8-114">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="f22d8-115">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="f22d8-115">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="f22d8-116">Добавлена поддержка указания ApiVersion и ApiVersionSetId при импорте API-интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="f22d8-116">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f22d8-117">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f22d8-117">Az.Automation</span></span>
* <span data-ttu-id="f22d8-118">Исправлена ошибка командлета Set-AzAutomationConnectionFieldValue при обработке строкового значения.</span><span class="sxs-lookup"><span data-stu-id="f22d8-118">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22d8-119">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22d8-119">Az.Compute</span></span>
* <span data-ttu-id="f22d8-120">В New AzImageConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="f22d8-120">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f22d8-121">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f22d8-121">Az.DataFactory</span></span>
* <span data-ttu-id="f22d8-122">Обновление выходных данных командлетов ADF, предназначенных для получения числа выполнений действий, конвейеров и триггеров, для поддержки канала Select-Object.</span><span class="sxs-lookup"><span data-stu-id="f22d8-122">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f22d8-123">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f22d8-123">Az.EventGrid</span></span>
* <span data-ttu-id="f22d8-124">Исправлена опечатка в документации по командлету New-AzEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="f22d8-124">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f22d8-125">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f22d8-125">Az.IotHub</span></span>
* <span data-ttu-id="f22d8-126">Добавлена поддержка повторного создания ключей политики авторизации.</span><span class="sxs-lookup"><span data-stu-id="f22d8-126">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f22d8-127">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22d8-127">Az.Network</span></span>
* <span data-ttu-id="f22d8-128">К тегам общедоступного IP-адреса добавлен тег RoutingPreference.</span><span class="sxs-lookup"><span data-stu-id="f22d8-128">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="f22d8-129">Улучшены примеры для справочной документации по командлету Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="f22d8-129">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f22d8-130">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f22d8-130">Az.PolicyInsights</span></span>
* <span data-ttu-id="f22d8-131">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="f22d8-131">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="f22d8-132">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9446.</span><span class="sxs-lookup"><span data-stu-id="f22d8-132">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f22d8-133">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f22d8-133">Az.OperationalInsights</span></span>
* <span data-ttu-id="f22d8-134">Исправленная модель источника данных CustomLog возвращена в командлет Get-AzOperationalInsightsDataSource.</span><span class="sxs-lookup"><span data-stu-id="f22d8-134">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f22d8-135">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f22d8-135">Az.RecoveryServices</span></span>
* <span data-ttu-id="f22d8-136">Выпущено исправление для команды get-policy для виртуальных машин IaaS.</span><span class="sxs-lookup"><span data-stu-id="f22d8-136">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="f22d8-137">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22d8-137">Az.Resources</span></span>
    - <span data-ttu-id="f22d8-138">Исправлен текст справки по параметру Get-AzPolicyState -Top.</span><span class="sxs-lookup"><span data-stu-id="f22d8-138">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="f22d8-139">Добавлена поддержка разбиения по страницам на стороне клиента для Get-AzPolicyAlias.</span><span class="sxs-lookup"><span data-stu-id="f22d8-139">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="f22d8-140">Добавлены новые параметры для Set-AzPolicyAssignment, -PolicyParameters и -PolicyParametersObject.</span><span class="sxs-lookup"><span data-stu-id="f22d8-140">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="f22d8-141">Добавлен ряд обновлений документов и примеров для командлетов политик.</span><span class="sxs-lookup"><span data-stu-id="f22d8-141">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f22d8-142">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f22d8-142">Az.ServiceBus</span></span>
* <span data-ttu-id="f22d8-143">Исправление ошибки № 4938: командлет New-AzureRmServiceBusQueue возвращает ответ BadRequest (Недопустимый запрос) при задании значения MaxSizeInMegabytes.</span><span class="sxs-lookup"><span data-stu-id="f22d8-143">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="f22d8-144">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22d8-144">Az.Sql</span></span>
* <span data-ttu-id="f22d8-145">Из выпуска предварительной версии в выпуск общедоступной версии добавлены командлеты группы отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f22d8-145">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="f22d8-146">Поддержка аудита Azure SQL Server и баз данных с помощью новых командлетов:</span><span class="sxs-lookup"><span data-stu-id="f22d8-146">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="f22d8-147">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="f22d8-147">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="f22d8-148">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="f22d8-148">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="f22d8-149">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="f22d8-149">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="f22d8-150">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="f22d8-150">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="f22d8-151">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="f22d8-151">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="f22d8-152">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="f22d8-152">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="f22d8-153">Из параметров оценки уязвимостей удалены ограничения, касающиеся электронной почты.</span><span class="sxs-lookup"><span data-stu-id="f22d8-153">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f22d8-154">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f22d8-154">Az.Storage</span></span>
* <span data-ttu-id="f22d8-155">Два параметра в указанном ниже командлете — -IndexDocument и -ErrorDocument404Path, — которые ранее были обязательными, стали необязательными:</span><span class="sxs-lookup"><span data-stu-id="f22d8-155">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="f22d8-156">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="f22d8-156">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="f22d8-157">Обновлена справка по командлету Get-AzStorageBlobContent: добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="f22d8-157">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="f22d8-158">При сбое выполнения командлета с ошибкой StorageException отображаются дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="f22d8-158">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="f22d8-159">Добавлена поддержка создания или обновления учетной записи хранения с использованием проверки подлинности AAD DS для службы "Файлы Azure".</span><span class="sxs-lookup"><span data-stu-id="f22d8-159">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="f22d8-160">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f22d8-160">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="f22d8-161">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f22d8-161">Set-AzStorageAccount</span></span>
* <span data-ttu-id="f22d8-162">Добавлена поддержка перечисления или закрытия дескрипторов файлов для общей папки, каталога файлов или файла:</span><span class="sxs-lookup"><span data-stu-id="f22d8-162">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="f22d8-163">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="f22d8-163">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="f22d8-164">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="f22d8-164">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="f22d8-165">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="f22d8-165">Az.StorageSync</span></span>
* <span data-ttu-id="f22d8-166">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="f22d8-166">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="f22d8-167">2.3.2 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f22d8-167">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f22d8-168">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f22d8-168">Az.Accounts</span></span>
* <span data-ttu-id="f22d8-169">Исправлена ошибка, связанная с использованием неправильного URL-адреса для вызовов функций.</span><span class="sxs-lookup"><span data-stu-id="f22d8-169">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="f22d8-170">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8983.</span><span class="sxs-lookup"><span data-stu-id="f22d8-170">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="f22d8-171">Устранена проблема с псевдонимами из AzureRM для командлетов Az.</span><span class="sxs-lookup"><span data-stu-id="f22d8-171">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="f22d8-172">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="f22d8-172">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="f22d8-173">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest.</span><span class="sxs-lookup"><span data-stu-id="f22d8-173">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22d8-174">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22d8-174">Az.Compute</span></span>
* <span data-ttu-id="f22d8-175">Простые наборы параметров New-AzVm и New-AzVmss теперь принимают параметр ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="f22d8-175">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="f22d8-176">Исправлена опечатка в справочной документации по New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="f22d8-176">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="f22d8-177">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="f22d8-177">Az.Dns</span></span>
* <span data-ttu-id="f22d8-178">Исправлена опечатка в справочных примерах по использованию Set-AzDnsZone.</span><span class="sxs-lookup"><span data-stu-id="f22d8-178">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f22d8-179">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f22d8-179">Az.EventGrid</span></span>
* <span data-ttu-id="f22d8-180">Обновлен для использования API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="f22d8-180">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="f22d8-181">Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="f22d8-181">New cmdlets:</span></span>
    - <span data-ttu-id="f22d8-182">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="f22d8-182">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="f22d8-183">Создает домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="f22d8-183">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="f22d8-184">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="f22d8-184">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="f22d8-185">Возвращает сведения о домене Сетки событий или список всех доменов Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="f22d8-185">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="f22d8-186">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="f22d8-186">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="f22d8-187">Удаляет домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="f22d8-187">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="f22d8-188">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="f22d8-188">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="f22d8-189">Повторно создает ключ общего доступа для домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="f22d8-189">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="f22d8-190">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="f22d8-190">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="f22d8-191">Возвращает ключи общего доступа, используемые для публикации событий в домене Сетки событий.</span><span class="sxs-lookup"><span data-stu-id="f22d8-191">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="f22d8-192">New-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="f22d8-192">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="f22d8-193">Создает раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="f22d8-193">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="f22d8-194">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="f22d8-194">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="f22d8-195">Возвращает сведения о разделе домена Сетки событий или список всех разделов определенного домена Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="f22d8-195">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="f22d8-196">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="f22d8-196">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="f22d8-197">Удаляет раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="f22d8-197">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="f22d8-198">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="f22d8-198">Updated cmdlets:</span></span>
    - <span data-ttu-id="f22d8-199">New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="f22d8-199">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="f22d8-200">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для нового домена Сетки событий и раздела домена Сетки событий и позволяющие создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="f22d8-200">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="f22d8-201">Добавляют новые обязательные параметры для указания имени нового домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="f22d8-201">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="f22d8-202">Добавляют новые наборы параметров для доменов и разделов домена и позволяют повторно использовать существующие параметры (например, EndPointType, SubjectBeginsWith и т. д.).</span><span class="sxs-lookup"><span data-stu-id="f22d8-202">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="f22d8-203">Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="f22d8-203">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="f22d8-204">срока действия подписки на событие;</span><span class="sxs-lookup"><span data-stu-id="f22d8-204">Event subscription expiration date,</span></span>
            - <span data-ttu-id="f22d8-205">параметров расширенной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="f22d8-205">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="f22d8-206">Добавляют новое перечисление для ServiceBusQueue в качестве места назначения.</span><span class="sxs-lookup"><span data-stu-id="f22d8-206">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="f22d8-207">Запрещают использование значение All в параметре -IncludedEventType и заменяют его следующим:</span><span class="sxs-lookup"><span data-stu-id="f22d8-207">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="f22d8-208">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="f22d8-208">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="f22d8-209">Добавляют новые необязательные параметры (Top, ODataQuery и NextLink) для поддержки разбиения на страницы и фильтрации результатов.</span><span class="sxs-lookup"><span data-stu-id="f22d8-209">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="f22d8-210">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="f22d8-210">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="f22d8-211">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для домена Сетки событий и раздела домена Сетки событий и позволяющие удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="f22d8-211">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="f22d8-212">Добавляют новые обязательные параметры для указания имени домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="f22d8-212">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f22d8-213">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f22d8-213">Az.FrontDoor</span></span>
* <span data-ttu-id="f22d8-214">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="f22d8-214">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="f22d8-215">Добавляет поддержку преобразований и новое значение оператора автозавершения (RegEx).</span><span class="sxs-lookup"><span data-stu-id="f22d8-215">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="f22d8-216">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="f22d8-216">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="f22d8-217">Добавляет новые значения автозавершения.</span><span class="sxs-lookup"><span data-stu-id="f22d8-217">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f22d8-218">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22d8-218">Az.Network</span></span>
* <span data-ttu-id="f22d8-219">Добавляет поддержку ресурса шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="f22d8-219">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="f22d8-220">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="f22d8-220">New cmdlets</span></span>
        - <span data-ttu-id="f22d8-221">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="f22d8-221">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="f22d8-222">Добавляет AvailablePrivateEndpointType.</span><span class="sxs-lookup"><span data-stu-id="f22d8-222">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="f22d8-223">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="f22d8-223">New cmdlets</span></span> 
        - <span data-ttu-id="f22d8-224">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="f22d8-224">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="f22d8-225">Добавляет PrivatePrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="f22d8-225">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="f22d8-226">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="f22d8-226">New cmdlets</span></span> 
        - <span data-ttu-id="f22d8-227">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f22d8-227">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="f22d8-228">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f22d8-228">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="f22d8-229">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f22d8-229">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="f22d8-230">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f22d8-230">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="f22d8-231">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f22d8-231">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="f22d8-232">Добавляет PrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="f22d8-232">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="f22d8-233">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="f22d8-233">New cmdlets</span></span>
        - <span data-ttu-id="f22d8-234">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f22d8-234">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="f22d8-235">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f22d8-235">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="f22d8-236">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f22d8-236">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="f22d8-237">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="f22d8-237">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="f22d8-238">Обновлены следующие команды для функции: флаг UseLocalAzureIpAddress для VPN-подключения.</span><span class="sxs-lookup"><span data-stu-id="f22d8-238">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="f22d8-239">Обновлен командлет New-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="f22d8-239">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="f22d8-240">Обновлен командлет Set-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="f22d8-240">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="f22d8-241">В пиринг ExpressRoute добавлено поле только для чтения PeeredConnections.</span><span class="sxs-lookup"><span data-stu-id="f22d8-241">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="f22d8-242">В ExpressRoute добавлено поле только для чтения GlobalReachEnabled.</span><span class="sxs-lookup"><span data-stu-id="f22d8-242">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="f22d8-243">Добавлен атрибут в рамках критического изменения, отменяющего статус устаревшего поля AllowGlobalReach в модели ExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="f22d8-243">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="f22d8-244">Исправлена проблема, связанная с ошибкой 8756, при использовании TargetListenerID с командлетами AzApplicationGatewayRedirectConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f22d8-244">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="f22d8-245">Исправлена ошибка в New-AzApplicationGatewayPathRuleConfig, не позволявшая задавать набор правил повторного создания.</span><span class="sxs-lookup"><span data-stu-id="f22d8-245">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="f22d8-246">Исправлено отображение VirtualNetworkTaps в NetworkInterfaceIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f22d8-246">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="f22d8-247">Исправлены командлеты Cortex Get для отображения всех частей.</span><span class="sxs-lookup"><span data-stu-id="f22d8-247">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="f22d8-248">Исправлено создание ссылок VirtualHub для ExpressRouteGateways и VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="f22d8-248">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="f22d8-249">В AzureFirewall и NatGateway добавлена поддержка Зон доступности.</span><span class="sxs-lookup"><span data-stu-id="f22d8-249">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="f22d8-250">Добавлен командлет Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="f22d8-250">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="f22d8-251">Добавлена поддержка нескольких общедоступных IP-адресов для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="f22d8-251">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="f22d8-252">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="f22d8-252">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="f22d8-253">Добавлен параметр -PublicIpAddress, который принимает один или несколько объектов общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="f22d8-253">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="f22d8-254">Добавлен параметр -VirtualNetwork, который принимает объект виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="f22d8-254">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="f22d8-255">Добавлены методы AddPublicIpAddress и RemovePublicIpAddress для объекта брандмауэра. Они принимают объект общедоступного IP-адреса в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="f22d8-255">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="f22d8-256">Не рекомендуется использовать параметры -PublicIpName и -VirtualNetworkName.</span><span class="sxs-lookup"><span data-stu-id="f22d8-256">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="f22d8-257">Обновлены следующие команды для функции: В параметрах проверки подлинности AAD VPN-клиента задан ресурс шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="f22d8-257">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="f22d8-258">Обновлен командлет New-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="f22d8-258">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="f22d8-259">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="f22d8-259">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="f22d8-260">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр-переключатель RemoveAadAuthentication для удаления в шлюзе параметров проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="f22d8-260">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f22d8-261">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f22d8-261">Az.OperationalInsights</span></span>
* <span data-ttu-id="f22d8-262">Добавлена поддержка SKU **pergb2018** в команде New-AzureRmOperationalInsightsWorkspace.</span><span class="sxs-lookup"><span data-stu-id="f22d8-262">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="f22d8-263">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22d8-263">Az.Resources</span></span>
* <span data-ttu-id="f22d8-264">Поддержка дополнительных вариантов экспорта шаблона.</span><span class="sxs-lookup"><span data-stu-id="f22d8-264">Support for additional Template Export options</span></span>
    - <span data-ttu-id="f22d8-265">В Export-AzResourceGroup добавлен параметр -SkipResourceNameParameterization.</span><span class="sxs-lookup"><span data-stu-id="f22d8-265">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="f22d8-266">В Export-AzResourceGroup добавлен параметр -SkipAllParameterization.</span><span class="sxs-lookup"><span data-stu-id="f22d8-266">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="f22d8-267">В Export-AzResourceGroup добавлен параметр -Resource для фильтрации экспортированных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f22d8-267">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f22d8-268">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f22d8-268">Az.ServiceFabric</span></span>
* <span data-ttu-id="f22d8-269">Исправлена ошибка, связанная с получением иногда неправильных отпечатков при добавлении сертификата ByExistingKeyVault.</span><span class="sxs-lookup"><span data-stu-id="f22d8-269">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="f22d8-270">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22d8-270">Az.Sql</span></span>
* <span data-ttu-id="f22d8-271">Исправлен суффикс конечной точки хранилища службы "Расширенная защита от угроз Azure".</span><span class="sxs-lookup"><span data-stu-id="f22d8-271">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="f22d8-272">Исправлена ошибка, связанная с возможностью пакета "Расширенная защита данных" переопределять политику службы "Расширенная защита от угроз".</span><span class="sxs-lookup"><span data-stu-id="f22d8-272">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="f22d8-273">Новые командлеты для Management.Sql позволяют клиентам добавлять ключи TDE и задавать средство защиты TDE для управляемых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="f22d8-273">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="f22d8-274">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f22d8-274">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="f22d8-275">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f22d8-275">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="f22d8-276">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f22d8-276">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="f22d8-277">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="f22d8-277">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="f22d8-278">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="f22d8-278">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f22d8-279">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f22d8-279">Az.Storage</span></span>
* <span data-ttu-id="f22d8-280">Поддержка класса Kind в FileStorage и значения Premium_ZRS в SkuName при создании учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="f22d8-280">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="f22d8-281">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f22d8-281">New-AzStorageAccount</span></span>
* <span data-ttu-id="f22d8-282">Уточнено описание командлета неизменности BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="f22d8-282">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="f22d8-283">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="f22d8-283">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f22d8-284">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f22d8-284">Az.Websites</span></span>
* <span data-ttu-id="f22d8-285">Оптимизирует Get-AzWebAppCertificate для фильтрации по группе ресурсов на сервере, а не в клиенте.</span><span class="sxs-lookup"><span data-stu-id="f22d8-285">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="f22d8-286">Добавляет параметр-переключатель - UseDisasterRecovery в Get AzWebAppSnapshot.</span><span class="sxs-lookup"><span data-stu-id="f22d8-286">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="f22d8-287">2.2.0 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f22d8-287">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="f22d8-288">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f22d8-288">Az.Cdn</span></span>
* <span data-ttu-id="f22d8-289">Обновлены командлеты для поддержки функции rulesEngine на основе API версии 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="f22d8-289">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22d8-290">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22d8-290">Az.Compute</span></span>
* <span data-ttu-id="f22d8-291">Добавлен параметр `NoWait`, который запускает операцию и немедленно возвращает значение еще до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="f22d8-291">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="f22d8-292">Обновлены командлеты:   Export-AzLogAnalyticRequestRateByInterval; Export-AzLogAnalyticThrottledRequest; Remove-AzVM; Remove-AzVMAccessExtension; Remove-AzVMAEMExtension; Remove-AzVMChefExtension; Remove-AzVMCustomScriptExtension; Remove-AzVMDiagnosticsExtension; Remove-AzVMDiskEncryptionExtension; Remove-AzVMDscExtension; Remove-AzVMSqlServerExtension; Restart-AzVM; Set-AzVM; Set-AzVMAccessExtension; Set-AzVMADDomainExtension; Set-AzVMAEMExtension; Set-AzVMBginfoExtension; Set-AzVMChefExtension; Set-AzVMCustomScriptExtension; Set-AzVMDiagnosticsExtension; Set-AzVMDscExtension; Set-AzVMExtension; Start-AzVM; Stop-AzVM; Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="f22d8-292">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f22d8-293">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f22d8-293">Az.EventHub</span></span>
* <span data-ttu-id="f22d8-294">Исправлена ошибка № 9231. Командлет Get-AzEventHubNamespace не возвращал теги.</span><span class="sxs-lookup"><span data-stu-id="f22d8-294">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="f22d8-295">Исправлена ошибка № 9230. Командлет Get-AzEventHubNamespace возвращал значение ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="f22d8-295">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f22d8-296">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22d8-296">Az.Network</span></span>
* <span data-ttu-id="f22d8-297">Обновлены параметры ResourceId и InputObject для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="f22d8-297">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="f22d8-298">Добавлены псевдонимы для параметров ResourceId и InputObject.</span><span class="sxs-lookup"><span data-stu-id="f22d8-298">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f22d8-299">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f22d8-299">Az.PolicyInsights</span></span>
* <span data-ttu-id="f22d8-300">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyEvent.</span><span class="sxs-lookup"><span data-stu-id="f22d8-300">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f22d8-301">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f22d8-301">Az.RecoveryServices</span></span>
* <span data-ttu-id="f22d8-302">Минимальный срок хранения политики IaaSVM изменился с 1 до 7 дней.</span><span class="sxs-lookup"><span data-stu-id="f22d8-302">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f22d8-303">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f22d8-303">Az.ServiceBus</span></span>
* <span data-ttu-id="f22d8-304">Исправлена ошибка № 9182. Командлет Get-AzServiceBusNamespace возвращал ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="f22d8-304">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f22d8-305">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f22d8-305">Az.ServiceFabric</span></span>
* <span data-ttu-id="f22d8-306">Исправлена опечатка в сообщении об ошибке для командлета Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="f22d8-306">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="f22d8-307">Исправлен отсутствующей символ в командных строках Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="f22d8-307">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="f22d8-308">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22d8-308">Az.Sql</span></span>
* <span data-ttu-id="f22d8-309">Для командлета New-AzureSqlInstance добавлен параметр DnsZonePartner, обеспечивающий поддержку AutoDr для Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f22d8-309">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="f22d8-310">Командлет Get-AzSqlDatabaseSecureConnectionPolicy объявлен неподдерживаемым.</span><span class="sxs-lookup"><span data-stu-id="f22d8-310">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="f22d8-311">Командлеты обнаружения угроз переименованы в командлеты Расширенной защиты от угроз.</span><span class="sxs-lookup"><span data-stu-id="f22d8-311">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="f22d8-312">Параметры -StorageSizeInGB и -LicenseType командлета New-AzSqlInstance теперь необязательны.</span><span class="sxs-lookup"><span data-stu-id="f22d8-312">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f22d8-313">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f22d8-313">Az.Websites</span></span>
* <span data-ttu-id="f22d8-314">Исправлены проблемы, когда удалялись теги при использовании Set-AzWebApp и Set-AzWebAppSlot со свойством -WebApp.</span><span class="sxs-lookup"><span data-stu-id="f22d8-314">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="f22d8-315">2.1.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f22d8-315">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="f22d8-316">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f22d8-316">Az.ApiManagement</span></span>
* <span data-ttu-id="f22d8-317">Созданы командлеты для управления диагностикой в глобальной области и в области API.</span><span class="sxs-lookup"><span data-stu-id="f22d8-317">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="f22d8-318">**Get-AzApiManagementDiagnostic** — получение диагностики, заданной глобально или на уровне области API.</span><span class="sxs-lookup"><span data-stu-id="f22d8-318">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="f22d8-319">**New-AzApiManagementDiagnostic** — создание диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="f22d8-319">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="f22d8-320">**New-AzApiManagementHttpMessageDiagnostic** — создание параметра диагностики, для которого регистрируются заголовки и размер байтов тела.</span><span class="sxs-lookup"><span data-stu-id="f22d8-320">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="f22d8-321">**New-AzApiManagementPipelineDiagnosticSetting** — создание параметров диагностики для сообщений HTTP, поступающих в шлюз или исходящих из него.</span><span class="sxs-lookup"><span data-stu-id="f22d8-321">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="f22d8-322">**New-AzApiManagementSamplingSetting** — создание параметра выборки для запросов и ответов касательно диагностики.</span><span class="sxs-lookup"><span data-stu-id="f22d8-322">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="f22d8-323">**Remove-AzApiManagementDiagnostic** — удаление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="f22d8-323">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="f22d8-324">**Set-AzApiManagementDiagnostic** — обновление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="f22d8-324">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="f22d8-325">Созданы командлеты для управления кэшем в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="f22d8-325">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="f22d8-326">**Get-AzApiManagementCache** — получение сведений о кэше, указанном идентификатором, или обо всех кэшах.</span><span class="sxs-lookup"><span data-stu-id="f22d8-326">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="f22d8-327">**New-AzApiManagementCache** — создание кэша по умолчанию или кэша в определенном регионе Azure.</span><span class="sxs-lookup"><span data-stu-id="f22d8-327">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="f22d8-328">**Remove-AzApiManagementCache** — удаление кэша.</span><span class="sxs-lookup"><span data-stu-id="f22d8-328">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="f22d8-329">**Update-AzApiManagementCache** — обновление кэша.</span><span class="sxs-lookup"><span data-stu-id="f22d8-329">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="f22d8-330">Созданы командлеты для управления схемой API.</span><span class="sxs-lookup"><span data-stu-id="f22d8-330">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="f22d8-331">**New-AzApiManagementSchema** — создание схемы для API.</span><span class="sxs-lookup"><span data-stu-id="f22d8-331">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="f22d8-332">**Get-AzApiManagementSchema** — получение схем, настроенных в API.</span><span class="sxs-lookup"><span data-stu-id="f22d8-332">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="f22d8-333">**Remove-AzApiManagementSchema** — удаление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="f22d8-333">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="f22d8-334">**Set-AzApiManagementSchema** — обновление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="f22d8-334">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="f22d8-335">Создан командлет для создания токена пользователя.</span><span class="sxs-lookup"><span data-stu-id="f22d8-335">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="f22d8-336">**New-AzApiManagementUserToken** — создание токена пользователя, по умолчанию действительного в течение 8 часов. С помощью этого командлета можно создавать токен для пользователя GIT.</span><span class="sxs-lookup"><span data-stu-id="f22d8-336">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="f22d8-337">Создан командлет для получения состояния сети.</span><span class="sxs-lookup"><span data-stu-id="f22d8-337">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="f22d8-338">**Get-AzApiManagementNetworkStatus** — получение состояния сети ресурсов, от которых зависит служба "Управление API".</span><span class="sxs-lookup"><span data-stu-id="f22d8-338">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="f22d8-339">Это полезно при развертывании службы ApiManagement в виртуальной сети и проверке того, не нарушена ли какая-либо из зависимостей.</span><span class="sxs-lookup"><span data-stu-id="f22d8-339">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="f22d8-340">Обновлен командлет **New-AzApiManagement** для управления службой ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="f22d8-340">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="f22d8-341">Добавлена поддержка нового SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="f22d8-341">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="f22d8-342">Добавлена поддержка для включения флага EnableClientCertificate в SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="f22d8-342">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="f22d8-343">Новый командлет **New-AzApiManagementSslSetting** позволяет настраивать параметр TLS/SSL для сервера (Backend) и внешнего интерфейса (Frontend).</span><span class="sxs-lookup"><span data-stu-id="f22d8-343">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="f22d8-344">Его также можно использовать для настройки Ciphers как 3DES, в ServerProtocols как Http2 для внешнего интерфейса (Frontend) службы ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="f22d8-344">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="f22d8-345">Добавлена поддержка настройки имени узла DeveloperPortal в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="f22d8-345">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="f22d8-346">Обновлен командлет **Get-AzApiManagementSsoToken** для извлечения объекта PsApiManagement в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="f22d8-346">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="f22d8-347">Обновлен командлет для отображения встроенных сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="f22d8-347">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="f22d8-348">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Код ошибки: ValidationError. Сообщение об ошибке: "Некоторые поля содержат неправильные значения". Сведения об ошибке: [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="f22d8-348">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="f22d8-349">Обновлен командлет **Export-AzApiManagementApi** для экспортирования программных интерфейсов в формате OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="f22d8-349">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="f22d8-350">Обновлен командлет **Import-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="f22d8-350">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="f22d8-351">Для импортирования API из спецификации документа OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="f22d8-351">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="f22d8-352">Для переопределения свойства PsApiManagementSchema, указанного в любом документе (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="f22d8-352">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="f22d8-353">Для переопределения свойства ServiceUrl, указанного в любом документе.</span><span class="sxs-lookup"><span data-stu-id="f22d8-353">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="f22d8-354">Обновлен командлет **Get-AzApiManagementPolicy** для возврата политики в формате, экранированном не для XML, с использованием rawxml.</span><span class="sxs-lookup"><span data-stu-id="f22d8-354">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="f22d8-355">Обновлен командлет **Set-AzApiManagementPolicy**. Он принимает политику в формате, экранированном не для XML, с использованием rawxml и в формате, экранированном для XML, с использованием XML.</span><span class="sxs-lookup"><span data-stu-id="f22d8-355">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="f22d8-356">Обновлен командлет **New-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="f22d8-356">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="f22d8-357">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="f22d8-357">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="f22d8-358">Для создания API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="f22d8-358">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="f22d8-359">Для клонирования API с использованием значений SourceApiId и SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="f22d8-359">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="f22d8-360">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="f22d8-360">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="f22d8-361">Обновлен командлет **Set-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="f22d8-361">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="f22d8-362">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="f22d8-362">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="f22d8-363">Для обновления API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="f22d8-363">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="f22d8-364">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="f22d8-364">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="f22d8-365">Обновлен командлет **New-AzApiManagementRevision**:</span><span class="sxs-lookup"><span data-stu-id="f22d8-365">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="f22d8-366">Для клонирования (копирования тегов, продуктов, операций и политик) существующей редакции с использованием SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="f22d8-366">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="f22d8-367">Новая редакция предполагает родительский идентификатор ApiId.</span><span class="sxs-lookup"><span data-stu-id="f22d8-367">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="f22d8-368">Для предоставления ApiRevisionDescription.</span><span class="sxs-lookup"><span data-stu-id="f22d8-368">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="f22d8-369">Для переопределения значения ServiceUrl при клонировании API.</span><span class="sxs-lookup"><span data-stu-id="f22d8-369">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="f22d8-370">Обновлен командлет **New-AzApiManagementIdentityProvider**:</span><span class="sxs-lookup"><span data-stu-id="f22d8-370">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="f22d8-371">Для настройки AAD или AADB2C с Authority.</span><span class="sxs-lookup"><span data-stu-id="f22d8-371">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="f22d8-372">Для установки политик SignupPolicy, SigninPolicy, ProfileEditingPolicy и PasswordResetPolicy.</span><span class="sxs-lookup"><span data-stu-id="f22d8-372">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="f22d8-373">Обновлен командлет **New-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="f22d8-373">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="f22d8-374">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="f22d8-374">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="f22d8-375">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="f22d8-375">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="f22d8-376">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="f22d8-376">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="f22d8-377">Обновлен командлет **Set-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="f22d8-377">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="f22d8-378">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="f22d8-378">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="f22d8-379">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="f22d8-379">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="f22d8-380">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="f22d8-380">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="f22d8-381">Следующие командлеты обновлены, чтобы принимать значение ResourceId в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="f22d8-381">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="f22d8-382">New-AzApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="f22d8-382">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="f22d8-383">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="f22d8-383">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="f22d8-384">Get-AzApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="f22d8-384">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="f22d8-385">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="f22d8-385">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="f22d8-386">Get-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="f22d8-386">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="f22d8-387">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="f22d8-387">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="f22d8-388">Get-AzApiManagementAuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="f22d8-388">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="f22d8-389">Get-AzApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="f22d8-389">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="f22d8-390">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="f22d8-390">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="f22d8-391">Get-AzApiManagementCertificate.</span><span class="sxs-lookup"><span data-stu-id="f22d8-391">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="f22d8-392">Remove-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="f22d8-392">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="f22d8-393">Remove-AzApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="f22d8-393">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f22d8-394">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f22d8-394">Az.Automation</span></span>
* <span data-ttu-id="f22d8-395">Обновлен командлет Get-AzAutomationJobOutputRecord для обработки значений в формате JSON и в виде текстовой записи.</span><span class="sxs-lookup"><span data-stu-id="f22d8-395">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="f22d8-396">исправлена проблема https://github.com/Azure/azure-powershell/issues/7977.</span><span class="sxs-lookup"><span data-stu-id="f22d8-396">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="f22d8-397">исправлена проблема https://github.com/Azure/azure-powershell/issues/8600.</span><span class="sxs-lookup"><span data-stu-id="f22d8-397">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="f22d8-398">Поведение командлета Start-AzAutomationDscCompilationJob изменено так, чтобы сразу же запустить задание, а не ждать его завершения.</span><span class="sxs-lookup"><span data-stu-id="f22d8-398">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="f22d8-399">исправлена проблема https://github.com/Azure/azure-powershell/issues/8347.</span><span class="sxs-lookup"><span data-stu-id="f22d8-399">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="f22d8-400">Исправлен командлет Get-AzAutomationDscNode, возвращающий все узлы при использовании -Name.</span><span class="sxs-lookup"><span data-stu-id="f22d8-400">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="f22d8-401">Теперь он возвращает только соответствующий узел.</span><span class="sxs-lookup"><span data-stu-id="f22d8-401">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22d8-402">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22d8-402">Az.Compute</span></span>
* <span data-ttu-id="f22d8-403">Добавлены параметры ProtectFromScaleIn и ProtectFromScaleSetAction для командлета Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="f22d8-403">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="f22d8-404">Командлет New-AzVM с простым набором параметров теперь по умолчанию использует доступное расположение, если регион "восточная часть США" не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f22d8-404">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f22d8-405">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f22d8-405">Az.DataLakeStore</span></span>
* <span data-ttu-id="f22d8-406">Обновлен пакет SDK ADLS для использования httpclient. В инфраструктуру Azure интегрирована проверка плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="f22d8-406">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f22d8-407">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f22d8-407">Az.Monitor</span></span>
* <span data-ttu-id="f22d8-408">Исправлены неправильные имена параметров в справочных примерах.</span><span class="sxs-lookup"><span data-stu-id="f22d8-408">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f22d8-409">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22d8-409">Az.Network</span></span>
* <span data-ttu-id="f22d8-410">Добавлен флаг DisableBgpRoutePropagation для выходных данных действующей таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="f22d8-410">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="f22d8-411">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="f22d8-411">Updated cmdlet:</span></span>
        - <span data-ttu-id="f22d8-412">Get-AzEffectiveRouteTable.</span><span class="sxs-lookup"><span data-stu-id="f22d8-412">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="f22d8-413">Исправлен двойной дефис в документации New-AzApplicationGatewayTrustedRootCertificate.</span><span class="sxs-lookup"><span data-stu-id="f22d8-413">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="f22d8-414">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22d8-414">Az.Resources</span></span>
* <span data-ttu-id="f22d8-415">Добавлен новый командлет Get-AzureRmDenyAssignment для получения запрещающих назначений.</span><span class="sxs-lookup"><span data-stu-id="f22d8-415">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="f22d8-416">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22d8-416">Az.Sql</span></span>
* <span data-ttu-id="f22d8-417">Командлеты Расширенной защиты от угроз переименованы на командлеты Расширенной защиты данных, и оценка уязвимости включена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f22d8-417">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="f22d8-418">2.0.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f22d8-418">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f22d8-419">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f22d8-419">Az.Accounts</span></span>
* <span data-ttu-id="f22d8-420">Обновлена библиотека аутентификации для устранения проблем с ADFS при использовании аутентификации на основе имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="f22d8-420">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f22d8-421">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f22d8-421">Az.CognitiveServices</span></span>
* <span data-ttu-id="f22d8-422">Отображается только заявление об отказе Bing для служб Поиска Bing.</span><span class="sxs-lookup"><span data-stu-id="f22d8-422">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="f22d8-423">Исправлена проблема с созданием учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f22d8-423">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22d8-424">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22d8-424">Az.Compute</span></span>
* <span data-ttu-id="f22d8-425">Функция группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="f22d8-425">Proximity placement group feature.</span></span>
    - <span data-ttu-id="f22d8-426">Добавлены следующие новые командлеты:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="f22d8-426">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="f22d8-427">Новый параметр ProximityPlacementGroupId будет добавлен в следующие командлеты:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="f22d8-427">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="f22d8-428">В командлет New-AzGalleryImageVersion добавлен параметр StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="f22d8-428">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="f22d8-429">TargetRegion в командлете New-AzGalleryImageVersion может содержать StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="f22d8-429">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="f22d8-430">Параметр-переключатель SkipShutdown добавлен в командлеты Stop-AzVM и Stop-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="f22d8-430">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="f22d8-431">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="f22d8-431">Breaking changes</span></span>
    - <span data-ttu-id="f22d8-432">Командлет SET-AzVMBootDiagnostics изменен на Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="f22d8-432">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="f22d8-433">Командлет Export-AzLogAnalyticThrottledRequests изменен на Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="f22d8-433">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="f22d8-434">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="f22d8-434">Az.DeploymentManager</span></span>
* <span data-ttu-id="f22d8-435">Первая общедоступная версия командлетов диспетчера развертывания Azure</span><span class="sxs-lookup"><span data-stu-id="f22d8-435">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="f22d8-436">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="f22d8-436">Az.Dns</span></span>
* <span data-ttu-id="f22d8-437">Автоматическое делегирование DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="f22d8-437">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="f22d8-438">Командлет для создания зоны DNS принимает имя родительской зоны в качестве дополнительного необязательного параметра.</span><span class="sxs-lookup"><span data-stu-id="f22d8-438">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="f22d8-439">Он добавляет записи NS в родительской зоне для созданной дочерней зоны.</span><span class="sxs-lookup"><span data-stu-id="f22d8-439">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f22d8-440">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f22d8-440">Az.FrontDoor</span></span>
* <span data-ttu-id="f22d8-441">Первая общедоступная версия командлетов Azure FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="f22d8-441">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="f22d8-442">Переименованы командлеты WAF для включения Waf.</span><span class="sxs-lookup"><span data-stu-id="f22d8-442">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="f22d8-443">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f22d8-443">Az.HDInsight</span></span>
* <span data-ttu-id="f22d8-444">Удалены два командлета:</span><span class="sxs-lookup"><span data-stu-id="f22d8-444">Removed two cmdlets:</span></span>
    - <span data-ttu-id="f22d8-445">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f22d8-445">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="f22d8-446">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f22d8-446">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="f22d8-447">Добавлен новый командлет Set-AzHDInsightGatewayCredential для замены Grant-AzHDInsightHttpServicesAccess.</span><span class="sxs-lookup"><span data-stu-id="f22d8-447">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="f22d8-448">Обновлен командлет Get-AzHDInsightJobOutput для различения ролей читателя и оператора HDInsight:</span><span class="sxs-lookup"><span data-stu-id="f22d8-448">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="f22d8-449">Пользователям с ролью читателя не нужно указывать параметр DefaultStorageAccountKey явным образом, иначе возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="f22d8-449">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="f22d8-450">На пользователей с ролью оператора HDInsight это не повлияет.</span><span class="sxs-lookup"><span data-stu-id="f22d8-450">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f22d8-451">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f22d8-451">Az.Monitor</span></span>
* <span data-ttu-id="f22d8-452">Новые командлеты для API SQR (запланированное правило запросов)</span><span class="sxs-lookup"><span data-stu-id="f22d8-452">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="f22d8-453">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="f22d8-453">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="f22d8-454">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="f22d8-454">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="f22d8-455">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="f22d8-455">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="f22d8-456">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="f22d8-456">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="f22d8-457">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="f22d8-457">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="f22d8-458">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="f22d8-458">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="f22d8-459">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f22d8-459">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f22d8-460">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f22d8-460">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f22d8-461">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f22d8-461">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f22d8-462">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f22d8-462">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f22d8-463">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f22d8-463">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f22d8-464">См. подробнее об [API SQR](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules).</span><span class="sxs-lookup"><span data-stu-id="f22d8-464">[More](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="f22d8-465">Обновлен файл Az.Monitor.md для включения командлетов для правила генерации оповещений на основе метрик GenV2(не классическая версия).</span><span class="sxs-lookup"><span data-stu-id="f22d8-465">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f22d8-466">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22d8-466">Az.Network</span></span>
* <span data-ttu-id="f22d8-467">Добавлена поддержка для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="f22d8-467">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="f22d8-468">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="f22d8-468">New cmdlets</span></span>
        - <span data-ttu-id="f22d8-469">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f22d8-469">New-AzNatGateway</span></span>
        - <span data-ttu-id="f22d8-470">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f22d8-470">Get-AzNatGateway</span></span>
        - <span data-ttu-id="f22d8-471">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f22d8-471">Set-AzNatGateway</span></span>
        - <span data-ttu-id="f22d8-472">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f22d8-472">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="f22d8-473">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="f22d8-473">Updated cmdlets</span></span>
        - <span data-ttu-id="f22d8-474">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="f22d8-474">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="f22d8-475">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="f22d8-475">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="f22d8-476">Обновлены следующие команды для функции: Настройка и удаление пользовательских маршрутов через шлюз в Бруклине.</span><span class="sxs-lookup"><span data-stu-id="f22d8-476">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="f22d8-477">Обновлен командлет New-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="f22d8-477">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="f22d8-478">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="f22d8-478">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f22d8-479">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f22d8-479">Az.PolicyInsights</span></span>
* <span data-ttu-id="f22d8-480">Добавлена поддержка сведений об оценке политики запросов.</span><span class="sxs-lookup"><span data-stu-id="f22d8-480">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="f22d8-481">Добавлен параметр -Expand в командлет Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="f22d8-481">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="f22d8-482">Добавлена поддержка -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="f22d8-482">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f22d8-483">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f22d8-483">Az.RecoveryServices</span></span>
* <span data-ttu-id="f22d8-484">Добавлена поддержка перекрестной подписки на Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f22d8-484">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="f22d8-485">Добавлена возможность отмечать предстоящие критически важные изменения для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f22d8-485">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="f22d8-486">Исправлены план восстановления и план действий для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f22d8-486">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="f22d8-487">Исправлено сетевое сопоставление обновления Azure Site Recovery (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="f22d8-487">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="f22d8-488">Исправлено направление защиты обновления Azure Site Recovery для управляемых дисков (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="f22d8-488">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="f22d8-489">Добавлены другие незначительные исправления.</span><span class="sxs-lookup"><span data-stu-id="f22d8-489">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="f22d8-490">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="f22d8-490">Az.Relay</span></span>
* <span data-ttu-id="f22d8-491">Исправлены опечатки в сообщениях для клиентов.</span><span class="sxs-lookup"><span data-stu-id="f22d8-491">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f22d8-492">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f22d8-492">Az.ServiceBus</span></span>
* <span data-ttu-id="f22d8-493">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="f22d8-493">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f22d8-494">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f22d8-494">Az.Storage</span></span>
* <span data-ttu-id="f22d8-495">Выполнено обновление клиентской библиотеки хранилища до версии 10.0.1 (пространство имен всех объектов из этого пакета SDK изменено с Microsoft.WindowsAzure.Storage. *на Microsoft.Azure.Storage*).</span><span class="sxs-lookup"><span data-stu-id="f22d8-495">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="f22d8-496">Выполнено обновление до Microsoft.Azure.Management.Storage версии 11.0.0 для включения поддержки нового API версии 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="f22d8-496">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="f22d8-497">Значение свойства Kind по умолчанию в учетной записи хранения изменено со Storage на StorageV2.</span><span class="sxs-lookup"><span data-stu-id="f22d8-497">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="f22d8-498">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f22d8-498">New-AzStorageAccount</span></span>
* <span data-ttu-id="f22d8-499">Изменено значение Sku.Name в выходных данных командлета учетной записи хранения в соответствии со значением Sku.Name во входных данных путем добавления _ (например, StandardLRS изменено на Standard_LRS).</span><span class="sxs-lookup"><span data-stu-id="f22d8-499">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="f22d8-500">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f22d8-500">New-AzStorageAccount</span></span>
    - <span data-ttu-id="f22d8-501">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f22d8-501">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="f22d8-502">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f22d8-502">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f22d8-503">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f22d8-503">Az.Websites</span></span>
* <span data-ttu-id="f22d8-504">Свойство Kind теперь будет задаваться объектам PSSite, возвращаемым командлетом Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="f22d8-504">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="f22d8-505">Get-AzWebApp\*Metrics и Get-AzAppServicePlanMetrics считаются нерекомендуемыми.</span><span class="sxs-lookup"><span data-stu-id="f22d8-505">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="f22d8-506">1.8.0 — апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f22d8-506">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f22d8-507">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="f22d8-507">Highlights since the last major release</span></span>
* <span data-ttu-id="f22d8-508">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="f22d8-508">General availability of `Az` module</span></span>
* <span data-ttu-id="f22d8-509">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="f22d8-509">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="f22d8-510">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="f22d8-510">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="f22d8-511">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="f22d8-511">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="f22d8-512">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="f22d8-512">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f22d8-513">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="f22d8-513">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="f22d8-514">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="f22d8-514">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f22d8-515">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f22d8-515">Az.Accounts</span></span>
* <span data-ttu-id="f22d8-516">Обновлен командлет Uninstall-AzureRm для правильного удаления модулей в Mac.</span><span class="sxs-lookup"><span data-stu-id="f22d8-516">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f22d8-517">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f22d8-517">Az.Batch</span></span>
* <span data-ttu-id="f22d8-518">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f22d8-518">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f22d8-519">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f22d8-519">Az.Cdn</span></span>
* <span data-ttu-id="f22d8-520">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f22d8-520">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f22d8-521">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f22d8-521">Az.CognitiveServices</span></span>
* <span data-ttu-id="f22d8-522">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f22d8-522">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22d8-523">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22d8-523">Az.Compute</span></span>
* <span data-ttu-id="f22d8-524">Устранена проблема с установкой AEM, если в идентификаторах ресурсов дисков группа ресурсов указана в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="f22d8-524">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="f22d8-525">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f22d8-525">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f22d8-526">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="f22d8-526">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f22d8-527">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f22d8-527">Az.DataFactory</span></span>
* <span data-ttu-id="f22d8-528">Добавлены свойства SsisProperties, если NodeCount не имеет значения NULL для управляемой среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="f22d8-528">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f22d8-529">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f22d8-529">Az.DataLakeStore</span></span>
* <span data-ttu-id="f22d8-530">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f22d8-530">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f22d8-531">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f22d8-531">Az.EventGrid</span></span>
* <span data-ttu-id="f22d8-532">Обновлен текст справки для конечной точки, указывающий, что необходимо создать ресурсы, прежде чем использовать командлеты для создания или обновления подписки на события.</span><span class="sxs-lookup"><span data-stu-id="f22d8-532">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f22d8-533">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f22d8-533">Az.EventHub</span></span>
* <span data-ttu-id="f22d8-534">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="f22d8-534">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="f22d8-535">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f22d8-535">Az.HDInsight</span></span>
* <span data-ttu-id="f22d8-536">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f22d8-536">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f22d8-537">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f22d8-537">Az.IotHub</span></span>
* <span data-ttu-id="f22d8-538">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f22d8-538">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f22d8-539">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f22d8-539">Az.KeyVault</span></span>
* <span data-ttu-id="f22d8-540">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f22d8-540">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f22d8-541">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="f22d8-541">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="f22d8-542">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="f22d8-542">Az.MachineLearning</span></span>
* <span data-ttu-id="f22d8-543">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f22d8-543">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="f22d8-544">Az.Media</span><span class="sxs-lookup"><span data-stu-id="f22d8-544">Az.Media</span></span>
* <span data-ttu-id="f22d8-545">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f22d8-545">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f22d8-546">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f22d8-546">Az.Monitor</span></span>
  * <span data-ttu-id="f22d8-547">Добавлены новые командлеты для правила генерации оповещений на основе метрик GenV2 (не классических).</span><span class="sxs-lookup"><span data-stu-id="f22d8-547">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="f22d8-548">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="f22d8-548">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="f22d8-549">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="f22d8-549">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="f22d8-550">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f22d8-550">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="f22d8-551">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f22d8-551">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="f22d8-552">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f22d8-552">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="f22d8-553">Обновлен пакет SDK Monitor до предварительной версии 0.22.0.</span><span class="sxs-lookup"><span data-stu-id="f22d8-553">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f22d8-554">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22d8-554">Az.Network</span></span>
* <span data-ttu-id="f22d8-555">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f22d8-555">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f22d8-556">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="f22d8-556">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="f22d8-557">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="f22d8-557">Az.NotificationHubs</span></span>
* <span data-ttu-id="f22d8-558">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f22d8-558">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f22d8-559">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f22d8-559">Az.OperationalInsights</span></span>
* <span data-ttu-id="f22d8-560">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f22d8-560">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="f22d8-561">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="f22d8-561">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="f22d8-562">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f22d8-562">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f22d8-563">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f22d8-563">Az.RecoveryServices</span></span>
* <span data-ttu-id="f22d8-564">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f22d8-564">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f22d8-565">Обновлен табличный формат для SQL на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="f22d8-565">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="f22d8-566">Добавлен альтернативный метод для получения расположения в Общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="f22d8-566">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="f22d8-567">Обновлено значение ScheduleRunDays в объекте SchedulePolicy в соответствии с часовым поясом.</span><span class="sxs-lookup"><span data-stu-id="f22d8-567">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f22d8-568">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f22d8-568">Az.RedisCache</span></span>
* <span data-ttu-id="f22d8-569">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f22d8-569">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f22d8-570">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22d8-570">Az.Resources</span></span>
* <span data-ttu-id="f22d8-571">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="f22d8-571">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="f22d8-572">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22d8-572">Az.Sql</span></span>
* <span data-ttu-id="f22d8-573">Заменена зависимость от пакета SDK монитора на обычный код.</span><span class="sxs-lookup"><span data-stu-id="f22d8-573">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="f22d8-574">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f22d8-574">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f22d8-575">Улучшен процесс классификации нескольких столбцов.</span><span class="sxs-lookup"><span data-stu-id="f22d8-575">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="f22d8-576">Добавлены свойства SKU (имя, семейство, производительность SKU) в отклике Get-AzSqlServerServiceObjective, а также по умолчанию задан табличный формат.</span><span class="sxs-lookup"><span data-stu-id="f22d8-576">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="f22d8-577">C помощью Get-AzSqlServerServiceObjective теперь можно получать список доступных целевых служб по расположению без необходимости заранее размещать сервер в регионе.</span><span class="sxs-lookup"><span data-stu-id="f22d8-577">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="f22d8-578">Поддерживается параметр часового пояса при создании Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f22d8-578">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="f22d8-579">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="f22d8-579">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f22d8-580">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f22d8-580">Az.Websites</span></span>
* <span data-ttu-id="f22d8-581">Исправлены командлеты Set-AzWebApp и Set-AzWebAppSlot, которые теперь не удаляют теги при выполнении.</span><span class="sxs-lookup"><span data-stu-id="f22d8-581">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="f22d8-582">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f22d8-582">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f22d8-583">Обновлен пакет SDK веб-узлов.</span><span class="sxs-lookup"><span data-stu-id="f22d8-583">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="f22d8-584">Удалено свойство AdminSiteName из PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="f22d8-584">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="f22d8-585">1.7.0 —апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f22d8-585">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f22d8-586">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="f22d8-586">Highlights since the last major release</span></span>
* <span data-ttu-id="f22d8-587">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="f22d8-587">General availability of `Az` module</span></span>
* <span data-ttu-id="f22d8-588">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="f22d8-588">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="f22d8-589">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="f22d8-589">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="f22d8-590">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="f22d8-590">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="f22d8-591">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="f22d8-591">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f22d8-592">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="f22d8-592">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="f22d8-593">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="f22d8-593">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f22d8-594">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f22d8-594">Az.Accounts</span></span>
* <span data-ttu-id="f22d8-595">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметр AzureAnalysisServicesEndpointResourceId.</span><span class="sxs-lookup"><span data-stu-id="f22d8-595">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f22d8-596">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f22d8-596">Az.AnalysisServices</span></span>
* <span data-ttu-id="f22d8-597">Использование ServiceClient в командлетах плоскости данных и удаление исходной логики проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="f22d8-597">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="f22d8-598">Add-AzureASAccount используется как оболочка для Connect-AzAccount во избежание критических изменений.</span><span class="sxs-lookup"><span data-stu-id="f22d8-598">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f22d8-599">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f22d8-599">Az.Automation</span></span>
* <span data-ttu-id="f22d8-600">Исправлена ошибка командлета New-AzAutomationSoftwareUpdateConfiguration, связанная с включением.</span><span class="sxs-lookup"><span data-stu-id="f22d8-600">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="f22d8-601">Теперь параметры IncludedKbNumber и IncludedPackageNameMask должны работать нормально.</span><span class="sxs-lookup"><span data-stu-id="f22d8-601">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="f22d8-602">Исправлена ошибка динамической группы управления обновлениями службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="f22d8-602">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22d8-603">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22d8-603">Az.Compute</span></span>
* <span data-ttu-id="f22d8-604">В командлеты New-AzDiskConfig и New-AzSnapshotConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="f22d8-604">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="f22d8-605">Теперь можно создавать виртуальные машину на основе образов из коллекции от других клиентов.</span><span class="sxs-lookup"><span data-stu-id="f22d8-605">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="f22d8-606">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f22d8-606">Az.ContainerInstance</span></span>
* <span data-ttu-id="f22d8-607">Исправлена проблема в параметре -Command командлета New-AzContainerGroup, из-за которой в конце добавлялся пустой аргумент.</span><span class="sxs-lookup"><span data-stu-id="f22d8-607">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f22d8-608">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f22d8-608">Az.DataFactory</span></span>
* <span data-ttu-id="f22d8-609">Пакет SDK для ADF .NET обновлен до версии 3.0.2.</span><span class="sxs-lookup"><span data-stu-id="f22d8-609">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="f22d8-610">Командлет Set-AzDataFactoryV2 обновлен с помощью дополнительных параметров для настроек, связанных с RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f22d8-610">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f22d8-611">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22d8-611">Az.Resources</span></span>
* <span data-ttu-id="f22d8-612">Улучшена обработка поставщиков Get-AzResource при предоставлении параметров -ResourceId или -ResourceGroupName, -Name и -ResourceType.</span><span class="sxs-lookup"><span data-stu-id="f22d8-612">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="f22d8-613">Улучшена обработка ошибок в командлетах Test-AzDeployment и Test-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="f22d8-613">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="f22d8-614">Теперь ошибки, возникающие за пределами проверки развертывания, обрабатываются и включаются в выходные данные команды.</span><span class="sxs-lookup"><span data-stu-id="f22d8-614">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="f22d8-615">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="f22d8-615">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="f22d8-616">Добавлен параметр-переключатель -IgnoreDynamicParameters, с помощью которого можно настроить командлеты развертывания так, чтобы они пропускали запросы в сценариях скриптов и заданий.</span><span class="sxs-lookup"><span data-stu-id="f22d8-616">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="f22d8-617">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="f22d8-617">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="f22d8-618">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22d8-618">Az.Sql</span></span>
* <span data-ttu-id="f22d8-619">Поддержка классификации данных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="f22d8-619">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f22d8-620">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f22d8-620">Az.Storage</span></span>
* <span data-ttu-id="f22d8-621">Подробные сообщения об ошибке передаются при создании контекста хранилища с помощью параметра -UseConnectedAccount, но без входа в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="f22d8-621">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="f22d8-622">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f22d8-622">New-AzStorageContext</span></span>
* <span data-ttu-id="f22d8-623">Поддержка свойств службы управления BLOB-объектов в указанной учетной записи хранения с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="f22d8-623">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="f22d8-624">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="f22d8-624">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="f22d8-625">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="f22d8-625">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="f22d8-626">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f22d8-626">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="f22d8-627">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f22d8-627">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="f22d8-628">Поддержка параметра -AsJob в командлетах для отправки и скачивания больших двоичных объектов и файлов.</span><span class="sxs-lookup"><span data-stu-id="f22d8-628">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="f22d8-629">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f22d8-629">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="f22d8-630">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f22d8-630">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="f22d8-631">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f22d8-631">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="f22d8-632">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f22d8-632">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="f22d8-633">1.6.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f22d8-633">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f22d8-634">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="f22d8-634">Highlights since the last major release</span></span>
* <span data-ttu-id="f22d8-635">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="f22d8-635">General availability of `Az` module</span></span>
* <span data-ttu-id="f22d8-636">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="f22d8-636">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="f22d8-637">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="f22d8-637">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="f22d8-638">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="f22d8-638">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="f22d8-639">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="f22d8-639">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f22d8-640">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="f22d8-640">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="f22d8-641">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="f22d8-641">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f22d8-642">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f22d8-642">Az.Automation</span></span>
* <span data-ttu-id="f22d8-643">В управление обновлениями службы автоматизации Azure внесены изменения для поддержки следующих новых функций:</span><span class="sxs-lookup"><span data-stu-id="f22d8-643">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="f22d8-644">динамическое группирование;</span><span class="sxs-lookup"><span data-stu-id="f22d8-644">Dynamic grouping</span></span>
    * <span data-ttu-id="f22d8-645">скрипты предварительного или последующего выполнения;</span><span class="sxs-lookup"><span data-stu-id="f22d8-645">Pre-Post script</span></span>
    * <span data-ttu-id="f22d8-646">параметр перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="f22d8-646">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22d8-647">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22d8-647">Az.Compute</span></span>
* <span data-ttu-id="f22d8-648">Устранена проблема, связанная с разрешением пути в Get-AzVmBootDiagnosticsData.</span><span class="sxs-lookup"><span data-stu-id="f22d8-648">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="f22d8-649">Обновление клиентской библиотеки вычислений до версии 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="f22d8-649">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f22d8-650">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f22d8-650">Az.KeyVault</span></span>
* <span data-ttu-id="f22d8-651">Добавлена поддержка подстановочных знаков в командлетах KeyVault.</span><span class="sxs-lookup"><span data-stu-id="f22d8-651">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f22d8-652">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22d8-652">Az.Network</span></span>
* <span data-ttu-id="f22d8-653">Добавлена поддержка анализа угроз для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="f22d8-653">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="f22d8-654">Добавлены настраиваемые правила и ресурс верхнего уровня для политики брандмауэра Шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="f22d8-654">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f22d8-655">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f22d8-655">Az.RecoveryServices</span></span>
* <span data-ttu-id="f22d8-656">В политику виртуальной машины Azure добавлен объект SnapshotRetentionInDays для поддержки мгновенного восстановления.</span><span class="sxs-lookup"><span data-stu-id="f22d8-656">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="f22d8-657">Добавлена поддержка канала для отмены регистрации контейнера.</span><span class="sxs-lookup"><span data-stu-id="f22d8-657">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="f22d8-658">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22d8-658">Az.Resources</span></span>
* <span data-ttu-id="f22d8-659">Обновлена поддержка подстановочных знаков для Get-AzResource и Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f22d8-659">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="f22d8-660">Обновлены учетные данные, используемые при общих вызовах к ARM.</span><span class="sxs-lookup"><span data-stu-id="f22d8-660">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="f22d8-661">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22d8-661">Az.Sql</span></span>
* <span data-ttu-id="f22d8-662">Изменен тип параметра (ExcludeDetectionType) командлетов для обнаружения угроз с DetectionTypes на string[] для поддержки актуального состояния при добавлении новых типов обнаружения и для поддержки автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="f22d8-662">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f22d8-663">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f22d8-663">Az.Storage</span></span>
* <span data-ttu-id="f22d8-664">Поддержка получения, настройки и удаления политики управления в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="f22d8-664">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="f22d8-665">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f22d8-665">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="f22d8-666">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f22d8-666">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="f22d8-667">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f22d8-667">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="f22d8-668">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="f22d8-668">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="f22d8-669">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="f22d8-669">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="f22d8-670">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="f22d8-670">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f22d8-671">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f22d8-671">Az.Websites</span></span>
* <span data-ttu-id="f22d8-672">Исправлена ошибка с шаблоном ARM, из-за которой прерывалось клонирование все слотов при использовании New-AzWebApp -IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="f22d8-672">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="f22d8-673">1.5.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f22d8-673">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f22d8-674">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f22d8-674">Az.Accounts</span></span>
* <span data-ttu-id="f22d8-675">Добавлена команда Register-AzModule для поддержки созданных командлетов AutoRest.</span><span class="sxs-lookup"><span data-stu-id="f22d8-675">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="f22d8-676">Обновлены примеры для Connect AzAccount.</span><span class="sxs-lookup"><span data-stu-id="f22d8-676">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f22d8-677">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f22d8-677">Az.Automation</span></span>
* <span data-ttu-id="f22d8-678">Исправлена проблема с получением некоторых ежемесячных расписаний в нескольких командлетах службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="f22d8-678">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="f22d8-679">Исправлен командлет Get-AzAutomationDscNode, возвращающий только первые 20 узлов.</span><span class="sxs-lookup"><span data-stu-id="f22d8-679">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="f22d8-680">Теперь он возвращает все узлы.</span><span class="sxs-lookup"><span data-stu-id="f22d8-680">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f22d8-681">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f22d8-681">Az.Cdn</span></span>
* <span data-ttu-id="f22d8-682">Добавлены новые командлеты PowerShell для включения и отключения HTTPS для личного домена и отключены устаревшие командлеты.</span><span class="sxs-lookup"><span data-stu-id="f22d8-682">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22d8-683">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22d8-683">Az.Compute</span></span>
* <span data-ttu-id="f22d8-684">Добавлена поддержка подстановочных знаков в командлетах Get.</span><span class="sxs-lookup"><span data-stu-id="f22d8-684">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f22d8-685">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f22d8-685">Az.DataFactory</span></span>
* <span data-ttu-id="f22d8-686">Обновлен пакет SDK для ADF .NET до версии 3.0.1.</span><span class="sxs-lookup"><span data-stu-id="f22d8-686">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f22d8-687">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f22d8-687">Az.LogicApp</span></span>
* <span data-ttu-id="f22d8-688">Исправлена проблема с получением только первой страницы результатов при выполнении команды ListWorkflows.</span><span class="sxs-lookup"><span data-stu-id="f22d8-688">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f22d8-689">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22d8-689">Az.Network</span></span>
* <span data-ttu-id="f22d8-690">Добавлена поддержка подстановочных знаков в командлетах Network.</span><span class="sxs-lookup"><span data-stu-id="f22d8-690">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f22d8-691">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f22d8-691">Az.RecoveryServices</span></span>
* <span data-ttu-id="f22d8-692">Добавлена поддержка SQL Server на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="f22d8-692">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="f22d8-693">Обновление пакета SDK</span><span class="sxs-lookup"><span data-stu-id="f22d8-693">SDK Update</span></span>
* <span data-ttu-id="f22d8-694">Удалена проверка VMappContainer в Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="f22d8-694">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="f22d8-695">Добавлены параметры Name и ServerName для Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="f22d8-695">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="f22d8-696">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22d8-696">Az.Resources</span></span>
* <span data-ttu-id="f22d8-697">Добавлен параметр `-TemplateObject` в командлеты для развертывания.</span><span class="sxs-lookup"><span data-stu-id="f22d8-697">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="f22d8-698">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2933.</span><span class="sxs-lookup"><span data-stu-id="f22d8-698">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="f22d8-699">Устранена проблема с передачей в конвейер результата `Get-AzResource` для `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="f22d8-699">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="f22d8-700">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8240.</span><span class="sxs-lookup"><span data-stu-id="f22d8-700">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="f22d8-701">Устранена проблема с изменением типа данных JSON при выполнении `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="f22d8-701">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="f22d8-702">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7930.</span><span class="sxs-lookup"><span data-stu-id="f22d8-702">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="f22d8-703">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22d8-703">Az.Sql</span></span>
* <span data-ttu-id="f22d8-704">Обновление AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="f22d8-704">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="f22d8-705">Исправлено поведение для пограничного случая при создании параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="f22d8-705">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f22d8-706">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f22d8-706">Az.Storage</span></span>
* <span data-ttu-id="f22d8-707">Включена поддержка Kind BlockBlobStorage при создании учетной записи хранения для New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="f22d8-707">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="f22d8-708">1.4.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f22d8-708">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="f22d8-709">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f22d8-709">Az.AnalysisServices</span></span>
* <span data-ttu-id="f22d8-710">Командлет AddAzureASAccount устарел.</span><span class="sxs-lookup"><span data-stu-id="f22d8-710">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f22d8-711">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f22d8-711">Az.Automation</span></span>
* <span data-ttu-id="f22d8-712">Обновлена справка для командлета Import-AzAutomationDscNodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f22d8-712">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="f22d8-713">Добавлена проверка имени конфигурации для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f22d8-713">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="f22d8-714">Улучшена обработка ошибок для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f22d8-714">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f22d8-715">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f22d8-715">Az.CognitiveServices</span></span>
* <span data-ttu-id="f22d8-716">Добавлен параметр CustomSubdomainName — новый необязательный параметр для командлета New-AzCognitiveServicesAccount, который указывает поддомен для ресурса.</span><span class="sxs-lookup"><span data-stu-id="f22d8-716">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22d8-717">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22d8-717">Az.Compute</span></span>
* <span data-ttu-id="f22d8-718">Устранена проблема с идентификаторами наборов параметров.</span><span class="sxs-lookup"><span data-stu-id="f22d8-718">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="f22d8-719">Обновлен командлет Get-AzVMExtension для отображения списка всех установленных расширений, если не указан параметр Name.</span><span class="sxs-lookup"><span data-stu-id="f22d8-719">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="f22d8-720">Для командлета Update-AzImage добавлены параметры Tag и ResourceId.</span><span class="sxs-lookup"><span data-stu-id="f22d8-720">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="f22d8-721">Командлет Get-AzVmssVM, который выполняется без указания идентификатора экземпляра и с параметром InstanceView, может выводить виртуальные машины из VMSS с представлением экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f22d8-721">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f22d8-722">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f22d8-722">Az.DataLakeStore</span></span>
* <span data-ttu-id="f22d8-723">Добавлены командлеты для перечисления и восстановления удаленного элемента ADL.</span><span class="sxs-lookup"><span data-stu-id="f22d8-723">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f22d8-724">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f22d8-724">Az.EventHub</span></span>
* <span data-ttu-id="f22d8-725">Добавлено новое логическое свойство SkipEmptyArchives для пропуска пустых архивов в классе CaptureDescription Eventhub.</span><span class="sxs-lookup"><span data-stu-id="f22d8-725">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="f22d8-726">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f22d8-726">Az.KeyVault</span></span>
* <span data-ttu-id="f22d8-727">Исправлена расстановка тегов для командлета Set-AzKeyVaultSecret.</span><span class="sxs-lookup"><span data-stu-id="f22d8-727">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f22d8-728">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f22d8-728">Az.LogicApp</span></span>
* <span data-ttu-id="f22d8-729">Добавлен SKU "Базовый" для учетных записей интеграции.</span><span class="sxs-lookup"><span data-stu-id="f22d8-729">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="f22d8-730">Добавлены типы сопоставлений Liquid, а также XSLT 2.0 и XSLT 3.0.</span><span class="sxs-lookup"><span data-stu-id="f22d8-730">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="f22d8-731">Новые командлеты для сборок учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="f22d8-731">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="f22d8-732">Get-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="f22d8-732">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="f22d8-733">New-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="f22d8-733">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="f22d8-734">Remove-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="f22d8-734">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="f22d8-735">Set-AzIntegrationAccountAssembly.</span><span class="sxs-lookup"><span data-stu-id="f22d8-735">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="f22d8-736">Новые командлеты для конфигурации пакета учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="f22d8-736">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="f22d8-737">Get-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="f22d8-737">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="f22d8-738">New-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="f22d8-738">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="f22d8-739">Remove-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="f22d8-739">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="f22d8-740">Set-AzIntegrationAccountBatchConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f22d8-740">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="f22d8-741">Обновлен пакет SDK Logic Apps до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="f22d8-741">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f22d8-742">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f22d8-742">Az.Monitor</span></span>
* <span data-ttu-id="f22d8-743">Обновлена справка для командлета Get-AzMetric.</span><span class="sxs-lookup"><span data-stu-id="f22d8-743">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f22d8-744">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22d8-744">Az.Network</span></span>
* <span data-ttu-id="f22d8-745">Обновлен пример справки для командлета Add-AzApplicationGatewayCustomError.</span><span class="sxs-lookup"><span data-stu-id="f22d8-745">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f22d8-746">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f22d8-746">Az.OperationalInsights</span></span>
* <span data-ttu-id="f22d8-747">Дополнительная поддержка создания и получения источников данных ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="f22d8-747">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="f22d8-748">Добавлен новый тип ApplicationInsights для получения определенных или всех источников данных ApplicationInsights для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="f22d8-748">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="f22d8-749">Добавлен командлет New-AzOperationalInsightsApplicationInsightsDataSource для создания источника данных с использованием параметров указанного ресурса Application-Insightss: subscription Id, resourceGroupName и name.</span><span class="sxs-lookup"><span data-stu-id="f22d8-749">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="f22d8-750">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22d8-750">Az.Resources</span></span>
* <span data-ttu-id="f22d8-751">исправлена проблема https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="f22d8-751">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="f22d8-752">исправлена проблема https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="f22d8-752">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="f22d8-753">исправлена проблема https://github.com/Azure/azure-powershell/issues/6219.</span><span class="sxs-lookup"><span data-stu-id="f22d8-753">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="f22d8-754">Исправлена ошибка, препятствующая повторному созданию KeyCredentials.</span><span class="sxs-lookup"><span data-stu-id="f22d8-754">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="f22d8-755">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22d8-755">Az.Sql</span></span>
* <span data-ttu-id="f22d8-756">Добавлена поддержка уровня гипермасштабирования в базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="f22d8-756">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="f22d8-757">Исправлена ошибка, из-за которой восстановление могло завершиться со сбоем при указании ненужных свойств в запросе на восстановление.</span><span class="sxs-lookup"><span data-stu-id="f22d8-757">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f22d8-758">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f22d8-758">Az.Websites</span></span>
* <span data-ttu-id="f22d8-759">Исправлен пример для командлета Get-AzWebAppSlotMetrics.</span><span class="sxs-lookup"><span data-stu-id="f22d8-759">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="f22d8-760">1.3.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f22d8-760">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f22d8-761">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f22d8-761">Az.Accounts</span></span>
* <span data-ttu-id="f22d8-762">Обновление до последней версии ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="f22d8-762">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f22d8-763">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f22d8-763">Az.AnalysisServices</span></span>
<span data-ttu-id="f22d8-764">Общедоступная версия модуля Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="f22d8-764">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22d8-765">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22d8-765">Az.Compute</span></span>
* <span data-ttu-id="f22d8-766">Расширение AEM: добавлена поддержка дисков UltraSSD, P60, P70 и P80.</span><span class="sxs-lookup"><span data-stu-id="f22d8-766">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="f22d8-767">Обновлено описание справки для командлета Set-AzVMBootDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="f22d8-767">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="f22d8-768">Обновлено описание справки и пример для командлета Update-AzImage.</span><span class="sxs-lookup"><span data-stu-id="f22d8-768">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f22d8-769">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f22d8-769">Az.RecoveryServices</span></span>
<span data-ttu-id="f22d8-770">Общедоступная версия модуля Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="f22d8-770">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f22d8-771">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22d8-771">Az.Resources</span></span>
* <span data-ttu-id="f22d8-772">Исправлена расстановка тегов для групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f22d8-772">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="f22d8-773">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="f22d8-773">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="f22d8-774">Исправлена проблема с игнорированием командлетом `Get-AzureRmRoleAssignment` параметра -ErrorAction.</span><span class="sxs-lookup"><span data-stu-id="f22d8-774">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="f22d8-775">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="f22d8-775">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="f22d8-776">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22d8-776">Az.Sql</span></span>
* <span data-ttu-id="f22d8-777">Добавлен командлет Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="f22d8-777">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="f22d8-778">Исправлена проблема с появлением исключения NullRef при выполнении командлетов SQL, если не выполнен вход в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="f22d8-778">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="f22d8-779">Исправлено исключение NullRef в командлете Get-AzSqlCapability.</span><span class="sxs-lookup"><span data-stu-id="f22d8-779">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="f22d8-780">1.2.1 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f22d8-780">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f22d8-781">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f22d8-781">Az.Accounts</span></span>
* <span data-ttu-id="f22d8-782">Выпуск с правильной версией службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="f22d8-782">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f22d8-783">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f22d8-783">Az.AnalysisServices</span></span>
* <span data-ttu-id="f22d8-784">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="f22d8-784">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f22d8-785">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f22d8-785">Az.RecoveryServices</span></span>
* <span data-ttu-id="f22d8-786">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="f22d8-786">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="f22d8-787">1.2.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f22d8-787">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f22d8-788">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f22d8-788">Az.Accounts</span></span>
* <span data-ttu-id="f22d8-789">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="f22d8-789">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f22d8-790">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="f22d8-790">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f22d8-791">Добавлено предупреждающее сообщение в PS Core для модуля Uninstall-AzureRm.</span><span class="sxs-lookup"><span data-stu-id="f22d8-791">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="f22d8-792">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f22d8-792">Az.Aks</span></span>
* <span data-ttu-id="f22d8-793">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="f22d8-793">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f22d8-794">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f22d8-794">Az.Automation</span></span>
* <span data-ttu-id="f22d8-795">Добавлена поддержка для модулей runbook Python 2.</span><span class="sxs-lookup"><span data-stu-id="f22d8-795">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="f22d8-796">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="f22d8-796">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f22d8-797">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f22d8-797">Az.Cdn</span></span>
* <span data-ttu-id="f22d8-798">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="f22d8-798">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22d8-799">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22d8-799">Az.Compute</span></span>
* <span data-ttu-id="f22d8-800">Добавлен командлет Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="f22d8-800">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="f22d8-801">Добавлен параметр TempDisk к командлету Set-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="f22d8-801">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="f22d8-802">Исправлено предупреждающее сообщение командлета New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="f22d8-802">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="f22d8-803">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f22d8-803">Az.ContainerRegistry</span></span>
* <span data-ttu-id="f22d8-804">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="f22d8-804">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f22d8-805">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f22d8-805">Az.DataFactory</span></span>
* <span data-ttu-id="f22d8-806">Пакет SDK ADF .Net обновлен до версии 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="f22d8-806">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f22d8-807">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f22d8-807">Az.DataLakeStore</span></span>
* <span data-ttu-id="f22d8-808">Исправлена проблема с конечной точкой ADLS при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="f22d8-808">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="f22d8-809">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7462.</span><span class="sxs-lookup"><span data-stu-id="f22d8-809">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="f22d8-810">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="f22d8-810">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f22d8-811">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f22d8-811">Az.IotHub</span></span>
* <span data-ttu-id="f22d8-812">Добавлен формат кодирования для командлета Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="f22d8-812">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f22d8-813">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f22d8-813">Az.KeyVault</span></span>
* <span data-ttu-id="f22d8-814">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="f22d8-814">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f22d8-815">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22d8-815">Az.Network</span></span>
* <span data-ttu-id="f22d8-816">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="f22d8-816">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="f22d8-817">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22d8-817">Az.Resources</span></span>
* <span data-ttu-id="f22d8-818">Исправлены неправильные примеры в справочной документации по командлетам New-AzADAppCredential и New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="f22d8-818">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="f22d8-819">Исправлена проблема, при которой путь для параметра -TemplateFile не удавалось разрешить до выполнения командлетов развертывания групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f22d8-819">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="f22d8-820">Az.Resources: исправлена документация для значения по умолчанию -Mode командлета New-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="f22d8-820">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="f22d8-821">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/7522.</span><span class="sxs-lookup"><span data-stu-id="f22d8-821">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="f22d8-822">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/5747.</span><span class="sxs-lookup"><span data-stu-id="f22d8-822">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="f22d8-823">Исправлена проблема с форматированием объекта PSResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="f22d8-823">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="f22d8-824">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2123.</span><span class="sxs-lookup"><span data-stu-id="f22d8-824">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f22d8-825">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f22d8-825">Az.ServiceFabric</span></span>
* <span data-ttu-id="f22d8-826">Исправлена проблема с появлением исключения в процессе отката при добавлении сертификата к модели VMSS: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="f22d8-826">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="f22d8-827">Исправлены некоторые сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="f22d8-827">Fix some error messages.</span></span>
* <span data-ttu-id="f22d8-828">Исправлена проблема с созданием кластера с шаблоном ARM по умолчанию для командлета New-AzServiceFabriCluster, который не работал с операцией миграции в Az.</span><span class="sxs-lookup"><span data-stu-id="f22d8-828">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="f22d8-829">Исправлена проблема с добавлением сертификата кластера или приложения: теперь они добавляются только в Масштабируемые наборы виртуальных машин, которые сопоставлены с кластером, путем проверки идентификатора кластера в расширении.</span><span class="sxs-lookup"><span data-stu-id="f22d8-829">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="f22d8-830">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="f22d8-830">Az.SignalR</span></span>
* <span data-ttu-id="f22d8-831">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="f22d8-831">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="f22d8-832">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22d8-832">Az.Sql</span></span>
* <span data-ttu-id="f22d8-833">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="f22d8-833">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f22d8-834">Обновлено описание параметра LicenseType с добавлением возможных значений.</span><span class="sxs-lookup"><span data-stu-id="f22d8-834">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="f22d8-835">Исправлена проблема с неправильным обновлением удостоверения управляемого экземпляра, если оно было единственным обновляемым свойством.</span><span class="sxs-lookup"><span data-stu-id="f22d8-835">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="f22d8-836">Поддержка пользовательских параметров сортировки в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="f22d8-836">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f22d8-837">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f22d8-837">Az.Storage</span></span>
* <span data-ttu-id="f22d8-838">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="f22d8-838">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f22d8-839">Добавлен вывод подробных сообщений об ошибке при получении или установке классических свойств ведения журнала или метрик в учетной записи хранилища класса Premium, так как учетная запись хранилища класса Premium не поддерживает классические функции ведения журнала и метрик.</span><span class="sxs-lookup"><span data-stu-id="f22d8-839">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="f22d8-840">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="f22d8-840">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="f22d8-841">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="f22d8-841">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="f22d8-842">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="f22d8-842">Az.TrafficManager</span></span>
* <span data-ttu-id="f22d8-843">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="f22d8-843">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f22d8-844">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f22d8-844">Az.Websites</span></span>
* <span data-ttu-id="f22d8-845">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="f22d8-845">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f22d8-846">Исправлена работа командлета New-AzWebAppSSLBinding: сертификат отправляется в правильную группу ресурсов и правильное расположение, если приложение размещено в ASE.</span><span class="sxs-lookup"><span data-stu-id="f22d8-846">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="f22d8-847">Исправлена работа командлета New-AzWebAppSSLBinding: теги не перезаписываются при привязке SSL-сертификата к приложению.</span><span class="sxs-lookup"><span data-stu-id="f22d8-847">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="f22d8-848">1.1.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f22d8-848">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f22d8-849">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f22d8-849">Az.Accounts</span></span>
* <span data-ttu-id="f22d8-850">Добавление области "Local" в Enable-AzureRmAlias.</span><span class="sxs-lookup"><span data-stu-id="f22d8-850">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22d8-851">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22d8-851">Az.Compute</span></span>
* <span data-ttu-id="f22d8-852">Теперь имя не является обязательным в идентификаторе набора параметров для Restart/Start/Stop/Remove/Set-AzVM и Save-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="f22d8-852">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="f22d8-853">Обновлено описание идентификатора в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="f22d8-853">Updated the description of ID in help files</span></span>
* <span data-ttu-id="f22d8-854">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="f22d8-854">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f22d8-855">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f22d8-855">Az.DataLakeStore</span></span>
* <span data-ttu-id="f22d8-856">Обновление версии пакета SDK для плоскости данных до 1.1.14 для устранения найденных проблем.</span><span class="sxs-lookup"><span data-stu-id="f22d8-856">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="f22d8-857">Исправлена обработка отрицательного времени доступа и времени изменения для getfilestatus и liststatus, исправлен токен отмены для асинхронных методов.</span><span class="sxs-lookup"><span data-stu-id="f22d8-857">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f22d8-858">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f22d8-858">Az.EventGrid</span></span>
* <span data-ttu-id="f22d8-859">Обновление для использования API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="f22d8-859">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="f22d8-860">Обновлены указанные ниже командлеты для поддержки нового сценария в API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="f22d8-860">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="f22d8-861">New-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="f22d8-861">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="f22d8-862">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="f22d8-862">Event Time-To-Live,</span></span>
        - <span data-ttu-id="f22d8-863">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="f22d8-863">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="f22d8-864">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="f22d8-864">Dead letter endpoint.</span></span>
    - <span data-ttu-id="f22d8-865">Update-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="f22d8-865">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="f22d8-866">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="f22d8-866">Event Time-To-Live,</span></span>
        - <span data-ttu-id="f22d8-867">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="f22d8-867">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="f22d8-868">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="f22d8-868">Dead letter endpoint.</span></span>
* <span data-ttu-id="f22d8-869">Для параметра EndpointType добавлены новые значения перечисления (storageQueue и hybridConnection) в командлеты New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="f22d8-869">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="f22d8-870">Если ожидается, что создание или обновление подписки на событие повлечет за собой действия со стороны пользователя, выполняемые вручную, отображается предупреждение при создании или обновлении подписки события.</span><span class="sxs-lookup"><span data-stu-id="f22d8-870">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f22d8-871">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f22d8-871">Az.IotHub</span></span>
* <span data-ttu-id="f22d8-872">Пакет SDK Центра Интернета вещей обновлен до последней версии.</span><span class="sxs-lookup"><span data-stu-id="f22d8-872">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f22d8-873">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f22d8-873">Az.LogicApp</span></span>
* <span data-ttu-id="f22d8-874">Get-AzLogicApp позволяет перечислить все параметры без указанного имени.</span><span class="sxs-lookup"><span data-stu-id="f22d8-874">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="f22d8-875">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22d8-875">Az.Resources</span></span>
* <span data-ttu-id="f22d8-876">Исправлена проблема с набором параметров при предоставлении параметров "-ODataQuery" и "-ResourceId" для "Get-AzResource".</span><span class="sxs-lookup"><span data-stu-id="f22d8-876">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="f22d8-877">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7875.</span><span class="sxs-lookup"><span data-stu-id="f22d8-877">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="f22d8-878">Исправлена обработка параметра -Custom в New/Set-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="f22d8-878">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="f22d8-879">Исправлена опечатка в документации по New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="f22d8-879">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="f22d8-880">Параметр "-MailNickname" стал обязательным для "New-AzADUser".</span><span class="sxs-lookup"><span data-stu-id="f22d8-880">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="f22d8-881">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8220.</span><span class="sxs-lookup"><span data-stu-id="f22d8-881">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="f22d8-882">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="f22d8-882">Az.SignalR</span></span>
* <span data-ttu-id="f22d8-883">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="f22d8-883">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="f22d8-884">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22d8-884">Az.Sql</span></span>
* <span data-ttu-id="f22d8-885">Зависимость клиента управления хранением преобразована для общей реализации в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="f22d8-885">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f22d8-886">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f22d8-886">Az.Storage</span></span>
* <span data-ttu-id="f22d8-887">Установка параметра StorageAccountName для контекста хранилища в качестве реального имени учетной записи хранения, если она была создана с использованием токена Sas, OAuth или анонимного доступа.</span><span class="sxs-lookup"><span data-stu-id="f22d8-887">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="f22d8-888">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f22d8-888">New-AzStorageContext</span></span>
* <span data-ttu-id="f22d8-889">Создание токена Sas большого двоичного объекта моментального снимка с параметром "-FullUri". Возвращаемый URI исправлен на URI моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="f22d8-889">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="f22d8-890">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="f22d8-890">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f22d8-891">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f22d8-891">Az.Websites</span></span>
* <span data-ttu-id="f22d8-892">Исправлена ошибка синтаксического анализа даты в "Get-AzDeletedWebApp".</span><span class="sxs-lookup"><span data-stu-id="f22d8-892">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="f22d8-893">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="f22d8-893">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="f22d8-894">1.0.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="f22d8-894">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="f22d8-895">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="f22d8-895">General</span></span>

- <span data-ttu-id="f22d8-896">Общедоступная версия модуля Az.</span><span class="sxs-lookup"><span data-stu-id="f22d8-896">General Availability of Az Module</span></span>
- <span data-ttu-id="f22d8-897">Справка в Интернете для каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="f22d8-897">Online help for each module</span></span>
- <span data-ttu-id="f22d8-898">Дополнительные сведения и стратегию развития см. в статье [Announcing New Module 'Az'](https://aka.ms/azps-announce) (Объявление о новом модуле Az)</span><span class="sxs-lookup"><span data-stu-id="f22d8-898">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="f22d8-899">Сведения о миграции с AzureRM см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="f22d8-899">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="f22d8-900">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f22d8-900">Az.Accounts</span></span>
- <span data-ttu-id="f22d8-901">Изменено с Az.Profile.</span><span class="sxs-lookup"><span data-stu-id="f22d8-901">Changed from Az.Profile</span></span>
- <span data-ttu-id="f22d8-902">Исправлены форматы таблиц для типов профиля и контекста.</span><span class="sxs-lookup"><span data-stu-id="f22d8-902">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="f22d8-903">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f22d8-903">Az.ApiManagement</span></span>
- <span data-ttu-id="f22d8-904">Исправления для #7002.</span><span class="sxs-lookup"><span data-stu-id="f22d8-904">Fixes for #7002</span></span>
- <span data-ttu-id="f22d8-905">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="f22d8-905">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="f22d8-906">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f22d8-906">Az.Batch</span></span>
- <span data-ttu-id="f22d8-907">Добавлена возможность видеть, какая версия агента узла пакетной службы Azure работает в пуле на каждой виртуальной машине, с помощью нового свойства `NodeAgentInformation` в `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="f22d8-907">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="f22d8-908">Значение `Caching` по умолчанию для `PSDataDisk` теперь `ReadWrite` вместо `None`.</span><span class="sxs-lookup"><span data-stu-id="f22d8-908">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="f22d8-909">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="f22d8-909">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="f22d8-910">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="f22d8-910">Az.Billing</span></span>
- <span data-ttu-id="f22d8-911">Объединены командлеты Billing, Consumption и UsageAggregates. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0).</span><span class="sxs-lookup"><span data-stu-id="f22d8-911">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="f22d8-912">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="f22d8-912">Az.CognitivServices</span></span>
- <span data-ttu-id="f22d8-913">Добавлены средства заполнения для SkuName и Typem, доступные в операции New-AzureRmCognitiveServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="f22d8-913">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="f22d8-914">Удален набор параметров GetSkusWithAccountParamSetName из Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="f22d8-914">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="f22d8-915">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f22d8-915">Az.ContainerInstance</span></span>
- <span data-ttu-id="f22d8-916">Добавлена поддержка ManagedIdentity.</span><span class="sxs-lookup"><span data-stu-id="f22d8-916">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="f22d8-917">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="f22d8-917">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="f22d8-918">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="f22d8-918">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="f22d8-919">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f22d8-919">Az.DataLakeStore</span></span>
- <span data-ttu-id="f22d8-920">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="f22d8-920">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="f22d8-921">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f22d8-921">Az.Monitor</span></span>
- <span data-ttu-id="f22d8-922">"Az.Insights" переименован в "Az.Monitor" и внесены другие незначительные критические изменения. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="f22d8-922">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="f22d8-923">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f22d8-923">Az.KeyVault</span></span>
- <span data-ttu-id="f22d8-924">Из типов вывода удалено устаревшее свойство PurgeDisabled</span><span class="sxs-lookup"><span data-stu-id="f22d8-924">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="f22d8-925">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="f22d8-925">Az.MachineLearning</span></span>
- <span data-ttu-id="f22d8-926">Включены командлеты из модуля Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="f22d8-926">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="f22d8-927">Az.Media</span><span class="sxs-lookup"><span data-stu-id="f22d8-927">Az.Media</span></span>
- <span data-ttu-id="f22d8-928">Удаляет устаревший псевдоним Tags из New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="f22d8-928">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="f22d8-929">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22d8-929">Az.Network</span></span>
<span data-ttu-id="f22d8-930">В шлюз приложений добавлена поддержка настройки RewriteRuleSets</span><span class="sxs-lookup"><span data-stu-id="f22d8-930">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="f22d8-931">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="f22d8-931">New cmdlets added:</span></span>
        - <span data-ttu-id="f22d8-932">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f22d8-932">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f22d8-933">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f22d8-933">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f22d8-934">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f22d8-934">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f22d8-935">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f22d8-935">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f22d8-936">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f22d8-936">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f22d8-937">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="f22d8-937">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="f22d8-938">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="f22d8-938">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="f22d8-939">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="f22d8-939">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="f22d8-940">В следующие командлеты добавлен необязательный параметр -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f22d8-940">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="f22d8-941">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f22d8-941">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="f22d8-942">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f22d8-942">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="f22d8-943">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f22d8-943">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="f22d8-944">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f22d8-944">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="f22d8-945">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f22d8-945">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="f22d8-946">New-AzureRmApplicationGatewayUrlPathMapConfig добавил с помощью идентификатора поддержку KeyVault для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="f22d8-946">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="f22d8-947">В следующие командлеты добавлен необязательный параметр -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f22d8-947">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="f22d8-948">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f22d8-948">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="f22d8-949">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f22d8-949">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="f22d8-950">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f22d8-950">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="f22d8-951">В командлет New-AzApplicationGateway добавлен необязательный параметр -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="f22d8-951">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="f22d8-952">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="f22d8-952">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="f22d8-953">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f22d8-953">Az.OperationalInsights</span></span>
- <span data-ttu-id="f22d8-954">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="f22d8-954">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="f22d8-955">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f22d8-955">Az.Profile</span></span>
- <span data-ttu-id="f22d8-956">Имя модуля изменено на Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="f22d8-956">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="f22d8-957">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f22d8-957">Az.RecoveryServices</span></span>
- <span data-ttu-id="f22d8-958">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="f22d8-958">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="f22d8-959">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22d8-959">Az.Resources</span></span>
- <span data-ttu-id="f22d8-960">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="f22d8-960">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="f22d8-961">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f22d8-961">Az.ServiceFabric</span></span>
- <span data-ttu-id="f22d8-962">Поддержка спецификации сертификата по общему имени и отпечатку</span><span class="sxs-lookup"><span data-stu-id="f22d8-962">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="f22d8-963">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="f22d8-963">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="f22d8-964">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="f22d8-964">Az.SIgnalR</span></span>
- <span data-ttu-id="f22d8-965">Общедоступная версия командлетов PowerShell для SIgnalR</span><span class="sxs-lookup"><span data-stu-id="f22d8-965">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="f22d8-966">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22d8-966">Az.Sql</span></span>
- <span data-ttu-id="f22d8-967">Добавлены новые типы обнаружения Data_Exfiltration и Unsafe_Action в командлеты обнаружения угроз</span><span class="sxs-lookup"><span data-stu-id="f22d8-967">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="f22d8-968">Примеры обновленной документации для командлетов аудита Sql</span><span class="sxs-lookup"><span data-stu-id="f22d8-968">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="f22d8-969">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="f22d8-969">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="f22d8-970">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f22d8-970">Az.Storage</span></span>
- <span data-ttu-id="f22d8-971">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="f22d8-971">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="f22d8-972">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f22d8-972">Az.Websites</span></span>
- <span data-ttu-id="f22d8-973">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="f22d8-973">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="f22d8-974">0.7.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="f22d8-974">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="f22d8-975">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="f22d8-975">General</span></span>

* <span data-ttu-id="f22d8-976">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="f22d8-976">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="f22d8-977">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22d8-977">Az.Compute</span></span>

* <span data-ttu-id="f22d8-978">Добавлена поддержка UltraSSD и образов коллекции в простых наборах параметров для командлетов `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="f22d8-978">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="f22d8-979">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f22d8-979">Az.DataLakeStore</span></span>

* <span data-ttu-id="f22d8-980">Исправлено косую черту в конце домена учетной записи ADLS</span><span class="sxs-lookup"><span data-stu-id="f22d8-980">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="f22d8-981">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f22d8-981">Az.FrontDoor</span></span>

* <span data-ttu-id="f22d8-982">Исправлены некоторые неработающие ссылки</span><span class="sxs-lookup"><span data-stu-id="f22d8-982">Fixed some broken links</span></span>
    - <span data-ttu-id="f22d8-983">В статьях New-AzureRmFrontDoor и Set-AzureRmFrontDoor исправлена ссылка на статью командлета New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="f22d8-983">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="f22d8-984">В статье New-AzureRmFrontDoorManagedRuleObject исправлена ссылка на статью командлета New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="f22d8-984">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="f22d8-985">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f22d8-985">Az.RecoveryServices</span></span>

* <span data-ttu-id="f22d8-986">Добавлены проверки на стороне клиента для операций восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="f22d8-986">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="f22d8-987">StorageAccountName и storageAccountResourceGroupName являются необязательными для восстановления afs.</span><span class="sxs-lookup"><span data-stu-id="f22d8-987">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="f22d8-988">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22d8-988">Az.Resources</span></span>

* <span data-ttu-id="f22d8-989">Исправление для https://github.com/Azure/azure-powershell/issues/7679.</span><span class="sxs-lookup"><span data-stu-id="f22d8-989">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="f22d8-990">Обновите Get-AzureRmRoleAssignment, чтобы использовать область подписки, если она указана при запросе классических администраторов.</span><span class="sxs-lookup"><span data-stu-id="f22d8-990">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="f22d8-991">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22d8-991">Az.Sql</span></span>

* <span data-ttu-id="f22d8-992">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="f22d8-992">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="f22d8-993">Устранена проблема с использованием Get-AzureRmSqlDatabaseVulnerabilityAssessment с .NET Core.</span><span class="sxs-lookup"><span data-stu-id="f22d8-993">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="f22d8-994">Изменена документация справочных сообщений, связанных с командлетами аудита SQL.</span><span class="sxs-lookup"><span data-stu-id="f22d8-994">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="f22d8-995">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f22d8-995">Az.Storage</span></span>

* <span data-ttu-id="f22d8-996">Добавлено -EnableHierarchicalNamespace к New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f22d8-996">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="f22d8-997">Устранена проблема, из-за которой командлет Copy File не может повторно использовать исходный контекст в пункте назначения, если не введен -DestContext</span><span class="sxs-lookup"><span data-stu-id="f22d8-997">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="f22d8-998">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="f22d8-998">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="f22d8-999">Поддержка статической конфигурации сайта</span><span class="sxs-lookup"><span data-stu-id="f22d8-999">Support Static Website configuration</span></span>
    - <span data-ttu-id="f22d8-1000">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="f22d8-1000">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="f22d8-1001">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="f22d8-1001">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="f22d8-1002">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f22d8-1002">Az.Websites</span></span>

* <span data-ttu-id="f22d8-1003">Set-AzureRmWebApp и Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f22d8-1003">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="f22d8-1004">Добавлен новый параметр (-AzureStoragePath), который указывает путь службы хранилища Azure для подключения в приложениях-контейнерах Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1004">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="f22d8-1005">Используйте выходные данные нового командлета New-AzureRmWebAppAzureStoragePath в качестве параметра, чтобы задать пути к службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1005">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="f22d8-1006">0.6.1 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1006">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="f22d8-1007">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f22d8-1007">Az.ApiManagement</span></span>
* <span data-ttu-id="f22d8-1008">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1008">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="f22d8-1009">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f22d8-1009">Az.Automation</span></span>
* <span data-ttu-id="f22d8-1010">Командлеты службы автоматизации Azure на базе Swagger.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1010">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="f22d8-1011">Добавлены командлеты для Управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1011">Added Update Management cmdlets</span></span>
* <span data-ttu-id="f22d8-1012">Добавлены командлеты для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1012">Added Source Control cmdlets</span></span>
* <span data-ttu-id="f22d8-1013">Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1013">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="f22d8-1014">Исправлена команда DSC для регистрации узла.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1014">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="f22d8-1015">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22d8-1015">Az.Compute</span></span>
* <span data-ttu-id="f22d8-1016">Исправлена проблема с удостоверением, назначаемым системой.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1016">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="f22d8-1017">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1017">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="f22d8-1018">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f22d8-1018">Az.ContainerInstance</span></span>
* <span data-ttu-id="f22d8-1019">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1019">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="f22d8-1020">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="f22d8-1020">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="f22d8-1021">Обновлено описание в примерах командлетов для Marketplace.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1021">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="f22d8-1022">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22d8-1022">Az.Network</span></span>
* <span data-ttu-id="f22d8-1023">Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1023">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="f22d8-1024">Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1024">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="f22d8-1025">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1025">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="f22d8-1026">Исправлены проблемы с использованием памяти в карте виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1026">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="f22d8-1027">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="f22d8-1027">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="f22d8-1028">Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1028">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="f22d8-1029">Параметры часового пояса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1029">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="f22d8-1030">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="f22d8-1030">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="f22d8-1031">Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1031">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="f22d8-1032">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1032">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="f22d8-1033">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="f22d8-1033">Az.Relay</span></span>
* <span data-ttu-id="f22d8-1034">Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1034">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="f22d8-1035">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22d8-1035">Az.Resources</span></span>
* <span data-ttu-id="f22d8-1036">Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1036">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="f22d8-1037">Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1037">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="f22d8-1038">Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1038">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="f22d8-1039">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f22d8-1039">Az.ServiceFabric</span></span>
* <span data-ttu-id="f22d8-1040">Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1040">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="f22d8-1041">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22d8-1041">Az.Sql</span></span>
* <span data-ttu-id="f22d8-1042">Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1042">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="f22d8-1043">Get-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1043">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f22d8-1044">New-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1044">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f22d8-1045">Set-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1045">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f22d8-1046">Remove-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1046">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f22d8-1047">Get-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1047">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f22d8-1048">New-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1048">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f22d8-1049">Restore-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1049">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f22d8-1050">Remove-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1050">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="f22d8-1051">Добавлено расширенное управление политиками аудита для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1051">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="f22d8-1052">Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1052">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="f22d8-1053">Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1053">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="f22d8-1054">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1054">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="f22d8-1055">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1055">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="f22d8-1056">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1056">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="f22d8-1057">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1057">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="f22d8-1058">Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1058">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="f22d8-1059">0.5.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1059">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="f22d8-1060">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="f22d8-1060">General</span></span>
* <span data-ttu-id="f22d8-1061">Добавлены средства заполнения ресурсов для многих основных командлетов — они позволяют вам переключать существующие имена ресурсов при вызове командлетов в интерактивном режиме</span><span class="sxs-lookup"><span data-stu-id="f22d8-1061">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="f22d8-1062">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f22d8-1062">Az.Profile</span></span>
* <span data-ttu-id="f22d8-1063">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1063">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="f22d8-1064">В командлете Connect-AzAccount параметр TenantId переименован в Tenant и добавлен псевдоним для TenantId</span><span class="sxs-lookup"><span data-stu-id="f22d8-1064">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="f22d8-1065">Обновлено описание TenantId для командлета Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="f22d8-1065">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="f22d8-1066">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1066">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="f22d8-1067">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1067">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="f22d8-1068">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1068">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="f22d8-1069">Устранена проблема, при которой командлет Disconnect-AzAccount вызывал сбой при отсутствии подключения</span><span class="sxs-lookup"><span data-stu-id="f22d8-1069">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="f22d8-1070">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f22d8-1070">Az.CognitiveServices</span></span>
* <span data-ttu-id="f22d8-1071">Добавлена операция Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1071">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22d8-1072">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22d8-1072">Az.Compute</span></span>
* <span data-ttu-id="f22d8-1073">Добавлены командлеты Add-AzVmssVMDataDisk и Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="f22d8-1073">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="f22d8-1074">Get-AzVMImage отображает AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="f22d8-1074">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="f22d8-1075">Устранена проблема, при которой значения параметров SetAzVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1075">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f22d8-1076">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f22d8-1076">Az.DataLakeStore</span></span>
* <span data-ttu-id="f22d8-1077">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1077">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="f22d8-1078">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1078">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="f22d8-1079">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="f22d8-1079">Az.Insights</span></span>
* <span data-ttu-id="f22d8-1080">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="f22d8-1080">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="f22d8-1081">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="f22d8-1081">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="f22d8-1082">Исправлена проблема № 7513 [Insights], при которой для командлета Set-AzDiagnosticSetting требовалось явное указание категорий во время создания параметра</span><span class="sxs-lookup"><span data-stu-id="f22d8-1082">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="f22d8-1083">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1083">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f22d8-1084">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22d8-1084">Az.Network</span></span>
* <span data-ttu-id="f22d8-1085">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="f22d8-1085">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="f22d8-1086">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="f22d8-1086">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="f22d8-1087">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="f22d8-1087">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="f22d8-1088">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f22d8-1088">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="f22d8-1089">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="f22d8-1089">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="f22d8-1090">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="f22d8-1090">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="f22d8-1091">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f22d8-1091">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f22d8-1092">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f22d8-1092">Az.PolicyInsights</span></span>
* <span data-ttu-id="f22d8-1093">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1093">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="f22d8-1094">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22d8-1094">Az.Resources</span></span>
* <span data-ttu-id="f22d8-1095">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1095">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="f22d8-1096">Разрешено перечисление ресурсов с помощью параметра -ResourceId для командлета Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="f22d8-1096">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f22d8-1097">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f22d8-1097">Az.ServiceBus</span></span>
* <span data-ttu-id="f22d8-1098">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1098">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f22d8-1099">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f22d8-1099">Az.ServiceFabric</span></span>
* <span data-ttu-id="f22d8-1100">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1100">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="f22d8-1101">Исправлен командлет Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="f22d8-1101">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="f22d8-1102">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="f22d8-1102">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="f22d8-1103">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="f22d8-1103">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="f22d8-1104">Исправлен командлет Update-AzServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1104">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="f22d8-1105">0.4.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1105">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="f22d8-1106">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f22d8-1106">Az.Profile</span></span>
* <span data-ttu-id="f22d8-1107">Устранена проблема с Get-AzSubscription в CloudShell</span><span class="sxs-lookup"><span data-stu-id="f22d8-1107">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="f22d8-1108">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1108">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22d8-1109">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22d8-1109">Az.Compute</span></span>
* <span data-ttu-id="f22d8-1110">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzVm</span><span class="sxs-lookup"><span data-stu-id="f22d8-1110">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="f22d8-1111">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1111">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f22d8-1112">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f22d8-1112">Az.DataLakeStore</span></span>
* <span data-ttu-id="f22d8-1113">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="f22d8-1113">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="f22d8-1114">Get-AzDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1114">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="f22d8-1115">Add-AzDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1115">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="f22d8-1116">Set-AzDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1116">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="f22d8-1117">Remove-AzDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1117">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f22d8-1118">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22d8-1118">Az.Network</span></span>
* <span data-ttu-id="f22d8-1119">Обновлен командлет Test-AzNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1119">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="f22d8-1120">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1120">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f22d8-1121">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22d8-1121">Az.Resources</span></span>
* <span data-ttu-id="f22d8-1122">Устранена проблема, из-за которой командлет Get-AzRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), благодаря добавлению понятного исключения в сценарий.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1122">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="f22d8-1123">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1123">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="f22d8-1124">0.3.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1124">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="f22d8-1125">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="f22d8-1125">Azure.Storage</span></span>
* <span data-ttu-id="f22d8-1126">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1126">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="f22d8-1127">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f22d8-1127">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="f22d8-1128">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="f22d8-1128">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="f22d8-1129">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1129">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="f22d8-1130">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="f22d8-1130">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="f22d8-1131">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f22d8-1131">Az.CognitiveServices</span></span>
* <span data-ttu-id="f22d8-1132">Поддержка Get-AzCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1132">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22d8-1133">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22d8-1133">Az.Compute</span></span>
* <span data-ttu-id="f22d8-1134">Исправлена команда Get-AzVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов</span><span class="sxs-lookup"><span data-stu-id="f22d8-1134">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="f22d8-1135">Добавлен пример использования SimpleParameterSet в справку командлета New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1135">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="f22d8-1136">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1136">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="f22d8-1137">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f22d8-1137">Az.DataFactoryV2</span></span>
* <span data-ttu-id="f22d8-1138">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1138">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f22d8-1139">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22d8-1139">Az.Network</span></span>
* <span data-ttu-id="f22d8-1140">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1140">Added NetworkProfile functionality.</span></span> <span data-ttu-id="f22d8-1141">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="f22d8-1141">new cmdlets added</span></span>
    - <span data-ttu-id="f22d8-1142">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f22d8-1142">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="f22d8-1143">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f22d8-1143">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="f22d8-1144">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f22d8-1144">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="f22d8-1145">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f22d8-1145">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="f22d8-1146">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="f22d8-1146">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="f22d8-1147">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="f22d8-1147">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="f22d8-1148">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1148">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="f22d8-1149">Добавлены командлеты: New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="f22d8-1149">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="f22d8-1150">Добавлены командлеты: Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="f22d8-1150">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f22d8-1151">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f22d8-1151">Az.RedisCache</span></span>
* <span data-ttu-id="f22d8-1152">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1152">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="f22d8-1153">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1153">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="f22d8-1154">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22d8-1154">Az.Resources</span></span>
* <span data-ttu-id="f22d8-1155">Добавлен отсутствующий параметр -Mode в командлет Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f22d8-1155">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="f22d8-1156">Исправлена ошибка командлета Get-AzProviderOperation для операций, когда Origin содержит User</span><span class="sxs-lookup"><span data-stu-id="f22d8-1156">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="f22d8-1157">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22d8-1157">Az.Sql</span></span>
* <span data-ttu-id="f22d8-1158">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1158">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f22d8-1159">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f22d8-1159">Az.Websites</span></span>
* <span data-ttu-id="f22d8-1160">Новый командлет Get-AzWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="f22d8-1160">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="f22d8-1161">Новые командлеты New-AzWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows</span><span class="sxs-lookup"><span data-stu-id="f22d8-1161">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="f22d8-1162">0.2.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="f22d8-1162">0.2.0 - September 2018</span></span>
 <span data-ttu-id="f22d8-1163">Первый выпуск</span><span class="sxs-lookup"><span data-stu-id="f22d8-1163">Initial Release</span></span>