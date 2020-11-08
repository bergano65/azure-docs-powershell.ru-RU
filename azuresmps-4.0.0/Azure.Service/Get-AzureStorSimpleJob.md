---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 2001E040-5551-40C3-81D2-9A8334DE02BF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7692d4407df8fb4af8647ee0b4490abe73b2c937
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075558"
---
# Get-AzureStorSimpleJob

## КРАТКИй обзор
Получает задания StorSimple.

## Максимальное

```
Get-AzureStorSimpleJob [-DeviceName <String>] [-InstanceId <String>] [-Status <String>] [-Type <String>]
 [-From <DateTime>] [-To <DateTime>] [-Skip <Int32>] [-First <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureStorSimpleJob** получает задачи Azure StorSimple.
Укажите идентификатор экземпляра, чтобы получить конкретное задание.
Укажите другие параметры, чтобы ограничить задания, которые получает этот командлет.

Этот командлет возвращает не более 200 заданий.
Если существует более 200 заданий, получите оставшиеся задания с помощью параметров *First* и *Skip* .
Если задать значение 100 для параметра *пропустить* и 50 для *первого* , этот командлет не будет возвращать первые 100 результатов.
Функция возвращает следующие 50 результаты после пропуска 100.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение задания с помощью идентификатора
```
PS C:\>Get-AzureStorSimpleJob -InstanceId "574f47e0-44e9-495c-b8a5-0203c57ebf6d"
BackupPolicy             : 
BackupTimeStamp          : 1/1/0001 12:00:00 AM
BackupType               : CloudSnapshot
DataStats                : Microsoft.WindowsAzure.Management.StorSimple.Models.DataStatistics
Device                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
Entity                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
ErrorDetails             : {}
HideProgressDetails      : False
InstanceId               : 574f47e0-44e9-495c-b8a5-0203c57ebf6d
IsInstantRestoreComplete : False
IsJobCancellable         : True
JobDetails               : Microsoft.WindowsAzure.Management.StorSimple.Models.JobStatusInfo
Name                     : 26447caf-59bb-41c9-a028-3224d296c7dc
Progress                 : 100
SourceDevice             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
SourceEntity             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
SourceVolume             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
Status                   : Completed
TimeStats                : Microsoft.WindowsAzure.Management.StorSimple.Models.TimeStatistics
Type                     : Backup
Volume                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
```

Эта команда получает сведения о задании с указанным ИДЕНТИФИКАТОРом.

### Пример 2: получение заданий с помощью имени устройства
```
PS C:\>Get-AzureStorSimpleJob -DeviceName "8600-Bravo 001" -First 2
InstanceId                           Type                         Status                                          DeviceName                                      StartTime                                       Progress                                       
----------                           ----                         ------                                          ----------                                      ---------                                       --------                                       
1997c33f-bfcc-4d08-9aba-28068340a1f9 Backup                       Running                                         8600-Bravo 001                                  4/15/2015 1:30:02 PM                            92                                             
85074062-ef6a-408a-b6c9-2a0904bb99ca Backup                       Completed                                       8600-Bravo 001                                  4/15/2015 1:30:02 PM                            100
```

Эта команда получает сведения о заданиях для устройства с названием 8600-Bravo 001.
Команда получает первые два задания для устройства.

### Пример 3: Получение завершенных заданий
```
PS C:\>Get-AzureStorSimpleJob -Status "Completed" -Skip 10 -First 2
```

Эта команда получает выполненные задания.
Команда возвращает только первые два задания после пропуска первых десяти заданий.

### Пример 4: задания резервного копирования вручную
```
PS C:\>Get-AzureStorSimpleJob -Type "ManualBackup"
```

Эта команда получает задания типа резервного копирования вручную.

### Пример 5: получение заданий между определенным временем
```
PS C:\>$StartTime = Get-Date -Year 2015 -Month 3 -Day 10
PS C:\> $EndTime = Get-Date -Year 2015 -Month 3 -Day 11 -Hour 12 -Minute 15
PS C:\>Get-AzureStorSimpleJob -DeviceName "Device07" -From $StartTime -To $EndTime
```

Первые две команды создают объекты **DateTime** с помощью командлета Get-Date.
Команды хранят новые значения времен в переменных $StartTime и $EndTime.
Для получения дополнительных сведений введите `Get-Help Get-Date` .

Последняя команда получает задания для устройства с именем Device07 между временем, хранящимся в $StartTime и $EndTime.

## ПАРАМЕТРЫ

### -Имя_устройства
Указывает имя устройства StorSimple.

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

### -First
Возвращает только указанное количество объектов.
Введите количество получаемых объектов.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -From
Указывает дату и время начала выполнения заданий, которые получает этот командлет.

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

### -InstanceId
Указывает ИД задания, которое требуется получить.

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

### -Profile
Указывает профиль Azure, из которого считывается этот командлет.
Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Skip
Пропускает указанное количество объектов и возвращает оставшиеся объекты.
Введите количество объектов для пропуска.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Status (состояние)
Указывает состояние.
Для этого параметра допустимы следующие значения:

- Использующ
- Completed
- Отменен
- Ошибкой
- Отмены
- CompletedWithErrors

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

### -To
Задает конечную дату и время для задания, которое получает этот командлет.

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

### -Type (тип)
Указывает тип задания.
Для этого параметра допустимы следующие значения:

- Копирование
- ManualBackup
- Восстановление
- CloneWorkflow
- DeviceRestore
- Обновление
- SupportPackage
- VirtualApplianceProvisioning

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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего
Вы не можете передавать входные данные в этот командлет.

## НАПРЯЖЕНИЕ

### IList \<DeviceJobDetails\> , DeviceJobDetails
Этот командлет возвращает список объектов сведений о задании или, если указан параметр *InstanceId* , возвращает один объект детализации задания.

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Остановить-AzureStorSimpleJob](./Stop-AzureStorSimpleJob.md)


