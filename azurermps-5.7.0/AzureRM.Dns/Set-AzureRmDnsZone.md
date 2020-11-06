---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/set-azurermdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsZone.md
ms.openlocfilehash: da504f6b8110335e6297d0c7efb2a1a27106e0e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559060"
---
# Set-AzureRmDnsZone

## КРАТКИй обзор
Обновление свойств зоны DNS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### Поля (по умолчанию)
```
Set-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### FieldsObjects
```
Set-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DataObject
```
Set-AzureRmDnsZone -Zone <DnsZone> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzureRmDnsZone** обновляет указанную зону DNS в службе Azure DNS.
Этот командлет не обновляет наборы записей в зоне.

Вы можете передать объект **dnsZone** как параметр или с помощью оператора конвейера или указать параметры *zonename* и *ResourceGroupName* .

Вы можете использовать параметр *Confirm* и $ConfirmPreference переменной Windows PowerShell, чтобы указать, нужно ли командлету запрашивать подтверждение.

Если зона DNS была передана как объект (с помощью объекта Zone или канала), она не будет обновлена, если она была изменена в службе DNS Azure, поскольку был получен локальный объект DnsZone. Это обеспечивает защиту для параллельных изменений. Вы можете отключить это поведение с параметром *перезаписи* , который обновляет зону независимо от текущих изменений.

## ИЛЛЮСТРИРУЮТ

### Пример 1: обновление зоны DNS
```
PS C:\>$Zone = Get-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzureRmDnsZone -Zone $Zone
```

Первая команда получает зону с именем myzone.com из указанной группы ресурсов, а затем сохраняет ее в переменной $Zone.

Вторая команда обновляет теги для $Zone.

Последняя команда фиксирует изменения.

### Пример 2: обновление тегов для зоны
```
PS C:\>Set-AzureRmDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

Эта команда обновляет теги для зоны с именем myzone.com, но сначала явно не получает зону.

### Пример 3: связывание частной зоны с виртуальной сетью с указанием идентификатора
```
PS C:\>$vnet = Get-AzureRmVirualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzureRmDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetworkId @($vnet.Id)
```

Эта команда связывает личную зону DNS myprivatezone.com с виртуальной сетью myvnet как сеть регистрации, указав ее идентификатор.

### Пример 4: привязка частной зоны к виртуальной сети путем указания сетевого объекта.
```
PS C:\>$vnet = Get-AzureRmVirualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzureRmDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetwork @($vnet)
```

Эта команда связывает частную зону DNS myprivatezone.com с виртуальной сетью myvnet в качестве сети регистрации, передавая объект виртуальной сети, представленный переменной $vnet, в командлет Set-AzureRmDnsZone.

## ПАРАМЕТРЫ

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

### -Name (имя)
Указывает имя DNS-зоны, которую нужно обновить.

```yaml
Type: String
Parameter Sets: Fields, FieldsObjects
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Overwrite
Если зона DNS была передана как объект (с помощью объекта Zone или канала), она не будет обновлена, если она была изменена в службе DNS Azure, поскольку был получен локальный объект DnsZone. Это обеспечивает защиту для параллельных изменений. Вы можете отключить это поведение с параметром *перезаписи* , который обновляет зону независимо от текущих изменений.

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

### -RegistrationVirtualNetwork
Список виртуальных сетей, которые будут регистрировать записи hostname для виртуальных машин в этой зоне DNS, доступны только для частных зон.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: FieldsObjects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RegistrationVirtualNetworkId
Список идентификаторов виртуальных сетей, которые будут регистрировать записи hostname для виртуальных машин в этой зоне DNS, только для частных зон.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResolutionVirtualNetwork
Список виртуальных сетей, которые можно использовать для разрешения записей в этой зоне DNS, только для частных зон.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: FieldsObjects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResolutionVirtualNetworkId
Список идентификаторов виртуальных сетей, которые можно использовать для разрешения записей в этой зоне DNS, только для частных зон.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов, содержащей зону для обновления.
Кроме того, необходимо указать параметр ZoneName.

Кроме того, вы можете указать зону, используя объект DnsZone с параметром *зоны* или конвейером.

```yaml
Type: String
Parameter Sets: Fields, FieldsObjects
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Тег
Пары "ключ-значение" в виде хэш-таблицы. Например:

@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}

```yaml
Type: Hashtable
Parameter Sets: Fields, FieldsObjects
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
Указывает зону DNS для обновления.

Кроме того, вы можете указать зону с помощью параметров *zonename* и *ResourceGroupName* .

```yaml
Type: DnsZone
Parameter Sets: Object
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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Microsoft. Azure. Commands. DNS. DnsZone
Вы можете передать на этот командлет объект DnsZone.

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. DNS. DnsZone
Этот командлет возвращает объект DnsZone, который представляет обновленную зону DNS с новым тегом ETag.

## Пуск
Вы можете использовать параметр *Confirm* , чтобы указать, будет ли этот командлет запрашивать подтверждение.
По умолчанию командлет запрашивает подтверждение, если значение переменной $ConfirmPreference Windows PowerShell — средний или ниже.

Если вы задаете параметр *Confirm* или *Confirm: $true* , этот командлет запрашивает подтверждение перед запуском.
Если вы задаете значение *Confirm: $false* , командлет не будет запрашивать подтверждение.

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmDnsZone](./Get-AzureRmDnsZone.md)

[New-AzureRmDnsZone](./New-AzureRmDnsZone.md)

[Remove-AzureRmDnsZone](./Remove-AzureRmDnsZone.md)
