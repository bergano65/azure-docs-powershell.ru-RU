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
ms.date: 11/14/2017
ms.openlocfilehash: cf58789ba69fd2fc157e37d0b052827b361246e5
ms.sourcegitcommit: c42c7176276ec4e1cc3360a93e6b15d32083bf9f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2017
---
# <a name="release-notes"></a>Заметки о выпуске

Здесь приведен список изменений, внесенных в Azure PowerShell в этом выпуске.

## <a name="20171208-version-511"></a>08.12.2017, версия 5.1.1
* Analysis Services:
    - В наборе проверок подстановка расположения заменена на динамическую подстановку, что позволило реализовать поддержку всех облаков.
* Служба автоматизации
    - Обновлен командлет Import-AzureRMAutomationRunbook.
        - Добавлена поддержка модулей runbook Python2.
* Пакетная служба
    - Исправлена ошибка, из-за которой при операциях с учетными записями без группы ресурсов не удавалось автоматически определить группу ресурсов.
* Среда выполнения приложений
    - С помощью командлета Get-AzureRmComputeResourceSku отображаются сведения о зоне.
    - Командлет Disable-AzureRmVmssDiskEncryption обновлен для исправления следующей ошибки: https://github.com/Azure/azure-powershell/issues/5038.
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
    - Обновлена конечная точка USGovernmentActiveDirectoryEndpoint: https://login.microsoftonline.us/.
        - Дополнительные сведения о сопоставлениях конечных точек службы "Azure для государственных организаций" см. на веб-странице https://docs.microsoft.com/en-us/azure/azure-government/documentation-government-developer-guide#endpoint-mapping.
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
    - Исправлена следующая проблема: https://github.com/Azure/azure-powershell/issues/4974.
        - При указании недопустимого значения AUDIT_CHANGED_GROUP для командлетов аудита больше не появляется сообщение об ошибке. Эта проблема будет решена в предстоящем выпуске.
    - Исправлена следующая проблема: https://github.com/Azure/azure-powershell/issues/5046.
        - Параметр AuditAction больше не игнорируется в командлетах аудита.
    - Исправлена ошибка в командлетах аудита, которая возникала, когда для параметра StorageKeyType указывалось значение Secondary.
        - Когда при настройке аудита больших двоичных объектов для параметра StorageKeyType указывалось значение Secondary, использовался первичный ключ учетной записи хранения, а не вторичный.
    - Изменена формулировка подтверждения для командлета Set-AzureRmSqlServerTransparentDataEncryptionProtector.
* Azure (RDFE):
    - Удалены все командлеты RemoteApp.
* Azure.Storage;
    - Клиентская библиотека службы хранилища Azure обновлена до версии 8.6.0, а библиотека перемещения данных службы хранилища Azure — до версии 0.6.5.

Изменения, внесенные после последнего выпуска: https://github.com/azure/azure-powershell/compare/v5.0.1-November2017...v5.1.1-December2017.

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

## <a name="2017118---version-500"></a>8.11.2017, версия 5.0.0
* ПРИМЕЧАНИЕ. Это важное изменение выпуска. Полный список важных изменений см. в руководстве по миграции (https://aka.ms/azps-migration-guide).
* Для всех командлетов в AzureRM теперь добавлена поддержка справки в Интернете.
    - Запустите командлет Get-Help с параметром -Online, чтобы открыть справку в Интернете в браузере по умолчанию.
* Analysis Services:
    * Исправлена команда Synchronize-AzureAsInstance для работы с новым REST API AsAzure для синхронизации.
* Управление API
    * Сведения о важных изменениях, внесенных в этот выпуск ApiManagement, см. в руководстве по миграции.
    * Обновлен командлет Get-AzureRmApiManagementUser (https://github.com/Azure/azure-powershell/issues/4510).
    * Обновлен командлет New-AzureRmApiManagementApi для создания API с пустым путем (https://github.com/Azure/azure-powershell/issues/4069).
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
* Среда выполнения приложений
    * Команды расширения шифрования диска Azure
        - Добавлен параметр -EncryptFormatAll для командлета Set-AzureRmVmDiskEncryptionExtension для шифрования дисков данных.
        - Добавлены параметры -ExtensionPublisherName и -ExtensionType для командлета Set-AzureRmVmDiskEncryptionExtension для переключения на другие версии расширения.
        - Добавлены параметры -ExtensionPublisherName и -ExtensionType для командлета Disable-AzureRmVmDiskEncryption для переключения на другие версии расширения.
        - Добавлены параметры -ExtensionPublisherName и -ExtensionType для командлета Get-AzureRmVmDiskEncryptionStatus для переключения на другие версии расширения.
* Data Lake Analytics
    * Сведения о важных изменениях, внесенных в этот выпуск DataLakeAnalytics, см. в руководстве по миграции.
    * Изменено одно из двух свойств OutputTypes командлета Get-AzureRmDataLakeAnalyticsAccount.
        - List\<DataLakeAnalyticsAccount> на List\<PSDataLakeAnalyticsAccountBasic>
        - Свойства PSDataLakeAnalyticsAccountBasic являются строгим подмножеством свойств DataLakeAnalyticsAccount.
        - Дополнительные свойства DataLakeAnalyticsAccount не возвращаются службой.  Следовательно, описываемое изменение точно это отражает. Эти дополнительные свойства по-прежнему связаны с PSDataLakeAnalyticsAccountBasic, но теперь они отмечены как Obsolete.
    * Изменено одно из двух свойств OutputTypes командлета Get-AzureRmDataLakeAnalyticsJob.
        - List\<JobInformation> на List\<PSJobInformationBasic>
        - Свойства PSJobInformationBasic являются строгим подмножеством свойств JobInformation.
        - Дополнительные свойства JobInformation не возвращаются службой.  Следовательно, описываемое изменение точно это отражает. Эти дополнительные свойства по-прежнему связаны с PSJobInformationBasic, но теперь они отмечены как Obsolete.
* Data Lake Store
    * Сведения о важных изменениях, внесенных в этот выпуск DataLakeStore, см. в руководстве по миграции.
    * Изменено одно из двух свойств OutputTypes командлета Get-AzureRmDataLakeStoreAccount.
        - List\<PSDataLakeStoreAccount> на List\<PSDataLakeStoreAccountBasic>
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
    * Исправлены ошибки (https://github.com/Azure/azure-powershell/issues/3164).
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
