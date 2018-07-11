---
title: Журнал изменений Azure PowerShell | Документация Майкрософт
description: Это руководство содержит историю изменений Azure PowerShell, внесенных в новом выпуске.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 255e26aea5ea3cea866faa0d095cdf643c8ef0a8
ms.sourcegitcommit: de0e60800df1add9f3400166faacca202ef567d9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/03/2018
ms.locfileid: "37406674"
---
# <a name="release-notes"></a><span data-ttu-id="e0d24-103">Заметки о выпуске</span><span class="sxs-lookup"><span data-stu-id="e0d24-103">Release notes</span></span>

<span data-ttu-id="e0d24-104">Здесь приведен список изменений, внесенных в Azure PowerShell в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="e0d24-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="640---july-2018"></a><span data-ttu-id="e0d24-105">6.4.0 — июль 2018 г.</span><span class="sxs-lookup"><span data-stu-id="e0d24-105">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="e0d24-106">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="e0d24-106">General</span></span>
* <span data-ttu-id="e0d24-107">Исправлено форматирование OutputType в файлах справки для большинства модулей.</span><span class="sxs-lookup"><span data-stu-id="e0d24-107">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="e0d24-108">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="e0d24-108">AzureRM.Profile</span></span>
* <span data-ttu-id="e0d24-109">В основные типы выходных данных добавлен атрибут Ps1Xml.</span><span class="sxs-lookup"><span data-stu-id="e0d24-109">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="e0d24-110">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="e0d24-110">AzureRM.Compute</span></span>
* <span data-ttu-id="e0d24-111">Функция добавления тега IP-адреса для масштабируемого набора виртуальных машин (VMSS)</span><span class="sxs-lookup"><span data-stu-id="e0d24-111">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="e0d24-112">Добавлен командлет New-AzureRmVmssIpTagConfig.</span><span class="sxs-lookup"><span data-stu-id="e0d24-112">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="e0d24-113">В New-AzureRmVmssIpConfig добавлен параметр IpTag.</span><span class="sxs-lookup"><span data-stu-id="e0d24-113">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="e0d24-114">Функция автоматического отката ОС для VMSS</span><span class="sxs-lookup"><span data-stu-id="e0d24-114">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="e0d24-115">В New-AzureRmVmssConfig и Update-AzureRmVmss добавлены параметры DisableAutoRollback.</span><span class="sxs-lookup"><span data-stu-id="e0d24-115">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="e0d24-116">Функция ведения журнала обновлений ОС для VMSS</span><span class="sxs-lookup"><span data-stu-id="e0d24-116">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="e0d24-117">В Get-AzureRmVmss добавлен параметр OSUpgradeHistory.</span><span class="sxs-lookup"><span data-stu-id="e0d24-117">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="e0d24-118">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="e0d24-118">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="e0d24-119">Добавлена поддержка списков управления доступом к каталогу с использованием следующих команд:</span><span class="sxs-lookup"><span data-stu-id="e0d24-119">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="e0d24-120">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry;</span><span class="sxs-lookup"><span data-stu-id="e0d24-120">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="e0d24-121">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry;</span><span class="sxs-lookup"><span data-stu-id="e0d24-121">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="e0d24-122">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="e0d24-122">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="e0d24-123">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e0d24-123">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="e0d24-124">Добавлены поддержка отмены выполнения и отслеживание хода выполнения для Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl и Remove-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="e0d24-124">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="e0d24-125">Добавлена поддержка отмены выполнения для Export-AzureRmDataLakeStoreChildItemProperties.</span><span class="sxs-lookup"><span data-stu-id="e0d24-125">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="e0d24-126">Исправлена очистка сообщений об отладке для командлетов, которые выполняют рекурсивные операции.</span><span class="sxs-lookup"><span data-stu-id="e0d24-126">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="e0d24-127">Исправлено расположение тестовых данных для командлетов DataLake.</span><span class="sxs-lookup"><span data-stu-id="e0d24-127">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="e0d24-128">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="e0d24-128">AzureRM.EventHub</span></span>
* <span data-ttu-id="e0d24-129">Для командлетов вывода списка операций Get-AzureRmEventHub и Get-AzureRmEventHubConsumerGroup добавлен необязательный параметр MaxCount.</span><span class="sxs-lookup"><span data-stu-id="e0d24-129">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="e0d24-130">Исправлена проблема с командлетом New-AzureRmEventHub, из-за которой требовалось указать по крайней мере один параметр при создании концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="e0d24-130">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="e0d24-131">Добавлен набор параметров по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e0d24-131">Provided Default Parameter set.</span></span>
* <span data-ttu-id="e0d24-132">Для командлета New-AzureRmEventHubKey добавлен необязательный параметр -KeyValue, который позволяет пользователю предоставить значение ключа.</span><span class="sxs-lookup"><span data-stu-id="e0d24-132">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="e0d24-133">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e0d24-133">AzureRM.KeyVault</span></span>
* <span data-ttu-id="e0d24-134">Исправлена ошибка, из-за которой при выполнении командлета Get-AzureRmKeyVault с параметром -Tag возвращались все ресурсы.</span><span class="sxs-lookup"><span data-stu-id="e0d24-134">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="e0d24-135">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="e0d24-135">AzureRM.Network</span></span>
* <span data-ttu-id="e0d24-136">Для параметра шлюзов виртуальной вести, избыточных в пределах зоны, предоставлены новые номера SKU.</span><span class="sxs-lookup"><span data-stu-id="e0d24-136">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="e0d24-137">Добавлены новые команды для функции поддержки партнерских API для ExpressRoute, развертываемых с помощью ARM:</span><span class="sxs-lookup"><span data-stu-id="e0d24-137">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="e0d24-138">добавлена команда Get-AzureRmExpressRouteCrossConnection;</span><span class="sxs-lookup"><span data-stu-id="e0d24-138">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="e0d24-139">добавлена команда Set-AzureRmExpressRouteCrossConnection;</span><span class="sxs-lookup"><span data-stu-id="e0d24-139">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="e0d24-140">добавлена команда Add-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="e0d24-140">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="e0d24-141">добавлена команда Get-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="e0d24-141">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="e0d24-142">добавлена команда Remove-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="e0d24-142">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="e0d24-143">добавлена команда Get-AzureRMExpressRouteCrossConnectionArpTable;</span><span class="sxs-lookup"><span data-stu-id="e0d24-143">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="e0d24-144">добавлена команда Get-AzureRMExpressRouteCrossConnectionRouteTable;</span><span class="sxs-lookup"><span data-stu-id="e0d24-144">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="e0d24-145">добавлена команда Get-AzureRMExpressRouteCrossConnectionRouteTableSummary.</span><span class="sxs-lookup"><span data-stu-id="e0d24-145">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="e0d24-146">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="e0d24-146">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="e0d24-147">Добавлен командлет Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="e0d24-147">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="e0d24-148">Этот командлет принимает идентификатор виртуальной машины и проверяет, защищена ли виртуальная машина с помощью какого-либо хранилища в подписке.</span><span class="sxs-lookup"><span data-stu-id="e0d24-148">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="e0d24-149">Если такое хранилище существует, командлет выводит данные о нем.</span><span class="sxs-lookup"><span data-stu-id="e0d24-149">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="e0d24-150">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="e0d24-150">AzureRM.Resources</span></span>
* <span data-ttu-id="e0d24-151">Обновлены командлеты Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="e0d24-151">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="e0d24-152">Добавлена поддержка вывода списка значений параметра -Scope на уровне группы управления.</span><span class="sxs-lookup"><span data-stu-id="e0d24-152">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="e0d24-153">Добавлена поддержка для получения отдельных назначений со значениями -Scope на уровне группы управления.</span><span class="sxs-lookup"><span data-stu-id="e0d24-153">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="e0d24-154">Для параметра управления добавлены параметры -Effective и -All.</span><span class="sxs-lookup"><span data-stu-id="e0d24-154">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="e0d24-155">Обновлены командлеты Get/New/Remove/Set-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="e0d24-155">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="e0d24-156">Добавлен параметр -ManagementGroupName для применения операций к заданной группе управления.</span><span class="sxs-lookup"><span data-stu-id="e0d24-156">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="e0d24-157">Добавлен параметр -SubscriptionId для применения операций к заданной подписке.</span><span class="sxs-lookup"><span data-stu-id="e0d24-157">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="e0d24-158">Обновлены командлеты Get/New/Remove/Set-AzureRmPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="e0d24-158">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="e0d24-159">Добавлен параметр -ManagementGroupName для применения операций к заданной группе управления.</span><span class="sxs-lookup"><span data-stu-id="e0d24-159">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="e0d24-160">Добавлен параметр -SubscriptionId для применения операций к заданной подписке.</span><span class="sxs-lookup"><span data-stu-id="e0d24-160">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="e0d24-161">Добавлена поддержка ссылок на секрет KeyVault в параметрах при использовании TemplateParameterObject в New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="e0d24-161">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="e0d24-162">Устранена проблема, из-за которой параметр -EndDate игнорировался в New-AzureRmADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="e0d24-162">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="e0d24-163">Устранена проблема, из-за которой в Add-AzureRmADGroupMember использовался неверный URL-адрес для запроса.</span><span class="sxs-lookup"><span data-stu-id="e0d24-163">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="e0d24-164">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e0d24-164">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="e0d24-165">Для командлета New-AzureRmServiceBusKey добавлен необязательный параметр -KeyValue, который позволяет пользователю предоставить значение ключа.</span><span class="sxs-lookup"><span data-stu-id="e0d24-165">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="e0d24-166">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="e0d24-166">AzureRM.Sql</span></span>
* <span data-ttu-id="e0d24-167">В справке по New-AzureRmSqlDatabaseRestorePoint добавлено описание определяемых пользователем точек восстановления для хранилища данных SQL.</span><span class="sxs-lookup"><span data-stu-id="e0d24-167">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="e0d24-168">Обновлена документация по параметру -ComputeGeneration, используемого в нескольких командлетах.</span><span class="sxs-lookup"><span data-stu-id="e0d24-168">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="e0d24-169">6.3.0 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="e0d24-169">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="e0d24-170">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="e0d24-170">AzureRM.Profile</span></span>
* <span data-ttu-id="e0d24-171">Обновлены сообщения об ошибках для Enable-AzureRmContextAutoSave.</span><span class="sxs-lookup"><span data-stu-id="e0d24-171">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="e0d24-172">Создание контекста для каждой подписки при выполнении Connect-AzureRmAccount без предыдущего контекста.</span><span class="sxs-lookup"><span data-stu-id="e0d24-172">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="e0d24-173">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="e0d24-173">Azure.Storage</span></span>
* <span data-ttu-id="e0d24-174">В файлы справки добавлены дополнительные сведения о параметре -Permissions.</span><span class="sxs-lookup"><span data-stu-id="e0d24-174">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="e0d24-175">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="e0d24-175">AzureRM.Compute</span></span>
* <span data-ttu-id="e0d24-176">Get-AzureRmVmDiskEncryptionStatus устраняет проблему, которая наблюдалась на виртуальных машинах без дисков данных.</span><span class="sxs-lookup"><span data-stu-id="e0d24-176">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="e0d24-177">Обновлена версия клиентской библиотеки Compute для исправления следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="e0d24-177">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="e0d24-178">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="e0d24-178">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="e0d24-179">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="e0d24-179">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="e0d24-180">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="e0d24-180">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="e0d24-181">В следующих командлетах исправлено отображение неправильных значений operation ID и operation status:</span><span class="sxs-lookup"><span data-stu-id="e0d24-181">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="e0d24-182">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e0d24-182">Start-AzureRmVM</span></span>
    - <span data-ttu-id="e0d24-183">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e0d24-183">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="e0d24-184">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e0d24-184">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="e0d24-185">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e0d24-185">Set-AzureRmVM</span></span>
    - <span data-ttu-id="e0d24-186">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="e0d24-186">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="e0d24-187">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e0d24-187">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="e0d24-188">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="e0d24-188">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="e0d24-189">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="e0d24-189">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="e0d24-190">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e0d24-190">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="e0d24-191">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e0d24-191">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="e0d24-192">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e0d24-192">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="e0d24-193">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e0d24-193">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="e0d24-194">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="e0d24-194">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="e0d24-195">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="e0d24-195">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="e0d24-196">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="e0d24-196">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="e0d24-197">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="e0d24-197">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="e0d24-198">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="e0d24-198">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="e0d24-199">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="e0d24-199">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="e0d24-200">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e0d24-200">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="e0d24-201">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e0d24-201">AzureRM.EventGrid</span></span>
