---
title: "Журнал изменений Azure PowerShell | Документация Майкрософт"
description: "Это руководство содержит историю изменений Azure PowerShell, внесенных в новом выпуске."
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: 
ms.date: 05/18/2017
ms.openlocfilehash: 04f89e8d47d0825d46cb1b8817efbcc0cafa0acd
ms.sourcegitcommit: 226527be7cb647acfe2ea9ab151185053ab3c6db
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/29/2017
---
# <a name="release-notes"></a><span data-ttu-id="77c40-103">Заметки о выпуске</span><span class="sxs-lookup"><span data-stu-id="77c40-103">Release notes</span></span>

<span data-ttu-id="77c40-104">Здесь приведен список изменений, внесенных в Azure PowerShell в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="77c40-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-380"></a><span data-ttu-id="77c40-105">Версия 3.8.0</span><span class="sxs-lookup"><span data-stu-id="77c40-105">Version 3.8.0</span></span>
* <span data-ttu-id="77c40-106">Среда выполнения приложений</span><span class="sxs-lookup"><span data-stu-id="77c40-106">Compute</span></span>
  - <span data-ttu-id="77c40-107">Исправлена ошибка в командлетах Get-*, чтобы можно было получить несколько страниц данных (более 120 элементов).</span><span class="sxs-lookup"><span data-stu-id="77c40-107">Fix bug in Get-* cmdlets, to allow retrieving multiple pages of data (more than 120 items)</span></span>
* <span data-ttu-id="77c40-108">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="77c40-108">DataLakeAnalytics</span></span>
  - <span data-ttu-id="77c40-109">Исправлена ошибка в справке некоторых команд для отображения корректной формулировки и примеров.</span><span class="sxs-lookup"><span data-stu-id="77c40-109">Fix help for some commands to have the proper verbage and examples.</span></span>
* <span data-ttu-id="77c40-110">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="77c40-110">DataLakeStore</span></span>
  - <span data-ttu-id="77c40-111">Добавлена поддержка начальной и конечной части командлета `Get-AzureRMDataLakeStoreItemContent`.</span><span class="sxs-lookup"><span data-stu-id="77c40-111">Add support for head and tail to the `Get-AzureRMDataLakeStoreItemContent` cmdlet.</span></span> <span data-ttu-id="77c40-112">Это гарантирует отображение строк с разделителями в новой строке при возврате значения "Первые N" или "Последние N".</span><span class="sxs-lookup"><span data-stu-id="77c40-112">This enables returning the top N or last N new line delimited rows to be displayed.</span></span>
* <span data-ttu-id="77c40-113">HDInsight</span><span class="sxs-lookup"><span data-stu-id="77c40-113">HDInsight</span></span>
  - <span data-ttu-id="77c40-114">Добавлена поддержка для типа кластера RServer.</span><span class="sxs-lookup"><span data-stu-id="77c40-114">Added support for RServer cluster type</span></span>
    + <span data-ttu-id="77c40-115">Вы можете указать размер виртуальной машины граничного узла для кластера RServer в командлете New-AzureRmHDInsightCluster или New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="77c40-115">Edgenode VM size can be specified for RServer cluster in New-AzureRmHDInsightCluster or New-AzureRmHDInsightClusterConfig</span></span>
    + <span data-ttu-id="77c40-116">RServer сейчас является параметром конфигурации в Add-AzureRmHDInsightConfigValues.</span><span class="sxs-lookup"><span data-stu-id="77c40-116">RServer is now a configuration option in Add-AzureRmHDInsightConfigValues.</span></span> <span data-ttu-id="77c40-117">Он позволяет настроить параметр RStudio, который указывает, что требуется выполнить установку R Studio.</span><span class="sxs-lookup"><span data-stu-id="77c40-117">It allows for RStudio flag to be set to indicate that R Studio installation should be done.</span></span>
* <span data-ttu-id="77c40-118">Приложение логики</span><span class="sxs-lookup"><span data-stu-id="77c40-118">LogicApp</span></span>
  - <span data-ttu-id="77c40-119">Исправлены командлеты Set-AzureRmIntegrationAccountSchema и Set-AzureRmIntegrationAccountMap для устранения ошибки свойства ContentLink (настройка свойств Content и ContentLink приводила к сбою при обновлении).</span><span class="sxs-lookup"><span data-stu-id="77c40-119">Set-AzureRmIntegrationAccountSchema and Set-AzureRmIntegrationAccountMap cmdlets are fixed for the contentlink issue(Both content and contentlink were set resulting in update failure).</span></span>
