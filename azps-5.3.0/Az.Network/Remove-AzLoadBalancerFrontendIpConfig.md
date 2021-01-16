---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: bde16a6f3ecd68307574ae5eac7760a177101cc1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506876"
---
# Remove-AzLoadBalancerFrontendIpConfig

## SYNOPSIS
Удаляет конфигурацию IP-адресов переднего управления из балансиров нагрузки.

## СИНТАКСИС

```
Remove-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## ОПИСАНИЕ
При этом из балансиров нагрузки Azure удаляется клиентский IP-адрес конфигурации **Remove-AzLoadBalancerFrontendIpConfig.**

## ПРИМЕРЫ

### Пример 1. Удаление конфигурации ПЕРЕДНЕГО IP-адреса из балансира нагрузки
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

Первая команда получает балансировку нагрузки, связанную с IP-конфигурацией, которую вы хотите удалить, а затем сохраняет ее в переменной $loadbalancer.
Вторая команда удаляет связанную конфигурацию IP-адреса из балансира нагрузки в $loadbalancer.

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
Указывает балансировую нагрузку, которая содержит ip-конфигурацию переднего ip-адреса, которую нужно удалить.

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
Указывает имя конфигурации IP-адреса переднего ip-адреса, который нужно удалить.

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

### Microsoft.Azure.Commands.Network.Models.PSLoadBalancer

## OUTPUTS

### Microsoft.Azure.Commands.Network.Models.PSLoadBalancer

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Add-AzLoadBalancerFrontendIpConfig](./Add-AzLoadBalancerFrontendIpConfig.md)

[Get-AzLoadBalancer](./Get-AzLoadBalancer.md)

[Get-AzLoadBalancerFrontendIpConfig](./Get-AzLoadBalancerFrontendIpConfig.md)

[New-AzLoadBalancerFrontendIpConfig](./New-AzLoadBalancerFrontendIpConfig.md)

[Set-AzLoadBalancerFrontendIpConfig](./Set-AzLoadBalancerFrontendIpConfig.md)


