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
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2019
ms.locfileid: "56153946"
---
# <a name="release-notes"></a><span data-ttu-id="47dbf-103">Заметки о выпуске</span><span class="sxs-lookup"><span data-stu-id="47dbf-103">Release notes</span></span>

<span data-ttu-id="47dbf-104">Здесь приведен список изменений, внесенных в Azure PowerShell в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="47dbf-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6130---november-2018"></a><span data-ttu-id="47dbf-105">6.13.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="47dbf-105">6.13.0 - November 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="47dbf-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="47dbf-106">AzureRM.Profile</span></span>
* <span data-ttu-id="47dbf-107">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-107">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="47dbf-108">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="47dbf-108">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="47dbf-109">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="47dbf-109">Update dependencies for type mapping issue</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="47dbf-110">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="47dbf-110">AzureRM.Automation</span></span>
* <span data-ttu-id="47dbf-111">Командлеты службы автоматизации Azure на базе Swagger.</span><span class="sxs-lookup"><span data-stu-id="47dbf-111">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="47dbf-112">Добавлены командлеты для Управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="47dbf-112">Added Update Management cmdlets</span></span>
* <span data-ttu-id="47dbf-113">Добавлены командлеты для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="47dbf-113">Added Source Control cmdlets</span></span>
* <span data-ttu-id="47dbf-114">Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="47dbf-114">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="47dbf-115">Исправлена команда DSC для регистрации узла.</span><span class="sxs-lookup"><span data-stu-id="47dbf-115">Fixed the DSC Register Node command</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="47dbf-116">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="47dbf-116">AzureRM.Compute</span></span>
* <span data-ttu-id="47dbf-117">Исправлена проблема с удостоверением, назначаемым системой.</span><span class="sxs-lookup"><span data-stu-id="47dbf-117">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="47dbf-118">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="47dbf-118">Update dependencies for type mapping issue</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="47dbf-119">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="47dbf-119">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="47dbf-120">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="47dbf-120">Update dependencies for type mapping issue</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="47dbf-121">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="47dbf-121">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="47dbf-122">Обновлено описание в примерах командлетов для Marketplace.</span><span class="sxs-lookup"><span data-stu-id="47dbf-122">update the examples description for marketplace cmdlets</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="47dbf-123">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="47dbf-123">AzureRM.Network</span></span>
* <span data-ttu-id="47dbf-124">Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="47dbf-124">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="47dbf-125">Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="47dbf-125">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="47dbf-126">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="47dbf-126">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="47dbf-127">Исправлены проблемы с использованием памяти в карте виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="47dbf-127">Fix issues with memory usage in VirtualNetwork map</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="47dbf-128">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="47dbf-128">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="47dbf-129">Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="47dbf-129">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="47dbf-130">Параметры часового пояса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="47dbf-130">Converted policy timezone to uppercase.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="47dbf-131">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="47dbf-131">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="47dbf-132">Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="47dbf-132">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="47dbf-133">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="47dbf-133">Update dependencies for type mapping issue</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="47dbf-134">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="47dbf-134">AzureRM.Relay</span></span>
* <span data-ttu-id="47dbf-135">Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.</span><span class="sxs-lookup"><span data-stu-id="47dbf-135">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="47dbf-136">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="47dbf-136">AzureRM.Resources</span></span>
* <span data-ttu-id="47dbf-137">Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.</span><span class="sxs-lookup"><span data-stu-id="47dbf-137">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="47dbf-138">Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.</span><span class="sxs-lookup"><span data-stu-id="47dbf-138">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="47dbf-139">Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.</span><span class="sxs-lookup"><span data-stu-id="47dbf-139">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="47dbf-140">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="47dbf-140">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="47dbf-141">Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.</span><span class="sxs-lookup"><span data-stu-id="47dbf-141">Add deprecation messages for upcoming breaking changes</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="47dbf-142">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="47dbf-142">AzureRM.Sql</span></span>
* <span data-ttu-id="47dbf-143">Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="47dbf-143">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="47dbf-144">Get-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="47dbf-144">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="47dbf-145">New-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="47dbf-145">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="47dbf-146">Set-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="47dbf-146">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="47dbf-147">Remove-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="47dbf-147">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="47dbf-148">Get-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="47dbf-148">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="47dbf-149">New-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="47dbf-149">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="47dbf-150">Restore-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="47dbf-150">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="47dbf-151">Remove-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="47dbf-151">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="47dbf-152">Добавлено расширенное управление политиками аудита для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="47dbf-152">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="47dbf-153">Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="47dbf-153">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="47dbf-154">Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.</span><span class="sxs-lookup"><span data-stu-id="47dbf-154">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="47dbf-155">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="47dbf-155">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="47dbf-156">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="47dbf-156">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="47dbf-157">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="47dbf-157">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="47dbf-158">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="47dbf-158">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="47dbf-159">Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="47dbf-159">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="6120---november-2018"></a><span data-ttu-id="47dbf-160">6.12.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="47dbf-160">6.12.0 - November 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="47dbf-161">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="47dbf-161">AzureRM.Profile</span></span>
* <span data-ttu-id="47dbf-162">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-162">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="47dbf-163">В командлете Connect-AzureRmAccount параметр TenantId переименован на Tenant и добавлен псевдоним для TenantId.</span><span class="sxs-lookup"><span data-stu-id="47dbf-163">Rename param TenantId in cmdlet Connect-AzureRmAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="47dbf-164">Обновлено описание TenantId для командлета Connect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="47dbf-164">Updated TenantId description for Connect-AzureRmAccount</span></span>
* <span data-ttu-id="47dbf-165">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="47dbf-165">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="47dbf-166">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="47dbf-166">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="47dbf-167">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="47dbf-167">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="47dbf-168">Устранена проблема, при которой командлет Disconnect-AzureRmAccount вызывал сбой при отсутствии подключения.</span><span class="sxs-lookup"><span data-stu-id="47dbf-168">Fix issue where 'Disconnect-AzureRmAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azurermautomation"></a><span data-ttu-id="47dbf-169">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="47dbf-169">AzureRM.Automation</span></span>
* <span data-ttu-id="47dbf-170">Имя файла библиотеки DLL командлетов переименовано на Microsoft.Azure.Commands.Automation.dll.</span><span class="sxs-lookup"><span data-stu-id="47dbf-170">Renamed cmdlet DLL filename to Microsoft.Azure.Commands.Automation.dll</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="47dbf-171">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="47dbf-171">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="47dbf-172">Добавлена операция Get-AzureRmCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="47dbf-172">Add Get-AzureRmCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="47dbf-173">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="47dbf-173">AzureRM.Compute</span></span>
* <span data-ttu-id="47dbf-174">Добавлены командлеты Add-AzureRmVmssVMDataDisk и Remove-AzureRmVmssVMDataDisk.</span><span class="sxs-lookup"><span data-stu-id="47dbf-174">Add Add-AzureRmVmssVMDataDisk and Remove-AzureRmVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="47dbf-175">Get-AzureRmVMImage отображает AutomaticOSUpgradeProperties.</span><span class="sxs-lookup"><span data-stu-id="47dbf-175">Get-AzureRmVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="47dbf-176">Устранена проблема, при которой значения параметров SetAzureRmVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="47dbf-176">Fixed SetAzureRmVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="47dbf-177">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="47dbf-177">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="47dbf-178">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="47dbf-178">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="47dbf-179">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="47dbf-179">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="47dbf-180">AzureRM.Insights;</span><span class="sxs-lookup"><span data-stu-id="47dbf-180">AzureRM.Insights</span></span>
* <span data-ttu-id="47dbf-181">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="47dbf-181">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="47dbf-182">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="47dbf-182">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="47dbf-183">Исправлена проблема № 7513 [Insights], ппри которой для командлета Set-AzureRMDiagnosticSetting требовалось явное указание категорий во время создания параметра.</span><span class="sxs-lookup"><span data-stu-id="47dbf-183">Fixed issue #7513 [Insights] Set-AzureRMDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="47dbf-184">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="47dbf-184">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="47dbf-185">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="47dbf-185">AzureRM.Network</span></span>
* <span data-ttu-id="47dbf-186">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="47dbf-186">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="47dbf-187">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="47dbf-187">Get-AzureRmExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="47dbf-188">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="47dbf-188">Get-AzureRmExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="47dbf-189">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="47dbf-189">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="47dbf-190">Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="47dbf-190">Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="47dbf-191">Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="47dbf-191">Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="47dbf-192">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="47dbf-192">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="47dbf-193">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="47dbf-193">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="47dbf-194">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="47dbf-194">Added policy remediation cmdlets</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="47dbf-195">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="47dbf-195">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="47dbf-196">Добавлена поддержка общих файловых ресурсов Azure в Службах восстановления.</span><span class="sxs-lookup"><span data-stu-id="47dbf-196">Added support for azure file shares in recovery services.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="47dbf-197">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="47dbf-197">AzureRM.Resources</span></span>
* <span data-ttu-id="47dbf-198">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="47dbf-198">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="47dbf-199">Разрешено перечисление ресурсов с использованием параметра -ResourceId для командлета Get-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="47dbf-199">Allow listing resources using the '-ResourceId' parameter for 'Get-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="47dbf-200">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="47dbf-200">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="47dbf-201">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="47dbf-201">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="47dbf-202">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="47dbf-202">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="47dbf-203">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="47dbf-203">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="47dbf-204">Исправлен командлет Add-AzureRmServiceFabricClusterCertificate.</span><span class="sxs-lookup"><span data-stu-id="47dbf-204">Fix 'Add-AzureRmServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="47dbf-205">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="47dbf-205">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="47dbf-206">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="47dbf-206">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="47dbf-207">Исправлен командлет Update-AzureRmServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="47dbf-207">Fix 'Update-AzureRmServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="6110---october-2018"></a><span data-ttu-id="47dbf-208">6.11.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="47dbf-208">6.11.0 - October 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="47dbf-209">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="47dbf-209">AzureRM.Profile</span></span>
* <span data-ttu-id="47dbf-210">Устранена проблема с Get-AzureRmSubscription в CloudShell.</span><span class="sxs-lookup"><span data-stu-id="47dbf-210">Fix issue with Get-AzureRmSubscription in CloudShell</span></span>
* <span data-ttu-id="47dbf-211">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-211">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="47dbf-212">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="47dbf-212">AzureRM.Backup</span></span>
* <span data-ttu-id="47dbf-213">Командлеты Azure Backup объявлены нерекомендуемыми.</span><span class="sxs-lookup"><span data-stu-id="47dbf-213">Deprecated Azure Backup cmdlets.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="47dbf-214">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="47dbf-214">AzureRM.Compute</span></span>
* <span data-ttu-id="47dbf-215">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzureRmVm.</span><span class="sxs-lookup"><span data-stu-id="47dbf-215">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzureRmVm'</span></span>
* <span data-ttu-id="47dbf-216">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="47dbf-216">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="47dbf-217">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="47dbf-217">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="47dbf-218">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="47dbf-218">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="47dbf-219">Get-AzureRmDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="47dbf-219">Get-AzureRmDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="47dbf-220">Add-AzureRmDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="47dbf-220">Add-AzureRmDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="47dbf-221">Set-AzureRmDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="47dbf-221">Set-AzureRmDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="47dbf-222">Remove-AzureRmDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="47dbf-222">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="47dbf-223">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="47dbf-223">AzureRM.Network</span></span>
* <span data-ttu-id="47dbf-224">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="47dbf-224">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="47dbf-225">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="47dbf-225">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="47dbf-226">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="47dbf-226">AzureRM.Resources</span></span>
* <span data-ttu-id="47dbf-227">Мы устранили проблему, из-за которой командлет Get-AzureRMRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), и добавили понятное исключение.</span><span class="sxs-lookup"><span data-stu-id="47dbf-227">Fix isssue where Get-AzureRMRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="47dbf-228">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="47dbf-228">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="6100---october-2018"></a><span data-ttu-id="47dbf-229">6.10.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="47dbf-229">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="47dbf-230">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="47dbf-230">Azure.Storage</span></span>
* <span data-ttu-id="47dbf-231">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="47dbf-231">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="47dbf-232">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="47dbf-232">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="47dbf-233">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="47dbf-233">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="47dbf-234">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="47dbf-234">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="47dbf-235">Поддержка Get-AzureRmCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="47dbf-235">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="47dbf-236">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="47dbf-236">AzureRM.Compute</span></span>
* <span data-ttu-id="47dbf-237">Исправлена команда Get-AzureRmVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов.</span><span class="sxs-lookup"><span data-stu-id="47dbf-237">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="47dbf-238">Добавлен пример использования SimpleParameterSet в справку командлета New-AzureRmVmss.</span><span class="sxs-lookup"><span data-stu-id="47dbf-238">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="47dbf-239">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="47dbf-239">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="47dbf-240">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="47dbf-240">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="47dbf-241">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="47dbf-241">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="47dbf-242">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="47dbf-242">AzureRM.Network</span></span>
* <span data-ttu-id="47dbf-243">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="47dbf-243">Added NetworkProfile functionality.</span></span> <span data-ttu-id="47dbf-244">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="47dbf-244">new cmdlets added</span></span>
    - <span data-ttu-id="47dbf-245">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="47dbf-245">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="47dbf-246">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="47dbf-246">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="47dbf-247">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="47dbf-247">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="47dbf-248">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="47dbf-248">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="47dbf-249">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="47dbf-249">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="47dbf-250">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="47dbf-250">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="47dbf-251">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="47dbf-251">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="47dbf-252">Добавлены командлеты: New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap.</span><span class="sxs-lookup"><span data-stu-id="47dbf-252">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="47dbf-253">Добавлены командлеты: Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="47dbf-253">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="47dbf-254">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="47dbf-254">AzureRM.RedisCache</span></span>
