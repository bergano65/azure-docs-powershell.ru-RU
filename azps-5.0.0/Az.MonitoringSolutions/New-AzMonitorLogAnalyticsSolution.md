---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/new-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: 6747a53f9e714926c5a4d1358e15cb387ddae69a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249405"
---
# New-AzMonitorLogAnalyticsSolution

## КРАТКИй обзор
Создание решения для службы анализа журналов.

## Максимальное

```
New-AzMonitorLogAnalyticsSolution -ResourceGroupName <String> -Location <String> -Type <String>
 -WorkspaceResourceId <String> [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## NОПИСАНИЕ
Создание решения для службы анализа журналов.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание решения для анализа журнала на мониторе для рабочей области "анализ журналов"
```powershell
PS C:\> $workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName azureps-manual-test -Name monitoringworkspace-2vob7n
PS C:\> New-AzMonitorLogAnalyticsSolution -Type Containers -ResourceGroupName azureps-manual-test -Location $workspace.Location -WorkspaceResourceId $workspace.ResourceId

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

Эта команда создает решение для аналитики журнала мониторинга для рабочей области "анализ журналов".

Чаще всего используются следующие типы:

| Команду | Nописание |
| :-----| :----- |
| SecurityCenterFree |  Центр безопасности Azure — бесплатная версия |
| Разрешения | Центр безопасности Azure |
| Обновлении | Управление обновлениями |
| ContainerInsights | Монитор Azure для контейнеров |
| ServiceMap | Карта обслуживания |
| AzureActivity | Анализ журнала активности |
| ChangeTracking | Отслеживание изменений и Инвентаризация |
| VMInsights | Монитор Azure для ВМ |
| SecurityInsights | Sentinel "Azure" |
| NetworkMonitoring | Монитор производительности сети |
| SQLVulnerabilityAssessment | Оценка уязвимости SQL |
| SQLAdvancedThreatProtection | Расширенная защита от угроз SQL |
| Антивредоносные программы | Оценка защиты от вредоносных программ |
| AzureAutomation | Гибридный рабочий процесс автоматизации |
| LogicAppsManagement | Управление логическими приложениями |
| SQLDataClassification | Классификация & обнаружения данных SQL |

## ПАРАМЕТРЫ

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

### -Location
Расположение ресурса.
Должно совпадать с аналитической рабочей областью журнала.

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

### -ResourceGroupName
Имя получаемой группы ресурсов.
Имя не учитывает регистр.

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

### -SubscriptionId
Получение учетных данных подписки, однозначно идентифицирующей подписку Microsoft Azure.
Идентификатор подписки образует часть URI для каждого вызова службы.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Тег
Теги ресурсов

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

### -Type (тип)
Тип создаваемого решения.
Например, "контейнер".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SolutionType

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkspaceResourceId
Идентификатор ресурса Azure для рабочей области, в которой будет развернуто или включено решение.

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

### -Confirm
Запрашивает подтверждение перед запуском командлета.

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
Показывает, что произойдет при запуске командлета.
Командлет не выполняется.

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

### Microsoft. Azure. PowerShell. командлеты. MonitoringSolutions. Models. Api20151101Preview. ISolution

## Пуск

СВЯЗЫВАЮТ

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ



[Get-AzOperationalInsightsWorkspace](https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace)

