## <a name="140---february-2019"></a><span data-ttu-id="6316b-101">1.4.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6316b-101">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="6316b-102">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6316b-102">Az.AnalysisServices</span></span>
* <span data-ttu-id="6316b-103">Командлет AddAzureASAccount устарел.</span><span class="sxs-lookup"><span data-stu-id="6316b-103">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6316b-104">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6316b-104">Az.Automation</span></span>
* <span data-ttu-id="6316b-105">Обновлена справка для командлета Import-AzAutomationDscNodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="6316b-105">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="6316b-106">Добавлена проверка имени конфигурации для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="6316b-106">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="6316b-107">Улучшена обработка ошибок для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="6316b-107">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6316b-108">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6316b-108">Az.CognitiveServices</span></span>
* <span data-ttu-id="6316b-109">Добавлен параметр CustomSubdomainName — новый необязательный параметр для командлета New-AzCognitiveServicesAccount, который указывает поддомен для ресурса.</span><span class="sxs-lookup"><span data-stu-id="6316b-109">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6316b-110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6316b-110">Az.Compute</span></span>
* <span data-ttu-id="6316b-111">Устранена проблема с идентификаторами наборов параметров.</span><span class="sxs-lookup"><span data-stu-id="6316b-111">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="6316b-112">Обновлен командлет Get-AzVMExtension для отображения списка всех установленных расширений, если не указан параметр Name.</span><span class="sxs-lookup"><span data-stu-id="6316b-112">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="6316b-113">Для командлета Update-AzImage добавлены параметры Tag и ResourceId.</span><span class="sxs-lookup"><span data-stu-id="6316b-113">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="6316b-114">Командлет Get-AzVmssVM, который выполняется без указания идентификатора экземпляра и с параметром InstanceView, может выводить виртуальные машины из VMSS с представлением экземпляра.</span><span class="sxs-lookup"><span data-stu-id="6316b-114">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6316b-115">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6316b-115">Az.DataLakeStore</span></span>
* <span data-ttu-id="6316b-116">Добавлены командлеты для перечисления и восстановления удаленного элемента ADL.</span><span class="sxs-lookup"><span data-stu-id="6316b-116">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6316b-117">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6316b-117">Az.EventHub</span></span>
* <span data-ttu-id="6316b-118">Добавлено новое логическое свойство SkipEmptyArchives для пропуска пустых архивов в классе CaptureDescription Eventhub.</span><span class="sxs-lookup"><span data-stu-id="6316b-118">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="6316b-119">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6316b-119">Az.KeyVault</span></span>
* <span data-ttu-id="6316b-120">Исправлена расстановка тегов для командлета Set-AzKeyVaultSecret.</span><span class="sxs-lookup"><span data-stu-id="6316b-120">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6316b-121">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6316b-121">Az.LogicApp</span></span>
* <span data-ttu-id="6316b-122">Добавлен SKU "Базовый" для учетных записей интеграции.</span><span class="sxs-lookup"><span data-stu-id="6316b-122">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="6316b-123">Добавлены типы сопоставлений Liquid, а также XSLT 2.0 и XSLT 3.0.</span><span class="sxs-lookup"><span data-stu-id="6316b-123">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="6316b-124">Новые командлеты для сборок учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="6316b-124">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="6316b-125">Get-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="6316b-125">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="6316b-126">New-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="6316b-126">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="6316b-127">Remove-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="6316b-127">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="6316b-128">Set-AzIntegrationAccountAssembly.</span><span class="sxs-lookup"><span data-stu-id="6316b-128">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="6316b-129">Новые командлеты для конфигурации пакета учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="6316b-129">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="6316b-130">Get-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="6316b-130">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="6316b-131">New-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="6316b-131">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="6316b-132">Remove-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="6316b-132">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="6316b-133">Set-AzIntegrationAccountBatchConfiguration.</span><span class="sxs-lookup"><span data-stu-id="6316b-133">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="6316b-134">Обновлен пакет SDK Logic Apps до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="6316b-134">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6316b-135">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6316b-135">Az.Monitor</span></span>
* <span data-ttu-id="6316b-136">Обновлена справка для командлета Get-AzMetric.</span><span class="sxs-lookup"><span data-stu-id="6316b-136">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6316b-137">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6316b-137">Az.Network</span></span>
* <span data-ttu-id="6316b-138">Обновлен пример справки для командлета Add-AzApplicationGatewayCustomError.</span><span class="sxs-lookup"><span data-stu-id="6316b-138">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6316b-139">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6316b-139">Az.OperationalInsights</span></span>
* <span data-ttu-id="6316b-140">Дополнительная поддержка создания и получения источников данных ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="6316b-140">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="6316b-141">Добавлен новый тип ApplicationInsights для получения определенных или всех источников данных ApplicationInsights для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="6316b-141">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="6316b-142">Добавлен командлет New-AzOperationalInsightsApplicationInsightsDataSource для создания источника данных с использованием параметров указанного ресурса Application-Insightss: subscription Id, resourceGroupName и name.</span><span class="sxs-lookup"><span data-stu-id="6316b-142">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="6316b-143">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6316b-143">Az.Resources</span></span>
* <span data-ttu-id="6316b-144">исправлена проблема https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="6316b-144">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="6316b-145">исправлена проблема https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="6316b-145">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="6316b-146">исправлена проблема https://github.com/Azure/azure-powershell/issues/6219.</span><span class="sxs-lookup"><span data-stu-id="6316b-146">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="6316b-147">Исправлена ошибка, препятствующая повторному созданию KeyCredentials.</span><span class="sxs-lookup"><span data-stu-id="6316b-147">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="6316b-148">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6316b-148">Az.Sql</span></span>
* <span data-ttu-id="6316b-149">Добавлена поддержка уровня гипермасштабирования в базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="6316b-149">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="6316b-150">Исправлена ошибка, из-за которой восстановление могло завершиться со сбоем при указании ненужных свойств в запросе на восстановление.</span><span class="sxs-lookup"><span data-stu-id="6316b-150">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6316b-151">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6316b-151">Az.Websites</span></span>
* <span data-ttu-id="6316b-152">Исправлен пример для командлета Get-AzWebAppSlotMetrics.</span><span class="sxs-lookup"><span data-stu-id="6316b-152">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="6316b-153">1.3.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6316b-153">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6316b-154">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6316b-154">Az.Accounts</span></span>
* <span data-ttu-id="6316b-155">Обновление до последней версии ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="6316b-155">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="6316b-156">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6316b-156">Az.AnalysisServices</span></span>
<span data-ttu-id="6316b-157">Общедоступная версия модуля Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="6316b-157">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6316b-158">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6316b-158">Az.Compute</span></span>
* <span data-ttu-id="6316b-159">Расширение AEM: добавлена поддержка дисков UltraSSD, P60, P70 и P80.</span><span class="sxs-lookup"><span data-stu-id="6316b-159">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="6316b-160">Обновлено описание справки для командлета Set-AzVMBootDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="6316b-160">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="6316b-161">Обновлено описание справки и пример для командлета Update-AzImage.</span><span class="sxs-lookup"><span data-stu-id="6316b-161">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6316b-162">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6316b-162">Az.RecoveryServices</span></span>
<span data-ttu-id="6316b-163">Общедоступная версия модуля Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="6316b-163">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6316b-164">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6316b-164">Az.Resources</span></span>
* <span data-ttu-id="6316b-165">Исправлена расстановка тегов для групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6316b-165">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="6316b-166">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="6316b-166">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="6316b-167">Исправлена проблема с игнорированием командлетом `Get-AzureRmRoleAssignment` параметра -ErrorAction.</span><span class="sxs-lookup"><span data-stu-id="6316b-167">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="6316b-168">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="6316b-168">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="6316b-169">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6316b-169">Az.Sql</span></span>
* <span data-ttu-id="6316b-170">Добавлен командлет Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="6316b-170">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="6316b-171">Исправлена проблема с появлением исключения NullRef при выполнении командлетов SQL, если не выполнен вход в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="6316b-171">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="6316b-172">Исправлено исключение NullRef в командлете Get-AzSqlCapability.</span><span class="sxs-lookup"><span data-stu-id="6316b-172">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="6316b-173">1.2.1 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6316b-173">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6316b-174">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6316b-174">Az.Accounts</span></span>
* <span data-ttu-id="6316b-175">Выпуск с правильной версией службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="6316b-175">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="6316b-176">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6316b-176">Az.AnalysisServices</span></span>
* <span data-ttu-id="6316b-177">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="6316b-177">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6316b-178">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6316b-178">Az.RecoveryServices</span></span>
* <span data-ttu-id="6316b-179">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="6316b-179">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="6316b-180">1.2.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6316b-180">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6316b-181">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6316b-181">Az.Accounts</span></span>
* <span data-ttu-id="6316b-182">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="6316b-182">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6316b-183">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="6316b-183">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6316b-184">Добавлено предупреждающее сообщение в PS Core для модуля Uninstall-AzureRm.</span><span class="sxs-lookup"><span data-stu-id="6316b-184">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="6316b-185">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="6316b-185">Az.Aks</span></span>
* <span data-ttu-id="6316b-186">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="6316b-186">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6316b-187">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6316b-187">Az.Automation</span></span>
* <span data-ttu-id="6316b-188">Добавлена поддержка для модулей runbook Python 2.</span><span class="sxs-lookup"><span data-stu-id="6316b-188">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="6316b-189">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="6316b-189">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6316b-190">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6316b-190">Az.Cdn</span></span>
* <span data-ttu-id="6316b-191">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="6316b-191">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6316b-192">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6316b-192">Az.Compute</span></span>
* <span data-ttu-id="6316b-193">Добавлен командлет Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="6316b-193">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="6316b-194">Добавлен параметр TempDisk к командлету Set-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="6316b-194">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="6316b-195">Исправлено предупреждающее сообщение командлета New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="6316b-195">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="6316b-196">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6316b-196">Az.ContainerRegistry</span></span>
* <span data-ttu-id="6316b-197">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="6316b-197">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6316b-198">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6316b-198">Az.DataFactory</span></span>
* <span data-ttu-id="6316b-199">Пакет SDK ADF .Net обновлен до версии 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="6316b-199">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6316b-200">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6316b-200">Az.DataLakeStore</span></span>
* <span data-ttu-id="6316b-201">Исправлена проблема с конечной точкой ADLS при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="6316b-201">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="6316b-202">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7462.</span><span class="sxs-lookup"><span data-stu-id="6316b-202">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="6316b-203">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="6316b-203">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6316b-204">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6316b-204">Az.IotHub</span></span>
* <span data-ttu-id="6316b-205">Добавлен формат кодирования для командлета Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="6316b-205">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6316b-206">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6316b-206">Az.KeyVault</span></span>
* <span data-ttu-id="6316b-207">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="6316b-207">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6316b-208">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6316b-208">Az.Network</span></span>
* <span data-ttu-id="6316b-209">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="6316b-209">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="6316b-210">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6316b-210">Az.Resources</span></span>
* <span data-ttu-id="6316b-211">Исправлены неправильные примеры в справочной документации по командлетам New-AzADAppCredential и New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="6316b-211">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="6316b-212">Исправлена проблема, при которой путь для параметра -TemplateFile не удавалось разрешить до выполнения командлетов развертывания групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6316b-212">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="6316b-213">Az.Resources: исправлена документация для значения по умолчанию -Mode командлета New-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="6316b-213">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="6316b-214">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/7522.</span><span class="sxs-lookup"><span data-stu-id="6316b-214">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="6316b-215">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/5747.</span><span class="sxs-lookup"><span data-stu-id="6316b-215">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="6316b-216">Исправлена проблема с форматированием объекта PSResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="6316b-216">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="6316b-217">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2123.</span><span class="sxs-lookup"><span data-stu-id="6316b-217">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6316b-218">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6316b-218">Az.ServiceFabric</span></span>
* <span data-ttu-id="6316b-219">Исправлена проблема с появлением исключения в процессе отката при добавлении сертификата к модели VMSS: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="6316b-219">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="6316b-220">Исправлены некоторые сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="6316b-220">Fix some error messages.</span></span>
* <span data-ttu-id="6316b-221">Исправлена проблема с созданием кластера с шаблоном ARM по умолчанию для командлета New-AzServiceFabriCluster, который не работал с операцией миграции в Az.</span><span class="sxs-lookup"><span data-stu-id="6316b-221">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="6316b-222">Исправлена проблема с добавлением сертификата кластера или приложения: теперь они добавляются только в Масштабируемые наборы виртуальных машин, которые сопоставлены с кластером, путем проверки идентификатора кластера в расширении.</span><span class="sxs-lookup"><span data-stu-id="6316b-222">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="6316b-223">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="6316b-223">Az.SignalR</span></span>
* <span data-ttu-id="6316b-224">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="6316b-224">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="6316b-225">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6316b-225">Az.Sql</span></span>
* <span data-ttu-id="6316b-226">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="6316b-226">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6316b-227">Обновлено описание параметра LicenseType с добавлением возможных значений.</span><span class="sxs-lookup"><span data-stu-id="6316b-227">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="6316b-228">Исправлена проблема с неправильным обновлением удостоверения управляемого экземпляра, если оно было единственным обновляемым свойством.</span><span class="sxs-lookup"><span data-stu-id="6316b-228">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="6316b-229">Поддержка пользовательских параметров сортировки в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="6316b-229">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6316b-230">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6316b-230">Az.Storage</span></span>
* <span data-ttu-id="6316b-231">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="6316b-231">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6316b-232">Добавлен вывод подробных сообщений об ошибке при получении или установке классических свойств ведения журнала или метрик в учетной записи хранилища класса Premium, так как учетная запись хранилища класса Premium не поддерживает классические функции ведения журнала и метрик.</span><span class="sxs-lookup"><span data-stu-id="6316b-232">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="6316b-233">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="6316b-233">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="6316b-234">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="6316b-234">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="6316b-235">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6316b-235">Az.TrafficManager</span></span>
* <span data-ttu-id="6316b-236">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="6316b-236">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6316b-237">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6316b-237">Az.Websites</span></span>
* <span data-ttu-id="6316b-238">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="6316b-238">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6316b-239">Исправлена работа командлета New-AzWebAppSSLBinding: сертификат отправляется в правильную группу ресурсов и правильное расположение, если приложение размещено в ASE.</span><span class="sxs-lookup"><span data-stu-id="6316b-239">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="6316b-240">Исправлена работа командлета New-AzWebAppSSLBinding: теги не перезаписываются при привязке SSL-сертификата к приложению.</span><span class="sxs-lookup"><span data-stu-id="6316b-240">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="6316b-241">1.1.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="6316b-241">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6316b-242">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6316b-242">Az.Accounts</span></span>
* <span data-ttu-id="6316b-243">Добавление области "Local" в Enable-AzureRmAlias.</span><span class="sxs-lookup"><span data-stu-id="6316b-243">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6316b-244">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6316b-244">Az.Compute</span></span>
* <span data-ttu-id="6316b-245">Теперь имя не является обязательным в идентификаторе набора параметров для Restart/Start/Stop/Remove/Set-AzVM и Save-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="6316b-245">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="6316b-246">Обновлено описание идентификатора в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="6316b-246">Updated the description of ID in help files</span></span>
* <span data-ttu-id="6316b-247">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="6316b-247">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6316b-248">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6316b-248">Az.DataLakeStore</span></span>
* <span data-ttu-id="6316b-249">Обновление версии пакета SDK для плоскости данных до 1.1.14 для устранения найденных проблем.</span><span class="sxs-lookup"><span data-stu-id="6316b-249">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="6316b-250">Исправлена обработка отрицательного времени доступа и времени изменения для getfilestatus и liststatus, исправлен токен отмены для асинхронных методов.</span><span class="sxs-lookup"><span data-stu-id="6316b-250">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="6316b-251">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6316b-251">Az.EventGrid</span></span>
* <span data-ttu-id="6316b-252">Обновление для использования API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="6316b-252">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="6316b-253">Обновлены указанные ниже командлеты для поддержки нового сценария в API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="6316b-253">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="6316b-254">New-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="6316b-254">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="6316b-255">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="6316b-255">Event Time-To-Live,</span></span>
        - <span data-ttu-id="6316b-256">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="6316b-256">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="6316b-257">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="6316b-257">Dead letter endpoint.</span></span>
    - <span data-ttu-id="6316b-258">Update-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="6316b-258">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="6316b-259">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="6316b-259">Event Time-To-Live,</span></span>
        - <span data-ttu-id="6316b-260">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="6316b-260">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="6316b-261">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="6316b-261">Dead letter endpoint.</span></span>
