---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/test-azmysqlflexibleserverconnect
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Test-AzMySqlFlexibleServerConnect.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Test-AzMySqlFlexibleServerConnect.md
ms.openlocfilehash: ccb22d41ec1a4f2f2bceb711a09f7448015f9f38
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100228097"
---
# Test-AzMySqlFlexibleServerConnect

## SYNOPSIS
Проверка подключения к серверу базы данных

## СИНТАКСИС

### Проверка (по умолчанию)
```
Test-AzMySqlFlexibleServerConnect -Name <String> -ResourceGroupName <String>
 -AdministratorLoginPassword <SecureString> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### TestAndQuery
```
Test-AzMySqlFlexibleServerConnect -Name <String> -QueryText <String> -ResourceGroupName <String>
 -AdministratorLoginPassword <SecureString> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### TestViaIdentity
```
Test-AzMySqlFlexibleServerConnect -AdministratorLoginPassword <SecureString> -InputObject <IMySqlIdentity>
 [-DatabaseName <String>] [-AdministratorUserName <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### TestViaIdentityAndQuery
```
Test-AzMySqlFlexibleServerConnect -QueryText <String> -AdministratorLoginPassword <SecureString>
 -InputObject <IMySqlIdentity> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## ОПИСАНИЕ
Проверка подключения к серверу базы данных

## ПРИМЕРЫ

### Пример 1. Проверка подключения по имени
```powershell
PS C:\> Get-AzMySqlFlexibleServerConnect -ResourceGroupName PowershellMySqlTest -Name mysql-test -AdministratorLoginPassword $password

The connection testing to mysql-test.database.azure.com was successful!
```

Проверка подключения по группе ресурсов и имени сервера

### Пример 2. Проверка подключения по удостоверению
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Get-AzMySqlFlexibleServerConnect -AdministratorLoginPassword $password

The connection testing to mysql-test.database.azure.com was successful!
```

Проверка подключения по удостоверению

### Пример 3. Проверка запроса по имени
```powershell
PS C:\> Get-AzMySqlFlexibleServerConnect -ResourceGroupName PowershellMySqlTest -Name mysql-test -AdministratorLoginPassword $password -Query "SELECT * FROM test"

col
-----
1
2
3
```

Проверка запроса по группе ресурсов и имени сервера

### Пример 4. Проверка подключения по удостоверению
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Get-AzMySqlFlexibleServerConnect -Query "SELECT * FROM test" -AdministratorLoginPassword $password

col
-----
1
2
3
```

Проверка запроса по удостоверению

## PARAMETERS

### -AdministratorLoginPassword
Пароль администратора.
Не менее 8 знаков и не более 128 символов.
Пароль должен содержать символы из трех следующих категорий: английские буквы верхнего регистра, английские нижние буквы, цифры и не буквы и цифры.

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AdministratorUserName
Имя пользователя администратора сервера.
После этого изменить его будет невозможно.

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

### -DatabaseName
Имя базы данных, к которой нужно подключиться.

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
Сервер для подключения.
Сведения о конструкции см. в разделе "Заметки" свойств INPUTOBJECT и создании таблицы с hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: TestViaIdentity, TestViaIdentityAndQuery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Имя сервера для подключения.

```yaml
Type: System.String
Parameter Sets: Test, TestAndQuery
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -QueryText
Проверяемая база данных запроса

```yaml
Type: System.String
Parameter Sets: TestAndQuery, TestViaIdentityAndQuery
Aliases:

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
Parameter Sets: Test, TestAndQuery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity

## OUTPUTS

### System.String

## ПРИМЕЧАНИЯ

ALIASES

СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ

Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства. Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.


INPUTOBJECT: <IMySqlIdentity> сервер для подключения.
  - `[ConfigurationName <String>]`: имя конфигурации сервера.
  - `[DatabaseName <String>]`: имя базы данных.
  - `[FirewallRuleName <String>]`: имя правила брандмауэра сервера.
  - `[Id <String>]`: путь удостоверения ресурса
  - `[KeyName <String>]`: имя ключа сервера.
  - `[LocationName <String>]`: название расположения.
  - `[ResourceGroupName <String>]`: Имя группы ресурсов. Имя нечувствительно к делу.
  - `[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: имя политики оповещения системы безопасности.
  - `[ServerName <String>]`: имя сервера.
  - `[SubscriptionId <String>]`: ИД целевой подписки.
  - `[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.

## СВЯЗАННЫЕ ССЫЛКИ

