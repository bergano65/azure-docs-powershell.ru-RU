---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33E
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/add-aztrafficmanagercustomheadertoendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToEndpoint.md
ms.openlocfilehash: 4a24953dd763c54cba7454bf9e46bb9373b0f450
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987409"
---
# Add-AzTrafficManagerCustomHeaderToEndpoint

## SYNOPSIS
Добавляет пользовательские сведения о заглавной точке в локальный объект конечной точки Диспетчера трафика.

## СИНТАКСИС

```
Add-AzTrafficManagerCustomHeaderToEndpoint -Name <String> -Value <String>
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## ОПИСАНИЕ
Cmdlet **Add-AzTrafficManagerCustomHeaderToEndpoint** добавляет пользовательские данные заголовок к локальному объекту конечной точки Диспетчера трафика Azure.
Конечную точку можно получить с помощью New-AzTrafficManagerEndpoint или Get-AzTrafficManagerEndpoint.

Этот cmdlet выполняется с объектом локальной конечной точки.
Зафиксировать изменения в конечной точке диспетчера трафика с помощью Set-AzTrafficManagerEndpoint управления.

## ПРИМЕРЫ

### Пример 1. Добавление пользовательских данных в конечную точку
```
PS C:\> $TrafficManagerEndpoint = New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzTrafficManagerCustomHeaderToEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

Первая команда создает конечную точку Диспетчера трафика Azure с помощью командлета **New-AzTrafficManagerEndpoint.**
При этом локализованная конечная точка хранится в переменной $TrafficManagerEndpoint.
Вторая команда добавляет настраиваемые сведения о заглавных точках в конечную точку, $TrafficManagerEndpoint.
Конечная команда обновляет конечную точку диспетчера трафика в соответствие с локальным значением в $TrafficManagerEndpoint.

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
Определяет имя добавляемой настраиваемой информации.

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

### -TrafficManagerEndpoint
Определяет локальный **объект TrafficManagerEndpoint.**
Этот cmdlet изменяет этот локальный объект.
Чтобы получить объект **TrafficManagerEndpoint,** воспользуйтесь Get-AzTrafficManagerEndpoint или New-AzTrafficManagerEndpoint управления.

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Значение
Определяет значение добавляемой настраиваемой информации.

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

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint

## OUTPUTS

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Remove-AzTrafficManagerCustomHeaderFromEndpoint](./Remove-AzTrafficManagerCustomHeaderFromEndpoint.md)

[New-AzTrafficManagerEndpoint](./New-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerEndpoint.md)

[Set-AzTrafficManagerEndpoint](./Set-AzTrafficManagerEndpoint.md)
