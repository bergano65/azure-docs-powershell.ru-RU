---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/powershell/module/az.support/get-azsupportticketcommunication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
ms.openlocfilehash: 106ee61629c1252300d63ca686848ba7cc926cea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981912"
---
# Get-AzSupportTicketCommunication

## SYNOPSIS
Получите сообщения в службу поддержки.

## СИНТАКСИС

### GetByNameParameterSet (по умолчанию)
```
Get-AzSupportTicketCommunication -SupportTicketName <String> [-Name <String>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

### GetByParentObjectParameterSet
```
Get-AzSupportTicketCommunication [-Name <String>] -SupportTicketObject <PSSupportTicket> [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

## ОПИСАНИЕ
Получает сообщения для билета в службу поддержки. Он получит все сообщения для билета, если не указать другие параметры. Вы также можете отфильтровать сообщения по CreatedDate или CommunicationType с помощью параметра Filter. Вот несколько примеров значений фильтра, которые можно указать.


| Сценарий                                                        | Фильтр                                                     |
|-----------------------------------------------------------------|------------------------------------------------------------|
| Получить веб-связь                                          | "CommunicationType eq 'Web'"                               |
| Получить связь по телефону                                        | "CommunicationType eq 'Phone'"                             |
| Получать сообщения, созданные 20 декабря 2019 г. или после этого | "CreatedDate ge 2019-12-20"                                |
| Получите сообщения, созданные после 20 декабря 2019 г.       | "CreatedDate gt 2019-12-20"                                |
| Возвращает веб-сообщения, созданные после 20 декабря 2019 г.            | "CreatedDate gt 2019-12-20 and CommunicationType eq 'Web'" |


Этот cmdlet поддерживает разведданный с помощью параметров First и Skip.

Вы также можете получить сообщение о едином сообщении в службу поддержки, указав его имя. 

## ПРИМЕРЫ

### Пример 1. Извлечение всех сообщений для получения билета в службу поддержки
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
```

### Пример 2. Извлечение сообщения по имени для получения билета в службу поддержки
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Name "testmessage1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage1 user@contoso.com     test message   2/4/2020 9:38:14 PM
```

### Пример 3. Извлечение первых 2 сообщений для получения билета в службу поддержки
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### Пример 4. Извлечение следующих 2 сообщений после пропуска первых 2 сообщений для сообщения в службу поддержки
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Skip 2 -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage4 user@contoso.com     test message4  2/4/2020 9:38:14 PM
testmessage5 user@contoso.com     test message5  2/4/2020 9:36:36 PM
```

### Пример 5. Извлечение всех веб-сообщений для получения билета в службу поддержки
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web'"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### Пример 6. Извлечение всех сообщений, созданных 20 декабря 2019 г., или после их получения в службу поддержки
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### Пример 7. Извлечение всех веб-сообщений, созданных 20 декабря 2019 г., или после их получения в службу поддержки
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web' and CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### Пример 8. Извлечение всех сообщений для получения билета в службу поддержки путем прокайки объекта билета поддержки
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Get-AzSupportTicketCommunication

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
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
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Имя связи.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SupportTicketName
Имя билета в службу поддержки.

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

### -SupportTicketObject
Объект билета в службу поддержки.

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSSupportTicket
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -IncludeTotalCount
Отчет об общем количестве объектов в наборе данных (integer), за которым следуют выбранные объекты.
Если не удается определить общее количество, отображается "Неизвестное общее количество". У значения integer есть свойство "Точность", которое указывает на надежность общего количества значений.
Значение точности в диапазонах от 0,0 до 1,0, где 0,0 означает, что не удалось подсчитать объекты, 1,0 означает, что число точное, а значение от 0,0 до 1,0 указывает на более надежную оценку.

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

### Microsoft.Azure.Commands.Support.Models.PSSupportTicket

## OUTPUTS

### Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ
