---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: ''
schema: 2.0.0
ms.openlocfilehash: c945838d7d237fb37610d3763525b0ecac838fbb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556260"
---
# Get-AzureStorageFileContent

## КРАТКИй обзор
Загружает содержимое файла.

## Максимальное

### Имя_общего_ресурса (по умолчанию)
```
Get-AzureStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Предоставить общий доступ
```
Get-AzureStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Папка
```
Get-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Файл
```
Get-AzureStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureStorageFileContent** загружает содержимое файла, а затем сохраняет его в указанном месте назначения.
Этот командлет не возвращает содержимое файла.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Загрузка файла из папки
```
PS C:\>Get-AzureStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

Эта команда загружает файл с именем CurrentDataFile в папке ContosoWorkingFolder из общей папки ContosoShare06 в текущую папку.

## ПАРАМЕТРЫ

### -CheckMd5
Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит содержимое в новом файле.
Если указать путь к уже существующему файлу и задать параметр *Force* , командлет перезапишет файл.
Если вы указали путь к существующему файлу и не указали параметр *Force* , командлет предложит перед продолжением.

Если указать путь к папке, этот командлет попытается создать файл с именем файла хранилища Azure.

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

### -ClientTimeoutPerRequest
Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит содержимое в новом файле.
Если указать путь к уже существующему файлу и задать параметр *Force* , командлет перезапишет файл.
Если вы указали путь к существующему файлу и не указали параметр *Force* , командлет предложит перед продолжением.

Если указать путь к папке, этот командлет попытается создать файл с именем файла хранилища Azure.

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
Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит содержимое в новом файле.
Если указать путь к уже существующему файлу и задать параметр *Force* , командлет перезапишет файл.
Если вы указали путь к существующему файлу и не указали параметр *Force* , командлет предложит перед продолжением.

Если указать путь к папке, этот командлет попытается создать файл с именем файла хранилища Azure.

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

### -Context
Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит содержимое в новом файле.
Если указать путь к уже существующему файлу и задать параметр *Force* , командлет перезапишет файл.
Если вы указали путь к существующему файлу и не указали параметр *Force* , командлет предложит перед продолжением.

Если указать путь к папке, этот командлет попытается создать файл с именем файла хранилища Azure.

```yaml
Type: IStorageContext
Parameter Sets: ShareName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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
Type: String
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
Чтобы получить каталог, используйте командлет New-AzureStorageDirectory.
Вы также можете использовать командлет Get-AzureStorageFile, чтобы получить каталог.

```yaml
Type: CloudFileDirectory
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
Чтобы получить объект **CloudFile** , используйте командлет Get-AzureStorageFile.

```yaml
Type: CloudFile
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
Type: SwitchParameter
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
Type: SwitchParameter
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
Type: String
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
Type: Int32
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
Чтобы получить объект **CloudFileShare** , используйте командлет Get-AzureStorageShare.
Этот объект имеет контекст хранилища.
Если вы задаете этот параметр, не указывайте параметр *контекста* .

```yaml
Type: CloudFileShare
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
Type: String
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
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureStorageFile](./Get-AzureStorageFile.md)

[Set-AzureStorageFileContent](./Set-AzureStorageFileContent.md)


