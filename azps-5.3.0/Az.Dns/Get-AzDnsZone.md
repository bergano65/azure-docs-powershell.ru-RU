---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
ms.openlocfilehash: 68fff050564eff7014a7428556d3d4b2ce68f06d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504947"
---
# Get-AzDnsZone

## SYNOPSIS
Получает зону DNS.

## СИНТАКСИС

### По умолчанию (по умолчанию)
```
Get-AzDnsZone [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroup
```
Get-AzDnsZone [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## ОПИСАНИЕ
**Cmdlet Get-AzDnsZone** получает зону службы доменных имен (DNS) из указанной группы ресурсов.
Если задать параметр *Name,* возвращается один **объект DnsZone.**
Если не указать параметр *Name,* возвращается массив, содержащий все зоны в указанной группе ресурсов.
Для обновления зоны можно использовать объект **DnsZone,** например **объекты RecordSet.**

## ПРИМЕРЫ

### Пример 1. Получить зону
```
PS C:\> $Zone = Get-AzDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

В этом примере зона DNS myzone.com из указанной группы ресурсов, а затем хранится в переменной $Zone ресурса.

### Пример 2. Получить все зоны в группе ресурсов
```
PS C:\> $Zones = Get-AzDnsZone -ResourceGroupName "MyResourceGroup"
```

В этом примере все зоны DNS в указанной группе ресурсов, а затем в переменной $Zones ресурсов.

### Пример 3. Получить все зоны подписки
```
PS C:\> $Zones = Get-AzDnsZone
```

В этом примере все зоны DNS в текущей подписке Azure, а затем в переменной $Zones Azure.

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
Указывает имя зоны DNS, которая будет получаться.
Если значение параметра *Name* не задано, этот cmdlet получает все зоны DNS в указанной группе ресурсов.
Если параметр *ResourceGroupName не* задан, этот cmdlet получает все зоны DNS в текущей подписке Azure.

```yaml
Type: System.String
Parameter Sets: ResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов, которая содержит зону DNS, которую нужно получить.
Если параметр *ResourceGroupName* не указан, необходимо также опустить параметр *Name.*
В этом случае этот cmdlet получает все зоны DNS в текущей подписке Azure.

```yaml
Type: System.String
Parameter Sets: ResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

## OUTPUTS

### Microsoft.Azure.Commands.Dns.DnsZone

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[New-AzDnsZone](./New-AzDnsZone.md)

[Remove-AzDnsZone](./Remove-AzDnsZone.md)

[Set-AzDnsZone](./Set-AzDnsZone.md)
