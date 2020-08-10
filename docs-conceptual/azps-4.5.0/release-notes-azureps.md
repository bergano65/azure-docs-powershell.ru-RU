---
title: Заметки о выпуске Azure PowerShell
description: Узнайте обо всех последних обновлениях модулей Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: 77cbbeb01f5c6fcbf0f61bfab3d3f63b74a53bc4
ms.sourcegitcommit: edfe63c6949cd59127028ac8a13bb4a8827d555c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/04/2020
ms.locfileid: "87566620"
---
# <a name="azure-powershell-release-notes"></a>Заметки о выпуске Azure PowerShell

## <a name="450---august-2020"></a>4.5.0 — август 2020 г.
#### <a name="azaccounts"></a>Az.Accounts
* Командлет Connect-AzAccount теперь принимает параметр MaxContextPopulation (№ 9865).
* Версия SubscriptionClient обновлена до 2019-06-01 и поддерживает отображение доменов арендаторов (№ 9838).
* Добавлена поддержка домашнего арендатора и сведений managedBy арендатора для подписки.
* Исправлено имя модуля и сведения о версии в данных телеметрии.
* Исправлено поведение SqlDatabaseDnsSuffix и ServiceManagementUrl, когда конечная точка метаданных среды возвращает несовместимое значение.

#### <a name="azaks"></a>Az.Aks
* Параметр ClientIdAndSecret замен на ServicePrincipalIdAndSecret и задан в виде псевдонима (№ 12381).
* Командлеты Get-AzAks, New-AzAks, Remove-AzAks, Set-AzAks заменены на Get-AzAksCluster, New-AzAksCluster, Remove-AzAksCluster, Set-AzAksCluster. Исходные командлеты заданы в виде псевдонимов (№ 12373).

#### <a name="azapimanagement"></a>Az.ApiManagement
* Добавлен новый командлет Add-AzApiManagementApiToGateway.
* Добавлен новый командлет Get-AzApiManagementGateway.
* Добавлен новый командлет Get-AzApiManagementGatewayHostnameConfiguration.
* Добавлен новый командлет Get-AzApiManagementGatewayKey.
* Добавлен новый командлет New-AzApiManagementGateway.
* Добавлен новый командлет New-AzApiManagementGatewayHostnameConfiguration.
* Добавлен новый командлет New-AzApiManagementResourceLocationObject.
* Добавлен новый командлет Remove-AzApiManagementApiFromGateway.
* Добавлен новый командлет Remove-AzApiManagementGateway.
* Добавлен новый командлет Remove-AzApiManagementGatewayHostnameConfiguration.
* Добавлен новый командлет Update-AzApiManagementGateway.
* Добавлен новый необязательный параметр [-GatewayId] в командлет Get-AzApiManagementApi.

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Задано явное использование действия "Отклонить" в качестве действия NetworkRules по умолчанию.

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Исправлена проблема, связанная с возникновением исключения при попытке Enum.Parse привести значение NULL к значениям перечисления Enabled или Disabled (№ 12344).

#### <a name="azhdinsight"></a>Az.HDInsight
* Добавлена поддержка создания кластера с функцией шифрования передаваемых данных.
    - Добавлен новый параметр EncryptionInTransit в командлет New-AzHDInsightCluster.
    - Добавлен новый параметр EncryptionInTransit в командлет New-AzHDInsightClusterConfig.
* Добавлена поддержка создания кластера с функцией приватного канала:
    - Добавлен новый параметр PublicNetworkAccessType и OutboundPublicNetworkAccessType в командлет New-AzHDInsightCluster.
    - Добавлен новый параметр PublicNetworkAccessType и OutboundPublicNetworkAccessType в командлет New-AzHDInsightClusterConfig.
* Реализовано возвращение сведений о виртуальной сети при вызове New-AzHDInsightCluster или Get-AzHDInsightCluster.

#### <a name="aznetwork"></a>Az.Network
* Включена поддержка параметра AddressPrefixType в Remove-AzExpressRouteCircuitConnectionConfig.
* Реализованы некритические изменения: функциональность PeerAddressType для частного пиринга в Remove-AzExpressRouteCircutPeeringConfig.
* Код изменен для игнорирования регистра в параметрах AddressPrefixType и PeerAddressType.
* Изменено сообщение с предупреждением для New-AzLoadBalancerFrontendIpConfig, New-AzPublicIpAddress и New-AzPublicIpPrefix.

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Добавлен параметр -ForceDelete для Remove-AzOperationalInsightsworkspace.
* Добавлен новый командлет Get-AzOperationalInsightsDeletedWorkspace.
* Добавлен новый командлет Restore-AzOperationalInsightsWorkspace.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Улучшена работа с обнаружением контейнеров и элементов Azure Backup.

#### <a name="azresources"></a>Az.Resources
* Добавлены свойства Condition, ConditionVersion и Description в New-AzRoleAssignment.
    - Это касается всех соответствующих изменений моделей данных.

#### <a name="azsql"></a>Az.Sql
* Исправлена ошибка, связанная с потенциальным игнорированием регистра имени сервера в New-AzSqlServer и Set-AzSqlServer.
* Исправлена ошибка, из-за которой возвращалось неправильное имя существующей базы данных в New-AzSqlDatabaseSecondary.

#### <a name="azstorage"></a>Az.Storage
* Добавлена поддержка создания маркера SAS контейнера и BLOB-объекта с новым разрешением x,t.
    -  New-AzStorageBlobSASToken
    -  New-AzStorageContainerSASToken
* Добавлена поддержка создания маркера SAS учетной записи с новым разрешением x,t,f.
    -  New-AzStorageAccountSASToken
* Добавлена поддержка получения данных об использовании одной общей папки.
    - Get-AzRmStorageShare

## <a name="440---july-2020"></a>4.4.0 — июль 2020 г.
#### <a name="azaccounts"></a>Az.Accounts
* Добавлен новый командлет Invoke-AzRestMethod.
* Устранена неполадка, из-за которой могли возникать ошибки с проверкой подлинности в сценариях с несколькими процессами, такими как выполнение нескольких командлетов Azure PowerShell с помощью Start-Job [№ 9448].

#### <a name="azaks"></a>Az.Aks
* Исправлена ошибка, из-за которой Get-AzAks выводит не все кластеры [ №12296].

#### <a name="azanalysisservices"></a>Az.AnalysisServices
* Удалена ссылка на проект для проверки подлинности.

#### <a name="azautomation"></a>Az.Automation
* Исправлена ошибка, из-за которой строка с escape-символами не преобразовывалась в объект JSON.

#### <a name="azcompute"></a>Az.Compute
* Добавлено предупреждение, которое отображается при использовании New-AzVmss, если версия образа не является последней.

#### <a name="azdatafactory"></a>Az.DataFactory
* Добавлены глобальные параметры в Фабрику данных.

#### <a name="azeventgrid"></a>Az.EventGrid
* Обновлен модуль для использования API версии 2020-06-01.
* Добавлены новые возможности:
    - сопоставление входных данных;
    - схема доставки событий;
    - Приватный канал
    - схема событий облака (версия 1.0);
    - раздел служебной шины как назначение;
    - функция Azure как назначение;
    - пакетная обработка данных веб-перехватчика;
    - безопасный веб-перехватчик (поддержка AAD);
    - фильтрация IP-адресов.
* Обновлены командлеты:
    - New-AzEventGridSubscription или Update-AzEventGridSubscription:
        - Добавлены новые необязательные параметры для поддержки пакетной обработки данных веб-перехватчика.
        - Добавлены новые необязательные параметры для поддержки безопасного веб-перехватчика с использованием AAD.
        - Добавлено новое перечисление для параметра EndpointType, чтобы обеспечить поддержку функции Azure и раздела служебной шины в качестве назначения.
        - Добавлен новый необязательный параметр для схемы доставки.
    - New-AzEventGridTopic или Update-AzEventGridTopic и New-AzEventGridDomain или Update-AzEventGridDomain:
        - Добавлены новые необязательные параметры для поддержки фильтрации IP-адресов.
    - New-AzEventGridTopic или New-AzEventGridDomain:
        - Добавлены новые необязательные параметры для поддержки сопоставления входных данных.

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Обновлен модуль для использования API версии 2020-05-01.
* Включена поддержка Приватного канала для ресурсов службы хранилища, Key Vault и службы веб-приложений.

#### <a name="azhdinsight"></a>Az.HDInsight
* Включена поддержка создания кластера с хранилищем ADLS 1-го и 2-го поколения в национальных облаках.

#### <a name="azmonitor"></a>Az.Monitor
* Исправлена ошибка с Get-AzDiagnosticSetting, связанная с присвоением значения NULL метрикам или журналам [№ 12272].

#### <a name="aznetwork"></a>Az.Network
* Исправлены ошибки с переключением параметров для подключения виртуальной сети концентратора к глобальной виртуальной сети.
* Добавлены новые командлеты для сайтов сетевых виртуальных модулей Azure.
    - Get-AzVirtualApplianceSite
    - New-AzVirtualApplianceSite
    - Remove-AzVirtualApplianceSite
    - Update-AzVirtualApplianceSite
    - New-AzOffice365PolicyProperty
* Добавлены новые командлеты для сетевого виртуального модуля Azure.
    - Get-AzNetworkVirtualAppliance
    - New-AzNetworkVirtualAppliance
    - Remove-AzNetworkVirtualAppliance
    - Update-AzNetworkVirtualAppliance
    - Get-AzNetworkVirtualApplianceSku
    - New-AzVirtualApplianceSkuProperty
* Общие командлеты для Шлюза приложений, подключенного к Приватному каналу.
* Общие командлеты для службы синхронизации хранилища, подключенной к Приватному каналу.
* Общие командлеты для службы SignalR, подключенной к Приватному каналу.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Удалена ссылка на проект для проверки подлинности.
* В Azure Backup представлена более точная справка по командлетам.
* В Azure Backup включена поддержка выборки заданий агента MAB с помощью командлета Get-AzRecoveryServicesBackupJob.

#### <a name="azresources"></a>Az.Resources
* Обновлен командлет Save-AzResourceGroupDeploymentTemplate для использования пакета SDK.
* Добавлен командлет Unregister-AzResourceProvider.

#### <a name="azsql"></a>Az.Sql
* Включена поддержка субъекта-службы и гостевых пользователей для командлета Set-AzSqlInstanceActiveDirectoryAdministrator.
* Исправлена ошибка в командлетах классификации данных.
* Включена поддержка отработки отказа Управляемого экземпляра SQL Azure. Invoke-AzSqlInstanceFailover

#### <a name="azstorage"></a>Az.Storage
* Исправлена ошибка, из-за которой в некоторых командлетах плоскости данных не добавлялся объект UserAgent.
* Включена поддержка создания и обновления учетной записи хранения с использованием MinimumTlsVersion и AllowBlobPublicAccess.
    -  New-AzStorageAccount
    -  Set-AzStorageAccount
* Включена поддержка включения и отключения управления версиями в службе BLOB-объектов учетной записи хранения.
    - Update-AzStorageBlobServiceProperty
* Включена поддержка вывода списка BLOB-объектов с данными о версиях BLOB-объектов.
    - Get-AzStorageBlob
* Включена поддержка получения или удаления одного моментального снимка BLOB-объекта или версии BLOB-объекта.
    - Get-AzStorageBlob
    - Remove-AzStorageBlob
* Включена поддержка конвейера на основе BLOB-объекта, созданного с помощью Azure.Storage.Blobs версии 12.
    - Get-AzStorageBlobContent
    - New-AzStorageBlobSASToken
    - Remove-AzStorageBlob
    - Set-AzStorageBlobContent
    - Start-AzStorageBlobCopy

#### <a name="azstoragesync"></a>Az.StorageSync
* Добавлена новая версия пакета SDK StorageSync, предназначенная для API версии 2020-03-01.
* Добавлен командлет для обновления службы синхронизации хранилища.
    - Set-AzStorageSyncService
* Добавлены классы IncomingTrafficPolicy и IncomingTrafficPolicy в командлеты службы синхронизации хранилища.

#### <a name="azwebsites"></a>Az.Websites
* Включена поддержка выполнения операций для слотов, которые находятся не в той же группе ресурсов, что и план службы приложений.

## <a name="430---june-2020"></a>4.3.0 — июнь 2020 года
#### <a name="azaccounts"></a>Az.Accounts
* Включена поддержка обнаружения параметров среды по умолчанию и добавления окружения с помощью командлета Add-AzEnvironment.
* Обновлены предварительно загруженные сборки [№ 12024], [№ 11976].
* Обновлена сборка Azure.Core.
* Исправлена ошибка, из-за которой выполнение Connect-AzAccount может завершаться сбоем при многопоточном выполнении [№ 11201].

#### <a name="azaks"></a>Az.Aks
* Заменено использование старого [API AccessProfile](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) вызовами API [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) и [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials).

#### <a name="azbatch"></a>Az.Batch
* Изменена версия SDK для Microsoft.Azure.Management.Batch для Az.Batch на 11.0.0.
* Включена возможность задать удостоверение BatchAccount в командлете New-AzBatchAccount.

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Включена поддержка отображения возможностей учетной записи.
* Включена поддержка изменения PublicNetworkAccess.

#### <a name="azcompute"></a>Az.Compute
* Добавлен параметр SimulateEviction в командлеты Set-AzVM и Set-AzVmssVM.
* Добавлен фрагмент Premium_LRS в средство заполнения аргументов параметра StorageAccountType для командлета New-AzGalleryImageVersion.
* Добавлены подсостояния для VMCustomScriptExtension [№ 11297].
* Добавлен фрагмент Delete в средство заполнения аргументов параметра EvictionPolicy для командлетов New-AzVM и New-AzVMConfig.
* Исправлено имя нового расширения виртуальной машины для SAP.

#### <a name="azdatafactory"></a>Az.DataFactory
* Обновлен пакет SDK ADF для .NET до версии 4.9.0.

#### <a name="azeventhub"></a>Az.EventHub
* Добавлены параметры управляемого удостоверения для командлетов New-AzEventHubNamespace и Set-AzEventHubNamespace.

#### <a name="azfunctions"></a>Az.Functions
* Включена поддержка создания приложений-функций PowerShell 7.0 и Java 11.

#### <a name="azhdinsight"></a>Az.HDInsight
* Включена поддержка перечисления узлов и перезагрузка отдельных узлов кластера HDInsight.

#### <a name="azhealthcareapis"></a>Az.HealthcareApis
* Обновлен пакет SDK до версии 1.1.0.
* Включена поддержка параметров экспорта и управляемого удостоверения.

#### <a name="azmonitor"></a>Az.Monitor
* Исправлен входной параметр объекта для Set-AzActivityLogAlert.
* Исправлен параметр InputObject для Set-AzActionGroup [№ 10868].

#### <a name="aznetwork"></a>Az.Network
* Включена поддержка параметра AddressPrefixType в Remove-AzExpressRouteCircuitConnectionConfig.
* Добавлены новые командлеты для политики Брандмауэра Azure.
    - New-AzFirewallPolicyDnsSetting
    - Включена поддержка полного доменного имени назначения в правилах сети для политики брандмауэра.
* Включена поддержка операций серверного пула адресов:
    - New-AzLoadBalancerBackendAddressConfig
    - New-AzLoadBalancerBackendAddressPool
    - Set-AzLoadBalancerBackendAddressPool
    - Remove-AzLoadBalancerBackendAddressPool
    - Get-AzLoadBalancerBackendAddressPool
* Добавлена проверка имени для New-AzIpGroup.
* Добавлены новые командлеты для политики Брандмауэра Azure.
    - New-AzFirewallPolicyThreatIntelWhitelist
* Обновлены следующие команды для функции: Включена возможность настройки и удаления пользовательских DNS-серверов в шлюзе VPN P2S виртуальной глобальной сети.
    - Обновлен командлет New-AzP2sVpnGateway: добавлен необязательный параметр -CustomDnsServer, чтобы пользователи могли указывать свои DNS-серверы для настройки в шлюзе VPN P2S для использования клиентами с подключением "точка — сеть".
    - Обновлен командлет Update-AzP2sVpnGateway: добавлен необязательный параметр -CustomDnsServer, чтобы пользователи могли указывать свои DNS-серверы для настройки в шлюзе VPN P2S для использования клиентами с подключением "точка — сеть".
* Обновлен командлет Update-AzVpnGateway:
    - добавлен необязательный параметр -BgpPeeringAddress, чтобы клиенты могли указывать пользовательские маршруты BGP для настройки в шлюзе VPN.
* Добавлен новый командлет для сброса состояния маршрутизации ресурса VirtualHub:
    - Reset-AzHubRouter
* Следующие обновления основаны на последнем изменении Swagger для политики брандмауэра:
    - изменены имена для RuleGroup, RuleCollectionGroup и RuleType;
    - включена поддержка коллекций правил NAT политики брандмауэра для поддержки нескольких коллекций правил NAT.
* [Критическое изменение] Добавлен обязательный параметр SourceIpGroup для командлетов New-AzFirewallPolicyApplicationRule и New-AzFirewallPolicyNetworkRule.
* [Критическое изменение] Параметр SourceAddress для командлета New-AzFirewallPolicyApplicationRule сделан обязательным.
* [Критическое изменение] Параметр SourceAddress для командлета New-AzFirewallPolicyApplicationRule сделан обязательным.
* [Критическое изменение] Удалены обязательные параметры: TranslatedAddress и TranslatedPort для командлета New-AzFirewallPolicyNatRuleCollection.
* Добавлены новые командлеты для поддержки Приватного канала в Шлюзе приложений:
    - New-AzApplicationGatewayPrivateLinkConfiguration
    - Get-AzApplicationGatewayPrivateLinkConfiguration
    - New-AzApplicationGatewayPrivateLinkConfiguration
    - Set-AzApplicationGatewayPrivateLinkConfiguration
    - Remove-AzApplicationGatewayPrivateLinkConfiguration
    - New-AzApplicationGatewayPrivateLinkIpConfiguration
* Добавлены новые командлеты для дочернего ресурса HubRouteTables VirtualHub:
    - New-AzVHubRoute
    - New-AzVHubRouteTable
    - Get-AzVHubRouteTable
    - Update-AzVHubRouteTable
    - Remove-AzVHubRouteTable
* Обновлены существующие командлеты для включения поддержки необязательного входного параметра RoutingConfiguration для настраиваемой маршрутизации в виртуальной глобальной сети.
    - New-AzExpressRouteConnection
    - Set-AzExpressRouteConnection
    - New-AzVirtualHubVnetConnection
    - Update-AzVirtualHubVnetConnection
    - New-AzVpnConnection
    - Update-AzVpnConnection
    - New-AzP2sVpnGateway
    - Update-AzP2sVpnGateway

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Исправлена ошибка, из-за которой PSWorkspace не реализует IOperationalInsightsWorkspace [№ 12135].
* Добавлено значение pergb2018 в действительный набор значений параметра Sku в командлете Set-AzOperationalInsightsWorkspace. 
* Добавлен псевдоним FunctionParameters для параметра FunctionParameter:
    - New-AzOperationalInsightsSavedSearch
    - Set-AzOperationalInsightsSavedSearch

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Включена поддержка выборки элементов MAB в Azure Backup.
* Включена поддержка типа диска StandardSSD_LRS в Azure Site Recovery.

#### <a name="azresources"></a>Az.Resources
* Добавлены параметры UsageLocation, GivenName, Surname, AccountEnabled, MailNickname, Mail для PSADUser [№ 10526], [№ 10497].
* Исправлена ошибка, из-за которой параметр -Mail не работает в командлете Get-AzADUser [№ 11981].
* Добавлен параметр -ExcludeChangeType в командлеты Get-AzDeploymentWhatIfResult и Get-AzResourceGroupDeploymentWhatIfResult.
* Добавлен параметр -WhatIfExcludeChangeType в командлеты New-AzDeployment и New-AzResourceGroupDeployment.
* Обновлены командлеты Test-Az*Deployment для отображения улучшенных сообщений об ошибках.
* Исправлено справочное сообщение для параметра -Name в командлетах создания развертывания и командлетах What-If.

#### <a name="azsql"></a>Az.Sql
* Включена поддержка субъекта-службы для командлета настройки администратора Azure Active Directory SQL Server.
* Исправлена ошибка синхронизации в командлетах классификации данных.
* Включена поддержка поиска пользователей по адресу электронной почты в командлете Set-AzSqlServerActiveDirectoryAdministrator [№ 12192].

#### <a name="azstorage"></a>Az.Storage
* Включена поддержка создания учетной записи хранения с помощью RequireInfrastructureEncryption.
    -  New-AzStorageAccount
* Перемещена логика загрузки Azure.Core в Az.Accounts.

#### <a name="azwebsites"></a>Az.Websites
* В командлет Restore-AzDeletedWebApp добавлена защитная мера при удалении созданного веб-приложения, если восстановление завершилось сбоем.
* Добавлены параметры SourceWebApp.Location для командлетов New-AzWebApp и New-AzWebAppSlot.
* Исправлена ошибка, препятствующая изменению параметров контейнера в командлетах Set-AzWebApp и Set-AzWebAppSlot.
* Исправлена ошибка получения SiteConfig, когда параметр -Name не указан для командлета Get-AzWebApp.
* Включена поддержка создания приложений ASP для Linux.
* Добавлены исключения для клонирования в группах ресурсов.

## <a name="420---june-2020"></a>4.2.0 — июнь 2020 г.
#### <a name="azaccounts"></a>Az.Accounts
* Исправлена проблема, из-за которой модуль Az мог пропускать журналы в заданиях службы автоматизации или PowerShell [№ 11492].

#### <a name="azanalysisservices"></a>Az.AnalysisServices
* Обновлена версия сборки командлетов плоскости данных.

#### <a name="azapimanagement"></a>Az.ApiManagement
* Обновлена версия сборки командлетов управления службами.

#### <a name="azbilling"></a>Az.Billing
* Обновлена версия сборки командлетов потребления.

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Реализована поддержка элементов управления PrivateEndpoint и PublicNetworkAccess. 

#### <a name="azdatafactory"></a>Az.DataFactory
* Обновлена версия сборки командлетов фабрики данных версии 2.

#### <a name="azdatashare"></a>Az.DataShare
* Вышла общедоступная версия модуля Az.DataShare.

#### <a name="azdesktopvirtualization"></a>Az.DesktopVirtualization
* Вышла общедоступная версия модуля Az.DesktopVirtualization.

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Пакет SDK обновлен до версии 0.21.0.
* Добавлены дополнительные параметры в следующие командлеты: 
    - New-AzOperationalInsightsSavedSearch
    - Set-AzOperationalInsightsSavedSearch

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Исправлен пример 3 для командлета Start-AzPolicyComplianceScan.

#### <a name="azpowerbiembedded"></a>Az.PowerBIEmbedded
* Обновлена версия сборки командлетов PowerBI.

#### <a name="azprivatedns"></a>Az.PrivateDns
* Исправлено форматирование строки с подробными выходными данными командлета Remove-AzPrivateDnsRecordSet.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Реализована поддержка Azure Site Recovery для создания плана восстановления и репликации между зонами из входного XML-файла.
* Обновлена версия сборки командлетов SiteRecovery и Backup.

#### <a name="azresources"></a>Az.Resources
* Добавлен параметр Tail в командлеты Get-AzDeploymentScriptLog и Save-AzDeploymentScriptLog.
* Отформатировано свойство Output и включено в отображаемые выходные данные командлета Get-AzDeploymentScript.
* Параметр -DeploymentScriptInputObject переименован в -DeploymentScriptObject.
* Исправлена ошибка с отсутствующими именами файлов или целевых объектов в сообщениях командлетов.
* Обновлена версия сборки командлетов диспетчера ресурсов и обработчика тегов.

#### <a name="azsql"></a>Az.Sql
* Добавлен параметр UsePrivateLinkConnection в командлеты New-AzSqlSyncGroup, Update-AzSqlSyncGroup, New-AzSqlSyncMember и Update-AzSqlSyncMember.
* Добавлен параметр SyncMemberAzureDatabaseResourceId в командлеты New-AzSqlSyncMember и Update-AzSqlSyncMember.
* Реализована поддержка поиска гостевых пользователей в командлете для настройки администратора Active Directory в SQL Server Azure.

#### <a name="azstorage"></a>Az.Storage
* Обновлена версия сборки командлетов плоскости данных.

## <a name="410---may-2020"></a>4.1.0 — май 2020 г.
### <a name="highlights-since-the-last-release"></a>Основные сведения о новых возможностях с момента последнего выпуска
* Поддерживаемые версии PowerShell: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7
* Вышла общедоступная версия модуля Az.Functions. 
* Состоялся основной выпуск Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources и Az.Storage.

#### <a name="azaccounts"></a>Az.Accounts
* Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметры AzureSynapseAnalyticsEndpointResourceId и AzureSynapseAnalyticsEndpointSuffix.
* В Az.Accounts добавлены сборки, связанные с Azure.Core. Добавлена поддержка Windows PowerShell 5.1, PowerShell Core 6.2.4 и PowerShell 7+.

#### <a name="azaks"></a>Az.Aks
* Версия API обновлена до 2019-10-01.
* Добавлена возможность создания контейнера Windows в службе Azure Kubernetes.
* Добавлены новые командлеты: New-AzAksNodePool, Update-AzAksNodePool, Remove-AzAksNodePool, Get-AzAksNodePool, Install-AzAksKubectl, Get-AzAksVersion.

#### <a name="azapimanagement"></a>Az.ApiManagement
* В New-AzApiManagement и Set-AzApiManagement параметр -AssignIdentity переименован в -SystemAssignedIdentity.
* В New-AzApiManagement и Set-AzApiManagement добавлен новый параметр -UserAssignedIdentity <строка[]>.
* Командлет Get-AzApiManagementProperty переименован в Get-AzApiManagementNamedValue. Параметр PropertyId переименован в NamedValueId.
* Командлет New-AzApiManagementProperty переименован в New-AzApiManagementNamedValue. Параметр PropertyId переименован в NamedValueId. 
* Командлет Set-AzApiManagementProperty переименован в Set-AzApiManagementNamedValue. Параметр PropertyId переименован в NamedValueId.
* Командлет Remove-AzApiManagementProperty переименован в Remove-AzApiManagementNamedValue. Параметр PropertyId переименован в NamedValueId.
* Добавлен новый командлет Get-AzApiManagementAuthorizationServerClientSecret, а Get-AzApiManagementAuthorizationServer теперь не возвращает секрет клиента.
* Добавлен новый командлет Get-AzApiManagementNamedValueSecretValue, а Get-AzApiManagementNamedValue теперь не возвращает значение секрета.
* Добавлен новый командлет Get-AzApiManagementOpenIdConnectProviderClientSecret, а Get-AzApiManagementOpenIdConnectProvider теперь не возвращает секрет клиента.
* Добавлен новый командлет Get-AzApiManagementSubscriptionKey, а Get-AzApiManagementSubscription теперь не возвращает ключи подписки.
* Добавлен новый командлет Get-AzApiManagementTenantAccessSecret, а Get-AzApiManagementTenantAccess теперь не возвращает ключи.
* Добавлен новый командлет Get-AzApiManagementTenantGitAccessSecret, а Get-AzApiManagementTenantGitAccess теперь не возвращает ключи.

#### <a name="azapplicationinsights"></a>Az.ApplicationInsights
* В New-AzApplicationInsights добавлены параметры RetentionInDays, PublicNetworkAccessForIngestion и PublicNetworkAccessForQuery.
* Создан командлет Update-AzApplicationInsights.
* Созданы командлеты для связанной учетной записи хранения.

#### <a name="azbatch"></a>Az.Batch
* В командлеты Az.Batch добавлена поддержка пакетов SDK Microsoft.Azure.Batch версии 13.0.0 и SDK Microsoft.Azure.Management.Batch версии 9.0.0.
* Теперь в New-AzBatchCertificate можно выбрать тип добавляемого сертификата с помощью нового параметра -CertificateKind.
* В PSApplication удалено свойство ApplicationPackages.
  - Отдельные пакеты в приложении теперь можно извлечь с помощью Get-AzBatchApplicationPackage. Пример: Get-AzBatchApplication -AccountName моя_учетная_запись -ResourceGroupName моя_группа_ресурсов -ApplicationId мое_приложение.
* При создании пула с помощью New-AzBatchPool свойство VirtualMachineImageId элемента PSImageReference теперь может ссылаться только на образ из Общей коллекции образов.
* При создании пула с помощью New-AzBatchPool пул можно подготовить без общедоступного IP-адреса, используя новое свойство PublicIPAddressConfiguration элемента PSNetworkConfiguration.
  - Свойство PublicIPs элемента PSNetworkConfiguration было передано элементу PSPublicIPAddressConfiguration. Это свойство можно указать, только если параметру IPAddressProvisioningType присвоено значение UserManaged.

#### <a name="azcompute"></a>Az.Compute
* В командлет Update-AzVM добавлен параметр HostId.
* Обновлена справочная документация по командлетам New-AzVMConfig, New-AzVmssConfig, Update-AzVmss, Set-AzVMOperatingSystem и Set-AzVmssOsProfile.
* Критические изменения
    - Параметр FilterExpression удален из командлета Get-AzVMImage.
    - Параметр AssignIdentity удален из командлетов New-AzVmssConfig, New-AzVMConfig и Update-AzVM.
    - Параметр AutomaticRepairMaxInstanceRepairsPercent удален из командлетов New-AzVmssConfig и Update-AzVmss.
    - Свойства AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus и VirtualMachineScaleSetsColocationStatus удалены из ProximityPlacementGroup.
    - Свойство MaxInstanceRepairsPercent удалено из AutomaticRepairsPolicy.
    - Типы AvailabilitySets, VirtualMachines и VirtualMachineScaleSets изменены с IList<SubResource> на IList<SubResourceWithColocationStatus>.
* Уточнено описание командлета Get-AzVM. 

#### <a name="azdatafactory"></a>Az.DataFactory
* Добавлена поддержка операций CRUD для свойств среды выполнения потока данных в управляемой среде выполнения интеграции.

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Добавлены новые командлеты для создания, обновления, извлечения и удаления объекта обработчика правил Front Door.
* Добавлены вспомогательные командлеты для создания объекта обработчика правил Front Door.
* Добавлена ссылка обработчика правил на объект правила маршрутизации Front Door.
* Добавлены параметры Приватного канала на серверный объект Front Door.

#### <a name="azfunctions"></a>Az.Functions
* Вышла общедоступная версия модуля Az.Functions.

#### <a name="azhdinsight"></a>Az.HDInsight
* Добавлена поддержка шифрования управляемых клиентом ключей.

#### <a name="azhealthcareapis"></a>Az.HealthcareApis
* Политики доступа для текущего субъекта теперь не используются по умолчанию.

#### <a name="aziothub"></a>Az.IotHub
* Добавлен командлет для вызова запроса в центре Интернета вещей для получения данных с помощью SQL-подобного языка.
* Устранена проблема, когда с помощью Add-AzIotHubDevice не удавалось создать устройство с поддержкой IoT Edge без дочерних устройств (№ 11597).
* Добавлен командлет для создания маркера SAS для Центра Интернета вещей, устройства или модуля.
* Добавлен командлет для вызова запроса метрик конфигурации.
* Появилась возможность управлять автоматическим развертыванием IoT Edge в большом масштабе. Ниже перечислены новые командлеты:
    - Add-AzIotHubDeployment;
    - Get-AzIotHubDeployment;
    - Remove-AzIotHubDeployment;
    - Set-AzIotHubDeployment.
* Добавлен командлет для вызова запроса метрик развертывания IoT Edge.
* Добавлен командлет для применения содержимого конфигурации к указанному пограничному устройству.

#### <a name="azkeyvault"></a>Az.KeyVault
* Удалены два псевдонима: New-AzKeyVaultCertificateAdministratorDetails и New-AzKeyVaultCertificateOrganizationDetails.
* При создании хранилища ключей обратимое удаление включено по умолчанию.
* Можно задать правила сети, чтобы при создании хранилища ключей управлять доступом из определенных сетевых расположений.
* Добавлена возможность создания собственных ключей (BYOK).
    - С помощью Add-AzKeyVaultKey теперь можно создавать ключ обмена ключами.
    - С помощью Get-AzKeyVaultKey можно скачать открытый ключ в формате PEM.
* Обновлен раздел KeyOps справочной документации по Add-AzKeyVaultKey.

#### <a name="azmonitor"></a>Az.Monitor
* Исправлена ошибка Set-AzDiagnosticSettings, когда политика хранения не применялась ко всем категориям (№ 11589).
* Добавлена поддержка критериев доступности веб-теста для оповещения метрики версии 2.
    - В New-AzMetricAlertRuleV2Criteria добавлена возможность создавать критерии доступности веб-теста.
    - Add-AzMetricAlertRuleV2 теперь поддерживает новые критерии доступности веб-теста.
* В PSLogProfile исправлено избыточное определение RetentionPolicy (№ 7608).
* В PSEventData удалены избыточные определения свойств (№ 11353).
* Командлет Get-AzLog переименован в Get-AzActivityLog.

#### <a name="aznetwork"></a>Az.Network
* Добавлен атрибут критического изменения, сообщающий о том, что поведение зоны по умолчанию будет изменено.
    - New-AzPublicIpAddress;
    - New-AzPublicIpPrefix;
    - New-AzLoadBalancerFrontendIpConfig.
* Добавлена поддержка нового ресурса верхнего уровня SecurityPartnerProvider.
    - Добавлены новые командлеты:
        - New-AzSecurityPartnerProvider;
        - Remove-AzSecurityPartnerProvider;
        - Get-AzSecurityPartnerProvider;
        - Set-AzSecurityPartnerProvider.
* В PSPrivateLinkResource добавлен параметр RequiredZoneNames, а в PSPrivateEndpointConnection — GroupId.
* Исправлен неправильный тип параметра SuccessThresholdRoundTripTimeMs для New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.
* В командлетах VirtualWan аргументу AllowVnetToVnetTraffic теперь по умолчанию присвоено значение True.
    - New-AzVirtualWan;
    - Update-AzVirtualWan.
* Добавлены новые командлеты для поддержки группы зон DNS для частной конечной точки.
    - New-AzPrivateDnsZoneConfig;
    - Get-AzPrivateDnsZoneGroup;
    - New-AzPrivateDnsZoneGroup;
    - Set-AzPrivateDnsZoneGroup;
    - Remove-AzPrivateDnsZoneGroup.
* В AzureFirewall добавлены параметры DNSEnableProxy, DNSRequireProxyForNetworkRules и DNSServers.
* В AzureFirewall добавлены параметры EnableDnsProxy, DnsProxyNotRequiredForNetworkRule и DnsServer.
    - Обновлен командлет:
        - New-AzFirewall.

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Обновлен устаревший код для использования новых пакетов SDK.
* Из-за устаревших API-интерфейсов удалены следующие командлеты:
    - Get-AzOperationalInsightsSavedSearchResult (псевдоним Get-AzOperationalInsightsSavedSearchResults);
    - Get-AzOperationalInsightsSearchResult (псевдоним Get-AzOperationalInsightsSearchResults);
    - Get-AzOperationalInsightsLinkTarget (псевдоним Get-AzOperationalInsightsLinkTargets).
* В Set-AzOperationalInsightsWorkspace и New-AzOperationalInsightsWorkspace добавлены новые параметры.
* Созданы командлеты для связанной учетной записи хранения.
* Созданы командлеты для кластеров и связанной службы.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* В Azure Site Recovery добавлена поддержка защиты поставщика Azure для групп размещения виртуальных машин Azure близкого взаимодействия.
* В Azure Site Recovery добавлена поддержка репликации из зоны в зону.
* В Azure Backup добавлена поддержка долгосрочного хранения для точек восстановления общей папки Azure.
* В выходные данные командлета Get-AzRecoveryServicesBackupItem добавлены свойства исключения диска, добавленного в Azure Backup.
* Добавлена частная конечная точка для файла учетных данных хранилища для службы Site Recovery.

#### <a name="azresources"></a>Az.Resources
* Добавлено предупреждение о задержке представления при создании определения роли.
* Командлеты политики теперь выводят строго типизированные объекты.
* Из командлета Get-AzResourceLock удален параметр -TenantLevel (№ 11335).
* Исправлена ошибка с Remove-AzResourceGroup -Id ResourceId (№ 9882).
* Добавлен новый командлет для получения результатов анализа гипотетических вариантов из шаблона ARM в области группы ресурсов: Get-AzDeploymentResourceGroupWhatIfResult.
* Добавлен новый командлет для получения результатов анализа гипотетических вариантов из шаблона ARM в области подписки: Get-AzDeploymentWhatIfResult.
   - Alias: Get-AzSubscriptionDeploymentWhatIf.
* Переопределены параметры -WhatIf и -Confirm для New-AzDeployment и New-AzResourceGroupDeployment для использования результатов анализа гипотетических вариантов из шаблона ARM.
* В командлеты развертывания добавлено сообщение об устаревании для параметра ApiVersion.
* Добавлена возможность отображения улучшенных сообщений об ошибках при развертывании.
* Добавлена возможность регистрации correlationId для сбоев развертывания.
* В выходные данные скрипта развертывания добавлено свойство error.
* Пакет NuGet Microsoft.Azure.Management.ResourceManager обновлен до версии 3.7.1-preview.
* Удаленные определенные тестовые случаи как свойство error в DeploymentValidateResult были изменены на доступные только для чтения из пакета NuGet версии 3.7.1-preview.
* Добавлен GenericResourceExpanded из пакета SDK ResourceManager версии 3.7.1-preview.
* Добавлена поддержка тегов для всех командлетов Get для развертывания, а также для следующих командлетов:
    - New-AzDeployment;
    - New-AzManagementGroupDeployment;
    - New-AzResourceGroupDeployment;
    - New-AzTenantDeployment.

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Исправлена ошибка при добавлении сертификата с помощью параметра -SecretIdentifier, когда возвращался неправильный отпечаток сертификата.

#### <a name="azsql"></a>Az.Sql
* Оптимизирована работа следующих командлетов:
    - Set-AzSqlDatabaseSensitivityClassification;
    - Set-AzSqlInstanceDatabaseSensitivityClassification;
    - Remove-AzSqlDatabaseSensitivityClassification;
    - Remove-AzSqlInstanceDatabaseSensitivityClassification;
    - Enable-AzSqlDatabaseSensitivityRecommendation;
    - Enable-AzSqlInstanceDatabaseSensitivityRecommendation;
    - Disable-AzSqlDatabaseSensitivityRecommendation;
    - Disable-AzSqlInstanceDatabaseSensitivityRecommendation.