* <span data-ttu-id="47dbf-255">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="47dbf-255">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="47dbf-256">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="47dbf-256">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="47dbf-257">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="47dbf-257">AzureRM.Resources</span></span>
* <span data-ttu-id="47dbf-258">Добавлен отсутствующий параметр -Mode в командлет Set-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="47dbf-258">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="47dbf-259">Исправлена ошибка командлета Get-AzureRmProviderOperation для операций, когда Origin содержит User.</span><span class="sxs-lookup"><span data-stu-id="47dbf-259">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="47dbf-260">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="47dbf-260">AzureRM.Sql</span></span>
* <span data-ttu-id="47dbf-261">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="47dbf-261">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="47dbf-262">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="47dbf-262">AzureRM.Storage</span></span>
* <span data-ttu-id="47dbf-263">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="47dbf-263">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="47dbf-264">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="47dbf-264">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="47dbf-265">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="47dbf-265">AzureRM.Websites</span></span>
* <span data-ttu-id="47dbf-266">Новый командлет Get-AzureRMWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера.</span><span class="sxs-lookup"><span data-stu-id="47dbf-266">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="47dbf-267">Новые командлеты New-AzureRMWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows.</span><span class="sxs-lookup"><span data-stu-id="47dbf-267">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="47dbf-268">6.9.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="47dbf-268">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="47dbf-269">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="47dbf-269">General</span></span>
* <span data-ttu-id="47dbf-270">В модуль развертывания AzureRM добавлен командлет AzureRM.SignalR.</span><span class="sxs-lookup"><span data-stu-id="47dbf-270">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="47dbf-271">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="47dbf-271">AzureRM.Profile</span></span>
* <span data-ttu-id="47dbf-272">Незначительные изменения в общем коде хранилища.</span><span class="sxs-lookup"><span data-stu-id="47dbf-272">Minor changes to the storage common code</span></span>
* <span data-ttu-id="47dbf-273">Обновлены файлы справки, в которые добавлены полные типы параметров.</span><span class="sxs-lookup"><span data-stu-id="47dbf-273">Updated help files to include full parameter types.</span></span>
* <span data-ttu-id="47dbf-274">В наборе параметров ServicePrincipalCertificateWithSubscriptionId параметр -ServicePrincipal теперь стал необязательным.</span><span class="sxs-lookup"><span data-stu-id="47dbf-274">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="47dbf-275">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="47dbf-275">Azure.Storage</span></span>
* <span data-ttu-id="47dbf-276">Поддержка создания контекста хранилища с использованием OAuth.</span><span class="sxs-lookup"><span data-stu-id="47dbf-276">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="47dbf-277">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="47dbf-277">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="47dbf-278">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="47dbf-278">AzureRM.Cdn</span></span>
* <span data-ttu-id="47dbf-279">Добавлен номер SKU для расценок на Standard_Microsoft в CDN.</span><span class="sxs-lookup"><span data-stu-id="47dbf-279">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="47dbf-280">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="47dbf-280">AzureRM.Compute</span></span>
* <span data-ttu-id="47dbf-281">Keyvault и Storage перенесены в общие зависимости.</span><span class="sxs-lookup"><span data-stu-id="47dbf-281">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="47dbf-282">Добавлена поддержка большего количества размеров виртуальных машин в командлеты AEM.</span><span class="sxs-lookup"><span data-stu-id="47dbf-282">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="47dbf-283">Добавлен параметр PublicIPPrefix в командлет New-AzureRmVmssIpConfig.</span><span class="sxs-lookup"><span data-stu-id="47dbf-283">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="47dbf-284">Добавлен параметр ResourceId в командлет Invoke-AzureRmVMRunCommand.</span><span class="sxs-lookup"><span data-stu-id="47dbf-284">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="47dbf-285">Добавлен командлет Invoke-AzureRmVmssVMRunCommand.</span><span class="sxs-lookup"><span data-stu-id="47dbf-285">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="47dbf-286">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="47dbf-286">AzureRM.Dns</span></span>
* <span data-ttu-id="47dbf-287">Добавлена поддержка для псевдонима записи во время создания записи DNS.</span><span class="sxs-lookup"><span data-stu-id="47dbf-287">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="47dbf-288">AzureRM.Insights;</span><span class="sxs-lookup"><span data-stu-id="47dbf-288">AzureRM.Insights</span></span>
* <span data-ttu-id="47dbf-289">Исправлены проблемы № 6833 и № 7102 (область настроек диагностики).</span><span class="sxs-lookup"><span data-stu-id="47dbf-289">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="47dbf-290">Проблемы с именем по умолчанию, например service, во время создания, получения и отображения списка параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="47dbf-290">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="47dbf-291">Проблемы при создании параметров диагностики с категориями.</span><span class="sxs-lookup"><span data-stu-id="47dbf-291">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="47dbf-292">Добавлено сообщение о том, что не рекомендуется использовать параметры интервалов времени в метриках.</span><span class="sxs-lookup"><span data-stu-id="47dbf-292">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="47dbf-293">Параметры интервалов времени по-прежнему принимаются (это не критическое изменение), но они игнорируются в серверной части, потому что действительно только значение PT1M.</span><span class="sxs-lookup"><span data-stu-id="47dbf-293">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="47dbf-294">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="47dbf-294">AzureRM.Network</span></span>
* <span data-ttu-id="47dbf-295">Изменения командлетов LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="47dbf-295">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="47dbf-296">LoadBalancerInboundNatPoolConfig: добавлены параметры IdleTimeoutInMinutes, EnableFloatingIp и EnableTcpReset.</span><span class="sxs-lookup"><span data-stu-id="47dbf-296">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="47dbf-297">LoadBalancerInboundNatRuleConfig: добавлен параметр EnableTcpReset.</span><span class="sxs-lookup"><span data-stu-id="47dbf-297">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="47dbf-298">LoadBalancerRuleConfig: добавлен параметр EnableTcpReset.</span><span class="sxs-lookup"><span data-stu-id="47dbf-298">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="47dbf-299">LoadBalancerProbeConfig: добавлена поддержка значения Https для параметра Protocol.</span><span class="sxs-lookup"><span data-stu-id="47dbf-299">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="47dbf-300">Добавлены новые команды для нового правила OutboundRule подресурса LoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="47dbf-300">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="47dbf-301">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="47dbf-301">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="47dbf-302">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="47dbf-302">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="47dbf-303">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="47dbf-303">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="47dbf-304">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="47dbf-304">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="47dbf-305">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="47dbf-305">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="47dbf-306">Добавлено новое свойство HostedWorkloads для PSNetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="47dbf-306">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="47dbf-307">Добавлены новые командлеты для функции "Брандмауэр Azure" (ARM):</span><span class="sxs-lookup"><span data-stu-id="47dbf-307">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="47dbf-308">Добавлен командлет Get-AzureRmFirewall.</span><span class="sxs-lookup"><span data-stu-id="47dbf-308">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="47dbf-309">Добавлен командлет Set-AzureRmFirewall.</span><span class="sxs-lookup"><span data-stu-id="47dbf-309">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="47dbf-310">Добавлен командлет New-AzureRmFirewall.</span><span class="sxs-lookup"><span data-stu-id="47dbf-310">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="47dbf-311">Добавлен командлет Remove-AzureRmFirewall.</span><span class="sxs-lookup"><span data-stu-id="47dbf-311">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="47dbf-312">Добавлен командлет New-AzureRmFirewallApplicationRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="47dbf-312">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="47dbf-313">Добавлен командлет New-AzureRmFirewallApplicationRule.</span><span class="sxs-lookup"><span data-stu-id="47dbf-313">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="47dbf-314">Добавлен командлет New-AzureRmFirewallNatRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="47dbf-314">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="47dbf-315">Добавлен командлет New-AzureRmFirewallNatRule.</span><span class="sxs-lookup"><span data-stu-id="47dbf-315">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="47dbf-316">Добавлен командлет New-AzureRmFirewallNetworkRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="47dbf-316">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="47dbf-317">Добавлен командлет New-AzureRmFirewallNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="47dbf-317">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="47dbf-318">Добавлена поддержка конфигурации для доверенного корневого сертификата и автомасштабирования в Шлюзе приложений.</span><span class="sxs-lookup"><span data-stu-id="47dbf-318">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="47dbf-319">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="47dbf-319">New Cmdlets added:</span></span>
      - <span data-ttu-id="47dbf-320">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="47dbf-320">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="47dbf-321">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="47dbf-321">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="47dbf-322">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="47dbf-322">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="47dbf-323">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="47dbf-323">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="47dbf-324">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="47dbf-324">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="47dbf-325">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="47dbf-325">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="47dbf-326">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="47dbf-326">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="47dbf-327">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="47dbf-327">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="47dbf-328">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="47dbf-328">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="47dbf-329">В следующие командлеты добавлен необязательный параметр -TrustedRootCertificate:</span><span class="sxs-lookup"><span data-stu-id="47dbf-329">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="47dbf-330">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="47dbf-330">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="47dbf-331">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="47dbf-331">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="47dbf-332">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="47dbf-332">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="47dbf-333">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="47dbf-333">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="47dbf-334">В следующие командлеты добавлен необязательный параметр -AutoscaleConfiguration:</span><span class="sxs-lookup"><span data-stu-id="47dbf-334">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="47dbf-335">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="47dbf-335">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="47dbf-336">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="47dbf-336">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="47dbf-337">Добавлен командлет для конечной точки интерфейса Get-AzureInterfaceEndpoint.</span><span class="sxs-lookup"><span data-stu-id="47dbf-337">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="47dbf-338">Добавлена поддержка нескольких префиксов адресов в подсети.</span><span class="sxs-lookup"><span data-stu-id="47dbf-338">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="47dbf-339">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="47dbf-339">Updated cmdlets:</span></span>
  - <span data-ttu-id="47dbf-340">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="47dbf-340">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="47dbf-341">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="47dbf-341">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="47dbf-342">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="47dbf-342">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="47dbf-343">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="47dbf-343">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="47dbf-344">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="47dbf-344">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="47dbf-345">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="47dbf-345">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="47dbf-346">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="47dbf-346">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="47dbf-347">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="47dbf-347">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="47dbf-348">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="47dbf-348">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="47dbf-349">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="47dbf-349">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="47dbf-350">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="47dbf-350">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="47dbf-351">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="47dbf-351">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="47dbf-352">New-AzureRmNetworkInterfaceIpConfig — Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="47dbf-352">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="47dbf-353">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="47dbf-353">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="47dbf-354">Add-AzureRmVirtualNetworkGatewayIpConfig;</span><span class="sxs-lookup"><span data-stu-id="47dbf-354">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="47dbf-355">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="47dbf-355">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="47dbf-356">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="47dbf-356">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="47dbf-357">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="47dbf-357">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="47dbf-358">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="47dbf-358">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="47dbf-359">Добавлены командлеты для делегирования подсети.</span><span class="sxs-lookup"><span data-stu-id="47dbf-359">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="47dbf-360">New-AzureRmDelegation: создание делегирования, которое можно добавить к подсети.</span><span class="sxs-lookup"><span data-stu-id="47dbf-360">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="47dbf-361">Remove-AzureRmDelegation: принятие подсети и удаление указанного имени делегирования из этой подсети.</span><span class="sxs-lookup"><span data-stu-id="47dbf-361">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="47dbf-362">Add-AzureRmDelegation: принятие подсети и добавление указанного имени службы в качестве делегирования для этой подсети.</span><span class="sxs-lookup"><span data-stu-id="47dbf-362">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="47dbf-363">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="47dbf-363">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="47dbf-364">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="47dbf-364">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="47dbf-365">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="47dbf-365">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="47dbf-366">Добавлена поддержка управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="47dbf-366">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="47dbf-367">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="47dbf-367">AzureRM.RedisCache</span></span>
