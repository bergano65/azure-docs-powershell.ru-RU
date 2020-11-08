---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 07c6e327-05f4-4279-a5fb-d4e860c897d4
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzTag.md
ms.openlocfilehash: 4adda2affcba1c29352f6fe9235a5f10a3c1382a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94234774"
---
# Update-AzTag

## КРАТКИй обзор

Выборочно обновляет набор тегов на ресурсе или в подписке.

## Максимальное

```powershell
Update-AzTag
   -ResourceId <String>
   -Operation <TagPatchOpeation>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]

```

## NОПИСАНИЕ

Командлет **Update-AzTag** с **ResourceId** , который выборочно обновляет набор тегов на ресурсе или подписке.
Эта операция позволяет заменять, объединять или выборочно удалять теги в указанном ресурсе или подписке. В конце операции для указанной сущности может быть не более 50 тегов. Параметр "заменить" заменяет весь набор существующих тегов новым набором. С помощью параметра "слияние" можно добавлять теги с новыми именами и обновлять значения тегов с существующими именами. Параметр "Удалить" позволяет выборочно удалять теги, основанные на указанных именах или парах "имя-значение".

## ИЛЛЮСТРИРУЮТ

### Пример 1: выборочное обновление набора тегов в подписке с помощью операции "слияние"

```powershell
PS C:\>$mergedTags = @{"key1"="value1"; "key3"="value3";}
PS C:\>Update-AzTag -ResourceId /subscriptions/{subId} -Tag $mergedTags -Operation Merge

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             key1     value1
             key2     value2
             key3     value3
```

Эта команда объединяет набор тегов в подписке с помощью {subId}.

### Пример 2: выборочное обновление набора тегов в подписке с помощью операции "заменить"

```powershell
PS C:\>$replacedTags = @{"key1"="value1"; "key3"="value3";}
PS C:\>Update-AzTag -ResourceId /subscriptions/{subId} -Tag $replacedTags -Operation Replace

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             key1     value1
             key3     value3
```

Эта команда Repalces набор тегов в подписке с помощью {subId}.

### Пример 3: выборочное обновление набора тегов в подписке с помощью операции "Удалить"

```powershell
PS C:\>$deletedTags = @{"key1"="value1"}
PS C:\>Update-AzTag -ResourceId /subscriptions/{subId} -Tag $deletedTags -Operation Delete

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             key3     value3
```

Эта команда удаляет набор тегов в подписке с помощью {subId}.

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

### -ResourceId
Идентификатор ресурса для помеченной сущности. Ресурс, Группа ресурсов или подписка может быть помечены.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Merge, Replace, Delete

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Тег
Набор тегов, которые нужно использовать для обновления.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Эксплуатация
Операция обновления. Параметры можно объединять, заменять и удалять.

```yaml
Type: Microsoft.Azure.Commands.Tags.Model.TagPatchOpeation
Parameter Sets: (All)
Aliases:
Accepted values: Merge, Replace, Delete

Required: True
Position: 2
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

### Microsoft. Azure. Commands. Tags. Model. TagPatchOpeation

### System. Collections. Hashtable

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Tags. Model. PSTagResource

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzTag](./Get-AzTag.md)

[New-AzTag](./New-AzTag.md)

[Remove-AzTag](./Remove-AzTag.md)
