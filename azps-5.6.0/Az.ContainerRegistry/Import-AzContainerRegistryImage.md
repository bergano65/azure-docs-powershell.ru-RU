---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/import-azcontainerregistryimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Import-AzContainerRegistryImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Import-AzContainerRegistryImage.md
ms.openlocfilehash: 675bc66afd41e5db2ee356ad45ee2fdd9b3482f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963208"
---
# Import-AzContainerRegistryImage

## SYNOPSIS
Импорт изображения из общеугорного или azure реестра в реестр контейнеров Azure.

## СИНТАКСИС

### ImportImageByResourceId (по умолчанию)
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryResourceId <String> [-Mode <String>] [-TargetTag <String[]>]
 [-UntaggedTargetRepository <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ImportImageByResourceIdWithCredential
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryResourceId <String> [-Mode <String>] [-TargetTag <String[]>]
 [-UntaggedTargetRepository <String[]>] [-Username <String>] -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ImportImageByRegistryUri
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryUri <String> [-Mode <String>] [-TargetTag <String[]>] [-UntaggedTargetRepository <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ImportImageByRegistryUriWithCredential
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryUri <String> [-Mode <String>] [-TargetTag <String[]>] [-UntaggedTargetRepository <String[]>]
 [-Username <String>] -Password <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## ОПИСАНИЕ
Импорт изображения из общеугорного или azure реестра в реестр контейнеров Azure.

## ПРИМЕРЫ

### Пример 1
```powershell
PS C:\> Import-AzContainerRegistryImage -SourceImage library/busybox:latest -ResourceGroupName $resourceGroupName -RegistryName $RegistryName -SourceRegistryUri docker.io -TargetTag busybox:latest
```

Импорт занятого почтового ящика в ACR. Примечание. 
* Перед исходным изображением нужно добавить "библиотека/". "busybox:latest" => "library/busybox:latest"
* Учетные данные необходимы, если исходный реестр не является общедоступным

### Пример 2
```powershell
PS C:\> Import-AzContainerRegistryImage -SourceImage $SourceRegistry.azurecr.io/busybox:latest -ResourceGroupName $resourceGroupName -RegistryName $RegistryName -SourceRegistryResourceId $SourceACRID -TargetTag busybox:latest
```

Импортировать занятое время из источника ACR, чтобы нацелить ACR. Примечание. 
* Учетные данные необходимы, если пользователь администратора для реестра источника отключен.

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

### -Mode
При принудительном перезаписи всех существующих целевых тегов.
При работе с NoForce все существующие целевые теги не будут работать перед началом копирования.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Force, NoForce

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Password
Пароль, используемый для проверки подлинности в реестре источника.

```yaml
Type: System.String
Parameter Sets: ImportImageByResourceIdWithCredential, ImportImageByRegistryUriWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RegistryName
Имя целевого реестра.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceImage
Имя репозитория для изображения источника.

Укажите изображение по репозиторию (привет, мир!).
Будет применяться новейший тег.

Укажите изображение по тегу ('hello-world:latest').

Указание изображения с помощью дайджеста манифеста на основе sha256 (' hello-world@sha256:abc123 ').

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

### -SourceRegistryResourceId
Идентификатор ресурса для источника azure Container Registry.

```yaml
Type: System.String
Parameter Sets: ImportImageByResourceId, ImportImageByResourceIdWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SourceRegistryUri
Адрес реестра источника (например, "mcr.microsoft.com").

```yaml
Type: System.String
Parameter Sets: ImportImageByRegistryUri, ImportImageByRegistryUriWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TargetTag
Список строк repo формы \[ \] :tag.
Если этот тег опущен, источник будет использоваться (или "последний", если также опущен исходный тег).

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UntaggedTargetRepository
Список строк с именами репозитория, которые нужно скопировать только для манифеста.
Тег не будет создан.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Username
Имя пользователя для проверки подлинности в реестре источника.

```yaml
Type: System.String
Parameter Sets: ImportImageByResourceIdWithCredential, ImportImageByRegistryUriWithCredential
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