* <span data-ttu-id="47dbf-368">Обновлена зависимость Insights.</span><span class="sxs-lookup"><span data-stu-id="47dbf-368">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="47dbf-369">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="47dbf-369">AzureRM.Resources</span></span>
* <span data-ttu-id="47dbf-370">В командлет New-AzureRmResourceGroupDeployment добавлен новый параметр RollbackAction.</span><span class="sxs-lookup"><span data-stu-id="47dbf-370">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="47dbf-371">Добавлена поддержка OnErrorDeployment с новым параметром.</span><span class="sxs-lookup"><span data-stu-id="47dbf-371">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="47dbf-372">Добавлена поддержка управляемого удостоверения при назначении политик.</span><span class="sxs-lookup"><span data-stu-id="47dbf-372">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="47dbf-373">При назначении политики с помощью New-AzureRmPolicyAssignment параметры со значениями по умолчанию больше не требуются.</span><span class="sxs-lookup"><span data-stu-id="47dbf-373">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="47dbf-374">Добавлен новый командлет Get-AzureRmPolicyAlias для получения псевдонимов политик.</span><span class="sxs-lookup"><span data-stu-id="47dbf-374">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="47dbf-375">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="47dbf-375">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="47dbf-376">Устранена проблема № 7161.</span><span class="sxs-lookup"><span data-stu-id="47dbf-376">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="47dbf-377">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="47dbf-377">AzureRM.SignalR</span></span>
* <span data-ttu-id="47dbf-378">Обновлены номера SKU для Free_F1 и Standard_S1.</span><span class="sxs-lookup"><span data-stu-id="47dbf-378">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="47dbf-379">Добавлены поле версии в объект PSSignalRResource и строка подключения в объект PSSignalRKeys.</span><span class="sxs-lookup"><span data-stu-id="47dbf-379">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="47dbf-380">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="47dbf-380">AzureRM.Storage</span></span>
* <span data-ttu-id="47dbf-381">Добавлена поддержка политики неизменяемости в AzureRm.Storage.</span><span class="sxs-lookup"><span data-stu-id="47dbf-381">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="47dbf-382">Remove-AzureRmStorageAccountNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="47dbf-382">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="47dbf-383">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="47dbf-383">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="47dbf-384">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="47dbf-384">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="47dbf-385">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="47dbf-385">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="47dbf-386">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="47dbf-386">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="47dbf-387">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="47dbf-387">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="47dbf-388">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="47dbf-388">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="47dbf-389">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="47dbf-389">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="47dbf-390">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="47dbf-390">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="47dbf-391">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="47dbf-391">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="47dbf-392">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="47dbf-392">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="47dbf-393">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="47dbf-393">AzureRM.Websites</span></span>
* <span data-ttu-id="47dbf-394">Добавлены два новых командлета: Get-AzureRmDeletedWebApp и Restore-AzureRmDeletedWebApp.</span><span class="sxs-lookup"><span data-stu-id="47dbf-394">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="47dbf-395">New-AzureRmAppServicePlan: добавлен параметр -HyperV для создания плана службы приложений с контейнером Windows.</span><span class="sxs-lookup"><span data-stu-id="47dbf-395">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="47dbf-396">New-AzureRmWebApp, New-AzureRmWebAppSlot, Set-AzureRmWebApp, Set-AzureRmWebAppSlot: добавлены новые параметры (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) для создания контейнера приложения Windows и управления им.</span><span class="sxs-lookup"><span data-stu-id="47dbf-396">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="47dbf-397">6.8.1 — август 2018 г.</span><span class="sxs-lookup"><span data-stu-id="47dbf-397">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="47dbf-398">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="47dbf-398">General</span></span>
* <span data-ttu-id="47dbf-399">Исправлена проблема с отсутствием настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="47dbf-399">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="47dbf-400">Обновлены общие сборки среды выполнения</span><span class="sxs-lookup"><span data-stu-id="47dbf-400">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="47dbf-401">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="47dbf-401">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="47dbf-402">Исправлена проблема с отсутствием настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="47dbf-402">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="47dbf-403">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6603.</span><span class="sxs-lookup"><span data-stu-id="47dbf-403">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="47dbf-404">Командлеты Import-AzureRmApiManagementApi и \*-AzureRmApiManagementCertificate теперь обрабатывают относительные пути.</span><span class="sxs-lookup"><span data-stu-id="47dbf-404">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="47dbf-405">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6879.</span><span class="sxs-lookup"><span data-stu-id="47dbf-405">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="47dbf-406">CertificateInformation — это задаваемое свойство, обеспечивающее правильную работу командлета Set-AzureRmApiManagement.</span><span class="sxs-lookup"><span data-stu-id="47dbf-406">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="47dbf-407">Проблема исправлена путем обновления пакета NuGet до версии 4.0.4-preview.</span><span class="sxs-lookup"><span data-stu-id="47dbf-407">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="47dbf-408">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6853.</span><span class="sxs-lookup"><span data-stu-id="47dbf-408">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="47dbf-409">Исправлен фильтр OData для поиска по имени продукта.</span><span class="sxs-lookup"><span data-stu-id="47dbf-409">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="47dbf-410">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6814.</span><span class="sxs-lookup"><span data-stu-id="47dbf-410">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="47dbf-411">Исправлен фильтр OData для поиска по имени API.</span><span class="sxs-lookup"><span data-stu-id="47dbf-411">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="47dbf-412">Добавлена поддержка средства ведения журнала Azure Monitor.</span><span class="sxs-lookup"><span data-stu-id="47dbf-412">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="47dbf-413">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="47dbf-413">AzureRM.Compute</span></span>
* <span data-ttu-id="47dbf-414">Исправлена проблема с отсутствием в выходных данных ошибки целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="47dbf-414">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="47dbf-415">Исправлена проблема с типом учетной записи хранения для виртуальной машины с управляемым диском.</span><span class="sxs-lookup"><span data-stu-id="47dbf-415">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="47dbf-416">Исправлена проблема с отсутствием настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="47dbf-416">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="47dbf-417">Исправлены командлеты расширения AEM для других сред, например Azure для Китая.</span><span class="sxs-lookup"><span data-stu-id="47dbf-417">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="47dbf-418">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="47dbf-418">AzureRM.Network</span></span>
* <span data-ttu-id="47dbf-419">Стандартное представление выходных данных командлетов изменено на представление таблиц.</span><span class="sxs-lookup"><span data-stu-id="47dbf-419">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="47dbf-420">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="47dbf-420">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="47dbf-421">Исправлена проблема с Update-AzureRmPowerBIEmbeddedCapacity при попытке масштабировать приостановленную емкость.</span><span class="sxs-lookup"><span data-stu-id="47dbf-421">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="47dbf-422">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="47dbf-422">AzureRM.Resources</span></span>
* <span data-ttu-id="47dbf-423">Исправлена проблема с созданием управляемых приложений из Marketplace.</span><span class="sxs-lookup"><span data-stu-id="47dbf-423">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="47dbf-424">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="47dbf-424">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="47dbf-425">Исправленные проблемы</span><span class="sxs-lookup"><span data-stu-id="47dbf-425">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="47dbf-426">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="47dbf-426">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="47dbf-427">Добавлена поддержка метода маршрутизации MultiValue.</span><span class="sxs-lookup"><span data-stu-id="47dbf-427">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="47dbf-428">Добавлен новый параметр MaxReturn для маршрутизации MultiValue.</span><span class="sxs-lookup"><span data-stu-id="47dbf-428">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="47dbf-429">Добавлена поддержка метода маршрутизации Subnet.</span><span class="sxs-lookup"><span data-stu-id="47dbf-429">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="47dbf-430">Добавлена поддержка диапазонов IP-адресов (подсетей) в конечных точках.</span><span class="sxs-lookup"><span data-stu-id="47dbf-430">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="47dbf-431">Добавлена поддержка пользовательских заголовков в профилях.</span><span class="sxs-lookup"><span data-stu-id="47dbf-431">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="47dbf-432">Добавлена поддержка диапазонов кода ожидаемого состояния в профилях.</span><span class="sxs-lookup"><span data-stu-id="47dbf-432">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="47dbf-433">Добавлена поддержка пользовательских заголовков в конечных точках.</span><span class="sxs-lookup"><span data-stu-id="47dbf-433">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="47dbf-434">6.8.0 — август 2018 г.</span><span class="sxs-lookup"><span data-stu-id="47dbf-434">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="47dbf-435">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="47dbf-435">General</span></span>
* <span data-ttu-id="47dbf-436">Исправлена проблема с отсутствием настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="47dbf-436">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="47dbf-437">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="47dbf-437">AzureRM.Profile</span></span>
* <span data-ttu-id="47dbf-438">Добавлено свойство срока действия для маркеров, возвращенных при выполнении Connect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="47dbf-438">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="47dbf-439">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="47dbf-439">AzureRM.Compute</span></span>
* <span data-ttu-id="47dbf-440">Исправлена проблема с отсутствием в выходных данных ошибки целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="47dbf-440">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="47dbf-441">Исправлена проблема с типом учетной записи хранения для виртуальной машины с управляемым диском.</span><span class="sxs-lookup"><span data-stu-id="47dbf-441">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="47dbf-442">Исправлены командлеты расширения AEM для других сред, например Azure для Китая.</span><span class="sxs-lookup"><span data-stu-id="47dbf-442">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="47dbf-443">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="47dbf-443">AzureRM.IotHub</span></span>
* <span data-ttu-id="47dbf-444">Исправлены примеры для New-AzureRmIotHubExportDevices и New-AzureRmIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="47dbf-444">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="47dbf-445">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="47dbf-445">AzureRM.Network</span></span>
* <span data-ttu-id="47dbf-446">Изменено представление моделей по умолчанию на представление таблиц.</span><span class="sxs-lookup"><span data-stu-id="47dbf-446">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="47dbf-447">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="47dbf-447">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="47dbf-448">Исправлена проблема с Update-AzureRmPowerBIEmbeddedCapacity при попытке масштабировать приостановленную емкость.</span><span class="sxs-lookup"><span data-stu-id="47dbf-448">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="47dbf-449">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="47dbf-449">AzureRM.Resources</span></span>
* <span data-ttu-id="47dbf-450">Исправлена проблема с созданием управляемого приложения из marketplace.</span><span class="sxs-lookup"><span data-stu-id="47dbf-450">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="47dbf-451">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="47dbf-451">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="47dbf-452">Исправления проблем</span><span class="sxs-lookup"><span data-stu-id="47dbf-452">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="47dbf-453">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="47dbf-453">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="47dbf-454">Добавлена поддержка метода маршрутизации MultiValue.</span><span class="sxs-lookup"><span data-stu-id="47dbf-454">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="47dbf-455">Добавлен новый параметр MaxReturn для маршрутизации MultiValue.</span><span class="sxs-lookup"><span data-stu-id="47dbf-455">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="47dbf-456">Добавлена поддержка метода маршрутизации Subnet.</span><span class="sxs-lookup"><span data-stu-id="47dbf-456">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="47dbf-457">Добавлена поддержка диапазонов IP-адресов (подсетей) в конечных точках.</span><span class="sxs-lookup"><span data-stu-id="47dbf-457">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="47dbf-458">Добавлена поддержка пользовательских заголовков в профилях.</span><span class="sxs-lookup"><span data-stu-id="47dbf-458">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="47dbf-459">Добавлена поддержка диапазонов кода состояния ожидания в профилях.</span><span class="sxs-lookup"><span data-stu-id="47dbf-459">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="47dbf-460">Добавлена поддержка пользовательских заголовков в конечных точках.</span><span class="sxs-lookup"><span data-stu-id="47dbf-460">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="47dbf-461">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="47dbf-461">AzureRM.Websites</span></span>
* <span data-ttu-id="47dbf-462">Исправлена проблема с отсутствием правильной настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="47dbf-462">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="47dbf-463">6.7.0 — август 2018 г.</span><span class="sxs-lookup"><span data-stu-id="47dbf-463">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="47dbf-464">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="47dbf-464">AzureRM.Profile</span></span>
* <span data-ttu-id="47dbf-465">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-465">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="47dbf-466">Добавлен идентификатор пользователя для имени контекста по умолчанию, чтобы избежать конфликтов контекста.</span><span class="sxs-lookup"><span data-stu-id="47dbf-466">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="47dbf-467">Устранены проблемы с командлетом Clear-AzureRmContext, которые приводили к проблемам с выбором контекста #6398.</span><span class="sxs-lookup"><span data-stu-id="47dbf-467">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="47dbf-468">Разрешено передавать домен клиента в параметр -TenantId для командлета Connect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="47dbf-468">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="47dbf-469">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="47dbf-469">Azure.Storage</span></span>
* <span data-ttu-id="47dbf-470">Удалено ограничение в 5 ТБ для квоты на общую папку Azure.</span><span class="sxs-lookup"><span data-stu-id="47dbf-470">Remove the 5TB limitation for Azure File Share quota</span></span>
* <span data-ttu-id="47dbf-471">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="47dbf-471">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="47dbf-472">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="47dbf-472">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="47dbf-473">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-473">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="47dbf-474">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="47dbf-474">Azure.AnalysisServices</span></span>
* <span data-ttu-id="47dbf-475">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-475">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="47dbf-476">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="47dbf-476">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="47dbf-477">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-477">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="47dbf-478">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="47dbf-478">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="47dbf-479">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-479">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="47dbf-480">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="47dbf-480">AzureRM.Automation</span></span>
* <span data-ttu-id="47dbf-481">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-481">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="47dbf-482">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="47dbf-482">AzureRM.Backup</span></span>
* <span data-ttu-id="47dbf-483">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-483">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="47dbf-484">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="47dbf-484">AzureRM.Batch</span></span>
* <span data-ttu-id="47dbf-485">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-485">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="47dbf-486">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="47dbf-486">AzureRM.Billing</span></span>
* <span data-ttu-id="47dbf-487">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-487">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="47dbf-488">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="47dbf-488">AzureRM.Cdn</span></span>
* <span data-ttu-id="47dbf-489">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-489">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="47dbf-490">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="47dbf-490">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="47dbf-491">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-491">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="47dbf-492">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="47dbf-492">AzureRM.Compute</span></span>
* <span data-ttu-id="47dbf-493">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-493">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="47dbf-494">В командлет New-AzureRmVmssConfig добавлен параметр EvictionPolicy.</span><span class="sxs-lookup"><span data-stu-id="47dbf-494">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="47dbf-495">Если расположение не указано, используйте в DiskFileParameterSet для New AzureRmVm расположение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="47dbf-495">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="47dbf-496">Исправлено описание параметров в Save-AzureRmVMImage.</span><span class="sxs-lookup"><span data-stu-id="47dbf-496">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="47dbf-497">Исправлен командлет Get-AzureRmVMDiskEncryptionStatus для определенных сценариев, связанных с однократным выполнением.</span><span class="sxs-lookup"><span data-stu-id="47dbf-497">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="47dbf-498">AzureRM.Consumption:</span><span class="sxs-lookup"><span data-stu-id="47dbf-498">AzureRM.Consumption</span></span>
* <span data-ttu-id="47dbf-499">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-499">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="47dbf-500">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="47dbf-500">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="47dbf-501">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-501">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="47dbf-502">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="47dbf-502">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="47dbf-503">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-503">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="47dbf-504">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="47dbf-504">AzureRM.DataFactories</span></span>
* <span data-ttu-id="47dbf-505">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-505">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="47dbf-506">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="47dbf-506">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="47dbf-507">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-507">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="47dbf-508">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="47dbf-508">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="47dbf-509">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-509">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="47dbf-510">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="47dbf-510">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="47dbf-511">Исправлена отладка, когда DebugPreference настраивается из командной строки PowerShell.</span><span class="sxs-lookup"><span data-stu-id="47dbf-511">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="47dbf-512">Обновлен пример для Set-AzureRmDataLakeStoreItemAcl.</span><span class="sxs-lookup"><span data-stu-id="47dbf-512">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="47dbf-513">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-513">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="47dbf-514">Обновлен пример для Set-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="47dbf-514">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="47dbf-515">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="47dbf-515">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="47dbf-516">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-516">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="47dbf-517">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="47dbf-517">AzureRM.Dns</span></span>
* <span data-ttu-id="47dbf-518">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-518">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="47dbf-519">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="47dbf-519">AzureRM.EventGrid</span></span>
* <span data-ttu-id="47dbf-520">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-520">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="47dbf-521">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="47dbf-521">AzureRM.EventHub</span></span>
* <span data-ttu-id="47dbf-522">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-522">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="47dbf-523">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="47dbf-523">AzureRM.HDInsight</span></span>
* <span data-ttu-id="47dbf-524">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-524">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="47dbf-525">AzureRM.Insights;</span><span class="sxs-lookup"><span data-stu-id="47dbf-525">AzureRM.Insights</span></span>
* <span data-ttu-id="47dbf-526">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-526">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="47dbf-527">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="47dbf-527">AzureRM.IotHub</span></span>
* <span data-ttu-id="47dbf-528">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-528">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="47dbf-529">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="47dbf-529">AzureRM.KeyVault</span></span>
* <span data-ttu-id="47dbf-530">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-530">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="47dbf-531">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="47dbf-531">AzureRM.LogicApp</span></span>
* <span data-ttu-id="47dbf-532">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-532">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="47dbf-533">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="47dbf-533">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="47dbf-534">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-534">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="47dbf-535">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="47dbf-535">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="47dbf-536">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-536">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="47dbf-537">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="47dbf-537">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="47dbf-538">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-538">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="47dbf-539">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="47dbf-539">AzureRM.Media</span></span>
* <span data-ttu-id="47dbf-540">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-540">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="47dbf-541">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="47dbf-541">AzureRM.Network</span></span>
* <span data-ttu-id="47dbf-542">Добавлен пример для Set-AzureRmLocalNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="47dbf-542">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="47dbf-543">Добавлены примеры и описания для Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey и New-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="47dbf-543">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="47dbf-544">Добавлены примеры для Remove-AzureRmVirtualNetworkGatewayIpConfig и Reset-AzureRmVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="47dbf-544">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="47dbf-545">Добавлен пример для Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.</span><span class="sxs-lookup"><span data-stu-id="47dbf-545">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="47dbf-546">Добавлен пример для Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.</span><span class="sxs-lookup"><span data-stu-id="47dbf-546">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="47dbf-547">Добавлен пример для Set-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="47dbf-547">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="47dbf-548">Повторно созданы командлеты для ApplicationSecurityGroup, RouteTable и Usage с помощью генератора кода последней версии.</span><span class="sxs-lookup"><span data-stu-id="47dbf-548">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="47dbf-549">Уточнено сообщение об ошибке для Get-AzureRmVirtualNetworkSubnetConfig при попытке получить подсеть, которая не существует.</span><span class="sxs-lookup"><span data-stu-id="47dbf-549">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="47dbf-550">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="47dbf-550">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="47dbf-551">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-551">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="47dbf-552">AzureRM.OperationalInsights;</span><span class="sxs-lookup"><span data-stu-id="47dbf-552">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="47dbf-553">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-553">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="47dbf-554">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="47dbf-554">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="47dbf-555">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-555">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="47dbf-556">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="47dbf-556">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="47dbf-557">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-557">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="47dbf-558">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="47dbf-558">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="47dbf-559">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-559">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="47dbf-560">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="47dbf-560">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="47dbf-561">Добавлен фильтр политик для командлета Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="47dbf-561">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="47dbf-562">Команда возвращает список элементов резервного копирования, защищенных политикой с заданным идентификатором.</span><span class="sxs-lookup"><span data-stu-id="47dbf-562">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="47dbf-563">Обновление Microsoft.Azure.Management.RecoveryServices.Backup до версии 3.0.0-preview.</span><span class="sxs-lookup"><span data-stu-id="47dbf-563">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="47dbf-564">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-564">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="47dbf-565">Добавлен параметр TargetResourceGroupName для Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="47dbf-565">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="47dbf-566">Группа ресурсов, в которую восстанавливаются управляемые диски.</span><span class="sxs-lookup"><span data-stu-id="47dbf-566">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="47dbf-567">Применимо к резервной копии виртуальной машины с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="47dbf-567">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="47dbf-568">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="47dbf-568">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="47dbf-569">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-569">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="47dbf-570">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="47dbf-570">AzureRM.RedisCache</span></span>
* <span data-ttu-id="47dbf-571">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-571">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="47dbf-572">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="47dbf-572">AzureRM.Relay</span></span>
* <span data-ttu-id="47dbf-573">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-573">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="47dbf-574">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="47dbf-574">AzureRM.Resources</span></span>
* <span data-ttu-id="47dbf-575">Поддержка развертывания шаблонов в области подписки.</span><span class="sxs-lookup"><span data-stu-id="47dbf-575">Support template deployment at subscription scope.</span></span> <span data-ttu-id="47dbf-576">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="47dbf-576">Add new Cmdlets:</span></span>
    - <span data-ttu-id="47dbf-577">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="47dbf-577">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="47dbf-578">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="47dbf-578">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="47dbf-579">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="47dbf-579">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="47dbf-580">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="47dbf-580">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="47dbf-581">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="47dbf-581">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="47dbf-582">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="47dbf-582">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="47dbf-583">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="47dbf-583">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="47dbf-584">Устранена проблема, когда при передаче контекста в Set-AzureRmResource возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="47dbf-584">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="47dbf-585">Исправлен пример в New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="47dbf-585">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="47dbf-586">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-586">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="47dbf-587">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="47dbf-587">AzureRM.Scheduler</span></span>
* <span data-ttu-id="47dbf-588">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-588">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="47dbf-589">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="47dbf-589">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="47dbf-590">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-590">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="47dbf-591">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="47dbf-591">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="47dbf-592">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-592">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="47dbf-593">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="47dbf-593">AzureRM.Sql</span></span>
* <span data-ttu-id="47dbf-594">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-594">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="47dbf-595">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="47dbf-595">AzureRM.Storage</span></span>
* <span data-ttu-id="47dbf-596">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-596">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="47dbf-597">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="47dbf-597">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="47dbf-598">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-598">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="47dbf-599">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="47dbf-599">AzureRM.Tags</span></span>
* <span data-ttu-id="47dbf-600">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-600">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="47dbf-601">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="47dbf-601">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="47dbf-602">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-602">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="47dbf-603">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="47dbf-603">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="47dbf-604">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-604">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="47dbf-605">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="47dbf-605">AzureRM.Websites</span></span>
* <span data-ttu-id="47dbf-606">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-606">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="47dbf-607">6.6.0 — июль 2018 г.</span><span class="sxs-lookup"><span data-stu-id="47dbf-607">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="47dbf-608">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="47dbf-608">General</span></span>
* <span data-ttu-id="47dbf-609">Обновлены все файлы справки: включены полные типы параметров и исправлены типы входных и выходных данных.</span><span class="sxs-lookup"><span data-stu-id="47dbf-609">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="47dbf-610">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="47dbf-610">AzureRM.Profile</span></span>
* <span data-ttu-id="47dbf-611">Обновлена библиотека Common.Strategy: теперь можно проверить, совместима ли текущая конфигурация ресурса с целевым ресурсом.</span><span class="sxs-lookup"><span data-stu-id="47dbf-611">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="47dbf-612">В Common.Storage добавлены типы ps1xml.</span><span class="sxs-lookup"><span data-stu-id="47dbf-612">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="47dbf-613">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="47dbf-613">Azure.Storage</span></span>
* <span data-ttu-id="47dbf-614">Добавлена поддержка для получения контекста хранилища из DefaultProfile.</span><span class="sxs-lookup"><span data-stu-id="47dbf-614">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="47dbf-615">В свойства типов выходных данных командлетов добавлен атрибут Ps1XmlAttribute.</span><span class="sxs-lookup"><span data-stu-id="47dbf-615">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="47dbf-616">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="47dbf-616">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="47dbf-617">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6370.</span><span class="sxs-lookup"><span data-stu-id="47dbf-617">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="47dbf-618">В AutoMapper исправлена ошибка, препятствовавшая преобразованию PsApiManagementApi в ApiContract.</span><span class="sxs-lookup"><span data-stu-id="47dbf-618">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="47dbf-619">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6515.</span><span class="sxs-lookup"><span data-stu-id="47dbf-619">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="47dbf-620">В File.Save исправлена ошибка, связанная с перегрузкой типом кодировки.</span><span class="sxs-lookup"><span data-stu-id="47dbf-620">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="47dbf-621">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6560.</span><span class="sxs-lookup"><span data-stu-id="47dbf-621">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="47dbf-622">Выполнено обновление до версии NuGet 4.0.3, что позволило исправить исключение шаблона в apiId.</span><span class="sxs-lookup"><span data-stu-id="47dbf-622">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="47dbf-623">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="47dbf-623">AzureRM.Compute</span></span>
* <span data-ttu-id="47dbf-624">Устранена ошибка при создании виртуальной машины с помощью командлета New-AzureRmVm и параметра DiskFileParameterSet, которая возникала из-за переименования типа учетной записи хранения PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="47dbf-624">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="47dbf-625">Исправлен командлет Invoke-AzureRmVMRunCommand.</span><span class="sxs-lookup"><span data-stu-id="47dbf-625">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="47dbf-626">Командлет Get-AzureRmAvailabilitySet теперь может выводить список всех групп доступности в подписке.</span><span class="sxs-lookup"><span data-stu-id="47dbf-626">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="47dbf-627">(Параметр ResouceGroupName теперь является необязательным.)</span><span class="sxs-lookup"><span data-stu-id="47dbf-627">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="47dbf-628">Обновлен параметр SimpleParameterSet командлета New-AzureRmVm, что позволило использовать ускоренную сеть на соответствующих виртуальных машинах.</span><span class="sxs-lookup"><span data-stu-id="47dbf-628">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="47dbf-629">Обновлен простой набор параметров New-AzureRmVmss, что позволило отменять создание масштабируемого набора виртуальных машин, если указанная пользователем подсистема балансировки нагрузки уже существует.</span><span class="sxs-lookup"><span data-stu-id="47dbf-629">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="47dbf-630">Обновлен пример для New-AzureRmDisk.</span><span class="sxs-lookup"><span data-stu-id="47dbf-630">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="47dbf-631">Добавлен пример для New-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="47dbf-631">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="47dbf-632">Обновлено описание командлета Set-AzureRmVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="47dbf-632">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="47dbf-633">Обновлен пример 1 для Set-AzureRmVMBginfoExtension: исправлены орфографические ошибки и префикс.</span><span class="sxs-lookup"><span data-stu-id="47dbf-633">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="47dbf-634">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="47dbf-634">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="47dbf-635">Пакет .NET SDK для ADF обновлен до версии 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="47dbf-635">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="47dbf-636">Добавлена поддержка совместного использования локальной среды IR несколькими фабриками данных.</span><span class="sxs-lookup"><span data-stu-id="47dbf-636">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="47dbf-637">Добавлен новый параметр -SharedIntegrationRuntimeResourceId для командлета Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-637">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="47dbf-638">Добавлен новый необязательный параметр -LinkedDataFactoryName для командлета Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="47dbf-638">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="47dbf-639">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="47dbf-639">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="47dbf-640">Пакет SDK для плоскости данных (Microsoft.Azure.DataLake.Store) обновлен до версии 1.1.9.</span><span class="sxs-lookup"><span data-stu-id="47dbf-640">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="47dbf-641">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="47dbf-641">AzureRM.EventHub</span></span>
* <span data-ttu-id="47dbf-642">Обновлена конвейерная передача для InputObject и ResourceId в командлетах remove.</span><span class="sxs-lookup"><span data-stu-id="47dbf-642">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="47dbf-643">AzureRM.Insights;</span><span class="sxs-lookup"><span data-stu-id="47dbf-643">AzureRM.Insights</span></span>
* <span data-ttu-id="47dbf-644">Исправлено форматирование OutputType в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="47dbf-644">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="47dbf-645">Применен пакет SDK Microsoft.Azure.Management.Monitor 0.19.1-preview.</span><span class="sxs-lookup"><span data-stu-id="47dbf-645">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="47dbf-646">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="47dbf-646">AzureRM.KeyVault</span></span>
* <span data-ttu-id="47dbf-647">Исправлена проблема с конвейерной передачей в командлете Set-AzureRmKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="47dbf-647">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="47dbf-648">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="47dbf-648">AzureRM.Network</span></span>
* <span data-ttu-id="47dbf-649">Добавлены примеры для командлетов LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="47dbf-649">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="47dbf-650">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="47dbf-650">AzureRM.Resources</span></span>
* <span data-ttu-id="47dbf-651">Устранена проблема, возникавшая при указании имени и значения тега для Get-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="47dbf-651">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="47dbf-652">Исправлен сценарий конвейерной передачи в Set-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="47dbf-652">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="47dbf-653">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="47dbf-653">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="47dbf-654">Обновлена конвейерная передача для InputObject и ResourceId в командлетах remove.</span><span class="sxs-lookup"><span data-stu-id="47dbf-654">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="47dbf-655">Исправлено несколько ошибок.</span><span class="sxs-lookup"><span data-stu-id="47dbf-655">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="47dbf-656">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="47dbf-656">AzureRM.Sql</span></span>
* <span data-ttu-id="47dbf-657">Добавлена поддержка Advanced Threat Protection для сервера с помощью следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="47dbf-657">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="47dbf-658">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="47dbf-658">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="47dbf-659">Добавлена поддержка оценки уязвимостей с помощью следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="47dbf-659">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="47dbf-660">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings;</span><span class="sxs-lookup"><span data-stu-id="47dbf-660">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="47dbf-661">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline;</span><span class="sxs-lookup"><span data-stu-id="47dbf-661">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="47dbf-662">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan.</span><span class="sxs-lookup"><span data-stu-id="47dbf-662">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="47dbf-663">Исправлен пример для Remove-AzureRmSqlServerFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="47dbf-663">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="47dbf-664">Исправлена неправильная обработка даты и времени для базового языка и региональных параметров, отличных от США, в Get-AzureSqlSyncGroupLog.</span><span class="sxs-lookup"><span data-stu-id="47dbf-664">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="47dbf-665">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="47dbf-665">AzureRM.Storage</span></span>
* <span data-ttu-id="47dbf-666">В свойства типов выходных данных командлетов добавлен атрибут Ps1XmlAttribute.</span><span class="sxs-lookup"><span data-stu-id="47dbf-666">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="47dbf-667">Выходные данные командлетов StorageAccount теперь отображаются в виде таблицы.</span><span class="sxs-lookup"><span data-stu-id="47dbf-667">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="47dbf-668">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="47dbf-668">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="47dbf-669">New-AzureRmStorageAccount;</span><span class="sxs-lookup"><span data-stu-id="47dbf-669">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="47dbf-670">Set-AzureRmStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="47dbf-670">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="47dbf-671">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="47dbf-671">AzureRM.Tags</span></span>
* <span data-ttu-id="47dbf-672">Удалено неверное утверждение из справки по командлетам Tag.</span><span class="sxs-lookup"><span data-stu-id="47dbf-672">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="47dbf-673">6.5.0 — июль 2018 г.</span><span class="sxs-lookup"><span data-stu-id="47dbf-673">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="47dbf-674">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="47dbf-674">AzureRM.Profile</span></span>
* <span data-ttu-id="47dbf-675">Обновлена справка для командлета Get-AzureRmContextAutosaveSetting.</span><span class="sxs-lookup"><span data-stu-id="47dbf-675">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="47dbf-676">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="47dbf-676">Azure.Storage</span></span>
* <span data-ttu-id="47dbf-677">Добавлена поддержка отправки BLOB-объекта или файла с помощью токена SAS, доступного только для записи.</span><span class="sxs-lookup"><span data-stu-id="47dbf-677">Support Upload Blob or File with write only Sas token</span></span>
* <span data-ttu-id="47dbf-678">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="47dbf-678">Set-AzureStorageBlobContent</span></span>
* <span data-ttu-id="47dbf-679">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="47dbf-679">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="47dbf-680">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="47dbf-680">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="47dbf-681">Для AS добавлено обязательное свойство ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="47dbf-681">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="47dbf-682">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="47dbf-682">AzureRM.Automation</span></span>
* <span data-ttu-id="47dbf-683">Обновлена справка и добавлены примеры для командлета New-AzureRMAutomationSchedule.</span><span class="sxs-lookup"><span data-stu-id="47dbf-683">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="47dbf-684">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="47dbf-684">AzureRM.Compute</span></span>
* <span data-ttu-id="47dbf-685">Добавлен параметр -Tag для командлета Update/New-AzureRmAvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="47dbf-685">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="47dbf-686">Добавлен пример для командлета Add-AzureRmVmssExtension.</span><span class="sxs-lookup"><span data-stu-id="47dbf-686">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="47dbf-687">Добавлены примеры для командлета Remove-AzureRmVmssExtension.</span><span class="sxs-lookup"><span data-stu-id="47dbf-687">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="47dbf-688">Обновлена справка для командлета Set-AzureRmVMAccessExtension.</span><span class="sxs-lookup"><span data-stu-id="47dbf-688">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="47dbf-689">Изменен класс SimpleParameterSet для командлета New-AzureRmVmss: теперь для SinglePlacementGroup по умолчанию задается значение false, а также добавляется параметр-переключатель SinglePlacementGroup, который позволяет пользователю создать VMSS в одной группе размещения.</span><span class="sxs-lookup"><span data-stu-id="47dbf-689">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="47dbf-690">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="47dbf-690">AzureRM.EventHub</span></span>
* <span data-ttu-id="47dbf-691">В класс PSEventHubDRConfigurationAttributes добавлено доступное только для чтения свойство PendingReplicationOperationsCount, которое показывает количество ожидающих репликации операций во время реплицирования.</span><span class="sxs-lookup"><span data-stu-id="47dbf-691">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="47dbf-692">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="47dbf-692">AzureRM.KeyVault</span></span>
* <span data-ttu-id="47dbf-693">Обновлено сообщение об ошибке для командлета Set-AzureRmKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="47dbf-693">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="47dbf-694">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="47dbf-694">AzureRM.LogicApp</span></span>
* <span data-ttu-id="47dbf-695">Исправлена ошибка "parameter set could not be resolved" (не удалось разрешить заданный параметр) в командлете New-AzureRmLogicApp.</span><span class="sxs-lookup"><span data-stu-id="47dbf-695">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="47dbf-696">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="47dbf-696">AzureRM.Network</span></span>
* <span data-ttu-id="47dbf-697">Включен пиринг между виртуальными сетями в нескольких клиентах для командлета Set/Add-AzureRmVirtualNetworkPeering.</span><span class="sxs-lookup"><span data-stu-id="47dbf-697">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="47dbf-698">Для шлюза приложений обновлены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="47dbf-698">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="47dbf-699">New-AzureRmApplicationGateway: добавлен флаг EnableFIPS и поддержка зон.</span><span class="sxs-lookup"><span data-stu-id="47dbf-699">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="47dbf-700">New-AzureRmApplicationGatewaySku: добавлены новые номера SKU Standard_v2 и WAF_v2.</span><span class="sxs-lookup"><span data-stu-id="47dbf-700">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="47dbf-701">Set-AzureRmApplicationGatewaySku: добавлены новые номера SKU Standard_v2 и WAF_v2.</span><span class="sxs-lookup"><span data-stu-id="47dbf-701">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="47dbf-702">Командлеты RouteTable пересозданы в последней версии генератора.</span><span class="sxs-lookup"><span data-stu-id="47dbf-702">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="47dbf-703">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="47dbf-703">AzureRM.Relay</span></span>
* <span data-ttu-id="47dbf-704">Обновлены файлы Markdown, исправлена проблема с именем параметра в примере.</span><span class="sxs-lookup"><span data-stu-id="47dbf-704">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="47dbf-705">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="47dbf-705">AzureRM.Resources</span></span>
* <span data-ttu-id="47dbf-706">Обновлены командлеты Roleassignment и roledefinition:</span><span class="sxs-lookup"><span data-stu-id="47dbf-706">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="47dbf-707">Удалены лишние вызовы roledefinition, выполняемые в ходе разбиения на страницы.</span><span class="sxs-lookup"><span data-stu-id="47dbf-707">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="47dbf-708">Исправлен командлет Get-AzureRmRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="47dbf-708">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="47dbf-709">Исправлена работа параметра -ExpandPrincipalGroups.</span><span class="sxs-lookup"><span data-stu-id="47dbf-709">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="47dbf-710">Устранена проблема в командлете Get-AzureRmResource, заключающая в том, что в параметре -ResourceType учитывался регистр символов.</span><span class="sxs-lookup"><span data-stu-id="47dbf-710">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="47dbf-711">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="47dbf-711">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="47dbf-712">Добавлены параметры top и skip для командлетов list.</span><span class="sxs-lookup"><span data-stu-id="47dbf-712">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="47dbf-713">Добавлены командлеты для перехода с пространства имен ценовой категории "Стандартный" на пространство ценовой категории "Премиум":</span><span class="sxs-lookup"><span data-stu-id="47dbf-713">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="47dbf-714">Start-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="47dbf-714">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="47dbf-715">Get-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="47dbf-715">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="47dbf-716">Complete-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="47dbf-716">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="47dbf-717">Stop-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="47dbf-717">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="47dbf-718">Remove-AzureRmServiceBusMigration.</span><span class="sxs-lookup"><span data-stu-id="47dbf-718">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="47dbf-719">В класс PSServiceBusDRConfigurationAttributes добавлено доступное только для чтения свойство PendingReplicationOperationsCount, которое показывает количество ожидающих репликации операций во время реплицирования.</span><span class="sxs-lookup"><span data-stu-id="47dbf-719">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="47dbf-720">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="47dbf-720">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="47dbf-721">Обновлен пример для командлета New-AzureRmServiceFabricCluster.</span><span class="sxs-lookup"><span data-stu-id="47dbf-721">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="47dbf-722">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="47dbf-722">AzureRM.Sql</span></span>
* <span data-ttu-id="47dbf-723">Добавлены новые командлеты для Management.Sql, позволяющие клиентам добавлять сертификат TDE в экземпляр SQL Server или управляемый экземпляр:</span><span class="sxs-lookup"><span data-stu-id="47dbf-723">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="47dbf-724">Add-AzureRmSqlServerTransparentDataEncryptionCertificate;</span><span class="sxs-lookup"><span data-stu-id="47dbf-724">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="47dbf-725">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate.</span><span class="sxs-lookup"><span data-stu-id="47dbf-725">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="47dbf-726">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="47dbf-726">AzureRM.Websites</span></span>
* <span data-ttu-id="47dbf-727">`Set-AzureRmWebApp -AssignIdentity` и `Set-AzureRmWebAppSlot -AssignIdentity` при установленном значении false теперь будут удалять свойство Identity из объекта сайта. Также при этом будет удаляться тег предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="47dbf-727">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="47dbf-728">Обновлен пример для `Get-AzureRmWebAppMetrics` и `Get-AzureRmAppServicePlanMetrics`.</span><span class="sxs-lookup"><span data-stu-id="47dbf-728">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="47dbf-729">`Set-AzureRmWebApp -PhpVersion` теперь поддерживает off как допустимую версию PHP.</span><span class="sxs-lookup"><span data-stu-id="47dbf-729">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="47dbf-730">6.4.0 — июль 2018 г.</span><span class="sxs-lookup"><span data-stu-id="47dbf-730">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="47dbf-731">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="47dbf-731">General</span></span>
* <span data-ttu-id="47dbf-732">Исправлено форматирование OutputType в файлах справки для большинства модулей.</span><span class="sxs-lookup"><span data-stu-id="47dbf-732">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="47dbf-733">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="47dbf-733">AzureRM.Profile</span></span>
* <span data-ttu-id="47dbf-734">В основные типы выходных данных добавлен атрибут Ps1Xml.</span><span class="sxs-lookup"><span data-stu-id="47dbf-734">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="47dbf-735">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="47dbf-735">AzureRM.Compute</span></span>
* <span data-ttu-id="47dbf-736">Функция добавления тега IP-адреса для масштабируемого набора виртуальных машин (VMSS)</span><span class="sxs-lookup"><span data-stu-id="47dbf-736">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="47dbf-737">Добавлен командлет New-AzureRmVmssIpTagConfig.</span><span class="sxs-lookup"><span data-stu-id="47dbf-737">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="47dbf-738">В New-AzureRmVmssIpConfig добавлен параметр IpTag.</span><span class="sxs-lookup"><span data-stu-id="47dbf-738">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="47dbf-739">Функция автоматического отката ОС для VMSS</span><span class="sxs-lookup"><span data-stu-id="47dbf-739">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="47dbf-740">В New-AzureRmVmssConfig и Update-AzureRmVmss добавлены параметры DisableAutoRollback.</span><span class="sxs-lookup"><span data-stu-id="47dbf-740">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="47dbf-741">Функция ведения журнала обновлений ОС для VMSS</span><span class="sxs-lookup"><span data-stu-id="47dbf-741">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="47dbf-742">В Get-AzureRmVmss добавлен параметр OSUpgradeHistory.</span><span class="sxs-lookup"><span data-stu-id="47dbf-742">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="47dbf-743">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="47dbf-743">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="47dbf-744">Добавлена поддержка списков управления доступом к каталогу с использованием следующих команд:</span><span class="sxs-lookup"><span data-stu-id="47dbf-744">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="47dbf-745">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry;</span><span class="sxs-lookup"><span data-stu-id="47dbf-745">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="47dbf-746">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry;</span><span class="sxs-lookup"><span data-stu-id="47dbf-746">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="47dbf-747">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="47dbf-747">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="47dbf-748">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="47dbf-748">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="47dbf-749">Добавлены поддержка отмены выполнения и отслеживание хода выполнения для Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl и Remove-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="47dbf-749">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="47dbf-750">Добавлена поддержка отмены выполнения для Export-AzureRmDataLakeStoreChildItemProperties.</span><span class="sxs-lookup"><span data-stu-id="47dbf-750">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="47dbf-751">Исправлена очистка сообщений об отладке для командлетов, которые выполняют рекурсивные операции.</span><span class="sxs-lookup"><span data-stu-id="47dbf-751">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="47dbf-752">Исправлено расположение тестовых данных для командлетов DataLake.</span><span class="sxs-lookup"><span data-stu-id="47dbf-752">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="47dbf-753">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="47dbf-753">AzureRM.EventHub</span></span>
* <span data-ttu-id="47dbf-754">Для командлетов вывода списка операций Get-AzureRmEventHub и Get-AzureRmEventHubConsumerGroup добавлен необязательный параметр MaxCount.</span><span class="sxs-lookup"><span data-stu-id="47dbf-754">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="47dbf-755">Исправлена проблема с командлетом New-AzureRmEventHub, из-за которой требовалось указать по крайней мере один параметр при создании концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="47dbf-755">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="47dbf-756">Добавлен набор параметров по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="47dbf-756">Provided Default Parameter set.</span></span>
* <span data-ttu-id="47dbf-757">Для командлета New-AzureRmEventHubKey добавлен необязательный параметр -KeyValue, который позволяет пользователю предоставить значение ключа.</span><span class="sxs-lookup"><span data-stu-id="47dbf-757">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="47dbf-758">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="47dbf-758">AzureRM.KeyVault</span></span>
* <span data-ttu-id="47dbf-759">Исправлена ошибка, из-за которой при выполнении командлета Get-AzureRmKeyVault с параметром -Tag возвращались все ресурсы.</span><span class="sxs-lookup"><span data-stu-id="47dbf-759">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="47dbf-760">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="47dbf-760">AzureRM.Network</span></span>
* <span data-ttu-id="47dbf-761">Для параметра шлюзов виртуальной вести, избыточных между зонами, предоставлены новые номера SKU.</span><span class="sxs-lookup"><span data-stu-id="47dbf-761">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="47dbf-762">Добавлены новые команды для функции API партнеров ExpressRoute (ARM):</span><span class="sxs-lookup"><span data-stu-id="47dbf-762">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="47dbf-763">добавлена команда Get-AzureRmExpressRouteCrossConnection;</span><span class="sxs-lookup"><span data-stu-id="47dbf-763">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="47dbf-764">добавлена команда Set-AzureRmExpressRouteCrossConnection;</span><span class="sxs-lookup"><span data-stu-id="47dbf-764">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="47dbf-765">добавлена команда Add-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="47dbf-765">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="47dbf-766">добавлена команда Get-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="47dbf-766">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="47dbf-767">добавлена команда Remove-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="47dbf-767">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="47dbf-768">добавлена команда Get-AzureRMExpressRouteCrossConnectionArpTable;</span><span class="sxs-lookup"><span data-stu-id="47dbf-768">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="47dbf-769">добавлена команда Get-AzureRMExpressRouteCrossConnectionRouteTable;</span><span class="sxs-lookup"><span data-stu-id="47dbf-769">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="47dbf-770">добавлена команда Get-AzureRMExpressRouteCrossConnectionRouteTableSummary.</span><span class="sxs-lookup"><span data-stu-id="47dbf-770">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="47dbf-771">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="47dbf-771">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="47dbf-772">Добавлен командлет Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="47dbf-772">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="47dbf-773">Этот командлет принимает идентификатор виртуальной машины и проверяет, защищена ли виртуальная машина с помощью какого-либо хранилища в подписке.</span><span class="sxs-lookup"><span data-stu-id="47dbf-773">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="47dbf-774">Если такое хранилище существует, командлет выводит данные о нем.</span><span class="sxs-lookup"><span data-stu-id="47dbf-774">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="47dbf-775">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="47dbf-775">AzureRM.Resources</span></span>
* <span data-ttu-id="47dbf-776">Обновлены командлеты Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="47dbf-776">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="47dbf-777">Добавлена поддержка вывода списка значений параметра -Scope на уровне группы управления.</span><span class="sxs-lookup"><span data-stu-id="47dbf-777">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="47dbf-778">Добавлена поддержка для получения отдельных назначений со значениями -Scope на уровне группы управления.</span><span class="sxs-lookup"><span data-stu-id="47dbf-778">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="47dbf-779">Для параметра управления добавлены параметры -Effective и -All.</span><span class="sxs-lookup"><span data-stu-id="47dbf-779">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="47dbf-780">Обновлены командлеты Get/New/Remove/Set-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="47dbf-780">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="47dbf-781">Добавлен параметр -ManagementGroupName для применения операций к заданной группе управления.</span><span class="sxs-lookup"><span data-stu-id="47dbf-781">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="47dbf-782">Добавлен параметр -SubscriptionId для применения операций к заданной подписке.</span><span class="sxs-lookup"><span data-stu-id="47dbf-782">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="47dbf-783">Обновлены командлеты Get/New/Remove/Set-AzureRmPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="47dbf-783">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="47dbf-784">Добавлен параметр -ManagementGroupName для применения операций к заданной группе управления.</span><span class="sxs-lookup"><span data-stu-id="47dbf-784">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="47dbf-785">Добавлен параметр -SubscriptionId для применения операций к заданной подписке.</span><span class="sxs-lookup"><span data-stu-id="47dbf-785">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="47dbf-786">Добавлена поддержка ссылок на секрет KeyVault в параметрах при использовании TemplateParameterObject в New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="47dbf-786">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="47dbf-787">Устранена проблема, из-за которой параметр -EndDate игнорировался в New-AzureRmADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="47dbf-787">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="47dbf-788">Устранена проблема, из-за которой в Add-AzureRmADGroupMember использовался неверный URL-адрес для запроса.</span><span class="sxs-lookup"><span data-stu-id="47dbf-788">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="47dbf-789">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="47dbf-789">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="47dbf-790">Для командлета New-AzureRmServiceBusKey добавлен необязательный параметр -KeyValue, который позволяет пользователю предоставить значение ключа.</span><span class="sxs-lookup"><span data-stu-id="47dbf-790">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="47dbf-791">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="47dbf-791">AzureRM.Sql</span></span>
* <span data-ttu-id="47dbf-792">В справке по New-AzureRmSqlDatabaseRestorePoint добавлено описание определяемых пользователем точек восстановления для хранилища данных SQL.</span><span class="sxs-lookup"><span data-stu-id="47dbf-792">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="47dbf-793">Обновлена документация по параметру -ComputeGeneration, используемого в нескольких командлетах.</span><span class="sxs-lookup"><span data-stu-id="47dbf-793">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="47dbf-794">6.3.0 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="47dbf-794">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="47dbf-795">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="47dbf-795">AzureRM.Profile</span></span>
* <span data-ttu-id="47dbf-796">Обновлены сообщения об ошибках для Enable-AzureRmContextAutoSave.</span><span class="sxs-lookup"><span data-stu-id="47dbf-796">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="47dbf-797">Создание контекста для каждой подписки при выполнении Connect-AzureRmAccount без предыдущего контекста.</span><span class="sxs-lookup"><span data-stu-id="47dbf-797">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="47dbf-798">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="47dbf-798">Azure.Storage</span></span>
* <span data-ttu-id="47dbf-799">В файлы справки добавлены дополнительные сведения о параметре -Permissions.</span><span class="sxs-lookup"><span data-stu-id="47dbf-799">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="47dbf-800">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="47dbf-800">AzureRM.Compute</span></span>
* <span data-ttu-id="47dbf-801">Get-AzureRmVmDiskEncryptionStatus устраняет проблему, которая наблюдалась на виртуальных машинах без дисков данных.</span><span class="sxs-lookup"><span data-stu-id="47dbf-801">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="47dbf-802">Обновлена версия клиентской библиотеки Compute для исправления следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="47dbf-802">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="47dbf-803">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="47dbf-803">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="47dbf-804">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="47dbf-804">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="47dbf-805">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="47dbf-805">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="47dbf-806">В следующих командлетах исправлено отображение неправильных значений operation ID и operation status:</span><span class="sxs-lookup"><span data-stu-id="47dbf-806">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="47dbf-807">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="47dbf-807">Start-AzureRmVM</span></span>
    - <span data-ttu-id="47dbf-808">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="47dbf-808">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="47dbf-809">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="47dbf-809">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="47dbf-810">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="47dbf-810">Set-AzureRmVM</span></span>
    - <span data-ttu-id="47dbf-811">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="47dbf-811">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="47dbf-812">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="47dbf-812">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="47dbf-813">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="47dbf-813">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="47dbf-814">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="47dbf-814">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="47dbf-815">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="47dbf-815">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="47dbf-816">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="47dbf-816">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="47dbf-817">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="47dbf-817">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="47dbf-818">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="47dbf-818">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="47dbf-819">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="47dbf-819">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="47dbf-820">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="47dbf-820">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="47dbf-821">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="47dbf-821">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="47dbf-822">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="47dbf-822">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="47dbf-823">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="47dbf-823">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="47dbf-824">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="47dbf-824">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="47dbf-825">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="47dbf-825">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="47dbf-826">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="47dbf-826">AzureRM.EventGrid</span></span>
