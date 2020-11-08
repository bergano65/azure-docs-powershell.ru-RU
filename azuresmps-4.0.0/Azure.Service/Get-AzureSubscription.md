---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 32BC6CE6-60EF-4A46-912B-8FE4FCCDF7CC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2b91906a25d2f2d7c40f96ed07a4fd7463722023
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075537"
---
# Get-AzureSubscription

## КРАТКИй обзор
Получение подписок на Azure в учетной записи Azure.

## Максимальное

### ByName (по умолчанию)
```
Get-AzureSubscription [-SubscriptionName <String>] [-ExtendedDetails] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ById
```
Get-AzureSubscription [-SubscriptionId <String>] [-ExtendedDetails] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### По умолчанию
```
Get-AzureSubscription [-Default] [-ExtendedDetails] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Текущей
```
Get-AzureSubscription [-Current] [-ExtendedDetails] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureSubscription** получает подписки в учетной записи Azure.
Вы можете использовать этот командлет для получения сведений о подписке и для канала подписки на другие командлеты.

Для **Get-AzureSubscription** требуется доступ к учетным записям Azure.
Перед запуском **Get-AzureSubscription** необходимо запустить командлет **Add-AzureAccount** или командлеты, которые загружают и устанавливают файл параметров публикации ( **Get-AzurePublishSettingsFile** , **Import-AzurePublishSettingsFile**.

В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.
Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение всех подписок
```
C:\PS>Get-AzureSubscription
```

Эта команда получает все подписки в учетной записи.

### Пример 2: получение подписки по имени
```
C:\PS>Get-AzureSubscription -SubscriptionName "MyProdSubscription"
```

Эта команда получает только подписку на "MyProdSubsciption".

### Пример 3: получение подписки по умолчанию
```
C:\PS>(Get-AzureSubscription -Default).SubscriptionName
```

Эта команда возвращает только имя подписки по умолчанию.
Команда сначала получает подписку, а затем использует метод Dot для получения свойства **SubscriptionName** подписки.

### Пример 4: получение свойств выбранных подписок
```
C:\PS>Get-AzureSubscription -Current | Format-List -Property SubscriptionName, Certificate
```

Эта команда возвращает список с именем и сертификатом текущей подписки.
Для получения текущей подписки используется команда **Get-AzureSubscription** .
Затем он поддает подписку на команду **Format-List** , которая отображает выбранные свойства в списке.

### Пример 5: использование альтернативного файла данных подписки
```
C:\PS>Get-AzureSubscription -SubscriptionDataFile "C:\Temp\MySubscriptions.xml"
```

Эта команда получает подписку из файла данных подписки C:\Temp\MySubscriptions.xml.
Если вы указали альтернативный файл данных подписки при выполнении командлетов **Add-AzureAccount** или **Import-PublishSettingsFile** , используйте параметр **SubscriptionDataFile** .

## ПАРАМЕТРЫ

### -Current
Возвращает только текущую подписку, то есть подписку, обозначенную как "Текущая". По умолчанию **Get-AzureSubscription** получает все подписки в учетных записях Azure.
Чтобы назначить подписку "Current", используйте **текущий** параметр командлета **SELECT-AzureSubscription** .

```yaml
Type: SwitchParameter
Parameter Sets: Current
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Default
Получает только подписку по умолчанию, то есть подписку, назначенную по умолчанию. По умолчанию **Get-AzureSubscription** получает все подписки в учетных записях Azure.
Чтобы назначить подписку по умолчанию, используйте параметр **по умолчанию** командлета **SELECT-AzureSubscription** .

```yaml
Type: SwitchParameter
Parameter Sets: Default
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExtendedDetails
Возвращает сведения о квоте для подписки в дополнение к стандартным параметрам.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
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

### -SubscriptionId
```yaml
Type: String
Parameter Sets: ById
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubscriptionName
Возвращает только указанную подписку.
Введите имя подписки.
Значение чувствительно к регистру.
Подстановочные знаки не поддерживаются.
По умолчанию **Get-AzureSubscription** получает все подписки в учетных записях Azure.

```yaml
Type: String
Parameter Sets: ByName
Aliases: Name

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
Вы можете передать входные данные свойству **SubscriptionName** по имени, но не по значению.

## НАПРЯЖЕНИЕ

### Microsoft. WindowsAzure. Commands. Utilities. Common. WindowsAzureSubscription

## Пуск
* Get-AzureSubscription получает данные из файла данных подписки, создаваемого командлетами **Add-AzureAccount** и **Import-PublishSettingsFile** .

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Add-AzureAccount](./Add-AzureAccount.md)

[Get-AzurePublishSettingsFile](./Get-AzurePublishSettingsFile.md)

[Import-AzurePublishSettingsFile](./Import-AzurePublishSettingsFile.md)

[Remove-AzureSubscription](./Remove-AzureSubscription.md)

[Set-AzureSubscription](./Set-AzureSubscription.md)