* Удалена проверка на стороне клиента параметра RetentionDays из командлета Set-AzSqlDatabaseBackupShortTermRetentionPolicy.
* Добавлен аудит учетной записи хранения в виртуальной сети. Исправлена ошибка при создании роли участника данных BLOB-объектов хранилища.

#### <a name="azstorage"></a>Az.Storage
* В командлет Get-AzStorageAccount добавлен параметр -AsJob.
* Параметр KeyVersion теперь является необязательным при изменении учетной записи хранения с помощью KeyvaultEncryption, что обеспечивает поддержку автоматической смены ключа.
    - Set-AzStorageAccount
* Исправлена ошибка при удалении каталога файлов Azure с конвейером.
    - Remove-AzStorageDirectory.
* Исправлена ошибка 9880. Значение DefaultAction для NetWorkRule приведено в соответствие со Swagger.
    - Update-AzStorageAccountNetworkRuleSet;
    - Get-AzStorageAccountNetworkRuleSet.
* Исправлена ошибка 11624. При добавлении NetworkRules дублирующиеся правила пропускаются, чтобы не происходил сбой сервера.
    - Add-AzStorageAccountNetworkRule.
* Версия пакета SDK Microsoft.Azure.Cosmos.Table обновлена до 1.0.7.
* Добавлено предупреждающее сообщение, напоминающее пользователю о необходимости повторного вывода списка с помощью ContinuationToken, когда в списке элементов Data Lake 2-го поколения возвращается только часть элементов.
    - Get-AzDataLakeGen2ChildItem
* Добавлена возможность создания или изменения учетной записи хранения с использованием проверки подлинности Active Directory для Файлов Azure.
    -  New-AzStorageAccount
    -  Set-AzStorageAccount
* Добавлена возможность создания и просмотра ключей Kerberos учетной записи хранения.
    -  New-AzStorageAccountKey;
    -  Get-AzStorageAccountKey.
* Добавлена возможность отработки отказа для учетной записи хранения.
    - Invoke-AzStorageAccountFailover.
* Обновлена справка по Get-AzStorageBlobCopyState.
* Обновлена справка по Get-AzStorageFileCopyState и Start-AzStorageBlobCopy.
* Появилась интегрированная клиентская библиотека хранилища версии 12 для командлетов очередей и файлов.
* Тип выходных данных изменен с CloudFile на AzureStorageFile. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.
    - Get-AzStorageFile;
    - Remove-AzStorageFile;
    - Get-AzStorageFileContent;
    - Set-AzStorageFileContent;
    - Start-AzStorageFileCopy.
* Тип выходных данных изменен с CloudFileDirectory на AzureStorageFileDirectory. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.
    - New-AzStorageDirectory;
    - Remove-AzStorageDirectory.
* Тип выходных данных изменен с CloudFileShare на AzureStorageFileShare. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.
    - Get-AzStorageShare;
    - New-AzStorageShare;
    - Remove-AzStorageShare.
* Тип выходных данных изменен с FileShareProperties на AzureStorageFileShare. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.
    - Set-AzStorageShareQuota.

#### <a name="aztrafficmanager"></a>Az.TrafficManager
* Исправлено неправильное имя профиля в подробных выходных данных DisableAzureTrafficManagerEndpoint.

#### <a name="azwebsites"></a>Az.Websites
* Исправлена опечатка в справке по Update-AzWebAppAccessRestrictionConfig.

## <a name="380---april-2020"></a>3.8.0 — апрель 2020 г.
### <a name="highlights-since-the-last-release"></a>Основные сведения о новых возможностях с момента последнего выпуска
* Версии PowerShell, которые поддерживает Az.Storage: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7

#### <a name="azaccounts"></a>Az.Accounts
* Обновлен URL-адрес опроса Azure PowerShell в Resolve-AzError [11507].

#### <a name="azapimanagement"></a>Az.ApiManagement
* Добавлено уведомление о критическом изменении для изменения выходных данных командлетов, выполняющих действия с файлами в Azure, в следующем выпуске.
* Обновлена документация для Set-AzApiManagementGroup с указанием параметра GroupId.

#### <a name="azcdn"></a>Az.Cdn
* Исправлено отображение ценовой категории (SKU), связанной с ChinaCDN.

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Включена поддержка Identity, Encryption, UserOwnedStorage.

#### <a name="azcompute"></a>Az.Compute
* Добавлен командлет Set-AzVmssOrchestrationServiceState.
* Get-AzVmss с параметром -InstanceView отображает состояния OrchestrationService.

#### <a name="aziothub"></a>Az.IotHub
* Реализовано управление конфигурацией двойника устройства Интернета вещей. Новые командлеты:
    - Get-AzIotHubDeviceTwin
    - Update-AzIotHubDeviceTwin
* Добавлен командлет для вызова прямого метода на устройстве в Центре Интернета вещей.
* Реализовано управление конфигурацией двойника модуля устройства Интернета вещей. Новые командлеты:
    - Get-AzIotHubModuleTwin
    - Update-AzIotHubModuleTwin
* Реализовано управление конфигурацией автоматического управления устройствами в центре Интернета вещей в большом масштабе. Ниже перечислены новые командлеты:
    - Add-AzIotHubConfiguration
    - Get-AzIotHubConfiguration
    - Remove-AzIotHubConfiguration
    - Set-AzIotHubConfiguration
* Добавлен командлет для вызова метода периферийного модуля в Центре Интернета вещей.

#### <a name="azkeyvault"></a>Az.KeyVault
* Добавлен новый командлет Update-AzKeyVault, который может включать защиту от обратимого удаления и очистки в хранилище.
* Включена поддержка Microsoft.PowerShell.SecretManagement [11178].
* Исправлена ошибка в примерах Remove-AzKeyVaultManagedStorageSasDefinition [11479].
* Включена поддержка частной конечной точки.

#### <a name="azmaintenance"></a>Az.Maintenance
* Опубликована версия выпуска командлетов обслуживания для общедоступной версии.

#### <a name="azmonitor"></a>Az.Monitor
* Добавлены командлеты для области приватных каналов:
    - Get-AzInsightsPrivateLinkScope
    - Remove-AzInsightsPrivateLinkScope
    - New-AzInsightsPrivateLinkScope
    - Update-AzInsightsPrivateLinkScope
    - Get-AzInsightsPrivateLinkScopedResource
    - New-AzInsightsPrivateLinkScopedResource
    - Remove-AzInsightsPrivateLinkScopedResource

#### <a name="aznetwork"></a>Az.Network
* Обновлены командлеты для включения подключения на частном IP-адресе для шлюза виртуальной сети:
    - New-AzVirtualNetworkGateway
    - Set-AzVirtualNetworkGateway
    - New-AzVirtualNetworkGatewayConnection
    - Set-AzVirtualNetworkGatewayConnection
* Обновлены командлеты для включения шлюзов LocalNetworkGateways и сайтов VpnSites на основе FQDN:
    - New-AzLocalNetworkGateway
    - New-AzVpnSiteLink
* Включена поддержка семейства адресов IPv6 в ExpressRouteCircuitConnectionConfig (Global Reach).
    - Добавлен командлет Set-AzExpressRouteCircuitConnectionConfig.
        - Позволяет выполнять настройку всех существующих свойств, включая IPv6CircuitConnectionProperties.
    - Обновлен командлет Add-AzExpressRouteCircuitConnectionConfig.
        - Добавлен еще один необязательный параметр AddressPrefixType для указания семейства адресов префикса адреса.
* Обновлены командлеты для включения параметра времени ожидания для обнаружения неиспользуемых одноранговых узлов (DPD) в подключениях шлюзов виртуальных сетей.
    - New-AzVirtualNetworkGatewayConnection;
    - Set-AzVirtualNetworkGatewayConnection.

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Добавлен командлет Start-AzPolicyComplianceScan для запуска проверок соответствия политикам.
* Добавлены версии определения политики, определения набора и назначения в выходные данные командлета Get-AzPolicyState.

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Улучшено форматирование и наглядность кода в примерах New-AzServiceFabricCluster.

#### <a name="azsql"></a>Az.Sql
* Добавлены командлеты Get-AzSqlInstanceOperation и Stop-AzSqlInstanceOperation.
* Включен аудит учетной записи хранения в виртуальной сети.

#### <a name="azstorage"></a>Az.Storage
* Добавлено уведомление о критическом изменении для изменения выходных данных командлетов, выполняющих действия с файлами в Azure, в следующем выпуске.
* Включена поддержка новых имен SKU StandardGZRS, StandardRAGZRS при создании или обновлении учетной записи хранения.
    - New-AzStorageAccount
    - Set-AzStorageAccount
* Добавлена поддержка DataLake 2-го поколения.
    - New-AzDataLakeGen2Item
    - Get-AzDataLakeGen2Item
    - Get-AzDataLakeGen2ChildItem
    - Move-AzDataLakeGen2Item
    - Set-AzDataLakeGen2ItemAclObject
    - Update-AzDataLakeGen2Item
    - Get-AzDataLakeGen2ItemContent
    - Remove-AzDataLakeGen2Item

## <a name="0100-preview---april-2020"></a>0.10.0-preview — апрель 2020 г.
### <a name="general"></a>Общие сведения
* Модуль Az стали доступными в предварительной версии в Azure Stack Hub. Это обеспечивает кросс-платформенную совместимость с Linux и macOs. Azure Stack Hub теперь поддерживает PowerShell Core с модулями Az (см. [дополнительные сведения](https://aka.ms/az4AzureStack))
* Модули Az поддерживают профиль 2019-03-01-hybrid:
  - Az.Billing
  - Az.Compute
  - Az.DataBoxEdge
  - Az.EventHub
  - Az.IotHub
  - Az.KeyVault
  - Az.Monitor
  - Az.Network
  - Az.Resources
  - Az.Storage
  - Az.Websites
* В PowerShell появились три новых модуля Az, которые работают с Azure Stack Hub: Az.Databox, Az.IotHub и Az.EventHub.
* Команды остаются прежними же за исключением незначительных изменений, таких как изменение AzureRM на Az.
* См. обновленную ссылку на документацию по [PowerShell для Azure Stack Hub](https://aka.ms/InstallASHPowerShell)

## <a name="370---march-2020"></a>3.7.0 — март 2020 г.
#### <a name="azaccounts"></a>Az.Accounts
* Исправлено исключение NullReferenceException командлетов Get-AzTenant/Get-AzDefault/Set-AzDefault, если вход не выполнен [10292]

#### <a name="azcompute"></a>Az.Compute
* Добавлены следующие параметры к командлету New-AzDiskConfig:
    - DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference
* Разрешено свойство Encryption для параметра Target командлета New-AzGalleryImageVersion.
* Исправлена проблема с tempDisk для командлетов Set-AzVmss -Reimage и Invoke-AzVMReimage. [11354]
* Добавлена поддержка нового расширения SAP для указанных ниже командлетов
    - Set-AzVMAEMExtension
    - Get-AzVMAEMExtension
    - Remove-AzVMAEMExtension
    - Update-AzVMAEMExtension
* Исправлены ошибки в примерах справки
* Показано точное строковое значение в табличном формате для свойства PowerState виртуальной машины.
* New-AzVmssConfig: исправлена сериализация свойства AutomaticRepairs, если параметр SinglePlacementGroup отключен. [11257]

#### <a name="azdatafactory"></a>Az.DataFactory
* Пакет SDK ADF для .NET обновлен до версии 4.8.0.
* Добавлены необязательные параметры для команды Invoke-AzDataFactoryV2Pipeline для поддержки повторного запуска.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Добавлено описание критического изменения для Export-AzDataLakeStoreItem и Import-AzDataLakeStoreItem.
* Добавлен параметр кодирования байтов для New-AzDataLakeStoreItem, Add-AzDAtaLakeStoreItemContent и Get-AzDAtaLakeStoreItemContent.

#### <a name="azhdinsight"></a>Az.HDInsight
* Добавлена поддержка указания минимальной поддерживаемой версии TLS при создании кластера.

#### <a name="aziothub"></a>Az.IotHub
* Добавлена поддержка для управления распределенными параметрами на отдельных устройствах. Ниже перечислены новые командлеты.
    - Get-AzIotHubDistributedTracing
    - Set-AzIotHubDistributedTracing

#### <a name="azkeyvault"></a>Az.KeyVault
* Добавлены атрибуты критических изменений для New-AzKeyVault.

#### <a name="azmonitor"></a>Az.Monitor
* Обновлена документация для New-AzScheduledQueryRuleLogMetricTrigger.

#### <a name="aznetwork"></a>Az.Network
* Обновлены командлеты для поддержки подключений VirtualHubVnetConnections между клиентами
    - New-AzVirtualHubVnetConnection
    - Update-AzVirtualHubVnetConnection
    - New-AzVirtualHub
    - Update-AzVirtualHub
* Удалена зависимость пакета SDK для управления SQL.

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Улучшены сообщения об ошибках.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* В Azure Site Recovery реализована поддержка повторной защиты и обновлены свойства зашифрованных виртуальных машин диска Azure.
* Добавлена возможность мониторинг аварийного восстановления для свойств VmwareToAzure в Azure Site Recovery.
* В Azure Backup реализована поддержка повторного обновления политики для элементов с ошибками.
* В Azure Backup реализована поддержка параметров исключения диска во время резервного копирования и восстановления.
* В Azure Backup реализована поддержка восстановления нескольких файлов или папок в AzureFileShare
* В Azure Backup реализована поддержка указанной пользователем группы Resourcegroup при обновлении политики IaasVM.

#### <a name="azresources"></a>Az.Resources
* Исправлена команда Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType для использования фактической версии apiVersion ресурсов (а не версии apiVersion по умолчанию) [11267].
* Добавлена возможность регистрации correlationId для сценариев с ошибками.
* Незначительно изменена документация по Get-AzResourceLock. Добавлен пример.
* Экранирована одинарная кавычка в значении параметра Get-AzADUser [11317].
* Добавлены новые командлеты для сценариев развертывания (Get-AzDeploymentScript, Get-AzDeploymentScriptLog, Save-AzDeploymentScriptLog, Remove-AzDeploymentScript).

#### <a name="azsql"></a>Az.Sql
* Добавлен параметр вторичной реплики для чтения для командлета Invoke-AzSqlDatabaseFailover.
* Добавлен командлет Disable-AzSqlServerActiveDirectoryOnlyAuthentication.
* Сохранен приоритет конфиденциальности при классификации столбцов в базе данных.

#### <a name="azsupport"></a>Az.Support
* Модуль Az.Support стал общедоступным.

#### <a name="azwebsites"></a>Az.Websites
* Реализована поддержка работы с правилами маршрутизации трафика веб-приложения через указанные ниже командлеты
    - Get-AzWebAppTrafficRouting
    - Update-AzWebAppTrafficRouting
    - Add-AzWebAppTrafficRouting
    - Remove-AzWebAppTrafficRouting

## <a name="361---march-2020"></a>3.6.1 — март 2020 г.
#### <a name="azaccounts"></a>Az.Accounts
* Открытие страницы опроса Azure PowerShell в Send-Feedback [11020].
* Отображение URL-адреса опроса Azure PowerShell в Resolve-Error [11021].
* Добавлена версия Az в UserAgent.

#### <a name="azapimanagement"></a>Az.ApiManagement
* Включена поддержка получения и настройки личного домена в конечной точке DeveloperPortal [11007].
* Export-AzApiManagementApi: включена поддержка скачивания определения API в формате JSON [9987].
* Import-AzApiManagementApi: включена поддержка импорта определения OpenApi 3.0 из документа JSON.
* New-AzApiManagementIdentityProvider и Set-AzApiManagementIdentityProvider: включена поддержка настройки входа арендатора для поставщика AAD B2C [9784].

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Добавлена ссылка на System.Buffers явным образом в CSPROJ и PSD1.

#### <a name="aziothub"></a>Az.IotHub
* Добавлена возможность управления устройствами в Центре Интернета вещей. Ниже перечислены новые командлеты.
    - Add-AzIotHubDevice
    - Get-AzIotHubDevice
    - Remove-AzIotHubDevice
    - Set-AzIotHubDevice
* Включена поддержка управления модулями в целевом устройстве Интернета вещей в Центре Интернета вещей. Ниже перечислены новые командлеты.
    - Add-AzIotHubModule
    - Get-AzIotHubModule
    - Remove-AzIotHubModule
    - Set-AzIotHubModule
* Добавлен командлет для получения строки подключения целевого устройства Интернета вещей в центре Интернета вещей.
* Добавлен командлет для получения строки подключения модуля на целевом устройстве Интернета вещей в центре Интернета вещей.
* Включена поддержка для получения или настройки родительского устройства для устройства Интернета вещей. Ниже перечислены новые командлеты.
    - Get-AzIotHubDeviceParent
    - Set-AzIotHubDeviceParent
* Включена поддержка управления связью "родители — потомки" устройства.

#### <a name="azmonitor"></a>Az.Monitor
* Исправлено выходное значение для Get-AzMetricDefinition [9714].

#### <a name="aznetwork"></a>Az.Network
* Обновлен пакет SDK для управления SQL.
* Исправлена проблема с разницей в именовании в классе PrivateLinkServiceConnectionState.
    - Сопоставление ActionsRequired с ActionRequired.
* Добавление PublicNetworkAccess в команды New-AzSqlServer и Set-AzSqlServer.

#### <a name="azresources"></a>Az.Resources
* Исправлена ошибка пустой ссылки в Get-AzRoleAssignment.
* Параметры -Force и -PassThru помечены необязательными в Remove-AzADGroup [10849].
* Исправлена ошибка, из-за которой MailNickname не возвращается в Remove-AzADGroup [11167].
* Исправлена ошибка, из-за которой операция канала Remove-AzADGroup не работает [11171].
* Исправлена ошибка с пустой ссылкой в GetAzureRoleAssignmentCommand.
* Добавлено критическое изменение атрибутов для будущих изменений командлетов политик.
* Обновлена команда Get-AzResourceGroup для выполнения фильтрации тегов группы ресурсов на стороне сервера.
* Расширены командлеты Tag для включения поддержки параметра -ResourceId.
    - Get-AzTag -ResourceId
    - New-AzTag -ResourceId
    - Remove-AzTag -ResourceId
* Добавлен новый командлет Tag.
    - Update-AzTag -ResourceId
* Предоставляется ScopedDeployment из пакета SDK 3.3.0.

#### <a name="azsql"></a>Az.Sql
* Добавление PublicNetworkAccess в команды New-AzSqlServer и Set-AzSqlServer.
* Включена поддержка конфигурации резервного копирования долгосрочного хранения для управляемых баз данных.
    - Получение или настройка политики LTR в управляемой базе данных.
    - Получение резервных копий LTR по управляемой базе данных, управляемому экземпляру или расположению.
    - Удаление резервной копии LTR.
    - Восстановление резервной копии LTR для создания новой управляемой базы данных.
* Добавление MinimalTlsVersion в New-AzSqlServer и Set-AzSqlServer.
* Добавление MinimalTlsVersion в New-AzSqlInstance и Set-AzSqlInstance.
* Обновлена версия пакета SDK для SQL для Az.Network.

#### <a name="azstorage"></a>Az.Storage
* Включена поддержка AllowProtectedAppendWrite в ImmutabilityPolicy.
    - Set-AzRmStorageContainerImmutabilityPolicy
* Добавлено предупреждение о критическом изменении для изменения типа AzureStorageTable в следующем выпуске.
    - New-AzStorageTable
    - Get-AzStorageTable

#### <a name="azwebsites"></a>Az.Websites
* Добавлен параметр Tag для New-AzAppServicePlan и Set-AzAppServicePlan.
* Завершение выполнения командлета, если при добавлении личного домена на веб-сайт возникает исключение.
* Включена поддержка выполнения операций для Служб приложений, которые находятся не в той же группе ресурсов, что и план службы приложений.
* Применение ограничения доступа к WebApp/Function в разных группах ресурсов.
* Исправлена ошибка с указанием пользовательских имен узлов для WebAppSlots.

## <a name="350---february-2020"></a>3.5.0 — февраль 2020 г.
### <a name="highlights-since-the-last-major-release"></a>Основные возможности с момента последнего основного выпуска
* Обновлены данные телеметрии на стороне клиента.
* В Az.IotHub добавлены командлеты для управления устройствами.
* В Az.SqlVirtualMachine добавлены командлеты для прослушивателя группы доступности.

#### <a name="azaccounts"></a>Az.Accounts
* В данные телеметрии на стороне клиента добавлены такие сведения, как идентификатор подписки, идентификатор арендатора и время выполнения.

#### <a name="azautomation"></a>Az.Automation
* Исправлена опечатка в примере 1 в справочной документации по New-AzAutomationSoftwareUpdateConfiguration.

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Обновлен пакет SDK до версии 7.0.
* Улучшено сообщение об ошибке, которое появляется, если ответы сервера не содержат текст.

#### <a name="azcompute"></a>Az.Compute
* Разрешено использовать пустое значение для ProximityPlacementGroupId во время обновления.

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Добавлен командлет для получения определений управляемых правил, которые могут использоваться в WAF.

#### <a name="aziothub"></a>Az.IotHub
* Добавлена возможность управления устройствами в Центре Интернета вещей. Ниже перечислены новые командлеты.
    - Add-AzIotHubDevice
    - Get-AzIotHubDevice
    - Remove-AzIotHubDevice
    - Set-AzIotHubDevice

#### <a name="azkeyvault"></a>Az.KeyVault
* Устранен дублирующийся текст для Add-AzKeyVaultKey.md.

#### <a name="azmonitor"></a>Az.Monitor
* Исправлено описание командлета Get-AzLog.
* В команду New-AzMetricAlertRuleV2 добавлен новый параметр ActionGroupId.
    - Пользователь может предоставить ActionGroupId(string) или ActionGorup(ActivityLogAlertActionGroup).

#### <a name="aznetwork"></a>Az.Network
* Добавлен еще один параметр -EnableProxyProtocol для командлета New-AzPrivateLinkService.
* Исправлен пример FilterData в Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.
* Добавлен пример Packet Capture для всех внутренних и внешних пакетов в Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.
* Добавлена поддерживаемая политика Брандмауэра Azure в брандмауэрах виртуальной сети.
    - Новые командлеты не добавлены. Снято ограничение политики брандмауэра в брандмауэрах виртуальных сетей.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Добавлена возможность восстановления в виде файлов для Баз данных SQL.

#### <a name="azresources"></a>Az.Resources
* Выполнен рефакторинг командлетов развертывания шаблона.
    - Добавлены новые командлеты для управления развертываниями в группе управления: *-AzManagementGroupDeployment.
    - Добавлены новые командлеты для управления развертываниями в области арендатора: *-AzTenantDeployment.
    - Выполнен рефакторинг командлетов *-AzDeployment для работы в области подписки.
    - Созданы псевдонимы *-AzSubscriptionDeployment для командлетов *-AzDeployment.
* Исправлен командлет Update-AzADApplication, когда параметр AvailableToOtherTenants не задан.
* Удален набор параметров ApplicationObjectWithoutCredentialParameterSet, чтобы предотвратить возникновение AmbiguousParameterSetException.
* Повторно созданы файлы справки.

#### <a name="azsql"></a>Az.Sql
* Добавлена возможность восстановления точки во времени между подписками в Управляемых экземплярах.
* Добавлена возможность изменения существующего поколения оборудования Управляемого экземпляра SQL.
* Исправлены примеры справки Update-AzSqlServerVulnerabilityAssessmentSetting: выходные данные параметра и свойства — EmailAdmins.

#### <a name="azsqlvirtualmachine"></a>Az.SqlVirtualMachine
* Добавлены командлеты для прослушивателя группы доступности.

#### <a name="azstoragesync"></a>Az.StorageSync
* В командлете Invoke-AzStorageSyncCompatibilityCheck обновлены поддерживаемые наборы символов.

## <a name="340---february-2020"></a>3.4.0 — февраль 2020 г.
### <a name="highlights-since-the-last-major-release"></a>Основные возможности с момента последнего основного выпуска
* Выпущена первоначальная версия 0.1.0 Az.CosmosDB
* Добавлена поддержка Az.Network ConnectionMonitor V2

#### <a name="azaccounts"></a>Az.Accounts
* Отключить автоматическое сохранение контекста, если AzureRmContext.json недоступен
* Обновление ссылки на Azure Powershell Common до предварительной версии 1.3.5

#### <a name="azapimanagement"></a>Az.ApiManagement
* **Get-AzApiManagementApiSchema** Исправлено получение схемы Open-API, связанной с API https://github.com/Azure/azure-powershell/issues/10626
* **New-AzApiManagementProduct*** и **Set-AzApiManagementProduct**
  - Исправить документацию для https://github.com/Azure/azure-powershell/issues/10472
* **Set-AzApiManagementApi** Добавлен пример, показывающий, как обновить ServiceUrl с помощью командлета

#### <a name="azcompute"></a>Az.Compute
* Ограничение числа состояний виртуальных машин до 100, чтобы избежать регулирования при выполнении Get-AzVM-Status без имени виртуальной машины.
* Добавление обновления командлета -AzDiskEncryptionSet
* Добавление параметров EncryptionType и DiskEncryptionSetId в следующие командлеты:
    - New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig
* Добавление параметра ColocationStatus в командлет Get-AzProximityPlacementGroup.

#### <a name="azdatafactory"></a>Az.DataFactory
* Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.7.0.

#### <a name="azdeploymentmanager"></a>Az.DeploymentManager
* Добавляет операции LIST для ресурсов
* Добавляет возможность выполнения операций на этапах Проверки работоспособности

#### <a name="azhdinsight"></a>Az.HDInsight
* Исправление ошибки в документе New-AzHDInsightCluster.

#### <a name="azkeyvault"></a>Az.KeyVault
* Добавление Псевдонимов имени в атрибут VaultName, чтобы Remove-AzureKeyVault соответствовал New-AzureKeyVault.

#### <a name="aznetwork"></a>Az.Network
* В Set-AzNetworkWatcherConfigFlowLog.md добавлен новый пример для демонстрации сценария отключения Аналитики трафика.
* Добавление поддержки назначения IP-конфигурации для брандмауэра Azure — выделенная подсеть и общедоступный IP-адрес, которые брандмауэр будет использовать для управления трафиком
    - Обновлен командлет New-AzFirewall:
        - добавлен параметр — ManagementPublicIpAddress (необязательный), который принимает объект общедоступного IP-адреса
        - Добавлен метод SetManagementIpConfiguration для объекта брандмауэра — в качестве входных данных требуется подсеть и общедоступный IP-адрес — имя подсети должно быть "AzureFirewallManagementSubnet"
* Исправлены примеры Get-AzNetworkSecurityGroup для отображения примеров для группы безопасности сети (NSG) вместо сетевых интерфейсов.
* Исправлена опечатка в команде New-AzVpnSite, которая препятствовала завершению параметра идентификатором ресурса.
* Добавлена поддержка конфигурации в наборе действий для правил подстановки URL-адресов в шлюзе приложения.
    - Добавлены новые командлеты:
        - New-AzApplicationGatewayRewriteRuleUrlConfiguration
    - В следующие командлеты добавлен необязательный параметр — UrlConfiguration
        - New-AzApplicationGatewayRewriteRuleActionSet
* Добавление поддержки для ресурсов NetworkWatcher ConnectionMonitor версии 2

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Поддержка оценки соответствия до определения того, какой ресурс нужно исправить
    - Добавление параметра "—ResourceDiscoverMode" в Start-AzPolicyRemediation
* Добавление командлета Get-AzPolicyMetadata для получения ресурсов метаданных политики
* Get-AzPolicyState и Get-AzPolicyStateSummary обновлены для API версии 2019-10-01

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Поддержка Azure Site Recovery для удаления реплицированного диска.
* В Azure Backup добавлена ​​поддержка добавления тегов при создании Хранилища служб восстановления.

#### <a name="azresources"></a>Az.Resources
* Сделайте команду "Область" необязательной в командлетах *—AzPolicyAssignment с настройкой по умолчанию для контекстной подписки
* Добавление примеров создания ADServicePrincipal с паролем и ключом учетных данных

#### <a name="azsql"></a>Az.Sql
Исправление командлета New-AzSqlDatabaseSecondary, чтобы проверить существование PartnerDatabaseName, а не DatabaseName.

#### <a name="azstorage"></a>Az.Storage
* Поддержка набора шифрования типа ключа таблиц и очередей в создании учетной записи хранения
    - New-AzStorageAccount
* Представление RequestId, если StorageException не имеет ExtendedErrorInformation
* Исправление примера 6 командлета Start-AzStorageBlobCopy

#### <a name="azwebsites"></a>Az.Websites
* Set-AzWebapp и Set-AzWebappSlot поддерживают свойства AlwaysOn, MinTls и FtpsState
* Устранение проблемы, при которой параметр HttpsOnly с одновременным изменением AppservicePlan с помощью одной команды Set-AzWebApp сбрасывал значение HttpsOnly до значения по умолчанию

## <a name="330---january-2020"></a>3.3.0 — январь 2020 г.
#### <a name="azaccounts"></a>Az.Accounts
* Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment: теперь они принимают параметры AzureAttestationServiceEndpointResourceId и AzureAttestationServiceEndpointSuffix.

#### <a name="azcdn"></a>Az.Cdn
* Теперь в командлете New-AzCdnEndpoint отображаются сведения из сообщения об ошибке.

#### <a name="azcompute"></a>Az.Compute
* Командлет Set-AzVMCustomScriptExtension исправлен для виртуальной машины с управляемым диском ОС без профиля ОС.

#### <a name="azcontainerinstance"></a>Az.ContainerInstance
* Исправлены имена параметров, используемые в примере командлета New-AzContainerGroup.

#### <a name="azdataboxedge"></a>Az.DataBoxEdge
* Добавлен командлет Get-AzDataBoxEdgeStorageContainer:
  - получение контейнера хранилища Edge.
* Добавлен командлет New-AzDataBoxEdgeStorageContainer:
  - создание контейнера хранилища Edge.
* Добавлен командлет Remove-AzDataBoxEdgeStorageContainer:
  - удаление контейнера хранилища Edge.
* Добавлен командлет Invoke-AzDataBoxEdgeStorageContainer:
  - вызов действия для обновления данных в контейнере хранилища Edge.
* Добавлен командлет Get-AzDataBoxEdgeStorageAccount:
  - получение учетной записи хранилища Edge.
* Добавлен командлет New-AzDataBoxEdgeStorageAccount:
  - создание учетной записи хранилища Edge.
* Добавлен командлет Remove-AzDataBoxEdgeStorageAccount:
  - удаление учетной записи хранилища Edge.
* Вызов командлета Invoke-AzDataBoxEdgeShare:
  - вызов действия для обновления данных в общей папке.
* Добавлен командлет Set-AzDataBoxEdgeStorageAccountCredential:
  - установка учетных данных для учетной записи хранилища Azure Data Box Edge.

#### <a name="azdatafactory"></a>Az.DataFactory
* Добавлены свойства AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId и VersionStatus для командлета Get-AzDataFactoryV2IntegrationRuntime.
* Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.6.0.
* Для командлета Set-AzureRmDataFactoryV2IntegrationRuntime добавлен параметр PublicIPs, позволяющий включить создание среды Azure-SSIS IR со статическими общедоступными IP-адресами.

#### <a name="azdevtestlabs"></a>Az.DevTestLabs
* Удалена недействительная ссылка в файле Get-AzDtlAllowedVMSizesPolicy.md.

#### <a name="azeventhub"></a>Az.EventHub
* Устранена проблема № 10634: исправлена ссылка на пустой объект для удаления пространства имен концентратора событий.

#### <a name="azhdinsight"></a>Az.HDInsight
* Устранена ошибка в файле Invoke-AzHDInsightHiveJob.md.

#### <a name="azmachinelearning"></a>Az.MachineLearning
* Вычислительная среда Машинного обучения больше недоступна, поэтому удалены следующие командлеты:
  - Get-AzMlOpCluster;
  - Get-AzMlOpClusterKey;
  - New-AzMlOpCluster;
  - Remove-AzMlOpCluster;
  - Set-AzMlOpCluster;
  - Test-AzMlOpClusterSystemServicesUpdateAvailability;
  - Update-AzMlOpClusterSystemService.

#### <a name="aznetwork"></a>Az.Network
* Обновлена зависимость Microsoft.Azure.Management.Sql от предварительной версии 1.36 до предварительной версии 1.37.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Добавлена поддержка Azure Site Recovery для виртуальных машин с управляемым диском, зашифрованных при хранении с помощью управляемых клиентом ключей, при восстановлении из Azure в поставщике Azure.
* Добавлена поддержка Azure Site Recovery для необязательного ввода идентификатора набора шифрования диска при включении защиты в рамках восстановления из VMware в Azure.
* Добавлена поддержка Azure Site Recovery для необязательного ввода идентификатора набора шифрования диска на уровне диска при включении защиты в рамках восстановления из VMware в Azure.
* Добавлена поддержка Azure Site Recovery для обновления элемента, защищенного репликацией, путем сопоставления набора шифрования диска при восстановлении из HyperV в Azure.

#### <a name="azresources"></a>Az.Resources
* Исправлена ошибка в справочном документе о командлете Remove-AzTag.

#### <a name="azsql"></a>Az.Sql
* Исправлена функция основных командлетов установки оценки уязвимостей: теперь она позволяет работать с базой данных master для базы данных Azure и ограничить ее в системных базах данных управляемого экземпляра.
* Устранена ошибка, возникающая при создании группы отработки отказа экземпляра SQL.

#### <a name="azsqlvirtualmachine"></a>Az.SqlVirtualMachine
* Добавлен новый допустимый тип лицензии: DR (аварийное восстановление).

#### <a name="azstorage"></a>Az.Storage
* Добавлено предупреждающее сообщение о критическом изменении значения DefaultAction в следующем выпуске:
    - Update-AzStorageAccountNetworkRuleSet.
* Включена поддержка получения времени последней синхронизации учетной записи хранения путем выполнения командлета Get-AzureRmStorageAccount с параметром -IncludeGeoReplicationStats:
    - Get-AzureRmStorageAccount.

## <a name="320---december-2019"></a>3.2.0 — декабрь 2019 г.

### <a name="general"></a>Общие сведения
* Обновление ссылок в .psd1 для использования относительного пути для всех модулей.

#### <a name="azaccounts"></a>Az.Accounts
* Установка правильного параметра UserAgent для телеметрии на стороне клиента для Az 4.0 (предварительная версия).
* Отображение понятного пользователю сообщения об ошибке, если в Az 4.0 (предварительная версия) не указан контекст.

#### <a name="azbatch"></a>Az.Batch
* Исправлена проблема [№ 10602](https://github.com/Azure/azure-powershell/issues/10602), из-за которой использование командлета **New-AzBatchPool** приводило к неправильной отправке VirtualMachineConfiguration.ContainerConfiguration или VirtualMachineConfiguration.DataDisks на сервер.

#### <a name="azdatafactory"></a>Az.DataFactory
* Обновление пакета SDK Фабрики данных для .NET до версии 4.5.0.

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Включена поддержка исключений управляемых правил WAF.
* Добавление SocketAddr в список автозавершения.

#### <a name="azhealthcareapis"></a>Az.HealthcareApis
* Обработка исключений.

#### <a name="azkeyvault"></a>Az.KeyVault
* Исправлена ошибка при получении доступа к значению, которое может быть не задано.
* Управление сертификатами шифрования на основе эллиптических кривых.
    - Включена возможность указания кривой для политик сертификатов.

#### <a name="azmonitor"></a>Az.Monitor
* Добавление необязательного аргумента в команду добавления параметров диагностики. Существующий аргумент switch указывает на то, что экспорт в Log Analytics должен выполняться в фиксированную схему (выделенный тип данных).

#### <a name="aznetwork"></a>Az.Network
* В приложении AzureFirewall, NAT и сетевых правилах включена поддержка IpGroups.

#### <a name="azresources"></a>Az.Resources
* Устранена проблема, из-за которой при развертывании шаблона не удавалось считать его параметр, если имя параметра конфликтовало с именем встроенного параметра.
* Обновлены командлеты политики для использования новой версии API 2019-09-01 с поддержкой группирования в определениях наборов политик.

#### <a name="azsql"></a>Az.Sql
* Обновлена функция автоматического создания расширенного хранилища для службы оценки уязвимостей в учетной записи StorageV2.

#### <a name="azstorage"></a>Az.Storage
* Включена поддержка создания маркера SAS на основе удостоверения контейнера и большого двоичного объекта с аутентификацией Oauth на основе контекста службы хранилища:
    - New-AzStorageContainerSASToken;
    - New-AzStorageBlobSASToken
* Отозвана поддержка ключей делегирования пользователя учетной записи хранения, а также всех маркеров SAS удостоверения:
    - Revoke-AzStorageAccountUserDelegationKeys.
* Выполнено обновление до Microsoft.Azure.Management.Storage версии 14.2.0 для включения поддержки нового API версии 2019-06-01.
* Включена поддержка QuotaGiB (квота общего ресурса в ГиБ) для значений свыше 5120 в командлетах для работы с общими папками в плоскости управления и добавлен псевдоним Quota для параметра QuotaGiB.
    - New-AzRmStorageShare;
    - Update-AzRmStorageShare;
* Добавлен псевдоним QuotaGiB для параметра Quota:
    - Set-AzStorageShareQuota.
* Устранена проблема, из-за которой при использовании AzStorageContainerAcl могла очищаться хранимая политика доступа:
    - Set-AzStorageContainerAcl.

## <a name="310---november-2019"></a>Версия 3.1.0 от ноября 2019 г.
### <a name="highlights-since-the-last-major-release"></a>Основные возможности с момента последнего основного выпуска
* Выпуск Az.DataBoxEdge 1.0.0
* Выпуск Az.SqlVirtualMachine 1.0.0

#### <a name="azcompute"></a>Az.Compute
* Функция повторного применения виртуальной машины
    - Добавлен параметр повторного применения в командлет Set-AzVM.
* Функция AutomaticRepairs масштабируемого набора виртуальных машин:
    - Добавлены параметры EnableAutomaticRepair, AutomaticRepairGracePeriod и AutomaticRepairMaxInstanceRepairsPercent в следующие командлеты:   New-AzVmssConfig Update-AzVmss
* Включена поддержка образа из коллекции разных клиентов для New-AzVM.
* Добавлен фрагмент Spot в средство заполнения аргументов параметра Priority в командлетах New-AzVM, New-AzVMConfig и New-AzVmss.
* Добавлены параметры DiskIOPSReadWrite и DiskMBpsReadWrite в командлет Add-AzVmssDataDisk.
* Изменен параметр SourceImageId командлета New-AzGalleryImageVersion на необязательный.
* Добавлены параметры OSDiskImage и DataDiskImage в командлет New-AzGalleryImageVersion.
* Добавлен параметр HyperVGeneration в командлет New-AzGalleryImageDefinition.
* Добавлены параметры SkipExtensionsOnOverprovisionedVMs в командлеты New-AzVmss, New-AzVmssConfig и Update-AzVmss.

#### <a name="azdataboxedge"></a>Az.DataBoxEdge
* Добавлен командлет `Get-AzDataBoxEdgeOrder`.
    - Получение заказа.
* Добавлен командлет `New-AzDataBoxEdgeOrder`.
    - Создание заказа.
* Добавлен командлет `Remove-AzDataBoxEdgeOrder`.
    - Удаление заказа.
* Изменен командлет `New-AzDataBoxEdgeShare`.
    - Создание локальной общей папки.
* Добавлен командлет `Set-AzDataBoxEdgeRole`.
    - Сопоставление IotRole с общей папкой.
* Добавлен командлет `Invoke-AzDataBoxEdgeDevice`.
    - Вызов проверки обновлений, скачивание обновления, установка обновления на устройстве.
* Добавлен командлет `Get-AzDataBoxEdgeTrigger`.
    - Получение сведений о триггерах.
* Добавлен командлет `New-AzDataBoxEdgeTrigger`.
    - Создание триггеров.
* Добавлен командлет `Remove-AzDataBoxEdgeTrigger`.
    - Удаление триггеров.

#### <a name="azdatafactory"></a>Az.DataFactory
* Обновление пакета SDK Фабрики данных для .NET до версии 4.4.0.
* Добавлен параметр ExpressCustomSetup в командлет Set-AzureRmDataFactoryV2IntegrationRuntime для включения конфигураций установки и сторонних компонентов без использования настраиваемого скрипта установки.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Обновлена документация по Get-AzDataLakeStoreDeletedItem и Restore-AzDataLakeStoreDeletedItem.

#### <a name="azeventhub"></a>Az.EventHub
* Исправлена проблема № 10301. Исправлен формат даты маркера SAS.

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Добавлен параметр MinimumTlsVersion в Enable-AzFrontDoorCustomDomainHttps и New-AzFrontDoorFrontendEndpointObject.
* Добавлены параметры HealthProbeMethod и EnabledState в New-AzFrontDoorHealthProbeSettingObject.
* Добавлен новый командлет для создания объекта BackendPoolsSettings для передачи при создании и обновлении Front Door.
    - New-AzFrontDoorBackendPoolsSettingObject

#### <a name="aznetwork"></a>Az.Network
* Изменены примеры параметра FilterData Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.

#### <a name="azprivatedns"></a>Az.PrivateDns
* Пакет SDK PrivateDns для .NET обновлен до версии 1.0.0

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Включена поддержка Azure Site Recovery для выбора типа диска при включении защиты.
* Внесено исправление Azure Site Recovery для изменения действия плана восстановления.
* Включена поддержка восстановления SQL Azure Backup для принятия баз данных файлового потока.

#### <a name="azrediscache"></a>Az.RedisCache
* Добавлен параметр MinimumTlsVersion в командлеты New-AzRedisCache и Set-AzRedisCache. Кроме того, добавлен параметр MinimumTlsVersion в выходные данные командлета Get-AzRedisCache.
* Добавлена проверка параметра -Size для командлетов Set-AzRedisCache и New-AzRedisCache.

#### <a name="azresources"></a>Az.Resources
- Обновлены командлеты политики для использования новой версии API 2019-06-01 с новым свойством EnforcementMode в назначении политики.
- Обновлен пример справки по созданию определения политики
- Исправлена ошибка с параметром -ServicePrincipalName командлета Remove-AZADServicePrincipal с возвратом пустой ссылки, если имя субъекта службы не найдено.
- Исправлена ошибка с New-AZADServicePrincipal с возвратом пустой ссылки, если у клиента нет подписки.
- Изменен командлет New-AzAdServicePrincipal для добавления учетных данных только для связанного приложения.

#### <a name="azsql"></a>Az.Sql
* Добавлена поддержка ReadReplicaCount для базы данных.
* Исправлена ошибка с Set-AzSqlDatabase, если избыточность в пределах зоны не настроена.

## <a name="300---november-2019"></a>Версия 3.0.0 от ноября 2019 г.
### <a name="general"></a>Общие сведения
* Выпущена версия Az.PrivateDns 1.0.0

#### <a name="azaccounts"></a>Az.Accounts
* Добавлено сообщение об устаревании для псевдонима "Resolve-Error".

#### <a name="azadvisor"></a>Az.Advisor
* Добавлена новая категория Operational Excellence (Эффективность работы) в командлет Get-AzAdvisorRecommendation.

#### <a name="azbatch"></a>Az.Batch
* `CoreQuota` в `BatchAccountContext` переименован в `DedicatedCoreQuota`. Также появился новый `LowPriorityCoreQuota`.
  - Это влияет на **Get-AzBatchAccount**.
* Параметр **New-AzBatchTask** `-ResourceFile` теперь принимает коллекцию объектов `PSResourceFile`, которые можно создать с помощью нового командлета **New-AzBatchResourceFile**.
* Новый командлет **New-AzBatchResourceFile**, который помогает создавать объекты `PSResourceFile`. Их можно передавать в **New-AzBatchTask** в параметре `-ResourceFile`.
  - Это позволяет поддерживать два новых типа файлов ресурсов, которые дополняют существующий метод `HttpUrl`:
    - Файлы ресурсов на основе `AutoStorageContainerName` скачивают весь контейнер автоматического хранения в узел пакетной службы.
    - Файлы ресурсов на основе `StorageContainerUrl` скачивают указанный в URL-адресе контейнер в узел пакетной службы.
* Удалено свойство `ApplicationPackages` в `PSApplication`, который возвращается из **Get-AzBatchApplication**.
  - Отдельные пакеты в приложении теперь можно извлечь с помощью **Get-AzBatchApplicationPackage**. Например: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.
* `ApplicationId` переименован в `ApplicationName` для **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** и **Set-AzBatchApplication**.
  - Теперь `ApplicationId` является псевдонимом для `ApplicationName`.
* Добавлено новое свойство `PSWindowsUserConfiguration` в `PSUserAccount`.
* `Version` переименован в `Name` для `PSApplicationPackage`.
* `BlobSource` переименован в `HttpUrl` для `PSResourceFile`.
* Удалено свойство `OSDisk` из `PSVirtualMachineConfiguration`.
* Удалена операция **Set-AzBatchPoolOSVersion**. Больше она не поддерживается.
* Удалено `TargetOSVersion` из `PSCloudServiceConfiguration`.
* `CurrentOSVersion` переименован в `OSVersion` для `PSCloudServiceConfiguration`.
* Удалено `DataEgressGiB` и `DataIngressGiB` из `PSPoolUsageMetrics`.
* Операция **Get-AzBatchNodeAgentSku** удалена и заменена на **Get-AzBatchSupportedImage**.
  - **Get-AzBatchSupportedImage** возвращает те же данные, что и **Get-AzBatchNodeAgentSku**, но в более удобном формате.
  - Также возвращаются новые непроверенные образы. Включается и дополнительная информация о `Capabilities` и `BatchSupportEndOfLife` для каждого образа.
* Добавлена возможность монтировать файловые системы на каждом узле пула с помощью нового параметра `MountConfiguration` в **New-AzBatchPool**.
* Теперь поддерживаются правила безопасности сети, которые блокируют сетевой доступ к пулу по исходящему порту трафика. Это выполняется с помощью свойства `SourcePortRanges` для `PSNetworkSecurityGroupRule`.
* Что касается выполнения контейнеров, пакетная служба теперь поддерживает выполнение задачи в рабочей папке контейнера или рабочей папке задачи пакетной службы. Выбор зависит от параметра `WorkingDirectory` в `PSTaskContainerSettings`.
* Добавлена возможность указать коллекцию общедоступных IP-адресов для `PSNetworkConfiguration` с помощью нового свойства `PublicIPs`. Это гарантирует, что узлы в пуле будут иметь IP-адреса из списка, предоставленного пользователем.
* Если значение не задано, по умолчанию для `WaitForSuccess` в `PSSTartTask` используется значение `$True` (ранее `$False`).
* Если значение не задано, по умолчанию для `Scope` в `PSAutoUserSpecification` используется значение `Pool` (ранее `Task` для Windows или `Pool` для Linux).

#### <a name="azcdn"></a>Az.Cdn
* Добавлены UrlRewriteAction и CacheKeyQueryStringAction в RulesEngine.
* Исправлено несколько ошибок, таких как отсутствующий входной параметр Selector в командлете New-AzDeliveryRuleCondition.

#### <a name="azcompute"></a>Az.Compute
* Функция набора шифрования диска
    - Новые командлеты:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet
    - Добавлен параметр ProximityPlacementGroupId в следующие командлеты:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk
    - Параметры DiskEncryptionSetId и EncryptionType добавлены в следующие командлеты:   New-AzDiskConfig   New-AzSnapshotConfig
* Добавлен параметр PublicIPAddressVersion в New-AzVmssIPConfig
* FileUris для расширения пользовательских скриптов теперь будет защищенным, а не общедоступным параметром
* Добавлено ScaleInPolicy в командлеты New-AzVmss, New-AzVmssConfig и Update-AzVmss
* Критические изменения
    - Параметр UploadSizeInBytes применяется теперь вместо DiskSizeGB для New-AzDiskConfig, если CreateOption имеет значение Upload
    - PublishingProfile.Source.ManagedImage.Id заменяется на StorageProfile.Source.Id в объекте GalleryImageVersion

#### <a name="azdatafactory"></a>Az.DataFactory
* Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.3.0.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Обновлен пакет SDK для ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), включает следующие исправления
* Не создается исключение при невозможности десериализовать значение времени создания для записи в корзине или каталоге.
* Предоставляется параметр для времени ожидания запроса в adlsclient
* Исправлена передача исходного значения syncflag для восстановления badoffset
* Исправлена операция EnumerateDirectory, чтобы она извлекала токен продолжения после проверки ответа
* Исправлена ошибка объединения

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Исправлены разные опечатки в разных частях модуля

#### <a name="azhdinsight"></a>Az.HDInsight
* Исправлена ошибка, из-за которой клиент получал сообщение об ошибке 'Not a valid Base-64 string' (Не является допустимой строкой Base64) при выполнении Get-AzHDInsightCluster для получения кластера с хранилищем ADLSGen1.
* Добавлен параметр с именем ApplicationId в три командлета Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig и New-AzHDInsightCluster, чтобы клиент мог предоставить идентификатор приложения субъекта-службы для доступа к Azure Data Lake.
* Для Microsoft.Azure.Management.HDInsight изменена версия с 2.1.0 на 5.1.0
* Удалены пять командлетов:
    - Get-AzHDInsightOMS
    - Enable-AzHDInsightOMS
    - Disable-AzHDInsightOMS
    - Grant-AzHDInsightRdpServicesAccess
    - Revoke-AzHDInsightRdpServicesAccess
* Добавлены три командлета:
    - Get-AzHDInsightMonitoring заменяет собой Get-AzHDInsightOMS.
    - Enable-AzHDInsightMonitoring заменяет собой Enable-AzHDInsightOMS.
    - Disable-AzHDInsightMonitoring заменяет собой Disable-AzHDInsightOMS.
* Исправлен командлет Get-AzHDInsightProperties, чтобы он поддерживал получение сведений о возможностях из определенного расположения.
* Удалены наборы параметров ("Spark1", "Spark2") из Add-AzHDInsightConfigValue.
* Добавлены примеры в справочные документы по командлету Add-AzHDInsightSecurityProfile.
* Изменен тип выходных данных для следующих командлетов:
*  - Для Get-AzHDInsightProperties тип выходных данных изменен с CapabilitiesResponse на AzureHDInsightCapabilities.
*  - Для Remove-AzHDInsightCluster тип выходных данных изменен с ClusterGetResponse на bool.
*  - Для Set-AzHDInsightGatewaySettings тип выходных данных изменен с HttpConnectivitySettings на GatewaySettings.
* Добавлены несколько условий для проверки сценариев.
* Удалены несколько псевдонимов: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.

#### <a name="aziothub"></a>Az.IotHub
* Критические изменения
    - Командлет Add-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.
    - Удален набор параметров __AllParameterSets для командлета Add-AzIotHubEventHubConsumerGroup.
    - Командлет Get-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.
    - Удален набор параметров __AllParameterSets для командлета Get-AzIotHubEventHubConsumerGroup.
    - Удалено свойство OperationsMonitoringProperties для типа Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties.
    - Удалено свойство OperationsMonitoringProperties для типа Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties.
    - Командлет New-AzIotHubExportDevice больше не поддерживает псевдоним New-AzIotHubExportDevices.
    - Командлет New-AzIotHubImportDevice больше не поддерживает псевдоним New-AzIotHubImportDevices.
    - Командлет Remove-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.
    - Удален набор параметров __AllParameterSets для командлета Remove-AzIotHubEventHubConsumerGroup.
    - Командлет Set-AzIotHub теперь не поддерживает параметр OperationsMonitoringProperties и не найдены псевдонимы для исходного имени параметра.
    - Удален набор параметров UpdateOperationsMonitoringProperties для командлета Set-AzIotHub.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Azure Site Recovery поддерживает настройку сетевых ресурсов, например групп безопасности сети, общедоступных IP-адресов и внутренних подсистем балансировки нагрузки из Azure в Azure.
* Azure Site Recovery поддерживает запись на управляемый диск из vMWare в Azure.
* Azure Site Recovery поддерживает сокращение NIC из vMWare в Azure.
* Azure Site Recovery поддерживает ускорение сети NIC из Azure в Azure.
* Azure Site Recovery поддерживает автоматическое обновление агента из Azure в Azure.
* Azure Site Recovery поддерживает стандартный SSD-накопитель из Azure в Azure.
* Azure Site Recovery поддерживает двухпроходное шифрование диска Azure из Azure в Azure.
* Azure Site Recovery поддерживает новый добавленный диск из Azure в Azure.
* Добавлена функция SoftDelete для виртуальных машин и соответствующие тесты

#### <a name="azresources"></a>Az.Resources
* Обновлена сборка зависимостей Microsoft.Extensions.Caching.Memory с версии 1.1.1 до 2.2

#### <a name="aznetwork"></a>Az.Network
* Изменены все командлеты для PrivateEndpointConnection, чтобы они поддерживали универсальный поставщик служб.
    - Обновлен командлет:
        - Approve-AzPrivateEndpointConnection.
        - Deny-AzPrivateEndpointConnection.
        - Get-AzPrivateEndpointConnection.
        - Remove-AzPrivateEndpointConnection.
        - Set-AzPrivateEndpointConnection
* Добавлен новый командлет для PrivateLinkResource, который поддерживает универсальный поставщик служб.
    - Новый командлет
        - Get-AzPrivateLinkResource
* Добавлены новые поля и параметр для протокола прокси версии 2.
    - Добавлено свойство EnableProxyProtocol в PrivateLinkService
    - Добавлено свойство LinkIdentifier в PrivateEndpointConnection
    - Обновлен New-AzPrivateLinkService для поддержки нового необязательного параметра EnableProxyProtocol.
* Исправлено описание параметра в справочной документации по командлету New-AzApplicationGatewaySku.
* Новые командлеты для поддержки политики брандмауэра Azure
* Добавлена поддержка дочерних ресурсов RouteTables для VirtualHub
    - Добавлены новые командлеты:
        - Add-AzVirtualHubRoute
        - Add-AzVirtualHubRouteTable
        - Get-AzVirtualHubRouteTable
        - Remove-AzVirtualHubRouteTable
        - Set-AzVirtualHub
* Добавлена поддержка новых свойств SKU для VirtualHub и VirtualWANType в VirtualWan
    - В следующие командлеты добавлены необязательные параметры:
        - New-AzVirtualHub: добавлен параметр Sku
        - Update-AzVirtualHub: добавлен параметр Sku
        - New-AzVirtualWan: добавлен параметр VirtualWANType
        - Update-AzVirtualWan: добавлен параметр VirtualWANType
* Добавлена поддержка свойства EnableInternetSecurity для HubVnetConnection, VpnConnection и ExpressRouteConnection
    - Добавлены новые командлеты:
        - Update-AzureRmVirtualHubVnetConnection
    - В следующие командлеты добавлены необязательные параметры:
        - New-AzureRmVirtualHubVnetConnection: добавлен параметр EnableInternetSecurity
        - New-AzureRmVpnConnection: добавлен параметр EnableInternetSecurity
        - Update-AzureRmVpnConnection: добавлен параметр EnableInternetSecurity
        - New-AzureRmExpressRouteConnection: добавлен параметр EnableInternetSecurity
        - Set-AzureRmExpressRouteConnection: добавлен параметр EnableInternetSecurity
* Добавлена поддержка настройки политики верхнего уровня WebApplicationFirewall
    - Добавлены новые командлеты:
        - New-AzApplicationGatewayFirewallPolicySetting
        - New-AzApplicationGatewayFirewallPolicyExclusion
        - New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride
        - New-AzApplicationGatewayFirewallPolicyManagedRuleOverride
        - New-AzApplicationGatewayFirewallPolicyManagedRule
        - New-AzApplicationGatewayFirewallPolicyManagedRuleSet
    - В следующие командлеты добавлены необязательные параметры:
        - New-AzApplicationGatewayFirewallPolicy: добавлены параметры PolicySetting, ManagedRule
* Добавлена поддержка оператора Geo-Match для CustomRule
    - Добавлен параметр GeoMatch в оператор для FirewallCondition
* Добавлена поддержка политики брандмауэра perListener и perSite
    - В следующие командлеты добавлены необязательные параметры:
        - New-AzApplicationGatewayHttpListener: добавлены параметры FirewallPolicy, FirewallPolicyId
        - New-AzApplicationGatewayPathRuleConfig: добавлены параметры FirewallPolicy, FirewallPolicyId
* Исправлен учет регистра для требуемой подсети с именем AzureBastionSubnet в PSBastion
* Поддержка полного доменного имени назначения в правилах сети и преобразованного полного доменного имени в правилах NAT для брандмауэра Azure
* Добавлена поддержка ресурсов верхнего уровня RouteTables для IpGroup
    - Добавлены новые командлеты:
        - New-AzIpGroup
        - Remove-AzIpGroup
        - Get-AzIpGroup
        - Set-AzIpGroup

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Удален командлет Add-AzServiceFabricApplicationCertificate, так как соответствующий сценарий выполняется командлетом Add-AzVmssSecret.

#### <a name="azsql"></a>Az.Sql
* Добавлена поддержка восстановления удаленных баз данных в управляемых экземплярах.
* Из кода удалены старые командлеты аудита.
* Удалены нерекомендуемые псевдонимы:
* Get-AzSqlDatabaseIndexRecommendations (вместо него используйте Get-AzSqlDatabaseIndexRecommendation)
* Get-AzSqlDatabaseRestorePoints (вместо него используйте Get-AzSqlDatabaseRestorePoint)
* Удален командлет Get-AzSqlDatabaseSecureConnectionPolicy
* Удалены псевдонимы для нерекомендуемых командлетов параметров оценки уязвимостей
* Командлеты расширенного обнаружения угроз объявлены устаревшими
* Добавлены командлеты для отключения и включения рекомендаций о конфиденциальности для столбцов в базе данных.

#### <a name="azstorage"></a>Az.Storage
* Поддержка включения большой общей папки при создании или обновлении учетной записи хранения
    -  New-AzStorageAccount
    -  Set-AzStorageAccount
* При закрытии или получении маркера файла пропускается проверка того, является ли входной путь файлом или каталогом, чтобы избежать сбоев при получении объектов в состоянии DeletePending.
    -  Get-AzStorageFileHandle
    -  Close-AzStorageFileHandle

## <a name="280---october-2019"></a>2.8.0 — октябрь 2019 г.
### <a name="general"></a>Общие сведения
* Выпуск Az.HealthcareApis 1.0.0

#### <a name="azaccounts"></a>Az.Accounts
* Обновление телеметрии и перезаписи URL-адресов для созданных модулей, исправление для модульных тестов Windows.

#### <a name="azapimanagement"></a>Az.ApiManagement
* **Set-AzApiManagementApi** — в ApiVersionSet добавлена поддержка обновления API.
    - исправлена проблема https://github.com/Azure/azure-powershell/issues/10068.

#### <a name="azautomation"></a>Az.Automation
* Исправлен командлет New-AzureAutomationSoftwareUpdateConfiguration для параметра перезагрузки Linux.

#### <a name="azbatch"></a>Az.Batch
* Командлет **Get-AzBatchNodeAgentSku** объявлен устаревшим и будет заменен на **Get-AzBatchSupportImage** в версии 2.0.0.

#### <a name="azcompute"></a>Az.Compute
* В командлеты New-AzVM и New-AzVmss добавлены параметры Priority, EvictionPolicy и MaxPrice.
* Исправлены предупреждающее сообщение для командлетов Add-AzVMAdditionalUnattendContent и Add-AzVMSshPublicKey и справочная документация по ним.
* Для Set-AzVMDiskEncryptionExtension исправлено исключение -skipVmBackup для виртуальных машин Linux с управляемыми дисками.
* Исправлена ошибка при изменении параметров шифрования в Set-AzVMDiskEncryptionExtension, реализован двухэтапный сценарий.

#### <a name="azdatafactory"></a>Az.DataFactory
* Добавлены команды CRUD для потока данных Фабрики данных Azure версии 2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow и Get-AzDataFactoryV2DataFlow.
* Добавлены команды действий для сеанса отладки потока данных Фабрики данных Azure версии 2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand и Stop-AzDataFactoryV2DataFlowDebugSession.
* Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.2.0.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Проверка учетной записи исправлена так, чтобы учетные записи, содержащие знак "-", можно было передавать без домена.

#### <a name="azhealthcareapis"></a>Az.HealthcareApis
* Версия PowerShell обновлена до 1.0.0.
* Версия пакета SDK обновлена до 1.0.2.
* В тестах обновлены ссылки на новую версию пакета SDK.
* Вложенная выходная структура заменена на плоскую.

#### <a name="aziothub"></a>Az.IotHub
* Добавлен новый источник маршрутизации DigitalTwinChangeEvents.
* Исправлены незначительные ошибки: Get-AzIothub не возвращает subscriptionId.

#### <a name="azmonitor"></a>Az.Monitor
* Добавлены новые получатели групп действий: -ItsmReceiver, -VoiceReceiver, -ArmRoleReceiver, -AzureFunctionReceiver, -LogicAppReceiver, -AutomationRunbookReceiver, -AzureAppPushReceiver.
* Для получателей включите общую схему оповещений. Это не касается получателей SMS, push-уведомлений приложения Azure, ITSM и голосовых сообщений.
* Веб-перехватчики теперь поддерживают аутентификацию Azure Active Directory.

#### <a name="aznetwork"></a>Az.Network
* Добавлен новый командлет Get-AzAvailableServiceAlias, позволяющий получить псевдонимы для политик конечной точки службы.
* В подключениях шлюза виртуальной сети появилась возможность добавлять селекторы трафика.
    - Добавлены новые командлеты:
        - New-AzureRmTrafficSelectorPolicy.
    - В командлеты добавлены необязательные параметры -TrafficSelectorPolicies, -New-AzureRmVirtualNetworkGatewayConnection, -Set-AzureRmVirtualNetworkGatewayConnection.
* В конфигурациях правил сетевой безопасности добавлена поддержка протоколов ESP и AH.
    - Обновлены командлеты:
        - Add-AzNetworkSecurityRuleConfig.
        - New-AzNetworkSecurityRuleConfig.
        - Set-AzNetworkSecurityRuleConfig.
* Улучшена обработка исключений в командлетах Cortex.
* Выпущены новые поколения и номера SKU VirtualNetworkGateways.
  - Представлены новые поколения VirtualNetworkGateways.
  - Представлены новые номера SKU VirtualNetworkGateways с высокой пропускной способностью.

#### <a name="azrediscache"></a>Az.RedisCache
* В справочную документацию по Set-AzRedisCache добавлены недостающие значения для параметра -Size.

#### <a name="azsql"></a>Az.Sql
* Добавлена возможность назначать администратора Active Directory в Управляемом экземпляре.

#### <a name="azstorage"></a>Az.Storage
* Клиентская библиотека службы хранилища Azure обновлена до версии 11.1.0.
* NextPageLink теперь позволяет получить список контейнеров с помощью API плоскости управления.
    -  Get-AzRmStorageContainer
* NextPageLink теперь позволяет получить список учетных записей хранения из подписки.
    -  Get-AzStorageAccount

#### <a name="azstoragesync"></a>Az.StorageSync
* Исправлена проблема 9810 с Reset-AzStorageSyncServerCertificate.

#### <a name="azwebsites"></a>Az.Websites
* Обновление плана службы приложений с помощью Set-AzWebApp приводило к сбою приложения.

## <a name="270---september-2019"></a>2.7.0 — сентябрь 2019 г.
#### <a name="azapimanagement"></a>Az.ApiManagement
* В справочной документации по командлету Set-AzApiManagementPolicy обновлено описание параметра -Format.
* Из справочной документации удалены ссылки на нерекомендуемый командлет Update-AzApiManagementDeployment. Вместо него следует использовать командлет Set-AzApiManagement.

#### <a name="azautomation"></a>Az.Automation
* В справочной документации по командлету Register-AzAutomationDscNode исправлена опечатка в примере.
* Добавлено уточнение об ограничениях ОС для командлета Register-AzAutomationDSCNode.
* Исправлено исключение пустой ссылки для параметра -Wait в командлете Start-AzAutomationRunbook.

#### <a name="azcompute"></a>Az.Compute
* Добавлен параметр UploadSizeInBytes для командлета New-AzDiskConfig.
* Добавлен добавочный параметр для командлета New-AzSnapshotConfig.
* Для виртуальной машины добавлены такие функции с низким приоритетом:
    - Для командлета New-AzVMConfig добавлены параметры MaxPrice, EvictionPolicy и Priority.
    - Для командлетов New-AzVmssConfig, Update-AzVM и Update-AzVmss добавлен параметр MaxPrice.
* Для командлета Get-AzAvailabilitySet устранена проблема со ссылкой на виртуальную машину, когда в нем перечисляются все группы доступности в подписке.
* Исправлено исключение NULL для командлета Get-AzRemoteDesktopFile.
* Исправлен метод поиска VHD для относительной конечной позиции.
* Устранена проблема с UltraSSD для командлетов New-AzVM и Update-AzVM.

#### <a name="azdatafactory"></a>Az.DataFactory
* Добавлены 3 новые команды для ADF версии 2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription и Get-AzDataFactoryV2TriggerSubscriptionStatus.
* Пакет SDK ADF для .NET обновлен до версии 4.1.3.

#### <a name="azhdinsight"></a>Az.HDInsight
* Укажите критические изменения.

#### <a name="aziothub"></a>Az.IotHub
* Добавлена поддержка для вызова отработки отказа для IotHub в георегион аварийного восстановления.
* Добавлена поддержка для управления обогащением сообщений для IotHub. Ниже перечислены новые командлеты:
    - Add-AzIotHubMessageEnrichment;
    - Get-AzIotHubMessageEnrichment;
    - Remove-AzIotHubMessageEnrichment;
    - Set-AzIotHubMessageEnrichment.

#### <a name="azmonitor"></a>Az.Monitor
* Указание на самую последнюю версию пакета SDK для монитора, т. е. 0.24.1-preview:
   - В командлеты метрик добавлены некритические изменения, т. е. перечисление единиц поддерживает несколько новых значений. Эти командлеты доступны только для чтения, поэтому входные данные командлетов не будут изменены.
   - Актуальная версия API запросов **ActionGroups** — **2019-06-01**. До этого была версия **2018-03-01**. Тесты сценария обновлены в соответствии с этим изменением.
   - В конструкторы классов **EmailReceiver** и **WebhookReceiver** добавлен один новый обязательный аргумент — логическое значение с именем **useCommonAlertSchema**. Сейчас для него установлено значение **false**, чтобы скрыть это критическое изменение от командлетов. **Примечание**. Это временное изменение, которое должно быть подтверждено командой оповещения.
   - Порядок аргументов для конструктора класса **Source** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK. Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.
   - Порядок аргументов для конструктора класса **AlertingAction** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK. Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.
* Добавлена поддержка критериев динамического порога для оповещения метрики версии 2:
    - New-AzMetricAlertRuleV2Criteria: теперь также позволяет создавать критерии динамического порога.
    - Add-AzMetricAlertRuleV2: теперь также позволяет принимать критерии динамического порога.
* Добавлены усовершенствования в командлетах запланированных правил запросов (SQR).
 - Командлеты будут принимать параметр Location в обоих форматах: расположение (например, eastus) или отображаемое имя расположения (например, "восточная часть США").
 - Параметр Enabled проиллюстрирован в файлах справки надлежащим образом.
 - Добавлены примеры для необязательного параметра ActionGroup.
 - Все файлы справки улучшены.
* Исправлена ошибка в определении типа области для командлета Set-AzActionRule.

#### <a name="aznetwork"></a>Az.Network
* Исправлен неправильный пример в справочной документации по командлету New-AzApplicationGateway.
* В справочную документацию по командлету Get-AzNetworkWatcherPacketCapture добавлено примечание, посвященное извлечению всех свойств для записи пакетов.
* В справочной документации по командлету Test-AzNetworkWatcherIPFlow исправлен пример: теперь он правильно перечисляет сетевые карты.
* Улучшен анализ облачных исключений для отображения дополнительных сведений (при их наличии).
* Улучшен анализ облачных исключений для обработки дополнительного типа исключения SDK.
* Исправлено неправильное сопоставление моделей правил безопасности.
* Добавлены свойства сетевого интерфейса для компонента частного IP-адреса.
    - Для интерфейса PSNetworkInterface добавлено свойство PrivateEndpoint с типом PSResourceId.
    - В PSNetworkInterfaceIPConfiguration добавлено свойство PrivateLinkConnectionProperties с типом PSIpConfigurationConnectivityInformation.
    - Добавлен новый класс модели: PSIpConfigurationConnectivityInformation.
* Добавлен новый тип ApplicationRuleProtocolType "mssql" для ресурса Брандмауэра Azure.
* Поддержка многоканального подключения в Виртуальной глобальной сети:
    - Новые командлеты
        - New-AzVpnSiteLink;
        - New-AzVpnSiteLinkConnection;
    - Обновлен командлет:
        - New-VpnSite;
        - Update-VpnSite;
        - New-VpnConnection;
        - Update-VpnConnection.
* Исправлены документы с некоторыми примерами PowerShell для использования командлетов AZ вместо командлетов AzureRM.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Для объекта AzureVMpolicy добавлен новый атрибут — ProtectedItemsCount.
* Добавлены тесты для политики виртуальной машины и восстановления исходной учетной записи хранения.

#### <a name="azresources"></a>Az.Resources
* Исправлена ошибка, при которой не удавалось вызвать командлет New-AzRoleAssignment без параметра Scope.

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Исправлена опечатка в примере в справочной документации по командлету Update-AzServiceFabricReliability.
* Добавлены новые командлеты для управления приложениями и службами:
    - New-AzServiceFabricApplication;
    - New-AzServiceFabricApplicationType;
    - New-AzServiceFabricApplicationTypeVersion;
    - New-AzServiceFabricService;
    - Update-AzServiceFabricApplication;
    - Get-AzServiceFabricApplication;
    - Get-AzServiceFabricApplicationType;
    - Get-AzServiceFabricApplicationTypeVersion;
    - Get-AzServiceFabricService;
    - Remove-AzServiceFabricApplication;
    - Remove-AzServiceFabricApplicationType;
    - Remove-AzServiceFabricApplicationTypeVersion;
    - Remove-AzServiceFabricServic.
* Пакет SDK для Service Fabric обновлен до версии 1.2.0, в которой используется версия API 2019-03-01 поставщика ресурсов Service Fabric.

#### <a name="azsignalr"></a>Az.SignalR
* Добавлены командлеты Update, Restart, CheckNameAvailability и GetUsage.

#### <a name="azsql"></a>Az.Sql
* Обновлен пример в справочной документации по командлету Get-AzSqlElasticPool.
* Добавлен пример виртуального ядра для командлета создания эластичного пула (New-AzSqlElasticPool).
* Удалена проверка свойства EmailAddresses и того, что свойство EmailAdmins правильное в случае, если свойство EmailAddresses пустое в командлетах Set-AzSqlServerAdvancedThreatProtectionPolicy и Set-AzSqlDatabaseAdvancedThreatProtectionPolicy.
* Теперь, если существует несколько параметров диагностики, включающих категорию аудита, параметры аудита сервера и базы данных удаляются.
* Исправлена проверка адресов электронной почты в нескольких командлетах оценки уязвимостей SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting и Update-AzSqlInstanceVulnerabilityAssessmentSetting).

#### <a name="azstorage"></a>Az.Storage
* Обновлен пример в справочной документации по командлету Get-AzStorageAccountKey.
* Теперь при отправке и загрузке файла Azure в конечном файле сохраняются свойства SMB исходного файла (атрибуты файла, время создания файла, время последней записи файла).
    -  Set-AzStorageFileContent
    -  Get-AzStorageFileContent
* Исправлена операция отправки блочного BLOB-объекта, в которой происходили сбои свойств и метаданных в контейнере с включенной ImmutabilityPolicy.
    -  Set-AzStorageBlobContent
* Добавлена поддержка управления общими папками Azure в API плоскости управления с помощью таких командлетов:
    -  New-AzRmStorageShare;
    -  Get-AzRmStorageShare;
    -  Update-AzRmStorageShare;
    -  Remove-AzRmStorageShare.

#### <a name="azwebsites"></a>Az.Websites
* Устранена проблема, из-за которой теги webapp удалялись при переносе приложения в новый ASP.
* Теперь командлет Publish-AzureWebapp работает в Linux и Windows.
* Обновлен пример в справочной документации по командлету Get-AzWebAppPublishingProfile.

## <a name="260---august-2019"></a>2.6.0 — август 2019 г.
#### <a name="general"></a>Общие сведения
* Исправлены опечатки в модулях.

#### <a name="azaccounts"></a>Az.Accounts
* Добавлена поддержка назначаемого пользователем удостоверения MSI при проверке подлинности в Функциях Azure (№ 9479).

#### <a name="azaks"></a>Az.Aks
* Устранена проблема с выходными данными для Get-AzAks.
    * Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9847.

#### <a name="azapimanagement"></a>Az.ApiManagement
* исправлена проблема https://github.com/Azure/azure-powershell/issues/9351.
    - Обновлена версия NuGet для .NET, которая не накладывает ограничений на productId, apiId, groupId и userId.
* **Get-AzApiManagementProduct**. Добавлена поддержка запросов к продуктам с помощью API.
  https://github.com/Azure/azure-powershell/issues/9482
* **New-AzApiManagementApiRevision**. Устранена проблема, из-за которой не задавался параметр ApiRevisionDescription при создании новой редакции API https://github.com/Azure/azure-powershell/issues/9752.
* Исправлено написание имени модели c PsApiManagementOAuth2AuthrozationServer на PsApiManagementOAuth2AuthorizationServer.

#### <a name="azbatch"></a>Az.Batch
* Исправлена опечатка в написании Windows со строчной буквы в справочных сообщениях и документации.

#### <a name="azcdn"></a>Az.Cdn
* Исправлена опечатка во вспомогательном приложении модуля CDN.

#### <a name="azcompute"></a>Az.Compute
* Добавлен параметр VmssId в новый командлет Add New-AzVMConfig.
* Добавлены параметры TerminateScheduledEvents и TerminateScheduledEventNotBeforeTimeoutInMinutes в New-AzVmssConfig и Update-AzVmss.
* Добавлено свойство HyperVGeneration в объект образа виртуальной машины.
* Добавлены компоненты Host и HostGroup.
    - Новые командлеты:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost
    - Параметр HostId добавлен в New-AzVMConfig и New-AzVM.
* Исправлен пример в документации по Invoke-AzVMRunCommand, в котором теперь используется правильное имя параметра.
* Исправлено описание VolumeType в справочной документации по Set-AzVMDiskEncryptionExtension и Set-AzVmssDiskEncryptionExtension.

#### <a name="azdatafactory"></a>Az.DataFactory
* Исправлена опечатка в написании Windows со строчной буквы в документации по New-AzDataFactoryEncryptValue.
* Пакет SDK ADF для .NET обновлен до версии 4.1.2.
* Добавлены параметры DataProxyIntegrationRuntimeName, DataProxyStagingLinkedServiceName и DataProxyStagingPath в командлет Set-AzureRmDataFactoryV2IntegrationRuntime, что позволяет настраивать локальную среду выполнения интеграции в качестве прокси-сервера для Azure-SSIS Integration Runtime.
* Обновлены PSTriggerRun для отображения активированных конвейеров, сообщений и свойств и PSActivityRun для отображения типа действия.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Устранена проблема, при которой Get-DataLakeStoreDeletedItem переставал отвечать на запросы при возникновении ошибок или удаленных исключений.

#### <a name="azeventhub"></a>Az.EventHub
* Исправлена проблема № 9658: опечатка в написании параметра VirtualNteworkRule у Set-AzEventHubNetworkRuleSet.
* Исправлена проблема № 9558: в Set-AzEventHubNamespace используется PATCH вместо PUT.
* В командлет Set-AzEventHubNamespace добавлен параметр EnableKafka.
* Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.

#### <a name="azmarketplaceordering"></a>Az.MarketplaceOrdering
* Исправлено написание Azure со строчной буквы.

#### <a name="azmonitor"></a>Az.Monitor
* Исправлены неправильные имена параметров в справочной документации.

#### <a name="aznetwork"></a>Az.Network
* Обновлен New-AzPrivateLinkServiceIpConfig.
    - Параметр PublicIpAddress объявлен нерекомендуемым, так как он не используется на стороне сервера.
    - Добавлен необязательный параметр Primary, указывающий, является ли текущая IP-конфигурация основной.
* Улучшена обработка исключений из-за ошибок запроса от пакета SDK. Устранена проблема, при которой исключения пакета SDK не обрабатывались правильно, из-за чего не отображались основные сведения об ошибке.
* Настроена логика проверки для префикса IPv6 IP-адреса для проверки правильности длины префикса IPv6.
* Обновлен Get-AzVirtualNetworkSubnetConfig: добавлен набор параметров для получения по идентификатору ресурса подсети.
* Обновлено описание параметра Location для AzNetworkServiceTag.

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Обновлена документация по New-AzOperationalInsightsLinuxSyslogDataSource.
    - Добавлен пример.
    - Обновлено описание параметра -Name.
* Добавлен пример для New-AzOperationalInsightsWindowsEventDataSource
* Изменено описание параметра -Name для New-AzOperationalInsightsWindowsEventDataSource.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Обновлен Get-AzRecoveryServicesBackupJobDetail.md.

#### <a name="azresources"></a>Az.Resources
* Добавлена поддержка новой версии API 2019-05-10 для Microsoft.Resource.
    - Добавлена поддержка copy.count = 0 для переменных, ресурсов и свойств.
    - Ресурсы, у которых condition = false или copy.count = 0, будут удаляться в полном режиме.
* В справочную документацию добавлен пример назначения политики на уровне подписки.

#### <a name="azservicebus"></a>Az.ServiceBus
* Исправлена проблема № 9658: опечатка в написании параметра VirtualNetworkRule В Set-AzServiceBusNetworkRuleSet.
* Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.
* Добавлена новая команда Test-AzServiceBusNameAvailability для проверки доступности имени для очереди и раздела.

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Устранены ошибки командлета для добавления типа узла:
    - ошибка NullReferenceException, возникавшая, если у группы ресурсов были другие VMSS, не связанные с кластером Service Fabric. Исправлена проблема https://github.com/Azure/azure-powershell/issues/8681.
    - Исправлена ошибка, из-за которой командлет завершился сбоем, если virtualNetwork находилась не в той группе ресурсов, к которой относится кластер. Исправлена проблема https://github.com/Azure/azure-powershell/issues/8407.
    - Командлет Add-AzServiceFabricApplicationCertificate объявлен нерекомендуемым.

#### <a name="azsql"></a>Az.Sql
* Обновление документации по старым командлетам аудита.

#### <a name="azstorage"></a>Az.Storage
* Обновлена справка по Get/Close-AzStorageFileHandle: в примеры добавлены сценарии использования командлетов и обновлено описание параметров.
* Добавлена поддержка StandardBlobTier в операции отправки BLOB-объекта и копирования BLOB-объекта.
    -  Set-AzStorageBlobContent
    -  Start-AzStorageBlobCopy
* Добавлена поддержка приоритета восстановления в операцию копирования BLOB-объекта.
    -  Start-AzStorageBlobCopy

#### <a name="azwebsites"></a>Az.Websites
* Добавлены уточнение для параметра -AppSettings в Set-AzWebApp и Set-AzWebAppSlot.

## <a name="250---july-2019"></a>2.5.0 — июль 2019 г.
#### <a name="azaccounts"></a>Az.Accounts
* Обновлен общий код для использования последней версии ClientRuntime.

#### <a name="azapplicationinsights"></a>Az.ApplicationInsights
* Исправлена опечатка в примере в документации по Remove-AzApplicationInsightsApiKey.

#### <a name="azautomation"></a>Az.Automation
* Исправлена опечатка в строке ресурса.

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Добавлена поддержка NetworkRuleSet.

#### <a name="azcompute"></a>Az.Compute
* Добавлены недостающие свойства (ComputerName, OsName, OsVersion и HyperVGeneration) для объекта представления экземпляра виртуальной машины.

#### <a name="azcontainerregistry"></a>Az.ContainerRegistry
* Исправлена опечатка в Remove-AzContainerRegistryReplication для параметра репликации.
    - См. подробнее: https://github.com/Azure/azure-powershell/issues/9633.

#### <a name="azdatafactory"></a>Az.DataFactory
* Пакет SDK для ADF .NET обновлен до версии 4.1.0.
* Исправлена опечатка в документации по Get-AzDataFactoryV2PipelineRun.

#### <a name="azeventhub"></a>Az.EventHub
* Добавлен новый командлет для создания маркера SAS: New-AzEventHubAuthorizationRuleSASToken.
* Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".

#### <a name="azkeyvault"></a>Az.KeyVault
* Добавлена поддержка для настройки параметра KeySize в политиках сертификатов.

#### <a name="azlogicapp"></a>Az.LogicApp
* Get-AzIntegrationAccountMap теперь надлежащим образом выводит все типы сопоставлений.
    - Добавлен новый параметр MapType для фильтрации.

#### <a name="azmanagedservices"></a>Az.ManagedServices
* Добавлена поддержка API версии 2019-06-01 (общедоступная).

#### <a name="aznetwork"></a>Az.Network
* Добавлена поддержка частной конечной точки и службы приватного канала.
    - Новые командлеты
        - Set-AzPrivateEndpoint.
        - Set-AzPrivateLinkService.
        - Approve-AzPrivateEndpointConnection.
        - Deny-AzPrivateEndpointConnection.
        - Get-AzPrivateEndpointConnection.
        - Remove-AzPrivateEndpointConnection.
        - Test-AzPrivateLinkServiceVisibility.
        - Get-AzAutoApprovedPrivateLinkService.
* Обновлены следующие команды для функции: Флаг PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies в подсети в виртуальной сети.
    - Обновлены командлеты New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig.
        - Добавлен необязательный параметр -PrivateEndpointNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к частной конечной точке в этой подсети.
        - Добавлен необязательный параметр -PrivateLinkServiceNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к службе приватного канала в этой подсети.
* Параметр ServiceName командлета AzPrivateLinkService был переименован на Name с псевдонимом ServiceName для обеспечения обратной совместимости.
* Включен протокол ICMP для настройки правил безопасности сети.
    - Обновлены командлеты
        - Add-AzNetworkSecurityRuleConfig.
        - New-AzNetworkSecurityRuleConfig.
        - Set-AzNetworkSecurityRuleConfig.
* Добавлен ConnectionProtocolType (Ikev1/Ikev2) в качестве настраиваемого параметра для командлета New-AzVirtualNetworkGatewayConnection.
* Добавлен PrivateIpAddressVersion в LoadBalancerFrontendIpConfiguration.
    - Обновлен командлет:
        - New-AzLoadBalancerFrontendIpConfig.
        - Add-AzLoadBalancerFrontendIpConfig.
        - Set-AzLoadBalancerFrontendIpConfig.
* Команда New-AzApplicationGatewayProbeConfig Шлюза приложений обновлена для поддержки настраиваемого порта в зонде.
    - Обновлен командлет New-AzApplicationGatewayProbeConfig: добавлен необязательный параметр Port, который используется при проверке внутреннего сервера. Этот параметр применяется к номерам SKU Standard_V2 и WAF_V2.

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Обновленная версия по умолчанию для сохраненных операций поиска имеет значение 1.
* Исправлены ошибки при обработке регулярных выражений со значениями NULL в журналах.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Обновлен файл Get-AzRecoveryServicesBackupJob.md.
* Обновлен файл Get-AzRecoveryServicesBackupContainer.md.
* Обновлен файл Get-AzRecoveryServicesVault.md.
* Обновлен файл Wait-AzRecoveryServicesBackupJob.md.
* Обновлен файл Set-AzRecoveryServicesVaultContext.md.
* Обновлен файл Get-AzRecoveryServicesBackupItem.md.
* Обновлен файл Get-AzRecoveryServicesBackupRecoveryPoint.md.
* Обновлен файл Restore-AzRecoveryServicesBackupItem.md.
* Обновлен вызов службы для отмены регистрации контейнера в общей папке Azure.
* Обновлен файл Set-AzRecoveryServicesAsrAlertSetting.md.

#### <a name="azresources"></a>Az.Resources
- Удален отсутствующий командлет, который упоминается в документации по New-AzResourceGroupDeployment.
- Обновлены командлеты политик для использования новой версии API 2019-01-01.

#### <a name="azservicebus"></a>Az.ServiceBus
* Добавлен новый командлет для создания маркера SAS: New-AzServiceBusAuthorizationRuleSASToken.
* Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".

#### <a name="azsql"></a>Az.Sql
* Исправлены отсутствующие примеры для командлета Set-AzSqlDatabaseSecondary.
* Исправлены заданные повторяющиеся проверки для оценки наличия уязвимостей без указания адресов электронной почты.
* Исправлена незначительная опечатка в сообщении предупреждения.

#### <a name="azstorage"></a>Az.Storage
* Обновлен пример в справочной документации для использования командлетом Get-AzStorageAccount правильного имени параметра.

#### <a name="azstoragesync"></a>Az.StorageSync
* Добавлен командлет Invoke-AzStorageSyncChangeDetection.
* Исправлена проблема № 9551, связанная с TierFilesOlderThanDays.

#### <a name="azwebsites"></a>Az.Websites
* Исправлена ошибка, при которой некоторые свойства SiteConfig не возвращались Get-AzWebApp и Set-AzWebApp.
* Добавлен новый параметр Location в Get-AzDeletedWebApp и Restore-AzDeletedWebApp.
* Исправлена ошибка, которая возникала при клонировании слотов веб-приложений с помощью командлета New-AzWebApp-IncludeSourceWebAppSlots.

## <a name="240---july-2019"></a>2.4.0 — июль 2019 г.
#### <a name="azaccounts"></a>Az.Accounts
* Добавлена поддержка командлетов профиля.
* Добавлена поддержка сред и плоскостей данных в созданных командлетах.
* Исправлена ошибка, когда в командлетах плоскости данных в Windows PowerShell в некоторых случаях использовалась неправильная конечная точка.

#### <a name="azadvisor"></a>Az.Advisor
* Выпущена общедоступная версия Az.Advisor.
* Теперь этот модуль входит в сводный модуль `Az`.

#### <a name="azapimanagement"></a>Az.ApiManagement
* исправлена проблема https://github.com/Azure/azure-powershell/issues/8671.
    - **Get-AzApiManagementSubscription**
        - Добавлена поддержка запрашивания подписок по пользователю и продукту.
        - Добавлена поддержка создания запросов с использованием области "/", "/apis", "/apis/echo-api".
* Исправлены проблемы https://github.com/Azure/azure-powershell/issues/9307 и https://github.com/Azure/azure-powershell/issues/8432.
    - **Import-AzApiManagementApi**
        - Добавлена поддержка указания ApiVersion и ApiVersionSetId при импорте API-интерфейсов.

#### <a name="azautomation"></a>Az.Automation
* Исправлена ошибка командлета Set-AzAutomationConnectionFieldValue при обработке строкового значения.

#### <a name="azcompute"></a>Az.Compute
* В New AzImageConfig добавлен параметр HyperVGeneration.

#### <a name="azdatafactory"></a>Az.DataFactory
* Обновление выходных данных командлетов ADF, предназначенных для получения числа выполнений действий, конвейеров и триггеров, для поддержки канала Select-Object.

#### <a name="azeventgrid"></a>Az.EventGrid
* Исправлена опечатка в документации по командлету New-AzEventGridSubscription.

#### <a name="aziothub"></a>Az.IotHub
* Добавлена поддержка повторного создания ключей политики авторизации.

#### <a name="aznetwork"></a>Az.Network
* К тегам общедоступного IP-адреса добавлен тег RoutingPreference.
* Улучшены примеры для справочной документации по командлету Get-AzNetworkServiceTag.

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyState.
    - Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9446.

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Исправленная модель источника данных CustomLog возвращена в командлет Get-AzOperationalInsightsDataSource.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Выпущено исправление для команды get-policy для виртуальных машин IaaS.

#### <a name="azresources"></a>Az.Resources
    - Исправлен текст справки по параметру Get-AzPolicyState -Top.
    - Добавлена поддержка разбиения по страницам на стороне клиента для Get-AzPolicyAlias.
    - Добавлены новые параметры для Set-AzPolicyAssignment, -PolicyParameters и -PolicyParametersObject.
    - Добавлен ряд обновлений документов и примеров для командлетов политик.

#### <a name="azservicebus"></a>Az.ServiceBus
* Исправление ошибки № 4938: командлет New-AzureRmServiceBusQueue возвращает ответ BadRequest (Недопустимый запрос) при задании значения MaxSizeInMegabytes.

#### <a name="azsql"></a>Az.Sql
* Из выпуска предварительной версии в выпуск общедоступной версии добавлены командлеты группы отработки отказа экземпляра.
* Поддержка аудита Azure SQL Server и баз данных с помощью новых командлетов:
    - Set-AzSqlServerAudit
    - Get-AzSqlServerAudit
    - Remove-AzSqlServerAudit
    - Set-AzSqlDatabaseAudit
    - Get-AzSqlDatabaseAudit
    - Remove-AzSqlDatabaseAudit
* Из параметров оценки уязвимостей удалены ограничения, касающиеся электронной почты.

#### <a name="azstorage"></a>Az.Storage
* Два параметра в указанном ниже командлете — -IndexDocument и -ErrorDocument404Path, — которые ранее были обязательными, стали необязательными:
    -  Enable-AzStorageStaticWebsite
* Обновлена справка по командлету Get-AzStorageBlobContent: добавлен пример.
* При сбое выполнения командлета с ошибкой StorageException отображаются дополнительные сведения об ошибке.
* Добавлена поддержка создания или обновления учетной записи хранения с использованием проверки подлинности AAD DS для службы "Файлы Azure".
    -  New-AzStorageAccount
    -  Set-AzStorageAccount
* Добавлена поддержка перечисления или закрытия дескрипторов файлов для общей папки, каталога файлов или файла:
    - Get-AzStorageFileHandle
    - Close-AzStorageFileHandle

#### <a name="azstoragesync"></a>Az.StorageSync
* Теперь этот модуль входит в сводный модуль `Az`.

## <a name="232---june-2019"></a>2.3.2 — июнь 2019 г.
#### <a name="azaccounts"></a>Az.Accounts
* Исправлена ошибка, связанная с использованием неправильного URL-адреса для вызовов функций.
    - Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8983.
* Устранена проблема с псевдонимами из AzureRM для командлетов Az.
  - Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic.
  - Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest.

#### <a name="azcompute"></a>Az.Compute
* Простые наборы параметров New-AzVm и New-AzVmss теперь принимают параметр ProximityPlacementGroup.
* Исправлена опечатка в справочной документации по New-AzVM.

#### <a name="azdns"></a>Az.Dns
* Исправлена опечатка в справочных примерах по использованию Set-AzDnsZone.

#### <a name="azeventgrid"></a>Az.EventGrid
* Обновлен для использования API версии 2019-06-01.
* Новые командлеты:
    - New-AzureRmEventGridDomain
        - Создает домен Сетки событий Azure.
    - Get-AzureRmEventGridDomain
        - Возвращает сведения о домене Сетки событий или список всех доменов Сетки событий в текущей подписке Azure.
    - Remove-AzureRmEventGridDomain
        - Удаляет домен Сетки событий Azure.
    - New-AzureRmEventGridDomainKey
        - Повторно создает ключ общего доступа для домена Сетки событий Azure.
    - Get-AzureRmEventGridDomainKey
        - Возвращает ключи общего доступа, используемые для публикации событий в домене Сетки событий.
    - New-AzureRmEventGridDomainTopic
        - Создает раздел домена Сетки событий Azure.
    - Get-AzureRmEventGridDomainTopic
        - Возвращает сведения о разделе домена Сетки событий или список всех разделов определенного домена Сетки событий в текущей подписке Azure.
    - Remove-AzureRmEventGridDomainTopic
        - Удаляет раздел домена Сетки событий Azure.
* Обновлены командлеты:
    - New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription
        - Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для нового домена Сетки событий и раздела домена Сетки событий и позволяющие создавать подписки на события в этих ресурсах.
        - Добавляют новые обязательные параметры для указания имени нового домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют создавать подписки на события в этих ресурсах.
        - Добавляют новые наборы параметров для доменов и разделов домена и позволяют повторно использовать существующие параметры (например, EndPointType, SubjectBeginsWith и т. д.).
        - Добавлены новые необязательные параметры для указания:
            - срока действия подписки на событие;
            - параметров расширенной фильтрации.
        - Добавляют новое перечисление для ServiceBusQueue в качестве места назначения.
        - Запрещают использование значение All в параметре -IncludedEventType и заменяют его следующим:
    - Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription
        - Добавляют новые необязательные параметры (Top, ODataQuery и NextLink) для поддержки разбиения на страницы и фильтрации результатов.
    - Remove-AzureRmEventGridSubscription
        - Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для домена Сетки событий и раздела домена Сетки событий и позволяющие удалять подписки на события в этих ресурсах.
        - Добавляют новые обязательные параметры для указания имени домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют удалять подписки на события в этих ресурсах.

#### <a name="azfrontdoor"></a>Az.FrontDoor
* New-AzFrontDoorWafMatchConditionObject
    - Добавляет поддержку преобразований и новое значение оператора автозавершения (RegEx).
* New-AzFrontDoorWafManagedRuleObject
    - Добавляет новые значения автозавершения.

#### <a name="aznetwork"></a>Az.Network
* Добавляет поддержку ресурса шлюза виртуальной сети.
    - Новые командлеты
        - Get-AzVirtualNetworkGatewayVpnClientConnectionHealth
* Добавляет AvailablePrivateEndpointType.
    - Новые командлеты
        - Get-AzAvailablePrivateEndpointType
* Добавляет PrivatePrivateLinkService.
    - Новые командлеты
        - Get-AzPrivateLinkService
        - New-AzPrivateLinkService
        - Remove-AzPrivateLinkService
        - New-AzPrivateLinkServiceIpConfig
        - Set-AzPrivateEndpointConnection
* Добавляет PrivateEndpoint.
    - Новые командлеты
        - Get-AzPrivateEndpoint
        - New-AzPrivateEndpoint
        - Remove-AzPrivateEndpoint
        - New-AzPrivateLinkServiceConnection
* Обновлены следующие команды для функции: флаг UseLocalAzureIpAddress для VPN-подключения.
    - Обновлен командлет New-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.
    - Обновлен командлет Set-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.
* В пиринг ExpressRoute добавлено поле только для чтения PeeredConnections.
* В ExpressRoute добавлено поле только для чтения GlobalReachEnabled.
* Добавлен атрибут в рамках критического изменения, отменяющего статус устаревшего поля AllowGlobalReach в модели ExpressRouteCircuit.
* Исправлена проблема, связанная с ошибкой 8756, при использовании TargetListenerID с командлетами AzApplicationGatewayRedirectConfiguration.
* Исправлена ошибка в New-AzApplicationGatewayPathRuleConfig, не позволявшая задавать набор правил повторного создания.
* Исправлено отображение VirtualNetworkTaps в NetworkInterfaceIpConfiguration.
* Исправлены командлеты Cortex Get для отображения всех частей.
* Исправлено создание ссылок VirtualHub для ExpressRouteGateways и VpnGateway.
* В AzureFirewall и NatGateway добавлена поддержка Зон доступности.
* Добавлен командлет Get-AzNetworkServiceTag.
* Добавлена поддержка нескольких общедоступных IP-адресов для Брандмауэра Azure.
    - Обновлен командлет New-AzFirewall:
        - Добавлен параметр -PublicIpAddress, который принимает один или несколько объектов общедоступных IP-адресов.
        - Добавлен параметр -VirtualNetwork, который принимает объект виртуальной сети.
        - Добавлены методы AddPublicIpAddress и RemovePublicIpAddress для объекта брандмауэра. Они принимают объект общедоступного IP-адреса в качестве входных данных.
        - Не рекомендуется использовать параметры -PublicIpName и -VirtualNetworkName.
* Обновлены следующие команды для функции: В параметрах проверки подлинности AAD VPN-клиента задан ресурс шлюза виртуальной сети.
    - Обновлен командлет New-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.
    - Обновлен командлет Set-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.
    - Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр-переключатель RemoveAadAuthentication для удаления в шлюзе параметров проверки подлинности AAD VPN-клиента.

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Добавлена поддержка SKU **pergb2018** в команде New-AzureRmOperationalInsightsWorkspace.

#### <a name="azresources"></a>Az.Resources
* Поддержка дополнительных вариантов экспорта шаблона.
    - В Export-AzResourceGroup добавлен параметр -SkipResourceNameParameterization.
    - В Export-AzResourceGroup добавлен параметр -SkipAllParameterization.
    - В Export-AzResourceGroup добавлен параметр -Resource для фильтрации экспортированных ресурсов.

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Исправлена ошибка, связанная с получением иногда неправильных отпечатков при добавлении сертификата ByExistingKeyVault.

#### <a name="azsql"></a>Az.Sql
* Исправлен суффикс конечной точки хранилища службы "Расширенная защита от угроз Azure".
* Исправлена ошибка, связанная с возможностью пакета "Расширенная защита данных" переопределять политику службы "Расширенная защита от угроз".
* Новые командлеты для Management.Sql позволяют клиентам добавлять ключи TDE и задавать средство защиты TDE для управляемых экземпляров.
   - Add-AzSqlInstanceKeyVaultKey
   - Get-AzSqlInstanceKeyVaultKey
   - Remove-AzSqlInstanceKeyVaultKey
   - Get-AzSqlInstanceTransparentDataEncryptionProtector
   - Set-AzSqlInstanceTransparentDataEncryptionProtector

#### <a name="azstorage"></a>Az.Storage
* Поддержка класса Kind в FileStorage и значения Premium_ZRS в SkuName при создании учетной записи хранения.
    - New-AzStorageAccount
* Уточнено описание командлета неизменности BLOB-объектов.
    -  Remove-AzRmStorageContainerImmutabilityPolicy

#### <a name="azwebsites"></a>Az.Websites
* Оптимизирует Get-AzWebAppCertificate для фильтрации по группе ресурсов на сервере, а не в клиенте.
* Добавляет параметр-переключатель - UseDisasterRecovery в Get AzWebAppSnapshot.

## <a name="220---june-2019"></a>2.2.0 — июнь 2019 г.
#### <a name="azcdn"></a>Az.Cdn
* Обновлены командлеты для поддержки функции rulesEngine на основе API версии 2019-04-15.

#### <a name="azcompute"></a>Az.Compute
* Добавлен параметр `NoWait`, который запускает операцию и немедленно возвращает значение еще до завершения операции.
    - Обновлены командлеты:   Export-AzLogAnalyticRequestRateByInterval; Export-AzLogAnalyticThrottledRequest; Remove-AzVM; Remove-AzVMAccessExtension; Remove-AzVMAEMExtension; Remove-AzVMChefExtension; Remove-AzVMCustomScriptExtension; Remove-AzVMDiagnosticsExtension; Remove-AzVMDiskEncryptionExtension; Remove-AzVMDscExtension; Remove-AzVMSqlServerExtension; Restart-AzVM; Set-AzVM; Set-AzVMAccessExtension; Set-AzVMADDomainExtension; Set-AzVMAEMExtension; Set-AzVMBginfoExtension; Set-AzVMChefExtension; Set-AzVMCustomScriptExtension; Set-AzVMDiagnosticsExtension; Set-AzVMDscExtension; Set-AzVMExtension; Start-AzVM; Stop-AzVM; Update-AzVM.

#### <a name="azeventhub"></a>Az.EventHub
* Исправлена ошибка № 9231. Командлет Get-AzEventHubNamespace не возвращал теги.
* Исправлена ошибка № 9230. Командлет Get-AzEventHubNamespace возвращал значение ResourceGroup вместо ResourceGroupName.

#### <a name="aznetwork"></a>Az.Network
* Обновлены параметры ResourceId и InputObject для ресурса Шлюза NAT.
    - Добавлены псевдонимы для параметров ResourceId и InputObject.

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyEvent.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Минимальный срок хранения политики IaaSVM изменился с 1 до 7 дней.

#### <a name="azservicebus"></a>Az.ServiceBus
* Исправлена ошибка № 9182. Командлет Get-AzServiceBusNamespace возвращал ResourceGroup вместо ResourceGroupName.

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Исправлена опечатка в сообщении об ошибке для командлета Update-AzServiceFabricReliability.
* Добавлен отсутствующий символ в командных строках Service Fabric.

#### <a name="azsql"></a>Az.Sql
* Для командлета New-AzureSqlInstance добавлен параметр DnsZonePartner, обеспечивающий поддержку AutoDr для Управляемого экземпляра.
* Командлет Get-AzSqlDatabaseSecureConnectionPolicy объявлен неподдерживаемым.
* Командлеты обнаружения угроз переименованы в командлеты Расширенной защиты от угроз.
* Параметры -StorageSizeInGB и -LicenseType командлета New-AzSqlInstance теперь необязательны.

#### <a name="azwebsites"></a>Az.Websites
* Исправлены проблемы, когда удалялись теги при использовании Set-AzWebApp и Set-AzWebAppSlot со свойством -WebApp.

## <a name="210---may-2019"></a>2.1.0 — май 2019 г.
#### <a name="azapimanagement"></a>Az.ApiManagement
* Созданы командлеты для управления диагностикой в глобальной области и в области API.
    - **Get-AzApiManagementDiagnostic** — получение диагностики, заданной глобально или на уровне области API.
    - **New-AzApiManagementDiagnostic** — создание диагностики в глобальной области или в области API.
    - **New-AzApiManagementHttpMessageDiagnostic** — создание параметра диагностики, для которого регистрируются заголовки и размер байтов тела.
    - **New-AzApiManagementPipelineDiagnosticSetting** — создание параметров диагностики для сообщений HTTP, поступающих в шлюз или исходящих из него.
    - **New-AzApiManagementSamplingSetting** — создание параметра выборки для запросов и ответов касательно диагностики.
    - **Remove-AzApiManagementDiagnostic** — удаление объекта диагностики в глобальной области или в области API.
    - **Set-AzApiManagementDiagnostic** — обновление объекта диагностики в глобальной области или в области API.
* Созданы командлеты для управления кэшем в службе ApiManagement.
    - **Get-AzApiManagementCache** — получение сведений о кэше, указанном идентификатором, или обо всех кэшах.
    - **New-AzApiManagementCache** — создание кэша по умолчанию или кэша в определенном регионе Azure.
    - **Remove-AzApiManagementCache** — удаление кэша.
    - **Update-AzApiManagementCache** — обновление кэша.
* Созданы командлеты для управления схемой API.
    - **New-AzApiManagementSchema** — создание схемы для API.
    - **Get-AzApiManagementSchema** — получение схем, настроенных в API.
    - **Remove-AzApiManagementSchema** — удаление схемы, настроенной в API.
    - **Set-AzApiManagementSchema** — обновление схемы, настроенной в API.
* Создан командлет для создания токена пользователя.
    - **New-AzApiManagementUserToken** — создание токена пользователя, по умолчанию действительного в течение 8 часов. С помощью этого командлета можно создавать токен для пользователя GIT.
* Создан командлет для получения состояния сети.
    - **Get-AzApiManagementNetworkStatus** — получение состояния подключения сети ресурсов, от которых зависит служба "Управление API". Это полезно при развертывании службы ApiManagement в виртуальной сети и проверке того, не нарушена ли какая-либо из зависимостей.
* Обновлен командлет **New-AzApiManagement** для управления службой ApiManagement.
    - Добавлена поддержка нового SKU Consumption.
    - Добавлена поддержка для включения флага EnableClientCertificate в SKU Consumption.
    - Новый командлет **New-AzApiManagementSslSetting** позволяет настраивать параметр TLS/SSL для сервера (Backend) и внешнего интерфейса (Frontend). Его также можно использовать для настройки Ciphers как 3DES, в ServerProtocols как Http2 для внешнего интерфейса (Frontend) службы ApiManagement.
    - Добавлена поддержка настройки имени узла DeveloperPortal в службе ApiManagement.
* Обновлен командлет **Get-AzApiManagementSsoToken** для извлечения объекта PsApiManagement в качестве входных данных.
* Обновлен командлет для отображения встроенных сообщений об ошибках.
     > PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Код ошибки: ValidationError. Сообщение об ошибке: "Некоторые поля содержат неправильные значения". Сведения об ошибке: [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]
* Обновлен командлет **Export-AzApiManagementApi** для экспортирования программных интерфейсов в формате OpenApi 3.0.
* Обновлен командлет **Import-AzApiManagementApi**:
    - Для импортирования API из спецификации документа OpenApi 3.0.
    - Для переопределения свойства PsApiManagementSchema, указанного в любом документе (Swagger, Wadl, Wsdl, OpenApi).
    - Для переопределения свойства ServiceUrl, указанного в любом документе.
* Обновлен командлет **Get-AzApiManagementPolicy** для возврата политики в формате, экранированном не для XML, с использованием rawxml.
* Обновлен командлет **Set-AzApiManagementPolicy**. Он принимает политику в формате, экранированном не для XML, с использованием rawxml и в формате, экранированном для XML, с использованием XML.
* Обновлен командлет **New-AzApiManagementApi**:
    - Для настройки API с помощью сервера авторизации OpenId.
    - Для создания API в ApiVersionSet.
    - Для клонирования API с использованием значений SourceApiId и SourceApiRevision.
    - Возможность настройки параметра SubscriptionRequired в области API.
* Обновлен командлет **Set-AzApiManagementApi**:
    - Для настройки API с помощью сервера авторизации OpenId.
    - Для обновления API в ApiVersionSet.
    - Возможность настройки параметра SubscriptionRequired в области API.
* Обновлен командлет **New-AzApiManagementRevision**:
    - Для клонирования (копирования тегов, продуктов, операций и политик) существующей редакции с использованием SourceApiRevision. Новая редакция предполагает родительский идентификатор ApiId.
    - Для предоставления ApiRevisionDescription.
    - Для переопределения значения ServiceUrl при клонировании API.
* Обновлен командлет **New-AzApiManagementIdentityProvider**:
    - Для настройки AAD или AADB2C с Authority.
    - Для установки политик SignupPolicy, SigninPolicy, ProfileEditingPolicy и PasswordResetPolicy.
* Обновлен командлет **New-AzApiManagementSubscription**.
    - Для учета новой модели SubscriptonModel с помощью Scope и UserId.
    - Для учета прежней модели подписки с помощью ProductId и UserId.
    - Добавлена поддержка для включения AllowTracing на уровне подписки.
* Обновлен командлет **Set-AzApiManagementSubscription**.
    - Для учета новой модели SubscriptonModel с помощью Scope и UserId.
    - Для учета прежней модели подписки с помощью ProductId и UserId.
    - Добавлена поддержка для включения AllowTracing на уровне подписки.
* Следующие командлеты обновлены, чтобы принимать значение ResourceId в качестве входных данных.
    - New-AzApiManagementContext.
        > New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso
    - Get-AzApiManagementApiRelease.
        > Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId
    - Get-AzApiManagementApiVersionSet.
        > Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset
    - Get-AzApiManagementAuthorizationServer.
    - Get-AzApiManagementBackend.
        > Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric
    - Get-AzApiManagementCertificate.
    - Remove-AzApiManagementApiVersionSet.
    - Remove-AzApiManagementSubscription.

#### <a name="azautomation"></a>Az.Automation
* Обновлен командлет Get-AzAutomationJobOutputRecord для обработки значений в формате JSON и в виде текстовой записи.
    - исправлена проблема https://github.com/Azure/azure-powershell/issues/7977.
    - исправлена проблема https://github.com/Azure/azure-powershell/issues/8600.
* Поведение командлета Start-AzAutomationDscCompilationJob изменено так, чтобы сразу же запустить задание, а не ждать его завершения.
    * исправлена проблема https://github.com/Azure/azure-powershell/issues/8347.
* Исправлен командлет Get-AzAutomationDscNode, возвращающий все узлы при использовании -Name. Теперь он возвращает только соответствующий узел.

#### <a name="azcompute"></a>Az.Compute
* Добавлены параметры ProtectFromScaleIn и ProtectFromScaleSetAction для командлета Update-AzVmssVM.
* Командлет New-AzVM с простым набором параметров теперь по умолчанию использует доступное расположение, если регион "восточная часть США" не поддерживается.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Обновлен пакет SDK ADLS для использования httpclient. В инфраструктуру Azure интегрирована проверка плоскости данных.

#### <a name="azmonitor"></a>Az.Monitor
* Исправлены неправильные имена параметров в справочных примерах.

#### <a name="aznetwork"></a>Az.Network
* Добавлен флаг DisableBgpRoutePropagation для выходных данных действующей таблицы маршрутов.
    - Обновлен командлет:
        - Get-AzEffectiveRouteTable.
* Исправлен двойной дефис в документации New-AzApplicationGatewayTrustedRootCertificate.

#### <a name="azresources"></a>Az.Resources
* Добавлен новый командлет Get-AzureRmDenyAssignment для получения запрещающих назначений.

#### <a name="azsql"></a>Az.Sql
* Командлеты Расширенной защиты от угроз переименованы на командлеты Расширенной защиты данных, и оценка уязвимости включена по умолчанию.

## <a name="200---may-2019"></a>2.0.0 — май 2019 г.
#### <a name="azaccounts"></a>Az.Accounts
* Обновлена библиотека аутентификации для устранения проблем с ADFS при использовании аутентификации на основе имени пользователя и пароля.

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Отображается только заявление об отказе Bing для служб Поиска Bing.
* Исправлена проблема с созданием учетной записи.

#### <a name="azcompute"></a>Az.Compute
* Функция группы размещения близкого взаимодействия.
    - Добавлены следующие новые командлеты:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup
    - Новый параметр ProximityPlacementGroupId будет добавлен в следующие командлеты:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig
* В командлет New-AzGalleryImageVersion добавлен параметр StorageAccountType.
* TargetRegion в командлете New-AzGalleryImageVersion может содержать StorageAccountType.
* Параметр-переключатель SkipShutdown добавлен в командлеты Stop-AzVM и Stop-AzVmss.
* Критические изменения
    - Командлет SET-AzVMBootDiagnostics изменен на Set-AzVMBootDiagnostic.
    - Командлет Export-AzLogAnalyticThrottledRequests изменен на Export-AzLogAnalyticThrottledRequests.

#### <a name="azdeploymentmanager"></a>Az.DeploymentManager
* Первая общедоступная версия командлетов диспетчера развертывания Azure

#### <a name="azdns"></a>Az.Dns
* Автоматическое делегирование DNS-сервера
    - Командлет для создания зоны DNS принимает имя родительской зоны в качестве дополнительного необязательного параметра.
    - Он добавляет записи NS в родительской зоне для созданной дочерней зоны.

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Первая общедоступная версия командлетов Azure FrontDoor.
* Переименованы командлеты WAF для включения Waf.
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a>Az.HDInsight
* Удалены два командлета:
    - Grant-AzHDInsightHttpServicesAccess
    - Revoke-AzHDInsightHttpServicesAccess
* Добавлен новый командлет Set-AzHDInsightGatewayCredential для замены Grant-AzHDInsightHttpServicesAccess.
* Обновлен командлет Get-AzHDInsightJobOutput для различения ролей читателя и оператора HDInsight:
    - Пользователям с ролью читателя не нужно указывать параметр DefaultStorageAccountKey явным образом, иначе возникает ошибка.
    - На пользователей с ролью оператора HDInsight это не повлияет.

#### <a name="azmonitor"></a>Az.Monitor
* Новые командлеты для API SQR (запланированное правило запросов)
    - New-AzScheduledQueryRuleAlertingAction
    - New-AzScheduledQueryRuleAznsActionGroup
    - New-AzScheduledQueryRuleLogMetricTrigger
    - New-AzScheduledQueryRuleSchedule
    - New-AzScheduledQueryRuleSource
    - New-AzScheduledQueryRuleTriggerCondition
    - New-AzScheduledQueryRule
    - Get-AzScheduledQueryRule
    - Set-AzScheduledQueryRule
    - Update-AzScheduledQueryRule
    - Remove-AzScheduledQueryRule
    - См. подробнее об [API SQR](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules).
    - Обновлен файл Az.Monitor.md для включения командлетов для правила генерации оповещений на основе метрик GenV2(не классическая версия).

#### <a name="aznetwork"></a>Az.Network
* Добавлена поддержка для ресурса Шлюза NAT.
    - Новые командлеты
        - New-AzNatGateway
        - Get-AzNatGateway
        - Set-AzNatGateway
        - Remove-AzNatGateway
   - Обновлены командлеты
        - New-AzureVirtualNetworkSubnetConfigCommand
        - Add-AzureVirtualNetworkSubnetConfigCommand
* Обновлены следующие команды для функции: Настройка и удаление пользовательских маршрутов через шлюз в Бруклине.
    - Обновлен командлет New-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.
    - Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Добавлена поддержка сведений об оценке политики запросов.
    - Добавлен параметр -Expand в командлет Get-AzPolicyState. Добавлена поддержка -Expand PolicyEvaluationDetails.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Добавлена поддержка перекрестной подписки на Azure Site Recovery.
* Добавлена возможность отмечать предстоящие критически важные изменения для Azure Site Recovery.
* Исправлены план восстановления и план действий для Azure Site Recovery.
* Исправлено сетевое сопоставление обновления Azure Site Recovery (Azure — Azure).
* Исправлено направление защиты обновления Azure Site Recovery для управляемых дисков (Azure — Azure).
* Добавлены другие незначительные исправления.

#### <a name="azrelay"></a>Az.Relay
* Исправлены опечатки в сообщениях для клиентов.

#### <a name="azservicebus"></a>Az.ServiceBus
* Добавлены новые командлеты для NetworkRuleSet пространства имен.

#### <a name="azstorage"></a>Az.Storage
* Выполнено обновление клиентской библиотеки хранилища до версии 10.0.1 (пространство имен всех объектов из этого пакета SDK изменено с Microsoft.WindowsAzure.Storage. *на Microsoft.Azure.Storage*).
* Выполнено обновление до Microsoft.Azure.Management.Storage версии 11.0.0 для включения поддержки нового API версии 2019-04-01.
* Значение свойства Kind по умолчанию в учетной записи хранения изменено со Storage на StorageV2.
    - New-AzStorageAccount
* Изменено значение Sku.Name в выходных данных командлета учетной записи хранения в соответствии со значением Sku.Name во входных данных путем добавления _ (например, StandardLRS изменено на Standard_LRS).
    - New-AzStorageAccount
    - Get-AzStorageAccount
    - Set-AzStorageAccount

#### <a name="azwebsites"></a>Az.Websites
* Свойство Kind теперь будет задаваться объектам PSSite, возвращаемым командлетом Get-AzWebApp.
* Get-AzWebApp*Metrics и Get-AzAppServicePlanMetrics считаются нерекомендуемыми.

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
