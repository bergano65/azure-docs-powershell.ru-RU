---
ms.openlocfilehash: 9915ff37e59a73c1d226a216213fd9016b55d3d4
ms.sourcegitcommit: 447276d46ffeeb37f0c07a570536665e36c5ddb8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/14/2019
ms.locfileid: "57882478"
---
## <a name="150---march-2019"></a><span data-ttu-id="b8d9d-101">1.5.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-101">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b8d9d-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b8d9d-102">Az.Accounts</span></span>
* <span data-ttu-id="b8d9d-103">Добавлена команда Register-AzModule для поддержки созданных командлетов AutoRest.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-103">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="b8d9d-104">Обновлены примеры для Connect AzAccount.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-104">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b8d9d-105">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b8d9d-105">Az.Automation</span></span>
* <span data-ttu-id="b8d9d-106">Исправлена проблема с получением некоторых ежемесячных расписаний в нескольких командлетах службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-106">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="b8d9d-107">Исправлен командлет Get-AzAutomationDscNode, возвращающий только первые 20 узлов.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-107">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="b8d9d-108">Теперь он возвращает все узлы.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-108">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="b8d9d-109">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b8d9d-109">Az.Cdn</span></span>
* <span data-ttu-id="b8d9d-110">Добавлены новые командлеты PowerShell для включения и отключения HTTPS для личного домена и отключены устаревшие командлеты.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-110">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b8d9d-111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b8d9d-111">Az.Compute</span></span>
* <span data-ttu-id="b8d9d-112">Добавлена поддержка подстановочных знаков в командлетах Get.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-112">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b8d9d-113">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b8d9d-113">Az.DataFactory</span></span>
* <span data-ttu-id="b8d9d-114">Обновлен пакет SDK для ADF .NET до версии 3.0.1.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-114">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="b8d9d-115">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b8d9d-115">Az.LogicApp</span></span>
* <span data-ttu-id="b8d9d-116">Исправлена проблема с получением только первой страницы результатов при выполнении команды ListWorkflows.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-116">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b8d9d-117">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b8d9d-117">Az.Network</span></span>
* <span data-ttu-id="b8d9d-118">Добавлена поддержка подстановочных знаков в командлетах Network.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-118">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b8d9d-119">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b8d9d-119">Az.RecoveryServices</span></span>
* <span data-ttu-id="b8d9d-120">Добавлена поддержка SQL Server на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-120">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="b8d9d-121">Обновление пакета SDK</span><span class="sxs-lookup"><span data-stu-id="b8d9d-121">SDK Update</span></span>
* <span data-ttu-id="b8d9d-122">Удалена проверка VMappContainer в Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-122">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="b8d9d-123">Добавлены параметры Name и ServerName для Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-123">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="b8d9d-124">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b8d9d-124">Az.Resources</span></span>
* <span data-ttu-id="b8d9d-125">Добавлен параметр `-TemplateObject` в командлеты для развертывания.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-125">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="b8d9d-126">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2933.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-126">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="b8d9d-127">Устранена проблема с передачей в конвейер результата `Get-AzResource` для `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-127">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="b8d9d-128">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8240.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-128">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="b8d9d-129">Устранена проблема с изменением типа данных JSON при выполнении `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-129">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="b8d9d-130">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7930.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-130">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="b8d9d-131">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b8d9d-131">Az.Sql</span></span>
* <span data-ttu-id="b8d9d-132">Обновление AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-132">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="b8d9d-133">Исправлено поведение для пограничного случая при создании параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-133">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b8d9d-134">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b8d9d-134">Az.Storage</span></span>
* <span data-ttu-id="b8d9d-135">Включена поддержка Kind BlockBlobStorage при создании учетной записи хранения для New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-135">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="b8d9d-136">1.4.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-136">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="b8d9d-137">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b8d9d-137">Az.AnalysisServices</span></span>
* <span data-ttu-id="b8d9d-138">Командлет AddAzureASAccount устарел.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-138">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b8d9d-139">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b8d9d-139">Az.Automation</span></span>
* <span data-ttu-id="b8d9d-140">Обновлена справка для командлета Import-AzAutomationDscNodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-140">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="b8d9d-141">Добавлена проверка имени конфигурации для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-141">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="b8d9d-142">Улучшена обработка ошибок для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-142">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="b8d9d-143">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b8d9d-143">Az.CognitiveServices</span></span>
* <span data-ttu-id="b8d9d-144">Добавлен параметр CustomSubdomainName — новый необязательный параметр для командлета New-AzCognitiveServicesAccount, который указывает поддомен для ресурса.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-144">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b8d9d-145">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b8d9d-145">Az.Compute</span></span>
* <span data-ttu-id="b8d9d-146">Устранена проблема с идентификаторами наборов параметров.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-146">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="b8d9d-147">Обновлен командлет Get-AzVMExtension для отображения списка всех установленных расширений, если не указан параметр Name.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-147">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="b8d9d-148">Для командлета Update-AzImage добавлены параметры Tag и ResourceId.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-148">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="b8d9d-149">Командлет Get-AzVmssVM, который выполняется без указания идентификатора экземпляра и с параметром InstanceView, может выводить виртуальные машины из VMSS с представлением экземпляра.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-149">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b8d9d-150">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b8d9d-150">Az.DataLakeStore</span></span>
* <span data-ttu-id="b8d9d-151">Добавлены командлеты для перечисления и восстановления удаленного элемента ADL.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-151">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="b8d9d-152">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b8d9d-152">Az.EventHub</span></span>
* <span data-ttu-id="b8d9d-153">Добавлено новое логическое свойство SkipEmptyArchives для пропуска пустых архивов в классе CaptureDescription Eventhub.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-153">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="b8d9d-154">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b8d9d-154">Az.KeyVault</span></span>
* <span data-ttu-id="b8d9d-155">Исправлена расстановка тегов для командлета Set-AzKeyVaultSecret.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-155">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="b8d9d-156">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b8d9d-156">Az.LogicApp</span></span>
* <span data-ttu-id="b8d9d-157">Добавлен SKU "Базовый" для учетных записей интеграции.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-157">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="b8d9d-158">Добавлены типы сопоставлений Liquid, а также XSLT 2.0 и XSLT 3.0.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-158">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="b8d9d-159">Новые командлеты для сборок учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="b8d9d-159">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="b8d9d-160">Get-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="b8d9d-160">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="b8d9d-161">New-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="b8d9d-161">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="b8d9d-162">Remove-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="b8d9d-162">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="b8d9d-163">Set-AzIntegrationAccountAssembly.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-163">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="b8d9d-164">Новые командлеты для конфигурации пакета учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="b8d9d-164">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="b8d9d-165">Get-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="b8d9d-165">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="b8d9d-166">New-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="b8d9d-166">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="b8d9d-167">Remove-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="b8d9d-167">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="b8d9d-168">Set-AzIntegrationAccountBatchConfiguration.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-168">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="b8d9d-169">Обновлен пакет SDK Logic Apps до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-169">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b8d9d-170">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b8d9d-170">Az.Monitor</span></span>
* <span data-ttu-id="b8d9d-171">Обновлена справка для командлета Get-AzMetric.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-171">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b8d9d-172">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b8d9d-172">Az.Network</span></span>
* <span data-ttu-id="b8d9d-173">Обновлен пример справки для командлета Add-AzApplicationGatewayCustomError.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-173">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b8d9d-174">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b8d9d-174">Az.OperationalInsights</span></span>
* <span data-ttu-id="b8d9d-175">Дополнительная поддержка создания и получения источников данных ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-175">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="b8d9d-176">Добавлен новый тип ApplicationInsights для получения определенных или всех источников данных ApplicationInsights для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-176">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="b8d9d-177">Добавлен командлет New-AzOperationalInsightsApplicationInsightsDataSource для создания источника данных с использованием параметров указанного ресурса Application-Insightss: subscription Id, resourceGroupName и name.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-177">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="b8d9d-178">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b8d9d-178">Az.Resources</span></span>
* <span data-ttu-id="b8d9d-179">исправлена проблема https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-179">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="b8d9d-180">исправлена проблема https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-180">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="b8d9d-181">исправлена проблема https://github.com/Azure/azure-powershell/issues/6219.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-181">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="b8d9d-182">Исправлена ошибка, препятствующая повторному созданию KeyCredentials.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-182">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="b8d9d-183">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b8d9d-183">Az.Sql</span></span>
* <span data-ttu-id="b8d9d-184">Добавлена поддержка уровня гипермасштабирования в базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-184">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="b8d9d-185">Исправлена ошибка, из-за которой восстановление могло завершиться со сбоем при указании ненужных свойств в запросе на восстановление.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-185">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b8d9d-186">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b8d9d-186">Az.Websites</span></span>
* <span data-ttu-id="b8d9d-187">Исправлен пример для командлета Get-AzWebAppSlotMetrics.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-187">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="b8d9d-188">1.3.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-188">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b8d9d-189">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b8d9d-189">Az.Accounts</span></span>
* <span data-ttu-id="b8d9d-190">Обновление до последней версии ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="b8d9d-190">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="b8d9d-191">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b8d9d-191">Az.AnalysisServices</span></span>
<span data-ttu-id="b8d9d-192">Общедоступная версия модуля Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-192">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b8d9d-193">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b8d9d-193">Az.Compute</span></span>
* <span data-ttu-id="b8d9d-194">Расширение AEM: добавлена поддержка дисков UltraSSD, P60, P70 и P80.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-194">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="b8d9d-195">Обновлено описание справки для командлета Set-AzVMBootDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-195">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="b8d9d-196">Обновлено описание справки и пример для командлета Update-AzImage.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-196">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b8d9d-197">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b8d9d-197">Az.RecoveryServices</span></span>
<span data-ttu-id="b8d9d-198">Общедоступная версия модуля Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-198">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b8d9d-199">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b8d9d-199">Az.Resources</span></span>
* <span data-ttu-id="b8d9d-200">Исправлена расстановка тегов для групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-200">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="b8d9d-201">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-201">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="b8d9d-202">Исправлена проблема с игнорированием командлетом `Get-AzureRmRoleAssignment` параметра -ErrorAction.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-202">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="b8d9d-203">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-203">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="b8d9d-204">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b8d9d-204">Az.Sql</span></span>
* <span data-ttu-id="b8d9d-205">Добавлен командлет Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-205">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="b8d9d-206">Исправлена проблема с появлением исключения NullRef при выполнении командлетов SQL, если не выполнен вход в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-206">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="b8d9d-207">Исправлено исключение NullRef в командлете Get-AzSqlCapability.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-207">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="b8d9d-208">1.2.1 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-208">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b8d9d-209">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b8d9d-209">Az.Accounts</span></span>
* <span data-ttu-id="b8d9d-210">Выпуск с правильной версией службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-210">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="b8d9d-211">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b8d9d-211">Az.AnalysisServices</span></span>
* <span data-ttu-id="b8d9d-212">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-212">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b8d9d-213">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b8d9d-213">Az.RecoveryServices</span></span>
* <span data-ttu-id="b8d9d-214">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-214">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="b8d9d-215">1.2.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-215">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b8d9d-216">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b8d9d-216">Az.Accounts</span></span>
* <span data-ttu-id="b8d9d-217">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-217">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="b8d9d-218">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-218">Update incorrect online help URLs</span></span>
* <span data-ttu-id="b8d9d-219">Добавлено предупреждающее сообщение в PS Core для модуля Uninstall-AzureRm.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-219">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="b8d9d-220">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="b8d9d-220">Az.Aks</span></span>
* <span data-ttu-id="b8d9d-221">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-221">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b8d9d-222">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b8d9d-222">Az.Automation</span></span>
* <span data-ttu-id="b8d9d-223">Добавлена поддержка для модулей runbook Python 2.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-223">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="b8d9d-224">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-224">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="b8d9d-225">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b8d9d-225">Az.Cdn</span></span>
* <span data-ttu-id="b8d9d-226">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-226">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b8d9d-227">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b8d9d-227">Az.Compute</span></span>
* <span data-ttu-id="b8d9d-228">Добавлен командлет Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-228">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="b8d9d-229">Добавлен параметр TempDisk к командлету Set-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-229">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="b8d9d-230">Исправлено предупреждающее сообщение командлета New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-230">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="b8d9d-231">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b8d9d-231">Az.ContainerRegistry</span></span>
* <span data-ttu-id="b8d9d-232">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-232">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b8d9d-233">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b8d9d-233">Az.DataFactory</span></span>
* <span data-ttu-id="b8d9d-234">Пакет SDK ADF .Net обновлен до версии 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-234">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b8d9d-235">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b8d9d-235">Az.DataLakeStore</span></span>
* <span data-ttu-id="b8d9d-236">Исправлена проблема с конечной точкой ADLS при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-236">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="b8d9d-237">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7462.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-237">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="b8d9d-238">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-238">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b8d9d-239">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b8d9d-239">Az.IotHub</span></span>
* <span data-ttu-id="b8d9d-240">Добавлен формат кодирования для командлета Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-240">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b8d9d-241">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b8d9d-241">Az.KeyVault</span></span>
* <span data-ttu-id="b8d9d-242">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-242">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b8d9d-243">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b8d9d-243">Az.Network</span></span>
* <span data-ttu-id="b8d9d-244">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-244">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="b8d9d-245">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b8d9d-245">Az.Resources</span></span>
* <span data-ttu-id="b8d9d-246">Исправлены неправильные примеры в справочной документации по командлетам New-AzADAppCredential и New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-246">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="b8d9d-247">Исправлена проблема, при которой путь для параметра -TemplateFile не удавалось разрешить до выполнения командлетов развертывания групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-247">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="b8d9d-248">Az.Resources: исправлена документация для значения по умолчанию -Mode командлета New-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-248">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="b8d9d-249">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/7522.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-249">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="b8d9d-250">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/5747.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-250">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="b8d9d-251">Исправлена проблема с форматированием объекта PSResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-251">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="b8d9d-252">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2123.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-252">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b8d9d-253">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b8d9d-253">Az.ServiceFabric</span></span>
* <span data-ttu-id="b8d9d-254">Исправлена проблема с появлением исключения в процессе отката при добавлении сертификата к модели VMSS: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-254">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="b8d9d-255">Исправлены некоторые сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-255">Fix some error messages.</span></span>
* <span data-ttu-id="b8d9d-256">Исправлена проблема с созданием кластера с шаблоном ARM по умолчанию для командлета New-AzServiceFabriCluster, который не работал с операцией миграции в Az.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-256">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="b8d9d-257">Исправлена проблема с добавлением сертификата кластера или приложения: теперь они добавляются только в Масштабируемые наборы виртуальных машин, которые сопоставлены с кластером, путем проверки идентификатора кластера в расширении.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-257">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="b8d9d-258">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="b8d9d-258">Az.SignalR</span></span>
* <span data-ttu-id="b8d9d-259">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-259">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="b8d9d-260">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b8d9d-260">Az.Sql</span></span>
* <span data-ttu-id="b8d9d-261">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-261">Update incorrect online help URLs</span></span>
* <span data-ttu-id="b8d9d-262">Обновлено описание параметра LicenseType с добавлением возможных значений.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-262">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="b8d9d-263">Исправлена проблема с неправильным обновлением удостоверения управляемого экземпляра, если оно было единственным обновляемым свойством.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-263">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="b8d9d-264">Поддержка пользовательских параметров сортировки в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-264">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b8d9d-265">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b8d9d-265">Az.Storage</span></span>
* <span data-ttu-id="b8d9d-266">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-266">Update incorrect online help URLs</span></span>
* <span data-ttu-id="b8d9d-267">Добавлен вывод подробных сообщений об ошибке при получении или установке классических свойств ведения журнала или метрик в учетной записи хранилища класса Premium, так как учетная запись хранилища класса Premium не поддерживает классические функции ведения журнала и метрик.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-267">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="b8d9d-268">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="b8d9d-268">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="b8d9d-269">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="b8d9d-269">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="b8d9d-270">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="b8d9d-270">Az.TrafficManager</span></span>
* <span data-ttu-id="b8d9d-271">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-271">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b8d9d-272">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b8d9d-272">Az.Websites</span></span>
* <span data-ttu-id="b8d9d-273">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-273">Update incorrect online help URLs</span></span>
* <span data-ttu-id="b8d9d-274">Исправлена работа командлета New-AzWebAppSSLBinding: сертификат отправляется в правильную группу ресурсов и правильное расположение, если приложение размещено в ASE.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-274">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="b8d9d-275">Исправлена работа командлета New-AzWebAppSSLBinding: теги не перезаписываются при привязке SSL-сертификата к приложению.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-275">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="b8d9d-276">1.1.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-276">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b8d9d-277">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b8d9d-277">Az.Accounts</span></span>
* <span data-ttu-id="b8d9d-278">Добавление области "Local" в Enable-AzureRmAlias.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-278">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b8d9d-279">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b8d9d-279">Az.Compute</span></span>
* <span data-ttu-id="b8d9d-280">Теперь имя не является обязательным в идентификаторе набора параметров для Restart/Start/Stop/Remove/Set-AzVM и Save-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-280">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="b8d9d-281">Обновлено описание идентификатора в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-281">Updated the description of ID in help files</span></span>
* <span data-ttu-id="b8d9d-282">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-282">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b8d9d-283">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b8d9d-283">Az.DataLakeStore</span></span>
* <span data-ttu-id="b8d9d-284">Обновление версии пакета SDK для плоскости данных до 1.1.14 для устранения найденных проблем.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-284">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="b8d9d-285">Исправлена обработка отрицательного времени доступа и времени изменения для getfilestatus и liststatus, исправлен токен отмены для асинхронных методов.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-285">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="b8d9d-286">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="b8d9d-286">Az.EventGrid</span></span>
* <span data-ttu-id="b8d9d-287">Обновление для использования API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-287">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="b8d9d-288">Обновлены указанные ниже командлеты для поддержки нового сценария в API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-288">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="b8d9d-289">New-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="b8d9d-289">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="b8d9d-290">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="b8d9d-290">Event Time-To-Live,</span></span>
        - <span data-ttu-id="b8d9d-291">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="b8d9d-291">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="b8d9d-292">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-292">Dead letter endpoint.</span></span>
    - <span data-ttu-id="b8d9d-293">Update-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="b8d9d-293">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="b8d9d-294">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="b8d9d-294">Event Time-To-Live,</span></span>
        - <span data-ttu-id="b8d9d-295">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="b8d9d-295">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="b8d9d-296">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-296">Dead letter endpoint.</span></span>
* <span data-ttu-id="b8d9d-297">Для параметра EndpointType добавлены новые значения перечисления (storageQueue и hybridConnection) в командлеты New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-297">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="b8d9d-298">Если ожидается, что создание или обновление подписки на событие повлечет за собой действия со стороны пользователя, выполняемые вручную, отображается предупреждение при создании или обновлении подписки события.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-298">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b8d9d-299">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b8d9d-299">Az.IotHub</span></span>
* <span data-ttu-id="b8d9d-300">Пакет SDK Центра Интернета вещей обновлен до последней версии.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-300">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="b8d9d-301">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b8d9d-301">Az.LogicApp</span></span>
* <span data-ttu-id="b8d9d-302">Get-AzLogicApp позволяет перечислить все параметры без указанного имени.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-302">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="b8d9d-303">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b8d9d-303">Az.Resources</span></span>
* <span data-ttu-id="b8d9d-304">Исправлена проблема с набором параметров при предоставлении параметров "-ODataQuery" и "-ResourceId" для "Get-AzResource".</span><span class="sxs-lookup"><span data-stu-id="b8d9d-304">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="b8d9d-305">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7875.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-305">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="b8d9d-306">Исправлена обработка параметра -Custom в New/Set-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-306">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="b8d9d-307">Исправлена опечатка в документации по New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-307">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="b8d9d-308">Параметр "-MailNickname" стал обязательным для "New-AzADUser".</span><span class="sxs-lookup"><span data-stu-id="b8d9d-308">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="b8d9d-309">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8220.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-309">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="b8d9d-310">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="b8d9d-310">Az.SignalR</span></span>
* <span data-ttu-id="b8d9d-311">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-311">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="b8d9d-312">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b8d9d-312">Az.Sql</span></span>
* <span data-ttu-id="b8d9d-313">Зависимость клиента управления хранением преобразована для общей реализации в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-313">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b8d9d-314">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b8d9d-314">Az.Storage</span></span>
* <span data-ttu-id="b8d9d-315">Установка параметра StorageAccountName для контекста хранилища в качестве реального имени учетной записи хранения, если она была создана с использованием токена Sas, OAuth или анонимного доступа.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-315">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="b8d9d-316">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="b8d9d-316">New-AzStorageContext</span></span>
* <span data-ttu-id="b8d9d-317">Создание токена Sas большого двоичного объекта моментального снимка с параметром "-FullUri". Возвращаемый URI исправлен на URI моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-317">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="b8d9d-318">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="b8d9d-318">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b8d9d-319">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b8d9d-319">Az.Websites</span></span>
* <span data-ttu-id="b8d9d-320">Исправлена ошибка синтаксического анализа даты в "Get-AzDeletedWebApp".</span><span class="sxs-lookup"><span data-stu-id="b8d9d-320">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="b8d9d-321">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-321">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="b8d9d-322">1.0.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-322">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="b8d9d-323">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="b8d9d-323">General</span></span>

