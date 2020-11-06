---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmAvailabilitySet.md
ms.openlocfilehash: 5f2769987c87942af78bda238de00df94168249a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565579"
---
# Get-AzureRmAvailabilitySet

## КРАТКИй обзор
Получает наборы доступности Azure в группе ресурсов.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Get-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmAvailabilitySet** получает наборы доступности Azure в группе ресурсов.
Вы можете указать имя определенного набора доступности, которое нужно получить.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение определенной группы доступности
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
```

Эта команда получает группу доступности с именем AvailablitySet03 в группе ресурсов с именем ResourceGroup11.

### Пример 2: получение всех наборов доступности
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11"
```

Эта команда получает все наборы доступности в группе ресурсов с именем ResourceGroup11.

## ПАРАМЕТРЫ

### -Name (имя)
Указывает имя набора доступности, который получает этот командлет.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
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

Required: True
Position: 0
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

[New-AzureRmAvailabilitySet](./New-AzureRmAvailabilitySet.md)

[Remove-AzureRmAvailabilitySet](./Remove-AzureRmAvailabilitySet.md)


