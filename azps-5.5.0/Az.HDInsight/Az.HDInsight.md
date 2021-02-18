---
Module Name: Az.HDInsight
Module Guid: 3fd1475f-cb23-4ffb-bf08-33d94b7d1acb
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight
Help Version: 4.1.2.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
ms.openlocfilehash: e3c3bb9d4d8225823ec84750c8292288ce25c15b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241437"
---
# Модуль Az.HDInsight
## Описание
В разделах этой статьи ются командылеты Azure PowerShell для Microsoft Azure HDInsight в структуре Диспетчера ресурсов Azure (ARM). Эти cmdlets используются для управления кластерами HDInsight и заданиями, которые работают на них. Командлеты существуют в области имен Microsoft.Azure.Commands.HDInsight.

## Az.HDInsight Cmdlets
### [Add-AzHDInsightClusterIdentity](Add-AzHDInsightClusterIdentity.md)
Добавляет удостоверение кластера к объекту конфигурации кластера.

### [Add-AzHDInsightComponentVersion](Add-AzHDInsightComponentVersion.md)
Добавляет версию службы, запущенной в кластере, в объект конфигурации кластера.

### [Add-AzHDInsightConfigValue](Add-AzHDInsightConfigValue.md)
Добавляет настройку значения конфигурации Hadoop или общей библиотеки "Раздел" в объект конфигурации кластера.

### [Add-AzHDInsightMetastore](Add-AzHDInsightMetastore.md)
Добавляет базу SQL, которая будет служить в качестве метахранилища Oozie или Оози, в объект конфигурации кластера.

### [Add-AzhdInsightScriptaction](Add-AzHDInsightScriptAction.md)
Добавляет действие сценария к объекту конфигурации кластера.

### [Add-AzhDInsightSecurityProfile](Add-AzHDInsightSecurityProfile.md)
Добавляет профиль безопасности в объект конфигурации кластера.

### [Add-AzHDInsightStorage](Add-AzHDInsightStorage.md)
Добавляет ключ хранилища Azure к объекту конфигурации кластера.

### [Disable-AzHDInsightMonitoring](Disable-AzHDInsightMonitoring.md)
Отключение мониторинга в кластере HDInsight, и соответствующие журналы перестанут поступать в рабочее пространство мониторинга, указанное во время его включения.

### [Enable-AzHDInsightMonitoring](Enable-AzHDInsightMonitoring.md)
Включает мониторинг в кластере HDInsight, а соответствующие журналы отправляются в рабочее пространство мониторинга, заданное во время его работы.

### [Get-AzHDInsightCluster](Get-AzHDInsightCluster.md)
Возвращает и перечисляет все кластеры Azure HDInsight, связанные с текущей подпиской или определенной группой ресурсов, либо извлекает определенный кластер.

### [Get-AzHDInsightClusterAutoscaleConfiguration](Get-AzHDInsightClusterAutoscaleConfiguration.md)
Получает настройку автоматической настройки кластера HDInsight.

### [Get-AzHDInsightHost](Get-AzHDInsightHost.md)
Список хостов кластера HDInsight.

### [Get-AzHDInsightJob](Get-AzHDInsightJob.md)
Возвращает список заданий из кластера и перечислены в обратном хронологическом порядке или получают определенное задание.

### [Get-AzHDInsightJobOutput](Get-AzHDInsightJobOutput.md)
Возвращает результаты журнала для задания из учетной записи хранения, связанной с указанным кластером.

### [Get-AzHDInsightMonitoring](Get-AzHDInsightMonitoring.md)
Состояние мониторинга установки на кластере.

### [Get-AzHDInsightPersistedScriptAction](Get-AzHDInsightPersistedScriptAction.md)
Возвращает неупорядоченные действия сценариев для кластера и перечисляет их в хронологическом порядке или получает сведения об указанном действии сохраняемого сценария.

### [Get-AzHDInsightProperty](Get-AzHDInsightProperty.md)
Свойства службы HDInsight, например доступные расположения и емкость.

### [Get-AzhdInsightScriptactionHistory](Get-AzHDInsightScriptActionHistory.md)
Получает историю действий сценария для кластера и перечисляет его в обратном хронологическом порядке или получает сведения о ранее выполненном действии сценария.

