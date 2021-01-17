---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsZone.md
ms.openlocfilehash: 633a71788bb9578438053f7a296422e99e7c488e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402327"
---
# Remove-AzDnsZone

## SYNOPSIS
Удаляет зону DNS из группы ресурсов.

## СИНТАКСИС

### Поля
```
Remove-AzDnsZone -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Объект
```
Remove-AzDnsZone -Zone <DnsZone> [-Overwrite] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## ОПИСАНИЕ
**Cmdlet Remove-AzDnsZone** окончательно удаляет зону службы доменных имен (DNS) из указанной группы ресурсов.
Все наборы записей, содержащиеся в зоне, также удаляются.
Передать объект **DnsZone** можно с помощью параметра *Name* или с помощью оператора конвейера. Кроме того, можно указать параметры *ZoneName* и *ResourceGroupName.*
Параметр Confirm и переменная $ConfirmPreference Windows PowerShell можно использовать для управления запросом на подтверждение с помощью cmdlet.
При указании зоны с использованием объекта **DnsZone** (передается через канал или параметр зоны), она не удаляется, если она была изменена в Azure DNS после извлечения локального объекта  **DnsZone** (только операции непосредственно в подсчете ресурсов зоны DNS в качестве изменений, операции с наборами записей в зоне не учитываются).
Это обеспечивает защиту при одновременном смене зоны.
Это можно сделать с помощью параметра *Overwrite,* который удаляет зону независимо от одновременного изменения.

## ПРИМЕРЫ

### Пример 1. Удаление зоны
```
PS C:\>Remove-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
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
Указывает имя зоны DNS, которую удаляет этот cmdlet.
Необходимо также указать параметр *ResourceGroupName.*
Кроме того, вы можете указать зону DNS с помощью *параметра Zone.*

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Overwrite
При указании зоны с использованием объекта **DnsZone** (передается через канал или параметр зоны), она не удаляется, если она была изменена в Azure DNS после извлечения локального объекта  **DnsZone** (только операции непосредственно в подсчете ресурсов зоны DNS в качестве изменений, операции с наборами записей в зоне не учитываются).
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
passthru

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

### -ResourceGroupName
Имя группы ресурсов, которая содержит удаляемую зону.
Необходимо также указать *параметр ZoneName.*
Кроме того, вы можете указать зону DNS с помощью объекта **DnsZone,** переданного через канал или *параметр Zone.*

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
Определяет зону DNS, которая нужно удалить.
Переданный **объект DnsZone** также можно передать через конвейер.
Вы также можете указать зону DNS, которая будет удалена, с помощью параметров *ZoneName* и *ResourceGroupName.*

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Confirm
Запрос на подтверждение перед запуском cmdlet.

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

### System.String

### Microsoft.Azure.Commands.Dns.DnsZone

## OUTPUTS

### System.Boolean

## ПРИМЕЧАНИЯ
В связи с потенциально высоким влиянием удаления зоны DNS по умолчанию этот $ConfirmPreference Windows PowerShell запросит подтверждение.
Если указать *"Подтвердить"* или *"$True:$True",* этот cmdlet запросит подтверждение перед запуском.
Если *указать confirm:$False,* то при этом не будет предложено подтвердить запрос. 

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzDnsZone](./Get-AzDnsZone.md)

[New-AzDnsZone](./New-AzDnsZone.md)

[Set-AzDnsZone](./Set-AzDnsZone.md)
