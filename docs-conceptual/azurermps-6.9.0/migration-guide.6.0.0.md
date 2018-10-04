---
title: Критически важные изменения в Microsoft Azure PowerShell 6.0.0
description: Это руководство по миграции содержит список критических изменений, внесенных в выпуск Azure PowerShell версии 6.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/01/2018
ms.openlocfilehash: 227bec0f7eb24b0941e9e21d37524b290c4b83a5
ms.sourcegitcommit: 6c38e86e16da99f65cd183c63e34f7176b121ab8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "47424791"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-600"></a>Критически важные изменения в Microsoft Azure PowerShell 6.0.0

Этот документ предназначен для уведомления о критических изменениях и является руководством по миграции для пользователей командлетов Microsoft Azure PowerShell. В каждом разделе описана причина критического изменения и самый простой путь миграции. Подробное описание см. в запросах на вытягивание для каждого изменения.

## <a name="table-of-contents"></a>Оглавление

- [Общие критически важные изменения](#general-breaking-changes)
    - [Минимальная требуемая версия изменена на PowerShell 5.0](#minimum-powershell-version-required-bumped-to-50)
    - [Автосохранение контекста включено по умолчанию](#context-autosave-enabled-by-default)
    - [Удаление псевдонимов Tags](#removal-of-tags-alias)
- [Критически важные изменения в командлетах AzureRM.Compute](#breaking-changes-to-azurermcompute-cmdlets)
- [Критически важные изменения в командлетах AzureRM.DataLakeStore](#breaking-changes-to-azurermdatalakestore-cmdlets)
- [Критически важные изменения в командлетах AzureRM.Dns](#breaking-changes-to-azurermdns-cmdlets)
- [Критически важные изменения в командлетах AzureRM.Insights](#breaking-changes-to-azurerminsights-cmdlets)
- [Критически важные изменения в командлетах AzureRM.KeyVault](#breaking-changes-to-azurermkeyvault-cmdlets)
- [Критически важные изменения в командлетах AzureRM.Network](#breaking-changes-to-azurermnetwork-cmdlets)
- [Критически важные изменения в командлетах AzureRM.RedisCache](#breaking-changes-to-azurermrediscache-cmdlets)
- [Критически важные изменения в командлетах AzureRM.Resources](#breaking-changes-to-azurermresources-cmdlets)
- [Критически важные изменения в командлетах AzureRM.Storage](#breaking-changes-to-azurermstorage-cmdlets)
- [Удаленные модули](#removed-modules)
    - [`AzureRM.ServerManagement`](#azurermservermanagement)
    - [`AzureRM.SiteRecovery`](#azurermsiterecovery)

## <a name="general-breaking-changes"></a>Общие критически важные изменения

### <a name="minimum-powershell-version-required-bumped-to-50"></a>Минимальная требуемая версия изменена на PowerShell 5.0

Ранее для выполнения любого командлета требовалась версия _не ниже_ Azure PowerShell 3.0. Со временем требуемая версия повысится до PowerShell 5.0. Сведения об обновлении до PowerShell 5.0 см. в [этой таблице](https://docs.microsoft.com/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).

### <a name="context-autosave-enabled-by-default"></a>Автосохранение контекста включено по умолчанию

Автосохранение контекста подразумевает хранение учетных данных Azure, которые могут использоваться в новых или других сеансах PowerShell. Дополнительные сведения об автосохранении контекста см. в [этом документе](https://docs.microsoft.com/powershell/azure/context-persistence).

Ранее эта функция была отключена по умолчанию, то есть сведения об аутентификации пользователей Azure не сохранялись между сеансами. Чтобы включить сохранение контекста пользователи выполняли командлет `Enable-AzureRmContextAutosave`. Со временем сохранение контекста будет включено по умолчанию, то есть контекст будет сохраняться при следующем входе в систему пользователей _без сохраненных настроек автосохранения контекста_. Пользователи смогут отключить эту функцию с помощью командлета `Disable-AzureRmContextAutosave`.

_Примечание_. Это изменение не повлияет на пользователей, которые ранее отключили автосохранение контекста или включили эту функцию и используют сохраненный контекст.

### <a name="removal-of-tags-alias"></a>Удаление псевдонимов Tags

Псевдоним `Tags` для параметра `Tag` удален во многих командлетах. Ниже приведен список модулей (и соответствующих командлетов), которых коснулось это изменение:

#### `AzureRM.ApiManagement`

- `New-AzureRmApiManagement`
- `New-AzureRmApiManagementProperty`
- `Set-AzureRmApiManagementProperty`

#### `AzureRM.Automation`
- `Set-AzureRmAutomationRunbook`

#### `AzureRM.Cdn`
- `New-AzureRmCdnEndpoint`
- `New-AzureRmCdnProfile`

#### `AzureRM.Compute`
- `New-AzureRmVM`
- `Update-AzureRmVM`

#### `AzureRM.DataFactories`
- `New-AzureRmDataFactories`

#### `AzureRM.DataLakeAnalytics`
- `New-AzureRmDataLakeAnalyticsAccount`

#### `AzureRM.DataLakeStore`
- `New-AzureRmDataLakeStoreAccount`
- `Set-AzureRmDataLakeStoreAccount`

#### `AzureRM.MachineLearning`
- `Update-AzureRmMlCommitmentPlan`

#### `AzureRM.Media`
- `Set-AzureRmMediaService`

#### `AzureRM.OperationalInsights`
- `New-AzureRmOperationalInsightsSavedSearch`
- `New-AzureRmOperationalInsightsWorkspace`
- `Set-AzureRmOperationalInsightsSavedSearch`
- `Set-AzureRmOperationalInsightsWorkspace`

## <a name="breaking-changes-to-azurermcompute-cmdlets"></a>Критически важные изменения в командлетах AzureRM.Compute

**Разное**
- Свойство имени SKU, вложенное в типы `PSDisk` и `PSSnapshot`, изменено с `StandardLRS` и `PremiumLRS` на `Standard_LRS` и `Premium_LRS` соответственно.

```powershell
$disk = Get-AzureRmDisk -ResourceGroupName "MyResourceGroup" -DiskName "MyDiskName"
$disk.Sku.Name       # This will now return Standard_LRS or Premium_LRS

$snapshot = Get-AzureRmSnapshot -ResourceGroupName "MyResourceGroup" -SnapshotName "MySnapshotName"
$snapshot.Sku.Name   # This will now return Standard_LRS or Premium_LRS
```

- Свойство учетной записи хранения, вложенное в типы `PSVirtualMachine`, `PSVirtualMachineScaleSet` и `PSImage`, изменено с `StandardLRS` и `PremiumLRS` на `Standard_LRS` и `Premium_LRS` соответственно.

```powershell
$vm = Get-AzureRmVM -ResourceGroupName "MyResourceGroup" -Name "MyVM"
$vm.StorageProfile.DataDisks[0].ManagedDisk.StorageAccountType   # This will now return Standard_LRS or Premium_LRS
```

**Add-AzureRmImageDataDisk**
- Допустимые значения для параметра `StorageAccountType` изменены с `StandardLRS` и `PremiumLRS` на `Standard_LRS` и `Premium_LRS`соответственно.

**Add-AzureRmVMDataDisk**
- Допустимые значения для параметра `StorageAccountType` изменены с `StandardLRS` и `PremiumLRS` на `Standard_LRS` и `Premium_LRS`соответственно.

**Add-AzureRmVmssDataDisk**
- Допустимые значения для параметра `StorageAccountType` изменены с `StandardLRS` и `PremiumLRS` на `Standard_LRS` и `Premium_LRS`соответственно.

**New-AzureRmAvailabilitySet**
- Параметр `Managed` изменен на `Sku`.

```powershell
# Old
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Managed

# New
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Sku "Aligned"
```

**New-AzureRmDiskConfig**
- Допустимые значения для параметра `SkuName` изменены с `StandardLRS` и `PremiumLRS` на `Standard_LRS` и `Premium_LRS`соответственно.

**New-AzureRmDiskUpdateConfig**
- Допустимые значения для параметра `SkuName` изменены с `StandardLRS` и `PremiumLRS` на `Standard_LRS` и `Premium_LRS`соответственно.

**New-AzureRmSnapshotConfig**
- Допустимые значения для параметра `SkuName` изменены с `StandardLRS` и `PremiumLRS` на `Standard_LRS` и `Premium_LRS`соответственно.

**New-AzureRmSnapshotUpdateConfig**
- Допустимые значения для параметра `SkuName` изменены с `StandardLRS` и `PremiumLRS` на `Standard_LRS` и `Premium_LRS`соответственно.

**Set-AzureRmImageOsDisk**
- Допустимые значения для параметра `StorageAccountType` изменены с `StandardLRS` и `PremiumLRS` на `Standard_LRS` и `Premium_LRS`соответственно.

**Set-AzureRmVMAEMExtension**
- Удален параметр `DisableWAD`.
    -  Система диагностики Microsoft Azure отключена по умолчанию.

**Set-AzureRmVMDataDisk**
- Допустимые значения для параметра `StorageAccountType` изменены с `StandardLRS` и `PremiumLRS` на `Standard_LRS` и `Premium_LRS`соответственно.

**Set-AzureRmVMOSDisk**
- Допустимые значения для параметра `StorageAccountType` изменены с `StandardLRS` и `PremiumLRS` на `Standard_LRS` и `Premium_LRS`соответственно.

**Set-AzureRmVmssStorageProfile**
- Допустимые значения для параметра `ManagedDisk` изменены с `StandardLRS` и `PremiumLRS` на `Standard_LRS` и `Premium_LRS`соответственно.

**Update-AzureRmVmss**
- Допустимые значения для параметра `ManagedDiskStorageAccountType` изменены с `StandardLRS` и `PremiumLRS` на `Standard_LRS` и `Premium_LRS`соответственно.

## <a name="breaking-changes-to-azurermdatalakestore-cmdlets"></a>Критически важные изменения в командлетах AzureRM.DataLakeStore

**Export-AzureRmDataLakeStoreItem**
- Удалены параметры `PerFileThreadCount` и `ConcurrentFileCount`. В дальнейшем используйте параметр `Concurrency`.

```powershell
# Old
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -Concurrency 160
```

**Import-AzureRmDataLakeStoreItem**
- Удалены параметры `PerFileThreadCount` и `ConcurrentFileCount`. В дальнейшем используйте параметр `Concurrency`.

```powershell
# Old
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -Concurrency 160
```

**Remove-AzureRmDataLakeStoreItem**
- Удален параметр `Clean`.

```powershell
# Old
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse -Clean

# New
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse
```

## <a name="breaking-changes-to-azurermdns-cmdlets"></a>Критически важные изменения в командлетах AzureRM.Dns

**New-AzureRmDnsRecordSet**
- Удален параметр `Force`.

**Remove-AzureRmDnsRecordSet**
- Удален параметр `Force`.

**Remove-AzureRmDnsZone**
- Удален параметр `Force`.

## <a name="breaking-changes-to-azurerminsights-cmdlets"></a>Критически важные изменения в командлетах AzureRM.Insights

**Add-AzureRmAutoscaleSetting**
- Удалены псевдонимы параметра `AutoscaleProfiles` и `Notifications`.

**Add-AzureRmLogProfile**
- Удалены псевдонимы параметра `Categories` и `Locations`.

**Add-AzureRmMetricAlertRule**
- Удален псевдоним параметра `Actions`.

**Add-AzureRmWebtestAlertRule**
- Удален псевдоним параметра `Actions`.

**Get-AzureRmLog**
- Удалены псевдонимы параметра `MaxRecords` и `MaxEvents`.

**Get-AzureRmMetricDefinition**
- Удален псевдоним параметра `MetricNames`.

**New-AzureRmAlertRuleEmail**
- Удалены псевдонимы параметра `CustomEmails` и `SendToServiceOwners`.

**New-AzureRmAlertRuleWebhook**
- Удален псевдоним параметра `Properties`.

**New-AzureRmAutoscaleNotification**
- Удалены псевдонимы параметра `CustomEmails`, `SendEmailToSubscriptionCoAdministrators` и `Webhooks`.

**New-AzureRmAutoscaleProfile**
- Удалены псевдонимы параметра `Rules`, `ScheduleDays`, `ScheduleHours` и `ScheduleMinutes`.

**New-AzureRmAutoscaleWebhook**
- Удален псевдоним параметра `Properties`.

## <a name="breaking-changes-to-azurermkeyvault-cmdlets"></a>Критически важные изменения в командлетах AzureRM.KeyVault

**Add-AzureKeyVaultCertificate**
- Параметр `CertificatePolicy` стал обязательным.

**Set-AzureKeyVaultManagedStorageSasDefinition**
- Этот командлет больше не принимает отдельные параметры, из которых состоит маркер доступа. Вместо этого он изменяет такие явные параметры маркеров, как `Service` или `Permissions`, на универсальный параметр `TemplateUri`, который соответствуют примеру маркера доступа, определенному в другом месте (предположительно с помощью командлетов службы хранилища PowerShell или созданных вручную в соответствии с документацией службы хранилища.) В командлете сохранен параметр `ValidityPeriod`.

Дополнительные сведения о создании общих маркеров доступа для службы хранилища Azure см. на страницах соответствующей документации.
- [Constructing a Service SAS] (https://docs.microsoft.com/rest/api/storageservices/Constructing-a-Service-SAS) (Создание подписанного URL-адреса уровня службы)
- [Создание подписанного URL-адреса уровня учетной записи] (https://docs.microsoft.com/rest/api/storageservices/constructing-an-account-sas)

```powershell
# Old
$sas = Set-AzureKeyVaultManagedStorageSasDefinition -VaultName myVault -Name myKey -Service Blob -Permissions 'rcw' -ValidityPeriod 180d

# New
$sctx=New-AzureStorageContext -StorageAccountName $sa.StorageAccountName -Protocol Https -StorageAccountKey Key1
$start=[System.DateTime]::Now.AddDays(-1)
$end=[System.DateTime]::Now.AddMonths(1)
$at=New-AzureStorageAccountSasToken -Service blob -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -StartTime $start -ExpiryTime $end -Context $sctx
$sas=Set-AzureKeyVaultManagedStorageSasDefinition -AccountName $sa.StorageAccountName -VaultName $kv.VaultName -Name accountsas -TemplateUri $at -SasType 'account' -ValidityPeriod ([System.Timespan]::FromDays(30))
```

**Set-AzureKeyVaultCertificateIssuer**
- Параметр `IssuerProvider` стал обязательным.

**Undo-AzureKeyVaultCertificateRemoval**
- Выходной параметр этого командлета изменен с `CertificateBundle` на `PSKeyVaultCertificate`.

**Undo-AzureRmKeyVaultRemoval**
- Параметр `ResourceGroupName` удален из набора параметров `InputObject`. Вместо этого значения извлекаются из свойства `ResourceId` параметра `InputObject`.

**Set-AzureRmKeyVaultAccessPolicy**
- Разрешение `all` удалено из `PermissionsToKeys`, `PermissionsToSecrets` и `PermissionsToCertificates`.

**Общие сведения**
- Свойство `ValueFromPipelineByPropertyName` удалено из всех командлетов, в которых включен запуск конвейера с использованием свойства `InputObject`.  Это коснулось следующих командлетов:
    - `Add-AzureKeyVaultCertificate`
    - `Add-AzureKeyVaultCertificateContact`
    - `Add-AzureKeyVaultKey`
    - `Backup-AzureKeyVaultKey`
    - `Backup-AzureKeyVaultSecret`
    - `Get-AzureKeyVaultCertficate`
    - `Get-AzureKeyVaultCertificateContact`
    - `Get-AzureKeyVaultCertificateIssuer`
    - `Get-AzureKeyVaultCertificateOperation`
    - `Get-AzureKeyVaultCertificatePolicy`
    - `Get-AzureKeyVaultKey`
    - `Get-AzureKeyVaultManagedStorageAccount`
    - `Get-AzureKeyVaultManagedStorageSasDefinition`
    - `Get-AzureKeyVaultSecret`
    - `Remove-AzureRmKeyVault`
    - `Remove-AzureRmKeyVaultAccessPolicy`
    - `Remove-AzureKeyVaultCertificate`
    - `Remove-AzureKeyVaultCertificateContact`
    - `Remove-AzureKeyVaultCertificateIssuer`
    - `Remove-AzureKeyVaultCertificateOperation`
    - `Remove-AzureKeyVaultKey`
    - `Remove-AzureKeyVaultManagedStorageAccount`
    - `Remove-AzureKeyVaultManagedStorageSasDefinition`
    - `Remove-AzureKeyVaultSecret`
    - `Restore-AzureKeyVaultKey`
    - `Restore-AzureKeyVaultSecret`
    - `Set-AzureRmKeyVaultAccessPolicy`
    - `Set-AzureKeyVaultCertificateAttribute`
    - `Set-AzureKeyVaultCertificateIssuer`
    - `Set-AzureKeyVaultCertificatePolicy`
    - `Set-AzureKeyVaultKeyAttribute`
    - `Set-AzureKeyVaultManagedStorageSasDefinition`
    - `Set-AzureKeyVaultSecret`
    - `Set-AzureKeyVaultSecretAttribute`
    - `Stop-AzureKeyVaultCertificateOperation`
    - `Undo-AzureKeyVaultCertificateRemoval`
    - `Undo-AzureKeyVaultKeyRemoval`
    - `Undo-AzureRmKeyVaultRemoval`
    - `Undo-AzureKeyVaultSecretRemoval`
    - `Update-AzureKeyVaultManagedStorageAccount`
    - `Update-AzureKeyVaultManagedStorageAccountKey`

- Уровни `ConfirmImpact` удалены из всех командлетов.  Это коснулось следующих командлетов:
    - `Remove-AzureRmKeyVault`
    - `Remove-AzureKeyVaultCertificate`
    - `Remove-AzureKeyVaultCertificateIssuer`
    - `Remove-AzureKeyVaultCertificateOperation`
    - `Remove-AzureKeyVaultKey`
    - `Remove-AzureKeyVaultManagedStorageAccount`
    - `Remove-AzureKeyVaultManagedStorageSasDefinition`
    - `Remove-AzureKeyVaultSecret`
    - `Stop-AzureKeyVaultCertificateOperation`
    - `Update-AzureKeyVaultManagedStorageAccountKey`

- Обновлен параметр `IKeyVaultDataServiceClient`. Теперь все операции с сертификатами возвращают PSTypes вместо типов пакетов SDK. А именно:
    - `SetCertificateContacts`
    - `GetCertificateContacts`
    - `GetCertificate`
    - `GetDeletedCertificate`
    - `MergeCertificate`
    - `ImportCertificate`
    - `DeleteCertificate`
    - `RecoverCertificate`
    - `EnrollCertificate`
    - `UpdateCertificate`
    - `GetCertificateOperation`
    - `DeleteCertificateOperation`
    - `CancelCertificateOperation`
    - `GetCertificatePolicy`
    - `UpdateCertificatePolicy`
    - `GetCertificateIssuer`
    - `SetCertificateIssuer`
    - `DeleteCertificateIssuer`

## <a name="breaking-changes-to-azurermnetwork-cmdlets"></a>Критически важные изменения в командлетах AzureRM.Network


**Add-AzureRmApplicationGatewayBackendHttpSettings**
- Удален параметр `ProbeEnabled`.

**Add-AzureRmVirtualNetworkPeering**
- Удален псевдоним параметра `AlloowGatewayTransit`.

**New-AzureRmApplicationGatewayBackendHttpSettings**
- Удален параметр `ProbeEnabled`.

**Set-AzureRmApplicationGatewayBackendHttpSettings**
- Удален параметр `ProbeEnabled`.

## <a name="breaking-changes-to-azurermrediscache-cmdlets"></a>Критически важные изменения в командлетах AzureRM.RedisCache

**New-AzureRmRedisCache**
- Параметры `Subnet` и `VirtualNetwork` заменены на `SubnetId`.
- Удален параметр `RedisVersion`.
- Параметр `MaxMemoryPolicy` заменен на `RedisConfiguration`.

```powershell
# Old
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -MaxMemoryPolicy "allkeys-lru"

# New
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

**Set-AzureRmRedisCache**
- Параметр `MaxMemoryPolicy` заменен на `RedisConfiguration`.

```powershell
# Old
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -MaxMemoryPolicy "allkeys-lru"

# New
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

## <a name="breaking-changes-to-azurermresources-cmdlets"></a>Критически важные изменения в командлетах AzureRM.Resources

**Find-AzureRmResource**
- Этот командлет удален и его функции переданы `Get-AzureRmResource`.

```powershell
# Old
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupNameContains "ResourceGroup"
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceNameContains "test"

# New
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupName "*ResourceGroup*"
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -Name "*test*"
```

**Find-AzureRmResourceGroup**
- Этот командлет удален и его функции переданы `Get-AzureRmResourceGroup`.

```powershell
# Old
Find-AzureRmResourceGroup
Find-AzureRmResourceGroup -Tag @{ "testtag" = $null }
Find-AzureRmResourceGroup -Tag @{ "testtag" = "testval" }

# New
Get-AzureRmResourceGroup
Get-AzureRmResourceGroup -Tag @{ "testtag" = $null }
Get-AzureRmResourceGroup -Tag @{ "testtag" = "testval" }
```

**Get-AzureRmRoleDefinition**
- Удален параметр `AtScopeAndBelow`.

```powershell

# Old
Get-AzureRmRoleDefinition [other required parameters] -AtScopeAndBelow

# New
Get-AzureRmRoleDefinition [other required parameters]
```

## <a name="breaking-changes-to-azurermstorage-cmdlets"></a>Критически важные изменения в командлетах AzureRM.Storage

**New-AzureRmStorageAccount**
- Удален параметр `EnableEncryptionService`.

**Set-AzureRmStorageAccount**
- Удалены параметры `EnableEncryptionService` и `DisableEncryptionService`.

## <a name="removed-modules"></a>Удаленные модули

### `AzureRM.ServerManagement`

Использование службы "Средства управления серверами" (SMT) [прекращено в прошлом году](https://blogs.technet.microsoft.com/servermanagement/2017/05/17/smt-preview-service-is-being-retired-on-june-30-2017/). Поэтому соответствующий модуль для SMT `AzureRM.ServerManagement` удален из `AzureRM` и в дальнейшем не будет предоставляться.

### `AzureRM.SiteRecovery`

Модуль `AzureRM.SiteRecovery` изменится на `AzureRM.RecoveryServices.SiteRecovery` — функциональное супермножество модуля `AzureRM.SiteRecovery`, содержащее новый набор эквивалентных командлетов. Полный список сопоставлений старых и новых командлетов см. ниже.

| Нерекомендуемые командлеты                                        | Эквивалентные командлеты                                                | Псевдонимы                                  |
|----------------------------------------------------------|------------------------------------------------------------------|------------------------------------------|
| `Edit-AzureRmSiteRecoveryRecoveryPlan`                   | `Edit-AzureRmRecoveryServicesAsrRecoveryPlan`                    | `Edit-ASRRecoveryPlan`                   |
| `Get-AzureRmSiteRecoveryFabric`                          | `Get-AzureRmRecoveryServicesAsrFabric`                           | `Get-ASRFabric`                          |
| `Get-AzureRmSiteRecoveryJob`                             | `Get-AzureRmRecoveryServicesAsrJob`                              | `Get-ASRJob`                             |
| `Get-AzureRmSiteRecoveryNetwork`                         | `Get-AzureRmRecoveryServicesAsrNetwork`                          | `Get-ASRNetwork`                         |
| `Get-AzureRmSiteRecoveryNetworkMapping`                  | `Get-AzureRmRecoveryServicesAsrNetworkMapping`                   | `Get-ASRNetworkMapping`                  |
| `Get-AzureRmSiteRecoveryPolicy`                          | `Get-AzureRmRecoveryServicesAsrPolicy`                           | `Get-ASRPolicy`                          |
| `Get-AzureRmSiteRecoveryProtectableItem`                 | `Get-AzureRmRecoveryServicesAsrProtectableItem`                  | `Get-ASRProtectableItem`                 |
| `Get-AzureRmSiteRecoveryProtectionContainer`             | `Get-AzureRmRecoveryServicesAsrProtectionContainer`              | `Get-ASRProtectionContainer`             |
| `Get-AzureRmSiteRecoveryProtectionContainerMapping`      | `Get-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `Get-ASRProtectionContainerMapping`      |
| `Get-AzureRmSiteRecoveryProtectionEntity`                | `Get-AzureRmRecoveryServicesAsrProtectableItem`                  | `Get-ASRProtectableItem`                 |
| `Get-AzureRmSiteRecoveryRecoveryPlan`                    | `Get-AzureRmRecoveryServicesAsrRecoveryPlan`                     | `Get-ASRRecoveryPlan`                    |
| `Get-AzureRmSiteRecoveryRecoveryPoint`                   | `Get-AzureRmRecoveryServicesAsrRecoveryPoint`                    | `Get-ASRRecoveryPoint`                   |
| `Get-AzureRmSiteRecoveryReplicationProtectedItem`        | `Get-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Get-ASRReplicationProtectedItem`        |
| `Get-AzureRmSiteRecoveryServer`                          | `Get-AzureRmRecoveryServicesAsrServicesProvider`                 | `Get-ASRServicesProvider`                |
| `Get-AzureRmSiteRecoveryServicesProvider`                | `Get-AzureRmRecoveryServicesAsrServicesProvider`                 | `Get-ASRServicesProvider`                |
| `Get-AzureRmSiteRecoverySite`                            | `Get-AzureRmRecoveryServicesAsrFabric`                           | `Get-ASRFabric`                          |
| `Get-AzureRmSiteRecoveryStorageClassification`           | `Get-AzureRmRecoveryServicesAsrStorageClassification`            | `Get-ASRStorageClassification`           |
| `Get-AzureRmSiteRecoveryStorageClassificationMapping`    | `Get-AzureRmRecoveryServicesAsrStorageClassificationMapping`     | `Get-ASRStorageClassificationMapping`    |
| `Get-AzureRmSiteRecoveryVault`                           | `Get-AzureRmRecoveryServicesVault`                               |                                          |
| `Get-AzureRmSiteRecoveryVaultSettings`                   | `Get-AzureRmRecoveryServicesAsrVaultContext`                     |                                          |
| `Get-AzureRmSiteRecoveryVaultSettingsFile`               | `Get-AzureRmRecoveryServicesVaultSettingsFile`                   |                                          |
| `Get-AzureRmSiteRecoveryVM`                              | `Get-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Get-ASRReplicationProtectedItem`        |
| `Import-AzureRmSiteRecoveryVaultSettingsFile`            | `Import-AzureRmRecoveryServicesAsrVaultSettingsFile`             |                                          |
| `New-AzureRmSiteRecoveryFabric`                          | `New-AzureRmRecoveryServicesAsrFabric`                           | `New-ASRFabric`                          |
| `New-AzureRmSiteRecoveryNetworkMapping`                  | `New-AzureRmRecoveryServicesAsrNetworkMapping`                   | `New-ASRNetworkMapping`                  |
| `New-AzureRmSiteRecoveryPolicy`                          | `New-AzureRmRecoveryServicesAsrPolicy`                           | `New-ASRPolicy`                          |
| `New-AzureRmSiteRecoveryProtectionContainerMapping`      | `New-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `New-ASRProtectionContainerMapping`      |
| `New-AzureRmSiteRecoveryRecoveryPlan`                    | `New-AzureRmRecoveryServicesAsrRecoveryPlan`                     | `New-ASRRecoveryPlan`                    |
| `New-AzureRmSiteRecoveryReplicationProtectedItem`        | `New-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `New-ASRReplicationProtectedItem`        |
| `New-AzureRmSiteRecoverySite`                            | `New-AzureRmRecoveryServicesAsrFabric`                           | `New-ASRFabric`                          |
| `New-AzureRmSiteRecoveryStorageClassificationMapping`    | `New-AzureRmRecoveryServicesAsrStorageClassificationMapping`     | `New-ASRStorageClassificationMapping`    |
| `New-AzureRmSiteRecoveryVault`                           | `New-AzureRmRecoveryServicesVault`                               |                                          |
| `Remove-AzureRmSiteRecoveryFabric`                       | `Remove-AzureRmRecoveryServicesAsrFabric`                        | `Remove-ASRFabric`                       |
| `Remove-AzureRmSiteRecoveryNetworkMapping`               | `Remove-AzureRmRecoveryServicesAsrNetworkMapping`                | `Remove-ASRNetworkMapping`               |
| `Remove-AzureRmSiteRecoveryPolicy`                       | `Remove-AzureRmRecoveryServicesAsrPolicy`                        | `Remove-ASRPolicy`                       |
| `Remove-AzureRmSiteRecoveryProtectionContainerMapping`   | `Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping`    | `Remove-ASRProtectionContainerMapping`   |
| `Remove-AzureRmSiteRecoveryRecoveryPlan`                 | `Remove-AzureRmRecoveryServicesAsrRecoveryPlan`                  | `Remove-ASRRecoveryPlan`                 |
| `Remove-AzureRmSiteRecoveryReplicationProtectedItem`     | `Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem`      | `Remove-ASRReplicationProtectedItem`     |
| `Remove-AzureRmSiteRecoveryServer`                       | `Remove-AzureRmRecoveryServicesAsrServicesProvider`              |                                          |
| `Remove-AzureRmSiteRecoveryServicesProvider`             | `Remove-AzureRmRecoveryServicesAsrServicesProvider`              | `Remove-ASRServicesProvider`             |
| `Remove-AzureRmSiteRecoverySite`                         | `Remove-AzureRmRecoveryServicesAsrFabric`                        | `Remove-ASRFabric`                       |
| `Remove-AzureRmSiteRecoveryStorageClassificationMapping` | `Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping`  | `Remove-ASRStorageClassificationMapping` |
| `Remove-AzureRmSiteRecoveryVault`                        | `Remove-AzureRmRecoveryServicesVault`                            |                                          |
| `Restart-AzureRmSiteRecoveryJob`                         | `Restart-AzureRmRecoveryServicesAsrJob`                          | `Restart-ASRJob`                         |
| `Resume-AzureRmSiteRecoveryJob`                          | `Resume-AzureRmRecoveryServicesAsrJob`                           | `Resume-ASRJob`                          |
| `Set-AzureRmSiteRecoveryProtectionEntity`                | `New-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `New-ASRReplicationProtectedItem`        |
| `Set-AzureRmSiteRecoveryReplicationProtectedItem`        | `Set-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Set-ASRReplicationProtectedItem`        |
| `Set-AzureRmSiteRecoveryVaultSettings`                   | `Set-AzureRmRecoveryServicesAsrVaultContext`                     | `Set-ASRVaultContext`                    |
| `Set-AzureRmSiteRecoveryVM`                              | `Set-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Set-ASRReplicationProtectedItem`        |
| `Start-AzureRmSiteRecoveryApplyRecoveryPoint`            | `Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint`             | `Start-ASRApplyRecoveryPoint`            |
| `Start-AzureRmSiteRecoveryCommitFailoverJob`             | `Start-AzureRmRecoveryServicesAsrCommitFailoverJob`              | `Start-ASRCommitFailoverJob`             |
| `Start-AzureRmSiteRecoveryPlannedFailoverJob`            | `Start-AzureRmRecoveryServicesAsrPlannedFailoverJob`             | `Start-ASRPlannedFailoverJob`            |
| `Start-AzureRmSiteRecoveryPolicyAssociationJob`          | `New-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `New-ASRProtectionContainerMapping`      |
| `Start-AzureRmSiteRecoveryPolicyDissociationJob`         | `Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping`    | `Remove-ASRProtectionContainerMapping`   |
| `Start-AzureRmSiteRecoveryTestFailoverJob`               | `Start-AzureRmRecoveryServicesAsrTestFailoverJob`                | `Start-ASRTestFailoverJob`               |
| `Start-AzureRmSiteRecoveryUnplannedFailoverJob`          | `Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob`           | `Start-ASRUnplannedFailoverJob`          |
| `Stop-AzureRmSiteRecoveryJob`                            | `Stop-AzureRmRecoveryServicesAsrJob`                             | `Stop-ASRJob`                            |
| `Update-AzureRmSiteRecoveryPolicy`                       | `Update-AzureRmRecoveryServicesAsrPolicy`                        | `Update-ASRPolicy`                       |
| `Update-AzureRmSiteRecoveryProtectionDirection`          | `Update-AzureRmRecoveryServicesAsrProtectionDirection`           | `Update-ASRProtectionDirection`          |
| `Update-AzureRmSiteRecoveryRecoveryPlan`                 | `Update-AzureRmRecoveryServicesAsrRecoveryPlan`                  | `Update-ASRRecoveryPlan`                 |
| `Update-AzureRmSiteRecoveryServer`                       | `Update-AzureRmRecoveryServicesAsrServicesProvider`              | `Update-ASRServicesProvider`             |
| `Update-AzureRmSiteRecoveryServicesProvider`             | `Update-AzureRmRecoveryServicesAsrvCenter`                       | `Update-ASRvCenter`                      |
