---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5490BB24-127E-4C21-B85F-B70D817B659A
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/save-azdatafactorylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
ms.openlocfilehash: 19d2c5c9b03b08bd31839dfe7e072de9517ff459
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900926"
---
# Save-AzDataFactoryLog

## КРАТКИй обзор
Загружает файлы журнала из службы обработки Azure HDInsight.

## Максимальное

### ByFactoryName (по умолчанию)
```
Save-AzDataFactoryLog [-DataFactoryName] <String> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Save-AzDataFactoryLog [-DataFactory] <PSDataFactory> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Save-AzDataFactoryLog** загружает файлы журнала, связанные с обработкой Azure HDInsight для проектов свинья или Hive, или для настраиваемых действий на локальном жестком диске.
Сначала необходимо выполнить командлет Get-AzDataFactoryRun, чтобы получить идентификатор для действия, выполняемого для среза данных, а затем использовать этот идентификатор для получения файлов журнала из хранилища BLOB-объектов, связанного с кластером HDInsight.
Если параметр *DownloadLogs* не указан, командлет просто возвращает расположение файлов журнала.
Если вы укажете *DownloadLogs* без указания выходного каталога (параметр *Output* ), файлы журнала загружаются в папку документы по умолчанию.
Если задать *DownloadLogs* и выходную папку ( *Output* ), файлы журнала будут загружены в указанную папку.

## ИЛЛЮСТРИРУЮТ

### Пример 1: сохранение файлов журнала в определенной папке
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs -Output "C:\Test"
```

Эта команда позволяет сохранить файлы журнала для действия с ИД 841b77c9-d56c-48d1-99a3-8c16c3e77d39, в котором действие относится к конвейеру в фабрике данных с именем LogProcessingFactory в группе ресурсов с именем ADF.
Файлы журнала сохраняются в папке C:\Test.

### Пример 2: сохранение файлов журнала в папке "документы по умолчанию"
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs
```

Эта команда позволяет сохранить файлы журнала в папке "документы" (по умолчанию).

### Пример 3: получение расположения файлов журнала
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39"
```

Эта команда возвращает расположение файлов журнала.
Обратите внимание, что *DownloadLogs* не указан.

## ПАРАМЕТРЫ

### — Фактическое.
Указывает объект **PSDataFactory** .

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
Этот командлет загружает файлы журнала для фабрики данных, которую указывает этот параметр.

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

### -DownloadLogs
Указывает на то, что этот командлет загружает файлы журнала на локальный компьютер.
Если папка *Ouptut* не указана, файлы сохраняются в папке "документы" во вложенной папке.

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

### -ID
Указывает идентификатор действия, выполняемого для среза данных.
Для получения идентификатора используйте командлет Get-AzDataFactoryRun.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Output
Указывает папку выходных данных, в которой сохраняются Скачанные файлы журнала.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов Azure.
Этот командлет создает фабрику данных, принадлежащую группе, которую указывает этот параметр.

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System. String

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Factoring. Models. PSRunLogInfo

## Пуск
* Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzDataFactoryRun](./Get-AzDataFactoryRun.md)

[Get-AzDataFactoryPipeline](./Get-AzDataFactoryPipeline.md)

[New-AzDataFactoryPipeline](./New-AzDataFactoryPipeline.md)

[Remove-AzDataFactoryPipeline](./Remove-AzDataFactoryPipeline.md)

[Set-AzDataFactoryPipelineActivePeriod](./Set-AzDataFactoryPipelineActivePeriod.md)

[Приостановить — AzDataFactoryPipeline](./Suspend-AzDataFactoryPipeline.md)


