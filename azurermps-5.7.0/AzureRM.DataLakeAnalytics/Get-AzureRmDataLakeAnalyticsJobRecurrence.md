---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsjobrecurrence
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobRecurrence.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobRecurrence.md
ms.openlocfilehash: 34d2921526f54e20697a11cf17708fef50e49fc2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561860"
---
# Get-AzureRmDataLakeAnalyticsJobRecurrence

## КРАТКИй обзор
Возвращает повторение или повторения задания Data Lake Analytics.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### GetAllInAccount (по умолчанию)
```
Get-AzureRmDataLakeAnalyticsJobRecurrence [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetBySpecificJobRecurrence
```
Get-AzureRmDataLakeAnalyticsJobRecurrence [-Account] <String> [-RecurrenceId] <Guid>
 [-SubmittedAfter <DateTimeOffset>] [-SubmittedBefore <DateTimeOffset>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Элемент **Get-AzureRmDataLakeAnalyticsJobRecurrence** возвращает указанное повторение задания Azure Data Lake Analytics или список повторений.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение указанного повторения
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobRecurrence -Account "contosoadla" -RecurrenceId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

Эта команда получает повторение указанной задачи с идентификатором "83cb7ad2-3523-4b82-b909-d478b0d8aea3" в учетной записи "contosoadla".

### Пример 2: получение списка всех повторений в учетной записи
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobRecurrence -AccountName "contosoadla"
```

Эта команда возвращает список всех повторений в учетной записи "contosoadla"

## ПАРАМЕТРЫ

### -Account (учетная запись)
Имя учетной записи Data Lake Analytics, под которой требуется получить повторение задачи.

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

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

### -RecurrenceId
Идентификатор определенного повторения задания, сведения о котором нужно вернуть.

```yaml
Type: Guid
Parameter Sets: GetBySpecificJobRecurrence
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -SubmittedAfter
Необязательный фильтр, возвращающий повторения заданий, отправленные только по истечении заданного времени.

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubmittedBefore
Необязательный фильтр, возвращающий повторение заданий (-ов), отправленных только до указанного времени.

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String
System. GUID

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. DataLakeAnalytics. Models. PSJobRecurrenceInformation

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

