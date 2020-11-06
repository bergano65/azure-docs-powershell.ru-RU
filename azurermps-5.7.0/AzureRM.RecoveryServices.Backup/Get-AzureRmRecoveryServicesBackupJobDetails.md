---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupjobdetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJobDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJobDetails.md
ms.openlocfilehash: 133a779a1227c74830fdae69b52db321a63a12e6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558947"
---
# Get-AzureRmRecoveryServicesBackupJobDetails

## КРАТКИй обзор
Получение сведений о задании резервного копирования.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### JobFilterSet (по умолчанию)
```
Get-AzureRmRecoveryServicesBackupJobDetails [-Job] <JobBase> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### IdFilterSet
```
Get-AzureRmRecoveryServicesBackupJobDetails [-JobId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmRecoveryServicesBackupJobDetails** получает сведения о задании резервного копирования Azure для указанного задания.

Настройте контекст хранилища с помощью командлета Set-AzureRmRecoveryServicesVaultContext, прежде чем использовать текущий командлет.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение сведений о задании резервного копирования для невыполненных заданий
```
PS C:\>$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status Failed
PS C:\> $JobDetails = Get-AzureRmRecoveryServicesBackupJobDetails -Job $Jobs[0]
PS C:\> $JobDetails.ErrorDetails
```

Первая команда получает массив невыполненных заданий в хранилище, а затем сохраняет их в массиве $Jobs.

Вторая команда возвращает сведения о задании для заданий, завершившихся сбоем, в $Jobs, а затем сохраняет их в переменной $JobDetails.

В последней команде отображаются сведения об ошибке для заданий, завершившихся сбоем.

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
Указывает задание, которое требуется получить.
Чтобы получить объект **BackupJob** , используйте командлет Get-AzureRmRecoveryServicesBackupJob.

```yaml
Type: JobBase
Parameter Sets: JobFilterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobId
Указывает идентификатор задания резервного копирования.
Идентификатор — это свойство InstanceId объекта **BackupJob** .

```yaml
Type: String
Parameter Sets: IdFilterSet
Aliases: 

Required: True
Position: 2
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

### Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. JobBase

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmRecoveryServicesBackupJob](./Get-AzureRmRecoveryServicesBackupJob.md)


