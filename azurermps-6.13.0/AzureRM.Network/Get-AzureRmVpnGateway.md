---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnGateway.md
ms.openlocfilehash: f1e7b829856558f438793a921154aa3f04666ff8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562908"
---
# Get-AzureRmVpnGateway

## КРАТКИй обзор
Получает ресурс VpnGateway с помощью ResourceGroupName и GatewayName или перечисляет все шлюзы с помощью ResourceGroupName или SubscriptionId.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### ListBySubscriptionId (по умолчанию)
```
Get-AzureRmVpnGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ListByResourceGroupName
```
Get-AzureRmVpnGateway -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Получает ресурс VpnGateway с помощью ResourceGroupName и GatewayName или перечисляет все шлюзы с помощью ResourceGroupName или SubscriptionId.

## ИЛЛЮСТРИРУЮТ

### Пример 1

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

В приведенном выше примере создается группа ресурсов, Виртуальная глобальная сеть, Виртуальная сетевая служба, виртуальный концентратор — Запад US в группе ресурсов "testRG" в Azure. Шлюз VPN будет создан на виртуальном концентраторе с двумя единицами масштабирования.

Затем он получает VpnGateway, используя его resourceGroupName и имя шлюза.

## ПАРАМЕТРЫ

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

### -Name (имя)
Название ресурса.

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VpnGatewayName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов.

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Network. Models. PSVpnGateway

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
