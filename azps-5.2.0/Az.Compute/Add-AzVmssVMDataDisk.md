---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
ms.openlocfilehash: 5e7901f3e2d18b0707ccf9c5f62f9ab55789a45e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416516"
---
# Add-AzVmssVMDataDisk

## SYNOPSIS
Добавляет диск данных в VMSs VM.

## СИНТАКСИС

```
Add-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-CreateOption] <String> [-ManagedDiskId] <String> [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-Caching <CachingTypes>] [-DiskSizeInGB <Int32>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
**Cmdlet Add-AzVmssVMDataDisk** добавляет диск данных в VMSs VM.

## ПРИМЕРЫ

### Пример 1. Добавление диска управляемых данных в VMSS-модем.
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVmssVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

Первая команда получает существующий управляемый диск.
Следующая команда получает существующий VMS-проект, который задается именем группы ресурсов, именем вим-замы и именем экземпляра.
Следующая команда добавляет управляемый диск в VMSs VM, которые хранятся в $VmssVM.
Конечная команда обновляет VMSs VM с добавленным диском данных.

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
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CreateOption
Указывает, создает ли этот cmdlet диск в виртуальной машине из платформы или изображения пользователя, создает пустой диск или влог существующий диск.
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
Параметр *VhdUri* используется в качестве расположения, определяющих, где будет храниться VHD-диск данных при его использовании виртуальной машиной.

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
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Lun
Определяет логический номер единицы (LUN) для диска данных.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ManagedDiskId
Определяет ИД управляемого диска.

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

### -StorageAccountType
Определяет тип учетной записи хранения управляемого диска.

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

### -VirtualMachineScaleSetVM
Определяет локальный масштаб виртуальной машины, для которого нужно добавить диск данных.
Для получения объекта VM-объекта в масштабе виртуальной машины можно использовать **cmdlet Get-AzVmssVM.**

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WriteAccelerator
Указывает, следует ли включить или отключить WriteAccelerator на диске управляемых данных.

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

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSetVM

### System.Int32

### System.String

### Microsoft.Azure.Management.Compute.Models.CachingTypes

## OUTPUTS

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSetVM

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ
