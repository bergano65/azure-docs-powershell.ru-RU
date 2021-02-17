---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicyevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
ms.openlocfilehash: 744618bb2cc12b4d57bfb1ed42267fcbbe7a86ab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100227252"
---
# Get-AzPolicyEvent

## SYNOPSIS
Возвращает события оценки политики, созданные по мере создания или обновления ресурсов.

## СИНТАКСИС

### SubscriptionScope (по умолчанию)
```
Get-AzPolicyEvent [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ManagementGroupScope
```
Get-AzPolicyEvent -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupScope
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PolicySetDefinitionScope
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PolicyDefinitionScope
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SubscriptionLevelPolicyAssignmentScope
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupLevelPolicyAssignmentScope
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceScope
```
Get-AzPolicyEvent -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>]
 [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## ОПИСАНИЕ
Возвращает события оценки политики, созданные по мере создания или обновления ресурсов. Записи событий политики можно запрашивать в различных областях на основе заданного интервала времени (по умолчанию — последний день). Результаты можно вычислять с фильтрацией, группировкой и групповыми агрегатами.

## ПРИМЕРЫ

### Пример 1. Просмотр событий политики в текущей области действия подписки
```powershell
PS C:\> Get-AzPolicyEvent
```

Возвращает записи событий политики, созданные в последний день для всех ресурсов в рамках подписки в контексте текущего сеанса.

### Пример 2. Просмотр событий политики в указанной области подписки
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

Возвращает записи событий политики, созданные в последний день для всех ресурсов в указанной подписке.

### Пример 3. Просмотр событий политики в области группы управления
```powershell
PS C:\> Get-AzPolicyEvent -ManagementGroupName "myManagementGroup"
```

Возвращает записи событий политики, созданные в последний день для всех ресурсов в указанной группе управления.

### Пример 4. Получать события политики в области группы ресурсов в текущей подписке
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup"
```

Возвращает записи событий политики, созданные в последний день для всех ресурсов в указанной группе ресурсов (в подписке в контексте текущего сеанса).

### Пример 5. Получать события политики в области группы ресурсов в указанной подписке
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

Возвращает записи событий политики, созданные в последний день для всех ресурсов в указанной группе ресурсов (в указанной подписке).

### Пример 6. Получить события политики для ресурса
```powershell
PS C:\> Get-AzPolicyEvent -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

Возвращает записи событий политики, созданные в последний день для указанного ресурса.

### Пример 7. Получить события политики для определения набора политик в текущей подписке
```powershell
PS C:\> Get-AzPolicyEvent -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Получает записи событий политики, созданные в последний день для всех ресурсов (в пределах клиента в контексте текущего сеанса), на которые влияет указанное определение набора политики (которое существует в подписке в контексте текущего сеанса).

### Пример 8. Получить события политики для определения набора политики в указанной подписке
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Возвращает записи событий политики, созданные в последний день для всех ресурсов (в пределах клиента в контексте текущего сеанса), на которые влияет указанное определение набора политики (которое существует в указанной подписке).

### Пример 9. Получить события политики для определения политики в текущей подписке
```powershell
PS C:\> Get-AzPolicyEvent -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Получает записи событий политики, созданные в последний день для всех ресурсов (в пределах клиента в контексте текущего сеанса), на которые влияет указанное определение политики (которое существует в подписке в контексте текущего сеанса).

### Пример 10. Получить события политики для определения политики в указанной подписке
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Возвращает записи событий политики, созданные в последний день для всех ресурсов (в пределах клиента в контексте текущего сеанса), на которые влияет указанное определение политики (которое существует в указанной подписке).

### Пример 11. Просмотр событий политики для назначения политики в текущей подписке
```powershell
PS C:\> Get-AzPolicyEvent -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Возвращает записи событий политики, созданные в последний день для всех ресурсов (в пределах клиента в контексте текущего сеанса), к работе с помощью указанного назначения политики (которое существует в подписке в контексте текущего сеанса).

### Пример 12. Получить события политики для назначения политики в указанной подписке
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Возвращает записи событий политики, созданные в последний день для всех ресурсов (в пределах клиента в контексте текущего сеанса), на которые влияет указанное назначение политики (существующее в указанной подписке).

### Пример 13. Получить события политики для назначения политики в указанной группе ресурсов в текущей подписке
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Возвращает записи событий политики, созданные в последний день для всех ресурсов (в клиенте в текущем контексте сеанса), к данным заданного назначения политики (которые существуют в группе ресурсов в подписке в контексте текущего сеанса).

### Пример 14. Просмотр событий политики в текущей области подписки с вариантами запроса OrderBy, Top и Select
```powershell
PS C:\> Get-AzPolicyEvent -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId"
```

Возвращает записи событий политики, созданные в последний день для всех ресурсов в рамках подписки в контексте текущего сеанса. Эта команда отбирает результаты по свойствам имени timestamp и policy assignment и принимает только 5 из 5 перечислены в этом порядке.
Кроме того, для каждой записи будет выбрано только подмножество столбцов.

