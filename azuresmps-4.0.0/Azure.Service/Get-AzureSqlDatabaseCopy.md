---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5AEF7D44-624D-4794-86FF-156E6729BB56
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8752766572975ef97094a3915446086c903a7fd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076295"
---
# Get-AzureSqlDatabaseCopy

## КРАТКИй обзор
Проверка состояния связей при копировании.

## Максимальное

### ByServerNameOnly (по умолчанию)
```
Get-AzureSqlDatabaseCopy -ServerName <String> [-DatabaseName <String>] [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByInputObject
```
Get-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ByDatabase
```
Get-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureSqlDatabaseCopy** проверяет состояние одного или нескольких активных связей копий.
Запустите этот командлет после запуска командлета Start-AzureSqlDatabaseCopy или Stop-AzureSqlDatabaseCopy.
Вы можете проверить связь с определенным копированием, все связи копий или отфильтрованный список связей копий, например все копии на конкретном целевом сервере.
Этот командлет можно выполнить на сервере, на котором размещается исходная или целевая база данных.

Этот командлет является синхронным.
Командлет блокирует консоль Azure PowerShell, пока не вернет объект Status.

Параметры *PartnerServer* и *PartnerDatabase* являются необязательными.
Если не указать ни один из этих параметров, этот командлет возвращает таблицу результатов.
Чтобы просмотреть состояние только для определенной базы данных, укажите оба параметра.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение состояния копии базы данных
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

Эта команда получает состояние базы данных "заказы" на сервере с именем lpqd0zbr8y.
Параметр *PartnerServer* ограничивает эту команду на сервер bk0b8kf658.

### Пример 2: получение состояния всех копий на serverGet состояние всех копий на сервере
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y"
```

Эта команда возвращает состояние всех активных копий на сервере с именем lpqd0zbr8y.

## ПАРАМЕТРЫ

### -База данных
Указывает объект, представляющий исходную базу данных SQL Azure.
Этот командлет получает состояние копирования базы данных, которую указывает этот параметр.

```yaml
Type: Database
Parameter Sets: ByDatabase
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseCopy
Указывает объект, представляющий базу данных.
Этот командлет получает состояние копирования базы данных, которую указывает этот параметр.
Этот параметр принимает входные данные конвейера.

```yaml
Type: DatabaseCopy
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
Указывает имя исходной базы данных.
Этот командлет получает состояние копии базы данных, которую указывает этот параметр.

```yaml
Type: String
Parameter Sets: ByServerNameOnly
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerDatabase
Указывает имя базы данных получателя.
Если эта база данных не найдена в динамическом административном представлении sys.dm_database_copies, этот командлет возвращает пустой объект Status.

```yaml
Type: String
Parameter Sets: ByServerNameOnly, ByDatabase
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerServer
Указывает имя сервера, на котором размещена целевая база данных.
Если этот сервер не найден в динамическом административном представлении sys.dm_database_copies, этот командлет возвращает пустой объект Status.

```yaml
Type: String
Parameter Sets: ByServerNameOnly, ByDatabase
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

### -ИмяСервера
Указывает имя сервера, на котором находится копия базы данных.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Microsoft. WindowsAzure. Commands. SqlDatabase. Model. DatabaseCopy

### Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. Database

## НАПРЯЖЕНИЕ

### Microsoft. WindowsAzure. Commands. SqlDatabase. Model. DatabaseCopy

## Пуск
* Проверка подлинности: для этого командлета требуется проверка подлинности на основе сертификата. Пример использования проверки подлинности на основе сертификатов для настройки текущей подписки приведен в описании командлета New-AzureSqlDatabaseServerContext.

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[База данных SQL Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Операции для баз данных SQL Azure](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Командлеты базы данных SQL Azure](./Azure.SQLDatabase.md)

[Start-AzureSqlDatabaseCopy](./Start-AzureSqlDatabaseCopy.md)

[Остановить-AzureSqlDatabaseCopy](./Stop-AzureSqlDatabaseCopy.md)