* <span data-ttu-id="e0d24-202">Удалены условия проверки ValidateNotNullOrEmpty для SubjectBeginsWith/SubjectEndsWith в командлете Update-AzureRmEventGridSubscription, что позволяет при необходимости заменять эти параметры пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="e0d24-202">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="e0d24-203">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e0d24-203">AzureRM.KeyVault</span></span>
* <span data-ttu-id="e0d24-204">Исправлена ошибка, когда при выполнении командлета Get-AzureRmKeyVault -Tag не возвращается ни один тег.</span><span class="sxs-lookup"><span data-stu-id="e0d24-204">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="e0d24-205">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e0d24-205">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="e0d24-206">Общедоступный выпуск командлетов Policy Insights.</span><span class="sxs-lookup"><span data-stu-id="e0d24-206">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="e0d24-207">Используется API версии 2018-04-04.</span><span class="sxs-lookup"><span data-stu-id="e0d24-207">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="e0d24-208">К результатам Get-AzureRmPolicyStateSummary добавлено PolicyDefinitionReferenceId.</span><span class="sxs-lookup"><span data-stu-id="e0d24-208">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="e0d24-209">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="e0d24-209">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="e0d24-210">Для командлетов RecoveryServices.Backup добавлен параметр -Vault.</span><span class="sxs-lookup"><span data-stu-id="e0d24-210">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="e0d24-211">Передача этого параметра переопределяет командлет Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="e0d24-211">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="e0d24-212">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="e0d24-212">AzureRM.Sql</span></span>
* <span data-ttu-id="e0d24-213">В файле справки обновлен пример для командлета Get-AzureRmSqlDatabaseExpanded.</span><span class="sxs-lookup"><span data-stu-id="e0d24-213">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="e0d24-214">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="e0d24-214">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="e0d24-215">Обновлен файл справки для командлета Add-AzureRmTrafficManagerEndpointConfig.</span><span class="sxs-lookup"><span data-stu-id="e0d24-215">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="e0d24-216">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="e0d24-216">AzureRM.Websites</span></span>
* <span data-ttu-id="e0d24-217">Изменено действие командлета Set-AzureRmWebApp. Теперь он не перезаписывает AppSettings, если используется параметр -AssignIdentity.</span><span class="sxs-lookup"><span data-stu-id="e0d24-217">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="e0d24-218">Командлет New-AzureRmWebAppSlot теперь учитывает дополнительный параметр AppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="e0d24-218">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="e0d24-219">6.2.1 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="e0d24-219">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="e0d24-220">AzureRM.OperationalInsights;</span><span class="sxs-lookup"><span data-stu-id="e0d24-220">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="e0d24-221">В обновленной модели PSWorkspace Network может использовать type в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="e0d24-221">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="e0d24-222">6.2.0 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="e0d24-222">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="e0d24-223">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="e0d24-223">AzureRM.Profile</span></span>
* <span data-ttu-id="e0d24-224">Исправлена ошибка с загрузкой Newtonsoft.Json версии 10.0.3 во время импорта модуля.</span><span class="sxs-lookup"><span data-stu-id="e0d24-224">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="e0d24-225">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="e0d24-225">AzureRM.Compute</span></span>
* <span data-ttu-id="e0d24-226">Функция обновления виртуальных машин VMSS.</span><span class="sxs-lookup"><span data-stu-id="e0d24-226">VMSS VM Update feature</span></span>
    - <span data-ttu-id="e0d24-227">Добавлены командлеты Update-AzureRmVmssVM и New-AzureRmVMDataDisk.</span><span class="sxs-lookup"><span data-stu-id="e0d24-227">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="e0d24-228">В командлет Add-AzureRmVMDataDisk добавлен параметр VirtualMachineScaleSetVM, который позволяет добавлять диски данных в виртуальные машины VMSS.</span><span class="sxs-lookup"><span data-stu-id="e0d24-228">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="e0d24-229">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e0d24-229">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="e0d24-230">Пакет SDK для ADF .NET обновлен до версии 0.8.0-preview. Новая версия содержит такие изменения:</span><span class="sxs-lookup"><span data-stu-id="e0d24-230">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="e0d24-231">добавлена операция для настройки репозитория фабрики;</span><span class="sxs-lookup"><span data-stu-id="e0d24-231">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="e0d24-232">связанная служба QuickBooks LinkedService теперь предоставляет свойства consumerKey и consumerSecret;</span><span class="sxs-lookup"><span data-stu-id="e0d24-232">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="e0d24-233">тип нескольких моделей изменен с SecretBase на Object;</span><span class="sxs-lookup"><span data-stu-id="e0d24-233">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="e0d24-234">добавлен триггер событий BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="e0d24-234">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="e0d24-235">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e0d24-235">AzureRM.KeyVault</span></span>
