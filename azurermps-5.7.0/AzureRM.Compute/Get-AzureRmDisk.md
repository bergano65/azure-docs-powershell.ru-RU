---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmDisk.md
ms.openlocfilehash: e34016b3bc7677c9591c07e54dd42a88a820d44b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565572"
---
# Get-AzureRmDisk

## КРАТКИй обзор
Получает свойства диска.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Get-AzureRmDisk [[-ResourceGroupName] <String>] [[-DiskName] <String>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmDisk** получает свойства диска.

## ИЛЛЮСТРИРУЮТ

### Пример 1
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

Эта команда получает свойства диска с именем "Disk01" в группе ресурсов "ResourceGroup01".

### Пример 2
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01'
```

Эта команда получает свойства всех дисков в группе ресурсов "ResourceGroup01".

### Пример 3
```
PS C:\> Get-AzureRmDisk
```

Эта команда получает свойства всех дисков подписки.

## ПАРАМЕТРЫ

### -DiskName
Указывает имя диска.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов.

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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String

## НАПРЯЖЕНИЕ

### Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskList

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

