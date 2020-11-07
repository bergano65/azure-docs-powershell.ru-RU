---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-Azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzResourceGroup.md
ms.openlocfilehash: d645f430c21a1e9675a0f356cffacbad6a7b5740
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910818"
---
# Set-AzResourceGroup

## КРАТКИй обзор
Изменяет группу ресурсов.

## Максимальное

### SetByResourceGroupName (по умолчанию)
```
Set-AzResourceGroup [-Name] <String> [-Tag] <Hashtable> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceGroupId
```
Set-AzResourceGroup [-Tag] <Hashtable> [-Id] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzResourceGroup** изменяет свойства группы ресурсов.
Вы можете использовать этот командлет для добавления, изменения или удаления тегов Azure, примененных к группе ресурсов.
Укажите параметр *Name (имя* ), чтобы определить группу ресурсов и параметр *Tag* , чтобы изменить теги.
Вы не можете использовать этот командлет для изменения имени группы ресурсов.

## ИЛЛЮСТРИРУЮТ

### Пример 1: применение тега к группе ресурсов
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

Эта команда применяет к группе ресурсов тег подразделения со значением, не имеющей существующих тегов.

### Пример 2: Добавление тегов в группу ресурсов
```
PS C:\>$Tags = (Get-AzResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

В этом примере в группу ресурсов, имеющую существующие теги, добавляется тег Status со значением утвержденный и тег FY2016. Так как указанные Теги заменяют существующие теги, необходимо включить существующие теги в новую коллекцию тегов, иначе они будут потеряны.
Первая команда получает группу ресурсов ContosoRG и использует метод Dot для получения значения свойства Tags. Команды хранят теги в переменной $Tags.
Вторая команда получает теги в переменной $Tags.
Третья команда использует оператор присваивания + = для добавления тегов status и FY2016 в массив тегов в переменной $Tags.
Четвертая команда использует параметр *Tag* для **Set-AzResourceGroup** , чтобы применить теги в переменной $Tags к группе ресурсов ContosoRG.
Пятая команда получает все теги, примененные к группе ресурсов ContosoRG. В выходных данных показано, что группа ресурсов содержит тег отдела и два новых тега, Status и FY2015.

### Пример 3: удаление всех тегов для группы ресурсов
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{}
```

Эта команда задает параметр *тега* с пустым значением хэш-таблицы для удаления всех тегов из группы ресурсов ContosoRG.

## ПАРАМЕТРЫ

### -ApiVersion
Указывает версию API, поддерживаемую поставщиком ресурсов.
Вы можете выбрать версию, отличную от версии по умолчанию.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Указывает идентификатор группы ресурсов, которую нужно изменить.

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (имя)
Указывает имя группы ресурсов, которую нужно изменить.

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre
Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.

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

### -Тег
Пары "ключ-значение" в виде хэш-таблицы. Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"} тег — это пара "имя-значение", которую можно создать и применить к ресурсам и группам ресурсов. После того как вы назначьте Теги ресурсам и группам, вы можете использовать параметр *Tag* Get-AzResource и Get-AzResourceGroup для поиска ресурсов и групп по имени или имени и значению тега. Теги можно использовать для классификации ресурсов, таких как отдел или центр затрат, а также для отслеживания заметок и примечаний к ресурсам.
Чтобы добавить или изменить тег, необходимо заменить коллекцию тегов для группы ресурсов. Чтобы удалить тег, введите хэш-таблицу со всеми тегами, которые в настоящее время применены к группе ресурсов из **Get-AzResourceGroup** , за исключением тега, который вы хотите удалить. Чтобы удалить все теги из группы ресурсов, укажите пустую хэш- `@{}` таблицу.

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Resources. PSResourceGroup

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzResource](./Get-AzResource.md)

[Get-AzResourceGroup](./Get-AzResourceGroup.md)

[New-AzResourceGroup](./New-AzResourceGroup.md)

[Remove-AzResourceGroup](./Remove-AzResourceGroup.md)
