---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitAuthorization.md
ms.openlocfilehash: f990e2bb408fc9bb76c992d7de3e01b5eb88311b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563452"
---
# Remove-AzureRmExpressRouteCircuitAuthorization

## КРАТКИй обзор
Удаление существующей авторизации конфигурации ExpressRoute.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Remove-AzureRmExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Remove-AzureRmExpressRouteCircuitAuthorization** удаляет авторизацию, связанную с цепью ExpressRoute. Каналы ExpressRoute соединяют локальную сеть с Azure с помощью провайдера соединений вместо общедоступного Интернета. Владелец канала ExpressRoute может создать до 10 авторизаций для каждой цепи; Эти авторизации создают ключ авторизации, который может использоваться владельцем виртуальной сети для подключения своей сети к каналу. В каждой виртуальной сети может быть только одна авторизация. Тем не менее, в любое время владелец цепи может использовать **Remove-AzureRmExpressRouteCircuitAuthorization** для удаления авторизации, назначенной виртуальной сети. Когда это случится, соответствующая виртуальная сеть больше не сможет использовать цепь ExpressRoute для подключения к Azure.

## ИЛЛЮСТРИРУЮТ

### Пример 1: удаление авторизации канала из канала ExpressRoute
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

В этом примере удаляется проверка подлинности канала из канала ExpressRoute. Первая команда использует командлет **Get-AzureRmExpressRouteCircuit** для создания ссылки на объект в канале ExpressRoute с именем ContosoCircuit и сохраняет результат в переменной с именем $Circuit.

Вторая команда отмечает ContosoCircuitAuthorization авторизации канала для удаления.

Третья команда использует командлет Set-AzureRmExpressRouteCircuit для подтверждения удаления канала ExpressRoute, хранящегося в переменной $Circuit.

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

### -ExpressRouteCircuit
Указывает объект ExpressRouteCircuit, который удаляется этим командлетом.

```yaml
Type: PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (имя)
Указывает имя авторизации канала, которое удаляется этим командлетом.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### PSExpressRouteCircuit
Этот командлет принимает конвейерные экземпляры объекта **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit** .

## НАПРЯЖЕНИЕ

### PSExpressRouteCircuit
Этот командлет изменяет существующие экземпляры объекта **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit** .

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Add-AzureRmExpressRouteCircuitAuthorization](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[Get-AzureRmExpressRouteCircuit](./Get-AzureRmExpressRouteCircuit.md)

[Get-AzureRmExpressRouteCircuitAuthorization](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[New-AzureRmExpressRouteCircuitAuthorization](./New-AzureRmExpressRouteCircuitAuthorization.md)

[Set-AzureRmExpressRouteCircuit](./Set-AzureRmExpressRouteCircuit.md)
