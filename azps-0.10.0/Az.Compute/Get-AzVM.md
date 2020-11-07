---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVM.md
ms.openlocfilehash: 2f33b0dbee4f584553eac1047471adef08e3523b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911544"
---
# Get-AzVM

## КРАТКИй обзор
Получает свойства виртуальной машины.

## Максимальное

### ListAllVirtualMachinesParamSet (по умолчанию)
```
Get-AzVM [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ListVirtualMachineInResourceGroupParamSet
```
Get-AzVM [-ResourceGroupName] <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetVirtualMachineInResourceGroupParamSet
```
Get-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ListNextLinkVirtualMachinesParamSet
```
Get-AzVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzVM** получает представление модели и экземпляр для виртуальной машины Azure.
Представление модели — это указанные пользователем свойства виртуальной машины.
Представление экземпляра — это состояние уровня экземпляра виртуальной машины.
Укажите параметр *Status* , чтобы получить только представление экземпляра виртуальной машины.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение свойств модели и представления экземпляров
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

Эта команда получает свойства представления модели и экземпляра виртуальной машины с именем VirtualMachine07.

### Пример 2: получение свойств представления экземпляра
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status
```

Эта команда получает свойства виртуальной машины с именем VirtualMachine07.
Эта команда задает параметр *Status* .
Таким образом, команда возвращает только свойства представления экземпляра.

### Пример 3: получение свойств для всех виртуальных машин в группе ресурсов
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11"
```

Эта команда получает свойства всех виртуальных машин в группе ресурсов с именем ResourceGroup11.

### Пример 4: получение всех виртуальных машин в подписке
```
PS C:\> Get-AzVM
```

Эта команда возвращает все виртуальные машины в вашей подписке.

## ПАРАМЕТРЫ

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

### -DisplayHint
Определяет способ отображения объекта виртуальной машины.

Допустимые значения:

--Компактный: отображаются только свойства верхнего уровня.

--Expand: отображает все свойства на всех уровнях.
```yaml
Type: DisplayHintType
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: 
Accepted values: Compact, Expand

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (имя)
Указывает имя виртуальной машины, которую требуется получить.

```yaml
Type: String
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NextLink
Указывает следующую ссылку.

```yaml
Type: Uri
Parameter Sets: ListNextLinkVirtualMachinesParamSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов.

```yaml
Type: String
Parameter Sets: ListVirtualMachineInResourceGroupParamSet, GetVirtualMachineInResourceGroupParamSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Status (состояние)
Указывает на то, что этот командлет получает только представление экземпляра виртуальной машины.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего
Этот командлет не поддерживает никаких входных данных.

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine

### Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineInstanceView

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[New-AzVM](./New-AzVM.md)

[Remove-AzVM](./Remove-AzVM.md)

[Restarting-AzVM](./Restart-AzVM.md)

[Start-AzVM](./Start-AzVM.md)

[Остановить-AzVM](./Stop-AzVM.md)

[Update-AzVM](./Update-AzVM.md)


