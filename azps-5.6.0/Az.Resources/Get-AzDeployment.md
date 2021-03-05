---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
ms.openlocfilehash: 92a0aac5043be520f6a7ed7afc2066e0532b79ec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960120"
---
# Get-AzDeployment

## SYNOPSIS
Получить развертывание

## СИНТАКСИС

### GetByDeploymentName (по умолчанию)
```
Get-AzDeployment [[-Name] <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByDeploymentId
```
Get-AzDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
Для развертывания требуется текущая область действия подписки с использованием **cmdlet Get-AzDeployment.**
Укажите *параметр "Имя"* *или "ИД",* чтобы отфильтровать результаты.
По умолчанию **Get-AzDeployment** получает все развертывания с текущей областью действия подписки.

## ПРИМЕРЫ

### Пример 1. Все развертывания в рамках подписки
```
PS C:\>Get-AzDeployment
```

Эта команда получает все развертывания в текущей области действия подписки.

### Пример 2. Получить развертывание по имени
```
PS C:\>Get-AzDeployment -Name "DeployRoles01"
```

Эта команда получает развертывание DeployRoles01 в рамках текущей подписки.
Вы можете назначить имя развертыванию при его создании с помощью проектлетов **New-AzDeployment.**
Если не назначить имя, в качестве имени по умолчанию будет использоваться шаблон, используемый для создания развертывания.

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

### -Id
Полное ид ресурса в развертывании.
пример: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}

```yaml
Type: System.String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Имя развертывания.

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Pre
Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
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

### Нет

## OUTPUTS

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDвслух

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ
