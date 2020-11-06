---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 18E1AD70-42A6-47A2-A685-6E218B6DC4BE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/save-azurermvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Save-AzureRmVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Save-AzureRmVhd.md
ms.openlocfilehash: db2148be139130f5963214c5e66809a3e66a22ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566540"
---
# Save-AzureRmVhd

## КРАТКИй обзор
Сохранение скачанных VHD-изображений на локальном компьютере.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### ResourceGroupParameterSetName
```
Save-AzureRmVhd [-ResourceGroupName] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### StorageKeyParameterSetName
```
Save-AzureRmVhd [-StorageKey] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Save-AzureRmVhd** сохраняет файлы. VHD из большого двоичного объекта, в котором они хранятся в файле.
Вы можете указать количество потоков загрузчика, используемых процессом, и определить, следует ли заменять уже существующий файл.
Этот командлет загружает содержимое в том виде, в котором оно установлено.
Преобразование форматов виртуальных жестких дисков (VHD) не применяется.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Загрузка изображения
```
PS C:\> Save-AzureRmVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -ResourceGroupName "rgname"
```

Эта команда загружает VHD-файл и сохраняет его в локальном пути. C:\vhd\Win7Image.vhd.

### Пример 2: скачивание изображения и перезапись локального файла
```
PS C:\> Save-AzureRmVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite -ResourceGroupName "rgname"
```

Эта команда загружает VHD-файл и сохраняет его в локальном пути.
Команда включает параметр *перезаписи* .
Таким образом, если C:\vhd\Win7Image.vhd уже существует, эта команда заменяет ее.

### Пример 3: Загрузка изображения с указанным количеством потоков
```
PS C:\> Save-AzureRmVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32 -ResourceGroupName "rgname"
```

Эта команда загружает VHD-файл и сохраняет его в локальном пути.
Команда задает значение 32 для параметра *NumberOfThreads* .
Таким образом, командлет использует потоки 32 для этого действия.

### Пример 4: Загрузка изображения и указание ключа хранилища
```
PS C:\> Save-AzureRmVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -StorageKey "zNvcH0r5vAGmC5AbwEtpcyWCMyBd3eMDbdaa4ua6kwxq6vTZH3Y+sw==" -ResourceGroupName "rgname"
```

Эта команда загружает VHD-файл и определяет ключ хранилища.

## ПАРАМЕТРЫ

### -AsJob
Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LocalFilePath
Указывает путь к локальному файлу сохраненного изображения.

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
Указывает количество потоков скачивания, используемых этим командлетом во время скачивания.

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

### -Overwrite
Указывает на то, что этот командлет заменяет файл, указанный в файле *LocalFilePath* , если он существует.

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
Указывает имя группы ресурсов для учетной записи хранения.

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
Задает универсальный код ресурса (URI) BLOB-объекта в `Azure` .

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
Указывает ключ хранилища для учетной записи хранения BLOB-объектов.
Если ключ не указан, этот командлет пытается определить ключ хранилища учетной записи в *sourceUri* из Azure.

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String

### System. URI

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. COMPUTE. Models. VhdDownloadContext

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Add-AzureRmVhd](./Add-AzureRMVhd.md)


