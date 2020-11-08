---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 37C788AC-B369-432B-8276-27FFB0B4CF10
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8d2913877a9f68621bb5c1c930443a46e91e5935
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94077391"
---
# Get-WAPackVMTemplate

## КРАТКИй обзор
Получение шаблонов виртуальных машин.

## Максимальное

### Пустой (по умолчанию)
```
Get-WAPackVMTemplate [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### FromId
```
Get-WAPackVMTemplate [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### FromName
```
Get-WAPackVMTemplate [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
Эти разделы устарели и будут исключены в будущем.
В этом разделе описан командлет в версии 0.8.1 модуля Microsoft Azure PowerShell.
Чтобы узнать версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .

Командлет **Get-WAPackVMTemplate** получает шаблоны виртуальных машин.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение шаблона виртуальной машины с помощью имени
```
PS C:\> Get-WAPackVMTemplate -Name "ContosoTemplate04"
```

Эта команда получает шаблон виртуальной машины с именем ContosoTemplate04.

### Пример 2: получение шаблона виртуальной машины с помощью идентификатора
```
PS C:\> Get-WAPackVMTemplate -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

Эта команда получает шаблон виртуальной машины с указанным ИДЕНТИФИКАТОРом.

### Пример 3: получение всех шаблонов виртуальных машин
```
PS C:\> Get-WAPackVMTemplate
```

Эта команда возвращает все шаблоны виртуальных машин.

## ПАРАМЕТРЫ

### -ID
Указывает уникальный идентификатор шаблона.

```yaml
Type: Guid
Parameter Sets: FromId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (имя)
Указывает имя шаблона.

```yaml
Type: String
Parameter Sets: FromName
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

[Get-WAPackVM](./Get-WAPackVM.md)


