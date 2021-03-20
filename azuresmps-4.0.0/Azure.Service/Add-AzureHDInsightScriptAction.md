---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 600D35F8-1E3C-4724-9F5E-75CF754F424F
online version: ''
schema: 2.0.0
ms.openlocfilehash: dc2fb7414cdd382572576c6c89e38d791cbc0831
ms.sourcegitcommit: 6f0b6059d096600ebff1c8514c35c467d2f482d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/20/2021
ms.locfileid: "104718739"
---
# Add-AzureHDInsightScriptAction

## SYNOPSIS
Добавляет действие сценария HDInsight.

## СИНТАКСИС

```
Add-AzureHDInsightScriptAction -Config <AzureHDInsightConfig> -Name <String>
 -ClusterRoleCollection <ClusterNodeType[]> -Uri <Uri> [-Parameters <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## ОПИСАНИЕ
Эта версия Azure PowerShell HDInsight не является нужной.
Эти cmdlets будут удалены до 1 января 2017 г.
Используйте более новую версию Azure PowerShell HDInsight.

Сведения об использовании новой hdInsight для создания кластеров см. в видео "Создание кластеров на основе Linux" в [HDInsight с помощью Azure PowerShell.](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/)
Сведения о том, как отправлять задания с помощью Azure PowerShell и других подходов, см. в сведениях о задании [Submit Hadoop в HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) . https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)
Справочные сведения о Azure PowerShell HDInsight см. в [cmdlets Azure HDInsight.](/powershell/module/servicemanagement/azure.service/?view=azuresmps-4.0.0#hd-insights)

С помощью cmdlet **Add-AzureHDInsightScriptAction** можно использовать функции Azure HDInsight, которые используются для установки дополнительного программного обеспечения или изменения конфигурации приложений, которые запускаются на кластере Hadoop с помощью Windows PowerShell сценариев.

На узлах кластера выполняется действие сценария при развертывании кластеров HDInsight и после узлов в конфигурации HDInsight кластера.
Сценарий выполняется в соответствии с правами учетной записи администратора и предоставляет полные права доступа к узлам кластера.
Вы можете предоставить каждому кластеру список действий сценариев, которые должны запускаться в указанной последовательности.

## ПРИМЕРЫ

### Пример 1. Добавление действия сценария в кластер
```
PS C:\>$Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4
PS C:\> $Config = Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction" -Uri http://test.com/test.ps1 -Parameters "test" -ClusterRoleCollection HeadNode,DataNode
PS C:\> New-AzureHDInsightCluster -Config $Config
```

Первая команда использует командлет **New-AzureHDInsightClusterConfig** для создания конфигурации кластера HDInsight, а затем сохраняет ее в переменной $Config.

Вторая команда использует командлет **Add-AzureHDInsightScriptAction** для добавления в $Config действия сценария TestScriptAction.

В последней команде используется командлет **New-AzureHDInsightCluster** для создания нового кластера HDInsight, который выполняет действие сценария, храняное в $Config.

### Пример 2. Добавление нескольких действий сценария в кластер
```
PS C:\>$Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4
PS C:\> $Config = Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction1" -Uri http://test.com/test1.ps1 -Parameters "Test1" -ClusterRoleCollection HeadNode,DataNode | Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction2" -Uri http://test.com/test2.ps1 -ClusterRoleCollection HeadNode
PS C:\> New-AzureHDInsightCluster -Config $Config
```

Первая команда использует командлет **New-AzureHDInsightClusterConfig** для создания конфигурации кластера HDInsight, а затем сохраняет ее в переменной $Config.

Вторая команда использует командлет **Add-AzureHDInsightScriptAction** для добавления указанного действия сценария в $Config, а затем с помощью оператора конвейера передает $Config **add-AzureHDInsightScriptAction** еще раз, чтобы добавить второе действие сценария в $Config.

В последней команде используется командлет **New-AzureHDInsightCluster** для создания кластера, который выполняет действия сценария в $Config.

## PARAMETERS

### -ClusterRoleCollection
Определяет узлы, для которых нужно выполнить сценарий.
Допустимыми значениями для этого параметра являются HeadNode или DataNode.

Можно указать одно или оба значения.

```yaml
Type: ClusterNodeType[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Config
Указывает объект конфигурации.
Этот cmdlet добавляет сведения о действиях сценария к объекту, указанному этим параметром.

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Указывает имя действия сценария.

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

### -Parameters
Параметры, необходимые для действия сценария.

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

### -Profile
Определяет профиль Azure, для которого читается этот cmdlet.
Если не указать профиль, этот cmdlet будет читать данные из локального профиля по умолчанию.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Uri
Определяет расположение URI запускаемого сценария.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

## OUTPUTS

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[New-AzureHDInsightCluster](./New-AzureHDInsightCluster.md)

[New-AzureHDInsightClusterConfig](./New-AzureHDInsightClusterConfig.md)


