---
ms.openlocfilehash: 911e1f7ff56feab2735f397a0128aab4aa7757c7
ms.sourcegitcommit: 0c012450805bef75472f48c74fe488baf6ba53bb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2019
ms.locfileid: "66498681"
---
## <a name="220---june-2019"></a><span data-ttu-id="f7f3b-101">2.2.0 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-101">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="f7f3b-102">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f7f3b-102">Az.Cdn</span></span>
* <span data-ttu-id="f7f3b-103">Обновлены командлеты для поддержки функции rulesEngine на основе API версии 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-103">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f7f3b-104">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f7f3b-104">Az.Compute</span></span>
* <span data-ttu-id="f7f3b-105">Добавлен параметр `NoWait`, который запускает операцию и немедленно возвращает значение еще до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-105">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="f7f3b-106">Обновлены командлеты:   Export-AzLogAnalyticRequestRateByInterval; Export-AzLogAnalyticThrottledRequest; Remove-AzVM; Remove-AzVMAccessExtension; Remove-AzVMAEMExtension; Remove-AzVMChefExtension; Remove-AzVMCustomScriptExtension; Remove-AzVMDiagnosticsExtension; Remove-AzVMDiskEncryptionExtension; Remove-AzVMDscExtension; Remove-AzVMSqlServerExtension; Restart-AzVM; Set-AzVM; Set-AzVMAccessExtension; Set-AzVMADDomainExtension; Set-AzVMAEMExtension; Set-AzVMBginfoExtension; Set-AzVMChefExtension; Set-AzVMCustomScriptExtension; Set-AzVMDiagnosticsExtension; Set-AzVMDscExtension; Set-AzVMExtension; Start-AzVM; Stop-AzVM; Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-106">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f7f3b-107">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f7f3b-107">Az.EventHub</span></span>
* <span data-ttu-id="f7f3b-108">Исправлена ошибка № 9231. Командлет Get-AzEventHubNamespace не возвращал теги.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-108">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="f7f3b-109">Исправлена ошибка № 9230. Командлет Get-AzEventHubNamespace возвращал значение ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-109">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f7f3b-110">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f7f3b-110">Az.Network</span></span>
* <span data-ttu-id="f7f3b-111">Обновлены параметры ResourceId и InputObject для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-111">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="f7f3b-112">Добавлены псевдонимы для параметров ResourceId и InputObject.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-112">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f7f3b-113">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f7f3b-113">Az.PolicyInsights</span></span>
* <span data-ttu-id="f7f3b-114">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyEvent.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-114">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f7f3b-115">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f7f3b-115">Az.RecoveryServices</span></span>
* <span data-ttu-id="f7f3b-116">Минимальный срок хранения политики IaaSVM изменился с 1 до 7 дней.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-116">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f7f3b-117">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f7f3b-117">Az.ServiceBus</span></span>
* <span data-ttu-id="f7f3b-118">Исправлена ошибка № 9182. Командлет Get-AzServiceBusNamespace возвращал ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-118">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f7f3b-119">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f7f3b-119">Az.ServiceFabric</span></span>
* <span data-ttu-id="f7f3b-120">Исправлена опечатка в сообщении об ошибке для командлета Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-120">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="f7f3b-121">Исправлен отсутствующей символ в командных строках Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-121">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="f7f3b-122">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f7f3b-122">Az.Sql</span></span>
* <span data-ttu-id="f7f3b-123">Для командлета New-AzureSqlInstance добавлен параметр DnsZonePartner, обеспечивающий поддержку AutoDr для Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-123">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="f7f3b-124">Командлет Get-AzSqlDatabaseSecureConnectionPolicy объявлен неподдерживаемым.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-124">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="f7f3b-125">Командлеты обнаружения угроз переименованы в командлеты Расширенной защиты от угроз.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-125">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="f7f3b-126">Параметры -StorageSizeInGB и -LicenseType командлета New-AzSqlInstance теперь необязательны.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-126">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f7f3b-127">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f7f3b-127">Az.Websites</span></span>
* <span data-ttu-id="f7f3b-128">Исправлены проблемы, когда удалялись теги при использовании Set-AzWebApp и Set-AzWebAppSlot со свойством -WebApp.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-128">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="f7f3b-129">2.1.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-129">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="f7f3b-130">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f7f3b-130">Az.ApiManagement</span></span>
* <span data-ttu-id="f7f3b-131">Созданы командлеты для управления диагностикой в глобальной области и в области API.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-131">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="f7f3b-132">**Get-AzApiManagementDiagnostic** — получение диагностики, заданной глобально или на уровне области API.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-132">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="f7f3b-133">**New-AzApiManagementDiagnostic** — создание диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-133">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="f7f3b-134">**New-AzApiManagementHttpMessageDiagnostic** — создание параметра диагностики, для которого регистрируются заголовки и размер байтов тела.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-134">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="f7f3b-135">**New-AzApiManagementPipelineDiagnosticSetting** — создание параметров диагностики для сообщений HTTP, поступающих в шлюз или исходящих из него.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-135">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="f7f3b-136">**New-AzApiManagementSamplingSetting** — создание параметра выборки для запросов и ответов касательно диагностики.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-136">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="f7f3b-137">**Remove-AzApiManagementDiagnostic** — удаление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-137">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="f7f3b-138">**Set-AzApiManagementDiagnostic** — обновление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-138">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="f7f3b-139">Созданы командлеты для управления кэшем в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-139">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="f7f3b-140">**Get-AzApiManagementCache** — получение сведений о кэше, указанном идентификатором, или обо всех кэшах.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-140">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="f7f3b-141">**New-AzApiManagementCache** — создание кэша по умолчанию или кэша в определенном регионе Azure.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-141">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="f7f3b-142">**Remove-AzApiManagementCache** — удаление кэша.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-142">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="f7f3b-143">**Update-AzApiManagementCache** — обновление кэша.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-143">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="f7f3b-144">Созданы командлеты для управления схемой API.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-144">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="f7f3b-145">**New-AzApiManagementSchema** — создание схемы для API.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-145">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="f7f3b-146">**Get-AzApiManagementSchema** — получение схем, настроенных в API.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-146">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="f7f3b-147">**Remove-AzApiManagementSchema** — удаление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-147">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="f7f3b-148">**Set-AzApiManagementSchema** — обновление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-148">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="f7f3b-149">Создан командлет для создания токена пользователя.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-149">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="f7f3b-150">**New-AzApiManagementUserToken** — создание токена пользователя, по умолчанию действительного в течение 8 часов. С помощью этого командлета можно создавать токен для пользователя GIT.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-150">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="f7f3b-151">Создан командлет для получения состояния сети.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-151">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="f7f3b-152">**Get-AzApiManagementNetworkStatus** — получение состояния сети ресурсов, от которых зависит служба "Управление API".</span><span class="sxs-lookup"><span data-stu-id="f7f3b-152">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="f7f3b-153">Это полезно при развертывании службы ApiManagement в виртуальной сети и проверке того, не нарушена ли какая-либо из зависимостей.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-153">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="f7f3b-154">Обновлен командлет **New-AzApiManagement** для управления службой ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-154">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="f7f3b-155">Добавлена поддержка нового SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-155">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="f7f3b-156">Добавлена поддержка для включения флага EnableClientCertificate в SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-156">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="f7f3b-157">Новый командлет **New-AzApiManagementSslSetting** позволяет настраивать параметр TLS/SSL для сервера (Backend) и внешнего интерфейса (Frontend).</span><span class="sxs-lookup"><span data-stu-id="f7f3b-157">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="f7f3b-158">Его также можно использовать для настройки Ciphers как 3DES, в ServerProtocols как Http2 для внешнего интерфейса (Frontend) службы ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-158">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="f7f3b-159">Добавлена поддержка настройки имени узла DeveloperPortal в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-159">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="f7f3b-160">Обновлен командлет **Get-AzApiManagementSsoToken** для извлечения объекта PsApiManagement в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-160">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="f7f3b-161">Обновлен командлет для отображения встроенных сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-161">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="f7f3b-162">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Код ошибки: ValidationError. Сообщение об ошибке: "Некоторые поля содержат неправильные значения". Сведения об ошибке: [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="f7f3b-162">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="f7f3b-163">Обновлен командлет **Export-AzApiManagementApi** для экспортирования программных интерфейсов в формате OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-163">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="f7f3b-164">Обновлен командлет **Import-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="f7f3b-164">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="f7f3b-165">Для импортирования API из спецификации документа OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-165">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="f7f3b-166">Для переопределения свойства PsApiManagementSchema, указанного в любом документе (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="f7f3b-166">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="f7f3b-167">Для переопределения свойства ServiceUrl, указанного в любом документе.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-167">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="f7f3b-168">Обновлен командлет **Get-AzApiManagementPolicy** для возврата политики в формате, экранированном не для XML, с использованием rawxml.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-168">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="f7f3b-169">Обновлен командлет **Set-AzApiManagementPolicy**. Он принимает политику в формате, экранированном не для XML, с использованием rawxml и в формате, экранированном для XML, с использованием XML.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-169">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="f7f3b-170">Обновлен командлет **New-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="f7f3b-170">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="f7f3b-171">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-171">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="f7f3b-172">Для создания API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-172">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="f7f3b-173">Для клонирования API с использованием значений SourceApiId и SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-173">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="f7f3b-174">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-174">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="f7f3b-175">Обновлен командлет **Set-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="f7f3b-175">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="f7f3b-176">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-176">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="f7f3b-177">Для обновления API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-177">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="f7f3b-178">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-178">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="f7f3b-179">Обновлен командлет **New-AzApiManagementRevision**:</span><span class="sxs-lookup"><span data-stu-id="f7f3b-179">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="f7f3b-180">Для клонирования (копирования тегов, продуктов, операций и политик) существующей редакции с использованием SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-180">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="f7f3b-181">Новая редакция предполагает родительский идентификатор ApiId.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-181">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="f7f3b-182">Для предоставления ApiRevisionDescription.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-182">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="f7f3b-183">Для переопределения значения ServiceUrl при клонировании API.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-183">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="f7f3b-184">Обновлен командлет **New-AzApiManagementIdentityProvider**:</span><span class="sxs-lookup"><span data-stu-id="f7f3b-184">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="f7f3b-185">Для настройки AAD или AADB2C с Authority.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-185">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="f7f3b-186">Для установки политик SignupPolicy, SigninPolicy, ProfileEditingPolicy и PasswordResetPolicy.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-186">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="f7f3b-187">Обновлен командлет **New-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-187">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="f7f3b-188">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-188">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="f7f3b-189">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-189">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="f7f3b-190">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-190">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="f7f3b-191">Обновлен командлет **Set-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-191">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="f7f3b-192">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-192">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="f7f3b-193">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-193">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="f7f3b-194">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-194">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="f7f3b-195">Следующие командлеты обновлены, чтобы принимать значение ResourceId в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-195">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="f7f3b-196">New-AzApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-196">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="f7f3b-197">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="f7f3b-197">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="f7f3b-198">Get-AzApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-198">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="f7f3b-199">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="f7f3b-199">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="f7f3b-200">Get-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-200">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="f7f3b-201">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="f7f3b-201">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="f7f3b-202">Get-AzApiManagementAuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-202">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="f7f3b-203">Get-AzApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-203">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="f7f3b-204">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="f7f3b-204">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="f7f3b-205">Get-AzApiManagementCertificate.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-205">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="f7f3b-206">Remove-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-206">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="f7f3b-207">Remove-AzApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-207">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f7f3b-208">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f7f3b-208">Az.Automation</span></span>
* <span data-ttu-id="f7f3b-209">Обновлен командлет Get-AzAutomationJobOutputRecord для обработки значений в формате JSON и в виде текстовой записи.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-209">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="f7f3b-210">исправлена проблема https://github.com/Azure/azure-powershell/issues/7977.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-210">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="f7f3b-211">исправлена проблема https://github.com/Azure/azure-powershell/issues/8600.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-211">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="f7f3b-212">Поведение командлета Start-AzAutomationDscCompilationJob изменено так, чтобы сразу же запустить задание, а не ждать его завершения.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-212">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="f7f3b-213">исправлена проблема https://github.com/Azure/azure-powershell/issues/8347.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-213">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="f7f3b-214">Исправлен командлет Get-AzAutomationDscNode, возвращающий все узлы при использовании -Name.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-214">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="f7f3b-215">Теперь он возвращает только соответствующий узел.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-215">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f7f3b-216">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f7f3b-216">Az.Compute</span></span>
* <span data-ttu-id="f7f3b-217">Добавлены параметры ProtectFromScaleIn и ProtectFromScaleSetAction для командлета Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-217">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="f7f3b-218">Командлет New-AzVM с простым набором параметров теперь по умолчанию использует доступное расположение, если регион "восточная часть США" не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-218">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f7f3b-219">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f7f3b-219">Az.DataLakeStore</span></span>
* <span data-ttu-id="f7f3b-220">Обновлен пакет SDK ADLS для использования httpclient. В инфраструктуру Azure интегрирована проверка плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-220">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f7f3b-221">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f7f3b-221">Az.Monitor</span></span>
* <span data-ttu-id="f7f3b-222">Исправлены неправильные имена параметров в справочных примерах.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-222">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f7f3b-223">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f7f3b-223">Az.Network</span></span>
* <span data-ttu-id="f7f3b-224">Добавлен флаг DisableBgpRoutePropagation для выходных данных действующей таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-224">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="f7f3b-225">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="f7f3b-225">Updated cmdlet:</span></span>
        - <span data-ttu-id="f7f3b-226">Get-AzEffectiveRouteTable.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-226">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="f7f3b-227">Исправлен двойной дефис в документации New-AzApplicationGatewayTrustedRootCertificate.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-227">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="f7f3b-228">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f7f3b-228">Az.Resources</span></span>
