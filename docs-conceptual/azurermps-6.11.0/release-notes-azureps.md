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
ms.sourcegitcommit: 5f946a535eccca0b3ddf3db8f617b32564a88938
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2018
ms.locfileid: "50001513"
---
# <a name="release-notes"></a><span data-ttu-id="fbc12-103">Заметки о выпуске</span><span class="sxs-lookup"><span data-stu-id="fbc12-103">Release notes</span></span>

<span data-ttu-id="fbc12-104">Здесь приведен список изменений, внесенных в Azure PowerShell в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="fbc12-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6110---october-2018"></a><span data-ttu-id="fbc12-105">6.11.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="fbc12-105">6.11.0 - October 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="fbc12-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="fbc12-106">AzureRM.Profile</span></span>
* <span data-ttu-id="fbc12-107">Устранена проблема с Get-AzureRmSubscription в CloudShell.</span><span class="sxs-lookup"><span data-stu-id="fbc12-107">Fix issue with Get-AzureRmSubscription in CloudShell</span></span>
* <span data-ttu-id="fbc12-108">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-108">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="fbc12-109">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="fbc12-109">AzureRM.Backup</span></span>
* <span data-ttu-id="fbc12-110">Командлеты Azure Backup объявлены нерекомендуемыми.</span><span class="sxs-lookup"><span data-stu-id="fbc12-110">Deprecated Azure Backup cmdlets.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="fbc12-111">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="fbc12-111">AzureRM.Compute</span></span>
* <span data-ttu-id="fbc12-112">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzureRmVm.</span><span class="sxs-lookup"><span data-stu-id="fbc12-112">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzureRmVm'</span></span>
* <span data-ttu-id="fbc12-113">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="fbc12-113">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="fbc12-114">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fbc12-114">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="fbc12-115">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="fbc12-115">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="fbc12-116">Get-AzureRmDataLakeStoreVirtualNetworkRule — позволяет получить или вывести правило виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="fbc12-116">Get-AzureRmDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="fbc12-117">Add-AzureRmDataLakeStoreVirtualNetworkRule — позволяет добавить правило виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="fbc12-117">Add-AzureRmDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="fbc12-118">Set-AzureRmDataLakeStoreVirtualNetworkRule — позволяет изменить определенное правило виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="fbc12-118">Set-AzureRmDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="fbc12-119">Remove-AzureRmDataLakeStoreVirtualNetworkRule — позволяет удалить правило виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="fbc12-119">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="fbc12-120">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="fbc12-120">AzureRM.Network</span></span>
* <span data-ttu-id="fbc12-121">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="fbc12-121">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="fbc12-122">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="fbc12-122">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="fbc12-123">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="fbc12-123">AzureRM.Resources</span></span>
* <span data-ttu-id="fbc12-124">Мы устранили проблему, из-за которой командлет Get-AzureRMRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), и добавили понятное исключение.</span><span class="sxs-lookup"><span data-stu-id="fbc12-124">Fix isssue where Get-AzureRMRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="fbc12-125">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="fbc12-125">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="6100---october-2018"></a><span data-ttu-id="fbc12-126">6.10.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="fbc12-126">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="fbc12-127">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="fbc12-127">Azure.Storage</span></span>
* <span data-ttu-id="fbc12-128">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="fbc12-128">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="fbc12-129">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="fbc12-129">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="fbc12-130">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="fbc12-130">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="fbc12-131">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="fbc12-131">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="fbc12-132">Поддержка Get-AzureRmCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="fbc12-132">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="fbc12-133">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="fbc12-133">AzureRM.Compute</span></span>
* <span data-ttu-id="fbc12-134">Исправлена команда Get-AzureRmVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов.</span><span class="sxs-lookup"><span data-stu-id="fbc12-134">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="fbc12-135">Добавлен пример использования SimpleParameterSet в справку командлета New-AzureRmVmss.</span><span class="sxs-lookup"><span data-stu-id="fbc12-135">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="fbc12-136">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="fbc12-136">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="fbc12-137">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="fbc12-137">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="fbc12-138">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="fbc12-138">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="fbc12-139">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="fbc12-139">AzureRM.Network</span></span>
* <span data-ttu-id="fbc12-140">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="fbc12-140">Added NetworkProfile functionality.</span></span> <span data-ttu-id="fbc12-141">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="fbc12-141">new cmdlets added</span></span>
    - <span data-ttu-id="fbc12-142">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="fbc12-142">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="fbc12-143">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="fbc12-143">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="fbc12-144">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="fbc12-144">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="fbc12-145">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="fbc12-145">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="fbc12-146">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="fbc12-146">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="fbc12-147">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="fbc12-147">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="fbc12-148">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="fbc12-148">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="fbc12-149">Добавлены командлеты: New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap.</span><span class="sxs-lookup"><span data-stu-id="fbc12-149">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="fbc12-150">Добавлены командлеты: Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="fbc12-150">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="fbc12-151">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="fbc12-151">AzureRM.RedisCache</span></span>
