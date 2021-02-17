---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: 6c58f25209a0acd227e2f04e7ca808916f283d46
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242141"
---
# Az.ServiceFabric Module
## Описание
Модуль "Ткань службы" Azure, который можно использовать для автоматизации двух конечных операций, таких как создание защищенного кластера, развертывание сертификатов кластера, добавление или удаление узлов из кластера и т. д. Полный список всех операций приведен ниже.

## Az.ServiceFabric Cmdlets
### [Add-AzServiceFabricClientCertificate](Add-AzServiceFabricClientCertificate.md)
Добавьте общие имена или эскизы в кластер в целях проверки подлинности клиента.

### [Add-AzServiceFabricClusterCertificate](Add-AzServiceFabricClusterCertificate.md)
Добавление сертификата дополнительного кластера в кластер.

### [Add-AzServiceFabricManagedClusterClientCertificate](Add-AzServiceFabricManagedClusterClientCertificate.md)
Добавьте общее имя сертификата или эскиз на кластер. При этом сертификат будет снова зарегистрирован для проверки подлинности клиента.

### [Add-AzServiceFabricManagedNodeTypeVMExtension](Add-AzServiceFabricManagedNodeTypeVMExtension.md)
Добавьте расширение VM к типу узла.

### [Add-AzServiceFabricManagedNodeTypeVMSecret](Add-AzServiceFabricManagedNodeTypeVMSecret.md)
Добавьте секрет сертификата к типу узла.

### [Add-AzServiceFabricNode](Add-AzServiceFabricNode.md)
Добавьте узлы для определенного типа узла в кластере.

### [Add-AzServiceFabricNodeType](Add-AzServiceFabricNodeType.md)
Добавьте новый тип узла в существующий кластер.

### [Get-AzServiceFabricApplication](Get-AzServiceFabricApplication.md)
Получить сведения о приложении "Служиная ткань".

### [Get-AzServiceFabricApplicationType](Get-AzServiceFabricApplicationType.md)
Получить сведения о типе приложения "Служивная ткань".

### [Get-AzServiceFabricApplicationTypeVersion](Get-AzServiceFabricApplicationTypeVersion.md)
Сведения о типе версии приложения "Служивная ткань".

### [Get-AzServiceFabricCluster](Get-AzServiceFabricCluster.md)
Получите сведения о ресурсах кластера.

### [Get-AzServiceFabricManagedCluster](Get-AzServiceFabricManagedCluster.md)
Получите сведения о ресурсах с управляемым кластером.

### [Get-AzServiceFabricManagedNodeType](Get-AzServiceFabricManagedNodeType.md)
Получите сведения о ресурсах типа "Управляемый узел".

### [Get-AzServiceFabricService](Get-AzServiceFabricService.md)
Получить сведения о службе "Ткань услуги" в указанном приложении и кластере.

### [New-AzServiceFabricApplication](New-AzServiceFabricApplication.md)
Создайте новое приложение для создания структуры обслуживания в указанной группе ресурсов и кластере.

### [New-AzServiceFabricApplicationType](New-AzServiceFabricApplicationType.md)
Создайте новый тип приложения-службы в указанной группе ресурсов и кластере.

### [New-AzServiceFabricApplicationTypeVersion](New-AzServiceFabricApplicationTypeVersion.md)
Создайте новую версию типа приложения в указанной группе ресурсов и кластере.

### [New-AzServiceFabricCluster](New-AzServiceFabricCluster.md)
В этой команде используются сертификаты, которые вы предоставляете, или системные самозаверяемые сертификаты для настроить новый кластер тканью службы. Он может использовать шаблон по умолчанию или настраиваемый шаблон, который вы предоставляете. Вы можете указать папку для экспорта самозаверяющих сертификатов или их позднего получения из хранилища ключей.

### [New-AzServiceFabricManagedCluster](New-AzServiceFabricManagedCluster.md)
Создание нового управляемого кластера.

### [New-AzServiceFabricManagedNodeType](New-AzServiceFabricManagedNodeType.md)
Создать ресурс нового типа узла.

### [New-AzServiceFabricService](New-AzServiceFabricService.md)
Создайте новую службу выкладок обслуживания в указанном приложении и кластере.

### [Remove-AzServiceFabricApplication](Remove-AzServiceFabricApplication.md)
Удалите приложение из кластера. При этом будут удалиться все службы, внося в приложение.

### [Remove-AzServiceFabricApplicationType](Remove-AzServiceFabricApplicationType.md)
Удалите из кластера структуру приложения для типа приложения. При этом будут удаляться все версии этого ресурса.

### [Remove-AzServiceFabricApplicationTypeVersion](Remove-AzServiceFabricApplicationTypeVersion.md)
Удалите из кластера структуру приложения версии приложения.

### [Remove-AzServiceFabricClientCertificate](Remove-AzServiceFabricClientCertificate.md)
Удалите имена или имена сертификатов клиентов, используемых для проверки подлинности клиента на кластере.

### [Remove-AzServiceFabricClusterCertificate](Remove-AzServiceFabricClusterCertificate.md)
Удалите сертификат кластера из использования для защиты кластера.

### [Remove-AzServiceFabricManagedCluster](Remove-AzServiceFabricManagedCluster.md)
Удалить ресурс кластера.

### [Remove-AzServiceFabricManagedClusterClientCertificate](Remove-AzServiceFabricManagedClusterClientCertificate.md)
Remvoe client certificate by thumbprint or common name.

### [Remove-AzServiceFabricManagedNodeType](Remove-AzServiceFabricManagedNodeType.md)
Удалите тип узла или конкретные узлы для этого типа.

### [Remove-AzServiceFabricManagedNodeTypeVMExtension](Remove-AzServiceFabricManagedNodeTypeVMExtension.md)
Удалите расширение VM из типа узла.

### [Remove-AzServiceFabricNode](Remove-AzServiceFabricNode.md)
Удалите узлы с определенного типа узла из кластера.

### [Remove-AzServiceFabricNodeType](Remove-AzServiceFabricNodeType.md)
Удалите из кластера полный тип узла.

### [Remove-AzServiceFabricService](Remove-AzServiceFabricService.md)
Удалите службу из кластера.

### [Remove-AzServiceFabricSetting](Remove-AzServiceFabricSetting.md)
Удалите один или несколько параметров "Служиная ткань" из кластера.

### [Restart-AzServiceFabricManagedNodeType](Restart-AzServiceFabricManagedNodeType.md)
Перезапустите определенные узлы из типа узла.

### [Set-AzServiceFabricManagedCluster](Set-AzServiceFabricManagedCluster.md)
Настройка свойств ресурсов кластера.

### [Set-AzServiceFabricManagedNodeType](Set-AzServiceFabricManagedNodeType.md)
Задает свойства ресурсов типа узла или запуск действий повторного действия повторного действия в определенных точках типа узла с параметром -Reimage.

### [Set-AzServiceFabricSetting](Set-AzServiceFabricSetting.md)
Добавьте или обновйте один или несколько параметров "Служиная ткань" в кластер.

### [Set-AzServiceFabricUpgradeType](Set-AzServiceFabricUpgradeType.md)
Измените тип обновления "Служивая ткань" для кластера.

### [Update-AzServiceFabricApplication](Update-AzServiceFabricApplication.md)
Обновив приложение с тканью службы. Это позволяет обновить параметры приложения и (или) версию типа приложения, которая активирует обновление приложения.

### [Update-AzServiceFabricDurability](Update-AzServiceFabricDurability.md)
Обновите уровень надежности (VMSKU) типа узла в кластере.

### [Update-AzServiceFabricReliability](Update-AzServiceFabricReliability.md)
Обновление уровня надежности основного типа узла в кластере.

