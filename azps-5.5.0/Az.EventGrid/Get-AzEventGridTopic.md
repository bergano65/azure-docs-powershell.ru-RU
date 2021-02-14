---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
ms.openlocfilehash: df3f6673729a868e7aeb349a34fba32b2033862e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100228497"
---
# Get-AzEventGridTopic

## SYNOPSIS
Возвращает сведения о теме сетки событий или список всех разделов сетки событий в текущей подписке Azure.

## СИНТАКСИС

### ResourceGroupNameParameterSet (по умолчанию)
```
Get-AzEventGridTopic [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### TopicNameParameterSet
```
Get-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdEventSubscriptionParameterSet
```
Get-AzEventGridTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### NextLinkParameterSet
```
Get-AzEventGridTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
Этот Get-AzEventGridTopic возвращает сведения о указанном разделе сетки событий или список всех тем сетки событий в текущей подписке Azure.
Если за предоставлено название темы, возвращаются сведения об отдельной теме сетки событий.
Если название темы не заданной, возвращается список разделов. Количество элементов, возвращаемых в этом списке, управляется параметром Top. Если значение не указано или $null, в списке будут указаны все элементы. В противном случае top будет указывать максимальное количество элементов, которые будут возвращены в списке.
Если по-прежнему доступны другие темы, значение в NextLink нужно использовать в следующем звонке для получения следующей страницы тем.
Наконец, параметр ODataQuery используется для фильтрации результатов поиска. Запрос фильтрации следует за синтаксисом OData, используя только свойство Name. Поддерживаются следующие операции: CONTAINS, eq (для равно), ne (для не равно), AND, OR и NOT.

## ПРИМЕРЫ

### Пример 1
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

Возвращает сведения о теме "Сетка событий" "Тема1" в группе ресурсов \` \` \` MyResourceGroupName. \`

### Пример 2
```powershell
PS C:\> Get-AzEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

Возвращает сведения о теме "Сетка событий" "Тема1" в группе ресурсов \` \` \` MyResourceGroupName. \`

### Пример 3
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName
```

Перечислите все разделы сетки событий в группе ресурсов \` MyResourceGroupName \` без разрежения.

### Пример 4
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

Перечислите первые 10 разделов сетки событий (если таковые есть) в группе ресурсов \` MyResourceGroupName, которая удовлетворяет $odataFilter \` запросу. Если доступно больше результатов, $result. NextLink не будет $null. Чтобы получить следующие страницы тем, пользователь должен переназвать Get-AzEventGridTopic использовать результат. NextLink, полученные в предыдущем звонке. Звонок должен остановиться в результатах. NextLink становится $null.

### Пример 5
```powershell
PS C:\> Get-AzEventGridTopic
```

Со списком всех разделов сетки событий в подписке без разгибов.

### Пример 6
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

Со списком первых 10 разделов сетки событий (если они есть) в подписке, которая удовлетворяет $odataFilter запросу. Если доступно больше результатов, $result. NextLink не будет $null. Чтобы получить следующие страницы тем, пользователь должен переназвать Get-AzEventGridTopic использовать результат. NextLink, полученные в предыдущем звонке. Звонок должен остановиться в результатах. NextLink становится $null.

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

### -Name
Имя темы EventGrid.

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
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
Parameter Sets: ResourceGroupNameParameterSet, TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
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
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Идентификатор ресурса, представляющий раздел сетки событий.

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Top
Максимальное количество ресурсов, которые нужно получить. Допустимым является значение от 1 до 100. Если указано верхнее значение и другие результаты по-прежнему доступны, результат будет содержать ссылку на следующую страницу, которая будет запрашиваться в NextLink. Если значение не указано, возвращается полный список ресурсов.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ResourceGroupNameParameterSet, TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
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

### System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]

## OUTPUTS

### Microsoft.Azure.Commands.EventGrid.Models.PSTopic

### Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ
