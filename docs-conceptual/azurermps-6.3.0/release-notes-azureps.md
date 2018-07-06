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
ms.openlocfilehash: 3811e28dda69d194d23934943fb47d562f869fc4
ms.sourcegitcommit: 5a5b6dd216d5f805204244146cf6f88ad2f34fb4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2018
ms.locfileid: "36237819"
---
# <a name="release-notes"></a><span data-ttu-id="05c5b-103">Заметки о выпуске</span><span class="sxs-lookup"><span data-stu-id="05c5b-103">Release notes</span></span>

<span data-ttu-id="05c5b-104">Здесь приведен список изменений, внесенных в Azure PowerShell в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="05c5b-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="630---june-2018"></a><span data-ttu-id="05c5b-105">6.3.0 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="05c5b-105">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="05c5b-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="05c5b-106">AzureRM.Profile</span></span>
* <span data-ttu-id="05c5b-107">Обновлены сообщения об ошибках для Enable-AzureRmContextAutoSave.</span><span class="sxs-lookup"><span data-stu-id="05c5b-107">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="05c5b-108">Создание контекста для каждой подписки при выполнении Connect-AzureRmAccount без предыдущего контекста.</span><span class="sxs-lookup"><span data-stu-id="05c5b-108">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="05c5b-109">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="05c5b-109">Azure.Storage</span></span>
* <span data-ttu-id="05c5b-110">В файлы справки добавлены дополнительные сведения о параметре -Permissions.</span><span class="sxs-lookup"><span data-stu-id="05c5b-110">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="05c5b-111">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="05c5b-111">AzureRM.Compute</span></span>
* <span data-ttu-id="05c5b-112">Get-AzureRmVmDiskEncryptionStatus устраняет проблему, которая наблюдалась на виртуальных машинах без дисков данных.</span><span class="sxs-lookup"><span data-stu-id="05c5b-112">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="05c5b-113">Обновлена версия клиентской библиотеки Compute для исправления следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="05c5b-113">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="05c5b-114">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="05c5b-114">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="05c5b-115">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="05c5b-115">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="05c5b-116">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="05c5b-116">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="05c5b-117">В следующих командлетах исправлено отображение неправильных значений operation ID и operation status:</span><span class="sxs-lookup"><span data-stu-id="05c5b-117">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="05c5b-118">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="05c5b-118">Start-AzureRmVM</span></span>
    - <span data-ttu-id="05c5b-119">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="05c5b-119">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="05c5b-120">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="05c5b-120">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="05c5b-121">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="05c5b-121">Set-AzureRmVM</span></span>
    - <span data-ttu-id="05c5b-122">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="05c5b-122">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="05c5b-123">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="05c5b-123">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="05c5b-124">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="05c5b-124">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="05c5b-125">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="05c5b-125">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="05c5b-126">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="05c5b-126">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="05c5b-127">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="05c5b-127">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="05c5b-128">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="05c5b-128">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="05c5b-129">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="05c5b-129">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="05c5b-130">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="05c5b-130">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="05c5b-131">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="05c5b-131">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="05c5b-132">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="05c5b-132">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="05c5b-133">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="05c5b-133">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="05c5b-134">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="05c5b-134">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="05c5b-135">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="05c5b-135">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="05c5b-136">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="05c5b-136">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="05c5b-137">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="05c5b-137">AzureRM.EventGrid</span></span>
