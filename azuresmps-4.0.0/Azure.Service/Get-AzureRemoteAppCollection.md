---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 8F00099A-042A-4450-B6CF-9EDA2350CBFC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94e1711bc42745b872a8e2abc8cf82e5e0e67db9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076329"
---
# Get-AzureRemoteAppCollection

## КРАТКИй обзор
Получение сведений о коллекции RemoteApp Azure.

## Максимальное

```
Get-AzureRemoteAppCollection [[-CollectionName] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRemoteAppCollection** извлекает сведения о коллекциях RemoteApp Azure в Microsoft Azure.
Он возвращает объект со сведениями о конкретной коллекции или не указан ни одной коллекцией для всех коллекций в текущей подписке.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение списка всех коллекций
```
PS C:\> Get-AzureRemoteAppCollection
```

Эта команда возвращает список всех коллекций RemoteApp Azure в подписке.

### Пример 2: получение сведений об указанной коллекции
```
PS C:\> Get-AzureRemoteAppCollection ContosoApps
```

Эта команда возвращает сведения о коллекции RemoteApp Azure с именем ContosoApps.

### Пример 3: получение списка коллекций с использованием подстановочных знаков
```
PS C:\> Get-AzureRemoteAppCollection Finance*
```

Эта команда возвращает список всех коллекций RemoteApp Azure, отвечающих финансовому запросу *.

## ПАРАМЕТРЫ

### -CollectionName
Указывает имя коллекции Azure RemoteApp.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### -Profile
Указывает профиль Azure, из которого считывается этот командлет.
Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.

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

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[New-AzureRemoteAppCollection](./New-AzureRemoteAppCollection.md)

[Remove-AzureRemoteAppCollection](./Remove-AzureRemoteAppCollection.md)

[Set-AzureRemoteAppCollection](./Set-AzureRemoteAppCollection.md)

[Update-AzureRemoteAppCollection](./Update-AzureRemoteAppCollection.md)


