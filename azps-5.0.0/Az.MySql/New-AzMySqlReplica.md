---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlReplica.md
ms.openlocfilehash: 5e5d83266dd86ccaf0bd5037c6af01f8b1846a69
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249391"
---
# New-AzMySqlReplica

## КРАТКИй обзор
Создание новой реплики из существующей базы данных.

## Максимальное

```
New-AzMySqlReplica -Replica <String> -ResourceGroupName <String> -Master <IServer> [-SubscriptionId <String>]
 [-Location <String>] [-Sku <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Создание новой реплики из существующей базы данных.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание новой реплики сервера MySql
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | New-AzMySqlReplica -Replica mysql-test-replica -ResourceGroupName PowershellMySqlTest

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-replica eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

Этот командлет создает новую реплику сервера MySql.

### Пример 2: создание новой реплики сервера MySql
```powershell
PS C:\> $mysql = Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test
PS C:\> New-AzMySqlReplica -Master $mysql -Replica mysql-test-replica -ResourceGroupName PowershellMySqlTest

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-replica eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

Этот командлет с мастером параметров (InputObject) создает новую реплику сервера MySql.

## ПАРАМЕТРЫ

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

### -Location
Расположение, в котором находится ресурс.

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
Исходный объект сервера, из которого создается реплика.
Для конструирования ознакомьтесь с разделом "Заметки" ЭТАЛОНных свойств и создайте хэш-таблицу.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Wait
Выполните команду асинхронно.

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

### -Реплика
Имя сервера.

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
Имя группы ресурсов, содержащей ресурс, это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.

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

### -SKU
Название SKU, обычно — «уровни + семейство + ядра», например B_Gen4_1, GP_Gen5_8.

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
Идентификатор подписки, определяющий подписку на Azure.

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

### -Confirm
Запрашивает подтверждение перед запуском командлета.

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
Показывает, что произойдет при запуске командлета.
Командлет не выполняется.

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## ВХОДНЫЕ данные

### Microsoft. Azure. PowerShell. командлеты. MySql. Models. Api20171201. IServer

## НАПРЯЖЕНИЕ

### Microsoft. Azure. PowerShell. командлеты. MySql. Models. Api20171201. IServer

## Пуск

СВЯЗЫВАЮТ

СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ

Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства. Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.


ОБРАЗЕЦ <IServer> : исходный объект сервера, из которого создается реплика.
  - `Location <String>`: Расположение, в котором находится ресурс.
  - `[Tag <ITrackedResourceTags>]`: Метаданные, зависящие от приложения, в виде пар "ключ-значение".
    - `[(Any) <String>]`: Это указывает на то, что в этот объект можно добавить любое свойство.
  - `[AdministratorLogin <String>]`: Имя для входа на сервер, на котором находится администратор. Может быть указан только в том случае, если сервер создается (и является обязательным для создания).
  - `[EarliestRestoreDate <DateTime?>]`: Самое раннее время создания точки восстановления (формат ISO8601)
  - `[FullyQualifiedDomainName <String>]`: Полное доменное имя сервера.
  - `[IdentityType <IdentityType?>]`: Тип удостоверения. Задайте для этого свойства значение "SystemAssigned", чтобы автоматически создать и назначить участника Azure Active Directory для ресурса.
  - `[InfrastructureEncryption <InfrastructureEncryption?>]`: Состояние, показывающее, включено ли шифрование инфраструктуры сервера.
  - `[MasterServerId <String>]`: Идентификатор главного сервера для сервера-реплики.
  - `[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Принудительная минимальная версия TLS для сервера.
  - `[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Разрешены ли доступ к общедоступной сети для этого сервера. Значение не является обязательным, но если оно передано, должно быть включено или отключено
  - `[ReplicaCapacity <Int32?>]`: Максимальное количество реплик, которые может иметь главный сервер.
  - `[ReplicationRole <String>]`: Роль репликации сервера.
  - `[SkuCapacity <Int32?>]`: Масштабирование и уменьшение производительности, представляющие вычислительные единицы сервера.
  - `[SkuFamily <String>]`: Семейство оборудования.
  - `[SkuName <String>]`: Название SKU, обычно — «уровни + семейство + ядра», например B_Gen4_1, GP_Gen5_8.
  - `[SkuSize <String>]`: Код размера, который должен обрабатываться ресурсом соответствующим образом.
  - `[SkuTier <SkuTier?>]`: Уровень определенного SKU, например Basic.
  - `[SslEnforcement <SslEnforcementEnum?>]`: Включение принудительного применения SSL или не при подключении к серверу.
  - `[StorageProfileBackupRetentionDay <Int32?>]`: Срок хранения резервных копий для сервера.
  - `[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Включение геоизбыточного резервирования или не для резервного копирования сервера.
  - `[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Включите автоматическое расширение хранилища.
  - `[StorageProfileStorageMb <Int32?>]`: Максимальный объем хранилища, разрешенный для сервера.
  - `[UserVisibleState <ServerState?>]`: Состояние сервера, доступного для пользователя.
  - `[Version <ServerVersion?>]`: Версия сервера.

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

