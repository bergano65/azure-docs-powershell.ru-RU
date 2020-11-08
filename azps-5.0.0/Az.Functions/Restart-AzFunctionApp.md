---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/restart-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Restart-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Restart-AzFunctionApp.md
ms.openlocfilehash: 408adc74257e1260e97c47b24d91cf437b915a5f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245415"
---
# Restart-AzFunctionApp

## КРАТКИй обзор
Перезапускает приложение функции.

## Максимальное

### RestartByName (по умолчанию)
```
Restart-AzFunctionApp -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ByObjectInput
```
Restart-AzFunctionApp -InputObject <ISite> [-Force] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## NОПИСАНИЕ
Перезапускает приложение функции.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение приложения функции по имени и перезапуску.
```powershell
PS C:\> Get-AzFunctionApp -Name MyAppName -ResourceGroupName MyResourceGroupName | Restart-AzFunctionApp -Force
```

Эта команда получает приложение с именем и перезапускает ее.

### Пример 2. Перезапустите приложение функции по имени.
```powershell
PS C:\> Restart-AzFunctionApp -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

Эта команда перезапускает приложение по имени.

## ПАРАМЕТРЫ

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Принудительно запускает приложение функции без запроса на подтверждение командлета.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Для конструирования просмотрите раздел заметок о свойствах INPUTOBJECT и создайте хэш-таблицу.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite
Parameter Sets: ByObjectInput
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (имя)
Имя приложения функции.

```yaml
Type: System.String
Parameter Sets: RestartByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Возвращает значение истина, если команда выполнена успешно.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName


```yaml
Type: System.String
Parameter Sets: RestartByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Идентификатор подписки Azure.

```yaml
Type: System.String
Parameter Sets: RestartByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Запрашивает подтверждение перед запуском командлета.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске командлета.
Командлет не выполняется.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## ВХОДНЫЕ данные

### Microsoft. Azure. PowerShell. командлеты. functions. Models. Api20190801. ISite

## НАПРЯЖЕНИЕ

### System. Boolean

## Пуск

СВЯЗЫВАЮТ

СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ

Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства. Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.


INPUTOBJECT <ISite> : 
  - `Location <String>`: Расположение ресурса.
  - `CloningInfoSourceWebAppId <String>`: Идентификатор ресурса ARM исходного приложения. Идентификатор ресурса приложения — это форма/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} для слотов производства и/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} для других слотов.
  - `[Kind <String>]`: Типа ресурса.
  - `[Tag <IResourceTags>]`: Теги ресурсов.
    - `[(Any) <String>]`: Это указывает на то, что в этот объект можно добавить любое свойство.
  - `[ClientAffinityEnabled <Boolean?>]`: <code>true</code> чтобы включить сходство клиентов <code>false</code> , остановите отправку cookie-файлов сходства сеансов, чтобы перенаправлять запросы клиентов в одном сеансе в один и тот же экземпляр. По умолчанию <code>true</code> .
  - `[ClientCertEnabled <Boolean?>]`: <code>true</code> Включение проверки подлинности сертификата клиента (TLS-аутентификация); в противном случае <code>false</code> . По умолчанию <code>false</code> .
  - `[ClientCertExclusionPath <String>]`: проверка подлинности сертификата клиента с разделителями-запятыми
  - `[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Параметр приложения переопределен для клонированного приложения. Если задано, эти параметры переопределяют параметры, скопированные из исходного приложения. В противном случае сохраняются параметры приложения исходного приложения.
    - `[(Any) <String>]`: Это указывает на то, что в этот объект можно добавить любое свойство.
  - `[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> позволяет клонировать пользовательские имена узлов из исходного приложения, в противном случае — <code>false</code> .
  - `[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> для клонирования системы управления версиями из исходного приложения, в противном случае <code>false</code> .
  - `[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> Настройка балансировки нагрузки для исходного и конечного приложений.
  - `[CloningInfoCorrelationId <String>]`: Идентификатор корреляции операции клонирования. Этот идентификатор связывает несколько операций клонирования, чтобы использовать один и тот же снимок.
  - `[CloningInfoHostingEnvironment <String>]`: Среда службы приложений.
  - `[CloningInfoOverwrite <Boolean?>]`: <code>true</code> чтобы перезаписать конечное приложение, в противном случае — <code>false</code> .
  - `[CloningInfoSourceWebAppLocation <String>]`: Расположение исходного приложения, например, "Западная часть США" или "Северная Европа"
  - `[CloningInfoTrafficManagerProfileId <String>]`: Идентификатор ресурса ARM профиля диспетчера трафика, который необходимо использовать, если он существует. Идентификатор ресурса диспетчера трафика имеет форму/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.
  - `[CloningInfoTrafficManagerProfileName <String>]`: Имя создаваемого профиля диспетчера трафика. Это требуется, только если профиль диспетчера трафика еще не существует.
  - `[Config <ISiteConfig>]`: Конфигурация приложения.
    - `IsPushEnabled <Boolean>`: Получает или задает флаг, указывающий, включена ли конечная точка отправки.
    - `[ActionMinProcessExecutionTime <String>]`: Минимальное время выполнения процесса перед принятием действия
    - `[ActionType <AutoHealActionType?>]`: Предопределенные действия, которые необходимо выполнить.
    - `[AlwaysOn <Boolean?>]`: <code>true</code> Если включена постоянная, в противном случае <code>false</code> .
    - `[ApiDefinitionUrl <String>]`: URL-адрес определения API.
    - `[ApiManagementConfigId <String>]`: APIM-Api идентификатор.
    - `[AppCommandLine <String>]`: Командная строка приложения для запуска.
    - `[AppSetting <INameValuePair[]>]`: Параметры приложения.
      - `[Name <String>]`: Имя пары.
      - `[Value <String>]`: Значение пары.
    - `[AutoHealEnabled <Boolean?>]`: <code>true</code> Если включена функция автоматического автосохранения; в противном случае <code>false</code> .
    - `[AutoSwapSlotName <String>]`: Имя слота автоматического подстановки.
    - `[ConnectionString <IConnStringInfo[]>]`: Строки подключения.
      - `[ConnectionString <String>]`: Строковое значение подключения.
      - `[Name <String>]`: Имя строки подключения.
      - `[Type <ConnectionStringType?>]`: Тип базы данных.
    - `[CorAllowedOrigin <String[]>]`: Возвращает или задает список источников, для которых должны быть разрешены межисточникические вызовы (например: http://example.com:12345) . Используйте "*" для разрешения всех.
    - `[CorSupportCredentials <Boolean?>]`: Получает или задает допустимые ли запросы CORS с учетными данными. https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentialsДля получения дополнительных сведений см.
    - `[CustomActionExe <String>]`: Исполняемый файл для запуска.
    - `[CustomActionParameter <String>]`: Параметры для исполняемого файла.
    - `[DefaultDocument <String[]>]`: Документы по умолчанию.
    - `[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> Если включено подробный журнал ошибок; в противном случае <code>false</code> .
    - `[DocumentRoot <String>]`: Корневой каталог документа.
    - `[DynamicTagsJson <String>]`: Возвращает или задает строку JSON, содержащую список динамических тегов, которые будут вычислены из утверждений пользователей в конечной точке регистрации принудительной отправки.
    - `[ExperimentRampUpRule <IRampUpRule[]>]`: Список правил увеличения.
      - `[ActionHostName <String>]`: Hostname (область), на который будет перенаправляться трафик, если это необходимо. Сокращен. myapp-stage.azurewebsites.net.
      - `[ChangeDecisionCallbackUrl <String>]`: Настраиваемый алгоритм принятия решений можно задать в расширении сайта TiPCallback, который можно указать URL-адресу. TiPCallback для формирования шаблонов и контрактов: расширение сайта.         https://www.siteextensions.net/packages/TiPCallback/
      - `[ChangeIntervalInMinute <Int32?>]`: Определяет интервал в минутах для повторного вычисления ReroutePercentage.
      - `[ChangeStep <Double?>]`: В сценарии автоматического увеличения можно добавить/удалить из <code>ReroutePercentage</code> него, пока он не достигнет значения \n <code>MinReroutePercentage</code> или         <code>MaxReroutePercentage</code> . Показатели сайтов проверяются каждые N минут, указанных в <code>ChangeIntervalInMinutes</code> .\nCustom алгоритме принятия решений, могут быть указаны в TiPCallback сайте расширение сайта, в котором можно указать URL-адрес <code>ChangeDecisionCallbackUrl</code> .
      - `[MaxReroutePercentage <Double?>]`: Определяет верхнюю нижнюю границу, в которой ReroutePercentage остается.
      - `[MinReroutePercentage <Double?>]`: Определяет нижнюю границу, над которой ReroutePercentage остается.
      - `[Name <String>]`: Имя правила маршрутизации. Рекомендуемое имя должно указывать на слот, который будет принимать трафик в эксперименте.
      - `[ReroutePercentage <Double?>]`: Процент трафика, на который будут перенаправляться <code>ActionHostName</code> .
    - `[FtpsState <FtpsState?>]`: Состояние службы FTP/FTPS
    - `[HandlerMapping <IHandlerMapping[]>]`: Сопоставления обработчиков.
      - `[Argument <String>]`: Аргументы командной строки, передаваемые в обработчик сценария.
      - `[Extension <String>]`: Запросы с этим расширением будут обрабатываться с помощью указанного приложения FastCGI.
      - `[ScriptProcessor <String>]`: Абсолютный путь к приложению FastCGI.
    - `[HealthCheckPath <String>]`: Путь проверки работоспособности
    - `[Http20Enabled <Boolean?>]`: Http20Enabled: Настройка веб-сайта, разрешающего клиентам подключаться по протоколу HTTP 2.0
    - `[HttpLoggingEnabled <Boolean?>]`: <code>true</code> Если ведение журнала HTTP включено; в противном случае <code>false</code> .
    - `[IPSecurityRestriction <IIPSecurityRestriction[]>]`: Ограничения IP-безопасности для main.
      - `[Action <String>]`: Разрешение или запрет доступа для этого диапазона IP-адресов.
      - `[Description <String>]`: Описание правила ограничения IP-адресов.
      - `[IPAddress <String>]`: IP-адрес, для которого действует ограничение безопасности.         Это может быть только адрес IPv4 (обязательный свойство подсети) или нотация CIDR, например IPv4/маска (первое соответствие разрядов). Свойство "маска подсети" не должно быть задано для CIDR.
      - `[Name <String>]`: Имя правила ограничения IP-адресов.
      - `[Priority <Int32?>]`: Приоритет правила ограничения IP-адресов.
      - `[SubnetMask <String>]`: Маска подсети для диапазона IP-адресов, для которого допустимы ограничения.
      - `[SubnetTrafficTag <Int32?>]`: (внутренняя) тег "трафик" подсети
      - `[Tag <IPFilterTag?>]`: Определяет, для чего будет использоваться этот IP-фильтр. Это необходимо для поддержки фильтрации IP на прокси-серверах.
      - `[VnetSubnetResourceId <String>]`: Идентификатор ресурса виртуальной сети
      - `[VnetTrafficTag <Int32?>]`: (внутренняя) тег "трафик виртуальной сети"
    - `[JavaContainer <String>]`: Контейнер Java.
    - `[JavaContainerVersion <String>]`: Версия контейнера Java.
    - `[JavaVersion <String>]`: Версия Java.
    - `[LimitMaxDiskSizeInMb <Int64?>]`: Максимально допустимое использование размера диска (МБ).
    - `[LimitMaxMemoryInMb <Int64?>]`: Максимально допустимое использование памяти в МЕГАБАЙТах.
    - `[LimitMaxPercentageCpu <Double?>]`: Максимальный разрешенный процент использования ЦП.
    - `[LinuxFxVersion <String>]`: Платформа и версия приложения для Linux
    - `[LoadBalancing <SiteLoadBalancing?>]`: Балансировка нагрузки сайта.
    - `[LocalMySqlEnabled <Boolean?>]`: <code>true</code> для включения Local MySQL; в противном случае <code>false</code> .
    - `[LogsDirectorySizeLimit <Int32?>]`: HTTP-журналы. Ограничение размера каталога.
    - `[MachineKeyDecryption <String>]`: Алгоритм, используемый для расшифровки.
    - `[MachineKeyDecryptionKey <String>]`: Ключ расшифровки.
    - `[MachineKeyValidation <String>]`: Проверка MachineKey.
    - `[MachineKeyValidationKey <String>]`: Ключ проверки.
    - `[ManagedPipelineMode <ManagedPipelineMode?>]`: Режим управляемого конвейера.
    - `[ManagedServiceIdentityId <Int32?>]`: ИД управляемой службы с удостоверением
    - `[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: Настройка минимальной версии TLS, необходимой для запросов SSL
    - `[NetFrameworkVersion <String>]`: Версия .NET Framework.
    - `[NodeVersion <String>]`: Версия Node.js.
    - `[NumberOfWorker <Int32?>]`: Количество сотрудников.
    - `[PhpVersion <String>]`: Версия PHP.
    - `[PowerShellVersion <String>]`: Версия PowerShell.
    - `[PreWarmedInstanceCount <Int32?>]`: Количество заданных экземпляров.         Этот параметр применяется только к планам потребления и эластичных БД
    - `[PublishingUsername <String>]`: Публикация имени пользователя.
    - `[PushKind <String>]`: Типа ресурса.
    - `[PythonVersion <String>]`: Версия Python.
    - `[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> Если включена удаленная отладка, в противном случае <code>false</code> .
    - `[RemoteDebuggingVersion <String>]`: Версия удаленной отладки.
    - `[RequestCount <Int32?>]`: Количество запросов.
    - `[RequestTimeInterval <String>]`: Интервал времени.
    - `[RequestTracingEnabled <Boolean?>]`: <code>true</code> Если трассировка запросов включена; в противном случае <code>false</code> .
    - `[RequestTracingExpirationTime <DateTime?>]`: Запрос времени окончания срока действия трассировки.
    - `[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: Ограничения IP-безопасности для SCM.
    - `[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: Ограничения IP-безопасности для SCM для использования Main.
    - `[ScmType <ScmType?>]`: Тип SCM.
    - `[SlowRequestCount <Int32?>]`: Количество запросов.
    - `[SlowRequestTimeInterval <String>]`: Интервал времени.
    - `[SlowRequestTimeTaken <String>]`: Затраченное время.
    - `[TagWhitelistJson <String>]`: Возвращает или задает строку JSON, содержащую список тегов, которые список разрешений использовать для конечной точки регистрации push-уведомлений.
    - `[TagsRequiringAuth <String>]`: Возвращает или задает строку JSON, содержащую список тегов, для использования которых требуется проверка подлинности пользователя в конечной точке регистрации принудительной отправки.         Теги могут состоять из буквенно-цифровых символов и следующих: "_", "@", "#", ".", ":", "-".         Проверка должна выполняться на PushRequestHandler.
    - `[TracingOption <String>]`: Параметры трассировки.
    - `[TriggerPrivateBytesInKb <Int32?>]`: Правило, основанное на частных байтах.
    - `[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: Правило, основанное на кодах состояния.
      - `[Count <Int32?>]`: Количество запросов.
      - `[Status <Int32?>]`: Код состояния HTTP.
      - `[SubStatus <Int32?>]`: Состояние запроса.
      - `[TimeInterval <String>]`: Интервал времени.
      - `[Win32Status <Int32?>]`: Код ошибки Win32.
    - `[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> использование 32-разрядного рабочего процесса; в противном случае <code>false</code> .
    - `[VirtualApplication <IVirtualApplication[]>]`: Виртуальные приложения.
      - `[PhysicalPath <String>]`: Физический путь.
      - `[PreloadEnabled <Boolean?>]`: <code>true</code> , если предварительная загрузка включена; в противном случае <code>false</code> .
      - `[VirtualDirectory <IVirtualDirectory[]>]`: Виртуальные каталоги для виртуального приложения.
        - `[PhysicalPath <String>]`: Физический путь.
        - `[VirtualPath <String>]`: Путь к виртуальному приложению.
      - `[VirtualPath <String>]`: Виртуальный путь.
    - `[VnetName <String>]`: Имя виртуальной сети.
    - `[WebSocketsEnabled <Boolean?>]`: <code>true</code> Если WebSocket включен; в противном случае <code>false</code> .
    - `[WindowsFxVersion <String>]`: Платформа и версия приложения ксеноновой
    - `[XManagedServiceIdentityId <Int32?>]`: Явный идентификатор удостоверения управляемой службы
  - `[ContainerSize <Int32?>]`: Размер контейнера функций.
  - `[DailyMemoryTimeQuota <Int32?>]`: Максимально допустимая дневная квота памяти (применимо только к динамическим приложениям).
  - `[Enabled <Boolean?>]`: <code>true</code> Если приложение включено; в противном случае — <code>false</code> . Если задать для этого параметра значение false, приложение будет отключено (приложение переводится в автономный режим).
  - `[HostNameSslState <IHostNameSslState[]>]`: Состояния SSL hostname используются для управления привязками SSL для имен узлов приложения.
    - `[HostType <HostType?>]`: Указывает, является ли имя хоста стандартным или именем репозитория.
    - `[Name <String>]`Имена.
    - `[SslState <SslState?>]`: Тип SSL.
    - `[Thumbprint <String>]`: Отпечаток сертификата SSL.
    - `[ToUpdate <Boolean?>]`: Установите для <code>true</code> обновления существующего hostname.
    - `[VirtualIP <String>]`: Виртуальный IP-адрес, назначенный имени узла, если включен SSL на основе IP.
  - `[HostNamesDisabled <Boolean?>]`: <code>true</code> Отключение общедоступных имен узлов для приложения; в противном случае <code>false</code> .          Если <code>true</code> приложение доступно только через процесс управления API.
  - `[HostingEnvironmentProfileId <String>]`: Идентификатор ресурса среды службы приложений.
  - `[HttpsOnly <Boolean?>]`: HttpsOnly: Настройка веб-сайта для приема только запросов HTTPS. Перенаправление вопросов для HTTP-запросов
  - `[HyperV <Boolean?>]`: Песочница Hyper-V.
  - `[IdentityType <ManagedServiceIdentityType?>]`: Тип удостоверения управляемой службы.
  - `[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: Список удостоверений пользователей, связанных с ресурсом. Ссылки на ключи словаря удостоверения пользователя будут идентификаторами ресурсов ARM в форме: "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}
    - `[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: Это указывает на то, что в этот объект можно добавить любое свойство.
  - `[IsXenon <Boolean?>]`: Устарело: Песочница Hyper-V.
  - `[RedundancyMode <RedundancyMode?>]`: Режим избыточности сайта
  - `[Reserved <Boolean?>]`: <code>true</code> по зарезервированному; в противном случае <code>false</code> .
  - `[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> чтобы остановить сайт SCM (KUDU), когда приложение остановлено, в противном случае <code>false</code> . По умолчанию используется значение <code>false</code> .
  - `[ServerFarmId <String>]`: Идентификатор ресурса связанного плана служб приложений, отформатированный как "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

