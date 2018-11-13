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
ms.openlocfilehash: 8a7b184ed06eb078956229fa67d02840014e3aaf
ms.sourcegitcommit: ac4b53bb42a25aae013a9d8cd9ae98ada9397274
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/08/2018
ms.locfileid: "51275526"
---
# <a name="release-notes"></a><span data-ttu-id="3c38d-103">Заметки о выпуске</span><span class="sxs-lookup"><span data-stu-id="3c38d-103">Release notes</span></span>

<span data-ttu-id="3c38d-104">Здесь приведен список изменений, внесенных в Azure PowerShell в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="3c38d-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6120---november-2018"></a><span data-ttu-id="3c38d-105">6.12.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="3c38d-105">6.12.0 - November 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="3c38d-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="3c38d-106">AzureRM.Profile</span></span>
* <span data-ttu-id="3c38d-107">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-107">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="3c38d-108">В командлете Connect-AzureRmAccount параметр TenantId переименован на Tenant и добавлен псевдоним для TenantId.</span><span class="sxs-lookup"><span data-stu-id="3c38d-108">Rename param TenantId in cmdlet Connect-AzureRmAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="3c38d-109">Обновлено описание TenantId для командлета Connect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="3c38d-109">Updated TenantId description for Connect-AzureRmAccount</span></span>
* <span data-ttu-id="3c38d-110">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="3c38d-110">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="3c38d-111">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="3c38d-111">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="3c38d-112">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="3c38d-112">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="3c38d-113">Устранена проблема, при которой командлет Disconnect-AzureRmAccount вызывал сбой при отсутствии подключения.</span><span class="sxs-lookup"><span data-stu-id="3c38d-113">Fix issue where 'Disconnect-AzureRmAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azurermautomation"></a><span data-ttu-id="3c38d-114">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="3c38d-114">AzureRM.Automation</span></span>
* <span data-ttu-id="3c38d-115">Имя файла библиотеки DLL командлетов переименовано на Microsoft.Azure.Commands.Automation.dll.</span><span class="sxs-lookup"><span data-stu-id="3c38d-115">Renamed cmdlet DLL filename to Microsoft.Azure.Commands.Automation.dll</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="3c38d-116">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3c38d-116">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="3c38d-117">Добавлена операция Get-AzureRmCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="3c38d-117">Add Get-AzureRmCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="3c38d-118">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="3c38d-118">AzureRM.Compute</span></span>
* <span data-ttu-id="3c38d-119">Добавлены командлеты Add-AzureRmVmssVMDataDisk и Remove-AzureRmVmssVMDataDisk.</span><span class="sxs-lookup"><span data-stu-id="3c38d-119">Add Add-AzureRmVmssVMDataDisk and Remove-AzureRmVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="3c38d-120">Get-AzureRmVMImage отображает AutomaticOSUpgradeProperties.</span><span class="sxs-lookup"><span data-stu-id="3c38d-120">Get-AzureRmVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="3c38d-121">Устранена проблема, при которой значения параметров SetAzureRmVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="3c38d-121">Fixed SetAzureRmVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="3c38d-122">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3c38d-122">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="3c38d-123">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="3c38d-123">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="3c38d-124">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="3c38d-124">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="3c38d-125">AzureRM.Insights;</span><span class="sxs-lookup"><span data-stu-id="3c38d-125">AzureRM.Insights</span></span>
* <span data-ttu-id="3c38d-126">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="3c38d-126">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="3c38d-127">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="3c38d-127">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="3c38d-128">Исправлена проблема № 7513 [Insights], ппри которой для командлета Set-AzureRMDiagnosticSetting требовалось явное указание категорий во время создания параметра.</span><span class="sxs-lookup"><span data-stu-id="3c38d-128">Fixed issue #7513 [Insights] Set-AzureRMDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="3c38d-129">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="3c38d-129">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="3c38d-130">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="3c38d-130">AzureRM.Network</span></span>
* <span data-ttu-id="3c38d-131">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="3c38d-131">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="3c38d-132">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="3c38d-132">Get-AzureRmExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="3c38d-133">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="3c38d-133">Get-AzureRmExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="3c38d-134">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="3c38d-134">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="3c38d-135">Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="3c38d-135">Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="3c38d-136">Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="3c38d-136">Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="3c38d-137">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="3c38d-137">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="3c38d-138">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="3c38d-138">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="3c38d-139">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="3c38d-139">Added policy remediation cmdlets</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="3c38d-140">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="3c38d-140">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="3c38d-141">Добавлена поддержка общих файловых ресурсов Azure в Службах восстановления.</span><span class="sxs-lookup"><span data-stu-id="3c38d-141">Added support for azure file shares in recovery services.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="3c38d-142">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="3c38d-142">AzureRM.Resources</span></span>
* <span data-ttu-id="3c38d-143">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="3c38d-143">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="3c38d-144">Разрешено перечисление ресурсов с использованием параметра -ResourceId для командлета Get-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="3c38d-144">Allow listing resources using the '-ResourceId' parameter for 'Get-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="3c38d-145">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3c38d-145">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="3c38d-146">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="3c38d-146">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="3c38d-147">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3c38d-147">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="3c38d-148">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="3c38d-148">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="3c38d-149">Исправлен командлет Add-AzureRmServiceFabricClusterCertificate.</span><span class="sxs-lookup"><span data-stu-id="3c38d-149">Fix 'Add-AzureRmServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="3c38d-150">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="3c38d-150">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="3c38d-151">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="3c38d-151">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="3c38d-152">Исправлен командлет Update-AzureRmServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="3c38d-152">Fix 'Update-AzureRmServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="6110---october-2018"></a><span data-ttu-id="3c38d-153">6.11.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="3c38d-153">6.11.0 - October 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="3c38d-154">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="3c38d-154">AzureRM.Profile</span></span>
* <span data-ttu-id="3c38d-155">Устранена проблема с Get-AzureRmSubscription в CloudShell.</span><span class="sxs-lookup"><span data-stu-id="3c38d-155">Fix issue with Get-AzureRmSubscription in CloudShell</span></span>
* <span data-ttu-id="3c38d-156">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-156">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="3c38d-157">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="3c38d-157">AzureRM.Backup</span></span>
* <span data-ttu-id="3c38d-158">Командлеты Azure Backup объявлены нерекомендуемыми.</span><span class="sxs-lookup"><span data-stu-id="3c38d-158">Deprecated Azure Backup cmdlets.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="3c38d-159">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="3c38d-159">AzureRM.Compute</span></span>
* <span data-ttu-id="3c38d-160">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzureRmVm.</span><span class="sxs-lookup"><span data-stu-id="3c38d-160">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzureRmVm'</span></span>
* <span data-ttu-id="3c38d-161">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="3c38d-161">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="3c38d-162">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3c38d-162">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="3c38d-163">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="3c38d-163">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="3c38d-164">Get-AzureRmDataLakeStoreVirtualNetworkRule — позволяет получить или вывести правило виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3c38d-164">Get-AzureRmDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="3c38d-165">Add-AzureRmDataLakeStoreVirtualNetworkRule — позволяет добавить правило виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3c38d-165">Add-AzureRmDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="3c38d-166">Set-AzureRmDataLakeStoreVirtualNetworkRule — позволяет изменить определенное правило виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3c38d-166">Set-AzureRmDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="3c38d-167">Remove-AzureRmDataLakeStoreVirtualNetworkRule — позволяет удалить правило виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3c38d-167">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="3c38d-168">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="3c38d-168">AzureRM.Network</span></span>
* <span data-ttu-id="3c38d-169">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="3c38d-169">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="3c38d-170">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="3c38d-170">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="3c38d-171">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="3c38d-171">AzureRM.Resources</span></span>
* <span data-ttu-id="3c38d-172">Мы устранили проблему, из-за которой командлет Get-AzureRMRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), и добавили понятное исключение.</span><span class="sxs-lookup"><span data-stu-id="3c38d-172">Fix isssue where Get-AzureRMRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="3c38d-173">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="3c38d-173">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="6100---october-2018"></a><span data-ttu-id="3c38d-174">6.10.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="3c38d-174">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="3c38d-175">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="3c38d-175">Azure.Storage</span></span>
* <span data-ttu-id="3c38d-176">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="3c38d-176">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="3c38d-177">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="3c38d-177">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="3c38d-178">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="3c38d-178">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="3c38d-179">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3c38d-179">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="3c38d-180">Поддержка Get-AzureRmCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="3c38d-180">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="3c38d-181">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="3c38d-181">AzureRM.Compute</span></span>
* <span data-ttu-id="3c38d-182">Исправлена команда Get-AzureRmVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов.</span><span class="sxs-lookup"><span data-stu-id="3c38d-182">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="3c38d-183">Добавлен пример использования SimpleParameterSet в справку командлета New-AzureRmVmss.</span><span class="sxs-lookup"><span data-stu-id="3c38d-183">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="3c38d-184">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="3c38d-184">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="3c38d-185">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="3c38d-185">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="3c38d-186">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="3c38d-186">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="3c38d-187">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="3c38d-187">AzureRM.Network</span></span>
* <span data-ttu-id="3c38d-188">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="3c38d-188">Added NetworkProfile functionality.</span></span> <span data-ttu-id="3c38d-189">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="3c38d-189">new cmdlets added</span></span>
    - <span data-ttu-id="3c38d-190">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3c38d-190">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="3c38d-191">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3c38d-191">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="3c38d-192">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3c38d-192">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="3c38d-193">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3c38d-193">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="3c38d-194">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="3c38d-194">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="3c38d-195">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="3c38d-195">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="3c38d-196">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="3c38d-196">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="3c38d-197">Добавлены командлеты: New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap.</span><span class="sxs-lookup"><span data-stu-id="3c38d-197">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="3c38d-198">Добавлены командлеты: Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="3c38d-198">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="3c38d-199">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="3c38d-199">AzureRM.RedisCache</span></span>
* <span data-ttu-id="3c38d-200">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="3c38d-200">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="3c38d-201">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="3c38d-201">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="3c38d-202">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="3c38d-202">AzureRM.Resources</span></span>
* <span data-ttu-id="3c38d-203">Добавлен отсутствующий параметр -Mode в командлет Set-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="3c38d-203">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="3c38d-204">Исправлена ошибка командлета Get-AzureRmProviderOperation для операций, когда Origin содержит User.</span><span class="sxs-lookup"><span data-stu-id="3c38d-204">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="3c38d-205">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="3c38d-205">AzureRM.Sql</span></span>
* <span data-ttu-id="3c38d-206">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="3c38d-206">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="3c38d-207">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="3c38d-207">AzureRM.Storage</span></span>
* <span data-ttu-id="3c38d-208">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="3c38d-208">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="3c38d-209">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="3c38d-209">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="3c38d-210">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="3c38d-210">AzureRM.Websites</span></span>
* <span data-ttu-id="3c38d-211">Новый командлет Get-AzureRMWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера.</span><span class="sxs-lookup"><span data-stu-id="3c38d-211">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="3c38d-212">Новые командлеты New-AzureRMWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows.</span><span class="sxs-lookup"><span data-stu-id="3c38d-212">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="3c38d-213">6.9.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="3c38d-213">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="3c38d-214">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="3c38d-214">General</span></span>
* <span data-ttu-id="3c38d-215">В модуль развертывания AzureRM добавлен командлет AzureRM.SignalR.</span><span class="sxs-lookup"><span data-stu-id="3c38d-215">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="3c38d-216">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="3c38d-216">AzureRM.Profile</span></span>
* <span data-ttu-id="3c38d-217">Незначительные изменения в общем коде хранилища.</span><span class="sxs-lookup"><span data-stu-id="3c38d-217">Minor changes to the storage common code</span></span>
* <span data-ttu-id="3c38d-218">Обновлены файлы справки, в которые добавлены полные типы параметров.</span><span class="sxs-lookup"><span data-stu-id="3c38d-218">Updated help files to include full parameter types.</span></span>
* <span data-ttu-id="3c38d-219">В наборе параметров ServicePrincipalCertificateWithSubscriptionId параметр -ServicePrincipal теперь стал необязательным.</span><span class="sxs-lookup"><span data-stu-id="3c38d-219">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="3c38d-220">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="3c38d-220">Azure.Storage</span></span>
* <span data-ttu-id="3c38d-221">Поддержка создания контекста хранилища с использованием OAuth.</span><span class="sxs-lookup"><span data-stu-id="3c38d-221">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="3c38d-222">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="3c38d-222">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="3c38d-223">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="3c38d-223">AzureRM.Cdn</span></span>
* <span data-ttu-id="3c38d-224">Добавлен номер SKU для расценок на Standard_Microsoft в CDN.</span><span class="sxs-lookup"><span data-stu-id="3c38d-224">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="3c38d-225">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="3c38d-225">AzureRM.Compute</span></span>
* <span data-ttu-id="3c38d-226">Keyvault и Storage перенесены в общие зависимости.</span><span class="sxs-lookup"><span data-stu-id="3c38d-226">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="3c38d-227">Добавлена поддержка большего количества размеров виртуальных машин в командлеты AEM.</span><span class="sxs-lookup"><span data-stu-id="3c38d-227">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="3c38d-228">Добавлен параметр PublicIPPrefix в командлет New-AzureRmVmssIpConfig.</span><span class="sxs-lookup"><span data-stu-id="3c38d-228">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="3c38d-229">Добавлен параметр ResourceId в командлет Invoke-AzureRmVMRunCommand.</span><span class="sxs-lookup"><span data-stu-id="3c38d-229">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="3c38d-230">Добавлен командлет Invoke-AzureRmVmssVMRunCommand.</span><span class="sxs-lookup"><span data-stu-id="3c38d-230">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="3c38d-231">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="3c38d-231">AzureRM.Dns</span></span>
* <span data-ttu-id="3c38d-232">Добавлена поддержка для псевдонима записи во время создания записи DNS.</span><span class="sxs-lookup"><span data-stu-id="3c38d-232">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="3c38d-233">AzureRM.Insights;</span><span class="sxs-lookup"><span data-stu-id="3c38d-233">AzureRM.Insights</span></span>
* <span data-ttu-id="3c38d-234">Исправлены проблемы № 6833 и № 7102 (область настроек диагностики).</span><span class="sxs-lookup"><span data-stu-id="3c38d-234">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="3c38d-235">Проблемы с именем по умолчанию, например service, во время создания, получения и отображения списка параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="3c38d-235">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="3c38d-236">Проблемы при создании параметров диагностики с категориями.</span><span class="sxs-lookup"><span data-stu-id="3c38d-236">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="3c38d-237">Добавлено сообщение о том, что не рекомендуется использовать параметры интервалов времени в метриках.</span><span class="sxs-lookup"><span data-stu-id="3c38d-237">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="3c38d-238">Параметры интервалов времени по-прежнему принимаются (это не критическое изменение), но они игнорируются в серверной части, потому что действительно только значение PT1M.</span><span class="sxs-lookup"><span data-stu-id="3c38d-238">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="3c38d-239">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="3c38d-239">AzureRM.Network</span></span>
* <span data-ttu-id="3c38d-240">Изменения командлетов LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3c38d-240">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="3c38d-241">LoadBalancerInboundNatPoolConfig: добавлены параметры IdleTimeoutInMinutes, EnableFloatingIp и EnableTcpReset.</span><span class="sxs-lookup"><span data-stu-id="3c38d-241">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="3c38d-242">LoadBalancerInboundNatRuleConfig: добавлен параметр EnableTcpReset.</span><span class="sxs-lookup"><span data-stu-id="3c38d-242">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="3c38d-243">LoadBalancerRuleConfig: добавлен параметр EnableTcpReset.</span><span class="sxs-lookup"><span data-stu-id="3c38d-243">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="3c38d-244">LoadBalancerProbeConfig: добавлена поддержка значения Https для параметра Protocol.</span><span class="sxs-lookup"><span data-stu-id="3c38d-244">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="3c38d-245">Добавлены новые команды для нового правила OutboundRule подресурса LoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="3c38d-245">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="3c38d-246">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3c38d-246">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="3c38d-247">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3c38d-247">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="3c38d-248">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3c38d-248">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="3c38d-249">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3c38d-249">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="3c38d-250">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3c38d-250">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="3c38d-251">Добавлено новое свойство HostedWorkloads для PSNetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="3c38d-251">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="3c38d-252">Добавлены новые командлеты для функции Брандмауэра Azure через ARM.</span><span class="sxs-lookup"><span data-stu-id="3c38d-252">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="3c38d-253">Добавлен командлет Get-AzureRmFirewall.</span><span class="sxs-lookup"><span data-stu-id="3c38d-253">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="3c38d-254">Добавлен командлет Set-AzureRmFirewall.</span><span class="sxs-lookup"><span data-stu-id="3c38d-254">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="3c38d-255">Добавлен командлет New-AzureRmFirewall.</span><span class="sxs-lookup"><span data-stu-id="3c38d-255">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="3c38d-256">Добавлен командлет Remove-AzureRmFirewall.</span><span class="sxs-lookup"><span data-stu-id="3c38d-256">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="3c38d-257">Добавлен командлет New-AzureRmFirewallApplicationRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="3c38d-257">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="3c38d-258">Добавлен командлет New-AzureRmFirewallApplicationRule.</span><span class="sxs-lookup"><span data-stu-id="3c38d-258">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="3c38d-259">Добавлен командлет New-AzureRmFirewallNatRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="3c38d-259">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="3c38d-260">Добавлен командлет New-AzureRmFirewallNatRule.</span><span class="sxs-lookup"><span data-stu-id="3c38d-260">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="3c38d-261">Добавлен командлет New-AzureRmFirewallNetworkRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="3c38d-261">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="3c38d-262">Добавлен командлет New-AzureRmFirewallNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="3c38d-262">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="3c38d-263">Добавлена поддержка конфигурации для доверенного корневого сертификата и автомасштабирования в Шлюзе приложений.</span><span class="sxs-lookup"><span data-stu-id="3c38d-263">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="3c38d-264">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="3c38d-264">New Cmdlets added:</span></span>
      - <span data-ttu-id="3c38d-265">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="3c38d-265">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="3c38d-266">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="3c38d-266">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="3c38d-267">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="3c38d-267">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="3c38d-268">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="3c38d-268">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="3c38d-269">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="3c38d-269">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="3c38d-270">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="3c38d-270">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="3c38d-271">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="3c38d-271">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="3c38d-272">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="3c38d-272">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="3c38d-273">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="3c38d-273">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="3c38d-274">В следующие командлеты добавлен необязательный параметр -TrustedRootCertificate:</span><span class="sxs-lookup"><span data-stu-id="3c38d-274">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="3c38d-275">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3c38d-275">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="3c38d-276">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3c38d-276">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="3c38d-277">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="3c38d-277">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="3c38d-278">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="3c38d-278">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="3c38d-279">В следующие командлеты добавлен необязательный параметр -AutoscaleConfiguration:</span><span class="sxs-lookup"><span data-stu-id="3c38d-279">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="3c38d-280">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3c38d-280">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="3c38d-281">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3c38d-281">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="3c38d-282">Добавлен командлет для конечной точки интерфейса Get-AzureInterfaceEndpoint.</span><span class="sxs-lookup"><span data-stu-id="3c38d-282">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="3c38d-283">Добавлена поддержка нескольких префиксов адресов в подсети.</span><span class="sxs-lookup"><span data-stu-id="3c38d-283">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="3c38d-284">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="3c38d-284">Updated cmdlets:</span></span>
  - <span data-ttu-id="3c38d-285">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="3c38d-285">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="3c38d-286">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="3c38d-286">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="3c38d-287">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="3c38d-287">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="3c38d-288">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="3c38d-288">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="3c38d-289">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="3c38d-289">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="3c38d-290">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="3c38d-290">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="3c38d-291">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="3c38d-291">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="3c38d-292">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="3c38d-292">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="3c38d-293">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="3c38d-293">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="3c38d-294">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="3c38d-294">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="3c38d-295">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="3c38d-295">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="3c38d-296">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3c38d-296">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="3c38d-297">New-AzureRmNetworkInterfaceIpConfig — Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3c38d-297">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="3c38d-298">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="3c38d-298">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="3c38d-299">Add-AzureRmVirtualNetworkGatewayIpConfig;</span><span class="sxs-lookup"><span data-stu-id="3c38d-299">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="3c38d-300">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="3c38d-300">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="3c38d-301">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="3c38d-301">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="3c38d-302">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="3c38d-302">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="3c38d-303">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3c38d-303">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="3c38d-304">Добавлены командлеты для делегирования подсети.</span><span class="sxs-lookup"><span data-stu-id="3c38d-304">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="3c38d-305">New-AzureRmDelegation — создает делегирование, которое можно добавить к подсети.</span><span class="sxs-lookup"><span data-stu-id="3c38d-305">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="3c38d-306">Remove-AzureRmDelegation — принимает подсеть и удаляет указанное имя делегирования из этой подсети.</span><span class="sxs-lookup"><span data-stu-id="3c38d-306">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="3c38d-307">Add-AzureRmDelegation — принимает подсеть и добавляет указанное имя службы в качестве делегирования для этой подсети.</span><span class="sxs-lookup"><span data-stu-id="3c38d-307">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="3c38d-308">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="3c38d-308">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="3c38d-309">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="3c38d-309">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="3c38d-310">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="3c38d-310">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="3c38d-311">Добавлена поддержка управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="3c38d-311">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="3c38d-312">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="3c38d-312">AzureRM.RedisCache</span></span>
* <span data-ttu-id="3c38d-313">Обновлена зависимость Insights.</span><span class="sxs-lookup"><span data-stu-id="3c38d-313">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="3c38d-314">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="3c38d-314">AzureRM.Resources</span></span>
* <span data-ttu-id="3c38d-315">В командлет New-AzureRmResourceGroupDeployment добавлен новый параметр RollbackAction.</span><span class="sxs-lookup"><span data-stu-id="3c38d-315">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="3c38d-316">Добавлена поддержка OnErrorDeployment с новым параметром.</span><span class="sxs-lookup"><span data-stu-id="3c38d-316">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="3c38d-317">Добавлена поддержка управляемого удостоверения при назначении политик.</span><span class="sxs-lookup"><span data-stu-id="3c38d-317">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="3c38d-318">При назначении политики с помощью New-AzureRmPolicyAssignment параметры со значениями по умолчанию больше не требуются.</span><span class="sxs-lookup"><span data-stu-id="3c38d-318">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="3c38d-319">Добавлен новый командлет Get-AzureRmPolicyAlias для получения псевдонимов политик.</span><span class="sxs-lookup"><span data-stu-id="3c38d-319">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="3c38d-320">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3c38d-320">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="3c38d-321">Устранена проблема № 7161.</span><span class="sxs-lookup"><span data-stu-id="3c38d-321">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="3c38d-322">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="3c38d-322">AzureRM.SignalR</span></span>
* <span data-ttu-id="3c38d-323">Обновлены номера SKU для Free_F1 и Standard_S1.</span><span class="sxs-lookup"><span data-stu-id="3c38d-323">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="3c38d-324">Добавлены поле версии в объект PSSignalRResource и строка подключения в объект PSSignalRKeys.</span><span class="sxs-lookup"><span data-stu-id="3c38d-324">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="3c38d-325">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="3c38d-325">AzureRM.Storage</span></span>
* <span data-ttu-id="3c38d-326">Добавлена поддержка политики неизменяемости в AzureRm.Storage.</span><span class="sxs-lookup"><span data-stu-id="3c38d-326">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="3c38d-327">Remove-AzureRmStorageAccountNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="3c38d-327">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="3c38d-328">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3c38d-328">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="3c38d-329">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3c38d-329">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="3c38d-330">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3c38d-330">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="3c38d-331">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3c38d-331">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="3c38d-332">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="3c38d-332">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="3c38d-333">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="3c38d-333">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="3c38d-334">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="3c38d-334">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="3c38d-335">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="3c38d-335">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="3c38d-336">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="3c38d-336">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="3c38d-337">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="3c38d-337">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="3c38d-338">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="3c38d-338">AzureRM.Websites</span></span>
* <span data-ttu-id="3c38d-339">Добавлены два новых командлета: Get-AzureRmDeletedWebApp и Restore-AzureRmDeletedWebApp.</span><span class="sxs-lookup"><span data-stu-id="3c38d-339">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="3c38d-340">New-AzureRmAppServicePlan: добавлен параметр -HyperV для создания плана службы приложений с контейнером Windows.</span><span class="sxs-lookup"><span data-stu-id="3c38d-340">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="3c38d-341">New-AzureRmWebApp, New-AzureRmWebAppSlot, Set-AzureRmWebApp, Set-AzureRmWebAppSlot: добавлены новые параметры (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) для создания контейнера приложения Windows и управления им.</span><span class="sxs-lookup"><span data-stu-id="3c38d-341">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="3c38d-342">6.8.1 — август 2018 г.</span><span class="sxs-lookup"><span data-stu-id="3c38d-342">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="3c38d-343">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="3c38d-343">General</span></span>
* <span data-ttu-id="3c38d-344">Исправлена проблема с отсутствием настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3c38d-344">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="3c38d-345">Обновлены общие сборки среды выполнения</span><span class="sxs-lookup"><span data-stu-id="3c38d-345">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="3c38d-346">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3c38d-346">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="3c38d-347">Исправлена проблема с отсутствием настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3c38d-347">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="3c38d-348">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6603.</span><span class="sxs-lookup"><span data-stu-id="3c38d-348">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="3c38d-349">Командлеты Import-AzureRmApiManagementApi и \*-AzureRmApiManagementCertificate теперь обрабатывают относительные пути.</span><span class="sxs-lookup"><span data-stu-id="3c38d-349">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="3c38d-350">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6879.</span><span class="sxs-lookup"><span data-stu-id="3c38d-350">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="3c38d-351">CertificateInformation — это задаваемое свойство, обеспечивающее правильную работу командлета Set-AzureRmApiManagement.</span><span class="sxs-lookup"><span data-stu-id="3c38d-351">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="3c38d-352">Проблема исправлена путем обновления пакета NuGet до версии 4.0.4-preview.</span><span class="sxs-lookup"><span data-stu-id="3c38d-352">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="3c38d-353">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6853.</span><span class="sxs-lookup"><span data-stu-id="3c38d-353">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="3c38d-354">Исправлен фильтр OData для поиска по имени продукта.</span><span class="sxs-lookup"><span data-stu-id="3c38d-354">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="3c38d-355">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6814.</span><span class="sxs-lookup"><span data-stu-id="3c38d-355">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="3c38d-356">Исправлен фильтр OData для поиска по имени API.</span><span class="sxs-lookup"><span data-stu-id="3c38d-356">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="3c38d-357">Добавлена поддержка средства ведения журнала Azure Monitor.</span><span class="sxs-lookup"><span data-stu-id="3c38d-357">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="3c38d-358">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="3c38d-358">AzureRM.Compute</span></span>
* <span data-ttu-id="3c38d-359">Исправлена проблема с отсутствием в выходных данных ошибки целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="3c38d-359">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="3c38d-360">Исправлена проблема с типом учетной записи хранения для виртуальной машины с управляемым диском.</span><span class="sxs-lookup"><span data-stu-id="3c38d-360">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="3c38d-361">Исправлена проблема с отсутствием настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3c38d-361">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="3c38d-362">Исправлены командлеты расширения AEM для других сред, например Azure для Китая.</span><span class="sxs-lookup"><span data-stu-id="3c38d-362">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="3c38d-363">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="3c38d-363">AzureRM.Network</span></span>
* <span data-ttu-id="3c38d-364">Стандартное представление выходных данных командлетов изменено на представление таблиц.</span><span class="sxs-lookup"><span data-stu-id="3c38d-364">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="3c38d-365">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="3c38d-365">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="3c38d-366">Исправлена проблема с Update-AzureRmPowerBIEmbeddedCapacity при попытке масштабировать приостановленную емкость.</span><span class="sxs-lookup"><span data-stu-id="3c38d-366">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="3c38d-367">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="3c38d-367">AzureRM.Resources</span></span>
* <span data-ttu-id="3c38d-368">Исправлена проблема с созданием управляемых приложений из Marketplace.</span><span class="sxs-lookup"><span data-stu-id="3c38d-368">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="3c38d-369">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3c38d-369">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="3c38d-370">Исправленные проблемы</span><span class="sxs-lookup"><span data-stu-id="3c38d-370">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="3c38d-371">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="3c38d-371">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="3c38d-372">Добавлена поддержка метода маршрутизации MultiValue.</span><span class="sxs-lookup"><span data-stu-id="3c38d-372">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="3c38d-373">Добавлен новый параметр MaxReturn для маршрутизации MultiValue.</span><span class="sxs-lookup"><span data-stu-id="3c38d-373">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="3c38d-374">Добавлена поддержка метода маршрутизации Subnet.</span><span class="sxs-lookup"><span data-stu-id="3c38d-374">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="3c38d-375">Добавлена поддержка диапазонов IP-адресов (подсетей) в конечных точках.</span><span class="sxs-lookup"><span data-stu-id="3c38d-375">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="3c38d-376">Добавлена поддержка пользовательских заголовков в профилях.</span><span class="sxs-lookup"><span data-stu-id="3c38d-376">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="3c38d-377">Добавлена поддержка диапазонов кода ожидаемого состояния в профилях.</span><span class="sxs-lookup"><span data-stu-id="3c38d-377">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="3c38d-378">Добавлена поддержка пользовательских заголовков в конечных точках.</span><span class="sxs-lookup"><span data-stu-id="3c38d-378">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="3c38d-379">6.8.0 — август 2018 г.</span><span class="sxs-lookup"><span data-stu-id="3c38d-379">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="3c38d-380">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="3c38d-380">General</span></span>
* <span data-ttu-id="3c38d-381">Исправлена проблема с отсутствием настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3c38d-381">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="3c38d-382">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="3c38d-382">AzureRM.Profile</span></span>
* <span data-ttu-id="3c38d-383">Добавлено свойство срока действия для маркеров, возвращенных при выполнении Connect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="3c38d-383">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="3c38d-384">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="3c38d-384">AzureRM.Compute</span></span>
* <span data-ttu-id="3c38d-385">Исправлена проблема с отсутствием в выходных данных ошибки целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="3c38d-385">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="3c38d-386">Исправлена проблема с типом учетной записи хранения для виртуальной машины с управляемым диском.</span><span class="sxs-lookup"><span data-stu-id="3c38d-386">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="3c38d-387">Исправлены командлеты расширения AEM для других сред, например Azure для Китая.</span><span class="sxs-lookup"><span data-stu-id="3c38d-387">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="3c38d-388">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="3c38d-388">AzureRM.IotHub</span></span>
* <span data-ttu-id="3c38d-389">Исправлены примеры для New-AzureRmIotHubExportDevices и New-AzureRmIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="3c38d-389">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="3c38d-390">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="3c38d-390">AzureRM.Network</span></span>
* <span data-ttu-id="3c38d-391">Изменено представление моделей по умолчанию на представление таблиц.</span><span class="sxs-lookup"><span data-stu-id="3c38d-391">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="3c38d-392">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="3c38d-392">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="3c38d-393">Исправлена проблема с Update-AzureRmPowerBIEmbeddedCapacity при попытке масштабировать приостановленную емкость.</span><span class="sxs-lookup"><span data-stu-id="3c38d-393">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="3c38d-394">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="3c38d-394">AzureRM.Resources</span></span>
* <span data-ttu-id="3c38d-395">Исправлена проблема с созданием управляемого приложения из marketplace.</span><span class="sxs-lookup"><span data-stu-id="3c38d-395">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="3c38d-396">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3c38d-396">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="3c38d-397">Исправления проблем</span><span class="sxs-lookup"><span data-stu-id="3c38d-397">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="3c38d-398">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="3c38d-398">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="3c38d-399">Добавлена поддержка метода маршрутизации MultiValue.</span><span class="sxs-lookup"><span data-stu-id="3c38d-399">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="3c38d-400">Добавлен новый параметр MaxReturn для маршрутизации MultiValue.</span><span class="sxs-lookup"><span data-stu-id="3c38d-400">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="3c38d-401">Добавлена поддержка метода маршрутизации Subnet.</span><span class="sxs-lookup"><span data-stu-id="3c38d-401">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="3c38d-402">Добавлена поддержка диапазонов IP-адресов (подсетей) в конечных точках.</span><span class="sxs-lookup"><span data-stu-id="3c38d-402">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="3c38d-403">Добавлена поддержка пользовательских заголовков в профилях.</span><span class="sxs-lookup"><span data-stu-id="3c38d-403">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="3c38d-404">Добавлена поддержка диапазонов кода состояния ожидания в профилях.</span><span class="sxs-lookup"><span data-stu-id="3c38d-404">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="3c38d-405">Добавлена поддержка пользовательских заголовков в конечных точках.</span><span class="sxs-lookup"><span data-stu-id="3c38d-405">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="3c38d-406">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="3c38d-406">AzureRM.Websites</span></span>
* <span data-ttu-id="3c38d-407">Исправлена проблема с отсутствием правильной настройки группы ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3c38d-407">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="3c38d-408">6.7.0 — август 2018 г.</span><span class="sxs-lookup"><span data-stu-id="3c38d-408">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="3c38d-409">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="3c38d-409">AzureRM.Profile</span></span>
* <span data-ttu-id="3c38d-410">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-410">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="3c38d-411">Добавлен идентификатор пользователя для имени контекста по умолчанию, чтобы избежать конфликтов контекста.</span><span class="sxs-lookup"><span data-stu-id="3c38d-411">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="3c38d-412">Устранены проблемы с командлетом Clear-AzureRmContext, которые приводили к проблемам с выбором контекста #6398.</span><span class="sxs-lookup"><span data-stu-id="3c38d-412">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="3c38d-413">Разрешено передавать домен клиента в параметр -TenantId для командлета Connect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="3c38d-413">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="3c38d-414">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="3c38d-414">Azure.Storage</span></span>
* <span data-ttu-id="3c38d-415">Удалено ограничение в 5 ТБ для квоты на общую папку Azure.</span><span class="sxs-lookup"><span data-stu-id="3c38d-415">Remove the 5TB limitation for Azure File Share quota</span></span>
* <span data-ttu-id="3c38d-416">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="3c38d-416">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="3c38d-417">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3c38d-417">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="3c38d-418">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-418">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="3c38d-419">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3c38d-419">Azure.AnalysisServices</span></span>
* <span data-ttu-id="3c38d-420">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-420">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="3c38d-421">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3c38d-421">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="3c38d-422">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-422">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="3c38d-423">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="3c38d-423">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="3c38d-424">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-424">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="3c38d-425">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="3c38d-425">AzureRM.Automation</span></span>
* <span data-ttu-id="3c38d-426">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-426">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="3c38d-427">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="3c38d-427">AzureRM.Backup</span></span>
* <span data-ttu-id="3c38d-428">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-428">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="3c38d-429">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="3c38d-429">AzureRM.Batch</span></span>
* <span data-ttu-id="3c38d-430">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-430">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="3c38d-431">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="3c38d-431">AzureRM.Billing</span></span>
* <span data-ttu-id="3c38d-432">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-432">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="3c38d-433">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="3c38d-433">AzureRM.Cdn</span></span>
* <span data-ttu-id="3c38d-434">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-434">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="3c38d-435">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3c38d-435">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="3c38d-436">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-436">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="3c38d-437">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="3c38d-437">AzureRM.Compute</span></span>
* <span data-ttu-id="3c38d-438">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-438">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="3c38d-439">В командлет New-AzureRmVmssConfig добавлен параметр EvictionPolicy.</span><span class="sxs-lookup"><span data-stu-id="3c38d-439">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="3c38d-440">Если расположение не указано, используйте в DiskFileParameterSet для New AzureRmVm расположение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3c38d-440">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="3c38d-441">Исправлено описание параметров в Save-AzureRmVMImage.</span><span class="sxs-lookup"><span data-stu-id="3c38d-441">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="3c38d-442">Исправлен командлет Get-AzureRmVMDiskEncryptionStatus для определенных сценариев, связанных с однократным выполнением.</span><span class="sxs-lookup"><span data-stu-id="3c38d-442">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="3c38d-443">AzureRM.Consumption:</span><span class="sxs-lookup"><span data-stu-id="3c38d-443">AzureRM.Consumption</span></span>
* <span data-ttu-id="3c38d-444">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-444">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="3c38d-445">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="3c38d-445">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="3c38d-446">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-446">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="3c38d-447">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="3c38d-447">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="3c38d-448">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-448">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="3c38d-449">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="3c38d-449">AzureRM.DataFactories</span></span>
* <span data-ttu-id="3c38d-450">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-450">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="3c38d-451">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="3c38d-451">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="3c38d-452">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-452">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="3c38d-453">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="3c38d-453">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="3c38d-454">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-454">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="3c38d-455">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3c38d-455">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="3c38d-456">Исправлена отладка, когда DebugPreference настраивается из командной строки PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3c38d-456">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="3c38d-457">Обновлен пример для Set-AzureRmDataLakeStoreItemAcl.</span><span class="sxs-lookup"><span data-stu-id="3c38d-457">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="3c38d-458">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-458">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="3c38d-459">Обновлен пример для Set-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="3c38d-459">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="3c38d-460">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="3c38d-460">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="3c38d-461">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-461">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="3c38d-462">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="3c38d-462">AzureRM.Dns</span></span>
* <span data-ttu-id="3c38d-463">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-463">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="3c38d-464">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="3c38d-464">AzureRM.EventGrid</span></span>
* <span data-ttu-id="3c38d-465">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-465">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="3c38d-466">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="3c38d-466">AzureRM.EventHub</span></span>
* <span data-ttu-id="3c38d-467">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-467">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="3c38d-468">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="3c38d-468">AzureRM.HDInsight</span></span>
* <span data-ttu-id="3c38d-469">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-469">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="3c38d-470">AzureRM.Insights;</span><span class="sxs-lookup"><span data-stu-id="3c38d-470">AzureRM.Insights</span></span>
* <span data-ttu-id="3c38d-471">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-471">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="3c38d-472">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="3c38d-472">AzureRM.IotHub</span></span>
* <span data-ttu-id="3c38d-473">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-473">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="3c38d-474">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3c38d-474">AzureRM.KeyVault</span></span>
* <span data-ttu-id="3c38d-475">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-475">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="3c38d-476">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="3c38d-476">AzureRM.LogicApp</span></span>
* <span data-ttu-id="3c38d-477">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-477">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="3c38d-478">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="3c38d-478">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="3c38d-479">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-479">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="3c38d-480">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="3c38d-480">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="3c38d-481">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-481">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="3c38d-482">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="3c38d-482">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="3c38d-483">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-483">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="3c38d-484">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="3c38d-484">AzureRM.Media</span></span>
* <span data-ttu-id="3c38d-485">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-485">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="3c38d-486">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="3c38d-486">AzureRM.Network</span></span>
* <span data-ttu-id="3c38d-487">Добавлен пример для Set-AzureRmLocalNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="3c38d-487">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="3c38d-488">Добавлены примеры и описания для Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey и New-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="3c38d-488">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="3c38d-489">Добавлены примеры для Remove-AzureRmVirtualNetworkGatewayIpConfig и Reset-AzureRmVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="3c38d-489">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="3c38d-490">Добавлен пример для Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.</span><span class="sxs-lookup"><span data-stu-id="3c38d-490">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="3c38d-491">Добавлен пример для Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.</span><span class="sxs-lookup"><span data-stu-id="3c38d-491">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="3c38d-492">Добавлен пример для Set-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="3c38d-492">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="3c38d-493">Повторно созданы командлеты для ApplicationSecurityGroup, RouteTable и Usage с помощью генератора кода последней версии.</span><span class="sxs-lookup"><span data-stu-id="3c38d-493">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="3c38d-494">Уточнено сообщение об ошибке для Get-AzureRmVirtualNetworkSubnetConfig при попытке получить подсеть, которая не существует.</span><span class="sxs-lookup"><span data-stu-id="3c38d-494">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="3c38d-495">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="3c38d-495">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="3c38d-496">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-496">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="3c38d-497">AzureRM.OperationalInsights;</span><span class="sxs-lookup"><span data-stu-id="3c38d-497">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="3c38d-498">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-498">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="3c38d-499">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="3c38d-499">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="3c38d-500">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-500">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="3c38d-501">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="3c38d-501">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="3c38d-502">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-502">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="3c38d-503">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3c38d-503">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="3c38d-504">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-504">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="3c38d-505">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="3c38d-505">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="3c38d-506">Добавлен фильтр политик для командлета Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="3c38d-506">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="3c38d-507">Команда возвращает список элементов резервного копирования, защищенных политикой с заданным идентификатором.</span><span class="sxs-lookup"><span data-stu-id="3c38d-507">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="3c38d-508">Обновление Microsoft.Azure.Management.RecoveryServices.Backup до версии 3.0.0-preview.</span><span class="sxs-lookup"><span data-stu-id="3c38d-508">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="3c38d-509">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-509">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="3c38d-510">Добавлен параметр TargetResourceGroupName для Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="3c38d-510">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="3c38d-511">Группа ресурсов, в которую восстанавливаются управляемые диски.</span><span class="sxs-lookup"><span data-stu-id="3c38d-511">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="3c38d-512">Применимо к резервной копии виртуальной машины с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="3c38d-512">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="3c38d-513">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="3c38d-513">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="3c38d-514">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-514">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="3c38d-515">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="3c38d-515">AzureRM.RedisCache</span></span>
* <span data-ttu-id="3c38d-516">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-516">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="3c38d-517">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="3c38d-517">AzureRM.Relay</span></span>
* <span data-ttu-id="3c38d-518">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-518">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="3c38d-519">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="3c38d-519">AzureRM.Resources</span></span>
* <span data-ttu-id="3c38d-520">Поддержка развертывания шаблонов в области подписки.</span><span class="sxs-lookup"><span data-stu-id="3c38d-520">Support template deployment at subscription scope.</span></span> <span data-ttu-id="3c38d-521">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="3c38d-521">Add new Cmdlets:</span></span>
    - <span data-ttu-id="3c38d-522">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="3c38d-522">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="3c38d-523">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="3c38d-523">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="3c38d-524">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="3c38d-524">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="3c38d-525">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="3c38d-525">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="3c38d-526">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="3c38d-526">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="3c38d-527">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="3c38d-527">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="3c38d-528">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="3c38d-528">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="3c38d-529">Устранена проблема, когда при передаче контекста в Set-AzureRmResource возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="3c38d-529">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="3c38d-530">Исправлен пример в New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="3c38d-530">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="3c38d-531">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-531">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="3c38d-532">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="3c38d-532">AzureRM.Scheduler</span></span>