* <span data-ttu-id="77c40-120">Сеть</span><span class="sxs-lookup"><span data-stu-id="77c40-120">Network</span></span>
  - <span data-ttu-id="77c40-121">Добавлена поддержка новых функций брандмауэра веб-приложения в шлюзах приложений.</span><span class="sxs-lookup"><span data-stu-id="77c40-121">Added support for new web application firewall features to Application Gateways</span></span>
    + <span data-ttu-id="77c40-122">Добавлен командлет New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig.</span><span class="sxs-lookup"><span data-stu-id="77c40-122">Added New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>
    + <span data-ttu-id="77c40-123">Добавлен командлет Get-AzureRmApplicationGatewayAvailableWafRuleSets (псевдоним: List-AzureRmApplicationGatewayAvailableWafRuleSets).</span><span class="sxs-lookup"><span data-stu-id="77c40-123">Added Get-AzureRmApplicationGatewayAvailableWafRuleSets (Alias: List-AzureRmApplicationGatewayAvailableWafRuleSets)</span></span>
    + <span data-ttu-id="77c40-124">Обновлен командлет New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration: добавлены параметры -RuleSetType, -RuleSetVersion и -DisabledRuleGroups.</span><span class="sxs-lookup"><span data-stu-id="77c40-124">Updated New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration: Added parameter -RuleSetType -RuleSetVersion and -DisabledRuleGroups</span></span>
    + <span data-ttu-id="77c40-125">Обновлен командлет Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration: добавлены параметры -RuleSetType, -RuleSetVersion и -DisabledRuleGroups.</span><span class="sxs-lookup"><span data-stu-id="77c40-125">Updated Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration: Added parameter -RuleSetType -RuleSetVersion and -DisabledRuleGroups</span></span>
  - <span data-ttu-id="77c40-126">Добавлена поддержка политик IPSec для подключений шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="77c40-126">Added support for IPSec policies to Virtual Network Gateway Connections</span></span>
  - <span data-ttu-id="77c40-127">Добавлен командлет New-AzureRmIpsecPolicy.</span><span class="sxs-lookup"><span data-stu-id="77c40-127">Added New-AzureRmIpsecPolicy</span></span>
  - <span data-ttu-id="77c40-128">Обновлен командлет New-AzureRmVirtualNetworkGatewayConnection: добавлены параметры -IpsecPolicies и -UsePolicyBasedTrafficSelectors.</span><span class="sxs-lookup"><span data-stu-id="77c40-128">Updated New-AzureRmVirtualNetworkGatewayConnection: Added parameter -IpsecPolicies and -UsePolicyBasedTrafficSelectors</span></span>
* <span data-ttu-id="77c40-129">Профиль</span><span class="sxs-lookup"><span data-stu-id="77c40-129">Profile</span></span>
  - <span data-ttu-id="77c40-130">*Устарело*. Командлет Save-AzureRmProfile переименован в Save-AzureRmContext. Используется псевдоним для устаревшего имени командлета, который будет удален в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="77c40-130">*Obsolete*: Save-AzureRmProfile is renamed to Save-AzureRmContext, there is an alias to the old cmdlet name, the alias will be removed in the next release.</span></span>
  - <span data-ttu-id="77c40-131">*Устарело*. Командлет Select-AzureRmProfile переименован на Import-AzureRmContext. Используется псевдоним для устаревшего имени командлета, который будет удален в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="77c40-131">*Obsolete*: Select-AzureRmProfile is renamed to Import-AzureRmContext, there is an alias to the old cmdlet name, the alias will be removed in the next release.</span></span>
  - <span data-ttu-id="77c40-132">Типы выходных данных командлетов профиля PSAzureContext и PSAzureProfile изменятся в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="77c40-132">The PSAzureContext and PSAzureProfile output types of profile cmdlets will be changed in the next release.</span></span>
  - <span data-ttu-id="77c40-133">Командлет Save-AzureRmContext не будет включать параметр OutputType в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="77c40-133">The Save-AzureRmContext cmdlet will have no OutputType in the next release.</span></span>
  - <span data-ttu-id="77c40-134">Исправлена ошибка в общем коде командлета для использования FIPS-совместимого алгоритма для хэша данных: https://github.com/Azure/azure-powershell/issues/3651.</span><span class="sxs-lookup"><span data-stu-id="77c40-134">Fix bug in cmdlet common code to use FIPS-compliant algorithm for data hashes: https://github.com/Azure/azure-powershell/issues/3651</span></span>
