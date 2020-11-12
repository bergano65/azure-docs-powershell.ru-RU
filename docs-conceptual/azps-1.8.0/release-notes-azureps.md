---
title: Заметки о выпуске Azure PowerShell
description: Узнайте обо всех последних обновлениях модулей Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/30/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 7d468fb760f9be23e8b8eea7f74adc1dd137e469
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2020
ms.locfileid: "93408332"
---
# <a name="azure-powershell-release-notes"></a>Заметки о выпуске Azure PowerShell
## <a name="180---april-2019"></a>1.8.0 — апрель 2019 г.
### <a name="highlights-since-the-last-major-release"></a>Основные возможности с момента последнего основного выпуска
* Общедоступная версия модуля `Az`.
* Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce
* Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/
* Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.
* Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.
* Добавлена поддержка для модулей runbook Python 2 в Az.Automation.
* Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:

#### <a name="azaccounts"></a>Az.Accounts
* Обновлен командлет Uninstall-AzureRm для правильного удаления модулей в Mac.

#### <a name="azbatch"></a>Az.Batch
* Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.

#### <a name="azcdn"></a>Az.Cdn
* Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.

#### <a name="azcompute"></a>Az.Compute
* Устранена проблема с установкой AEM, если в идентификаторах ресурсов дисков группа ресурсов указана в нижнем регистре.
* Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.
* Исправлена документация по подстановочным знакам.

#### <a name="azdatafactory"></a>Az.DataFactory
* Добавлены свойства SsisProperties, если NodeCount не имеет значения NULL для управляемой среды выполнения интеграции.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.

#### <a name="azeventgrid"></a>Az.EventGrid
* Обновлен текст справки для конечной точки, указывающий, что необходимо создать ресурсы, прежде чем использовать командлеты для создания или обновления подписки на события.

#### <a name="azeventhub"></a>Az.EventHub
* Добавлены новые командлеты для NetworkRuleSet пространства имен.

#### <a name="azhdinsight"></a>Az.HDInsight
* Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.

#### <a name="aziothub"></a>Az.IotHub
* Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.

#### <a name="azkeyvault"></a>Az.KeyVault
* Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.
* Исправлена документация по подстановочным знакам.

#### <a name="azmachinelearning"></a>Az.MachineLearning
* Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.

#### <a name="azmedia"></a>Az.Media
* Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.

#### <a name="azmonitor"></a>Az.Monitor
  * Добавлены новые командлеты для правила генерации оповещений на основе метрик GenV2 (не классических).
      - New-AzMetricAlertRuleV2DimensionSelection
      - New-AzMetricAlertRuleV2Criteria
      - Remove-AzMetricAlertRuleV2
      - Get-AzMetricAlertRuleV2
      - Add-AzMetricAlertRuleV2
  * Обновлен пакет SDK Monitor до предварительной версии 0.22.0.

#### <a name="aznetwork"></a>Az.Network
* Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.
* Исправлена документация по подстановочным знакам.

#### <a name="aznotificationhubs"></a>Az.NotificationHubs
* Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.

#### <a name="azpowerbiembedded"></a>Az.PowerBIEmbedded
* Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.
* Обновлен табличный формат для SQL на виртуальной машине Azure.
* Добавлен альтернативный метод для получения расположения в Общей папке Azure.
* Обновлено значение ScheduleRunDays в объекте SchedulePolicy в соответствии с часовым поясом.

#### <a name="azrediscache"></a>Az.RedisCache
* Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.

#### <a name="azresources"></a>Az.Resources
* Исправлена документация по подстановочным знакам.

#### <a name="azsql"></a>Az.Sql
* Заменена зависимость от пакета SDK монитора на обычный код.
* Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.
* Улучшен процесс классификации нескольких столбцов.
* Добавлены свойства SKU (имя, семейство, производительность SKU) в отклике Get-AzSqlServerServiceObjective, а также по умолчанию задан табличный формат.
* C помощью Get-AzSqlServerServiceObjective теперь можно получать список доступных целевых служб по расположению без необходимости заранее размещать сервер в регионе.
* Поддерживается параметр часового пояса при создании Управляемого экземпляра.
* Исправлена документация по подстановочным знакам.

#### <a name="azwebsites"></a>Az.Websites
* Исправлены командлеты Set-AzWebApp и Set-AzWebAppSlot, которые теперь не удаляют теги при выполнении.
* Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.
* Обновлен пакет SDK веб-узлов.
* Удалено свойство AdminSiteName из PSAppServicePlan.

## <a name="170---april-2019"></a>1.7.0 —апрель 2019 г.
### <a name="highlights-since-the-last-major-release"></a>Основные возможности с момента последнего основного выпуска
* Общедоступная версия модуля `Az`.
* Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce
* Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/
* Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.
* Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.
* Добавлена поддержка для модулей runbook Python 2 в Az.Automation.
* Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:

#### <a name="azaccounts"></a>Az.Accounts
* Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметр AzureAnalysisServicesEndpointResourceId.

#### <a name="azanalysisservices"></a>Az.AnalysisServices
* Использование ServiceClient в командлетах плоскости данных и удаление исходной логики проверки подлинности.
* Add-AzureASAccount используется как оболочка для Connect-AzAccount во избежание критических изменений.

