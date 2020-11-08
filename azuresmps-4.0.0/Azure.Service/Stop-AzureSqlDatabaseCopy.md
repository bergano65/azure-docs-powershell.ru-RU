---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: CB601E21-424D-4B09-85E5-A4B2A5068267
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2b7674cb5b7abc489dc6aa6d3746f499b9686312
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076403"
---
# Stop-AzureSqlDatabaseCopy

## КРАТКИй обзор
Завершает отношение непрерывного копирования.

## Максимальное

### ByInputObject
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-ForcedTermination] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByDatabase
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByDatabaseName
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Stop-AzureSqlDatabaseCopy** завершает связь непрерывного копирования.
Этот командлет останавливает перемещение данных между исходной базой данных и дополнительной или целевой базой данных, а затем изменяет состояние базы данных-получателя на автономную базу данных в Интернете.

Существует два способа завершить отношение непрерывного копирования, прекращение или запланированное прекращение и принудительное прекращение с возможной потерей данных.
На сервере, на котором размещается исходная база данных, вы можете запустить этот командлет в режиме завершения или принудительного завершения.
На сервере, на котором размещается база данных получателя, необходимо использовать режим принудительного завершения.

Запланированное прекращение ожиданий до тех пор, пока все зафиксированные транзакции в исходной базе данных не будут реплицированы в базу данных-получатель после выполнения командлета.
Принудительное прекращение не ждет репликации всех незавершенных транзакций и может привести к потере данных в базе данных получателя.

Несмотря на то, что состояние репликации — ОЖИДАНИе, только принудительное завершение может успешно завершить связь непрерывного копирования.
Если состояние репликации — ОЖИДАНИе, оконечное значение, которое не было принудительно, не поддерживается.

## ИЛЛЮСТРИРУЮТ

### Пример 1: прекращение связи непрерывной копии
```
PS C:\>Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

Эта команда завершает связь непрерывной копии для базы данных "заказы" на сервере с именем lpqd0zbr8y.
Сервер с именем bk0b8kf658 размещает базу данных получателя.

### Пример 2: принудительное прекращение связи непрерывной копии
```
PS C:\>$DatabaseCopy = Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders"
PS C:\> $DatabaseCopy | Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -ForcedTermination
```

Первая команда получает отношение копирования базы данных "заказы" на сервере с именем lpqd0zbr8y.

Вторая команда принудительно завершает связь непрерывной копии с сервера, на котором размещается база данных-получатель.

## ПАРАМЕТРЫ

### -База данных
Указывает объект, представляющий исходную базу данных SQL Azure.
Этот командлет завершает связь непрерывной копии базы данных, которую указывает этот параметр.

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
Этот командлет завершает связь непрерывной копии базы данных, которую указывает этот параметр.
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
Этот командлет завершает связь непрерывной копии базы данных, которую указывает этот параметр.

```yaml
Type: String
Parameter Sets: ByDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Принудительное выполнение команды без запроса подтверждения пользователя.

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

### -ForcedTermination
Указывает на то, что этот командлет приводит к принудительному завершению связи непрерывного копирования.
Принудительное прекращение работы может привести к потере данных.
Чтобы выполнить этот командлет на сервере, на котором размещена целевая база данных, необходимо указать этот параметр.
Чтобы выполнить этот командлет на сервере, на котором размещается исходная база данных, необходимо указать этот параметр, если база данных-получатель недоступна.

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

### -PartnerDatabase
Указывает имя базы данных получателя.
Если указать имя, оно должно совпадать с именем исходной базы данных.

```yaml
Type: String
Parameter Sets: ByDatabase, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerServer
Указывает имя сервера, на котором размещена целевая база данных.

```yaml
Type: String
Parameter Sets: ByDatabase, ByDatabaseName
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
Указывает имя сервера, на котором находится исходная база данных.

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

### -Confirm
Запрашивает подтверждение перед запуском командлета.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Microsoft. WindowsAzure. Commands. SqlDatabase. Model. DatabaseCopy

### Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. Database

## НАПРЯЖЕНИЕ

### Ничего

## Пуск
* Проверка подлинности: для этого командлета требуется проверка подлинности на основе сертификата. Пример использования проверки подлинности на основе сертификатов для настройки текущей подписки можно найти в командлете **New-AzureSqlDatabaseServerContext** .
* Ограничения: на сервере, на котором размещается база данных получателя, поддерживается только принудительное прекращение работы.
* Последствия прекращения работы в бывшей базе данных получателя: после завершения работы база данных получателя становится независимой базой данных. Если заполнение уже завершено в базе данных получателя, после того как вы откроете эту базу данных для получения полного доступа. Если исходная база данных является базой данных для чтения и записи, она также становится базой данных для чтения и записи.

  Если в данный момент выполняется заполнение, инициализация будет прервана, а Предыдущая база данных не будет видна на сервере, на котором размещается база данных получателя.

* Исходную базу данных можно выбрать в режиме "только для чтения". Это гарантирует, что исходная и база данных синхронизируются после завершения и гарантирует, что транзакции не будут зафиксированы. После завершения оконечного напряжения установите для источника обратно режим чтения и записи. При необходимости вы также можете настроить для базы данных-получателя в режим чтения и записи.
* Наблюдение: чтобы проверить состояние операций как в исходном, так и на целевом элементе отношения непрерывного копирования, используйте командлет **Get-AzureSqlDatabaseOperation** .

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[База данных SQL Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Операции для баз данных SQL Azure](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Остановить копирование базы данных](https://msdn.microsoft.com/en-us/library/dn509573.aspx)

[Командлеты базы данных SQL Azure](./Azure.SQLDatabase.md)

[Get-AzureSqlDatabaseCopy](./Get-AzureSqlDatabaseCopy.md)

[Start-AzureSqlDatabaseCopy](./Start-AzureSqlDatabaseCopy.md)


