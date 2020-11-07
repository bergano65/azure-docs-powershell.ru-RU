---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 364C41D0-A5DB-4AEF-853A-FE5A11AD9155
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayfrontendipconfig
schema: 2.0.0
ms.openlocfilehash: c138ced515932d158bb2a4a067ed405d8084db4e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913840"
---
# Get-AzureRmApplicationGatewayFrontendIPConfig

## КРАТКИй обзор
Получает интерфейсную конфигурацию IP-конфигурации для шлюза приложения.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Get-AzureRmApplicationGatewayFrontendIPConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmApplicationGatewayFrontendIPConfig** получает интерфейсную конфигурацию IP-конфигурации для шлюза приложений.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение указанной переднего плана IP-конфигурации
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIP= Get-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -ApplicationGateway $AppGw
```

Первая команда получает шлюз приложения с именем ApplicationGateway01 из группы ресурсов с именем ResourceGroup01 и сохраняет его в переменной $AppGw. Вторая команда получает клиентскую IP-конфигурацию с именем FrontEndIP01 from $AppGw и сохраняет ее в переменной $FrontEndIP.

### Пример 2: получение списка конфигураций IP-адресов интерфейсов
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIPs= Get-AzureRmApplicationGatewayFrontendIPConfig  -ApplicationGateway $AppGw
```

Первая команда получает шлюз приложения с именем ApplicationGateway01 из группы ресурсов с именем ResourceGroup01 и сохраняет его в переменной $AppGw. Вторая команда получает список IP-конфигураций переднего плана из $AppGw и сохраняет их в переменной $FrontEndIPs.

## ПАРАМЕТРЫ

### -ApplicationGateway
Указывает объект шлюза приложения, который содержит интерфейсную конфигурацию IP.

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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
Задает имя интерфейса IP-конфигурации, который получает интерфейсный командлет.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
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

### Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendIPConfiguration

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Add-AzureRmApplicationGatewayFrontendIPConfig](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[New-AzureRmApplicationGatewayFrontendIPConfig](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[Remove-AzureRmApplicationGatewayFrontendIPConfig](./Remove-AzureRmApplicationGatewayFrontendIPConfig.md)

[Set-AzureRmApplicationGatewayFrontendIPConfig](./Set-AzureRmApplicationGatewayFrontendIPConfig.md)