* <span data-ttu-id="fbc12-152">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="fbc12-152">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="fbc12-153">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="fbc12-153">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="fbc12-154">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="fbc12-154">AzureRM.Resources</span></span>
* <span data-ttu-id="fbc12-155">Добавлен отсутствующий параметр -Mode в командлет Set-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="fbc12-155">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="fbc12-156">Исправлена ошибка командлета Get-AzureRmProviderOperation для операций, когда Origin содержит User.</span><span class="sxs-lookup"><span data-stu-id="fbc12-156">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="fbc12-157">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="fbc12-157">AzureRM.Sql</span></span>
* <span data-ttu-id="fbc12-158">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="fbc12-158">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="fbc12-159">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="fbc12-159">AzureRM.Storage</span></span>
* <span data-ttu-id="fbc12-160">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="fbc12-160">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="fbc12-161">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="fbc12-161">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="fbc12-162">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="fbc12-162">AzureRM.Websites</span></span>
* <span data-ttu-id="fbc12-163">Новый командлет Get-AzureRMWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера.</span><span class="sxs-lookup"><span data-stu-id="fbc12-163">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="fbc12-164">Новые командлеты New-AzureRMWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows.</span><span class="sxs-lookup"><span data-stu-id="fbc12-164">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="fbc12-165">6.9.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="fbc12-165">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="fbc12-166">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="fbc12-166">General</span></span>
* <span data-ttu-id="fbc12-167">В модуль развертывания AzureRM добавлен командлет AzureRM.SignalR.</span><span class="sxs-lookup"><span data-stu-id="fbc12-167">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="fbc12-168">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="fbc12-168">AzureRM.Profile</span></span>
* <span data-ttu-id="fbc12-169">Незначительные изменения в общем коде хранилища.</span><span class="sxs-lookup"><span data-stu-id="fbc12-169">Minor changes to the storage common code</span></span>
* <span data-ttu-id="fbc12-170">Обновлены файлы справки, в которые добавлены полные типы параметров.</span><span class="sxs-lookup"><span data-stu-id="fbc12-170">Updated help files to include full parameter types.</span></span>
- <span data-ttu-id="fbc12-171">В наборе параметров ServicePrincipalCertificateWithSubscriptionId параметр -ServicePrincipal теперь стал необязательным.</span><span class="sxs-lookup"><span data-stu-id="fbc12-171">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="fbc12-172">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="fbc12-172">Azure.Storage</span></span>
* <span data-ttu-id="fbc12-173">Поддержка создания контекста хранилища с использованием OAuth.</span><span class="sxs-lookup"><span data-stu-id="fbc12-173">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="fbc12-174">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="fbc12-174">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="fbc12-175">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="fbc12-175">AzureRM.Cdn</span></span>
* <span data-ttu-id="fbc12-176">Добавлен номер SKU для расценок на Standard_Microsoft в CDN.</span><span class="sxs-lookup"><span data-stu-id="fbc12-176">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="fbc12-177">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="fbc12-177">AzureRM.Compute</span></span>
* <span data-ttu-id="fbc12-178">Keyvault и Storage перенесены в общие зависимости.</span><span class="sxs-lookup"><span data-stu-id="fbc12-178">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="fbc12-179">Добавлена поддержка большего количества размеров виртуальных машин в командлеты AEM.</span><span class="sxs-lookup"><span data-stu-id="fbc12-179">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="fbc12-180">Добавлен параметр PublicIPPrefix в командлет New-AzureRmVmssIpConfig.</span><span class="sxs-lookup"><span data-stu-id="fbc12-180">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="fbc12-181">Добавлен параметр ResourceId в командлет Invoke-AzureRmVMRunCommand.</span><span class="sxs-lookup"><span data-stu-id="fbc12-181">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="fbc12-182">Добавлен командлет Invoke-AzureRmVmssVMRunCommand.</span><span class="sxs-lookup"><span data-stu-id="fbc12-182">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="fbc12-183">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="fbc12-183">AzureRM.Dns</span></span>
* <span data-ttu-id="fbc12-184">Добавлена поддержка для псевдонима записи во время создания записи DNS.</span><span class="sxs-lookup"><span data-stu-id="fbc12-184">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="fbc12-185">AzureRM.Insights;</span><span class="sxs-lookup"><span data-stu-id="fbc12-185">AzureRM.Insights</span></span>
* <span data-ttu-id="fbc12-186">Исправлены проблемы № 6833 и № 7102 (область настроек диагностики).</span><span class="sxs-lookup"><span data-stu-id="fbc12-186">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="fbc12-187">Проблемы с именем по умолчанию, например service, во время создания, получения и отображения списка параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="fbc12-187">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="fbc12-188">Проблемы при создании параметров диагностики с категориями.</span><span class="sxs-lookup"><span data-stu-id="fbc12-188">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="fbc12-189">Добавлено сообщение о том, что не рекомендуется использовать параметры интервалов времени в метриках.</span><span class="sxs-lookup"><span data-stu-id="fbc12-189">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="fbc12-190">Параметры интервалов времени по-прежнему принимаются (это не критическое изменение), но они игнорируются в серверной части, потому что действительно только значение PT1M.</span><span class="sxs-lookup"><span data-stu-id="fbc12-190">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="fbc12-191">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="fbc12-191">AzureRM.Network</span></span>
* <span data-ttu-id="fbc12-192">Изменения командлетов LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fbc12-192">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="fbc12-193">LoadBalancerInboundNatPoolConfig: добавлены параметры IdleTimeoutInMinutes, EnableFloatingIp и EnableTcpReset.</span><span class="sxs-lookup"><span data-stu-id="fbc12-193">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="fbc12-194">LoadBalancerInboundNatRuleConfig: добавлен параметр EnableTcpReset.</span><span class="sxs-lookup"><span data-stu-id="fbc12-194">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="fbc12-195">LoadBalancerRuleConfig: добавлен параметр EnableTcpReset.</span><span class="sxs-lookup"><span data-stu-id="fbc12-195">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="fbc12-196">LoadBalancerProbeConfig: добавлена поддержка значения Https для параметра Protocol.</span><span class="sxs-lookup"><span data-stu-id="fbc12-196">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="fbc12-197">Добавлены новые команды для нового правила OutboundRule подресурса LoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="fbc12-197">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="fbc12-198">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fbc12-198">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="fbc12-199">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fbc12-199">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="fbc12-200">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fbc12-200">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="fbc12-201">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fbc12-201">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="fbc12-202">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fbc12-202">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="fbc12-203">Добавлено новое свойство HostedWorkloads для PSNetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="fbc12-203">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="fbc12-204">Добавлены новые командлеты для функции Брандмауэра Azure через ARM.</span><span class="sxs-lookup"><span data-stu-id="fbc12-204">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="fbc12-205">Добавлен командлет Get-AzureRmFirewall.</span><span class="sxs-lookup"><span data-stu-id="fbc12-205">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="fbc12-206">Добавлен командлет Set-AzureRmFirewall.</span><span class="sxs-lookup"><span data-stu-id="fbc12-206">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="fbc12-207">Добавлен командлет New-AzureRmFirewall.</span><span class="sxs-lookup"><span data-stu-id="fbc12-207">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="fbc12-208">Добавлен командлет Remove-AzureRmFirewall.</span><span class="sxs-lookup"><span data-stu-id="fbc12-208">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="fbc12-209">Добавлен командлет New-AzureRmFirewallApplicationRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="fbc12-209">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="fbc12-210">Добавлен командлет New-AzureRmFirewallApplicationRule.</span><span class="sxs-lookup"><span data-stu-id="fbc12-210">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="fbc12-211">Добавлен командлет New-AzureRmFirewallNatRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="fbc12-211">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="fbc12-212">Добавлен командлет New-AzureRmFirewallNatRule.</span><span class="sxs-lookup"><span data-stu-id="fbc12-212">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="fbc12-213">Добавлен командлет New-AzureRmFirewallNetworkRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="fbc12-213">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="fbc12-214">Добавлен командлет New-AzureRmFirewallNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="fbc12-214">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="fbc12-215">Добавлена поддержка конфигурации для доверенного корневого сертификата и автомасштабирования в Шлюзе приложений.</span><span class="sxs-lookup"><span data-stu-id="fbc12-215">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="fbc12-216">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="fbc12-216">New Cmdlets added:</span></span>
      - <span data-ttu-id="fbc12-217">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="fbc12-217">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="fbc12-218">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="fbc12-218">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="fbc12-219">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="fbc12-219">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="fbc12-220">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="fbc12-220">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="fbc12-221">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="fbc12-221">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="fbc12-222">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="fbc12-222">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="fbc12-223">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="fbc12-223">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="fbc12-224">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="fbc12-224">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="fbc12-225">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="fbc12-225">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="fbc12-226">В следующие командлеты добавлен необязательный параметр -TrustedRootCertificate:</span><span class="sxs-lookup"><span data-stu-id="fbc12-226">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="fbc12-227">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fbc12-227">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="fbc12-228">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fbc12-228">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="fbc12-229">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="fbc12-229">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="fbc12-230">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="fbc12-230">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="fbc12-231">В следующие командлеты добавлен необязательный параметр -AutoscaleConfiguration:</span><span class="sxs-lookup"><span data-stu-id="fbc12-231">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="fbc12-232">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fbc12-232">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="fbc12-233">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fbc12-233">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="fbc12-234">Добавлен командлет для конечной точки интерфейса Get-AzureInterfaceEndpoint.</span><span class="sxs-lookup"><span data-stu-id="fbc12-234">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="fbc12-235">Добавлена поддержка нескольких префиксов адресов в подсети.</span><span class="sxs-lookup"><span data-stu-id="fbc12-235">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="fbc12-236">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="fbc12-236">Updated cmdlets:</span></span>
  - <span data-ttu-id="fbc12-237">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="fbc12-237">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="fbc12-238">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="fbc12-238">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="fbc12-239">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="fbc12-239">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="fbc12-240">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="fbc12-240">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="fbc12-241">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="fbc12-241">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="fbc12-242">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="fbc12-242">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="fbc12-243">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="fbc12-243">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="fbc12-244">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="fbc12-244">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="fbc12-245">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="fbc12-245">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="fbc12-246">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="fbc12-246">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="fbc12-247">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="fbc12-247">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="fbc12-248">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="fbc12-248">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="fbc12-249">New-AzureRmNetworkInterfaceIpConfig — Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="fbc12-249">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="fbc12-250">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="fbc12-250">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="fbc12-251">Add-AzureRmVirtualNetworkGatewayIpConfig;</span><span class="sxs-lookup"><span data-stu-id="fbc12-251">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="fbc12-252">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="fbc12-252">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="fbc12-253">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="fbc12-253">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="fbc12-254">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="fbc12-254">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="fbc12-255">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="fbc12-255">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="fbc12-256">Добавлены командлеты для делегирования подсети.</span><span class="sxs-lookup"><span data-stu-id="fbc12-256">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="fbc12-257">New-AzureRmDelegation — создает делегирование, которое можно добавить к подсети.</span><span class="sxs-lookup"><span data-stu-id="fbc12-257">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="fbc12-258">Remove-AzureRmDelegation — принимает подсеть и удаляет указанное имя делегирования из этой подсети.</span><span class="sxs-lookup"><span data-stu-id="fbc12-258">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="fbc12-259">Add-AzureRmDelegation — принимает подсеть и добавляет указанное имя службы в качестве делегирования для этой подсети.</span><span class="sxs-lookup"><span data-stu-id="fbc12-259">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="fbc12-260">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="fbc12-260">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="fbc12-261">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="fbc12-261">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="fbc12-262">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="fbc12-262">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="fbc12-263">Добавлена поддержка управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="fbc12-263">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="fbc12-264">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="fbc12-264">AzureRM.RedisCache</span></span>
