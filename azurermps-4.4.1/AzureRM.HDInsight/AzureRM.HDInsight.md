---
Module Name: AzureRM.HDInsight
Module Guid: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
Download Help Link:
  object Object: 
Help Version:
  object Object: 
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/AzureRM.HDInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/AzureRM.HDInsight.md
ms.openlocfilehash: fba8b9d96666a3a7d625e8f2af7274a6c086f94d
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "93555052"
---
# Модуль AzureRM. HDInsight
## Nописание
В этом разделе приведены командлеты Azure PowerShell для Microsoft Azure HDInsight в платформе диспетчера ресурсов Azure (ARM). Эти командлеты используются для управления кластерами HDInsight и заданиями, которые выполняются на них. Командлеты существуют в пространстве имен Microsoft. Azure. Commands. HDInsight.

## Командлеты AzureRM. HDInsight
### [Add-AzureRmHDInsightClusterIdentity](Add-AzureRmHDInsightClusterIdentity.md)
Добавляет удостоверение кластера в объект конфигурации кластера.

### [Add-AzureRmHDInsightComponentVersion](Add-AzureRmHDInsightComponentVersion.md)
Добавляет версию службы, работающей на кластере, в объект конфигурации кластера.

### [Add-AzureRmHDInsightConfigValues](Add-AzureRmHDInsightConfigValues.md)
Добавляет настройку значения конфигурации Hadoop и (или) общей библиотеки куста в объект конфигурации кластера.

### [Add-AzureRmHDInsightMetastore](Add-AzureRmHDInsightMetastore.md)
Добавляет базу данных SQL, которая будет служить кустом или Oozie MetaStore объекту конфигурации кластера.

### [Add-AzureRmHDInsightScriptAction](Add-AzureRmHDInsightScriptAction.md)
Добавляет действие сценария в объект конфигурации кластера.

### [Add-AzureRmHDInsightSecurityProfile](Add-AzureRmHDInsightSecurityProfile.md)
Добавляет profileto безопасности объекта конфигурации кластера.

### [Add-AzureRmHDInsightStorage](Add-AzureRmHDInsightStorage.md)
Добавляет ключ хранилища Azure к объекту конфигурации кластера.

### [Get-AzureRmHDInsightCluster](Get-AzureRmHDInsightCluster.md)
Возвращает и перечисляет все кластеры HDInsight Azure, связанные с текущей подпиской или указанной группой ресурсов, или извлекает определенный кластер.

### [Get-AzureRmHDInsightJob](Get-AzureRmHDInsightJob.md)
Получает список заданий из кластера и перечисляет их в обратном хронологическом порядке или извлекает конкретное задание.

### [Get-AzureRmHDInsightJobOutput](Get-AzureRmHDInsightJobOutput.md)
Получает выходные данные журнала для задания из учетной записи хранения, связанной с указанным кластером.

### [Get-AzureRmHDInsightPersistedScriptAction](Get-AzureRmHDInsightPersistedScriptAction.md)
Получает хранимые действия сценария для кластера и перечисляет их в хронологическом порядке или получает сведения о указанном сохраненном действии сценария.

### [Get-AzureRmHDInsightProperties](Get-AzureRmHDInsightProperties.md)
Получение свойств службы HDInsight, например доступных местоположений и емкости.

### [Get-AzureRmHDInsightScriptActionHistory](Get-AzureRmHDInsightScriptActionHistory.md)
Получает журнал действий сценария для кластера и перечисляет его в обратном хронологическом порядке или получает сведения о ранее выполненном действии сценария.

### [Grant-AzureRmHDInsightHttpServicesAccess](Grant-AzureRmHDInsightHttpServicesAccess.md)
Предоставление доступа к кластеру через HTTP.

### [Grant-AzureRmHDInsightRdpServicesAccess](Grant-AzureRmHDInsightRdpServicesAccess.md)
Предоставление доступа к кластеру Windows для подключения к удаленному рабочему столу.

### [Invoke-AzureRmHDInsightHiveJob](Invoke-AzureRmHDInsightHiveJob.md)
Отправляет запрос на куст в кластер HDInsight и извлекает результаты запроса в одной операции.

### [New-AzureRmHDInsightCluster](New-AzureRmHDInsightCluster.md)
Создает кластер HDInsight Azure в указанной группе ресурсов для текущей подписки.

### [New-AzureRmHDInsightClusterConfig](New-AzureRmHDInsightClusterConfig.md)
Создает несохраняемый объект конфигурации кластера, описывающий конфигурацию кластера Azure HDInsight.

### [New-AzureRmHDInsightHiveJobDefinition](New-AzureRmHDInsightHiveJobDefinition.md)
Создание объекта задания куста.

### [New-AzureRmHDInsightMapReduceJobDefinition](New-AzureRmHDInsightMapReduceJobDefinition.md)
Создает объект задания MapReduce.

### [New-AzureRmHDInsightPigJobDefinition](New-AzureRmHDInsightPigJobDefinition.md)
Создает объект задания свинья.

### [New-AzureRmHDInsightSqoopJobDefinition](New-AzureRmHDInsightSqoopJobDefinition.md)
Создает объект задания Sqoop.

### [New-AzureRmHDInsightStreamingMapReduceJobDefinition](New-AzureRmHDInsightStreamingMapReduceJobDefinition.md)
Создает потоковый объект задания MapReduce.

### [Remove-AzureRmHDInsightCluster](Remove-AzureRmHDInsightCluster.md)
Удаляет указанный кластер HDInsight из текущей подписки.

### [Remove-AzureRmHDInsightPersistedScriptAction](Remove-AzureRmHDInsightPersistedScriptAction.md)
Удаляет сохраненное действие сценария из кластера HDInsight.

### [REVOKE-AzureRmHDInsightHttpServicesAccess](Revoke-AzureRmHDInsightHttpServicesAccess.md)
Отключает доступ к кластеру через HTTP.

### [REVOKE-AzureRmHDInsightRdpServicesAccess](Revoke-AzureRmHDInsightRdpServicesAccess.md)
Запрещает RDP-доступ к кластеру Windows.

### [Set-AzureRmHDInsightClusterSize](Set-AzureRmHDInsightClusterSize.md)
Задает количество рабочих узлов в указанном кластере.

### [Set-AzureRmHDInsightDefaultStorage](Set-AzureRmHDInsightDefaultStorage.md)
Задает параметр учетной записи хранения по умолчанию в объекте конфигурации кластера.

### [Set-AzureRmHDInsightPersistedScriptAction](Set-AzureRmHDInsightPersistedScriptAction.md)
Задает ранее выполненное действие сценария, которое должно быть сохраненным сценарием.

### [Start-AzureRmHDInsightJob](Start-AzureRmHDInsightJob.md)
Запускает определенное задание Azure HDInsight в указанном кластере.

### [Остановить-AzureRmHDInsightJob](Stop-AzureRmHDInsightJob.md)
Останавливает указанное запущенное задание в кластере.

### [Submit-AzureRmHDInsightScriptAction](Submit-AzureRmHDInsightScriptAction.md)
Отправка нового действия сценария в кластер HDInsight Azure.

### [Use-AzureRmHDInsightCluster](Use-AzureRmHDInsightCluster.md)
Выбор кластера для использования с командлетом Invoke-RmAzureHDInsightHiveJob.

### [Wait-AzureRmHDInsightJob](Wait-AzureRmHDInsightJob.md)
Ожидание завершения или сбоя указанного задания.

