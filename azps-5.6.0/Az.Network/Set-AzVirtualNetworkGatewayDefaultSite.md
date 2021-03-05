---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/powershell/module/az.network/set-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 8e35347813849badfa50100cc4cac418e2d66332
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979443"
---
# Set-AzVirtualNetworkGatewayDefaultSite

## SYNOPSIS
Задает сайт по умолчанию для виртуального сетевого шлюза.

## СИНТАКСИС

```
Set-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
Командлет **Set-AzVirtualNetworkGatewayDefaultSite** назначает принудительный сайт по умолчанию для туннелизации виртуальному сетевому шлюзу.
Принудительный туннелинг позволяет перенаправлять интернет-трафик с виртуальных машин Azure в вашу локальное сеть; это позволяет проверять и проверять трафик до его выпуска.
Принудительный туннелинг осуществляется с помощью VPN-туннель. для этого туннель требуется сайт по умолчанию — локальный шлюз, в котором перенаправляется весь интернет-трафик Azure.
**Сайт Set-AzVirtualNetworkGatewayDefaultSite** позволяет изменить сайт по умолчанию, который назначен шлюзу.

## ПРИМЕРЫ

### Пример 1. Назначение сайта по умолчанию виртуальному сетевому шлюзу
```
PS C:\>$LocalGateway = Get-AzLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

В этом примере сайт по умолчанию назначается виртуальному сетевому шлюзу с именем ContosoVirtualGateway.
Первая команда создает ссылку на локальный шлюз ContosoLocalGateway.
Эта ссылка на объект, которая хранится в переменной с именем $LocalGateway представляет шлюз, который нужно настроить как сайт по умолчанию.
Вторая команда затем создает ссылку на объект на виртуальный сетевой шлюз и сохраняет результат в переменной с $VirtualGateway.
Третья команда использует командлет **Set-AzVirtualNetworkGatewayDefaultSite,** чтобы назначить сайту ContosoVirtualGateway по умолчанию.

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

### -GatewayDefaultSite
Указывает ссылку на локальный сетевой шлюз, который должен быть назначен в качестве сайта по умолчанию для указанной виртуальной сети.
С помощью Get-AzLocalNetworkGateway можно создать ссылку на локальный шлюз.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGateway
Указывает ссылку на виртуальный сетевой шлюз, для которой будет назначен сайт по умолчанию.
Вы можете создать ссылку на виртуальный сетевой шлюз с помощью **Get-AzVirtualNetworkGateway** и указав имя шлюза.
Переменную $VirtualGateway затем можно использовать в качестве значения параметра *параметра VirtualNetworkGateway:*

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway

### Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway

## OUTPUTS

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzLocalNetworkGateway](./Get-AzLocalNetworkGateway.md)

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[Remove-AzVirtualNetworkGatewayDefaultSite](./Remove-AzVirtualNetworkGatewayDefaultSite.md)


