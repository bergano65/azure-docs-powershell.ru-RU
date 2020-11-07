---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4403232b45b2a1e69d6148a118e69ccaf80e4a1e
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908441"
---
# Get-AzsUserSubscription

## КРАТКИй обзор
Получите список подписок пользователей в качестве администратора.

## Максимальное

### Список (по умолчанию)
```
Get-AzsUserSubscription [-Filter <String>] [<CommonParameters>]
```

### Получить
```
Get-AzsUserSubscription -SubscriptionId <Guid> [<CommonParameters>]
```

## NОПИСАНИЕ
Получите список подписок пользователей в качестве администратора.

## ИЛЛЮСТРИРУЮТ

### --------------------------ПРИМЕР 1--------------------------
```
Get-AzsUserSubscription
```

Получите список подписок пользователей в качестве администратора.

## ПАРАМЕТРЫ

### -Фильтр
Параметр фильтра OData.

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

### -SubscriptionId
Параметр идентификатора подписки.

```yaml
Type: Guid
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

### Microsoft. AzureStack. Management. Subscriptions. admin. Models. Subscription

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

