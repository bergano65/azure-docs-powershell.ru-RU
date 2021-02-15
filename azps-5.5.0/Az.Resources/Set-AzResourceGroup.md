---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
ms.openlocfilehash: 0523041357becb38475bb496c94ba1fd48c5acaf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100217708"
---
# Set-AzResourceGroup

## SYNOPSIS
Изменяет группу ресурсов.

## СИНТАКСИС

### SetByResourceGroupName (по умолчанию)
```
Set-AzResourceGroup -Name <String> [-Tag] <Hashtable> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceGroupId
```
Set-AzResourceGroup [-Tag] <Hashtable> -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
При **этом свойства** группы ресурсов изменяется с их свойствами.
С помощью этого командлета можно добавлять, изменять и удалять теги Azure, примененные к группе ресурсов.
Укажите *параметр Name,* чтобы идентифицировать группу ресурсов, и параметр *Tag,* чтобы изменить теги.
С помощью этого cmdlet невозможно изменить имя группы ресурсов.

## ПРИМЕРЫ

### Пример 1. Применение тега к группе ресурсов
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

Эта команда применяет тег Department со значением ИТ для группы ресурсов, не имеющей тегов.

### Пример 2. Добавление тегов в группу ресурсов
```
PS C:\>$Tags = (Get-AzResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

В этом примере тег состояния со значением "Утверждено" и тегом "ФГ2016" добавляется в группу ресурсов, которая имеет теги. Поскольку эти теги заменяют существующие, необходимо включить существующие теги в новую коллекцию тегов или потерять их.
Первая команда получает группу ресурсов ContosoRG и использует метод точки, чтобы получить значение свойства "Теги". Команда сохраняет теги в переменной $Tags.
Вторая команда получает теги в переменной $Tags.
Третья команда использует оператор назначения += для добавления тегов состояния и FY2016 в массив тегов в переменной $Tags.
Четвертая команда использует параметр *Tag* группы **Set-AzResourceGroup** для применения тегов переменной $Tags к группе ресурсов ContosoRG.
Пятая команда получает все теги, примененные к группе ресурсов ContosoRG. Выходные данные показывают, что группа ресурсов имеет тег "Отдел" и два новых тега: "Состояние" и "ФГ2015".

### Пример 3. Удаление всех тегов для группы ресурсов
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{}
```

Эта команда определяет параметр *Tag* с пустым значением для hash table, чтобы удалить все теги из группы ресурсов ContosoRG.

## PARAMETERS

### -ApiVersion
Указывает версию API, которая поддерживается поставщиком ресурсов.
Можно указать другую версию, чем версия по умолчанию.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -Id
Определяет код группы ресурсов, который нужно изменить.

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Имя группы ресурсов, которая будет изменяться.

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre
Указывает на то, что этот cmdlet рассматривает предварительные версии API при автоматическом определении используемой версии.

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

### -Tag
Пары "ключевое значение" в виде hash table. Например: @{key0="value0";key1=$null;key2="value2"} Тег — это пара "имя-значение", которую можно создать и применить к ресурсам и группам ресурсов. После назначения тегов ресурсам и группам можно  использовать параметр "Тег" в Get-AzResource и Get-AzResourceGroup для поиска ресурсов и групп по имени или имени и значению тега. С помощью тегов можно классифицировать ресурсы,например по отделам или затратам, а также для отслеживания заметок и примечаний к ресурсам.
Чтобы добавить или изменить тег, необходимо заменить коллекцию тегов для группы ресурсов. Чтобы удалить тег, введите в качестве тега из **Get-AzResourceGroup** таблицу со всеми тегами, которые в данный момент применены к группе ресурсов, кроме тега, который вы хотите удалить. Чтобы удалить все теги из группы ресурсов, укажите пустую `@{}` таблицу:

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

### System.Collections.Hashtable

## OUTPUTS

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzResource](./Get-AzResource.md)

[Get-AzResourceGroup](./Get-AzResourceGroup.md)

[New-AzResourceGroup](./New-AzResourceGroup.md)

[Remove-AzResourceGroup](./Remove-AzResourceGroup.md)
