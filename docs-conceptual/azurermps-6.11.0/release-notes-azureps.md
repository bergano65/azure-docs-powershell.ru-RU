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
# <a name="release-notes"></a><span data-ttu-id="9fa4b-103">Заметки о выпуске</span><span class="sxs-lookup"><span data-stu-id="9fa4b-103">Release notes</span></span>

<span data-ttu-id="9fa4b-104">Здесь приведен список изменений, внесенных в Azure PowerShell в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6110---october-2018"></a><span data-ttu-id="9fa4b-105">6.11.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-105">6.11.0 - October 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="9fa4b-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="9fa4b-106">AzureRM.Profile</span></span>
* <span data-ttu-id="9fa4b-107">Устранена проблема с Get-AzureRmSubscription в CloudShell.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-107">Fix issue with Get-AzureRmSubscription in CloudShell</span></span>
* <span data-ttu-id="9fa4b-108">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-108">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="9fa4b-109">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="9fa4b-109">AzureRM.Backup</span></span>
* <span data-ttu-id="9fa4b-110">Командлеты Azure Backup объявлены нерекомендуемыми.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-110">Deprecated Azure Backup cmdlets.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="9fa4b-111">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="9fa4b-111">AzureRM.Compute</span></span>
* <span data-ttu-id="9fa4b-112">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzureRmVm.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-112">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzureRmVm'</span></span>
* <span data-ttu-id="9fa4b-113">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-113">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="9fa4b-114">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9fa4b-114">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="9fa4b-115">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="9fa4b-115">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="9fa4b-116">Get-AzureRmDataLakeStoreVirtualNetworkRule — позволяет получить или вывести правило виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-116">Get-AzureRmDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="9fa4b-117">Add-AzureRmDataLakeStoreVirtualNetworkRule — позволяет добавить правило виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-117">Add-AzureRmDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="9fa4b-118">Set-AzureRmDataLakeStoreVirtualNetworkRule — позволяет изменить определенное правило виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-118">Set-AzureRmDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="9fa4b-119">Remove-AzureRmDataLakeStoreVirtualNetworkRule — позволяет удалить правило виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-119">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="9fa4b-120">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="9fa4b-120">AzureRM.Network</span></span>
* <span data-ttu-id="9fa4b-121">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-121">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="9fa4b-122">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-122">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="9fa4b-123">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="9fa4b-123">AzureRM.Resources</span></span>
* <span data-ttu-id="9fa4b-124">Мы устранили проблему, из-за которой командлет Get-AzureRMRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), и добавили понятное исключение.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-124">Fix isssue where Get-AzureRMRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="9fa4b-125">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-125">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="6100---october-2018"></a><span data-ttu-id="9fa4b-126">6.10.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-126">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="9fa4b-127">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="9fa4b-127">Azure.Storage</span></span>
* <span data-ttu-id="9fa4b-128">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-128">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="9fa4b-129">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="9fa4b-129">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="9fa4b-130">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="9fa4b-130">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="9fa4b-131">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="9fa4b-131">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="9fa4b-132">Поддержка Get-AzureRmCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-132">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="9fa4b-133">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="9fa4b-133">AzureRM.Compute</span></span>
* <span data-ttu-id="9fa4b-134">Исправлена команда Get-AzureRmVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-134">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="9fa4b-135">Добавлен пример использования SimpleParameterSet в справку командлета New-AzureRmVmss.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-135">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="9fa4b-136">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-136">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="9fa4b-137">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="9fa4b-137">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="9fa4b-138">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-138">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="9fa4b-139">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="9fa4b-139">AzureRM.Network</span></span>
* <span data-ttu-id="9fa4b-140">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-140">Added NetworkProfile functionality.</span></span> <span data-ttu-id="9fa4b-141">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="9fa4b-141">new cmdlets added</span></span>
    - <span data-ttu-id="9fa4b-142">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="9fa4b-142">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="9fa4b-143">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="9fa4b-143">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="9fa4b-144">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="9fa4b-144">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="9fa4b-145">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="9fa4b-145">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="9fa4b-146">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="9fa4b-146">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="9fa4b-147">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="9fa4b-147">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="9fa4b-148">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-148">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="9fa4b-149">Добавлены командлеты: New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-149">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="9fa4b-150">Добавлены командлеты: Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="9fa4b-150">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="9fa4b-151">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="9fa4b-151">AzureRM.RedisCache</span></span>
* <span data-ttu-id="9fa4b-152">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-152">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="9fa4b-153">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-153">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="9fa4b-154">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="9fa4b-154">AzureRM.Resources</span></span>
* <span data-ttu-id="9fa4b-155">Добавлен отсутствующий параметр -Mode в командлет Set-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-155">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="9fa4b-156">Исправлена ошибка командлета Get-AzureRmProviderOperation для операций, когда Origin содержит User.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-156">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="9fa4b-157">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="9fa4b-157">AzureRM.Sql</span></span>
* <span data-ttu-id="9fa4b-158">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-158">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="9fa4b-159">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="9fa4b-159">AzureRM.Storage</span></span>
* <span data-ttu-id="9fa4b-160">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-160">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="9fa4b-161">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="9fa4b-161">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="9fa4b-162">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="9fa4b-162">AzureRM.Websites</span></span>
* <span data-ttu-id="9fa4b-163">Новый командлет Get-AzureRMWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-163">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="9fa4b-164">Новые командлеты New-AzureRMWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-164">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="9fa4b-165">6.9.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-165">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="9fa4b-166">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="9fa4b-166">General</span></span>
* <span data-ttu-id="9fa4b-167">В модуль развертывания AzureRM добавлен командлет AzureRM.SignalR.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-167">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="9fa4b-168">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="9fa4b-168">AzureRM.Profile</span></span>
* <span data-ttu-id="9fa4b-169">Незначительные изменения в общем коде хранилища.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-169">Minor changes to the storage common code</span></span>
* <span data-ttu-id="9fa4b-170">Обновлены файлы справки, в которые добавлены полные типы параметров.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-170">Updated help files to include full parameter types.</span></span>
- <span data-ttu-id="9fa4b-171">В наборе параметров ServicePrincipalCertificateWithSubscriptionId параметр -ServicePrincipal теперь стал необязательным.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-171">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="9fa4b-172">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="9fa4b-172">Azure.Storage</span></span>
* <span data-ttu-id="9fa4b-173">Поддержка создания контекста хранилища с использованием OAuth.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-173">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="9fa4b-174">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="9fa4b-174">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="9fa4b-175">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="9fa4b-175">AzureRM.Cdn</span></span>
* <span data-ttu-id="9fa4b-176">Добавлен номер SKU для расценок на Standard_Microsoft в CDN.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-176">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="9fa4b-177">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="9fa4b-177">AzureRM.Compute</span></span>
* <span data-ttu-id="9fa4b-178">Keyvault и Storage перенесены в общие зависимости.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-178">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="9fa4b-179">Добавлена поддержка большего количества размеров виртуальных машин в командлеты AEM.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-179">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="9fa4b-180">Добавлен параметр PublicIPPrefix в командлет New-AzureRmVmssIpConfig.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-180">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="9fa4b-181">Добавлен параметр ResourceId в командлет Invoke-AzureRmVMRunCommand.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-181">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="9fa4b-182">Добавлен командлет Invoke-AzureRmVmssVMRunCommand.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-182">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="9fa4b-183">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="9fa4b-183">AzureRM.Dns</span></span>
* <span data-ttu-id="9fa4b-184">Добавлена поддержка для псевдонима записи во время создания записи DNS.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-184">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="9fa4b-185">AzureRM.Insights;</span><span class="sxs-lookup"><span data-stu-id="9fa4b-185">AzureRM.Insights</span></span>
* <span data-ttu-id="9fa4b-186">Исправлены проблемы № 6833 и № 7102 (область настроек диагностики).</span><span class="sxs-lookup"><span data-stu-id="9fa4b-186">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="9fa4b-187">Проблемы с именем по умолчанию, например service, во время создания, получения и отображения списка параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-187">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="9fa4b-188">Проблемы при создании параметров диагностики с категориями.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-188">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="9fa4b-189">Добавлено сообщение о том, что не рекомендуется использовать параметры интервалов времени в метриках.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-189">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="9fa4b-190">Параметры интервалов времени по-прежнему принимаются (это не критическое изменение), но они игнорируются в серверной части, потому что действительно только значение PT1M.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-190">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="9fa4b-191">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="9fa4b-191">AzureRM.Network</span></span>
* <span data-ttu-id="9fa4b-192">Изменения командлетов LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9fa4b-192">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="9fa4b-193">LoadBalancerInboundNatPoolConfig: добавлены параметры IdleTimeoutInMinutes, EnableFloatingIp и EnableTcpReset.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-193">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="9fa4b-194">LoadBalancerInboundNatRuleConfig: добавлен параметр EnableTcpReset.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-194">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="9fa4b-195">LoadBalancerRuleConfig: добавлен параметр EnableTcpReset.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-195">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="9fa4b-196">LoadBalancerProbeConfig: добавлена поддержка значения Https для параметра Protocol.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-196">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="9fa4b-197">Добавлены новые команды для нового правила OutboundRule подресурса LoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-197">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="9fa4b-198">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9fa4b-198">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="9fa4b-199">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9fa4b-199">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="9fa4b-200">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9fa4b-200">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="9fa4b-201">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9fa4b-201">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="9fa4b-202">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9fa4b-202">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="9fa4b-203">Добавлено новое свойство HostedWorkloads для PSNetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-203">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="9fa4b-204">Добавлены новые командлеты для функции Брандмауэра Azure через ARM.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-204">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="9fa4b-205">Добавлен командлет Get-AzureRmFirewall.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-205">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="9fa4b-206">Добавлен командлет Set-AzureRmFirewall.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-206">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="9fa4b-207">Добавлен командлет New-AzureRmFirewall.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-207">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="9fa4b-208">Добавлен командлет Remove-AzureRmFirewall.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-208">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="9fa4b-209">Добавлен командлет New-AzureRmFirewallApplicationRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-209">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="9fa4b-210">Добавлен командлет New-AzureRmFirewallApplicationRule.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-210">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="9fa4b-211">Добавлен командлет New-AzureRmFirewallNatRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-211">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="9fa4b-212">Добавлен командлет New-AzureRmFirewallNatRule.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-212">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="9fa4b-213">Добавлен командлет New-AzureRmFirewallNetworkRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-213">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="9fa4b-214">Добавлен командлет New-AzureRmFirewallNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-214">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="9fa4b-215">Добавлена поддержка конфигурации для доверенного корневого сертификата и автомасштабирования в Шлюзе приложений.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-215">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="9fa4b-216">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="9fa4b-216">New Cmdlets added:</span></span>
      - <span data-ttu-id="9fa4b-217">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="9fa4b-217">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="9fa4b-218">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="9fa4b-218">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="9fa4b-219">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="9fa4b-219">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="9fa4b-220">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="9fa4b-220">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="9fa4b-221">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="9fa4b-221">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="9fa4b-222">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="9fa4b-222">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="9fa4b-223">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="9fa4b-223">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="9fa4b-224">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="9fa4b-224">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="9fa4b-225">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="9fa4b-225">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="9fa4b-226">В следующие командлеты добавлен необязательный параметр -TrustedRootCertificate:</span><span class="sxs-lookup"><span data-stu-id="9fa4b-226">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="9fa4b-227">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9fa4b-227">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="9fa4b-228">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9fa4b-228">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="9fa4b-229">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="9fa4b-229">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="9fa4b-230">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="9fa4b-230">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="9fa4b-231">В следующие командлеты добавлен необязательный параметр -AutoscaleConfiguration:</span><span class="sxs-lookup"><span data-stu-id="9fa4b-231">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="9fa4b-232">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9fa4b-232">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="9fa4b-233">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9fa4b-233">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="9fa4b-234">Добавлен командлет для конечной точки интерфейса Get-AzureInterfaceEndpoint.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-234">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="9fa4b-235">Добавлена поддержка нескольких префиксов адресов в подсети.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-235">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="9fa4b-236">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="9fa4b-236">Updated cmdlets:</span></span>
  - <span data-ttu-id="9fa4b-237">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9fa4b-237">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="9fa4b-238">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9fa4b-238">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="9fa4b-239">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9fa4b-239">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="9fa4b-240">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9fa4b-240">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="9fa4b-241">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="9fa4b-241">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="9fa4b-242">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="9fa4b-242">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="9fa4b-243">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="9fa4b-243">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="9fa4b-244">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="9fa4b-244">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="9fa4b-245">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9fa4b-245">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="9fa4b-246">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9fa4b-246">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="9fa4b-247">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9fa4b-247">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="9fa4b-248">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="9fa4b-248">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="9fa4b-249">New-AzureRmNetworkInterfaceIpConfig — Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="9fa4b-249">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="9fa4b-250">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="9fa4b-250">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="9fa4b-251">Add-AzureRmVirtualNetworkGatewayIpConfig;</span><span class="sxs-lookup"><span data-stu-id="9fa4b-251">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="9fa4b-252">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="9fa4b-252">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="9fa4b-253">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="9fa4b-253">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="9fa4b-254">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="9fa4b-254">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="9fa4b-255">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="9fa4b-255">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="9fa4b-256">Добавлены командлеты для делегирования подсети.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-256">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="9fa4b-257">New-AzureRmDelegation — создает делегирование, которое можно добавить к подсети.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-257">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="9fa4b-258">Remove-AzureRmDelegation — принимает подсеть и удаляет указанное имя делегирования из этой подсети.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-258">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="9fa4b-259">Add-AzureRmDelegation — принимает подсеть и добавляет указанное имя службы в качестве делегирования для этой подсети.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-259">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="9fa4b-260">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="9fa4b-260">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="9fa4b-261">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="9fa4b-261">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="9fa4b-262">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="9fa4b-262">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="9fa4b-263">Добавлена поддержка управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-263">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="9fa4b-264">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="9fa4b-264">AzureRM.RedisCache</span></span>
