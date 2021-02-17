---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
ms.openlocfilehash: 368ae4ad814c9414ea211ea6e44c2d3fbda005f7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100216905"
---
# Get-AzSupportTicket

## SYNOPSIS
Получить билеты в службу поддержки.

## СИНТАКСИС

### ListParameterSet (по умолчанию)
```
Get-AzSupportTicket [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### GetByNameParameterSet
```
Get-AzSupportTicket -Name <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## ОПИСАНИЕ
Получает список билетов в службу поддержки. Он получит все билеты в службу поддержки, если не указать параметры. Вы также можете отфильтровать билеты в службу поддержки по status или CreatedDate с помощью параметра Filter. Вот несколько примеров значений фильтра, которые можно указать.

| Сценарий                                                         | Фильтр                                           |
|------------------------------------------------------------------|--------------------------------------------------|
| Получить открытые билеты                               | "Status eq 'Open'"                               |
| Получить билеты, которые находятся в закрытом состоянии                             | "Status eq 'Closed'"                             |
| Получите билеты, созданные 20 декабря 2019 г. или после этого         | "CreatedDate ge 2019-12-20"                      |
| Получите билеты, созданные после 20 декабря 2019 г.               | "CreatedDate gt 2019-12-20"                      |
| Возвращает количество открытых билетов, созданных после 20 декабря 2019 г. | "CreatedDate gt 2019-12-20 and Status eq 'Open'" |


Этот cmdlet поддерживает разведданный с помощью параметров First и Skip.

Вы также можете получить один билет в службу поддержки, указав его имя. 

## ПРИМЕРЫ

### Пример 1. Получить первые 2 билетов
```powershell
PS C:\> Get-AzSupportTicket -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### Пример 2. Получите первые 2 билета после пропуска первых 2
```powershell
PS C:\> Get-AzSupportTicket -Skip 2 -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test3 test title3                  150010521000314 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test4 test title4                  150010521000315 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### Пример 3. Получить билет в службу поддержки по имени
```powershell
PS C:\> Get-AzSupportTicket -Name "test1"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
```

### Пример 4. Первые 2 билета в службу поддержки отфильтровыются по статусу
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Closed'" -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### Пример 5. Получить все билеты в службу поддержки, созданные после 20 декабря 2019 г. в состоянии "Открыть"
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Open' and CreatedDate gt 2019-12-20"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test6 test title6                  150010521000311 Minimal  Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
test7 test title7                  150010521000312 Minimal  Billing                       Open   2/5/2020 1:33:53 AM
```

## PARAMETERS

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

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

### -Filter
Фильтр, применяемый к результатам этого cmdlet.

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Имя билета в службу поддержки, который получает этот cmdlet.

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeTotalCount
Отчет об общем количестве объектов в наборе данных (integer), за которым следуют выбранные объекты.
Если не удается определить общее количество, отображается "Неизвестное общее количество". У значения integer есть свойство "Точность", которое указывает на надежность общего количества значений.
Значение точности в диапазонах от 0,0 до 1,0, где 0,0 означает, что не удалось подсчитать объекты, 1,0 — точное число, а значение в диапазоне от 0,0 до 1,0 указывает на более надежную оценку.

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

### -Skip
Игнорирует указанное количество объектов, а затем возвращает оставшиеся объекты.
Введите количество объектов, которые нужно пропустить.

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -First
Возвращает только указанное количество объектов.
Введите количество объектов, которые нужно получить.

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Нет

## OUTPUTS

### Microsoft.Azure.Commands.Support.Models.PSSupportTicket

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ
