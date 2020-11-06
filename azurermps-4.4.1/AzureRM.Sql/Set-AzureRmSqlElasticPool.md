---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
ms.openlocfilehash: 512c77862c44af68b26eb300eb9a692c115b0750
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562000"
---
# Set-AzureRmSqlElasticPool

## КРАТКИй обзор
Изменяет свойства пула эластичных баз данных в базе данных Azure SQL.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Set-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Edition <DatabaseEdition>] [-Dtu <Int32>]
 [-StorageMB <Int32>] [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzureRmSqlElasticPool** изменяет свойства пула эластичных баз данных в базе данных Azure SQL. Этот командлет может изменить минимальное количество единиц пропускной способности базы данных (DTU) на базу данных в дополнение к максимальному количеству DTU на базу данных, число DTU для пула и ограничение хранилища для пула.

Для нескольких параметров ( *-DTU,-DatabaseDtuMin и-DatabaseDtuMax* ) необходимо, чтобы значение было задано в списке допустимых значений для этого параметра. Например, параметр-DatabaseDtuMax для стандартного пула 100 eDTU может иметь только значение 10, 20, 50 или 100.  Сведения о допустимых значениях можно найти в таблице для пула определенного размера в [эластичных пулах](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).

## ИЛЛЮСТРИРУЮТ

### Пример 1: изменение свойств эластичного пула
```
PS C:\>Set-AzureRmSqlDatabaseElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Dtu 1000 -DatabaseDtuMax 100 -DatabaseDtuMin 20
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/Server01/elasticPools/ElasticPool01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
ElasticPoolName   : ElasticPool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 200
DatabaseDtuMax    : 100
DatabaseDtuMin    : 20
StorageMB         : 204800
Tags              :
```

Эта команда изменяет свойства пула эластичных БД с именем elasticpool01. Команда задает количество DTU для эластичного пула в 1000 и устанавливает минимальные и максимальные значения DTU.

### Пример 2: изменение максимального хранилища эластичного пула
```
PS C:\>Set-AzureRmSqlDatabaseElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -StorageMB 2097152
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/Server01/elasticPools/ElasticPool01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
ElasticPoolName   : ElasticPool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Premium
Dtu               : 200
DatabaseDtuMax    : 100
DatabaseDtuMin    : 20
StorageMB         : 2097152
Tags              :
```

Эта команда изменяет свойства пула эластичных БД с именем elasticpool01. Команда задает максимальный объем хранилища для пула эластичных БД равным 2 ТБ.

## ПАРАМЕТРЫ

### -DatabaseDtuMax
Указывает максимальное количество DTU, которое может использовать любая единственная база данных в пуле. 

Сведения о допустимых значениях можно найти в таблице для пула определенного размера в [эластичных пулах](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool). 

Значения по умолчанию для разных выпусков описаны ниже.

- Базового.  5 DTU
- Стандартная. 100 DTU
- Версию. 125 DTU


```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseDtuMin
Указывает минимальное количество DTU, которое будет гарантировано для всех баз данных в пуле для эластичного пула.

Сведения о допустимых значениях можно найти в таблице для пула определенного размера в [эластичных пулах](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).

Значением по умолчанию является нуль (0).

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DTU
Указывает общее количество общих DTU для пула эластичных БД. 

Сведения о допустимых значениях можно найти в таблице для пула определенного размера в [эластичных пулах](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool). 

Значения по умолчанию для разных выпусков описаны ниже.

- Базового. 100 DTU
- Стандартная. 100 DTU
- Версию. 125 DTU

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Edition
Указывает выпуск базы данных SQL Azure для пула эластичных БД. Изменить выпуск нельзя. Для этого параметра допустимы следующие значения:

- Ничего
- Базового
- Стандартная
- Версию
- PremiumRS
- Хранилище Datawarehouse
- Бесплатно

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases: 
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ElasticPoolName
Указывает имя эластичного пула.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов, которой назначен эластичный пул.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ИмяСервера
Указывает имя сервера, на котором размещается эластичный пул.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageMB
Указывает предельный размер (в мегабайтах) для пула эластичных БД. Дополнительные сведения можно найти в командлетах New-AzureRmSqlElasticPool.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Теги
Указывает словарь пар "ключ-значение", который этот командлет связывает с пулом эластичных БД в форме хэш-таблицы. Например:

`@{key0="value0";"key 1"=$null;key2="value2"}`

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Запрашивает подтверждение перед запуском командлета.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmSqlElasticPool](./Get-AzureRmSqlElasticPool.md)

[Get-AzureRmSqlElasticPoolActivity](./Get-AzureRmSqlElasticPoolActivity.md)

[Get-AzureRmSqlElasticPoolDatabase](./Get-AzureRmSqlElasticPoolDatabase.md)

[New-AzureRmSqlElasticPool](./New-AzureRmSqlElasticPool.md)

[Документация по базам данных SQL](https://docs.microsoft.com/azure/sql-database/)
