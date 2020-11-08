---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 83E8DAD8-151A-408D-819F-274CB813ABDA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6f9a5753fdf4f87afc6baacbe9fc4c33c9be08ef
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076559"
---
# Get-AzureSqlRecoverableDatabase

## КРАТКИй обзор
Получение баз данных, которые могут быть восстановлены с указанного сервера.

## Максимальное

### AllDatabasesOnGivenServer (по умолчанию)
```
Get-AzureSqlRecoverableDatabase -ServerName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### GivenDatabaseOnGivenServer
```
Get-AzureSqlRecoverableDatabase -ServerName <String> -DatabaseName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### GivenDatabaseObject
```
Get-AzureSqlRecoverableDatabase -Database <RecoverableDatabase> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureSqlRecoverableDatabase** Получает доступную для восстановления базу данных с указанного сервера.
Этот командлет получает указанную базу данных с возможностью восстановления или все базы данных с возможностью восстановления на сервере.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение всех баз данных, которые могут быть восстановлены
```
PS C:\> Get-AzureSqlRecoverableDatabase -ServerName "Server01"
```

Эта команда получает все базы данных с возможностью восстановления, которые могут быть восстановлены на сервере с именем Server01.

### Пример 2: получение определенной базы данных с возможностью восстановления
```
PS C:\> Get-AzureSqlRecoverableDatabase -ServerName "Server01" -DatabaseName "Database17"
```

Эта команда получает базу данных с именем Database17 на сервере с именем Server01.

## ПАРАМЕТРЫ

### -База данных
Указывает объект, который представляет базу данных с возможностью восстановления, которую получает этот командлет.

```yaml
Type: RecoverableDatabase
Parameter Sets: GivenDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
Указывает имя базы данных с возможностью восстановления, которую получает этот командлет.

```yaml
Type: String
Parameter Sets: GivenDatabaseOnGivenServer
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
Указывает имя сервера, с которого этот командлет получает восстановленные базы данных.

```yaml
Type: String
Parameter Sets: AllDatabasesOnGivenServer, GivenDatabaseOnGivenServer
Aliases: 

Required: True
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

### IEnumerable\<Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase\>

## Пуск
* Для запуска этого командлета необходимо использовать проверку подлинности на основе сертификата. На компьютере, на котором запускается этот командлет, выполните следующие команды: 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[База данных SQL Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Получить базу данных с возможностью восстановления](https://msdn.microsoft.com/en-us/library/azure/dn800985.aspx)

[Операции для баз данных SQL Azure](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Start-AzureSqlDatabaseRecovery](./Start-AzureSqlDatabaseRecovery.md)


