---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImageType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImageType.md
ms.openlocfilehash: 15b1316940c42534844245eaaf1aee3e450adc4b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559199"
---
# Get-AzureRmVMExtensionImageType

## КРАТКИй обзор
Получает тип расширения Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Get-AzureRmVMExtensionImageType -Location <String> -PublisherName <String> [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmVMExtensionImageType** получает тип расширения Azure.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение типа изображения расширения
```
PS C:\> Get-AzureRmVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

Эта команда получает тип изображения расширения для указанного издателя и места.

## ПАРАМЕТРЫ

### -Location
Указывает расположение расширения.
Этот командлет получает тип расширения в расположении, указанном этим параметром.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublisherName
Указывает имя издателя расширения.
Чтобы получить издатель расширения, используйте командлет Get-AzureRmVMImagePublisher.
Этот командлет получает тип расширения от издателя, который указывает этот параметр.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
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

[Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md)

[Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md)


