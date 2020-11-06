---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchtaskcounts
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTaskCounts.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTaskCounts.md
ms.openlocfilehash: d0b98081675cd11d8d3eb60a6495ac87a1111034
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559323"
---
# Get-AzureBatchTaskCounts

## КРАТКИй обзор
Получает количество задач для указанного задания.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### Номер
```
Get-AzureBatchTaskCounts [-JobId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>]
```

### ParentObject
```
Get-AzureBatchTaskCounts [[-Job] <PSCloudJob>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>]
```

## NОПИСАНИЕ
Командлет **Get-AzureBatchTaskCounts** получает число пакетных задач Azure для пакетного задания.
Укажите задание с помощью параметра *JOBID* или параметра *задания* .
Счетчики задач предоставляют общее количество задач по активному, выполняющемуся или завершенному состоянию задачи, а также количество задач, которые были успешно выполнены или завершились сбоем. Задачи в состоянии подготовки считаются запущенными. Если validationStatus не является действительным, служба пакетной службы не смогла проверить количество состояний задачи, как указано в API "задачи списка". ValidationStatus может быть недействительным, если задание имеет более 200 000 задач.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение количества задач по ИДЕНТИФИКАТОРу
```
PS C:\> Get-AzureBatchTaskCounts -JobId "Job01" -Id "Task03" -BatchContext $Context
Active              : 1
Completed           : 0
Failed              : 0
Running             : 1
Succeeded           : 5
ValidationStatus    : Validated
```

Эта команда получает количество задач для Job01 заданий.
Используйте командлет Get-AzureRmBatchAccountKeys для присвоения контекста переменной $Context.

## ПАРАМЕТРЫ

### -BatchContext
Экземпляр BatchAccountContext, который будет использоваться при взаимодействии со службой пакетной обработки.
Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.
Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.
При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.
Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.

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

### -Job
Указывает задание, содержащее задачи, которые получает этот командлет.
Чтобы получить объект **PSCloudJob** , используйте командлет Get-AzureBatchJob.

```yaml
Type: PSCloudJob
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -JobId
Идентификатор задания, для которого требуется получить количество задач.

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## ВХОДНЫЕ данные

### System. String
Microsoft.Azure.Commands.BatCH. Models. PSCloudJob Microsoft.Azure.Commands.Batch.BatchAccountContext


## НАПРЯЖЕНИЕ

### Microsoft.Azure.Commands.BatCH. Models. PSTaskCounts


## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Get-AzureBatchJob](./Get-AzureBatchJob.md)

[Командлеты пакетной службы Azure](./AzureRM.Batch.md)
