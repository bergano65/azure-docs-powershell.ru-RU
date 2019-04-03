---
ms.openlocfilehash: 2db9810e20254373a487013de50d4297d4ec50d5
ms.sourcegitcommit: 8f59e11e5c991543964154d63648aa1e6ae22512
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/26/2019
ms.locfileid: "58475396"
---
## <a name="160---march-2019"></a><span data-ttu-id="61fa8-101">1.6.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="61fa8-101">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="61fa8-102">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="61fa8-102">Highlights since the last major release</span></span>
* <span data-ttu-id="61fa8-103">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="61fa8-103">General availability of `Az` module</span></span>
* <span data-ttu-id="61fa8-104">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="61fa8-104">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="61fa8-105">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="61fa8-105">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="61fa8-106">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="61fa8-106">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="61fa8-107">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="61fa8-107">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="61fa8-108">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="61fa8-108">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="61fa8-109">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="61fa8-109">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="61fa8-110">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="61fa8-110">Az.Automation</span></span>
* <span data-ttu-id="61fa8-111">В управление обновлениями службы автоматизации Azure внесены изменения для поддержки следующих новых функций:</span><span class="sxs-lookup"><span data-stu-id="61fa8-111">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="61fa8-112">динамическое группирование;</span><span class="sxs-lookup"><span data-stu-id="61fa8-112">Dynamic grouping</span></span>
    * <span data-ttu-id="61fa8-113">скрипты предварительного или последующего выполнения;</span><span class="sxs-lookup"><span data-stu-id="61fa8-113">Pre-Post script</span></span>
    * <span data-ttu-id="61fa8-114">параметр перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="61fa8-114">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="61fa8-115">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="61fa8-115">Az.Compute</span></span>
