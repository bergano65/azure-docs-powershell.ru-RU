---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 56026A74-A6DC-47A5-9643-5828C3D0E83B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 32219154f2036ee028b05a369c46be1d8e1def87
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076293"
---
# Get-AzureSqlDatabaseOperation

## КРАТКИй обзор
Возвращает состояние операций с базой данных на сервере Azure.

## Максимальное

### ByConnectionContext (по умолчанию)
```
Get-AzureSqlDatabaseOperation -ConnectionContext <IServerDataServiceContext> [-Database <Database>]
 [-DatabaseName <String>] [-OperationGuid <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByServerName
```
Get-AzureSqlDatabaseOperation -ServerName <String> [-Database <Database>] [-DatabaseName <String>]
 [-OperationGuid <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureSqlDatabaseOperation** получает состояние операций базы данных на указанном сервере Azure.
Если указан только параметр *ServerName* или *ConnectionContext* , командлет получает все операции с базой данных сервера.
Если вы также указываете базу данных с помощью параметра *Database* или *DatabaseName* , этот командлет получает все операции для указанной базы данных.
Если вы укажете идентификатор GUID операции, *ServerName* или *ConnectionContext* , командлет возвращает одну операцию базы данных.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение состояния всех операций с базой данных для базы данных
```
PS C:\> $Operations = Get-AzureSqlDatabaseOperation -ConnectionContext $Context -DatabaseName "Database17"
```

Эта команда возвращает состояние всех операций с базой данных в базе данных с именем Database17 на сервере, которое указывает контекстом подключения $Context.

### Пример 2: получение состояния всех операций базы данных для сервера
```
PS C:\> $Operations = Get-AzureSqlDatabaseOperation -ConnectionContext $Context
```

Эта команда возвращает состояние всех операций с базой данных на сервере, которые $Context указывает контекстом подключения.

## ПАРАМЕТРЫ

### -ConnectionContext
Указывает контекст подключения сервера.

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
Указывает объект, представляющий базу данных SQL Azure.
Если указать этот параметр, необходимо указать параметр *ServerName* или параметр *ConnectionContext* .

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

### -DatabaseName
Указывает имя базы данных.
Если указать этот параметр, необходимо указать параметр *ServerName* или параметр *ConnectionContext* .

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

### -OperationGuid
Указывает ИД операции, представляющей определенную операцию с базой данных, для которой этот командлет получает состояние.
Идентификаторы операций можно получить, запросив все операции с базой данных для базы данных или сервера SQL Azure.
Если указать этот параметр, необходимо указать параметр *ServerName* или параметр *ConnectionContext* .

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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
Указывает имя сервера.

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

### Microsoft. WindowsAzure. Commands. SqlDatabase. Model. SqlDatabaseServerContext

### System. GUID

## НАПРЯЖЕНИЕ

### Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. Database. DatabaseOperationResponseList []
Этот командлет возвращает массив объектов **DatabaseOperationResponseList** , если вы получаете несколько операций.

### Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. Database. DatabaseOperationResponse

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[База данных SQL Azure](https://msdn.microsoft.com/library/ee336279.aspx)

[Состояние операции с базой данных](https://msdn.microsoft.com/en-us/library/azure/dn720371.aspx)

[Операции для баз данных SQL Azure](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)

[New-AzureSqlDatabaseServerContext](./New-AzureSqlDatabaseServerContext.md)