* <span data-ttu-id="9fa4b-265">Обновлена зависимость Insights.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-265">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="9fa4b-266">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="9fa4b-266">AzureRM.Resources</span></span>
* <span data-ttu-id="9fa4b-267">В командлет New-AzureRmResourceGroupDeployment добавлен новый параметр RollbackAction.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-267">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="9fa4b-268">Добавлена поддержка OnErrorDeployment с новым параметром.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-268">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="9fa4b-269">Добавлена поддержка управляемого удостоверения при назначении политик.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-269">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="9fa4b-270">При назначении политики с помощью New-AzureRmPolicyAssignment параметры со значениями по умолчанию больше не требуются.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-270">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="9fa4b-271">Добавлен новый командлет Get-AzureRmPolicyAlias для получения псевдонимов политик.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-271">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="9fa4b-272">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="9fa4b-272">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="9fa4b-273">Устранена проблема № 7161.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-273">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="9fa4b-274">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="9fa4b-274">AzureRM.SignalR</span></span>
* <span data-ttu-id="9fa4b-275">Обновлены номера SKU для Free_F1 и Standard_S1.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-275">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="9fa4b-276">Добавлены поле версии в объект PSSignalRResource и строка подключения в объект PSSignalRKeys.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-276">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="9fa4b-277">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="9fa4b-277">AzureRM.Storage</span></span>
* <span data-ttu-id="9fa4b-278">Добавлена поддержка политики неизменяемости в AzureRm.Storage.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-278">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="9fa4b-279">Remove-AzureRmStorageAccountNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-279">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="9fa4b-280">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9fa4b-280">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="9fa4b-281">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9fa4b-281">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="9fa4b-282">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9fa4b-282">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="9fa4b-283">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9fa4b-283">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="9fa4b-284">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="9fa4b-284">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="9fa4b-285">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="9fa4b-285">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="9fa4b-286">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="9fa4b-286">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="9fa4b-287">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="9fa4b-287">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="9fa4b-288">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="9fa4b-288">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="9fa4b-289">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="9fa4b-289">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="9fa4b-290">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="9fa4b-290">AzureRM.Websites</span></span>
* <span data-ttu-id="9fa4b-291">Добавлены два новых командлета: Get-AzureRmDeletedWebApp и Restore-AzureRmDeletedWebApp.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-291">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="9fa4b-292">New-AzureRmAppServicePlan: добавлен параметр -HyperV для создания плана службы приложений с контейнером Windows.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-292">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="9fa4b-293">New-AzureRmWebApp, New-AzureRmWebAppSlot, Set-AzureRmWebApp, Set-AzureRmWebAppSlot: добавлены новые параметры (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) для создания контейнера приложения Windows и управления им.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-293">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="9fa4b-294">6.8.1 — август 2018 г.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-294">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="9fa4b-295">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="9fa4b-295">General</span></span>
* <span data-ttu-id="9fa4b-296">Исправлена проблема с отсутствием настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-296">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="9fa4b-297">Обновлены общие сборки среды выполнения</span><span class="sxs-lookup"><span data-stu-id="9fa4b-297">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="9fa4b-298">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="9fa4b-298">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="9fa4b-299">Исправлена проблема с отсутствием настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-299">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="9fa4b-300">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6603.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-300">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="9fa4b-301">Командлеты Import-AzureRmApiManagementApi и \*-AzureRmApiManagementCertificate теперь обрабатывают относительные пути.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-301">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="9fa4b-302">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6879.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-302">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="9fa4b-303">CertificateInformation — это задаваемое свойство, обеспечивающее правильную работу командлета Set-AzureRmApiManagement.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-303">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="9fa4b-304">Проблема исправлена путем обновления пакета NuGet до версии 4.0.4-preview.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-304">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="9fa4b-305">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6853.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-305">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="9fa4b-306">Исправлен фильтр OData для поиска по имени продукта.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-306">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="9fa4b-307">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6814.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-307">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="9fa4b-308">Исправлен фильтр OData для поиска по имени API.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-308">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="9fa4b-309">Добавлена поддержка средства ведения журнала Azure Monitor.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-309">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="9fa4b-310">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="9fa4b-310">AzureRM.Compute</span></span>
* <span data-ttu-id="9fa4b-311">Исправлена проблема с отсутствием в выходных данных ошибки целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-311">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="9fa4b-312">Исправлена проблема с типом учетной записи хранения для виртуальной машины с управляемым диском.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-312">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="9fa4b-313">Исправлена проблема с отсутствием настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-313">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="9fa4b-314">Исправлены командлеты расширения AEM для других сред, например Azure для Китая.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-314">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="9fa4b-315">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="9fa4b-315">AzureRM.Network</span></span>
* <span data-ttu-id="9fa4b-316">Стандартное представление выходных данных командлетов изменено на представление таблиц.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-316">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="9fa4b-317">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="9fa4b-317">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="9fa4b-318">Исправлена проблема с Update-AzureRmPowerBIEmbeddedCapacity при попытке масштабировать приостановленную емкость.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-318">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="9fa4b-319">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="9fa4b-319">AzureRM.Resources</span></span>
* <span data-ttu-id="9fa4b-320">Исправлена проблема с созданием управляемых приложений из Marketplace.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-320">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="9fa4b-321">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="9fa4b-321">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="9fa4b-322">Исправленные проблемы</span><span class="sxs-lookup"><span data-stu-id="9fa4b-322">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="9fa4b-323">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="9fa4b-323">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="9fa4b-324">Добавлена поддержка метода маршрутизации MultiValue.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-324">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="9fa4b-325">Добавлен новый параметр MaxReturn для маршрутизации MultiValue.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-325">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="9fa4b-326">Добавлена поддержка метода маршрутизации Subnet.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-326">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="9fa4b-327">Добавлена поддержка диапазонов IP-адресов (подсетей) в конечных точках.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-327">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="9fa4b-328">Добавлена поддержка пользовательских заголовков в профилях.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-328">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="9fa4b-329">Добавлена поддержка диапазонов кода ожидаемого состояния в профилях.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-329">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="9fa4b-330">Добавлена поддержка пользовательских заголовков в конечных точках.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-330">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="9fa4b-331">6.8.0 — август 2018 г.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-331">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="9fa4b-332">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="9fa4b-332">General</span></span>
* <span data-ttu-id="9fa4b-333">Исправлена проблема с отсутствием настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-333">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="9fa4b-334">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="9fa4b-334">AzureRM.Profile</span></span>
* <span data-ttu-id="9fa4b-335">Добавлено свойство срока действия для маркеров, возвращенных при выполнении Connect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-335">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="9fa4b-336">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="9fa4b-336">AzureRM.Compute</span></span>
* <span data-ttu-id="9fa4b-337">Исправлена проблема с отсутствием в выходных данных ошибки целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-337">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="9fa4b-338">Исправлена проблема с типом учетной записи хранения для виртуальной машины с управляемым диском.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-338">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="9fa4b-339">Исправлены командлеты расширения AEM для других сред, например Azure для Китая.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-339">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="9fa4b-340">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="9fa4b-340">AzureRM.IotHub</span></span>
* <span data-ttu-id="9fa4b-341">Исправлены примеры для New-AzureRmIotHubExportDevices и New-AzureRmIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-341">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="9fa4b-342">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="9fa4b-342">AzureRM.Network</span></span>
* <span data-ttu-id="9fa4b-343">Изменено представление моделей по умолчанию на представление таблиц.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-343">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="9fa4b-344">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="9fa4b-344">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="9fa4b-345">Исправлена проблема с Update-AzureRmPowerBIEmbeddedCapacity при попытке масштабировать приостановленную емкость.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-345">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="9fa4b-346">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="9fa4b-346">AzureRM.Resources</span></span>
* <span data-ttu-id="9fa4b-347">Исправлена проблема с созданием управляемого приложения из marketplace.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-347">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="9fa4b-348">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="9fa4b-348">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="9fa4b-349">Исправления проблем</span><span class="sxs-lookup"><span data-stu-id="9fa4b-349">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="9fa4b-350">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="9fa4b-350">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="9fa4b-351">Добавлена поддержка метода маршрутизации MultiValue.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-351">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="9fa4b-352">Добавлен новый параметр MaxReturn для маршрутизации MultiValue.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-352">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="9fa4b-353">Добавлена поддержка метода маршрутизации Subnet.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-353">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="9fa4b-354">Добавлена поддержка диапазонов IP-адресов (подсетей) в конечных точках.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-354">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="9fa4b-355">Добавлена поддержка пользовательских заголовков в профилях.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-355">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="9fa4b-356">Добавлена поддержка диапазонов кода состояния ожидания в профилях.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-356">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="9fa4b-357">Добавлена поддержка пользовательских заголовков в конечных точках.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-357">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="9fa4b-358">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="9fa4b-358">AzureRM.Websites</span></span>
* <span data-ttu-id="9fa4b-359">Исправлена проблема с отсутствием правильной настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-359">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="9fa4b-360">6.7.0 — август 2018 г.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-360">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="9fa4b-361">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="9fa4b-361">AzureRM.Profile</span></span>
* <span data-ttu-id="9fa4b-362">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-362">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="9fa4b-363">Добавлен идентификатор пользователя для имени контекста по умолчанию, чтобы избежать конфликтов контекста.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-363">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="9fa4b-364">Устранены проблемы с командлетом Clear-AzureRmContext, которые приводили к проблемам с выбором контекста #6398.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-364">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="9fa4b-365">Разрешено передавать домен клиента в параметр -TenantId для командлета Connect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-365">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="9fa4b-366">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="9fa4b-366">Azure.Storage</span></span>
* <span data-ttu-id="9fa4b-367">Удалено ограничение в 5 ТБ для квоты на общую папку Azure.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-367">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="9fa4b-368">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="9fa4b-368">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="9fa4b-369">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="9fa4b-369">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="9fa4b-370">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-370">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="9fa4b-371">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="9fa4b-371">Azure.AnalysisServices</span></span>
* <span data-ttu-id="9fa4b-372">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-372">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="9fa4b-373">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="9fa4b-373">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="9fa4b-374">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-374">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="9fa4b-375">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="9fa4b-375">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="9fa4b-376">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-376">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="9fa4b-377">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="9fa4b-377">AzureRM.Automation</span></span>
* <span data-ttu-id="9fa4b-378">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-378">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="9fa4b-379">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="9fa4b-379">AzureRM.Backup</span></span>
* <span data-ttu-id="9fa4b-380">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-380">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="9fa4b-381">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="9fa4b-381">AzureRM.Batch</span></span>
* <span data-ttu-id="9fa4b-382">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-382">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="9fa4b-383">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="9fa4b-383">AzureRM.Billing</span></span>
* <span data-ttu-id="9fa4b-384">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-384">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="9fa4b-385">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="9fa4b-385">AzureRM.Cdn</span></span>
* <span data-ttu-id="9fa4b-386">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-386">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="9fa4b-387">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="9fa4b-387">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="9fa4b-388">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-388">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="9fa4b-389">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="9fa4b-389">AzureRM.Compute</span></span>
* <span data-ttu-id="9fa4b-390">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-390">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="9fa4b-391">В командлет New-AzureRmVmssConfig добавлен параметр EvictionPolicy.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-391">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="9fa4b-392">Если расположение не указано, используйте в DiskFileParameterSet для New AzureRmVm расположение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-392">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="9fa4b-393">Исправлено описание параметров в Save-AzureRmVMImage.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-393">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="9fa4b-394">Исправлен командлет Get-AzureRmVMDiskEncryptionStatus для определенных сценариев, связанных с однократным выполнением.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-394">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="9fa4b-395">AzureRM.Consumption:</span><span class="sxs-lookup"><span data-stu-id="9fa4b-395">AzureRM.Consumption</span></span>
* <span data-ttu-id="9fa4b-396">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-396">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="9fa4b-397">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="9fa4b-397">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="9fa4b-398">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-398">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="9fa4b-399">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="9fa4b-399">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="9fa4b-400">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-400">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="9fa4b-401">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="9fa4b-401">AzureRM.DataFactories</span></span>
* <span data-ttu-id="9fa4b-402">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-402">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="9fa4b-403">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="9fa4b-403">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="9fa4b-404">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-404">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="9fa4b-405">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="9fa4b-405">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="9fa4b-406">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-406">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="9fa4b-407">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9fa4b-407">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="9fa4b-408">Исправлена отладка, когда DebugPreference настраивается из командной строки PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-408">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="9fa4b-409">Обновлен пример для Set-AzureRmDataLakeStoreItemAcl.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-409">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="9fa4b-410">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-410">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="9fa4b-411">Обновлен пример для Set-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-411">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="9fa4b-412">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="9fa4b-412">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="9fa4b-413">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-413">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="9fa4b-414">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="9fa4b-414">AzureRM.Dns</span></span>
* <span data-ttu-id="9fa4b-415">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-415">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="9fa4b-416">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="9fa4b-416">AzureRM.EventGrid</span></span>
* <span data-ttu-id="9fa4b-417">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-417">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="9fa4b-418">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="9fa4b-418">AzureRM.EventHub</span></span>
* <span data-ttu-id="9fa4b-419">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-419">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="9fa4b-420">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="9fa4b-420">AzureRM.HDInsight</span></span>
* <span data-ttu-id="9fa4b-421">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-421">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="9fa4b-422">AzureRM.Insights;</span><span class="sxs-lookup"><span data-stu-id="9fa4b-422">AzureRM.Insights</span></span>
* <span data-ttu-id="9fa4b-423">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-423">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="9fa4b-424">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="9fa4b-424">AzureRM.IotHub</span></span>
* <span data-ttu-id="9fa4b-425">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-425">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="9fa4b-426">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="9fa4b-426">AzureRM.KeyVault</span></span>
* <span data-ttu-id="9fa4b-427">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-427">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="9fa4b-428">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="9fa4b-428">AzureRM.LogicApp</span></span>
* <span data-ttu-id="9fa4b-429">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-429">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="9fa4b-430">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="9fa4b-430">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="9fa4b-431">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-431">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="9fa4b-432">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="9fa4b-432">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="9fa4b-433">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-433">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="9fa4b-434">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="9fa4b-434">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="9fa4b-435">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-435">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="9fa4b-436">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="9fa4b-436">AzureRM.Media</span></span>
* <span data-ttu-id="9fa4b-437">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-437">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="9fa4b-438">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="9fa4b-438">AzureRM.Network</span></span>
* <span data-ttu-id="9fa4b-439">Добавлен пример для Set-AzureRmLocalNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-439">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="9fa4b-440">Добавлены примеры и описания для Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey и New-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-440">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="9fa4b-441">Добавлены примеры для Remove-AzureRmVirtualNetworkGatewayIpConfig и Reset-AzureRmVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-441">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="9fa4b-442">Добавлен пример для Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-442">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="9fa4b-443">Добавлен пример для Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-443">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="9fa4b-444">Добавлен пример для Set-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-444">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="9fa4b-445">Повторно созданы командлеты для ApplicationSecurityGroup, RouteTable и Usage с помощью генератора кода последней версии.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-445">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="9fa4b-446">Уточнено сообщение об ошибке для Get-AzureRmVirtualNetworkSubnetConfig при попытке получить подсеть, которая не существует.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-446">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="9fa4b-447">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="9fa4b-447">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="9fa4b-448">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-448">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="9fa4b-449">AzureRM.OperationalInsights;</span><span class="sxs-lookup"><span data-stu-id="9fa4b-449">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="9fa4b-450">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-450">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="9fa4b-451">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="9fa4b-451">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="9fa4b-452">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-452">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="9fa4b-453">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="9fa4b-453">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="9fa4b-454">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-454">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="9fa4b-455">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="9fa4b-455">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="9fa4b-456">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-456">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="9fa4b-457">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="9fa4b-457">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="9fa4b-458">Добавлен фильтр политик для командлета Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-458">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="9fa4b-459">Команда возвращает список элементов резервного копирования, защищенных политикой с заданным идентификатором.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-459">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="9fa4b-460">Обновление Microsoft.Azure.Management.RecoveryServices.Backup до версии 3.0.0-preview.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-460">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="9fa4b-461">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-461">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="9fa4b-462">Добавлен параметр TargetResourceGroupName для Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-462">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="9fa4b-463">Группа ресурсов, в которую восстанавливаются управляемые диски.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-463">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="9fa4b-464">Применимо к резервной копии виртуальной машины с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-464">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="9fa4b-465">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="9fa4b-465">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="9fa4b-466">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-466">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="9fa4b-467">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="9fa4b-467">AzureRM.RedisCache</span></span>
* <span data-ttu-id="9fa4b-468">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-468">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="9fa4b-469">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="9fa4b-469">AzureRM.Relay</span></span>
* <span data-ttu-id="9fa4b-470">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-470">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="9fa4b-471">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="9fa4b-471">AzureRM.Resources</span></span>
* <span data-ttu-id="9fa4b-472">Поддержка развертывания шаблонов в области подписки.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-472">Support template deployment at subscription scope.</span></span> <span data-ttu-id="9fa4b-473">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="9fa4b-473">Add new Cmdlets:</span></span>
    - <span data-ttu-id="9fa4b-474">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="9fa4b-474">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="9fa4b-475">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="9fa4b-475">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="9fa4b-476">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="9fa4b-476">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="9fa4b-477">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="9fa4b-477">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="9fa4b-478">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="9fa4b-478">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="9fa4b-479">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="9fa4b-479">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="9fa4b-480">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="9fa4b-480">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="9fa4b-481">Устранена проблема, когда при передаче контекста в Set-AzureRmResource возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-481">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="9fa4b-482">Исправлен пример в New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-482">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="9fa4b-483">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-483">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="9fa4b-484">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="9fa4b-484">AzureRM.Scheduler</span></span>
