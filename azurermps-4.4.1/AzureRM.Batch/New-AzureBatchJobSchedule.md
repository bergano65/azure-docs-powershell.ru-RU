---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 87E7FA51-427E-4DB8-A6A2-D8638FD3DB8B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJobSchedule.md
ms.openlocfilehash: 0a31b787b1be6d45caca74d01ee5d15d00071641
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565654"
---
# New-AzureBatchJobSchedule

## КРАТКИй обзор
Создание расписания заданий в пакетной службе.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
New-AzureBatchJobSchedule [-Id] <String> [-DisplayName <String>] -Schedule <PSSchedule>
 -JobSpecification <PSJobSpecification> [-Metadata <IDictionary>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzureBatchJobSchedule** создает расписание задач в пакетной службе Azure.
Параметр *BatchAccountContext* указывает учетную запись, в которой этот командлет создает расписание.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Создание расписания задания
```
PS C:\>$Schedule = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSSchedule"
PS C:\> $Schedule.RecurrenceInterval = [TimeSpan]::FromDays(1)
PS C:\> $JobSpecification = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSJobSpecification"
PS C:\> $JobSpecification.PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation"
PS C:\> $JobSpecification.PoolInformation.PoolId = "ContosoPool06"
PS C:\> New-AzureBatchJobSchedule -Id "JobSchedule17" -Schedule $Schedule -JobSpecification $JobSpecification -BatchContext $Context
```

В этом примере создается расписание задания.

Первые пять команд создают и изменяют объекты **PSSchedule** , **PSJobSpecification** и **PSPoolInformation** .
Команды используют командлеты New-Object и стандартный синтаксис PowerShell для Azure.
Команды хранят эти объекты в переменных $Schedule и $JobSpecification.

В последней команде создается расписание заданий с ИДЕНТИФИКАТОРом JobSchedule17.
В этом расписании создаются задания с интервалом повторения в один день.
Задания выполняются в пуле с ИД ContosoPool06, как указано в пятом команде.
Используйте командлет **Get-AzureRmBatchAccountKeys** , чтобы назначить контекст переменной $context.

## ПАРАМЕТРЫ

### -BatchContext
Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.
Чтобы получить объект **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzureRmBatchAccountKeys.

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DisplayName
Задает отображаемое имя расписания задания.

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

### -ID
Указывает идентификатор расписания задания, создаваемого этим командлетом.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -JobSpecification
Задает сведения о заданиях, которые включает этот командлет в расписание задания.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Metadata
Задает метаданные в виде пар "ключ-значение", которые нужно добавить в расписание задания.
Ключом является имя метаданных.
Значением является значение метаданных.

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Планирование
Указывает расписание, определяющее время создания заданий.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSSchedule
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
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

### BatchAccountContext
Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Disable-AzureBatchJobSchedule](./Disable-AzureBatchJobSchedule.md)

[Enable-AzureBatchJobSchedule](./Enable-AzureBatchJobSchedule.md)

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Get-AzureBatchJobSchedule](./Get-AzureBatchJobSchedule.md)

[Remove-AzureBatchJobSchedule](./Remove-AzureBatchJobSchedule.md)

[Остановить-AzureBatchJobSchedule](./Stop-AzureBatchJobSchedule.md)

[Командлеты пакетной службы Azure](./AzureRM.Batch.md)


