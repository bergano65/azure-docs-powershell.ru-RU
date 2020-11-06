---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 5a2490e25d42e6285183d1f78182ce0d7c92f02f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566678"
---
# Remove-AzureRmVirtualNetworkGatewayDefaultSite

## КРАТКИй обзор
Удаляет сайт по умолчанию из шлюза виртуальной сети.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Remove-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Remove-AzureRmVirtualNetworkGatewayDefaultSite** удаляет сайт по умолчанию для принудительного туннелирования из шлюза виртуальной сети.
Принудительное туннелирование обеспечивает способ переадресации трафика с привязкой к Интернету с виртуальных машин Azure в локальную сеть; Это позволяет проверять и проверять трафик перед его выпуском.
Принудительное туннелирование выполняется с помощью туннеля виртуальной частной сети (VPN). для этого туннеля требуется сайт по умолчанию, локальный шлюз, на котором перенаправляются все данные, связанные с Интернетом Azure.

**Remove-AzureRmVirtualNetworkGatewayDefaultSite** удаляет сайт по умолчанию, назначенный шлюзу.
Если вы это сделаете, вы должны использовать Set-AzureRmVirtualNetworkGatewayDefaultSite для назначения нового сайта по умолчанию, прежде чем шлюз можно будет использовать для принудительного туннелирования.

## ИЛЛЮСТРИРУЮТ

### Пример 1: удаление сайта по умолчанию, назначенного шлюзу виртуальной сети
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworknGateway $Gateway
```

В этом примере удаляется сайт по умолчанию, который в данный момент назначен шлюзу виртуальной сети с именем ContosoVirtualGateway.

Первая команда использует **Get-AzureRmVirtualNetworkGateway** для создания ссылки на объект Gateway. Эта ссылка на объект хранится в переменной с именем $Gateway.

Вторая команда использует команду **Remove-AzureRmVirtualNetworkGatewayDefaultSite** , чтобы удалить сайт по умолчанию, назначенный этому шлюзу.

## ПАРАМЕТРЫ

### -VirtualNetworkGateway
Указывает ссылку на объект шлюза виртуальной сети, содержащего сайт по умолчанию, который нужно удалить.
Вы можете создать ссылку на объект для шлюза виртуальной сети, используя Get-AzureRmVirtualNetworkGateway и указав имя шлюза.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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

[Get-AzureRmVirtualNetworkGateway](./Get-AzureRmVirtualNetworkGateway.md)

[Set-AzureRmVirtualNetworkGatewayDefaultSite](./Set-AzureRmVirtualNetworkGatewayDefaultSite.md)


