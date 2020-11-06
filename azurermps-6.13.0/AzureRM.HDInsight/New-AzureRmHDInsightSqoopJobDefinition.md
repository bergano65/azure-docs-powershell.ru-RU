---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 4ED47646-542B-4983-B46B-B603BE33D499
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightsqoopjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightSqoopJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightSqoopJobDefinition.md
ms.openlocfilehash: 709c87084cc871814e4760e0d2641c59b0e5a64e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564460"
---
# New-AzureRmHDInsightSqoopJobDefinition

## КРАТКИй обзор
Создает объект задания Sqoop.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
New-AzureRmHDInsightSqoopJobDefinition [-Files <String[]>] [-StatusFolder <String>] [-File <String>]
 [-Command <String>] [-LibDir <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzureRmHDInsightSqoopJobDefinition** определяет объект задания Sqoop для использования с кластером HDInsight Azure.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Создание определения задания Sqoop
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzureRmHDInsightSqoopJobDefinition -StatusFolder $statusFolder `
            -Command $sqoopCommand `
        | Start-AzureRmHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

Эта команда создает определение задания Sqoop.

## ПАРАМЕТРЫ

### -Command
Задает команду Sqoop.

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
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

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

### -Файл
Задает путь к файлу, содержащему запрос для запуска.
Файл должен быть доступен в учетной записи хранения, связанной с кластером.
Вы можете использовать этот параметр вместо параметра *запроса* .

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

### -Файлы
Указывает набор файлов, связанных с заданием куста.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LibDir
Указывает каталог библиотеки для задания Sqoop.

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

### -StatusFolder
Указывает расположение папки, содержащей стандартные выходные данные и выходные ошибки для задания.

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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightSqoopJobDefinition

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Start-AzureRmHDInsightJob](./Start-AzureRmHDInsightJob.md)


