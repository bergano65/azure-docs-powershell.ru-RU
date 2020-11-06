---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/new-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/New-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/New-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 6badeec8b2425a5ca8e10dc88039a1d28e055cc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560188"
---
# New-AzureRmPowerBIEmbeddedCapacity

## КРАТКИй обзор
Создает новую внедренную емкость PowerBI.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
New-AzureRmPowerBIEmbeddedCapacity 
    [-ResourceGroupName] <String> 
    [-Name] <String> 
    [-Location] <String>
    [-Sku] <String> 
    [-Administrator] <String>
    [[-Tag] <Hashtable>] 
    [-WhatIf] 
    [-Confirm] 
    [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет New-AzureRmPowerBIEmbeddedCapacity создает новую пропускную способность PowerBI Embedded.

## ИЛЛЮСТРИРУЮТ

### Пример 1
```
PS C:\> New-AzureRmPowerBIEmbeddedCapacity -ResourceGroupName "testRG" -Name "testcapacity" -Location "West Central US" -Sku "A1" -Administrator admin@microsoft.com
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}
```

Создает емкость с именем testcapacity в области "Центральная часть США и в группе ресурсов" в Azure Region testRG. Уровень SKU для производственной мощности будет равен a1.

## ПАРАМЕТРЫ

### -ResourceGroupName
Имя группы ресурсов Azure, к которой относится емкость

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### -Name (имя)
Имя встроенной емкости PowerBI

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept wildcard characters: False
```

### -Location
Регион Azure, на котором размещена емкость для PowerBI Embedded

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept wildcard characters: False
```

### -SKU
Название SKU для производственной мощности.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: A1, A2, A3, A4, A5, A6

Required: True
Position: 3
Default value: None
Accept wildcard characters: False
```

### -Администратор
Имена пропускной способности, разделенные запятыми, которые нужно установить в качестве администратора емкости

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept wildcard characters: False
```

### -Тег
Пары "ключ-значение" в виде хэш-таблицы, установленной в качестве тегов в пропускной способности.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### -Confirm
Предлагает пользователю подтвердить необходимость выполнения операции.

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
Описывает действия, которые будет выполнять текущая операция без их фактического выполнения.

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

### Ничего
Этот командлет не поддерживает никаких входных данных.

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmPowerBIEmbeddedCapacity](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[Remove-AzureRmPowerBIEmbeddedCapacity](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
