---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/export-azloganalyticrequestratebyinterval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
ms.openlocfilehash: feae2282f6b989b8d595b2a51cd147975e689174
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969411"
---
# Export-AzLogAnalyticRequestRateByInterval

## SYNOPSIS
Экспортировать журналы, в которые в заданное время будут экспортироваться запросы API, сделанные этой подпиской, для демонстрации действий регулирования.

## СИНТАКСИС

```
Export-AzLogAnalyticRequestRateByInterval [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-IntervalLength] <IntervalInMins> [-GroupByOperationName]
 [-GroupByResourceName] [-GroupByThrottlePolicy] [-GroupByApplicationId] [-GroupByUserAgent] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## ОПИСАНИЕ
Экспорт статистических данных о вызовах подписки в API Microsoft.Compute с учетом успешности, сбоя или состояния регулирования заранее определенные интервалы времени. Журналы можно дополнительно сгруппировать по пяти параметрам: GroupByOperationName, GroupByThrottlePolicy, GroupByResourceName, GroupByUserAgent или GroupByApplicationId.
Обратите внимание, что этот cmdlet собирает только журналы поставщиков ресурсов Compute; кроме того, данные о типах ресурсов "Диск" и "Моментальный снимок" пока недоступны.

Обзор регулирования API поставщика ресурсов для компьютеров см. в . https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-request-limits 

## ПРИМЕРЫ

### Пример 1. Экспорт записей, агрегированных по имени операции
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByOperationName
This command downloads a .csv file to the provided container. The format of the file is:

TIMESTAMP             operationName   TotalRequests SuccessfulRequests ThrottledRequests
---------             -------------   ------------- ------------------ -----------------
2/21/2018  7:00:00 PM <operationName> 10            10                 0
2/21/2018  7:30:00 PM <operationName> 8             8                  0
2/21/2018  9:00:00 PM <operationName> 9             9                  0

```

Эта команда хранит агрегированные номера звонков API Microsoft.Compute, разделенные на успех, сбой или регулирование между 2018-02-20T17:54:14 and 2018-02-22T17:54:17 в URI SAS, агрегированном по имени операции.

### Пример 2. Экспорт записей, агрегированных по id приложения
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByApplicationId

This command downloads a .csv file to the provided container. The format of the file is:

TIMESTAMP             clientApplicationId   TotalRequests SuccessfulRequests ThrottledRequests
---------             -------------------   ------------- ------------------ -----------------
2/21/2018  7:00:00 PM <clientApplicationId> 10            10                 0
2/21/2018  7:30:00 PM <clientApplicationId> 8             8                  0
2/21/2018  9:00:00 PM <clientApplicationId> 9             9                  0

```

Эта команда хранит совокупные номера звонков API Microsoft.Compute, разделенные на успех, сбой или регулирование между 2018-02-20T17:54:14 и 2018-02-22T17:54:17 в URI SAS, агрегированном по id приложения. 

### Пример 3. Экспорт записей, агрегированных агентом пользователя
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByUserAgent
This command downloads a .csv file to the provided container. The format of the file is:

TIMESTAMP             userAgent   TotalRequests SuccessfulRequests ThrottledRequests
---------             ---------   ------------- ------------------ -----------------
2/21/2018  7:00:00 PM <userAgent> 10            10                 0
2/21/2018  7:30:00 PM <userAgent> 8             8                  0
2/21/2018  9:00:00 PM <userAgent> 9             9                  0

```

Эта команда хранит агрегированные номера звонков API Microsoft.Compute, разделенные на успех, сбой или регулирование между 2018-02-20T17:54:14 и 2018-02-22T17:54:17 в URI SAS, обобщенном агентом пользователя. 

## PARAMETERS

### -AsJob
Запуск cmdlet в фоновом режиме

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
SAS Uri контейнера BLOB-приложений, в который LogAnalytics Api записывает журналы вывода.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
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

### -FromTime
Со времени запроса

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GroupByApplicationId
Результат группового запроса по ИД приложения.

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

### -GroupByOperationName
Результат запроса группы по имени операции.

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
Результат запроса группы по имени ресурса.

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
Результат группового запроса с примененной политикой Throttle.

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

### -GroupByUserAgent
Результат запроса группы по userAgent.

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

### -IntervalLength
Значение интервала в минутах, используемом для создания журналов вызовов LogAnalytics.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.IntervalInMins
Parameter Sets: (All)
Aliases:
Accepted values: ThreeMins, FiveMins, ThirtyMins, SixtyMins

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location
Расположение, для которого запрашивается аналитический журнал.

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

### -NoWait
Начинает операцию и возвращает ее немедленно до ее завершения. Чтобы определить успешное завершение операции, используйте другой механизм.

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

### -ToTime
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

### -Confirm
Запрос на подтверждение перед запуском cmdlet.

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
Показывает, что произойдет при запуске cmdlet.
Этот cmdlet не будет выполниться.

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
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

## OUTPUTS

### Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ
