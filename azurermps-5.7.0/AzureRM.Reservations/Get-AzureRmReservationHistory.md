---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationHistory.md
ms.openlocfilehash: 75ff92efe1a37e55396da7dc6d644408952ed179
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566920"
---
# Get-AzureRmReservationHistory

## КРАТКИй обзор
Получение `Reservation` журнала изменений.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### CommandLine (по умолчанию)
```
Get-AzureRmReservationHistory -ReservationOrderId <String> -ReservationId <String> [<CommonParameters>]
```

### PipeObject
```
Get-AzureRmReservationHistory -Reservation <PSReservation> [<CommonParameters>]
```

## NОПИСАНИЕ
Список всех исправлений для `Reservation` .

## ИЛЛЮСТРИРУЮТ

### Пример 1
```
PS C:\> Get-AzureRmReservationHistory -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "00000000-ffff-ffff-0000-00000fffff"
```

Получение истории исправлений для определенного резервирования

## ПАРАМЕТРЫ

### -Резервирование
Параметр объекта pipe для `Reservation` s

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
ReservationId, в `Reservation` котором будет отображаться история

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ReservationOrderId
ReservationOrderId `ReservationOrder` , где находится `Reservation`

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String
Microsoft. Azure. Commands. резервирования. Models. PSReservation

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. резервирования. Models. PSReservationPage

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

