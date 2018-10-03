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
ms.openlocfilehash: 3cb71087a61a0fcd06c014394e8f9e5654d4c1a8
ms.sourcegitcommit: 19dffee617477001f98d43e39a50ce1fad087b74
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2018
ms.locfileid: "47179009"
---
# <a name="release-notes"></a><span data-ttu-id="f18dd-103">Заметки о выпуске</span><span class="sxs-lookup"><span data-stu-id="f18dd-103">Release notes</span></span>

<span data-ttu-id="f18dd-104">Здесь приведен список изменений, внесенных в Azure PowerShell в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="f18dd-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="690---september-2018"></a><span data-ttu-id="f18dd-105">6.9.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="f18dd-105">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="f18dd-106">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="f18dd-106">General</span></span>
* <span data-ttu-id="f18dd-107">В модуль развертывания AzureRM добавлен командлет AzureRM.SignalR.</span><span class="sxs-lookup"><span data-stu-id="f18dd-107">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="f18dd-108">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="f18dd-108">AzureRM.Profile</span></span>
* <span data-ttu-id="f18dd-109">Незначительные изменения в общем коде хранилища.</span><span class="sxs-lookup"><span data-stu-id="f18dd-109">Minor changes to the storage common code</span></span>
* <span data-ttu-id="f18dd-110">Обновлены файлы справки, в которые добавлены полные типы параметров.</span><span class="sxs-lookup"><span data-stu-id="f18dd-110">Updated help files to include full parameter types.</span></span>
- <span data-ttu-id="f18dd-111">В наборе параметров ServicePrincipalCertificateWithSubscriptionId параметр -ServicePrincipal теперь стал необязательным.</span><span class="sxs-lookup"><span data-stu-id="f18dd-111">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="f18dd-112">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="f18dd-112">Azure.Storage</span></span>
* <span data-ttu-id="f18dd-113">Поддержка создания контекста хранилища с использованием OAuth.</span><span class="sxs-lookup"><span data-stu-id="f18dd-113">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="f18dd-114">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="f18dd-114">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="f18dd-115">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="f18dd-115">AzureRM.Cdn</span></span>
* <span data-ttu-id="f18dd-116">Добавлен номер SKU для расценок на Standard_Microsoft в CDN.</span><span class="sxs-lookup"><span data-stu-id="f18dd-116">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="f18dd-117">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="f18dd-117">AzureRM.Compute</span></span>
* <span data-ttu-id="f18dd-118">Keyvault и Storage перенесены в общие зависимости.</span><span class="sxs-lookup"><span data-stu-id="f18dd-118">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="f18dd-119">Добавлена поддержка большего количества размеров виртуальных машин в командлеты AEM.</span><span class="sxs-lookup"><span data-stu-id="f18dd-119">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="f18dd-120">Добавлен параметр PublicIPPrefix в командлет New-AzureRmVmssIpConfig.</span><span class="sxs-lookup"><span data-stu-id="f18dd-120">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="f18dd-121">Добавлен параметр ResourceId в командлет Invoke-AzureRmVMRunCommand.</span><span class="sxs-lookup"><span data-stu-id="f18dd-121">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="f18dd-122">Добавлен командлет Invoke-AzureRmVmssVMRunCommand.</span><span class="sxs-lookup"><span data-stu-id="f18dd-122">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="f18dd-123">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="f18dd-123">AzureRM.Dns</span></span>
* <span data-ttu-id="f18dd-124">Добавлена поддержка для псевдонима записи во время создания записи DNS.</span><span class="sxs-lookup"><span data-stu-id="f18dd-124">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="f18dd-125">AzureRM.Insights;</span><span class="sxs-lookup"><span data-stu-id="f18dd-125">AzureRM.Insights</span></span>
* <span data-ttu-id="f18dd-126">Исправлены проблемы № 6833 и № 7102 (область настроек диагностики).</span><span class="sxs-lookup"><span data-stu-id="f18dd-126">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="f18dd-127">Проблемы с именем по умолчанию, например service, во время создания, получения и отображения списка параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="f18dd-127">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="f18dd-128">Проблемы при создании параметров диагностики с категориями.</span><span class="sxs-lookup"><span data-stu-id="f18dd-128">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="f18dd-129">Добавлено сообщение о том, что не рекомендуется использовать параметры интервалов времени в метриках.</span><span class="sxs-lookup"><span data-stu-id="f18dd-129">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="f18dd-130">Параметры интервалов времени по-прежнему принимаются (это не критическое изменение), но они игнорируются в серверной части, потому что действительно только значение PT1M.</span><span class="sxs-lookup"><span data-stu-id="f18dd-130">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="f18dd-131">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="f18dd-131">AzureRM.Network</span></span>
* <span data-ttu-id="f18dd-132">Изменения командлетов LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f18dd-132">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="f18dd-133">LoadBalancerInboundNatPoolConfig: добавлены параметры IdleTimeoutInMinutes, EnableFloatingIp и EnableTcpReset.</span><span class="sxs-lookup"><span data-stu-id="f18dd-133">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="f18dd-134">LoadBalancerInboundNatRuleConfig: добавлен параметр EnableTcpReset.</span><span class="sxs-lookup"><span data-stu-id="f18dd-134">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="f18dd-135">LoadBalancerRuleConfig: добавлен параметр EnableTcpReset.</span><span class="sxs-lookup"><span data-stu-id="f18dd-135">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="f18dd-136">LoadBalancerProbeConfig: добавлена поддержка значения Https для параметра Protocol.</span><span class="sxs-lookup"><span data-stu-id="f18dd-136">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="f18dd-137">Добавлены новые команды для нового правила OutboundRule подресурса LoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="f18dd-137">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="f18dd-138">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f18dd-138">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="f18dd-139">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f18dd-139">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="f18dd-140">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f18dd-140">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="f18dd-141">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f18dd-141">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="f18dd-142">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f18dd-142">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="f18dd-143">Добавлено новое свойство HostedWorkloads для PSNetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="f18dd-143">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="f18dd-144">Добавлены новые командлеты для функции Брандмауэра Azure через ARM.</span><span class="sxs-lookup"><span data-stu-id="f18dd-144">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="f18dd-145">Добавлен командлет Get-AzureRmFirewall.</span><span class="sxs-lookup"><span data-stu-id="f18dd-145">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="f18dd-146">Добавлен командлет Set-AzureRmFirewall.</span><span class="sxs-lookup"><span data-stu-id="f18dd-146">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="f18dd-147">Добавлен командлет New-AzureRmFirewall.</span><span class="sxs-lookup"><span data-stu-id="f18dd-147">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="f18dd-148">Добавлен командлет Remove-AzureRmFirewall.</span><span class="sxs-lookup"><span data-stu-id="f18dd-148">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="f18dd-149">Добавлен командлет New-AzureRmFirewallApplicationRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="f18dd-149">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="f18dd-150">Добавлен командлет New-AzureRmFirewallApplicationRule.</span><span class="sxs-lookup"><span data-stu-id="f18dd-150">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="f18dd-151">Добавлен командлет New-AzureRmFirewallNatRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="f18dd-151">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="f18dd-152">Добавлен командлет New-AzureRmFirewallNatRule.</span><span class="sxs-lookup"><span data-stu-id="f18dd-152">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="f18dd-153">Добавлен командлет New-AzureRmFirewallNetworkRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="f18dd-153">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="f18dd-154">Добавлен командлет New-AzureRmFirewallNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="f18dd-154">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="f18dd-155">Добавлена поддержка конфигурации для доверенного корневого сертификата и автомасштабирования в Шлюзе приложений.</span><span class="sxs-lookup"><span data-stu-id="f18dd-155">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="f18dd-156">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="f18dd-156">New Cmdlets added:</span></span>
      - <span data-ttu-id="f18dd-157">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f18dd-157">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="f18dd-158">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f18dd-158">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="f18dd-159">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f18dd-159">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="f18dd-160">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f18dd-160">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="f18dd-161">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f18dd-161">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="f18dd-162">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f18dd-162">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="f18dd-163">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f18dd-163">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="f18dd-164">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f18dd-164">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="f18dd-165">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f18dd-165">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="f18dd-166">В следующие командлеты добавлен необязательный параметр -TrustedRootCertificate:</span><span class="sxs-lookup"><span data-stu-id="f18dd-166">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="f18dd-167">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f18dd-167">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="f18dd-168">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f18dd-168">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="f18dd-169">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="f18dd-169">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="f18dd-170">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="f18dd-170">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="f18dd-171">В следующие командлеты добавлен необязательный параметр -AutoscaleConfiguration:</span><span class="sxs-lookup"><span data-stu-id="f18dd-171">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="f18dd-172">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f18dd-172">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="f18dd-173">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f18dd-173">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="f18dd-174">Добавлен командлет для конечной точки интерфейса Get-AzureInterfaceEndpoint.</span><span class="sxs-lookup"><span data-stu-id="f18dd-174">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="f18dd-175">Добавлена поддержка нескольких префиксов адресов в подсети.</span><span class="sxs-lookup"><span data-stu-id="f18dd-175">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="f18dd-176">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="f18dd-176">Updated cmdlets:</span></span>
  - <span data-ttu-id="f18dd-177">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f18dd-177">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="f18dd-178">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f18dd-178">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="f18dd-179">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f18dd-179">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="f18dd-180">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f18dd-180">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="f18dd-181">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f18dd-181">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="f18dd-182">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f18dd-182">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="f18dd-183">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f18dd-183">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="f18dd-184">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f18dd-184">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="f18dd-185">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f18dd-185">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="f18dd-186">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f18dd-186">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="f18dd-187">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f18dd-187">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="f18dd-188">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f18dd-188">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="f18dd-189">New-AzureRmNetworkInterfaceIpConfig — Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f18dd-189">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="f18dd-190">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="f18dd-190">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="f18dd-191">Add-AzureRmVirtualNetworkGatewayIpConfig;</span><span class="sxs-lookup"><span data-stu-id="f18dd-191">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="f18dd-192">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f18dd-192">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="f18dd-193">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f18dd-193">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="f18dd-194">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f18dd-194">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="f18dd-195">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f18dd-195">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="f18dd-196">Добавлены командлеты для делегирования подсети.</span><span class="sxs-lookup"><span data-stu-id="f18dd-196">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="f18dd-197">New-AzureRmDelegation — создает делегирование, которое можно добавить к подсети.</span><span class="sxs-lookup"><span data-stu-id="f18dd-197">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="f18dd-198">Remove-AzureRmDelegation — принимает подсеть и удаляет указанное имя делегирования из этой подсети.</span><span class="sxs-lookup"><span data-stu-id="f18dd-198">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="f18dd-199">Add-AzureRmDelegation — принимает подсеть и добавляет указанное имя службы в качестве делегирования для этой подсети.</span><span class="sxs-lookup"><span data-stu-id="f18dd-199">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="f18dd-200">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="f18dd-200">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="f18dd-201">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="f18dd-201">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="f18dd-202">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="f18dd-202">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="f18dd-203">Добавлена поддержка управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="f18dd-203">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="f18dd-204">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f18dd-204">AzureRM.RedisCache</span></span>
* <span data-ttu-id="f18dd-205">Обновлена зависимость Insights.</span><span class="sxs-lookup"><span data-stu-id="f18dd-205">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="f18dd-206">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="f18dd-206">AzureRM.Resources</span></span>
* <span data-ttu-id="f18dd-207">В командлет New-AzureRmResourceGroupDeployment добавлен новый параметр RollbackAction.</span><span class="sxs-lookup"><span data-stu-id="f18dd-207">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="f18dd-208">Добавлена поддержка OnErrorDeployment с новым параметром.</span><span class="sxs-lookup"><span data-stu-id="f18dd-208">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="f18dd-209">Добавлена поддержка управляемого удостоверения при назначении политик.</span><span class="sxs-lookup"><span data-stu-id="f18dd-209">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="f18dd-210">При назначении политики с помощью New-AzureRmPolicyAssignment параметры со значениями по умолчанию больше не требуются.</span><span class="sxs-lookup"><span data-stu-id="f18dd-210">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="f18dd-211">Добавлен новый командлет Get-AzureRmPolicyAlias для получения псевдонимов политик.</span><span class="sxs-lookup"><span data-stu-id="f18dd-211">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="f18dd-212">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f18dd-212">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="f18dd-213">Устранена проблема № 7161.</span><span class="sxs-lookup"><span data-stu-id="f18dd-213">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="f18dd-214">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="f18dd-214">AzureRM.SignalR</span></span>
* <span data-ttu-id="f18dd-215">Обновлены номера SKU для Free_F1 и Standard_S1.</span><span class="sxs-lookup"><span data-stu-id="f18dd-215">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="f18dd-216">Добавлены поле версии в объект PSSignalRResource и строка подключения в объект PSSignalRKeys.</span><span class="sxs-lookup"><span data-stu-id="f18dd-216">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="f18dd-217">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="f18dd-217">AzureRM.Storage</span></span>
* <span data-ttu-id="f18dd-218">Добавлена поддержка политики неизменяемости в AzureRm.Storage.</span><span class="sxs-lookup"><span data-stu-id="f18dd-218">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="f18dd-219">Remove-AzureRmStorageAccountNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="f18dd-219">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="f18dd-220">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f18dd-220">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="f18dd-221">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f18dd-221">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="f18dd-222">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f18dd-222">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="f18dd-223">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f18dd-223">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="f18dd-224">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="f18dd-224">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="f18dd-225">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="f18dd-225">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="f18dd-226">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="f18dd-226">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="f18dd-227">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="f18dd-227">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="f18dd-228">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="f18dd-228">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="f18dd-229">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="f18dd-229">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="f18dd-230">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="f18dd-230">AzureRM.Websites</span></span>
* <span data-ttu-id="f18dd-231">Добавлены два новых командлета: Get-AzureRmDeletedWebApp и Restore-AzureRmDeletedWebApp.</span><span class="sxs-lookup"><span data-stu-id="f18dd-231">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="f18dd-232">New-AzureRmAppServicePlan: добавлен параметр -HyperV для создания плана службы приложений с контейнером Windows.</span><span class="sxs-lookup"><span data-stu-id="f18dd-232">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="f18dd-233">New-AzureRmWebApp, New-AzureRmWebAppSlot, Set-AzureRmWebApp, Set-AzureRmWebAppSlot: добавлены новые параметры (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) для создания контейнера приложения Windows и управления им.</span><span class="sxs-lookup"><span data-stu-id="f18dd-233">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="f18dd-234">6.8.1 — август 2018 г.</span><span class="sxs-lookup"><span data-stu-id="f18dd-234">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="f18dd-235">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="f18dd-235">General</span></span>
* <span data-ttu-id="f18dd-236">Исправлена проблема с отсутствием настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f18dd-236">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="f18dd-237">Обновлены общие сборки среды выполнения</span><span class="sxs-lookup"><span data-stu-id="f18dd-237">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="f18dd-238">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f18dd-238">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="f18dd-239">Исправлена проблема с отсутствием настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f18dd-239">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="f18dd-240">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6603.</span><span class="sxs-lookup"><span data-stu-id="f18dd-240">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="f18dd-241">Командлеты Import-AzureRmApiManagementApi и \*-AzureRmApiManagementCertificate теперь обрабатывают относительные пути.</span><span class="sxs-lookup"><span data-stu-id="f18dd-241">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="f18dd-242">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6879.</span><span class="sxs-lookup"><span data-stu-id="f18dd-242">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="f18dd-243">CertificateInformation — это задаваемое свойство, обеспечивающее правильную работу командлета Set-AzureRmApiManagement.</span><span class="sxs-lookup"><span data-stu-id="f18dd-243">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="f18dd-244">Проблема исправлена путем обновления пакета NuGet до версии 4.0.4-preview.</span><span class="sxs-lookup"><span data-stu-id="f18dd-244">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="f18dd-245">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6853.</span><span class="sxs-lookup"><span data-stu-id="f18dd-245">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="f18dd-246">Исправлен фильтр OData для поиска по имени продукта.</span><span class="sxs-lookup"><span data-stu-id="f18dd-246">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="f18dd-247">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6814.</span><span class="sxs-lookup"><span data-stu-id="f18dd-247">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="f18dd-248">Исправлен фильтр OData для поиска по имени API.</span><span class="sxs-lookup"><span data-stu-id="f18dd-248">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="f18dd-249">Добавлена поддержка средства ведения журнала Azure Monitor.</span><span class="sxs-lookup"><span data-stu-id="f18dd-249">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="f18dd-250">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="f18dd-250">AzureRM.Compute</span></span>
* <span data-ttu-id="f18dd-251">Исправлена проблема с отсутствием в выходных данных ошибки целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="f18dd-251">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="f18dd-252">Исправлена проблема с типом учетной записи хранения для виртуальной машины с управляемым диском.</span><span class="sxs-lookup"><span data-stu-id="f18dd-252">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="f18dd-253">Исправлена проблема с отсутствием настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f18dd-253">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="f18dd-254">Исправлены командлеты расширения AEM для других сред, например Azure для Китая.</span><span class="sxs-lookup"><span data-stu-id="f18dd-254">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="f18dd-255">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="f18dd-255">AzureRM.Network</span></span>
* <span data-ttu-id="f18dd-256">Стандартное представление выходных данных командлетов изменено на представление таблиц.</span><span class="sxs-lookup"><span data-stu-id="f18dd-256">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="f18dd-257">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="f18dd-257">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="f18dd-258">Исправлена проблема с Update-AzureRmPowerBIEmbeddedCapacity при попытке масштабировать приостановленную емкость.</span><span class="sxs-lookup"><span data-stu-id="f18dd-258">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="f18dd-259">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="f18dd-259">AzureRM.Resources</span></span>
* <span data-ttu-id="f18dd-260">Исправлена проблема с созданием управляемых приложений из Marketplace.</span><span class="sxs-lookup"><span data-stu-id="f18dd-260">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="f18dd-261">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f18dd-261">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="f18dd-262">Исправленные проблемы</span><span class="sxs-lookup"><span data-stu-id="f18dd-262">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="f18dd-263">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="f18dd-263">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="f18dd-264">Добавлена поддержка метода маршрутизации MultiValue.</span><span class="sxs-lookup"><span data-stu-id="f18dd-264">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="f18dd-265">Добавлен новый параметр MaxReturn для маршрутизации MultiValue.</span><span class="sxs-lookup"><span data-stu-id="f18dd-265">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="f18dd-266">Добавлена поддержка метода маршрутизации Subnet.</span><span class="sxs-lookup"><span data-stu-id="f18dd-266">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="f18dd-267">Добавлена поддержка диапазонов IP-адресов (подсетей) в конечных точках.</span><span class="sxs-lookup"><span data-stu-id="f18dd-267">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="f18dd-268">Добавлена поддержка пользовательских заголовков в профилях.</span><span class="sxs-lookup"><span data-stu-id="f18dd-268">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="f18dd-269">Добавлена поддержка диапазонов кода ожидаемого состояния в профилях.</span><span class="sxs-lookup"><span data-stu-id="f18dd-269">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="f18dd-270">Добавлена поддержка пользовательских заголовков в конечных точках.</span><span class="sxs-lookup"><span data-stu-id="f18dd-270">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="f18dd-271">6.8.0 — август 2018 г.</span><span class="sxs-lookup"><span data-stu-id="f18dd-271">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="f18dd-272">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="f18dd-272">General</span></span>
* <span data-ttu-id="f18dd-273">Исправлена проблема с отсутствием настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f18dd-273">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="f18dd-274">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="f18dd-274">AzureRM.Profile</span></span>
* <span data-ttu-id="f18dd-275">Добавлено свойство срока действия для маркеров, возвращенных при выполнении Connect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="f18dd-275">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="f18dd-276">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="f18dd-276">AzureRM.Compute</span></span>
* <span data-ttu-id="f18dd-277">Исправлена проблема с отсутствием в выходных данных ошибки целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="f18dd-277">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="f18dd-278">Исправлена проблема с типом учетной записи хранения для виртуальной машины с управляемым диском.</span><span class="sxs-lookup"><span data-stu-id="f18dd-278">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="f18dd-279">Исправлены командлеты расширения AEM для других сред, например Azure для Китая.</span><span class="sxs-lookup"><span data-stu-id="f18dd-279">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="f18dd-280">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="f18dd-280">AzureRM.IotHub</span></span>
* <span data-ttu-id="f18dd-281">Исправлены примеры для New-AzureRmIotHubExportDevices и New-AzureRmIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="f18dd-281">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="f18dd-282">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="f18dd-282">AzureRM.Network</span></span>
* <span data-ttu-id="f18dd-283">Изменено представление моделей по умолчанию на представление таблиц.</span><span class="sxs-lookup"><span data-stu-id="f18dd-283">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="f18dd-284">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="f18dd-284">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="f18dd-285">Исправлена проблема с Update-AzureRmPowerBIEmbeddedCapacity при попытке масштабировать приостановленную емкость.</span><span class="sxs-lookup"><span data-stu-id="f18dd-285">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="f18dd-286">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="f18dd-286">AzureRM.Resources</span></span>
* <span data-ttu-id="f18dd-287">Исправлена проблема с созданием управляемого приложения из marketplace.</span><span class="sxs-lookup"><span data-stu-id="f18dd-287">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="f18dd-288">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f18dd-288">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="f18dd-289">Исправления проблем</span><span class="sxs-lookup"><span data-stu-id="f18dd-289">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="f18dd-290">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="f18dd-290">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="f18dd-291">Добавлена поддержка метода маршрутизации MultiValue.</span><span class="sxs-lookup"><span data-stu-id="f18dd-291">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="f18dd-292">Добавлен новый параметр MaxReturn для маршрутизации MultiValue.</span><span class="sxs-lookup"><span data-stu-id="f18dd-292">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="f18dd-293">Добавлена поддержка метода маршрутизации Subnet.</span><span class="sxs-lookup"><span data-stu-id="f18dd-293">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="f18dd-294">Добавлена поддержка диапазонов IP-адресов (подсетей) в конечных точках.</span><span class="sxs-lookup"><span data-stu-id="f18dd-294">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="f18dd-295">Добавлена поддержка пользовательских заголовков в профилях.</span><span class="sxs-lookup"><span data-stu-id="f18dd-295">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="f18dd-296">Добавлена поддержка диапазонов кода состояния ожидания в профилях.</span><span class="sxs-lookup"><span data-stu-id="f18dd-296">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="f18dd-297">Добавлена поддержка пользовательских заголовков в конечных точках.</span><span class="sxs-lookup"><span data-stu-id="f18dd-297">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="f18dd-298">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="f18dd-298">AzureRM.Websites</span></span>
* <span data-ttu-id="f18dd-299">Исправлена проблема с отсутствием правильной настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f18dd-299">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="f18dd-300">6.7.0 — август 2018 г.</span><span class="sxs-lookup"><span data-stu-id="f18dd-300">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="f18dd-301">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="f18dd-301">AzureRM.Profile</span></span>
* <span data-ttu-id="f18dd-302">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-302">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="f18dd-303">Добавлен идентификатор пользователя для имени контекста по умолчанию, чтобы избежать конфликтов контекста.</span><span class="sxs-lookup"><span data-stu-id="f18dd-303">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="f18dd-304">Устранены проблемы с командлетом Clear-AzureRmContext, которые приводили к проблемам с выбором контекста #6398.</span><span class="sxs-lookup"><span data-stu-id="f18dd-304">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="f18dd-305">Разрешено передавать домен клиента в параметр -TenantId для командлета Connect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="f18dd-305">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="f18dd-306">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="f18dd-306">Azure.Storage</span></span>
* <span data-ttu-id="f18dd-307">Удалено ограничение в 5 ТБ для квоты на общую папку Azure.</span><span class="sxs-lookup"><span data-stu-id="f18dd-307">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="f18dd-308">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="f18dd-308">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="f18dd-309">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f18dd-309">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="f18dd-310">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-310">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="f18dd-311">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f18dd-311">Azure.AnalysisServices</span></span>
* <span data-ttu-id="f18dd-312">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-312">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="f18dd-313">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f18dd-313">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="f18dd-314">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-314">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="f18dd-315">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="f18dd-315">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="f18dd-316">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-316">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="f18dd-317">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="f18dd-317">AzureRM.Automation</span></span>
* <span data-ttu-id="f18dd-318">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-318">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="f18dd-319">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="f18dd-319">AzureRM.Backup</span></span>
* <span data-ttu-id="f18dd-320">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-320">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="f18dd-321">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="f18dd-321">AzureRM.Batch</span></span>
* <span data-ttu-id="f18dd-322">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-322">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="f18dd-323">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="f18dd-323">AzureRM.Billing</span></span>
* <span data-ttu-id="f18dd-324">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-324">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="f18dd-325">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="f18dd-325">AzureRM.Cdn</span></span>
* <span data-ttu-id="f18dd-326">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-326">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="f18dd-327">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f18dd-327">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="f18dd-328">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-328">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="f18dd-329">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="f18dd-329">AzureRM.Compute</span></span>
* <span data-ttu-id="f18dd-330">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-330">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="f18dd-331">В командлет New-AzureRmVmssConfig добавлен параметр EvictionPolicy.</span><span class="sxs-lookup"><span data-stu-id="f18dd-331">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="f18dd-332">Если расположение не указано, используйте в DiskFileParameterSet для New AzureRmVm расположение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f18dd-332">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="f18dd-333">Исправлено описание параметров в Save-AzureRmVMImage.</span><span class="sxs-lookup"><span data-stu-id="f18dd-333">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="f18dd-334">Исправлен командлет Get-AzureRmVMDiskEncryptionStatus для определенных сценариев, связанных с однократным выполнением.</span><span class="sxs-lookup"><span data-stu-id="f18dd-334">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="f18dd-335">AzureRM.Consumption:</span><span class="sxs-lookup"><span data-stu-id="f18dd-335">AzureRM.Consumption</span></span>
* <span data-ttu-id="f18dd-336">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-336">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="f18dd-337">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f18dd-337">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="f18dd-338">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-338">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="f18dd-339">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f18dd-339">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="f18dd-340">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-340">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="f18dd-341">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="f18dd-341">AzureRM.DataFactories</span></span>
* <span data-ttu-id="f18dd-342">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-342">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="f18dd-343">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f18dd-343">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="f18dd-344">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-344">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="f18dd-345">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="f18dd-345">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="f18dd-346">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-346">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="f18dd-347">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f18dd-347">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="f18dd-348">Исправлена отладка, когда DebugPreference настраивается из командной строки PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f18dd-348">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="f18dd-349">Обновлен пример для Set-AzureRmDataLakeStoreItemAcl.</span><span class="sxs-lookup"><span data-stu-id="f18dd-349">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="f18dd-350">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-350">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="f18dd-351">Обновлен пример для Set-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="f18dd-351">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="f18dd-352">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="f18dd-352">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="f18dd-353">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-353">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="f18dd-354">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="f18dd-354">AzureRM.Dns</span></span>
* <span data-ttu-id="f18dd-355">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-355">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="f18dd-356">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f18dd-356">AzureRM.EventGrid</span></span>
* <span data-ttu-id="f18dd-357">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-357">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="f18dd-358">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="f18dd-358">AzureRM.EventHub</span></span>
* <span data-ttu-id="f18dd-359">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-359">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="f18dd-360">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f18dd-360">AzureRM.HDInsight</span></span>
* <span data-ttu-id="f18dd-361">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-361">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="f18dd-362">AzureRM.Insights;</span><span class="sxs-lookup"><span data-stu-id="f18dd-362">AzureRM.Insights</span></span>
* <span data-ttu-id="f18dd-363">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-363">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="f18dd-364">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="f18dd-364">AzureRM.IotHub</span></span>
* <span data-ttu-id="f18dd-365">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-365">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="f18dd-366">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f18dd-366">AzureRM.KeyVault</span></span>
* <span data-ttu-id="f18dd-367">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-367">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="f18dd-368">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f18dd-368">AzureRM.LogicApp</span></span>
* <span data-ttu-id="f18dd-369">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-369">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="f18dd-370">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="f18dd-370">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="f18dd-371">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-371">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="f18dd-372">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="f18dd-372">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="f18dd-373">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-373">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="f18dd-374">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="f18dd-374">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="f18dd-375">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-375">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="f18dd-376">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="f18dd-376">AzureRM.Media</span></span>
* <span data-ttu-id="f18dd-377">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-377">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="f18dd-378">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="f18dd-378">AzureRM.Network</span></span>
* <span data-ttu-id="f18dd-379">Добавлен пример для Set-AzureRmLocalNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="f18dd-379">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="f18dd-380">Добавлены примеры и описания для Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey и New-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="f18dd-380">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="f18dd-381">Добавлены примеры для Remove-AzureRmVirtualNetworkGatewayIpConfig и Reset-AzureRmVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="f18dd-381">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="f18dd-382">Добавлен пример для Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.</span><span class="sxs-lookup"><span data-stu-id="f18dd-382">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="f18dd-383">Добавлен пример для Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.</span><span class="sxs-lookup"><span data-stu-id="f18dd-383">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="f18dd-384">Добавлен пример для Set-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="f18dd-384">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="f18dd-385">Повторно созданы командлеты для ApplicationSecurityGroup, RouteTable и Usage с помощью генератора кода последней версии.</span><span class="sxs-lookup"><span data-stu-id="f18dd-385">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="f18dd-386">Уточнено сообщение об ошибке для Get-AzureRmVirtualNetworkSubnetConfig при попытке получить подсеть, которая не существует.</span><span class="sxs-lookup"><span data-stu-id="f18dd-386">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="f18dd-387">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="f18dd-387">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="f18dd-388">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-388">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="f18dd-389">AzureRM.OperationalInsights;</span><span class="sxs-lookup"><span data-stu-id="f18dd-389">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="f18dd-390">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-390">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="f18dd-391">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f18dd-391">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="f18dd-392">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-392">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="f18dd-393">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="f18dd-393">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="f18dd-394">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-394">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="f18dd-395">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f18dd-395">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="f18dd-396">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-396">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="f18dd-397">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="f18dd-397">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="f18dd-398">Добавлен фильтр политик для командлета Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="f18dd-398">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="f18dd-399">Команда возвращает список элементов резервного копирования, защищенных политикой с заданным идентификатором.</span><span class="sxs-lookup"><span data-stu-id="f18dd-399">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="f18dd-400">Обновление Microsoft.Azure.Management.RecoveryServices.Backup до версии 3.0.0-preview.</span><span class="sxs-lookup"><span data-stu-id="f18dd-400">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="f18dd-401">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-401">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="f18dd-402">Добавлен параметр TargetResourceGroupName для Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="f18dd-402">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="f18dd-403">Группа ресурсов, в которую восстанавливаются управляемые диски.</span><span class="sxs-lookup"><span data-stu-id="f18dd-403">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="f18dd-404">Применимо к резервной копии виртуальной машины с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="f18dd-404">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="f18dd-405">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="f18dd-405">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="f18dd-406">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-406">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="f18dd-407">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f18dd-407">AzureRM.RedisCache</span></span>
* <span data-ttu-id="f18dd-408">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-408">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="f18dd-409">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="f18dd-409">AzureRM.Relay</span></span>
* <span data-ttu-id="f18dd-410">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-410">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="f18dd-411">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="f18dd-411">AzureRM.Resources</span></span>
* <span data-ttu-id="f18dd-412">Поддержка развертывания шаблонов в области подписки.</span><span class="sxs-lookup"><span data-stu-id="f18dd-412">Support template deployment at subscription scope.</span></span> <span data-ttu-id="f18dd-413">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="f18dd-413">Add new Cmdlets:</span></span>
    - <span data-ttu-id="f18dd-414">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="f18dd-414">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="f18dd-415">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="f18dd-415">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="f18dd-416">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="f18dd-416">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="f18dd-417">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="f18dd-417">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="f18dd-418">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="f18dd-418">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="f18dd-419">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="f18dd-419">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="f18dd-420">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="f18dd-420">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="f18dd-421">Устранена проблема, когда при передаче контекста в Set-AzureRmResource возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="f18dd-421">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="f18dd-422">Исправлен пример в New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="f18dd-422">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="f18dd-423">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-423">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="f18dd-424">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="f18dd-424">AzureRM.Scheduler</span></span>
