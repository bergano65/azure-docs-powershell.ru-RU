---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 910b432382eb24f6c5eaf77d3e0c7fe3dc547413
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910124"
---
# Add-AzRouteFilterRuleConfig

## КРАТКИй обзор
Добавляет правило фильтра маршрутов к фильтру маршрутов.

## Максимальное

```
Add-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет Add-AzRouteFilterRuleConfig добавляет правило фильтра маршрутов в фильтр маршрута Azure.

## ИЛЛЮСТРИРУЮТ

### --------------------------Пример 1: Добавление правила фильтра маршрутов в фильтр маршрута--------------------------
```
PS C:\>$RouteFilter = Get-AzRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

Первая команда получает фильтр маршрутов с именем routefilter01 с помощью командлета Get-AzRouteFilter.
Команда сохраняет фильтр в переменной $RouteFilter.

## ПАРАМЕТРЫ

### -Доступ
Задает доступ к правилу фильтра маршрутов, допустимые значения — Deny или Allow.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CommunityList
Список значений сообщества, по которому будет фильтроваться фильтр маршрутов

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -Force
Не запрашивать подтверждение, если вы хотите переделать ресурс

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (имя)
Указывает имя правила фильтра маршрутов, которое нужно добавить в фильтр маршрутов.

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

### -RouteFilter
Указывает фильтр маршрутов, к которому этот командлет добавляет правило фильтра маршрутов.

```yaml
Type: PSRouteFilter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RouteFilterRuleType
Указывает тип правила фильтра маршрутов.
Допустимые значения: Community

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Community

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Запрашивает подтверждение перед запуском командлета.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске командлета. Командлет не выполняется.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### PSRouteFilter
Параметр "RouteFilter" принимает значение типа "PSRouteFilter" из конвейера.

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Network. Models. PSRouteFilter

## Пуск
Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzRouteFilterRuleConfig](./Get-AzRouteFilterRuleConfig.md)

[Get-AzRouteFilter](./Get-AzRouteFilter.md)

[New-AzRouteFilterRuleConfigConfig](./New-AzRouteFilterRuleConfigConfig.md)

[Remove-AzRouteFilterRuleConfigConfig](./Remove-AzRouteFilterRuleConfigConfig.md)

[Set-AzRouteFilterRuleConfigConfig](./Set-AzRouteFilterRuleConfigConfig.md)

[Set-AzRouteFilter](./Set-AzRouteFilter.md)