#### <a name="azautomation"></a>Az.Automation
* Исправлена ошибка командлета New-AzAutomationSoftwareUpdateConfiguration, связанная с включением. Теперь параметры IncludedKbNumber и IncludedPackageNameMask должны работать нормально.
* Исправлена ошибка динамической группы управления обновлениями службы автоматизации Azure.

#### <a name="azcompute"></a>Az.Compute
* В командлеты New-AzDiskConfig и New-AzSnapshotConfig добавлен параметр HyperVGeneration.
* Теперь можно создавать виртуальные машину на основе образов из коллекции от других клиентов.

#### <a name="azcontainerinstance"></a>Az.ContainerInstance
* Исправлена проблема в параметре -Command командлета New-AzContainerGroup, из-за которой в конце добавлялся пустой аргумент.

#### <a name="azdatafactory"></a>Az.DataFactory
* Пакет SDK для ADF .NET обновлен до версии 3.0.2.
* Командлет Set-AzDataFactoryV2 обновлен с помощью дополнительных параметров для настроек, связанных с RepoConfiguration.

#### <a name="azresources"></a>Az.Resources
* Улучшена обработка поставщиков Get-AzResource при предоставлении параметров -ResourceId или -ResourceGroupName, -Name и -ResourceType.
* Улучшена обработка ошибок в командлетах Test-AzDeployment и Test-AzResourceGroupDeployment.
    - Теперь ошибки, возникающие за пределами проверки развертывания, обрабатываются и включаются в выходные данные команды.
    - Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.
* Добавлен параметр-переключатель -IgnoreDynamicParameters, с помощью которого можно настроить командлеты развертывания так, чтобы они пропускали запросы в сценариях скриптов и заданий.
    - Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.

#### <a name="azsql"></a>Az.Sql
* Поддержка классификации данных в базе данных.

#### <a name="azstorage"></a>Az.Storage
* Подробные сообщения об ошибке передаются при создании контекста хранилища с помощью параметра -UseConnectedAccount, но без входа в учетную запись Azure.
    - New-AzStorageContext
* Поддержка свойств службы управления BLOB-объектов в указанной учетной записи хранения с помощью API плоскости управления.
    - Update-AzStorageBlobServiceProperty
    - Get-AzStorageBlobServiceProperty
    - Enable-AzStorageBlobDeleteRetentionPolicy
    - Disable-AzStorageBlobDeleteRetentionPolicy
* Поддержка параметра -AsJob в командлетах для отправки и скачивания больших двоичных объектов и файлов.
    - Get-AzStorageBlobContent
    - Set-AzStorageBlobContent
    - Get-AzStorageFileContent
    - Set-AzStorageFileContent

## <a name="160---march-2019"></a>1.6.0 — март 2019 г.
### <a name="highlights-since-the-last-major-release"></a>Основные возможности с момента последнего основного выпуска
* Общедоступная версия модуля `Az`.
* Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce
* Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/
* Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.
* Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.
* Добавлена поддержка для модулей runbook Python 2 в Az.Automation.
* Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:

#### <a name="azautomation"></a>Az.Automation
* В управление обновлениями службы автоматизации Azure внесены изменения для поддержки следующих новых функций:
    * динамическое группирование;
    * скрипты предварительного или последующего выполнения;
    * параметр перезагрузки.

#### <a name="azcompute"></a>Az.Compute
* Устранена проблема, связанная с разрешением пути в Get-AzVmBootDiagnosticsData.
* Обновление клиентской библиотеки вычислений до версии 25.0.0.

#### <a name="azkeyvault"></a>Az.KeyVault
* Добавлена поддержка подстановочных знаков в командлетах KeyVault.

#### <a name="aznetwork"></a>Az.Network
* Добавлена поддержка анализа угроз для Брандмауэра Azure.
* Добавлены настраиваемые правила и ресурс верхнего уровня для политики брандмауэра Шлюза приложений.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* В политику виртуальной машины Azure добавлен объект SnapshotRetentionInDays для поддержки мгновенного восстановления.
* Добавлена поддержка канала для отмены регистрации контейнера.

#### <a name="azresources"></a>Az.Resources
* Обновлена поддержка подстановочных знаков для Get-AzResource и Get-AzResourceGroup.
* Обновлены учетные данные, используемые при общих вызовах к ARM.

#### <a name="azsql"></a>Az.Sql
* Изменен тип параметра (ExcludeDetectionType) командлетов для обнаружения угроз с DetectionTypes на string[] для поддержки актуального состояния при добавлении новых типов обнаружения и для поддержки автозаполнения.

#### <a name="azstorage"></a>Az.Storage
* Поддержка получения, настройки и удаления политики управления в учетной записи хранения.
    - Set-AzStorageAccountManagementPolicy
    - Get-AzStorageAccountManagementPolicy
    - Remove-AzStorageAccountManagementPolicy
    - Add-AzStorageAccountManagementPolicyAction
    - New-AzStorageAccountManagementPolicyFilter
    - New-AzStorageAccountManagementPolicyRule

#### <a name="azwebsites"></a>Az.Websites
* Исправлена ошибка с шаблоном ARM, из-за которой прерывалось клонирование все слотов при использовании New-AzWebApp -IncludeSourceWebAppSlots.

## <a name="150---march-2019"></a>1.5.0 — март 2019 г.
#### <a name="azaccounts"></a>Az.Accounts
* Добавлена команда Register-AzModule для поддержки созданных командлетов AutoRest.
* Обновлены примеры для Connect AzAccount.

#### <a name="azautomation"></a>Az.Automation
* Исправлена проблема с получением некоторых ежемесячных расписаний в нескольких командлетах службы автоматизации Azure.
* Исправлен командлет Get-AzAutomationDscNode, возвращающий только первые 20 узлов. Теперь он возвращает все узлы.

#### <a name="azcdn"></a>Az.Cdn
* Добавлены новые командлеты PowerShell для включения и отключения HTTPS для личного домена и отключены устаревшие командлеты.

#### <a name="azcompute"></a>Az.Compute
* Добавлена поддержка подстановочных знаков в командлетах Get.

#### <a name="azdatafactory"></a>Az.DataFactory
* Обновлен пакет SDK для ADF .NET до версии 3.0.1.

#### <a name="azlogicapp"></a>Az.LogicApp
* Исправлена проблема с получением только первой страницы результатов при выполнении команды ListWorkflows.

#### <a name="aznetwork"></a>Az.Network
* Добавлена поддержка подстановочных знаков в командлетах Network.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Добавлена поддержка SQL Server на виртуальной машине Azure.
* Обновление пакета SDK
* Удалена проверка VMappContainer в Get-ProtectableItem.
* Добавлены параметры Name и ServerName для Get-ProtectableItem.

#### <a name="azresources"></a>Az.Resources
* Добавлен параметр `-TemplateObject` в командлеты для развертывания.
    - Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2933.
* Устранена проблема с передачей в конвейер результата `Get-AzResource` для `Set-AzResource`.
    - Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8240.
* Устранена проблема с изменением типа данных JSON при выполнении `Set-AzResource`.
    - Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7930.

#### <a name="azsql"></a>Az.Sql
* Обновление AuditingEndpointsCommunicator.
    - Исправлено поведение для пограничного случая при создании параметров диагностики.

#### <a name="azstorage"></a>Az.Storage
* Включена поддержка Kind BlockBlobStorage при создании учетной записи хранения для New-AzStorageAccount.

## <a name="140---february-2019"></a>1.4.0 — февраль 2019 г.
#### <a name="azanalysisservices"></a>Az.AnalysisServices
* Командлет AddAzureASAccount устарел.

#### <a name="azautomation"></a>Az.Automation
* Обновлена справка для командлета Import-AzAutomationDscNodeConfiguration.
* Добавлена проверка имени конфигурации для командлета Import-AzAutomationDscConfiguration.
* Улучшена обработка ошибок для командлета Import-AzAutomationDscConfiguration.

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Добавлен параметр CustomSubdomainName — новый необязательный параметр для командлета New-AzCognitiveServicesAccount, который указывает поддомен для ресурса.

#### <a name="azcompute"></a>Az.Compute
* Устранена проблема с идентификаторами наборов параметров.
* Обновлен командлет Get-AzVMExtension для отображения списка всех установленных расширений, если не указан параметр Name.
* Для командлета Update-AzImage добавлены параметры Tag и ResourceId.
* Командлет Get-AzVmssVM, который выполняется без указания идентификатора экземпляра и с параметром InstanceView, может выводить виртуальные машины из VMSS с представлением экземпляра.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Добавлены командлеты для перечисления и восстановления удаленного элемента ADL.

#### <a name="azeventhub"></a>Az.EventHub
* Добавлено новое логическое свойство SkipEmptyArchives для пропуска пустых архивов в классе CaptureDescription Eventhub.

#### <a name="azkeyvault"></a>Az.KeyVault
* Исправлена расстановка тегов для командлета Set-AzKeyVaultSecret.

#### <a name="azlogicapp"></a>Az.LogicApp
* Добавлен SKU "Базовый" для учетных записей интеграции.
* Добавлены типы сопоставлений Liquid, а также XSLT 2.0 и XSLT 3.0.
* Новые командлеты для сборок учетных записей интеграции:
    - Get-AzIntegrationAccountAssembly;
    - New-AzIntegrationAccountAssembly;
    - Remove-AzIntegrationAccountAssembly;
    - Set-AzIntegrationAccountAssembly.
* Новые командлеты для конфигурации пакета учетных записей интеграции:
    - Get-AzIntegrationAccountBatchConfiguration;
    - New-AzIntegrationAccountBatchConfiguration;
    - Remove-AzIntegrationAccountBatchConfiguration;
    - Set-AzIntegrationAccountBatchConfiguration.
* Обновлен пакет SDK Logic Apps до версии 4.1.0.

#### <a name="azmonitor"></a>Az.Monitor
* Обновлена справка для командлета Get-AzMetric.

#### <a name="aznetwork"></a>Az.Network
* Обновлен пример справки для командлета Add-AzApplicationGatewayCustomError.

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Дополнительная поддержка создания и получения источников данных ApplicationInsights.
    - Добавлен новый тип ApplicationInsights для получения определенных или всех источников данных ApplicationInsights для указанной рабочей области.
    - Добавлен командлет New-AzOperationalInsightsApplicationInsightsDataSource для создания источника данных с использованием параметров указанного ресурса Application-Insightss: subscription Id, resourceGroupName и name.

#### <a name="azresources"></a>Az.Resources
* исправлена проблема https://github.com/Azure/azure-powershell/issues/8166.
* исправлена проблема https://github.com/Azure/azure-powershell/issues/8235.
* исправлена проблема https://github.com/Azure/azure-powershell/issues/6219.
* Исправлена ошибка, препятствующая повторному созданию KeyCredentials.

#### <a name="azsql"></a>Az.Sql
* Добавлена поддержка уровня гипермасштабирования в базе данных SQL.
* Исправлена ошибка, из-за которой восстановление могло завершиться со сбоем при указании ненужных свойств в запросе на восстановление.

#### <a name="azwebsites"></a>Az.Websites
* Исправлен пример для командлета Get-AzWebAppSlotMetrics.

## <a name="130---february-2019"></a>1.3.0 — февраль 2019 г.
#### <a name="azaccounts"></a>Az.Accounts
* Обновление до последней версии ClientRuntime

#### <a name="azanalysisservices"></a>Az.AnalysisServices
Общедоступная версия модуля Az.AnalysisServices.

#### <a name="azcompute"></a>Az.Compute
* Расширение AEM: добавлена поддержка дисков UltraSSD, P60, P70 и P80.
* Обновлено описание справки для командлета Set-AzVMBootDiagnostics.
* Обновлено описание справки и пример для командлета Update-AzImage.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
Общедоступная версия модуля Az.RecoveryServices.

#### <a name="azresources"></a>Az.Resources
* Исправлена расстановка тегов для групп ресурсов.
    - Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8166.
* Исправлена проблема с игнорированием командлетом `Get-AzureRmRoleAssignment` параметра -ErrorAction.
    - Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8235.

#### <a name="azsql"></a>Az.Sql
* Добавлен командлет Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy.
* Исправлена проблема с появлением исключения NullRef при выполнении командлетов SQL, если не выполнен вход в учетную запись Azure.
* Исправлено исключение NullRef в командлете Get-AzSqlCapability.

## <a name="121---january-2019"></a>1.2.1 — январь 2019 г.
#### <a name="azaccounts"></a>Az.Accounts
* Выпуск с правильной версией службы аутентификации.

#### <a name="azanalysisservices"></a>Az.AnalysisServices
* Выпуск с обновленной зависимостью службы аутентификации.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Выпуск с обновленной зависимостью службы аутентификации.

## <a name="120---january-2019"></a>1.2.0 — январь 2019 г.
#### <a name="azaccounts"></a>Az.Accounts
* Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.
* Исправлены неправильные URL-адреса онлайн-справки.
* Добавлено предупреждающее сообщение в PS Core для модуля Uninstall-AzureRm.

#### <a name="azaks"></a>Az.Aks
* Исправлены неправильные URL-адреса онлайн-справки.

#### <a name="azautomation"></a>Az.Automation
* Добавлена поддержка для модулей runbook Python 2.
* Исправлены неправильные URL-адреса онлайн-справки.

#### <a name="azcdn"></a>Az.Cdn
* Исправлены неправильные URL-адреса онлайн-справки.

#### <a name="azcompute"></a>Az.Compute
* Добавлен командлет Invoke-AzVMReimage.
* Добавлен параметр TempDisk к командлету Set-AzVmss.
* Исправлено предупреждающее сообщение командлета New-AzVM.

#### <a name="azcontainerregistry"></a>Az.ContainerRegistry
* Исправлены неправильные URL-адреса онлайн-справки.

#### <a name="azdatafactory"></a>Az.DataFactory
* Пакет SDK ADF .Net обновлен до версии 3.0.0.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Исправлена проблема с конечной точкой ADLS при использовании MSI.
    - Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7462.
* Исправлены неправильные URL-адреса онлайн-справки.

#### <a name="aziothub"></a>Az.IotHub
* Добавлен формат кодирования для командлета Add-IotHubRoutingEndpoint.

#### <a name="azkeyvault"></a>Az.KeyVault
* Исправлены неправильные URL-адреса онлайн-справки.

#### <a name="aznetwork"></a>Az.Network
* Исправлены неправильные URL-адреса онлайн-справки.

#### <a name="azresources"></a>Az.Resources
* Исправлены неправильные примеры в справочной документации по командлетам New-AzADAppCredential и New-AzADSpCredential.
* Исправлена проблема, при которой путь для параметра -TemplateFile не удавалось разрешить до выполнения командлетов развертывания групп ресурсов.
* Az.Resources: исправлена документация для значения по умолчанию -Mode командлета New-AzureRmPolicyDefinition.
* Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/7522.
* Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/5747.
* Исправлена проблема с форматированием объекта PSResourceGroupDeployment.
    - Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2123.

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Исправлена проблема с появлением исключения в процессе отката при добавлении сертификата к модели VMSS: https://github.com/Azure/service-fabric-issues/issues/932.
* Исправлены некоторые сообщения об ошибках.
* Исправлена проблема с созданием кластера с шаблоном ARM по умолчанию для командлета New-AzServiceFabriCluster, который не работал с операцией миграции в Az.
* Исправлена проблема с добавлением сертификата кластера или приложения: теперь они добавляются только в Масштабируемые наборы виртуальных машин, которые сопоставлены с кластером, путем проверки идентификатора кластера в расширении.

#### <a name="azsignalr"></a>Az.SignalR
* Исправлены неправильные URL-адреса онлайн-справки.

#### <a name="azsql"></a>Az.Sql
* Исправлены неправильные URL-адреса онлайн-справки.
* Обновлено описание параметра LicenseType с добавлением возможных значений.
* Исправлена проблема с неправильным обновлением удостоверения управляемого экземпляра, если оно было единственным обновляемым свойством.
* Поддержка пользовательских параметров сортировки в управляемых экземплярах.

#### <a name="azstorage"></a>Az.Storage
* Исправлены неправильные URL-адреса онлайн-справки.
* Добавлен вывод подробных сообщений об ошибке при получении или установке классических свойств ведения журнала или метрик в учетной записи хранилища класса Premium, так как учетная запись хранилища класса Premium не поддерживает классические функции ведения журнала и метрик.
    - Get/Set-AzStorageServiceLoggingProperty
    - Get/Set-AzStorageServiceMetricsProperty

#### <a name="aztrafficmanager"></a>Az.TrafficManager
* Исправлены неправильные URL-адреса онлайн-справки.

#### <a name="azwebsites"></a>Az.Websites
* Исправлены неправильные URL-адреса онлайн-справки.
* Исправлена работа командлета New-AzWebAppSSLBinding: сертификат отправляется в правильную группу ресурсов и правильное расположение, если приложение размещено в ASE.
* Исправлена работа командлета New-AzWebAppSSLBinding: теги не перезаписываются при привязке SSL-сертификата к приложению.

## <a name="110---january-2019"></a>1.1.0 — январь 2019 г.
#### <a name="azaccounts"></a>Az.Accounts
* Добавление области "Local" в Enable-AzureRmAlias.

#### <a name="azcompute"></a>Az.Compute
* Теперь имя не является обязательным в идентификаторе набора параметров для Restart/Start/Stop/Remove/Set-AzVM и Save-AzVMImage.
* Обновлено описание идентификатора в файлах справки.
* Устранена проблема обратной совместимости с модулем Az.Accounts.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Обновление версии пакета SDK для плоскости данных до 1.1.14 для устранения найденных проблем.
    - Исправлена обработка отрицательного времени доступа и времени изменения для getfilestatus и liststatus, исправлен токен отмены для асинхронных методов.

#### <a name="azeventgrid"></a>Az.EventGrid
* Обновление для использования API версии 2019-01-01.
* Обновлены указанные ниже командлеты для поддержки нового сценария в API версии 2019-01-01.
    - New-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:
        - срока жизни события;
        - максимального числа попыток доставки для событий;
        - конечной точки недоставленных сообщений.
    - Update-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:
        - срока жизни события;
        - максимального числа попыток доставки для событий;
        - конечной точки недоставленных сообщений.
* Для параметра EndpointType добавлены новые значения перечисления (storageQueue и hybridConnection) в командлеты New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription.
* Если ожидается, что создание или обновление подписки на событие повлечет за собой действия со стороны пользователя, выполняемые вручную, отображается предупреждение при создании или обновлении подписки события.

#### <a name="aziothub"></a>Az.IotHub
* Пакет SDK Центра Интернета вещей обновлен до последней версии.

#### <a name="azlogicapp"></a>Az.LogicApp
* Get-AzLogicApp позволяет перечислить все параметры без указанного имени.

#### <a name="azresources"></a>Az.Resources
* Исправлена проблема с набором параметров при предоставлении параметров "-ODataQuery" и "-ResourceId" для "Get-AzResource".
    - Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7875.
* Исправлена обработка параметра -Custom в New/Set-AzPolicyDefinition.
* Исправлена опечатка в документации по New-AzDeployment.
* Параметр "-MailNickname" стал обязательным для "New-AzADUser".
    - Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8220.

#### <a name="azsignalr"></a>Az.SignalR
* Устранена проблема обратной совместимости с модулем Az.Accounts.

#### <a name="azsql"></a>Az.Sql
* Зависимость клиента управления хранением преобразована для общей реализации в пакете SDK.

#### <a name="azstorage"></a>Az.Storage
* Установка параметра StorageAccountName для контекста хранилища в качестве реального имени учетной записи хранения, если она была создана с использованием токена Sas, OAuth или анонимного доступа.
    - New-AzStorageContext
* Создание токена Sas большого двоичного объекта моментального снимка с параметром "-FullUri". Возвращаемый URI исправлен на URI моментального снимка.
    - New-AzStorageBlobSASToken

#### <a name="azwebsites"></a>Az.Websites
* Исправлена ошибка синтаксического анализа даты в "Get-AzDeletedWebApp".
* Устранена проблема обратной совместимости с модулем Az.Accounts.

## <a name="100---december-2018"></a>1.0.0 — декабрь 2018 г.
### <a name="general"></a>Общие сведения

