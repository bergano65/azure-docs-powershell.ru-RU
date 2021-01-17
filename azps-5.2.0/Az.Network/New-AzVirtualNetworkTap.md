---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkTap.md
ms.openlocfilehash: 0ac64d9b1aee363a1681b8d62da2ecf73574f7cd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412319"
---
# New-AzVirtualNetworkTap

## SYNOPSIS
Создает ресурс VirtualNetworkTap.

## СИНТАКСИС

### SetByResource (по умолчанию)
```
New-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-DestinationPort <Int32>]
 [-Location <String>] [-Tag <Hashtable>]
 [-DestinationNetworkInterfaceIPConfiguration <PSNetworkInterfaceIPConfiguration>]
 [-DestinationLoadBalancerFrontEndIPConfiguration <PSFrontendIPConfiguration>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByResourceId
```
New-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-DestinationPort <Int32>]
 [-Location <String>] [-Tag <Hashtable>] [-DestinationNetworkInterfaceIPConfigurationId <String>]
 [-DestinationLoadBalancerFrontEndIPConfigurationId <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## ОПИСАНИЕ
Командлет **New-AzVirtualNetworkTap** создает ресурс виртуального сетевого касания Azure.

## ПРИМЕРЫ

### Пример 1. Создание виртуального касания в сети Azure
```
PS C:\>New-AzVirtualNetworkTap -Name "VirtualNetworkTap1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -DestinationPort 8888 -DestinationNetworkInterfaceIPConfiguration $destinationNic.IpConfigurations[0]
```

Эта команда создает виртуальный сетевой касание с именем VirtualNetworkTap1, который имеет сведения о конечной конфигурации VM (DestinationIpConfiguration, DestinationPort).
Весь исходный трафик, на который настроен трафик VM, будет перенаправлен на этот IP-адрес назначения + порт.

### Пример 2. Создание виртуального сетевого касания Azure с помощью IP-адреса LoadBalancer
```
# Create LoadBalancer
PS C:\>$frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
PS C:\>New-AzVirtualNetworkTap -Name "VirtualNetworkTap1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -DestinationLoadBalancerFrontEndIPConfiguration $frontend
```

Эта команда создает виртуальный сетевой касание с именем VirtualNetworkTap1, который имеет сведения о конечной конфигурации VM (FrontEndIpConfiguration).
Весь трафик, касаемыйся источника, настроенного на VM, будет маршрутироваться в эту загрузку LoadBalancer IpConfiguration. Порт назначения по умолчанию — 4789.

## PARAMETERS

### -AsJob
Запуск cmdlet в фоновом режиме

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

### -DestinationLoadBalancerFrontEndIPConfiguration
Ссылка на ресурс конфигурации переднего IP-адреса балансиров нагрузки назначения.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DestinationLoadBalancerFrontEndIPConfigurationId
Ссылка на ресурс конфигурации переднего IP-адреса балансиров нагрузки назначения.

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DestinationNetworkInterfaceIPConfiguration
Ссылка на ресурс конфигурации IP-интерфейса конечной сети.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DestinationNetworkInterfaceIPConfigurationId
Ссылка на ресурс конфигурации IP-интерфейса конечной сети.

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DestinationPort
Порт назначения сборщика пакетов

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Location
Расположение.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Имя касания.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов виртуального сетевого касания.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
A hashtable which represents resource tags.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Показывает, что произойдет при запуске cmdlet.
Этот cmdlet не будет выполниться.

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

### System.String

### System.Int32

### System.Collections.Hashtable

### Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration

### Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration

## OUTPUTS

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzVirtualNetworkTap](./Get-AzVirtualNetworkTap.md)

[Remove-AzVirtualNetworkTap](./Remove-AzVirtualNetworkTap.md)

[Set-AzVirtualNetworkTap](./Set-AzVirtualNetworkTap.md)
