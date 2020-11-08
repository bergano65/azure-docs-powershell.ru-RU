---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobrangetorestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
ms.openlocfilehash: cfbe2cc695ceb2db7c498e8ee2750fa0427da114
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243799"
---
# New-AzStorageBlobRangeToRestore

## КРАТКИй обзор
Создает объект диапазона BLOB-объектов для восстановления учетной записи хранения.

## Максимальное

```
New-AzStorageBlobRangeToRestore [-StartRange <String>] [-EndRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzStorageBlobRangeToRestore** создает объект диапазона BLOB, который можно использовать в Restore-AzStorageBlobRange.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Создание диапазона больших двоичных объектов для восстановления
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
```

Эта команда создает диапазон больших двоичных объектов для восстановления, который начинается с container1/blob1 (include) и заканчивается на container2/blob2 (исключить).

### Пример 2: создает диапазон BLOB-объектов, который будет восстанавливаться из первого большого двоичного объекта в алфавитном порядке, в определенный блоб (исключить).
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange container2/blob2
```

Эта команда создает диапазон BLOB-объектов, который будет восстанавливаться из первого большого двоичного файла в алфавитном порядке, в определенный блоб container2/blob2 (исключить).

### Пример 3: создает диапазон BLOB-объектов, который будет восстанавливаться с определенного большого двоичного объекта (include) до последнего BLOB в алфавитном порядке.
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange ""
```

Эта команда создает диапазон больших двоичных объектов, который будет восстанавливаться с определенного блоба container1/blob1 (include) до последнего BLOB в алфавитном порядке.

### Пример 4: Создание диапазона BLOB-объектов, в котором будут восстановлены все большие двоичные объекты
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange ""
```

Эта команда создает диапазон BLOB-объектов, который восстанавливает все большие двоичные объекты.

## ПАРАМЕТРЫ

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndRange
Укажите конечный диапазон для восстановления BLOB-объектов.
Конечный диапазон будет исключен из восстановления больших двоичных объектов.
Установите для него пустое strng, чтобы вернуться к концу.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartRange
Укажите диапазон начала восстановления BLOB-объектов.
Начальный диапазон будет включен в восстановление больших двоичных объектов.
Установите для него пустую строку, чтобы восстановить ее с начала.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Management. Storage. Models. PSBlobRestoreRange

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