- Общедоступная версия модуля Az.
- Справка в Интернете для каждого модуля.
- Дополнительные сведения и стратегию развития см. в статье [Announcing New Module 'Az'](https://aka.ms/azps-announce) (Объявление о новом модуле Az)
- Сведения о миграции с AzureRM см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)

### <a name="azaccounts"></a>Az.Accounts
- Изменено с Az.Profile.
- Исправлены форматы таблиц для типов профиля и контекста.

### <a name="azapimanagement"></a>Az.ApiManagement
- Исправления для #7002.
- Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)

### <a name="azbatch"></a>Az.Batch
- Добавлена возможность видеть, какая версия агента узла пакетной службы Azure работает в пуле на каждой виртуальной машине, с помощью нового свойства `NodeAgentInformation` в `PSComputeNode`.
- Значение `Caching` по умолчанию для `PSDataDisk` теперь `ReadWrite` вместо `None`.
- Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)

### <a name="azbilling"></a>Az.Billing
- Объединены командлеты Billing, Consumption и UsageAggregates. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0).

### <a name="azcognitivservices"></a>Az.CognitivServices
- Добавлены средства заполнения для SkuName и Typem, доступные в операции New-AzureRmCognitiveServicesAccount.
- Удален набор параметров GetSkusWithAccountParamSetName из Get-AzCognitiveServicesAccountSkus.

### <a name="azcontainerinstance"></a>Az.ContainerInstance
- Добавлена поддержка ManagedIdentity.

### <a name="azdatalakeanalytics"></a>Az.DataLakeAnalytics
- Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)

### <a name="azdatalakestore"></a>Az.DataLakeStore
- Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)

### <a name="azmonitor"></a>Az.Monitor
- "Az.Insights" переименован в "Az.Monitor" и внесены другие незначительные критические изменения. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)

### <a name="azkeyvault"></a>Az.KeyVault
- Из типов вывода удалено устаревшее свойство PurgeDisabled

### <a name="azmachinelearning"></a>Az.MachineLearning
- Включены командлеты из модуля Az.MachineLearningCompute

### <a name="azmedia"></a>Az.Media
- Удаляет устаревший псевдоним Tags из New-AzMediaService

### <a name="aznetwork"></a>Az.Network
В шлюз приложений добавлена поддержка настройки RewriteRuleSets
    - Добавлены новые командлеты:
        - Add-AzureRmApplicationGatewayRewriteRuleSet
        - Get-AzureRmApplicationGatewayRewriteRuleSet
        - New-AzureRmApplicationGatewayRewriteRuleSet
        - Remove-AzureRmApplicationGatewayRewriteRuleSet
        - Set-AzureRmApplicationGatewayRewriteRuleSet
        - New-AzureRmApplicationGatewayRewriteRule
        - New-AzureRmApplicationGatewayRewriteRuleActionSet
        - New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration
    - В следующие командлеты добавлен необязательный параметр -RewriteRuleSet
        - New-AzureRmApplicationGateway
        - New-AzureRmApplicationGatewayRequestRoutingRule
        - Add-AzureRmApplicationGatewayRequestRoutingRule
        - New-AzureRmApplicationGatewayPathRuleConfig
        - Add-AzureRmApplicationGatewayUrlPathMapConfig
        - New-AzureRmApplicationGatewayUrlPathMapConfig добавил с помощью идентификатора поддержку KeyVault для шлюза приложений.
    - В следующие командлеты добавлен необязательный параметр -KeyVaultSecretId, -KeyVaultSecret
        - Add-AzApplicationGatewaySslCertificate
        - New-AzApplicationGatewaySslCertificate
        - Set-AzApplicationGatewaySslCertificate
    - В командлет New-AzApplicationGateway добавлен необязательный параметр -UserAssignedIdentity
- Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)

### <a name="azoperationalinsights"></a>Az.OperationalInsights
- Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)

### <a name="azprofile"></a>Az.Profile
- Имя модуля изменено на Az.Accounts.

### <a name="azrecoveryservices"></a>Az.RecoveryServices
- Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)

### <a name="azresources"></a>Az.Resources
- Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)

### <a name="azservicefabric"></a>Az.ServiceFabric
- Поддержка спецификации сертификата по общему имени и отпечатку
- Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)

### <a name="azsignalr"></a>Az.SIgnalR
- Общедоступная версия командлетов PowerShell для SIgnalR

### <a name="azsql"></a>Az.Sql
- Добавлены новые типы обнаружения Data_Exfiltration и Unsafe_Action в командлеты обнаружения угроз
- Примеры обновленной документации для командлетов аудита Sql
- Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)

### <a name="azstorage"></a>Az.Storage
- Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)

### <a name="azwebsites"></a>Az.Websites
- Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)

## <a name="070---december-2018"></a>0.7.0 — декабрь 2018 г.

### <a name="general"></a>Общие сведения

* Незначительные изменения для предстоящего перехода AzureRM на Az

### <a name="azcompute"></a>Az.Compute

* Добавлена поддержка UltraSSD и образов коллекции в простых наборах параметров для командлетов `New-AzVm(ss)`.

### <a name="azdatalakestore"></a>Az.DataLakeStore

* Исправлено косую черту в конце домена учетной записи ADLS

