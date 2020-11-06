---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 856B76FC-88ED-4A29-9DC6-C482398D702E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Restore-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Restore-AzureRmBackupItem.md
ms.openlocfilehash: b449b96417f0ac05fa857a48a10143a285ed888f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560511"
---
# Restore-AzureRmBackupItem

## КРАТКИй обзор
Восстанавливает данные и конфигурацию элемента резервного копирования в точку восстановления.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Restore-AzureRmBackupItem [-StorageAccountName] <String> [-RecoveryPoint] <AzureRMBackupRecoveryPoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **RESTORE-AzureRmBackupItem** восстанавливает данные и конфигурацию элемента резервного копирования Azure для указанной точки восстановления.
Этот командлет запускает восстановление из резервного хранилища в учетную запись.

Операция восстановления не восстанавливает полную виртуальную машину.
Она восстанавливает данные о дисках и сведения о конфигурации.
После завершения операции восстановления необходимо создать виртуальную машину и запустить ее.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Восстановление виртуальной машины в точке восстановления
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> $BackupItem = Get-AzureRmBackupItem -Container $Container
PS C:\> $RecoveryPoint = Get-AzureRmBackupRecoveryPoint -Item $BackupItem 
PS C:\> Restore-AzureRmBackupItem -StorageAccountName "DestinationAccount" -RecoveryPoint $RecoveryPoint 
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Restore         InProgress      26-Aug-15 1:14:01 PM   01-Jan-01 12:00:00 AM
```

Первая команда получает хранилище с именем Vault03 с помощью командлета Get-AzureRmBackupVault.
Команда сохраняет этот объект в переменной $Vault.

Вторая команда получает контейнер с указанным именем в хранилище $Vault с помощью командлета **Get-AzureRmBackupContainer** .
Команда сохраняет этот объект в переменной $Container.

Третья команда возвращает элемент резервного копирования в контейнере $Container с помощью командлета **Get-AzureRmBackupItem** .
Команда сохраняет этот объект в переменной $BackupItem.

Четвертая команда получает точку восстановления для элемента в $BackupItem.
Команда сохраняет этот объект в переменной $RecoveryPoint.

Последняя команда восстанавливает точку восстановления в $RecoveryPoint для учетной записи с именем DestinationAccount.

## ПАРАМЕТРЫ

### -RecoveryPoint
Указывает точку восстановления, в которую нужно восстановить виртуальную машину.
Чтобы получить **AzureRmBackupRecoveryPoint** , используйте командлет Get-AzureRmBackupRecoveryPoint.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupRecoveryPoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -StorageAccountName
Указывает имя целевой учетной записи хранения в подписке.
В ходе процесса восстановления этот командлет сохраняет диски и сведения о конфигурации в этой учетной записи хранения.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
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

### AzureRmBackupRecoveryPoint

## НАПРЯЖЕНИЕ

### AzureRmBackupJob

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Backup-AzureRmBackupItem](./Backup-AzureRmBackupItem.md)

[Get-AzureRmBackupItem](./Get-AzureRmBackupItem.md)

[Get-AzureRmBackupRecoveryPoint](./Get-AzureRmBackupRecoveryPoint.md)


