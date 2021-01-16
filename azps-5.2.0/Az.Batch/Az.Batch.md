---
Module Name: Az.Batch
Module Guid: a8f00f40-1c1a-49b5-9db3-24076b75c3cf
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.batch
Help Version: 4.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Az.Batch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Az.Batch.md
ms.openlocfilehash: f6bd55502c5c800bff245b905bc5334b1bf35bdb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396444"
---
# Az.Batch Module
## Описание
Командлеты Azure Batch в модуле Azure позволяют управлять пакетными службами Microsoft Azure в Azure PowerShell.

## Az.Batch cmdlets
### [Disable-AzBatchAutoScale](Disable-AzBatchAutoScale.md)
Отключает автоматическое масштабирование пула.

### [Disable-AzBatchComputeNodeScheduling](Disable-AzBatchComputeNodeScheduling.md)
Отключает планирование задач для указанного узла вычислений.

### [Disable-AzBatchJob](Disable-AzBatchJob.md)
Отключает пакетное задание.

### [Disable-AzBatchJobSchedule](Disable-AzBatchJobSchedule.md)
Отключает расписание пакетных рабочих мест.

### [Enable-AzBatchAutoScale](Enable-AzBatchAutoScale.md)
Включает автоматическое масштабирование пула.

### [Enable-AzBatchComputeNodeScheduling](Enable-AzBatchComputeNodeScheduling.md)
Включает планирование задач для указанного узла вычислений.

### [Enable-AzBatchJob](Enable-AzBatchJob.md)
Включает пакетное задание.

### [Enable-AzBatchJobSchedule](Enable-AzBatchJobSchedule.md)
Включает расписание пакетных рабочих мест.

### [Enable-AzBatchTask](Enable-AzBatchTask.md)
Повторно активирует задачу.

### [Get-AzBatchAccount](Get-AzBatchAccount.md)
Пакетная учетная запись в текущей подписке.

### [Get-AzBatchAccountKey](Get-AzBatchAccountKey.md)
Ключи для пакетной учетной записи.

### [Get-AzBatchApplication](Get-AzBatchApplication.md)
Получает сведения об указанном приложении.

### [Get-AzBatchApplicationPackage](Get-AzBatchApplicationPackage.md)
Сведения о пакете приложения в пакетной учетной записи.

### [Get-AzBatchCertificate](Get-AzBatchCertificate.md)
Получает сертификаты в пакетной учетной записи.

### [Get-AzBatchComputeNode](Get-AzBatchComputeNode.md)
Получает узлы пакетных вычислений из пула.

### [Get-AzBatchJob](Get-AzBatchJob.md)
Пакетные задания для пакетной учетной записи или расписания заданий.

### [Get-AzBatchJobPreparationAndReleaseTaskStatus](Get-AzBatchJobPreparationAndReleaseTaskStatus.md)
Пакетная подготовка задания и освобождение состояния задачи.

### [Get-AzBatchJobSchedule](Get-AzBatchJobSchedule.md)
Получает расписание пакетных рабочих мест.

### [Get-AzBatchJobStatistic](Get-AzBatchJobStatistic.md)
Получает сводную статистику по заданиям для учетной записи с пакетом.

### [Get-AzBatchLocationQuota](Get-AzBatchLocationQuota.md)
Получает квоты пакетных служб для подписки в заданное расположение.

### [Get-AzBatchNodeFile](Get-AzBatchNodeFile.md)
Свойства пакетных файлов узлов.

### [Get-AzBatchNodeFileContent](Get-AzBatchNodeFileContent.md)
Получает пакетный файл узла.

### [Get-AzBatchPool](Get-AzBatchPool.md)
Получает пакетные пулы в указанной учетной записи пакета.

### [Get-AzBatchPoolNodeCount](Get-AzBatchPoolNodeCount.md)
Получает количество пакетных узлов для каждого состояния узла, сгруппировали по id пула.

### [Get-AzBatchPoolStatistic](Get-AzBatchPoolStatistic.md)
Получает сводную статистику пула для пакетной учетной записи.

### [Get-AzBatchPoolUsageMetric](Get-AzBatchPoolUsageMetric.md)
Возвращает показатели использования пула для пакетной учетной записи.

### [Get-AzBatchRemoteDesktopProtocolFile](Get-AzBatchRemoteDesktopProtocolFile.md)
Получает RDP-файл из узла для вычислений.

### [Get-AzBatchRemoteLoginSetting](Get-AzBatchRemoteLoginSetting.md)
Возвращает параметры удаленного логона для узла компьютеров.

### [Get-AzBatchSubtask](Get-AzBatchSubtask.md)
Возвращает сведения о подзадаче для указанной задачи.

### [Get-AzBatchSupportedImage](Get-AzBatchSupportedImage.md)
Получает поддерживаемые пакетом изображения для учетной записи пакета.

### [Get-AzBatchTask](Get-AzBatchTask.md)
Получает пакетные задачи для задания.

### [Get-AzBatchTaskCount](Get-AzBatchTaskCount.md)
Возвращает количество задач для указанного задания.

### [New-AzBatchAccount](New-AzBatchAccount.md)
Создается пакетная учетная запись.

### [New-AzBatchAccountKey](New-AzBatchAccountKey.md)
Повторное сгенерирует ключ учетной записи пакета.

### [New-AzBatchApplication](New-AzBatchApplication.md)
Добавляет приложение в указанную учетную запись пакета.

### [New-AzBatchApplicationPackage](New-AzBatchApplicationPackage.md)
Создает пакет приложения в пакетной учетной записи.

### [New-AzBatchCertificate](New-AzBatchCertificate.md)
Добавляет сертификат в указанную учетную запись пакета.

### [New-AzBatchComputeNodeUser](New-AzBatchComputeNodeUser.md)
Создает учетную запись пользователя на узле пакетных вычислений.

### [New-AzBatchJob](New-AzBatchJob.md)
Создает задание в службе обработки пакетов.

### [New-AzBatchJobSchedule](New-AzBatchJobSchedule.md)
Создает расписание задания в пакетной службе.

### [New-AzBatchPool](New-AzBatchPool.md)
Создает пул в пакетной службе.

### [New-AzBatchResourceFile](New-AzBatchResourceFile.md)
Создает файл ресурса для использования `New-AzBatchTask` по.

### [New-AzBatchTask](New-AzBatchTask.md)
Создает пакетную задачу для задания.

### [Remove-AzBatchAccount](Remove-AzBatchAccount.md)
Удаляет учетную запись пакета.

### [Remove-AzBatchApplication](Remove-AzBatchApplication.md)
Удаляет приложение из учетной записи пакета.

### [Remove-AzBatchApplicationPackage](Remove-AzBatchApplicationPackage.md)
Удаляет запись пакета приложения и двоичный файл.

### [Remove-AzBatchCertificate](Remove-AzBatchCertificate.md)
Удаляет сертификат из учетной записи.

### [Remove-AzBatchComputeNode](Remove-AzBatchComputeNode.md)
Удаляет вычислительные узлы из пула.

### [Remove-AzBatchComputeNodeUser](Remove-AzBatchComputeNodeUser.md)
Удаляет учетную запись пользователя из узла пакетных вычислений.

### [Remove-AzBatchJob](Remove-AzBatchJob.md)
Удаляет задание пакета.

### [Remove-AzBatchJobSchedule](Remove-AzBatchJobSchedule.md)
Удаляет расписание пакетных рабочих мест.

### [Remove-AzBatchNodeFile](Remove-AzBatchNodeFile.md)
Удаляет файл узла для узла задачи или узла вычислений.

### [Remove-AzBatchPool](Remove-AzBatchPool.md)
Удаляет указанный пакетный пул.

### [Remove-AzBatchTask](Remove-AzBatchTask.md)
Удаляет пакетную задачу.

### [Reset-AzBatchComputeNode](Reset-AzBatchComputeNode.md)
Переустановка операционной системы на указанном узле вычислений.

### [Restart-AzBatchComputeNode](Restart-AzBatchComputeNode.md)
Перезагружает указанный узел вычислений.

### [Set-AzBatchAccount](Set-AzBatchAccount.md)
Обновляет учетную запись пакета.

### [Set-AzBatchApplication](Set-AzBatchApplication.md)
Обновляет параметры указанного приложения.

### [Set-AzBatchComputeNodeUser](Set-AzBatchComputeNodeUser.md)
Изменяет свойства учетной записи на узле пакетных вычислений.

### [Set-AzBatchJob](Set-AzBatchJob.md)
Обновляет задание пакета.

### [Set-AzBatchJobSchedule](Set-AzBatchJobSchedule.md)
Задает расписание задания.

### [Set-AzBatchPool](Set-AzBatchPool.md)
Обновляет свойства пула.

### [Set-AzBatchTask](Set-AzBatchTask.md)
Обновляет свойства задачи.

### [Start-AzBatchComputeNodeServiceLogUpload](Start-AzBatchComputeNodeServiceLogUpload.md)
Отправка файлов журнала журнала службы вычислений в контейнер хранилища Azure.

### [Start-AzBatchPoolResize](Start-AzBatchPoolResize.md)
Начинается с того, чтобы перенаблить пул.

### [Stop-AzBatchCertificateDeletion](Stop-AzBatchCertificateDeletion.md)
Отмена сбойного удаления сертификата.

### [Stop-AzBatchJob](Stop-AzBatchJob.md)
Остановка пакетного задания.

### [Stop-AzBatchJobSchedule](Stop-AzBatchJobSchedule.md)
Остановка графика пакетных задания.

### [Stop-AzBatchPoolResize](Stop-AzBatchPoolResize.md)
Останавливает операцию по окнам пула.

### [Stop-AzBatchTask](Stop-AzBatchTask.md)
Остановка пакетной задачи.

### [Test-AzBatchAutoScale](Test-AzBatchAutoScale.md)
Возвращает результат автоматической формулы масштабирования в пуле.