* <span data-ttu-id="61fa8-116">Устранена проблема, связанная с разрешением пути в Get-AzVmBootDiagnosticsData.</span><span class="sxs-lookup"><span data-stu-id="61fa8-116">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="61fa8-117">Обновление клиентской библиотеки вычислений до версии 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="61fa8-117">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="61fa8-118">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="61fa8-118">Az.KeyVault</span></span>
* <span data-ttu-id="61fa8-119">Добавлена поддержка подстановочных знаков в командлетах KeyVault.</span><span class="sxs-lookup"><span data-stu-id="61fa8-119">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="61fa8-120">Az.Network</span><span class="sxs-lookup"><span data-stu-id="61fa8-120">Az.Network</span></span>
* <span data-ttu-id="61fa8-121">Добавлена поддержка анализа угроз для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="61fa8-121">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="61fa8-122">Добавлены настраиваемые правила и ресурс верхнего уровня для политики брандмауэра Шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="61fa8-122">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="61fa8-123">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="61fa8-123">Az.RecoveryServices</span></span>
* <span data-ttu-id="61fa8-124">В политику виртуальной машины Azure добавлен объект SnapshotRetentionInDays для поддержки мгновенного восстановления.</span><span class="sxs-lookup"><span data-stu-id="61fa8-124">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="61fa8-125">Добавлена поддержка канала для отмены регистрации контейнера.</span><span class="sxs-lookup"><span data-stu-id="61fa8-125">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="61fa8-126">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="61fa8-126">Az.Resources</span></span>
* <span data-ttu-id="61fa8-127">Обновлена поддержка подстановочных знаков для Get-AzResource и Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="61fa8-127">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="61fa8-128">Обновлены учетные данные, используемые при общих вызовах к ARM.</span><span class="sxs-lookup"><span data-stu-id="61fa8-128">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="61fa8-129">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="61fa8-129">Az.Sql</span></span>
* <span data-ttu-id="61fa8-130">Изменен тип параметра (ExcludeDetectionType) командлетов для обнаружения угроз с DetectionTypes на string[] для поддержки актуального состояния при добавлении новых типов обнаружения и для поддержки автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="61fa8-130">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="61fa8-131">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="61fa8-131">Az.Storage</span></span>
* <span data-ttu-id="61fa8-132">Поддержка получения, настройки и удаления политики управления в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="61fa8-132">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="61fa8-133">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="61fa8-133">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="61fa8-134">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="61fa8-134">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="61fa8-135">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="61fa8-135">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="61fa8-136">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="61fa8-136">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="61fa8-137">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="61fa8-137">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="61fa8-138">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="61fa8-138">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="61fa8-139">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="61fa8-139">Az.Websites</span></span>
* <span data-ttu-id="61fa8-140">Исправлена ошибка с шаблоном ARM, из-за которой прерывалось клонирование все слотов при использовании New-AzWebApp -IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="61fa8-140">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="61fa8-141">1.5.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="61fa8-141">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="61fa8-142">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="61fa8-142">Az.Accounts</span></span>
* <span data-ttu-id="61fa8-143">Добавлена команда Register-AzModule для поддержки созданных командлетов AutoRest.</span><span class="sxs-lookup"><span data-stu-id="61fa8-143">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="61fa8-144">Обновлены примеры для Connect AzAccount.</span><span class="sxs-lookup"><span data-stu-id="61fa8-144">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="61fa8-145">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="61fa8-145">Az.Automation</span></span>
* <span data-ttu-id="61fa8-146">Исправлена проблема с получением некоторых ежемесячных расписаний в нескольких командлетах службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="61fa8-146">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="61fa8-147">Исправлен командлет Get-AzAutomationDscNode, возвращающий только первые 20 узлов.</span><span class="sxs-lookup"><span data-stu-id="61fa8-147">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="61fa8-148">Теперь он возвращает все узлы.</span><span class="sxs-lookup"><span data-stu-id="61fa8-148">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="61fa8-149">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="61fa8-149">Az.Cdn</span></span>
* <span data-ttu-id="61fa8-150">Добавлены новые командлеты PowerShell для включения и отключения HTTPS для личного домена и отключены устаревшие командлеты.</span><span class="sxs-lookup"><span data-stu-id="61fa8-150">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="61fa8-151">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="61fa8-151">Az.Compute</span></span>
* <span data-ttu-id="61fa8-152">Добавлена поддержка подстановочных знаков в командлетах Get.</span><span class="sxs-lookup"><span data-stu-id="61fa8-152">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="61fa8-153">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="61fa8-153">Az.DataFactory</span></span>
* <span data-ttu-id="61fa8-154">Обновлен пакет SDK для ADF .NET до версии 3.0.1.</span><span class="sxs-lookup"><span data-stu-id="61fa8-154">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="61fa8-155">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="61fa8-155">Az.LogicApp</span></span>
* <span data-ttu-id="61fa8-156">Исправлена проблема с получением только первой страницы результатов при выполнении команды ListWorkflows.</span><span class="sxs-lookup"><span data-stu-id="61fa8-156">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="61fa8-157">Az.Network</span><span class="sxs-lookup"><span data-stu-id="61fa8-157">Az.Network</span></span>
* <span data-ttu-id="61fa8-158">Добавлена поддержка подстановочных знаков в командлетах Network.</span><span class="sxs-lookup"><span data-stu-id="61fa8-158">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="61fa8-159">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="61fa8-159">Az.RecoveryServices</span></span>
* <span data-ttu-id="61fa8-160">Добавлена поддержка SQL Server на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="61fa8-160">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="61fa8-161">Обновление пакета SDK</span><span class="sxs-lookup"><span data-stu-id="61fa8-161">SDK Update</span></span>
* <span data-ttu-id="61fa8-162">Удалена проверка VMappContainer в Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="61fa8-162">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="61fa8-163">Добавлены параметры Name и ServerName для Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="61fa8-163">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="61fa8-164">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="61fa8-164">Az.Resources</span></span>
* <span data-ttu-id="61fa8-165">Добавлен параметр `-TemplateObject` в командлеты для развертывания.</span><span class="sxs-lookup"><span data-stu-id="61fa8-165">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="61fa8-166">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2933.</span><span class="sxs-lookup"><span data-stu-id="61fa8-166">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="61fa8-167">Устранена проблема с передачей в конвейер результата `Get-AzResource` для `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="61fa8-167">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="61fa8-168">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8240.</span><span class="sxs-lookup"><span data-stu-id="61fa8-168">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="61fa8-169">Устранена проблема с изменением типа данных JSON при выполнении `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="61fa8-169">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="61fa8-170">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7930.</span><span class="sxs-lookup"><span data-stu-id="61fa8-170">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="61fa8-171">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="61fa8-171">Az.Sql</span></span>
* <span data-ttu-id="61fa8-172">Обновление AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="61fa8-172">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="61fa8-173">Исправлено поведение для пограничного случая при создании параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="61fa8-173">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="61fa8-174">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="61fa8-174">Az.Storage</span></span>
* <span data-ttu-id="61fa8-175">Включена поддержка Kind BlockBlobStorage при создании учетной записи хранения для New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="61fa8-175">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="61fa8-176">1.4.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="61fa8-176">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="61fa8-177">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="61fa8-177">Az.AnalysisServices</span></span>
* <span data-ttu-id="61fa8-178">Командлет AddAzureASAccount устарел.</span><span class="sxs-lookup"><span data-stu-id="61fa8-178">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="61fa8-179">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="61fa8-179">Az.Automation</span></span>
* <span data-ttu-id="61fa8-180">Обновлена справка для командлета Import-AzAutomationDscNodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="61fa8-180">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="61fa8-181">Добавлена проверка имени конфигурации для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="61fa8-181">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="61fa8-182">Улучшена обработка ошибок для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="61fa8-182">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="61fa8-183">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="61fa8-183">Az.CognitiveServices</span></span>
* <span data-ttu-id="61fa8-184">Добавлен параметр CustomSubdomainName — новый необязательный параметр для командлета New-AzCognitiveServicesAccount, который указывает поддомен для ресурса.</span><span class="sxs-lookup"><span data-stu-id="61fa8-184">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="61fa8-185">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="61fa8-185">Az.Compute</span></span>
* <span data-ttu-id="61fa8-186">Устранена проблема с идентификаторами наборов параметров.</span><span class="sxs-lookup"><span data-stu-id="61fa8-186">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="61fa8-187">Обновлен командлет Get-AzVMExtension для отображения списка всех установленных расширений, если не указан параметр Name.</span><span class="sxs-lookup"><span data-stu-id="61fa8-187">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="61fa8-188">Для командлета Update-AzImage добавлены параметры Tag и ResourceId.</span><span class="sxs-lookup"><span data-stu-id="61fa8-188">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="61fa8-189">Командлет Get-AzVmssVM, который выполняется без указания идентификатора экземпляра и с параметром InstanceView, может выводить виртуальные машины из VMSS с представлением экземпляра.</span><span class="sxs-lookup"><span data-stu-id="61fa8-189">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="61fa8-190">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="61fa8-190">Az.DataLakeStore</span></span>
* <span data-ttu-id="61fa8-191">Добавлены командлеты для перечисления и восстановления удаленного элемента ADL.</span><span class="sxs-lookup"><span data-stu-id="61fa8-191">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="61fa8-192">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="61fa8-192">Az.EventHub</span></span>
* <span data-ttu-id="61fa8-193">Добавлено новое логическое свойство SkipEmptyArchives для пропуска пустых архивов в классе CaptureDescription Eventhub.</span><span class="sxs-lookup"><span data-stu-id="61fa8-193">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="61fa8-194">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="61fa8-194">Az.KeyVault</span></span>
* <span data-ttu-id="61fa8-195">Исправлена расстановка тегов для командлета Set-AzKeyVaultSecret.</span><span class="sxs-lookup"><span data-stu-id="61fa8-195">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="61fa8-196">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="61fa8-196">Az.LogicApp</span></span>
* <span data-ttu-id="61fa8-197">Добавлен SKU "Базовый" для учетных записей интеграции.</span><span class="sxs-lookup"><span data-stu-id="61fa8-197">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="61fa8-198">Добавлены типы сопоставлений Liquid, а также XSLT 2.0 и XSLT 3.0.</span><span class="sxs-lookup"><span data-stu-id="61fa8-198">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="61fa8-199">Новые командлеты для сборок учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="61fa8-199">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="61fa8-200">Get-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="61fa8-200">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="61fa8-201">New-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="61fa8-201">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="61fa8-202">Remove-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="61fa8-202">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="61fa8-203">Set-AzIntegrationAccountAssembly.</span><span class="sxs-lookup"><span data-stu-id="61fa8-203">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="61fa8-204">Новые командлеты для конфигурации пакета учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="61fa8-204">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="61fa8-205">Get-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="61fa8-205">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="61fa8-206">New-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="61fa8-206">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="61fa8-207">Remove-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="61fa8-207">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="61fa8-208">Set-AzIntegrationAccountBatchConfiguration.</span><span class="sxs-lookup"><span data-stu-id="61fa8-208">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="61fa8-209">Обновлен пакет SDK Logic Apps до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="61fa8-209">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="61fa8-210">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="61fa8-210">Az.Monitor</span></span>
* <span data-ttu-id="61fa8-211">Обновлена справка для командлета Get-AzMetric.</span><span class="sxs-lookup"><span data-stu-id="61fa8-211">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="61fa8-212">Az.Network</span><span class="sxs-lookup"><span data-stu-id="61fa8-212">Az.Network</span></span>
* <span data-ttu-id="61fa8-213">Обновлен пример справки для командлета Add-AzApplicationGatewayCustomError.</span><span class="sxs-lookup"><span data-stu-id="61fa8-213">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="61fa8-214">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="61fa8-214">Az.OperationalInsights</span></span>
* <span data-ttu-id="61fa8-215">Дополнительная поддержка создания и получения источников данных ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="61fa8-215">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="61fa8-216">Добавлен новый тип ApplicationInsights для получения определенных или всех источников данных ApplicationInsights для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="61fa8-216">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="61fa8-217">Добавлен командлет New-AzOperationalInsightsApplicationInsightsDataSource для создания источника данных с использованием параметров указанного ресурса Application-Insightss: subscription Id, resourceGroupName и name.</span><span class="sxs-lookup"><span data-stu-id="61fa8-217">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="61fa8-218">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="61fa8-218">Az.Resources</span></span>
* <span data-ttu-id="61fa8-219">исправлена проблема https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="61fa8-219">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="61fa8-220">исправлена проблема https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="61fa8-220">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="61fa8-221">исправлена проблема https://github.com/Azure/azure-powershell/issues/6219.</span><span class="sxs-lookup"><span data-stu-id="61fa8-221">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="61fa8-222">Исправлена ошибка, препятствующая повторному созданию KeyCredentials.</span><span class="sxs-lookup"><span data-stu-id="61fa8-222">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="61fa8-223">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="61fa8-223">Az.Sql</span></span>
* <span data-ttu-id="61fa8-224">Добавлена поддержка уровня гипермасштабирования в базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="61fa8-224">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="61fa8-225">Исправлена ошибка, из-за которой восстановление могло завершиться со сбоем при указании ненужных свойств в запросе на восстановление.</span><span class="sxs-lookup"><span data-stu-id="61fa8-225">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="61fa8-226">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="61fa8-226">Az.Websites</span></span>
* <span data-ttu-id="61fa8-227">Исправлен пример для командлета Get-AzWebAppSlotMetrics.</span><span class="sxs-lookup"><span data-stu-id="61fa8-227">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="61fa8-228">1.3.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="61fa8-228">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="61fa8-229">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="61fa8-229">Az.Accounts</span></span>
* <span data-ttu-id="61fa8-230">Обновление до последней версии ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="61fa8-230">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="61fa8-231">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="61fa8-231">Az.AnalysisServices</span></span>
<span data-ttu-id="61fa8-232">Общедоступная версия модуля Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="61fa8-232">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="61fa8-233">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="61fa8-233">Az.Compute</span></span>
* <span data-ttu-id="61fa8-234">Расширение AEM: добавлена поддержка дисков UltraSSD, P60, P70 и P80.</span><span class="sxs-lookup"><span data-stu-id="61fa8-234">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="61fa8-235">Обновлено описание справки для командлета Set-AzVMBootDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="61fa8-235">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="61fa8-236">Обновлено описание справки и пример для командлета Update-AzImage.</span><span class="sxs-lookup"><span data-stu-id="61fa8-236">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="61fa8-237">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="61fa8-237">Az.RecoveryServices</span></span>
<span data-ttu-id="61fa8-238">Общедоступная версия модуля Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="61fa8-238">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="61fa8-239">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="61fa8-239">Az.Resources</span></span>
* <span data-ttu-id="61fa8-240">Исправлена расстановка тегов для групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="61fa8-240">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="61fa8-241">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="61fa8-241">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="61fa8-242">Исправлена проблема с игнорированием командлетом `Get-AzureRmRoleAssignment` параметра -ErrorAction.</span><span class="sxs-lookup"><span data-stu-id="61fa8-242">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="61fa8-243">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="61fa8-243">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="61fa8-244">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="61fa8-244">Az.Sql</span></span>
* <span data-ttu-id="61fa8-245">Добавлен командлет Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="61fa8-245">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="61fa8-246">Исправлена проблема с появлением исключения NullRef при выполнении командлетов SQL, если не выполнен вход в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="61fa8-246">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="61fa8-247">Исправлено исключение NullRef в командлете Get-AzSqlCapability.</span><span class="sxs-lookup"><span data-stu-id="61fa8-247">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="61fa8-248">1.2.1 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="61fa8-248">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="61fa8-249">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="61fa8-249">Az.Accounts</span></span>
* <span data-ttu-id="61fa8-250">Выпуск с правильной версией службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="61fa8-250">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="61fa8-251">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="61fa8-251">Az.AnalysisServices</span></span>
* <span data-ttu-id="61fa8-252">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="61fa8-252">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="61fa8-253">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="61fa8-253">Az.RecoveryServices</span></span>
* <span data-ttu-id="61fa8-254">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="61fa8-254">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="61fa8-255">1.2.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="61fa8-255">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="61fa8-256">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="61fa8-256">Az.Accounts</span></span>
* <span data-ttu-id="61fa8-257">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="61fa8-257">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="61fa8-258">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="61fa8-258">Update incorrect online help URLs</span></span>
* <span data-ttu-id="61fa8-259">Добавлено предупреждающее сообщение в PS Core для модуля Uninstall-AzureRm.</span><span class="sxs-lookup"><span data-stu-id="61fa8-259">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="61fa8-260">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="61fa8-260">Az.Aks</span></span>
* <span data-ttu-id="61fa8-261">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="61fa8-261">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="61fa8-262">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="61fa8-262">Az.Automation</span></span>
* <span data-ttu-id="61fa8-263">Добавлена поддержка для модулей runbook Python 2.</span><span class="sxs-lookup"><span data-stu-id="61fa8-263">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="61fa8-264">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="61fa8-264">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="61fa8-265">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="61fa8-265">Az.Cdn</span></span>
* <span data-ttu-id="61fa8-266">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="61fa8-266">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="61fa8-267">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="61fa8-267">Az.Compute</span></span>
* <span data-ttu-id="61fa8-268">Добавлен командлет Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="61fa8-268">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="61fa8-269">Добавлен параметр TempDisk к командлету Set-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="61fa8-269">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="61fa8-270">Исправлено предупреждающее сообщение командлета New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="61fa8-270">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="61fa8-271">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="61fa8-271">Az.ContainerRegistry</span></span>
* <span data-ttu-id="61fa8-272">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="61fa8-272">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="61fa8-273">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="61fa8-273">Az.DataFactory</span></span>
* <span data-ttu-id="61fa8-274">Пакет SDK ADF .Net обновлен до версии 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="61fa8-274">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="61fa8-275">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="61fa8-275">Az.DataLakeStore</span></span>
* <span data-ttu-id="61fa8-276">Исправлена проблема с конечной точкой ADLS при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="61fa8-276">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="61fa8-277">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7462.</span><span class="sxs-lookup"><span data-stu-id="61fa8-277">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="61fa8-278">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="61fa8-278">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="61fa8-279">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="61fa8-279">Az.IotHub</span></span>
* <span data-ttu-id="61fa8-280">Добавлен формат кодирования для командлета Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="61fa8-280">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="61fa8-281">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="61fa8-281">Az.KeyVault</span></span>
* <span data-ttu-id="61fa8-282">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="61fa8-282">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="61fa8-283">Az.Network</span><span class="sxs-lookup"><span data-stu-id="61fa8-283">Az.Network</span></span>
* <span data-ttu-id="61fa8-284">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="61fa8-284">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="61fa8-285">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="61fa8-285">Az.Resources</span></span>
* <span data-ttu-id="61fa8-286">Исправлены неправильные примеры в справочной документации по командлетам New-AzADAppCredential и New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="61fa8-286">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="61fa8-287">Исправлена проблема, при которой путь для параметра -TemplateFile не удавалось разрешить до выполнения командлетов развертывания групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="61fa8-287">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="61fa8-288">Az.Resources: исправлена документация для значения по умолчанию -Mode командлета New-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="61fa8-288">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="61fa8-289">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/7522.</span><span class="sxs-lookup"><span data-stu-id="61fa8-289">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="61fa8-290">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/5747.</span><span class="sxs-lookup"><span data-stu-id="61fa8-290">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="61fa8-291">Исправлена проблема с форматированием объекта PSResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="61fa8-291">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="61fa8-292">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2123.</span><span class="sxs-lookup"><span data-stu-id="61fa8-292">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="61fa8-293">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="61fa8-293">Az.ServiceFabric</span></span>
* <span data-ttu-id="61fa8-294">Исправлена проблема с появлением исключения в процессе отката при добавлении сертификата к модели VMSS: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="61fa8-294">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="61fa8-295">Исправлены некоторые сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="61fa8-295">Fix some error messages.</span></span>
* <span data-ttu-id="61fa8-296">Исправлена проблема с созданием кластера с шаблоном ARM по умолчанию для командлета New-AzServiceFabriCluster, который не работал с операцией миграции в Az.</span><span class="sxs-lookup"><span data-stu-id="61fa8-296">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="61fa8-297">Исправлена проблема с добавлением сертификата кластера или приложения: теперь они добавляются только в Масштабируемые наборы виртуальных машин, которые сопоставлены с кластером, путем проверки идентификатора кластера в расширении.</span><span class="sxs-lookup"><span data-stu-id="61fa8-297">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="61fa8-298">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="61fa8-298">Az.SignalR</span></span>
* <span data-ttu-id="61fa8-299">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="61fa8-299">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="61fa8-300">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="61fa8-300">Az.Sql</span></span>
* <span data-ttu-id="61fa8-301">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="61fa8-301">Update incorrect online help URLs</span></span>
* <span data-ttu-id="61fa8-302">Обновлено описание параметра LicenseType с добавлением возможных значений.</span><span class="sxs-lookup"><span data-stu-id="61fa8-302">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="61fa8-303">Исправлена проблема с неправильным обновлением удостоверения управляемого экземпляра, если оно было единственным обновляемым свойством.</span><span class="sxs-lookup"><span data-stu-id="61fa8-303">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="61fa8-304">Поддержка пользовательских параметров сортировки в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="61fa8-304">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="61fa8-305">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="61fa8-305">Az.Storage</span></span>
* <span data-ttu-id="61fa8-306">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="61fa8-306">Update incorrect online help URLs</span></span>
* <span data-ttu-id="61fa8-307">Добавлен вывод подробных сообщений об ошибке при получении или установке классических свойств ведения журнала или метрик в учетной записи хранилища класса Premium, так как учетная запись хранилища класса Premium не поддерживает классические функции ведения журнала и метрик.</span><span class="sxs-lookup"><span data-stu-id="61fa8-307">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="61fa8-308">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="61fa8-308">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="61fa8-309">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="61fa8-309">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="61fa8-310">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="61fa8-310">Az.TrafficManager</span></span>
* <span data-ttu-id="61fa8-311">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="61fa8-311">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="61fa8-312">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="61fa8-312">Az.Websites</span></span>
* <span data-ttu-id="61fa8-313">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="61fa8-313">Update incorrect online help URLs</span></span>
* <span data-ttu-id="61fa8-314">Исправлена работа командлета New-AzWebAppSSLBinding: сертификат отправляется в правильную группу ресурсов и правильное расположение, если приложение размещено в ASE.</span><span class="sxs-lookup"><span data-stu-id="61fa8-314">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="61fa8-315">Исправлена работа командлета New-AzWebAppSSLBinding: теги не перезаписываются при привязке SSL-сертификата к приложению.</span><span class="sxs-lookup"><span data-stu-id="61fa8-315">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="61fa8-316">1.1.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="61fa8-316">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="61fa8-317">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="61fa8-317">Az.Accounts</span></span>
* <span data-ttu-id="61fa8-318">Добавление области "Local" в Enable-AzureRmAlias.</span><span class="sxs-lookup"><span data-stu-id="61fa8-318">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="61fa8-319">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="61fa8-319">Az.Compute</span></span>
* <span data-ttu-id="61fa8-320">Теперь имя не является обязательным в идентификаторе набора параметров для Restart/Start/Stop/Remove/Set-AzVM и Save-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="61fa8-320">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="61fa8-321">Обновлено описание идентификатора в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="61fa8-321">Updated the description of ID in help files</span></span>
* <span data-ttu-id="61fa8-322">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="61fa8-322">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="61fa8-323">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="61fa8-323">Az.DataLakeStore</span></span>
* <span data-ttu-id="61fa8-324">Обновление версии пакета SDK для плоскости данных до 1.1.14 для устранения найденных проблем.</span><span class="sxs-lookup"><span data-stu-id="61fa8-324">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="61fa8-325">Исправлена обработка отрицательного времени доступа и времени изменения для getfilestatus и liststatus, исправлен токен отмены для асинхронных методов.</span><span class="sxs-lookup"><span data-stu-id="61fa8-325">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="61fa8-326">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="61fa8-326">Az.EventGrid</span></span>
* <span data-ttu-id="61fa8-327">Обновление для использования API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="61fa8-327">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="61fa8-328">Обновлены указанные ниже командлеты для поддержки нового сценария в API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="61fa8-328">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="61fa8-329">New-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="61fa8-329">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="61fa8-330">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="61fa8-330">Event Time-To-Live,</span></span>
        - <span data-ttu-id="61fa8-331">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="61fa8-331">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="61fa8-332">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="61fa8-332">Dead letter endpoint.</span></span>
    - <span data-ttu-id="61fa8-333">Update-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="61fa8-333">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="61fa8-334">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="61fa8-334">Event Time-To-Live,</span></span>
        - <span data-ttu-id="61fa8-335">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="61fa8-335">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="61fa8-336">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="61fa8-336">Dead letter endpoint.</span></span>