* <span data-ttu-id="fbc12-265">Обновлена зависимость Insights.</span><span class="sxs-lookup"><span data-stu-id="fbc12-265">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="fbc12-266">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="fbc12-266">AzureRM.Resources</span></span>
* <span data-ttu-id="fbc12-267">В командлет New-AzureRmResourceGroupDeployment добавлен новый параметр RollbackAction.</span><span class="sxs-lookup"><span data-stu-id="fbc12-267">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="fbc12-268">Добавлена поддержка OnErrorDeployment с новым параметром.</span><span class="sxs-lookup"><span data-stu-id="fbc12-268">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="fbc12-269">Добавлена поддержка управляемого удостоверения при назначении политик.</span><span class="sxs-lookup"><span data-stu-id="fbc12-269">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="fbc12-270">При назначении политики с помощью New-AzureRmPolicyAssignment параметры со значениями по умолчанию больше не требуются.</span><span class="sxs-lookup"><span data-stu-id="fbc12-270">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="fbc12-271">Добавлен новый командлет Get-AzureRmPolicyAlias для получения псевдонимов политик.</span><span class="sxs-lookup"><span data-stu-id="fbc12-271">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="fbc12-272">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="fbc12-272">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="fbc12-273">Устранена проблема № 7161.</span><span class="sxs-lookup"><span data-stu-id="fbc12-273">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="fbc12-274">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="fbc12-274">AzureRM.SignalR</span></span>
* <span data-ttu-id="fbc12-275">Обновлены номера SKU для Free_F1 и Standard_S1.</span><span class="sxs-lookup"><span data-stu-id="fbc12-275">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="fbc12-276">Добавлены поле версии в объект PSSignalRResource и строка подключения в объект PSSignalRKeys.</span><span class="sxs-lookup"><span data-stu-id="fbc12-276">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="fbc12-277">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="fbc12-277">AzureRM.Storage</span></span>
* <span data-ttu-id="fbc12-278">Добавлена поддержка политики неизменяемости в AzureRm.Storage.</span><span class="sxs-lookup"><span data-stu-id="fbc12-278">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="fbc12-279">Remove-AzureRmStorageAccountNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="fbc12-279">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="fbc12-280">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="fbc12-280">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="fbc12-281">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="fbc12-281">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="fbc12-282">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="fbc12-282">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="fbc12-283">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="fbc12-283">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="fbc12-284">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="fbc12-284">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="fbc12-285">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="fbc12-285">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="fbc12-286">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="fbc12-286">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="fbc12-287">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="fbc12-287">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="fbc12-288">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="fbc12-288">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="fbc12-289">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="fbc12-289">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="fbc12-290">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="fbc12-290">AzureRM.Websites</span></span>
* <span data-ttu-id="fbc12-291">Добавлены два новых командлета: Get-AzureRmDeletedWebApp и Restore-AzureRmDeletedWebApp.</span><span class="sxs-lookup"><span data-stu-id="fbc12-291">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="fbc12-292">New-AzureRmAppServicePlan: добавлен параметр -HyperV для создания плана службы приложений с контейнером Windows.</span><span class="sxs-lookup"><span data-stu-id="fbc12-292">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="fbc12-293">New-AzureRmWebApp, New-AzureRmWebAppSlot, Set-AzureRmWebApp, Set-AzureRmWebAppSlot: добавлены новые параметры (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) для создания контейнера приложения Windows и управления им.</span><span class="sxs-lookup"><span data-stu-id="fbc12-293">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="fbc12-294">6.8.1 — август 2018 г.</span><span class="sxs-lookup"><span data-stu-id="fbc12-294">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="fbc12-295">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="fbc12-295">General</span></span>
* <span data-ttu-id="fbc12-296">Исправлена проблема с отсутствием настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fbc12-296">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="fbc12-297">Обновлены общие сборки среды выполнения</span><span class="sxs-lookup"><span data-stu-id="fbc12-297">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="fbc12-298">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fbc12-298">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="fbc12-299">Исправлена проблема с отсутствием настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fbc12-299">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="fbc12-300">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6603.</span><span class="sxs-lookup"><span data-stu-id="fbc12-300">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="fbc12-301">Командлеты Import-AzureRmApiManagementApi и \*-AzureRmApiManagementCertificate теперь обрабатывают относительные пути.</span><span class="sxs-lookup"><span data-stu-id="fbc12-301">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="fbc12-302">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6879.</span><span class="sxs-lookup"><span data-stu-id="fbc12-302">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="fbc12-303">CertificateInformation — это задаваемое свойство, обеспечивающее правильную работу командлета Set-AzureRmApiManagement.</span><span class="sxs-lookup"><span data-stu-id="fbc12-303">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="fbc12-304">Проблема исправлена путем обновления пакета NuGet до версии 4.0.4-preview.</span><span class="sxs-lookup"><span data-stu-id="fbc12-304">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="fbc12-305">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6853.</span><span class="sxs-lookup"><span data-stu-id="fbc12-305">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="fbc12-306">Исправлен фильтр OData для поиска по имени продукта.</span><span class="sxs-lookup"><span data-stu-id="fbc12-306">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="fbc12-307">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6814.</span><span class="sxs-lookup"><span data-stu-id="fbc12-307">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="fbc12-308">Исправлен фильтр OData для поиска по имени API.</span><span class="sxs-lookup"><span data-stu-id="fbc12-308">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="fbc12-309">Добавлена поддержка средства ведения журнала Azure Monitor.</span><span class="sxs-lookup"><span data-stu-id="fbc12-309">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="fbc12-310">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="fbc12-310">AzureRM.Compute</span></span>
* <span data-ttu-id="fbc12-311">Исправлена проблема с отсутствием в выходных данных ошибки целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="fbc12-311">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="fbc12-312">Исправлена проблема с типом учетной записи хранения для виртуальной машины с управляемым диском.</span><span class="sxs-lookup"><span data-stu-id="fbc12-312">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="fbc12-313">Исправлена проблема с отсутствием настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fbc12-313">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="fbc12-314">Исправлены командлеты расширения AEM для других сред, например Azure для Китая.</span><span class="sxs-lookup"><span data-stu-id="fbc12-314">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="fbc12-315">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="fbc12-315">AzureRM.Network</span></span>
* <span data-ttu-id="fbc12-316">Стандартное представление выходных данных командлетов изменено на представление таблиц.</span><span class="sxs-lookup"><span data-stu-id="fbc12-316">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="fbc12-317">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="fbc12-317">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="fbc12-318">Исправлена проблема с Update-AzureRmPowerBIEmbeddedCapacity при попытке масштабировать приостановленную емкость.</span><span class="sxs-lookup"><span data-stu-id="fbc12-318">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="fbc12-319">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="fbc12-319">AzureRM.Resources</span></span>
* <span data-ttu-id="fbc12-320">Исправлена проблема с созданием управляемых приложений из Marketplace.</span><span class="sxs-lookup"><span data-stu-id="fbc12-320">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="fbc12-321">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="fbc12-321">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="fbc12-322">Исправленные проблемы</span><span class="sxs-lookup"><span data-stu-id="fbc12-322">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="fbc12-323">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="fbc12-323">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="fbc12-324">Добавлена поддержка метода маршрутизации MultiValue.</span><span class="sxs-lookup"><span data-stu-id="fbc12-324">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="fbc12-325">Добавлен новый параметр MaxReturn для маршрутизации MultiValue.</span><span class="sxs-lookup"><span data-stu-id="fbc12-325">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="fbc12-326">Добавлена поддержка метода маршрутизации Subnet.</span><span class="sxs-lookup"><span data-stu-id="fbc12-326">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="fbc12-327">Добавлена поддержка диапазонов IP-адресов (подсетей) в конечных точках.</span><span class="sxs-lookup"><span data-stu-id="fbc12-327">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="fbc12-328">Добавлена поддержка пользовательских заголовков в профилях.</span><span class="sxs-lookup"><span data-stu-id="fbc12-328">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="fbc12-329">Добавлена поддержка диапазонов кода ожидаемого состояния в профилях.</span><span class="sxs-lookup"><span data-stu-id="fbc12-329">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="fbc12-330">Добавлена поддержка пользовательских заголовков в конечных точках.</span><span class="sxs-lookup"><span data-stu-id="fbc12-330">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="fbc12-331">6.8.0 — август 2018 г.</span><span class="sxs-lookup"><span data-stu-id="fbc12-331">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="fbc12-332">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="fbc12-332">General</span></span>
* <span data-ttu-id="fbc12-333">Исправлена проблема с отсутствием настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fbc12-333">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="fbc12-334">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="fbc12-334">AzureRM.Profile</span></span>
* <span data-ttu-id="fbc12-335">Добавлено свойство срока действия для маркеров, возвращенных при выполнении Connect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="fbc12-335">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="fbc12-336">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="fbc12-336">AzureRM.Compute</span></span>
* <span data-ttu-id="fbc12-337">Исправлена проблема с отсутствием в выходных данных ошибки целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="fbc12-337">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="fbc12-338">Исправлена проблема с типом учетной записи хранения для виртуальной машины с управляемым диском.</span><span class="sxs-lookup"><span data-stu-id="fbc12-338">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="fbc12-339">Исправлены командлеты расширения AEM для других сред, например Azure для Китая.</span><span class="sxs-lookup"><span data-stu-id="fbc12-339">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="fbc12-340">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="fbc12-340">AzureRM.IotHub</span></span>
* <span data-ttu-id="fbc12-341">Исправлены примеры для New-AzureRmIotHubExportDevices и New-AzureRmIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="fbc12-341">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="fbc12-342">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="fbc12-342">AzureRM.Network</span></span>
* <span data-ttu-id="fbc12-343">Изменено представление моделей по умолчанию на представление таблиц.</span><span class="sxs-lookup"><span data-stu-id="fbc12-343">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="fbc12-344">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="fbc12-344">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="fbc12-345">Исправлена проблема с Update-AzureRmPowerBIEmbeddedCapacity при попытке масштабировать приостановленную емкость.</span><span class="sxs-lookup"><span data-stu-id="fbc12-345">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="fbc12-346">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="fbc12-346">AzureRM.Resources</span></span>
* <span data-ttu-id="fbc12-347">Исправлена проблема с созданием управляемого приложения из marketplace.</span><span class="sxs-lookup"><span data-stu-id="fbc12-347">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="fbc12-348">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="fbc12-348">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="fbc12-349">Исправления проблем</span><span class="sxs-lookup"><span data-stu-id="fbc12-349">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="fbc12-350">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="fbc12-350">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="fbc12-351">Добавлена поддержка метода маршрутизации MultiValue.</span><span class="sxs-lookup"><span data-stu-id="fbc12-351">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="fbc12-352">Добавлен новый параметр MaxReturn для маршрутизации MultiValue.</span><span class="sxs-lookup"><span data-stu-id="fbc12-352">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="fbc12-353">Добавлена поддержка метода маршрутизации Subnet.</span><span class="sxs-lookup"><span data-stu-id="fbc12-353">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="fbc12-354">Добавлена поддержка диапазонов IP-адресов (подсетей) в конечных точках.</span><span class="sxs-lookup"><span data-stu-id="fbc12-354">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="fbc12-355">Добавлена поддержка пользовательских заголовков в профилях.</span><span class="sxs-lookup"><span data-stu-id="fbc12-355">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="fbc12-356">Добавлена поддержка диапазонов кода состояния ожидания в профилях.</span><span class="sxs-lookup"><span data-stu-id="fbc12-356">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="fbc12-357">Добавлена поддержка пользовательских заголовков в конечных точках.</span><span class="sxs-lookup"><span data-stu-id="fbc12-357">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="fbc12-358">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="fbc12-358">AzureRM.Websites</span></span>
* <span data-ttu-id="fbc12-359">Исправлена проблема с отсутствием правильной настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fbc12-359">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="fbc12-360">6.7.0 — август 2018 г.</span><span class="sxs-lookup"><span data-stu-id="fbc12-360">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="fbc12-361">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="fbc12-361">AzureRM.Profile</span></span>
* <span data-ttu-id="fbc12-362">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-362">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="fbc12-363">Добавлен идентификатор пользователя для имени контекста по умолчанию, чтобы избежать конфликтов контекста.</span><span class="sxs-lookup"><span data-stu-id="fbc12-363">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="fbc12-364">Устранены проблемы с командлетом Clear-AzureRmContext, которые приводили к проблемам с выбором контекста #6398.</span><span class="sxs-lookup"><span data-stu-id="fbc12-364">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="fbc12-365">Разрешено передавать домен клиента в параметр -TenantId для командлета Connect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="fbc12-365">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="fbc12-366">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="fbc12-366">Azure.Storage</span></span>
* <span data-ttu-id="fbc12-367">Удалено ограничение в 5 ТБ для квоты на общую папку Azure.</span><span class="sxs-lookup"><span data-stu-id="fbc12-367">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="fbc12-368">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="fbc12-368">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="fbc12-369">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="fbc12-369">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="fbc12-370">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-370">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="fbc12-371">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="fbc12-371">Azure.AnalysisServices</span></span>
* <span data-ttu-id="fbc12-372">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-372">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="fbc12-373">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fbc12-373">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="fbc12-374">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-374">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="fbc12-375">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="fbc12-375">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="fbc12-376">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-376">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="fbc12-377">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="fbc12-377">AzureRM.Automation</span></span>
* <span data-ttu-id="fbc12-378">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-378">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="fbc12-379">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="fbc12-379">AzureRM.Backup</span></span>
* <span data-ttu-id="fbc12-380">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-380">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="fbc12-381">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="fbc12-381">AzureRM.Batch</span></span>
* <span data-ttu-id="fbc12-382">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-382">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="fbc12-383">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="fbc12-383">AzureRM.Billing</span></span>
* <span data-ttu-id="fbc12-384">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-384">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="fbc12-385">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="fbc12-385">AzureRM.Cdn</span></span>
* <span data-ttu-id="fbc12-386">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-386">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="fbc12-387">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="fbc12-387">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="fbc12-388">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-388">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="fbc12-389">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="fbc12-389">AzureRM.Compute</span></span>
* <span data-ttu-id="fbc12-390">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-390">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="fbc12-391">В командлет New-AzureRmVmssConfig добавлен параметр EvictionPolicy.</span><span class="sxs-lookup"><span data-stu-id="fbc12-391">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="fbc12-392">Если расположение не указано, используйте в DiskFileParameterSet для New AzureRmVm расположение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fbc12-392">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="fbc12-393">Исправлено описание параметров в Save-AzureRmVMImage.</span><span class="sxs-lookup"><span data-stu-id="fbc12-393">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="fbc12-394">Исправлен командлет Get-AzureRmVMDiskEncryptionStatus для определенных сценариев, связанных с однократным выполнением.</span><span class="sxs-lookup"><span data-stu-id="fbc12-394">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="fbc12-395">AzureRM.Consumption:</span><span class="sxs-lookup"><span data-stu-id="fbc12-395">AzureRM.Consumption</span></span>
* <span data-ttu-id="fbc12-396">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-396">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="fbc12-397">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="fbc12-397">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="fbc12-398">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-398">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="fbc12-399">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fbc12-399">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="fbc12-400">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-400">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="fbc12-401">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="fbc12-401">AzureRM.DataFactories</span></span>
* <span data-ttu-id="fbc12-402">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-402">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="fbc12-403">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="fbc12-403">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="fbc12-404">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-404">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="fbc12-405">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="fbc12-405">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="fbc12-406">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-406">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="fbc12-407">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fbc12-407">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="fbc12-408">Исправлена отладка, когда DebugPreference настраивается из командной строки PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fbc12-408">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="fbc12-409">Обновлен пример для Set-AzureRmDataLakeStoreItemAcl.</span><span class="sxs-lookup"><span data-stu-id="fbc12-409">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="fbc12-410">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-410">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="fbc12-411">Обновлен пример для Set-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="fbc12-411">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="fbc12-412">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="fbc12-412">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="fbc12-413">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-413">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="fbc12-414">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="fbc12-414">AzureRM.Dns</span></span>
* <span data-ttu-id="fbc12-415">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-415">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="fbc12-416">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="fbc12-416">AzureRM.EventGrid</span></span>
* <span data-ttu-id="fbc12-417">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-417">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="fbc12-418">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="fbc12-418">AzureRM.EventHub</span></span>
* <span data-ttu-id="fbc12-419">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-419">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="fbc12-420">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="fbc12-420">AzureRM.HDInsight</span></span>
* <span data-ttu-id="fbc12-421">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-421">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="fbc12-422">AzureRM.Insights;</span><span class="sxs-lookup"><span data-stu-id="fbc12-422">AzureRM.Insights</span></span>
* <span data-ttu-id="fbc12-423">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-423">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="fbc12-424">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="fbc12-424">AzureRM.IotHub</span></span>
* <span data-ttu-id="fbc12-425">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-425">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="fbc12-426">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fbc12-426">AzureRM.KeyVault</span></span>
* <span data-ttu-id="fbc12-427">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-427">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="fbc12-428">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="fbc12-428">AzureRM.LogicApp</span></span>
* <span data-ttu-id="fbc12-429">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-429">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="fbc12-430">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="fbc12-430">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="fbc12-431">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-431">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="fbc12-432">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="fbc12-432">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="fbc12-433">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-433">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="fbc12-434">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="fbc12-434">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="fbc12-435">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-435">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="fbc12-436">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="fbc12-436">AzureRM.Media</span></span>
* <span data-ttu-id="fbc12-437">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-437">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="fbc12-438">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="fbc12-438">AzureRM.Network</span></span>
* <span data-ttu-id="fbc12-439">Добавлен пример для Set-AzureRmLocalNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="fbc12-439">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="fbc12-440">Добавлены примеры и описания для Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey и New-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="fbc12-440">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="fbc12-441">Добавлены примеры для Remove-AzureRmVirtualNetworkGatewayIpConfig и Reset-AzureRmVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="fbc12-441">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="fbc12-442">Добавлен пример для Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.</span><span class="sxs-lookup"><span data-stu-id="fbc12-442">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="fbc12-443">Добавлен пример для Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.</span><span class="sxs-lookup"><span data-stu-id="fbc12-443">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="fbc12-444">Добавлен пример для Set-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="fbc12-444">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="fbc12-445">Повторно созданы командлеты для ApplicationSecurityGroup, RouteTable и Usage с помощью генератора кода последней версии.</span><span class="sxs-lookup"><span data-stu-id="fbc12-445">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="fbc12-446">Уточнено сообщение об ошибке для Get-AzureRmVirtualNetworkSubnetConfig при попытке получить подсеть, которая не существует.</span><span class="sxs-lookup"><span data-stu-id="fbc12-446">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="fbc12-447">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="fbc12-447">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="fbc12-448">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-448">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="fbc12-449">AzureRM.OperationalInsights;</span><span class="sxs-lookup"><span data-stu-id="fbc12-449">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="fbc12-450">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-450">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="fbc12-451">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="fbc12-451">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="fbc12-452">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-452">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="fbc12-453">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="fbc12-453">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="fbc12-454">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-454">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="fbc12-455">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fbc12-455">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="fbc12-456">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-456">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="fbc12-457">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="fbc12-457">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="fbc12-458">Добавлен фильтр политик для командлета Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="fbc12-458">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="fbc12-459">Команда возвращает список элементов резервного копирования, защищенных политикой с заданным идентификатором.</span><span class="sxs-lookup"><span data-stu-id="fbc12-459">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="fbc12-460">Обновление Microsoft.Azure.Management.RecoveryServices.Backup до версии 3.0.0-preview.</span><span class="sxs-lookup"><span data-stu-id="fbc12-460">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="fbc12-461">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-461">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="fbc12-462">Добавлен параметр TargetResourceGroupName для Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="fbc12-462">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="fbc12-463">Группа ресурсов, в которую восстанавливаются управляемые диски.</span><span class="sxs-lookup"><span data-stu-id="fbc12-463">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="fbc12-464">Применимо к резервной копии виртуальной машины с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="fbc12-464">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="fbc12-465">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="fbc12-465">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="fbc12-466">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-466">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="fbc12-467">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="fbc12-467">AzureRM.RedisCache</span></span>
* <span data-ttu-id="fbc12-468">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-468">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="fbc12-469">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="fbc12-469">AzureRM.Relay</span></span>
* <span data-ttu-id="fbc12-470">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-470">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="fbc12-471">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="fbc12-471">AzureRM.Resources</span></span>
* <span data-ttu-id="fbc12-472">Поддержка развертывания шаблонов в области подписки.</span><span class="sxs-lookup"><span data-stu-id="fbc12-472">Support template deployment at subscription scope.</span></span> <span data-ttu-id="fbc12-473">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="fbc12-473">Add new Cmdlets:</span></span>
    - <span data-ttu-id="fbc12-474">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="fbc12-474">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="fbc12-475">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="fbc12-475">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="fbc12-476">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="fbc12-476">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="fbc12-477">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="fbc12-477">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="fbc12-478">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="fbc12-478">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="fbc12-479">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="fbc12-479">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="fbc12-480">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="fbc12-480">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="fbc12-481">Устранена проблема, когда при передаче контекста в Set-AzureRmResource возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="fbc12-481">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="fbc12-482">Исправлен пример в New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="fbc12-482">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="fbc12-483">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-483">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="fbc12-484">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="fbc12-484">AzureRM.Scheduler</span></span>
