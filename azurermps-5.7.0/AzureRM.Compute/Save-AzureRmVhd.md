---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 18E1AD70-42A6-47A2-A685-6E218B6DC4BE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVhd.md
ms.openlocfilehash: b428ec98090c0fdd2d6b12bf7dfa06e833b58d42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732870"
---
# Save-AzureRmVhd

## КРАТКИй обзор
Сохранение скачанных VHD-изображений на локальном компьютере.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### ResourceGroupParameterSetName
```
Save-AzureRmVhd [-ResourceGroupName] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [<CommonParameters>]
```

### StorageKeyParameterSetName
```
Save-AzureRmVhd [-StorageKey] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Save-AzureRmVhd** сохраняет файлы. VHD из большого двоичного объекта, в котором они хранятся в файле.
Вы можете указать количество потоков загрузчика, используемых процессом, и определить, следует ли заменять уже существующий файл.

Этот командлет загружает содержимое в том виде, в котором оно установлено.
Преобразование форматов виртуальных жестких дисков (VHD) не применяется.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Загрузка изображения
```
PS C:\> Save-AzureRmVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

Эта команда загружает VHD-файл и сохраняет его в локальном пути. C:\vhd\Win7Image.vhd.

### Пример 2: скачивание изображения и перезапись локального файла
```
PS C:\> Save-AzureRmVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

Эта команда загружает VHD-файл и сохраняет его в локальном пути.
Команда включает параметр *перезаписи* .
Таким образом, если C:\vhd\Win7Image.vhd уже существует, эта команда заменяет ее.

### Пример 3: Загрузка изображения с указанным количеством потоков
```
PS C:\> Save-AzureRmVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32
```

Эта команда загружает VHD-файл и сохраняет его в локальном пути.
Команда задает значение 32 для параметра *NumberOfThreads* .
Таким образом, командлет использует потоки 32 для этого действия.

### Пример 4: Загрузка изображения и указание ключа хранилища
```
PS C:\> Save-AzureRmVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -StorageKey "zNvcH0r5vAGmC5AbwEtpcyWCMyBd3eMDbdaa4ua6kwxq6vTZH3Y+sw=="
```

Эта команда загружает VHD-файл и определяет ключ хранилища.

## ПАРАМЕТРЫ

### -LocalFilePath
Указывает путь к локальному файлу сохраненного изображения.

```yaml
Type: FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NumberOfThreads
Указывает количество потоков скачивания, используемых этим командлетом во время скачивания.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Overwrite
Указывает на то, что этот командлет заменяет файл, указанный в файле *LocalFilePath* , если он существует.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов виртуальной машины.

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SourceUri
Задает универсальный код ресурса (URI) BLOB-объекта в `Azure` .

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: src, Source

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageKey
Указывает ключ хранилища для учетной записи хранения BLOB-объектов.
Если ключ не указан, этот командлет пытается определить ключ хранилища учетной записи в *sourceUri* из Azure.

```yaml
Type: String
Parameter Sets: StorageKeyParameterSetName
Aliases: sk

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего
Этот командлет не поддерживает никаких входных данных.

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Add-AzureRmVhd](./Add-AzureRMVhd.md)


