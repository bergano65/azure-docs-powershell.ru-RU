---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/invoke-azurermoperationalinsightsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Invoke-AzureRmOperationalInsightsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Invoke-AzureRmOperationalInsightsQuery.md
ms.openlocfilehash: e3bfdd771413f17d4dd560a350d45fdb3f47c5a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560227"
---
# Invoke-AzureRmOperationalInsightsQuery

## КРАТКИй обзор
Возвращает результаты поиска на основе указанных параметров.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### ByWorkspaceId (по умолчанию)
```
Invoke-AzureRmOperationalInsightsQuery -WorkspaceId <String> -Query <String> [-Timespan <TimeSpan>]
 [-Wait <Int32>] [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByWorkspaceObject
```
Invoke-AzureRmOperationalInsightsQuery -Workspace <PSWorkspace> -Query <String> [-Timespan <TimeSpan>]
 [-Wait <Int32>] [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Invoke-AzureRmOperationalInsightsQuery** возвращает результаты поиска на основе указанных параметров.

Вы можете получить доступ к статусу поиска в свойстве Metadata возвращаемого объекта.
Если состояние имеет значение ожидание, поиск не закончится, и результаты будут отправлены из архива.

Результаты поиска можно получить из свойства Value возвращаемого объекта.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение результатов поиска с помощью запроса
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $queryResults.Results
...
```

После вызова $queryResults. Results будет содержать все результирующие строки из запроса.

### Пример 2: Convert $results. Результат IEnumberable с массивом
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $resultsArray = [System.Linq.Enumerable]::ToArray($results.Results)
...
```

Некоторые запросы могут привести к возврату очень больших наборов данных. По этой причине по умолчанию командлет возвращает интерфейс IEnumerable, чтобы снизить стоимость памяти. Если вы предпочитаете получить массив результатов, можно использовать метод расширения LINQ Enumerable. ToArray () для преобразования IEnumerable в массив.

### Пример 3: получение результатов поиска с помощью запроса за определенный период времени
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -Timespan (New-TimeSpan -Hours 24)
PS C:\> $queryResults.Results
...
```

Результаты из этого запроса будут ограничены на последние 24 часа.

### Пример 4: включение статистики & отображения в результатах запроса
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -IncludeRender -IncludeStatistics
PS C:\> $queryResults.Results
...
PS C:\> $queryResults.Render
...
PS C:\> $queryResults.Statistics
...
```

[https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions)Подробнее об отображении и сведениях о статистике см.

## ПАРАМЕТРЫ

### -AsJob
Выполнить командлет в фоновом режиме
```yaml
Type: SwitchParameter
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeRender
Если задано, сведения о отрисовке запросов метрик будут включены в ответ.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeStatistics
Если задано значение, статистика запроса будет включена в ответ.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Query
Запрос, который необходимо выполнить.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TimeSpan
Интервал времени, по которому необходимо выполнить запрос.

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Wait
Применяет верхнюю границу к количеству времени, которое сервер тратит на обработку запроса.
Обнаружить https://dev.loganalytics.io/documentation/Using-the-API/Timeouts

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Рабочая область
Рабочая область

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WorkspaceId
ИДЕНТИФИКАТОР рабочей области.

```yaml
Type: String
Parameter Sets: ByWorkspaceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace
Если вы перейдете, идентификатор рабочей области извлекается из PSWorkspace. В противном случае можно задать идентификатор рабочей области вручную с помощью параметра workspaceId.

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. OperationalInsights. Models. PSQueryResponse
***PSQueryResponse*** отображает результаты, выводятся & статистики запроса.

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

