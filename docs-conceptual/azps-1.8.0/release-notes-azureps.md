---
ms.openlocfilehash: 10d8d50131b3c55ae19c5142c42cb47f37c68c92
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "63068920"
---
## <a name="180---april-2019"></a><span data-ttu-id="b8d9b-101">1.8.0 — апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-101">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="b8d9b-102">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="b8d9b-102">Highlights since the last major release</span></span>
* <span data-ttu-id="b8d9b-103">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-103">General availability of `Az` module</span></span>
* <span data-ttu-id="b8d9b-104">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="b8d9b-104">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="b8d9b-105">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="b8d9b-105">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="b8d9b-106">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-106">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="b8d9b-107">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-107">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="b8d9b-108">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-108">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="b8d9b-109">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="b8d9b-109">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="b8d9b-110">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b8d9b-110">Az.Accounts</span></span>
* <span data-ttu-id="b8d9b-111">Обновлен командлет Uninstall-AzureRm для правильного удаления модулей в Mac.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-111">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="b8d9b-112">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="b8d9b-112">Az.Batch</span></span>
* <span data-ttu-id="b8d9b-113">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-113">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="b8d9b-114">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b8d9b-114">Az.Cdn</span></span>
* <span data-ttu-id="b8d9b-115">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-115">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="b8d9b-116">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b8d9b-116">Az.CognitiveServices</span></span>
* <span data-ttu-id="b8d9b-117">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-117">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b8d9b-118">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b8d9b-118">Az.Compute</span></span>
* <span data-ttu-id="b8d9b-119">Устранена проблема с установкой AEM, если в идентификаторах ресурсов дисков группа ресурсов указана в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-119">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="b8d9b-120">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-120">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b8d9b-121">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-121">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b8d9b-122">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b8d9b-122">Az.DataFactory</span></span>
* <span data-ttu-id="b8d9b-123">Добавлены свойства SsisProperties, если NodeCount не имеет значения NULL для управляемой среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-123">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b8d9b-124">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b8d9b-124">Az.DataLakeStore</span></span>
* <span data-ttu-id="b8d9b-125">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-125">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="b8d9b-126">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="b8d9b-126">Az.EventGrid</span></span>
* <span data-ttu-id="b8d9b-127">Обновлен текст справки для конечной точки, указывающий, что необходимо создать ресурсы, прежде чем использовать командлеты для создания или обновления подписки на события.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-127">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="b8d9b-128">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b8d9b-128">Az.EventHub</span></span>
* <span data-ttu-id="b8d9b-129">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-129">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="b8d9b-130">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b8d9b-130">Az.HDInsight</span></span>
* <span data-ttu-id="b8d9b-131">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-131">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b8d9b-132">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b8d9b-132">Az.IotHub</span></span>
* <span data-ttu-id="b8d9b-133">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-133">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b8d9b-134">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b8d9b-134">Az.KeyVault</span></span>
* <span data-ttu-id="b8d9b-135">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-135">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b8d9b-136">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-136">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="b8d9b-137">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="b8d9b-137">Az.MachineLearning</span></span>
* <span data-ttu-id="b8d9b-138">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-138">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="b8d9b-139">Az.Media</span><span class="sxs-lookup"><span data-stu-id="b8d9b-139">Az.Media</span></span>
* <span data-ttu-id="b8d9b-140">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-140">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b8d9b-141">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b8d9b-141">Az.Monitor</span></span>
  * <span data-ttu-id="b8d9b-142">Добавлены новые командлеты для правила генерации оповещений на основе метрик GenV2 (не классических).</span><span class="sxs-lookup"><span data-stu-id="b8d9b-142">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="b8d9b-143">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="b8d9b-143">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="b8d9b-144">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="b8d9b-144">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="b8d9b-145">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="b8d9b-145">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="b8d9b-146">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="b8d9b-146">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="b8d9b-147">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="b8d9b-147">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="b8d9b-148">Обновлен пакет SDK Monitor до предварительной версии 0.22.0.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-148">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b8d9b-149">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b8d9b-149">Az.Network</span></span>
