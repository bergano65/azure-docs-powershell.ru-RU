---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
ms.openlocfilehash: 176328452c123c3d3cada88940efcdadf88943e0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912165"
---
# New-AzTag

## КРАТКИй обзор
Создание предопределенного тега Azure или добавление значений в существующий тег | Создает или обновляет весь набор тегов на ресурсе или подписке.

## Максимальное

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

## NОПИСАНИЕ

**CreatePredefinedTagSet** : командлет **New-AzTag** создает предопределенный тег Azure с необязательным предварительно заданным значением.
Кроме того, с ее помощью можно добавлять дополнительные значения для существующих предопределенных тегов.
Чтобы создать предопределенный тег, введите уникальное имя тега.
Чтобы добавить значение в существующий предопределенный тег, укажите имя существующего тега и новое значение.
Этот командлет возвращает объект, который представляет новый или измененный тег со значениями и количеством ресурсов, к которым он был применен.
Модуль тегов Azure, частью которого является **New-AzTag** , может помочь вам управлять стандартными тегами Azure.
Тег Azure — это пара "имя-значение", которую можно использовать для классификации ресурсов и групп ресурсов Azure, таких как отдел или центр затрат, а также для отслеживания заметок и примечаний к ресурсам и группам.
Вы можете определять и применять теги за один шаг, но стандартные теги позволяют устанавливать стандартные, противоречивые и предсказуемые имена и значения для тегов в вашей подписке.
Чтобы применить предопределенный тег к ресурсу или группе ресурсов, используйте параметр *Tag* командлета New-AzTag.
Чтобы найти группы ресурсов с указанным именем тега или именем и значением, используйте параметр *Tag* для командлета Get-AzResourceGroup.
Каждый тег имеет имя.
Значения не являются обязательными.
Предопределенный тег Azure может иметь несколько значений, но при применении тега к ресурсу или группе ресурсов следует применять имя тега и только одно из его значений.
Например, вы можете создать готовый тег отдела со значением для каждого отдела, например "Финансы", "Отдел кадров" и т. д.
Когда вы примените к ресурсу тег отдела, вы можете применить только одно предопределенное значение, например "процент".

**CreateByResourceIdParameterSet** : командлет **New-AzTag** с **ResourceId** создает или обновляет весь набор тегов на ресурсе или подписке.
Эта операция позволяет добавить или заменить весь набор тегов в указанном ресурсе или подписке. Для указанной сущности может быть не более 50 тегов.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание предопределенного тега
```powershell
PS C:\>New-AzTag -Name "FY2015"
                                
Name   ValuesTable Count Values 
----   ----------- ----- ------
FY2015             0     {}
```

Эта команда создает предопределенный тег с именем FY2015.
У этого тега нет значений.
Вы можете применить к ресурсу или группе ресурсов тег без значений или использовать **New-AzTag** для добавления значений в тег.
Вы также можете указать значение при применении тега к ресурсу или группе ресурсов.

### Пример 2: создание предопределенного тега со значением
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

Эта команда создает предопределенный тег с именем Department и значением Finance.

### Пример 3: Добавление значения к стандартному тегу
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

Эти команды создают предопределенный тег отдела с двумя значениями.
Если имя тега существует, **New-AzTag** добавляет значение в существующий тег вместо создания нового.

### Пример 4: использование предопределенного тега
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

В этом примере команды создают и используют предопределенный тег.

### Пример 5: создание или обновление всего набора тегов в подписке

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

Эта команда создает или обновляет весь набор тегов в подписке с помощью {subId}.

### Пример 6: создание или обновление всего набора тегов на ресурсе

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

Эта команда создает или обновляет весь набор тегов в ресурсе с помощью {resourceId}.

## ПАРАМЕТРЫ

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

### -Name (имя)
Задает предопределенное имя тега.
Чтобы создать новый предопределенный тег, введите уникальное имя.
Чтобы добавить значение в существующий тег, введите имя существующего тега.
Если существующий предопределенный тег имеет указанное имя, **New-AzTag** добавляет указанное значение, если оно есть, в тег с этим именем вместо создания нового тега.

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

### -Value (значение)
Задает предварительно определенное значение тега.
Предопределенные Теги могут содержать несколько значений, но в каждой из них можно вводить только одно значение.
Этот параметр является необязательным, поскольку теги могут иметь имена без значений.

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
Идентификатор ресурса для сущности, на которую размещается тег. Ресурс, Группа ресурсов или подписка может быть помечены.

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

### -Тег
Теги, помещаемые в ресурс.

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
Запрашивает подтверждение перед запуском командлета.

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
Показывает, что произойдет при запуске командлета.
Командлет не выполняется.

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## ВХОДНЫЕ данные

### System. String

### System. Collections. Hashtable

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag | Microsoft. Azure. Commands. Tags. Model. PSTagResource

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzTag](./Get-AzTag.md)

[Remove-AzTag](./Remove-AzTag.md)

[Update-AzTag](./Update-AzTag.md)