* <span data-ttu-id="47dbf-827">Удалены условия проверки ValidateNotNullOrEmpty для SubjectBeginsWith/SubjectEndsWith в командлете Update-AzureRmEventGridSubscription, что позволяет при необходимости заменять эти параметры пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="47dbf-827">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="47dbf-828">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="47dbf-828">AzureRM.KeyVault</span></span>
* <span data-ttu-id="47dbf-829">Исправлена ошибка, когда при выполнении командлета Get-AzureRmKeyVault -Tag не возвращается ни один тег.</span><span class="sxs-lookup"><span data-stu-id="47dbf-829">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="47dbf-830">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="47dbf-830">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="47dbf-831">Общедоступный выпуск командлетов Policy Insights.</span><span class="sxs-lookup"><span data-stu-id="47dbf-831">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="47dbf-832">Используется API версии 2018-04-04.</span><span class="sxs-lookup"><span data-stu-id="47dbf-832">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="47dbf-833">К результатам Get-AzureRmPolicyStateSummary добавлено PolicyDefinitionReferenceId.</span><span class="sxs-lookup"><span data-stu-id="47dbf-833">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="47dbf-834">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="47dbf-834">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="47dbf-835">Для командлетов RecoveryServices.Backup добавлен параметр -Vault.</span><span class="sxs-lookup"><span data-stu-id="47dbf-835">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="47dbf-836">Передача этого параметра переопределяет командлет Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="47dbf-836">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="47dbf-837">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="47dbf-837">AzureRM.Sql</span></span>
* <span data-ttu-id="47dbf-838">В файле справки обновлен пример для командлета Get-AzureRmSqlDatabaseExpanded.</span><span class="sxs-lookup"><span data-stu-id="47dbf-838">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="47dbf-839">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="47dbf-839">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="47dbf-840">Обновлен файл справки для командлета Add-AzureRmTrafficManagerEndpointConfig.</span><span class="sxs-lookup"><span data-stu-id="47dbf-840">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="47dbf-841">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="47dbf-841">AzureRM.Websites</span></span>
* <span data-ttu-id="47dbf-842">Изменено действие командлета Set-AzureRmWebApp. Теперь он не перезаписывает AppSettings, если используется параметр -AssignIdentity.</span><span class="sxs-lookup"><span data-stu-id="47dbf-842">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="47dbf-843">Командлет New-AzureRmWebAppSlot теперь учитывает дополнительный параметр AppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="47dbf-843">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="47dbf-844">6.2.1 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="47dbf-844">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="47dbf-845">AzureRM.OperationalInsights;</span><span class="sxs-lookup"><span data-stu-id="47dbf-845">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="47dbf-846">В обновленной модели PSWorkspace Network может использовать type в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="47dbf-846">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="47dbf-847">6.2.0 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="47dbf-847">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="47dbf-848">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="47dbf-848">AzureRM.Profile</span></span>
* <span data-ttu-id="47dbf-849">Исправлена ошибка с загрузкой Newtonsoft.Json версии 10.0.3 во время импорта модуля.</span><span class="sxs-lookup"><span data-stu-id="47dbf-849">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="47dbf-850">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="47dbf-850">AzureRM.Compute</span></span>
* <span data-ttu-id="47dbf-851">Функция обновления виртуальных машин VMSS.</span><span class="sxs-lookup"><span data-stu-id="47dbf-851">VMSS VM Update feature</span></span>
    - <span data-ttu-id="47dbf-852">Добавлены командлеты Update-AzureRmVmssVM и New-AzureRmVMDataDisk.</span><span class="sxs-lookup"><span data-stu-id="47dbf-852">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="47dbf-853">В командлет Add-AzureRmVMDataDisk добавлен параметр VirtualMachineScaleSetVM, который позволяет добавлять диски данных в виртуальные машины VMSS.</span><span class="sxs-lookup"><span data-stu-id="47dbf-853">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="47dbf-854">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="47dbf-854">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="47dbf-855">Пакет SDK для ADF .NET обновлен до версии 0.8.0-preview. Новая версия содержит такие изменения:</span><span class="sxs-lookup"><span data-stu-id="47dbf-855">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="47dbf-856">добавлена операция для настройки репозитория фабрики;</span><span class="sxs-lookup"><span data-stu-id="47dbf-856">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="47dbf-857">связанная служба QuickBooks LinkedService теперь предоставляет свойства consumerKey и consumerSecret;</span><span class="sxs-lookup"><span data-stu-id="47dbf-857">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="47dbf-858">тип нескольких моделей изменен с SecretBase на Object;</span><span class="sxs-lookup"><span data-stu-id="47dbf-858">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="47dbf-859">добавлен триггер событий BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="47dbf-859">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="47dbf-860">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="47dbf-860">AzureRM.KeyVault</span></span>
