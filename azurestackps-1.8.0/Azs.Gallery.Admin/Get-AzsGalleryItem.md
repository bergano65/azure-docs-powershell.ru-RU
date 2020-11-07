---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0fa95e34c6a220a496a79f7a72c65c222f1376f1
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908326"
---
# Get-AzsGalleryItem

## КРАТКИй обзор
Список элементов коллекции.

## Максимальное

### Список (по умолчанию)
```
Get-AzsGalleryItem [<CommonParameters>]
```

### Получить
```
Get-AzsGalleryItem [-Name] <String> [<CommonParameters>]
```

## NОПИСАНИЕ
Получение списка элементов коллекции, доступных в Azure Stack Marketplace

## ИЛЛЮСТРИРУЮТ

### ПРИМЕР 1
```
Get-AzsGalleryItem
```

Элементы коллекции списка.

### ПРИМЕР 2
```
Get-AzsGalleryItem -Name 'microsoft.vmss.1.3.6'
```

Получение элемента коллекции по имени.

## ПАРАМЕТРЫ

### -Name (имя)
Удостоверение элемента коллекции.
Содержит имя издателя, имя элемента и может включать версию, разделенную на символ точки.

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

### Microsoft. AzureStack. Management. Gallery. admin. Model. GalleryItem

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
