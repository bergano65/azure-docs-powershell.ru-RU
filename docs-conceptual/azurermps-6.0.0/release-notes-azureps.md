---
title: Журнал изменений Azure PowerShell | Документация Майкрософт
description: Это руководство содержит историю изменений Azure PowerShell, внесенных в новом выпуске.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 8515a267e80e5d1f7bb97557efa72b9e86b7b45d
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/08/2018
---
# <a name="release-notes"></a>Заметки о выпуске

Здесь приведен список изменений, внесенных в Azure PowerShell в этом выпуске.

---

## <a name="600---may-2018"></a>6.0.0 — май 2018 г.

### <a name="general"></a>Общие сведения
* Минимальная версия зависимости от модулей повышена до PowerShell 5.0.

### <a name="azurestorage"></a>Azure.Storage;
* Добавлена поддержка имени контейнера хранилища BLOB-объектов:
    - New-AzureStorageBlobContainer;
    - Remove-AzureStorageBlobContainer;
    - Set-AzureStorageBlobContent
    - Get-AzureStorageBlobContent
* Исправлена проблема, из-за которой в выходных данных командлетов службы хранилища, которые завершались ошибкой, отсутствовали подробные сведения об ошибке.

### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Представлено много критически важных изменений.
    - Дополнительные сведения см. в руководстве по миграции.

### <a name="azurermautomation"></a>AzureRM.Automation
* Из следующих командлетов удален нерекомендуемый псевдоним Tags:
    - Set-AzureRmAutomationRunbook.

### <a name="azurermbatch"></a>AzureRM.Batch
* В документации по New-AzureBatchPool удален нерекомендуемый пример.

### <a name="azurermcdn"></a>AzureRM.Cdn
* Представлено много критически важных изменений.
    - Дополнительные сведения см. в руководстве по миграции.

### <a name="azurermcompute"></a>AzureRM.Compute
* New-AzureRmVm и New-AzureRmVmss поддерживают подробные выходные данные параметров.
* New-AzureRmVm и New-AzureRmVmss (простой набор параметров) поддерживают назначение виртуальной машине определяемых пользователем и (или) определяемые системой удостоверений.
* В масштабируемый набор виртуальных машин добавлены функции Redeploy и PerformMaintenance.
    -  В Set-AzureRmVmss и Set-AzureRmVmssVM добавлены новые параметры-переключатели -Redeploy и -PerformMaintenance.
* В командлет Set-AzureRmVMOperatingSystem добавлен параметр-переключатель DisableVMAgent.
* В New-AzureRmVm и New-AzureRmVmss (простой набор параметров) добавлена поддержка образа Win10.
* Добавлен командлет Repair-AzureRmVmssServiceFabricUpdateDomain.
* Представлено много критически важных изменений.
    - Дополнительные сведения см. в руководстве по миграции.
* Для Set-AzureRmVmDiskEncryptionExtension параметры AAD стали необязательными.

### <a name="azurermdatafactories"></a>AzureRM.DataFactories
* Из следующих командлетов удален нерекомендуемый псевдоним Tags:
    - New-AzureRmDataFactory

### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Обновлен пакет .Net SDK для ADF до версии 0.7.0-preview, содержащий следующие изменения:
    - Для действия ExecuteSSISPackage добавлены параметры выполнения и свойство диспетчера подключений.
    - Обновлены связанные службы PostgreSql и MySql для использования всей строки подключения вместо параметров сервера, базы данных, схемы, имени пользователя и пароля.
    - Из связанной службы DB2 удалена схема.
    - Из связанной службы Teradata удалено свойство схемы.
    - Для Responsys добавлены параметры LinkedService, Dataset, CopySource.

### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* Из следующих командлетов удален нерекомендуемый псевдоним Tags:
    - New-AzureRmDataLakeAnalyticsAccount;
    - Set-AzureRmDataLakeAnalyticsAccount.

### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Добавлена новая функция рекурсивного изменения списка ACL в командлеты Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAclEntry и Set-AzureRmDataLakeStoreItemAcl.
* Добавлен новый командлет для получения сводки по содержимому в каталоге.
* Добавлен новый командлет для получения дампа ACL и сведений об использовании диска.
* Исправлен тип возвращаемого значения Set-AzureRmDataLakeStoreItemAcl с логического на IEnumerable<DataLakeStoreItemAce>
* Исправлен тип возвращаемого значения Set-AzureRmDataLakeStoreItemAclEntry с логического на IEnumerable<DataLakeStoreItemAce>
* В командлеты Export-AzureRmDataLakeStoreItem, Import-AzureRmDataLakeStoreItem, Remove-AzureRmDataLakeStoreItem внесены критически важные изменения.

