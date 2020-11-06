---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E54BFD3A-CD54-4E6B-9574-92B8D3E88FF3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlob.md
gitcommit: https://github.com/Azure/azure-powershell/blob/f8503a90f782f51c8baa0360f98adb33f2a6f26f
ms.openlocfilehash: e05dc3ed962e7d1d4610663dd129c0977b784280
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565765"
---
# Get-AzureStorageBlob

## КРАТКИй обзор
Список больших двоичных объектов в контейнере.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### BlobName (по умолчанию)
```
Get-AzureStorageBlob [[-Blob] <String>] [-Container] <String> [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### BlobPrefix
```
Get-AzureStorageBlob [-Prefix <String>] [-Container] <String> [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureStorageBlob** перечисляет большие двоичные объекты в указанном контейнере в учетной записи хранения Azure.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение большого двоичного объекта по имени BLOB-объектов
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Blob blob*
```

Эта команда использует имя большого двоичного объекта и подстановочный знак для получения большого двоичного объекта.

### Пример 2: получение большого двоичного объекта с помощью конвейера
```
PS C:\>Get-AzureStorageContainer -Name container* | Get-AzureStorageBlob
```

Эта команда использует конвейер для получения большого двоичного объекта.

### Пример 3: получение имени большого двоичного объекта с помощью префикса
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Prefix "blob"
```

Эта команда использует префикс имени, чтобы получить большой двоичный объект.

### Пример 4: список больших двоичных объектов в нескольких пакетах
```
PS C:\>$MaxReturn = 10000
PS C:\> $ContainerName = "abc"
PS C:\> $Total = 0
PS C:\> $Token = $Null
PS C:\> do
 {
     $Blobs = Get-AzureStorageBlob -Container $ContainerName -MaxCount $MaxReturn  -ContinuationToken $Token
     $Total += $Blobs.Count
     if($Blobs.Length -le 0) { Break;}
     $Token = $Blobs[$blobs.Count -1].ContinuationToken;
 }
 While ($Token -ne $Null)
PS C:\> Echo "Total $Total blobs in container $ContainerName"
```

В этом примере параметры *maxcount* и *ContinuationToken* используются для перечисления больших двоичных объектов хранилища Azure в нескольких пакетах.
Первые четыре команды назначают значения переменным для использования в примере.

Пятая команда задает оператор **Do-** in, использующий командлет **Get-AzureStorageBlob** для получения больших двоичных объектов.
Оператор включает токен продолжения, хранящийся в переменной $Token.
$Token изменения значения по мере выполнения цикла.
Для получения дополнительных сведений введите `Get-Help About_Do` .

В последней команде используется команда **echo** для отображения итогового значения.

## ПАРАМЕТРЫ

### -BLOB
Указывает имя или шаблон имени, которые можно использовать для поиска с подстановочными знаками.
Если имя BLOB-объектов не указано, командлет выводит список всех больших двоичных объектов в указанном контейнере.
Если для этого параметра задано значение, командлет выводит список всех больших двоичных объектов с именами, которые соответствуют этому параметру.

```yaml
Type: String
Parameter Sets: BlobName
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
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

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Context
Указывает учетную запись хранения Azure, из которой вы хотите получить список больших двоичных объектов.
Вы можете использовать командлет New-AzureStorageContext для создания контекста хранилища.

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

### -ContinuationToken
Указывает маркер продолжения для списка больших двоичных объектов.
Используйте этот параметр и параметр *maxcount* для перечисления BLOB-объектов в нескольких пакетах.

```yaml
Type: BlobContinuationToken
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxCount
Задает максимальное количество объектов, возвращаемых этим командлетом.

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

### -Prefix (префикс)
Задает префикс для имен больших двоичных объектов, которые требуется получить.
Этот параметр не поддерживает использование регулярных выражений и подстановочных знаков для поиска.
Это означает, что если контейнер содержит только большие двоичные объекты с именами "My", "MyBlob1" и "MyBlob2", а вы указали "-prefix My *", командлет не вернет BLOB-объекты.
Тем не менее, если указать "-prefix My", командлет возвращает "My", "MyBlob1" и "MyBlob2".

```yaml
Type: String
Parameter Sets: BlobPrefix
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### IStorageContext

Параметр "Context" принимает значение типа "IStorageContext" из конвейера.

## НАПРЯЖЕНИЕ

### AzureStorageBlob

## Пуск


## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureStorageBlobContent](./Get-AzureStorageBlobContent.md)

[Remove-AzureStorageBlob](./Remove-AzureStorageBlob.md)

[Set-AzureStorageBlobContent](./Set-AzureStorageBlobContent.md)


