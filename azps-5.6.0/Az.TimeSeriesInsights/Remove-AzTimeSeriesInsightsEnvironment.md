---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: 89fa39a5e6e1bb2ded61c41dd553b6d7d0473d4f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963379"
---
# Remove-AzTimeSeriesInsightsEnvironment

## SYNOPSIS
Удаляет среду с указанным именем в указанной группе подписок и ресурсов.

## СИНТАКСИС

### Delete (По умолчанию)
```
Remove-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### DeleteViaIdentity
```
Remove-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## ОПИСАНИЕ
Удаляет среду с указанным именем в указанной группе подписок и ресурсов.

## ПРИМЕРЫ

### Пример 1. Удаление среды с ряду времени по имени
```powershell
PS C:\> Remove-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsill

```

Эта команда удаляет среду статистики по рядам времени.

### Пример 2. Удаление среды статистики по рядам времени для объекта
```powershell
PS C:\> $env = Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsill
PS C:\> Remove-AzTimeSeriesInsightsEnvironment -InputObject $env

```

Эта команда удаляет среду статистики по рядам времени.

## PARAMETERS

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

### -InputObject
Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Имя среды Time Series Insights, связанной с указанной группой ресурсов.

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Возвращает "Истина" в случае успешной команды.

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

### -ResourceGroupName
Имя группы ресурсов Azure.

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
ИД подписки Azure.

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
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

### Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity

## OUTPUTS

### System.Boolean

## ПРИМЕЧАНИЯ

ALIASES

СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ

Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства. Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.


INPUTOBJECT <ITimeSeriesInsightsIdentity> : Параметр identity
  - `[AccessPolicyName <String>]`: имя политики доступа.
  - `[EnvironmentName <String>]`: название среды
  - `[EventSourceName <String>]`: имя источника события "Time Series Insights", связанного с указанной средой.
  - `[Id <String>]`: путь удостоверения ресурса
  - `[ReferenceDataSetName <String>]`: Имя набора справочных данных.
  - `[ResourceGroupName <String>]`: Имя группы ресурсов Azure.
  - `[SubscriptionId <String>]`: Azure Subscription ID.

## СВЯЗАННЫЕ ССЫЛКИ

