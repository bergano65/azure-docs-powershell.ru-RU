---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 560053ca6b5e49ffcef8dbb6ee4b0ba32f3ed276
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911010"
---
# Set-AzVirtualNetworkGatewayDefaultSite

## КРАТКИй обзор
Задает сайт по умолчанию для шлюза виртуальной сети.

## Максимальное

```
Set-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzVirtualNetworkGatewayDefaultSite** назначает сайт по умолчанию для виртуального сетевого шлюза с принудительным туннелированием.
Принудительное туннелирование обеспечивает способ переадресации трафика с привязкой к Интернету с виртуальных машин Azure в локальную сеть; Это позволяет проверять и проверять трафик перед его выпуском.
Принудительное туннелирование выполняется с помощью туннеля виртуальной частной сети (VPN). для этого туннеля требуется сайт по умолчанию, локальный шлюз, на котором перенаправляются все данные, связанные с Интернетом Azure.
**Set-AzVirtualNetworkGatewayDefaultSite** предоставляет способ изменения сайта по умолчанию, назначенного шлюзом.

## ИЛЛЮСТРИРУЮТ

### Пример 1: назначение сайта по умолчанию шлюзу виртуальной сети
```
PS C:\>$LocalGateway = Get-AzLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

В этом примере сайт по умолчанию назначается шлюзу виртуальной сети с именем ContosoVirtualGateway.

Первая команда создает ссылку на объект на локальный шлюз с именем ContosoLocalGateway.
Эта ссылка на объект, хранящаяся в переменной с именем $LocalGateway, представляет шлюз для настройки в качестве сайта по умолчанию.

.
Вторая команда создает ссылку на объект для шлюза виртуальной сети и сохраняет результат в переменной с именем $VirtualGateway.

Третья команда использует командлет **Set-AzVirtualNetworkGatewayDefaultSite** , чтобы назначить сайт по умолчанию ContosoVirtualGateway.

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

### -GatewayDefaultSite
Указывает ссылку на объект для шлюза локальной сети, назначаемого в качестве сайта по умолчанию для указанной виртуальной сети.
Вы можете использовать командлет Get-AzLocalNetworkGateway для создания ссылки на объект на локальный шлюз.

```yaml
Type: PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGateway
Указывает ссылку на объект шлюза виртуальной сети, на котором будет назначен сайт по умолчанию.
Вы можете создать ссылку на объект для шлюза виртуальной сети с помощью **Get-AzVirtualNetworkGateway** и указать имя шлюза.

Переменную $VirtualGateway можно использовать в качестве значения параметра для параметра *VirtualNetworkGateway* :

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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

###  
Этот командлет принимает конвейерные экземпляры объекта **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** .

## НАПРЯЖЕНИЕ

###  
Этот командлет изменяет существующие экземпляры объекта **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** .

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzLocalNetworkGateway](./Get-AzLocalNetworkGateway.md)

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[Remove-AzVirtualNetworkGatewayDefaultSite](./Remove-AzVirtualNetworkGatewayDefaultSite.md)


