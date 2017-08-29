---
title: "Журнал изменений Azure PowerShell | Документация Майкрософт"
description: "Это руководство содержит историю изменений Azure PowerShell, внесенных в новом выпуске."
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-resource-manager
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: 
ms.date: 05/18/2017
ms.openlocfilehash: 5c8fa2a5a8f94cd24b66f42c237749a7b89af3b3
ms.sourcegitcommit: ec0b3565264ff7c9f03315ded182f3d5cce534fc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/13/2017
---
# <a name="release-notes"></a>Заметки о выпуске

Здесь приведен список изменений, внесенных в Azure PowerShell в этом выпуске.

## <a name="version-400"></a>Версия 4.0.0

* Этот выпуск содержит критические изменения. Ознакомьтесь с [руководством по миграции](https://aka.ms/azps-migration-guide), где содержатся сведения об изменениях и влиянии на существующие сценарии.
* Управление API
  - Добавлена поддержка настройки внешних групп в New-AzureRmApiManagementGroup.
* Выставление счетов
  - Новый командлет Get-AzureRmBillingPeriod:
    + командлет, извлекающий сведения о расчетных периодах в подписке Azure.
  - Обновлен командлет Get-AzureRmBillingInvoice.
  - Новое свойство BillingPeriodNames.
  - Представление выходных данных в виде списка.
* Среда выполнения приложений
  - Обновлены командлеты Set-AzureRmVMAEMExtension и Test-AzureRmVMAEMExtension для поддержки управляемых дисков уровня "Премиум".
  - Параметры шифрования службы архивации для виртуальных машин IaaS и восстановления при сбое.
  - Параметр ChefServiceInterval переименован в ChefDaemonInterval. Но и старое значение продолжит работать.
  - Из объекта виртуальной машины PS удалены повторяющиеся свойства DataDiskNames и NetworkInterfaceIDs.
  - Соответственно, параметры DataDiskNames и NetworkInterfaceIDs стали необязательными в командлетах Remove-AzureRmVMDataDisk и Remove-AzureRmVMNetworkInterface.
  - В командлетах Get исправлена ошибка конвейера при возвращении объекта списка.
  - Командлеты, конфликтовавшие с командлетами RDFE, были переименованы. Дополнительные сведения см. по этой ссылке: https://github.com/Azure/azure-powershell/issues/2917.
    + `New-AzureVMSqlServerAutoBackupConfig` был переименован в `New-AzureRmVMSqlServerAutoBackupConfig`.
    + `New-AzureVMSqlServerAutoPatchingConfig` был переименован в `New-AzureRmVMSqlServerAutoPatchingConfig`.
    + `New-AzureVMSqlServerKeyVaultCredentialConfig` был переименован в `New-AzureRmVMSqlServerKeyVaultCredentialConfig`.
* Потребление
  - Новый командлет Get-AzureRmConsumptionUsageDetail:
    + командлет, извлекающий сведения об использовании в подписке.
* Реестр контейнеров
  - Добавлены командлеты PowerShell для реестра контейнеров Azure:
    + New-AzureRmContainerRegistry;
    + Get-AzureRmContainerRegistry;
    + Update-AzureRmContainerRegistry;
    + Remove-AzureRmContainerRegistry;
    + Get-AzureRmContainerRegistryCredential;
    + Update-AzureRmContainerRegistryCredential;
    + Test-AzureRmContainerRegistryNameAvailability.
* Data Lake Analytics
  - Добавлена поддержка получения и отображения списка пакетов каталога.
  - Добавлена поддержка получения списка следующих элементов из более далеких предков:
    + Таблица
    + TVF
    + Просмотр
    + Статистика
* Data Lake Store
  - Для `Import-AzureRMDataLakeStoreItem` и `Export-AzureRMDataLakeStoreItem` ведение журнала трассировки по умолчанию отключено, чтобы повысить производительность. Если ведение журнала трассировки необходимо, используйте параметры `-DiagnosticLogLevel` и `-DiagnosticLogPath`.
  - Исправлена ошибка, из-за которой происходил сбой в работе PowerShell при передаче в ADLS множества небольших файлов.
* концентратор событий.
  - Исправление ошибок:
    + Исправлена ошибка в командлете Set-AzureRmEventHubNamespace. "Tier" (Категория) не может иметь значение null, поэтому оно исправлено на SkuName.
    + В командлете Set-AzureRmEventHub исправлена ошибка "Ссылка на объект не указывает на экземпляр объекта" при обновлении концентратора событий.
* Аналитика
  - Add-AzureRm*AlertRule:
    + возвращает один объект (newResource, statusCode, requestId);
  - Get-AzureRmAlertRule:
    + выходные данные теперь перечисляются, а не считаются одним объектом. Тип не изменился, он по-прежнему представляет собой список.
  - Remove-AzureRmAlertRule:
    + свойство statusCode теперь соответствует коду состояния, возвращаемому запросом. Раньше оно всегда имело значение "ОК".
  - Add-AzureRmAutoscaleSetting:
    + теперь возвращает один объект (а не список, как раньше), который содержит statusCode, requestId и созданный или обновленный ресурс;
    + код состояния теперь соответствует состоянию, возвращаемому запросом. Раньше он всегда имел значение "ОК".
  - New-AzureRmAutoscaleRule:
    + параметр ScaleActionType был расширен и теперь получает значения ChangeCount, PercentChangeCount и ExactCount.
  - Remove-AzureRmAutoscaleSetting:
    + свойство statusCode в выходных данных теперь соответствует коду состояния, возвращаемому запросом. Раньше оно всегда имело значение "ОК".
  - Get-AzureRMLogProfile:
    + выходные данные теперь перечисляются, а не считаются одним объектом. Тип выходных данных по-прежнему представляет собой список.
  - Remove-AzureRmLogProfile:
    + реализован параметр PassThru.
  - API метрик:
    + пакет SDK теперь извлекает метрики из MDM.
  - Get-AzureRmMetricDefinition:
    + выходные данные по-прежнему представляют собой список, но структура списка изменилась.
  - Get-AzureRmMetric:
    + вызов изменился. Теперь он имеет такой синтаксис: Get-AzureRmMetric ResourceId [MetricNames [TimeGrain] [AggregationType] [StartTime] [EndTime]] [DetailedOutput];
    + выходные данные представляют собой список, а структура элементов списка изменилась.
* Хранилище ключей
  - Добавление поддержки архивации и восстановления секретов Key Vault:
    + секреты можно архивировать и восстанавливать в соответствии с функциональными возможностями, которые поддерживаются для ключей.

  - Теперь командлеты службы архивации для ключей и секретов принимают соответствующий объект в качестве входного параметра:
    + вызывающий объект может выстраивать операции извлечения и архивации в цепочку: Get-AzureKeyVaultKey -VaultName myVault -Name myKey | Backup-AzureKeyVaultKey.

  - Теперь командлеты службы архивации поддерживают параметр -Force, позволяющий перезаписать существующий файл:
    + обратите внимание, что попытка перезаписать существующий файл больше не вызывает исключение. Вместо этого пользователю будет предложено выбрать дальнейшие действия.
* Приложение логики
  - Новые параметры для командлетов аварийного восстановления контрольного номера обмена:
    + необязательный параметр -AgreementType (X12 или Edifact) для указания соответствующих контрольных номеров.
* Машинное обучение
  - Использована новая версия пакета SDK для .NET машинного обучения Azure и добавлен новый командлет:
    + Add-AzureRmMlWebServiceRegionalProperty.
  - Небольшие исправления формулировок в тексте справки.
* Сеть
  - Добавлен командлет Test-AzureRmNetworkWatcherConnectivity:
    + возвращает сведения о подключении для указанной исходной виртуальной машины и целевого объекта;
    + если подключение между исходным и целевым объектами не удается установить, то командлет возвращает сведения об этой проблеме.
* Профиль
  - Добавлен командлет Send-Feedback, который позволяет пользователю инициировать набор запросов, который отправляет отзыв команде Azure PowerShell.
  - Удалены следующие псевдонимы, так как они конфликтовали с существующими именами командлетов в модуле Azure:
    + `Enable-AzureDataCollection` (поддерживается `Enable-AzureRmDataCollection`);
    + `Disable-AzureDataCollection` (поддерживается `Disable-AzureRmDataCollection`).
* Передача
  - Добавлены командлеты для ретранслятора Azure, которые позволяют пользователям создавать все ресурсы ретранслятора Azure и управлять ими:
    + `New-AzureRmRelayNamespace`
    + `Get-AzureRmRelayNamespace`
    + `Set-AzureRmRelayNamespace`
    + `Remove-AzureRmRelayNamespace`
    + `New-AzureRmWcfRelay`
    + `Get-AzureRmWcfRelay`
    + `Set-AzureRmWcfRelay`
    + `Remove-AzureRmWcfRelay`
    + `New-AzureRmRelayHybridConnection`
    + `Get-AzureRmRelayHybridConnection`
    + `Set-AzureRmRelayHybridConnection`
    + `Remove-AzureRmRelayHybridConnection`
    + `Test-AzureRmRelayName`
    + `Get-AzureRmRelayOperation`
    + `New-AzureRmRelayKey`
    + `Get-AzureRmRelayKey`
    + `New-AzureRmRelayAuthorizationRule`
    + `Get-AzureRmRelayAuthorizationRule`
    + `Set-AzureRmRelayAuthorizationRule`
    + `Remove-AzureRmRelayAuthorizationRule`
* Ресурсы
  - Поддержка развертываний между группами ресурсов с помощью командлета New-AzureRmResourceGroupDeployment:
    + теперь пользователи могут использовать вложенные развертывания для развертывания в разных группах ресурсов.
* Служебная шина

  - Исправление ошибки. Свойствам объекта очереди служебной шины были присвоены значения null, а объект используется в качестве входного параметра в командлете Set-AzureRmServiceBusQueue для обновления очереди:
   - это относится к свойствам LockDuration, EntityAvailabilityStatus, DuplicateDetectionHistoryTimeWindow, MaxDeliveryCount и MessageCount.
* Service Fabric

  - Добавлены командлеты для Service Fabric:
    + Add-AzureRmServiceFabricApplicationCertificate — добавляет сертификат, который будет использоваться в качестве сертификата приложения;
    + Add-AzureRmServiceFabricClientCertificate — добавляет общее имя или отпечаток в параметры кластера для аутентификации клиента;
    + Add-AzureRmServiceFabricClusterCertificate — добавляет в кластер дополнительный сертификат кластера для смены существующего сертификата;
    + Add-AzureRmServiceFabricNodes — добавляет в кластер узлы или виртуальные машины определенного типа узла;
    + Add-AzureRmServiceFabricNodeType — добавляет в существующий кластер тип узла или виртуальные машины;
    + Get-AzureRmServiceFabricCluster — получает сведения о ресурсе кластера;
    + New-AzureRmServiceFabricCluster — создает кластер Service Fabric. Эта команда имеет множество перегрузок для реализации различных сценариев;
    + Remove-AzureRmServiceFabricClientCertificate — удаляет сертификат клиента, чтобы он не использовался для доступа к кластеру;
    + Remove-AzureRmServiceFabricClusterCertificate — удаляет сертификат кластера, чтобы он не использовался для обеспечения безопасности кластера;
    + Remove-AzureRmServiceFabricNodes — удаляет из кластера узлы определенного типа;
    + Remove-AzureRmServiceFabricNodeType — удаляет из кластера тип узла;
    + Remove-AzureRmServiceFabricSettings — удаляет из кластера один или несколько параметров Service Fabric;
    + Set-AzureRmServiceFabricSettings — добавляет в кластер или обновляет в нем один или несколько параметров Service Fabric;
    + Set-AzureRmServiceFabricUpgradeType — изменяет в кластере тип обновления Service Fabric;
    + Update-AzureRmServiceFabricDurability — изменяет уровень устойчивости кластера;
    + Update-AzureRmServiceFabricReliability — изменяет уровень надежности кластера.
* SQL
  - В командлет New-AzureRmSqlDatabase добавлен параметр -SampleName.
  - Обновлены командлеты групп отработки отказа Azure.
  - Удалены параметры Tag.
  - Из командлета Remove-AzureRmSqlDatabaseFailoverGroup удалены параметры PartnerResourceGroupName и PartnerServerName.
  - В командлеты New- и Set- добавлен параметр GracePeriodWithDataLossHours, который в конечном счете должен заменить параметр GracePeriodWithDataLossHour.
  - Документация была конкретизирована и обновлена.
  - Изменено форматирование возвращаемых объектов и исправлены некоторые ошибки, из-за которых не всегда заполнялись поля.
  - В объект группы отработки отказа добавлены свойства DatabaseNames и PartnerLocation.
  - Исправлена ошибка, из-за которой командлет Switch- немедленно возвращал результат, не дожидаясь завершения операции.
  - Исправлена ошибка переполнения целочисленного значения при использовании высоких значений льготного периода.
  - Льготный период изменяется до минимального значения (1 час), если указано меньшее значение.
  - Из допустимых значений параметра ExcludedDetectionType командлетов Set-AzureRmSqlDatabaseThreatDetectionPolicy и Set-AzureRmSqlServerThreatDetectionPolicy удалено значение Usage_Anomaly.
* Хранилище
  - Пакет SDK для поставщика ресурсов хранилища обновлен до версии 6.3.0.
  - New/Set-AzureRmStorageAccount: добавлен новый параметр для поддержки EnableHttpsTrafficOnly.
  - New/Set/Get-AzureRmStorageAccount: возвращаемая учетная запись хранения содержит новый атрибут EnableHttpsTrafficOnly.
* Azure.Storage;
  - Клиентская библиотека службы хранилища Azure обновлена до версии 8.1.1, а библиотека перемещения данных службы хранилища Azure — до версии 0.5.1.
  - Добавлен новый командлет для поддержки функции добавочного копирования больших двоичных объектов.
