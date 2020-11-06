---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFile.md
ms.openlocfilehash: 5f1834eb603c5023ee49722ee0d7772af40f821c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563219"
---
# Get-AzureStorageFile

## КРАТКИй обзор
Перечисление каталогов и файлов для пути.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### Имя_общего_ресурса (по умолчанию)
```
Get-AzureStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### Предоставить общий доступ
```
Get-AzureStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### Папка
```
Get-AzureStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureStorageFile** выводит список папок и файлов для указанного вами общего доступа или каталога.
Укажите параметр *path* , чтобы получить экземпляр каталога или файла по указанному пути.
Этот командлет возвращает объекты **AzureStorageFile** и **AzureStorageDirectory** .
Вы можете использовать свойство " **подкаталог** " для различения папок и файлов.

## ИЛЛЮСТРИРУЮТ

### Пример 1: список папок в общем доступе
```
PS C:\>Get-AzureStorageFile -ShareName "ContosoShare06" | where {$_.GetType().Name -eq "CloudFileDirectory"}
```

Эта команда выводит список только для каталогов в ContosoShare06 общего доступа.
Сначала она извлекает оба файла и каталоги, передает их оператору **WHERE** с помощью оператора конвейера, а затем удаляет все объекты, тип которых не "CloudFileDirectory".

### Пример 2: список папок с файлами
```
PS C:\> Get-AzureStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzureStorageFile
```

Эта команда выводит список файлов и папок в каталоге ContosoWorkingFolder в разделе Общий доступ ContosoShare06.
Сначала он получает экземпляр службы каталогов, а затем конвейер в командлет **Get-AzureStorageFile для получения** списка каталогов.

## ПАРАМЕТРЫ

### -ClientTimeoutPerRequest
Указывает интервал времени ожидания для одного запроса службы (в секундах).
Если предыдущий вызов завершается сбоем в течение указанного интервала, этот командлет повторно пытается выполнить запрос.
Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.

```yaml
Type: System.Nullable`1[System.Int32]
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
Этот параметр помогает уменьшить число проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.
Значение по умолчанию — 10.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Context
Указывает контекст хранилища Azure.
Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Каталог
Определяет папку как объект **CloudFileDirectory** .
Этот командлет получает папку, указанную в этом параметре.
Чтобы получить каталог, используйте командлет New-AzureStorageDirectory.
Вы также можете использовать командлет **Get-AzureStorageFile** , чтобы получить доступ к каталогу.

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Path
Указывает путь к папке.
Если параметр *путь* не указан, **Get-AzureStorageFile** приводит к перечислению каталогов и файлов в указанной общей папке или в каталоге.
Если вы включаете параметр *path* , функция **Get-AzureStorageFile** возвращает экземпляр каталога или файла в указанном пути.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Задает интервал времени ожидания службы (в секундах) для запроса.
Если заданный интервал проходит до обработки запроса службой, служба хранилища возвращает ошибку.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Общий доступ
Указывает объект **CloudFileShare** .
Этот командлет получает файл или каталог из общей папки, которую указываете этот параметр.
Чтобы получить объект **CloudFileShare** , используйте командлет Get-AzureStorageShare.
Этот объект имеет контекст хранилища.
Если вы задаете этот параметр, не указывайте параметр *контекста* .

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Имя_общего_ресурса
Указывает имя общего файлового файла.
Этот командлет получает файл или каталог из общей папки, которую указываете этот параметр.

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Microsoft. WindowsAzure. Storage. File. CloudFileShare
Параметры: Share (ByValue)

### Microsoft. WindowsAzure. Storage. File. CloudFileDirectory
Параметры: Каталог (ByValue)

### Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext

## НАПРЯЖЕНИЕ

### Microsoft. WindowsAzure. Storage. File. CloudFile

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureStorageFileContent](./Get-AzureStorageFileContent.md)

[New-AzureStorageDirectory](./New-AzureStorageDirectory.md)

[Remove-AzureStorageDirectory](./Remove-AzureStorageDirectory.md)

[Remove-AzureStorageFile](./Remove-AzureStorageFile.md)

[Set-AzureStorageFileContent](./Set-AzureStorageFileContent.md)


