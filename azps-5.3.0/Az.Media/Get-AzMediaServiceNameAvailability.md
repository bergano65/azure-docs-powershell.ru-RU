---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 23C6C9D3-A745-46C8-AB2C-B874223FBFFF
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservicenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
ms.openlocfilehash: d7718ffafd6383e0873e61955cd231ca8b6a409d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422631"
---
# Get-AzMediaServiceNameAvailability

## SYNOPSIS
Проверяет, доступно ли имя службы мультимедиа.
Имена служб мультимедиа являются уникальными глобально.

## СИНТАКСИС

```
Get-AzMediaServiceNameAvailability [-DefaultProfile <IAzureContextContainer>] [-AccountName] <String>
 [<CommonParameters>]
```

## ОПИСАНИЕ
Для проверки доступности имени медиа-службы будет доступен ли такой служарныйлет **Get-AzMediaServiceNameAvailability.**
Имена служб мультимедиа являются уникальными глобально.

## ПРИМЕРЫ

### Пример 1. Проверка на наличии имени службы мультимедиа
```
PS C:\>Get-AzMediaServiceNameAvailability -AccountName "MediaService1"
```

Эта команда проверяет, доступно ли имя MediaService1.

## PARAMETERS

### -AccountName
Указывает имя службы мультимедиа, которую получает этот cmdlet.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Нет

## OUTPUTS

### Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzMediaService](./Get-AzMediaService.md)

[New-AzMediaService](./New-AzMediaService.md)

[Remove-AzMediaService](./Remove-AzMediaService.md)

[Set-AzMediaService](./Set-AzMediaService.md)


