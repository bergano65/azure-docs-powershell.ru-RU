---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
ms.openlocfilehash: e596ea3092cd5fda045c20f80c9208015b57a42d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394180"
---
# Remove-AzRouteFilterRuleConfig

## SYNOPSIS
Удаляет правило фильтра маршрутов из фильтра маршрутов.

## СИНТАКСИС

```
Remove-AzRouteFilterRuleConfig -Name <String> -RouteFilter <PSRouteFilter> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## ОПИСАНИЕ
Чтобы **удалить правило фильтра** маршрутов из фильтра маршрутов, удалите из него правило фильтра маршрутов.

## ПРИМЕРЫ

### Пример 1
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01"
```

Первая команда получает фильтр маршрутов с именем RouteFilter01, который принадлежит группе ресурсов ResourceGroup01, и сохраняет его в переменной $rf ресурса.
Вторая команда удаляет правило фильтра маршрутов "Правило01" из фильтра маршрутов, $rf.

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

### -Force
Не спрашивайте подтверждения при переописи ресурса

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Имя правила фильтрации маршрутов

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

### -RouteFilter
Маршрутизатор

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Confirm
Перед запуском cmdlet вам будет предложено подтвердить его.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске cmdlet. Этот cmdlet не будет выполниться.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.Network.Models.PSRouteFilter

## OUTPUTS

### Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Add-AzRouteFilterRuleConfig](./Add-AzRouteFilterRuleConfig.md)

[Get-AzRouteFilterRuleConfig](./Get-AzRouteFilterRuleConfig.md)

[New-AzRouteFilterRuleConfig](./New-AzRouteFilterRuleConfig.md)

[Set-AzRouteFilterRuleConfig](./Set-AzRouteFilterRuleConfig.md)

[Get-AzRouteFilter](./Get-AzRouteFilter.md)

[New-AzRouteFilter](./New-AzRouteFilter.md)

[Remove-AzRouteFilter](./Remove-AzRouteFilter.md)

[Set-AzRouteFilter](./Set-AzRouteFilter.md)
