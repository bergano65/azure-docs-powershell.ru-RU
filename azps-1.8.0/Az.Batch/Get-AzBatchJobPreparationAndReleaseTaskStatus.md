---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjobpreparationandreleasetaskstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
ms.openlocfilehash: accba78cd05d6fcc18eb7f48c7cfb2839c0e9417
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93731890"
---
# Get-AzBatchJobPreparationAndReleaseTaskStatus

## КРАТКИй обзор
Возвращает состояние подготовки пакетного задания и выпуск задачи.

## Максимальное

### ID (по умолчанию)
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-Id] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-InputObject] <PSCloudJob> [-Filter <String>]
 [-MaxCount <Int32>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzBatchJobPreparationAndReleaseTaskStatus** получает статус подготовки пакетного задания Azure и состояние задачи выпуска для пакетного задания.
Для этого командлета необходимо указать параметр *ID* или экземпляр **PSCloudJob** .

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение сведений о подготовке задания и его выпуске
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $Context -Id Test

ComputeNodeId                          : tvm-2316545714_1-20170613t201733z
ComputeNodeUrl                         : https://account.westus.batch.azure.com/pools/test/nodes/tvm-2316545714_1-20170613t201733z
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 : test
```

Эта команда получает состояние задачи подготовки и выпуска для задания "тест".
Используйте командлет Get-AzBatchAccountKeys для присвоения контекста переменной $Context.

### Пример 2: получение сведений о подготовке и выпуске задания с фильтром и выбор указанного
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $context -Id Test -Filter "nodeId eq 'tvm-2316545714_1-20170613t201733z'" -Select "jobPreparationTaskExecutionInfo"

ComputeNodeId                          :
ComputeNodeUrl                         :
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 :
```

Эта команда получает состояние задачи подготовки и освобождения для задания "тест" на узле "TVM-2316545714_1-20170613t201733z" и использует предложение SELECT, чтобы указать, что нужно возвращать только сведения о JobPreparationTaskExecutionInformation

## ПАРАМЕТРЫ

### -BatchContext
Экземпляр BatchAccountContext, который будет использоваться при взаимодействии со службой пакетной обработки.
Используйте командлет Get-AzBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.

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

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

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

### -Expand
Указывает предложение развертывания протокола Open Data Protocol (OData).
Укажите значение этого параметра, чтобы получить связанные сущности от основной сущности, которые вы получаете.

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

### -Фильтр
Задает предложение фильтра OData.
Если вы не укажете фильтр, этот командлет возвращает состояние задачи "подготовка" и "выпуск" для задания.

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
Указывает идентификатор задания, для которого требуется получить задачи подготовки и выпуска.
Подстановочные знаки указывать нельзя.

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Указывает объект **PSCloudJob** , который представляет задание для получения состояния задачи подготовки и выпуска.
Чтобы получить объект **PSCloudJob** , используйте командлет Get-AzBatchJob.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MaxCount
Задает максимальное количество возвращаемых заданий и состояние задачи "выпустить".
Если вы задаете нулевое значение (0) или меньше, в командлете не используется верхний предел.
Значение по умолчанию — 1000.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SELECT
Задает предложение SELECT OData.
Укажите значение этого параметра, чтобы получить конкретные свойства, а не все свойства объекта.

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

### Microsoft.Azure.Commands.BatCH. Models. PSCloudJob

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## НАПРЯЖЕНИЕ

### Microsoft.Azure.Commands.BatCH. Models. PSJobPreparationAndReleaseTaskExecutionInformation

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzBatchJob](./Get-AzBatchJob.md)

[Командлеты пакетной службы Azure](/powershell/module/az.batch)
