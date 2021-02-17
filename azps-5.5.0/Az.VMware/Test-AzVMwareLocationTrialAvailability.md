---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/test-azvmwarelocationtrialavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Test-AzVMwareLocationTrialAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Test-AzVMwareLocationTrialAvailability.md
ms.openlocfilehash: f667e5f2c6f85e06e1d16a35b1279d88af5e2ed7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100229564"
---
# Test-AzVMwareLocationTrialAvailability

## SYNOPSIS
Возврат состояния пробной подписки по регионам

## СИНТАКСИС

### Проверка (по умолчанию)
```
Test-AzVMwareLocationTrialAvailability -Location <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### CheckViaIdentity
```
Test-AzVMwareLocationTrialAvailability -InputObject <IVMwareIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## ОПИСАНИЕ
Возврат состояния пробной подписки по регионам

## ПРИМЕРЫ

### Пример 1. Проверка доступности пробной версия
```powershell
PS C:\> Test-AzVMwareLocationTrialAvailability -Location australiaeast

AvailableHost Status
------------- ------
0             TrialDisabled
```

Проверка доступности пробной версия

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
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity
Parameter Sets: CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Location
Регион Azure

```yaml
Type: System.String
Parameter Sets: Check
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
Type: System.String
Parameter Sets: Check
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity

## OUTPUTS

### Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.ITrial

## ПРИМЕЧАНИЯ

ALIASES

СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ

Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства. Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.


INPUTOBJECT <IVMwareIdentity> : Параметр identity
  - `[AuthorizationName <String>]`: Имя авторизации каналов ExpressRoute в частном облаке
  - `[ClusterName <String>]`: название кластера в частном облаке
  - `[HcxEnterpriseSiteName <String>]`: имя корпоративного сайта HCX в частном облаке
  - `[Id <String>]`: путь удостоверения ресурса
  - `[Location <String>]`: регион Azure
  - `[PrivateCloudName <String>]`: Имя закрытого облака
  - `[ResourceGroupName <String>]`: Имя группы ресурсов. Имя нечувствительно к делу.
  - `[SubscriptionId <String>]`: ИД целевой подписки.

## СВЯЗАННЫЕ ССЫЛКИ

