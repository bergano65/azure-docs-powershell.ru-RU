---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: 3fb6b89f5708c951731c45e0d32e0f7a379cf754
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569263"
---
# Get-AzureRmRecoveryServicesBackupJob

## КРАТКИй обзор
Получает задания резервного копирования.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Get-AzureRmRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmRecoveryServicesBackupJob** получает задания резервного копирования Azure для определенного хранилища.

Настройте контекст хранилища с помощью командлета Set-AzureRmRecoveryServicesVaultContext, прежде чем использовать текущий командлет.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение всех выполняемых заданий
```
PS C:\>$Joblist = Get-AzureRMRecoveryservicesBackupJob -Status Inprogress
PS C:\> $Joblist[0]
WorkloadName     Operation            Status               StartTime                 EndTime                                             
------------     ---------            ------               ---------                 -------                                             
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

Первая команда получает состояние выполняющегося задания в виде массива, а затем сохраняет его в переменной $Joblist.

Вторая команда отображает первый элемент в массиве $Joblist.

### Пример 2: получение всех невыполненных заданий за последние 7 дней
```
PS C:\>Get-AzureRmRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed
```

Эта команда возвращает задания с ошибкой за последнюю неделю в хранилище.
Параметр *from* указывает время, семь дней в прошлом, указанное в формате UTC.
В команде не указывается значение параметра " *Кому* ".
Таким образом, используется значение по умолчанию для текущего времени.

### Пример 3: получение выполняющегося задания и ожидание завершения
```
PS C:\> 
$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status InProgress
$Job = $Jobs[0]
    while ( $Job.Status -ne Completed )
    {
       Write-Host "Waiting for completion..."
       Start-Sleep -Seconds 10
       $job = Get-AzureRmBackAzureRmRecoveryServicesBackupJob  -Job $Job
    }
    Write-Host "Done!"
    Waiting for completion... 
    Waiting for completion... 
    Waiting for completion... 
    Done!
```

Этот сценарий опрашивает первое задание, которое выполняется в данный момент, пока задание не будет завершено.

## ПАРАМЕТРЫ

### -BackupManagementType
Указывает тип управления резервным копированием.
В настоящее время поддерживается только AzureVM.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -From
Задает начало в качестве объекта **DateTime** для диапазона времени для задач, которые получает этот командлет.
Чтобы получить объект **DateTime** , используйте командлет Get-Date.
Чтобы получить дополнительные сведения о объектах **DateTime** , введите `Get-Help Get-Date` .
Используйте формат UTC для дат.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Job
Указывает имя задания резервного копирования, которое требуется получить.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobId
Указывает идентификатор задания, которое получает этот командлет.
Идентификатор — это свойство InstanceId объекта **AzureRmRecoveryServicesBackupJob** .
Чтобы получить объект **AzureRmRecoveryServicesBackupJob** , используйте Get-AzureRmRecoveryServicesBackupJob.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Эксплуатация
Указывает операцию заданий, которые получает этот командлет.
Для этого параметра допустимы следующие значения:

- Копирование
- ConfigureBackup
- DeleteBackupData
- Отменить
- Восстановление
- Снять защиту
- Отмените регистрацию

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobOperation]
Parameter Sets: (All)
Aliases: 
Accepted values: Backup, Restore, ConfigureBackup, DisableBackup, DeleteBackupData

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Status (состояние)
Указывает состояние заданий, которые получает этот командлет.
Для этого параметра допустимы следующие значения:

- Ход выполнения
- Ошибкой
- Отменен
- Отмена
- Completed
- CompletedWithWarnings

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobStatus]
Parameter Sets: (All)
Aliases: 
Accepted values: InProgress, Cancelling, Cancelled, Completed, CompletedWithWarnings, Failed

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -To
Задает конечный объект в качестве объекта **DateTime** из диапазона времени для задач, которые получает этот командлет.
Значение по умолчанию — текущее системное время.
Если указать этот параметр, необходимо также указать параметр *from* .
Используйте формат UTC для дат.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. JobBase

### System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. JobBase]

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmRecoveryServicesBackupJobDetails](./Get-AzureRmRecoveryServicesBackupJobDetails.md)

[Остановить-AzureRmRecoveryServicesBackupJob](./Stop-AzureRmRecoveryServicesBackupJob.md)

[Wait-AzureRmRecoveryServicesBackupJob](./Wait-AzureRmRecoveryServicesBackupJob.md)


