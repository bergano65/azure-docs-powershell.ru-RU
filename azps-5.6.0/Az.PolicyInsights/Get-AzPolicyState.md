---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/get-azpolicystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
ms.openlocfilehash: 82aa08a3d4b4eb42638e1b9def55b5d936f176b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989092"
---
# Get-AzPolicyState

## SYNOPSIS
Возвращает состояния соответствия политике для ресурсов.

## СИНТАКСИС

### SubscriptionScope (по умолчанию)
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ManagementGroupScope
```
Get-AzPolicyState [-All] -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupScope
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceScope
```
Get-AzPolicyState [-All] -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-Expand <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PolicySetDefinitionScope
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PolicyDefinitionScope
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SubscriptionLevelPolicyAssignmentScope
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupLevelPolicyAssignmentScope
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
Возвращает состояния соответствия политике для ресурсов. Записи состояния политики можно запрашивать в различных областях. В зависимости от заданного интервала времени (по умолчанию — последний день) можно запрашивать последние состояния политики или все переходы между состояниями политики. Результаты можно вычислять с фильтрацией, группировкой и групповыми агрегатами.

## ПРИМЕРЫ

### Пример 1. Последние состояния политики в текущей области действия подписки
```powershell
PS C:\> Get-AzPolicyState
```

Возвращает последние записи состояния политики, созданные в последний день для всех ресурсов в рамках подписки в текущем контексте сеанса.

### Пример 2. Последние состояния политики в указанной области подписки
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

Возвращает последние записи состояния политики, созданные в последний день для всех ресурсов в указанной подписке.

### Пример 3. Просмотр всех областей политики в текущей области действия подписки
```powershell
PS C:\> Get-AzPolicyState -All
```

Возвращает все исторические записи об условиях политики (включая последние), созданные в последний день для всех ресурсов подписки в текущем контексте сеанса.

### Пример 4. Последние состояния политики в области групп управления
```powershell
PS C:\> Get-AzPolicyState -ManagementGroupName "myManagementGroup"
```

Возвращает последние записи состояния политики, созданные в последний день для всех ресурсов в указанной группе управления.

### Пример 5. Последние состояния политики в области группы ресурсов в текущей подписке
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup"
```

Возвращает последние записи состояния политики, созданные в последний день для всех ресурсов в указанной группе ресурсов (в подписке в контексте текущего сеанса).

### Пример 6. Последние состояния политики в области группы ресурсов в указанной подписке
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

Возвращает последние записи состояния политики, созданные в последний день для всех ресурсов в указанной группе ресурсов (в указанной подписке).

### Пример 7. Последние состояния политики для ресурса
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

Возвращает последние записи состояния политики, созданные в последний день для указанного ресурса.

### Пример 8. Определение последних состояния политики для определения набора политик в текущей подписке
```powershell
PS C:\> Get-AzPolicyState -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Возвращает последние записи состояния политики, созданные в последний день для всех ресурсов (в пределах клиента в текущем сеансе), на которые влияет указанное определение набора политики (которое существует в подписке в контексте текущего сеанса).

### Пример 9. Получите последние состояния политики для определения набора политик в указанной подписке
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Возвращает последние записи состояния политики, созданные в последний день для всех ресурсов (в пределах клиента в текущем сеансе), на которые влияет указанное определение набора политики (которое существует в указанной подписке).

### Пример 10. Последние состояния политики для определения политики в текущей подписке
```powershell
PS C:\> Get-AzPolicyState -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Возвращает последние записи состояния политики, созданные в последний день для всех ресурсов (в пределах клиента в текущем сеансе), на которые влияет указанное определение политики (которое существует в подписке в контексте текущего сеанса).

### Пример 11. Просмотр последних состояния политики для определения политики в указанной подписке
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Возвращает последние записи состояния политики, созданные в последний день для всех ресурсов (в пределах клиента в текущем сеансе), на которые влияет указанное определение политики (которое существует в указанной подписке).

### Пример 12. Получать последние состояния политики для назначения политики в текущей подписке
```powershell
PS C:\> Get-AzPolicyState -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Возвращает последние записи состояния политики, созданные в последний день для всех ресурсов (в пределах клиента в текущем сеансе), к работе с помощью указанного назначения политики (которое существует в подписке в контексте текущего сеанса).

### Пример 13. Получать последние состояния политики для назначения политики в указанной подписке
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Возвращает последние записи состояния политики, созданные в последний день для всех ресурсов (в пределах клиента в текущем сеансе), к работе с помощью указанного назначения политики (существующего в указанной подписке).

### Пример 14. Получать последние состояния политики для назначения политики в указанной группе ресурсов в текущей подписке
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Возвращает последние записи состояния политики, созданные в последний день для всех ресурсов (в пределах клиента в текущем сеансе), к данным о назначении политики (которые существуют в группе ресурсов в подписке в контексте текущего сеанса).

