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
ms.openlocfilehash: 6a33d1a85fc61d0281bf1183163185b0dc4d3a12
ms.sourcegitcommit: f6f5e256143aa6c097de3e57e930d8badea49f30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/18/2018
ms.locfileid: "49399065"
---
# <a name="release-notes"></a><span data-ttu-id="76bf9-103">Заметки о выпуске</span><span class="sxs-lookup"><span data-stu-id="76bf9-103">Release notes</span></span>

<span data-ttu-id="76bf9-104">Здесь приведен список изменений, внесенных в Azure PowerShell в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="76bf9-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6100---october-2018"></a><span data-ttu-id="76bf9-105">6.10.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="76bf9-105">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="76bf9-106">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="76bf9-106">Azure.Storage</span></span>
* <span data-ttu-id="76bf9-107">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="76bf9-107">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="76bf9-108">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="76bf9-108">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="76bf9-109">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="76bf9-109">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="76bf9-110">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="76bf9-110">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="76bf9-111">Поддержка Get-AzureRmCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="76bf9-111">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="76bf9-112">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="76bf9-112">AzureRM.Compute</span></span>
* <span data-ttu-id="76bf9-113">Исправлена команда Get-AzureRmVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов.</span><span class="sxs-lookup"><span data-stu-id="76bf9-113">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="76bf9-114">Добавлен пример использования SimpleParameterSet в справку командлета New-AzureRmVmss.</span><span class="sxs-lookup"><span data-stu-id="76bf9-114">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="76bf9-115">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="76bf9-115">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="76bf9-116">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="76bf9-116">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="76bf9-117">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="76bf9-117">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="76bf9-118">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="76bf9-118">AzureRM.Network</span></span>
* <span data-ttu-id="76bf9-119">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="76bf9-119">Added NetworkProfile functionality.</span></span> <span data-ttu-id="76bf9-120">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="76bf9-120">new cmdlets added</span></span>
    - <span data-ttu-id="76bf9-121">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="76bf9-121">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="76bf9-122">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="76bf9-122">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="76bf9-123">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="76bf9-123">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="76bf9-124">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="76bf9-124">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="76bf9-125">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="76bf9-125">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="76bf9-126">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="76bf9-126">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="76bf9-127">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="76bf9-127">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="76bf9-128">Добавлены командлеты: New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap.</span><span class="sxs-lookup"><span data-stu-id="76bf9-128">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="76bf9-129">Добавлены командлеты: Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="76bf9-129">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="76bf9-130">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="76bf9-130">AzureRM.RedisCache</span></span>
* <span data-ttu-id="76bf9-131">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="76bf9-131">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="76bf9-132">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="76bf9-132">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="76bf9-133">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="76bf9-133">AzureRM.Resources</span></span>
* <span data-ttu-id="76bf9-134">Добавлен отсутствующий параметр -Mode в командлет Set-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="76bf9-134">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="76bf9-135">Исправлена ошибка командлета Get-AzureRmProviderOperation для операций, когда Origin содержит User.</span><span class="sxs-lookup"><span data-stu-id="76bf9-135">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="76bf9-136">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="76bf9-136">AzureRM.Sql</span></span>
* <span data-ttu-id="76bf9-137">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="76bf9-137">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="76bf9-138">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="76bf9-138">AzureRM.Storage</span></span>
* <span data-ttu-id="76bf9-139">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="76bf9-139">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="76bf9-140">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="76bf9-140">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="76bf9-141">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="76bf9-141">AzureRM.Websites</span></span>
* <span data-ttu-id="76bf9-142">Новый командлет Get-AzureRMWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера.</span><span class="sxs-lookup"><span data-stu-id="76bf9-142">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="76bf9-143">Новые командлеты New-AzureRMWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows.</span><span class="sxs-lookup"><span data-stu-id="76bf9-143">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="76bf9-144">6.9.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="76bf9-144">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="76bf9-145">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="76bf9-145">General</span></span>
* <span data-ttu-id="76bf9-146">В модуль развертывания AzureRM добавлен командлет AzureRM.SignalR.</span><span class="sxs-lookup"><span data-stu-id="76bf9-146">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="76bf9-147">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="76bf9-147">AzureRM.Profile</span></span>
* <span data-ttu-id="76bf9-148">Незначительные изменения в общем коде хранилища.</span><span class="sxs-lookup"><span data-stu-id="76bf9-148">Minor changes to the storage common code</span></span>
* <span data-ttu-id="76bf9-149">Обновлены файлы справки, в которые добавлены полные типы параметров.</span><span class="sxs-lookup"><span data-stu-id="76bf9-149">Updated help files to include full parameter types.</span></span>
- <span data-ttu-id="76bf9-150">В наборе параметров ServicePrincipalCertificateWithSubscriptionId параметр -ServicePrincipal теперь стал необязательным.</span><span class="sxs-lookup"><span data-stu-id="76bf9-150">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="76bf9-151">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="76bf9-151">Azure.Storage</span></span>
* <span data-ttu-id="76bf9-152">Поддержка создания контекста хранилища с использованием OAuth.</span><span class="sxs-lookup"><span data-stu-id="76bf9-152">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="76bf9-153">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="76bf9-153">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="76bf9-154">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="76bf9-154">AzureRM.Cdn</span></span>
* <span data-ttu-id="76bf9-155">Добавлен номер SKU для расценок на Standard_Microsoft в CDN.</span><span class="sxs-lookup"><span data-stu-id="76bf9-155">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="76bf9-156">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="76bf9-156">AzureRM.Compute</span></span>
* <span data-ttu-id="76bf9-157">Keyvault и Storage перенесены в общие зависимости.</span><span class="sxs-lookup"><span data-stu-id="76bf9-157">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="76bf9-158">Добавлена поддержка большего количества размеров виртуальных машин в командлеты AEM.</span><span class="sxs-lookup"><span data-stu-id="76bf9-158">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="76bf9-159">Добавлен параметр PublicIPPrefix в командлет New-AzureRmVmssIpConfig.</span><span class="sxs-lookup"><span data-stu-id="76bf9-159">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="76bf9-160">Добавлен параметр ResourceId в командлет Invoke-AzureRmVMRunCommand.</span><span class="sxs-lookup"><span data-stu-id="76bf9-160">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="76bf9-161">Добавлен командлет Invoke-AzureRmVmssVMRunCommand.</span><span class="sxs-lookup"><span data-stu-id="76bf9-161">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="76bf9-162">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="76bf9-162">AzureRM.Dns</span></span>
* <span data-ttu-id="76bf9-163">Добавлена поддержка для псевдонима записи во время создания записи DNS.</span><span class="sxs-lookup"><span data-stu-id="76bf9-163">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="76bf9-164">AzureRM.Insights;</span><span class="sxs-lookup"><span data-stu-id="76bf9-164">AzureRM.Insights</span></span>
* <span data-ttu-id="76bf9-165">Исправлены проблемы № 6833 и № 7102 (область настроек диагностики).</span><span class="sxs-lookup"><span data-stu-id="76bf9-165">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="76bf9-166">Проблемы с именем по умолчанию, например service, во время создания, получения и отображения списка параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="76bf9-166">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="76bf9-167">Проблемы при создании параметров диагностики с категориями.</span><span class="sxs-lookup"><span data-stu-id="76bf9-167">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="76bf9-168">Добавлено сообщение о том, что не рекомендуется использовать параметры интервалов времени в метриках.</span><span class="sxs-lookup"><span data-stu-id="76bf9-168">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="76bf9-169">Параметры интервалов времени по-прежнему принимаются (это не критическое изменение), но они игнорируются в серверной части, потому что действительно только значение PT1M.</span><span class="sxs-lookup"><span data-stu-id="76bf9-169">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="76bf9-170">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="76bf9-170">AzureRM.Network</span></span>
* <span data-ttu-id="76bf9-171">Изменения командлетов LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="76bf9-171">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="76bf9-172">LoadBalancerInboundNatPoolConfig: добавлены параметры IdleTimeoutInMinutes, EnableFloatingIp и EnableTcpReset.</span><span class="sxs-lookup"><span data-stu-id="76bf9-172">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="76bf9-173">LoadBalancerInboundNatRuleConfig: добавлен параметр EnableTcpReset.</span><span class="sxs-lookup"><span data-stu-id="76bf9-173">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="76bf9-174">LoadBalancerRuleConfig: добавлен параметр EnableTcpReset.</span><span class="sxs-lookup"><span data-stu-id="76bf9-174">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="76bf9-175">LoadBalancerProbeConfig: добавлена поддержка значения Https для параметра Protocol.</span><span class="sxs-lookup"><span data-stu-id="76bf9-175">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="76bf9-176">Добавлены новые команды для нового правила OutboundRule подресурса LoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="76bf9-176">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="76bf9-177">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="76bf9-177">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="76bf9-178">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="76bf9-178">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="76bf9-179">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="76bf9-179">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="76bf9-180">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="76bf9-180">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="76bf9-181">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="76bf9-181">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="76bf9-182">Добавлено новое свойство HostedWorkloads для PSNetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="76bf9-182">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="76bf9-183">Добавлены новые командлеты для функции Брандмауэра Azure через ARM.</span><span class="sxs-lookup"><span data-stu-id="76bf9-183">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="76bf9-184">Добавлен командлет Get-AzureRmFirewall.</span><span class="sxs-lookup"><span data-stu-id="76bf9-184">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="76bf9-185">Добавлен командлет Set-AzureRmFirewall.</span><span class="sxs-lookup"><span data-stu-id="76bf9-185">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="76bf9-186">Добавлен командлет New-AzureRmFirewall.</span><span class="sxs-lookup"><span data-stu-id="76bf9-186">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="76bf9-187">Добавлен командлет Remove-AzureRmFirewall.</span><span class="sxs-lookup"><span data-stu-id="76bf9-187">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="76bf9-188">Добавлен командлет New-AzureRmFirewallApplicationRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="76bf9-188">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="76bf9-189">Добавлен командлет New-AzureRmFirewallApplicationRule.</span><span class="sxs-lookup"><span data-stu-id="76bf9-189">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="76bf9-190">Добавлен командлет New-AzureRmFirewallNatRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="76bf9-190">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="76bf9-191">Добавлен командлет New-AzureRmFirewallNatRule.</span><span class="sxs-lookup"><span data-stu-id="76bf9-191">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="76bf9-192">Добавлен командлет New-AzureRmFirewallNetworkRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="76bf9-192">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="76bf9-193">Добавлен командлет New-AzureRmFirewallNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="76bf9-193">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="76bf9-194">Добавлена поддержка конфигурации для доверенного корневого сертификата и автомасштабирования в Шлюзе приложений.</span><span class="sxs-lookup"><span data-stu-id="76bf9-194">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="76bf9-195">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="76bf9-195">New Cmdlets added:</span></span>
      - <span data-ttu-id="76bf9-196">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="76bf9-196">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="76bf9-197">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="76bf9-197">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="76bf9-198">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="76bf9-198">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="76bf9-199">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="76bf9-199">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="76bf9-200">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="76bf9-200">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="76bf9-201">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="76bf9-201">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="76bf9-202">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="76bf9-202">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="76bf9-203">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="76bf9-203">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="76bf9-204">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="76bf9-204">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="76bf9-205">В следующие командлеты добавлен необязательный параметр -TrustedRootCertificate:</span><span class="sxs-lookup"><span data-stu-id="76bf9-205">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="76bf9-206">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="76bf9-206">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="76bf9-207">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="76bf9-207">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="76bf9-208">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="76bf9-208">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="76bf9-209">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="76bf9-209">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="76bf9-210">В следующие командлеты добавлен необязательный параметр -AutoscaleConfiguration:</span><span class="sxs-lookup"><span data-stu-id="76bf9-210">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="76bf9-211">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="76bf9-211">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="76bf9-212">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="76bf9-212">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="76bf9-213">Добавлен командлет для конечной точки интерфейса Get-AzureInterfaceEndpoint.</span><span class="sxs-lookup"><span data-stu-id="76bf9-213">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="76bf9-214">Добавлена поддержка нескольких префиксов адресов в подсети.</span><span class="sxs-lookup"><span data-stu-id="76bf9-214">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="76bf9-215">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="76bf9-215">Updated cmdlets:</span></span>
  - <span data-ttu-id="76bf9-216">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="76bf9-216">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="76bf9-217">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="76bf9-217">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="76bf9-218">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="76bf9-218">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="76bf9-219">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="76bf9-219">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="76bf9-220">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="76bf9-220">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="76bf9-221">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="76bf9-221">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="76bf9-222">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="76bf9-222">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="76bf9-223">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="76bf9-223">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="76bf9-224">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="76bf9-224">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="76bf9-225">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="76bf9-225">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="76bf9-226">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="76bf9-226">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="76bf9-227">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="76bf9-227">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="76bf9-228">New-AzureRmNetworkInterfaceIpConfig — Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="76bf9-228">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="76bf9-229">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="76bf9-229">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="76bf9-230">Add-AzureRmVirtualNetworkGatewayIpConfig;</span><span class="sxs-lookup"><span data-stu-id="76bf9-230">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="76bf9-231">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="76bf9-231">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="76bf9-232">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="76bf9-232">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="76bf9-233">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="76bf9-233">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="76bf9-234">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="76bf9-234">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="76bf9-235">Добавлены командлеты для делегирования подсети.</span><span class="sxs-lookup"><span data-stu-id="76bf9-235">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="76bf9-236">New-AzureRmDelegation — создает делегирование, которое можно добавить к подсети.</span><span class="sxs-lookup"><span data-stu-id="76bf9-236">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="76bf9-237">Remove-AzureRmDelegation — принимает подсеть и удаляет указанное имя делегирования из этой подсети.</span><span class="sxs-lookup"><span data-stu-id="76bf9-237">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="76bf9-238">Add-AzureRmDelegation — принимает подсеть и добавляет указанное имя службы в качестве делегирования для этой подсети.</span><span class="sxs-lookup"><span data-stu-id="76bf9-238">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="76bf9-239">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="76bf9-239">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="76bf9-240">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="76bf9-240">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="76bf9-241">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="76bf9-241">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="76bf9-242">Добавлена поддержка управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="76bf9-242">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="76bf9-243">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="76bf9-243">AzureRM.RedisCache</span></span>
* <span data-ttu-id="76bf9-244">Обновлена зависимость Insights.</span><span class="sxs-lookup"><span data-stu-id="76bf9-244">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="76bf9-245">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="76bf9-245">AzureRM.Resources</span></span>
* <span data-ttu-id="76bf9-246">В командлет New-AzureRmResourceGroupDeployment добавлен новый параметр RollbackAction.</span><span class="sxs-lookup"><span data-stu-id="76bf9-246">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="76bf9-247">Добавлена поддержка OnErrorDeployment с новым параметром.</span><span class="sxs-lookup"><span data-stu-id="76bf9-247">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="76bf9-248">Добавлена поддержка управляемого удостоверения при назначении политик.</span><span class="sxs-lookup"><span data-stu-id="76bf9-248">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="76bf9-249">При назначении политики с помощью New-AzureRmPolicyAssignment параметры со значениями по умолчанию больше не требуются.</span><span class="sxs-lookup"><span data-stu-id="76bf9-249">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="76bf9-250">Добавлен новый командлет Get-AzureRmPolicyAlias для получения псевдонимов политик.</span><span class="sxs-lookup"><span data-stu-id="76bf9-250">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="76bf9-251">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="76bf9-251">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="76bf9-252">Устранена проблема № 7161.</span><span class="sxs-lookup"><span data-stu-id="76bf9-252">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="76bf9-253">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="76bf9-253">AzureRM.SignalR</span></span>
* <span data-ttu-id="76bf9-254">Обновлены номера SKU для Free_F1 и Standard_S1.</span><span class="sxs-lookup"><span data-stu-id="76bf9-254">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="76bf9-255">Добавлены поле версии в объект PSSignalRResource и строка подключения в объект PSSignalRKeys.</span><span class="sxs-lookup"><span data-stu-id="76bf9-255">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="76bf9-256">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="76bf9-256">AzureRM.Storage</span></span>
* <span data-ttu-id="76bf9-257">Добавлена поддержка политики неизменяемости в AzureRm.Storage.</span><span class="sxs-lookup"><span data-stu-id="76bf9-257">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="76bf9-258">Remove-AzureRmStorageAccountNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="76bf9-258">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="76bf9-259">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="76bf9-259">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="76bf9-260">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="76bf9-260">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="76bf9-261">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="76bf9-261">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="76bf9-262">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="76bf9-262">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="76bf9-263">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="76bf9-263">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="76bf9-264">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="76bf9-264">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="76bf9-265">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="76bf9-265">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="76bf9-266">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="76bf9-266">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="76bf9-267">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="76bf9-267">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="76bf9-268">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="76bf9-268">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="76bf9-269">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="76bf9-269">AzureRM.Websites</span></span>
* <span data-ttu-id="76bf9-270">Добавлены два новых командлета: Get-AzureRmDeletedWebApp и Restore-AzureRmDeletedWebApp.</span><span class="sxs-lookup"><span data-stu-id="76bf9-270">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="76bf9-271">New-AzureRmAppServicePlan: добавлен параметр -HyperV для создания плана службы приложений с контейнером Windows.</span><span class="sxs-lookup"><span data-stu-id="76bf9-271">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="76bf9-272">New-AzureRmWebApp, New-AzureRmWebAppSlot, Set-AzureRmWebApp, Set-AzureRmWebAppSlot: добавлены новые параметры (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) для создания контейнера приложения Windows и управления им.</span><span class="sxs-lookup"><span data-stu-id="76bf9-272">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="76bf9-273">6.8.1 — август 2018 г.</span><span class="sxs-lookup"><span data-stu-id="76bf9-273">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="76bf9-274">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="76bf9-274">General</span></span>
* <span data-ttu-id="76bf9-275">Исправлена проблема с отсутствием настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="76bf9-275">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="76bf9-276">Обновлены общие сборки среды выполнения</span><span class="sxs-lookup"><span data-stu-id="76bf9-276">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="76bf9-277">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="76bf9-277">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="76bf9-278">Исправлена проблема с отсутствием настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="76bf9-278">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="76bf9-279">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6603.</span><span class="sxs-lookup"><span data-stu-id="76bf9-279">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="76bf9-280">Командлеты Import-AzureRmApiManagementApi и \*-AzureRmApiManagementCertificate теперь обрабатывают относительные пути.</span><span class="sxs-lookup"><span data-stu-id="76bf9-280">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="76bf9-281">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6879.</span><span class="sxs-lookup"><span data-stu-id="76bf9-281">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="76bf9-282">CertificateInformation — это задаваемое свойство, обеспечивающее правильную работу командлета Set-AzureRmApiManagement.</span><span class="sxs-lookup"><span data-stu-id="76bf9-282">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="76bf9-283">Проблема исправлена путем обновления пакета NuGet до версии 4.0.4-preview.</span><span class="sxs-lookup"><span data-stu-id="76bf9-283">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="76bf9-284">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6853.</span><span class="sxs-lookup"><span data-stu-id="76bf9-284">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="76bf9-285">Исправлен фильтр OData для поиска по имени продукта.</span><span class="sxs-lookup"><span data-stu-id="76bf9-285">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="76bf9-286">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6814.</span><span class="sxs-lookup"><span data-stu-id="76bf9-286">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="76bf9-287">Исправлен фильтр OData для поиска по имени API.</span><span class="sxs-lookup"><span data-stu-id="76bf9-287">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="76bf9-288">Добавлена поддержка средства ведения журнала Azure Monitor.</span><span class="sxs-lookup"><span data-stu-id="76bf9-288">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="76bf9-289">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="76bf9-289">AzureRM.Compute</span></span>
* <span data-ttu-id="76bf9-290">Исправлена проблема с отсутствием в выходных данных ошибки целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="76bf9-290">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="76bf9-291">Исправлена проблема с типом учетной записи хранения для виртуальной машины с управляемым диском.</span><span class="sxs-lookup"><span data-stu-id="76bf9-291">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="76bf9-292">Исправлена проблема с отсутствием настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="76bf9-292">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="76bf9-293">Исправлены командлеты расширения AEM для других сред, например Azure для Китая.</span><span class="sxs-lookup"><span data-stu-id="76bf9-293">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="76bf9-294">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="76bf9-294">AzureRM.Network</span></span>
* <span data-ttu-id="76bf9-295">Стандартное представление выходных данных командлетов изменено на представление таблиц.</span><span class="sxs-lookup"><span data-stu-id="76bf9-295">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="76bf9-296">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="76bf9-296">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="76bf9-297">Исправлена проблема с Update-AzureRmPowerBIEmbeddedCapacity при попытке масштабировать приостановленную емкость.</span><span class="sxs-lookup"><span data-stu-id="76bf9-297">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="76bf9-298">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="76bf9-298">AzureRM.Resources</span></span>
* <span data-ttu-id="76bf9-299">Исправлена проблема с созданием управляемых приложений из Marketplace.</span><span class="sxs-lookup"><span data-stu-id="76bf9-299">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="76bf9-300">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="76bf9-300">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="76bf9-301">Исправленные проблемы</span><span class="sxs-lookup"><span data-stu-id="76bf9-301">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="76bf9-302">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="76bf9-302">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="76bf9-303">Добавлена поддержка метода маршрутизации MultiValue.</span><span class="sxs-lookup"><span data-stu-id="76bf9-303">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="76bf9-304">Добавлен новый параметр MaxReturn для маршрутизации MultiValue.</span><span class="sxs-lookup"><span data-stu-id="76bf9-304">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="76bf9-305">Добавлена поддержка метода маршрутизации Subnet.</span><span class="sxs-lookup"><span data-stu-id="76bf9-305">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="76bf9-306">Добавлена поддержка диапазонов IP-адресов (подсетей) в конечных точках.</span><span class="sxs-lookup"><span data-stu-id="76bf9-306">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="76bf9-307">Добавлена поддержка пользовательских заголовков в профилях.</span><span class="sxs-lookup"><span data-stu-id="76bf9-307">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="76bf9-308">Добавлена поддержка диапазонов кода ожидаемого состояния в профилях.</span><span class="sxs-lookup"><span data-stu-id="76bf9-308">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="76bf9-309">Добавлена поддержка пользовательских заголовков в конечных точках.</span><span class="sxs-lookup"><span data-stu-id="76bf9-309">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="76bf9-310">6.8.0 — август 2018 г.</span><span class="sxs-lookup"><span data-stu-id="76bf9-310">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="76bf9-311">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="76bf9-311">General</span></span>
* <span data-ttu-id="76bf9-312">Исправлена проблема с отсутствием настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="76bf9-312">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="76bf9-313">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="76bf9-313">AzureRM.Profile</span></span>
* <span data-ttu-id="76bf9-314">Добавлено свойство срока действия для маркеров, возвращенных при выполнении Connect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="76bf9-314">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="76bf9-315">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="76bf9-315">AzureRM.Compute</span></span>
* <span data-ttu-id="76bf9-316">Исправлена проблема с отсутствием в выходных данных ошибки целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="76bf9-316">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="76bf9-317">Исправлена проблема с типом учетной записи хранения для виртуальной машины с управляемым диском.</span><span class="sxs-lookup"><span data-stu-id="76bf9-317">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="76bf9-318">Исправлены командлеты расширения AEM для других сред, например Azure для Китая.</span><span class="sxs-lookup"><span data-stu-id="76bf9-318">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="76bf9-319">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="76bf9-319">AzureRM.IotHub</span></span>
* <span data-ttu-id="76bf9-320">Исправлены примеры для New-AzureRmIotHubExportDevices и New-AzureRmIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="76bf9-320">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="76bf9-321">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="76bf9-321">AzureRM.Network</span></span>
* <span data-ttu-id="76bf9-322">Изменено представление моделей по умолчанию на представление таблиц.</span><span class="sxs-lookup"><span data-stu-id="76bf9-322">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="76bf9-323">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="76bf9-323">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="76bf9-324">Исправлена проблема с Update-AzureRmPowerBIEmbeddedCapacity при попытке масштабировать приостановленную емкость.</span><span class="sxs-lookup"><span data-stu-id="76bf9-324">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="76bf9-325">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="76bf9-325">AzureRM.Resources</span></span>
* <span data-ttu-id="76bf9-326">Исправлена проблема с созданием управляемого приложения из marketplace.</span><span class="sxs-lookup"><span data-stu-id="76bf9-326">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="76bf9-327">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="76bf9-327">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="76bf9-328">Исправления проблем</span><span class="sxs-lookup"><span data-stu-id="76bf9-328">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="76bf9-329">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="76bf9-329">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="76bf9-330">Добавлена поддержка метода маршрутизации MultiValue.</span><span class="sxs-lookup"><span data-stu-id="76bf9-330">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="76bf9-331">Добавлен новый параметр MaxReturn для маршрутизации MultiValue.</span><span class="sxs-lookup"><span data-stu-id="76bf9-331">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="76bf9-332">Добавлена поддержка метода маршрутизации Subnet.</span><span class="sxs-lookup"><span data-stu-id="76bf9-332">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="76bf9-333">Добавлена поддержка диапазонов IP-адресов (подсетей) в конечных точках.</span><span class="sxs-lookup"><span data-stu-id="76bf9-333">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="76bf9-334">Добавлена поддержка пользовательских заголовков в профилях.</span><span class="sxs-lookup"><span data-stu-id="76bf9-334">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="76bf9-335">Добавлена поддержка диапазонов кода состояния ожидания в профилях.</span><span class="sxs-lookup"><span data-stu-id="76bf9-335">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="76bf9-336">Добавлена поддержка пользовательских заголовков в конечных точках.</span><span class="sxs-lookup"><span data-stu-id="76bf9-336">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="76bf9-337">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="76bf9-337">AzureRM.Websites</span></span>
* <span data-ttu-id="76bf9-338">Исправлена проблема с отсутствием правильной настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="76bf9-338">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="76bf9-339">6.7.0 — август 2018 г.</span><span class="sxs-lookup"><span data-stu-id="76bf9-339">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="76bf9-340">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="76bf9-340">AzureRM.Profile</span></span>
* <span data-ttu-id="76bf9-341">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-341">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="76bf9-342">Добавлен идентификатор пользователя для имени контекста по умолчанию, чтобы избежать конфликтов контекста.</span><span class="sxs-lookup"><span data-stu-id="76bf9-342">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="76bf9-343">Устранены проблемы с командлетом Clear-AzureRmContext, которые приводили к проблемам с выбором контекста #6398.</span><span class="sxs-lookup"><span data-stu-id="76bf9-343">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="76bf9-344">Разрешено передавать домен клиента в параметр -TenantId для командлета Connect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="76bf9-344">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="76bf9-345">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="76bf9-345">Azure.Storage</span></span>
* <span data-ttu-id="76bf9-346">Удалено ограничение в 5 ТБ для квоты на общую папку Azure.</span><span class="sxs-lookup"><span data-stu-id="76bf9-346">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="76bf9-347">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="76bf9-347">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="76bf9-348">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="76bf9-348">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="76bf9-349">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-349">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="76bf9-350">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="76bf9-350">Azure.AnalysisServices</span></span>
* <span data-ttu-id="76bf9-351">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-351">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="76bf9-352">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="76bf9-352">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="76bf9-353">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-353">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="76bf9-354">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="76bf9-354">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="76bf9-355">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-355">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="76bf9-356">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="76bf9-356">AzureRM.Automation</span></span>
* <span data-ttu-id="76bf9-357">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-357">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="76bf9-358">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="76bf9-358">AzureRM.Backup</span></span>
* <span data-ttu-id="76bf9-359">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-359">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="76bf9-360">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="76bf9-360">AzureRM.Batch</span></span>
* <span data-ttu-id="76bf9-361">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-361">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="76bf9-362">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="76bf9-362">AzureRM.Billing</span></span>
* <span data-ttu-id="76bf9-363">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-363">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="76bf9-364">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="76bf9-364">AzureRM.Cdn</span></span>
* <span data-ttu-id="76bf9-365">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-365">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="76bf9-366">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="76bf9-366">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="76bf9-367">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-367">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="76bf9-368">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="76bf9-368">AzureRM.Compute</span></span>
* <span data-ttu-id="76bf9-369">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-369">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="76bf9-370">В командлет New-AzureRmVmssConfig добавлен параметр EvictionPolicy.</span><span class="sxs-lookup"><span data-stu-id="76bf9-370">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="76bf9-371">Если расположение не указано, используйте в DiskFileParameterSet для New AzureRmVm расположение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="76bf9-371">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="76bf9-372">Исправлено описание параметров в Save-AzureRmVMImage.</span><span class="sxs-lookup"><span data-stu-id="76bf9-372">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="76bf9-373">Исправлен командлет Get-AzureRmVMDiskEncryptionStatus для определенных сценариев, связанных с однократным выполнением.</span><span class="sxs-lookup"><span data-stu-id="76bf9-373">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="76bf9-374">AzureRM.Consumption:</span><span class="sxs-lookup"><span data-stu-id="76bf9-374">AzureRM.Consumption</span></span>
* <span data-ttu-id="76bf9-375">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-375">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="76bf9-376">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="76bf9-376">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="76bf9-377">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-377">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="76bf9-378">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="76bf9-378">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="76bf9-379">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-379">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="76bf9-380">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="76bf9-380">AzureRM.DataFactories</span></span>
* <span data-ttu-id="76bf9-381">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-381">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="76bf9-382">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="76bf9-382">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="76bf9-383">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-383">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="76bf9-384">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="76bf9-384">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="76bf9-385">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-385">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="76bf9-386">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="76bf9-386">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="76bf9-387">Исправлена отладка, когда DebugPreference настраивается из командной строки PowerShell.</span><span class="sxs-lookup"><span data-stu-id="76bf9-387">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="76bf9-388">Обновлен пример для Set-AzureRmDataLakeStoreItemAcl.</span><span class="sxs-lookup"><span data-stu-id="76bf9-388">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="76bf9-389">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-389">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="76bf9-390">Обновлен пример для Set-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="76bf9-390">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="76bf9-391">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="76bf9-391">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="76bf9-392">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-392">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="76bf9-393">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="76bf9-393">AzureRM.Dns</span></span>
* <span data-ttu-id="76bf9-394">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-394">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="76bf9-395">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="76bf9-395">AzureRM.EventGrid</span></span>
* <span data-ttu-id="76bf9-396">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-396">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="76bf9-397">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="76bf9-397">AzureRM.EventHub</span></span>
* <span data-ttu-id="76bf9-398">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-398">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="76bf9-399">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="76bf9-399">AzureRM.HDInsight</span></span>
* <span data-ttu-id="76bf9-400">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-400">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="76bf9-401">AzureRM.Insights;</span><span class="sxs-lookup"><span data-stu-id="76bf9-401">AzureRM.Insights</span></span>
* <span data-ttu-id="76bf9-402">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-402">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="76bf9-403">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="76bf9-403">AzureRM.IotHub</span></span>
* <span data-ttu-id="76bf9-404">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-404">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="76bf9-405">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="76bf9-405">AzureRM.KeyVault</span></span>
* <span data-ttu-id="76bf9-406">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-406">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="76bf9-407">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="76bf9-407">AzureRM.LogicApp</span></span>
* <span data-ttu-id="76bf9-408">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-408">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="76bf9-409">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="76bf9-409">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="76bf9-410">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-410">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="76bf9-411">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="76bf9-411">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="76bf9-412">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-412">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="76bf9-413">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="76bf9-413">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="76bf9-414">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-414">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="76bf9-415">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="76bf9-415">AzureRM.Media</span></span>
* <span data-ttu-id="76bf9-416">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-416">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="76bf9-417">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="76bf9-417">AzureRM.Network</span></span>
* <span data-ttu-id="76bf9-418">Добавлен пример для Set-AzureRmLocalNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="76bf9-418">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="76bf9-419">Добавлены примеры и описания для Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey и New-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="76bf9-419">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="76bf9-420">Добавлены примеры для Remove-AzureRmVirtualNetworkGatewayIpConfig и Reset-AzureRmVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="76bf9-420">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="76bf9-421">Добавлен пример для Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.</span><span class="sxs-lookup"><span data-stu-id="76bf9-421">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="76bf9-422">Добавлен пример для Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.</span><span class="sxs-lookup"><span data-stu-id="76bf9-422">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="76bf9-423">Добавлен пример для Set-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="76bf9-423">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="76bf9-424">Повторно созданы командлеты для ApplicationSecurityGroup, RouteTable и Usage с помощью генератора кода последней версии.</span><span class="sxs-lookup"><span data-stu-id="76bf9-424">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="76bf9-425">Уточнено сообщение об ошибке для Get-AzureRmVirtualNetworkSubnetConfig при попытке получить подсеть, которая не существует.</span><span class="sxs-lookup"><span data-stu-id="76bf9-425">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="76bf9-426">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="76bf9-426">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="76bf9-427">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-427">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="76bf9-428">AzureRM.OperationalInsights;</span><span class="sxs-lookup"><span data-stu-id="76bf9-428">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="76bf9-429">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-429">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="76bf9-430">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="76bf9-430">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="76bf9-431">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-431">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="76bf9-432">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="76bf9-432">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="76bf9-433">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-433">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="76bf9-434">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="76bf9-434">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="76bf9-435">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-435">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="76bf9-436">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="76bf9-436">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="76bf9-437">Добавлен фильтр политик для командлета Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="76bf9-437">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="76bf9-438">Команда возвращает список элементов резервного копирования, защищенных политикой с заданным идентификатором.</span><span class="sxs-lookup"><span data-stu-id="76bf9-438">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="76bf9-439">Обновление Microsoft.Azure.Management.RecoveryServices.Backup до версии 3.0.0-preview.</span><span class="sxs-lookup"><span data-stu-id="76bf9-439">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="76bf9-440">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-440">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="76bf9-441">Добавлен параметр TargetResourceGroupName для Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="76bf9-441">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="76bf9-442">Группа ресурсов, в которую восстанавливаются управляемые диски.</span><span class="sxs-lookup"><span data-stu-id="76bf9-442">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="76bf9-443">Применимо к резервной копии виртуальной машины с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="76bf9-443">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="76bf9-444">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="76bf9-444">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="76bf9-445">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-445">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="76bf9-446">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="76bf9-446">AzureRM.RedisCache</span></span>
* <span data-ttu-id="76bf9-447">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-447">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="76bf9-448">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="76bf9-448">AzureRM.Relay</span></span>
* <span data-ttu-id="76bf9-449">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-449">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="76bf9-450">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="76bf9-450">AzureRM.Resources</span></span>
* <span data-ttu-id="76bf9-451">Поддержка развертывания шаблонов в области подписки.</span><span class="sxs-lookup"><span data-stu-id="76bf9-451">Support template deployment at subscription scope.</span></span> <span data-ttu-id="76bf9-452">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="76bf9-452">Add new Cmdlets:</span></span>
    - <span data-ttu-id="76bf9-453">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="76bf9-453">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="76bf9-454">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="76bf9-454">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="76bf9-455">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="76bf9-455">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="76bf9-456">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="76bf9-456">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="76bf9-457">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="76bf9-457">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="76bf9-458">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="76bf9-458">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="76bf9-459">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="76bf9-459">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="76bf9-460">Устранена проблема, когда при передаче контекста в Set-AzureRmResource возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="76bf9-460">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="76bf9-461">Исправлен пример в New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="76bf9-461">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="76bf9-462">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-462">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="76bf9-463">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="76bf9-463">AzureRM.Scheduler</span></span>
