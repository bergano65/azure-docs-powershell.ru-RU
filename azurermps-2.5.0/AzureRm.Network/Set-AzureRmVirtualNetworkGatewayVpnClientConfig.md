---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EFB0D7A6-0C8A-4514-873D-672641CCCAF3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewayvpnclientconfig
schema: 2.0.0
ms.openlocfilehash: 471ad0ba4126026960879e5babbb592f352d3bcc
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914386"
---
# Set-AzureRmVirtualNetworkGatewayVpnClientConfig

## КРАТКИй обзор
Установка пула адресов VPN-клиентов для шлюза виртуальной сети.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### По умолчанию (по умолчанию)
```
Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RadiusServerConfiguration
```
Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]> -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzureRmVirtualNetworkVpnClientConfig** настраивает пул клиентских адресов для шлюза виртуальной сети.
Клиентам виртуальных частных сетей (VPN), которые подключаются к этому шлюзу, будет назначен IP-адрес из этого пула адресов.

## ИЛЛЮСТРИРУЮТ

### Пример 1: назначение пула адресов VPN-клиентов для шлюза виртуальной сети
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16"
```

В этом примере пул адресов VPN-клиентов назначается шлюзу виртуальной сети с именем ContosoVirtualGateway.

Первая команда создает ссылку на объект для шлюза, а объект хранится в переменной с именем $Gateway.

Вторая команда в примере использует командлет **Set-AzureRmVirtualNetworkGatewayVpnClientConfig** , чтобы назначить пулу адресов 10.0.0.0/16 для ContosoVirtualGateway.

### Пример 2: Настройка проверки подлинности на основе внешней RADIUS на существующем шлюзе
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> $Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force
PS C:\> Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd
```

В этом примере пул адресов VPN-клиентов назначается шлюзу виртуальной сети с именем ContosoVirtualGateway.

Первая команда создает ссылку на объект для шлюза, а объект хранится в переменной с именем $Gateway.

Вторая команда в примере использует командлет **Set-AzureRmVirtualNetworkGatewayVpnClientConfig** , чтобы назначить пулу адресов 10.0.0.0/16 для ContosoVirtualGateway. Кроме того, он настраивает внешний сервер RADIUS "TestRadiusServer", который будет использоваться для проверки подлинности для клиентов VPN.

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

### -RadiusServerAddress
Адрес внешнего RADIUS-сервера P2S.

```yaml
Type: String
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RadiusServerSecret
Секретный P2S внешнего RADIUS-сервера.

```yaml
Type: SecureString
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGateway
Указывает ссылку на объект шлюза виртуальной сети, который содержит параметры конфигурации VPN-клиента, изменяемые этим командлетом.
Вы можете создать ссылку на объект для шлюза виртуальной сети, используя Get-AzureRmVirtualNetworkGateway и указав имя шлюза.

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VpnClientAddressPool
Задает IP-адреса, назначаемые клиентам, которые подключаются к этому шлюзу.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске командлета. Командлет не выполняется.

```yaml
Type: SwitchParameter
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

###  
Этот командлет принимает конвейерные экземпляры объекта **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** .

## НАПРЯЖЕНИЕ

###  
Этот командлет изменяет существующие экземпляры объекта **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** .

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmVpnClientPackage](./Get-AzureRmVpnClientPackage.md)

[Get-AzureRmVirtualNetworkGateway](./Get-AzureRmVirtualNetworkGateway.md)

[Изменить размер — AzureRmVirtualNetworkGateway](./Resize-AzureRmVirtualNetworkGateway.md)


