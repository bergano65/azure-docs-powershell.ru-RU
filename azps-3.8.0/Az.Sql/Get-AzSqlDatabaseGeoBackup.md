---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 256AA6F4-D856-4713-A0AC-0DA1A145AA5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
ms.openlocfilehash: 0ca3a6c467ab5fd7dd681164d88686a6360394ee
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066021"
---
# Get-AzSqlDatabaseGeoBackup

## КРАТКИй обзор
Получает геоизбыточную резервную копию базы данных.

## Максимальное

```
Get-AzSqlDatabaseGeoBackup [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzSqlDatabaseGeoBackup** получает указанную геоизбыточную резервную копию базы данных SQL или все доступные геоизбыточные резервные копии на указанном сервере.
Резервная копия с геоизбыточным резервированием — это ресурс restorable с использованием файлов данных из отдельного географического расположения.
Вы можете использовать Geo-Restore для восстановления геоизбыточной резервной копии в случае сбоя в регионе, чтобы восстановить базу данных в новом регионе.
Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение всех геоизбыточных резервных копий на сервере
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

Эта команда получает все доступные резервные копии с геоизбыточным хранилищем на указанном сервере.

### Пример 2: получение указанной геоизбыточной резервной копии
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

Эта команда возвращает геоизбыточное резервное копирование базы данных с именем ContosoDatabase.

### Пример 3: получение всех геоизбыточных резервных копий на сервере с помощью фильтрации
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "Contoso*"
```

Эта команда получает все доступные резервные копии с геоизбыточной учетной записью на указанном сервере, который начинается со слова contoso.

## ПАРАМЕТРЫ

### -DatabaseName
Указывает имя базы данных, которую требуется получить.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
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
Указывает имя группы ресурсов, которой назначен сервер базы данных SQL.

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

### -ИмяСервера
Указывает имя сервера, на котором размещается резервная копия для восстановления.

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
Запрашивает подтверждение перед запуском командлета.

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
Показывает, что произойдет при запуске командлета.
Командлет не выполняется.

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## ВХОДНЫЕ данные

### System. String

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. SQL. Backup. Model. AzureSqlDatabaseGeoBackupModel

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Обзор: бесперебойная работа в облаке и аварийное восстановление базы данных с помощью базы данных SQL](http://go.microsoft.com/fwlink/?LinkId=746881)

[Восстановление базы данных SQL Azure из сбоя](http://go.microsoft.com/fwlink/?LinkId=746882)

[Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md)

[Документация по базам данных SQL](https://docs.microsoft.com/azure/sql-database/)
