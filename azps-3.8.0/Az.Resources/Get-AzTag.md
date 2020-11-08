---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
ms.openlocfilehash: 058f4a61f1e7ff2fe7f416ea0e4ada098c9efe51
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073780"
---
# Get-AzTag

## КРАТКИй обзор
Получает предопределенные Теги Azure | Возвращает весь набор тегов на ресурсе или в подписке.

## Максимальное

### GetPredefinedTagParameterSet
```
Get-AzTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceIdParameterSet
```
Get-AzTag -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ

**GetPredefinedTagSet** : командлет **Get-AzTag** получает предопределенные Теги Azure в вашей подписке.
Этот командлет возвращает основные сведения о тегах и подробное описание тегов и их значений.
Все выходные объекты включают свойство Count, представляющее количество ресурсов и групп ресурсов, к которым применены теги и значения.
Модуль тегов Azure, с помощью **Get-AzTag** , — это часть, которая может помочь вам управлять предопределенными тегами Azure.
Тег Azure — это пара "имя-значение", которую можно использовать для классификации ресурсов и групп ресурсов Azure, таких как отдел или центр затрат, а также для отслеживания заметок и примечаний к ресурсам и группам.
Вы можете определять и применять теги за один шаг, но стандартные теги позволяют устанавливать стандартные, противоречивые и предсказуемые имена и значения для тегов в вашей подписке.
Чтобы создать предопределенный тег, используйте командлет New-AzTag.
Чтобы применить предопределенный тег к группе ресурсов, используйте параметр *Tag* командлета New-AzTag.
Для поиска групп ресурсов с определенным именем тега или именем и значением используйте параметр *Tag* для командлета Get-AzResourceGroup.

**GetByResourceIdParameterSet** : командлет **Get-AzTag** с **ResourceId** получает полный набор тегов для ресурса или подписки.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение всех стандартных тегов
```powershell
PS C:\>Get-AzTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

Эта команда получает все предопределенные теги в подписке.
Свойство Count показывает, сколько вхождений тега применено к ресурсам и группам ресурсов в подписке.

### Пример 2: получение тега по имени
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

Эта команда получает подробные сведения о теге отдела и его значениях.
Свойство Count показывает, сколько вхождений тега и каждого из его значений применено к ресурсам и группам ресурсов в подписке.

### Пример 3: получение значений всех тегов
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

Эта команда использует *подробный* параметр для получения подробных сведений обо всех предопределенных тегах в подписке.
Параметр *Detailed* является эквивалентом использования параметра *Name* для каждого тега.

### Пример 4: получение всего набора тегов в подписке

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

Эта команда возвращает весь набор тегов в подписке с помощью {subId}.

### Пример 5: получение всего набора тегов на ресурсе

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

Эта команда возвращает весь набор тегов для ресурса с {resourceId}.

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

### -Подробно
Указывает на то, что при выполнении этой операции в выходных данных добавляются сведения о значениях тегов.

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

### -Name (имя)
Имя предопределенного тега.
По умолчанию **Get-AzTag** получает основные сведения обо всех предопределенных тегах в подписке.
При указании параметра *Name* *подробный* параметр не действует.

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
Идентификатор ресурса для помеченной сущности. Ресурс, Группа ресурсов или подписка может быть помечены.

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## ВХОДНЫЕ данные

### System. String

### System. Management. Automation. SwitchParameter

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag | Microsoft. Azure. Commands. Tags. Model. PSTagResource

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[New-AzTag](./New-AzTag.md)

[Remove-AzTag](./Remove-AzTag.md)

[Update-AzTag](./Update-AzTag.md)
