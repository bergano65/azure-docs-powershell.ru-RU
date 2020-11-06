---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmContainerService.md
ms.openlocfilehash: d2a53d221adf7483899056791aefd00b03aca26e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565574"
---
# Get-AzureRmContainerService

## КРАТКИй обзор
Возвращает службу контейнеров.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Get-AzureRmContainerService [[-ResourceGroupName] <String>] [[-Name] <String>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmContainerService** Получает службу контейнеров.
Вы можете просматривать свойства службы контейнеров, в том числе состояние, количество основных и агентов, а также полное доменное имя главного и агента.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение службы контейнеров
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

Эта команда получает службу контейнеров с именем CSResourceGroup17.

## ПАРАМЕТРЫ

### -Name (имя)
Указывает имя службы контейнеров, которую получает этот командлет.

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

### -ResourceGroupName
Указывает группу ресурсов для службы контейнеров, которую получает этот командлет.

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

### Ничего
Этот командлет не поддерживает никаких входных данных.

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[New-AzureRmContainerService](./New-AzureRmContainerService.md)

[Remove-AzureRmContainerService](./Remove-AzureRmContainerService.md)

[Update-AzureRmContainerService](./Update-AzureRmContainerService.md)


