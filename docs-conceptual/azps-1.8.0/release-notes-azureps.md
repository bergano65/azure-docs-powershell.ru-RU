---
ms.openlocfilehash: 10d8d50131b3c55ae19c5142c42cb47f37c68c92
ms.sourcegitcommit: 6171bab74aec6785938cad54d584f425ddbb850e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/21/2019
ms.locfileid: "65971909"
---
## <a name="180---april-2019"></a><span data-ttu-id="7fee2-101">1.8.0 — апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7fee2-101">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7fee2-102">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="7fee2-102">Highlights since the last major release</span></span>
* <span data-ttu-id="7fee2-103">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="7fee2-103">General availability of `Az` module</span></span>
* <span data-ttu-id="7fee2-104">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="7fee2-104">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="7fee2-105">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="7fee2-105">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="7fee2-106">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="7fee2-106">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="7fee2-107">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="7fee2-107">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7fee2-108">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="7fee2-108">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="7fee2-109">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="7fee2-109">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7fee2-110">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7fee2-110">Az.Accounts</span></span>
* <span data-ttu-id="7fee2-111">Обновлен командлет Uninstall-AzureRm для правильного удаления модулей в Mac.</span><span class="sxs-lookup"><span data-stu-id="7fee2-111">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="7fee2-112">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7fee2-112">Az.Batch</span></span>
* <span data-ttu-id="7fee2-113">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7fee2-113">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7fee2-114">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7fee2-114">Az.Cdn</span></span>
* <span data-ttu-id="7fee2-115">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7fee2-115">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7fee2-116">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7fee2-116">Az.CognitiveServices</span></span>
* <span data-ttu-id="7fee2-117">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7fee2-117">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7fee2-118">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7fee2-118">Az.Compute</span></span>
* <span data-ttu-id="7fee2-119">Устранена проблема с установкой AEM, если в идентификаторах ресурсов дисков группа ресурсов указана в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="7fee2-119">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="7fee2-120">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7fee2-120">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7fee2-121">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="7fee2-121">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7fee2-122">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7fee2-122">Az.DataFactory</span></span>
* <span data-ttu-id="7fee2-123">Добавлены свойства SsisProperties, если NodeCount не имеет значения NULL для управляемой среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="7fee2-123">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7fee2-124">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7fee2-124">Az.DataLakeStore</span></span>
* <span data-ttu-id="7fee2-125">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7fee2-125">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7fee2-126">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7fee2-126">Az.EventGrid</span></span>
* <span data-ttu-id="7fee2-127">Обновлен текст справки для конечной точки, указывающий, что необходимо создать ресурсы, прежде чем использовать командлеты для создания или обновления подписки на события.</span><span class="sxs-lookup"><span data-stu-id="7fee2-127">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7fee2-128">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7fee2-128">Az.EventHub</span></span>
* <span data-ttu-id="7fee2-129">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="7fee2-129">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="7fee2-130">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7fee2-130">Az.HDInsight</span></span>
* <span data-ttu-id="7fee2-131">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7fee2-131">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7fee2-132">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7fee2-132">Az.IotHub</span></span>
* <span data-ttu-id="7fee2-133">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7fee2-133">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7fee2-134">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7fee2-134">Az.KeyVault</span></span>
* <span data-ttu-id="7fee2-135">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7fee2-135">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7fee2-136">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="7fee2-136">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="7fee2-137">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="7fee2-137">Az.MachineLearning</span></span>
* <span data-ttu-id="7fee2-138">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7fee2-138">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="7fee2-139">Az.Media</span><span class="sxs-lookup"><span data-stu-id="7fee2-139">Az.Media</span></span>
* <span data-ttu-id="7fee2-140">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7fee2-140">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7fee2-141">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7fee2-141">Az.Monitor</span></span>
  * <span data-ttu-id="7fee2-142">Добавлены новые командлеты для правила генерации оповещений на основе метрик GenV2 (не классических).</span><span class="sxs-lookup"><span data-stu-id="7fee2-142">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="7fee2-143">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="7fee2-143">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="7fee2-144">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="7fee2-144">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="7fee2-145">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="7fee2-145">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="7fee2-146">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="7fee2-146">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="7fee2-147">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="7fee2-147">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="7fee2-148">Обновлен пакет SDK Monitor до предварительной версии 0.22.0.</span><span class="sxs-lookup"><span data-stu-id="7fee2-148">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7fee2-149">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7fee2-149">Az.Network</span></span>
