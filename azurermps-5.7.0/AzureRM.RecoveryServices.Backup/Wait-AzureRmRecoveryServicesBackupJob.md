---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: F671A7CC-2A27-460E-B064-2FBF1B9C6A0B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/wait-azurermrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Wait-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Wait-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: 651c1cd08f8a2c711a4a0cec16ddb965ccfa8211
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558903"
---
# Wait-AzureRmRecoveryServicesBackupJob

## КРАТКИй обзор
Ожидание завершения задания резервного копирования.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Wait-AzureRmRecoveryServicesBackupJob [-Job] <Object> [[-Timeout] <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Wait-AzureRmRecoveryServicesBackupJob** ожидает завершения задания резервного копирования Azure.
Задания резервного копирования могут занять много времени.
Если вы запускаете задание резервного копирования в составе сценария, может потребоваться принудительное ожидание завершения задания, прежде чем продолжить выполнение других задач.

Сценарий, включающий этот командлет, может быть более простым, чем тот, который опрашивает службу резервного копирования для задания состояния.

Настройте контекст хранилища с помощью командлета Set-AzureRmRecoveryServicesVaultContext, прежде чем использовать текущий командлет.

## ИЛЛЮСТРИРУЮТ

### Пример 1: ожидание завершения задания
```
PS C:\>
$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status InProgress
    $Job = $Jobs[0]
    while ( $Job.Status -ne Completed )
    {
       Write-Host "Waiting for completion..."
       Start-Sleep -Seconds 10
       $Job = Get-AzureRmBackAzureRmRecoveryServicesBackupJob -Job $Job
    }
   Write-Host "Done!"
    Waiting for completion... 
    Waiting for completion... 
    Waiting for completion... 
    Done!
```

Этот сценарий опрашивает первое задание, которое выполняется в данный момент, пока задание не будет завершено.

## ПАРАМЕТРЫ

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

### -Job
Указывает задание, которое нужно дождаться.
Чтобы получить объект **BackupJob** , используйте командлет Get-AzureRmRecoveryServicesBackupJob.

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Timeout
Задает максимальное время в секундах, в течение которого этот командлет ожидает завершения задания.
Рекомендуется указать значение времени ожидания.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### DataObject
Параметр "задание" принимает значение типа "Object" из конвейера

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. JobBase

### System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. JobBase]

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmRecoveryServicesBackupJob](./Get-AzureRmRecoveryServicesBackupJob.md)


