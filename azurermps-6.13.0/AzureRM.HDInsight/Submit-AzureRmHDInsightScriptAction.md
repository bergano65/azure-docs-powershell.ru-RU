---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 15C5D659-472B-41DD-806A-A0A175434EE3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/submit-azurermhdinsightscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Submit-AzureRmHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Submit-AzureRmHDInsightScriptAction.md
ms.openlocfilehash: 884741f6543dee05ed8236385071ad345321413e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564459"
---
# Submit-AzureRmHDInsightScriptAction

## КРАТКИй обзор
Отправка нового действия сценария в кластер HDInsight Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Submit-AzureRmHDInsightScriptAction [-ClusterName] <String> [-Name] <String> [-Uri] <Uri>
 [-NodeTypes] <RuntimeScriptActionClusterNodeType[]> [[-Parameters] <String>] [[-ApplicationName] <String>]
 [-PersistOnSuccess] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Submit-AzureRmHDInsightScriptAction** отправляет новое действие сценария в кластер HDInsight Azure.
Используйте *PersistOnSuccess* , чтобы действие сценария выполнялось каждый раз при масштабировании кластера до тех пор, пока действие сценария завершится успешно.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Отправка нового действия сценария в запущенный кластер HDInsight
```
PS C:\>Submit-AzureRmHDInsightScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "scriptaction" `
            -Uri "<script action URI>" `
            -NodeTypes Worker -PersistOnSuccess
```

Эта команда отправляет действие сценария в запущенный кластер HDInsight.

## ПАРАМЕТРЫ

### -ИмяПриложения
Указывает имя приложения для действия сценария.
Если *applicationName* задано, для *PersistOnSuccess* должно быть задано значение false, узлы должны содержать только edgenode и количество действий сценария должно равняться 1.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -Name (имя)
Задает имя действия сценария.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NodeType
Задает типы узлов, для которых нужно выполнить действие сценария.

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.RuntimeScriptActionClusterNodeType[]
Parameter Sets: (All)
Aliases:
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Parameters
Задает параметры действия сценария.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PersistOnSuccess
Указывает на то, что действие сценария должно выполняться каждый раз при масштабировании кластера.
Этот параметр ключа игнорируется, если действие сценария завершается сбоем.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
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

### -URI
Задает общедоступный URI для действия сценария (сценарий PowerShell или bash).

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String

### System. URI

### Microsoft. Azure. Commands. HDInsight. Models. Management. RuntimeScriptActionClusterNodeType []

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightRuntimeScriptActionOperationResource

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Add-AzureRmHDInsightScriptAction](./Add-AzureRmHDInsightScriptAction.md)


