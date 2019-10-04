---
title: Заметки о выпуске Azure PowerShell
description: Узнайте обо всех последних обновлениях модулей Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/25/2019
ms.openlocfilehash: b879d970d3237098e481dba0419ee65efa8d51cd
ms.sourcegitcommit: f0f09eee03ef9dd7fe07432252a3dc8ca93e3a7b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "71319312"
---
## <a name="270---september-2019"></a>2.7.0 — сентябрь 2019 г.
#### <a name="azapimanagement"></a>Az.ApiManagement
* В справочной документации по командлету Set-AzApiManagementPolicy обновлено описание параметра -Format.
* Из справочной документации удалены ссылки на нерекомендуемый командлет Update-AzApiManagementDeployment. Вместо него следует использовать командлет Set-AzApiManagement.

#### <a name="azautomation"></a>Az.Automation
* В справочной документации по командлету Register-AzAutomationDscNode исправлена опечатка в примере.
* Добавлено уточнение об ограничениях ОС для командлета Register-AzAutomationDSCNode.
* Исправлено исключение пустой ссылки для параметра -Wait в командлете Start-AzAutomationRunbook.

#### <a name="azcompute"></a>Az.Compute
* Добавлен параметр UploadSizeInBytes для командлета New-AzDiskConfig.
* Добавлен добавочный параметр для командлета New-AzSnapshotConfig.
* Для виртуальной машины добавлены такие функции с низким приоритетом:
    - Для командлета New-AzVMConfig добавлены параметры MaxPrice, EvictionPolicy и Priority.
    - Для командлетов New-AzVmssConfig, Update-AzVM и Update-AzVmss добавлен параметр MaxPrice.
* Для командлета Get-AzAvailabilitySet устранена проблема со ссылкой на виртуальную машину, когда в нем перечисляются все группы доступности в подписке.
* Исправлено исключение NULL для командлета Get-AzRemoteDesktopFile.
* Исправлен метод поиска VHD для относительной конечной позиции.
* Устранена проблема с UltraSSD для командлетов New-AzVM и Update-AzVM.

#### <a name="azdatafactory"></a>Az.DataFactory
* Добавлены 3 новые команды для ADF версии 2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription и Get-AzDataFactoryV2TriggerSubscriptionStatus.
* Пакет SDK ADF для .NET обновлен до версии 4.1.3.

#### <a name="azhdinsight"></a>Az.HDInsight
* Укажите критические изменения.

#### <a name="aziothub"></a>Az.IotHub
* Добавлена поддержка для вызова отработки отказа для IotHub в георегион аварийного восстановления.
* Добавлена поддержка для управления обогащением сообщений для IotHub. Ниже перечислены новые командлеты:
    - Add-AzIotHubMessageEnrichment;
    - Get-AzIotHubMessageEnrichment;
    - Remove-AzIotHubMessageEnrichment;
    - Set-AzIotHubMessageEnrichment.

#### <a name="azmonitor"></a>Az.Monitor
* Указание на самую последнюю версию пакета SDK для монитора, т. е. 0.24.1-preview:
   - В командлеты метрик добавлены некритические изменения, т. е. перечисление единиц поддерживает несколько новых значений. Эти командлеты доступны только для чтения, поэтому входные данные командлетов не будут изменены.
   - Актуальная версия API запросов **ActionGroups** — **2019-06-01**. До этого была версия **2018-03-01**. Тесты сценария обновлены в соответствии с этим изменением.
   - В конструкторы классов **EmailReceiver** и **WebhookReceiver** добавлен один новый обязательный аргумент — логическое значение с именем **useCommonAlertSchema**. Сейчас для него установлено значение **false**, чтобы скрыть это критическое изменение от командлетов. **Примечание**. Это временное изменение, которое должно быть подтверждено командой оповещения.
   - Порядок аргументов для конструктора класса **Source** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK. Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.
   - Порядок аргументов для конструктора класса **AlertingAction** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK. Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.
* Добавлена поддержка критериев динамического порога для оповещения метрики версии 2:
    - New-AzMetricAlertRuleV2Criteria: теперь также позволяет создавать критерии динамического порога.
    - Add-AzMetricAlertRuleV2: теперь также позволяет принимать критерии динамического порога.
* Добавлены усовершенствования в командлетах запланированных правил запросов (SQR).
 - Командлеты будут принимать параметр Location в обоих форматах: расположение (например, eastus) или отображаемое имя расположения (например, "восточная часть США").
 - Параметр Enabled проиллюстрирован в файлах справки надлежащим образом.
 - Добавлены примеры для необязательного параметра ActionGroup.
 - Все файлы справки улучшены.
* Исправлена ошибка в определении типа области для командлета Set-AzActionRule.

#### <a name="aznetwork"></a>Az.Network
* Исправлен неправильный пример в справочной документации по командлету New-AzApplicationGateway. 
* В справочную документацию по командлету Get-AzNetworkWatcherPacketCapture добавлено примечание, посвященное извлечению всех свойств для записи пакетов.
* В справочной документации по командлету Test-AzNetworkWatcherIPFlow исправлен пример: теперь он правильно перечисляет сетевые карты.
* Улучшен анализ облачных исключений для отображения дополнительных сведений (при их наличии).
* Улучшен анализ облачных исключений для обработки дополнительного типа исключения SDK.
* Исправлено неправильное сопоставление моделей правил безопасности.
* Добавлены свойства сетевого интерфейса для компонента частного IP-адреса.
    - Для интерфейса PSNetworkInterface добавлено свойство PrivateEndpoint с типом PSResourceId.
    - В PSNetworkInterfaceIPConfiguration добавлено свойство PrivateLinkConnectionProperties с типом PSIpConfigurationConnectivityInformation.
    - Добавлен новый класс модели: PSIpConfigurationConnectivityInformation.
* Добавлен новый тип ApplicationRuleProtocolType "mssql" для ресурса Брандмауэра Azure.
* Поддержка многоканального подключения в Виртуальной глобальной сети:
    - Новые командлеты
        - New-AzVpnSiteLink;
        - New-AzVpnSiteLinkConnection;
    - Обновлен командлет:
        - New-VpnSite;
        - Update-VpnSite;
        - New-VpnConnection;
        - Update-VpnConnection.
* Исправлены документы с некоторыми примерами PowerShell для использования командлетов AZ вместо командлетов AzureRM.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Для объекта AzureVMpolicy добавлен новый атрибут — ProtectedItemsCount.
* Добавлены тесты для политики виртуальной машины и восстановления исходной учетной записи хранения.

#### <a name="azresources"></a>Az.Resources
* Исправлена ошибка, при которой не удавалось вызвать командлет New-AzRoleAssignment без параметра Scope.

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Исправлена опечатка в примере в справочной документации по командлету Update-AzServiceFabricReliability.
* Добавлены новые командлеты для управления приложениями и службами:
    - New-AzServiceFabricApplication;
    - New-AzServiceFabricApplicationType;
    - New-AzServiceFabricApplicationTypeVersion;
    - New-AzServiceFabricService;
    - Update-AzServiceFabricApplication;
    - Get-AzServiceFabricApplication;
    - Get-AzServiceFabricApplicationType;
    - Get-AzServiceFabricApplicationTypeVersion;
    - Get-AzServiceFabricService;
    - Remove-AzServiceFabricApplication;
    - Remove-AzServiceFabricApplicationType;
    - Remove-AzServiceFabricApplicationTypeVersion;
    - Remove-AzServiceFabricServic.
* Пакет SDK для Service Fabric обновлен до версии 1.2.0, в которой используется версия API 2019-03-01 поставщика ресурсов Service Fabric.

#### <a name="azsignalr"></a>Az.SignalR
* Добавлены командлеты Update, Restart, CheckNameAvailability и GetUsage.

#### <a name="azsql"></a>Az.Sql
* Обновлен пример в справочной документации по командлету Get-AzSqlElasticPool.
* Добавлен пример виртуального ядра для командлета создания эластичного пула (New-AzSqlElasticPool).
* Удалена проверка свойства EmailAddresses и того, что свойство EmailAdmins правильное в случае, если свойство EmailAddresses пустое в командлетах Set-AzSqlServerAdvancedThreatProtectionPolicy и Set-AzSqlDatabaseAdvancedThreatProtectionPolicy.
* Теперь, если существует несколько параметров диагностики, включающих категорию аудита, параметры аудита сервера и базы данных удаляются.
* Исправлена проверка адресов электронной почты в нескольких командлетах оценки уязвимостей SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting и Update-AzSqlInstanceVulnerabilityAssessmentSetting).

#### <a name="azstorage"></a>Az.Storage
* Обновлен пример в справочной документации по командлету Get-AzStorageAccountKey.
* Теперь при отправке и загрузке файла Azure в конечном файле сохраняются свойства SMB исходного файла (атрибуты файла, время создания файла, время последней записи файла).
    -  Set-AzStorageFileContent
    -  Get-AzStorageFileContent
* Исправлена операция отправки блочного BLOB-объекта, в которой происходили сбои свойств и метаданных в контейнере с включенной ImmutabilityPolicy.
    -  Set-AzStorageBlobContent
* Добавлена поддержка управления общими папками Azure в API плоскости управления с помощью таких командлетов:
    -  New-AzRmStorageShare;
    -  Get-AzRmStorageShare;
    -  Update-AzRmStorageShare;
    -  Remove-AzRmStorageShare.

#### <a name="azwebsites"></a>Az.Websites
* Устранена проблема, из-за которой теги webapp удалялись при переносе приложения в новый ASP.
* Теперь командлет Publish-AzureWebapp работает в Linux и Windows.
* Обновлен пример в справочной документации по командлету Get-AzWebAppPublishingProfile.

## <a name="260---august-2019"></a>2.6.0 — август 2019 г.
#### <a name="general"></a>Общие сведения
* Исправлены опечатки в модулях.

#### <a name="azaccounts"></a>Az.Accounts
* Добавлена поддержка назначаемого пользователем удостоверения MSI при проверке подлинности в Функциях Azure (№ 9479).

#### <a name="azaks"></a>Az.Aks
* Устранена проблема с выходными данными для Get-AzAks.
    * Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9847.

#### <a name="azapimanagement"></a>Az.ApiManagement
* исправлена проблема https://github.com/Azure/azure-powershell/issues/9351.
    - Обновлена версия NuGet для .NET, которая не накладывает ограничений на productId, apiId, groupId и userId.
* **Get-AzApiManagementProduct**. Добавлена поддержка запросов к продуктам с помощью API.
  https://github.com/Azure/azure-powershell/issues/9482
* **New-AzApiManagementApiRevision**. Устранена проблема, из-за которой не задавался параметр ApiRevisionDescription при создании новой редакции API https://github.com/Azure/azure-powershell/issues/9752.
* Исправлено написание имени модели c PsApiManagementOAuth2AuthrozationServer на PsApiManagementOAuth2AuthorizationServer.

#### <a name="azbatch"></a>Az.Batch
* Исправлена опечатка в написании Windows со строчной буквы в справочных сообщениях и документации.

#### <a name="azcdn"></a>Az.Cdn
* Исправлена опечатка во вспомогательном приложении модуля CDN.

#### <a name="azcompute"></a>Az.Compute
* Добавлен параметр VmssId в новый командлет Add New-AzVMConfig.
* Добавлены параметры TerminateScheduledEvents и TerminateScheduledEventNotBeforeTimeoutInMinutes в New-AzVmssConfig и Update-AzVmss.
* Добавлено свойство HyperVGeneration в объект образа виртуальной машины.
* Добавлены компоненты Host и HostGroup.
    - Новые командлеты:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost
    - Параметр HostId добавлен в New-AzVMConfig и New-AzVM.
* Исправлен пример в документации по Invoke-AzVMRunCommand, в котором теперь используется правильное имя параметра.
* Исправлено описание VolumeType в справочной документации по Set-AzVMDiskEncryptionExtension и Set-AzVmssDiskEncryptionExtension.

#### <a name="azdatafactory"></a>Az.DataFactory
* Исправлена опечатка в написании Windows со строчной буквы в документации по New-AzDataFactoryEncryptValue.
* Пакет SDK ADF для .NET обновлен до версии 4.1.2.
* Добавлены параметры DataProxyIntegrationRuntimeName, DataProxyStagingLinkedServiceName и DataProxyStagingPath в командлет Set-AzureRmDataFactoryV2IntegrationRuntime, что позволяет настраивать локальную среду выполнения интеграции в качестве прокси-сервера для Azure-SSIS Integration Runtime.
* Обновлены PSTriggerRun для отображения активированных конвейеров, сообщений и свойств и PSActivityRun для отображения типа действия.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Устранена проблема, при которой Get-DataLakeStoreDeletedItem переставал отвечать на запросы при возникновении ошибок или удаленных исключений.

#### <a name="azeventhub"></a>Az.EventHub
* Исправлена проблема № 9658: опечатка в написании параметра VirtualNteworkRule у Set-AzEventHubNetworkRuleSet.
* Исправлена проблема № 9558: в Set-AzEventHubNamespace используется PATCH вместо PUT.
* В командлет Set-AzEventHubNamespace добавлен параметр EnableKafka.
* Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.

#### <a name="azmarketplaceordering"></a>Az.MarketplaceOrdering
* Исправлено написание Azure со строчной буквы.

#### <a name="azmonitor"></a>Az.Monitor
* Исправлены неправильные имена параметров в справочной документации.

#### <a name="aznetwork"></a>Az.Network
* Обновлен New-AzPrivateLinkServiceIpConfig.
    - Параметр PublicIpAddress объявлен нерекомендуемым, так как он не используется на стороне сервера.
    - Добавлен необязательный параметр Primary, указывающий, является ли текущая IP-конфигурация основной.
* Улучшена обработка исключений из-за ошибок запроса от пакета SDK. Устранена проблема, при которой исключения пакета SDK не обрабатывались правильно, из-за чего не отображались основные сведения об ошибке.
* Настроена логика проверки для префикса IPv6 IP-адреса для проверки правильности длины префикса IPv6. 
* Обновлен Get-AzVirtualNetworkSubnetConfig: добавлен набор параметров для получения по идентификатору ресурса подсети.
* Обновлено описание параметра Location для AzNetworkServiceTag.

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Обновлена документация по New-AzOperationalInsightsLinuxSyslogDataSource.
    - Добавлен пример.
    - Обновлено описание параметра -Name.
* Добавлен пример для New-AzOperationalInsightsWindowsEventDataSource
* Изменено описание параметра -Name для New-AzOperationalInsightsWindowsEventDataSource.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Обновлен Get-AzRecoveryServicesBackupJobDetail.md.

#### <a name="azresources"></a>Az.Resources
* Добавлена поддержка новой версии API 2019-05-10 для Microsoft.Resource.
    - Добавлена поддержка copy.count = 0 для переменных, ресурсов и свойств.
    - Ресурсы, у которых condition = false или copy.count = 0, будут удаляться в полном режиме.
* В справочную документацию добавлен пример назначения политики на уровне подписки.

#### <a name="azservicebus"></a>Az.ServiceBus
* Исправлена проблема № 9658: опечатка в написании параметра VirtualNetworkRule В Set-AzServiceBusNetworkRuleSet.
* Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.
* Добавлена новая команда Test-AzServiceBusNameAvailability для проверки доступности имени для очереди и раздела. 

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Устранены ошибки командлета для добавления типа узла:
    - ошибка NullReferenceException, возникавшая, если у группы ресурсов были другие VMSS, не связанные с кластером Service Fabric. Исправлена проблема https://github.com/Azure/azure-powershell/issues/8681.
    - Исправлена ошибка, из-за которой командлет завершился сбоем, если virtualNetwork находилась не в той группе ресурсов, к которой относится кластер. Исправлена проблема https://github.com/Azure/azure-powershell/issues/8407.
    - Командлет Add-AzServiceFabricApplicationCertificate объявлен нерекомендуемым.

#### <a name="azsql"></a>Az.Sql
* Обновление документации по старым командлетам аудита.

#### <a name="azstorage"></a>Az.Storage
* Обновлена справка по Get/Close-AzStorageFileHandle: в примеры добавлены сценарии использования командлетов и обновлено описание параметров.
* Добавлена поддержка StandardBlobTier в операции отправки BLOB-объекта и копирования BLOB-объекта.
    -  Set-AzStorageBlobContent
    -  Start-AzStorageBlobCopy
* Добавлена поддержка приоритета восстановления в операцию копирования BLOB-объекта.
    -  Start-AzStorageBlobCopy

#### <a name="azwebsites"></a>Az.Websites
* Добавлены уточнение для параметра -AppSettings в Set-AzWebApp и Set-AzWebAppSlot.

## <a name="250---july-2019"></a>2.5.0 — июль 2019 г.
#### <a name="azaccounts"></a>Az.Accounts
* Обновлен общий код для использования последней версии ClientRuntime.

#### <a name="azapplicationinsights"></a>Az.ApplicationInsights
* Исправлена опечатка в примере в документации по Remove-AzApplicationInsightsApiKey. 

#### <a name="azautomation"></a>Az.Automation
* Исправлена опечатка в строке ресурса. 

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Добавлена поддержка NetworkRuleSet.

#### <a name="azcompute"></a>Az.Compute
* Добавлены недостающие свойства (ComputerName, OsName, OsVersion и HyperVGeneration) для объекта представления экземпляра виртуальной машины.

#### <a name="azcontainerregistry"></a>Az.ContainerRegistry
* Исправлена опечатка в Remove-AzContainerRegistryReplication для параметра репликации.
    - См. подробнее: https://github.com/Azure/azure-powershell/issues/9633.

#### <a name="azdatafactory"></a>Az.DataFactory
* Пакет SDK для ADF .NET обновлен до версии 4.1.0.
* Исправлена опечатка в документации по Get-AzDataFactoryV2PipelineRun.

#### <a name="azeventhub"></a>Az.EventHub
* Добавлен новый командлет для создания маркера SAS: New-AzEventHubAuthorizationRuleSASToken.
* Добавлена проверка и сообщение об ошибке для случаев, когда для правил авторизации назначаются только права "Управление".

#### <a name="azkeyvault"></a>Az.KeyVault
* Добавлена поддержка для настройки параметра KeySize в политиках сертификатов.

#### <a name="azlogicapp"></a>Az.LogicApp
* Get-AzIntegrationAccountMap теперь надлежащим образом выводит все типы сопоставлений.
    - Добавлен новый параметр MapType для фильтрации.

#### <a name="azmanagedservices"></a>Az.ManagedServices
* Добавлена поддержка API версии 2019-06-01 (общедоступная).

#### <a name="aznetwork"></a>Az.Network
* Добавлена поддержка частной конечной точки и службы приватного канала.
    - Новые командлеты
        - Set-AzPrivateEndpoint.
        - Set-AzPrivateLinkService.
        - Approve-AzPrivateEndpointConnection.
        - Deny-AzPrivateEndpointConnection.
        - Get-AzPrivateEndpointConnection.
        - Remove-AzPrivateEndpointConnection.
        - Test-AzPrivateLinkServiceVisibility.
        - Get-AzAutoApprovedPrivateLinkService.
* Обновлены следующие команды для функции: Флаг PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies в подсети в виртуальной сети.
    - Обновлены командлеты New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig.
        - Добавлен необязательный параметр -PrivateEndpointNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к частной конечной точке в этой подсети.
        - Добавлен необязательный параметр -PrivateLinkServiceNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к службе приватного канала в этой подсети.
* Параметр ServiceName командлета AzPrivateLinkService был переименован на Name с псевдонимом ServiceName для обеспечения обратной совместимости.
* Включен протокол ICMP для настройки правил безопасности сети.
    - Обновлены командлеты
        - Add-AzNetworkSecurityRuleConfig.
        - New-AzNetworkSecurityRuleConfig.
        - Set-AzNetworkSecurityRuleConfig.
* Добавлен ConnectionProtocolType (Ikev1/Ikev2) в качестве настраиваемого параметра для командлета New-AzVirtualNetworkGatewayConnection.
* Добавлен PrivateIpAddressVersion в LoadBalancerFrontendIpConfiguration.
    - Обновлен командлет:
        - New-AzLoadBalancerFrontendIpConfig.
        - Add-AzLoadBalancerFrontendIpConfig.
        - Set-AzLoadBalancerFrontendIpConfig.
* Команда New-AzApplicationGatewayProbeConfig Шлюза приложений обновлена для поддержки настраиваемого порта в зонде.
    - Обновлен командлет New-AzApplicationGatewayProbeConfig: добавлен необязательный параметр Port, который используется при проверке внутреннего сервера. Этот параметр применяется к номерам SKU Standard_V2 и WAF_V2.

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Обновленная версия по умолчанию для сохраненных операций поиска имеет значение 1. 
* Исправлены ошибки при обработке регулярных выражений со значениями NULL в журналах.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Обновлен файл Get-AzRecoveryServicesBackupJob.md.
* Обновлен файл Get-AzRecoveryServicesBackupContainer.md.
* Обновлен файл Get-AzRecoveryServicesVault.md.
* Обновлен файл Wait-AzRecoveryServicesBackupJob.md.
* Обновлен файл Set-AzRecoveryServicesVaultContext.md.
* Обновлен файл Get-AzRecoveryServicesBackupItem.md.
* Обновлен файл Get-AzRecoveryServicesBackupRecoveryPoint.md.
* Обновлен файл Restore-AzRecoveryServicesBackupItem.md.
* Обновлен вызов службы для отмены регистрации контейнера в общей папке Azure.
* Обновлен файл Set-AzRecoveryServicesAsrAlertSetting.md.

#### <a name="azresources"></a>Az.Resources
- Удален отсутствующий командлет, который упоминается в документации по New-AzResourceGroupDeployment.
- Обновлены командлеты политик для использования новой версии API 2019-01-01.

#### <a name="azservicebus"></a>Az.ServiceBus
* Добавлен новый командлет для создания маркера SAS: New-AzServiceBusAuthorizationRuleSASToken.
* Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".

#### <a name="azsql"></a>Az.Sql
* Исправлены отсутствующие примеры для командлета Set-AzSqlDatabaseSecondary.
* Исправлены заданные повторяющиеся проверки для оценки наличия уязвимостей без указания адресов электронной почты.
* Исправлена незначительная опечатка в сообщении предупреждения.

#### <a name="azstorage"></a>Az.Storage
* Обновлен пример в справочной документации для использования командлетом Get-AzStorageAccount правильного имени параметра.

#### <a name="azstoragesync"></a>Az.StorageSync
* Добавлен командлет Invoke-AzStorageSyncChangeDetection.
* Исправлена проблема № 9551, связанная с TierFilesOlderThanDays.

#### <a name="azwebsites"></a>Az.Websites
* Исправлена ошибка, при которой некоторые свойства SiteConfig не возвращались Get-AzWebApp и Set-AzWebApp.
* Добавлен новый параметр Location в Get-AzDeletedWebApp и Restore-AzDeletedWebApp.
* Исправлена ошибка, которая возникала при клонировании слотов веб-приложений с помощью командлета New-AzWebApp-IncludeSourceWebAppSlots.

## <a name="240---july-2019"></a>2.4.0 — июль 2019 г.
#### <a name="azaccounts"></a>Az.Accounts
* Добавлена поддержка командлетов профиля.
* Добавлена поддержка сред и плоскостей данных в созданных командлетах.
* Исправлена ошибка, когда в командлетах плоскости данных в Windows PowerShell в некоторых случаях использовалась неправильная конечная точка.

#### <a name="azadvisor"></a>Az.Advisor
* Выпущена общедоступная версия Az.Advisor.
* Теперь этот модуль входит в сводный модуль `Az`.

#### <a name="azapimanagement"></a>Az.ApiManagement
* исправлена проблема https://github.com/Azure/azure-powershell/issues/8671.
    - **Get-AzApiManagementSubscription**
        - Добавлена поддержка запрашивания подписок по пользователю и продукту.
        - Добавлена поддержка создания запросов с использованием области "/", "/apis", "/apis/echo-api".
* Исправлены проблемы https://github.com/Azure/azure-powershell/issues/9307 и https://github.com/Azure/azure-powershell/issues/8432.
    - **Import-AzApiManagementApi**
        - Добавлена поддержка указания ApiVersion и ApiVersionSetId при импорте API-интерфейсов.

#### <a name="azautomation"></a>Az.Automation
* Исправлена ошибка командлета Set-AzAutomationConnectionFieldValue при обработке строкового значения.

#### <a name="azcompute"></a>Az.Compute
* В New AzImageConfig добавлен параметр HyperVGeneration.

#### <a name="azdatafactory"></a>Az.DataFactory
* Обновление выходных данных командлетов ADF, предназначенных для получения числа выполнений действий, конвейеров и триггеров, для поддержки канала Select-Object.

#### <a name="azeventgrid"></a>Az.EventGrid
* Исправлена опечатка в документации по командлету New-AzEventGridSubscription.

#### <a name="aziothub"></a>Az.IotHub
* Добавлена поддержка повторного создания ключей политики авторизации.

#### <a name="aznetwork"></a>Az.Network
* К тегам общедоступного IP-адреса добавлен тег RoutingPreference.
* Улучшены примеры для справочной документации по командлету Get-AzNetworkServiceTag.

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyState.
    - Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9446.

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Исправленная модель источника данных CustomLog возвращена в командлет Get-AzOperationalInsightsDataSource.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Выпущено исправление для команды get-policy для виртуальных машин IaaS.

#### <a name="azresources"></a>Az.Resources
    - Исправлен текст справки по параметру Get-AzPolicyState -Top.
    - Добавлена поддержка разбиения по страницам на стороне клиента для Get-AzPolicyAlias.
    - Добавлены новые параметры для Set-AzPolicyAssignment, -PolicyParameters и -PolicyParametersObject.
    - Добавлен ряд обновлений документов и примеров для командлетов политик.

#### <a name="azservicebus"></a>Az.ServiceBus
* Исправление ошибки № 4938: командлет New-AzureRmServiceBusQueue возвращает ответ BadRequest (Недопустимый запрос) при задании значения MaxSizeInMegabytes.

#### <a name="azsql"></a>Az.Sql
* Из выпуска предварительной версии в выпуск общедоступной версии добавлены командлеты группы отработки отказа экземпляра.
* Поддержка аудита Azure SQL Server и баз данных с помощью новых командлетов:
    - Set-AzSqlServerAudit
    - Get-AzSqlServerAudit
    - Remove-AzSqlServerAudit
    - Set-AzSqlDatabaseAudit
    - Get-AzSqlDatabaseAudit
    - Remove-AzSqlDatabaseAudit
* Из параметров оценки уязвимостей удалены ограничения, касающиеся электронной почты.

#### <a name="azstorage"></a>Az.Storage
* Два параметра в указанном ниже командлете — -IndexDocument и -ErrorDocument404Path, — которые ранее были обязательными, стали необязательными:
    -  Enable-AzStorageStaticWebsite
* Обновлена справка по командлету Get-AzStorageBlobContent: добавлен пример.
* При сбое выполнения командлета с ошибкой StorageException отображаются дополнительные сведения об ошибке.
* Добавлена поддержка создания или обновления учетной записи хранения с использованием проверки подлинности AAD DS для службы "Файлы Azure".
    -  New-AzStorageAccount
    -  Set-AzStorageAccount
* Добавлена поддержка перечисления или закрытия дескрипторов файлов для общей папки, каталога файлов или файла:
    - Get-AzStorageFileHandle
    - Close-AzStorageFileHandle

#### <a name="azstoragesync"></a>Az.StorageSync
* Теперь этот модуль входит в сводный модуль `Az`.

## <a name="232---june-2019"></a>2.3.2 — июнь 2019 г.
#### <a name="azaccounts"></a>Az.Accounts
* Исправлена ошибка, связанная с использованием неправильного URL-адреса для вызовов функций.
    - Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8983.
* Устранена проблема с псевдонимами из AzureRM для командлетов Az.
  - Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic.
  - Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest.

#### <a name="azcompute"></a>Az.Compute
* Простые наборы параметров New-AzVm и New-AzVmss теперь принимают параметр ProximityPlacementGroup.
* Исправлена опечатка в справочной документации по New-AzVM.

#### <a name="azdns"></a>Az.Dns
* Исправлена опечатка в справочных примерах по использованию Set-AzDnsZone.

#### <a name="azeventgrid"></a>Az.EventGrid
* Обновлен для использования API версии 2019-06-01.
* Новые командлеты:
    - New-AzureRmEventGridDomain
        - Создает домен Сетки событий Azure.
    - Get-AzureRmEventGridDomain
        - Возвращает сведения о домене Сетки событий или список всех доменов Сетки событий в текущей подписке Azure.
    - Remove-AzureRmEventGridDomain
        - Удаляет домен Сетки событий Azure.
    - New-AzureRmEventGridDomainKey
        - Повторно создает ключ общего доступа для домена Сетки событий Azure.
    - Get-AzureRmEventGridDomainKey
        - Возвращает ключи общего доступа, используемые для публикации событий в домене Сетки событий.
    - New-AzureRmEventGridDomainTopic
        - Создает раздел домена Сетки событий Azure.
    - Get-AzureRmEventGridDomainTopic
        - Возвращает сведения о разделе домена Сетки событий или список всех разделов определенного домена Сетки событий в текущей подписке Azure. 
    - Remove-AzureRmEventGridDomainTopic
        - Удаляет раздел домена Сетки событий Azure.
* Обновлены командлеты:
    - New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription
        - Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для нового домена Сетки событий и раздела домена Сетки событий и позволяющие создавать подписки на события в этих ресурсах.
        - Добавляют новые обязательные параметры для указания имени нового домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют создавать подписки на события в этих ресурсах.
        - Добавляют новые наборы параметров для доменов и разделов домена и позволяют повторно использовать существующие параметры (например, EndPointType, SubjectBeginsWith и т. д.).
        - Добавлены новые необязательные параметры для указания:
            - срока действия подписки на событие;
            - параметров расширенной фильтрации.
        - Добавляют новое перечисление для ServiceBusQueue в качестве места назначения.
        - Запрещают использование значение All в параметре -IncludedEventType и заменяют его следующим: 
    - Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription
        - Добавляют новые необязательные параметры (Top, ODataQuery и NextLink) для поддержки разбиения на страницы и фильтрации результатов.
    - Remove-AzureRmEventGridSubscription
        - Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для домена Сетки событий и раздела домена Сетки событий и позволяющие удалять подписки на события в этих ресурсах.
        - Добавляют новые обязательные параметры для указания имени домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют удалять подписки на события в этих ресурсах.

#### <a name="azfrontdoor"></a>Az.FrontDoor
* New-AzFrontDoorWafMatchConditionObject
    - Добавляет поддержку преобразований и новое значение оператора автозавершения (RegEx).
* New-AzFrontDoorWafManagedRuleObject
    - Добавляет новые значения автозавершения.

#### <a name="aznetwork"></a>Az.Network
* Добавляет поддержку ресурса шлюза виртуальной сети.
    - Новые командлеты
        - Get-AzVirtualNetworkGatewayVpnClientConnectionHealth
* Добавляет AvailablePrivateEndpointType.
    - Новые командлеты 
        - Get-AzAvailablePrivateEndpointType
* Добавляет PrivatePrivateLinkService.
    - Новые командлеты 
        - Get-AzPrivateLinkService 
        - New-AzPrivateLinkService
        - Remove-AzPrivateLinkService
        - New-AzPrivateLinkServiceIpConfig
        - Set-AzPrivateEndpointConnection
* Добавляет PrivateEndpoint.
    - Новые командлеты
        - Get-AzPrivateEndpoint
        - New-AzPrivateEndpoint
        - Remove-AzPrivateEndpoint
        - New-AzPrivateLinkServiceConnection
* Обновлены следующие команды для функции: флаг UseLocalAzureIpAddress для VPN-подключения.
    - Обновлен командлет New-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.
    - Обновлен командлет Set-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.
* В пиринг ExpressRoute добавлено поле только для чтения PeeredConnections.
* В ExpressRoute добавлено поле только для чтения GlobalReachEnabled.
* Добавлен атрибут в рамках критического изменения, отменяющего статус устаревшего поля AllowGlobalReach в модели ExpressRouteCircuit.
* Исправлена проблема, связанная с ошибкой 8756, при использовании TargetListenerID с командлетами AzApplicationGatewayRedirectConfiguration.
* Исправлена ошибка в New-AzApplicationGatewayPathRuleConfig, не позволявшая задавать набор правил повторного создания.
* Исправлено отображение VirtualNetworkTaps в NetworkInterfaceIpConfiguration.
* Исправлены командлеты Cortex Get для отображения всех частей.
* Исправлено создание ссылок VirtualHub для ExpressRouteGateways и VpnGateway.
* В AzureFirewall и NatGateway добавлена поддержка Зон доступности.
* Добавлен командлет Get-AzNetworkServiceTag.
* Добавлена поддержка нескольких общедоступных IP-адресов для Брандмауэра Azure.
    - Обновлен командлет New-AzFirewall:
        - Добавлен параметр -PublicIpAddress, который принимает один или несколько объектов общедоступных IP-адресов.
        - Добавлен параметр -VirtualNetwork, который принимает объект виртуальной сети.
        - Добавлены методы AddPublicIpAddress и RemovePublicIpAddress для объекта брандмауэра. Они принимают объект общедоступного IP-адреса в качестве входных данных.
        - Не рекомендуется использовать параметры -PublicIpName и -VirtualNetworkName. 
* Обновлены следующие команды для функции: В параметрах проверки подлинности AAD VPN-клиента задан ресурс шлюза виртуальной сети. 
    - Обновлен командлет New-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.
    - Обновлен командлет Set-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.
    - Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр-переключатель RemoveAadAuthentication для удаления в шлюзе параметров проверки подлинности AAD VPN-клиента.

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Добавлена поддержка SKU **pergb2018** в команде New-AzureRmOperationalInsightsWorkspace.

#### <a name="azresources"></a>Az.Resources
* Поддержка дополнительных вариантов экспорта шаблона.
    - В Export-AzResourceGroup добавлен параметр -SkipResourceNameParameterization.
    - В Export-AzResourceGroup добавлен параметр -SkipAllParameterization.
    - В Export-AzResourceGroup добавлен параметр -Resource для фильтрации экспортированных ресурсов.

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Исправлена ошибка, связанная с получением иногда неправильных отпечатков при добавлении сертификата ByExistingKeyVault.

#### <a name="azsql"></a>Az.Sql
* Исправлен суффикс конечной точки хранилища службы "Расширенная защита от угроз Azure".
* Исправлена ошибка, связанная с возможностью пакета "Расширенная защита данных" переопределять политику службы "Расширенная защита от угроз".
* Новые командлеты для Management.Sql позволяют клиентам добавлять ключи TDE и задавать средство защиты TDE для управляемых экземпляров.
   - Add-AzSqlInstanceKeyVaultKey
   - Get-AzSqlInstanceKeyVaultKey
   - Remove-AzSqlInstanceKeyVaultKey
   - Get-AzSqlInstanceTransparentDataEncryptionProtector
   - Set-AzSqlInstanceTransparentDataEncryptionProtector

#### <a name="azstorage"></a>Az.Storage
* Поддержка класса Kind в FileStorage и значения Premium_ZRS в SkuName при создании учетной записи хранения.
    - New-AzStorageAccount
* Уточнено описание командлета неизменности BLOB-объектов.
    -  Remove-AzRmStorageContainerImmutabilityPolicy

#### <a name="azwebsites"></a>Az.Websites
* Оптимизирует Get-AzWebAppCertificate для фильтрации по группе ресурсов на сервере, а не в клиенте.
* Добавляет параметр-переключатель - UseDisasterRecovery в Get AzWebAppSnapshot.

## <a name="220---june-2019"></a>2.2.0 — июнь 2019 г.
#### <a name="azcdn"></a>Az.Cdn
* Обновлены командлеты для поддержки функции rulesEngine на основе API версии 2019-04-15.

#### <a name="azcompute"></a>Az.Compute
* Добавлен параметр `NoWait`, который запускает операцию и немедленно возвращает значение еще до завершения операции.
    - Обновлены командлеты:   Export-AzLogAnalyticRequestRateByInterval; Export-AzLogAnalyticThrottledRequest; Remove-AzVM; Remove-AzVMAccessExtension; Remove-AzVMAEMExtension; Remove-AzVMChefExtension; Remove-AzVMCustomScriptExtension; Remove-AzVMDiagnosticsExtension; Remove-AzVMDiskEncryptionExtension; Remove-AzVMDscExtension; Remove-AzVMSqlServerExtension; Restart-AzVM; Set-AzVM; Set-AzVMAccessExtension; Set-AzVMADDomainExtension; Set-AzVMAEMExtension; Set-AzVMBginfoExtension; Set-AzVMChefExtension; Set-AzVMCustomScriptExtension; Set-AzVMDiagnosticsExtension; Set-AzVMDscExtension; Set-AzVMExtension; Start-AzVM; Stop-AzVM; Update-AzVM.

#### <a name="azeventhub"></a>Az.EventHub
* Исправлена ошибка № 9231. Командлет Get-AzEventHubNamespace не возвращал теги.
* Исправлена ошибка № 9230. Командлет Get-AzEventHubNamespace возвращал значение ResourceGroup вместо ResourceGroupName.

#### <a name="aznetwork"></a>Az.Network
* Обновлены параметры ResourceId и InputObject для ресурса Шлюза NAT.
    - Добавлены псевдонимы для параметров ResourceId и InputObject.

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyEvent.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Минимальный срок хранения политики IaaSVM изменился с 1 до 7 дней.

#### <a name="azservicebus"></a>Az.ServiceBus
* Исправлена ошибка № 9182. Командлет Get-AzServiceBusNamespace возвращал ResourceGroup вместо ResourceGroupName.

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Исправлена опечатка в сообщении об ошибке для командлета Update-AzServiceFabricReliability.
* Исправлен отсутствующей символ в командных строках Service Fabric.

#### <a name="azsql"></a>Az.Sql
* Для командлета New-AzureSqlInstance добавлен параметр DnsZonePartner, обеспечивающий поддержку AutoDr для Управляемого экземпляра.
* Командлет Get-AzSqlDatabaseSecureConnectionPolicy объявлен неподдерживаемым.
* Командлеты обнаружения угроз переименованы в командлеты Расширенной защиты от угроз.
* Параметры -StorageSizeInGB и -LicenseType командлета New-AzSqlInstance теперь необязательны.

#### <a name="azwebsites"></a>Az.Websites
* Исправлены проблемы, когда удалялись теги при использовании Set-AzWebApp и Set-AzWebAppSlot со свойством -WebApp.

## <a name="210---may-2019"></a>2.1.0 — май 2019 г.
#### <a name="azapimanagement"></a>Az.ApiManagement
* Созданы командлеты для управления диагностикой в глобальной области и в области API.
    - **Get-AzApiManagementDiagnostic** — получение диагностики, заданной глобально или на уровне области API.
    - **New-AzApiManagementDiagnostic** — создание диагностики в глобальной области или в области API.
    - **New-AzApiManagementHttpMessageDiagnostic** — создание параметра диагностики, для которого регистрируются заголовки и размер байтов тела.
    - **New-AzApiManagementPipelineDiagnosticSetting** — создание параметров диагностики для сообщений HTTP, поступающих в шлюз или исходящих из него.
    - **New-AzApiManagementSamplingSetting** — создание параметра выборки для запросов и ответов касательно диагностики.
    - **Remove-AzApiManagementDiagnostic** — удаление объекта диагностики в глобальной области или в области API.
    - **Set-AzApiManagementDiagnostic** — обновление объекта диагностики в глобальной области или в области API.
* Созданы командлеты для управления кэшем в службе ApiManagement.
    - **Get-AzApiManagementCache** — получение сведений о кэше, указанном идентификатором, или обо всех кэшах.
    - **New-AzApiManagementCache** — создание кэша по умолчанию или кэша в определенном регионе Azure.
    - **Remove-AzApiManagementCache** — удаление кэша.
    - **Update-AzApiManagementCache** — обновление кэша.
* Созданы командлеты для управления схемой API.
    - **New-AzApiManagementSchema** — создание схемы для API.
    - **Get-AzApiManagementSchema** — получение схем, настроенных в API.
    - **Remove-AzApiManagementSchema** — удаление схемы, настроенной в API.
    - **Set-AzApiManagementSchema** — обновление схемы, настроенной в API.
* Создан командлет для создания токена пользователя. 
    - **New-AzApiManagementUserToken** — создание токена пользователя, по умолчанию действительного в течение 8 часов. С помощью этого командлета можно создавать токен для пользователя GIT.
* Создан командлет для получения состояния сети.
    - **Get-AzApiManagementNetworkStatus** — получение состояния сети ресурсов, от которых зависит служба "Управление API". Это полезно при развертывании службы ApiManagement в виртуальной сети и проверке того, не нарушена ли какая-либо из зависимостей.
* Обновлен командлет **New-AzApiManagement** для управления службой ApiManagement. 
    - Добавлена поддержка нового SKU Consumption.
    - Добавлена поддержка для включения флага EnableClientCertificate в SKU Consumption.
    - Новый командлет **New-AzApiManagementSslSetting** позволяет настраивать параметр TLS/SSL для сервера (Backend) и внешнего интерфейса (Frontend). Его также можно использовать для настройки Ciphers как 3DES, в ServerProtocols как Http2 для внешнего интерфейса (Frontend) службы ApiManagement.
    - Добавлена поддержка настройки имени узла DeveloperPortal в службе ApiManagement.
* Обновлен командлет **Get-AzApiManagementSsoToken** для извлечения объекта PsApiManagement в качестве входных данных.
* Обновлен командлет для отображения встроенных сообщений об ошибках. 
     > PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Код ошибки: ValidationError. Сообщение об ошибке: "Некоторые поля содержат неправильные значения". Сведения об ошибке: [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]
* Обновлен командлет **Export-AzApiManagementApi** для экспортирования программных интерфейсов в формате OpenApi 3.0.
* Обновлен командлет **Import-AzApiManagementApi**:
    - Для импортирования API из спецификации документа OpenApi 3.0.
    - Для переопределения свойства PsApiManagementSchema, указанного в любом документе (Swagger, Wadl, Wsdl, OpenApi).
    - Для переопределения свойства ServiceUrl, указанного в любом документе.
* Обновлен командлет **Get-AzApiManagementPolicy** для возврата политики в формате, экранированном не для XML, с использованием rawxml.
* Обновлен командлет **Set-AzApiManagementPolicy**. Он принимает политику в формате, экранированном не для XML, с использованием rawxml и в формате, экранированном для XML, с использованием XML.
* Обновлен командлет **New-AzApiManagementApi**: 
    - Для настройки API с помощью сервера авторизации OpenId.
    - Для создания API в ApiVersionSet.
    - Для клонирования API с использованием значений SourceApiId и SourceApiRevision.
    - Возможность настройки параметра SubscriptionRequired в области API. 
* Обновлен командлет **Set-AzApiManagementApi**:
    - Для настройки API с помощью сервера авторизации OpenId.
    - Для обновления API в ApiVersionSet.    
    - Возможность настройки параметра SubscriptionRequired в области API. 
* Обновлен командлет **New-AzApiManagementRevision**:
    - Для клонирования (копирования тегов, продуктов, операций и политик) существующей редакции с использованием SourceApiRevision. Новая редакция предполагает родительский идентификатор ApiId.
    - Для предоставления ApiRevisionDescription.
    - Для переопределения значения ServiceUrl при клонировании API.
* Обновлен командлет **New-AzApiManagementIdentityProvider**:
    - Для настройки AAD или AADB2C с Authority.
    - Для установки политик SignupPolicy, SigninPolicy, ProfileEditingPolicy и PasswordResetPolicy.
* Обновлен командлет **New-AzApiManagementSubscription**.
    - Для учета новой модели SubscriptonModel с помощью Scope и UserId.
    - Для учета прежней модели подписки с помощью ProductId и UserId.
    - Добавлена поддержка для включения AllowTracing на уровне подписки.
* Обновлен командлет **Set-AzApiManagementSubscription**.
    - Для учета новой модели SubscriptonModel с помощью Scope и UserId.
    - Для учета прежней модели подписки с помощью ProductId и UserId.
    - Добавлена поддержка для включения AllowTracing на уровне подписки.
* Следующие командлеты обновлены, чтобы принимать значение ResourceId в качестве входных данных.
    - New-AzApiManagementContext.
        > New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso
    - Get-AzApiManagementApiRelease.
        > Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId
    - Get-AzApiManagementApiVersionSet.
        > Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset
    - Get-AzApiManagementAuthorizationServer.
    - Get-AzApiManagementBackend.
        > Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric
    - Get-AzApiManagementCertificate. 
    - Remove-AzApiManagementApiVersionSet.
    - Remove-AzApiManagementSubscription.

#### <a name="azautomation"></a>Az.Automation
* Обновлен командлет Get-AzAutomationJobOutputRecord для обработки значений в формате JSON и в виде текстовой записи.
    - исправлена проблема https://github.com/Azure/azure-powershell/issues/7977.
    - исправлена проблема https://github.com/Azure/azure-powershell/issues/8600.
* Поведение командлета Start-AzAutomationDscCompilationJob изменено так, чтобы сразу же запустить задание, а не ждать его завершения.
    * исправлена проблема https://github.com/Azure/azure-powershell/issues/8347.
* Исправлен командлет Get-AzAutomationDscNode, возвращающий все узлы при использовании -Name. Теперь он возвращает только соответствующий узел.

#### <a name="azcompute"></a>Az.Compute
* Добавлены параметры ProtectFromScaleIn и ProtectFromScaleSetAction для командлета Update-AzVmssVM.
* Командлет New-AzVM с простым набором параметров теперь по умолчанию использует доступное расположение, если регион "восточная часть США" не поддерживается.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Обновлен пакет SDK ADLS для использования httpclient. В инфраструктуру Azure интегрирована проверка плоскости данных.

#### <a name="azmonitor"></a>Az.Monitor
* Исправлены неправильные имена параметров в справочных примерах.

