---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.CostManagement/new-AzCostManagementQueryFilterObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
ms.openlocfilehash: e7b5c605af531bd1c1251a1c615da9498059d43d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395532"
---
# New-AzCostManagementQueryFilterObject

## SYNOPSIS
Создание объекта в памяти для queryFilter

## СИНТАКСИС

```
New-AzCostManagementQueryFilterObject [-And <IQueryFilter[]>] [-Dimensions <IQueryComparisonExpression>]
 [-Not <IQueryFilter>] [-Or <IQueryFilter[]>] [-Tag <IQueryComparisonExpression>] [<CommonParameters>]
```

## ОПИСАНИЕ
Создание объекта в памяти для queryFilter

## ПРИМЕРЫ

### Пример 1. Создание объекта фильтра запроса для экспорта управления затратами
```powershell
PS C:\> $orDimension = New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Operator In -Value @('East US', 'West Europe')
PS C:\> $orTag = New-AzCostManagementQueryComparisonExpressionObject -Name 'Environment' -Operator In -Value @('UAT', 'Prod')
PS C:\> New-AzCostManagementQueryFilterObject -or @((New-AzCostManagementQueryFilterObject -Dimension $orDimension), (New-AzCostManagementQueryFilterObject -Tag $orTag))

And       :
Dimension : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
Not       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter
Or        : {Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter, Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter}
Tag       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
```

эта команда создает объект фильтра запроса для экспорта управления затратами.

## PARAMETERS

### -And
Логическое выражение AND.
Должен иметь не менее 2 элементов.
Чтобы построить таблицу, см. раздел "ЗАМЕТКИ" для свойств AND и создание hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Размеры
Выражение сравнения для измерений.
Чтобы создать таблицу, см. раздел "ЗАМЕТКИ" для свойств "РАЗМЕРЫ" и создание таблицы с hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryComparisonExpression
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Not
Логическое выражение NOT.
Чтобы построить таблицу, см. раздел "ЗАМЕТКИ" для СВОЙСТВА NOT и создание hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Или
Логическое выражение OR.
Должен иметь не менее 2 элементов.
Чтобы создать таблицу, см. раздел "ЗАМЕТКИ" для свойств OR и создание hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Выражение сравнения для тега.
Чтобы построить таблицу, см. раздел "ЗАМЕТКИ" для свойств тега и создание hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryComparisonExpression
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

## OUTPUTS

### Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter

## ПРИМЕЧАНИЯ

ALIASES

СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ

Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства. Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.


AND <IQueryFilter[]>: логическое выражение AND. Должен иметь не менее 2 элементов.
  - `[And <IQueryFilter[]>]`: логическое выражение AND. Должен иметь не менее 2 элементов.
  - `[Dimensions <IQueryComparisonExpression>]`: имеет выражение сравнения для измерения
    - `Name <String>`: имя столбца, который нужно использовать для сравнения.
    - `Operator <OperatorType>`Оператор, который нужно использовать для сравнения.
    - `Value <String[]>`: массив значений, которые нужно использовать для сравнения
  - `[Not <IQueryFilter>]`: логическое выражение NOT.
  - `[Or <IQueryFilter[]>]`: логическое выражение OR. Должен иметь не менее 2 элементов.
  - `[Tag <IQueryComparisonExpression>]`: имеет выражение сравнения для тега

DIMENSIONS <IQueryComparisonExpression> : имеет выражение сравнения для измерений.
  - `Name <String>`: имя столбца, который нужно использовать для сравнения.
  - `Operator <OperatorType>`Оператор, который нужно использовать для сравнения.
  - `Value <String[]>`: массив значений, которые нужно использовать для сравнения

NOT <IQueryFilter> : логическое выражение NOT.
  - `[And <IQueryFilter[]>]`: логическое выражение AND. Должен иметь не менее 2 элементов.
  - `[Dimensions <IQueryComparisonExpression>]`: имеет выражение сравнения для измерения
    - `Name <String>`: имя столбца, который нужно использовать для сравнения.
    - `Operator <OperatorType>`Оператор, который нужно использовать для сравнения.
    - `Value <String[]>`: массив значений, которые нужно использовать для сравнения
  - `[Not <IQueryFilter>]`: логическое выражение NOT.
  - `[Or <IQueryFilter[]>]`: логическое выражение OR. Должен иметь не менее 2 элементов.
  - `[Tag <IQueryComparisonExpression>]`: имеет выражение сравнения для тега

ИЛИ <IQueryFilter[]>: логическое выражение OR. Должен иметь не менее 2 элементов.
  - `[And <IQueryFilter[]>]`: логическое выражение AND. Должен иметь не менее 2 элементов.
  - `[Dimensions <IQueryComparisonExpression>]`: имеет выражение сравнения для измерения
    - `Name <String>`: имя столбца, который нужно использовать для сравнения.
    - `Operator <OperatorType>`Оператор, который нужно использовать для сравнения.
    - `Value <String[]>`: массив значений, которые нужно использовать для сравнения
  - `[Not <IQueryFilter>]`: логическое выражение NOT.
  - `[Or <IQueryFilter[]>]`: логическое выражение OR. Должен иметь не менее 2 элементов.
  - `[Tag <IQueryComparisonExpression>]`: имеет выражение сравнения для тега

TAG <IQueryComparisonExpression> : имеет выражение сравнения для тега.
  - `Name <String>`: имя столбца, который нужно использовать для сравнения.
  - `Operator <OperatorType>`Оператор, который нужно использовать для сравнения.
  - `Value <String[]>`: массив значений, которые нужно использовать для сравнения

## СВЯЗАННЫЕ ССЫЛКИ

