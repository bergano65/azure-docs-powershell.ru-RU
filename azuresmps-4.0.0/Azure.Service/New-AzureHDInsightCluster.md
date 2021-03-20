---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 3EDD612F-AC5D-4D4D-BB14-2FB8DE5EDCCE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0f2cee18de1f563be754caaea4d283d92eef4c2d
ms.sourcegitcommit: 6f0b6059d096600ebff1c8514c35c467d2f482d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/20/2021
ms.locfileid: "104714441"
---
# New-AzureHDInsightCluster

## SYNOPSIS
Создает кластер HDInsight.

## СИНТАКСИС

### Кластер по config (с конкретными учетными данными подписки) (по умолчанию)
```
New-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>]
 -Config <AzureHDInsightConfig> -Credential <PSCredential> [-EndPoint <Uri>] [-IgnoreSslErrors <Boolean>]
 -Location <String> -Name <String> [-Subscription <String>] [-Version <String>] [-OSType <OSType>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Кластер по имени (с учетными данными конкретной подписки)
```
New-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>]
 -ClusterSizeInNodes <Int32> -Credential <PSCredential> -DefaultStorageAccountKey <String>
 -DefaultStorageAccountName <String> -DefaultStorageContainerName <String> [-EndPoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Location <String> -Name <String> [-Subscription <String>] [-Version <String>]
 [-HeadNodeVMSize <String>] [-ClusterType <ClusterType>] [-VirtualNetworkId <String>] [-SubnetName <String>]
 [-DataNodeVMSize <String>] [-ZookeeperNodeVMSize <String>] [-OSType <OSType>] [-SshCredential <PSCredential>]
 [-SshPublicKey <String>] [-RdpCredential <PSCredential>] [-RdpAccessExpiry <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## ОПИСАНИЕ
Эта версия Azure PowerShell HDInsight не является нужной.
Эти cmdlets будут удалены до 1 января 2017 г.
Используйте более новую версию Azure PowerShell HDInsight.

Сведения об использовании новой hdInsight для создания кластеров см. в видео "Создание кластеров на основе Linux" в [HDInsight с помощью Azure PowerShell.](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/)
Сведения о том, как отправлять задания с помощью Azure PowerShell и других подходов, см. в сведениях о задании [Submit Hadoop в HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) . https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)
Справочные сведения о Azure PowerShell HDInsight см. в [cmdlets Azure HDInsight.](/powershell/module/servicemanagement/azure.service/?view=azuresmps-4.0.0#hd-insights)

Cmdlet **New-AzureHDInsightCluster** создает кластер Azure HDInsight с использованием указанных параметров или с помощью объекта конфигурации, созданного с помощью **командылета New-AzureHDInsightClusterConfig.**

## ПРИМЕРЫ

### Пример 1. Создание кластера HDInsight
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $Key1 = Get-AzureStorageKey -StorageAccountName "MyBlobStorage" | %{ $_.Primary }
PS C:\> $Key2 = Get-AzureStorageKey -StorageAccountName "MySecondBlobStorage" | %{ $_.Primary }
PS C:\> $Creds = Get-Credential
PS C:\> $OozieCreds = Get-Credential
PS C:\> $HiveCreds = Get-Credential
PS C:\> New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4
    | Set-AzureHDInsightDefaultStorage -StorageAccountName "MyBlobStorage.blob.core.windows.net" -StorageAccountKey $Key1 -StorageContainerName "MyContainer"
    | Add-AzureHDInsightStorage -StorageAccountName "MySecondBlobStorage.blob.core.windows.net" -StorageAccountKey $Key2
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.windows.net" -DatabaseName "MyOozieDatabaseName" -Credential $OozieCreds -MetastoreType OozieMetastore
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.windows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore
    | New-AzureHDInsightCluster -Subscription $SubId -Credential $Creds
```

В этом примере создается кластер HDInsight для текущей подписки.

Первая команда использует командлет **Get-AzureSubscription** для получения текущего ИД подписки, а затем сохраняет его в переменной $SubId подписки.

Вторая и третья команды используют командлет **Get-AzureStorageKey** для получения первичных ключей хранилища для MyBlobStorage и MySecondBlobStorage, а затем сохранить их в переменных $Key 1 и $Key 2 соответственно.

Четвертая, пятая и шестая команды используют командлет **Get-Credential** для получения учетных данных для текущей подписки и для Oozie иГол, а затем хранят их в переменных.

Конечная команда выполняет последовательность операций с помощью этих командлетов:

- **New-AzureHDInsightClusterConfig** для создания конфигурации кластера HDInsight.
- **Set-AzureHDInsightDefaultStorage,** чтобы установить для учетной записи хранилища по умолчанию для конфигурации значение MyBlobStorage.blob.core.windows.net.
- **Add-AzureHDInsightStorage,** чтобы добавить в конфигурацию вторую учетную запись MySecondBlobStorage.blob.core.windows.net хранения.
- **Add-AzureHDInsightMetastore,** чтобы добавить в конфигурацию метамагию для Oozie и метасхему для Сергея.
- **New-AzureHDInsightCluster** для создания кластера HDInsight с новой конфигурацией.

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

### -ClusterSizeInNodes
Количество узлов данных, которые нужно создать для кластера.

```yaml
Type: Int32
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: Nodes, Size

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClusterType
Тип кластера, который нужно создать.

```yaml
Type: ClusterType
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Config
Определяет объект конфигурации, созданный с помощью **командылета New-AzureHDInsightClusterConfig.**

```yaml
Type: AzureHDInsightConfig
Parameter Sets: Cluster By Config (with Specific Subscription Credential)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Credential
Определяет учетные данные пользователя для УЧЕТной записи HDInsight, используемой по умолчанию для удаленного доступа к кластеру Hadoop.
Эти учетные данные отличаются от учетных данных подписки пользователя.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: Cred

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DataNodeVMSize
Определяет размер виртуальной машины для узла данных.

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultStorageAccountKey
Указывает ключ учетной записи хранения, которая используется по умолчанию для кластера HDInsight.

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: StorageKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultStorageAccountName
Указывает имя учетной записи хранения по умолчанию, которая используется кластером HDInsight.

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: StorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultStorageContainerName
Имя контейнера по умолчанию в учетной записи хранилища Azure, которая используется в кластере HDInsight по умолчанию.

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: StorageContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndPoint
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

### -HeadNodeVMSize
Определяет размер виртуальной машины для главного узла.

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
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

### -Location
Определяет регион, в котором нужно создать кластер HDInsight.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Loc

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Указывает имя кластера Azure HDInsight, который нужно создать.

```yaml
Type: String
Parameter Sets: Cluster By Config (with Specific Subscription Credential)
Aliases: ClusterName, DnsName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: ClusterName, DnsName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OSType
Указывает операционную систему для кластера.

```yaml
Type: OSType
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

### -RdpAccessExpiry
Указывает срок действия в качестве объекта **даты и** времени для доступа к кластеру протокола удаленных рабочих столов.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RdpCredential
Определяет учетные данные для доступа RDP к кластеру.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SshCredential
Определяет имя пользователя и пароль защищенной оболочки (SSH) для кластера HDInsight.
Этот параметр действителен только для кластеров Linux.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SshPublicKey
Указывает общедоступный ключ SSH для кластера HDInsight.
Этот параметр действителен только для кластеров Linux.

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

### -SubnetName
Имя подсети.

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Подписка
Указывает подписку Azure, в которой нужно создать кластер HDInsight.

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

### -Версия
Указывает версию кластера HDInsight, которая будет создаваться.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Ver

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualNetworkId
Определяет ИД виртуальной сети, в которую нужно подавь кластер.

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeeperNodeVMSize
Определяет размер виртуальной машины для узлаKeeper.
Этот параметр действителен только для кластеров HBase или Storm.

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases:

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

[Add-AzureHDInsightMetastore](./Add-AzureHDInsightMetastore.md)

[Add-AzureHDInsightStorage](./Add-AzureHDInsightStorage.md)

[Get-AzureHDInsightCluster](./Get-AzureHDInsightCluster.md)

[New-AzureHDInsightClusterConfig](./New-AzureHDInsightClusterConfig.md)

[Remove-AzureHDInsightCluster](./Remove-AzureHDInsightCluster.md)

[Set-AzureHDInsightDefaultStorage](./Set-AzureHDInsightDefaultStorage.md)

[Use-AzureHDInsightCluster](./Use-AzureHDInsightCluster.md)


