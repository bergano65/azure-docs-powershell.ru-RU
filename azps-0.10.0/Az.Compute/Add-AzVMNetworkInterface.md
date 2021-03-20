---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: BF80D456-DAB1-4B51-B50F-A75C2C66A472
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
ms.openlocfilehash: 1ebaa4d0f6a36b7c0330cc987cd62183298c8d10
ms.sourcegitcommit: 6f0b6059d096600ebff1c8514c35c467d2f482d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/20/2021
ms.locfileid: "104713282"
---
# Add-AzVMNetworkInterface

## SYNOPSIS
Добавляет сетевой интерфейс на виртуальную машину.

## СИНТАКСИС

### GetNicFromNicId (по умолчанию)
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine> [-Id] <String> [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetNicFromNicObject
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine>
 [-NetworkInterface] <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
Командлет **Add-AzVMNetworkInterface** добавляет сетевой интерфейс на виртуальную машину.
Вы можете добавить интерфейс при создании виртуальной машины или его добавлении в существующую виртуальную машину.

## ПРИМЕРЫ

### Пример 1. Добавление сетевого интерфейса на новую виртуальную машину
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
```

Первая команда создает объект виртуальной машины, а затем сохраняет его в $VirtualMachine переменной.
Эта команда назначает имя и размер виртуальной машине.

Вторая команда добавляет сетевой интерфейс к виртуальной машине, которая хранится в $VirtualMachine.

### Пример 2. Добавление сетевого интерфейса к существующей виртуальной машине
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

Первая команда получает виртуальную машину с именем VirtualMachine07 с помощью **командлета Get-AzVM.**
Эта команда сохраняет виртуальную машину в переменной $VirtualMachine.

Вторая команда добавляет сетевой интерфейс к виртуальной машине, которая хранится в $VirtualMachine.

Последняя команда обновляет состояние виртуальной машины, которая хранится в $VirtualMachine ResourceGroup11.

## PARAMETERS

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

### -Id
Определяет ИД сетевого интерфейса, который нужно добавить на виртуальную машину.
Для получения сетевого интерфейса можно использовать командлет [Get-AzNetworkInterface.](/module/az.network/get-aznetworkinterface)

```yaml
Type: String
Parameter Sets: GetNicFromNicId
Aliases: NicId, NetworkInterfaceId

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NetworkInterface
Определяет сетевой интерфейс.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]
Parameter Sets: GetNicFromNicObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Primary
Указывает на то, что этот cmdlet добавляет сетевой интерфейс в качестве основного.

```yaml
Type: SwitchParameter
Parameter Sets: GetNicFromNicId
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Определяет объект локальной виртуальной машины, к которому нужно добавить сетевой интерфейс.
Чтобы создать виртуальную машину, воспользуйтесь **cmdlet New-AzVMConfig.**
Чтобы получить виртуальную машину, воспользуйтесь **cmdlet get-AzVM.**

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

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.Collections.Generic.List'1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterface]
Параметр NetworkInterface принимает значение типа System.Collections.Generic.List'1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterface]" из конвейера.

### PSVirtualMachine
Параметр VM принимает значение типа PSVirtualMa в конвейере

## OUTPUTS

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelse

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[New-AzVMConfig](./New-AzVMConfig.md)

[Get-AzVM](./Get-AzVM.md)

[Get-AzAvailabilitySet](./Get-AzAvailabilitySet.md)
