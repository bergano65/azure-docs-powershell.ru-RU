---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: bfd90797ff60c42927b23424e3c100efd16a6d24
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911105"
---
# Remove-AzVirtualNetworkGatewayDefaultSite

## КРАТКИй обзор
Удаляет сайт по умолчанию из шлюза виртуальной сети.

## Максимальное

```
Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Remove-AzVirtualNetworkGatewayDefaultSite** удаляет сайт по умолчанию для принудительного туннелирования из шлюза виртуальной сети.
Принудительное туннелирование обеспечивает способ переадресации трафика с привязкой к Интернету с виртуальных машин Azure в локальную сеть; Это позволяет проверять и проверять трафик перед его выпуском.
Принудительное туннелирование выполняется с помощью туннеля виртуальной частной сети (VPN). для этого туннеля требуется сайт по умолчанию, локальный шлюз, на котором перенаправляются все данные, связанные с Интернетом Azure.

**Remove-AzVirtualNetworkGatewayDefaultSite** удаляет сайт по умолчанию, назначенный шлюзу.
Если вы это сделаете, вы должны использовать Set-AzVirtualNetworkGatewayDefaultSite для назначения нового сайта по умолчанию, прежде чем шлюз можно будет использовать для принудительного туннелирования.

## ИЛЛЮСТРИРУЮТ

### Пример 1: удаление сайта по умолчанию, назначенного шлюзу виртуальной сети
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworknGateway $Gateway
```

В этом примере удаляется сайт по умолчанию, который в данный момент назначен шлюзу виртуальной сети с именем ContosoVirtualGateway.

Первая команда использует **Get-AzVirtualNetworkGateway** для создания ссылки на объект Gateway. Эта ссылка на объект хранится в переменной с именем $Gateway.

Вторая команда использует команду **Remove-AzVirtualNetworkGatewayDefaultSite** , чтобы удалить сайт по умолчанию, назначенный этому шлюзу.

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

### -VirtualNetworkGateway
Указывает ссылку на объект шлюза виртуальной сети, содержащего сайт по умолчанию, который нужно удалить.
Вы можете создать ссылку на объект для шлюза виртуальной сети, используя Get-AzVirtualNetworkGateway и указав имя шлюза.

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

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[Set-AzVirtualNetworkGatewayDefaultSite](./Set-AzVirtualNetworkGatewayDefaultSite.md)


