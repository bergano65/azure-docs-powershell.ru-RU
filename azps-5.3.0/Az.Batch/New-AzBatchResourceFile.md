---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchresourcefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
ms.openlocfilehash: 43cbf86ca473b6984ee2190b1d10df61b6d32e64
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509629"
---
# New-AzBatchResourceFile

## SYNOPSIS
Создает файл ресурса для использования `New-AzBatchTask` по.

## СИНТАКСИС

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

## ОПИСАНИЕ
Создает файл ресурса для использования `New-AzBatchTask` по.

## ПРИМЕРЫ

### Пример 1. Создание файла ресурса из URL-адреса HTTP, указываного на один файл
```
PS C:\> $file = New-AzBatchResourceFile -HttpUrl "https://testacct.blob.core.windows.net/" -FilePath "file1"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

Создание `PSResourceFile` ССЫЛКи на HTTP-URL-адрес.

### Пример 2. Создание файла ресурса на url-адресе контейнера хранилища Azure
```
PS C:\> $file = New-AzBatchResourceFile -StorageContainerUrl "https://testacct.blob.core.windows.net/mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

Создает URL-адрес контейнера хранилища `PSResourceFile` Azure. Все файлы в контейнере будут загружены в указанную папку.

### Пример 3. Создание файла ресурса с именем контейнера автосъемки
```
PS C:\> $file = New-AzBatchResourceFile -AutoStorageContainerName "mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

Создание имени контейнера для `PSResourceFile` автосхранилища. Все файлы в контейнере будут загружены в указанную папку.

## PARAMETERS

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
Получает префикс BLOB-то, который будет использовать при скачии BLOB-людей из контейнера хранилища Azure.
Будут скачины только те BLOB-lob, имена которых начинаются с указанного префикса.
Этот префикс может быть частью имени файла или поднаправлением.
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
Возвращает атрибут режима разрешений файла в восьмеся бытовом формате.
Это свойство применимо только в том случае, если файл ресурса загружается на узел Linux.
Если это свойство не задано для узла Linux, по умолчанию задано значение 0770.

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
Расположение на узле вычислений, в которое нужно скачать файлы, относительно рабочего каталога задачи. Если задан параметр HttpUrl, то параметр FilePath является required и описывает путь, в который нужно скачать файл, включая имя файла. В противном случае, если заданы параметры AutoStorageContainerName или StorageContainerUrl, FilePath является необязательным и является каталогом, в который нужно скачать файлы. В случае использования FilePath в качестве каталога любая структура каталога, уже связанная с входными данными, сохраняется полностью и ее можно будет ввести в указанный каталог FilePath. Указанный относительный путь не может выйти из рабочего каталога задачи (например, с помощью ".").

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
URL-адрес скачиваемого файла.
Если URL-адрес — хранилище BLOB-адресов Azure, он должен быть прочитан с помощью анонимного доступа. то есть пакетная служба не может скачать BLOB-файл с учетными данными.
Получить такой URL-адрес для BLOB-сайта в хранилище Azure можно двумя способами: включив подпись общего доступа (SAS), которая предоставляет разрешения на чтение для этого BLOB-сайта, или задайте ACL для BLOB-сайта или контейнера, чтобы разрешить общий доступ.

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
URL-адрес контейнера BLOB-lob в хранилище BLOB-хранилищ Azure.
Этот URL-адрес должен быть доступны для чтения и списка с использованием анонимного доступа; то есть пакетная служба не имеет учетных данных при скачии BLOB-людей из контейнера.
Получить такой URL-адрес для контейнера в хранилище Azure можно двумя способами: с использованием подписи SAS, которая предоставляет разрешения на чтение контейнера, или установить для него разрешение на общедоступный доступ.

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
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Нет

## OUTPUTS

### Microsoft.Azure.Commands.Batch. Models.PSResourceFile

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[New-AzBatchTask](./New-AzBatchTask.md)