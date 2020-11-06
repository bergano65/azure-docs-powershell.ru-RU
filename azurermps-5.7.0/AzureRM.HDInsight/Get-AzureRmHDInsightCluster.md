---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: FA154E07-EA26-4688-986E-C53C3A9E4F06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightCluster.md
ms.openlocfilehash: 76cf830e79c2374d81c57a1341ae99636333e273
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566184"
---
# Get-AzureRmHDInsightCluster

## КРАТКИй обзор
Возвращает и перечисляет все кластеры HDInsight Azure, связанные с текущей подпиской или указанной группой ресурсов, или извлекает определенный кластер.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Get-AzureRmHDInsightCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmHDInsightCluster** включает в себя кластеры служб Azure HDInsight для текущей подписки.
Используйте параметр *имя_кластера* для получения подробных сведений о конкретном кластере.

## ИЛЛЮСТРИРУЮТ

### Пример 1: список всех кластеров Azure HDInsight
```
PS C:\>Get-AzureRmHDInsightCluster
```

Эта команда выводит список всех кластеров Azure HDInsight.

## ПАРАМЕТРЫ

### -Имя_кластера
Указывает имя кластера.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
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

### -ResourceGroupName
Указывает имя группы ресурсов.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего
Этот командлет не поддерживает никаких входных данных.

## НАПРЯЖЕНИЕ

### System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. AzureHDInsightCluster]

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Remove-AzureRmHDInsightCluster](./Remove-AzureRmHDInsightCluster.md)

[Use-AzureRmHDInsightCluster](./Use-AzureRmHDInsightCluster.md)


