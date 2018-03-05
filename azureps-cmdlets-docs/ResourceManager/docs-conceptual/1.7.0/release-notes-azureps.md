---
title: "Журнал изменений Azure PowerShell | Документация Майкрософт"
description: "Это руководство содержит историю изменений Azure PowerShell, внесенных в новом выпуске."
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: 
ms.date: 05/18/2017
ms.openlocfilehash: 0a3f152751fee569d3ac5fba6bcff8c1737f7b8c
ms.sourcegitcommit: 226527be7cb647acfe2ea9ab151185053ab3c6db
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/29/2017
---
# <a name="release-notes"></a><span data-ttu-id="7ce7a-103">Заметки о выпуске</span><span class="sxs-lookup"><span data-stu-id="7ce7a-103">Release notes</span></span>

<span data-ttu-id="7ce7a-104">Здесь приведен список изменений, внесенных в Azure PowerShell в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="7ce7a-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-170"></a><span data-ttu-id="7ce7a-105">Версия 1.7.0</span><span class="sxs-lookup"><span data-stu-id="7ce7a-105">Version 1.7.0</span></span>

* <span data-ttu-id="7ce7a-106">**Изменено поведение параметров -Force, -Confirm и $ConfirmPreference для всех командлетов. Мы внесли изменения в эту реализацию для соответствия рекомендациям PowerShell. Для большинства командлетов это значит удаление параметра Force, а чтобы пропустить приглашение ShouldProcess, пользователям потребуется включить параметр -Confirm:$false в скрипты PowerShell.**</span><span class="sxs-lookup"><span data-stu-id="7ce7a-106">**Behavioral change for -Force, –Confirm and $ConfirmPreference parameters for all cmdlets. We are changing this implementation to be in line with PowerShell guidelines. For most cmdlets, this means removing the Force parameter and to skip the ShouldProcess prompt, users will need to include the parameter: ‘-Confirm:$false’ in their PowerShell scripts.**</span></span> <span data-ttu-id="7ce7a-107">Эти изменения обеспечили следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="7ce7a-107">This changes are addressing following issues:</span></span>
  - <span data-ttu-id="7ce7a-108">Правильная реализация функций –WhatIf, что позволяет пользователю определить влияние командлета или скрипта без внесения фактических изменений.</span><span class="sxs-lookup"><span data-stu-id="7ce7a-108">Correct implementation of –WhatIf functionality, allowing a user to determine the effects of a cmdlet or script without making any actual changes</span></span>
  - <span data-ttu-id="7ce7a-109">Контроль над запросом с помощью параметра $ConfirmPreference для всего сеанса, чтобы пользователь запрашивался на основе влияния предполагаемого изменения (как описано в параметре ConfirmImpact командлета).</span><span class="sxs-lookup"><span data-stu-id="7ce7a-109">Control over prompting using a session-wide $ConfirmPreference, so that the user is prompted based on the impact of a prospective change (as reported in the ConfirmImpact setting in the cmdlet)</span></span>
  - <span data-ttu-id="7ce7a-110">Контроль над запросами на подтверждение команд с помощью параметра -Confirm для конкретного командлета.</span><span class="sxs-lookup"><span data-stu-id="7ce7a-110">Cmdlet-specific control over confirmation prompts using the –Confirm parameter</span></span>
  - <span data-ttu-id="7ce7a-111">Согласованное использование параметров ShouldContinue и –Force для командлетов только для действий, требующих запроса от пользователя из-за особого характера изменений (например, удаление скрытых файлов).</span><span class="sxs-lookup"><span data-stu-id="7ce7a-111">Consistent use of ShouldContinue and the –Force parameter across cmdlets, for only those actions that would require prompting from the user due to the special nature of the changes (for example, deleting hidden files)</span></span>
  - <span data-ttu-id="7ce7a-112">Согласованность с другими командлетами PowerShell, чтобы знания скриптов PowerShell из других командлетов могли быть применимы к командлетам Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7ce7a-112">Consistency with other PowerShell cmdlets, so that PowerShell scripting knowledge from other cmdlets is immediately applicable to the Azure PowerShell cmdlets.</span></span>

