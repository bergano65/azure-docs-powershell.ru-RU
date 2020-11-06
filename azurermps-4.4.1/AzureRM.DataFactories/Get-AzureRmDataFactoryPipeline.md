---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 5224BDF5-D492-4160-893E-4BB5F76C22F3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: 9188e0084c73ab984c898e94cbf94c33cde52995
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569584"
---
# Get-AzureRmDataFactoryPipeline

## КРАТКИй обзор
Получение сведений о конвейерах в фабрике данных Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### ByFactoryName (по умолчанию)
```
Get-AzureRmDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzureRmDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmDataFactoryPipeline** получает сведения о конвейерах в фабрике данных Azure.
Если вы задаете имя конвейера, этот командлет получает сведения об этом конвейере.
Если имя не задано, этот командлет получает сведения обо всех конвейерах в фабрике данных.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение сведений обо всех каналах
```
PS C:\>Get-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
```

Эта команда получает сведения обо всех конвейерах в фабрике данных с именем WikiADF.
Вы можете выполнить одну из следующих команд:
Во втором используется объект **фактов** в качестве параметра.

### Пример 2: получение сведений о конкретном конвейере
```
PS C:\>Get-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.PipelineProperties
```

Эта команда получает сведения о конвейере с именем DPWikisample в фабрике данных с именем WikiADF.
Команда передает эти данные командлету Format-List с помощью оператора конвейера.
Этот командлет форматирует результаты.
Для получения дополнительных сведений введите `Get-Help Format-List` .

### Пример 3: получение свойств определенного конвейера
```
PS C:\> (Get-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Properties
Activities  : {WikiHiveActivity, BlobToSqlCopyActivity}
Description : DP Wikipedia Sample Pipelines
End         : 6/6/2014 8:00:00 AM
IsPaused    : 
RuntimeInfo : Microsoft.DataFactories.PipelineRuntimeInfo
Start       : 6/5/2014 8:00:00 PM
```

Эта команда получает сведения о конвейере с именем DPWikisample в фабрике данных с именем WikiADF и использует стандартную нотацию для просмотра свойства **Properties** , связанного с этим конвейером.

### Пример 4: получение действий для определенного конвейера
```
PS C:\>(Get-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.Activities
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

Эта команда получает сведения о конвейере с именем DPWikisample в фабрике данных с именем WikiADF, а затем использует стандартную нотацию для просмотра свойства **activitys** , связанного с этим конвейером.

### Пример 5: получение сведений о среде выполнения для определенного конвейера
```
PS C:\>(Get-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.RuntimeInfo
DeploymentTime
--------------
6/5/2014 10:36:46 PM
```

Эта команда получает сведения о конвейере с именем DPWikisample в фабрике данных с именем WikiADF и использует стандартную нотацию для просмотра свойства **RuntimeInfo** , связанного с этим конвейером.

### Пример 6: получение сведений о входных данных для первого действия
```
PS C:\>(Get-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Properties.Activities[0].Inputs | Format-List
EndTime   : 
Length    : 
Name      : DAWikipediaClickEvents
StartTime :
```

Эта команда получает сведения о конвейере с именем DPWikisample в фабрике данных с именем WikiADF, а затем использует стандартную нотацию для просмотра свойства **activitys** , связанного с этим конвейером.
Команда отображает свойство **Inputs** первого элемента массива " **действия** " с помощью **Format-List**.

## ПАРАМЕТРЫ

### — Фактическое.
Указывает объект **PSDataFactory** .
Этот командлет получает конвейеры, которые принадлежат к фабрике данных, которую указывает этот параметр.

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
Этот командлет получает конвейеры, которые принадлежат к фабрике данных, которую указывает этот параметр.

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

### -Name (имя)
Указывает имя конвейера, сведения о котором требуется получить.

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
Этот командлет получает конвейеры, принадлежащие к группе, которую указывает этот параметр.

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

### System. Collections. Generic. List ' 1 [[Microsoft. WindowsAzure. Commands. Utilities. PSPipeline, Microsoft. WindowsAzure. Commands, Version = 0.8.2.0, Culture = Neutral, PublicKeyToken = 31bf3856ad364e35]] Microsoft. WindowsAzure. Commands. Utilities. PSPipeline

## Пуск
* Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[New-AzureRmDataFactoryPipeline](./New-AzureRmDataFactoryPipeline.md)

[Remove-AzureRmDataFactoryPipeline](./Remove-AzureRmDataFactoryPipeline.md)

[Возобновить — AzureRmDataFactoryPipeline](./Resume-AzureRmDataFactoryPipeline.md)

[Set-AzureRmDataFactoryPipelineActivePeriod](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[Приостановить — AzureRmDataFactoryPipeline](./Suspend-AzureRmDataFactoryPipeline.md)


