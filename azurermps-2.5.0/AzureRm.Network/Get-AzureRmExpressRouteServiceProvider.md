---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteserviceprovider
schema: 2.0.0
ms.openlocfilehash: 7e4febe620b8a440d1f9a5eb0c9432da9ff47c74
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913834"
---
# Get-AzureRmExpressRouteServiceProvider

## КРАТКИй обзор
Получает список поставщиков услуг ExpressRoute и их атрибутов.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Get-AzureRmExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmExpressRouteServiceProvider** извлекает список поставщиков служб ExpressRoute и их атрибуты. Атрибут: расположение и параметры пропускной способности.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение списка поставщика услуг с разположениями в «Silicon впадина»
```
Get-AzureRmExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Network. Models. PSExpressRouteServiceProvider

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmExpressRouteCircuitARPTable](Get-AzureRmExpressRouteCircuitARPTable.md)

[Get-AzureRmExpressRouteCircuitRouteTable](Get-AzureRmExpressRouteCircuitRouteTable.md)

[Get-AzureRmExpressRouteCircuitRouteTableSummary](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[Get-AzureRmExpressRouteCircuitStats](Get-AzureRmExpressRouteCircuitStats.md)
