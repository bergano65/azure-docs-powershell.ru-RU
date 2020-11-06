---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorroutingruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorRoutingRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorRoutingRuleObject.md
ms.openlocfilehash: c03a76943857e3615269a9584a3975ae6ab86666
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566453"
---
# New-AzureRmFrontDoorRoutingRuleObject

## КРАТКИй обзор
Создание PSRoutingRuleObject для создания передней дверцы

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
New-AzureRmFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> -BackendPoolName <String> [-AcceptedProtocol <PSProtocol[]>]
 [-PatternToMatch <String[]>] [-CustomForwardingPath <String>] [-ForwardingProtocol <PSForwardingProtocol>]
 [-EnableCaching <Boolean>] [-QueryParameterStripDirective <PSQueryParameterStripDirective>]
 [-DynamicCompression <PSEnabledState>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Создание PSRoutingRuleObject для создания передней дверцы

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание PSRoutingRuleObject для создания передней дверцы
```powershell
PS C:\> New-AzureRmFrontDoorRoutingRuleObject -Name $routingRuleName -FrontDoorName $frontDoorName -ResourceGroupName  -FrontendEndpointName "frontendEndpoint1" -BackendPoolName "backendPool1" 

FrontendEndpointIds          : {/subscriptions/{subid}/resourceGroups/{rgname}/pro
                               viders/Microsoft.Network/frontDoors/{frontdoorname}/FrontendEndpoints/frontendEndpoint1}
AcceptedProtocols            : {Http, Https}
PatternsToMatch              : {/*}
ForwardingProtocol           : MatchRequest
CustomForwardingPath         :
QueryParameterStripDirective : StripAll
DynamicCompression           : Enabled
HealthProbeSettings          :
BackendPoolId                : /subscriptions/{subid}/resourceGroups/{rgname}/prov
                               iders/Microsoft.Network/frontDoors/{frontdoorname}/BackendPools/backendPool1
EnableCaching                : Disabled
EnabledState                 : Enabled
ResourceState                :
Id                           :
Name                         : routingrule1
Type                         :
```

Создание PSRoutingRuleObject для создания передней дверцы

## ПАРАМЕТРЫ

### -AcceptedProtocol
Схемы протоколов для сопоставления с этим правилом.
Значение по умолчанию: {HTTPS, http}

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSProtocol[]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendPoolName
Идентификатор ресурса для BackendPool, к которому это правило адресуется

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

### -CustomForwardingPath
Настраиваемый путь, используемый для перезаписи путей к ресурсам, подходящих для этого правила.
Оставьте поле пустым, чтобы использовать входящий путь.

```yaml
Type: System.String
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

### -DynamicCompression
Следует ли включить динамическое сжатие для кэшированного содержимого, если включено кэширование.
Значение по умолчанию — Enabled

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableCaching
Следует ли включить кэширование для этого маршрута. Значение по умолчанию: ложь

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnabledState
Следует ли включить использование этого правила.
Значение по умолчанию — Enabled

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForwardingProtocol
Протокол, который будет использоваться этим правилом при пересылке трафика по умолчанию, имеет значение MatchRequest.

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingProtocol
Parameter Sets: (All)
Aliases:
Accepted values: HttpOnly, HttpsOnly, MatchRequest

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FrontDoorName
Имя передней дверцы, к которой относится данное правило маршрутизации.

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

### -FrontendEndpointName
Имена конечных точек с интерфейсом, связанных с этим правилом

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

### -Name (имя)
RoutingRule имя.

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

### -PatternToMatch
В шаблонах маршрутов правила не должно быть каких-либо знаков * за исключением случаев, когда это возможно после конечной точки или в конце пути. Значение по умолчанию —/*

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -QueryParameterStripDirective
Обработка терминов запроса URL-адреса при создании ключа кэша.
Значение по умолчанию — StripAll

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSQueryParameterStripDirective
Parameter Sets: (All)
Aliases:
Accepted values: StripNone, StripAll

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов, в которой будет создано RoutingRule.

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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. FrontDoor. Models. PSRoutingRule

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)