<span data-ttu-id="7ce7a-113">**Обратите внимание, что теперь для *автоматического пропуска всех запросов во всех случаях* для командлетов Azure PowerShell необходимо указать два параметра:**</span><span class="sxs-lookup"><span data-stu-id="7ce7a-113">**Notice that now to *automatically skip all Prompts in all Circumstances* Azure PowerShell cmdlets require the user to supply two parameters:**</span></span>
```powershell
My-CmdletWithConfirmation –Confirm:$false -Force
```
* <span data-ttu-id="7ce7a-114">Служба вычислений Azure</span><span class="sxs-lookup"><span data-stu-id="7ce7a-114">Azure Compute</span></span>
  - <span data-ttu-id="7ce7a-115">Set-AzureRmVMADDomainExtension.</span><span class="sxs-lookup"><span data-stu-id="7ce7a-115">Set-AzureRmVMADDomainExtension</span></span>
  - <span data-ttu-id="7ce7a-116">Get-AzureRmVMADDomainExtension.</span><span class="sxs-lookup"><span data-stu-id="7ce7a-116">Get-AzureRmVMADDomainExtension</span></span>
  - <span data-ttu-id="7ce7a-117">Параметр -Redeploy для Restart-AzureVM.</span><span class="sxs-lookup"><span data-stu-id="7ce7a-117">-Redeploy parameter for Restart-AzureVM</span></span>
  - <span data-ttu-id="7ce7a-118">Параметр -Validate для Move-AzureService, Move-AzureStorageAccount и Move-AzureVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="7ce7a-118">-Validate parameter for Move-AzureService, Move-AzureStorageAccount, and Move-AzureVirtualNetwork</span></span>
  - <span data-ttu-id="7ce7a-119">Как и прежде, параметры имени и версии для командлетов расширения являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="7ce7a-119">Name and version parameters for extension cmdlets are optional as before.</span></span>
  - <span data-ttu-id="7ce7a-120">Командлет New-AzureVM может узнать тип лицензии у объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7ce7a-120">New-AzureVM can get a license type from VM object.</span></span>
* <span data-ttu-id="7ce7a-121">Хранилище Azure</span><span class="sxs-lookup"><span data-stu-id="7ce7a-121">Azure Storage</span></span>
  - <span data-ttu-id="7ce7a-122">В следующих командлетах параметр Tags изменен на Tag, а для параметра Tags добавлен псевдоним:</span><span class="sxs-lookup"><span data-stu-id="7ce7a-122">Change Tags Parameter to Tag, and add parameter alias Tags</span></span>
    + <span data-ttu-id="7ce7a-123">New-AzureRmStorageAccount;</span><span class="sxs-lookup"><span data-stu-id="7ce7a-123">New-AzureRmStorageAccount</span></span>
    + <span data-ttu-id="7ce7a-124">Set-AzureRmStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="7ce7a-124">Set-AzureRmStorageAccount</span></span>
* <span data-ttu-id="7ce7a-125">Сеть Azure</span><span class="sxs-lookup"><span data-stu-id="7ce7a-125">Azure Network</span></span>
  - <span data-ttu-id="7ce7a-126">Добавлен новый командлет для пиринга между виртуальными сетями.</span><span class="sxs-lookup"><span data-stu-id="7ce7a-126">New cmdlet added for Virtual Network Peering</span></span>
* <span data-ttu-id="7ce7a-127">кэш Azure Redis</span><span class="sxs-lookup"><span data-stu-id="7ce7a-127">Azure Redis Cache</span></span>
  - <span data-ttu-id="7ce7a-128">Добавлен новый командлет для Reset-AzureRmRedisCache.</span><span class="sxs-lookup"><span data-stu-id="7ce7a-128">New cmdlet added for Reset-AzureRmRedisCache</span></span>
  - <span data-ttu-id="7ce7a-129">Добавлен новый командлет для Export-AzureRmRedisCache.</span><span class="sxs-lookup"><span data-stu-id="7ce7a-129">New cmdlet added for Export-AzureRmRedisCache</span></span>
  - <span data-ttu-id="7ce7a-130">Добавлен новый командлет для Import-AzureRmRedisCache.</span><span class="sxs-lookup"><span data-stu-id="7ce7a-130">New cmdlet added for Import-AzureRmRedisCache</span></span>
  - <span data-ttu-id="7ce7a-131">Теперь командлет New-AzureRmRedisCache включает изменение параметра для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="7ce7a-131">Modified cmdlet New-AzureRmRedisCache to include parameter change for vNet</span></span>