### Пример 15. Последние состояния политики в текущей области действия подписки с вариантами запроса OrderBy, Top и Select
```powershell
PS C:\> Get-AzPolicyState -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId, IsCompliant"
```

Возвращает последние записи состояния политики, созданные в последний день для всех ресурсов в рамках подписки в текущем контексте сеанса. Эта команда отбирает результаты по свойствам timestamp и policy assignment (Имя назначения политики) и отбирает только 5 из 5 перечислены в этом порядке.
Кроме того, для каждой записи будет выбрано только подмножество столбцов.

### Пример 16. Последние состояния политики в текущей области действия подписки с помощью параметров запроса "От" и "На"
```powershell
PS C:\> Get-AzPolicyState -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

Возвращает последние записи состояния политики, созданные в диапазоне дат, указанном для всех ресурсов подписки в текущем контексте сеанса.

### Пример 17. Последние состояния политики в текущей области подписки с параметром "Фильтровать запрос"
```powershell
PS C:\> Get-AzPolicyState -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ComplianceState eq 'NonCompliant' and ResourceLocation ne 'eastus'"
```

Возвращает последние записи состояния политики, созданные в последний день для всех ресурсов в рамках подписки в текущем контексте сеанса.
Команда ограничивает результаты, возвращаемые с помощью фильтрации на основе действия определения политики (включая действия запрета или аудита), состояния соответствия (включая только состояние, не соответствует требованиям) и расположения ресурсов (за исключением расположения на востоке).

### Пример 18. Получение последних состояния политики в текущей области подписки с указанием агрегата "Применить" для подсчета строк
```powershell
PS C:\> Get-AzPolicyState -Apply "aggregate(`$count as NumberOfRecords)"
```

Возвращает количество последних записей состояния политики, созданных в последний день для всех ресурсов подписки в текущем контексте сеанса.
Команда возвращает количество только записей состояния политики, которое возвращается в свойстве AdditionalProperties.

### Пример 19. Получение последних состояния политики в текущей области действия подписки с указанием группировки с агрегатом
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumStates))" -OrderBy "NumStates desc" -Top 5
```

Возвращает последние записи состояния политики, созданные в последний день для всех ресурсов в рамках подписки в текущем контексте сеанса. Команда ограничивает результаты, возвращаемые с помощью фильтрации на основе состояния соответствия требованиям (включая только состояние, не соответствует требованиям).
Она группирует результаты на основе назначения политики, определения набора политик и определения политики, а также вычисляет количество записей в каждой группе, которое возвращается в свойстве AdditionalProperties.
Она заказывает результаты по агрегату в порядке убыения и принимает только пять лучших из перечислены в этом порядке.

### Пример 20. Получение последних состояния политики в текущей области подписки с указанием группировки без агрегирования
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((ResourceId))"
```

Возвращает последние записи состояния политики, созданные в последний день для всех ресурсов в рамках подписки в текущем контексте сеанса. Команда ограничивает результаты, возвращаемые с помощью фильтрации на основе состояния соответствия требованиям (включая только состояние, не соответствует требованиям).
Результаты группируются на основе ид ресурса. При этом создается список всех ресурсов в подписке, которые не соответствуют хотя бы одной политике.

### Пример 21. Получение последних областей политики в текущей области действия подписки с указанием нескольких групп
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumNonCompliantResources))" -OrderBy "NumNonCompliantResources desc" -Top 5
```

### Пример 22. Сведения о последних состояниях политики, включая сведения о оценке политики для ресурса
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1" -Expand "PolicyEvaluationDetails"
```

Возвращает последние записи состояния политики, созданные в последний день для всех ресурсов в рамках подписки в текущем контексте сеанса. Команда ограничивает результаты, возвращаемые с помощью фильтрации на основе состояния соответствия требованиям (включая только состояние, не соответствует требованиям).
Сначала результаты группируются на основе назначения политики, определения набора политики, определения политики и ид ресурса. Затем она затем группирует результаты этой группировки с такими же свойствами, за исключением ид ресурса, и вычисляет количество записей в каждой из этих групп, возвращаемого в свойстве AdditionalProperties.
Она упорядочена по результатам подсчета в порядке убывления и занимает только 5 лучших из перечислены в этом порядке.
При этом будут создаваться 5 политик с большим количеством несовместимых ресурсов.

## PARAMETERS

### -Все
В течение заданного интервала получите все состояния политики, а не только последние.

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

### -Развернуть
Расширение выражения с помощью нотации OData.

```yaml
Type: System.String
Parameter Sets: ResourceScope
Aliases:

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

### Microsoft.Azure.Commands.PolicyInsights.Models.PolicyState

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzPolicyStateSummary](./Get-AzPolicyStateSummary.md)
