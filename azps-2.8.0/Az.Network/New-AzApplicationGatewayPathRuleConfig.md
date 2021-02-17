---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: 6592f79291c069ade40b30277461f5e0e218b937
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100407052"
---
# New-AzApplicationGatewayPathRuleConfig

## SYNOPSIS
Создает правило пути шлюза приложения.

## СИНТАКСИС

### SetByResourceId
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
Для создания правила пути шлюза приложения создается **cmdlet New-AzApplicationGatewayPathRuleConfig.**
Правила, созданные этим cmdlet, можно добавить в коллекцию параметров конфигурации карты URL-адреса, а затем на назначенную шлюзу.
Параметры конфигурации карты пути используются для балансировки нагрузки шлюза приложения.

## ПРИМЕРЫ

### Пример 1
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

Эти команды создают новое правило пути шлюза приложения, а затем назначьте его шлюзу приложения с помощью командлета **Add-AzApplicationGatewayUrlPathConfig.**
Для этого первая команда создает ссылку на шлюз ContosoApplicationGateway.
Эта ссылка на объект хранится в переменной с именем $Gateway.
Следующие две команды создают пул адресов для дополнительных адресов и объект параметров HTTP. Эти объекты (которые хранятся в переменных $AddressPool и $HttpSettings) необходимы для создания объекта правила пути.
Четвертая команда создает объект правила пути и сохраняется в переменной с $PathRuleConfig.
Пятая команда использует **Add-AzApplicationGatewayUrlPathMapConfig** для добавления параметров конфигурации и нового правила пути, содержаногося в этих параметрах, в ContosoApplicationGateway.

## PARAMETERS

### -BackendAddressPool
Указывает ссылку на коллекцию параметров пула адресов для дополнительных адресов, которые будут добавлены в параметры конфигурации правил путей шлюза.
Эту ссылку на объект можно создать с помощью New-AzApplicationGatewayBackendAddressPool и синтаксиса, аналогичных этой: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`
При предыдущей команде в пул адресов добавляется два IP-адреса (192.16.1.1 и 192.168.1.2).
Обратите внимание, что IP-адрес заключен в кавычках и разделен запятой.
Итоговую переменную ($AddressPool) можно использовать в качестве значения параметра для параметра *DefaultBackendAddressPool.*
Пул серверных адресов представляет IP-адреса серверов.
Эти IP-адреса должны принадлежать виртуальной подсети сети или должны быть общедоступными IP-адресами.
Этот параметр нельзя использовать в одной команде с параметром *DefaultBackendAddressPoolId.*

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendAddressPoolId
Определяет ИД существующего пула адресов для дополнительных адресов, который можно добавить в параметры конфигурации пути шлюза.
Коды пула адресов можно вернуть с помощью Get-AzApplicationGatewayBackendAddressPool-адресов.
После этого можно использовать параметр *DefaultBackendAddressPoolId* вместо параметра *DefaultBackendAddressPool.*
Например: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups /appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" Пул адресов серверов представляет IP-адреса серверов.
Эти IP-адреса должны принадлежать виртуальной подсети сети или должны быть общедоступными IP-адресами.

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

### -BackendHttpSettings
Указывает ссылку на коллекцию дополнительных параметров HTTP, которые будут добавлены в параметры конфигурации пути шлюза.
Эту ссылку на объект можно создать с помощью New-AzApplicationGatewayBackendHttpSettings и синтаксиса $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" The resulting variable, $HttpSettings, затем можно использовать параметр DefaultBackendAddressPool в качестве значения параметра *DefaultBackendAddressPool:* -DefaultBackendHttpSettings $HttpSettings Параметры HTTP-файлов настраивают свойства, такие как порт, протокол и на основе cookie, для пула backend.
Если вы используете этот параметр, нельзя использовать параметр *DefaultBackendHttpSettingsId* в одной команде.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendHttpSettingsId
Определяет ИД существующего коллекции параметров HTTP-адреса, который можно добавить в параметры конфигурации пути шлюза.
Коды параметров HTTP можно вернуть с помощью Get-AzApplicationGatewayBackendHttpSettings..
После этого можно использовать параметр *DefaultBackendHttpSettingsId* вместо *параметра DefaultBackendHttpSettings.*
Например: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" The backend HTTP settings configure properties such as port, protocol, и бесконечность на основе файлов cookie для пула backend.
Если вы используете этот параметр, нельзя использовать параметр *DefaultBackendHttpSettings в* одной команде.

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

### -Name
Указывает имя конфигурации правила пути, которую создает этот cmdlet.

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

### -Paths
Определяет одно или несколько правил пути шлюза приложения.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RedirectConfiguration
RedirectConfiguration шлюза приложения

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RedirectConfigurationId
ID of the application gateway RedirectConfiguration

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

### -RewriteRuleSet
RewriteRuleSet шлюза приложения

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RewriteRuleSetId
ИД шлюза приложения RewriteRuleSet

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
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Нет

## OUTPUTS

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Add-AzApplicationGatewayUrlPathMapConfig](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[Get-AzApplicationGateway](./Get-AzApplicationGateway.md)

[Get-AzApplicationGatewayUrlPathMapConfig](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[New-AzApplicationGatewayBackendAddressPool](./New-AzApplicationGatewayBackendAddressPool.md)


[New-AzApplicationGatewayPathRuleConfig](./New-AzApplicationGatewayPathRuleConfig.md)

[New-AzApplicationGatewayUrlPathMapConfig](./New-AzApplicationGatewayUrlPathMapConfig.md)

[Remove-AzApplicationGatewayUrlPathMapConfig](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[Set-AzApplicationGatewayUrlPathMapConfig](./Set-AzApplicationGatewayUrlPathMapConfig.md)


