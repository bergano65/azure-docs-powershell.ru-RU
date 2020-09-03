---
title: Журнал изменений Azure PowerShell | Документация Майкрософт
description: Это руководство содержит историю изменений Azure PowerShell, внесенных в новом выпуске.
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 08/28/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 189b360f8825b7de93b67b0b2cbe670d00187327
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "89241361"
---
# <a name="release-notes"></a>Заметки о выпуске

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

Здесь приведен список изменений, внесенных в Azure PowerShell в этом выпуске.

---
## <a name="6130---november-2018"></a>6.13.0 — ноябрь 2018 г.
#### <a name="azurermprofile"></a>AzureRM.Profile
* Обновлен общий код для использования последней версии ClientRuntime.

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Обновлены зависимости для устранения проблемы сопоставления типов.

#### <a name="azurermautomation"></a>AzureRM.Automation
* Командлеты службы автоматизации Azure на базе Swagger.
* Добавлены командлеты для Управления обновлениями.
* Добавлены командлеты для системы управления версиями.
* Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.
* Исправлена команда DSC для регистрации узла.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Исправлена проблема с удостоверением, назначаемым системой.
* Обновлены зависимости для устранения проблемы сопоставления типов.

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* Обновлены зависимости для устранения проблемы сопоставления типов.

#### <a name="azurermmarketplaceordering"></a>AzureRM.MarketplaceOrdering
* Обновлено описание в примерах командлетов для Marketplace.

#### <a name="azurermnetwork"></a>AzureRM.Network
* Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.
* Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.
* Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.
* Исправлены проблемы с использованием памяти в карте виртуальной сети.

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.
* Параметры часового пояса преобразованы в верхний регистр.

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.
* Обновлены зависимости для устранения проблемы сопоставления типов.

#### <a name="azurermrelay"></a>AzureRM.Relay
* Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.

#### <a name="azurermresources"></a>AzureRM.Resources
* Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.
* Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.
* Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.

#### <a name="azurermsql"></a>AzureRM.Sql
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

## <a name="6120---november-2018"></a>6.12.0 — ноябрь 2018 г.
#### <a name="azurermprofile"></a>AzureRM.Profile
* Обновлен общий код для использования последней версии ClientRuntime.
* В командлете Connect-AzureRmAccount параметр TenantId переименован на Tenant и добавлен псевдоним для TenantId.
* Обновлено описание TenantId для командлета Connect-AzureRmAccount.
* Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.
    - https://github.com/Azure/azure-powershell/issues/6936
* Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.
    - https://github.com/Azure/azure-powershell/issues/7453
* Устранена проблема с конечными точками DataLake при использовании MSI.
    - https://github.com/Azure/azure-powershell/issues/7462
* Устранена проблема, при которой командлет Disconnect-AzureRmAccount вызывал сбой при отсутствии подключения.
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azurermautomation"></a>AzureRM.Automation
* Имя файла библиотеки DLL командлетов переименовано на Microsoft.Azure.Commands.Automation.dll.

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* Добавлена операция Get-AzureRmCognitiveServicesAccountSkus.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Добавлены командлеты Add-AzureRmVmssVMDataDisk и Remove-AzureRmVmssVMDataDisk.
* Get-AzureRmVMImage отображает AutomaticOSUpgradeProperties.
* Устранена проблема, при которой значения параметров SetAzureRmVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Обновлен пакет DataLake до версии 1.1.10.
* Параметр по умолчанию Concurrency добавлен к многопоточным операциям.

#### <a name="azurerminsights"></a>AzureRM.Insights;
* Исправлена проблема № 7267 (область автомасштабирования).
    - Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).
* Исправлена проблема № 7513 [Insights], ппри которой для командлета Set-AzureRMDiagnosticSetting требовалось явное указание категорий во время создания параметра.
    - Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.

#### <a name="azurermnetwork"></a>AzureRM.Network
* Параметр PeeringType является обязательным для следующих командлетов:
    - Get-AzureRmExpressRouteCircuitRouteTable
    - Get-AzureRmExpressRouteCircuitARPTable
    - Get-AzureRmExpressRouteCircuitRouteTableSummary
    - Get-AzureRMExpressRouteCrossConnectionArpTable
    - Get-AzureRMExpressRouteCrossConnectionRouteTable
    - Get-AzureRMExpressRouteCrossConnectionRouteTableSummary

#### <a name="azurermpolicyinsights"></a>AzureRM.PolicyInsights
* Добавлена политика исправления командлетов.

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* Добавлена поддержка общих файловых ресурсов Azure в Службах восстановления.

#### <a name="azurermresources"></a>AzureRM.Resources
* Исправление для https://github.com/Azure/azure-powershell/issues/7402.
    - Разрешено перечисление ресурсов с использованием параметра -ResourceId для командлета Get-AzureRmResource.

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Устранена проблема с добавлением сертификата в VMSS Linux.
* Исправлен командлет Add-AzureRmServiceFabricClusterCertificate.
    - Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).
    - Исключение отображается правильно (Azure/service-fabric-issues#1054).
* Исправлен командлет Update-AzureRmServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.

## <a name="6110---october-2018"></a>6.11.0 — октябрь 2018 г.
#### <a name="azurermprofile"></a>AzureRM.Profile
* Устранена проблема с Get-AzureRmSubscription в CloudShell.
* Обновлен общий код для использования последней версии ClientRuntime.

#### <a name="azurermbackup"></a>AzureRM.Backup
* Командлеты Azure Backup объявлены нерекомендуемыми.

#### <a name="azurermcompute"></a>AzureRM.Compute
* В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzureRmVm.
* Во все командлеты добавлено средство заполнения для аргумента ResourceName.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Добавлена поддержка правил виртуальной сети:
    - Get-AzureRmDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.
    - Add-AzureRmDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.
    - Set-AzureRmDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.
    - Remove-AzureRmDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.

#### <a name="azurermnetwork"></a>AzureRM.Network
* Обновлен командлет Test-AzureRmNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.
* Во все командлеты добавлено средство заполнения для аргумента ResourceName.

#### <a name="azurermresources"></a>AzureRM.Resources
* Мы устранили проблему, из-за которой командлет Get-AzureRMRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), и добавили понятное исключение. Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.

## <a name="6100---october-2018"></a>6.10.0 — октябрь 2018 г.
#### <a name="azurestorage"></a>Azure.Storage;
* Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.
    - Start-AzureStorageBlobCopy
    - Start-AzureStorageFileCopy

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* Поддержка Get-AzureRmCognitiveServicesAccountSkus без существующей учетной записи.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Исправлена команда Get-AzureRmVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов.
* Добавлен пример использования SimpleParameterSet в справку командлета New-AzureRmVmss.
* Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Пакет .NET SDK для ADF обновлен до версии 2.3.0.

#### <a name="azurermnetwork"></a>AzureRM.Network
* Добавлена функциональность NetworkProfile. Добавлены новые командлеты:
    - Get-AzureRMNetworkProfile
    - New-AzureRMNetworkProfile
    - Remove-AzureRMNetworkProfile
    - Set-AzureRMNetworkProfile
    - New-AzureRMContainerNicConfig
    - New-AzureRmContainerNicConfigIpConfig
* Добавлен канал связи служб в модель подсети.
* Добавлены командлеты: New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap.
* Добавлены командлеты: Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig

#### <a name="azurermrediscache"></a>AzureRM.RedisCache
* С этого момента добавлена поддержка любой строки в качестве параметра Size. Добавлено значение P5 во всплывающее окно PSArgumentCompleter.

#### <a name="azurermresources"></a>AzureRM.Resources
* Добавлен отсутствующий параметр -Mode в командлет Set-AzureRmPolicyDefinition.
* Исправлена ошибка командлета Get-AzureRmProviderOperation для операций, когда Origin содержит User.

#### <a name="azurermsql"></a>AzureRM.Sql
* Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.

#### <a name="azurermstorage"></a>AzureRM.Storage
* Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.
    - Get-AzureRmStorageUsage

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Новый командлет Get-AzureRMWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера.
* Новые командлеты New-AzureRMWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows.

## <a name="690---september-2018"></a>6.9.0 — сентябрь 2018 г.
#### <a name="general"></a>Общие сведения
* В модуль развертывания AzureRM добавлен командлет AzureRM.SignalR.

#### <a name="azurermprofile"></a>AzureRM.Profile
* Незначительные изменения в общем коде хранилища.
* Обновлены файлы справки, в которые добавлены полные типы параметров.
* В наборе параметров ServicePrincipalCertificateWithSubscriptionId параметр -ServicePrincipal теперь стал необязательным.

#### <a name="azurestorage"></a>Azure.Storage;
* Поддержка создания контекста хранилища с использованием OAuth.
    - New-AzureStorageContext

#### <a name="azurermcdn"></a>AzureRM.Cdn
* Добавлен номер SKU для расценок на Standard_Microsoft в CDN.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Keyvault и Storage перенесены в общие зависимости.
* Добавлена поддержка большего количества размеров виртуальных машин в командлеты AEM.
* Добавлен параметр PublicIPPrefix в командлет New-AzureRmVmssIpConfig.
* Добавлен параметр ResourceId в командлет Invoke-AzureRmVMRunCommand.
* Добавлен командлет Invoke-AzureRmVmssVMRunCommand.

#### <a name="azurermdns"></a>AzureRM.Dns
* Добавлена поддержка для псевдонима записи во время создания записи DNS.

#### <a name="azurerminsights"></a>AzureRM.Insights;
* Исправлены проблемы № 6833 и № 7102 (область настроек диагностики).
    - Проблемы с именем по умолчанию, например service, во время создания, получения и отображения списка параметров диагностики.
    - Проблемы при создании параметров диагностики с категориями.
* Добавлено сообщение о том, что не рекомендуется использовать параметры интервалов времени в метриках.
    - Параметры интервалов времени по-прежнему принимаются (это не критическое изменение), но они игнорируются в серверной части, потому что действительно только значение PT1M.

#### <a name="azurermnetwork"></a>AzureRM.Network
* Изменения командлетов LoadBalancer
  - LoadBalancerInboundNatPoolConfig: добавлены параметры IdleTimeoutInMinutes, EnableFloatingIp и EnableTcpReset.
  - LoadBalancerInboundNatRuleConfig: добавлен параметр EnableTcpReset.
  - LoadBalancerRuleConfig: добавлен параметр EnableTcpReset.
  - LoadBalancerProbeConfig: добавлена поддержка значения Https для параметра Protocol.
* Добавлены новые команды для нового правила OutboundRule подресурса LoadBalancer.
  - Add-AzureRmLoadBalancerOutboundRuleConfig
  - Get-AzureRmLoadBalancerOutboundRuleConfig
  - New-AzureRmLoadBalancerOutboundRuleConfig
  - Set-AzureRmLoadBalancerOutboundRuleConfig
  - Remove-AzureRmLoadBalancerOutboundRuleConfig
* Добавлено новое свойство HostedWorkloads для PSNetworkInterface.
* Добавлены новые командлеты для функции "Брандмауэр Azure" (ARM):
  - Добавлен командлет Get-AzureRmFirewall.
  - Добавлен командлет Set-AzureRmFirewall.
  - Добавлен командлет New-AzureRmFirewall.
  - Добавлен командлет Remove-AzureRmFirewall.
  - Добавлен командлет New-AzureRmFirewallApplicationRuleCollection.
  - Добавлен командлет New-AzureRmFirewallApplicationRule.
  - Добавлен командлет New-AzureRmFirewallNatRuleCollection.
  - Добавлен командлет New-AzureRmFirewallNatRule.
  - Добавлен командлет New-AzureRmFirewallNetworkRuleCollection.
  - Добавлен командлет New-AzureRmFirewallNetworkRule.
* Добавлена поддержка конфигурации для доверенного корневого сертификата и автомасштабирования в Шлюзе приложений.
  - Добавлены новые командлеты:
      - Add-AzureRmApplicationGatewayTrustedRootCertificate
      - Get-AzureRmApplicationGatewayTrustedRootCertificate
      - New-AzureRmApplicationGatewayTrustedRootCertificate
      - Remove-AzureRmApplicationGatewayTrustedRootCertificate
      - Set-AzureRmApplicationGatewayTrustedRootCertificate
      - Get-AzureRmApplicationGatewayAutoscaleConfiguration
      - New-AzureRmApplicationGatewayAutoscaleConfiguration
      - Remove-AzureRmApplicationGatewayAutoscaleConfiguration
      - Set-AzureRmApplicationGatewayAutoscaleConfiguration
  - В следующие командлеты добавлен необязательный параметр -TrustedRootCertificate:
      - New-AzureRmApplicationGateway
      - Set-AzureRmApplicationGateway
      - New-AzureRmApplicationGatewayBackendHttpSetting
      - Set-AzureRmApplicationGatewayBackendHttpSetting
  - В следующие командлеты добавлен необязательный параметр -AutoscaleConfiguration:
      - New-AzureRmApplicationGateway
      - Set-AzureRmApplicationGateway
