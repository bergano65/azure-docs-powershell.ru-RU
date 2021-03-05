---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 57A6DB40-43EC-402C-9784-06817ECD99B8
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 04c7ef7dd041ce26802f23117edab79353816283
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994076"
---
# Get-AzApplicationGatewayRequestRoutingRule

## SYNOPSIS
Получает правило маршрутинга запросов шлюза приложения.

## СИНТАКСИС

```
Get-AzApplicationGatewayRequestRoutingRule [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
Cmdlet **Get-AzApplicationGatewayRequestRoutingRule** получает правило маршрутизации запросов шлюза приложения.

## ПРИМЕРЫ

### Пример 1. Получите определенное правило маршрутинга запросов
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRequestRoutingRule -"Rule01" -ApplicationGateway $AppGW
```

Первая команда получает шлюз приложения ApplicationGateway01 и сохраняет результат в переменной с $AppGW.
Вторая команда получает правило маршрутизов запроса "Правило01" из шлюза приложения, храняного в переменной с $AppGW.

### Пример 2. Получить список правил маршрутки запросов
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rules = Get-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGW
```

Первая команда получает шлюз приложения ApplicationGateway01 и сохраняет результат в переменной с $AppGW.
Вторая команда получает список правил маршрутизов запросов из шлюза приложения, храняного в переменной с именем $AppGW.

## PARAMETERS

### -ApplicationGateway
Определяет объект шлюза приложения, который содержит правило маршрутинга запросов.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

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

### -Name
Указывает имя правила маршрутки запроса, которое получает этот cmdlet.

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

### Microsoft.Azure.Commands.Network.Models.PSApplicationGateway

## OUTPUTS

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Add-AzApplicationGatewayRequestRoutingRule](./Add-AzApplicationGatewayRequestRoutingRule.md)

[New-AzApplicationGatewayRequestRoutingRule](./New-AzApplicationGatewayRequestRoutingRule.md)

[Remove-AzApplicationGatewayRequestRoutingRule](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[Set-AzApplicationGatewayRequestRoutingRule](./Set-AzApplicationGatewayRequestRoutingRule.md)


