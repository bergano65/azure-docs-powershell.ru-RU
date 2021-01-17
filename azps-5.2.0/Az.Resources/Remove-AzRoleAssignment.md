---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8C1D738C-825D-4718-AD2A-9CFEAA7DBD3B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleAssignment.md
ms.openlocfilehash: fc954dcf2ce3b9a1c066b3986bbc0bbea302ea2d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98405660"
---
# Remove-AzRoleAssignment

## SYNOPSIS
Удаляет назначение роли для указанного директора, которому назначена определенная роль в определенной области.

## СИНТАКСИС

### EmptyParameterSet (по умолчанию)
```
Remove-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceWithObjectIdParameterSet
```
Remove-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceGroupWithObjectIdParameterSet
```
Remove-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ScopeWithObjectIdParameterSet
```
Remove-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RoleIdWithScopeAndObjectIdParameterSet
```
Remove-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceWithSignInNameParameterSet
```
Remove-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceGroupWithSignInNameParameterSet
```
Remove-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ScopeWithSignInNameParameterSet
```
Remove-AzRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceWithSPNParameterSet
```
Remove-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceGroupWithSPNParameterSet
```
Remove-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ScopeWithSPNParameterSet
```
Remove-AzRoleAssignment -ServicePrincipalName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RoleAssignmentParameterSet
```
Remove-AzRoleAssignment [-PassThru] [-InputObject] <PSRoleAssignment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## ОПИСАНИЕ
С помощью Remove-AzRoleAssignment управления можно отоблескать доступ к любой основной деятельности в заданной области и данной роли.
Объект назначения, то есть основной должен быть указан.
Основным может быть пользователь (с помощью параметров SignInName или ObjectId для идентификации пользователя), группа безопасности (с помощью параметра ObjectId для идентификации группы) или задача службы (для определения параметра ServicePrincipalName или ObjectId используется параметр ServicePrincipal).
Роль, которая назначена основной, должна быть указана с помощью параметра RoleDefinitionName.
Область назначения может быть указана и, если не указана, по умолчанию задана область действия подписки, т. е. оно попытается удалить назначение указанному основному заданию и роли в области подписки.
Область назначения можно укакручить с помощью одного из следующих параметров:
а)
Область: это вся полнейская область, начиная с \<subscriptionId\> /subscriptions/b.
ResourceGroupName — имя любой группы ресурсов в рамках подписки.
в.
ResourceName, ResourceType, ResourceGroupName и (необязательно) ParentResource — определяет определенный ресурс в подписке.

## ПРИМЕРЫ

### Пример 1
```
PS C:\> Remove-AzRoleAssignment -ResourceGroupName rg1 -SignInName john.doe@contoso.com -RoleDefinitionName Reader
```

Удаляет назначение ролей для тех, кому назначена роль "Читатель" в области "Группа ресурсов john.doe@contoso.com rg1".

### Пример 2
```
PS C:\> Remove-AzRoleAssignment -ObjectId 36f81fc3-b00f-48cd-8218-3879f51ff39f -RoleDefinitionName Reader
```

Удаляет назначение роли для группы, которая была определена объективным объектом и назначена роли "Читатель".
По умолчанию для удаления задания используется текущая подписка.

### Пример 3
```
PS C:\> $roleassignment = Get-AzRoleAssignment |Select-Object -First 1 -Wait
PS C:\> Remove-AzRoleAssignment -InputObject $roleassignment
```

Удаляет первый объект назначения роли, извлеченный Get-AzRoleAssignment командлета.

## PARAMETERS

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

### -InputObject
Объект "Назначение ролей".

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment
Parameter Sets: RoleAssignmentParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ObjectId
ОбъектId Azure AD пользователя, группы или основной службы.

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ParentResource
Родительский ресурс в иерархии (из ресурса, указанного с помощью параметра ResourceName), если он имеется.
Необходимо использовать в сочетании с параметрами ResourceGroupName, ResourceType и ResourceName, чтобы создать иерархическую область в виде относительного URI, определяемого ресурсом.

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Отображение удаленного назначения роли, если он задан.

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

### -ResourceGroupName
Имя группы ресурсов, которая назначена роли.
Пытается удалить назначение в указанной области действия группы ресурсов.
При использовании в сочетании с параметрами ResourceName, ResourceType и (необязательно)ParentResource команда формирует иерархическую область в виде относительного URI, определяемого ресурсом.

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceName
Имя ресурса.
Например, storageaccountprod.
Необходимо использовать в сочетании с параметрами ResourceGroupName, ResourceType и (необязательно)ParentResource, чтобы построить иерархическую область в виде относительного URI, определяемого ресурсом, и удаления назначения в этой области.

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceType
Тип ресурса.
Например, Microsoft.Network/virtualNetworks.
Необходимо использовать в сочетании с параметрами ResourceGroupName, ResourceName и (необязательно)ParentResource для создания иерархической области в виде относительного URI, определяемого ресурсом, и удаления назначения из этой области.

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RoleDefinitionId
ИД роли "СДБ", для которой нужно удалить назначение.

```yaml
Type: System.Guid
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RoleDefinitionName
Имя роли СДВ, для которой нужно удалить назначение, например "Читатель", "Участник", "Виртуальный администратор сети" и т. д.

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Scope
Область удаления назначения роли.
В формате относительного URI.
Например: "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".
Если не указано, будет предпринята попытка удалить роль на уровне подписки.
Если указано, оно должно начинаться с "/subscriptions/{id}".

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalName
Имя ServicePrincipalName приложения Azure AD

```yaml
Type: System.String
Parameter Sets: ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SignInName
Адрес электронной почты или имя директора пользователя.

```yaml
Type: System.String
Parameter Sets: ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ScopeWithSignInNameParameterSet
Aliases: Email, UserPrincipalName

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

### System.Guid

### Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment

## OUTPUTS

### Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment

## ПРИМЕЧАНИЯ
Ключевые слова: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment

## СВЯЗАННЫЕ ССЫЛКИ

[New-AzRoleAssignment](./New-AzRoleAssignment.md)

[Get-AzRoleAssignment](./Get-AzRoleAssignment.md)

[Get-AzRoleDefinition](./Get-AzRoleDefinition.md)

