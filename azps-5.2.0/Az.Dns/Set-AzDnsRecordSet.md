---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/set-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
ms.openlocfilehash: e75d394596b85c75dc79b0eb0d2b19525aa9c7c4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402311"
---
# Set-AzDnsRecordSet

## SYNOPSIS
Обновляет набор записей DNS.

## СИНТАКСИС

```
Set-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## ОПИСАНИЕ
**Cmdlet Set-AzDnsRecordSet** обновляет набор записей в службе DNS Azure из локального объекта **RecordSet.**
Объект **RecordSet** можно передать в качестве параметра или с помощью оператора конвейера.
С помощью переменных *Confirm* и $ConfirmPreference Windows PowerShell можно управлять запросом на подтверждение с помощью cmdlet.
Набор записей не обновляется, если он был изменен в Azure DNS после извлечения локального объекта **RecordSet.**
Это обеспечивает защиту от одновременного изменения.
Вы можете скрыть это поведение с помощью параметра *Overwrite,* который обновляет набор записей независимо от одновременного изменения.

## ПРИМЕРЫ

### Пример 1. Обновление набора записей
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzDnsRecordSet
```

Первая команда использует Get-AzDnsRecordSet для получения указанного набора записей, а затем сохраняет его в $RecordSet переменной.
Вторая и третья команды — это внестроковые операции по добавлению в набор записей A двух записей.
В последней команде для фиксации обновления используется командлет **Set-AzDnsRecordSet.**

### Пример 2. Обновление записи SOA
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet
```

Первая команда использует командлет **Get-AzDnsRecordset** для получения указанного набора записей, а затем сохраняет его в $RecordSet переменной.
Вторая команда обновляет указанную запись SOA в $RecordSet.
В последней команде для распространения обновления в $RecordSet используется командлет **Set-AzDnsRecordSet.**

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

### -Overwrite
Обновление набора записей независимо от изменений.
Набор записей не будет обновляться, если он был изменен в Azure DNS после извлечения локального объекта **RecordSet.**
Это обеспечивает защиту от одновременного изменения.
Чтобы скрыть это поведение, можно использовать параметр *Overwrite,* что приводит к обновлению набора записей независимо от одновременного изменения.

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
Набор **записей, который** нужно обновить.

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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
Показывает, что произойдет при запуске cmdlet. Этот cmdlet не будет выполниться. Показывает, что произойдет при запуске cmdlet. Этот cmdlet не будет выполниться.

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

### Microsoft.Azure.Commands.Dns.DnsRecordSet

## OUTPUTS

### Microsoft.Azure.Commands.Dns.DnsRecordSet

## ПРИМЕЧАНИЯ
С помощью параметра *Confirm* (Подтвердить) можно управлять запросом на подтверждение с помощью этого cmdlet.
По умолчанию с помощью cmdlet вы можете получить подтверждение, если переменная $ConfirmPreference Windows PowerShell имеет значение "Средний" или "Ниже".
Если указать *"Подтвердить"* или *"$True:$True",* этот cmdlet запросит подтверждение перед запуском.
Если *указать confirm:$False,* то при этом не будет предложено подтвердить запрос. 

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzDnsRecordSet](./Get-AzDnsRecordSet.md)

[New-AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Remove-AzDnsRecordSet](./Remove-AzDnsRecordSet.md)
