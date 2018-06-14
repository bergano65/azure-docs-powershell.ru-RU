---
title: Журнал изменений Azure PowerShell | Документация Майкрософт
description: Это руководство содержит историю изменений Azure PowerShell, внесенных в новом выпуске.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: b777a5fe036cda58a930ac0f5aaef3b9a7c2b420
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2018
ms.locfileid: "34853446"
---
# <a name="release-notes"></a>Заметки о выпуске

Здесь приведен список изменений, внесенных в Azure PowerShell в этом выпуске.

## <a name="version-380"></a>Версия 3.8.0
* Службы вычислений
  - Исправлена ошибка в командлетах Get-*, чтобы можно было получить несколько страниц данных (более 120 элементов).
* Data Lake Analytics
  - Исправлена ошибка в справке некоторых команд для отображения корректной формулировки и примеров.
* Data Lake Store
  - Добавлена поддержка начальной и конечной части командлета `Get-AzureRMDataLakeStoreItemContent`. Это гарантирует отображение строк с разделителями в новой строке при возврате значения "Первые N" или "Последние N".
* HDInsight
  - Добавлена поддержка для типа кластера RServer.
    + Вы можете указать размер виртуальной машины граничного узла для кластера RServer в командлете New-AzureRmHDInsightCluster или New-AzureRmHDInsightClusterConfig.
    + RServer сейчас является параметром конфигурации в Add-AzureRmHDInsightConfigValues. Он позволяет настроить параметр RStudio, который указывает, что требуется выполнить установку R Studio.
* Приложение логики
  - Исправлены командлеты Set-AzureRmIntegrationAccountSchema и Set-AzureRmIntegrationAccountMap для устранения ошибки свойства ContentLink (настройка свойств Content и ContentLink приводила к сбою при обновлении).
* Сеть
  - Добавлена поддержка новых функций брандмауэра веб-приложения в шлюзах приложений.
    + Добавлен командлет New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig.
    + Добавлен командлет Get-AzureRmApplicationGatewayAvailableWafRuleSets (псевдоним: List-AzureRmApplicationGatewayAvailableWafRuleSets).
    + Обновлен командлет New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration: добавлены параметры -RuleSetType, -RuleSetVersion и -DisabledRuleGroups.
    + Обновлен командлет Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration: добавлены параметры -RuleSetType, -RuleSetVersion и -DisabledRuleGroups.
  - Добавлена поддержка политик IPSec для подключений шлюза виртуальной сети.
  - Добавлен командлет New-AzureRmIpsecPolicy.
  - Обновлен командлет New-AzureRmVirtualNetworkGatewayConnection: добавлены параметры -IpsecPolicies и -UsePolicyBasedTrafficSelectors.
* Профиль
  - *Устарело*. Командлет Save-AzureRmProfile переименован в Save-AzureRmContext. Используется псевдоним для устаревшего имени командлета, который будет удален в следующем выпуске.
  - *Устарело*. Командлет Select-AzureRmProfile переименован на Import-AzureRmContext. Используется псевдоним для устаревшего имени командлета, который будет удален в следующем выпуске.
  - Типы выходных данных командлетов профиля PSAzureContext и PSAzureProfile изменятся в следующем выпуске.
  - Командлет Save-AzureRmContext не будет включать параметр OutputType в следующем выпуске.
  - Исправлена ошибка в общем коде командлета для использования FIPS-совместимого алгоритма для хэша данных: https://github.com/Azure/azure-powershell/issues/3651.
* SQL
  - Исправлены ошибки в командлетах групп отработки отказа Azure.
  - Исправлена ошибка опроса операции.
  - Исправлено значение GracePeriodWithDataLossHour при настройке ручного режима FailoverPolicy.
* TrafficManager
  - Добавлена поддержка метода географической маршрутизации трафика.
    + Для параметра TrafficRoutingMethod командлета New-AzureRmTrafficManagerProfile доступно новое значение — Geographic.
    + Для командлетов New-AzureRmTrafficManagerEndpoint и Add-AzureRmTrafficManagerEndpointConfig доступен новый параметр — GeoMapping.
    + Исправлена ошибка передачи для командлета Get-AzureRmTrafficManagerProfile, который возвращал коллекцию профилей.
* Управление службами
  - Для командлета Restart-AzureVM добавлен параметр InitiateMaintenance для выполнения обслуживания во время перезапуска виртуальной машины.
  - Для командлета Get-AzureVM добавлено поле состояния обслуживания.
  - Добавлены новые командлеты для поддержки обновления хранилища служб восстановления:
    + Test-AzureRecoveryServicesVaultUpgrade;
    + Invoke-AzureRecoveryServicesVaultUpgrade.
