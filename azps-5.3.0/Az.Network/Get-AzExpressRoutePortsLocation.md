---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportslocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
ms.openlocfilehash: 918ef18717cb09bad28ee10b91f635181dd5b3cb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422279"
---
# Get-AzExpressRoutePortsLocation

## SYNOPSIS
Возвращает расположения, в которых доступны ресурсы ExpressRoutePort.

## СИНТАКСИС

```
Get-AzExpressRoutePortsLocation [-LocationName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## ОПИСАНИЕ
Для извлечения ресурсов **ExpressRoutePortsLocation используется cmdlet Get-AzExpressRoutePortsLocation.** Если в качестве входного данных задано определенное расположение, он отображает подробные сведения о конкретном расположении, то есть список доступных пропускной способности в этом расположении.

## ПРИМЕРЫ

### Пример 1
```powershell
PS C:\> Get-AzExpressRoutePortsLocation
```

Здесь перечислены расположения, в которых доступны ресурсы ExpressRoutePort.

### Пример 2
```powershell
PS C:\> Get-AzExpressRoutePortsLocation -LocationName $loc
```

Список пропускной способности ExpressRoutePort, доступных в $loc.

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

### -LocationName
Название расположения.

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

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

## OUTPUTS

### Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ
