---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D4349562-1392-44B6-9353-6231F0CB5C51
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66618c0a684a8e54d41bbe4014ee1e6c893acdbf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076128"
---
# Remove-AzureSchedulerJobCollection

## КРАТКИй обзор
Удаляет коллекцию заданий планировщика.

## Максимальное

```
Remove-AzureSchedulerJobCollection [-Force] [-Location <String>] -JobCollectionName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.
Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .

Командлет **Remove-AzureSchedulerJobCollection** удаляет коллекцию заданий планировщика и все задания из этой коллекции.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Удаление коллекции заданий для местоположения
```
PS C:\> Remove-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01"
```

Эта команда удаляет коллекцию заданий планировщика с именем JobCollection01 в расположении для северной центральной точки США.
Команда также удаляет задания в разделе JobCollection01.

### Пример 2: Удаление расположения задания
```
PS C:\> Remove-AzureSchedulerJobCollection -JobCollectionName "JobCollection02"
```

Эта команда удаляет коллекцию заданий планировщика с именем JobCollection02.
Команда также удаляет задания в разделе JobCollection02.

## ПАРАМЕТРЫ

### -Force
Указывает на то, что этот командлет удаляет коллекцию заданий планировщика без запроса подтверждения.

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

### -JobCollectionName
Указывает имя удаляемой коллекции заданий планировщика.

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

### -Location
Указывает имя расположения, на котором размещается облачная служба.
Допустимые значения: 

- В любом уголке Азии
- В любом уголке Европы
- Где бы мы ни находились
- Восточная Азия
- Восточная часть США
- Северный Центральный США
- Северная Европа
- Южная Центральная американская
- Юго-Восточная Азия
- Западная Европа
- Западная часть США

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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureSchedulerJobCollection](./Get-AzureSchedulerJobCollection.md)

[New-AzureSchedulerJobCollection](./New-AzureSchedulerJobCollection.md)

[Set-AzureSchedulerJobCollection](./Set-AzureSchedulerJobCollection.md)


