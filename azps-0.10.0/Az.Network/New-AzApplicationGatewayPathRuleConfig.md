---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: b6722412717d0ef087c2540ff49d3d7a5b87913c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909757"
---
# New-AzApplicationGatewayPathRuleConfig

## КРАТКИй обзор
Создает правило пути для шлюза приложения.

## Максимальное

### SetByResourceId
```
New-AzApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
New-AzApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzApplicationGatewayPathRuleConfig** создает правило пути к шлюзу приложения.
Правила, созданные этим командлетом, можно добавить в коллекцию параметров конфигурации карты URL-пути, а затем назначить шлюзу.

Параметры конфигурации схемы пути используются в балансировке нагрузки для шлюза приложений.

## ИЛЛЮСТРИРУЮТ

### Пример 1
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSetting -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

Эти команды создают новое правило для пути к шлюзу приложения, а затем используют командлет **Add-AzApplicationGatewayUrlPathMapConfig** , чтобы назначить это правило для шлюза приложений.
Для этого первая команда создает ссылку на объект для шлюза ContosoApplicationGateway.
Эта ссылка на объект хранится в переменной с именем $Gateway.

Следующие две команды создают пул адресных ресурсов и объект параметров HTTP для внутренних баз данных. Эти объекты (хранящиеся в переменных $AddressPool и $HttpSettings) необходимы для создания объекта правила для пути.

Четвертая команда создает объект правила пути и хранится в переменной с именем $PathRuleConfig.

Пятая команда использует **Add-AzApplicationGatewayUrlPathMapConfig** , чтобы добавить параметры конфигурации и правило нового пути, содержащееся в этих параметрах, в ContosoApplicationGateway.

## ПАРАМЕТРЫ

### -BackendAddressPool
Задает ссылку на объект для коллекции параметров пула адресных данных, которые будут добавлены в параметры конфигурации правил для путей к шлюзу.
Вы можете создать ссылку на объект с помощью командлета New-AzApplicationGatewayBackendAddressPool и синтаксиса, как показано ниже.

`$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`

Предыдущая команда добавляет в пул адресов два IP-адреса (192.16.1.1 и 192.168.1.2).
Обратите внимание, что IP-адрес заключен в кавычки и отделен с помощью запятых.

Конечную переменную, $AddressPool, можно использовать в качестве значения параметра для параметра *DefaultBackendAddressPool* .

Пул серверных адресов представляет IP-адреса на внутренних серверах.
Эти IP-адреса должны либо принадлежать к подсети виртуальной сети, либо быть общедоступными IP-адресами.
Если вы используете этот параметр, нельзя использовать параметр *DefaultBackendAddressPoolId* в той же команде.

```yaml
Type: PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendAddressPoolId
Указывает идентификатор существующего пула серверных адресов, который можно добавить к параметрам конфигурации правила для пути шлюза.
Идентификаторы пула адресов можно вернуть с помощью командлета Get-AzApplicationGatewayBackendAddressPool.
После появления идентификатора вы можете использовать параметр *DefaultBackendAddressPoolId* вместо параметра *DefaultBackendAddressPool* .
Например:

-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool"

Пул серверных адресов представляет IP-адреса на внутренних серверах.
Эти IP-адреса должны либо принадлежать к подсети виртуальной сети, либо быть общедоступными IP-адресами.

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

### -BackendHttpSettings
Указывает ссылку на объект на коллекцию параметров внутренних HTTP-данных, которые должны быть добавлены в параметры конфигурации правила для пути к шлюзу.
Вы можете создать ссылку на объект с помощью командлета New-AzApplicationGatewayBackendHttpSetting и синтаксиса, как показано ниже.

$HttpSettings = New-AzApplicationGatewayBackendHttpSetting-Name "ContosoHttpSetings"-Port 80-Protocol "http"-CookieBasedAffinity "Disabled"

Конечную переменную, $HttpSettings, можно использовать в качестве значения параметра для параметра *DefaultBackendAddressPool* :

-DefaultBackendHttpSettings $HttpSettings

Внутренние параметры HTTP настраивают такие свойства, как порт, протокол и сходство на основе файлов cookie для пула баз данных.
Если вы используете этот параметр, нельзя использовать параметр *DefaultBackendHttpSettingsId* в той же команде.

```yaml
Type: PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendHttpSettingsId
Указывает идентификатор существующей коллекции параметров HTTP-сервера, которую можно добавить в параметры конфигурации правила для пути шлюза.
Идентификаторы параметра HTTP можно вернуть с помощью командлета Get-AzApplicationGatewayBackendHttpSetting.
После появления идентификатора вы можете использовать параметр *DefaultBackendHttpSettingsId* вместо параметра *DefaultBackendHttpSettings* .
Например:

-DefaultBackendSettings ID "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings"

Внутренние параметры HTTP настраивают такие свойства, как порт, протокол и сходство на основе файлов cookie для пула баз данных.
Если вы используете этот параметр, нельзя использовать параметр *DefaultBackendHttpSettings* в той же команде.

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

### -Name (имя)
Указывает имя конфигурации правила для пути, создаваемой этим командлетом.

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

### -Paths
Задает один или несколько правил пути к шлюзу приложения.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RedirectConfiguration
RedirectConfiguration шлюза приложений

```yaml
Type: PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RedirectConfigurationId
Идентификатор RedirectConfiguration шлюза приложения

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

###  
**New-AzApplicationGatewayPathRuleConfig** не поддерживает конвейерные входные данные.

## НАПРЯЖЕНИЕ

###  
**New-AzApplicationGatewayPathRuleConfig** создает новые экземпляры объекта **Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayPathRule** .

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Add-AzApplicationGatewayUrlPathMapConfig](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[Get-AzApplicationGateway](./Get-AzApplicationGateway.md)

[Get-AzApplicationGatewayUrlPathMapConfig](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[New-AzApplicationGatewayBackendAddressPool](./New-AzApplicationGatewayBackendAddressPool.md)

[New-AzApplicationGatewayBackendHttpSetting](./New-AzApplicationGatewayBackendHttpSetting.md)

[New-AzApplicationGatewayPathRuleConfig](./New-AzApplicationGatewayPathRuleConfig.md)

[New-AzApplicationGatewayUrlPathMapConfig](./New-AzApplicationGatewayUrlPathMapConfig.md)

[Remove-AzApplicationGatewayUrlPathMapConfig](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[Set-AzApplicationGatewayUrlPathMapConfig](./Set-AzApplicationGatewayUrlPathMapConfig.md)


