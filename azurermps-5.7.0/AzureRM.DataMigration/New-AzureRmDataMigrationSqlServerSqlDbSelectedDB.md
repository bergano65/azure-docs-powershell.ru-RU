---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationsqlserversqldbselecteddb
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationSqlServerSqlDbSelectedDB.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationSqlServerSqlDbSelectedDB.md
ms.openlocfilehash: 1be43b5d08011a71ec093df2f93c63dd04c6004d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563564"
---
# New-AzureRmDataMigrationSqlServerSqlDbSelectedDB

## КРАТКИй обзор
Создает объект MigrateSqlServerSqlDbDatabaseInput, содержащий сведения об исходной и целевой базах данных для миграции.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
New-AzureRmDataMigrationSqlServerSqlDbSelectedDB [-Id <String>] [-Name <String>] [-TargetDatabaseName <String>]
 [-MakeSourceDbReadOnly] [-TableMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>]
```

## NОПИСАНИЕ
Командлет New-AzureRmDataMigrationSqlServerSqlDbSelectedDB создает объект MigrateSqlServerSqlDbDatabaseInput, содержащий сведения об исходных и целевых базах данных, а также о сопоставлениях таблиц для миграции. Этот командлет можно использовать в качестве параметра с помощью командлета New-AzureRmDataMigrationTask.

## ИЛЛЮСТРИРУЮТ

### Пример 1
```
PS C:\> New-AzureRmDataMigrationSqlServerSqlDbSelectedDB  -Name AdventuerWorks2016 -TargetDatabaseName AdventureWorks2016
 -MakeSourceDbReadOnly -TableMap $tableMap
```

В приведенном выше примере создается объект MigrateSqlServerSqlDbDatabaseInput для переноса базы данных **AdventureWorks2016** в базу данных SQL Azure с тем же именем.

## ПАРАМЕТРЫ

### -Confirm
Запрашивает подтверждение перед запуском командлета.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MakeSourceDbReadOnly
Настройка базы данных в режим только для чтения перед миграцией

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

### -Name (имя)
Имя базы данных.

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

### -TableMap
Сопоставление исходного кода с целевыми таблицами

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetDatabaseName
Имя целевой базы данных.

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

## ВХОДНЫЕ данные

### Ничего


## НАПРЯЖЕНИЕ

### Microsoft. Azure. Management. Migration. Models. MigrateSqlServerSqlDbDatabaseInput


## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ


