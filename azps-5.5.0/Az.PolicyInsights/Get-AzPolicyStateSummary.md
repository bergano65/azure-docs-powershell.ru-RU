---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicystatesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
ms.openlocfilehash: ad622662615e74908c3d34c513e8570286b76297
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240333"
---
# Get-AzPolicyStateSummary

## SYNOPSIS
Возвращает сводку по последним состояниям соответствия политике для ресурсов.

## СИНТАКСИС

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

## ОПИСАНИЕ
Представление сводки номеров последних политик соответствия требованиям в различных областях, разбитое на назначения политик и определения политик. Он включает только состояния, не совместимые с политикой.

## ПРИМЕРЫ

### Пример 1. Просмотр последних отчетов о состояниях, не совместимых с политиками, в текущей области действия подписки
```powershell
PS C:\> Get-AzPolicyStateSummary
```

Возвращает сводку по последним состояниям соответствия политике, созданную в последний день для всех ресурсов подписки в текущем контексте сеанса.

### Пример 2. Вывод последних отчетов о состояниях, не совместимых с политиками, в указанной области подписки
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

Возвращает сводку по последним состояниям соответствия политике, созданную в последний день для всех ресурсов в указанной подписке.

### Пример 3. Получать последние сведения о состояниях политики, не соответствующим требованиям, в области группы управления
```powershell
PS C:\> Get-AzPolicyStateSummary -ManagementGroupName "myManagementGroup"
```

Возвращает сводку по последним состояниям соответствия политике, созданную в последний день для всех ресурсов в указанной группе управления.

### Пример 4. Получать последние сведения о состояниях политики, не соответствующим требованиям, в области группы ресурсов в текущей подписке
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup"
```

Возвращает сводку по последним состояниям соответствия политике, созданную в последний день для всех ресурсов в указанной группе ресурсов (в подписке в контексте текущего сеанса).

### Пример 5. Получать последние сведения о состояниях политики, не соответствующим требованиям, в области группы ресурсов в указанной подписке
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

Возвращает сводку по последним состояниям соответствия политике, созданную в последний день для всех ресурсов в указанной группе ресурсов (в указанной подписке).

### Пример 6. Просмотр последних отчетов о состояниях, не совместимых с политиками, для ресурса
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

Возвращает сводку по последним состояниям соответствия политике, созданную в последний день для указанного ресурса.

### Пример 7. Просмотр последних отчетов о состояниях, не совместимых с политиками, для определения набора политик в текущей подписке
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Возвращает сводку по последним состояниям соответствия политике, созданным в последний день для всех ресурсов (в клиенте в текущем контексте сеанса), на которые влияет указанное определение набора политики (которое существует в подписке в контексте текущего сеанса).

### Пример 8. Просмотр последних отчетов о состояниях, не совместимых с политиками, для определения набора политик в указанной подписке
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Возвращает сводку по последним состояниям соответствия политике, созданным в последний день для всех ресурсов (в пределах клиента в текущем сеансе), на которые влияет указанное определение набора политики (которое существует в указанной подписке).

### Пример 9. Просмотр последних отчетов о состояниях, не совместимых с политиками, для определения политики в текущей подписке
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Возвращает сводку по последним состояниям соответствия политике, созданным в последний день для всех ресурсов (в клиенте в контексте текущего сеанса), на которые влияет указанное определение политики (которое существует в подписке в контексте текущего сеанса).

### Пример 10. Просмотр последних отчетов о состояниях, не совместимых с политиками, для определения политики в указанной подписке
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Возвращает сводку по последним состояниям соответствия политике, созданным в последний день для всех ресурсов (в клиенте в контексте текущего сеанса), на которые влияет указанное определение политики (которое существует в указанной подписке).

### Пример 11. Просмотр последних отчетов о состояниях, не совместимых с политиками, для назначения политики в текущей подписке
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Возвращает сводку по последним состояниям соответствия политике, созданным в последний день для всех ресурсов (в клиенте в текущем контексте сеанса), на которые влияет указанное назначение политики (которое существует в подписке в контексте текущего сеанса).

### Пример 12. Просмотр последних отчетов о состояниях, не совместимых с политиками, для назначения политики в указанной подписке
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Возвращает сводку по последним состояниям соответствия политике, созданным в последний день для всех ресурсов (в пределах клиента в контексте текущего сеанса), на которые влияет указанное назначение политики (которое существует в указанной подписке).

### Пример 13. Просмотр последних отчетов о состояниях, не совместимых с политиками, для назначения политики в указанной группе ресурсов в текущей подписке
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Возвращает сводку по последним состояниям соответствия политике, созданным в последний день для всех ресурсов (в клиенте в контексте текущего сеанса), на которые влияет указанное назначение политики (которое существует в группе ресурсов в подписке в контексте текущего сеанса).

### Пример 14. Просмотр последних отчетов о состояниях, не совместимых с политиками, в текущей области действия подписки с параметром "Верхний запрос"
```powershell
PS C:\> Get-AzPolicyStateSummary -Top 5
```

Возвращает сводку по последним состояниям соответствия политике, созданную в последний день для всех ресурсов подписки в текущем контексте сеанса. Команда заказывает сводки назначений политики в результатах в порядке убываний не соответствующими требованиям ресурсами и выводит только 5 из них.

### Пример 15. Получите последние сведения о состояниях политики, не соответствующим требованиям, в текущей области действия подписки с помощью параметров запроса "От" и "На"
```powershell
PS C:\> Get-AzPolicyStateSummary -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

Возвращает сводку по последним состояниям соответствия политике, созданную в диапазоне дат, указанном для всех ресурсов подписки в текущем контексте сеанса.

### Пример 16. Просмотр последних отчетов о состояниях политики, не соответствующим требованиям, в текущей области действия подписки с параметром "Фильтровать запрос"
```powershell
PS C:\> Get-AzPolicyStateSummary -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

Возвращает сводку по последним состояниям соответствия политике, созданную в последний день для всех ресурсов подписки в текущем контексте сеанса.
Команда ограничивает результаты, возвращаемые с помощью фильтрации на основе действия определения политики (включая действия запрета или аудита) и расположения ресурсов (за исключением расположения на востоке).

## PARAMETERS

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

### Microsoft.Azure.Commands.PolicyInsights.Models.PolicyStateSummary

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzPolicyState](./Get-AzPolicyState.md)
