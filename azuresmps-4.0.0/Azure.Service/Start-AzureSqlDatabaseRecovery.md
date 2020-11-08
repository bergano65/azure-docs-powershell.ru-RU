---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F63769D6-9A31-4A67-972A-1E0428853C86
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88f61718e363a630b70519590025a6da80364aeb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075423"
---
# Start-AzureSqlDatabaseRecovery

## КРАТКИй обзор
Инициирует запрос на восстановление для базы данных.

## Максимальное

### BySourceDatabaseName
```
Start-AzureSqlDatabaseRecovery -SourceServerName <String> -SourceDatabaseName <String>
 [-TargetServerName <String>] [-TargetDatabaseName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### BySourceDatabaseObject
```
Start-AzureSqlDatabaseRecovery -SourceDatabase <RecoverableDatabase> [-TargetServerName <String>]
 [-TargetDatabaseName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Start-AzureSqlDatabaseRecovery** инициирует запрос на восстановление для реальной или удаленной базы данных.
Этот командлет поддерживает базовое восстановление, которое использует последнюю известную доступную резервную копию для базы данных.
Операция восстановления создает новую базу данных.
Если вы восстановите базу данных Live на том же сервере, необходимо указать другое имя для новой базы данных.

Чтобы выполнить восстановление базы данных на момент времени, вместо этого используйте командлет **Start-AzureSqlDatabaseRestore** .

## ИЛЛЮСТРИРУЮТ

### Пример 1: восстановление базы данных, указанной как объект
```
PS C:\> $Database = Get-AzureSqlRecoverableDatabase -ServerName "Server01" -DatabaseName "Database17" 
PS C:\> $Operation = Start-AzureSqlDatabaseRecovery -SourceDatabase $Database -TargetDatabaseName "DatabaseRestored"
```

Первая команда получает объект базы данных с помощью командлета **Get-AzureSqlRecoverableDatabase** .
Команда сохраняет этот объект в переменной $Database.

Во второй команде база данных, сохраненная в $Database, будет восстановлена.

### Пример 2: восстановление базы данных с указанным именем
```
PS C:\> $Operation = Start-AzureSqlDatabaseRecovery -SourceServerName "Server01" -SourceDatabaseName "Database17" -TargetDatabaseName "DatabaseRestored"
```

Эта команда используется для восстановления базы данных с использованием имени базы данных.

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

### -SourceDatabase
Указывает объект базы данных, представляющий базу данных, которую этот командлет подявляет.

```yaml
Type: RecoverableDatabase
Parameter Sets: BySourceDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SourceDatabaseName
Указывает имя базы данных, которую этот командлет обнаружить.

```yaml
Type: String
Parameter Sets: BySourceDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceServerName
Указывает имя сервера, на котором находится база данных источника и что она запущена, или на которой была выполнена удаленная база данных.

```yaml
Type: String
Parameter Sets: BySourceDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetDatabaseName
Указывает имя восстановленной базы данных.
Если исходная база данных по-прежнему находится в режиме реального времени, для восстановления ее на том же сервере необходимо указать имя, отличное от имени базы данных-источника.

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

### -TargetServerName
Указывает имя сервера, на который нужно восстановить базу данных.
Базу данных можно восстановить на том же или другом сервере.

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

### Microsoft. WindowsAzure. Management. SQL. Models. RecoverableDatabase

## НАПРЯЖЕНИЕ

### Microsoft. WindowsAzure. Management. SQL. Models. RecoverDatabaseOperation

## Пуск
* Для запуска этого командлета необходимо использовать проверку подлинности на основе сертификата. На компьютере, на котором вы запускаете этот командлет, выполните следующие команды: 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[База данных SQL Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Создание запроса на восстановление базы данных](https://msdn.microsoft.com/en-us/library/dn800986.aspx)

[Георепликация в базе данных SQL Azure](https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/)

[Операции для баз данных SQL Azure](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlRecoverableDatabase](./Get-AzureSqlRecoverableDatabase.md)

[Start-AzureSqlDatabaseRestore](./Start-AzureSqlDatabaseRestore.md)


