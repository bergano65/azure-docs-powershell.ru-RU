---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 587e42ac4c9f318ff46381fdef5b09fa7ce55b63
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214804"
---
# Get-AzEventGridSubscription

## SYNOPSIS
Получает сведения о подписке на событие или список всех подписок на события в текущей подписке Azure.

## СИНТАКСИС

### EventSubscriptionTopicNameParameterSet (по умолчанию)
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-TopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdEventSubscriptionParameterSet
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceId] <String> [-IncludeFullEndpointUrl]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionDomainNameParameterSet
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-DomainName <String>] [-DomainTopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>]
 [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionTopicTypeNameParameterSet
```
Get-AzEventGridSubscription [-ResourceGroupName <String>] [-TopicTypeName <String>] [-Location <String>]
 [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### EventSubscriptionCustomTopicInputObjectParameterSet
```
Get-AzEventGridSubscription [-InputObject] <PSTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionDomainInputObjectParameterSet
```
Get-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionDomainTopicInputObjectParameterSet
```
Get-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### NextLinkParameterSet
```
Get-AzEventGridSubscription [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## ОПИСАНИЕ
Этот Get-AzEventGridSubscription возвращает сведения о указанной подписке на сетку событий или список всех подписок на сетку событий в текущей подписке Azure или группе ресурсов.
Если за предоставлено название подписки на событие, возвращаются сведения об отдельной подписке на сетку событий.
Если название подписки на событие не предоставлено, возвращается список всех подписок на события. Количество элементов, возвращаемых в этом списке, управляется параметром Top. Если значение "Верхнее" не указано или $null, в списке будут указаны все элементы подписки на события. В противном случае top будет указывать максимальное количество элементов, которые будут возвращены в списке.
Если по-прежнему доступны дополнительные подписки на события, значение в NextLink следует использовать в следующем звонке, чтобы получить следующую страницу подписок на события.
Наконец, параметр ODataQuery используется для фильтрации результатов поиска. Запрос фильтрации следует за синтаксисом OData, используя только свойство Name. Поддерживаются следующие операции: CONTAINS, eq (для равно), ne (для не равно), AND, OR и NOT.

## ПРИМЕРЫ

### Пример 1
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

Сведения о подписке на событие EventSubscription1, созданной для темы "Тема1" в группе ресурсов \` \` \` \` \` MyResourceGroupName. \`

### Пример 2
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

Получает сведения о подписке на событие EventSubscription1, созданной для темы "Тема1" в группе ресурсов \` \` \` \` \` MyResourceGroupName, включая полный URL-адрес конечной точки, если это подписка на событие на основе \` webhook.

### Пример 3
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

Получите список всех подписок на события, созданные для темы "Тема1", в группе ресурсов \` \` \` MyResourceGroupName \` без разрежения.

### Пример 4
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Со списком первых 10 подписок на события (если таковые есть), созданных для темы "Тема1", в группе ресурсов \` \` \` MyResourceGroupName, которая удовлетворяет $odataFilter \` запросу. Если доступно больше результатов, $result. NextLink не будет $null. Чтобы получить следующую страницу подписки на события, пользователь должен повторно позвонить в Get-AzEventGridSubscription и использует результат. NextLink, полученные в предыдущем звонке. Звонок должен остановиться в результатах. NextLink становится $null.

### Пример 5
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

Получает сведения о подписке \` на событие EventSubscription1, созданной для группы \` ресурсов \` MyResourceGroupName. \`

### Пример 6
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

Получает сведения о подписке \` на событие EventSubscription1, \` созданной для выбранной подписки Azure.

### Пример 7
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

Список всех подписок на глобальные события, созданные в группе ресурсов \` MyResourceGroupName \` без разрежения.

### Пример 8
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Top 5 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Со списком первых 5 подписок на события (если таковые есть), созданных в группе ресурсов \` MyResourceGroupName, удовлетворяющий $odataFilter \` запросу. Если доступно больше результатов, $result. NextLink не будет $null. Чтобы получить следующую страницу подписки на события, пользователь должен повторно позвонить в Get-AzEventGridSubscription и использует результат. NextLink, полученные в предыдущем звонке. Звонок должен остановиться в результатах. NextLink становится $null.

### Пример 9
```powershell
PS C:\> Get-AzEventGridSubscription
```

Возвращает список всех подписок на глобальные события, созданные в выбранной подписке Azure без разрывления на них разрывений.

### Пример 10
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Список первых 15 подписок на глобальные события (если они есть), созданных в выбранной подписке Azure, которая удовлетворяет запросу $odataFilter событий. Если доступно больше результатов, $result. NextLink не будет $null. Чтобы получить следующую страницу подписки на события, пользователь должен повторно позвонить в Get-AzEventGridSubscription и использует результат. NextLink, полученные в предыдущем звонке. Звонок должен остановиться в результатах. NextLink становится $null.

### Пример 11
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

Получает список всех подписок на региональные события, созданные в группе ресурсов MyResourceGroupName в указанном расположении \` \` \` westus2 \` без разрежения.

### Пример 12
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2 -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Перечислите первые 15 подписок на региональные события (если таковые есть), созданные в группе ресурсов MyResourceGroupName в указанном расположении \` \` \` westus2, удовлетворяющий $odataFilter \` запросу. Если доступно больше результатов, $result. NextLink не будет $null. Чтобы получить следующую страницу подписки на события, пользователь должен повторно позвонить в Get-AzEventGridSubscription и использует результат. NextLink, полученные в предыдущем звонке. Звонок должен остановиться в результатах. NextLink становится $null.

### Пример 13
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

Возвращает список всех подписок на события, созданные для указанного пространства имен EventHub без разбиения на разбиение на нее.

### Пример 14
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" -Top 25 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Со списком первых 25 подписок на события (если они есть), созданных для указанного пространства имен EventHub, удовлетворяющий $odataFilter запросу. Если доступно больше результатов, $result. NextLink не будет $null. Чтобы получить следующую страницу подписки на события, пользователь должен повторно позвонить в Get-AzEventGridSubscription и использует результат. NextLink, полученные в предыдущем звонке. Звонок должен остановиться в результатах. NextLink становится $null.

### Пример 15
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

Возвращает список всех подписок на события, созданные для определенного типа темы (пространства имен EventHub) в указанном расположении без разбиения на разделы.

### Пример 16
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Список первых 15 подписок на события (если они есть), созданные для указанного типа темы (пространства имен EventHub) в указанном расположении, которое удовлетворяет запросу $odataFilter событий. Если доступно больше результатов, $result. NextLink не будет $null. Чтобы получить следующую страницу подписки на события, пользователь должен повторно позвонить в Get-AzEventGridSubscription и использует результат. NextLink, полученные в предыдущем звонке. Звонок должен остановиться в результатах. NextLink становится $null.

### Пример 17
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

Возвращает список всех подписок на события, созданные для определенной группы ресурсов без разрывления на них разрывений.

### Пример 18
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName -Top 100 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Со списком первых 100 подписок на события (если они есть), созданных для определенной группы ресурсов, которая удовлетворяет $odataFilter запросу. Если доступно больше результатов, $result. NextLink не будет $null. Чтобы получить следующую страницу подписки на события, пользователь должен повторно позвонить в Get-AzEventGridSubscription и использует результат. NextLink, полученные в предыдущем звонке. Звонок должен остановиться в результатах. NextLink становится $null.

## PARAMETERS

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainInputObject
Объект EventGrid Domain.

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: EventSubscriptionDomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DomainName
Доменное имя EventGrid.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DomainTopicInputObject
Объект EventGrid Domain Topic.

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic
Parameter Sets: EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DomainTopicName
Имя темы домена EventGrid.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EventSubscriptionName
Название подписки на событие

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IncludeFullEndpointUrl
Включив полный URL-адрес конечной точки назначения подписки на событие.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Объект EventGrid Topic.

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Location
Расположение

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NextLink
Ссылка на следующую страницу ресурсов, которые нужно получить. Это значение получается при первом Get-AzEventGrid, когда для запроса остается доступно больше ресурсов.

```yaml
Type: System.String
Parameter Sets: NextLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ODataQuery
Запрос OData, используемый для фильтрации результатов списка. Фильтрация в настоящее время разрешена только для свойства Name. Поддерживаются следующие операции: CONTAINS, eq (для равно), ne (для не равно), AND, OR и NOT.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Идентификатор ресурса, для которого созданы подписки на события.

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Top
Запрос OData, используемый для фильтрации результатов списка. Фильтрация в настоящее время разрешена только для свойства Name. Поддерживаются следующие операции: CONTAINS, eq (для равно), ne (для не равно), AND, OR и NOT.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TopicName
Имя темы EventGrid.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TopicTypeName
Имя TopicType

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

### Microsoft.Azure.Commands.EventGrid.Models.PSTopic

### Microsoft.Azure.Commands.EventGrid.Models.PSDomain

### Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic

### System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]

## OUTPUTS

### Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ
