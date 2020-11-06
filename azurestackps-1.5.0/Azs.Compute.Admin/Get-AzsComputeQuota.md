---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 30a1bc70b4e704d8dadf864dedf7173476909cf2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555944"
---
# Get-AzsComputeQuota

## КРАТКИй обзор
Возвращает квоты с указанием предельных квот для вычисляемых объектов.

## Максимальное

### Список (по умолчанию)
```
Get-AzsComputeQuota [-Location <String>] [<CommonParameters>]
```

### Получить
```
Get-AzsComputeQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### ResourceId
```
Get-AzsComputeQuota -ResourceId <String> [<CommonParameters>]
```

## NОПИСАНИЕ
Получение списка существующих квот.

## ИЛЛЮСТРИРУЮТ

### --------------------------ПРИМЕР 1--------------------------
```
Get-AzsComputeQuota -Location 'local'
```

Получить все расчетные квоты в указанном расположении.

### --------------------------ПРИМЕР 2--------------------------
```
Get-AzsComputeQuota 'Default Quota'
```

Получить определенную расчетную квоту.

## ПАРАМЕТРЫ

### -Location
Расположение ресурса.

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (имя)
Имя квоты.

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Идентификатор ресурса.

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

### ComputeQuotaObject

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