* <span data-ttu-id="9fa4b-485">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-485">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="9fa4b-486">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="9fa4b-486">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="9fa4b-487">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-487">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="9fa4b-488">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="9fa4b-488">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="9fa4b-489">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-489">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="9fa4b-490">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="9fa4b-490">AzureRM.Sql</span></span>
* <span data-ttu-id="9fa4b-491">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-491">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="9fa4b-492">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="9fa4b-492">AzureRM.Storage</span></span>
* <span data-ttu-id="9fa4b-493">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-493">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="9fa4b-494">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="9fa4b-494">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="9fa4b-495">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-495">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="9fa4b-496">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="9fa4b-496">AzureRM.Tags</span></span>
* <span data-ttu-id="9fa4b-497">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-497">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="9fa4b-498">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="9fa4b-498">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="9fa4b-499">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-499">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="9fa4b-500">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="9fa4b-500">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="9fa4b-501">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-501">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="9fa4b-502">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="9fa4b-502">AzureRM.Websites</span></span>
* <span data-ttu-id="9fa4b-503">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-503">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="9fa4b-504">6.6.0 — июль 2018 г.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-504">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="9fa4b-505">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="9fa4b-505">General</span></span>
* <span data-ttu-id="9fa4b-506">Обновлены все файлы справки: включены полные типы параметров и исправлены типы входных и выходных данных.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-506">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="9fa4b-507">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="9fa4b-507">AzureRM.Profile</span></span>
* <span data-ttu-id="9fa4b-508">Обновлена библиотека Common.Strategy: теперь можно проверить, совместима ли текущая конфигурация ресурса с целевым ресурсом.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-508">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="9fa4b-509">В Common.Storage добавлены типы ps1xml.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-509">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="9fa4b-510">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="9fa4b-510">Azure.Storage</span></span>
* <span data-ttu-id="9fa4b-511">Добавлена поддержка для получения контекста хранилища из DefaultProfile.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-511">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="9fa4b-512">В свойства типов выходных данных командлетов добавлен атрибут Ps1XmlAttribute.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-512">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="9fa4b-513">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="9fa4b-513">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="9fa4b-514">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6370.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-514">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="9fa4b-515">В AutoMapper исправлена ошибка, препятствовавшая преобразованию PsApiManagementApi в ApiContract.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-515">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="9fa4b-516">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6515.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-516">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="9fa4b-517">В File.Save исправлена ошибка, связанная с перегрузкой типом кодировки.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-517">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="9fa4b-518">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6560.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-518">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="9fa4b-519">Выполнено обновление до версии NuGet 4.0.3, что позволило исправить исключение шаблона в apiId.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-519">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="9fa4b-520">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="9fa4b-520">AzureRM.Compute</span></span>
* <span data-ttu-id="9fa4b-521">Устранена ошибка при создании виртуальной машины с помощью командлета New-AzureRmVm и параметра DiskFileParameterSet, которая возникала из-за переименования типа учетной записи хранения PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-521">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="9fa4b-522">Исправлен командлет Invoke-AzureRmVMRunCommand.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-522">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="9fa4b-523">Командлет Get-AzureRmAvailabilitySet теперь может выводить список всех групп доступности в подписке.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-523">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="9fa4b-524">(Параметр ResouceGroupName теперь является необязательным.)</span><span class="sxs-lookup"><span data-stu-id="9fa4b-524">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="9fa4b-525">Обновлен параметр SimpleParameterSet командлета New-AzureRmVm, что позволило использовать ускоренную сеть на соответствующих виртуальных машинах.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-525">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="9fa4b-526">Обновлен простой набор параметров New-AzureRmVmss, что позволило отменять создание масштабируемого набора виртуальных машин, если указанная пользователем подсистема балансировки нагрузки уже существует.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-526">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="9fa4b-527">Обновлен пример для New-AzureRmDisk.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-527">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="9fa4b-528">Добавлен пример для New-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-528">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="9fa4b-529">Обновлено описание командлета Set-AzureRmVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-529">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="9fa4b-530">Обновлен пример 1 для Set-AzureRmVMBginfoExtension: исправлены орфографические ошибки и префикс.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-530">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="9fa4b-531">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="9fa4b-531">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="9fa4b-532">Пакет .NET SDK для ADF обновлен до версии 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-532">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="9fa4b-533">Добавлена поддержка совместного использования локальной среды IR несколькими фабриками данных.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-533">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="9fa4b-534">Добавлен новый параметр -SharedIntegrationRuntimeResourceId для командлета Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-534">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="9fa4b-535">Добавлен новый необязательный параметр -LinkedDataFactoryName для командлета Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-535">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="9fa4b-536">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9fa4b-536">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="9fa4b-537">Пакет SDK для плоскости данных (Microsoft.Azure.DataLake.Store) обновлен до версии 1.1.9.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-537">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="9fa4b-538">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="9fa4b-538">AzureRM.EventHub</span></span>
* <span data-ttu-id="9fa4b-539">Обновлена конвейерная передача для InputObject и ResourceId в командлетах remove.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-539">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="9fa4b-540">AzureRM.Insights;</span><span class="sxs-lookup"><span data-stu-id="9fa4b-540">AzureRM.Insights</span></span>
* <span data-ttu-id="9fa4b-541">Исправлено форматирование OutputType в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-541">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="9fa4b-542">Применен пакет SDK Microsoft.Azure.Management.Monitor 0.19.1-preview.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-542">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="9fa4b-543">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="9fa4b-543">AzureRM.KeyVault</span></span>
* <span data-ttu-id="9fa4b-544">Исправлена проблема с конвейерной передачей в командлете Set-AzureRmKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-544">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="9fa4b-545">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="9fa4b-545">AzureRM.Network</span></span>
* <span data-ttu-id="9fa4b-546">Добавлены примеры для командлетов LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-546">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="9fa4b-547">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="9fa4b-547">AzureRM.Resources</span></span>
* <span data-ttu-id="9fa4b-548">Устранена проблема, возникавшая при указании имени и значения тега для Get-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-548">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="9fa4b-549">Исправлен сценарий конвейерной передачи в Set-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-549">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="9fa4b-550">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="9fa4b-550">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="9fa4b-551">Обновлена конвейерная передача для InputObject и ResourceId в командлетах remove.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-551">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="9fa4b-552">Исправлено несколько ошибок.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-552">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="9fa4b-553">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="9fa4b-553">AzureRM.Sql</span></span>
* <span data-ttu-id="9fa4b-554">Добавлена поддержка Advanced Threat Protection для сервера с помощью следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="9fa4b-554">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="9fa4b-555">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-555">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="9fa4b-556">Добавлена поддержка оценки уязвимостей с помощью следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="9fa4b-556">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="9fa4b-557">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings;</span><span class="sxs-lookup"><span data-stu-id="9fa4b-557">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="9fa4b-558">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline;</span><span class="sxs-lookup"><span data-stu-id="9fa4b-558">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="9fa4b-559">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-559">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="9fa4b-560">Исправлен пример для Remove-AzureRmSqlServerFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-560">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="9fa4b-561">Исправлена неправильная обработка даты и времени для базового языка и региональных параметров, отличных от США, в Get-AzureSqlSyncGroupLog.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-561">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="9fa4b-562">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="9fa4b-562">AzureRM.Storage</span></span>
* <span data-ttu-id="9fa4b-563">В свойства типов выходных данных командлетов добавлен атрибут Ps1XmlAttribute.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-563">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="9fa4b-564">Выходные данные командлетов StorageAccount теперь отображаются в виде таблицы.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-564">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="9fa4b-565">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9fa4b-565">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="9fa4b-566">New-AzureRmStorageAccount;</span><span class="sxs-lookup"><span data-stu-id="9fa4b-566">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="9fa4b-567">Set-AzureRmStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-567">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="9fa4b-568">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="9fa4b-568">AzureRM.Tags</span></span>
* <span data-ttu-id="9fa4b-569">Удалено неверное утверждение из справки по командлетам Tag.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-569">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="9fa4b-570">6.5.0 — июль 2018 г.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-570">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="9fa4b-571">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="9fa4b-571">AzureRM.Profile</span></span>
* <span data-ttu-id="9fa4b-572">Обновлена справка для командлета Get-AzureRmContextAutosaveSetting.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-572">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="9fa4b-573">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="9fa4b-573">Azure.Storage</span></span>
* <span data-ttu-id="9fa4b-574">Добавлена поддержка отправки BLOB-объекта или файла с помощью токена SAS, доступного только для записи.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-574">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="9fa4b-575">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="9fa4b-575">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="9fa4b-576">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="9fa4b-576">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="9fa4b-577">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="9fa4b-577">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="9fa4b-578">Для AS добавлено обязательное свойство ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-578">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="9fa4b-579">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="9fa4b-579">AzureRM.Automation</span></span>
* <span data-ttu-id="9fa4b-580">Обновлена справка и добавлены примеры для командлета New-AzureRMAutomationSchedule.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-580">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="9fa4b-581">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="9fa4b-581">AzureRM.Compute</span></span>
* <span data-ttu-id="9fa4b-582">Добавлен параметр -Tag для командлета Update/New-AzureRmAvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-582">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="9fa4b-583">Добавлен пример для командлета Add-AzureRmVmssExtension.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-583">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="9fa4b-584">Добавлены примеры для командлета Remove-AzureRmVmssExtension.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-584">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="9fa4b-585">Обновлена справка для командлета Set-AzureRmVMAccessExtension.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-585">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="9fa4b-586">Изменен класс SimpleParameterSet для командлета New-AzureRmVmss: теперь для SinglePlacementGroup по умолчанию задается значение false, а также добавляется параметр-переключатель SinglePlacementGroup, который позволяет пользователю создать VMSS в одной группе размещения.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-586">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="9fa4b-587">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="9fa4b-587">AzureRM.EventHub</span></span>
* <span data-ttu-id="9fa4b-588">В класс PSEventHubDRConfigurationAttributes добавлено доступное только для чтения свойство PendingReplicationOperationsCount, которое показывает количество ожидающих репликации операций во время реплицирования.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-588">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="9fa4b-589">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="9fa4b-589">AzureRM.KeyVault</span></span>
* <span data-ttu-id="9fa4b-590">Обновлено сообщение об ошибке для командлета Set-AzureRmKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-590">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="9fa4b-591">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="9fa4b-591">AzureRM.LogicApp</span></span>
* <span data-ttu-id="9fa4b-592">Исправлена ошибка "parameter set could not be resolved" (не удалось разрешить заданный параметр) в командлете New-AzureRmLogicApp.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-592">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="9fa4b-593">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="9fa4b-593">AzureRM.Network</span></span>
* <span data-ttu-id="9fa4b-594">Включен пиринг между виртуальными сетями в нескольких клиентах для командлета Set/Add-AzureRmVirtualNetworkPeering.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-594">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="9fa4b-595">Для шлюза приложений обновлены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="9fa4b-595">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="9fa4b-596">New-AzureRmApplicationGateway: добавлены флаг EnableFIPS и поддержка зон.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-596">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="9fa4b-597">New-AzureRmApplicationGatewaySku: добавлены новые номера SKU Standard_v2 и WAF_v2.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-597">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="9fa4b-598">Set-AzureRmApplicationGatewaySku: добавлены новые номера SKU Standard_v2 и WAF_v2.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-598">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="9fa4b-599">Командлеты RouteTable пересозданы в последней версии генератора.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-599">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="9fa4b-600">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="9fa4b-600">AzureRM.Relay</span></span>
* <span data-ttu-id="9fa4b-601">Обновлены файлы Markdown, исправлена проблема с именем параметра в примере.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-601">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="9fa4b-602">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="9fa4b-602">AzureRM.Resources</span></span>
* <span data-ttu-id="9fa4b-603">Обновлены командлеты Roleassignment и roledefinition:</span><span class="sxs-lookup"><span data-stu-id="9fa4b-603">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="9fa4b-604">Удалены лишние вызовы roledefinition, выполняемые в ходе разбиения на страницы.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-604">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="9fa4b-605">Исправлен командлет Get-AzureRmRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-605">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="9fa4b-606">Исправлена работа параметра -ExpandPrincipalGroups.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-606">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="9fa4b-607">Устранена проблема в командлете Get-AzureRmResource, заключающая в том, что в параметре -ResourceType учитывался регистр символов.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-607">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="9fa4b-608">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="9fa4b-608">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="9fa4b-609">Добавлены параметры top и skip для командлетов list.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-609">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="9fa4b-610">Добавлены командлеты для перехода с пространства имен ценовой категории "Стандартный" на пространство ценовой категории "Премиум":</span><span class="sxs-lookup"><span data-stu-id="9fa4b-610">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="9fa4b-611">Start-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="9fa4b-611">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="9fa4b-612">Get-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="9fa4b-612">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="9fa4b-613">Complete-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="9fa4b-613">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="9fa4b-614">Stop-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="9fa4b-614">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="9fa4b-615">Remove-AzureRmServiceBusMigration.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-615">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="9fa4b-616">В класс PSServiceBusDRConfigurationAttributes добавлено доступное только для чтения свойство PendingReplicationOperationsCount, которое показывает количество ожидающих репликации операций во время реплицирования.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-616">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="9fa4b-617">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="9fa4b-617">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="9fa4b-618">Обновлен пример для командлета New-AzureRmServiceFabricCluster.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-618">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="9fa4b-619">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="9fa4b-619">AzureRM.Sql</span></span>
* <span data-ttu-id="9fa4b-620">Добавлены новые командлеты для Management.Sql, позволяющие клиентам добавлять сертификат TDE в экземпляр SQL Server или управляемый экземпляр:</span><span class="sxs-lookup"><span data-stu-id="9fa4b-620">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="9fa4b-621">Add-AzureRmSqlServerTransparentDataEncryptionCertificate;</span><span class="sxs-lookup"><span data-stu-id="9fa4b-621">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="9fa4b-622">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-622">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="9fa4b-623">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="9fa4b-623">AzureRM.Websites</span></span>
* <span data-ttu-id="9fa4b-624">`Set-AzureRmWebApp -AssignIdentity` и `Set-AzureRmWebAppSlot -AssignIdentity` при установленном значении false теперь будут удалять свойство Identity из объекта сайта. Также при этом будет удаляться тег предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-624">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="9fa4b-625">Обновлен пример для `Get-AzureRmWebAppMetrics` и `Get-AzureRmAppServicePlanMetrics`.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-625">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="9fa4b-626">`Set-AzureRmWebApp -PhpVersion` теперь поддерживает off как допустимую версию PHP.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-626">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="9fa4b-627">6.4.0 — июль 2018 г.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-627">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="9fa4b-628">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="9fa4b-628">General</span></span>
* <span data-ttu-id="9fa4b-629">Исправлено форматирование OutputType в файлах справки для большинства модулей.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-629">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="9fa4b-630">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="9fa4b-630">AzureRM.Profile</span></span>
* <span data-ttu-id="9fa4b-631">В основные типы выходных данных добавлен атрибут Ps1Xml.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-631">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="9fa4b-632">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="9fa4b-632">AzureRM.Compute</span></span>
* <span data-ttu-id="9fa4b-633">Функция добавления тега IP-адреса для масштабируемого набора виртуальных машин (VMSS)</span><span class="sxs-lookup"><span data-stu-id="9fa4b-633">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="9fa4b-634">Добавлен командлет New-AzureRmVmssIpTagConfig.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-634">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="9fa4b-635">В New-AzureRmVmssIpConfig добавлен параметр IpTag.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-635">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="9fa4b-636">Функция автоматического отката ОС для VMSS</span><span class="sxs-lookup"><span data-stu-id="9fa4b-636">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="9fa4b-637">В New-AzureRmVmssConfig и Update-AzureRmVmss добавлены параметры DisableAutoRollback.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-637">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="9fa4b-638">Функция ведения журнала обновлений ОС для VMSS</span><span class="sxs-lookup"><span data-stu-id="9fa4b-638">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="9fa4b-639">В Get-AzureRmVmss добавлен параметр OSUpgradeHistory.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-639">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="9fa4b-640">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="9fa4b-640">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="9fa4b-641">Добавлена поддержка списков управления доступом к каталогу с использованием следующих команд:</span><span class="sxs-lookup"><span data-stu-id="9fa4b-641">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="9fa4b-642">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry;</span><span class="sxs-lookup"><span data-stu-id="9fa4b-642">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="9fa4b-643">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry;</span><span class="sxs-lookup"><span data-stu-id="9fa4b-643">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="9fa4b-644">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-644">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="9fa4b-645">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9fa4b-645">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="9fa4b-646">Добавлены поддержка отмены выполнения и отслеживание хода выполнения для Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl и Remove-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-646">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="9fa4b-647">Добавлена поддержка отмены выполнения для Export-AzureRmDataLakeStoreChildItemProperties.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-647">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="9fa4b-648">Исправлена очистка сообщений об отладке для командлетов, которые выполняют рекурсивные операции.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-648">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="9fa4b-649">Исправлено расположение тестовых данных для командлетов DataLake.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-649">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="9fa4b-650">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="9fa4b-650">AzureRM.EventHub</span></span>
* <span data-ttu-id="9fa4b-651">Для командлетов вывода списка операций Get-AzureRmEventHub и Get-AzureRmEventHubConsumerGroup добавлен необязательный параметр MaxCount.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-651">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="9fa4b-652">Исправлена проблема с командлетом New-AzureRmEventHub, из-за которой требовалось указать по крайней мере один параметр при создании концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-652">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="9fa4b-653">Добавлен набор параметров по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-653">Provided Default Parameter set.</span></span>
* <span data-ttu-id="9fa4b-654">Для командлета New-AzureRmEventHubKey добавлен необязательный параметр -KeyValue, который позволяет пользователю предоставить значение ключа.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-654">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="9fa4b-655">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="9fa4b-655">AzureRM.KeyVault</span></span>
* <span data-ttu-id="9fa4b-656">Исправлена ошибка, из-за которой при выполнении командлета Get-AzureRmKeyVault с параметром -Tag возвращались все ресурсы.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-656">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="9fa4b-657">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="9fa4b-657">AzureRM.Network</span></span>
* <span data-ttu-id="9fa4b-658">Для параметра шлюзов виртуальной вести, избыточных между зонами, предоставлены новые номера SKU.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-658">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="9fa4b-659">Добавлены новые команды для функции поддержки партнерских API для ExpressRoute, развертываемых с помощью ARM:</span><span class="sxs-lookup"><span data-stu-id="9fa4b-659">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="9fa4b-660">добавлена команда Get-AzureRmExpressRouteCrossConnection;</span><span class="sxs-lookup"><span data-stu-id="9fa4b-660">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="9fa4b-661">добавлена команда Set-AzureRmExpressRouteCrossConnection;</span><span class="sxs-lookup"><span data-stu-id="9fa4b-661">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="9fa4b-662">добавлена команда Add-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="9fa4b-662">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="9fa4b-663">добавлена команда Get-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="9fa4b-663">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="9fa4b-664">добавлена команда Remove-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="9fa4b-664">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="9fa4b-665">добавлена команда Get-AzureRMExpressRouteCrossConnectionArpTable;</span><span class="sxs-lookup"><span data-stu-id="9fa4b-665">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="9fa4b-666">добавлена команда Get-AzureRMExpressRouteCrossConnectionRouteTable;</span><span class="sxs-lookup"><span data-stu-id="9fa4b-666">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="9fa4b-667">добавлена команда Get-AzureRMExpressRouteCrossConnectionRouteTableSummary.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-667">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="9fa4b-668">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="9fa4b-668">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="9fa4b-669">Добавлен командлет Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-669">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="9fa4b-670">Этот командлет принимает идентификатор виртуальной машины и проверяет, защищена ли виртуальная машина с помощью какого-либо хранилища в подписке.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-670">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="9fa4b-671">Если такое хранилище существует, командлет выводит данные о нем.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-671">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="9fa4b-672">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="9fa4b-672">AzureRM.Resources</span></span>
* <span data-ttu-id="9fa4b-673">Обновлены командлеты Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="9fa4b-673">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="9fa4b-674">Добавлена поддержка вывода списка значений параметра -Scope на уровне группы управления.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-674">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="9fa4b-675">Добавлена поддержка для получения отдельных назначений со значениями -Scope на уровне группы управления.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-675">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="9fa4b-676">Для параметра управления добавлены параметры -Effective и -All.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-676">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="9fa4b-677">Обновлены командлеты Get/New/Remove/Set-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-677">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="9fa4b-678">Добавлен параметр -ManagementGroupName для применения операций к заданной группе управления.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-678">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="9fa4b-679">Добавлен параметр -SubscriptionId для применения операций к заданной подписке.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-679">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="9fa4b-680">Обновлены командлеты Get/New/Remove/Set-AzureRmPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-680">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="9fa4b-681">Добавлен параметр -ManagementGroupName для применения операций к заданной группе управления.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-681">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="9fa4b-682">Добавлен параметр -SubscriptionId для применения операций к заданной подписке.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-682">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="9fa4b-683">Добавлена поддержка ссылок на секрет KeyVault в параметрах при использовании TemplateParameterObject в New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-683">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="9fa4b-684">Устранена проблема, из-за которой параметр -EndDate игнорировался в New-AzureRmADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-684">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="9fa4b-685">Устранена проблема, из-за которой в Add-AzureRmADGroupMember использовался неверный URL-адрес для запроса.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-685">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="9fa4b-686">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="9fa4b-686">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="9fa4b-687">Для командлета New-AzureRmServiceBusKey добавлен необязательный параметр -KeyValue, который позволяет пользователю предоставить значение ключа.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-687">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="9fa4b-688">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="9fa4b-688">AzureRM.Sql</span></span>
* <span data-ttu-id="9fa4b-689">В справке по New-AzureRmSqlDatabaseRestorePoint добавлено описание определяемых пользователем точек восстановления для хранилища данных SQL.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-689">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="9fa4b-690">Обновлена документация по параметру -ComputeGeneration, используемого в нескольких командлетах.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-690">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="9fa4b-691">6.3.0 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-691">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="9fa4b-692">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="9fa4b-692">AzureRM.Profile</span></span>
* <span data-ttu-id="9fa4b-693">Обновлены сообщения об ошибках для Enable-AzureRmContextAutoSave.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-693">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="9fa4b-694">Создание контекста для каждой подписки при выполнении Connect-AzureRmAccount без предыдущего контекста.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-694">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="9fa4b-695">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="9fa4b-695">Azure.Storage</span></span>
* <span data-ttu-id="9fa4b-696">В файлы справки добавлены дополнительные сведения о параметре -Permissions.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-696">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="9fa4b-697">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="9fa4b-697">AzureRM.Compute</span></span>
* <span data-ttu-id="9fa4b-698">Get-AzureRmVmDiskEncryptionStatus устраняет проблему, которая наблюдалась на виртуальных машинах без дисков данных.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-698">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="9fa4b-699">Обновлена версия клиентской библиотеки Compute для исправления следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="9fa4b-699">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="9fa4b-700">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="9fa4b-700">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="9fa4b-701">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="9fa4b-701">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="9fa4b-702">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="9fa4b-702">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="9fa4b-703">В следующих командлетах исправлено отображение неправильных значений operation ID и operation status:</span><span class="sxs-lookup"><span data-stu-id="9fa4b-703">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="9fa4b-704">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9fa4b-704">Start-AzureRmVM</span></span>
    - <span data-ttu-id="9fa4b-705">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9fa4b-705">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="9fa4b-706">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9fa4b-706">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="9fa4b-707">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9fa4b-707">Set-AzureRmVM</span></span>
    - <span data-ttu-id="9fa4b-708">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="9fa4b-708">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="9fa4b-709">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9fa4b-709">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="9fa4b-710">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="9fa4b-710">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="9fa4b-711">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="9fa4b-711">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="9fa4b-712">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9fa4b-712">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="9fa4b-713">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9fa4b-713">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="9fa4b-714">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9fa4b-714">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="9fa4b-715">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9fa4b-715">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="9fa4b-716">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="9fa4b-716">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="9fa4b-717">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="9fa4b-717">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="9fa4b-718">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="9fa4b-718">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="9fa4b-719">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="9fa4b-719">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="9fa4b-720">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="9fa4b-720">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="9fa4b-721">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="9fa4b-721">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="9fa4b-722">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9fa4b-722">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="9fa4b-723">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="9fa4b-723">AzureRM.EventGrid</span></span>
