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
ms.openlocfilehash: 2a6e20137f12ae9317c7eeed330a2433774e1ea9
ms.sourcegitcommit: f648ac92fafb16cc0e9ca6bc85d00fa327baf396
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/28/2018
ms.locfileid: "43018705"
---
# <a name="release-notes"></a>Заметки о выпуске

Здесь приведен список изменений, внесенных в Azure PowerShell в этом выпуске.

---
## <a name="670---august-2018"></a>6.7.0 — август 2018 г.
#### <a name="azurermprofile"></a>AzureRM.Profile
* Обновление до последней версии Azure ClientRuntime.
* Добавлен идентификатор пользователя для имени контекста по умолчанию, чтобы избежать конфликтов контекста.
    - https://github.com/Azure/azure-powershell/issues/6489
* Устранены проблемы с командлетом Clear-AzureRmContext, которые приводили к проблемам с выбором контекста #6398.
* Разрешено передавать домен клиента в параметр -TenantId для командлета Connect-AzureRmAccount.
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a>Azure.Storage;
* Удалено ограничение в 5 ТБ для квоты на общую папку Azure.
- Set-AzureStorageShareQuota

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azureanalysisservices"></a>Azure.AnalysisServices
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermapplicationinsights"></a>AzureRM.ApplicationInsights
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermautomation"></a>AzureRM.Automation
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermbackup"></a>AzureRM.Backup
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermbatch"></a>AzureRM.Batch
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermbilling"></a>AzureRM.Billing
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermcdn"></a>AzureRM.Cdn
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Обновление до последней версии Azure ClientRuntime.
* В командлет New-AzureRmVmssConfig добавлен параметр EvictionPolicy.
* Если расположение не указано, используйте в DiskFileParameterSet для New AzureRmVm расположение по умолчанию.
* Исправлено описание параметров в Save-AzureRmVMImage.
* Исправлен командлет Get-AzureRmVMDiskEncryptionStatus для определенных сценариев, связанных с однократным выполнением.

#### <a name="azurermconsumption"></a>AzureRM.Consumption:
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermcontainerregistry"></a>AzureRM.ContainerRegistry
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermdatafactories"></a>AzureRM.DataFactories
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Исправлена отладка, когда DebugPreference настраивается из командной строки PowerShell.
* Обновлен пример для Set-AzureRmDataLakeStoreItemAcl.
* Обновление до последней версии Azure ClientRuntime.
* Обновлен пример для Set-AzureRmDataLakeStoreItemAclEntry.

#### <a name="azurermdevtestlabs"></a>AzureRM.DevTestLabs
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermdns"></a>AzureRM.Dns
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermeventgrid"></a>AzureRM.EventGrid
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermhdinsight"></a>AzureRM.HDInsight
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurerminsights"></a>AzureRM.Insights;
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermiothub"></a>AzureRM.IotHub
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermlogicapp"></a>AzureRM.LogicApp
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermmachinelearning"></a>AzureRM.MachineLearning
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermmachinelearningcompute"></a>AzureRM.MachineLearningCompute
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermmarketplaceordering"></a>AzureRM.MarketplaceOrdering
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermmedia"></a>AzureRM.Media
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermnetwork"></a>AzureRM.Network
* Добавлен пример для Set-AzureRmLocalNetworkGateway.
* Добавлены примеры и описания для Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey и New-AzureRmVirtualNetworkGatewayConnection.
* Добавлены примеры для Remove-AzureRmVirtualNetworkGatewayIpConfig и Reset-AzureRmVirtualNetworkGateway.
* Добавлен пример для Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.
* Добавлен пример для Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.
* Добавлен пример для Set-AzureRmVirtualNetworkGatewayConnection.
* Повторно созданы командлеты для ApplicationSecurityGroup, RouteTable и Usage с помощью генератора кода последней версии.
* Уточнено сообщение об ошибке для Get-AzureRmVirtualNetworkSubnetConfig при попытке получить подсеть, которая не существует.

#### <a name="azurermnotificationhubs"></a>AzureRM.NotificationHubs
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights;
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermpolicyinsights"></a>AzureRM.PolicyInsights
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermpowerbiembedded"></a>AzureRM.PowerBIEmbedded
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermrecoveryservices"></a>AzureRM.RecoveryServices
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* Добавлен фильтр политик для командлета Get-AzureRmRecoveryServicesBackItem. Команда возвращает список элементов резервного копирования, защищенных политикой с заданным идентификатором.
* Обновление Microsoft.Azure.Management.RecoveryServices.Backup до версии 3.0.0-preview.
* Обновление до последней версии Azure ClientRuntime.
* Добавлен параметр TargetResourceGroupName для Restore-AzureRmRecoveryServicesBackupItem. Группа ресурсов, в которую восстанавливаются управляемые диски. Применимо к резервной копии виртуальной машины с управляемыми дисками.

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermrediscache"></a>AzureRM.RedisCache
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermrelay"></a>AzureRM.Relay
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermresources"></a>AzureRM.Resources
* Поддержка развертывания шаблонов в области подписки. Добавлены новые командлеты:
    - New-AzureRmDeployment
    - Get-AzureRmDeployment
    - Test-AzureRmDeployment
    - Remove-AzureRmDeployment
    - Stop-AzureRmDeployment
    - Save-AzureRmDeploymentTemplate
    - Get-AzureRmDeploymentOperation
* Устранена проблема, когда при передаче контекста в Set-AzureRmResource возникает ошибка.
    - https://github.com/Azure/azure-powershell/issues/5705
* Исправлен пример в New-AzureRmResourceGroupDeployment.
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermscheduler"></a>AzureRM.Scheduler
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermsql"></a>AzureRM.Sql
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermstorage"></a>AzureRM.Storage
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermstreamanalytics"></a>AzureRM.StreamAnalytics
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermtags"></a>AzureRM.Tags
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermusageaggregates"></a>AzureRM.UsageAggregates
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Обновление до последней версии Azure ClientRuntime.

## <a name="660---july-2018"></a>6.6.0 — июль 2018 г.
#### <a name="general"></a>Общие сведения
* Обновлены все файлы справки: включены полные типы параметров и исправлены типы входных и выходных данных.

#### <a name="azurermprofile"></a>AzureRM.Profile
* Обновлена библиотека Common.Strategy: теперь можно проверить, совместима ли текущая конфигурация ресурса с целевым ресурсом.
* В Common.Storage добавлены типы ps1xml.

#### <a name="azurestorage"></a>Azure.Storage;
* Добавлена поддержка для получения контекста хранилища из DefaultProfile.
* В свойства типов выходных данных командлетов добавлен атрибут Ps1XmlAttribute.

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6370.
    - В AutoMapper исправлена ошибка, препятствовавшая преобразованию PsApiManagementApi в ApiContract.
* Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6515.
    - В File.Save исправлена ошибка, связанная с перегрузкой типом кодировки.
* Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6560.
    - Выполнено обновление до версии NuGet 4.0.3, что позволило исправить исключение шаблона в apiId.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Устранена ошибка при создании виртуальной машины с помощью командлета New-AzureRmVm и параметра DiskFileParameterSet, которая возникала из-за переименования типа учетной записи хранения PremiumLRS.
* Исправлен командлет Invoke-AzureRmVMRunCommand.
* Командлет Get-AzureRmAvailabilitySet теперь может выводить список всех групп доступности в подписке.  (Параметр ResouceGroupName теперь является необязательным.)
* Обновлен параметр SimpleParameterSet командлета New-AzureRmVm, что позволило использовать ускоренную сеть на соответствующих виртуальных машинах.
* Обновлен простой набор параметров New-AzureRmVmss, что позволило отменять создание масштабируемого набора виртуальных машин, если указанная пользователем подсистема балансировки нагрузки уже существует.
* Обновлен пример для New-AzureRmDisk.
* Добавлен пример для New-AzureRmVM.
* Обновлено описание командлета Set-AzureRmVMOSDisk.
* Обновлен пример 1 для Set-AzureRmVMBginfoExtension: исправлены орфографические ошибки и префикс. 

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Пакет .NET SDK для ADF обновлен до версии 1.1.0.
* Добавлена поддержка совместного использования локальной среды IR несколькими фабриками данных.
     - Добавлен новый параметр -SharedIntegrationRuntimeResourceId для командлета Set-AzureRmDataFactoryV2IntegrationRuntime.
     - Добавлен новый необязательный параметр -LinkedDataFactoryName для командлета Remove-AzureRmDataFactoryV2IntegrationRuntime.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Пакет SDK для плоскости данных (Microsoft.Azure.DataLake.Store) обновлен до версии 1.1.9.

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Обновлена конвейерная передача для InputObject и ResourceId в командлетах remove.

#### <a name="azurerminsights"></a>AzureRM.Insights;
* Исправлено форматирование OutputType в файлах справки.
* Применен пакет SDK Microsoft.Azure.Management.Monitor 0.19.1-preview.

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Исправлена проблема с конвейерной передачей в командлете Set-AzureRmKeyVaultAccessPolicy.

#### <a name="azurermnetwork"></a>AzureRM.Network
* Добавлены примеры для командлетов LoadBalancerInboundNatPoolConfig.

#### <a name="azurermresources"></a>AzureRM.Resources
* Устранена проблема, возникавшая при указании имени и значения тега для Get-AzureRmResource.
    - https://github.com/Azure/azure-powershell/issues/6765
* Исправлен сценарий конвейерной передачи в Set-AzureRmResource.

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Обновлена конвейерная передача для InputObject и ResourceId в командлетах remove.
* Исправлено несколько ошибок.
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a>AzureRM.Sql
* Добавлена поддержка Advanced Threat Protection для сервера с помощью следующих командлетов:
    - Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy.
* Добавлена поддержка оценки уязвимостей с помощью следующих командлетов:
    - Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings;
    - Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline;
    - Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan.
* Исправлен пример для Remove-AzureRmSqlServerFirewallRule.
* Исправлена неправильная обработка даты и времени для базового языка и региональных параметров, отличных от США, в Get-AzureSqlSyncGroupLog.

#### <a name="azurermstorage"></a>AzureRM.Storage
* В свойства типов выходных данных командлетов добавлен атрибут Ps1XmlAttribute.
* Выходные данные командлетов StorageAccount теперь отображаются в виде таблицы.
    - Get-AzureRmStorageAccount
    - New-AzureRmStorageAccount;
    - Set-AzureRmStorageAccount.

#### <a name="azurermtags"></a>AzureRM.Tags
* Удалено неверное утверждение из справки по командлетам Tag.
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a>6.5.0 — июль 2018 г.
#### <a name="azurermprofile"></a>AzureRM.Profile
* Обновлена справка для командлета Get-AzureRmContextAutosaveSetting.

#### <a name="azurestorage"></a>Azure.Storage;
* Добавлена поддержка отправки BLOB-объекта или файла с помощью токена SAS, доступного только для записи.
- Set-AzureStorageBlobContent
- Set-AzureStorageFileContent

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Для AS добавлено обязательное свойство ResourceGroupName.

#### <a name="azurermautomation"></a>AzureRM.Automation
* Обновлена справка и добавлены примеры для командлета New-AzureRMAutomationSchedule.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Добавлен параметр -Tag для командлета Update/New-AzureRmAvailabilitySet.
* Добавлен пример для командлета Add-AzureRmVmssExtension.
* Добавлены примеры для командлета Remove-AzureRmVmssExtension.
* Обновлена справка для командлета Set-AzureRmVMAccessExtension.
* Изменен класс SimpleParameterSet для командлета New-AzureRmVmss: теперь для SinglePlacementGroup по умолчанию задается значение false, а также добавляется параметр-переключатель SinglePlacementGroup, который позволяет пользователю создать VMSS в одной группе размещения.

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* В класс PSEventHubDRConfigurationAttributes добавлено доступное только для чтения свойство PendingReplicationOperationsCount, которое показывает количество ожидающих репликации операций во время реплицирования.

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Обновлено сообщение об ошибке для командлета Set-AzureRmKeyVaultAccessPolicy.

#### <a name="azurermlogicapp"></a>AzureRM.LogicApp
* Исправлена ошибка "parameter set could not be resolved" (не удалось разрешить заданный параметр) в командлете New-AzureRmLogicApp.

#### <a name="azurermnetwork"></a>AzureRM.Network
* Включен пиринг между виртуальными сетями в нескольких клиентах для командлета Set/Add-AzureRmVirtualNetworkPeering.
* Для шлюза приложений обновлены следующие командлеты:
    - New-AzureRmApplicationGateway: добавлены флаг EnableFIPS и поддержка зон.
    - New-AzureRmApplicationGatewaySku: добавлены новые номера SKU Standard_v2 и WAF_v2.
    - Set-AzureRmApplicationGatewaySku: добавлены новые номера SKU Standard_v2 и WAF_v2.
* Командлеты RouteTable пересозданы в последней версии генератора.

#### <a name="azurermrelay"></a>AzureRM.Relay
* Обновлены файлы Markdown, исправлена проблема с именем параметра в примере.

#### <a name="azurermresources"></a>AzureRM.Resources
* Обновлены командлеты Roleassignment и roledefinition:
    - Удалены лишние вызовы roledefinition, выполняемые в ходе разбиения на страницы.
* Исправлен командлет Get-AzureRmRoleAssignment.
    - Исправлена работа параметра -ExpandPrincipalGroups.
* Устранена проблема в командлете Get-AzureRmResource, заключающая в том, что в параметре -ResourceType учитывался регистр символов.

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Добавлены параметры top и skip для командлетов list.
* Добавлены командлеты для перехода с пространства имен ценовой категории "Стандартный" на пространство ценовой категории "Премиум":
    - Start-AzureRmServiceBusMigration;
    - Get-AzureRmServiceBusMigration;
    - Complete-AzureRmServiceBusMigration;
    - Stop-AzureRmServiceBusMigration;
    - Remove-AzureRmServiceBusMigration.
* В класс PSServiceBusDRConfigurationAttributes добавлено доступное только для чтения свойство PendingReplicationOperationsCount, которое показывает количество ожидающих репликации операций во время реплицирования.

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Обновлен пример для командлета New-AzureRmServiceFabricCluster.

#### <a name="azurermsql"></a>AzureRM.Sql
* Добавлены новые командлеты для Management.Sql, позволяющие клиентам добавлять сертификат TDE в экземпляр SQL Server или управляемый экземпляр:
    - Add-AzureRmSqlServerTransparentDataEncryptionCertificate;
    - Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate.

#### <a name="azurermwebsites"></a>AzureRM.Websites
* `Set-AzureRmWebApp -AssignIdentity` и `Set-AzureRmWebAppSlot -AssignIdentity` при установленном значении false теперь будут удалять свойство Identity из объекта сайта. Также при этом будет удаляться тег предварительной версии.
* Обновлен пример для `Get-AzureRmWebAppMetrics` и `Get-AzureRmAppServicePlanMetrics`.
* `Set-AzureRmWebApp -PhpVersion` теперь поддерживает off как допустимую версию PHP.

## <a name="640---july-2018"></a>6.4.0 — июль 2018 г.
#### <a name="general"></a>Общие сведения
* Исправлено форматирование OutputType в файлах справки для большинства модулей.

#### <a name="azurermprofile"></a>AzureRM.Profile
* В основные типы выходных данных добавлен атрибут Ps1Xml.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Функция добавления тега IP-адреса для масштабируемого набора виртуальных машин (VMSS)
    - Добавлен командлет New-AzureRmVmssIpTagConfig.
    - В New-AzureRmVmssIpConfig добавлен параметр IpTag.
* Функция автоматического отката ОС для VMSS
    - В New-AzureRmVmssConfig и Update-AzureRmVmss добавлены параметры DisableAutoRollback.
* Функция ведения журнала обновлений ОС для VMSS
    - В Get-AzureRmVmss добавлен параметр OSUpgradeHistory.

#### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* Добавлена поддержка списков управления доступом к каталогу с использованием следующих команд:
    - Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry;
    - Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry;
    - Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Добавлены поддержка отмены выполнения и отслеживание хода выполнения для Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl и Remove-AzureRmDataLakeStoreItemAclEntry.
* Добавлена поддержка отмены выполнения для Export-AzureRmDataLakeStoreChildItemProperties.
* Исправлена очистка сообщений об отладке для командлетов, которые выполняют рекурсивные операции.
* Исправлено расположение тестовых данных для командлетов DataLake.

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Для командлетов вывода списка операций Get-AzureRmEventHub и Get-AzureRmEventHubConsumerGroup добавлен необязательный параметр MaxCount.
* Исправлена проблема с командлетом New-AzureRmEventHub, из-за которой требовалось указать по крайней мере один параметр при создании концентратора событий. Добавлен набор параметров по умолчанию.
* Для командлета New-AzureRmEventHubKey добавлен необязательный параметр -KeyValue, который позволяет пользователю предоставить значение ключа.

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Исправлена ошибка, из-за которой при выполнении командлета Get-AzureRmKeyVault с параметром -Tag возвращались все ресурсы.

#### <a name="azurermnetwork"></a>AzureRM.Network
* Для параметра шлюзов виртуальной вести, избыточных между зонами, предоставлены новые номера SKU.
* Добавлены новые команды для функции поддержки партнерских API для ExpressRoute, развертываемых с помощью ARM:
    - добавлена команда Get-AzureRmExpressRouteCrossConnection;
    - добавлена команда Set-AzureRmExpressRouteCrossConnection;
    - добавлена команда Add-AzureRmExpressRouteCrossConnectionPeering;
    - добавлена команда Get-AzureRmExpressRouteCrossConnectionPeering;
    - добавлена команда Remove-AzureRmExpressRouteCrossConnectionPeering;
    - добавлена команда Get-AzureRMExpressRouteCrossConnectionArpTable;
    - добавлена команда Get-AzureRMExpressRouteCrossConnectionRouteTable;
    - добавлена команда Get-AzureRMExpressRouteCrossConnectionRouteTableSummary.

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* Добавлен командлет Get-AzureRmRecoveryServicesBackupStatus. Этот командлет принимает идентификатор виртуальной машины и проверяет, защищена ли виртуальная машина с помощью какого-либо хранилища в подписке. Если такое хранилище существует, командлет выводит данные о нем.

#### <a name="azurermresources"></a>AzureRM.Resources
* Обновлены командлеты Get-AzureRmPolicyAssignment:
    - Добавлена поддержка вывода списка значений параметра -Scope на уровне группы управления.
    - Добавлена поддержка для получения отдельных назначений со значениями -Scope на уровне группы управления.
    - Для параметра управления добавлены параметры -Effective и -All.
* Обновлены командлеты Get/New/Remove/Set-AzureRmPolicyDefinition.
    - Добавлен параметр -ManagementGroupName для применения операций к заданной группе управления.
    - Добавлен параметр -SubscriptionId для применения операций к заданной подписке.
* Обновлены командлеты Get/New/Remove/Set-AzureRmPolicySetDefinition.
    - Добавлен параметр -ManagementGroupName для применения операций к заданной группе управления.
    - Добавлен параметр -SubscriptionId для применения операций к заданной подписке.
* Добавлена поддержка ссылок на секрет KeyVault в параметрах при использовании TemplateParameterObject в New-AzureRmResourceGroupDeployment.
* Устранена проблема, из-за которой параметр -EndDate игнорировался в New-AzureRmADAppCredential.
    - https://github.com/Azure/azure-powershell/issues/6505
* Устранена проблема, из-за которой в Add-AzureRmADGroupMember использовался неверный URL-адрес для запроса.
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Для командлета New-AzureRmServiceBusKey добавлен необязательный параметр -KeyValue, который позволяет пользователю предоставить значение ключа.

#### <a name="azurermsql"></a>AzureRM.Sql
* В справке по New-AzureRmSqlDatabaseRestorePoint добавлено описание определяемых пользователем точек восстановления для хранилища данных SQL.
* Обновлена документация по параметру -ComputeGeneration, используемого в нескольких командлетах.

## <a name="630---june-2018"></a>6.3.0 — июнь 2018 г.
#### <a name="azurermprofile"></a>AzureRM.Profile
* Обновлены сообщения об ошибках для Enable-AzureRmContextAutoSave.
* Создание контекста для каждой подписки при выполнении Connect-AzureRmAccount без предыдущего контекста.

#### <a name="azurestorage"></a>Azure.Storage;
* В файлы справки добавлены дополнительные сведения о параметре -Permissions.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Get-AzureRmVmDiskEncryptionStatus устраняет проблему, которая наблюдалась на виртуальных машинах без дисков данных. 
* Обновлена версия клиентской библиотеки Compute для исправления следующих командлетов:
    - Grant-AzureRmDiskAccess
    - Grant-AzureRmSnapshotAccess
    - Save-AzureRmVMImage
* В следующих командлетах исправлено отображение неправильных значений operation ID и operation status:
    - Start-AzureRmVM
    - Stop-AzureRmVM
    - Restart-AzureRmVM
    - Set-AzureRmVM
    - Remove-AzuerRmVM
    - Set-AzureRmVmss
    - Start-AzureRmVmssRollingOSUpgrade
    - Stop-AzureRmVmssRollingUpgrade
    - Start-AzureRmVmss
    - Restart-AzureRmVmss
    - Stop-AzureRmVmss
    - Remove-AzureRmVmss
    - ConvertTo-AzureRmVMManagedDisk
    - Revoke-AzureRmSnapshotAccess
    - Remove-AzureRmSnapshot
    - Revoke-AzureRmDiskAccess
    - Remove-AzureRmDisk
    - Remove-AzureRmContainerService
    - Remove-AzureRmAvailabilitySet

#### <a name="azurermeventgrid"></a>AzureRM.EventGrid
* Удалены условия проверки ValidateNotNullOrEmpty для SubjectBeginsWith/SubjectEndsWith в командлете Update-AzureRmEventGridSubscription, что позволяет при необходимости заменять эти параметры пустой строкой.

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Исправлена ошибка, когда при выполнении командлета Get-AzureRmKeyVault -Tag не возвращается ни один тег.

#### <a name="azurermpolicyinsights"></a>AzureRM.PolicyInsights
* Общедоступный выпуск командлетов Policy Insights.
    - Используется API версии 2018-04-04.
    - К результатам Get-AzureRmPolicyStateSummary добавлено PolicyDefinitionReferenceId.

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* Для командлетов RecoveryServices.Backup добавлен параметр -Vault. Передача этого параметра переопределяет командлет Set-AzureRmRecoveryServicesContext.

#### <a name="azurermsql"></a>AzureRM.Sql
* В файле справки обновлен пример для командлета Get-AzureRmSqlDatabaseExpanded.

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Обновлен файл справки для командлета Add-AzureRmTrafficManagerEndpointConfig.

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Изменено действие командлета Set-AzureRmWebApp. Теперь он не перезаписывает AppSettings, если используется параметр -AssignIdentity.
* Командлет New-AzureRmWebAppSlot теперь учитывает дополнительный параметр AppServicePlan.

## <a name="621---june-2018"></a>6.2.1 — июнь 2018 г.
### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights;
* В обновленной модели PSWorkspace Network может использовать type в качестве параметра.

## <a name="620---june-2018"></a>6.2.0 — июнь 2018 г.
#### <a name="azurermprofile"></a>AzureRM.Profile
* Исправлена ошибка с загрузкой Newtonsoft.Json версии 10.0.3 во время импорта модуля.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Функция обновления виртуальных машин VMSS.
    - Добавлены командлеты Update-AzureRmVmssVM и New-AzureRmVMDataDisk.
    - В командлет Add-AzureRmVMDataDisk добавлен параметр VirtualMachineScaleSetVM, который позволяет добавлять диски данных в виртуальные машины VMSS.

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Пакет SDK для ADF .NET обновлен до версии 0.8.0-preview. Новая версия содержит такие изменения:
    - добавлена операция для настройки репозитория фабрики;
    - связанная служба QuickBooks LinkedService теперь предоставляет свойства consumerKey и consumerSecret;
    - тип нескольких моделей изменен с SecretBase на Object;
    - добавлен триггер событий BLOB-объектов.

### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* В документацию добавлены примеры выходных данных.

### <a name="azurermnetwork"></a>AzureRM.Network
* В командлеты Наблюдателя за сетями добавлены параметры Аналитики трафика.

#### <a name="azurermresources"></a>AzureRM.Resources
* Исправлена ошибка, когда командлет Get-AzureRmResource возвращает свойство Properties объектов PSResource.

#### <a name="azurermscheduler"></a>AzureRM.Scheduler
* Исправлена ошибка, когда обновление ServiceBusQueueJob не задает новые значения для проверки подлинности.

### <a name="azurermsql"></a>AzureRM.Sql
* В перечисленные ниже командлеты добавлен необязательный параметр LicenseType.
    - New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase;
    - New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool;
    - New-AzureRmSqlDatabaseCopy
    - New-AzureRmSqlDatabaseSecondary
    - Restore-AzureRmSqlDatabase

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Командлет New-AzureRMWebApp теперь использует общие алгоритмы из библиотеки Strategy.

## <a name="610---may-2018"></a>6.1.0 — май 2018 г.
#### <a name="azurermprofile"></a>AzureRM.Profile
* Устранена проблема с выполнением Clear-AzureRmContext, при которой сохранялся пустой контекст с именем предыдущего контекста по умолчанию, что не позволяло пользователю создать новый контекст со старым именем.

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Включены операции связывания и отмены связи в автономной системе.

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Добавлена поддержка ApiVersions, ApiReleases и ApiRevisions.
* Добавлена поддержка серверной части ServiceFabric.
* Добавлена поддержка средства ведения журнала Application Insights.
* Добавлена поддержка для распознавания номера SKU уровня "Базовый" как допустимого номера SKU службы управления API.
* Добавлена поддержка установки сертификатов, выданных частным центром сертификации в качестве корневого или обычного ЦС.
* Добавлена поддержка для приема пользовательских SSL-сертификатов с помощью KeyVault и нескольких имен узлов прокси-сервера.
* Добавлена поддержка для удостоверения MSI.
* Добавлена поддержка для принятия политик с помощью URL-адреса. Примечание. Указанные ниже командлеты в следующей версии будут отмечены как нерекомендуемые.
   - Import-AzureRmApiManagementHostnameCertificate
   - New-AzureRmApiManagementHostnameConfiguration
   - Set-AzureRmApiManagementHostnames
   - Update-AzureRmApiManagementDeployment

#### <a name="azurermbatch"></a>AzureRM.Batch
* Выпущен новый командлет Get-AzureBatchPoolNodeCounts.
* Выпущен новый командлет Start-AzureBatchComputeNodeServiceLogUpload.

#### <a name="azurermconsumption"></a>AzureRM.Consumption:
* Добавлены новые параметры Expand, ResourceGroup, InstanceName, InstanceId, Tags и командлет высшего уровня Get-AzureRmConsumptionUsageDetail.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Исправлен пример для Export-AzureRmDataLakeStoreChildItemProperties.
* Исправлено исключение параметра NULL при использовании рекурсии в Set-AzureRmDataLakeStoreItemAclEntry. 
* Исправлены файлы справки для Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl и Remove-AzureRmDataLakeStoreItemAclEntry. 

#### <a name="azurermnetwork"></a>AzureRM.Network
* Пакет SDK для сети обновлен с предварительной версии 18.0.0 до предварительной версии 19.0.0.
* Добавлен командлет для создания конфигурации протокола.
    - New-AzureRmNetworkWatcherProtocolConfiguration.
* Добавлен командлет для добавления нового подключения канала к существующему каналу ExpressRoute.
    - Add-AzureRmExpressRouteCircuitConnectionConfig.
* Добавлен командлет для удаления подключения канала к существующему каналу ExpressRoute.
    - Remove-AzureRmExpressRouteCircuitConnectionConfig.
* Добавлен командлет для получения подключения канала.
    - Get-AzureRmExpressRouteCircuitConnectionConfig.

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Исправлена процедура аутентификации сервера с использованием созданных сертификатов (проблема № 5998).

#### <a name="azurermsql"></a>AzureRM.Sql
* Обновлены командлеты аудита, которые теперь позволяют удалять AuditActions или AuditActionGroups.
* Исправлена проблема с Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy, при которой установка новой гибкой политики хранения завершалась ошибкой с сообщением "Configure long term retention policy with azure recovery service vault and policy is no longer supported. Please submit request with the new flexible retention policy" (Настройка политики долгосрочного хранения с помощью хранилища и политики служб восстановления Azure больше не поддерживается. Отправьте запрос с использованием новой гибкой политики хранения).
* Обновлены все командлеты, связанные со службой "База данных SQL Azure", с созданием эластичных пулов и обновлением. Теперь используются новые API баз данных с поддержкой свойства номеров SKU для обеспечения масштабируемости и связанных с уровнями возможностей.
* Обновлены командлеты, в том числе: 
    - New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase;
    - New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool;
    - New-AzureRmSqlDatabaseCopy
    - New-AzureRmSqlDatabaseSecondary
    - Restore-AzureRmSqlDatabase

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Обновлены параметры для Get-AzureRmTrafficManagerProfile. Теперь при использовании параметра -Name требуется параметр -ResourceGroupName.