* Добавлен командлет для конечной точки интерфейса Get-AzureInterfaceEndpoint.
* Добавлена поддержка нескольких префиксов адресов в подсети. Обновлены командлеты:
  - New-AzureRmVirtualNetworkSubnetConfig
  - Set-AzureRmVirtualNetworkSubnetConfig
  - Add-AzureRmVirtualNetworkSubnetConfig
  - Get-AzureRmVirtualNetworkSubnetConfig
  - Add-AzureRmApplicationGatewayAuthenticationCertificate
  - Add-AzureRmApplicationGatewayFrontendIPConfig
  - New-AzureRmApplicationGatewayFrontendIPConfig
  - Set-AzureRmApplicationGatewayFrontendIPConfig
  - Add-AzureRmApplicationGatewayIPConfiguration
  - New-AzureRmApplicationGatewayIPConfiguration
  - Set-AzureRmApplicationGatewayIPConfiguration
  - Add-AzureRmNetworkInterfaceIpConfig
  - New-AzureRmNetworkInterfaceIpConfig — Set-AzureRmNetworkInterfaceIpConfig
  - New-AzureRmVirtualNetworkGatewayIpConfig
  - Add-AzureRmVirtualNetworkGatewayIpConfig;
  - Set-AzureRmLoadBalancerFrontendIpConfig
  - Add-AzureRmLoadBalancerFrontendIpConfig
  - New-AzureRmLoadBalancerFrontendIpConfig
  - New-AzureRmNetworkInterface
* Добавлены командлеты для делегирования подсети.
  - New-AzureRmDelegation: создание делегирования, которое можно добавить к подсети.
  - Remove-AzureRmDelegation: принятие подсети и удаление указанного имени делегирования из этой подсети.
  - Add-AzureRmDelegation: принятие подсети и добавление указанного имени службы в качестве делегирования для этой подсети.
  - Get-AzureRmDelegation
  - Get-AzureRmAvailableServiceDelegations

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* Добавлена поддержка управляемого диска.

#### <a name="azurermrediscache"></a>AzureRM.RedisCache
* Обновлена зависимость Insights.

#### <a name="azurermresources"></a>AzureRM.Resources
* В командлет New-AzureRmResourceGroupDeployment добавлен новый параметр RollbackAction.
    - Добавлена поддержка OnErrorDeployment с новым параметром.
* Добавлена поддержка управляемого удостоверения при назначении политик.
* При назначении политики с помощью New-AzureRmPolicyAssignment параметры со значениями по умолчанию больше не требуются.
* Добавлен новый командлет Get-AzureRmPolicyAlias для получения псевдонимов политик.

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Устранена проблема № 7161.

#### <a name="azurermsignalr"></a>AzureRM.SignalR
* Обновлены номера SKU для Free_F1 и Standard_S1.
* Добавлены поле версии в объект PSSignalRResource и строка подключения в объект PSSignalRKeys.

#### <a name="azurermstorage"></a>AzureRM.Storage
* Добавлена поддержка политики неизменяемости в AzureRm.Storage.
    - Remove-AzureRmStorageAccountNetworkRule.
    - Get-AzureRmStorageContainer
    - Update-AzureRmStorageContainer
    - New-AzureRmStorageContainer
    - Remove-AzureRmStorageContainer
    - Add-AzureRmStorageContainerLegalHold
    - Remove-AzureRmStorageContainerLegalHold
    - Set-AzureRmStorageContainerImmutabilityPolicy
    - Get-AzureRmStorageContainerImmutabilityPolicy
    - Remove-AzureRmStorageContainerImmutabilityPolicy
    - Lock-AzureRmStorageContainerImmutabilityPolicy

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Добавлены два новых командлета: Get-AzureRmDeletedWebApp и Restore-AzureRmDeletedWebApp.
* New-AzureRmAppServicePlan: добавлен параметр -HyperV для создания плана службы приложений с контейнером Windows.
* New-AzureRmWebApp, New-AzureRmWebAppSlot, Set-AzureRmWebApp, Set-AzureRmWebAppSlot: добавлены новые параметры (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) для создания контейнера приложения Windows и управления им.

## <a name="681---august-2018"></a>6.8.1 — август 2018 г.
#### <a name="general"></a>Общие сведения
* Исправлена проблема с отсутствием настройки группы ресурсов по умолчанию.
* Обновлены общие сборки среды выполнения

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Исправлена проблема с отсутствием настройки группы ресурсов по умолчанию.
* Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6603.
    - Командлеты Import-AzureRmApiManagementApi и *-AzureRmApiManagementCertificate теперь обрабатывают относительные пути.
* Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6879.
    - CertificateInformation — это задаваемое свойство, обеспечивающее правильную работу командлета Set-AzureRmApiManagement. Проблема исправлена путем обновления пакета NuGet до версии 4.0.4-preview.
* Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6853.
    - Исправлен фильтр OData для поиска по имени продукта.
* Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6814.
    - Исправлен фильтр OData для поиска по имени API.
* Добавлена поддержка средства ведения журнала Azure Monitor.


#### <a name="azurermcompute"></a>AzureRM.Compute
* Исправлена проблема с отсутствием в выходных данных ошибки целевого объекта.
* Исправлена проблема с типом учетной записи хранения для виртуальной машины с управляемым диском.
* Исправлена проблема с отсутствием настройки группы ресурсов по умолчанию.
* Исправлены командлеты расширения AEM для других сред, например Azure для Китая.

#### <a name="azurermnetwork"></a>AzureRM.Network
* Стандартное представление выходных данных командлетов изменено на представление таблиц.

#### <a name="azurermpowerbiembedded"></a>AzureRM.PowerBIEmbedded
* Исправлена проблема с Update-AzureRmPowerBIEmbeddedCapacity при попытке масштабировать приостановленную емкость.


#### <a name="azurermresources"></a>AzureRM.Resources
* Исправлена проблема с созданием управляемых приложений из Marketplace.

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Исправленные проблемы
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Добавлена поддержка метода маршрутизации MultiValue.
    - Добавлен новый параметр MaxReturn для маршрутизации MultiValue.