* <span data-ttu-id="b8d9b-150">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-150">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b8d9b-151">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-151">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="b8d9b-152">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="b8d9b-152">Az.NotificationHubs</span></span>
* <span data-ttu-id="b8d9b-153">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-153">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b8d9b-154">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b8d9b-154">Az.OperationalInsights</span></span>
* <span data-ttu-id="b8d9b-155">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-155">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="b8d9b-156">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="b8d9b-156">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="b8d9b-157">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-157">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b8d9b-158">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b8d9b-158">Az.RecoveryServices</span></span>
* <span data-ttu-id="b8d9b-159">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-159">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b8d9b-160">Обновлен табличный формат для SQL на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-160">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="b8d9b-161">Добавлен альтернативный метод для получения расположения в Общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-161">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="b8d9b-162">Обновлено значение ScheduleRunDays в объекте SchedulePolicy в соответствии с часовым поясом.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-162">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="b8d9b-163">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="b8d9b-163">Az.RedisCache</span></span>
* <span data-ttu-id="b8d9b-164">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-164">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b8d9b-165">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b8d9b-165">Az.Resources</span></span>
* <span data-ttu-id="b8d9b-166">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-166">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="b8d9b-167">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b8d9b-167">Az.Sql</span></span>
* <span data-ttu-id="b8d9b-168">Заменена зависимость от пакета SDK монитора на обычный код.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-168">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="b8d9b-169">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-169">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b8d9b-170">Улучшен процесс классификации нескольких столбцов.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-170">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="b8d9b-171">Добавлены свойства SKU (имя, семейство, производительность SKU) в отклике Get-AzSqlServerServiceObjective, а также по умолчанию задан табличный формат.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-171">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="b8d9b-172">C помощью Get-AzSqlServerServiceObjective теперь можно получать список доступных целевых служб по расположению без необходимости заранее размещать сервер в регионе.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-172">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="b8d9b-173">Поддерживается параметр часового пояса при создании Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-173">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="b8d9b-174">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-174">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b8d9b-175">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b8d9b-175">Az.Websites</span></span>
* <span data-ttu-id="b8d9b-176">Исправлены командлеты Set-AzWebApp и Set-AzWebAppSlot, которые теперь не удаляют теги при выполнении.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-176">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="b8d9b-177">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-177">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b8d9b-178">Обновлен пакет SDK веб-узлов.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-178">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="b8d9b-179">Удалено свойство AdminSiteName из PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-179">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="b8d9b-180">1.7.0 —апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-180">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="b8d9b-181">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="b8d9b-181">Highlights since the last major release</span></span>
* <span data-ttu-id="b8d9b-182">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-182">General availability of `Az` module</span></span>
* <span data-ttu-id="b8d9b-183">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="b8d9b-183">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="b8d9b-184">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="b8d9b-184">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="b8d9b-185">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-185">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="b8d9b-186">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-186">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="b8d9b-187">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-187">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="b8d9b-188">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="b8d9b-188">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="b8d9b-189">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b8d9b-189">Az.Accounts</span></span>
* <span data-ttu-id="b8d9b-190">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметр AzureAnalysisServicesEndpointResourceId.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-190">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="b8d9b-191">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b8d9b-191">Az.AnalysisServices</span></span>
* <span data-ttu-id="b8d9b-192">Использование ServiceClient в командлетах плоскости данных и удаление исходной логики проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-192">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="b8d9b-193">Add-AzureASAccount используется как оболочка для Connect-AzAccount во избежание критических изменений.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-193">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b8d9b-194">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b8d9b-194">Az.Automation</span></span>
* <span data-ttu-id="b8d9b-195">Исправлена ошибка командлета New-AzAutomationSoftwareUpdateConfiguration, связанная с включением.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-195">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="b8d9b-196">Теперь параметры IncludedKbNumber и IncludedPackageNameMask должны работать нормально.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-196">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="b8d9b-197">Исправлена ошибка динамической группы управления обновлениями службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-197">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b8d9b-198">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b8d9b-198">Az.Compute</span></span>
* <span data-ttu-id="b8d9b-199">В командлеты New-AzDiskConfig и New-AzSnapshotConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-199">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="b8d9b-200">Теперь можно создавать виртуальные машину на основе образов из коллекции от других клиентов.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-200">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="b8d9b-201">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="b8d9b-201">Az.ContainerInstance</span></span>
* <span data-ttu-id="b8d9b-202">Исправлена проблема в параметре -Command командлета New-AzContainerGroup, из-за которой в конце добавлялся пустой аргумент.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-202">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b8d9b-203">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b8d9b-203">Az.DataFactory</span></span>
* <span data-ttu-id="b8d9b-204">Пакет SDK для ADF .NET обновлен до версии 3.0.2.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-204">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="b8d9b-205">Командлет Set-AzDataFactoryV2 обновлен с помощью дополнительных параметров для настроек, связанных с RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-205">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b8d9b-206">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b8d9b-206">Az.Resources</span></span>
* <span data-ttu-id="b8d9b-207">Улучшена обработка поставщиков Get-AzResource при предоставлении параметров -ResourceId или -ResourceGroupName, -Name и -ResourceType.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-207">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="b8d9b-208">Улучшена обработка ошибок в командлетах Test-AzDeployment и Test-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-208">Improve error handling for for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="b8d9b-209">Теперь ошибки, возникающие за пределами проверки развертывания, обрабатываются и включаются в выходные данные команды.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-209">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="b8d9b-210">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-210">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="b8d9b-211">Добавлен параметр-переключатель -IgnoreDynamicParameters, с помощью которого можно настроить командлеты развертывания так, чтобы они пропускали запросы в сценариях скриптов и заданий.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-211">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="b8d9b-212">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-212">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="b8d9b-213">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b8d9b-213">Az.Sql</span></span>
* <span data-ttu-id="b8d9b-214">Поддержка классификации данных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-214">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b8d9b-215">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b8d9b-215">Az.Storage</span></span>
* <span data-ttu-id="b8d9b-216">Подробные сообщения об ошибке передаются при создании контекста хранилища с помощью параметра -UseConnectedAccount, но без входа в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-216">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="b8d9b-217">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="b8d9b-217">New-AzStorageContext</span></span>
* <span data-ttu-id="b8d9b-218">Поддержка свойств службы управления BLOB-объектов в указанной учетной записи хранения с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-218">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="b8d9b-219">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="b8d9b-219">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="b8d9b-220">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="b8d9b-220">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="b8d9b-221">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b8d9b-221">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="b8d9b-222">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b8d9b-222">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="b8d9b-223">Поддержка параметра -AsJob в командлетах для отправки и скачивания больших двоичных объектов и файлов.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-223">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="b8d9b-224">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b8d9b-224">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="b8d9b-225">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b8d9b-225">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="b8d9b-226">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="b8d9b-226">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="b8d9b-227">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="b8d9b-227">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="b8d9b-228">1.6.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-228">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="b8d9b-229">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="b8d9b-229">Highlights since the last major release</span></span>
* <span data-ttu-id="b8d9b-230">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-230">General availability of `Az` module</span></span>
* <span data-ttu-id="b8d9b-231">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="b8d9b-231">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="b8d9b-232">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="b8d9b-232">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="b8d9b-233">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-233">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="b8d9b-234">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-234">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="b8d9b-235">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-235">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="b8d9b-236">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="b8d9b-236">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b8d9b-237">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b8d9b-237">Az.Automation</span></span>
* <span data-ttu-id="b8d9b-238">В управление обновлениями службы автоматизации Azure внесены изменения для поддержки следующих новых функций:</span><span class="sxs-lookup"><span data-stu-id="b8d9b-238">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="b8d9b-239">динамическое группирование;</span><span class="sxs-lookup"><span data-stu-id="b8d9b-239">Dynamic grouping</span></span>
    * <span data-ttu-id="b8d9b-240">скрипты предварительного или последующего выполнения;</span><span class="sxs-lookup"><span data-stu-id="b8d9b-240">Pre-Post script</span></span>
    * <span data-ttu-id="b8d9b-241">параметр перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-241">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b8d9b-242">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b8d9b-242">Az.Compute</span></span>
