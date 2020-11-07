---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermexpressroutecircuitauthorization
schema: 2.0.0
ms.openlocfilehash: f0e66c1e601ab63eec6d2540edd3ba0235727e9a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913797"
---
# New-AzureRmExpressRouteCircuitAuthorization

## КРАТКИй обзор
Создание авторизации канала ExpressRoute.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
New-AzureRmExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzureRmExpressRouteCircuitAuthorization** создает разрешение на канал, которое можно добавить в цепь ExpressRoute. Каналы ExpressRoute соединяют локальную сеть с облаком Microsoft, используя поставщик услуг по подключению к сети, а не общедоступный Интернет. Владелец канала ExpressRoute может создать до 10 авторизаций для каждой цепи; Эти авторизации создают ключ проверки подлинности, который может использоваться владельцем виртуальной сети для подключения к каналу сети. На виртуальную сеть может быть только одна авторизация.

После того как вы создадите цепь ExpressRoute, вы можете использовать **Add-AzureRmExpressRouteCircuitAuthorization** , чтобы добавить авторизацию для этого канала.
Кроме того, вы можете использовать **New-AzureRmExpressRouteCircuitAuthorization** для создания авторизации, которая может быть добавлена в новую цепь одновременно с созданием канала.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание авторизации новой цепи
```
$Authorization = New-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

Эта команда создает новое разрешение на канал с именем ContosoCircuitAuthorization и сохраняет этот объект в переменной с именем $Authorization. Сохранение объекта в переменной играет важную роль: Несмотря на то, что **New-AzureRmExpressRouteCircuitAuthorization** может создавать полномочия на канал, он не может добавить эту авторизацию в маршрут цепи. Вместо этого переменная $Authorization используется New-AzureRmExpressRouteCircuit при создании новой цепи ExpressRoute.

Дополнительные сведения можно найти в документации по командлету New-AzureRmExpressRouteCircuit.

## ПАРАМЕТРЫ

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (имя)
Указывает уникальное имя для новой авторизации канала ExpressRoute.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего
Этот командлет не поддерживает конвейерный вход.

## НАПРЯЖЕНИЕ

### PSExpressRouteCircuitAuthorization
Этот командлет создает экземпляры объекта **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitAuthorization** .

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Add-AzureRmExpressRouteCircuitAuthorization](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[Get-AzureRmExpressRouteCircuitAuthorization](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[Remove-AzureRmExpressRouteCircuitAuthorization](./Remove-AzureRmExpressRouteCircuitAuthorization.md)

