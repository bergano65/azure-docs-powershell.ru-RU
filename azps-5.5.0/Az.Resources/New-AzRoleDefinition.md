---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8300B143-E322-419E-BC98-DBA56DD90A59
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
ms.openlocfilehash: 8916b35da467fb16fd3802b726a7e105093b1c7a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100217724"
---
# New-AzRoleDefinition

## SYNOPSIS
Создает пользовательскую роль в Azure RBAC.
В качестве входных данных можно ввести файл определения роли JSON или объект PSRoleDefinition.
Сначала используйте команду Get-AzRoleDefinition для создания объекта определения базовой роли.
Затем измените его свойства, как требуется.
Наконец, используйте эту команду для создания пользовательской роли с помощью определения роли.

## СИНТАКСИС

### InputFileParameterSet
```
New-AzRoleDefinition [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RoleDefinitionParameterSet
```
New-AzRoleDefinition [-Role] <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
Этот New-AzRoleDefinition создает пользовательскую роль в azure Role-Based Access Control.
Предопределять определение роли в качестве входных данных для команды в качестве файла JSON или объекта PSRoleDefinition.
Определение входной роли ДОЛЖНО содержать следующие свойства:
1) DisplayName: имя настраиваемой роли
2) Описание: краткое описание роли, которая суммирует доступ, который предоставляет роль.
3) Действия: набор операций, доступ к которым предоставляет пользовательская роль.
Используйте Get-AzProviderOperation, чтобы получить операцию для поставщиков ресурсов Azure, которые можно защищены с помощью Azure RBAC.
Ниже ются допустимые строки операций.
 - "*/read" предоставляет доступ к операциям чтения всем поставщикам ресурсов Azure.
 - "Microsoft.Network/*/read" предоставляет доступ к операциям чтения для всех типов ресурсов в поставщике ресурсов Microsoft.Network Azure.
 - Microsoft.Compute/virtualMa ветвях/*" предоставляет доступ ко всем операциям виртуальной машины и ее потомковым типам ресурсов.
4) AssignableScopes: набор областей (подписки Azure или группы ресурсов), в которых настраиваемая роль будет доступна для назначения.
С помощью AssignableScopes вы можете сделать настраиваемую роль доступной для назначений только в необходимых подписках или группах ресурсов, а не загромождать пользовательский интерфейс для остальных подписок или групп ресурсов.
Ниже ются некоторые допустимые области назначения:
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": делает роль доступной для назначения в двух подписках.
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": делает роль доступной для назначения по одной подписке.
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": делает роль доступной для назначения только в группе сетевых ресурсов.
Определение входной роли МОЖЕТ содержать следующие свойства:
1) NotActions: набор операций, которые необходимо исключить из действий для определения эффективных действий для настраиваемой роли.
Если вы не хотите предоставлять доступ к определенной роли для определенной операции, удобнее использовать notActions, чтобы исключить ее, а не указывать все операции, кроме конкретной.
2) DataActions — набор операций с данными, доступ к которым предоставляет пользовательская роль.
3) NotDataActions: набор операций, которые необходимо исключить из действий dataActions для определения эффективных действий с данными для настраиваемой роли.
Если вы не хотите предоставлять доступ к определенной роли для определенной операции данных, удобнее использовать NotDataActions, чтобы исключить ее, а не указывать все операции, кроме конкретной.
ПРИМЕЧАНИЕ. Если пользователю назначена роль, которая указывает операцию в notActions, а также назначена другая роль, предоставляет доступ к этой же операции — пользователь сможет выполнить эту операцию.
NotActions не является правилом запрета— это просто удобный способ создать набор разрешенных операций, когда требуется исключить определенные операции.
Ниже представлен пример определения роли json, которое можно ввести { "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ "*/read", "Microsoft.ClassicCompute/virtualmaоes/restart/action", "Microsoft.ClassicCompute/virtualmaиes/start/action" \] , "NotActions": \[ "*/write" \] , "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \] , "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/write" \] , "AssignableScopes": \[ "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" \] }

## ПРИМЕРЫ

### Пример 1. Создание с помощью PSRoleDefinitionObject
```powershell
PS C:\> $role = Get-AzRoleDefinition -Name "Virtual Machine Contributor"

PS C:\> $role.Id = $null
PS C:\> $role.Name = "Virtual Machine Operator"
PS C:\> $role.Description = "Can monitor, start, and restart virtual machines."
PS C:\> $role.Actions.RemoveRange(0,$role.Actions.Count)
PS C:\> $role.Actions.Add("Microsoft.Compute/*/read")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/start/action")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/restart/action")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/downloadRemoteDesktopConnectionFile/action")
PS C:\> $role.Actions.Add("Microsoft.Network/*/read")
PS C:\> $role.Actions.Add("Microsoft.Storage/*/read")
PS C:\> $role.Actions.Add("Microsoft.Authorization/*/read")
PS C:\> $role.Actions.Add("Microsoft.Resources/subscriptions/resourceGroups/read")
PS C:\> $role.Actions.Add("Microsoft.Resources/subscriptions/resourceGroups/resources/read")
PS C:\> $role.Actions.Add("Microsoft.Insights/alertRules/*")
PS C:\> $role.Actions.Add("Microsoft.Support/*")
PS C:\> $role.AssignableScopes.Clear()
PS C:\> $role.AssignableScopes.Add("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")

PS C:\> New-AzRoleDefinition -Role $role
```

### Пример 2. Создание с помощью файла JSON
```powershell
PS C:\> New-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

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

### -InputFile
Имя файла, содержащее одно определение роли json.

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Роль
Объект определения роли.

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Нет

## OUTPUTS

### Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition

## ПРИМЕЧАНИЯ
Ключевые слова: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzProviderOperation](./Get-AzProviderOperation.md)

[Get-AzRoleDefinition](./Get-AzRoleDefinition.md)

[Set-AzRoleDefinition](./Set-AzRoleDefinition.md)

[Remove-AzRoleDefinition](./Remove-AzRoleDefinition.md)

