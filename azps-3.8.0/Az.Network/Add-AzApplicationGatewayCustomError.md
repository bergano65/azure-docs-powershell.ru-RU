---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 424dd1c13dbc6d860bec05da84704caba96735af
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066330"
---
# Add-AzApplicationGatewayCustomError

## КРАТКИй обзор
Добавляет настраиваемое сообщение об ошибке в шлюз приложений.

## Максимальное

```
Add-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Add-AzApplicationGatewayCustomError** Добавляет настраиваемое сообщение об ошибке в шлюз приложений.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Добавление настраиваемой ошибки на уровне шлюза приложения
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Add-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

Эта команда добавляет настраиваемую ошибку кода состояния HTTP 502 в $appgw шлюза приложений и возвращает обновленный шлюз.

### Пример 2: Добавление настраиваемой ошибки на уровень прослушивателя шлюза приложения
```powershell
PS C:\> $resourceGroup = "resourceGroupName"
PS C:\> $AppGWName = "applicationGatewayName"
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $listenerName = "listenerName"
PS C:\> $AppGw = Get-AzApplicationGateway -Name $AppGWName -ResourceGroupName $rg
PS C:\> $listener = Get-AzApplicationGatewayHttpListener -ApplicationGateway $AppGW -Name $listenerName
PS C:\> $updatedListener = Add-AzApplicationGatewayHttpListenerCustomError -HttpListener $listener -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url 
PS C:\> Set-AzApplicationGateway -ApplicationGateway $AppGw
```

Эта команда добавляет настраиваемую ошибку кода состояния HTTP 502 в $appgw шлюза приложений на уровне прослушивателя и возвращают обновленный шлюз.

## ПАРАМЕТРЫ

### -ApplicationGateway
Шлюз приложений

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -CustomErrorPageUrl
URL-адрес страницы "ошибка" клиента шлюза приложения.

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

### -StatusCode
Код состояния ошибки клиента шлюза приложения.

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Microsoft. Azure. Commands. Network. Models. PSApplicationGateway

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzApplicationGatewayCustomError](./Get-AzApplicationGatewayCustomError.md)

[New-AzApplicationGatewayCustomError](./New-AzApplicationGatewayCustomError.md)

[Remove-AzApplicationGatewayCustomError](./Remove-AzApplicationGatewayCustomError.md)

[Set-AzApplicationGatewayCustomError](./Set-AzApplicationGatewayCustomError.md)