* <span data-ttu-id="76bf9-464">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-464">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="76bf9-465">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="76bf9-465">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="76bf9-466">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-466">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="76bf9-467">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="76bf9-467">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="76bf9-468">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-468">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="76bf9-469">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="76bf9-469">AzureRM.Sql</span></span>
* <span data-ttu-id="76bf9-470">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-470">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="76bf9-471">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="76bf9-471">AzureRM.Storage</span></span>
* <span data-ttu-id="76bf9-472">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-472">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="76bf9-473">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="76bf9-473">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="76bf9-474">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-474">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="76bf9-475">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="76bf9-475">AzureRM.Tags</span></span>
* <span data-ttu-id="76bf9-476">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-476">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="76bf9-477">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="76bf9-477">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="76bf9-478">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-478">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="76bf9-479">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="76bf9-479">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="76bf9-480">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-480">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="76bf9-481">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="76bf9-481">AzureRM.Websites</span></span>
* <span data-ttu-id="76bf9-482">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-482">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="76bf9-483">6.6.0 — июль 2018 г.</span><span class="sxs-lookup"><span data-stu-id="76bf9-483">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="76bf9-484">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="76bf9-484">General</span></span>
* <span data-ttu-id="76bf9-485">Обновлены все файлы справки: включены полные типы параметров и исправлены типы входных и выходных данных.</span><span class="sxs-lookup"><span data-stu-id="76bf9-485">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="76bf9-486">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="76bf9-486">AzureRM.Profile</span></span>
* <span data-ttu-id="76bf9-487">Обновлена библиотека Common.Strategy: теперь можно проверить, совместима ли текущая конфигурация ресурса с целевым ресурсом.</span><span class="sxs-lookup"><span data-stu-id="76bf9-487">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="76bf9-488">В Common.Storage добавлены типы ps1xml.</span><span class="sxs-lookup"><span data-stu-id="76bf9-488">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="76bf9-489">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="76bf9-489">Azure.Storage</span></span>
* <span data-ttu-id="76bf9-490">Добавлена поддержка для получения контекста хранилища из DefaultProfile.</span><span class="sxs-lookup"><span data-stu-id="76bf9-490">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="76bf9-491">В свойства типов выходных данных командлетов добавлен атрибут Ps1XmlAttribute.</span><span class="sxs-lookup"><span data-stu-id="76bf9-491">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="76bf9-492">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="76bf9-492">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="76bf9-493">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6370.</span><span class="sxs-lookup"><span data-stu-id="76bf9-493">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="76bf9-494">В AutoMapper исправлена ошибка, препятствовавшая преобразованию PsApiManagementApi в ApiContract.</span><span class="sxs-lookup"><span data-stu-id="76bf9-494">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="76bf9-495">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6515.</span><span class="sxs-lookup"><span data-stu-id="76bf9-495">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="76bf9-496">В File.Save исправлена ошибка, связанная с перегрузкой типом кодировки.</span><span class="sxs-lookup"><span data-stu-id="76bf9-496">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="76bf9-497">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6560.</span><span class="sxs-lookup"><span data-stu-id="76bf9-497">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="76bf9-498">Выполнено обновление до версии NuGet 4.0.3, что позволило исправить исключение шаблона в apiId.</span><span class="sxs-lookup"><span data-stu-id="76bf9-498">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="76bf9-499">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="76bf9-499">AzureRM.Compute</span></span>
* <span data-ttu-id="76bf9-500">Устранена ошибка при создании виртуальной машины с помощью командлета New-AzureRmVm и параметра DiskFileParameterSet, которая возникала из-за переименования типа учетной записи хранения PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="76bf9-500">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="76bf9-501">Исправлен командлет Invoke-AzureRmVMRunCommand.</span><span class="sxs-lookup"><span data-stu-id="76bf9-501">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="76bf9-502">Командлет Get-AzureRmAvailabilitySet теперь может выводить список всех групп доступности в подписке.</span><span class="sxs-lookup"><span data-stu-id="76bf9-502">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="76bf9-503">(Параметр ResouceGroupName теперь является необязательным.)</span><span class="sxs-lookup"><span data-stu-id="76bf9-503">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="76bf9-504">Обновлен параметр SimpleParameterSet командлета New-AzureRmVm, что позволило использовать ускоренную сеть на соответствующих виртуальных машинах.</span><span class="sxs-lookup"><span data-stu-id="76bf9-504">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="76bf9-505">Обновлен простой набор параметров New-AzureRmVmss, что позволило отменять создание масштабируемого набора виртуальных машин, если указанная пользователем подсистема балансировки нагрузки уже существует.</span><span class="sxs-lookup"><span data-stu-id="76bf9-505">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="76bf9-506">Обновлен пример для New-AzureRmDisk.</span><span class="sxs-lookup"><span data-stu-id="76bf9-506">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="76bf9-507">Добавлен пример для New-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="76bf9-507">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="76bf9-508">Обновлено описание командлета Set-AzureRmVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="76bf9-508">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="76bf9-509">Обновлен пример 1 для Set-AzureRmVMBginfoExtension: исправлены орфографические ошибки и префикс.</span><span class="sxs-lookup"><span data-stu-id="76bf9-509">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="76bf9-510">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="76bf9-510">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="76bf9-511">Пакет .NET SDK для ADF обновлен до версии 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="76bf9-511">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="76bf9-512">Добавлена поддержка совместного использования локальной среды IR несколькими фабриками данных.</span><span class="sxs-lookup"><span data-stu-id="76bf9-512">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="76bf9-513">Добавлен новый параметр -SharedIntegrationRuntimeResourceId для командлета Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-513">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="76bf9-514">Добавлен новый необязательный параметр -LinkedDataFactoryName для командлета Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="76bf9-514">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="76bf9-515">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="76bf9-515">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="76bf9-516">Пакет SDK для плоскости данных (Microsoft.Azure.DataLake.Store) обновлен до версии 1.1.9.</span><span class="sxs-lookup"><span data-stu-id="76bf9-516">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="76bf9-517">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="76bf9-517">AzureRM.EventHub</span></span>
* <span data-ttu-id="76bf9-518">Обновлена конвейерная передача для InputObject и ResourceId в командлетах remove.</span><span class="sxs-lookup"><span data-stu-id="76bf9-518">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="76bf9-519">AzureRM.Insights;</span><span class="sxs-lookup"><span data-stu-id="76bf9-519">AzureRM.Insights</span></span>
* <span data-ttu-id="76bf9-520">Исправлено форматирование OutputType в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="76bf9-520">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="76bf9-521">Применен пакет SDK Microsoft.Azure.Management.Monitor 0.19.1-preview.</span><span class="sxs-lookup"><span data-stu-id="76bf9-521">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="76bf9-522">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="76bf9-522">AzureRM.KeyVault</span></span>
* <span data-ttu-id="76bf9-523">Исправлена проблема с конвейерной передачей в командлете Set-AzureRmKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="76bf9-523">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="76bf9-524">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="76bf9-524">AzureRM.Network</span></span>
* <span data-ttu-id="76bf9-525">Добавлены примеры для командлетов LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="76bf9-525">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="76bf9-526">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="76bf9-526">AzureRM.Resources</span></span>
* <span data-ttu-id="76bf9-527">Устранена проблема, возникавшая при указании имени и значения тега для Get-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="76bf9-527">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="76bf9-528">Исправлен сценарий конвейерной передачи в Set-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="76bf9-528">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="76bf9-529">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="76bf9-529">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="76bf9-530">Обновлена конвейерная передача для InputObject и ResourceId в командлетах remove.</span><span class="sxs-lookup"><span data-stu-id="76bf9-530">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="76bf9-531">Исправлено несколько ошибок.</span><span class="sxs-lookup"><span data-stu-id="76bf9-531">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="76bf9-532">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="76bf9-532">AzureRM.Sql</span></span>
* <span data-ttu-id="76bf9-533">Добавлена поддержка Advanced Threat Protection для сервера с помощью следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="76bf9-533">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="76bf9-534">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="76bf9-534">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="76bf9-535">Добавлена поддержка оценки уязвимостей с помощью следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="76bf9-535">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="76bf9-536">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings;</span><span class="sxs-lookup"><span data-stu-id="76bf9-536">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="76bf9-537">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline;</span><span class="sxs-lookup"><span data-stu-id="76bf9-537">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="76bf9-538">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan.</span><span class="sxs-lookup"><span data-stu-id="76bf9-538">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="76bf9-539">Исправлен пример для Remove-AzureRmSqlServerFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="76bf9-539">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="76bf9-540">Исправлена неправильная обработка даты и времени для базового языка и региональных параметров, отличных от США, в Get-AzureSqlSyncGroupLog.</span><span class="sxs-lookup"><span data-stu-id="76bf9-540">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="76bf9-541">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="76bf9-541">AzureRM.Storage</span></span>
* <span data-ttu-id="76bf9-542">В свойства типов выходных данных командлетов добавлен атрибут Ps1XmlAttribute.</span><span class="sxs-lookup"><span data-stu-id="76bf9-542">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="76bf9-543">Выходные данные командлетов StorageAccount теперь отображаются в виде таблицы.</span><span class="sxs-lookup"><span data-stu-id="76bf9-543">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="76bf9-544">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="76bf9-544">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="76bf9-545">New-AzureRmStorageAccount;</span><span class="sxs-lookup"><span data-stu-id="76bf9-545">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="76bf9-546">Set-AzureRmStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="76bf9-546">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="76bf9-547">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="76bf9-547">AzureRM.Tags</span></span>
* <span data-ttu-id="76bf9-548">Удалено неверное утверждение из справки по командлетам Tag.</span><span class="sxs-lookup"><span data-stu-id="76bf9-548">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="76bf9-549">6.5.0 — июль 2018 г.</span><span class="sxs-lookup"><span data-stu-id="76bf9-549">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="76bf9-550">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="76bf9-550">AzureRM.Profile</span></span>
* <span data-ttu-id="76bf9-551">Обновлена справка для командлета Get-AzureRmContextAutosaveSetting.</span><span class="sxs-lookup"><span data-stu-id="76bf9-551">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="76bf9-552">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="76bf9-552">Azure.Storage</span></span>
* <span data-ttu-id="76bf9-553">Добавлена поддержка отправки BLOB-объекта или файла с помощью токена SAS, доступного только для записи.</span><span class="sxs-lookup"><span data-stu-id="76bf9-553">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="76bf9-554">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="76bf9-554">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="76bf9-555">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="76bf9-555">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="76bf9-556">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="76bf9-556">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="76bf9-557">Для AS добавлено обязательное свойство ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="76bf9-557">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="76bf9-558">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="76bf9-558">AzureRM.Automation</span></span>
* <span data-ttu-id="76bf9-559">Обновлена справка и добавлены примеры для командлета New-AzureRMAutomationSchedule.</span><span class="sxs-lookup"><span data-stu-id="76bf9-559">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="76bf9-560">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="76bf9-560">AzureRM.Compute</span></span>
* <span data-ttu-id="76bf9-561">Добавлен параметр -Tag для командлета Update/New-AzureRmAvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="76bf9-561">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="76bf9-562">Добавлен пример для командлета Add-AzureRmVmssExtension.</span><span class="sxs-lookup"><span data-stu-id="76bf9-562">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="76bf9-563">Добавлены примеры для командлета Remove-AzureRmVmssExtension.</span><span class="sxs-lookup"><span data-stu-id="76bf9-563">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="76bf9-564">Обновлена справка для командлета Set-AzureRmVMAccessExtension.</span><span class="sxs-lookup"><span data-stu-id="76bf9-564">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="76bf9-565">Изменен класс SimpleParameterSet для командлета New-AzureRmVmss: теперь для SinglePlacementGroup по умолчанию задается значение false, а также добавляется параметр-переключатель SinglePlacementGroup, который позволяет пользователю создать VMSS в одной группе размещения.</span><span class="sxs-lookup"><span data-stu-id="76bf9-565">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="76bf9-566">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="76bf9-566">AzureRM.EventHub</span></span>
* <span data-ttu-id="76bf9-567">В класс PSEventHubDRConfigurationAttributes добавлено доступное только для чтения свойство PendingReplicationOperationsCount, которое показывает количество ожидающих репликации операций во время реплицирования.</span><span class="sxs-lookup"><span data-stu-id="76bf9-567">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="76bf9-568">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="76bf9-568">AzureRM.KeyVault</span></span>
* <span data-ttu-id="76bf9-569">Обновлено сообщение об ошибке для командлета Set-AzureRmKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="76bf9-569">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="76bf9-570">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="76bf9-570">AzureRM.LogicApp</span></span>
* <span data-ttu-id="76bf9-571">Исправлена ошибка "parameter set could not be resolved" (не удалось разрешить заданный параметр) в командлете New-AzureRmLogicApp.</span><span class="sxs-lookup"><span data-stu-id="76bf9-571">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="76bf9-572">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="76bf9-572">AzureRM.Network</span></span>
* <span data-ttu-id="76bf9-573">Включен пиринг между виртуальными сетями в нескольких клиентах для командлета Set/Add-AzureRmVirtualNetworkPeering.</span><span class="sxs-lookup"><span data-stu-id="76bf9-573">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="76bf9-574">Для шлюза приложений обновлены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="76bf9-574">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="76bf9-575">New-AzureRmApplicationGateway: добавлены флаг EnableFIPS и поддержка зон.</span><span class="sxs-lookup"><span data-stu-id="76bf9-575">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="76bf9-576">New-AzureRmApplicationGatewaySku: добавлены новые номера SKU Standard_v2 и WAF_v2.</span><span class="sxs-lookup"><span data-stu-id="76bf9-576">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="76bf9-577">Set-AzureRmApplicationGatewaySku: добавлены новые номера SKU Standard_v2 и WAF_v2.</span><span class="sxs-lookup"><span data-stu-id="76bf9-577">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="76bf9-578">Командлеты RouteTable пересозданы в последней версии генератора.</span><span class="sxs-lookup"><span data-stu-id="76bf9-578">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="76bf9-579">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="76bf9-579">AzureRM.Relay</span></span>
* <span data-ttu-id="76bf9-580">Обновлены файлы Markdown, исправлена проблема с именем параметра в примере.</span><span class="sxs-lookup"><span data-stu-id="76bf9-580">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="76bf9-581">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="76bf9-581">AzureRM.Resources</span></span>
* <span data-ttu-id="76bf9-582">Обновлены командлеты Roleassignment и roledefinition:</span><span class="sxs-lookup"><span data-stu-id="76bf9-582">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="76bf9-583">Удалены лишние вызовы roledefinition, выполняемые в ходе разбиения на страницы.</span><span class="sxs-lookup"><span data-stu-id="76bf9-583">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="76bf9-584">Исправлен командлет Get-AzureRmRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="76bf9-584">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="76bf9-585">Исправлена работа параметра -ExpandPrincipalGroups.</span><span class="sxs-lookup"><span data-stu-id="76bf9-585">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="76bf9-586">Устранена проблема в командлете Get-AzureRmResource, заключающая в том, что в параметре -ResourceType учитывался регистр символов.</span><span class="sxs-lookup"><span data-stu-id="76bf9-586">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="76bf9-587">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="76bf9-587">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="76bf9-588">Добавлены параметры top и skip для командлетов list.</span><span class="sxs-lookup"><span data-stu-id="76bf9-588">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="76bf9-589">Добавлены командлеты для перехода с пространства имен ценовой категории "Стандартный" на пространство ценовой категории "Премиум":</span><span class="sxs-lookup"><span data-stu-id="76bf9-589">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="76bf9-590">Start-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="76bf9-590">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="76bf9-591">Get-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="76bf9-591">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="76bf9-592">Complete-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="76bf9-592">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="76bf9-593">Stop-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="76bf9-593">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="76bf9-594">Remove-AzureRmServiceBusMigration.</span><span class="sxs-lookup"><span data-stu-id="76bf9-594">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="76bf9-595">В класс PSServiceBusDRConfigurationAttributes добавлено доступное только для чтения свойство PendingReplicationOperationsCount, которое показывает количество ожидающих репликации операций во время реплицирования.</span><span class="sxs-lookup"><span data-stu-id="76bf9-595">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="76bf9-596">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="76bf9-596">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="76bf9-597">Обновлен пример для командлета New-AzureRmServiceFabricCluster.</span><span class="sxs-lookup"><span data-stu-id="76bf9-597">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="76bf9-598">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="76bf9-598">AzureRM.Sql</span></span>
* <span data-ttu-id="76bf9-599">Добавлены новые командлеты для Management.Sql, позволяющие клиентам добавлять сертификат TDE в экземпляр SQL Server или управляемый экземпляр:</span><span class="sxs-lookup"><span data-stu-id="76bf9-599">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="76bf9-600">Add-AzureRmSqlServerTransparentDataEncryptionCertificate;</span><span class="sxs-lookup"><span data-stu-id="76bf9-600">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="76bf9-601">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate.</span><span class="sxs-lookup"><span data-stu-id="76bf9-601">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="76bf9-602">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="76bf9-602">AzureRM.Websites</span></span>
* <span data-ttu-id="76bf9-603">`Set-AzureRmWebApp -AssignIdentity` и `Set-AzureRmWebAppSlot -AssignIdentity` при установленном значении false теперь будут удалять свойство Identity из объекта сайта. Также при этом будет удаляться тег предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="76bf9-603">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="76bf9-604">Обновлен пример для `Get-AzureRmWebAppMetrics` и `Get-AzureRmAppServicePlanMetrics`.</span><span class="sxs-lookup"><span data-stu-id="76bf9-604">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="76bf9-605">`Set-AzureRmWebApp -PhpVersion` теперь поддерживает off как допустимую версию PHP.</span><span class="sxs-lookup"><span data-stu-id="76bf9-605">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="76bf9-606">6.4.0 — июль 2018 г.</span><span class="sxs-lookup"><span data-stu-id="76bf9-606">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="76bf9-607">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="76bf9-607">General</span></span>
* <span data-ttu-id="76bf9-608">Исправлено форматирование OutputType в файлах справки для большинства модулей.</span><span class="sxs-lookup"><span data-stu-id="76bf9-608">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="76bf9-609">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="76bf9-609">AzureRM.Profile</span></span>
* <span data-ttu-id="76bf9-610">В основные типы выходных данных добавлен атрибут Ps1Xml.</span><span class="sxs-lookup"><span data-stu-id="76bf9-610">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="76bf9-611">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="76bf9-611">AzureRM.Compute</span></span>
* <span data-ttu-id="76bf9-612">Функция добавления тега IP-адреса для масштабируемого набора виртуальных машин (VMSS)</span><span class="sxs-lookup"><span data-stu-id="76bf9-612">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="76bf9-613">Добавлен командлет New-AzureRmVmssIpTagConfig.</span><span class="sxs-lookup"><span data-stu-id="76bf9-613">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="76bf9-614">В New-AzureRmVmssIpConfig добавлен параметр IpTag.</span><span class="sxs-lookup"><span data-stu-id="76bf9-614">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="76bf9-615">Функция автоматического отката ОС для VMSS</span><span class="sxs-lookup"><span data-stu-id="76bf9-615">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="76bf9-616">В New-AzureRmVmssConfig и Update-AzureRmVmss добавлены параметры DisableAutoRollback.</span><span class="sxs-lookup"><span data-stu-id="76bf9-616">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="76bf9-617">Функция ведения журнала обновлений ОС для VMSS</span><span class="sxs-lookup"><span data-stu-id="76bf9-617">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="76bf9-618">В Get-AzureRmVmss добавлен параметр OSUpgradeHistory.</span><span class="sxs-lookup"><span data-stu-id="76bf9-618">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="76bf9-619">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="76bf9-619">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="76bf9-620">Добавлена поддержка списков управления доступом к каталогу с использованием следующих команд:</span><span class="sxs-lookup"><span data-stu-id="76bf9-620">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="76bf9-621">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry;</span><span class="sxs-lookup"><span data-stu-id="76bf9-621">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="76bf9-622">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry;</span><span class="sxs-lookup"><span data-stu-id="76bf9-622">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="76bf9-623">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="76bf9-623">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="76bf9-624">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="76bf9-624">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="76bf9-625">Добавлены поддержка отмены выполнения и отслеживание хода выполнения для Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl и Remove-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="76bf9-625">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="76bf9-626">Добавлена поддержка отмены выполнения для Export-AzureRmDataLakeStoreChildItemProperties.</span><span class="sxs-lookup"><span data-stu-id="76bf9-626">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="76bf9-627">Исправлена очистка сообщений об отладке для командлетов, которые выполняют рекурсивные операции.</span><span class="sxs-lookup"><span data-stu-id="76bf9-627">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="76bf9-628">Исправлено расположение тестовых данных для командлетов DataLake.</span><span class="sxs-lookup"><span data-stu-id="76bf9-628">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="76bf9-629">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="76bf9-629">AzureRM.EventHub</span></span>
* <span data-ttu-id="76bf9-630">Для командлетов вывода списка операций Get-AzureRmEventHub и Get-AzureRmEventHubConsumerGroup добавлен необязательный параметр MaxCount.</span><span class="sxs-lookup"><span data-stu-id="76bf9-630">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="76bf9-631">Исправлена проблема с командлетом New-AzureRmEventHub, из-за которой требовалось указать по крайней мере один параметр при создании концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="76bf9-631">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="76bf9-632">Добавлен набор параметров по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="76bf9-632">Provided Default Parameter set.</span></span>
* <span data-ttu-id="76bf9-633">Для командлета New-AzureRmEventHubKey добавлен необязательный параметр -KeyValue, который позволяет пользователю предоставить значение ключа.</span><span class="sxs-lookup"><span data-stu-id="76bf9-633">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="76bf9-634">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="76bf9-634">AzureRM.KeyVault</span></span>
* <span data-ttu-id="76bf9-635">Исправлена ошибка, из-за которой при выполнении командлета Get-AzureRmKeyVault с параметром -Tag возвращались все ресурсы.</span><span class="sxs-lookup"><span data-stu-id="76bf9-635">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="76bf9-636">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="76bf9-636">AzureRM.Network</span></span>
* <span data-ttu-id="76bf9-637">Для параметра шлюзов виртуальной вести, избыточных в пределах зоны, предоставлены новые номера SKU.</span><span class="sxs-lookup"><span data-stu-id="76bf9-637">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="76bf9-638">Добавлены новые команды для функции поддержки партнерских API для ExpressRoute, развертываемых с помощью ARM:</span><span class="sxs-lookup"><span data-stu-id="76bf9-638">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="76bf9-639">добавлена команда Get-AzureRmExpressRouteCrossConnection;</span><span class="sxs-lookup"><span data-stu-id="76bf9-639">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="76bf9-640">добавлена команда Set-AzureRmExpressRouteCrossConnection;</span><span class="sxs-lookup"><span data-stu-id="76bf9-640">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="76bf9-641">добавлена команда Add-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="76bf9-641">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="76bf9-642">добавлена команда Get-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="76bf9-642">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="76bf9-643">добавлена команда Remove-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="76bf9-643">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="76bf9-644">добавлена команда Get-AzureRMExpressRouteCrossConnectionArpTable;</span><span class="sxs-lookup"><span data-stu-id="76bf9-644">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="76bf9-645">добавлена команда Get-AzureRMExpressRouteCrossConnectionRouteTable;</span><span class="sxs-lookup"><span data-stu-id="76bf9-645">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="76bf9-646">добавлена команда Get-AzureRMExpressRouteCrossConnectionRouteTableSummary.</span><span class="sxs-lookup"><span data-stu-id="76bf9-646">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="76bf9-647">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="76bf9-647">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="76bf9-648">Добавлен командлет Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="76bf9-648">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="76bf9-649">Этот командлет принимает идентификатор виртуальной машины и проверяет, защищена ли виртуальная машина с помощью какого-либо хранилища в подписке.</span><span class="sxs-lookup"><span data-stu-id="76bf9-649">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="76bf9-650">Если такое хранилище существует, командлет выводит данные о нем.</span><span class="sxs-lookup"><span data-stu-id="76bf9-650">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="76bf9-651">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="76bf9-651">AzureRM.Resources</span></span>
* <span data-ttu-id="76bf9-652">Обновлены командлеты Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="76bf9-652">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="76bf9-653">Добавлена поддержка вывода списка значений параметра -Scope на уровне группы управления.</span><span class="sxs-lookup"><span data-stu-id="76bf9-653">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="76bf9-654">Добавлена поддержка для получения отдельных назначений со значениями -Scope на уровне группы управления.</span><span class="sxs-lookup"><span data-stu-id="76bf9-654">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="76bf9-655">Для параметра управления добавлены параметры -Effective и -All.</span><span class="sxs-lookup"><span data-stu-id="76bf9-655">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="76bf9-656">Обновлены командлеты Get/New/Remove/Set-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="76bf9-656">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="76bf9-657">Добавлен параметр -ManagementGroupName для применения операций к заданной группе управления.</span><span class="sxs-lookup"><span data-stu-id="76bf9-657">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="76bf9-658">Добавлен параметр -SubscriptionId для применения операций к заданной подписке.</span><span class="sxs-lookup"><span data-stu-id="76bf9-658">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="76bf9-659">Обновлены командлеты Get/New/Remove/Set-AzureRmPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="76bf9-659">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="76bf9-660">Добавлен параметр -ManagementGroupName для применения операций к заданной группе управления.</span><span class="sxs-lookup"><span data-stu-id="76bf9-660">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="76bf9-661">Добавлен параметр -SubscriptionId для применения операций к заданной подписке.</span><span class="sxs-lookup"><span data-stu-id="76bf9-661">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="76bf9-662">Добавлена поддержка ссылок на секрет KeyVault в параметрах при использовании TemplateParameterObject в New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="76bf9-662">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="76bf9-663">Устранена проблема, из-за которой параметр -EndDate игнорировался в New-AzureRmADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="76bf9-663">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="76bf9-664">Устранена проблема, из-за которой в Add-AzureRmADGroupMember использовался неверный URL-адрес для запроса.</span><span class="sxs-lookup"><span data-stu-id="76bf9-664">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="76bf9-665">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="76bf9-665">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="76bf9-666">Для командлета New-AzureRmServiceBusKey добавлен необязательный параметр -KeyValue, который позволяет пользователю предоставить значение ключа.</span><span class="sxs-lookup"><span data-stu-id="76bf9-666">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="76bf9-667">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="76bf9-667">AzureRM.Sql</span></span>
* <span data-ttu-id="76bf9-668">В справке по New-AzureRmSqlDatabaseRestorePoint добавлено описание определяемых пользователем точек восстановления для хранилища данных SQL.</span><span class="sxs-lookup"><span data-stu-id="76bf9-668">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="76bf9-669">Обновлена документация по параметру -ComputeGeneration, используемого в нескольких командлетах.</span><span class="sxs-lookup"><span data-stu-id="76bf9-669">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="76bf9-670">6.3.0 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="76bf9-670">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="76bf9-671">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="76bf9-671">AzureRM.Profile</span></span>
* <span data-ttu-id="76bf9-672">Обновлены сообщения об ошибках для Enable-AzureRmContextAutoSave.</span><span class="sxs-lookup"><span data-stu-id="76bf9-672">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="76bf9-673">Создание контекста для каждой подписки при выполнении Connect-AzureRmAccount без предыдущего контекста.</span><span class="sxs-lookup"><span data-stu-id="76bf9-673">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="76bf9-674">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="76bf9-674">Azure.Storage</span></span>
* <span data-ttu-id="76bf9-675">В файлы справки добавлены дополнительные сведения о параметре -Permissions.</span><span class="sxs-lookup"><span data-stu-id="76bf9-675">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="76bf9-676">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="76bf9-676">AzureRM.Compute</span></span>
* <span data-ttu-id="76bf9-677">Get-AzureRmVmDiskEncryptionStatus устраняет проблему, которая наблюдалась на виртуальных машинах без дисков данных.</span><span class="sxs-lookup"><span data-stu-id="76bf9-677">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="76bf9-678">Обновлена версия клиентской библиотеки Compute для исправления следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="76bf9-678">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="76bf9-679">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="76bf9-679">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="76bf9-680">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="76bf9-680">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="76bf9-681">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="76bf9-681">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="76bf9-682">В следующих командлетах исправлено отображение неправильных значений operation ID и operation status:</span><span class="sxs-lookup"><span data-stu-id="76bf9-682">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="76bf9-683">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="76bf9-683">Start-AzureRmVM</span></span>
    - <span data-ttu-id="76bf9-684">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="76bf9-684">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="76bf9-685">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="76bf9-685">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="76bf9-686">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="76bf9-686">Set-AzureRmVM</span></span>
    - <span data-ttu-id="76bf9-687">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="76bf9-687">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="76bf9-688">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="76bf9-688">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="76bf9-689">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="76bf9-689">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="76bf9-690">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="76bf9-690">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="76bf9-691">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="76bf9-691">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="76bf9-692">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="76bf9-692">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="76bf9-693">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="76bf9-693">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="76bf9-694">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="76bf9-694">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="76bf9-695">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="76bf9-695">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="76bf9-696">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="76bf9-696">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="76bf9-697">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="76bf9-697">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="76bf9-698">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="76bf9-698">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="76bf9-699">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="76bf9-699">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="76bf9-700">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="76bf9-700">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="76bf9-701">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="76bf9-701">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="76bf9-702">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="76bf9-702">AzureRM.EventGrid</span></span>
