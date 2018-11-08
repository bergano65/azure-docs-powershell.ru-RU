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
ms.openlocfilehash: eec8b5960f787fa9ca1130b4f8b49c9d896aa99e
ms.sourcegitcommit: 1f699b72bf544d92459da9d888cc0091f9415b65
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "50971981"
---
# <a name="release-notes"></a><span data-ttu-id="ab659-103">Заметки о выпуске</span><span class="sxs-lookup"><span data-stu-id="ab659-103">Release notes</span></span>

<span data-ttu-id="ab659-104">Здесь приведен список изменений, внесенных в Azure PowerShell в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="ab659-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6110---october-2018"></a><span data-ttu-id="ab659-105">6.11.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="ab659-105">6.11.0 - October 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ab659-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ab659-106">AzureRM.Profile</span></span>
* <span data-ttu-id="ab659-107">Устранена проблема с Get-AzureRmSubscription в CloudShell.</span><span class="sxs-lookup"><span data-stu-id="ab659-107">Fix issue with Get-AzureRmSubscription in CloudShell</span></span>
* <span data-ttu-id="ab659-108">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-108">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="ab659-109">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="ab659-109">AzureRM.Backup</span></span>
* <span data-ttu-id="ab659-110">Командлеты Azure Backup объявлены нерекомендуемыми.</span><span class="sxs-lookup"><span data-stu-id="ab659-110">Deprecated Azure Backup cmdlets.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ab659-111">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ab659-111">AzureRM.Compute</span></span>
* <span data-ttu-id="ab659-112">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzureRmVm.</span><span class="sxs-lookup"><span data-stu-id="ab659-112">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzureRmVm'</span></span>
* <span data-ttu-id="ab659-113">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="ab659-113">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="ab659-114">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ab659-114">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="ab659-115">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="ab659-115">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="ab659-116">Get-AzureRmDataLakeStoreVirtualNetworkRule — позволяет получить или вывести правило виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ab659-116">Get-AzureRmDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="ab659-117">Add-AzureRmDataLakeStoreVirtualNetworkRule — позволяет добавить правило виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ab659-117">Add-AzureRmDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="ab659-118">Set-AzureRmDataLakeStoreVirtualNetworkRule — позволяет изменить определенное правило виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ab659-118">Set-AzureRmDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="ab659-119">Remove-AzureRmDataLakeStoreVirtualNetworkRule — позволяет удалить правило виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ab659-119">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ab659-120">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ab659-120">AzureRM.Network</span></span>
* <span data-ttu-id="ab659-121">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="ab659-121">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="ab659-122">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="ab659-122">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ab659-123">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ab659-123">AzureRM.Resources</span></span>
* <span data-ttu-id="ab659-124">Мы устранили проблему, из-за которой командлет Get-AzureRMRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), и добавили понятное исключение.</span><span class="sxs-lookup"><span data-stu-id="ab659-124">Fix isssue where Get-AzureRMRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="ab659-125">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="ab659-125">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="6100---october-2018"></a><span data-ttu-id="ab659-126">6.10.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="ab659-126">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="ab659-127">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="ab659-127">Azure.Storage</span></span>
* <span data-ttu-id="ab659-128">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="ab659-128">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="ab659-129">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="ab659-129">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="ab659-130">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="ab659-130">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="ab659-131">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ab659-131">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="ab659-132">Поддержка Get-AzureRmCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="ab659-132">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ab659-133">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ab659-133">AzureRM.Compute</span></span>
* <span data-ttu-id="ab659-134">Исправлена команда Get-AzureRmVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов.</span><span class="sxs-lookup"><span data-stu-id="ab659-134">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="ab659-135">Добавлен пример использования SimpleParameterSet в справку командлета New-AzureRmVmss.</span><span class="sxs-lookup"><span data-stu-id="ab659-135">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="ab659-136">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="ab659-136">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="ab659-137">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ab659-137">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="ab659-138">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="ab659-138">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ab659-139">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ab659-139">AzureRM.Network</span></span>
* <span data-ttu-id="ab659-140">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="ab659-140">Added NetworkProfile functionality.</span></span> <span data-ttu-id="ab659-141">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="ab659-141">new cmdlets added</span></span>
    - <span data-ttu-id="ab659-142">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ab659-142">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="ab659-143">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ab659-143">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="ab659-144">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ab659-144">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="ab659-145">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ab659-145">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="ab659-146">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="ab659-146">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="ab659-147">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="ab659-147">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="ab659-148">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="ab659-148">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="ab659-149">Добавлены командлеты: New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap.</span><span class="sxs-lookup"><span data-stu-id="ab659-149">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="ab659-150">Добавлены командлеты: Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="ab659-150">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="ab659-151">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ab659-151">AzureRM.RedisCache</span></span>
