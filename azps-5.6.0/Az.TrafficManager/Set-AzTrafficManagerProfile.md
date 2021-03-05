---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/set-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
ms.openlocfilehash: 4a4d09fb0e44dcb09781b2155e1bfe2d10a0cc80
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987213"
---
# Set-AzTrafficManagerProfile

## SYNOPSIS
Обновляет профиль диспетчера трафика.

## СИНТАКСИС

```
Set-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
Cmdlet **Set-AzTrafficManagerProfile** обновляет профиль Azure Traffic Manager.
Этот cmdlet обновляет параметры профиля из локального объекта профиля.
Объект профиля можно указать либо с помощью параметра *TrafficManagerProfile,* либо с помощью конвейера.

Вы можете получить локальный объект, который представляет профиль, с помощью Get-AzTrafficManagerProfile управления.
Измените объект локально, а затем с помощью **Set-AzTrafficManagerProfile** зафиксировать изменения.

## ПРИМЕРЫ

### Пример 1. Обновление профиля
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

Первая команда получает профиль Диспетчера трафика Azure с помощью Get-AzTrafficManagerProfile командлета.
Команда сохраняет профиль локально в переменной $TrafficManagerProfile.

Вторая команда изменяет профиль локально.
Эта команда отключает профиль.

Третья команда обновляет профиль диспетчера трафика с именем ContosoProfile в соответствие с локальным значением в $TrafficManagerProfile.

## PARAMETERS

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

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

### -TrafficManagerProfile
Определяет локальный **объект TrafficManagerProfile.**
Этот командлет обновляет диспетчер трафика в связи с этим локальным объектом.

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile

## OUTPUTS

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Add-AzTrafficManagerEndpointConfig](./Add-AzTrafficManagerEndpointConfig.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[New-AzTrafficManagerProfile](./New-AzTrafficManagerProfile.md)

[Remove-AzTrafficManagerEndpointConfig](./Remove-AzTrafficManagerEndpointConfig.md)

[Remove-AzTrafficManagerProfile](./Remove-AzTrafficManagerProfile.md)


