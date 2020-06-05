---
title: Журнал изменений Azure PowerShell
description: Это руководство содержит историю изменений Azure PowerShell, внесенных в новом выпуске.
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 2/20/2018
ms.openlocfilehash: cf8d1fc76feb07e075339255de63e09f59187dc6
ms.sourcegitcommit: 9f5c7d231b069ad501729bf015a829f3fe89bc6a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/28/2020
ms.locfileid: "84122056"
---
# <a name="azure-powershell-release-notes"></a>Заметки о выпуске Azure PowerShell

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

Здесь приведен список изменений, внесенных в Azure PowerShell в этом выпуске.

---

## <a name="azure-powershell-570"></a>Azure PowerShell 5.7.0

Установщик Azure PowerShell 5.7.0: [ссылка](https://github.com/Azure/azure-powershell/releases/download/v5.7.0-April2018/azure-powershell.5.7.0.msi)

Модуль из коллекции для командлетов ARM: [ссылка](https://www.powershellgallery.com/packages/AzureRM/5.7.0).

Чтобы установить `AzureRM` из коллекции PowerShell, выполните такую команду:

```powershell-interactive
Install-Module -Name AzureRM -Repository PSGallery -Force
```

Чтобы обновить более старую версию `AzureRM`, выполните такую команду:

```powershell-interactive
Update-Module -Name AzureRM
```

### <a name="changes-since-last-release"></a>Изменения с момента последнего выпуска

#### <a name="general"></a>Общие сведения
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurestorage"></a>Azure.Storage;
* Устранена проблема, когда командлеты для отправки файлов и BLOB-объектов выдают ошибку на машинах с включенной политикой FIPS.
    - Set-AzureStorageBlobContent
    - Set-AzureStorageFileContent

#### <a name="azurermbilling"></a>AzureRM.Billing
* Добавлен новый командлет Get-AzureRmEnrollmentAccount.
  - Командлет для получения учетных записей регистрации.

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* Реализована интеграция с пакетом SDK для управления Cognitive Services версии 4.0.0.
* Добавлена операция Add Get-AzureRmCognitiveServicesAccountUsage.

#### <a name="azurermcompute"></a>AzureRM.Compute
* В `Get-AzureRmVmssDiskEncryptionStatus` добавлена поддержка состояния шифрования на уровне дисков данных.
* В `Get-AzureRmVmssVmDiskEncryptionStatus` добавлена поддержка состояния шифрования на уровне дисков данных.
* Обновлены функции отказоустойчивости в пределах зоны.
* В New-AzureRmVm и New-AzureRmVmss (простой набор параметров) добавлена поддержка зон доступности.

#### <a name="azurermcontainerregistry"></a>AzureRM.ContainerRegistry
* Исключена зависимость от Commands.Resources.Rest, а также пакетов SDK службы хранилища и ARM.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Добавлена функциональность отладки.
* Обновлен пакет SDK для плоскости данных ADLS до версии 1.1.2.
* В Export-AzureRmDataLakeStoreItem параметры PerFileThreadCount и ConcurrentFileCount объявлены нерекомендуемыми, а также добавлен новый параметр Concurrency.
* В Import-AzureRMDataLakeStoreItem параметры PerFileThreadCount и ConcurrentFileCount объявлены нерекомендуемыми, а также добавлен новый параметр Concurrency.
* В Get-AzureRMDataLakeStoreItemContent исправлено поведение заключительного фрагмента содержимого, размер которого превышает 4 МБ.
* В Set-AzureRMDataLakeStoreItemExpiry добавлен новый набор параметров SetRelativeExpiry для настройки относительного времени истечения срока действия.
* В Remove-AzureRmDataLakeStoreItem параметр Clean объявлен нерекомендуемым.

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* В AzureRmEventHubGeoDRConfiguration исправлен параметр AlternameName.

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Обновлены командлеты для поддержки конвейерного режима.
* Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.

#### <a name="azurermnetwork"></a>AzureRM.Network
* Исправлены сообщения об ошибках для сетевых командлетов.

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* В фильтр CorrelationFilter командлета Rules добавлен параметр properties для поддержки настраиваемых свойств.
* Обновлена справка по New-AzureRmServiceBusGeoDRConfiguration и исправлены выходные данные командлета Rules.
* Исправлены свойства автоматической пересылки в командлетах New-AzureRmServiceBusQueue и New-AzureRmServiceBusSubscription.

#### <a name="azurermsql"></a>AzureRM.Sql
* Добавлен новый командлет Stop-AzureRmSqlElasticPoolActivity для поддержки отмены асинхронных операций в эластичном пуле.
* Добавлена дополнительная информация в ответ командлетов Get-AzureRmSqlDatabaseActivity и Get-AzureRmSqlElasticPoolActivity.

Изменения с момента последнего выпуска: https://github.com/Azure/azure-powershell/compare/v5.6.0-March2018...v5.7.0-April2018

## <a name="560---march-2018"></a>5.6.0 — март 2018 г.

#### <a name="general"></a>Общие сведения
* Исправлена проблема с группой ресурсов по умолчанию в CloudShell.
* Исправлена проблема с выполнением неправильных скриптов запуска во время импорта модуля.

#### <a name="azurermprofile"></a>AzureRM.Profile
* Включена аутентификация MSI в неподдерживаемых сценариях.
* Добавлена поддержка определяемого пользователем управляемого удостоверения службы.

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Исправлена проблема с очисткой скриптов в сборке.

#### <a name="azurermcdn"></a>AzureRM.Cdn
* Исправлена проблема с очисткой скриптов в сборке.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Поддержка дисков данных командлетами New-AzureRmVM и New-AzureRmVMSS.
* Поддержка пользовательских образов по имени или идентификатору командлетами New-AzureRmVM и New-AzureRmVMSS.
* Функция аналитики журналов
    - Добавлен командлет Export-AzureRmLogAnalyticRequestRateByInterval.
    - Добавлен командлет Export-AzureRmLogAnalyticThrottledRequests.

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* Исправлена проблема с наборами параметров для реестра контейнеров и подключением тома службы файлов Azure.

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Обновлен пакет .Net SDK для ADF до версии 0.6.0-preview, содержащий следующие изменения:
    - Добавлены новые действия AzureDatabricks LinkedService и DatabricksNotebook.
    - Добавлены свойства headNodeSize и dataNodeSize в HDInsightOnDemand LinkedService.
    - Добавлено LinkedService, Dataset, CopySource для SalesforceMarketingCloud.
    - Добавлена поддержка SecureOutput для всех действий.
    - Добавлено новое свойство BatchCount для действия ForEach, которое определяет количество одновременных действий для выполнения.
    - Добавлено новое действие фильтра.
    - Добавлена поддержка параметров связанной службы.

#### <a name="azurermdns"></a>AzureRM.Dns
* Добавлена поддержка Частной зоны DNS (общедоступная предварительная версия).
    - Добавлена возможность создания зон DNS, которые видны только для связанных виртуальных сетей.

#### <a name="azurermnetwork"></a>AzureRM.Network
* Обновлены типы моделей для обеспечения совместимости с командлетами DNS.

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* Добавлены изменения Azure ASR для Azure Site Recovery (командлеты, которые сейчас поддерживают операции Enterprise — Enterprise, Enterprise — Azure, HyperV — Azure, VMware — Azure).
    - New-AzureRmRecoveryServicesAsrProtectionContainer
    - New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig
    - Remove-AzureRmRecoveryServicesAsrProtectionContainer
    - Update-AzureRmRecoveryServicesAsrProtectionDirection

#### <a name="azurermstorage"></a>AzureRM.Storage
* Прекращено использование параметров EnableEncryptionService и DisableEncryptionService для командлетов учетной записи хранения New- и Set-, так как по умолчанию включено кэшрование неактивных данных без возможности отключения.
    - New-AzureRmStorageAccount;
    - Set-AzureRmStorageAccount.

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Исправлена справка по командлету Remove-AzureRmWebAppSlot.

## <a name="550---march-2018"></a>5.5.0 — март 2018 г.
#### <a name="azurermprofile"></a>AzureRM.Profile
* Устранена проблема с импортом псевдонимов.
* Загрузка версии Newtonsoft.Json 10.0.3 параллельно с версией 6.0.8.

#### <a name="azurestorage"></a>Azure.Storage;
* Поддержка функции обратимого удаления:
    - Enable-AzureStorageDeleteRetentionPolicy
    - Disable-AzureStorageDeleteRetentionPolicy
    - Get-AzureStorageBlob

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Устранена проблема с импортом псевдонимов.
* Добавлена поддержка брандмауэра и функции запросов с масштабированием, а также поддержка API версии 2017-08-01.

#### <a name="azurermautomation"></a>AzureRM.Automation
* Устранена проблема с импортом псевдонимов.

#### <a name="azurermcdn"></a>AzureRM.Cdn
* Устранена проблема с импортом псевдонимов.

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* Обновлен файл notice.txt и текст уведомления.

#### <a name="azurermcompute"></a>AzureRM.Compute
* New-AzureRmVMSS отображает строки подключения в режиме подробного протоколирования.
* New-AzureRmVmss поддерживает общедоступные IP-адреса, правила балансировки нагрузки и правила NAT для входящего трафика.
* Функция WriteAccelerator:
    - В следующие командлеты добавлен новый параметр-переключатель WriteAccelerator: Set-AzureRmVMOSDisk, Set-AzureRmVMDataDisk, Add-AzureRmVMDataDisk  и Add-AzureRmVmssDataDisk.
    - В следующий командлет добавлен новый параметр-переключатель OsDiskWriteAccelerator:     Set-AzureRmVmssStorageProfile.
    - В следующие командлеты добавлен новый логический параметр OsDiskWriteAccelerator:     Update-AzureRmVM и Update-AzureRmVmss.

#### <a name="azurermdatafactories"></a>AzureRM.DataFactories
* Устранена проблема с шифрованием учетных данных, при которой происходила ошибка некоторых операций шифрования.
* Обеспечен общий доступ к среде выполнения интеграции в фабрике данных.

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* В команду Set-AzureRmDataFactoryV2IntegrationRuntime добавлены параметры SetupScriptContainerSasUri и Edition для включения функций выборочной установки и выбора выпусков.
* Устранена проблема с шифрованием учетных данных, при которой происходила ошибка некоторых операций шифрования.
* Обеспечен общий доступ к среде выполнения интеграции в фабрике данных.

#### <a name="azurermhdinsight"></a>AzureRM.HDInsight
* Устранена проблема с импортом псевдонимов.

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Исправлен пример для Set-AzureRmKeyVaultAccessPolicy.

#### <a name="azurermnetwork"></a>AzureRM.Network
* Устранена проблема с импортом псевдонимов.

#### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights;
* Устранена проблема с импортом псевдонимов.

#### <a name="azurermrecoveryservices"></a>AzureRM.RecoveryServices
* Устранена проблема с импортом псевдонимов.

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* Устранена проблема с импортом псевдонимов.

#### <a name="azurermresources"></a>AzureRM.Resources
* Устранена проблема с импортом псевдонимов.

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Для очереди добавлено свойство EnableBatchedOperations.
* Для подписок добавлено свойство DeadLetteringOnFilterEvaluationExceptions.

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Обновлен командлет Service Fabric:
  - обновлены шаблоны ARM;
  - для операций со сбоем больше не выполняется откат;
  - Add-AzureRmServiceFabricNodeType;
    - для виртуальных машин по умолчанию используются управляемые диски;
    - используется существующая подсеть VMSS;
    - все операции являются идемпотентными;
  - Remove-AzureRmServiceFabricNodeType удаляет частично созданные масштабируемые наборы виртуальных машин и (или) типы узлов кластеров;
  - исправлены выходные данные объекта PSCluster для сложных типов свойств.

#### <a name="azurermsql"></a>AzureRM.Sql
* Устранена проблема с импортом псевдонимов.
* Ответ Get-AzureRmSqlServer, New-AzureRmSqlServer и Remove-AzureRmSqlServer теперь содержит свойство FullyQualifiedDomainName.

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Устранена проблема с импортом псевдонимов.
* В New-AzureRMWebApp добавлен набор параметров, упрощающих создание веб-приложений, с поддержкой локального репозитория Git.

## <a name="540---february-2018"></a>5.4.0 — февраль 2018 г.
#### <a name="azurermautomation"></a>AzureRM.Automation
* Добавлен псевдоним из New-AzureRmAutomationModule в Import-AzureRmAutomationModule.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Исправлена ошибка ErrorAction для некоторых командлетов Get.

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* Применен пакет SDK 2018-02-01 для службы "Экземпляры контейнеров Azure".
    - Добавлена поддержка метки имени DNS.

#### <a name="azurermdevtestlabs"></a>AzureRM.DevTestLabs
* Исправлены все командлеты GET, который ранее не работали.

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Исправлена ошибка в справочных сведениях о Get-AzureRmEventHubGeoDRConfiguration.

#### <a name="azurermnetwork"></a>AzureRM.Network
* Добавлен командлет для создания монитора подключения.
    - New-AzureRmNetworkWatcherConnectionMonitor
* Добавлен командлет для обновления монитора подключения.
    - Set-AzureRmNetworkWatcherConnectionMonitor
* Добавлен командлет для получения монитора подключения или списка мониторов подключения.
    - Get-AzureRmNetworkWatcherConnectionMonitor
* Добавлен командлет для выполнения запроса к монитору подключения.
    - Get-AzureRmNetworkWatcherConnectionMonitorReport
* Добавлен командлет для запуска монитора подключения.
    - Start-AzureRmNetworkWatcherConnectionMonitor
* Добавлен командлет для остановки монитора подключения.
    - Stop-AzureRmNetworkWatcherConnectionMonitor
* Добавлен командлет для удаления монитора подключения.
    - Remove-AzureRmNetworkWatcherConnectionMonitor
* Обновлена документация AzureRmApplicationGatewayBackendAddressPool для удаления устаревшего примера.
* Добавлен флаг EnableHttp2 для шлюза приложений.
    - Обновлен командлет New-AzureRmApplicationGateway: добавлен необязательный параметр -EnableHttp2.
* Добавлены теги IpTag для PublicIpAddress.
    - Обновлен командлет New-AzureRmPublicIpAddress: добавлен параметр IpTags.
    - Добавлены теги IpTag для New-AzureRmPublicIpTag.
* Добавлено свойство DisableBgpRoutePropagation в RouteTable и effectiveRoute.

#### <a name="azurermresources"></a>AzureRM.Resources
* Register-AzureRmProviderFeature: в документацию добавлен отсутствовавший пример.
* Register-AzureRmResourceProvider: в документацию добавлен отсутствовавший пример.

#### <a name="azurermstorage"></a>AzureRM.Storage
* Прекращено использование параметров EnableEncryptionService и DisableEncryptionService для командлетов учетной записи хранения New- и Set-, так как по умолчанию включено кэшрование неактивных данных без возможности отключения.
    - New-AzureRmStorageAccount;
    - Set-AzureRmStorageAccount.


## <a name="530---february-2018"></a>5.3.0 — февраль 2018 г.
### <a name="azurermprofile"></a>AzureRM.Profile
* Добавлено предупреждение о прекращении поддержки для PowerShell версий 3 и 4.
* Команда `Add-AzureRmAccount` переименована на `Connect-AzureRmAccount`; добавлен псевдоним для старого имени командлета, а другие псевдонимы (`Login-AzAccount` и `Login-AzureRmAccount`) могут ссылаться на новое имя командлета.
* Команда `Remove-AzureRmAccount` переименована на `Disconnect-AzureRmAccount`; добавлен псевдоним для старого имени командлета, а другие псевдонимы (`Logout-AzAccount` и `Logout-AzureRmAccount`) могут ссылаться на новое имя командлета.
* Исправлены строки ресурса для использования `Connect-AzureRmAccount` вместо `Login-AzureRmAccount`.
* `Add-AzureRmEnvironment` и `Set-AzureRmEnvironment`
  - Добавлены `-AzureOperationalInsightsEndpoint` и `-AzureOperationalInsightsEndpointResourceId` как параметры для использования с плоскостью данных OperationalInsights (RP).

### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Исправлена возможность использования `Login-AzureRmAccount` для использования `Connect-AzureRmAccount`.

### <a name="azurermcompute"></a>AzureRM.Compute
* Добавлен параметр `-AvailabilitySetName` к упрощенному набору параметров `New-AzureRmVM`.
* Исправлена возможность использования `Login-AzureRmAccount` для использования `Connect-AzureRmAccount`.
* Поддержка пользовательских удостоверений для виртуальных машин и масштабируемых наборов виртуальных машин.
    - Добавлены параметры `-IdentityType` и `-IdentityId` к `New-AzureRmVMConfig`, `New-AzureRmVmssConfig`, `Update-AzureRmVM` и `Update-AzureRmVmss`
* Добавлен параметр `-EnableIPForwarding` для команды `Add-AzureRmVmssNetworkInterfaceConfig`.
* Добавлен параметр `-Priority` для команды `New-AzureRmVmssConfig`.

### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* Исправлена возможность использования `Login-AzureRmAccount` для использования `Connect-AzureRmAccount`.

### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Исправлена возможность использования `Login-AzureRmAccount` для использования `Connect-AzureRmAccount`.
* Исправлено сообщение об ошибке `Test-AzureRmDataLakeStoreAccount` при выполнении этого командлета, без выполнения входа с помощью `Login-AzureRmAccount`.

### <a name="azurermeventgrid"></a>AzureRM.EventGrid
* Обновлено для использования API версии 2018-01-01.

### <a name="azurermeventhub"></a>AzureRM.EventHub

* Добавлены следующие новые команды для операций аварийного восстановления с георепликацией:
  - Создание псевдонима (конфигурация аварийного восстановления):
    - `New-AzureRmEventHubGeoDRConfiguration`
  - Получение псевдонима (конфигурация аварийного восстановления):
    - `Get-AzureRmEventHubGeoDRConfiguration`
  - Отключение аварийного восстановления и остановка репликации изменений из основного пространства имен в дополнительное.
    - `Set-AzureRmEventHubGeoDRConfigurationBreakPair`
  - Вызов отработки аварийного восстановления и перенастройка псевдонима пространства имен для указания на дополнительное пространство.
    - `Set-AzureRmEventHubGeoDRConfigurationFailOver`
  - Удаление псевдонима (конфигурация аварийного восстановления).
    - `Remove-AzureRmEventHubGeoDRConfiguration`
* Добавлены следующие новые команды для проверки имени пространства имен и имени конфигурации аварийного восстановления с георепликацией (доступность псевдонима):
  - Проверка доступности псевдонима или имени пространства имен (конфигурация аварийного восстановления):
    - `Test-AzureRmEventHubName`

### <a name="azurerminsights"></a>AzureRM.Insights;
* Исправлена возможность использования `Login-AzureRmAccount` для использования `Connect-AzureRmAccount`.

### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Исправлена возможность использования `Login-AzureRmAccount` для использования `Connect-AzureRmAccount`.

### <a name="azurermnetwork"></a>AzureRM.Network
* Исправлено сообщение о перезаписи: "Вы действительно хотите перезаписать ресурс?".

#### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights;
* Добавлена поддержка запросов API версии 2 с помощью `Invoke-AzureRmOperationalInsightsQuery`. Дополнительные сведение о новом API-интерфейсе см. здесь: [https://dev.loganalytics.io/](https://dev.loganalytics.io/).

### <a name="azurermresources"></a>AzureRM.Resources
* `Get-AzureRmADServicePrincipal`: из пустого набора параметров по умолчанию удален параметр `-ServicePrincipalName` из-за наличия набора параметров имени субъекта-службы.

### <a name="azurermservicebus"></a>AzureRM.ServiceBus

* Добавлено исправление для `Remove-AzureRmServiceBusRule` и `Get-AzureRmServiceBusKey`.
* Добавлены следующие новые командлеты для операций аварийного восстановления с георепликацией:
  - Создание псевдонима (конфигурация аварийного восстановления):
    - `New-AzureRmServiceBusDRConfigurations`
  - Получение псевдонима (конфигурация аварийного восстановления):
    - `Get-AzureRmServiceBusDRConfigurations`
  - Отключение аварийного восстановления и остановка репликации изменений из основного пространства имен в дополнительное.
    - `Set-AzureRmServiceBusDRConfigurationsBreakPairing`
  - Вызов отработки аварийного восстановления и перенастройка псевдонима пространства имен для указания на дополнительное пространство.
    - `Set-AzureRmServiceBusDRConfigurationsFailOver`
  - Удаление псевдонима (конфигурация аварийного восстановления).
    - `Remove-AzureRmServiceBusDRConfigurations`
* Обновлены командлеты `Test-AzureRmServiceBusName` для поддержки аварийного восстановления с георепликацией (операции проверки доступности имени псевдонима):
  - Проверка доступности псевдонима или имени пространства имен (конфигурация аварийного восстановления):
    - `Test-AzureRmServiceBusName`

### <a name="azurermusageaggregates"></a>AzureRM.UsageAggregates
* Исправлена возможность использования `Login-AzureRmAccount` для использования `Connect-AzureRmAccount`.

## <a name="520---january-2018"></a>5.2.0 — январь 2018 г.
#### <a name="azurermprofile"></a>AzureRM.Profile
* Добавлено средство заполнения групп ресурсов для параметров -ResourceGroup, которое включает заполнение нажатием клавиши TAB в группах ресурсов в текущей подписке.
* Add-AzureRmAccount
  * Добавлено имя входа -MSI для аутентификации с использованием учетных данных удостоверения управляемой службы текущей виртуальной машины или службы.
  * Исправлена аутентификация Key Vault при входе в систему с маркерами доступа, предоставленными пользователем.

#### <a name="azurestorage"></a>Azure.Storage;
* Добавлены командлеты для получения и настройки свойств службы хранилища.
    - Get-AzureStorageServiceProperty
    - Update-AzureStorageServiceProperty

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Добавлено средство заполнения групп ресурсов для параметров -ResourceGroup, которое включает заполнение нажатием клавиши TAB в группах ресурсов в текущей подписке.

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Добавлено средство заполнения расположения для параметров -Location, которое включает заполнение нажатием клавиши TAB в допустимых расположениях.
* Добавлено средство заполнения групп ресурсов для параметров -ResourceGroup, которое включает заполнение нажатием клавиши TAB в группах ресурсов в текущей подписке.
* Параметр -Tags заменен параметром -Tag для командлетов New-AzureRmApiManagementProperty, Set-AzureRmApiManagementProperty и New-AzureRmApiManagement.

#### <a name="azurermapplicationinsights"></a>AzureRM.ApplicationInsights
* Добавлено средство заполнения расположения для параметров -Location, которое включает заполнение нажатием клавиши TAB в допустимых расположениях.
* Добавлено средство заполнения групп ресурсов для параметров -ResourceGroup, которое включает заполнение нажатием клавиши TAB в группах ресурсов в текущей подписке.

#### <a name="azurermautomation"></a>AzureRM.Automation
* Добавлено средство заполнения расположения для параметров -Location, которое включает заполнение нажатием клавиши TAB в допустимых расположениях.
* Добавлено средство заполнения групп ресурсов для параметров -ResourceGroup, которое включает заполнение нажатием клавиши TAB в группах ресурсов в текущей подписке.
* Параметр -Tags заменен параметром -Tag для командлета Set-AzureRmAutomationRunbook.

#### <a name="azurermbackup"></a>AzureRM.Backup
* Добавлено средство заполнения расположения для параметров -Location, которое включает заполнение нажатием клавиши TAB в допустимых расположениях.
* Добавлено средство заполнения групп ресурсов для параметров -ResourceGroup, которое включает заполнение нажатием клавиши TAB в группах ресурсов в текущей подписке.

#### <a name="azurermbatch"></a>AzureRM.Batch
* Добавлено средство заполнения расположения для параметров -Location, которое включает заполнение нажатием клавиши TAB в допустимых расположениях.
* Добавлено средство заполнения групп ресурсов для параметров -ResourceGroup, которое включает заполнение нажатием клавиши TAB в группах ресурсов в текущей подписке.

#### <a name="azurermcdn"></a>AzureRM.Cdn
* Добавлено средство заполнения расположения для параметров -Location, которое включает заполнение нажатием клавиши TAB в допустимых расположениях.
* Добавлено средство заполнения групп ресурсов для параметров -ResourceGroup, которое включает заполнение нажатием клавиши TAB в группах ресурсов в текущей подписке.
* Параметр -Tags заменен параметром -Tag для командлетов New-AzureRmCdnEndpoint и New-AzureRmCdnProfile

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* Реализована интеграция с пакетом SDK для управления Cognitive Services версии 3.0.0.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Добавлен упрощенный набор параметров для командлета New-AzureRmVmss, который создает масштабируемый набор виртуальных машин и все необходимые ресурсы с помощью стандартных интеллектуальных значений.
* Добавлено средство заполнения расположения для параметров -Location, которое включает заполнение нажатием клавиши TAB в допустимых расположениях.
* Добавлено средство заполнения групп ресурсов для параметров -ResourceGroup, которое включает заполнение нажатием клавиши TAB в группах ресурсов в текущей подписке.
* Параметр -Tags заменен параметром -Tag для командлетов New-AzureRmVm и Update-AzureRmVm.
* Исправлен командлет Get-AzureRmComputeResourceSku при включении зоны в ограничение.
* Обновлена схема конфигурации агента диагностики для поддержки приемника Azure Monitor.

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* Добавлено средство заполнения расположения для параметров -Location, которое включает заполнение нажатием клавиши TAB в допустимых расположениях.
* Добавлено средство заполнения групп ресурсов для параметров -ResourceGroup, которое включает заполнение нажатием клавиши TAB в группах ресурсов в текущей подписке.

#### <a name="azurermcontainerregistry"></a>AzureRM.ContainerRegistry
* Добавлено средство заполнения расположения для параметров -Location, которое включает заполнение нажатием клавиши TAB в допустимых расположениях.
* Добавлено средство заполнения групп ресурсов для параметров -ResourceGroup, которое включает заполнение нажатием клавиши TAB в группах ресурсов в текущей подписке.

#### <a name="azurermdatafactories"></a>AzureRM.DataFactories
* Включена поддержка Azure Key Vault для всех связанных служб хранилищ данных.
* Добавлено свойство типа лицензии для среды выполнения интеграции Integration Services Azure.
* Добавлено средство заполнения расположения для параметров -Location, которое включает заполнение нажатием клавиши TAB в допустимых расположениях.
* Добавлено средство заполнения групп ресурсов для параметров -ResourceGroup, которое включает заполнение нажатием клавиши TAB в группах ресурсов в текущей подписке.
* Параметр -Tags заменен параметром -Tag для командлета New-AzureRmDataFactory.

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Включена поддержка Azure Key Vault для всех связанных служб хранилищ данных.
* Добавлено свойство типа лицензии для среды выполнения интеграции Integration Services Azure.
* Добавлено средство заполнения расположения для параметров -Location, которое включает заполнение нажатием клавиши TAB в допустимых расположениях.
* Добавлено средство заполнения групп ресурсов для параметров -ResourceGroup, которое включает заполнение нажатием клавиши TAB в группах ресурсов в текущей подписке.
* Добавлен параметр типа лицензии для командлета Set-AzureRmDataFactoryV2IntegrationRuntime для включения функций AHUB.

#### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* Добавлено средство заполнения расположения для параметров -Location, которое включает заполнение нажатием клавиши TAB в допустимых расположениях.
* Добавлено средство заполнения групп ресурсов для параметров -ResourceGroup, которое включает заполнение нажатием клавиши TAB в группах ресурсов в текущей подписке.
* Параметр -Tags заменен параметром -Tag для командлетов New-AzureRmDataLakeAnalyticsAccount и Set-AzureRmDataLakeAnalyticsAccount.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Добавлено средство заполнения расположения для параметров -Location, которое включает заполнение нажатием клавиши TAB в допустимых расположениях.
* Добавлено средство заполнения групп ресурсов для параметров -ResourceGroup, которое включает заполнение нажатием клавиши TAB в группах ресурсов в текущей подписке.
* Параметр -Tags заменен параметром -Tag для командлетов New-AzureRmDataLakeStoreAccount и Set-AzureRmDataLakeStoreAccount.

#### <a name="azurermdevtestlabs"></a>AzureRM.DevTestLabs
* Добавлено средство заполнения групп ресурсов для параметров -ResourceGroup, которое включает заполнение нажатием клавиши TAB в группах ресурсов в текущей подписке.

#### <a name="azurermdns"></a>AzureRM.Dns
* Добавлено средство заполнения групп ресурсов для параметров -ResourceGroup, которое включает заполнение нажатием клавиши TAB в группах ресурсов в текущей подписке.

#### <a name="azurermeventgrid"></a>AzureRM.EventGrid
* Добавлены следующие новые командлеты:
  - Update-AzureRmEventGridSubscription
    - Обновлены свойства подписки на события Сетки событий.
* Добавлено средство заполнения расположения для параметров -Location, которое включает заполнение нажатием клавиши TAB в допустимых расположениях.
* Добавлено средство заполнения групп ресурсов для параметров -ResourceGroup, которое включает заполнение нажатием клавиши TAB в группах ресурсов в текущей подписке.

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Добавлено средство заполнения расположения для параметров -Location, которое включает заполнение нажатием клавиши TAB в допустимых расположениях.
* Добавлено средство заполнения групп ресурсов для параметров -ResourceGroup, которое включает заполнение нажатием клавиши TAB в группах ресурсов в текущей подписке.

#### <a name="azurermhdinsight"></a>AzureRM.HDInsight
* Добавлено средство заполнения расположения для параметров -Location, которое включает заполнение нажатием клавиши TAB в допустимых расположениях.
* Добавлено средство заполнения групп ресурсов для параметров -ResourceGroup, которое включает заполнение нажатием клавиши TAB в группах ресурсов в текущей подписке.

#### <a name="azurerminsights"></a>AzureRM.Insights;
* Добавлено средство заполнения расположения для параметров -Location, которое включает заполнение нажатием клавиши TAB в допустимых расположениях.
* Добавлено средство заполнения групп ресурсов для параметров -ResourceGroup, которое включает заполнение нажатием клавиши TAB в группах ресурсов в текущей подписке.

#### <a name="azurermiothub"></a>AzureRM.IotHub
* Добавлена поддержка сертификатов для командлетов Центра Интернета вещей.
* Добавлено средство заполнения расположения для параметров -Location, которое включает заполнение нажатием клавиши TAB в допустимых расположениях.
* Добавлено средство заполнения групп ресурсов для параметров -ResourceGroup, которое включает заполнение нажатием клавиши TAB в группах ресурсов в текущей подписке.

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Добавлено средство заполнения расположения для параметров -Location, которое включает заполнение нажатием клавиши TAB в допустимых расположениях.
* Добавлено средство заполнения групп ресурсов для параметров -ResourceGroup, которое включает заполнение нажатием клавиши TAB в группах ресурсов в текущей подписке.
* Добавлена поддержка параметра -AsJob для долго выполняющихся командлетов KeyVault. Благодаря этому выбранные командлеты могут выполняться в фоновом режиме и возвращать задание для отслеживания и контроля хода выполнения.
  * Это касается командлета Remove-AzureRmKeyVault
* Исправлена ошибка в командлете Set-AzureRmKeyVaultAccessPolicy, когда фильтр AAD настраивал в качестве имени субъекта-службы предоставляемое имя участника-пользователя вместо настройки имени участника-пользователя.
  - Дополнительные сведения о проблеме см. здесь: https://github.com/Azure/azure-powershell/issues/5201.

#### <a name="azurermlogicapp"></a>AzureRM.LogicApp
* Добавлено средство заполнения расположения для параметров -Location, которое включает заполнение нажатием клавиши TAB в допустимых расположениях.
* Добавлено средство заполнения групп ресурсов для параметров -ResourceGroup, которое включает заполнение нажатием клавиши TAB в группах ресурсов в текущей подписке.

#### <a name="azurermmachinelearning"></a>AzureRM.MachineLearning
* Добавлено средство заполнения расположения для параметров -Location, которое включает заполнение нажатием клавиши TAB в допустимых расположениях.
* Добавлено средство заполнения групп ресурсов для параметров -ResourceGroup, которое включает заполнение нажатием клавиши TAB в группах ресурсов в текущей подписке.
* Параметр -Tags заменен параметром -Tag для командлета Update-AzureRmMlCommitmentPlan.

#### <a name="azurermmachinelearningcompute"></a>AzureRM.MachineLearningCompute
* Добавлен параметр IncludeAllResources для командлета Remove-AzureRmMlOpCluster.
  - Использование этого параметра приводит к удалению всех ресурсов, которые были созданы с помощью кластера.
* Добавлено средство заполнения расположения для параметров -Location, которое включает заполнение нажатием клавиши TAB в допустимых расположениях.
* Добавлено средство заполнения групп ресурсов для параметров -ResourceGroup, которое включает заполнение нажатием клавиши TAB в группах ресурсов в текущей подписке.

#### <a name="azurermmedia"></a>AzureRM.Media
* Добавлено средство заполнения расположения для параметров -Location, которое включает заполнение нажатием клавиши TAB в допустимых расположениях.
* Добавлено средство заполнения групп ресурсов для параметров -ResourceGroup, которое включает заполнение нажатием клавиши TAB в группах ресурсов в текущей подписке.
* Параметр -Tags заменен параметром -Tag для командлетов Set-AzureRmMediaService и New-AzureRmMediaService.

#### <a name="azurermnetwork"></a>AzureRM.Network
* Добавлена поддержка параметра -AsJob в долго выполняющихся командлетах Network. Благодаря этому выбранные командлеты могут выполняться в фоновом режиме и возвращать задание для отслеживания и контроля хода выполнения.
* Добавлено средство заполнения расположения для параметров -Location, которое включает заполнение нажатием клавиши TAB в допустимых расположениях.
* Добавлено средство заполнения групп ресурсов для параметров -ResourceGroup, которое включает заполнение нажатием клавиши TAB в группах ресурсов в текущей подписке.

#### <a name="azurermnotificationhubs"></a>AzureRM.NotificationHubs
* Добавлено средство заполнения расположения для параметров -Location, которое включает заполнение нажатием клавиши TAB в допустимых расположениях.
* Добавлено средство заполнения групп ресурсов для параметров -ResourceGroup, которое включает заполнение нажатием клавиши TAB в группах ресурсов в текущей подписке.
* Параметр -Tags заменен параметром -Tag для командлетов New-AzureRmNotificationHubsNamespace и Set-AzureRmNotificationHubsNamespace.

#### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights;
* Добавлено средство заполнения расположения для параметров -Location, которое включает заполнение нажатием клавиши TAB в допустимых расположениях.
* Добавлено средство заполнения групп ресурсов для параметров -ResourceGroup, которое включает заполнение нажатием клавиши TAB в группах ресурсов в текущей подписке.
* Параметр -Tags заменен параметром -Tag для командлетов New-AzureRmOperationalInsightsSavedSearch, Set-AzureRmOperationalInsightsSavedSearch, New-AzureRmOperationalInsightsWorkspace и Set-AzureRmOperationalInsightsWorkspace.

#### <a name="azurermpowerbiembedded"></a>AzureRM.PowerBIEmbedded
* Добавлено средство заполнения расположения для параметров -Location, которое включает заполнение нажатием клавиши TAB в допустимых расположениях.
* Добавлено средство заполнения групп ресурсов для параметров -ResourceGroup, которое включает заполнение нажатием клавиши TAB в группах ресурсов в текущей подписке.

#### <a name="azurermrecoveryservices"></a>AzureRM.RecoveryServices
* Добавлено средство заполнения расположения для параметров -Location, которое включает заполнение нажатием клавиши TAB в допустимых расположениях.
* Добавлено средство заполнения групп ресурсов для параметров -ResourceGroup, которое включает заполнение нажатием клавиши TAB в группах ресурсов в текущей подписке.

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* Добавлено средство заполнения групп ресурсов для параметров -ResourceGroup, которое включает заполнение нажатием клавиши TAB в группах ресурсов в текущей подписке.
* Добавлен параметр -UseOriginalStorageAccount для командлета Restore-AzureRmRecoveryServicesBackupItem.
  - Включение этого флажка приводит к восстановлению дисков в их исходных учетных записях хранения, что позволяет пользователям хранить конфигурацию восстановленной виртуальной машины как можно более сходной с исходной виртуальной машиной.
  - Он также помогает повысить производительность операции восстановления.

#### <a name="azurermrediscache"></a>AzureRM.RedisCache
* Добавлено средство заполнения расположения для параметров -Location, которое включает заполнение нажатием клавиши TAB в допустимых расположениях.
* Добавлено средство заполнения групп ресурсов для параметров -ResourceGroup, которое включает заполнение нажатием клавиши TAB в группах ресурсов в текущей подписке.
* Добавлено три новых командлета для правил брандмауэра.
* Добавлено три новых командлета для георепликации.
* Добавлена поддержка зон и тегов.
* Использование группы ресурсов как необязательной по возможности.

#### <a name="azurermrelay"></a>AzureRM.Relay
* Добавлено средство заполнения расположения для параметров -Location, которое включает заполнение нажатием клавиши TAB в допустимых расположениях.
* Добавлено средство заполнения групп ресурсов для параметров -ResourceGroup, которое включает заполнение нажатием клавиши TAB в группах ресурсов в текущей подписке.

#### <a name="azurermresources"></a>AzureRM.Resources
* Добавлено средство заполнения расположения для параметров -Location, которое включает заполнение нажатием клавиши TAB в допустимых расположениях.
* Добавлено средство заполнения групп ресурсов для параметров -ResourceGroup, которое включает заполнение нажатием клавиши TAB в группах ресурсов в текущей подписке.
* Добавлена поддержка параметра -AsJob для долго выполняющихся командлетов Resources. Благодаря этому выбранные командлеты могут выполняться в фоновом режиме и возвращать задание для отслеживания и контроля хода выполнения.
* Добавлен псевдоним из командлета Get-AzureRmProviderOperation в командлет Get-AzureRmResourceProviderAction для обеспечения соответствия с соглашением об именовании.

#### <a name="azurermscheduler"></a>AzureRM.Scheduler
* Добавлено средство заполнения расположения для параметров -Location, которое включает заполнение нажатием клавиши TAB в допустимых расположениях.
* Добавлено средство заполнения групп ресурсов для параметров -ResourceGroup, которое включает заполнение нажатием клавиши TAB в группах ресурсов в текущей подписке.

#### <a name="azurermservermanagement"></a>AzureRM.ServerManagement
* Добавлено средство заполнения расположения для параметров -Location, которое включает заполнение нажатием клавиши TAB в допустимых расположениях.
* Добавлено средство заполнения групп ресурсов для параметров -ResourceGroup, которое включает заполнение нажатием клавиши TAB в группах ресурсов в текущей подписке.
* Параметр -Tags заменен параметром -Tag для командлетов New-AzureRmServerManagementNode и New-AzureRmServerManagementGateway.

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Добавлено средство заполнения расположения для параметров -Location, которое включает заполнение нажатием клавиши TAB в допустимых расположениях.
* Добавлено средство заполнения групп ресурсов для параметров -ResourceGroup, которое включает заполнение нажатием клавиши TAB в группах ресурсов в текущей подписке.

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Добавлено средство заполнения расположения для параметров -Location, которое включает заполнение нажатием клавиши TAB в допустимых расположениях.
* Добавлено средство заполнения групп ресурсов для параметров -ResourceGroup, которое включает заполнение нажатием клавиши TAB в группах ресурсов в текущей подписке.

#### <a name="azurermsiterecovery"></a>AzureRM.SiteRecovery
* Добавлено средство заполнения расположения для параметров -Location, которое включает заполнение нажатием клавиши TAB в допустимых расположениях.
* Добавлено средство заполнения групп ресурсов для параметров -ResourceGroup, которое включает заполнение нажатием клавиши TAB в группах ресурсов в текущей подписке.

#### <a name="azurermsql"></a>AzureRM.Sql
* Обновлено описание параметров команд аудита.
* Добавлено средство заполнения расположения для параметров -Location, которое включает заполнение нажатием клавиши TAB в допустимых расположениях.
* Добавлено средство заполнения групп ресурсов для параметров -ResourceGroup, которое включает заполнение нажатием клавиши TAB в группах ресурсов в текущей подписке.
* Добавлен параметр -AsJob для долго выполняющихся командлетов.
* Исключен параметр -DatabaseName из командлета Get-AzureRmSqlServiceObjective.

#### <a name="azurermstorage"></a>AzureRM.Storage
* Добавлено средство заполнения расположения для параметров -Location, которое включает заполнение нажатием клавиши TAB в допустимых расположениях.
* Добавлено средство заполнения групп ресурсов для параметров -ResourceGroup, которое включает заполнение нажатием клавиши TAB в группах ресурсов в текущей подписке.
* Устранена проблема с пустой ссылкой при выполнении командлета New-AzureRMStorageAccount с параметром -EnableEncryptionService None.
* Добавлена поддержка параметра -AsJob для долго выполняющихся командлетов Storage. Благодаря этому выбранные командлеты могут выполняться в фоновом режиме и возвращать задание для отслеживания и контроля хода выполнения.
    - Затронутые командлеты: New-, Remove-, Add- и Update- для учетной записи хранения и сетевого правила учетной записи хранения.

#### <a name="azurermstreamanalytics"></a>AzureRM.StreamAnalytics
* Добавлено средство заполнения расположения для параметров -Location, которое включает заполнение нажатием клавиши TAB в допустимых расположениях.
* Добавлено средство заполнения групп ресурсов для параметров -ResourceGroup, которое включает заполнение нажатием клавиши TAB в группах ресурсов в текущей подписке.

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Добавлено средство заполнения расположения для параметров -Location, которое включает заполнение нажатием клавиши TAB в допустимых расположениях.
* Добавлено средство заполнения групп ресурсов для параметров -ResourceGroup, которое включает заполнение нажатием клавиши TAB в группах ресурсов в текущей подписке.

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Добавлено средство заполнения расположения для параметров -Location, которое включает заполнение нажатием клавиши TAB в допустимых расположениях.
* Добавлено средство заполнения групп ресурсов для параметров -ResourceGroup, которое включает заполнение нажатием клавиши TAB в группах ресурсов в текущей подписке.
* Добавлена поддержка параметра -AsJob для долго выполняющихся командлетов Websites. Благодаря этому выбранные командлеты могут выполняться в фоновом режиме и возвращать задание для отслеживания и контроля хода выполнения.
     - Затронутые командлеты: New-, Remove-, Add- и Set-для веб-приложений, плана службы приложений и слотов.

## <a name="2017128-version-511"></a>8\.12.2017, версия 5.1.1
* Analysis Services:
  - В наборе проверок подстановка расположения заменена на динамическую подстановку, что позволило реализовать поддержку всех облаков.
* Служба автоматизации
  - Обновлен командлет Import-AzureRMAutomationRunbook.
    - Добавлена поддержка модулей runbook Python2.
* Пакетная служба Azure
  - Исправлена ошибка, из-за которой при операциях с учетными записями без группы ресурсов не удавалось автоматически определить группу ресурсов.
* Службы вычислений
  - С помощью командлета Get-AzureRmComputeResourceSku отображаются сведения о зоне.
  - Обновлен командлет Disable-AzureRmVmssDiskEncryption для устранения проблемы, описанной здесь: https://github.com/Azure/azure-powershell/issues/5038.
  - Добавлена поддержка параметра -AsJob в командлетах для длительных вычислений. Благодаря этому выбранные командлеты могут выполняться в фоновом режиме и возвращать задание для отслеживания и контроля хода выполнения.
    - В частности, это касается командлетов New-, Update-, Set-, Remove-, Start-, Restart- и Stop- для виртуальных машин и масштабируемых наборов виртуальных машин.
    - Добавлен упрощенный набор параметров для командлета New-AzureRmVM, который создает виртуальную машину и все необходимые ресурсы с помощью стандартных интеллектуальных значений.
* Экземпляры контейнеров
  - Применен пакет SDK 2017-10-01 для службы "Экземпляры контейнеров Azure":
    - поддержка выполнения контейнера до завершения;
    - поддержка подключения тома службы файлов Azure;
    - поддержка открытия нескольких портов для общедоступного IP-адреса.
* Реестр контейнеров
  - Новые командлеты для георепликации и веб-перехватчиков:
    - Get/New/Remove-AzureRmContainerRegistryReplication;
    - Get/New/Remove/Test/Update-AzureRmContainerRegistryWebhook.
* Фабрики данных:
    - Функция шифрования учетных данных теперь работает как с включенным (по сети), так и с отключенным удаленным доступом (на локальном компьютере).
* DataFactoryV2:
  - Добавлены два новых командлета: Update-AzureRmDataFactoryV2 and Stop-AzureRmDataFactoryV2PipelineRun.
* Data Lake Analytics
  - Добавлен параметр ScriptParameter для командлета Submit-AzureRmDataLakeAnalyticsJob.
    - Подробные сведения о параметре ScriptParameter можно получить с помощью параметра Get-Help в командлете Submit-AzureRmDataLakeAnalyticsJob.
  - Для командлета New-AzureRmDataLakeAnalyticsAccount параметр MaxDegreeOfParallelism заменен на MaxAnalyticsUnits.
    - Для параметра MaxAnalyticsUnits добавлен псевдоним MaxDegreeOfParallelism.
  - Для командлета New-AzureRmDataLakeAnalyticsComputePolicy параметр MaxDegreeOfParallelismPerJob заменен на MaxAnalyticsUnitsPerJob.
    - Для параметра MaxAnalyticsUnitsPerJob добавлен псевдоним MaxDegreeOfParallelismPerJob.
  - Для командлета Set-AzureRmDataLakeAnalyticsAccount параметр MaxDegreeOfParallelism заменен на MaxAnalyticsUnits.
    - Для параметра MaxAnalyticsUnits добавлен псевдоним MaxDegreeOfParallelism.
  - Для командлета Submit-AzureRmDataLakeAnalyticsJob параметр DegreeOfParallelism заменен на AnalyticsUnits.
    - Для параметра AnalyticsUnits добавлен псевдоним DegreeOfParallelism.
  - Для командлета Update-AzureRmDataLakeAnalyticsComputePolicy параметр MaxDegreeOfParallelismPerJob заменен на MaxAnalyticsUnitsPerJob.
    - Для параметра MaxAnalyticsUnitsPerJob добавлен псевдоним MaxDegreeOfParallelismPerJob.
* MachineLearningCompute:
  - Добавлен командлет Add Set-AzureRmMlOpCluster.
    - Обновлено число агентов или конфигурация SSL для кластера.
  - Свойства оркестратора являются необязательными.
    - Служба создаст субъект-службу при его отсутствии, поэтому свойства оркестратора стали необязательными.
* PowerBIEmbedded:
  - Добавлена поддержка командлетов для емкостей Power BI Embedded.
  - Новый командлет Get-AzureRmPowerBIEmbeddedCapacity получает сведения о емкости Power BI Embedded.
  - Новый командлет New-AzureRmPowerBIEmbeddedCapacity создает емкость Power BI Embedded.
  - Новый командлет Remove-AzureRmPowerBIEmbeddedCapacity удаляет экземпляр емкости Power BI Embedded.
  - Новый командлет Resume-AzureRmPowerBIEmbeddedCapacity возобновляет экземпляр емкости Power BI Embedded.
  - Новый командлет Suspend-AzureRmPowerBIEmbeddedCapacity приостанавливает экземпляр емкости Power BI Embedded.
  - Новый командлет Test-AzureRmPowerBIEmbeddedCapacity проверяет наличие экземпляра емкости Power BI Embedded.
  - Новый командлет Update-AzureRmPowerBIEmbeddedCapacity вносит изменения в экземпляр емкости Power BI Embedded.
* Профиль
  - Для USGovernmentActiveDirectoryEndpoint установлено значение https://login.microsoftonline.us/.
    - Дополнительные сведения о сопоставлениях конечных точек Azure для государственных организаций см. здесь: https://docs.microsoft.com/azure/azure-government/documentation-government-developer-guide#endpoint-mapping.
    - Добавлена поддержка параметра - AsJob для командлетов, благодаря которому выбранные командлеты могут выполняться в фоновом режиме и возвращать задание для отслеживания и контроля хода выполнения.
    - Добавлен параметр -AsJob для командлета Get-AzureRmSubscription.
* RecoveryServices.Backup
  - После исправления ошибки командлет Get-AzureRmRecoveryServicesBackupItem должен выполнять сравнение без учета регистра для фильтрации имен контейнеров.
  - Исправлена ошибка: в параметре AzureVmItem теперь есть свойство, которое показывает время последней операции резервного копирования, — LastBackupTime.
* Ресурсы
  - Исправлена ошибка, из-за которой командлет где Get-AzureRMRoleAssignment выполнял назначения без имени roledefiniton для пользовательских ролей.
    - Теперь пользователи могут использовать командлет Get-AzureRMRoleAssignment с назначениями, у которых есть имя roledefiniton, независимо от типа роли.
  - Исправлена ошибка, из-за которой командлет Set-AzureRMRoleRoleDefinition выдавал ошибку "Удаленный рабочий стол не найден", когда в разделе assignablescopes появлялась новая область.
    - Теперь пользователи могут использовать командлет Set-AzureRMRoleRoleDefinition с назначаемыми областями, включая новые области, независимо от их расположения.
  - Разрешено использовать области с символом "/" в конце.
    - Теперь пользователи могут использовать командлеты RoleDefinition и RoleAssignment с областями, заканчивающимися символом "/", в соответствии с API и CLI.
  - Пользователям разрешено создавать командлеты RoleAssignment с флагом делегирования.
    - Теперь при использовании командлета New-AzureRMRoleAssignment могут добавлять флаг делегирования.
  - После исправления команды get в RoleAssignment учитывается параметр области.
  - Добавлен псевдоним для ServicePrincipalName в командлете New-AzureRmRoleAssignment.
    - Теперь при использовании командлета New-AzureRmRoleAssignment пользователи могут заменять ServicePrincipalName на ApplicationId.
* SiteRecovery:
  - При подготовке к следующему выпуску критически важных изменений для всех командлетов в этом модуле были добавлены предупреждения о прекращении поддержки.
    - Дополнительные сведения о том, как перенести командлеты из AzureRM, см. в руководстве по предстоящим критическим изменениям.
* SQL
  - Добавлена возможность переименовывать базы данных с помощью командлета Set-AzureRmSqlDatabase.
  - Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/4974.
    - При указании недопустимого значения AUDIT_CHANGED_GROUP для командлетов аудита больше не появляется сообщение об ошибке. Эта проблема будет решена в предстоящем выпуске.
  - Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/5046.
    - Параметр AuditAction больше не игнорируется в командлетах аудита.
  - Исправлена ошибка в командлетах аудита, которая возникала, когда для параметра StorageKeyType указывалось значение Secondary.
    - Когда при настройке аудита больших двоичных объектов для параметра StorageKeyType указывалось значение Secondary, использовался первичный ключ учетной записи хранения, а не вторичный.
  - Изменена формулировка подтверждения для командлета Set-AzureRmSqlServerTransparentDataEncryptionProtector.
* Azure (RDFE):
    - Удалены все командлеты RemoteApp.
* Azure.Storage;
    - Клиентская библиотека службы хранилища Azure обновлена до версии 8.6.0, а библиотека перемещения данных службы хранилища Azure — до версии 0.6.5.

## <a name="20171110-version-501"></a>10.11.2017, версия 5.0.1
* Исправлена проблема при передаче данных, которая приводила к сбою выполнения некоторых командлетов в следующих модулях:
  - AzureRM.ApiManagement
  - AzureRM.Backup
  - AzureRM.Batch
  - AzureRM.Compute
  - AzureRM.DataFactories
  - AzureRM.HDInsight
  - AzureRM.KeyVault
  - AzureRM.RecoveryServices
  - AzureRM.RecoveryServices.Backup
  - AzureRM.RecoveryServices.SiteRecovery
  - AzureRM.RedisCache
  - AzureRM.SiteRecovery
  - AzureRM.Sql
  - AzureRM.Storage
  - AzureRM.StreamAnalytics

## <a name="2017118---version-500"></a>8\.11.2017, версия 5.0.0
* Примечание. Это критическое изменение выпуска. Полный список критических изменений см. в руководстве по миграции (https://aka.ms/azps-migration-guide) ).
* Для всех командлетов в AzureRM теперь добавлена поддержка справки в Интернете.
  - Запустите командлет Get-Help с параметром -Online, чтобы открыть справку в Интернете в браузере по умолчанию.
* Analysis Services:
  * Исправлена команда Synchronize-AzureAsInstance для работы с новым REST API AsAzure для синхронизации.
* Управление API
  * Сведения о важных изменениях, внесенных в этот выпуск ApiManagement, см. в руководстве по миграции.
  * Обновлен командлет Get-AzureRmApiManagementUser для устранения проблемы, описанной здесь: https://github.com/Azure/azure-powershell/issues/4510.
  * Обновлен командлет New-AzureRmApiManagementApi для создания API с пустым путем (https://github.com/Azure/azure-powershell/issues/4069 ).
* ApplicationInsights
  * Добавлены команды для получения, создания и удаления ресурса Application Insights.
    - Get-AzureRmApplicationInsights
    - New-AzureRmApplicationInsights
    - Remove-AzureRmApplicationInsights
  * Добавлены команды для получения, обновления, тарификации и ежедневного ограничения ресурса Application Insights.
    - Get-AzureRmApplicationInsights -IncludeDailyCap
    - Set-AzureRmApplicationInsightsPricingPlan
    - Set-AzureRmApplicationInsightsDailyCap
  * Добавлены команды для получения, создания и удаления непрерывного экспорта ресурса Application Insights.
    - Get-AzureRmApplicationInsightsContinuousExport
    - Set-AzureRmApplicationInsightsContinuousExport
    - New-AzureRmApplicationInsightsContinuousExport
    - Remove-AzureRmApplicationInsightsContinuousExport
  * Добавлены команды для получения, создания и удаления ключей API ресурса Application Insights.
    - Get-AzureRmApplicationInsightsApiKey
    - New-AzureRmApplicationInsightsApiKey
    - Remove-AzureRmApplicationInsightsApiKey
* AzureBatch
  * Добавлены новые параметры для командлета `New-AzureRmBatchAccount`.
    - `PoolAllocationMode`: режим выделения для создания пулов в учетной записи пакетной службы. Чтобы создать учетную запись пакетной службы, которая выделяет узлы в пользовательской подписке, установите значение `UserSubscription`.
    - `KeyVaultId`: идентификатор ресурса хранилища ключей Azure, связанный с учетной записью пакетной службы.
    - `KeyVaultUrl`: URL-адрес хранилища ключей Azure, связанный с учетной записью пакетной службы.
  * Обновлены параметры для командлета `New-AzureBatchTask`.
    - Удален параметр `RunElevated`. Добавлен параметр `UserIdentity` для замены `RunElevated`. Аналогичное поведение можно реализовать, определив `PSUserIdentity`, как показано ниже:
      - $autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
      - $userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
    - Добавлен параметр `AuthenticationTokenSettings`. Этот параметр позволяет обращаться к пакетной службе для предоставления маркера аутентификации выполняющейся задаче (вместо того, чтобы передавать ключи учетной записи пакетной службы этой задаче для выполнения запросов к пакетной службе).
    - Добавлен параметр `ContainerSettings`.
      - Этот параметр позволяет обращаться к пакетной службе для запуска задачи в пределах контейнера.
    - Добавлен параметр `OutputFiles`.
      - Этот параметр позволяет настроить задачу для передачи файлов в службу хранилища Azure после ее завершения.
  * Обновлены параметры для командлета `New-AzureBatchPool`.
    - Добавлен параметр `UserAccounts`.
      - Этот параметр определяет учетные записи пользователей, созданные на каждом узле в пуле.
    - Добавлен параметр `TargetLowPriorityComputeNodes`; параметр `TargetDedicated` переименован в `TargetDedicatedComputeNodes`.
      - Для параметра `TargetDedicatedComputeNodes` создан псевдоним `TargetDedicated`.
    - Добавлен параметр `NetworkConfiguration`.
      - Этот параметр позволяет настраивать параметры сети пулов.
  * Обновлены параметры для командлета `New-AzureBatchCertificate`.
    - Параметр `Password` теперь имеет значение `SecureString`.
  * Обновлены параметры для командлета `New-AzureBatchComputeNodeUser`.
    - Параметр `Password` теперь имеет значение `SecureString`.
  * Обновлены параметры для командлета `Set-AzureBatchComputeNodeUser`.
    - Параметр `Password` теперь имеет значение `SecureString`.
  * Параметр `Name` переименован в `Path` для командлетов `Get-AzureBatchNodeFile`, `Get-AzureBatchNodeFileContent` и `Remove-AzureBatchNodeFile`.
    - Для параметра `Path` создан псевдоним `Name`.
  * Изменения объектов
    - Полный список см. в журнале изменений пакетной службы
  * Добавлена поддержка аутентификации на основе Azure Active Directory.
    - Чтобы использовать аутентификацию Azure Active Directory, необходимо получить объект `BatchAccountContext` с помощью командлета `Get-AzureRmBatchAccount` и передать `BatchAccountContext` параметру `-BatchContext` командлета пакетной службы. Аутентификация Azure Active Directory является обязательной для учетных записей с `PoolAllocationMode = UserSubscription`.
    - Для существующих или новых учетных записей, созданных с помощью `PoolAllocationMode = BatchService`, можно продолжать использовать аутентификацию на основе общих ключей, получая объект `BatchAccountContext` с помощью командлета `Get-AzureRmBatchAccoutKeys`.
* Службы вычислений
  * Команды расширения шифрования диска Azure
    - Добавлен параметр -EncryptFormatAll для командлета Set-AzureRmVmDiskEncryptionExtension для шифрования дисков данных.
    - Добавлены параметры -ExtensionPublisherName и -ExtensionType для командлета Set-AzureRmVmDiskEncryptionExtension для переключения на другие версии расширения.
    - Добавлены параметры -ExtensionPublisherName и -ExtensionType для командлета Disable-AzureRmVmDiskEncryption для переключения на другие версии расширения.
    - Добавлены параметры -ExtensionPublisherName и -ExtensionType для командлета Get-AzureRmVmDiskEncryptionStatus для переключения на другие версии расширения.
* Data Lake Analytics
  * Сведения о важных изменениях, внесенных в этот выпуск DataLakeAnalytics, см. в руководстве по миграции.
  * Изменено одно из двух свойств OutputTypes командлета Get-AzureRmDataLakeAnalyticsAccount.
    - Список \<DataLakeAnalyticsAccount> заменен на список \<PSDataLakeAnalyticsAccountBasic>.
    - Свойства PSDataLakeAnalyticsAccountBasic являются строгим подмножеством свойств DataLakeAnalyticsAccount.
    - Дополнительные свойства DataLakeAnalyticsAccount не возвращаются службой.  Следовательно, описываемое изменение точно это отражает. Эти дополнительные свойства по-прежнему связаны с PSDataLakeAnalyticsAccountBasic, но теперь они отмечены как Obsolete.
  * Изменено одно из двух свойств OutputTypes командлета Get-AzureRmDataLakeAnalyticsJob.
    - Список \<JobInformation> заменен на список \<PSJobInformationBasic>.
    - Свойства PSJobInformationBasic являются строгим подмножеством свойств JobInformation.
    - Дополнительные свойства JobInformation не возвращаются службой.  Следовательно, описываемое изменение точно это отражает. Эти дополнительные свойства по-прежнему связаны с PSJobInformationBasic, но теперь они отмечены как Obsolete.
* Data Lake Store
  * Сведения о важных изменениях, внесенных в этот выпуск DataLakeStore, см. в руководстве по миграции.
  * Изменено одно из двух свойств OutputTypes командлета Get-AzureRmDataLakeStoreAccount.
    - Список \<PSDataLakeStoreAccount> заменен на список \<PSDataLakeStoreAccountBasic>.
    - Свойства PSDataLakeStoreAccountBasic являются строгим подмножеством свойств PSDataLakeStoreAccount.
    - Дополнительные свойства PSDataLakeStoreAccount не возвращаются службой.  Следовательно, описываемое изменение точно это отражает. Эти дополнительные свойства по-прежнему связаны с PSDataLakeStoreAccountBasic, но теперь они отмечены как Obsolete.
* DNS:
  * Добавлена поддержка типов записей CAA в Azure DNS.
    - Добавлена поддержка всех операций с типом записи CAA.
* концентратор событий.
  * Сведения о важных изменениях, внесенных в этот выпуск EventHub, см. в руководстве по миграции.
* Аналитика
  * Сведения о важных изменениях, внесенных в этот выпуск Insights, см. в руководстве по миграции.
* Сеть
  * Сведения о важных изменениях, внесенных в этот выпуск Network, см. в руководстве по миграции.
  * Добавлен командлет для отображения списка доступных поставщиков услуг Интернета в заданном регионе Azure.
    - Get-AzureRmNetworkWatcherReachabilityProvidersList
  * Добавлен командлет для получения оценки относительной задержки для поставщиков услуг Интернета из указанного расположения в регионы Azure.
    - Get-AzureRmNetworkWatcherReachabilityReport
* Профиль
  - Set-AzureRmDefault
    - Используйте этот командлет, чтобы задать группу ресурсов по умолчанию.  Параметр -ResourceGroup будет использоваться как дополнительный для некоторых командлетов и как параметр по умолчанию, если группа ресурсов не определена.
    - ```Set-AzureRmDefault -ResourceGroupName "ExampleResourceGroup"```
    - Если указанная группа ресурсов существует в подписке, она будет использоваться по умолчанию.  В противном случае группа ресурсов будет создана для использования по умолчанию.
  - Get-AzureRmDefault
    - Используйте этот командлет для получения текущей группы ресурсов по умолчанию (а также используемых по умолчанию в будущем).
    - ```Get-AzureRmDefault -ResourceGroup```
  - Clear-AzureRmDefault
    - Используйте этот командлет для удаления текущей группы ресурсов по умолчанию.
    - ```Clear-AzureRmDefault -ResourceGroup```
  - Add-AzureRmEnvironment и Set-AzureRmEnvironment
    - Добавьте параметр BatchAudience, который определяет аудиторию Active Directory пакетной службы Azure для использования при получении маркеров аутентификации для пакетной службы.
* RecoveryServices.Backup
  * Добавлены командлеты для мгновенного восстановления файлов.
    - Get-AzureRmRecoveryServicesBackupRPMountScript
    - Disable-AzureRmRecoveryServicesBackupRPMountScript
  * Пакет SDK RecoveryServices.Backup обновлен до последней версии.
  * Обновлены тесты для рабочей нагрузки виртуальной машины Azure, чтобы все настройки, необходимые для тестовых запусков, выполнялись самими тестами.
  * Устранены проблемы, описанные здесь: https://github.com/Azure/azure-powershell/issues/3164.
* Службы восстановления. Site Recovery
  * Изменения VMware ASR для Azure Site Recovery (командлеты, которые сейчас поддерживают операции Enterprise — Enterprise, Enterprise — Azure, HyperV — Azure).
    - New-AzureRmRecoveryServicesAsrPolicy
    - New-AzureRmRecoveryServicesAsrProtectedItem
    - Update-AzureRmRecoveryServicesAsrPolicy
    - Update-AzureRmRecoveryServicesAsrProtectionDirection
  * Добавлена поддержка хранилища под управлением AAD
  * Добавлены командлеты для управления ресурсами VCenter
    - Get-AzureRmRecoveryServicesAsrVCenter
    - New-AzureRmRecoveryServicesAsrVCenter
    - Remove-AzureRmRecoveryServicesAsrVCenter
    - Update-AzureRmRecoveryServicesAsrVCenter
  * Добавлены другие командлеты
    - Get-AzureRmRecoveryServicesAsrAlertSetting
    - Get-AzureRmRecoveryServicesAsrEvent
    - New-AzureRmRecoveryServicesAsrProtectableItem
    - Set-AzureRmRecoveryServicesAsrAlertSetting
    - Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob
    - Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob
    - Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob
    - Update-AzureRmRecoveryServicesAsrMobilityService
* Служебная шина
  - Сведения о важных изменениях, внесенных в этот выпуск ServiceBus, см. в руководстве по миграции.
* SQL
  * Добавлена поддержка для отображения и отмены асинхронной операции updateslo для базы данных.
    - Обновите существующий командлет Get-AzureRmSqlDatabaseActivity, чтобы вернуть состояние операции updateslo для базы данных.
    - Добавьте новый командлет Stop-AzureRmSqlDatabaseActivity, чтобы отменить асинхронную операцию updateslo для базы данных.
  * Добавлена поддержка избыточности зон для баз данных и эластичных пулов.
    - Добавлен параметр ZoneRedundant для командлета New-AzureRmSqlDatabase.
    - Добавлен параметр ZoneRedundant для командлета Set-AzureRmSqlDatabase.
    - Добавлен параметр ZoneRedundant для командлета New-AzureRmSqlElasticPool.
    - Добавлен параметр ZoneRedundant для командлета Set-AzureRmSqlElasticPool.
  * Добавлена поддержка псевдонимов для сервера DNS.
    - Добавлен командлет Get-AzureRmSqlServerDnsAlias, который получает псевдонимы сервера DNS по имени сервера и псевдонима, а также перечисляет псевдонимы сервера DNS для Azure SQL Server.
    - Добавлен командлет New-AzureRmSqlServerDnsAlias, который создает псевдоним сервера DNS для указанного сервера Azure SQL Server.
    - Добавлен командлет Set-AzurermSqlServerDnsAlias, который обновляет сервер Azure SQL Server , на который указывает псевдоним сервера DNS.
    - Добавлен командлет Remove-AzureRmSqlServerDnsAlias, который удаляет псевдоним сервера DNS для сервера Azure SQL Server.
* Azure.Storage;
  * Клиентская библиотека службы хранилища Azure обновлена до версии 8.5.0, а библиотека перемещения данных службы хранилища Azure — до версии 0.6.3.
  * Добавлена поддержка моментальных снимков файловых ресурсов.
    - Добавлен параметр SnapshotTime для командлета Get-AzureStorageShare.
    - Добавлен параметр IncludeAllSnapshot для командлета Remove-AzureStorageShare.
