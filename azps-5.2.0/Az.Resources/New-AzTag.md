---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
ms.openlocfilehash: 937ac50ac34f8b04912a0d500dedb5b490806b1a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414132"
---
# New-AzTag

## SYNOPSIS
Создание предопределеного тега Azure или сужит значения к существующему тегу | Создает или обновляет весь набор тегов для ресурса или подписки.

## СИНТАКСИС

### CreatePredefinedTagParameterSet

```powershell
New-AzTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### CreateByResourceIdParameterSet

```powershell
New-AzTag
   -ResourceId <String>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## ОПИСАНИЕ

**CreatePredefinedTagSet:** командлет **New-AzTag** создает готовый тег Azure с необязательным предопределительным значением.
С ее помощью также можно добавлять дополнительные значения к существующим предопределяемой метке.
Чтобы создать предопределный тег, введите уникальное имя тега.
Чтобы добавить значение к существующему предопределему тегу, укажите имя существующего и новое значение.
Этот командлет возвращает объект, который представляет новый или измененный тег со значениями и количеством ресурсов, к которым он был применен.
Модуль "Теги Azure", который входит в **состав тега New-AzTag,** помогает управлять предопределенами тегами Azure.
Тег Azure — это пара "имя-значение", которую можно использовать для классификации ресурсов и групп ресурсов Azure, например по отделам или центрам затрат, а также для отслеживания заметок и примечаний о ресурсах и группах.
Теги можно определять и применять в одном шаге, но предопределяемые теги помечают стандартные, согласованные, предсказуемые имена и значения для тегов в подписке.
Чтобы применить предопределяный тег к ресурсу или группе ресурсов, используйте параметр *"Тег"* New-AzTag командлета.
Для поиска групп ресурсов с указанным именем или именем и значением тега используйте параметр *Tag* Get-AzResourceGroup командлета.
У каждого тега есть имя.
Значения необязательны.
Предопределяемая метка Azure может иметь несколько значений, но при применении тега к ресурсу или группе ресурсов нужно применить имя тега и только одно из его значений.
Например, можно создать предопределный тег "Отдел" со значением для каждого отдела, например финансового, отдела кадров и ИТ-отдела.
При применении тега "Отдел" к ресурсу применяется только одно заранее задаированное значение, например "Финансы".

**CreateByResourceIdParameterSet:** командлет **New-AzTag** с **ResourceId** создает или обновляет весь набор тегов для ресурса или подписки.
Эта операция позволяет добавить или заменить весь набор тегов для указанного ресурса или подписки. Указанное лицо может иметь не более 50 тегов.

## ПРИМЕРЫ

### Пример 1. Создание предопределеного тега
```powershell
PS C:\>New-AzTag -Name "FY2015"
                                
Name   ValuesTable Count Values 
----   ----------- ----- ------
FY2015             0     {}
```

Эта команда создает предопределен тег с именем "ФГ2015".
Этот тег не имеет значений.
К ресурсу или группе ресурсов можно применить тег без значений или добавить к тегу значения с помощью **new-AzTag.**
Вы также можете указать значение при применении тега к ресурсу или группе ресурсов.

### Пример 2. Создание предопределеного тега со значением
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

Эта команда создает предопределный тег "Отдел" со значением "Финансы".

### Пример 3. Добавление значения к предопределему тегу
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0 
PS C:\>New-AzTag -Name "Department" -Value "IT"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0
        IT          0
```

Эти команды создают предопределяный тег "Отдел" с двумя значениями.
Если тег существует, **New-AzTag** добавляет значение к существующему тегу, а не создает новый.

### Пример 4. Использование предопределеного тега
```powershell
PS C:\>New-AzTag -Name "CostCenter" -Value "0001"
Name:   CostCenter
Count:  0
Values: 
        Name        Count
        =========   =====
        0001        0 
PS C:\>Set-AzResourceGroup -Name "EngineerBlog" -Tag @{Name="CostCenter";Value="0001"}
Name:      EngineerBlog
Location:  East US
Resources: 
            
  Name             Type                     Location
    ===============  =======================  ========
    EngineerBlog     Microsoft.Web/sites      West US
    EngSvr01         Microsoft.Sql/servers    West US
    EngDB02          Microsoft.Sql/databases  West US
Tags: 
    Name         Value
    ==========   =====
    CostCenter   0001 
PS C:\>Get-AzTag -Name "CostCenter"
Name:   CostCenter
Count:  1
Values: 
        Name        Count
        =========   =====
        0001        1 
PS C:\>Get-AzResourceGroup -Tag @{Name="CostCenter"}
Name:      EngineerBlog
Location:  East US
Resources: 
     Name             Type                     Location
    ===============  =======================  ========
    EngineerBlog     Microsoft.Web/sites      West US

    EngSvr01         Microsoft.Sql/servers    West US
    EngDB02          Microsoft.Sql/databases  West US
Tags: 
    Name         Value
    ==========   =====
    CostCenter   0001
```

С помощью команд в этом примере можно создать и использовать предопределяный тег.

### Пример 5. Создание или обновление всего набора тегов в подписке

```powershell
PS C:\>$Tags = @{"tagKey1"="tagValue1"; "tagKey2"="tagValue2"}
PS C:\>New-AzTag -ResourceId /subscriptions/{subId} -Tag $Tags

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             tagKey1  tagValue1
             tagKey2  tagValue2
```

Эта команда создает или обновляет весь набор тегов в подписке {subId}.

### Пример 6. Создание или обновление всего набора тегов для ресурса

```powershell
PS C:\>$Tags = @{"Dept"="Finance"; "Status"="Normal"}
PS C:\>New-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1 -Tag $Tags

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

Эта команда создает или обновляет весь набор тегов на ресурсе с помощью {resourceId}.

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
Определяет предопределное имя тега.
Чтобы создать новый предопределный тег, введите уникальное имя.
Чтобы добавить значение к существующему тегу, введите имя существующего тега.
Если имя существующего предопределяемого тега задано, **New-AzTag** добавляет указанное значение (если имеется) к тегу с этим именем, а не создает новый.

```yaml
Type: System.String
Parameter Sets: CreatePredefinedTagParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Value
Определяет заранее определенное значение тега.
Предопределять теги могут иметь несколько значений, но в каждой команде можно ввести только одно значение.
Этот параметр необязателен, так как теги могут иметь имена без значений.

```yaml
Type: System.String
Parameter Sets: CreatePredefinedTagParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Идентификатор ресурса для сущности, помеченной тегом. Ресурс, группа ресурсов или подписка могут быть помечены тегами.

```yaml
Type: System.String
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Теги, которые нужно поместить на ресурс.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: 1
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
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

### System.Collections.Hashtable

## OUTPUTS

### Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzTag](./Get-AzTag.md)

[Remove-AzTag](./Remove-AzTag.md)

[Update-AzTag](./Update-AzTag.md)