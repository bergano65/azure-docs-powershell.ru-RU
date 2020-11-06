---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationorderid
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrderId.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrderId.md
ms.openlocfilehash: ce6132c7c9b782969b78094de4a055415f3f30ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563343"
---
# Get-AzureRmReservationOrderId

## КРАТКИй обзор
Получить список приемлемых `ReservationOrder` идентификаторов.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Get-AzureRmReservationOrderId [-SubscriptionId <String>] [<CommonParameters>]
```

## NОПИСАНИЕ
Получите идентификаторы `ReservationOrder` , которые можно применить к этой подписке.

## ИЛЛЮСТРИРУЮТ

### Пример 1
```
PS C:\> Get-AzureRmReservationOrderId
```

Применить к `ReservationOrder` подписке по умолчанию

### Пример 2
```
PS C:\> Get-AzureRmReservationOrderId -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

Применить к `ReservationOrder` указанной подписке

## ПАРАМЕТРЫ

### -SubscriptionId
Идентификатор подписки для получения примененного `ReservationOrder` s

```yaml
Type: String
Parameter Sets: (All)
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

### Ничего

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. резервирования. Models. PSAppliedReservationOrderId

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

