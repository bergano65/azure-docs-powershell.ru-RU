---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: https://docs.microsoft.com/powershell/module/az.dns/remove-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
ms.openlocfilehash: ab4f7bf6693eda413587b572832706d617b3e683
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984777"
---
# Remove-AzDnsRecordSet

## SYNOPSIS
Удаляет набор записей.

## СИНТАКСИС

### Поля
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String> -ResourceGroupName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Смешанный
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Объект
```
Remove-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## ОПИСАНИЕ
Для удаления указанного набора записей из указанной зоны будет удален набор записей **Remove-AzDnsRecordSet.**
Нельзя удалить soA или NS-записи, автоматически созданные в апексе зоны.
Передать объект **RecordSet** этому cmdlet можно с помощью оператора конвейера или параметра.
Чтобы определить запись, заданную по имени и типу, без использования объекта **RecordSet,** необходимо передать зону в качестве объекта **DnsZone** этому cmdlet с помощью оператора конвейера или в качестве параметра либо указать *параметры ZoneName* и *ResourceGroupName.*
Параметр Confirm и переменная $ConfirmPreference Windows PowerShell можно использовать для управления запросом на подтверждение с помощью cmdlet.
При указании набора записей с использованием объекта **RecordSet** набор записей не удаляется, если он был изменен в Azure DNS после извлечения локального объекта **RecordSet.**
Это обеспечивает защиту от одновременного изменения.
Вы можете скрыть это с помощью параметра *Overwrite,* который удаляет набор записей независимо от одновременного изменения.

## ПРИМЕРЫ

### Пример 1. Удаление набора записей
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet
```

Первая команда получает указанный набор записей, а затем сохраняет его в $RecordSet переменной. Вторая команда удаляет набор записей из $RecordSet.

### Пример 2. Удаление набора записей и подавления всего подтверждения
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

Первая команда получает указанный набор записей.
Вторая команда удаляет набор записей, даже если он изменился до этого времени.
Запросы на подтверждение будут подавляться.

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

### -Name
Имя наборов **записей,** которые нужно удалить.
При указании записи, заданной по имени, необходимо указать зону DNS с помощью параметра *Zone* или *ZoneName* и *ResourceGroupName.*
Набор записей также можно укадрять с помощью объекта **RecordSet,** который передается с помощью *параметра RecordSet.*

```yaml
Type: System.String
Parameter Sets: Fields, Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Overwrite
При указании набора записей с использованием объекта **RecordSet** набор записей не удаляется, если он был изменен в Azure DNS после извлечения локального объекта **RecordSet.**
Это обеспечивает защиту от одновременного изменения.
Это можно сделать с помощью параметра *Overwrite,* который удаляет набор записей независимо от изменений одновременно.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
passthru

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

### -RecordSet
Определяет объект **RecordSet,** который нужно удалить.
Кроме того, набор записей можно настроить с помощью параметров  *Name* и *Zone* (Имя), *ZoneName*(Имя зоны) и *ResourceGroupName (Имя* группы ресурсов).

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RecordType
Тип записи DNS.
Допустимые значения:
- A
- AAAA
- CNAME
- MX
- NS
- PTR
- SRV
- При удалении зоны записи TXT SOA удаляются автоматически.
Удалить записи SOA вручную нельзя.

```yaml
Type: Microsoft.Azure.Management.Dns.Models.RecordType
Parameter Sets: Fields, Mixed
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Определяет группу ресурсов, которая содержит зону DNS, которая содержит **набор записей,** который нужно удалить.
Этот параметр применяется только в том случае, если набор записей и зона DNS заданы с использованием параметров *Name* и *ZoneName.*
Кроме того, набор записей можно указать с помощью *параметра RecordSet* или *параметра Name* и *Zone.*

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
Определяет зону DNS, которая содержит **набор записей,** который нужно удалить.
Этот параметр применяется только при указании набора записей с помощью *параметра Name.*
Кроме того, набор записей можно указать с помощью параметра *RecordSet* или параметров *Name,* *ZoneName* и *ResourceGroupName.*

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ZoneName
Имя зоны, которая содержит **набор записей,** который нужно удалить.
Необходимо также указать *параметры Name* и *ResourceGroupName.*
Кроме того, набор записей можно укадрять с помощью *параметра RecordSet* или *параметров Name* и *Zone.*

```yaml
Type: System.String
Parameter Sets: Fields
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

### Microsoft.Azure.Management.Dns.Models.RecordType

### System.String

### Microsoft.Azure.Commands.Dns.DnsZone

### Microsoft.Azure.Commands.Dns.DnsRecordSet

## OUTPUTS

### System.Boolean

## ПРИМЕЧАНИЯ
С помощью параметра *Confirm* (Подтвердить) можно управлять запросом на подтверждение с помощью этого cmdlet.
По умолчанию с помощью cmdlet вы можете получить подтверждение, если переменная $ConfirmPreference Windows PowerShell имеет значение "Средний" или "Ниже".
Если указать *"Подтвердить"* или *"$True:$True",* этот cmdlet запросит подтверждение перед запуском.
Если *указать confirm:$False,* то при этом не будет предложено подтвердить запрос.

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzDnsRecordSet](./Get-AzDnsRecordSet.md)

[New-AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Set-AzDnsRecordSet](./Set-AzDnsRecordSet.md)
