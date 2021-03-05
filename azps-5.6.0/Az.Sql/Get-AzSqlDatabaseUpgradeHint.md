---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D64FB139-04E2-47BC-86FB-EEEA23839F2F
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabaseupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
ms.openlocfilehash: 9018dab5f09bbab6a3fb1197ee8aabd09141e664
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014675"
---
# Get-AzSqlDatabaseUpgradeHint

## SYNOPSIS
Получает подсказки о ценах на уровень для базы данных.

## СИНТАКСИС

```
Get-AzSqlDatabaseUpgradeHint [-ServerName] <String> [-DatabaseName <String>]
 [-ExcludeElasticPoolCandidates <Boolean>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## ОПИСАНИЕ
На **основе cmdlet Get-AzSqlDataBaseUpgradeHint** можно получить подсказки о ценах на обновление базы данных Azure SQL.
Базы данных, которые все еще находятся на уровнях цен на веб-сайты и бизнес, могут перейти на новые уровни цен "Базовый", "Стандартный" и "Премиум".
Этот cmdlet также поддерживается службой SQL Server Stretch Database в Azure.

## ПРИМЕРЫ

### Пример 1. Получить рекомендации для всех баз данных на сервере
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

Эта команда возвращает подсказки об обновлении для всех баз данных на сервере Server01.

### Пример 2. Получить рекомендации для конкретной базы данных
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

Эта команда возвращает подсказки об обновлении для конкретной базы данных.

### Пример 3. Получить рекомендации для всех баз данных, которые не находятся в эластичном пуле баз данных
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ExcludeElasticPoolCandidates $True
```

Эта команда возвращает подсказки об обновлении для всех баз данных, которые не находятся в эластичном пуле.

### Пример 4. Получить рекомендации для всех баз данных на сервере с помощью фильтрации
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

Эта команда возвращает подсказки об обновлении для всех баз данных на сервере Server01, которые начинаются с "Database".

## PARAMETERS

### -DatabaseName
Указывает имя базы данных SQL, для которой этот cmdlet получает подсказку об обновлении.
Если база данных не указана, этот cmdlet будет подсказок для всех баз данных на логическом сервере.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

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

### -ExcludeElasticPoolCandidates
Указывает на то, исключены ли базы данных в пулах эластичных баз данных из возвращенных рекомендаций.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов, которой назначена база данных.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServerName
Указывает имя сервера, на котором размещена база данных, для которой этот cmdlet получает подсказку об обновлении.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

### System.Boolean

## OUTPUTS

### Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzSqlDatabaseExpanded](./Get-AzSqlDatabaseExpanded.md)

[Get-AzSqlElasticPoolRecommendation](./Get-AzSqlElasticPoolRecommendation.md)


