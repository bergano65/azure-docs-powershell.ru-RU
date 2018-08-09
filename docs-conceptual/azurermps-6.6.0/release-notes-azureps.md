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
ms.openlocfilehash: 3961f5c37869d0dc877b85bad535f399181040db
ms.sourcegitcommit: afae9f2f091b21ed07d5aec1c249cf859a8b89a4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/09/2018
ms.locfileid: "39653497"
---
# <a name="release-notes"></a><span data-ttu-id="e0d5e-103">Заметки о выпуске</span><span class="sxs-lookup"><span data-stu-id="e0d5e-103">Release notes</span></span>

<span data-ttu-id="e0d5e-104">Здесь приведен список изменений, внесенных в Azure PowerShell в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="660---july-2018"></a><span data-ttu-id="e0d5e-105">6.6.0 — июль 2018 г.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-105">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="e0d5e-106">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="e0d5e-106">General</span></span>
* <span data-ttu-id="e0d5e-107">Обновлены все файлы справки: включены полные типы параметров и исправлены типы входных и выходных данных.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-107">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="e0d5e-108">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="e0d5e-108">AzureRM.Profile</span></span>
* <span data-ttu-id="e0d5e-109">Обновлена библиотека Common.Strategy: теперь можно проверить, совместима ли текущая конфигурация ресурса с целевым ресурсом.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-109">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span> <span data-ttu-id="e0d5e-110">По умолчанию всегда используется значение true.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-110">Default is always true, individual resources and overridet the default.</span></span>
* <span data-ttu-id="e0d5e-111">В Common.Storage добавлены типы ps1xml.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-111">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="e0d5e-112">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="e0d5e-112">Azure.Storage</span></span>
* <span data-ttu-id="e0d5e-113">Служба поддержки теперь может получать контекст хранилища из DefaulfProfile.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-113">Support get Storage Context from DefaulfProfile</span></span>
* <span data-ttu-id="e0d5e-114">В свойства типов выходных данных командлетов добавлен атрибут Ps1XmlAttribute.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-114">Add Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="e0d5e-115">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e0d5e-115">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="e0d5e-116">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6370.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-116">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="e0d5e-117">В AutoMapper исправлена ошибка, препятствовавшая преобразованию PsApiManagementApi в ApiContract.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-117">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="e0d5e-118">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6515.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-118">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="e0d5e-119">В File.Save исправлена ошибка, связанная с перегрузкой типом кодировки.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-119">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="e0d5e-120">Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6560.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-120">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="e0d5e-121">Выполнено обновление до версии NuGet 4.0.3, что позволило исправить исключение шаблона в apiId.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-121">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="e0d5e-122">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="e0d5e-122">AzureRM.Compute</span></span>
* <span data-ttu-id="e0d5e-123">Устранена ошибка при создании виртуальной машины с помощью командлета New-AzureRmVm и параметра DiskFileParameterSet, которая возникала из-за переименования типа учетной записи хранения PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-123">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="e0d5e-124">Исправлен командлет Invoke-AzureRmVMRunCommand.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-124">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="e0d5e-125">Командлет Get-AzureRmAvailabilitySet теперь может выводить список всех групп доступности в подписке.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-125">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="e0d5e-126">(Параметр ResouceGroupName теперь является необязательным.)</span><span class="sxs-lookup"><span data-stu-id="e0d5e-126">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="e0d5e-127">Обновлен параметр SimpleParameterSet командлета New-AzureRmVm, что позволило использовать ускоренную сеть на соответствующих виртуальных машинах.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-127">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="e0d5e-128">Обновлен простой набор параметров New-AzureRmVmss, что позволило отменять создание масштабируемого набора виртуальных машин, если указанная пользователем подсистема балансировки нагрузки уже существует.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-128">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="e0d5e-129">Обновлен пример для New-AzureRmDisk.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-129">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="e0d5e-130">Добавлен пример для New-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-130">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="e0d5e-131">Обновлено описание командлета Set-AzureRmVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-131">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="e0d5e-132">Обновлен пример 1 для Set-AzureRmVMBginfoExtension: исправлены орфографические ошибки и префикс.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-132">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="e0d5e-133">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e0d5e-133">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="e0d5e-134">Пакет .NET SDK для ADF обновлен до версии 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-134">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="e0d5e-135">Добавлена поддержка совместного использования локальной среды IR несколькими фабриками данных.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-135">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="e0d5e-136">Добавлен новый параметр -SharedIntegrationRuntimeResourceId для командлета Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-136">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="e0d5e-137">Добавлен новый необязательный параметр -LinkedDataFactoryName для командлета Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-137">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="e0d5e-138">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e0d5e-138">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="e0d5e-139">Пакет SDK для плоскости данных (Microsoft.Azure.DataLake.Store) обновлен до версии 1.1.9.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-139">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="e0d5e-140">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="e0d5e-140">AzureRM.EventHub</span></span>
* <span data-ttu-id="e0d5e-141">Обновлена конвейерная передача для InputObject и ResourceId в командлетах remove.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-141">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="e0d5e-142">AzureRM.Insights;</span><span class="sxs-lookup"><span data-stu-id="e0d5e-142">AzureRM.Insights</span></span>
* <span data-ttu-id="e0d5e-143">Исправлено форматирование OutputType в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-143">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="e0d5e-144">Применен пакет SDK Microsoft.Azure.Management.Monitor 0.19.1-preview.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-144">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="e0d5e-145">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e0d5e-145">AzureRM.KeyVault</span></span>
* <span data-ttu-id="e0d5e-146">Исправлена проблема с конвейерной передачей в командлете Set-AzureRmKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-146">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="e0d5e-147">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="e0d5e-147">AzureRM.Network</span></span>
* <span data-ttu-id="e0d5e-148">Добавлены примеры для командлетов LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-148">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="e0d5e-149">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="e0d5e-149">AzureRM.Resources</span></span>
* <span data-ttu-id="e0d5e-150">Устранена проблема, возникавшая при указании имени и значения тега для Get-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-150">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="e0d5e-151">Исправлен сценарий конвейерной передачи в Set-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-151">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="e0d5e-152">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e0d5e-152">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="e0d5e-153">Обновлена конвейерная передача для InputObject и ResourceId в командлетах remove.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-153">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="e0d5e-154">Исправлено несколько ошибок.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-154">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="e0d5e-155">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="e0d5e-155">AzureRM.Sql</span></span>
* <span data-ttu-id="e0d5e-156">Добавлена поддержка Advanced Threat Protection для сервера с помощью следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="e0d5e-156">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="e0d5e-157">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-157">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="e0d5e-158">Добавлена поддержка оценки уязвимостей с помощью следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="e0d5e-158">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="e0d5e-159">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings;</span><span class="sxs-lookup"><span data-stu-id="e0d5e-159">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="e0d5e-160">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline;</span><span class="sxs-lookup"><span data-stu-id="e0d5e-160">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="e0d5e-161">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-161">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="e0d5e-162">Исправлен пример для Remove-AzureRmSqlServerFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-162">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="e0d5e-163">Исправлена неправильная обработка даты и времени для базового языка и региональных параметров, отличных от США, в Get-AzureSqlSyncGroupLog.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-163">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="e0d5e-164">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="e0d5e-164">AzureRM.Storage</span></span>
* <span data-ttu-id="e0d5e-165">В свойства типов выходных данных командлетов добавлен атрибут Ps1XmlAttribute.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-165">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="e0d5e-166">Выходные данные командлетов StorageAccount теперь отображаются в виде таблицы.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-166">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="e0d5e-167">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e0d5e-167">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="e0d5e-168">New-AzureRmStorageAccount;</span><span class="sxs-lookup"><span data-stu-id="e0d5e-168">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="e0d5e-169">Set-AzureRmStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-169">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="e0d5e-170">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="e0d5e-170">AzureRM.Tags</span></span>
* <span data-ttu-id="e0d5e-171">Удалено неверное утверждение из справки по командлетам Tag.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-171">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="e0d5e-172">6.5.0 — июль 2018 г.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-172">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="e0d5e-173">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="e0d5e-173">AzureRM.Profile</span></span>
* <span data-ttu-id="e0d5e-174">Обновлена справка для командлета Get-AzureRmContextAutosaveSetting.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-174">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="e0d5e-175">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="e0d5e-175">Azure.Storage</span></span>
* <span data-ttu-id="e0d5e-176">Добавлена поддержка отправки BLOB-объекта или файла с помощью токена SAS, доступного только для записи.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-176">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="e0d5e-177">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e0d5e-177">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="e0d5e-178">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e0d5e-178">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="e0d5e-179">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e0d5e-179">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="e0d5e-180">Для AS добавлено обязательное свойство ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-180">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="e0d5e-181">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="e0d5e-181">AzureRM.Automation</span></span>
* <span data-ttu-id="e0d5e-182">Обновлена справка и добавлены примеры для командлета New-AzureRMAutomationSchedule.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-182">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="e0d5e-183">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="e0d5e-183">AzureRM.Compute</span></span>
* <span data-ttu-id="e0d5e-184">Добавлен параметр -Tag для командлета Update/New-AzureRmAvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-184">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="e0d5e-185">Добавлен пример для командлета Add-AzureRmVmssExtension.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-185">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="e0d5e-186">Добавлены примеры для командлета Remove-AzureRmVmssExtension.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-186">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="e0d5e-187">Обновлена справка для командлета Set-AzureRmVMAccessExtension.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-187">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="e0d5e-188">Изменен класс SimpleParameterSet для командлета New-AzureRmVmss: теперь для SinglePlacementGroup по умолчанию задается значение false, а также добавляется параметр-переключатель SinglePlacementGroup, который позволяет пользователю создать VMSS в одной группе размещения.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-188">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="e0d5e-189">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="e0d5e-189">AzureRM.EventHub</span></span>
* <span data-ttu-id="e0d5e-190">В класс PSEventHubDRConfigurationAttributes добавлено доступное только для чтения свойство PendingReplicationOperationsCount, которое показывает количество ожидающих репликации операций во время реплицирования.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-190">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="e0d5e-191">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e0d5e-191">AzureRM.KeyVault</span></span>
* <span data-ttu-id="e0d5e-192">Обновлено сообщение об ошибке для командлета Set-AzureRmKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-192">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="e0d5e-193">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e0d5e-193">AzureRM.LogicApp</span></span>
* <span data-ttu-id="e0d5e-194">Исправлена ошибка "parameter set could not be resolved" (не удалось разрешить заданный параметр) в командлете New-AzureRmLogicApp.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-194">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="e0d5e-195">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="e0d5e-195">AzureRM.Network</span></span>
* <span data-ttu-id="e0d5e-196">Включен пиринг между виртуальными сетями в нескольких клиентах для командлета Set/Add-AzureRmVirtualNetworkPeering.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-196">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="e0d5e-197">Для шлюза приложений обновлены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="e0d5e-197">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="e0d5e-198">New-AzureRmApplicationGateway: добавлены флаг EnableFIPS и поддержка зон.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-198">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="e0d5e-199">New-AzureRmApplicationGatewaySku: добавлены новые номера SKU Standard_v2 и WAF_v2.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-199">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="e0d5e-200">Set-AzureRmApplicationGatewaySku: добавлены новые номера SKU Standard_v2 и WAF_v2.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-200">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="e0d5e-201">Командлеты RouteTable пересозданы в последней версии генератора.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-201">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="e0d5e-202">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="e0d5e-202">AzureRM.Relay</span></span>
* <span data-ttu-id="e0d5e-203">Обновлены файлы Markdown, исправлена проблема с именем параметра в примере.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-203">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="e0d5e-204">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="e0d5e-204">AzureRM.Resources</span></span>
* <span data-ttu-id="e0d5e-205">Обновлены командлеты Roleassignment и roledefinition:</span><span class="sxs-lookup"><span data-stu-id="e0d5e-205">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="e0d5e-206">Удалены лишние вызовы roledefinition, выполняемые в ходе разбиения на страницы.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-206">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="e0d5e-207">Исправлен командлет Get-AzureRmRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-207">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="e0d5e-208">Исправлена работа параметра -ExpandPrincipalGroups.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-208">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="e0d5e-209">Устранена проблема в командлете Get-AzureRmResource, заключающая в том, что в параметре -ResourceType учитывался регистр символов.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-209">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="e0d5e-210">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e0d5e-210">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="e0d5e-211">Добавлены параметры top и skip для командлетов list.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-211">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="e0d5e-212">Добавлены командлеты для перехода с пространства имен ценовой категории "Стандартный" на пространство ценовой категории "Премиум":</span><span class="sxs-lookup"><span data-stu-id="e0d5e-212">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="e0d5e-213">Start-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="e0d5e-213">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="e0d5e-214">Get-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="e0d5e-214">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="e0d5e-215">Complete-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="e0d5e-215">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="e0d5e-216">Stop-AzureRmServiceBusMigration;</span><span class="sxs-lookup"><span data-stu-id="e0d5e-216">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="e0d5e-217">Remove-AzureRmServiceBusMigration.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-217">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="e0d5e-218">В класс PSServiceBusDRConfigurationAttributes добавлено доступное только для чтения свойство PendingReplicationOperationsCount, которое показывает количество ожидающих репликации операций во время реплицирования.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-218">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="e0d5e-219">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e0d5e-219">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="e0d5e-220">Обновлен пример для командлета New-AzureRmServiceFabricCluster.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-220">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="e0d5e-221">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="e0d5e-221">AzureRM.Sql</span></span>
* <span data-ttu-id="e0d5e-222">Добавлены новые командлеты для Management.Sql, позволяющие клиентам добавлять сертификат TDE в экземпляр SQL Server или управляемый экземпляр:</span><span class="sxs-lookup"><span data-stu-id="e0d5e-222">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="e0d5e-223">Add-AzureRmSqlServerTransparentDataEncryptionCertificate;</span><span class="sxs-lookup"><span data-stu-id="e0d5e-223">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="e0d5e-224">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-224">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="e0d5e-225">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="e0d5e-225">AzureRM.Websites</span></span>
* <span data-ttu-id="e0d5e-226">`Set-AzureRmWebApp -AssignIdentity` и `Set-AzureRmWebAppSlot -AssignIdentity` при установленном значении false теперь будут удалять свойство Identity из объекта сайта. Также при этом будет удаляться тег предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-226">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="e0d5e-227">Обновлен пример для `Get-AzureRmWebAppMetrics` и `Get-AzureRmAppServicePlanMetrics`.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-227">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="e0d5e-228">`Set-AzureRmWebApp -PhpVersion` теперь поддерживает off как допустимую версию PHP.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-228">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="e0d5e-229">6.4.0 — июль 2018 г.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-229">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="e0d5e-230">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="e0d5e-230">General</span></span>
* <span data-ttu-id="e0d5e-231">Исправлено форматирование OutputType в файлах справки для большинства модулей.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-231">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="e0d5e-232">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="e0d5e-232">AzureRM.Profile</span></span>
* <span data-ttu-id="e0d5e-233">В основные типы выходных данных добавлен атрибут Ps1Xml.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-233">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="e0d5e-234">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="e0d5e-234">AzureRM.Compute</span></span>
* <span data-ttu-id="e0d5e-235">Функция добавления тега IP-адреса для масштабируемого набора виртуальных машин (VMSS)</span><span class="sxs-lookup"><span data-stu-id="e0d5e-235">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="e0d5e-236">Добавлен командлет New-AzureRmVmssIpTagConfig.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-236">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="e0d5e-237">В New-AzureRmVmssIpConfig добавлен параметр IpTag.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-237">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="e0d5e-238">Функция автоматического отката ОС для VMSS</span><span class="sxs-lookup"><span data-stu-id="e0d5e-238">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="e0d5e-239">В New-AzureRmVmssConfig и Update-AzureRmVmss добавлены параметры DisableAutoRollback.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-239">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="e0d5e-240">Функция ведения журнала обновлений ОС для VMSS</span><span class="sxs-lookup"><span data-stu-id="e0d5e-240">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="e0d5e-241">В Get-AzureRmVmss добавлен параметр OSUpgradeHistory.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-241">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="e0d5e-242">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="e0d5e-242">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="e0d5e-243">Добавлена поддержка списков управления доступом к каталогу с использованием следующих команд:</span><span class="sxs-lookup"><span data-stu-id="e0d5e-243">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="e0d5e-244">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry;</span><span class="sxs-lookup"><span data-stu-id="e0d5e-244">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="e0d5e-245">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry;</span><span class="sxs-lookup"><span data-stu-id="e0d5e-245">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="e0d5e-246">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-246">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="e0d5e-247">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e0d5e-247">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="e0d5e-248">Добавлены поддержка отмены выполнения и отслеживание хода выполнения для Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl и Remove-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-248">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="e0d5e-249">Добавлена поддержка отмены выполнения для Export-AzureRmDataLakeStoreChildItemProperties.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-249">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="e0d5e-250">Исправлена очистка сообщений об отладке для командлетов, которые выполняют рекурсивные операции.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-250">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="e0d5e-251">Исправлено расположение тестовых данных для командлетов DataLake.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-251">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="e0d5e-252">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="e0d5e-252">AzureRM.EventHub</span></span>
* <span data-ttu-id="e0d5e-253">Для командлетов вывода списка операций Get-AzureRmEventHub и Get-AzureRmEventHubConsumerGroup добавлен необязательный параметр MaxCount.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-253">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="e0d5e-254">Исправлена проблема с командлетом New-AzureRmEventHub, из-за которой требовалось указать по крайней мере один параметр при создании концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-254">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="e0d5e-255">Добавлен набор параметров по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-255">Provided Default Parameter set.</span></span>
* <span data-ttu-id="e0d5e-256">Для командлета New-AzureRmEventHubKey добавлен необязательный параметр -KeyValue, который позволяет пользователю предоставить значение ключа.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-256">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="e0d5e-257">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e0d5e-257">AzureRM.KeyVault</span></span>
* <span data-ttu-id="e0d5e-258">Исправлена ошибка, из-за которой при выполнении командлета Get-AzureRmKeyVault с параметром -Tag возвращались все ресурсы.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-258">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="e0d5e-259">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="e0d5e-259">AzureRM.Network</span></span>
* <span data-ttu-id="e0d5e-260">Для параметра шлюзов виртуальной вести, избыточных в пределах зоны, предоставлены новые номера SKU.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-260">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="e0d5e-261">Добавлены новые команды для функции поддержки партнерских API для ExpressRoute, развертываемых с помощью ARM:</span><span class="sxs-lookup"><span data-stu-id="e0d5e-261">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="e0d5e-262">добавлена команда Get-AzureRmExpressRouteCrossConnection;</span><span class="sxs-lookup"><span data-stu-id="e0d5e-262">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="e0d5e-263">добавлена команда Set-AzureRmExpressRouteCrossConnection;</span><span class="sxs-lookup"><span data-stu-id="e0d5e-263">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="e0d5e-264">добавлена команда Add-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="e0d5e-264">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="e0d5e-265">добавлена команда Get-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="e0d5e-265">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="e0d5e-266">добавлена команда Remove-AzureRmExpressRouteCrossConnectionPeering;</span><span class="sxs-lookup"><span data-stu-id="e0d5e-266">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="e0d5e-267">добавлена команда Get-AzureRMExpressRouteCrossConnectionArpTable;</span><span class="sxs-lookup"><span data-stu-id="e0d5e-267">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="e0d5e-268">добавлена команда Get-AzureRMExpressRouteCrossConnectionRouteTable;</span><span class="sxs-lookup"><span data-stu-id="e0d5e-268">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="e0d5e-269">добавлена команда Get-AzureRMExpressRouteCrossConnectionRouteTableSummary.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-269">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="e0d5e-270">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="e0d5e-270">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="e0d5e-271">Добавлен командлет Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-271">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="e0d5e-272">Этот командлет принимает идентификатор виртуальной машины и проверяет, защищена ли виртуальная машина с помощью какого-либо хранилища в подписке.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-272">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="e0d5e-273">Если такое хранилище существует, командлет выводит данные о нем.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-273">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="e0d5e-274">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="e0d5e-274">AzureRM.Resources</span></span>
* <span data-ttu-id="e0d5e-275">Обновлены командлеты Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="e0d5e-275">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="e0d5e-276">Добавлена поддержка вывода списка значений параметра -Scope на уровне группы управления.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-276">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="e0d5e-277">Добавлена поддержка для получения отдельных назначений со значениями -Scope на уровне группы управления.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-277">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="e0d5e-278">Для параметра управления добавлены параметры -Effective и -All.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-278">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="e0d5e-279">Обновлены командлеты Get/New/Remove/Set-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-279">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="e0d5e-280">Добавлен параметр -ManagementGroupName для применения операций к заданной группе управления.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-280">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="e0d5e-281">Добавлен параметр -SubscriptionId для применения операций к заданной подписке.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-281">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="e0d5e-282">Обновлены командлеты Get/New/Remove/Set-AzureRmPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-282">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="e0d5e-283">Добавлен параметр -ManagementGroupName для применения операций к заданной группе управления.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-283">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="e0d5e-284">Добавлен параметр -SubscriptionId для применения операций к заданной подписке.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-284">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="e0d5e-285">Добавлена поддержка ссылок на секрет KeyVault в параметрах при использовании TemplateParameterObject в New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-285">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="e0d5e-286">Устранена проблема, из-за которой параметр -EndDate игнорировался в New-AzureRmADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-286">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="e0d5e-287">Устранена проблема, из-за которой в Add-AzureRmADGroupMember использовался неверный URL-адрес для запроса.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-287">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="e0d5e-288">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e0d5e-288">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="e0d5e-289">Для командлета New-AzureRmServiceBusKey добавлен необязательный параметр -KeyValue, который позволяет пользователю предоставить значение ключа.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-289">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="e0d5e-290">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="e0d5e-290">AzureRM.Sql</span></span>
* <span data-ttu-id="e0d5e-291">В справке по New-AzureRmSqlDatabaseRestorePoint добавлено описание определяемых пользователем точек восстановления для хранилища данных SQL.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-291">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="e0d5e-292">Обновлена документация по параметру -ComputeGeneration, используемого в нескольких командлетах.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-292">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="e0d5e-293">6.3.0 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-293">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="e0d5e-294">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="e0d5e-294">AzureRM.Profile</span></span>
* <span data-ttu-id="e0d5e-295">Обновлены сообщения об ошибках для Enable-AzureRmContextAutoSave.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-295">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="e0d5e-296">Создание контекста для каждой подписки при выполнении Connect-AzureRmAccount без предыдущего контекста.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-296">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="e0d5e-297">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="e0d5e-297">Azure.Storage</span></span>
* <span data-ttu-id="e0d5e-298">В файлы справки добавлены дополнительные сведения о параметре -Permissions.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-298">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="e0d5e-299">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="e0d5e-299">AzureRM.Compute</span></span>
* <span data-ttu-id="e0d5e-300">Get-AzureRmVmDiskEncryptionStatus устраняет проблему, которая наблюдалась на виртуальных машинах без дисков данных.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-300">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="e0d5e-301">Обновлена версия клиентской библиотеки Compute для исправления следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="e0d5e-301">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="e0d5e-302">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="e0d5e-302">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="e0d5e-303">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="e0d5e-303">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="e0d5e-304">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="e0d5e-304">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="e0d5e-305">В следующих командлетах исправлено отображение неправильных значений operation ID и operation status:</span><span class="sxs-lookup"><span data-stu-id="e0d5e-305">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="e0d5e-306">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e0d5e-306">Start-AzureRmVM</span></span>
    - <span data-ttu-id="e0d5e-307">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e0d5e-307">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="e0d5e-308">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e0d5e-308">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="e0d5e-309">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e0d5e-309">Set-AzureRmVM</span></span>
    - <span data-ttu-id="e0d5e-310">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="e0d5e-310">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="e0d5e-311">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e0d5e-311">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="e0d5e-312">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="e0d5e-312">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="e0d5e-313">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="e0d5e-313">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="e0d5e-314">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e0d5e-314">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="e0d5e-315">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e0d5e-315">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="e0d5e-316">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e0d5e-316">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="e0d5e-317">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e0d5e-317">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="e0d5e-318">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="e0d5e-318">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="e0d5e-319">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="e0d5e-319">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="e0d5e-320">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="e0d5e-320">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="e0d5e-321">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="e0d5e-321">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="e0d5e-322">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="e0d5e-322">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="e0d5e-323">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="e0d5e-323">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="e0d5e-324">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e0d5e-324">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="e0d5e-325">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e0d5e-325">AzureRM.EventGrid</span></span>
