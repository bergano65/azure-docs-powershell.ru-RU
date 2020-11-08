---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A2C22A8A-EF50-4BE3-82DF-5ED6F69C00CA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 457775a74fb7921a3c8b6b5e635bd7df7e704faa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075568"
---
# Get-AzureSqlDatabaseServiceObjective

## КРАТКИй обзор
Получение целей обслуживания для сервера базы данных SQL Azure.

## Максимальное

### ByConnectionContext (по умолчанию)
```
Get-AzureSqlDatabaseServiceObjective -Context <IServerDataServiceContext>
 [-ServiceObjective <ServiceObjective>] [-ServiceObjectiveName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ByServerName
```
Get-AzureSqlDatabaseServiceObjective -ServerName <String> [-ServiceObjective <ServiceObjective>]
 [-ServiceObjectiveName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureSqlDatabaseServiceObjective** получает цели службы для сервера базы данных SQL Azure.
Цели обслуживания обозначаются как уровни производительности.
Если цель службы не указана, этот командлет возвращает все допустимые цели обслуживания для указанного сервера.

Этот командлет применим к базовым, стандартным и расширенным уровням обслуживания.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение всех целей обслуживания с помощью контекста подключения
```
PS C:\> Get-AzureSqlDatabaseServiceObjective -Context $Context
```

Эта команда получает все цели обслуживания для сервера, который $Context указывает контекстом подключения.

### Пример 2: получение всех целей обслуживания с помощью имени сервера
```
PS C:\> Get-AzureSqlDatabaseServiceObjective -ServerName "Server01"
```

Эта команда получает все цели обслуживания для сервера с именем Server01.

## ПАРАМЕТРЫ

### -Context
Указывает контекст подключения сервера.

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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

### -ServiceObjective
Указывает объект, который представляет цель службы, которую получает этот командлет.
Допустимые значения: 

- Basic: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c
- Стандартный (S0): f1173c43-91bd-4AAA-973c-54e79e15235b
- Стандартный (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928
- Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7
- * Стандартный (S3): 789681b8-CA10-4eb0-bdf2-e0b050601b40
- Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d
- Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d
- Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0
- Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446

* Стандартный (S3) является частью последнего обновления базы данных SQL версии 12 (Предварительная версия).
Дополнительные сведения можно найти в разделе [новые возможности базы данных SQL Azure версии 12](https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/) ( `https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/` ) в библиотеке Azure.

```yaml
Type: ServiceObjective
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ServiceObjectiveName
Указывает имя цели обслуживания, которую требуется получить.
Допустимые значения: Basic, S0, S1, S2, S3, P1, P2 и P3.

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

### Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. ServiceObjective

## НАПРЯЖЕНИЕ

### IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServiceObjective\>

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[База данных SQL Azure](https://msdn.microsoft.com/library/ee336279.aspx)

[Получить цель уровня обслуживания](https://msdn.microsoft.com/en-us/library/azure/dn505709.aspx)

[Операции для баз данных SQL Azure](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[New-AzureSqlDatabaseServerContext](./New-AzureSqlDatabaseServerContext.md)


