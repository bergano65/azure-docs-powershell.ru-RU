---
Module Name: AzureRM.Insights
Module Guid: 698c387c-bd6b-41c6-82ce-721f1ef39548
Download Help Link:
  object Object: 
Help Version:
  object Object: 
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/AzureRM.Insights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/AzureRM.Insights.md
ms.openlocfilehash: d4f7819a3ddbf49f4a3c4ed56cd8273b1f2e1848
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "93555048"
---
# Модуль AzureRM. Insights
## Nописание
В этом разделе отображаются разделы справки по командлетам Azure Insights.

## Командлеты AzureRM. Insights
### [Add-AzureRmAutoscaleSetting](Add-AzureRmAutoscaleSetting.md)
Создание параметра автомасштабирования.

### [Add-AzureRmLogAlertRule](Add-AzureRmLogAlertRule.md)
Добавляет или заменяет правило оповещения в журнале.

### [Add-AzureRmLogProfile](Add-AzureRmLogProfile.md)
Создание нового профиля журнала активности. Этот профиль используется для архивации журнала активности в учетную запись хранения Azure или потоковой передачи в центр событий Azure в той же подписке. 

- **Учетная** запись хранилища (учетная запись хранилища Premium не поддерживается) поддерживается только для стандартной учетной записи хранения. Возможно, он либо имеет тип ARM, либо классический. Если он зарегистрирован в учетной записи хранения, стоимость хранения журнала активности оплачивается по обычным стандартным тарифам на хранение. На каждую подписку может быть одновременно задан только один профиль, но для экспорта журнала активности можно использовать только одну учетную запись хранения на подписку. 

- **Центр событий** — для экспорта журнала активности может использоваться только один центр событий на каждую подписку. Если журнал активности является потоком для концентратора событий, применяются стандартные цены центра событий. 

В журнале активности события могут относиться к региону или быть "глобальным". Глобально, это означает, что эти события не зависят от региона и не зависят от региона, в большинстве событий — в эту категорию. Если профиль журнала активности задан на портале, он неявно добавляет "Global" вместе с любым другим регионом, выбранным в пользовательском интерфейсе. При использовании командлета расположение как "Global" должно быть явно упомянуто отдельно от любого другого региона. 

**Примечание** . Если **вы не можете установить "Global" в указанных ниже областях, это приведет к тому, что журнал активности не будет экспортирован.** 

### [Add-AzureRmMetricAlertRule](Add-AzureRmMetricAlertRule.md)
Добавляет или обновляет правило оповещения на основе метрики.

### [Add-AzureRmWebtestAlertRule](Add-AzureRmWebtestAlertRule.md)
Добавляет или обновляет правило оповещения для веб-теста.

### [Disable-AzureRmActivityLogAlert](Disable-AzureRmActivityLogAlert.md)
Отключает оповещение журнала активности и задает его Теги.

### [Enable-AzureRmActivityLogAlert](Enable-AzureRmActivityLogAlert.md)
Включает предупреждение журнала активности и задает его Теги.

### [Get-AzureRmActionGroup](Get-AzureRmActionGroup.md)
Получает группу действий.

### [Get-AzureRmActivityLogAlert](Get-AzureRmActivityLogAlert.md)
Получает один или несколько ресурсов для оповещения журнала активности.

### [Get-AzureRmAlertHistory](Get-AzureRmAlertHistory.md)
Получает историю оповещений.

### [Get-AzureRmAlertRule](Get-AzureRmAlertRule.md)
Возвращает правила оповещения.

### [Get-AzureRmAutoscaleHistory](Get-AzureRmAutoscaleHistory.md)
Получает журнал автомасштабирования.

### [Get-AzureRmAutoscaleSetting](Get-AzureRmAutoscaleSetting.md)
Получает параметры автомасштабирования.

### [Get-AzureRmDiagnosticSetting](Get-AzureRmDiagnosticSetting.md)
Получает записанные в журнал временные Гранки и категории.

### [Get-AzureRmLog](Get-AzureRmLog.md)
Возвращает журнал событий.

### [Get-AzureRmLogProfile](Get-AzureRmLogProfile.md)
Получает профиль журнала.

### [Get-AzureRmMetric](Get-AzureRmMetric.md)
Возвращает значения метрик ресурса.

### [Get-AzureRmMetricDefinition](Get-AzureRmMetricDefinition.md)
Получение определений метрик.

### [Get-AzureRmUsage](Get-AzureRmUsage.md)
Получает метрики использования для ресурса.

### [New-AzureRmActionGroup](New-AzureRmActionGroup.md)
Создает объект ссылки на ActionGroup в памяти.

### [New-AzureRmActionGroupReceiver](New-AzureRmActionGroupReceiver.md)
Создает нового приемника группы действий.

### [New-AzureRmActivityLogAlertCondition](New-AzureRmActivityLogAlertCondition.md)
Создает новый объект условия предупреждения журнала активности в памяти.

### [New-AzureRmAlertRuleEmail](New-AzureRmAlertRuleEmail.md)
Создание действия электронной почты для правила оповещения.

### [New-AzureRmAlertRuleWebhook](New-AzureRmAlertRuleWebhook.md)
Создание веб-перехватчика правила оповещения.

### [New-AzureRmAutoscaleNotification](New-AzureRmAutoscaleNotification.md)
Создает уведомление об автомасштабировании электронной почты.

### [New-AzureRmAutoscaleProfile](New-AzureRmAutoscaleProfile.md)
Создание профиля автомасштабирования.

### [New-AzureRmAutoscaleRule](New-AzureRmAutoscaleRule.md)
Создает правило автомасштабирования.

### [New-AzureRmAutoscaleWebhook](New-AzureRmAutoscaleWebhook.md)
Создание веб-перехватчика автомасштабирования.

### [Remove-AzureRmActionGroup](Remove-AzureRmActionGroup.md)
Удаление группы действий.

### [Remove-AzureRmActivityLogAlert](Remove-AzureRmActivityLogAlert.md)
Удаляет оповещение журнала активности.

### [Remove-AzureRmAlertRule](Remove-AzureRmAlertRule.md)
Удаление правила оповещения.

### [Remove-AzureRmAutoscaleSetting](Remove-AzureRmAutoscaleSetting.md)
Удаление параметра автомасштабирования.

### [Remove-AzureRmLogProfile](Remove-AzureRmLogProfile.md)
Удаление профиля журнала.

### [Set-AzureRmActionGroup](Set-AzureRmActionGroup.md)
Создает новую или обновляет существующую группу действий.

### [Set-AzureRmActivityLogAlert](Set-AzureRmActivityLogAlert.md)
Создание нового или установка существующего оповещения журнала активности.

### [Set-AzureRmDiagnosticSetting](Set-AzureRmDiagnosticSetting.md)
Задает параметры журналов и метрик для ресурса.

