---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/restore-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restore-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restore-AzPostgreSqlServer.md
ms.openlocfilehash: c9e4134b6787f78442a18836c15ce190c3e685d8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391900"
---
# Restore-AzPostgreSqlServer

## SYNOPSIS
Восстановление сервера из существующей резервной копии

## СИНТАКСИС

### GeoRestore (по умолчанию)
```
Restore-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer> -UseGeoRestore
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### PointInTimeRestore
```
Restore-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer>
 -RestorePointInTime <DateTime> -UsePointInTimeRestore [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## ОПИСАНИЕ
Восстановление сервера из существующей резервной копии

## ПРИМЕРЫ

### Пример 1. Восстановление сервера PostgreSql с помощью GeoReplica Restore
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName postgresqltestserverreplica | Restore-AzPostgreSqlServer -Name PostgreSqlTestServer -ResourceGroupName PostgreSqlTestRG -UseGeoRestore

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

Этот cmdlet restores PostgreSql server using GeoReplica Restore.

### Пример 2. Восстановление сервера PostgreSql с помощью восстановления PointInTime
```powershell
PS C:\> $restorePointInTime = (Get-Date).AddMinutes(-10)
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Restore-AzPostgreSqlServer -Name PostgreSqlTestServerGEO -ResourceGroupName PostgreSqlTestRG -RestorePointInTime $restorePointInTime -UsePointInTimeRestore

Name                    Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                    -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestservergeo eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

Эти cmdlets restore PostgreSql server using PointInTime Restore.

## PARAMETERS

### -AsJob
Выполнить команду как задание.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -InputObject
Исходный сервер, из который нужно восстановить.
Сведения о конструкции см. в разделе "Заметки" свойств INPUTOBJECT и создании таблицы с hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Location
Расположение ресурса.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Имя сервера.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait
Запустите команду асинхронно.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов, которая содержит ресурс. Это значение можно получить через API диспетчера ресурсов Azure или на портале.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestorePointInTime
Расположение ресурса.

```yaml
Type: System.DateTime
Parameter Sets: PointInTimeRestore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SKU
Как правило, это название SKU уровня +family + cores, например B_Gen4_1, GP_Gen5_8.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Идентификатор подписки, который определяет подписку Azure.

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

### -Tag
Метаданные конкретного приложения в виде пар ключевых значений.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseGeoRestore
Восстановление с помощью георежима

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeoRestore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UsePointInTimeRestore
Восстановление с помощью режима PointInTime

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PointInTimeRestore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Перед запуском cmdlet вам будет предложено подтвердить его.

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
Показывает, что произойдет при запуске cmdlet.
Этот cmdlet не будет выполниться.

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

### Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer

## OUTPUTS

### Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer

## ПРИМЕЧАНИЯ

ALIASES

СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ

Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства. Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.


INPUTOBJECT: <IServer> исходный сервер, из который нужно восстановить.
  - `Location <String>`. Расположение ресурса.
  - `[Tag <ITrackedResourceTags>]`: метаданные конкретного приложения в виде пар ключевых значений.
    - `[(Any) <String>]`— это означает, что к этому объекту можно добавить любое свойство.
  - `[AdministratorLogin <String>]`: имя администратора для входа на сервер. Может быть указано только при создании сервера (и требуется для создания).
  - `[EarliestRestoreDate <DateTime?>]`: самое раннее время создания точки восстановления (формат ISO8601)
  - `[FullyQualifiedDomainName <String>]`: полное доменное имя сервера.
  - `[IdentityType <IdentityType?>]`: Тип удостоверения. Задайте для этого назначения ресурсу systemAssigned, чтобы автоматически создать и назначить ресурсу главную сумму Azure Active Directory.
  - `[InfrastructureEncryption <InfrastructureEncryption?>]`Состояние, показывающая, включено ли шифрование инфраструктуры сервера.
  - `[MasterServerId <String>]`. Он является для сервера репликации.
  - `[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: привязйте минимальную версию TLS для сервера.
  - `[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: разрешен ли доступ к общедоступным сетям для этого сервера. Значение является необязательным, но если он передан, необходимо использовать значения "Включено" или "Отключено".
  - `[ReplicaCapacity <Int32?>]`: Максимальное количество реплик, которые может иметь этот сервер.
  - `[ReplicationRole <String>]`: роль репликации сервера.
  - `[SkuCapacity <Int32?>]`: пропускная способность, представляющая вычислительные единицы сервера.
  - `[SkuFamily <String>]`: семейство оборудования.
  - `[SkuName <String>]`: название SKU, как правило, уровень + семья + ядер, например, B_Gen4_1, GP_Gen5_8.
  - `[SkuSize <String>]`: код размера, который должен быть интерпретируется ресурсом при необходимости.
  - `[SkuTier <SkuTier?>]`. Уровень конкретного SKU, например "Простой".
  - `[SslEnforcement <SslEnforcementEnum?>]`: включить или не включить ssl-при подключении к серверу.
  - `[StorageProfileBackupRetentionDay <Int32?>]`: дней резервного копирования для хранения на сервере.
  - `[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: включить гео избыточные или не архивные копии на сервере.
  - `[StorageProfileStorageAutogrow <StorageAutogrow?>]`: включить автоматическое рост хранилища.
  - `[StorageProfileStorageMb <Int32?>]`: Максимальное хранилище, разрешенное для сервера.
  - `[UserVisibleState <ServerState?>]`Состояние сервера, которое видно пользователю.
  - `[Version <ServerVersion?>]`: Версия сервера.

## СВЯЗАННЫЕ ССЫЛКИ