* <span data-ttu-id="76bf9-703">Удалены условия проверки ValidateNotNullOrEmpty для SubjectBeginsWith/SubjectEndsWith в командлете Update-AzureRmEventGridSubscription, что позволяет при необходимости заменять эти параметры пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="76bf9-703">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="76bf9-704">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="76bf9-704">AzureRM.KeyVault</span></span>
* <span data-ttu-id="76bf9-705">Исправлена ошибка, когда при выполнении командлета Get-AzureRmKeyVault -Tag не возвращается ни один тег.</span><span class="sxs-lookup"><span data-stu-id="76bf9-705">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="76bf9-706">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="76bf9-706">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="76bf9-707">Общедоступный выпуск командлетов Policy Insights.</span><span class="sxs-lookup"><span data-stu-id="76bf9-707">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="76bf9-708">Используется API версии 2018-04-04.</span><span class="sxs-lookup"><span data-stu-id="76bf9-708">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="76bf9-709">К результатам Get-AzureRmPolicyStateSummary добавлено PolicyDefinitionReferenceId.</span><span class="sxs-lookup"><span data-stu-id="76bf9-709">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="76bf9-710">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="76bf9-710">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="76bf9-711">Для командлетов RecoveryServices.Backup добавлен параметр -Vault.</span><span class="sxs-lookup"><span data-stu-id="76bf9-711">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="76bf9-712">Передача этого параметра переопределяет командлет Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="76bf9-712">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="76bf9-713">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="76bf9-713">AzureRM.Sql</span></span>
* <span data-ttu-id="76bf9-714">В файле справки обновлен пример для командлета Get-AzureRmSqlDatabaseExpanded.</span><span class="sxs-lookup"><span data-stu-id="76bf9-714">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="76bf9-715">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="76bf9-715">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="76bf9-716">Обновлен файл справки для командлета Add-AzureRmTrafficManagerEndpointConfig.</span><span class="sxs-lookup"><span data-stu-id="76bf9-716">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="76bf9-717">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="76bf9-717">AzureRM.Websites</span></span>
* <span data-ttu-id="76bf9-718">Изменено действие командлета Set-AzureRmWebApp. Теперь он не перезаписывает AppSettings, если используется параметр -AssignIdentity.</span><span class="sxs-lookup"><span data-stu-id="76bf9-718">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="76bf9-719">Командлет New-AzureRmWebAppSlot теперь учитывает дополнительный параметр AppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="76bf9-719">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="76bf9-720">6.2.1 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="76bf9-720">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="76bf9-721">AzureRM.OperationalInsights;</span><span class="sxs-lookup"><span data-stu-id="76bf9-721">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="76bf9-722">В обновленной модели PSWorkspace Network может использовать type в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="76bf9-722">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="76bf9-723">6.2.0 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="76bf9-723">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="76bf9-724">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="76bf9-724">AzureRM.Profile</span></span>
* <span data-ttu-id="76bf9-725">Исправлена ошибка с загрузкой Newtonsoft.Json версии 10.0.3 во время импорта модуля.</span><span class="sxs-lookup"><span data-stu-id="76bf9-725">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="76bf9-726">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="76bf9-726">AzureRM.Compute</span></span>
* <span data-ttu-id="76bf9-727">Функция обновления виртуальных машин VMSS.</span><span class="sxs-lookup"><span data-stu-id="76bf9-727">VMSS VM Update feature</span></span>
    - <span data-ttu-id="76bf9-728">Добавлены командлеты Update-AzureRmVmssVM и New-AzureRmVMDataDisk.</span><span class="sxs-lookup"><span data-stu-id="76bf9-728">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="76bf9-729">В командлет Add-AzureRmVMDataDisk добавлен параметр VirtualMachineScaleSetVM, который позволяет добавлять диски данных в виртуальные машины VMSS.</span><span class="sxs-lookup"><span data-stu-id="76bf9-729">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="76bf9-730">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="76bf9-730">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="76bf9-731">Пакет SDK для ADF .NET обновлен до версии 0.8.0-preview. Новая версия содержит такие изменения:</span><span class="sxs-lookup"><span data-stu-id="76bf9-731">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="76bf9-732">добавлена операция для настройки репозитория фабрики;</span><span class="sxs-lookup"><span data-stu-id="76bf9-732">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="76bf9-733">связанная служба QuickBooks LinkedService теперь предоставляет свойства consumerKey и consumerSecret;</span><span class="sxs-lookup"><span data-stu-id="76bf9-733">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="76bf9-734">тип нескольких моделей изменен с SecretBase на Object;</span><span class="sxs-lookup"><span data-stu-id="76bf9-734">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="76bf9-735">добавлен триггер событий BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="76bf9-735">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="76bf9-736">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="76bf9-736">AzureRM.KeyVault</span></span>
