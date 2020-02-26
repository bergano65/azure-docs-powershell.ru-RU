---
title: Все отличия между AzureRM и Az версии 1.0.0 для Azure PowerShell
description: Это руководство по миграции содержит список критических изменений, внесенных в выпуск Az версии 1 в Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2019
ms.openlocfilehash: e5121d61b0f5f68ff3e1f33d774e3533adfeb64f
ms.sourcegitcommit: a321ef9d134c684fa24ababcbd898f86b00d9364
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "77477769"
---
# <a name="breaking-changes-for-az-100"></a>Критические изменения для Az 1.0.0

В этом документе содержатся подробные сведения об отличиях между AzureRM 6.x и новым модулем Az версии 1.x и более поздних. Пункты в оглавлении помогут вам разобраться со всеми этапами переноса, включая изменения модуля, которые могут повлиять на скрипты.

Общие советы по началу перехода с Az на AzureRM см. в [этой статье](migrate-from-azurerm-to-az.md).

> [!IMPORTANT]
> Кроме того, после выхода версии Az 1.0.0 также были внесены критические изменения, которые представлены в Az 2.0.0. Выполнив действия по переходу с AzureRM на Az, представленные в этом руководстве, перейдите к статье [о критических изменениях в Az 2.0.0](migrate-az-2.0.0.md), чтобы узнать, необходимо ли вам внести дополнительные изменения.

## <a name="table-of-contents"></a>Оглавление

- [Общие критически важные изменения](#general-breaking-changes)
  - [Изменения префикса существительного командлета](#cmdlet-noun-prefix-changes)
  - [Изменение имени модуля](#module-name-changes)
  - [Удаленные модули](#removed-modules)
  - [Windows PowerShell 5.1 и .NET 4.7.2](#windows-powershell-51-and-net-472)
  - [Временное удаление входа пользователя с помощью PSCredential](#temporary-removal-of-user-login-using-pscredential)
  - [Вход с кодом устройства по умолчанию вместо запроса веб-браузера](#default-device-code-login-instead-of-web-browser-prompt)
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

В этом разделе описаны общие критические изменения, которые являются частью этой переработанной версии модуля Az.

### <a name="cmdlet-noun-prefix-changes"></a>Изменения префикса существительного командлета

В модуле AzureRM в существительных командлетов используется префикс `AzureRM` или `Azure`.  Az упрощает и нормализует имена командлетов, так что все командлеты используют "Az" в качестве префикса существительного командлета. Пример:

```azurepowershell-interactive
Get-AzureRMVM
Get-AzureKeyVaultSecret
```

изменено на:

```azurepowershell-interactive
Get-AzVM
Get-AzKeyVaultSecret
```

Чтобы упростить переход на эти новые имена командлетов, Az представляет два новых командлета: [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) и [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).  `Enable-AzureRmAlias` создает псевдонимы для старых имен командлетов в AzureRM, которые сопоставляются с новыми именами командлетов Az. Используя аргумент `-Scope` с командлетом `Enable-AzureRmAlias`, вы можете выбрать, в контексте чего будут включены псевдонимы.

Следующий сценарий в AzureRM является примером.

```azurepowershell-interactive
#Requires -Modules AzureRM.Storage
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

Его можно выполнить с минимальными изменениями с помощью `Enable-AzureRmAlias`.

```azurepowershell-interactive
#Requires -Modules Az.Storage
Enable-AzureRmAlias -Scope Process
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

При выполнении `Enable-AzureRmAlias -Scope CurrentUser` псевдонимы будут включены для всех открытых сеансов PowerShell, так что после выполнения этого командлета такой сценарий не нужно будет изменять.

```azurepowershell-interactive
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

Дополнительные сведения об использовании командлетов псевдонимов см. в [справочнике по командлету Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias).

Когда вы будете готовы отключить псевдонимы, запустите командлет `Disable-AzureRmAlias`, который удаляет созданные псевдонимы. Дополнительные сведения см. в [справочнике по командлету Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).

> [!IMPORTANT]
> Убедитесь, что отключили псевдонимы для _всех_ областей, в которых они были включены.

### <a name="module-name-changes"></a>Изменение имени модуля

Имена модулей изменены с `AzureRM.*` на `Az.*`, за исключением следующих модулей.

| Модуль AzureRM | Модуль Az |
|----------------|-----------|
| Azure.Storage; | Az.Storage |
| Azure.AnalysisServices | Az.AnalysisServices |
| AzureRM.Profile | Az.Accounts |
| AzureRM.Insights; | Az.Monitor |
| AzureRM.DataFactories | Az.DataFactory |
| AzureRM.DataFactoryV2 | Az.DataFactory |
| AzureRM.RecoveryServices.Backup | Az.RecoveryServices |
| AzureRM.RecoveryServices.SiteRecovery | Az.RecoveryServices |
| AzureRM.Tags | Az.Resources |
| AzureRM.MachineLearningCompute | Az.MachineLearning |
| AzureRM.UsageAggregates | Az.Billing |
| AzureRM.Consumption: | Az.Billing |

Изменения в именах модулей означают, что любой сценарий, который использует `#Requires` или `Import-Module` для загрузки определенных модулей, необходимо будет изменить, чтобы вместо него использовать новый модуль. Для модулей, в которых суффикс командлета не был изменен, это означает, что хотя имя модуля изменилось, суффикс, указывающий пространство операции, _не изменился_.

#### <a name="migrating-requires-and-import-module-statements"></a>Перенос инструкций #Requires и Import-Module

Скрипты, объявляющие зависимости от модулей AzureRM с помощью `#Requires` или `Import-Module`, должны быть обновлены для использования новых имен модулей. Пример:

```azurepowershell-interactive
#Requires -Module AzureRM.Compute
```

следует изменить на

```azurepowershell-interactive
#Requires -Module Az.Compute
```

Для `Import-Module`:

```azurepowershell-interactive
Import-Module -Name AzureRM.Compute
```

следует изменить на

```azurepowershell-interactive
Import-Module -Name Az.Compute
```

### <a name="migrating-fully-qualified-cmdlet-invocations"></a>Миграция вызовов командлета Fully-Qualified

Скрипты, использующие вызовы командлетов с указанием модуля, например:

```azurepowershell-interactive
AzureRM.Compute\Get-AzureRmVM
```

Следует изменить, чтобы использовать новые имена модулей и командлетов:

```azurepowershell-interactive
Az.Compute\Get-AzVM
```

### <a name="migrating-module-manifest-dependencies"></a>Перенос зависимостей манифеста модуля

Модули, которые выражают зависимости от модулей AzureRM через файл манифеста модуля (PSD1), должны обновить имена модулей в разделе `RequiredModules`.

```powershell
RequiredModules = @(@{ModuleName="AzureRM.Profile"; ModuleVersion="5.8.2"})
```

Необходимо изменить на:

```powershell
RequiredModules = @(@{ModuleName="Az.Profile"; ModuleVersion="1.0.0"})
```

### <a name="removed-modules"></a>Удаленные модули

Следующие модули удалены:

- `AzureRM.Backup`
- `AzureRM.Compute.ManagedService`
- `AzureRM.Scheduler`

Средства для работы с этими службами больше не поддерживаются.  Клиентам рекомендуется обратиться к альтернативным службам, как только появится возможность.

### <a name="windows-powershell-51-and-net-472"></a>Windows PowerShell 5.1 и .NET 4.7.2

Для использования Az с PowerShell 5.1 для Windows требуется установить .NET Framework 4.7.2. Для использования PowerShell Core 6.x или более поздней версии .NET Framework не требуется.

### <a name="temporary-removal-of-user-login-using-pscredential"></a>Временное удаление входа пользователя с помощью PSCredential

Из-за изменений в процессе проверки подлинности для .NET Standard мы временно удаляем вход пользователя через PSCredential. Эта возможность будет доступна в выпуске от 15 января 2019 г. для Windows PowerShell 5.1. Это подробно описано в [этом сообщении на сайте GitHub](https://github.com/Azure/azure-powershell/issues/7430).

### <a name="default-device-code-login-instead-of-web-browser-prompt"></a>Вход с кодом устройства по умолчанию вместо запроса веб-браузера

Из-за изменений в процессе проверки подлинности для .NET Standard мы используем вход устройства в качестве потока входа по умолчанию во время интерактивного входа. Вход через веб-браузер будет повторно представлен для Windows PowerShell 5.1 в качестве версии по умолчанию в выпуске от 15 января 2019 г. В это время пользователи смогут выбрать вход устройства с помощью параметра Switch.

## <a name="module-breaking-changes"></a>Критические изменения модуля

В этом разделе описаны конкретные критические изменения для отдельных модулей и командлетов.

### <a name="azapimanagement-previously-azurermapimanagement"></a>Az.ApiManagement (ранее AzureRM.ApiManagement)

- Удалены приведенные ниже командлеты.
  - New-AzureRmApiManagementHostnameConfiguration
  - Set-AzureRmApiManagementHostnames
  - Update-AzureRmApiManagementDeployment
  - Import-AzureRmApiManagementHostnameCertificate
  - Используйте командлет **Set-AzApiManagement**, чтобы задать эти свойства.
- Удалены приведенные ниже свойства.
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
- Параметр `VmScaleSetVMParameterSet` удален из командлета `Add-AzVMDataDisk`. Больше нельзя отдельно добавлять диск данных в виртуальную машину из масштабируемого набора.

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
  ```azurepowershell-interactive
  New-AzureRMDataLakeStoreAccount -Tags @{TagName="TagValue"}
  ```

  следует изменить на
  ```azurepowershell-interactive
  New-AzDataLakeStoreAccount -Tag @{TagName="TagValue"}
  ```

- Из объекта `PSDataLakeStoreAccountBasic` удалены нерекомендуемые свойства: `Identity`, `EncryptionState`, `EncryptionProvisioningState`, `EncryptionConfig`, `FirewallState`, `FirewallRules`, `VirtualNetworkRules`, `TrustedIdProviderState`, `TrustedIdProviders`, `DefaultGroup`, `NewTier`, `CurrentTier`, `FirewallAllowAzureIps`.  Любой сценарий, который использует `PSDatalakeStoreAccount`, возвращенный из `Get-AzDataLakeStoreAccount`, не должен ссылаться на эти свойства.

### <a name="azkeyvault-previously-azurermkeyvault"></a>Az.KeyVault (ранее AzureRM.KeyVault)

- Свойство `PurgeDisabled` удалено из объектов `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem` и `PSKeyVaultSecretAttributes`. Скрипты больше не должны ссылаться на свойство ```PurgeDisabled``` для принятия решений об обработке.

### <a name="azmedia-previously-azurermmedia"></a>Az.Media (ранее AzureRM.Media)

- Удалите нерекомендуемый псевдоним свойства `Tags` из командлета `New-AzMediaService`. Сценарии, которые используют
  ```azurepowershell-interactive
  New-AzureRMMediaService -Tags @{TagName="TagValue"}
  ```

  следует изменить на
  ```azurepowershell-interactive
  New-AzMediaService -Tag @{TagName="TagValue"}
  ```

### <a name="azmonitor-previously-azurerminsights"></a>Az.Monitor (ранее AzureRM.Insights)

- Множественные имена `Categories` и `Timegrains` параметра удалены в пользу единичных имен параметров из командлета `Set-AzDiagnosticSetting`. Сценарии, которые используют
  ```azurepowershell-interactive
  Set-AzureRmDiagnosticSetting -Timegrains PT1M -Categories Category1, Category2
  ```

  следует изменить на
  ```azurepowershell-interactive
  Set-AzDiagnosticSetting -Timegrain PT1M -Category Category1, Category2
  ```

### <a name="aznetwork-previously-azurermnetwork"></a>Az.Network (ранее AzureRM.Network)

- Из командлета `Get-AzServiceEndpointPolicyDefinition` удален нерекомендуемый параметр `ResourceId`
- Из объекта `PSVirtualNetwork` удалено нерекомендуемое свойство `EnableVmProtection`
- Нерекомендуемый командлет `Set-AzVirtualNetworkGatewayVpnClientConfig` удален

Скрипты больше не должны принимать решения об обработке на основе значений этих полей.

### <a name="azoperationalinsights-previously-azurermoperationalinsights"></a>Az.OperationalInsights (ранее AzureRM.OperationalInsights)

- Набор параметров по умолчанию для `Get-AzOperationalInsightsDataSource` удален и заменен на `ByWorkspaceNameByKind`.

  Сценарии, в которых перечислены источники данных, использующие
  ```azurepowershell-interactive
  Get-AzureRmOperationalInsightsDataSource
  ```

  следует изменить, чтобы указать вид
  ```azurepowershell-interactive
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

  ```azurepowershell-interactive
  New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $secPassword
  ```

  Следует изменить, чтобы получить пароль из выходных данных.

  ```azurepowershell-interactive
  $credential = New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
  $secPassword = $credential.Secret
  ```

### <a name="azservicefabric-previously-azurermservicefabric"></a>Az.ServiceFabric (ранее AzureRM.ServiceFabric)

- Следующие типы возвращаемого значения командлета были изменены.
  - Свойство `ServiceTypeHealthPolicies` типа `ApplicationHealthPolicy` удалено.
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
  - Например, `$ctx = New-AzureStorageContext -StorageAccountName $accountName`.
- Параметр `Location` стал обязательным в командлете `Get-AzStorageUsage`
- Методы API службы хранилища теперь используют асинхронную модель на основе задач (TAP) вместо синхронных вызовов API. В приведенных ниже примерах показаны новые асинхронные команды.

#### <a name="blob-snapshot"></a>Моментальный снимок большого двоичного объекта

AzureRM:

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$b.ICloudBlob.Snapshot()
```

Az:

```azurepowershell-interactive
$b = Get-AzStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$task = $b.ICloudBlob.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="share-snapshot"></a>Общий доступ к снимку

AzureRM:

```azurepowershell-interactive
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$snapshot = $Share.Snapshot()
```

Az:

```azurepowershell-interactive
$Share = Get-AzStorageShare -Name $containerName -Context $ctx
$task = $Share.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="undelete-soft-deleted-blob"></a>Отмена удаления обратимо удаленных больших двоичных объектов

AzureRM:

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$b.ICloudBlob.Undelete()
```

Az:

```azurepowershell-interactive
$b = Get-AzStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$task = $b.ICloudBlob.UndeleteAsync()
$task.Wait()
```

#### <a name="set-blob-tier"></a>Установка уровня большого двоичного объекта

AzureRM:

```azurepowershell-interactive
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$blockBlob.ICloudBlob.SetStandardBlobTier("hot")

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$pageBlob.ICloudBlob.SetPremiumBlobTier("P4")
```

Az:

```azurepowershell-interactive
$blockBlob = Get-AzStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$task = $blockBlob.ICloudBlob.SetStandardBlobTierAsync("hot")
$task.Wait()

$pageBlob = Get-AzStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$task = $pageBlob.ICloudBlob.SetPremiumBlobTierAsync("P4")
$task.Wait()
```

### <a name="azwebsites-previously-azurermwebsites"></a>Az.Websites (ранее AzureRM.Websites)

- Из объектов `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo` и `PSSite` удалены нерекомендуемые свойства.
