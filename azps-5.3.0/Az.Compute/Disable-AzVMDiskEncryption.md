---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 979E956B-4C74-426E-A617-E50C4EBC8A20
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/disable-azvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
ms.openlocfilehash: 1aad073ebd1f1a5e14abfd728ba6e6266a2d6fb8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519647"
---
# Disable-AzVMDiskEncryption

## SYNOPSIS
Отключает шифрование на виртуальной машине IaaS.

## СИНТАКСИС

```
Disable-AzVMDiskEncryption [-ResourceGroupName] <String> [-VMName] <String> [[-VolumeType] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [-Force] [-DisableAutoUpgradeMinorVersion]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## ОПИСАНИЕ
**Cmdlet Disable-AzVMDiskEncryption** отключает шифрование в инфраструктуре в качестве виртуальной машины (IaaS).
Этот cmdlet поддерживается только на виртуальных машинах Windows, а не на виртуальных машинах Linux.
Этот cmdlet устанавливает расширение на виртуальной машине, чтобы отключить шифрование.
Если параметр *Name* не указан, создается расширение со стандартным именем AzureDiskEncryption для VMs Windows.
Внимание! Этот cmdlet перезагружает виртуальную машину.

## ПРИМЕРЫ

### Пример 1. Отключение шифрования для всех томов на виртуальной машине Windows
```
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName "Group001" -VMName "VM002"
```

Эта команда отключает шифрование для объемов типов виртуальных машин с именем VM002, принадлежащих группе ресурсов Group001.
Так как *параметр VolumeType* не указан, для параметра Cmdlet задано значение All.

### Пример 2. Отключение шифрования для томов данных на виртуальной машине Windows
```
PS C:\> $ResourceGroup = "Group002"
PS C:\> $VMName = "VM004"
PS C:\> $VolumeType = "Data"
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName $ResourceGroup -VMName $VMName -VolumeType $VolumeType
```

Эта команда отключает шифрование для объемов данных типа виртуальной машины с именем VM004, которая принадлежит к группе ресурсов Group002.

## PARAMETERS

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

### -DisableAutoUpgradeMinorVersion
Указывает на то, что этот cmdlet отключает автоматическое обновление незначительных версий расширения.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ExtensionPublisherName
Имя издателя расширения. Укажите этот параметр только для переопределения значения по умолчанию microsoft.Azure.Security.

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

### -ExtensionType
Тип расширения. Укажите этот параметр, чтобы переопречить стандартное значение AzureDiskEncryption для VMs Windows и AzureDiskEncryptionForLinux для VMs для Linux.

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

### -Force
Запуск команды без запроса подтверждения.

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

### -Name
Указывает имя ресурса Azure Resource Manager (ARM), представляюного расширение.
Если этот параметр не указан, этот cmdlet по умолчанию имеет значение AzureDiskEncryption для VMs Windows.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 3
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
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TypeHandlerVersion
Указывает версию расширения шифрования.
Если значение для этого параметра не задано, используется последняя версия расширения.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Указывает имя виртуальной машины, на которую этот cmdlet отключает шифрование.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VolumeType
Определяет тип томов виртуальной машины для выполнения операции шифрования.
На виртуальных машинах Windows допустимые значения: 
- Все
- ОС
- "Данные".
Если значение для этого параметра не задано, по умолчанию будет указано значение "Все".
Отключение шифрования в настоящее время не поддерживается в Linux.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OS, Data, All

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Запрос на подтверждение перед запуском cmdlet.

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
Показывает, что произойдет при запуске cmdlet.
Этот cmdlet не будет выполниться.

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
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

### System.Management.Automation.SwitchParameter

## OUTPUTS

### Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzVMDiskEncryptionStatus](./Get-AzVMDiskEncryptionStatus.md)

[Remove-AzVMDiskEncryptionExtension](./Remove-AzVMDiskEncryptionExtension.md)

[Set-AzVMDiskEncryptionExtension](./Set-AzVMDiskEncryptionExtension.md)