* <span data-ttu-id="b8d9b-243">Устранена проблема, связанная с разрешением пути в Get-AzVmBootDiagnosticsData.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-243">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="b8d9b-244">Обновление клиентской библиотеки вычислений до версии 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-244">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b8d9b-245">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b8d9b-245">Az.KeyVault</span></span>
* <span data-ttu-id="b8d9b-246">Добавлена поддержка подстановочных знаков в командлетах KeyVault.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-246">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b8d9b-247">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b8d9b-247">Az.Network</span></span>
* <span data-ttu-id="b8d9b-248">Добавлена поддержка анализа угроз для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-248">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="b8d9b-249">Добавлены настраиваемые правила и ресурс верхнего уровня для политики брандмауэра Шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-249">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b8d9b-250">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b8d9b-250">Az.RecoveryServices</span></span>
* <span data-ttu-id="b8d9b-251">В политику виртуальной машины Azure добавлен объект SnapshotRetentionInDays для поддержки мгновенного восстановления.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-251">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="b8d9b-252">Добавлена поддержка канала для отмены регистрации контейнера.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-252">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="b8d9b-253">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b8d9b-253">Az.Resources</span></span>
* <span data-ttu-id="b8d9b-254">Обновлена поддержка подстановочных знаков для Get-AzResource и Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-254">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="b8d9b-255">Обновлены учетные данные, используемые при общих вызовах к ARM.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-255">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="b8d9b-256">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b8d9b-256">Az.Sql</span></span>
* <span data-ttu-id="b8d9b-257">Изменен тип параметра (ExcludeDetectionType) командлетов для обнаружения угроз с DetectionTypes на string[] для поддержки актуального состояния при добавлении новых типов обнаружения и для поддержки автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-257">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b8d9b-258">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b8d9b-258">Az.Storage</span></span>
* <span data-ttu-id="b8d9b-259">Поддержка получения, настройки и удаления политики управления в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-259">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="b8d9b-260">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="b8d9b-260">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="b8d9b-261">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="b8d9b-261">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="b8d9b-262">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="b8d9b-262">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="b8d9b-263">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="b8d9b-263">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="b8d9b-264">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="b8d9b-264">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="b8d9b-265">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="b8d9b-265">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b8d9b-266">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b8d9b-266">Az.Websites</span></span>
* <span data-ttu-id="b8d9b-267">Исправлена ошибка с шаблоном ARM, из-за которой прерывалось клонирование все слотов при использовании New-AzWebApp -IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-267">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="b8d9b-268">1.5.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-268">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b8d9b-269">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b8d9b-269">Az.Accounts</span></span>
* <span data-ttu-id="b8d9b-270">Добавлена команда Register-AzModule для поддержки созданных командлетов AutoRest.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-270">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="b8d9b-271">Обновлены примеры для Connect AzAccount.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-271">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b8d9b-272">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b8d9b-272">Az.Automation</span></span>
* <span data-ttu-id="b8d9b-273">Исправлена проблема с получением некоторых ежемесячных расписаний в нескольких командлетах службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-273">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="b8d9b-274">Исправлен командлет Get-AzAutomationDscNode, возвращающий только первые 20 узлов.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-274">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="b8d9b-275">Теперь он возвращает все узлы.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-275">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="b8d9b-276">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b8d9b-276">Az.Cdn</span></span>
* <span data-ttu-id="b8d9b-277">Добавлены новые командлеты PowerShell для включения и отключения HTTPS для личного домена и отключены устаревшие командлеты.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-277">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b8d9b-278">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b8d9b-278">Az.Compute</span></span>
* <span data-ttu-id="b8d9b-279">Добавлена поддержка подстановочных знаков в командлетах Get.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-279">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b8d9b-280">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b8d9b-280">Az.DataFactory</span></span>
* <span data-ttu-id="b8d9b-281">Обновлен пакет SDK для ADF .NET до версии 3.0.1.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-281">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="b8d9b-282">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b8d9b-282">Az.LogicApp</span></span>
* <span data-ttu-id="b8d9b-283">Исправлена проблема с получением только первой страницы результатов при выполнении команды ListWorkflows.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-283">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b8d9b-284">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b8d9b-284">Az.Network</span></span>
* <span data-ttu-id="b8d9b-285">Добавлена поддержка подстановочных знаков в командлетах Network.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-285">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b8d9b-286">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b8d9b-286">Az.RecoveryServices</span></span>
* <span data-ttu-id="b8d9b-287">Добавлена поддержка SQL Server на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-287">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="b8d9b-288">Обновление пакета SDK</span><span class="sxs-lookup"><span data-stu-id="b8d9b-288">SDK Update</span></span>
* <span data-ttu-id="b8d9b-289">Удалена проверка VMappContainer в Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-289">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="b8d9b-290">Добавлены параметры Name и ServerName для Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-290">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="b8d9b-291">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b8d9b-291">Az.Resources</span></span>
* <span data-ttu-id="b8d9b-292">Добавлен параметр `-TemplateObject` в командлеты для развертывания.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-292">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="b8d9b-293">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2933.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-293">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="b8d9b-294">Устранена проблема с передачей в конвейер результата `Get-AzResource` для `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-294">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="b8d9b-295">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8240.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-295">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="b8d9b-296">Устранена проблема с изменением типа данных JSON при выполнении `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-296">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="b8d9b-297">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7930.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-297">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="b8d9b-298">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b8d9b-298">Az.Sql</span></span>
* <span data-ttu-id="b8d9b-299">Обновление AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-299">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="b8d9b-300">Исправлено поведение для пограничного случая при создании параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-300">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b8d9b-301">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b8d9b-301">Az.Storage</span></span>
* <span data-ttu-id="b8d9b-302">Включена поддержка Kind BlockBlobStorage при создании учетной записи хранения для New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-302">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="b8d9b-303">1.4.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-303">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="b8d9b-304">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b8d9b-304">Az.AnalysisServices</span></span>
* <span data-ttu-id="b8d9b-305">Командлет AddAzureASAccount устарел.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-305">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b8d9b-306">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b8d9b-306">Az.Automation</span></span>
* <span data-ttu-id="b8d9b-307">Обновлена справка для командлета Import-AzAutomationDscNodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-307">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="b8d9b-308">Добавлена проверка имени конфигурации для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-308">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="b8d9b-309">Улучшена обработка ошибок для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-309">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="b8d9b-310">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b8d9b-310">Az.CognitiveServices</span></span>
* <span data-ttu-id="b8d9b-311">Добавлен параметр CustomSubdomainName — новый необязательный параметр для командлета New-AzCognitiveServicesAccount, который указывает поддомен для ресурса.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-311">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b8d9b-312">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b8d9b-312">Az.Compute</span></span>
* <span data-ttu-id="b8d9b-313">Устранена проблема с идентификаторами наборов параметров.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-313">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="b8d9b-314">Обновлен командлет Get-AzVMExtension для отображения списка всех установленных расширений, если не указан параметр Name.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-314">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="b8d9b-315">Для командлета Update-AzImage добавлены параметры Tag и ResourceId.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-315">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="b8d9b-316">Командлет Get-AzVmssVM, который выполняется без указания идентификатора экземпляра и с параметром InstanceView, может выводить виртуальные машины из VMSS с представлением экземпляра.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-316">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b8d9b-317">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b8d9b-317">Az.DataLakeStore</span></span>
* <span data-ttu-id="b8d9b-318">Добавлены командлеты для перечисления и восстановления удаленного элемента ADL.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-318">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="b8d9b-319">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b8d9b-319">Az.EventHub</span></span>
* <span data-ttu-id="b8d9b-320">Добавлено новое логическое свойство SkipEmptyArchives для пропуска пустых архивов в классе CaptureDescription Eventhub.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-320">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="b8d9b-321">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b8d9b-321">Az.KeyVault</span></span>
* <span data-ttu-id="b8d9b-322">Исправлена расстановка тегов для командлета Set-AzKeyVaultSecret.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-322">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="b8d9b-323">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b8d9b-323">Az.LogicApp</span></span>
* <span data-ttu-id="b8d9b-324">Добавлен SKU "Базовый" для учетных записей интеграции.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-324">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="b8d9b-325">Добавлены типы сопоставлений Liquid, а также XSLT 2.0 и XSLT 3.0.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-325">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="b8d9b-326">Новые командлеты для сборок учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="b8d9b-326">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="b8d9b-327">Get-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="b8d9b-327">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="b8d9b-328">New-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="b8d9b-328">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="b8d9b-329">Remove-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="b8d9b-329">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="b8d9b-330">Set-AzIntegrationAccountAssembly.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-330">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="b8d9b-331">Новые командлеты для конфигурации пакета учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="b8d9b-331">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="b8d9b-332">Get-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="b8d9b-332">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="b8d9b-333">New-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="b8d9b-333">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="b8d9b-334">Remove-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="b8d9b-334">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="b8d9b-335">Set-AzIntegrationAccountBatchConfiguration.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-335">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="b8d9b-336">Обновлен пакет SDK Logic Apps до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-336">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b8d9b-337">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b8d9b-337">Az.Monitor</span></span>
* <span data-ttu-id="b8d9b-338">Обновлена справка для командлета Get-AzMetric.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-338">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b8d9b-339">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b8d9b-339">Az.Network</span></span>
* <span data-ttu-id="b8d9b-340">Обновлен пример справки для командлета Add-AzApplicationGatewayCustomError.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-340">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b8d9b-341">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b8d9b-341">Az.OperationalInsights</span></span>
* <span data-ttu-id="b8d9b-342">Дополнительная поддержка создания и получения источников данных ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-342">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="b8d9b-343">Добавлен новый тип ApplicationInsights для получения определенных или всех источников данных ApplicationInsights для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-343">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="b8d9b-344">Добавлен командлет New-AzOperationalInsightsApplicationInsightsDataSource для создания источника данных с использованием параметров указанного ресурса Application-Insightss: subscription Id, resourceGroupName и name.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-344">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="b8d9b-345">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b8d9b-345">Az.Resources</span></span>
* <span data-ttu-id="b8d9b-346">исправлена проблема https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-346">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="b8d9b-347">исправлена проблема https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-347">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="b8d9b-348">исправлена проблема https://github.com/Azure/azure-powershell/issues/6219.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-348">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="b8d9b-349">Исправлена ошибка, препятствующая повторному созданию KeyCredentials.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-349">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="b8d9b-350">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b8d9b-350">Az.Sql</span></span>
* <span data-ttu-id="b8d9b-351">Добавлена поддержка уровня гипермасштабирования в базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-351">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="b8d9b-352">Исправлена ошибка, из-за которой восстановление могло завершиться со сбоем при указании ненужных свойств в запросе на восстановление.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-352">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b8d9b-353">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b8d9b-353">Az.Websites</span></span>
* <span data-ttu-id="b8d9b-354">Исправлен пример для командлета Get-AzWebAppSlotMetrics.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-354">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="b8d9b-355">1.3.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-355">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b8d9b-356">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b8d9b-356">Az.Accounts</span></span>
* <span data-ttu-id="b8d9b-357">Обновление до последней версии ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="b8d9b-357">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="b8d9b-358">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b8d9b-358">Az.AnalysisServices</span></span>
<span data-ttu-id="b8d9b-359">Общедоступная версия модуля Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-359">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b8d9b-360">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b8d9b-360">Az.Compute</span></span>
* <span data-ttu-id="b8d9b-361">Расширение AEM: добавлена поддержка дисков UltraSSD, P60, P70 и P80.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-361">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="b8d9b-362">Обновлено описание справки для командлета Set-AzVMBootDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-362">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="b8d9b-363">Обновлено описание справки и пример для командлета Update-AzImage.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-363">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b8d9b-364">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b8d9b-364">Az.RecoveryServices</span></span>
<span data-ttu-id="b8d9b-365">Общедоступная версия модуля Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-365">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b8d9b-366">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b8d9b-366">Az.Resources</span></span>
* <span data-ttu-id="b8d9b-367">Исправлена расстановка тегов для групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-367">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="b8d9b-368">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-368">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="b8d9b-369">Исправлена проблема с игнорированием командлетом `Get-AzureRmRoleAssignment` параметра -ErrorAction.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-369">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="b8d9b-370">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-370">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="b8d9b-371">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b8d9b-371">Az.Sql</span></span>
* <span data-ttu-id="b8d9b-372">Добавлен командлет Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-372">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="b8d9b-373">Исправлена проблема с появлением исключения NullRef при выполнении командлетов SQL, если не выполнен вход в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-373">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="b8d9b-374">Исправлено исключение NullRef в командлете Get-AzSqlCapability.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-374">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="b8d9b-375">1.2.1 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-375">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b8d9b-376">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b8d9b-376">Az.Accounts</span></span>
* <span data-ttu-id="b8d9b-377">Выпуск с правильной версией службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-377">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="b8d9b-378">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b8d9b-378">Az.AnalysisServices</span></span>
* <span data-ttu-id="b8d9b-379">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-379">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b8d9b-380">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b8d9b-380">Az.RecoveryServices</span></span>
* <span data-ttu-id="b8d9b-381">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-381">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="b8d9b-382">1.2.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-382">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b8d9b-383">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b8d9b-383">Az.Accounts</span></span>
* <span data-ttu-id="b8d9b-384">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-384">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="b8d9b-385">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-385">Update incorrect online help URLs</span></span>
* <span data-ttu-id="b8d9b-386">Добавлено предупреждающее сообщение в PS Core для модуля Uninstall-AzureRm.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-386">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="b8d9b-387">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="b8d9b-387">Az.Aks</span></span>
* <span data-ttu-id="b8d9b-388">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-388">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b8d9b-389">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b8d9b-389">Az.Automation</span></span>
* <span data-ttu-id="b8d9b-390">Добавлена поддержка для модулей runbook Python 2.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-390">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="b8d9b-391">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-391">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="b8d9b-392">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b8d9b-392">Az.Cdn</span></span>
* <span data-ttu-id="b8d9b-393">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-393">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b8d9b-394">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b8d9b-394">Az.Compute</span></span>
* <span data-ttu-id="b8d9b-395">Добавлен командлет Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-395">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="b8d9b-396">Добавлен параметр TempDisk к командлету Set-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-396">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="b8d9b-397">Исправлено предупреждающее сообщение командлета New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-397">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="b8d9b-398">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b8d9b-398">Az.ContainerRegistry</span></span>
* <span data-ttu-id="b8d9b-399">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-399">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b8d9b-400">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b8d9b-400">Az.DataFactory</span></span>
* <span data-ttu-id="b8d9b-401">Пакет SDK ADF .Net обновлен до версии 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-401">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b8d9b-402">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b8d9b-402">Az.DataLakeStore</span></span>
* <span data-ttu-id="b8d9b-403">Исправлена проблема с конечной точкой ADLS при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-403">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="b8d9b-404">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7462.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-404">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="b8d9b-405">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-405">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b8d9b-406">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b8d9b-406">Az.IotHub</span></span>
* <span data-ttu-id="b8d9b-407">Добавлен формат кодирования для командлета Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-407">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b8d9b-408">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b8d9b-408">Az.KeyVault</span></span>
* <span data-ttu-id="b8d9b-409">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-409">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b8d9b-410">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b8d9b-410">Az.Network</span></span>
* <span data-ttu-id="b8d9b-411">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-411">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="b8d9b-412">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b8d9b-412">Az.Resources</span></span>
* <span data-ttu-id="b8d9b-413">Исправлены неправильные примеры в справочной документации по командлетам New-AzADAppCredential и New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-413">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="b8d9b-414">Исправлена проблема, при которой путь для параметра -TemplateFile не удавалось разрешить до выполнения командлетов развертывания групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-414">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="b8d9b-415">Az.Resources: исправлена документация для значения по умолчанию -Mode командлета New-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-415">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="b8d9b-416">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/7522.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-416">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="b8d9b-417">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/5747.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-417">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="b8d9b-418">Исправлена проблема с форматированием объекта PSResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-418">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="b8d9b-419">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2123.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-419">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b8d9b-420">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b8d9b-420">Az.ServiceFabric</span></span>
* <span data-ttu-id="b8d9b-421">Исправлена проблема с появлением исключения в процессе отката при добавлении сертификата к модели VMSS: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-421">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="b8d9b-422">Исправлены некоторые сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-422">Fix some error messages.</span></span>
* <span data-ttu-id="b8d9b-423">Исправлена проблема с созданием кластера с шаблоном ARM по умолчанию для командлета New-AzServiceFabriCluster, который не работал с операцией миграции в Az.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-423">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="b8d9b-424">Исправлена проблема с добавлением сертификата кластера или приложения: теперь они добавляются только в Масштабируемые наборы виртуальных машин, которые сопоставлены с кластером, путем проверки идентификатора кластера в расширении.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-424">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="b8d9b-425">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="b8d9b-425">Az.SignalR</span></span>
* <span data-ttu-id="b8d9b-426">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-426">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="b8d9b-427">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b8d9b-427">Az.Sql</span></span>
* <span data-ttu-id="b8d9b-428">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-428">Update incorrect online help URLs</span></span>
* <span data-ttu-id="b8d9b-429">Обновлено описание параметра LicenseType с добавлением возможных значений.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-429">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="b8d9b-430">Исправлена проблема с неправильным обновлением удостоверения управляемого экземпляра, если оно было единственным обновляемым свойством.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-430">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="b8d9b-431">Поддержка пользовательских параметров сортировки в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-431">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b8d9b-432">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b8d9b-432">Az.Storage</span></span>
* <span data-ttu-id="b8d9b-433">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-433">Update incorrect online help URLs</span></span>
* <span data-ttu-id="b8d9b-434">Добавлен вывод подробных сообщений об ошибке при получении или установке классических свойств ведения журнала или метрик в учетной записи хранилища класса Premium, так как учетная запись хранилища класса Premium не поддерживает классические функции ведения журнала и метрик.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-434">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="b8d9b-435">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="b8d9b-435">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="b8d9b-436">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="b8d9b-436">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="b8d9b-437">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="b8d9b-437">Az.TrafficManager</span></span>
* <span data-ttu-id="b8d9b-438">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-438">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b8d9b-439">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b8d9b-439">Az.Websites</span></span>
* <span data-ttu-id="b8d9b-440">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-440">Update incorrect online help URLs</span></span>
* <span data-ttu-id="b8d9b-441">Исправлена работа командлета New-AzWebAppSSLBinding: сертификат отправляется в правильную группу ресурсов и правильное расположение, если приложение размещено в ASE.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-441">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="b8d9b-442">Исправлена работа командлета New-AzWebAppSSLBinding: теги не перезаписываются при привязке SSL-сертификата к приложению.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-442">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="b8d9b-443">1.1.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-443">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b8d9b-444">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b8d9b-444">Az.Accounts</span></span>
* <span data-ttu-id="b8d9b-445">Добавление области "Local" в Enable-AzureRmAlias.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-445">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b8d9b-446">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b8d9b-446">Az.Compute</span></span>
* <span data-ttu-id="b8d9b-447">Теперь имя не является обязательным в идентификаторе набора параметров для Restart/Start/Stop/Remove/Set-AzVM и Save-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-447">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="b8d9b-448">Обновлено описание идентификатора в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-448">Updated the description of ID in help files</span></span>
* <span data-ttu-id="b8d9b-449">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-449">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b8d9b-450">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b8d9b-450">Az.DataLakeStore</span></span>
* <span data-ttu-id="b8d9b-451">Обновление версии пакета SDK для плоскости данных до 1.1.14 для устранения найденных проблем.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-451">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="b8d9b-452">Исправлена обработка отрицательного времени доступа и времени изменения для getfilestatus и liststatus, исправлен токен отмены для асинхронных методов.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-452">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="b8d9b-453">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="b8d9b-453">Az.EventGrid</span></span>
* <span data-ttu-id="b8d9b-454">Обновление для использования API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-454">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="b8d9b-455">Обновлены указанные ниже командлеты для поддержки нового сценария в API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-455">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="b8d9b-456">New-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="b8d9b-456">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="b8d9b-457">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="b8d9b-457">Event Time-To-Live,</span></span>
        - <span data-ttu-id="b8d9b-458">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="b8d9b-458">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="b8d9b-459">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-459">Dead letter endpoint.</span></span>
    - <span data-ttu-id="b8d9b-460">Update-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="b8d9b-460">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="b8d9b-461">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="b8d9b-461">Event Time-To-Live,</span></span>
        - <span data-ttu-id="b8d9b-462">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="b8d9b-462">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="b8d9b-463">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-463">Dead letter endpoint.</span></span>
