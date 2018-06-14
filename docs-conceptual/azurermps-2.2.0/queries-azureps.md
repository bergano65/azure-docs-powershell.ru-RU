---
title: Обращение к ресурсам Azure и форматирование результатов | Документация Майкрософт
description: Как обратиться к ресурсам в Azure и форматировать результаты запроса.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: 1584c8166078b7d7d24ce8748307fde0f565b662
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2018
ms.locfileid: "34853481"
---
# <a name="querying-for-azure-resources"></a>Обращение к ресурсам Azure

Вы можете обращаться к ресурсам с помощью встроенных командлетов PowerShell. В PowerShell имена командлетов представлены в формате **_глагол-существительное_**. Командлеты, в которых используется глагол **_Get_** (Получить) — это командлеты запроса. Существительные командлета — это типы ресурсов Azure, к которым будет применено действие командлета.


## <a name="selecting-simple-properties"></a>Выбор простых свойств

Для каждого командлета Azure PowerShell определено форматирование по умолчанию. Самые распространенные свойства каждого типа ресурсов автоматически отображаются в формате таблицы или списка. Дополнительные сведения о форматировании выходных данных см. в статье о [форматировании результатов запроса](formatting-output.md).

Используйте командлет `Get-AzureRmVM`, чтобы получить список виртуальных машин своей учетной записи.

```powershell
Get-AzureRmVM
```

Результаты по умолчанию автоматически форматируются в виде таблицы.

```
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

Командлет `Select-Object` можно использовать для выбора определенных свойств, которые вас интересуют.

```powershell
Get-AzureRmVM | Select Name,ResourceGroupName,Location
```

```
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

## <a name="selecting-complex-nested-properties"></a>Выбор сложных вложенных свойств

Если вы хотите выбрать свойства, которые глубоко вложены в выходные данные JSON, необходимо указать полный путь к такому свойству. Следующий пример показывает, как выбрать имя виртуальной машины и тип ОС с помощью командлета `Get-AzureRmVM`.

```powershell
Get-AzureRmVM | Select Name,@{Name='OSType'; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```
Name           OSType
----           ------
MyUnbuntu1610   Linux
MyWin2016VM   Windows
```

## <a name="filter-result-using-the-where-object-cmdlet"></a>Фильтрация результатов с помощью командлета Where-Object

Командлет `Where-Object` позволяет фильтровать результаты на основе любого значения свойства. В следующем примере фильтр выбирает только виртуальные машины, имя которых содержит текст RGD.

```powershell
Get-AzureRmVM | Where ResourceGroupName -like RGD* | Select ResourceGroupName,Name
```

```
ResourceGroupName  Name
-----------------  ----
RGDEMO001          KBDemo001VM
RGDEMO001          KBDemo020
```

В следующем примере результаты вернут виртуальные машины размера Standard_DS1_V2.

```powershell
Get-AzureRmVM | Where vmSize -eq Standard_DS1_V2
```

```
ResourceGroupName          Name     Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----     --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610   westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM   westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```
