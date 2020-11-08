---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F4FE79DB-B481-49BD-A33B-7C642A136890
online version: ''
schema: 2.0.0
ms.openlocfilehash: 588fcf73c258364e41117eed05c62de7eaa231e9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075973"
---
# New-AzureSqlDatabase

## КРАТКИй обзор
Создает базу данных SQL Azure.

## Максимальное

### ByConnectionContext
```
New-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String>
 [-Collation <String>] [-Edition <DatabaseEdition>] [-ServiceObjective <ServiceObjective>] [-MaxSizeGB <Int32>]
 [-MaxSizeBytes <Int64>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByServerName
```
New-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-Collation <String>]
 [-Edition <DatabaseEdition>] [-ServiceObjective <ServiceObjective>] [-MaxSizeGB <Int32>]
 [-MaxSizeBytes <Int64>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzureSqlDatabase** создает базу данных Azure SQL.
Вы можете указать сервер, используя контекст подключения к серверу базы данных SQL Azure, созданный с помощью командлета **New-AzureSqlDatabaseServerContext** .
Или, если указать имя сервера, командлет использует текущие сведения о подписке Azure для проверки подлинности запроса на доступ к серверу.

Когда вы создаете новую базу данных, указав сервер базы данных Azure SQL, командлет **New-AzureSqlDatabase** создает временный контекст подключения, используя указанное имя сервера и текущую информацию о подписке Azure для выполнения этой операции.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание базы данных
```
PS C:\> $Database01 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01" -Edition "Business" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

Эта команда создает базу данных Azure SQL с именем Database1 для контекста подключения к серверу базы данных SQL Azure $Context.

### Пример 2: создание базы данных в текущей подписке
```
PS C:\> $Database01 = New-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01" -Edition "Business" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

В этом примере создается база данных с именем Database1 на указанном сервере базы данных SQL Azure с именем lpqd0zbr8y.
Командлет использует текущие сведения о подписке Azure для проверки подлинности запроса на доступ к серверу.

## ПАРАМЕТРЫ

### -Параметры сортировки
Задает параметры сортировки для новой базы данных.

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

### -ConnectionContext
Указывает контекст подключения сервера, на котором этот командлет создает базу данных.

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
Указывает имя новой базы данных.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Edition
Указывает выпуск для новой базы данных SQL Azure.
Допустимые значения: 

- Ничего
- Сайта
- Деловы
- Базового
- Стандартная
-  Версию

По умолчанию используется значение Web.

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Разрешает выполнение действия без запроса подтверждения у пользователя.

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

### -MaxSizeBytes
Указывает максимальный размер базы данных в байтах.
Вы можете указать либо этот параметр, либо параметр *MaxSizeGB* .
Посмотрите описание параметра *MaxSizeGB* для приемлемых значений в соответствии с выпуском.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxSizeGB
Задает максимальный размер базы данных в гигабайтах.
Вы можете указать либо этот параметр, либо параметр *MaxSizeBytes* .
Приемлемые значения зависят от выпуска.

Основные значения выпусков: 1 или 2

Стандартные значения выпуска: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200 или 250

Расширенные значения выпуска: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300 и 400

Значения веб-выпуска: 1 или 5

Значения для выпуска Business Edition: 10, 20, 30, 40, 50, 100 или 150

```yaml
Type: Int32
Parameter Sets: (All)
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
Указывает имя сервера базы данных SQL Azure, на котором будет содержаться новая база данных.

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

### -ServiceObjective
Указывает объект, который представляет новую цель обслуживания (уровень производительности) для этой базы данных.
Это значение представляет уровень ресурсов, назначенных этой базе данных.
Допустимые значения: 

Basic: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c Standard (S0): f1173c43-91bd-4AAA-973c-54e79e15235b Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928 Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7 * Standard (S3): 789681b8-CA10-4eb0-bdf2-e0b050601b40 Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P2

* Стандартный (S3) является частью последнего обновления базы данных SQL версии 12 (Предварительная версия).
Дополнительные сведения можно найти в разделе новые возможности предварительного просмотра базы данных SQL Azure версии 12 https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/ .

```yaml
Type: ServiceObjective
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

## НАПРЯЖЕНИЕ

### Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. Database

## Пуск
* Чтобы удалить базу данных, созданную с помощью **New-AzureSqlDatabase** , используйте командлет Remove-AzureSqlDatabase.

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[База данных SQL Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Создание базы данных](https://msdn.microsoft.com/en-us/library/azure/dn505701.aspx)

[Операции для баз данных SQL Azure](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)

[New-AzureSqlDatabaseServerContext](./New-AzureSqlDatabaseServerContext.md)

[Remove-AzureSqlDatabase](./Remove-AzureSqlDatabase.md)

[Set-AzureSqlDatabase](./Set-AzureSqlDatabase.md)