* <span data-ttu-id="ab659-152">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="ab659-152">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="ab659-153">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="ab659-153">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ab659-154">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ab659-154">AzureRM.Resources</span></span>
* <span data-ttu-id="ab659-155">Добавлен отсутствующий параметр -Mode в командлет Set-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="ab659-155">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="ab659-156">Исправлена ошибка командлета Get-AzureRmProviderOperation для операций, когда Origin содержит User.</span><span class="sxs-lookup"><span data-stu-id="ab659-156">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ab659-157">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ab659-157">AzureRM.Sql</span></span>
* <span data-ttu-id="ab659-158">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="ab659-158">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="ab659-159">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="ab659-159">AzureRM.Storage</span></span>
* <span data-ttu-id="ab659-160">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="ab659-160">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="ab659-161">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="ab659-161">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ab659-162">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ab659-162">AzureRM.Websites</span></span>
* <span data-ttu-id="ab659-163">Новый командлет Get-AzureRMWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера.</span><span class="sxs-lookup"><span data-stu-id="ab659-163">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="ab659-164">Новые командлеты New-AzureRMWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows.</span><span class="sxs-lookup"><span data-stu-id="ab659-164">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="ab659-165">6.9.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="ab659-165">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ab659-166">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="ab659-166">General</span></span>
* <span data-ttu-id="ab659-167">В модуль развертывания AzureRM добавлен командлет AzureRM.SignalR.</span><span class="sxs-lookup"><span data-stu-id="ab659-167">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="ab659-168">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ab659-168">AzureRM.Profile</span></span>
* <span data-ttu-id="ab659-169">Незначительные изменения в общем коде хранилища.</span><span class="sxs-lookup"><span data-stu-id="ab659-169">Minor changes to the storage common code</span></span>
* <span data-ttu-id="ab659-170">Обновлены файлы справки, в которые добавлены полные типы параметров.</span><span class="sxs-lookup"><span data-stu-id="ab659-170">Updated help files to include full parameter types.</span></span>
- <span data-ttu-id="ab659-171">В наборе параметров ServicePrincipalCertificateWithSubscriptionId параметр -ServicePrincipal теперь стал необязательным.</span><span class="sxs-lookup"><span data-stu-id="ab659-171">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="ab659-172">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="ab659-172">Azure.Storage</span></span>
* <span data-ttu-id="ab659-173">Поддержка создания контекста хранилища с использованием OAuth.</span><span class="sxs-lookup"><span data-stu-id="ab659-173">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="ab659-174">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="ab659-174">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="ab659-175">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="ab659-175">AzureRM.Cdn</span></span>
* <span data-ttu-id="ab659-176">Добавлен номер SKU для расценок на Standard_Microsoft в CDN.</span><span class="sxs-lookup"><span data-stu-id="ab659-176">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="ab659-177">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ab659-177">AzureRM.Compute</span></span>
* <span data-ttu-id="ab659-178">Keyvault и Storage перенесены в общие зависимости.</span><span class="sxs-lookup"><span data-stu-id="ab659-178">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="ab659-179">Добавлена поддержка большего количества размеров виртуальных машин в командлеты AEM.</span><span class="sxs-lookup"><span data-stu-id="ab659-179">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="ab659-180">Добавлен параметр PublicIPPrefix в командлет New-AzureRmVmssIpConfig.</span><span class="sxs-lookup"><span data-stu-id="ab659-180">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="ab659-181">Добавлен параметр ResourceId в командлет Invoke-AzureRmVMRunCommand.</span><span class="sxs-lookup"><span data-stu-id="ab659-181">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="ab659-182">Добавлен командлет Invoke-AzureRmVmssVMRunCommand.</span><span class="sxs-lookup"><span data-stu-id="ab659-182">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="ab659-183">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="ab659-183">AzureRM.Dns</span></span>
* <span data-ttu-id="ab659-184">Добавлена поддержка для псевдонима записи во время создания записи DNS.</span><span class="sxs-lookup"><span data-stu-id="ab659-184">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="ab659-185">AzureRM.Insights;</span><span class="sxs-lookup"><span data-stu-id="ab659-185">AzureRM.Insights</span></span>
* <span data-ttu-id="ab659-186">Исправлены проблемы № 6833 и № 7102 (область настроек диагностики).</span><span class="sxs-lookup"><span data-stu-id="ab659-186">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="ab659-187">Проблемы с именем по умолчанию, например service, во время создания, получения и отображения списка параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="ab659-187">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="ab659-188">Проблемы при создании параметров диагностики с категориями.</span><span class="sxs-lookup"><span data-stu-id="ab659-188">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="ab659-189">Добавлено сообщение о том, что не рекомендуется использовать параметры интервалов времени в метриках.</span><span class="sxs-lookup"><span data-stu-id="ab659-189">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="ab659-190">Параметры интервалов времени по-прежнему принимаются (это не критическое изменение), но они игнорируются в серверной части, потому что действительно только значение PT1M.</span><span class="sxs-lookup"><span data-stu-id="ab659-190">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ab659-191">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ab659-191">AzureRM.Network</span></span>
* <span data-ttu-id="ab659-192">Изменения командлетов LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ab659-192">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="ab659-193">LoadBalancerInboundNatPoolConfig: добавлены параметры IdleTimeoutInMinutes, EnableFloatingIp и EnableTcpReset.</span><span class="sxs-lookup"><span data-stu-id="ab659-193">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="ab659-194">LoadBalancerInboundNatRuleConfig: добавлен параметр EnableTcpReset.</span><span class="sxs-lookup"><span data-stu-id="ab659-194">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="ab659-195">LoadBalancerRuleConfig: добавлен параметр EnableTcpReset.</span><span class="sxs-lookup"><span data-stu-id="ab659-195">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="ab659-196">LoadBalancerProbeConfig: добавлена поддержка значения Https для параметра Protocol.</span><span class="sxs-lookup"><span data-stu-id="ab659-196">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="ab659-197">Добавлены новые команды для нового правила OutboundRule подресурса LoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="ab659-197">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="ab659-198">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ab659-198">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="ab659-199">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ab659-199">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="ab659-200">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ab659-200">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="ab659-201">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ab659-201">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="ab659-202">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ab659-202">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="ab659-203">Добавлено новое свойство HostedWorkloads для PSNetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="ab659-203">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="ab659-204">Добавлены новые командлеты для функции Брандмауэра Azure через ARM.</span><span class="sxs-lookup"><span data-stu-id="ab659-204">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="ab659-205">Добавлен командлет Get-AzureRmFirewall.</span><span class="sxs-lookup"><span data-stu-id="ab659-205">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="ab659-206">Добавлен командлет Set-AzureRmFirewall.</span><span class="sxs-lookup"><span data-stu-id="ab659-206">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="ab659-207">Добавлен командлет New-AzureRmFirewall.</span><span class="sxs-lookup"><span data-stu-id="ab659-207">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="ab659-208">Добавлен командлет Remove-AzureRmFirewall.</span><span class="sxs-lookup"><span data-stu-id="ab659-208">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="ab659-209">Добавлен командлет New-AzureRmFirewallApplicationRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="ab659-209">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="ab659-210">Добавлен командлет New-AzureRmFirewallApplicationRule.</span><span class="sxs-lookup"><span data-stu-id="ab659-210">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="ab659-211">Добавлен командлет New-AzureRmFirewallNatRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="ab659-211">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="ab659-212">Добавлен командлет New-AzureRmFirewallNatRule.</span><span class="sxs-lookup"><span data-stu-id="ab659-212">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="ab659-213">Добавлен командлет New-AzureRmFirewallNetworkRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="ab659-213">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="ab659-214">Добавлен командлет New-AzureRmFirewallNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="ab659-214">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="ab659-215">Добавлена поддержка конфигурации для доверенного корневого сертификата и автомасштабирования в Шлюзе приложений.</span><span class="sxs-lookup"><span data-stu-id="ab659-215">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="ab659-216">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="ab659-216">New Cmdlets added:</span></span>
      - <span data-ttu-id="ab659-217">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ab659-217">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="ab659-218">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ab659-218">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="ab659-219">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ab659-219">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="ab659-220">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ab659-220">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="ab659-221">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ab659-221">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="ab659-222">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ab659-222">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="ab659-223">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ab659-223">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="ab659-224">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ab659-224">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="ab659-225">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ab659-225">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="ab659-226">В следующие командлеты добавлен необязательный параметр -TrustedRootCertificate:</span><span class="sxs-lookup"><span data-stu-id="ab659-226">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="ab659-227">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ab659-227">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="ab659-228">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ab659-228">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="ab659-229">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="ab659-229">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="ab659-230">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="ab659-230">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="ab659-231">В следующие командлеты добавлен необязательный параметр -AutoscaleConfiguration:</span><span class="sxs-lookup"><span data-stu-id="ab659-231">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="ab659-232">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ab659-232">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="ab659-233">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ab659-233">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="ab659-234">Добавлен командлет для конечной точки интерфейса Get-AzureInterfaceEndpoint.</span><span class="sxs-lookup"><span data-stu-id="ab659-234">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="ab659-235">Добавлена поддержка нескольких префиксов адресов в подсети.</span><span class="sxs-lookup"><span data-stu-id="ab659-235">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="ab659-236">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="ab659-236">Updated cmdlets:</span></span>
  - <span data-ttu-id="ab659-237">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ab659-237">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="ab659-238">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ab659-238">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="ab659-239">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ab659-239">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="ab659-240">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ab659-240">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="ab659-241">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ab659-241">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="ab659-242">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ab659-242">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="ab659-243">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ab659-243">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="ab659-244">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ab659-244">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="ab659-245">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ab659-245">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="ab659-246">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ab659-246">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="ab659-247">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ab659-247">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="ab659-248">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ab659-248">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="ab659-249">New-AzureRmNetworkInterfaceIpConfig — Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ab659-249">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="ab659-250">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="ab659-250">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="ab659-251">Add-AzureRmVirtualNetworkGatewayIpConfig;</span><span class="sxs-lookup"><span data-stu-id="ab659-251">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="ab659-252">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ab659-252">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="ab659-253">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ab659-253">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="ab659-254">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ab659-254">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="ab659-255">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ab659-255">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="ab659-256">Добавлены командлеты для делегирования подсети.</span><span class="sxs-lookup"><span data-stu-id="ab659-256">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="ab659-257">New-AzureRmDelegation — создает делегирование, которое можно добавить к подсети.</span><span class="sxs-lookup"><span data-stu-id="ab659-257">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="ab659-258">Remove-AzureRmDelegation — принимает подсеть и удаляет указанное имя делегирования из этой подсети.</span><span class="sxs-lookup"><span data-stu-id="ab659-258">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="ab659-259">Add-AzureRmDelegation — принимает подсеть и добавляет указанное имя службы в качестве делегирования для этой подсети.</span><span class="sxs-lookup"><span data-stu-id="ab659-259">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="ab659-260">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="ab659-260">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="ab659-261">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="ab659-261">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="ab659-262">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="ab659-262">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="ab659-263">Добавлена поддержка управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="ab659-263">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="ab659-264">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ab659-264">AzureRM.RedisCache</span></span>
