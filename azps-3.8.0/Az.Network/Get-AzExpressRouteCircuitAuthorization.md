---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 7c942968439d7d55fe78a3dd95c36501a2eaf10f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065848"
---
# Get-AzExpressRouteCircuitAuthorization

## КРАТКИй обзор
Получение сведений об авторизации канала ExpressRoute.

## Максимальное

```
Get-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzExpressRouteCircuitAuthorization** получает сведения о авторизациях, назначенных каналу ExpressRoute. Каналы ExpressRoute соединяют локальную сеть с облаком Microsoft, используя поставщик услуг по подключению к сети, а не общедоступный Интернет. Владелец канала ExpressRoute может создать до 10 авторизаций для каждой цепи; Эти авторизации создают ключ авторизации, который может использоваться владельцем виртуальной сети для подключения своей сети к цепи (одной авторизации на виртуальную сеть). Ключи авторизации, а также другие сведения об авторизации можно просмотреть в любое время, выполнив **Get-AzExpressRouteCircuitAuthorization**.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение всех авторизаций ExpressRoute
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit
```

Эти команды возвращают сведения обо всех параметрах авторизации ExpressRoute, связанных с цепью ExpressRoute. Первая команда использует командлет **Get-AzExpressRouteCircuit** для создания ссылки на объект в канале с именем ContosoCircuit; Ссылка на объект хранится в $Circuit переменной. Вторая команда использует ссылку на объект и командлет **Get-AzExpressRouteCircuitAuthorization** для получения сведений об авторизации, связанных с ContosoCircuit.

### Пример 2: получение всех авторизаций ExpressRoute с помощью командлета Where-Object
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

Эти команды представляют собой вариант команд, используемых в примере 1. Однако в этом случае информация возвращается только для тех авторизаций, которые доступны для использования (то есть для авторизаций, которые не назначены виртуальной сети). Для этого данные авторизации канала возвращаются в команде 2 и передаются в командлет **Where-Object** .
**Where-Object** затем выберет только те авторизации, для которых в свойстве *AuthorizationUseStatus* задано значение доступно. Чтобы вычислить только недоступные разрешения, используйте следующий синтаксис для предложения WHERE. `{$_.AuthorizationUseStatus -ne "Available"}`

## ПАРАМЕТРЫ

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpressRouteCircuit
Указывает для авторизации канала ExpressRoute.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
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
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## ВХОДНЫЕ данные

### Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitAuthorization

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Add-AzExpressRouteCircuitAuthorization](./Add-AzExpressRouteCircuitAuthorization.md)

[Get-AzExpressRouteCircuit](./Get-AzExpressRouteCircuit.md)

[New-AzExpressRouteCircuitAuthorization](./New-AzExpressRouteCircuitAuthorization.md)

[Remove-AzExpressRouteCircuitAuthorization](./Remove-AzExpressRouteCircuitAuthorization.md)
