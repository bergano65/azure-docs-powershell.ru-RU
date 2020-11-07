---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8b71c522a8d4dc006428ca2a400160a0ce7ce68b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914486"
---
# Get-AzureRmDnsZone

## КРАТКИй обзор
Возвращает зону DNS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### По умолчанию (по умолчанию)
```
Get-AzureRmDnsZone [<CommonParameters>]
```

### Группа
```
Get-AzureRmDnsZone [-Name <String>] -ResourceGroupName <String> [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmDnsZone** получает DNS-зону из заданной группы ресурсов.
Если указан параметр *Name* , возвращается один объект **dnsZone** .
Если параметр *Name* не указан, возвращается массив, содержащий все зоны в указанной группе ресурсов.
Вы можете использовать объект **dnsZone** , чтобы обновить зону, например добавить в нее объекты **набора записей** .

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение зоны
```
PS C:\> $Zone = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

В этом примере возвращается зона DNS с именем myzone.com из указанной группы ресурсов, а затем она сохраняется в переменной $Zone.

### Пример 2: получение всех зон в группе ресурсов
```
PS C:\> $Zones = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup"
```

В этом примере выполняется получение всех зон DNS в указанной группе ресурсов и их сохранение в переменной $Zones.

### Пример 3: получение всех зон в подписке
```
PS C:\> $Zones = Get-AzureRmDnsZone
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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего
Этот командлет не позволяет передавать входные данные.

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. DNS. DnsZone
Этот командлет возвращает объект, который представляет зону DNS.
Если имя зоны не задано, возвращается массив объектов зоны.

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[New-AzureRmDnsZone](./New-AzureRmDnsZone.md)

[Remove-AzureRmDnsZone](./Remove-AzureRmDnsZone.md)

[Set-AzureRmDnsZone](./Set-AzureRmDnsZone.md)