* <span data-ttu-id="61fa8-337">Для параметра EndpointType добавлены новые значения перечисления (storageQueue и hybridConnection) в командлеты New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="61fa8-337">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="61fa8-338">Если ожидается, что создание или обновление подписки на событие повлечет за собой действия со стороны пользователя, выполняемые вручную, отображается предупреждение при создании или обновлении подписки события.</span><span class="sxs-lookup"><span data-stu-id="61fa8-338">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="61fa8-339">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="61fa8-339">Az.IotHub</span></span>
* <span data-ttu-id="61fa8-340">Пакет SDK Центра Интернета вещей обновлен до последней версии.</span><span class="sxs-lookup"><span data-stu-id="61fa8-340">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="61fa8-341">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="61fa8-341">Az.LogicApp</span></span>
* <span data-ttu-id="61fa8-342">Get-AzLogicApp позволяет перечислить все параметры без указанного имени.</span><span class="sxs-lookup"><span data-stu-id="61fa8-342">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="61fa8-343">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="61fa8-343">Az.Resources</span></span>
* <span data-ttu-id="61fa8-344">Исправлена проблема с набором параметров при предоставлении параметров "-ODataQuery" и "-ResourceId" для "Get-AzResource".</span><span class="sxs-lookup"><span data-stu-id="61fa8-344">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="61fa8-345">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7875.</span><span class="sxs-lookup"><span data-stu-id="61fa8-345">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="61fa8-346">Исправлена обработка параметра -Custom в New/Set-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="61fa8-346">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="61fa8-347">Исправлена опечатка в документации по New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="61fa8-347">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="61fa8-348">Параметр "-MailNickname" стал обязательным для "New-AzADUser".</span><span class="sxs-lookup"><span data-stu-id="61fa8-348">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="61fa8-349">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8220.</span><span class="sxs-lookup"><span data-stu-id="61fa8-349">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="61fa8-350">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="61fa8-350">Az.SignalR</span></span>
* <span data-ttu-id="61fa8-351">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="61fa8-351">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="61fa8-352">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="61fa8-352">Az.Sql</span></span>
* <span data-ttu-id="61fa8-353">Зависимость клиента управления хранением преобразована для общей реализации в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="61fa8-353">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="61fa8-354">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="61fa8-354">Az.Storage</span></span>
* <span data-ttu-id="61fa8-355">Установка параметра StorageAccountName для контекста хранилища в качестве реального имени учетной записи хранения, если она была создана с использованием токена Sas, OAuth или анонимного доступа.</span><span class="sxs-lookup"><span data-stu-id="61fa8-355">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="61fa8-356">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="61fa8-356">New-AzStorageContext</span></span>
* <span data-ttu-id="61fa8-357">Создание токена Sas большого двоичного объекта моментального снимка с параметром "-FullUri". Возвращаемый URI исправлен на URI моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="61fa8-357">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="61fa8-358">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="61fa8-358">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="61fa8-359">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="61fa8-359">Az.Websites</span></span>
* <span data-ttu-id="61fa8-360">Исправлена ошибка синтаксического анализа даты в "Get-AzDeletedWebApp".</span><span class="sxs-lookup"><span data-stu-id="61fa8-360">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="61fa8-361">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="61fa8-361">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="61fa8-362">1.0.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="61fa8-362">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="61fa8-363">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="61fa8-363">General</span></span>

