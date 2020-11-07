---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: efe2a149d2ca02c075b2e0a1f73191e9e2b8859b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910147"
---
# Add-AzExpressRouteCircuitAuthorization

## КРАТКИй обзор
Добавление авторизации канала ExpressRoute.

## Максимальное

```
Add-AzExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Add-AzExpressRouteCircuitAuthorization** добавляет авторизацию в канал ExpressRoute. Каналы ExpressRoute соединяют локальную сеть с облаком Microsoft, используя поставщик услуг по подключению к сети, а не общедоступный Интернет. Владелец канала ExpressRoute может создать до 10 авторизаций для каждой цепи; Эти авторизации создают ключ авторизации, который может использоваться владельцем виртуальной сети для подключения своей сети к цепи (одной авторизации на виртуальную сеть). **Add-AzExpressRouteCircuitAuthorization** добавляет новую авторизацию в цепь и, в то же время, создает соответствующий ключ проверки подлинности. Эти ключи можно просмотреть в любое время, запустив командлет Get-AzExpressRouteCircuitAuthorization и, при необходимости, можно скопировать его и перенаправить на соответствующий владелец сети.

Обратите внимание, что после выполнения **Add-AzExpressRouteCircuitAuthorization** необходимо вызвать командлет Set-AzExpressRouteCircuit, чтобы активировать ключ. Если вы не вызываете **Set-AzExpressRouteCircuit** , авторизация будет добавлена в цепь, но не будет включена для использования.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Добавление авторизации для указанной цепи ExpressRoute
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

Команды в этом примере добавляют новую авторизацию в существующую цепь ExpressRoute. Первая команда использует **Get-AzExpressRouteCircuit** для создания ссылки на объект в канале с именем ContosoCircuit. Ссылка на объект хранится в переменной с именем $Circuit.

Во второй команде командлет **Add-AzExpressRouteCircuitAuthorization** используется для добавления новой авторизации (ContosoCircuitAuthorization) в цепь ExpressRoute. Эта команда добавляет авторизацию, но не активирует эту авторизацию. Для активации авторизации требуется **Set-AzExpressRouteCircuit** , показанный в финальной команде примера.

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### PSExpressRouteCircuit
**Add-AzExpressRouteCircuitAuthorization** принимает конвейерные экземпляры объекта **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit** .

## НАПРЯЖЕНИЕ

### PSExpressRouteCircuit
**Add-AzExpressRouteCircuitAuthorization** изменяет экземпляры объекта **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit** .

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzExpressRouteCircuit](./Get-AzExpressRouteCircuit.md)

[Get-AzExpressRouteCircuitAuthorization](./Get-AzExpressRouteCircuitAuthorization.md)

[New-AzExpressRouteCircuitAuthorization](./New-AzExpressRouteCircuitAuthorization.md)

[Remove-AzExpressRouteCircuitAuthorization](./Remove-AzExpressRouteCircuitAuthorization.md)

[Set-AzExpressRouteCircuit](./Set-AzExpressRouteCircuit.md)
