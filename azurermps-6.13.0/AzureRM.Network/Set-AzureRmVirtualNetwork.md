---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
ms.openlocfilehash: 2a81b7bf5420bdbf4fa5252d71c511c7152e47fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562779"
---
# Set-AzureRmVirtualNetwork

## КРАТКИй обзор
Задает состояние цели для виртуальной сети.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Set-AzureRmVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzureRmVirtualNetwork** задает состояние цели для виртуальной сети Azure.

## ИЛЛЮСТРИРУЮТ

### 1: создание виртуальной сети и удаление одной из ее подсетей.
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" ## Create resource group
$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24" ## Create backend subnet

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet ## Create virtual network

Remove-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork ## Remove subnet from in memory representation of virtual network

$virtualNetwork | Set-AzureRmVirtualNetwork ## Remove subnet from virtual network
```

В этом примере создается виртуальная сеть под названием TestResourceGroup с двумя подсетями: frontendSubnet и backendSubnet. После этого она удаляет подсеть backendSubnet из представления виртуальной сети в памяти. Затем командлет Set-AzureRmVirtualNetwork используется для записи измененного состояния виртуальной сети на стороне службы. При выполнении командлета Set-AzureRmVirtualNetwork удаляется backendSubnet.

## ПАРАМЕТРЫ

### -AsJob
Выполнить командлет в фоновом режиме

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualNetwork
Указывает объект **VirtualNetwork** , который представляет состояние цели.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork
Параметры: VirtualNetwork (ByValue)

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)

[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)

[New-AzureRmVirtualNetwork](./New-AzureRmVirtualNetwork.md)

[Remove-AzureRmVirtualNetwork](./Remove-AzureRmVirtualNetwork.md)


