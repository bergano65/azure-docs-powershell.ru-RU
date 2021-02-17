---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7F07494-FBCA-4A77-92BF-E0A2D7ACCD21
online version: ''
schema: 2.0.0
ms.openlocfilehash: 35e29655e8447644b6c5449309424595e45ca187
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100413070"
---
# Start-AzureSqlDatabaseCopy

## SYNOPSIS
Начинает операцию копирования базы данных Azure SQL.

## СИНТАКСИС

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

## ОПИСАНИЕ
Для запуска однобайтового копирования или непрерывной копии определенной базы данных Azure SQL запускается проектный SQL **AzureSqlDataCopy.**
Этот cmdlet не является транзакцией.

Исходная база данных является исходной.
Копия является вторичной или целевой базой данных.
При непрерывной копии исходные и целевые базы данных не могут находиться на одном сервере, а серверы, на основе которой они находятся, должны быть частью одной подписки.

Если параметр *ContinuousCopy* не задан, этот cmdlet создает разовую копию базы данных.
После того как ответ будет получен, операция по-прежнему может быть в процессе выполнения.
Вы можете отслеживать операцию с помощью Get-AzureSqlDatabaseCopy или Get-AzureSqlDatabaseOperation.

Если задать *Режим ContinuousCopy,* этот cmdlet создаст рывную копию базы данных.
После того как ответ будет получен, операция будет в процессе выполнения.
Вы можете отслеживать операцию с помощью **Get-AzureSqlDatabaseCopy** или **Get-AzureSqlDatabaseOperation.**

Вы можете создать непрерывную копию в виде интерактивной или автономной базы данных.
Веб-лентоемая копия используется для настройки active Geo-Replication для базы данных Azure https://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/ SQL.
Для настройки стандартной Geo-Replication для базы данных Azure SQL используется SQL копировать. https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/

## ПРИМЕРЫ

### Пример 1. Запланируйте непрерывную копию базы данных
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy
```

Эта команда запланирует непрерывную копию базы данных "Заказы" на сервере lpqd0zbr8y.
Команда создает целевую базу данных на сервере с именем bk0b8kf658.

### Пример 2. Создание одно экземпляра на одном сервере
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerDatabase "OrdersCopy"
```

Эта команда создает разовую копию базы данных "Заказы" на сервере с именем lpqd0zbr8y.
Команда создает копию с именем OrdersCopy на том же сервере.

### Пример 3. Запланируйте непрерывную копию автономной базы данных
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy -OfflineSecondary
```

Эта команда запланирует непрерывную копию базы данных "Заказы" на сервере lpqd0zbr8y.
Эта команда создает целевую базу данных автономного режима на сервере bk0b8kf658.

## PARAMETERS

### -ContinuousCopy
Означает, что копия базы данных будет непрерывной (копией).
Непрерывная копия не поддерживается на одном сервере.
Если этот параметр не задан, выполняется разовая копия.
Для разной копии исходные и партнерские базы данных должны быть на одном сервере.

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

### -Database
Определяет объект, который представляет исходный источник базы SQL Azure.
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
Указывает имя базы данных.

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
Запуск команды без запроса подтверждения.

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
Указывает, что непрерывной копией является пассивная, а не активная копия.
Если базой данных является standard edition, этот параметр является required.
Если этот параметр задан, необходимо также у *указывается ContinuousCopy.*

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
Если для *параметра ContinuousCopy задан параметр ContinuousCopy,* значение *partnerDatabase* должно совпадать с именем базы данных.
Если не указать *ContinuousCopy,* необходимо указать имя целевой базы данных, которое может быть другим.

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
Имя сервера, на котором размещена целевая база данных.
Этот сервер должен быть в той же подписке Azure, что и исходный сервер базы данных.

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
Указывает имя сервера, на котором находится базовая база данных.

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
Перед запуском cmdlet вам будет предложено подтвердить его.

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
Показывает, что произойдет при запуске cmdlet.
Этот cmdlet не будет выполниться.

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
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database

## OUTPUTS

### Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy

## ПРИМЕЧАНИЯ
* Проверка подлинности: этот cmdlet требует проверки подлинности на основе сертификата. Пример использования проверки подлинности на основе сертификата для проверки текущей подписки см. в New-AzureSqlDatabaseServerContext.
* Мониторинг. Чтобы проверить состояние активных на сервере связей непрерывной копии, используйте для этого cmdlet **Get-AzureSqlDataBaseCopy.** Чтобы проверить состояние операций как в источнике, так и в целевом объекте непрерывной копии, воспользуйтесь cmdlet **Get-AzureSqlDatabaseOperation.**

## СВЯЗАННЫЕ ССЫЛКИ

[База SQL Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Операции для баз данных Azure SQL](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Запуск копирования базы данных](https://msdn.microsoft.com/en-us/library/azure/dn509576.aspx)



[Get-AzureSqlDatabaseCopy](./Get-AzureSqlDatabaseCopy.md)

[Stop-AzureSqlDatabaseCopy](./Stop-AzureSqlDatabaseCopy.md)


