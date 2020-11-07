---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 48CF206C-AF63-4013-834E-8EC3646D180B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: dd29dd7e58a233d62e3af5260971d56300a43230
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732339"
---
# Set-AzureRmSqlDatabaseDataMaskingRule

## КРАТКИй обзор
Задает свойства правила маскирования данных для базы данных.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Set-AzureRmSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzureRmSqlDatabaseDataMaskingRule** задает правило маскирования данных для базы данных SQL Azure.
Чтобы использовать командлет, укажите параметры *ResourceGroupName* , *ServerName* , *DatabaseName* и *RuleId* , чтобы определить правило.
Вы можете предоставить любой из параметров *SchemaName* , *TableName* и *ColumnName* , чтобы перенацелить правило.
Укажите параметр *MaskingFunction* , чтобы изменить способ маскирования данных.

Если вы задаете значение числа или текста для *MaskingFunction* , вы можете указать параметры *NumberFrom* и *NumberTo* для масок номеров, а также параметры *PrefixSize* , *ReplacementString* и *SuffixSize* для маскирования текста.
Если команда выполнена успешно, а параметр *PassThru* указан, командлет возвращает объект, описывающий свойства правила масок данных и идентификаторы правил.
Идентификаторы правила включают, но не ограничиваются, **ResourceGroupName** , **ServerName** , **DatabaseName** и **RuleId**.

Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.

## ИЛЛЮСТРИРУЮТ

### Пример 1: изменение диапазона правила маскировки данных в базе данных
```
PS C:\>Set-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

Эта команда изменяет правило маскировки данных с ИДЕНТИФИКАТОРом Rule17.
Это правило работает в базе данных с именем Database01 на сервере Server01.
Эта команда изменяет границы интервала, в течение которого случайное число генерируется как маскированное значение.
Новый диапазон находится в диапазоне от 23 до 42.

## ПАРАМЕТРЫ

### -ColumnName
Задает имя столбца, на которое указывает правило маскирования.

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

### -DatabaseName
Указывает имя базы данных.

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

### -MaskingFunction
Указывает функцию маскирования, используемую правилом.
Для этого параметра допустимы следующие значения:

- По умолчанию
- Маскировка
- Текстовые
- Счетчик
- SocialSecurityNumber
- CreditCardNumber
- Отправить по электронной почте

По умолчанию используется значение по умолчанию.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: NoMasking, Default, Text, Number, SocialSecurityNumber, CreditCardNumber, Email

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NumberFrom
Задает меньшую границу интервала, из которого выделено случайное значение.
Указывайте этот параметр только в том случае, если для параметра *MaskingFunction* задано значение Number.
Значение по умолчанию — 0.

```yaml
Type: Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NumberTo
Задает верхнюю границу интервала, из которого выделено случайное значение.
Указывайте этот параметр только в том случае, если для параметра *MaskingFunction* задано значение Number.
Значение по умолчанию — 0.

```yaml
Type: Double
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrefixSize
Указывает число знаков в начале текста, для которого не задана маска.
Указывайте этот параметр только в том случае, если для параметра *MaskingFunction* задано значение Text.
Значение по умолчанию — 0.

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

### -ReplacementString
Задает количество символов в конце текста, которые не были скрыты.
Указывайте этот параметр только в том случае, если для параметра *MaskingFunction* задано значение Text.
Значение по умолчанию — 0.

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

### -ResourceGroupName
Указывает имя группы ресурсов, которой назначена база данных.

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

### -SchemaName
Указывает имя схемы.

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

### -ИмяСервера
Указывает имя сервера, на котором размещается база данных.

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

### -SuffixSize
Задает количество символов в конце текста, которые не были скрыты.
Указывайте этот параметр только в том случае, если для параметра *MaskingFunction* задано значение Text.
Значение по умолчанию — 0.

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

### -TableName
Указывает имя таблицы базы данных, которая содержит столбец с маскированием.

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

###  
Ничего

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. SQL. Security. Model. DatabaseDataMaskingRuleModel

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmSqlDatabaseDataMaskingRule](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[New-AzureRmSqlDatabaseDataMaskingRule](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[Remove-AzureRmSqlDatabaseDataMaskingRule](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[Документация по базам данных SQL](https://docs.microsoft.com/azure/sql-database/)


