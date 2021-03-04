---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5224BDF5-D492-4160-893E-4BB5F76C22F3
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
ms.openlocfilehash: 5db024152a01fdab8233e388da5ae176849f4b7d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975411"
---
# Get-AzDataFactoryPipeline

## SYNOPSIS
Сведения о конвейерах в фабрике данных Azure.

## СИНТАКСИС

### ByFactoryName (По умолчанию)
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
**Cmdlet Get-AzDataFactoryPipeline** получает сведения о конвейерах в фабрике данных Azure.
Если указать имя конвейера, этот cmdlet получит сведения о нем.
Если имя не указано, этот cmdlet получает сведения обо всех конвейерах в фабрике данных.

## ПРИМЕРЫ

### Пример 1. Сведения обо всех конвейерах
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
```

Эта команда получает сведения обо всех конвейерах в фабрике данных с именем ВикиADF.
Вы можете использовать одну из следующих команд:
Во втором используется объект **DataFactory** в качестве параметра.

### Пример 2. Просмотр сведений об определенном канале
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.PipelineProperties
```

Эта команда получает сведения о конвейере DPWikisample в фабрике данных с именем WikiADF.
Эта команда передает эти сведения в командлет Format-List с помощью оператора конвейера.
Этот cmdlet formats the results (Форматирование результатов).
Для получения дополнительных сведений введите `Get-Help Format-List` .

### Пример 3. Просмотр свойств для определенного конвейера
```
PS C:\> (Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Properties
Activities  : {WikiHiveActivity, BlobToSqlCopyActivity}
Description : DP Wikipedia Sample Pipelines
End         : 6/6/2014 8:00:00 AM
IsPaused    : 
RuntimeInfo : Microsoft.DataFactories.PipelineRuntimeInfo
Start       : 6/5/2014 8:00:00 PM
```

Эта команда получает сведения о конвейере DPWikisample в фабрике данных WikiADF, а затем использует стандартную точку нотации для просмотра свойства **Properties,** связанного с этим каналом.

### Пример 4. Просмотр действий для определенного конвейера
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.Activities
Transformation    : Microsoft.DataFactories.HDInsightActivityProperties
Description       : 
Inputs            : {DAWikipediaClickEvents}
LinkedServiceName : HDILinkedService
Name              : WikiHiveActivity
Outputs           : {DACuratedWikiData}
Policy            : Microsoft.DataFactories.ActivityPolicy

Transformation    : Microsoft.DataFactories.CopyActivityProperties
Description       : 
Inputs            : {DACuratedWikiData}
LinkedServiceName : HDILinkedService
Name              : BlobToSqlCopyActivity
Outputs           : {DAWikiAggregatedData}
Policy            : Microsoft.DataFactories.ActivityPolicy
```

Эта команда получает сведения о конвейере DPWikisample в фабрике данных WikiADF, а  затем использует стандартную точку для просмотра свойства "Действия", связанного с этим каналом.

### Пример 5. Просмотр сведений о времени запуска для определенного конвейера
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.RuntimeInfo
DeploymentTime
--------------
6/5/2014 10:36:46 PM
```

Эта команда получает сведения о конвейере DPWikisample в фабрике данных WikiADF, а затем использует стандартную точку для просмотра свойства **RuntimeInfo,** связанного с этим конвейером.

### Пример 6. Просмотр сведений о вводе данных для первого действия
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Properties.Activities[0].Inputs | Format-List
EndTime   : 
Length    : 
Name      : DAWikipediaClickEvents
StartTime :
```

Эта команда получает сведения о конвейере DPWikisample в фабрике данных WikiADF, а  затем использует стандартную точку для просмотра свойства "Действия", связанного с этим каналом.
Команда отображает свойство **Inputs** первого элемента массива **Activities** с помощью **Format-List.**

## PARAMETERS

### -DataFactory
Указывает объект **PSDataFactory.**
Этот cmdlet получает конвейеры, которые относятся к фабрике данных, указанной этим параметром.

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
Название фабрики данных.
Этот cmdlet получает конвейеры, которые относятся к фабрике данных, указанной этим параметром.

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

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Название конвейера, сведения о котором нужно получить.

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
Имя группы ресурсов Azure.
Этот cmdlet получает конвейеры, которые относятся к группе, указанной этим параметром.

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

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

## OUTPUTS

### Microsoft.Azure.Commands.DataFactories.Models.PSPipeline

## ПРИМЕЧАНИЯ
* Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories

## СВЯЗАННЫЕ ССЫЛКИ

[New-AzDataFactoryPipeline](./New-AzDataFactoryPipeline.md)

[Remove-AzDataFactoryPipeline](./Remove-AzDataFactoryPipeline.md)

[Resume-AzDataFactoryPipeline](./Resume-AzDataFactoryPipeline.md)

[Set-AzDataFactoryPipelineActivePeriod](./Set-AzDataFactoryPipelineActivePeriod.md)

[Suspend-AzDataFactoryPipeline](./Suspend-AzDataFactoryPipeline.md)


