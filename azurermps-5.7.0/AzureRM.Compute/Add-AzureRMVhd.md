---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D08DAA8B-B7BF-4167-AB16-F2723985A0B7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRMVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRMVhd.md
ms.openlocfilehash: 7faa179ae8c8c43d750e4f042f7bc925b772f4e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563728"
---
# Add-AzureRmVhd

## КРАТКИй обзор
Передача виртуального жесткого диска из локальной виртуальной машины в большой двоичный объект в учетной записи облачного хранилища в Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Add-AzureRmVhd [[-ResourceGroupName] <String>] [-Destination] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfUploaderThreads] <Int32>] [[-BaseImageUriToPatch] <Uri>] [-OverWrite] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Add-AzureRmVhd** отправляет локальные виртуальные жесткие диски в формате VHD в учетную запись хранения BLOB как фиксированные виртуальные жесткие диски.
Вы можете настроить количество потоков передачи данных, которые будут использоваться, или перезаписать существующий BLOB-объект в указанном URI назначения.
Кроме того, поддерживается возможность отправки исправленной версии локального файла VHD.
После отправки базового виртуального жесткого диска вы можете отправлять разностные диски, в которых в качестве родительских используются базовые образы.
URI-адрес подписи общего доступа (SAS) также поддерживается.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Добавление VHD-файла
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

Эта команда добавляет VHD-файл в учетную запись хранения.

### Пример 2: Добавление файла виртуального жесткого диска и переопределение места назначения
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

Эта команда добавляет VHD-файл в учетную запись хранения.
Команда перезапишет существующий файл.

### Пример 3: Добавление файла виртуального жесткого диска и указание количества потоков
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfUploaderThreads 32
```

Эта команда добавляет VHD-файл в учетную запись хранения.
Команда задает количество потоков, используемых для отправки файла.

### Пример 4: Добавление файла виртуального жесткого диска и указание URI SAS
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01 -09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveO SIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

Эта команда добавляет VHD-файл в учетную запись хранения и определяет универсальный код ресурса (URI) SAS.

## ПАРАМЕТРЫ

### -BaseImageUriToPatch
Задает универсальный код ресурса (URI) базового изображения в хранилище BLOB-объектов Azure.
В качестве значения этого параметра можно указать SAS.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: bs

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Destination
Задает универсальный код ресурса (URI) большого двоичного объекта в хранилище BLOB-объектов.
Параметр поддерживает URI SAS, хотя назначение сценариев для установки не может быть URI SAS.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: dst

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LocalFilePath
Задает путь к локальному VHD-файлу.

```yaml
Type: FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NumberOfUploaderThreads
Указывает количество потоков данных, которые будут использоваться при загрузке VHD-файла.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Overwrite
Указывает на то, что этот командлет перезаписывает существующий большой двоичный объект в указанном URI назначения, если он существует.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов виртуальной машины.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
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

[Сохранить — AzureRmVhd](./Save-AzureRmVhd.md)


