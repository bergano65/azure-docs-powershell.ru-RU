---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightgatewaycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightGatewayCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightGatewayCredential.md
ms.openlocfilehash: f3997247c9a32fa9066e17dff3a09f2bd65a80d5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328275"
---
# Set-AzHDInsightGatewayCredential

## SYNOPSIS
Задает учетные данные шлюза HTTP в кластере Azure HDInsight.

## СИНТАКСИС

### SetByNameParameterSet (по умолчанию)
```
Set-AzHDInsightGatewayCredential [-Name] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetByInputObjectParameterSet
```
Set-AzHDInsightGatewayCredential [-HttpCredential] <PSCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] -InputObject <AzureHDInsightCluster> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetByResourceIdParameterSet
```
Set-AzHDInsightGatewayCredential [-HttpCredential] <PSCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## ОПИСАНИЕ
Cmdlet **Set-AzHDInsightGatewayCredential** задает учетные данные шлюза для кластера Azure HDInsight.

## ПРИМЕРЫ

### Пример 1
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Set-AzHDInsightGatewayCredential `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds
```

Эта команда задает учетные данные шлюза для кластера с именем hadoop-001 по набору параметров имени.

### Пример 2
```powershell
PS C:\> Set-AzHDInsightGatewayCredential `
            -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.HDInsight/clusters/your-hadoop-001" `
            -HttpCredential $clusterCreds
```

Эта команда задает учетные данные шлюза для кластера с именем hadoop-001 by ResourceId.

### Пример 3
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Get-AzHDInsightCluster -ClusterName $clusterName | Set-AzHDInsightGatewayCredential `
            -HttpCredential $clusterCreds
```

Эта команда задает учетные данные шлюза для кластера "ваш-hadoop-001" с помощью набора параметров InputObject.

## PARAMETERS

### -AsJob
Запустите cmdlet в фоновом режиме.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -httpCredential
Возвращает или устанавливает вход для пользователя кластера.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InputObject
Возвращает или устанавливает объект ввода.

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Возвращает или задает имя кластера.

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Возвращает или задает имя группы ресурсов.

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Возвращает или задает ид ресурса.

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Запрос на подтверждение перед запуском cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске cmdlet. Этот cmdlet не будет выполниться.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

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

### Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightGatewaySettings

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ
