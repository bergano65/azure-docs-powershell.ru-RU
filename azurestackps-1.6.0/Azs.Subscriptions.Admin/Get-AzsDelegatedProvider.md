---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88c19285ee7188dab272eeab7a668f5f5dfe22a4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556032"
---
# Get-AzsDelegatedProvider

## КРАТКИй обзор
Получение списка delegatedProviders.

## Максимальное

### Список (по умолчанию)
```
Get-AzsDelegatedProvider [<CommonParameters>]
```

### Получить
```
Get-AzsDelegatedProvider [-DelegatedProviderId] <Guid> [<CommonParameters>]
```

## NОПИСАНИЕ
Получение списка delegatedProviders.

## ИЛЛЮСТРИРУЮТ

### --------------------------ПРИМЕР 1--------------------------
```
Get-AzsDelegatedProvider
```

Получение списка делегированных поставщиков.

### --------------------------ПРИМЕР 2--------------------------
```
Get-AzsDelegatedProvider -DelegatedProviderId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

Получить определенного делегируемого поставщика.

## ПАРАМЕТРЫ

### -DelegatedProviderId
Идентификатор DelegatedProvider.

```yaml
Type: Guid
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
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

