---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermexpressroutecircuitauthorization
schema: 2.0.0
ms.openlocfilehash: 9b41eb0c95c2b1693e56c8b11fee86b6e49a4609
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913856"
---
# Add-AzureRmExpressRouteCircuitAuthorization

## КРАТКИй обзор
Добавление авторизации канала ExpressRoute.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Add-AzureRmExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Add-AzureRmExpressRouteCircuitAuthorization** добавляет авторизацию в канал ExpressRoute. Каналы ExpressRoute соединяют локальную сеть с облаком Microsoft, используя поставщик услуг по подключению к сети, а не общедоступный Интернет. Владелец канала ExpressRoute может создать до 10 авторизаций для каждой цепи; Эти авторизации создают ключ авторизации, который может использоваться владельцем виртуальной сети для подключения своей сети к цепи (одной авторизации на виртуальную сеть). **Add-AzureRmExpressRouteCircuitAuthorization** добавляет новую авторизацию в цепь и, в то же время, создает соответствующий ключ проверки подлинности. Эти ключи можно просмотреть в любое время, запустив командлет Get-AzureRmExpressRouteCircuitAuthorization и, при необходимости, можно скопировать его и перенаправить на соответствующий владелец сети.

Обратите внимание, что после выполнения **Add-AzureRmExpressRouteCircuitAuthorization** необходимо вызвать командлет Set-AzureRmExpressRouteCircuit, чтобы активировать ключ. Если вы не вызываете **Set-AzureRmExpressRouteCircuit** , авторизация будет добавлена в цепь, но не будет включена для использования.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Добавление авторизации для указанной цепи ExpressRoute
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

Команды в этом примере добавляют новую авторизацию в существующую цепь ExpressRoute. Первая команда использует **Get-AzureRmExpressRouteCircuit** для создания ссылки на объект в канале с именем ContosoCircuit. Ссылка на объект хранится в переменной с именем $Circuit.

Во второй команде командлет **Add-AzureRmExpressRouteCircuitAuthorization** используется для добавления новой авторизации (ContosoCircuitAuthorization) в цепь ExpressRoute. Эта команда добавляет авторизацию, но не активирует эту авторизацию. Для активации авторизации требуется **Set-AzureRmExpressRouteCircuit** , показанный в финальной команде примера.

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
Указывает канал ExpressRoute, на который добавляется этот командлет.

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
Указывает имя добавляемой авторизации цепи.

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

### PSExpressRouteCircuit
**Add-AzureRmExpressRouteCircuitAuthorization** принимает конвейерные экземпляры объекта **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit** .

## НАПРЯЖЕНИЕ

### PSExpressRouteCircuit
**Add-AzureRmExpressRouteCircuitAuthorization** изменяет экземпляры объекта **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit** .

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmExpressRouteCircuit](./Get-AzureRmExpressRouteCircuit.md)

[Get-AzureRmExpressRouteCircuitAuthorization](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[New-AzureRmExpressRouteCircuitAuthorization](./New-AzureRmExpressRouteCircuitAuthorization.md)

[Remove-AzureRmExpressRouteCircuitAuthorization](./Remove-AzureRmExpressRouteCircuitAuthorization.md)

[Set-AzureRmExpressRouteCircuit](./Set-AzureRmExpressRouteCircuit.md)
