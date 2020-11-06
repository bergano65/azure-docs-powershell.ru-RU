---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 72E0E558-74D7-4A50-A975-FA7D0C0B301E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlDatabase.md
ms.openlocfilehash: 61f66a61d14738da034644fc3dfef865c8719181
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562024"
---
# Restore-AzureRmSqlDatabase

## КРАТКИй обзор
Восстанавливает базу данных SQL.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### FromPointInTimeBackup
```
Restore-AzureRmSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> [-Edition <DatabaseEdition>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### FromDeletedDatabaseBackup
```
Restore-AzureRmSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> [-Edition <DatabaseEdition>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### FromGeoBackup
```
Restore-AzureRmSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <DatabaseEdition>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### FromLongTermRetentionBackup
```
Restore-AzureRmSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <DatabaseEdition>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **RESTORE-AzureRmSqlDatabase** восстанавливает базу данных SQL из резервной копии с геоизбыточностью, резервной копии удаленной базы данных, длительной резервной копии хранения или момента времени в действующей базе данных.
Восстановленная база данных будет создана как новая.

Вы можете создать эластичную базу данных SQL, указав параметр *ElasticPoolName* в существующем пуле эластичных БД.

## ИЛЛЮСТРИРУЮТ

### Пример 1: восстановление базы данных на момент времени
```
PS C:\>$Database = Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -Edition "Standard" -ServiceObjectiveName "S2"
```

Первая команда получает базу данных SQL с именем Database01 и сохраняет ее в переменной $Database.

Вторая команда восстанавливает базу данных $Database из указанного резервного копирования на момент времени в базу данных с именем RestoredDatabase.

### Пример 2: восстановление базы данных из состояния на момент времени в пул эластичных БД
```
PS C:\>$Database = Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -ElasticPoolName "ElasticPool01"
```

Первая команда получает базу данных SQL с именем Database01 и сохраняет ее в переменной $Database.

Вторая команда восстанавливает базу данных $Database из указанного резервного копирования на момент времени в базу данных SQL с именем RestoredDatabase в пуле эластичных БД с именем elasticpool01.

### Пример 3: восстановление удаленной базы данных
```
PS C:\>$DeletedDatabase = Get-AzureRmSqlDeletedDatabaseBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -Edition "Standard" -ServiceObjectiveName "S2" -PointInTime UTCDateTime
```

Первая команда получает удаленную резервную копию базы данных, которую вы хотите восстановить, с помощью [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).
Вторая команда запускает восстановление из удаленной резервной копии базы данных с помощью командлета [RESTORE-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md) . Если параметр-PointInTime не указан, база данных будет восстановлена до времени удаления.

### Пример 4: восстановление удаленной базы данных в пуле эластичных БД
```
PS C:\>$DeletedDatabase = Get-AzureRmSqlDeletedDatabaseBackup -ResourceGroupName $resourceGroupName -ServerName $sqlServerName -DatabaseName 'DatabaseToRestore'
PS C:\> Restore-AzureRmSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -ElasticPoolName "elasticpool01" -PointInTime UTCDateTime
```

Первая команда получает удаленную резервную копию базы данных, которую вы хотите восстановить, с помощью [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).
Вторая команда запускает восстановление из удаленной резервной копии базы данных с помощью [RESTORE-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md). Если параметр-PointInTime не указан, база данных будет восстановлена до времени удаления.

### Пример 5: Geo-Restore базы данных
```
PS C:\>$GeoBackup = Get-AzureRmSqlDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromGeoBackup -ResourceGroupName "TargetResourceGroup" -ServerName "TargetServer" -TargetDatabaseName "RestoredDatabase" -ResourceId $GeoBackup.ResourceID -Edition "Standard" -RequestedServiceObjectiveName "S2"
```

Первая команда получает геоизбыточное резервное копирование базы данных с именем Database01 и сохраняет его в переменной $GeoBackup.

Вторая команда восстанавливает резервную копию в $GeoBackup на базу данных SQL с именем RestoredDatabase.

## ПАРАМЕТРЫ

### -DeletionDate
Указывает дату удаления как объект **DateTime** .
Чтобы получить объект **DateTime** , используйте командлет Get-Date.

```yaml
Type: System.DateTime
Parameter Sets: FromDeletedDatabaseBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Edition
Указывает выпуск базы данных SQL.
Для этого параметра допустимы следующие значения:

- Ничего
- Версию
- Базового
- Стандартная
- Хранилище Datawarehouse
- Бесплатно

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases: 
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ElasticPoolName
Указывает имя эластичного пула, в который нужно добавить базу данных SQL.

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

### -FromDeletedDatabaseBackup
Указывает на то, что этот командлет восстанавливает базу данных из резервной копии удаленной базы данных SQL.
Вы можете использовать командлет Get-AzureRMSqlDeletedDatabaseBackup для получения резервной копии удаленной базы данных SQL.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromDeletedDatabaseBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FromGeoBackup
Указывает на то, что этот командлет восстанавливает базу данных SQL из резервной копии с избыточностью.
Вы можете использовать командлет Get-AzureRMSqlDatabaseGeoBackup, чтобы получить геоизбыточную резервную копию.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromGeoBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FromLongTermRetentionBackup
Указывает на то, что этот командлет восстанавливает базу данных SQL из резервной копии длительного хранения.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromLongTermRetentionBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FromPointInTimeBackup
Указывает на то, что этот командлет восстанавливает базу данных SQL из резервной копии на момент времени.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromPointInTimeBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PointInTime
Задает момент времени в виде объекта **DateTime** , на который вы хотите восстановить базу данных SQL.
Чтобы получить объект **DateTime** , используйте командлет **Get-Date** .

Используйте этот параметр вместе с параметром *FromPointInTimeBackup* .

```yaml
Type: System.DateTime
Parameter Sets: FromPointInTimeBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: FromDeletedDatabaseBackup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов, к которой этот командлет назначает базу данных SQL.

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

### -ResourceId
Указывает идентификатор ресурса для восстановления.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ИмяСервера
Указывает имя сервера базы данных SQL.

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

### -ServiceObjectiveName
Указывает имя цели обслуживания.

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

### -TargetDatabaseName
Указывает имя базы данных, в которую будет восстановлено значение.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Восстановление базы данных SQL Azure из сбоя](https://go.microsoft.com/fwlink/?LinkId=746882)

[Восстановление базы данных SQL Azure из пользовательской ошибки](https://go.microsoft.com/fwlink/?LinkId=746944)

[Get-AzureRmSqlDatabase](./Get-AzureRmSqlDatabase.md)

[Get-AzureRMSqlDatabaseGeoBackup](./Get-AzureRMSqlDatabaseGeoBackup.md)

[Get-AzureRMSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md)

[Документация по базам данных SQL](https://docs.microsoft.com/azure/sql-database/)

