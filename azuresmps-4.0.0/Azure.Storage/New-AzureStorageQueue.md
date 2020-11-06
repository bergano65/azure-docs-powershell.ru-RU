---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 76876cb76e65c913401d62fc7f08b3cb8b5626c0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555899"
---
# New-AzureStorageQueue

## КРАТКИй обзор
Создание очереди хранилища.

## Максимальное

```
New-AzureStorageQueue [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzureStorageQueue** создает очередь хранилища в Azure.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание очереди хранилища Azure
```
PS C:\>New-AzureStorageQueue -Name "queueabc"
```

В этом примере создается очередь хранилища с именем queueabc.

### Пример 2: создание нескольких очередей хранилища Azure
```
PS C:\>"queue1 queue2 queue3".split() | New-AzureStorageQueue
```

В этом примере создается несколько очередей хранилища.
Он использует метод Split класса String .NET и передает имена в конвейере.

## ПАРАМЕТРЫ

### -Context
Указывает контекст хранилища Azure.
Вы можете создать его с помощью командлета New-AzureStorageContext.

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

### -Name (имя)
Указывает имя очереди.

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureStorageQueue](./Get-AzureStorageQueue.md)

[Remove-AzureStorageQueue](./Remove-AzureStorageQueue.md)