* <span data-ttu-id="3c38d-533">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-533">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="3c38d-534">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3c38d-534">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="3c38d-535">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-535">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="3c38d-536">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3c38d-536">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="3c38d-537">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-537">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="3c38d-538">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="3c38d-538">AzureRM.Sql</span></span>
* <span data-ttu-id="3c38d-539">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-539">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="3c38d-540">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="3c38d-540">AzureRM.Storage</span></span>
* <span data-ttu-id="3c38d-541">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-541">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="3c38d-542">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="3c38d-542">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="3c38d-543">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-543">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="3c38d-544">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="3c38d-544">AzureRM.Tags</span></span>
* <span data-ttu-id="3c38d-545">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-545">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="3c38d-546">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="3c38d-546">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="3c38d-547">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-547">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="3c38d-548">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="3c38d-548">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="3c38d-549">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-549">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="3c38d-550">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="3c38d-550">AzureRM.Websites</span></span>
* <span data-ttu-id="3c38d-551">Обновление до последней версии Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-551">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="3c38d-552">6.6.0 — июль 2018 г.</span><span class="sxs-lookup"><span data-stu-id="3c38d-552">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="3c38d-553">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="3c38d-553">General</span></span>
* <span data-ttu-id="3c38d-554">Обновлены все файлы справки: включены полные типы параметров и исправлены типы входных и выходных данных.</span><span class="sxs-lookup"><span data-stu-id="3c38d-554">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="3c38d-555">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="3c38d-555">AzureRM.Profile</span></span>
* <span data-ttu-id="3c38d-556">Обновлена библиотека Common.Strategy: теперь можно проверить, совместима ли текущая конфигурация ресурса с целевым ресурсом.</span><span class="sxs-lookup"><span data-stu-id="3c38d-556">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="3c38d-557">В Common.Storage добавлены типы ps1xml.</span><span class="sxs-lookup"><span data-stu-id="3c38d-557">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="3c38d-558">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="3c38d-558">Azure.Storage</span></span>
* <span data-ttu-id="3c38d-559">Добавлена поддержка для получения контекста хранилища из DefaultProfile.</span><span class="sxs-lookup"><span data-stu-id="3c38d-559">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="3c38d-560">В свойства типов выходных данных командлетов добавлен атрибут Ps1XmlAttribute.</span><span class="sxs-lookup"><span data-stu-id="3c38d-560">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="3c38d-561">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3c38d-561">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="3c38d-562">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6370.</span><span class="sxs-lookup"><span data-stu-id="3c38d-562">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="3c38d-563">В AutoMapper исправлена ошибка, препятствовавшая преобразованию PsApiManagementApi в ApiContract.</span><span class="sxs-lookup"><span data-stu-id="3c38d-563">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="3c38d-564">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6515.</span><span class="sxs-lookup"><span data-stu-id="3c38d-564">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="3c38d-565">В File.Save исправлена ошибка, связанная с перегрузкой типом кодировки.</span><span class="sxs-lookup"><span data-stu-id="3c38d-565">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="3c38d-566">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6560.</span><span class="sxs-lookup"><span data-stu-id="3c38d-566">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="3c38d-567">Выполнено обновление до версии NuGet 4.0.3, что позволило исправить исключение шаблона в apiId.</span><span class="sxs-lookup"><span data-stu-id="3c38d-567">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="3c38d-568">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="3c38d-568">AzureRM.Compute</span></span>
* <span data-ttu-id="3c38d-569">Устранена ошибка при создании виртуальной машины с помощью командлета New-AzureRmVm и параметра DiskFileParameterSet, которая возникала из-за переименования типа учетной записи хранения PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="3c38d-569">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="3c38d-570">Исправлен командлет Invoke-AzureRmVMRunCommand.</span><span class="sxs-lookup"><span data-stu-id="3c38d-570">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="3c38d-571">Командлет Get-AzureRmAvailabilitySet теперь может выводить список всех групп доступности в подписке.</span><span class="sxs-lookup"><span data-stu-id="3c38d-571">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="3c38d-572">(Параметр ResouceGroupName теперь является необязательным.)</span><span class="sxs-lookup"><span data-stu-id="3c38d-572">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="3c38d-573">Обновлен параметр SimpleParameterSet командлета New-AzureRmVm, что позволило использовать ускоренную сеть на соответствующих виртуальных машинах.</span><span class="sxs-lookup"><span data-stu-id="3c38d-573">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="3c38d-574">Обновлен простой набор параметров New-AzureRmVmss, что позволило отменять создание масштабируемого набора виртуальных машин, если указанная пользователем подсистема балансировки нагрузки уже существует.</span><span class="sxs-lookup"><span data-stu-id="3c38d-574">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="3c38d-575">Обновлен пример для New-AzureRmDisk.</span><span class="sxs-lookup"><span data-stu-id="3c38d-575">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="3c38d-576">Добавлен пример для New-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="3c38d-576">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="3c38d-577">Обновлено описание командлета Set-AzureRmVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="3c38d-577">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="3c38d-578">Обновлен пример 1 для Set-AzureRmVMBginfoExtension: исправлены орфографические ошибки и префикс.</span><span class="sxs-lookup"><span data-stu-id="3c38d-578">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="3c38d-579">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="3c38d-579">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="3c38d-580">Пакет .NET SDK для ADF обновлен до версии 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="3c38d-580">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="3c38d-581">Добавлена поддержка совместного использования локальной среды IR несколькими фабриками данных.</span><span class="sxs-lookup"><span data-stu-id="3c38d-581">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="3c38d-582">Добавлен новый параметр -SharedIntegrationRuntimeResourceId для командлета Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-582">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="3c38d-583">Добавлен новый необязательный параметр -LinkedDataFactoryName для командлета Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="3c38d-583">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="3c38d-584">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3c38d-584">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="3c38d-585">Пакет SDK для плоскости данных (Microsoft.Azure.DataLake.Store) обновлен до версии 1.1.9.</span><span class="sxs-lookup"><span data-stu-id="3c38d-585">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="3c38d-586">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="3c38d-586">AzureRM.EventHub</span></span>
* <span data-ttu-id="3c38d-587">Обновлена конвейерная передача для InputObject и ResourceId в командлетах remove.</span><span class="sxs-lookup"><span data-stu-id="3c38d-587">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="3c38d-588">AzureRM.Insights;</span><span class="sxs-lookup"><span data-stu-id="3c38d-588">AzureRM.Insights</span></span>
* <span data-ttu-id="3c38d-589">Исправлено форматирование OutputType в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="3c38d-589">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="3c38d-590">Применен пакет SDK Microsoft.Azure.Management.Monitor 0.19.1-preview.</span><span class="sxs-lookup"><span data-stu-id="3c38d-590">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="3c38d-591">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3c38d-591">AzureRM.KeyVault</span></span>
* <span data-ttu-id="3c38d-592">Исправлена проблема с конвейерной передачей в командлете Set-AzureRmKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="3c38d-592">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="3c38d-593">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="3c38d-593">AzureRM.Network</span></span>
* <span data-ttu-id="3c38d-594">Добавлены примеры для командлетов LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="3c38d-594">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="3c38d-595">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="3c38d-595">AzureRM.Resources</span></span>
* <span data-ttu-id="3c38d-596">Устранена проблема, возникавшая при указании имени и значения тега для Get-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="3c38d-596">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="3c38d-597">Исправлен сценарий конвейерной передачи в Set-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="3c38d-597">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="3c38d-598">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3c38d-598">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="3c38d-599">Обновлена конвейерная передача для InputObject и ResourceId в командлетах remove.</span><span class="sxs-lookup"><span data-stu-id="3c38d-599">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="3c38d-600">Исправлено несколько ошибок.</span><span class="sxs-lookup"><span data-stu-id="3c38d-600">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="3c38d-601">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="3c38d-601">AzureRM.Sql</span></span>
* <span data-ttu-id="3c38d-602">Добавлена поддержка Advanced Threat Protection для сервера с помощью следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="3c38d-602">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="3c38d-603">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="3c38d-603">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="3c38d-604">Добавлена поддержка оценки уязвимостей с помощью следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="3c38d-604">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="3c38d-605">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings;</span><span class="sxs-lookup"><span data-stu-id="3c38d-605">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="3c38d-606">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline;</span><span class="sxs-lookup"><span data-stu-id="3c38d-606">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="3c38d-607">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan.</span><span class="sxs-lookup"><span data-stu-id="3c38d-607">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="3c38d-608">Исправлен пример для Remove-AzureRmSqlServerFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="3c38d-608">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="3c38d-609">Исправлена неправильная обработка даты и времени для базового языка и региональных параметров, отличных от США, в Get-AzureSqlSyncGroupLog.</span><span class="sxs-lookup"><span data-stu-id="3c38d-609">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="3c38d-610">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="3c38d-610">AzureRM.Storage</span></span>
* <span data-ttu-id="3c38d-611">В свойства типов выходных данных командлетов добавлен атрибут Ps1XmlAttribute.</span><span class="sxs-lookup"><span data-stu-id="3c38d-611">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="3c38d-612">Выходные данные командлетов StorageAccount теперь отображаются в виде таблицы.</span><span class="sxs-lookup"><span data-stu-id="3c38d-612">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="3c38d-613">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3c38d-613">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="3c38d-614">New-AzureRmStorageAccount;</span><span class="sxs-lookup"><span data-stu-id="3c38d-614">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="3c38d-615">Set-AzureRmStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="3c38d-615">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="3c38d-616">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="3c38d-616">AzureRM.Tags</span></span>
* <span data-ttu-id="3c38d-617">Удалено неверное утверждение из справки по командлетам Tag.</span><span class="sxs-lookup"><span data-stu-id="3c38d-617">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="3c38d-618">6.5.0 — июль 2018 г.</span><span class="sxs-lookup"><span data-stu-id="3c38d-618">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="3c38d-619">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="3c38d-619">AzureRM.Profile</span></span>
* <span data-ttu-id="3c38d-620">Обновлена справка для командлета Get-AzureRmContextAutosaveSetting.</span><span class="sxs-lookup"><span data-stu-id="3c38d-620">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="3c38d-621">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="3c38d-621">Azure.Storage</span></span>
* <span data-ttu-id="3c38d-622">Добавлена поддержка отправки BLOB-объекта или файла с помощью токена SAS, доступного только для записи.</span><span class="sxs-lookup"><span data-stu-id="3c38d-622">Support Upload Blob or File with write only Sas token</span></span>
* <span data-ttu-id="3c38d-623">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="3c38d-623">Set-AzureStorageBlobContent</span></span>
* <span data-ttu-id="3c38d-624">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="3c38d-624">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="3c38d-625">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3c38d-625">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="3c38d-626">Для AS добавлено обязательное свойство ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="3c38d-626">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="3c38d-627">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="3c38d-627">AzureRM.Automation</span></span>
* <span data-ttu-id="3c38d-628">Обновлена справка и добавлены примеры для командлета New-AzureRMAutomationSchedule.</span><span class="sxs-lookup"><span data-stu-id="3c38d-628">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="3c38d-629">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="3c38d-629">AzureRM.Compute</span></span>
* <span data-ttu-id="3c38d-630">Добавлен параметр -Tag для командлета Update/New-AzureRmAvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="3c38d-630">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="3c38d-631">Добавлен пример для командлета Add-AzureRmVmssExtension.</span><span class="sxs-lookup"><span data-stu-id="3c38d-631">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="3c38d-632">Добавлены примеры для командлета Remove-AzureRmVmssExtension.</span><span class="sxs-lookup"><span data-stu-id="3c38d-632">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="3c38d-633">Обновлена справка для командлета Set-AzureRmVMAccessExtension.</span><span class="sxs-lookup"><span data-stu-id="3c38d-633">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="3c38d-634">Изменен класс SimpleParameterSet для командлета New-AzureRmVmss: теперь для SinglePlacementGroup по умолчанию задается значение false, а также добавляется параметр-переключатель SinglePlacementGroup, который позволяет пользователю создать VMSS в одной группе размещения.</span><span class="sxs-lookup"><span data-stu-id="3c38d-634">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="3c38d-635">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="3c38d-635">AzureRM.EventHub</span></span>
* <span data-ttu-id="3c38d-636">В класс PSEventHubDRConfigurationAttributes добавлено доступное только для чтения свойство PendingReplicationOperationsCount, которое показывает количество ожидающих репликации операций во время реплицирования.</span><span class="sxs-lookup"><span data-stu-id="3c38d-636">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="3c38d-637">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3c38d-637">AzureRM.KeyVault</span></span>
* <span data-ttu-id="3c38d-638">Обновлено сообщение об ошибке для командлета Set-AzureRmKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="3c38d-638">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="3c38d-639">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="3c38d-639">AzureRM.LogicApp</span></span>
* <span data-ttu-id="3c38d-640">Исправлена ошибка "parameter set could not be resolved" (не удалось разрешить заданный параметр) в командлете New-AzureRmLogicApp.</span><span class="sxs-lookup"><span data-stu-id="3c38d-640">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="3c38d-641">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="3c38d-641">AzureRM.Network</span></span>
* <span data-ttu-id="3c38d-642">Включен пиринг между виртуальными сетями в нескольких клиентах для командлета Set/Add-AzureRmVirtualNetworkPeering.</span><span class="sxs-lookup"><span data-stu-id="3c38d-642">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="3c38d-643">Для шлюза приложений обновлены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="3c38d-643">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="3c38d-644">New-AzureRmApplicationGateway: добавлены флаг EnableFIPS и поддержка зон.</span><span class="sxs-lookup"><span data-stu-id="3c38d-644">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="3c38d-645">New-AzureRmApplicationGatewaySku: добавлены новые номера SKU Standard_v2 и WAF_v2.</span><span class="sxs-lookup"><span data-stu-id="3c38d-645">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="3c38d-646">Set-AzureRmApplicationGatewaySku: добавлены новые номера SKU Standard_v2 и WAF_v2.</span><span class="sxs-lookup"><span data-stu-id="3c38d-646">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="3c38d-647">Командлеты RouteTable пересозданы в последней версии генератора.</span><span class="sxs-lookup"><span data-stu-id="3c38d-647">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="3c38d-648">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="3c38d-648">AzureRM.Relay</span></span>
* <span data-ttu-id="3c38d-649">Обновлены файлы Markdown, исправлена проблема с именем параметра в примере.</span><span class="sxs-lookup"><span data-stu-id="3c38d-649">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="3c38d-650">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="3c38d-650">AzureRM.Resources</span></span>
* <span data-ttu-id="3c38d-651">Обновлены командлеты Roleassignment и roledefinition:</span><span class="sxs-lookup"><span data-stu-id="3c38d-651">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="3c38d-652">Удалены лишние вызовы roledefinition, выполняемые в ходе разбиения на страницы.</span><span class="sxs-lookup"><span data-stu-id="3c38d-652">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="3c38d-653">Исправлен командлет Get-AzureRmRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="3c38d-653">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="3c38d-654">Исправлена работа параметра -ExpandPrincipalGroups.</span><span class="sxs-lookup"><span data-stu-id="3c38d-654">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="3c38d-655">Устранена проблема в командлете Get-AzureRmResource, заключающая в том, что в параметре -ResourceType учитывался регистр символов.</span><span class="sxs-lookup"><span data-stu-id="3c38d-655">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="3c38d-656">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3c38d-656">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="3c38d-657">Добавлены параметры top и skip для командлетов list.</span><span class="sxs-lookup"><span data-stu-id="3c38d-657">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="3c38d-658">Добавлены командлеты для перехода с пространства имен ценовой категории "Стандартный" на пространство ценовой категории "Премиум":</span><span class="sxs-lookup"><span data-stu-id="3c38d-658">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="3c38d-659">Start-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="3c38d-659">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="3c38d-660">Get-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="3c38d-660">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="3c38d-661">Complete-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="3c38d-661">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="3c38d-662">Stop-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="3c38d-662">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="3c38d-663">Remove-AzureRmServiceBusMigration.</span><span class="sxs-lookup"><span data-stu-id="3c38d-663">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="3c38d-664">В класс PSServiceBusDRConfigurationAttributes добавлено доступное только для чтения свойство PendingReplicationOperationsCount, которое показывает количество ожидающих репликации операций во время реплицирования.</span><span class="sxs-lookup"><span data-stu-id="3c38d-664">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="3c38d-665">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3c38d-665">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="3c38d-666">Обновлен пример для командлета New-AzureRmServiceFabricCluster.</span><span class="sxs-lookup"><span data-stu-id="3c38d-666">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="3c38d-667">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="3c38d-667">AzureRM.Sql</span></span>
* <span data-ttu-id="3c38d-668">Добавлены новые командлеты для Management.Sql, позволяющие клиентам добавлять сертификат TDE в экземпляр SQL Server или управляемый экземпляр:</span><span class="sxs-lookup"><span data-stu-id="3c38d-668">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="3c38d-669">Add-AzureRmSqlServerTransparentDataEncryptionCertificate;</span><span class="sxs-lookup"><span data-stu-id="3c38d-669">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="3c38d-670">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate.</span><span class="sxs-lookup"><span data-stu-id="3c38d-670">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="3c38d-671">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="3c38d-671">AzureRM.Websites</span></span>
* <span data-ttu-id="3c38d-672">`Set-AzureRmWebApp -AssignIdentity` и `Set-AzureRmWebAppSlot -AssignIdentity` при установленном значении false теперь будут удалять свойство Identity из объекта сайта. Также при этом будет удаляться тег предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="3c38d-672">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="3c38d-673">Обновлен пример для `Get-AzureRmWebAppMetrics` и `Get-AzureRmAppServicePlanMetrics`.</span><span class="sxs-lookup"><span data-stu-id="3c38d-673">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="3c38d-674">`Set-AzureRmWebApp -PhpVersion` теперь поддерживает off как допустимую версию PHP.</span><span class="sxs-lookup"><span data-stu-id="3c38d-674">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="3c38d-675">6.4.0 — июль 2018 г.</span><span class="sxs-lookup"><span data-stu-id="3c38d-675">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="3c38d-676">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="3c38d-676">General</span></span>
* <span data-ttu-id="3c38d-677">Исправлено форматирование OutputType в файлах справки для большинства модулей.</span><span class="sxs-lookup"><span data-stu-id="3c38d-677">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="3c38d-678">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="3c38d-678">AzureRM.Profile</span></span>
* <span data-ttu-id="3c38d-679">В основные типы выходных данных добавлен атрибут Ps1Xml.</span><span class="sxs-lookup"><span data-stu-id="3c38d-679">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="3c38d-680">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="3c38d-680">AzureRM.Compute</span></span>
* <span data-ttu-id="3c38d-681">Функция добавления тега IP-адреса для масштабируемого набора виртуальных машин (VMSS)</span><span class="sxs-lookup"><span data-stu-id="3c38d-681">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="3c38d-682">Добавлен командлет New-AzureRmVmssIpTagConfig.</span><span class="sxs-lookup"><span data-stu-id="3c38d-682">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="3c38d-683">В New-AzureRmVmssIpConfig добавлен параметр IpTag.</span><span class="sxs-lookup"><span data-stu-id="3c38d-683">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="3c38d-684">Функция автоматического отката ОС для VMSS</span><span class="sxs-lookup"><span data-stu-id="3c38d-684">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="3c38d-685">В New-AzureRmVmssConfig и Update-AzureRmVmss добавлены параметры DisableAutoRollback.</span><span class="sxs-lookup"><span data-stu-id="3c38d-685">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="3c38d-686">Функция ведения журнала обновлений ОС для VMSS</span><span class="sxs-lookup"><span data-stu-id="3c38d-686">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="3c38d-687">В Get-AzureRmVmss добавлен параметр OSUpgradeHistory.</span><span class="sxs-lookup"><span data-stu-id="3c38d-687">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="3c38d-688">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="3c38d-688">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="3c38d-689">Добавлена поддержка списков управления доступом к каталогу с использованием следующих команд:</span><span class="sxs-lookup"><span data-stu-id="3c38d-689">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="3c38d-690">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry;</span><span class="sxs-lookup"><span data-stu-id="3c38d-690">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="3c38d-691">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry;</span><span class="sxs-lookup"><span data-stu-id="3c38d-691">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="3c38d-692">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="3c38d-692">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="3c38d-693">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3c38d-693">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="3c38d-694">Добавлены поддержка отмены выполнения и отслеживание хода выполнения для Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl и Remove-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="3c38d-694">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="3c38d-695">Добавлена поддержка отмены выполнения для Export-AzureRmDataLakeStoreChildItemProperties.</span><span class="sxs-lookup"><span data-stu-id="3c38d-695">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="3c38d-696">Исправлена очистка сообщений об отладке для командлетов, которые выполняют рекурсивные операции.</span><span class="sxs-lookup"><span data-stu-id="3c38d-696">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="3c38d-697">Исправлено расположение тестовых данных для командлетов DataLake.</span><span class="sxs-lookup"><span data-stu-id="3c38d-697">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="3c38d-698">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="3c38d-698">AzureRM.EventHub</span></span>
* <span data-ttu-id="3c38d-699">Для командлетов вывода списка операций Get-AzureRmEventHub и Get-AzureRmEventHubConsumerGroup добавлен необязательный параметр MaxCount.</span><span class="sxs-lookup"><span data-stu-id="3c38d-699">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="3c38d-700">Исправлена проблема с командлетом New-AzureRmEventHub, из-за которой требовалось указать по крайней мере один параметр при создании концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="3c38d-700">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="3c38d-701">Добавлен набор параметров по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3c38d-701">Provided Default Parameter set.</span></span>
* <span data-ttu-id="3c38d-702">Для командлета New-AzureRmEventHubKey добавлен необязательный параметр -KeyValue, который позволяет пользователю предоставить значение ключа.</span><span class="sxs-lookup"><span data-stu-id="3c38d-702">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="3c38d-703">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3c38d-703">AzureRM.KeyVault</span></span>
* <span data-ttu-id="3c38d-704">Исправлена ошибка, из-за которой при выполнении командлета Get-AzureRmKeyVault с параметром -Tag возвращались все ресурсы.</span><span class="sxs-lookup"><span data-stu-id="3c38d-704">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="3c38d-705">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="3c38d-705">AzureRM.Network</span></span>
* <span data-ttu-id="3c38d-706">Для параметра шлюзов виртуальной вести, избыточных между зонами, предоставлены новые номера SKU.</span><span class="sxs-lookup"><span data-stu-id="3c38d-706">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="3c38d-707">Добавлены новые команды для функции поддержки партнерских API для ExpressRoute, развертываемых с помощью ARM:</span><span class="sxs-lookup"><span data-stu-id="3c38d-707">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="3c38d-708">добавлена команда Get-AzureRmExpressRouteCrossConnection;</span><span class="sxs-lookup"><span data-stu-id="3c38d-708">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="3c38d-709">добавлена команда Set-AzureRmExpressRouteCrossConnection;</span><span class="sxs-lookup"><span data-stu-id="3c38d-709">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="3c38d-710">добавлена команда Add-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="3c38d-710">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="3c38d-711">добавлена команда Get-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="3c38d-711">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="3c38d-712">добавлена команда Remove-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="3c38d-712">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="3c38d-713">добавлена команда Get-AzureRMExpressRouteCrossConnectionArpTable;</span><span class="sxs-lookup"><span data-stu-id="3c38d-713">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="3c38d-714">добавлена команда Get-AzureRMExpressRouteCrossConnectionRouteTable;</span><span class="sxs-lookup"><span data-stu-id="3c38d-714">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="3c38d-715">добавлена команда Get-AzureRMExpressRouteCrossConnectionRouteTableSummary.</span><span class="sxs-lookup"><span data-stu-id="3c38d-715">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="3c38d-716">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="3c38d-716">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="3c38d-717">Добавлен командлет Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="3c38d-717">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="3c38d-718">Этот командлет принимает идентификатор виртуальной машины и проверяет, защищена ли виртуальная машина с помощью какого-либо хранилища в подписке.</span><span class="sxs-lookup"><span data-stu-id="3c38d-718">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="3c38d-719">Если такое хранилище существует, командлет выводит данные о нем.</span><span class="sxs-lookup"><span data-stu-id="3c38d-719">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="3c38d-720">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="3c38d-720">AzureRM.Resources</span></span>
* <span data-ttu-id="3c38d-721">Обновлены командлеты Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="3c38d-721">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="3c38d-722">Добавлена поддержка вывода списка значений параметра -Scope на уровне группы управления.</span><span class="sxs-lookup"><span data-stu-id="3c38d-722">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="3c38d-723">Добавлена поддержка для получения отдельных назначений со значениями -Scope на уровне группы управления.</span><span class="sxs-lookup"><span data-stu-id="3c38d-723">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="3c38d-724">Для параметра управления добавлены параметры -Effective и -All.</span><span class="sxs-lookup"><span data-stu-id="3c38d-724">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="3c38d-725">Обновлены командлеты Get/New/Remove/Set-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="3c38d-725">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="3c38d-726">Добавлен параметр -ManagementGroupName для применения операций к заданной группе управления.</span><span class="sxs-lookup"><span data-stu-id="3c38d-726">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="3c38d-727">Добавлен параметр -SubscriptionId для применения операций к заданной подписке.</span><span class="sxs-lookup"><span data-stu-id="3c38d-727">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="3c38d-728">Обновлены командлеты Get/New/Remove/Set-AzureRmPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="3c38d-728">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="3c38d-729">Добавлен параметр -ManagementGroupName для применения операций к заданной группе управления.</span><span class="sxs-lookup"><span data-stu-id="3c38d-729">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="3c38d-730">Добавлен параметр -SubscriptionId для применения операций к заданной подписке.</span><span class="sxs-lookup"><span data-stu-id="3c38d-730">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="3c38d-731">Добавлена поддержка ссылок на секрет KeyVault в параметрах при использовании TemplateParameterObject в New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="3c38d-731">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="3c38d-732">Устранена проблема, из-за которой параметр -EndDate игнорировался в New-AzureRmADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="3c38d-732">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="3c38d-733">Устранена проблема, из-за которой в Add-AzureRmADGroupMember использовался неверный URL-адрес для запроса.</span><span class="sxs-lookup"><span data-stu-id="3c38d-733">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="3c38d-734">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3c38d-734">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="3c38d-735">Для командлета New-AzureRmServiceBusKey добавлен необязательный параметр -KeyValue, который позволяет пользователю предоставить значение ключа.</span><span class="sxs-lookup"><span data-stu-id="3c38d-735">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="3c38d-736">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="3c38d-736">AzureRM.Sql</span></span>
* <span data-ttu-id="3c38d-737">В справке по New-AzureRmSqlDatabaseRestorePoint добавлено описание определяемых пользователем точек восстановления для хранилища данных SQL.</span><span class="sxs-lookup"><span data-stu-id="3c38d-737">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="3c38d-738">Обновлена документация по параметру -ComputeGeneration, используемого в нескольких командлетах.</span><span class="sxs-lookup"><span data-stu-id="3c38d-738">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="3c38d-739">6.3.0 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="3c38d-739">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="3c38d-740">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="3c38d-740">AzureRM.Profile</span></span>
* <span data-ttu-id="3c38d-741">Обновлены сообщения об ошибках для Enable-AzureRmContextAutoSave.</span><span class="sxs-lookup"><span data-stu-id="3c38d-741">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="3c38d-742">Создание контекста для каждой подписки при выполнении Connect-AzureRmAccount без предыдущего контекста.</span><span class="sxs-lookup"><span data-stu-id="3c38d-742">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="3c38d-743">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="3c38d-743">Azure.Storage</span></span>
* <span data-ttu-id="3c38d-744">В файлы справки добавлены дополнительные сведения о параметре -Permissions.</span><span class="sxs-lookup"><span data-stu-id="3c38d-744">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="3c38d-745">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="3c38d-745">AzureRM.Compute</span></span>
* <span data-ttu-id="3c38d-746">Get-AzureRmVmDiskEncryptionStatus устраняет проблему, которая наблюдалась на виртуальных машинах без дисков данных.</span><span class="sxs-lookup"><span data-stu-id="3c38d-746">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="3c38d-747">Обновлена версия клиентской библиотеки Compute для исправления следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="3c38d-747">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="3c38d-748">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="3c38d-748">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="3c38d-749">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="3c38d-749">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="3c38d-750">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="3c38d-750">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="3c38d-751">В следующих командлетах исправлено отображение неправильных значений operation ID и operation status:</span><span class="sxs-lookup"><span data-stu-id="3c38d-751">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="3c38d-752">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3c38d-752">Start-AzureRmVM</span></span>
    - <span data-ttu-id="3c38d-753">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3c38d-753">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="3c38d-754">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3c38d-754">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="3c38d-755">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3c38d-755">Set-AzureRmVM</span></span>
    - <span data-ttu-id="3c38d-756">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="3c38d-756">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="3c38d-757">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3c38d-757">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="3c38d-758">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="3c38d-758">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="3c38d-759">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="3c38d-759">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="3c38d-760">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3c38d-760">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="3c38d-761">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3c38d-761">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="3c38d-762">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3c38d-762">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="3c38d-763">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3c38d-763">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="3c38d-764">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="3c38d-764">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="3c38d-765">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="3c38d-765">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="3c38d-766">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="3c38d-766">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="3c38d-767">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="3c38d-767">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="3c38d-768">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="3c38d-768">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="3c38d-769">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="3c38d-769">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="3c38d-770">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="3c38d-770">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="3c38d-771">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="3c38d-771">AzureRM.EventGrid</span></span>
