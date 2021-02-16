---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbReplica.md
ms.openlocfilehash: 0ce25af607d2460abf2ec4585dacc124a1f2e65c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100219196"
---
# New-AzMariaDbReplica

## SYNOPSIS
Создает реплику сервера MariaDB.

## СИНТАКСИС

### Имя Сервера (по умолчанию)
```
New-AzMariaDbReplica -MasterName <String> -ReplicaName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ServerObject
```
New-AzMariaDbReplica -Master <IServer> -ReplicaName <String> [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## ОПИСАНИЕ
Создает реплику сервера MariaDB.

## ПРИМЕРЫ

### Пример 1. Создание копии DB для MariaDB
```powershell
PS C:\> New-AzMariaDbReplica -MasterName mariadb-test-9pebvn -ReplicaName mariadb-test-9pebvn-rep01 -ResourceGroupName mariadb-test-qu5ov0

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep01 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

Эта команда создает копию DB для MariaDB.

### Пример 2. Создание копии DB для MariaDB
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 | New-AzMariaDbReplica -ReplicaName mariadb-test-9pebvn-rep02

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep02 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

Эта команда создает копию DB для MariaDB.

### Пример 3. Создание копии DB для MariaDB
```powershell
PS C:\> $mariaDb = Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 
PS C:\> New-AzMariaDbReplica -Master $mariaDb -ReplicaName mariadb-test-9pebvn-rep03

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep03 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

Эта команда с параметром inputobject создает копию db с параметром inputobject для MariaDB.

## PARAMETERS

### -AsJob
Запуск команды в качестве задания

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
Region DefaultParameters— учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

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

### -Master
Исходный сервер, из который нужно восстановить.
Чтобы построить таблицу, см. раздел "ЗАМЕТКИ" для свойств MASTER и создание hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer
Parameter Sets: ServerObject
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MasterName
Имя сервера MariaDB.

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait
Запуск команды асинхронно

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

### -ReplicaName
Имя реплики.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReplicaServerName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Это значение можно получить через API Диспетчера ресурсов Azure или на портале.

```yaml
Type: System.String
Parameter Sets: ServerName
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
Этот ИД подписки является частью URI каждого звонка службы.

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
Метаданные приложения в виде пар ключевых значений.

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

### Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer

## OUTPUTS

### Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer

## ПРИМЕЧАНИЯ

ALIASES

СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ

Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства. Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.


MASTER: <IServer> исходный сервер, из который нужно восстановить.
  - `Location <String>`. Расположение ресурса.
  - `[Tag <ITrackedResourceTags>]`: метаданные конкретного приложения в виде пар ключевых значений.
    - `[(Any) <String>]`— это означает, что к этому объекту можно добавить любое свойство.
  - `[AdministratorLogin <String>]`. Имя администратора для входа на сервер. Может быть указано только при создании сервера (и требуется для создания).
  - `[EarliestRestoreDate <DateTime?>]`: самое раннее время создания точки восстановления (формат ISO8601)
  - `[FullyQualifiedDomainName <String>]`: полное доменное имя сервера.
  - `[IdentityType <IdentityType?>]`: Тип удостоверения. Задайте для этого назначения "SystemAssigned", чтобы автоматически создать и назначить ресурсу главную сумму Azure Active Directory.
  - `[MasterServerId <String>]`. Он является для сервера репликации.
  - `[ReplicaCapacity <Int32?>]`: Максимальное количество реплик, которые может иметь этаго сервер.
  - `[ReplicationRole <String>]`: роль репликации сервера.
  - `[SkuCapacity <Int32?>]`: пропускная способность, представляющая вычислительные единицы сервера.
  - `[SkuFamily <String>]`: семейство оборудования.
  - `[SkuName <String>]`: название SKU, как правило, уровень + семья + ядер, например B_Gen4_1, GP_Gen5_8.
  - `[SkuSize <String>]`: код размера, который должен быть интерпретируется ресурсом при необходимости.
  - `[SkuTier <SkuTier?>]`. Уровень конкретного SKU, например "Простой".
  - `[SslEnforcement <SslEnforcementEnum?>]`: включить или не включить ssl-при подключении к серверу.
  - `[StorageProfileBackupRetentionDay <Int32?>]`: дней резервного копирования для хранения на сервере.
  - `[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: включить гео избыточное или не для резервного копирования на сервере.
  - `[StorageProfileStorageAutogrow <StorageAutogrow?>]`: включить автоматическое рост хранилища.
  - `[StorageProfileStorageMb <Int32?>]`: Максимальное хранилище, разрешенное для сервера.
  - `[UserVisibleState <ServerState?>]`Состояние сервера, которое видно пользователю.
  - `[Version <ServerVersion?>]`: Версия сервера.

## СВЯЗАННЫЕ ССЫЛКИ

