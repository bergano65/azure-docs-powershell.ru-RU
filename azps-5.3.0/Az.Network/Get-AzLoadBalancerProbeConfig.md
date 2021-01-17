---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 278228EB-0126-4F27-A30F-51DC498C65FE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 5b6031657438bfc28ce76519c8489e041a060965
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422252"
---
# Get-AzLoadBalancerProbeConfig

## SYNOPSIS
Получает конфигурацию формы для балансиров нагрузки.

## СИНТАКСИС

```
Get-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
Для балансиров нагрузки с его стороны возвращается одна или несколько конфигураций **для get-AzLoadBalancerProbeConfig.**

## ПРИМЕРЫ

### Пример 1. Настройка баланса нагрузки
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $slb
```

Первая команда получает балансировку нагрузки MyLoadBalancer, а затем сохраняет его в переменной $slb.
Вторая команда получает связанную конфигурацию с именем MyProbe из балансиров нагрузки в $slb.

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

### -LoadBalancer
Определяет балансировую нагрузку, связанную с конфигурацией, которую нужно получить.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Name
Указывает имя конфигурации, которая будет получаться.

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

### Microsoft.Azure.Commands.Network.Models.PSLoadBalancer

## OUTPUTS

### Microsoft.Azure.Commands.Network.Models.PSProbe

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Add-AzLoadBalancerProbeConfig](./Add-AzLoadBalancerProbeConfig.md)

[Get-AzLoadBalancer](./Get-AzLoadBalancer.md)

[New-AzLoadBalancerProbeConfig](./New-AzLoadBalancerProbeConfig.md)

[Remove-AzLoadBalancerProbeConfig](./Remove-AzLoadBalancerProbeConfig.md)

[Set-AzLoadBalancerProbeConfig](./Set-AzLoadBalancerProbeConfig.md)


