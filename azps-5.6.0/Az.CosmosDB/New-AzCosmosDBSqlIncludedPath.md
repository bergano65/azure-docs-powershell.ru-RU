---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqlincludedpath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPath.md
ms.openlocfilehash: a9d77cc76521eca1e99dac630673ef3825d1155b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962435"
---
# New-AzCosmosDBSqlIncludedPath

## SYNOPSIS
Создание объекта типа PSIncludedPath. Его можно передать в качестве значения параметра для Set-AzCosmosDBSqlContainer.

## СИНТАКСИС

```
New-AzCosmosDBSqlIncludedPath [-Path <String>] [-Index <PSIndexes[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
Объект, соответствующий API Sql IncludedPath.

## ПРИМЕРЫ

### Пример 1
```powershell
PS C:\> $index1 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
$index2 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash

New-AzCosmosDBSqlIncludedPath -Path "/*" -Index $index1,$index2

Path Indexes
---- -------
/*   {Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes,Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes}
```

## PARAMETERS

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Index
Список индексов для этого пути

```yaml
Type: PSIndexes[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Путь, к которому относится индексация.
Путь индекса обычно начинается с корневого и заканчивается поддиками (/path/*)

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Нет

## OUTPUTS

### Microsoft.Azure.Commands.ВацDB.Models.PSIncludedPath

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ
