---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: D28EB28D-DBC6-48D5-AB0A-C56F56CD0104
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/set-azmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaServiceKey.md
ms.openlocfilehash: 44c1ff2fe283e3cd804d20a8df21023b3c222150
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214297"
---
# Set-AzMediaServiceKey

## SYNOPSIS
Повторно сгенерирует ключ, используемый для доступа к конечной точке REST, связанной со службой мультимедиа.

## СИНТАКСИС

```
Set-AzMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String> [-KeyType] <KeyType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## ОПИСАНИЕ
С **помощью cmdlet Set-AzMediaServiceKey** можно сгенерировать ключ, используемый для доступа к конечной точке REST, связанной со службой мультимедиа.

## ПРИМЕРЫ

### Пример 1. Повторное сгенерировать первичный ключ, используемый для доступа к службе мультимедиа
```
PS C:\>Set-AzMediaServiceKey -ResourceGroupName "ResourceGroup004" -AccountName "MediaService001" -KeyType Primary
```

Эта команда повторно сгенерирует первичный ключ для службы мультимедиа MediaService001, которая принадлежит к группе ресурсов ResourceGroup004.

### Пример 2. Повторное сгенерирует дополнительный ключ, используемый для доступа к службе мультимедиа.
```
PS C:\>Set-AzMediaServiceKey -ResourceGroupName "Resourcegroup123" -AccountName "MediaService002" -KeyType Secondary
```

Эта команда повторно сгенерирует дополнительный ключ для службы мультимедиа MediaService002, которая принадлежит к группе ресурсов Resourcegroup123.

## PARAMETERS

### -AccountName
Указывает имя службы мультимедиа, которую повторно сгенерирует этот cmderlet.

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

### -KeyType
Указывает ключевой тип службы мультимедиа.
Допустимыми значениями для этого параметра являются первичный или дополнительный.

```yaml
Type: Microsoft.Azure.Management.Media.Models.KeyType
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 2
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

### -Confirm
Перед запуском cmdlet вам будет предложено подтвердить его.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске cmdlet.
Этот cmdlet не будет выполниться.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

## OUTPUTS

### Microsoft.Azure.Commands.Media.Models.PSServiceKey

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzMediaServiceKey](./Get-AzMediaServiceKey.md)


