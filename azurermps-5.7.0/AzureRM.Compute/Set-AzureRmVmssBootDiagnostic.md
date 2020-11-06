---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssBootDiagnostic.md
ms.openlocfilehash: 868bf95ca2f54105143f122665ffa89732ada167
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565552"
---
# Set-AzureRmVmssBootDiagnostic

## КРАТКИй обзор
Настройка профиля диагностики загрузки для шкалы виртуальных машин.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Set-AzureRmVmssBootDiagnostic [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Настройка профиля диагностики загрузки для шкалы виртуальных машин.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Настройка свойства профиля диагностики загрузки для VMSS
```
PS C:\> $vmss = New-AzureRmVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzureRmVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzureRmVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

Эта команда задает свойство профиля диагностики загрузки для VMSS с именем ContosoVMSS.

## ПАРАМЕТРЫ

### -Включено
Следует ли включить диагностику загрузки на множестве масштабов виртуальных машин.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageUri
Универсальный код ресурса (URI) учетной записи хранения, которая используется для размещения выходных данных консоли и снимка экрана.

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

### -VirtualMachineScaleSet
Указывает объект VMSS.
Для создания объекта можно использовать командлет New-AzureRmVmssConfig.

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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSet
System. Nullable "1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]] System. String

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSet

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

