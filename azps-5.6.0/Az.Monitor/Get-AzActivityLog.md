---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azactivitylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
ms.openlocfilehash: b966f15cc42ffc61f7d88cd5a1855f31564742ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980200"
---
# Get-AzActivityLog

## SYNOPSIS
Получить события журнала действий.

## СИНТАКСИС

### GetByCorrelationId
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByResourceId
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByResourceGroup
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceGroupName] <String> [-MaxRecord <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceProvider
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetBySubscription
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
Он Get-AzActivityLog получить события журнала действий. События могут быть связаны с текущим ИД подписки, корреляцией, группой ресурсов, ИД ресурса или поставщиком ресурсов.

## ПРИМЕРЫ

### Пример 1. Получить журнал событий по ИД подписки
```
PS C:\>Get-AzActivityLog
```

Эта команда содержит не более 1000 событий, связанных с ИД подписки пользователя, которые были за 7 дней от текущей даты и времени.

### Пример 2. Получите журнал событий по ИД подписки с максимальным количеством событий
```
PS C:\>Get-AzActivityLog -MaxRecord 100
```

Эта команда содержит не более 100 событий, связанных с ИД подписки пользователя, которые были за 7 дней от текущей даты и времени.

### Пример 3. Получите журнал событий по ИД подписки с временем начала.
```
PS C:\>Get-AzActivityLog -StartTime 2017-06-01T10:30
```

Эта команда содержит не более 1000 событий, связанных с ИД подписки пользователя, который прошел в 2017-06-01T10:30 по локальному времени или после него, если дата и время не старше 90 дней с текущей даты и времени.

### Пример 4. Получите журнал событий по ИД подписки с временем начала и окончания.
```
PS C:\>Get-AzActivityLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

Эта команда содержит не более 1000 событий, связанных с ИД подписки пользователя, которые произошли в 2017-04-01T10:30 по местному времени и до 2017-04-14T11:30 локального времени, если весь диапазон дат и времени не превышает 90 дней с текущего, то есть период хранения.

### Пример 5. Получить журнал событий по корреляции
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

Эта команда содержит не более 1000 событий, связанных с указанным ид корреляции, которые произошли за 7 дней от текущей даты и времени. 
**ПРИМЕЧАНИЕ.** Обычно это только одно событие.

### Пример 6. Получите журнал событий по ид корреляции с максимальным количеством событий
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxRecord 100
```

Эта команда содержит не более 100 событий, связанных с указанным ид корреляции, которые произошли за 7 дней от текущей даты и времени. 
**ПРИМЕЧАНИЕ.** Обычно это только одно событие.

### Пример 7. Получите журнал событий по корреляции и времени начала
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

Эта команда содержит не более 1000 событий, связанных с указанным id корреляции, которые произошли в 2017-05-22T04:30:00 локального времени, если время начала не прошло более 90 дней с текущей даты/времени.
**ПРИМЕЧАНИЕ.** Обычно это только одно событие.

### Пример 8. Получите журнал событий по ид корреляции со временем начала и окончания
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

Эта команда содержит не более 1000 событий, связанных с указанным ид корреляции, которые произошли в 2017-04-15T04:30 локального времени, но до 2017-04-25T12:30 локального времени, если весь диапазон дат и времени не был старше 90 дней с текущей даты/времени, то есть период хранения.

### Пример 9. Получить журнал событий для группы ресурсов
```
PS C:\>Get-AzActivityLog -ResourceGroupName "Contoso-Web-CentralUS"
```

Эта команда содержит не более 1000 событий, связанных с указанной группой ресурсов, которые были заданы за 7 дней от текущей даты и времени.

### Пример 10. Получите журнал событий для группы ресурсов с максимальным количеством событий
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -MaxRecord 100
```

Эта команда содержит не более 100 событий, связанных с указанной группой ресурсов, которые были заданы на 7 дней от текущей даты и времени.

### Пример 11. Получить журнал событий для группы ресурсов по времени начала
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

Эта команда содержит не более 1000 событий, связанных с указанной группой ресурсов, которые произошли в 2017-05-22T04:30:00 по локальному времени, если время начала не превышает 90 дней с текущей даты или времени.

### Пример 12. Получить журнал событий для группы ресурсов с временем начала и окончания
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

Эта команда содержит не более 1000 событий, связанных с указанной группой ресурсов, которые произошли в 2017-04-15T04:30 локального времени, но до 2017-04-25T12:30 локального времени, если весь диапазон дат и времени не превышает 90 дней с текущей даты/времени, то есть период хранения.

### Пример 13. Получить журнал событий по ИД ресурса
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

Эта команда содержит не более 1000 событий, связанных с указанным ИД ресурса, которые были заданы за 7 дней от текущей даты и времени.

### Пример 14. Получите журнал событий по ИД ресурса с максимальным количеством событий
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxRecord 100
```

Эта команда содержит не более 100 событий, связанных с указанным ИД ресурса, которые были заданы на 7 дней от текущей даты и времени.

### Пример 15. Получить журнал событий по ИД ресурса с временем начала
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

Эта команда содержит не более 1000 событий, связанных с указанным ИД ресурса, которые произошли в 2017-05-22T04:30:00 по локальному времени, если время начала не старше 90 дней с текущей даты и времени.

### Пример 16. Получите журнал событий по ИД ресурса с временем начала и окончания
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

Эта команда содержит не более 1000 событий, связанных с указанным ИД ресурса, которые произошли в 2017-04-15T04:30 локального времени, но до 2017-04-25T12:30 локального времени, если весь диапазон дат и времени не превышает 90 дней с текущего, то есть период хранения.

### Пример 17. Получить журнал событий от поставщика ресурсов
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web"
```

Эта команда содержит не более 1000 событий, связанных с указанным поставщиком ресурсов, которые прошли 7 дней с текущей даты и времени.

### Пример 18. Получите журнал событий от поставщика ресурсов с максимальным количеством событий
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -MaxRecord 100
```

Эта команда содержит не более 100 событий, связанных с указанным поставщиком ресурсов, которые были заданы на 7 дней от текущей даты и времени.

### Пример 19. Получить журнал событий от поставщика ресурсов с временем начала
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

Эта команда содержит не более 1000 событий, связанных с указанным поставщиком ресурсов, которые произошли в 2017-05-22T04:30:00 по локальному времени, если время начала не превышает 90 дней с текущей даты/времени.

### Пример 20. Получить журнал событий от поставщика ресурсов с временем начала и окончания
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

Эта команда содержит не более 1000 событий, связанных с указанным поставщиком ресурсов, которые произошли в локальное время с 04.04.2017 по 15.04.30, но до 2017-04-25T12:30 локального времени, если весь диапазон дат и времени не превышает 90 дней с текущей даты или времени, то есть период хранения.

## PARAMETERS

### -Caller
The caller of the events to fetch

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CorrelationId
The CorrelationId

```yaml
Type: System.String
Parameter Sets: GetByCorrelationId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -DetailedOutput
Возврат объекта со всеми сведениями о событиях (по умолчанию возвращает только некоторые атрибуты, то есть без подробностей)

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EndTime
Время окончания запроса

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxRecord
Максимальное количество записей для выборки.
Псевдоним: MaxRecords, MaxEvents

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
The ResourceId

```yaml
Type: System.String
Parameter Sets: GetByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceProvider
Имя ресурса

```yaml
Type: System.String
Parameter Sets: GetByResourceProvider
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StartTime
CorrelationId запроса

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Status
Состояние событий, извлекаемого

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.String

### System.Management.Automation.SwitchParameter

### System.Int32

## OUTPUTS

### Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ
