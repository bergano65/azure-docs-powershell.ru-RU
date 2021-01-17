---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
ms.openlocfilehash: dc110c8989951c6cf5a68e35fbc22c6545c84a1a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402372"
---
# New-AzDnsZone

## SYNOPSIS
Создает новую зону DNS.

## СИНТАКСИС

### ИД (по умолчанию)
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZoneId <String>]
 [-Tag <Hashtable>] [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Имена
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZoneName <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Объекты
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZone <DnsZone>]
 [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## ОПИСАНИЕ
Для создания новой зоны службы доменных имен (DNS) в указанной группе ресурсов будет создаваться новый зоны **New-AzDnsZone.** Необходимо указать уникальное имя зоны DNS для параметра *Name,* иначе при этом будет возвращена ошибка. После создания зоны создайте в New-AzDnsRecordSet наборы записей с помощью New-AzDnsRecordSet.
Параметр Confirm  и переменная $ConfirmPreference Windows PowerShell можно использовать для управления запросом на подтверждение с помощью cmdlet.

## ПРИМЕРЫ

### Пример 1. Создание зоны DNS
```
PS C:\>$Zone = New-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

Эта команда создает новую зону DNS myzone.com в указанной группе ресурсов, а затем сохраняет ее в переменной $Zone ресурса.

### Пример 2. Создание частной зоны DNS с указанием виртуальных сетевых ID
```
PS C:\>$ResVirtualNetworkId = "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testresgroup/providers/Microsoft.Network/virtualNetworks/resvnet"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetworkId @($ResVirtualNetworkId)
```

Эта команда создает новую частную зону DNS с именем myprivatezone.com в указанной группе ресурсов с связанным разрешением виртуальной сети (указывает ее ИД), а затем сохраняет ее в переменной $Zone ресурса.

### Пример 3. Создание частной зоны DNS с указанием виртуальных сетевых объектов
```
PS C:\>$ResVirtualNetwork = Get-AzVirtualNetwork -Name "resvnet" -ResourceGroupName "testresgroup"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetwork @($ResVirtualNetwork)
```

Эта команда создает новую частную зону DNS с именем myprivatezone.com в указанной группе ресурсов с связанным разрешением виртуальной сети (на нее ссылается переменная $ResVirtualNetwork), а затем сохраняет ее в переменной $Zone ресурса.

### Пример 4. Создание зоны DNS с делегирования путем указания имени родительской зоны
```
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZoneName "zone.com"
```

Эта команда создает новую зону DNS ребенка с именем mychild.zone.com в указанной группе ресурсов и сохраняет в переменной $Zone ресурса.
Она также добавляет делегирования в родительскую зону DNS zone.com в той же подписке и группе ресурсов, что и для детей.

### Пример 5. Создание зоны DNS с делегирования путем указания родительского зоны
```
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZoneId "/subscriptions/**67e2/resourceGroups/other-rg/providers/Microsoft.Network/dnszones/zone.com"
```

Эта команда создает новую зону DNS ребенка с именем mychild.zone.com в указанной группе ресурсов и сохраняет ее в $Zone переменной.
Она также добавляет делегирования в родительскую зону DNS zone.com в группе ресурсов с другой предоставленной подпиской, то же, что и в созданной зоне для детей.

### Пример 6. Создание зоны DNS с делегирования путем указания объекта родительской зоны
```
PS C:\>$PZone = New-AzDnsZone -Name "zone.com" -ResourceGroupName "MyResourceGroup" 
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZone @($PZone)
```

Эта команда создает новую зону DNS ребенка с именем mychild.zone.com в указанной группе ресурсов и сохраняет в переменной $Zone ресурса.
Она также добавляет делегирования в родительскую зону DNS zone.com как переданную в объекте ParentZone.

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
Имя зоны DNS, которая будет создаваться.

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

### -ParentZone
Полное имя родительской зоны, в который нужно добавить делегирования (без конечной точки).

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ParentZoneId
ИД ресурса родительской зоны для добавления делегирования (без конечной точки).

```yaml
Type: System.String
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ParentZoneName
Полное имя родительской зоны, в который нужно добавить делегирования (без конечной точки).

```yaml
Type: System.String
Parameter Sets: Names
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RegistrationVirtualNetwork
Список виртуальных сетей, которые будут регистрировать записи об имени виртуальных машин в этой зоне DNS, доступен только для частных зон.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RegistrationVirtualNetworkId
Список виртуальных сетевых кодов, которые будут регистрировать записи об именах хостов виртуальных машин в этой зоне DNS, доступен только для частных зон.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResolutionVirtualNetwork
Список виртуальных сетей для разрешения записей в этой зоне DNS, доступный только для частных зон.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResolutionVirtualNetworkId
Список виртуальных сетевых ИД, которые можно разрешать записи в этой зоне DNS, доступен только для частных зон.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Определяет группу ресурсов, в которой нужно создать зону.

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

### -Tag
Пары значений ключа в виде hash table. Например: @{key0="value0";key1=$null;key2="value2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ZoneType
Тип зоны (общедоступный или закрытый). Зоны без типа и с типом "Общедоступный" доступны в общедоступных DNS-компаниях, обслуживающих самолет, для использования в иерархии DNS. Зоны с типом "Частное" видны только в наборе связанных виртуальных сетей (функция предварительной версии). Это свойство нельзя изменить для зоны.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Dns.Models.ZoneType]
Parameter Sets: (All)
Aliases:
Accepted values: Public, Private

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Перед запуском cmdlet вам будет предложено подтвердить его.

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

### System.String

### System.Nullable'1[[Microsoft.Azure.Management.Dns.Models.ZoneType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]

### System.Collections.Hashtable

### System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.Collections.Generic.List'1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]

## OUTPUTS

### Microsoft.Azure.Commands.Dns.DnsZone

## ПРИМЕЧАНИЯ
С помощью параметра *Confirm* (Подтвердить) можно управлять запросом на подтверждение с помощью этого cmdlet.
По умолчанию с помощью cmdlet вы можете получить подтверждение, если переменная $ConfirmPreference Windows PowerShell имеет значение "Средний" или "Ниже".
Если указать *"Подтвердить"* или *"$True:$True",* этот cmdlet запросит подтверждение перед запуском.
Если *указать confirm:$False,* то при этом не будет предложено подтвердить запрос.

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzDnsZone](./Get-AzDnsZone.md)

[New-AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Remove-AzDnsZone](./Remove-AzDnsZone.md)
