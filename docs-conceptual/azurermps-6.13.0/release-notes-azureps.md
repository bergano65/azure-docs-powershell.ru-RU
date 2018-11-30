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
ms.openlocfilehash: 7f517f0b3768a2075557b131158ee1264ea9ab3f
ms.sourcegitcommit: 558436c824d9b59731aa9b963cdc8df4dea932e7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/29/2018
ms.locfileid: "52587845"
---
# <a name="release-notes"></a><span data-ttu-id="e6428-103">Заметки о выпуске</span><span class="sxs-lookup"><span data-stu-id="e6428-103">Release notes</span></span>

<span data-ttu-id="e6428-104">Здесь приведен список изменений, внесенных в Azure PowerShell в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="e6428-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6130---november-2018"></a><span data-ttu-id="e6428-105">6.13.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="e6428-105">6.13.0 - November 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="e6428-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="e6428-106">AzureRM.Profile</span></span>
* <span data-ttu-id="e6428-107">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-107">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="e6428-108">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e6428-108">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="e6428-109">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="e6428-109">Update dependencies for type mapping issue</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="e6428-110">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="e6428-110">AzureRM.Automation</span></span>
* <span data-ttu-id="e6428-111">Командлеты службы автоматизации Azure на базе Swagger.</span><span class="sxs-lookup"><span data-stu-id="e6428-111">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="e6428-112">Добавлены командлеты для Управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="e6428-112">Added Update Management cmdlets</span></span>
* <span data-ttu-id="e6428-113">Добавлены командлеты для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="e6428-113">Added Source Control cmdlets</span></span>
* <span data-ttu-id="e6428-114">Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="e6428-114">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="e6428-115">Исправлена команда DSC для регистрации узла.</span><span class="sxs-lookup"><span data-stu-id="e6428-115">Fixed the DSC Register Node command</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="e6428-116">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="e6428-116">AzureRM.Compute</span></span>
* <span data-ttu-id="e6428-117">Исправлена проблема с удостоверением, назначаемым системой.</span><span class="sxs-lookup"><span data-stu-id="e6428-117">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="e6428-118">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="e6428-118">Update dependencies for type mapping issue</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="e6428-119">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e6428-119">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="e6428-120">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="e6428-120">Update dependencies for type mapping issue</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="e6428-121">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="e6428-121">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="e6428-122">Обновлено описание в примерах командлетов для Marketplace.</span><span class="sxs-lookup"><span data-stu-id="e6428-122">update the examples description for marketplace cmdlets</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="e6428-123">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="e6428-123">AzureRM.Network</span></span>
* <span data-ttu-id="e6428-124">Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="e6428-124">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="e6428-125">Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="e6428-125">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="e6428-126">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="e6428-126">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="e6428-127">Исправлены проблемы с использованием памяти в карте виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="e6428-127">Fix issues with memory usage in VirtualNetwork map</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="e6428-128">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="e6428-128">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="e6428-129">Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="e6428-129">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="e6428-130">Параметры часового пояса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="e6428-130">Converted policy timezone to uppercase.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="e6428-131">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="e6428-131">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="e6428-132">Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="e6428-132">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="e6428-133">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="e6428-133">Update dependencies for type mapping issue</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="e6428-134">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="e6428-134">AzureRM.Relay</span></span>
* <span data-ttu-id="e6428-135">Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.</span><span class="sxs-lookup"><span data-stu-id="e6428-135">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="e6428-136">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="e6428-136">AzureRM.Resources</span></span>
* <span data-ttu-id="e6428-137">Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.</span><span class="sxs-lookup"><span data-stu-id="e6428-137">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="e6428-138">Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.</span><span class="sxs-lookup"><span data-stu-id="e6428-138">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="e6428-139">Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.</span><span class="sxs-lookup"><span data-stu-id="e6428-139">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="e6428-140">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e6428-140">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="e6428-141">Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.</span><span class="sxs-lookup"><span data-stu-id="e6428-141">Add deprecation messages for upcoming breaking changes</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="e6428-142">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="e6428-142">AzureRM.Sql</span></span>
* <span data-ttu-id="e6428-143">Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="e6428-143">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="e6428-144">Get-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="e6428-144">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e6428-145">New-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="e6428-145">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e6428-146">Set-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="e6428-146">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e6428-147">Remove-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="e6428-147">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e6428-148">Get-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="e6428-148">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e6428-149">New-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="e6428-149">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e6428-150">Restore-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="e6428-150">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e6428-151">Remove-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="e6428-151">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="e6428-152">Добавлено расширенное управление политиками аудита для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="e6428-152">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="e6428-153">Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="e6428-153">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="e6428-154">Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.</span><span class="sxs-lookup"><span data-stu-id="e6428-154">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="e6428-155">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="e6428-155">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="e6428-156">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="e6428-156">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="e6428-157">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="e6428-157">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="e6428-158">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="e6428-158">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="e6428-159">Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="e6428-159">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="6120---november-2018"></a><span data-ttu-id="e6428-160">6.12.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="e6428-160">6.12.0 - November 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="e6428-161">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="e6428-161">AzureRM.Profile</span></span>
* <span data-ttu-id="e6428-162">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-162">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="e6428-163">В командлете Connect-AzureRmAccount параметр TenantId переименован на Tenant и добавлен псевдоним для TenantId.</span><span class="sxs-lookup"><span data-stu-id="e6428-163">Rename param TenantId in cmdlet Connect-AzureRmAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="e6428-164">Обновлено описание TenantId для командлета Connect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="e6428-164">Updated TenantId description for Connect-AzureRmAccount</span></span>
* <span data-ttu-id="e6428-165">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="e6428-165">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="e6428-166">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="e6428-166">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="e6428-167">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="e6428-167">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="e6428-168">Устранена проблема, при которой командлет Disconnect-AzureRmAccount вызывал сбой при отсутствии подключения.</span><span class="sxs-lookup"><span data-stu-id="e6428-168">Fix issue where 'Disconnect-AzureRmAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azurermautomation"></a><span data-ttu-id="e6428-169">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="e6428-169">AzureRM.Automation</span></span>
* <span data-ttu-id="e6428-170">Имя файла библиотеки DLL командлетов переименовано на Microsoft.Azure.Commands.Automation.dll.</span><span class="sxs-lookup"><span data-stu-id="e6428-170">Renamed cmdlet DLL filename to Microsoft.Azure.Commands.Automation.dll</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="e6428-171">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e6428-171">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="e6428-172">Добавлена операция Get-AzureRmCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="e6428-172">Add Get-AzureRmCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="e6428-173">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="e6428-173">AzureRM.Compute</span></span>
* <span data-ttu-id="e6428-174">Добавлены командлеты Add-AzureRmVmssVMDataDisk и Remove-AzureRmVmssVMDataDisk.</span><span class="sxs-lookup"><span data-stu-id="e6428-174">Add Add-AzureRmVmssVMDataDisk and Remove-AzureRmVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="e6428-175">Get-AzureRmVMImage отображает AutomaticOSUpgradeProperties.</span><span class="sxs-lookup"><span data-stu-id="e6428-175">Get-AzureRmVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="e6428-176">Устранена проблема, при которой значения параметров SetAzureRmVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="e6428-176">Fixed SetAzureRmVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="e6428-177">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e6428-177">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="e6428-178">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="e6428-178">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="e6428-179">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="e6428-179">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="e6428-180">AzureRM.Insights;</span><span class="sxs-lookup"><span data-stu-id="e6428-180">AzureRM.Insights</span></span>
* <span data-ttu-id="e6428-181">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="e6428-181">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="e6428-182">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="e6428-182">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="e6428-183">Исправлена проблема № 7513 [Insights], ппри которой для командлета Set-AzureRMDiagnosticSetting требовалось явное указание категорий во время создания параметра.</span><span class="sxs-lookup"><span data-stu-id="e6428-183">Fixed issue #7513 [Insights] Set-AzureRMDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="e6428-184">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="e6428-184">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="e6428-185">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="e6428-185">AzureRM.Network</span></span>
* <span data-ttu-id="e6428-186">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="e6428-186">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="e6428-187">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="e6428-187">Get-AzureRmExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="e6428-188">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="e6428-188">Get-AzureRmExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="e6428-189">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="e6428-189">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="e6428-190">Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="e6428-190">Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="e6428-191">Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="e6428-191">Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="e6428-192">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="e6428-192">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="e6428-193">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e6428-193">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="e6428-194">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="e6428-194">Added policy remediation cmdlets</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="e6428-195">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="e6428-195">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="e6428-196">Добавлена поддержка общих файловых ресурсов Azure в Службах восстановления.</span><span class="sxs-lookup"><span data-stu-id="e6428-196">Added support for azure file shares in recovery services.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="e6428-197">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="e6428-197">AzureRM.Resources</span></span>
* <span data-ttu-id="e6428-198">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="e6428-198">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="e6428-199">Разрешено перечисление ресурсов с использованием параметра -ResourceId для командлета Get-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="e6428-199">Allow listing resources using the '-ResourceId' parameter for 'Get-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="e6428-200">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e6428-200">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="e6428-201">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="e6428-201">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="e6428-202">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e6428-202">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="e6428-203">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="e6428-203">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="e6428-204">Исправлен командлет Add-AzureRmServiceFabricClusterCertificate.</span><span class="sxs-lookup"><span data-stu-id="e6428-204">Fix 'Add-AzureRmServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="e6428-205">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="e6428-205">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="e6428-206">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="e6428-206">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="e6428-207">Исправлен командлет Update-AzureRmServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="e6428-207">Fix 'Update-AzureRmServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="6110---october-2018"></a><span data-ttu-id="e6428-208">6.11.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="e6428-208">6.11.0 - October 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="e6428-209">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="e6428-209">AzureRM.Profile</span></span>
* <span data-ttu-id="e6428-210">Устранена проблема с Get-AzureRmSubscription в CloudShell.</span><span class="sxs-lookup"><span data-stu-id="e6428-210">Fix issue with Get-AzureRmSubscription in CloudShell</span></span>
* <span data-ttu-id="e6428-211">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-211">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="e6428-212">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="e6428-212">AzureRM.Backup</span></span>
* <span data-ttu-id="e6428-213">Командлеты Azure Backup объявлены нерекомендуемыми.</span><span class="sxs-lookup"><span data-stu-id="e6428-213">Deprecated Azure Backup cmdlets.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="e6428-214">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="e6428-214">AzureRM.Compute</span></span>
* <span data-ttu-id="e6428-215">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzureRmVm.</span><span class="sxs-lookup"><span data-stu-id="e6428-215">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzureRmVm'</span></span>
* <span data-ttu-id="e6428-216">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="e6428-216">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="e6428-217">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e6428-217">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="e6428-218">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="e6428-218">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="e6428-219">Get-AzureRmDataLakeStoreVirtualNetworkRule — позволяет получить или вывести правило виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e6428-219">Get-AzureRmDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="e6428-220">Add-AzureRmDataLakeStoreVirtualNetworkRule — позволяет добавить правило виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e6428-220">Add-AzureRmDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="e6428-221">Set-AzureRmDataLakeStoreVirtualNetworkRule — позволяет изменить определенное правило виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e6428-221">Set-AzureRmDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="e6428-222">Remove-AzureRmDataLakeStoreVirtualNetworkRule — позволяет удалить правило виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e6428-222">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="e6428-223">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="e6428-223">AzureRM.Network</span></span>
* <span data-ttu-id="e6428-224">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="e6428-224">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="e6428-225">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="e6428-225">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="e6428-226">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="e6428-226">AzureRM.Resources</span></span>
* <span data-ttu-id="e6428-227">Мы устранили проблему, из-за которой командлет Get-AzureRMRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), и добавили понятное исключение.</span><span class="sxs-lookup"><span data-stu-id="e6428-227">Fix isssue where Get-AzureRMRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="e6428-228">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="e6428-228">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="6100---october-2018"></a><span data-ttu-id="e6428-229">6.10.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="e6428-229">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="e6428-230">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="e6428-230">Azure.Storage</span></span>
* <span data-ttu-id="e6428-231">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="e6428-231">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="e6428-232">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="e6428-232">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="e6428-233">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="e6428-233">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="e6428-234">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e6428-234">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="e6428-235">Поддержка Get-AzureRmCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="e6428-235">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="e6428-236">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="e6428-236">AzureRM.Compute</span></span>
* <span data-ttu-id="e6428-237">Исправлена команда Get-AzureRmVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов.</span><span class="sxs-lookup"><span data-stu-id="e6428-237">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="e6428-238">Добавлен пример использования SimpleParameterSet в справку командлета New-AzureRmVmss.</span><span class="sxs-lookup"><span data-stu-id="e6428-238">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="e6428-239">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="e6428-239">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="e6428-240">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e6428-240">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="e6428-241">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="e6428-241">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="e6428-242">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="e6428-242">AzureRM.Network</span></span>
* <span data-ttu-id="e6428-243">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="e6428-243">Added NetworkProfile functionality.</span></span> <span data-ttu-id="e6428-244">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="e6428-244">new cmdlets added</span></span>
    - <span data-ttu-id="e6428-245">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e6428-245">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="e6428-246">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e6428-246">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="e6428-247">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e6428-247">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="e6428-248">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e6428-248">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="e6428-249">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="e6428-249">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="e6428-250">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="e6428-250">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="e6428-251">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="e6428-251">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="e6428-252">Добавлены командлеты: New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap.</span><span class="sxs-lookup"><span data-stu-id="e6428-252">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="e6428-253">Добавлены командлеты: Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="e6428-253">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="e6428-254">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="e6428-254">AzureRM.RedisCache</span></span>
* <span data-ttu-id="e6428-255">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="e6428-255">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="e6428-256">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="e6428-256">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="e6428-257">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="e6428-257">AzureRM.Resources</span></span>
* <span data-ttu-id="e6428-258">Добавлен отсутствующий параметр -Mode в командлет Set-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="e6428-258">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="e6428-259">Исправлена ошибка командлета Get-AzureRmProviderOperation для операций, когда Origin содержит User.</span><span class="sxs-lookup"><span data-stu-id="e6428-259">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="e6428-260">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="e6428-260">AzureRM.Sql</span></span>
* <span data-ttu-id="e6428-261">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="e6428-261">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="e6428-262">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="e6428-262">AzureRM.Storage</span></span>
* <span data-ttu-id="e6428-263">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="e6428-263">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="e6428-264">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="e6428-264">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="e6428-265">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="e6428-265">AzureRM.Websites</span></span>
* <span data-ttu-id="e6428-266">Новый командлет Get-AzureRMWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера.</span><span class="sxs-lookup"><span data-stu-id="e6428-266">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="e6428-267">Новые командлеты New-AzureRMWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows.</span><span class="sxs-lookup"><span data-stu-id="e6428-267">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="e6428-268">6.9.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="e6428-268">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="e6428-269">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="e6428-269">General</span></span>
* <span data-ttu-id="e6428-270">В модуль развертывания AzureRM добавлен командлет AzureRM.SignalR.</span><span class="sxs-lookup"><span data-stu-id="e6428-270">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="e6428-271">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="e6428-271">AzureRM.Profile</span></span>
* <span data-ttu-id="e6428-272">Незначительные изменения в общем коде хранилища.</span><span class="sxs-lookup"><span data-stu-id="e6428-272">Minor changes to the storage common code</span></span>
* <span data-ttu-id="e6428-273">Обновлены файлы справки, в которые добавлены полные типы параметров.</span><span class="sxs-lookup"><span data-stu-id="e6428-273">Updated help files to include full parameter types.</span></span>
* <span data-ttu-id="e6428-274">В наборе параметров ServicePrincipalCertificateWithSubscriptionId параметр -ServicePrincipal теперь стал необязательным.</span><span class="sxs-lookup"><span data-stu-id="e6428-274">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="e6428-275">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="e6428-275">Azure.Storage</span></span>
* <span data-ttu-id="e6428-276">Поддержка создания контекста хранилища с использованием OAuth.</span><span class="sxs-lookup"><span data-stu-id="e6428-276">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="e6428-277">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="e6428-277">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="e6428-278">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="e6428-278">AzureRM.Cdn</span></span>
* <span data-ttu-id="e6428-279">Добавлен номер SKU для расценок на Standard_Microsoft в CDN.</span><span class="sxs-lookup"><span data-stu-id="e6428-279">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="e6428-280">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="e6428-280">AzureRM.Compute</span></span>
* <span data-ttu-id="e6428-281">Keyvault и Storage перенесены в общие зависимости.</span><span class="sxs-lookup"><span data-stu-id="e6428-281">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="e6428-282">Добавлена поддержка большего количества размеров виртуальных машин в командлеты AEM.</span><span class="sxs-lookup"><span data-stu-id="e6428-282">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="e6428-283">Добавлен параметр PublicIPPrefix в командлет New-AzureRmVmssIpConfig.</span><span class="sxs-lookup"><span data-stu-id="e6428-283">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="e6428-284">Добавлен параметр ResourceId в командлет Invoke-AzureRmVMRunCommand.</span><span class="sxs-lookup"><span data-stu-id="e6428-284">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="e6428-285">Добавлен командлет Invoke-AzureRmVmssVMRunCommand.</span><span class="sxs-lookup"><span data-stu-id="e6428-285">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="e6428-286">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="e6428-286">AzureRM.Dns</span></span>
* <span data-ttu-id="e6428-287">Добавлена поддержка для псевдонима записи во время создания записи DNS.</span><span class="sxs-lookup"><span data-stu-id="e6428-287">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="e6428-288">AzureRM.Insights;</span><span class="sxs-lookup"><span data-stu-id="e6428-288">AzureRM.Insights</span></span>
* <span data-ttu-id="e6428-289">Исправлены проблемы № 6833 и № 7102 (область настроек диагностики).</span><span class="sxs-lookup"><span data-stu-id="e6428-289">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="e6428-290">Проблемы с именем по умолчанию, например service, во время создания, получения и отображения списка параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="e6428-290">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="e6428-291">Проблемы при создании параметров диагностики с категориями.</span><span class="sxs-lookup"><span data-stu-id="e6428-291">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="e6428-292">Добавлено сообщение о том, что не рекомендуется использовать параметры интервалов времени в метриках.</span><span class="sxs-lookup"><span data-stu-id="e6428-292">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="e6428-293">Параметры интервалов времени по-прежнему принимаются (это не критическое изменение), но они игнорируются в серверной части, потому что действительно только значение PT1M.</span><span class="sxs-lookup"><span data-stu-id="e6428-293">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="e6428-294">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="e6428-294">AzureRM.Network</span></span>
* <span data-ttu-id="e6428-295">Изменения командлетов LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e6428-295">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="e6428-296">LoadBalancerInboundNatPoolConfig: добавлены параметры IdleTimeoutInMinutes, EnableFloatingIp и EnableTcpReset.</span><span class="sxs-lookup"><span data-stu-id="e6428-296">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="e6428-297">LoadBalancerInboundNatRuleConfig: добавлен параметр EnableTcpReset.</span><span class="sxs-lookup"><span data-stu-id="e6428-297">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="e6428-298">LoadBalancerRuleConfig: добавлен параметр EnableTcpReset.</span><span class="sxs-lookup"><span data-stu-id="e6428-298">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="e6428-299">LoadBalancerProbeConfig: добавлена поддержка значения Https для параметра Protocol.</span><span class="sxs-lookup"><span data-stu-id="e6428-299">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="e6428-300">Добавлены новые команды для нового правила OutboundRule подресурса LoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="e6428-300">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="e6428-301">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e6428-301">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="e6428-302">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e6428-302">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="e6428-303">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e6428-303">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="e6428-304">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e6428-304">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="e6428-305">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e6428-305">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="e6428-306">Добавлено новое свойство HostedWorkloads для PSNetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="e6428-306">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="e6428-307">Добавлены новые командлеты для функции Брандмауэра Azure через ARM.</span><span class="sxs-lookup"><span data-stu-id="e6428-307">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="e6428-308">Добавлен командлет Get-AzureRmFirewall.</span><span class="sxs-lookup"><span data-stu-id="e6428-308">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="e6428-309">Добавлен командлет Set-AzureRmFirewall.</span><span class="sxs-lookup"><span data-stu-id="e6428-309">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="e6428-310">Добавлен командлет New-AzureRmFirewall.</span><span class="sxs-lookup"><span data-stu-id="e6428-310">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="e6428-311">Добавлен командлет Remove-AzureRmFirewall.</span><span class="sxs-lookup"><span data-stu-id="e6428-311">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="e6428-312">Добавлен командлет New-AzureRmFirewallApplicationRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="e6428-312">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="e6428-313">Добавлен командлет New-AzureRmFirewallApplicationRule.</span><span class="sxs-lookup"><span data-stu-id="e6428-313">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="e6428-314">Добавлен командлет New-AzureRmFirewallNatRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="e6428-314">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="e6428-315">Добавлен командлет New-AzureRmFirewallNatRule.</span><span class="sxs-lookup"><span data-stu-id="e6428-315">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="e6428-316">Добавлен командлет New-AzureRmFirewallNetworkRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="e6428-316">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="e6428-317">Добавлен командлет New-AzureRmFirewallNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="e6428-317">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="e6428-318">Добавлена поддержка конфигурации для доверенного корневого сертификата и автомасштабирования в Шлюзе приложений.</span><span class="sxs-lookup"><span data-stu-id="e6428-318">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="e6428-319">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="e6428-319">New Cmdlets added:</span></span>
      - <span data-ttu-id="e6428-320">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e6428-320">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="e6428-321">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e6428-321">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="e6428-322">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e6428-322">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="e6428-323">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e6428-323">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="e6428-324">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e6428-324">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="e6428-325">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="e6428-325">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="e6428-326">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="e6428-326">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="e6428-327">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="e6428-327">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="e6428-328">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="e6428-328">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="e6428-329">В следующие командлеты добавлен необязательный параметр -TrustedRootCertificate:</span><span class="sxs-lookup"><span data-stu-id="e6428-329">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="e6428-330">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e6428-330">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="e6428-331">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e6428-331">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="e6428-332">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="e6428-332">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="e6428-333">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="e6428-333">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="e6428-334">В следующие командлеты добавлен необязательный параметр -AutoscaleConfiguration:</span><span class="sxs-lookup"><span data-stu-id="e6428-334">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="e6428-335">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e6428-335">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="e6428-336">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e6428-336">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="e6428-337">Добавлен командлет для конечной точки интерфейса Get-AzureInterfaceEndpoint.</span><span class="sxs-lookup"><span data-stu-id="e6428-337">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="e6428-338">Добавлена поддержка нескольких префиксов адресов в подсети.</span><span class="sxs-lookup"><span data-stu-id="e6428-338">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="e6428-339">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="e6428-339">Updated cmdlets:</span></span>
  - <span data-ttu-id="e6428-340">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e6428-340">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="e6428-341">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e6428-341">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="e6428-342">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e6428-342">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="e6428-343">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e6428-343">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="e6428-344">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="e6428-344">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="e6428-345">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="e6428-345">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="e6428-346">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="e6428-346">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="e6428-347">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="e6428-347">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="e6428-348">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e6428-348">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="e6428-349">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e6428-349">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="e6428-350">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e6428-350">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="e6428-351">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e6428-351">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="e6428-352">New-AzureRmNetworkInterfaceIpConfig — Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e6428-352">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="e6428-353">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="e6428-353">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="e6428-354">Add-AzureRmVirtualNetworkGatewayIpConfig;</span><span class="sxs-lookup"><span data-stu-id="e6428-354">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="e6428-355">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e6428-355">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="e6428-356">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e6428-356">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="e6428-357">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e6428-357">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="e6428-358">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e6428-358">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="e6428-359">Добавлены командлеты для делегирования подсети.</span><span class="sxs-lookup"><span data-stu-id="e6428-359">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="e6428-360">New-AzureRmDelegation — создает делегирование, которое можно добавить к подсети.</span><span class="sxs-lookup"><span data-stu-id="e6428-360">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="e6428-361">Remove-AzureRmDelegation — принимает подсеть и удаляет указанное имя делегирования из этой подсети.</span><span class="sxs-lookup"><span data-stu-id="e6428-361">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="e6428-362">Add-AzureRmDelegation — принимает подсеть и добавляет указанное имя службы в качестве делегирования для этой подсети.</span><span class="sxs-lookup"><span data-stu-id="e6428-362">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="e6428-363">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="e6428-363">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="e6428-364">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="e6428-364">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="e6428-365">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="e6428-365">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="e6428-366">Добавлена поддержка управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="e6428-366">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="e6428-367">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="e6428-367">AzureRM.RedisCache</span></span>
