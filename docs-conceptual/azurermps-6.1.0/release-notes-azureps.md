---
title: Журнал изменений Azure PowerShell | Документация Майкрософт
description: Это руководство содержит историю изменений Azure PowerShell, внесенных в новом выпуске.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 0b7902155c47f2e6355e9147c203867288caab81
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/23/2018
ms.locfileid: "34462139"
---
# <a name="release-notes"></a>Заметки о выпуске

Здесь приведен список изменений, внесенных в Azure PowerShell в этом выпуске.

---
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