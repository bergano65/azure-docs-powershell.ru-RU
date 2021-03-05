---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConnectionString.md
ms.openlocfilehash: c85ece43045144d0befd6a6ed1e7ac1d7431796f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010451"
---
# Get-AzMySqlConnectionString

## SYNOPSIS
Получите строку подключения в соответствии с поставщиком клиентских подключений.

## СИНТАКСИС

### Получить (по умолчанию)
```
Get-AzMySqlConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzMySqlConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## ОПИСАНИЕ
Получите строку подключения в соответствии с поставщиком клиентских подключений.

## ПРИМЕРЫ

### Пример 1. Получить строку подключения mySql server по группе ресурсов и имени сервера
```powershell
PS C:\> Get-AzMySqlConnectionString -Client ADO.NET -Name mysql-test -ResourceGroupName PowershellMySqlTest

Server=mysql-test.mysql.database.azure.com; Port=3306; Database={your_database}; Uid=mysql_test@mysql-test; Pwd={your_password};
```

Этот cmdlet получает строку подключения MySql server по группе ресурсов и имени сервера.

### Пример 2. Получить строку подключения к серверу MySql по удостоверениям
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Get-AzMySqlConnectionString -Client PHP

$con=mysqli_init(); mysqli_real_connect($con, "mysql-test.mysql.database.azure.com", "mysql_test@mysql-test", {your_password}, {your_database}, 3306);
```

Этот cmdlet получает строку подключения mySql server по удостоверениям.

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
Сервер строки подключения.
Сведения о конструкции см. в разделе "Заметки" свойств INPUTOBJECT и создании таблицы с hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer
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

### Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer

## OUTPUTS

### System.String

## ПРИМЕЧАНИЯ

ALIASES

СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ

Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства. Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.


INPUTOBJECT: <IServer> сервер для строки подключения.
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
  - `[ReplicaCapacity <Int32?>]`: Максимальное количество реплик, которые может иметь этот сервер.
  - `[ReplicationRole <String>]`: роль репликации сервера.
  - `[SkuCapacity <Int32?>]`: пропускная способность, представляющая вычислительные единицы сервера.
  - `[SkuFamily <String>]`: семейство оборудования.
  - `[SkuName <String>]`: название SKU, как правило, уровень + семья + ядер, например B_Gen4_1, GP_Gen5_8.
  - `[SkuSize <String>]`: код размера, который должен быть интерпретируется ресурсом при необходимости.
  - `[SkuTier <SkuTier?>]`. Уровень конкретного SKU, например "Простой".
  - `[SslEnforcement <SslEnforcementEnum?>]`: включить или не включить ssl-при подключении к серверу.
  - `[StorageProfileBackupRetentionDay <Int32?>]`: дней хранения резервных копий для сервера.
  - `[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: включить гео избыточное или не для резервного копирования на сервере.
  - `[StorageProfileStorageAutogrow <StorageAutogrow?>]`: включить автоматическое рост хранилища.
  - `[StorageProfileStorageMb <Int32?>]`: Максимальное хранилище, разрешенное для сервера.
  - `[UserVisibleState <ServerState?>]`Состояние сервера, которое видно пользователю.
  - `[Version <ServerVersion?>]`: Версия сервера.

## СВЯЗАННЫЕ ССЫЛКИ