* <span data-ttu-id="e0d24-236">В документацию добавлены примеры выходных данных.</span><span class="sxs-lookup"><span data-stu-id="e0d24-236">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="e0d24-237">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="e0d24-237">AzureRM.Network</span></span>
* <span data-ttu-id="e0d24-238">В командлеты Наблюдателя за сетями добавлены параметры Аналитики трафика.</span><span class="sxs-lookup"><span data-stu-id="e0d24-238">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="e0d24-239">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="e0d24-239">AzureRM.Resources</span></span>
* <span data-ttu-id="e0d24-240">Исправлена ошибка, когда командлет Get-AzureRmResource возвращает свойство Properties объектов PSResource.</span><span class="sxs-lookup"><span data-stu-id="e0d24-240">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="e0d24-241">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="e0d24-241">AzureRM.Scheduler</span></span>
* <span data-ttu-id="e0d24-242">Исправлена ошибка, когда обновление ServiceBusQueueJob не задает новые значения для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="e0d24-242">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="e0d24-243">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="e0d24-243">AzureRM.Sql</span></span>
* <span data-ttu-id="e0d24-244">В перечисленные ниже командлеты добавлен необязательный параметр LicenseType.</span><span class="sxs-lookup"><span data-stu-id="e0d24-244">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="e0d24-245">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="e0d24-245">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="e0d24-246">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool;</span><span class="sxs-lookup"><span data-stu-id="e0d24-246">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="e0d24-247">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="e0d24-247">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="e0d24-248">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="e0d24-248">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="e0d24-249">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e0d24-249">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="e0d24-250">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="e0d24-250">AzureRM.Websites</span></span>
* <span data-ttu-id="e0d24-251">Командлет New-AzureRMWebApp теперь использует общие алгоритмы из библиотеки Strategy.</span><span class="sxs-lookup"><span data-stu-id="e0d24-251">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="e0d24-252">6.1.0 — май 2018 г.</span><span class="sxs-lookup"><span data-stu-id="e0d24-252">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="e0d24-253">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="e0d24-253">AzureRM.Profile</span></span>
* <span data-ttu-id="e0d24-254">Устранена проблема с выполнением Clear-AzureRmContext, при которой сохранялся пустой контекст с именем предыдущего контекста по умолчанию, что не позволяло пользователю создать новый контекст со старым именем.</span><span class="sxs-lookup"><span data-stu-id="e0d24-254">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="e0d24-255">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e0d24-255">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="e0d24-256">Включены операции связывания и отмены связи в автономной системе.</span><span class="sxs-lookup"><span data-stu-id="e0d24-256">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="e0d24-257">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e0d24-257">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="e0d24-258">Добавлена поддержка ApiVersions, ApiReleases и ApiRevisions.</span><span class="sxs-lookup"><span data-stu-id="e0d24-258">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="e0d24-259">Добавлена поддержка серверной части ServiceFabric.</span><span class="sxs-lookup"><span data-stu-id="e0d24-259">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="e0d24-260">Добавлена поддержка средства ведения журнала Application Insights.</span><span class="sxs-lookup"><span data-stu-id="e0d24-260">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="e0d24-261">Добавлена поддержка для распознавания номера SKU уровня "Базовый" как допустимого номера SKU службы управления API.</span><span class="sxs-lookup"><span data-stu-id="e0d24-261">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="e0d24-262">Добавлена поддержка установки сертификатов, выданных частным центром сертификации в качестве корневого или обычного ЦС.</span><span class="sxs-lookup"><span data-stu-id="e0d24-262">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="e0d24-263">Добавлена поддержка для приема пользовательских SSL-сертификатов с помощью KeyVault и нескольких имен узлов прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="e0d24-263">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="e0d24-264">Добавлена поддержка для удостоверения MSI.</span><span class="sxs-lookup"><span data-stu-id="e0d24-264">Added support for MSI identity</span></span>
* <span data-ttu-id="e0d24-265">Добавлена поддержка для принятия политик с помощью URL-адреса. Примечание. Указанные ниже командлеты в следующей версии будут отмечены как нерекомендуемые.</span><span class="sxs-lookup"><span data-stu-id="e0d24-265">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="e0d24-266">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="e0d24-266">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="e0d24-267">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="e0d24-267">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="e0d24-268">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="e0d24-268">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="e0d24-269">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="e0d24-269">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="e0d24-270">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="e0d24-270">AzureRM.Batch</span></span>
* <span data-ttu-id="e0d24-271">Выпущен новый командлет Get-AzureBatchPoolNodeCounts.</span><span class="sxs-lookup"><span data-stu-id="e0d24-271">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="e0d24-272">Выпущен новый командлет Start-AzureBatchComputeNodeServiceLogUpload.</span><span class="sxs-lookup"><span data-stu-id="e0d24-272">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="e0d24-273">AzureRM.Consumption:</span><span class="sxs-lookup"><span data-stu-id="e0d24-273">AzureRM.Consumption</span></span>
* <span data-ttu-id="e0d24-274">Добавлены новые параметры Expand, ResourceGroup, InstanceName, InstanceId, Tags и командлет высшего уровня Get-AzureRmConsumptionUsageDetail.</span><span class="sxs-lookup"><span data-stu-id="e0d24-274">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="e0d24-275">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e0d24-275">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="e0d24-276">Исправлен пример для Export-AzureRmDataLakeStoreChildItemProperties.</span><span class="sxs-lookup"><span data-stu-id="e0d24-276">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="e0d24-277">Исправлено исключение параметра NULL при использовании рекурсии в Set-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="e0d24-277">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="e0d24-278">Исправлены файлы справки для Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl и Remove-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="e0d24-278">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="e0d24-279">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="e0d24-279">AzureRM.Network</span></span>
* <span data-ttu-id="e0d24-280">Пакет SDK для сети обновлен с предварительной версии 18.0.0 до предварительной версии 19.0.0.</span><span class="sxs-lookup"><span data-stu-id="e0d24-280">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="e0d24-281">Добавлен командлет для создания конфигурации протокола.</span><span class="sxs-lookup"><span data-stu-id="e0d24-281">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="e0d24-282">New-AzureRmNetworkWatcherProtocolConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e0d24-282">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="e0d24-283">Добавлен командлет для добавления нового подключения канала к существующему каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e0d24-283">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="e0d24-284">Add-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="e0d24-284">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="e0d24-285">Добавлен командлет для удаления подключения канала к существующему каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e0d24-285">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="e0d24-286">Remove-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="e0d24-286">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="e0d24-287">Добавлен командлет для получения подключения канала.</span><span class="sxs-lookup"><span data-stu-id="e0d24-287">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="e0d24-288">Get-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="e0d24-288">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="e0d24-289">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e0d24-289">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="e0d24-290">Исправлена процедура аутентификации сервера с использованием созданных сертификатов (проблема № 5998).</span><span class="sxs-lookup"><span data-stu-id="e0d24-290">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="e0d24-291">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="e0d24-291">AzureRM.Sql</span></span>
* <span data-ttu-id="e0d24-292">Обновлены командлеты аудита, которые теперь позволяют удалять AuditActions или AuditActionGroups.</span><span class="sxs-lookup"><span data-stu-id="e0d24-292">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="e0d24-293">Исправлена проблема с Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy, при которой установка новой гибкой политики хранения завершалась ошибкой с сообщением "Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span><span class="sxs-lookup"><span data-stu-id="e0d24-293">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="e0d24-294">Please submit request with the new flexible retention policy" (Настройка политики долгосрочного хранения с помощью хранилища и политики служб восстановления Azure больше не поддерживается. Отправьте запрос с использованием новой гибкой политики хранения).</span><span class="sxs-lookup"><span data-stu-id="e0d24-294">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="e0d24-295">Обновлены все командлеты, связанные со службой "База данных SQL Azure", с созданием эластичных пулов и обновлением. Теперь используются новые API баз данных с поддержкой свойства номеров SKU для обеспечения масштабируемости и связанных с уровнями возможностей.</span><span class="sxs-lookup"><span data-stu-id="e0d24-295">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="e0d24-296">Обновлены командлеты, в том числе:</span><span class="sxs-lookup"><span data-stu-id="e0d24-296">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="e0d24-297">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="e0d24-297">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="e0d24-298">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool;</span><span class="sxs-lookup"><span data-stu-id="e0d24-298">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="e0d24-299">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="e0d24-299">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="e0d24-300">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="e0d24-300">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="e0d24-301">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e0d24-301">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="e0d24-302">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="e0d24-302">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="e0d24-303">Обновлены параметры для Get-AzureRmTrafficManagerProfile. Теперь при использовании параметра -Name требуется параметр -ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="e0d24-303">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>