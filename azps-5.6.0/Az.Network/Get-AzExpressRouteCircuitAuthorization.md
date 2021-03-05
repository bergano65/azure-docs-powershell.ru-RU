---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 2c58549ee79cd24d29c1e3549d729995313c5748
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967848"
---
# Get-AzExpressRouteCircuitAuthorization

## SYNOPSIS
Сведения о авторизации каналов ExpressRoute.

## СИНТАКСИС

```
Get-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
Cmdlet **Get-AzExpressRouteCircuitAuthorization получает** сведения о разрешениях, которые назначены каналу ExpressRoute. Схемы ExpressRoute подключают вашу локальное сеть к Microsoft Cloud с помощью поставщика услуг подключения, а не через общедоступный Интернет. Владелец каналов ExpressRoute может создать до 10 авторизации для каждого из них. Эти авторизации создают ключ авторизации, который может использовать виртуальный владелец сети для подключения своей сети к каналу (по одной авторизации на виртуальную сеть). Ключи авторизации, а также другие сведения о авторизации можно просмотреть в любое время с помощью **get-AzExpressRouteCircuitAuthorization.**

## ПРИМЕРЫ

### Пример 1. Получить все авторизации ExpressRoute
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit
```

Эти команды возвращают сведения обо всех авторизациях ExpressRoute, связанных с каналом ExpressRoute. Первая команда использует командлет **Get-AzExpressRouteCircuit** для создания ссылки на объект в канале ContosoCircuit; эта ссылка на объект хранится в переменной $Circuit. Затем вторая команда использует эту ссылку на объект и командлет **Get-AzExpressRouteCircuitAuthorization** для возврата сведений о разрешениях, связанных с ContosoCircuit.

### Пример 2. Получить все авторизацию ExpressRoute с Where-Object-управления
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

Эти команды представляют собой один из вариантов команд, используемых в примере 1. Однако в этом случае сведения возвращаются только для тех авторов, которые доступны для использования (то есть для авторизации, не назначенной виртуальной сети). Для этого сведения о авторизации канала возвращаются в команде 2 и сдаются **командлету Where-Object** по каналу.
**Затем Where-Object** выбирает только те авторизации, для которых свойство *AuthorizationUseStatus* имеет разрешение Available. Чтобы перечислить только те авторизации, которые недоступны, используйте такой синтаксис для предложения Where: `{$_.AuthorizationUseStatus -ne "Available"}`

## PARAMETERS

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
Определяет авторизацию каналов ExpressRoute.

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

### -Name
Указывает имя авторизации каналов ExpressRoute, которую получает этот cmdlet.
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
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit

## OUTPUTS

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Add-AzExpressRouteCircuitAuthorization](./Add-AzExpressRouteCircuitAuthorization.md)

[Get-AzExpressRouteCircuit](./Get-AzExpressRouteCircuit.md)

[New-AzExpressRouteCircuitAuthorization](./New-AzExpressRouteCircuitAuthorization.md)

[Remove-AzExpressRouteCircuitAuthorization](./Remove-AzExpressRouteCircuitAuthorization.md)
