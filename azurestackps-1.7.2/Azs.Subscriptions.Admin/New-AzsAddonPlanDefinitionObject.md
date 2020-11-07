---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 57d7037f6deb669531bb03c3bf4f2e504586f832
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904425"
---
# New-AzsAddonPlanDefinitionObject

## КРАТКИй обзор
Название нужного плана, связанного с предложением или разорвать его связь.

## Максимальное

```
New-AzsAddonPlanDefinitionObject [[-PlanId] <String>] [[-MaxAcquisitionCount] <Int64>] [<CommonParameters>]
```

## NОПИСАНИЕ
Название нужного плана, связанного с предложением или разорвать его связь.

## ИЛЛЮСТРИРУЮТ

### --------------------------ПРИМЕР 1--------------------------
```
New-AzsAddonPlanDefinitionObject -PlanId $planIdentifier -MaxAcquisitionCount 500
```

Создайте новый объект определения плана для указанного плана с ограничением приобретения 500.

## ПАРАМЕТРЫ

### -MaxAcquisitionCount
Максимальное количество экземпляров, которое может быть получено одной подпиской.
Если не указано, предполагается значение 1.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PlanId
Идентификатор плана.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

