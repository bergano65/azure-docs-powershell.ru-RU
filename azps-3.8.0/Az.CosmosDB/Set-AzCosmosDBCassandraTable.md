---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBCassandraTable.md
ms.openlocfilehash: e79353d5265a2d58b72e49ee1978ea92599bed39
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074439"
---
# Set-AzCosmosDBCassandraTable

## КРАТКИй обзор
Задает таблицу CosmosDB Cassandra.

## Максимальное

### ByNameParameterSet (по умолчанию)
```
Set-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-Throughput <Int32>] [-TtlInSeconds <Int32>] -Schema <PSCassandraSchema>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByParentObjectParameterSet
```
Set-AzCosmosDBCassandraTable -Name <String> [-Throughput <Int32>] [-TtlInSeconds <Int32>]
 -Schema <PSCassandraSchema> -InputObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzCosmosDBCassandraTable** задает CosmosDB Cassandra keyspace.

## ИЛЛЮСТРИРУЮТ

### Пример 1
```powershell
PS C:\> Set-AzCosmosDBCassandraTable -ResourceGroupName {rgName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {tableName}
Name        Id    Resource
----        --    -------
{name}     {id}   Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetPropertiesResource
```

Объект Resource включает значения свойств _rid, _ts, _etag, DefaultTtl и Schema.

## ПАРАМЕТРЫ

### -Имя_учетной_записи
Имя учетной записи базы данных Cosmos DB.

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### -InputObject
Объект Cassandra keyspace.

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -KeyspaceName
Cassandra keyspace имя.

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (имя)
Имя таблицы Cassandra.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов.

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Schema
Объект PSCassandraSchema.
Для создания объекта используйте New-AzCosmosDBCassandraSchema.

```yaml
Type: PSCassandraSchema
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Пропускная способность
Пропускная способность Cassandra keyspace (RU/s).
Значение по умолчанию — 400.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TtlInSeconds
Срок жизни по умолчанию (в секундах).
Если значение отсутствует или равно-1, срок действия элементов не истекает.
Если для параметра установлено значение n, срок действия элементов заканчивается на n секунд после последнего изменения.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## ВХОДНЫЕ данные

### Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraSchema

### Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraTableGetResults

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