* <span data-ttu-id="7ce7a-132">Архивация и восстановление базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="7ce7a-132">Azure SQL DB Backup/Restore</span></span>
  - <span data-ttu-id="7ce7a-133">Командлеты для функции долгосрочного хранения резервных копий:</span><span class="sxs-lookup"><span data-stu-id="7ce7a-133">Cmdlets for LTR (Long Term Retention) backup feature</span></span>
  - <span data-ttu-id="7ce7a-134">Get-AzureRmSqlServerBackupLongTermRetentionVault;</span><span class="sxs-lookup"><span data-stu-id="7ce7a-134">Get-AzureRmSqlServerBackupLongTermRetentionVault</span></span>
  - <span data-ttu-id="7ce7a-135">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy;</span><span class="sxs-lookup"><span data-stu-id="7ce7a-135">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>
  - <span data-ttu-id="7ce7a-136">Set-AzureRmSqlServerBackupLongTermRetentionVault;</span><span class="sxs-lookup"><span data-stu-id="7ce7a-136">Set-AzureRmSqlServerBackupLongTermRetentionVault</span></span>
  - <span data-ttu-id="7ce7a-137">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="7ce7a-137">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>
  - <span data-ttu-id="7ce7a-138">Restore-AzureRmSqlDatabase теперь поддерживает восстановление до точки во времени для удаленной базы данных.</span><span class="sxs-lookup"><span data-stu-id="7ce7a-138">Restore-AzureRmSqlDatabase now supports point-in-time restore of a deleted database</span></span>
  - <span data-ttu-id="7ce7a-139">Restore-AzureRmSqlDatabase теперь поддерживает восстановление из резервной копии долгосрочного хранения.</span><span class="sxs-lookup"><span data-stu-id="7ce7a-139">Restore-AzureRmSqlDatabase now supports restoring from a Long Term Retention backup</span></span>
* <span data-ttu-id="7ce7a-140">Приложение логики Azure</span><span class="sxs-lookup"><span data-stu-id="7ce7a-140">Azure LogicApp</span></span>
  - <span data-ttu-id="7ce7a-141">Добавлены командлеты учетных записей интеграции приложения логики:</span><span class="sxs-lookup"><span data-stu-id="7ce7a-141">Added LogicApp Integration accounts cmdlets.</span></span>
  - <span data-ttu-id="7ce7a-142">Get-AzureRmIntegrationAccountAgreement;</span><span class="sxs-lookup"><span data-stu-id="7ce7a-142">Get-AzureRmIntegrationAccountAgreement</span></span>
  - <span data-ttu-id="7ce7a-143">Get-AzureRmIntegrationAccountCallbackUrl;</span><span class="sxs-lookup"><span data-stu-id="7ce7a-143">Get-AzureRmIntegrationAccountCallbackUrl</span></span>
  - <span data-ttu-id="7ce7a-144">Get-AzureRmIntegrationAccountCertificate;</span><span class="sxs-lookup"><span data-stu-id="7ce7a-144">Get-AzureRmIntegrationAccountCertificate</span></span>
  - <span data-ttu-id="7ce7a-145">Get-AzureRmIntegrationAccount;</span><span class="sxs-lookup"><span data-stu-id="7ce7a-145">Get-AzureRmIntegrationAccount</span></span>
  - <span data-ttu-id="7ce7a-146">Get-AzureRmIntegrationAccountMap;</span><span class="sxs-lookup"><span data-stu-id="7ce7a-146">Get-AzureRmIntegrationAccountMap</span></span>
  - <span data-ttu-id="7ce7a-147">Get-AzureRmIntegrationAccountPartner;</span><span class="sxs-lookup"><span data-stu-id="7ce7a-147">Get-AzureRmIntegrationAccountPartner</span></span>
  - <span data-ttu-id="7ce7a-148">Get-AzureRmIntegrationAccountSchema;</span><span class="sxs-lookup"><span data-stu-id="7ce7a-148">Get-AzureRmIntegrationAccountSchema</span></span>
  - <span data-ttu-id="7ce7a-149">New-AzureRmIntegrationAccountAgreement;</span><span class="sxs-lookup"><span data-stu-id="7ce7a-149">New-AzureRmIntegrationAccountAgreement</span></span>
  - <span data-ttu-id="7ce7a-150">New-AzureRmIntegrationAccountCertificate;</span><span class="sxs-lookup"><span data-stu-id="7ce7a-150">New-AzureRmIntegrationAccountCertificate</span></span>
  - <span data-ttu-id="7ce7a-151">New-AzureRmIntegrationAccount;</span><span class="sxs-lookup"><span data-stu-id="7ce7a-151">New-AzureRmIntegrationAccount</span></span>
  - <span data-ttu-id="7ce7a-152">New-AzureRmIntegrationAccountMap;</span><span class="sxs-lookup"><span data-stu-id="7ce7a-152">New-AzureRmIntegrationAccountMap</span></span>
  - <span data-ttu-id="7ce7a-153">New-AzureRmIntegrationAccountPartner;</span><span class="sxs-lookup"><span data-stu-id="7ce7a-153">New-AzureRmIntegrationAccountPartner</span></span>
  - <span data-ttu-id="7ce7a-154">New-AzureRmIntegrationAccountSchema;</span><span class="sxs-lookup"><span data-stu-id="7ce7a-154">New-AzureRmIntegrationAccountSchema</span></span>
  - <span data-ttu-id="7ce7a-155">Remove-AzureRmIntegrationAccountAgreement;</span><span class="sxs-lookup"><span data-stu-id="7ce7a-155">Remove-AzureRmIntegrationAccountAgreement</span></span>
  - <span data-ttu-id="7ce7a-156">Remove-AzureRmIntegrationAccountCertificate;</span><span class="sxs-lookup"><span data-stu-id="7ce7a-156">Remove-AzureRmIntegrationAccountCertificate</span></span>
  - <span data-ttu-id="7ce7a-157">Remove-AzureRmIntegrationAccount;</span><span class="sxs-lookup"><span data-stu-id="7ce7a-157">Remove-AzureRmIntegrationAccount</span></span>
  - <span data-ttu-id="7ce7a-158">Remove-AzureRmIntegrationAccountMap;</span><span class="sxs-lookup"><span data-stu-id="7ce7a-158">Remove-AzureRmIntegrationAccountMap</span></span>
  - <span data-ttu-id="7ce7a-159">Remove-AzureRmIntegrationAccountPartner;</span><span class="sxs-lookup"><span data-stu-id="7ce7a-159">Remove-AzureRmIntegrationAccountPartner</span></span>
  - <span data-ttu-id="7ce7a-160">Remove-AzureRmIntegrationAccountSchema;</span><span class="sxs-lookup"><span data-stu-id="7ce7a-160">Remove-AzureRmIntegrationAccountSchema</span></span>
  - <span data-ttu-id="7ce7a-161">Set-AzureRmIntegrationAccountAgreement;</span><span class="sxs-lookup"><span data-stu-id="7ce7a-161">Set-AzureRmIntegrationAccountAgreement</span></span>
  - <span data-ttu-id="7ce7a-162">Set-AzureRmIntegrationAccountCertificate;</span><span class="sxs-lookup"><span data-stu-id="7ce7a-162">Set-AzureRmIntegrationAccountCertificate</span></span>
  - <span data-ttu-id="7ce7a-163">Set-AzureRmIntegrationAccount;</span><span class="sxs-lookup"><span data-stu-id="7ce7a-163">Set-AzureRmIntegrationAccount</span></span>
  - <span data-ttu-id="7ce7a-164">Set-AzureRmIntegrationAccountMap;</span><span class="sxs-lookup"><span data-stu-id="7ce7a-164">Set-AzureRmIntegrationAccountMap</span></span>
  - <span data-ttu-id="7ce7a-165">Set-AzureRmIntegrationAccountPartner;</span><span class="sxs-lookup"><span data-stu-id="7ce7a-165">Set-AzureRmIntegrationAccountPartner</span></span>
  - <span data-ttu-id="7ce7a-166">Set-AzureRmIntegrationAccountSchema.</span><span class="sxs-lookup"><span data-stu-id="7ce7a-166">Set-AzureRmIntegrationAccountSchema</span></span>
* <span data-ttu-id="7ce7a-167">Хранилище озера данных Azure</span><span class="sxs-lookup"><span data-stu-id="7ce7a-167">Azure Data Lake Store</span></span>
  - <span data-ttu-id="7ce7a-168">Существенно улучшена производительность передачи и скачивания файлов и папок.</span><span class="sxs-lookup"><span data-stu-id="7ce7a-168">Drastically improve performance of file and folder upload and download.</span></span>
  - <span data-ttu-id="7ce7a-169">Внесены некоторые изменения имен параметров для скачивания и добавлены два новых параметра для передачи:</span><span class="sxs-lookup"><span data-stu-id="7ce7a-169">This includes a slight change to the parameter names for download and inclusion of two new parameters for upload:</span></span>
    + <span data-ttu-id="7ce7a-170">NumThreads -> PerFileThreadCount обозначает число потоков, используемых в одном файле;</span><span class="sxs-lookup"><span data-stu-id="7ce7a-170">NumThreads -> PerFileThreadCount, used to indicate the number of threads to use in a single file</span></span>
    + <span data-ttu-id="7ce7a-171">ConcurrentFileCount указывает количество файлов для отправки или загрузки папки в параллельном режиме.</span><span class="sxs-lookup"><span data-stu-id="7ce7a-171">ConcurrentFileCount, used to indicate the number of files to upload/download in parallel for folder upload/download.</span></span>
  - <span data-ttu-id="7ce7a-172">Значения потоков по умолчанию теперь разработаны так, чтобы обеспечить лучшую пропускную способность для большинства размеров файлов.</span><span class="sxs-lookup"><span data-stu-id="7ce7a-172">Default threading values are now designed to give a better all around throughput for most file sizes.</span></span> <span data-ttu-id="7ce7a-173">Если производительность ниже требуемой, указанные выше значения можно изменить в соответствии с требованиями.</span><span class="sxs-lookup"><span data-stu-id="7ce7a-173">If performance is not as desired, the values above can be modified to meet requirements.</span></span>
* <span data-ttu-id="7ce7a-174">Аналитика озера данных Azure</span><span class="sxs-lookup"><span data-stu-id="7ce7a-174">Azure Data Lake Analytics</span></span>
  - <span data-ttu-id="7ce7a-175">Get-AzureRMDataLakeAnalyticsDataSource теперь возвращает все источники данных, когда вызывается без аргументов.</span><span class="sxs-lookup"><span data-stu-id="7ce7a-175">Get-AzureRMDataLakeAnalyticsDataSource now returns all data sources when called with no arguments.</span></span>
  - <span data-ttu-id="7ce7a-176">Это изменение также удаляет параметр типа источника данных из командлета.</span><span class="sxs-lookup"><span data-stu-id="7ce7a-176">This change also removes the data source type parameter from the cmdlet.</span></span>
  - <span data-ttu-id="7ce7a-177">Это изменение приводит к возврату нового объекта для операции перечисления со следующими свойствами:</span><span class="sxs-lookup"><span data-stu-id="7ce7a-177">This change results in a new object being returned for the list operation with the following properties:</span></span>
    + <span data-ttu-id="7ce7a-178">Type — тип источника данных.</span><span class="sxs-lookup"><span data-stu-id="7ce7a-178">Type, the type of data source</span></span>
    + <span data-ttu-id="7ce7a-179">Name — имя источника данных.</span><span class="sxs-lookup"><span data-stu-id="7ce7a-179">Name, the name of the data source</span></span>
    + <span data-ttu-id="7ce7a-180">IsDefault — присвоено значение true, если для учетной записи это источник данных по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7ce7a-180">IsDefault, set to true if this is the default data source for the account</span></span>
  - <span data-ttu-id="7ce7a-181">Get-AzureRMDataLakeAnalyticsJob исправлен для списка определенных значений смещения времени и даты при фильтрации по submittedBefore и submittedAfter.</span><span class="sxs-lookup"><span data-stu-id="7ce7a-181">Get-AzureRMDataLakeAnalyticsJob fixed for list for certain date time offset values when filtering on submittedBefore and submittedAfter.</span></span>
