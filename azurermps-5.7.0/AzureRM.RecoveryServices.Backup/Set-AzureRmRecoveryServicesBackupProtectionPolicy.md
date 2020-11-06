---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/set-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Set-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Set-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 5a60320736e65fae83547bbf9b2825979f73601e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558908"
---
# Set-AzureRmRecoveryServicesBackupProtectionPolicy

## КРАТКИй обзор
Изменение политики защиты резервных копий.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Set-AzureRmRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase>
 [[-RetentionPolicy] <RetentionPolicyBase>] [[-SchedulePolicy] <SchedulePolicyBase>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzureRmBackupProtectionPolicy** изменяет существующую политику защиты резервного копирования Azure.
Вы можете изменить расписание архивации и компоненты политики хранения.

Все внесенные изменения повлияют на резервное копирование и хранение элементов, связанных с политикой.

Настройте контекст хранилища с помощью командлета Set-AzureRmRecoveryServicesVaultContext, прежде чем использовать текущий командлет.

## ИЛЛЮСТРИРУЮТ

### Пример 1: изменение политики защиты резервной копии
```
PS C:\>$SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> $RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $Pol = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Set-AzureRmRecoveryServicesBackupProtectionPolicy -Policy $Pol -SchedulePolicy $SchPol -RetentionPolicy $RetPol
```

Первая команда получает базовый объект SchedulePolicy, а затем сохраняет его в переменной $SchPol.

Вторая команда удаляет все запланированные значения времени выполнения из политики расписания в $SchPol.

Третья команда использует командлет Get-Date, чтобы получить текущую дату и время, а затем сохраняет их в переменной $DT.

Четвертая команда добавляет дату и время в $DT к времени выполнения расписания для политики расписания.

Пятое приложение получает базовый объект политики хранения и сохраняет его в переменной $RetPol.

Шестая команда задает продолжительность хранения в 365 дней.

Седьмая команда получает политику защиты резервного копирования с именем NewPolicy и сохраняет ее в переменной $Pol.

Последняя команда изменяет политику защиты резервных копий в $Pol с помощью политики расписания в $SchPol и политики хранения в $RetPol.

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

### -Policy (политика)
Задает политику защиты резервного копирования, которую изменяет этот командлет.
Чтобы получить объект **BackupProtectionPolicy** , используйте командлет Get-AzureRmRecoveryServicesBackupProtectionPolicy.

```yaml
Type: PolicyBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RetentionPolicy
Указывает базовую политику хранения.
Чтобы получить объект **RetentionPolicy** , используйте командлет Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.

```yaml
Type: RetentionPolicyBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SchedulePolicy
Указывает базовый объект политики расписания.
Чтобы получить объект **SchedulePolicy** , используйте объект Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.

```yaml
Type: SchedulePolicyBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
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

### PolicyBase
Параметр "Policy" принимает значение типа "PolicyBase" из конвейера.

## НАПРЯЖЕНИЕ

### System. Collections. Generic. List "1 [Microsoft. Azure. командлеты. RecoveryServices. Backup. JobBase]

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmRecoveryServicesBackupProtectionPolicy](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[Get-AzureRmRecoveryServicesBackupRetentionPolicyObject](./Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md)

[New-AzureRmRecoveryServicesBackupProtectionPolicy](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[Remove-AzureRmRecoveryServicesBackupProtectionPolicy](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)