* <span data-ttu-id="05c5b-138">Удалены условия проверки ValidateNotNullOrEmpty для SubjectBeginsWith/SubjectEndsWith в командлете Update-AzureRmEventGridSubscription, что позволяет при необходимости заменять эти параметры пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="05c5b-138">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="05c5b-139">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="05c5b-139">AzureRM.KeyVault</span></span>
* <span data-ttu-id="05c5b-140">Исправлена ошибка, когда при выполнении командлета Get-AzureRmKeyVault -Tag не возвращается ни один тег.</span><span class="sxs-lookup"><span data-stu-id="05c5b-140">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="05c5b-141">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="05c5b-141">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="05c5b-142">Общедоступный выпуск командлетов Policy Insights.</span><span class="sxs-lookup"><span data-stu-id="05c5b-142">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="05c5b-143">Используется API версии 2018-04-04.</span><span class="sxs-lookup"><span data-stu-id="05c5b-143">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="05c5b-144">К результатам Get-AzureRmPolicyStateSummary добавлено PolicyDefinitionReferenceId.</span><span class="sxs-lookup"><span data-stu-id="05c5b-144">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="05c5b-145">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="05c5b-145">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="05c5b-146">Для командлетов RecoveryServices.Backup добавлен параметр -Vault.</span><span class="sxs-lookup"><span data-stu-id="05c5b-146">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="05c5b-147">Передача этого параметра переопределяет командлет Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="05c5b-147">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="05c5b-148">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="05c5b-148">AzureRM.Sql</span></span>
* <span data-ttu-id="05c5b-149">В файле справки обновлен пример для командлета Get-AzureRmSqlDatabaseExpanded.</span><span class="sxs-lookup"><span data-stu-id="05c5b-149">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="05c5b-150">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="05c5b-150">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="05c5b-151">Обновлен файл справки для командлета Add-AzureRmTrafficManagerEndpointConfig.</span><span class="sxs-lookup"><span data-stu-id="05c5b-151">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="05c5b-152">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="05c5b-152">AzureRM.Websites</span></span>
* <span data-ttu-id="05c5b-153">Изменено действие командлета Set-AzureRmWebApp. Теперь он не перезаписывает AppSettings, если используется параметр -AssignIdentity.</span><span class="sxs-lookup"><span data-stu-id="05c5b-153">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="05c5b-154">Командлет New-AzureRmWebAppSlot теперь учитывает дополнительный параметр AppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="05c5b-154">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="05c5b-155">6.2.1 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="05c5b-155">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="05c5b-156">AzureRM.OperationalInsights;</span><span class="sxs-lookup"><span data-stu-id="05c5b-156">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="05c5b-157">В обновленной модели PSWorkspace Network может использовать type в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="05c5b-157">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="05c5b-158">6.2.0 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="05c5b-158">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="05c5b-159">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="05c5b-159">AzureRM.Profile</span></span>
* <span data-ttu-id="05c5b-160">Исправлена ошибка с загрузкой Newtonsoft.Json версии 10.0.3 во время импорта модуля.</span><span class="sxs-lookup"><span data-stu-id="05c5b-160">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="05c5b-161">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="05c5b-161">AzureRM.Compute</span></span>
* <span data-ttu-id="05c5b-162">Функция обновления виртуальных машин VMSS.</span><span class="sxs-lookup"><span data-stu-id="05c5b-162">VMSS VM Update feature</span></span>
    - <span data-ttu-id="05c5b-163">Добавлены командлеты Update-AzureRmVmssVM и New-AzureRmVMDataDisk.</span><span class="sxs-lookup"><span data-stu-id="05c5b-163">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="05c5b-164">В командлет Add-AzureRmVMDataDisk добавлен параметр VirtualMachineScaleSetVM, который позволяет добавлять диски данных в виртуальные машины VMSS.</span><span class="sxs-lookup"><span data-stu-id="05c5b-164">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="05c5b-165">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="05c5b-165">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="05c5b-166">Пакет SDK для ADF .NET обновлен до версии 0.8.0-preview. Новая версия содержит такие изменения:</span><span class="sxs-lookup"><span data-stu-id="05c5b-166">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="05c5b-167">добавлена операция для настройки репозитория фабрики;</span><span class="sxs-lookup"><span data-stu-id="05c5b-167">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="05c5b-168">связанная служба QuickBooks LinkedService теперь предоставляет свойства consumerKey и consumerSecret;</span><span class="sxs-lookup"><span data-stu-id="05c5b-168">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="05c5b-169">тип нескольких моделей изменен с SecretBase на Object;</span><span class="sxs-lookup"><span data-stu-id="05c5b-169">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="05c5b-170">добавлен триггер событий BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="05c5b-170">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="05c5b-171">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="05c5b-171">AzureRM.KeyVault</span></span>
* <span data-ttu-id="05c5b-172">В документацию добавлены примеры выходных данных.</span><span class="sxs-lookup"><span data-stu-id="05c5b-172">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="05c5b-173">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="05c5b-173">AzureRM.Network</span></span>
* <span data-ttu-id="05c5b-174">В командлеты Наблюдателя за сетями добавлены параметры Аналитики трафика.</span><span class="sxs-lookup"><span data-stu-id="05c5b-174">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="05c5b-175">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="05c5b-175">AzureRM.Resources</span></span>
* <span data-ttu-id="05c5b-176">Исправлена ошибка, когда командлет Get-AzureRmResource возвращает свойство Properties объектов PSResource.</span><span class="sxs-lookup"><span data-stu-id="05c5b-176">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="05c5b-177">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="05c5b-177">AzureRM.Scheduler</span></span>
* <span data-ttu-id="05c5b-178">Исправлена ошибка, когда обновление ServiceBusQueueJob не задает новые значения для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="05c5b-178">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="05c5b-179">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="05c5b-179">AzureRM.Sql</span></span>
* <span data-ttu-id="05c5b-180">В перечисленные ниже командлеты добавлен необязательный параметр LicenseType.</span><span class="sxs-lookup"><span data-stu-id="05c5b-180">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="05c5b-181">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="05c5b-181">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="05c5b-182">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool;</span><span class="sxs-lookup"><span data-stu-id="05c5b-182">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="05c5b-183">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="05c5b-183">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="05c5b-184">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="05c5b-184">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="05c5b-185">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="05c5b-185">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="05c5b-186">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="05c5b-186">AzureRM.Websites</span></span>
* <span data-ttu-id="05c5b-187">Командлет New-AzureRMWebApp теперь использует общие алгоритмы из библиотеки Strategy.</span><span class="sxs-lookup"><span data-stu-id="05c5b-187">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="05c5b-188">6.1.0 — май 2018 г.</span><span class="sxs-lookup"><span data-stu-id="05c5b-188">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="05c5b-189">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="05c5b-189">AzureRM.Profile</span></span>
* <span data-ttu-id="05c5b-190">Устранена проблема с выполнением Clear-AzureRmContext, при которой сохранялся пустой контекст с именем предыдущего контекста по умолчанию, что не позволяло пользователю создать новый контекст со старым именем.</span><span class="sxs-lookup"><span data-stu-id="05c5b-190">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="05c5b-191">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="05c5b-191">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="05c5b-192">Включены операции связывания и отмены связи в автономной системе.</span><span class="sxs-lookup"><span data-stu-id="05c5b-192">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="05c5b-193">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="05c5b-193">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="05c5b-194">Добавлена поддержка ApiVersions, ApiReleases и ApiRevisions.</span><span class="sxs-lookup"><span data-stu-id="05c5b-194">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="05c5b-195">Добавлена поддержка серверной части ServiceFabric.</span><span class="sxs-lookup"><span data-stu-id="05c5b-195">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="05c5b-196">Добавлена поддержка средства ведения журнала Application Insights.</span><span class="sxs-lookup"><span data-stu-id="05c5b-196">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="05c5b-197">Добавлена поддержка для распознавания номера SKU уровня "Базовый" как допустимого номера SKU службы управления API.</span><span class="sxs-lookup"><span data-stu-id="05c5b-197">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="05c5b-198">Добавлена поддержка установки сертификатов, выданных частным центром сертификации в качестве корневого или обычного ЦС.</span><span class="sxs-lookup"><span data-stu-id="05c5b-198">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="05c5b-199">Добавлена поддержка для приема пользовательских SSL-сертификатов с помощью KeyVault и нескольких имен узлов прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="05c5b-199">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="05c5b-200">Добавлена поддержка для удостоверения MSI.</span><span class="sxs-lookup"><span data-stu-id="05c5b-200">Added support for MSI identity</span></span>
* <span data-ttu-id="05c5b-201">Добавлена поддержка для принятия политик с помощью URL-адреса. Примечание. Указанные ниже командлеты в следующей версии будут отмечены как нерекомендуемые.</span><span class="sxs-lookup"><span data-stu-id="05c5b-201">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="05c5b-202">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="05c5b-202">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="05c5b-203">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="05c5b-203">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="05c5b-204">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="05c5b-204">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="05c5b-205">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="05c5b-205">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="05c5b-206">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="05c5b-206">AzureRM.Batch</span></span>
* <span data-ttu-id="05c5b-207">Выпущен новый командлет Get-AzureBatchPoolNodeCounts.</span><span class="sxs-lookup"><span data-stu-id="05c5b-207">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="05c5b-208">Выпущен новый командлет Start-AzureBatchComputeNodeServiceLogUpload.</span><span class="sxs-lookup"><span data-stu-id="05c5b-208">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="05c5b-209">AzureRM.Consumption:</span><span class="sxs-lookup"><span data-stu-id="05c5b-209">AzureRM.Consumption</span></span>
* <span data-ttu-id="05c5b-210">Добавлены новые параметры Expand, ResourceGroup, InstanceName, InstanceId, Tags и командлет высшего уровня Get-AzureRmConsumptionUsageDetail.</span><span class="sxs-lookup"><span data-stu-id="05c5b-210">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="05c5b-211">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="05c5b-211">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="05c5b-212">Исправлен пример для Export-AzureRmDataLakeStoreChildItemProperties.</span><span class="sxs-lookup"><span data-stu-id="05c5b-212">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="05c5b-213">Исправлено исключение параметра NULL при использовании рекурсии в Set-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="05c5b-213">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="05c5b-214">Исправлены файлы справки для Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl и Remove-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="05c5b-214">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="05c5b-215">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="05c5b-215">AzureRM.Network</span></span>
* <span data-ttu-id="05c5b-216">Пакет SDK для сети обновлен с предварительной версии 18.0.0 до предварительной версии 19.0.0.</span><span class="sxs-lookup"><span data-stu-id="05c5b-216">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="05c5b-217">Добавлен командлет для создания конфигурации протокола.</span><span class="sxs-lookup"><span data-stu-id="05c5b-217">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="05c5b-218">New-AzureRmNetworkWatcherProtocolConfiguration.</span><span class="sxs-lookup"><span data-stu-id="05c5b-218">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="05c5b-219">Добавлен командлет для добавления нового подключения канала к существующему каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="05c5b-219">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="05c5b-220">Add-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="05c5b-220">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="05c5b-221">Добавлен командлет для удаления подключения канала к существующему каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="05c5b-221">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="05c5b-222">Remove-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="05c5b-222">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="05c5b-223">Добавлен командлет для получения подключения канала.</span><span class="sxs-lookup"><span data-stu-id="05c5b-223">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="05c5b-224">Get-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="05c5b-224">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="05c5b-225">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="05c5b-225">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="05c5b-226">Исправлена процедура аутентификации сервера с использованием созданных сертификатов (проблема № 5998).</span><span class="sxs-lookup"><span data-stu-id="05c5b-226">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="05c5b-227">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="05c5b-227">AzureRM.Sql</span></span>
* <span data-ttu-id="05c5b-228">Обновлены командлеты аудита, которые теперь позволяют удалять AuditActions или AuditActionGroups.</span><span class="sxs-lookup"><span data-stu-id="05c5b-228">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="05c5b-229">Исправлена проблема с Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy, при которой установка новой гибкой политики хранения завершалась ошибкой с сообщением "Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span><span class="sxs-lookup"><span data-stu-id="05c5b-229">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="05c5b-230">Please submit request with the new flexible retention policy" (Настройка политики долгосрочного хранения с помощью хранилища и политики служб восстановления Azure больше не поддерживается. Отправьте запрос с использованием новой гибкой политики хранения).</span><span class="sxs-lookup"><span data-stu-id="05c5b-230">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="05c5b-231">Обновлены все командлеты, связанные со службой "База данных SQL Azure", с созданием эластичных пулов и обновлением. Теперь используются новые API баз данных с поддержкой свойства номеров SKU для обеспечения масштабируемости и связанных с уровнями возможностей.</span><span class="sxs-lookup"><span data-stu-id="05c5b-231">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="05c5b-232">Обновлены командлеты, в том числе:</span><span class="sxs-lookup"><span data-stu-id="05c5b-232">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="05c5b-233">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="05c5b-233">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="05c5b-234">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool;</span><span class="sxs-lookup"><span data-stu-id="05c5b-234">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="05c5b-235">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="05c5b-235">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="05c5b-236">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="05c5b-236">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="05c5b-237">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="05c5b-237">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="05c5b-238">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="05c5b-238">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="05c5b-239">Обновлены параметры для Get-AzureRmTrafficManagerProfile. Теперь при использовании параметра -Name требуется параметр -ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="05c5b-239">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>