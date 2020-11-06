---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: ''
schema: 2.0.0
ms.openlocfilehash: d615c0a807c12640f20a72b97a2c11c2efcd5b28
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556247"
---
# Get-AzureStorageServiceLoggingProperty

## КРАТКИй обзор
Получение свойств ведения журнала для служб хранилища Azure.

## Максимальное

```
Get-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureStorageServiceLoggingProperty** получает свойства ведения журнала для служб хранилища Azure.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение свойств ведения журнала для службы больших двоичных объектов
```
C:\PS>Get-AzureStorageServiceLoggingProperty -ServiceType Blob
```

Эта команда получает свойства ведения журнала для хранилища BLOB-объектов.

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

### -ServiceType
Указывает тип службы хранилища.
Этот командлет получает свойства ведения журнала для типа службы, которое указывает этот параметр.
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

[Set-AzureStorageServiceLoggingProperty](./Set-AzureStorageServiceLoggingProperty.md)


