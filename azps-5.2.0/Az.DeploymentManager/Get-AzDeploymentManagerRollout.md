---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
ms.openlocfilehash: c01c41ff476ee4e6b8a6291f5ebcfbf4c176b775
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324243"
---
# Get-AzDeploymentManagerRollout

## SYNOPSIS
Получает разкат.

## СИНТАКСИС

### Интерактивный (по умолчанию)
```
Get-AzDeploymentManagerRollout [-ResourceGroupName] <String> [[-Name] <String>] [-RetryAttempt <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceId
```
Get-AzDeploymentManagerRollout [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InputObject
```
Get-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## ОПИСАНИЕ
**Cmdlet Get-AzDeploymentManagerRollout** получает сведение и возвращает объект, который представляет это сведение со всеми подробными сведениями о ходе выполнения.
Укажите имя и группу ресурсов для разката. Кроме того, вы можете предоставить объект rollout или ResourceId.

В возвращаемом объекте развертывания содержатся службы, единицы обслуживания и этапы развертывания, которые были развернуты, а также те из них, которые уже развернуты. Пока не будут развернуты те из них, которые нужно развернуть.

## ПРИМЕРЫ

### Пример 1. Получить разкат
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

Эта команда получает раздатку ContosoRollout в contosoResourceGroup. 

### Пример 2. Получить и отобразить сведения о сведении о разкате
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -Verbose
```

Эта команда получает раздатку ContosoRollout в contosoResourceGroup. Переключатель -Verbose (Подробный) отображает все сведения о сведении с иерархической структурой; Показаны Службы,units и действия для каждого этапа и контекстная информация для каждого этапа, в котором показана целостная часть сведений.

### Пример 3. Разкат с использованием идентификатора ресурса
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

Эта команда получает раздатку ContosoRollout в contosoResourceGroup.

### Пример 4. Получить разкат с помощью объекта.
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

Эта команда получает разкат, имя и группа ресурсов которого соответствуют свойствам Name и ResourceGroupName $rolloutObject соответственно.

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

### -InputObject
Объект разката.

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Имя разката.

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Группа ресурсов.

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Идентификатор ресурса.

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RetryAttempt
Попытка повторного разката.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Interactive
Aliases:

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

### System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]

### Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout

## OUTPUTS

### Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ
