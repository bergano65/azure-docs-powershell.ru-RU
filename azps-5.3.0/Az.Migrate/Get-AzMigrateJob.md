---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
ms.openlocfilehash: bb28550a0b23fa9032832873a78771d25d2a38bd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518245"
---
# Get-AzMigrateJob

## SYNOPSIS
Извлекает состояние задания миграции Azure.

## СИНТАКСИС

### ListByName (по умолчанию)
```
Get-AzMigrateJob -ProjectName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetById
```
Get-AzMigrateJob -JobID <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetByInputObject
```
Get-AzMigrateJob -InputObject <IJob> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### GetByName
```
Get-AzMigrateJob -JobName <String> -ProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### ListById
```
Get-AzMigrateJob -ProjectID <String> -ResourceGroupID <String> [-SubscriptionId <String>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## ОПИСАНИЕ
При Get-AzMigrateJob будет снова отознано состояние задания миграции Azure.

## ПРИМЕРЫ

### Пример 1. По заданиям
```powershell
PS C:\> Get-AzMigrateJob -JobID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b" 

ActivityId                       : 68af14b4-46ae-48d1-b3e9-cdcffb9e8a93 ActivityId: 74d1a396-1d37-4264-8a5b-b727aaef0171
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 9/16/20 11:57:33 AM
Error                            : {}
FriendlyName                     : Associate replication policy
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b
Location                         :
Name                             : 997e2a92-5afe-49c7-a81a-89660aec9b7b
ScenarioName                     : AssociateProtectionProfile
StartTime                        : 9/16/20 11:57:32 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 42752b89-5fad-52fd-bf93-679fbdb6fed9
TargetObjectName                 : migrateAzMigratePWSHTc8d1sitepolicy
Task                             : {CloudPairingPrerequisitesCheck, CloudPairingPrepareSite}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

Задание будет извлечено по его ИД.

### Пример 2. Список по группе ресурсов и проекту
```powershell
PS C:\> Get-AzMigrateJob -ResourceGroupName 'azmigratepwshtestasr13072020' -ProjectName 'AzMigrateTestProjectPWSH'

ActivityId                       :
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         :
EndTime                          : 9/21/20 4:13:40 PM
Error                            : {}
FriendlyName                     : Update the virtual machine
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/1c89e38e-34ec-4903-aa7c-115201bf2de1
Location                         :
Name                             : 1c89e38e-34ec-4903-aa7c-115201bf2de1
ScenarioName                     : UpdateVmProperties
StartTime                        : 9/21/20 4:13:34 PM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 593b735d-2a34-53b2-b8ed-e33da5650703
TargetObjectName                 : rb-w2k12r2-1
Task                             : {}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

Это все задания в проекте.

### Пример 3. Группы ресурсов, проекта и должности
```powershell
PS C:\> Get-AzMigrateJob -ResourceGroupName 'azmigratepwshtestasr13072020' -ProjectName 'AzMigrateTestProjectPWSH' -JobName 7ae1ee7c-442c-499d-8b0e-81d52a42b71e

ActivityId                       : 6986b7e5-0f1f-49d8-8b4b-77e6f66bcb92 ActivityId: eb73c6a1-7c66-469f-a853-d896aa38cc0f
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 8/21/20 6:41:48 AM
Error                            : {}
FriendlyName                     : Create replication policy
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/7ae1ee7c-442c-499d-8b0e-81d52a42b71e
Location                         :
Name                             : 7ae1ee7c-442c-499d-8b0e-81d52a42b71e
ScenarioName                     : AddProtectionProfile
StartTime                        : 8/21/20 6:41:48 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 18b2ccec-e39a-517b-ae5d-dd395e9f4f96
TargetObjectName                 : samplePolicy3
Task                             : {AddProtectionProfilePreflightsCheckTask, AddProtectionProfileTask}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

Это задание будет конкретным.

## PARAMETERS

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Filter
Параметры фильтра OData.

```yaml
Type: System.String
Parameter Sets: ListById, ListByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Определяет объект задания для сервера репликации.
Сведения о конструкции см. в разделе "Заметки" свойств INPUTOBJECT и создании таблицы с hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob
Parameter Sets: GetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobID
Определяет ид задания, для которого требуется получить подробные сведения.

```yaml
Type: System.String
Parameter Sets: GetById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobName
Идентификатор задания

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProjectID
Определяет проект миграции Azure, в котором репликация серверов.

```yaml
Type: System.String
Parameter Sets: ListById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProjectName
Имя проекта миграции.

```yaml
Type: System.String
Parameter Sets: GetByName, ListByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupID
Группа ресурсов в azure Migrate Project в текущей подписке.

```yaml
Type: System.String
Parameter Sets: ListById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов, в которой находится хранилище служб восстановления.

```yaml
Type: System.String
Parameter Sets: GetByName, ListByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
ИД подписки Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

## OUTPUTS

### Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob

## ПРИМЕЧАНИЯ

ALIASES

СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ

Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства. Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.


INPUTOBJECT: <IJob> определяет объект задания сервера репликации.
  - `[Location <String>]`: расположение ресурса
  - `[ActivityId <String>]`: ИД действия.
  - `[AllowedAction <String[]>]`: Разрешено действие задания.
  - `[CustomDetailAffectedObjectDetail <IJobDetailsAffectedObjectDetails>]`. Затронутые свойства объекта, такие как исходный сервер, source cloud, target server, target cloud и т. д., основаны на сведениях о объекте рабочего процесса.
    - `[(Any) <String>]`— это означает, что к этому объекту можно добавить любое свойство.
  - `[EndTime <DateTime?>]`: время окончания.
  - `[Error <IJobErrorDetails[]>]`: Ошибки.
    - `[CreationTime <DateTime?>]`: Время создания ошибки задания.
    - `[ErrorLevel <String>]`: Уровень ошибки.
    - `[ProviderErrorDetailErrorCode <Int32?>]`: Код ошибки.
    - `[ProviderErrorDetailErrorId <String>]`: ИД ошибки поставщика.
    - `[ProviderErrorDetailErrorMessage <String>]`: Сообщение об ошибке.
    - `[ProviderErrorDetailPossibleCaus <String>]`: возможные причины возникновения ошибки.
    - `[ProviderErrorDetailRecommendedAction <String>]`Рекомендуемое действие для устранения ошибки.
    - `[ServiceErrorDetailActivityId <String>]`: ИД действия.
    - `[ServiceErrorDetailCode <String>]`: Код ошибки.
    - `[ServiceErrorDetailMessage <String>]`: сообщение об ошибке.
    - `[ServiceErrorDetailPossibleCaus <String>]`: Возможные причины ошибки.
    - `[ServiceErrorDetailRecommendedAction <String>]`: Рекомендуемое действие для устранения ошибки.
    - `[TaskId <String>]`: ИД задачи.
  - `[FriendlyName <String>]`: DisplayName.
  - `[ScenarioName <String>]`: ScenarioName.
  - `[StartTime <DateTime?>]`: Время начала.
  - `[State <String>]`: Состояние задания. Это одно из этих значений: NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended или Other.
  - `[StateDescription <String>]`: Описание состояния задания. Например: для состояния "Успешное состояние" описание может быть завершено, частично Сужение, CompletedWithInformation или Skipped.
  - `[TargetInstanceType <String>]`: Тип затронутого объекта— класс {Microsoft.Azure.SiteRecovery.V2015_11_10.AffectedObjectType}.
  - `[TargetObjectId <String>]`: Затронутый ИД объекта.
  - `[TargetObjectName <String>]`: имя затронутого объекта.
  - `[Task <IAsrTask[]>]`Задачи.
    - `[AllowedAction <String[]>]`. Состояние и действия, применимые к данной задаче.
    - `[CustomDetailInstanceType <String>]`: Тип сведений о задаче.
    - `[EndTime <DateTime?>]`: время окончания.
    - `[Error <IJobErrorDetails[]>]`: Сведения об ошибке задачи.
    - `[FriendlyName <String>]`: Имя.
    - `[GroupTaskCustomDetailChildTask <IAsrTask[]>]`: Задачи ребенка.
    - `[GroupTaskCustomDetailInstanceType <String>]`: Тип сведений о задаче.
    - `[Name <String>]`: Уникальное имя задачи.
    - `[StartTime <DateTime?>]`: Время начала.
    - `[State <String>]`: Состояние. Это одно из этих значений: NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended или Other.
    - `[StateDescription <String>]`: Описание состояния задачи. Например: для состояния "Успешное состояние" описание может быть завершено, частично Сужение, CompletedWithInformation или Skipped.
    - `[TaskId <String>]`: ИД.
    - `[TaskType <String>]`Тип задачи. Сведения в свойстве CustomDetails зависят от этого типа.

## СВЯЗАННЫЕ ССЫЛКИ