#### <a name="aznetwork"></a>Az.Network
* Добавлен флаг DisableBgpRoutePropagation для выходных данных действующей таблицы маршрутов.
    - Обновлен командлет:
        - Get-AzEffectiveRouteTable.
* Исправлен двойной дефис в документации New-AzApplicationGatewayTrustedRootCertificate.

#### <a name="azresources"></a>Az.Resources
* Добавлен новый командлет Get-AzureRmDenyAssignment для получения запрещающих назначений.

#### <a name="azsql"></a>Az.Sql
* Командлеты Расширенной защиты от угроз переименованы на командлеты Расширенной защиты данных, и оценка уязвимости включена по умолчанию.

## <a name="200---may-2019"></a>2.0.0 — май 2019 г.
#### <a name="azaccounts"></a>Az.Accounts
* Обновлена библиотека аутентификации для устранения проблем с ADFS при использовании аутентификации на основе имени пользователя и пароля.

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Отображается только заявление об отказе Bing для служб Поиска Bing.
* Исправлена проблема с созданием учетной записи.

#### <a name="azcompute"></a>Az.Compute
* Функция группы размещения близкого взаимодействия.
    - Добавлены следующие новые командлеты:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup
    - Новый параметр ProximityPlacementGroupId будет добавлен в следующие командлеты:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig
* В командлет New-AzGalleryImageVersion добавлен параметр StorageAccountType.
* TargetRegion в командлете New-AzGalleryImageVersion может содержать StorageAccountType.
* Параметр-переключатель SkipShutdown добавлен в командлеты Stop-AzVM и Stop-AzVmss.       
* Критические изменения
    - Командлет SET-AzVMBootDiagnostics изменен на Set-AzVMBootDiagnostic.
    - Командлет Export-AzLogAnalyticThrottledRequests изменен на Export-AzLogAnalyticThrottledRequests.

#### <a name="azdeploymentmanager"></a>Az.DeploymentManager
* Первая общедоступная версия командлетов диспетчера развертывания Azure

#### <a name="azdns"></a>Az.Dns
* Автоматическое делегирование DNS-сервера
    - Командлет для создания зоны DNS принимает имя родительской зоны в качестве дополнительного необязательного параметра.
    - Он добавляет записи NS в родительской зоне для созданной дочерней зоны.

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Первая общедоступная версия командлетов Azure FrontDoor.
* Переименованы командлеты WAF для включения Waf.
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a>Az.HDInsight
* Удалены два командлета:
    - Grant-AzHDInsightHttpServicesAccess
    - Revoke-AzHDInsightHttpServicesAccess
* Добавлен новый командлет Set-AzHDInsightGatewayCredential для замены Grant-AzHDInsightHttpServicesAccess.
* Обновлен командлет Get-AzHDInsightJobOutput для различения ролей читателя и оператора HDInsight:
    - Пользователям с ролью читателя не нужно указывать параметр DefaultStorageAccountKey явным образом, иначе возникает ошибка.
    - На пользователей с ролью оператора HDInsight это не повлияет.

#### <a name="azmonitor"></a>Az.Monitor
* Новые командлеты для API SQR (запланированное правило запросов)  
    - New-AzScheduledQueryRuleAlertingAction
    - New-AzScheduledQueryRuleAznsActionGroup
    - New-AzScheduledQueryRuleLogMetricTrigger
    - New-AzScheduledQueryRuleSchedule
    - New-AzScheduledQueryRuleSource
    - New-AzScheduledQueryRuleTriggerCondition
    - New-AzScheduledQueryRule
    - Get-AzScheduledQueryRule
    - Set-AzScheduledQueryRule
    - Update-AzScheduledQueryRule
    - Remove-AzScheduledQueryRule
    - См. подробнее об [API SQR](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules).
    - Обновлен файл Az.Monitor.md для включения командлетов для правила генерации оповещений на основе метрик GenV2(не классическая версия).

#### <a name="aznetwork"></a>Az.Network
* Добавлена поддержка для ресурса Шлюза NAT.
    - Новые командлеты
        - New-AzNatGateway
        - Get-AzNatGateway
        - Set-AzNatGateway
        - Remove-AzNatGateway
   - Обновлены командлеты
        - New-AzureVirtualNetworkSubnetConfigCommand
        - Add-AzureVirtualNetworkSubnetConfigCommand
* Обновлены следующие команды для функции: Настройка и удаление пользовательских маршрутов через шлюз в Бруклине.
    - Обновлен командлет New-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.
    - Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Добавлена поддержка сведений об оценке политики запросов.
    - Добавлен параметр -Expand в командлет Get-AzPolicyState. Добавлена поддержка -Expand PolicyEvaluationDetails.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Добавлена поддержка перекрестной подписки на Azure Site Recovery.
* Добавлена возможность отмечать предстоящие критически важные изменения для Azure Site Recovery.
* Исправлены план восстановления и план действий для Azure Site Recovery.
* Исправлено сетевое сопоставление обновления Azure Site Recovery (Azure — Azure).
* Исправлено направление защиты обновления Azure Site Recovery для управляемых дисков (Azure — Azure).
* Добавлены другие незначительные исправления.

#### <a name="azrelay"></a>Az.Relay
* Исправлены опечатки в сообщениях для клиентов.

#### <a name="azservicebus"></a>Az.ServiceBus
* Добавлены новые командлеты для NetworkRuleSet пространства имен.

#### <a name="azstorage"></a>Az.Storage
* Выполнено обновление клиентской библиотеки хранилища до версии 10.0.1 (пространство имен всех объектов из этого пакета SDK изменено с Microsoft.WindowsAzure.Storage. *на Microsoft.Azure.Storage*).
* Выполнено обновление до Microsoft.Azure.Management.Storage версии 11.0.0 для включения поддержки нового API версии 2019-04-01.
* Значение свойства Kind по умолчанию в учетной записи хранения изменено со Storage на StorageV2.
    - New-AzStorageAccount
* Изменено значение Sku.Name в выходных данных командлета учетной записи хранения в соответствии со значением Sku.Name во входных данных путем добавления _ (например, StandardLRS изменено на Standard_LRS).
    - New-AzStorageAccount
    - Get-AzStorageAccount
    - Set-AzStorageAccount

#### <a name="azwebsites"></a>Az.Websites
* Свойство Kind теперь будет задаваться объектам PSSite, возвращаемым командлетом Get-AzWebApp.
* Get-AzWebApp*Metrics и Get-AzAppServicePlanMetrics считаются нерекомендуемыми.

## <a name="180---april-2019"></a>1.8.0 — апрель 2019 г.
### <a name="highlights-since-the-last-major-release"></a>Основные возможности с момента последнего основного выпуска
* Общедоступная версия модуля `Az`.
* Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce
* Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/
* Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.
* Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.
* Добавлена поддержка для модулей runbook Python 2 в Az.Automation.
* Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:

#### <a name="azaccounts"></a>Az.Accounts
* Обновлен командлет Uninstall-AzureRm для правильного удаления модулей в Mac.

#### <a name="azbatch"></a>Az.Batch
* Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.

#### <a name="azcdn"></a>Az.Cdn
* Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.

#### <a name="azcompute"></a>Az.Compute
* Устранена проблема с установкой AEM, если в идентификаторах ресурсов дисков группа ресурсов указана в нижнем регистре.
* Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.
* Исправлена документация по подстановочным знакам.

#### <a name="azdatafactory"></a>Az.DataFactory
* Добавлены свойства SsisProperties, если NodeCount не имеет значения NULL для управляемой среды выполнения интеграции.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.

#### <a name="azeventgrid"></a>Az.EventGrid
* Обновлен текст справки для конечной точки, указывающий, что необходимо создать ресурсы, прежде чем использовать командлеты для создания или обновления подписки на события.

#### <a name="azeventhub"></a>Az.EventHub
* Добавлены новые командлеты для NetworkRuleSet пространства имен. 

#### <a name="azhdinsight"></a>Az.HDInsight
* Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.

#### <a name="aziothub"></a>Az.IotHub
* Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.

#### <a name="azkeyvault"></a>Az.KeyVault
* Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.
* Исправлена документация по подстановочным знакам.

#### <a name="azmachinelearning"></a>Az.MachineLearning
* Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.

#### <a name="azmedia"></a>Az.Media
* Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.

#### <a name="azmonitor"></a>Az.Monitor
  * Добавлены новые командлеты для правила генерации оповещений на основе метрик GenV2 (не классических).
      - New-AzMetricAlertRuleV2DimensionSelection
      - New-AzMetricAlertRuleV2Criteria
      - Remove-AzMetricAlertRuleV2
      - Get-AzMetricAlertRuleV2
      - Add-AzMetricAlertRuleV2
  * Обновлен пакет SDK Monitor до предварительной версии 0.22.0.

#### <a name="aznetwork"></a>Az.Network
* Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.
* Исправлена документация по подстановочным знакам.

#### <a name="aznotificationhubs"></a>Az.NotificationHubs
* Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.

#### <a name="azpowerbiembedded"></a>Az.PowerBIEmbedded
* Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.
* Обновлен табличный формат для SQL на виртуальной машине Azure.
* Добавлен альтернативный метод для получения расположения в Общей папке Azure.
* Обновлено значение ScheduleRunDays в объекте SchedulePolicy в соответствии с часовым поясом.

#### <a name="azrediscache"></a>Az.RedisCache
* Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.

#### <a name="azresources"></a>Az.Resources
* Исправлена документация по подстановочным знакам.

#### <a name="azsql"></a>Az.Sql
* Заменена зависимость от пакета SDK монитора на обычный код.
* Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.
* Улучшен процесс классификации нескольких столбцов.
* Добавлены свойства SKU (имя, семейство, производительность SKU) в отклике Get-AzSqlServerServiceObjective, а также по умолчанию задан табличный формат.
* C помощью Get-AzSqlServerServiceObjective теперь можно получать список доступных целевых служб по расположению без необходимости заранее размещать сервер в регионе.
* Поддерживается параметр часового пояса при создании Управляемого экземпляра.
* Исправлена документация по подстановочным знакам.

#### <a name="azwebsites"></a>Az.Websites
* Исправлены командлеты Set-AzWebApp и Set-AzWebAppSlot, которые теперь не удаляют теги при выполнении.
* Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.
* Обновлен пакет SDK веб-узлов.
* Удалено свойство AdminSiteName из PSAppServicePlan.

## <a name="170---april-2019"></a>1.7.0 —апрель 2019 г.
### <a name="highlights-since-the-last-major-release"></a>Основные возможности с момента последнего основного выпуска
* Общедоступная версия модуля `Az`.
* Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce
* Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/
* Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.
* Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.
* Добавлена поддержка для модулей runbook Python 2 в Az.Automation.
* Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:

#### <a name="azaccounts"></a>Az.Accounts
* Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметр AzureAnalysisServicesEndpointResourceId.

#### <a name="azanalysisservices"></a>Az.AnalysisServices
* Использование ServiceClient в командлетах плоскости данных и удаление исходной логики проверки подлинности.
* Add-AzureASAccount используется как оболочка для Connect-AzAccount во избежание критических изменений.

#### <a name="azautomation"></a>Az.Automation
* Исправлена ошибка командлета New-AzAutomationSoftwareUpdateConfiguration, связанная с включением. Теперь параметры IncludedKbNumber и IncludedPackageNameMask должны работать нормально.
* Исправлена ошибка динамической группы управления обновлениями службы автоматизации Azure.

#### <a name="azcompute"></a>Az.Compute
* В командлеты New-AzDiskConfig и New-AzSnapshotConfig добавлен параметр HyperVGeneration.
* Теперь можно создавать виртуальные машину на основе образов из коллекции от других клиентов. 

#### <a name="azcontainerinstance"></a>Az.ContainerInstance
* Исправлена проблема в параметре -Command командлета New-AzContainerGroup, из-за которой в конце добавлялся пустой аргумент.

#### <a name="azdatafactory"></a>Az.DataFactory
* Пакет SDK для ADF .NET обновлен до версии 3.0.2.
* Командлет Set-AzDataFactoryV2 обновлен с помощью дополнительных параметров для настроек, связанных с RepoConfiguration.

#### <a name="azresources"></a>Az.Resources
* Улучшена обработка поставщиков Get-AzResource при предоставлении параметров -ResourceId или -ResourceGroupName, -Name и -ResourceType.
* Улучшена обработка ошибок в командлетах Test-AzDeployment и Test-AzResourceGroupDeployment.
    - Теперь ошибки, возникающие за пределами проверки развертывания, обрабатываются и включаются в выходные данные команды.
    - Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.
* Добавлен параметр-переключатель -IgnoreDynamicParameters, с помощью которого можно настроить командлеты развертывания так, чтобы они пропускали запросы в сценариях скриптов и заданий.
    - Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.

#### <a name="azsql"></a>Az.Sql
* Поддержка классификации данных в базе данных.

#### <a name="azstorage"></a>Az.Storage
* Подробные сообщения об ошибке передаются при создании контекста хранилища с помощью параметра -UseConnectedAccount, но без входа в учетную запись Azure.
    - New-AzStorageContext
* Поддержка свойств службы управления BLOB-объектов в указанной учетной записи хранения с помощью API плоскости управления.
    - Update-AzStorageBlobServiceProperty
    - Get-AzStorageBlobServiceProperty
    - Enable-AzStorageBlobDeleteRetentionPolicy
    - Disable-AzStorageBlobDeleteRetentionPolicy
* Поддержка параметра -AsJob в командлетах для отправки и скачивания больших двоичных объектов и файлов.
    - Get-AzStorageBlobContent
    - Set-AzStorageBlobContent
    - Get-AzStorageFileContent
    - Set-AzStorageFileContent

## <a name="160---march-2019"></a>1.6.0 — март 2019 г.
### <a name="highlights-since-the-last-major-release"></a>Основные возможности с момента последнего основного выпуска
* Общедоступная версия модуля `Az`.
* Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce
* Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/
* Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.
* Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.
* Добавлена поддержка для модулей runbook Python 2 в Az.Automation.
* Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:

#### <a name="azautomation"></a>Az.Automation
* В управление обновлениями службы автоматизации Azure внесены изменения для поддержки следующих новых функций:
    * динамическое группирование;
    * скрипты предварительного или последующего выполнения;
    * параметр перезагрузки.

#### <a name="azcompute"></a>Az.Compute
* Устранена проблема, связанная с разрешением пути в Get-AzVmBootDiagnosticsData.
* Обновление клиентской библиотеки вычислений до версии 25.0.0.

#### <a name="azkeyvault"></a>Az.KeyVault
* Добавлена поддержка подстановочных знаков в командлетах KeyVault.

#### <a name="aznetwork"></a>Az.Network
* Добавлена поддержка анализа угроз для Брандмауэра Azure.
* Добавлены настраиваемые правила и ресурс верхнего уровня для политики брандмауэра Шлюза приложений.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* В политику виртуальной машины Azure добавлен объект SnapshotRetentionInDays для поддержки мгновенного восстановления.
* Добавлена поддержка канала для отмены регистрации контейнера.

#### <a name="azresources"></a>Az.Resources
* Обновлена поддержка подстановочных знаков для Get-AzResource и Get-AzResourceGroup.
* Обновлены учетные данные, используемые при общих вызовах к ARM.

#### <a name="azsql"></a>Az.Sql
* Изменен тип параметра (ExcludeDetectionType) командлетов для обнаружения угроз с DetectionTypes на string[] для поддержки актуального состояния при добавлении новых типов обнаружения и для поддержки автозаполнения.

#### <a name="azstorage"></a>Az.Storage
* Поддержка получения, настройки и удаления политики управления в учетной записи хранения.
    - Set-AzStorageAccountManagementPolicy
    - Get-AzStorageAccountManagementPolicy
    - Remove-AzStorageAccountManagementPolicy
    - Add-AzStorageAccountManagementPolicyAction
    - New-AzStorageAccountManagementPolicyFilter
    - New-AzStorageAccountManagementPolicyRule

#### <a name="azwebsites"></a>Az.Websites
* Исправлена ошибка с шаблоном ARM, из-за которой прерывалось клонирование все слотов при использовании New-AzWebApp -IncludeSourceWebAppSlots. 

## <a name="150---march-2019"></a>1.5.0 — март 2019 г.
#### <a name="azaccounts"></a>Az.Accounts
* Добавлена команда Register-AzModule для поддержки созданных командлетов AutoRest.
* Обновлены примеры для Connect AzAccount.

#### <a name="azautomation"></a>Az.Automation
* Исправлена проблема с получением некоторых ежемесячных расписаний в нескольких командлетах службы автоматизации Azure.
* Исправлен командлет Get-AzAutomationDscNode, возвращающий только первые 20 узлов. Теперь он возвращает все узлы.

#### <a name="azcdn"></a>Az.Cdn
* Добавлены новые командлеты PowerShell для включения и отключения HTTPS для личного домена и отключены устаревшие командлеты.

#### <a name="azcompute"></a>Az.Compute
* Добавлена поддержка подстановочных знаков в командлетах Get.

#### <a name="azdatafactory"></a>Az.DataFactory
* Обновлен пакет SDK для ADF .NET до версии 3.0.1.

#### <a name="azlogicapp"></a>Az.LogicApp
* Исправлена проблема с получением только первой страницы результатов при выполнении команды ListWorkflows.

#### <a name="aznetwork"></a>Az.Network
* Добавлена поддержка подстановочных знаков в командлетах Network.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Добавлена поддержка SQL Server на виртуальной машине Azure.
* Обновление пакета SDK
* Удалена проверка VMappContainer в Get-ProtectableItem.
* Добавлены параметры Name и ServerName для Get-ProtectableItem.

#### <a name="azresources"></a>Az.Resources
* Добавлен параметр `-TemplateObject` в командлеты для развертывания.
    - Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2933.
* Устранена проблема с передачей в конвейер результата `Get-AzResource` для `Set-AzResource`.
    - Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8240.
* Устранена проблема с изменением типа данных JSON при выполнении `Set-AzResource`.
    - Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7930.

#### <a name="azsql"></a>Az.Sql
* Обновление AuditingEndpointsCommunicator.
    - Исправлено поведение для пограничного случая при создании параметров диагностики.

#### <a name="azstorage"></a>Az.Storage
* Включена поддержка Kind BlockBlobStorage при создании учетной записи хранения для New-AzStorageAccount.

## <a name="140---february-2019"></a>1.4.0 — февраль 2019 г.
#### <a name="azanalysisservices"></a>Az.AnalysisServices
* Командлет AddAzureASAccount устарел.

#### <a name="azautomation"></a>Az.Automation
* Обновлена справка для командлета Import-AzAutomationDscNodeConfiguration.
* Добавлена проверка имени конфигурации для командлета Import-AzAutomationDscConfiguration.
* Улучшена обработка ошибок для командлета Import-AzAutomationDscConfiguration.

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Добавлен параметр CustomSubdomainName — новый необязательный параметр для командлета New-AzCognitiveServicesAccount, который указывает поддомен для ресурса.

#### <a name="azcompute"></a>Az.Compute
* Устранена проблема с идентификаторами наборов параметров.
* Обновлен командлет Get-AzVMExtension для отображения списка всех установленных расширений, если не указан параметр Name.
* Для командлета Update-AzImage добавлены параметры Tag и ResourceId.
* Командлет Get-AzVmssVM, который выполняется без указания идентификатора экземпляра и с параметром InstanceView, может выводить виртуальные машины из VMSS с представлением экземпляра.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Добавлены командлеты для перечисления и восстановления удаленного элемента ADL.

#### <a name="azeventhub"></a>Az.EventHub
* Добавлено новое логическое свойство SkipEmptyArchives для пропуска пустых архивов в классе CaptureDescription Eventhub. 

#### <a name="azkeyvault"></a>Az.KeyVault
* Исправлена расстановка тегов для командлета Set-AzKeyVaultSecret.

#### <a name="azlogicapp"></a>Az.LogicApp
* Добавлен SKU "Базовый" для учетных записей интеграции.
* Добавлены типы сопоставлений Liquid, а также XSLT 2.0 и XSLT 3.0.
* Новые командлеты для сборок учетных записей интеграции:
    - Get-AzIntegrationAccountAssembly;
    - New-AzIntegrationAccountAssembly;
    - Remove-AzIntegrationAccountAssembly;
    - Set-AzIntegrationAccountAssembly.
* Новые командлеты для конфигурации пакета учетных записей интеграции:
    - Get-AzIntegrationAccountBatchConfiguration;
    - New-AzIntegrationAccountBatchConfiguration;
    - Remove-AzIntegrationAccountBatchConfiguration;
    - Set-AzIntegrationAccountBatchConfiguration.
* Обновлен пакет SDK Logic Apps до версии 4.1.0.

#### <a name="azmonitor"></a>Az.Monitor
* Обновлена справка для командлета Get-AzMetric.

#### <a name="aznetwork"></a>Az.Network
* Обновлен пример справки для командлета Add-AzApplicationGatewayCustomError.

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Дополнительная поддержка создания и получения источников данных ApplicationInsights.
    - Добавлен новый тип ApplicationInsights для получения определенных или всех источников данных ApplicationInsights для указанной рабочей области. 
    - Добавлен командлет New-AzOperationalInsightsApplicationInsightsDataSource для создания источника данных с использованием параметров указанного ресурса Application-Insightss: subscription Id, resourceGroupName и name. 

#### <a name="azresources"></a>Az.Resources
* исправлена проблема https://github.com/Azure/azure-powershell/issues/8166.
* исправлена проблема https://github.com/Azure/azure-powershell/issues/8235.
* исправлена проблема https://github.com/Azure/azure-powershell/issues/6219.
* Исправлена ошибка, препятствующая повторному созданию KeyCredentials.

#### <a name="azsql"></a>Az.Sql
* Добавлена поддержка уровня гипермасштабирования в базе данных SQL.
* Исправлена ошибка, из-за которой восстановление могло завершиться со сбоем при указании ненужных свойств в запросе на восстановление.

#### <a name="azwebsites"></a>Az.Websites
* Исправлен пример для командлета Get-AzWebAppSlotMetrics.

## <a name="130---february-2019"></a>1.3.0 — февраль 2019 г.
#### <a name="azaccounts"></a>Az.Accounts
* Обновление до последней версии ClientRuntime

#### <a name="azanalysisservices"></a>Az.AnalysisServices
Общедоступная версия модуля Az.AnalysisServices.

#### <a name="azcompute"></a>Az.Compute
* Расширение AEM: добавлена поддержка дисков UltraSSD, P60, P70 и P80.
* Обновлено описание справки для командлета Set-AzVMBootDiagnostics.
* Обновлено описание справки и пример для командлета Update-AzImage.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
Общедоступная версия модуля Az.RecoveryServices.

#### <a name="azresources"></a>Az.Resources
* Исправлена расстановка тегов для групп ресурсов. 
    - Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8166.
* Исправлена проблема с игнорированием командлетом `Get-AzureRmRoleAssignment` параметра -ErrorAction. 
    - Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8235.

#### <a name="azsql"></a>Az.Sql
* Добавлен командлет Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy.
* Исправлена проблема с появлением исключения NullRef при выполнении командлетов SQL, если не выполнен вход в учетную запись Azure.
* Исправлено исключение NullRef в командлете Get-AzSqlCapability.

## <a name="121---january-2019"></a>1.2.1 — январь 2019 г.
#### <a name="azaccounts"></a>Az.Accounts
* Выпуск с правильной версией службы аутентификации.

#### <a name="azanalysisservices"></a>Az.AnalysisServices
* Выпуск с обновленной зависимостью службы аутентификации.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Выпуск с обновленной зависимостью службы аутентификации.

## <a name="120---january-2019"></a>1.2.0 — январь 2019 г.
#### <a name="azaccounts"></a>Az.Accounts
* Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.
* Исправлены неправильные URL-адреса онлайн-справки.
* Добавлено предупреждающее сообщение в PS Core для модуля Uninstall-AzureRm.

#### <a name="azaks"></a>Az.Aks
* Исправлены неправильные URL-адреса онлайн-справки.

#### <a name="azautomation"></a>Az.Automation
* Добавлена поддержка для модулей runbook Python 2.
* Исправлены неправильные URL-адреса онлайн-справки.

#### <a name="azcdn"></a>Az.Cdn
* Исправлены неправильные URL-адреса онлайн-справки.

#### <a name="azcompute"></a>Az.Compute
* Добавлен командлет Invoke-AzVMReimage.
* Добавлен параметр TempDisk к командлету Set-AzVmss.
* Исправлено предупреждающее сообщение командлета New-AzVM.

#### <a name="azcontainerregistry"></a>Az.ContainerRegistry
* Исправлены неправильные URL-адреса онлайн-справки.

#### <a name="azdatafactory"></a>Az.DataFactory
* Пакет SDK ADF .Net обновлен до версии 3.0.0.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Исправлена проблема с конечной точкой ADLS при использовании MSI.
    - Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7462.
* Исправлены неправильные URL-адреса онлайн-справки.

#### <a name="aziothub"></a>Az.IotHub
* Добавлен формат кодирования для командлета Add-IotHubRoutingEndpoint.

#### <a name="azkeyvault"></a>Az.KeyVault
* Исправлены неправильные URL-адреса онлайн-справки.

#### <a name="aznetwork"></a>Az.Network
* Исправлены неправильные URL-адреса онлайн-справки.

#### <a name="azresources"></a>Az.Resources
* Исправлены неправильные примеры в справочной документации по командлетам New-AzADAppCredential и New-AzADSpCredential.
* Исправлена проблема, при которой путь для параметра -TemplateFile не удавалось разрешить до выполнения командлетов развертывания групп ресурсов.
* Az.Resources: исправлена документация для значения по умолчанию -Mode командлета New-AzureRmPolicyDefinition.
* Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/7522.
* Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/5747.
* Исправлена проблема с форматированием объекта PSResourceGroupDeployment.
    - Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2123.

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Исправлена проблема с появлением исключения в процессе отката при добавлении сертификата к модели VMSS: https://github.com/Azure/service-fabric-issues/issues/932.
* Исправлены некоторые сообщения об ошибках.
* Исправлена проблема с созданием кластера с шаблоном ARM по умолчанию для командлета New-AzServiceFabriCluster, который не работал с операцией миграции в Az.
* Исправлена проблема с добавлением сертификата кластера или приложения: теперь они добавляются только в Масштабируемые наборы виртуальных машин, которые сопоставлены с кластером, путем проверки идентификатора кластера в расширении.

#### <a name="azsignalr"></a>Az.SignalR
* Исправлены неправильные URL-адреса онлайн-справки.

#### <a name="azsql"></a>Az.Sql
* Исправлены неправильные URL-адреса онлайн-справки.
* Обновлено описание параметра LicenseType с добавлением возможных значений.
* Исправлена проблема с неправильным обновлением удостоверения управляемого экземпляра, если оно было единственным обновляемым свойством.
* Поддержка пользовательских параметров сортировки в управляемых экземплярах.

#### <a name="azstorage"></a>Az.Storage
* Исправлены неправильные URL-адреса онлайн-справки.
* Добавлен вывод подробных сообщений об ошибке при получении или установке классических свойств ведения журнала или метрик в учетной записи хранилища класса Premium, так как учетная запись хранилища класса Premium не поддерживает классические функции ведения журнала и метрик.
    - Get/Set-AzStorageServiceLoggingProperty
    - Get/Set-AzStorageServiceMetricsProperty

#### <a name="aztrafficmanager"></a>Az.TrafficManager
* Исправлены неправильные URL-адреса онлайн-справки.

#### <a name="azwebsites"></a>Az.Websites
* Исправлены неправильные URL-адреса онлайн-справки.
* Исправлена работа командлета New-AzWebAppSSLBinding: сертификат отправляется в правильную группу ресурсов и правильное расположение, если приложение размещено в ASE.
* Исправлена работа командлета New-AzWebAppSSLBinding: теги не перезаписываются при привязке SSL-сертификата к приложению.

## <a name="110---january-2019"></a>1.1.0 — январь 2019 г.
#### <a name="azaccounts"></a>Az.Accounts
* Добавление области "Local" в Enable-AzureRmAlias.

#### <a name="azcompute"></a>Az.Compute
* Теперь имя не является обязательным в идентификаторе набора параметров для Restart/Start/Stop/Remove/Set-AzVM и Save-AzVMImage.
* Обновлено описание идентификатора в файлах справки.
* Устранена проблема обратной совместимости с модулем Az.Accounts.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Обновление версии пакета SDK для плоскости данных до 1.1.14 для устранения найденных проблем.
    - Исправлена обработка отрицательного времени доступа и времени изменения для getfilestatus и liststatus, исправлен токен отмены для асинхронных методов.

#### <a name="azeventgrid"></a>Az.EventGrid
* Обновление для использования API версии 2019-01-01.
* Обновлены указанные ниже командлеты для поддержки нового сценария в API версии 2019-01-01.
    - New-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:
        - срока жизни события;
        - максимального числа попыток доставки для событий;
        - конечной точки недоставленных сообщений.
    - Update-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:
        - срока жизни события;
        - максимального числа попыток доставки для событий;
        - конечной точки недоставленных сообщений.
* Для параметра EndpointType добавлены новые значения перечисления (storageQueue и hybridConnection) в командлеты New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription.
* Если ожидается, что создание или обновление подписки на событие повлечет за собой действия со стороны пользователя, выполняемые вручную, отображается предупреждение при создании или обновлении подписки события.

#### <a name="aziothub"></a>Az.IotHub
* Пакет SDK Центра Интернета вещей обновлен до последней версии.

#### <a name="azlogicapp"></a>Az.LogicApp
* Get-AzLogicApp позволяет перечислить все параметры без указанного имени.

#### <a name="azresources"></a>Az.Resources
* Исправлена проблема с набором параметров при предоставлении параметров "-ODataQuery" и "-ResourceId" для "Get-AzResource".
    - Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7875.
* Исправлена обработка параметра -Custom в New/Set-AzPolicyDefinition.
* Исправлена опечатка в документации по New-AzDeployment.
* Параметр "-MailNickname" стал обязательным для "New-AzADUser".
    - Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8220.

#### <a name="azsignalr"></a>Az.SignalR
* Устранена проблема обратной совместимости с модулем Az.Accounts.

#### <a name="azsql"></a>Az.Sql
* Зависимость клиента управления хранением преобразована для общей реализации в пакете SDK.

#### <a name="azstorage"></a>Az.Storage
* Установка параметра StorageAccountName для контекста хранилища в качестве реального имени учетной записи хранения, если она была создана с использованием токена Sas, OAuth или анонимного доступа.
    - New-AzStorageContext
* Создание токена Sas большого двоичного объекта моментального снимка с параметром "-FullUri". Возвращаемый URI исправлен на URI моментального снимка.
    - New-AzStorageBlobSASToken

#### <a name="azwebsites"></a>Az.Websites
* Исправлена ошибка синтаксического анализа даты в "Get-AzDeletedWebApp".
* Устранена проблема обратной совместимости с модулем Az.Accounts.

## <a name="100---december-2018"></a>1.0.0 — декабрь 2018 г.
### <a name="general"></a>Общие сведения

- Общедоступная версия модуля Az.
- Справка в Интернете для каждого модуля.
- Дополнительные сведения и стратегию развития см. в статье [Announcing New Module 'Az'](https://aka.ms/azps-announce) (Объявление о новом модуле Az)
- Сведения о миграции с AzureRM см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)

### <a name="azaccounts"></a>Az.Accounts
- Изменено с Az.Profile.
- Исправлены форматы таблиц для типов профиля и контекста.

### <a name="azapimanagement"></a>Az.ApiManagement
- Исправления для #7002.
- Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)

### <a name="azbatch"></a>Az.Batch
- Добавлена возможность видеть, какая версия агента узла пакетной службы Azure работает в пуле на каждой виртуальной машине, с помощью нового свойства `NodeAgentInformation` в `PSComputeNode`.
- Значение `Caching` по умолчанию для `PSDataDisk` теперь `ReadWrite` вместо `None`.
- Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)

### <a name="azbilling"></a>Az.Billing
- Объединены командлеты Billing, Consumption и UsageAggregates. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0).

### <a name="azcognitivservices"></a>Az.CognitivServices
- Добавлены средства заполнения для SkuName и Typem, доступные в операции New-AzureRmCognitiveServicesAccount.
- Удален набор параметров GetSkusWithAccountParamSetName из Get-AzCognitiveServicesAccountSkus.

### <a name="azcontainerinstance"></a>Az.ContainerInstance
- Добавлена поддержка ManagedIdentity.

### <a name="azdatalakeanalytics"></a>Az.DataLakeAnalytics
- Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)

### <a name="azdatalakestore"></a>Az.DataLakeStore
- Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)

### <a name="azmonitor"></a>Az.Monitor
- "Az.Insights" переименован в "Az.Monitor" и внесены другие незначительные критические изменения. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)

### <a name="azkeyvault"></a>Az.KeyVault
- Из типов вывода удалено устаревшее свойство PurgeDisabled

### <a name="azmachinelearning"></a>Az.MachineLearning
- Включены командлеты из модуля Az.MachineLearningCompute

### <a name="azmedia"></a>Az.Media
- Удаляет устаревший псевдоним Tags из New-AzMediaService

### <a name="aznetwork"></a>Az.Network
В шлюз приложений добавлена поддержка настройки RewriteRuleSets
    - Добавлены новые командлеты:
        - Add-AzureRmApplicationGatewayRewriteRuleSet
        - Get-AzureRmApplicationGatewayRewriteRuleSet
        - New-AzureRmApplicationGatewayRewriteRuleSet
        - Remove-AzureRmApplicationGatewayRewriteRuleSet
        - Set-AzureRmApplicationGatewayRewriteRuleSet
        - New-AzureRmApplicationGatewayRewriteRule
        - New-AzureRmApplicationGatewayRewriteRuleActionSet
        - New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration
    - В следующие командлеты добавлен необязательный параметр -RewriteRuleSet
        - New-AzureRmApplicationGateway
        - New-AzureRmApplicationGatewayRequestRoutingRule
        - Add-AzureRmApplicationGatewayRequestRoutingRule
        - New-AzureRmApplicationGatewayPathRuleConfig
        - Add-AzureRmApplicationGatewayUrlPathMapConfig
        - New-AzureRmApplicationGatewayUrlPathMapConfig добавил с помощью идентификатора поддержку KeyVault для шлюза приложений.
    - В следующие командлеты добавлен необязательный параметр -KeyVaultSecretId, -KeyVaultSecret
        - Add-AzApplicationGatewaySslCertificate
        - New-AzApplicationGatewaySslCertificate
        - Set-AzApplicationGatewaySslCertificate
    - В командлет New-AzApplicationGateway добавлен необязательный параметр -UserAssignedIdentity
- Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)

### <a name="azoperationalinsights"></a>Az.OperationalInsights
- Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)

### <a name="azprofile"></a>Az.Profile
- Имя модуля изменено на Az.Accounts.

### <a name="azrecoveryservices"></a>Az.RecoveryServices
- Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)

### <a name="azresources"></a>Az.Resources
- Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)

### <a name="azservicefabric"></a>Az.ServiceFabric
- Поддержка спецификации сертификата по общему имени и отпечатку
- Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)

### <a name="azsignalr"></a>Az.SIgnalR
- Общедоступная версия командлетов PowerShell для SIgnalR

### <a name="azsql"></a>Az.Sql
- Добавлены новые типы обнаружения Data_Exfiltration и Unsafe_Action в командлеты обнаружения угроз
- Примеры обновленной документации для командлетов аудита Sql
- Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)

### <a name="azstorage"></a>Az.Storage
- Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)

### <a name="azwebsites"></a>Az.Websites
- Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)

## <a name="070---december-2018"></a>0.7.0 — декабрь 2018 г.

### <a name="general"></a>Общие сведения

* Незначительные изменения для предстоящего перехода AzureRM на Az

### <a name="azcompute"></a>Az.Compute

* Добавлена поддержка UltraSSD и образов коллекции в простых наборах параметров для командлетов `New-AzVm(ss)`.

### <a name="azdatalakestore"></a>Az.DataLakeStore

* Исправлено косую черту в конце домена учетной записи ADLS

### <a name="azfrontdoor"></a>Az.FrontDoor

* Исправлены некоторые неработающие ссылки
    - В статьях New-AzureRmFrontDoor и Set-AzureRmFrontDoor исправлена ссылка на статью командлета New-AzureRmFrontDoorHealthProbeSettingObject.
    - В статье New-AzureRmFrontDoorManagedRuleObject исправлена ссылка на статью командлета New-AzureRmFrontDoorRuleGroupOverrideObject.

### <a name="azrecoveryservices"></a>Az.RecoveryServices

* Добавлены проверки на стороне клиента для операций восстановления общей папки Azure.
* StorageAccountName и storageAccountResourceGroupName являются необязательными для восстановления afs.

### <a name="azresources"></a>Az.Resources

* Исправление для https://github.com/Azure/azure-powershell/issues/7679.
    - Обновите Get-AzureRmRoleAssignment, чтобы использовать область подписки, если она указана при запросе классических администраторов.

### <a name="azsql"></a>Az.Sql

* Незначительные изменения для предстоящего перехода AzureRM на Az
* Устранена проблема с использованием Get-AzureRmSqlDatabaseVulnerabilityAssessment с .NET Core.
* Изменена документация справочных сообщений, связанных с командлетами аудита SQL.

### <a name="azstorage"></a>Az.Storage

* Добавлено -EnableHierarchicalNamespace к New-AzureRmStorageAccount
* Устранена проблема, из-за которой командлет Copy File не может повторно использовать исходный контекст в пункте назначения, если не введен -DestContext
    - Start-AzureStorageFileCopy
* Поддержка статической конфигурации сайта
    - Enable-AzureStorageStaticWebsite
    - Disable-AzureStorageStaticWebsite

### <a name="azwebsites"></a>Az.Websites

* Set-AzureRmWebApp и Set-AzureRmWebAppSlot 
    - Добавлен новый параметр (-AzureStoragePath), который указывает путь службы хранилища Azure для подключения в приложениях-контейнерах Windows и Linux. Используйте выходные данные нового командлета New-AzureRmWebAppAzureStoragePath в качестве параметра, чтобы задать пути к службе хранилища Azure.

## <a name="061---november-2018"></a>0.6.1 — ноябрь 2018 г.

### <a name="azapimanagement"></a>Az.ApiManagement
* Обновлены зависимости для устранения проблемы сопоставления типов.

### <a name="azautomation"></a>Az.Automation
* Командлеты службы автоматизации Azure на базе Swagger.
* Добавлены командлеты для Управления обновлениями.
* Добавлены командлеты для системы управления версиями.
* Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.
* Исправлена команда DSC для регистрации узла.

### <a name="azcompute"></a>Az.Compute
* Исправлена проблема с удостоверением, назначаемым системой.
* Обновлены зависимости для устранения проблемы сопоставления типов.

### <a name="azcontainerinstance"></a>Az.ContainerInstance
* Обновлены зависимости для устранения проблемы сопоставления типов.

### <a name="azmarketplaceordering"></a>Az.MarketplaceOrdering
* Обновлено описание в примерах командлетов для Marketplace.

### <a name="aznetwork"></a>Az.Network
* Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.
* Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.
* Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта. 
* Исправлены проблемы с использованием памяти в карте виртуальной сети.

### <a name="azrecoveryservicesbackup"></a>Az.RecoveryServices.Backup
* Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.
* Параметры часового пояса преобразованы в верхний регистр.

### <a name="azrecoveryservicessiterecovery"></a>Az.RecoveryServices.SiteRecovery
* Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.
* Обновлены зависимости для устранения проблемы сопоставления типов.

### <a name="azrelay"></a>Az.Relay
* Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.

### <a name="azresources"></a>Az.Resources
* Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.
* Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.
* Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.

### <a name="azservicefabric"></a>Az.ServiceFabric
* Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.

### <a name="azsql"></a>Az.Sql
* Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.
    - Get-AzureRmSqlInstance.
    - New-AzureRmSqlInstance.
    - Set-AzureRmSqlInstance.
    - Remove-AzureRmSqlInstance.
    - Get-AzureRmSqlInstanceDatabase.
    - New-AzureRmSqlInstanceDatabase.
    - Restore-AzureRmSqlInstanceDatabase.
    - Remove-AzureRmSqlInstanceDatabase.
* Добавлено расширенное управление политиками аудита для сервера или базы данных.
    - Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.
    - Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.
    - Set-AzureRmSqlServerAuditing.
    - Get-AzureRmSqlServerAuditing.
    - Set-AzureRmSqlDatabaseAuditing.
    - Get-AzureRmSqlDatabaseAuditing.
* Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.

## <a name="050---november-2018"></a>0.5.0 — ноябрь 2018 г.
#### <a name="general"></a>Общие сведения
* Добавлены средства заполнения ресурсов для многих основных командлетов — они позволяют вам переключать существующие имена ресурсов при вызове командлетов в интерактивном режиме

#### <a name="azprofile"></a>Az.Profile
* Обновлен общий код для использования последней версии ClientRuntime.
* В командлете Connect-AzAccount параметр TenantId переименован в Tenant и добавлен псевдоним для TenantId
* Обновлено описание TenantId для командлета Connect-AzAccount
* Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.
    - https://github.com/Azure/azure-powershell/issues/6936
* Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.
    - https://github.com/Azure/azure-powershell/issues/7453
* Устранена проблема с конечными точками DataLake при использовании MSI.
    - https://github.com/Azure/azure-powershell/issues/7462
* Устранена проблема, при которой командлет Disconnect-AzAccount вызывал сбой при отсутствии подключения
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Добавлена операция Get-AzCognitiveServicesAccountSkus.

#### <a name="azcompute"></a>Az.Compute
* Добавлены командлеты Add-AzVmssVMDataDisk и Remove-AzVmssVMDataDisk
* Get-AzVMImage отображает AutomaticOSUpgradeProperties
* Устранена проблема, при которой значения параметров SetAzVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Обновлен пакет DataLake до версии 1.1.10.
* Параметр по умолчанию Concurrency добавлен к многопоточным операциям.

#### <a name="azinsights"></a>Az.Insights
* Исправлена проблема № 7267 (область автомасштабирования).
    - Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).
* Исправлена проблема № 7513 [Insights], при которой для командлета Set-AzDiagnosticSetting требовалось явное указание категорий во время создания параметра
    - Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.

#### <a name="aznetwork"></a>Az.Network
* Параметр PeeringType является обязательным для следующих командлетов:
    - Get-AzExpressRouteCircuitRouteTable
    - Get-AzExpressRouteCircuitARPTable
    - Get-AzExpressRouteCircuitRouteTableSummary
    - Get-AzExpressRouteCrossConnectionArpTable
    - Get-AzExpressRouteCrossConnectionRouteTable
    - Get-AzExpressRouteCrossConnectionRouteTableSummary

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Добавлена политика исправления командлетов.

#### <a name="azresources"></a>Az.Resources
* Исправление для https://github.com/Azure/azure-powershell/issues/7402.
    - Разрешено перечисление ресурсов с помощью параметра -ResourceId для командлета Get-AzResource

#### <a name="azservicebus"></a>Az.ServiceBus
* Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Устранена проблема с добавлением сертификата в VMSS Linux.
* Исправлен командлет Add-AzServiceFabricClusterCertificate
    - Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).
    - Исключение отображается правильно (Azure/service-fabric-issues#1054).
* Исправлен командлет Update-AzServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.

## <a name="040---october-2018"></a>0.4.0 — октябрь 2018 г.
#### <a name="azprofile"></a>Az.Profile
* Устранена проблема с Get-AzSubscription в CloudShell
* Обновлен общий код для использования последней версии ClientRuntime.

#### <a name="azcompute"></a>Az.Compute
* В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzVm
* Во все командлеты добавлено средство заполнения для аргумента ResourceName.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Добавлена поддержка правил виртуальной сети:
    - Get-AzDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.
    - Add-AzDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.
    - Set-AzDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.
    - Remove-AzDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.

#### <a name="aznetwork"></a>Az.Network
* Обновлен командлет Test-AzNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.
* Во все командлеты добавлено средство заполнения для аргумента ResourceName.

#### <a name="azresources"></a>Az.Resources
* Устранена проблема, из-за которой командлет Get-AzRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), благодаря добавлению понятного исключения в сценарий. Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.

## <a name="030---october-2018"></a>0.3.0 — октябрь 2018 г.
#### <a name="azurestorage"></a>Azure.Storage;
* Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.
    - Start-AzureStorageBlobCopy
    - Start-AzureStorageFileCopy
* Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.
    - Get-AzStorageUsage
    
#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Поддержка Get-AzCognitiveServicesAccountSkus без существующей учетной записи.

#### <a name="azcompute"></a>Az.Compute
* Исправлена команда Get-AzVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов
* Добавлен пример использования SimpleParameterSet в справку командлета New-AzVmss.
* Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.

#### <a name="azdatafactoryv2"></a>Az.DataFactoryV2
* Пакет .NET SDK для ADF обновлен до версии 2.3.0.

#### <a name="aznetwork"></a>Az.Network
* Добавлена функциональность NetworkProfile. Добавлены новые командлеты:
    - Get-AzNetworkProfile
    - New-AzNetworkProfile
    - Remove-AzNetworkProfile
    - Set-AzNetworkProfile
    - New-AzContainerNicConfig
    - New-AzContainerNicConfigIpConfig
* Добавлен канал связи служб в модель подсети.
* Добавлены командлеты: New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap
* Добавлены командлеты: Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig

#### <a name="azrediscache"></a>Az.RedisCache
* С этого момента добавлена поддержка любой строки в качестве параметра Size. Добавлено значение P5 во всплывающее окно PSArgumentCompleter.

#### <a name="azresources"></a>Az.Resources
* Добавлен отсутствующий параметр -Mode в командлет Set-AzPolicyDefinition
* Исправлена ошибка командлета Get-AzProviderOperation для операций, когда Origin содержит User

#### <a name="azsql"></a>Az.Sql
* Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.

#### <a name="azwebsites"></a>Az.Websites
* Новый командлет Get-AzWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера
* Новые командлеты New-AzWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows

## <a name="020---september-2018"></a>0.2.0 — сентябрь 2018 г.
 Первый выпуск