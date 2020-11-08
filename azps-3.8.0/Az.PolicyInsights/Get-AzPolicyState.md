---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
ms.openlocfilehash: 04600529ded8b95da578d59f0b2f46cd396594ba
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072979"
---
# Get-AzPolicyState

## КРАТКИй обзор
Возвращает состояние соответствия политике для ресурсов.

## Максимальное

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

## NОПИСАНИЕ
Возвращает состояние соответствия политике для ресурсов. Записи состояния политики можно запрашивать в различных областях. На основе указанного интервала времени (по умолчанию — последний день) можно запрашивать либо последние состояния политики, либо все переходы состояния политики. Результаты могут быть вычислены с фильтрацией, группировкой и группировкой.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение последних состояний политики в текущей области подписки
```powershell
PS C:\> Get-AzPolicyState
```

Возвращает последние записи состояния политики, созданные за последний день для всех ресурсов в рамках подписки в текущем контексте сеанса.

### Пример 2: получение последних состояний политики в указанной области подписки
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

Возвращает последние записи состояния политики, созданные за последний день для всех ресурсов в указанной подписке.

### Пример 3: получение всех состояний политики в текущей области подписки
```powershell
PS C:\> Get-AzPolicyState -All
```

Возвращает все записи состояния политики (включая последние), созданные за последний день для всех ресурсов в рамках подписки в текущем контексте сеанса.

### Пример 4: получение последних состояний политики в области группы управления
```powershell
PS C:\> Get-AzPolicyState -ManagementGroupName "myManagementGroup"
```

Возвращает последние записи состояния политики, созданные за последний день для всех ресурсов в указанной группе управления.

### Пример 5: получение последних состояний политики в области "область группы ресурсов" в текущей подписке
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup"
```

Возвращает последние записи состояния политики, созданные за последний день для всех ресурсов в указанной группе ресурсов (в контексте текущего сеанса).

### Пример 6: получение последних состояний политики в области "Группа ресурсов" в указанной подписке
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

Возвращает последние записи состояния политики, созданные за последний день для всех ресурсов в указанной группе ресурсов (в указанной подписке).

### Пример 7: получение последних состояний политики для ресурса
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

Возвращает последние записи состояния политики, созданные за последний день для указанного ресурса.

### Пример 8: получение последних состояний политики для определения политики в текущей подписке
```powershell
PS C:\> Get-AzPolicyState -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Возвращает последние записи состояния политики, созданные в последнем дне для всех ресурсов (в рамках текущего контекста сеанса), которые были применены указанным определением политики (которое существует в текущем контексте сеанса).

### Пример 9: получение последних состояний политики для определения политики в указанной подписке
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Возвращает последние записи состояния политики, созданные за последний день для всех ресурсов (в рамках текущего контекста сеанса), которые были применены указанным определением политики (которое существует в указанной подписке).

### Пример 10: получение последних состояний политики для определения политики в текущей подписке
```powershell
PS C:\> Get-AzPolicyState -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Возвращает последние записи состояния политики, созданные в последнем дне для всех ресурсов (в рамках текущего контекста сеанса), которые были применены указанным определением политики (которое существует в текущем контексте сеанса).

### Пример 11: получение последних состояний политики для определения политики в указанной подписке
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Возвращает последние записи состояния политики, созданные в последнем дне для всех ресурсов (в рамках текущего контекста сеанса), которые были применены указанным определением политики (которое существует в указанной подписке).

### Пример 12: получение последних состояний политики для назначения политики в текущей подписке
```powershell
PS C:\> Get-AzPolicyState -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Возвращает последние записи состояния политики, созданные в последнем дне для всех ресурсов (в рамках текущего контекста сеанса), на которые влияет указанное назначение политики (оно существует в текущем контексте сеанса).

### Пример 13: получение последних состояний политики для назначения политики в указанной подписке
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Возвращает последние записи состояния политики, созданные за последний день для всех ресурсов (в рамках текущего контекста сеанса), на которые влияет указанное назначение политики (которое существует в указанной подписке).

### Пример 14: получение последних состояний политики для назначения политики в указанной группе ресурсов в текущей подписке
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Возвращает последние записи состояния политики, созданные в последнем дне для всех ресурсов (в рамках текущего контекста сеанса), на которые влияет указанное назначение политики (которое существует в группе ресурсов в текущем контексте сеанса).

### Пример 15: получение последних состояний политики в текущей области подписки с параметрами OrderBy, Top и SELECT запроса
```powershell
PS C:\> Get-AzPolicyState -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId, IsCompliant"
```

Возвращает последние записи состояния политики, созданные за последний день для всех ресурсов в рамках подписки в текущем контексте сеанса. Команда упорядочивает результаты по свойствам timestamp и Name назначения политики и занимает только первые 5 из указанных в этом порядке.
Он также выберет для списка только подмножество столбцов для каждой записи.

