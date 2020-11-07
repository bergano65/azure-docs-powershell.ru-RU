---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Get-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Get-AzDnsZone.md
ms.openlocfilehash: fe650e87635d16d3768bd527bf7422fe644c885e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911236"
---
# Get-AzDnsZone

## КРАТКИй обзор
Возвращает зону DNS.

## Максимальное

### По умолчанию (по умолчанию)
```
Get-AzDnsZone [<CommonParameters>]
```

### Группа
```
Get-AzDnsZone [-Name <String>] -ResourceGroupName <String> [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzDnsZone** получает DNS-зону из заданной группы ресурсов.
Если указан параметр *Name* , возвращается один объект **dnsZone** .
Если параметр *Name* не указан, возвращается массив, содержащий все зоны в указанной группе ресурсов.
Вы можете использовать объект **dnsZone** , чтобы обновить зону, например добавить в нее объекты **набора записей** .

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение зоны
```
PS C:\> $Zone = Get-AzDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

В этом примере возвращается зона DNS с именем myzone.com из указанной группы ресурсов, а затем она сохраняется в переменной $Zone.

### Пример 2: получение всех зон в группе ресурсов
```
PS C:\> $Zones = Get-AzDnsZone -ResourceGroupName "MyResourceGroup"
```

В этом примере выполняется получение всех зон DNS в указанной группе ресурсов и их сохранение в переменной $Zones.

### Пример 3: получение всех зон в подписке
```
PS C:\> $Zones = Get-AzDnsZone
```

В этом примере выполняется получение всех зон DNS в текущей подписке Azure и их сохранение в переменной $Zones.

## ПАРАМЕТРЫ

### -Name (имя)
Указывает имя зоны DNS, которую требуется получить.

Если вы не укажете значение параметра *Name* , этот командлет получает все зоны DNS в указанной группе ресурсов.
Если параметр *ResourceGroupName* также опущен, этот командлет получает все зоны DNS в текущей подписке Azure.

```yaml
Type: String
Parameter Sets: ResourceGroup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов, содержащей зону DNS, которую требуется получить.

Если *ResourceGroupName* не указан, необходимо также опустить параметр *Name* .
В этом случае этот командлет получает все зоны DNS в текущей подписке Azure.

```yaml
Type: String
Parameter Sets: ResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего
Этот командлет не позволяет передавать входные данные.

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. DNS. DnsZone
Этот командлет возвращает объект, который представляет зону DNS.
Если имя зоны не задано, возвращается массив объектов зоны.

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[New-AzDnsZone](./New-AzDnsZone.md)

[Remove-AzDnsZone](./Remove-AzDnsZone.md)

[Set-AzDnsZone](./Set-AzDnsZone.md)