* <span data-ttu-id="7fee2-150">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7fee2-150">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7fee2-151">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="7fee2-151">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="7fee2-152">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="7fee2-152">Az.NotificationHubs</span></span>
* <span data-ttu-id="7fee2-153">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7fee2-153">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7fee2-154">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7fee2-154">Az.OperationalInsights</span></span>
* <span data-ttu-id="7fee2-155">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7fee2-155">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="7fee2-156">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="7fee2-156">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="7fee2-157">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7fee2-157">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7fee2-158">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7fee2-158">Az.RecoveryServices</span></span>
* <span data-ttu-id="7fee2-159">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7fee2-159">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7fee2-160">Обновлен табличный формат для SQL на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="7fee2-160">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="7fee2-161">Добавлен альтернативный метод для получения расположения в Общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="7fee2-161">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="7fee2-162">Обновлено значение ScheduleRunDays в объекте SchedulePolicy в соответствии с часовым поясом.</span><span class="sxs-lookup"><span data-stu-id="7fee2-162">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="7fee2-163">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="7fee2-163">Az.RedisCache</span></span>
* <span data-ttu-id="7fee2-164">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7fee2-164">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7fee2-165">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fee2-165">Az.Resources</span></span>
* <span data-ttu-id="7fee2-166">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="7fee2-166">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="7fee2-167">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7fee2-167">Az.Sql</span></span>
* <span data-ttu-id="7fee2-168">Заменена зависимость от пакета SDK монитора на обычный код.</span><span class="sxs-lookup"><span data-stu-id="7fee2-168">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="7fee2-169">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7fee2-169">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7fee2-170">Улучшен процесс классификации нескольких столбцов.</span><span class="sxs-lookup"><span data-stu-id="7fee2-170">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="7fee2-171">Добавлены свойства SKU (имя, семейство, производительность SKU) в отклике Get-AzSqlServerServiceObjective, а также по умолчанию задан табличный формат.</span><span class="sxs-lookup"><span data-stu-id="7fee2-171">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="7fee2-172">C помощью Get-AzSqlServerServiceObjective теперь можно получать список доступных целевых служб по расположению без необходимости заранее размещать сервер в регионе.</span><span class="sxs-lookup"><span data-stu-id="7fee2-172">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="7fee2-173">Поддерживается параметр часового пояса при создании Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7fee2-173">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="7fee2-174">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="7fee2-174">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7fee2-175">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7fee2-175">Az.Websites</span></span>
* <span data-ttu-id="7fee2-176">Исправлены командлеты Set-AzWebApp и Set-AzWebAppSlot, которые теперь не удаляют теги при выполнении.</span><span class="sxs-lookup"><span data-stu-id="7fee2-176">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="7fee2-177">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7fee2-177">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7fee2-178">Обновлен пакет SDK веб-узлов.</span><span class="sxs-lookup"><span data-stu-id="7fee2-178">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="7fee2-179">Удалено свойство AdminSiteName из PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="7fee2-179">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="7fee2-180">1.7.0 —апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7fee2-180">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7fee2-181">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="7fee2-181">Highlights since the last major release</span></span>
* <span data-ttu-id="7fee2-182">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="7fee2-182">General availability of `Az` module</span></span>
* <span data-ttu-id="7fee2-183">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="7fee2-183">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="7fee2-184">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="7fee2-184">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="7fee2-185">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="7fee2-185">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="7fee2-186">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="7fee2-186">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7fee2-187">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="7fee2-187">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="7fee2-188">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="7fee2-188">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7fee2-189">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7fee2-189">Az.Accounts</span></span>
* <span data-ttu-id="7fee2-190">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметр AzureAnalysisServicesEndpointResourceId.</span><span class="sxs-lookup"><span data-stu-id="7fee2-190">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="7fee2-191">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7fee2-191">Az.AnalysisServices</span></span>
* <span data-ttu-id="7fee2-192">Использование ServiceClient в командлетах плоскости данных и удаление исходной логики проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="7fee2-192">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="7fee2-193">Add-AzureASAccount используется как оболочка для Connect-AzAccount во избежание критических изменений.</span><span class="sxs-lookup"><span data-stu-id="7fee2-193">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7fee2-194">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7fee2-194">Az.Automation</span></span>
* <span data-ttu-id="7fee2-195">Исправлена ошибка командлета New-AzAutomationSoftwareUpdateConfiguration, связанная с включением.</span><span class="sxs-lookup"><span data-stu-id="7fee2-195">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="7fee2-196">Теперь параметры IncludedKbNumber и IncludedPackageNameMask должны работать нормально.</span><span class="sxs-lookup"><span data-stu-id="7fee2-196">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="7fee2-197">Исправлена ошибка динамической группы управления обновлениями службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="7fee2-197">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7fee2-198">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7fee2-198">Az.Compute</span></span>
* <span data-ttu-id="7fee2-199">В командлеты New-AzDiskConfig и New-AzSnapshotConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="7fee2-199">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="7fee2-200">Теперь можно создавать виртуальные машину на основе образов из коллекции от других клиентов.</span><span class="sxs-lookup"><span data-stu-id="7fee2-200">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="7fee2-201">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7fee2-201">Az.ContainerInstance</span></span>
* <span data-ttu-id="7fee2-202">Исправлена проблема в параметре -Command командлета New-AzContainerGroup, из-за которой в конце добавлялся пустой аргумент.</span><span class="sxs-lookup"><span data-stu-id="7fee2-202">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7fee2-203">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7fee2-203">Az.DataFactory</span></span>
* <span data-ttu-id="7fee2-204">Пакет SDK для ADF .NET обновлен до версии 3.0.2.</span><span class="sxs-lookup"><span data-stu-id="7fee2-204">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="7fee2-205">Командлет Set-AzDataFactoryV2 обновлен с помощью дополнительных параметров для настроек, связанных с RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7fee2-205">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7fee2-206">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fee2-206">Az.Resources</span></span>
* <span data-ttu-id="7fee2-207">Улучшена обработка поставщиков Get-AzResource при предоставлении параметров -ResourceId или -ResourceGroupName, -Name и -ResourceType.</span><span class="sxs-lookup"><span data-stu-id="7fee2-207">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="7fee2-208">Улучшена обработка ошибок в командлетах Test-AzDeployment и Test-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="7fee2-208">Improve error handling for for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="7fee2-209">Теперь ошибки, возникающие за пределами проверки развертывания, обрабатываются и включаются в выходные данные команды.</span><span class="sxs-lookup"><span data-stu-id="7fee2-209">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="7fee2-210">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="7fee2-210">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="7fee2-211">Добавлен параметр-переключатель -IgnoreDynamicParameters, с помощью которого можно настроить командлеты развертывания так, чтобы они пропускали запросы в сценариях скриптов и заданий.</span><span class="sxs-lookup"><span data-stu-id="7fee2-211">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="7fee2-212">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="7fee2-212">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="7fee2-213">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7fee2-213">Az.Sql</span></span>
* <span data-ttu-id="7fee2-214">Поддержка классификации данных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="7fee2-214">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7fee2-215">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7fee2-215">Az.Storage</span></span>
* <span data-ttu-id="7fee2-216">Подробные сообщения об ошибке передаются при создании контекста хранилища с помощью параметра -UseConnectedAccount, но без входа в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="7fee2-216">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="7fee2-217">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="7fee2-217">New-AzStorageContext</span></span>
* <span data-ttu-id="7fee2-218">Поддержка свойств службы управления BLOB-объектов в указанной учетной записи хранения с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="7fee2-218">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="7fee2-219">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="7fee2-219">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="7fee2-220">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="7fee2-220">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="7fee2-221">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7fee2-221">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="7fee2-222">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7fee2-222">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="7fee2-223">Поддержка параметра -AsJob в командлетах для отправки и скачивания больших двоичных объектов и файлов.</span><span class="sxs-lookup"><span data-stu-id="7fee2-223">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="7fee2-224">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7fee2-224">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="7fee2-225">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7fee2-225">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="7fee2-226">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7fee2-226">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="7fee2-227">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7fee2-227">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="7fee2-228">1.6.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7fee2-228">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7fee2-229">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="7fee2-229">Highlights since the last major release</span></span>
* <span data-ttu-id="7fee2-230">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="7fee2-230">General availability of `Az` module</span></span>
* <span data-ttu-id="7fee2-231">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="7fee2-231">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="7fee2-232">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="7fee2-232">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="7fee2-233">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="7fee2-233">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="7fee2-234">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="7fee2-234">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7fee2-235">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="7fee2-235">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="7fee2-236">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="7fee2-236">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7fee2-237">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7fee2-237">Az.Automation</span></span>
* <span data-ttu-id="7fee2-238">В управление обновлениями службы автоматизации Azure внесены изменения для поддержки следующих новых функций:</span><span class="sxs-lookup"><span data-stu-id="7fee2-238">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="7fee2-239">динамическое группирование;</span><span class="sxs-lookup"><span data-stu-id="7fee2-239">Dynamic grouping</span></span>
    * <span data-ttu-id="7fee2-240">скрипты предварительного или последующего выполнения;</span><span class="sxs-lookup"><span data-stu-id="7fee2-240">Pre-Post script</span></span>
    * <span data-ttu-id="7fee2-241">параметр перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="7fee2-241">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7fee2-242">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7fee2-242">Az.Compute</span></span>
