---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConnectionString.md
ms.openlocfilehash: 7f2040455e48130615a52ba06186b189b67ea971
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100225492"
---
# Get-AzPostgreSqlConnectionString

## SYNOPSIS
Получите строку подключения в соответствии с поставщиком клиентских подключений.

## СИНТАКСИС

### Получить (по умолчанию)
```
Get-AzPostgreSqlConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzPostgreSqlConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## ОПИСАНИЕ
Получите строку подключения в соответствии с поставщиком клиентских подключений.

## ПРИМЕРЫ

### Пример 1. Получить строку подключения PostgreSql по группе ресурсов и имени сервера
```powershell
PS C:\> Get-AzPostgreSqlConnectionString -Client ADO.NET -Name PostgreSqlTestServer -ResourceGroupName PostgreSqlTestRG

Server=postgresqltestserver.postgres.database.azure.com;Database={your_database};Port=5432;User Id=pwsh@postgresqltestserver;Password={your_password};Ssl Mode=Require;
```

Этот cmdlet получает строку подключения PostgreSql server по группе ресурсов и имени сервера.

### Пример 2. Получить строку подключения Сервера PostgreSql по удостоверениям
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Get-AzPostgreSqlConnectionString -Client PHP

host=postgresqltestserver.postgres.database.azure.com port=5432 dbname={your_database} user=pwsh@postgresqltestserver password={your_password} sslmode=require
```

Этот cmdlet получает строку подключения PostgreSql server по удостоверениям.

## PARAMETERS

### -Client
Поставщик клиентских подключений.

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
Сервер строки подключения Для сстройки. См. раздел "ЗАМЕТКИ" для свойств INPUTOBJECT и создание hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer
Parameter Sets: GetViaIdentity
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
Parameter Sets: Get
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов, которая содержит ресурс. Это значение можно получить через API Диспетчера ресурсов Azure или на портале.

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Идентификатор подписки, который определяет подписку Azure.

```yaml
Type: System.String
Parameter Sets: Get
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

### Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer

## OUTPUTS

### System.String

## ПРИМЕЧАНИЯ

ALIASES

СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ

Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства. Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.


INPUTOBJECT: <IServer> сервер для строки подключения
  - `Location <String>`: географическое расположение ресурса
  - `[Tag <ITrackedResourceTags>]`: теги ресурсов.
    - `[(Any) <String>]`— это означает, что к этому объекту можно добавить любое свойство.
  - `[AdministratorLogin <String>]`: имя администратора для входа на сервер. Может быть указано только при создании сервера (и требуется для создания).
  - `[EarliestRestoreDate <DateTime?>]`: самое раннее время создания точки восстановления (формат ISO8601)
  - `[FullyQualifiedDomainName <String>]`: полное доменное имя сервера.
  - `[IdentityType <IdentityType?>]`: Тип удостоверения. Задайте для этого назначения "SystemAssigned", чтобы автоматически создать и назначить ресурсу главную сумму Azure Active Directory.
  - `[InfrastructureEncryption <InfrastructureEncryption?>]`Состояние, показывающая, включено ли шифрование инфраструктуры сервера.
  - `[MasterServerId <String>]`. Он является для сервера репликации.
  - `[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: привязйте минимальную версию TLS для сервера.
  - `[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: разрешен ли доступ к общедоступным сетям для этого сервера. Значение является необязательным, но если он передан, необходимо использовать значения "Включено" или "Отключено".
  - `[ReplicaCapacity <Int32?>]`: Максимальное количество реплик, которые может иметь этаго сервер.
  - `[ReplicationRole <String>]`: роль репликации сервера.
  - `[SkuCapacity <Int32?>]`: пропускная способность, представляющая вычислительные единицы сервера.
  - `[SkuFamily <String>]`: семейство оборудования.
  - `[SkuName <String>]`: название SKU, как правило, уровень + семья + ядер, например B_Gen4_1, GP_Gen5_8.
  - `[SkuSize <String>]`: код размера, который должен быть интерпретируется ресурсом при необходимости.
  - `[SkuTier <SkuTier?>]`. Уровень конкретного SKU, например "Простой".
  - `[SslEnforcement <SslEnforcementEnum?>]`: включить или не включить ssl-при подключении к серверу.
  - `[StorageProfileBackupRetentionDay <Int32?>]`: дней хранения резервных копий для сервера.
  - `[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: включить гео избыточные или не архивные копии на сервере.
  - `[StorageProfileStorageAutogrow <StorageAutogrow?>]`: включить автоматическое рост хранилища.
  - `[StorageProfileStorageMb <Int32?>]`: Максимальное хранилище, разрешенное для сервера.
  - `[UserVisibleState <ServerState?>]`Состояние сервера, которое видно пользователю.
  - `[Version <ServerVersion?>]`: Версия сервера.

## СВЯЗАННЫЕ ССЫЛКИ

