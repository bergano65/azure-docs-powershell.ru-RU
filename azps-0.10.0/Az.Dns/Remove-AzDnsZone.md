---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Remove-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Remove-AzDnsZone.md
ms.openlocfilehash: bc77e2c69f285f0acab0bed8e6a40592374ebd18
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910420"
---
# Remove-AzDnsZone

## КРАТКИй обзор
Удаляет зону DNS из группы ресурсов.

## Максимальное

### »
```
Remove-AzDnsZone -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### DataObject
```
Remove-AzDnsZone -Zone <DnsZone> [-Overwrite] [-Force] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Remove-AzDnsZone** окончательно УДАЛЯЕТ зону DNS из определенной группы ресурсов.
Все наборы записей, содержащиеся в зоне, также удаляются.

Вы можете передать объект **dnsZone** с помощью параметра *Name* или оператора Pipeline либо указать параметры *zonename* и *ResourceGroupName* .

Вы можете использовать параметр Confirm и $ConfirmPreference переменной Windows PowerShell, чтобы указать, нужно ли командлету запрашивать подтверждение.

При указании зоны с помощью объекта **dnsZone** (который передается через конвейер или параметр *зоны* ) зона не удаляется, если она была изменена в Azure DNS, так как изменялись данные локального объекта **dnsZone** (операции с наборами записей в зоне не изменяются).
Это обеспечивает защиту для одновременных изменений зоны.
Это может быть подавлено с помощью параметра *overwrite* , что приводит к удалению зоны независимо от текущих изменений.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Удаление зоны
```
PS C:\>Remove-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

Эта команда удаляет зону с именем myzone.com из группы ресурсов с именем MyResourceGroup.

## ПАРАМЕТРЫ

### -Force
Этот параметр устарел для этого командлета.
Оно будет удалено в следующем выпуске.

Чтобы указать, будет ли этот командлет запрашивать подтверждение, используйте параметр *Confirm* .

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (имя)
Указывает имя DNS-зоны, которую удаляет этот командлет.
Кроме того, необходимо указать параметр *ResourceGroupName* .

Кроме того, вы можете указать зону DNS с помощью параметра *Zone* .

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Overwrite
При указании зоны с помощью объекта **dnsZone** (который передается через конвейер или параметр *зоны* ) зона не удаляется, если она была изменена в Azure DNS, так как изменялись данные локального объекта **dnsZone** (операции с наборами записей в зоне не изменяются).
Это обеспечивает защиту для одновременных изменений зоны.

Это может быть подавлено с помощью параметра *overwrite* , что приводит к удалению зоны независимо от текущих изменений.

```yaml
Type: SwitchParameter
Parameter Sets: Object
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
PassThru

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов, содержащей зону, которую нужно удалить.
Кроме того, необходимо указать параметр *zonename* .

Кроме того, вы можете указать зону DNS с помощью объекта **dnsZone** , передаваемого через конвейер или параметр *Zone* .

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
Указывает зону DNS для удаления.
Переданный объект **dnsZone** также можно передать через конвейер.

Кроме того, вы можете указать зону DNS для удаления с помощью параметров *zonename* и *ResourceGroupName* .

```yaml
Type: DnsZone
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Confirm
Запрашивает подтверждение перед запуском командлета.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
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

### Microsoft. Azure. Commands. DNS. DnsZone
Вы можете передать на этот командлет объект **dnsZone** .

## НАПРЯЖЕНИЕ

### Ничего
Этот командлет не создает никаких выходных данных.

## Пуск
Из-за потенциально высокого воздействия на удаление зоны DNS по умолчанию этот командлет запрашивает подтверждение, если переменная $ConfirmPreference Windows PowerShell имеет любое значение, отличное от None.

Если вы задаете параметр *Confirm* или *Confirm: $true* , этот командлет запрашивает подтверждение перед запуском.
Если вы задаете значение *Confirm: $false* , командлет не будет запрашивать подтверждение. 

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzDnsZone](./Get-AzDnsZone.md)

[New-AzDnsZone](./New-AzDnsZone.md)

[Set-AzDnsZone](./Set-AzDnsZone.md)
