---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 30C1AF6C-A8DC-4CA0-9E5F-10641A29D0E8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: ae640ffb0f595419bba57ff92d7789692af55d3f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559900"
---
# New-AzureRmDataFactoryPipeline

## КРАТКИй обзор
Создание конвейера в фабрике данных.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### ByFactoryName (по умолчанию)
```
New-AzureRmDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByFactoryObject
```
New-AzureRmDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory> [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzureRmDataFactoryPipeline** создает конвейер в фабрике данных Azure.
Если указать имя для конвейера, который уже существует, командлет запрашивает подтверждение перед заменой конвейера.
Если указан параметр *Force* , командлет заменяет существующий конвейер без подтверждения.

Для выполнения этих операций выполните указанные ниже действия. 

- Создание фабрики данных. 
- Создание связанных служб. 
- Создание наборов данных. 
- Создание конвейера.

Если конвейер с таким именем уже существует в фабрике данных, этот командлет предложит вам подтвердить, нужно ли перезаписывать существующий конвейер с помощью нового конвейера.
Если вы подтвердите перезапись существующего конвейера, определение конвейера также заменяется.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание конвейера
```
PS C:\>New-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json" 
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF11
Properties        : Microsoft.DataFactories.PipelineProperties
```

Эта команда создает конвейер с именем DPWikisample в фабрике данных с именем ADF.
Команда основывается на сведениях в DPWikisample.jsфайле.
Этот файл содержит сведения о действиях, таких как копирование и действия по HDInsight в конвейере.

## ПАРАМЕТРЫ

### — Фактическое.
Указывает объект **PSDataFactory** .
Этот командлет создает конвейер для фабрики данных, которую указывает этот параметр.

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataFactoryName
Указывает имя фабрики данных.
Этот командлет создает конвейер для фабрики данных, которую указывает этот параметр.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Файл
Указывает полный путь к файлу нотации объектов JavaScript (JSON), который содержит описание конвейера.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Указывает на то, что этот командлет заменяет существующий конвейер без запроса на подтверждение.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (имя)
Указывает имя создаваемого конвейера.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов Azure.
Этот командлет создает конвейер для группы, которую указывает этот параметр.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Запрашивает подтверждение перед запуском командлета.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

### Microsoft. WindowsAzure. Commands. Utilities. PSPipeline

## Пуск
* Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmDataFactoryPipeline](./Get-AzureRmDataFactoryPipeline.md)

[Remove-AzureRmDataFactoryPipeline](./Remove-AzureRmDataFactoryPipeline.md)

[Возобновить — AzureRmDataFactoryPipeline](./Resume-AzureRmDataFactoryPipeline.md)

[Set-AzureRmDataFactoryPipelineActivePeriod](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[Приостановить — AzureRmDataFactoryPipeline](./Suspend-AzureRmDataFactoryPipeline.md)


