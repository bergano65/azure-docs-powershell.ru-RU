---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 7427A101-9439-45B9-B72E-F8C2DA85E412
online version: ''
schema: 2.0.0
ms.openlocfilehash: c10ae808d105079b9739516bf9eaf316241b1b11
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076298"
---
# Get-AzureSqlDatabase

## КРАТКИй обзор
Извлекает одну или несколько баз данных.

## Максимальное

### ByConnectionContext (по умолчанию)
```
Get-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> [-Database <Database>]
 [-DatabaseName <String>] [-RestorableDropped] [-RestorableDroppedDatabase <RestorableDroppedDatabase>]
 [-DatabaseDeletionDate <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByServerName
```
Get-AzureSqlDatabase -ServerName <String> [-Database <Database>] [-DatabaseName <String>] [-RestorableDropped]
 [-RestorableDroppedDatabase <RestorableDroppedDatabase>] [-DatabaseDeletionDate <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureSqlDatabase** получает один или несколько экземпляров базы данных Azure SQL с сервера базы данных Azure SQL.
Вы можете указать сервер с контекстом подключения к серверу базы данных SQL Azure, который вы создаете с помощью командлета **New-AzureSqlDatabaseServerContext** .
Или, если указать имя сервера базы данных SQL Azure, командлет использует текущие сведения о подписке Azure для проверки подлинности запроса на доступ к серверу.

Если не указать базу данных, командлет **Get-AzureSqlDatabase** возвращает все базы данных с указанного сервера.

Получение restorable удаленных баз данных:

Извлечение restorable удаленных баз данных с помощью параметра *RestorableDropped* .
Для возврата всех restorable удаленных баз данных используйте параметр *RestorableDropped* без *DatabaseName* и *DatabaseDeletionDate*.
Чтобы вернуть определенную restorable удаленную базу данных, используйте параметр *RestorableDropped* с параметрами *DatabaseName* и *DatabaseDeletionDate* .
При извлечении определенной restorable удаленной базы данных с помощью параметра *DatabaseName* необходимо также указать параметр *DatabaseDeletionDate* , а указанное значение *DatabaseDeletionDate* должно содержать миллисекунды для соответствия необходимой базе данных.

Командлет **Get-AzureSqlDatabase** возвращает либо все restorable удаленные базы данных на сервере, либо определенную базу данных, которая соответствует обоим параметрам *DatabaseName* и *DatabaseDeletionDate*.
Для возврата restorable удаленным базам данных, которые удовлетворяют разным критериям, таким как все restorable удаленные базы данных с определенным именем, нужно вернуть все restorable удаленные базы данных, а затем отфильтровать результаты на клиенте.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение всех баз данных на сервере
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y"
```

Эта команда извлекает все базы данных на сервере с именем lpqd0zbr8y.

### Пример 2: получение всех удаленных баз данных restorable на сервере
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -RestorableDropped
```

Эта команда извлекает все удаленные базы данных restorable на сервере с именем lpqd0zbr8y.

### Пример 3: получение базы данных с сервера, указанного контекстом подключения
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
```

Эта команда извлекает базу данных с именем Database01 с сервера, указанного контекстом подключения $Context.

### Пример 4: сохранение объекта базы данных в переменной
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
```

Эта команда извлекает базу данных с именем Database01 с сервера с именем lpqd0zbr8y.
Объект базы данных сохраняется в переменной $Database 01.

### Пример 5: получение restorable удаленной базы данных
```
PS C:\> $DroppedDB = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01" -DatabaseDeletionDate "2012-11-09T22:59:43.000Z" -RestorableDropped
```

Эта команда извлекает restorable удаленную базу данных с именем Database01, которая была удалена на 11/9/2012 с сервера с именем lpqd0zbr8y.
Эта команда сохраняет результаты в переменной $DroppedDB.

### Пример 6: получение всех restorable удаленных баз данных на сервере и фильтрация результатов
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -RestorableDropped | Where-Object {$_.Name -eq "ContactDB"}
```

Эта команда извлекает все удаленные базы данных restorable на сервере с именем lpqd0zbr8y, а затем фильтрует результаты только для баз данных с именем ContactDB.

## ПАРАМЕТРЫ

### -ConnectionContext
Указывает контекст подключения сервера, с которого требуется получить базу данных.

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -База данных
Указывает объект, представляющий базу данных, которую этот командлет извлекает.

```yaml
Type: Database
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseDeletionDate
Указывает дату и время удаления.
Если указан параметр *RestorableDropped* , укажите этот параметр, чтобы получить restorable удаленную базу данных, исходя из даты и времени удаления.

Параметр *DatabaseDeletionDate* должен содержать миллисекунды в соответствии со временем нужной базы данных.
Если задать значение без миллисекунд, база данных не будет найдена.

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

### -DatabaseName
Указывает имя базы данных, которую этот командлет извлекает.

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
Указывает на то, что этот командлет возвращает объекты *RestorableDroppedDatabase* , а не объекты *базы данных* .
Вы можете использовать параметр *DatabaseDeletionDate* , чтобы выбрать определенную restorable удаленную базу данных.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestorableDroppedDatabase
Указывает объект, представляющий restorable удаленную базу данных, которую этот командлет извлекает.

```yaml
Type: RestorableDroppedDatabase
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ИмяСервера
Указывает имя сервера, содержащего базу данных, которую этот командлет извлекает.
Командлет использует текущую подписку Azure для доступа к серверу.

```yaml
Type: String
Parameter Sets: ByServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. Database

### Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. RestorableDroppedDatabase

## НАПРЯЖЕНИЕ

### IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database\>
Этот командлет возвращает объект *базы данных* , если не указан параметр *RestorableDropped* .

### IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase\>
Этот командлет возвращает объект *RestorableDroppedDatabase* , если указан параметр *RestorableDropped* .

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[База данных SQL Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Операции для баз данных SQL Azure](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[New-AzureSqlDatabase](./New-AzureSqlDatabase.md)

[New-AzureSqlDatabaseServerContext](./New-AzureSqlDatabaseServerContext.md)

[Remove-AzureSqlDatabase](./Remove-AzureSqlDatabase.md)

[Set-AzureSqlDatabase](./Set-AzureSqlDatabase.md)


