---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: d94e7001df730b22fb900b284c6fac47b5d81b8b
ms.sourcegitcommit: 0b94b9566124331d0b15eb7f5a811305c254172e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/15/2019
ms.locfileid: "93720074"
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

### [Get-AzServiceFabricApplication](Get-AzServiceFabricApplication.md)
Получение сведений о приложении "структура служб".

### [Get-AzServiceFabricApplicationType](Get-AzServiceFabricApplicationType.md)
Получение подробных сведений о типе приложения в структуре служб.

### [Get-AzServiceFabricApplicationTypeVersion](Get-AzServiceFabricApplicationTypeVersion.md)
Получение сведений о версии для типа приложения "структура обслуживания".

### [Get-AzServiceFabricCluster](Get-AzServiceFabricCluster.md)
Получение сведений о ресурсе кластера.

### [Get-AzServiceFabricService](Get-AzServiceFabricService.md)
Получение сведений о службе фабрики служб в указанном приложении и кластере.

### [New-AzServiceFabricApplication](New-AzServiceFabricApplication.md)
Создание нового приложения фабрики служб в указанной группе ресурсов и кластере.

### [New-AzServiceFabricApplicationType](New-AzServiceFabricApplicationType.md)
Создание нового типа приложения "структура службы" в заданной группе ресурсов и кластере.

### [New-AzServiceFabricApplicationTypeVersion](New-AzServiceFabricApplicationTypeVersion.md)
Создать новую версию типа приложения в указанной группе ресурсов и кластере.

### [New-AzServiceFabricCluster](New-AzServiceFabricCluster.md)
Эта команда использует сертификаты, предоставленные системой или автоматически подписанные сертификаты, для настройки нового кластера фабрики служб. Он может использовать шаблон по умолчанию или настраиваемый шаблон, который вы предоставляете. Вы можете указать папку для экспорта самозаверяющих сертификатов в хранилище ключей или их последующего получения из него. 

### [New-AzServiceFabricService](New-AzServiceFabricService.md)
Создание новой службы Service Fabric в указанном приложении и кластере.

### [Remove-AzServiceFabricApplication](Remove-AzServiceFabricApplication.md)
Удаление приложения из кластера. Это приведет к удалению всех служб в приложении.

### [Remove-AzServiceFabricApplicationType](Remove-AzServiceFabricApplicationType.md)
Удаление сервисной фабрики тип приложения из кластера. Это приведет к удалению всех версий типов под этим ресурсом.

### [Remove-AzServiceFabricApplicationTypeVersion](Remove-AzServiceFabricApplicationTypeVersion.md)
Удаление служебной фабрики версия типа приложения из кластера.

### [Remove-AzServiceFabricClientCertificate](Remove-AzServiceFabricClientCertificate.md)
Для проверки подлинности клиента в кластере удалите клиентские сертификаты или имена субъектов сертификата (-ов).

### [Remove-AzServiceFabricClusterCertificate](Remove-AzServiceFabricClusterCertificate.md)
Удаление сертификата кластера из использования для системы безопасности кластера.

### [Remove-AzServiceFabricNode](Remove-AzServiceFabricNode.md)
Удаление узлов из кластера с определенным типом узла.

### [Remove-AzServiceFabricNodeType](Remove-AzServiceFabricNodeType.md)
Удаление типа полного узла из кластера.

### [Remove-AzServiceFabricService](Remove-AzServiceFabricService.md)
Удаление службы из кластера.

### [Remove-AzServiceFabricSetting](Remove-AzServiceFabricSetting.md)
Удалите из кластера один или несколько параметров структуры служб.

### [Set-AzServiceFabricSetting](Set-AzServiceFabricSetting.md)
Добавьте или обновите один или несколько параметров структуры служб в кластере.

### [Set-AzServiceFabricUpgradeType](Set-AzServiceFabricUpgradeType.md)
Изменение типа обновления структуры обслуживания кластера.

### [Update-AzServiceFabricApplication](Update-AzServiceFabricApplication.md)
Обновите приложение фабрики служб. Это позволит обновить параметры приложения и (или) обновить версию типа приложения, которая вызывает обновление приложения.

### [Update-AzServiceFabricDurability](Update-AzServiceFabricDurability.md)
Обновите уровень устойчивости или VmSku типа узла в кластере.

### [Update-AzServiceFabricReliability](Update-AzServiceFabricReliability.md)
Обновите уровень надежности основного типа узла в кластере.

