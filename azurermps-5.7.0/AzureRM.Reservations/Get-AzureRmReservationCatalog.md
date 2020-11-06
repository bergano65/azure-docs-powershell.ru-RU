---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationcatalog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationCatalog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationCatalog.md
ms.openlocfilehash: 4714b97773583197807d6ca54152ee25ab520909
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563352"
---
# Get-AzureRmReservationCatalog

## КРАТКИй обзор
Получение каталога для доступного резервирования

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Get-AzureRmReservationCatalog [-SubscriptionId <String>] [<CommonParameters>]
```

## NОПИСАНИЕ
Получите регионы и SKU, доступные для зарезервированного экземпляра покупки для указанной подписки Azure.

## ИЛЛЮСТРИРУЮТ

### Пример 1
```
PS C:\> Get-AzureRmReservationCatalog
```

Получение каталога для подписки по умолчанию

### Пример 2
```
PS C:\> Get-AzureRmReservationCatalog -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

Получение каталога для указанной подписки

## ПАРАМЕТРЫ

### -SubscriptionId
Идентификатор подписки

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

### System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. резервирования. Models. PSCatalog, Microsoft. Azure. Commands. резервирования, Version = 1.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

