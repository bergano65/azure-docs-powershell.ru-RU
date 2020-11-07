---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: FB9ACBA2-081E-4876-A21A-F5BA11CBEDA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/publish-azvmdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
ms.openlocfilehash: d099feea5efe52d8bcc6a0067550a7c4ae9bbc3a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911441"
---
# Publish-AzVMDscConfiguration

## КРАТКИй обзор
Передает сценарий DSC в хранилище BLOB-объектов Azure.

## Максимальное

### UploadArchive (по умолчанию)
```
Publish-AzVMDscConfiguration [-ResourceGroupName] <String> [-ConfigurationPath] <String>
 [[-ContainerName] <String>] [-StorageAccountName] <String> [-StorageEndpointSuffix <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### CreateArchive
```
Publish-AzVMDscConfiguration [-ConfigurationPath] <String> [[-OutputArchivePath] <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Publish-AzVMDscConfiguration** передает в хранилище больших двоичных объектов Azure сценарий Desired State Configuration (DSC), который позже можно применить к виртуальным машинам Azure с помощью командлета Set-AzVMDscExtension.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание ZIP-пакета для отправки в хранилище Azure
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1"
```

Эта команда создает ZIP-пакет для указанного сценария и зависимых модулей ресурсов и отправляет его в хранилище Azure.

### Пример 2: создание ZIP-пакета и сохранение его в локальном файле
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1" -OutputArchivePath ".\MyConfiguration.ps1.zip"
```

Эта команда создает ZIP-пакет для указанного сценария и зависимых от него модулей ресурсов и сохраняет его в локальном файле с именем .\MyConfiguration.ps1.zip.

### Пример 3: Добавление конфигурации в архив, а затем его отправка в хранилище
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -SkipDependencyDetection
```

Эта команда добавляет конфигурацию с именем Sample.ps1 в архив конфигурации для отправки в хранилище Azure и пропускает зависимые модули ресурсов.

### Пример 4: Добавление данных конфигурации и конфигурации в архив, а затем их отправка в хранилище
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -ConfigurationDataPath "C:\SampleData.psd1"
```

Эта команда добавляет конфигурацию с именем Sample.ps1 и данными конфигурации с именем SampleData.psd1 в архив конфигурации для отправки в хранилище Azure.

### Пример 5: Добавление конфигурации, данных конфигурации и дополнительного содержимого в архив, а затем его отправка в хранилище
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -AdditionalPath @("C:\ContentDir1", "C:\File.txt") -ConfigurationDataPath "C:\SampleData.psd1"
```

Эта команда добавляет конфигурацию с именем Sample.ps1, данными конфигурации SampleData.psd1 и дополнительным содержимым в архив конфигурации для отправки в хранилище Azure.

## ПАРАМЕТРЫ

### -AdditionalPath
Задает путь к файлу или папке, которые нужно включить в архив конфигурации.
Оно будет загружено на виртуальную машину вместе с конфигурацией.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationDataPath
Задает путь к файлу PSD1, который задает данные для конфигурации.
Она будет добавлена в архив конфигурации, а затем передана в функцию конфигурации.
Он перезаписывается путем данных конфигурации, предоставленным с помощью командлета Set-AzVMDscExtension

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationPath
Задает путь к файлу, содержащему одну или несколько конфигураций.
Файл может быть файлом сценария Windows PowerShell (PS1) или файлом модуля Windows PowerShell (. PSM1).

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ContainerName
Указывает имя контейнера хранилища Azure, в который загружается конфигурация.

```yaml
Type: String
Parameter Sets: UploadArchive
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Принудительное выполнение команды без запроса подтверждения пользователя.

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

### -OutputArchivePath
Задает путь к локальному ZIP-файлу для записи архива конфигурации.
При использовании этого параметра сценарий конфигурации не загружается в хранилище BLOB-объектов Azure.

```yaml
Type: String
Parameter Sets: CreateArchive
Aliases: ConfigurationArchivePath

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов, которая содержит учетную запись хранения.

```yaml
Type: String
Parameter Sets: UploadArchive
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkipDependencyDetection
Указывает на то, что этот командлет исключает зависимости ресурса DSC из архива конфигурации.

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

### -StorageAccountName
Указывает имя учетной записи хранения Azure, используемой для передачи сценария конфигурации в контейнер, указанный в параметре *ContainerName* .

```yaml
Type: String
Parameter Sets: UploadArchive
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageEndpointSuffix
Указывает суффикс для конечной точки хранилища.

```yaml
Type: String
Parameter Sets: UploadArchive
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Подстрок
Параметр "ConfigurationPath" принимает значение типа String из конвейера.

## НАПРЯЖЕНИЕ

### System. String

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzVMDscExtension](./Get-AzVMDscExtension.md)

[Remove-AzVMDscExtension](./Remove-AzVMDscExtension.md)

[Set-AzVMDscExtension](./Set-AzVMDscExtension.md)


