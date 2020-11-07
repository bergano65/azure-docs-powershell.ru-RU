---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 36EB9CE6-EAC9-471C-97D6-14E882E0F710
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchComputeNodeScheduling.md
ms.openlocfilehash: 6c890836d8ca22e617fdc88788a6809cbce8581c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734088"
---
# Enable-AzureBatchComputeNodeScheduling

## КРАТКИй обзор
Включает планирование задач на заданном вычислительном узле.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### ID (по умолчанию)
```
Enable-AzureBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Enable-AzureBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Enable-AzureBatchComputeNodeScheduling** включает планирование задач на заданном вычислительном узле.
Вычислительный узел — это виртуальная машина Azure, выделенная для определенной рабочей нагрузки приложения.

## ИЛЛЮСТРИРУЮТ

### Пример 1: включение планирования задач на вычислительном узле
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Enable-AzureBatchComputeNodeScheduling  -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

Эти команды включают планирование задач на вычислительном узле TVM-1783593343_34-20151117t222514z.
Для этого в первой команде примера создается ссылка на объект, содержащая ключи учетной записи для пакетной учетной записи contosobatchaccount.
Эта ссылка на объект хранится в переменной с именем $context.

Вторая команда использует эту ссылку на объект и командлет **Enable-AzureBatchComputeNodeScheduling** для подключения к пулу myPool и включения планирования задач в TVM-1783593343_34-20151117t222514z.

### Пример 2: включение планирования задач на вычислительных узлах в пуле
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Enable-AzureBatchComputeNodeScheduling  -BatchContext $Context
```

Эти команды включают планирование задач на всех вычислительных узлах, обнаруженных в пуле Pool06.
Для выполнения этой задачи в первой команде в примере создается ссылка на объект с ключами учетной записи для пакетной учетной записи contosobatchaccount.
Эта ссылка на объект хранится в переменной с именем $context.

Во второй команде в примере используется ссылка на объект и **Get-AzureBatchComputeNode** , чтобы вернуть коллекцию всех вычислительных узлов, обнаруженных в Pool06.
Затем эта коллекция передается командлету **Enable-AzureBatchComputeNodeScheduling** , который включает планирование задач на каждом из вычислительных узлов коллекции.

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

### -ComputeNode
Указывает ссылку на объект на вычислительный узел, для которого включено планирование задач.
Эта ссылка на объект создается с помощью командлета Get-AzureBatchComputeNode и сохраняет возвращаемый объект COMPUTE Node в переменной.

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

### -ID
Указывает идентификатор вычислительного узла, на котором включено планирование задач.

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
Указывает идентификатор пула пакетов, содержащего вычислительный узел, для которого включено планирование задач.

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

### PSComputeNode
Параметр "ComputeNode" принимает значение типа "PSComputeNode" из конвейера.

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Disable-AzureBatchComputeNodeScheduling](./Disable-AzureBatchComputeNodeScheduling.md)


