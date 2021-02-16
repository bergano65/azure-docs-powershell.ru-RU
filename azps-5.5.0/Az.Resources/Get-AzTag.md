---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
ms.openlocfilehash: 058f4a61f1e7ff2fe7f416ea0e4ada098c9efe51
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240077"
---
# Get-AzTag

## SYNOPSIS
Предопределяет теги Azure | Возвращает весь набор тегов для ресурса или подписки.

## СИНТАКСИС

### GetPredefinedTagParameterSet
```
Get-AzTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceIdParameterSet
```
Get-AzTag -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ

**GetPredefinedTagSet:** командлет **Get-AzTag** получает предопределять теги Azure в вашей подписке.
Этот командлет возвращает основные сведения о тегах или подробные сведения о тегах и их значениях.
Все выходные объекты содержат свойство Count, которое представляет количество ресурсов и групп ресурсов, к которым были применены теги и значения.
Модуль "Теги Azure", который входит в **состав тега Get-AzTag,** помогает управлять предопределными тегами Azure.
Тег Azure — это пара "имя-значение", которую можно использовать для классификации ресурсов и групп ресурсов Azure, например по отделам или центрам затрат, а также для отслеживания заметок и примечаний к ресурсам и группам.
Теги можно определять и применять в одном шаге, но предопределяемые теги помечают стандартные, согласованные, предсказуемые имена и значения для тегов в подписке.
Чтобы создать предопределный тег, воспользуйтесь New-AzTag командлетом.
Чтобы применить предопределный тег к группе ресурсов, используйте параметр *"Тег"* New-AzTag командлета.
Для поиска в группах ресурсов определенного имени или имени тега и значения используйте параметр *Tag* Get-AzResourceGroup командлета.

**GetByResourceIdParameterSet:** командлет **Get-AzTag** с **ResourceId** получает весь набор тегов для ресурса или подписки.

## ПРИМЕРЫ

### Пример 1. Получить все предопределные теги
```powershell
PS C:\>Get-AzTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

Эта команда получает все заранее задав теги в подписке.
Свойство Count показывает, сколько раз тег применялся к ресурсам и группам ресурсов в подписке.

### Пример 2. Пометка тега по имени
```powershell
PS C:\>Get-AzTag -Name "Department"

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3
```

Эта команда получает подробные сведения о теге Department и его значениях.
Свойство Count показывает, сколько раз тег и каждое из его значений применялось к ресурсам и группам ресурсов в подписке.

### Пример 3. Получить значения всех тегов
```powershell
PS C:\>Get-AzTag -Detailed

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3


Name:   FY2015
Count:  2


Name:   CostCenter
Count:  20
Values: 

        Name        Count
        ==========  =====

        0001          5
        0002         10
        0003          5
```

Эта команда использует параметр *Detailed* для получения подробных сведений обо всех предопределеных тегах в подписке.
Использование *параметра Detailed* эквивалентно использованию *параметра Name* для каждого тега.

### Пример 4. Получите весь набор тегов в подписке

```powershell
PS C:\>Get-AzTag -ResourceId /subscriptions/{subId}

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             tagKey1  tagValue1
             tagKey2  tagValue2
```

Эта команда получает весь набор тегов для подписки {subId}.

### Пример 5. Получить весь набор тегов для ресурса

```powershell
PS C:\>Get-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

Эта команда получает весь набор тегов для ресурса с помощью {resourceId}.

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

### -Подробный
Указывает на то, что эта операция добавляет к выходным данным сведения о значениях тегов.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetPredefinedTagParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Имя предопределяемого тега.
По умолчанию **Get-AzTag** получает основные сведения обо всех предопределеных тегах в подписке.
Если задать параметр *Name,* подробный *параметр* не будет действовать.

```yaml
Type: System.String
Parameter Sets: GetPredefinedTagParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Идентификатор ресурса для сущности с тегами. Ресурс, группа ресурсов или подписка могут быть помечены тегами.

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

### System.Management.Automation.SwitchParameter

## OUTPUTS

### Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[New-AzTag](./New-AzTag.md)

[Remove-AzTag](./Remove-AzTag.md)

[Update-AzTag](./Update-AzTag.md)
