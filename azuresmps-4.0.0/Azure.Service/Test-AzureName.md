---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 0DF54C9D-7A19-4591-A1FC-33C6A4C9BF33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 05a99e1a4965329c0eeb29fe0e014814fd1807b2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075937"
---
# Test-AzureName

## КРАТКИй обзор
Проверяет, существует ли имя облачной службы Microsoft Azure, имя службы хранилища или имя пространства имен служебной шины.

## Максимальное

### Сервиса
```
Test-AzureName [-Service] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Склад
```
Test-AzureName [-Storage] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ServiceBusNamespace
```
Test-AzureName [-ServiceBusNamespace] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Веб-сайта
```
Test-AzureName [-Website] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
Если имя существует, командлет возвращает $True.
Если имя не существует, оно возвращает $False.

## ИЛЛЮСТРИРУЮТ

### Пример 1
```
PS C:\> Test-AzureName -Service "MyNameService1"
```

Эта команда проверяет, является ли "MyNameService1" существующим именем облачной службы Microsoft Azure.

### Пример 2
```
PS C:\> Test-AzureName -Storage "mystorename1"
```

Эта команда проверяет, является ли "mystorename1" существующим именем службы хранилища Microsoft Azure.

### Пример 3
```
PS C:\> Test-AzureName -ServiceBusNamespace "mynamespace"
```

Эта команда проверяет, является ли "MyNamespace" существующим именем пространства имен служебной шины Microsoft Azure.

## ПАРАМЕТРЫ

### -Name (имя)
Указывает имя службы или учетной записи хранилища для проверки.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
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

### -Служба
Задает проверку существующей учетной записи службы.

```yaml
Type: SwitchParameter
Parameter Sets: Service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceBusNamespace
Задает проверку пространства имен для существующего Service Bus.

```yaml
Type: SwitchParameter
Parameter Sets: ServiceBusNamespace
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Хранилище
Определяет проверку существующей учетной записи хранения.

```yaml
Type: SwitchParameter
Parameter Sets: Storage
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Веб-сайт
Проверка существующего веб-сайта.

```yaml
Type: SwitchParameter
Parameter Sets: Website
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

## Пуск
* node-dev, PHP-Dev, Python-dev

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

