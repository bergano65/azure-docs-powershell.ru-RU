---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVpnClientIpsecParameter.md
ms.openlocfilehash: 38dcfdb1188a810b0f154dfed31f8a1ef3206247
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565848"
---
# Set-AzureRmVpnClientIpsecParameter

## КРАТКИй обзор
Задает параметры IPsec VPN для существующего шлюза виртуальной сети.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### ByFactoryName (по умолчанию)
```
Set-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByFactoryObject
```
Set-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByResourceId
```
Set-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzureRmVpnClientIpsecParameter** задает параметры IPsec VPN для существующего шлюза виртуальной сети.
После создания шлюза виртуальной сети он задает набор политик IPSec по умолчанию для шлюза VPN. В случае наведите указатель мыши на сайт, чтобы использовать определенную политику IPSec для подключения к шлюзу VPN, пользователь должен сначала настроить политику IPSec в VPN-шлюзе. **Set-AzureRmVpnClientIpsecParameter** обеспечивает эти возможности.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Установка настраиваемой политики IPSec VPN для существующего шлюза виртуальной сети.
```powershell
PS C:\>$vpnclientipsecparams = New-AzureRmVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName "ContosoLocalGateway" -ResourceGroupName "ContosoResourceGroup" -VpnClientIPsecParameter $vpnclientipsecparams
```

В этом примере в качестве настраиваемой политики IPSec для VPN указан IP-адрес существующего виртуального сетевого шлюза с именем ContosoVirtualGateway из группы ресурсов ContosoResourceGroup.
New-AzureRmVpnClientIpsecParameter, который используется для создания объекта параметров VPN-IPSec с использованием переданных значений одного или всех параметров, которые пользователь может настроить для любого из существующих шлюзов виртуальной сети в ResourceGroup.
Созданный объект VpnClientIPsecParameters передается Set-AzureRmVpnClientIpsecParameter команде для настройки указанной настраиваемой политики IPSec VPN на виртуальном сетевом шлюзе, как показано в примере выше. Эта команда возвращает объект VpnClientIPsecParameters, который показывает наборы параметров.

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

### -InputObject
Объект Gateaway виртуальной сети

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов.

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

### -ResourceId
Идентификатор ресурса Azure.

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGatewayName
Имя шлюза виртуальной сети.

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

### -VpnClientIPsecParameter
Параметры IPsec VPN-клиента. Это значение параметра может быть создано с помощью команды PS Let: New-AzureRmVpnClientIpsecParameter

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Confirm
Запрашивает подтверждение перед запуском командлета.

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
Показывает, что произойдет при запуске командлета.
Командлет не выполняется.

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Microsoft. Azure. Commands. Network. Models. PSVpnClientIPsecParameters
Параметры: VpnClientIPsecParameter (ByValue)

### Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway
Параметры: InputObject (ByValue)

### System. String

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Network. Models. PSVpnClientIPsecParameters

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[New-AzureRmVpnClientIpsecParameters](./New-AzureRmVpnClientIpsecParameters.md)
