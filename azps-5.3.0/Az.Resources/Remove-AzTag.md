---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
ms.openlocfilehash: 22a43739ec63f8287ce51c4c4f4a125b4e5b1c65
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507657"
---
# Remove-AzTag

## SYNOPSIS
Удаление предопределельных тегов и значений Azure | Удаляет весь набор тегов для ресурса или подписки.

## СИНТАКСИС

### RemovePredefinedTagParameterSet

```powershell
Remove-AzTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveByResourceIdParameterSet

```powershell
Remove-AzTag
   -ResourceId <String>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## ОПИСАНИЕ

**RemovePredefinedTagSet:** командлет **Remove-AzTag** удаляет предопределные теги и значения Azure из вашей подписки.
Чтобы удалить определенные значения из заранее определенного тега, используйте параметр *Value.*
По умолчанию **remove-AzTag** удаляет указанный тег и все его значения. Удалить тег или значение, примененные в данный момент к ресурсу или группе ресурсов, невозможно.
Перед **использованием командлета Remove-AzTag** используйте параметр *Tag* командлета Set-AzResourceGroup, чтобы удалить тег или значения из группы ресурсов или ресурса.
Модуль "Теги Azure", который входит в **состав тега Remove-AzTag,** помогает управлять предопределными тегами Azure.
Тег Azure — это пара "имя-значение", которую можно использовать для классификации ресурсов и групп ресурсов Azure, например по отделам или центрам затрат, а также для отслеживания заметок и примечаний к ресурсам и группам.
Теги можно определять и применять в одном шаге, но предопределяемые теги помечают стандартные, согласованные, предсказуемые имена и значения для тегов в подписке.

**RemoveByResourceIdParameterSet:** командлет **Remove-AzTag** с **ResourceId** удаляет весь набор тегов для ресурса или подписки.

## ПРИМЕРЫ

### Пример 1. Удаление предопределеного тега
```powershell
PS C:\>Remove-AzTag -Name "Department"
```

Эта команда удаляет предопределный тег "Отдел" и все его значения.
Если тег применен к ресурсам или группам ресурсов, команда не будет применена.

### Пример 2. Удаление значения из предопределеного тега
```powershell
PS C:\>Remove-AzTag -Name "Department" -Value "HumanResources" -PassThru
Name:   Department
Count:  14
Values: 

        Name        Count
        =========   =====

        Finance        2
        IT            12
```

Эта команда удаляет значение HumanResources из предопределенного тега Department.
Тег не удаляется.
Если значение было применено к ресурсам или группам ресурсов, команда не может быть применена.

### Пример 3. Удаление всего набора тегов в подписке

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}
```

Эта команда удаляет весь набор тегов в подписке с {subId}. Он не возвращает объект, удаленный, если он не прошел через "-PassThru".

### Пример 4. Удаление всего набора тегов для ресурса

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1 -PassThru

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

Эта команда удаляет весь набор тегов для ресурса с помощью {resourceId}. Он возвращает удаленный проект при передаче в "-PassThru".

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
Имя предопределяемого тега, который нужно удалить.
По умолчанию **remove-AzTag** удаляет указанный тег и все его значения.
Чтобы удалить выбранные значения, но не тег, используйте параметр *Value.*

```yaml
Type: System.String
Parameter Sets: RemovePredefinedTagParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Значение
Удаляет указанные значения из предопределяемого тега, но не удаляет его.

```yaml
Type: System.String[]
Parameter Sets: RemovePredefinedTagParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Идентификатор ресурса для сущности с тегами. Ресурс, группа ресурсов или подписка могут быть помечены тегами.

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Возвращает объект, который представляет удаленный тег или итоговую метку с удаленным значением.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
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
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

### System.String[]

### System.Management.Automation.SwitchParameter

## OUTPUTS

### Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzTag](./Get-AzTag.md)

[New-AzTag](./New-AzTag.md)

[Update-AzTag](./Update-AzTag.md)