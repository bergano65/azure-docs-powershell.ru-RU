---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 18E1AD70-42A6-47A2-A685-6E218B6DC4BE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/save-azvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVhd.md
ms.openlocfilehash: 14b0ad981eb44a855f57e6d86df5fd1c03de42e1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519487"
---
# Save-AzVhd

## SYNOPSIS
Сохранение скачаемых VHD-изображений локально.

## СИНТАКСИС

### ResourceGroupParameterSetName
```
Save-AzVhd [-ResourceGroupName] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### StorageKeyParameterSetName
```
Save-AzVhd [-StorageKey] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo> [[-NumberOfThreads] <Int32>]
 [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
При **этом VHD-изображения** сохраняются в BLOB-проекте, в котором они хранятся в файле.
Вы можете указать количество потоков скачивания, которые использует процесс, и указать, следует ли заменить уже существующий файл.
Этот cmdlet скачивает содержимое в том же случае, как есть.
Преобразование формата виртуального жесткого диска (VHD) не применяется.

## ПРИМЕРЫ

### Пример 1. Скачивание изображения
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -ResourceGroupName "rgname"
```

Эта команда скачивает VHD-файл и сохраняет его в локальном пути C:\vhd\Win7Image.vhd.

### Пример 2. Скачивание изображения и переописывание локального файла
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite -ResourceGroupName "rgname"
```

Эта команда скачивает VHD-файл и сохраняет его в локальном пути.
Команда включает параметр *Overwrite.*
Поэтому если C:\vhd\Win7Image.vhd уже существует, эта команда заменяет его.

### Пример 3. Скачивание изображения с использованием заданного количества потоков
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32 -ResourceGroupName "rgname"
```

Эта команда скачивает VHD-файл и сохраняет его в локальном пути.
Команда указывает значение 32 для *параметра NumberOfThreads.*
Таким образом, для этого действия используется 32 потока.

### Пример 4. Скачивание изображения и указание ключа хранилища
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -StorageKey "zNvcH0r5vAGmC5AbwEtpcyWCMyBd3eMDbdaa4ua6kwxq6vTZH3Y+sw==" -ResourceGroupName "rgname"
```

Эта команда скачивает VHD-файл и указывает ключ хранилища.

## PARAMETERS

### -AsJob
Запустите его в фоновом режиме и верните задание для отслеживания хода выполнения.

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

### -LocalFilePath
Путь к локальному файлу сохраненного изображения.

```yaml
Type: System.IO.FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NumberOfThreads
Количество потоков скачивания, которое этот cmdlet использует во время скачивания.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OverWrite
Указывает на то, что этот cmdlet заменяет файл, заданный *файлом LocalFilePath,* если он существует.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов учетной записи хранения.

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SourceUri
Указывает URI URI унифицированного ресурса для BLOB-части. `Azure`

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: src, Source

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageKey
Указывает ключ хранилища для учетной записи хранилища BLOB-хранилищ.
Если ключ не указан, этот cmdlet пытается определить ключ хранилища учетной записи в *SourceUri* из Azure.

```yaml
Type: System.String
Parameter Sets: StorageKeyParameterSetName
Aliases: sk

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

### System.Uri

## OUTPUTS

### Microsoft.Azure.Commands.Compute.Models.VhdDownloadContext

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Add-AzVhd](./Add-AzVhd.md)


