---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6FBFAEFF-786D-440A-94B2-8C27BE033A0A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
ms.openlocfilehash: 6f22c8026d3b72a6c9cd52563252aa3d4bcad039
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914109"
---
# Add-AzureRmApplicationGatewayBackendAddressPool

## КРАТКИй обзор
Добавляет пул серверных адресов в шлюз приложений.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Add-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Add-AzureRmApplicationGatewayBackendAddressPool** добавляет пул серверных адресов в шлюз приложений.
Внутренний адрес можно указать с помощью IP-адреса, полного доменного имени (FQDN) или ИД IP-конфигурации.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Добавление пула серверных адресов с помощью полного доменного имени сервера
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", " contoso1.com"
```

Первая команда получает шлюз приложения с именем ApplicationGateway01 в группе ресурсов с именем ResourceGroup01 и сохраняет ее в переменной $AppGw. Вторая команда добавляет пул одноранговых адресов для шлюза приложений, хранящегося в $AppGw, с помощью полных доменных имен.

### Пример 2: Добавление пула односерверных адресов с помощью IP-адресов внутреннего сервера
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add -AzureApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

Первая команда получает шлюз приложения с именем ApplicationGateway01 в группе ресурсов с именем ResourceGroup01 и сохраняет ее в переменной $AppGw. Вторая команда добавляет пул одноадресных адресов для шлюза приложений, хранящегося в $AppGw, используя IP-адреса.

### Пример 3: Seta пула одноранговых адресов с помощью идентификатора IP-адреса сервера внутренней стороны
```
PS C:\>$Nic01 = Get-AzureRmNetworkInterface -Name "Nic01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Nic02 = Get-AzureRmNetworkInterface -Name "Nic02" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPConfigurationIds $nic01.Properties.IpConfigurations[0].Id, $nic02.Properties.IpConfiguration[0].Id
```

Первая команда получает объект сетевого интерфейса с именем Nic01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $Nic 01. Вторая команда получает объект сетевого интерфейса с именем Nic02, который принадлежит группе ресурсов с именем ResourceGroup02, и сохраняет его в переменной $Nic 02. Третья команда получает шлюз приложения с именем ApplicationGateway01 в группе ресурсов с именем ResourceGroup01 и сохраняет его в переменной $AppGw. В приведенной выше команде используются коды конфигурации IP-адресов для $Nic 01 и $Nic 02, чтобы добавить пул серверных адресов для шлюза приложений, хранящегося в $AppGw.

## ПАРАМЕТРЫ

### -ApplicationGateway
Указывает шлюз приложений, к которому этот командлет добавляет пул серверных адресов.

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

### -BackendFqdns
Указывает список полных доменных имен, которые этот командлет добавляет как пул внутренних серверов.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendIPAddresses
Задает список серверных IP-адресов, которые этот командлет добавляет как пул серверного сервера.

```yaml
Type: System.Collections.Generic.List`1[System.String]
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
Указывает имя серверного пула, который добавляет этот командлет.

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

### -Confirm
Запрашивает подтверждение перед запуском командлета.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске командлета.
Командлет не выполняется.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

###  
System. String

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Network. Models. PSApplicationGateway

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmApplicationGatewayBackendAddressPool](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[Get-AzureRmApplicationGatewayBackendAddressPool](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[New-AzureRmApplicationGatewayBackendAddressPool](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[Remove-AzureRmApplicationGatewayBackendAddressPool](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)

[Set-AzureRmApplicationGatewayBackendAddressPool](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


