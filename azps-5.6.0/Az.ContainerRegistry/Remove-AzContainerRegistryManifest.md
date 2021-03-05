---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/remove-azcontainerregistrymanifest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryManifest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryManifest.md
ms.openlocfilehash: def99b11efa5070881cc3226b9ec85449b4cc0b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963160"
---
# Remove-AzContainerRegistryManifest

## SYNOPSIS
Удаление манифеста ACR. 

## СИНТАКСИС

### ByManifestParameterSet (по умолчанию)
```
Remove-AzContainerRegistryManifest -RepositoryName <String> -Manifest <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByTagParameterSet
```
Remove-AzContainerRegistryManifest -RepositoryName <String> -Tag <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## ОПИСАНИЕ
Удаление манифеста ACR.
Чтобы использовать этот cmdlet, запустите `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`
в первую очередь.

## ПРИМЕРЫ

### Пример 1
```powershell
Remove-AzContainerRegistryManifest -RegistryName registry -RepositoryName test/busybox27 -Manifest sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab
True
```

Delete manifest sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab for repository test/busybox27 under registry

### Пример 2
```powershell
Remove-AzContainerRegistryManifest -RegistryName registry -RepositoryName test/busybox27 -Tag latest
True
```

Удалить манифест с новейшим тегом для проверки репозитория /busybox27 в реестре

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

### -Manifest
Ссылка на манифест.

```yaml
Type: System.String
Parameter Sets: ByManifestParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RegistryName
Имя реестра контейнера Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RepositoryName
Имя репозитория.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Тег.

```yaml
Type: System.String
Parameter Sets: ByTagParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Запрос на подтверждение перед запуском cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

## OUTPUTS

### System.Boolean

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ
