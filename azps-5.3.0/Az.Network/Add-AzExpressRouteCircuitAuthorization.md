---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 047400472d3f42d5daff0f0ea6aed44455608eb3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518158"
---
# Add-AzExpressRouteCircuitAuthorization

## SYNOPSIS
Добавляет авторизацию каналов ExpressRoute.

## СИНТАКСИС

```
Add-AzExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
Cmdlet **Add-AzExpressRouteCircuitAuthorization добавляет** авторизацию в канал ExpressRoute. С помощью каналов ExpressRoute ваша локальной сети подключается к Облаку Майкрософт с помощью поставщика услуг подключения, а не открытого Интернета. Владелец каналов ExpressRoute может создать до 10 авторизации для каждого из них. Эти авторизации создают ключ авторизации, который может использовать виртуальный владелец сети для подключения своей сети к каналу (по одной авторизации на виртуальную сеть). **Add-AzExpressRouteCircuitAuthorization** добавляет новую авторизацию в канал и одновременно создает соответствующий ключ авторизации. Эти ключи можно просмотреть в любое время с помощью Get-AzExpressRouteCircuitAuthorization- и при необходимости скопировать и перена вперед для соответствующего владельца сети.
Обратите внимание, что после запуска **Add-AzExpressRouteCircuitAuthorization** необходимо вызвать Set-AzExpressRouteCircuit для активации ключа. Если вы не позвоните **в Set-AzExpressRouteCircuit,** авторизация будет добавлена в канал, но не будет включена для использования.

## ПРИМЕРЫ

### Пример 1. Добавление авторизации в указанный канал ExpressRoute
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

Команды в этом примере добавляют новую авторизацию в существующий канал ExpressRoute. Первая команда использует **Get-AzExpressRouteCircuit** для создания ссылки на объект в канал ContosoCircuit. Эта ссылка на объект хранится в переменной с именем $Circuit.
Во второй команде командлет **Add-AzExpressRouteCircuitAuthorization** используется для добавления новой авторизации (ContosoCircuitAuthorization) в канал ExpressRoute. Эта команда добавляет авторизацию, но не активирует ее. Для активации авторизации требуется **Set-AzExpressRouteCircuit,** показанный в последней команде в примере.

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
Определяет канал ExpressRoute, в который этот cmdlet добавляет авторизацию.

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
Указывает имя добавляемой авторизации каналов.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit

## OUTPUTS

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzExpressRouteCircuit](./Get-AzExpressRouteCircuit.md)

[Get-AzExpressRouteCircuitAuthorization](./Get-AzExpressRouteCircuitAuthorization.md)

[New-AzExpressRouteCircuitAuthorization](./New-AzExpressRouteCircuitAuthorization.md)

[Remove-AzExpressRouteCircuitAuthorization](./Remove-AzExpressRouteCircuitAuthorization.md)

[Set-AzExpressRouteCircuit](./Set-AzExpressRouteCircuit.md)