### Пример 15. Просмотр событий политики в текущей области подписки с вариантами запросов "От" и "На"
```powershell
PS C:\> Get-AzPolicyEvent -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

Возвращает записи событий политики, созданные в диапазоне дат, указанном для всех ресурсов подписки в текущем контексте сеанса.

### Пример 16. Просмотр событий политики в текущей области подписки с параметром "Фильтровать запрос"
```powershell
PS C:\> Get-AzPolicyEvent -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

Возвращает записи событий политики, созданные в последний день для всех ресурсов в рамках подписки в контексте текущего сеанса.
Команда ограничивает результаты, возвращаемые с помощью фильтрации на основе действия определения политики (включая действия запрета или аудита) и расположения ресурсов (за исключением расположения на востоке).

### Пример 17. Получение событий политики в текущей области подписки с указанием агрегата "Применить" для подсчета строк
```powershell
PS C:\> Get-AzPolicyEvent -Apply "aggregate(`$count as NumberOfRecords)"
```

Возвращает количество записей событий политики, созданных в последний день для всех ресурсов подписки в текущем контексте сеанса.
Команда возвращает количество только записей событий политики, которое возвращается в свойстве AdditionalProperties.

### Пример 18. Получение событий политики в текущей области подписки с указанием группировки с агрегатом "Применить"
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, PolicyDefinitionAction, ResourceId), aggregate(`$count as NumEvents))" -OrderBy "NumEvents desc" -Top 5
```

Возвращает записи событий политики, созданные в последний день для всех ресурсов в рамках подписки в контексте текущего сеанса. Команда ограничивает результаты, возвращаемые с помощью фильтрации на основе действия определения политики (включая только события аудита и запрета).
Она группирует результаты на основе назначения политики, определения политики, действия определения политики и ид ресурса, а также вычисляет количество записей в каждой группе, возвращаемой в свойстве AdditionalProperties.
Она упорядочена по результатам подсчета в порядке убывления и занимает только 5 лучших из перечислены в этом порядке.

### Пример 19. Получение событий политики в текущей области подписки с указанием группировки без агрегирования
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((ResourceId))"
```

Возвращает записи событий политики, созданные в последний день для всех ресурсов в рамках подписки в контексте текущего сеанса. Команда ограничивает результаты, возвращаемые с помощью фильтрации на основе действия определения политики (включая только события аудита и запрета).
Результаты группируются на основе ид ресурса. Будет создан список всех ресурсов в подписке, которые создали событие политики как минимум для одной политики аудита или запрета.

### Пример 20. Получение событий политики в текущей области действия подписки с указанием нескольких групп
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicyDefinitionId), aggregate(`$count as NumDeniedResources))" -OrderBy "NumDeniedResources desc" -Top 5
```

Возвращает записи событий политики, созданные в последний день для всех ресурсов в рамках подписки в контексте текущего сеанса. Команда ограничивает результаты, возвращаемые с помощью фильтрации на основе действия определения политики (включая только события запрета).
Сначала результаты группируются на основе назначения политики, определения политики и ид ресурса. Затем она затем группирует результаты этой группировки с такими же свойствами, за исключением ид ресурса, и вычисляет количество записей в каждой из этих групп, возвращаемого в свойстве AdditionalProperties.
Она упорядочена по результатам подсчета в порядке убывления и занимает только 5 лучших из перечислены в этом порядке.
При этом создаются 5 самых распространенных политик запрета с большим количеством отказано в ресурсах.

## PARAMETERS

### -Apply
Применение выражения для агрегатов с помощью нотации OData.

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

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

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

### -Filter
Фильтрация выражения с использованием нотации OData.

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

### -From
Timestamp в формате ISO 8601, определяющий время начала интервала для запроса.
Если этот параметр не задан, по умолчанию значение параметра "To" за вычетом 1 дня.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagementGroupName
Имя группы управления.

```yaml
Type: System.String
Parameter Sets: ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OrderBy
Выражение порядка с использованием нотации OData.
Одно или несколько имен столбцов, разделенных запятой, с необязательными именами "desc" (по умолчанию) или "asc".

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

### -PolicyAssignmentName
Имя назначения политики.

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelPolicyAssignmentScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicyDefinitionName
Имя определения политики.

```yaml
Type: System.String
Parameter Sets: PolicyDefinitionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicySetDefinitionName
Имя определения набора политик.

```yaml
Type: System.String
Parameter Sets: PolicySetDefinitionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов.

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
ИД ресурса.

```yaml
Type: System.String
Parameter Sets: ResourceScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Select
Выберите выражение, используя нотацию OData.
Одно или несколько имен столбцов, разделенных запятой.
Ограничивает столбцы в каждой записи только теми, которые запрашиваются.

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

### -SubscriptionId
ИД подписки.

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, ResourceGroupScope, PolicySetDefinitionScope, PolicyDefinitionScope, SubscriptionLevelPolicyAssignmentScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -To
Timestamp в формате ISO 8601, определяющий время окончания интервала для запроса.
По умолчанию заданы значения времени запроса.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Top
Максимальное количество возвращаемых записей.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

## OUTPUTS

### Microsoft.Azure.Commands.PolicyInsights.Models.PolicyEvent

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ
