---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A6899341-1E5E-4F8B-8D5D-5923B1223628
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: fb0e73d338c54b93626ee3a5ee78bbbe4adca884
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518869"
---
# Get-AzDataLakeAnalyticsCatalogItem

## SYNOPSIS
Возвращает элемент каталога или типы элементов в средстве анализа для озера Данных.

## СИНТАКСИС

```
Get-AzDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [[-Path] <CatalogPathInstance>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
**Get-AzDataLakeAnalyticsCatalogItem** получает указанный элемент каталога Azure Data Lake Analytics или возвращает элементы каталога указанного типа.

## ПРИМЕРЫ

### Пример 1. Получить указанную базу данных
```
PS C:\>Get-AzDataLakeAnalyticsCatalogItem -Account "contosoadla" -ItemType Database -Path "databaseName"
```

Эта команда получает указанную базу данных.

### Пример 2. Доступ к таблицам в указанной базе данных и схеме
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "contosoadla" -ItemType Table -Path "databaseName.schemaName"
```

Эта команда получает список таблиц в указанной базе данных.

## PARAMETERS

### -Account
Указывает имя учетной записи Data Lake Analytics.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -ItemType
Определяет тип элемента каталога, извлекаемого или указанного в списке.
Допустимые значения этого параметра:
- База данных
- Схема
- Сборка
- Таблица
- TableValuedFunction
- TableStatistics
- ExternalDataSource
- "Вид"
- Процедура
- Секретная
- Учетные данные
- Типы
- TablePartition

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType
Parameter Sets: (All)
Aliases:
Accepted values: Database, Schema, Assembly, Table, TablePartition, TableValuedFunction, TableStatistics, ExternalDataSource, View, Procedure, Secret, Credential, Types, Package

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
Путь к элементу с несколькими элементами, которые нужно извлечь, или к родительскому элементу элементов списка.
Части пути должны быть разделены точками (.).

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

### Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType

### Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance

## OUTPUTS

### Microsoft.Azure.Management.DataLake.Analytics.Models.CatalogItem

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Test-AzDataLakeAnalyticsCatalogItem](./Test-AzDataLakeAnalyticsCatalogItem.md)


