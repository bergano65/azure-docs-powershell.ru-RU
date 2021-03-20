---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: EB196CF5-3E2C-4F38-A983-3365A379672A
online version: ''
schema: 2.0.0
ms.openlocfilehash: d1b38246c9047c29bc876332184501fcd704e78c
ms.sourcegitcommit: 6f0b6059d096600ebff1c8514c35c467d2f482d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/20/2021
ms.locfileid: "104714183"
---
# Add-AzureHDInsightMetastore

## SYNOPSIS
Добавляет учетную SQL Server базы данных в конфигурацию кластера HDInsight.

## СИНТАКСИС

```
Add-AzureHDInsightMetastore -Config <AzureHDInsightConfig> -Credential <PSCredential> -DatabaseName <String>
 -MetastoreType <AzureHDInsightMetastoreType> -SqlAzureServerName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## ОПИСАНИЕ
Эта версия Azure PowerShell HDInsight не является нужной.
Эти cmdlets будут удалены до 1 января 2017 г.
Используйте более новую версию Azure PowerShell HDInsight.

Сведения об использовании новой hdInsight для создания кластеров см. в видео "Создание кластеров на основе Linux" в [HDInsight с помощью Azure PowerShell.](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/)
Сведения о том, как отправлять задания с помощью Azure PowerShell и других подходов, см. в сведениях о задании [Submit Hadoop в HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) . https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)
Справочные сведения о Azure PowerShell HDInsight см. в [cmdlets Azure HDInsight.](/powershell/module/servicemanagement/azure.service/?view=azuresmps-4.0.0#hd-insights)

Cmdlet **Add-AzureHDInsightMetastore** добавляет базу данных Microsoft SQL Server в конфигурацию Azure HDInsight, созданную с помощью **cmdlet New-AzureHDInsightClusterConfig.**
База данных используется для хранения метаданных для Охи или Оози.

## ПРИМЕРЫ

### Пример 1. Добавление метамака
```
PS C:\>$Metaconfig = Add-AzureHDInsightMetastore -Config $Config -SqlAzureServerName "ContosoSQLServer" -DatabaseName "DBname" -Credential (Get-Credential) -MetastoreType HiveMetaStore
```

Эта команда добавляет базу SQL Server с именем ContosoSQLServer, которая будет служить метасемой "Вирус" для кластера HDInsight.

### Пример 2. Настройка хранилища и добавление метахранилищ
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
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.widows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore
    | New-AzureHDInsightCluster -Subscription $SubId -Credential $Creds
```

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

### -Config
Указывает объект конфигурации.
Этот cmdlet добавляет сведения из метахранилища к объекту конфигурации, указанному этим параметром.

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

### -Credential
Определяет учетные данные, которые используются для доступа к SQL Server базе данных.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseName
Имя базы данных, в которой хранятся метаданные Oozie или Оozie.

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

### -MetastoreType
Указывает тип метасхранилища.
Допустимыми значениями для этого параметра являются:ГодаMetaStore или OozieMetaStore.

```yaml
Type: AzureHDInsightMetastoreType
Parameter Sets: (All)
Aliases:

Required: True
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

### -SqlAzureServerName
Определяет полное доменное имя (FQDN) сайта SQL Server содержат базу данных для хранения метаданных.

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

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

## OUTPUTS

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Add-AzureHDInsightStorage](./Add-AzureHDInsightStorage.md)

[New-AzureHDInsightCluster](./New-AzureHDInsightCluster.md)

[New-AzureHDInsightClusterConfig](./New-AzureHDInsightClusterConfig.md)

[Set-AzureHDInsightDefaultStorage](./Set-AzureHDInsightDefaultStorage.md)
