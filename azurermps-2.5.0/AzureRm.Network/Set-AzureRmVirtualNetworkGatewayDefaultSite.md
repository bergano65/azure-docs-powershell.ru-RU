---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewaydefaultsite
schema: 2.0.0
ms.openlocfilehash: 463951ca6b6679671f330a3ddb0f9460a878a3d3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914390"
---
# Set-AzureRmVirtualNetworkGatewayDefaultSite

## КРАТКИй обзор
Задает сайт по умолчанию для шлюза виртуальной сети.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Set-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzureRmVirtualNetworkGatewayDefaultSite** назначает сайт по умолчанию для виртуального сетевого шлюза с принудительным туннелированием.
Принудительное туннелирование обеспечивает способ переадресации трафика с привязкой к Интернету с виртуальных машин Azure в локальную сеть; Это позволяет проверять и проверять трафик перед его выпуском.
Принудительное туннелирование выполняется с помощью туннеля виртуальной частной сети (VPN). для этого туннеля требуется сайт по умолчанию, локальный шлюз, на котором перенаправляются все данные, связанные с Интернетом Azure.
**Set-AzureRmVirtualNetworkGatewayDefaultSite** предоставляет способ изменения сайта по умолчанию, назначенного шлюзом.

## ИЛЛЮСТРИРУЮТ

### Пример 1: назначение сайта по умолчанию шлюзу виртуальной сети
```
PS C:\>$LocalGateway = Get-AzureRmLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzureRmVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

В этом примере сайт по умолчанию назначается шлюзу виртуальной сети с именем ContosoVirtualGateway.

Первая команда создает ссылку на объект на локальный шлюз с именем ContosoLocalGateway.
Эта ссылка на объект, хранящаяся в переменной с именем $LocalGateway, представляет шлюз для настройки в качестве сайта по умолчанию.

.
Вторая команда создает ссылку на объект для шлюза виртуальной сети и сохраняет результат в переменной с именем $VirtualGateway.

Третья команда использует командлет **Set-AzureRmVirtualNetworkGatewayDefaultSite** , чтобы назначить сайт по умолчанию ContosoVirtualGateway.

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
Вы можете использовать командлет Get-AzureRmLocalNetworkGateway для создания ссылки на объект на локальный шлюз.

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
Вы можете создать ссылку на объект для шлюза виртуальной сети с помощью **Get-AzureRmVirtualNetworkGateway** и указать имя шлюза.

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

###  
Этот командлет принимает конвейерные экземпляры объекта **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** .

## НАПРЯЖЕНИЕ

###  
Этот командлет изменяет существующие экземпляры объекта **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** .

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmLocalNetworkGateway](./Get-AzureRmLocalNetworkGateway.md)

[Get-AzureRmVirtualNetworkGateway](./Get-AzureRmVirtualNetworkGateway.md)

[Remove-AzureRmVirtualNetworkGatewayDefaultSite](./Remove-AzureRmVirtualNetworkGatewayDefaultSite.md)


