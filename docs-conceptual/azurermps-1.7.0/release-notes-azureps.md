---
title: "Журнал изменений Azure PowerShell | Документация Майкрософт"
description: "Это руководство содержит историю изменений Azure PowerShell, внесенных в новом выпуске."
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: 
ms.date: 05/18/2017
ms.openlocfilehash: 0a3f152751fee569d3ac5fba6bcff8c1737f7b8c
ms.sourcegitcommit: 226527be7cb647acfe2ea9ab151185053ab3c6db
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/29/2017
---
# <a name="release-notes"></a>Заметки о выпуске

Здесь приведен список изменений, внесенных в Azure PowerShell в этом выпуске.

## <a name="version-170"></a>Версия 1.7.0

* **Изменено поведение параметров -Force, -Confirm и $ConfirmPreference для всех командлетов. Мы внесли изменения в эту реализацию для соответствия рекомендациям PowerShell. Для большинства командлетов это значит удаление параметра Force, а чтобы пропустить приглашение ShouldProcess, пользователям потребуется включить параметр -Confirm:$false в скрипты PowerShell.** Эти изменения обеспечили следующие возможности:
  - Правильная реализация функций –WhatIf, что позволяет пользователю определить влияние командлета или скрипта без внесения фактических изменений.
  - Контроль над запросом с помощью параметра $ConfirmPreference для всего сеанса, чтобы пользователь запрашивался на основе влияния предполагаемого изменения (как описано в параметре ConfirmImpact командлета).
  - Контроль над запросами на подтверждение команд с помощью параметра -Confirm для конкретного командлета.
  - Согласованное использование параметров ShouldContinue и –Force для командлетов только для действий, требующих запроса от пользователя из-за особого характера изменений (например, удаление скрытых файлов).
  - Согласованность с другими командлетами PowerShell, чтобы знания скриптов PowerShell из других командлетов могли быть применимы к командлетам Azure PowerShell.

**Обратите внимание, что теперь для *автоматического пропуска всех запросов во всех случаях* для командлетов Azure PowerShell необходимо указать два параметра:**
```powershell
My-CmdletWithConfirmation –Confirm:$false -Force
```
* Служба вычислений Azure
  - Set-AzureRmVMADDomainExtension.
  - Get-AzureRmVMADDomainExtension.
  - Параметр -Redeploy для Restart-AzureVM.
  - Параметр -Validate для Move-AzureService, Move-AzureStorageAccount и Move-AzureVirtualNetwork.
  - Как и прежде, параметры имени и версии для командлетов расширения являются необязательными.
  - Командлет New-AzureVM может узнать тип лицензии у объекта виртуальной машины.
* Хранилище Azure
  - В следующих командлетах параметр Tags изменен на Tag, а для параметра Tags добавлен псевдоним:
    + New-AzureRmStorageAccount;
    + Set-AzureRmStorageAccount.
* Сеть Azure
  - Добавлен новый командлет для пиринга между виртуальными сетями.
* кэш Azure Redis
  - Добавлен новый командлет для Reset-AzureRmRedisCache.
  - Добавлен новый командлет для Export-AzureRmRedisCache.
  - Добавлен новый командлет для Import-AzureRmRedisCache.
  - Теперь командлет New-AzureRmRedisCache включает изменение параметра для виртуальной сети.
* Архивация и восстановление базы данных SQL Azure
  - Командлеты для функции долгосрочного хранения резервных копий:
  - Get-AzureRmSqlServerBackupLongTermRetentionVault;
  - Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy;
  - Set-AzureRmSqlServerBackupLongTermRetentionVault;
  - Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.
  - Restore-AzureRmSqlDatabase теперь поддерживает восстановление до точки во времени для удаленной базы данных.
  - Restore-AzureRmSqlDatabase теперь поддерживает восстановление из резервной копии долгосрочного хранения.
