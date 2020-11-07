---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitauthorization
schema: 2.0.0
ms.openlocfilehash: ec11ab37bc3fcb787de2b97f46941f23ede1b45a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913631"
---
# Get-AzureRmExpressRouteCircuitAuthorization

## КРАТКИй обзор
Получение сведений об авторизации канала ExpressRoute.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Get-AzureRmExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmExpressRouteCircuitAuthorization** получает сведения о авторизациях, назначенных каналу ExpressRoute. Каналы ExpressRoute соединяют локальную сеть с облаком Microsoft, используя поставщик услуг по подключению к сети, а не общедоступный Интернет. Владелец канала ExpressRoute может создать до 10 авторизаций для каждой цепи; Эти авторизации создают ключ авторизации, который может использоваться владельцем виртуальной сети для подключения своей сети к цепи (одной авторизации на виртуальную сеть). Ключи авторизации, а также другие сведения об авторизации можно просмотреть в любое время, выполнив **Get-AzureRmExpressRouteCircuitAuthorization**.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение всех авторизаций ExpressRoute
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzureRmExpressRouteCircuitAuthorization -Circuit $Circuit
```

Эти команды возвращают сведения обо всех параметрах авторизации ExpressRoute, связанных с цепью ExpressRoute. Первая команда использует командлет **Get-AzureRmExpressRouteCircuit** для создания ссылки на объект в канале с именем ContosoCircuit; Ссылка на объект хранится в $Circuit переменной. Вторая команда использует ссылку на объект и командлет **Get-AzureRmExpressRouteCircuitAuthorization** для получения сведений об авторизации, связанных с ContosoCircuit.

### Пример 2: получение всех авторизаций ExpressRoute с помощью командлета Where-Object
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzureRmExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

Эти команды представляют собой вариант команд, используемых в примере 1. Однако в этом случае информация возвращается только для тех авторизаций, которые доступны для использования (то есть для авторизаций, которые не назначены виртуальной сети). Для этого данные авторизации канала возвращаются в команде 2 и передаются в командлет **Where-Object** .
**Where-Object** затем выберет только те авторизации, для которых в свойстве *AuthorizationUseStatus* задано значение доступно. Чтобы вычислить только недоступные разрешения, используйте следующий синтаксис для предложения WHERE.

`{$_.AuthorizationUseStatus -ne "Available"}`

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
Указывает для авторизации канала ExpressRoute.

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
Указывает имя авторизации канала ExpressRoute, которое получает этот командлет.

-Name "ContosoCircuitAuthorization"

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
**Get-AzureRmExpressRouteCircuitAuthorization** принимает конвейерные экземпляры объекта **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit** .

## НАПРЯЖЕНИЕ

### PSExpressRouteCircuitAuthorization
Функция **Get-AzureRmExpressRouteCircuitAuthorization** возвращает экземпляры объекта **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitAuthorization** .

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Add-AzureRmExpressRouteCircuitAuthorization](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[Get-AzureRmExpressRouteCircuit](./Get-AzureRmExpressRouteCircuit.md)

[New-AzureRmExpressRouteCircuitAuthorization](./New-AzureRmExpressRouteCircuitAuthorization.md)

[Remove-AzureRmExpressRouteCircuitAuthorization](./Remove-AzureRmExpressRouteCircuitAuthorization.md)
