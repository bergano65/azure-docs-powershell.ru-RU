---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D08DAA8B-B7BF-4167-AB16-F2723985A0B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVhd.md
ms.openlocfilehash: d0031ad2a6b4c38937e7faaf0743d6181608ff15
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519670"
---
# Add-AzVhd

## SYNOPSIS
Отправка виртуального жесткого диска с локальной виртуальной машины в большой объект в учетной записи облачного хранилища в Azure.

## СИНТАКСИС

```
Add-AzVhd [[-ResourceGroupName] <String>] [-Destination] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfUploaderThreads] <Int32>] [[-BaseImageUriToPatch] <Uri>] [-OverWrite] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
Для отправки локального виртуального жесткого диска (в формате VHD) в учетную запись хранилища **BLOB-файлов** в качестве фиксированных виртуальных жестких дисков.
Вы можете настроить количество потоков отправки, которые будут использоваться, или переписать существующий BLOB-проект в указанном URI назначения.
Кроме того, поддерживается возможность отправки исправленной версии локального VHD-файла.
Если базовый виртуальный жесткий диск уже загружен, вы можете загружать разные диски, в качестве родительского на которые используется базовое изображение.
Также поддерживается URI подписи общего доступа (SAS).

## ПРИМЕРЫ

### Пример 1. Добавление VHD-файла
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

Эта команда добавляет VHD-файл в учетную запись хранения.

### Пример 2. Добавление VHD-файла и переописывание назначения
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

Эта команда добавляет VHD-файл в учетную запись хранения.
Команда перепишет существующий файл.

### Пример 3. Добавление VHD-файла и указание количества потоков
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfUploaderThreads 32
```

Эта команда добавляет VHD-файл в учетную запись хранения.
Команда определяет количество потоков, которые нужно использовать для отправки файла.

### Пример 4. Добавление VHD-файла и указание URI SAS
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01 -09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveO SIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

Эта команда добавляет VHD-файл в учетную запись хранения и указывает URI SAS.

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

### -BaseImageUriToPatch
Определяет URI для базового BLOB-адреса изображения в хранилище BLOB-устройств Azure.
В качестве значения этого параметра можно у указывает SAS.

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: bs

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Destination
Определяет URI BLOB-части в хранилище BLOB-хранилищ.
Параметр поддерживает URI SAS, хотя назначением сценариев исправления не может быть URI SAS.

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: dst

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LocalFilePath
Путь к локальному VHD-файлу.

```yaml
Type: System.IO.FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NumberOfUploaderThreads
Количество потоков отправки, которые будут использоваться при отправке VHD-файла.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OverWrite
Указывает на то, что этот cmdlet переопишет существующий BLOB-проект в указанном URI назначения, если он существует.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

### System.Uri

### System.IO.FileInfo

### System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.Management.Automation.SwitchParameter

## OUTPUTS

### Microsoft.Azure.Commands.Compute.Models.VhdUploadContext

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Save-AzVhd](./Save-AzVhd.md)