* <span data-ttu-id="f18dd-425">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-425">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="f18dd-426">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f18dd-426">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="f18dd-427">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-427">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="f18dd-428">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f18dd-428">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="f18dd-429">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-429">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="f18dd-430">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="f18dd-430">AzureRM.Sql</span></span>
* <span data-ttu-id="f18dd-431">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-431">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="f18dd-432">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="f18dd-432">AzureRM.Storage</span></span>
* <span data-ttu-id="f18dd-433">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-433">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="f18dd-434">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="f18dd-434">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="f18dd-435">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-435">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="f18dd-436">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="f18dd-436">AzureRM.Tags</span></span>
* <span data-ttu-id="f18dd-437">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-437">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="f18dd-438">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="f18dd-438">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="f18dd-439">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-439">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="f18dd-440">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="f18dd-440">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="f18dd-441">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-441">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="f18dd-442">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="f18dd-442">AzureRM.Websites</span></span>
* <span data-ttu-id="f18dd-443">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-443">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="f18dd-444">6.6.0 — июль 2018 г.</span><span class="sxs-lookup"><span data-stu-id="f18dd-444">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="f18dd-445">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="f18dd-445">General</span></span>
* <span data-ttu-id="f18dd-446">Обновлены все файлы справки: включены полные типы параметров и исправлены типы входных и выходных данных.</span><span class="sxs-lookup"><span data-stu-id="f18dd-446">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="f18dd-447">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="f18dd-447">AzureRM.Profile</span></span>
* <span data-ttu-id="f18dd-448">Обновлена библиотека Common.Strategy: теперь можно проверить, совместима ли текущая конфигурация ресурса с целевым ресурсом.</span><span class="sxs-lookup"><span data-stu-id="f18dd-448">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="f18dd-449">В Common.Storage добавлены типы ps1xml.</span><span class="sxs-lookup"><span data-stu-id="f18dd-449">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="f18dd-450">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="f18dd-450">Azure.Storage</span></span>
* <span data-ttu-id="f18dd-451">Добавлена поддержка для получения контекста хранилища из DefaultProfile.</span><span class="sxs-lookup"><span data-stu-id="f18dd-451">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="f18dd-452">В свойства типов выходных данных командлетов добавлен атрибут Ps1XmlAttribute.</span><span class="sxs-lookup"><span data-stu-id="f18dd-452">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="f18dd-453">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f18dd-453">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="f18dd-454">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6370.</span><span class="sxs-lookup"><span data-stu-id="f18dd-454">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="f18dd-455">В AutoMapper исправлена ошибка, препятствовавшая преобразованию PsApiManagementApi в ApiContract.</span><span class="sxs-lookup"><span data-stu-id="f18dd-455">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="f18dd-456">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6515.</span><span class="sxs-lookup"><span data-stu-id="f18dd-456">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="f18dd-457">В File.Save исправлена ошибка, связанная с перегрузкой типом кодировки.</span><span class="sxs-lookup"><span data-stu-id="f18dd-457">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="f18dd-458">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6560.</span><span class="sxs-lookup"><span data-stu-id="f18dd-458">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="f18dd-459">Выполнено обновление до версии NuGet 4.0.3, что позволило исправить исключение шаблона в apiId.</span><span class="sxs-lookup"><span data-stu-id="f18dd-459">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="f18dd-460">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="f18dd-460">AzureRM.Compute</span></span>
* <span data-ttu-id="f18dd-461">Устранена ошибка при создании виртуальной машины с помощью командлета New-AzureRmVm и параметра DiskFileParameterSet, которая возникала из-за переименования типа учетной записи хранения PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="f18dd-461">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="f18dd-462">Исправлен командлет Invoke-AzureRmVMRunCommand.</span><span class="sxs-lookup"><span data-stu-id="f18dd-462">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="f18dd-463">Командлет Get-AzureRmAvailabilitySet теперь может выводить список всех групп доступности в подписке.</span><span class="sxs-lookup"><span data-stu-id="f18dd-463">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="f18dd-464">(Параметр ResouceGroupName теперь является необязательным.)</span><span class="sxs-lookup"><span data-stu-id="f18dd-464">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="f18dd-465">Обновлен параметр SimpleParameterSet командлета New-AzureRmVm, что позволило использовать ускоренную сеть на соответствующих виртуальных машинах.</span><span class="sxs-lookup"><span data-stu-id="f18dd-465">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="f18dd-466">Обновлен простой набор параметров New-AzureRmVmss, что позволило отменять создание масштабируемого набора виртуальных машин, если указанная пользователем подсистема балансировки нагрузки уже существует.</span><span class="sxs-lookup"><span data-stu-id="f18dd-466">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="f18dd-467">Обновлен пример для New-AzureRmDisk.</span><span class="sxs-lookup"><span data-stu-id="f18dd-467">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="f18dd-468">Добавлен пример для New-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="f18dd-468">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="f18dd-469">Обновлено описание командлета Set-AzureRmVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="f18dd-469">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="f18dd-470">Обновлен пример 1 для Set-AzureRmVMBginfoExtension: исправлены орфографические ошибки и префикс.</span><span class="sxs-lookup"><span data-stu-id="f18dd-470">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="f18dd-471">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f18dd-471">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="f18dd-472">Пакет .NET SDK для ADF обновлен до версии 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="f18dd-472">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="f18dd-473">Добавлена поддержка совместного использования локальной среды IR несколькими фабриками данных.</span><span class="sxs-lookup"><span data-stu-id="f18dd-473">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="f18dd-474">Добавлен новый параметр -SharedIntegrationRuntimeResourceId для командлета Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-474">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="f18dd-475">Добавлен новый необязательный параметр -LinkedDataFactoryName для командлета Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="f18dd-475">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="f18dd-476">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f18dd-476">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="f18dd-477">Пакет SDK для плоскости данных (Microsoft.Azure.DataLake.Store) обновлен до версии 1.1.9.</span><span class="sxs-lookup"><span data-stu-id="f18dd-477">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="f18dd-478">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="f18dd-478">AzureRM.EventHub</span></span>
* <span data-ttu-id="f18dd-479">Обновлена конвейерная передача для InputObject и ResourceId в командлетах remove.</span><span class="sxs-lookup"><span data-stu-id="f18dd-479">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="f18dd-480">AzureRM.Insights;</span><span class="sxs-lookup"><span data-stu-id="f18dd-480">AzureRM.Insights</span></span>
* <span data-ttu-id="f18dd-481">Исправлено форматирование OutputType в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="f18dd-481">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="f18dd-482">Применен пакет SDK Microsoft.Azure.Management.Monitor 0.19.1-preview.</span><span class="sxs-lookup"><span data-stu-id="f18dd-482">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="f18dd-483">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f18dd-483">AzureRM.KeyVault</span></span>
* <span data-ttu-id="f18dd-484">Исправлена проблема с конвейерной передачей в командлете Set-AzureRmKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="f18dd-484">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="f18dd-485">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="f18dd-485">AzureRM.Network</span></span>
* <span data-ttu-id="f18dd-486">Добавлены примеры для командлетов LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="f18dd-486">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="f18dd-487">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="f18dd-487">AzureRM.Resources</span></span>
* <span data-ttu-id="f18dd-488">Устранена проблема, возникавшая при указании имени и значения тега для Get-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="f18dd-488">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="f18dd-489">Исправлен сценарий конвейерной передачи в Set-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="f18dd-489">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="f18dd-490">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f18dd-490">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="f18dd-491">Обновлена конвейерная передача для InputObject и ResourceId в командлетах remove.</span><span class="sxs-lookup"><span data-stu-id="f18dd-491">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="f18dd-492">Исправлено несколько ошибок.</span><span class="sxs-lookup"><span data-stu-id="f18dd-492">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="f18dd-493">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="f18dd-493">AzureRM.Sql</span></span>
* <span data-ttu-id="f18dd-494">Добавлена поддержка Advanced Threat Protection для сервера с помощью следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="f18dd-494">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="f18dd-495">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="f18dd-495">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="f18dd-496">Добавлена поддержка оценки уязвимостей с помощью следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="f18dd-496">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="f18dd-497">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings;</span><span class="sxs-lookup"><span data-stu-id="f18dd-497">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="f18dd-498">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline;</span><span class="sxs-lookup"><span data-stu-id="f18dd-498">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="f18dd-499">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan.</span><span class="sxs-lookup"><span data-stu-id="f18dd-499">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="f18dd-500">Исправлен пример для Remove-AzureRmSqlServerFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="f18dd-500">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="f18dd-501">Исправлена неправильная обработка даты и времени для базового языка и региональных параметров, отличных от США, в Get-AzureSqlSyncGroupLog.</span><span class="sxs-lookup"><span data-stu-id="f18dd-501">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="f18dd-502">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="f18dd-502">AzureRM.Storage</span></span>
* <span data-ttu-id="f18dd-503">В свойства типов выходных данных командлетов добавлен атрибут Ps1XmlAttribute.</span><span class="sxs-lookup"><span data-stu-id="f18dd-503">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="f18dd-504">Выходные данные командлетов StorageAccount теперь отображаются в виде таблицы.</span><span class="sxs-lookup"><span data-stu-id="f18dd-504">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="f18dd-505">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f18dd-505">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="f18dd-506">New-AzureRmStorageAccount;</span><span class="sxs-lookup"><span data-stu-id="f18dd-506">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="f18dd-507">Set-AzureRmStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="f18dd-507">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="f18dd-508">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="f18dd-508">AzureRM.Tags</span></span>
* <span data-ttu-id="f18dd-509">Удалено неверное утверждение из справки по командлетам Tag.</span><span class="sxs-lookup"><span data-stu-id="f18dd-509">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="f18dd-510">6.5.0 — июль 2018 г.</span><span class="sxs-lookup"><span data-stu-id="f18dd-510">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="f18dd-511">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="f18dd-511">AzureRM.Profile</span></span>
* <span data-ttu-id="f18dd-512">Обновлена справка для командлета Get-AzureRmContextAutosaveSetting.</span><span class="sxs-lookup"><span data-stu-id="f18dd-512">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="f18dd-513">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="f18dd-513">Azure.Storage</span></span>
* <span data-ttu-id="f18dd-514">Добавлена поддержка отправки BLOB-объекта или файла с помощью токена SAS, доступного только для записи.</span><span class="sxs-lookup"><span data-stu-id="f18dd-514">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="f18dd-515">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f18dd-515">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="f18dd-516">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f18dd-516">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="f18dd-517">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f18dd-517">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="f18dd-518">Для AS добавлено обязательное свойство ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="f18dd-518">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="f18dd-519">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="f18dd-519">AzureRM.Automation</span></span>
* <span data-ttu-id="f18dd-520">Обновлена справка и добавлены примеры для командлета New-AzureRMAutomationSchedule.</span><span class="sxs-lookup"><span data-stu-id="f18dd-520">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="f18dd-521">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="f18dd-521">AzureRM.Compute</span></span>
* <span data-ttu-id="f18dd-522">Добавлен параметр -Tag для командлета Update/New-AzureRmAvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="f18dd-522">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="f18dd-523">Добавлен пример для командлета Add-AzureRmVmssExtension.</span><span class="sxs-lookup"><span data-stu-id="f18dd-523">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="f18dd-524">Добавлены примеры для командлета Remove-AzureRmVmssExtension.</span><span class="sxs-lookup"><span data-stu-id="f18dd-524">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="f18dd-525">Обновлена справка для командлета Set-AzureRmVMAccessExtension.</span><span class="sxs-lookup"><span data-stu-id="f18dd-525">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="f18dd-526">Изменен класс SimpleParameterSet для командлета New-AzureRmVmss: теперь для SinglePlacementGroup по умолчанию задается значение false, а также добавляется параметр-переключатель SinglePlacementGroup, который позволяет пользователю создать VMSS в одной группе размещения.</span><span class="sxs-lookup"><span data-stu-id="f18dd-526">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="f18dd-527">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="f18dd-527">AzureRM.EventHub</span></span>
* <span data-ttu-id="f18dd-528">В класс PSEventHubDRConfigurationAttributes добавлено доступное только для чтения свойство PendingReplicationOperationsCount, которое показывает количество ожидающих репликации операций во время реплицирования.</span><span class="sxs-lookup"><span data-stu-id="f18dd-528">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="f18dd-529">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f18dd-529">AzureRM.KeyVault</span></span>
* <span data-ttu-id="f18dd-530">Обновлено сообщение об ошибке для командлета Set-AzureRmKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="f18dd-530">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="f18dd-531">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f18dd-531">AzureRM.LogicApp</span></span>
* <span data-ttu-id="f18dd-532">Исправлена ошибка "parameter set could not be resolved" (не удалось разрешить заданный параметр) в командлете New-AzureRmLogicApp.</span><span class="sxs-lookup"><span data-stu-id="f18dd-532">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="f18dd-533">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="f18dd-533">AzureRM.Network</span></span>
* <span data-ttu-id="f18dd-534">Включен пиринг между виртуальными сетями в нескольких клиентах для командлета Set/Add-AzureRmVirtualNetworkPeering.</span><span class="sxs-lookup"><span data-stu-id="f18dd-534">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="f18dd-535">Для шлюза приложений обновлены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="f18dd-535">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="f18dd-536">New-AzureRmApplicationGateway: добавлены флаг EnableFIPS и поддержка зон.</span><span class="sxs-lookup"><span data-stu-id="f18dd-536">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="f18dd-537">New-AzureRmApplicationGatewaySku: добавлены новые номера SKU Standard_v2 и WAF_v2.</span><span class="sxs-lookup"><span data-stu-id="f18dd-537">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="f18dd-538">Set-AzureRmApplicationGatewaySku: добавлены новые номера SKU Standard_v2 и WAF_v2.</span><span class="sxs-lookup"><span data-stu-id="f18dd-538">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="f18dd-539">Командлеты RouteTable пересозданы в последней версии генератора.</span><span class="sxs-lookup"><span data-stu-id="f18dd-539">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="f18dd-540">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="f18dd-540">AzureRM.Relay</span></span>
* <span data-ttu-id="f18dd-541">Обновлены файлы Markdown, исправлена проблема с именем параметра в примере.</span><span class="sxs-lookup"><span data-stu-id="f18dd-541">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="f18dd-542">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="f18dd-542">AzureRM.Resources</span></span>
* <span data-ttu-id="f18dd-543">Обновлены командлеты Roleassignment и roledefinition:</span><span class="sxs-lookup"><span data-stu-id="f18dd-543">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="f18dd-544">Удалены лишние вызовы roledefinition, выполняемые в ходе разбиения на страницы.</span><span class="sxs-lookup"><span data-stu-id="f18dd-544">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="f18dd-545">Исправлен командлет Get-AzureRmRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="f18dd-545">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="f18dd-546">Исправлена работа параметра -ExpandPrincipalGroups.</span><span class="sxs-lookup"><span data-stu-id="f18dd-546">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="f18dd-547">Устранена проблема в командлете Get-AzureRmResource, заключающая в том, что в параметре -ResourceType учитывался регистр символов.</span><span class="sxs-lookup"><span data-stu-id="f18dd-547">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="f18dd-548">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f18dd-548">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="f18dd-549">Добавлены параметры top и skip для командлетов list.</span><span class="sxs-lookup"><span data-stu-id="f18dd-549">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="f18dd-550">Добавлены командлеты для перехода с пространства имен ценовой категории "Стандартный" на пространство ценовой категории "Премиум":</span><span class="sxs-lookup"><span data-stu-id="f18dd-550">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="f18dd-551">Start-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="f18dd-551">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="f18dd-552">Get-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="f18dd-552">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="f18dd-553">Complete-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="f18dd-553">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="f18dd-554">Stop-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="f18dd-554">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="f18dd-555">Remove-AzureRmServiceBusMigration.</span><span class="sxs-lookup"><span data-stu-id="f18dd-555">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="f18dd-556">В класс PSServiceBusDRConfigurationAttributes добавлено доступное только для чтения свойство PendingReplicationOperationsCount, которое показывает количество ожидающих репликации операций во время реплицирования.</span><span class="sxs-lookup"><span data-stu-id="f18dd-556">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="f18dd-557">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f18dd-557">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="f18dd-558">Обновлен пример для командлета New-AzureRmServiceFabricCluster.</span><span class="sxs-lookup"><span data-stu-id="f18dd-558">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="f18dd-559">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="f18dd-559">AzureRM.Sql</span></span>
* <span data-ttu-id="f18dd-560">Добавлены новые командлеты для Management.Sql, позволяющие клиентам добавлять сертификат TDE в экземпляр SQL Server или управляемый экземпляр:</span><span class="sxs-lookup"><span data-stu-id="f18dd-560">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="f18dd-561">Add-AzureRmSqlServerTransparentDataEncryptionCertificate;</span><span class="sxs-lookup"><span data-stu-id="f18dd-561">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="f18dd-562">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate.</span><span class="sxs-lookup"><span data-stu-id="f18dd-562">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="f18dd-563">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="f18dd-563">AzureRM.Websites</span></span>
* <span data-ttu-id="f18dd-564">`Set-AzureRmWebApp -AssignIdentity` и `Set-AzureRmWebAppSlot -AssignIdentity` при установленном значении false теперь будут удалять свойство Identity из объекта сайта. Также при этом будет удаляться тег предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="f18dd-564">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="f18dd-565">Обновлен пример для `Get-AzureRmWebAppMetrics` и `Get-AzureRmAppServicePlanMetrics`.</span><span class="sxs-lookup"><span data-stu-id="f18dd-565">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="f18dd-566">`Set-AzureRmWebApp -PhpVersion` теперь поддерживает off как допустимую версию PHP.</span><span class="sxs-lookup"><span data-stu-id="f18dd-566">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="f18dd-567">6.4.0 — июль 2018 г.</span><span class="sxs-lookup"><span data-stu-id="f18dd-567">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="f18dd-568">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="f18dd-568">General</span></span>
* <span data-ttu-id="f18dd-569">Исправлено форматирование OutputType в файлах справки для большинства модулей.</span><span class="sxs-lookup"><span data-stu-id="f18dd-569">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="f18dd-570">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="f18dd-570">AzureRM.Profile</span></span>
* <span data-ttu-id="f18dd-571">В основные типы выходных данных добавлен атрибут Ps1Xml.</span><span class="sxs-lookup"><span data-stu-id="f18dd-571">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="f18dd-572">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="f18dd-572">AzureRM.Compute</span></span>
* <span data-ttu-id="f18dd-573">Функция добавления тега IP-адреса для масштабируемого набора виртуальных машин (VMSS)</span><span class="sxs-lookup"><span data-stu-id="f18dd-573">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="f18dd-574">Добавлен командлет New-AzureRmVmssIpTagConfig.</span><span class="sxs-lookup"><span data-stu-id="f18dd-574">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="f18dd-575">В New-AzureRmVmssIpConfig добавлен параметр IpTag.</span><span class="sxs-lookup"><span data-stu-id="f18dd-575">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="f18dd-576">Функция автоматического отката ОС для VMSS</span><span class="sxs-lookup"><span data-stu-id="f18dd-576">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="f18dd-577">В New-AzureRmVmssConfig и Update-AzureRmVmss добавлены параметры DisableAutoRollback.</span><span class="sxs-lookup"><span data-stu-id="f18dd-577">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="f18dd-578">Функция ведения журнала обновлений ОС для VMSS</span><span class="sxs-lookup"><span data-stu-id="f18dd-578">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="f18dd-579">В Get-AzureRmVmss добавлен параметр OSUpgradeHistory.</span><span class="sxs-lookup"><span data-stu-id="f18dd-579">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="f18dd-580">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="f18dd-580">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="f18dd-581">Добавлена поддержка списков управления доступом к каталогу с использованием следующих команд:</span><span class="sxs-lookup"><span data-stu-id="f18dd-581">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="f18dd-582">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry;</span><span class="sxs-lookup"><span data-stu-id="f18dd-582">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="f18dd-583">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry;</span><span class="sxs-lookup"><span data-stu-id="f18dd-583">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="f18dd-584">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="f18dd-584">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="f18dd-585">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f18dd-585">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="f18dd-586">Добавлены поддержка отмены выполнения и отслеживание хода выполнения для Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl и Remove-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="f18dd-586">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="f18dd-587">Добавлена поддержка отмены выполнения для Export-AzureRmDataLakeStoreChildItemProperties.</span><span class="sxs-lookup"><span data-stu-id="f18dd-587">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="f18dd-588">Исправлена очистка сообщений об отладке для командлетов, которые выполняют рекурсивные операции.</span><span class="sxs-lookup"><span data-stu-id="f18dd-588">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="f18dd-589">Исправлено расположение тестовых данных для командлетов DataLake.</span><span class="sxs-lookup"><span data-stu-id="f18dd-589">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="f18dd-590">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="f18dd-590">AzureRM.EventHub</span></span>
* <span data-ttu-id="f18dd-591">Для командлетов вывода списка операций Get-AzureRmEventHub и Get-AzureRmEventHubConsumerGroup добавлен необязательный параметр MaxCount.</span><span class="sxs-lookup"><span data-stu-id="f18dd-591">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="f18dd-592">Исправлена проблема с командлетом New-AzureRmEventHub, из-за которой требовалось указать по крайней мере один параметр при создании концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="f18dd-592">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="f18dd-593">Добавлен набор параметров по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f18dd-593">Provided Default Parameter set.</span></span>
* <span data-ttu-id="f18dd-594">Для командлета New-AzureRmEventHubKey добавлен необязательный параметр -KeyValue, который позволяет пользователю предоставить значение ключа.</span><span class="sxs-lookup"><span data-stu-id="f18dd-594">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="f18dd-595">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f18dd-595">AzureRM.KeyVault</span></span>
* <span data-ttu-id="f18dd-596">Исправлена ошибка, из-за которой при выполнении командлета Get-AzureRmKeyVault с параметром -Tag возвращались все ресурсы.</span><span class="sxs-lookup"><span data-stu-id="f18dd-596">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="f18dd-597">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="f18dd-597">AzureRM.Network</span></span>
* <span data-ttu-id="f18dd-598">Для параметра шлюзов виртуальной вести, избыточных в пределах зоны, предоставлены новые номера SKU.</span><span class="sxs-lookup"><span data-stu-id="f18dd-598">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="f18dd-599">Добавлены новые команды для функции поддержки партнерских API для ExpressRoute, развертываемых с помощью ARM:</span><span class="sxs-lookup"><span data-stu-id="f18dd-599">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="f18dd-600">добавлена команда Get-AzureRmExpressRouteCrossConnection;</span><span class="sxs-lookup"><span data-stu-id="f18dd-600">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="f18dd-601">добавлена команда Set-AzureRmExpressRouteCrossConnection;</span><span class="sxs-lookup"><span data-stu-id="f18dd-601">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="f18dd-602">добавлена команда Add-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="f18dd-602">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="f18dd-603">добавлена команда Get-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="f18dd-603">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="f18dd-604">добавлена команда Remove-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="f18dd-604">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="f18dd-605">добавлена команда Get-AzureRMExpressRouteCrossConnectionArpTable;</span><span class="sxs-lookup"><span data-stu-id="f18dd-605">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="f18dd-606">добавлена команда Get-AzureRMExpressRouteCrossConnectionRouteTable;</span><span class="sxs-lookup"><span data-stu-id="f18dd-606">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="f18dd-607">добавлена команда Get-AzureRMExpressRouteCrossConnectionRouteTableSummary.</span><span class="sxs-lookup"><span data-stu-id="f18dd-607">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="f18dd-608">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="f18dd-608">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="f18dd-609">Добавлен командлет Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="f18dd-609">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="f18dd-610">Этот командлет принимает идентификатор виртуальной машины и проверяет, защищена ли виртуальная машина с помощью какого-либо хранилища в подписке.</span><span class="sxs-lookup"><span data-stu-id="f18dd-610">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="f18dd-611">Если такое хранилище существует, командлет выводит данные о нем.</span><span class="sxs-lookup"><span data-stu-id="f18dd-611">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="f18dd-612">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="f18dd-612">AzureRM.Resources</span></span>
* <span data-ttu-id="f18dd-613">Обновлены командлеты Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="f18dd-613">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="f18dd-614">Добавлена поддержка вывода списка значений параметра -Scope на уровне группы управления.</span><span class="sxs-lookup"><span data-stu-id="f18dd-614">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="f18dd-615">Добавлена поддержка для получения отдельных назначений со значениями -Scope на уровне группы управления.</span><span class="sxs-lookup"><span data-stu-id="f18dd-615">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="f18dd-616">Для параметра управления добавлены параметры -Effective и -All.</span><span class="sxs-lookup"><span data-stu-id="f18dd-616">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="f18dd-617">Обновлены командлеты Get/New/Remove/Set-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="f18dd-617">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="f18dd-618">Добавлен параметр -ManagementGroupName для применения операций к заданной группе управления.</span><span class="sxs-lookup"><span data-stu-id="f18dd-618">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="f18dd-619">Добавлен параметр -SubscriptionId для применения операций к заданной подписке.</span><span class="sxs-lookup"><span data-stu-id="f18dd-619">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="f18dd-620">Обновлены командлеты Get/New/Remove/Set-AzureRmPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="f18dd-620">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="f18dd-621">Добавлен параметр -ManagementGroupName для применения операций к заданной группе управления.</span><span class="sxs-lookup"><span data-stu-id="f18dd-621">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="f18dd-622">Добавлен параметр -SubscriptionId для применения операций к заданной подписке.</span><span class="sxs-lookup"><span data-stu-id="f18dd-622">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="f18dd-623">Добавлена поддержка ссылок на секрет KeyVault в параметрах при использовании TemplateParameterObject в New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="f18dd-623">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="f18dd-624">Устранена проблема, из-за которой параметр -EndDate игнорировался в New-AzureRmADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="f18dd-624">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="f18dd-625">Устранена проблема, из-за которой в Add-AzureRmADGroupMember использовался неверный URL-адрес для запроса.</span><span class="sxs-lookup"><span data-stu-id="f18dd-625">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="f18dd-626">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f18dd-626">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="f18dd-627">Для командлета New-AzureRmServiceBusKey добавлен необязательный параметр -KeyValue, который позволяет пользователю предоставить значение ключа.</span><span class="sxs-lookup"><span data-stu-id="f18dd-627">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="f18dd-628">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="f18dd-628">AzureRM.Sql</span></span>
* <span data-ttu-id="f18dd-629">В справке по New-AzureRmSqlDatabaseRestorePoint добавлено описание определяемых пользователем точек восстановления для хранилища данных SQL.</span><span class="sxs-lookup"><span data-stu-id="f18dd-629">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="f18dd-630">Обновлена документация по параметру -ComputeGeneration, используемого в нескольких командлетах.</span><span class="sxs-lookup"><span data-stu-id="f18dd-630">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="f18dd-631">6.3.0 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="f18dd-631">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="f18dd-632">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="f18dd-632">AzureRM.Profile</span></span>
* <span data-ttu-id="f18dd-633">Обновлены сообщения об ошибках для Enable-AzureRmContextAutoSave.</span><span class="sxs-lookup"><span data-stu-id="f18dd-633">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="f18dd-634">Создание контекста для каждой подписки при выполнении Connect-AzureRmAccount без предыдущего контекста.</span><span class="sxs-lookup"><span data-stu-id="f18dd-634">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="f18dd-635">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="f18dd-635">Azure.Storage</span></span>
* <span data-ttu-id="f18dd-636">В файлы справки добавлены дополнительные сведения о параметре -Permissions.</span><span class="sxs-lookup"><span data-stu-id="f18dd-636">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="f18dd-637">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="f18dd-637">AzureRM.Compute</span></span>
* <span data-ttu-id="f18dd-638">Get-AzureRmVmDiskEncryptionStatus устраняет проблему, которая наблюдалась на виртуальных машинах без дисков данных.</span><span class="sxs-lookup"><span data-stu-id="f18dd-638">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="f18dd-639">Обновлена версия клиентской библиотеки Compute для исправления следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="f18dd-639">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="f18dd-640">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="f18dd-640">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="f18dd-641">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="f18dd-641">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="f18dd-642">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="f18dd-642">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="f18dd-643">В следующих командлетах исправлено отображение неправильных значений operation ID и operation status:</span><span class="sxs-lookup"><span data-stu-id="f18dd-643">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="f18dd-644">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f18dd-644">Start-AzureRmVM</span></span>
    - <span data-ttu-id="f18dd-645">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f18dd-645">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="f18dd-646">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f18dd-646">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="f18dd-647">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f18dd-647">Set-AzureRmVM</span></span>
    - <span data-ttu-id="f18dd-648">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="f18dd-648">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="f18dd-649">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f18dd-649">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="f18dd-650">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="f18dd-650">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="f18dd-651">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="f18dd-651">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="f18dd-652">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f18dd-652">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="f18dd-653">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f18dd-653">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="f18dd-654">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f18dd-654">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="f18dd-655">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f18dd-655">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="f18dd-656">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="f18dd-656">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="f18dd-657">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="f18dd-657">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="f18dd-658">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="f18dd-658">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="f18dd-659">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="f18dd-659">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="f18dd-660">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="f18dd-660">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="f18dd-661">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="f18dd-661">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="f18dd-662">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f18dd-662">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="f18dd-663">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f18dd-663">AzureRM.EventGrid</span></span>
