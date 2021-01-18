---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 13EF1028-43DE-424D-8185-EC45B5CEF2C1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 4c8dd4df4c3dd2d9aac8491b3d04e1755e6b4c38
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517953"
---
# Set-AzNetworkInterfaceIpConfig

## SYNOPSIS
Обновляет конфигурацию IP-адреса для сетевого интерфейса.

## СИНТАКСИС

### SetByResource (по умолчанию)
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>]
 [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### SetByResourceId
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
Командлет **Set-AzNetworkInterfaceIpConfig** обновляет конфигурацию IP-адреса для сетевого интерфейса.

## ПРИМЕРЫ

### 1. Изменение IP-адреса конфигурации IP-адреса
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet
    -Primary

$nic | Set-AzNetworkInterface
```

Первые две команды получают виртуальную сеть подсети под названием myvnet и подсеть подсети mysubnet и хранят ее в переменных, $vnet и $subnet соответственно. Третья команда получает сетевой интерфейс nic1, связанный с конфигурацией IP,которая должна быть обновлена. Третья команда задает личный IP-адрес основного IP-конфигурации ipconfig1 с 10.0.0.11. Наконец, последняя команда обновляет интерфейс сети, обеспечивая успешное внесение изменений.
    

### 2. Связывание конфигурации IP-адреса с группой безопасности приложения
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$asg = Get-ApplicationSecurityGroup -Name myasg -ResourceGroupName myrg

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet -ApplicationSecurityGroup $asg
    -Primary

$nic | Set-AzNetworkInterface
```

В этом примере переменная $asg содержит ссылку на группу безопасности приложения.
Четвертая команда получает сетевой интерфейс nic1, связанный с конфигурацией IP,которая должна быть обновлена. Этот Set-AzNetworkInterfaceIpConfig задает частный IP-адрес основного IP-адреса конфигурации ipconfig1 10.0.0.11 и создает связь с извлеченной группой безопасности приложения.
Наконец, последняя команда обновляет интерфейс сети, обеспечивая успешное внесение изменений.

## PARAMETERS

### -ApplicationGatewayBackendAddressPool
Набор ссылок на пул адресов backend шлюза приложений, к которому относится эта конфигурация IP-интерфейса.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ApplicationGatewayBackendAddressPoolId
Набор ссылок на пул адресов backend шлюза приложений, к которому относится эта конфигурация IP-интерфейса.

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ApplicationSecurityGroup
Набор ссылок на группы безопасности приложений, к которым относится эта конфигурация IP-интерфейса.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ApplicationSecurityGroupId
Набор ссылок на группы безопасности приложений, к которым относится эта конфигурация IP-интерфейса.

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -LoadBalancerBackendAddressPool
Набор ссылок на пул адресов для балансиров нагрузки, к которому относится эта конфигурация IP-интерфейса.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerBackendAddressPoolId
Набор ссылок на пул адресов для балансиров нагрузки, к которому относится эта конфигурация IP-интерфейса.

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerInboundNatRule
Набор ссылок на правила перевода сетевых адресов (NAT), к которым принадлежит эта конфигурация IP-интерфейса.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerInboundNatRuleId
Набор ссылок на входящие правила NAT для балансиров нагрузки, к которым относится эта конфигурация IP-интерфейса.

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Задает имя конфигурации IP-адреса сети, для которой задан этот cmdlet.

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

### -NetworkInterface
Определяет объект **NetworkInterface.**
Этот cmdlet добавляет конфигурацию IP-адреса сетевого интерфейса к объекту, указанному этим параметром.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Primary
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

### -PrivateIpAddress
Определяет статический IP-адрес конфигурации IP-интерфейса.

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

### -PrivateIpAddressVersion
Указывает версию IP-адреса конфигурации IP-интерфейса.
Допустимые значения этого параметра:
- IPv4
- IPv6

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIpAddress
Указывает объект **PublicIPAddress.**
Этот cmdlet создает ссылку на общедоступный IP-адрес, который связывается с этой конфигурацией IP-интерфейса сети.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIpAddressId
Этот cmdlet создает ссылку на общедоступный IP-адрес, который связывается с этой конфигурацией IP-интерфейса сети.

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Subnet
Указывает объект **подсети.**
Этот cmdlet создает ссылку на подсеть, в которой создается конфигурация IP-интерфейса.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetId
Этот cmdlet создает ссылку на подсеть, в которой создается конфигурация IP-интерфейса.

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.Network.Models.PSNetworkInterface

### System.String[]

### Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]

### Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]

### Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]

## OUTPUTS

### Microsoft.Azure.Commands.Network.Models.PSNetworkInterface

## ПРИМЕЧАНИЯ
* Ключевые слова: azure, azurerm, arm, resource, management, manager, network, networking

## СВЯЗАННЫЕ ССЫЛКИ

[Add-AzNetworkInterfaceIpConfig](./Add-AzNetworkInterfaceIpConfig.md)

[Get-AzNetworkInterfaceIpConfig](./Get-AzNetworkInterfaceIpConfig.md)

[New-AzNetworkInterfaceIpConfig](./New-AzNetworkInterfaceIpConfig.md)

[Remove-AzNetworkInterfaceIpConfig](./Remove-AzNetworkInterfaceIpConfig.md)
