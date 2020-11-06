---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteConfig.md
ms.openlocfilehash: dd23891bc56ac2eb8fce30708d9a72055a567bf3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562947"
---
# Get-AzureRmRouteConfig

## КРАТКИй обзор
Возвращает маршруты из таблицы маршрутов.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Get-AzureRmRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmRouteConfig** получает маршруты из таблицы маршрута Azure.
Вы можете указать маршрут по имени.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение таблицы маршрутов
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Get-AzureRmRouteConfig -Name "Route07"
Name              : route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

Эта команда получает таблицу маршрутов с именем RouteTable01 с помощью командлета **Get-AzureRmRouteTable** .
Команда передает эту таблицу в текущий командлет с помощью оператора конвейера.
Текущий командлет получает маршрут с именем Route07 в таблице маршрутов с именем RouteTable01.

## ПАРАМЕТРЫ

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

### -Name (имя)
Указывает имя маршрута, который получает этот командлет.

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

### -RouteTable
Указывает таблицу маршрутов, из которой этот командлет получает маршруты.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Microsoft. Azure. Commands. Network. Models. PSRouteTable

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Network. Models. PSRoute

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Add-AzureRmRouteConfig](./Add-AzureRmRouteConfig.md)

[Get-AzureRmRouteTable](./Get-AzureRmRouteTable.md)

[New-AzureRmRouteConfig](./New-AzureRmRouteConfig.md)

[Remove-AzureRmRouteConfig](./Remove-AzureRmRouteConfig.md)

[Set-AzureRmRouteConfig](./Set-AzureRmRouteConfig.md)