* Добавлена поддержка метода маршрутизации Subnet.
    - Добавлена поддержка диапазонов IP-адресов (подсетей) в конечных точках.
* Добавлена поддержка пользовательских заголовков в профилях.
* Добавлена поддержка диапазонов кода ожидаемого состояния в профилях.
* Добавлена поддержка пользовательских заголовков в конечных точках.

## <a name="680---august-2018"></a>6.8.0 — август 2018 г.
#### <a name="general"></a>Общие сведения
* Исправлена проблема с отсутствием настройки группы ресурсов по умолчанию.

#### <a name="azurermprofile"></a>AzureRM.Profile
* Добавлено свойство срока действия для маркеров, возвращенных при выполнении Connect-AzureRmAccount.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Исправлена проблема с отсутствием в выходных данных ошибки целевого объекта.
* Исправлена проблема с типом учетной записи хранения для виртуальной машины с управляемым диском.
* Исправлены командлеты расширения AEM для других сред, например Azure для Китая.

#### <a name="azurermiothub"></a>AzureRM.IotHub
* Исправлены примеры для New-AzureRmIotHubExportDevices и New-AzureRmIotHubImportDevices.

#### <a name="azurermnetwork"></a>AzureRM.Network
* Изменено представление моделей по умолчанию на представление таблиц.

#### <a name="azurermpowerbiembedded"></a>AzureRM.PowerBIEmbedded
* Исправлена проблема с Update-AzureRmPowerBIEmbeddedCapacity при попытке масштабировать приостановленную емкость.

#### <a name="azurermresources"></a>AzureRM.Resources
* Исправлена проблема с созданием управляемого приложения из marketplace.

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Исправления проблем
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Добавлена поддержка метода маршрутизации MultiValue.
    - Добавлен новый параметр MaxReturn для маршрутизации MultiValue.
* Добавлена поддержка метода маршрутизации Subnet.
    - Добавлена поддержка диапазонов IP-адресов (подсетей) в конечных точках.
* Добавлена поддержка пользовательских заголовков в профилях.
* Добавлена поддержка диапазонов кода состояния ожидания в профилях.
* Добавлена поддержка пользовательских заголовков в конечных точках.

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Исправлена проблема с отсутствием правильной настройки группы ресурсов по умолчанию.

## <a name="670---august-2018"></a>6.7.0 — август 2018 г.
#### <a name="azurermprofile"></a>AzureRM.Profile
* Обновление до последней версии Azure ClientRuntime.
* Добавлен идентификатор пользователя для имени контекста по умолчанию, чтобы избежать конфликтов контекста.
    - https://github.com/Azure/azure-powershell/issues/6489
* Устранены проблемы с командлетом Clear-AzureRmContext, которые приводили к проблемам с выбором контекста #6398.
* Разрешено передавать домен клиента в параметр -TenantId для командлета Connect-AzureRmAccount.
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a>Azure.Storage;
* Удалено ограничение в 5 ТБ для квоты на общую папку Azure.
* Set-AzureStorageShareQuota

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azureanalysisservices"></a>Azure.AnalysisServices
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermapplicationinsights"></a>AzureRM.ApplicationInsights
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermautomation"></a>AzureRM.Automation
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermbackup"></a>AzureRM.Backup
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermbatch"></a>AzureRM.Batch
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermbilling"></a>AzureRM.Billing
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermcdn"></a>AzureRM.Cdn
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Обновление до последней версии Azure ClientRuntime.
* В командлет New-AzureRmVmssConfig добавлен параметр EvictionPolicy.
* Если расположение не указано, используйте в DiskFileParameterSet для New AzureRmVm расположение по умолчанию.
* Исправлено описание параметров в Save-AzureRmVMImage.
* Исправлен командлет Get-AzureRmVMDiskEncryptionStatus для определенных сценариев, связанных с однократным выполнением.

#### <a name="azurermconsumption"></a>AzureRM.Consumption:
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermcontainerregistry"></a>AzureRM.ContainerRegistry
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermdatafactories"></a>AzureRM.DataFactories
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Исправлена отладка, когда DebugPreference настраивается из командной строки PowerShell.
* Обновлен пример для Set-AzureRmDataLakeStoreItemAcl.
* Обновление до последней версии Azure ClientRuntime.
* Обновлен пример для Set-AzureRmDataLakeStoreItemAclEntry.

#### <a name="azurermdevtestlabs"></a>AzureRM.DevTestLabs
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermdns"></a>AzureRM.Dns
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermeventgrid"></a>AzureRM.EventGrid
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermhdinsight"></a>AzureRM.HDInsight
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurerminsights"></a>AzureRM.Insights;
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermiothub"></a>AzureRM.IotHub
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermlogicapp"></a>AzureRM.LogicApp
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermmachinelearning"></a>AzureRM.MachineLearning
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermmachinelearningcompute"></a>AzureRM.MachineLearningCompute
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermmarketplaceordering"></a>AzureRM.MarketplaceOrdering
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermmedia"></a>AzureRM.Media
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermnetwork"></a>AzureRM.Network
* Добавлен пример для Set-AzureRmLocalNetworkGateway.
* Добавлены примеры и описания для Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey и New-AzureRmVirtualNetworkGatewayConnection.
* Добавлены примеры для Remove-AzureRmVirtualNetworkGatewayIpConfig и Reset-AzureRmVirtualNetworkGateway.
* Добавлен пример для Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.
* Добавлен пример для Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.
* Добавлен пример для Set-AzureRmVirtualNetworkGatewayConnection.
* Повторно созданы командлеты для ApplicationSecurityGroup, RouteTable и Usage с помощью генератора кода последней версии.
* Уточнено сообщение об ошибке для Get-AzureRmVirtualNetworkSubnetConfig при попытке получить подсеть, которая не существует.

#### <a name="azurermnotificationhubs"></a>AzureRM.NotificationHubs
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights;
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermpolicyinsights"></a>AzureRM.PolicyInsights
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermpowerbiembedded"></a>AzureRM.PowerBIEmbedded
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermrecoveryservices"></a>AzureRM.RecoveryServices
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* Добавлен фильтр политик для командлета Get-AzureRmRecoveryServicesBackItem. Команда возвращает список элементов резервного копирования, защищенных политикой с заданным идентификатором.
* Обновление Microsoft.Azure.Management.RecoveryServices.Backup до версии 3.0.0-preview.
* Обновление до последней версии Azure ClientRuntime.
* Добавлен параметр TargetResourceGroupName для Restore-AzureRmRecoveryServicesBackupItem. Группа ресурсов, в которую восстанавливаются управляемые диски. Применимо к резервной копии виртуальной машины с управляемыми дисками.

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermrediscache"></a>AzureRM.RedisCache
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermrelay"></a>AzureRM.Relay
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermresources"></a>AzureRM.Resources
* Поддержка развертывания шаблонов в области подписки. Добавлены новые командлеты:
    - New-AzureRmDeployment
    - Get-AzureRmDeployment
    - Test-AzureRmDeployment
    - Remove-AzureRmDeployment
    - Stop-AzureRmDeployment
    - Save-AzureRmDeploymentTemplate
    - Get-AzureRmDeploymentOperation
* Устранена проблема, когда при передаче контекста в Set-AzureRmResource возникает ошибка.
    - https://github.com/Azure/azure-powershell/issues/5705
* Исправлен пример в New-AzureRmResourceGroupDeployment.
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermscheduler"></a>AzureRM.Scheduler
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermsql"></a>AzureRM.Sql
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermstorage"></a>AzureRM.Storage
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermstreamanalytics"></a>AzureRM.StreamAnalytics
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermtags"></a>AzureRM.Tags
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermusageaggregates"></a>AzureRM.UsageAggregates
* Обновление до последней версии Azure ClientRuntime.

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Обновление до последней версии Azure ClientRuntime.

## <a name="660---july-2018"></a>6.6.0 — июль 2018 г.
#### <a name="general"></a>Общие сведения
* Обновлены все файлы справки: включены полные типы параметров и исправлены типы входных и выходных данных.

#### <a name="azurermprofile"></a>AzureRM.Profile
* Обновлена библиотека Common.Strategy: теперь можно проверить, совместима ли текущая конфигурация ресурса с целевым ресурсом.
* В Common.Storage добавлены типы ps1xml.

#### <a name="azurestorage"></a>Azure.Storage;
* Добавлена поддержка для получения контекста хранилища из DefaultProfile.
* В свойства типов выходных данных командлетов добавлен атрибут Ps1XmlAttribute.

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6370.
    - В AutoMapper исправлена ошибка, препятствовавшая преобразованию PsApiManagementApi в ApiContract.
* Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6515.
    - В File.Save исправлена ошибка, связанная с перегрузкой типом кодировки.
* Устранена проблема, описанная здесь: https://github.com/Azure/azure-powershell/issues/6560.
    - Выполнено обновление до версии NuGet 4.0.3, что позволило исправить исключение шаблона в apiId.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Устранена ошибка при создании виртуальной машины с помощью командлета New-AzureRmVm и параметра DiskFileParameterSet, которая возникала из-за переименования типа учетной записи хранения PremiumLRS.
* Исправлен командлет Invoke-AzureRmVMRunCommand.
* Командлет Get-AzureRmAvailabilitySet теперь может выводить список всех групп доступности в подписке.  (Параметр ResouceGroupName теперь является необязательным.)
* Обновлен параметр SimpleParameterSet командлета New-AzureRmVm, что позволило использовать ускоренную сеть на соответствующих виртуальных машинах.
* Обновлен простой набор параметров New-AzureRmVmss, что позволило отменять создание масштабируемого набора виртуальных машин, если указанная пользователем подсистема балансировки нагрузки уже существует.
* Обновлен пример для New-AzureRmDisk.
* Добавлен пример для New-AzureRmVM.
* Обновлено описание командлета Set-AzureRmVMOSDisk.
* Обновлен пример 1 для Set-AzureRmVMBginfoExtension: исправлены орфографические ошибки и префикс.

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Пакет .NET SDK для ADF обновлен до версии 1.1.0.
* Добавлена поддержка совместного использования локальной среды IR несколькими фабриками данных.
     - Добавлен новый параметр -SharedIntegrationRuntimeResourceId для командлета Set-AzureRmDataFactoryV2IntegrationRuntime.
     - Добавлен новый необязательный параметр -LinkedDataFactoryName для командлета Remove-AzureRmDataFactoryV2IntegrationRuntime.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Пакет SDK для плоскости данных (Microsoft.Azure.DataLake.Store) обновлен до версии 1.1.9.

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Обновлена конвейерная передача для InputObject и ResourceId в командлетах remove.

#### <a name="azurerminsights"></a>AzureRM.Insights;
* Исправлено форматирование OutputType в файлах справки.
* Применен пакет SDK Microsoft.Azure.Management.Monitor 0.19.1-preview.

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Исправлена проблема с конвейерной передачей в командлете Set-AzureRmKeyVaultAccessPolicy.

#### <a name="azurermnetwork"></a>AzureRM.Network
* Добавлены примеры для командлетов LoadBalancerInboundNatPoolConfig.

#### <a name="azurermresources"></a>AzureRM.Resources
* Устранена проблема, возникавшая при указании имени и значения тега для Get-AzureRmResource.
    - https://github.com/Azure/azure-powershell/issues/6765
* Исправлен сценарий конвейерной передачи в Set-AzureRmResource.

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Обновлена конвейерная передача для InputObject и ResourceId в командлетах remove.
* Исправлено несколько ошибок.
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a>AzureRM.Sql
* Добавлена поддержка Advanced Threat Protection для сервера с помощью следующих командлетов:
    - Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy.
* Добавлена поддержка оценки уязвимостей с помощью следующих командлетов:
    - Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings;
    - Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline;
    - Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan.
* Исправлен пример для Remove-AzureRmSqlServerFirewallRule.
* Исправлена неправильная обработка даты и времени для базового языка и региональных параметров, отличных от США, в Get-AzureSqlSyncGroupLog.

#### <a name="azurermstorage"></a>AzureRM.Storage
* В свойства типов выходных данных командлетов добавлен атрибут Ps1XmlAttribute.
* Выходные данные командлетов StorageAccount теперь отображаются в виде таблицы.
    - Get-AzureRmStorageAccount
    - New-AzureRmStorageAccount;
    - Set-AzureRmStorageAccount.

#### <a name="azurermtags"></a>AzureRM.Tags
* Удалено неверное утверждение из справки по командлетам Tag.
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a>6.5.0 — июль 2018 г.
#### <a name="azurermprofile"></a>AzureRM.Profile
* Обновлена справка для командлета Get-AzureRmContextAutosaveSetting.

#### <a name="azurestorage"></a>Azure.Storage;
* Добавлена поддержка отправки BLOB-объекта или файла с помощью токена SAS, доступного только для записи.
* Set-AzureStorageBlobContent
* Set-AzureStorageFileContent

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Для AS добавлено обязательное свойство ResourceGroupName.

#### <a name="azurermautomation"></a>AzureRM.Automation
* Обновлена справка и добавлены примеры для командлета New-AzureRMAutomationSchedule.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Добавлен параметр -Tag для командлета Update/New-AzureRmAvailabilitySet.
* Добавлен пример для командлета Add-AzureRmVmssExtension.
* Добавлены примеры для командлета Remove-AzureRmVmssExtension.
* Обновлена справка для командлета Set-AzureRmVMAccessExtension.
* Изменен класс SimpleParameterSet для командлета New-AzureRmVmss: теперь для SinglePlacementGroup по умолчанию задается значение false, а также добавляется параметр-переключатель SinglePlacementGroup, который позволяет пользователю создать VMSS в одной группе размещения.

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* В класс PSEventHubDRConfigurationAttributes добавлено доступное только для чтения свойство PendingReplicationOperationsCount, которое показывает количество ожидающих репликации операций во время реплицирования.

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Обновлено сообщение об ошибке для командлета Set-AzureRmKeyVaultAccessPolicy.

#### <a name="azurermlogicapp"></a>AzureRM.LogicApp
* Исправлена ошибка "parameter set could not be resolved" (не удалось разрешить заданный параметр) в командлете New-AzureRmLogicApp.

#### <a name="azurermnetwork"></a>AzureRM.Network
* Включен пиринг между виртуальными сетями в нескольких клиентах для командлета Set/Add-AzureRmVirtualNetworkPeering.
* Для шлюза приложений обновлены следующие командлеты:
    - New-AzureRmApplicationGateway: добавлен флаг EnableFIPS и поддержка зон.
    - New-AzureRmApplicationGatewaySku: добавлены новые номера SKU Standard_v2 и WAF_v2.
    - Set-AzureRmApplicationGatewaySku: добавлены новые номера SKU Standard_v2 и WAF_v2.
* Командлеты RouteTable пересозданы в последней версии генератора.

#### <a name="azurermrelay"></a>AzureRM.Relay
* Обновлены файлы Markdown, исправлена проблема с именем параметра в примере.

#### <a name="azurermresources"></a>AzureRM.Resources
* Обновлены командлеты Roleassignment и roledefinition:
    - Удалены лишние вызовы roledefinition, выполняемые в ходе разбиения на страницы.
* Исправлен командлет Get-AzureRmRoleAssignment.
    - Исправлена работа параметра -ExpandPrincipalGroups.
* Устранена проблема в командлете Get-AzureRmResource, заключающая в том, что в параметре -ResourceType учитывался регистр символов.

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Добавлены параметры top и skip для командлетов list.
* Добавлены командлеты для перехода с пространства имен ценовой категории "Стандартный" на пространство ценовой категории "Премиум":
    - Start-AzureRmServiceBusMigration;
    - Get-AzureRmServiceBusMigration;
    - Complete-AzureRmServiceBusMigration;
    - Stop-AzureRmServiceBusMigration;
    - Remove-AzureRmServiceBusMigration.
* В класс PSServiceBusDRConfigurationAttributes добавлено доступное только для чтения свойство PendingReplicationOperationsCount, которое показывает количество ожидающих репликации операций во время реплицирования.

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Обновлен пример для командлета New-AzureRmServiceFabricCluster.

#### <a name="azurermsql"></a>AzureRM.Sql
* Добавлены новые командлеты для Management.Sql, позволяющие клиентам добавлять сертификат TDE в экземпляр SQL Server или управляемый экземпляр:
    - Add-AzureRmSqlServerTransparentDataEncryptionCertificate;
    - Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate.

#### <a name="azurermwebsites"></a>AzureRM.Websites
* `Set-AzureRmWebApp -AssignIdentity` и `Set-AzureRmWebAppSlot -AssignIdentity` при установленном значении false теперь будут удалять свойство Identity из объекта сайта. Также при этом будет удаляться тег предварительной версии.
* Обновлен пример для `Get-AzureRmWebAppMetrics` и `Get-AzureRmAppServicePlanMetrics`.
* `Set-AzureRmWebApp -PhpVersion` теперь поддерживает off как допустимую версию PHP.

## <a name="640---july-2018"></a>6.4.0 — июль 2018 г.
#### <a name="general"></a>Общие сведения
* Исправлено форматирование OutputType в файлах справки для большинства модулей.

#### <a name="azurermprofile"></a>AzureRM.Profile
* В основные типы выходных данных добавлен атрибут Ps1Xml.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Функция добавления тега IP-адреса для масштабируемого набора виртуальных машин (VMSS)
    - Добавлен командлет New-AzureRmVmssIpTagConfig.
    - В New-AzureRmVmssIpConfig добавлен параметр IpTag.
* Функция автоматического отката ОС для VMSS
    - В New-AzureRmVmssConfig и Update-AzureRmVmss добавлены параметры DisableAutoRollback.
* Функция ведения журнала обновлений ОС для VMSS
    - В Get-AzureRmVmss добавлен параметр OSUpgradeHistory.

#### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* Добавлена поддержка списков управления доступом к каталогу с использованием следующих команд:
    - Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry;
    - Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry;
    - Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Добавлены поддержка отмены выполнения и отслеживание хода выполнения для Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl и Remove-AzureRmDataLakeStoreItemAclEntry.
* Добавлена поддержка отмены выполнения для Export-AzureRmDataLakeStoreChildItemProperties.
* Исправлена очистка сообщений об отладке для командлетов, которые выполняют рекурсивные операции.
* Исправлено расположение тестовых данных для командлетов DataLake.

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Для командлетов вывода списка операций Get-AzureRmEventHub и Get-AzureRmEventHubConsumerGroup добавлен необязательный параметр MaxCount.
* Исправлена проблема с командлетом New-AzureRmEventHub, из-за которой требовалось указать по крайней мере один параметр при создании концентратора событий. Добавлен набор параметров по умолчанию.
* Для командлета New-AzureRmEventHubKey добавлен необязательный параметр -KeyValue, который позволяет пользователю предоставить значение ключа.

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Исправлена ошибка, из-за которой при выполнении командлета Get-AzureRmKeyVault с параметром -Tag возвращались все ресурсы.