* <span data-ttu-id="77c40-135">SQL</span><span class="sxs-lookup"><span data-stu-id="77c40-135">Sql</span></span>
  - <span data-ttu-id="77c40-136">Исправлены ошибки в командлетах групп отработки отказа Azure.</span><span class="sxs-lookup"><span data-stu-id="77c40-136">Bug fixes on Azure Failover Group Cmdlets</span></span>
  - <span data-ttu-id="77c40-137">Исправлена ошибка опроса операции.</span><span class="sxs-lookup"><span data-stu-id="77c40-137">Fix for operation polling</span></span>
  - <span data-ttu-id="77c40-138">Исправлено значение GracePeriodWithDataLossHour при настройке ручного режима FailoverPolicy.</span><span class="sxs-lookup"><span data-stu-id="77c40-138">Fix GracePeriodWithDataLossHour value when setting FailoverPolicy to Manual</span></span>
* <span data-ttu-id="77c40-139">TrafficManager</span><span class="sxs-lookup"><span data-stu-id="77c40-139">TrafficManager</span></span>
  - <span data-ttu-id="77c40-140">Добавлена поддержка метода географической маршрутизации трафика.</span><span class="sxs-lookup"><span data-stu-id="77c40-140">Support for the Geographic traffic routing method</span></span>
    + <span data-ttu-id="77c40-141">Для параметра TrafficRoutingMethod командлета New-AzureRmTrafficManagerProfile доступно новое значение — Geographic.</span><span class="sxs-lookup"><span data-stu-id="77c40-141">New value 'Geographic' for the TrafficRoutingMethod parameter of New-AzureRmTrafficManagerProfile</span></span>
    + <span data-ttu-id="77c40-142">Для командлетов New-AzureRmTrafficManagerEndpoint и Add-AzureRmTrafficManagerEndpointConfig доступен новый параметр — GeoMapping.</span><span class="sxs-lookup"><span data-stu-id="77c40-142">New parameter 'GeoMapping' for the New-AzureRmTrafficManagerEndpoint and Add-AzureRmTrafficManagerEndpointConfig</span></span>
    + <span data-ttu-id="77c40-143">Исправлена ошибка передачи для командлета Get-AzureRmTrafficManagerProfile, который возвращал коллекцию профилей.</span><span class="sxs-lookup"><span data-stu-id="77c40-143">Fix piping for Get-AzureRmTrafficManagerProfile when it returns a collection of profiles</span></span>
* <span data-ttu-id="77c40-144">Управление службами</span><span class="sxs-lookup"><span data-stu-id="77c40-144">ServiceManagement</span></span>
  - <span data-ttu-id="77c40-145">Для командлета Restart-AzureVM добавлен параметр InitiateMaintenance для выполнения обслуживания во время перезапуска виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="77c40-145">Restart-AzureVM: Added InitiateMaintenance parameter for performing maintenance during VM restart.</span></span>
  - <span data-ttu-id="77c40-146">Для командлета Get-AzureVM добавлено поле состояния обслуживания.</span><span class="sxs-lookup"><span data-stu-id="77c40-146">Get-AzureVM: Added Maintenance Status field.</span></span>
  - <span data-ttu-id="77c40-147">Добавлены новые командлеты для поддержки обновления хранилища служб восстановления:</span><span class="sxs-lookup"><span data-stu-id="77c40-147">Added new cmdlets to support Recovery Services vault upgrade</span></span>
    + <span data-ttu-id="77c40-148">Test-AzureRecoveryServicesVaultUpgrade;</span><span class="sxs-lookup"><span data-stu-id="77c40-148">Test-AzureRecoveryServicesVaultUpgrade</span></span>
    + <span data-ttu-id="77c40-149">Invoke-AzureRecoveryServicesVaultUpgrade.</span><span class="sxs-lookup"><span data-stu-id="77c40-149">Invoke-AzureRecoveryServicesVaultUpgrade</span></span>
