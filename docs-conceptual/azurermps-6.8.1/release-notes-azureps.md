---
title: Журнал изменений Azure PowerShell | Документация Майкрософт
description: Это руководство содержит историю изменений Azure PowerShell, внесенных в новом выпуске.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 08/28/2018
ms.openlocfilehash: f4f3141998be14f0b5b223aed1af283534bf061d
ms.sourcegitcommit: bc88e64c494337821274d6a66c1edad656c119c5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/20/2018
ms.locfileid: "46300839"
---
# <a name="release-notes"></a><span data-ttu-id="ff120-103">Заметки о выпуске</span><span class="sxs-lookup"><span data-stu-id="ff120-103">Release notes</span></span>

<span data-ttu-id="ff120-104">Здесь приведен список изменений, внесенных в Azure PowerShell в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="ff120-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="681---august-2018"></a><span data-ttu-id="ff120-105">6.8.1 — август 2018 г.</span><span class="sxs-lookup"><span data-stu-id="ff120-105">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ff120-106">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="ff120-106">General</span></span>
* <span data-ttu-id="ff120-107">Исправлена проблема с отсутствием настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ff120-107">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="ff120-108">Обновлены общие сборки среды выполнения</span><span class="sxs-lookup"><span data-stu-id="ff120-108">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="ff120-109">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ff120-109">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="ff120-110">Исправлена проблема с отсутствием настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ff120-110">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="ff120-111">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6603.</span><span class="sxs-lookup"><span data-stu-id="ff120-111">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="ff120-112">Командлеты Import-AzureRmApiManagementApi и \*-AzureRmApiManagementCertificate теперь обрабатывают относительные пути.</span><span class="sxs-lookup"><span data-stu-id="ff120-112">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="ff120-113">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6879.</span><span class="sxs-lookup"><span data-stu-id="ff120-113">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="ff120-114">CertificateInformation — это задаваемое свойство, обеспечивающее правильную работу командлета Set-AzureRmApiManagement.</span><span class="sxs-lookup"><span data-stu-id="ff120-114">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="ff120-115">Проблема исправлена путем обновления пакета NuGet до версии 4.0.4-preview.</span><span class="sxs-lookup"><span data-stu-id="ff120-115">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="ff120-116">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6853.</span><span class="sxs-lookup"><span data-stu-id="ff120-116">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="ff120-117">Исправлен фильтр OData для поиска по имени продукта.</span><span class="sxs-lookup"><span data-stu-id="ff120-117">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="ff120-118">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6814.</span><span class="sxs-lookup"><span data-stu-id="ff120-118">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="ff120-119">Исправлен фильтр OData для поиска по имени API.</span><span class="sxs-lookup"><span data-stu-id="ff120-119">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="ff120-120">Добавлена поддержка средства ведения журнала Azure Monitor.</span><span class="sxs-lookup"><span data-stu-id="ff120-120">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="ff120-121">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ff120-121">AzureRM.Compute</span></span>
* <span data-ttu-id="ff120-122">Исправлена проблема с отсутствием в выходных данных ошибки целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="ff120-122">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="ff120-123">Исправлена проблема с типом учетной записи хранения для виртуальной машины с управляемым диском.</span><span class="sxs-lookup"><span data-stu-id="ff120-123">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="ff120-124">Исправлена проблема с отсутствием настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ff120-124">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="ff120-125">Исправлены командлеты расширения AEM для других сред, например Azure для Китая.</span><span class="sxs-lookup"><span data-stu-id="ff120-125">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ff120-126">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ff120-126">AzureRM.Network</span></span>
* <span data-ttu-id="ff120-127">Стандартное представление выходных данных командлетов изменено на представление таблиц.</span><span class="sxs-lookup"><span data-stu-id="ff120-127">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="ff120-128">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="ff120-128">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="ff120-129">Исправлена проблема с Update-AzureRmPowerBIEmbeddedCapacity при попытке масштабировать приостановленную емкость.</span><span class="sxs-lookup"><span data-stu-id="ff120-129">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="ff120-130">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ff120-130">AzureRM.Resources</span></span>
* <span data-ttu-id="ff120-131">Исправлена проблема с созданием управляемых приложений из Marketplace.</span><span class="sxs-lookup"><span data-stu-id="ff120-131">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ff120-132">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ff120-132">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ff120-133">Исправленные проблемы</span><span class="sxs-lookup"><span data-stu-id="ff120-133">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="ff120-134">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ff120-134">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="ff120-135">Добавлена поддержка метода маршрутизации MultiValue.</span><span class="sxs-lookup"><span data-stu-id="ff120-135">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="ff120-136">Добавлен новый параметр MaxReturn для маршрутизации MultiValue.</span><span class="sxs-lookup"><span data-stu-id="ff120-136">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="ff120-137">Добавлена поддержка метода маршрутизации Subnet.</span><span class="sxs-lookup"><span data-stu-id="ff120-137">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="ff120-138">Добавлена поддержка диапазонов IP-адресов (подсетей) в конечных точках.</span><span class="sxs-lookup"><span data-stu-id="ff120-138">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="ff120-139">Добавлена поддержка пользовательских заголовков в профилях.</span><span class="sxs-lookup"><span data-stu-id="ff120-139">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="ff120-140">Добавлена поддержка диапазонов кода ожидаемого состояния в профилях.</span><span class="sxs-lookup"><span data-stu-id="ff120-140">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="ff120-141">Добавлена поддержка пользовательских заголовков в конечных точках.</span><span class="sxs-lookup"><span data-stu-id="ff120-141">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="ff120-142">6.8.0 — август 2018 г.</span><span class="sxs-lookup"><span data-stu-id="ff120-142">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ff120-143">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="ff120-143">General</span></span>
* <span data-ttu-id="ff120-144">Исправлена проблема с отсутствием настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ff120-144">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="ff120-145">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ff120-145">AzureRM.Profile</span></span>
* <span data-ttu-id="ff120-146">Добавлено свойство срока действия для маркеров, возвращенных при выполнении Connect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="ff120-146">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ff120-147">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ff120-147">AzureRM.Compute</span></span>
* <span data-ttu-id="ff120-148">Исправлена проблема с отсутствием в выходных данных ошибки целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="ff120-148">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="ff120-149">Исправлена проблема с типом учетной записи хранения для виртуальной машины с управляемым диском.</span><span class="sxs-lookup"><span data-stu-id="ff120-149">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="ff120-150">Исправлены командлеты расширения AEM для других сред, например Azure для Китая.</span><span class="sxs-lookup"><span data-stu-id="ff120-150">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="ff120-151">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="ff120-151">AzureRM.IotHub</span></span>
* <span data-ttu-id="ff120-152">Исправлены примеры для New-AzureRmIotHubExportDevices и New-AzureRmIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="ff120-152">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ff120-153">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ff120-153">AzureRM.Network</span></span>
* <span data-ttu-id="ff120-154">Изменено представление моделей по умолчанию на представление таблиц.</span><span class="sxs-lookup"><span data-stu-id="ff120-154">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="ff120-155">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="ff120-155">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="ff120-156">Исправлена проблема с Update-AzureRmPowerBIEmbeddedCapacity при попытке масштабировать приостановленную емкость.</span><span class="sxs-lookup"><span data-stu-id="ff120-156">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ff120-157">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ff120-157">AzureRM.Resources</span></span>
* <span data-ttu-id="ff120-158">Исправлена проблема с созданием управляемого приложения из marketplace.</span><span class="sxs-lookup"><span data-stu-id="ff120-158">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ff120-159">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ff120-159">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ff120-160">Исправления проблем</span><span class="sxs-lookup"><span data-stu-id="ff120-160">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="ff120-161">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ff120-161">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="ff120-162">Добавлена поддержка метода маршрутизации MultiValue.</span><span class="sxs-lookup"><span data-stu-id="ff120-162">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="ff120-163">Добавлен новый параметр MaxReturn для маршрутизации MultiValue.</span><span class="sxs-lookup"><span data-stu-id="ff120-163">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="ff120-164">Добавлена поддержка метода маршрутизации Subnet.</span><span class="sxs-lookup"><span data-stu-id="ff120-164">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="ff120-165">Добавлена поддержка диапазонов IP-адресов (подсетей) в конечных точках.</span><span class="sxs-lookup"><span data-stu-id="ff120-165">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="ff120-166">Добавлена поддержка пользовательских заголовков в профилях.</span><span class="sxs-lookup"><span data-stu-id="ff120-166">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="ff120-167">Добавлена поддержка диапазонов кода состояния ожидания в профилях.</span><span class="sxs-lookup"><span data-stu-id="ff120-167">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="ff120-168">Добавлена поддержка пользовательских заголовков в конечных точках.</span><span class="sxs-lookup"><span data-stu-id="ff120-168">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ff120-169">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ff120-169">AzureRM.Websites</span></span>
* <span data-ttu-id="ff120-170">Исправлена проблема с отсутствием правильной настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ff120-170">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="ff120-171">6.7.0 — август 2018 г.</span><span class="sxs-lookup"><span data-stu-id="ff120-171">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ff120-172">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ff120-172">AzureRM.Profile</span></span>
* <span data-ttu-id="ff120-173">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-173">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="ff120-174">Добавлен идентификатор пользователя для имени контекста по умолчанию, чтобы избежать конфликтов контекста.</span><span class="sxs-lookup"><span data-stu-id="ff120-174">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="ff120-175">Устранены проблемы с командлетом Clear-AzureRmContext, которые приводили к проблемам с выбором контекста #6398.</span><span class="sxs-lookup"><span data-stu-id="ff120-175">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="ff120-176">Разрешено передавать домен клиента в параметр -TenantId для командлета Connect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="ff120-176">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="ff120-177">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="ff120-177">Azure.Storage</span></span>
* <span data-ttu-id="ff120-178">Удалено ограничение в 5 ТБ для квоты на общую папку Azure.</span><span class="sxs-lookup"><span data-stu-id="ff120-178">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="ff120-179">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="ff120-179">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="ff120-180">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ff120-180">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="ff120-181">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-181">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="ff120-182">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ff120-182">Azure.AnalysisServices</span></span>
* <span data-ttu-id="ff120-183">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-183">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="ff120-184">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ff120-184">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="ff120-185">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-185">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="ff120-186">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="ff120-186">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="ff120-187">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-187">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="ff120-188">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="ff120-188">AzureRM.Automation</span></span>
* <span data-ttu-id="ff120-189">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-189">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="ff120-190">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="ff120-190">AzureRM.Backup</span></span>
* <span data-ttu-id="ff120-191">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-191">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="ff120-192">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="ff120-192">AzureRM.Batch</span></span>
* <span data-ttu-id="ff120-193">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-193">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="ff120-194">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="ff120-194">AzureRM.Billing</span></span>
* <span data-ttu-id="ff120-195">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-195">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="ff120-196">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="ff120-196">AzureRM.Cdn</span></span>
* <span data-ttu-id="ff120-197">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-197">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="ff120-198">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ff120-198">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="ff120-199">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-199">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ff120-200">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ff120-200">AzureRM.Compute</span></span>
* <span data-ttu-id="ff120-201">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-201">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="ff120-202">В командлет New-AzureRmVmssConfig добавлен параметр EvictionPolicy.</span><span class="sxs-lookup"><span data-stu-id="ff120-202">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="ff120-203">Если расположение не указано, используйте в DiskFileParameterSet для New AzureRmVm расположение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ff120-203">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="ff120-204">Исправлено описание параметров в Save-AzureRmVMImage.</span><span class="sxs-lookup"><span data-stu-id="ff120-204">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="ff120-205">Исправлен командлет Get-AzureRmVMDiskEncryptionStatus для определенных сценариев, связанных с однократным выполнением.</span><span class="sxs-lookup"><span data-stu-id="ff120-205">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="ff120-206">AzureRM.Consumption:</span><span class="sxs-lookup"><span data-stu-id="ff120-206">AzureRM.Consumption</span></span>
* <span data-ttu-id="ff120-207">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-207">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="ff120-208">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ff120-208">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="ff120-209">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-209">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="ff120-210">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ff120-210">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="ff120-211">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-211">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="ff120-212">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="ff120-212">AzureRM.DataFactories</span></span>
* <span data-ttu-id="ff120-213">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-213">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="ff120-214">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ff120-214">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="ff120-215">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-215">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="ff120-216">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="ff120-216">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="ff120-217">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-217">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="ff120-218">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ff120-218">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="ff120-219">Исправлена отладка, когда DebugPreference настраивается из командной строки PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ff120-219">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="ff120-220">Обновлен пример для Set-AzureRmDataLakeStoreItemAcl.</span><span class="sxs-lookup"><span data-stu-id="ff120-220">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="ff120-221">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-221">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="ff120-222">Обновлен пример для Set-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="ff120-222">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="ff120-223">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="ff120-223">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="ff120-224">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-224">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="ff120-225">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="ff120-225">AzureRM.Dns</span></span>
* <span data-ttu-id="ff120-226">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-226">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="ff120-227">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ff120-227">AzureRM.EventGrid</span></span>
* <span data-ttu-id="ff120-228">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-228">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="ff120-229">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="ff120-229">AzureRM.EventHub</span></span>
* <span data-ttu-id="ff120-230">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-230">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="ff120-231">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ff120-231">AzureRM.HDInsight</span></span>
* <span data-ttu-id="ff120-232">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-232">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="ff120-233">AzureRM.Insights;</span><span class="sxs-lookup"><span data-stu-id="ff120-233">AzureRM.Insights</span></span>
* <span data-ttu-id="ff120-234">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-234">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="ff120-235">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="ff120-235">AzureRM.IotHub</span></span>
* <span data-ttu-id="ff120-236">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-236">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="ff120-237">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ff120-237">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ff120-238">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-238">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="ff120-239">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ff120-239">AzureRM.LogicApp</span></span>
* <span data-ttu-id="ff120-240">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-240">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="ff120-241">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="ff120-241">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="ff120-242">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-242">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="ff120-243">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="ff120-243">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="ff120-244">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-244">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="ff120-245">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="ff120-245">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="ff120-246">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-246">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="ff120-247">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="ff120-247">AzureRM.Media</span></span>
* <span data-ttu-id="ff120-248">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-248">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ff120-249">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ff120-249">AzureRM.Network</span></span>
* <span data-ttu-id="ff120-250">Добавлен пример для Set-AzureRmLocalNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="ff120-250">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="ff120-251">Добавлены примеры и описания для Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey и New-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="ff120-251">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="ff120-252">Добавлены примеры для Remove-AzureRmVirtualNetworkGatewayIpConfig и Reset-AzureRmVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="ff120-252">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="ff120-253">Добавлен пример для Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.</span><span class="sxs-lookup"><span data-stu-id="ff120-253">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="ff120-254">Добавлен пример для Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.</span><span class="sxs-lookup"><span data-stu-id="ff120-254">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="ff120-255">Добавлен пример для Set-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="ff120-255">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="ff120-256">Повторно созданы командлеты для ApplicationSecurityGroup, RouteTable и Usage с помощью генератора кода последней версии.</span><span class="sxs-lookup"><span data-stu-id="ff120-256">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="ff120-257">Уточнено сообщение об ошибке для Get-AzureRmVirtualNetworkSubnetConfig при попытке получить подсеть, которая не существует.</span><span class="sxs-lookup"><span data-stu-id="ff120-257">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="ff120-258">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="ff120-258">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="ff120-259">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-259">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="ff120-260">AzureRM.OperationalInsights;</span><span class="sxs-lookup"><span data-stu-id="ff120-260">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="ff120-261">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-261">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="ff120-262">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ff120-262">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="ff120-263">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-263">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="ff120-264">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="ff120-264">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="ff120-265">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-265">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="ff120-266">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ff120-266">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="ff120-267">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-267">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="ff120-268">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="ff120-268">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="ff120-269">Добавлен фильтр политик для командлета Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="ff120-269">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="ff120-270">Команда возвращает список элементов резервного копирования, защищенных политикой с заданным идентификатором.</span><span class="sxs-lookup"><span data-stu-id="ff120-270">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="ff120-271">Обновление Microsoft.Azure.Management.RecoveryServices.Backup до версии 3.0.0-preview.</span><span class="sxs-lookup"><span data-stu-id="ff120-271">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="ff120-272">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-272">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="ff120-273">Добавлен параметр TargetResourceGroupName для Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="ff120-273">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="ff120-274">Группа ресурсов, в которую восстанавливаются управляемые диски.</span><span class="sxs-lookup"><span data-stu-id="ff120-274">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="ff120-275">Применимо к резервной копии виртуальной машины с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="ff120-275">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="ff120-276">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="ff120-276">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="ff120-277">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-277">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="ff120-278">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ff120-278">AzureRM.RedisCache</span></span>
* <span data-ttu-id="ff120-279">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-279">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="ff120-280">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="ff120-280">AzureRM.Relay</span></span>
* <span data-ttu-id="ff120-281">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-281">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ff120-282">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ff120-282">AzureRM.Resources</span></span>
* <span data-ttu-id="ff120-283">Поддержка развертывания шаблонов в области подписки.</span><span class="sxs-lookup"><span data-stu-id="ff120-283">Support template deployment at subscription scope.</span></span> <span data-ttu-id="ff120-284">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="ff120-284">Add new Cmdlets:</span></span>
    - <span data-ttu-id="ff120-285">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ff120-285">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="ff120-286">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ff120-286">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="ff120-287">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ff120-287">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="ff120-288">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ff120-288">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="ff120-289">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ff120-289">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="ff120-290">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="ff120-290">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="ff120-291">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="ff120-291">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="ff120-292">Устранена проблема, когда при передаче контекста в Set-AzureRmResource возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="ff120-292">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="ff120-293">Исправлен пример в New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="ff120-293">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="ff120-294">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-294">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="ff120-295">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="ff120-295">AzureRM.Scheduler</span></span>
* <span data-ttu-id="ff120-296">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-296">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ff120-297">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ff120-297">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ff120-298">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-298">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="ff120-299">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ff120-299">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="ff120-300">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-300">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ff120-301">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ff120-301">AzureRM.Sql</span></span>
* <span data-ttu-id="ff120-302">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-302">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="ff120-303">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="ff120-303">AzureRM.Storage</span></span>
* <span data-ttu-id="ff120-304">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-304">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="ff120-305">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="ff120-305">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="ff120-306">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-306">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="ff120-307">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="ff120-307">AzureRM.Tags</span></span>
* <span data-ttu-id="ff120-308">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-308">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="ff120-309">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ff120-309">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="ff120-310">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-310">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="ff120-311">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="ff120-311">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="ff120-312">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-312">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ff120-313">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ff120-313">AzureRM.Websites</span></span>
* <span data-ttu-id="ff120-314">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-314">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="ff120-315">6.6.0 — июль 2018 г.</span><span class="sxs-lookup"><span data-stu-id="ff120-315">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ff120-316">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="ff120-316">General</span></span>
* <span data-ttu-id="ff120-317">Обновлены все файлы справки: включены полные типы параметров и исправлены типы входных и выходных данных.</span><span class="sxs-lookup"><span data-stu-id="ff120-317">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="ff120-318">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ff120-318">AzureRM.Profile</span></span>
* <span data-ttu-id="ff120-319">Обновлена библиотека Common.Strategy: теперь можно проверить, совместима ли текущая конфигурация ресурса с целевым ресурсом.</span><span class="sxs-lookup"><span data-stu-id="ff120-319">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="ff120-320">В Common.Storage добавлены типы ps1xml.</span><span class="sxs-lookup"><span data-stu-id="ff120-320">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="ff120-321">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="ff120-321">Azure.Storage</span></span>
* <span data-ttu-id="ff120-322">Добавлена поддержка для получения контекста хранилища из DefaultProfile.</span><span class="sxs-lookup"><span data-stu-id="ff120-322">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="ff120-323">В свойства типов выходных данных командлетов добавлен атрибут Ps1XmlAttribute.</span><span class="sxs-lookup"><span data-stu-id="ff120-323">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="ff120-324">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ff120-324">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="ff120-325">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6370.</span><span class="sxs-lookup"><span data-stu-id="ff120-325">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="ff120-326">В AutoMapper исправлена ошибка, препятствовавшая преобразованию PsApiManagementApi в ApiContract.</span><span class="sxs-lookup"><span data-stu-id="ff120-326">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="ff120-327">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6515.</span><span class="sxs-lookup"><span data-stu-id="ff120-327">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="ff120-328">В File.Save исправлена ошибка, связанная с перегрузкой типом кодировки.</span><span class="sxs-lookup"><span data-stu-id="ff120-328">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="ff120-329">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6560.</span><span class="sxs-lookup"><span data-stu-id="ff120-329">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="ff120-330">Выполнено обновление до версии NuGet 4.0.3, что позволило исправить исключение шаблона в apiId.</span><span class="sxs-lookup"><span data-stu-id="ff120-330">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ff120-331">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ff120-331">AzureRM.Compute</span></span>
* <span data-ttu-id="ff120-332">Устранена ошибка при создании виртуальной машины с помощью командлета New-AzureRmVm и параметра DiskFileParameterSet, которая возникала из-за переименования типа учетной записи хранения PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="ff120-332">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="ff120-333">Исправлен командлет Invoke-AzureRmVMRunCommand.</span><span class="sxs-lookup"><span data-stu-id="ff120-333">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="ff120-334">Командлет Get-AzureRmAvailabilitySet теперь может выводить список всех групп доступности в подписке.</span><span class="sxs-lookup"><span data-stu-id="ff120-334">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="ff120-335">(Параметр ResouceGroupName теперь является необязательным.)</span><span class="sxs-lookup"><span data-stu-id="ff120-335">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="ff120-336">Обновлен параметр SimpleParameterSet командлета New-AzureRmVm, что позволило использовать ускоренную сеть на соответствующих виртуальных машинах.</span><span class="sxs-lookup"><span data-stu-id="ff120-336">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="ff120-337">Обновлен простой набор параметров New-AzureRmVmss, что позволило отменять создание масштабируемого набора виртуальных машин, если указанная пользователем подсистема балансировки нагрузки уже существует.</span><span class="sxs-lookup"><span data-stu-id="ff120-337">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="ff120-338">Обновлен пример для New-AzureRmDisk.</span><span class="sxs-lookup"><span data-stu-id="ff120-338">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="ff120-339">Добавлен пример для New-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="ff120-339">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="ff120-340">Обновлено описание командлета Set-AzureRmVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="ff120-340">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="ff120-341">Обновлен пример 1 для Set-AzureRmVMBginfoExtension: исправлены орфографические ошибки и префикс.</span><span class="sxs-lookup"><span data-stu-id="ff120-341">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="ff120-342">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ff120-342">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="ff120-343">Пакет .NET SDK для ADF обновлен до версии 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="ff120-343">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="ff120-344">Добавлена поддержка совместного использования локальной среды IR несколькими фабриками данных.</span><span class="sxs-lookup"><span data-stu-id="ff120-344">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="ff120-345">Добавлен новый параметр -SharedIntegrationRuntimeResourceId для командлета Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-345">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="ff120-346">Добавлен новый необязательный параметр -LinkedDataFactoryName для командлета Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="ff120-346">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="ff120-347">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ff120-347">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="ff120-348">Пакет SDK для плоскости данных (Microsoft.Azure.DataLake.Store) обновлен до версии 1.1.9.</span><span class="sxs-lookup"><span data-stu-id="ff120-348">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="ff120-349">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="ff120-349">AzureRM.EventHub</span></span>
* <span data-ttu-id="ff120-350">Обновлена конвейерная передача для InputObject и ResourceId в командлетах remove.</span><span class="sxs-lookup"><span data-stu-id="ff120-350">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="ff120-351">AzureRM.Insights;</span><span class="sxs-lookup"><span data-stu-id="ff120-351">AzureRM.Insights</span></span>
* <span data-ttu-id="ff120-352">Исправлено форматирование OutputType в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="ff120-352">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="ff120-353">Применен пакет SDK Microsoft.Azure.Management.Monitor 0.19.1-preview.</span><span class="sxs-lookup"><span data-stu-id="ff120-353">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="ff120-354">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ff120-354">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ff120-355">Исправлена проблема с конвейерной передачей в командлете Set-AzureRmKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="ff120-355">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ff120-356">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ff120-356">AzureRM.Network</span></span>
* <span data-ttu-id="ff120-357">Добавлены примеры для командлетов LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="ff120-357">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ff120-358">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ff120-358">AzureRM.Resources</span></span>
* <span data-ttu-id="ff120-359">Устранена проблема, возникавшая при указании имени и значения тега для Get-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="ff120-359">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="ff120-360">Исправлен сценарий конвейерной передачи в Set-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="ff120-360">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ff120-361">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ff120-361">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ff120-362">Обновлена конвейерная передача для InputObject и ResourceId в командлетах remove.</span><span class="sxs-lookup"><span data-stu-id="ff120-362">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="ff120-363">Исправлено несколько ошибок.</span><span class="sxs-lookup"><span data-stu-id="ff120-363">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="ff120-364">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ff120-364">AzureRM.Sql</span></span>
* <span data-ttu-id="ff120-365">Добавлена поддержка Advanced Threat Protection для сервера с помощью следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="ff120-365">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="ff120-366">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="ff120-366">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="ff120-367">Добавлена поддержка оценки уязвимостей с помощью следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="ff120-367">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="ff120-368">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings;</span><span class="sxs-lookup"><span data-stu-id="ff120-368">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="ff120-369">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline;</span><span class="sxs-lookup"><span data-stu-id="ff120-369">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="ff120-370">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan.</span><span class="sxs-lookup"><span data-stu-id="ff120-370">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="ff120-371">Исправлен пример для Remove-AzureRmSqlServerFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="ff120-371">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="ff120-372">Исправлена неправильная обработка даты и времени для базового языка и региональных параметров, отличных от США, в Get-AzureSqlSyncGroupLog.</span><span class="sxs-lookup"><span data-stu-id="ff120-372">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="ff120-373">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="ff120-373">AzureRM.Storage</span></span>
* <span data-ttu-id="ff120-374">В свойства типов выходных данных командлетов добавлен атрибут Ps1XmlAttribute.</span><span class="sxs-lookup"><span data-stu-id="ff120-374">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="ff120-375">Выходные данные командлетов StorageAccount теперь отображаются в виде таблицы.</span><span class="sxs-lookup"><span data-stu-id="ff120-375">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="ff120-376">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ff120-376">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="ff120-377">New-AzureRmStorageAccount;</span><span class="sxs-lookup"><span data-stu-id="ff120-377">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="ff120-378">Set-AzureRmStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="ff120-378">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="ff120-379">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="ff120-379">AzureRM.Tags</span></span>
* <span data-ttu-id="ff120-380">Удалено неверное утверждение из справки по командлетам Tag.</span><span class="sxs-lookup"><span data-stu-id="ff120-380">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="ff120-381">6.5.0 — июль 2018 г.</span><span class="sxs-lookup"><span data-stu-id="ff120-381">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ff120-382">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ff120-382">AzureRM.Profile</span></span>
* <span data-ttu-id="ff120-383">Обновлена справка для командлета Get-AzureRmContextAutosaveSetting.</span><span class="sxs-lookup"><span data-stu-id="ff120-383">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="ff120-384">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="ff120-384">Azure.Storage</span></span>
* <span data-ttu-id="ff120-385">Добавлена поддержка отправки BLOB-объекта или файла с помощью токена SAS, доступного только для записи.</span><span class="sxs-lookup"><span data-stu-id="ff120-385">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="ff120-386">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ff120-386">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="ff120-387">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ff120-387">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="ff120-388">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ff120-388">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="ff120-389">Для AS добавлено обязательное свойство ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="ff120-389">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="ff120-390">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="ff120-390">AzureRM.Automation</span></span>
* <span data-ttu-id="ff120-391">Обновлена справка и добавлены примеры для командлета New-AzureRMAutomationSchedule.</span><span class="sxs-lookup"><span data-stu-id="ff120-391">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ff120-392">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ff120-392">AzureRM.Compute</span></span>
* <span data-ttu-id="ff120-393">Добавлен параметр -Tag для командлета Update/New-AzureRmAvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="ff120-393">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="ff120-394">Добавлен пример для командлета Add-AzureRmVmssExtension.</span><span class="sxs-lookup"><span data-stu-id="ff120-394">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="ff120-395">Добавлены примеры для командлета Remove-AzureRmVmssExtension.</span><span class="sxs-lookup"><span data-stu-id="ff120-395">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="ff120-396">Обновлена справка для командлета Set-AzureRmVMAccessExtension.</span><span class="sxs-lookup"><span data-stu-id="ff120-396">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="ff120-397">Изменен класс SimpleParameterSet для командлета New-AzureRmVmss: теперь для SinglePlacementGroup по умолчанию задается значение false, а также добавляется параметр-переключатель SinglePlacementGroup, который позволяет пользователю создать VMSS в одной группе размещения.</span><span class="sxs-lookup"><span data-stu-id="ff120-397">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="ff120-398">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="ff120-398">AzureRM.EventHub</span></span>
* <span data-ttu-id="ff120-399">В класс PSEventHubDRConfigurationAttributes добавлено доступное только для чтения свойство PendingReplicationOperationsCount, которое показывает количество ожидающих репликации операций во время реплицирования.</span><span class="sxs-lookup"><span data-stu-id="ff120-399">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="ff120-400">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ff120-400">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ff120-401">Обновлено сообщение об ошибке для командлета Set-AzureRmKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="ff120-401">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="ff120-402">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ff120-402">AzureRM.LogicApp</span></span>
* <span data-ttu-id="ff120-403">Исправлена ошибка "parameter set could not be resolved" (не удалось разрешить заданный параметр) в командлете New-AzureRmLogicApp.</span><span class="sxs-lookup"><span data-stu-id="ff120-403">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ff120-404">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ff120-404">AzureRM.Network</span></span>
* <span data-ttu-id="ff120-405">Включен пиринг между виртуальными сетями в нескольких клиентах для командлета Set/Add-AzureRmVirtualNetworkPeering.</span><span class="sxs-lookup"><span data-stu-id="ff120-405">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="ff120-406">Для шлюза приложений обновлены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="ff120-406">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="ff120-407">New-AzureRmApplicationGateway: добавлены флаг EnableFIPS и поддержка зон.</span><span class="sxs-lookup"><span data-stu-id="ff120-407">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="ff120-408">New-AzureRmApplicationGatewaySku: добавлены новые номера SKU Standard_v2 и WAF_v2.</span><span class="sxs-lookup"><span data-stu-id="ff120-408">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="ff120-409">Set-AzureRmApplicationGatewaySku: добавлены новые номера SKU Standard_v2 и WAF_v2.</span><span class="sxs-lookup"><span data-stu-id="ff120-409">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="ff120-410">Командлеты RouteTable пересозданы в последней версии генератора.</span><span class="sxs-lookup"><span data-stu-id="ff120-410">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="ff120-411">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="ff120-411">AzureRM.Relay</span></span>
* <span data-ttu-id="ff120-412">Обновлены файлы Markdown, исправлена проблема с именем параметра в примере.</span><span class="sxs-lookup"><span data-stu-id="ff120-412">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ff120-413">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ff120-413">AzureRM.Resources</span></span>
* <span data-ttu-id="ff120-414">Обновлены командлеты Roleassignment и roledefinition:</span><span class="sxs-lookup"><span data-stu-id="ff120-414">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="ff120-415">Удалены лишние вызовы roledefinition, выполняемые в ходе разбиения на страницы.</span><span class="sxs-lookup"><span data-stu-id="ff120-415">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="ff120-416">Исправлен командлет Get-AzureRmRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="ff120-416">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="ff120-417">Исправлена работа параметра -ExpandPrincipalGroups.</span><span class="sxs-lookup"><span data-stu-id="ff120-417">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="ff120-418">Устранена проблема в командлете Get-AzureRmResource, заключающая в том, что в параметре -ResourceType учитывался регистр символов.</span><span class="sxs-lookup"><span data-stu-id="ff120-418">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ff120-419">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ff120-419">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ff120-420">Добавлены параметры top и skip для командлетов list.</span><span class="sxs-lookup"><span data-stu-id="ff120-420">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="ff120-421">Добавлены командлеты для перехода с пространства имен ценовой категории "Стандартный" на пространство ценовой категории "Премиум":</span><span class="sxs-lookup"><span data-stu-id="ff120-421">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="ff120-422">Start-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="ff120-422">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="ff120-423">Get-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="ff120-423">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="ff120-424">Complete-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="ff120-424">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="ff120-425">Stop-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="ff120-425">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="ff120-426">Remove-AzureRmServiceBusMigration.</span><span class="sxs-lookup"><span data-stu-id="ff120-426">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="ff120-427">В класс PSServiceBusDRConfigurationAttributes добавлено доступное только для чтения свойство PendingReplicationOperationsCount, которое показывает количество ожидающих репликации операций во время реплицирования.</span><span class="sxs-lookup"><span data-stu-id="ff120-427">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="ff120-428">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ff120-428">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="ff120-429">Обновлен пример для командлета New-AzureRmServiceFabricCluster.</span><span class="sxs-lookup"><span data-stu-id="ff120-429">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ff120-430">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ff120-430">AzureRM.Sql</span></span>
* <span data-ttu-id="ff120-431">Добавлены новые командлеты для Management.Sql, позволяющие клиентам добавлять сертификат TDE в экземпляр SQL Server или управляемый экземпляр:</span><span class="sxs-lookup"><span data-stu-id="ff120-431">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="ff120-432">Add-AzureRmSqlServerTransparentDataEncryptionCertificate;</span><span class="sxs-lookup"><span data-stu-id="ff120-432">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="ff120-433">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate.</span><span class="sxs-lookup"><span data-stu-id="ff120-433">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ff120-434">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ff120-434">AzureRM.Websites</span></span>
* <span data-ttu-id="ff120-435">`Set-AzureRmWebApp -AssignIdentity` и `Set-AzureRmWebAppSlot -AssignIdentity` при установленном значении false теперь будут удалять свойство Identity из объекта сайта. Также при этом будет удаляться тег предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="ff120-435">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="ff120-436">Обновлен пример для `Get-AzureRmWebAppMetrics` и `Get-AzureRmAppServicePlanMetrics`.</span><span class="sxs-lookup"><span data-stu-id="ff120-436">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="ff120-437">`Set-AzureRmWebApp -PhpVersion` теперь поддерживает off как допустимую версию PHP.</span><span class="sxs-lookup"><span data-stu-id="ff120-437">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="ff120-438">6.4.0 — июль 2018 г.</span><span class="sxs-lookup"><span data-stu-id="ff120-438">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ff120-439">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="ff120-439">General</span></span>
* <span data-ttu-id="ff120-440">Исправлено форматирование OutputType в файлах справки для большинства модулей.</span><span class="sxs-lookup"><span data-stu-id="ff120-440">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="ff120-441">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ff120-441">AzureRM.Profile</span></span>
* <span data-ttu-id="ff120-442">В основные типы выходных данных добавлен атрибут Ps1Xml.</span><span class="sxs-lookup"><span data-stu-id="ff120-442">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ff120-443">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ff120-443">AzureRM.Compute</span></span>
* <span data-ttu-id="ff120-444">Функция добавления тега IP-адреса для масштабируемого набора виртуальных машин (VMSS)</span><span class="sxs-lookup"><span data-stu-id="ff120-444">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="ff120-445">Добавлен командлет New-AzureRmVmssIpTagConfig.</span><span class="sxs-lookup"><span data-stu-id="ff120-445">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="ff120-446">В New-AzureRmVmssIpConfig добавлен параметр IpTag.</span><span class="sxs-lookup"><span data-stu-id="ff120-446">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="ff120-447">Функция автоматического отката ОС для VMSS</span><span class="sxs-lookup"><span data-stu-id="ff120-447">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="ff120-448">В New-AzureRmVmssConfig и Update-AzureRmVmss добавлены параметры DisableAutoRollback.</span><span class="sxs-lookup"><span data-stu-id="ff120-448">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="ff120-449">Функция ведения журнала обновлений ОС для VMSS</span><span class="sxs-lookup"><span data-stu-id="ff120-449">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="ff120-450">В Get-AzureRmVmss добавлен параметр OSUpgradeHistory.</span><span class="sxs-lookup"><span data-stu-id="ff120-450">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="ff120-451">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="ff120-451">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="ff120-452">Добавлена поддержка списков управления доступом к каталогу с использованием следующих команд:</span><span class="sxs-lookup"><span data-stu-id="ff120-452">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="ff120-453">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry;</span><span class="sxs-lookup"><span data-stu-id="ff120-453">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="ff120-454">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry;</span><span class="sxs-lookup"><span data-stu-id="ff120-454">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="ff120-455">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="ff120-455">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="ff120-456">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ff120-456">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="ff120-457">Добавлены поддержка отмены выполнения и отслеживание хода выполнения для Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl и Remove-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="ff120-457">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="ff120-458">Добавлена поддержка отмены выполнения для Export-AzureRmDataLakeStoreChildItemProperties.</span><span class="sxs-lookup"><span data-stu-id="ff120-458">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="ff120-459">Исправлена очистка сообщений об отладке для командлетов, которые выполняют рекурсивные операции.</span><span class="sxs-lookup"><span data-stu-id="ff120-459">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="ff120-460">Исправлено расположение тестовых данных для командлетов DataLake.</span><span class="sxs-lookup"><span data-stu-id="ff120-460">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="ff120-461">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="ff120-461">AzureRM.EventHub</span></span>
* <span data-ttu-id="ff120-462">Для командлетов вывода списка операций Get-AzureRmEventHub и Get-AzureRmEventHubConsumerGroup добавлен необязательный параметр MaxCount.</span><span class="sxs-lookup"><span data-stu-id="ff120-462">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="ff120-463">Исправлена проблема с командлетом New-AzureRmEventHub, из-за которой требовалось указать по крайней мере один параметр при создании концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="ff120-463">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="ff120-464">Добавлен набор параметров по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ff120-464">Provided Default Parameter set.</span></span>
* <span data-ttu-id="ff120-465">Для командлета New-AzureRmEventHubKey добавлен необязательный параметр -KeyValue, который позволяет пользователю предоставить значение ключа.</span><span class="sxs-lookup"><span data-stu-id="ff120-465">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="ff120-466">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ff120-466">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ff120-467">Исправлена ошибка, из-за которой при выполнении командлета Get-AzureRmKeyVault с параметром -Tag возвращались все ресурсы.</span><span class="sxs-lookup"><span data-stu-id="ff120-467">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ff120-468">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ff120-468">AzureRM.Network</span></span>
* <span data-ttu-id="ff120-469">Для параметра шлюзов виртуальной вести, избыточных в пределах зоны, предоставлены новые номера SKU.</span><span class="sxs-lookup"><span data-stu-id="ff120-469">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="ff120-470">Добавлены новые команды для функции поддержки партнерских API для ExpressRoute, развертываемых с помощью ARM:</span><span class="sxs-lookup"><span data-stu-id="ff120-470">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="ff120-471">добавлена команда Get-AzureRmExpressRouteCrossConnection;</span><span class="sxs-lookup"><span data-stu-id="ff120-471">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="ff120-472">добавлена команда Set-AzureRmExpressRouteCrossConnection;</span><span class="sxs-lookup"><span data-stu-id="ff120-472">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="ff120-473">добавлена команда Add-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="ff120-473">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="ff120-474">добавлена команда Get-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="ff120-474">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="ff120-475">добавлена команда Remove-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="ff120-475">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="ff120-476">добавлена команда Get-AzureRMExpressRouteCrossConnectionArpTable;</span><span class="sxs-lookup"><span data-stu-id="ff120-476">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="ff120-477">добавлена команда Get-AzureRMExpressRouteCrossConnectionRouteTable;</span><span class="sxs-lookup"><span data-stu-id="ff120-477">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="ff120-478">добавлена команда Get-AzureRMExpressRouteCrossConnectionRouteTableSummary.</span><span class="sxs-lookup"><span data-stu-id="ff120-478">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="ff120-479">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="ff120-479">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="ff120-480">Добавлен командлет Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="ff120-480">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="ff120-481">Этот командлет принимает идентификатор виртуальной машины и проверяет, защищена ли виртуальная машина с помощью какого-либо хранилища в подписке.</span><span class="sxs-lookup"><span data-stu-id="ff120-481">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="ff120-482">Если такое хранилище существует, командлет выводит данные о нем.</span><span class="sxs-lookup"><span data-stu-id="ff120-482">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ff120-483">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ff120-483">AzureRM.Resources</span></span>
* <span data-ttu-id="ff120-484">Обновлены командлеты Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="ff120-484">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="ff120-485">Добавлена поддержка вывода списка значений параметра -Scope на уровне группы управления.</span><span class="sxs-lookup"><span data-stu-id="ff120-485">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="ff120-486">Добавлена поддержка для получения отдельных назначений со значениями -Scope на уровне группы управления.</span><span class="sxs-lookup"><span data-stu-id="ff120-486">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="ff120-487">Для параметра управления добавлены параметры -Effective и -All.</span><span class="sxs-lookup"><span data-stu-id="ff120-487">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="ff120-488">Обновлены командлеты Get/New/Remove/Set-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="ff120-488">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="ff120-489">Добавлен параметр -ManagementGroupName для применения операций к заданной группе управления.</span><span class="sxs-lookup"><span data-stu-id="ff120-489">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="ff120-490">Добавлен параметр -SubscriptionId для применения операций к заданной подписке.</span><span class="sxs-lookup"><span data-stu-id="ff120-490">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="ff120-491">Обновлены командлеты Get/New/Remove/Set-AzureRmPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="ff120-491">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="ff120-492">Добавлен параметр -ManagementGroupName для применения операций к заданной группе управления.</span><span class="sxs-lookup"><span data-stu-id="ff120-492">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="ff120-493">Добавлен параметр -SubscriptionId для применения операций к заданной подписке.</span><span class="sxs-lookup"><span data-stu-id="ff120-493">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="ff120-494">Добавлена поддержка ссылок на секрет KeyVault в параметрах при использовании TemplateParameterObject в New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="ff120-494">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="ff120-495">Устранена проблема, из-за которой параметр -EndDate игнорировался в New-AzureRmADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="ff120-495">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="ff120-496">Устранена проблема, из-за которой в Add-AzureRmADGroupMember использовался неверный URL-адрес для запроса.</span><span class="sxs-lookup"><span data-stu-id="ff120-496">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="ff120-497">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ff120-497">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ff120-498">Для командлета New-AzureRmServiceBusKey добавлен необязательный параметр -KeyValue, который позволяет пользователю предоставить значение ключа.</span><span class="sxs-lookup"><span data-stu-id="ff120-498">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ff120-499">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ff120-499">AzureRM.Sql</span></span>
* <span data-ttu-id="ff120-500">В справке по New-AzureRmSqlDatabaseRestorePoint добавлено описание определяемых пользователем точек восстановления для хранилища данных SQL.</span><span class="sxs-lookup"><span data-stu-id="ff120-500">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="ff120-501">Обновлена документация по параметру -ComputeGeneration, используемого в нескольких командлетах.</span><span class="sxs-lookup"><span data-stu-id="ff120-501">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="ff120-502">6.3.0 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="ff120-502">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ff120-503">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ff120-503">AzureRM.Profile</span></span>
* <span data-ttu-id="ff120-504">Обновлены сообщения об ошибках для Enable-AzureRmContextAutoSave.</span><span class="sxs-lookup"><span data-stu-id="ff120-504">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="ff120-505">Создание контекста для каждой подписки при выполнении Connect-AzureRmAccount без предыдущего контекста.</span><span class="sxs-lookup"><span data-stu-id="ff120-505">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="ff120-506">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="ff120-506">Azure.Storage</span></span>
* <span data-ttu-id="ff120-507">В файлы справки добавлены дополнительные сведения о параметре -Permissions.</span><span class="sxs-lookup"><span data-stu-id="ff120-507">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ff120-508">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ff120-508">AzureRM.Compute</span></span>
* <span data-ttu-id="ff120-509">Get-AzureRmVmDiskEncryptionStatus устраняет проблему, которая наблюдалась на виртуальных машинах без дисков данных.</span><span class="sxs-lookup"><span data-stu-id="ff120-509">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="ff120-510">Обновлена версия клиентской библиотеки Compute для исправления следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="ff120-510">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="ff120-511">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="ff120-511">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="ff120-512">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="ff120-512">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="ff120-513">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="ff120-513">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="ff120-514">В следующих командлетах исправлено отображение неправильных значений operation ID и operation status:</span><span class="sxs-lookup"><span data-stu-id="ff120-514">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="ff120-515">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ff120-515">Start-AzureRmVM</span></span>
    - <span data-ttu-id="ff120-516">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ff120-516">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="ff120-517">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ff120-517">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="ff120-518">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ff120-518">Set-AzureRmVM</span></span>
    - <span data-ttu-id="ff120-519">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="ff120-519">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="ff120-520">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ff120-520">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="ff120-521">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="ff120-521">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="ff120-522">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="ff120-522">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="ff120-523">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ff120-523">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="ff120-524">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ff120-524">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="ff120-525">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ff120-525">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="ff120-526">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ff120-526">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="ff120-527">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="ff120-527">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="ff120-528">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="ff120-528">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="ff120-529">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="ff120-529">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="ff120-530">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="ff120-530">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="ff120-531">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="ff120-531">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="ff120-532">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="ff120-532">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="ff120-533">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ff120-533">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="ff120-534">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ff120-534">AzureRM.EventGrid</span></span>
* <span data-ttu-id="ff120-535">Удалены условия проверки ValidateNotNullOrEmpty для SubjectBeginsWith/SubjectEndsWith в командлете Update-AzureRmEventGridSubscription, что позволяет при необходимости заменять эти параметры пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="ff120-535">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="ff120-536">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ff120-536">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ff120-537">Исправлена ошибка, когда при выполнении командлета Get-AzureRmKeyVault -Tag не возвращается ни один тег.</span><span class="sxs-lookup"><span data-stu-id="ff120-537">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="ff120-538">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ff120-538">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="ff120-539">Общедоступный выпуск командлетов Policy Insights.</span><span class="sxs-lookup"><span data-stu-id="ff120-539">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="ff120-540">Используется API версии 2018-04-04.</span><span class="sxs-lookup"><span data-stu-id="ff120-540">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="ff120-541">К результатам Get-AzureRmPolicyStateSummary добавлено PolicyDefinitionReferenceId.</span><span class="sxs-lookup"><span data-stu-id="ff120-541">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="ff120-542">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="ff120-542">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="ff120-543">Для командлетов RecoveryServices.Backup добавлен параметр -Vault.</span><span class="sxs-lookup"><span data-stu-id="ff120-543">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="ff120-544">Передача этого параметра переопределяет командлет Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="ff120-544">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ff120-545">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ff120-545">AzureRM.Sql</span></span>
* <span data-ttu-id="ff120-546">В файле справки обновлен пример для командлета Get-AzureRmSqlDatabaseExpanded.</span><span class="sxs-lookup"><span data-stu-id="ff120-546">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="ff120-547">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ff120-547">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="ff120-548">Обновлен файл справки для командлета Add-AzureRmTrafficManagerEndpointConfig.</span><span class="sxs-lookup"><span data-stu-id="ff120-548">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ff120-549">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ff120-549">AzureRM.Websites</span></span>
* <span data-ttu-id="ff120-550">Изменено действие командлета Set-AzureRmWebApp. Теперь он не перезаписывает AppSettings, если используется параметр -AssignIdentity.</span><span class="sxs-lookup"><span data-stu-id="ff120-550">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="ff120-551">Командлет New-AzureRmWebAppSlot теперь учитывает дополнительный параметр AppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="ff120-551">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="ff120-552">6.2.1 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="ff120-552">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="ff120-553">AzureRM.OperationalInsights;</span><span class="sxs-lookup"><span data-stu-id="ff120-553">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="ff120-554">В обновленной модели PSWorkspace Network может использовать type в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="ff120-554">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="ff120-555">6.2.0 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="ff120-555">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ff120-556">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ff120-556">AzureRM.Profile</span></span>
* <span data-ttu-id="ff120-557">Исправлена ошибка с загрузкой Newtonsoft.Json версии 10.0.3 во время импорта модуля.</span><span class="sxs-lookup"><span data-stu-id="ff120-557">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ff120-558">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ff120-558">AzureRM.Compute</span></span>
* <span data-ttu-id="ff120-559">Функция обновления виртуальных машин VMSS.</span><span class="sxs-lookup"><span data-stu-id="ff120-559">VMSS VM Update feature</span></span>
    - <span data-ttu-id="ff120-560">Добавлены командлеты Update-AzureRmVmssVM и New-AzureRmVMDataDisk.</span><span class="sxs-lookup"><span data-stu-id="ff120-560">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="ff120-561">В командлет Add-AzureRmVMDataDisk добавлен параметр VirtualMachineScaleSetVM, который позволяет добавлять диски данных в виртуальные машины VMSS.</span><span class="sxs-lookup"><span data-stu-id="ff120-561">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="ff120-562">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ff120-562">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="ff120-563">Пакет SDK для ADF .NET обновлен до версии 0.8.0-preview. Новая версия содержит такие изменения:</span><span class="sxs-lookup"><span data-stu-id="ff120-563">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="ff120-564">добавлена операция для настройки репозитория фабрики;</span><span class="sxs-lookup"><span data-stu-id="ff120-564">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="ff120-565">связанная служба QuickBooks LinkedService теперь предоставляет свойства consumerKey и consumerSecret;</span><span class="sxs-lookup"><span data-stu-id="ff120-565">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="ff120-566">тип нескольких моделей изменен с SecretBase на Object;</span><span class="sxs-lookup"><span data-stu-id="ff120-566">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="ff120-567">добавлен триггер событий BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="ff120-567">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="ff120-568">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ff120-568">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ff120-569">В документацию добавлены примеры выходных данных.</span><span class="sxs-lookup"><span data-stu-id="ff120-569">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="ff120-570">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ff120-570">AzureRM.Network</span></span>
* <span data-ttu-id="ff120-571">В командлеты Наблюдателя за сетями добавлены параметры Аналитики трафика.</span><span class="sxs-lookup"><span data-stu-id="ff120-571">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ff120-572">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ff120-572">AzureRM.Resources</span></span>
* <span data-ttu-id="ff120-573">Исправлена ошибка, когда командлет Get-AzureRmResource возвращает свойство Properties объектов PSResource.</span><span class="sxs-lookup"><span data-stu-id="ff120-573">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="ff120-574">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="ff120-574">AzureRM.Scheduler</span></span>
* <span data-ttu-id="ff120-575">Исправлена ошибка, когда обновление ServiceBusQueueJob не задает новые значения для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="ff120-575">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="ff120-576">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ff120-576">AzureRM.Sql</span></span>
* <span data-ttu-id="ff120-577">В перечисленные ниже командлеты добавлен необязательный параметр LicenseType.</span><span class="sxs-lookup"><span data-stu-id="ff120-577">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="ff120-578">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="ff120-578">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="ff120-579">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool;</span><span class="sxs-lookup"><span data-stu-id="ff120-579">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="ff120-580">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="ff120-580">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="ff120-581">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ff120-581">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="ff120-582">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ff120-582">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ff120-583">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ff120-583">AzureRM.Websites</span></span>
* <span data-ttu-id="ff120-584">Командлет New-AzureRMWebApp теперь использует общие алгоритмы из библиотеки Strategy.</span><span class="sxs-lookup"><span data-stu-id="ff120-584">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="ff120-585">6.1.0 — май 2018 г.</span><span class="sxs-lookup"><span data-stu-id="ff120-585">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ff120-586">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ff120-586">AzureRM.Profile</span></span>
* <span data-ttu-id="ff120-587">Устранена проблема с выполнением Clear-AzureRmContext, при которой сохранялся пустой контекст с именем предыдущего контекста по умолчанию, что не позволяло пользователю создать новый контекст со старым именем.</span><span class="sxs-lookup"><span data-stu-id="ff120-587">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="ff120-588">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ff120-588">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="ff120-589">Включены операции связывания и отмены связи в автономной системе.</span><span class="sxs-lookup"><span data-stu-id="ff120-589">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="ff120-590">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ff120-590">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="ff120-591">Добавлена поддержка ApiVersions, ApiReleases и ApiRevisions.</span><span class="sxs-lookup"><span data-stu-id="ff120-591">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="ff120-592">Добавлена поддержка серверной части ServiceFabric.</span><span class="sxs-lookup"><span data-stu-id="ff120-592">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="ff120-593">Добавлена поддержка средства ведения журнала Application Insights.</span><span class="sxs-lookup"><span data-stu-id="ff120-593">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="ff120-594">Добавлена поддержка для распознавания номера SKU уровня "Базовый" как допустимого номера SKU службы управления API.</span><span class="sxs-lookup"><span data-stu-id="ff120-594">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="ff120-595">Добавлена поддержка установки сертификатов, выданных частным центром сертификации в качестве корневого или обычного ЦС.</span><span class="sxs-lookup"><span data-stu-id="ff120-595">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="ff120-596">Добавлена поддержка для приема пользовательских SSL-сертификатов с помощью KeyVault и нескольких имен узлов прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="ff120-596">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="ff120-597">Добавлена поддержка для удостоверения MSI.</span><span class="sxs-lookup"><span data-stu-id="ff120-597">Added support for MSI identity</span></span>
* <span data-ttu-id="ff120-598">Добавлена поддержка для принятия политик с помощью URL-адреса. Примечание. Указанные ниже командлеты в следующей версии будут отмечены как нерекомендуемые.</span><span class="sxs-lookup"><span data-stu-id="ff120-598">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="ff120-599">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="ff120-599">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="ff120-600">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff120-600">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="ff120-601">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="ff120-601">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="ff120-602">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="ff120-602">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="ff120-603">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="ff120-603">AzureRM.Batch</span></span>
* <span data-ttu-id="ff120-604">Выпущен новый командлет Get-AzureBatchPoolNodeCounts.</span><span class="sxs-lookup"><span data-stu-id="ff120-604">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="ff120-605">Выпущен новый командлет Start-AzureBatchComputeNodeServiceLogUpload.</span><span class="sxs-lookup"><span data-stu-id="ff120-605">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="ff120-606">AzureRM.Consumption:</span><span class="sxs-lookup"><span data-stu-id="ff120-606">AzureRM.Consumption</span></span>
* <span data-ttu-id="ff120-607">Добавлены новые параметры Expand, ResourceGroup, InstanceName, InstanceId, Tags и командлет высшего уровня Get-AzureRmConsumptionUsageDetail.</span><span class="sxs-lookup"><span data-stu-id="ff120-607">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="ff120-608">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ff120-608">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="ff120-609">Исправлен пример для Export-AzureRmDataLakeStoreChildItemProperties.</span><span class="sxs-lookup"><span data-stu-id="ff120-609">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="ff120-610">Исправлено исключение параметра NULL при использовании рекурсии в Set-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="ff120-610">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="ff120-611">Исправлены файлы справки для Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl и Remove-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="ff120-611">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="ff120-612">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ff120-612">AzureRM.Network</span></span>
* <span data-ttu-id="ff120-613">Пакет SDK для сети обновлен с предварительной версии 18.0.0 до предварительной версии 19.0.0.</span><span class="sxs-lookup"><span data-stu-id="ff120-613">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="ff120-614">Добавлен командлет для создания конфигурации протокола.</span><span class="sxs-lookup"><span data-stu-id="ff120-614">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="ff120-615">New-AzureRmNetworkWatcherProtocolConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ff120-615">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="ff120-616">Добавлен командлет для добавления нового подключения канала к существующему каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ff120-616">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="ff120-617">Add-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="ff120-617">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="ff120-618">Добавлен командлет для удаления подключения канала к существующему каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ff120-618">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="ff120-619">Remove-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="ff120-619">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="ff120-620">Добавлен командлет для получения подключения канала.</span><span class="sxs-lookup"><span data-stu-id="ff120-620">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="ff120-621">Get-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="ff120-621">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="ff120-622">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ff120-622">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="ff120-623">Исправлена процедура аутентификации сервера с использованием созданных сертификатов (проблема № 5998).</span><span class="sxs-lookup"><span data-stu-id="ff120-623">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ff120-624">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ff120-624">AzureRM.Sql</span></span>
* <span data-ttu-id="ff120-625">Обновлены командлеты аудита, которые теперь позволяют удалять AuditActions или AuditActionGroups.</span><span class="sxs-lookup"><span data-stu-id="ff120-625">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="ff120-626">Исправлена проблема с Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy, при которой установка новой гибкой политики хранения завершалась ошибкой с сообщением "Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span><span class="sxs-lookup"><span data-stu-id="ff120-626">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="ff120-627">Please submit request with the new flexible retention policy" (Настройка политики долгосрочного хранения с помощью хранилища и политики служб восстановления Azure больше не поддерживается. Отправьте запрос с использованием новой гибкой политики хранения).</span><span class="sxs-lookup"><span data-stu-id="ff120-627">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="ff120-628">Обновлены все командлеты, связанные со службой "База данных SQL Azure", с созданием эластичных пулов и обновлением. Теперь используются новые API баз данных с поддержкой свойства номеров SKU для обеспечения масштабируемости и связанных с уровнями возможностей.</span><span class="sxs-lookup"><span data-stu-id="ff120-628">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="ff120-629">Обновлены командлеты, в том числе:</span><span class="sxs-lookup"><span data-stu-id="ff120-629">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="ff120-630">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="ff120-630">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="ff120-631">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool;</span><span class="sxs-lookup"><span data-stu-id="ff120-631">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="ff120-632">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="ff120-632">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="ff120-633">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ff120-633">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="ff120-634">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ff120-634">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="ff120-635">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ff120-635">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="ff120-636">Обновлены параметры для Get-AzureRmTrafficManagerProfile. Теперь при использовании параметра -Name требуется параметр -ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="ff120-636">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
