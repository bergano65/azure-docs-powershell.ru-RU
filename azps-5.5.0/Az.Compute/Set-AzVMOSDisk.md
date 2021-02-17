---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8F7AF1B8-D769-452C-92CF-4486C3EB894D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOSDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOSDisk.md
ms.openlocfilehash: 66bcaab66f6385bdc9f59233054d90932ac6fa33
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238646"
---
# Set-AzVMOSDisk

## SYNOPSIS
Задает свойства диска операционной системы на виртуальной машине.

## СИНТАКСИС

### DefaultParamSet (по умолчанию)
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WindowsParamSet
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Windows] [-DiskSizeInGB <Int32>]
 [-ManagedDiskId <String>] [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DiffDiskSetting <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WindowsDiskEncryptionParameterSet
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Windows] [-DiskEncryptionKeyUrl] <String>
 [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### LinuxParamSet
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Linux] [-DiskSizeInGB <Int32>]
 [-ManagedDiskId <String>] [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DiffDiskSetting <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### LinuxDiskEncryptionParameterSet
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Linux] [-DiskEncryptionKeyUrl] <String>
 [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
Для свойства диска операционной системы на виртуальной машине задаются свойства диска **Set-AzVMOSDisk.**

## ПРИМЕРЫ

### Пример 1. Настройка свойств на виртуальной машине из изображения платформы
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential) 
PS C:\> $VirtualMachine = Set-AzVMSourceImage -VM $VirtualMachine -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.10" -Version "latest" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption FromImage
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

Первая команда получает набор доступности с именем AvailabilitySet13 в группе ресурсов ResourceGroup11, а затем сохраняет этот объект в переменной $AvailabilitySet ресурса.
Вторая команда создает объект виртуальной машины, а затем сохраняет его в $VirtualMachine переменной.
Эта команда назначает имя и размер виртуальной машине.
Виртуальная машину входит в набор доступности, который хранится в $AvailabilitySet.
Конечная команда задает свойства на виртуальной машине в $VirtualMachine.

### Пример 2. Задает свойства на виртуальной машине на основе изображения пользователя
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential)
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -SourceImageUri "https://mystorageaccount.blob.core.windows.net/vhds/myOSImage.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption fromImage -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

Первая команда получает набор доступности с именем AvailabilitySet13 в группе ресурсов ResourceGroup11 и сохраняет этот объект в $AvailabilitySet переменной.
Вторая команда создает объект виртуальной машины и сохраняет его в переменной $VirtualMachine.
Эта команда назначает имя и размер виртуальной машине.
Виртуальная машину входит в набор доступности, который хранится в $AvailabilitySet.
Конечная команда задает свойства на виртуальной машине в $VirtualMachine.

### Пример 3. Задает свойства на виртуальной машине со специализированным изображением пользователя
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption Attach -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

Первая команда получает набор доступности с именем AvailabilitySet13 в группе ресурсов ResourceGroup11 и сохраняет этот объект в $AvailabilitySet переменной.
Вторая команда создает объект виртуальной машины и сохраняет его в переменной $VirtualMachine.
Эта команда назначает имя и размер виртуальной машине.
Виртуальная машину входит в набор доступности, который хранится в $AvailabilitySet.
Конечная команда задает свойства на виртуальной машине в $VirtualMachine.

### Пример 4. Настройка параметров шифрования диска на диске операционной системы виртуальной машины
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite -Windows -CreateOption "Attach" -DiskEncryptionKeyUrl "https://mytestvault.vault.azure.net/secrets/Test1/514ceb769c984379a7e0230bddaaaaaa" -DiskEncryptionKeyVaultId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myresourcegroup/providers/Microsoft.KeyVault/vaults/mytestvault"
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName " ResourceGroup11"
```

В этом примере за устанавливаются параметры шифрования диска на диске операционной системы виртуальной машины.

## PARAMETERS

### -Кэшинг
Определяет режим кэшации диска операционной системы.
Допустимые значения: 
- ReadOnly
- Значением по умолчанию readWrite является ReadWrite.
Изменение значения кэшинга приводит к перезапуску виртуальной машины.
Этот параметр влияет на производительность диска.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CreateOption
Определяет, создает ли этот cmdlet диск в виртуальной машине из платформы или изображения пользователя либо влог существующий диск.
Допустимые значения: 
- Вложите.
Укажите этот параметр, чтобы создать виртуальную машину на специализированном диске.
При указании этого параметра не укажите параметр *SourceImageUri.*
Вместо этого используйте Set-AzVMSourceImage.
Кроме того, с помощью параметров *Windows* или *Linux* необходимо укаймь платформы Azure тип операционной системы на VHD.
Параметр *VhdUri* достаточно для определения расположения диска для вложения на платформе Azure. 
- FromImage.
Укажите этот параметр, чтобы создать виртуальную машину на платформе или обобщенное изображение пользователя.
В случае обобщенного изображения пользователя необходимо указать параметр *SourceImageUri,* а также параметры *Windows* или *Linux,* чтобы указать платформе Azure расположение и тип VHD-диска операционной системы вместо использования cmdlet **Set-AzVMSourceImage.**
В случае изображения платформы достаточно *параметра VhdUri.* 
- "Пустая".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
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

### -DiffDiskSetting
Определяет различные параметры диска операционной системы.

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

### -DiskEncryptionKeyUrl
Определяет расположение ключа шифрования диска.

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: True
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskEncryptionKeyVaultId
Определяет код ресурса хранилища ключа, содержащего ключ шифрования диска.

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: True
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskEncryptionSetId
Определяет код ресурса для набора шифрования диска, управляемого клиентом.  Эта проверка может быть задана только для управляемого диска.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskSizeInGB
Определяет размер диска операционной системы в ГБ.

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

### -KeyEncryptionKeyUrl
Определяет расположение ключа шифрования.

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyEncryptionKeyVaultId
Определяет код ресурса хранилища ключей, содержащий ключ шифрования.

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Linux
Указывает на то, что операционная система на изображении пользователя — Linux.
Укажите этот параметр для развертывания виртуальной машины на основе изображений пользователя.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LinuxParamSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagedDiskId
Определяет ИД управляемого диска.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Указывает имя диска операционной системы.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: OSDiskName, DiskName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceImageUri
Определяет URI VHD для сценариев использования изображений пользователей.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceImage

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountType
Определяет тип учетной записи хранения управляемого диска.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VhdUri
Указывает URI виртуального жесткого диска (VHD).
Для виртуальной машины на основе изображений этот параметр определяет VHD-файл, который будет создаваться при указании изображения платформы или изображения пользователя.
Это расположение, из которого копируется изображение двоичного большого объекта (BLOB-объекта), чтобы запустить виртуальную машину.
Для сценария загрузки виртуальной машины на диске этот параметр указывает VHD-файл, который используется виртуальной машиной непосредственно для запуска.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: OSDiskVhdUri, DiskVhdUri

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Определяет объект локальной виртуальной машины, для которого нужно настроить свойства диска операционной системы.
Чтобы получить объект виртуальной машины, воспользуйтесь Get-AzVM..

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Windows
Указывает на то, что операционная система на изображении пользователя — Windows.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsParamSet, WindowsDiskEncryptionParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WriteAccelerator
Указывает, следует ли включить или отключить WriteAccelerator на диске ОС.

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

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelse

### System.String

## OUTPUTS

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelse

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzVM](./Get-AzVM.md)

[Get-AzAvailabilitySet](./Get-AzAvailabilitySet.md)

[New-AzVMConfig](./New-AzVMConfig.md)