* <span data-ttu-id="f7f3b-229">Добавлен новый командлет Get-AzureRmDenyAssignment для получения запрещающих назначений.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-229">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="f7f3b-230">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f7f3b-230">Az.Sql</span></span>
* <span data-ttu-id="f7f3b-231">Командлеты Расширенной защиты от угроз переименованы на командлеты Расширенной защиты данных, и оценка уязвимости включена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-231">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="f7f3b-232">2.0.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-232">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f7f3b-233">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f7f3b-233">Az.Accounts</span></span>
* <span data-ttu-id="f7f3b-234">Обновлена библиотека аутентификации для устранения проблем с ADFS при использовании аутентификации на основе имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-234">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f7f3b-235">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f7f3b-235">Az.CognitiveServices</span></span>
* <span data-ttu-id="f7f3b-236">Отображается только заявление об отказе Bing для служб Поиска Bing.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-236">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="f7f3b-237">Исправлена проблема с созданием учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-237">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f7f3b-238">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f7f3b-238">Az.Compute</span></span>
* <span data-ttu-id="f7f3b-239">Функция группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-239">Proximity placement group feature.</span></span>
    - <span data-ttu-id="f7f3b-240">Добавлены следующие новые командлеты:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="f7f3b-240">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="f7f3b-241">Новый параметр ProximityPlacementGroupId будет добавлен в следующие командлеты:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="f7f3b-241">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="f7f3b-242">В командлет New-AzGalleryImageVersion добавлен параметр StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-242">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="f7f3b-243">TargetRegion в командлете New-AzGalleryImageVersion может содержать StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-243">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="f7f3b-244">Параметр-переключатель SkipShutdown добавлен в командлеты Stop-AzVM и Stop-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-244">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="f7f3b-245">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="f7f3b-245">Breaking changes</span></span>
    - <span data-ttu-id="f7f3b-246">Командлет SET-AzVMBootDiagnostics изменен на Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-246">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="f7f3b-247">Командлет Export-AzLogAnalyticThrottledRequests изменен на Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-247">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="f7f3b-248">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="f7f3b-248">Az.DeploymentManager</span></span>
* <span data-ttu-id="f7f3b-249">Первая общедоступная версия командлетов диспетчера развертывания Azure</span><span class="sxs-lookup"><span data-stu-id="f7f3b-249">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="f7f3b-250">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="f7f3b-250">Az.Dns</span></span>
* <span data-ttu-id="f7f3b-251">Автоматическое делегирование DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="f7f3b-251">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="f7f3b-252">Командлет для создания зоны DNS принимает имя родительской зоны в качестве дополнительного необязательного параметра.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-252">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="f7f3b-253">Он добавляет записи NS в родительской зоне для созданной дочерней зоны.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-253">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f7f3b-254">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f7f3b-254">Az.FrontDoor</span></span>
* <span data-ttu-id="f7f3b-255">Первая общедоступная версия командлетов Azure FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-255">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="f7f3b-256">Переименованы командлеты WAF для включения Waf.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-256">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="f7f3b-257">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f7f3b-257">Az.HDInsight</span></span>
* <span data-ttu-id="f7f3b-258">Удалены два командлета:</span><span class="sxs-lookup"><span data-stu-id="f7f3b-258">Removed two cmdlets:</span></span>
    - <span data-ttu-id="f7f3b-259">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f7f3b-259">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="f7f3b-260">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f7f3b-260">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="f7f3b-261">Добавлен новый командлет Set-AzHDInsightGatewayCredential для замены Grant-AzHDInsightHttpServicesAccess.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-261">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="f7f3b-262">Обновлен командлет Get-AzHDInsightJobOutput для различения ролей читателя и оператора HDInsight:</span><span class="sxs-lookup"><span data-stu-id="f7f3b-262">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="f7f3b-263">Пользователям с ролью читателя не нужно указывать параметр DefaultStorageAccountKey явным образом, иначе возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-263">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="f7f3b-264">На пользователей с ролью оператора HDInsight это не повлияет.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-264">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f7f3b-265">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f7f3b-265">Az.Monitor</span></span>
* <span data-ttu-id="f7f3b-266">Новые командлеты для API SQR (запланированное правило запросов)</span><span class="sxs-lookup"><span data-stu-id="f7f3b-266">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="f7f3b-267">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="f7f3b-267">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="f7f3b-268">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="f7f3b-268">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="f7f3b-269">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="f7f3b-269">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="f7f3b-270">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="f7f3b-270">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="f7f3b-271">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="f7f3b-271">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="f7f3b-272">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="f7f3b-272">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="f7f3b-273">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f7f3b-273">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f7f3b-274">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f7f3b-274">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f7f3b-275">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f7f3b-275">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f7f3b-276">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f7f3b-276">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f7f3b-277">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f7f3b-277">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f7f3b-278">См. подробнее об [API SQR](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules).</span><span class="sxs-lookup"><span data-stu-id="f7f3b-278">[More](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="f7f3b-279">Обновлен файл Az.Monitor.md для включения командлетов для правила генерации оповещений на основе метрик GenV2(не классическая версия).</span><span class="sxs-lookup"><span data-stu-id="f7f3b-279">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f7f3b-280">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f7f3b-280">Az.Network</span></span>
* <span data-ttu-id="f7f3b-281">Добавлена поддержка для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-281">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="f7f3b-282">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="f7f3b-282">New cmdlets</span></span>
        - <span data-ttu-id="f7f3b-283">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f7f3b-283">New-AzNatGateway</span></span>
        - <span data-ttu-id="f7f3b-284">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f7f3b-284">Get-AzNatGateway</span></span>
        - <span data-ttu-id="f7f3b-285">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f7f3b-285">Set-AzNatGateway</span></span>
        - <span data-ttu-id="f7f3b-286">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f7f3b-286">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="f7f3b-287">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="f7f3b-287">Updated cmdlets</span></span>
        - <span data-ttu-id="f7f3b-288">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="f7f3b-288">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="f7f3b-289">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="f7f3b-289">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="f7f3b-290">Обновлены следующие команды для функции: Настройка и удаление пользовательских маршрутов через шлюз в Бруклине.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-290">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="f7f3b-291">Обновлен командлет New-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-291">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="f7f3b-292">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-292">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f7f3b-293">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f7f3b-293">Az.PolicyInsights</span></span>
* <span data-ttu-id="f7f3b-294">Добавлена поддержка сведений об оценке политики запросов.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-294">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="f7f3b-295">Добавлен параметр -Expand в командлет Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-295">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="f7f3b-296">Добавлена поддержка -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-296">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f7f3b-297">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f7f3b-297">Az.RecoveryServices</span></span>
* <span data-ttu-id="f7f3b-298">Добавлена поддержка перекрестной подписки на Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-298">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="f7f3b-299">Добавлена возможность отмечать предстоящие критически важные изменения для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-299">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="f7f3b-300">Исправлены план восстановления и план действий для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-300">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="f7f3b-301">Исправлено сетевое сопоставление обновления Azure Site Recovery (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="f7f3b-301">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="f7f3b-302">Исправлено направление защиты обновления Azure Site Recovery для управляемых дисков (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="f7f3b-302">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="f7f3b-303">Добавлены другие незначительные исправления.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-303">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="f7f3b-304">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="f7f3b-304">Az.Relay</span></span>
* <span data-ttu-id="f7f3b-305">Исправлены опечатки в сообщениях для клиентов.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-305">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f7f3b-306">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f7f3b-306">Az.ServiceBus</span></span>
* <span data-ttu-id="f7f3b-307">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-307">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f7f3b-308">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f7f3b-308">Az.Storage</span></span>
* <span data-ttu-id="f7f3b-309">Выполнено обновление клиентской библиотеки хранилища до версии 10.0.1 (пространство имен всех объектов из этого пакета SDK изменено с Microsoft.WindowsAzure.Storage. *на Microsoft.Azure.Storage*).</span><span class="sxs-lookup"><span data-stu-id="f7f3b-309">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="f7f3b-310">Выполнено обновление до Microsoft.Azure.Management.Storage версии 11.0.0 для включения поддержки нового API версии 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-310">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="f7f3b-311">Значение свойства Kind по умолчанию в учетной записи хранения изменено со Storage на StorageV2.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-311">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="f7f3b-312">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f7f3b-312">New-AzStorageAccount</span></span>
* <span data-ttu-id="f7f3b-313">Изменено значение Sku.Name в выходных данных командлета учетной записи хранения в соответствии со значением Sku.Name во входных данных путем добавления _ (например, StandardLRS изменено на Standard_LRS).</span><span class="sxs-lookup"><span data-stu-id="f7f3b-313">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="f7f3b-314">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f7f3b-314">New-AzStorageAccount</span></span>
    - <span data-ttu-id="f7f3b-315">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f7f3b-315">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="f7f3b-316">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f7f3b-316">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f7f3b-317">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f7f3b-317">Az.Websites</span></span>
* <span data-ttu-id="f7f3b-318">Свойство Kind теперь будет задаваться объектам PSSite, возвращаемым командлетом Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-318">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="f7f3b-319">Get-AzWebApp\*Metrics и Get-AzAppServicePlanMetrics считаются нерекомендуемыми.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-319">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="f7f3b-320">1.8.0 — апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-320">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f7f3b-321">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="f7f3b-321">Highlights since the last major release</span></span>
* <span data-ttu-id="f7f3b-322">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-322">General availability of `Az` module</span></span>
* <span data-ttu-id="f7f3b-323">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="f7f3b-323">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="f7f3b-324">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="f7f3b-324">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="f7f3b-325">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-325">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="f7f3b-326">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-326">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f7f3b-327">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-327">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="f7f3b-328">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="f7f3b-328">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f7f3b-329">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f7f3b-329">Az.Accounts</span></span>
* <span data-ttu-id="f7f3b-330">Обновлен командлет Uninstall-AzureRm для правильного удаления модулей в Mac.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-330">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f7f3b-331">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f7f3b-331">Az.Batch</span></span>
* <span data-ttu-id="f7f3b-332">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-332">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f7f3b-333">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f7f3b-333">Az.Cdn</span></span>
* <span data-ttu-id="f7f3b-334">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-334">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f7f3b-335">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f7f3b-335">Az.CognitiveServices</span></span>
* <span data-ttu-id="f7f3b-336">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-336">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f7f3b-337">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f7f3b-337">Az.Compute</span></span>
* <span data-ttu-id="f7f3b-338">Устранена проблема с установкой AEM, если в идентификаторах ресурсов дисков группа ресурсов указана в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-338">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="f7f3b-339">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-339">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f7f3b-340">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-340">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f7f3b-341">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f7f3b-341">Az.DataFactory</span></span>
* <span data-ttu-id="f7f3b-342">Добавлены свойства SsisProperties, если NodeCount не имеет значения NULL для управляемой среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-342">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f7f3b-343">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f7f3b-343">Az.DataLakeStore</span></span>
* <span data-ttu-id="f7f3b-344">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-344">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f7f3b-345">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f7f3b-345">Az.EventGrid</span></span>
* <span data-ttu-id="f7f3b-346">Обновлен текст справки для конечной точки, указывающий, что необходимо создать ресурсы, прежде чем использовать командлеты для создания или обновления подписки на события.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-346">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f7f3b-347">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f7f3b-347">Az.EventHub</span></span>
* <span data-ttu-id="f7f3b-348">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-348">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="f7f3b-349">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f7f3b-349">Az.HDInsight</span></span>
* <span data-ttu-id="f7f3b-350">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-350">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f7f3b-351">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f7f3b-351">Az.IotHub</span></span>
* <span data-ttu-id="f7f3b-352">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-352">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f7f3b-353">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f7f3b-353">Az.KeyVault</span></span>
* <span data-ttu-id="f7f3b-354">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-354">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f7f3b-355">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-355">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="f7f3b-356">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="f7f3b-356">Az.MachineLearning</span></span>
* <span data-ttu-id="f7f3b-357">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-357">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="f7f3b-358">Az.Media</span><span class="sxs-lookup"><span data-stu-id="f7f3b-358">Az.Media</span></span>
* <span data-ttu-id="f7f3b-359">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-359">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f7f3b-360">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f7f3b-360">Az.Monitor</span></span>
  * <span data-ttu-id="f7f3b-361">Добавлены новые командлеты для правила генерации оповещений на основе метрик GenV2 (не классических).</span><span class="sxs-lookup"><span data-stu-id="f7f3b-361">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="f7f3b-362">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="f7f3b-362">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="f7f3b-363">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="f7f3b-363">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="f7f3b-364">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f7f3b-364">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="f7f3b-365">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f7f3b-365">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="f7f3b-366">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f7f3b-366">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="f7f3b-367">Обновлен пакет SDK Monitor до предварительной версии 0.22.0.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-367">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f7f3b-368">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f7f3b-368">Az.Network</span></span>
* <span data-ttu-id="f7f3b-369">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-369">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f7f3b-370">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-370">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="f7f3b-371">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="f7f3b-371">Az.NotificationHubs</span></span>
* <span data-ttu-id="f7f3b-372">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-372">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f7f3b-373">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f7f3b-373">Az.OperationalInsights</span></span>
* <span data-ttu-id="f7f3b-374">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-374">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="f7f3b-375">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="f7f3b-375">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="f7f3b-376">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-376">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f7f3b-377">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f7f3b-377">Az.RecoveryServices</span></span>
* <span data-ttu-id="f7f3b-378">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-378">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f7f3b-379">Обновлен табличный формат для SQL на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-379">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="f7f3b-380">Добавлен альтернативный метод для получения расположения в Общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-380">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="f7f3b-381">Обновлено значение ScheduleRunDays в объекте SchedulePolicy в соответствии с часовым поясом.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-381">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f7f3b-382">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f7f3b-382">Az.RedisCache</span></span>
* <span data-ttu-id="f7f3b-383">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-383">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f7f3b-384">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f7f3b-384">Az.Resources</span></span>
* <span data-ttu-id="f7f3b-385">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-385">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="f7f3b-386">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f7f3b-386">Az.Sql</span></span>
* <span data-ttu-id="f7f3b-387">Заменена зависимость от пакета SDK монитора на обычный код.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-387">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="f7f3b-388">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-388">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f7f3b-389">Улучшен процесс классификации нескольких столбцов.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-389">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="f7f3b-390">Добавлены свойства SKU (имя, семейство, производительность SKU) в отклике Get-AzSqlServerServiceObjective, а также по умолчанию задан табличный формат.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-390">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="f7f3b-391">C помощью Get-AzSqlServerServiceObjective теперь можно получать список доступных целевых служб по расположению без необходимости заранее размещать сервер в регионе.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-391">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="f7f3b-392">Поддерживается параметр часового пояса при создании Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-392">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="f7f3b-393">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-393">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f7f3b-394">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f7f3b-394">Az.Websites</span></span>
* <span data-ttu-id="f7f3b-395">Исправлены командлеты Set-AzWebApp и Set-AzWebAppSlot, которые теперь не удаляют теги при выполнении.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-395">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="f7f3b-396">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-396">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f7f3b-397">Обновлен пакет SDK веб-узлов.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-397">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="f7f3b-398">Удалено свойство AdminSiteName из PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-398">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="f7f3b-399">1.7.0 —апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-399">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f7f3b-400">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="f7f3b-400">Highlights since the last major release</span></span>
* <span data-ttu-id="f7f3b-401">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-401">General availability of `Az` module</span></span>
* <span data-ttu-id="f7f3b-402">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="f7f3b-402">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="f7f3b-403">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="f7f3b-403">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="f7f3b-404">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-404">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="f7f3b-405">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-405">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f7f3b-406">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-406">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="f7f3b-407">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="f7f3b-407">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f7f3b-408">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f7f3b-408">Az.Accounts</span></span>
* <span data-ttu-id="f7f3b-409">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметр AzureAnalysisServicesEndpointResourceId.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-409">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f7f3b-410">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f7f3b-410">Az.AnalysisServices</span></span>
* <span data-ttu-id="f7f3b-411">Использование ServiceClient в командлетах плоскости данных и удаление исходной логики проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-411">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="f7f3b-412">Add-AzureASAccount используется как оболочка для Connect-AzAccount во избежание критических изменений.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-412">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f7f3b-413">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f7f3b-413">Az.Automation</span></span>
* <span data-ttu-id="f7f3b-414">Исправлена ошибка командлета New-AzAutomationSoftwareUpdateConfiguration, связанная с включением.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-414">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="f7f3b-415">Теперь параметры IncludedKbNumber и IncludedPackageNameMask должны работать нормально.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-415">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="f7f3b-416">Исправлена ошибка динамической группы управления обновлениями службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-416">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f7f3b-417">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f7f3b-417">Az.Compute</span></span>
* <span data-ttu-id="f7f3b-418">В командлеты New-AzDiskConfig и New-AzSnapshotConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-418">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="f7f3b-419">Теперь можно создавать виртуальные машину на основе образов из коллекции от других клиентов.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-419">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="f7f3b-420">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f7f3b-420">Az.ContainerInstance</span></span>
* <span data-ttu-id="f7f3b-421">Исправлена проблема в параметре -Command командлета New-AzContainerGroup, из-за которой в конце добавлялся пустой аргумент.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-421">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f7f3b-422">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f7f3b-422">Az.DataFactory</span></span>
* <span data-ttu-id="f7f3b-423">Пакет SDK для ADF .NET обновлен до версии 3.0.2.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-423">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="f7f3b-424">Командлет Set-AzDataFactoryV2 обновлен с помощью дополнительных параметров для настроек, связанных с RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-424">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f7f3b-425">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f7f3b-425">Az.Resources</span></span>
* <span data-ttu-id="f7f3b-426">Улучшена обработка поставщиков Get-AzResource при предоставлении параметров -ResourceId или -ResourceGroupName, -Name и -ResourceType.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-426">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="f7f3b-427">Улучшена обработка ошибок в командлетах Test-AzDeployment и Test-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-427">Improve error handling for for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="f7f3b-428">Теперь ошибки, возникающие за пределами проверки развертывания, обрабатываются и включаются в выходные данные команды.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-428">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="f7f3b-429">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-429">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="f7f3b-430">Добавлен параметр-переключатель -IgnoreDynamicParameters, с помощью которого можно настроить командлеты развертывания так, чтобы они пропускали запросы в сценариях скриптов и заданий.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-430">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="f7f3b-431">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-431">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="f7f3b-432">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f7f3b-432">Az.Sql</span></span>
* <span data-ttu-id="f7f3b-433">Поддержка классификации данных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-433">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f7f3b-434">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f7f3b-434">Az.Storage</span></span>
* <span data-ttu-id="f7f3b-435">Подробные сообщения об ошибке передаются при создании контекста хранилища с помощью параметра -UseConnectedAccount, но без входа в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-435">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="f7f3b-436">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f7f3b-436">New-AzStorageContext</span></span>
* <span data-ttu-id="f7f3b-437">Поддержка свойств службы управления BLOB-объектов в указанной учетной записи хранения с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-437">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="f7f3b-438">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="f7f3b-438">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="f7f3b-439">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="f7f3b-439">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="f7f3b-440">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f7f3b-440">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="f7f3b-441">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f7f3b-441">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="f7f3b-442">Поддержка параметра -AsJob в командлетах для отправки и скачивания больших двоичных объектов и файлов.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-442">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="f7f3b-443">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f7f3b-443">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="f7f3b-444">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f7f3b-444">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="f7f3b-445">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f7f3b-445">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="f7f3b-446">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f7f3b-446">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="f7f3b-447">1.6.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-447">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f7f3b-448">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="f7f3b-448">Highlights since the last major release</span></span>
* <span data-ttu-id="f7f3b-449">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-449">General availability of `Az` module</span></span>
* <span data-ttu-id="f7f3b-450">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="f7f3b-450">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="f7f3b-451">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="f7f3b-451">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="f7f3b-452">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-452">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="f7f3b-453">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-453">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f7f3b-454">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-454">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="f7f3b-455">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="f7f3b-455">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f7f3b-456">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f7f3b-456">Az.Automation</span></span>
* <span data-ttu-id="f7f3b-457">В управление обновлениями службы автоматизации Azure внесены изменения для поддержки следующих новых функций:</span><span class="sxs-lookup"><span data-stu-id="f7f3b-457">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="f7f3b-458">динамическое группирование;</span><span class="sxs-lookup"><span data-stu-id="f7f3b-458">Dynamic grouping</span></span>
    * <span data-ttu-id="f7f3b-459">скрипты предварительного или последующего выполнения;</span><span class="sxs-lookup"><span data-stu-id="f7f3b-459">Pre-Post script</span></span>
    * <span data-ttu-id="f7f3b-460">параметр перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-460">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f7f3b-461">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f7f3b-461">Az.Compute</span></span>
* <span data-ttu-id="f7f3b-462">Устранена проблема, связанная с разрешением пути в Get-AzVmBootDiagnosticsData.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-462">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="f7f3b-463">Обновление клиентской библиотеки вычислений до версии 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-463">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f7f3b-464">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f7f3b-464">Az.KeyVault</span></span>
* <span data-ttu-id="f7f3b-465">Добавлена поддержка подстановочных знаков в командлетах KeyVault.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-465">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f7f3b-466">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f7f3b-466">Az.Network</span></span>
* <span data-ttu-id="f7f3b-467">Добавлена поддержка анализа угроз для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-467">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="f7f3b-468">Добавлены настраиваемые правила и ресурс верхнего уровня для политики брандмауэра Шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-468">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f7f3b-469">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f7f3b-469">Az.RecoveryServices</span></span>
* <span data-ttu-id="f7f3b-470">В политику виртуальной машины Azure добавлен объект SnapshotRetentionInDays для поддержки мгновенного восстановления.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-470">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="f7f3b-471">Добавлена поддержка канала для отмены регистрации контейнера.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-471">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="f7f3b-472">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f7f3b-472">Az.Resources</span></span>
* <span data-ttu-id="f7f3b-473">Обновлена поддержка подстановочных знаков для Get-AzResource и Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-473">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="f7f3b-474">Обновлены учетные данные, используемые при общих вызовах к ARM.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-474">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="f7f3b-475">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f7f3b-475">Az.Sql</span></span>
* <span data-ttu-id="f7f3b-476">Изменен тип параметра (ExcludeDetectionType) командлетов для обнаружения угроз с DetectionTypes на string[] для поддержки актуального состояния при добавлении новых типов обнаружения и для поддержки автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-476">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f7f3b-477">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f7f3b-477">Az.Storage</span></span>
* <span data-ttu-id="f7f3b-478">Поддержка получения, настройки и удаления политики управления в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-478">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="f7f3b-479">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f7f3b-479">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="f7f3b-480">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f7f3b-480">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="f7f3b-481">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f7f3b-481">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="f7f3b-482">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="f7f3b-482">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="f7f3b-483">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="f7f3b-483">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="f7f3b-484">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="f7f3b-484">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f7f3b-485">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f7f3b-485">Az.Websites</span></span>
* <span data-ttu-id="f7f3b-486">Исправлена ошибка с шаблоном ARM, из-за которой прерывалось клонирование все слотов при использовании New-AzWebApp -IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-486">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="f7f3b-487">1.5.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-487">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f7f3b-488">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f7f3b-488">Az.Accounts</span></span>
* <span data-ttu-id="f7f3b-489">Добавлена команда Register-AzModule для поддержки созданных командлетов AutoRest.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-489">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="f7f3b-490">Обновлены примеры для Connect AzAccount.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-490">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f7f3b-491">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f7f3b-491">Az.Automation</span></span>
* <span data-ttu-id="f7f3b-492">Исправлена проблема с получением некоторых ежемесячных расписаний в нескольких командлетах службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-492">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="f7f3b-493">Исправлен командлет Get-AzAutomationDscNode, возвращающий только первые 20 узлов.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-493">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="f7f3b-494">Теперь он возвращает все узлы.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-494">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f7f3b-495">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f7f3b-495">Az.Cdn</span></span>
* <span data-ttu-id="f7f3b-496">Добавлены новые командлеты PowerShell для включения и отключения HTTPS для личного домена и отключены устаревшие командлеты.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-496">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f7f3b-497">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f7f3b-497">Az.Compute</span></span>
* <span data-ttu-id="f7f3b-498">Добавлена поддержка подстановочных знаков в командлетах Get.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-498">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f7f3b-499">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f7f3b-499">Az.DataFactory</span></span>
* <span data-ttu-id="f7f3b-500">Обновлен пакет SDK для ADF .NET до версии 3.0.1.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-500">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f7f3b-501">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f7f3b-501">Az.LogicApp</span></span>
* <span data-ttu-id="f7f3b-502">Исправлена проблема с получением только первой страницы результатов при выполнении команды ListWorkflows.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-502">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f7f3b-503">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f7f3b-503">Az.Network</span></span>
* <span data-ttu-id="f7f3b-504">Добавлена поддержка подстановочных знаков в командлетах Network.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-504">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f7f3b-505">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f7f3b-505">Az.RecoveryServices</span></span>
* <span data-ttu-id="f7f3b-506">Добавлена поддержка SQL Server на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-506">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="f7f3b-507">Обновление пакета SDK</span><span class="sxs-lookup"><span data-stu-id="f7f3b-507">SDK Update</span></span>
* <span data-ttu-id="f7f3b-508">Удалена проверка VMappContainer в Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-508">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="f7f3b-509">Добавлены параметры Name и ServerName для Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-509">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="f7f3b-510">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f7f3b-510">Az.Resources</span></span>
* <span data-ttu-id="f7f3b-511">Добавлен параметр `-TemplateObject` в командлеты для развертывания.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-511">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="f7f3b-512">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2933.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-512">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="f7f3b-513">Устранена проблема с передачей в конвейер результата `Get-AzResource` для `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-513">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="f7f3b-514">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8240.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-514">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="f7f3b-515">Устранена проблема с изменением типа данных JSON при выполнении `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-515">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="f7f3b-516">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7930.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-516">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="f7f3b-517">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f7f3b-517">Az.Sql</span></span>
* <span data-ttu-id="f7f3b-518">Обновление AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-518">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="f7f3b-519">Исправлено поведение для пограничного случая при создании параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-519">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f7f3b-520">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f7f3b-520">Az.Storage</span></span>
* <span data-ttu-id="f7f3b-521">Включена поддержка Kind BlockBlobStorage при создании учетной записи хранения для New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-521">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="f7f3b-522">1.4.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-522">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="f7f3b-523">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f7f3b-523">Az.AnalysisServices</span></span>
* <span data-ttu-id="f7f3b-524">Командлет AddAzureASAccount устарел.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-524">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f7f3b-525">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f7f3b-525">Az.Automation</span></span>
* <span data-ttu-id="f7f3b-526">Обновлена справка для командлета Import-AzAutomationDscNodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-526">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="f7f3b-527">Добавлена проверка имени конфигурации для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-527">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="f7f3b-528">Улучшена обработка ошибок для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-528">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f7f3b-529">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f7f3b-529">Az.CognitiveServices</span></span>
* <span data-ttu-id="f7f3b-530">Добавлен параметр CustomSubdomainName — новый необязательный параметр для командлета New-AzCognitiveServicesAccount, который указывает поддомен для ресурса.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-530">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f7f3b-531">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f7f3b-531">Az.Compute</span></span>
* <span data-ttu-id="f7f3b-532">Устранена проблема с идентификаторами наборов параметров.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-532">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="f7f3b-533">Обновлен командлет Get-AzVMExtension для отображения списка всех установленных расширений, если не указан параметр Name.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-533">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="f7f3b-534">Для командлета Update-AzImage добавлены параметры Tag и ResourceId.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-534">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="f7f3b-535">Командлет Get-AzVmssVM, который выполняется без указания идентификатора экземпляра и с параметром InstanceView, может выводить виртуальные машины из VMSS с представлением экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-535">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f7f3b-536">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f7f3b-536">Az.DataLakeStore</span></span>
* <span data-ttu-id="f7f3b-537">Добавлены командлеты для перечисления и восстановления удаленного элемента ADL.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-537">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f7f3b-538">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f7f3b-538">Az.EventHub</span></span>
* <span data-ttu-id="f7f3b-539">Добавлено новое логическое свойство SkipEmptyArchives для пропуска пустых архивов в классе CaptureDescription Eventhub.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-539">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="f7f3b-540">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f7f3b-540">Az.KeyVault</span></span>
* <span data-ttu-id="f7f3b-541">Исправлена расстановка тегов для командлета Set-AzKeyVaultSecret.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-541">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f7f3b-542">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f7f3b-542">Az.LogicApp</span></span>
* <span data-ttu-id="f7f3b-543">Добавлен SKU "Базовый" для учетных записей интеграции.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-543">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="f7f3b-544">Добавлены типы сопоставлений Liquid, а также XSLT 2.0 и XSLT 3.0.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-544">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="f7f3b-545">Новые командлеты для сборок учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="f7f3b-545">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="f7f3b-546">Get-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="f7f3b-546">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="f7f3b-547">New-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="f7f3b-547">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="f7f3b-548">Remove-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="f7f3b-548">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="f7f3b-549">Set-AzIntegrationAccountAssembly.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-549">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="f7f3b-550">Новые командлеты для конфигурации пакета учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="f7f3b-550">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="f7f3b-551">Get-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="f7f3b-551">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="f7f3b-552">New-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="f7f3b-552">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="f7f3b-553">Remove-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="f7f3b-553">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="f7f3b-554">Set-AzIntegrationAccountBatchConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-554">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="f7f3b-555">Обновлен пакет SDK Logic Apps до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-555">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f7f3b-556">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f7f3b-556">Az.Monitor</span></span>
* <span data-ttu-id="f7f3b-557">Обновлена справка для командлета Get-AzMetric.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-557">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f7f3b-558">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f7f3b-558">Az.Network</span></span>
* <span data-ttu-id="f7f3b-559">Обновлен пример справки для командлета Add-AzApplicationGatewayCustomError.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-559">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f7f3b-560">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f7f3b-560">Az.OperationalInsights</span></span>
* <span data-ttu-id="f7f3b-561">Дополнительная поддержка создания и получения источников данных ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-561">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="f7f3b-562">Добавлен новый тип ApplicationInsights для получения определенных или всех источников данных ApplicationInsights для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-562">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="f7f3b-563">Добавлен командлет New-AzOperationalInsightsApplicationInsightsDataSource для создания источника данных с использованием параметров указанного ресурса Application-Insightss: subscription Id, resourceGroupName и name.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-563">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="f7f3b-564">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f7f3b-564">Az.Resources</span></span>
* <span data-ttu-id="f7f3b-565">исправлена проблема https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-565">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="f7f3b-566">исправлена проблема https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-566">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="f7f3b-567">исправлена проблема https://github.com/Azure/azure-powershell/issues/6219.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-567">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="f7f3b-568">Исправлена ошибка, препятствующая повторному созданию KeyCredentials.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-568">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="f7f3b-569">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f7f3b-569">Az.Sql</span></span>
* <span data-ttu-id="f7f3b-570">Добавлена поддержка уровня гипермасштабирования в базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-570">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="f7f3b-571">Исправлена ошибка, из-за которой восстановление могло завершиться со сбоем при указании ненужных свойств в запросе на восстановление.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-571">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f7f3b-572">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f7f3b-572">Az.Websites</span></span>
* <span data-ttu-id="f7f3b-573">Исправлен пример для командлета Get-AzWebAppSlotMetrics.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-573">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="f7f3b-574">1.3.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-574">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f7f3b-575">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f7f3b-575">Az.Accounts</span></span>
* <span data-ttu-id="f7f3b-576">Обновление до последней версии ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="f7f3b-576">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f7f3b-577">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f7f3b-577">Az.AnalysisServices</span></span>
<span data-ttu-id="f7f3b-578">Общедоступная версия модуля Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-578">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f7f3b-579">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f7f3b-579">Az.Compute</span></span>
* <span data-ttu-id="f7f3b-580">Расширение AEM: добавлена поддержка дисков UltraSSD, P60, P70 и P80.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-580">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="f7f3b-581">Обновлено описание справки для командлета Set-AzVMBootDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-581">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="f7f3b-582">Обновлено описание справки и пример для командлета Update-AzImage.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-582">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f7f3b-583">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f7f3b-583">Az.RecoveryServices</span></span>
<span data-ttu-id="f7f3b-584">Общедоступная версия модуля Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-584">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f7f3b-585">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f7f3b-585">Az.Resources</span></span>
* <span data-ttu-id="f7f3b-586">Исправлена расстановка тегов для групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-586">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="f7f3b-587">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-587">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="f7f3b-588">Исправлена проблема с игнорированием командлетом `Get-AzureRmRoleAssignment` параметра -ErrorAction.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-588">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="f7f3b-589">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-589">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="f7f3b-590">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f7f3b-590">Az.Sql</span></span>
* <span data-ttu-id="f7f3b-591">Добавлен командлет Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-591">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="f7f3b-592">Исправлена проблема с появлением исключения NullRef при выполнении командлетов SQL, если не выполнен вход в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-592">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="f7f3b-593">Исправлено исключение NullRef в командлете Get-AzSqlCapability.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-593">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="f7f3b-594">1.2.1 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-594">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f7f3b-595">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f7f3b-595">Az.Accounts</span></span>
* <span data-ttu-id="f7f3b-596">Выпуск с правильной версией службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-596">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f7f3b-597">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f7f3b-597">Az.AnalysisServices</span></span>
* <span data-ttu-id="f7f3b-598">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-598">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f7f3b-599">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f7f3b-599">Az.RecoveryServices</span></span>
* <span data-ttu-id="f7f3b-600">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-600">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="f7f3b-601">1.2.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-601">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f7f3b-602">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f7f3b-602">Az.Accounts</span></span>
* <span data-ttu-id="f7f3b-603">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-603">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f7f3b-604">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-604">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f7f3b-605">Добавлено предупреждающее сообщение в PS Core для модуля Uninstall-AzureRm.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-605">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="f7f3b-606">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f7f3b-606">Az.Aks</span></span>
* <span data-ttu-id="f7f3b-607">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-607">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f7f3b-608">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f7f3b-608">Az.Automation</span></span>
* <span data-ttu-id="f7f3b-609">Добавлена поддержка для модулей runbook Python 2.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-609">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="f7f3b-610">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-610">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f7f3b-611">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f7f3b-611">Az.Cdn</span></span>
* <span data-ttu-id="f7f3b-612">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-612">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f7f3b-613">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f7f3b-613">Az.Compute</span></span>
* <span data-ttu-id="f7f3b-614">Добавлен командлет Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-614">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="f7f3b-615">Добавлен параметр TempDisk к командлету Set-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-615">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="f7f3b-616">Исправлено предупреждающее сообщение командлета New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-616">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="f7f3b-617">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f7f3b-617">Az.ContainerRegistry</span></span>
* <span data-ttu-id="f7f3b-618">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-618">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f7f3b-619">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f7f3b-619">Az.DataFactory</span></span>
* <span data-ttu-id="f7f3b-620">Пакет SDK ADF .Net обновлен до версии 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-620">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f7f3b-621">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f7f3b-621">Az.DataLakeStore</span></span>
* <span data-ttu-id="f7f3b-622">Исправлена проблема с конечной точкой ADLS при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-622">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="f7f3b-623">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7462.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-623">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="f7f3b-624">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-624">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f7f3b-625">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f7f3b-625">Az.IotHub</span></span>
* <span data-ttu-id="f7f3b-626">Добавлен формат кодирования для командлета Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-626">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f7f3b-627">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f7f3b-627">Az.KeyVault</span></span>
* <span data-ttu-id="f7f3b-628">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-628">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f7f3b-629">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f7f3b-629">Az.Network</span></span>
* <span data-ttu-id="f7f3b-630">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-630">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="f7f3b-631">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f7f3b-631">Az.Resources</span></span>
* <span data-ttu-id="f7f3b-632">Исправлены неправильные примеры в справочной документации по командлетам New-AzADAppCredential и New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-632">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="f7f3b-633">Исправлена проблема, при которой путь для параметра -TemplateFile не удавалось разрешить до выполнения командлетов развертывания групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-633">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="f7f3b-634">Az.Resources: исправлена документация для значения по умолчанию -Mode командлета New-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-634">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="f7f3b-635">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/7522.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-635">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="f7f3b-636">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/5747.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-636">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="f7f3b-637">Исправлена проблема с форматированием объекта PSResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-637">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="f7f3b-638">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2123.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-638">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f7f3b-639">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f7f3b-639">Az.ServiceFabric</span></span>
* <span data-ttu-id="f7f3b-640">Исправлена проблема с появлением исключения в процессе отката при добавлении сертификата к модели VMSS: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-640">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="f7f3b-641">Исправлены некоторые сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-641">Fix some error messages.</span></span>
* <span data-ttu-id="f7f3b-642">Исправлена проблема с созданием кластера с шаблоном ARM по умолчанию для командлета New-AzServiceFabriCluster, который не работал с операцией миграции в Az.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-642">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="f7f3b-643">Исправлена проблема с добавлением сертификата кластера или приложения: теперь они добавляются только в Масштабируемые наборы виртуальных машин, которые сопоставлены с кластером, путем проверки идентификатора кластера в расширении.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-643">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="f7f3b-644">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="f7f3b-644">Az.SignalR</span></span>
* <span data-ttu-id="f7f3b-645">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-645">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="f7f3b-646">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f7f3b-646">Az.Sql</span></span>
* <span data-ttu-id="f7f3b-647">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-647">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f7f3b-648">Обновлено описание параметра LicenseType с добавлением возможных значений.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-648">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="f7f3b-649">Исправлена проблема с неправильным обновлением удостоверения управляемого экземпляра, если оно было единственным обновляемым свойством.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-649">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="f7f3b-650">Поддержка пользовательских параметров сортировки в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-650">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f7f3b-651">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f7f3b-651">Az.Storage</span></span>
* <span data-ttu-id="f7f3b-652">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-652">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f7f3b-653">Добавлен вывод подробных сообщений об ошибке при получении или установке классических свойств ведения журнала или метрик в учетной записи хранилища класса Premium, так как учетная запись хранилища класса Premium не поддерживает классические функции ведения журнала и метрик.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-653">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="f7f3b-654">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="f7f3b-654">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="f7f3b-655">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="f7f3b-655">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="f7f3b-656">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="f7f3b-656">Az.TrafficManager</span></span>
* <span data-ttu-id="f7f3b-657">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-657">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f7f3b-658">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f7f3b-658">Az.Websites</span></span>
* <span data-ttu-id="f7f3b-659">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-659">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f7f3b-660">Исправлена работа командлета New-AzWebAppSSLBinding: сертификат отправляется в правильную группу ресурсов и правильное расположение, если приложение размещено в ASE.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-660">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="f7f3b-661">Исправлена работа командлета New-AzWebAppSSLBinding: теги не перезаписываются при привязке SSL-сертификата к приложению.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-661">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="f7f3b-662">1.1.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-662">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f7f3b-663">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f7f3b-663">Az.Accounts</span></span>
* <span data-ttu-id="f7f3b-664">Добавление области "Local" в Enable-AzureRmAlias.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-664">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f7f3b-665">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f7f3b-665">Az.Compute</span></span>
* <span data-ttu-id="f7f3b-666">Теперь имя не является обязательным в идентификаторе набора параметров для Restart/Start/Stop/Remove/Set-AzVM и Save-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-666">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="f7f3b-667">Обновлено описание идентификатора в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-667">Updated the description of ID in help files</span></span>
* <span data-ttu-id="f7f3b-668">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-668">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f7f3b-669">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f7f3b-669">Az.DataLakeStore</span></span>
* <span data-ttu-id="f7f3b-670">Обновление версии пакета SDK для плоскости данных до 1.1.14 для устранения найденных проблем.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-670">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="f7f3b-671">Исправлена обработка отрицательного времени доступа и времени изменения для getfilestatus и liststatus, исправлен токен отмены для асинхронных методов.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-671">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f7f3b-672">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f7f3b-672">Az.EventGrid</span></span>
* <span data-ttu-id="f7f3b-673">Обновление для использования API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-673">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="f7f3b-674">Обновлены указанные ниже командлеты для поддержки нового сценария в API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-674">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="f7f3b-675">New-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="f7f3b-675">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="f7f3b-676">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="f7f3b-676">Event Time-To-Live,</span></span>
        - <span data-ttu-id="f7f3b-677">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="f7f3b-677">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="f7f3b-678">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-678">Dead letter endpoint.</span></span>
    - <span data-ttu-id="f7f3b-679">Update-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="f7f3b-679">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="f7f3b-680">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="f7f3b-680">Event Time-To-Live,</span></span>
        - <span data-ttu-id="f7f3b-681">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="f7f3b-681">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="f7f3b-682">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-682">Dead letter endpoint.</span></span>
* <span data-ttu-id="f7f3b-683">Для параметра EndpointType добавлены новые значения перечисления (storageQueue и hybridConnection) в командлеты New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-683">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="f7f3b-684">Если ожидается, что создание или обновление подписки на событие повлечет за собой действия со стороны пользователя, выполняемые вручную, отображается предупреждение при создании или обновлении подписки события.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-684">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f7f3b-685">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f7f3b-685">Az.IotHub</span></span>
* <span data-ttu-id="f7f3b-686">Пакет SDK Центра Интернета вещей обновлен до последней версии.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-686">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f7f3b-687">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f7f3b-687">Az.LogicApp</span></span>
* <span data-ttu-id="f7f3b-688">Get-AzLogicApp позволяет перечислить все параметры без указанного имени.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-688">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="f7f3b-689">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f7f3b-689">Az.Resources</span></span>
* <span data-ttu-id="f7f3b-690">Исправлена проблема с набором параметров при предоставлении параметров "-ODataQuery" и "-ResourceId" для "Get-AzResource".</span><span class="sxs-lookup"><span data-stu-id="f7f3b-690">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="f7f3b-691">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7875.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-691">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="f7f3b-692">Исправлена обработка параметра -Custom в New/Set-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-692">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="f7f3b-693">Исправлена опечатка в документации по New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-693">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="f7f3b-694">Параметр "-MailNickname" стал обязательным для "New-AzADUser".</span><span class="sxs-lookup"><span data-stu-id="f7f3b-694">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="f7f3b-695">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8220.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-695">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="f7f3b-696">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="f7f3b-696">Az.SignalR</span></span>
* <span data-ttu-id="f7f3b-697">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-697">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="f7f3b-698">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f7f3b-698">Az.Sql</span></span>
* <span data-ttu-id="f7f3b-699">Зависимость клиента управления хранением преобразована для общей реализации в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-699">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f7f3b-700">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f7f3b-700">Az.Storage</span></span>
* <span data-ttu-id="f7f3b-701">Установка параметра StorageAccountName для контекста хранилища в качестве реального имени учетной записи хранения, если она была создана с использованием токена Sas, OAuth или анонимного доступа.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-701">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="f7f3b-702">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f7f3b-702">New-AzStorageContext</span></span>
* <span data-ttu-id="f7f3b-703">Создание токена Sas большого двоичного объекта моментального снимка с параметром "-FullUri". Возвращаемый URI исправлен на URI моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-703">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="f7f3b-704">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="f7f3b-704">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f7f3b-705">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f7f3b-705">Az.Websites</span></span>
* <span data-ttu-id="f7f3b-706">Исправлена ошибка синтаксического анализа даты в "Get-AzDeletedWebApp".</span><span class="sxs-lookup"><span data-stu-id="f7f3b-706">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="f7f3b-707">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-707">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="f7f3b-708">1.0.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-708">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="f7f3b-709">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="f7f3b-709">General</span></span>

- <span data-ttu-id="f7f3b-710">Общедоступная версия модуля Az.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-710">General Availability of Az Module</span></span>
- <span data-ttu-id="f7f3b-711">Справка в Интернете для каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-711">Online help for each module</span></span>
- <span data-ttu-id="f7f3b-712">Дополнительные сведения и стратегию развития см. в статье [Announcing New Module 'Az'](https://aka.ms/azps-announce) (Объявление о новом модуле Az)</span><span class="sxs-lookup"><span data-stu-id="f7f3b-712">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="f7f3b-713">Сведения о миграции с AzureRM см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="f7f3b-713">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="f7f3b-714">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f7f3b-714">Az.Accounts</span></span>
- <span data-ttu-id="f7f3b-715">Изменено с Az.Profile.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-715">Changed from Az.Profile</span></span>
- <span data-ttu-id="f7f3b-716">Исправлены форматы таблиц для типов профиля и контекста.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-716">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="f7f3b-717">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f7f3b-717">Az.ApiManagement</span></span>
- <span data-ttu-id="f7f3b-718">Исправления для #7002.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-718">Fixes for #7002</span></span>
- <span data-ttu-id="f7f3b-719">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="f7f3b-719">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="f7f3b-720">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f7f3b-720">Az.Batch</span></span>
- <span data-ttu-id="f7f3b-721">Добавлена возможность видеть, какая версия агента узла пакетной службы Azure работает в пуле на каждой виртуальной машине, с помощью нового свойства `NodeAgentInformation` в `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-721">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="f7f3b-722">Значение `Caching` по умолчанию для `PSDataDisk` теперь `ReadWrite` вместо `None`.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-722">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="f7f3b-723">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="f7f3b-723">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="f7f3b-724">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="f7f3b-724">Az.Billing</span></span>
- <span data-ttu-id="f7f3b-725">Объединены командлеты Billing, Consumption и UsageAggregates. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0).</span><span class="sxs-lookup"><span data-stu-id="f7f3b-725">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="f7f3b-726">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="f7f3b-726">Az.CognitivServices</span></span>
- <span data-ttu-id="f7f3b-727">Добавлены средства заполнения для SkuName и Typem, доступные в операции New-AzureRmCognitiveServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-727">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="f7f3b-728">Удален набор параметров GetSkusWithAccountParamSetName из Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-728">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="f7f3b-729">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f7f3b-729">Az.ContainerInstance</span></span>
- <span data-ttu-id="f7f3b-730">Добавлена поддержка ManagedIdentity.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-730">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="f7f3b-731">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="f7f3b-731">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="f7f3b-732">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="f7f3b-732">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="f7f3b-733">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f7f3b-733">Az.DataLakeStore</span></span>
- <span data-ttu-id="f7f3b-734">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="f7f3b-734">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="f7f3b-735">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f7f3b-735">Az.Monitor</span></span>
- <span data-ttu-id="f7f3b-736">"Az.Insights" переименован в "Az.Monitor" и внесены другие незначительные критические изменения. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="f7f3b-736">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="f7f3b-737">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f7f3b-737">Az.KeyVault</span></span>
- <span data-ttu-id="f7f3b-738">Из типов вывода удалено устаревшее свойство PurgeDisabled</span><span class="sxs-lookup"><span data-stu-id="f7f3b-738">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="f7f3b-739">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="f7f3b-739">Az.MachineLearning</span></span>
- <span data-ttu-id="f7f3b-740">Включены командлеты из модуля Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="f7f3b-740">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="f7f3b-741">Az.Media</span><span class="sxs-lookup"><span data-stu-id="f7f3b-741">Az.Media</span></span>
- <span data-ttu-id="f7f3b-742">Удаляет устаревший псевдоним Tags из New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="f7f3b-742">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="f7f3b-743">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f7f3b-743">Az.Network</span></span>
<span data-ttu-id="f7f3b-744">В шлюз приложений добавлена поддержка настройки RewriteRuleSets</span><span class="sxs-lookup"><span data-stu-id="f7f3b-744">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="f7f3b-745">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="f7f3b-745">New cmdlets added:</span></span>
        - <span data-ttu-id="f7f3b-746">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f7f3b-746">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f7f3b-747">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f7f3b-747">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f7f3b-748">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f7f3b-748">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f7f3b-749">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f7f3b-749">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f7f3b-750">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f7f3b-750">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f7f3b-751">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="f7f3b-751">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="f7f3b-752">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="f7f3b-752">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="f7f3b-753">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="f7f3b-753">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="f7f3b-754">В следующие командлеты добавлен необязательный параметр -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f7f3b-754">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="f7f3b-755">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f7f3b-755">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="f7f3b-756">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f7f3b-756">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="f7f3b-757">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f7f3b-757">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="f7f3b-758">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f7f3b-758">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="f7f3b-759">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f7f3b-759">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="f7f3b-760">New-AzureRmApplicationGatewayUrlPathMapConfig добавил с помощью идентификатора поддержку KeyVault для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-760">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="f7f3b-761">В следующие командлеты добавлен необязательный параметр -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f7f3b-761">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="f7f3b-762">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f7f3b-762">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="f7f3b-763">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f7f3b-763">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="f7f3b-764">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f7f3b-764">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="f7f3b-765">В командлет New-AzApplicationGateway добавлен необязательный параметр -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="f7f3b-765">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="f7f3b-766">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="f7f3b-766">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="f7f3b-767">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f7f3b-767">Az.OperationalInsights</span></span>
- <span data-ttu-id="f7f3b-768">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="f7f3b-768">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="f7f3b-769">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f7f3b-769">Az.Profile</span></span>
- <span data-ttu-id="f7f3b-770">Имя модуля изменено на Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-770">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="f7f3b-771">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f7f3b-771">Az.RecoveryServices</span></span>
- <span data-ttu-id="f7f3b-772">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="f7f3b-772">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="f7f3b-773">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f7f3b-773">Az.Resources</span></span>
- <span data-ttu-id="f7f3b-774">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="f7f3b-774">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="f7f3b-775">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f7f3b-775">Az.ServiceFabric</span></span>
- <span data-ttu-id="f7f3b-776">Поддержка спецификации сертификата по общему имени и отпечатку</span><span class="sxs-lookup"><span data-stu-id="f7f3b-776">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="f7f3b-777">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="f7f3b-777">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="f7f3b-778">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="f7f3b-778">Az.SIgnalR</span></span>
- <span data-ttu-id="f7f3b-779">Общедоступная версия командлетов PowerShell для SIgnalR</span><span class="sxs-lookup"><span data-stu-id="f7f3b-779">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="f7f3b-780">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f7f3b-780">Az.Sql</span></span>
- <span data-ttu-id="f7f3b-781">Добавлены новые типы обнаружения Data_Exfiltration и Unsafe_Action в командлеты обнаружения угроз</span><span class="sxs-lookup"><span data-stu-id="f7f3b-781">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="f7f3b-782">Примеры обновленной документации для командлетов аудита Sql</span><span class="sxs-lookup"><span data-stu-id="f7f3b-782">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="f7f3b-783">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="f7f3b-783">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="f7f3b-784">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f7f3b-784">Az.Storage</span></span>
- <span data-ttu-id="f7f3b-785">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="f7f3b-785">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="f7f3b-786">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f7f3b-786">Az.Websites</span></span>
- <span data-ttu-id="f7f3b-787">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="f7f3b-787">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="f7f3b-788">0.7.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-788">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="f7f3b-789">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="f7f3b-789">General</span></span>

* <span data-ttu-id="f7f3b-790">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="f7f3b-790">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="f7f3b-791">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f7f3b-791">Az.Compute</span></span>

* <span data-ttu-id="f7f3b-792">Добавлена поддержка UltraSSD и образов коллекции в простых наборах параметров для командлетов `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-792">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="f7f3b-793">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f7f3b-793">Az.DataLakeStore</span></span>

* <span data-ttu-id="f7f3b-794">Исправлено косую черту в конце домена учетной записи ADLS</span><span class="sxs-lookup"><span data-stu-id="f7f3b-794">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="f7f3b-795">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f7f3b-795">Az.FrontDoor</span></span>

* <span data-ttu-id="f7f3b-796">Исправлены некоторые неработающие ссылки</span><span class="sxs-lookup"><span data-stu-id="f7f3b-796">Fixed some broken links</span></span>
    - <span data-ttu-id="f7f3b-797">В статьях New-AzureRmFrontDoor и Set-AzureRmFrontDoor исправлена ссылка на статью командлета New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-797">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="f7f3b-798">В статье New-AzureRmFrontDoorManagedRuleObject исправлена ссылка на статью командлета New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-798">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="f7f3b-799">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f7f3b-799">Az.RecoveryServices</span></span>

* <span data-ttu-id="f7f3b-800">Добавлены проверки на стороне клиента для операций восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-800">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="f7f3b-801">StorageAccountName и storageAccountResourceGroupName являются необязательными для восстановления afs.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-801">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="f7f3b-802">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f7f3b-802">Az.Resources</span></span>

* <span data-ttu-id="f7f3b-803">Исправление для https://github.com/Azure/azure-powershell/issues/7679.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-803">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="f7f3b-804">Обновите Get-AzureRmRoleAssignment, чтобы использовать область подписки, если она указана при запросе классических администраторов.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-804">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="f7f3b-805">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f7f3b-805">Az.Sql</span></span>

* <span data-ttu-id="f7f3b-806">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="f7f3b-806">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="f7f3b-807">Устранена проблема с использованием Get-AzureRmSqlDatabaseVulnerabilityAssessment с .NET Core.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-807">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="f7f3b-808">Изменена документация справочных сообщений, связанных с командлетами аудита SQL.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-808">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="f7f3b-809">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f7f3b-809">Az.Storage</span></span>

* <span data-ttu-id="f7f3b-810">Добавлено -EnableHierarchicalNamespace к New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f7f3b-810">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="f7f3b-811">Устранена проблема, из-за которой командлет Copy File не может повторно использовать исходный контекст в пункте назначения, если не введен -DestContext</span><span class="sxs-lookup"><span data-stu-id="f7f3b-811">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="f7f3b-812">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="f7f3b-812">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="f7f3b-813">Поддержка статической конфигурации сайта</span><span class="sxs-lookup"><span data-stu-id="f7f3b-813">Support Static Website configuration</span></span>
    - <span data-ttu-id="f7f3b-814">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="f7f3b-814">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="f7f3b-815">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="f7f3b-815">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="f7f3b-816">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f7f3b-816">Az.Websites</span></span>

* <span data-ttu-id="f7f3b-817">Set-AzureRmWebApp и Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f7f3b-817">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="f7f3b-818">Добавлен новый параметр (-AzureStoragePath), который указывает путь службы хранилища Azure для подключения в приложениях-контейнерах Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-818">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="f7f3b-819">Используйте выходные данные нового командлета New-AzureRmWebAppAzureStoragePath в качестве параметра, чтобы задать пути к службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-819">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="f7f3b-820">0.6.1 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-820">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="f7f3b-821">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f7f3b-821">Az.ApiManagement</span></span>
* <span data-ttu-id="f7f3b-822">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-822">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="f7f3b-823">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f7f3b-823">Az.Automation</span></span>
* <span data-ttu-id="f7f3b-824">Командлеты службы автоматизации Azure на базе Swagger.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-824">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="f7f3b-825">Добавлены командлеты для Управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-825">Added Update Management cmdlets</span></span>
* <span data-ttu-id="f7f3b-826">Добавлены командлеты для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-826">Added Source Control cmdlets</span></span>
* <span data-ttu-id="f7f3b-827">Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-827">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="f7f3b-828">Исправлена команда DSC для регистрации узла.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-828">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="f7f3b-829">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f7f3b-829">Az.Compute</span></span>
* <span data-ttu-id="f7f3b-830">Исправлена проблема с удостоверением, назначаемым системой.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-830">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="f7f3b-831">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-831">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="f7f3b-832">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f7f3b-832">Az.ContainerInstance</span></span>
* <span data-ttu-id="f7f3b-833">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-833">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="f7f3b-834">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="f7f3b-834">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="f7f3b-835">Обновлено описание в примерах командлетов для Marketplace.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-835">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="f7f3b-836">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f7f3b-836">Az.Network</span></span>
* <span data-ttu-id="f7f3b-837">Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-837">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="f7f3b-838">Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-838">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="f7f3b-839">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-839">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="f7f3b-840">Исправлены проблемы с использованием памяти в карте виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-840">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="f7f3b-841">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="f7f3b-841">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="f7f3b-842">Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-842">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="f7f3b-843">Параметры часового пояса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-843">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="f7f3b-844">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="f7f3b-844">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="f7f3b-845">Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-845">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="f7f3b-846">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-846">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="f7f3b-847">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="f7f3b-847">Az.Relay</span></span>
* <span data-ttu-id="f7f3b-848">Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-848">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="f7f3b-849">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f7f3b-849">Az.Resources</span></span>
* <span data-ttu-id="f7f3b-850">Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-850">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="f7f3b-851">Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-851">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="f7f3b-852">Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-852">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="f7f3b-853">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f7f3b-853">Az.ServiceFabric</span></span>
* <span data-ttu-id="f7f3b-854">Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-854">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="f7f3b-855">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f7f3b-855">Az.Sql</span></span>
* <span data-ttu-id="f7f3b-856">Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-856">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="f7f3b-857">Get-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-857">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f7f3b-858">New-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-858">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f7f3b-859">Set-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-859">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f7f3b-860">Remove-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-860">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f7f3b-861">Get-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-861">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f7f3b-862">New-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-862">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f7f3b-863">Restore-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-863">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f7f3b-864">Remove-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-864">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="f7f3b-865">Добавлено расширенное управление политиками аудита для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-865">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="f7f3b-866">Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-866">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="f7f3b-867">Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-867">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="f7f3b-868">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-868">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="f7f3b-869">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-869">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="f7f3b-870">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-870">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="f7f3b-871">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-871">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="f7f3b-872">Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-872">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="f7f3b-873">0.5.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-873">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="f7f3b-874">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="f7f3b-874">General</span></span>
* <span data-ttu-id="f7f3b-875">Добавлены средства заполнения ресурсов для многих основных командлетов — они позволяют вам переключать существующие имена ресурсов при вызове командлетов в интерактивном режиме</span><span class="sxs-lookup"><span data-stu-id="f7f3b-875">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="f7f3b-876">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f7f3b-876">Az.Profile</span></span>
* <span data-ttu-id="f7f3b-877">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-877">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="f7f3b-878">В командлете Connect-AzAccount параметр TenantId переименован в Tenant и добавлен псевдоним для TenantId</span><span class="sxs-lookup"><span data-stu-id="f7f3b-878">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="f7f3b-879">Обновлено описание TenantId для командлета Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="f7f3b-879">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="f7f3b-880">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-880">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="f7f3b-881">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-881">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="f7f3b-882">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-882">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="f7f3b-883">Устранена проблема, при которой командлет Disconnect-AzAccount вызывал сбой при отсутствии подключения</span><span class="sxs-lookup"><span data-stu-id="f7f3b-883">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="f7f3b-884">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f7f3b-884">Az.CognitiveServices</span></span>
* <span data-ttu-id="f7f3b-885">Добавлена операция Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-885">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f7f3b-886">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f7f3b-886">Az.Compute</span></span>
* <span data-ttu-id="f7f3b-887">Добавлены командлеты Add-AzVmssVMDataDisk и Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="f7f3b-887">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="f7f3b-888">Get-AzVMImage отображает AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="f7f3b-888">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="f7f3b-889">Устранена проблема, при которой значения параметров SetAzVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-889">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f7f3b-890">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f7f3b-890">Az.DataLakeStore</span></span>
* <span data-ttu-id="f7f3b-891">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-891">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="f7f3b-892">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-892">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="f7f3b-893">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="f7f3b-893">Az.Insights</span></span>
* <span data-ttu-id="f7f3b-894">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="f7f3b-894">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="f7f3b-895">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="f7f3b-895">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="f7f3b-896">Исправлена проблема № 7513 [Insights], при которой для командлета Set-AzDiagnosticSetting требовалось явное указание категорий во время создания параметра</span><span class="sxs-lookup"><span data-stu-id="f7f3b-896">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="f7f3b-897">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-897">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f7f3b-898">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f7f3b-898">Az.Network</span></span>
* <span data-ttu-id="f7f3b-899">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="f7f3b-899">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="f7f3b-900">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="f7f3b-900">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="f7f3b-901">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="f7f3b-901">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="f7f3b-902">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f7f3b-902">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="f7f3b-903">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="f7f3b-903">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="f7f3b-904">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="f7f3b-904">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="f7f3b-905">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f7f3b-905">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f7f3b-906">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f7f3b-906">Az.PolicyInsights</span></span>
* <span data-ttu-id="f7f3b-907">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-907">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="f7f3b-908">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f7f3b-908">Az.Resources</span></span>
* <span data-ttu-id="f7f3b-909">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-909">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="f7f3b-910">Разрешено перечисление ресурсов с помощью параметра -ResourceId для командлета Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="f7f3b-910">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f7f3b-911">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f7f3b-911">Az.ServiceBus</span></span>
* <span data-ttu-id="f7f3b-912">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-912">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f7f3b-913">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f7f3b-913">Az.ServiceFabric</span></span>
* <span data-ttu-id="f7f3b-914">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-914">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="f7f3b-915">Исправлен командлет Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="f7f3b-915">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="f7f3b-916">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="f7f3b-916">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="f7f3b-917">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="f7f3b-917">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="f7f3b-918">Исправлен командлет Update-AzServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-918">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="f7f3b-919">0.4.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-919">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="f7f3b-920">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f7f3b-920">Az.Profile</span></span>
* <span data-ttu-id="f7f3b-921">Устранена проблема с Get-AzSubscription в CloudShell</span><span class="sxs-lookup"><span data-stu-id="f7f3b-921">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="f7f3b-922">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-922">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f7f3b-923">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f7f3b-923">Az.Compute</span></span>
* <span data-ttu-id="f7f3b-924">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzVm</span><span class="sxs-lookup"><span data-stu-id="f7f3b-924">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="f7f3b-925">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-925">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f7f3b-926">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f7f3b-926">Az.DataLakeStore</span></span>
* <span data-ttu-id="f7f3b-927">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="f7f3b-927">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="f7f3b-928">Get-AzDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-928">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="f7f3b-929">Add-AzDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-929">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="f7f3b-930">Set-AzDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-930">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="f7f3b-931">Remove-AzDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-931">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f7f3b-932">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f7f3b-932">Az.Network</span></span>
* <span data-ttu-id="f7f3b-933">Обновлен командлет Test-AzNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-933">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="f7f3b-934">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-934">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f7f3b-935">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f7f3b-935">Az.Resources</span></span>
* <span data-ttu-id="f7f3b-936">Устранена проблема, из-за которой командлет Get-AzRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), благодаря добавлению понятного исключения в сценарий.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-936">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="f7f3b-937">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-937">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="f7f3b-938">0.3.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-938">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="f7f3b-939">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="f7f3b-939">Azure.Storage</span></span>
* <span data-ttu-id="f7f3b-940">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-940">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="f7f3b-941">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f7f3b-941">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="f7f3b-942">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="f7f3b-942">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="f7f3b-943">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-943">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="f7f3b-944">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="f7f3b-944">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="f7f3b-945">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f7f3b-945">Az.CognitiveServices</span></span>
* <span data-ttu-id="f7f3b-946">Поддержка Get-AzCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-946">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f7f3b-947">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f7f3b-947">Az.Compute</span></span>
* <span data-ttu-id="f7f3b-948">Исправлена команда Get-AzVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов</span><span class="sxs-lookup"><span data-stu-id="f7f3b-948">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="f7f3b-949">Добавлен пример использования SimpleParameterSet в справку командлета New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-949">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="f7f3b-950">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-950">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="f7f3b-951">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f7f3b-951">Az.DataFactoryV2</span></span>
* <span data-ttu-id="f7f3b-952">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-952">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f7f3b-953">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f7f3b-953">Az.Network</span></span>
* <span data-ttu-id="f7f3b-954">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-954">Added NetworkProfile functionality.</span></span> <span data-ttu-id="f7f3b-955">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="f7f3b-955">new cmdlets added</span></span>
    - <span data-ttu-id="f7f3b-956">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f7f3b-956">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="f7f3b-957">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f7f3b-957">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="f7f3b-958">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f7f3b-958">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="f7f3b-959">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f7f3b-959">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="f7f3b-960">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="f7f3b-960">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="f7f3b-961">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="f7f3b-961">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="f7f3b-962">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-962">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="f7f3b-963">Добавлены командлеты: New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="f7f3b-963">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="f7f3b-964">Добавлены командлеты: Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="f7f3b-964">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f7f3b-965">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f7f3b-965">Az.RedisCache</span></span>
* <span data-ttu-id="f7f3b-966">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-966">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="f7f3b-967">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-967">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="f7f3b-968">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f7f3b-968">Az.Resources</span></span>
* <span data-ttu-id="f7f3b-969">Добавлен отсутствующий параметр -Mode в командлет Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f7f3b-969">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="f7f3b-970">Исправлена ошибка командлета Get-AzProviderOperation для операций, когда Origin содержит User</span><span class="sxs-lookup"><span data-stu-id="f7f3b-970">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="f7f3b-971">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f7f3b-971">Az.Sql</span></span>
* <span data-ttu-id="f7f3b-972">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-972">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f7f3b-973">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f7f3b-973">Az.Websites</span></span>
* <span data-ttu-id="f7f3b-974">Новый командлет Get-AzWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="f7f3b-974">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="f7f3b-975">Новые командлеты New-AzWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows</span><span class="sxs-lookup"><span data-stu-id="f7f3b-975">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="f7f3b-976">0.2.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="f7f3b-976">0.2.0 - September 2018</span></span>
 <span data-ttu-id="f7f3b-977">Первый выпуск</span><span class="sxs-lookup"><span data-stu-id="f7f3b-977">Initial Release</span></span>