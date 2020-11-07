---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/set-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Set-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Set-AzDnsRecordSet.md
ms.openlocfilehash: 1b2ee31c136c24478ddd69d58c264ce44886c057
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910419"
---
# Set-AzDnsRecordSet

## КРАТКИй обзор
Обновляет набор записей DNS.

## Максимальное

```
Set-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzDnsRecordSet** обновляет набор записей в службе DNS Azure из локального объекта **набора записей** .

Вы можете передать объект **набора записей** как параметр или с помощью оператора конвейера.

Вы можете использовать параметр *Confirm* и $ConfirmPreference переменной Windows PowerShell, чтобы указать, нужно ли командлету запрашивать подтверждение.

Набор записей не обновляется, если он был изменен в Azure DNS, так как был получен объект локального **набора записей** .
Это обеспечивает защиту для параллельных изменений.
Это поведение можно отключить с помощью параметра *перезаписи* , который обновляет набор записей независимо от количества параллельных изменений.

## ИЛЛЮСТРИРУЮТ

### Пример 1: обновление набор записей
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzDnsRecordSet
```

Первая команда использует командлет Get-AzDnsRecordSet для получения указанного множества записей и сохраняет его в переменной $RecordSet.

Вторая и третья команды — это автономные операции, позволяющие добавить в набор записей две записи.

В последней команде используется командлет **Set-AzDnsRecordSet** , чтобы зафиксировать обновление.

### Пример 2: Обновление записи SOA
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet
```

Первая команда использует командлет **Get-AzDnsRecordset** для получения указанного множества записей и сохраняет ее в переменной $Recordset.

Вторая команда обновляет указанную запись SOA в $RecordSet.

В последней команде используется командлет **Set-AzDnsRecordSet** , чтобы распространить обновление в $Recordset.

## ПАРАМЕТРЫ

### -Overwrite
Указывает, что нужно обновить набор записей независимо от одновременно выполняемых изменений.

Набор записей не будет обновлен, если он был изменен в Azure DNS, так как был получен объект локального **набора записей** .
Это обеспечивает защиту для параллельных изменений.
Чтобы отменить это поведение, можно использовать параметр *overwrite* , который приводит к обновлению набора записей независимо от одновременного изменения.

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

### -Набор записей
Указывает **набор записей** для обновления.

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

### Microsoft. Azure. Commands. DNS. DnsRecordSet
Вы можете передать в этот командлет объект **набора записей** .

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. DNS. DnsRecordSet
Этот командлет возвращает объект, который представляет обновленный объект **набора записей** .

## Пуск
Вы можете использовать параметр *Confirm* , чтобы указать, будет ли этот командлет запрашивать подтверждение.
По умолчанию командлет запрашивает подтверждение, если значение переменной $ConfirmPreference Windows PowerShell — средний или ниже.

Если вы задаете параметр *Confirm* или *Confirm: $true* , этот командлет запрашивает подтверждение перед запуском.
Если вы задаете значение *Confirm: $false* , командлет не будет запрашивать подтверждение. 

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzDnsRecordSet](./Get-AzDnsRecordSet.md)

[New-AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Remove-AzDnsRecordSet](./Remove-AzDnsRecordSet.md)
