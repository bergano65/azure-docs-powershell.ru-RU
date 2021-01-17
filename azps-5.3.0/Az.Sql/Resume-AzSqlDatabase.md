---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 84CF049A-D293-4FEB-8608-179146EADE41
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/resume-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Resume-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Resume-AzSqlDatabase.md
ms.openlocfilehash: a31a77f4e0780b5100018962b3475a0dffa97d9f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98420199"
---
# Resume-AzSqlDatabase

## SYNOPSIS
Возобновление базы SQL хранилища данных.

## СИНТАКСИС

```
Resume-AzSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## ОПИСАНИЕ
Для **возобновления базы данных Azure SQL AzSqlDatabase.**

## ПРИМЕРЫ

### Пример 1. Возобновление базы данных Azure SQL хранилищ данных
```
PS C:\>Resume-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

Эта команда возобновляет приостановленную базу данных Azure SQL хранилища данных.

## PARAMETERS

### -AsJob
Запуск cmdlet в фоновом режиме

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

### -DatabaseName
Указывает имя базы данных, которую этот cmdlet возобновляет.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
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
Указывает имя сервера, на котором размещена база данных, возобновляемая этим cmdlet.

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
Перед запуском cmdlet вам будет предложено подтвердить его.

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

## OUTPUTS

### Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel

## ПРИМЕЧАНИЯ
* **Cmdlet Resume-AzSqlDatabase** работает только в базах данных Azure SQL хранилища данных. Эта операция не поддерживается в выпусках Azure SQL Database Basic, Standard и Premium.

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzSqlDatabase](./Get-AzSqlDatabase.md)

[New-AzSqlDatabase](./New-AzSqlDatabase.md)

[Remove-AzSqlDatabase](./Remove-AzSqlDatabase.md)

[Set-AzSqlDatabase](./Set-AzSqlDatabase.md)

[Suspend-AzSqlDatabase](./Suspend-AzSqlDatabase.md)

[SQL базы данных](https://docs.microsoft.com/azure/sql-database/)


