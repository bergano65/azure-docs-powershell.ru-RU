---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5ff90957a655837dbdf75ce3f4242222615f2a73
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555468"
---
# Get-AzsUserSubscription

## КРАТКИй обзор
Получение списка подписок на пользователя в качестве оператора.

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
Получение списка подписок на пользователя в качестве оператора.

## ИЛЛЮСТРИРУЮТ

### --------------------------ПРИМЕР 1--------------------------
```
Get-AzsUserSubscription
```

Получение списка подписок на пользователя в качестве оператора.

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

### Microsoft. AzureStack. Management. Subscriptions. admin. Models. Subscription

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