* <span data-ttu-id="e6428-368">Обновлена зависимость Insights.</span><span class="sxs-lookup"><span data-stu-id="e6428-368">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="e6428-369">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="e6428-369">AzureRM.Resources</span></span>
* <span data-ttu-id="e6428-370">В командлет New-AzureRmResourceGroupDeployment добавлен новый параметр RollbackAction.</span><span class="sxs-lookup"><span data-stu-id="e6428-370">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="e6428-371">Добавлена поддержка OnErrorDeployment с новым параметром.</span><span class="sxs-lookup"><span data-stu-id="e6428-371">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="e6428-372">Добавлена поддержка управляемого удостоверения при назначении политик.</span><span class="sxs-lookup"><span data-stu-id="e6428-372">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="e6428-373">При назначении политики с помощью New-AzureRmPolicyAssignment параметры со значениями по умолчанию больше не требуются.</span><span class="sxs-lookup"><span data-stu-id="e6428-373">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="e6428-374">Добавлен новый командлет Get-AzureRmPolicyAlias для получения псевдонимов политик.</span><span class="sxs-lookup"><span data-stu-id="e6428-374">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="e6428-375">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e6428-375">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="e6428-376">Устранена проблема № 7161.</span><span class="sxs-lookup"><span data-stu-id="e6428-376">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="e6428-377">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="e6428-377">AzureRM.SignalR</span></span>
* <span data-ttu-id="e6428-378">Обновлены номера SKU для Free_F1 и Standard_S1.</span><span class="sxs-lookup"><span data-stu-id="e6428-378">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="e6428-379">Добавлены поле версии в объект PSSignalRResource и строка подключения в объект PSSignalRKeys.</span><span class="sxs-lookup"><span data-stu-id="e6428-379">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="e6428-380">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="e6428-380">AzureRM.Storage</span></span>
* <span data-ttu-id="e6428-381">Добавлена поддержка политики неизменяемости в AzureRm.Storage.</span><span class="sxs-lookup"><span data-stu-id="e6428-381">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="e6428-382">Remove-AzureRmStorageAccountNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="e6428-382">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="e6428-383">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="e6428-383">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="e6428-384">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="e6428-384">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="e6428-385">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="e6428-385">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="e6428-386">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="e6428-386">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="e6428-387">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="e6428-387">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="e6428-388">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="e6428-388">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="e6428-389">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="e6428-389">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="e6428-390">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="e6428-390">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="e6428-391">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="e6428-391">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="e6428-392">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="e6428-392">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="e6428-393">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="e6428-393">AzureRM.Websites</span></span>
* <span data-ttu-id="e6428-394">Добавлены два новых командлета: Get-AzureRmDeletedWebApp и Restore-AzureRmDeletedWebApp.</span><span class="sxs-lookup"><span data-stu-id="e6428-394">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="e6428-395">New-AzureRmAppServicePlan: добавлен параметр -HyperV для создания плана службы приложений с контейнером Windows.</span><span class="sxs-lookup"><span data-stu-id="e6428-395">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="e6428-396">New-AzureRmWebApp, New-AzureRmWebAppSlot, Set-AzureRmWebApp, Set-AzureRmWebAppSlot: добавлены новые параметры (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) для создания контейнера приложения Windows и управления им.</span><span class="sxs-lookup"><span data-stu-id="e6428-396">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="e6428-397">6.8.1 — август 2018 г.</span><span class="sxs-lookup"><span data-stu-id="e6428-397">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="e6428-398">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="e6428-398">General</span></span>
* <span data-ttu-id="e6428-399">Исправлена проблема с отсутствием настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e6428-399">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="e6428-400">Обновлены общие сборки среды выполнения</span><span class="sxs-lookup"><span data-stu-id="e6428-400">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="e6428-401">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e6428-401">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="e6428-402">Исправлена проблема с отсутствием настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e6428-402">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="e6428-403">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6603.</span><span class="sxs-lookup"><span data-stu-id="e6428-403">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="e6428-404">Командлеты Import-AzureRmApiManagementApi и \*-AzureRmApiManagementCertificate теперь обрабатывают относительные пути.</span><span class="sxs-lookup"><span data-stu-id="e6428-404">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="e6428-405">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6879.</span><span class="sxs-lookup"><span data-stu-id="e6428-405">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="e6428-406">CertificateInformation — это задаваемое свойство, обеспечивающее правильную работу командлета Set-AzureRmApiManagement.</span><span class="sxs-lookup"><span data-stu-id="e6428-406">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="e6428-407">Проблема исправлена путем обновления пакета NuGet до версии 4.0.4-preview.</span><span class="sxs-lookup"><span data-stu-id="e6428-407">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="e6428-408">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6853.</span><span class="sxs-lookup"><span data-stu-id="e6428-408">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="e6428-409">Исправлен фильтр OData для поиска по имени продукта.</span><span class="sxs-lookup"><span data-stu-id="e6428-409">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="e6428-410">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6814.</span><span class="sxs-lookup"><span data-stu-id="e6428-410">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="e6428-411">Исправлен фильтр OData для поиска по имени API.</span><span class="sxs-lookup"><span data-stu-id="e6428-411">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="e6428-412">Добавлена поддержка средства ведения журнала Azure Monitor.</span><span class="sxs-lookup"><span data-stu-id="e6428-412">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="e6428-413">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="e6428-413">AzureRM.Compute</span></span>
* <span data-ttu-id="e6428-414">Исправлена проблема с отсутствием в выходных данных ошибки целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="e6428-414">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="e6428-415">Исправлена проблема с типом учетной записи хранения для виртуальной машины с управляемым диском.</span><span class="sxs-lookup"><span data-stu-id="e6428-415">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="e6428-416">Исправлена проблема с отсутствием настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e6428-416">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="e6428-417">Исправлены командлеты расширения AEM для других сред, например Azure для Китая.</span><span class="sxs-lookup"><span data-stu-id="e6428-417">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="e6428-418">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="e6428-418">AzureRM.Network</span></span>
* <span data-ttu-id="e6428-419">Стандартное представление выходных данных командлетов изменено на представление таблиц.</span><span class="sxs-lookup"><span data-stu-id="e6428-419">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="e6428-420">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="e6428-420">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="e6428-421">Исправлена проблема с Update-AzureRmPowerBIEmbeddedCapacity при попытке масштабировать приостановленную емкость.</span><span class="sxs-lookup"><span data-stu-id="e6428-421">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="e6428-422">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="e6428-422">AzureRM.Resources</span></span>
* <span data-ttu-id="e6428-423">Исправлена проблема с созданием управляемых приложений из Marketplace.</span><span class="sxs-lookup"><span data-stu-id="e6428-423">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="e6428-424">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e6428-424">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="e6428-425">Исправленные проблемы</span><span class="sxs-lookup"><span data-stu-id="e6428-425">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="e6428-426">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="e6428-426">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="e6428-427">Добавлена поддержка метода маршрутизации MultiValue.</span><span class="sxs-lookup"><span data-stu-id="e6428-427">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="e6428-428">Добавлен новый параметр MaxReturn для маршрутизации MultiValue.</span><span class="sxs-lookup"><span data-stu-id="e6428-428">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="e6428-429">Добавлена поддержка метода маршрутизации Subnet.</span><span class="sxs-lookup"><span data-stu-id="e6428-429">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="e6428-430">Добавлена поддержка диапазонов IP-адресов (подсетей) в конечных точках.</span><span class="sxs-lookup"><span data-stu-id="e6428-430">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="e6428-431">Добавлена поддержка пользовательских заголовков в профилях.</span><span class="sxs-lookup"><span data-stu-id="e6428-431">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="e6428-432">Добавлена поддержка диапазонов кода ожидаемого состояния в профилях.</span><span class="sxs-lookup"><span data-stu-id="e6428-432">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="e6428-433">Добавлена поддержка пользовательских заголовков в конечных точках.</span><span class="sxs-lookup"><span data-stu-id="e6428-433">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="e6428-434">6.8.0 — август 2018 г.</span><span class="sxs-lookup"><span data-stu-id="e6428-434">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="e6428-435">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="e6428-435">General</span></span>
* <span data-ttu-id="e6428-436">Исправлена проблема с отсутствием настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e6428-436">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="e6428-437">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="e6428-437">AzureRM.Profile</span></span>
* <span data-ttu-id="e6428-438">Добавлено свойство срока действия для маркеров, возвращенных при выполнении Connect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="e6428-438">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="e6428-439">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="e6428-439">AzureRM.Compute</span></span>
* <span data-ttu-id="e6428-440">Исправлена проблема с отсутствием в выходных данных ошибки целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="e6428-440">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="e6428-441">Исправлена проблема с типом учетной записи хранения для виртуальной машины с управляемым диском.</span><span class="sxs-lookup"><span data-stu-id="e6428-441">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="e6428-442">Исправлены командлеты расширения AEM для других сред, например Azure для Китая.</span><span class="sxs-lookup"><span data-stu-id="e6428-442">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="e6428-443">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="e6428-443">AzureRM.IotHub</span></span>
* <span data-ttu-id="e6428-444">Исправлены примеры для New-AzureRmIotHubExportDevices и New-AzureRmIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="e6428-444">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="e6428-445">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="e6428-445">AzureRM.Network</span></span>
* <span data-ttu-id="e6428-446">Изменено представление моделей по умолчанию на представление таблиц.</span><span class="sxs-lookup"><span data-stu-id="e6428-446">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="e6428-447">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="e6428-447">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="e6428-448">Исправлена проблема с Update-AzureRmPowerBIEmbeddedCapacity при попытке масштабировать приостановленную емкость.</span><span class="sxs-lookup"><span data-stu-id="e6428-448">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="e6428-449">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="e6428-449">AzureRM.Resources</span></span>
* <span data-ttu-id="e6428-450">Исправлена проблема с созданием управляемого приложения из marketplace.</span><span class="sxs-lookup"><span data-stu-id="e6428-450">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="e6428-451">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e6428-451">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="e6428-452">Исправления проблем</span><span class="sxs-lookup"><span data-stu-id="e6428-452">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="e6428-453">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="e6428-453">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="e6428-454">Добавлена поддержка метода маршрутизации MultiValue.</span><span class="sxs-lookup"><span data-stu-id="e6428-454">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="e6428-455">Добавлен новый параметр MaxReturn для маршрутизации MultiValue.</span><span class="sxs-lookup"><span data-stu-id="e6428-455">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="e6428-456">Добавлена поддержка метода маршрутизации Subnet.</span><span class="sxs-lookup"><span data-stu-id="e6428-456">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="e6428-457">Добавлена поддержка диапазонов IP-адресов (подсетей) в конечных точках.</span><span class="sxs-lookup"><span data-stu-id="e6428-457">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="e6428-458">Добавлена поддержка пользовательских заголовков в профилях.</span><span class="sxs-lookup"><span data-stu-id="e6428-458">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="e6428-459">Добавлена поддержка диапазонов кода состояния ожидания в профилях.</span><span class="sxs-lookup"><span data-stu-id="e6428-459">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="e6428-460">Добавлена поддержка пользовательских заголовков в конечных точках.</span><span class="sxs-lookup"><span data-stu-id="e6428-460">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="e6428-461">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="e6428-461">AzureRM.Websites</span></span>
* <span data-ttu-id="e6428-462">Исправлена проблема с отсутствием правильной настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e6428-462">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="e6428-463">6.7.0 — август 2018 г.</span><span class="sxs-lookup"><span data-stu-id="e6428-463">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="e6428-464">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="e6428-464">AzureRM.Profile</span></span>
* <span data-ttu-id="e6428-465">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-465">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="e6428-466">Добавлен идентификатор пользователя для имени контекста по умолчанию, чтобы избежать конфликтов контекста.</span><span class="sxs-lookup"><span data-stu-id="e6428-466">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="e6428-467">Устранены проблемы с командлетом Clear-AzureRmContext, которые приводили к проблемам с выбором контекста #6398.</span><span class="sxs-lookup"><span data-stu-id="e6428-467">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="e6428-468">Разрешено передавать домен клиента в параметр -TenantId для командлета Connect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="e6428-468">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="e6428-469">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="e6428-469">Azure.Storage</span></span>
* <span data-ttu-id="e6428-470">Удалено ограничение в 5 ТБ для квоты на общую папку Azure.</span><span class="sxs-lookup"><span data-stu-id="e6428-470">Remove the 5TB limitation for Azure File Share quota</span></span>
* <span data-ttu-id="e6428-471">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="e6428-471">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="e6428-472">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e6428-472">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="e6428-473">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-473">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="e6428-474">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e6428-474">Azure.AnalysisServices</span></span>
* <span data-ttu-id="e6428-475">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-475">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="e6428-476">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e6428-476">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="e6428-477">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-477">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="e6428-478">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="e6428-478">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="e6428-479">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-479">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="e6428-480">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="e6428-480">AzureRM.Automation</span></span>
* <span data-ttu-id="e6428-481">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-481">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="e6428-482">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="e6428-482">AzureRM.Backup</span></span>
* <span data-ttu-id="e6428-483">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-483">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="e6428-484">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="e6428-484">AzureRM.Batch</span></span>
* <span data-ttu-id="e6428-485">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-485">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="e6428-486">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="e6428-486">AzureRM.Billing</span></span>
* <span data-ttu-id="e6428-487">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-487">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="e6428-488">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="e6428-488">AzureRM.Cdn</span></span>
* <span data-ttu-id="e6428-489">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-489">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="e6428-490">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e6428-490">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="e6428-491">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-491">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="e6428-492">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="e6428-492">AzureRM.Compute</span></span>
* <span data-ttu-id="e6428-493">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-493">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="e6428-494">В командлет New-AzureRmVmssConfig добавлен параметр EvictionPolicy.</span><span class="sxs-lookup"><span data-stu-id="e6428-494">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="e6428-495">Если расположение не указано, используйте в DiskFileParameterSet для New AzureRmVm расположение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e6428-495">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="e6428-496">Исправлено описание параметров в Save-AzureRmVMImage.</span><span class="sxs-lookup"><span data-stu-id="e6428-496">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="e6428-497">Исправлен командлет Get-AzureRmVMDiskEncryptionStatus для определенных сценариев, связанных с однократным выполнением.</span><span class="sxs-lookup"><span data-stu-id="e6428-497">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="e6428-498">AzureRM.Consumption:</span><span class="sxs-lookup"><span data-stu-id="e6428-498">AzureRM.Consumption</span></span>
* <span data-ttu-id="e6428-499">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-499">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="e6428-500">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e6428-500">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="e6428-501">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-501">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="e6428-502">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e6428-502">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="e6428-503">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-503">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="e6428-504">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="e6428-504">AzureRM.DataFactories</span></span>
* <span data-ttu-id="e6428-505">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-505">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="e6428-506">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e6428-506">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="e6428-507">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-507">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="e6428-508">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="e6428-508">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="e6428-509">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-509">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="e6428-510">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e6428-510">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="e6428-511">Исправлена отладка, когда DebugPreference настраивается из командной строки PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e6428-511">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="e6428-512">Обновлен пример для Set-AzureRmDataLakeStoreItemAcl.</span><span class="sxs-lookup"><span data-stu-id="e6428-512">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="e6428-513">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-513">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="e6428-514">Обновлен пример для Set-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="e6428-514">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="e6428-515">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="e6428-515">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="e6428-516">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-516">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="e6428-517">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="e6428-517">AzureRM.Dns</span></span>
* <span data-ttu-id="e6428-518">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-518">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="e6428-519">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e6428-519">AzureRM.EventGrid</span></span>
* <span data-ttu-id="e6428-520">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-520">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="e6428-521">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="e6428-521">AzureRM.EventHub</span></span>
* <span data-ttu-id="e6428-522">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-522">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="e6428-523">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e6428-523">AzureRM.HDInsight</span></span>
* <span data-ttu-id="e6428-524">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-524">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="e6428-525">AzureRM.Insights;</span><span class="sxs-lookup"><span data-stu-id="e6428-525">AzureRM.Insights</span></span>
* <span data-ttu-id="e6428-526">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-526">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="e6428-527">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="e6428-527">AzureRM.IotHub</span></span>
* <span data-ttu-id="e6428-528">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-528">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="e6428-529">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e6428-529">AzureRM.KeyVault</span></span>
* <span data-ttu-id="e6428-530">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-530">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="e6428-531">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e6428-531">AzureRM.LogicApp</span></span>
* <span data-ttu-id="e6428-532">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-532">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="e6428-533">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="e6428-533">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="e6428-534">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-534">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="e6428-535">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="e6428-535">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="e6428-536">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-536">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="e6428-537">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="e6428-537">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="e6428-538">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-538">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="e6428-539">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="e6428-539">AzureRM.Media</span></span>
* <span data-ttu-id="e6428-540">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-540">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="e6428-541">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="e6428-541">AzureRM.Network</span></span>
* <span data-ttu-id="e6428-542">Добавлен пример для Set-AzureRmLocalNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="e6428-542">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="e6428-543">Добавлены примеры и описания для Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey и New-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="e6428-543">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="e6428-544">Добавлены примеры для Remove-AzureRmVirtualNetworkGatewayIpConfig и Reset-AzureRmVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="e6428-544">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="e6428-545">Добавлен пример для Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.</span><span class="sxs-lookup"><span data-stu-id="e6428-545">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="e6428-546">Добавлен пример для Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.</span><span class="sxs-lookup"><span data-stu-id="e6428-546">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="e6428-547">Добавлен пример для Set-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="e6428-547">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="e6428-548">Повторно созданы командлеты для ApplicationSecurityGroup, RouteTable и Usage с помощью генератора кода последней версии.</span><span class="sxs-lookup"><span data-stu-id="e6428-548">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="e6428-549">Уточнено сообщение об ошибке для Get-AzureRmVirtualNetworkSubnetConfig при попытке получить подсеть, которая не существует.</span><span class="sxs-lookup"><span data-stu-id="e6428-549">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="e6428-550">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="e6428-550">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="e6428-551">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-551">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="e6428-552">AzureRM.OperationalInsights;</span><span class="sxs-lookup"><span data-stu-id="e6428-552">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="e6428-553">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-553">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="e6428-554">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e6428-554">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="e6428-555">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-555">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="e6428-556">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="e6428-556">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="e6428-557">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-557">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="e6428-558">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e6428-558">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="e6428-559">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-559">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="e6428-560">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="e6428-560">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="e6428-561">Добавлен фильтр политик для командлета Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="e6428-561">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="e6428-562">Команда возвращает список элементов резервного копирования, защищенных политикой с заданным идентификатором.</span><span class="sxs-lookup"><span data-stu-id="e6428-562">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="e6428-563">Обновление Microsoft.Azure.Management.RecoveryServices.Backup до версии 3.0.0-preview.</span><span class="sxs-lookup"><span data-stu-id="e6428-563">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="e6428-564">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-564">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="e6428-565">Добавлен параметр TargetResourceGroupName для Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="e6428-565">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="e6428-566">Группа ресурсов, в которую восстанавливаются управляемые диски.</span><span class="sxs-lookup"><span data-stu-id="e6428-566">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="e6428-567">Применимо к резервной копии виртуальной машины с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="e6428-567">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="e6428-568">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="e6428-568">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="e6428-569">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-569">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="e6428-570">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="e6428-570">AzureRM.RedisCache</span></span>
* <span data-ttu-id="e6428-571">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-571">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="e6428-572">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="e6428-572">AzureRM.Relay</span></span>
* <span data-ttu-id="e6428-573">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-573">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="e6428-574">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="e6428-574">AzureRM.Resources</span></span>
* <span data-ttu-id="e6428-575">Поддержка развертывания шаблонов в области подписки.</span><span class="sxs-lookup"><span data-stu-id="e6428-575">Support template deployment at subscription scope.</span></span> <span data-ttu-id="e6428-576">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="e6428-576">Add new Cmdlets:</span></span>
    - <span data-ttu-id="e6428-577">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="e6428-577">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="e6428-578">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="e6428-578">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="e6428-579">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="e6428-579">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="e6428-580">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="e6428-580">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="e6428-581">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="e6428-581">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="e6428-582">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="e6428-582">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="e6428-583">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="e6428-583">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="e6428-584">Устранена проблема, когда при передаче контекста в Set-AzureRmResource возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="e6428-584">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="e6428-585">Исправлен пример в New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="e6428-585">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="e6428-586">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-586">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="e6428-587">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="e6428-587">AzureRM.Scheduler</span></span>
* <span data-ttu-id="e6428-588">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-588">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="e6428-589">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e6428-589">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="e6428-590">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-590">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="e6428-591">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e6428-591">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="e6428-592">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-592">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="e6428-593">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="e6428-593">AzureRM.Sql</span></span>
* <span data-ttu-id="e6428-594">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-594">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="e6428-595">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="e6428-595">AzureRM.Storage</span></span>
* <span data-ttu-id="e6428-596">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-596">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="e6428-597">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="e6428-597">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="e6428-598">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-598">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="e6428-599">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="e6428-599">AzureRM.Tags</span></span>
* <span data-ttu-id="e6428-600">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-600">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="e6428-601">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="e6428-601">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="e6428-602">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-602">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="e6428-603">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="e6428-603">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="e6428-604">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-604">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="e6428-605">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="e6428-605">AzureRM.Websites</span></span>
* <span data-ttu-id="e6428-606">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-606">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="e6428-607">6.6.0 — июль 2018 г.</span><span class="sxs-lookup"><span data-stu-id="e6428-607">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="e6428-608">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="e6428-608">General</span></span>
* <span data-ttu-id="e6428-609">Обновлены все файлы справки: включены полные типы параметров и исправлены типы входных и выходных данных.</span><span class="sxs-lookup"><span data-stu-id="e6428-609">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="e6428-610">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="e6428-610">AzureRM.Profile</span></span>
* <span data-ttu-id="e6428-611">Обновлена библиотека Common.Strategy: теперь можно проверить, совместима ли текущая конфигурация ресурса с целевым ресурсом.</span><span class="sxs-lookup"><span data-stu-id="e6428-611">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="e6428-612">В Common.Storage добавлены типы ps1xml.</span><span class="sxs-lookup"><span data-stu-id="e6428-612">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="e6428-613">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="e6428-613">Azure.Storage</span></span>
* <span data-ttu-id="e6428-614">Добавлена поддержка для получения контекста хранилища из DefaultProfile.</span><span class="sxs-lookup"><span data-stu-id="e6428-614">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="e6428-615">В свойства типов выходных данных командлетов добавлен атрибут Ps1XmlAttribute.</span><span class="sxs-lookup"><span data-stu-id="e6428-615">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="e6428-616">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e6428-616">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="e6428-617">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6370.</span><span class="sxs-lookup"><span data-stu-id="e6428-617">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="e6428-618">В AutoMapper исправлена ошибка, препятствовавшая преобразованию PsApiManagementApi в ApiContract.</span><span class="sxs-lookup"><span data-stu-id="e6428-618">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="e6428-619">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6515.</span><span class="sxs-lookup"><span data-stu-id="e6428-619">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="e6428-620">В File.Save исправлена ошибка, связанная с перегрузкой типом кодировки.</span><span class="sxs-lookup"><span data-stu-id="e6428-620">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="e6428-621">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6560.</span><span class="sxs-lookup"><span data-stu-id="e6428-621">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="e6428-622">Выполнено обновление до версии NuGet 4.0.3, что позволило исправить исключение шаблона в apiId.</span><span class="sxs-lookup"><span data-stu-id="e6428-622">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="e6428-623">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="e6428-623">AzureRM.Compute</span></span>
* <span data-ttu-id="e6428-624">Устранена ошибка при создании виртуальной машины с помощью командлета New-AzureRmVm и параметра DiskFileParameterSet, которая возникала из-за переименования типа учетной записи хранения PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="e6428-624">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="e6428-625">Исправлен командлет Invoke-AzureRmVMRunCommand.</span><span class="sxs-lookup"><span data-stu-id="e6428-625">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="e6428-626">Командлет Get-AzureRmAvailabilitySet теперь может выводить список всех групп доступности в подписке.</span><span class="sxs-lookup"><span data-stu-id="e6428-626">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="e6428-627">(Параметр ResouceGroupName теперь является необязательным.)</span><span class="sxs-lookup"><span data-stu-id="e6428-627">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="e6428-628">Обновлен параметр SimpleParameterSet командлета New-AzureRmVm, что позволило использовать ускоренную сеть на соответствующих виртуальных машинах.</span><span class="sxs-lookup"><span data-stu-id="e6428-628">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="e6428-629">Обновлен простой набор параметров New-AzureRmVmss, что позволило отменять создание масштабируемого набора виртуальных машин, если указанная пользователем подсистема балансировки нагрузки уже существует.</span><span class="sxs-lookup"><span data-stu-id="e6428-629">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="e6428-630">Обновлен пример для New-AzureRmDisk.</span><span class="sxs-lookup"><span data-stu-id="e6428-630">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="e6428-631">Добавлен пример для New-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="e6428-631">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="e6428-632">Обновлено описание командлета Set-AzureRmVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="e6428-632">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="e6428-633">Обновлен пример 1 для Set-AzureRmVMBginfoExtension: исправлены орфографические ошибки и префикс.</span><span class="sxs-lookup"><span data-stu-id="e6428-633">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="e6428-634">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e6428-634">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="e6428-635">Пакет .NET SDK для ADF обновлен до версии 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="e6428-635">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="e6428-636">Добавлена поддержка совместного использования локальной среды IR несколькими фабриками данных.</span><span class="sxs-lookup"><span data-stu-id="e6428-636">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="e6428-637">Добавлен новый параметр -SharedIntegrationRuntimeResourceId для командлета Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-637">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="e6428-638">Добавлен новый необязательный параметр -LinkedDataFactoryName для командлета Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="e6428-638">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="e6428-639">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e6428-639">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="e6428-640">Пакет SDK для плоскости данных (Microsoft.Azure.DataLake.Store) обновлен до версии 1.1.9.</span><span class="sxs-lookup"><span data-stu-id="e6428-640">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="e6428-641">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="e6428-641">AzureRM.EventHub</span></span>
* <span data-ttu-id="e6428-642">Обновлена конвейерная передача для InputObject и ResourceId в командлетах remove.</span><span class="sxs-lookup"><span data-stu-id="e6428-642">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="e6428-643">AzureRM.Insights;</span><span class="sxs-lookup"><span data-stu-id="e6428-643">AzureRM.Insights</span></span>
* <span data-ttu-id="e6428-644">Исправлено форматирование OutputType в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="e6428-644">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="e6428-645">Применен пакет SDK Microsoft.Azure.Management.Monitor 0.19.1-preview.</span><span class="sxs-lookup"><span data-stu-id="e6428-645">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="e6428-646">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e6428-646">AzureRM.KeyVault</span></span>
* <span data-ttu-id="e6428-647">Исправлена проблема с конвейерной передачей в командлете Set-AzureRmKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="e6428-647">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="e6428-648">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="e6428-648">AzureRM.Network</span></span>
* <span data-ttu-id="e6428-649">Добавлены примеры для командлетов LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="e6428-649">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="e6428-650">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="e6428-650">AzureRM.Resources</span></span>
* <span data-ttu-id="e6428-651">Устранена проблема, возникавшая при указании имени и значения тега для Get-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="e6428-651">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="e6428-652">Исправлен сценарий конвейерной передачи в Set-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="e6428-652">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="e6428-653">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e6428-653">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="e6428-654">Обновлена конвейерная передача для InputObject и ResourceId в командлетах remove.</span><span class="sxs-lookup"><span data-stu-id="e6428-654">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="e6428-655">Исправлено несколько ошибок.</span><span class="sxs-lookup"><span data-stu-id="e6428-655">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="e6428-656">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="e6428-656">AzureRM.Sql</span></span>
* <span data-ttu-id="e6428-657">Добавлена поддержка Advanced Threat Protection для сервера с помощью следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="e6428-657">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="e6428-658">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="e6428-658">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="e6428-659">Добавлена поддержка оценки уязвимостей с помощью следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="e6428-659">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="e6428-660">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings;</span><span class="sxs-lookup"><span data-stu-id="e6428-660">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="e6428-661">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline;</span><span class="sxs-lookup"><span data-stu-id="e6428-661">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="e6428-662">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan.</span><span class="sxs-lookup"><span data-stu-id="e6428-662">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="e6428-663">Исправлен пример для Remove-AzureRmSqlServerFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="e6428-663">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="e6428-664">Исправлена неправильная обработка даты и времени для базового языка и региональных параметров, отличных от США, в Get-AzureSqlSyncGroupLog.</span><span class="sxs-lookup"><span data-stu-id="e6428-664">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="e6428-665">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="e6428-665">AzureRM.Storage</span></span>
* <span data-ttu-id="e6428-666">В свойства типов выходных данных командлетов добавлен атрибут Ps1XmlAttribute.</span><span class="sxs-lookup"><span data-stu-id="e6428-666">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="e6428-667">Выходные данные командлетов StorageAccount теперь отображаются в виде таблицы.</span><span class="sxs-lookup"><span data-stu-id="e6428-667">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="e6428-668">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e6428-668">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="e6428-669">New-AzureRmStorageAccount;</span><span class="sxs-lookup"><span data-stu-id="e6428-669">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="e6428-670">Set-AzureRmStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="e6428-670">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="e6428-671">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="e6428-671">AzureRM.Tags</span></span>
* <span data-ttu-id="e6428-672">Удалено неверное утверждение из справки по командлетам Tag.</span><span class="sxs-lookup"><span data-stu-id="e6428-672">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="e6428-673">6.5.0 — июль 2018 г.</span><span class="sxs-lookup"><span data-stu-id="e6428-673">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="e6428-674">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="e6428-674">AzureRM.Profile</span></span>
* <span data-ttu-id="e6428-675">Обновлена справка для командлета Get-AzureRmContextAutosaveSetting.</span><span class="sxs-lookup"><span data-stu-id="e6428-675">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="e6428-676">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="e6428-676">Azure.Storage</span></span>
* <span data-ttu-id="e6428-677">Добавлена поддержка отправки BLOB-объекта или файла с помощью токена SAS, доступного только для записи.</span><span class="sxs-lookup"><span data-stu-id="e6428-677">Support Upload Blob or File with write only Sas token</span></span>
* <span data-ttu-id="e6428-678">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e6428-678">Set-AzureStorageBlobContent</span></span>
* <span data-ttu-id="e6428-679">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e6428-679">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="e6428-680">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e6428-680">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="e6428-681">Для AS добавлено обязательное свойство ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="e6428-681">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="e6428-682">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="e6428-682">AzureRM.Automation</span></span>
* <span data-ttu-id="e6428-683">Обновлена справка и добавлены примеры для командлета New-AzureRMAutomationSchedule.</span><span class="sxs-lookup"><span data-stu-id="e6428-683">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="e6428-684">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="e6428-684">AzureRM.Compute</span></span>
* <span data-ttu-id="e6428-685">Добавлен параметр -Tag для командлета Update/New-AzureRmAvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="e6428-685">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="e6428-686">Добавлен пример для командлета Add-AzureRmVmssExtension.</span><span class="sxs-lookup"><span data-stu-id="e6428-686">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="e6428-687">Добавлены примеры для командлета Remove-AzureRmVmssExtension.</span><span class="sxs-lookup"><span data-stu-id="e6428-687">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="e6428-688">Обновлена справка для командлета Set-AzureRmVMAccessExtension.</span><span class="sxs-lookup"><span data-stu-id="e6428-688">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="e6428-689">Изменен класс SimpleParameterSet для командлета New-AzureRmVmss: теперь для SinglePlacementGroup по умолчанию задается значение false, а также добавляется параметр-переключатель SinglePlacementGroup, который позволяет пользователю создать VMSS в одной группе размещения.</span><span class="sxs-lookup"><span data-stu-id="e6428-689">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="e6428-690">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="e6428-690">AzureRM.EventHub</span></span>
* <span data-ttu-id="e6428-691">В класс PSEventHubDRConfigurationAttributes добавлено доступное только для чтения свойство PendingReplicationOperationsCount, которое показывает количество ожидающих репликации операций во время реплицирования.</span><span class="sxs-lookup"><span data-stu-id="e6428-691">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="e6428-692">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e6428-692">AzureRM.KeyVault</span></span>
* <span data-ttu-id="e6428-693">Обновлено сообщение об ошибке для командлета Set-AzureRmKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="e6428-693">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="e6428-694">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e6428-694">AzureRM.LogicApp</span></span>
* <span data-ttu-id="e6428-695">Исправлена ошибка "parameter set could not be resolved" (не удалось разрешить заданный параметр) в командлете New-AzureRmLogicApp.</span><span class="sxs-lookup"><span data-stu-id="e6428-695">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="e6428-696">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="e6428-696">AzureRM.Network</span></span>
* <span data-ttu-id="e6428-697">Включен пиринг между виртуальными сетями в нескольких клиентах для командлета Set/Add-AzureRmVirtualNetworkPeering.</span><span class="sxs-lookup"><span data-stu-id="e6428-697">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="e6428-698">Для шлюза приложений обновлены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="e6428-698">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="e6428-699">New-AzureRmApplicationGateway: добавлены флаг EnableFIPS и поддержка зон.</span><span class="sxs-lookup"><span data-stu-id="e6428-699">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="e6428-700">New-AzureRmApplicationGatewaySku: добавлены новые номера SKU Standard_v2 и WAF_v2.</span><span class="sxs-lookup"><span data-stu-id="e6428-700">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="e6428-701">Set-AzureRmApplicationGatewaySku: добавлены новые номера SKU Standard_v2 и WAF_v2.</span><span class="sxs-lookup"><span data-stu-id="e6428-701">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="e6428-702">Командлеты RouteTable пересозданы в последней версии генератора.</span><span class="sxs-lookup"><span data-stu-id="e6428-702">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="e6428-703">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="e6428-703">AzureRM.Relay</span></span>
* <span data-ttu-id="e6428-704">Обновлены файлы Markdown, исправлена проблема с именем параметра в примере.</span><span class="sxs-lookup"><span data-stu-id="e6428-704">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="e6428-705">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="e6428-705">AzureRM.Resources</span></span>
* <span data-ttu-id="e6428-706">Обновлены командлеты Roleassignment и roledefinition:</span><span class="sxs-lookup"><span data-stu-id="e6428-706">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="e6428-707">Удалены лишние вызовы roledefinition, выполняемые в ходе разбиения на страницы.</span><span class="sxs-lookup"><span data-stu-id="e6428-707">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="e6428-708">Исправлен командлет Get-AzureRmRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="e6428-708">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="e6428-709">Исправлена работа параметра -ExpandPrincipalGroups.</span><span class="sxs-lookup"><span data-stu-id="e6428-709">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="e6428-710">Устранена проблема в командлете Get-AzureRmResource, заключающая в том, что в параметре -ResourceType учитывался регистр символов.</span><span class="sxs-lookup"><span data-stu-id="e6428-710">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="e6428-711">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e6428-711">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="e6428-712">Добавлены параметры top и skip для командлетов list.</span><span class="sxs-lookup"><span data-stu-id="e6428-712">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="e6428-713">Добавлены командлеты для перехода с пространства имен ценовой категории "Стандартный" на пространство ценовой категории "Премиум":</span><span class="sxs-lookup"><span data-stu-id="e6428-713">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="e6428-714">Start-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="e6428-714">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="e6428-715">Get-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="e6428-715">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="e6428-716">Complete-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="e6428-716">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="e6428-717">Stop-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="e6428-717">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="e6428-718">Remove-AzureRmServiceBusMigration.</span><span class="sxs-lookup"><span data-stu-id="e6428-718">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="e6428-719">В класс PSServiceBusDRConfigurationAttributes добавлено доступное только для чтения свойство PendingReplicationOperationsCount, которое показывает количество ожидающих репликации операций во время реплицирования.</span><span class="sxs-lookup"><span data-stu-id="e6428-719">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="e6428-720">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e6428-720">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="e6428-721">Обновлен пример для командлета New-AzureRmServiceFabricCluster.</span><span class="sxs-lookup"><span data-stu-id="e6428-721">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="e6428-722">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="e6428-722">AzureRM.Sql</span></span>
* <span data-ttu-id="e6428-723">Добавлены новые командлеты для Management.Sql, позволяющие клиентам добавлять сертификат TDE в экземпляр SQL Server или управляемый экземпляр:</span><span class="sxs-lookup"><span data-stu-id="e6428-723">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="e6428-724">Add-AzureRmSqlServerTransparentDataEncryptionCertificate;</span><span class="sxs-lookup"><span data-stu-id="e6428-724">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="e6428-725">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate.</span><span class="sxs-lookup"><span data-stu-id="e6428-725">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="e6428-726">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="e6428-726">AzureRM.Websites</span></span>
* <span data-ttu-id="e6428-727">`Set-AzureRmWebApp -AssignIdentity` и `Set-AzureRmWebAppSlot -AssignIdentity` при установленном значении false теперь будут удалять свойство Identity из объекта сайта. Также при этом будет удаляться тег предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="e6428-727">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="e6428-728">Обновлен пример для `Get-AzureRmWebAppMetrics` и `Get-AzureRmAppServicePlanMetrics`.</span><span class="sxs-lookup"><span data-stu-id="e6428-728">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="e6428-729">`Set-AzureRmWebApp -PhpVersion` теперь поддерживает off как допустимую версию PHP.</span><span class="sxs-lookup"><span data-stu-id="e6428-729">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="e6428-730">6.4.0 — июль 2018 г.</span><span class="sxs-lookup"><span data-stu-id="e6428-730">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="e6428-731">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="e6428-731">General</span></span>
* <span data-ttu-id="e6428-732">Исправлено форматирование OutputType в файлах справки для большинства модулей.</span><span class="sxs-lookup"><span data-stu-id="e6428-732">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="e6428-733">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="e6428-733">AzureRM.Profile</span></span>
* <span data-ttu-id="e6428-734">В основные типы выходных данных добавлен атрибут Ps1Xml.</span><span class="sxs-lookup"><span data-stu-id="e6428-734">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="e6428-735">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="e6428-735">AzureRM.Compute</span></span>
* <span data-ttu-id="e6428-736">Функция добавления тега IP-адреса для масштабируемого набора виртуальных машин (VMSS)</span><span class="sxs-lookup"><span data-stu-id="e6428-736">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="e6428-737">Добавлен командлет New-AzureRmVmssIpTagConfig.</span><span class="sxs-lookup"><span data-stu-id="e6428-737">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="e6428-738">В New-AzureRmVmssIpConfig добавлен параметр IpTag.</span><span class="sxs-lookup"><span data-stu-id="e6428-738">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="e6428-739">Функция автоматического отката ОС для VMSS</span><span class="sxs-lookup"><span data-stu-id="e6428-739">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="e6428-740">В New-AzureRmVmssConfig и Update-AzureRmVmss добавлены параметры DisableAutoRollback.</span><span class="sxs-lookup"><span data-stu-id="e6428-740">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="e6428-741">Функция ведения журнала обновлений ОС для VMSS</span><span class="sxs-lookup"><span data-stu-id="e6428-741">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="e6428-742">В Get-AzureRmVmss добавлен параметр OSUpgradeHistory.</span><span class="sxs-lookup"><span data-stu-id="e6428-742">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="e6428-743">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="e6428-743">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="e6428-744">Добавлена поддержка списков управления доступом к каталогу с использованием следующих команд:</span><span class="sxs-lookup"><span data-stu-id="e6428-744">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="e6428-745">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry;</span><span class="sxs-lookup"><span data-stu-id="e6428-745">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="e6428-746">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry;</span><span class="sxs-lookup"><span data-stu-id="e6428-746">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="e6428-747">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="e6428-747">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="e6428-748">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e6428-748">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="e6428-749">Добавлены поддержка отмены выполнения и отслеживание хода выполнения для Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl и Remove-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="e6428-749">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="e6428-750">Добавлена поддержка отмены выполнения для Export-AzureRmDataLakeStoreChildItemProperties.</span><span class="sxs-lookup"><span data-stu-id="e6428-750">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="e6428-751">Исправлена очистка сообщений об отладке для командлетов, которые выполняют рекурсивные операции.</span><span class="sxs-lookup"><span data-stu-id="e6428-751">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="e6428-752">Исправлено расположение тестовых данных для командлетов DataLake.</span><span class="sxs-lookup"><span data-stu-id="e6428-752">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="e6428-753">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="e6428-753">AzureRM.EventHub</span></span>
* <span data-ttu-id="e6428-754">Для командлетов вывода списка операций Get-AzureRmEventHub и Get-AzureRmEventHubConsumerGroup добавлен необязательный параметр MaxCount.</span><span class="sxs-lookup"><span data-stu-id="e6428-754">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="e6428-755">Исправлена проблема с командлетом New-AzureRmEventHub, из-за которой требовалось указать по крайней мере один параметр при создании концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="e6428-755">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="e6428-756">Добавлен набор параметров по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e6428-756">Provided Default Parameter set.</span></span>
* <span data-ttu-id="e6428-757">Для командлета New-AzureRmEventHubKey добавлен необязательный параметр -KeyValue, который позволяет пользователю предоставить значение ключа.</span><span class="sxs-lookup"><span data-stu-id="e6428-757">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="e6428-758">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e6428-758">AzureRM.KeyVault</span></span>
* <span data-ttu-id="e6428-759">Исправлена ошибка, из-за которой при выполнении командлета Get-AzureRmKeyVault с параметром -Tag возвращались все ресурсы.</span><span class="sxs-lookup"><span data-stu-id="e6428-759">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="e6428-760">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="e6428-760">AzureRM.Network</span></span>
* <span data-ttu-id="e6428-761">Для параметра шлюзов виртуальной вести, избыточных между зонами, предоставлены новые номера SKU.</span><span class="sxs-lookup"><span data-stu-id="e6428-761">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="e6428-762">Добавлены новые команды для функции поддержки партнерских API для ExpressRoute, развертываемых с помощью ARM:</span><span class="sxs-lookup"><span data-stu-id="e6428-762">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="e6428-763">добавлена команда Get-AzureRmExpressRouteCrossConnection;</span><span class="sxs-lookup"><span data-stu-id="e6428-763">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="e6428-764">добавлена команда Set-AzureRmExpressRouteCrossConnection;</span><span class="sxs-lookup"><span data-stu-id="e6428-764">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="e6428-765">добавлена команда Add-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="e6428-765">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="e6428-766">добавлена команда Get-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="e6428-766">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="e6428-767">добавлена команда Remove-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="e6428-767">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="e6428-768">добавлена команда Get-AzureRMExpressRouteCrossConnectionArpTable;</span><span class="sxs-lookup"><span data-stu-id="e6428-768">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="e6428-769">добавлена команда Get-AzureRMExpressRouteCrossConnectionRouteTable;</span><span class="sxs-lookup"><span data-stu-id="e6428-769">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="e6428-770">добавлена команда Get-AzureRMExpressRouteCrossConnectionRouteTableSummary.</span><span class="sxs-lookup"><span data-stu-id="e6428-770">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="e6428-771">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="e6428-771">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="e6428-772">Добавлен командлет Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="e6428-772">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="e6428-773">Этот командлет принимает идентификатор виртуальной машины и проверяет, защищена ли виртуальная машина с помощью какого-либо хранилища в подписке.</span><span class="sxs-lookup"><span data-stu-id="e6428-773">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="e6428-774">Если такое хранилище существует, командлет выводит данные о нем.</span><span class="sxs-lookup"><span data-stu-id="e6428-774">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="e6428-775">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="e6428-775">AzureRM.Resources</span></span>
* <span data-ttu-id="e6428-776">Обновлены командлеты Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="e6428-776">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="e6428-777">Добавлена поддержка вывода списка значений параметра -Scope на уровне группы управления.</span><span class="sxs-lookup"><span data-stu-id="e6428-777">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="e6428-778">Добавлена поддержка для получения отдельных назначений со значениями -Scope на уровне группы управления.</span><span class="sxs-lookup"><span data-stu-id="e6428-778">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="e6428-779">Для параметра управления добавлены параметры -Effective и -All.</span><span class="sxs-lookup"><span data-stu-id="e6428-779">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="e6428-780">Обновлены командлеты Get/New/Remove/Set-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="e6428-780">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="e6428-781">Добавлен параметр -ManagementGroupName для применения операций к заданной группе управления.</span><span class="sxs-lookup"><span data-stu-id="e6428-781">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="e6428-782">Добавлен параметр -SubscriptionId для применения операций к заданной подписке.</span><span class="sxs-lookup"><span data-stu-id="e6428-782">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="e6428-783">Обновлены командлеты Get/New/Remove/Set-AzureRmPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="e6428-783">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="e6428-784">Добавлен параметр -ManagementGroupName для применения операций к заданной группе управления.</span><span class="sxs-lookup"><span data-stu-id="e6428-784">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="e6428-785">Добавлен параметр -SubscriptionId для применения операций к заданной подписке.</span><span class="sxs-lookup"><span data-stu-id="e6428-785">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="e6428-786">Добавлена поддержка ссылок на секрет KeyVault в параметрах при использовании TemplateParameterObject в New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="e6428-786">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="e6428-787">Устранена проблема, из-за которой параметр -EndDate игнорировался в New-AzureRmADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="e6428-787">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="e6428-788">Устранена проблема, из-за которой в Add-AzureRmADGroupMember использовался неверный URL-адрес для запроса.</span><span class="sxs-lookup"><span data-stu-id="e6428-788">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="e6428-789">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e6428-789">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="e6428-790">Для командлета New-AzureRmServiceBusKey добавлен необязательный параметр -KeyValue, который позволяет пользователю предоставить значение ключа.</span><span class="sxs-lookup"><span data-stu-id="e6428-790">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="e6428-791">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="e6428-791">AzureRM.Sql</span></span>
* <span data-ttu-id="e6428-792">В справке по New-AzureRmSqlDatabaseRestorePoint добавлено описание определяемых пользователем точек восстановления для хранилища данных SQL.</span><span class="sxs-lookup"><span data-stu-id="e6428-792">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="e6428-793">Обновлена документация по параметру -ComputeGeneration, используемого в нескольких командлетах.</span><span class="sxs-lookup"><span data-stu-id="e6428-793">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="e6428-794">6.3.0 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="e6428-794">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="e6428-795">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="e6428-795">AzureRM.Profile</span></span>
* <span data-ttu-id="e6428-796">Обновлены сообщения об ошибках для Enable-AzureRmContextAutoSave.</span><span class="sxs-lookup"><span data-stu-id="e6428-796">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="e6428-797">Создание контекста для каждой подписки при выполнении Connect-AzureRmAccount без предыдущего контекста.</span><span class="sxs-lookup"><span data-stu-id="e6428-797">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="e6428-798">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="e6428-798">Azure.Storage</span></span>
* <span data-ttu-id="e6428-799">В файлы справки добавлены дополнительные сведения о параметре -Permissions.</span><span class="sxs-lookup"><span data-stu-id="e6428-799">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="e6428-800">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="e6428-800">AzureRM.Compute</span></span>
* <span data-ttu-id="e6428-801">Get-AzureRmVmDiskEncryptionStatus устраняет проблему, которая наблюдалась на виртуальных машинах без дисков данных.</span><span class="sxs-lookup"><span data-stu-id="e6428-801">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="e6428-802">Обновлена версия клиентской библиотеки Compute для исправления следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="e6428-802">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="e6428-803">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="e6428-803">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="e6428-804">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="e6428-804">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="e6428-805">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="e6428-805">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="e6428-806">В следующих командлетах исправлено отображение неправильных значений operation ID и operation status:</span><span class="sxs-lookup"><span data-stu-id="e6428-806">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="e6428-807">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e6428-807">Start-AzureRmVM</span></span>
    - <span data-ttu-id="e6428-808">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e6428-808">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="e6428-809">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e6428-809">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="e6428-810">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e6428-810">Set-AzureRmVM</span></span>
    - <span data-ttu-id="e6428-811">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="e6428-811">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="e6428-812">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e6428-812">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="e6428-813">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="e6428-813">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="e6428-814">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="e6428-814">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="e6428-815">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e6428-815">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="e6428-816">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e6428-816">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="e6428-817">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e6428-817">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="e6428-818">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e6428-818">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="e6428-819">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="e6428-819">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="e6428-820">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="e6428-820">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="e6428-821">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="e6428-821">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="e6428-822">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="e6428-822">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="e6428-823">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="e6428-823">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="e6428-824">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="e6428-824">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="e6428-825">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e6428-825">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="e6428-826">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e6428-826">AzureRM.EventGrid</span></span>
* <span data-ttu-id="e6428-827">Удалены условия проверки ValidateNotNullOrEmpty для SubjectBeginsWith/SubjectEndsWith в командлете Update-AzureRmEventGridSubscription, что позволяет при необходимости заменять эти параметры пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="e6428-827">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="e6428-828">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e6428-828">AzureRM.KeyVault</span></span>
* <span data-ttu-id="e6428-829">Исправлена ошибка, когда при выполнении командлета Get-AzureRmKeyVault -Tag не возвращается ни один тег.</span><span class="sxs-lookup"><span data-stu-id="e6428-829">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="e6428-830">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e6428-830">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="e6428-831">Общедоступный выпуск командлетов Policy Insights.</span><span class="sxs-lookup"><span data-stu-id="e6428-831">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="e6428-832">Используется API версии 2018-04-04.</span><span class="sxs-lookup"><span data-stu-id="e6428-832">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="e6428-833">К результатам Get-AzureRmPolicyStateSummary добавлено PolicyDefinitionReferenceId.</span><span class="sxs-lookup"><span data-stu-id="e6428-833">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="e6428-834">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="e6428-834">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="e6428-835">Для командлетов RecoveryServices.Backup добавлен параметр -Vault.</span><span class="sxs-lookup"><span data-stu-id="e6428-835">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="e6428-836">Передача этого параметра переопределяет командлет Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="e6428-836">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="e6428-837">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="e6428-837">AzureRM.Sql</span></span>
* <span data-ttu-id="e6428-838">В файле справки обновлен пример для командлета Get-AzureRmSqlDatabaseExpanded.</span><span class="sxs-lookup"><span data-stu-id="e6428-838">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="e6428-839">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="e6428-839">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="e6428-840">Обновлен файл справки для командлета Add-AzureRmTrafficManagerEndpointConfig.</span><span class="sxs-lookup"><span data-stu-id="e6428-840">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="e6428-841">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="e6428-841">AzureRM.Websites</span></span>
* <span data-ttu-id="e6428-842">Изменено действие командлета Set-AzureRmWebApp. Теперь он не перезаписывает AppSettings, если используется параметр -AssignIdentity.</span><span class="sxs-lookup"><span data-stu-id="e6428-842">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="e6428-843">Командлет New-AzureRmWebAppSlot теперь учитывает дополнительный параметр AppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="e6428-843">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="e6428-844">6.2.1 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="e6428-844">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="e6428-845">AzureRM.OperationalInsights;</span><span class="sxs-lookup"><span data-stu-id="e6428-845">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="e6428-846">В обновленной модели PSWorkspace Network может использовать type в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="e6428-846">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="e6428-847">6.2.0 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="e6428-847">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="e6428-848">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="e6428-848">AzureRM.Profile</span></span>
* <span data-ttu-id="e6428-849">Исправлена ошибка с загрузкой Newtonsoft.Json версии 10.0.3 во время импорта модуля.</span><span class="sxs-lookup"><span data-stu-id="e6428-849">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="e6428-850">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="e6428-850">AzureRM.Compute</span></span>
* <span data-ttu-id="e6428-851">Функция обновления виртуальных машин VMSS.</span><span class="sxs-lookup"><span data-stu-id="e6428-851">VMSS VM Update feature</span></span>
    - <span data-ttu-id="e6428-852">Добавлены командлеты Update-AzureRmVmssVM и New-AzureRmVMDataDisk.</span><span class="sxs-lookup"><span data-stu-id="e6428-852">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="e6428-853">В командлет Add-AzureRmVMDataDisk добавлен параметр VirtualMachineScaleSetVM, который позволяет добавлять диски данных в виртуальные машины VMSS.</span><span class="sxs-lookup"><span data-stu-id="e6428-853">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="e6428-854">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e6428-854">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="e6428-855">Пакет SDK для ADF .NET обновлен до версии 0.8.0-preview. Новая версия содержит такие изменения:</span><span class="sxs-lookup"><span data-stu-id="e6428-855">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="e6428-856">добавлена операция для настройки репозитория фабрики;</span><span class="sxs-lookup"><span data-stu-id="e6428-856">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="e6428-857">связанная служба QuickBooks LinkedService теперь предоставляет свойства consumerKey и consumerSecret;</span><span class="sxs-lookup"><span data-stu-id="e6428-857">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="e6428-858">тип нескольких моделей изменен с SecretBase на Object;</span><span class="sxs-lookup"><span data-stu-id="e6428-858">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="e6428-859">добавлен триггер событий BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="e6428-859">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="e6428-860">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e6428-860">AzureRM.KeyVault</span></span>
* <span data-ttu-id="e6428-861">В документацию добавлены примеры выходных данных.</span><span class="sxs-lookup"><span data-stu-id="e6428-861">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="e6428-862">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="e6428-862">AzureRM.Network</span></span>
* <span data-ttu-id="e6428-863">В командлеты Наблюдателя за сетями добавлены параметры Аналитики трафика.</span><span class="sxs-lookup"><span data-stu-id="e6428-863">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="e6428-864">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="e6428-864">AzureRM.Resources</span></span>
* <span data-ttu-id="e6428-865">Исправлена ошибка, когда командлет Get-AzureRmResource возвращает свойство Properties объектов PSResource.</span><span class="sxs-lookup"><span data-stu-id="e6428-865">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="e6428-866">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="e6428-866">AzureRM.Scheduler</span></span>
* <span data-ttu-id="e6428-867">Исправлена ошибка, когда обновление ServiceBusQueueJob не задает новые значения для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="e6428-867">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="e6428-868">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="e6428-868">AzureRM.Sql</span></span>
* <span data-ttu-id="e6428-869">В перечисленные ниже командлеты добавлен необязательный параметр LicenseType.</span><span class="sxs-lookup"><span data-stu-id="e6428-869">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="e6428-870">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="e6428-870">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="e6428-871">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool;</span><span class="sxs-lookup"><span data-stu-id="e6428-871">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="e6428-872">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="e6428-872">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="e6428-873">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="e6428-873">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="e6428-874">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e6428-874">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="e6428-875">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="e6428-875">AzureRM.Websites</span></span>
* <span data-ttu-id="e6428-876">Командлет New-AzureRMWebApp теперь использует общие алгоритмы из библиотеки Strategy.</span><span class="sxs-lookup"><span data-stu-id="e6428-876">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="e6428-877">6.1.0 — май 2018 г.</span><span class="sxs-lookup"><span data-stu-id="e6428-877">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="e6428-878">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="e6428-878">AzureRM.Profile</span></span>
* <span data-ttu-id="e6428-879">Устранена проблема с выполнением Clear-AzureRmContext, при которой сохранялся пустой контекст с именем предыдущего контекста по умолчанию, что не позволяло пользователю создать новый контекст со старым именем.</span><span class="sxs-lookup"><span data-stu-id="e6428-879">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="e6428-880">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e6428-880">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="e6428-881">Включены операции связывания и отмены связи в автономной системе.</span><span class="sxs-lookup"><span data-stu-id="e6428-881">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="e6428-882">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e6428-882">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="e6428-883">Добавлена поддержка ApiVersions, ApiReleases и ApiRevisions.</span><span class="sxs-lookup"><span data-stu-id="e6428-883">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="e6428-884">Добавлена поддержка серверной части ServiceFabric.</span><span class="sxs-lookup"><span data-stu-id="e6428-884">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="e6428-885">Добавлена поддержка средства ведения журнала Application Insights.</span><span class="sxs-lookup"><span data-stu-id="e6428-885">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="e6428-886">Добавлена поддержка для распознавания номера SKU уровня "Базовый" как допустимого номера SKU службы управления API.</span><span class="sxs-lookup"><span data-stu-id="e6428-886">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="e6428-887">Добавлена поддержка установки сертификатов, выданных частным центром сертификации в качестве корневого или обычного ЦС.</span><span class="sxs-lookup"><span data-stu-id="e6428-887">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="e6428-888">Добавлена поддержка для приема пользовательских SSL-сертификатов с помощью KeyVault и нескольких имен узлов прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="e6428-888">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="e6428-889">Добавлена поддержка для удостоверения MSI.</span><span class="sxs-lookup"><span data-stu-id="e6428-889">Added support for MSI identity</span></span>
* <span data-ttu-id="e6428-890">Добавлена поддержка для принятия политик с помощью URL-адреса. Примечание. Указанные ниже командлеты в следующей версии будут отмечены как нерекомендуемые.</span><span class="sxs-lookup"><span data-stu-id="e6428-890">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="e6428-891">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="e6428-891">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="e6428-892">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="e6428-892">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="e6428-893">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="e6428-893">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="e6428-894">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="e6428-894">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="e6428-895">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="e6428-895">AzureRM.Batch</span></span>
* <span data-ttu-id="e6428-896">Выпущен новый командлет Get-AzureBatchPoolNodeCounts.</span><span class="sxs-lookup"><span data-stu-id="e6428-896">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="e6428-897">Выпущен новый командлет Start-AzureBatchComputeNodeServiceLogUpload.</span><span class="sxs-lookup"><span data-stu-id="e6428-897">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="e6428-898">AzureRM.Consumption:</span><span class="sxs-lookup"><span data-stu-id="e6428-898">AzureRM.Consumption</span></span>
* <span data-ttu-id="e6428-899">Добавлены новые параметры Expand, ResourceGroup, InstanceName, InstanceId, Tags и командлет высшего уровня Get-AzureRmConsumptionUsageDetail.</span><span class="sxs-lookup"><span data-stu-id="e6428-899">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="e6428-900">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e6428-900">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="e6428-901">Исправлен пример для Export-AzureRmDataLakeStoreChildItemProperties.</span><span class="sxs-lookup"><span data-stu-id="e6428-901">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="e6428-902">Исправлено исключение параметра NULL при использовании рекурсии в Set-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="e6428-902">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="e6428-903">Исправлены файлы справки для Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl и Remove-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="e6428-903">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="e6428-904">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="e6428-904">AzureRM.Network</span></span>
* <span data-ttu-id="e6428-905">Пакет SDK для сети обновлен с предварительной версии 18.0.0 до предварительной версии 19.0.0.</span><span class="sxs-lookup"><span data-stu-id="e6428-905">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="e6428-906">Добавлен командлет для создания конфигурации протокола.</span><span class="sxs-lookup"><span data-stu-id="e6428-906">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="e6428-907">New-AzureRmNetworkWatcherProtocolConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e6428-907">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="e6428-908">Добавлен командлет для добавления нового подключения канала к существующему каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e6428-908">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="e6428-909">Add-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="e6428-909">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="e6428-910">Добавлен командлет для удаления подключения канала к существующему каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e6428-910">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="e6428-911">Remove-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="e6428-911">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="e6428-912">Добавлен командлет для получения подключения канала.</span><span class="sxs-lookup"><span data-stu-id="e6428-912">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="e6428-913">Get-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="e6428-913">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="e6428-914">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e6428-914">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="e6428-915">Исправлена процедура аутентификации сервера с использованием созданных сертификатов (проблема № 5998).</span><span class="sxs-lookup"><span data-stu-id="e6428-915">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="e6428-916">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="e6428-916">AzureRM.Sql</span></span>
* <span data-ttu-id="e6428-917">Обновлены командлеты аудита, которые теперь позволяют удалять AuditActions или AuditActionGroups.</span><span class="sxs-lookup"><span data-stu-id="e6428-917">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="e6428-918">Исправлена проблема с Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy, при которой установка новой гибкой политики хранения завершалась ошибкой с сообщением "Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span><span class="sxs-lookup"><span data-stu-id="e6428-918">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="e6428-919">Please submit request with the new flexible retention policy" (Настройка политики долгосрочного хранения с помощью хранилища и политики служб восстановления Azure больше не поддерживается. Отправьте запрос с использованием новой гибкой политики хранения).</span><span class="sxs-lookup"><span data-stu-id="e6428-919">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="e6428-920">Обновлены все командлеты, связанные со службой "База данных SQL Azure", с созданием эластичных пулов и обновлением. Теперь используются новые API баз данных с поддержкой свойства номеров SKU для обеспечения масштабируемости и связанных с уровнями возможностей.</span><span class="sxs-lookup"><span data-stu-id="e6428-920">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="e6428-921">Обновлены командлеты, в том числе:</span><span class="sxs-lookup"><span data-stu-id="e6428-921">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="e6428-922">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="e6428-922">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="e6428-923">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool;</span><span class="sxs-lookup"><span data-stu-id="e6428-923">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="e6428-924">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="e6428-924">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="e6428-925">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="e6428-925">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="e6428-926">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e6428-926">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="e6428-927">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="e6428-927">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="e6428-928">Обновлены параметры для Get-AzureRmTrafficManagerProfile. Теперь при использовании параметра -Name требуется параметр -ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="e6428-928">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>