---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/split-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Split-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Split-AzureRmReservation.md
ms.openlocfilehash: 89c19f2c61604f3c38ba8cc9679f956d68df3179
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563347"
---
# Split-AzureRmReservation

## КРАТКИй обзор
Разделение а `Reservation` .

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### CommandLine (по умолчанию)
```
Split-AzureRmReservation -ReservationOrderId <String> -ReservationId <String> -Quantity <Nullable`1[]>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### PipeObject
```
Split-AzureRmReservation -Quantity <Nullable`1[]> -Reservation <PSReservation> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Разделите элемент на `Reservation` две `Reservation` s с указанным распределением количества.

## ИЛЛЮСТРИРУЮТ

### Пример 1
```
PS C:\> Split-AzureRmReservation -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111" -Quantities 2,3
```

Разделение заданной `Reservation` `Reservation` величины на две с помощью соответствующих количеств

## ПАРАМЕТРЫ

### -Количество
Целые числа, разделенные запятыми, в поле количества двух `Reservation` s

```yaml
Type: Nullable`1[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Резервирование
Параметр объекта pipe для `Reservation`

```yaml
Type: PSReservation
Parameter Sets: PipeObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ReservationId
Идентификатор `Reservation` для разделения

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReservationOrderId
Идентификатор элемента, `ReservationOrder` содержащего сведения о том `Reservation` , что пользователь хочет разделить

```yaml
Type: String
Parameter Sets: CommandLine
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске командлета. Командлет не выполняется.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Microsoft. Azure. Commands. резервирования. Models. PSReservation

## НАПРЯЖЕНИЕ

### System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. резервирования. Models. PSReservation, Microsoft. Azure. Commands. резервирования, Version = 1.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

