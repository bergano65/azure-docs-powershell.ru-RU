---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2cabb88c490c7fdea56fd5ffde280cfd55bc8f3d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555628"
---
# Get-AzureRmTenant

## КРАТКИй обзор
Возвращает клиентов, которые авторизованы для текущего пользователя.

## Максимальное

```
Get-AzureRmTenant [[-TenantId] <String>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет Get-AzureRmTenant получает клиентов, которые авторизованы для текущего пользователя.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Загрузка всех клиентов
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmTenant

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com

TenantId : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Domain   : microsoft.com
```

В этом примере показано, как получить всех авторизованных клиентов учетной записи Azure.

### Пример 2: как относящихся к определенному клиенту
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com
```

В этом примере показано, как получить определенного авторизованного клиента учетной записи Azure.

## ПАРАМЕТРЫ

### -TenantId
Указывает идентификатор клиента, который получает этот командлет.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Domain, Tenant

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

### PSAzureTenant
Этот командлет возвращает ИД клиента и сведения о соответствующем домене для клиентов, которые уполномочены для текущей учетной записи.

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

