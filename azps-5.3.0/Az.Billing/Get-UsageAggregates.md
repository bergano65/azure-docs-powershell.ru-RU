---
external help file: Microsoft.Azure.PowerShell.Cmdlets.UsageAggregates.dll-Help.xml
Module Name: Az.Billing
ms.assetid: 52B3ECCB-80E5-4E16-954A-B83D0BDC7E22
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-usageaggregates
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-UsageAggregates.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-UsageAggregates.md
ms.openlocfilehash: 858966f5fb20f001dc21363875362673884fcc90
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519768"
---
# Get-UsageAggregates

## SYNOPSIS
Получает сведения об использовании подписки Azure.

## СИНТАКСИС

```
Get-UsageAggregates -ReportedStartTime <DateTime> -ReportedEndTime <DateTime>
 [-AggregationGranularity <AggregationGranularity>] [-ShowDetails <Boolean>] [-ContinuationToken <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
С **помощью cmdlet Get-UsageAggregates** можно агрегировать данные об использовании подписки Azure по следующим свойствам: 
- Время начала и окончания данных об использовании.
- Точность агрегирования ( ежедневно или почасовая).
- Детализация на уровне экземпляра для нескольких экземпляров одного и того же ресурса.
Для поиска согласованных результатов возвращаемая информация основана на том, когда ресурс Azure сообщил сведения об использовании.
Дополнительные сведения см. в справочнике azure Billing REST API https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) (Microsoft Developer Network библиотеке).

## ПРИМЕРЫ

### Пример 1. Извлечение данных подписки
```
PS C:\>Get-UsageAggregates -ReportedStartTime "5/2/2015" -ReportedEndTime "5/5/2015"
```

Эта команда извлекает данные об использовании подписки с 02.05.2015 по 05.05.2015.

## PARAMETERS

### -AggregationGranularity
Определяет точность агрегирования для данных.
Допустимые значения: ежедневно и почасово.
Значение по умолчанию — "Ежедневно".

```yaml
Type: Microsoft.Azure.Commerce.UsageAggregates.Models.AggregationGranularity
Parameter Sets: (All)
Aliases:
Accepted values: Daily, Hourly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContinuationToken
Определяет маркер продолжения, полученный из ответа во время предыдущего вызова.
Для большого набора результатов ответы по страницам высвеяются с помощью маркеров продолжения.
Маркер продолжения служит закладкой для выполнения.
Если этот параметр не задан, данные извлекаются с начала дня или часа, указанного в *ReportedStartTime.*
Мы рекомендуем следующую ссылку в ответе на страницу с данными.

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

### -ReportedEndTime
Время окончания, указанное для записи использования ресурсов в системе вычитания Azure.
Azure — это распределенная система, охватывающая несколько центра обработки данных по всему миру, поэтому существует задержка между фактическим использованием ресурса, т. е. временем использования ресурса, и когда событие использования достигло системы вычитания ( это время, за которое было положено использование ресурсов).
Чтобы получить все события использования подписки, о чем сообщалось за период времени, вы можете сделать запрос по отчитаемой информации о времени.
Несмотря на то что запрос был запросчитано по времени, с помощью cmdlet можно агрегировать данные ответов по времени использования ресурсов.
Данные об использовании ресурсов удобно использовать для анализа данных.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportedStartTime
Время начала, указанное для записи использования ресурсов в системе вычитания Azure.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShowDetails
Указывает, возвращает ли этот cmdlet сведения на уровне экземпляра с данными об использовании.
Значение по умолчанию — $True.
Если $False, служба собирает результаты на стороне сервера и возвращает меньше групп.
Например, если вы работаете на трех веб-сайтах, по умолчанию вы получите три строки для использования веб-сайтов.
Однако если значение $False, все данные для одного и того же **subscriptionId,** **meterId,** **usageStartTime** и **usageEndTime** свернуты в один элемент строки.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Нет

## OUTPUTS

### Microsoft.Azure.Commerce.UsageAggregates.Models.UsageAggregationGetResponse

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ
