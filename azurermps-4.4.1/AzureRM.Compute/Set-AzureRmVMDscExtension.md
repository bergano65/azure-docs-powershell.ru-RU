---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 04F58D88-53D6-42CA-852C-9E2A129898C7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMDscExtension.md
ms.openlocfilehash: f041a0b4d07a5123554b3d9b544ea496c87e19ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560460"
---
# Set-AzureRmVMDscExtension

## КРАТКИй обзор
Настраивает расширение DSC на виртуальной машине.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Set-AzureRmVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-ArchiveBlobName] <String> [-ArchiveStorageAccountName] <String> [-ArchiveResourceGroupName <String>]
 [-ArchiveStorageEndpointSuffix <String>] [-ArchiveContainerName <String>] [-ConfigurationName <String>]
 [-ConfigurationArgument <Hashtable>] [-ConfigurationData <String>] [-Version] <String> [-Force]
 [-Location <String>] [-AutoUpdate] [-WmfVersion <String>] [-DataCollection <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzureRmVMDscExtension** настраивает расширение конфигурации Windows POWERSHELL (DSC) на виртуальной машине в группе ресурсов.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Настройка расширения DSC
```
PS C:\> Set-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -Version "1.10" -Location "West US"
```

Эта команда задает расширение DSC на виртуальной машине с именем VM07, чтобы скачать Sample.ps1.zip из учетной записи хранения с именем STG и контейнером по умолчанию.
Команда вызывает конфигурацию с именем ConfigName.
Файл Sample.ps1.zip был ранее загружен с помощью команды **Publish-AzureRmVMDscConfiguration**.

### Пример 2: Настройка расширения DSC с данными конфигурации
```
PS C:\> Set-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM13" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName "WindowsPowerShellDSC" -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US"
```

Эта команда задает расширение на виртуальной машине с именем VM13, чтобы скачать Sample.ps1.zip из учетной записи хранения с именем STG и контейнером с именем WindowsPowerShellDSC.
Команда конфигурации с именем ConfigName и определяет данные конфигурации и аргументы.
Файл Sample.ps1.zip был ранее загружен с помощью команды **Publish-AzureRmVMDscConfiguration**.

### Пример 3: Настройка расширения DSC с данными конфигурации с автоматическим обновлением
```
PS C:\> Set-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM22" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName WindowsPowerShellDSC -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US" -AutoUpdate
```

Эта команда задает расширение на виртуальной машине с именем VM22, чтобы скачать Sample.ps1.zip из учетной записи хранения с именем STG и контейнером с именем WindowsPowerShellDSC.
Эта команда вызывает конфигурацию с именем ConfigName и определяет данные конфигурации и аргументы.
Эта команда также позволяет автоматически обновлять обработчик расширений до последней версии.
Sample.ps1.zip был ранее загружен с помощью команды **Publish-AzureRmVMDscConfiguration**.

## ПАРАМЕТРЫ

### -ArchiveBlobName
Указывает имя файла конфигурации, который ранее был загружен с помощью командлета Publish-AzureRmVMDscConfiguration.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConfigurationArchiveBlob

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ArchiveContainerName
Форель имя контейнера хранилища Azure, в котором находится архив конфигурации.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ArchiveResourceGroupName
Указывает имя группы ресурсов, которая содержит учетную запись хранения, которая содержит архив конфигурации.
Этот параметр необязателен, если учетная запись хранения и виртуальная машина находятся в одной группе ресурсов.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ArchiveStorageAccountName
Указывает имя учетной записи хранения Azure, используемой для загрузки ArchiveBlobName.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ArchiveStorageEndpointSuffix
Указывает суффикс конечной точки хранилища.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Автоматическое обновление
Указывает версию обработчика расширения, заданную параметром *Version* .
По умолчанию обработчик расширений не обновляется.
С помощью параметра "автоматическое *Обновление* " Включите для автоматического обновления обработчика расширений самую последнюю версию и когда она доступна.

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

### -ConfigurationArgument
Указывает хэш-таблицу, которая содержит аргументы для функции конфигурации.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationData
Задает путь к файлу PSD1, который задает данные для конфигурации.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationName
Указывает имя конфигурации, которую вызывает расширение DSC.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Коллекция
Указывает тип сбора данных.
Допустимые значения этого параметра: Включение и отключение.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Force
Принудительное выполнение команды без запроса подтверждения пользователя.

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

### -Location
Указывает путь к расширению ресурса.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (имя)
Указывает имя ресурса диспетчера ресурсов Azure, представляющего расширение.
Значением по умолчанию является Microsoft. PowerShell. DSC.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
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

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Version
Определяет версию расширения DSC, к которой Set-AzureRmVMDscExtension применяются параметры.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Указывает имя виртуальной машины, на которой установлен обработчик расширений DSC.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WmfVersion
Указывает версию WMF.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: 4.0, 5.0, 5.1, latest

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmVMDscExtension](./Get-AzureRmVMDscExtension.md)

[Remove-AzureRmVMDscExtension](./Remove-AzureRmVMDscExtension.md)

[Publish-AzureRmVMDscConfiguration](./Publish-AzureRmVMDscConfiguration.md)


