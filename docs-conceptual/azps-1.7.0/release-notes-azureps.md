---
ms.openlocfilehash: 54d7a9da878e085e90479fb229876c9be6dafd74
ms.sourcegitcommit: 89066b7c4b527357bb2024e1ad708df84c131804
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2019
ms.locfileid: "59364238"
---
## <a name="170---april-2019"></a><span data-ttu-id="9375d-101">1.7.0 —апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="9375d-101">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="9375d-102">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="9375d-102">Highlights since the last major release</span></span>
* <span data-ttu-id="9375d-103">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="9375d-103">General availability of `Az` module</span></span>
* <span data-ttu-id="9375d-104">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="9375d-104">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="9375d-105">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="9375d-105">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="9375d-106">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="9375d-106">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="9375d-107">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="9375d-107">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="9375d-108">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="9375d-108">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="9375d-109">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="9375d-109">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="9375d-110">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9375d-110">Az.Accounts</span></span>
* <span data-ttu-id="9375d-111">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметр AzureAnalysisServicesEndpointResourceId.</span><span class="sxs-lookup"><span data-stu-id="9375d-111">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="9375d-112">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="9375d-112">Az.AnalysisServices</span></span>
* <span data-ttu-id="9375d-113">Использование ServiceClient в командлетах плоскости данных и удаление исходной логики проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="9375d-113">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="9375d-114">Add-AzureASAccount используется как оболочка для Connect-AzAccount во избежание критических изменений.</span><span class="sxs-lookup"><span data-stu-id="9375d-114">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="9375d-115">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="9375d-115">Az.Automation</span></span>
* <span data-ttu-id="9375d-116">Исправлена ошибка командлета New-AzAutomationSoftwareUpdateConfiguration, связанная с включением.</span><span class="sxs-lookup"><span data-stu-id="9375d-116">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="9375d-117">Теперь параметры IncludedKbNumber и IncludedPackageNameMask должны работать нормально.</span><span class="sxs-lookup"><span data-stu-id="9375d-117">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="9375d-118">Исправлена ошибка динамической группы управления обновлениями службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="9375d-118">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9375d-119">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9375d-119">Az.Compute</span></span>
* <span data-ttu-id="9375d-120">В командлеты New-AzDiskConfig и New-AzSnapshotConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="9375d-120">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="9375d-121">Теперь можно создавать виртуальные машину на основе образов из коллекции от других клиентов.</span><span class="sxs-lookup"><span data-stu-id="9375d-121">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="9375d-122">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="9375d-122">Az.ContainerInstance</span></span>
* <span data-ttu-id="9375d-123">Исправлена проблема в параметре -Command командлета New-AzContainerGroup, из-за которой в конце добавлялся пустой аргумент.</span><span class="sxs-lookup"><span data-stu-id="9375d-123">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="9375d-124">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="9375d-124">Az.DataFactory</span></span>
* <span data-ttu-id="9375d-125">Пакет SDK для ADF .NET обновлен до версии 3.0.2.</span><span class="sxs-lookup"><span data-stu-id="9375d-125">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="9375d-126">Командлет Set-AzDataFactoryV2 обновлен с помощью дополнительных параметров для настроек, связанных с RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="9375d-126">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="9375d-127">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9375d-127">Az.Resources</span></span>
* <span data-ttu-id="9375d-128">Улучшена обработка поставщиков Get-AzResource при предоставлении параметров -ResourceId или -ResourceGroupName, -Name и -ResourceType.</span><span class="sxs-lookup"><span data-stu-id="9375d-128">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="9375d-129">Улучшена обработка ошибок в командлетах Test-AzDeployment и Test-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="9375d-129">Improve error handling for for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="9375d-130">Теперь ошибки, возникающие за пределами проверки развертывания, обрабатываются и включаются в выходные данные команды.</span><span class="sxs-lookup"><span data-stu-id="9375d-130">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="9375d-131">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="9375d-131">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="9375d-132">Добавлен параметр-переключатель -IgnoreDynamicParameters, с помощью которого можно настроить командлеты развертывания так, чтобы они пропускали запросы в сценариях скриптов и заданий.</span><span class="sxs-lookup"><span data-stu-id="9375d-132">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="9375d-133">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="9375d-133">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="9375d-134">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9375d-134">Az.Sql</span></span>
* <span data-ttu-id="9375d-135">Поддержка классификации данных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="9375d-135">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="9375d-136">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="9375d-136">Az.Storage</span></span>
* <span data-ttu-id="9375d-137">Подробные сообщения об ошибке передаются при создании контекста хранилища с помощью параметра -UseConnectedAccount, но без входа в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="9375d-137">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="9375d-138">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="9375d-138">New-AzStorageContext</span></span>
* <span data-ttu-id="9375d-139">Поддержка свойств службы управления BLOB-объектов в указанной учетной записи хранения с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="9375d-139">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="9375d-140">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="9375d-140">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="9375d-141">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="9375d-141">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="9375d-142">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="9375d-142">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="9375d-143">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="9375d-143">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="9375d-144">Поддержка параметра -AsJob в командлетах для отправки и скачивания больших двоичных объектов и файлов.</span><span class="sxs-lookup"><span data-stu-id="9375d-144">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="9375d-145">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="9375d-145">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="9375d-146">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="9375d-146">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="9375d-147">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="9375d-147">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="9375d-148">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="9375d-148">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="9375d-149">1.6.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="9375d-149">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="9375d-150">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="9375d-150">Highlights since the last major release</span></span>
* <span data-ttu-id="9375d-151">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="9375d-151">General availability of `Az` module</span></span>
* <span data-ttu-id="9375d-152">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="9375d-152">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="9375d-153">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="9375d-153">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="9375d-154">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="9375d-154">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="9375d-155">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="9375d-155">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="9375d-156">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="9375d-156">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="9375d-157">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="9375d-157">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="9375d-158">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="9375d-158">Az.Automation</span></span>
* <span data-ttu-id="9375d-159">В управление обновлениями службы автоматизации Azure внесены изменения для поддержки следующих новых функций:</span><span class="sxs-lookup"><span data-stu-id="9375d-159">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="9375d-160">динамическое группирование;</span><span class="sxs-lookup"><span data-stu-id="9375d-160">Dynamic grouping</span></span>
    * <span data-ttu-id="9375d-161">скрипты предварительного или последующего выполнения;</span><span class="sxs-lookup"><span data-stu-id="9375d-161">Pre-Post script</span></span>
    * <span data-ttu-id="9375d-162">параметр перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="9375d-162">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9375d-163">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9375d-163">Az.Compute</span></span>