* <span data-ttu-id="f18dd-664">Удалены условия проверки ValidateNotNullOrEmpty для SubjectBeginsWith/SubjectEndsWith в командлете Update-AzureRmEventGridSubscription, что позволяет при необходимости заменять эти параметры пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="f18dd-664">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="f18dd-665">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f18dd-665">AzureRM.KeyVault</span></span>
* <span data-ttu-id="f18dd-666">Исправлена ошибка, когда при выполнении командлета Get-AzureRmKeyVault -Tag не возвращается ни один тег.</span><span class="sxs-lookup"><span data-stu-id="f18dd-666">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="f18dd-667">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f18dd-667">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="f18dd-668">Общедоступный выпуск командлетов Policy Insights.</span><span class="sxs-lookup"><span data-stu-id="f18dd-668">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="f18dd-669">Используется API версии 2018-04-04.</span><span class="sxs-lookup"><span data-stu-id="f18dd-669">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="f18dd-670">К результатам Get-AzureRmPolicyStateSummary добавлено PolicyDefinitionReferenceId.</span><span class="sxs-lookup"><span data-stu-id="f18dd-670">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="f18dd-671">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="f18dd-671">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="f18dd-672">Для командлетов RecoveryServices.Backup добавлен параметр -Vault.</span><span class="sxs-lookup"><span data-stu-id="f18dd-672">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="f18dd-673">Передача этого параметра переопределяет командлет Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="f18dd-673">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="f18dd-674">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="f18dd-674">AzureRM.Sql</span></span>
* <span data-ttu-id="f18dd-675">В файле справки обновлен пример для командлета Get-AzureRmSqlDatabaseExpanded.</span><span class="sxs-lookup"><span data-stu-id="f18dd-675">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="f18dd-676">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="f18dd-676">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="f18dd-677">Обновлен файл справки для командлета Add-AzureRmTrafficManagerEndpointConfig.</span><span class="sxs-lookup"><span data-stu-id="f18dd-677">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="f18dd-678">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="f18dd-678">AzureRM.Websites</span></span>
* <span data-ttu-id="f18dd-679">Изменено действие командлета Set-AzureRmWebApp. Теперь он не перезаписывает AppSettings, если используется параметр -AssignIdentity.</span><span class="sxs-lookup"><span data-stu-id="f18dd-679">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="f18dd-680">Командлет New-AzureRmWebAppSlot теперь учитывает дополнительный параметр AppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="f18dd-680">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="f18dd-681">6.2.1 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="f18dd-681">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="f18dd-682">AzureRM.OperationalInsights;</span><span class="sxs-lookup"><span data-stu-id="f18dd-682">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="f18dd-683">В обновленной модели PSWorkspace Network может использовать type в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="f18dd-683">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="f18dd-684">6.2.0 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="f18dd-684">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="f18dd-685">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="f18dd-685">AzureRM.Profile</span></span>
* <span data-ttu-id="f18dd-686">Исправлена ошибка с загрузкой Newtonsoft.Json версии 10.0.3 во время импорта модуля.</span><span class="sxs-lookup"><span data-stu-id="f18dd-686">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="f18dd-687">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="f18dd-687">AzureRM.Compute</span></span>
* <span data-ttu-id="f18dd-688">Функция обновления виртуальных машин VMSS.</span><span class="sxs-lookup"><span data-stu-id="f18dd-688">VMSS VM Update feature</span></span>
    - <span data-ttu-id="f18dd-689">Добавлены командлеты Update-AzureRmVmssVM и New-AzureRmVMDataDisk.</span><span class="sxs-lookup"><span data-stu-id="f18dd-689">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="f18dd-690">В командлет Add-AzureRmVMDataDisk добавлен параметр VirtualMachineScaleSetVM, который позволяет добавлять диски данных в виртуальные машины VMSS.</span><span class="sxs-lookup"><span data-stu-id="f18dd-690">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="f18dd-691">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f18dd-691">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="f18dd-692">Пакет SDK для ADF .NET обновлен до версии 0.8.0-preview. Новая версия содержит такие изменения:</span><span class="sxs-lookup"><span data-stu-id="f18dd-692">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="f18dd-693">добавлена операция для настройки репозитория фабрики;</span><span class="sxs-lookup"><span data-stu-id="f18dd-693">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="f18dd-694">связанная служба QuickBooks LinkedService теперь предоставляет свойства consumerKey и consumerSecret;</span><span class="sxs-lookup"><span data-stu-id="f18dd-694">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="f18dd-695">тип нескольких моделей изменен с SecretBase на Object;</span><span class="sxs-lookup"><span data-stu-id="f18dd-695">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="f18dd-696">добавлен триггер событий BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="f18dd-696">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="f18dd-697">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f18dd-697">AzureRM.KeyVault</span></span>
