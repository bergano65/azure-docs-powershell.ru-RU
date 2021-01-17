---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloud.md
ms.openlocfilehash: 31400d3b9b6e57190a852ae579fffcaa9fc60401
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98423751"
---
# Get-AzVMWarePrivateCloud

## SYNOPSIS
Получите частное облако

## СИНТАКСИС

### Список1 (по умолчанию)
```
Get-AzVMWarePrivateCloud [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Получить
```
Get-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Список
```
Get-AzVMWarePrivateCloud -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## ОПИСАНИЕ
Получите частное облако

## ПРИМЕРЫ

### Пример 1. Список частного облака в рамках подписки
```powershell
PS C:\> Get-AzVMWarePrivateCloud

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

Перечислить частное облако в рамках подписки

### Пример 2. Список закрытого облака в группе ресурсов
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

Список закрытого облака в группе ресурсов

### Пример 3. Частное облако
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

Получить частное облако

## PARAMETERS

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Имя закрытого облака

```yaml
Type: System.String
Parameter Sets: Get
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов.
Имя нечувствительно к делу.

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
ИД целевой подписки.

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity

## OUTPUTS

### Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud

## ПРИМЕЧАНИЯ

ALIASES

СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ

Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства. Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.


INPUTOBJECT <IVMWareIdentity> : Параметр identity
  - `[AuthorizationName <String>]`: Имя авторизации каналов ExpressRoute в частном облаке
  - `[ClusterName <String>]`: название кластера в частном облаке
  - `[HcxEnterpriseSiteName <String>]`: имя корпоративного сайта HCX в частном облаке
  - `[Id <String>]`: путь удостоверения ресурса
  - `[Location <String>]`: регион Azure
  - `[PrivateCloudName <String>]`: Имя закрытого облака
  - `[ResourceGroupName <String>]`: Имя группы ресурсов. Имя нечувствительно к делу.
  - `[SubscriptionId <String>]`: ИД целевой подписки.

## СВЯЗАННЫЕ ССЫЛКИ