* <span data-ttu-id="47dbf-861">В документацию добавлены примеры выходных данных.</span><span class="sxs-lookup"><span data-stu-id="47dbf-861">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="47dbf-862">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="47dbf-862">AzureRM.Network</span></span>
* <span data-ttu-id="47dbf-863">В командлеты Наблюдателя за сетями добавлены параметры Аналитики трафика.</span><span class="sxs-lookup"><span data-stu-id="47dbf-863">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="47dbf-864">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="47dbf-864">AzureRM.Resources</span></span>
* <span data-ttu-id="47dbf-865">Исправлена ошибка, когда командлет Get-AzureRmResource возвращает свойство Properties объектов PSResource.</span><span class="sxs-lookup"><span data-stu-id="47dbf-865">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="47dbf-866">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="47dbf-866">AzureRM.Scheduler</span></span>
* <span data-ttu-id="47dbf-867">Исправлена ошибка, когда обновление ServiceBusQueueJob не задает новые значения для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="47dbf-867">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="47dbf-868">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="47dbf-868">AzureRM.Sql</span></span>
* <span data-ttu-id="47dbf-869">В перечисленные ниже командлеты добавлен необязательный параметр LicenseType.</span><span class="sxs-lookup"><span data-stu-id="47dbf-869">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="47dbf-870">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="47dbf-870">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="47dbf-871">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool;</span><span class="sxs-lookup"><span data-stu-id="47dbf-871">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="47dbf-872">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="47dbf-872">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="47dbf-873">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="47dbf-873">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="47dbf-874">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="47dbf-874">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="47dbf-875">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="47dbf-875">AzureRM.Websites</span></span>
* <span data-ttu-id="47dbf-876">Командлет New-AzureRMWebApp теперь использует общие алгоритмы из библиотеки Strategy.</span><span class="sxs-lookup"><span data-stu-id="47dbf-876">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="47dbf-877">6.1.0 — май 2018 г.</span><span class="sxs-lookup"><span data-stu-id="47dbf-877">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="47dbf-878">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="47dbf-878">AzureRM.Profile</span></span>
* <span data-ttu-id="47dbf-879">Устранена проблема с выполнением Clear-AzureRmContext, при которой сохранялся пустой контекст с именем предыдущего контекста по умолчанию, что не позволяло пользователю создать новый контекст со старым именем.</span><span class="sxs-lookup"><span data-stu-id="47dbf-879">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="47dbf-880">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="47dbf-880">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="47dbf-881">Включены операции связывания и отмены связи в автономной системе.</span><span class="sxs-lookup"><span data-stu-id="47dbf-881">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="47dbf-882">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="47dbf-882">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="47dbf-883">Добавлена поддержка ApiVersions, ApiReleases и ApiRevisions.</span><span class="sxs-lookup"><span data-stu-id="47dbf-883">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="47dbf-884">Добавлена поддержка серверной части ServiceFabric.</span><span class="sxs-lookup"><span data-stu-id="47dbf-884">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="47dbf-885">Добавлена поддержка средства ведения журнала Application Insights.</span><span class="sxs-lookup"><span data-stu-id="47dbf-885">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="47dbf-886">Добавлена поддержка для распознавания номера SKU уровня "Базовый" как допустимого номера SKU службы управления API.</span><span class="sxs-lookup"><span data-stu-id="47dbf-886">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="47dbf-887">Добавлена поддержка установки сертификатов, выданных частным центром сертификации в качестве корневого или обычного ЦС.</span><span class="sxs-lookup"><span data-stu-id="47dbf-887">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="47dbf-888">Добавлена поддержка для приема пользовательских SSL-сертификатов с помощью KeyVault и нескольких имен узлов прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="47dbf-888">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="47dbf-889">Добавлена поддержка для удостоверения MSI.</span><span class="sxs-lookup"><span data-stu-id="47dbf-889">Added support for MSI identity</span></span>
* <span data-ttu-id="47dbf-890">Добавлена поддержка для принятия политик с помощью URL-адреса. Примечание. Указанные ниже командлеты в следующем выпуске будут отмечены как нерекомендуемые:</span><span class="sxs-lookup"><span data-stu-id="47dbf-890">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="47dbf-891">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="47dbf-891">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="47dbf-892">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="47dbf-892">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="47dbf-893">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="47dbf-893">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="47dbf-894">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="47dbf-894">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="47dbf-895">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="47dbf-895">AzureRM.Batch</span></span>
* <span data-ttu-id="47dbf-896">Выпущен новый командлет Get-AzureBatchPoolNodeCounts.</span><span class="sxs-lookup"><span data-stu-id="47dbf-896">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="47dbf-897">Выпущен новый командлет Start-AzureBatchComputeNodeServiceLogUpload.</span><span class="sxs-lookup"><span data-stu-id="47dbf-897">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="47dbf-898">AzureRM.Consumption:</span><span class="sxs-lookup"><span data-stu-id="47dbf-898">AzureRM.Consumption</span></span>
* <span data-ttu-id="47dbf-899">Добавлены новые параметры Expand, ResourceGroup, InstanceName, InstanceId, Tags и командлет высшего уровня Get-AzureRmConsumptionUsageDetail.</span><span class="sxs-lookup"><span data-stu-id="47dbf-899">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="47dbf-900">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="47dbf-900">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="47dbf-901">Исправлен пример для Export-AzureRmDataLakeStoreChildItemProperties.</span><span class="sxs-lookup"><span data-stu-id="47dbf-901">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="47dbf-902">Исправлено исключение параметра NULL при использовании рекурсии в Set-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="47dbf-902">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="47dbf-903">Исправлены файлы справки для Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl и Remove-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="47dbf-903">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="47dbf-904">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="47dbf-904">AzureRM.Network</span></span>
* <span data-ttu-id="47dbf-905">Пакет SDK для сети обновлен с предварительной версии 18.0.0 до предварительной версии 19.0.0.</span><span class="sxs-lookup"><span data-stu-id="47dbf-905">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="47dbf-906">Добавлен командлет для создания конфигурации протокола.</span><span class="sxs-lookup"><span data-stu-id="47dbf-906">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="47dbf-907">New-AzureRmNetworkWatcherProtocolConfiguration.</span><span class="sxs-lookup"><span data-stu-id="47dbf-907">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="47dbf-908">Добавлен командлет для добавления нового подключения канала к существующему каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="47dbf-908">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="47dbf-909">Add-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="47dbf-909">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="47dbf-910">Добавлен командлет для удаления подключения канала к существующему каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="47dbf-910">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="47dbf-911">Remove-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="47dbf-911">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="47dbf-912">Добавлен командлет для получения подключения канала.</span><span class="sxs-lookup"><span data-stu-id="47dbf-912">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="47dbf-913">Get-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="47dbf-913">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="47dbf-914">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="47dbf-914">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="47dbf-915">Исправлена процедура аутентификации сервера с использованием созданных сертификатов (проблема № 5998).</span><span class="sxs-lookup"><span data-stu-id="47dbf-915">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="47dbf-916">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="47dbf-916">AzureRM.Sql</span></span>
* <span data-ttu-id="47dbf-917">Обновлены командлеты аудита, которые теперь позволяют удалять AuditActions или AuditActionGroups.</span><span class="sxs-lookup"><span data-stu-id="47dbf-917">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="47dbf-918">Исправлена проблема с Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy, при которой установка новой гибкой политики хранения завершалась ошибкой с сообщением "Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span><span class="sxs-lookup"><span data-stu-id="47dbf-918">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="47dbf-919">Please submit request with the new flexible retention policy" (Настройка политики долгосрочного хранения с помощью хранилища и политики служб восстановления Azure больше не поддерживается. Отправьте запрос с использованием новой гибкой политики хранения).</span><span class="sxs-lookup"><span data-stu-id="47dbf-919">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="47dbf-920">Обновлены все командлеты, связанные со службой "База данных SQL Azure", с созданием эластичных пулов и обновлением. Теперь используются новые API баз данных с поддержкой свойства номеров SKU для обеспечения масштабируемости и связанных с уровнями возможностей.</span><span class="sxs-lookup"><span data-stu-id="47dbf-920">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="47dbf-921">Обновлены командлеты, в том числе:</span><span class="sxs-lookup"><span data-stu-id="47dbf-921">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="47dbf-922">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="47dbf-922">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="47dbf-923">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool;</span><span class="sxs-lookup"><span data-stu-id="47dbf-923">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="47dbf-924">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="47dbf-924">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="47dbf-925">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="47dbf-925">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="47dbf-926">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="47dbf-926">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="47dbf-927">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="47dbf-927">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="47dbf-928">Обновлены параметры для Get-AzureRmTrafficManagerProfile. Теперь при использовании параметра -Name требуется параметр -ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="47dbf-928">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
