---
Module Name: Az.HDInsight
Module Guid: 3fd1475f-cb23-4ffb-bf08-33d94b7d1acb
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight
Help Version: 4.1.2.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
ms.openlocfilehash: 78153558764d12a63d6c1b599da2067338969628
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "93719870"
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
Добавляет profileto безопасности объекта конфигурации кластера.

### [Add-AzHDInsightStorage](Add-AzHDInsightStorage.md)
Добавляет ключ хранилища Azure к объекту конфигурации кластера.

### [Disable-AzHDInsightOperationsManagementSuite](Disable-AzHDInsightOperationsManagementSuite.md)
Отключает набор Operations Management Suite (OMS) в HDInsight кластере, и необходимые журналы перестают передаваться в рабочую область OMS, указанную во время включения.

### [Enable-AzHDInsightOperationsManagementSuite](Enable-AzHDInsightOperationsManagementSuite.md)
Включает набор Operations Management Suite (OMS) в кластере HDInsight, и необходимые журналы будут отправлены в рабочую область OMS, указанную во время включения.

### [Get-AzHDInsightCluster](Get-AzHDInsightCluster.md)
Возвращает и перечисляет все кластеры HDInsight Azure, связанные с текущей подпиской или указанной группой ресурсов, или извлекает определенный кластер.

### [Get-AzHDInsightJob](Get-AzHDInsightJob.md)
Получает список заданий из кластера и перечисляет их в обратном хронологическом порядке или извлекает конкретное задание.

### [Get-AzHDInsightJobOutput](Get-AzHDInsightJobOutput.md)
Получает выходные данные журнала для задания из учетной записи хранения, связанной с указанным кластером.

### [Get-AzHDInsightOperationsManagementSuite](Get-AzHDInsightOperationsManagementSuite.md)
Получает состояние установки Operations Management Suite (OMS) в кластере.

### [Get-AzHDInsightPersistedScriptAction](Get-AzHDInsightPersistedScriptAction.md)
Получает хранимые действия сценария для кластера и перечисляет их в хронологическом порядке или получает сведения о указанном сохраненном действии сценария.

### [Get-AzHDInsightProperty](Get-AzHDInsightProperty.md)
Получение свойств службы HDInsight, например доступных местоположений и емкости.

### [Get-AzHDInsightScriptActionHistory](Get-AzHDInsightScriptActionHistory.md)
Получает журнал действий сценария для кластера и перечисляет его в обратном хронологическом порядке или получает сведения о ранее выполненном действии сценария.

### [Grant-AzHDInsightHttpServicesAccess](Grant-AzHDInsightHttpServicesAccess.md)
Предоставление доступа к кластеру через HTTP.

### [Grant-AzHDInsightRdpServicesAccess](Grant-AzHDInsightRdpServicesAccess.md)
Предоставление доступа к кластеру Windows для подключения к удаленному рабочему столу.

### [Invoke-AzHDInsightHiveJob](Invoke-AzHDInsightHiveJob.md)
Отправляет запрос на куст в кластер HDInsight и извлекает результаты запроса в одной операции.

### [New-AzHDInsightCluster](New-AzHDInsightCluster.md)
Создает кластер HDInsight Azure в указанной группе ресурсов для текущей подписки.

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

### [Remove-AzHDInsightPersistedScriptAction](Remove-AzHDInsightPersistedScriptAction.md)
Удаляет сохраненное действие сценария из кластера HDInsight.

### [REVOKE-AzHDInsightHttpServicesAccess](Revoke-AzHDInsightHttpServicesAccess.md)
Отключает доступ к кластеру через HTTP.

### [REVOKE-AzHDInsightRdpServicesAccess](Revoke-AzHDInsightRdpServicesAccess.md)
Запрещает RDP-доступ к кластеру Windows.

### [Set-AzHDInsightClusterSize](Set-AzHDInsightClusterSize.md)
Задает количество рабочих узлов в указанном кластере.

### [Set-AzHDInsightDefaultStorage](Set-AzHDInsightDefaultStorage.md)
Задает параметр учетной записи хранения по умолчанию в объекте конфигурации кластера.

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

