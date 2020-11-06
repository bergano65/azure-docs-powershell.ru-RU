---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9a58f869d5308b176a68614cbb2fa2fec401fa14
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556076"
---
# New-AzureStorageTable

## КРАТКИй обзор
Создание таблицы хранилища.

## Максимальное

```
New-AzureStorageTable [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzureStorageTable** создает таблицу хранилища, связанную с учетной записью хранения в Azure.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание таблицы хранилища Azure
```
PS C:\>New-AzureStorageTable -Name "tableabc"
```

Эта команда создает таблицу хранилища с именем tableabc.

### Пример 2: создание нескольких таблиц хранилища Azure
```
PS C:\>"table1 table2 table3".split() | New-AzureStorageTable
```

Эта команда создает несколько таблиц.
Он использует метод **Split** класса **String** .NET и передает имена в конвейере.

## ПАРАМЕТРЫ

### -Context
Указывает контекст хранилища.
Чтобы создать его, можно использовать командлет New-AzureStorageContext.

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
Задает имя новой таблицы.

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Table

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

[Get-AzureStorageTable](./Get-AzureStorageTable.md)

[Remove-AzureStorageTable](./Remove-AzureStorageTable.md)


