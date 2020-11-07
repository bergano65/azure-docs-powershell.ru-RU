---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4027b13fb398d69bee09be5c0a939ff86a099e39
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914490"
---
# Get-AzureRmDnsRecordSet

## КРАТКИй обзор
Получает набор записей DNS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### »
```
Get-AzureRmDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String>
 [-RecordType <RecordType>] [<CommonParameters>]
```

### DataObject
```
Get-AzureRmDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmDnsRecordSet** получает набор записей DNS (Domain Name System) с указанными именем и типом в указанной зоне.

Если не указать параметры *Name* или *RecordType* , этот командлет возвращает все наборы записей указанного типа в зоне.
Если указать параметр *RecordType* , но не параметр *Name* , этот командлет возвращает все наборы записей с указанным типом записи.

Вы можете использовать оператор конвейера для передачи объекта **dnsZone** в этот командлет или передавать объект **dnsZone** в качестве параметра *зоны* или можно указать зону и группу ресурсов по имени.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение наборов записей с указанным именем и типом
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

Эта команда получает набор записей с именем www в заданной группе ресурсов и зоне, а затем сохраняет его в переменной $RecordSet.
Так как указаны параметры *Name* и *RecordType* , возвращается только один объект **Recordset** .

### Пример 2: получение наборов записей указанного типа
```
PS C:\>$RecordSets = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

Эта команда получает массив всех наборов записей типа A в зоне с именем myzone.com в группе ресурсов с именем MyResourceGroup и сохраняет их в переменной $RecordSets.

### Пример 3: получение всех наборов записей в зоне
```
PS C:\>$RecordSets = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

Эта команда получает массив всех наборов записей в зоне с именем myzone.com в группе ресурсов с именем MyResourceGroup, а затем сохраняет их в переменной $RecordSets.

### Пример 4: получение всех наборов записей в зоне с помощью объекта DnsZone
```
PS C:\> $Zone = Get-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzureRmDnsRecordSet -Zone $Zone
```

Этот пример эквивалентен примеру 3 выше.
На этот раз зона задается с помощью объекта Zone.

## ПАРАМЕТРЫ

### -Name (имя)
Указывает имя **набора записей** для получения.
Если параметр *Name* не указан, возвращаются все наборы записей указанного типа.

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Object
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RecordType
Указывает тип DNS-записи, которую получает этот командлет.

Допустимые значения: 

- Помощью
- AAAA
- CNAME
- МХ
- СЛУЖБУ
- УКАЗАТЕЛЯ
- ЗОНЫ
- МОГЛА
- ТХТ

Если параметр *RecordType* не указан, необходимо также опустить параметр *Name* . Затем этот командлет возвращает все наборы записей в зоне (для всех имен и типов).

```yaml
Type: RecordType
Parameter Sets: (All)
Aliases: 
Accepted values: A, AAAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает группу ресурсов, которая содержит зону DNS.
Имя зоны также должно быть указано с помощью параметра *zonename* .

Кроме того, вы можете указать зону и группу ресурсов, передав объект **dnsZone** с помощью параметра *Zone* .

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
Указывает зону DNS, которая содержит набор записей, который получает этот командлет.
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

### -ИмяЗоны
Указывает имя зоны DNS, которая содержит набор записей, для которого требуется получить доступ.
Группа ресурсов, содержащая зону, также должна быть указана с помощью параметра *ResourceGroupName* .

Кроме того, вы можете указать зону и группу ресурсов, передав объект зоны DNS с помощью параметра *Zone* .

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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Microsoft. Azure. Commands. DNS. DnsZone
Вы можете передать на этот командлет объект **dnsZone** .
Объект **dnsZone** представляет зону, в которой следует искать объект **набора записей** .

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. DNS. DnsRecordSet
Этот командлет возвращает один или несколько объектов, представляющих найденные наборы записей.
Если указаны параметры *Name* и *RecordType* , возвращается не более одного **набора записей** , в противном случае несколько объектов **набора записей** возвращаются в виде массива.

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[New-AzureRmDnsRecordSet](./New-AzureRmDnsRecordSet.md)

[Remove-AzureRmDnsRecordSet](./Remove-AzureRmDnsRecordSet.md)

[Set-AzureRmDnsRecordSet](./Set-AzureRmDnsRecordSet.md)


