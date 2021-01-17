---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlConfiguration.md
ms.openlocfilehash: e1b0ea3d07a7504e75f8bd6143820c52e73d9cf9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391895"
---
# Update-AzPostgreSqlConfiguration

## SYNOPSIS
Обновляет конфигурацию сервера.
Используйте Update-AzPostgreSqlServer если вы хотите обновить AdministratorLoginPassword, sku и т. д.

## СИНТАКСИС

### UpdateExpanded (по умолчанию)
```
Update-AzPostgreSqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### UpdateViaIdentityExpanded
```
Update-AzPostgreSqlConfiguration -InputObject <IPostgreSqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## ОПИСАНИЕ
Обновляет конфигурацию сервера.
Используйте Update-AzPostgreSqlServer если вы хотите обновить AdministratorLoginPassword, sku и т. д.

## ПРИМЕРЫ

### Пример 1. Обновление конфигурации PostgreSql по имени
```powershell
PS C:\> Update-AzPostgreSqlConfiguration -Name intervalstyle -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -Value SQL_STANDARD

Name          Value
----          -----
intervalstyle SQL_STANDARD
```

Этот cmdlet обновляет конфигурацию PostgreSql по имени.

### Пример 2. Обновление конфигурации PostgreSql с помощью удостоверения.
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/configurations/deadlock_timeout"
PS C:\> Update-AzPostgreSqlConfiguration -InputObject $ID -Value 2000

Name             Value
----             -----
deadlock_timeout 2000
```

Эти cmdlets update PostgreSql configuration by identity.

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
Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Имя конфигурации сервера.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ConfigurationName

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

### -ResourceGroupName
Имя группы ресурсов.
Имя нечувствительно к делу.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerName
Имя сервера.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Source
Источник конфигурации.

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
ИД целевой подписки.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Value
Значение конфигурации.

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

### Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity

## OUTPUTS

### Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration

## ПРИМЕЧАНИЯ

ALIASES

СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ

Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства. Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.


INPUTOBJECT <IPostgreSqlIdentity> : Параметр identity
  - `[ConfigurationName <String>]`: Имя конфигурации сервера.
  - `[DatabaseName <String>]`: имя базы данных.
  - `[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.
  - `[Id <String>]`: путь удостоверения ресурса
  - `[LocationName <String>]`: Название расположения.
  - `[ResourceGroupName <String>]`: Имя группы ресурсов. Имя нечувствительно к делу.
  - `[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.
  - `[ServerName <String>]`: имя сервера.
  - `[SubscriptionId <String>]`: ИД целевой подписки.
  - `[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.

## СВЯЗАННЫЕ ССЫЛКИ

