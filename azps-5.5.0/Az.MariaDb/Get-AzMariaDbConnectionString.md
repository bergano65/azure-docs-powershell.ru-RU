---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
ms.openlocfilehash: 1a6e96a8b8e030628655bdf95c58b726341dd2cc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100224332"
---
# Get-AzMariaDbConnectionString

## SYNOPSIS
Получите строку подключения для MariaDB под заданной структурой.

## СИНТАКСИС

### Имя Сервера (по умолчанию)
```
Get-AzMariaDbConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### ServerObject
```
Get-AzMariaDbConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## ОПИСАНИЕ
Получите строку подключения для MariaDB под заданной структурой.

## ПРИМЕРЫ

### Пример 1. Получить строку подключения от MariaDB
```powershell
PS C:\> Get-AzMariaDbConnectionString -ServerName mariadb-asd-01 -ResourceGroupName mariadb-test-qu5ov0 -Client ADO.NET

Server=mariadb-asd-01.mariadb.database.azure.com; Port=3306; Database={your_database}; Uid=adminuser@mariadb-asd-01; Pwd={your_password}; SslMode=Preferred;
```

Эта команда получает строку подключения MariaDB.

### Пример 2. Получить строку подключения для MariaDB
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-gp-t03 -ResourceGroupName lucas-manual-test | Get-AzMariaDbConnectionString -Client PHP

$con=mysqli_init();mysqli_ssl_set($con, NULL, NULL, {ca-cert filename}, NULL, NULL); mysqli_real_connect($con, "mariadb-gp-t03.mariadb.database.azure.com", "adminuser@mariadb-gp-t03", {your_password}, {your_database}, 3306);
```

Эта команда получает строку подключения MariaDB.

## PARAMETERS

### -Client
Подключение типа клиента

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

### -InputObject
Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer
Parameter Sets: ServerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Имя сервера.

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

### -ResourceGroupName
Имя группы ресурсов, которая содержит ресурс.

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

### -SubscriptionId
ИД подписки является частью URI для каждого звонка в службу

```yaml
Type: System.String
Parameter Sets: ServerName
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

### Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer

## OUTPUTS

### System.String

## ПРИМЕЧАНИЯ

ALIASES

СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ

Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства. Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.


INPUTOBJECT <IServer> : Параметр identity
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