### <a name="azfrontdoor"></a>Az.FrontDoor

* Исправлены некоторые неработающие ссылки
    - В статьях New-AzureRmFrontDoor и Set-AzureRmFrontDoor исправлена ссылка на статью командлета New-AzureRmFrontDoorHealthProbeSettingObject.
    - В статье New-AzureRmFrontDoorManagedRuleObject исправлена ссылка на статью командлета New-AzureRmFrontDoorRuleGroupOverrideObject.

### <a name="azrecoveryservices"></a>Az.RecoveryServices

* Добавлены проверки на стороне клиента для операций восстановления общей папки Azure.
* StorageAccountName и storageAccountResourceGroupName являются необязательными для восстановления afs.

### <a name="azresources"></a>Az.Resources

* Исправление для https://github.com/Azure/azure-powershell/issues/7679.
    - Обновите Get-AzureRmRoleAssignment, чтобы использовать область подписки, если она указана при запросе классических администраторов.

### <a name="azsql"></a>Az.Sql

* Незначительные изменения для предстоящего перехода AzureRM на Az
* Устранена проблема с использованием Get-AzureRmSqlDatabaseVulnerabilityAssessment с .NET Core.
* Изменена документация справочных сообщений, связанных с командлетами аудита SQL.

### <a name="azstorage"></a>Az.Storage

* Добавлено -EnableHierarchicalNamespace к New-AzureRmStorageAccount
* Устранена проблема, из-за которой командлет Copy File не может повторно использовать исходный контекст в пункте назначения, если не введен -DestContext
    - Start-AzureStorageFileCopy
* Поддержка статической конфигурации сайта
    - Enable-AzureStorageStaticWebsite
    - Disable-AzureStorageStaticWebsite

### <a name="azwebsites"></a>Az.Websites

* Set-AzureRmWebApp и Set-AzureRmWebAppSlot
    - Добавлен новый параметр (-AzureStoragePath), который указывает путь службы хранилища Azure для подключения в приложениях-контейнерах Windows и Linux. Используйте выходные данные нового командлета New-AzureRmWebAppAzureStoragePath в качестве параметра, чтобы задать пути к службе хранилища Azure.

## <a name="061---november-2018"></a>0.6.1 — ноябрь 2018 г.

### <a name="azapimanagement"></a>Az.ApiManagement
* Обновлены зависимости для устранения проблемы сопоставления типов.

### <a name="azautomation"></a>Az.Automation
* Командлеты службы автоматизации Azure на базе Swagger.
* Добавлены командлеты для Управления обновлениями.
* Добавлены командлеты для системы управления версиями.
* Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.
* Исправлена команда DSC для регистрации узла.

### <a name="azcompute"></a>Az.Compute
* Исправлена проблема с удостоверением, назначаемым системой.
* Обновлены зависимости для устранения проблемы сопоставления типов.

### <a name="azcontainerinstance"></a>Az.ContainerInstance
* Обновлены зависимости для устранения проблемы сопоставления типов.

### <a name="azmarketplaceordering"></a>Az.MarketplaceOrdering
* Обновлено описание в примерах командлетов для Marketplace.

### <a name="aznetwork"></a>Az.Network
* Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.
* Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.
* Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.
* Исправлены проблемы с использованием памяти в карте виртуальной сети.

### <a name="azrecoveryservicesbackup"></a>Az.RecoveryServices.Backup
* Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.
* Параметры часового пояса преобразованы в верхний регистр.

### <a name="azrecoveryservicessiterecovery"></a>Az.RecoveryServices.SiteRecovery
* Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.
* Обновлены зависимости для устранения проблемы сопоставления типов.

### <a name="azrelay"></a>Az.Relay
* Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.

### <a name="azresources"></a>Az.Resources
* Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.
* Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.
* Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.

### <a name="azservicefabric"></a>Az.ServiceFabric
* Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.

### <a name="azsql"></a>Az.Sql
* Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.
    - Get-AzureRmSqlInstance.
    - New-AzureRmSqlInstance.
    - Set-AzureRmSqlInstance.
    - Remove-AzureRmSqlInstance.
    - Get-AzureRmSqlInstanceDatabase.
    - New-AzureRmSqlInstanceDatabase.
    - Restore-AzureRmSqlInstanceDatabase.
    - Remove-AzureRmSqlInstanceDatabase.
* Добавлено расширенное управление политиками аудита для сервера или базы данных.
    - Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.
    - Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.
    - Set-AzureRmSqlServerAuditing.
    - Get-AzureRmSqlServerAuditing.
    - Set-AzureRmSqlDatabaseAuditing.
    - Get-AzureRmSqlDatabaseAuditing.
* Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.

## <a name="050---november-2018"></a>0.5.0 — ноябрь 2018 г.
#### <a name="general"></a>Общие сведения
* Добавлены средства заполнения ресурсов для многих основных командлетов — они позволяют вам переключать существующие имена ресурсов при вызове командлетов в интерактивном режиме

#### <a name="azprofile"></a>Az.Profile
* Обновлен общий код для использования последней версии ClientRuntime.
* В командлете Connect-AzAccount параметр TenantId переименован в Tenant и добавлен псевдоним для TenantId
* Обновлено описание TenantId для командлета Connect-AzAccount
* Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.
    - https://github.com/Azure/azure-powershell/issues/6936
* Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.
    - https://github.com/Azure/azure-powershell/issues/7453
* Устранена проблема с конечными точками DataLake при использовании MSI.
    - https://github.com/Azure/azure-powershell/issues/7462
* Устранена проблема, при которой командлет Disconnect-AzAccount вызывал сбой при отсутствии подключения
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Добавлена операция Get-AzCognitiveServicesAccountSkus.

#### <a name="azcompute"></a>Az.Compute
* Добавлены командлеты Add-AzVmssVMDataDisk и Remove-AzVmssVMDataDisk
* Get-AzVMImage отображает AutomaticOSUpgradeProperties
* Устранена проблема, при которой значения параметров SetAzVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Обновлен пакет DataLake до версии 1.1.10.
* Параметр по умолчанию Concurrency добавлен к многопоточным операциям.

#### <a name="azinsights"></a>Az.Insights
* Исправлена проблема № 7267 (область автомасштабирования).
    - Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).
* Исправлена проблема № 7513 [Insights], при которой для командлета Set-AzDiagnosticSetting требовалось явное указание категорий во время создания параметра
    - Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.

#### <a name="aznetwork"></a>Az.Network
* Параметр PeeringType является обязательным для следующих командлетов:
    - Get-AzExpressRouteCircuitRouteTable
    - Get-AzExpressRouteCircuitARPTable
    - Get-AzExpressRouteCircuitRouteTableSummary
    - Get-AzExpressRouteCrossConnectionArpTable
    - Get-AzExpressRouteCrossConnectionRouteTable
    - Get-AzExpressRouteCrossConnectionRouteTableSummary

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Добавлена политика исправления командлетов.

#### <a name="azresources"></a>Az.Resources
* Исправление для https://github.com/Azure/azure-powershell/issues/7402.
    - Разрешено перечисление ресурсов с помощью параметра -ResourceId для командлета Get-AzResource

#### <a name="azservicebus"></a>Az.ServiceBus
* Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Устранена проблема с добавлением сертификата в VMSS Linux.
* Исправлен командлет Add-AzServiceFabricClusterCertificate
    - Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).
    - Исключение отображается правильно (Azure/service-fabric-issues#1054).
* Исправлен командлет Update-AzServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.

## <a name="040---october-2018"></a>0.4.0 — октябрь 2018 г.
#### <a name="azprofile"></a>Az.Profile
* Устранена проблема с Get-AzSubscription в CloudShell
* Обновлен общий код для использования последней версии ClientRuntime.

#### <a name="azcompute"></a>Az.Compute
* В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzVm
* Во все командлеты добавлено средство заполнения для аргумента ResourceName.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Добавлена поддержка правил виртуальной сети:
    - Get-AzDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.
    - Add-AzDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.
    - Set-AzDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.
    - Remove-AzDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.

#### <a name="aznetwork"></a>Az.Network
* Обновлен командлет Test-AzNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.
* Во все командлеты добавлено средство заполнения для аргумента ResourceName.

#### <a name="azresources"></a>Az.Resources
* Устранена проблема, из-за которой командлет Get-AzRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), благодаря добавлению понятного исключения в сценарий. Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.

## <a name="030---october-2018"></a>0.3.0 — октябрь 2018 г.
#### <a name="azurestorage"></a>Azure.Storage;
* Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.
    - Start-AzureStorageBlobCopy
    - Start-AzureStorageFileCopy
* Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.
    - Get-AzStorageUsage

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Поддержка Get-AzCognitiveServicesAccountSkus без существующей учетной записи.

#### <a name="azcompute"></a>Az.Compute
* Исправлена команда Get-AzVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов
* Добавлен пример использования SimpleParameterSet в справку командлета New-AzVmss.
* Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.

#### <a name="azdatafactoryv2"></a>Az.DataFactoryV2
* Пакет .NET SDK для ADF обновлен до версии 2.3.0.

#### <a name="aznetwork"></a>Az.Network
* Добавлена функциональность NetworkProfile. Добавлены новые командлеты:
    - Get-AzNetworkProfile
    - New-AzNetworkProfile
    - Remove-AzNetworkProfile
    - Set-AzNetworkProfile
    - New-AzContainerNicConfig
    - New-AzContainerNicConfigIpConfig
* Добавлен канал связи служб в модель подсети.
* Добавлены командлеты: New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap
* Добавлены командлеты: Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig

#### <a name="azrediscache"></a>Az.RedisCache
* С этого момента добавлена поддержка любой строки в качестве параметра Size. Добавлено значение P5 во всплывающее окно PSArgumentCompleter.

#### <a name="azresources"></a>Az.Resources
* Добавлен отсутствующий параметр -Mode в командлет Set-AzPolicyDefinition
* Исправлена ошибка командлета Get-AzProviderOperation для операций, когда Origin содержит User

#### <a name="azsql"></a>Az.Sql
* Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.

#### <a name="azwebsites"></a>Az.Websites
* Новый командлет Get-AzWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера
* Новые командлеты New-AzWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows

## <a name="020---september-2018"></a>0.2.0 — сентябрь 2018 г.
 Начальный выпуск
