---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 4B373447-3078-4C1F-932E-8337AB170DEB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchpoolusagemetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolUsageMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolUsageMetrics.md
ms.openlocfilehash: b8a6a7b40d0dd4756aff94c1e1b653efef03bca6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559339"
---
# Get-AzureBatchPoolUsageMetrics

## КРАТКИй обзор
Получает метрики использования пула для учетной записи пакетной службы.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Get-AzureBatchPoolUsageMetrics [-StartTime <DateTime>] [-EndTime <DateTime>] [-Filter <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureBatchPoolUsageMetrics** получает метрики использования, агрегированные по пулам между отдельными интервалами времени для указанной учетной записи.
Вы можете получить статистику для определенного пула и для интервала времени.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Получение метрик использования пула для диапазона времени
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $StartTime = Get-Date -Date "2016-05-16 00:00:00Z"
PS C:\> $EndTime = Get-Date -Date "2016-05-16 01:00:00Z"
PS C:\> Get-AzureBatchPoolUsageMetrics -StartTime $StartTime -EndTime $EndTime -BatchContext $context
DataEgressGiB      : 6.68875873088837E-06
DataIngressGiB     : 1.9485130906105E-05
EndTime            : 5/16/2016 12:30:00 AM
PoolId             : testpool1
StartTime          : 5/16/2016 12:00:00 AM
TotalCoreHours     : 8
VirtualMachineSize : standard_d4

DataEgressGiB      : 5.61587512493134E-06
DataIngressGiB     : 1.76150351762772E-05
EndTime            : 5/16/2016 12:30:00 AM
PoolId             : testpool2
StartTime          : 5/16/2016 12:00:00 AM
TotalCoreHours     : 12
VirtualMachineSize : standard_d4

DataEgressGiB      : 7.36676156520844E-06
DataIngressGiB     : 2.10804864764214E-05
EndTime            : 5/16/2016 1:00:00 AM
PoolId             : testpool1
StartTime          : 5/16/2016 12:30:00 AM
TotalCoreHours     : 7.99999999955555
VirtualMachineSize : standard_d4

DataEgressGiB      : 5.80586493015289E-06
DataIngressGiB     : 1.80602073669434E-05
EndTime            : 5/16/2016 1:00:00 AM
PoolId             : testpool2
StartTime          : 5/16/2016 12:30:00 AM
TotalCoreHours     : 11.9999999993333
VirtualMachineSize : standard_d4
```

Первая команда создает ссылку на объект для учетной записи пакетной службы с именем ContosoBatchAccount с помощью **Get-AzureRmBatchAccountKeys**.
Команда сохраняет ссылку на этот объект в переменной $Context.

Следующие две команды создают объекты **DateTime** с помощью командлета Get-Date.
Команды хранят эти значения в переменных $StartTime и $EndTime, которые используются в финальной команде.

Последняя команда возвращает все метрики использования пула, агрегированные по пулам, через интервал времени между указанными временем начала и окончания.

### Пример 2: Получение метрик использования пула с помощью фильтра
```
PS C:\>Get-AzureBatchPoolUsageMetrics -Filter "poolId eq 'ContosoPool'" -BatchContext $Context
DataEgressGiB      : 9.0496614575386E-06
DataIngressGiB     : 2.60043889284134E-05
EndTime            : 5/16/2016 5:30:00 PM
PoolId             : MyPool
StartTime          : 5/16/2016 5:00:00 PM
TotalCoreHours     : 12
VirtualMachineSize : standard_d4
```

Эта команда возвращает метрики использования для пула с именем ContosoPool.
Команда задает строку фильтра для задания пула и использует то же значение $Context, что и в предыдущем примере.

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

### -EndTime
Указывает конец интервала времени, для которого этот командлет получает метрики использования.
Укажите время по крайней мере два часа раньше.
Если время окончания не задано, в этом командлете используется последний из доступных интервалов агрегатов.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Фильтр
Задает предложение фильтра OData, которое используется для фильтрации метрик, которые этот командлет retruns.
Единственным допустимым свойством **poolId** является строковое значение.
Возможны следующие операции: EQ, GE, gt, Le, lt, StartsWith.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartTime
Задает начало интервала времени, в течение которого этот командлет получает метрики использования.
Укажите время в интервале времени не менее двух и не более чем на полчаса.
Если время начала не задано, в этом командлете используется последний из доступных интервалов агрегатов.

```yaml
Type: DateTime
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

### BatchAccountContext
Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.

## НАПРЯЖЕНИЕ

### PSPoolUsageMetrics

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Get-AzureBatchPoolStatistics](./Get-AzureBatchPoolStatistics.md)

[Get-AzureBatchJobStatistics](./Get-AzureBatchJobStatistics.md)


