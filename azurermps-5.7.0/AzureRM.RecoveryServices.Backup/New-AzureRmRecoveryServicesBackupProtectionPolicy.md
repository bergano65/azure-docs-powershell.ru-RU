---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/new-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/New-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/New-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: e9834236a72a68f64cc9b19d6576e56102f96b13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558912"
---
# New-AzureRmRecoveryServicesBackupProtectionPolicy

## КРАТКИй обзор
Создание политики защиты резервных копий.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
New-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzureRmRecoveryServicesBackupProtectionPolicy** создает политику защиты резервного копирования в хранилище.
Политика защиты связана по крайней мере с одной политикой хранения.
Политика хранения определяет, как долго будет храниться резервная копия Azure.

Вы можете использовать командлет Get-AzureRmRecoveryServicesBackupRetentionPolicyObject, чтобы получить политику хранения по умолчанию.
Вы также можете использовать командлет Get-AzureRmRecoveryServicesBackupSchedulePolicyObject для получения политики расписания по умолчанию.
Объекты **SchedulePolicy** и **RetentionPolicy** используются в качестве входных данных для командлета **New-AzureRmRecoveryServicesBackupProtectionPolicy** .

Настройте контекст хранилища с помощью командлета Set-AzureRmRecoveryServicesVaultContext, прежде чем использовать текущий командлет.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Создание политики защиты резервных копий
```
PS C:\> $SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Dt = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($Dt.ToUniversalTime())
PS C:\> $RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

Первая команда получает базовый **SchedulePolicyObject** и сохраняет ее в переменной $SchPol.

Вторая команда удаляет все запланированные значения времени выполнения из политики расписания в $SchPol.

Третья команда использует командлет Get-Date, чтобы получить текущую дату и время.

Четвертая команда добавляет текущую дату и время в $Dt как запланированное время выполнения для политики расписания.

Пятая команда получает базовый объект **RetentionPolicy** , а затем сохраняет его в переменной $RetPol.

Шестая команда задает для политики продолжительность хранения 365 дней.

Последняя команда создает объект **BackupProtectionPolicy** на основе политики расписания и хранения, созданной предыдущими командами.

## ПАРАМЕТРЫ

### -BackupManagementType
Указывает тип управления резервным копированием.
Для этого параметра допустимы следующие значения:

- AzureVM 
- AzureSQLDatabase

```yaml
Type: BackupManagementType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Name (имя)
Указывает имя политики.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RetentionPolicy
Указывает базовый объект **RetentionPolicy** .
Вы можете использовать командлет Get-AzureRmRecoveryServicesBackupRetentionPolicyObject, чтобы получить объект **RetentionPolicy** .

```yaml
Type: RetentionPolicyBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SchedulePolicy
Указывает базовый объект **SchedulePolicy** .
Вы можете использовать командлет Get-AzureRmRecoveryServicesBackupSchedulePolicyObject, чтобы получить объект **SchedulePolicy** .

```yaml
Type: SchedulePolicyBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WorkloadType
Указывает тип рабочей нагрузки.
Для этого параметра допустимы следующие значения:

- AzureVM 
- AzureSQLDatabase

```yaml
Type: WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Запрашивает подтверждение перед запуском командлета.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске командлета. Командлет не выполняется.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

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
Этот командлет не поддерживает никаких входных данных.

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. PolicyBase

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Enable-AzureRmRecoveryServicesBackupProtection](./Enable-AzureRmRecoveryServicesBackupProtection.md)

[Get-AzureRmRecoveryServicesBackupProtectionPolicy](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[Get-AzureRmRecoveryServicesBackupRetentionPolicyObject](./Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md)

[Get-AzureRmRecoveryServicesBackupSchedulePolicyObject](./Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md)

[Remove-AzureRmRecoveryServicesBackupProtectionPolicy](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[Set-AzureRmRecoveryServicesBackupProtectionPolicy](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


