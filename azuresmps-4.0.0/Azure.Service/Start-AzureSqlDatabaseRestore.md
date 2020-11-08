---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 383F36F3-3F52-4FC3-99F7-831096E6037D
online version: ''
schema: 2.0.0
ms.openlocfilehash: ff7c7cd50b06a4110b6af12611f3d91eaedfd227
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075426"
---
# Start-AzureSqlDatabaseRestore

## КРАТКИй обзор
Выполняет восстановление базы данных на момент времени.

## Максимальное

### BySourceDatabaseObject
```
Start-AzureSqlDatabaseRestore [-SourceServerName <String>] -SourceDatabase <Database>
 [-TargetServerName <String>] -TargetDatabaseName <String> [-PointInTime <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### BySourceRestorableDroppedDatabaseObject
```
Start-AzureSqlDatabaseRestore [-SourceServerName <String>]
 -SourceRestorableDroppedDatabase <RestorableDroppedDatabase> [-TargetServerName <String>]
 -TargetDatabaseName <String> [-PointInTime <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### BySourceDatabaseName
```
Start-AzureSqlDatabaseRestore -SourceServerName <String> -SourceDatabaseName <String>
 [-TargetServerName <String>] -TargetDatabaseName <String> [-PointInTime <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### BySourceRestorableDroppedDatabaseName
```
Start-AzureSqlDatabaseRestore -SourceServerName <String> -SourceDatabaseName <String>
 -SourceDatabaseDeletionDate <DateTime> [-TargetServerName <String>] [-RestorableDropped]
 -TargetDatabaseName <String> [-PointInTime <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Start-AzureSqlDatabaseRestore** выполняет восстановление базовой, стандартной или расширенной базы данных на момент времени.
База данных Azure SQL сохраняет основные резервные копии базы данных 7 дней, Standard в течение 14 дней и Premium в течение 35 дней.
Операция восстановления создает новую базу данных.
Если исходная база данных не удалена, параметр *SourceDatabaseName* и *TargetDatabaseName* должен иметь разные значения.

База данных SQL Azure в настоящее время не поддерживает восстановление на нескольких серверах.
Имена исходного и целевого серверов должны совпадать.

## ИЛЛЮСТРИРУЮТ

### Пример 1: восстановление базы данных, указанной как объект, на определенный момент времени
```
PS C:\> $Database = Get-AzureSqlDatabase -ServerName "Server01" -DatabaseName "Database17" 
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceDatabase $Database -TargetDatabaseName "DatabaseRestored" -PointInTime "2013-01-01 06:00:00"
```

Первая команда получает объект базы данных с именем Database17 на сервере с именем Server01 и сохраняет его в переменной $Database.

Вторая команда восстанавливает базу данных в определенный момент времени.
Команда задает имя для новой базы данных.

### Пример 2: восстановление базы данных, указанной по имени, на определенный момент времени
```
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceServerName "Server01" -SourceDatabaseName "Database17" -TargetDatabaseName "DatabaseRestored" -PointInTime "2013-01-01 06:00:00"
```

Эта команда восстанавливает базу данных с именем Database17 на определенный момент времени.
Команда задает имя для новой базы данных.

### Пример 3: восстановление удаленной базы данных, указанной в качестве объекта, на определенный момент времени
```
PS C:\> $Database = Get-AzureSqlDatabase -RestorableDropped -ServerName "Server01" -DatabaseName "Database01" -DatabaseDeletionDate "2012-11-09T22:59:43.000Z" 
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceRestorableDroppedDatabase $Database -TargetDatabaseName "DroppedDatabaseRestored"
```

Первая команда получает объект базы данных с именем Database01 на сервере с именем Server01.
Команда задает параметр *RestorableDropped* .
Таким образом, командлет возвращает restorable удаленную базу данных с указанной точкой восстановления.
Команда сохраняет этот объект базы данных в переменной $Database.

Вторая команда восстанавливает удаленную базу данных, указанную в $Database.
Команда задает имя для новой базы данных.

## ПАРАМЕТРЫ

### -PointInTime
Указывает точку восстановления, в которую нужно восстановить базу данных.
По завершении операции восстановления база данных восстанавливается в состояние, которое оно указывает на дату и время, указанные этим параметром.
По умолчанию для реальной базы данных этот параметр установлен на текущее время, а для удаленной базы данных этот командлет использует время удаления базы данных.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Указывает профиль Azure, из которого считывается этот командлет.
Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestorableDropped
Указывает на то, что этот командлет восстанавливает удаленную базу данных restorable.

```yaml
Type: SwitchParameter
Parameter Sets: BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceDatabase
Указывает имя базы данных, которая восстанавливается этим командлетом.

```yaml
Type: Database
Parameter Sets: BySourceDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SourceDatabaseDeletionDate
Указывает дату и время удаления базы данных.
Если указать время, совпадающее с фактическим временем удаления базы данных, необходимо включить миллисекунды.

```yaml
Type: DateTime
Parameter Sets: BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceDatabaseName
Указывает имя базы данных Live, которое восстанавливается этим командлетом.

```yaml
Type: String
Parameter Sets: BySourceDatabaseName, BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceRestorableDroppedDatabase
Указывает объект, представляющий restorable удаленную базу данных, которая восстанавливается этим командлетом.
Чтобы получить объект **RestorableDroppedDatabase** , используйте командлет Get-AzureSqlDatabase и укажите параметр *RestorableDropped* .

```yaml
Type: RestorableDroppedDatabase
Parameter Sets: BySourceRestorableDroppedDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SourceServerName
Указывает имя сервера, на котором находится база данных источника и что она запущена, или на которой была выполнена удаленная база данных.

```yaml
Type: String
Parameter Sets: BySourceDatabaseObject, BySourceRestorableDroppedDatabaseObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: BySourceDatabaseName, BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetDatabaseName
Указывает имя новой базы данных, созданной операцией восстановления.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetServerName
Указывает имя сервера, на который этот командлет восстанавливает базу данных.

База данных SQL Azure в настоящее время не поддерживает восстановление на нескольких серверах.
Имена исходного и целевого серверов должны совпадать.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. RestorableDroppedDatabase

### Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. Database

## НАПРЯЖЕНИЕ

### Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. RestoreDatabaseOperation

## Пуск
* Для запуска этого командлета необходимо использовать проверку подлинности на основе сертификатов. На компьютере, на котором запускается этот командлет, выполните следующие команды: 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[База данных SQL Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Создание запроса на восстановление базы данных](https://msdn.microsoft.com/en-us/library/dn509571.aspx)

[Операции для баз данных SQL Azure](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)


