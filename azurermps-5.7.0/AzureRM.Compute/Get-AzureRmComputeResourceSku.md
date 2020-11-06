---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmComputeResourceSku.md
ms.openlocfilehash: b9e1c42ca3a67a80a939a4e79626253b903764f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559223"
---
# Get-AzureRmComputeResourceSku

## КРАТКИй обзор
Список всех конфигураций вычислительных ресурсов

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Get-AzureRmComputeResourceSku [<CommonParameters>]
```

## NОПИСАНИЕ
Список всех конфигураций вычислительных ресурсов

## ИЛЛЮСТРИРУЮТ

### Пример 1
```
PS C:\> PS C:\> Get-AzureRmComputeResourceSku | where {$_.Locations.Contains("westus")};
```

Список всех вычислительных конфигураций ресурсов в Западном регионе США

## ПАРАМЕТРЫ

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего


## НАПРЯЖЕНИЕ

### System. Object

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

