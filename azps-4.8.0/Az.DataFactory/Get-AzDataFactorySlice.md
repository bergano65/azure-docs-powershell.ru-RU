---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: C102232A-C9C8-4CEE-8535-7C7A70057B06
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryslice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
ms.openlocfilehash: a71ccc37fe1c6b6811b955c5d84353dfecd66c2f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236804"
---
# Get-AzDataFactorySlice

## КРАТКИй обзор
Получает срезы данных для набора данных в фабрике данных Azure.

## Максимальное

### ByFactoryName (по умолчанию)
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactoryName] <String> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactory] <PSDataFactory> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzDataFactorySlice** получает срезы данных для набора данных в службе фабрики данных Azure.
Укажите время начала и время окончания, чтобы определить диапазон срезов данных для просмотра.
Состояние среза данных — одно из следующих значений: 
- PendingExecution.
Обработка данных не начата. 
- Выполняется.
Выполняется обработка данных. 
- Начать.
Обработка данных завершена.
Срез данных готов к зависимым сегментам, чтобы использовать его. 
- Ошибкой.
Не удалось выполнить вызов, создающий срез. 
- Пуст.
Фабрика данных пропускает обработку среза. 
- Повторить.
Фабрика данных повторяет запуск, создающий срез. 
- Время ожидания истекло. Превышено время ожидания обработки данных. 
- PendingValidation.
Срез данных ожидает подтверждения перед обработкой. 
- Повторите проверку.
Фабрика данных повторяет проверку среза. 
- Проверка не удалась.
Проверка среза завершилась ошибкой.
Для каждого сектора вы можете просмотреть дополнительные сведения о запуске, который создает срез с помощью командлета Get-AzDataFactoryRun.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение срезов данных для набора данных
```powershell
PS C:\>Get-AzDataFactorySlice -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-20T10:00:00Z
ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 1:00:00 AM
End               : 5/21/2014 2:00:00 AM
RetryCount        : 0
Status            : Ready

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 2:00:00 AM
End               : 5/21/2014 3:00:00 AM
RetryCount        : 0
Status            : Ready

. . . 

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 8:00:00 PM
End               : 5/21/2014 9:00:00 PM
RetryCount        : 0
Status            : PendingExecution

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 9:00:00 PM
End               : 5/21/2014 10:00:00 PM
RetryCount        : 0
Status            : PendingExecution

. . .
```

Эта команда получает все срезы данных для набора данных с именем WikiAggregatedData в фабрике данных с именем WikiADF.
Команда получает срезы, созданные после того, как указан параметр StartDateTime.
Следующий пример кода задает доступность для этого набора данных каждый час в файле нотации JavaScript Object Notation (JSON).
доступность: {period: "Hour"; periodMultiplier: 1} некоторые результаты готовы, а другие — PendingExecution.
Готовые срезы уже запущены.
Ожидающие отрезки выполняются в конце каждого часа в интервале, указанном в командлете Set-AzDataFactoryPipelineActivePeriod.
В этом примере начальные и конечные периоды для конвейера и среза имеют значение один день (24 часа).

### Пример 2

Получает срезы данных для набора данных в фабрике данных Azure. (автоматически сформированные)

```powershell <!-- Aladdin Generated Example --> 
Get-AzDataFactorySlice -DataFactoryName 'WikiADF' -DatasetName 'DAWikiAggregatedData' -EndDateTime 2014-05-22T16:00:00Z -ResourceGroupName 'ADF' -StartDateTime 2014-05-20T10:00:00Z
```

## ПАРАМЕТРЫ

### — Фактическое.
Указывает объект **PSDataFactory** .
Этот командлет получает срезы, которые относятся к фабрике данных, которую указывает этот параметр.

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
Этот командлет получает срезы, которые относятся к фабрике данных, которую указывает этот параметр.

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

### -DatasetName
Указывает имя набора данных, для которого этот командлет получает срезы.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
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

### -EndDateTime
Указывает конец периода времени в качестве объекта **DateTime** .
Этот командлет получает срезы, созданные до того момента, когда этот параметр указан.
Чтобы получить дополнительные сведения о объектах **DateTime** , введите `Get-Help Get-Date` .
*EndDateTime* должен быть указан в формате ISO8601, как показано в следующих примерах: 2015-01-01Z 2015-01-01T00:00-1-01:00Z 1:00:01T00 z (UTC) 2015-0,01-: 00.00 – 8 – 00.000

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов Azure.
Этот командлет получает срезы, которые относятся к группе, которую указывает этот параметр.

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

### -StartDateTime
Задает начало периода времени в качестве объекта **DateTime** .
Этот командлет получает срезы, созданные после того, как указан этот параметр.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System. String

## НАПРЯЖЕНИЕ

### Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice

## Пуск
* Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Set-AzDataFactorySliceStatus](./Set-AzDataFactorySliceStatus.md)

[Get-AzDataFactoryRun](./Get-AzDataFactoryRun.md)

[Set-AzDataFactoryPipelineActivePeriod](./Set-AzDataFactoryPipelineActivePeriod.md)


