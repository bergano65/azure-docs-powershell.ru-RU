---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 2099938F-5325-416C-AE10-6813546A1055
online version: https://docs.microsoft.com/powershell/module/az.media/get-azmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceKey.md
ms.openlocfilehash: 59f288c74c8f5230375a475df839c491e07e58d3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996621"
---
# Get-AzMediaServiceKey

## SYNOPSIS
Получает основные сведения о доступе к конечной точке REST, связанной со службой мультимедиа.

## СИНТАКСИС

```
Get-AzMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
С **помощью cmdlet Get-AzMediaServiceKey** можно получить основные сведения о доступе к конечной точке REST, связанной со службой мультимедиа Azure.

## ПРИМЕРЫ

### Пример 1. Получите основные сведения о доступе к службе мультимедиа
```
PS C:\>Get-AzMediaServiceKey -ResourceGroupName "ResourceGroup001" -AccountName "MediaService001"
```

Эта команда получает основные сведения о доступе к службе мультимедиа MediaService001, которая принадлежит к группе ресурсов ResourceGroup001.

## PARAMETERS

### -AccountName
Указывает имя службы мультимедиа, из которую этот cmdlet получает ключи службы мультимедиа.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -ResourceGroupName
Имя группы ресурсов, которая содержит службу мультимедиа.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

## OUTPUTS

### Microsoft.Azure.Commands.Media.Models.PSServiceKeys

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Set-AzMediaServiceKey](./Set-AzMediaServiceKey.md)


