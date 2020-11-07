---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/set-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Set-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Set-AzDnsZone.md
ms.openlocfilehash: 9b6d84f9007a872db0e41efa78d8e16d7269eb02
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910415"
---
# Set-AzDnsZone

## КРАТКИй обзор
Обновление свойств зоны DNS.

## Максимальное

### »
```
Set-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### DataObject
```
Set-AzDnsZone -Zone <DnsZone> [-Overwrite] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzDnsZone** обновляет указанную зону DNS в службе Azure DNS.
Этот командлет не обновляет наборы записей в зоне.

Вы можете передать объект **dnsZone** как параметр или с помощью оператора конвейера или указать параметры *zonename* и *ResourceGroupName* .

Вы можете использовать параметр *Confirm* и $ConfirmPreference переменной Windows PowerShell, чтобы указать, нужно ли командлету запрашивать подтверждение.

Если зона DNS была передана как объект (с помощью объекта Zone или канала), она не будет обновлена, если она была изменена в службе DNS Azure, поскольку был получен локальный объект DnsZone. Это обеспечивает защиту для параллельных изменений. Вы можете отключить это поведение с параметром *перезаписи* , который обновляет зону независимо от текущих изменений.

## ИЛЛЮСТРИРУЮТ

### Пример 1: обновление зоны DNS
```
PS C:\>$Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzDnsZone -Zone $Zone
```

Первая команда получает зону с именем myzone.com из указанной группы ресурсов, а затем сохраняет ее в переменной $Zone.

Вторая команда обновляет теги для $Zone.

Последняя команда фиксирует изменения.

### Пример 2: обновление тегов для зоны
```
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

Эта команда обновляет теги для зоны с именем myzone.com, но сначала явно не получает зону.

## ПАРАМЕТРЫ

### -Name (имя)
Указывает имя DNS-зоны, которую нужно обновить.

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
Если зона DNS была передана как объект (с помощью объекта Zone или канала), она не будет обновлена, если она была изменена в службе DNS Azure, поскольку был получен локальный объект DnsZone. Это обеспечивает защиту для параллельных изменений. Вы можете отключить это поведение с параметром *перезаписи* , который обновляет зону независимо от текущих изменений.

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

### -ResourceGroupName
Указывает имя группы ресурсов, содержащей зону для обновления.
Кроме того, необходимо указать параметр ZoneName.

Кроме того, вы можете указать зону, используя объект DnsZone с параметром *зоны* или конвейером.

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

### -Тег
Пары "ключ-значение" в виде хэш-таблицы. Например:

@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}

```yaml
Type: Hashtable
Parameter Sets: Fields
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
Указывает зону DNS для обновления.

Кроме того, вы можете указать зону с помощью параметров *zonename* и *ResourceGroupName* .

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
Показывает, что произойдет при запуске командлета. Командлет не выполняется. Показывает, что произойдет при запуске командлета. Командлет не выполняется.

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
Вы можете передать на этот командлет объект DnsZone.

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. DNS. DnsZone
Этот командлет возвращает объект DnsZone, который представляет обновленную зону DNS с новым тегом ETag.

## Пуск
Вы можете использовать параметр *Confirm* , чтобы указать, будет ли этот командлет запрашивать подтверждение.
По умолчанию командлет запрашивает подтверждение, если значение переменной $ConfirmPreference Windows PowerShell — средний или ниже.

Если вы задаете параметр *Confirm* или *Confirm: $true* , этот командлет запрашивает подтверждение перед запуском.
Если вы задаете значение *Confirm: $false* , командлет не будет запрашивать подтверждение.

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzDnsZone](./Get-AzDnsZone.md)

[New-AzDnsZone](./New-AzDnsZone.md)

[Remove-AzDnsZone](./Remove-AzDnsZone.md)