---
title: Форматирование выходных данных командлетов Azure PowerShell
description: Сведения о том, как форматировать выходные данные командлетов для Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 390285bcf483e75b7a2b77d345ccb108669f66e5
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2019
ms.locfileid: "56153970"
---
# <a name="format-azurepowershell-cmdlet-output"></a>Форматирование выходных данных командлетов Azure PowerShell

По умолчанию каждый командлет Azure PowerShell заранее определяет форматирование выходных данных, что упрощает их чтение.  Среда PowerShell также позволяет гибко настраивать выходные данные или преобразовать выходные данные командлета в другой формат с помощью следующих командлетов:

| Форматирование      | Преобразование       |
|-----------------|------------------|
| [Format-Custom](/powershell/module/microsoft.powershell.utility/format-custom) | [ConvertTo-Csv](/powershell/module/microsoft.powershell.utility/convertto-csv)  |
| [Format-List](/powershell/module/microsoft.powershell.utility/format-list)   | [ConvertTo-Html](/powershell/module/microsoft.powershell.utility/convertto-html) |
| [Format-Table](/powershell/module/microsoft.powershell.utility/format-table)  | [ConvertTo-Json](/powershell/module/microsoft.powershell.utility/convertto-json) |
| [Format-Wide](/powershell/module/microsoft.powershell.utility/format-wide)   | [ConvertTo-Xml](/powershell/module/microsoft.powershell.utility/convertto-xml)  |

## <a name="format-examples"></a>Примеры форматирования

В этом примере показано, как получить список виртуальных машин Azure в подписке по умолчанию.  По умолчанию выходные данные команды `Get-AzureRmVM` представлены в табличном формате.

```azurepowershell-interactive
Get-AzureRmVM
```

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

Если вы хотите ограничить число возвращаемых столбцов, используйте командлет `Format-Table`. В следующем примере показано, как получить тот же список виртуальных машин, но ограничить выходные данные так, чтобы они содержали только имя виртуальной машины, группу ресурсов и расположение виртуальной машины.  Параметр `-Autosize` изменяет размеры столбцов в соответствии с размером данных.

```azurepowershell-interactive
Get-AzureRmVM | Format-Table Name,ResourceGroupName,Location -AutoSize
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

Выходные данные также можно отформатировать в виде списка. В следующем примере показано, как использовать командлет `Format-List`.

```azurepowershell-interactive
Get-AzureRmVM | Format-List Name,VmId,Location,ResourceGroupName
```

```output
Name              : MyUnbuntu1610
VmId              : 33422f9b-e339-4704-bad8-dbe094585496
Location          : westeurope
ResourceGroupName : MYWESTEURG

Name              : MyWin2016VM
VmId              : 4650c755-fc2b-4fc7-a5bc-298d5c00808f
Location          : westeurope
ResourceGroupName : MYWESTEURG
```

## <a name="convert-to-other-data-types"></a>Преобразование в другие типы данных

При помощи PowerShell также можно получить выходные данные команды и преобразовать их в несколько форматов данных. В следующем примере описано, как использовать командлет `Select-Object`, чтобы получить атрибуты виртуальных машин в нашей подписке и преобразовать выходные данные в формат CSV, который можно легко импортировать в базу данных или электронную таблицу.

```azurepowershell-interactive
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Csv -NoTypeInformation
```

```output
"ResourceGroupName","Id","VmId","Name","Location","ProvisioningState"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610","33422f9b-e339-4704-bad8-dbe094585496","MyUnbuntu1610","westeurope","Succeeded"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM","4650c755-fc2b-4fc7-a5bc-298d5c00808f","MyWin2016VM","westeurope","Succeeded"
```

Выходные данные можно также преобразовать в формат JSON.  В следующем примере создается тот же список виртуальных машин, но формат выходных данных меняется на JSON.

```azurepowershell-interactive
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Json
```

```output
[
    {
        "ResourceGroupName":  "MYWESTEURG",
        "Id":  "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTEURG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610",
        "VmId":  "33422f9b-e339-4704-bad8-dbe094585496",
        "Name":  "MyUnbuntu1610",
        "Location":  "westeurope",
        "ProvisioningState":  "Succeeded"
    },
    {
        "ResourceGroupName":  "MYWESTEURG",
        "Id":  "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTEURG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM",
        "VmId":  "4650c755-fc2b-4fc7-a5bc-298d5c00808f",
        "Name":  "MyWin2016VM",
        "Location":  "westeurope",
        "ProvisioningState":  "Succeeded"
    }
]
```
