---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: 5eedeea96f7c1c2491e7388734b51977cb0dd1c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561375"
---
# Set-AzureRmSqlDatabaseAuditing

## КРАТКИй обзор
Изменение параметров аудита для базы данных SQL Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Set-AzureRmSqlDatabaseAuditing -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>]
 [-AuditAction <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzureRmSqlDatabaseAuditing** изменяет параметры аудита для базы данных SQL Azure.
Чтобы использовать командлет, используйте параметры *ResourceGroupName* , *ServerName* и *DatabaseName* для идентификации базы данных.
Укажите параметр *StorageAccountName* , чтобы указать учетную запись хранения для журналов аудита и параметр *StorageKeyType* , чтобы определить ключи хранилища.
Используйте параметр *State* для включения или отключения политики.

Вы также можете определить хранение журналов аудита, задав значение параметра *RetentionInDays* , чтобы определить период для журналов аудита.

После успешного выполнения командлета аудит базы данных включен.
Если командлет завершился успешно и вы используете параметр *PassThru* , он возвращает объект, описывающий текущую политику аудита BLOB-объектов, в дополнение к идентификаторам базы данных.
Идентификаторы баз данных включают, но не ограничиваются, **ResourceGroupName** , **ServerName** и **DatabaseName**.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Включение политики аудита для базы данных SQL Azure
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

### Пример 2: отключение политики аудита больших двоичных объектов для базы данных SQL Azure
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

## ПАРАМЕТРЫ

### -AuditAction
Набор действий аудита.  
Ниже перечислены поддерживаемые действия для аудита.  
ВЫБРАННЫЕ  
Обновление  
ВСТАВКОЙ  
Удаление  
ВЫПОЛНЯЕТ  
ОШИБК  
Указывает  

Для определения действия, подлежащие аудиту, можно использовать общую форму:

транзактное ON [Object] [участник]

Обратите внимание, что в приведенном выше формате объект [Object] может ссылаться на объект, например на таблицу, представление или сохраненную процедуру, а также на всю базу данных или схему. В последних случаях используются базы данных форм: [dbname] и SCHEMA:: [SchemaName].

Например:  
ВЫБОР на dbo. myTable по открытым  
Выберите базу данных:: myDatabase по общедоступным  
Выбор схемы:: mySchema по общедоступным  

Дополнительные сведения можно найти в разделе https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AuditActionGroup
Рекомендуемый набор групп действий: в этом случае будут проверены все запросы и хранимые процедуры, выполненные для базы данных, а также успешные и неудачные входные данные.  
  
"BATCH_COMPLETED_GROUP",  
"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",  
"FAILED_DATABASE_AUTHENTICATION_GROUP"  

Это сочетание также является набором, настроенным по умолчанию. Эти группы охватывают все инструкции SQL и хранимые процедуры, выполненные для базы данных, и их нельзя использовать в сочетании с другими группами, так как это приводит к дублированию журналов аудита.
Дополнительные сведения можно найти в разделе https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .

```yaml
Type: AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, AUDIT_CHANGE_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DatabaseName
Имя базы данных SQL.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -PassThru
{{Fill описание пропускания}}

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

### -ResourceGroupName
Имя группы ресурсов.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RetentionInDays
Количество дней хранения для журналов аудита.

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ИмяСервера
Имя сервера базы данных SQL.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -State
Состояние политики.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountName
Имя учетной записи хранения. Подстановочные знаки не разрешены.  
Этот параметр не является обязательным.  
Если этот параметр не указан, командлет использует учетную запись хранения, которая была ранее определена как часть политики аудита.  
Если политика аудита не задана в первый раз и вы не указали этот параметр, командлет завершится сбоем.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageKeyType
Указывает, какие клавиши доступа к хранилищу следует использовать.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске командлета. Командлет не выполняется.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего
Этот командлет не поддерживает никаких входных данных.

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. SQL. Security. Model. DatabaseBlobAuditingSettingsModel

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
