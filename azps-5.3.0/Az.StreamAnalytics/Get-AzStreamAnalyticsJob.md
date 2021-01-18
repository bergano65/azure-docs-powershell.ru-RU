---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1D10C1EA-632A-4953-85B1-596A45C30B24
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
ms.openlocfilehash: 826089ca0db48e89138e9df78f0aa483b110ba30
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98516994"
---
# Get-AzStreamAnalyticsJob

## SYNOPSIS
Получает сведения о заданиях в stream Analytics.

## СИНТАКСИС

### ByResourceGroup
```
Get-AzStreamAnalyticsJob [-ResourceGroupName] <String> [[-Name] <String>] [-NoExpand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### BySubscription
```
Get-AzStreamAnalyticsJob [-NoExpand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
В **этом** списке перечислены все задания аналитики Stream, определенные в подписке Azure или указанной группе ресурсов, а также сведения об определенном задании в группе ресурсов.

## ПРИМЕРЫ

### ПРИМЕР 1. Просмотр сведений обо всех заданиях в подписке
```
PS C:\>Get-AzStreamAnalyticsJob
```

Эта команда возвращает сведения обо всех заданиях аналитики Stream в подписке Azure.

### ПРИМЕР 2. Просмотр сведений обо всех заданиях в группе ресурсов
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US"
```

Эта команда возвращает сведения обо всех заданиях Аналитики StreamAnalytics в группе ресурсов StreamAnalytics-Default-West-US.

### ПРИМЕР 3. Просмотр сведений об определенном заданиях в группе ресурсов
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

Эта команда возвращает сведения о streamingJob задания Stream Analytics в группе ресурсов StreamAnalytics-Default-West-US.

## PARAMETERS

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

### -Name
Указывает имя задания Azure Stream Analytics, которое нужно извлечь.

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NoExpand
Указывает на то, что он получит задание Azure Stream Analytics, но не будет возвращать сведения о входных данных, результатах и преобразовании.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов, к которой относится задание Azure Stream Analytics.

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

### System.Management.Automation.SwitchParameter

## OUTPUTS

### Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[New-AzStreamAnalyticsJob](./New-AzStreamAnalyticsJob.md)

[Remove-AzStreamAnalyticsJob](./Remove-AzStreamAnalyticsJob.md)

[Start-AzStreamAnalyticsJob](./Start-AzStreamAnalyticsJob.md)

[Stop-AzStreamAnalyticsJob](./Stop-AzStreamAnalyticsJob.md)


