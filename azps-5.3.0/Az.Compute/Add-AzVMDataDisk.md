---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
ms.openlocfilehash: 29233b0bdce273205acffcb87dbf3a8adb1d4a52
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519662"
---
# Add-AzVMDataDisk

## SYNOPSIS
Добавляет диск данных на виртуальную машину.

## СИНТАКСИС

### VmNormalDiskParameterSetName (по умолчанию)
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-SourceImageUri] <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### VmManagedDiskParameterSetName
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-ManagedDiskId] <String>]
 [[-StorageAccountType] <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
**Cmdlet Add-AzVMDataDisk** добавляет диск данных на виртуальную машину.
Диск данных можно добавить при создании виртуальной машины или на существующую виртуальную машину.

## ПРИМЕРЫ

### Пример 1. Добавление дисков данных на новую виртуальную машину
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

Первая команда создает объект виртуальной машины, а затем сохраняет его в $VirtualMachine переменной.
Эта команда назначает имя и размер виртуальной машине.
Следующие три команды назначают пути из трех дисков данных переменным $DataDiskVhdUri 01, $DataDiskVhdUri 02 и $DataDiskVhdUri 03.
Этот подход подходит только для учитаемости следующих команд:
Последние три команды добавляют диск данных на виртуальную машину, храняную в $VirtualMachine.
Команда определяет имя и расположение диска, а также другие свойства диска.
URI каждого диска хранится в $DataDiskVhdUri 01, $DataDiskVhdUri 02 и $DataDiskVhdUri 03.

### Пример 2. Добавление диска данных в существующую виртуальную машину
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

Первая команда получает виртуальную машину с именем VirtualMachine07 с помощью [командлета Get-AzVM.](./Get-AzVM.md)
Эта команда сохраняет виртуальную машину в переменной $VirtualMachine.
Вторая команда добавляет диск данных на виртуальную машину, которая хранится в $VirtualMachine.
Последняя команда обновляет состояние виртуальной машины, которая хранится в $VirtualMachine ResourceGroup11.

### Пример 3. Добавление диска данных на новую виртуальную машину из обобщенного изображения пользователя
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

Первая команда создает объект виртуальной машины и сохраняет его в $VirtualMachine переменной.
Эта команда назначает имя и размер виртуальной машине.
Следующие две команды назначают пути к изображению данных и дискам данных переменным $DataImageUri и $DataDiskUri данных соответственно.
Этот подход используется для повышения учитаемости следующих команд:
Полученные команды добавляют диск данных на виртуальную машину, храняную в $VirtualMachine.
Команда определяет имя и расположение диска, а также другие свойства диска.

### Пример 4. Добавление дисков данных на новую виртуальную машину с специализированного изображения пользователя
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

Первая команда создает объект виртуальной машины и сохраняет его в $VirtualMachine переменной.
Эта команда назначает имя и размер виртуальной машине.
Следующая команда назначает пути диска данных переменной $DataDiskUri данных.
Этот подход используется для повышения учитаемости следующих команд:
Конечная команда добавляет диск данных на виртуальную машину, храняную в $VirtualMachine.
Команда определяет имя и расположение диска, а также другие свойства диска.

## PARAMETERS

### -Кэшинг
Определяет режим кэшации диска.
Допустимые значения этого параметра:
- ReadOnly
- ReadWrite
- По умолчанию значение "ReadWrite" отсутствует.
Изменение этого значения приводит к перезапуску виртуальной машины.
Этот параметр влияет на согласованность и производительность диска.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CreateOption
Определяет, создает ли этот cmdlet диск в виртуальной машине из платформы или изображения пользователя, создает пустой диск или влог существующий диск.
Допустимые значения этого параметра:
- Вложите.
Укажите этот параметр, чтобы создать виртуальную машину на специализированном диске.
При указании этого параметра не укажите параметр *SourceImageUri.*
Для *того* чтобы указать платформе Azure расположение виртуального жесткого диска (VHD), который нужно прикрепить в качестве диска данных к виртуальной машине, достаточно знать VHDUri.
- "Пустая".
Укажите это, чтобы создать пустой диск данных.
- FromImage.
Укажите этот параметр, чтобы создать виртуальную машину на общем изображении или диске.
При указании этого параметра необходимо также указать параметр *SourceImageUri,* чтобы указать платформе Azure расположение VHD, который нужно прикрепить в качестве диска данных.
Параметр *VhdUri* используется в качестве расположения, определяющих, где будет храниться VHD-диск данных при его использования виртуальной машиной.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
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
Определяет размер в гигабайтах пустого диска, который нужно прикрепить к виртуальной машине.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Lun
Определяет логический номер единицы (LUN) для диска данных.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ManagedDiskId
Определяет ИД управляемого диска.

```yaml
Type: System.String
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Имя добавляемого диска данных.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SourceImageUri
Определяет исходный URI диска, в который вложен этот cmdlet.

```yaml
Type: System.String
Parameter Sets: VmNormalDiskParameterSetName
Aliases: SourceImage

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountType
Определяет тип учетной записи хранения управляемого диска.

```yaml
Type: System.String
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VhdUri
URI указывает URI для виртуального жесткого диска (VHD), который создается при создании изображения платформы или пользователя.
Этот cmdlet копирует изображение двоичного большого объекта (BLOB-объекта) в это расположение.
Это расположение, из которого нужно запустить виртуальную машину.

```yaml
Type: System.String
Parameter Sets: VmNormalDiskParameterSetName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Определяет объект локальной виртуальной машины, к которому нужно добавить диск данных.
Для получения объекта виртуальной машины можно использовать **cmdlet Get-AzVM.**
Для создания объекта виртуальной машины можно использовать **cmdlet New-AzVMConfig.**

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -WriteAccelerator
Указывает, следует ли включить или отключить WriteAccelerator на диске управляемых данных.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VmManagedDiskParameterSetName
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

### Microsoft.Azure.Management.Compute.Models.CachingTypes

### System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## OUTPUTS

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelse

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSetVM

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Remove-AzVMDataDisk](./Remove-AzVMDataDisk.md)

[Get-AzVM](./Get-AzVM.md)

[New-AzVMConfig](./New-AzVMConfig.md)