* <span data-ttu-id="b8d9b-464">Для параметра EndpointType добавлены новые значения перечисления (storageQueue и hybridConnection) в командлеты New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-464">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="b8d9b-465">Если ожидается, что создание или обновление подписки на событие повлечет за собой действия со стороны пользователя, выполняемые вручную, отображается предупреждение при создании или обновлении подписки события.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-465">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b8d9b-466">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b8d9b-466">Az.IotHub</span></span>
* <span data-ttu-id="b8d9b-467">Пакет SDK Центра Интернета вещей обновлен до последней версии.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-467">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="b8d9b-468">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b8d9b-468">Az.LogicApp</span></span>
* <span data-ttu-id="b8d9b-469">Get-AzLogicApp позволяет перечислить все параметры без указанного имени.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-469">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="b8d9b-470">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b8d9b-470">Az.Resources</span></span>
* <span data-ttu-id="b8d9b-471">Исправлена проблема с набором параметров при предоставлении параметров "-ODataQuery" и "-ResourceId" для "Get-AzResource".</span><span class="sxs-lookup"><span data-stu-id="b8d9b-471">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="b8d9b-472">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7875.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-472">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="b8d9b-473">Исправлена обработка параметра -Custom в New/Set-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-473">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="b8d9b-474">Исправлена опечатка в документации по New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-474">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="b8d9b-475">Параметр "-MailNickname" стал обязательным для "New-AzADUser".</span><span class="sxs-lookup"><span data-stu-id="b8d9b-475">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="b8d9b-476">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8220.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-476">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="b8d9b-477">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="b8d9b-477">Az.SignalR</span></span>
* <span data-ttu-id="b8d9b-478">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-478">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="b8d9b-479">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b8d9b-479">Az.Sql</span></span>
* <span data-ttu-id="b8d9b-480">Зависимость клиента управления хранением преобразована для общей реализации в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-480">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b8d9b-481">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b8d9b-481">Az.Storage</span></span>
* <span data-ttu-id="b8d9b-482">Установка параметра StorageAccountName для контекста хранилища в качестве реального имени учетной записи хранения, если она была создана с использованием токена Sas, OAuth или анонимного доступа.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-482">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="b8d9b-483">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="b8d9b-483">New-AzStorageContext</span></span>
* <span data-ttu-id="b8d9b-484">Создание токена Sas большого двоичного объекта моментального снимка с параметром "-FullUri". Возвращаемый URI исправлен на URI моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-484">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="b8d9b-485">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="b8d9b-485">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b8d9b-486">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b8d9b-486">Az.Websites</span></span>
* <span data-ttu-id="b8d9b-487">Исправлена ошибка синтаксического анализа даты в "Get-AzDeletedWebApp".</span><span class="sxs-lookup"><span data-stu-id="b8d9b-487">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="b8d9b-488">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-488">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="b8d9b-489">1.0.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-489">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="b8d9b-490">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="b8d9b-490">General</span></span>

- <span data-ttu-id="b8d9b-491">Общедоступная версия модуля Az.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-491">General Availability of Az Module</span></span>
- <span data-ttu-id="b8d9b-492">Справка в Интернете для каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-492">Online help for each module</span></span>
- <span data-ttu-id="b8d9b-493">Дополнительные сведения и стратегию развития см. в статье [Announcing New Module 'Az'](https://aka.ms/azps-announce) (Объявление о новом модуле Az)</span><span class="sxs-lookup"><span data-stu-id="b8d9b-493">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="b8d9b-494">Сведения о миграции с AzureRM см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="b8d9b-494">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="b8d9b-495">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b8d9b-495">Az.Accounts</span></span>
- <span data-ttu-id="b8d9b-496">Изменено с Az.Profile.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-496">Changed from Az.Profile</span></span>
- <span data-ttu-id="b8d9b-497">Исправлены форматы таблиц для типов профиля и контекста.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-497">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="b8d9b-498">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b8d9b-498">Az.ApiManagement</span></span>
- <span data-ttu-id="b8d9b-499">Исправления для #7002.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-499">Fixes for #7002</span></span>
- <span data-ttu-id="b8d9b-500">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="b8d9b-500">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="b8d9b-501">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="b8d9b-501">Az.Batch</span></span>
- <span data-ttu-id="b8d9b-502">Добавлена возможность видеть, какая версия агента узла пакетной службы Azure работает в пуле на каждой виртуальной машине, с помощью нового свойства `NodeAgentInformation` в `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-502">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="b8d9b-503">Значение `Caching` по умолчанию для `PSDataDisk` теперь `ReadWrite` вместо `None`.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-503">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="b8d9b-504">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="b8d9b-504">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="b8d9b-505">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="b8d9b-505">Az.Billing</span></span>
- <span data-ttu-id="b8d9b-506">Объединены командлеты Billing, Consumption и UsageAggregates. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0).</span><span class="sxs-lookup"><span data-stu-id="b8d9b-506">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="b8d9b-507">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="b8d9b-507">Az.CognitivServices</span></span>
- <span data-ttu-id="b8d9b-508">Добавлены средства заполнения для SkuName и Typem, доступные в операции New-AzureRmCognitiveServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-508">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="b8d9b-509">Удален набор параметров GetSkusWithAccountParamSetName из Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-509">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="b8d9b-510">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="b8d9b-510">Az.ContainerInstance</span></span>
- <span data-ttu-id="b8d9b-511">Добавлена поддержка ManagedIdentity.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-511">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="b8d9b-512">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="b8d9b-512">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="b8d9b-513">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="b8d9b-513">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="b8d9b-514">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b8d9b-514">Az.DataLakeStore</span></span>
- <span data-ttu-id="b8d9b-515">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="b8d9b-515">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="b8d9b-516">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b8d9b-516">Az.Monitor</span></span>
- <span data-ttu-id="b8d9b-517">"Az.Insights" переименован в "Az.Monitor" и внесены другие незначительные критические изменения. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="b8d9b-517">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="b8d9b-518">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b8d9b-518">Az.KeyVault</span></span>
- <span data-ttu-id="b8d9b-519">Из типов вывода удалено устаревшее свойство PurgeDisabled</span><span class="sxs-lookup"><span data-stu-id="b8d9b-519">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="b8d9b-520">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="b8d9b-520">Az.MachineLearning</span></span>
- <span data-ttu-id="b8d9b-521">Включены командлеты из модуля Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="b8d9b-521">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="b8d9b-522">Az.Media</span><span class="sxs-lookup"><span data-stu-id="b8d9b-522">Az.Media</span></span>
- <span data-ttu-id="b8d9b-523">Удаляет устаревший псевдоним Tags из New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="b8d9b-523">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="b8d9b-524">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b8d9b-524">Az.Network</span></span>
<span data-ttu-id="b8d9b-525">В шлюз приложений добавлена поддержка настройки RewriteRuleSets</span><span class="sxs-lookup"><span data-stu-id="b8d9b-525">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="b8d9b-526">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="b8d9b-526">New cmdlets added:</span></span>
        - <span data-ttu-id="b8d9b-527">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b8d9b-527">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b8d9b-528">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b8d9b-528">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b8d9b-529">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b8d9b-529">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b8d9b-530">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b8d9b-530">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b8d9b-531">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b8d9b-531">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b8d9b-532">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="b8d9b-532">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="b8d9b-533">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="b8d9b-533">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="b8d9b-534">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="b8d9b-534">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="b8d9b-535">В следующие командлеты добавлен необязательный параметр -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b8d9b-535">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="b8d9b-536">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b8d9b-536">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="b8d9b-537">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b8d9b-537">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="b8d9b-538">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b8d9b-538">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="b8d9b-539">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b8d9b-539">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="b8d9b-540">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="b8d9b-540">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="b8d9b-541">New-AzureRmApplicationGatewayUrlPathMapConfig добавил с помощью идентификатора поддержку KeyVault для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-541">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="b8d9b-542">В следующие командлеты добавлен необязательный параметр -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b8d9b-542">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="b8d9b-543">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b8d9b-543">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="b8d9b-544">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b8d9b-544">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="b8d9b-545">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b8d9b-545">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="b8d9b-546">В командлет New-AzApplicationGateway добавлен необязательный параметр -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="b8d9b-546">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="b8d9b-547">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="b8d9b-547">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="b8d9b-548">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b8d9b-548">Az.OperationalInsights</span></span>
- <span data-ttu-id="b8d9b-549">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="b8d9b-549">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="b8d9b-550">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="b8d9b-550">Az.Profile</span></span>
- <span data-ttu-id="b8d9b-551">Имя модуля изменено на Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-551">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="b8d9b-552">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b8d9b-552">Az.RecoveryServices</span></span>
- <span data-ttu-id="b8d9b-553">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="b8d9b-553">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="b8d9b-554">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b8d9b-554">Az.Resources</span></span>
- <span data-ttu-id="b8d9b-555">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="b8d9b-555">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="b8d9b-556">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b8d9b-556">Az.ServiceFabric</span></span>
- <span data-ttu-id="b8d9b-557">Поддержка спецификации сертификата по общему имени и отпечатку</span><span class="sxs-lookup"><span data-stu-id="b8d9b-557">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="b8d9b-558">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="b8d9b-558">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="b8d9b-559">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="b8d9b-559">Az.SIgnalR</span></span>
- <span data-ttu-id="b8d9b-560">Общедоступная версия командлетов PowerShell для SIgnalR</span><span class="sxs-lookup"><span data-stu-id="b8d9b-560">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="b8d9b-561">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b8d9b-561">Az.Sql</span></span>
- <span data-ttu-id="b8d9b-562">Добавлены новые типы обнаружения Data_Exfiltration и Unsafe_Action в командлеты обнаружения угроз</span><span class="sxs-lookup"><span data-stu-id="b8d9b-562">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="b8d9b-563">Примеры обновленной документации для командлетов аудита Sql</span><span class="sxs-lookup"><span data-stu-id="b8d9b-563">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="b8d9b-564">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="b8d9b-564">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="b8d9b-565">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b8d9b-565">Az.Storage</span></span>
- <span data-ttu-id="b8d9b-566">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="b8d9b-566">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="b8d9b-567">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b8d9b-567">Az.Websites</span></span>
- <span data-ttu-id="b8d9b-568">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="b8d9b-568">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="b8d9b-569">0.7.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-569">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="b8d9b-570">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="b8d9b-570">General</span></span>

* <span data-ttu-id="b8d9b-571">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="b8d9b-571">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="b8d9b-572">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b8d9b-572">Az.Compute</span></span>

* <span data-ttu-id="b8d9b-573">Добавлена поддержка UltraSSD и образов коллекции в простых наборах параметров для командлетов `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-573">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="b8d9b-574">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b8d9b-574">Az.DataLakeStore</span></span>

* <span data-ttu-id="b8d9b-575">Исправлено косую черту в конце домена учетной записи ADLS</span><span class="sxs-lookup"><span data-stu-id="b8d9b-575">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="b8d9b-576">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b8d9b-576">Az.FrontDoor</span></span>

* <span data-ttu-id="b8d9b-577">Исправлены некоторые неработающие ссылки</span><span class="sxs-lookup"><span data-stu-id="b8d9b-577">Fixed some broken links</span></span>
    - <span data-ttu-id="b8d9b-578">В статьях New-AzureRmFrontDoor и Set-AzureRmFrontDoor исправлена ссылка на статью командлета New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-578">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="b8d9b-579">В статье New-AzureRmFrontDoorManagedRuleObject исправлена ссылка на статью командлета New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-579">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="b8d9b-580">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b8d9b-580">Az.RecoveryServices</span></span>

* <span data-ttu-id="b8d9b-581">Добавлены проверки на стороне клиента для операций восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-581">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="b8d9b-582">StorageAccountName и storageAccountResourceGroupName являются необязательными для восстановления afs.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-582">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="b8d9b-583">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b8d9b-583">Az.Resources</span></span>

* <span data-ttu-id="b8d9b-584">Исправление для https://github.com/Azure/azure-powershell/issues/7679.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-584">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="b8d9b-585">Обновите Get-AzureRmRoleAssignment, чтобы использовать область подписки, если она указана при запросе классических администраторов.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-585">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="b8d9b-586">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b8d9b-586">Az.Sql</span></span>

* <span data-ttu-id="b8d9b-587">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="b8d9b-587">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="b8d9b-588">Устранена проблема с использованием Get-AzureRmSqlDatabaseVulnerabilityAssessment с .NET Core.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-588">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="b8d9b-589">Изменена документация справочных сообщений, связанных с командлетами аудита SQL.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-589">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="b8d9b-590">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b8d9b-590">Az.Storage</span></span>

* <span data-ttu-id="b8d9b-591">Добавлено -EnableHierarchicalNamespace к New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b8d9b-591">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="b8d9b-592">Устранена проблема, из-за которой командлет Copy File не может повторно использовать исходный контекст в пункте назначения, если не введен -DestContext</span><span class="sxs-lookup"><span data-stu-id="b8d9b-592">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="b8d9b-593">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="b8d9b-593">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="b8d9b-594">Поддержка статической конфигурации сайта</span><span class="sxs-lookup"><span data-stu-id="b8d9b-594">Support Static Website configuration</span></span>
    - <span data-ttu-id="b8d9b-595">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="b8d9b-595">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="b8d9b-596">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="b8d9b-596">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="b8d9b-597">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b8d9b-597">Az.Websites</span></span>

* <span data-ttu-id="b8d9b-598">Set-AzureRmWebApp и Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b8d9b-598">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="b8d9b-599">Добавлен новый параметр (-AzureStoragePath), который указывает путь службы хранилища Azure для подключения в приложениях-контейнерах Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-599">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="b8d9b-600">Используйте выходные данные нового командлета New-AzureRmWebAppAzureStoragePath в качестве параметра, чтобы задать пути к службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-600">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="b8d9b-601">0.6.1 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-601">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="b8d9b-602">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b8d9b-602">Az.ApiManagement</span></span>
* <span data-ttu-id="b8d9b-603">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-603">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="b8d9b-604">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b8d9b-604">Az.Automation</span></span>
* <span data-ttu-id="b8d9b-605">Командлеты службы автоматизации Azure на базе Swagger.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-605">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="b8d9b-606">Добавлены командлеты для Управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-606">Added Update Management cmdlets</span></span>
* <span data-ttu-id="b8d9b-607">Добавлены командлеты для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-607">Added Source Control cmdlets</span></span>
* <span data-ttu-id="b8d9b-608">Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-608">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="b8d9b-609">Исправлена команда DSC для регистрации узла.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-609">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="b8d9b-610">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b8d9b-610">Az.Compute</span></span>
* <span data-ttu-id="b8d9b-611">Исправлена проблема с удостоверением, назначаемым системой.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-611">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="b8d9b-612">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-612">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="b8d9b-613">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="b8d9b-613">Az.ContainerInstance</span></span>
* <span data-ttu-id="b8d9b-614">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-614">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="b8d9b-615">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="b8d9b-615">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="b8d9b-616">Обновлено описание в примерах командлетов для Marketplace.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-616">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="b8d9b-617">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b8d9b-617">Az.Network</span></span>
* <span data-ttu-id="b8d9b-618">Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-618">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="b8d9b-619">Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-619">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="b8d9b-620">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-620">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="b8d9b-621">Исправлены проблемы с использованием памяти в карте виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-621">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="b8d9b-622">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="b8d9b-622">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="b8d9b-623">Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-623">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="b8d9b-624">Параметры часового пояса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-624">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="b8d9b-625">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="b8d9b-625">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="b8d9b-626">Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-626">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="b8d9b-627">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-627">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="b8d9b-628">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="b8d9b-628">Az.Relay</span></span>
* <span data-ttu-id="b8d9b-629">Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-629">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="b8d9b-630">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b8d9b-630">Az.Resources</span></span>
* <span data-ttu-id="b8d9b-631">Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-631">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="b8d9b-632">Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-632">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="b8d9b-633">Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-633">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="b8d9b-634">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b8d9b-634">Az.ServiceFabric</span></span>
* <span data-ttu-id="b8d9b-635">Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-635">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="b8d9b-636">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b8d9b-636">Az.Sql</span></span>
* <span data-ttu-id="b8d9b-637">Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-637">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="b8d9b-638">Get-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-638">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b8d9b-639">New-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-639">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b8d9b-640">Set-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-640">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b8d9b-641">Remove-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-641">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b8d9b-642">Get-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-642">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="b8d9b-643">New-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-643">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="b8d9b-644">Restore-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-644">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="b8d9b-645">Remove-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-645">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="b8d9b-646">Добавлено расширенное управление политиками аудита для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-646">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="b8d9b-647">Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-647">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="b8d9b-648">Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-648">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="b8d9b-649">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-649">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="b8d9b-650">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-650">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="b8d9b-651">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-651">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="b8d9b-652">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-652">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="b8d9b-653">Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-653">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="b8d9b-654">0.5.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-654">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="b8d9b-655">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="b8d9b-655">General</span></span>
* <span data-ttu-id="b8d9b-656">Добавлены средства заполнения ресурсов для многих основных командлетов — они позволяют вам переключать существующие имена ресурсов при вызове командлетов в интерактивном режиме</span><span class="sxs-lookup"><span data-stu-id="b8d9b-656">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="b8d9b-657">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="b8d9b-657">Az.Profile</span></span>
* <span data-ttu-id="b8d9b-658">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-658">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="b8d9b-659">В командлете Connect-AzAccount параметр TenantId переименован в Tenant и добавлен псевдоним для TenantId</span><span class="sxs-lookup"><span data-stu-id="b8d9b-659">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="b8d9b-660">Обновлено описание TenantId для командлета Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="b8d9b-660">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="b8d9b-661">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-661">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="b8d9b-662">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-662">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="b8d9b-663">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-663">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="b8d9b-664">Устранена проблема, при которой командлет Disconnect-AzAccount вызывал сбой при отсутствии подключения</span><span class="sxs-lookup"><span data-stu-id="b8d9b-664">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="b8d9b-665">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b8d9b-665">Az.CognitiveServices</span></span>
* <span data-ttu-id="b8d9b-666">Добавлена операция Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-666">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b8d9b-667">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b8d9b-667">Az.Compute</span></span>
* <span data-ttu-id="b8d9b-668">Добавлены командлеты Add-AzVmssVMDataDisk и Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="b8d9b-668">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="b8d9b-669">Get-AzVMImage отображает AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="b8d9b-669">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="b8d9b-670">Устранена проблема, при которой значения параметров SetAzVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-670">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b8d9b-671">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b8d9b-671">Az.DataLakeStore</span></span>
* <span data-ttu-id="b8d9b-672">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-672">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="b8d9b-673">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-673">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="b8d9b-674">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="b8d9b-674">Az.Insights</span></span>
* <span data-ttu-id="b8d9b-675">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="b8d9b-675">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="b8d9b-676">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="b8d9b-676">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="b8d9b-677">Исправлена проблема № 7513 [Insights], при которой для командлета Set-AzDiagnosticSetting требовалось явное указание категорий во время создания параметра</span><span class="sxs-lookup"><span data-stu-id="b8d9b-677">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="b8d9b-678">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-678">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b8d9b-679">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b8d9b-679">Az.Network</span></span>
* <span data-ttu-id="b8d9b-680">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="b8d9b-680">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="b8d9b-681">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="b8d9b-681">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="b8d9b-682">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="b8d9b-682">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="b8d9b-683">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="b8d9b-683">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="b8d9b-684">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="b8d9b-684">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="b8d9b-685">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="b8d9b-685">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="b8d9b-686">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="b8d9b-686">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="b8d9b-687">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b8d9b-687">Az.PolicyInsights</span></span>
* <span data-ttu-id="b8d9b-688">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-688">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="b8d9b-689">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b8d9b-689">Az.Resources</span></span>
* <span data-ttu-id="b8d9b-690">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-690">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="b8d9b-691">Разрешено перечисление ресурсов с помощью параметра -ResourceId для командлета Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="b8d9b-691">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="b8d9b-692">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b8d9b-692">Az.ServiceBus</span></span>
* <span data-ttu-id="b8d9b-693">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-693">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b8d9b-694">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b8d9b-694">Az.ServiceFabric</span></span>
* <span data-ttu-id="b8d9b-695">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-695">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="b8d9b-696">Исправлен командлет Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="b8d9b-696">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="b8d9b-697">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="b8d9b-697">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="b8d9b-698">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="b8d9b-698">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="b8d9b-699">Исправлен командлет Update-AzServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-699">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="b8d9b-700">0.4.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-700">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="b8d9b-701">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="b8d9b-701">Az.Profile</span></span>
* <span data-ttu-id="b8d9b-702">Устранена проблема с Get-AzSubscription в CloudShell</span><span class="sxs-lookup"><span data-stu-id="b8d9b-702">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="b8d9b-703">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-703">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b8d9b-704">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b8d9b-704">Az.Compute</span></span>
* <span data-ttu-id="b8d9b-705">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzVm</span><span class="sxs-lookup"><span data-stu-id="b8d9b-705">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="b8d9b-706">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-706">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b8d9b-707">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b8d9b-707">Az.DataLakeStore</span></span>
* <span data-ttu-id="b8d9b-708">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="b8d9b-708">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="b8d9b-709">Get-AzDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-709">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="b8d9b-710">Add-AzDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-710">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="b8d9b-711">Set-AzDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-711">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="b8d9b-712">Remove-AzDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-712">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b8d9b-713">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b8d9b-713">Az.Network</span></span>
* <span data-ttu-id="b8d9b-714">Обновлен командлет Test-AzNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-714">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="b8d9b-715">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-715">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b8d9b-716">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b8d9b-716">Az.Resources</span></span>
* <span data-ttu-id="b8d9b-717">Устранена проблема, из-за которой командлет Get-AzRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), благодаря добавлению понятного исключения в сценарий.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-717">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="b8d9b-718">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-718">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="b8d9b-719">0.3.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-719">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="b8d9b-720">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="b8d9b-720">Azure.Storage</span></span>
* <span data-ttu-id="b8d9b-721">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-721">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="b8d9b-722">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="b8d9b-722">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="b8d9b-723">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="b8d9b-723">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="b8d9b-724">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-724">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="b8d9b-725">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="b8d9b-725">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="b8d9b-726">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b8d9b-726">Az.CognitiveServices</span></span>
* <span data-ttu-id="b8d9b-727">Поддержка Get-AzCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-727">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b8d9b-728">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b8d9b-728">Az.Compute</span></span>
* <span data-ttu-id="b8d9b-729">Исправлена команда Get-AzVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов</span><span class="sxs-lookup"><span data-stu-id="b8d9b-729">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="b8d9b-730">Добавлен пример использования SimpleParameterSet в справку командлета New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-730">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="b8d9b-731">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-731">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="b8d9b-732">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b8d9b-732">Az.DataFactoryV2</span></span>
* <span data-ttu-id="b8d9b-733">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-733">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b8d9b-734">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b8d9b-734">Az.Network</span></span>
* <span data-ttu-id="b8d9b-735">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-735">Added NetworkProfile functionality.</span></span> <span data-ttu-id="b8d9b-736">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="b8d9b-736">new cmdlets added</span></span>
    - <span data-ttu-id="b8d9b-737">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b8d9b-737">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="b8d9b-738">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b8d9b-738">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="b8d9b-739">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b8d9b-739">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="b8d9b-740">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b8d9b-740">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="b8d9b-741">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="b8d9b-741">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="b8d9b-742">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="b8d9b-742">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="b8d9b-743">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-743">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="b8d9b-744">Добавлены командлеты: New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="b8d9b-744">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="b8d9b-745">Добавлены командлеты: Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="b8d9b-745">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="b8d9b-746">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="b8d9b-746">Az.RedisCache</span></span>
* <span data-ttu-id="b8d9b-747">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-747">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="b8d9b-748">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-748">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="b8d9b-749">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b8d9b-749">Az.Resources</span></span>
* <span data-ttu-id="b8d9b-750">Добавлен отсутствующий параметр -Mode в командлет Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b8d9b-750">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="b8d9b-751">Исправлена ошибка командлета Get-AzProviderOperation для операций, когда Origin содержит User</span><span class="sxs-lookup"><span data-stu-id="b8d9b-751">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="b8d9b-752">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b8d9b-752">Az.Sql</span></span>
* <span data-ttu-id="b8d9b-753">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-753">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b8d9b-754">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b8d9b-754">Az.Websites</span></span>
* <span data-ttu-id="b8d9b-755">Новый командлет Get-AzWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="b8d9b-755">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="b8d9b-756">Новые командлеты New-AzWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows</span><span class="sxs-lookup"><span data-stu-id="b8d9b-756">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="b8d9b-757">0.2.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-757">0.2.0 - September 2018</span></span>
 <span data-ttu-id="b8d9b-758">Первый выпуск</span><span class="sxs-lookup"><span data-stu-id="b8d9b-758">Initial Release</span></span>