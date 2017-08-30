Установщик Azure PowerShell 4.3.1: [ссылка](https://github.com/Azure/azure-powershell/releases/download/v4.3.1-August2017/azure-powershell.4.3.1.msi).

Модуль из коллекции для командлетов ARM: [ссылка](https://www.powershellgallery.com/packages/AzureRM/4.3.1).

Модуль из коллекции для командлетов прежних версий для службы управления (RDFE): [ссылка](https://www.powershellgallery.com/packages/Azure/4.3.1).

## <a name="changes-in-431"></a>Изменения в версии 4.3.1

- Исправлена проблема, из-за которой определенные сборки не подписывались, в результате чего при импорте модулей происходила ошибка `could not load file or assembly`.

## <a name="changes-in-430"></a>Изменения в версии 4.3.0

* Analysis Services:
    * Исправлена ошибка в Set-AzureRmAnalysisServciesServer.
        - Если администратор не был указан, он удалялся.
    * В New-AzureRmAnalysisServicesServer и Set-AzureRmAnalysisServicesServer добавлен параметр BackupBlobContainerUri.
        - Позволяет настроить или отключить контейнер больших двоичных объектов резервных копий для архивации и восстановления сервера Azure Analysis Services.
    * В New-AzureRmAnalysisServicesServer и Set-AzureRmAnalysisServicesServer обновлен поиск номера SKU.
        - Жесткое программирование номера SKU изменено на динамический поиск.
    * Поддержка входа в систему с помощью субъекта-службы для Add-AzureAnalysisServicesAccount.
* Служба автоматизации
    * Внесены изменения в командлеты Automation DSC*, позволяющие получить более 100 записей.
    * Устранена проблема, из-за которой подробные потоки прекращали работать после вызова некоторых командлетов службы автоматизации (например, Get-AzureRmAutomationVariable, Get-AzureRmAutomationJob).
    * В StartAzureAutomationDscCompilationJob и ImportAzureAutomationDscNodeConfiguration добавлена поддержка управления версиями сборок NodeConfiguration.
    * Исправлены существующие проблемы: устранена проблема с псевдонимом № 3775, а также исправлены проблемы с псевдонимом runOn и поддержкой HybridWorkers.
* Среда выполнения приложений
    * Set-AzureRmVMAEMExtension: добавлена поддержка новых размеров дисков уровня "Премиум".
    * Set-AzureRmVMAEMExtension: добавлена поддержка серии M.
    * В Add-AzureRmVmssExtension добавлен параметр ForceUpdateTag.
    * В New-AzureRmVmssIpConfig добавлен параметр Primary.
    * В Add-AzureRmVmssNetworkInterfaceConfig добавлен параметр EnableAcceleratedNetworking.
    * В Set-AzureRmVmss добавлен параметр InstanceId.
    * Предоставление MaintenanceRedeployStatus в выходных данных Get-AzureRmVM -Status.
    * Предоставление Restriction и Capability в табличном формате Get-AzureRmComputeResourceSku.
* Data Lake Store
    * Устранение проблемы: https://github.com/Azure/azure-powershell/issues/4323.
* концентратор событий.
    * В NamespaceAttributes добавлено свойство ResourceGroup.
        - ResourceGroup позволяет получить имя группы ресурсов пространства имен.
    * В командлеты добавлены новый параметр и псевдоним параметра.
        - В приведенные ниже командлеты добавлены свойство Parametersets для пространства имен и концентратора событий для функционирования правила авторизации.
        - New-AzureRmEventHubAuthorizationRule
            + Добавляет новое правило авторизации для существующего пространства имен или концентратора событий.
        - Get-AzureRmEventHubAuthorizationRule
            + Возвращает правило авторизации или список правил авторизации для существующего пространства имен или концентратора событий.
        - Set-AzureRmEventHubAuthorizationRule
            + Обновляет свойства существующего правила авторизации пространства имен концентратора событий.
        - Remove-AzureRmEventHubAuthorizationRule
            + Удаляет правило авторизации существующего пространства имен или концентратора событий.
        - New-AzureRmEventHubKey
            + Создает новый первичный или вторичный ключ для правила авторизации существующего пространства имен или концентратора событий.
        - Get-AzureRmEventHubKey
            + Получает первичный или вторичный ключ для правила авторизации существующего пространства имен или концентратора событий.
* Сеть
    * New-AzureRmExpressRouteCircuitPeeringConfig: добавлена поддержка IPv6. Добавлен новый необязательный параметр.
        - PeerAddressType.
    * Set-AzureRmExpressRouteCircuitPeeringConfig: добавлена поддержка IPv6. Добавлен новый необязательный параметр.
        - PeerAddressType.
    * Remove-AzureRmExpressRouteCircuitPeeringConfig: добавлена поддержка IPv6. Добавлен новый необязательный параметр.
        - PeerAddressType.
    * Параметр -ProbeEnabled помечен как устаревший.
        - Add-AzureRmApplicationGatewayBackendHttpSettings
        - New-AzureRmApplicationGatewayBackendHttpSettings
        - Set-AzureRmApplicationGatewayBackendHttpSettings
* Профиль
    * Сбор данных включен по умолчанию. Данные об использовании собираются корпорацией Майкрософт, чтобы улучшить взаимодействие с пользователем. Эти данные являются анонимными и не содержат значения аргументов командной строки.
        - Отключите эту функцию с помощью командлета Disable-AzureRmDataCollection.
        - Включите эту функцию с помощью командлета Enable-AzureRmDataCollection.
* Ресурсы
    * Добавлена поддержка проверки областей для следующих командлетов roledefinition и roleassignment перед отправкой запроса к ARM:
        - Get-AzureRMRoleAssignment;
        - New-AzureRMRoleAssignment;
        - Remove-AzureRMRoleAssignment;
        - Get-AzureRMRoleDefinition;
        - New-AzureRMRoleDefinition;
        - Remove-AzureRMRoleDefinition;
        - Set-AzureRMRoleDefinition.
* Служебная шина
    * Ниже приведены новые командлеты для правил авторизации пространств имен, очередей и разделов. Операции с правилом авторизации выполняются в соответствии с заданным параметром.
     - New-AzureRmServiceBusAuthorizationRule.
       - Добавляет новое правило авторизации для существующего пространства имен, очереди или раздела служебной шины.
     - Get-AzureRmServiceBusAuthorizationRule.
       - Возвращает правило авторизации или список правил авторизации для существующего пространства имен, очереди или раздела служебной шины.
     - Set-AzureRmServiceBusAuthorizationRule.
       - Обновляет свойства существующего правила авторизации пространства имен, очереди или раздела служебной шины.
     - New-AzureRmServiceBusKey.
       - Создает новый первичный или вторичный ключ для правила авторизации существующего пространства имен, очереди или раздела служебной шины.
     - Get-AzureRmServiceBusKey.
       - Создает новый первичный или вторичный ключ для правила авторизации существующего пространства имен, очереди или раздела служебной шины.
     - Remove-AzureRmServiceBusNamespaceAuthorizationRule
       - Удаляет существующее правило авторизации пространства имен, очереди или раздела служебной шины.
    * В NamespaceAttributes добавлено свойство ResourceGroup.
* SQL
    * Командлет Set-AzureRmSqlServerTransparentDataEncryptionProtector обновлен для отображения предупреждения и запроса подтверждения в случае, если для типа средства защиты шифрования задается значение AzureKeyVault.
    * Добавлены обновленные командлеты для параметров аудита.
        - Добавлен командлет Get-AzureRmSqlDatabaseAuditing, который получает параметры аудита базы данных SQL Azure.
        - Добавлен командлет Get-AzureRmSqlServerAuditing, который получает параметры аудита сервера SQL Azure Server.
        - Добавлен командлет Set-AzureRmSqlDatabaseAuditing, который изменяет параметры аудита для базы данных SQL Azure.
        - Добавлен командлет Set-AzureRmSqlServerAuditing, который изменяет параметры аудита сервера SQL Azure Server.
    * Объявлены неподдерживаемыми существующие командлеты для политик аудита.
        - Объявлен неподдерживаемым Get-AzureRmSqlDatabaseAuditingPolicy.
        - Объявлен неподдерживаемым Get-AzureRmSqlServerAuditingPolicy.
        - Объявлен неподдерживаемым Set-AzureRmSqlDatabaseAuditingPolicy.
        - Объявлен неподдерживаемым Set-AzureRmSqlServerAuditingPolicy.
        - Объявлен неподдерживаемым Use-AzureRmSqlServerAuditingPolicy.
        - Объявлен неподдерживаемым Remove-AzureRmSqlDatabaseAuditing.
        - Объявлен неподдерживаемым Remove-AzureRmSqlServerAuditing.
    * При анализе файла схемы для Update-AzureRmSqlSyncGroup теперь не учитывается регистр.
* Хранилище
    * Добавлена поддержка NeworkRule в командлетах, предназначенных для учетных записей хранения в режиме ресурсов.
        - New-AzureRmStorageAccount;
        - Set-AzureRmStorageAccount.
        - Get-AzureRmStorageAccountNetworkRuleSet.
        - Update-AzureRmStorageAccountNetworkRuleSet.
        - Add-AzureRmStorageAccountNetworkRule.
        - Remove-AzureRmStorageAccountNetworkRule.

Ознакомьтесь с [изменениями, внесенными после последнего выпуска](https://github.com/Azure/azure-powershell/compare/v4.2.1-July2017...v4.3.1-August2017).
