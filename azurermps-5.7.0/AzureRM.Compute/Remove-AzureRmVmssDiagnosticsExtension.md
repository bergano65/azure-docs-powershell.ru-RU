---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 5F135E64-9432-4D08-961F-4604410378A3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDiagnosticsExtension.md
ms.openlocfilehash: 07f679c714c7c8f6f65f89681e3c8df0fff133df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563739"
---
# Remove-AzureRmVmssDiagnosticsExtension

## КРАТКИй обзор
Удаляет расширение диагностики из VMSS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Remove-AzureRmVmssDiagnosticsExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Name] <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Remove-AzureRmVmssDiagnosticsExtension** удаляет расширение диагностики из установленной шкалы виртуальных машин (VMSS).

## ИЛЛЮСТРИРУЮТ

### Пример 1: удаление расширения диагностики из VMSS
```
PS C:\> Remove-AzureRmVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

Эта команда удаляет расширение диагностики из VMSS.

## ПАРАМЕТРЫ

### -Name (имя)
Указывает имя расширения, которое этот командлет удаляет из VMSS.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
Указывает VMSS, из которого нужно удалить расширение.

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего
Этот командлет не поддерживает никаких входных данных.

## НАПРЯЖЕНИЕ

###  
Этот командлет не создает никаких выходных данных.

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Add-AzureRmVmssDiagnosticsExtension](./Add-AzureRmVmssDiagnosticsExtension.md)

[Remove-AzureRmVMDiagnosticsExtension](./Remove-AzureRmVMDiagnosticsExtension.md)

[Remove-AzureRmVmssExtension](./Remove-AzureRmVmssExtension.md)