* <span data-ttu-id="9375d-164">Устранена проблема, связанная с разрешением пути в Get-AzVmBootDiagnosticsData.</span><span class="sxs-lookup"><span data-stu-id="9375d-164">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="9375d-165">Обновление клиентской библиотеки вычислений до версии 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="9375d-165">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="9375d-166">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="9375d-166">Az.KeyVault</span></span>
* <span data-ttu-id="9375d-167">Добавлена поддержка подстановочных знаков в командлетах KeyVault.</span><span class="sxs-lookup"><span data-stu-id="9375d-167">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="9375d-168">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9375d-168">Az.Network</span></span>
* <span data-ttu-id="9375d-169">Добавлена поддержка анализа угроз для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="9375d-169">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="9375d-170">Добавлены настраиваемые правила и ресурс верхнего уровня для политики брандмауэра Шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="9375d-170">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="9375d-171">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="9375d-171">Az.RecoveryServices</span></span>
* <span data-ttu-id="9375d-172">В политику виртуальной машины Azure добавлен объект SnapshotRetentionInDays для поддержки мгновенного восстановления.</span><span class="sxs-lookup"><span data-stu-id="9375d-172">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="9375d-173">Добавлена поддержка канала для отмены регистрации контейнера.</span><span class="sxs-lookup"><span data-stu-id="9375d-173">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="9375d-174">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9375d-174">Az.Resources</span></span>
* <span data-ttu-id="9375d-175">Обновлена поддержка подстановочных знаков для Get-AzResource и Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9375d-175">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="9375d-176">Обновлены учетные данные, используемые при общих вызовах к ARM.</span><span class="sxs-lookup"><span data-stu-id="9375d-176">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="9375d-177">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9375d-177">Az.Sql</span></span>
* <span data-ttu-id="9375d-178">Изменен тип параметра (ExcludeDetectionType) командлетов для обнаружения угроз с DetectionTypes на string[] для поддержки актуального состояния при добавлении новых типов обнаружения и для поддержки автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="9375d-178">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="9375d-179">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="9375d-179">Az.Storage</span></span>
* <span data-ttu-id="9375d-180">Поддержка получения, настройки и удаления политики управления в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="9375d-180">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="9375d-181">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="9375d-181">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="9375d-182">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="9375d-182">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="9375d-183">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="9375d-183">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="9375d-184">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="9375d-184">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="9375d-185">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="9375d-185">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="9375d-186">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="9375d-186">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="9375d-187">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="9375d-187">Az.Websites</span></span>
* <span data-ttu-id="9375d-188">Исправлена ошибка с шаблоном ARM, из-за которой прерывалось клонирование все слотов при использовании New-AzWebApp -IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="9375d-188">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="9375d-189">1.5.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="9375d-189">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="9375d-190">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9375d-190">Az.Accounts</span></span>
* <span data-ttu-id="9375d-191">Добавлена команда Register-AzModule для поддержки созданных командлетов AutoRest.</span><span class="sxs-lookup"><span data-stu-id="9375d-191">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="9375d-192">Обновлены примеры для Connect AzAccount.</span><span class="sxs-lookup"><span data-stu-id="9375d-192">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="9375d-193">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="9375d-193">Az.Automation</span></span>
* <span data-ttu-id="9375d-194">Исправлена проблема с получением некоторых ежемесячных расписаний в нескольких командлетах службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="9375d-194">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="9375d-195">Исправлен командлет Get-AzAutomationDscNode, возвращающий только первые 20 узлов.</span><span class="sxs-lookup"><span data-stu-id="9375d-195">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="9375d-196">Теперь он возвращает все узлы.</span><span class="sxs-lookup"><span data-stu-id="9375d-196">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="9375d-197">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="9375d-197">Az.Cdn</span></span>
* <span data-ttu-id="9375d-198">Добавлены новые командлеты PowerShell для включения и отключения HTTPS для личного домена и отключены устаревшие командлеты.</span><span class="sxs-lookup"><span data-stu-id="9375d-198">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9375d-199">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9375d-199">Az.Compute</span></span>
* <span data-ttu-id="9375d-200">Добавлена поддержка подстановочных знаков в командлетах Get.</span><span class="sxs-lookup"><span data-stu-id="9375d-200">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="9375d-201">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="9375d-201">Az.DataFactory</span></span>
* <span data-ttu-id="9375d-202">Обновлен пакет SDK для ADF .NET до версии 3.0.1.</span><span class="sxs-lookup"><span data-stu-id="9375d-202">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="9375d-203">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="9375d-203">Az.LogicApp</span></span>
* <span data-ttu-id="9375d-204">Исправлена проблема с получением только первой страницы результатов при выполнении команды ListWorkflows.</span><span class="sxs-lookup"><span data-stu-id="9375d-204">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="9375d-205">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9375d-205">Az.Network</span></span>
* <span data-ttu-id="9375d-206">Добавлена поддержка подстановочных знаков в командлетах Network.</span><span class="sxs-lookup"><span data-stu-id="9375d-206">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="9375d-207">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="9375d-207">Az.RecoveryServices</span></span>
* <span data-ttu-id="9375d-208">Добавлена поддержка SQL Server на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="9375d-208">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="9375d-209">Обновление пакета SDK</span><span class="sxs-lookup"><span data-stu-id="9375d-209">SDK Update</span></span>
* <span data-ttu-id="9375d-210">Удалена проверка VMappContainer в Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="9375d-210">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="9375d-211">Добавлены параметры Name и ServerName для Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="9375d-211">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="9375d-212">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9375d-212">Az.Resources</span></span>
* <span data-ttu-id="9375d-213">Добавлен параметр `-TemplateObject` в командлеты для развертывания.</span><span class="sxs-lookup"><span data-stu-id="9375d-213">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="9375d-214">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2933.</span><span class="sxs-lookup"><span data-stu-id="9375d-214">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="9375d-215">Устранена проблема с передачей в конвейер результата `Get-AzResource` для</span><span class="sxs-lookup"><span data-stu-id="9375d-215">Fix issue when piping the result of `Get-AzResource` to</span></span> `Set-AzResource`
    - <span data-ttu-id="9375d-216">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8240.</span><span class="sxs-lookup"><span data-stu-id="9375d-216">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="9375d-217">Устранена проблема с изменением типа данных JSON при выполнении</span><span class="sxs-lookup"><span data-stu-id="9375d-217">Fix issue with JSON data type change when running</span></span> `Set-AzResource`
    - <span data-ttu-id="9375d-218">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7930.</span><span class="sxs-lookup"><span data-stu-id="9375d-218">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="9375d-219">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9375d-219">Az.Sql</span></span>
* <span data-ttu-id="9375d-220">Обновление AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="9375d-220">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="9375d-221">Исправлено поведение для пограничного случая при создании параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="9375d-221">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="9375d-222">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="9375d-222">Az.Storage</span></span>
* <span data-ttu-id="9375d-223">Включена поддержка Kind BlockBlobStorage при создании учетной записи хранения для New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="9375d-223">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="9375d-224">1.4.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="9375d-224">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="9375d-225">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="9375d-225">Az.AnalysisServices</span></span>
* <span data-ttu-id="9375d-226">Командлет AddAzureASAccount устарел.</span><span class="sxs-lookup"><span data-stu-id="9375d-226">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="9375d-227">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="9375d-227">Az.Automation</span></span>
* <span data-ttu-id="9375d-228">Обновлена справка для командлета Import-AzAutomationDscNodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="9375d-228">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="9375d-229">Добавлена проверка имени конфигурации для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="9375d-229">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="9375d-230">Улучшена обработка ошибок для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="9375d-230">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="9375d-231">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="9375d-231">Az.CognitiveServices</span></span>
* <span data-ttu-id="9375d-232">Добавлен параметр CustomSubdomainName — новый необязательный параметр для командлета New-AzCognitiveServicesAccount, который указывает поддомен для ресурса.</span><span class="sxs-lookup"><span data-stu-id="9375d-232">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9375d-233">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9375d-233">Az.Compute</span></span>
* <span data-ttu-id="9375d-234">Устранена проблема с идентификаторами наборов параметров.</span><span class="sxs-lookup"><span data-stu-id="9375d-234">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="9375d-235">Обновлен командлет Get-AzVMExtension для отображения списка всех установленных расширений, если не указан параметр Name.</span><span class="sxs-lookup"><span data-stu-id="9375d-235">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="9375d-236">Для командлета Update-AzImage добавлены параметры Tag и ResourceId.</span><span class="sxs-lookup"><span data-stu-id="9375d-236">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="9375d-237">Командлет Get-AzVmssVM, который выполняется без указания идентификатора экземпляра и с параметром InstanceView, может выводить виртуальные машины из VMSS с представлением экземпляра.</span><span class="sxs-lookup"><span data-stu-id="9375d-237">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="9375d-238">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9375d-238">Az.DataLakeStore</span></span>
* <span data-ttu-id="9375d-239">Добавлены командлеты для перечисления и восстановления удаленного элемента ADL.</span><span class="sxs-lookup"><span data-stu-id="9375d-239">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="9375d-240">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="9375d-240">Az.EventHub</span></span>
* <span data-ttu-id="9375d-241">Добавлено новое логическое свойство SkipEmptyArchives для пропуска пустых архивов в классе CaptureDescription Eventhub.</span><span class="sxs-lookup"><span data-stu-id="9375d-241">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="9375d-242">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="9375d-242">Az.KeyVault</span></span>
* <span data-ttu-id="9375d-243">Исправлена расстановка тегов для командлета Set-AzKeyVaultSecret.</span><span class="sxs-lookup"><span data-stu-id="9375d-243">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="9375d-244">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="9375d-244">Az.LogicApp</span></span>
* <span data-ttu-id="9375d-245">Добавлен SKU "Базовый" для учетных записей интеграции.</span><span class="sxs-lookup"><span data-stu-id="9375d-245">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="9375d-246">Добавлены типы сопоставлений Liquid, а также XSLT 2.0 и XSLT 3.0.</span><span class="sxs-lookup"><span data-stu-id="9375d-246">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="9375d-247">Новые командлеты для сборок учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="9375d-247">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="9375d-248">Get-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="9375d-248">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="9375d-249">New-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="9375d-249">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="9375d-250">Remove-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="9375d-250">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="9375d-251">Set-AzIntegrationAccountAssembly.</span><span class="sxs-lookup"><span data-stu-id="9375d-251">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="9375d-252">Новые командлеты для конфигурации пакета учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="9375d-252">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="9375d-253">Get-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="9375d-253">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="9375d-254">New-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="9375d-254">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="9375d-255">Remove-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="9375d-255">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="9375d-256">Set-AzIntegrationAccountBatchConfiguration.</span><span class="sxs-lookup"><span data-stu-id="9375d-256">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="9375d-257">Обновлен пакет SDK Logic Apps до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="9375d-257">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="9375d-258">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="9375d-258">Az.Monitor</span></span>
* <span data-ttu-id="9375d-259">Обновлена справка для командлета Get-AzMetric.</span><span class="sxs-lookup"><span data-stu-id="9375d-259">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="9375d-260">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9375d-260">Az.Network</span></span>
* <span data-ttu-id="9375d-261">Обновлен пример справки для командлета Add-AzApplicationGatewayCustomError.</span><span class="sxs-lookup"><span data-stu-id="9375d-261">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="9375d-262">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="9375d-262">Az.OperationalInsights</span></span>
* <span data-ttu-id="9375d-263">Дополнительная поддержка создания и получения источников данных ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="9375d-263">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="9375d-264">Добавлен новый тип ApplicationInsights для получения определенных или всех источников данных ApplicationInsights для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="9375d-264">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="9375d-265">Добавлен командлет New-AzOperationalInsightsApplicationInsightsDataSource для создания источника данных с использованием параметров указанного ресурса Application-Insightss: subscription Id, resourceGroupName и name.</span><span class="sxs-lookup"><span data-stu-id="9375d-265">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="9375d-266">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9375d-266">Az.Resources</span></span>
* <span data-ttu-id="9375d-267">исправлена проблема https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="9375d-267">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="9375d-268">исправлена проблема https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="9375d-268">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="9375d-269">исправлена проблема https://github.com/Azure/azure-powershell/issues/6219.</span><span class="sxs-lookup"><span data-stu-id="9375d-269">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="9375d-270">Исправлена ошибка, препятствующая повторному созданию KeyCredentials.</span><span class="sxs-lookup"><span data-stu-id="9375d-270">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="9375d-271">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9375d-271">Az.Sql</span></span>
* <span data-ttu-id="9375d-272">Добавлена поддержка уровня гипермасштабирования в базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="9375d-272">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="9375d-273">Исправлена ошибка, из-за которой восстановление могло завершиться со сбоем при указании ненужных свойств в запросе на восстановление.</span><span class="sxs-lookup"><span data-stu-id="9375d-273">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="9375d-274">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="9375d-274">Az.Websites</span></span>
* <span data-ttu-id="9375d-275">Исправлен пример для командлета Get-AzWebAppSlotMetrics.</span><span class="sxs-lookup"><span data-stu-id="9375d-275">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="9375d-276">1.3.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="9375d-276">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="9375d-277">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9375d-277">Az.Accounts</span></span>
* <span data-ttu-id="9375d-278">Обновление до последней версии ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="9375d-278">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="9375d-279">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="9375d-279">Az.AnalysisServices</span></span>
<span data-ttu-id="9375d-280">Общедоступная версия модуля Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="9375d-280">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9375d-281">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9375d-281">Az.Compute</span></span>
* <span data-ttu-id="9375d-282">Расширение AEM: добавлена поддержка дисков UltraSSD, P60, P70 и P80.</span><span class="sxs-lookup"><span data-stu-id="9375d-282">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="9375d-283">Обновлено описание справки для командлета Set-AzVMBootDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="9375d-283">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="9375d-284">Обновлено описание справки и пример для командлета Update-AzImage.</span><span class="sxs-lookup"><span data-stu-id="9375d-284">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="9375d-285">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="9375d-285">Az.RecoveryServices</span></span>
<span data-ttu-id="9375d-286">Общедоступная версия модуля Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="9375d-286">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="9375d-287">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9375d-287">Az.Resources</span></span>
* <span data-ttu-id="9375d-288">Исправлена расстановка тегов для групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9375d-288">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="9375d-289">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="9375d-289">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="9375d-290">Исправлена проблема с игнорированием командлетом `Get-AzureRmRoleAssignment` параметра -ErrorAction.</span><span class="sxs-lookup"><span data-stu-id="9375d-290">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="9375d-291">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="9375d-291">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="9375d-292">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9375d-292">Az.Sql</span></span>
* <span data-ttu-id="9375d-293">Добавлен командлет Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="9375d-293">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="9375d-294">Исправлена проблема с появлением исключения NullRef при выполнении командлетов SQL, если не выполнен вход в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="9375d-294">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="9375d-295">Исправлено исключение NullRef в командлете Get-AzSqlCapability.</span><span class="sxs-lookup"><span data-stu-id="9375d-295">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="9375d-296">1.2.1 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="9375d-296">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="9375d-297">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9375d-297">Az.Accounts</span></span>
* <span data-ttu-id="9375d-298">Выпуск с правильной версией службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="9375d-298">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="9375d-299">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="9375d-299">Az.AnalysisServices</span></span>
* <span data-ttu-id="9375d-300">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="9375d-300">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="9375d-301">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="9375d-301">Az.RecoveryServices</span></span>
* <span data-ttu-id="9375d-302">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="9375d-302">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="9375d-303">1.2.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="9375d-303">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="9375d-304">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9375d-304">Az.Accounts</span></span>
* <span data-ttu-id="9375d-305">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="9375d-305">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="9375d-306">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="9375d-306">Update incorrect online help URLs</span></span>
* <span data-ttu-id="9375d-307">Добавлено предупреждающее сообщение в PS Core для модуля Uninstall-AzureRm.</span><span class="sxs-lookup"><span data-stu-id="9375d-307">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="9375d-308">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="9375d-308">Az.Aks</span></span>
* <span data-ttu-id="9375d-309">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="9375d-309">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="9375d-310">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="9375d-310">Az.Automation</span></span>
* <span data-ttu-id="9375d-311">Добавлена поддержка для модулей runbook Python 2.</span><span class="sxs-lookup"><span data-stu-id="9375d-311">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="9375d-312">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="9375d-312">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="9375d-313">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="9375d-313">Az.Cdn</span></span>
* <span data-ttu-id="9375d-314">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="9375d-314">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9375d-315">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9375d-315">Az.Compute</span></span>
* <span data-ttu-id="9375d-316">Добавлен командлет Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="9375d-316">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="9375d-317">Добавлен параметр TempDisk к командлету Set-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="9375d-317">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="9375d-318">Исправлено предупреждающее сообщение командлета New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="9375d-318">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="9375d-319">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="9375d-319">Az.ContainerRegistry</span></span>
* <span data-ttu-id="9375d-320">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="9375d-320">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="9375d-321">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="9375d-321">Az.DataFactory</span></span>
* <span data-ttu-id="9375d-322">Пакет SDK ADF .Net обновлен до версии 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="9375d-322">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="9375d-323">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9375d-323">Az.DataLakeStore</span></span>
* <span data-ttu-id="9375d-324">Исправлена проблема с конечной точкой ADLS при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="9375d-324">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="9375d-325">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7462.</span><span class="sxs-lookup"><span data-stu-id="9375d-325">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="9375d-326">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="9375d-326">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="9375d-327">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="9375d-327">Az.IotHub</span></span>
* <span data-ttu-id="9375d-328">Добавлен формат кодирования для командлета Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="9375d-328">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="9375d-329">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="9375d-329">Az.KeyVault</span></span>
* <span data-ttu-id="9375d-330">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="9375d-330">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="9375d-331">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9375d-331">Az.Network</span></span>
* <span data-ttu-id="9375d-332">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="9375d-332">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="9375d-333">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9375d-333">Az.Resources</span></span>
* <span data-ttu-id="9375d-334">Исправлены неправильные примеры в справочной документации по командлетам New-AzADAppCredential и New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="9375d-334">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="9375d-335">Исправлена проблема, при которой путь для параметра -TemplateFile не удавалось разрешить до выполнения командлетов развертывания групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9375d-335">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="9375d-336">Az.Resources: исправлена документация для значения по умолчанию -Mode командлета New-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="9375d-336">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="9375d-337">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/7522.</span><span class="sxs-lookup"><span data-stu-id="9375d-337">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="9375d-338">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/5747.</span><span class="sxs-lookup"><span data-stu-id="9375d-338">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="9375d-339">Исправлена проблема с форматированием объекта PSResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="9375d-339">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="9375d-340">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2123.</span><span class="sxs-lookup"><span data-stu-id="9375d-340">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="9375d-341">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="9375d-341">Az.ServiceFabric</span></span>
* <span data-ttu-id="9375d-342">Исправлена проблема с появлением исключения в процессе отката при добавлении сертификата к модели VMSS: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="9375d-342">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="9375d-343">Исправлены некоторые сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="9375d-343">Fix some error messages.</span></span>
* <span data-ttu-id="9375d-344">Исправлена проблема с созданием кластера с шаблоном ARM по умолчанию для командлета New-AzServiceFabriCluster, который не работал с операцией миграции в Az.</span><span class="sxs-lookup"><span data-stu-id="9375d-344">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="9375d-345">Исправлена проблема с добавлением сертификата кластера или приложения: теперь они добавляются только в Масштабируемые наборы виртуальных машин, которые сопоставлены с кластером, путем проверки идентификатора кластера в расширении.</span><span class="sxs-lookup"><span data-stu-id="9375d-345">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="9375d-346">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="9375d-346">Az.SignalR</span></span>
* <span data-ttu-id="9375d-347">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="9375d-347">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="9375d-348">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9375d-348">Az.Sql</span></span>
* <span data-ttu-id="9375d-349">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="9375d-349">Update incorrect online help URLs</span></span>
* <span data-ttu-id="9375d-350">Обновлено описание параметра LicenseType с добавлением возможных значений.</span><span class="sxs-lookup"><span data-stu-id="9375d-350">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="9375d-351">Исправлена проблема с неправильным обновлением удостоверения управляемого экземпляра, если оно было единственным обновляемым свойством.</span><span class="sxs-lookup"><span data-stu-id="9375d-351">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="9375d-352">Поддержка пользовательских параметров сортировки в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="9375d-352">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="9375d-353">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="9375d-353">Az.Storage</span></span>
* <span data-ttu-id="9375d-354">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="9375d-354">Update incorrect online help URLs</span></span>
* <span data-ttu-id="9375d-355">Добавлен вывод подробных сообщений об ошибке при получении или установке классических свойств ведения журнала или метрик в учетной записи хранилища класса Premium, так как учетная запись хранилища класса Premium не поддерживает классические функции ведения журнала и метрик.</span><span class="sxs-lookup"><span data-stu-id="9375d-355">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="9375d-356">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="9375d-356">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="9375d-357">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="9375d-357">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="9375d-358">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="9375d-358">Az.TrafficManager</span></span>
* <span data-ttu-id="9375d-359">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="9375d-359">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="9375d-360">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="9375d-360">Az.Websites</span></span>
* <span data-ttu-id="9375d-361">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="9375d-361">Update incorrect online help URLs</span></span>
* <span data-ttu-id="9375d-362">Исправлена работа командлета New-AzWebAppSSLBinding: сертификат отправляется в правильную группу ресурсов и правильное расположение, если приложение размещено в ASE.</span><span class="sxs-lookup"><span data-stu-id="9375d-362">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="9375d-363">Исправлена работа командлета New-AzWebAppSSLBinding: теги не перезаписываются при привязке SSL-сертификата к приложению.</span><span class="sxs-lookup"><span data-stu-id="9375d-363">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="9375d-364">1.1.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="9375d-364">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="9375d-365">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9375d-365">Az.Accounts</span></span>
* <span data-ttu-id="9375d-366">Добавление области "Local" в Enable-AzureRmAlias.</span><span class="sxs-lookup"><span data-stu-id="9375d-366">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9375d-367">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9375d-367">Az.Compute</span></span>
* <span data-ttu-id="9375d-368">Теперь имя не является обязательным в идентификаторе набора параметров для Restart/Start/Stop/Remove/Set-AzVM и Save-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="9375d-368">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="9375d-369">Обновлено описание идентификатора в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="9375d-369">Updated the description of ID in help files</span></span>
* <span data-ttu-id="9375d-370">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="9375d-370">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="9375d-371">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9375d-371">Az.DataLakeStore</span></span>
* <span data-ttu-id="9375d-372">Обновление версии пакета SDK для плоскости данных до 1.1.14 для устранения найденных проблем.</span><span class="sxs-lookup"><span data-stu-id="9375d-372">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="9375d-373">Исправлена обработка отрицательного времени доступа и времени изменения для getfilestatus и liststatus, исправлен токен отмены для асинхронных методов.</span><span class="sxs-lookup"><span data-stu-id="9375d-373">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="9375d-374">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="9375d-374">Az.EventGrid</span></span>
* <span data-ttu-id="9375d-375">Обновление для использования API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="9375d-375">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="9375d-376">Обновлены указанные ниже командлеты для поддержки нового сценария в API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="9375d-376">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="9375d-377">New-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="9375d-377">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="9375d-378">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="9375d-378">Event Time-To-Live,</span></span>
        - <span data-ttu-id="9375d-379">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="9375d-379">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="9375d-380">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="9375d-380">Dead letter endpoint.</span></span>
    - <span data-ttu-id="9375d-381">Update-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="9375d-381">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="9375d-382">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="9375d-382">Event Time-To-Live,</span></span>
        - <span data-ttu-id="9375d-383">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="9375d-383">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="9375d-384">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="9375d-384">Dead letter endpoint.</span></span>
