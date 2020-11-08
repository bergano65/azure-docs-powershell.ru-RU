---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsZone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
ms.openlocfilehash: 06b8a8bd7027b95d7f51e186b0184707ffd296a8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065472"
---
# Set-AzPrivateDnsZone

## КРАТКИй обзор
Обновление частной зоны DNS из группы ресурсов.

## Максимальное

### Поля (по умолчанию)
```
Set-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceId
```
Set-AzPrivateDnsZone -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DataObject
```
Set-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Tag <Hashtable>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzPrivateDnsZone** постоянно обновляет закрытую зону доменных имен (DNS) для указанной группы ресурсов.
Вы можете передать объект **PrivateDnsZone** с помощью параметра *PrivateZone* или с помощью оператора конвейера или можно указать параметры *Name* и *ResourceGroupName* .
Вы можете использовать параметр Confirm и $ConfirmPreference переменной Windows PowerShell, чтобы указать, нужно ли командлету запрашивать подтверждение.
При указании зоны с помощью объекта **PrivateDnsZone** (который передается через конвейер или параметр *зоны* ), зона не обновляется, если она была изменена в Azure DNS с момента получения изменений локального объекта **PrivateDnsZone** (операции с наборами записей в этой зоне не будут возобновляться в соответствии с изменениями.
Это обеспечивает защиту для одновременных изменений зоны.
Это может быть подавлено с помощью параметра *overwrite* , который обновляет зону независимо от текущих изменений.

## ИЛЛЮСТРИРУЮТ

### Пример 1: обновление частной зоны
```
PS C:\>Set-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup" -Tag @{tag1="value1";tag2="value2"}


This command updates the zone named myzone.com from the resource group named MyResourceGroup with the tags provided. Use Get-AzPrivateDnsZone to retrieve the updated zone. Updated zone would look something like this:

Name                          : myzone.com
ResourceId                    : "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/PrivateZones/myzone.com"
ResourceGroupName             : MyResourceGroup
Location                      : 
Etag                          : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                          : {tag1="value1";tag2="value2"}
NumberOfRecordSets            : 1
MaxNumberOfRecordSets         : 5000
```

## ПАРАМЕТРЫ

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

### -Name (имя)
Указывает имя частной DNS-зоны, которая обновляется этим командлетом.
Кроме того, необходимо указать параметр *ResourceGroupName* .
Кроме того, вы можете указать частную зону DNS с помощью параметра *Zone* .

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Overwrite
При указании зоны с помощью объекта **PrivateDnsZone** (который передается через конвейер или параметр *зоны* ), зона не обновляется, если она была изменена в Azure DNS с момента получения изменений локального объекта **dnsZone** (операции с наборами записей в этой зоне не будут возобновляться в соответствии с изменениями.
Это обеспечивает защиту для одновременных изменений зоны.
Это может быть подавлено с помощью параметра *overwrite* , который обновляет зону независимо от текущих изменений.

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

### -PrivateZone
Объект зоны, который нужно настроить.

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов, содержащей зону, которую нужно обновить.
Кроме того, необходимо указать параметр *zonename* .
Кроме того, вы можете указать частную DNS-зону с помощью объекта **dnsZone** , передаваемого через конвейер или параметр *Zone* .

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Частный секретный ИД зоны DNS.

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Тег
Хэш-таблица, представляющая Теги ресурсов.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Запрашивает подтверждение перед запуском командлета.

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
Показывает, что произойдет при запуске командлета.
Командлет не выполняется.

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String

### Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsZone

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsZone

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzPrivateDnsZone](./Get-AzPrivateDnsZone.md)

[New-AzPrivateDnsZone](./New-AzPrivateDnsZone.md)

[Set-AzPrivateDnsZone](./Set-AzPrivateDnsZone.md)
