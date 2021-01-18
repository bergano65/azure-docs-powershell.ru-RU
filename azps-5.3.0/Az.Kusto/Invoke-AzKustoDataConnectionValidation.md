---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodataconnectionvalidation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDataConnectionValidation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDataConnectionValidation.md
ms.openlocfilehash: fa75072cdb29d7aedc7a78ba4e20950b904f1c7f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518329"
---
# Invoke-AzKustoDataConnectionValidation

## SYNOPSIS
Проверяет, действительны ли параметры подключения к данным.

## СИНТАКСИС

### DataExpandedEventHub (по умолчанию)
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -EventHubResourceId <String>
 -Kind <Kind> -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### DataExpandedEventGrid
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -EventHubResourceId <String>
 -Kind <Kind> -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### DataExpandedIotHub
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -IotHubResourceId <String>
 -Kind <Kind> -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### DataViaIdentityExpandedEventGrid
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -EventHubResourceId <String> -Kind <Kind> -Location <String>
 -StorageAccountResourceId <String> [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### DataViaIdentityExpandedEventHub
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -EventHubResourceId <String> -Kind <Kind> -Location <String>
 [-Compression <Compression>] [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### DataViaIdentityExpandedIotHub
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -IotHubResourceId <String> -Kind <Kind> -Location <String>
 -SharedAccessPolicyName <String> [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### UpdateExpandedEventGrid
```
Invoke-AzKustoDataConnectionValidation -ConsumerGroup <String> -DataConnectionName <String> -Kind <Kind>
 -Location <String> [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### UpdateViaIdentityExpandedEventGrid
```
Invoke-AzKustoDataConnectionValidation -ConsumerGroup <String> -DataConnectionName <String> -Kind <Kind>
 -Location <String> [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## ОПИСАНИЕ
Проверяет, действительны ли параметры подключения к данным.

## ПРИМЕРЫ

### Пример 1. Проверка параметров подключения к данным EventHub
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location "East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

Команда выше проверяет подключение к данным EventHub с именем "myeventhubdc" для базы данных mykustodatabase в кластере testnewkustocluster.

### Пример 2. Проверка параметров подключения к данным EventGrid
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location "East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

Команда выше проверяет подключение к данным EventGrid "myeventgriddc" для базы данных mykustodatabase в кластере testnewkustocluster.

### Пример 3. Проверка параметров подключения к данным IotHub
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location "East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

Команда выше проверяет подключение к данным IotHub с именем myiothubdc для базы данных mykustodatabase в кластере testnewkustocluster.

### Пример 4. Проверка параметров подключения к данным EventHub с помощью удостоверения
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" 
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myeventhubdc" -Location "East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

Команда выше проверяет подключение к данным EventHub с именем "myeventhubdc" для базы данных mykustodatabase в кластере testnewkustocluster.

### Пример 5. Проверка параметров подключения к данным EventGrid с помощью удостоверения
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase"
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myeventgriddc" -Location "East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

Команда выше проверяет подключение к данным EventGrid с именем myeventgriddc для базы данных mykustodatabase в кластере testnewkustocluster.

### Пример 6. Проверка параметров подключения к данным IotHub с помощью удостоверения
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" 
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myiothubdc" -Location "East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

Команда выше проверяет подключение к данным IotHub с именем myiothubdc для базы данных mykustodatabase в кластере testnewkustocluster.

## PARAMETERS

### -BlobStorageEventType
Имя обработки события типа события хранилища BLOB-типов.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.BlobStorageEventType
Parameter Sets: UpdateExpandedEventGrid, UpdateViaIdentityExpandedEventGrid
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClusterName
Название кластера "Кусто".

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Сжатие
Тип сжатия сообщений в центре событий.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Compression
Parameter Sets: DataExpandedEventHub, DataViaIdentityExpandedEventHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConsumerGroup
Группа потребительских событий/iot-концентратора.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseName
Имя базы данных в кластере Кусто.

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DataConnectionName
Имя подключения к данным.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DataFormat
Формат данных сообщения.
При желании формат данных можно добавить в каждое сообщение.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.EventGridDataFormat
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -EventHubResourceId
ИД ресурса в центре событий, который будет использоваться для создания подключения к данным или сетки событий, настроен для отправки событий.

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataViaIdentityExpandedEventGrid, DataViaIdentityExpandedEventHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EventSystemProperty
Системные свойства концентратора событий и iot.

```yaml
Type: System.String[]
Parameter Sets: DataExpandedEventHub, DataExpandedIotHub, DataViaIdentityExpandedEventHub, DataViaIdentityExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IgnoreFirstRecord
Если зафиксировать это, означает, что при чтении следует игнорировать первую запись каждого файла.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateExpandedEventGrid, UpdateViaIdentityExpandedEventGrid
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DataViaIdentityExpandedEventGrid, DataViaIdentityExpandedEventHub, DataViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -IotHubResourceId
ИД ресурса концентратора IOT, который будет использоваться для создания подключения к данным.

```yaml
Type: System.String
Parameter Sets: DataExpandedIotHub, DataViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kind
Тип конечной точки для подключения к данным

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location
Расположение ресурса.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MappingRuleName
Правило сопоставления, используемее для передачи данных.
При желании сведения о сопоставлении можно добавить в каждое сообщение.

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
Имя группы ресурсов, содержащей кластер Кусто.

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SharedAccessPolicyName
Имя политики доступа.

```yaml
Type: System.String
Parameter Sets: DataExpandedIotHub, DataViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountResourceId
ИД ресурса учетной записи хранения, в которой находятся данные.

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataViaIdentityExpandedEventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.
Он является частью URI каждого звонка службы.

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -TableName
Таблица, в которой нужно ввести данные.
При желании в каждое сообщение можно добавить сведения из таблицы.

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

### -Confirm
Запрос на подтверждение перед запуском cmdlet.

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

### Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity

## OUTPUTS

### Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnectionValidationResult

## ПРИМЕЧАНИЯ

ALIASES

СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ

Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства. Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.


INPUTOBJECT <IKustoIdentity> : Параметр identity
  - `[AttachedDatabaseConfigurationName <String>]`: имя конфигурации вложенной базы данных.
  - `[ClusterName <String>]`Название кластера "Кусто".
  - `[DataConnectionName <String>]`: имя подключения к данным.
  - `[DatabaseName <String>]`Имя базы данных в кластере Кусто.
  - `[Id <String>]`: путь удостоверения ресурса
  - `[Location <String>]`: расположение в Azure.
  - `[PrincipalAssignmentName <String>]`: Имя «Кусто principalAssignment».
  - `[ResourceGroupName <String>]`Название группы ресурсов, содержащей кластер Кусто.
  - `[SubscriptionId <String>]`: получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure. Он является частью URI каждого звонка службы.

## СВЯЗАННЫЕ ССЫЛКИ

