---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 92E2409B-14BC-428F-8BAF-60D8DAFA5F57
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1adaafdfdd4331bbba86530eb532964430ed7c69
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075935"
---
# Test-AzureTrafficManagerDomainName

## КРАТКИй обзор
Проверяет, доступно ли имя домена в качестве профиля диспетчера трафика.

## Максимальное

```
Test-AzureTrafficManagerDomainName -DomainName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Test-AzureTrafficManagerDomainName** проверяет, доступно ли имя домена в качестве профиля диспетчера трафика Microsoft Azure.
Если доменное имя доступно, этот командлет возвращает значение $True.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Проверка наличия доменного имени
```
PS C:\>Test-AzureTrafficManagerDomainName -DomainName "ContosoApp.trafficmanager.net"
$True
```

Эта команда проверяет, доступен ли доменное имя ContosoApp.trafficmanager.net в качестве профиля диспетчера трафика.

## ПАРАМЕТРЫ

### -ИмяДомена
Указывает имя доменного имени для проверки.
Необходимо включить следующую строку: 

. trafficmanager.net

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Указывает профиль Azure, из которого считывается этот командлет. Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.

```yaml
Type: AzureSMProfile
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

## НАПРЯЖЕНИЕ

### System. Boolean
Этот командлет создает $True или $False.
Если доменное имя доступно, этот командлет возвращает значение $True.

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

