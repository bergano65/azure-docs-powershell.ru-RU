---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebService.md
ms.openlocfilehash: 5632de726797dd36af377f76b5919590c5826606
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564359"
---
# Get-AzureRmMlWebService

## КРАТКИй обзор
Извлекает сводные данные для одной или нескольких веб-служб.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Get-AzureRmMlWebService [-ResourceGroupName <String>] [-Name <String>] [-Region <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Извлекает сведения определения веб-службы.
В зависимости от параметров, которые передавались, командлет возвращает определения для определенной веб-службы, коллекцию defintions для веб-служб для указанной группы ресурсов в текущей подписке или коллекцию defintions для веб-служб в текущей подписке.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение подробных сведений о конкретной веб-службе
```
Get-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### Пример 2: получение всех ресурсов веб-службы в текущей подписке
```
Get-AzureRmMlWebService
```

### Пример 3: получение всех веб-служб в текущей подписке и данной группе ресурсов
```
Get-AzureRmMlWebService -ResourceGroupName "myresourcegroup"
```

## ПАРАМЕТРЫ

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (имя)
Имя веб-службы, сведения о которой извлекаются.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Region (регион)
Имя Regio

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Группа ресурсов, из которой извлекаются сведения о веб-службе.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

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

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Management. MachineLearning. WebService. Models.

## Пуск
Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
