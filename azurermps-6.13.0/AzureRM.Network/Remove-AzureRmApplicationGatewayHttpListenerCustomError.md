---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: d0f26991498d8efc88eaacf9d01ed7e95d92e2cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560064"
---
# Remove-AzureRmApplicationGatewayHttpListenerCustomError

## КРАТКИй обзор
Удаляет настраиваемую ошибку из HTTP-прослушивателя шлюза приложения.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Remove-AzureRmApplicationGatewayHttpListenerCustomError -StatusCode <String>
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Remove-AzureRmApplicationGatewayCustomError** удаляет настраиваемую ошибку из HTTP-прослушивателя шлюза приложения.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Удаление настраиваемой ошибки из прослушивателя HTTP
```powershell
PS C:\> $updatedlistener = Remove-AzureRmApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

Эта команда удаляет настраиваемую ошибку кода состояния HTTP 502 из прослушивателя HTTP $listener 01 и возвращает обновленный прослушиватель.

## ПАРАМЕТРЫ

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

### -HttpListener
Прослушиватель HTTP шлюза приложений

```yaml
Type: PSApplicationGatewayHttpListener
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -StatusCode
Код состояния ошибки клиента шлюза приложения.

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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.
Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