### [Invoke-AzHDInsightHiveJob](Invoke-AzHDInsightHiveJob.md)
Отправка запроса на вирус в кластер HDInsight и извлечение результатов запроса за одну операцию.

### [New-AzHDInsightCluster](New-AzHDInsightCluster.md)
Создает кластер Azure HDInsight в указанной группе ресурсов для текущей подписки.

### [New-AzHDInsightClusterAutoscaleConfiguration](New-AzHDInsightClusterAutoscaleConfiguration.md)
Создает объект, который не сохраняется, описывая конфигурацию автоматической настройки кластера Azure HDInsight.

### [New-AzHDInsightClusterAutoscaleScheduleCondition](New-AzHDInsightClusterAutoscaleScheduleCondition.md)
Создание условия автоматической шкалы на основе календарного плана.

### [New-AzHDInsightClusterConfig](New-AzHDInsightClusterConfig.md)
Создает объект конфигурации кластера, который не сохраняется и описывает конфигурацию кластера Azure HDInsight.

### [New-AzHDInsightHiveJobDefinition](New-AzHDInsightHiveJobDefinition.md)
Создает объект задания "Вирус".

### [New-AzHDInsightMapReduceJobDefinition](New-AzHDInsightMapReduceJobDefinition.md)
Создание объекта задания MapReduce.

### [New-AzHDInsightPigJobDefinition](New-AzHDInsightPigJobDefinition.md)
Создает объект задания Pig.

### [New-AzHDInsightSqoopJobDefinition](New-AzHDInsightSqoopJobDefinition.md)
Создание объекта задания Sqoop.

### [New-AzHDInsightStreamingMapReduceJobDefinition](New-AzHDInsightStreamingMapReduceJobDefinition.md)
Создает объект задания Streaming MapReduce.

### [Remove-AzHDInsightCluster](Remove-AzHDInsightCluster.md)
Удаляет указанный кластер HDInsight из текущей подписки.

### [Remove-AzHDInsightClusterAutoscaleConfiguration](Remove-AzHDInsightClusterAutoscaleConfiguration.md)
Удаляет настройку автоматических шкал кластера HDInsight.

### [Remove-AzHDInsightPersistedScriptAction](Remove-AzHDInsightPersistedScriptAction.md)
Удаляет неуохраняемую действие сценария из кластера HDInsight.

### [Restart-AzhdInsightHost](Restart-AzHDInsightHost.md)
Перезапуск конкретных хостов кластера HDInsight.

### [Set-AzHDInsightClusterAutoscaleConfiguration](Set-AzHDInsightClusterAutoscaleConfiguration.md)
Настраивает автоматическую настройку кластера Azure HDInsight.

### [Set-AzHDInsightClusterDiskEncryptionKey](Set-AzHDInsightClusterDiskEncryptionKey.md)
Поворот ключа шифрования диска для указанного кластера HDInsight.

### [Set-AzhdInsightClusterSize](Set-AzHDInsightClusterSize.md)
Задает количество узлов рабочих в указанном кластере.

### [Set-AzHDInsightDefaultStorage](Set-AzHDInsightDefaultStorage.md)
Задает учетную запись хранения по умолчанию в объекте конфигурации кластера.

### [Set-AzHDInsightGatewayCredential](Set-AzHDInsightGatewayCredential.md)
Задает учетные данные шлюза HTTP в кластере Azure HDInsight.

### [Set-AzHDInsightPersistedScriptAction](Set-AzHDInsightPersistedScriptAction.md)
Для ранее выполненного действия сценария устанавливается его сохраняемая возможность.

### [Start-AzHDInsightJob](Start-AzHDInsightJob.md)
Запускает задание Azure HDInsight в заданном кластере.

### [Stop-AzHDInsightJob](Stop-AzHDInsightJob.md)
Остановка заданного задания в кластере.

### [Submit-AzhdInsightScriptaction](Submit-AzHDInsightScriptAction.md)
Отправка нового действия сценария в кластер Azure HDInsight.

### [Use-AzHDInsightCluster](Use-AzHDInsightCluster.md)
Выбирает кластер, который будет использоваться с Invoke-RmAzureHDInsightHiveJob..

### [Wait-AzHDInsightJob](Wait-AzHDInsightJob.md)
Ожидание завершения или сбоя определенного задания.