* <span data-ttu-id="6316b-262">Для параметра EndpointType добавлены новые значения перечисления (storageQueue и hybridConnection) в командлеты New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="6316b-262">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="6316b-263">Если ожидается, что создание или обновление подписки на событие повлечет за собой действия со стороны пользователя, выполняемые вручную, отображается предупреждение при создании или обновлении подписки события.</span><span class="sxs-lookup"><span data-stu-id="6316b-263">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6316b-264">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6316b-264">Az.IotHub</span></span>
* <span data-ttu-id="6316b-265">Пакет SDK Центра Интернета вещей обновлен до последней версии.</span><span class="sxs-lookup"><span data-stu-id="6316b-265">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6316b-266">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6316b-266">Az.LogicApp</span></span>
* <span data-ttu-id="6316b-267">Get-AzLogicApp позволяет перечислить все параметры без указанного имени.</span><span class="sxs-lookup"><span data-stu-id="6316b-267">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="6316b-268">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6316b-268">Az.Resources</span></span>
* <span data-ttu-id="6316b-269">Исправлена проблема с набором параметров при предоставлении параметров "-ODataQuery" и "-ResourceId" для "Get-AzResource".</span><span class="sxs-lookup"><span data-stu-id="6316b-269">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="6316b-270">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7875.</span><span class="sxs-lookup"><span data-stu-id="6316b-270">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="6316b-271">Исправлена обработка параметра -Custom в New/Set-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="6316b-271">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="6316b-272">Исправлена опечатка в документации по New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="6316b-272">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="6316b-273">Параметр "-MailNickname" стал обязательным для "New-AzADUser".</span><span class="sxs-lookup"><span data-stu-id="6316b-273">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="6316b-274">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8220.</span><span class="sxs-lookup"><span data-stu-id="6316b-274">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="6316b-275">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="6316b-275">Az.SignalR</span></span>
* <span data-ttu-id="6316b-276">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="6316b-276">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="6316b-277">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6316b-277">Az.Sql</span></span>
* <span data-ttu-id="6316b-278">Зависимость клиента управления хранением преобразована для общей реализации в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="6316b-278">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6316b-279">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6316b-279">Az.Storage</span></span>
* <span data-ttu-id="6316b-280">Установка параметра StorageAccountName для контекста хранилища в качестве реального имени учетной записи хранения, если она была создана с использованием токена Sas, OAuth или анонимного доступа.</span><span class="sxs-lookup"><span data-stu-id="6316b-280">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="6316b-281">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="6316b-281">New-AzStorageContext</span></span>
* <span data-ttu-id="6316b-282">Создание токена Sas большого двоичного объекта моментального снимка с параметром "-FullUri". Возвращаемый URI исправлен на URI моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="6316b-282">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="6316b-283">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="6316b-283">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6316b-284">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6316b-284">Az.Websites</span></span>
* <span data-ttu-id="6316b-285">Исправлена ошибка синтаксического анализа даты в "Get-AzDeletedWebApp".</span><span class="sxs-lookup"><span data-stu-id="6316b-285">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="6316b-286">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="6316b-286">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="6316b-287">1.0.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="6316b-287">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="6316b-288">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="6316b-288">General</span></span>

