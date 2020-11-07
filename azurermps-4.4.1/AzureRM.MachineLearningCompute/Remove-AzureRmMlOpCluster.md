---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
ms.openlocfilehash: 63e401c09a2d224b53d260855990198a409d4846
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733107"
---
# Remove-AzureRmMlOpCluster

## КРАТКИй обзор
Удаление кластера операций.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### Удаление кластера выопераций из входных параметров командлета.
```
Remove-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-WhatIf] [-Confirm]
```

### Удаление кластера выопераций из определения экземпляра OperationalizationCluster.
```
Remove-AzureRmMlOpCluster -InputObject <PSOperationalizationCluster> [-WhatIf] [-Confirm]
```

### Удаление кластера выопераций из идентификатора ресурсов Azure.
```
Remove-AzureRmMlOpCluster -ResourceId <String> [-WhatIf] [-Confirm]
```

## NОПИСАНИЕ
Удаление кластера операций. Некоторые ресурсы, связанные с кластером, могут не быть удалены. Например, служба контейнера Azure будет удалена, но связанные виртуальные машины — нет. Учетная запись хранения, реестр контейнера и Application Insights не удаляются для диагностических данных.

## ИЛЛЮСТРИРУЮТ

### Пример 1
```
PS C:\> Remove-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

### Пример 2
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster | Remove-AzureRmMlOpCluster 
```

## ПАРАМЕТРЫ

### -InputObject
Объект кластера для операции.

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Remove an operationalization cluster from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### -Name (имя)
Название кластера операций.

```yaml
Type: String
Parameter Sets: Remove an operationalization cluster from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов для кластера операций.

```yaml
Type: String
Parameter Sets: Remove an operationalization cluster from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Идентификатор ресурса Azure для кластера "эксплуатация".

```yaml
Type: String
Parameter Sets: Remove an operationalization cluster from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

## ВХОДНЫЕ данные

### Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster
### System. String


## НАПРЯЖЕНИЕ

### System. void


## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

