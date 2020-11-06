---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 23C6C9D3-A745-46C8-AB2C-B874223FBFFF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/get-azurermmediaservicenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceNameAvailability.md
ms.openlocfilehash: 8de8b9f389f8d57d844c17d92dd492390fbf1884
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560123"
---
# Get-AzureRmMediaServiceNameAvailability

## КРАТКИй обзор
Проверяет, доступно ли имя службы мультимедиа.
Имена служб мультимедиа глобально уникальны.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Get-AzureRmMediaServiceNameAvailability [-DefaultProfile <IAzureContextContainer>] [-AccountName] <String>
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmMediaServiceNameAvailability** проверяет, доступно ли имя службы мультимедиа.
Имена служб мультимедиа глобально уникальны.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Проверка наличия имени службы мультимедиа
```
PS C:\>Get-AzureRmMediaServiceNameAvailability -AccountName "MediaService1"
```

Эта команда проверяет, доступно ли имя MediaService1.

## ПАРАМЕТРЫ

### -Имя_учетной_записи
Указывает имя службы мультимедиа, которую получает этот командлет.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

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

### Ничего

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Media. Models. PSCheckNameAvailabilityOutput

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmMediaService](./Get-AzureRmMediaService.md)

[New-AzureRmMediaService](./New-AzureRmMediaService.md)

[Remove-AzureRmMediaService](./Remove-AzureRmMediaService.md)

[Set-AzureRmMediaService](./Set-AzureRmMediaService.md)


