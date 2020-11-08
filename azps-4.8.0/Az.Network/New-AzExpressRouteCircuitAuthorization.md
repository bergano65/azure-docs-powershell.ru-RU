---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 28b45f5368fb7a63450276c054654313d7e1c517
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243006"
---
# New-AzExpressRouteCircuitAuthorization

## КРАТКИй обзор
Создание авторизации канала ExpressRoute.

## Максимальное

```
New-AzExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzExpressRouteCircuitAuthorization** создает разрешение на канал, которое можно добавить в цепь ExpressRoute. Каналы ExpressRoute соединяют локальную сеть с облаком Microsoft, используя поставщик услуг по подключению к сети, а не общедоступный Интернет. Владелец канала ExpressRoute может создать до 10 авторизаций для каждой цепи; Эти авторизации создают ключ проверки подлинности, который может использоваться владельцем виртуальной сети для подключения к каналу сети. На виртуальную сеть может быть только одна авторизация.
После того как вы создадите цепь ExpressRoute, вы можете использовать **Add-AzExpressRouteCircuitAuthorization** , чтобы добавить авторизацию для этого канала.
Кроме того, вы можете использовать **New-AzExpressRouteCircuitAuthorization** для создания авторизации, которая может быть добавлена в новую цепь одновременно с созданием канала.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание авторизации новой цепи
```
$Authorization = New-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

Эта команда создает новое разрешение на канал с именем ContosoCircuitAuthorization и сохраняет этот объект в переменной с именем $Authorization. Сохранение объекта в переменной играет важную роль: Несмотря на то, что **New-AzExpressRouteCircuitAuthorization** может создавать полномочия на канал, он не может добавить эту авторизацию в маршрут цепи. Вместо этого переменная $Authorization используется New-AzExpressRouteCircuit при создании новой цепи ExpressRoute.
Дополнительные сведения можно найти в документации по командлету New-AzExpressRouteCircuit.

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

### -Name (имя)
Указывает уникальное имя для новой авторизации канала ExpressRoute.

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitAuthorization

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Add-AzExpressRouteCircuitAuthorization](./Add-AzExpressRouteCircuitAuthorization.md)

[Get-AzExpressRouteCircuitAuthorization](./Get-AzExpressRouteCircuitAuthorization.md)

[Remove-AzExpressRouteCircuitAuthorization](./Remove-AzExpressRouteCircuitAuthorization.md)