* Приложение логики Azure
  - Добавлены командлеты учетных записей интеграции приложения логики:
  - Get-AzureRmIntegrationAccountAgreement;
  - Get-AzureRmIntegrationAccountCallbackUrl;
  - Get-AzureRmIntegrationAccountCertificate;
  - Get-AzureRmIntegrationAccount;
  - Get-AzureRmIntegrationAccountMap;
  - Get-AzureRmIntegrationAccountPartner;
  - Get-AzureRmIntegrationAccountSchema;
  - New-AzureRmIntegrationAccountAgreement;
  - New-AzureRmIntegrationAccountCertificate;
  - New-AzureRmIntegrationAccount;
  - New-AzureRmIntegrationAccountMap;
  - New-AzureRmIntegrationAccountPartner;
  - New-AzureRmIntegrationAccountSchema;
  - Remove-AzureRmIntegrationAccountAgreement;
  - Remove-AzureRmIntegrationAccountCertificate;
  - Remove-AzureRmIntegrationAccount;
  - Remove-AzureRmIntegrationAccountMap;
  - Remove-AzureRmIntegrationAccountPartner;
  - Remove-AzureRmIntegrationAccountSchema;
  - Set-AzureRmIntegrationAccountAgreement;
  - Set-AzureRmIntegrationAccountCertificate;
  - Set-AzureRmIntegrationAccount;
  - Set-AzureRmIntegrationAccountMap;
  - Set-AzureRmIntegrationAccountPartner;
  - Set-AzureRmIntegrationAccountSchema.
* Хранилище озера данных Azure
  - Существенно улучшена производительность передачи и скачивания файлов и папок.
  - Внесены некоторые изменения имен параметров для скачивания и добавлены два новых параметра для передачи:
    + NumThreads -> PerFileThreadCount обозначает число потоков, используемых в одном файле;
    + ConcurrentFileCount указывает количество файлов для отправки или загрузки папки в параллельном режиме.
  - Значения потоков по умолчанию теперь разработаны так, чтобы обеспечить лучшую пропускную способность для большинства размеров файлов. Если производительность ниже требуемой, указанные выше значения можно изменить в соответствии с требованиями.
* Аналитика озера данных Azure
  - Get-AzureRMDataLakeAnalyticsDataSource теперь возвращает все источники данных, когда вызывается без аргументов.
  - Это изменение также удаляет параметр типа источника данных из командлета.
  - Это изменение приводит к возврату нового объекта для операции перечисления со следующими свойствами:
    + Type — тип источника данных.
    + Name — имя источника данных.
    + IsDefault — присвоено значение true, если для учетной записи это источник данных по умолчанию.
  - Get-AzureRMDataLakeAnalyticsJob исправлен для списка определенных значений смещения времени и даты при фильтрации по submittedBefore и submittedAfter.
* Веб-приложения
  - Добавлен командлет Swap-AzureRmWebAppSlot для обычной замены и замены с предварительным просмотром.
  - Командлет Set-AzureRmWebAppSlot теперь поддерживает автоматический перенос.
* Cлужба управления Azure API 
  - Исправлены командлеты развертывания управления API Azure для облака Azure для Китая.
  - Удален командлет Set-AzureRmApiManagementTenantGitAccess, так как доступ к Git включен по умолчанию.
* Архивация с помощью служб восстановления Azure
  - Добавлена поддержка для рабочей нагрузки SQL Azure.
  - Добавлена поддержка для архивации и восстановления зашифрованных виртуальных машин Azure.
  - Backup-AzureRmRecoveryServicesBackupItem — добавлена необязательная функция периода хранения для точек восстановления.
  - Исправлены незначительные ошибки, связанные с фильтрами, в командлетах Get-AzureRmRecoveryServicesBackupContainer и Get-AzureRmRecoveryServicesBackupItem.
* Служба автоматизации Azure
  - Добавлен командлет Get-AzureRmAutomationHybridWorkerGroup.
