---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E4B1AA31-1185-4035-86E6-2BB2587285C6
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8273613081ab6bab0c9c3481df90f5b680b3355
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076274"
---
# Get-AzureWebsite

## КРАТКИй обзор
Получение веб-сайтов Azure в текущей подписке.

## Максимальное

```
Get-AzureWebsite [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureWebsite** получает сведения о веб-сайтах Azure в текущей подписке.

По умолчанию **Get-AzureWebsite** получает все веб-сайты Azure в текущей подписке и возвращает объект, который предоставляет основные сведения о сайтах.
При использовании параметра *Name* **Get-AzureWebsite** возвращает объект с подробными сведениями, в том числе с подробными сведениями о конфигурации.

Текущая подписка — это подписку, обозначенную как "Текущая". Чтобы найти текущую подписку, используйте *текущий* параметр командлета [Get-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397623) .
Чтобы изменить текущую подписку, используйте командлет [SELECT-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397628) .

В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.
Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение всех веб-сайтов в подписке
```
PS C:\> Get-AzureWebsite
```

Эта команда получает все веб-сайты Azure в текущей подписке.

### Пример 2: получение веб-сайта по имени
```
PS C:\> Get-AzureWebsite -Name ContosoWeb
```

Эта команда получает подробные сведения о веб-сайте ContosoWeb Azure, включая сведения о конфигурации.
При использовании параметра *Name* **Get-AzureWebsite** возвращает объект **SiteWithConfig** с расширенными сведениями о веб-сайте.

### Пример 3: получение подробных сведений обо всех веб-сайтах
```
PS C:\> Get-AzureWebsite | ForEach-Object {Get-AzureWebsite -Name $_.Name}
```

Эта команда получает подробные сведения обо всех веб-сайтах в подписке.
Она использует команду **Get-AzureWebsite** для получения всех веб-сайтов, а затем использует командлет **ForEach-Object** для получения каждого веб-сайта по имени.

### Пример 4: получение сведений о слоте развертывания
```
PS C:\> Get-AzureWebsite -Name ContosoWeb -Slot Staging
```

Эта команда получает промежуточный слот развертывания на веб-сайте ContosoWeb.
Слоты развертывания позволяют тестировать разные версии веб-сайта Azure без их освобождения.

### Пример 5: получение экземпляров веб-сайтов
```
PS C:\>(Get-AzureWebsite -Name ContosoWeb).Instances

InstanceId
----------
2d8e712fb8f85d061c30fd793a534e6700a175f9a9ab12ca55cb3b0edfcc10ee
5834916b8cef49249b18187708223a33fbbc4352d33b48369f3166644bdd3445

PS C:\>(Get-AzureWebsite -Name ContosoWeb).Instances.Count
2
```

Команды в этом примере используют свойство Instances веб-сайта Azure для получения сведений о текущих экземплярах веб-сайта.
Свойство **Instances** Добавлено в объект **SiteWithConfig** в версии 0.8.3 модуля Azure.

Первая команда получает идентификаторы экземпляров всех запущенных в данный момент экземпляров веб-сайта.
Вторая команда возвращает число запущенных экземпляров веб-сайта.
Свойство **Count** можно использовать в любом массиве.

## ПАРАМЕТРЫ

### -Name (имя)
Получение подробных сведений о конфигурации указанного веб-сайта.
Введите имя одного веб-сайта в подписке.
По умолчанию **Get-AzureWebsite** получает все веб-сайты в текущей подписке.
Значение *Name* не поддерживает подстановочные знаки.

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

### -Slot
Получает указанную область развертывания для веб-сайта.
Введите имя гнезда, например "промежуточное хранение" или "производство".
Дополнительные сведения о слотах развертывания можно найти в разделе поэтапное развертывание на веб-сайтах Microsoft Azure https://azure.microsoft.com/en-us/documentation/articles/web-sites-staged-publishing/ .
Чтобы добавить слот развертывания на существующий веб-сайт Azure, используйте командлет Set-AzureWebsite.

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

### Ничего
Вы можете передавать входные данные командлету по имени свойства, но не по значению.

## НАПРЯЖЕНИЕ

### Microsoft. WindowsAzure. Commands. Utilities. website. Services. Entities. site
По умолчанию **Get-AzureWebsite** возвращает массив объектов **сайта** .

### Microsoft. WindowsAzure. Commands. Utilities. website. Services. Entities. SiteWithConfig
При использовании параметра *Name* **Get-AzureWebsite** возвращает объект **SiteWithConfig** .

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[New-AzureWebsite](./New-AzureWebsite.md)

[Remove-AzureWebsite](./Remove-AzureWebsite.md)

[Start-AzureWebsite](./Start-AzureWebsite.md)

[Остановить-AzureWebsite](./Stop-AzureWebsite.md)

[Show-AzureWebsite](./Show-AzureWebsite.md)