### <a name="azurermdns"></a>AzureRM.Dns
* Представлено много критически важных изменений.
    - Дополнительные сведения см. в руководстве по миграции.

### <a name="azurermeventhub"></a>AzureRM.EventHub
* В справку добавлены отсутствующие ранее примеры для командлетов.

### <a name="azurerminsights"></a>AzureRM.Insights;
* Представлено много критически важных изменений.
    - Дополнительные сведения см. в руководстве по миграции.

### <a name="azurermiothub"></a>AzureRM.IotHub
* Для IotHub включены теги и SKU "Базовый".

### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Внесены критически важные изменения для поддержки конвейерного режима.
* Добавлены новые командлеты: Backup/Restore-AzureKeyVaultManagedStorageAccount, Backup/Restore-AzureKeyVaultCertificate, Undo-AzureKeyVaultManagedStorageSasDefinitionRemoval и Undo-AzureKeyVaultManagedStorageAccountRemoval.

### <a name="azurermmachinelearning"></a>AzureRM.MachineLearning
* Из следующих командлетов удален нерекомендуемый псевдоним Tags:
    - Update-AzureRmMlCommitmentPlan

### <a name="azurermmedia"></a>AzureRM.Media
* Из следующих командлетов удален нерекомендуемый псевдоним Tags:
    - Set-AzureRmMediaService.

### <a name="azurermnetwork"></a>AzureRM.Network
* Добавлена поддержка ресурса плана защиты от атак DDoS.
* Представлено много критически важных изменений.
    - Дополнительные сведения см. в руководстве по миграции.

### <a name="azurermnotificationhubs"></a>AzureRM.NotificationHubs
* Представлено много критически важных изменений.
    - Дополнительные сведения см. в руководстве по миграции.

### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights;
* Представлено много критически важных изменений.
    - Дополнительные сведения см. в руководстве по миграции.

### <a name="azurermprofile"></a>AzureRM.Profile
* Автосохранение контекста включено по умолчанию.
* В среде Azure для государственных организаций США добавлены свойства USGovernmentOperationalInsightsEndpoint и USGovernmentOperationalInsightsEndpointResourceId.

### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* Исправлен заголовок аутентификации в сценариях SiteRecovery.

### <a name="azurermrediscache"></a>AzureRM.RedisCache
* Представлено много критически важных изменений.
    - Дополнительные сведения см. в руководстве по миграции.

### <a name="azurermresources"></a>AzureRM.Resources
* Удален устаревший параметр -AtScopeAndBelow из вызова Get-AzureRmRoledefinition.
* В результаты Get-AzureRmRoleAssignment добавлены данные о назначениях для удаленных элементов USers, Groups и ServicePrincipals.
* Добавлены средства заполнения вкладок для Scope и ResourceType.
* Добавлен вспомогательный командлет для создания субъектов служб.
* Функции Get - и -Find объединены в Get-AzureRmResource.
* Добавлены командлеты Active Directory:
  - Remove-AzureRmADGroupMember;
  - Get-AzureRmADGroup;
  - New-AzureRmADGroup;
  - Remove-AzureRmADGroup;
  - Remove-AzureRmADUser;
  - Update-AzureRmADApplication;
  - Update-AzureRmADServicePrincipal;
  - Update-AzureRmADUser.

### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Обновлен используемый по умолчанию SKU версии образа Linux.
  - NewAzureServiceFabricCluster.cs default UbuntuServer1604 Sku update

### <a name="azurermstorage"></a>AzureRM.Storage
* Представлено много критически важных изменений.
    - Дополнительные сведения см. в руководстве по миграции.

### <a name="azurermwebsites"></a>AzureRM.Websites
* Пакет SDK для веб-сайтов обновлен до последней версии.
* Для Set-AzureRmWebApp и Set-AzureRmWebAppSlot добавлены свойства -AssignIdentity и -Httpsonly.
* Добавлены два новых командлета: Get-AzureRmWebAppSnapshots и Restore-AzureRmWebAppSnapshot.