* <span data-ttu-id="7ce7a-182">Веб-приложения</span><span class="sxs-lookup"><span data-stu-id="7ce7a-182">Web Apps</span></span>
  - <span data-ttu-id="7ce7a-183">Добавлен командлет Swap-AzureRmWebAppSlot для обычной замены и замены с предварительным просмотром.</span><span class="sxs-lookup"><span data-stu-id="7ce7a-183">Add Swap-AzureRmWebAppSlot cmdlet for regular swap and swap with preview</span></span>
  - <span data-ttu-id="7ce7a-184">Командлет Set-AzureRmWebAppSlot теперь поддерживает автоматический перенос.</span><span class="sxs-lookup"><span data-stu-id="7ce7a-184">Extend Set-AzureRmWebAppSlot cmdlet to support auto swap</span></span>
* <span data-ttu-id="7ce7a-185">Cлужба управления Azure API </span><span class="sxs-lookup"><span data-stu-id="7ce7a-185">Azure API Management</span></span>
  - <span data-ttu-id="7ce7a-186">Исправлены командлеты развертывания управления API Azure для облака Azure для Китая.</span><span class="sxs-lookup"><span data-stu-id="7ce7a-186">Fixed Azure Api Management Deployment cmdlets for AzureChinaCloud.</span></span>
  - <span data-ttu-id="7ce7a-187">Удален командлет Set-AzureRmApiManagementTenantGitAccess, так как доступ к Git включен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7ce7a-187">Removed cmdlet Set-AzureRmApiManagementTenantGitAccess as Git Access is enabled by Default.</span></span>
* <span data-ttu-id="7ce7a-188">Архивация с помощью служб восстановления Azure</span><span class="sxs-lookup"><span data-stu-id="7ce7a-188">Azure Recovery Services Backup</span></span>
  - <span data-ttu-id="7ce7a-189">Добавлена поддержка для рабочей нагрузки SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="7ce7a-189">Added support for the Azure SQL workload</span></span>
  - <span data-ttu-id="7ce7a-190">Добавлена поддержка для архивации и восстановления зашифрованных виртуальных машин Azure.</span><span class="sxs-lookup"><span data-stu-id="7ce7a-190">Added support for backing up and restoring encrypted Azure VMs</span></span>
  - <span data-ttu-id="7ce7a-191">Backup-AzureRmRecoveryServicesBackupItem — добавлена необязательная функция периода хранения для точек восстановления.</span><span class="sxs-lookup"><span data-stu-id="7ce7a-191">Backup-AzureRmRecoveryServicesBackupItem - Added optional retention time feature for recovery points</span></span>
  - <span data-ttu-id="7ce7a-192">Исправлены незначительные ошибки, связанные с фильтрами, в командлетах Get-AzureRmRecoveryServicesBackupContainer и Get-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="7ce7a-192">Minor filter-related bug fixes in Get-AzureRmRecoveryServicesBackupContainer and Get-AzureRmRecoveryServicesBackupItem cmdlets</span></span>
* <span data-ttu-id="7ce7a-193">Служба автоматизации Azure</span><span class="sxs-lookup"><span data-stu-id="7ce7a-193">Azure Automation</span></span>
  - <span data-ttu-id="7ce7a-194">Добавлен командлет Get-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="7ce7a-194">Added Get-AzureRmAutomationHybridWorkerGroup</span></span>