---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 914b75e3952f7841aaf3ff505f51f7b4ebdc6044
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555635"
---
# Get-AzureRmContext

## КРАТКИй обзор
Получает метаданные, используемые для проверки подлинности запросов диспетчера ресурсов Azure.

## Максимальное

```
Get-AzureRmContext [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет Get-AzureRmContext получает текущие метаданные, используемые для проверки подлинности запросов диспетчера ресурсов Azure.

Этот командлет получает учетную запись Active Directory, клиента Active Directory, подписку на Azure и целевую среду Azure.
Командлеты диспетчера ресурсов Azure по умолчанию используют эти параметры при выполнении запросов в диспетчере ресурсов Azure.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Загрузка текущего контекста
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmContext

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

В этом примере мы используем подписку на Azure для входа в нашу учетную запись с помощью Add-AzureRmAccount, а затем получили контекст текущего сеанса, вызвав Get-AzureRmContext.

## ПАРАМЕТРЫ

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

### PSAzureContext
Этот командлет возвращает учетную запись, клиента и подписку, используемые командлетами диспетчера ресурсов Azure.

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Set-AzureRMContext]()

