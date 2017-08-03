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
ms.date: 07/26/2017
ms.openlocfilehash: cc2fe75f498f9043e5a4b632c144877af0143173
ms.sourcegitcommit: 20bcef86db4e4869125bb63085fcffd009c19280
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/27/2017
---
# <a name="release-notes"></a>Заметки о выпуске

Здесь приведен список изменений, внесенных в Azure PowerShell в этом выпуске.

## <a name="20170717---version-421"></a>17.07.2017: версия 4.2.1
* Среда выполнения приложений
    - Устранена проблема с командлетами создания и обновления диска виртуальной машины и моментального снимка диска виртуальной машины (ссылка) [https://github.com/azure/azure-powershell/issues/4309].
      - New-AzureRmDisk
      - New-AzureRmSnapshot
      - Update-AzureRmDisk
      - Update-AzureRmSnapshot
* Профиль
    - Устранена проблема с неинтерактивной аутентификацией пользователя в RDFE (ссылка) [https://github.com/Azure/azure-powershell/issues/4299].
* Управление службами
    - Устранена проблема с неинтерактивной аутентификацией пользователя (ссылка) [https://github.com/Azure/azure-powershell/issues/4299].

## <a name="2017711---version-420"></a>11.07.2017: версия 4.2.0
* Analysis Services:
    * Добавлен новый API уровня данных.
        - Добавлен API для получения журнала сервера Analysis Services, Export-AzureAnalysisServicesInstanceLog.
* Служба автоматизации
    * Правильно задано значение часового пояса для еженедельного и ежемесячного расписаний для New-AzureRmAutomationSchedule.
        - Дополнительные сведения можно найти в этом выпуске: https://github.com/Azure/azure-powershell/issues/3043.
* AzureBatch
    - Добавлен новый командлет Get-AzureBatchJobPreparationAndReleaseTaskStatus.
    - В параметры Get-AzureBatchNodeFileContent добавлены начало и конец диапазона байтов.
* Cognitive Services:
    * Интеграция с пакетом SDK управления Cognitive Services версии 1.0.0.
    * Исправлена ошибка при проверке длины имени учетной записи.
* Среда выполнения приложений
    * Поддержка типов учетной записи хранения для диска образа:
        - В Set-AzureRmImageOsDisk и Add-AzureRmImageDataDisk добавлен параметр StorageAccountType.
    * Функция PrivateIP и PublicIP в IP-конфигурации VMSS:
        - В New-AzureRmVmssIpConfig добавлены имена PrivateIPAddressVersion, PublicIPAddressConfigurationName, PublicIPAddressConfigurationIdleTimeoutInMinutes и DnsSetting.
        - В New-AzureRmVmssIpConfig добавлен параметр PrivateIPAddressVersion для указания IPv4 или IPv6.
    * Функция обслуживания производительности:
        - В Restart-AzureRmVM добавлен параметр PerformMaintenance.
        - Get-AzureRmVM -Status отображает сведения об обслуживании производительности заданной виртуальной машины.
    * Функция идентификации виртуальных машин:
        - В New-AzureRmVMConfig и UpdateAzureRmVM добавлен параметр IdentityType.
        - Get-AzureRmVM отображает сведения об идентификаторе заданной виртуальной машины.
    * Функция идентификации VMSS:
        - В New-AzureRmVmssConfig добавлен параметр IdentityType.
        - Get-AzureRmVmss отображает сведения об идентификаторе заданного VMSS.
    * Функция диагностики загрузки VMSS:
        - Добавлен новый командлет для настройки диагностики загрузки объекта VMSS: Set-AzureRmVmssBootDiagnostics.
        - В New-AzureRmVmssConfig добавлен параметр BootDiagnostic.
    * Функция LicenseType для VMSS:
        - В New-AzureRmVmssConfig добавлен параметр LicenseType.
    * Поддержка RecoveryPolicyMode:
        - В New-AzureRmVmssConfig добавлен параметр RecoveryPolicyMode.
    * Функция SKU вычислительных ресурсов:
        - Новый командлет Get-AzureRmComputeResourceSku выводит все номера SKU вычислительных ресурсов.
* Фабрики данных:
    * New-AzureRmDataFactoryGatewayKey объявлен нерекомендуемым.
    * Добавлена функция ключа аутентификации шлюза и командлеты для нее: New-AzureRmDataFactoryGatewayAuthKey и Get-AzureRmDataFactoryGatewayAuthKey.
* Data Lake Analytics
    * Добавлена поддержка CRUD для политики вычислений с помощью следующих команд:
        - New-AzureRMDataLakeAnalyticsComputePolicy;
        - Get-AzureRMDataLakeAnalyticsComputePolicy;
        - Remove-AzureRMDataLakeAnalyticsComputePolicy;
        - Update-AzureRMDataLakeAnalyticsComputePolicy.
    * Добавлена поддержка метаданных связи задания для упрощения работы с повторяющимися заданиями и конвейерами заданий. Следующие команды были обновлены или добавлены:
        - Submit-AzureRMDataLakeAnalyticsJob;
        - Get-AzureRMDataLakeAnalyticsJob;
        - Get-AzureRMDataLakeAnalyticsJobRecurrence;
        - Get-AzureRMDataLakeAnalyticsJobPipeline.
    * Обновлена аудитория токена для интерфейсов API заданий и каталогов для использования правильной аудитории Data Lake вместо аудитории ресурсов Azure.
* Data Lake Store
    * В командлет Set-AzureRMDataLakeStoreAccount добавлена поддержка управляемой пользователем смены ключей Key Vault.
    * Добавлено качественное обновление для автоматической активации вызова `enableKeyVault`, когда пользователь, управляющий Key Vault, добавляет или сменяет ключ.
    * Обновлена аудитория токена для интерфейсов API заданий и каталогов для использования правильной аудитории Data Lake вместо аудитории ресурсов Azure.
    * Исправлена ошибка, ограничивающая размер файлов, создаваемых и добавляемых с помощью следующих командлетов:
        - New-AzureRmDataLakeStoreItem
        - Add-AzureRmDataLakeStoreItemContent
* DNS:
    * Устранена ошибка канальной передачи для Get-AzureRmDnsZone.
        - Дополнительные сведения можно найти здесь: https://github.com/Azure/azure-powershell/issues/4203.
* HDInsight
    * Добавлена поддержка включения и отключения Operations Management Suite (OMS).
    * Новые командлеты
        - Enable-AzureRmHDInsightOperationsManagementSuite;
        - Disable-AzureRmHDInsightOperationsManagementSuite;
        - Get-AzureRmHDInsightOperationsManagementSuite.
    * Добавлены новые параметры для задания настраиваемых конфигураций Spark для Add-AzureRmHDInsightConfigValues:
        - параметры SparkDefaults и SparkThriftConf для Spark 1.6;
        - параметры Spark2Defaults и Spark2ThriftConf для Spark 2.0.
* Аналитика
    * Проблема № 4215 (запрос на изменение): удален 15-дневный лимит для временного окна командлета Get-AzureRmLog. Также внесены незначительные изменения в имена модульных тестов.
    * Устранена проблема № 3957 для Get-AzureRmLog.
        - Проблема № 1: серверная часть возвращала по 200 записей на странице, которые были связаны с помощью токена перехода на следующую страницу. Клиенты видели, что командлет возвращает только 200 записей, хотя они знали, что записей больше. Это происходило независимо от значения, которое они задавали для параметра MaxEvents, если только это значение не было меньше 200.
        - Проблема № 2: документация содержала неправильные данные об этом командлете, например: временное окно по умолчанию составляло 1 час.
        - Исправление № 1: теперь этот командлет соответствует токену перехода, возвращаемому серверной частью, до достижения MaxEvents или конца набора.<br>Значение по умолчанию для MaxEvents равно 1000, а максимальное — 100 000. Любое значение MaxEvents, меньшее 1, игнорируется, и используется значение по умолчанию. Эти значения и поведение не изменились, просто теперь они правильно описаны в документации.<br>Добавлен псевдоним для MaxEvents, MaxRecords, так как имя командлета больше не связано с событиями, а только с журналами.
        - Исправление № 2: документация содержит правильные и более подробные сведения. Это новый псевдоним, правильное временное окно, правильное значение по умолчанию, минимальное и максимальное значения.
* Хранилище ключей
    * Удалите из запроса каталога адрес электронной почты, когда в командлетах Set-AzureRMKeyVaultAccessPolicy и Remove-AzureRMKeyVaultAccessPolicy указывается параметр -UserPrincipalName.
      - Теперь у обоих командлетов есть параметр -EmailAddress, который может использоваться вместо параметра -UserPrincipalName, когда в запросе удобно использовать адрес электронной почты.  При наличии в каталоге более одного соответствующего адреса электронной почты выполнение командлета завершится ошибкой.
* Сеть
    * New-AzureRmIpsecPolicy: SALifeTimeSeconds и SADataSizeKilobytes больше не являются обязательными параметрами.
        - Значение SALifeTimeSeconds по умолчанию составляет 27 000 секунд.
        - Значение SADataSizeKilobytes по умолчанию составляет 102 400 000 КБ.
    * Добавлена поддержка конфигурации пользовательского набора шифрования с использованием политики SSL, а также вывод списка всех API с параметрами SSL в шлюзе приложений.
        - Добавлены необязательные параметры -PolicyType, -PolicyName, -MinProtocolVersion и -Ciphersuite.
            - Add-AzureRmApplicationGatewaySslPolicy.
            - New-AzureRmApplicationGatewaySslPolicy
            - Set-AzureRmApplicationGatewaySslPolicy
        - Добавлен командлет Get-AzureRmApplicationGatewayAvailableSslOptions (псевдоним: List-AzureRmApplicationGatewayAvailableSslOptions).
        - Добавлен командлет Get-AzureRmApplicationGatewaySslPredefinedPolicy (псевдоним: List-AzureRmApplicationGatewaySslPredefinedPolicy).
    * Добавлена поддержка перенаправления в шлюзе приложений.
        - Добавлен командлет Add-AzureRmApplicationGatewayRedirectConfiguration.
        - Добавлен командлет Get-AzureRmApplicationGatewayRedirectConfiguration.
        - Добавлен командлет New-AzureRmApplicationGatewayRedirectConfiguration.
        - Добавлен командлет Remove-AzureRmApplicationGatewayRedirectConfiguration.
        - Добавлен командлет Set-AzureRmApplicationGatewayRedirectConfiguration.
        - Добавлен необязательный параметр -RedirectConfiguration:
            - Add-AzureRmApplicationGatewayRequestRoutingRule
            - New-AzureRmApplicationGatewayRequestRoutingRule
            - Set-AzureRmApplicationGatewayRequestRoutingRule
        - Добавлен необязательный параметр -DefaultRedirectConfiguration:
            - Add-AzureRmApplicationGatewayUrlPathMapConfig
            - New-AzureRmApplicationGatewayUrlPathMapConfig
            - Set-AzureRmApplicationGatewayUrlPathMapConfig
        - Добавлен необязательный параметр -RedirectConfiguration:
            - Add-AzureRmApplicationGatewayPathRuleConfig;
            - New-AzureRmApplicationGatewayPathRuleConfig
            - Set-AzureRmApplicationGatewayPathRuleConfig.
        - Добавлен необязательный параметр -RedirectConfigurations:
            - New-AzureRmApplicationGateway
            - Set-AzureRmApplicationGateway
    * Добавлена поддержка службы "Веб-сайты Azure" в шлюзе приложений.
        - Добавлен командлет New-AzureRmApplicationGatewayProbeHealthResponseMatch.
        - Добавлены дополнительные параметры -PickHostNameFromBackendHttpSettings, -MinServers и -Match.
            - Add-AzureRmApplicationGatewayProbeConfig
            - New-AzureRmApplicationGatewayProbeConfig
            - Set-AzureRmApplicationGatewayProbeConfig
        - Добавлены дополнительные параметры -PickHostNameFromBackendAddress, -AffinityCookieName, -ProbeEnabled и -Path.
            - Add-AzureRmApplicationGatewayBackendHttpSettings
            - New-AzureRmApplicationGatewayBackendHttpSettings
            - Set-AzureRmApplicationGatewayBackendHttpSettings
    * Командлет Get-AzureRmPublicIPaddress обновлен для извлечения ресурсов publicipaddress, созданных с помощью масштабируемого набора виртуальных машин.
    * Добавлен командлет для получения текущих данных об использовании виртуальной сети:
        - Get-AzureRmVirtualNetworkUsageList.
* Профиль
    * Исправлена ошибка, возникавшая при использовании командлета Import-AzureRmContext или Save-AzureRmContext.
        - Дополнительные сведения можно найти в этом выпуске: https://github.com/Azure/azure-powershell/issues/3954.
* Службы восстановления. Site Recovery
    * Добавлен новый модуль для операций Azure Site Recovery.
        - Все его командлеты начинаются с AzureRmRecoveryServicesAsr*.
* SQL
    * В AzureRM.Sql добавлены командлеты PowerShell для синхронизации данных.
    * Командлеты AzureRmSqlServer обновлены для использования новой версии REST API, чтобы избежать истечения времени ожидания при создании сервера.
    * Объявлены нерекомендуемыми командлеты для обновления сервера, так как прежняя версия сервера (2.0) больше не существует.
    * В командлеты New-AzureRmSqlServer и Set-AzureRmSqlServer добавлен новый необязательный параметр AssignIdentity для поддержки инициализации удостоверения для ресурса SQL Server.
    * Параметр ResourceGroupName теперь является необязательным для командлета Get-AzureRmSqlServer.
        - Дополнительные сведения можно найти в этом выпуске: https://github.com/Azure/azure-powershell/issues/635.
* Управление службами для ExpressRoute:
    * В командлет New-AzureBgpPeering добавлены следующие новые возможности:
        - PeerAddressType: можно указать значение IPv4 или IPv6 для создания пиринга BGP соответствующего типа семейства адресов.
    * В командлет Set-AzureBgpPeering добавлены следующие новые возможности:
        - PeerAddressType: можно указать значение IPv4 или IPv6 для обновления пиринга BGP соответствующего типа семейства адресов.
    * В командлет Remove-AzureBgpPeering добавлены следующие новые возможности:
        - PeerAddressType: можно указать значение IPv4 или IPv6 для удаления пиринга BGP соответствующего типа семейства адресов.

## <a name="20170607---version-410"></a>07.06.2017: версия 4.1.0
* Analysis Services:
    * Добавлены новые номера SKU: B1, В2, S0.
    * Добавлена поддержка масштабирования.
* Cognitive Services:
    * Обновлена подробная информация о лицензионных соглашениях, отображаемая при создании ресурсов Cognitive Services.
* Среда выполнения приложений
    * Исправлен командлет Test-AzureRmVMAEMExtension для применения к виртуальным машинам с несколькими управляемыми дисками.
    * Обновлен командлет Set-AzureRmVMAEMExtension: добавлены сведения о кэшировании управляемых дисков уровня "Премиум".
    * Add-AzureRmVhd: ограничение размера VHD увеличено до 4 ТБ.
    * Stop-AzureRmVM: уточнено описание параметра STayProvisioned в документации.
    * New-AzureRmDiskUpdateConfig
      * Нерекомендуемые параметры: CreateOption, StorageAccountId, ImageReference, SourceUri, SourceResourceId.
    * Set-AzureRmDiskUpdateImageReference: нерекомендуемый командлет.
    * New-AzureRmSnapshotUpdateConfig
      * Нерекомендуемые параметры: CreateOption, StorageAccountId, ImageReference, SourceUri, SourceResourceId.
    * Set-AzureRmSnapshotUpdateImageReference: нерекомендуемый командлет.
* Data Lake Store
    * Enable-AzureRmDataLakeStoreKeyVault (Enable-AdlStoreKeyVault):
      * Включение управляемого шифрования Key Vault для Data Lake Store.
* DevTest Labs:
    * Обновлены командлеты для работы с текущей и обновленной версиями API DevTest Labs.
* Центр Интернета вещей:
    * Добавлена поддержка маршрутизации для командлетов Центра Интернета вещей.
* Хранилище ключей
  * Добавлены новые командлеты для поддержки управляемых ключей учетной записи хранения Key Vault:
    * Get-AzureKeyVaultManagedStorageAccount;
    * Add-AzureKeyVaultManagedStorageAccount;
    * Remove-AzureKeyVaultManagedStorageAccount;
    * Update-AzureKeyVaultManagedStorageAccount;
    * Update-AzureKeyVaultManagedStorageAccountKey;
    * Get-AzureKeyVaultManagedStorageSasDefinition;
    * Set-AzureKeyVaultManagedStorageSasDefinition;
    * Remove-AzureKeyVaultManagedStorageSasDefinition.
* Сеть
    * Get-AzureRmNetworkUsage: новый командлет для отображения сведений о загрузке и использовании сети.
    * Добавлены новые параметры GatewaySku для VirtualNetworkGateways:
        * Для VPN-шлюзов добавлены новые SKU: VpnGw1, VpnGw2, VpnGw3.
    * Set-AzureRmNetworkWatcherConfigFlowLog
      * Исправлены справочные примеры.
* NotificationHubs
    * Прозрачное обновление командлетов NotificationHubs для нового API.
* Профиль
    * Resolve-AzureRmError:
      * Новый командлет для отображения сведений об ошибках и исключениях, порождаемых командлетами, включая данные запросов и ответов сервера.
    * Send-Feedback:
      * Включение отправки отзывов без регистрации в журнале.
    * Get-AzureRmSubscription
      * Исправлена ошибка извлечения подписок CSP.
* Ресурсы
    * Исправлена проблема, из-за которой выполнение Get-AzureRMRoleAssignment приводило к ошибке "Недопустимый запрос", если число roleassignments было 1000.
        * Теперь пользователи могут использовать Get-AzureRMRoleAssignment, даже если возвращается больше 1000 значений roleassignments.
* SQL
    * Restore-AzureRmSqlDatabase: обновлен пример в документации.
* Хранилище
    * Добавлен параметр AssignIdentity для поддержки командлетов, предназначенных для учетных записей хранения в режиме ресурсов.
        * New-AzureRmStorageAccount;
        * Set-AzureRmStorageAccount.
    * Добавлена поддержка ключа клиента в командлетах, предназначенных для учетных записей хранения в режиме ресурсов.
        * Set-AzureRmStorageAccount.
        * New-AzureRmStorageAccountEncryptionKeySource.
* TrafficManager

    * Добавлены новые параметры Monitor: MonitorIntervalInSeconds, MonitorTimeoutInSeconds, MonitorToleratedNumberOfFailures.
    * В Monitor добавлен протокол TCP.
* Управление службами
    * Add-AzureVhd: ограничение размера VHD увеличено до 4 ТБ.
    * New-AzureBGPPeering: поддержка устаревшего режима.
* Azure.Storage;
    * Обновлена справка для параметров, которые принимают подстановочные знаки, а также обновлен тип StorageContext.

## <a name="20170523---version-402"></a>23.05.2017: версия 4.0.2
* Профиль
    * Add-AzureRmAccount
      * Добавлен псевдоним параметра `-EnvironmentName` для обеспечения обратной совместимости с версиями 2.x AzureRM.profile.

## <a name="20170512---version-401"></a>12.05.2017: версия 4.0.1
 * Устранена проблема с New-AzureStorageContext при использовании вне сети: https://github.com/Azure/azure-powershell/issues/3939.

## <a name="20170510---version-400"></a>10.05.2017: версия 4.0.0


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
