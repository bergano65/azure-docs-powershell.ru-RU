---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: aeb41c41ad7476f88da7dfa29b3fef2912e28a8e
ms.sourcegitcommit: 6f0b6059d096600ebff1c8514c35c467d2f482d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/20/2021
ms.locfileid: "104717532"
---
# Remove-AzApplicationGatewayClientAuthConfiguration

## SYNOPSIS
Удаляет конфигурацию проверки подлинности клиента для объекта профиля SSL.

## СИНТАКСИС

```
Remove-AzApplicationGatewayClientAuthConfiguration -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
**Cmdlet Remove-AzApplicationGateWayClientAuthConfiguration** удаляет конфигурацию проверки подлинности клиента для объекта профиля SSL.

## ПРИМЕРЫ

### Пример 1
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "Profile01" -ApplicationGateway $AppGw
PS C:\> Remove-AzApplicationGatewayClientAuthConfiguration -SslProfile $profile
```

Первая команда получает шлюз приложения ApplicationGateway01 в группе ресурсов ResourceGroup01 и сохраняет его в $AppGw переменной. Вторая команда получает профиль SSL profile01 для $AppGw и сохраняет его в переменной $profile. Последняя команда удаляет конфигурацию проверки подлинности клиента для SSL-профиля, храняшегося в $profile.

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

### -SslProfile
Профиль SSL

```yaml
Type: PSApplicationGatewaySslProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile

## OUTPUTS

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[New-AzApplicationGatewayClientAuthConfiguration](./New-AzApplicationGatewayClientAuthConfiguration.md)

[Get-AzApplicationGatewayClientAuthConfiguration](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[Set-AzApplicationGatewayClientAuthConfiguration](./Set-AzApplicationGatewayClientAuthConfiguration.md)