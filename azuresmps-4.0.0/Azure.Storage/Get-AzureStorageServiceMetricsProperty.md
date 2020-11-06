---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: ''
schema: 2.0.0
ms.openlocfilehash: b9117d5a4149842ffd136caf1c986c70a4b5e187
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556240"
---
# Get-AzureStorageServiceMetricsProperty

## КРАТКИй обзор
Возвращает свойства метрик для службы хранилища Azure.

## Максимальное

```
Get-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureStorageServiceMetricsProperty** получает свойства метрик для службы хранилища Azure.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение свойств метрик для службы больших двоичных объектов
```
C:\PS>Get-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

Эта команда получает свойства метрик для хранилища больших двоичных объектов для типа метрики "Часы".

## ПАРАМЕТРЫ

### -Context
Указывает контекст хранилища Azure.
Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -MetricsType
Указывает тип метрики.
Этот командлет получает свойства метрик службы хранилища Azure для типа метрики, указанном в этом параметре.
Допустимые значения этого параметра: hours и Minute.

```yaml
Type: ServiceMetricsType
Parameter Sets: (All)
Aliases: 
Accepted values: Hour, Minute

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceType
Указывает тип службы хранилища.
Этот командлет получает свойства метрик для типа, который указывает этот параметр.
Для этого параметра допустимы следующие значения:

- Большом 
- Таблич
- Поместить
- Файл 

Значение "файл" в настоящее время не поддерживается.

```yaml
Type: StorageServiceType
Parameter Sets: (All)
Aliases: 
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
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

[New-AzureStorageContext](./New-AzureStorageContext.md)

[Set-AzureStorageServiceMetricsProperty](./Set-AzureStorageServiceMetricsProperty.md)


