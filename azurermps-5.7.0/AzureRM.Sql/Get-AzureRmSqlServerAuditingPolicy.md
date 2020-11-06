---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 40674DC7-E35F-4C9F-8CE0-D1C6F524C9FB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: a12c9846b9e52d3c5e19c74b5a0f755acb27daf6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561436"
---
# Get-AzureRmSqlServerAuditingPolicy

## КРАТКИй обзор
Возвращает политику аудита сервера SQL Server.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Get-AzureRmSqlServerAuditingPolicy -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmSqlServerAuditingPolicy** получает политику аудита для Azure SQL Server.
Укажите параметры *ResourceGroupName* , *ServerName* и *DatabaseName* , чтобы идентифицировать базу данных.
Этот командлет возвращает политику, которая используется в базах данных Azure SQL, которые определены в указанном сервере Azure SQL Server и используют его политику аудита.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение политики аудита для Azure SQL Server с определенными для него разаудитом таблиц
```
PS C:\>Get-AzureRmSqlServerAuditingPolicy -ResourceGroupName "resourcegroup01" -ServerName "server01"
EventType              : {PlainSQL_Success, PlainSQL_Failure, ParameterizedSQL_Success, ParameterizedSQL_Failure...} 
TableIdentifier        : MyAuditTableName
FullAuditLogsTableName : SQLDBAuditLogsMyAuditTableName
ResourceGroupName      : resourcegroup01
ServerName             : server01
AuditType              : Table
AuditState             : Enabled
StorageAccountName     : mystorage
StorageKeyType         : Primary
RetentionInDays        : 0
```

### Пример 2: получение политики аудита для Azure SQL Server с определенными аудитом больших двоичных объектов
```
PS C:\>Get-AzureRmSqlServerAuditingPolicy -ResourceGroupName "resourcegroup01" -ServerName "server01"
AuditActionGroup       : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                          BATCH_COMPLETED_GROUP, ...} 
ResourceGroupName      : resourcegroup01
ServerName             : server01
AuditType              : Blob
AuditState             : Enabled
StorageAccountName     : mystorage
StorageKeyType         : Primary
RetentionInDays        : 0
```

## ПАРАМЕТРЫ

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

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

### -ResourceGroupName
Указывает имя группы ресурсов, которой назначен Azure SQL Server.

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

### -ИмяСервера
Указывает имя сервера Azure SQL Server, для которого этот командлет получает политику аудита.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
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

### Ничего
Этот командлет не поддерживает никаких входных данных.

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. SQL. Security. Model. ServerAuditingPolicyModel

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Set-AzureRmSqlServerAuditingPolicy](./Set-AzureRmSqlServerAuditingPolicy.md)

[Use-AzureRmSqlServerAuditingPolicy](./Use-AzureRmSqlServerAuditingPolicy.md)

[Документация по базам данных SQL](https://docs.microsoft.com/azure/sql-database/)


