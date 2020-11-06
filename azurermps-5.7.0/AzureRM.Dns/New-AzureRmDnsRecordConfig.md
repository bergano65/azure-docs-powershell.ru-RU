---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: AD97BCAF-69BA-4C16-8B57-AB243D796B71
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/new-azurermdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsRecordConfig.md
ms.openlocfilehash: f44472ac83c1d92baab5d4c7c3b4c8d325e3dfbe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567010"
---
# New-AzureRmDnsRecordConfig

## КРАТКИй обзор
Создание нового локального объекта записи DNS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### Помощью
```
New-AzureRmDnsRecordConfig -Ipv4Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### AAAA
```
New-AzureRmDnsRecordConfig -Ipv6Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Службу
```
New-AzureRmDnsRecordConfig -Nsdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### МХ
```
New-AzureRmDnsRecordConfig -Exchange <String> -Preference <UInt16> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Указателя
```
New-AzureRmDnsRecordConfig -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ТХТ
```
New-AzureRmDnsRecordConfig -Value <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Могла
```
New-AzureRmDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### CName
```
New-AzureRmDnsRecordConfig -Cname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Caa
```
New-AzureRmDnsRecordConfig -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzureRmDnsRecordConfig** создает локальный объект **DnsRecord** .
Массив этих объектов передается в командлет New-AzureRmDnsRecordSet с помощью параметра *DnsRecords* для указания записей для создания в наборе записей.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание набора записей типа A
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzureRmDnsRecordConfig -IPv4Address 1.2.3.4)

# To create a record set containing multiple records, use New-AzureRmDnsRecordConfig to add each record to the $Records array,
# then call New-AzureRmDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzureRmDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

В этом примере в myzone.com зоны создается **набор записей** с именем www.
Набор записей имеет тип A и имеет значение TTL, равное 1 часу (3600 секунд).
Она состоит из одной записи DNS.

### Пример 2: создание набора записей типа AAAA
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

В этом примере в myzone.com зоны создается **набор записей** с именем www.
Набор записей имеет тип AAAA и имеет значение TTL, равное 1 часу (3600 секунд).
Она состоит из одной записи DNS.

Чтобы создать набор **записей** с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.

### Пример 3: создание набора записей с типом CNAME
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

В этом примере в myzone.com зоны создается **набор записей** с именем www.
Набор записей имеет тип CNAME и имеет значение TTL, равное 1 часу (3600 секунд).
Она состоит из одной записи DNS.

Чтобы создать набор **записей** с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.

### Пример 4: создание набора записей типа MX
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Эта команда создает **набор записей** с именем www в зоне MyZone.com.
Набор записей имеет тип MX и имеет значение TTL, равное 1 часу (3600 секунд).
Она состоит из одной записи DNS.

Чтобы создать набор **записей** с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.

### Пример 5: создание набора записей с типом "NS"
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Эта команда создает **набор записей** с именем ns1 в зоне MyZone.com.
Набор записей имеет тип NS и имеет значение TTL, равное 1 часу (3600 секунд).
Она состоит из одной записи DNS.

Чтобы создать набор **записей** с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.

### Пример 6: создание набора записей типа PTR
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

Эта команда создает **набор записей** с именем 4 в зоне 3.2.1.in-addr. arpa.
Набор записей имеет тип PTR и имеет значение TTL, равное 1 часу (3600 секунд).
Она состоит из одной записи DNS.

Чтобы создать набор **записей** с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.

### Пример 7: создание набора записей типа SRV
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Эта команда создает **набор записей** с именем _sip. _tcp в зоне MyZone.com.
Набор записей имеет тип SRV и имеет значение TTL, равное 1 часу (3600 секунд).
Она состоит из одной записи DNS, указывающей на IP-адрес 2001.2.3.4.

Служба SIP и протокол TCP задаются как часть имени набора записей, а не как часть данных записи.

Чтобы создать набор **записей** с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.

### Пример 8: создание набора записей типа TXT
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Эта команда создает **набор записей** с именем, указанным в MyZone.com Zone.
Набор записей имеет тип TXT и имеет значение TTL, равное 1 часу (3600 секунд).
Она состоит из одной записи DNS.

Чтобы создать набор **записей** с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.

## ПАРАМЕТРЫ

### -CaaFlags
Флаги для записи CAA, которую нужно добавить. Должно быть числом от 0 до 255.

```yaml
Type: Byte
Parameter Sets: Caa
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CaaTag
Поле тега записи CAA, которую нужно добавить.

```yaml
Type: String
Parameter Sets: Caa
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CaaValue
Поле значения для записи CAA, которую нужно добавить.

```yaml
Type: String
Parameter Sets: Caa
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CNAME
Задает доменное имя для записи канонического имени (CNAME).

```yaml
Type: String
Parameter Sets: CName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Exchange
Указывает имя почтового сервера для записи почтового обменника (MX).

```yaml
Type: String
Parameter Sets: Mx
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
Parameter Sets: Aaaa
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
Parameter Sets: Ns
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
Parameter Sets: Srv
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
Parameter Sets: Mx
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
Parameter Sets: Srv
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
Parameter Sets: Ptr
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Target
Указывает целевой объект для записи SRV.

```yaml
Type: String
Parameter Sets: Srv
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
Parameter Sets: Txt
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
Parameter Sets: Srv
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

### Ничего.

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. DNS. DnsRecordBase

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Add-AzureRmDnsRecordConfig](./Add-AzureRmDnsRecordConfig.md)

[New-AzureRmDnsRecordSet](./New-AzureRmDnsRecordSet.md)

[Remove-AzureRmDnsRecordConfig](./Remove-AzureRmDnsRecordConfig.md)