* <span data-ttu-id="3c38d-772">Удалены условия проверки ValidateNotNullOrEmpty для SubjectBeginsWith/SubjectEndsWith в командлете Update-AzureRmEventGridSubscription, что позволяет при необходимости заменять эти параметры пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="3c38d-772">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="3c38d-773">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3c38d-773">AzureRM.KeyVault</span></span>
* <span data-ttu-id="3c38d-774">Исправлена ошибка, когда при выполнении командлета Get-AzureRmKeyVault -Tag не возвращается ни один тег.</span><span class="sxs-lookup"><span data-stu-id="3c38d-774">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="3c38d-775">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="3c38d-775">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="3c38d-776">Общедоступный выпуск командлетов Policy Insights.</span><span class="sxs-lookup"><span data-stu-id="3c38d-776">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="3c38d-777">Используется API версии 2018-04-04.</span><span class="sxs-lookup"><span data-stu-id="3c38d-777">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="3c38d-778">К результатам Get-AzureRmPolicyStateSummary добавлено PolicyDefinitionReferenceId.</span><span class="sxs-lookup"><span data-stu-id="3c38d-778">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="3c38d-779">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="3c38d-779">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="3c38d-780">Для командлетов RecoveryServices.Backup добавлен параметр -Vault.</span><span class="sxs-lookup"><span data-stu-id="3c38d-780">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="3c38d-781">Передача этого параметра переопределяет командлет Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="3c38d-781">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="3c38d-782">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="3c38d-782">AzureRM.Sql</span></span>
* <span data-ttu-id="3c38d-783">В файле справки обновлен пример для командлета Get-AzureRmSqlDatabaseExpanded.</span><span class="sxs-lookup"><span data-stu-id="3c38d-783">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="3c38d-784">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="3c38d-784">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="3c38d-785">Обновлен файл справки для командлета Add-AzureRmTrafficManagerEndpointConfig.</span><span class="sxs-lookup"><span data-stu-id="3c38d-785">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="3c38d-786">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="3c38d-786">AzureRM.Websites</span></span>
* <span data-ttu-id="3c38d-787">Изменено действие командлета Set-AzureRmWebApp. Теперь он не перезаписывает AppSettings, если используется параметр -AssignIdentity.</span><span class="sxs-lookup"><span data-stu-id="3c38d-787">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="3c38d-788">Командлет New-AzureRmWebAppSlot теперь учитывает дополнительный параметр AppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="3c38d-788">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="3c38d-789">6.2.1 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="3c38d-789">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="3c38d-790">AzureRM.OperationalInsights;</span><span class="sxs-lookup"><span data-stu-id="3c38d-790">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="3c38d-791">В обновленной модели PSWorkspace Network может использовать type в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="3c38d-791">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="3c38d-792">6.2.0 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="3c38d-792">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="3c38d-793">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="3c38d-793">AzureRM.Profile</span></span>
* <span data-ttu-id="3c38d-794">Исправлена ошибка с загрузкой Newtonsoft.Json версии 10.0.3 во время импорта модуля.</span><span class="sxs-lookup"><span data-stu-id="3c38d-794">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="3c38d-795">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="3c38d-795">AzureRM.Compute</span></span>
* <span data-ttu-id="3c38d-796">Функция обновления виртуальных машин VMSS.</span><span class="sxs-lookup"><span data-stu-id="3c38d-796">VMSS VM Update feature</span></span>
    - <span data-ttu-id="3c38d-797">Добавлены командлеты Update-AzureRmVmssVM и New-AzureRmVMDataDisk.</span><span class="sxs-lookup"><span data-stu-id="3c38d-797">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="3c38d-798">В командлет Add-AzureRmVMDataDisk добавлен параметр VirtualMachineScaleSetVM, который позволяет добавлять диски данных в виртуальные машины VMSS.</span><span class="sxs-lookup"><span data-stu-id="3c38d-798">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="3c38d-799">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="3c38d-799">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="3c38d-800">Пакет SDK для ADF .NET обновлен до версии 0.8.0-preview. Новая версия содержит такие изменения:</span><span class="sxs-lookup"><span data-stu-id="3c38d-800">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="3c38d-801">добавлена операция для настройки репозитория фабрики;</span><span class="sxs-lookup"><span data-stu-id="3c38d-801">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="3c38d-802">связанная служба QuickBooks LinkedService теперь предоставляет свойства consumerKey и consumerSecret;</span><span class="sxs-lookup"><span data-stu-id="3c38d-802">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="3c38d-803">тип нескольких моделей изменен с SecretBase на Object;</span><span class="sxs-lookup"><span data-stu-id="3c38d-803">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="3c38d-804">добавлен триггер событий BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="3c38d-804">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="3c38d-805">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3c38d-805">AzureRM.KeyVault</span></span>
* <span data-ttu-id="3c38d-806">В документацию добавлены примеры выходных данных.</span><span class="sxs-lookup"><span data-stu-id="3c38d-806">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="3c38d-807">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="3c38d-807">AzureRM.Network</span></span>
* <span data-ttu-id="3c38d-808">В командлеты Наблюдателя за сетями добавлены параметры Аналитики трафика.</span><span class="sxs-lookup"><span data-stu-id="3c38d-808">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="3c38d-809">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="3c38d-809">AzureRM.Resources</span></span>
* <span data-ttu-id="3c38d-810">Исправлена ошибка, когда командлет Get-AzureRmResource возвращает свойство Properties объектов PSResource.</span><span class="sxs-lookup"><span data-stu-id="3c38d-810">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="3c38d-811">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="3c38d-811">AzureRM.Scheduler</span></span>
* <span data-ttu-id="3c38d-812">Исправлена ошибка, когда обновление ServiceBusQueueJob не задает новые значения для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="3c38d-812">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="3c38d-813">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="3c38d-813">AzureRM.Sql</span></span>
* <span data-ttu-id="3c38d-814">В перечисленные ниже командлеты добавлен необязательный параметр LicenseType.</span><span class="sxs-lookup"><span data-stu-id="3c38d-814">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="3c38d-815">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="3c38d-815">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="3c38d-816">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool;</span><span class="sxs-lookup"><span data-stu-id="3c38d-816">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="3c38d-817">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="3c38d-817">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="3c38d-818">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="3c38d-818">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="3c38d-819">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3c38d-819">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="3c38d-820">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="3c38d-820">AzureRM.Websites</span></span>
* <span data-ttu-id="3c38d-821">Командлет New-AzureRMWebApp теперь использует общие алгоритмы из библиотеки Strategy.</span><span class="sxs-lookup"><span data-stu-id="3c38d-821">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="3c38d-822">6.1.0 — май 2018 г.</span><span class="sxs-lookup"><span data-stu-id="3c38d-822">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="3c38d-823">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="3c38d-823">AzureRM.Profile</span></span>
* <span data-ttu-id="3c38d-824">Устранена проблема с выполнением Clear-AzureRmContext, при которой сохранялся пустой контекст с именем предыдущего контекста по умолчанию, что не позволяло пользователю создать новый контекст со старым именем.</span><span class="sxs-lookup"><span data-stu-id="3c38d-824">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="3c38d-825">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3c38d-825">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="3c38d-826">Включены операции связывания и отмены связи в автономной системе.</span><span class="sxs-lookup"><span data-stu-id="3c38d-826">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="3c38d-827">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3c38d-827">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="3c38d-828">Добавлена поддержка ApiVersions, ApiReleases и ApiRevisions.</span><span class="sxs-lookup"><span data-stu-id="3c38d-828">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="3c38d-829">Добавлена поддержка серверной части ServiceFabric.</span><span class="sxs-lookup"><span data-stu-id="3c38d-829">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="3c38d-830">Добавлена поддержка средства ведения журнала Application Insights.</span><span class="sxs-lookup"><span data-stu-id="3c38d-830">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="3c38d-831">Добавлена поддержка для распознавания номера SKU уровня "Базовый" как допустимого номера SKU службы управления API.</span><span class="sxs-lookup"><span data-stu-id="3c38d-831">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="3c38d-832">Добавлена поддержка установки сертификатов, выданных частным центром сертификации в качестве корневого или обычного ЦС.</span><span class="sxs-lookup"><span data-stu-id="3c38d-832">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="3c38d-833">Добавлена поддержка для приема пользовательских SSL-сертификатов с помощью KeyVault и нескольких имен узлов прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="3c38d-833">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="3c38d-834">Добавлена поддержка для удостоверения MSI.</span><span class="sxs-lookup"><span data-stu-id="3c38d-834">Added support for MSI identity</span></span>
* <span data-ttu-id="3c38d-835">Добавлена поддержка для принятия политик с помощью URL-адреса. Примечание. Указанные ниже командлеты в следующей версии будут отмечены как нерекомендуемые.</span><span class="sxs-lookup"><span data-stu-id="3c38d-835">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="3c38d-836">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="3c38d-836">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="3c38d-837">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="3c38d-837">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="3c38d-838">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="3c38d-838">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="3c38d-839">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="3c38d-839">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="3c38d-840">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="3c38d-840">AzureRM.Batch</span></span>
* <span data-ttu-id="3c38d-841">Выпущен новый командлет Get-AzureBatchPoolNodeCounts.</span><span class="sxs-lookup"><span data-stu-id="3c38d-841">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="3c38d-842">Выпущен новый командлет Start-AzureBatchComputeNodeServiceLogUpload.</span><span class="sxs-lookup"><span data-stu-id="3c38d-842">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="3c38d-843">AzureRM.Consumption:</span><span class="sxs-lookup"><span data-stu-id="3c38d-843">AzureRM.Consumption</span></span>
* <span data-ttu-id="3c38d-844">Добавлены новые параметры Expand, ResourceGroup, InstanceName, InstanceId, Tags и командлет высшего уровня Get-AzureRmConsumptionUsageDetail.</span><span class="sxs-lookup"><span data-stu-id="3c38d-844">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="3c38d-845">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3c38d-845">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="3c38d-846">Исправлен пример для Export-AzureRmDataLakeStoreChildItemProperties.</span><span class="sxs-lookup"><span data-stu-id="3c38d-846">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="3c38d-847">Исправлено исключение параметра NULL при использовании рекурсии в Set-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="3c38d-847">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="3c38d-848">Исправлены файлы справки для Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl и Remove-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="3c38d-848">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="3c38d-849">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="3c38d-849">AzureRM.Network</span></span>
* <span data-ttu-id="3c38d-850">Пакет SDK для сети обновлен с предварительной версии 18.0.0 до предварительной версии 19.0.0.</span><span class="sxs-lookup"><span data-stu-id="3c38d-850">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="3c38d-851">Добавлен командлет для создания конфигурации протокола.</span><span class="sxs-lookup"><span data-stu-id="3c38d-851">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="3c38d-852">New-AzureRmNetworkWatcherProtocolConfiguration.</span><span class="sxs-lookup"><span data-stu-id="3c38d-852">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="3c38d-853">Добавлен командлет для добавления нового подключения канала к существующему каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="3c38d-853">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="3c38d-854">Add-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="3c38d-854">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="3c38d-855">Добавлен командлет для удаления подключения канала к существующему каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="3c38d-855">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="3c38d-856">Remove-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="3c38d-856">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="3c38d-857">Добавлен командлет для получения подключения канала.</span><span class="sxs-lookup"><span data-stu-id="3c38d-857">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="3c38d-858">Get-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="3c38d-858">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="3c38d-859">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3c38d-859">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="3c38d-860">Исправлена процедура аутентификации сервера с использованием созданных сертификатов (проблема № 5998).</span><span class="sxs-lookup"><span data-stu-id="3c38d-860">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="3c38d-861">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="3c38d-861">AzureRM.Sql</span></span>
* <span data-ttu-id="3c38d-862">Обновлены командлеты аудита, которые теперь позволяют удалять AuditActions или AuditActionGroups.</span><span class="sxs-lookup"><span data-stu-id="3c38d-862">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="3c38d-863">Исправлена проблема с Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy, при которой установка новой гибкой политики хранения завершалась ошибкой с сообщением "Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span><span class="sxs-lookup"><span data-stu-id="3c38d-863">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="3c38d-864">Please submit request with the new flexible retention policy" (Настройка политики долгосрочного хранения с помощью хранилища и политики служб восстановления Azure больше не поддерживается. Отправьте запрос с использованием новой гибкой политики хранения).</span><span class="sxs-lookup"><span data-stu-id="3c38d-864">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="3c38d-865">Обновлены все командлеты, связанные со службой "База данных SQL Azure", с созданием эластичных пулов и обновлением. Теперь используются новые API баз данных с поддержкой свойства номеров SKU для обеспечения масштабируемости и связанных с уровнями возможностей.</span><span class="sxs-lookup"><span data-stu-id="3c38d-865">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="3c38d-866">Обновлены командлеты, в том числе:</span><span class="sxs-lookup"><span data-stu-id="3c38d-866">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="3c38d-867">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="3c38d-867">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="3c38d-868">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool;</span><span class="sxs-lookup"><span data-stu-id="3c38d-868">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="3c38d-869">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="3c38d-869">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="3c38d-870">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="3c38d-870">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="3c38d-871">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3c38d-871">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="3c38d-872">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="3c38d-872">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="3c38d-873">Обновлены параметры для Get-AzureRmTrafficManagerProfile. Теперь при использовании параметра -Name требуется параметр -ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="3c38d-873">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
