---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchresourcefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
ms.openlocfilehash: 43cbf86ca473b6984ee2190b1d10df61b6d32e64
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248134"
---
# New-AzBatchResourceFile

## КРАТКИй обзор
Создание файла ресурсов для использования `New-AzBatchTask` .

## Максимальное

### HttpUrl (по умолчанию)
```
New-AzBatchResourceFile -HttpUrl <String> -FilePath <String> [-FileMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### StorageContainerUrl
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] [-BlobPrefix <String>]
 -StorageContainerUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AutoStorageContainerName
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] -AutoStorageContainerName <String>
 [-BlobPrefix <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Создание файла ресурсов для использования `New-AzBatchTask` .

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание файла ресурсов на основе URL-адреса HTTP, указывающего на один файл
```
PS C:\> $file = New-AzBatchResourceFile -HttpUrl "https://testacct.blob.core.windows.net/" -FilePath "file1"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

Создает `PSResourceFile` ссылку на URL-адрес HTTP.

### Пример 2: создание файла ресурсов из URL-адреса контейнера хранилища Azure
```
PS C:\> $file = New-AzBatchResourceFile -StorageContainerUrl "https://testacct.blob.core.windows.net/mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

Создает `PSResourceFile` ссылку на URL-адрес контейнера хранилища Azure. Все файлы в контейнере будут загружены в указанную папку.

### Пример 3: создание файла ресурсов из имени контейнера для автоматического хранения
```
PS C:\> $file = New-AzBatchResourceFile -AutoStorageContainerName "mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

Создает `PSResourceFile` ссылку на имя контейнера автоматического хранения. Все файлы в контейнере будут загружены в указанную папку.

## ПАРАМЕТРЫ

### -AutoStorageContainerName
Имя контейнера хранилища в учетной записи автоматического хранения.

```yaml
Type: System.String
Parameter Sets: AutoStorageContainerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BlobPrefix
Получает префикс BLOB-объектов, который будет использоваться при загрузке больших двоичных объектов из контейнера хранилища Azure.
Будут загружены только те BLOB-объекты, имена которых начинаются с указанного префикса.
Этот префикс может быть неполным именем файла или подкаталогом.
Если префикс не указан, будут загружены все файлы в контейнере.

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl, AutoStorageContainerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -FileMode
Получает атрибут режима разрешений для файлов в восьмеричном формате.
Это свойство применимо только в том случае, если файл ресурсов загружен на узел Linux.
Если это свойство не задано для узла Linux, значение по умолчанию — 0770.

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

### -FilePath
Расположение на вычислительном узле, в которое загружаются файлы, относящихся к рабочему каталогу задачи. Если указан параметр HttpUrl, необходимо указать путь к файлу и имя файла, в который будет загружен файл, включая его. В противном случае, если указаны параметры AutoStorageContainerName или StorageContainerUrl, путь является необязательным и является каталогом для загрузки файлов. В том случае, если путь FilePath используется в качестве каталога, все структуры каталогов, уже связанные с введенными данными, будут сохранены в полном виде и добавлены в указанный каталог FilePath. Указанный относительный путь не может прерывать рабочий каталог задачи (например, с помощью "...").

```yaml
Type: System.String
Parameter Sets: HttpUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl, AutoStorageContainerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HttpUrl
URL-адрес файла, который нужно скачать.
Если URL — это хранилище BLOB-объектов Azure, оно должно быть доступно для чтения с помощью анонимного доступа; Это значит, что при загрузке большого двоичного объекта Служба пакетов не предоставляет никаких учетных данных.
Существует два способа получения такого URL-адреса для большого двоичного объекта в хранилище Azure: Включите для него разрешения на чтение на доступ к большому двоичному объекту или установите для него ACL или контейнер, чтобы разрешить общий доступ.

```yaml
Type: System.String
Parameter Sets: HttpUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageContainerUrl
URL-адрес контейнера BLOB в хранилище BLOB-объектов Azure.
Этот URL-адрес должен быть читаемым и доступен для просмотра с использованием анонимного доступа; Это значит, что при загрузке больших двоичных объектов из контейнера служба Batch не предоставляет никаких учетных данных.
Существует два способа получения такого URL-адреса для контейнера в хранилище Azure: Включите на него подпись общего доступа (SAS), предоставляя разрешения на чтение для контейнера, или установите для контейнера ACL разрешение Public Access.

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## ВХОДНЫЕ данные

### Ничего

## НАПРЯЖЕНИЕ

### Microsoft.Azure.Commands.BatCH. Models. PSResourceFile

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[New-AzBatchTask](./New-AzBatchTask.md)