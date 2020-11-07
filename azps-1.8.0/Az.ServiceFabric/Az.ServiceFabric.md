---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: 01bf8c630f4fc4d137e98be5b1996eaf47ea3363
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "93719883"
---
# AZ. ServiceFabric Module
## Nописание
Модуль служб Azure Service Fabric, который можно использовать для автоматизации операций End-2, таких как создание защищенного кластера, развертывание сертификатов кластера, Добавление и удаление узлов из кластера и т. д. Полный список всех операций приведен ниже.

## Командлеты AZ. ServiceFabric
### [Add-AzServiceFabricApplicationCertificate](Add-AzServiceFabricApplicationCertificate.md)
Добавьте новый сертификат в набор масштабов виртуальной машины (-ов), образующих кластер. Этот сертификат предназначен для использования в качестве сертификата приложения.

### [Add-AzServiceFabricClientCertificate](Add-AzServiceFabricClientCertificate.md)
Добавьте в кластер общее имя или отпечаток для целей проверки подлинности клиента.

### [Add-AzServiceFabricClusterCertificate](Add-AzServiceFabricClusterCertificate.md)
Добавьте в кластер дополнительный сертификат кластера.

### [Add-AzServiceFabricNode](Add-AzServiceFabricNode.md)
Добавьте узлы в конкретный тип узла в кластере.

### [Add-AzServiceFabricNodeType](Add-AzServiceFabricNodeType.md)
Добавление нового типа узла в существующий кластер.

### [Get-AzServiceFabricCluster](Get-AzServiceFabricCluster.md)
Получение сведений о ресурсе кластера.

### [New-AzServiceFabricCluster](New-AzServiceFabricCluster.md)
Эта команда использует сертификаты, предоставленные системой или автоматически подписанные сертификаты, для настройки нового кластера фабрики служб. Он может использовать шаблон по умолчанию или настраиваемый шаблон, который вы предоставляете. Вы можете указать папку для экспорта самозаверяющих сертификатов в хранилище ключей или их последующего получения из него. 

### [Remove-AzServiceFabricClientCertificate](Remove-AzServiceFabricClientCertificate.md)
Для проверки подлинности клиента в кластере удалите клиентские сертификаты или имена субъектов сертификата (-ов).

### [Remove-AzServiceFabricClusterCertificate](Remove-AzServiceFabricClusterCertificate.md)
Удаление сертификата кластера из использования для системы безопасности кластера.

### [Remove-AzServiceFabricNode](Remove-AzServiceFabricNode.md)
Удаление узлов из кластера с определенным типом узла.

### [Remove-AzServiceFabricNodeType](Remove-AzServiceFabricNodeType.md)
Удаление типа полного узла из кластера.

### [Remove-AzServiceFabricSetting](Remove-AzServiceFabricSetting.md)
Удалите из кластера один или несколько параметров структуры служб.

### [Set-AzServiceFabricSetting](Set-AzServiceFabricSetting.md)
Добавьте или обновите один или несколько параметров структуры служб в кластере.

### [Set-AzServiceFabricUpgradeType](Set-AzServiceFabricUpgradeType.md)
Изменение типа обновления структуры обслуживания кластера.

### [Update-AzServiceFabricDurability](Update-AzServiceFabricDurability.md)
Обновите уровень устойчивости или VmSku типа узла в кластере.

### [Update-AzServiceFabricReliability](Update-AzServiceFabricReliability.md)
Обновите уровень надежности основного типа узла в кластере.