* <span data-ttu-id="fbc12-485">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-485">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="fbc12-486">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="fbc12-486">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="fbc12-487">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-487">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="fbc12-488">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fbc12-488">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="fbc12-489">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-489">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="fbc12-490">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="fbc12-490">AzureRM.Sql</span></span>
* <span data-ttu-id="fbc12-491">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-491">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="fbc12-492">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="fbc12-492">AzureRM.Storage</span></span>
* <span data-ttu-id="fbc12-493">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-493">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="fbc12-494">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="fbc12-494">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="fbc12-495">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-495">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="fbc12-496">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="fbc12-496">AzureRM.Tags</span></span>
* <span data-ttu-id="fbc12-497">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-497">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="fbc12-498">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="fbc12-498">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="fbc12-499">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-499">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="fbc12-500">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="fbc12-500">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="fbc12-501">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-501">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="fbc12-502">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="fbc12-502">AzureRM.Websites</span></span>
* <span data-ttu-id="fbc12-503">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-503">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="fbc12-504">6.6.0 — июль 2018 г.</span><span class="sxs-lookup"><span data-stu-id="fbc12-504">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="fbc12-505">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="fbc12-505">General</span></span>
* <span data-ttu-id="fbc12-506">Обновлены все файлы справки: включены полные типы параметров и исправлены типы входных и выходных данных.</span><span class="sxs-lookup"><span data-stu-id="fbc12-506">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="fbc12-507">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="fbc12-507">AzureRM.Profile</span></span>
* <span data-ttu-id="fbc12-508">Обновлена библиотека Common.Strategy: теперь можно проверить, совместима ли текущая конфигурация ресурса с целевым ресурсом.</span><span class="sxs-lookup"><span data-stu-id="fbc12-508">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="fbc12-509">В Common.Storage добавлены типы ps1xml.</span><span class="sxs-lookup"><span data-stu-id="fbc12-509">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="fbc12-510">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="fbc12-510">Azure.Storage</span></span>
* <span data-ttu-id="fbc12-511">Добавлена поддержка для получения контекста хранилища из DefaultProfile.</span><span class="sxs-lookup"><span data-stu-id="fbc12-511">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="fbc12-512">В свойства типов выходных данных командлетов добавлен атрибут Ps1XmlAttribute.</span><span class="sxs-lookup"><span data-stu-id="fbc12-512">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="fbc12-513">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fbc12-513">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="fbc12-514">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6370.</span><span class="sxs-lookup"><span data-stu-id="fbc12-514">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="fbc12-515">В AutoMapper исправлена ошибка, препятствовавшая преобразованию PsApiManagementApi в ApiContract.</span><span class="sxs-lookup"><span data-stu-id="fbc12-515">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="fbc12-516">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6515.</span><span class="sxs-lookup"><span data-stu-id="fbc12-516">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="fbc12-517">В File.Save исправлена ошибка, связанная с перегрузкой типом кодировки.</span><span class="sxs-lookup"><span data-stu-id="fbc12-517">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="fbc12-518">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6560.</span><span class="sxs-lookup"><span data-stu-id="fbc12-518">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="fbc12-519">Выполнено обновление до версии NuGet 4.0.3, что позволило исправить исключение шаблона в apiId.</span><span class="sxs-lookup"><span data-stu-id="fbc12-519">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="fbc12-520">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="fbc12-520">AzureRM.Compute</span></span>
* <span data-ttu-id="fbc12-521">Устранена ошибка при создании виртуальной машины с помощью командлета New-AzureRmVm и параметра DiskFileParameterSet, которая возникала из-за переименования типа учетной записи хранения PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="fbc12-521">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="fbc12-522">Исправлен командлет Invoke-AzureRmVMRunCommand.</span><span class="sxs-lookup"><span data-stu-id="fbc12-522">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="fbc12-523">Командлет Get-AzureRmAvailabilitySet теперь может выводить список всех групп доступности в подписке.</span><span class="sxs-lookup"><span data-stu-id="fbc12-523">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="fbc12-524">(Параметр ResouceGroupName теперь является необязательным.)</span><span class="sxs-lookup"><span data-stu-id="fbc12-524">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="fbc12-525">Обновлен параметр SimpleParameterSet командлета New-AzureRmVm, что позволило использовать ускоренную сеть на соответствующих виртуальных машинах.</span><span class="sxs-lookup"><span data-stu-id="fbc12-525">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="fbc12-526">Обновлен простой набор параметров New-AzureRmVmss, что позволило отменять создание масштабируемого набора виртуальных машин, если указанная пользователем подсистема балансировки нагрузки уже существует.</span><span class="sxs-lookup"><span data-stu-id="fbc12-526">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="fbc12-527">Обновлен пример для New-AzureRmDisk.</span><span class="sxs-lookup"><span data-stu-id="fbc12-527">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="fbc12-528">Добавлен пример для New-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="fbc12-528">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="fbc12-529">Обновлено описание командлета Set-AzureRmVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="fbc12-529">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="fbc12-530">Обновлен пример 1 для Set-AzureRmVMBginfoExtension: исправлены орфографические ошибки и префикс.</span><span class="sxs-lookup"><span data-stu-id="fbc12-530">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="fbc12-531">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="fbc12-531">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="fbc12-532">Пакет .NET SDK для ADF обновлен до версии 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="fbc12-532">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="fbc12-533">Добавлена поддержка совместного использования локальной среды IR несколькими фабриками данных.</span><span class="sxs-lookup"><span data-stu-id="fbc12-533">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="fbc12-534">Добавлен новый параметр -SharedIntegrationRuntimeResourceId для командлета Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-534">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="fbc12-535">Добавлен новый необязательный параметр -LinkedDataFactoryName для командлета Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc12-535">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="fbc12-536">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fbc12-536">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="fbc12-537">Пакет SDK для плоскости данных (Microsoft.Azure.DataLake.Store) обновлен до версии 1.1.9.</span><span class="sxs-lookup"><span data-stu-id="fbc12-537">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="fbc12-538">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="fbc12-538">AzureRM.EventHub</span></span>
* <span data-ttu-id="fbc12-539">Обновлена конвейерная передача для InputObject и ResourceId в командлетах remove.</span><span class="sxs-lookup"><span data-stu-id="fbc12-539">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="fbc12-540">AzureRM.Insights;</span><span class="sxs-lookup"><span data-stu-id="fbc12-540">AzureRM.Insights</span></span>
* <span data-ttu-id="fbc12-541">Исправлено форматирование OutputType в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="fbc12-541">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="fbc12-542">Применен пакет SDK Microsoft.Azure.Management.Monitor 0.19.1-preview.</span><span class="sxs-lookup"><span data-stu-id="fbc12-542">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="fbc12-543">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fbc12-543">AzureRM.KeyVault</span></span>
* <span data-ttu-id="fbc12-544">Исправлена проблема с конвейерной передачей в командлете Set-AzureRmKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="fbc12-544">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="fbc12-545">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="fbc12-545">AzureRM.Network</span></span>
* <span data-ttu-id="fbc12-546">Добавлены примеры для командлетов LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="fbc12-546">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="fbc12-547">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="fbc12-547">AzureRM.Resources</span></span>
* <span data-ttu-id="fbc12-548">Устранена проблема, возникавшая при указании имени и значения тега для Get-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="fbc12-548">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="fbc12-549">Исправлен сценарий конвейерной передачи в Set-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="fbc12-549">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="fbc12-550">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="fbc12-550">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="fbc12-551">Обновлена конвейерная передача для InputObject и ResourceId в командлетах remove.</span><span class="sxs-lookup"><span data-stu-id="fbc12-551">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="fbc12-552">Исправлено несколько ошибок.</span><span class="sxs-lookup"><span data-stu-id="fbc12-552">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="fbc12-553">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="fbc12-553">AzureRM.Sql</span></span>
* <span data-ttu-id="fbc12-554">Добавлена поддержка Advanced Threat Protection для сервера с помощью следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="fbc12-554">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="fbc12-555">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="fbc12-555">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="fbc12-556">Добавлена поддержка оценки уязвимостей с помощью следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="fbc12-556">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="fbc12-557">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings;</span><span class="sxs-lookup"><span data-stu-id="fbc12-557">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="fbc12-558">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline;</span><span class="sxs-lookup"><span data-stu-id="fbc12-558">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="fbc12-559">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan.</span><span class="sxs-lookup"><span data-stu-id="fbc12-559">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="fbc12-560">Исправлен пример для Remove-AzureRmSqlServerFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="fbc12-560">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="fbc12-561">Исправлена неправильная обработка даты и времени для базового языка и региональных параметров, отличных от США, в Get-AzureSqlSyncGroupLog.</span><span class="sxs-lookup"><span data-stu-id="fbc12-561">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="fbc12-562">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="fbc12-562">AzureRM.Storage</span></span>
* <span data-ttu-id="fbc12-563">В свойства типов выходных данных командлетов добавлен атрибут Ps1XmlAttribute.</span><span class="sxs-lookup"><span data-stu-id="fbc12-563">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="fbc12-564">Выходные данные командлетов StorageAccount теперь отображаются в виде таблицы.</span><span class="sxs-lookup"><span data-stu-id="fbc12-564">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="fbc12-565">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fbc12-565">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="fbc12-566">New-AzureRmStorageAccount;</span><span class="sxs-lookup"><span data-stu-id="fbc12-566">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="fbc12-567">Set-AzureRmStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="fbc12-567">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="fbc12-568">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="fbc12-568">AzureRM.Tags</span></span>
* <span data-ttu-id="fbc12-569">Удалено неверное утверждение из справки по командлетам Tag.</span><span class="sxs-lookup"><span data-stu-id="fbc12-569">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="fbc12-570">6.5.0 — июль 2018 г.</span><span class="sxs-lookup"><span data-stu-id="fbc12-570">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="fbc12-571">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="fbc12-571">AzureRM.Profile</span></span>
* <span data-ttu-id="fbc12-572">Обновлена справка для командлета Get-AzureRmContextAutosaveSetting.</span><span class="sxs-lookup"><span data-stu-id="fbc12-572">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="fbc12-573">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="fbc12-573">Azure.Storage</span></span>
* <span data-ttu-id="fbc12-574">Добавлена поддержка отправки BLOB-объекта или файла с помощью токена SAS, доступного только для записи.</span><span class="sxs-lookup"><span data-stu-id="fbc12-574">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="fbc12-575">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="fbc12-575">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="fbc12-576">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="fbc12-576">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="fbc12-577">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="fbc12-577">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="fbc12-578">Для AS добавлено обязательное свойство ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="fbc12-578">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="fbc12-579">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="fbc12-579">AzureRM.Automation</span></span>
* <span data-ttu-id="fbc12-580">Обновлена справка и добавлены примеры для командлета New-AzureRMAutomationSchedule.</span><span class="sxs-lookup"><span data-stu-id="fbc12-580">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="fbc12-581">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="fbc12-581">AzureRM.Compute</span></span>
* <span data-ttu-id="fbc12-582">Добавлен параметр -Tag для командлета Update/New-AzureRmAvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="fbc12-582">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="fbc12-583">Добавлен пример для командлета Add-AzureRmVmssExtension.</span><span class="sxs-lookup"><span data-stu-id="fbc12-583">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="fbc12-584">Добавлены примеры для командлета Remove-AzureRmVmssExtension.</span><span class="sxs-lookup"><span data-stu-id="fbc12-584">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="fbc12-585">Обновлена справка для командлета Set-AzureRmVMAccessExtension.</span><span class="sxs-lookup"><span data-stu-id="fbc12-585">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="fbc12-586">Изменен класс SimpleParameterSet для командлета New-AzureRmVmss: теперь для SinglePlacementGroup по умолчанию задается значение false, а также добавляется параметр-переключатель SinglePlacementGroup, который позволяет пользователю создать VMSS в одной группе размещения.</span><span class="sxs-lookup"><span data-stu-id="fbc12-586">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="fbc12-587">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="fbc12-587">AzureRM.EventHub</span></span>
* <span data-ttu-id="fbc12-588">В класс PSEventHubDRConfigurationAttributes добавлено доступное только для чтения свойство PendingReplicationOperationsCount, которое показывает количество ожидающих репликации операций во время реплицирования.</span><span class="sxs-lookup"><span data-stu-id="fbc12-588">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="fbc12-589">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fbc12-589">AzureRM.KeyVault</span></span>
* <span data-ttu-id="fbc12-590">Обновлено сообщение об ошибке для командлета Set-AzureRmKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="fbc12-590">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="fbc12-591">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="fbc12-591">AzureRM.LogicApp</span></span>
* <span data-ttu-id="fbc12-592">Исправлена ошибка "parameter set could not be resolved" (не удалось разрешить заданный параметр) в командлете New-AzureRmLogicApp.</span><span class="sxs-lookup"><span data-stu-id="fbc12-592">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="fbc12-593">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="fbc12-593">AzureRM.Network</span></span>
* <span data-ttu-id="fbc12-594">Включен пиринг между виртуальными сетями в нескольких клиентах для командлета Set/Add-AzureRmVirtualNetworkPeering.</span><span class="sxs-lookup"><span data-stu-id="fbc12-594">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="fbc12-595">Для шлюза приложений обновлены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="fbc12-595">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="fbc12-596">New-AzureRmApplicationGateway: добавлены флаг EnableFIPS и поддержка зон.</span><span class="sxs-lookup"><span data-stu-id="fbc12-596">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="fbc12-597">New-AzureRmApplicationGatewaySku: добавлены новые номера SKU Standard_v2 и WAF_v2.</span><span class="sxs-lookup"><span data-stu-id="fbc12-597">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="fbc12-598">Set-AzureRmApplicationGatewaySku: добавлены новые номера SKU Standard_v2 и WAF_v2.</span><span class="sxs-lookup"><span data-stu-id="fbc12-598">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="fbc12-599">Командлеты RouteTable пересозданы в последней версии генератора.</span><span class="sxs-lookup"><span data-stu-id="fbc12-599">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="fbc12-600">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="fbc12-600">AzureRM.Relay</span></span>
* <span data-ttu-id="fbc12-601">Обновлены файлы Markdown, исправлена проблема с именем параметра в примере.</span><span class="sxs-lookup"><span data-stu-id="fbc12-601">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="fbc12-602">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="fbc12-602">AzureRM.Resources</span></span>
* <span data-ttu-id="fbc12-603">Обновлены командлеты Roleassignment и roledefinition:</span><span class="sxs-lookup"><span data-stu-id="fbc12-603">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="fbc12-604">Удалены лишние вызовы roledefinition, выполняемые в ходе разбиения на страницы.</span><span class="sxs-lookup"><span data-stu-id="fbc12-604">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="fbc12-605">Исправлен командлет Get-AzureRmRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="fbc12-605">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="fbc12-606">Исправлена работа параметра -ExpandPrincipalGroups.</span><span class="sxs-lookup"><span data-stu-id="fbc12-606">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="fbc12-607">Устранена проблема в командлете Get-AzureRmResource, заключающая в том, что в параметре -ResourceType учитывался регистр символов.</span><span class="sxs-lookup"><span data-stu-id="fbc12-607">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="fbc12-608">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="fbc12-608">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="fbc12-609">Добавлены параметры top и skip для командлетов list.</span><span class="sxs-lookup"><span data-stu-id="fbc12-609">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="fbc12-610">Добавлены командлеты для перехода с пространства имен ценовой категории "Стандартный" на пространство ценовой категории "Премиум":</span><span class="sxs-lookup"><span data-stu-id="fbc12-610">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="fbc12-611">Start-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="fbc12-611">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="fbc12-612">Get-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="fbc12-612">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="fbc12-613">Complete-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="fbc12-613">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="fbc12-614">Stop-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="fbc12-614">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="fbc12-615">Remove-AzureRmServiceBusMigration.</span><span class="sxs-lookup"><span data-stu-id="fbc12-615">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="fbc12-616">В класс PSServiceBusDRConfigurationAttributes добавлено доступное только для чтения свойство PendingReplicationOperationsCount, которое показывает количество ожидающих репликации операций во время реплицирования.</span><span class="sxs-lookup"><span data-stu-id="fbc12-616">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="fbc12-617">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fbc12-617">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="fbc12-618">Обновлен пример для командлета New-AzureRmServiceFabricCluster.</span><span class="sxs-lookup"><span data-stu-id="fbc12-618">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="fbc12-619">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="fbc12-619">AzureRM.Sql</span></span>
* <span data-ttu-id="fbc12-620">Добавлены новые командлеты для Management.Sql, позволяющие клиентам добавлять сертификат TDE в экземпляр SQL Server или управляемый экземпляр:</span><span class="sxs-lookup"><span data-stu-id="fbc12-620">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="fbc12-621">Add-AzureRmSqlServerTransparentDataEncryptionCertificate;</span><span class="sxs-lookup"><span data-stu-id="fbc12-621">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="fbc12-622">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate.</span><span class="sxs-lookup"><span data-stu-id="fbc12-622">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="fbc12-623">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="fbc12-623">AzureRM.Websites</span></span>
* <span data-ttu-id="fbc12-624">`Set-AzureRmWebApp -AssignIdentity` и `Set-AzureRmWebAppSlot -AssignIdentity` при установленном значении false теперь будут удалять свойство Identity из объекта сайта. Также при этом будет удаляться тег предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="fbc12-624">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="fbc12-625">Обновлен пример для `Get-AzureRmWebAppMetrics` и `Get-AzureRmAppServicePlanMetrics`.</span><span class="sxs-lookup"><span data-stu-id="fbc12-625">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="fbc12-626">`Set-AzureRmWebApp -PhpVersion` теперь поддерживает off как допустимую версию PHP.</span><span class="sxs-lookup"><span data-stu-id="fbc12-626">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="fbc12-627">6.4.0 — июль 2018 г.</span><span class="sxs-lookup"><span data-stu-id="fbc12-627">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="fbc12-628">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="fbc12-628">General</span></span>
* <span data-ttu-id="fbc12-629">Исправлено форматирование OutputType в файлах справки для большинства модулей.</span><span class="sxs-lookup"><span data-stu-id="fbc12-629">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="fbc12-630">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="fbc12-630">AzureRM.Profile</span></span>
* <span data-ttu-id="fbc12-631">В основные типы выходных данных добавлен атрибут Ps1Xml.</span><span class="sxs-lookup"><span data-stu-id="fbc12-631">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="fbc12-632">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="fbc12-632">AzureRM.Compute</span></span>
* <span data-ttu-id="fbc12-633">Функция добавления тега IP-адреса для масштабируемого набора виртуальных машин (VMSS)</span><span class="sxs-lookup"><span data-stu-id="fbc12-633">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="fbc12-634">Добавлен командлет New-AzureRmVmssIpTagConfig.</span><span class="sxs-lookup"><span data-stu-id="fbc12-634">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="fbc12-635">В New-AzureRmVmssIpConfig добавлен параметр IpTag.</span><span class="sxs-lookup"><span data-stu-id="fbc12-635">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="fbc12-636">Функция автоматического отката ОС для VMSS</span><span class="sxs-lookup"><span data-stu-id="fbc12-636">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="fbc12-637">В New-AzureRmVmssConfig и Update-AzureRmVmss добавлены параметры DisableAutoRollback.</span><span class="sxs-lookup"><span data-stu-id="fbc12-637">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="fbc12-638">Функция ведения журнала обновлений ОС для VMSS</span><span class="sxs-lookup"><span data-stu-id="fbc12-638">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="fbc12-639">В Get-AzureRmVmss добавлен параметр OSUpgradeHistory.</span><span class="sxs-lookup"><span data-stu-id="fbc12-639">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="fbc12-640">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="fbc12-640">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="fbc12-641">Добавлена поддержка списков управления доступом к каталогу с использованием следующих команд:</span><span class="sxs-lookup"><span data-stu-id="fbc12-641">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="fbc12-642">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry;</span><span class="sxs-lookup"><span data-stu-id="fbc12-642">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="fbc12-643">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry;</span><span class="sxs-lookup"><span data-stu-id="fbc12-643">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="fbc12-644">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="fbc12-644">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="fbc12-645">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fbc12-645">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="fbc12-646">Добавлены поддержка отмены выполнения и отслеживание хода выполнения для Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl и Remove-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="fbc12-646">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="fbc12-647">Добавлена поддержка отмены выполнения для Export-AzureRmDataLakeStoreChildItemProperties.</span><span class="sxs-lookup"><span data-stu-id="fbc12-647">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="fbc12-648">Исправлена очистка сообщений об отладке для командлетов, которые выполняют рекурсивные операции.</span><span class="sxs-lookup"><span data-stu-id="fbc12-648">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="fbc12-649">Исправлено расположение тестовых данных для командлетов DataLake.</span><span class="sxs-lookup"><span data-stu-id="fbc12-649">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="fbc12-650">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="fbc12-650">AzureRM.EventHub</span></span>
* <span data-ttu-id="fbc12-651">Для командлетов вывода списка операций Get-AzureRmEventHub и Get-AzureRmEventHubConsumerGroup добавлен необязательный параметр MaxCount.</span><span class="sxs-lookup"><span data-stu-id="fbc12-651">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="fbc12-652">Исправлена проблема с командлетом New-AzureRmEventHub, из-за которой требовалось указать по крайней мере один параметр при создании концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="fbc12-652">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="fbc12-653">Добавлен набор параметров по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fbc12-653">Provided Default Parameter set.</span></span>
* <span data-ttu-id="fbc12-654">Для командлета New-AzureRmEventHubKey добавлен необязательный параметр -KeyValue, который позволяет пользователю предоставить значение ключа.</span><span class="sxs-lookup"><span data-stu-id="fbc12-654">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="fbc12-655">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fbc12-655">AzureRM.KeyVault</span></span>
* <span data-ttu-id="fbc12-656">Исправлена ошибка, из-за которой при выполнении командлета Get-AzureRmKeyVault с параметром -Tag возвращались все ресурсы.</span><span class="sxs-lookup"><span data-stu-id="fbc12-656">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="fbc12-657">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="fbc12-657">AzureRM.Network</span></span>
* <span data-ttu-id="fbc12-658">Для параметра шлюзов виртуальной вести, избыточных в пределах зоны, предоставлены новые номера SKU.</span><span class="sxs-lookup"><span data-stu-id="fbc12-658">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="fbc12-659">Добавлены новые команды для функции поддержки партнерских API для ExpressRoute, развертываемых с помощью ARM:</span><span class="sxs-lookup"><span data-stu-id="fbc12-659">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="fbc12-660">добавлена команда Get-AzureRmExpressRouteCrossConnection;</span><span class="sxs-lookup"><span data-stu-id="fbc12-660">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="fbc12-661">добавлена команда Set-AzureRmExpressRouteCrossConnection;</span><span class="sxs-lookup"><span data-stu-id="fbc12-661">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="fbc12-662">добавлена команда Add-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="fbc12-662">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="fbc12-663">добавлена команда Get-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="fbc12-663">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="fbc12-664">добавлена команда Remove-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="fbc12-664">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="fbc12-665">добавлена команда Get-AzureRMExpressRouteCrossConnectionArpTable;</span><span class="sxs-lookup"><span data-stu-id="fbc12-665">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="fbc12-666">добавлена команда Get-AzureRMExpressRouteCrossConnectionRouteTable;</span><span class="sxs-lookup"><span data-stu-id="fbc12-666">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="fbc12-667">добавлена команда Get-AzureRMExpressRouteCrossConnectionRouteTableSummary.</span><span class="sxs-lookup"><span data-stu-id="fbc12-667">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="fbc12-668">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="fbc12-668">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="fbc12-669">Добавлен командлет Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="fbc12-669">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="fbc12-670">Этот командлет принимает идентификатор виртуальной машины и проверяет, защищена ли виртуальная машина с помощью какого-либо хранилища в подписке.</span><span class="sxs-lookup"><span data-stu-id="fbc12-670">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="fbc12-671">Если такое хранилище существует, командлет выводит данные о нем.</span><span class="sxs-lookup"><span data-stu-id="fbc12-671">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="fbc12-672">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="fbc12-672">AzureRM.Resources</span></span>
* <span data-ttu-id="fbc12-673">Обновлены командлеты Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="fbc12-673">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="fbc12-674">Добавлена поддержка вывода списка значений параметра -Scope на уровне группы управления.</span><span class="sxs-lookup"><span data-stu-id="fbc12-674">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="fbc12-675">Добавлена поддержка для получения отдельных назначений со значениями -Scope на уровне группы управления.</span><span class="sxs-lookup"><span data-stu-id="fbc12-675">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="fbc12-676">Для параметра управления добавлены параметры -Effective и -All.</span><span class="sxs-lookup"><span data-stu-id="fbc12-676">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="fbc12-677">Обновлены командлеты Get/New/Remove/Set-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="fbc12-677">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="fbc12-678">Добавлен параметр -ManagementGroupName для применения операций к заданной группе управления.</span><span class="sxs-lookup"><span data-stu-id="fbc12-678">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="fbc12-679">Добавлен параметр -SubscriptionId для применения операций к заданной подписке.</span><span class="sxs-lookup"><span data-stu-id="fbc12-679">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="fbc12-680">Обновлены командлеты Get/New/Remove/Set-AzureRmPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="fbc12-680">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="fbc12-681">Добавлен параметр -ManagementGroupName для применения операций к заданной группе управления.</span><span class="sxs-lookup"><span data-stu-id="fbc12-681">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="fbc12-682">Добавлен параметр -SubscriptionId для применения операций к заданной подписке.</span><span class="sxs-lookup"><span data-stu-id="fbc12-682">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="fbc12-683">Добавлена поддержка ссылок на секрет KeyVault в параметрах при использовании TemplateParameterObject в New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="fbc12-683">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="fbc12-684">Устранена проблема, из-за которой параметр -EndDate игнорировался в New-AzureRmADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="fbc12-684">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="fbc12-685">Устранена проблема, из-за которой в Add-AzureRmADGroupMember использовался неверный URL-адрес для запроса.</span><span class="sxs-lookup"><span data-stu-id="fbc12-685">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="fbc12-686">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="fbc12-686">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="fbc12-687">Для командлета New-AzureRmServiceBusKey добавлен необязательный параметр -KeyValue, который позволяет пользователю предоставить значение ключа.</span><span class="sxs-lookup"><span data-stu-id="fbc12-687">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="fbc12-688">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="fbc12-688">AzureRM.Sql</span></span>
* <span data-ttu-id="fbc12-689">В справке по New-AzureRmSqlDatabaseRestorePoint добавлено описание определяемых пользователем точек восстановления для хранилища данных SQL.</span><span class="sxs-lookup"><span data-stu-id="fbc12-689">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="fbc12-690">Обновлена документация по параметру -ComputeGeneration, используемого в нескольких командлетах.</span><span class="sxs-lookup"><span data-stu-id="fbc12-690">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="fbc12-691">6.3.0 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="fbc12-691">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="fbc12-692">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="fbc12-692">AzureRM.Profile</span></span>
* <span data-ttu-id="fbc12-693">Обновлены сообщения об ошибках для Enable-AzureRmContextAutoSave.</span><span class="sxs-lookup"><span data-stu-id="fbc12-693">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="fbc12-694">Создание контекста для каждой подписки при выполнении Connect-AzureRmAccount без предыдущего контекста.</span><span class="sxs-lookup"><span data-stu-id="fbc12-694">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="fbc12-695">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="fbc12-695">Azure.Storage</span></span>
* <span data-ttu-id="fbc12-696">В файлы справки добавлены дополнительные сведения о параметре -Permissions.</span><span class="sxs-lookup"><span data-stu-id="fbc12-696">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="fbc12-697">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="fbc12-697">AzureRM.Compute</span></span>
* <span data-ttu-id="fbc12-698">Get-AzureRmVmDiskEncryptionStatus устраняет проблему, которая наблюдалась на виртуальных машинах без дисков данных.</span><span class="sxs-lookup"><span data-stu-id="fbc12-698">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="fbc12-699">Обновлена версия клиентской библиотеки Compute для исправления следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="fbc12-699">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="fbc12-700">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="fbc12-700">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="fbc12-701">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="fbc12-701">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="fbc12-702">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="fbc12-702">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="fbc12-703">В следующих командлетах исправлено отображение неправильных значений operation ID и operation status:</span><span class="sxs-lookup"><span data-stu-id="fbc12-703">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="fbc12-704">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="fbc12-704">Start-AzureRmVM</span></span>
    - <span data-ttu-id="fbc12-705">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="fbc12-705">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="fbc12-706">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="fbc12-706">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="fbc12-707">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="fbc12-707">Set-AzureRmVM</span></span>
    - <span data-ttu-id="fbc12-708">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="fbc12-708">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="fbc12-709">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fbc12-709">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="fbc12-710">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="fbc12-710">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="fbc12-711">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="fbc12-711">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="fbc12-712">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fbc12-712">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="fbc12-713">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fbc12-713">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="fbc12-714">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fbc12-714">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="fbc12-715">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fbc12-715">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="fbc12-716">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="fbc12-716">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="fbc12-717">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="fbc12-717">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="fbc12-718">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="fbc12-718">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="fbc12-719">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="fbc12-719">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="fbc12-720">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="fbc12-720">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="fbc12-721">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="fbc12-721">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="fbc12-722">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="fbc12-722">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="fbc12-723">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="fbc12-723">AzureRM.EventGrid</span></span>
