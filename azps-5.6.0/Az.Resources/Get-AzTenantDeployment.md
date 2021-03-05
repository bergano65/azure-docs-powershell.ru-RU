---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
ms.openlocfilehash: 1755438dfc5bdb9b4eedf46ec364e851a2bca154
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997223"
---
# Get-AzTenantDeployment

## SYNOPSIS
Развертывание в области клиента

## СИНТАКСИС

### GetByDeploymentName (по умолчанию)
```
Get-AzTenantDeployment [[-Name] <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByDeploymentId
```
Get-AzTenantDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
Для развертывания в области клиента развертывание возвращается с использованием **cmdlet Get-AzTenantDeployment.**
Укажите *параметр "Имя"* *или "ИД",* чтобы отфильтровать результаты.
По умолчанию **Get-AzTenantDeployment** получает все развертывания в рамках клиента.

## ПРИМЕРЫ

### Пример 1. Получить все развертывания в рамках клиента
```
PS C:\>Get-AzTenantDeployment
```

Эта команда получает все развертывания в текущей области клиента.

### Пример 2. Получить развертывание по имени
```
PS C:\>Get-AzDeployment -Name "Deploy01"
```

Эта команда получает развертывание Deploy01 в текущей области клиента.
Вы можете назначить имя развертыванию при его создании с помощью выполнения с помощью проектлетов **New-AzTenantDeployment.**
Если не назначить имя, в качестве имени по умолчанию будет использоваться шаблон, используемый для создания развертывания.

### Пример 3. Получить развертывание по ИД
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Resources/deployments/Deploy01"
```

Эта команда получает развертывание Deploy01 в области клиента.

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
пример: /providers/Microsoft.Resources/deployments/{deploymentName}

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
