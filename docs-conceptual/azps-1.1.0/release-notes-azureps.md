---
ms.openlocfilehash: 179d22fa065944695e4769f2698e3cabc7666b04
ms.sourcegitcommit: c6fd0e490fa0e33b8b768b679682a47d8faae1cf
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/16/2019
ms.locfileid: "54342153"
---
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