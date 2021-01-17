---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2DF5FB4D-A5CB-439C-AC6F-DF2130AF33EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 9e93d6fd17d4ba308e6d5752554fb03639fce769
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407063"
---
# Disable-AzBatchComputeNodeScheduling

## SYNOPSIS
Отключает планирование задач для указанного узла вычислений.

## СИНТАКСИС

### ИД (по умолчанию)
```
Disable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String>
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Disable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>]
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
**Cmdlet Disable-AzBatchComputeNodeScheduling** отключает планирование задач в указанном узле вычислений.
Узел вычислений — это виртуальная машинка Azure, выделенная для конкретной рабочей нагрузки приложения.
Если отключить планирование задач на узле компьютеров, вы также сможете определить, что делать с заданиями, которые в настоящий момент находятся в очереди задач узла.
**Disable-AzBatchComputeNodeScheduling** позволяет: 
- Прервать задачи и поместить их обратно в очередь заданий.
Это позволяет перепланировать эти задачи на другом узле компьютеров. 
- Завершайте задачи и удаляйте их из очереди заданий.
Задачи, остановленные таким способом, не будут запланированы повторно. 
- Дождите завершения всех задач, которые выполняются в данный момент, а затем отключили планирование задач на узле вычислений. 
- Дождите завершения всех задач и истечения всех периодов хранения данных, а затем отключаете планирование задач на узле компьютеров.

## ПРИМЕРЫ

### Пример 1. Отключение планирования задач на узле вычислений
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Disable-AzBatchComputeNodeScheduling -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

Эти команды отключат расписание задач на узле вычислений tvm-1783593343_34-20151117t222514z.
Для этого первая команда в примере создает ссылку на ключи учетных записей для пакетной учетной записи contosobatchaccount.
Эта ссылка на объект хранится в переменной с именем $context.
Затем вторая команда использует эту ссылку на объект и командлет **Disable-AzBatchComputeNodeScheduling** для подключения к пулу myPool и отключения планирования задач в узле tvm-1783593343_34-20151117t222514z.
Так как *параметр DisableComputeNodeSchedulingOptions* не был включен в список задач, которые в данный момент запускаются на узле вычислений, будет выполняться повторно.

### Пример 2. Отключение планирования задач на всех узлах компьютеров в пуле
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Disable-AzBatchComputeNodeScheduling -BatchContext $Context
```

Эти команды отключать планирование задач на всех узлах компьютеров в пакетном пуле пула.
Для выполнения этой задачи первая команда в примере создает ссылку на ключи учетных записей для пакетной учетной записи contosobatchaccount.
Эта ссылка на объект хранится в переменной с именем $context.
Вторая команда в этом примере использует эту ссылку на объект и **Get-AzBatchComputeNode** для получения коллекции всех узлов вычислений, найденных в Pool06.
Затем эта коллекция передается в канал, чтобы отключить планирование задач на каждом узле вычислений в коллекции. 
Так как *параметр DisableComputeNodeSchedulingOptions* не был включен в список задач, которые в настоящее время будут выполняться на узлах компьютеров, будет выполняться повторно.

## PARAMETERS

### -BatchContext
Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.
Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой batchy будет использоваться проверка подлинности Azure Active Directory. Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа. При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию. Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.

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

### -ComputeNode
Указывает ссылку на узел вычислений, для которой отключено планирование задач.
Эта ссылка создается с помощью Get-AzBatchComputeNode и хранения возвращаемого объекта узла вычислений в переменной.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject
Aliases:

Required: False
Position: 0
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

### -DisableSchedulingOption
Определяет, как этот cmdlet работает с задачами, которые в данный момент запущены на узле компьютера, где планирование отключено.
Допустимые значения этого параметра:
- "Просрочено".
Задачи немедленно останавливаются и возвращаются в очередь заданий.
Это позволяет перепланировать задачи на другом узле компьютеров.
Это значение по умолчанию. 
- Завершить.
Задачи немедленно останавливаются и удаляются из очереди заданий.
Переплановка этих задач не планируется. 
- "Простое задание задач".
Выполнение текущих задач можно выполнить до отключения планирования задач на узле вычислений.
Новые задачи не будут запланированы на этом узле. 
- RetainedData.
В настоящий момент задачи завершаются, а срок хранения данных может истечь до отключения планирования задач на узле вычислений.
Новые задачи не будут запланированы на этом узле.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.DisableComputeNodeSchedulingOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
Определяет ИД узла компьютеров, на котором отключено планирование задач.

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PoolId
Определяет ИД пула пакетов, который содержит узел вычислений, для которых отключено планирование задач.
Если вы используете параметр *PoolId,* не используйте его *в* той же команде.

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

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.Commands.Batch. Models.PSComputeNode

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## OUTPUTS

### System.Void

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Enable-AzBatchComputeNodeScheduling](./Enable-AzBatchComputeNodeScheduling.md)


