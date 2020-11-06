---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 457FD595-D5E1-45C4-9DB8-C3C6C30A0E94
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: 746a9a9908865047d5b904b5b47b71ca9c30fbd3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562012"
---
# Set-AzureRmSqlDatabaseThreatDetectionPolicy

## КРАТКИй обзор
Задает политику обнаружения угроз для базы данных.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Set-AzureRmSqlDatabaseThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <DetectionType[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzureRmSqlDatabaseThreatDetectionPolicy** устанавливает политику обнаружения угроз в базе данных Azure SQL.
Чтобы включить обнаружение угроз для базы данных, необходимо включить в этой базе данных политику аудита.

Чтобы использовать этот командлет, укажите параметры *ResourceGroupName* , *ServerName* и *DatabaseName* , чтобы идентифицировать базу данных.

Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Настройка политики обнаружения угроз для базы данных
```
PS C:\>Set-AzureRmSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

Эта команда задает политику обнаружения угроз для базы данных с именем Database01 на сервере с именем Server01.

## ПАРАМЕТРЫ

### -DatabaseName
Указывает имя базы данных, в которой задана политика.

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

### -EmailAdmins
Определяет, является ли политика обнаружения угроз контактными администраторами с помощью электронной почты.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ExcludedDetectionType
Указывает массив типов обнаружения, исключаемых из политики.
Для этого параметра допустимы следующие значения:

- Sql_Injection 
- Sql_Injection_Vulnerability 
- Access_Anomaly 
- Ничего

```yaml
Type: Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]
Parameter Sets: (All)
Aliases: 
Accepted values: Sql_Injection, Sql_Injection_Vulnerability, Access_Anomaly, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NotificationRecipientsEmails
Указывает список адресов электронной почты, разделенных точкой с запятой, по которым политика отправляет оповещения.

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

### -RetentionInDays
Количество дней хранения для журналов аудита

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
Указывает имя сервера.

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

### -StorageAccountName
Указывает имя учетной записи хранения, которую нужно использовать. Подстановочные знаки не разрешены. Этот параметр не является обязательным. Если этот параметр не указан, командлет будет использовать учетную запись хранения, которая была ранее определена как часть политики обнаружения угроз для базы данных. Если определена политика обнаружения угроз базы данных в первый раз и этот параметр не указан, командлет завершится сбоем.

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

###  
Вы не можете передавать входные данные в этот командлет.

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. SQL. ThreatDetection. Model. DatabaseThreatDetectionPolicyModel
Этот командлет возвращает объект **model. DatabaseThreatDetectionPolicyModel** .

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmSqlDatabaseThreatDetectionPolicy](./Get-AzureRmSqlServerThreatDetectionPolicy.md)

[Remove-AzureRmSqlDatabaseThreatDetectionPolicy](./Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md)

[Документация по базам данных SQL](https://docs.microsoft.com/azure/sql-database/)