#### <a name="azurermnetwork"></a>AzureRM.Network
* Для параметра шлюзов виртуальной вести, избыточных между зонами, предоставлены новые номера SKU.
* Добавлены новые команды для функции API партнеров ExpressRoute (ARM):
    - добавлена команда Get-AzureRmExpressRouteCrossConnection;
    - добавлена команда Set-AzureRmExpressRouteCrossConnection;
    - добавлена команда Add-AzureRmExpressRouteCrossConnectionPeering;
    - добавлена команда Get-AzureRmExpressRouteCrossConnectionPeering;
    - добавлена команда Remove-AzureRmExpressRouteCrossConnectionPeering;
    - добавлена команда Get-AzureRMExpressRouteCrossConnectionArpTable;
    - добавлена команда Get-AzureRMExpressRouteCrossConnectionRouteTable;
    - добавлена команда Get-AzureRMExpressRouteCrossConnectionRouteTableSummary.

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* Добавлен командлет Get-AzureRmRecoveryServicesBackupStatus. Этот командлет принимает идентификатор виртуальной машины и проверяет, защищена ли виртуальная машина с помощью какого-либо хранилища в подписке. Если такое хранилище существует, командлет выводит данные о нем.

#### <a name="azurermresources"></a>AzureRM.Resources
* Обновлены командлеты Get-AzureRmPolicyAssignment:
    - Добавлена поддержка вывода списка значений параметра -Scope на уровне группы управления.
    - Добавлена поддержка для получения отдельных назначений со значениями -Scope на уровне группы управления.
    - Для параметра управления добавлены параметры -Effective и -All.
* Обновлены командлеты Get/New/Remove/Set-AzureRmPolicyDefinition.
    - Добавлен параметр -ManagementGroupName для применения операций к заданной группе управления.
    - Добавлен параметр -SubscriptionId для применения операций к заданной подписке.
* Обновлены командлеты Get/New/Remove/Set-AzureRmPolicySetDefinition.
    - Добавлен параметр -ManagementGroupName для применения операций к заданной группе управления.
    - Добавлен параметр -SubscriptionId для применения операций к заданной подписке.
* Добавлена поддержка ссылок на секрет KeyVault в параметрах при использовании TemplateParameterObject в New-AzureRmResourceGroupDeployment.
* Устранена проблема, из-за которой параметр -EndDate игнорировался в New-AzureRmADAppCredential.
    - https://github.com/Azure/azure-powershell/issues/6505
* Устранена проблема, из-за которой в Add-AzureRmADGroupMember использовался неверный URL-адрес для запроса.
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Для командлета New-AzureRmServiceBusKey добавлен необязательный параметр -KeyValue, который позволяет пользователю предоставить значение ключа.

#### <a name="azurermsql"></a>AzureRM.Sql
* В справке по New-AzureRmSqlDatabaseRestorePoint добавлено описание определяемых пользователем точек восстановления для хранилища данных SQL.
* Обновлена документация по параметру -ComputeGeneration, используемого в нескольких командлетах.

## <a name="630---june-2018"></a>6.3.0 — июнь 2018 г.
#### <a name="azurermprofile"></a>AzureRM.Profile
* Обновлены сообщения об ошибках для Enable-AzureRmContextAutoSave.
* Создание контекста для каждой подписки при выполнении Connect-AzureRmAccount без предыдущего контекста.

#### <a name="azurestorage"></a>Azure.Storage;
* В файлы справки добавлены дополнительные сведения о параметре -Permissions.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Get-AzureRmVmDiskEncryptionStatus устраняет проблему, которая наблюдалась на виртуальных машинах без дисков данных.
* Обновлена версия клиентской библиотеки Compute для исправления следующих командлетов:
    - Grant-AzureRmDiskAccess
    - Grant-AzureRmSnapshotAccess
    - Save-AzureRmVMImage
* В следующих командлетах исправлено отображение неправильных значений operation ID и operation status:
    - Start-AzureRmVM
    - Stop-AzureRmVM
    - Restart-AzureRmVM
    - Set-AzureRmVM
    - Remove-AzuerRmVM
    - Set-AzureRmVmss
    - Start-AzureRmVmssRollingOSUpgrade
    - Stop-AzureRmVmssRollingUpgrade
    - Start-AzureRmVmss
    - Restart-AzureRmVmss
    - Stop-AzureRmVmss
    - Remove-AzureRmVmss
    - ConvertTo-AzureRmVMManagedDisk
    - Revoke-AzureRmSnapshotAccess
    - Remove-AzureRmSnapshot
    - Revoke-AzureRmDiskAccess
    - Remove-AzureRmDisk
    - Remove-AzureRmContainerService
    - Remove-AzureRmAvailabilitySet

#### <a name="azurermeventgrid"></a>AzureRM.EventGrid
* Удалены условия проверки ValidateNotNullOrEmpty для SubjectBeginsWith/SubjectEndsWith в командлете Update-AzureRmEventGridSubscription, что позволяет при необходимости заменять эти параметры пустой строкой.

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Исправлена ошибка, когда при выполнении командлета Get-AzureRmKeyVault -Tag не возвращается ни один тег.

#### <a name="azurermpolicyinsights"></a>AzureRM.PolicyInsights
* Общедоступный выпуск командлетов Policy Insights.
    - Используется API версии 2018-04-04.
    - К результатам Get-AzureRmPolicyStateSummary добавлено PolicyDefinitionReferenceId.

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* Для командлетов RecoveryServices.Backup добавлен параметр -Vault. Передача этого параметра переопределяет командлет Set-AzureRmRecoveryServicesContext.

#### <a name="azurermsql"></a>AzureRM.Sql
* В файле справки обновлен пример для командлета Get-AzureRmSqlDatabaseExpanded.

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Обновлен файл справки для командлета Add-AzureRmTrafficManagerEndpointConfig.

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Изменено действие командлета Set-AzureRmWebApp. Теперь он не перезаписывает AppSettings, если используется параметр -AssignIdentity.
* Командлет New-AzureRmWebAppSlot теперь учитывает дополнительный параметр AppServicePlan.

## <a name="621---june-2018"></a>6.2.1 — июнь 2018 г.
### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights;
* В обновленной модели PSWorkspace Network может использовать type в качестве параметра.

## <a name="620---june-2018"></a>6.2.0 — июнь 2018 г.
#### <a name="azurermprofile"></a>AzureRM.Profile
* Исправлена ошибка с загрузкой Newtonsoft.Json версии 10.0.3 во время импорта модуля.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Функция обновления виртуальных машин VMSS.
    - Добавлены командлеты Update-AzureRmVmssVM и New-AzureRmVMDataDisk.
    - В командлет Add-AzureRmVMDataDisk добавлен параметр VirtualMachineScaleSetVM, который позволяет добавлять диски данных в виртуальные машины VMSS.

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Пакет SDK для ADF .NET обновлен до версии 0.8.0-preview. Новая версия содержит такие изменения:
    - добавлена операция для настройки репозитория фабрики;
    - связанная служба QuickBooks LinkedService теперь предоставляет свойства consumerKey и consumerSecret;
    - тип нескольких моделей изменен с SecretBase на Object;
    - добавлен триггер событий BLOB-объектов.

### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* В документацию добавлены примеры выходных данных.

### <a name="azurermnetwork"></a>AzureRM.Network
* В командлеты Наблюдателя за сетями добавлены параметры Аналитики трафика.

#### <a name="azurermresources"></a>AzureRM.Resources
* Исправлена ошибка, когда командлет Get-AzureRmResource возвращает свойство Properties объектов PSResource.

#### <a name="azurermscheduler"></a>AzureRM.Scheduler
* Исправлена ошибка, когда обновление ServiceBusQueueJob не задает новые значения для проверки подлинности.

### <a name="azurermsql"></a>AzureRM.Sql
* В перечисленные ниже командлеты добавлен необязательный параметр LicenseType.
    - New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase;
    - New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool;
    - New-AzureRmSqlDatabaseCopy
    - New-AzureRmSqlDatabaseSecondary
    - Restore-AzureRmSqlDatabase

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Командлет New-AzureRMWebApp теперь использует общие алгоритмы из библиотеки Strategy.

## <a name="610---may-2018"></a>6.1.0 — май 2018 г.
#### <a name="azurermprofile"></a>AzureRM.Profile
* Устранена проблема с выполнением Clear-AzureRmContext, при которой сохранялся пустой контекст с именем предыдущего контекста по умолчанию, что не позволяло пользователю создать новый контекст со старым именем.

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Включены операции связывания и отмены связи в автономной системе.

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Добавлена поддержка ApiVersions, ApiReleases и ApiRevisions.
* Добавлена поддержка серверной части ServiceFabric.
* Добавлена поддержка средства ведения журнала Application Insights.
* Добавлена поддержка для распознавания номера SKU уровня "Базовый" как допустимого номера SKU службы управления API.
* Добавлена поддержка установки сертификатов, выданных частным центром сертификации в качестве корневого или обычного ЦС.
* Добавлена поддержка для приема пользовательских SSL-сертификатов с помощью KeyVault и нескольких имен узлов прокси-сервера.
* Добавлена поддержка для удостоверения MSI.
* Добавлена поддержка для принятия политик с помощью URL-адреса. Примечание. Указанные ниже командлеты в следующем выпуске будут отмечены как нерекомендуемые:
   - Import-AzureRmApiManagementHostnameCertificate
   - New-AzureRmApiManagementHostnameConfiguration
   - Set-AzureRmApiManagementHostnames
   - Update-AzureRmApiManagementDeployment

#### <a name="azurermbatch"></a>AzureRM.Batch
* Выпущен новый командлет Get-AzureBatchPoolNodeCounts.
* Выпущен новый командлет Start-AzureBatchComputeNodeServiceLogUpload.

#### <a name="azurermconsumption"></a>AzureRM.Consumption:
* Добавлены новые параметры Expand, ResourceGroup, InstanceName, InstanceId, Tags и командлет высшего уровня Get-AzureRmConsumptionUsageDetail.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Исправлен пример для Export-AzureRmDataLakeStoreChildItemProperties.
* Исправлено исключение параметра NULL при использовании рекурсии в Set-AzureRmDataLakeStoreItemAclEntry.
* Исправлены файлы справки для Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl и Remove-AzureRmDataLakeStoreItemAclEntry.

#### <a name="azurermnetwork"></a>AzureRM.Network
* Пакет SDK для сети обновлен с предварительной версии 18.0.0 до предварительной версии 19.0.0.
* Добавлен командлет для создания конфигурации протокола.
    - New-AzureRmNetworkWatcherProtocolConfiguration.
* Добавлен командлет для добавления нового подключения канала к существующему каналу ExpressRoute.
    - Add-AzureRmExpressRouteCircuitConnectionConfig.
* Добавлен командлет для удаления подключения канала к существующему каналу ExpressRoute.
    - Remove-AzureRmExpressRouteCircuitConnectionConfig.
* Добавлен командлет для получения подключения канала.
    - Get-AzureRmExpressRouteCircuitConnectionConfig.

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Исправлена процедура аутентификации сервера с использованием созданных сертификатов (проблема № 5998).

#### <a name="azurermsql"></a>AzureRM.Sql
* Обновлены командлеты аудита, которые теперь позволяют удалять AuditActions или AuditActionGroups.
* Исправлена проблема с Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy, при которой установка новой гибкой политики хранения завершалась ошибкой с сообщением "Configure long term retention policy with azure recovery service vault and policy is no longer supported. Please submit request with the new flexible retention policy" (Настройка политики долгосрочного хранения с помощью хранилища и политики служб восстановления Azure больше не поддерживается. Отправьте запрос с использованием новой гибкой политики хранения).
* Обновлены все командлеты, связанные со службой "База данных SQL Azure", с созданием эластичных пулов и обновлением. Теперь используются новые API баз данных с поддержкой свойства номеров SKU для обеспечения масштабируемости и связанных с уровнями возможностей.
* Обновлены командлеты, в том числе:
    - New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase;
    - New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool;
    - New-AzureRmSqlDatabaseCopy
    - New-AzureRmSqlDatabaseSecondary
    - Restore-AzureRmSqlDatabase

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Обновлены параметры для Get-AzureRmTrafficManagerProfile. Теперь при использовании параметра -Name требуется параметр -ResourceGroupName.
