---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrder.md
ms.openlocfilehash: 12e76c3412f54ba840528f9ff1a40acd388cd109
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560732"
---
# Get-AzureRmReservationOrder

## КРАТКИй обзор
Получить `ReservationOrder`

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Get-AzureRmReservationOrder [-ReservationOrderId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Список всех `ReservationOrder` пользователей, к которым у пользователя есть доступ в текущем клиенте. Если задан параметр ReservationOrderId, получите этот конкретный ReservationOrder.

## ИЛЛЮСТРИРУЮТ

### Пример 1
```
PS C:\> Get-AzureRmReservationOrder
```

Список всех `ReservationOrder` пользователей, имеющих доступ к текущему клиенту

### Пример 2
```
PS C:\> Get-AzureRmReservationOrder -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff"
```

Получение `ReservationOrder` с помощью указанного ReservationOrderId

## ПАРАМЕТРЫ

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReservationOrderId
Идентификатор определенного ReservationOrder, который пользователь хочет просмотреть

```yaml
Type: System.Guid
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

### Microsoft. Azure. Commands. резервирования. Models. PSReservationOrderPage

### Microsoft. Azure. Commands. резервирования. Models. PSReservationOrder

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
