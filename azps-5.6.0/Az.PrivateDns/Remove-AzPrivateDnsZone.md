---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/powershell/module/az.privatedns/remove-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
ms.openlocfilehash: 8c8e7059a6c23c928180b8d6fab3cfdbbfd9ed5d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970408"
---
# Remove-AzPrivateDnsZone

## SYNOPSIS
Удаляет частную зону DNS из группы ресурсов.

## СИНТАКСИС

### Поля (по умолчанию)
```
Remove-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Объект
```
Remove-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceId
```
Remove-AzPrivateDnsZone -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## ОПИСАНИЕ
**Cmdlet Remove-AzPrivateDnsZone** окончательно удаляет частную зону службы доменных имен (DNS) из указанной группы ресурсов.
Все наборы записей, содержащиеся в зоне, также удаляются.
Передать объект **PrivateDnsZone** можно с помощью параметра *PrivateZone* или с помощью оператора конвейера. Кроме того, можно указать параметры *Name* и *ResourceGroupName.*
Параметр Confirm и переменная $ConfirmPreference Windows PowerShell можно использовать для управления запросом на подтверждение с помощью cmdlet.
При указании зоны с использованием объекта **PrivateDnsZone** (передается через канал или параметр зоны), она не удаляется, если она была изменена в Azure DNS после извлечения локального объекта **PrivateDnsZone** (только операции непосредственно в подсчете ресурсов зоны DNS в качестве изменений, операции с наборами записей в зоне не учитываются). 
Это обеспечивает защиту при одновременном смене зоны.
Это можно сделать с помощью параметра *Overwrite,* который удаляет зону независимо от одновременного изменения.

## ПРИМЕРЫ

### Пример 1. Удаление закрытой зоны
```
PS C:\>Remove-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

Эта команда удаляет зону с именем myzone.com из группы ресурсов MyResourceGroup.

## PARAMETERS

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

### -Name
Указывает имя закрытой зоны DNS, которую удаляет этот cmdlet.
Необходимо также указать параметр *ResourceGroupName.*
Кроме того, вы можете указать зону DNS с помощью *параметра Zone.*

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Overwrite
При указании зоны с использованием объекта **PrivateDnsZone** (передается через канал или параметр зоны), она не удаляется, если она была изменена в Azure DNS с момента извлечения локального объекта **PrivateDnsZone** (только операции непосредственно в подсчете ресурсов зоны DNS в качестве изменений, операции с наборами записей в зоне не учитываются). 
Это обеспечивает защиту при одновременном смене зоны.
Это можно сделать с помощью параметра *Overwrite,* который удаляет зону независимо от одновременного изменения.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Используется для передачи результата (boolean) операции удаления частной зоны далее по конвейеру.

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

### -PrivateZone
Объект закрытой зоны, который нужно удалить.

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов, которая содержит удаляемую зону.
Необходимо также указать *параметр ZoneName.*
Кроме того, вы можете указать зону DNS с помощью объекта **PrivateDnsZone,** переданного через канал или параметр *зоны.*

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Private DNS Zone ResourceID.

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
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
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone

### System.String

## OUTPUTS

### System.Boolean

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzPrivateDnsZone](./Get-AzPrivateDnsZone.md)

[New-AzPrivateDnsZone](./New-AzPrivateDnsZone.md)

[Set-AzPrivateDnsZone](./Set-AzPrivateDnsZone.md)
