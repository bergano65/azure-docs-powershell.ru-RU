---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3efb6270-f908-4734-bdb1-6c7e4e4eb382
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
ms.openlocfilehash: 6561037b9174fd732d616f425324c164529e6367
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967816"
---
# Get-AzExpressRouteCrossConnection

## SYNOPSIS
Получает перекрестное подключение Azure ExpressRoute из Azure.

## СИНТАКСИС

```
Get-AzExpressRouteCrossConnection [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
Для извлечения объекта перекрестного подключения ExpressRoute из подписки используется cmdlet **Get-AzExpressRouteCrossConnection.**
AzureRmExpressRouteCrossConnection

## ПРИМЕРЫ

### Пример 1. Подключение ExpressRoute к интернету
```
Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
```

### Пример 2. Список перекрестных подключений ExpressRoute с помощью фильтра
```
Get-AzExpressRouteCrossConnection -Name test*
```

Этот cmdlet will list all ExpressRoute cross connections that begin with "test"

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

### -Name
Имя перекрестного подключения ExpressRoute.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### -ResourceGroupName
Имя группы ресурсов, которая содержит перекрестное подключение ExpressRoute.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Нет
Этот cmdlet не принимает входные данные.

## OUTPUTS

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Set-AzExpressRouteCrossConnection](Set-AzExpressRouteCrossConnection.md)