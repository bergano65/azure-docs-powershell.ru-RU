---
title: Критические изменения в Microsoft Azure PowerShell Az 1.0.0
description: Это руководство по миграции содержит список критических изменений, внесенных в выпуск Az версии 1 в Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/14/2018
ms.openlocfilehash: be3e19dc4b689adbc63b933dd9f3454122d5344a
ms.sourcegitcommit: c6fd0e490fa0e33b8b768b679682a47d8faae1cf
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/16/2019
ms.locfileid: "54342212"
---
# <a name="migration-guide-for-az-100"></a>Руководство по миграции для Az версии 1.0.0

Этот документ описывает изменения между AzureRM версии 6.x и Az версии 1.0.0.

## <a name="table-of-contents"></a>Оглавление
- [Общие критически важные изменения](#general-breaking-changes)
  - [Изменения префикса существительного командлета](#cmdlet-noun-prefix-changes)
  - [Изменение имени модуля](#module-name-changes)
  - [Удаленные модули](#removed-modules)
  - [Windows PowerShell 5.1 и .NET 4.7.2](#windows-powershell-51-and-net-472)
  - [Временное удаление входа пользователя с помощью PSCredential](#temporary-removal-of-user-login-using-pscredential)
  - [Вход с кодом устройства по умолчанию вместо запроса веб-браузера](#temporary-default-device-code-login-instead-of-web-browser-prompt)
- [Критические изменения модуля](#module-breaking-changes)
  - [Az.ApiManagement (ранее AzureRM.ApiManagement)](#azapimanagement-previously-azurermapimanagement)
  - [Az.Billing (ранее AzureRM.Billing, AzureRM.Consitation и AzureRM.UsageAggregates)](#azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates)
  - [Az.CognitiveServices (ранее AzureRM.CognitiveServices)](#azcognitiveservices-previously-azurermcognitiveservices)
  - [Az.Compute (ранее AzureRM.Compute)](#azcompute-previously-azurermcompute)
  - [Az.DataFactory (ранее AzureRM.DataFactories и AzureRM.DataFactoryV2)](#azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2)
  - [Az.DataLakeAnalytics (ранее AzureRM.DataLakeAnalytics)](#azdatalakeanalytics-previously-azurermdatalakeanalytics)
  - [Az.DataLakeStore (ранее AzureRM.DataLakeStore)](#azdatalakestore-previously-azurermdatalakestore)
  - [Az.KeyVault (ранее AzureRM.KeyVault)](#azkeyvault-previously-azurermkeyvault)
  - [Az.Media (ранее AzureRM.Media)](#azmedia-previously-azurermmedia)
  - [Az.Monitor (ранее AzureRM.Insights)](#azmonitor-previously-azurerminsights)
  - [Az.Network (ранее AzureRM.Network)](#aznetwork-previously-azurermnetwork)
  - [Az.OperationalInsights (ранее AzureRM.OperationalInsights)](#azoperationalinsights-previously-azurermoperationalinsights)
  - [Az.RecoveryServices (ранее AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup и AzureRM.RecoveryServices.SiteRecovery)](#azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery)
  - [Az.Resources (ранее AzureRM.Resources)](#azresources-previously-azurermresources)
  - [Az.ServiceFabric (ранее AzureRM.ServiceFabric)](#azservicefabric-previously-azurermservicefabric)
  - [Az.Sql (ранее AzureRM.Sql)](#azsql-previously-azurermsql)
  - [Az.Storage (ранее Azure.Storage и AzureRM.Storage)](#azstorage-previously-azurestorage-and-azurermstorage)
  - [Az.Websites (ранее AzureRM.Websites)](#azwebsites-previously-azurermwebsites)

## <a name="general-breaking-changes"></a>Общие критически важные изменения
### <a name="cmdlet-noun-prefix-changes"></a>Изменения префикса существительного командлета
В AzureRM командлеты использовали либо "AzureRM", либо "Azure" в качестве префикса существительного.  Az упрощает и нормализует имена командлетов, так что все командлеты используют "Az" в качестве префикса существительного командлета. Например: 
```powershell
Get-AzureRMVM
Get-AzureKeyVaultSecret
```

Изменено на
```powershell
Get-AzVM
Get-AzKeyVaultSecret
```

Чтобы упростить переход на эти новые имена командлетов, Az представляет два новых командлета: ```Enable-AzureRmAlias``` и ```Disable-AzureRmAlias```.  ```Enable-AzureRmAlias``` создает псевдонимы из старых имен командлетов в AzureRM для новых имен командлетов Az.  Командлет позволяет создавать псевдонимы в текущем сеансе или во всех сеансах путем изменения профиля пользователя или компьютера. 

Следующий сценарий в AzureRM является примером.
```powershell
#Requires -Modules AzureRM.Storage
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

Его можно выполнить с минимальными изменениями с помощью ```Enable-AzureRmAlias```.
```powershell
#Requires -Modules Az.Storage
Enable-AzureRmAlias
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

Выполнение ```Enable-AzureRmAlias -Scope CurrentUser``` включит псевдонимы для всех открытых сеансов PowerShell, так что после выполнения этого командлета такой сценарий вообще не нужно будет изменять.
```powershell
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

Для получения дополнительных сведений об использовании командлетов псевдонимов выполните ```Get-Help -Online Enable-AzureRmAlias``` в командной строке PowerShell.

```Disable-AzureRmAlias``` удаляет псевдонимы командлетов AzureRM, созданные ```Enable-AzureRmAlias```.  Для получения дополнительных сведений выполните ```Get-Help -Online Disable-AzureRmAlias``` в командной строке PowerShell.

### <a name="module-name-changes"></a>Изменение имени модуля
- Имена модулей изменены с `AzureRM.*` на `Az.*`, за исключением следующих модулей.
```
AzureRM.Profile                       -> Az.Accounts
Azure.AnalysisServices                -> Az.AnalysisServices
AzureRM.Consumption                   -> Az.Billing
AzureRM.UsageAggregates               -> Az.Billing
AzureRM.DataFactories                 -> Az.DataFactory
AzureRM.DataFactoryV2                 -> Az.DataFactory
AzureRM.MachineLearningCompute        -> Az.MachineLearning
AzureRM.Insights                      -> Az.Monitor
AzureRM.RecoveryServices.Backup       -> Az.RecoveryServices
AzureRM.RecoveryServices.SiteRecovery -> Az.RecoveryServices
AzureRM.Tags                          -> Az.Resources
Azure.Storage                         -> Az.Storage
```

Изменения в именах модулей означают, что любой сценарий, который использует ```#Requires``` или ```Import-Module``` для загрузки определенных модулей, необходимо будет изменить, чтобы вместо него использовать новый модуль.

#### <a name="migrating-requires-statements"></a>Миграция операторов #Requires
Сценарии, использующие #Requires для объявления зависимости от модулей AzureRM, должны быть обновлены для использования новых имен модулей.
```powershell
#Requires -Module AzureRM.Compute
```

Следует изменить на
```powershell
#Requires -Module Az.Compute
```

#### <a name="migrating-import-module-statements"></a>Миграция операторов Import-Module
Сценарии, которые используют ```Import-Module``` для загрузки модулей AzureRM, необходимо обновить, чтобы отразились новые имена модулей.
```powershell
Import-Module -Name AzureRM.Compute
```

Следует изменить на
```powershell
Import-Module -Name Az.Compute
```

### <a name="migrating-fully-qualified-cmdlet-invocations"></a>Миграция вызовов командлета Fully-Qualified
Сценарии, использующие квалифицированные вызовы командлетов, ниже приведен пример.
```powershell
AzureRM.Compute\Get-AzureRmVM
```

Следует изменить, чтобы использовать новые имена модулей и командлетов.
```powershell
Az.Compute\Get-AzVM
```

### <a name="migrating-module-manifest-dependencies"></a>Миграция зависимостей манифеста модуля
Модули, которые выражают зависимости от модулей AzureRM через файл манифеста модуля (.psd1), должны обновить имена модулей в разделе "RequiredModules".

```powershell
RequiredModules = @(@{ModuleName="AzureRM.Profile"; ModuleVersion="5.8.2"})
```

Следует изменить на

```powershell
RequiredModules = @(@{ModuleName="Az.Profile"; ModuleVersion="1.0.0"})
```

### <a name="removed-modules"></a>Удаленные модули
- `AzureRM.Backup`
- `AzureRM.Compute.ManagedService`
- `AzureRM.Scheduler`

Средства для работы с этими службами больше не поддерживаются.  Клиентам рекомендуется обратиться к альтернативным службам, как только появится возможность.

### <a name="windows-powershell-51-and-net-472"></a>Windows PowerShell 5.1 и .NET 4.7.2
- Для использования Az с Windows PowerShell 5.1 требуется установка .NET 4.7.2. Тем не менее для использования Az с PowerShell Core не требуется .NET 4.7.2. 

### <a name="temporary-removal-of-user-login-using-pscredential"></a>Временное удаление входа пользователя с помощью PSCredential
- Из-за изменений в процессе проверки подлинности для .NET Standard мы временно удаляем вход пользователя через PSCredential. Эта возможность будет доступна в выпуске от 15 января 2019 г. для Windows PowerShell 5.1. Это подробно описано [здесь.](https://github.com/Azure/azure-powershell/issues/7430)

### <a name="default-device-code-login-instead-of-web-browser-prompt"></a>Вход с кодом устройства по умолчанию вместо запроса веб-браузера
- Из-за изменений в процессе проверки подлинности для .NET Standard мы используем вход устройства в качестве потока входа по умолчанию во время интерактивного входа. Вход через веб-браузер будет повторно представлен для Windows PowerShell 5.1 в качестве версии по умолчанию в выпуске от 15 января 2019 г. В это время пользователи смогут выбрать вход устройства с помощью параметра Switch.

## <a name="module-breaking-changes"></a>Критические изменения модуля

### <a name="azapimanagement-previously-azurermapimanagement"></a>Az.ApiManagement (ранее AzureRM.ApiManagement)
- Удаление приведенных ниже командлетов.
  - New-AzureRmApiManagementHostnameConfiguration
  - Set-AzureRmApiManagementHostnames
  - Update-AzureRmApiManagementDeployment
  - Import-AzureRmApiManagementHostnameCertificate
  - Используйте командлет **Set-AzApiManagement**, чтобы установить эти свойства
- Следующие свойства были удалены.
  - Удалены свойства: `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` и `ScmHostnameConfiguration` типа `PsApiManagementHostnameConfiguration` из `PsApiManagementContext`. Вместо этого используйте: `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` и `ScmCustomHostnameConfiguration` типа `PsApiManagementCustomHostNameConfiguration`.
  - Свойство `StaticIPs` удалено из PsApiManagementContext. Свойство было разделено на `PublicIPAddresses` и `PrivateIPAddresses`.
  - Обязательное свойство `Location` удалено из командлета New-AzureApiManagementVirtualNetwork.

### <a name="azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates"></a>Az.Billing (ранее AzureRM.Billing, AzureRM.Consitation и AzureRM.UsageAggregates)
- Параметр `InvoiceName` удален из командлета `Get-AzConsumptionUsageDetail`.  Для сценариев необходимо использовать другие параметры идентификации для счета.

### <a name="azcognitiveservices-previously-azurermcognitiveservices"></a>Az.CognitiveServices (ранее AzureRM.CognitiveServices)
- Набор параметров `GetSkusWithAccountParamSetName` удален из командлета `Get-AzCognitiveServicesAccountSkus`.  Необходимо получить Skus по типу и расположению учетной записи, а не использовать ResourceGroupName и имя учетной записи.

### <a name="azcompute-previously-azurermcompute"></a>Az.Compute (ранее AzureRM.Compute)
- `IdentityIds` удалены из свойства `Identity` в объектах `PSVirtualMachine` и `PSVirtualMachineScaleSet`. Сценарии больше не должны использовать значение этого поля для принятия решений об обработке.
- Тип свойства `InstanceView` объекта `PSVirtualMachineScaleSetVM` изменен с `VirtualMachineInstanceView` на `VirtualMachineScaleSetVMInstanceView`
- Свойства `AutoOSUpgradePolicy` и `AutomaticOSUpgrade` удалены из свойства `UpgradePolicy`
- Тип свойства `Sku` в объекте `PSSnapshotUpdate` изменен с `DiskSku` на `SnapshotSku`
- `VmScaleSetVMParameterSet` удалено из командлета `Add-AzVMDataDisk`, вы больше не можете отдельно добавлять диск с данными в виртуальную машину масштабируемого набора.

### <a name="azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2"></a>Az.DataFactory (ранее AzureRM.DataFactories и AzureRM.DataFactoryV2)
- Параметр `GatewayName` стал обязательным в командлете `New-AzDataFactoryEncryptValue`
- Командлет `New-AzDataFactoryGatewayKey` удалено
- Параметр `LinkedServiceName` удален из командлета `Get-AzDataFactoryV2ActivityRun`. Сценарии больше не должны использовать значение этого поля для принятия решений об обработке.

### <a name="azdatalakeanalytics-previously-azurermdatalakeanalytics"></a>Az.DataLakeAnalytics (ранее AzureRM.DataLakeAnalytics)
- Удалены следующие нерекомендуемые командлеты: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret` и `Set-AzDataLakeAnalyticsCatalogSecret`.

### <a name="azdatalakestore-previously-azurermdatalakestore"></a>Az.DataLakeStore (ранее AzureRM.DataLakeStore)
- В следующих командлетах параметр `Encoding` изменен с типа `FileSystemCmdletProviderEncoding` на `System.Text.Encoding`. Это изменение удаляет значения кодирования `String` и `Oem`. Все остальные предыдущие значения кодирования остаются.
  - New-AzureRmDataLakeStoreItem
  - Add-AzureRmDataLakeStoreItemContent
  - Get-AzureRmDataLakeStoreItemContent
- Удален нерекомендуемый псевдоним свойства `Tags` из командлетов `New-AzDataLakeStoreAccount` и `Set-AzDataLakeStoreAccount`.

  Сценарии, которые используют
  ```powershell
  New-AzureRMDataLakeStoreAccount -Tags @{TagName="TagValue"}
  ```

  следует изменить на
  ```powershell
  New-AzDataLakeStoreAccount -Tag @{TagName="TagValue"}
  ```

- Из объекта ```PSDataLakeStoreAccountBasic``` удалены нерекомендуемые свойства: ```Identity```, ```EncryptionState```, ```EncrypotionProvisioningState```, ```EncryptionConfig```, ```FirewallState```, ```FirewallRules```, ```VirtualNetworkRules```, ```TrustedIdProviderState```, ```TrustedIdProviders```, ```DefaultGroup```, ```NewTier```, ```CurrentTier```, ```FirewallAllowAzureIps```.  Любой сценарий, который использует ```PSDatalakeStoreAccount```, возвращенный из ```Get-AzDataLakeStoreAccount```, не должен ссылаться на эти свойства.

### <a name="azkeyvault-previously-azurermkeyvault"></a>Az.KeyVault (ранее AzureRM.KeyVault)
- Свойство `PurgeDisabled` было удалено из объектов `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem` и `PSKeyVaultSecretAttributes`. Сценарии больше не должны ссылаться на свойство ```PurgeDisabled``` для принятия решений об обработке.

### <a name="azmedia-previously-azurermmedia"></a>Az.Media (ранее AzureRM.Media)
- Удалите нерекомендуемый псевдоним свойства `Tags` из командлета `New-AzMediaService`. Сценарии, которые используют
  ```powershell
  New-AzureRMMediaService -Tags @{TagName="TagValue"}
  ```

  следует изменить на
  ```powershell
  New-AzMMediaService -Tag @{TagName="TagValue"}
  ```
### <a name="azmonitor-previously-azurerminsights"></a>Az.Monitor (ранее AzureRM.Insights)
- Множественные имена `Categories` и `Timegrains` параметра удалены в пользу единичных имен параметров из командлета `Set-AzDiagnosticSetting`. Сценарии, которые используют
  ```powershell
  Set-AzureRmDiagnosticSetting -Timegrains PT1M -Categories Category1, Category2
  ```

  следует изменить на
  ```powershell
  Set-AzDiagnosticSetting -Timegrain PT1M -Category Category1, Category2
  ```
### <a name="aznetwork-previously-azurermnetwork"></a>Az.Network (ранее AzureRM.Network)
- Из командлета `Get-AzServiceEndpointPolicyDefinition` удален нерекомендуемый параметр `ResourceId`
- Из объекта `PSVirtualNetwork` удалено нерекомендуемое свойство `EnableVmProtection`
- Нерекомендуемый командлет `Set-AzVirtualNetworkGatewayVpnClientConfig` удален
  
Сценарии больше не должны принимать решения об обработке на основе значений этих полей.

### <a name="azoperationalinsights-previously-azurermoperationalinsights"></a>Az.OperationalInsights (ранее AzureRM.OperationalInsights)
- Набор параметров по умолчанию для `Get-AzOperationalInsightsDataSource` удален и заменен на `ByWorkspaceNameByKind`.

  Сценарии, в которых перечислены источники данных, использующие
  ```powershell
  Get-AzureRmOperationalInsightsDataSource
  ```

  следует изменить, чтобы указать вид
  ```powershell
  Get-AzOperationalInsightsDataSource -Kind AzureActivityLog
  ```

### <a name="azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery"></a>Az.RecoveryServices (ранее AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup и AzureRM.RecoveryServices.SiteRecovery)
- Из командлета `New/Set-AzRecoveryServicesAsrPolicy` удален параметр `Encryption`.
- Параметр `TargetStorageAccountName` теперь является обязательным для восстановления управляемого диска в командлете `Restore-AzRecoveryServicesBackupItem`.
- В командлете `Restore-AzRecoveryServicesBackupItem` удалены параметры `StorageAccountName` и `StorageAccountResourceGroupName`.
- В командлете `Get-AzRecoveryServicesBackupContainer` удален параметр `Name`.

### <a name="azresources-previously-azurermresources"></a>Az.Resources (ранее AzureRM.Resources)
- Из командлета `New/Set-AzPolicyAssignment` удален параметр `Sku`.
- Параметр `Password` удален из командлетов `New-AzADServicePrincipal` и `New-AzADSpCredential`. Пароли генерируются автоматически. Сценарии, которые предоставили пароль:
  ```powershell
  New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $secPassword
  ```

  следует изменить, чтобы получить пароль из выходных данных.
  ```powershell
  $credential = New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
  $secPassword = $credential.Secret
  ```

### <a name="azservicefabric-previously-azurermservicefabric"></a>Az.ServiceFabric (ранее AzureRM.ServiceFabric)
- Следующие типы возвращаемого значения командлета были изменены.
  - Свойство `SerivceTypeHealthPolicies` типа `ApplicationHealthPolicy` удалено.
  - Свойство `ApplicationHealthPolicies` типа `ClusterUpgradeDeltaHealthPolicy` удалено.
  - Свойство `OverrideUserUpgradePolicy` типа `ClusterUpgradePolicy` удалено.
  - Эти изменения влияют на следующие командлеты:
    - Add-AzServiceFabricClientCertificate;
    - Add-AzServiceFabricClusterCertificate;
    - Add-AzServiceFabricNode;
    - Add-AzServiceFabricNodeType;
    - Get-AzServiceFabricCluster;
    - Remove-AzServiceFabricClientCertificate;
    - Remove-AzServiceFabricClusterCertificate;
    - Remove-AzServiceFabricNode;
    - Remove-AzServiceFabricNodeType;
    - Remove-AzServiceFabricSetting;
    - Set-AzServiceFabricSetting;
    - Set-AzServiceFabricUpgradeType;
    - Update-AzServiceFabricDurability;
    - Update-AzServiceFabricReliability.

### <a name="azsql-previously-azurermsql"></a>Az.Sql (ранее AzureRM.Sql)
- Из командлета `Set-AzSqlDatabaseBackupLongTermRetentionPolicy` удалены параметры `State` и `ResourceId`.
- Удалены следующие нерекомендуемые командлеты: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`.
- Из командлета `Get-AzSqlDatabaseBackupLongTermRetentionPolicy` удален нерекомендуемый параметр `Current`
- Из командлета `Get-AzSqlServerServiceObjective` удален нерекомендуемый параметр `DatabaseName`
- Из командлета `Set-AzSqlDatabaseDataMaskingPolicy` удален нерекомендуемый параметр `PrivilegedLogin`

### <a name="azstorage-previously-azurestorage-and-azurermstorage"></a>Az.Storage (ранее Azure.Storage и AzureRM.Storage)
- Для поддержки создания контекста хранения Oauth только с именем учетной записи хранения набор параметров по умолчанию был изменен на `OAuthParameterSet`.
  - Пример: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`
- Параметр `Location` стал обязательным в командлете `Get-AzStorageUsage`
- Методы API службы хранилища теперь используют асинхронную модель на основе задач (TAP) вместо синхронных вызовов API.
#### <a name="1-blob-snapshot"></a>1. Моментальный снимок большого двоичного объекта
##### <a name="before"></a>До:
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$b.ICloudBlob.Snapshot()
```

##### <a name="after"></a>После:
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$task = $b.ICloudBlob.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="2-share-snapshot"></a>2. Общий доступ к снимку
##### <a name="before"></a>До:
```powershell
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$snapshot = $Share.Snapshot()
```
#####  <a name="after"></a>После:
```powershell

$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$task = $Share.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="3-undelete-a-soft-delete-blob"></a>3. Отмена обратимого удаления большого двоичного объекта
##### <a name="before"></a>До:
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$b.ICloudBlob.Undelete()
```
##### <a name="after"></a>После:
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$task = $b.ICloudBlob.UndeleteAsync()
$task.Wait()
```

#### <a name="4-set-blob-tier"></a>4. Установка уровня большого двоичного объекта
##### <a name="before"></a>До:
```powershell
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$blockBlob.ICloudBlob.SetStandardBlobTier("hot")

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$pageBlob.ICloudBlob.SetPremiumBlobTier("P4")
```

##### <a name="after"></a>После:
```powershell
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$task = $blockBlob.ICloudBlob.SetStandardBlobTierAsync("hot")
$task.Wait()

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$task = $pageBlob.ICloudBlob.SetPremiumBlobTierAsync("P4")
$task.Wait()
```

### <a name="azwebsites-previously-azurermwebsites"></a>Az.Websites (ранее AzureRM.Websites)
- Из объектов `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo` и `PSSite` удалены нерекомендуемые свойства.