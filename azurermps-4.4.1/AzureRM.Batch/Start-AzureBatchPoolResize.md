---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 82DC8DC4-D8EC-4847-A54C-B779256FD590
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchPoolResize.md
ms.openlocfilehash: 558f8c062e60f6e9f7c18c05be8f1ccb2eafa9fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566304"
---
# Start-AzureBatchPoolResize

## КРАТКИй обзор
Начало изменения размера пула.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Start-AzureBatchPoolResize [-Id] <String> -TargetDedicated <Int32> [-ResizeTimeout <TimeSpan>]
 [-ComputeNodeDeallocationOption <ComputeNodeDeallocationOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Start-AzureBatchPoolResize** запускает операцию изменения размера пакета Azure в пуле.

## ИЛЛЮСТРИРУЮТ

### Пример 1: изменение размера пула на 12 узлов
```
PS C:\>Start-AzureBatchPoolResize -Id "ContosoPool06" -TargetDedicated 12 -BatchContext $Context
```

Эта команда запускает операцию изменения размера в пуле с ИД ContosoPool06.
Цель для операции составляет 12 выделенных вычислительных узлов.
Используйте командлет Get-AzureRmBatchAccountKeys для присвоения контекста переменной $Context.

### Пример 2: изменение размера пула с помощью параметра "изъятие"
```
PS C:\>Get-AzureBatchPool -Id "ContosoPool06" -BatchContext $Context | Start-AzureBatchPoolResize -TargetDedicated 5 -ResizeTimeout ([TimeSpan]::FromHours(1)) -ComputeNodeDeallocationOption ([Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]::Terminate) -BatchContext $Context
```

Этот командлет изменяет размер пула до пяти выделенных вычислительных узлов.
Команда получает пул с ИД ContosoPool06 с помощью командлета Get-AzureBatchPool.
Команда передает этот объект пула в текущий командлет с помощью оператора конвейера.
Команда запускает операцию изменения размера в пуле.
Цель — пять выделенных вычислительных узлов.
В команде указывается период ожидания в 1 час.
Команда задает параметр завершения выделения.

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

### -ComputeNodeDeallocationOption
Задает параметр изъятия для операции изменения размера, которую запускает этот командлет.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]
Parameter Sets: (All)
Aliases: 
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Указывает идентификатор пула, размер которого изменяется этим командлетом.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ResizeTimeout
Задает время ожидания для операции изменения размера.
Если пул не достиг целевого размера по этому времени, операция изменения размера будет остановлена.

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetDedicated
Задает целевое количество выделенных вычислительных узлов.

```yaml
Type: System.Int32
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

### Подстрок
Параметр ID принимает значение типа String из конвейера.

## НАПРЯЖЕНИЕ

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Get-AzureBatchPool](./Get-AzureBatchPool.md)

[Остановить-AzureBatchPoolResize](./Stop-AzureBatchPoolResize.md)

[Командлеты пакетной службы Azure](./AzureRM.Batch.md)