* <span data-ttu-id="e0d5e-326">Удалены условия проверки ValidateNotNullOrEmpty для SubjectBeginsWith/SubjectEndsWith в командлете Update-AzureRmEventGridSubscription, что позволяет при необходимости заменять эти параметры пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-326">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="e0d5e-327">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e0d5e-327">AzureRM.KeyVault</span></span>
* <span data-ttu-id="e0d5e-328">Исправлена ошибка, когда при выполнении командлета Get-AzureRmKeyVault -Tag не возвращается ни один тег.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-328">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="e0d5e-329">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e0d5e-329">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="e0d5e-330">Общедоступный выпуск командлетов Policy Insights.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-330">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="e0d5e-331">Используется API версии 2018-04-04.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-331">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="e0d5e-332">К результатам Get-AzureRmPolicyStateSummary добавлено PolicyDefinitionReferenceId.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-332">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="e0d5e-333">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="e0d5e-333">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="e0d5e-334">Для командлетов RecoveryServices.Backup добавлен параметр -Vault.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-334">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="e0d5e-335">Передача этого параметра переопределяет командлет Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-335">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="e0d5e-336">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="e0d5e-336">AzureRM.Sql</span></span>
* <span data-ttu-id="e0d5e-337">В файле справки обновлен пример для командлета Get-AzureRmSqlDatabaseExpanded.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-337">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="e0d5e-338">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="e0d5e-338">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="e0d5e-339">Обновлен файл справки для командлета Add-AzureRmTrafficManagerEndpointConfig.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-339">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="e0d5e-340">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="e0d5e-340">AzureRM.Websites</span></span>
* <span data-ttu-id="e0d5e-341">Изменено действие командлета Set-AzureRmWebApp. Теперь он не перезаписывает AppSettings, если используется параметр -AssignIdentity.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-341">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="e0d5e-342">Командлет New-AzureRmWebAppSlot теперь учитывает дополнительный параметр AppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-342">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="e0d5e-343">6.2.1 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-343">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="e0d5e-344">AzureRM.OperationalInsights;</span><span class="sxs-lookup"><span data-stu-id="e0d5e-344">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="e0d5e-345">В обновленной модели PSWorkspace Network может использовать type в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-345">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="e0d5e-346">6.2.0 — июнь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-346">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="e0d5e-347">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="e0d5e-347">AzureRM.Profile</span></span>
* <span data-ttu-id="e0d5e-348">Исправлена ошибка с загрузкой Newtonsoft.Json версии 10.0.3 во время импорта модуля.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-348">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="e0d5e-349">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="e0d5e-349">AzureRM.Compute</span></span>
* <span data-ttu-id="e0d5e-350">Функция обновления виртуальных машин VMSS.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-350">VMSS VM Update feature</span></span>
    - <span data-ttu-id="e0d5e-351">Добавлены командлеты Update-AzureRmVmssVM и New-AzureRmVMDataDisk.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-351">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="e0d5e-352">В командлет Add-AzureRmVMDataDisk добавлен параметр VirtualMachineScaleSetVM, который позволяет добавлять диски данных в виртуальные машины VMSS.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-352">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="e0d5e-353">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e0d5e-353">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="e0d5e-354">Пакет SDK для ADF .NET обновлен до версии 0.8.0-preview. Новая версия содержит такие изменения:</span><span class="sxs-lookup"><span data-stu-id="e0d5e-354">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="e0d5e-355">добавлена операция для настройки репозитория фабрики;</span><span class="sxs-lookup"><span data-stu-id="e0d5e-355">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="e0d5e-356">связанная служба QuickBooks LinkedService теперь предоставляет свойства consumerKey и consumerSecret;</span><span class="sxs-lookup"><span data-stu-id="e0d5e-356">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="e0d5e-357">тип нескольких моделей изменен с SecretBase на Object;</span><span class="sxs-lookup"><span data-stu-id="e0d5e-357">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="e0d5e-358">добавлен триггер событий BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-358">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="e0d5e-359">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e0d5e-359">AzureRM.KeyVault</span></span>
* <span data-ttu-id="e0d5e-360">В документацию добавлены примеры выходных данных.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-360">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="e0d5e-361">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="e0d5e-361">AzureRM.Network</span></span>
* <span data-ttu-id="e0d5e-362">В командлеты Наблюдателя за сетями добавлены параметры Аналитики трафика.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-362">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="e0d5e-363">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="e0d5e-363">AzureRM.Resources</span></span>
* <span data-ttu-id="e0d5e-364">Исправлена ошибка, когда командлет Get-AzureRmResource возвращает свойство Properties объектов PSResource.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-364">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="e0d5e-365">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="e0d5e-365">AzureRM.Scheduler</span></span>
* <span data-ttu-id="e0d5e-366">Исправлена ошибка, когда обновление ServiceBusQueueJob не задает новые значения для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-366">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="e0d5e-367">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="e0d5e-367">AzureRM.Sql</span></span>
* <span data-ttu-id="e0d5e-368">В перечисленные ниже командлеты добавлен необязательный параметр LicenseType.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-368">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="e0d5e-369">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="e0d5e-369">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="e0d5e-370">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool;</span><span class="sxs-lookup"><span data-stu-id="e0d5e-370">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="e0d5e-371">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="e0d5e-371">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="e0d5e-372">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="e0d5e-372">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="e0d5e-373">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e0d5e-373">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="e0d5e-374">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="e0d5e-374">AzureRM.Websites</span></span>
* <span data-ttu-id="e0d5e-375">Командлет New-AzureRMWebApp теперь использует общие алгоритмы из библиотеки Strategy.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-375">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="e0d5e-376">6.1.0 — май 2018 г.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-376">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="e0d5e-377">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="e0d5e-377">AzureRM.Profile</span></span>
* <span data-ttu-id="e0d5e-378">Устранена проблема с выполнением Clear-AzureRmContext, при которой сохранялся пустой контекст с именем предыдущего контекста по умолчанию, что не позволяло пользователю создать новый контекст со старым именем.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-378">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="e0d5e-379">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e0d5e-379">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="e0d5e-380">Включены операции связывания и отмены связи в автономной системе.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-380">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="e0d5e-381">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e0d5e-381">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="e0d5e-382">Добавлена поддержка ApiVersions, ApiReleases и ApiRevisions.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-382">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="e0d5e-383">Добавлена поддержка серверной части ServiceFabric.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-383">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="e0d5e-384">Добавлена поддержка средства ведения журнала Application Insights.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-384">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="e0d5e-385">Добавлена поддержка для распознавания номера SKU уровня "Базовый" как допустимого номера SKU службы управления API.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-385">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="e0d5e-386">Добавлена поддержка установки сертификатов, выданных частным центром сертификации в качестве корневого или обычного ЦС.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-386">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="e0d5e-387">Добавлена поддержка для приема пользовательских SSL-сертификатов с помощью KeyVault и нескольких имен узлов прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-387">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="e0d5e-388">Добавлена поддержка для удостоверения MSI.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-388">Added support for MSI identity</span></span>
* <span data-ttu-id="e0d5e-389">Добавлена поддержка для принятия политик с помощью URL-адреса. Примечание. Указанные ниже командлеты в следующей версии будут отмечены как нерекомендуемые.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-389">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="e0d5e-390">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="e0d5e-390">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="e0d5e-391">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="e0d5e-391">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="e0d5e-392">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="e0d5e-392">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="e0d5e-393">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="e0d5e-393">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="e0d5e-394">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="e0d5e-394">AzureRM.Batch</span></span>
* <span data-ttu-id="e0d5e-395">Выпущен новый командлет Get-AzureBatchPoolNodeCounts.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-395">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="e0d5e-396">Выпущен новый командлет Start-AzureBatchComputeNodeServiceLogUpload.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-396">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="e0d5e-397">AzureRM.Consumption:</span><span class="sxs-lookup"><span data-stu-id="e0d5e-397">AzureRM.Consumption</span></span>
* <span data-ttu-id="e0d5e-398">Добавлены новые параметры Expand, ResourceGroup, InstanceName, InstanceId, Tags и командлет высшего уровня Get-AzureRmConsumptionUsageDetail.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-398">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="e0d5e-399">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e0d5e-399">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="e0d5e-400">Исправлен пример для Export-AzureRmDataLakeStoreChildItemProperties.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-400">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="e0d5e-401">Исправлено исключение параметра NULL при использовании рекурсии в Set-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-401">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="e0d5e-402">Исправлены файлы справки для Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl и Remove-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-402">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="e0d5e-403">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="e0d5e-403">AzureRM.Network</span></span>
* <span data-ttu-id="e0d5e-404">Пакет SDK для сети обновлен с предварительной версии 18.0.0 до предварительной версии 19.0.0.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-404">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="e0d5e-405">Добавлен командлет для создания конфигурации протокола.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-405">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="e0d5e-406">New-AzureRmNetworkWatcherProtocolConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-406">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="e0d5e-407">Добавлен командлет для добавления нового подключения канала к существующему каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-407">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="e0d5e-408">Add-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-408">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="e0d5e-409">Добавлен командлет для удаления подключения канала к существующему каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-409">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="e0d5e-410">Remove-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-410">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="e0d5e-411">Добавлен командлет для получения подключения канала.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-411">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="e0d5e-412">Get-AzureRmExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-412">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="e0d5e-413">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e0d5e-413">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="e0d5e-414">Исправлена процедура аутентификации сервера с использованием созданных сертификатов (проблема № 5998).</span><span class="sxs-lookup"><span data-stu-id="e0d5e-414">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="e0d5e-415">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="e0d5e-415">AzureRM.Sql</span></span>
* <span data-ttu-id="e0d5e-416">Обновлены командлеты аудита, которые теперь позволяют удалять AuditActions или AuditActionGroups.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-416">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="e0d5e-417">Исправлена проблема с Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy, при которой установка новой гибкой политики хранения завершалась ошибкой с сообщением "Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-417">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="e0d5e-418">Please submit request with the new flexible retention policy" (Настройка политики долгосрочного хранения с помощью хранилища и политики служб восстановления Azure больше не поддерживается. Отправьте запрос с использованием новой гибкой политики хранения).</span><span class="sxs-lookup"><span data-stu-id="e0d5e-418">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="e0d5e-419">Обновлены все командлеты, связанные со службой "База данных SQL Azure", с созданием эластичных пулов и обновлением. Теперь используются новые API баз данных с поддержкой свойства номеров SKU для обеспечения масштабируемости и связанных с уровнями возможностей.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-419">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="e0d5e-420">Обновлены командлеты, в том числе:</span><span class="sxs-lookup"><span data-stu-id="e0d5e-420">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="e0d5e-421">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="e0d5e-421">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="e0d5e-422">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool;</span><span class="sxs-lookup"><span data-stu-id="e0d5e-422">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="e0d5e-423">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="e0d5e-423">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="e0d5e-424">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="e0d5e-424">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="e0d5e-425">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e0d5e-425">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="e0d5e-426">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="e0d5e-426">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="e0d5e-427">Обновлены параметры для Get-AzureRmTrafficManagerProfile. Теперь при использовании параметра -Name требуется параметр -ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="e0d5e-427">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>