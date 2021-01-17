---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D342
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagercustomheaderfromendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromEndpoint.md
ms.openlocfilehash: 35ab92add873e603101400f77e813fb115386fd4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391423"
---
# Remove-AzTrafficManagerCustomHeaderFromEndpoint

## SYNOPSIS
Удаляет пользовательские данные загона из локального объекта конечной точки Диспетчера трафика.

## СИНТАКСИС

```
Remove-AzTrafficManagerCustomHeaderFromEndpoint -Name <String> -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## ОПИСАНИЕ
Cmdlet **Remove-AzTrafficManagerCustomHeaderFromEndpoint** удаляет пользовательские данные заголовок из локального объекта конечной точки Диспетчера трафика Azure.
Конечную точку можно получить с помощью New-AzTrafficManagerEndpoint или Get-AzTrafficManagerEndpoint.

Этот cmdlet выполняется с объектом локальной конечной точки.
Зафиксировать изменения в конечной точке диспетчера трафика с помощью Set-AzTrafficManagerEndpoint управления.

## ПРИМЕРЫ

### Пример 1. Удаление сведений настраиваемой подсети из конечной точки
```
PS C:\> $TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzTrafficManagerCustomHeaderFromEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

Первая команда получает конечную точку Azure contoso из профиля ContosoProfile в группе ресурсов ResourceGroup11, а затем сохраняет объект в переменной $TrafficManagerEndpoint ресурса.
Вторая команда удаляет настраиваемые данные загона из конечной точки, храняной в $TrafficManagerEndpoint.
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
Указывает имя удаляемой настраиваемой информации.

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

[Add-AzTrafficManagerCustomHeaderToEndpoint](./Add-AzTrafficManagerCustomHeaderToEndpoint.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerEndpoint.md)

[New-AzTrafficManagerEndpoint](./New-AzTrafficManagerEndpoint.md)

[Set-AzTrafficManagerEndpoint](./Set-AzTrafficManagerEndpoint.md)
