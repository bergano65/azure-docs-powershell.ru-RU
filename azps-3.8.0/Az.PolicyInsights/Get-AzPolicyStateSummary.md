---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicystatesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
ms.openlocfilehash: ad622662615e74908c3d34c513e8570286b76297
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072974"
---
# Get-AzPolicyStateSummary

## КРАТКИй обзор
Получает актуальные сведения о состояниях соответствия политике для ресурсов.

## Максимальное

### SubscriptionScope (по умолчанию)
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ManagementGroupScope
```
Get-AzPolicyStateSummary -ManagementGroupName <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupScope
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### PolicySetDefinitionScope
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### PolicyDefinitionScope
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### SubscriptionLevelPolicyAssignmentScope
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceGroupLevelPolicyAssignmentScope
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceScope
```
Get-AzPolicyStateSummary -ResourceId <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Возвращает представление сводки о последних параметрах соответствия политике в различных областях, с разбивкой на назначения политики и определения политик. Она содержит только несоответствующие состояния политики.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение последних несоответствующих состояний политики сводка в текущей области подписки
```powershell
PS C:\> Get-AzPolicyStateSummary
```

Возвращает представление сводки о последних состояниях соответствия политике, созданных за последний день для всех ресурсов в рамках подписки в текущем контексте сеанса.

### Пример 2: получение актуальной сводки о состояниях политик, не соответствующих требованиям, в указанной области действия подписки
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

Возвращает представление сводки о последних состояниях соответствия политике, созданных за последний день для всех ресурсов в указанной подписке.

### Пример 3: получение последних несовместимых состояний политики в области группы управления
```powershell
PS C:\> Get-AzPolicyStateSummary -ManagementGroupName "myManagementGroup"
```

Возвращает представление сводки о последних состояниях соответствия политике, созданных за последний день для всех ресурсов в указанной группе управления.

### Пример 4: получение последних несовместимых состояний политики в области "область группы ресурсов" в текущей подписке
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup"
```

Возвращает представление сводки о последних состояниях соответствия политике, созданных за последний день для всех ресурсов в указанной группе ресурсов (в контексте текущего сеанса).

### Пример 5: получение последних несоответствующих состояний политики в области "область группы ресурсов" в указанной подписке
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

Возвращает представление сводки о последних состояниях соответствия политике, созданных за последний день для всех ресурсов в указанной группе ресурсов (в указанной подписке).

### Пример 6: получение последних несовместимых состояний политики для ресурса
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

Возвращает представление сводки о последних состояниях соответствия политике, созданных за последний день для указанного ресурса.

### Пример 7: получение последних несовместимых состояний политики для определения политики в текущей подписке
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Возвращает представление сводки о последних политиках соответствия политике, созданных за последний день для всех ресурсов (в рамках текущего контекста сеанса), которые были применены указанным определением набора политик (которое существует в подписке в текущем контексте сеанса).

### Пример 8: получение последних несовместимых состояний политики для определения политики в указанной подписке
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Возвращает представление сводки о последних политиках соответствия политике, созданных за последний день для всех ресурсов (в рамках текущего контекста сеанса), которые были применены указанным определением набора политик (которое существует в указанной подписке).

### Пример 9: получение последних несовместимых состояний политики для определения политики в текущей подписке
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Возвращает представление сводки о последних политиках соответствия политике, созданных за последний день для всех ресурсов (в рамках текущего контекста сеанса), которые были применены указанным определением политики (которое существует в текущем контексте сеанса).

### Пример 10: получение последних несовместимых состояний политики для определения политики в указанной подписке
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Возвращает представление сводки о последних политиках соответствия политике, созданных за последний день для всех ресурсов (в рамках текущего контекста сеанса), которые были применены указанным определением политики (которое существует в указанной подписке).

### Пример 11: получение последних несовместимых состояний политики для назначения политики в текущей подписке
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Возвращает представление сводки о последних политиках соответствия политике, созданных за последний день для всех ресурсов (в рамках текущего контекста сеанса), на которые влияет указанное назначение политики (оно существует в текущем контексте сеанса).

### Пример 12: получение последних несовместимых состояний политики для назначения политики в указанной подписке
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Возвращает представление сводки о последних состояниях соответствия политике, созданных за последний день для всех ресурсов (в рамках текущего контекста сеанса), на которые влияет указанное назначение политики (которое существует в указанной подписке).

### Пример 13: получение последних несовместимых состояний политики для назначения политики в указанной группе ресурсов в текущей подписке
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Возвращает представление сводки о последних состояниях соответствия политике, созданных за последний день для всех ресурсов (в рамках текущего контекста сеанса), на которые влияет указанное назначение политики (которое существует в группе ресурсов в контексте текущего сеанса).

### Пример 14: получение последних несоответствующих состояний политики в текущей области подписки с параметром Top Query
```powershell
PS C:\> Get-AzPolicyStateSummary -Top 5
```

Возвращает представление сводки о последних состояниях соответствия политике, созданных за последний день для всех ресурсов в рамках подписки в текущем контексте сеанса. Команда упорядочивает данные о назначениях политики в результатах по убывающему представлению несоответствующих ресурсов в порядке убывания и использует только первые 5 из этих сводок назначений политики.

### Пример 15: получение последних несоответствующих состояний политики в текущей области подписки с параметрами "из" и "по запросу"
```powershell
PS C:\> Get-AzPolicyStateSummary -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

Возвращает представление сводки о последних состояниях соответствия политике, созданных в диапазоне дат, указанном для всех ресурсов в контексте текущего сеанса.

### Пример 16: получение последних несоответствующих состояний политики в текущей области подписки с помощью параметра "запрос фильтра"
```powershell
PS C:\> Get-AzPolicyStateSummary -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

Возвращает представление сводки о последних состояниях соответствия политике, созданных за последний день для всех ресурсов в рамках подписки в текущем контексте сеанса.
Команда ограничивает результаты, возвращаемые фильтром, на основе действия с определением политики (в том числе действия запрета или аудита) и расположения ресурсов (исключение расположения eastus).

## ПАРАМЕТРЫ

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

### Microsoft. Azure. Commands. PolicyInsights. Models. PolicyStateSummary

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzPolicyState](./Get-AzPolicyState.md)
