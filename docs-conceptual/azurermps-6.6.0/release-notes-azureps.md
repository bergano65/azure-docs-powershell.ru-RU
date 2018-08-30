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
ms.openlocfilehash: 340c1d2d28e1b97cdd2ec98033361eb00b4302da
ms.sourcegitcommit: 72086f8d368ec84bd403e802305acfc336c08978
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/14/2018
ms.locfileid: "43019064"
---
# <a name="release-notes"></a><span data-ttu-id="27533-103">Заметки о выпуске</span><span class="sxs-lookup"><span data-stu-id="27533-103">Release notes</span></span>

<span data-ttu-id="27533-104">Здесь приведен список изменений, внесенных в Azure PowerShell в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="27533-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="660---july-2018"></a><span data-ttu-id="27533-105">6.6.0 — июль 2018 г.</span><span class="sxs-lookup"><span data-stu-id="27533-105">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="27533-106">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="27533-106">General</span></span>
* <span data-ttu-id="27533-107">Обновлены все файлы справки: включены полные типы параметров и исправлены типы входных и выходных данных.</span><span class="sxs-lookup"><span data-stu-id="27533-107">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="27533-108">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="27533-108">AzureRM.Profile</span></span>
* <span data-ttu-id="27533-109">Обновлена библиотека Common.Strategy: теперь можно проверить, совместима ли текущая конфигурация ресурса с целевым ресурсом.</span><span class="sxs-lookup"><span data-stu-id="27533-109">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="27533-110">В Common.Storage добавлены типы ps1xml.</span><span class="sxs-lookup"><span data-stu-id="27533-110">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="27533-111">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="27533-111">Azure.Storage</span></span>
* <span data-ttu-id="27533-112">Добавлена поддержка для получения контекста хранилища из DefaultProfile.</span><span class="sxs-lookup"><span data-stu-id="27533-112">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="27533-113">В свойства типов выходных данных командлетов добавлен атрибут Ps1XmlAttribute.</span><span class="sxs-lookup"><span data-stu-id="27533-113">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="27533-114">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="27533-114">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="27533-115">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6370.</span><span class="sxs-lookup"><span data-stu-id="27533-115">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="27533-116">В AutoMapper исправлена ошибка, препятствовавшая преобразованию PsApiManagementApi в ApiContract.</span><span class="sxs-lookup"><span data-stu-id="27533-116">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="27533-117">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6515.</span><span class="sxs-lookup"><span data-stu-id="27533-117">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="27533-118">В File.Save исправлена ошибка, связанная с перегрузкой типом кодировки.</span><span class="sxs-lookup"><span data-stu-id="27533-118">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="27533-119">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6560.</span><span class="sxs-lookup"><span data-stu-id="27533-119">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="27533-120">Выполнено обновление до версии NuGet 4.0.3, что позволило исправить исключение шаблона в apiId.</span><span class="sxs-lookup"><span data-stu-id="27533-120">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="27533-121">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="27533-121">AzureRM.Compute</span></span>
* <span data-ttu-id="27533-122">Устранена ошибка при создании виртуальной машины с помощью командлета New-AzureRmVm и параметра DiskFileParameterSet, которая возникала из-за переименования типа учетной записи хранения PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="27533-122">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="27533-123">Исправлен командлет Invoke-AzureRmVMRunCommand.</span><span class="sxs-lookup"><span data-stu-id="27533-123">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="27533-124">Командлет Get-AzureRmAvailabilitySet теперь может выводить список всех групп доступности в подписке.</span><span class="sxs-lookup"><span data-stu-id="27533-124">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="27533-125">(Параметр ResouceGroupName теперь является необязательным.)</span><span class="sxs-lookup"><span data-stu-id="27533-125">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="27533-126">Обновлен параметр SimpleParameterSet командлета New-AzureRmVm, что позволило использовать ускоренную сеть на соответствующих виртуальных машинах.</span><span class="sxs-lookup"><span data-stu-id="27533-126">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="27533-127">Обновлен простой набор параметров New-AzureRmVmss, что позволило отменять создание масштабируемого набора виртуальных машин, если указанная пользователем подсистема балансировки нагрузки уже существует.</span><span class="sxs-lookup"><span data-stu-id="27533-127">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="27533-128">Обновлен пример для New-AzureRmDisk.</span><span class="sxs-lookup"><span data-stu-id="27533-128">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="27533-129">Добавлен пример для New-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="27533-129">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="27533-130">Обновлено описание командлета Set-AzureRmVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="27533-130">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="27533-131">Обновлен пример 1 для Set-AzureRmVMBginfoExtension: исправлены орфографические ошибки и префикс.</span><span class="sxs-lookup"><span data-stu-id="27533-131">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="27533-132">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="27533-132">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="27533-133">Пакет .NET SDK для ADF обновлен до версии 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="27533-133">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="27533-134">Добавлена поддержка совместного использования локальной среды IR несколькими фабриками данных.</span><span class="sxs-lookup"><span data-stu-id="27533-134">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="27533-135">Добавлен новый параметр -SharedIntegrationRuntimeResourceId для командлета Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="27533-135">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="27533-136">Добавлен новый необязательный параметр -LinkedDataFactoryName для командлета Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="27533-136">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="27533-137">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27533-137">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="27533-138">Пакет SDK для плоскости данных (Microsoft.Azure.DataLake.Store) обновлен до версии 1.1.9.</span><span class="sxs-lookup"><span data-stu-id="27533-138">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="27533-139">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="27533-139">AzureRM.EventHub</span></span>
* <span data-ttu-id="27533-140">Обновлена конвейерная передача для InputObject и ResourceId в командлетах remove.</span><span class="sxs-lookup"><span data-stu-id="27533-140">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="27533-141">AzureRM.Insights;</span><span class="sxs-lookup"><span data-stu-id="27533-141">AzureRM.Insights</span></span>
* <span data-ttu-id="27533-142">Исправлено форматирование OutputType в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="27533-142">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="27533-143">Применен пакет SDK Microsoft.Azure.Management.Monitor 0.19.1-preview.</span><span class="sxs-lookup"><span data-stu-id="27533-143">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="27533-144">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="27533-144">AzureRM.KeyVault</span></span>
* <span data-ttu-id="27533-145">Исправлена проблема с конвейерной передачей в командлете Set-AzureRmKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="27533-145">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="27533-146">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="27533-146">AzureRM.Network</span></span>
* <span data-ttu-id="27533-147">Добавлены примеры для командлетов LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="27533-147">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="27533-148">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="27533-148">AzureRM.Resources</span></span>
* <span data-ttu-id="27533-149">Устранена проблема, возникавшая при указании имени и значения тега для Get-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="27533-149">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="27533-150">Исправлен сценарий конвейерной передачи в Set-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="27533-150">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="27533-151">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="27533-151">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="27533-152">Обновлена конвейерная передача для InputObject и ResourceId в командлетах remove.</span><span class="sxs-lookup"><span data-stu-id="27533-152">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="27533-153">Исправлено несколько ошибок.</span><span class="sxs-lookup"><span data-stu-id="27533-153">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="27533-154">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="27533-154">AzureRM.Sql</span></span>
* <span data-ttu-id="27533-155">Добавлена поддержка Advanced Threat Protection для сервера с помощью следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="27533-155">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="27533-156">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="27533-156">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="27533-157">Добавлена поддержка оценки уязвимостей с помощью следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="27533-157">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="27533-158">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings;</span><span class="sxs-lookup"><span data-stu-id="27533-158">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="27533-159">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline;</span><span class="sxs-lookup"><span data-stu-id="27533-159">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="27533-160">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan.</span><span class="sxs-lookup"><span data-stu-id="27533-160">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="27533-161">Исправлен пример для Remove-AzureRmSqlServerFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="27533-161">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="27533-162">Исправлена неправильная обработка даты и времени для базового языка и региональных параметров, отличных от США, в Get-AzureSqlSyncGroupLog.</span><span class="sxs-lookup"><span data-stu-id="27533-162">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="27533-163">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="27533-163">AzureRM.Storage</span></span>
* <span data-ttu-id="27533-164">В свойства типов выходных данных командлетов добавлен атрибут Ps1XmlAttribute.</span><span class="sxs-lookup"><span data-stu-id="27533-164">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="27533-165">Выходные данные командлетов StorageAccount теперь отображаются в виде таблицы.</span><span class="sxs-lookup"><span data-stu-id="27533-165">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="27533-166">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27533-166">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="27533-167">New-AzureRmStorageAccount;</span><span class="sxs-lookup"><span data-stu-id="27533-167">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="27533-168">Set-AzureRmStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="27533-168">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="27533-169">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="27533-169">AzureRM.Tags</span></span>
* <span data-ttu-id="27533-170">Удалено неверное утверждение из справки по командлетам Tag.</span><span class="sxs-lookup"><span data-stu-id="27533-170">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="27533-171">6.5.0 — июль 2018 г.</span><span class="sxs-lookup"><span data-stu-id="27533-171">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="27533-172">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="27533-172">AzureRM.Profile</span></span>
* <span data-ttu-id="27533-173">Обновлена справка для командлета Get-AzureRmContextAutosaveSetting.</span><span class="sxs-lookup"><span data-stu-id="27533-173">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="27533-174">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="27533-174">Azure.Storage</span></span>
* <span data-ttu-id="27533-175">Добавлена поддержка отправки BLOB-объекта или файла с помощью токена SAS, доступного только для записи.</span><span class="sxs-lookup"><span data-stu-id="27533-175">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="27533-176">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="27533-176">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="27533-177">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="27533-177">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="27533-178">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="27533-178">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="27533-179">Для AS добавлено обязательное свойство ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="27533-179">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="27533-180">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="27533-180">AzureRM.Automation</span></span>
* <span data-ttu-id="27533-181">Обновлена справка и добавлены примеры для командлета New-AzureRMAutomationSchedule.</span><span class="sxs-lookup"><span data-stu-id="27533-181">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="27533-182">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="27533-182">AzureRM.Compute</span></span>
* <span data-ttu-id="27533-183">Добавлен параметр -Tag для командлета Update/New-AzureRmAvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="27533-183">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="27533-184">Добавлен пример для командлета Add-AzureRmVmssExtension.</span><span class="sxs-lookup"><span data-stu-id="27533-184">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="27533-185">Добавлены примеры для командлета Remove-AzureRmVmssExtension.</span><span class="sxs-lookup"><span data-stu-id="27533-185">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="27533-186">Обновлена справка для командлета Set-AzureRmVMAccessExtension.</span><span class="sxs-lookup"><span data-stu-id="27533-186">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="27533-187">Изменен класс SimpleParameterSet для командлета New-AzureRmVmss: теперь для SinglePlacementGroup по умолчанию задается значение false, а также добавляется параметр-переключатель SinglePlacementGroup, который позволяет пользователю создать VMSS в одной группе размещения.</span><span class="sxs-lookup"><span data-stu-id="27533-187">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="27533-188">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="27533-188">AzureRM.EventHub</span></span>
* <span data-ttu-id="27533-189">В класс PSEventHubDRConfigurationAttributes добавлено доступное только для чтения свойство PendingReplicationOperationsCount, которое показывает количество ожидающих репликации операций во время реплицирования.</span><span class="sxs-lookup"><span data-stu-id="27533-189">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="27533-190">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="27533-190">AzureRM.KeyVault</span></span>
* <span data-ttu-id="27533-191">Обновлено сообщение об ошибке для командлета Set-AzureRmKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="27533-191">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="27533-192">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="27533-192">AzureRM.LogicApp</span></span>
* <span data-ttu-id="27533-193">Исправлена ошибка "parameter set could not be resolved" (не удалось разрешить заданный параметр) в командлете New-AzureRmLogicApp.</span><span class="sxs-lookup"><span data-stu-id="27533-193">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="27533-194">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="27533-194">AzureRM.Network</span></span>
* <span data-ttu-id="27533-195">Включен пиринг между виртуальными сетями в нескольких клиентах для командлета Set/Add-AzureRmVirtualNetworkPeering.</span><span class="sxs-lookup"><span data-stu-id="27533-195">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="27533-196">Для шлюза приложений обновлены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="27533-196">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="27533-197">New-AzureRmApplicationGateway: добавлены флаг EnableFIPS и поддержка зон.</span><span class="sxs-lookup"><span data-stu-id="27533-197">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="27533-198">New-AzureRmApplicationGatewaySku: добавлены новые номера SKU Standard_v2 и WAF_v2.</span><span class="sxs-lookup"><span data-stu-id="27533-198">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="27533-199">Set-AzureRmApplicationGatewaySku: добавлены новые номера SKU Standard_v2 и WAF_v2.</span><span class="sxs-lookup"><span data-stu-id="27533-199">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="27533-200">Командлеты RouteTable пересозданы в последней версии генератора.</span><span class="sxs-lookup"><span data-stu-id="27533-200">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="27533-201">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="27533-201">AzureRM.Relay</span></span>
* <span data-ttu-id="27533-202">Обновлены файлы Markdown, исправлена проблема с именем параметра в примере.</span><span class="sxs-lookup"><span data-stu-id="27533-202">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="27533-203">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="27533-203">AzureRM.Resources</span></span>
* <span data-ttu-id="27533-204">Обновлены командлеты Roleassignment и roledefinition:</span><span class="sxs-lookup"><span data-stu-id="27533-204">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="27533-205">Удалены лишние вызовы roledefinition, выполняемые в ходе разбиения на страницы.</span><span class="sxs-lookup"><span data-stu-id="27533-205">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="27533-206">Исправлен командлет Get-AzureRmRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="27533-206">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="27533-207">Исправлена работа параметра -ExpandPrincipalGroups.</span><span class="sxs-lookup"><span data-stu-id="27533-207">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="27533-208">Устранена проблема в командлете Get-AzureRmResource, заключающая в том, что в параметре -ResourceType учитывался регистр символов.</span><span class="sxs-lookup"><span data-stu-id="27533-208">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="27533-209">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="27533-209">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="27533-210">Добавлены параметры top и skip для командлетов list.</span><span class="sxs-lookup"><span data-stu-id="27533-210">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="27533-211">Добавлены командлеты для перехода с пространства имен ценовой категории "Стандартный" на пространство ценовой категории "Премиум":</span><span class="sxs-lookup"><span data-stu-id="27533-211">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="27533-212">Start-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="27533-212">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="27533-213">Get-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="27533-213">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="27533-214">Complete-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="27533-214">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="27533-215">Stop-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="27533-215">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="27533-216">Remove-AzureRmServiceBusMigration.</span><span class="sxs-lookup"><span data-stu-id="27533-216">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="27533-217">В класс PSServiceBusDRConfigurationAttributes добавлено доступное только для чтения свойство PendingReplicationOperationsCount, которое показывает количество ожидающих репликации операций во время реплицирования.</span><span class="sxs-lookup"><span data-stu-id="27533-217">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="27533-218">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="27533-218">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="27533-219">Обновлен пример для командлета New-AzureRmServiceFabricCluster.</span><span class="sxs-lookup"><span data-stu-id="27533-219">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="27533-220">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="27533-220">AzureRM.Sql</span></span>
* <span data-ttu-id="27533-221">Добавлены новые командлеты для Management.Sql, позволяющие клиентам добавлять сертификат TDE в экземпляр SQL Server или управляемый экземпляр:</span><span class="sxs-lookup"><span data-stu-id="27533-221">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="27533-222">Add-AzureRmSqlServerTransparentDataEncryptionCertificate;</span><span class="sxs-lookup"><span data-stu-id="27533-222">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="27533-223">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate.</span><span class="sxs-lookup"><span data-stu-id="27533-223">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="27533-224">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="27533-224">AzureRM.Websites</span></span>
* <span data-ttu-id="27533-225">`Set-AzureRmWebApp -AssignIdentity` и `Set-AzureRmWebAppSlot -AssignIdentity` при установленном значении false теперь будут удалять свойство Identity из объекта сайта. Также при этом будет удаляться тег предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="27533-225">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="27533-226">Обновлен пример для `Get-AzureRmWebAppMetrics` и `Get-AzureRmAppServicePlanMetrics`.</span><span class="sxs-lookup"><span data-stu-id="27533-226">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="27533-227">`Set-AzureRmWebApp -PhpVersion` теперь поддерживает off как допустимую версию PHP.</span><span class="sxs-lookup"><span data-stu-id="27533-227">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="27533-228">6.4.0 — июль 2018 г.</span><span class="sxs-lookup"><span data-stu-id="27533-228">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="27533-229">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="27533-229">General</span></span>
* <span data-ttu-id="27533-230">Исправлено форматирование OutputType в файлах справки для большинства модулей.</span><span class="sxs-lookup"><span data-stu-id="27533-230">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="27533-231">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="27533-231">AzureRM.Profile</span></span>
* <span data-ttu-id="27533-232">В основные типы выходных данных добавлен атрибут Ps1Xml.</span><span class="sxs-lookup"><span data-stu-id="27533-232">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="27533-233">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="27533-233">AzureRM.Compute</span></span>
* <span data-ttu-id="27533-234">Функция добавления тега IP-адреса для масштабируемого набора виртуальных машин (VMSS)</span><span class="sxs-lookup"><span data-stu-id="27533-234">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="27533-235">Добавлен командлет New-AzureRmVmssIpTagConfig.</span><span class="sxs-lookup"><span data-stu-id="27533-235">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="27533-236">В New-AzureRmVmssIpConfig добавлен параметр IpTag.</span><span class="sxs-lookup"><span data-stu-id="27533-236">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="27533-237">Функция автоматического отката ОС для VMSS</span><span class="sxs-lookup"><span data-stu-id="27533-237">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="27533-238">В New-AzureRmVmssConfig и Update-AzureRmVmss добавлены параметры DisableAutoRollback.</span><span class="sxs-lookup"><span data-stu-id="27533-238">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="27533-239">Функция ведения журнала обновлений ОС для VMSS</span><span class="sxs-lookup"><span data-stu-id="27533-239">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="27533-240">В Get-AzureRmVmss добавлен параметр OSUpgradeHistory.</span><span class="sxs-lookup"><span data-stu-id="27533-240">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="27533-241">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="27533-241">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="27533-242">Добавлена поддержка списков управления доступом к каталогу с использованием следующих команд:</span><span class="sxs-lookup"><span data-stu-id="27533-242">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="27533-243">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry;</span><span class="sxs-lookup"><span data-stu-id="27533-243">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="27533-244">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry;</span><span class="sxs-lookup"><span data-stu-id="27533-244">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="27533-245">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="27533-245">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="27533-246">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27533-246">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="27533-247">Добавлены поддержка отмены выполнения и отслеживание хода выполнения для Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl и Remove-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="27533-247">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="27533-248">Добавлена поддержка отмены выполнения для Export-AzureRmDataLakeStoreChildItemProperties.</span><span class="sxs-lookup"><span data-stu-id="27533-248">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="27533-249">Исправлена очистка сообщений об отладке для командлетов, которые выполняют рекурсивные операции.</span><span class="sxs-lookup"><span data-stu-id="27533-249">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="27533-250">Исправлено расположение тестовых данных для командлетов DataLake.</span><span class="sxs-lookup"><span data-stu-id="27533-250">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="27533-251">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="27533-251">AzureRM.EventHub</span></span>
* <span data-ttu-id="27533-252">Для командлетов вывода списка операций Get-AzureRmEventHub и Get-AzureRmEventHubConsumerGroup добавлен необязательный параметр MaxCount.</span><span class="sxs-lookup"><span data-stu-id="27533-252">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="27533-253">Исправлена проблема с командлетом New-AzureRmEventHub, из-за которой требовалось указать по крайней мере один параметр при создании концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="27533-253">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="27533-254">Добавлен набор параметров по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="27533-254">Provided Default Parameter set.</span></span>
* <span data-ttu-id="27533-255">Для командлета New-AzureRmEventHubKey добавлен необязательный параметр -KeyValue, который позволяет пользователю предоставить значение ключа.</span><span class="sxs-lookup"><span data-stu-id="27533-255">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="27533-256">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="27533-256">AzureRM.KeyVault</span></span>
* <span data-ttu-id="27533-257">Исправлена ошибка, из-за которой при выполнении командлета Get-AzureRmKeyVault с параметром -Tag возвращались все ресурсы.</span><span class="sxs-lookup"><span data-stu-id="27533-257">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="27533-258">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="27533-258">AzureRM.Network</span></span>
* <span data-ttu-id="27533-259">Для параметра шлюзов виртуальной вести, избыточных в пределах зоны, предоставлены новые номера SKU.</span><span class="sxs-lookup"><span data-stu-id="27533-259">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="27533-260">Добавлены новые команды для функции поддержки партнерских API для ExpressRoute, развертываемых с помощью ARM:</span><span class="sxs-lookup"><span data-stu-id="27533-260">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="27533-261">добавлена команда Get-AzureRmExpressRouteCrossConnection;</span><span class="sxs-lookup"><span data-stu-id="27533-261">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="27533-262">добавлена команда Set-AzureRmExpressRouteCrossConnection;</span><span class="sxs-lookup"><span data-stu-id="27533-262">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="27533-263">добавлена команда Add-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="27533-263">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="27533-264">добавлена команда Get-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="27533-264">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="27533-265">добавлена команда Remove-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="27533-265">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="27533-266">добавлена команда Get-AzureRMExpressRouteCrossConnectionArpTable;</span><span class="sxs-lookup"><span data-stu-id="27533-266">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="27533-267">добавлена команда Get-AzureRMExpressRouteCrossConnectionRouteTable;</span><span class="sxs-lookup"><span data-stu-id="27533-267">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="27533-268">добавлена команда Get-AzureRMExpressRouteCrossConnectionRouteTableSummary.</span><span class="sxs-lookup"><span data-stu-id="27533-268">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="27533-269">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="27533-269">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="27533-270">Добавлен командлет Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="27533-270">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="27533-271">Этот командлет принимает идентификатор виртуальной машины и проверяет, защищена ли виртуальная машина с помощью какого-либо хранилища в подписке.</span><span class="sxs-lookup"><span data-stu-id="27533-271">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="27533-272">Если такое хранилище существует, командлет выводит данные о нем.</span><span class="sxs-lookup"><span data-stu-id="27533-272">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="27533-273">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="27533-273">AzureRM.Resources</span></span>
* <span data-ttu-id="27533-274">Обновлены командлеты Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="27533-274">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="27533-275">Добавлена поддержка вывода списка значений параметра -Scope на уровне группы управления.</span><span class="sxs-lookup"><span data-stu-id="27533-275">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="27533-276">Добавлена поддержка для получения отдельных назначений со значениями -Scope на уровне группы управления.</span><span class="sxs-lookup"><span data-stu-id="27533-276">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="27533-277">Для параметра управления добавлены параметры -Effective и -All.</span><span class="sxs-lookup"><span data-stu-id="27533-277">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="27533-278">Обновлены командлеты Get/New/Remove/Set-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="27533-278">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="27533-279">Добавлен параметр -ManagementGroupName для применения операций к заданной группе управления.</span><span class="sxs-lookup"><span data-stu-id="27533-279">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="27533-280">Добавлен параметр -SubscriptionId для применения операций к заданной подписке.</span><span class="sxs-lookup"><span data-stu-id="27533-280">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="27533-281">Обновлены командлеты Get/New/Remove/Set-AzureRmPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="27533-281">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="27533-282">Добавлен параметр -ManagementGroupName для применения операций к заданной группе управления.</span><span class="sxs-lookup"><span data-stu-id="27533-282">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="27533-283">Добавлен параметр -SubscriptionId для применения операций к заданной подписке.</span><span class="sxs-lookup"><span data-stu-id="27533-283">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="27533-284">Добавлена поддержка ссылок на секрет KeyVault в параметрах при использовании TemplateParameterObject в New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="27533-284">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="27533-285">Устранена проблема, из-за которой параметр -EndDate игнорировался в New-AzureRmADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="27533-285">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="27533-286">Устранена проблема, из-за которой в Add-AzureRmADGroupMember использовался неверный URL-адрес для запроса.</span><span class="sxs-lookup"><span data-stu-id="27533-286">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="27533-287">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="27533-287">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="27533-288">Для командлета New-AzureRmServiceBusKey добавлен необязательный параметр -KeyValue, который позволяет пользователю предоставить значение ключа.</span><span class="sxs-lookup"><span data-stu-id="27533-288">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="27533-289">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="27533-289">AzureRM.Sql</span></span>
* <span data-ttu-id="27533-290">В справке по New-AzureRmSqlDatabaseRestorePoint добавлено описание определяемых пользователем точек восстановления для хранилища данных SQL.</span><span class="sxs-lookup"><span data-stu-id="27533-290">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="27533-291">Обновлена документация по параметру -ComputeGeneration, используемого в нескольких командлетах.</span><span class="sxs-lookup"><span data-stu-id="27533-291">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="27533-292">6.3.0 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="27533-292">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="27533-293">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="27533-293">AzureRM.Profile</span></span>
* <span data-ttu-id="27533-294">Обновлены сообщения об ошибках для Enable-AzureRmContextAutoSave.</span><span class="sxs-lookup"><span data-stu-id="27533-294">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="27533-295">Создание контекста для каждой подписки при выполнении Connect-AzureRmAccount без предыдущего контекста.</span><span class="sxs-lookup"><span data-stu-id="27533-295">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="27533-296">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="27533-296">Azure.Storage</span></span>
* <span data-ttu-id="27533-297">В файлы справки добавлены дополнительные сведения о параметре -Permissions.</span><span class="sxs-lookup"><span data-stu-id="27533-297">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="27533-298">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="27533-298">AzureRM.Compute</span></span>
* <span data-ttu-id="27533-299">Get-AzureRmVmDiskEncryptionStatus устраняет проблему, которая наблюдалась на виртуальных машинах без дисков данных.</span><span class="sxs-lookup"><span data-stu-id="27533-299">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="27533-300">Обновлена версия клиентской библиотеки Compute для исправления следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="27533-300">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="27533-301">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="27533-301">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="27533-302">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="27533-302">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="27533-303">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="27533-303">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="27533-304">В следующих командлетах исправлено отображение неправильных значений operation ID и operation status:</span><span class="sxs-lookup"><span data-stu-id="27533-304">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="27533-305">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="27533-305">Start-AzureRmVM</span></span>
    - <span data-ttu-id="27533-306">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="27533-306">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="27533-307">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="27533-307">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="27533-308">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="27533-308">Set-AzureRmVM</span></span>
    - <span data-ttu-id="27533-309">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="27533-309">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="27533-310">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="27533-310">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="27533-311">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="27533-311">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="27533-312">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="27533-312">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="27533-313">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="27533-313">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="27533-314">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="27533-314">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="27533-315">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="27533-315">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="27533-316">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="27533-316">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="27533-317">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="27533-317">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="27533-318">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="27533-318">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="27533-319">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="27533-319">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="27533-320">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="27533-320">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="27533-321">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="27533-321">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="27533-322">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="27533-322">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="27533-323">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="27533-323">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="27533-324">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="27533-324">AzureRM.EventGrid</span></span>
* <span data-ttu-id="27533-325">Удалены условия проверки ValidateNotNullOrEmpty для SubjectBeginsWith/SubjectEndsWith в командлете Update-AzureRmEventGridSubscription, что позволяет при необходимости заменять эти параметры пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="27533-325">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="27533-326">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="27533-326">AzureRM.KeyVault</span></span>
* <span data-ttu-id="27533-327">Исправлена ошибка, когда при выполнении командлета Get-AzureRmKeyVault -Tag не возвращается ни один тег.</span><span class="sxs-lookup"><span data-stu-id="27533-327">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="27533-328">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="27533-328">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="27533-329">Общедоступный выпуск командлетов Policy Insights.</span><span class="sxs-lookup"><span data-stu-id="27533-329">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="27533-330">Используется API версии 2018-04-04.</span><span class="sxs-lookup"><span data-stu-id="27533-330">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="27533-331">К результатам Get-AzureRmPolicyStateSummary добавлено PolicyDefinitionReferenceId.</span><span class="sxs-lookup"><span data-stu-id="27533-331">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="27533-332">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="27533-332">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="27533-333">Для командлетов RecoveryServices.Backup добавлен параметр -Vault.</span><span class="sxs-lookup"><span data-stu-id="27533-333">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="27533-334">Передача этого параметра переопределяет командлет Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="27533-334">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="27533-335">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="27533-335">AzureRM.Sql</span></span>
* <span data-ttu-id="27533-336">В файле справки обновлен пример для командлета Get-AzureRmSqlDatabaseExpanded.</span><span class="sxs-lookup"><span data-stu-id="27533-336">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="27533-337">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="27533-337">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="27533-338">Обновлен файл справки для командлета Add-AzureRmTrafficManagerEndpointConfig.</span><span class="sxs-lookup"><span data-stu-id="27533-338">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="27533-339">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="27533-339">AzureRM.Websites</span></span>
* <span data-ttu-id="27533-340">Изменено действие командлета Set-AzureRmWebApp. Теперь он не перезаписывает AppSettings, если используется параметр -AssignIdentity.</span><span class="sxs-lookup"><span data-stu-id="27533-340">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="27533-341">Командлет New-AzureRmWebAppSlot теперь учитывает дополнительный параметр AppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="27533-341">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="27533-342">6.2.1 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="27533-342">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="27533-343">AzureRM.OperationalInsights;</span><span class="sxs-lookup"><span data-stu-id="27533-343">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="27533-344">В обновленной модели PSWorkspace Network может использовать type в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="27533-344">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="27533-345">6.2.0 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="27533-345">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="27533-346">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="27533-346">AzureRM.Profile</span></span>
* <span data-ttu-id="27533-347">Исправлена ошибка с загрузкой Newtonsoft.Json версии 10.0.3 во время импорта модуля.</span><span class="sxs-lookup"><span data-stu-id="27533-347">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="27533-348">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="27533-348">AzureRM.Compute</span></span>
* <span data-ttu-id="27533-349">Функция обновления виртуальных машин VMSS.</span><span class="sxs-lookup"><span data-stu-id="27533-349">VMSS VM Update feature</span></span>
    - <span data-ttu-id="27533-350">Добавлены командлеты Update-AzureRmVmssVM и New-AzureRmVMDataDisk.</span><span class="sxs-lookup"><span data-stu-id="27533-350">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="27533-351">В командлет Add-AzureRmVMDataDisk добавлен параметр VirtualMachineScaleSetVM, который позволяет добавлять диски данных в виртуальные машины VMSS.</span><span class="sxs-lookup"><span data-stu-id="27533-351">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="27533-352">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="27533-352">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="27533-353">Пакет SDK для ADF .NET обновлен до версии 0.8.0-preview. Новая версия содержит такие изменения:</span><span class="sxs-lookup"><span data-stu-id="27533-353">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="27533-354">добавлена операция для настройки репозитория фабрики;</span><span class="sxs-lookup"><span data-stu-id="27533-354">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="27533-355">связанная служба QuickBooks LinkedService теперь предоставляет свойства consumerKey и consumerSecret;</span><span class="sxs-lookup"><span data-stu-id="27533-355">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="27533-356">тип нескольких моделей изменен с SecretBase на Object;</span><span class="sxs-lookup"><span data-stu-id="27533-356">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="27533-357">добавлен триггер событий BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="27533-357">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="27533-358">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="27533-358">AzureRM.KeyVault</span></span>