* <span data-ttu-id="7fee2-243">Устранена проблема, связанная с разрешением пути в Get-AzVmBootDiagnosticsData.</span><span class="sxs-lookup"><span data-stu-id="7fee2-243">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="7fee2-244">Обновление клиентской библиотеки вычислений до версии 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="7fee2-244">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7fee2-245">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7fee2-245">Az.KeyVault</span></span>
* <span data-ttu-id="7fee2-246">Добавлена поддержка подстановочных знаков в командлетах KeyVault.</span><span class="sxs-lookup"><span data-stu-id="7fee2-246">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7fee2-247">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7fee2-247">Az.Network</span></span>
* <span data-ttu-id="7fee2-248">Добавлена поддержка анализа угроз для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="7fee2-248">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="7fee2-249">Добавлены настраиваемые правила и ресурс верхнего уровня для политики брандмауэра Шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="7fee2-249">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7fee2-250">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7fee2-250">Az.RecoveryServices</span></span>
* <span data-ttu-id="7fee2-251">В политику виртуальной машины Azure добавлен объект SnapshotRetentionInDays для поддержки мгновенного восстановления.</span><span class="sxs-lookup"><span data-stu-id="7fee2-251">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="7fee2-252">Добавлена поддержка канала для отмены регистрации контейнера.</span><span class="sxs-lookup"><span data-stu-id="7fee2-252">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="7fee2-253">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fee2-253">Az.Resources</span></span>
* <span data-ttu-id="7fee2-254">Обновлена поддержка подстановочных знаков для Get-AzResource и Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7fee2-254">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="7fee2-255">Обновлены учетные данные, используемые при общих вызовах к ARM.</span><span class="sxs-lookup"><span data-stu-id="7fee2-255">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="7fee2-256">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7fee2-256">Az.Sql</span></span>
* <span data-ttu-id="7fee2-257">Изменен тип параметра (ExcludeDetectionType) командлетов для обнаружения угроз с DetectionTypes на string[] для поддержки актуального состояния при добавлении новых типов обнаружения и для поддержки автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="7fee2-257">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7fee2-258">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7fee2-258">Az.Storage</span></span>
* <span data-ttu-id="7fee2-259">Поддержка получения, настройки и удаления политики управления в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="7fee2-259">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="7fee2-260">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7fee2-260">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="7fee2-261">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7fee2-261">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="7fee2-262">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7fee2-262">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="7fee2-263">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="7fee2-263">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="7fee2-264">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="7fee2-264">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="7fee2-265">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="7fee2-265">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7fee2-266">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7fee2-266">Az.Websites</span></span>
* <span data-ttu-id="7fee2-267">Исправлена ошибка с шаблоном ARM, из-за которой прерывалось клонирование все слотов при использовании New-AzWebApp -IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="7fee2-267">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="7fee2-268">1.5.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7fee2-268">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7fee2-269">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7fee2-269">Az.Accounts</span></span>
* <span data-ttu-id="7fee2-270">Добавлена команда Register-AzModule для поддержки созданных командлетов AutoRest.</span><span class="sxs-lookup"><span data-stu-id="7fee2-270">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="7fee2-271">Обновлены примеры для Connect AzAccount.</span><span class="sxs-lookup"><span data-stu-id="7fee2-271">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7fee2-272">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7fee2-272">Az.Automation</span></span>
* <span data-ttu-id="7fee2-273">Исправлена проблема с получением некоторых ежемесячных расписаний в нескольких командлетах службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="7fee2-273">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="7fee2-274">Исправлен командлет Get-AzAutomationDscNode, возвращающий только первые 20 узлов.</span><span class="sxs-lookup"><span data-stu-id="7fee2-274">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="7fee2-275">Теперь он возвращает все узлы.</span><span class="sxs-lookup"><span data-stu-id="7fee2-275">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7fee2-276">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7fee2-276">Az.Cdn</span></span>
* <span data-ttu-id="7fee2-277">Добавлены новые командлеты PowerShell для включения и отключения HTTPS для личного домена и отключены устаревшие командлеты.</span><span class="sxs-lookup"><span data-stu-id="7fee2-277">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7fee2-278">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7fee2-278">Az.Compute</span></span>
* <span data-ttu-id="7fee2-279">Добавлена поддержка подстановочных знаков в командлетах Get.</span><span class="sxs-lookup"><span data-stu-id="7fee2-279">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7fee2-280">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7fee2-280">Az.DataFactory</span></span>
* <span data-ttu-id="7fee2-281">Обновлен пакет SDK для ADF .NET до версии 3.0.1.</span><span class="sxs-lookup"><span data-stu-id="7fee2-281">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7fee2-282">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7fee2-282">Az.LogicApp</span></span>
* <span data-ttu-id="7fee2-283">Исправлена проблема с получением только первой страницы результатов при выполнении команды ListWorkflows.</span><span class="sxs-lookup"><span data-stu-id="7fee2-283">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7fee2-284">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7fee2-284">Az.Network</span></span>
* <span data-ttu-id="7fee2-285">Добавлена поддержка подстановочных знаков в командлетах Network.</span><span class="sxs-lookup"><span data-stu-id="7fee2-285">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7fee2-286">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7fee2-286">Az.RecoveryServices</span></span>
* <span data-ttu-id="7fee2-287">Добавлена поддержка SQL Server на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="7fee2-287">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="7fee2-288">Обновление пакета SDK</span><span class="sxs-lookup"><span data-stu-id="7fee2-288">SDK Update</span></span>
* <span data-ttu-id="7fee2-289">Удалена проверка VMappContainer в Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="7fee2-289">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="7fee2-290">Добавлены параметры Name и ServerName для Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="7fee2-290">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="7fee2-291">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fee2-291">Az.Resources</span></span>
* <span data-ttu-id="7fee2-292">Добавлен параметр `-TemplateObject` в командлеты для развертывания.</span><span class="sxs-lookup"><span data-stu-id="7fee2-292">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="7fee2-293">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2933.</span><span class="sxs-lookup"><span data-stu-id="7fee2-293">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="7fee2-294">Устранена проблема с передачей в конвейер результата `Get-AzResource` для `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="7fee2-294">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="7fee2-295">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8240.</span><span class="sxs-lookup"><span data-stu-id="7fee2-295">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="7fee2-296">Устранена проблема с изменением типа данных JSON при выполнении `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="7fee2-296">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="7fee2-297">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7930.</span><span class="sxs-lookup"><span data-stu-id="7fee2-297">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="7fee2-298">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7fee2-298">Az.Sql</span></span>
* <span data-ttu-id="7fee2-299">Обновление AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="7fee2-299">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="7fee2-300">Исправлено поведение для пограничного случая при создании параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="7fee2-300">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7fee2-301">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7fee2-301">Az.Storage</span></span>
* <span data-ttu-id="7fee2-302">Включена поддержка Kind BlockBlobStorage при создании учетной записи хранения для New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="7fee2-302">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="7fee2-303">1.4.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7fee2-303">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="7fee2-304">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7fee2-304">Az.AnalysisServices</span></span>
* <span data-ttu-id="7fee2-305">Командлет AddAzureASAccount устарел.</span><span class="sxs-lookup"><span data-stu-id="7fee2-305">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7fee2-306">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7fee2-306">Az.Automation</span></span>
* <span data-ttu-id="7fee2-307">Обновлена справка для командлета Import-AzAutomationDscNodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7fee2-307">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="7fee2-308">Добавлена проверка имени конфигурации для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7fee2-308">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="7fee2-309">Улучшена обработка ошибок для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7fee2-309">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7fee2-310">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7fee2-310">Az.CognitiveServices</span></span>
* <span data-ttu-id="7fee2-311">Добавлен параметр CustomSubdomainName — новый необязательный параметр для командлета New-AzCognitiveServicesAccount, который указывает поддомен для ресурса.</span><span class="sxs-lookup"><span data-stu-id="7fee2-311">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7fee2-312">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7fee2-312">Az.Compute</span></span>
* <span data-ttu-id="7fee2-313">Устранена проблема с идентификаторами наборов параметров.</span><span class="sxs-lookup"><span data-stu-id="7fee2-313">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="7fee2-314">Обновлен командлет Get-AzVMExtension для отображения списка всех установленных расширений, если не указан параметр Name.</span><span class="sxs-lookup"><span data-stu-id="7fee2-314">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="7fee2-315">Для командлета Update-AzImage добавлены параметры Tag и ResourceId.</span><span class="sxs-lookup"><span data-stu-id="7fee2-315">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="7fee2-316">Командлет Get-AzVmssVM, который выполняется без указания идентификатора экземпляра и с параметром InstanceView, может выводить виртуальные машины из VMSS с представлением экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7fee2-316">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7fee2-317">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7fee2-317">Az.DataLakeStore</span></span>
* <span data-ttu-id="7fee2-318">Добавлены командлеты для перечисления и восстановления удаленного элемента ADL.</span><span class="sxs-lookup"><span data-stu-id="7fee2-318">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7fee2-319">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7fee2-319">Az.EventHub</span></span>
* <span data-ttu-id="7fee2-320">Добавлено новое логическое свойство SkipEmptyArchives для пропуска пустых архивов в классе CaptureDescription Eventhub.</span><span class="sxs-lookup"><span data-stu-id="7fee2-320">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="7fee2-321">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7fee2-321">Az.KeyVault</span></span>
* <span data-ttu-id="7fee2-322">Исправлена расстановка тегов для командлета Set-AzKeyVaultSecret.</span><span class="sxs-lookup"><span data-stu-id="7fee2-322">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7fee2-323">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7fee2-323">Az.LogicApp</span></span>
* <span data-ttu-id="7fee2-324">Добавлен SKU "Базовый" для учетных записей интеграции.</span><span class="sxs-lookup"><span data-stu-id="7fee2-324">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="7fee2-325">Добавлены типы сопоставлений Liquid, а также XSLT 2.0 и XSLT 3.0.</span><span class="sxs-lookup"><span data-stu-id="7fee2-325">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="7fee2-326">Новые командлеты для сборок учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="7fee2-326">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="7fee2-327">Get-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="7fee2-327">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="7fee2-328">New-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="7fee2-328">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="7fee2-329">Remove-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="7fee2-329">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="7fee2-330">Set-AzIntegrationAccountAssembly.</span><span class="sxs-lookup"><span data-stu-id="7fee2-330">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="7fee2-331">Новые командлеты для конфигурации пакета учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="7fee2-331">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="7fee2-332">Get-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="7fee2-332">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="7fee2-333">New-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="7fee2-333">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="7fee2-334">Remove-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="7fee2-334">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="7fee2-335">Set-AzIntegrationAccountBatchConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7fee2-335">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="7fee2-336">Обновлен пакет SDK Logic Apps до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="7fee2-336">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7fee2-337">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7fee2-337">Az.Monitor</span></span>
* <span data-ttu-id="7fee2-338">Обновлена справка для командлета Get-AzMetric.</span><span class="sxs-lookup"><span data-stu-id="7fee2-338">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7fee2-339">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7fee2-339">Az.Network</span></span>
* <span data-ttu-id="7fee2-340">Обновлен пример справки для командлета Add-AzApplicationGatewayCustomError.</span><span class="sxs-lookup"><span data-stu-id="7fee2-340">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7fee2-341">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7fee2-341">Az.OperationalInsights</span></span>
* <span data-ttu-id="7fee2-342">Дополнительная поддержка создания и получения источников данных ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="7fee2-342">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="7fee2-343">Добавлен новый тип ApplicationInsights для получения определенных или всех источников данных ApplicationInsights для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="7fee2-343">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="7fee2-344">Добавлен командлет New-AzOperationalInsightsApplicationInsightsDataSource для создания источника данных с использованием параметров указанного ресурса Application-Insightss: subscription Id, resourceGroupName и name.</span><span class="sxs-lookup"><span data-stu-id="7fee2-344">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="7fee2-345">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fee2-345">Az.Resources</span></span>
* <span data-ttu-id="7fee2-346">исправлена проблема https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="7fee2-346">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="7fee2-347">исправлена проблема https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="7fee2-347">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="7fee2-348">исправлена проблема https://github.com/Azure/azure-powershell/issues/6219.</span><span class="sxs-lookup"><span data-stu-id="7fee2-348">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="7fee2-349">Исправлена ошибка, препятствующая повторному созданию KeyCredentials.</span><span class="sxs-lookup"><span data-stu-id="7fee2-349">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="7fee2-350">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7fee2-350">Az.Sql</span></span>
* <span data-ttu-id="7fee2-351">Добавлена поддержка уровня гипермасштабирования в базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="7fee2-351">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="7fee2-352">Исправлена ошибка, из-за которой восстановление могло завершиться со сбоем при указании ненужных свойств в запросе на восстановление.</span><span class="sxs-lookup"><span data-stu-id="7fee2-352">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7fee2-353">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7fee2-353">Az.Websites</span></span>
* <span data-ttu-id="7fee2-354">Исправлен пример для командлета Get-AzWebAppSlotMetrics.</span><span class="sxs-lookup"><span data-stu-id="7fee2-354">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="7fee2-355">1.3.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7fee2-355">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7fee2-356">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7fee2-356">Az.Accounts</span></span>
* <span data-ttu-id="7fee2-357">Обновление до последней версии ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="7fee2-357">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="7fee2-358">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7fee2-358">Az.AnalysisServices</span></span>
<span data-ttu-id="7fee2-359">Общедоступная версия модуля Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="7fee2-359">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7fee2-360">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7fee2-360">Az.Compute</span></span>
* <span data-ttu-id="7fee2-361">Расширение AEM: добавлена поддержка дисков UltraSSD, P60, P70 и P80.</span><span class="sxs-lookup"><span data-stu-id="7fee2-361">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="7fee2-362">Обновлено описание справки для командлета Set-AzVMBootDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="7fee2-362">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="7fee2-363">Обновлено описание справки и пример для командлета Update-AzImage.</span><span class="sxs-lookup"><span data-stu-id="7fee2-363">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7fee2-364">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7fee2-364">Az.RecoveryServices</span></span>
<span data-ttu-id="7fee2-365">Общедоступная версия модуля Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="7fee2-365">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7fee2-366">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fee2-366">Az.Resources</span></span>
* <span data-ttu-id="7fee2-367">Исправлена расстановка тегов для групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7fee2-367">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="7fee2-368">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="7fee2-368">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="7fee2-369">Исправлена проблема с игнорированием командлетом `Get-AzureRmRoleAssignment` параметра -ErrorAction.</span><span class="sxs-lookup"><span data-stu-id="7fee2-369">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="7fee2-370">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="7fee2-370">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="7fee2-371">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7fee2-371">Az.Sql</span></span>
* <span data-ttu-id="7fee2-372">Добавлен командлет Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="7fee2-372">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="7fee2-373">Исправлена проблема с появлением исключения NullRef при выполнении командлетов SQL, если не выполнен вход в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="7fee2-373">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="7fee2-374">Исправлено исключение NullRef в командлете Get-AzSqlCapability.</span><span class="sxs-lookup"><span data-stu-id="7fee2-374">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="7fee2-375">1.2.1 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7fee2-375">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7fee2-376">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7fee2-376">Az.Accounts</span></span>
* <span data-ttu-id="7fee2-377">Выпуск с правильной версией службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="7fee2-377">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="7fee2-378">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7fee2-378">Az.AnalysisServices</span></span>
* <span data-ttu-id="7fee2-379">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="7fee2-379">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7fee2-380">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7fee2-380">Az.RecoveryServices</span></span>
* <span data-ttu-id="7fee2-381">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="7fee2-381">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="7fee2-382">1.2.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7fee2-382">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7fee2-383">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7fee2-383">Az.Accounts</span></span>
* <span data-ttu-id="7fee2-384">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="7fee2-384">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7fee2-385">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="7fee2-385">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7fee2-386">Добавлено предупреждающее сообщение в PS Core для модуля Uninstall-AzureRm.</span><span class="sxs-lookup"><span data-stu-id="7fee2-386">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="7fee2-387">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="7fee2-387">Az.Aks</span></span>
* <span data-ttu-id="7fee2-388">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="7fee2-388">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7fee2-389">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7fee2-389">Az.Automation</span></span>
* <span data-ttu-id="7fee2-390">Добавлена поддержка для модулей runbook Python 2.</span><span class="sxs-lookup"><span data-stu-id="7fee2-390">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="7fee2-391">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="7fee2-391">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7fee2-392">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7fee2-392">Az.Cdn</span></span>
* <span data-ttu-id="7fee2-393">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="7fee2-393">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7fee2-394">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7fee2-394">Az.Compute</span></span>
* <span data-ttu-id="7fee2-395">Добавлен командлет Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="7fee2-395">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="7fee2-396">Добавлен параметр TempDisk к командлету Set-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="7fee2-396">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="7fee2-397">Исправлено предупреждающее сообщение командлета New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="7fee2-397">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="7fee2-398">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7fee2-398">Az.ContainerRegistry</span></span>
* <span data-ttu-id="7fee2-399">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="7fee2-399">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7fee2-400">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7fee2-400">Az.DataFactory</span></span>
* <span data-ttu-id="7fee2-401">Пакет SDK ADF .Net обновлен до версии 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="7fee2-401">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7fee2-402">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7fee2-402">Az.DataLakeStore</span></span>
* <span data-ttu-id="7fee2-403">Исправлена проблема с конечной точкой ADLS при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="7fee2-403">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="7fee2-404">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7462.</span><span class="sxs-lookup"><span data-stu-id="7fee2-404">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="7fee2-405">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="7fee2-405">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7fee2-406">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7fee2-406">Az.IotHub</span></span>
* <span data-ttu-id="7fee2-407">Добавлен формат кодирования для командлета Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="7fee2-407">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7fee2-408">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7fee2-408">Az.KeyVault</span></span>
* <span data-ttu-id="7fee2-409">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="7fee2-409">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7fee2-410">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7fee2-410">Az.Network</span></span>
* <span data-ttu-id="7fee2-411">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="7fee2-411">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="7fee2-412">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fee2-412">Az.Resources</span></span>
* <span data-ttu-id="7fee2-413">Исправлены неправильные примеры в справочной документации по командлетам New-AzADAppCredential и New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="7fee2-413">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="7fee2-414">Исправлена проблема, при которой путь для параметра -TemplateFile не удавалось разрешить до выполнения командлетов развертывания групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7fee2-414">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="7fee2-415">Az.Resources: исправлена документация для значения по умолчанию -Mode командлета New-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="7fee2-415">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="7fee2-416">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/7522.</span><span class="sxs-lookup"><span data-stu-id="7fee2-416">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="7fee2-417">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/5747.</span><span class="sxs-lookup"><span data-stu-id="7fee2-417">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="7fee2-418">Исправлена проблема с форматированием объекта PSResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="7fee2-418">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="7fee2-419">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2123.</span><span class="sxs-lookup"><span data-stu-id="7fee2-419">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7fee2-420">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7fee2-420">Az.ServiceFabric</span></span>
* <span data-ttu-id="7fee2-421">Исправлена проблема с появлением исключения в процессе отката при добавлении сертификата к модели VMSS: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="7fee2-421">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="7fee2-422">Исправлены некоторые сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="7fee2-422">Fix some error messages.</span></span>
* <span data-ttu-id="7fee2-423">Исправлена проблема с созданием кластера с шаблоном ARM по умолчанию для командлета New-AzServiceFabriCluster, который не работал с операцией миграции в Az.</span><span class="sxs-lookup"><span data-stu-id="7fee2-423">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="7fee2-424">Исправлена проблема с добавлением сертификата кластера или приложения: теперь они добавляются только в Масштабируемые наборы виртуальных машин, которые сопоставлены с кластером, путем проверки идентификатора кластера в расширении.</span><span class="sxs-lookup"><span data-stu-id="7fee2-424">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="7fee2-425">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="7fee2-425">Az.SignalR</span></span>
* <span data-ttu-id="7fee2-426">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="7fee2-426">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="7fee2-427">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7fee2-427">Az.Sql</span></span>
* <span data-ttu-id="7fee2-428">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="7fee2-428">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7fee2-429">Обновлено описание параметра LicenseType с добавлением возможных значений.</span><span class="sxs-lookup"><span data-stu-id="7fee2-429">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="7fee2-430">Исправлена проблема с неправильным обновлением удостоверения управляемого экземпляра, если оно было единственным обновляемым свойством.</span><span class="sxs-lookup"><span data-stu-id="7fee2-430">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="7fee2-431">Поддержка пользовательских параметров сортировки в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="7fee2-431">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7fee2-432">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7fee2-432">Az.Storage</span></span>
* <span data-ttu-id="7fee2-433">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="7fee2-433">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7fee2-434">Добавлен вывод подробных сообщений об ошибке при получении или установке классических свойств ведения журнала или метрик в учетной записи хранилища класса Premium, так как учетная запись хранилища класса Premium не поддерживает классические функции ведения журнала и метрик.</span><span class="sxs-lookup"><span data-stu-id="7fee2-434">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="7fee2-435">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="7fee2-435">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="7fee2-436">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="7fee2-436">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="7fee2-437">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="7fee2-437">Az.TrafficManager</span></span>
* <span data-ttu-id="7fee2-438">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="7fee2-438">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7fee2-439">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7fee2-439">Az.Websites</span></span>
* <span data-ttu-id="7fee2-440">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="7fee2-440">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7fee2-441">Исправлена работа командлета New-AzWebAppSSLBinding: сертификат отправляется в правильную группу ресурсов и правильное расположение, если приложение размещено в ASE.</span><span class="sxs-lookup"><span data-stu-id="7fee2-441">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="7fee2-442">Исправлена работа командлета New-AzWebAppSSLBinding: теги не перезаписываются при привязке SSL-сертификата к приложению.</span><span class="sxs-lookup"><span data-stu-id="7fee2-442">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="7fee2-443">1.1.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7fee2-443">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7fee2-444">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7fee2-444">Az.Accounts</span></span>
* <span data-ttu-id="7fee2-445">Добавление области "Local" в Enable-AzureRmAlias.</span><span class="sxs-lookup"><span data-stu-id="7fee2-445">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7fee2-446">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7fee2-446">Az.Compute</span></span>
* <span data-ttu-id="7fee2-447">Теперь имя не является обязательным в идентификаторе набора параметров для Restart/Start/Stop/Remove/Set-AzVM и Save-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="7fee2-447">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="7fee2-448">Обновлено описание идентификатора в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="7fee2-448">Updated the description of ID in help files</span></span>
* <span data-ttu-id="7fee2-449">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="7fee2-449">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7fee2-450">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7fee2-450">Az.DataLakeStore</span></span>
* <span data-ttu-id="7fee2-451">Обновление версии пакета SDK для плоскости данных до 1.1.14 для устранения найденных проблем.</span><span class="sxs-lookup"><span data-stu-id="7fee2-451">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="7fee2-452">Исправлена обработка отрицательного времени доступа и времени изменения для getfilestatus и liststatus, исправлен токен отмены для асинхронных методов.</span><span class="sxs-lookup"><span data-stu-id="7fee2-452">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7fee2-453">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7fee2-453">Az.EventGrid</span></span>
* <span data-ttu-id="7fee2-454">Обновление для использования API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="7fee2-454">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="7fee2-455">Обновлены указанные ниже командлеты для поддержки нового сценария в API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="7fee2-455">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="7fee2-456">New-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="7fee2-456">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="7fee2-457">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="7fee2-457">Event Time-To-Live,</span></span>
        - <span data-ttu-id="7fee2-458">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="7fee2-458">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="7fee2-459">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="7fee2-459">Dead letter endpoint.</span></span>
    - <span data-ttu-id="7fee2-460">Update-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="7fee2-460">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="7fee2-461">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="7fee2-461">Event Time-To-Live,</span></span>
        - <span data-ttu-id="7fee2-462">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="7fee2-462">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="7fee2-463">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="7fee2-463">Dead letter endpoint.</span></span>