- <span data-ttu-id="6316b-289">Общедоступная версия модуля Az.</span><span class="sxs-lookup"><span data-stu-id="6316b-289">General Availability of Az Module</span></span>
- <span data-ttu-id="6316b-290">Справка в Интернете для каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="6316b-290">Online help for each module</span></span>
- <span data-ttu-id="6316b-291">Дополнительные сведения и стратегию развития см. в статье [Announcing New Module 'Az'](https://aka.ms/azps-announce) (Объявление о новом модуле Az)</span><span class="sxs-lookup"><span data-stu-id="6316b-291">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="6316b-292">Сведения о миграции с AzureRM см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="6316b-292">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="6316b-293">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6316b-293">Az.Accounts</span></span>
- <span data-ttu-id="6316b-294">Изменено с Az.Profile.</span><span class="sxs-lookup"><span data-stu-id="6316b-294">Changed from Az.Profile</span></span>
- <span data-ttu-id="6316b-295">Исправлены форматы таблиц для типов профиля и контекста.</span><span class="sxs-lookup"><span data-stu-id="6316b-295">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="6316b-296">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6316b-296">Az.ApiManagement</span></span>
- <span data-ttu-id="6316b-297">Исправления для #7002.</span><span class="sxs-lookup"><span data-stu-id="6316b-297">Fixes for #7002</span></span>
- <span data-ttu-id="6316b-298">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="6316b-298">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="6316b-299">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6316b-299">Az.Batch</span></span>
- <span data-ttu-id="6316b-300">Добавлена возможность видеть, какая версия агента узла пакетной службы Azure работает в пуле на каждой виртуальной машине, с помощью нового свойства `NodeAgentInformation` в `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="6316b-300">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="6316b-301">Значение `Caching` по умолчанию для `PSDataDisk` теперь `ReadWrite` вместо `None`.</span><span class="sxs-lookup"><span data-stu-id="6316b-301">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="6316b-302">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="6316b-302">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="6316b-303">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="6316b-303">Az.Billing</span></span>
- <span data-ttu-id="6316b-304">Объединены командлеты Billing, Consumption и UsageAggregates. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0).</span><span class="sxs-lookup"><span data-stu-id="6316b-304">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="6316b-305">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="6316b-305">Az.CognitivServices</span></span>
- <span data-ttu-id="6316b-306">Добавлены средства заполнения для SkuName и Typem, доступные в операции New-AzureRmCognitiveServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="6316b-306">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="6316b-307">Удален набор параметров GetSkusWithAccountParamSetName из Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="6316b-307">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="6316b-308">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6316b-308">Az.ContainerInstance</span></span>
- <span data-ttu-id="6316b-309">Добавлена поддержка ManagedIdentity.</span><span class="sxs-lookup"><span data-stu-id="6316b-309">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="6316b-310">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="6316b-310">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="6316b-311">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="6316b-311">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="6316b-312">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6316b-312">Az.DataLakeStore</span></span>
- <span data-ttu-id="6316b-313">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="6316b-313">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="6316b-314">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6316b-314">Az.Monitor</span></span>
- <span data-ttu-id="6316b-315">"Az.Insights" переименован в "Az.Monitor" и внесены другие незначительные критические изменения. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="6316b-315">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="6316b-316">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6316b-316">Az.KeyVault</span></span>
- <span data-ttu-id="6316b-317">Из типов вывода удалено устаревшее свойство PurgeDisabled</span><span class="sxs-lookup"><span data-stu-id="6316b-317">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="6316b-318">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="6316b-318">Az.MachineLearning</span></span>
- <span data-ttu-id="6316b-319">Включены командлеты из модуля Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="6316b-319">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="6316b-320">Az.Media</span><span class="sxs-lookup"><span data-stu-id="6316b-320">Az.Media</span></span>
- <span data-ttu-id="6316b-321">Удаляет устаревший псевдоним Tags из New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="6316b-321">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="6316b-322">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6316b-322">Az.Network</span></span>
<span data-ttu-id="6316b-323">В шлюз приложений добавлена поддержка настройки RewriteRuleSets</span><span class="sxs-lookup"><span data-stu-id="6316b-323">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="6316b-324">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="6316b-324">New cmdlets added:</span></span>
        - <span data-ttu-id="6316b-325">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6316b-325">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6316b-326">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6316b-326">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6316b-327">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6316b-327">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6316b-328">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6316b-328">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6316b-329">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6316b-329">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6316b-330">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="6316b-330">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="6316b-331">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="6316b-331">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="6316b-332">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="6316b-332">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="6316b-333">В следующие командлеты добавлен необязательный параметр -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6316b-333">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="6316b-334">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6316b-334">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="6316b-335">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6316b-335">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="6316b-336">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6316b-336">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="6316b-337">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6316b-337">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="6316b-338">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6316b-338">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="6316b-339">New-AzureRmApplicationGatewayUrlPathMapConfig добавил с помощью идентификатора поддержку KeyVault для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="6316b-339">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="6316b-340">В следующие командлеты добавлен необязательный параметр -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6316b-340">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="6316b-341">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6316b-341">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="6316b-342">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6316b-342">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="6316b-343">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6316b-343">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="6316b-344">В командлет New-AzApplicationGateway добавлен необязательный параметр -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="6316b-344">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="6316b-345">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="6316b-345">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="6316b-346">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6316b-346">Az.OperationalInsights</span></span>
- <span data-ttu-id="6316b-347">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="6316b-347">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="6316b-348">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6316b-348">Az.Profile</span></span>
- <span data-ttu-id="6316b-349">Имя модуля изменено на Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="6316b-349">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="6316b-350">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6316b-350">Az.RecoveryServices</span></span>
- <span data-ttu-id="6316b-351">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="6316b-351">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="6316b-352">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6316b-352">Az.Resources</span></span>
- <span data-ttu-id="6316b-353">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="6316b-353">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="6316b-354">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6316b-354">Az.ServiceFabric</span></span>
- <span data-ttu-id="6316b-355">Поддержка спецификации сертификата по общему имени и отпечатку</span><span class="sxs-lookup"><span data-stu-id="6316b-355">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="6316b-356">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="6316b-356">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="6316b-357">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="6316b-357">Az.SIgnalR</span></span>
- <span data-ttu-id="6316b-358">Общедоступная версия командлетов PowerShell для SIgnalR</span><span class="sxs-lookup"><span data-stu-id="6316b-358">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="6316b-359">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6316b-359">Az.Sql</span></span>
- <span data-ttu-id="6316b-360">Добавлены новые типы обнаружения Data_Exfiltration и Unsafe_Action в командлеты обнаружения угроз</span><span class="sxs-lookup"><span data-stu-id="6316b-360">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="6316b-361">Примеры обновленной документации для командлетов аудита Sql</span><span class="sxs-lookup"><span data-stu-id="6316b-361">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="6316b-362">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="6316b-362">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="6316b-363">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6316b-363">Az.Storage</span></span>
- <span data-ttu-id="6316b-364">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="6316b-364">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="6316b-365">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6316b-365">Az.Websites</span></span>
- <span data-ttu-id="6316b-366">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="6316b-366">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="6316b-367">0.7.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="6316b-367">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="6316b-368">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="6316b-368">General</span></span>

* <span data-ttu-id="6316b-369">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="6316b-369">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="6316b-370">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6316b-370">Az.Compute</span></span>

* <span data-ttu-id="6316b-371">Добавлена поддержка UltraSSD и образов коллекции в простых наборах параметров для командлетов `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="6316b-371">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="6316b-372">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6316b-372">Az.DataLakeStore</span></span>

* <span data-ttu-id="6316b-373">Исправлено косую черту в конце домена учетной записи ADLS</span><span class="sxs-lookup"><span data-stu-id="6316b-373">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="6316b-374">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6316b-374">Az.FrontDoor</span></span>

* <span data-ttu-id="6316b-375">Исправлены некоторые неработающие ссылки</span><span class="sxs-lookup"><span data-stu-id="6316b-375">Fixed some broken links</span></span>
    - <span data-ttu-id="6316b-376">В статьях New-AzureRmFrontDoor и Set-AzureRmFrontDoor исправлена ссылка на статью командлета New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="6316b-376">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="6316b-377">В статье New-AzureRmFrontDoorManagedRuleObject исправлена ссылка на статью командлета New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="6316b-377">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="6316b-378">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6316b-378">Az.RecoveryServices</span></span>

* <span data-ttu-id="6316b-379">Добавлены проверки на стороне клиента для операций восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="6316b-379">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="6316b-380">StorageAccountName и storageAccountResourceGroupName являются необязательными для восстановления afs.</span><span class="sxs-lookup"><span data-stu-id="6316b-380">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="6316b-381">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6316b-381">Az.Resources</span></span>

* <span data-ttu-id="6316b-382">Исправление для https://github.com/Azure/azure-powershell/issues/7679.</span><span class="sxs-lookup"><span data-stu-id="6316b-382">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="6316b-383">Обновите Get-AzureRmRoleAssignment, чтобы использовать область подписки, если она указана при запросе классических администраторов.</span><span class="sxs-lookup"><span data-stu-id="6316b-383">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="6316b-384">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6316b-384">Az.Sql</span></span>

* <span data-ttu-id="6316b-385">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="6316b-385">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="6316b-386">Устранена проблема с использованием Get-AzureRmSqlDatabaseVulnerabilityAssessment с .NET Core.</span><span class="sxs-lookup"><span data-stu-id="6316b-386">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="6316b-387">Изменена документация справочных сообщений, связанных с командлетами аудита SQL.</span><span class="sxs-lookup"><span data-stu-id="6316b-387">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="6316b-388">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6316b-388">Az.Storage</span></span>

* <span data-ttu-id="6316b-389">Добавлено -EnableHierarchicalNamespace к New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6316b-389">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="6316b-390">Устранена проблема, из-за которой командлет Copy File не может повторно использовать исходный контекст в пункте назначения, если не введен -DestContext</span><span class="sxs-lookup"><span data-stu-id="6316b-390">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="6316b-391">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="6316b-391">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="6316b-392">Поддержка статической конфигурации сайта</span><span class="sxs-lookup"><span data-stu-id="6316b-392">Support Static Website configuration</span></span>
    - <span data-ttu-id="6316b-393">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="6316b-393">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="6316b-394">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="6316b-394">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="6316b-395">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6316b-395">Az.Websites</span></span>

* <span data-ttu-id="6316b-396">Set-AzureRmWebApp и Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6316b-396">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="6316b-397">Добавлен новый параметр (-AzureStoragePath), который указывает путь службы хранилища Azure для подключения в приложениях-контейнерах Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="6316b-397">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="6316b-398">Используйте выходные данные нового командлета New-AzureRmWebAppAzureStoragePath в качестве параметра, чтобы задать пути к службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="6316b-398">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="6316b-399">0.6.1 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="6316b-399">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="6316b-400">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6316b-400">Az.ApiManagement</span></span>
* <span data-ttu-id="6316b-401">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="6316b-401">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="6316b-402">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6316b-402">Az.Automation</span></span>
* <span data-ttu-id="6316b-403">Командлеты службы автоматизации Azure на базе Swagger.</span><span class="sxs-lookup"><span data-stu-id="6316b-403">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="6316b-404">Добавлены командлеты для Управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="6316b-404">Added Update Management cmdlets</span></span>
* <span data-ttu-id="6316b-405">Добавлены командлеты для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="6316b-405">Added Source Control cmdlets</span></span>
* <span data-ttu-id="6316b-406">Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="6316b-406">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="6316b-407">Исправлена команда DSC для регистрации узла.</span><span class="sxs-lookup"><span data-stu-id="6316b-407">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="6316b-408">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6316b-408">Az.Compute</span></span>
* <span data-ttu-id="6316b-409">Исправлена проблема с удостоверением, назначаемым системой.</span><span class="sxs-lookup"><span data-stu-id="6316b-409">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="6316b-410">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="6316b-410">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="6316b-411">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6316b-411">Az.ContainerInstance</span></span>
* <span data-ttu-id="6316b-412">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="6316b-412">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="6316b-413">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="6316b-413">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="6316b-414">Обновлено описание в примерах командлетов для Marketplace.</span><span class="sxs-lookup"><span data-stu-id="6316b-414">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="6316b-415">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6316b-415">Az.Network</span></span>
* <span data-ttu-id="6316b-416">Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="6316b-416">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="6316b-417">Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="6316b-417">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="6316b-418">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="6316b-418">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="6316b-419">Исправлены проблемы с использованием памяти в карте виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="6316b-419">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="6316b-420">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="6316b-420">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="6316b-421">Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="6316b-421">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="6316b-422">Параметры часового пояса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="6316b-422">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="6316b-423">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="6316b-423">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="6316b-424">Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="6316b-424">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="6316b-425">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="6316b-425">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="6316b-426">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="6316b-426">Az.Relay</span></span>
* <span data-ttu-id="6316b-427">Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.</span><span class="sxs-lookup"><span data-stu-id="6316b-427">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="6316b-428">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6316b-428">Az.Resources</span></span>
* <span data-ttu-id="6316b-429">Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.</span><span class="sxs-lookup"><span data-stu-id="6316b-429">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="6316b-430">Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.</span><span class="sxs-lookup"><span data-stu-id="6316b-430">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="6316b-431">Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.</span><span class="sxs-lookup"><span data-stu-id="6316b-431">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="6316b-432">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6316b-432">Az.ServiceFabric</span></span>
* <span data-ttu-id="6316b-433">Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.</span><span class="sxs-lookup"><span data-stu-id="6316b-433">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="6316b-434">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6316b-434">Az.Sql</span></span>
* <span data-ttu-id="6316b-435">Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="6316b-435">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="6316b-436">Get-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="6316b-436">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6316b-437">New-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="6316b-437">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6316b-438">Set-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="6316b-438">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6316b-439">Remove-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="6316b-439">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6316b-440">Get-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="6316b-440">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="6316b-441">New-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="6316b-441">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="6316b-442">Restore-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="6316b-442">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="6316b-443">Remove-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="6316b-443">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="6316b-444">Добавлено расширенное управление политиками аудита для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="6316b-444">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="6316b-445">Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="6316b-445">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="6316b-446">Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.</span><span class="sxs-lookup"><span data-stu-id="6316b-446">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="6316b-447">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="6316b-447">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="6316b-448">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="6316b-448">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="6316b-449">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="6316b-449">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="6316b-450">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="6316b-450">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="6316b-451">Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="6316b-451">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="6316b-452">0.5.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="6316b-452">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="6316b-453">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="6316b-453">General</span></span>
* <span data-ttu-id="6316b-454">Добавлены средства заполнения ресурсов для многих основных командлетов — они позволяют вам переключать существующие имена ресурсов при вызове командлетов в интерактивном режиме</span><span class="sxs-lookup"><span data-stu-id="6316b-454">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="6316b-455">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6316b-455">Az.Profile</span></span>
* <span data-ttu-id="6316b-456">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6316b-456">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="6316b-457">В командлете Connect-AzAccount параметр TenantId переименован в Tenant и добавлен псевдоним для TenantId</span><span class="sxs-lookup"><span data-stu-id="6316b-457">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="6316b-458">Обновлено описание TenantId для командлета Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="6316b-458">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="6316b-459">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="6316b-459">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="6316b-460">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="6316b-460">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="6316b-461">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="6316b-461">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="6316b-462">Устранена проблема, при которой командлет Disconnect-AzAccount вызывал сбой при отсутствии подключения</span><span class="sxs-lookup"><span data-stu-id="6316b-462">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="6316b-463">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6316b-463">Az.CognitiveServices</span></span>
* <span data-ttu-id="6316b-464">Добавлена операция Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="6316b-464">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6316b-465">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6316b-465">Az.Compute</span></span>
* <span data-ttu-id="6316b-466">Добавлены командлеты Add-AzVmssVMDataDisk и Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="6316b-466">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="6316b-467">Get-AzVMImage отображает AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="6316b-467">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="6316b-468">Устранена проблема, при которой значения параметров SetAzVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="6316b-468">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6316b-469">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6316b-469">Az.DataLakeStore</span></span>
* <span data-ttu-id="6316b-470">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="6316b-470">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="6316b-471">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="6316b-471">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="6316b-472">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="6316b-472">Az.Insights</span></span>
* <span data-ttu-id="6316b-473">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="6316b-473">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="6316b-474">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="6316b-474">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="6316b-475">Исправлена проблема № 7513 [Insights], при которой для командлета Set-AzDiagnosticSetting требовалось явное указание категорий во время создания параметра</span><span class="sxs-lookup"><span data-stu-id="6316b-475">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="6316b-476">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="6316b-476">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6316b-477">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6316b-477">Az.Network</span></span>
* <span data-ttu-id="6316b-478">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="6316b-478">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="6316b-479">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="6316b-479">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="6316b-480">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="6316b-480">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="6316b-481">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="6316b-481">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="6316b-482">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="6316b-482">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="6316b-483">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="6316b-483">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="6316b-484">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="6316b-484">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6316b-485">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6316b-485">Az.PolicyInsights</span></span>
* <span data-ttu-id="6316b-486">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="6316b-486">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="6316b-487">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6316b-487">Az.Resources</span></span>
* <span data-ttu-id="6316b-488">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="6316b-488">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="6316b-489">Разрешено перечисление ресурсов с помощью параметра -ResourceId для командлета Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="6316b-489">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6316b-490">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6316b-490">Az.ServiceBus</span></span>
* <span data-ttu-id="6316b-491">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="6316b-491">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6316b-492">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6316b-492">Az.ServiceFabric</span></span>
* <span data-ttu-id="6316b-493">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="6316b-493">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="6316b-494">Исправлен командлет Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="6316b-494">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="6316b-495">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="6316b-495">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="6316b-496">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="6316b-496">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="6316b-497">Исправлен командлет Update-AzServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="6316b-497">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="6316b-498">0.4.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="6316b-498">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="6316b-499">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6316b-499">Az.Profile</span></span>
* <span data-ttu-id="6316b-500">Устранена проблема с Get-AzSubscription в CloudShell</span><span class="sxs-lookup"><span data-stu-id="6316b-500">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="6316b-501">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6316b-501">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6316b-502">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6316b-502">Az.Compute</span></span>
* <span data-ttu-id="6316b-503">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzVm</span><span class="sxs-lookup"><span data-stu-id="6316b-503">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="6316b-504">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="6316b-504">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6316b-505">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6316b-505">Az.DataLakeStore</span></span>
* <span data-ttu-id="6316b-506">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="6316b-506">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="6316b-507">Get-AzDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6316b-507">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="6316b-508">Add-AzDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6316b-508">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="6316b-509">Set-AzDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6316b-509">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="6316b-510">Remove-AzDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6316b-510">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6316b-511">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6316b-511">Az.Network</span></span>
* <span data-ttu-id="6316b-512">Обновлен командлет Test-AzNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="6316b-512">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="6316b-513">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="6316b-513">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6316b-514">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6316b-514">Az.Resources</span></span>
* <span data-ttu-id="6316b-515">Устранена проблема, из-за которой командлет Get-AzRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), благодаря добавлению понятного исключения в сценарий.</span><span class="sxs-lookup"><span data-stu-id="6316b-515">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="6316b-516">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="6316b-516">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="6316b-517">0.3.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="6316b-517">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="6316b-518">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="6316b-518">Azure.Storage</span></span>
* <span data-ttu-id="6316b-519">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="6316b-519">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="6316b-520">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="6316b-520">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="6316b-521">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="6316b-521">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="6316b-522">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="6316b-522">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="6316b-523">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="6316b-523">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="6316b-524">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6316b-524">Az.CognitiveServices</span></span>
* <span data-ttu-id="6316b-525">Поддержка Get-AzCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="6316b-525">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6316b-526">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6316b-526">Az.Compute</span></span>
* <span data-ttu-id="6316b-527">Исправлена команда Get-AzVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов</span><span class="sxs-lookup"><span data-stu-id="6316b-527">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="6316b-528">Добавлен пример использования SimpleParameterSet в справку командлета New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="6316b-528">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="6316b-529">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="6316b-529">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="6316b-530">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6316b-530">Az.DataFactoryV2</span></span>
* <span data-ttu-id="6316b-531">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="6316b-531">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6316b-532">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6316b-532">Az.Network</span></span>
* <span data-ttu-id="6316b-533">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="6316b-533">Added NetworkProfile functionality.</span></span> <span data-ttu-id="6316b-534">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="6316b-534">new cmdlets added</span></span>
    - <span data-ttu-id="6316b-535">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6316b-535">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="6316b-536">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6316b-536">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="6316b-537">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6316b-537">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="6316b-538">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6316b-538">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="6316b-539">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="6316b-539">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="6316b-540">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="6316b-540">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="6316b-541">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="6316b-541">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="6316b-542">Добавлены командлеты: New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="6316b-542">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="6316b-543">Добавлены командлеты: Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="6316b-543">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="6316b-544">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6316b-544">Az.RedisCache</span></span>
* <span data-ttu-id="6316b-545">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="6316b-545">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="6316b-546">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="6316b-546">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="6316b-547">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6316b-547">Az.Resources</span></span>
* <span data-ttu-id="6316b-548">Добавлен отсутствующий параметр -Mode в командлет Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6316b-548">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="6316b-549">Исправлена ошибка командлета Get-AzProviderOperation для операций, когда Origin содержит User</span><span class="sxs-lookup"><span data-stu-id="6316b-549">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="6316b-550">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6316b-550">Az.Sql</span></span>
* <span data-ttu-id="6316b-551">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="6316b-551">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6316b-552">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6316b-552">Az.Websites</span></span>
* <span data-ttu-id="6316b-553">Новый командлет Get-AzWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="6316b-553">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="6316b-554">Новые командлеты New-AzWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows</span><span class="sxs-lookup"><span data-stu-id="6316b-554">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="6316b-555">0.2.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="6316b-555">0.2.0 - September 2018</span></span>
 <span data-ttu-id="6316b-556">Первый выпуск</span><span class="sxs-lookup"><span data-stu-id="6316b-556">Initial Release</span></span>