* <span data-ttu-id="9375d-385">Для параметра EndpointType добавлены новые значения перечисления (storageQueue и hybridConnection) в командлеты New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="9375d-385">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="9375d-386">Если ожидается, что создание или обновление подписки на событие повлечет за собой действия со стороны пользователя, выполняемые вручную, отображается предупреждение при создании или обновлении подписки события.</span><span class="sxs-lookup"><span data-stu-id="9375d-386">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="9375d-387">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="9375d-387">Az.IotHub</span></span>
* <span data-ttu-id="9375d-388">Пакет SDK Центра Интернета вещей обновлен до последней версии.</span><span class="sxs-lookup"><span data-stu-id="9375d-388">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="9375d-389">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="9375d-389">Az.LogicApp</span></span>
* <span data-ttu-id="9375d-390">Get-AzLogicApp позволяет перечислить все параметры без указанного имени.</span><span class="sxs-lookup"><span data-stu-id="9375d-390">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="9375d-391">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9375d-391">Az.Resources</span></span>
* <span data-ttu-id="9375d-392">Исправлена проблема с набором параметров при предоставлении параметров "-ODataQuery" и "-ResourceId" для "Get-AzResource".</span><span class="sxs-lookup"><span data-stu-id="9375d-392">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="9375d-393">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7875.</span><span class="sxs-lookup"><span data-stu-id="9375d-393">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="9375d-394">Исправлена обработка параметра -Custom в New/Set-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="9375d-394">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="9375d-395">Исправлена опечатка в документации по New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="9375d-395">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="9375d-396">Параметр "-MailNickname" стал обязательным для "New-AzADUser".</span><span class="sxs-lookup"><span data-stu-id="9375d-396">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="9375d-397">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8220.</span><span class="sxs-lookup"><span data-stu-id="9375d-397">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="9375d-398">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="9375d-398">Az.SignalR</span></span>
* <span data-ttu-id="9375d-399">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="9375d-399">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="9375d-400">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9375d-400">Az.Sql</span></span>
* <span data-ttu-id="9375d-401">Зависимость клиента управления хранением преобразована для общей реализации в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="9375d-401">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="9375d-402">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="9375d-402">Az.Storage</span></span>
* <span data-ttu-id="9375d-403">Установка параметра StorageAccountName для контекста хранилища в качестве реального имени учетной записи хранения, если она была создана с использованием токена Sas, OAuth или анонимного доступа.</span><span class="sxs-lookup"><span data-stu-id="9375d-403">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="9375d-404">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="9375d-404">New-AzStorageContext</span></span>
* <span data-ttu-id="9375d-405">Создание токена Sas большого двоичного объекта моментального снимка с параметром "-FullUri". Возвращаемый URI исправлен на URI моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="9375d-405">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="9375d-406">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="9375d-406">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="9375d-407">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="9375d-407">Az.Websites</span></span>
* <span data-ttu-id="9375d-408">Исправлена ошибка синтаксического анализа даты в "Get-AzDeletedWebApp".</span><span class="sxs-lookup"><span data-stu-id="9375d-408">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="9375d-409">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="9375d-409">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="9375d-410">1.0.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="9375d-410">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="9375d-411">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="9375d-411">General</span></span>

