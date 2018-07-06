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
# <a name="release-notes"></a>Заметки о выпуске

Здесь приведен список изменений, внесенных в Azure PowerShell в этом выпуске.

---
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