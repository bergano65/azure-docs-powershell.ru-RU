---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e4c464d2d0e822b745acc2a7c6daecf329449105
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555400"
---
# Get-AzsDisk

## КРАТКИй обзор
Возвращает список управляемых дисков, которые можно перенести в указанном общем доступе.

## Максимальное

### Список (по умолчанию)
```
Get-AzsDisk [-Location <String>] [-Start <Int32>] [-SharePath <String>] [-Count <Int32>]
 [-UserSubscriptionId <String>] [-Status <String>] [<CommonParameters>]
```

### ResourceId
```
Get-AzsDisk -ResourceId <String> [<CommonParameters>]
```

### Получить
```
Get-AzsDisk [-Location <String>] -Name <String> [<CommonParameters>]
```

## NОПИСАНИЕ
Возвращает список дисков.

## ИЛЛЮСТРИРУЮТ

### --------------------------ПРИМЕР 1--------------------------
```
$disks = Get-AzsDisk -location local
```

Возвращает список управляемых дисков на локальном расположении.
По умолчанию первые диски 100 будут

### --------------------------ПРИМЕР 2--------------------------
```
$disk = Get-AzsDisk -location local -name $DiskId
```

Получение определенного управляемого диска.

## ПАРАМЕТРЫ

### — Количество
Максимальное количество возвращаемых дисков.

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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
Идентификатор GUID диска.

```yaml
Type: String
Parameter Sets: Get
Aliases: DiskId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Идентификатор ресурса.

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SharePath
Исходный файл, к которому относится ресурс.

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Start
Начальный индекс дисков в запросе.

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Status (состояние)
Параметры состояния диска.

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserSubscriptionId
Идентификатор подписки клиента, которому принадлежит ресурс.

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

### Microsoft. AzureStack. Management. COMPUTE. admin. Model. Disk

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

