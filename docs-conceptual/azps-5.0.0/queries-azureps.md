---
title: Выходные данные запроса командлетов Azure PowerShell
description: Как обратиться к ресурсам в Azure и форматировать результаты запроса.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/10/2019
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 2754df5132ca9d528217fa5caad95b7f59cc8215
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92753926"
---
# <a name="query-output-of-azure-powershell"></a>Выходные данные запроса к Azure PowerShell 

Результаты каждого командлета Azure PowerShell представлены в виде объекта Azure PowerShell. Даже командлеты, не являющиеся явными операциями `Get-`, могут возвращать значение, которое можно проверить, чтобы получить информацию о созданном или измененном ресурсе. Хотя большинство командлетов возвращают один объект, некоторые возвращают массив, для которого необходимо выполнять итерацию.

Практически во всех случаях запрос возвращает выходные данные Azure PowerShell с помощью командлета [Select-Object](/powershell/module/Microsoft.PowerShell.Utility/Select-Object), который часто сокращается до `select`. Выходные данные можно отфильтровать с помощью [Where-Object](/powershell/module/Microsoft.PowerShell.Core/Where-Object) или его псевдонима `where`.

## <a name="select-simple-properties"></a>Выбор простых свойств

В формате таблицы по умолчанию для командлетов Azure PowerShell не отображаются все доступные свойства. Полный список свойств можно получить, воспользовавшись командлетом [Format-List](/powershell/module/microsoft.powershell.utility/format-list) или передав выходные данные в `Select-Object *`:

```azurepowershell-interactive
Get-AzVM -Name TestVM -ResourceGroupName TestGroup | Select-Object *
```

```output
ResourceGroupName        : TESTGROUP
Id                       : /subscriptions/711d8ed1-b888-4c52-8ab9-66f07b87eb6b/resourceGroups/TESTGROUP/providers/Micro
                           soft.Compute/virtualMachines/TestVM
VmId                     : 711d8ed1-b888-4c52-8ab9-66f07b87eb6b
Name                     : TestVM
Type                     : Microsoft.Compute/virtualMachines
Location                 : westus2
LicenseType              :
Tags                     : {}
AvailabilitySetReference :
DiagnosticsProfile       :
Extensions               : {}
HardwareProfile          : Microsoft.Azure.Management.Compute.Models.HardwareProfile
InstanceView             :
NetworkProfile           : Microsoft.Azure.Management.Compute.Models.NetworkProfile
OSProfile                : Microsoft.Azure.Management.Compute.Models.OSProfile
Plan                     :
ProvisioningState        : Succeeded
StorageProfile           : Microsoft.Azure.Management.Compute.Models.StorageProfile
DisplayHint              : Compact
Identity                 :
Zones                    : {}
FullyQualifiedDomainName :
AdditionalCapabilities   :
RequestId                : 711d8ed1-b888-4c52-8ab9-66f07b87eb6b
StatusCode               : OK
```

Как только вы узнаете имена интересующих вас свойств, такие имена можно будет использовать с `Select-Object`, чтобы получить свойства напрямую:

```azurepowershell-interactive
Get-AzVM -Name TestVM -ResourceGroupName TestGroup | Select-Object Name,VmId,ProvisioningState
```

```output
Name   VmId                                 ProvisioningState
----   ----                                 -----------------
TestVM 711d8ed1-b888-4c52-8ab9-66f07b87eb6b Succeeded
```

Результат выполнения `Select-Object` всегда форматируется для отображения запрашиваемой информации. Чтобы узнать об использовании форматирования в качестве части результатов запроса командлета, см. статью [Форматирование выходных данных командлетов Azure PowerShell](formatting-output.md).

## <a name="select-nested-properties"></a>Выбор вложенных свойств

В некоторых свойствах выходных данных командлета Azure PowerShell используются вложенные объекты, например свойство `StorageProfile` в выходных данных `Get-AzVM`. Чтобы получить значение из вложенного свойства, укажите отображаемое имя и полный путь к значению, которое необходимо проверить, как часть аргумента словаря в `Select-Object`:

```azurepowershell-interactive
Get-AzVM -ResourceGroupName TestGroup | `
    Select-Object Name,@{Name="OSType"; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```output
Name     OSType
----     ------
TestVM    Linux
TestVM2   Linux
WinVM   Windows
```

Каждый аргумент словаря выбирает одно свойство из объекта. Извлекаемое свойство должно быть частью выражения.

## <a name="filter-results"></a>Фильтрация результатов 

Командлет `Where-Object` позволяет фильтровать результаты в зависимости от любого значения свойства, включая вложенные свойства. В следующем примере показано, как использовать `Where-Object` для поиска виртуальных машин Linux в группе ресурсов.

```azurepowershell-interactive
Get-AzVM -ResourceGroupName TestGroup | `
    Where-Object {$_.StorageProfile.OSDisk.OSType -eq "Linux"}
```

```output
ResourceGroupName    Name Location          VmSize OsType        NIC ProvisioningState Zone
-----------------    ---- --------          ------ ------        --- ----------------- ----
TestGroup          TestVM  westus2 Standard_D2s_v3  Linux  testvm299         Succeeded
TestGroup         TestVM2  westus2 Standard_D2s_v3  Linux testvm2669         Succeeded
```

Вы можете передать результаты `Select-Object` и `Where-Object` из одного командлета в другой. Чтобы повысить производительность, рекомендуем поместить операцию `Where-Object` перед `Select-Object`:

```azurepowershell-interactive
Get-AzVM -ResourceGroupName TestGroup | `
    Where-Object {$_.StorageProfile.OsDisk.OsType -eq "Linux"} | `
    Select-Object Name,VmID,ProvisioningState
```

```output
Name    VmId                                 ProvisioningState
----    ----                                 -----------------
TestVM  711d8ed1-b888-4c52-8ab9-66f07b87eb6  Succeeded
TestVM2 cbcee769-dd78-45e3-a14d-2ad11c647d0  Succeeded
```
