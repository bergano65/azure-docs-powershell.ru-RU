---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Update-AzSqlServerAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: e46ddc53ff7abd7faeee908cf3689683f3575069
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94315941"
---
# Update-AzSqlServerAdvancedThreatProtectionSetting

## КРАТКИй обзор
Задает дополнительные параметры защиты от угроз на сервере.

## Максимальное

```
Update-AzSqlServerAdvancedThreatProtectionSetting [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Update-AzSqlServerAdvancedThreatProtectionSetting** устанавливает дополнительные параметры защиты от угроз на сервере Azure SQL Server.
Для включения расширенной защиты от угроз на сервере параметры аудита должны быть включены на этом сервере.
Чтобы использовать этот командлет, укажите параметры *ResourceGroupName* и ServerName для идентификации сервера.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Настройка расширенных параметров защиты от угроз для базы данных
```powershell
PS C:\>Update-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

Эта команда задает расширенные параметры защиты от угроз для сервера с именем Server01.

### Пример 2

Задает дополнительные параметры защиты от угроз на сервере. (автоматически сформированные)

```powershell
<!-- Aladdin Generated Example --> 
Update-AzSqlServerAdvancedThreatProtectionSetting -EmailAdmins $false -ResourceGroupName 'ResourceGroup11' -RetentionInDays <UInt32> -ServerName 'Server01' -StorageAccountName 'mystorageAccount'
```

## ПАРАМЕТРЫ

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EmailAdmins
Указывает, имеют ли дополнительные параметры защиты от угроз администраторам контакты с помощью электронной почты.

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
Указывает массив типов обнаружения, исключаемых из параметров.
Для этого параметра допустимы следующие значения:
- Sql_Injection
- Sql_Injection_Vulnerability
- Access_Anomaly
- Ничего

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NotificationRecipientsEmails
Указывает список адресов электронной почты, разделенных точкой с запятой, по которым параметры отправляют оповещения.

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
Указывает имя группы ресурсов, к которой принадлежит сервер.

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
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountName
Указывает имя учетной записи хранения, которую нужно использовать. Подстановочные знаки не разрешены. Этот параметр не является обязательным. Если этот параметр не указан, командлет будет использовать учетную запись хранения, которая была ранее определена как часть параметров расширенной защиты от угроз для базы данных. Если при первом определении параметров обнаружения угроз базы данных этот параметр не указан, командлет завершится сбоем.

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## ВХОДНЫЕ данные

### System. String

### System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]

### Microsoft. Azure. Commands. SQL. ThreatDetection. Model. DetectionType []

### System. Nullable "1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. SQL. ThreatDetection. Model. ServerThreatDetectionsettingsModel

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzSqlServerThreatDetectionsettings](./Get-AzSqlServerThreatDetectionsettings.md)

[Remove-AzSqlServerThreatDetectionsettings](03e90cd1-6ae2-4134-bc5e-28cc080614c9)

[Документация по базам данных SQL](https://docs.microsoft.com/azure/sql-database/)
