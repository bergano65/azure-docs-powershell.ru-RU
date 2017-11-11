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
ms.openlocfilehash: 143d92384fd270711378f6741ba59e88c12833d1
ms.sourcegitcommit: b256bf48e15ee98865de0fae50e7b81878b03a54
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2017
---
# <a name="release-notes"></a>Заметки о выпуске

Здесь приведен список изменений, внесенных в Azure PowerShell в этом выпуске.

## <a name="version-220"></a>Версия 2.2.0
* Среда выполнения приложений
  - Добавлена поддержка для запроса состояния шифрования из расширения AzureDiskEncryptionForLinux.
* Фабрика данных
  - Добавлен новый командлет для перечисления окон действий:
    + Get-AzureRmDataFactoryActivityWindow.
* Data Lake
  - В следующих командлетах параметр `Host` изменен на `DatabaseHost`, а в `Host` добавлен псевдоним:
    + New-AzureRmDataLakeAnalyticsCatalogSecret;
    + Set-AzureRmDataLakeAnalyticsCatalogSecret.
  - Добавлена поддержка для удаления списка ACL и списка ACL по умолчанию.
  - Добавлена поддержка для получения и настройки разрешений без имени для файлов и папок.
* Хранилище ключей
  - Добавлена поддержка следующих сертификатов:
    + Add-AzureKeyVaultCertificate;
    + Add-AzureKeyVaultCertificateContact;
    + Get-AzureKeyVaultCertificate;
    + Get-AzureKeyVaultCertificateContact;
    + Get-AzureKeyVaultCertificateIssuer;
    + Get-AzureKeyVaultCertificateOperation;
    + Get-AzureKeyVaultCertificatePolicy;
    + Import-AzureKeyVaultCertificate;
    + New-AzureKeyVaultCertificateAdministratorDetails;
    + New-AzureKeyVaultCertificateOrganizationDetails;
    + New-AzureKeyVaultCertificatePolicy;
    + Remove-AzureKeyVaultCertificate;
    + Remove-AzureKeyVaultCertificateContact;
    + Remove-AzureKeyVaultCertificateIssuer;
    + Remove-AzureKeyVaultCertificateOperation;
    + Set-AzureKeyVaultCertificateAttribute;
    + Set-AzureKeyVaultCertificateIssuer;
    + Set-AzureKeyVaultCertificatePolicy;
    + Stop-AzureKeyVaultCertificateOperation.
* Сеть

  - Для сетевого интерфейса добавлен новый параметр переключателя, чтобы включить или отключить ускорение работы в сети — +New-AzureRmNetworkInterface -EnableAcceleratedNetworking.
  - Добавлены командлеты PowerShell для включения функций шлюза в режиме "активный-активный":
    + Add-AzureRmVirtualNetworkGatewayIpConfig;
    + Remove-AzureRmVirtualNetworkGatewayIpConfig.
  - Добавлен новый командлет:
    + Test-AzureRmPrivateIpAddressAvailability.
* Ресурсы
  - Добавлена поддержка зон в командлетах поставщика и ресурсов:
    + Get-AzureRmProvider;
    + New-AzureRmResource;
    + Set-AzureRmResource.
* SQL
  - Добавлены новые командлеты для управления политикой обнаружения угроз SQL Azure на уровне сервера:
    + Get-AzureRmSqlServerThreatDetectionPolicy;
    + Remove-AzureRmSqlServerThreatDetectionPolicy;
    + Set-AzureRmSqlServerThreatDetectionPolicy.
  - Добавлены новые командлеты для поддержки включения или отключения GeoBackupPolicy для Sql Azure DataWarehouses:
    + Get-AzureRmSqlDatabaseGeoBackupPolicy;
    + Set-AzureRmSqlDatabaseGeoBackupPolicy.
  - Добавлены новые командлеты для API-интерфейсов помощников SQL Azure и рекомендуемых действий:
    + Get-AzureRmSqlDatabaseAdvisor;
    + Get-AzureRmSqlElasticPoolAdvisor;
    + Get-AzureRmSqlServerAdvisor;
    + Get-AzureRmSqlDatabaseRecommendedActions;
    + Get-AzureRmSqlElasticPoolRecommendedActions;
    + Get-AzureRmSqlServerRecommendedActions;
    + Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus;
    + Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus;
    + Set-AzureRmSqlServerAdvisorAutoExecuteStatus;
    + Set-AzureRmSqlDatabaseRecommendedActionState;
    + Set-AzureRmSqlElasticPoolRecommendedActionState;
    + Set-AzureRmSqlServerRecommendedActionState.