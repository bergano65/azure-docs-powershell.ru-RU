---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 2DF5FB4D-A5CB-439C-AC6F-DF2130AF33EC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/disable-azurebatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchComputeNodeScheduling.md
ms.openlocfilehash: 40eb6d3cfd3961c876a5da07ced1ebcf383166e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570263"
---
# Disable-AzureBatchComputeNodeScheduling

## КРАТКИй обзор
Отключает планирование задач на заданном вычислительном узле.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### ID (по умолчанию)
```
Disable-AzureBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String>
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Disable-AzureBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>]
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Disable-AzureBatchComputeNodeScheduling** отключает планирование задач на заданном вычислительном узле.
Вычислительный узел — это виртуальная машина Azure, выделенная для определенной рабочей нагрузки приложения.
При отключении планирования задач на вычислительном узле вы также сможете определить, что делать в очереди задач узла.
**Disable-AzureBatchComputeNodeScheduling** позволяет выполнять указанные ниже действия. 

- Прервать задачи и вернуть их в очередь заданий.
Это позволяет перепланировать эти задачи на другом вычислительном узле. 
- Завершите задачи и удалите их из очереди заданий.
Задачи, остановленные таким образом, не будут перепланированы. 
- Дождитесь завершения всех задач, выполняемых в настоящее время, а затем отключите планирование задач на узле COMPUTE Node. 
- Дождитесь завершения всех выполняемых задач и истечения срока хранения данных, а затем отключите планирование задач на узле COMPUTE Node.

## ИЛЛЮСТРИРУЮТ

### Пример 1: отключение планирования задач на вычислительном узле
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Disable-AzureBatchComputeNodeScheduling -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

Эти команды отключают расписание задач на COMPUTE node TVM-1783593343_34-20151117t222514z.
Для этого первой командой в примере создается ссылка на объект для contosobatchaccount учетной записи пакетной службы.
Эта ссылка на объект хранится в переменной с именем $context.

Вторая команда использует эту ссылку на объект и командлет **Disable-AzureBatchComputeNodeScheduling** для подключения к пулу myPool и отключения планирования задач на узле TVM-1783593343_34-20151117t222514z.

Так как параметр *DisableComputeNodeSchedulingOptions* не включал в себя все задачи, которые выполняются на вычислительном узле, они будут повторно помещены в очередь.

### Пример 2: отключение планирования задач на всех вычислительных узлах в пуле
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Disable-AzureBatchComputeNodeScheduling -BatchContext $Context
```

Эти команды отключают планирование задач на всех узлах компьютера в Pool06 пула пакетов.
Для выполнения этой задачи в первой команде в примере создается ссылка на объект для учетной записи пакетной contosobatchaccount с помощью ключа учетной записи.
Эта ссылка на объект хранится в переменной с именем $context.

Во второй команде в примере используется ссылка на объект и **Get-AzureBatchComputeNode** , чтобы вернуть коллекцию всех вычислительных узлов, обнаруженных в Pool06.
После этого коллекция передается на командлет **Disable-AzureBatchComputeNodeScheduling** , чтобы отключить планирование задач на каждом из вычислительных узлов коллекции.

Так как параметр *DisableComputeNodeSchedulingOptions* не включал в себя все задачи, которые выполняются на вычислительных узлах, они будут повторно помещены в очередь.

## ПАРАМЕТРЫ

### -BatchContext
Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.
Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой. Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа. При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа. Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ComputeNode
Указывает ссылку на объект на вычислительный узел, если планирование задач отключено.
Эта ссылка на объект создается с помощью командлета Get-AzureBatchComputeNode и сохраняет возвращаемый объект COMPUTE Node в переменной.

```yaml
Type: PSComputeNode
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableSchedulingOption
Указывает, как этот командлет обрабатывает все задачи, которые выполняются в данный момент на узле компьютера, где планирование отключено.
Для этого параметра допустимы следующие значения:

- Поочередно.
Задачи немедленно останавливаются и возвращаются в очередь заданий.
Это позволяет перепланировать задачи на другом вычислительном узле.
Это значение по умолчанию. 
- Разорван.
Задачи немедленно останавливаются и удаляются из очереди заданий.
Эти задачи не будут перепланированы. 
- TaskCompletion.
Запущенные в данный момент задачи можно выполнить, прежде чем планирование задач будет отключено на вычислительном узле.
На этом узле не будут планироваться новые задачи. 
- RetainedData.
Запущенные в настоящее время задачи смогут завершить работу, и срок хранения данных будет ограничен, прежде чем планирование задач на узле COMPUTE node станет недоступным.
На этом узле не будут планироваться новые задачи.

```yaml
Type: DisableComputeNodeSchedulingOption
Parameter Sets: (All)
Aliases: 
Accepted values: Requeue, Terminate, TaskCompletion

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Указывает идентификатор вычислительного узла, на котором отключено планирование задач.

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PoolId
Указывает идентификатор пула пакетов, содержащего вычислительный узел, для которого планирование задач отключено.

Если вы используете параметр *PoolId* , не используйте параметр *ComputeNode* в той же команде.

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### BatchAccountContext
Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.

### PSComputeNode
Параметр "ComputeNode" принимает значение типа "PSComputeNode" из конвейера.

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Enable-AzureBatchComputeNodeScheduling](./Enable-AzureBatchComputeNodeScheduling.md)


