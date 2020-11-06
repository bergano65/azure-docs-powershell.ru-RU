---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: CBD157D2-37C5-491F-A806-6B39F1D0415A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3191d7369597fbfb0781b550a57f0032f9aaad4f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556279"
---
# Get-AzureStorageBlobCopyState

## КРАТКИй обзор
Получает состояние копии большого двоичного объекта хранилища Azure.

## Максимальное

### NamePipeline (по умолчанию)
```
Get-AzureStorageBlobCopyState [-Blob] <String> [-Container] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### BlobPipeline
```
Get-AzureStorageBlobCopyState -CloudBlob <CloudBlob> [-WaitForComplete] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### ContainerPipeline
```
Get-AzureStorageBlobCopyState -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureStorageBlobCopyState** получает состояние копии большого двоичного объекта хранилища Azure.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение состояния копии большого двоичного объекта
```
C:\PS>Get-AzureStorageBlobCopyState -Blob "ContosoPlanning2015" -Container "ContosoUploads"
```

Эта команда возвращает состояние копирования большого двоичного объекта с именем ContosoPlanning2015 в контейнере ContosoUploads.

### Пример 2: получение состояния копии для большого двоичного объекта с помощью конвейера
```
C:\PS>Get-AzureStorageBlob -Blob "ContosoPlanning2015" -Container "ContosoUploads" | Get-AzureStorageBlobCopyState
```

Эта команда получает двоичный объект с именем ContosoPlanning2015 в контейнере с именем ContosoUploads с помощью командлета **Get-AzureStorageBlob** , а затем передает результат в текущий командлет с помощью оператора конвейера.
Командлет **Get-AzureStorageBlobCopyState** получает состояние копирования для этого большого двоичного объекта.

### Пример 3: получение состояния копии для большого двоичного объекта в контейнере с помощью конвейера
```
C:\PS>Get-AzureStorageContainer -Name "ContosoUploads" | Get-AzureStorageBlobCopyState -Blob "ContosoPlanning2015"
```

Эта команда получает контейнер с именем с помощью командлета **Get-AzureStorageBlob** , а затем передает результат в текущий командлет.
Командлет **Get-AzureStorageContainer** получает состояние копирования для большого двоичного объекта с именем ContosoPlanning2015 в этом контейнере.

## ПАРАМЕТРЫ

### -BLOB
Указывает имя большого двоичного объекта.
Этот командлет получает состояние операции копирования BLOB-объектов хранилища Azure, которую указывает этот параметр.

```yaml
Type: String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientTimeoutPerRequest
Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.
Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.
Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CloudBlob
Указывает объект **CloudBlob** из библиотеки клиента хранилища Azure.
Чтобы получить объект **CloudBlob** , используйте командлет Get-AzureStorageBlob.

```yaml
Type: CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CloudBlobContainer
Указывает объект **CloudBlobContainer** из библиотеки клиента хранилища Azure.
Этот командлет получает состояние копирования большого двоичного объекта в контейнере, указанном этим параметром.
Чтобы получить объект **CloudBlobContainer** , используйте командлет Get-AzureStorageContainer.

```yaml
Type: CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConcurrentTaskCount
Задает максимальное количество одновременных сетевых вызовов.
Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.
Указанное значение является абсолютным числом и не умножается на количество ядер.
Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.
Значение по умолчанию — 10.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Container
Указывает имя контейнера.
Этот командлет получает состояние копирования для большого двоичного объекта в контейнере, указанном в этом параметре.

```yaml
Type: String
Parameter Sets: NamePipeline
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -ServerTimeoutPerRequest
Указывает интервал времени ожидания службы (в секундах) для запроса.
Если заданный интервал проходит до обработки запроса службой, служба хранилища возвращает ошибку.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WaitForComplete
Указывает на то, что этот командлет ожидает завершения копирования.
Если этот параметр не указан, этот командлет возвращает результат немедленно.

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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

### CopyState

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Start-AzureStorageBlobCopy](./Start-AzureStorageBlobCopy.md)

[Остановить-AzureStorageBlobCopy](./Stop-AzureStorageBlobCopy.md)


