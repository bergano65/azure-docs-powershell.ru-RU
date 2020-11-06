---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 8C6D9533-68FD-4AFF-91FB-8307A8C8EAEB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightRdpServicesAccess.md
ms.openlocfilehash: f05cae3484067f227fde8f30cd7806307832b185
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559800"
---
# Revoke-AzureRmHDInsightRdpServicesAccess

## КРАТКИй обзор
Запрещает RDP-доступ к кластеру Windows.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Revoke-AzureRmHDInsightRdpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **REVOKE-AzureRmHDInsightRdpServicesAccess** отключает доступ к протоколу удаленного рабочего стола (RDP) к кластеру Azure HDInsight на базе Windows.

## ИЛЛЮСТРИРУЮТ

### Пример 1: отключение доступа к указанному кластеру через RDP
```
PS C:\>Revoke-AzureRmHDInsightRdpServicesAccess -ClusterName "your-hadoop-001"
```

Эта команда запрещает доступ по протоколу RDP к кластеру с именем-Hadoop-001.

## ПАРАМЕТРЫ

### -Имя_кластера
Указывает имя кластера.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
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

## НАПРЯЖЕНИЕ

### System. void

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Grant-AzureRmHDInsightRdpServicesAccess](./Grant-AzureRmHDInsightRdpServicesAccess.md)


