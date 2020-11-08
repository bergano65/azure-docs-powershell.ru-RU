---
Module Name: Az.HDInsight
Module Guid: 3fd1475f-cb23-4ffb-bf08-33d94b7d1acb
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight
Help Version: 4.1.2.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
ms.openlocfilehash: e3c3bb9d4d8225823ec84750c8292288ce25c15b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245383"
---
# AZ. HDInsight Module
## Nописание
В этом разделе приведены командлеты Azure PowerShell для Microsoft Azure HDInsight в платформе диспетчера ресурсов Azure (ARM). Эти командлеты используются для управления кластерами HDInsight и заданиями, которые выполняются на них. Командлеты существуют в пространстве имен Microsoft. Azure. Commands. HDInsight.

## Командлеты AZ. HDInsight
### [Add-AzHDInsightClusterIdentity](Add-AzHDInsightClusterIdentity.md)
Добавляет удостоверение кластера в объект конфигурации кластера.

### [Add-AzHDInsightComponentVersion](Add-AzHDInsightComponentVersion.md)
Добавляет версию службы, работающей на кластере, в объект конфигурации кластера.

### [Add-AzHDInsightConfigValue](Add-AzHDInsightConfigValue.md)
Добавляет настройку значения конфигурации Hadoop и (или) общей библиотеки куста в объект конфигурации кластера.

### [Add-AzHDInsightMetastore](Add-AzHDInsightMetastore.md)
Добавляет базу данных SQL, которая будет служить кустом или Oozie MetaStore объекту конфигурации кластера.

### [Add-AzHDInsightScriptAction](Add-AzHDInsightScriptAction.md)
Добавляет действие сценария в объект конфигурации кластера.

### [Add-AzHDInsightSecurityProfile](Add-AzHDInsightSecurityProfile.md)
Добавление профиля безопасности в объект конфигурации кластера.

### [Add-AzHDInsightStorage](Add-AzHDInsightStorage.md)
Добавляет ключ хранилища Azure к объекту конфигурации кластера.

### [Disable-AzHDInsightMonitoring](Disable-AzHDInsightMonitoring.md)
Отключение мониторинга в кластере HDInsight и необходимые журналы будут прекращаться в рабочую область мониторинга, указанную во время включения.

### [Enable-AzHDInsightMonitoring](Enable-AzHDInsightMonitoring.md)
Включает мониторинг в кластере HDInsight, и необходимые журналы будут отправлены в рабочую область мониторинга, указанную во время включения.

### [Get-AzHDInsightCluster](Get-AzHDInsightCluster.md)
Возвращает и перечисляет все кластеры HDInsight Azure, связанные с текущей подпиской или указанной группой ресурсов, или извлекает определенный кластер.

### [Get-AzHDInsightClusterAutoscaleConfiguration](Get-AzHDInsightClusterAutoscaleConfiguration.md)
Получает конфигурацию автомасштабирования кластера HDInsight.

### [Get-AzHDInsightHost](Get-AzHDInsightHost.md)
Список узлов кластера HDInsight.

### [Get-AzHDInsightJob](Get-AzHDInsightJob.md)
Получает список заданий из кластера и перечисляет их в обратном хронологическом порядке или извлекает конкретное задание.

### [Get-AzHDInsightJobOutput](Get-AzHDInsightJobOutput.md)
Получает выходные данные журнала для задания из учетной записи хранения, связанной с указанным кластером.

### [Get-AzHDInsightMonitoring](Get-AzHDInsightMonitoring.md)
Получает состояние наблюдения за установкой на кластере.

### [Get-AzHDInsightPersistedScriptAction](Get-AzHDInsightPersistedScriptAction.md)
Получает хранимые действия сценария для кластера и перечисляет их в хронологическом порядке или получает сведения о указанном сохраненном действии сценария.

### [Get-AzHDInsightProperty](Get-AzHDInsightProperty.md)
Получение свойств службы HDInsight, например доступных местоположений и емкости.

### [Get-AzHDInsightScriptActionHistory](Get-AzHDInsightScriptActionHistory.md)
Получает журнал действий сценария для кластера и перечисляет его в обратном хронологическом порядке или получает сведения о ранее выполненном действии сценария.

### [Invoke-AzHDInsightHiveJob](Invoke-AzHDInsightHiveJob.md)
Отправляет запрос на куст в кластер HDInsight и извлекает результаты запроса в одной операции.

### [New-AzHDInsightCluster](New-AzHDInsightCluster.md)
Создает кластер HDInsight Azure в указанной группе ресурсов для текущей подписки.

### [New-AzHDInsightClusterAutoscaleConfiguration](New-AzHDInsightClusterAutoscaleConfiguration.md)
Создает несохраняемый объект, описывающий конфигурацию автомасштабирования для кластера HDInsight Azure.

### [New-AzHDInsightClusterAutoscaleScheduleCondition](New-AzHDInsightClusterAutoscaleScheduleCondition.md)
Создает условие автомасштабирования на основе расписания.

### [New-AzHDInsightClusterConfig](New-AzHDInsightClusterConfig.md)
Создает несохраняемый объект конфигурации кластера, описывающий конфигурацию кластера Azure HDInsight.

### [New-AzHDInsightHiveJobDefinition](New-AzHDInsightHiveJobDefinition.md)
Создание объекта задания куста.

### [New-AzHDInsightMapReduceJobDefinition](New-AzHDInsightMapReduceJobDefinition.md)
Создает объект задания MapReduce.

### [New-AzHDInsightPigJobDefinition](New-AzHDInsightPigJobDefinition.md)
Создает объект задания свинья.

### [New-AzHDInsightSqoopJobDefinition](New-AzHDInsightSqoopJobDefinition.md)
Создает объект задания Sqoop.

### [New-AzHDInsightStreamingMapReduceJobDefinition](New-AzHDInsightStreamingMapReduceJobDefinition.md)
Создает потоковый объект задания MapReduce.

### [Remove-AzHDInsightCluster](Remove-AzHDInsightCluster.md)
Удаляет указанный кластер HDInsight из текущей подписки.

### [Remove-AzHDInsightClusterAutoscaleConfiguration](Remove-AzHDInsightClusterAutoscaleConfiguration.md)
Удаляет конфигурацию автоматического масштабирования в кластере HDInsight.

### [Remove-AzHDInsightPersistedScriptAction](Remove-AzHDInsightPersistedScriptAction.md)
Удаляет сохраненное действие сценария из кластера HDInsight.

### [Restarting-AzHDInsightHost](Restart-AzHDInsightHost.md)
Перезапускает определенные узлы кластера HDInsight.

### [Set-AzHDInsightClusterAutoscaleConfiguration](Set-AzHDInsightClusterAutoscaleConfiguration.md)
Задает конфигурацию автомасштабирования для кластера HDInsight Azure.

### [Set-AzHDInsightClusterDiskEncryptionKey](Set-AzHDInsightClusterDiskEncryptionKey.md)
Поворачивает ключ шифрования диска для указанного кластера HDInsight.

### [Set-AzHDInsightClusterSize](Set-AzHDInsightClusterSize.md)
Задает количество рабочих узлов в указанном кластере.

### [Set-AzHDInsightDefaultStorage](Set-AzHDInsightDefaultStorage.md)
Задает параметр учетной записи хранения по умолчанию в объекте конфигурации кластера.

### [Set-AzHDInsightGatewayCredential](Set-AzHDInsightGatewayCredential.md)
Задает учетные данные шлюза HTTP для кластера HDInsight Azure.

### [Set-AzHDInsightPersistedScriptAction](Set-AzHDInsightPersistedScriptAction.md)
Задает ранее выполненное действие сценария, которое должно быть сохраненным сценарием.

### [Start-AzHDInsightJob](Start-AzHDInsightJob.md)
Запускает определенное задание Azure HDInsight в указанном кластере.

### [Остановить-AzHDInsightJob](Stop-AzHDInsightJob.md)
Останавливает указанное запущенное задание в кластере.

### [Submit-AzHDInsightScriptAction](Submit-AzHDInsightScriptAction.md)
Отправка нового действия сценария в кластер HDInsight Azure.

### [Use-AzHDInsightCluster](Use-AzHDInsightCluster.md)
Выбор кластера для использования с командлетом Invoke-RmAzureHDInsightHiveJob.

### [Wait-AzHDInsightJob](Wait-AzHDInsightJob.md)
Ожидание завершения или сбоя указанного задания.

