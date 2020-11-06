---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMSize.md
ms.openlocfilehash: d75ff7f549ddb1efd9f5640b9b2d634449faa21c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565565"
---
# Get-AzureRmVMSize

## КРАТКИй обзор
Получает доступные размеры виртуальных машин.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### ListVirtualMachineSizeParamSet (по умолчанию)
```
Get-AzureRmVMSize [-Location] <String> [<CommonParameters>]
```

### ListAvailableSizesForAvailabilitySet
```
Get-AzureRmVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String> [<CommonParameters>]
```

### ListAvailableSizesForVirtualMachine
```
Get-AzureRmVMSize [-ResourceGroupName] <String> [-VMName] <String> [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmVMSize** получает доступ к размерам виртуальных машин.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение размеров виртуальных машин для местоположения
```
PS C:\> Get-AzureRmVMSize -Location "Central US"
```

Эта команда получает доступные размеры для виртуальных машин в указанном расположении.

### Пример 2: получение размеров для группы доступности
```
PS C:\> Get-AzureRmVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

Эта команда получает доступные размеры виртуальных машин, которые можно развернуть в группе доступности с именем AvailabilitySet17.

### Пример 3: получение размеров для существующей виртуальной машины
```
PS C:\> Get-AzureRmVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

Эта команда получает доступные размеры для существующей виртуальной машины с именем VirtualMachine12.
Вы можете изменить размер этой виртуальной машины на размер, который получает эта команда.

## ПАРАМЕТРЫ

### -AvailabilitySetName
Указывает имя набора доступности, для которого этот командлет получает доступные размеры виртуальных машин.

```yaml
Type: String
Parameter Sets: ListAvailableSizesForAvailabilitySet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Location
Указывает расположение, для которого этот командлет получает доступные размеры виртуальных машин.

```yaml
Type: String
Parameter Sets: ListVirtualMachineSizeParamSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов виртуальной машины.

```yaml
Type: String
Parameter Sets: ListAvailableSizesForAvailabilitySet, ListAvailableSizesForVirtualMachine
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Указывает имя виртуальной машины, которую этот командлет получает доступные размеры виртуальных машин для изменения размера.

```yaml
Type: String
Parameter Sets: ListAvailableSizesForVirtualMachine
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего
Этот командлет не поддерживает никаких входных данных.

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmVM](./Get-AzureRmVM.md)