### Пример 16: получение последних состояний политики в текущей области подписки с параметрами "из" и "по запросу"
```powershell
PS C:\> Get-AzPolicyState -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

Возвращает последние записи состояния политики, созданные в диапазоне дат, указанном для всех ресурсов в рамках подписки в текущем контексте сеанса.

### Пример 17: получение последних состояний политики в текущей области подписки с помощью параметра "Фильтрация запроса"
```powershell
PS C:\> Get-AzPolicyState -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ComplianceState eq 'NonCompliant' and ResourceLocation ne 'eastus'"
```

Возвращает последние записи состояния политики, созданные за последний день для всех ресурсов в рамках подписки в текущем контексте сеанса.
Команда ограничивает результаты, возвращаемые фильтром, на основе действия, связанного с определением политики (в том числе действия запрета или аудита), состояния соответствия (включает только состояние "не соответствует требованиям") и расположения ресурса (исключает расположение eastus).

### Пример 18: получение последних состояний политики в текущей области подписок с применением функции определения агрегата количества строк
```powershell
PS C:\> Get-AzPolicyState -Apply "aggregate(`$count as NumberOfRecords)"
```

Получает количество последних записей состояния политики, созданных за последний день для всех ресурсов в рамках подписки в текущем контексте сеанса.
Команда возвращает количество записей состояния политики, которое возвращается в рамках свойства AdditionalProperties.

### Пример 19: получение последних состояний политики в текущей области подписки с применением задания группировки с агрегированием
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumStates))" -OrderBy "NumStates desc" -Top 5
```

Возвращает последние записи состояния политики, созданные за последний день для всех ресурсов в рамках подписки в текущем контексте сеанса. Команда ограничивает результаты, возвращаемые фильтром, на основе состояния соответствия требованиям (включает только состояние "не соответствует требованиям").
Результаты группируются на основе назначения политики, определения политики и определения политики, а также вычисляется количество записей в каждой группе, которое возвращается в рамках свойства AdditionalProperties.
Результаты статистического выражения упорядочиваются по убыванию и выполняются только первые 5 из указанных в этом порядке.

### Пример 20: получение последних состояний политики в текущей области подписки с применением задания группирования без агрегата
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((ResourceId))"
```

Возвращает последние записи состояния политики, созданные за последний день для всех ресурсов в рамках подписки в текущем контексте сеанса. Команда ограничивает результаты, возвращаемые фильтром, на основе состояния соответствия требованиям (включает только состояние "не соответствует требованиям").
Результаты группируются на основе идентификатора ресурса. Это приведет к формированию списка всех ресурсов в подписке, которые не соответствуют требованиям хотя бы одной политики.

### Пример 21: получение последних состояний политики в текущей области подписки с применением задания нескольких групп
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumNonCompliantResources))" -OrderBy "NumNonCompliantResources desc" -Top 5
```

### Пример 22: получение последних состояний политики, включая сведения об оценке политики для ресурса
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1" -Expand "PolicyEvaluationDetails"
```

Возвращает последние записи состояния политики, созданные за последний день для всех ресурсов в рамках подписки в текущем контексте сеанса. Команда ограничивает результаты, возвращаемые фильтром, на основе состояния соответствия требованиям (включает только состояние "не соответствует требованиям").
Результаты сначала группируются в соответствии с назначением политики, определением политики, определением политики и идентификатором ресурса. Затем он дополнительно группирует результаты этого группирования с теми же свойствами, но за исключением идентификатора ресурса, и вычисляет количество записей в каждой из этих групп, которое возвращается в рамках свойства AdditionalProperties.
Результаты статистического выражения упорядочиваются по убыванию и выполняются только первые 5 из указанных в этом порядке.
Это приведет к формированию 5 основных политик с наибольшим количеством несоответствующих ресурсов.

## ПАРАМЕТРЫ

### -ALL
Выводит все состояния политики в течение заданного интервала времени, а не только самую последнюю.

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

### -Apply (Применить)
Применение выражения для агрегатов с использованием нотации OData.

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

### -Expand
Развертывание выражения с использованием нотации OData.

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

### -Фильтр
Выражение фильтра с использованием нотации OData.

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
Отформатированная отметка времени ISO 8601 с указанием времени начала интервала для запроса.
Если не указано, по умолчанию используется значение параметра "до" за вычетом 1 дня.

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
Выражение упорядочивания с использованием нотации OData.
Одно или несколько имен столбцов с разделителями-запятыми с дополнительным аргументом "DESC" (значение по умолчанию) или "ASC".

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
Имя определения политики.

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
Идентификатор ресурса.

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

### -SELECT
Выберите выражение с помощью нотации OData.
Одно или несколько имен столбцов с разделителями-запятыми.
Ограничивает столбцы каждой записи только запрошенными.

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
Идентификатор подписки.

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
Отформатированная отметка времени ISO 8601, указывающая время окончания интервала для запроса.
Если не указано, по умолчанию используется время запроса.

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## ВХОДНЫЕ данные

### System. String

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. PolicyInsights. Models. PolicyState

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzPolicyStateSummary](./Get-AzPolicyStateSummary.md)