* <span data-ttu-id="ab659-265">Обновлена зависимость Insights.</span><span class="sxs-lookup"><span data-stu-id="ab659-265">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ab659-266">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ab659-266">AzureRM.Resources</span></span>
* <span data-ttu-id="ab659-267">В командлет New-AzureRmResourceGroupDeployment добавлен новый параметр RollbackAction.</span><span class="sxs-lookup"><span data-stu-id="ab659-267">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="ab659-268">Добавлена поддержка OnErrorDeployment с новым параметром.</span><span class="sxs-lookup"><span data-stu-id="ab659-268">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="ab659-269">Добавлена поддержка управляемого удостоверения при назначении политик.</span><span class="sxs-lookup"><span data-stu-id="ab659-269">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="ab659-270">При назначении политики с помощью New-AzureRmPolicyAssignment параметры со значениями по умолчанию больше не требуются.</span><span class="sxs-lookup"><span data-stu-id="ab659-270">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="ab659-271">Добавлен новый командлет Get-AzureRmPolicyAlias для получения псевдонимов политик.</span><span class="sxs-lookup"><span data-stu-id="ab659-271">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ab659-272">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ab659-272">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ab659-273">Устранена проблема № 7161.</span><span class="sxs-lookup"><span data-stu-id="ab659-273">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="ab659-274">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="ab659-274">AzureRM.SignalR</span></span>
* <span data-ttu-id="ab659-275">Обновлены номера SKU для Free_F1 и Standard_S1.</span><span class="sxs-lookup"><span data-stu-id="ab659-275">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="ab659-276">Добавлены поле версии в объект PSSignalRResource и строка подключения в объект PSSignalRKeys.</span><span class="sxs-lookup"><span data-stu-id="ab659-276">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="ab659-277">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="ab659-277">AzureRM.Storage</span></span>
* <span data-ttu-id="ab659-278">Добавлена поддержка политики неизменяемости в AzureRm.Storage.</span><span class="sxs-lookup"><span data-stu-id="ab659-278">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="ab659-279">Remove-AzureRmStorageAccountNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="ab659-279">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="ab659-280">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ab659-280">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="ab659-281">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ab659-281">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="ab659-282">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ab659-282">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="ab659-283">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ab659-283">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="ab659-284">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="ab659-284">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="ab659-285">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="ab659-285">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="ab659-286">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ab659-286">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="ab659-287">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ab659-287">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="ab659-288">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ab659-288">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="ab659-289">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ab659-289">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ab659-290">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ab659-290">AzureRM.Websites</span></span>
* <span data-ttu-id="ab659-291">Добавлены два новых командлета: Get-AzureRmDeletedWebApp и Restore-AzureRmDeletedWebApp.</span><span class="sxs-lookup"><span data-stu-id="ab659-291">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="ab659-292">New-AzureRmAppServicePlan: добавлен параметр -HyperV для создания плана службы приложений с контейнером Windows.</span><span class="sxs-lookup"><span data-stu-id="ab659-292">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="ab659-293">New-AzureRmWebApp, New-AzureRmWebAppSlot, Set-AzureRmWebApp, Set-AzureRmWebAppSlot: добавлены новые параметры (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) для создания контейнера приложения Windows и управления им.</span><span class="sxs-lookup"><span data-stu-id="ab659-293">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="ab659-294">6.8.1 — август 2018 г.</span><span class="sxs-lookup"><span data-stu-id="ab659-294">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ab659-295">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="ab659-295">General</span></span>
* <span data-ttu-id="ab659-296">Исправлена проблема с отсутствием настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ab659-296">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="ab659-297">Обновлены общие сборки среды выполнения</span><span class="sxs-lookup"><span data-stu-id="ab659-297">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="ab659-298">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ab659-298">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="ab659-299">Исправлена проблема с отсутствием настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ab659-299">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="ab659-300">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6603.</span><span class="sxs-lookup"><span data-stu-id="ab659-300">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="ab659-301">Командлеты Import-AzureRmApiManagementApi и \*-AzureRmApiManagementCertificate теперь обрабатывают относительные пути.</span><span class="sxs-lookup"><span data-stu-id="ab659-301">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="ab659-302">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6879.</span><span class="sxs-lookup"><span data-stu-id="ab659-302">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="ab659-303">CertificateInformation — это задаваемое свойство, обеспечивающее правильную работу командлета Set-AzureRmApiManagement.</span><span class="sxs-lookup"><span data-stu-id="ab659-303">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="ab659-304">Проблема исправлена путем обновления пакета NuGet до версии 4.0.4-preview.</span><span class="sxs-lookup"><span data-stu-id="ab659-304">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="ab659-305">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6853.</span><span class="sxs-lookup"><span data-stu-id="ab659-305">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="ab659-306">Исправлен фильтр OData для поиска по имени продукта.</span><span class="sxs-lookup"><span data-stu-id="ab659-306">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="ab659-307">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6814.</span><span class="sxs-lookup"><span data-stu-id="ab659-307">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="ab659-308">Исправлен фильтр OData для поиска по имени API.</span><span class="sxs-lookup"><span data-stu-id="ab659-308">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="ab659-309">Добавлена поддержка средства ведения журнала Azure Monitor.</span><span class="sxs-lookup"><span data-stu-id="ab659-309">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="ab659-310">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ab659-310">AzureRM.Compute</span></span>
* <span data-ttu-id="ab659-311">Исправлена проблема с отсутствием в выходных данных ошибки целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="ab659-311">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="ab659-312">Исправлена проблема с типом учетной записи хранения для виртуальной машины с управляемым диском.</span><span class="sxs-lookup"><span data-stu-id="ab659-312">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="ab659-313">Исправлена проблема с отсутствием настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ab659-313">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="ab659-314">Исправлены командлеты расширения AEM для других сред, например Azure для Китая.</span><span class="sxs-lookup"><span data-stu-id="ab659-314">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ab659-315">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ab659-315">AzureRM.Network</span></span>
* <span data-ttu-id="ab659-316">Стандартное представление выходных данных командлетов изменено на представление таблиц.</span><span class="sxs-lookup"><span data-stu-id="ab659-316">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="ab659-317">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="ab659-317">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="ab659-318">Исправлена проблема с Update-AzureRmPowerBIEmbeddedCapacity при попытке масштабировать приостановленную емкость.</span><span class="sxs-lookup"><span data-stu-id="ab659-318">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="ab659-319">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ab659-319">AzureRM.Resources</span></span>
* <span data-ttu-id="ab659-320">Исправлена проблема с созданием управляемых приложений из Marketplace.</span><span class="sxs-lookup"><span data-stu-id="ab659-320">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ab659-321">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ab659-321">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ab659-322">Исправленные проблемы</span><span class="sxs-lookup"><span data-stu-id="ab659-322">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="ab659-323">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ab659-323">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="ab659-324">Добавлена поддержка метода маршрутизации MultiValue.</span><span class="sxs-lookup"><span data-stu-id="ab659-324">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="ab659-325">Добавлен новый параметр MaxReturn для маршрутизации MultiValue.</span><span class="sxs-lookup"><span data-stu-id="ab659-325">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="ab659-326">Добавлена поддержка метода маршрутизации Subnet.</span><span class="sxs-lookup"><span data-stu-id="ab659-326">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="ab659-327">Добавлена поддержка диапазонов IP-адресов (подсетей) в конечных точках.</span><span class="sxs-lookup"><span data-stu-id="ab659-327">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="ab659-328">Добавлена поддержка пользовательских заголовков в профилях.</span><span class="sxs-lookup"><span data-stu-id="ab659-328">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="ab659-329">Добавлена поддержка диапазонов кода ожидаемого состояния в профилях.</span><span class="sxs-lookup"><span data-stu-id="ab659-329">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="ab659-330">Добавлена поддержка пользовательских заголовков в конечных точках.</span><span class="sxs-lookup"><span data-stu-id="ab659-330">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="ab659-331">6.8.0 — август 2018 г.</span><span class="sxs-lookup"><span data-stu-id="ab659-331">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ab659-332">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="ab659-332">General</span></span>
* <span data-ttu-id="ab659-333">Исправлена проблема с отсутствием настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ab659-333">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="ab659-334">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ab659-334">AzureRM.Profile</span></span>
* <span data-ttu-id="ab659-335">Добавлено свойство срока действия для маркеров, возвращенных при выполнении Connect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="ab659-335">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ab659-336">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ab659-336">AzureRM.Compute</span></span>
* <span data-ttu-id="ab659-337">Исправлена проблема с отсутствием в выходных данных ошибки целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="ab659-337">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="ab659-338">Исправлена проблема с типом учетной записи хранения для виртуальной машины с управляемым диском.</span><span class="sxs-lookup"><span data-stu-id="ab659-338">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="ab659-339">Исправлены командлеты расширения AEM для других сред, например Azure для Китая.</span><span class="sxs-lookup"><span data-stu-id="ab659-339">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="ab659-340">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="ab659-340">AzureRM.IotHub</span></span>
* <span data-ttu-id="ab659-341">Исправлены примеры для New-AzureRmIotHubExportDevices и New-AzureRmIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="ab659-341">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ab659-342">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ab659-342">AzureRM.Network</span></span>
* <span data-ttu-id="ab659-343">Изменено представление моделей по умолчанию на представление таблиц.</span><span class="sxs-lookup"><span data-stu-id="ab659-343">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="ab659-344">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="ab659-344">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="ab659-345">Исправлена проблема с Update-AzureRmPowerBIEmbeddedCapacity при попытке масштабировать приостановленную емкость.</span><span class="sxs-lookup"><span data-stu-id="ab659-345">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ab659-346">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ab659-346">AzureRM.Resources</span></span>
* <span data-ttu-id="ab659-347">Исправлена проблема с созданием управляемого приложения из marketplace.</span><span class="sxs-lookup"><span data-stu-id="ab659-347">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ab659-348">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ab659-348">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ab659-349">Исправления проблем</span><span class="sxs-lookup"><span data-stu-id="ab659-349">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="ab659-350">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ab659-350">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="ab659-351">Добавлена поддержка метода маршрутизации MultiValue.</span><span class="sxs-lookup"><span data-stu-id="ab659-351">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="ab659-352">Добавлен новый параметр MaxReturn для маршрутизации MultiValue.</span><span class="sxs-lookup"><span data-stu-id="ab659-352">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="ab659-353">Добавлена поддержка метода маршрутизации Subnet.</span><span class="sxs-lookup"><span data-stu-id="ab659-353">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="ab659-354">Добавлена поддержка диапазонов IP-адресов (подсетей) в конечных точках.</span><span class="sxs-lookup"><span data-stu-id="ab659-354">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="ab659-355">Добавлена поддержка пользовательских заголовков в профилях.</span><span class="sxs-lookup"><span data-stu-id="ab659-355">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="ab659-356">Добавлена поддержка диапазонов кода состояния ожидания в профилях.</span><span class="sxs-lookup"><span data-stu-id="ab659-356">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="ab659-357">Добавлена поддержка пользовательских заголовков в конечных точках.</span><span class="sxs-lookup"><span data-stu-id="ab659-357">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ab659-358">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ab659-358">AzureRM.Websites</span></span>
* <span data-ttu-id="ab659-359">Исправлена проблема с отсутствием правильной настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ab659-359">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="ab659-360">6.7.0 — август 2018 г.</span><span class="sxs-lookup"><span data-stu-id="ab659-360">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ab659-361">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ab659-361">AzureRM.Profile</span></span>
* <span data-ttu-id="ab659-362">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-362">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="ab659-363">Добавлен идентификатор пользователя для имени контекста по умолчанию, чтобы избежать конфликтов контекста.</span><span class="sxs-lookup"><span data-stu-id="ab659-363">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="ab659-364">Устранены проблемы с командлетом Clear-AzureRmContext, которые приводили к проблемам с выбором контекста #6398.</span><span class="sxs-lookup"><span data-stu-id="ab659-364">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="ab659-365">Разрешено передавать домен клиента в параметр -TenantId для командлета Connect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="ab659-365">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="ab659-366">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="ab659-366">Azure.Storage</span></span>
* <span data-ttu-id="ab659-367">Удалено ограничение в 5 ТБ для квоты на общую папку Azure.</span><span class="sxs-lookup"><span data-stu-id="ab659-367">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="ab659-368">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="ab659-368">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="ab659-369">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ab659-369">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="ab659-370">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-370">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="ab659-371">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ab659-371">Azure.AnalysisServices</span></span>
* <span data-ttu-id="ab659-372">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-372">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="ab659-373">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ab659-373">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="ab659-374">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-374">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="ab659-375">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="ab659-375">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="ab659-376">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-376">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="ab659-377">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="ab659-377">AzureRM.Automation</span></span>
* <span data-ttu-id="ab659-378">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-378">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="ab659-379">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="ab659-379">AzureRM.Backup</span></span>
* <span data-ttu-id="ab659-380">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-380">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="ab659-381">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="ab659-381">AzureRM.Batch</span></span>
* <span data-ttu-id="ab659-382">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-382">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="ab659-383">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="ab659-383">AzureRM.Billing</span></span>
* <span data-ttu-id="ab659-384">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-384">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="ab659-385">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="ab659-385">AzureRM.Cdn</span></span>
* <span data-ttu-id="ab659-386">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-386">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="ab659-387">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ab659-387">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="ab659-388">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-388">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ab659-389">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ab659-389">AzureRM.Compute</span></span>
* <span data-ttu-id="ab659-390">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-390">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="ab659-391">В командлет New-AzureRmVmssConfig добавлен параметр EvictionPolicy.</span><span class="sxs-lookup"><span data-stu-id="ab659-391">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="ab659-392">Если расположение не указано, используйте в DiskFileParameterSet для New AzureRmVm расположение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ab659-392">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="ab659-393">Исправлено описание параметров в Save-AzureRmVMImage.</span><span class="sxs-lookup"><span data-stu-id="ab659-393">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="ab659-394">Исправлен командлет Get-AzureRmVMDiskEncryptionStatus для определенных сценариев, связанных с однократным выполнением.</span><span class="sxs-lookup"><span data-stu-id="ab659-394">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="ab659-395">AzureRM.Consumption:</span><span class="sxs-lookup"><span data-stu-id="ab659-395">AzureRM.Consumption</span></span>
* <span data-ttu-id="ab659-396">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-396">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="ab659-397">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ab659-397">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="ab659-398">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-398">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="ab659-399">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ab659-399">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="ab659-400">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-400">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="ab659-401">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="ab659-401">AzureRM.DataFactories</span></span>
* <span data-ttu-id="ab659-402">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-402">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="ab659-403">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ab659-403">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="ab659-404">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-404">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="ab659-405">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="ab659-405">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="ab659-406">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-406">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="ab659-407">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ab659-407">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="ab659-408">Исправлена отладка, когда DebugPreference настраивается из командной строки PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ab659-408">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="ab659-409">Обновлен пример для Set-AzureRmDataLakeStoreItemAcl.</span><span class="sxs-lookup"><span data-stu-id="ab659-409">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="ab659-410">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-410">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="ab659-411">Обновлен пример для Set-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="ab659-411">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="ab659-412">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="ab659-412">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="ab659-413">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-413">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="ab659-414">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="ab659-414">AzureRM.Dns</span></span>
* <span data-ttu-id="ab659-415">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-415">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="ab659-416">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ab659-416">AzureRM.EventGrid</span></span>
* <span data-ttu-id="ab659-417">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-417">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="ab659-418">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="ab659-418">AzureRM.EventHub</span></span>
* <span data-ttu-id="ab659-419">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-419">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="ab659-420">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ab659-420">AzureRM.HDInsight</span></span>
* <span data-ttu-id="ab659-421">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-421">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="ab659-422">AzureRM.Insights;</span><span class="sxs-lookup"><span data-stu-id="ab659-422">AzureRM.Insights</span></span>
* <span data-ttu-id="ab659-423">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-423">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="ab659-424">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="ab659-424">AzureRM.IotHub</span></span>
* <span data-ttu-id="ab659-425">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-425">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="ab659-426">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ab659-426">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ab659-427">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-427">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="ab659-428">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ab659-428">AzureRM.LogicApp</span></span>
* <span data-ttu-id="ab659-429">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-429">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="ab659-430">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="ab659-430">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="ab659-431">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-431">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="ab659-432">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="ab659-432">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="ab659-433">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-433">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="ab659-434">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="ab659-434">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="ab659-435">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-435">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="ab659-436">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="ab659-436">AzureRM.Media</span></span>
* <span data-ttu-id="ab659-437">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-437">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ab659-438">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ab659-438">AzureRM.Network</span></span>
* <span data-ttu-id="ab659-439">Добавлен пример для Set-AzureRmLocalNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="ab659-439">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="ab659-440">Добавлены примеры и описания для Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey и New-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="ab659-440">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="ab659-441">Добавлены примеры для Remove-AzureRmVirtualNetworkGatewayIpConfig и Reset-AzureRmVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="ab659-441">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="ab659-442">Добавлен пример для Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.</span><span class="sxs-lookup"><span data-stu-id="ab659-442">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="ab659-443">Добавлен пример для Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.</span><span class="sxs-lookup"><span data-stu-id="ab659-443">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="ab659-444">Добавлен пример для Set-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="ab659-444">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="ab659-445">Повторно созданы командлеты для ApplicationSecurityGroup, RouteTable и Usage с помощью генератора кода последней версии.</span><span class="sxs-lookup"><span data-stu-id="ab659-445">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="ab659-446">Уточнено сообщение об ошибке для Get-AzureRmVirtualNetworkSubnetConfig при попытке получить подсеть, которая не существует.</span><span class="sxs-lookup"><span data-stu-id="ab659-446">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="ab659-447">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="ab659-447">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="ab659-448">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-448">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="ab659-449">AzureRM.OperationalInsights;</span><span class="sxs-lookup"><span data-stu-id="ab659-449">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="ab659-450">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-450">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="ab659-451">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ab659-451">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="ab659-452">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-452">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="ab659-453">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="ab659-453">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="ab659-454">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-454">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="ab659-455">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ab659-455">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="ab659-456">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-456">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="ab659-457">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="ab659-457">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="ab659-458">Добавлен фильтр политик для командлета Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="ab659-458">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="ab659-459">Команда возвращает список элементов резервного копирования, защищенных политикой с заданным идентификатором.</span><span class="sxs-lookup"><span data-stu-id="ab659-459">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="ab659-460">Обновление Microsoft.Azure.Management.RecoveryServices.Backup до версии 3.0.0-preview.</span><span class="sxs-lookup"><span data-stu-id="ab659-460">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="ab659-461">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-461">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="ab659-462">Добавлен параметр TargetResourceGroupName для Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="ab659-462">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="ab659-463">Группа ресурсов, в которую восстанавливаются управляемые диски.</span><span class="sxs-lookup"><span data-stu-id="ab659-463">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="ab659-464">Применимо к резервной копии виртуальной машины с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="ab659-464">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="ab659-465">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="ab659-465">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="ab659-466">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-466">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="ab659-467">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ab659-467">AzureRM.RedisCache</span></span>
* <span data-ttu-id="ab659-468">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-468">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="ab659-469">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="ab659-469">AzureRM.Relay</span></span>
* <span data-ttu-id="ab659-470">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-470">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ab659-471">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ab659-471">AzureRM.Resources</span></span>
* <span data-ttu-id="ab659-472">Поддержка развертывания шаблонов в области подписки.</span><span class="sxs-lookup"><span data-stu-id="ab659-472">Support template deployment at subscription scope.</span></span> <span data-ttu-id="ab659-473">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="ab659-473">Add new Cmdlets:</span></span>
    - <span data-ttu-id="ab659-474">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ab659-474">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="ab659-475">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ab659-475">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="ab659-476">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ab659-476">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="ab659-477">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ab659-477">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="ab659-478">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ab659-478">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="ab659-479">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="ab659-479">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="ab659-480">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="ab659-480">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="ab659-481">Устранена проблема, когда при передаче контекста в Set-AzureRmResource возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="ab659-481">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="ab659-482">Исправлен пример в New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="ab659-482">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="ab659-483">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-483">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="ab659-484">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="ab659-484">AzureRM.Scheduler</span></span>
* <span data-ttu-id="ab659-485">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-485">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ab659-486">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ab659-486">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ab659-487">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-487">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="ab659-488">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ab659-488">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="ab659-489">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-489">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ab659-490">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ab659-490">AzureRM.Sql</span></span>
* <span data-ttu-id="ab659-491">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-491">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="ab659-492">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="ab659-492">AzureRM.Storage</span></span>
* <span data-ttu-id="ab659-493">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-493">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="ab659-494">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="ab659-494">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="ab659-495">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-495">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="ab659-496">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="ab659-496">AzureRM.Tags</span></span>
* <span data-ttu-id="ab659-497">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-497">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="ab659-498">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ab659-498">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="ab659-499">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-499">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="ab659-500">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="ab659-500">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="ab659-501">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-501">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ab659-502">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ab659-502">AzureRM.Websites</span></span>
* <span data-ttu-id="ab659-503">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-503">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="ab659-504">6.6.0 — июль 2018 г.</span><span class="sxs-lookup"><span data-stu-id="ab659-504">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ab659-505">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="ab659-505">General</span></span>
* <span data-ttu-id="ab659-506">Обновлены все файлы справки: включены полные типы параметров и исправлены типы входных и выходных данных.</span><span class="sxs-lookup"><span data-stu-id="ab659-506">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="ab659-507">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ab659-507">AzureRM.Profile</span></span>
* <span data-ttu-id="ab659-508">Обновлена библиотека Common.Strategy: теперь можно проверить, совместима ли текущая конфигурация ресурса с целевым ресурсом.</span><span class="sxs-lookup"><span data-stu-id="ab659-508">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="ab659-509">В Common.Storage добавлены типы ps1xml.</span><span class="sxs-lookup"><span data-stu-id="ab659-509">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="ab659-510">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="ab659-510">Azure.Storage</span></span>
* <span data-ttu-id="ab659-511">Добавлена поддержка для получения контекста хранилища из DefaultProfile.</span><span class="sxs-lookup"><span data-stu-id="ab659-511">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="ab659-512">В свойства типов выходных данных командлетов добавлен атрибут Ps1XmlAttribute.</span><span class="sxs-lookup"><span data-stu-id="ab659-512">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="ab659-513">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ab659-513">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="ab659-514">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6370.</span><span class="sxs-lookup"><span data-stu-id="ab659-514">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="ab659-515">В AutoMapper исправлена ошибка, препятствовавшая преобразованию PsApiManagementApi в ApiContract.</span><span class="sxs-lookup"><span data-stu-id="ab659-515">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="ab659-516">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6515.</span><span class="sxs-lookup"><span data-stu-id="ab659-516">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="ab659-517">В File.Save исправлена ошибка, связанная с перегрузкой типом кодировки.</span><span class="sxs-lookup"><span data-stu-id="ab659-517">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="ab659-518">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6560.</span><span class="sxs-lookup"><span data-stu-id="ab659-518">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="ab659-519">Выполнено обновление до версии NuGet 4.0.3, что позволило исправить исключение шаблона в apiId.</span><span class="sxs-lookup"><span data-stu-id="ab659-519">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ab659-520">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ab659-520">AzureRM.Compute</span></span>
* <span data-ttu-id="ab659-521">Устранена ошибка при создании виртуальной машины с помощью командлета New-AzureRmVm и параметра DiskFileParameterSet, которая возникала из-за переименования типа учетной записи хранения PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="ab659-521">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="ab659-522">Исправлен командлет Invoke-AzureRmVMRunCommand.</span><span class="sxs-lookup"><span data-stu-id="ab659-522">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="ab659-523">Командлет Get-AzureRmAvailabilitySet теперь может выводить список всех групп доступности в подписке.</span><span class="sxs-lookup"><span data-stu-id="ab659-523">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="ab659-524">(Параметр ResouceGroupName теперь является необязательным.)</span><span class="sxs-lookup"><span data-stu-id="ab659-524">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="ab659-525">Обновлен параметр SimpleParameterSet командлета New-AzureRmVm, что позволило использовать ускоренную сеть на соответствующих виртуальных машинах.</span><span class="sxs-lookup"><span data-stu-id="ab659-525">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="ab659-526">Обновлен простой набор параметров New-AzureRmVmss, что позволило отменять создание масштабируемого набора виртуальных машин, если указанная пользователем подсистема балансировки нагрузки уже существует.</span><span class="sxs-lookup"><span data-stu-id="ab659-526">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="ab659-527">Обновлен пример для New-AzureRmDisk.</span><span class="sxs-lookup"><span data-stu-id="ab659-527">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="ab659-528">Добавлен пример для New-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="ab659-528">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="ab659-529">Обновлено описание командлета Set-AzureRmVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="ab659-529">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="ab659-530">Обновлен пример 1 для Set-AzureRmVMBginfoExtension: исправлены орфографические ошибки и префикс.</span><span class="sxs-lookup"><span data-stu-id="ab659-530">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="ab659-531">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ab659-531">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="ab659-532">Пакет .NET SDK для ADF обновлен до версии 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="ab659-532">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="ab659-533">Добавлена поддержка совместного использования локальной среды IR несколькими фабриками данных.</span><span class="sxs-lookup"><span data-stu-id="ab659-533">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="ab659-534">Добавлен новый параметр -SharedIntegrationRuntimeResourceId для командлета Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-534">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="ab659-535">Добавлен новый необязательный параметр -LinkedDataFactoryName для командлета Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="ab659-535">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="ab659-536">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ab659-536">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="ab659-537">Пакет SDK для плоскости данных (Microsoft.Azure.DataLake.Store) обновлен до версии 1.1.9.</span><span class="sxs-lookup"><span data-stu-id="ab659-537">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="ab659-538">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="ab659-538">AzureRM.EventHub</span></span>
* <span data-ttu-id="ab659-539">Обновлена конвейерная передача для InputObject и ResourceId в командлетах remove.</span><span class="sxs-lookup"><span data-stu-id="ab659-539">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="ab659-540">AzureRM.Insights;</span><span class="sxs-lookup"><span data-stu-id="ab659-540">AzureRM.Insights</span></span>
* <span data-ttu-id="ab659-541">Исправлено форматирование OutputType в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="ab659-541">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="ab659-542">Применен пакет SDK Microsoft.Azure.Management.Monitor 0.19.1-preview.</span><span class="sxs-lookup"><span data-stu-id="ab659-542">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="ab659-543">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ab659-543">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ab659-544">Исправлена проблема с конвейерной передачей в командлете Set-AzureRmKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="ab659-544">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ab659-545">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ab659-545">AzureRM.Network</span></span>
* <span data-ttu-id="ab659-546">Добавлены примеры для командлетов LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="ab659-546">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ab659-547">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ab659-547">AzureRM.Resources</span></span>
* <span data-ttu-id="ab659-548">Устранена проблема, возникавшая при указании имени и значения тега для Get-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="ab659-548">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="ab659-549">Исправлен сценарий конвейерной передачи в Set-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="ab659-549">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ab659-550">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ab659-550">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ab659-551">Обновлена конвейерная передача для InputObject и ResourceId в командлетах remove.</span><span class="sxs-lookup"><span data-stu-id="ab659-551">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="ab659-552">Исправлено несколько ошибок.</span><span class="sxs-lookup"><span data-stu-id="ab659-552">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="ab659-553">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ab659-553">AzureRM.Sql</span></span>
* <span data-ttu-id="ab659-554">Добавлена поддержка Advanced Threat Protection для сервера с помощью следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="ab659-554">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="ab659-555">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="ab659-555">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="ab659-556">Добавлена поддержка оценки уязвимостей с помощью следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="ab659-556">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="ab659-557">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings;</span><span class="sxs-lookup"><span data-stu-id="ab659-557">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="ab659-558">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline;</span><span class="sxs-lookup"><span data-stu-id="ab659-558">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="ab659-559">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan.</span><span class="sxs-lookup"><span data-stu-id="ab659-559">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="ab659-560">Исправлен пример для Remove-AzureRmSqlServerFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="ab659-560">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="ab659-561">Исправлена неправильная обработка даты и времени для базового языка и региональных параметров, отличных от США, в Get-AzureSqlSyncGroupLog.</span><span class="sxs-lookup"><span data-stu-id="ab659-561">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="ab659-562">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="ab659-562">AzureRM.Storage</span></span>
* <span data-ttu-id="ab659-563">В свойства типов выходных данных командлетов добавлен атрибут Ps1XmlAttribute.</span><span class="sxs-lookup"><span data-stu-id="ab659-563">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="ab659-564">Выходные данные командлетов StorageAccount теперь отображаются в виде таблицы.</span><span class="sxs-lookup"><span data-stu-id="ab659-564">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="ab659-565">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ab659-565">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="ab659-566">New-AzureRmStorageAccount;</span><span class="sxs-lookup"><span data-stu-id="ab659-566">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="ab659-567">Set-AzureRmStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="ab659-567">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="ab659-568">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="ab659-568">AzureRM.Tags</span></span>
* <span data-ttu-id="ab659-569">Удалено неверное утверждение из справки по командлетам Tag.</span><span class="sxs-lookup"><span data-stu-id="ab659-569">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="ab659-570">6.5.0 — июль 2018 г.</span><span class="sxs-lookup"><span data-stu-id="ab659-570">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ab659-571">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ab659-571">AzureRM.Profile</span></span>
* <span data-ttu-id="ab659-572">Обновлена справка для командлета Get-AzureRmContextAutosaveSetting.</span><span class="sxs-lookup"><span data-stu-id="ab659-572">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="ab659-573">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="ab659-573">Azure.Storage</span></span>
* <span data-ttu-id="ab659-574">Добавлена поддержка отправки BLOB-объекта или файла с помощью токена SAS, доступного только для записи.</span><span class="sxs-lookup"><span data-stu-id="ab659-574">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="ab659-575">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ab659-575">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="ab659-576">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ab659-576">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="ab659-577">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ab659-577">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="ab659-578">Для AS добавлено обязательное свойство ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="ab659-578">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="ab659-579">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="ab659-579">AzureRM.Automation</span></span>
* <span data-ttu-id="ab659-580">Обновлена справка и добавлены примеры для командлета New-AzureRMAutomationSchedule.</span><span class="sxs-lookup"><span data-stu-id="ab659-580">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ab659-581">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ab659-581">AzureRM.Compute</span></span>
* <span data-ttu-id="ab659-582">Добавлен параметр -Tag для командлета Update/New-AzureRmAvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="ab659-582">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="ab659-583">Добавлен пример для командлета Add-AzureRmVmssExtension.</span><span class="sxs-lookup"><span data-stu-id="ab659-583">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="ab659-584">Добавлены примеры для командлета Remove-AzureRmVmssExtension.</span><span class="sxs-lookup"><span data-stu-id="ab659-584">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="ab659-585">Обновлена справка для командлета Set-AzureRmVMAccessExtension.</span><span class="sxs-lookup"><span data-stu-id="ab659-585">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="ab659-586">Изменен класс SimpleParameterSet для командлета New-AzureRmVmss: теперь для SinglePlacementGroup по умолчанию задается значение false, а также добавляется параметр-переключатель SinglePlacementGroup, который позволяет пользователю создать VMSS в одной группе размещения.</span><span class="sxs-lookup"><span data-stu-id="ab659-586">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="ab659-587">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="ab659-587">AzureRM.EventHub</span></span>
* <span data-ttu-id="ab659-588">В класс PSEventHubDRConfigurationAttributes добавлено доступное только для чтения свойство PendingReplicationOperationsCount, которое показывает количество ожидающих репликации операций во время реплицирования.</span><span class="sxs-lookup"><span data-stu-id="ab659-588">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="ab659-589">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ab659-589">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ab659-590">Обновлено сообщение об ошибке для командлета Set-AzureRmKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="ab659-590">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="ab659-591">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ab659-591">AzureRM.LogicApp</span></span>
* <span data-ttu-id="ab659-592">Исправлена ошибка "parameter set could not be resolved" (не удалось разрешить заданный параметр) в командлете New-AzureRmLogicApp.</span><span class="sxs-lookup"><span data-stu-id="ab659-592">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ab659-593">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ab659-593">AzureRM.Network</span></span>
* <span data-ttu-id="ab659-594">Включен пиринг между виртуальными сетями в нескольких клиентах для командлета Set/Add-AzureRmVirtualNetworkPeering.</span><span class="sxs-lookup"><span data-stu-id="ab659-594">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="ab659-595">Для шлюза приложений обновлены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="ab659-595">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="ab659-596">New-AzureRmApplicationGateway: добавлены флаг EnableFIPS и поддержка зон.</span><span class="sxs-lookup"><span data-stu-id="ab659-596">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="ab659-597">New-AzureRmApplicationGatewaySku: добавлены новые номера SKU Standard_v2 и WAF_v2.</span><span class="sxs-lookup"><span data-stu-id="ab659-597">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="ab659-598">Set-AzureRmApplicationGatewaySku: добавлены новые номера SKU Standard_v2 и WAF_v2.</span><span class="sxs-lookup"><span data-stu-id="ab659-598">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="ab659-599">Командлеты RouteTable пересозданы в последней версии генератора.</span><span class="sxs-lookup"><span data-stu-id="ab659-599">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="ab659-600">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="ab659-600">AzureRM.Relay</span></span>
* <span data-ttu-id="ab659-601">Обновлены файлы Markdown, исправлена проблема с именем параметра в примере.</span><span class="sxs-lookup"><span data-stu-id="ab659-601">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ab659-602">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ab659-602">AzureRM.Resources</span></span>
* <span data-ttu-id="ab659-603">Обновлены командлеты Roleassignment и roledefinition:</span><span class="sxs-lookup"><span data-stu-id="ab659-603">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="ab659-604">Удалены лишние вызовы roledefinition, выполняемые в ходе разбиения на страницы.</span><span class="sxs-lookup"><span data-stu-id="ab659-604">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="ab659-605">Исправлен командлет Get-AzureRmRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="ab659-605">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="ab659-606">Исправлена работа параметра -ExpandPrincipalGroups.</span><span class="sxs-lookup"><span data-stu-id="ab659-606">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="ab659-607">Устранена проблема в командлете Get-AzureRmResource, заключающая в том, что в параметре -ResourceType учитывался регистр символов.</span><span class="sxs-lookup"><span data-stu-id="ab659-607">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ab659-608">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ab659-608">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ab659-609">Добавлены параметры top и skip для командлетов list.</span><span class="sxs-lookup"><span data-stu-id="ab659-609">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="ab659-610">Добавлены командлеты для перехода с пространства имен ценовой категории "Стандартный" на пространство ценовой категории "Премиум":</span><span class="sxs-lookup"><span data-stu-id="ab659-610">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="ab659-611">Start-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="ab659-611">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="ab659-612">Get-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="ab659-612">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="ab659-613">Complete-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="ab659-613">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="ab659-614">Stop-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="ab659-614">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="ab659-615">Remove-AzureRmServiceBusMigration.</span><span class="sxs-lookup"><span data-stu-id="ab659-615">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="ab659-616">В класс PSServiceBusDRConfigurationAttributes добавлено доступное только для чтения свойство PendingReplicationOperationsCount, которое показывает количество ожидающих репликации операций во время реплицирования.</span><span class="sxs-lookup"><span data-stu-id="ab659-616">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="ab659-617">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ab659-617">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="ab659-618">Обновлен пример для командлета New-AzureRmServiceFabricCluster.</span><span class="sxs-lookup"><span data-stu-id="ab659-618">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ab659-619">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ab659-619">AzureRM.Sql</span></span>
* <span data-ttu-id="ab659-620">Добавлены новые командлеты для Management.Sql, позволяющие клиентам добавлять сертификат TDE в экземпляр SQL Server или управляемый экземпляр:</span><span class="sxs-lookup"><span data-stu-id="ab659-620">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="ab659-621">Add-AzureRmSqlServerTransparentDataEncryptionCertificate;</span><span class="sxs-lookup"><span data-stu-id="ab659-621">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="ab659-622">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate.</span><span class="sxs-lookup"><span data-stu-id="ab659-622">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ab659-623">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ab659-623">AzureRM.Websites</span></span>
* <span data-ttu-id="ab659-624">`Set-AzureRmWebApp -AssignIdentity` и `Set-AzureRmWebAppSlot -AssignIdentity` при установленном значении false теперь будут удалять свойство Identity из объекта сайта. Также при этом будет удаляться тег предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="ab659-624">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="ab659-625">Обновлен пример для `Get-AzureRmWebAppMetrics` и `Get-AzureRmAppServicePlanMetrics`.</span><span class="sxs-lookup"><span data-stu-id="ab659-625">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="ab659-626">`Set-AzureRmWebApp -PhpVersion` теперь поддерживает off как допустимую версию PHP.</span><span class="sxs-lookup"><span data-stu-id="ab659-626">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="ab659-627">6.4.0 — июль 2018 г.</span><span class="sxs-lookup"><span data-stu-id="ab659-627">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ab659-628">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="ab659-628">General</span></span>
* <span data-ttu-id="ab659-629">Исправлено форматирование OutputType в файлах справки для большинства модулей.</span><span class="sxs-lookup"><span data-stu-id="ab659-629">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="ab659-630">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ab659-630">AzureRM.Profile</span></span>
* <span data-ttu-id="ab659-631">В основные типы выходных данных добавлен атрибут Ps1Xml.</span><span class="sxs-lookup"><span data-stu-id="ab659-631">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ab659-632">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ab659-632">AzureRM.Compute</span></span>
* <span data-ttu-id="ab659-633">Функция добавления тега IP-адреса для масштабируемого набора виртуальных машин (VMSS)</span><span class="sxs-lookup"><span data-stu-id="ab659-633">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="ab659-634">Добавлен командлет New-AzureRmVmssIpTagConfig.</span><span class="sxs-lookup"><span data-stu-id="ab659-634">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="ab659-635">В New-AzureRmVmssIpConfig добавлен параметр IpTag.</span><span class="sxs-lookup"><span data-stu-id="ab659-635">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="ab659-636">Функция автоматического отката ОС для VMSS</span><span class="sxs-lookup"><span data-stu-id="ab659-636">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="ab659-637">В New-AzureRmVmssConfig и Update-AzureRmVmss добавлены параметры DisableAutoRollback.</span><span class="sxs-lookup"><span data-stu-id="ab659-637">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="ab659-638">Функция ведения журнала обновлений ОС для VMSS</span><span class="sxs-lookup"><span data-stu-id="ab659-638">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="ab659-639">В Get-AzureRmVmss добавлен параметр OSUpgradeHistory.</span><span class="sxs-lookup"><span data-stu-id="ab659-639">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="ab659-640">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="ab659-640">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="ab659-641">Добавлена поддержка списков управления доступом к каталогу с использованием следующих команд:</span><span class="sxs-lookup"><span data-stu-id="ab659-641">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="ab659-642">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry;</span><span class="sxs-lookup"><span data-stu-id="ab659-642">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="ab659-643">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry;</span><span class="sxs-lookup"><span data-stu-id="ab659-643">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="ab659-644">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="ab659-644">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="ab659-645">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ab659-645">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="ab659-646">Добавлены поддержка отмены выполнения и отслеживание хода выполнения для Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl и Remove-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="ab659-646">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="ab659-647">Добавлена поддержка отмены выполнения для Export-AzureRmDataLakeStoreChildItemProperties.</span><span class="sxs-lookup"><span data-stu-id="ab659-647">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="ab659-648">Исправлена очистка сообщений об отладке для командлетов, которые выполняют рекурсивные операции.</span><span class="sxs-lookup"><span data-stu-id="ab659-648">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="ab659-649">Исправлено расположение тестовых данных для командлетов DataLake.</span><span class="sxs-lookup"><span data-stu-id="ab659-649">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="ab659-650">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="ab659-650">AzureRM.EventHub</span></span>
* <span data-ttu-id="ab659-651">Для командлетов вывода списка операций Get-AzureRmEventHub и Get-AzureRmEventHubConsumerGroup добавлен необязательный параметр MaxCount.</span><span class="sxs-lookup"><span data-stu-id="ab659-651">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="ab659-652">Исправлена проблема с командлетом New-AzureRmEventHub, из-за которой требовалось указать по крайней мере один параметр при создании концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="ab659-652">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="ab659-653">Добавлен набор параметров по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ab659-653">Provided Default Parameter set.</span></span>
* <span data-ttu-id="ab659-654">Для командлета New-AzureRmEventHubKey добавлен необязательный параметр -KeyValue, который позволяет пользователю предоставить значение ключа.</span><span class="sxs-lookup"><span data-stu-id="ab659-654">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="ab659-655">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ab659-655">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ab659-656">Исправлена ошибка, из-за которой при выполнении командлета Get-AzureRmKeyVault с параметром -Tag возвращались все ресурсы.</span><span class="sxs-lookup"><span data-stu-id="ab659-656">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ab659-657">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ab659-657">AzureRM.Network</span></span>
* <span data-ttu-id="ab659-658">Для параметра шлюзов виртуальной вести, избыточных в пределах зоны, предоставлены новые номера SKU.</span><span class="sxs-lookup"><span data-stu-id="ab659-658">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="ab659-659">Добавлены новые команды для функции поддержки партнерских API для ExpressRoute, развертываемых с помощью ARM:</span><span class="sxs-lookup"><span data-stu-id="ab659-659">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="ab659-660">добавлена команда Get-AzureRmExpressRouteCrossConnection;</span><span class="sxs-lookup"><span data-stu-id="ab659-660">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="ab659-661">добавлена команда Set-AzureRmExpressRouteCrossConnection;</span><span class="sxs-lookup"><span data-stu-id="ab659-661">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="ab659-662">добавлена команда Add-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="ab659-662">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="ab659-663">добавлена команда Get-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="ab659-663">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="ab659-664">добавлена команда Remove-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="ab659-664">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="ab659-665">добавлена команда Get-AzureRMExpressRouteCrossConnectionArpTable;</span><span class="sxs-lookup"><span data-stu-id="ab659-665">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="ab659-666">добавлена команда Get-AzureRMExpressRouteCrossConnectionRouteTable;</span><span class="sxs-lookup"><span data-stu-id="ab659-666">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="ab659-667">добавлена команда Get-AzureRMExpressRouteCrossConnectionRouteTableSummary.</span><span class="sxs-lookup"><span data-stu-id="ab659-667">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="ab659-668">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="ab659-668">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="ab659-669">Добавлен командлет Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="ab659-669">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="ab659-670">Этот командлет принимает идентификатор виртуальной машины и проверяет, защищена ли виртуальная машина с помощью какого-либо хранилища в подписке.</span><span class="sxs-lookup"><span data-stu-id="ab659-670">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="ab659-671">Если такое хранилище существует, командлет выводит данные о нем.</span><span class="sxs-lookup"><span data-stu-id="ab659-671">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ab659-672">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ab659-672">AzureRM.Resources</span></span>
* <span data-ttu-id="ab659-673">Обновлены командлеты Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="ab659-673">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="ab659-674">Добавлена поддержка вывода списка значений параметра -Scope на уровне группы управления.</span><span class="sxs-lookup"><span data-stu-id="ab659-674">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="ab659-675">Добавлена поддержка для получения отдельных назначений со значениями -Scope на уровне группы управления.</span><span class="sxs-lookup"><span data-stu-id="ab659-675">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="ab659-676">Для параметра управления добавлены параметры -Effective и -All.</span><span class="sxs-lookup"><span data-stu-id="ab659-676">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="ab659-677">Обновлены командлеты Get/New/Remove/Set-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="ab659-677">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="ab659-678">Добавлен параметр -ManagementGroupName для применения операций к заданной группе управления.</span><span class="sxs-lookup"><span data-stu-id="ab659-678">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="ab659-679">Добавлен параметр -SubscriptionId для применения операций к заданной подписке.</span><span class="sxs-lookup"><span data-stu-id="ab659-679">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="ab659-680">Обновлены командлеты Get/New/Remove/Set-AzureRmPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="ab659-680">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="ab659-681">Добавлен параметр -ManagementGroupName для применения операций к заданной группе управления.</span><span class="sxs-lookup"><span data-stu-id="ab659-681">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="ab659-682">Добавлен параметр -SubscriptionId для применения операций к заданной подписке.</span><span class="sxs-lookup"><span data-stu-id="ab659-682">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="ab659-683">Добавлена поддержка ссылок на секрет KeyVault в параметрах при использовании TemplateParameterObject в New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="ab659-683">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="ab659-684">Устранена проблема, из-за которой параметр -EndDate игнорировался в New-AzureRmADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="ab659-684">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="ab659-685">Устранена проблема, из-за которой в Add-AzureRmADGroupMember использовался неверный URL-адрес для запроса.</span><span class="sxs-lookup"><span data-stu-id="ab659-685">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="ab659-686">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ab659-686">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ab659-687">Для командлета New-AzureRmServiceBusKey добавлен необязательный параметр -KeyValue, который позволяет пользователю предоставить значение ключа.</span><span class="sxs-lookup"><span data-stu-id="ab659-687">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ab659-688">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ab659-688">AzureRM.Sql</span></span>
* <span data-ttu-id="ab659-689">В справке по New-AzureRmSqlDatabaseRestorePoint добавлено описание определяемых пользователем точек восстановления для хранилища данных SQL.</span><span class="sxs-lookup"><span data-stu-id="ab659-689">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="ab659-690">Обновлена документация по параметру -ComputeGeneration, используемого в нескольких командлетах.</span><span class="sxs-lookup"><span data-stu-id="ab659-690">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="ab659-691">6.3.0 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="ab659-691">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ab659-692">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ab659-692">AzureRM.Profile</span></span>
* <span data-ttu-id="ab659-693">Обновлены сообщения об ошибках для Enable-AzureRmContextAutoSave.</span><span class="sxs-lookup"><span data-stu-id="ab659-693">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="ab659-694">Создание контекста для каждой подписки при выполнении Connect-AzureRmAccount без предыдущего контекста.</span><span class="sxs-lookup"><span data-stu-id="ab659-694">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="ab659-695">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="ab659-695">Azure.Storage</span></span>
* <span data-ttu-id="ab659-696">В файлы справки добавлены дополнительные сведения о параметре -Permissions.</span><span class="sxs-lookup"><span data-stu-id="ab659-696">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ab659-697">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ab659-697">AzureRM.Compute</span></span>
* <span data-ttu-id="ab659-698">Get-AzureRmVmDiskEncryptionStatus устраняет проблему, которая наблюдалась на виртуальных машинах без дисков данных.</span><span class="sxs-lookup"><span data-stu-id="ab659-698">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="ab659-699">Обновлена версия клиентской библиотеки Compute для исправления следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="ab659-699">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="ab659-700">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="ab659-700">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="ab659-701">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="ab659-701">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="ab659-702">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="ab659-702">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="ab659-703">В следующих командлетах исправлено отображение неправильных значений operation ID и operation status:</span><span class="sxs-lookup"><span data-stu-id="ab659-703">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="ab659-704">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ab659-704">Start-AzureRmVM</span></span>
    - <span data-ttu-id="ab659-705">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ab659-705">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="ab659-706">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ab659-706">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="ab659-707">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ab659-707">Set-AzureRmVM</span></span>
    - <span data-ttu-id="ab659-708">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="ab659-708">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="ab659-709">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ab659-709">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="ab659-710">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="ab659-710">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="ab659-711">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="ab659-711">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="ab659-712">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ab659-712">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="ab659-713">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ab659-713">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="ab659-714">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ab659-714">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="ab659-715">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ab659-715">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="ab659-716">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="ab659-716">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="ab659-717">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="ab659-717">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="ab659-718">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="ab659-718">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="ab659-719">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="ab659-719">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="ab659-720">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="ab659-720">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="ab659-721">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="ab659-721">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="ab659-722">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ab659-722">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="ab659-723">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ab659-723">AzureRM.EventGrid</span></span>