* <span data-ttu-id="27533-359">В документацию добавлены примеры выходных данных.</span><span class="sxs-lookup"><span data-stu-id="27533-359">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="27533-360">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="27533-360">AzureRM.Network</span></span>
* <span data-ttu-id="27533-361">В командлеты Наблюдателя за сетями добавлены параметры Аналитики трафика.</span><span class="sxs-lookup"><span data-stu-id="27533-361">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="27533-362">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="27533-362">AzureRM.Resources</span></span>
* <span data-ttu-id="27533-363">Исправлена ошибка, когда командлет Get-AzureRmResource возвращает свойство Properties объектов PSResource.</span><span class="sxs-lookup"><span data-stu-id="27533-363">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="27533-364">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="27533-364">AzureRM.Scheduler</span></span>
* <span data-ttu-id="27533-365">Исправлена ошибка, когда обновление ServiceBusQueueJob не задает новые значения для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="27533-365">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="27533-366">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="27533-366">AzureRM.Sql</span></span>
* <span data-ttu-id="27533-367">В перечисленные ниже командлеты добавлен необязательный параметр LicenseType.</span><span class="sxs-lookup"><span data-stu-id="27533-367">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="27533-368">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="27533-368">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="27533-369">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool;</span><span class="sxs-lookup"><span data-stu-id="27533-369">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="27533-370">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="27533-370">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="27533-371">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="27533-371">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="27533-372">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="27533-372">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="27533-373">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="27533-373">AzureRM.Websites</span></span>
* <span data-ttu-id="27533-374">Командлет New-AzureRMWebApp теперь использует общие алгоритмы из библиотеки Strategy.</span><span class="sxs-lookup"><span data-stu-id="27533-374">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="27533-375">6.1.0 — май 2018 г.</span><span class="sxs-lookup"><span data-stu-id="27533-375">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="27533-376">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="27533-376">AzureRM.Profile</span></span>
* <span data-ttu-id="27533-377">Устранена проблема с выполнением Clear-AzureRmContext, при которой сохранялся пустой контекст с именем предыдущего контекста по умолчанию, что не позволяло пользователю создать новый контекст со старым именем.</span><span class="sxs-lookup"><span data-stu-id="27533-377">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="27533-378">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="27533-378">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="27533-379">Включены операции связывания и отмены связи в автономной системе.</span><span class="sxs-lookup"><span data-stu-id="27533-379">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="27533-380">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="27533-380">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="27533-381">Добавлена поддержка ApiVersions, ApiReleases и ApiRevisions.</span><span class="sxs-lookup"><span data-stu-id="27533-381">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="27533-382">Добавлена поддержка серверной части ServiceFabric.</span><span class="sxs-lookup"><span data-stu-id="27533-382">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="27533-383">Добавлена поддержка средства ведения журнала Application Insights.</span><span class="sxs-lookup"><span data-stu-id="27533-383">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="27533-384">Добавлена поддержка для распознавания номера SKU уровня "Базовый" как допустимого номера SKU службы управления API.</span><span class="sxs-lookup"><span data-stu-id="27533-384">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="27533-385">Добавлена поддержка установки сертификатов, выданных частным центром сертификации в качестве корневого или обычного ЦС.</span><span class="sxs-lookup"><span data-stu-id="27533-385">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="27533-386">Добавлена поддержка для приема пользовательских SSL-сертификатов с помощью KeyVault и нескольких имен узлов прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="27533-386">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="27533-387">Добавлена поддержка для удостоверения MSI.</span><span class="sxs-lookup"><span data-stu-id="27533-387">Added support for MSI identity</span></span>
* <span data-ttu-id="27533-388">Добавлена поддержка для принятия политик с помощью URL-адреса. Примечание. Указанные ниже командлеты в следующей версии будут отмечены как нерекомендуемые.</span><span class="sxs-lookup"><span data-stu-id="27533-388">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="27533-389">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="27533-389">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="27533-390">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="27533-390">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="27533-391">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="27533-391">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="27533-392">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="27533-392">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="27533-393">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="27533-393">AzureRM.Batch</span></span>
* <span data-ttu-id="27533-394">Выпущен новый командлет Get-AzureBatchPoolNodeCounts.</span><span class="sxs-lookup"><span data-stu-id="27533-394">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="27533-395">Выпущен новый командлет Start-AzureBatchComputeNodeServiceLogUpload.</span><span class="sxs-lookup"><span data-stu-id="27533-395">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="27533-396">AzureRM.Consumption:</span><span class="sxs-lookup"><span data-stu-id="27533-396">AzureRM.Consumption</span></span>
* <span data-ttu-id="27533-397">Добавлены новые параметры Expand, ResourceGroup, InstanceName, InstanceId, Tags и командлет высшего уровня Get-AzureRmConsumptionUsageDetail.</span><span class="sxs-lookup"><span data-stu-id="27533-397">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="27533-398">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27533-398">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="27533-399">Исправлен пример для Export-AzureRmDataLakeStoreChildItemProperties.</span><span class="sxs-lookup"><span data-stu-id="27533-399">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="27533-400">Исправлено исключение параметра NULL при использовании рекурсии в Set-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="27533-400">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="27533-401">Исправлены файлы справки для Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl и Remove-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="27533-401">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="27533-402">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="27533-402">AzureRM.Network</span></span>
* <span data-ttu-id="27533-403">Пакет SDK для сети обновлен с предварительной версии 18.0.0 до предварительной версии 19.0.0.</span><span class="sxs-lookup"><span data-stu-id="27533-403">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="27533-404">Добавлен командлет для создания конфигурации протокола.</span><span class="sxs-lookup"><span data-stu-id="27533-404">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="27533-405">New-AzureRmNetworkWatcherProtocolConfiguration.</span><span class="sxs-lookup"><span data-stu-id="27533-405">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="27533-406">Добавлен командлет для добавления нового подключения канала к существующему каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="27533-406">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="27533-407">Add-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="27533-407">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="27533-408">Добавлен командлет для удаления подключения канала к существующему каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="27533-408">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="27533-409">Remove-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="27533-409">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="27533-410">Добавлен командлет для получения подключения канала.</span><span class="sxs-lookup"><span data-stu-id="27533-410">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="27533-411">Get-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="27533-411">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="27533-412">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="27533-412">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="27533-413">Исправлена процедура аутентификации сервера с использованием созданных сертификатов (проблема № 5998).</span><span class="sxs-lookup"><span data-stu-id="27533-413">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="27533-414">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="27533-414">AzureRM.Sql</span></span>
* <span data-ttu-id="27533-415">Обновлены командлеты аудита, которые теперь позволяют удалять AuditActions или AuditActionGroups.</span><span class="sxs-lookup"><span data-stu-id="27533-415">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="27533-416">Исправлена проблема с Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy, при которой установка новой гибкой политики хранения завершалась ошибкой с сообщением "Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span><span class="sxs-lookup"><span data-stu-id="27533-416">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="27533-417">Please submit request with the new flexible retention policy" (Настройка политики долгосрочного хранения с помощью хранилища и политики служб восстановления Azure больше не поддерживается. Отправьте запрос с использованием новой гибкой политики хранения).</span><span class="sxs-lookup"><span data-stu-id="27533-417">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="27533-418">Обновлены все командлеты, связанные со службой "База данных SQL Azure", с созданием эластичных пулов и обновлением. Теперь используются новые API баз данных с поддержкой свойства номеров SKU для обеспечения масштабируемости и связанных с уровнями возможностей.</span><span class="sxs-lookup"><span data-stu-id="27533-418">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="27533-419">Обновлены командлеты, в том числе:</span><span class="sxs-lookup"><span data-stu-id="27533-419">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="27533-420">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="27533-420">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="27533-421">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool;</span><span class="sxs-lookup"><span data-stu-id="27533-421">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="27533-422">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="27533-422">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="27533-423">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="27533-423">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="27533-424">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="27533-424">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="27533-425">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="27533-425">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="27533-426">Обновлены параметры для Get-AzureRmTrafficManagerProfile. Теперь при использовании параметра -Name требуется параметр -ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="27533-426">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
