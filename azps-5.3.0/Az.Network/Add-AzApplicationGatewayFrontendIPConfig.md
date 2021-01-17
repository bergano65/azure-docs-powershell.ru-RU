---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0ECE4232-EA5D-46A0-8260-69646E27FA9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: dadb58348305434294a9a435a136733f0b6ef1e1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422404"
---
# Add-AzApplicationGatewayFrontendIPConfig

## SYNOPSIS
Добавляет конфигурацию переднего IP-адреса к шлюзу приложения.

## СИНТАКСИС

### SetByResourceId
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-PrivateLinkConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
Для шлюза приложения добавляется конфигурация переднего IP-адреса **Add-AzApplicationGatewayFrontendIPConfig.**
Шлюз приложения поддерживает два типа конфигураций переднего IP-адреса: 
- Общедоступные IP-адреса
- Частные IP-адреса с использованием внутренней балансировки нагрузки (ILB) Шлюз приложения может иметь как минимум один общедоступный IP-адрес и один частный IP-адрес.
Добавьте общедоступный и частный IP-адреса в качестве отдельных ip-адресов переднего ip-адреса.

## ПРИМЕРЫ

### Пример 1. Добавление общего IP-адреса в качестве ip-адреса переднего
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

Первая команда создает общедоступный IP-адрес и сохраняет его в переменной $PublicIp.
Вторая команда получает шлюз приложения ApplicationGateway01, который принадлежит к группе ресурсов ResourceGroup01, и сохраняет его в переменной $AppGw Ресурса.
Третья команда добавляет у шлюза в $AppGw ip-адрес переднего $AppGw, используя адрес, $PublicIp.

### Пример 2. Добавление статического закрытого IP-адреса в качестве ip-адреса переднего
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

Первая команда получает виртуальную сеть VNet01, которая принадлежит группе ресурсов ResourceGroup01, и сохраняет ее в переменной $VNet ресурса.
Вторая команда получает конфигурацию подсети "Подсеть" с $VNet из первой команды и сохраняет ее в $Subnet переменной.
Третья команда получает шлюз приложения ApplicationGateway01, который принадлежит к группе ресурсов ResourceGroup01, и сохраняет его в переменной $AppGw ресурса.
Четвертая команда добавляет конфигурацию переднего IP-адреса FrontendIP02 с использованием $Subnet из второй команды и личного IP-адреса 10.0.1.1.

### Пример 3. Добавление динамического закрытого IP-адреса в качестве IP-адреса переднего
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

Первая команда получает виртуальную сеть VNet01, которая принадлежит группе ресурсов ResourceGroup01, и сохраняет ее в переменной $VNet ресурса.
Вторая команда получает конфигурацию подсети "Подсеть" с $VNet из первой команды и сохраняет ее в $Subnet переменной.
Третья команда получает шлюз приложения ApplicationGateway01, который принадлежит к группе ресурсов ResourceGroup01, и сохраняет его в переменной $AppGw ресурса.
Четвертая команда добавляет переднюю конфигурацию IP-адреса FrontendIP02 с $Subnet из второй команды.

## PARAMETERS

### -ApplicationGateway
Указывает шлюз приложения, к которому этот cmdlet добавляет конфигурацию переднего IP-адреса.

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Имя ip-конфигурации переднего ip-адреса, который нужно добавить.

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

### -PrivateIPAddress
Указывает частный IP-адрес, который нужно добавить в качестве переднего IP-адреса шлюза приложения.
Если задан этот IP-адрес, он статически выделяется из подсети.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateLinkConfiguration
PrivateLinkConfiguration

```yaml
Type: PSApplicationGatewayPrivateLinkConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateLinkConfigurationId
PrivateLinkConfigurationId

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIPAddress
Указывает общедоступный IP-адрес, который этот cmdlet добавляет в качестве переднего IP-адреса шлюза приложения.

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIPAddressId
Определяет код общего IP-адреса, который этот cmdlet добавляет в качестве переднего IP-адреса шлюза приложения.

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Subnet
Указывает подсеть, которую этот cmdlet добавляет в качестве конфигурации переднего IP-адреса.
Если этот параметр указан, предполагается, что шлюз приложения поддерживает конфигурацию на основе частных IP-адресов.
Если указан *параметр PrivateIPAddress,* он должен принадлежать этой подсети.
Если *адрес PrivateIPAddress* не указан, один из IP-адресов этой подсети динамически выбирается в качестве переднего IP-адреса шлюза приложения.

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetId
Определяет код подсети, который этот cmdlet добавляет в качестве конфигурации переднего IP-адреса.
Передача подсети подразумевает частный IP-адрес.
Если указан *параметр PrivateIPAddress,* он должен принадлежать этой подсети.
В противном случае один из IP-адресов из этой подсети динамически выбирается в качестве переднего IP-адреса шлюза приложения.

```yaml
Type: String
Parameter Sets: SetByResourceId
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

### Microsoft.Azure.Commands.Network.Models.PSApplicationGateway

## OUTPUTS

### Microsoft.Azure.Commands.Network.Models.PSApplicationGateway

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzApplicationGatewayFrontendIPConfig](./Get-AzApplicationGatewayFrontendIPConfig.md)

[New-AzApplicationGatewayFrontendIPConfig](./New-AzApplicationGatewayFrontendIPConfig.md)

[Remove-AzApplicationGatewayFrontendIPConfig](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[Set-AzApplicationGatewayFrontendIPConfig](./Set-AzApplicationGatewayFrontendIPConfig.md)