- <span data-ttu-id="9375d-412">Общедоступная версия модуля Az.</span><span class="sxs-lookup"><span data-stu-id="9375d-412">General Availability of Az Module</span></span>
- <span data-ttu-id="9375d-413">Справка в Интернете для каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="9375d-413">Online help for each module</span></span>
- <span data-ttu-id="9375d-414">Дополнительные сведения и стратегию развития см. в статье [Announcing New Module 'Az'](https://aka.ms/azps-announce) (Объявление о новом модуле Az)</span><span class="sxs-lookup"><span data-stu-id="9375d-414">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="9375d-415">Сведения о миграции с AzureRM см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="9375d-415">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="9375d-416">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9375d-416">Az.Accounts</span></span>
- <span data-ttu-id="9375d-417">Изменено с Az.Profile.</span><span class="sxs-lookup"><span data-stu-id="9375d-417">Changed from Az.Profile</span></span>
- <span data-ttu-id="9375d-418">Исправлены форматы таблиц для типов профиля и контекста.</span><span class="sxs-lookup"><span data-stu-id="9375d-418">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="9375d-419">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="9375d-419">Az.ApiManagement</span></span>
- <span data-ttu-id="9375d-420">Исправления для #7002.</span><span class="sxs-lookup"><span data-stu-id="9375d-420">Fixes for #7002</span></span>
- <span data-ttu-id="9375d-421">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="9375d-421">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="9375d-422">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="9375d-422">Az.Batch</span></span>
- <span data-ttu-id="9375d-423">Добавлена возможность видеть, какая версия агента узла пакетной службы Azure работает в пуле на каждой виртуальной машине, с помощью нового свойства `NodeAgentInformation` в `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="9375d-423">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="9375d-424">Значение `Caching` по умолчанию для `PSDataDisk` теперь `ReadWrite` вместо `None`.</span><span class="sxs-lookup"><span data-stu-id="9375d-424">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="9375d-425">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="9375d-425">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="9375d-426">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="9375d-426">Az.Billing</span></span>
- <span data-ttu-id="9375d-427">Объединены командлеты Billing, Consumption и UsageAggregates. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0).</span><span class="sxs-lookup"><span data-stu-id="9375d-427">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="9375d-428">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="9375d-428">Az.CognitivServices</span></span>
- <span data-ttu-id="9375d-429">Добавлены средства заполнения для SkuName и Typem, доступные в операции New-AzureRmCognitiveServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="9375d-429">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="9375d-430">Удален набор параметров GetSkusWithAccountParamSetName из Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="9375d-430">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="9375d-431">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="9375d-431">Az.ContainerInstance</span></span>
- <span data-ttu-id="9375d-432">Добавлена поддержка ManagedIdentity.</span><span class="sxs-lookup"><span data-stu-id="9375d-432">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="9375d-433">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="9375d-433">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="9375d-434">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="9375d-434">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="9375d-435">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9375d-435">Az.DataLakeStore</span></span>
- <span data-ttu-id="9375d-436">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="9375d-436">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="9375d-437">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="9375d-437">Az.Monitor</span></span>
- <span data-ttu-id="9375d-438">"Az.Insights" переименован в "Az.Monitor" и внесены другие незначительные критические изменения. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="9375d-438">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="9375d-439">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="9375d-439">Az.KeyVault</span></span>
- <span data-ttu-id="9375d-440">Из типов вывода удалено устаревшее свойство PurgeDisabled</span><span class="sxs-lookup"><span data-stu-id="9375d-440">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="9375d-441">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="9375d-441">Az.MachineLearning</span></span>
- <span data-ttu-id="9375d-442">Включены командлеты из модуля Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="9375d-442">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="9375d-443">Az.Media</span><span class="sxs-lookup"><span data-stu-id="9375d-443">Az.Media</span></span>
- <span data-ttu-id="9375d-444">Удаляет устаревший псевдоним Tags из New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="9375d-444">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="9375d-445">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9375d-445">Az.Network</span></span>
<span data-ttu-id="9375d-446">В шлюз приложений добавлена поддержка настройки RewriteRuleSets</span><span class="sxs-lookup"><span data-stu-id="9375d-446">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="9375d-447">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="9375d-447">New cmdlets added:</span></span>
        - <span data-ttu-id="9375d-448">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9375d-448">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="9375d-449">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9375d-449">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="9375d-450">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9375d-450">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="9375d-451">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9375d-451">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="9375d-452">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9375d-452">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="9375d-453">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="9375d-453">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="9375d-454">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="9375d-454">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="9375d-455">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="9375d-455">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="9375d-456">В следующие командлеты добавлен необязательный параметр -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9375d-456">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="9375d-457">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9375d-457">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="9375d-458">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="9375d-458">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="9375d-459">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="9375d-459">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="9375d-460">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9375d-460">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="9375d-461">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9375d-461">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="9375d-462">New-AzureRmApplicationGatewayUrlPathMapConfig добавил с помощью идентификатора поддержку KeyVault для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="9375d-462">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="9375d-463">В следующие командлеты добавлен необязательный параметр -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="9375d-463">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="9375d-464">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9375d-464">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="9375d-465">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9375d-465">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="9375d-466">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9375d-466">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="9375d-467">В командлет New-AzApplicationGateway добавлен необязательный параметр -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="9375d-467">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="9375d-468">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="9375d-468">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="9375d-469">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="9375d-469">Az.OperationalInsights</span></span>
- <span data-ttu-id="9375d-470">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="9375d-470">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="9375d-471">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="9375d-471">Az.Profile</span></span>
- <span data-ttu-id="9375d-472">Имя модуля изменено на Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="9375d-472">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="9375d-473">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="9375d-473">Az.RecoveryServices</span></span>
- <span data-ttu-id="9375d-474">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="9375d-474">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="9375d-475">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9375d-475">Az.Resources</span></span>
- <span data-ttu-id="9375d-476">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="9375d-476">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="9375d-477">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="9375d-477">Az.ServiceFabric</span></span>
- <span data-ttu-id="9375d-478">Поддержка спецификации сертификата по общему имени и отпечатку</span><span class="sxs-lookup"><span data-stu-id="9375d-478">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="9375d-479">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="9375d-479">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="9375d-480">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="9375d-480">Az.SIgnalR</span></span>
- <span data-ttu-id="9375d-481">Общедоступная версия командлетов PowerShell для SIgnalR</span><span class="sxs-lookup"><span data-stu-id="9375d-481">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="9375d-482">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9375d-482">Az.Sql</span></span>
- <span data-ttu-id="9375d-483">Добавлены новые типы обнаружения Data_Exfiltration и Unsafe_Action в командлеты обнаружения угроз</span><span class="sxs-lookup"><span data-stu-id="9375d-483">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="9375d-484">Примеры обновленной документации для командлетов аудита Sql</span><span class="sxs-lookup"><span data-stu-id="9375d-484">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="9375d-485">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="9375d-485">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="9375d-486">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="9375d-486">Az.Storage</span></span>
- <span data-ttu-id="9375d-487">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="9375d-487">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="9375d-488">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="9375d-488">Az.Websites</span></span>
- <span data-ttu-id="9375d-489">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="9375d-489">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="9375d-490">0.7.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="9375d-490">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="9375d-491">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="9375d-491">General</span></span>

* <span data-ttu-id="9375d-492">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="9375d-492">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="9375d-493">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9375d-493">Az.Compute</span></span>

* <span data-ttu-id="9375d-494">Добавлена поддержка UltraSSD и образов коллекции в простых наборах параметров для командлетов `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="9375d-494">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="9375d-495">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9375d-495">Az.DataLakeStore</span></span>

* <span data-ttu-id="9375d-496">Исправлено косую черту в конце домена учетной записи ADLS</span><span class="sxs-lookup"><span data-stu-id="9375d-496">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="9375d-497">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="9375d-497">Az.FrontDoor</span></span>

* <span data-ttu-id="9375d-498">Исправлены некоторые неработающие ссылки</span><span class="sxs-lookup"><span data-stu-id="9375d-498">Fixed some broken links</span></span>
    - <span data-ttu-id="9375d-499">В статьях New-AzureRmFrontDoor и Set-AzureRmFrontDoor исправлена ссылка на статью командлета New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="9375d-499">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="9375d-500">В статье New-AzureRmFrontDoorManagedRuleObject исправлена ссылка на статью командлета New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="9375d-500">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="9375d-501">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="9375d-501">Az.RecoveryServices</span></span>

* <span data-ttu-id="9375d-502">Добавлены проверки на стороне клиента для операций восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="9375d-502">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="9375d-503">StorageAccountName и storageAccountResourceGroupName являются необязательными для восстановления afs.</span><span class="sxs-lookup"><span data-stu-id="9375d-503">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="9375d-504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9375d-504">Az.Resources</span></span>

* <span data-ttu-id="9375d-505">Исправление для https://github.com/Azure/azure-powershell/issues/7679.</span><span class="sxs-lookup"><span data-stu-id="9375d-505">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="9375d-506">Обновите Get-AzureRmRoleAssignment, чтобы использовать область подписки, если она указана при запросе классических администраторов.</span><span class="sxs-lookup"><span data-stu-id="9375d-506">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="9375d-507">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9375d-507">Az.Sql</span></span>

* <span data-ttu-id="9375d-508">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="9375d-508">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="9375d-509">Устранена проблема с использованием Get-AzureRmSqlDatabaseVulnerabilityAssessment с .NET Core.</span><span class="sxs-lookup"><span data-stu-id="9375d-509">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="9375d-510">Изменена документация справочных сообщений, связанных с командлетами аудита SQL.</span><span class="sxs-lookup"><span data-stu-id="9375d-510">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="9375d-511">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="9375d-511">Az.Storage</span></span>

* <span data-ttu-id="9375d-512">Добавлено -EnableHierarchicalNamespace к New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9375d-512">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="9375d-513">Устранена проблема, из-за которой командлет Copy File не может повторно использовать исходный контекст в пункте назначения, если не введен -DestContext</span><span class="sxs-lookup"><span data-stu-id="9375d-513">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="9375d-514">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="9375d-514">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="9375d-515">Поддержка статической конфигурации сайта</span><span class="sxs-lookup"><span data-stu-id="9375d-515">Support Static Website configuration</span></span>
    - <span data-ttu-id="9375d-516">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="9375d-516">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="9375d-517">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="9375d-517">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="9375d-518">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="9375d-518">Az.Websites</span></span>

* <span data-ttu-id="9375d-519">Set-AzureRmWebApp и Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9375d-519">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="9375d-520">Добавлен новый параметр (-AzureStoragePath), который указывает путь службы хранилища Azure для подключения в приложениях-контейнерах Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="9375d-520">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="9375d-521">Используйте выходные данные нового командлета New-AzureRmWebAppAzureStoragePath в качестве параметра, чтобы задать пути к службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="9375d-521">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="9375d-522">0.6.1 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="9375d-522">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="9375d-523">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="9375d-523">Az.ApiManagement</span></span>
* <span data-ttu-id="9375d-524">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="9375d-524">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="9375d-525">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="9375d-525">Az.Automation</span></span>
* <span data-ttu-id="9375d-526">Командлеты службы автоматизации Azure на базе Swagger.</span><span class="sxs-lookup"><span data-stu-id="9375d-526">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="9375d-527">Добавлены командлеты для Управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="9375d-527">Added Update Management cmdlets</span></span>
* <span data-ttu-id="9375d-528">Добавлены командлеты для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="9375d-528">Added Source Control cmdlets</span></span>
* <span data-ttu-id="9375d-529">Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="9375d-529">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="9375d-530">Исправлена команда DSC для регистрации узла.</span><span class="sxs-lookup"><span data-stu-id="9375d-530">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="9375d-531">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9375d-531">Az.Compute</span></span>
* <span data-ttu-id="9375d-532">Исправлена проблема с удостоверением, назначаемым системой.</span><span class="sxs-lookup"><span data-stu-id="9375d-532">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="9375d-533">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="9375d-533">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="9375d-534">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="9375d-534">Az.ContainerInstance</span></span>
* <span data-ttu-id="9375d-535">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="9375d-535">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="9375d-536">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="9375d-536">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="9375d-537">Обновлено описание в примерах командлетов для Marketplace.</span><span class="sxs-lookup"><span data-stu-id="9375d-537">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="9375d-538">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9375d-538">Az.Network</span></span>
* <span data-ttu-id="9375d-539">Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="9375d-539">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="9375d-540">Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="9375d-540">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="9375d-541">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="9375d-541">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="9375d-542">Исправлены проблемы с использованием памяти в карте виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="9375d-542">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="9375d-543">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="9375d-543">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="9375d-544">Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="9375d-544">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="9375d-545">Параметры часового пояса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="9375d-545">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="9375d-546">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="9375d-546">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="9375d-547">Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="9375d-547">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="9375d-548">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="9375d-548">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="9375d-549">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="9375d-549">Az.Relay</span></span>
* <span data-ttu-id="9375d-550">Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.</span><span class="sxs-lookup"><span data-stu-id="9375d-550">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="9375d-551">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9375d-551">Az.Resources</span></span>
* <span data-ttu-id="9375d-552">Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и</span><span class="sxs-lookup"><span data-stu-id="9375d-552">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and</span></span> `Set-AzureRmPolicyAssignment`
* <span data-ttu-id="9375d-553">Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.</span><span class="sxs-lookup"><span data-stu-id="9375d-553">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="9375d-554">Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.</span><span class="sxs-lookup"><span data-stu-id="9375d-554">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="9375d-555">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="9375d-555">Az.ServiceFabric</span></span>
* <span data-ttu-id="9375d-556">Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.</span><span class="sxs-lookup"><span data-stu-id="9375d-556">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="9375d-557">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9375d-557">Az.Sql</span></span>
* <span data-ttu-id="9375d-558">Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="9375d-558">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="9375d-559">Get-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="9375d-559">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="9375d-560">New-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="9375d-560">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="9375d-561">Set-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="9375d-561">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="9375d-562">Remove-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="9375d-562">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="9375d-563">Get-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="9375d-563">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="9375d-564">New-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="9375d-564">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="9375d-565">Restore-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="9375d-565">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="9375d-566">Remove-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="9375d-566">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="9375d-567">Добавлено расширенное управление политиками аудита для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="9375d-567">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="9375d-568">Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="9375d-568">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="9375d-569">Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.</span><span class="sxs-lookup"><span data-stu-id="9375d-569">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="9375d-570">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="9375d-570">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="9375d-571">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="9375d-571">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="9375d-572">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="9375d-572">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="9375d-573">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="9375d-573">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="9375d-574">Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="9375d-574">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="9375d-575">0.5.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="9375d-575">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="9375d-576">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="9375d-576">General</span></span>
* <span data-ttu-id="9375d-577">Добавлены средства заполнения ресурсов для многих основных командлетов — они позволяют вам переключать существующие имена ресурсов при вызове командлетов в интерактивном режиме</span><span class="sxs-lookup"><span data-stu-id="9375d-577">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="9375d-578">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="9375d-578">Az.Profile</span></span>
* <span data-ttu-id="9375d-579">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9375d-579">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="9375d-580">В командлете Connect-AzAccount параметр TenantId переименован в Tenant и добавлен псевдоним для TenantId</span><span class="sxs-lookup"><span data-stu-id="9375d-580">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="9375d-581">Обновлено описание TenantId для командлета Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="9375d-581">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="9375d-582">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="9375d-582">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="9375d-583">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="9375d-583">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="9375d-584">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="9375d-584">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="9375d-585">Устранена проблема, при которой командлет Disconnect-AzAccount вызывал сбой при отсутствии подключения</span><span class="sxs-lookup"><span data-stu-id="9375d-585">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="9375d-586">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="9375d-586">Az.CognitiveServices</span></span>
* <span data-ttu-id="9375d-587">Добавлена операция Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="9375d-587">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9375d-588">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9375d-588">Az.Compute</span></span>
* <span data-ttu-id="9375d-589">Добавлены командлеты Add-AzVmssVMDataDisk и Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="9375d-589">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="9375d-590">Get-AzVMImage отображает AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="9375d-590">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="9375d-591">Устранена проблема, при которой значения параметров SetAzVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="9375d-591">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="9375d-592">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9375d-592">Az.DataLakeStore</span></span>
* <span data-ttu-id="9375d-593">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="9375d-593">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="9375d-594">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="9375d-594">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="9375d-595">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="9375d-595">Az.Insights</span></span>
* <span data-ttu-id="9375d-596">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="9375d-596">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="9375d-597">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="9375d-597">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="9375d-598">Исправлена проблема № 7513 [Insights], при которой для командлета Set-AzDiagnosticSetting требовалось явное указание категорий во время создания параметра</span><span class="sxs-lookup"><span data-stu-id="9375d-598">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="9375d-599">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="9375d-599">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="9375d-600">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9375d-600">Az.Network</span></span>
* <span data-ttu-id="9375d-601">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="9375d-601">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="9375d-602">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="9375d-602">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="9375d-603">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="9375d-603">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="9375d-604">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="9375d-604">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="9375d-605">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="9375d-605">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="9375d-606">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="9375d-606">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="9375d-607">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="9375d-607">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="9375d-608">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="9375d-608">Az.PolicyInsights</span></span>
* <span data-ttu-id="9375d-609">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="9375d-609">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="9375d-610">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9375d-610">Az.Resources</span></span>
* <span data-ttu-id="9375d-611">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="9375d-611">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="9375d-612">Разрешено перечисление ресурсов с помощью параметра -ResourceId для командлета Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="9375d-612">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="9375d-613">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="9375d-613">Az.ServiceBus</span></span>
* <span data-ttu-id="9375d-614">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="9375d-614">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="9375d-615">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="9375d-615">Az.ServiceFabric</span></span>
* <span data-ttu-id="9375d-616">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="9375d-616">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="9375d-617">Исправлен командлет Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="9375d-617">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="9375d-618">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="9375d-618">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="9375d-619">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="9375d-619">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="9375d-620">Исправлен командлет Update-AzServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="9375d-620">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="9375d-621">0.4.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="9375d-621">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="9375d-622">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="9375d-622">Az.Profile</span></span>
* <span data-ttu-id="9375d-623">Устранена проблема с Get-AzSubscription в CloudShell</span><span class="sxs-lookup"><span data-stu-id="9375d-623">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="9375d-624">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9375d-624">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9375d-625">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9375d-625">Az.Compute</span></span>
* <span data-ttu-id="9375d-626">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzVm</span><span class="sxs-lookup"><span data-stu-id="9375d-626">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="9375d-627">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="9375d-627">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="9375d-628">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9375d-628">Az.DataLakeStore</span></span>
* <span data-ttu-id="9375d-629">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="9375d-629">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="9375d-630">Get-AzDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9375d-630">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="9375d-631">Add-AzDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9375d-631">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="9375d-632">Set-AzDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9375d-632">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="9375d-633">Remove-AzDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9375d-633">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="9375d-634">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9375d-634">Az.Network</span></span>
* <span data-ttu-id="9375d-635">Обновлен командлет Test-AzNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="9375d-635">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="9375d-636">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="9375d-636">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="9375d-637">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9375d-637">Az.Resources</span></span>
* <span data-ttu-id="9375d-638">Устранена проблема, из-за которой командлет Get-AzRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), благодаря добавлению понятного исключения в сценарий.</span><span class="sxs-lookup"><span data-stu-id="9375d-638">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="9375d-639">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="9375d-639">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="9375d-640">0.3.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="9375d-640">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="9375d-641">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="9375d-641">Azure.Storage</span></span>
* <span data-ttu-id="9375d-642">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="9375d-642">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="9375d-643">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="9375d-643">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="9375d-644">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="9375d-644">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="9375d-645">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="9375d-645">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="9375d-646">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="9375d-646">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="9375d-647">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="9375d-647">Az.CognitiveServices</span></span>
* <span data-ttu-id="9375d-648">Поддержка Get-AzCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="9375d-648">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9375d-649">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9375d-649">Az.Compute</span></span>
* <span data-ttu-id="9375d-650">Исправлена команда Get-AzVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов</span><span class="sxs-lookup"><span data-stu-id="9375d-650">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="9375d-651">Добавлен пример использования SimpleParameterSet в справку командлета New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="9375d-651">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="9375d-652">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="9375d-652">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="9375d-653">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="9375d-653">Az.DataFactoryV2</span></span>
* <span data-ttu-id="9375d-654">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="9375d-654">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="9375d-655">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9375d-655">Az.Network</span></span>
* <span data-ttu-id="9375d-656">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="9375d-656">Added NetworkProfile functionality.</span></span> <span data-ttu-id="9375d-657">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="9375d-657">new cmdlets added</span></span>
    - <span data-ttu-id="9375d-658">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="9375d-658">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="9375d-659">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="9375d-659">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="9375d-660">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="9375d-660">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="9375d-661">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="9375d-661">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="9375d-662">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="9375d-662">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="9375d-663">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="9375d-663">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="9375d-664">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="9375d-664">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="9375d-665">Добавлены командлеты: New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="9375d-665">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="9375d-666">Добавлены командлеты: Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="9375d-666">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="9375d-667">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="9375d-667">Az.RedisCache</span></span>
* <span data-ttu-id="9375d-668">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="9375d-668">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="9375d-669">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="9375d-669">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="9375d-670">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9375d-670">Az.Resources</span></span>
* <span data-ttu-id="9375d-671">Добавлен отсутствующий параметр -Mode в командлет Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="9375d-671">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="9375d-672">Исправлена ошибка командлета Get-AzProviderOperation для операций, когда Origin содержит User</span><span class="sxs-lookup"><span data-stu-id="9375d-672">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="9375d-673">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9375d-673">Az.Sql</span></span>
* <span data-ttu-id="9375d-674">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="9375d-674">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="9375d-675">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="9375d-675">Az.Websites</span></span>
* <span data-ttu-id="9375d-676">Новый командлет Get-AzWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="9375d-676">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="9375d-677">Новые командлеты New-AzWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows</span><span class="sxs-lookup"><span data-stu-id="9375d-677">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="9375d-678">0.2.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="9375d-678">0.2.0 - September 2018</span></span>
 <span data-ttu-id="9375d-679">Первый выпуск</span><span class="sxs-lookup"><span data-stu-id="9375d-679">Initial Release</span></span>