* <span data-ttu-id="9fa4b-724">Удалены условия проверки ValidateNotNullOrEmpty для SubjectBeginsWith/SubjectEndsWith в командлете Update-AzureRmEventGridSubscription, что позволяет при необходимости заменять эти параметры пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-724">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="9fa4b-725">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="9fa4b-725">AzureRM.KeyVault</span></span>
* <span data-ttu-id="9fa4b-726">Исправлена ошибка, когда при выполнении командлета Get-AzureRmKeyVault -Tag не возвращается ни один тег.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-726">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="9fa4b-727">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="9fa4b-727">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="9fa4b-728">Общедоступный выпуск командлетов Policy Insights.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-728">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="9fa4b-729">Используется API версии 2018-04-04.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-729">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="9fa4b-730">К результатам Get-AzureRmPolicyStateSummary добавлено PolicyDefinitionReferenceId.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-730">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="9fa4b-731">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="9fa4b-731">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="9fa4b-732">Для командлетов RecoveryServices.Backup добавлен параметр -Vault.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-732">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="9fa4b-733">Передача этого параметра переопределяет командлет Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-733">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="9fa4b-734">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="9fa4b-734">AzureRM.Sql</span></span>
* <span data-ttu-id="9fa4b-735">В файле справки обновлен пример для командлета Get-AzureRmSqlDatabaseExpanded.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-735">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="9fa4b-736">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="9fa4b-736">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="9fa4b-737">Обновлен файл справки для командлета Add-AzureRmTrafficManagerEndpointConfig.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-737">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="9fa4b-738">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="9fa4b-738">AzureRM.Websites</span></span>
* <span data-ttu-id="9fa4b-739">Изменено действие командлета Set-AzureRmWebApp. Теперь он не перезаписывает AppSettings, если используется параметр -AssignIdentity.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-739">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="9fa4b-740">Командлет New-AzureRmWebAppSlot теперь учитывает дополнительный параметр AppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-740">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="9fa4b-741">6.2.1 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-741">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="9fa4b-742">AzureRM.OperationalInsights;</span><span class="sxs-lookup"><span data-stu-id="9fa4b-742">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="9fa4b-743">В обновленной модели PSWorkspace Network может использовать type в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-743">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="9fa4b-744">6.2.0 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-744">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="9fa4b-745">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="9fa4b-745">AzureRM.Profile</span></span>
* <span data-ttu-id="9fa4b-746">Исправлена ошибка с загрузкой Newtonsoft.Json версии 10.0.3 во время импорта модуля.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-746">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="9fa4b-747">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="9fa4b-747">AzureRM.Compute</span></span>
* <span data-ttu-id="9fa4b-748">Функция обновления виртуальных машин VMSS.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-748">VMSS VM Update feature</span></span>
    - <span data-ttu-id="9fa4b-749">Добавлены командлеты Update-AzureRmVmssVM и New-AzureRmVMDataDisk.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-749">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="9fa4b-750">В командлет Add-AzureRmVMDataDisk добавлен параметр VirtualMachineScaleSetVM, который позволяет добавлять диски данных в виртуальные машины VMSS.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-750">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="9fa4b-751">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="9fa4b-751">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="9fa4b-752">Пакет SDK для ADF .NET обновлен до версии 0.8.0-preview. Новая версия содержит такие изменения:</span><span class="sxs-lookup"><span data-stu-id="9fa4b-752">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="9fa4b-753">добавлена операция для настройки репозитория фабрики;</span><span class="sxs-lookup"><span data-stu-id="9fa4b-753">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="9fa4b-754">связанная служба QuickBooks LinkedService теперь предоставляет свойства consumerKey и consumerSecret;</span><span class="sxs-lookup"><span data-stu-id="9fa4b-754">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="9fa4b-755">тип нескольких моделей изменен с SecretBase на Object;</span><span class="sxs-lookup"><span data-stu-id="9fa4b-755">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="9fa4b-756">добавлен триггер событий BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-756">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="9fa4b-757">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="9fa4b-757">AzureRM.KeyVault</span></span>