* <span data-ttu-id="76bf9-737">В документацию добавлены примеры выходных данных.</span><span class="sxs-lookup"><span data-stu-id="76bf9-737">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="76bf9-738">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="76bf9-738">AzureRM.Network</span></span>
* <span data-ttu-id="76bf9-739">В командлеты Наблюдателя за сетями добавлены параметры Аналитики трафика.</span><span class="sxs-lookup"><span data-stu-id="76bf9-739">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="76bf9-740">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="76bf9-740">AzureRM.Resources</span></span>
* <span data-ttu-id="76bf9-741">Исправлена ошибка, когда командлет Get-AzureRmResource возвращает свойство Properties объектов PSResource.</span><span class="sxs-lookup"><span data-stu-id="76bf9-741">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="76bf9-742">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="76bf9-742">AzureRM.Scheduler</span></span>
* <span data-ttu-id="76bf9-743">Исправлена ошибка, когда обновление ServiceBusQueueJob не задает новые значения для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="76bf9-743">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="76bf9-744">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="76bf9-744">AzureRM.Sql</span></span>
* <span data-ttu-id="76bf9-745">В перечисленные ниже командлеты добавлен необязательный параметр LicenseType.</span><span class="sxs-lookup"><span data-stu-id="76bf9-745">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="76bf9-746">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="76bf9-746">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="76bf9-747">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool;</span><span class="sxs-lookup"><span data-stu-id="76bf9-747">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="76bf9-748">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="76bf9-748">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="76bf9-749">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="76bf9-749">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="76bf9-750">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="76bf9-750">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="76bf9-751">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="76bf9-751">AzureRM.Websites</span></span>
* <span data-ttu-id="76bf9-752">Командлет New-AzureRMWebApp теперь использует общие алгоритмы из библиотеки Strategy.</span><span class="sxs-lookup"><span data-stu-id="76bf9-752">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="76bf9-753">6.1.0 — май 2018 г.</span><span class="sxs-lookup"><span data-stu-id="76bf9-753">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="76bf9-754">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="76bf9-754">AzureRM.Profile</span></span>
* <span data-ttu-id="76bf9-755">Устранена проблема с выполнением Clear-AzureRmContext, при которой сохранялся пустой контекст с именем предыдущего контекста по умолчанию, что не позволяло пользователю создать новый контекст со старым именем.</span><span class="sxs-lookup"><span data-stu-id="76bf9-755">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="76bf9-756">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="76bf9-756">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="76bf9-757">Включены операции связывания и отмены связи в автономной системе.</span><span class="sxs-lookup"><span data-stu-id="76bf9-757">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="76bf9-758">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="76bf9-758">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="76bf9-759">Добавлена поддержка ApiVersions, ApiReleases и ApiRevisions.</span><span class="sxs-lookup"><span data-stu-id="76bf9-759">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="76bf9-760">Добавлена поддержка серверной части ServiceFabric.</span><span class="sxs-lookup"><span data-stu-id="76bf9-760">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="76bf9-761">Добавлена поддержка средства ведения журнала Application Insights.</span><span class="sxs-lookup"><span data-stu-id="76bf9-761">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="76bf9-762">Добавлена поддержка для распознавания номера SKU уровня "Базовый" как допустимого номера SKU службы управления API.</span><span class="sxs-lookup"><span data-stu-id="76bf9-762">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="76bf9-763">Добавлена поддержка установки сертификатов, выданных частным центром сертификации в качестве корневого или обычного ЦС.</span><span class="sxs-lookup"><span data-stu-id="76bf9-763">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="76bf9-764">Добавлена поддержка для приема пользовательских SSL-сертификатов с помощью KeyVault и нескольких имен узлов прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="76bf9-764">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="76bf9-765">Добавлена поддержка для удостоверения MSI.</span><span class="sxs-lookup"><span data-stu-id="76bf9-765">Added support for MSI identity</span></span>
* <span data-ttu-id="76bf9-766">Добавлена поддержка для принятия политик с помощью URL-адреса. Примечание. Указанные ниже командлеты в следующей версии будут отмечены как нерекомендуемые.</span><span class="sxs-lookup"><span data-stu-id="76bf9-766">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="76bf9-767">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="76bf9-767">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="76bf9-768">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="76bf9-768">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="76bf9-769">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="76bf9-769">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="76bf9-770">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="76bf9-770">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="76bf9-771">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="76bf9-771">AzureRM.Batch</span></span>
* <span data-ttu-id="76bf9-772">Выпущен новый командлет Get-AzureBatchPoolNodeCounts.</span><span class="sxs-lookup"><span data-stu-id="76bf9-772">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="76bf9-773">Выпущен новый командлет Start-AzureBatchComputeNodeServiceLogUpload.</span><span class="sxs-lookup"><span data-stu-id="76bf9-773">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="76bf9-774">AzureRM.Consumption:</span><span class="sxs-lookup"><span data-stu-id="76bf9-774">AzureRM.Consumption</span></span>
* <span data-ttu-id="76bf9-775">Добавлены новые параметры Expand, ResourceGroup, InstanceName, InstanceId, Tags и командлет высшего уровня Get-AzureRmConsumptionUsageDetail.</span><span class="sxs-lookup"><span data-stu-id="76bf9-775">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="76bf9-776">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="76bf9-776">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="76bf9-777">Исправлен пример для Export-AzureRmDataLakeStoreChildItemProperties.</span><span class="sxs-lookup"><span data-stu-id="76bf9-777">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="76bf9-778">Исправлено исключение параметра NULL при использовании рекурсии в Set-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="76bf9-778">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="76bf9-779">Исправлены файлы справки для Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl и Remove-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="76bf9-779">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="76bf9-780">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="76bf9-780">AzureRM.Network</span></span>
* <span data-ttu-id="76bf9-781">Пакет SDK для сети обновлен с предварительной версии 18.0.0 до предварительной версии 19.0.0.</span><span class="sxs-lookup"><span data-stu-id="76bf9-781">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="76bf9-782">Добавлен командлет для создания конфигурации протокола.</span><span class="sxs-lookup"><span data-stu-id="76bf9-782">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="76bf9-783">New-AzureRmNetworkWatcherProtocolConfiguration.</span><span class="sxs-lookup"><span data-stu-id="76bf9-783">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="76bf9-784">Добавлен командлет для добавления нового подключения канала к существующему каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="76bf9-784">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="76bf9-785">Add-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="76bf9-785">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="76bf9-786">Добавлен командлет для удаления подключения канала к существующему каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="76bf9-786">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="76bf9-787">Remove-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="76bf9-787">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="76bf9-788">Добавлен командлет для получения подключения канала.</span><span class="sxs-lookup"><span data-stu-id="76bf9-788">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="76bf9-789">Get-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="76bf9-789">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="76bf9-790">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="76bf9-790">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="76bf9-791">Исправлена процедура аутентификации сервера с использованием созданных сертификатов (проблема № 5998).</span><span class="sxs-lookup"><span data-stu-id="76bf9-791">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="76bf9-792">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="76bf9-792">AzureRM.Sql</span></span>
* <span data-ttu-id="76bf9-793">Обновлены командлеты аудита, которые теперь позволяют удалять AuditActions или AuditActionGroups.</span><span class="sxs-lookup"><span data-stu-id="76bf9-793">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="76bf9-794">Исправлена проблема с Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy, при которой установка новой гибкой политики хранения завершалась ошибкой с сообщением "Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span><span class="sxs-lookup"><span data-stu-id="76bf9-794">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="76bf9-795">Please submit request with the new flexible retention policy" (Настройка политики долгосрочного хранения с помощью хранилища и политики служб восстановления Azure больше не поддерживается. Отправьте запрос с использованием новой гибкой политики хранения).</span><span class="sxs-lookup"><span data-stu-id="76bf9-795">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="76bf9-796">Обновлены все командлеты, связанные со службой "База данных SQL Azure", с созданием эластичных пулов и обновлением. Теперь используются новые API баз данных с поддержкой свойства номеров SKU для обеспечения масштабируемости и связанных с уровнями возможностей.</span><span class="sxs-lookup"><span data-stu-id="76bf9-796">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="76bf9-797">Обновлены командлеты, в том числе:</span><span class="sxs-lookup"><span data-stu-id="76bf9-797">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="76bf9-798">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="76bf9-798">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="76bf9-799">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool;</span><span class="sxs-lookup"><span data-stu-id="76bf9-799">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="76bf9-800">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="76bf9-800">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="76bf9-801">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="76bf9-801">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="76bf9-802">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="76bf9-802">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="76bf9-803">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="76bf9-803">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="76bf9-804">Обновлены параметры для Get-AzureRmTrafficManagerProfile. Теперь при использовании параметра -Name требуется параметр -ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="76bf9-804">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
