---
title: Выходные данные запроса командлетов Azure PowerShell
description: Как обратиться к ресурсам в Azure и форматировать результаты запроса.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: 6bd1bea43303e9f5a2b46d63a3ac51b4c4031b9f
ms.sourcegitcommit: 4afdba3cd7e1d348876ce59f3503fdcd258f79ab
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/15/2018
ms.locfileid: "51575864"
---
# <a name="query-output-of-azure-powershell-cmdlets"></a>Выходные данные запроса командлетов Azure PowerShell

Вы можете обращаться к ресурсам с помощью встроенных командлетов PowerShell. В PowerShell имена командлетов представлены в формате **_глагол-существительное_**. Командлеты, в которых используется глагол **_Get_** (Получить) — это командлеты запроса. Существительные командлета — это типы ресурсов Azure, к которым будет применено действие командлета.

## <a name="select-simple-properties"></a>Выбор простых свойств

Для каждого командлета Azure PowerShell определено форматирование по умолчанию. Самые распространенные свойства каждого типа ресурсов автоматически отображаются в формате таблицы или списка. Дополнительные сведения о форматировании выходных данных см. в статье о [форматировании результатов запроса](formatting-output.md).

Используйте командлет `Get-AzureRmVM`, чтобы получить список виртуальных машин своей учетной записи.

```azurepowershell-interactive
Get-AzureRmVM
```

Результаты по умолчанию автоматически форматируются в виде таблицы.

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

Командлет `Select-Object` можно использовать для выбора определенных свойств, которые вас интересуют.

```azurepowershell-interactive
Get-AzureRmVM | Select Name,ResourceGroupName,Location
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

## <a name="select-complex-nested-properties"></a>Выбор сложных вложенных свойств

Если требуется выбрать свойство, вложенное в выходные данные JSON, укажите полный путь к такому свойству. Следующий пример показывает, как выбрать имя виртуальной машины и тип ОС с помощью командлета `Get-AzureRmVM`.

```azurepowershell-interactive
Get-AzureRmVM | Select Name,@{Name='OSType'; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```output
Name           OSType
----           ------
MyUnbuntu1610   Linux
MyWin2016VM   Windows
```

## <a name="filter-results-with-the-where-object-cmdlet"></a>Фильтрация результатов с помощью командлета Where-Object

Командлет `Where-Object` позволяет фильтровать результаты на основе любого значения свойства. В следующем примере фильтр выбирает только виртуальные машины, имя которых содержит текст RGD.

```azurepowershell-interactive
Get-AzureRmVM | Where ResourceGroupName -like RGD* | Select ResourceGroupName,Name
```

```output
ResourceGroupName  Name
-----------------  ----
RGDEMO001          KBDemo001VM
RGDEMO001          KBDemo020
```

В следующем примере результаты вернут виртуальные машины размера Standard_DS1_V2.

```azurepowershell-interactive
Get-AzureRmVM | Where vmSize -eq Standard_DS1_V2
```

```output
ResourceGroupName          Name     Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----     --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610   westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM   westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```