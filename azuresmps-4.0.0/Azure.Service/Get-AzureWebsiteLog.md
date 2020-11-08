---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: BFB57100-93F6-4FD2-8ECA-7F54BEB0D6B0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7114f39ee2b105c80429151df8347b5c17dcfea0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076506"
---
# Get-AzureWebsiteLog

## КРАТКИй обзор
Получает журналы для указанного веб-сайта.

## Максимальное

### Копирован
```
Get-AzureWebsiteLog [-Path <String>] [-Message <String>] [-Tail] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ListPath
```
Get-AzureWebsiteLog [-ListPath] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.
Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .

Получает журнал для указанного веб-сайта.

## ИЛЛЮСТРИРУЮТ

### Пример 1: запуск потоковой передачи журнала
```
PS C:\> Get-AzureWebsiteLog -Tail
```

В этом примере начинается потоковая передача журнала для всех журналов приложений.

### Пример 2: запуск потоковой передачи журнала для журналов HTTP
```
PS C:\> Get-AzureWebsiteLog -Tail -Path http
```

В этом примере начинается потоковая передача журнала для журналов HTTP.

### Пример 3: запуск потоковой передачи журнала для журналов ошибок
```
PS C:\> Get-AzureWebsiteLog -Tail -Message Error
```

В этом примере начинается потоковая передача журнала и отображаются только журналы ошибок.

### Пример 4: отображение журналов avaiable
```
PS C:\> Get-AzureWebsiteLog -Name MyWebsite -ListPath
```

В этом примере перечислены все доступные пути журналов на веб-сайте.

## ПАРАМЕТРЫ

### -ListPath
Указывает, следует ли отображать пути к журналу.

```yaml
Type: SwitchParameter
Parameter Sets: ListPath
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Сообщение
Указывает строку, которая будет использоваться для фильтрации сообщения журнала.
Будут возвращены только журналы, содержащие эту строку.

```yaml
Type: String
Parameter Sets: Tail
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (имя)
Имя веб-сайта.

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

### -Path
Путь, из которого будет получен журнал.
По умолчанию он является корневым, то есть включает все пути.

```yaml
Type: String
Parameter Sets: Tail
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
Указывает имя гнезда.

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

### -Tail
Указывает, следует ли передавать журналы.

```yaml
Type: SwitchParameter
Parameter Sets: Tail
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureWebsite](./Get-AzureWebsite.md)

[New-AzureWebsite](./New-AzureWebsite.md)

[Remove-AzureWebsite](./Remove-AzureWebsite.md)

[Start-AzureWebsite](./Start-AzureWebsite.md)


