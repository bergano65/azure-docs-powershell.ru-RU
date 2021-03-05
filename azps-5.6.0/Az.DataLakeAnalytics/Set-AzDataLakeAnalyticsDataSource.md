---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 2F28118E-6A34-4261-85BD-8CFDDC8A2707
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: cb51b1c703d527a2888bd0e80d8cc7a50d044e36
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962371"
---
# Set-AzDataLakeAnalyticsDataSource

## SYNOPSIS
Изменяет сведения об источнике данных учетной записи Data Lake Analytics.

## СИНТАКСИС

```
Set-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
**Cmdlet Set-AzDataLakeAnalyticsDataSource** изменяет сведения об источнике данных учетной записи Azure Data Lake Analytics.

## ПРИМЕРЫ

### Пример 1. Изменение ключа доступа к источнику данных
```
PS C:\>Set-AzDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "contosowasb" -AccessKey "...newaccesskey..."
```

Эта команда изменяет ключ доступа, который хранится в источнике данных хранилища BLOB-приложений Azure.

## PARAMETERS

### -AccessKey
Указывает новый ключ доступа к источнику данных хранилища BLOB-элементов Azure.

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

### -BLOB
Имя источника данных хранилища BLOB-источников Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AzureBlob

Required: True
Position: 1
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

### -ResourceGroupName
Имя группы ресурсов для учетной записи Data Lake Analytics.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

## OUTPUTS

### System.Void

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Add-AzDataLakeAnalyticsDataSource](./Add-AzDataLakeAnalyticsDataSource.md)

[Remove-AzDataLakeAnalyticsDataSource](./Remove-AzDataLakeAnalyticsDataSource.md)


