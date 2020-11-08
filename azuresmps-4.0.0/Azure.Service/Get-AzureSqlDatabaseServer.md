---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 0ACEDE22-1C2B-4846-A949-710AF6C148D0
online version: ''
schema: 2.0.0
ms.openlocfilehash: d513d6d019c84984923541624063e657e2250b61
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075571"
---
# Get-AzureSqlDatabaseServer

## КРАТКИй обзор
Получает сведения о серверах баз данных Azure SQL.

## Максимальное

```
Get-AzureSqlDatabaseServer [-ServerName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureSqlDatabaseServer** получает сведения о экземплярах сервера базы данных SQL Azure в текущей подписке.
Если указать сервер по имени, этот командлет возвращает объект, содержащий сведения об этом сервере.
В противном случае командлет возвращает сведения обо всех серверах.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение сведений обо всех серверах
```
PS C:\> Get-AzureSqlDatabaseServer
```

Эта команда возвращает сведения обо всех экземплярах сервера базы данных SQL Azure в текущей подписке.

### Пример 2: получение сведений о конкретном сервере
```
PS C:\> Get-AzureSqlDatabaseServer -ServerName "lpqd0zbr8y"
```

Эта команда возвращает сведения о сервере с именем lpqd0zbr8y.

## ПАРАМЕТРЫ

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
Указывает имя сервера, который удаляет этот командлет.
Укажите имя сервера, а не полное DNS-имя.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Microsoft. WindowsAzure. Commands. SqlDatabase. Model. SqlDatabaseServerContext

## НАПРЯЖЕНИЕ

### IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext\>

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[База данных SQL Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Серверы списков](https://msdn.microsoft.com/en-us/library/azure/dn505702.aspx)

[Операции для баз данных SQL Azure](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[New-AzureSqlDatabaseServer](./New-AzureSqlDatabaseServer.md)

[Remove-AzureSqlDatabaseServer](./Remove-AzureSqlDatabaseServer.md)

[Set-AzureSqlDatabaseServer](./Set-AzureSqlDatabaseServer.md)


