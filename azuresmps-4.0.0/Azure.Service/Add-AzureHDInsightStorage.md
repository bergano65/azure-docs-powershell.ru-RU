---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 1B6AC121-1AA0-4D28-B1EA-C96147FDD168
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3b1eab77edb4743cc6568d2766f1dbc70b19254a
ms.sourcegitcommit: 6f0b6059d096600ebff1c8514c35c467d2f482d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/20/2021
ms.locfileid: "104718722"
---
# Add-AzureHDInsightStorage

## SYNOPSIS
Добавляет запись учетной записи хранилища BLOB-хранилищ в конфигурацию HDInsight.

## СИНТАКСИС

```
Add-AzureHDInsightStorage -Config <AzureHDInsightConfig> -StorageAccountKey <String>
 -StorageAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## ОПИСАНИЕ
Эта версия Azure PowerShell HDInsight не является нужной.
Эти cmdlets будут удалены до 1 января 2017 г.
Используйте более новую версию Azure PowerShell HDInsight.

Сведения об использовании новой hdInsight для создания кластеров см. в видео "Создание кластеров на основе Linux" в [HDInsight с помощью Azure PowerShell.](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/)
Сведения о том, как отправлять задания с помощью Azure PowerShell и других подходов, см. в сведениях о задании [Submit Hadoop в HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) . https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)
Справочные сведения о Azure PowerShell HDInsight см. в [cmdlets Azure HDInsight.](/powershell/module/servicemanagement/azure.service/?view=azuresmps-4.0.0#hd-insights)

**Cmdlet Add-AzureHDInsightStorage** добавляет запись учетной записи хранилища BLOB-хранилищ в конфигурацию Azure HDInsight.

## ПРИМЕРЫ

### Пример 1. Добавление учетной записи хранения
```
PS C:\>$StoreConfig = Add-AzureHDInsightStorage -Config $Config -StorageAccountName "MyStorage" -StorageAccountKey "Key"
```

Эта команда добавляет учетную запись хранения MyStorage к объекту конфигурации, $Config, а затем сохраняет конфигурацию в переменной $StoreConfig конфигурации.

### Пример 2. Настройка нескольких учетных записей хранения
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
    | Add-AzureHDInsightMetastore -SqlAzureServerName "Sqlserver01.database.windows.net" -DatabaseName "MyOozieDatabaseName" -Credential $OozieCreds -MetastoreType OozieMetastore
    | Add-AzureHDInsightMetastore -SqlAzureServerName "Sqlserver01.database.windows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore
    | New-AzureHDInsightCluster -Subscription $SubID -Credential $Creds
```

Первая команда использует командлет **Get-AzureSubscription** для получения текущего ИД подписки, а затем сохраняет его в переменной $SubId подписки.

Вторая и третья команды используют командлет **Get-AzureStorageKey** для получения первичных ключей хранилища для MyBlobStorage и MySecondBlobStorage, а затем сохранить их в переменных $Key 1 и $Key 2 соответственно.

Четвертая, пятая и шестая команды получают учетные данные для текущей подписки и для Oozie иГол, а затем хранят их в переменных.

Конечная команда выполняет последовательность операций с помощью этих командлетов:

- **New-AzureHDInsightClusterConfig** для создания конфигурации кластера HDInsight
- **Set-AzureHDInsightDefaultStorage,** чтобы установить для учетной записи хранилища по умолчанию для конфигурации значение MyBlobStorage.blob.core.windows.net
- **Add-AzureHDInsightStorage,** чтобы добавить в конфигурацию вторую учетную запись MySecondBlobStorage.blob.core.windows.net с именем "MySecondBlobStorage.blob.core.windows.net".
- **Add-AzureHDInsightStorage** для добавления в конфигурацию метамагаба для Oozie и метасхемы для Тега
- Создание кластера HDInsight с новой конфигурацией **new-AzureHDInsightCluster**

## PARAMETERS

### -Config
Указывает объект конфигурации.
Этот cmdlet добавляет сведения об учетной записи хранения к объекту, указанному этим параметром.

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

### -StorageAccountKey
Определяет ключ учетной записи хранения, который используется для доступа к учетной записи хранения.

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

### -StorageAccountName
Имя добавляемой учетной записи хранения Azure.

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

[New-AzureHDInsightCluster](./New-AzureHDInsightCluster.md)

[New-AzureHDInsightClusterConfig](./New-AzureHDInsightClusterConfig.md)

[Set-AzureHDInsightDefaultStorage](./Set-AzureHDInsightDefaultStorage.md)