* <span data-ttu-id="7fee2-464">Для параметра EndpointType добавлены новые значения перечисления (storageQueue и hybridConnection) в командлеты New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="7fee2-464">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="7fee2-465">Если ожидается, что создание или обновление подписки на событие повлечет за собой действия со стороны пользователя, выполняемые вручную, отображается предупреждение при создании или обновлении подписки события.</span><span class="sxs-lookup"><span data-stu-id="7fee2-465">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7fee2-466">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7fee2-466">Az.IotHub</span></span>
* <span data-ttu-id="7fee2-467">Пакет SDK Центра Интернета вещей обновлен до последней версии.</span><span class="sxs-lookup"><span data-stu-id="7fee2-467">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7fee2-468">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7fee2-468">Az.LogicApp</span></span>
* <span data-ttu-id="7fee2-469">Get-AzLogicApp позволяет перечислить все параметры без указанного имени.</span><span class="sxs-lookup"><span data-stu-id="7fee2-469">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="7fee2-470">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fee2-470">Az.Resources</span></span>
* <span data-ttu-id="7fee2-471">Исправлена проблема с набором параметров при предоставлении параметров "-ODataQuery" и "-ResourceId" для "Get-AzResource".</span><span class="sxs-lookup"><span data-stu-id="7fee2-471">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="7fee2-472">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7875.</span><span class="sxs-lookup"><span data-stu-id="7fee2-472">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="7fee2-473">Исправлена обработка параметра -Custom в New/Set-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="7fee2-473">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="7fee2-474">Исправлена опечатка в документации по New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="7fee2-474">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="7fee2-475">Параметр "-MailNickname" стал обязательным для "New-AzADUser".</span><span class="sxs-lookup"><span data-stu-id="7fee2-475">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="7fee2-476">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8220.</span><span class="sxs-lookup"><span data-stu-id="7fee2-476">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="7fee2-477">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="7fee2-477">Az.SignalR</span></span>
* <span data-ttu-id="7fee2-478">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="7fee2-478">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="7fee2-479">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7fee2-479">Az.Sql</span></span>
* <span data-ttu-id="7fee2-480">Зависимость клиента управления хранением преобразована для общей реализации в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="7fee2-480">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7fee2-481">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7fee2-481">Az.Storage</span></span>
* <span data-ttu-id="7fee2-482">Установка параметра StorageAccountName для контекста хранилища в качестве реального имени учетной записи хранения, если она была создана с использованием токена Sas, OAuth или анонимного доступа.</span><span class="sxs-lookup"><span data-stu-id="7fee2-482">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="7fee2-483">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="7fee2-483">New-AzStorageContext</span></span>
* <span data-ttu-id="7fee2-484">Создание токена Sas большого двоичного объекта моментального снимка с параметром "-FullUri". Возвращаемый URI исправлен на URI моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="7fee2-484">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="7fee2-485">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="7fee2-485">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7fee2-486">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7fee2-486">Az.Websites</span></span>
* <span data-ttu-id="7fee2-487">Исправлена ошибка синтаксического анализа даты в "Get-AzDeletedWebApp".</span><span class="sxs-lookup"><span data-stu-id="7fee2-487">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="7fee2-488">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="7fee2-488">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="7fee2-489">1.0.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="7fee2-489">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="7fee2-490">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="7fee2-490">General</span></span>

