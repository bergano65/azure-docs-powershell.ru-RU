---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionApp.md
ms.openlocfilehash: 08485ab1686b87c6421f456b53caa5d1deaf0c7d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401295"
---
# Update-AzFunctionApp

## SYNOPSIS
Обновляет приложение функций.

## СИНТАКСИС

### ByName (по умолчанию)
```
Update-AzFunctionApp -Name <String> -ResourceGroupName <String> [-ApplicationInsightsKey <String>]
 [-ApplicationInsightsName <String>] [-IdentityID <String>] [-IdentityType <ManagedServiceIdentityType>]
 [-PlanName <String>] [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ByObjectInput
```
Update-AzFunctionApp -InputObject <ISite> [-ApplicationInsightsKey <String>]
 [-ApplicationInsightsName <String>] [-IdentityID <String>] [-IdentityType <ManagedServiceIdentityType>]
 [-PlanName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## ОПИСАНИЕ
Обновляет приложение функций.

## ПРИМЕРЫ

### Пример 1. Обновление плана размещения приложений с функцией.
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -PlanName NewPlanName 
```

Эта команда обновляет план размещения приложений.

### Пример 2. Настройка управляемого удостоверения SystemAssigned для приложения функции.
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -IdentityType SystemAssigned 
```

Эта команда задает управляемое удостоверение SystemAssigned для приложения функции.

### Пример 3. Обновление функции приложения Application Insights.
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -ApplicationInsightsName ApplicationInsightsProjectName 
```

Эта команда обновляет функцию application Insights приложения.

### Пример 3. Удаление управляемых удостоверений из приложения с функцией.
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -IdentityType None 
```

Эта команда удаляет управляемое удостоверение из приложения function.

## PARAMETERS

### -ApplicationInsightsKey
Ключ инструментов для анализа приложений, который нужно добавить.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppInsightsKey

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationInsightsName
Имя существующего проекта App Insights, который нужно добавить в приложение функций.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppInsightsName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJob
Выполняется в качестве фонового задания.

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

### -DefaultProfile


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

### -IdentityID
Определяет список удостоверений пользователей, связанных с приложением функции.
Ссылки на удостоверения пользователей будут ARM ресурса в форме: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IdentityType
Определяет тип удостоверения, используемого для приложения функции.
Тип "Нет" удаляет все удостоверения из приложения функции.
Допустимыми значениями для этого параметра являются: - SystemAssigned - UserAssigned - None

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Support.ManagedServiceIdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Сведения о конструкции см. в разделе "Заметки" свойств INPUTOBJECT и создании таблицы с hash.

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

### -Name
Имя приложения функции.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait
Начинает операцию и возвращает ее немедленно до ее завершения.
Чтобы определить успешное завершение операции, используйте другой механизм.

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

### -PlanName
Название плана обслуживания.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
ИД подписки Azure.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Теги ресурсов.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Перед запуском cmdlet вам будет предложено подтвердить его.

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
Показывает, что произойдет при запуске cmdlet.
Этот cmdlet не будет выполниться.

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
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite

## OUTPUTS

### Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite

## ПРИМЕЧАНИЯ

ALIASES

СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ

Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства. Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.


<ISite>INPUTOBJECT: 
  - `Location <String>`: Расположение ресурса.
  - `CloningInfoSourceWebAppId <String>`: ARM ресурса в приложении-источнике. ИД ресурса приложения имеет форму /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} для производственных слотов и /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} для других слотов.
  - `[Kind <String>]`: Тип ресурса.
  - `[Tag <IResourceTags>]`: теги ресурсов.
    - `[(Any) <String>]`— это означает, что к этому объекту можно добавить любое свойство.
  - `[ClientAffinityEnabled <Boolean?>]`: включить клиентские сходства; прекратить отправку файлов cookie сеанса, которые будут отправлять запросы клиентов в том же сеансе <code>true</code> <code>false</code> в тот же экземпляр. Значение по умолчанию <code>true</code> .
  - `[ClientCertEnabled <Boolean?>]`: <code>true</code> чтобы включить проверку подлинности сертификата клиента (внося в TLS вся проверка подлинности); в противном случае <code>false</code> . Значение по умолчанию <code>false</code> .
  - `[ClientCertExclusionPath <String>]`: пути исключения, разделенные запятой для проверки подлинности сертификата клиента
  - `[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: параметры приложений переопределяются для клонированных приложений. При этом эти параметры переопределяют параметры, клонированные из приложения-источника. В противном случае параметры приложения из источника сохраняются.
    - `[(Any) <String>]`— это означает, что к этому объекту можно добавить любое свойство.
  - `[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> чтобы клонировать пользовательские имена хостов из source app; в противном <code>false</code> случае.
  - `[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> чтобы клонировать управление исходным источником из source app; в противном случае <code>false</code> .
  - `[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> чтобы настроить балансировку нагрузки для приложения для назначения и источника.
  - `[CloningInfoCorrelationId <String>]`: Correlation ID of cloning operation. Этот ID связывает несколько операций клонирования, чтобы использовать один и тот же моментальный снимок.
  - `[CloningInfoHostingEnvironment <String>]`: Среда службы приложений.
  - `[CloningInfoOverwrite <Boolean?>]`: <code>true</code> чтобы переписать приложение; в противном случае <code>false</code> .
  - `[CloningInfoSourceWebAppLocation <String>]`: Расположение source app ex: West US or North Europe
  - `[CloningInfoTrafficManagerProfileId <String>]`: ARM ресурса профиля Диспетчера трафика, если он существует. Код ресурса Диспетчера трафика имеет форму /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.
  - `[CloningInfoTrafficManagerProfileName <String>]`: Имя профиля Диспетчера трафика, который нужно создать. Это необходимо только в том случае, если профиль Диспетчера трафика еще не существует.
  - `[Config <ISiteConfig>]`: Настройка приложения.
    - `IsPushEnabled <Boolean>`: получает или устанавливает флажок, указывающий, включена ли конечная точка push-сигнала.
    - `[ActionMinProcessExecutionTime <String>]`: минимальное время, необходимое для выполнения процесса перед выполнением действия
    - `[ActionType <AutoHealActionType?>]`: Предопределированное действие.
    - `[AlwaysOn <Boolean?>]`: <code>true</code> если включена always on; в противном случае <code>false</code> .
    - `[ApiDefinitionUrl <String>]`URL-адрес определения API.
    - `[ApiManagementConfigId <String>]`: APIM-Api идентификатора.
    - `[AppCommandLine <String>]`: запуск командной строки приложения.
    - `[AppSetting <INameValuePair[]>]`: Параметры приложения.
      - `[Name <String>]`: Парное имя.
      - `[Value <String>]`: Парный значение.
    - `[AutoHealEnabled <Boolean?>]`: <code>true</code> если автосъемка включена; в противном случае <code>false</code> .
    - `[AutoSwapSlotName <String>]`: название разъема для автоматического обмена.
    - `[ConnectionString <IConnStringInfo[]>]`: строки подключения.
      - `[ConnectionString <String>]`: строка подключения.
      - `[Name <String>]`: Имя строки подключения.
      - `[Type <ConnectionStringType?>]`: Тип базы данных.
    - `[CorAllowedOrigin <String[]>]`: получает или задает список источников, которые должны быть разрешены для звонков в перекрестных источниках (например: http://example.com:12345) . Используйте "*", чтобы разрешить все.
    - `[CorSupportCredentials <Boolean?>]`: получает или устанавливает, разрешено ли запросы CORS с учетными данными. Дополнительные         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         сведения см. в этой информации.
    - `[CustomActionExe <String>]`: исполняемый для выполнения.
    - `[CustomActionParameter <String>]`: Параметры исполняемого исполняемого параметров.
    - `[DefaultDocument <String[]>]`: Документы по умолчанию.
    - `[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> если включено подробное ведение журнала ошибок; в противном случае <code>false</code> .
    - `[DocumentRoot <String>]`: корневой документ.
    - `[DynamicTagsJson <String>]`: возвращает или задает строку JSON, содержащую список динамических тегов, которые будут вычисляться из утверждений пользователей на конечной точке push-регистрации.
    - `[ExperimentRampUpRule <IRampUpRule[]>]`: Список правил для работы с новыми бизнес-ами.
      - `[ActionHostName <String>]`: Hostname of a slot, to which the traffic will be redirected if decided to. Например, myapp-stage.azurewebsites.net.
      - `[ChangeDecisionCallbackUrl <String>]`В расширении сайта TiPCallback можно у указывается алгоритм пользовательского решения. Подробнее о scaffold и контрактах см. в расширении сайта TiPCallback.         https://www.siteextensions.net/packages/TiPCallback/
      - `[ChangeIntervalInMinute <Int32?>]`: определяет интервал в минутах для повторного проговаривания ReroutePercentage.
      - `[ChangeStep <Double?>]`. В автоматическом сценарии обнуляйте эту возможность, пока не дойдете до <code>ReroutePercentage</code> \n <code>MinReroutePercentage</code> или         <code>MaxReroutePercentage</code> . Метрики сайта проверяются каждые N минут, указанные в <code>ChangeIntervalInMinutes</code> алгоритме решения .\nCustom, в расширении сайта TiPCallback, в котором можно у указывает URL-адрес. <code>ChangeDecisionCallbackUrl</code>
      - `[MaxReroutePercentage <Double?>]`: указывает верхнюю границу, под которой будет находиться ReroutePercentage.
      - `[MinReroutePercentage <Double?>]`: указывает нижнюю границу, над которой будет находиться ReroutePercentage.
      - `[Name <String>]`: имя правила маршрутки. Рекомендуется указать на слот, в котором будет приниматься трафик в эксперименте.
      - `[ReroutePercentage <Double?>]`: процент трафика, на который будет перенаправлен <code>ActionHostName</code> трафик.
    - `[FtpsState <FtpsState?>]`: состояние FTP или FTPS
    - `[HandlerMapping <IHandlerMapping[]>]`: Сопоставления обработера.
      - `[Argument <String>]`: аргументы командной строки, которые передаются в процессор сценариев.
      - `[Extension <String>]`: Запросы с этим расширением обрабатываются с помощью указанного приложения FastCGI.
      - `[ScriptProcessor <String>]`: абсолютный путь к приложению FastCGI.
    - `[HealthCheckPath <String>]`: путь проверки здоровья
    - `[Http20Enabled <Boolean?>]`Http20Enabled: настройка веб-сайта для разрешения клиентам подключения через http2.0
    - `[HttpLoggingEnabled <Boolean?>]`: если включено ведение журнала <code>true</code> HTTP; в противном случае <code>false</code> .
    - `[IPSecurityRestriction <IIPSecurityRestriction[]>]`: ограничения безопасности IP для основного.
      - `[Action <String>]`. Разрешить или запретить доступ для этого диапазона IP-адресов.
      - `[Description <String>]`: Описание правила ограничения IP.
      - `[IPAddress <String>]`: IP-адрес, на который действует ограничение безопасности.         Оно может быть в чистом ipv4-адресе (обязательном свойстве SubnetMask) или нотации CIDR, например ipv4/mask (совпадение с ведущим битом). Для CIDR свойство SubnetMask не должно быть указано.
      - `[Name <String>]`: имя правила ограничения IP.
      - `[Priority <Int32?>]`: Приоритет правила ограничения IP.
      - `[SubnetMask <String>]`: Маска подсети для диапазона IP-адресов, на которые действует ограничение.
      - `[SubnetTrafficTag <Int32?>]`: (внутренний) тег трафика подсети
      - `[Tag <IPFilterTag?>]`: определяет, для чего будет использоваться этот ФИЛЬТР IP-адресов. Это необходимо для поддержки фильтрации по IP-адресам на прокси-прокси.
      - `[VnetSubnetResourceId <String>]`: ИД виртуального сетевого ресурса
      - `[VnetTrafficTag <Int32?>]`: (внутренний) тег трафика Vnet
    - `[JavaContainer <String>]`: контейнер Java.
    - `[JavaContainerVersion <String>]`: Версия контейнера Java.
    - `[JavaVersion <String>]`: Версия Java.
    - `[LimitMaxDiskSizeInMb <Int64?>]`: Максимальный допустимый размер диска в МБ.
    - `[LimitMaxMemoryInMb <Int64?>]`: Максимальное разрешено использование памяти в МБ.
    - `[LimitMaxPercentageCpu <Double?>]`: Процент использования ЦП (максимально допустимый).
    - `[LinuxFxVersion <String>]`: Linux App Framework и версия
    - `[LoadBalancing <SiteLoadBalancing?>]`: Балансировка нагрузки сайта.
    - `[LocalMySqlEnabled <Boolean?>]`: <code>true</code> чтобы включить локальный MySQL; в противном случае <code>false</code> .
    - `[LogsDirectorySizeLimit <Int32?>]`: ограничение размера каталога http-журналов.
    - `[MachineKeyDecryption <String>]`: алгоритм, используемый для расшифровки.
    - `[MachineKeyDecryptionKey <String>]`: ключ расшифровки.
    - `[MachineKeyValidation <String>]`: Проверка MachineKey.
    - `[MachineKeyValidationKey <String>]`: Ключ проверки.
    - `[ManagedPipelineMode <ManagedPipelineMode?>]`: Управляемый режим конвейера.
    - `[ManagedServiceIdentityId <Int32?>]`: Managed Service Identity Id
    - `[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: настройка минимальной версии TLS, необходимой для SSL-запросов
    - `[NetFrameworkVersion <String>]`: версия .NET Framework.
    - `[NodeVersion <String>]`: версия Node.js.
    - `[NumberOfWorker <Int32?>]`: Количество сотрудников.
    - `[PhpVersion <String>]`: Версия PHP.
    - `[PowerShellVersion <String>]`: версия PowerShell.
    - `[PreWarmedInstanceCount <Int32?>]`: Количество предварительно заранее         Этот параметр применяется только к планам потребления и эластичности.
    - `[PublishingUsername <String>]`: имя пользователя публикации.
    - `[PushKind <String>]`: Тип ресурса.
    - `[PythonVersion <String>]`: Version of Python.
    - `[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> если включена удаленная отладка; в противном случае <code>false</code> .
    - `[RemoteDebuggingVersion <String>]`: Версия удаленного отладки.
    - `[RequestCount <Int32?>]`: Количество запросов.
    - `[RequestTimeInterval <String>]`: Интервал времени.
    - `[RequestTracingEnabled <Boolean?>]`: <code>true</code> если включена трассировка запроса; в противном случае <code>false</code> .
    - `[RequestTracingExpirationTime <DateTime?>]`: запрос на трассировку срока действия.
    - `[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: ограничения безопасности IP-адресов для SCM.
    - `[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: ограничения безопасности IP-адресов для использования основного.
    - `[ScmType <ScmType?>]`: тип SCM.
    - `[SlowRequestCount <Int32?>]`: Количество запросов.
    - `[SlowRequestTimeInterval <String>]`: Интервал времени.
    - `[SlowRequestTimeTaken <String>]`: время, за взятое.
    - `[TagWhitelistJson <String>]`: возвращает или задает строку JSON, содержащую список тегов, которые будут исключены в белый список для использования конечной точкой push-регистрации.
    - `[TagsRequiringAuth <String>]`: возвращает или задает строку JSON, содержащую список тегов, для которых требуется проверка подлинности пользователя в конечной точке push-регистрации.         Теги могут состоять из букв и цифр и следующих знаков: '_', '@', '#', '.', ':', '-'         Проверка должна выполняться в pushRequestHandler.
    - `[TracingOption <String>]`: Параметры трасситуры.
    - `[TriggerPrivateBytesInKb <Int32?>]`: правило, основанное на закрытыхбайтах.
    - `[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: правило, основанное на кодах состояния.
      - `[Count <Int32?>]`: Количество запросов.
      - `[Status <Int32?>]`: код состояния HTTP.
      - `[SubStatus <Int32?>]`: Запросить состояние подгруппы.
      - `[TimeInterval <String>]`: Интервал времени.
      - `[Win32Status <Int32?>]`: код ошибки Win32.
    - `[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> использовать процесс 32-битных сотрудников; в противном случае <code>false</code> .
    - `[VirtualApplication <IVirtualApplication[]>]`: Виртуальные приложения.
      - `[PhysicalPath <String>]`: Физический путь.
      - `[PreloadEnabled <Boolean?>]`: <code>true</code> если включена предварительная загрузка; в противном случае <code>false</code> .
      - `[VirtualDirectory <IVirtualDirectory[]>]`: виртуальные каталоги для виртуального приложения.
        - `[PhysicalPath <String>]`: Физический путь.
        - `[VirtualPath <String>]`: Путь к виртуальному приложению.
      - `[VirtualPath <String>]`: Виртуальный путь.
    - `[VnetName <String>]`: Имя виртуальной сети.
    - `[WebSocketsEnabled <Boolean?>]`: <code>true</code> если webSocket включена; в противном случае <code>false</code> .
    - `[WindowsFxVersion <String>]`: Xenon App Framework и версия
    - `[XManagedServiceIdentityId <Int32?>]`: Explicit Managed Service Identity Id
  - `[ContainerSize <Int32?>]`: Размер контейнера функции.
  - `[DailyMemoryTimeQuota <Int32?>]`: Максимальная квота суточного времени памяти (применима только для динамических приложений).
  - `[Enabled <Boolean?>]`: <code>true</code> если приложение включено; в противном случае <code>false</code> . Если установить для этого значения значение false, приложение отключается (переключает его в автономный режим).
  - `[HostNameSslState <IHostNameSslState[]>]`. Состояния SSL hostname используются для управления привязками SSL для имен хостов приложения.
    - `[HostType <HostType?>]`: указывает, является ли имя хранилищ стандартным или репозиторием.
    - `[Name <String>]`: Hostname ..
    - `[SslState <SslState?>]`: Тип SSL.
    - `[Thumbprint <String>]`: Эскиз SSL-сертификата.
    - `[ToUpdate <Boolean?>]`: Установите этот <code>true</code> код для обновления существующего имени.
    - `[VirtualIP <String>]`: Виртуальный IP-адрес, присвоенный имени хоста, если включен SSL на основе IP-адресов.
  - `[HostNamesDisabled <Boolean?>]`: <code>true</code> чтобы отключить общедоступные имена хостов приложения; в противном случае <code>false</code> .          Если приложение доступно только в процессе управления <code>true</code> API.
  - `[HostingEnvironmentProfileId <String>]`: ИД ресурса среды служб приложений.
  - `[HttpsOnly <Boolean?>]`HttpsOnly: настраивает на веб-сайте прием только http-запросов. Перенаправление вопросов по http-запросам
  - `[HyperV <Boolean?>]`: "песочница Hyper-V".
  - `[IdentityType <ManagedServiceIdentityType?>]`: Тип управляемого удостоверения службы.
  - `[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`Список удостоверений, связанных с ресурсом. Ссылки на ключ словаря удостоверений пользователей будут ARM идентификаторы ресурсов в форме: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}
    - `[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`— это означает, что к этому объекту можно добавить любое свойство.
  - `[IsXenon <Boolean?>]`: Устарело: песочница Hyper-V.
  - `[RedundancyMode <RedundancyMode?>]`: режим избыточности сайта
  - `[Reserved <Boolean?>]`: <code>true</code> если зарезервирован; в противном <code>false</code> случае.
  - `[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> чтобы остановить сайт SCM (KUDU), когда приложение остановлено; в противном <code>false</code> случае. Значение по умолчанию <code>false</code> : .
  - `[ServerFarmId <String>]`: Код ресурса связанного плана службы приложения в формате "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".

## СВЯЗАННЫЕ ССЫЛКИ

