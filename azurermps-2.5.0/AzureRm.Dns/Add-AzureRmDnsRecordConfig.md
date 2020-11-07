---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: CD119EBE-E1A4-4E9D-B3BA-FDAF89BF0DDB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f2ba0cb03b4819c444f43a59f5556cf2ec8c17a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913656"
---
# Add-AzureRmDnsRecordConfig

## КРАТКИй обзор
Добавляет запись DNS в локальный объект локального множества записей.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### Помощью
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String> [<CommonParameters>]
```

### AAAA
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String> [<CommonParameters>]
```

### СЛУЖБУ
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [<CommonParameters>]
```

### МХ
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [<CommonParameters>]
```

### УКАЗАТЕЛЯ
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String> [<CommonParameters>]
```

### ТХТ
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [<CommonParameters>]
```

### МОГЛА
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [<CommonParameters>]
```

### CNAME
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Add-AzureRmDnsRecordConfig** добавляет запись DNS (Domain Name System) в объект **набора записей** .
Объект **Recordset** является автономным объектом, и изменения в нем не изменяют ответы DNS, пока не будет запущен командлет Set-AzureRmDnsRecordSet, чтобы сохранить изменения в службе Microsoft Azure DNS.

Записи SOA создаются при создании зоны DNS и удаляются при удалении зоны DNS.
Вы не можете добавлять и удалять записи SOA, но можете редактировать их.

Вы можете передать объект **набора записей** в этот командлет как параметр или с помощью оператора конвейера.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Добавление записи A в набор записей
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzureRmDnsRecordSet
```

В этом примере к существующему набору записей добавляется запись A.

### Пример 2: Добавление записи AAAA в набор записей
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzureRmDnsRecordSet
```

В этом примере добавляется запись AAAA в существующий наборы записей.

### Пример 3: Добавление записи CNAME в набор записей
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Cname contoso.com | Set-AzureRmDnsRecordSet
```

В этом примере добавляется запись CNAME к существующему набору записей.
Так как набор записей CNAME может содержать не более одной записи, сначала должна быть пустая набор записей, или существующие записи должны быть удалены с помощью Remove-AzureRmDnsRecordConfig.

### Пример 4: Добавление записи MX в набор записей
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzureRmDnsRecordSet
```

В этом примере добавляется запись MX в существующий наборы записей.
Имя записи "@" обозначает набор записей на Апексе зоны.

### Пример 5: Добавление записи NS в набор записей
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Nsdname ns1.myzone.com | Set-AzureRmDnsRecordSet
```

В этом примере добавляется запись NS для существующего множества записей.

### Пример 6: Добавление записи PTR в набор записей
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzureRmDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzureRmDnsRecordConfig -Ptrdname www.contoso.com | Set-AzureRmDnsRecordSet
```

В этом примере к существующему набору записей добавляется запись PTR.

### Пример 7: Добавление записи SRV в набор записей
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzureRmDnsRecordSet
```

В этом примере добавляется запись SRV для существующего множества записей.

### Пример 8: Добавление записи TXT в набор записей
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Value "This is a TXT Record" | Set-AzureRmDnsRecordSet
```

В этом примере к существующему набору записей добавляется запись TXT.

## ПАРАМЕТРЫ

### -CNAME
Задает доменное имя для записи канонического имени (CNAME).

```yaml
Type: String
Parameter Sets: CNAME
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Exchange
Указывает имя почтового сервера для записи почтового обменника (MX).

```yaml
Type: String
Parameter Sets: MX
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ipv4Address
Задает IPv4-адрес для записи A.

```yaml
Type: String
Parameter Sets: A
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ipv6Address
Задает IPv6-адрес для записи AAAA.

```yaml
Type: String
Parameter Sets: AAAA
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nsdname
Указывает имя сервера доменных имен для записи сервера доменных имен (NS).

```yaml
Type: String
Parameter Sets: NS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Port (порт)
Указывает порт для записи службы (SRV).

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Предпочтения
Задает приоритет MX-записи.

```yaml
Type: UInt16
Parameter Sets: MX
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Priority (приоритет)
Указывает приоритет записи SRV.

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ptrdname
Указывает целевое доменное имя записи ресурса указателя (PTR).

```yaml
Type: String
Parameter Sets: PTR
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Набор записей
Указывает объект **набора записей** , который нужно изменить.

```yaml
Type: DnsRecordSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Target
Указывает целевой объект для записи SRV.

```yaml
Type: String
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Value (значение)
Задает значение для записи TXT.

```yaml
Type: String
Parameter Sets: TXT
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Weight
Определяет вес записи SRV.

```yaml
Type: UInt16
Parameter Sets: SRV
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

### Microsoft. Azure. Commands. DNS. DnsRecordSet
Вы можете передать в этот командлет объект **набора записей** .
Это автономное представление **набора записей** , и изменения в нем не изменяют ответы DNS до тех пор, пока вы не запустили командлет Set-AzureRmDnsRecordSet.

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. DNS. DnsRecordSet
Этот командлет возвращает измененный объект **набора записей** .
Кроме того, переданный объект изменяется напрямую.

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmDnsRecordSet](./Get-AzureRmDnsRecordSet.md)

[Remove-AzureRmDnsRecordConfig](./Remove-AzureRmDnsRecordConfig.md)

[Set-AzureRmDnsRecordSet](./Set-AzureRmDnsRecordSet.md)