* <span data-ttu-id="9fa4b-758">В документацию добавлены примеры выходных данных.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-758">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="9fa4b-759">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="9fa4b-759">AzureRM.Network</span></span>
* <span data-ttu-id="9fa4b-760">В командлеты Наблюдателя за сетями добавлены параметры Аналитики трафика.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-760">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="9fa4b-761">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="9fa4b-761">AzureRM.Resources</span></span>
* <span data-ttu-id="9fa4b-762">Исправлена ошибка, когда командлет Get-AzureRmResource возвращает свойство Properties объектов PSResource.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-762">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="9fa4b-763">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="9fa4b-763">AzureRM.Scheduler</span></span>
* <span data-ttu-id="9fa4b-764">Исправлена ошибка, когда обновление ServiceBusQueueJob не задает новые значения для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-764">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="9fa4b-765">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="9fa4b-765">AzureRM.Sql</span></span>
* <span data-ttu-id="9fa4b-766">В перечисленные ниже командлеты добавлен необязательный параметр LicenseType.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-766">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="9fa4b-767">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="9fa4b-767">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="9fa4b-768">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool;</span><span class="sxs-lookup"><span data-stu-id="9fa4b-768">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="9fa4b-769">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="9fa4b-769">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="9fa4b-770">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="9fa4b-770">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="9fa4b-771">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9fa4b-771">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="9fa4b-772">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="9fa4b-772">AzureRM.Websites</span></span>
* <span data-ttu-id="9fa4b-773">Командлет New-AzureRMWebApp теперь использует общие алгоритмы из библиотеки Strategy.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-773">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="9fa4b-774">6.1.0 — май 2018 г.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-774">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="9fa4b-775">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="9fa4b-775">AzureRM.Profile</span></span>
* <span data-ttu-id="9fa4b-776">Устранена проблема с выполнением Clear-AzureRmContext, при которой сохранялся пустой контекст с именем предыдущего контекста по умолчанию, что не позволяло пользователю создать новый контекст со старым именем.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-776">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="9fa4b-777">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="9fa4b-777">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="9fa4b-778">Включены операции связывания и отмены связи в автономной системе.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-778">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="9fa4b-779">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="9fa4b-779">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="9fa4b-780">Добавлена поддержка ApiVersions, ApiReleases и ApiRevisions.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-780">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="9fa4b-781">Добавлена поддержка серверной части ServiceFabric.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-781">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="9fa4b-782">Добавлена поддержка средства ведения журнала Application Insights.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-782">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="9fa4b-783">Добавлена поддержка для распознавания номера SKU уровня "Базовый" как допустимого номера SKU службы управления API.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-783">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="9fa4b-784">Добавлена поддержка установки сертификатов, выданных частным центром сертификации в качестве корневого или обычного ЦС.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-784">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="9fa4b-785">Добавлена поддержка для приема пользовательских SSL-сертификатов с помощью KeyVault и нескольких имен узлов прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-785">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="9fa4b-786">Добавлена поддержка для удостоверения MSI.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-786">Added support for MSI identity</span></span>
* <span data-ttu-id="9fa4b-787">Добавлена поддержка для принятия политик с помощью URL-адреса. Примечание. Указанные ниже командлеты в следующей версии будут отмечены как нерекомендуемые.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-787">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="9fa4b-788">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="9fa4b-788">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="9fa4b-789">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="9fa4b-789">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="9fa4b-790">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="9fa4b-790">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="9fa4b-791">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="9fa4b-791">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="9fa4b-792">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="9fa4b-792">AzureRM.Batch</span></span>
* <span data-ttu-id="9fa4b-793">Выпущен новый командлет Get-AzureBatchPoolNodeCounts.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-793">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="9fa4b-794">Выпущен новый командлет Start-AzureBatchComputeNodeServiceLogUpload.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-794">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="9fa4b-795">AzureRM.Consumption:</span><span class="sxs-lookup"><span data-stu-id="9fa4b-795">AzureRM.Consumption</span></span>
* <span data-ttu-id="9fa4b-796">Добавлены новые параметры Expand, ResourceGroup, InstanceName, InstanceId, Tags и командлет высшего уровня Get-AzureRmConsumptionUsageDetail.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-796">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="9fa4b-797">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9fa4b-797">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="9fa4b-798">Исправлен пример для Export-AzureRmDataLakeStoreChildItemProperties.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-798">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="9fa4b-799">Исправлено исключение параметра NULL при использовании рекурсии в Set-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-799">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="9fa4b-800">Исправлены файлы справки для Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl и Remove-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-800">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="9fa4b-801">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="9fa4b-801">AzureRM.Network</span></span>
* <span data-ttu-id="9fa4b-802">Пакет SDK для сети обновлен с предварительной версии 18.0.0 до предварительной версии 19.0.0.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-802">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="9fa4b-803">Добавлен командлет для создания конфигурации протокола.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-803">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="9fa4b-804">New-AzureRmNetworkWatcherProtocolConfiguration.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-804">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="9fa4b-805">Добавлен командлет для добавления нового подключения канала к существующему каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-805">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="9fa4b-806">Add-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-806">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="9fa4b-807">Добавлен командлет для удаления подключения канала к существующему каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-807">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="9fa4b-808">Remove-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-808">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="9fa4b-809">Добавлен командлет для получения подключения канала.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-809">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="9fa4b-810">Get-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-810">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="9fa4b-811">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="9fa4b-811">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="9fa4b-812">Исправлена процедура аутентификации сервера с использованием созданных сертификатов (проблема № 5998).</span><span class="sxs-lookup"><span data-stu-id="9fa4b-812">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="9fa4b-813">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="9fa4b-813">AzureRM.Sql</span></span>
* <span data-ttu-id="9fa4b-814">Обновлены командлеты аудита, которые теперь позволяют удалять AuditActions или AuditActionGroups.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-814">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="9fa4b-815">Исправлена проблема с Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy, при которой установка новой гибкой политики хранения завершалась ошибкой с сообщением "Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-815">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="9fa4b-816">Please submit request with the new flexible retention policy" (Настройка политики долгосрочного хранения с помощью хранилища и политики служб восстановления Azure больше не поддерживается. Отправьте запрос с использованием новой гибкой политики хранения).</span><span class="sxs-lookup"><span data-stu-id="9fa4b-816">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="9fa4b-817">Обновлены все командлеты, связанные со службой "База данных SQL Azure", с созданием эластичных пулов и обновлением. Теперь используются новые API баз данных с поддержкой свойства номеров SKU для обеспечения масштабируемости и связанных с уровнями возможностей.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-817">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="9fa4b-818">Обновлены командлеты, в том числе:</span><span class="sxs-lookup"><span data-stu-id="9fa4b-818">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="9fa4b-819">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="9fa4b-819">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="9fa4b-820">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool;</span><span class="sxs-lookup"><span data-stu-id="9fa4b-820">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="9fa4b-821">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="9fa4b-821">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="9fa4b-822">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="9fa4b-822">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="9fa4b-823">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9fa4b-823">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="9fa4b-824">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="9fa4b-824">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="9fa4b-825">Обновлены параметры для Get-AzureRmTrafficManagerProfile. Теперь при использовании параметра -Name требуется параметр -ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="9fa4b-825">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
