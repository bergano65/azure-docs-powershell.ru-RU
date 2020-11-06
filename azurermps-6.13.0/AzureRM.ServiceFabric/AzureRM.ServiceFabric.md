---
Module Name: AzureRM.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
ms.openlocfilehash: 6d93775a028e7a590a8da9cc008640fb8484bdf2
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "93554579"
---
# Модуль AzureRM. ServiceFabric
## Nописание
Модуль служб Azure Service Fabric, который можно использовать для автоматизации операций End-2, таких как создание защищенного кластера, развертывание сертификатов кластера, Добавление и удаление узлов из кластера и т. д. Полный список всех операций приведен ниже.

## Командлеты AzureRM. ServiceFabric
### [Add-AzureRmServiceFabricApplicationCertificate](Add-AzureRmServiceFabricApplicationCertificate.md)
Добавьте новый сертификат в набор масштабов виртуальной машины (-ов), образующих кластер. Этот сертификат предназначен для использования в качестве сертификата приложения.

### [Add-AzureRmServiceFabricClientCertificate](Add-AzureRmServiceFabricClientCertificate.md)
Добавьте в кластер общее имя или отпечаток для целей проверки подлинности клиента.

### [Add-AzureRmServiceFabricClusterCertificate](Add-AzureRmServiceFabricClusterCertificate.md)
Добавьте в кластер дополнительный сертификат кластера.

### [Add-AzureRmServiceFabricNode](Add-AzureRmServiceFabricNode.md)
Добавьте узлы в конкретный тип узла в кластере.

### [Add-AzureRmServiceFabricNodeType](Add-AzureRmServiceFabricNodeType.md)
Добавление нового типа узла в существующий кластер.

### [Get-AzureRmServiceFabricCluster](Get-AzureRmServiceFabricCluster.md)
Получение сведений о ресурсе кластера.

### [New-AzureRmServiceFabricCluster](New-AzureRmServiceFabricCluster.md)
Эта команда использует сертификаты, предоставленные системой или автоматически подписанные сертификаты, для настройки нового кластера фабрики служб. Он может использовать шаблон по умолчанию или настраиваемый шаблон, который вы предоставляете. Вы можете указать папку для экспорта самозаверяющих сертификатов в хранилище ключей или их последующего получения из него. 

### [Remove-AzureRmServiceFabricClientCertificate](Remove-AzureRmServiceFabricClientCertificate.md)
Для проверки подлинности клиента в кластере удалите клиентские сертификаты или имена субъектов сертификата (-ов).

### [Remove-AzureRmServiceFabricClusterCertificate](Remove-AzureRmServiceFabricClusterCertificate.md)
Удаление сертификата кластера из использования для системы безопасности кластера.

### [Remove-AzureRmServiceFabricNode](Remove-AzureRmServiceFabricNode.md)
Удаление узлов из кластера с определенным типом узла.

### [Remove-AzureRmServiceFabricNodeType](Remove-AzureRmServiceFabricNodeType.md)
Удаление типа полного узла из кластера.

### [Remove-AzureRmServiceFabricSetting](Remove-AzureRmServiceFabricSetting.md)
Удалите из кластера один или несколько параметров структуры служб.

### [Set-AzureRmServiceFabricSetting](Set-AzureRmServiceFabricSetting.md)
Добавьте или обновите один или несколько параметров структуры служб в кластере.

### [Set-AzureRmServiceFabricUpgradeType](Set-AzureRmServiceFabricUpgradeType.md)
Изменение типа обновления структуры обслуживания кластера.

### [Update-AzureRmServiceFabricDurability](Update-AzureRmServiceFabricDurability.md)
Обновите уровень устойчивости или VmSku типа узла в кластере.

### [Update-AzureRmServiceFabricReliability](Update-AzureRmServiceFabricReliability.md)
Обновите уровень надежности основного типа узла в кластере.

