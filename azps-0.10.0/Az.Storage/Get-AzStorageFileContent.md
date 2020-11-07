---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
ms.openlocfilehash: aa1c7cebbcb6fe24b06638644d19b07c83c2ff04
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910767"
---
# Get-AzStorageFileContent

## КРАТКИй обзор
Загружает содержимое файла.

## Максимальное

### Имя_общего_ресурса (по умолчанию)
```
Get-AzStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Предоставить общий доступ
```
Get-AzStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Папка
```
Get-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Файл
```
Get-AzStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzStorageFileContent** загружает содержимое файла, а затем сохраняет его в указанном месте назначения.
Этот командлет не возвращает содержимое файла.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Загрузка файла из папки
```
PS C:\>Get-AzStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

Эта команда загружает файл с именем CurrentDataFile в папке ContosoWorkingFolder из общей папки ContosoShare06 в текущую папку.

### Пример 2: Загрузка файлов в разделе "пример общего файлового файла"
```
PS C:\>Get-AzStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzStorageFileContent
```

В этом примере загружаются файлы из примера общего файлового файла

## ПАРАМЕТРЫ

### -CheckMd5
Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит содержимое в новом файле.
Если указать путь к уже существующему файлу и задать параметр *Force* , командлет перезапишет файл.
Если вы указали путь к существующему файлу и не указали параметр *Force* , командлет предложит перед продолжением.
Если указать путь к папке, этот командлет попытается создать файл с именем файла хранилища Azure.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientTimeoutPerRequest
Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит содержимое в новом файле.
Если указать путь к уже существующему файлу и задать параметр *Force* , командлет перезапишет файл.
Если вы указали путь к существующему файлу и не указали параметр *Force* , командлет предложит перед продолжением.
Если указать путь к папке, этот командлет попытается создать файл с именем файла хранилища Azure.

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
Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит содержимое в новом файле.
Если указать путь к уже существующему файлу и задать параметр *Force* , командлет перезапишет файл.
Если вы указали путь к существующему файлу и не указали параметр *Force* , командлет предложит перед продолжением.
Если указать путь к папке, этот командлет попытается создать файл с именем файла хранилища Azure.

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
Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит содержимое в новом файле.
Если указать путь к уже существующему файлу и задать параметр *Force* , командлет перезапишет файл.
Если вы указали путь к существующему файлу и не указали параметр *Force* , командлет предложит перед продолжением.
Если указать путь к папке, этот командлет попытается создать файл с именем файла хранилища Azure.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Destination
Указывает конечный путь.
Этот командлет загружает содержимое файлов в расположение, которое указывает этот параметр.
Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит содержимое в новом файле.
Если указать путь к уже существующему файлу и задать параметр *Force* , командлет перезапишет файл.
Если вы указали путь к существующему файлу и не указали параметр *Force* , командлет предложит перед продолжением.
Если указать путь к папке, этот командлет попытается создать файл с именем файла хранилища Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Каталог
Определяет папку как объект **CloudFileDirectory** .
Этот командлет получает содержимое файла в папке, которую указывает этот параметр.
Чтобы получить каталог, используйте командлет New-AzStorageDirectory.
Вы также можете использовать командлет Get-AzStorageFile, чтобы получить каталог.

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

### -Файл
Указывает файл как объект **CloudFile** .
Этот командлет получает файл, который указывает этот параметр.
Чтобы получить объект **CloudFile** , используйте командлет Get-AzStorageFile.

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Force
Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит содержимое в новом файле.
Если указать путь к уже существующему файлу и задать параметр *Force* , командлет перезапишет файл.
Если вы указали путь к существующему файлу и не указали параметр *Force* , командлет предложит перед продолжением.
Если указать путь к папке, этот командлет попытается создать файл с именем файла хранилища Azure.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит содержимое в новом файле.
Если указать путь к уже существующему файлу и задать параметр *Force* , командлет перезапишет файл.
Если вы указали путь к существующему файлу и не указали параметр *Force* , командлет предложит перед продолжением.
Если указать путь к папке, этот командлет попытается создать файл с именем файла хранилища Azure.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Задает путь к файлу.
Этот командлет получает содержимое файла, который указывает этот параметр.
Если файл не существует, этот командлет возвращает ошибку.

```yaml
Type: System.String
Parameter Sets: ShareName, Share, Directory
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит содержимое в новом файле.
Если указать путь к уже существующему файлу и задать параметр *Force* , командлет перезапишет файл.
Если вы указали путь к существующему файлу и не указали параметр *Force* , командлет предложит перед продолжением.
Если указать путь к папке, этот командлет попытается создать файл с именем файла хранилища Azure.

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
Этот командлет загружает содержимое файла в указанном параметре "поделиться".
Чтобы получить объект **CloudFileShare** , используйте командлет Get-AzStorageShare.
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
Этот командлет загружает содержимое файла в указанном параметре "поделиться".

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

### -Confirm
Запрашивает подтверждение перед запуском командлета.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске командлета.
Командлет не выполняется.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## ВХОДНЫЕ данные

### Microsoft. WindowsAz. Storage. File. CloudFileShare
Параметры: Share (ByValue)

### Microsoft. WindowsAz. Storage. File. CloudFileDirectory
Параметры: Каталог (ByValue)

### Microsoft. WindowsAz. Storage. File. CloudFile
Параметры: File (ByValue)

### Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext

## НАПРЯЖЕНИЕ

### Microsoft. WindowsAz. Storage. File. CloudFile

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzStorageFile](./Get-AzStorageFile.md)

[Set-AzStorageFileContent](./Set-AzStorageFileContent.md)