- <span data-ttu-id="61fa8-364">Общедоступная версия модуля Az.</span><span class="sxs-lookup"><span data-stu-id="61fa8-364">General Availability of Az Module</span></span>
- <span data-ttu-id="61fa8-365">Справка в Интернете для каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="61fa8-365">Online help for each module</span></span>
- <span data-ttu-id="61fa8-366">Дополнительные сведения и стратегию развития см. в статье [Announcing New Module 'Az'](https://aka.ms/azps-announce) (Объявление о новом модуле Az)</span><span class="sxs-lookup"><span data-stu-id="61fa8-366">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="61fa8-367">Сведения о миграции с AzureRM см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="61fa8-367">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="61fa8-368">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="61fa8-368">Az.Accounts</span></span>
- <span data-ttu-id="61fa8-369">Изменено с Az.Profile.</span><span class="sxs-lookup"><span data-stu-id="61fa8-369">Changed from Az.Profile</span></span>
- <span data-ttu-id="61fa8-370">Исправлены форматы таблиц для типов профиля и контекста.</span><span class="sxs-lookup"><span data-stu-id="61fa8-370">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="61fa8-371">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="61fa8-371">Az.ApiManagement</span></span>
- <span data-ttu-id="61fa8-372">Исправления для #7002.</span><span class="sxs-lookup"><span data-stu-id="61fa8-372">Fixes for #7002</span></span>
- <span data-ttu-id="61fa8-373">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="61fa8-373">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="61fa8-374">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="61fa8-374">Az.Batch</span></span>
- <span data-ttu-id="61fa8-375">Добавлена возможность видеть, какая версия агента узла пакетной службы Azure работает в пуле на каждой виртуальной машине, с помощью нового свойства `NodeAgentInformation` в `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="61fa8-375">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="61fa8-376">Значение `Caching` по умолчанию для `PSDataDisk` теперь `ReadWrite` вместо `None`.</span><span class="sxs-lookup"><span data-stu-id="61fa8-376">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="61fa8-377">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="61fa8-377">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="61fa8-378">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="61fa8-378">Az.Billing</span></span>
- <span data-ttu-id="61fa8-379">Объединены командлеты Billing, Consumption и UsageAggregates. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0).</span><span class="sxs-lookup"><span data-stu-id="61fa8-379">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="61fa8-380">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="61fa8-380">Az.CognitivServices</span></span>
- <span data-ttu-id="61fa8-381">Добавлены средства заполнения для SkuName и Typem, доступные в операции New-AzureRmCognitiveServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="61fa8-381">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="61fa8-382">Удален набор параметров GetSkusWithAccountParamSetName из Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="61fa8-382">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="61fa8-383">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="61fa8-383">Az.ContainerInstance</span></span>
- <span data-ttu-id="61fa8-384">Добавлена поддержка ManagedIdentity.</span><span class="sxs-lookup"><span data-stu-id="61fa8-384">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="61fa8-385">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="61fa8-385">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="61fa8-386">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="61fa8-386">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="61fa8-387">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="61fa8-387">Az.DataLakeStore</span></span>
- <span data-ttu-id="61fa8-388">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="61fa8-388">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="61fa8-389">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="61fa8-389">Az.Monitor</span></span>
- <span data-ttu-id="61fa8-390">"Az.Insights" переименован в "Az.Monitor" и внесены другие незначительные критические изменения. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="61fa8-390">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="61fa8-391">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="61fa8-391">Az.KeyVault</span></span>
- <span data-ttu-id="61fa8-392">Из типов вывода удалено устаревшее свойство PurgeDisabled</span><span class="sxs-lookup"><span data-stu-id="61fa8-392">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="61fa8-393">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="61fa8-393">Az.MachineLearning</span></span>
- <span data-ttu-id="61fa8-394">Включены командлеты из модуля Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="61fa8-394">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="61fa8-395">Az.Media</span><span class="sxs-lookup"><span data-stu-id="61fa8-395">Az.Media</span></span>
- <span data-ttu-id="61fa8-396">Удаляет устаревший псевдоним Tags из New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="61fa8-396">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="61fa8-397">Az.Network</span><span class="sxs-lookup"><span data-stu-id="61fa8-397">Az.Network</span></span>
<span data-ttu-id="61fa8-398">В шлюз приложений добавлена поддержка настройки RewriteRuleSets</span><span class="sxs-lookup"><span data-stu-id="61fa8-398">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="61fa8-399">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="61fa8-399">New cmdlets added:</span></span>
        - <span data-ttu-id="61fa8-400">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="61fa8-400">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="61fa8-401">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="61fa8-401">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="61fa8-402">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="61fa8-402">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="61fa8-403">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="61fa8-403">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="61fa8-404">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="61fa8-404">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="61fa8-405">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="61fa8-405">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="61fa8-406">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="61fa8-406">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="61fa8-407">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="61fa8-407">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="61fa8-408">В следующие командлеты добавлен необязательный параметр -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="61fa8-408">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="61fa8-409">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="61fa8-409">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="61fa8-410">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="61fa8-410">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="61fa8-411">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="61fa8-411">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="61fa8-412">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="61fa8-412">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="61fa8-413">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="61fa8-413">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="61fa8-414">New-AzureRmApplicationGatewayUrlPathMapConfig добавил с помощью идентификатора поддержку KeyVault для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="61fa8-414">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="61fa8-415">В следующие командлеты добавлен необязательный параметр -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="61fa8-415">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="61fa8-416">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="61fa8-416">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="61fa8-417">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="61fa8-417">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="61fa8-418">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="61fa8-418">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="61fa8-419">В командлет New-AzApplicationGateway добавлен необязательный параметр -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="61fa8-419">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="61fa8-420">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="61fa8-420">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="61fa8-421">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="61fa8-421">Az.OperationalInsights</span></span>
- <span data-ttu-id="61fa8-422">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="61fa8-422">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="61fa8-423">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="61fa8-423">Az.Profile</span></span>
- <span data-ttu-id="61fa8-424">Имя модуля изменено на Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="61fa8-424">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="61fa8-425">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="61fa8-425">Az.RecoveryServices</span></span>
- <span data-ttu-id="61fa8-426">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="61fa8-426">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="61fa8-427">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="61fa8-427">Az.Resources</span></span>
- <span data-ttu-id="61fa8-428">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="61fa8-428">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="61fa8-429">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="61fa8-429">Az.ServiceFabric</span></span>
- <span data-ttu-id="61fa8-430">Поддержка спецификации сертификата по общему имени и отпечатку</span><span class="sxs-lookup"><span data-stu-id="61fa8-430">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="61fa8-431">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="61fa8-431">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="61fa8-432">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="61fa8-432">Az.SIgnalR</span></span>
- <span data-ttu-id="61fa8-433">Общедоступная версия командлетов PowerShell для SIgnalR</span><span class="sxs-lookup"><span data-stu-id="61fa8-433">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="61fa8-434">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="61fa8-434">Az.Sql</span></span>
- <span data-ttu-id="61fa8-435">Добавлены новые типы обнаружения Data_Exfiltration и Unsafe_Action в командлеты обнаружения угроз</span><span class="sxs-lookup"><span data-stu-id="61fa8-435">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="61fa8-436">Примеры обновленной документации для командлетов аудита Sql</span><span class="sxs-lookup"><span data-stu-id="61fa8-436">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="61fa8-437">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="61fa8-437">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="61fa8-438">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="61fa8-438">Az.Storage</span></span>
- <span data-ttu-id="61fa8-439">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="61fa8-439">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="61fa8-440">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="61fa8-440">Az.Websites</span></span>
- <span data-ttu-id="61fa8-441">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="61fa8-441">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="61fa8-442">0.7.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="61fa8-442">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="61fa8-443">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="61fa8-443">General</span></span>

* <span data-ttu-id="61fa8-444">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="61fa8-444">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="61fa8-445">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="61fa8-445">Az.Compute</span></span>

* <span data-ttu-id="61fa8-446">Добавлена поддержка UltraSSD и образов коллекции в простых наборах параметров для командлетов `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="61fa8-446">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="61fa8-447">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="61fa8-447">Az.DataLakeStore</span></span>

* <span data-ttu-id="61fa8-448">Исправлено косую черту в конце домена учетной записи ADLS</span><span class="sxs-lookup"><span data-stu-id="61fa8-448">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="61fa8-449">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="61fa8-449">Az.FrontDoor</span></span>

* <span data-ttu-id="61fa8-450">Исправлены некоторые неработающие ссылки</span><span class="sxs-lookup"><span data-stu-id="61fa8-450">Fixed some broken links</span></span>
    - <span data-ttu-id="61fa8-451">В статьях New-AzureRmFrontDoor и Set-AzureRmFrontDoor исправлена ссылка на статью командлета New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="61fa8-451">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="61fa8-452">В статье New-AzureRmFrontDoorManagedRuleObject исправлена ссылка на статью командлета New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="61fa8-452">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="61fa8-453">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="61fa8-453">Az.RecoveryServices</span></span>

* <span data-ttu-id="61fa8-454">Добавлены проверки на стороне клиента для операций восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="61fa8-454">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="61fa8-455">StorageAccountName и storageAccountResourceGroupName являются необязательными для восстановления afs.</span><span class="sxs-lookup"><span data-stu-id="61fa8-455">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="61fa8-456">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="61fa8-456">Az.Resources</span></span>

* <span data-ttu-id="61fa8-457">Исправление для https://github.com/Azure/azure-powershell/issues/7679.</span><span class="sxs-lookup"><span data-stu-id="61fa8-457">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="61fa8-458">Обновите Get-AzureRmRoleAssignment, чтобы использовать область подписки, если она указана при запросе классических администраторов.</span><span class="sxs-lookup"><span data-stu-id="61fa8-458">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="61fa8-459">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="61fa8-459">Az.Sql</span></span>

* <span data-ttu-id="61fa8-460">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="61fa8-460">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="61fa8-461">Устранена проблема с использованием Get-AzureRmSqlDatabaseVulnerabilityAssessment с .NET Core.</span><span class="sxs-lookup"><span data-stu-id="61fa8-461">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="61fa8-462">Изменена документация справочных сообщений, связанных с командлетами аудита SQL.</span><span class="sxs-lookup"><span data-stu-id="61fa8-462">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="61fa8-463">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="61fa8-463">Az.Storage</span></span>

* <span data-ttu-id="61fa8-464">Добавлено -EnableHierarchicalNamespace к New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="61fa8-464">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="61fa8-465">Устранена проблема, из-за которой командлет Copy File не может повторно использовать исходный контекст в пункте назначения, если не введен -DestContext</span><span class="sxs-lookup"><span data-stu-id="61fa8-465">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="61fa8-466">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="61fa8-466">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="61fa8-467">Поддержка статической конфигурации сайта</span><span class="sxs-lookup"><span data-stu-id="61fa8-467">Support Static Website configuration</span></span>
    - <span data-ttu-id="61fa8-468">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="61fa8-468">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="61fa8-469">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="61fa8-469">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="61fa8-470">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="61fa8-470">Az.Websites</span></span>

* <span data-ttu-id="61fa8-471">Set-AzureRmWebApp и Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="61fa8-471">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="61fa8-472">Добавлен новый параметр (-AzureStoragePath), который указывает путь службы хранилища Azure для подключения в приложениях-контейнерах Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="61fa8-472">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="61fa8-473">Используйте выходные данные нового командлета New-AzureRmWebAppAzureStoragePath в качестве параметра, чтобы задать пути к службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="61fa8-473">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="61fa8-474">0.6.1 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="61fa8-474">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="61fa8-475">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="61fa8-475">Az.ApiManagement</span></span>
* <span data-ttu-id="61fa8-476">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="61fa8-476">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="61fa8-477">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="61fa8-477">Az.Automation</span></span>
* <span data-ttu-id="61fa8-478">Командлеты службы автоматизации Azure на базе Swagger.</span><span class="sxs-lookup"><span data-stu-id="61fa8-478">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="61fa8-479">Добавлены командлеты для Управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="61fa8-479">Added Update Management cmdlets</span></span>
* <span data-ttu-id="61fa8-480">Добавлены командлеты для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="61fa8-480">Added Source Control cmdlets</span></span>
* <span data-ttu-id="61fa8-481">Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="61fa8-481">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="61fa8-482">Исправлена команда DSC для регистрации узла.</span><span class="sxs-lookup"><span data-stu-id="61fa8-482">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="61fa8-483">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="61fa8-483">Az.Compute</span></span>
* <span data-ttu-id="61fa8-484">Исправлена проблема с удостоверением, назначаемым системой.</span><span class="sxs-lookup"><span data-stu-id="61fa8-484">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="61fa8-485">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="61fa8-485">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="61fa8-486">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="61fa8-486">Az.ContainerInstance</span></span>
* <span data-ttu-id="61fa8-487">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="61fa8-487">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="61fa8-488">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="61fa8-488">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="61fa8-489">Обновлено описание в примерах командлетов для Marketplace.</span><span class="sxs-lookup"><span data-stu-id="61fa8-489">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="61fa8-490">Az.Network</span><span class="sxs-lookup"><span data-stu-id="61fa8-490">Az.Network</span></span>
* <span data-ttu-id="61fa8-491">Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="61fa8-491">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="61fa8-492">Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="61fa8-492">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="61fa8-493">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="61fa8-493">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="61fa8-494">Исправлены проблемы с использованием памяти в карте виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="61fa8-494">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="61fa8-495">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="61fa8-495">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="61fa8-496">Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="61fa8-496">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="61fa8-497">Параметры часового пояса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="61fa8-497">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="61fa8-498">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="61fa8-498">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="61fa8-499">Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="61fa8-499">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="61fa8-500">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="61fa8-500">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="61fa8-501">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="61fa8-501">Az.Relay</span></span>
* <span data-ttu-id="61fa8-502">Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.</span><span class="sxs-lookup"><span data-stu-id="61fa8-502">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="61fa8-503">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="61fa8-503">Az.Resources</span></span>
* <span data-ttu-id="61fa8-504">Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.</span><span class="sxs-lookup"><span data-stu-id="61fa8-504">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="61fa8-505">Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.</span><span class="sxs-lookup"><span data-stu-id="61fa8-505">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="61fa8-506">Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.</span><span class="sxs-lookup"><span data-stu-id="61fa8-506">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="61fa8-507">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="61fa8-507">Az.ServiceFabric</span></span>
* <span data-ttu-id="61fa8-508">Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.</span><span class="sxs-lookup"><span data-stu-id="61fa8-508">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="61fa8-509">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="61fa8-509">Az.Sql</span></span>
* <span data-ttu-id="61fa8-510">Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="61fa8-510">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="61fa8-511">Get-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="61fa8-511">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="61fa8-512">New-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="61fa8-512">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="61fa8-513">Set-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="61fa8-513">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="61fa8-514">Remove-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="61fa8-514">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="61fa8-515">Get-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="61fa8-515">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="61fa8-516">New-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="61fa8-516">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="61fa8-517">Restore-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="61fa8-517">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="61fa8-518">Remove-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="61fa8-518">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="61fa8-519">Добавлено расширенное управление политиками аудита для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="61fa8-519">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="61fa8-520">Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="61fa8-520">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="61fa8-521">Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.</span><span class="sxs-lookup"><span data-stu-id="61fa8-521">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="61fa8-522">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="61fa8-522">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="61fa8-523">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="61fa8-523">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="61fa8-524">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="61fa8-524">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="61fa8-525">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="61fa8-525">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="61fa8-526">Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="61fa8-526">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="61fa8-527">0.5.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="61fa8-527">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="61fa8-528">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="61fa8-528">General</span></span>
* <span data-ttu-id="61fa8-529">Добавлены средства заполнения ресурсов для многих основных командлетов — они позволяют вам переключать существующие имена ресурсов при вызове командлетов в интерактивном режиме</span><span class="sxs-lookup"><span data-stu-id="61fa8-529">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="61fa8-530">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="61fa8-530">Az.Profile</span></span>
* <span data-ttu-id="61fa8-531">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="61fa8-531">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="61fa8-532">В командлете Connect-AzAccount параметр TenantId переименован в Tenant и добавлен псевдоним для TenantId</span><span class="sxs-lookup"><span data-stu-id="61fa8-532">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="61fa8-533">Обновлено описание TenantId для командлета Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="61fa8-533">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="61fa8-534">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="61fa8-534">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="61fa8-535">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="61fa8-535">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="61fa8-536">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="61fa8-536">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="61fa8-537">Устранена проблема, при которой командлет Disconnect-AzAccount вызывал сбой при отсутствии подключения</span><span class="sxs-lookup"><span data-stu-id="61fa8-537">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="61fa8-538">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="61fa8-538">Az.CognitiveServices</span></span>
* <span data-ttu-id="61fa8-539">Добавлена операция Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="61fa8-539">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="61fa8-540">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="61fa8-540">Az.Compute</span></span>
* <span data-ttu-id="61fa8-541">Добавлены командлеты Add-AzVmssVMDataDisk и Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="61fa8-541">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="61fa8-542">Get-AzVMImage отображает AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="61fa8-542">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="61fa8-543">Устранена проблема, при которой значения параметров SetAzVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="61fa8-543">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="61fa8-544">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="61fa8-544">Az.DataLakeStore</span></span>
* <span data-ttu-id="61fa8-545">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="61fa8-545">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="61fa8-546">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="61fa8-546">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="61fa8-547">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="61fa8-547">Az.Insights</span></span>
* <span data-ttu-id="61fa8-548">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="61fa8-548">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="61fa8-549">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="61fa8-549">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="61fa8-550">Исправлена проблема № 7513 [Insights], при которой для командлета Set-AzDiagnosticSetting требовалось явное указание категорий во время создания параметра</span><span class="sxs-lookup"><span data-stu-id="61fa8-550">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="61fa8-551">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="61fa8-551">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="61fa8-552">Az.Network</span><span class="sxs-lookup"><span data-stu-id="61fa8-552">Az.Network</span></span>
* <span data-ttu-id="61fa8-553">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="61fa8-553">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="61fa8-554">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="61fa8-554">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="61fa8-555">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="61fa8-555">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="61fa8-556">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="61fa8-556">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="61fa8-557">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="61fa8-557">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="61fa8-558">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="61fa8-558">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="61fa8-559">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="61fa8-559">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="61fa8-560">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="61fa8-560">Az.PolicyInsights</span></span>
* <span data-ttu-id="61fa8-561">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="61fa8-561">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="61fa8-562">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="61fa8-562">Az.Resources</span></span>
* <span data-ttu-id="61fa8-563">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="61fa8-563">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="61fa8-564">Разрешено перечисление ресурсов с помощью параметра -ResourceId для командлета Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="61fa8-564">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="61fa8-565">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="61fa8-565">Az.ServiceBus</span></span>
* <span data-ttu-id="61fa8-566">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="61fa8-566">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="61fa8-567">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="61fa8-567">Az.ServiceFabric</span></span>
* <span data-ttu-id="61fa8-568">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="61fa8-568">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="61fa8-569">Исправлен командлет Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="61fa8-569">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="61fa8-570">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="61fa8-570">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="61fa8-571">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="61fa8-571">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="61fa8-572">Исправлен командлет Update-AzServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="61fa8-572">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="61fa8-573">0.4.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="61fa8-573">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="61fa8-574">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="61fa8-574">Az.Profile</span></span>
* <span data-ttu-id="61fa8-575">Устранена проблема с Get-AzSubscription в CloudShell</span><span class="sxs-lookup"><span data-stu-id="61fa8-575">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="61fa8-576">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="61fa8-576">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="61fa8-577">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="61fa8-577">Az.Compute</span></span>
* <span data-ttu-id="61fa8-578">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzVm</span><span class="sxs-lookup"><span data-stu-id="61fa8-578">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="61fa8-579">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="61fa8-579">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="61fa8-580">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="61fa8-580">Az.DataLakeStore</span></span>
* <span data-ttu-id="61fa8-581">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="61fa8-581">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="61fa8-582">Get-AzDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="61fa8-582">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="61fa8-583">Add-AzDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="61fa8-583">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="61fa8-584">Set-AzDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="61fa8-584">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="61fa8-585">Remove-AzDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="61fa8-585">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="61fa8-586">Az.Network</span><span class="sxs-lookup"><span data-stu-id="61fa8-586">Az.Network</span></span>
* <span data-ttu-id="61fa8-587">Обновлен командлет Test-AzNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="61fa8-587">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="61fa8-588">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="61fa8-588">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="61fa8-589">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="61fa8-589">Az.Resources</span></span>
* <span data-ttu-id="61fa8-590">Устранена проблема, из-за которой командлет Get-AzRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), благодаря добавлению понятного исключения в сценарий.</span><span class="sxs-lookup"><span data-stu-id="61fa8-590">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="61fa8-591">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="61fa8-591">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="61fa8-592">0.3.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="61fa8-592">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="61fa8-593">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="61fa8-593">Azure.Storage</span></span>
* <span data-ttu-id="61fa8-594">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="61fa8-594">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="61fa8-595">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="61fa8-595">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="61fa8-596">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="61fa8-596">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="61fa8-597">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="61fa8-597">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="61fa8-598">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="61fa8-598">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="61fa8-599">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="61fa8-599">Az.CognitiveServices</span></span>
* <span data-ttu-id="61fa8-600">Поддержка Get-AzCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="61fa8-600">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="61fa8-601">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="61fa8-601">Az.Compute</span></span>
* <span data-ttu-id="61fa8-602">Исправлена команда Get-AzVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов</span><span class="sxs-lookup"><span data-stu-id="61fa8-602">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="61fa8-603">Добавлен пример использования SimpleParameterSet в справку командлета New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="61fa8-603">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="61fa8-604">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="61fa8-604">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="61fa8-605">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="61fa8-605">Az.DataFactoryV2</span></span>
* <span data-ttu-id="61fa8-606">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="61fa8-606">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="61fa8-607">Az.Network</span><span class="sxs-lookup"><span data-stu-id="61fa8-607">Az.Network</span></span>
* <span data-ttu-id="61fa8-608">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="61fa8-608">Added NetworkProfile functionality.</span></span> <span data-ttu-id="61fa8-609">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="61fa8-609">new cmdlets added</span></span>
    - <span data-ttu-id="61fa8-610">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="61fa8-610">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="61fa8-611">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="61fa8-611">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="61fa8-612">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="61fa8-612">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="61fa8-613">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="61fa8-613">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="61fa8-614">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="61fa8-614">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="61fa8-615">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="61fa8-615">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="61fa8-616">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="61fa8-616">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="61fa8-617">Добавлены командлеты: New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="61fa8-617">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="61fa8-618">Добавлены командлеты: Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="61fa8-618">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="61fa8-619">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="61fa8-619">Az.RedisCache</span></span>
* <span data-ttu-id="61fa8-620">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="61fa8-620">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="61fa8-621">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="61fa8-621">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="61fa8-622">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="61fa8-622">Az.Resources</span></span>
* <span data-ttu-id="61fa8-623">Добавлен отсутствующий параметр -Mode в командлет Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="61fa8-623">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="61fa8-624">Исправлена ошибка командлета Get-AzProviderOperation для операций, когда Origin содержит User</span><span class="sxs-lookup"><span data-stu-id="61fa8-624">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="61fa8-625">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="61fa8-625">Az.Sql</span></span>
* <span data-ttu-id="61fa8-626">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="61fa8-626">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="61fa8-627">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="61fa8-627">Az.Websites</span></span>
* <span data-ttu-id="61fa8-628">Новый командлет Get-AzWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="61fa8-628">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="61fa8-629">Новые командлеты New-AzWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows</span><span class="sxs-lookup"><span data-stu-id="61fa8-629">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="61fa8-630">0.2.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="61fa8-630">0.2.0 - September 2018</span></span>
 <span data-ttu-id="61fa8-631">Первый выпуск</span><span class="sxs-lookup"><span data-stu-id="61fa8-631">Initial Release</span></span>