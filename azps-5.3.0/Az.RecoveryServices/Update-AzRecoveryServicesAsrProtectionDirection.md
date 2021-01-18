---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectiondirection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: 326f73e0a056c6d68d0bdd96ddca1aea7c1c6147
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98516862"
---
# Update-AzRecoveryServicesAsrProtectionDirection

## SYNOPSIS
Обновляет направление репликации для указанного элемента, защищенного репликацией, или для плана восстановления. Используется для повторной защиты или репликации сбойной репликации по плану репликации или восстановления.

## СИНТАКСИС

### ByRPIObject (по умолчанию)
```
Update-AzRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AzureToVMware
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToVMware] [-Account <ASRRunAsAccount>]
 -DataStore <ASRDataStore> [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 -RetentionVolume <ASRRetentionVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### VMwareToAzure
```
Update-AzRecoveryServicesAsrProtectionDirection [-VMwareToAzure] -Account <ASRRunAsAccount>
 [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HyperVToAzure
```
Update-AzRecoveryServicesAsrProtectionDirection [-HyperVToAzure] [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### EnterpriseToEnterprise
```
Update-AzRecoveryServicesAsrProtectionDirection [-VmmToVmm]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AzureToAzure
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -LogStorageAccountId <String>
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryResourceGroupId <String>] [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-RecoveryBootDiagStorageAccountId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### AzureToAzureWithMultipleStorageAccount
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-RecoveryResourceGroupId <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-RecoveryBootDiagStorageAccountId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByRPObject
```
Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByPEObject
```
Update-AzRecoveryServicesAsrProtectionDirection -Direction <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## ОПИСАНИЕ
Для **указанного** объекта восстановления сайта Azure после завершения отработки обновления обновляется направление репликации для указанного объекта восстановления сайта Azure.

## ПРИМЕРЫ

### Пример 1
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

Запуск операции направления обновления для указанного плана восстановления и возврат объекта задания ASR, используемого для отслеживания операции.

### Пример 2
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi
```

Начните операцию направления обновления для указанного элемента, защищенного репликацией, в целевом регионе Azure, определяемом сопоставлением контейнера защиты и использованием кэша (в том же регионе, что и VM).

### Пример 3
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi
```

Начните операцию направления обновления для указанного элемента, защищенного репликацией, в целевом регионе Azure, определяемом сопоставлением контейнера защиты и предоставленной конфигурацией репликации диска.

### Пример 4
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi `
 -DiskEncryptionVaultId  $DiskEncryptionVaultId -DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
 -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

    
Начните операцию направления обновления для указанного элемента, защищенного зашифрованной репликацией, в целевом регионе Azure, определяемом сопоставлением контейнера защиты и предоставленной конфигурацией репликации диска.

### Пример 5
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi -RecoveryProximityPlacementGroupId $ppg
```

Начните операцию направления обновления для указанного элемента, защищенного репликацией, в целевом регионе Azure, определяемом сопоставлением контейнера защиты и использованием хранилища кэша (в том же регионе, что и VM) и группы расположения.


## PARAMETERS

### -Account
Запустите как учетную запись, которая будет использоваться для push-установки службы мобильной установки при необходимости. Должен быть в списке "Выполнить как учетные записи" в материале ASR.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AzureToAzure
Указывает аварийное восстановление Из Azure в Azure.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AzureToAzureDiskReplicationConfiguration
Определяет конфигурацию диска для аварийного восстановления.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AzureToVMware
Указывает сценарий переключения Azure на vMWare.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DataStore
Хранилище данных VMWARE, используемого для vmdisk.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRDataStore
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### -Direction
Определяет направление, используемого для обновления после отбойного обновления.
Допустимые значения этого параметра:

- PrimaryToRecovery
- RecoveryToPrimary

```yaml
Type: System.String
Parameter Sets: ByRPIObject, AzureToVMware, VMwareToAzure, HyperVToAzure, EnterpriseToEnterprise, ByRPObject, ByPEObject
Aliases:
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskEncryptionSecretUrl
Указывает секретный URL-адрес шифрования диска с версией (шифрованием диска Azure), который будет использоваться для восстановления VM после отбойного канала.

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskEncryptionVaultId
Определяет код секретного сейфа шифрования диска (шифрование диска Azure), который будет использоваться для восстановления VM после отбойного сбойа.

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HyperVToAzure
Переускорение виртуальной машины Hyper-V после срывов.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HyperVToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyEncryptionKeyUrl
Указывает URL-адрес ключа шифрования диска (шифрование диска Azure), который будет использоваться для восстановления VM-компьютера после отбойного процесса.

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyEncryptionVaultId
Определяет код keyVault ключа шифрования диска(шифрование диска Azure), который будет использоваться для восстановления VM после отбоя.

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LogStorageAccountId
Определяет ИД учетной записи хранения, который будет хранить журнал репликации ВМ-сообщений.

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MasterTarget
Master Target Server Details (Сведения о целевом сервере).

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRMasterTargetServer
Parameter Sets: AzureToVMware, VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProcessServer
Сервер обработки, используемый для репликации.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: AzureToVMware, VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProtectionContainerMapping
Защита containerMapping, используемая для репликации.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: AzureToVMware, VMwareToAzure, AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryAvailabilitySetId
Набор доступности, в который следует создать виртуальную машину при ото которую вы сможете отоправить компьютер.

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryAzureStorageAccountId
Определяет ИД учетной записи хранения Azure, к которая будет реплицироваться.

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVToAzure, AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryBootDiagStorageAccountId
Указывает учетную запись хранения для диагностики загрузки для восстановления Azure VM.

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryCloudServiceId
ИД ресурса облачной службы восстановления для отохода от сбойной работы этой виртуальной машины.

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryPlan
Указывает объект плана восстановления ASR.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RecoveryProximityPlacementGroupId
ИД ресурса группы расположения расположения близости восстановления для отостановки отостановки этой виртуальной машины.

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryResourceGroupId
ID recovery resourceGroup для защищенного VM-

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplicationProtectedItem
Определяет защищенный репликацией asR элемент.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, AzureToVMware, VMwareToAzure, HyperVToAzure, EnterpriseToEnterprise, AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RetentionVolume
Громкость хранения на целевом сервере,который используется.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRetentionVolume
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VmmToVmm
Обновите направление репликации для сбойного с виртуальной машины Hyper-V, которая защищена между двумя сайтами vMM Managed Hyper-V.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMwareToAzure
Обновление направления репликации из VMware в Azure.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Запрос на подтверждение перед запуском cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске cmdlet. Этот cmdlet не будет выполниться.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan

### Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem

## OUTPUTS

### Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ
