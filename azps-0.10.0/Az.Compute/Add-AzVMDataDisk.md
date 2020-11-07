---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMDataDisk.md
ms.openlocfilehash: 4c7e59b847ec1ae1d95c5a884c8979d12d193084
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910469"
---
# Add-AzVMDataDisk

## КРАТКИй обзор
Добавляет диск с данными на виртуальную машину.

## Максимальное

```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <DiskCreateOptionTypes>
 [[-SourceImageUri] <String>] [[-ManagedDiskId] <String>] [[-StorageAccountType] <StorageAccountTypes>]
 [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Add-AzVMDataDisk** добавляет диск с данными на виртуальную машину.
Вы можете добавить диск с данными при создании виртуальной машины или добавить диск с данными на существующую виртуальную машину.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Добавление дисков с данными на новую виртуальную машину
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

В первой команде создается объект виртуальной машины, который затем сохраняется в переменной $VirtualMachine.
Команда назначает имя и размер виртуальной машине.

Следующие три команды назначают пути к трем дискам с данными в $DataDiskVhdUri 01, $DataDiskVhdUri 02 и $DataDiskVhdUri 03.
Этот подход предназначен для чтения следующих команд.

Последние три команды добавляют диск с данными на виртуальную машину, хранящуюся в $VirtualMachine.
Команда задает имя и расположение диска, а также другие свойства диска.
Универсальный код ресурса (URI) каждого диска хранится в $DataDiskVhdUri 01, $DataDiskVhdUri 02 и $DataDiskVhdUri 03.

### Пример 2: Добавление диска данных к существующей виртуальной машине
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

Первая команда получает виртуальную машину с именем VirtualMachine07 с помощью командлета [Get-AzVM](./Get-AzVM.md) .
Команда сохраняет виртуальную машину в переменной $VirtualMachine.

Вторая команда добавляет диск с данными для виртуальной машины, хранящейся в $VirtualMachine.

Последняя команда обновляет состояние виртуальной машины, сохраненной в $VirtualMachine в ResourceGroup11.

### Пример 3: Добавление диска с данными на новую виртуальную машину из обобщенного пользовательского образа
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

Первая команда создает объект виртуальной машины и сохраняет его в переменной $VirtualMachine.
Команда назначает имя и размер виртуальной машине.

Следующие две команды назначают пути для изображения данных и дисков данных в $DataImageUri и $DataDiskUri переменные соответственно.
Этот подход используется для повышения удобочитаемости следующих команд.

Последние команды добавляют к виртуальной машине диск с данными, хранящийся в $VirtualMachine.
Команда задает имя и расположение диска, а также другие свойства диска.

### Пример 4: Добавление дисков с данными на новую виртуальную машину из специализированного пользовательского образа
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

Первая команда создает объект виртуальной машины и сохраняет его в переменной $VirtualMachine.
Команда назначает имя и размер виртуальной машине.

Следующие команды назначают пути к диску данных переменной $DataDiskUri.
Этот подход используется для повышения удобочитаемости следующих команд.

В последней команде вы можете добавить диск с данными на виртуальную машину, хранящуюся в $VirtualMachine.
Команда задает имя и расположение диска, а также другие свойства диска.

## ПАРАМЕТРЫ

### -Caching
Задает режим кэширования диска.
Для этого параметра допустимы следующие значения:

- Чтения
- Операцию
- Ничего

Значением по умолчанию является ReadWrite.
Изменение этого значения приводит к перезапуску виртуальной машины.

Этот параметр влияет на согласованность и производительность диска.

```yaml
Type: CachingTypes
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
Указывает, создает ли этот командлет диск на виртуальной машине из платформы или пользовательского образа, создает пустой диск или прикрепляет существующий диск.
Для этого параметра допустимы следующие значения:

- Подключает.
Укажите этот параметр, чтобы создать виртуальную машину на основе специализированного диска.
Если вы задаете этот параметр, не указывайте параметр *SourceImageUri* .
*VhdUri* — это все, что необходимо для того, чтобы указать платформе Azure расположение виртуального жесткого диска (VHD) для присоединения в качестве диска данных виртуальной машине.
- Очистку.
Укажите этот объект, чтобы создать пустой диск с данными.
- FromImage.
Укажите этот параметр, чтобы создать виртуальную машину на основе обобщенного образа или диска.
При указании этого параметра необходимо указать параметр *SourceImageUri* , чтобы сообщить платформе Azure о том, что расположение виртуального жесткого диска будет прикрепляться в качестве диска данных.
Параметр *VhdUri* используется в качестве расположения, которое определяет, где будет храниться диск данных, когда он используется виртуальной машиной.

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: True
Position: 6
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

### -DiskSizeInGB
Задает размер пустого диска (в гигабайтах), который нужно прикрепить к виртуальной машине.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LUN
Задает логический номер устройства (LUN) для диска с данными.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ManagedDiskId
Указывает идентификатор управляемого диска.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (имя)
Указывает имя диска данных, который нужно добавить.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SourceImageUri
Указывает URI источника диска, к которому прикрепляется этот командлет.

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourceImage

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountType
Указывает тип учетной записи хранения для управляемого диска.

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VhdUri
Задает универсальный код ресурса (URI) для файла виртуального жесткого диска (VHD), который будет создан при использовании образа платформы или пользовательского образа.
Этот командлет копирует большой двоичный объект изображения (BLOB) в это расположение.
Это место, с которого запускается виртуальная машина.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Указывает локальный объект виртуальной машины, к которому нужно добавить диск с данными.
Вы можете использовать командлет **Get-AzVM** для получения объекта виртуальной машины.
Вы можете использовать командлет **New-AzVMConfig** для создания объекта виртуальной машины.

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -WriteAccelerator
Указывает, следует ли включить или отключить WriteAccelerator на диске с данными.

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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### PSVirtualMachine
Параметр VM принимает значение типа "PSVirtualMachine" из конвейера.

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Remove-AzVMDataDisk](./Remove-AzVMDataDisk.md)

[Get-AzVM](./Get-AzVM.md)

[New-AzVMConfig](./New-AzVMConfig.md)
