---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 1A84AF77-1AEF-4FD0-9FAA-D195B361FCEB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/set-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnEndpoint.md
ms.openlocfilehash: 13b5b219ec789ac54332caa366cfb0277f0bfacb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563732"
---
# Set-AzureRmCdnEndpoint

## КРАТКИй обзор
Обновляет конечную точку CDN.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Set-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzureRmCdnEndpoint** обновляет конечную точку сети доставки содержимого (CDN) для Azure.

## ИЛЛЮСТРИРУЮТ

## ПАРАМЕТРЫ

### -CdnEndpoint
Указывает конечную точку, которую обновляет этот командлет.

```yaml
Type: PSEndpoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

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

### PSEndpoint
Параметр "CdnEndpoint" принимает значение типа "PSEndpoint" из конвейера.

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. CDN. Models. Endpoint. PSEndpoint

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmCdnEndpoint](./Get-AzureRmCdnEndpoint.md)

[New-AzureRmCdnEndpoint](./New-AzureRmCdnEndpoint.md)

[Remove-AzureRmCdnEndpoint](./Remove-AzureRmCdnEndpoint.md)

[Start-AzureRmCdnEndpoint](./Start-AzureRmCdnEndpoint.md)

[Остановить-AzureRmCdnEndpoint](./Stop-AzureRmCdnEndpoint.md)


