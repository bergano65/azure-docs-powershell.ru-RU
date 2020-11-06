---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f2bccab190fc27b5e97ecf3af502d3488f28998
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556227"
---
# Get-AzureStorageTable

## КРАТКИй обзор
Список таблиц хранилища.

## Максимальное

### TableName (по умолчанию)
```
Get-AzureStorageTable [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### TablePrefix
```
Get-AzureStorageTable -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureStorageTable** перечисляет таблицы хранения, связанные с учетной записью хранения в Azure.

## ИЛЛЮСТРИРУЮТ

### Пример 1: список всех таблиц хранилища Azure
```
PS C:\>Get-AzureStorageTable
```

Эта команда получает все таблицы хранилища для учетной записи хранения.

### Пример 2: список таблиц хранилища Azure с использованием подстановочных знаков
```
PS C:\>Get-AzureStorageTable -Name table*
```

Эта команда использует подстановочный знак для получения таблиц хранилища, имя которых начинается с Table.

### Пример 3: список таблиц хранилища Azure с использованием префикса имени таблицы
```
PS C:\>Get-AzureStorageTable -Prefix "table"
```

Эта команда использует параметр *prefix* для получения таблиц хранилища, имя которых начинается с Table.

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
Указывает имя таблицы.
Если имя таблицы пусто, командлет выводит список всех таблиц.
В противном случае выводится список всех таблиц, соответствующих указанному имени или шаблону обычного имени.

```yaml
Type: String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Prefix (префикс)
Задает префикс, используемый в имени таблицы или таблиц, которые требуется получить.
Вы можете использовать этот параметр, чтобы найти все таблицы, которые начинаются с одной строки, например Table.

```yaml
Type: String
Parameter Sets: TablePrefix
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

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[New-AzureStorageTable](./New-AzureStorageTable.md)

[Remove-AzureStorageTable](./Remove-AzureStorageTable.md)


