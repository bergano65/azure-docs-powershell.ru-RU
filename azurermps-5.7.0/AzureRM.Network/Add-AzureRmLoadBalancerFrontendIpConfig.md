---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 07FF274A-F365-44E5-A66B-6740CD165664
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: b64e24bb816ce7d01b99c0dbaa808ecdac99a082
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566611"
---
# Add-AzureRmLoadBalancerFrontendIpConfig

## КРАТКИй обзор
Добавление интерфейсной конфигурации IP в подсистему балансировки нагрузки.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### SetByResourceSubnet
```
Add-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -Subnet <PSSubnet> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceIdSubnet
```
Add-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -SubnetId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceIdPublicIpAddress
```
Add-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddressId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourcePublicIpAddress
```
Add-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddress <PSPublicIpAddress> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Add-AzureRmLoadBalancerFrontendIpConifg** добавляет IP-конфигурацию переднего плана в подсистему балансировки нагрузки Azure.

## ИЛЛЮСТРИРУЮТ

### Пример 1. Добавление интерфейсной конфигурации IP с динамическим IP-адресом
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyRg" | Get-AzureRmVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet | Set-AzureRmLoadBalancer
```

Первая команда получает виртуальную сеть Azure с именем MyVnet и передает результат с помощью конвейера в командлет **Get-AzureRmVirtualNetworkSubnetConfig** , чтобы получить подсеть с именем MySubnet.
Затем команда сохраняет результат в переменной с именем $Subnet.
Вторая команда получает подсистему балансировки нагрузки с именем MyLB и передает результат в командлет **Add-AzureRmLoadBalancerFrontendIpConfig** , который добавляет интерфейсную конфигурацию IP в подсистему балансировки нагрузки с динамическим частным IP-адресом из подсети, хранящейся в переменной с именем $MySubnet.

### Пример 2. Добавление интерфейсной конфигурации IP со статическим IP-адресом
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "RG001" | Get-AzureRmVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet -PrivateIpAddress "10.0.1.6" | Set-AzureRmLoadBalancer
```

Первая команда получает виртуальную сеть Azure с именем MyVnet и передает результат с помощью конвейера в командлет **Get-AzureRmVirtualNetworkSubnetConfig** , чтобы получить подсеть с именем MySubnet.
Затем команда сохраняет результат в переменной с именем $Subnet.
Вторая команда получает подсистему балансировки нагрузки с именем MyLB и передает результат в командлет **Add-AzureRmLoadBalancerFrontendIpConfig** , который добавляет интерфейсную конфигурацию IP в подсистему балансировки нагрузки со статическим частным IP-адресом из подсети, хранящейся в переменной с именем $Subnet.

### Пример 3. Добавление интерфейсной конфигурации IP с помощью общедоступного IP-адреса
```
PS C:\>$PublicIp = Get-AzureRmPublicIpAddress -ResourceGroupName "myRG" -Name "MyPub"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddress $PublicIp | Set-AzureRmLoadBalancer
```

Первая команда получает общедоступный IP-адрес Azure с именем MyPub и сохраняет результат в переменной с именем $PublicIp.
Вторая команда получает подсистему балансировки нагрузки с именем MyLB и передает результат в командлет **Add-AzureRmLoadBalancerFrontendIpConfig** , который добавляет интерфейсную конфигурацию IP в подсистему балансировки нагрузки с общедоступным IP-адресом, хранящимся в переменной с именем $PublicIp.

## ПАРАМЕТРЫ

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

### -Подсистема балансировки
Указывает объект подсистемы **балансировки нагрузки** .
Этот командлет добавляет IP-конфигурацию переднего плана в подсистему балансировки нагрузки, указанную в этом параметре.

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (имя)
Указывает имя добавляемой интерфейсной конфигурации IP-адресов.

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

### -PrivateIpAddress
Задает частный IP-адрес, который нужно связать с интерфейсной конфигурацией IP.

```yaml
Type: String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIpAddress
Указывает общедоступный IP-адрес для связи с интерфейсной конфигурацией IP-интерфейса.

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIpAddressId
Specifes. идентификатор общедоступного IP-адреса, в который добавляется интерфейсная конфигурация IP-интерфейса.

```yaml
Type: String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Подсеть
Указывает объект подсети, в который нужно добавить интерфейсную конфигурацию IP-адресов.

```yaml
Type: PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetId
Указывает идентификатор подсети, в который нужно добавить интерфейсную конфигурацию IP-адресов.

```yaml
Type: String
Parameter Sets: SetByResourceIdSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Zone
Список зон доступности, обозначающих IP-адрес, выделенный для ресурса, должен быть от него.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### PSLoadBalancer
Параметр "подсистема" "подсистемы" принимает значение типа "PSLoadBalancer" из конвейера.

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Network. Models. PSLoadBalancer

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmLoadBalancerFrontendIpConfig](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)

[Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[New-AzureRmLoadBalancerFrontendIpConfig](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[Remove-AzureRmLoadBalancerFrontendIpConfig](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[Set-AzureRmLoadBalancerFrontendIpConfig](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