* <span data-ttu-id="f18dd-698">В документацию добавлены примеры выходных данных.</span><span class="sxs-lookup"><span data-stu-id="f18dd-698">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="f18dd-699">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="f18dd-699">AzureRM.Network</span></span>
* <span data-ttu-id="f18dd-700">В командлеты Наблюдателя за сетями добавлены параметры Аналитики трафика.</span><span class="sxs-lookup"><span data-stu-id="f18dd-700">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="f18dd-701">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="f18dd-701">AzureRM.Resources</span></span>
* <span data-ttu-id="f18dd-702">Исправлена ошибка, когда командлет Get-AzureRmResource возвращает свойство Properties объектов PSResource.</span><span class="sxs-lookup"><span data-stu-id="f18dd-702">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="f18dd-703">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="f18dd-703">AzureRM.Scheduler</span></span>
* <span data-ttu-id="f18dd-704">Исправлена ошибка, когда обновление ServiceBusQueueJob не задает новые значения для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="f18dd-704">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="f18dd-705">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="f18dd-705">AzureRM.Sql</span></span>
* <span data-ttu-id="f18dd-706">В перечисленные ниже командлеты добавлен необязательный параметр LicenseType.</span><span class="sxs-lookup"><span data-stu-id="f18dd-706">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="f18dd-707">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="f18dd-707">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="f18dd-708">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool;</span><span class="sxs-lookup"><span data-stu-id="f18dd-708">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="f18dd-709">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="f18dd-709">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="f18dd-710">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="f18dd-710">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="f18dd-711">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f18dd-711">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="f18dd-712">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="f18dd-712">AzureRM.Websites</span></span>
* <span data-ttu-id="f18dd-713">Командлет New-AzureRMWebApp теперь использует общие алгоритмы из библиотеки Strategy.</span><span class="sxs-lookup"><span data-stu-id="f18dd-713">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="f18dd-714">6.1.0 — май 2018 г.</span><span class="sxs-lookup"><span data-stu-id="f18dd-714">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="f18dd-715">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="f18dd-715">AzureRM.Profile</span></span>
* <span data-ttu-id="f18dd-716">Устранена проблема с выполнением Clear-AzureRmContext, при которой сохранялся пустой контекст с именем предыдущего контекста по умолчанию, что не позволяло пользователю создать новый контекст со старым именем.</span><span class="sxs-lookup"><span data-stu-id="f18dd-716">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="f18dd-717">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f18dd-717">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="f18dd-718">Включены операции связывания и отмены связи в автономной системе.</span><span class="sxs-lookup"><span data-stu-id="f18dd-718">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="f18dd-719">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f18dd-719">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="f18dd-720">Добавлена поддержка ApiVersions, ApiReleases и ApiRevisions.</span><span class="sxs-lookup"><span data-stu-id="f18dd-720">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="f18dd-721">Добавлена поддержка серверной части ServiceFabric.</span><span class="sxs-lookup"><span data-stu-id="f18dd-721">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="f18dd-722">Добавлена поддержка средства ведения журнала Application Insights.</span><span class="sxs-lookup"><span data-stu-id="f18dd-722">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="f18dd-723">Добавлена поддержка для распознавания номера SKU уровня "Базовый" как допустимого номера SKU службы управления API.</span><span class="sxs-lookup"><span data-stu-id="f18dd-723">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="f18dd-724">Добавлена поддержка установки сертификатов, выданных частным центром сертификации в качестве корневого или обычного ЦС.</span><span class="sxs-lookup"><span data-stu-id="f18dd-724">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="f18dd-725">Добавлена поддержка для приема пользовательских SSL-сертификатов с помощью KeyVault и нескольких имен узлов прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="f18dd-725">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="f18dd-726">Добавлена поддержка для удостоверения MSI.</span><span class="sxs-lookup"><span data-stu-id="f18dd-726">Added support for MSI identity</span></span>
* <span data-ttu-id="f18dd-727">Добавлена поддержка для принятия политик с помощью URL-адреса. Примечание. Указанные ниже командлеты в следующей версии будут отмечены как нерекомендуемые.</span><span class="sxs-lookup"><span data-stu-id="f18dd-727">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="f18dd-728">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="f18dd-728">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="f18dd-729">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="f18dd-729">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="f18dd-730">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="f18dd-730">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="f18dd-731">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="f18dd-731">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="f18dd-732">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="f18dd-732">AzureRM.Batch</span></span>
* <span data-ttu-id="f18dd-733">Выпущен новый командлет Get-AzureBatchPoolNodeCounts.</span><span class="sxs-lookup"><span data-stu-id="f18dd-733">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="f18dd-734">Выпущен новый командлет Start-AzureBatchComputeNodeServiceLogUpload.</span><span class="sxs-lookup"><span data-stu-id="f18dd-734">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="f18dd-735">AzureRM.Consumption:</span><span class="sxs-lookup"><span data-stu-id="f18dd-735">AzureRM.Consumption</span></span>
* <span data-ttu-id="f18dd-736">Добавлены новые параметры Expand, ResourceGroup, InstanceName, InstanceId, Tags и командлет высшего уровня Get-AzureRmConsumptionUsageDetail.</span><span class="sxs-lookup"><span data-stu-id="f18dd-736">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="f18dd-737">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f18dd-737">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="f18dd-738">Исправлен пример для Export-AzureRmDataLakeStoreChildItemProperties.</span><span class="sxs-lookup"><span data-stu-id="f18dd-738">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="f18dd-739">Исправлено исключение параметра NULL при использовании рекурсии в Set-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="f18dd-739">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="f18dd-740">Исправлены файлы справки для Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl и Remove-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="f18dd-740">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="f18dd-741">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="f18dd-741">AzureRM.Network</span></span>
* <span data-ttu-id="f18dd-742">Пакет SDK для сети обновлен с предварительной версии 18.0.0 до предварительной версии 19.0.0.</span><span class="sxs-lookup"><span data-stu-id="f18dd-742">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="f18dd-743">Добавлен командлет для создания конфигурации протокола.</span><span class="sxs-lookup"><span data-stu-id="f18dd-743">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="f18dd-744">New-AzureRmNetworkWatcherProtocolConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f18dd-744">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="f18dd-745">Добавлен командлет для добавления нового подключения канала к существующему каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f18dd-745">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="f18dd-746">Add-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="f18dd-746">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="f18dd-747">Добавлен командлет для удаления подключения канала к существующему каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f18dd-747">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="f18dd-748">Remove-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="f18dd-748">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="f18dd-749">Добавлен командлет для получения подключения канала.</span><span class="sxs-lookup"><span data-stu-id="f18dd-749">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="f18dd-750">Get-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="f18dd-750">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="f18dd-751">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f18dd-751">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="f18dd-752">Исправлена процедура аутентификации сервера с использованием созданных сертификатов (проблема № 5998).</span><span class="sxs-lookup"><span data-stu-id="f18dd-752">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="f18dd-753">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="f18dd-753">AzureRM.Sql</span></span>
* <span data-ttu-id="f18dd-754">Обновлены командлеты аудита, которые теперь позволяют удалять AuditActions или AuditActionGroups.</span><span class="sxs-lookup"><span data-stu-id="f18dd-754">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="f18dd-755">Исправлена проблема с Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy, при которой установка новой гибкой политики хранения завершалась ошибкой с сообщением "Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span><span class="sxs-lookup"><span data-stu-id="f18dd-755">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="f18dd-756">Please submit request with the new flexible retention policy" (Настройка политики долгосрочного хранения с помощью хранилища и политики служб восстановления Azure больше не поддерживается. Отправьте запрос с использованием новой гибкой политики хранения).</span><span class="sxs-lookup"><span data-stu-id="f18dd-756">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="f18dd-757">Обновлены все командлеты, связанные со службой "База данных SQL Azure", с созданием эластичных пулов и обновлением. Теперь используются новые API баз данных с поддержкой свойства номеров SKU для обеспечения масштабируемости и связанных с уровнями возможностей.</span><span class="sxs-lookup"><span data-stu-id="f18dd-757">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="f18dd-758">Обновлены командлеты, в том числе:</span><span class="sxs-lookup"><span data-stu-id="f18dd-758">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="f18dd-759">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="f18dd-759">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="f18dd-760">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool;</span><span class="sxs-lookup"><span data-stu-id="f18dd-760">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="f18dd-761">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="f18dd-761">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="f18dd-762">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="f18dd-762">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="f18dd-763">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f18dd-763">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="f18dd-764">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="f18dd-764">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="f18dd-765">Обновлены параметры для Get-AzureRmTrafficManagerProfile. Теперь при использовании параметра -Name требуется параметр -ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="f18dd-765">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
