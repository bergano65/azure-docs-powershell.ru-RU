---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AE8E26F2-CF8E-4340-936D-230731B5BA32
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 214f408a5120982a903ed0d0d934c44073c32df8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986765"
---
# New-AzApplicationGatewayFrontendIPConfig

## SYNOPSIS
Создает конфигурацию ip-адреса переднего ip-адреса для шлюза приложения.

## СИНТАКСИС

### SetByResourceId
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-SubnetId <String>]
 [-PublicIPAddressId <String>] [-PrivateLinkConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
Для шлюза приложения Azure создается клиентский IP-адрес конфигурации **New-AzApplicationGatewayFrontendIPConfig.**
Шлюз приложения поддерживает два типа настройки переднего IP-адреса: 
- Общедоступные IP-адреса: частные IP-адреса с использованием внутренней балансировки нагрузки (ILB).
 Шлюз приложения может иметь как минимум один общедоступный и один частный IP-адрес.
Общедоступный и частный IP-адреса следует добавлять отдельно в качестве IP-адресов переднего.

## ПРИМЕРЫ

### Пример 1. Создание передней конфигурации IP-адреса с использованием объекта общедоступных IP-ресурсов
```
PS C:\>$PublicIP = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIP01" -location "West US" -AllocationMethod Dynamic
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -PublicIPAddress $PublicIP
```

Первая команда создает объект общедоступных IP-ресурсов и сохраняет его в переменной $PublicIP.
Вторая команда использует $PublicIP, чтобы создать новую конфигурацию переднего IP-адреса с именем FrontEndIP01 и $FrontEnd переменной.

### Пример 2. Создание статического закрытого IP-адреса в качестве переднего IP-адреса
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

Первая команда получает виртуальную сеть VNet01, которая принадлежит группе ресурсов ResourceGroup01, и сохраняет ее в переменной $VNet ресурса.
Вторая команда получает конфигурацию подсети "Подсеть" с $VNet из первой команды и сохраняет ее в $Subnet переменной.
Третья команда создает конфигурацию переднего IP-адреса с именем FrontEndIP02, используя $Subnet из второй команды и личный IP-адрес 10.0.1.1, а затем сохраняет его в переменной $FrontEnd.

### Пример 3. Создание динамического закрытого IP-адреса в качестве переднего IP-адреса
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP03" -Subnet $Subnet
```

Первая команда получает виртуальную сеть VNet01, которая принадлежит группе ресурсов ResourceGroup01, и сохраняет ее в переменной $VNet ресурса.
Вторая команда получает конфигурацию подсети "Подсеть" с $VNet из первой команды и сохраняет ее в $Subnet переменной.
Третья команда создает конфигурацию переднего IP-адреса с именем FrontEndIP03 $Subnet из второй команды и сохраняет ее в переменной $FrontEnd.

## PARAMETERS

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
Указывает имя ip-конфигурации переднего ip-адреса, которую создает этот cmdlet.

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
Указывает частный IP-адрес, который этот cmdlet связывает с IP-адресом переднего ip-адреса шлюза приложения.
Это можно сделать только в том случае, если указана подсеть.
Этот IP-адрес статически выделен из подсети.

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
Указывает общедоступный IP-адрес, который этот cmdlet связывает с IP-адресом переднего IP-адреса шлюза приложения.

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
Указывает общедоступный IP-адрес, который этот cmdlet связывает с ip-адресом переднего ip-адреса шлюза приложения.

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
Определяет объект подсети, который этот cmdlet связывает с IP-адресом переднего ip-адреса шлюза приложения.
Если этот параметр указан, предполагается, что шлюз использует частный IP-адрес.
Если *задан параметр PrivateIPAddress,* он должен принадлежать к подсети, заданной этим параметром.
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
Определяет код подсети, который этот cmdlet связывает с ip-конфигурацией шлюза приложения.
Если указать параметр *"Подсеть",* это означает, что шлюз использует частный IP-адрес.
Если *задан параметр PrivateIPAddress,* он должен принадлежать подсети, указанной *подсетей.*
Если *адрес PrivateIPAddress* не указан, один из IP-адресов этой подсети динамически выбирается в качестве переднего IP-адреса шлюза приложения.

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

### Нет

## OUTPUTS

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Add-AzApplicationGatewayFrontendIPConfig](./Add-AzApplicationGatewayFrontendIPConfig.md)

[Get-AzApplicationGatewayFrontendIPConfig](./Get-AzApplicationGatewayFrontendIPConfig.md)

[Remove-AzApplicationGatewayFrontendIPConfig](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[Set-AzApplicationGatewayFrontendIPConfig](./Set-AzApplicationGatewayFrontendIPConfig.md)


