---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzTag.md
ms.openlocfilehash: 242f207faa98c6165e4c64f095f9b171f1d72d5c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910885"
---
# New-AzTag

## КРАТКИй обзор
Создает предопределенный тег Azure или добавляет значения в существующий тег.

## Максимальное

```
New-AzTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzTag** создает предопределенный тег Azure с необязательным предварительно заданным значением.
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

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание предопределенного тега
```
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
```
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
```
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
```
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
Указывает имя тега.
Чтобы создать новый предопределенный тег, введите уникальное имя.
Чтобы добавить значение в существующий тег, введите имя существующего тега.
Если существующий предопределенный тег имеет указанное имя, **New-AzTag** добавляет указанное значение, если оно есть, в тег с этим именем вместо создания нового тега.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Value (значение)
Задает значение тега.
Предопределенные Теги могут содержать несколько значений, но в каждой из них можно вводить только одно значение.
Этот параметр является необязательным, поскольку теги могут иметь имена без значений.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzTag](./Get-AzTag.md)

[Remove-AzTag](./Remove-AzTag.md)