- <span data-ttu-id="7fee2-491">Общедоступная версия модуля Az.</span><span class="sxs-lookup"><span data-stu-id="7fee2-491">General Availability of Az Module</span></span>
- <span data-ttu-id="7fee2-492">Справка в Интернете для каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="7fee2-492">Online help for each module</span></span>
- <span data-ttu-id="7fee2-493">Дополнительные сведения и стратегию развития см. в статье [Announcing New Module 'Az'](https://aka.ms/azps-announce) (Объявление о новом модуле Az)</span><span class="sxs-lookup"><span data-stu-id="7fee2-493">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="7fee2-494">Сведения о миграции с AzureRM см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="7fee2-494">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="7fee2-495">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7fee2-495">Az.Accounts</span></span>
- <span data-ttu-id="7fee2-496">Изменено с Az.Profile.</span><span class="sxs-lookup"><span data-stu-id="7fee2-496">Changed from Az.Profile</span></span>
- <span data-ttu-id="7fee2-497">Исправлены форматы таблиц для типов профиля и контекста.</span><span class="sxs-lookup"><span data-stu-id="7fee2-497">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="7fee2-498">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7fee2-498">Az.ApiManagement</span></span>
- <span data-ttu-id="7fee2-499">Исправления для #7002.</span><span class="sxs-lookup"><span data-stu-id="7fee2-499">Fixes for #7002</span></span>
- <span data-ttu-id="7fee2-500">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="7fee2-500">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="7fee2-501">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7fee2-501">Az.Batch</span></span>
- <span data-ttu-id="7fee2-502">Добавлена возможность видеть, какая версия агента узла пакетной службы Azure работает в пуле на каждой виртуальной машине, с помощью нового свойства `NodeAgentInformation` в `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="7fee2-502">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="7fee2-503">Значение `Caching` по умолчанию для `PSDataDisk` теперь `ReadWrite` вместо `None`.</span><span class="sxs-lookup"><span data-stu-id="7fee2-503">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="7fee2-504">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="7fee2-504">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="7fee2-505">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="7fee2-505">Az.Billing</span></span>
- <span data-ttu-id="7fee2-506">Объединены командлеты Billing, Consumption и UsageAggregates. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0).</span><span class="sxs-lookup"><span data-stu-id="7fee2-506">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="7fee2-507">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="7fee2-507">Az.CognitivServices</span></span>
- <span data-ttu-id="7fee2-508">Добавлены средства заполнения для SkuName и Typem, доступные в операции New-AzureRmCognitiveServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="7fee2-508">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="7fee2-509">Удален набор параметров GetSkusWithAccountParamSetName из Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="7fee2-509">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="7fee2-510">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7fee2-510">Az.ContainerInstance</span></span>
- <span data-ttu-id="7fee2-511">Добавлена поддержка ManagedIdentity.</span><span class="sxs-lookup"><span data-stu-id="7fee2-511">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="7fee2-512">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="7fee2-512">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="7fee2-513">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="7fee2-513">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="7fee2-514">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7fee2-514">Az.DataLakeStore</span></span>
- <span data-ttu-id="7fee2-515">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="7fee2-515">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="7fee2-516">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7fee2-516">Az.Monitor</span></span>
- <span data-ttu-id="7fee2-517">"Az.Insights" переименован в "Az.Monitor" и внесены другие незначительные критические изменения. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="7fee2-517">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="7fee2-518">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7fee2-518">Az.KeyVault</span></span>
- <span data-ttu-id="7fee2-519">Из типов вывода удалено устаревшее свойство PurgeDisabled</span><span class="sxs-lookup"><span data-stu-id="7fee2-519">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="7fee2-520">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="7fee2-520">Az.MachineLearning</span></span>
- <span data-ttu-id="7fee2-521">Включены командлеты из модуля Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="7fee2-521">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="7fee2-522">Az.Media</span><span class="sxs-lookup"><span data-stu-id="7fee2-522">Az.Media</span></span>
- <span data-ttu-id="7fee2-523">Удаляет устаревший псевдоним Tags из New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="7fee2-523">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="7fee2-524">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7fee2-524">Az.Network</span></span>
<span data-ttu-id="7fee2-525">В шлюз приложений добавлена поддержка настройки RewriteRuleSets</span><span class="sxs-lookup"><span data-stu-id="7fee2-525">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="7fee2-526">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="7fee2-526">New cmdlets added:</span></span>
        - <span data-ttu-id="7fee2-527">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7fee2-527">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7fee2-528">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7fee2-528">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7fee2-529">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7fee2-529">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7fee2-530">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7fee2-530">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7fee2-531">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7fee2-531">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7fee2-532">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="7fee2-532">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="7fee2-533">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="7fee2-533">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="7fee2-534">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="7fee2-534">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="7fee2-535">В следующие командлеты добавлен необязательный параметр -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7fee2-535">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="7fee2-536">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7fee2-536">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="7fee2-537">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7fee2-537">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="7fee2-538">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7fee2-538">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="7fee2-539">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7fee2-539">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="7fee2-540">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7fee2-540">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="7fee2-541">New-AzureRmApplicationGatewayUrlPathMapConfig добавил с помощью идентификатора поддержку KeyVault для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="7fee2-541">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="7fee2-542">В следующие командлеты добавлен необязательный параметр -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7fee2-542">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="7fee2-543">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7fee2-543">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="7fee2-544">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7fee2-544">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="7fee2-545">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7fee2-545">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="7fee2-546">В командлет New-AzApplicationGateway добавлен необязательный параметр -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="7fee2-546">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="7fee2-547">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="7fee2-547">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="7fee2-548">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7fee2-548">Az.OperationalInsights</span></span>
- <span data-ttu-id="7fee2-549">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="7fee2-549">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="7fee2-550">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7fee2-550">Az.Profile</span></span>
- <span data-ttu-id="7fee2-551">Имя модуля изменено на Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="7fee2-551">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="7fee2-552">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7fee2-552">Az.RecoveryServices</span></span>
- <span data-ttu-id="7fee2-553">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="7fee2-553">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="7fee2-554">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fee2-554">Az.Resources</span></span>
- <span data-ttu-id="7fee2-555">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="7fee2-555">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="7fee2-556">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7fee2-556">Az.ServiceFabric</span></span>
- <span data-ttu-id="7fee2-557">Поддержка спецификации сертификата по общему имени и отпечатку</span><span class="sxs-lookup"><span data-stu-id="7fee2-557">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="7fee2-558">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="7fee2-558">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="7fee2-559">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="7fee2-559">Az.SIgnalR</span></span>
- <span data-ttu-id="7fee2-560">Общедоступная версия командлетов PowerShell для SIgnalR</span><span class="sxs-lookup"><span data-stu-id="7fee2-560">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="7fee2-561">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7fee2-561">Az.Sql</span></span>
- <span data-ttu-id="7fee2-562">Добавлены новые типы обнаружения Data_Exfiltration и Unsafe_Action в командлеты обнаружения угроз</span><span class="sxs-lookup"><span data-stu-id="7fee2-562">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="7fee2-563">Примеры обновленной документации для командлетов аудита Sql</span><span class="sxs-lookup"><span data-stu-id="7fee2-563">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="7fee2-564">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="7fee2-564">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="7fee2-565">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7fee2-565">Az.Storage</span></span>
- <span data-ttu-id="7fee2-566">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="7fee2-566">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="7fee2-567">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7fee2-567">Az.Websites</span></span>
- <span data-ttu-id="7fee2-568">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="7fee2-568">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="7fee2-569">0.7.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="7fee2-569">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="7fee2-570">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="7fee2-570">General</span></span>

* <span data-ttu-id="7fee2-571">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="7fee2-571">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="7fee2-572">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7fee2-572">Az.Compute</span></span>

* <span data-ttu-id="7fee2-573">Добавлена поддержка UltraSSD и образов коллекции в простых наборах параметров для командлетов `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="7fee2-573">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="7fee2-574">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7fee2-574">Az.DataLakeStore</span></span>

* <span data-ttu-id="7fee2-575">Исправлено косую черту в конце домена учетной записи ADLS</span><span class="sxs-lookup"><span data-stu-id="7fee2-575">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="7fee2-576">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7fee2-576">Az.FrontDoor</span></span>

* <span data-ttu-id="7fee2-577">Исправлены некоторые неработающие ссылки</span><span class="sxs-lookup"><span data-stu-id="7fee2-577">Fixed some broken links</span></span>
    - <span data-ttu-id="7fee2-578">В статьях New-AzureRmFrontDoor и Set-AzureRmFrontDoor исправлена ссылка на статью командлета New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="7fee2-578">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="7fee2-579">В статье New-AzureRmFrontDoorManagedRuleObject исправлена ссылка на статью командлета New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="7fee2-579">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="7fee2-580">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7fee2-580">Az.RecoveryServices</span></span>

* <span data-ttu-id="7fee2-581">Добавлены проверки на стороне клиента для операций восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="7fee2-581">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="7fee2-582">StorageAccountName и storageAccountResourceGroupName являются необязательными для восстановления afs.</span><span class="sxs-lookup"><span data-stu-id="7fee2-582">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="7fee2-583">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fee2-583">Az.Resources</span></span>

* <span data-ttu-id="7fee2-584">Исправление для https://github.com/Azure/azure-powershell/issues/7679.</span><span class="sxs-lookup"><span data-stu-id="7fee2-584">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="7fee2-585">Обновите Get-AzureRmRoleAssignment, чтобы использовать область подписки, если она указана при запросе классических администраторов.</span><span class="sxs-lookup"><span data-stu-id="7fee2-585">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="7fee2-586">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7fee2-586">Az.Sql</span></span>

* <span data-ttu-id="7fee2-587">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="7fee2-587">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="7fee2-588">Устранена проблема с использованием Get-AzureRmSqlDatabaseVulnerabilityAssessment с .NET Core.</span><span class="sxs-lookup"><span data-stu-id="7fee2-588">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="7fee2-589">Изменена документация справочных сообщений, связанных с командлетами аудита SQL.</span><span class="sxs-lookup"><span data-stu-id="7fee2-589">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="7fee2-590">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7fee2-590">Az.Storage</span></span>

* <span data-ttu-id="7fee2-591">Добавлено -EnableHierarchicalNamespace к New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7fee2-591">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="7fee2-592">Устранена проблема, из-за которой командлет Copy File не может повторно использовать исходный контекст в пункте назначения, если не введен -DestContext</span><span class="sxs-lookup"><span data-stu-id="7fee2-592">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="7fee2-593">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="7fee2-593">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="7fee2-594">Поддержка статической конфигурации сайта</span><span class="sxs-lookup"><span data-stu-id="7fee2-594">Support Static Website configuration</span></span>
    - <span data-ttu-id="7fee2-595">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="7fee2-595">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="7fee2-596">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="7fee2-596">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="7fee2-597">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7fee2-597">Az.Websites</span></span>

* <span data-ttu-id="7fee2-598">Set-AzureRmWebApp и Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7fee2-598">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="7fee2-599">Добавлен новый параметр (-AzureStoragePath), который указывает путь службы хранилища Azure для подключения в приложениях-контейнерах Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="7fee2-599">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="7fee2-600">Используйте выходные данные нового командлета New-AzureRmWebAppAzureStoragePath в качестве параметра, чтобы задать пути к службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="7fee2-600">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="7fee2-601">0.6.1 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="7fee2-601">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="7fee2-602">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7fee2-602">Az.ApiManagement</span></span>
* <span data-ttu-id="7fee2-603">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="7fee2-603">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="7fee2-604">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7fee2-604">Az.Automation</span></span>
* <span data-ttu-id="7fee2-605">Командлеты службы автоматизации Azure на базе Swagger.</span><span class="sxs-lookup"><span data-stu-id="7fee2-605">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="7fee2-606">Добавлены командлеты для Управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="7fee2-606">Added Update Management cmdlets</span></span>
* <span data-ttu-id="7fee2-607">Добавлены командлеты для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="7fee2-607">Added Source Control cmdlets</span></span>
* <span data-ttu-id="7fee2-608">Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="7fee2-608">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="7fee2-609">Исправлена команда DSC для регистрации узла.</span><span class="sxs-lookup"><span data-stu-id="7fee2-609">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="7fee2-610">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7fee2-610">Az.Compute</span></span>
* <span data-ttu-id="7fee2-611">Исправлена проблема с удостоверением, назначаемым системой.</span><span class="sxs-lookup"><span data-stu-id="7fee2-611">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="7fee2-612">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="7fee2-612">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="7fee2-613">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7fee2-613">Az.ContainerInstance</span></span>
* <span data-ttu-id="7fee2-614">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="7fee2-614">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="7fee2-615">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="7fee2-615">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="7fee2-616">Обновлено описание в примерах командлетов для Marketplace.</span><span class="sxs-lookup"><span data-stu-id="7fee2-616">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="7fee2-617">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7fee2-617">Az.Network</span></span>
* <span data-ttu-id="7fee2-618">Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="7fee2-618">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="7fee2-619">Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="7fee2-619">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="7fee2-620">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="7fee2-620">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="7fee2-621">Исправлены проблемы с использованием памяти в карте виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="7fee2-621">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="7fee2-622">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="7fee2-622">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="7fee2-623">Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="7fee2-623">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="7fee2-624">Параметры часового пояса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="7fee2-624">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="7fee2-625">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="7fee2-625">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="7fee2-626">Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="7fee2-626">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="7fee2-627">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="7fee2-627">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="7fee2-628">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="7fee2-628">Az.Relay</span></span>
* <span data-ttu-id="7fee2-629">Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.</span><span class="sxs-lookup"><span data-stu-id="7fee2-629">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="7fee2-630">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fee2-630">Az.Resources</span></span>
* <span data-ttu-id="7fee2-631">Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.</span><span class="sxs-lookup"><span data-stu-id="7fee2-631">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="7fee2-632">Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.</span><span class="sxs-lookup"><span data-stu-id="7fee2-632">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="7fee2-633">Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.</span><span class="sxs-lookup"><span data-stu-id="7fee2-633">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="7fee2-634">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7fee2-634">Az.ServiceFabric</span></span>
* <span data-ttu-id="7fee2-635">Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.</span><span class="sxs-lookup"><span data-stu-id="7fee2-635">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="7fee2-636">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7fee2-636">Az.Sql</span></span>
* <span data-ttu-id="7fee2-637">Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="7fee2-637">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="7fee2-638">Get-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="7fee2-638">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7fee2-639">New-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="7fee2-639">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7fee2-640">Set-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="7fee2-640">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7fee2-641">Remove-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="7fee2-641">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7fee2-642">Get-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="7fee2-642">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="7fee2-643">New-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="7fee2-643">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="7fee2-644">Restore-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="7fee2-644">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="7fee2-645">Remove-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="7fee2-645">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="7fee2-646">Добавлено расширенное управление политиками аудита для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="7fee2-646">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="7fee2-647">Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="7fee2-647">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="7fee2-648">Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.</span><span class="sxs-lookup"><span data-stu-id="7fee2-648">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="7fee2-649">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="7fee2-649">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="7fee2-650">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="7fee2-650">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="7fee2-651">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="7fee2-651">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="7fee2-652">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="7fee2-652">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="7fee2-653">Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="7fee2-653">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="7fee2-654">0.5.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="7fee2-654">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="7fee2-655">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="7fee2-655">General</span></span>
* <span data-ttu-id="7fee2-656">Добавлены средства заполнения ресурсов для многих основных командлетов — они позволяют вам переключать существующие имена ресурсов при вызове командлетов в интерактивном режиме</span><span class="sxs-lookup"><span data-stu-id="7fee2-656">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="7fee2-657">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7fee2-657">Az.Profile</span></span>
* <span data-ttu-id="7fee2-658">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="7fee2-658">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="7fee2-659">В командлете Connect-AzAccount параметр TenantId переименован в Tenant и добавлен псевдоним для TenantId</span><span class="sxs-lookup"><span data-stu-id="7fee2-659">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="7fee2-660">Обновлено описание TenantId для командлета Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="7fee2-660">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="7fee2-661">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="7fee2-661">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="7fee2-662">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="7fee2-662">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="7fee2-663">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="7fee2-663">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="7fee2-664">Устранена проблема, при которой командлет Disconnect-AzAccount вызывал сбой при отсутствии подключения</span><span class="sxs-lookup"><span data-stu-id="7fee2-664">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="7fee2-665">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7fee2-665">Az.CognitiveServices</span></span>
* <span data-ttu-id="7fee2-666">Добавлена операция Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="7fee2-666">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7fee2-667">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7fee2-667">Az.Compute</span></span>
* <span data-ttu-id="7fee2-668">Добавлены командлеты Add-AzVmssVMDataDisk и Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="7fee2-668">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="7fee2-669">Get-AzVMImage отображает AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="7fee2-669">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="7fee2-670">Устранена проблема, при которой значения параметров SetAzVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="7fee2-670">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7fee2-671">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7fee2-671">Az.DataLakeStore</span></span>
* <span data-ttu-id="7fee2-672">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="7fee2-672">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="7fee2-673">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="7fee2-673">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="7fee2-674">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="7fee2-674">Az.Insights</span></span>
* <span data-ttu-id="7fee2-675">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="7fee2-675">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="7fee2-676">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="7fee2-676">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="7fee2-677">Исправлена проблема № 7513 [Insights], при которой для командлета Set-AzDiagnosticSetting требовалось явное указание категорий во время создания параметра</span><span class="sxs-lookup"><span data-stu-id="7fee2-677">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="7fee2-678">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="7fee2-678">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7fee2-679">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7fee2-679">Az.Network</span></span>
* <span data-ttu-id="7fee2-680">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="7fee2-680">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="7fee2-681">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="7fee2-681">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="7fee2-682">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="7fee2-682">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="7fee2-683">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="7fee2-683">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="7fee2-684">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="7fee2-684">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="7fee2-685">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="7fee2-685">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="7fee2-686">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="7fee2-686">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7fee2-687">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7fee2-687">Az.PolicyInsights</span></span>
* <span data-ttu-id="7fee2-688">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="7fee2-688">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="7fee2-689">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fee2-689">Az.Resources</span></span>
* <span data-ttu-id="7fee2-690">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="7fee2-690">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="7fee2-691">Разрешено перечисление ресурсов с помощью параметра -ResourceId для командлета Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="7fee2-691">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7fee2-692">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7fee2-692">Az.ServiceBus</span></span>
* <span data-ttu-id="7fee2-693">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="7fee2-693">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7fee2-694">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7fee2-694">Az.ServiceFabric</span></span>
* <span data-ttu-id="7fee2-695">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="7fee2-695">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="7fee2-696">Исправлен командлет Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="7fee2-696">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="7fee2-697">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="7fee2-697">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="7fee2-698">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="7fee2-698">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="7fee2-699">Исправлен командлет Update-AzServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="7fee2-699">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="7fee2-700">0.4.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="7fee2-700">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="7fee2-701">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7fee2-701">Az.Profile</span></span>
* <span data-ttu-id="7fee2-702">Устранена проблема с Get-AzSubscription в CloudShell</span><span class="sxs-lookup"><span data-stu-id="7fee2-702">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="7fee2-703">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="7fee2-703">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7fee2-704">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7fee2-704">Az.Compute</span></span>
* <span data-ttu-id="7fee2-705">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzVm</span><span class="sxs-lookup"><span data-stu-id="7fee2-705">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="7fee2-706">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="7fee2-706">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7fee2-707">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7fee2-707">Az.DataLakeStore</span></span>
* <span data-ttu-id="7fee2-708">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="7fee2-708">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="7fee2-709">Get-AzDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7fee2-709">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="7fee2-710">Add-AzDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7fee2-710">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="7fee2-711">Set-AzDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7fee2-711">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="7fee2-712">Remove-AzDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7fee2-712">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7fee2-713">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7fee2-713">Az.Network</span></span>
* <span data-ttu-id="7fee2-714">Обновлен командлет Test-AzNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="7fee2-714">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="7fee2-715">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="7fee2-715">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7fee2-716">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fee2-716">Az.Resources</span></span>
* <span data-ttu-id="7fee2-717">Устранена проблема, из-за которой командлет Get-AzRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), благодаря добавлению понятного исключения в сценарий.</span><span class="sxs-lookup"><span data-stu-id="7fee2-717">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="7fee2-718">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="7fee2-718">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="7fee2-719">0.3.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="7fee2-719">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="7fee2-720">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="7fee2-720">Azure.Storage</span></span>
* <span data-ttu-id="7fee2-721">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="7fee2-721">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="7fee2-722">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="7fee2-722">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="7fee2-723">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="7fee2-723">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="7fee2-724">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="7fee2-724">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="7fee2-725">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="7fee2-725">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="7fee2-726">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7fee2-726">Az.CognitiveServices</span></span>
* <span data-ttu-id="7fee2-727">Поддержка Get-AzCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="7fee2-727">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7fee2-728">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7fee2-728">Az.Compute</span></span>
* <span data-ttu-id="7fee2-729">Исправлена команда Get-AzVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов</span><span class="sxs-lookup"><span data-stu-id="7fee2-729">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="7fee2-730">Добавлен пример использования SimpleParameterSet в справку командлета New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="7fee2-730">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="7fee2-731">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="7fee2-731">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="7fee2-732">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="7fee2-732">Az.DataFactoryV2</span></span>
* <span data-ttu-id="7fee2-733">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="7fee2-733">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7fee2-734">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7fee2-734">Az.Network</span></span>
* <span data-ttu-id="7fee2-735">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="7fee2-735">Added NetworkProfile functionality.</span></span> <span data-ttu-id="7fee2-736">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="7fee2-736">new cmdlets added</span></span>
    - <span data-ttu-id="7fee2-737">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7fee2-737">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="7fee2-738">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7fee2-738">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="7fee2-739">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7fee2-739">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="7fee2-740">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7fee2-740">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="7fee2-741">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="7fee2-741">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="7fee2-742">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="7fee2-742">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="7fee2-743">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="7fee2-743">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="7fee2-744">Добавлены командлеты: New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="7fee2-744">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="7fee2-745">Добавлены командлеты: Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="7fee2-745">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="7fee2-746">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="7fee2-746">Az.RedisCache</span></span>
* <span data-ttu-id="7fee2-747">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="7fee2-747">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="7fee2-748">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="7fee2-748">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="7fee2-749">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7fee2-749">Az.Resources</span></span>
* <span data-ttu-id="7fee2-750">Добавлен отсутствующий параметр -Mode в командлет Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7fee2-750">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="7fee2-751">Исправлена ошибка командлета Get-AzProviderOperation для операций, когда Origin содержит User</span><span class="sxs-lookup"><span data-stu-id="7fee2-751">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="7fee2-752">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7fee2-752">Az.Sql</span></span>
* <span data-ttu-id="7fee2-753">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="7fee2-753">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7fee2-754">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7fee2-754">Az.Websites</span></span>
* <span data-ttu-id="7fee2-755">Новый командлет Get-AzWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="7fee2-755">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="7fee2-756">Новые командлеты New-AzWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows</span><span class="sxs-lookup"><span data-stu-id="7fee2-756">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="7fee2-757">0.2.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="7fee2-757">0.2.0 - September 2018</span></span>
 <span data-ttu-id="7fee2-758">Первый выпуск</span><span class="sxs-lookup"><span data-stu-id="7fee2-758">Initial Release</span></span>