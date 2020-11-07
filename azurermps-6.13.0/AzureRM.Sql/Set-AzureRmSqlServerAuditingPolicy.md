---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4FCC7D8B-A46E-4E5B-8BE2-F62B3D3E715D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: dd3c54b8e2769e1b7643d154b259b4f47fd51f2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732441"
---
# Set-AzureRmSqlServerAuditingPolicy

## КРАТКИй обзор
Изменение политики аудита на сервере базы данных SQL.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Set-AzureRmSqlServerAuditingPolicy [-AuditType <AuditType>] [-AuditActionGroup <AuditActionGroups[]>]
 [-PassThru] [-EventType <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-TableIdentifier <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzureRmSqlServerAuditingPolicy** изменяет политику аудита на сервере базы данных SQL Azure.
Укажите параметры *ResourceGroupName* и *ServerName* для идентификации сервера, параметр *StorageAccountName* , чтобы указать учетную запись хранения для журналов аудита, а также параметр *StorageKeyType* , чтобы определить ключи хранения для использования.
Вы также можете задать хранение для таблицы Audit Logs, задав значения параметров *RetentionInDays* и *TableIdentifier* , чтобы определить период и начальное значение для имен таблиц журнала аудита.
Укажите параметр *EventType* , чтобы определить типы событий для аудита.
После запуска этого командлета выполняется аудит баз данных, использующих политику этого сервера.
Если командлет завершился успешно и вы указываете параметр *PassThru* , командлет возвращает объект, который описывает текущую политику аудита и идентификаторы сервера.
Идентификаторы сервера включают **ResourceGroupName** и **ServerName**.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Настройка политики аудита для Azure SQL Server использование аудита таблиц
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AuditType Table -StorageAccountName "Storage22"
```

Эта команда задает для политики аудита сервера с именем Server01 использование учетной записи хранения с именем Storage22.

### Пример 2: Настройка ключа учетной записи хранения для существующей политики аудита на сервере Azure SQL Server
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountKey Secondary
```

Эта команда задает для политики аудита сервера с именем Server01 использование вторичного ключа.
Команда не изменяет имя учетной записи хранения.

### Пример 3: Настройка политики аудита сервера Azure SQL Server для использования определенного типа события
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventType Login_Failure
```

### Пример 4: Настройка политики аудита для базы данных для использования аудита больших двоичных объектов
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AuditType Blob -StorageAccountName "Storage31" -AuditActionGroup "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" -RetentionInDays 8
```

Эта команда задает политику аудита сервера с именем Server01, чтобы использовать тип события Login_Failure.
Эта команда не изменяет другие настройки.

## ПАРАМЕТРЫ

### -AuditActionGroup
Укажите одну или несколько групп действий аудита. Этот параметр применим только к аудиту больших двоичных объектов.

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, AUDIT_CHANGE_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AuditType
Укажите тип аудита. Журналы аудита можно записывать в хранилище таблиц или хранилище BLOB-объектов. Аудит больших двоичных объектов обеспечивает более высокий уровень производительности и поддерживает аудит на уровне объектов.

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditType
Parameter Sets: (All)
Aliases:
Accepted values: NotSet, Table, Blob

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

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

### -EventType
Указывает типы событий для аудита.
Этот параметр применим только к аудиту таблиц.
Вы можете указать несколько типов событий.
Вы можете задать аудит для всех типов событий или нет, чтобы указать, что никакие события не будут проверяться.
Если вы задаете значение "все" или "нет" одновременно, команда не выполняется.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: PlainSQL_Success, PlainSQL_Failure, ParameterizedSQL_Success, ParameterizedSQL_Failure, StoredProcedure_Success, StoredProcedure_Failure, Login_Success, Login_Failure, TransactionManagement_Success, TransactionManagement_Failure, All, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Возвращает объект, который представляет собой элемент, с которым вы работаете.
По умолчанию этот командлет не создает никаких выходных данных.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов, содержащей базу данных.

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

### -RetentionInDays
Указывает количество дней хранения для таблицы журналов аудита.
Нулевое значение (0) означает, что таблица не сохраняется.
Это значение по умолчанию.
Если вы задаете значение больше нуля, необходимо также указать значение параметра *TableIdentifer* .

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ИмяСервера
Указывает имя сервера, который содержит базу данных.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountName
Указывает имя учетной записи хранения для аудита базы данных.
Подстановочные знаки не разрешены.
Если этот параметр не указан, командлет использует учетную запись хранения, которая была ранее определена как часть политики аудита базы данных.
Если политика аудита базы данных в первый раз определена, а этот параметр не указан, команда не выполняется.

```yaml
Type: System.String
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
Для этого параметра допустимы следующие значения:
- Главная
- Вспомогательное значение по умолчанию — PRIMARY.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TableIdentifier
Указывает имя таблицы журналов аудита.
Укажите это значение, если для параметра *RetentionInDays* задано значение больше нуля.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Microsoft. Azure. Commands. SQL. Audit. Model. AuditType

### Microsoft. Azure. Commands. SQL. Audit. Model. AuditActionGroups []

### System. String []

### System. String

### System. Nullable "1 [[System. UInt32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. SQL. Audit. Model. AuditingPolicyModel

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmSqlServerAuditingPolicy](./Get-AzureRmSqlServerAuditingPolicy.md)

[Use-AzureRmSqlServerAuditingPolicy](./Use-AzureRmSqlServerAuditingPolicy.md)

[Документация по базам данных SQL](https://docs.microsoft.com/azure/sql-database/)


