---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: ''
schema: 2.0.0
ms.openlocfilehash: b86ad0382fa7f87ac8aabb6b026b84d5a879f8ad
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914474"
---
# Remove-AzureRmDnsRecordSet

## КРАТКИй обзор
Удаляет набор записей.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### »
```
Remove-AzureRmDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String>
 -ResourceGroupName <String> [-Force] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Смешивания
```
Remove-AzureRmDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-Force] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DataObject
```
Remove-AzureRmDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-Force] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Remove-AzureRmDnsRecordSet** удаляет набор записей из указанной зоны.
Вы не можете удалить записи SOA или сервера имен (NS), которые будут автоматически созданы на зоне Апекс.

Вы можете передать в этот командлет объект **набора записей** с помощью оператора конвейера или в качестве параметра.
Чтобы определить набор записей по имени и типу, не используя объект **Recordset** , необходимо передать зону как объект **dnsZone** с помощью оператора конвейера или в качестве параметра либо можно указать параметры *zonename* и *ResourceGroupName* .

Вы можете использовать параметр Confirm и $ConfirmPreference переменной Windows PowerShell, чтобы указать, нужно ли командлету запрашивать подтверждение.

При указании набора записей с помощью объекта **Recordset** набор записей не удаляется, если он был изменен в Azure DNS, так как был получен объект локального **набора записей** .
Это обеспечивает защиту для параллельных изменений.
Вы можете отключить этот параметр с помощью параметра *overwrite* , который удаляет набор записей независимо от текущих изменений.

## ИЛЛЮСТРИРУЮТ

### Пример 1: удаление набор записей
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordSet -RecordSet $RecordSet
```

Первая команда получает указанный наборы записей и сохраняет ее в переменной $RecordSet. Вторая команда удаляет запись, указанную в $RecordSet.

### Пример 2: удаление набор записей и отключение всех подтверждений
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzureRmDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzureRmDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

Первая команда получает указанный наборы записей.

Вторая команда удаляет наборы записей, даже если она была изменена.
Запросы на подтверждение подавляются.

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
Указывает имя **набора записей** , который нужно удалить.
Когда вы указываете набор записей по имени, зона DNS должна быть указана с помощью параметра *Zone* или параметров *zonename* и *ResourceGroupName* .

Кроме того, набор записей можно указать с помощью объекта **Recordset** , передаваемого с помощью параметра *Recordset* .

```yaml
Type: String
Parameter Sets: Fields, Mixed
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Overwrite
При указании набора записей с помощью объекта **Recordset** набор записей не удаляется, если он был изменен в Azure DNS, так как был получен объект локального **набора записей** .
Это обеспечивает защиту для параллельных изменений.
Это может быть подавлено с помощью параметра *overwrite* , который удаляет набор записей независимо от текущих изменений.

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

### -Набор записей
Указывает объект **набора записей** , который нужно удалить.

Кроме того, можно задать набор записей с помощью параметров *имени* и *зоны* либо с помощью параметров *Name* , *имя_зоны* и *ResourceGroupName* .

```yaml
Type: DnsRecordSet
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RecordType
Указывает тип DNS-записи.

Допустимые значения:

- Помощью
- AAAA
- CNAME
- МХ
- СЛУЖБУ
- УКАЗАТЕЛЯ
- МОГЛА
- ТХТ

Записи SOA удаляются автоматически при удалении зоны.
Записи SOA нельзя удалять вручную.

```yaml
Type: RecordType
Parameter Sets: Fields, Mixed
Aliases: 
Accepted values: A, AAAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает группу ресурсов, которая содержит DNS-зону, которая содержит **набор записей** для удаления.
Этот параметр применяется только в том случае, если набор записей и зона DNS указаны с использованием параметров *Name* и *zonename* .

Кроме того, вы можете задать набор записей с помощью параметра " *набор записей* " или параметров " *имя* " и " *зона* ".

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
Указывает DNS-зону, которая содержит **набор записей** для удаления.
Этот параметр применяется только при указании заданной записи с помощью параметра *Name* .

Кроме того, вы можете задать набор записей с помощью параметра " *набор записей* " или параметров *Name* , *имя_зоны* и *ResourceGroupName* .

```yaml
Type: DnsZone
Parameter Sets: Mixed
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ИмяЗоны
Указывает имя зоны, содержащей **набор записей** для удаления.
Кроме того, необходимо указать параметры *Name* и *ResourceGroupName* .

Кроме того, можно задать набор записей с помощью параметра " *набор записей* ", а также параметров *имени* и *зоны* .

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Microsoft. Azure. Commands. DNS. DnsRecordSet
Вы можете передать в этот командлет объект **набора записей** .

## НАПРЯЖЕНИЕ

### Ничего
Этот командлет не создает никаких выходных данных.

## Пуск
Вы можете использовать параметр *Confirm* , чтобы указать, будет ли этот командлет запрашивать подтверждение.
По умолчанию командлет запрашивает подтверждение, если значение переменной $ConfirmPreference Windows PowerShell — средний или ниже.

Если вы задаете параметр *Confirm* или *Confirm: $true* , этот командлет запрашивает подтверждение перед запуском.
Если вы задаете значение *Confirm: $false* , командлет не будет запрашивать подтверждение.

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmDnsRecordSet](./Get-AzureRmDnsRecordSet.md)

[New-AzureRmDnsRecordSet](./New-AzureRmDnsRecordSet.md)

[Set-AzureRmDnsRecordSet](./Set-AzureRmDnsRecordSet.md)