* <span data-ttu-id="ab659-724">Удалены условия проверки ValidateNotNullOrEmpty для SubjectBeginsWith/SubjectEndsWith в командлете Update-AzureRmEventGridSubscription, что позволяет при необходимости заменять эти параметры пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="ab659-724">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="ab659-725">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ab659-725">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ab659-726">Исправлена ошибка, когда при выполнении командлета Get-AzureRmKeyVault -Tag не возвращается ни один тег.</span><span class="sxs-lookup"><span data-stu-id="ab659-726">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="ab659-727">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ab659-727">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="ab659-728">Общедоступный выпуск командлетов Policy Insights.</span><span class="sxs-lookup"><span data-stu-id="ab659-728">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="ab659-729">Используется API версии 2018-04-04.</span><span class="sxs-lookup"><span data-stu-id="ab659-729">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="ab659-730">К результатам Get-AzureRmPolicyStateSummary добавлено PolicyDefinitionReferenceId.</span><span class="sxs-lookup"><span data-stu-id="ab659-730">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="ab659-731">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="ab659-731">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="ab659-732">Для командлетов RecoveryServices.Backup добавлен параметр -Vault.</span><span class="sxs-lookup"><span data-stu-id="ab659-732">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="ab659-733">Передача этого параметра переопределяет командлет Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="ab659-733">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ab659-734">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ab659-734">AzureRM.Sql</span></span>
* <span data-ttu-id="ab659-735">В файле справки обновлен пример для командлета Get-AzureRmSqlDatabaseExpanded.</span><span class="sxs-lookup"><span data-stu-id="ab659-735">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="ab659-736">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ab659-736">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="ab659-737">Обновлен файл справки для командлета Add-AzureRmTrafficManagerEndpointConfig.</span><span class="sxs-lookup"><span data-stu-id="ab659-737">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ab659-738">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ab659-738">AzureRM.Websites</span></span>
* <span data-ttu-id="ab659-739">Изменено действие командлета Set-AzureRmWebApp. Теперь он не перезаписывает AppSettings, если используется параметр -AssignIdentity.</span><span class="sxs-lookup"><span data-stu-id="ab659-739">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="ab659-740">Командлет New-AzureRmWebAppSlot теперь учитывает дополнительный параметр AppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="ab659-740">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="ab659-741">6.2.1 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="ab659-741">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="ab659-742">AzureRM.OperationalInsights;</span><span class="sxs-lookup"><span data-stu-id="ab659-742">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="ab659-743">В обновленной модели PSWorkspace Network может использовать type в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="ab659-743">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="ab659-744">6.2.0 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="ab659-744">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ab659-745">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ab659-745">AzureRM.Profile</span></span>
* <span data-ttu-id="ab659-746">Исправлена ошибка с загрузкой Newtonsoft.Json версии 10.0.3 во время импорта модуля.</span><span class="sxs-lookup"><span data-stu-id="ab659-746">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ab659-747">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ab659-747">AzureRM.Compute</span></span>
* <span data-ttu-id="ab659-748">Функция обновления виртуальных машин VMSS.</span><span class="sxs-lookup"><span data-stu-id="ab659-748">VMSS VM Update feature</span></span>
    - <span data-ttu-id="ab659-749">Добавлены командлеты Update-AzureRmVmssVM и New-AzureRmVMDataDisk.</span><span class="sxs-lookup"><span data-stu-id="ab659-749">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="ab659-750">В командлет Add-AzureRmVMDataDisk добавлен параметр VirtualMachineScaleSetVM, который позволяет добавлять диски данных в виртуальные машины VMSS.</span><span class="sxs-lookup"><span data-stu-id="ab659-750">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="ab659-751">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ab659-751">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="ab659-752">Пакет SDK для ADF .NET обновлен до версии 0.8.0-preview. Новая версия содержит такие изменения:</span><span class="sxs-lookup"><span data-stu-id="ab659-752">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="ab659-753">добавлена операция для настройки репозитория фабрики;</span><span class="sxs-lookup"><span data-stu-id="ab659-753">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="ab659-754">связанная служба QuickBooks LinkedService теперь предоставляет свойства consumerKey и consumerSecret;</span><span class="sxs-lookup"><span data-stu-id="ab659-754">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="ab659-755">тип нескольких моделей изменен с SecretBase на Object;</span><span class="sxs-lookup"><span data-stu-id="ab659-755">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="ab659-756">добавлен триггер событий BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="ab659-756">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="ab659-757">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ab659-757">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ab659-758">В документацию добавлены примеры выходных данных.</span><span class="sxs-lookup"><span data-stu-id="ab659-758">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="ab659-759">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ab659-759">AzureRM.Network</span></span>
* <span data-ttu-id="ab659-760">В командлеты Наблюдателя за сетями добавлены параметры Аналитики трафика.</span><span class="sxs-lookup"><span data-stu-id="ab659-760">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ab659-761">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ab659-761">AzureRM.Resources</span></span>
* <span data-ttu-id="ab659-762">Исправлена ошибка, когда командлет Get-AzureRmResource возвращает свойство Properties объектов PSResource.</span><span class="sxs-lookup"><span data-stu-id="ab659-762">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="ab659-763">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="ab659-763">AzureRM.Scheduler</span></span>
* <span data-ttu-id="ab659-764">Исправлена ошибка, когда обновление ServiceBusQueueJob не задает новые значения для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="ab659-764">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="ab659-765">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ab659-765">AzureRM.Sql</span></span>
* <span data-ttu-id="ab659-766">В перечисленные ниже командлеты добавлен необязательный параметр LicenseType.</span><span class="sxs-lookup"><span data-stu-id="ab659-766">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="ab659-767">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="ab659-767">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="ab659-768">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool;</span><span class="sxs-lookup"><span data-stu-id="ab659-768">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="ab659-769">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="ab659-769">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="ab659-770">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ab659-770">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="ab659-771">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ab659-771">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ab659-772">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ab659-772">AzureRM.Websites</span></span>
* <span data-ttu-id="ab659-773">Командлет New-AzureRMWebApp теперь использует общие алгоритмы из библиотеки Strategy.</span><span class="sxs-lookup"><span data-stu-id="ab659-773">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="ab659-774">6.1.0 — май 2018 г.</span><span class="sxs-lookup"><span data-stu-id="ab659-774">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ab659-775">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ab659-775">AzureRM.Profile</span></span>
* <span data-ttu-id="ab659-776">Устранена проблема с выполнением Clear-AzureRmContext, при которой сохранялся пустой контекст с именем предыдущего контекста по умолчанию, что не позволяло пользователю создать новый контекст со старым именем.</span><span class="sxs-lookup"><span data-stu-id="ab659-776">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="ab659-777">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ab659-777">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="ab659-778">Включены операции связывания и отмены связи в автономной системе.</span><span class="sxs-lookup"><span data-stu-id="ab659-778">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="ab659-779">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ab659-779">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="ab659-780">Добавлена поддержка ApiVersions, ApiReleases и ApiRevisions.</span><span class="sxs-lookup"><span data-stu-id="ab659-780">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="ab659-781">Добавлена поддержка серверной части ServiceFabric.</span><span class="sxs-lookup"><span data-stu-id="ab659-781">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="ab659-782">Добавлена поддержка средства ведения журнала Application Insights.</span><span class="sxs-lookup"><span data-stu-id="ab659-782">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="ab659-783">Добавлена поддержка для распознавания номера SKU уровня "Базовый" как допустимого номера SKU службы управления API.</span><span class="sxs-lookup"><span data-stu-id="ab659-783">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="ab659-784">Добавлена поддержка установки сертификатов, выданных частным центром сертификации в качестве корневого или обычного ЦС.</span><span class="sxs-lookup"><span data-stu-id="ab659-784">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="ab659-785">Добавлена поддержка для приема пользовательских SSL-сертификатов с помощью KeyVault и нескольких имен узлов прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="ab659-785">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="ab659-786">Добавлена поддержка для удостоверения MSI.</span><span class="sxs-lookup"><span data-stu-id="ab659-786">Added support for MSI identity</span></span>
* <span data-ttu-id="ab659-787">Добавлена поддержка для принятия политик с помощью URL-адреса. Примечание. Указанные ниже командлеты в следующей версии будут отмечены как нерекомендуемые.</span><span class="sxs-lookup"><span data-stu-id="ab659-787">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="ab659-788">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="ab659-788">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="ab659-789">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="ab659-789">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="ab659-790">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="ab659-790">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="ab659-791">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="ab659-791">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="ab659-792">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="ab659-792">AzureRM.Batch</span></span>
* <span data-ttu-id="ab659-793">Выпущен новый командлет Get-AzureBatchPoolNodeCounts.</span><span class="sxs-lookup"><span data-stu-id="ab659-793">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="ab659-794">Выпущен новый командлет Start-AzureBatchComputeNodeServiceLogUpload.</span><span class="sxs-lookup"><span data-stu-id="ab659-794">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="ab659-795">AzureRM.Consumption:</span><span class="sxs-lookup"><span data-stu-id="ab659-795">AzureRM.Consumption</span></span>
* <span data-ttu-id="ab659-796">Добавлены новые параметры Expand, ResourceGroup, InstanceName, InstanceId, Tags и командлет высшего уровня Get-AzureRmConsumptionUsageDetail.</span><span class="sxs-lookup"><span data-stu-id="ab659-796">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="ab659-797">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ab659-797">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="ab659-798">Исправлен пример для Export-AzureRmDataLakeStoreChildItemProperties.</span><span class="sxs-lookup"><span data-stu-id="ab659-798">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="ab659-799">Исправлено исключение параметра NULL при использовании рекурсии в Set-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="ab659-799">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="ab659-800">Исправлены файлы справки для Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl и Remove-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="ab659-800">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="ab659-801">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ab659-801">AzureRM.Network</span></span>
* <span data-ttu-id="ab659-802">Пакет SDK для сети обновлен с предварительной версии 18.0.0 до предварительной версии 19.0.0.</span><span class="sxs-lookup"><span data-stu-id="ab659-802">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="ab659-803">Добавлен командлет для создания конфигурации протокола.</span><span class="sxs-lookup"><span data-stu-id="ab659-803">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="ab659-804">New-AzureRmNetworkWatcherProtocolConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ab659-804">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="ab659-805">Добавлен командлет для добавления нового подключения канала к существующему каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ab659-805">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="ab659-806">Add-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="ab659-806">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="ab659-807">Добавлен командлет для удаления подключения канала к существующему каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ab659-807">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="ab659-808">Remove-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="ab659-808">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="ab659-809">Добавлен командлет для получения подключения канала.</span><span class="sxs-lookup"><span data-stu-id="ab659-809">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="ab659-810">Get-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="ab659-810">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="ab659-811">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ab659-811">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="ab659-812">Исправлена процедура аутентификации сервера с использованием созданных сертификатов (проблема № 5998).</span><span class="sxs-lookup"><span data-stu-id="ab659-812">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ab659-813">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ab659-813">AzureRM.Sql</span></span>
* <span data-ttu-id="ab659-814">Обновлены командлеты аудита, которые теперь позволяют удалять AuditActions или AuditActionGroups.</span><span class="sxs-lookup"><span data-stu-id="ab659-814">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="ab659-815">Исправлена проблема с Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy, при которой установка новой гибкой политики хранения завершалась ошибкой с сообщением "Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span><span class="sxs-lookup"><span data-stu-id="ab659-815">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="ab659-816">Please submit request with the new flexible retention policy" (Настройка политики долгосрочного хранения с помощью хранилища и политики служб восстановления Azure больше не поддерживается. Отправьте запрос с использованием новой гибкой политики хранения).</span><span class="sxs-lookup"><span data-stu-id="ab659-816">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="ab659-817">Обновлены все командлеты, связанные со службой "База данных SQL Azure", с созданием эластичных пулов и обновлением. Теперь используются новые API баз данных с поддержкой свойства номеров SKU для обеспечения масштабируемости и связанных с уровнями возможностей.</span><span class="sxs-lookup"><span data-stu-id="ab659-817">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="ab659-818">Обновлены командлеты, в том числе:</span><span class="sxs-lookup"><span data-stu-id="ab659-818">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="ab659-819">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="ab659-819">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="ab659-820">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool;</span><span class="sxs-lookup"><span data-stu-id="ab659-820">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="ab659-821">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="ab659-821">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="ab659-822">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ab659-822">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="ab659-823">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ab659-823">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="ab659-824">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ab659-824">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="ab659-825">Обновлены параметры для Get-AzureRmTrafficManagerProfile. Теперь при использовании параметра -Name требуется параметр -ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="ab659-825">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
