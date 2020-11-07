---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: B5CA6FD9-49EE-4115-8477-551CE5D8E6CE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 2365b806bd274bb9cc18f84c83a29423408780d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732401"
---
# Get-AzureRmSiteRecoveryJob

## КРАТКИй обзор
Возвращает сведения о операции для текущего хранилища веб-сайтов.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### ByParam (по умолчанию)
```
Get-AzureRmSiteRecoveryJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByName
```
Get-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByObject
```
Get-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmSiteRecoveryJob** получает задания Azure Site Recovery.
Вы можете использовать этот командлет, чтобы просмотреть сведения об операции для текущего хранилища сайта для восстановления.

## ИЛЛЮСТРИРУЮТ

## ПАРАМЕТРЫ

### -EndTime
Указывает время окончания для заданий.
Этот командлет получает все задания, которые были запущены до указанного времени.
Чтобы получить объект **DateTime** для этого параметра, используйте командлет Get-Date.
Для получения дополнительных сведений введите `Get-Help Get-Date` .

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Job
Указывает задание восстановления сайта.

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (имя)
Задает уникальное имя, идентифицирующее задание.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartTime
Задает время начала для заданий.
Этот командлет получает все задания, которые были запущены по истечении заданного времени.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -State
Задает состояние ввода для задания по восстановлению сайта.
Этот командлет получает все задания, которые соответствуют указанному состоянию.
Для этого параметра допустимы следующие значения:

- NotStarted
- Ход выполнения
- LSP
- Другие
- Ошибкой
- Отменен
- Остановить

```yaml
Type: System.String
Parameter Sets: ByParam
Aliases: 
Accepted values: NotStarted, InProgress, Succeeded, Other, Failed, Cancelled, Suspended

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetObjectId
Указывает идентификатор объекта, для которого задано задание.

```yaml
Type: System.String
Parameter Sets: ByParam
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

### ASRJob
Параметр "задание" принимает значение типа "ASRJob" из конвейера.

## НАПРЯЖЕНИЕ

### System. Collections. Generic. IEnumerable 1 [Microsoft. Azure. Commands. SiteRecovery. ASRJob]

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Restarting-AzureRmSiteRecoveryJob](./Restart-AzureRmSiteRecoveryJob.md)

[Возобновить — AzureRmSiteRecoveryJob](./Resume-AzureRmSiteRecoveryJob.md)

[Остановить-AzureRmSiteRecoveryJob](./Stop-AzureRmSiteRecoveryJob.md)
