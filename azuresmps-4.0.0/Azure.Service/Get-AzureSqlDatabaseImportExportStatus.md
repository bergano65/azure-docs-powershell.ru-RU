---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 4661C479-6E3B-425D-B9D2-B36D7A83130C
online version: ''
schema: 2.0.0
ms.openlocfilehash: c3c55ebd22337a8078f3ae495b3901317f4201e0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076294"
---
# Get-AzureSqlDatabaseImportExportStatus

## КРАТКИй обзор
Возвращает состояние запроса на импорт или экспорт.

## Максимальное

### ByConnectionInfo
```
Get-AzureSqlDatabaseImportExportStatus -Username <String> -Password <String> -ServerName <String>
 -RequestId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByRequestObject
```
Get-AzureSqlDatabaseImportExportStatus -Request <ImportExportRequest> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureSqlDatabaseImportExportStatus** получает состояние запроса на импорт или экспорт.
Командлет Start-AzureSqlDatabaseImport или Start-AzureSqlDatabaseExport инициирует запросы.
Вы можете задать объект Request с помощью параметра *request* или определить запрос с помощью параметра *RequestId* и *имени пользователя* , *пароля* и *сервера* доменных параметров.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение состояния запроса на экспорт
```
PS C:\> $ExportRequest = Start-AzureSqlDatabaseExport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
PS C:\> Get-AzureSqlDatabaseImportExportStatus -Request $ExportRequest
```

Первая команда создает запрос на экспорт, а затем сохраняет его в переменной $ExportRequest.

Вторая команда возвращает состояние запроса на экспорт, который хранится в $ExportRequest.

## ПАРАМЕТРЫ

### -Password (пароль)
Указывает пароль, необходимый для подключения к серверу базы данных SQL Azure.
Вы должны указать этот параметр, если вы указали параметр *RequestId* .

```yaml
Type: String
Parameter Sets: ByConnectionInfo
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

### -Request
Указывает объект **ImportExportRequest** .
Чтобы получить объект запроса на импорт или экспорт, используйте командлет Start-AzureSqlDatabaseImport или Start-AzureSqlDatabaseExport.

```yaml
Type: ImportExportRequest
Parameter Sets: ByRequestObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequestId
Указывает GUID операции импорта или экспорта, для которой этот командлет получает состояние.
Если указан этот параметр, необходимо указать *имя пользователя* , *пароль* и *имя сервера* .

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ИмяСервера
Указывает имя сервера базы данных SQL Azure.
Вы должны указать этот параметр, если вы указали параметр *RequestId* .

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Username
Указывает имя пользователя, необходимое для подключения к серверу базы данных SQL Azure.
Вы должны указать этот параметр, если вы указали параметр *RequestId* .

```yaml
Type: String
Parameter Sets: ByConnectionInfo
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

## НАПРЯЖЕНИЕ

### Microsoft. WindowsAzure. Commands. SqlDatabase. Services. ImportExport. StatusInfo

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[База данных SQL Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Получение состояния импорта базы данных экспорта](https://msdn.microsoft.com/en-us/library/azure/dn781289.aspx)

[Операции для баз данных SQL Azure](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Start-AzureSqlDatabaseExport](./Start-AzureSqlDatabaseExport.md)

[Start-AzureSqlDatabaseImport](./Start-AzureSqlDatabaseImport.md)