* <span data-ttu-id="fbc12-724">Удалены условия проверки ValidateNotNullOrEmpty для SubjectBeginsWith/SubjectEndsWith в командлете Update-AzureRmEventGridSubscription, что позволяет при необходимости заменять эти параметры пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="fbc12-724">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="fbc12-725">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fbc12-725">AzureRM.KeyVault</span></span>
* <span data-ttu-id="fbc12-726">Исправлена ошибка, когда при выполнении командлета Get-AzureRmKeyVault -Tag не возвращается ни один тег.</span><span class="sxs-lookup"><span data-stu-id="fbc12-726">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="fbc12-727">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="fbc12-727">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="fbc12-728">Общедоступный выпуск командлетов Policy Insights.</span><span class="sxs-lookup"><span data-stu-id="fbc12-728">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="fbc12-729">Используется API версии 2018-04-04.</span><span class="sxs-lookup"><span data-stu-id="fbc12-729">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="fbc12-730">К результатам Get-AzureRmPolicyStateSummary добавлено PolicyDefinitionReferenceId.</span><span class="sxs-lookup"><span data-stu-id="fbc12-730">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="fbc12-731">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="fbc12-731">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="fbc12-732">Для командлетов RecoveryServices.Backup добавлен параметр -Vault.</span><span class="sxs-lookup"><span data-stu-id="fbc12-732">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="fbc12-733">Передача этого параметра переопределяет командлет Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="fbc12-733">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="fbc12-734">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="fbc12-734">AzureRM.Sql</span></span>
* <span data-ttu-id="fbc12-735">В файле справки обновлен пример для командлета Get-AzureRmSqlDatabaseExpanded.</span><span class="sxs-lookup"><span data-stu-id="fbc12-735">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="fbc12-736">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="fbc12-736">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="fbc12-737">Обновлен файл справки для командлета Add-AzureRmTrafficManagerEndpointConfig.</span><span class="sxs-lookup"><span data-stu-id="fbc12-737">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="fbc12-738">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="fbc12-738">AzureRM.Websites</span></span>
* <span data-ttu-id="fbc12-739">Изменено действие командлета Set-AzureRmWebApp. Теперь он не перезаписывает AppSettings, если используется параметр -AssignIdentity.</span><span class="sxs-lookup"><span data-stu-id="fbc12-739">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="fbc12-740">Командлет New-AzureRmWebAppSlot теперь учитывает дополнительный параметр AppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="fbc12-740">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="fbc12-741">6.2.1 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="fbc12-741">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="fbc12-742">AzureRM.OperationalInsights;</span><span class="sxs-lookup"><span data-stu-id="fbc12-742">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="fbc12-743">В обновленной модели PSWorkspace Network может использовать type в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="fbc12-743">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="fbc12-744">6.2.0 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="fbc12-744">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="fbc12-745">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="fbc12-745">AzureRM.Profile</span></span>
* <span data-ttu-id="fbc12-746">Исправлена ошибка с загрузкой Newtonsoft.Json версии 10.0.3 во время импорта модуля.</span><span class="sxs-lookup"><span data-stu-id="fbc12-746">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="fbc12-747">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="fbc12-747">AzureRM.Compute</span></span>
* <span data-ttu-id="fbc12-748">Функция обновления виртуальных машин VMSS.</span><span class="sxs-lookup"><span data-stu-id="fbc12-748">VMSS VM Update feature</span></span>
    - <span data-ttu-id="fbc12-749">Добавлены командлеты Update-AzureRmVmssVM и New-AzureRmVMDataDisk.</span><span class="sxs-lookup"><span data-stu-id="fbc12-749">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="fbc12-750">В командлет Add-AzureRmVMDataDisk добавлен параметр VirtualMachineScaleSetVM, который позволяет добавлять диски данных в виртуальные машины VMSS.</span><span class="sxs-lookup"><span data-stu-id="fbc12-750">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="fbc12-751">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="fbc12-751">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="fbc12-752">Пакет SDK для ADF .NET обновлен до версии 0.8.0-preview. Новая версия содержит такие изменения:</span><span class="sxs-lookup"><span data-stu-id="fbc12-752">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="fbc12-753">добавлена операция для настройки репозитория фабрики;</span><span class="sxs-lookup"><span data-stu-id="fbc12-753">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="fbc12-754">связанная служба QuickBooks LinkedService теперь предоставляет свойства consumerKey и consumerSecret;</span><span class="sxs-lookup"><span data-stu-id="fbc12-754">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="fbc12-755">тип нескольких моделей изменен с SecretBase на Object;</span><span class="sxs-lookup"><span data-stu-id="fbc12-755">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="fbc12-756">добавлен триггер событий BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="fbc12-756">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="fbc12-757">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fbc12-757">AzureRM.KeyVault</span></span>
