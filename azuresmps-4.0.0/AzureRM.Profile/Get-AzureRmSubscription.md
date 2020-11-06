---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 13dd14f59b28e3b5730f207c675771e1275392d3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555631"
---
# Get-AzureRmSubscription

## КРАТКИй обзор
Получение подписок, доступ к которым разрешен текущей учетной записью.

## Максимальное

### ListByIdInTenant (по умолчанию)
```
Get-AzureRmSubscription [-SubscriptionId <String>] [-TenantId <String>] [<CommonParameters>]
```

### ListByNameInTenant
```
Get-AzureRmSubscription [-SubscriptionName <String>] [-TenantId <String>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет Get-AzureRmSubscription получает идентификатор подписки, имя подписки и домашний клиент для подписок, доступ к которым имеет текущая учетная запись.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение всех подписок во всех клиентах
```
PS C:\>Get-AzureRmSubscription -All

Subscription Name : Contoso Subscription 1
SubscriptionId    : xxxx-xxxx-xxxx-xxxx
TenantId          : yyyy-yyyy-yyyy-yyyy
```

Эта команда получает все подписки во всех клиентах, которые авторизованы для текущей учетной записи.

### Пример 2: получение всех подписок для определенного клиента
```
PS C:\>Get-AzureRmSubscription -TenantId "xxxx-xxxx-xxxx-xxxx"

Subscription Name : Contoso Subscription 1
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx

Subscription Name : Contoso Subscription 2
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx
```

Список всех подписок в данном клиенте, которые авторизованы для текущей учетной записи.

### Пример 3: получение всех подписок в текущем клиенте
```
PS C:\>Get-AzureRmSubscription

Subscription Name : Contoso Subscription 1
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx

Subscription Name : Contoso Subscription 2
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx
```

Эта команда получает все подписки в текущем клиенте, которые авторизованы для текущего пользователя.

### Пример 4: изменение текущего контекста на использование конкретной подписки
```
PS C:\>Get-AzureRmSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzureRmContext

Subscription Name : Contoso Subscription 1
SubscriptionId    : xxxx-xxxx-xxxx-xxxx
TenantId          : yyyy-yyyy-yyyy-yyyy
```

Эта команда получает указанную подписку, а затем задает текущий контекст для ее использования.
Все последующие командлеты в этом сеансе используют новую подписку (на подписку Contoso 1) по умолчанию.

## ПАРАМЕТРЫ

### -SubscriptionId
Указывает идентификатор подписки, которую требуется получить.

```yaml
Type: String
Parameter Sets: ListByIdInTenant
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubscriptionName
Указывает имя подписку, которую требуется получить.

```yaml
Type: String
Parameter Sets: ListByNameInTenant
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TenantId
Указывает ИД клиента, который содержит подписки, которые требуется получить.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

### PSAzureSubscription

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

