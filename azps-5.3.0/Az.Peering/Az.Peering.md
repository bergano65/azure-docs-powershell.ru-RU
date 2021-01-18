---
Module Name: Az.Peering
Module Guid: 6c848b97-4dd4-49ef-b385-43c64905d25a
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.peering.md
Help Version: 0.1.0
Locale: e-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Az.Peering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Az.Peering.md
ms.openlocfilehash: 568c235bee84238d53849e8fb9dc3258e907cb18
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506047"
---
# Модуль Az.Peering
## Описание
Служба пиринга Майкрософт позволяет клиентам и майкрософт подключаться к Azure и представлять свои сетевые ресурсы в ARM объектах.

## Az.Peering Cmdlets
### [Get-AzLegacyPeering](Get-AzLegacyPeering.md)
Используется для преобразования устаревших ресурсов пиринга в ресурсы управления ресурсами Azure (ARM). 

### [Get-AzPeerAsn](Get-AzPeerAsn.md)
Получает объект PeerAsn из ARM.

### [Get-AzPeering](Get-AzPeering.md)
Получает ресурсы пиринга для подписки

### [Get-AzPeeringLocation](Get-AzPeeringLocation.md)
Получает расположения пиринга, предлагаемые корпорацией Майкрософт

### [Get-AzPeeringReceivedRoute](Get-AzPeeringReceivedRoute.md)
Список полученных маршрутов для пиринга.

### [Get-AzPeeringRegisteredAsn](Get-AzPeeringRegisteredAsn.md)
Получает зарегистрированные asN для пиринга серверов маршрутов Exchange в Интернете.

### [Get-AzPeeringRegisteredPrefix](Get-AzPeeringRegisteredPrefix.md)
Возвращает или перечисляет зарегистрированный префикс для пиринга.

### [Get-AzPeeringService](Get-AzPeeringService.md)
Получить список объектов одноранговой службы для одного объекта.

### [Get-AzPeeringServiceCountry](Get-AzPeeringServiceCountry.md)
Список стран, доступных для пиринга.

### [Get-AzPeeringServiceLocation](Get-AzPeeringServiceLocation.md)
Возвращает список местоположений пиринга, предлагаемых корпорацией Майкрософт.

### [Get-AzPeeringServicePrefix](Get-AzPeeringServicePrefix.md)
Получает список префиксов службы пиринга для подписки.

### [Get-AzPeeringServiceProvider](Get-AzPeeringServiceProvider.md)
Получает список поставщиков услуг пиринга, партнерских с Корпорацией Майкрософт.

### [New-AzPeerAsn](New-AzPeerAsn.md)
Создание нового одноранговых asN 

### [New-AzPeerAsnContactDetail](New-AzPeerAsnContactDetail.md)
Создает контакт в памяти для peerAsn. 

### [New-AzPeering](New-AzPeering.md)
Создание нового ресурса для ARM пиринга

### [New-AzPeeringDirectConnectionObject](New-AzPeeringDirectConnectionObject.md)
Создает psObject в памяти, который будет использоваться для создания или изменения пиринга.

### [New-AzPeeringExchangeConnectionObject](New-AzPeeringExchangeConnectionObject.md)
Создает psObject в памяти, который будет использоваться для создания или изменения пиринга.

### [New-AzPeeringRegisteredAsn](New-AzPeeringRegisteredAsn.md)
Создание зарегистрированного asN для пиринга

### [New-AzPeeringRegisteredPrefix](New-AzPeeringRegisteredPrefix.md)
Создание зарегистрированных префиксов для объектов пиринга.

### [New-AzPeeringService](New-AzPeeringService.md)
Создает новую службу пиринга.

### [New-AzPeeringServicePrefix](New-AzPeeringServicePrefix.md)
Создание нового префикса службы пиринга

### [Remove-AzPeerAsn](Remove-AzPeerAsn.md)
Удалить одноранговой asn

### [Remove-AzPeering](Remove-AzPeering.md)
Удаление пиринга. При этом будут удалены все детские ресурсы или оповещения для ресурса.

### [Remove-AzPeeringRegisteredAsn](Remove-AzPeeringRegisteredAsn.md)
Удаление зарегистрированного ASN из родительского ресурса пиринга.

### [Remove-AzPeeringRegisteredPrefix](Remove-AzPeeringRegisteredPrefix.md)
Удаление зарегистрированного префикса из родительского ресурса пиринга.

### [Remove-AzPeeringServicePrefix](Remove-AzPeeringServicePrefix.md)
Удаление нового префикса службы пиринга

### [Set-AzPeerAsn](Set-AzPeerAsn.md)
Обновление контактных данных

### [Set-AzPeeringDirectConnectionObject](Set-AzPeeringDirectConnectionObject.md)
Задает или обновляет сведения о прямом под соединении. 

### [Set-AzPeeringExchangeConnectionObject](Set-AzPeeringExchangeConnectionObject.md)
Задает или обновляет сведения о подменю Exchange. 

### [Set-AzPeeringRegisteredAsn](Set-AzPeeringRegisteredAsn.md)
Задает или обновляет зарегистрированное ASN от родительского ресурса пиринга.

### [Set-AzPeeringRegisteredPrefix](Set-AzPeeringRegisteredPrefix.md)
Задает или обновляет зарегистрированный префикс от родительского ресурса пиринга.

### [Update-AzPeering](Update-AzPeering.md)
Задает пиринг. Используйте эту команду в сочетании с или `Set-AzDirectPeeringConnectionObject` `Set-AzExchangePeeringConnectionObject` .

