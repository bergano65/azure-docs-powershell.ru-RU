---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 77CDEE77-FD5D-4C2D-B027-FF1F6FF6618E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGateway.md
ms.openlocfilehash: 6c15f0dce8102acb609b2e7dcfb9ca4c17626906
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559712"
---
# Get-AzureRmApplicationGateway

## КРАТКИй обзор
Получает шлюз приложения.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Get-AzureRmApplicationGateway [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmApplicationGateway** получает шлюз приложения.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение указанного шлюза приложения
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

Эта команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $AppGw.

### Пример 2: получение списка шлюзов приложений в группе ресурсов
```
PS C:\>$AppGwList = Get-AzureRmApplicationGateway -ResourceGroupName "ResourceGroup01"
```

Эта команда получает список всех шлюзов приложений в группе ресурсов с именем ResourceGroup01 и сохраняет их в переменной $AppGwList.

### Пример 3: получение списка шлюзов приложений в подписке
```
PS C:\>$AppGwList = Get-AzureRmApplicationGateway
```

Эта команда возвращает список всех шлюзов приложений в подписке и сохраняет их в переменной $AppGwList.

## ПАРАМЕТРЫ

### -Name (имя)
Указывает имя шлюза приложения, который получает этот командлет.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов, которая содержит шлюз приложения.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### System. String

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Network. Models. PSApplicationGateway

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Остановить-AzureRmApplicationGateway](./Stop-AzureRmApplicationGateway.md)


