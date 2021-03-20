---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 3B39F43D-E74A-441D-91BC-26C324C1EDF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1e1494895cd4b0694d37a526b79783e2aa97cd67
ms.sourcegitcommit: 6f0b6059d096600ebff1c8514c35c467d2f482d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/20/2021
ms.locfileid: "104714200"
---
# Get-AzureHDInsightCluster

## SYNOPSIS
Возвращает кластер HDInsight.

## СИНТАКСИС

```
Get-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] [-Name <String>] [-Subscription <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## ОПИСАНИЕ
Эта версия Azure PowerShell HDInsight не является нужной.
Эти cmdlets будут удалены до 1 января 2017 г.
Используйте более новую версию Azure PowerShell HDInsight.

Сведения об использовании новой hdInsight для создания кластеров см. в видео "Создание кластеров на основе Linux" в [HDInsight с помощью Azure PowerShell.](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/)
Сведения о том, как отправлять задания с помощью Azure PowerShell и других подходов, см. в сведениях о задании [Submit Hadoop в HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) . https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)
Справочные сведения о Azure PowerShell HDInsight см. в [cmdlets Azure HDInsight.](/powershell/module/servicemanagement/azure.service/?view=azuresmps-4.0.0#hd-insights)

Для **текущей подписки cmdlet Get-AzureHDInsightCluster** получает кластеры службы Azure HDInsight.
Параметр Name можно использовать *для* получения определенного кластера.

## ПРИМЕРЫ

### Пример 1. Получить кластеры в подписке
```
PS C:\> Get-AzureHDInsightCluster
```

Эта команда получает сведения о кластерах HDInsight в текущей подписке.

## PARAMETERS

### -Certificate
Указывает сертификат управления для подписки Azure.

```yaml
Type: X509Certificate2
Parameter Sets: (All)
Aliases: Cert

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
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostedService
Определяет пространство имен службы HDInsight.
Если этот параметр не задан, используется пространство имен по умолчанию.

```yaml
Type: String
Parameter Sets: (All)
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
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Название кластера HDInsight, который нужно получить.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName, DnsName

Required: False
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
Подписка, которая содержит кластер HDInsight, который нужно получить.

```yaml
Type: String
Parameter Sets: (All)
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

[New-AzureHDInsightCluster](./New-AzureHDInsightCluster.md)

[Remove-AzureHDInsightCluster](./Remove-AzureHDInsightCluster.md)

[Use-AzureHDInsightCluster](./Use-AzureHDInsightCluster.md)


