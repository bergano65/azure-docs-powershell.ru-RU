---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 45DF71E0-77E1-4D20-AD09-2C06680F659F
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
ms.openlocfilehash: bb2e9a9729ed911902e493422109cae764ad6d5f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402375"
---
# New-AzDnsRecordSet

## SYNOPSIS
Создает набор записей DNS.

## СИНТАКСИС

### Поля (по умолчанию)
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> -Ttl <UInt32>
 -RecordType <RecordType> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AliasFields
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> [-Ttl <UInt32>]
 -RecordType <RecordType> -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>]
 [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Объект
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> -Ttl <UInt32> -RecordType <RecordType>
 [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AliasObject
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> [-Ttl <UInt32>] -RecordType <RecordType>
 -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## ОПИСАНИЕ
С **помощью cmdlet New-AzDnsRecordSet** создается новый набор записей службы доменных имен (DNS) с указанным именем и типом в указанной зоне.
Объект **RecordSet** — это набор записей DNS с одинаковым именем и типом.
Обратите внимание, что имя является относительно зоны, а не полного имени.
Параметр *DnsRecords* определяет записи в наборе записей.
Этот параметр использует массив записей DNS, построенный с использованием new-AzDnsRecordConfig.
Вы можете использовать оператор конвейера, чтобы передать объект **DnsZone** этому cmdlet, или передать объект **DnsZone** в качестве параметра *зоны.* Кроме того, вы можете указать зону по имени.
С помощью переменных *Confirm* и $ConfirmPreference Windows PowerShell можно управлять запросом на подтверждение с помощью cmdlet.
Если совпадающий **набор записей** уже существует (то же имя и тип записи), необходимо указать параметр *Overwrite,* в противном случае командлет не создаст новый **Набор записей.**

## ПРИМЕРЫ

### Пример 1. Создание наборов записей типа A
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -IPv4Address 1.2.3.4)

# To create a record set containing multiple records, use New-AzDnsRecordConfig to add each record to the $Records array,
# then call New-AzDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

В этом примере создается **набор записей с** именем www в зоне myzone.com.
Набор записей имеет тип A и имеет срок жизни 1 час (3600 секунд).
Она содержит одну запись DNS.

### Пример 2. Создание наборов записей типа AAAA
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

В этом примере создается **набор записей с** именем www в зоне myzone.com.
Набор записей имеет тип AAAA и имеет срок жизни 1 час (3600 секунд).
Она содержит одну запись DNS.
Чтобы создать набор **записей,** используя только одну строку pn_PowerShell_short или создать набор записей с несколькими записями, см. пример 1.

### Пример 3. Создание наборов записей типа CNAME
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

В этом примере создается **набор записей с** именем www в зоне myzone.com.
Набор записей имеет тип CNAME и имеет срок жизни 1 час (3600 секунд).
Она содержит одну запись DNS.
Чтобы создать набор **записей,** используя только одну строку pn_PowerShell_short или создать набор записей с несколькими записями, см. пример 1.

### Пример 4. Создание наборов записей типа MX
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "mail" -RecordType MX -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Эта команда создает набор **записей с именем** www в зоне myzone.com.
Набор записей имеет тип MX и имеет срок жизни 1 час (3600 секунд).
Она содержит одну запись DNS.
Чтобы создать набор **записей,** используя только одну строку pn_PowerShell_short или создать набор записей с несколькими записями, см. пример 1.

### Пример 5. Создание наборов записей типа NS
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Эта команда создает набор **записей с** именем ns1 в зоне myzone.com.
Набор записей имеет тип NS и имеет срок жизни 1 час (3600 секунд).
Она содержит одну запись DNS.
Чтобы создать набор **записей,** используя только одну строку pn_PowerShell_short или создать набор записей с несколькими записями, см. пример 1.

### Пример 6. Создание наборов записей типа PTR
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

Эта команда создает набор **записей с** именем 4 в зоне 3.2.1.in-addr.arpa.
Набор записей имеет тип PTR и имеет срок жизни 1 час (3600 секунд).
Она содержит одну запись DNS.
Чтобы создать набор **записей,** используя только одну строку pn_PowerShell_short или создать набор записей с несколькими записями, см. пример 1.

### Пример 7. Создание recordSet типа SRV
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Эта команда создает набор **записей с** именем _sip._tcp в myzone.com.
Набор записей имеет тип SRV и имеет срок жизни 1 час (3600 секунд).
Она содержит одну запись DNS, указывав на IP-адрес 2001.2.3.4.
Служба (sip) и протокол (tcp) указаны как часть имени набора записей, а не как часть данных записи.
Чтобы создать набор **записей,** используя только одну строку pn_PowerShell_short или создать набор записей с несколькими записями, см. пример 1.

### Пример 8. Создание наборов записей типа TXT
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Эта команда создает **именуемую** команду RecordSet в myzone.com.
Набор записей имеет тип TXT и имеет срок жизни 1 час (3600 секунд).
Она содержит одну запись DNS.
Чтобы создать набор **записей,** используя только одну строку pn_PowerShell_short или создать набор записей с несколькими записями, см. пример 1.

### Пример 9. Создание наборов записей в апексе зоны
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Эта команда создает набор **записей** в апексе (корневом) точках зоны myzone.com.
Для этого имя набора записей задано как @(включая двойные кавычка).
Записи CNAME невозможно создать в апексе зоны.
Это ограничение стандартов DNS. это не ограничение службы Azure DNS.
Чтобы создать набор **записей,** используя только одну строку pn_PowerShell_short или создать набор записей с несколькими записями, см. пример 1.

### Пример 10. Создание набора записей с подстрогными знаками
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Эта команда создает набор **записей с именем** * в myzone.com.
Это набор записей с подстрокными знаками.
Чтобы создать набор **записей,** используя только одну строку pn_PowerShell_short или создать набор записей с несколькими записями, см. пример 1.

### Пример 11. Создание пустого набора записей
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords @()
```

Эта команда создает набор **записей с именем** www в зоне myzone.com.
Набор записей имеет тип A и имеет срок жизни 1 час (3600 секунд).
Это пустой набор записей, который выступать в качестве места для добавления записей.

### Пример 12. Создание набора записей и подавления всего подтверждения
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

Эта команда создает **набор записей.**
Параметр *"Перезаписать"* гарантирует, что этот набор записей перезаписает все существующие записи с одинаковыми именами и типами (существующие записи в этом наборе будут потеряны).
Параметр *Confirm* со значением $False подавляет запрос на подтверждение.

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

### -DnsRecords
Определяет массив DNS-записей, которые нужно включить в набор.
С помощью New-AzDnsRecordConfig DNS можно создавать объекты записей DNS.
Дополнительные сведения см. в примерах.

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordBase[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Метаданные
Указывает массив метаданных, который нужно связать с RecordSet.
Метаданные заданы с помощью пар имен и значений, представленных в виде hash tables, например @{"dept"="shopping";" env"="production"}.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Имя создаемого **наборов записей.**

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Overwrite
Указывает на то, что этот cmdlet переописает указанный набор **записей,** если он уже существует.

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

### -RecordType
Тип записи DNS, которая будет создаваться.
Допустимые значения:
- A
- AAAA
- CNAME
- MX
- NS
- PTR
- SRV
- TXT SOA records are created automatically when the zone is created and cannot be created manually.

```yaml
Type: Microsoft.Azure.Management.Dns.Models.RecordType
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Определяет группу ресурсов, которая содержит зону DNS.
Чтобы указать имя зоны, необходимо также указать параметр *ZoneName.*
Вы также можете указать зону и группу ресурсов, указав объект зоны DNS с помощью *параметра Zone (Зона).*

```yaml
Type: System.String
Parameter Sets: Fields, AliasFields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TargetResourceId
ИД целевого ресурса "Псевдоним".

```yaml
Type: System.String
Parameter Sets: AliasFields, AliasObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ttl
Время жизни (TTL) для DNS RecordSet.

```yaml
Type: System.UInt32
Parameter Sets: Fields, Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.UInt32
Parameter Sets: AliasFields, AliasObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
Определяет DnsZone, в котором нужно создать **RecordSet.**
Вы также можете указать зону с помощью параметров *ZoneName* и *ResourceGroupName.*

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object, AliasObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ZoneName
Определяет имя зоны, в которой нужно создать **Набор записей.**
Кроме того, с помощью параметра *ResourceGroupName* необходимо указать группу ресурсов, содержащую зону.
Вы также можете указать зону и группу ресурсов, указав объект зоны DNS с помощью *параметра Zone (Зона).*

```yaml
Type: System.String
Parameter Sets: Fields, AliasFields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### System.UInt32

### Microsoft.Azure.Management.Dns.Models.RecordType

### System.Collections.Hashtable

### Microsoft.Azure.Commands.Dns.DnsRecordBase[]

## OUTPUTS

### Microsoft.Azure.Commands.Dns.DnsRecordSet

## ПРИМЕЧАНИЯ
С помощью параметра *Confirm* (Подтвердить) можно управлять запросом на подтверждение с помощью этого cmdlet.
По умолчанию с помощью cmdlet вы можете получить подтверждение, если переменная $ConfirmPreference Windows PowerShell имеет значение "Средний" или "Ниже".
Если указать *"Подтвердить"* или *"$True:$True",* этот cmdlet запросит подтверждение перед запуском.
Если *указать confirm:$False,* то при этом не будет предложено подтвердить запрос.

## СВЯЗАННЫЕ ССЫЛКИ

[Add-AzDnsRecordConfig](./Add-AzDnsRecordConfig.md)

[Get-AzDnsRecordSet](./Get-AzDnsRecordSet.md)

[New-AzDnsRecordConfig](./New-AzDnsRecordConfig.md)

[Remove-AzDnsRecordSet](./Remove-AzDnsRecordSet.md)

[Set-AzDnsRecordSet](./Set-AzDnsRecordSet.md)
