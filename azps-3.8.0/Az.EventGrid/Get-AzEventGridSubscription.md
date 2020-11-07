---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 5adc6e203166903b0c76d906ce03cd72cb73c3d4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912270"
---
# Get-AzEventGridSubscription

## КРАТКИй обзор
Получает сведения о подписке на события или возвращает список всех подписок на события в текущей подписке Azure.

## Максимальное

### EventSubscriptionTopicNameParameterSet (по умолчанию)
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [[-ResourceGroupName] <String>]
 [[-TopicName] <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdEventSubscriptionParameterSet
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [-ResourceId] <String>
 [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### EventSubscriptionDomainNameParameterSet
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [[-ResourceGroupName] <String>]
 [-DomainName <String>] [-DomainTopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>]
 [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionTopicTypeNameParameterSet
```
Get-AzEventGridSubscription [[-ResourceGroupName] <String>] [[-TopicTypeName] <String>] [[-Location] <String>]
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

## NОПИСАНИЕ
Командлет Get-AzEventGridSubscription получает либо сведения о заданной подписке на сетку событий, либо список всех подписок на сетку событий в текущей подписке или группе ресурсов Azure.
Если задано имя подписки на событие, возвращается информация об одной подписке на сетку событий.
Если имя подписки на событие не указано, возвращается список всех подписок на события. Количество элементов, возвращенных в этом списке, управляется параметром Top. Если значение Top не указано или $null, список будет содержать все элементы подписки на события. В противном случае в поле Top будет указано максимальное число элементов, возвращаемых в списке.
Если по-прежнему доступны дополнительные подписки на события, значение в NextLink следует использовать при следующем вызове для получения следующей страницы подписок на события.
Наконец, параметр ODataQuery используется для выполнения фильтрации результатов поиска. Запрос фильтрации следует за синтаксисом OData, используя только свойство Name. Поддерживаются следующие операции: CONTAINS, EQ (для равенства), NE (неравенство), и, или, или нет.

## ИЛЛЮСТРИРУЮТ

### Пример 1
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

Получает сведения о подписке \` на события EventSubscription1, \` созданной для \` элемент1 темы \` в группе ресурсов \` MyResourceGroupName \` .

### Пример 2
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

Получает подробные сведения о подписке \` на события EventSubscription1 \` , созданные для темы \` элемент1 \` в группе ресурсов \` MyResourceGroupName \` , включая полный URL-адрес конечной точки, если он является подпиской на события на основе веб-перехватчика.

### Пример 3
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

Получение списка всех подписок на события, созданных для темы \` элемент1 \` в группе ресурсов \` MyResourceGroupName \` без разбивки на страницы.

### Пример 4
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Список первых 10 подписок на события (если таковые имеются), созданных для темы \` элемент1 \` в группе ресурсов \` MyResourceGroupName \` , которые удовлетворяют $odataFilter запросу. Если доступны дополнительные результаты, $result. NextLink не будет $null. Чтобы получить следующие страницы подписок на события, предполагается, что пользователь повторно вызывает Get-AzEventGridSubscription и использует результат. NextLink, полученный в результате предыдущего звонка. Вызывающий объект должен остановиться по результатам. NextLink становится $nullом.

### Пример 5
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

Получает подробные сведения о подписке на события \` EventSubscription1 \` , созданные для группы ресурсов \` MyResourceGroupName \` .

### Пример 6
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

Получает подробные сведения о подписке \` на события EventSubscription1 \` , созданные для выбранной в данный момент подписки Azure.

### Пример 7
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

Получает список всех глобальных подписок на события, созданных в группе ресурсов \` MyResourceGroupName \` без разбивки на страницы.

### Пример 8
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Top 5 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Список первых пяти подписок на события (при их наличии), созданных в группе ресурсов \` MyResourceGroupName \` , которая удовлетворяет запросу $odataFilter. Если доступны дополнительные результаты, $result. NextLink не будет $null. Чтобы получить следующие страницы подписок на события, предполагается, что пользователь повторно вызывает Get-AzEventGridSubscription и использует результат. NextLink, полученный в результате предыдущего звонка. Вызывающий объект должен остановиться по результатам. NextLink становится $nullом.

### Пример 9
```powershell
PS C:\> Get-AzEventGridSubscription
```

Получает список всех глобальных подписок на события, созданных в текущей выбранной подписке Azure без разбивки на страницы.

### Пример 10
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Список первых 15 глобальных подписок на события (если таковые имеются), созданных в текущей выбранной подписке Azure, соответствующей $odataFilter запросу. Если доступны дополнительные результаты, $result. NextLink не будет $null. Чтобы получить следующие страницы подписок на события, предполагается, что пользователь повторно вызывает Get-AzEventGridSubscription и использует результат. NextLink, полученный в результате предыдущего звонка. Вызывающий объект должен остановиться по результатам. NextLink становится $nullом.

### Пример 11
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

Получает список всех региональных подписок на мероприятия, созданных в группе ресурсов \` MyResourceGroupName \` в указанном расположении \` westus2 \` без разбивки на страницы.

### Пример 12
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2 -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Перечислите первые 15 региональных подписок на события (если таковые имеются), созданные в группе ресурсов \` MyResourceGroupName \` в указанном местоположении \` westus2 \` , которые удовлетворяют $odataFilter запросу. Если доступны дополнительные результаты, $result. NextLink не будет $null. Чтобы получить следующие страницы подписок на события, предполагается, что пользователь повторно вызывает Get-AzEventGridSubscription и использует результат. NextLink, полученный в результате предыдущего звонка. Вызывающий объект должен остановиться по результатам. NextLink становится $nullом.

### Пример 13
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

Получает список всех подписок на события, созданных для указанного пространства имен EventHub без разбивки на страницы.

### Пример 14
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" -Top 25 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Список первых 25 подписок на события (если таковые имеются), созданных для указанного пространства имен EventHub, удовлетворяющего запросу $odataFilter. Если доступны дополнительные результаты, $result. NextLink не будет $null. Чтобы получить следующие страницы подписок на события, предполагается, что пользователь повторно вызывает Get-AzEventGridSubscription и использует результат. NextLink, полученный в результате предыдущего звонка. Вызывающий объект должен остановиться по результатам. NextLink становится $nullом.

### Пример 15
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

Получает список всех подписок на события, созданных для указанного типа темы (пространства имен EventHub) в указанном месте без разбивки на страницы.

### Пример 16
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Список первых 15 подписок на события (если таковые имеются), созданных для указанного типа темы (пространства имен EventHub) в указанном расположении, удовлетворяющем запросу $odataFilter. Если доступны дополнительные результаты, $result. NextLink не будет $null. Чтобы получить следующие страницы подписок на события, предполагается, что пользователь повторно вызывает Get-AzEventGridSubscription и использует результат. NextLink, полученный в результате предыдущего звонка. Вызывающий объект должен остановиться по результатам. NextLink становится $nullом.

### Пример 17
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

Возвращает список всех подписок на события, созданных для определенной группы ресурсов без разбивки на страницы.

### Пример 18
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName -Top 100 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Список первых 100 подписок на события (если таковые имеются), созданных для конкретной группы ресурсов, которая удовлетворяет запросу $odataFilter. Если доступны дополнительные результаты, $result. NextLink не будет $null. Чтобы получить следующие страницы подписок на события, предполагается, что пользователь повторно вызывает Get-AzEventGridSubscription и использует результат. NextLink, полученный в результате предыдущего звонка. Вызывающий объект должен остановиться по результатам. NextLink становится $nullом.

## ПАРАМЕТРЫ

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
Объект Domain EventGrid.

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

### -ИмяДомена
EventGrid Domain Name (доменное имя).

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
Объект темы домена EventGrid.

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

### -EventSubscriptionName
Имя подписки на события

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IncludeFullEndpointUrl
Включите полный URL-адрес конечной точки для назначения подписки на событие.

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
Объект темы EventGrid.

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
Поиска

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NextLink
Ссылка на следующую страницу ресурсов, которые необходимо получить. Это значение получается с помощью первого вызова командлета Get-AzEventGrid, когда больше ресурсов по-прежнему доступны для запроса.

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
Запрос OData, используемый для фильтрации результатов списка. В настоящее время фильтрация разрешена только для свойства Name. Поддерживаются следующие операции: CONTAINS, EQ (для равенства), NE (неравенство), и, или, или нет.

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
Position: 0
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
Запрос OData, используемый для фильтрации результатов списка. В настоящее время фильтрация разрешена только для свойства Name. Поддерживаются следующие операции: CONTAINS, EQ (для равенства), NE (неравенство), и, или, или нет.

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
Название раздела EventGrid.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet
Aliases:

Required: False
Position: 2
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
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String

### Microsoft. Azure. Commands. EventGrid. Models. PSTopic

### Microsoft.Azure.Commands.EventGrid.Models.PSDomain

### Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic

### System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
