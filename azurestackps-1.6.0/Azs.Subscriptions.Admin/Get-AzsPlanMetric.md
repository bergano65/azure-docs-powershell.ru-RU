---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cadf5ad37119ab6b50191e50e8ec281fe4bce2d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555988"
---
# Get-AzsPlanMetric

## КРАТКИй обзор
Получение метрик плана.

## Максимальное

```
Get-AzsPlanMetric [-ResourceGroupName] <String> [-PlanName] <String> [<CommonParameters>]
```

## NОПИСАНИЕ
Получение метрик плана.

## ИЛЛЮСТРИРУЮТ

### --------------------------ПРИМЕР 1--------------------------
```
Get-AzsPlanMetric -ResourceGroupName rg1 -PlanName plan1
```

Получение метрик плана.

## ПАРАМЕТРЫ

### -PlanName
Название плана.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Группа ресурсов, в которой находится ресурс.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

### Microsoft. AzureStack. Management. Subscriptions. admin. Models. Metric

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

