---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 28b45f5368fb7a63450276c054654313d7e1c517
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407724"
---
# New-AzExpressRouteCircuitAuthorization

## SYNOPSIS
Создает авторизацию каналов ExpressRoute.

## СИНТАКСИС

```
New-AzExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## ОПИСАНИЕ
**Новый-AzExpressRouteCircuitAuthorization создает** авторизацию каналов, которую можно добавить в канал ExpressRoute. Схемы ExpressRoute подключают вашу локальное сеть к Microsoft Cloud с помощью поставщика услуг подключения, а не через общедоступный Интернет. Владелец каналов ExpressRoute может создать до 10 авторизации для каждого из них. Эти авторизации создают ключ авторизации, который может использовать виртуальный владелец сети для подключения сети к каналу. В виртуальной сети может быть только одна авторизация.
После создания схемы ExpressRoute вы можете добавить авторизацию в канал с помощью **Add-AzExpressRouteCircuitAuthorization.**
Кроме того, вы можете создать авторизацию, которую можно добавить в новый канал при создании схемы, с помощью **New-AzExpressRouteCircuitAuthorization.**

## ПРИМЕРЫ

### Пример 1. Создание авторизации каналов
```
$Authorization = New-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

Эта команда создает новый канал авторизации ContosoCircuitAuthorization и сохраняет этот объект в переменной с именем $Authorization. Важно сохранить объект в переменной: хотя **New-AzExpressRouteCircuitAuthorization** может создать авторизацию каналов, она не может добавить это авторизацию в маршрут схемы. Вместо этого переменная $Authorization используется New-AzExpressRouteCircuit при создании нового схемы ExpressRoute.
Дополнительные сведения см. в документации New-AzExpressRouteCircuit управления проектами.

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

### -Name
Указывает уникальное имя для новой авторизации каналов ExpressRoute.

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

### Нет

## OUTPUTS

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Add-AzExpressRouteCircuitAuthorization](./Add-AzExpressRouteCircuitAuthorization.md)

[Get-AzExpressRouteCircuitAuthorization](./Get-AzExpressRouteCircuitAuthorization.md)

[Remove-AzExpressRouteCircuitAuthorization](./Remove-AzExpressRouteCircuitAuthorization.md)

