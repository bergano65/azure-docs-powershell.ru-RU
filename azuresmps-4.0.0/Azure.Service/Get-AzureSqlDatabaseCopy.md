---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5AEF7D44-624D-4794-86FF-156E6729BB56
online version: ''
schema: 2.0.0
ms.openlocfilehash: 95e276bf6af11698a4b3b82077175ec2ede2d7dc
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402428"
---
# Get-AzureSqlDatabaseCopy

## SYNOPSIS
Проверяет состояние связей копирования.

## СИНТАКСИС

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

## ОПИСАНИЕ
**Cmdlet Get-AzureSqlDataCopy** проверяет состояние одной или более активных связей копирования.
Запустите этот cmdlet после запуска Start-AzureSqlDatabaseCopy или Stop-AzureSqlDatabaseCopy.
Вы можете проверить конкретную связь копирования, все связи копирования или отфильтрованный список связей копирования, например все копии на определенном целевом сервере.
Этот cmdlet можно выполнить на сервере, на котором размещена базовая или целевая база данных.

Этот cmdlet является синхронным.
Этот cmdlet блокирует консоль Azure PowerShell, пока не будет возвращен объект состояния.

Параметры *PartnerServer* и *PartnerDatabase* необязательны.
Если ни один из параметров не указан, этот cmdlet возвращает таблицу результатов.
Чтобы увидеть состояние только для конкретной базы данных, укажите оба параметра.

## ПРИМЕРЫ

### Пример 1. Просмотр состояния копии базы данных
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

Эта команда получает состояние базы данных "Заказы" на сервере lpqd0zbr8y.
Параметр *PartnerServer ограничивает* эту команду сервером bk0b8kf658.

### Пример 2. Получить состояние всех копий на сервереGet состояние всех копий на сервере
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y"
```

Эта команда получает состояние всех активных копий на сервере lpqd0zbr8y.

## PARAMETERS

### -Database
Определяет объект, который представляет исходный источник базы SQL Azure.
Этот cmdlet получает состояние копии базы данных, указанной этим параметром.

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
Определяет объект, который представляет базу данных.
Этот cmdlet получает состояние копии базы данных, указанной этим параметром.
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
Указывает имя базы данных.
Этот cmdlet возвращает состояние копии базы данных, указанной этим параметром.

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
Указывает имя вторичной базы данных.
Если эта база данных не найдена в sys.dm_database_copies управления, этот cmdlet возвращает пустой объект состояния.

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
Имя сервера, на котором размещена целевая база данных.
Если этот сервер не найден в sys.dm_database_copies управления, этот cmdlet возвращает пустой объект состояния.

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
Определяет профиль Azure, для которого читается этот cmdlet.
Если не указать профиль, этот cmdlet будет читать данные из локального профиля по умолчанию.

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

### -ServerName
Имя сервера, на котором находится копия базы данных.

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
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy

### Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database

## OUTPUTS

### Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy

## ПРИМЕЧАНИЯ
* Проверка подлинности: этот cmdlet требует проверки подлинности на основе сертификата. Пример использования проверки подлинности на основе сертификата для проверки текущей подписки см. в New-AzureSqlDatabaseServerContext.

## СВЯЗАННЫЕ ССЫЛКИ

[База SQL Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Операции для баз данных Azure SQL](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)



[Start-AzureSqlDatabaseCopy](./Start-AzureSqlDatabaseCopy.md)

[Stop-AzureSqlDatabaseCopy](./Stop-AzureSqlDatabaseCopy.md)


