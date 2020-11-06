---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/export-azurermloganalyticthrottledrequests
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Export-AzureRmLogAnalyticThrottledRequests.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Export-AzureRmLogAnalyticThrottledRequests.md
ms.openlocfilehash: 97f68475ab935df66b67f0cab92466e68732a735
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561104"
---
# Export-AzureRmLogAnalyticThrottledRequests

## КРАТКИй обзор
Экспорт журналов, показывающих общее число запросов API для подписки в заданном окне времени.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Export-AzureRmLogAnalyticThrottledRequests [-GroupByOperationName] [-FromTime] <DateTime>
 [-GroupByThrottlePolicy] [-BlobContainerSasUri] <String> [-GroupByResourceName] [-ToTime] <DateTime>
 [-Location] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Это экспортирует общее количество запросов API Microsoft. COMPUTE.
Журналы можно дополнительно объединять тремя вариантами: GroupByOperationName, GroupByThrottlePolicy или GroupByResourceName.
Обратите внимание, что этот командлет собирает только CRP журналы.

Общие сведения о регулировании API поставщика ресурсов вычислительной среды содержатся в разделе https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits . 

## ИЛЛЮСТРИРУЮТ

### Пример 1
```
PS C:\> Export-AzureRmLogAnalyticThrottledRequests -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

Эта команда хранит общее число вызовов API Microsoft. COMPUTE между 2018-02-20T17:54:14 и 2018-02-22T17:54:17 в заданном URI SAS, агрегированные по названию операции.

## ПАРАМЕТРЫ

### -AsJob
Выполнить командлет в фоновом режиме

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

### -BlobContainerSasUri
Универсальный код ресурса (URI) SAS контейнера BLOB-объектов для ведения журнала, на который LogAnalytics API записывает выходные файлы.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
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

### -FromTime
Время выполнения запроса

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GroupByOperationName
Результат запроса группировки по имени операции.

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

### -GroupByResourceName
Результат запроса Group по названию ресурса.

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

### -GroupByThrottlePolicy
Результаты запроса на группировку по политике регулирования.

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

### -Location
Место, на которое запрашивается аналитический журнал.

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

### -ToTime
Время запроса

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

### -Confirm
Запрашивает подтверждение перед запуском командлета.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске командлета.
Командлет не выполняется.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSLogAnalyticsOperationResult

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