- <span data-ttu-id="b8d9d-324">Общедоступная версия модуля Az.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-324">General Availability of Az Module</span></span>
- <span data-ttu-id="b8d9d-325">Справка в Интернете для каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-325">Online help for each module</span></span>
- <span data-ttu-id="b8d9d-326">Дополнительные сведения и стратегию развития см. в статье [Announcing New Module 'Az'](https://aka.ms/azps-announce) (Объявление о новом модуле Az)</span><span class="sxs-lookup"><span data-stu-id="b8d9d-326">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="b8d9d-327">Сведения о миграции с AzureRM см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="b8d9d-327">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="b8d9d-328">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b8d9d-328">Az.Accounts</span></span>
- <span data-ttu-id="b8d9d-329">Изменено с Az.Profile.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-329">Changed from Az.Profile</span></span>
- <span data-ttu-id="b8d9d-330">Исправлены форматы таблиц для типов профиля и контекста.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-330">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="b8d9d-331">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b8d9d-331">Az.ApiManagement</span></span>
- <span data-ttu-id="b8d9d-332">Исправления для #7002.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-332">Fixes for #7002</span></span>
- <span data-ttu-id="b8d9d-333">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="b8d9d-333">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="b8d9d-334">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="b8d9d-334">Az.Batch</span></span>
- <span data-ttu-id="b8d9d-335">Добавлена возможность видеть, какая версия агента узла пакетной службы Azure работает в пуле на каждой виртуальной машине, с помощью нового свойства `NodeAgentInformation` в `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-335">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="b8d9d-336">Значение `Caching` по умолчанию для `PSDataDisk` теперь `ReadWrite` вместо `None`.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-336">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="b8d9d-337">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="b8d9d-337">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="b8d9d-338">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="b8d9d-338">Az.Billing</span></span>
- <span data-ttu-id="b8d9d-339">Объединены командлеты Billing, Consumption и UsageAggregates. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0).</span><span class="sxs-lookup"><span data-stu-id="b8d9d-339">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="b8d9d-340">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="b8d9d-340">Az.CognitivServices</span></span>
- <span data-ttu-id="b8d9d-341">Добавлены средства заполнения для SkuName и Typem, доступные в операции New-AzureRmCognitiveServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-341">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="b8d9d-342">Удален набор параметров GetSkusWithAccountParamSetName из Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-342">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="b8d9d-343">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="b8d9d-343">Az.ContainerInstance</span></span>
- <span data-ttu-id="b8d9d-344">Добавлена поддержка ManagedIdentity.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-344">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="b8d9d-345">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="b8d9d-345">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="b8d9d-346">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="b8d9d-346">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="b8d9d-347">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b8d9d-347">Az.DataLakeStore</span></span>
- <span data-ttu-id="b8d9d-348">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="b8d9d-348">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="b8d9d-349">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b8d9d-349">Az.Monitor</span></span>
- <span data-ttu-id="b8d9d-350">"Az.Insights" переименован в "Az.Monitor" и внесены другие незначительные критические изменения. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="b8d9d-350">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="b8d9d-351">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b8d9d-351">Az.KeyVault</span></span>
- <span data-ttu-id="b8d9d-352">Из типов вывода удалено устаревшее свойство PurgeDisabled</span><span class="sxs-lookup"><span data-stu-id="b8d9d-352">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="b8d9d-353">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="b8d9d-353">Az.MachineLearning</span></span>
- <span data-ttu-id="b8d9d-354">Включены командлеты из модуля Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="b8d9d-354">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="b8d9d-355">Az.Media</span><span class="sxs-lookup"><span data-stu-id="b8d9d-355">Az.Media</span></span>
- <span data-ttu-id="b8d9d-356">Удаляет устаревший псевдоним Tags из New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="b8d9d-356">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="b8d9d-357">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b8d9d-357">Az.Network</span></span>
<span data-ttu-id="b8d9d-358">В шлюз приложений добавлена поддержка настройки RewriteRuleSets</span><span class="sxs-lookup"><span data-stu-id="b8d9d-358">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="b8d9d-359">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="b8d9d-359">New cmdlets added:</span></span>
        - <span data-ttu-id="b8d9d-360">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b8d9d-360">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b8d9d-361">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b8d9d-361">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b8d9d-362">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b8d9d-362">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b8d9d-363">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b8d9d-363">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b8d9d-364">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b8d9d-364">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b8d9d-365">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="b8d9d-365">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="b8d9d-366">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="b8d9d-366">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="b8d9d-367">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="b8d9d-367">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="b8d9d-368">В следующие командлеты добавлен необязательный параметр -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b8d9d-368">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="b8d9d-369">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b8d9d-369">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="b8d9d-370">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b8d9d-370">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="b8d9d-371">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b8d9d-371">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="b8d9d-372">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b8d9d-372">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="b8d9d-373">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="b8d9d-373">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="b8d9d-374">New-AzureRmApplicationGatewayUrlPathMapConfig добавил с помощью идентификатора поддержку KeyVault для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-374">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="b8d9d-375">В следующие командлеты добавлен необязательный параметр -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b8d9d-375">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="b8d9d-376">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b8d9d-376">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="b8d9d-377">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b8d9d-377">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="b8d9d-378">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b8d9d-378">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="b8d9d-379">В командлет New-AzApplicationGateway добавлен необязательный параметр -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="b8d9d-379">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="b8d9d-380">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="b8d9d-380">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="b8d9d-381">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b8d9d-381">Az.OperationalInsights</span></span>
- <span data-ttu-id="b8d9d-382">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="b8d9d-382">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="b8d9d-383">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="b8d9d-383">Az.Profile</span></span>
- <span data-ttu-id="b8d9d-384">Имя модуля изменено на Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-384">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="b8d9d-385">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b8d9d-385">Az.RecoveryServices</span></span>
- <span data-ttu-id="b8d9d-386">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="b8d9d-386">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="b8d9d-387">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b8d9d-387">Az.Resources</span></span>
- <span data-ttu-id="b8d9d-388">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="b8d9d-388">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="b8d9d-389">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b8d9d-389">Az.ServiceFabric</span></span>
- <span data-ttu-id="b8d9d-390">Поддержка спецификации сертификата по общему имени и отпечатку</span><span class="sxs-lookup"><span data-stu-id="b8d9d-390">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="b8d9d-391">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="b8d9d-391">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="b8d9d-392">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="b8d9d-392">Az.SIgnalR</span></span>
- <span data-ttu-id="b8d9d-393">Общедоступная версия командлетов PowerShell для SIgnalR</span><span class="sxs-lookup"><span data-stu-id="b8d9d-393">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="b8d9d-394">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b8d9d-394">Az.Sql</span></span>
- <span data-ttu-id="b8d9d-395">Добавлены новые типы обнаружения Data_Exfiltration и Unsafe_Action в командлеты обнаружения угроз</span><span class="sxs-lookup"><span data-stu-id="b8d9d-395">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="b8d9d-396">Примеры обновленной документации для командлетов аудита Sql</span><span class="sxs-lookup"><span data-stu-id="b8d9d-396">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="b8d9d-397">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="b8d9d-397">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="b8d9d-398">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b8d9d-398">Az.Storage</span></span>
- <span data-ttu-id="b8d9d-399">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="b8d9d-399">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="b8d9d-400">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b8d9d-400">Az.Websites</span></span>
- <span data-ttu-id="b8d9d-401">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="b8d9d-401">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="b8d9d-402">0.7.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-402">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="b8d9d-403">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="b8d9d-403">General</span></span>

* <span data-ttu-id="b8d9d-404">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="b8d9d-404">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="b8d9d-405">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b8d9d-405">Az.Compute</span></span>

* <span data-ttu-id="b8d9d-406">Добавлена поддержка UltraSSD и образов коллекции в простых наборах параметров для командлетов `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-406">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="b8d9d-407">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b8d9d-407">Az.DataLakeStore</span></span>

* <span data-ttu-id="b8d9d-408">Исправлено косую черту в конце домена учетной записи ADLS</span><span class="sxs-lookup"><span data-stu-id="b8d9d-408">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="b8d9d-409">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b8d9d-409">Az.FrontDoor</span></span>

* <span data-ttu-id="b8d9d-410">Исправлены некоторые неработающие ссылки</span><span class="sxs-lookup"><span data-stu-id="b8d9d-410">Fixed some broken links</span></span>
    - <span data-ttu-id="b8d9d-411">В статьях New-AzureRmFrontDoor и Set-AzureRmFrontDoor исправлена ссылка на статью командлета New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-411">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="b8d9d-412">В статье New-AzureRmFrontDoorManagedRuleObject исправлена ссылка на статью командлета New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-412">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="b8d9d-413">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b8d9d-413">Az.RecoveryServices</span></span>

* <span data-ttu-id="b8d9d-414">Добавлены проверки на стороне клиента для операций восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-414">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="b8d9d-415">StorageAccountName и storageAccountResourceGroupName являются необязательными для восстановления afs.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-415">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="b8d9d-416">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b8d9d-416">Az.Resources</span></span>

* <span data-ttu-id="b8d9d-417">Исправление для https://github.com/Azure/azure-powershell/issues/7679.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-417">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="b8d9d-418">Обновите Get-AzureRmRoleAssignment, чтобы использовать область подписки, если она указана при запросе классических администраторов.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-418">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="b8d9d-419">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b8d9d-419">Az.Sql</span></span>

* <span data-ttu-id="b8d9d-420">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="b8d9d-420">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="b8d9d-421">Устранена проблема с использованием Get-AzureRmSqlDatabaseVulnerabilityAssessment с .NET Core.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-421">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="b8d9d-422">Изменена документация справочных сообщений, связанных с командлетами аудита SQL.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-422">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="b8d9d-423">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b8d9d-423">Az.Storage</span></span>

* <span data-ttu-id="b8d9d-424">Добавлено -EnableHierarchicalNamespace к New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b8d9d-424">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="b8d9d-425">Устранена проблема, из-за которой командлет Copy File не может повторно использовать исходный контекст в пункте назначения, если не введен -DestContext</span><span class="sxs-lookup"><span data-stu-id="b8d9d-425">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="b8d9d-426">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="b8d9d-426">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="b8d9d-427">Поддержка статической конфигурации сайта</span><span class="sxs-lookup"><span data-stu-id="b8d9d-427">Support Static Website configuration</span></span>
    - <span data-ttu-id="b8d9d-428">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="b8d9d-428">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="b8d9d-429">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="b8d9d-429">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="b8d9d-430">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b8d9d-430">Az.Websites</span></span>

* <span data-ttu-id="b8d9d-431">Set-AzureRmWebApp и Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b8d9d-431">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="b8d9d-432">Добавлен новый параметр (-AzureStoragePath), который указывает путь службы хранилища Azure для подключения в приложениях-контейнерах Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-432">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="b8d9d-433">Используйте выходные данные нового командлета New-AzureRmWebAppAzureStoragePath в качестве параметра, чтобы задать пути к службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-433">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="b8d9d-434">0.6.1 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-434">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="b8d9d-435">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b8d9d-435">Az.ApiManagement</span></span>
* <span data-ttu-id="b8d9d-436">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-436">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="b8d9d-437">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b8d9d-437">Az.Automation</span></span>
* <span data-ttu-id="b8d9d-438">Командлеты службы автоматизации Azure на базе Swagger.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-438">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="b8d9d-439">Добавлены командлеты для Управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-439">Added Update Management cmdlets</span></span>
* <span data-ttu-id="b8d9d-440">Добавлены командлеты для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-440">Added Source Control cmdlets</span></span>
* <span data-ttu-id="b8d9d-441">Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-441">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="b8d9d-442">Исправлена команда DSC для регистрации узла.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-442">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="b8d9d-443">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b8d9d-443">Az.Compute</span></span>
* <span data-ttu-id="b8d9d-444">Исправлена проблема с удостоверением, назначаемым системой.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-444">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="b8d9d-445">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-445">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="b8d9d-446">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="b8d9d-446">Az.ContainerInstance</span></span>
* <span data-ttu-id="b8d9d-447">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-447">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="b8d9d-448">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="b8d9d-448">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="b8d9d-449">Обновлено описание в примерах командлетов для Marketplace.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-449">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="b8d9d-450">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b8d9d-450">Az.Network</span></span>
* <span data-ttu-id="b8d9d-451">Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-451">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="b8d9d-452">Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-452">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="b8d9d-453">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-453">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="b8d9d-454">Исправлены проблемы с использованием памяти в карте виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-454">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="b8d9d-455">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="b8d9d-455">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="b8d9d-456">Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-456">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="b8d9d-457">Параметры часового пояса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-457">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="b8d9d-458">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="b8d9d-458">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="b8d9d-459">Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-459">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="b8d9d-460">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-460">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="b8d9d-461">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="b8d9d-461">Az.Relay</span></span>
* <span data-ttu-id="b8d9d-462">Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-462">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="b8d9d-463">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b8d9d-463">Az.Resources</span></span>
* <span data-ttu-id="b8d9d-464">Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-464">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="b8d9d-465">Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-465">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="b8d9d-466">Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-466">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="b8d9d-467">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b8d9d-467">Az.ServiceFabric</span></span>
* <span data-ttu-id="b8d9d-468">Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-468">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="b8d9d-469">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b8d9d-469">Az.Sql</span></span>
* <span data-ttu-id="b8d9d-470">Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-470">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="b8d9d-471">Get-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-471">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b8d9d-472">New-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-472">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b8d9d-473">Set-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-473">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b8d9d-474">Remove-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-474">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b8d9d-475">Get-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-475">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="b8d9d-476">New-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-476">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="b8d9d-477">Restore-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-477">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="b8d9d-478">Remove-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-478">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="b8d9d-479">Добавлено расширенное управление политиками аудита для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-479">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="b8d9d-480">Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-480">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="b8d9d-481">Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-481">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="b8d9d-482">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-482">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="b8d9d-483">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-483">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="b8d9d-484">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-484">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="b8d9d-485">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-485">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="b8d9d-486">Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-486">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="b8d9d-487">0.5.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-487">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="b8d9d-488">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="b8d9d-488">General</span></span>
* <span data-ttu-id="b8d9d-489">Добавлены средства заполнения ресурсов для многих основных командлетов — они позволяют вам переключать существующие имена ресурсов при вызове командлетов в интерактивном режиме</span><span class="sxs-lookup"><span data-stu-id="b8d9d-489">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="b8d9d-490">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="b8d9d-490">Az.Profile</span></span>
* <span data-ttu-id="b8d9d-491">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-491">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="b8d9d-492">В командлете Connect-AzAccount параметр TenantId переименован в Tenant и добавлен псевдоним для TenantId</span><span class="sxs-lookup"><span data-stu-id="b8d9d-492">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="b8d9d-493">Обновлено описание TenantId для командлета Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="b8d9d-493">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="b8d9d-494">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-494">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="b8d9d-495">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-495">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="b8d9d-496">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-496">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="b8d9d-497">Устранена проблема, при которой командлет Disconnect-AzAccount вызывал сбой при отсутствии подключения</span><span class="sxs-lookup"><span data-stu-id="b8d9d-497">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="b8d9d-498">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b8d9d-498">Az.CognitiveServices</span></span>
* <span data-ttu-id="b8d9d-499">Добавлена операция Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-499">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b8d9d-500">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b8d9d-500">Az.Compute</span></span>
* <span data-ttu-id="b8d9d-501">Добавлены командлеты Add-AzVmssVMDataDisk и Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="b8d9d-501">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="b8d9d-502">Get-AzVMImage отображает AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="b8d9d-502">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="b8d9d-503">Устранена проблема, при которой значения параметров SetAzVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-503">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b8d9d-504">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b8d9d-504">Az.DataLakeStore</span></span>
* <span data-ttu-id="b8d9d-505">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-505">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="b8d9d-506">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-506">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="b8d9d-507">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="b8d9d-507">Az.Insights</span></span>
* <span data-ttu-id="b8d9d-508">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="b8d9d-508">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="b8d9d-509">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="b8d9d-509">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="b8d9d-510">Исправлена проблема № 7513 [Insights], при которой для командлета Set-AzDiagnosticSetting требовалось явное указание категорий во время создания параметра</span><span class="sxs-lookup"><span data-stu-id="b8d9d-510">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="b8d9d-511">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-511">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b8d9d-512">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b8d9d-512">Az.Network</span></span>
* <span data-ttu-id="b8d9d-513">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="b8d9d-513">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="b8d9d-514">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="b8d9d-514">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="b8d9d-515">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="b8d9d-515">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="b8d9d-516">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="b8d9d-516">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="b8d9d-517">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="b8d9d-517">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="b8d9d-518">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="b8d9d-518">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="b8d9d-519">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="b8d9d-519">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="b8d9d-520">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b8d9d-520">Az.PolicyInsights</span></span>
* <span data-ttu-id="b8d9d-521">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-521">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="b8d9d-522">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b8d9d-522">Az.Resources</span></span>
* <span data-ttu-id="b8d9d-523">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-523">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="b8d9d-524">Разрешено перечисление ресурсов с помощью параметра -ResourceId для командлета Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="b8d9d-524">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="b8d9d-525">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b8d9d-525">Az.ServiceBus</span></span>
* <span data-ttu-id="b8d9d-526">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-526">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b8d9d-527">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b8d9d-527">Az.ServiceFabric</span></span>
* <span data-ttu-id="b8d9d-528">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-528">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="b8d9d-529">Исправлен командлет Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="b8d9d-529">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="b8d9d-530">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="b8d9d-530">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="b8d9d-531">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="b8d9d-531">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="b8d9d-532">Исправлен командлет Update-AzServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-532">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="b8d9d-533">0.4.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-533">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="b8d9d-534">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="b8d9d-534">Az.Profile</span></span>
* <span data-ttu-id="b8d9d-535">Устранена проблема с Get-AzSubscription в CloudShell</span><span class="sxs-lookup"><span data-stu-id="b8d9d-535">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="b8d9d-536">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-536">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b8d9d-537">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b8d9d-537">Az.Compute</span></span>
* <span data-ttu-id="b8d9d-538">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzVm</span><span class="sxs-lookup"><span data-stu-id="b8d9d-538">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="b8d9d-539">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-539">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b8d9d-540">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b8d9d-540">Az.DataLakeStore</span></span>
* <span data-ttu-id="b8d9d-541">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="b8d9d-541">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="b8d9d-542">Get-AzDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-542">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="b8d9d-543">Add-AzDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-543">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="b8d9d-544">Set-AzDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-544">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="b8d9d-545">Remove-AzDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-545">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b8d9d-546">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b8d9d-546">Az.Network</span></span>
* <span data-ttu-id="b8d9d-547">Обновлен командлет Test-AzNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-547">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="b8d9d-548">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-548">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b8d9d-549">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b8d9d-549">Az.Resources</span></span>
* <span data-ttu-id="b8d9d-550">Устранена проблема, из-за которой командлет Get-AzRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), благодаря добавлению понятного исключения в сценарий.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-550">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="b8d9d-551">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-551">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="b8d9d-552">0.3.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-552">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="b8d9d-553">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="b8d9d-553">Azure.Storage</span></span>
* <span data-ttu-id="b8d9d-554">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-554">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="b8d9d-555">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="b8d9d-555">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="b8d9d-556">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="b8d9d-556">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="b8d9d-557">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-557">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="b8d9d-558">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="b8d9d-558">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="b8d9d-559">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b8d9d-559">Az.CognitiveServices</span></span>
* <span data-ttu-id="b8d9d-560">Поддержка Get-AzCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-560">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b8d9d-561">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b8d9d-561">Az.Compute</span></span>
* <span data-ttu-id="b8d9d-562">Исправлена команда Get-AzVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов</span><span class="sxs-lookup"><span data-stu-id="b8d9d-562">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="b8d9d-563">Добавлен пример использования SimpleParameterSet в справку командлета New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-563">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="b8d9d-564">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-564">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="b8d9d-565">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b8d9d-565">Az.DataFactoryV2</span></span>
* <span data-ttu-id="b8d9d-566">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-566">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b8d9d-567">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b8d9d-567">Az.Network</span></span>
* <span data-ttu-id="b8d9d-568">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-568">Added NetworkProfile functionality.</span></span> <span data-ttu-id="b8d9d-569">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="b8d9d-569">new cmdlets added</span></span>
    - <span data-ttu-id="b8d9d-570">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b8d9d-570">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="b8d9d-571">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b8d9d-571">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="b8d9d-572">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b8d9d-572">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="b8d9d-573">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b8d9d-573">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="b8d9d-574">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="b8d9d-574">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="b8d9d-575">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="b8d9d-575">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="b8d9d-576">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-576">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="b8d9d-577">Добавлены командлеты: New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="b8d9d-577">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="b8d9d-578">Добавлены командлеты: Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="b8d9d-578">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="b8d9d-579">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="b8d9d-579">Az.RedisCache</span></span>
* <span data-ttu-id="b8d9d-580">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-580">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="b8d9d-581">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-581">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="b8d9d-582">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b8d9d-582">Az.Resources</span></span>
* <span data-ttu-id="b8d9d-583">Добавлен отсутствующий параметр -Mode в командлет Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b8d9d-583">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="b8d9d-584">Исправлена ошибка командлета Get-AzProviderOperation для операций, когда Origin содержит User</span><span class="sxs-lookup"><span data-stu-id="b8d9d-584">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="b8d9d-585">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b8d9d-585">Az.Sql</span></span>
* <span data-ttu-id="b8d9d-586">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-586">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b8d9d-587">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b8d9d-587">Az.Websites</span></span>
* <span data-ttu-id="b8d9d-588">Новый командлет Get-AzWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="b8d9d-588">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="b8d9d-589">Новые командлеты New-AzWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows</span><span class="sxs-lookup"><span data-stu-id="b8d9d-589">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="b8d9d-590">0.2.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="b8d9d-590">0.2.0 - September 2018</span></span>
 <span data-ttu-id="b8d9d-591">Первый выпуск</span><span class="sxs-lookup"><span data-stu-id="b8d9d-591">Initial Release</span></span>