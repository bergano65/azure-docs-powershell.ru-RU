---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmsshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
ms.openlocfilehash: 4c6d2b3376bb5e92d048db61d68c7cfb1b94ee01
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981112"
---
# Add-AzVMSshPublicKey

## SYNOPSIS
Добавляет общедоступные ключи SSH для виртуальной машины при создании только виртуальной машины.

## СИНТАКСИС

```
Add-AzVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
С **помощью cmdlet Add-AzVMSshPublicKey** можно добавить общедоступные ключи, которые можно использовать для подключения к виртуальной машине Linux через безопасную оболочку (SSH). Этот не может использоваться после создания VM, если вы попытались использовать его после создания VM без Update-AzVM, ошибки не будет, если вы используете команду с Update-AzVM, команда будет иметь ошибку.

## ПРИМЕРЫ

### Пример 1. Добавление открытого ключа на виртуальную машину
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

Первая команда получает виртуальную машину с именем VirtualMachine07 с помощью **командлета Get-AzVM.**
Эта команда сохраняет виртуальную машину в переменной $VirtualMachine.
Вторая команда добавляет открытый ключ к расположению в VirtualMachine07, указанному параметром Path.

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

### -KeyData
Определяет кодику с основанием 64 для открытого ключа.
Вы можете подключиться к виртуальной машине Linux с помощью SSH или ключа, указанного для этого параметра.

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

### -Path
Указывает полный путь к файлу на виртуальной машине, где этот cmdlet хранит общедоступный ключ SSH.
Если файл уже существует, этот cmdlet будет выдан с ключом.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Определяет объект виртуальной машины, который изменяет этот cmdlet.
Чтобы получить объект виртуальной машины, используйте [cmdlet Get-AzVM.](./Get-AzVM.md)
Для создания объекта виртуальной машины можно использовать [cmdlet New-AzVMConfig.](./New-AzVMConfig.md)

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

[New-AzVMConfig](./New-AzVMConfig.md)
