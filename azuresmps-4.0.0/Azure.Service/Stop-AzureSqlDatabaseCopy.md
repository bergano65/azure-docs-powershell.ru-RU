---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: CB601E21-424D-4B09-85E5-A4B2A5068267
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7716587787515221a6e016436a6e3d030c1ab0eb
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405624"
---
# Stop-AzureSqlDatabaseCopy

## SYNOPSIS
Прерывает непрерывное копирование.

## СИНТАКСИС

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

## ОПИСАНИЕ
**Cmdlet Stop-AzureSqlDataCopy** завершает непрерывное копирование.
Этот cmdlet останавливает перемещение данных между конечной и вторичной или целевой базой данных, а затем меняет состояние вторичной базы данных на отдельное сетевое.

Существует два способа прекращения непрерывной связи, прекращения или запланированного прекращения действия и принудительных расторжения отношений в связи с возможной потерей данных.
На сервере, на котором размещена базовая база данных, этот cmdlet можно запустить в режиме расторжения или принудительных расторжения.
На сервере, на котором размещена вторичная база данных, необходимо использовать режим принудительного прекращения действия.

Запланированное завершение будет реплицировано во вторичную базу данных до тех пор, пока все все транзакции, запланированные в базе данных, на момент запуска этого cmdlet не будут реплицированы во вторичную базу данных.
Принудительный расторжение не ждет репликации всех оставшиеся транзакций и может привести к потере данных во вторичной базе данных.

Во время ожидания состояния репликации только принудительное прекращение связи может привести к завершению непрерывной копии.
Если ожидается статус репликации, расторжение, которое не является принудительным, не поддерживается.

## ПРИМЕРЫ

### Пример 1. Прекращение непрерывной связи копирования
```
PS C:\>Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

Эта команда прерывает непрерывное копирование базы данных "Заказы" на сервере lpqd0zbr8y.
На сервере bk0b8kf658 размещена вторичная база данных.

### Пример 2. Прекращение связи непрерывной копии
```
PS C:\>$DatabaseCopy = Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders"
PS C:\> $DatabaseCopy | Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -ForcedTermination
```

Первая команда получает отношение копирования базы данных с именем Orders на сервере lpqd0zbr8y.

Вторая команда прерывает связь непрерывной копии с сервера, на котором размещена вторичная база данных.

## PARAMETERS

### -Database
Определяет объект, который представляет исходный источник базы SQL Azure.
Этот cmdlet завершает непрерывное копирование базы данных, указанной этим параметром.

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
Этот cmdlet завершает непрерывное копирование базы данных, указанной этим параметром.
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
Этот cmdlet завершает непрерывное копирование базы данных, указанной этим параметром.

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

### -ForcedTermination
Указывает на то, что этот cmdlet приводит к принудительному прекращению отношения непрерывной копии.
Принудительный выход из компании может привести к потере данных.
Чтобы выполнить этот cmdlet на сервере, на котором размещена целевая база данных, необходимо указать этот параметр.
Чтобы выполнить этот cmdlet на сервере, на котором размещена базовая база данных, если она недоступна, необходимо указать этот параметр.

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
Указывает имя вторичной базы данных.
Если указать имя, оно должно совпадать с именем в базе данных.

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
Имя сервера, на котором размещена целевая база данных.

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

### Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy

### Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database

## OUTPUTS

### Нет

## ПРИМЕЧАНИЯ
* Проверка подлинности: этот cmdlet требует проверки подлинности на основе сертификата. Пример использования проверки подлинности на основе сертификата для проверки текущей подписки см. в cmdlet **New-AzureSqlDatabaseServerContext.**
* Ограничения: на сервере, на котором размещена вторичная база данных, поддерживается только принудительный выход из системы.
* Влияние прекращения действия на бывшего вторичную базу данных: после прекращения работы она становится независимой базой данных. Если заполнение уже выполнено во вторичной базе данных, после завершения этой базы данных она будет открыта для полного доступа. Если она является базой данных для чтения и записи, бывшая вторичная база данных тоже становится доступной для чтения.

  Если в данный момент происходит начальное значение, начальное значение будет прервано, а бывшего дополнительного база данных никогда не будет видно на сервере, на котором размещена эта база данных.

* Вы можете настроить режим только для чтения в базе данных. Это гарантирует синхронизацию исходных и дополнительных баз данных после расторжения соглашения, а также гарантирует, что во время расторжения соглашения не будут совершены никакие транзакции. По окончании срока действия перенастройте источник в режим чтения и записи. При желании можно также настроить режим записи бывшего вторичная база данных.
* Мониторинг: чтобы проверить состояние операций как в источнике, так и в целевом объекте связи непрерывной копии, используйте cmdlet **Get-AzureSqlDataBaseOperation.**

## СВЯЗАННЫЕ ССЫЛКИ

[База SQL Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Операции для баз данных Azure SQL](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Остановка копирования базы данных](https://msdn.microsoft.com/en-us/library/dn509573.aspx)



[Get-AzureSqlDatabaseCopy](./Get-AzureSqlDatabaseCopy.md)

[Start-AzureSqlDatabaseCopy](./Start-AzureSqlDatabaseCopy.md)