* <span data-ttu-id="fbc12-758">В документацию добавлены примеры выходных данных.</span><span class="sxs-lookup"><span data-stu-id="fbc12-758">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="fbc12-759">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="fbc12-759">AzureRM.Network</span></span>
* <span data-ttu-id="fbc12-760">В командлеты Наблюдателя за сетями добавлены параметры Аналитики трафика.</span><span class="sxs-lookup"><span data-stu-id="fbc12-760">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="fbc12-761">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="fbc12-761">AzureRM.Resources</span></span>
* <span data-ttu-id="fbc12-762">Исправлена ошибка, когда командлет Get-AzureRmResource возвращает свойство Properties объектов PSResource.</span><span class="sxs-lookup"><span data-stu-id="fbc12-762">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="fbc12-763">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="fbc12-763">AzureRM.Scheduler</span></span>
* <span data-ttu-id="fbc12-764">Исправлена ошибка, когда обновление ServiceBusQueueJob не задает новые значения для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="fbc12-764">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="fbc12-765">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="fbc12-765">AzureRM.Sql</span></span>
* <span data-ttu-id="fbc12-766">В перечисленные ниже командлеты добавлен необязательный параметр LicenseType.</span><span class="sxs-lookup"><span data-stu-id="fbc12-766">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="fbc12-767">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="fbc12-767">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="fbc12-768">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool;</span><span class="sxs-lookup"><span data-stu-id="fbc12-768">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="fbc12-769">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="fbc12-769">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="fbc12-770">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="fbc12-770">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="fbc12-771">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fbc12-771">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="fbc12-772">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="fbc12-772">AzureRM.Websites</span></span>
* <span data-ttu-id="fbc12-773">Командлет New-AzureRMWebApp теперь использует общие алгоритмы из библиотеки Strategy.</span><span class="sxs-lookup"><span data-stu-id="fbc12-773">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="fbc12-774">6.1.0 — май 2018 г.</span><span class="sxs-lookup"><span data-stu-id="fbc12-774">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="fbc12-775">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="fbc12-775">AzureRM.Profile</span></span>
* <span data-ttu-id="fbc12-776">Устранена проблема с выполнением Clear-AzureRmContext, при которой сохранялся пустой контекст с именем предыдущего контекста по умолчанию, что не позволяло пользователю создать новый контекст со старым именем.</span><span class="sxs-lookup"><span data-stu-id="fbc12-776">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="fbc12-777">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="fbc12-777">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="fbc12-778">Включены операции связывания и отмены связи в автономной системе.</span><span class="sxs-lookup"><span data-stu-id="fbc12-778">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="fbc12-779">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fbc12-779">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="fbc12-780">Добавлена поддержка ApiVersions, ApiReleases и ApiRevisions.</span><span class="sxs-lookup"><span data-stu-id="fbc12-780">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="fbc12-781">Добавлена поддержка серверной части ServiceFabric.</span><span class="sxs-lookup"><span data-stu-id="fbc12-781">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="fbc12-782">Добавлена поддержка средства ведения журнала Application Insights.</span><span class="sxs-lookup"><span data-stu-id="fbc12-782">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="fbc12-783">Добавлена поддержка для распознавания номера SKU уровня "Базовый" как допустимого номера SKU службы управления API.</span><span class="sxs-lookup"><span data-stu-id="fbc12-783">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="fbc12-784">Добавлена поддержка установки сертификатов, выданных частным центром сертификации в качестве корневого или обычного ЦС.</span><span class="sxs-lookup"><span data-stu-id="fbc12-784">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="fbc12-785">Добавлена поддержка для приема пользовательских SSL-сертификатов с помощью KeyVault и нескольких имен узлов прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="fbc12-785">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="fbc12-786">Добавлена поддержка для удостоверения MSI.</span><span class="sxs-lookup"><span data-stu-id="fbc12-786">Added support for MSI identity</span></span>
* <span data-ttu-id="fbc12-787">Добавлена поддержка для принятия политик с помощью URL-адреса. Примечание. Указанные ниже командлеты в следующей версии будут отмечены как нерекомендуемые.</span><span class="sxs-lookup"><span data-stu-id="fbc12-787">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="fbc12-788">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="fbc12-788">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="fbc12-789">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="fbc12-789">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="fbc12-790">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="fbc12-790">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="fbc12-791">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="fbc12-791">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="fbc12-792">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="fbc12-792">AzureRM.Batch</span></span>
* <span data-ttu-id="fbc12-793">Выпущен новый командлет Get-AzureBatchPoolNodeCounts.</span><span class="sxs-lookup"><span data-stu-id="fbc12-793">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="fbc12-794">Выпущен новый командлет Start-AzureBatchComputeNodeServiceLogUpload.</span><span class="sxs-lookup"><span data-stu-id="fbc12-794">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="fbc12-795">AzureRM.Consumption:</span><span class="sxs-lookup"><span data-stu-id="fbc12-795">AzureRM.Consumption</span></span>
* <span data-ttu-id="fbc12-796">Добавлены новые параметры Expand, ResourceGroup, InstanceName, InstanceId, Tags и командлет высшего уровня Get-AzureRmConsumptionUsageDetail.</span><span class="sxs-lookup"><span data-stu-id="fbc12-796">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="fbc12-797">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fbc12-797">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="fbc12-798">Исправлен пример для Export-AzureRmDataLakeStoreChildItemProperties.</span><span class="sxs-lookup"><span data-stu-id="fbc12-798">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="fbc12-799">Исправлено исключение параметра NULL при использовании рекурсии в Set-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="fbc12-799">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="fbc12-800">Исправлены файлы справки для Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl и Remove-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="fbc12-800">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="fbc12-801">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="fbc12-801">AzureRM.Network</span></span>
* <span data-ttu-id="fbc12-802">Пакет SDK для сети обновлен с предварительной версии 18.0.0 до предварительной версии 19.0.0.</span><span class="sxs-lookup"><span data-stu-id="fbc12-802">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="fbc12-803">Добавлен командлет для создания конфигурации протокола.</span><span class="sxs-lookup"><span data-stu-id="fbc12-803">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="fbc12-804">New-AzureRmNetworkWatcherProtocolConfiguration.</span><span class="sxs-lookup"><span data-stu-id="fbc12-804">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="fbc12-805">Добавлен командлет для добавления нового подключения канала к существующему каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="fbc12-805">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="fbc12-806">Add-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="fbc12-806">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="fbc12-807">Добавлен командлет для удаления подключения канала к существующему каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="fbc12-807">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="fbc12-808">Remove-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="fbc12-808">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="fbc12-809">Добавлен командлет для получения подключения канала.</span><span class="sxs-lookup"><span data-stu-id="fbc12-809">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="fbc12-810">Get-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="fbc12-810">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="fbc12-811">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fbc12-811">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="fbc12-812">Исправлена процедура аутентификации сервера с использованием созданных сертификатов (проблема № 5998).</span><span class="sxs-lookup"><span data-stu-id="fbc12-812">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="fbc12-813">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="fbc12-813">AzureRM.Sql</span></span>
* <span data-ttu-id="fbc12-814">Обновлены командлеты аудита, которые теперь позволяют удалять AuditActions или AuditActionGroups.</span><span class="sxs-lookup"><span data-stu-id="fbc12-814">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="fbc12-815">Исправлена проблема с Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy, при которой установка новой гибкой политики хранения завершалась ошибкой с сообщением "Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span><span class="sxs-lookup"><span data-stu-id="fbc12-815">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="fbc12-816">Please submit request with the new flexible retention policy" (Настройка политики долгосрочного хранения с помощью хранилища и политики служб восстановления Azure больше не поддерживается. Отправьте запрос с использованием новой гибкой политики хранения).</span><span class="sxs-lookup"><span data-stu-id="fbc12-816">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="fbc12-817">Обновлены все командлеты, связанные со службой "База данных SQL Azure", с созданием эластичных пулов и обновлением. Теперь используются новые API баз данных с поддержкой свойства номеров SKU для обеспечения масштабируемости и связанных с уровнями возможностей.</span><span class="sxs-lookup"><span data-stu-id="fbc12-817">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="fbc12-818">Обновлены командлеты, в том числе:</span><span class="sxs-lookup"><span data-stu-id="fbc12-818">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="fbc12-819">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="fbc12-819">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="fbc12-820">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool;</span><span class="sxs-lookup"><span data-stu-id="fbc12-820">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="fbc12-821">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="fbc12-821">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="fbc12-822">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="fbc12-822">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="fbc12-823">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fbc12-823">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="fbc12-824">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="fbc12-824">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="fbc12-825">Обновлены параметры для Get-AzureRmTrafficManagerProfile. Теперь при использовании параметра -Name требуется параметр -ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="fbc12-825">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
