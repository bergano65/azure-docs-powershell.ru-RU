---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 60A5ACF7-2637-4BDC-BF41-80E81B23F4CD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4a0fa409e532640142c03a7570259b6f785c7395
ms.sourcegitcommit: 6f0b6059d096600ebff1c8514c35c467d2f482d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/20/2021
ms.locfileid: "104719283"
---
# Start-AzureHDInsightJob

## SYNOPSIS
Запускает задание HDInsight.

## СИНТАКСИС

### Запуск задания в кластере HDInsight (по умолчанию)
```
Start-AzureHDInsightJob -Cluster <String> [-Credential <PSCredential>]
 -JobDefinition <AzureHDInsightJobDefinition> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Запуск задания в кластере HDInsight (с учетными данными конкретной подписки)
```
Start-AzureHDInsightJob [-Certificate <X509Certificate2>] [-HostedService <String>] -Cluster <String>
 [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] -JobDefinition <AzureHDInsightJobDefinition>
 [-Subscription <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## ОПИСАНИЕ
Эта версия Azure PowerShell HDInsight не является нужной.
Эти cmdlets будут удалены до 1 января 2017 г.
Используйте более новую версию Azure PowerShell HDInsight.

Сведения об использовании новой hdInsight для создания кластеров см. в видео "Создание кластеров на основе Linux" в [HDInsight с помощью Azure PowerShell.](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/)
Сведения о том, как отправлять задания с помощью Azure PowerShell и других подходов, см. в сведениях о задании [Submit Hadoop в HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) . https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)
Справочные сведения о Azure PowerShell HDInsight см. в [cmdlets Azure HDInsight.](/powershell/module/servicemanagement/azure.service/?view=azuresmps-4.0.0#hd-insights)

С **его использованием** запускается задание Azure HDInsight в заданном кластере.
В качестве задания можно начать задание MapReduce, задание потоковой передачи, задание "Кот" или задание "Порося".

## ПРИМЕРЫ

### Пример 1. Запуск задания HDInsight
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $ClusterName = "Cluster01"
PS C:\> $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "Wordcount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount"
PS C:\> $WordCountJob | Start-AzureHDInsightJob -Cluster $ClusterName
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -Subscription $SubId -StandardError
```

Первая команда получает текущий ИД подписки, а затем сохраняет его в переменной $SubId подписки.

Вторая команда назначает переменной $ClusterName "Кластер01".

Третья команда использует командлет **New-AzureHDInsightMapReduceJobDefinition** для создания определения задания MapReduce, а затем сохраняет его в переменной $WordCountJob.

Конечная команда использует оператор конвейера для $WordCountJob запуска задания в командлет **Start-AzureHDInsightJob.**
После начала задания оно передается в cmdlet **Wait-AzureHDInsightJob,** который ждет завершения задания, прежде чем передавать его на **cmdlet Get-AzureHDInsightJobOutput,** чтобы получить результаты задания.

## PARAMETERS

### -Certificate
Указывает сертификат управления для подписки Azure.

```yaml
Type: X509Certificate2
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Кластер
Указывает кластер.
Этот cmdlet запускает задание для кластера, указанного этим параметром.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Credential
Определяет учетные данные кластера для прямого http-доступа к кластеру.
Этот параметр можно указать вместо параметра *Subscription* для проверки подлинности доступа к кластеру.

```yaml
Type: PSCredential
Parameter Sets: Start jobDetails on an HDInsight Cluster
Aliases: Cred

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Конечная точка
Указывает конечную точку, используемую для подключения к Azure.
Если этот параметр не задан, используется конечная точка по умолчанию.

```yaml
Type: Uri
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostedService
Определяет пространство имен службы HDInsight, если вы не хотите использовать пространство имен по умолчанию.

```yaml
Type: String
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IgnoreSslErrors
Указывает на то, игнорируются ли ошибки SSL.

```yaml
Type: Boolean
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobDefinition
Указывает конечную точку, которая будет использовать при подключении к Microsoft Azure, если она отличается от используемой по умолчанию.

```yaml
Type: AzureHDInsightJobDefinition
Parameter Sets: (All)
Aliases: jobDetails

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### -Подписка
Указывает подписку.
Этот cmdlet запускает задание для подписки, указанной этим параметром.

```yaml
Type: String
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: Sub

Required: False
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

[Get-AzureHDInsightJob](./Get-AzureHDInsightJob.md)

[Get-AzureHDInsightJobOutput](./Get-AzureHDInsightJobOutput.md)

[New-AzureHDInsightMapReduceJobDefinition](./New-AzureHDInsightMapReduceJobDefinition.md)

[Stop-AzureHDInsightJob](./Stop-AzureHDInsightJob.md)

[Wait-AzureHDInsightJob](./Wait-AzureHDInsightJob.md)


