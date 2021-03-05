---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: https://docs.microsoft.com/powershell/module/az.network/set-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 2c32263d52f8e260c67395484b2a9a2e3e479ecb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973651"
---
# Set-AzVirtualNetworkGatewayConnectionSharedKey

## SYNOPSIS
Настраивает общий ключ подключения виртуального сетевого шлюза.

## СИНТАКСИС

```
Set-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## ОПИСАНИЕ
Командлет **Set-AzVirtualNetworkGatewayConnectionSharedKey** настраивает общий ключ подключения виртуального сетевого шлюза.

## ПРИМЕРЫ

### Пример 1
```powershell
PS C:\Users\alzam> Set-AzVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName VPNGatewayV3 -Name VNet1toVNet2 -Value abcd1234

Confirm
Are you sure you want to overwrite resource 'VNet1toVNet2'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
abcd1234
```

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

### -Force
Запуск команды без запроса подтверждения.

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

### -Name
Указывает имя общего ключа виртуального сетевого шлюза.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов, к которой принадлежит виртуальный сетевой шлюз.

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

### -Значение
Указывает значение общего ключа.

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

### -Confirm
Запрос на подтверждение перед запуском cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

## OUTPUTS

### System.String

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzVirtualNetworkGatewayConnectionSharedKey](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[Reset-AzVirtualNetworkGatewayConnectionSharedKey](./Reset-AzVirtualNetworkGatewayConnectionSharedKey.md)
