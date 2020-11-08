---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7F07494-FBCA-4A77-92BF-E0A2D7ACCD21
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc350cdf117ebbf72b023f64895f4c563e73566b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075845"
---
# Start-AzureSqlDatabaseCopy

## КРАТКИй обзор
Запускает операцию копирования базы данных SQL Azure.

## Максимальное

### ByInputObject
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByInputObjectContinuous
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByDatabaseName
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByDatabaseNameContinuous
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Start-AzureSqlDatabaseCopy** запускает операцию однократного копирования или непрерывную операцию копирования для конкретной базы данных Azure SQL.
Этот командлет не является транзакционным.

Исходная база данных — исходная база данных.
Копия — это дополнительная или целевая база данных.
Для непрерывной копии исходная и целевая базы данных не могут находиться на одном и том же сервере, а серверы, на которых размещаются исходная и целевая базы данных, должны входить в одну и ту же подписку.

Если параметр *ContinuousCopy* не указан, этот командлет создает единовременно одновременную копию исходной базы данных.
После получения ответа операцию можно продолжать.
Вы можете отслеживать операцию с помощью командлета Get-AzureSqlDatabaseCopy или Get-AzureSqlDatabaseOperation.

Если вы укажете *ContinuousCopy* , этот командлет создает непрерывную копию исходной базы данных.
При получении ответа операция выполняется.
Вы можете наблюдать за операцией с помощью **Get-AzureSqlDatabaseCopy** или **Get-AzureSqlDatabaseOperation**.

Вы можете создать непрерывную копию базы данных в Интернете или в автономном режиме.
Для настройки Active Geo-Replication для базы данных SQL Azure используется непрерывная оперативная копия https://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/ .
Автономная непрерывная копия используется для настройки стандартных Geo-Replication для базы данных SQL Azure https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/ .

## ИЛЛЮСТРИРУЮТ

### Пример 1: Планирование непрерывной копии базы данных
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy
```

Эта команда планирует непрерывную копию базы данных с именем "заказы" на сервере с именем lpqd0zbr8y.
Команда создает целевую базу данных на сервере с именем bk0b8kf658.

### Пример 2: создание однократного копирования на одном и том же сервере
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerDatabase "OrdersCopy"
```

Эта команда создает одновременную копию базы данных с именем "заказы" на сервере с именем lpqd0zbr8y.
Команда создает копию с именем OrdersCopy на том же сервере.

### Пример 3: Планирование непрерывной копии базы данных в автономном режиме
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy -OfflineSecondary
```

Эта команда планирует непрерывную копию базы данных с именем "заказы" на сервере с именем lpqd0zbr8y.
Эта команда создает автономную целевую базу данных на сервере с именем bk0b8kf658.

## ПАРАМЕТРЫ

### -ContinuousCopy
Указывает на то, что копия базы данных будет непрерывной копией (базой данных реплики).
Непрерывное копирование не поддерживается на одном и том же сервере.
Если этот параметр не указан, выполняется одновременная копия.
Для одновременных копий базы данных источников и партнеров должны находиться на одном и том же сервере.

```yaml
Type: SwitchParameter
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -База данных
Указывает объект, представляющий исходную базу данных SQL Azure.
Этот параметр принимает входные данные конвейера.

```yaml
Type: Database
Parameter Sets: ByInputObject, ByInputObjectContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
Указывает имя исходной базы данных.

```yaml
Type: String
Parameter Sets: ByDatabaseName, ByDatabaseNameContinuous
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

### -OfflineSecondary
Указывает на то, что непрерывное копирование является пассивным, а не активной копией.
Если исходная база данных является базой данных стандартного выпуска, этот параметр является обязательным.
Если указан этот параметр, необходимо также указать *ContinuousCopy* .

```yaml
Type: SwitchParameter
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerDatabase
Указывает имя целевой базы данных.
Если указан параметр *ContinuousCopy* , значение для *PartnerDatabase* должно совпадать с именем исходной базы данных.
Если вы не указали *ContinuousCopy* , необходимо указать имя целевой базы данных, которое может отличаться от имени базы данных-источника.

```yaml
Type: String
Parameter Sets: ByInputObject, ByDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerServer
Указывает имя сервера, на котором размещена целевая база данных.
Этот сервер должен находиться в той же подписке Azure, что и сервер исходной базы данных.

```yaml
Type: String
Parameter Sets: ByInputObject, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: True
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

### Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. Database

## НАПРЯЖЕНИЕ

### Microsoft. WindowsAzure. Commands. SqlDatabase. Model. DatabaseCopy

## Пуск
* Проверка подлинности: для этого командлета требуется проверка подлинности на основе сертификата. Пример использования проверки подлинности на основе сертификатов для настройки текущей подписки можно найти в разделе New-AzureSqlDatabaseServerContext командлет.
* Наблюдение: Проверка состояния одного или нескольких связей непрерывной копии, которые активны на сервере, с помощью командлета **Get-AzureSqlDatabaseCopy** . Чтобы проверить состояние операций как в исходном, так и на целевом объекте отношения непрерывной копии, используйте командлет **Get-AzureSqlDatabaseOperation** .

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[База данных SQL Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Операции для баз данных SQL Azure](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Начать копирование базы данных](https://msdn.microsoft.com/en-us/library/azure/dn509576.aspx)

[Командлеты базы данных SQL Azure](./Azure.SQLDatabase.md)

[Get-AzureSqlDatabaseCopy](./Get-AzureSqlDatabaseCopy.md)

[Остановить-AzureSqlDatabaseCopy](./Stop-AzureSqlDatabaseCopy.md)


