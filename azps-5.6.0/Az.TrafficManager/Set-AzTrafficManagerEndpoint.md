---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/set-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 8f8ba0297ac0302e50dfdfdc25ddc3941fb10e34
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987241"
---
# Set-AzTrafficManagerEndpoint

## SYNOPSIS
Обновляет конечную точку Диспетчера трафика.

## СИНТАКСИС

```
Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
Cmdlet **Set-AzTrafficManagerEndpoint** обновляет конечную точку в Диспетчере трафика Azure.
Этот cmdlet обновляет параметры локального объекта конечной точки.
Объект конечной точки можно указать либо с помощью параметра *TrafficManagerEndpoint,* либо с помощью конвейера.

Локальный объект, который представляет конечную точку, можно получить с помощью Get-AzTrafficManagerEndpoint.
Измените объект локально, а затем зафиксировать изменения с помощью **Set-AzTrafficManagerEndpoint.**

## ПРИМЕРЫ

### Пример 1. Обновление конечной точки
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

Первая команда получает конечную точку Диспетчера трафика Azure с помощью командлета **Get-AzTrafficManagerEndpoint.**
Конечная точка хранится локально в переменной $TrafficManagerEndpoint.

Вторая команда изменяет конечную точку локально.
Эта команда изменяет вес конечной точки на 20.

Третья команда обновляет конечную точку диспетчера трафика в соответствие с локальным значением в $TrafficManagerEndpoint.

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

### -TrafficManagerEndpoint
Определяет локальный **объект TrafficManagerEndpoint.**
Этот командлет обновляет диспетчер трафика в связи с этим локальным объектом.

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
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

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint

## OUTPUTS

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ
