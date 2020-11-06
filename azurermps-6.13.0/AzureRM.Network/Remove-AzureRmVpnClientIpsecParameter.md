---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientIpsecParameter.md
ms.openlocfilehash: b88fff9775665f5b20f403d46f11bba89dc61220
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562799"
---
# Remove-AzureRmVpnClientIpsecParameter

## КРАТКИй обзор
Удаление настраиваемой политики IPSec VPN, установленной на ресурсе шлюза виртуальной сети.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### ByFactoryName (по умолчанию)
```
Remove-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByFactoryObject
```
Remove-AzureRmVpnClientIpsecParameter -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByResourceId
```
Remove-AzureRmVpnClientIpsecParameter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Шлюз виртуальной сети — это объект, представляющий ваш шлюз в Azure.
Командлет **Remove-AzureRmVpnClientIpsecParameter** удаляет особые параметры IPsec VPN, заданные в шлюзе виртуальной сети, который в свою очередь задает политику IPSec по умолчанию для VPN-шлюза на основе имени VirtualNetworkGateway и имени группы ресурсов.

## ИЛЛЮСТРИРУЮТ

### 1: удаление параметров VPN-IPSec, заданных для шлюза виртуальной сети.
```
PS C:\> $delete = Remove-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName myGateway -ResourceGroupName myRG
```

Удаляет особые параметры IPsec VPN, заданные в шлюзе виртуальной сети, с именем "myGateway" в группе ресурсов "myRG". Эта команда возвращает логический объект, который отображается, если удаление прошло успешно или завершилось сбоем.
Примечание. в результате будет задана политика IPSec по умолчанию для шлюза виртуальной сети.

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
Parameter Sets: ByFactoryName
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
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway
Параметры: InputObject (ByValue)

### System. String

## НАПРЯЖЕНИЕ

### System. Boolean

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
