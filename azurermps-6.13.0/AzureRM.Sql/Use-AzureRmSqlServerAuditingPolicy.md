---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 381F5B34-983C-4733-B384-35D6579B79A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/use-azurermsqlserverauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Use-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Use-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: a0dc151c86caf41131649f7e4e37ee60c6f19b01
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565786"
---
# Use-AzureRmSqlServerAuditingPolicy

## КРАТКИй обзор
Указывает, что база данных использует политику аудита на своем хост-сервере.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Use-AzureRmSqlServerAuditingPolicy [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **use-AzureRmSqlServerAuditingPolicy** указывает, что база данных использует политику аудита на своем хост-сервере.
Укажите параметры *ResourceGroupName* , *ServerName* и *DatabaseName* , чтобы идентифицировать базу данных.
Если для сервера базы данных не определена политика аудита, этот командлет завершается сбоем.
Если узел использует аудит уровня сервера, обнаружение угроз удаляется.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Настройка базы данных для использования политики аудита сервера
```
PS C:\>Use-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server02" -DatabaseName "Database01"
```

Эта команда указывает на то, что база данных с именем Database01 on Server02 использует политику аудита сервера.

## ПАРАМЕТРЫ

### -DatabaseName
Указывает имя базы данных, которая будет использовать политику аудита.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
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
Указывает имя группы ресурсов, которой назначен сервер.

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
Указывает имя сервера, на котором размещается база данных, использующая политику аудита.

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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. SQL. Audit. Model. AuditingPolicyModel

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmSqlDatabaseAuditingPolicy](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[Get-AzureRmSqlServerAuditingPolicy](./Get-AzureRmSqlServerAuditingPolicy.md)

[Set-AzureRmSqlDatabaseAuditingPolicy](./Set-AzureRmSqlDatabaseAuditingPolicy.md)

[Set-AzureRmSqlServerAuditingPolicy](./Set-AzureRmSqlServerAuditingPolicy.md)

[Документация по базам данных SQL](https://docs.microsoft.com/azure/sql-database/)


