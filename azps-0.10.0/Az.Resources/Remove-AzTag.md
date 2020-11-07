---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzTag.md
ms.openlocfilehash: 5b7e58545b2c463c08a961758ecdb3cbce7b222c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910836"
---
# Remove-AzTag

## КРАТКИй обзор
Удаляет предопределенные теги или значения Azure.

## Максимальное

```
Remove-AzTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Remove-AzTag** удаляет из подписки предопределенные Теги и значения Azure.
Для удаления определенных значений из предопределенного тега используйте параметр *value* .
По умолчанию **Remove-AzTag** удаляет указанный тег и все его значения. Вы не можете удалить тег или значение, которые в настоящее время применены к ресурсам или группам ресурсов.
Перед использованием **Remove-AzTag** используйте параметр *Tag* командлета Set-AzResourceGroup для удаления тега или значений из ресурса или группы ресурсов.
Модуль тегов Azure, который **Remove-AzTag** является частью, может помочь вам управлять предопределенными тегами Azure.
Тег Azure — это пара "имя-значение", которую можно использовать для классификации ресурсов и групп ресурсов Azure, таких как отдел или центр затрат, а также для отслеживания заметок и примечаний к ресурсам и группам.
Вы можете определять и применять теги за один шаг, но стандартные теги позволяют устанавливать стандартные, противоречивые и предсказуемые имена и значения для тегов в вашей подписке.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Удаление предопределенного тега
```
PS C:\>Remove-AzTag -Name "Department"
```

Эта команда удаляет предопределенный тег с именем Department и все его значения.
Если тег применен к ресурсам или группам ресурсов, команда не выполняется.

### Пример 2: Удаление значения из предопределенного тега
```
PS C:\>Remove-AzTag -Name "Department" -Value "HumanResources" -PassThru
Name:   Department
Count:  14
Values: 

        Name        Count
        =========   =====

        Finance        2
        IT            12
```

Эта команда удаляет значение HumanResources из предопределенного тега отдела.
Тег не удаляется.
Если значение было применено к ресурсам или группам ресурсов, команда завершится сбоем.

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
Указывает имя тега, который нужно удалить.
По умолчанию **Remove-AzTag** удаляет указанный тег и все его значения.
Чтобы удалить выделенные значения, но не удалять тег, используйте параметр *value* .

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

### -PassThru
Возвращает объект, который представляет удаленный тег или получившийся тег с удаленным значением.

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

### -Value (значение)
Удаляет указанные значения из предопределенного тега, но не удаляет тег.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String

### System. String []

### System. Management. Automation. SwitchParameter

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzTag](./Get-AzTag.md)

[New-AzTag](./New-AzTag.md)

