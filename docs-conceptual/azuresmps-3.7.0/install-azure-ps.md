---
title: Установка и настройка модуля управления службами Azure PowerShell | Документация Майкрософт
description: Как установить и настроить Azure PowerShell для первого использования.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/06/2017
ms.openlocfilehash: f46fe25352c100976dd8fc3b1c48ddfc3926f906
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/08/2018
---
# <a name="installing-the-azure-powershell-service-management-module"></a>Установка модуля управления службами Azure PowerShell

Предпочтительный способ установки Azure PowerShell — из [коллекции PowerShell](https://www.powershellgallery.com/).

## <a name="step-1-install-powershellget"></a>Шаг 1. Установка PowerShellGet

Чтобы установить элементы из коллекции PowerShell, требуется модуль PowerShellGet. Убедитесь, что в системе установлена соответствующая версия PowerShellGet и что выполнены другие требования к системе. Выполните следующую команду, чтобы определить наличие PowerShellGet в вашей системе:

```powershell
Get-Module PowerShellGet -list | Select-Object Name,Version,Path
```

Должен отобразиться похожий результат:

```
Name          Version Path
----          ------- ----
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

Если у вас не установлен PowerShellGet, перейдите к разделу [Как получить PowerShellGet](#how-to-get-powershellget).

## <a name="step-2-install-azure-powershell"></a>Шаг 2. Установка Azure PowerShell

Войдите в консоль Windows PowerShell с правами администратора и выполните следующую команду:

```powershell
Install-Module Azure
```

Модуль Azure — это модуль свертки для командлетов Azure Resource Manager. При установке модуля AzureRM из коллекции PowerShell будут скачаны и установлены все модули Azure, которые ранее не были установлены.

Модуль управления службой Azure использует те же зависимости, что и модули Azure PowerShell Resource Manager. Если вы установили модули Azure PowerShell Resource Manager, необходимо добавить параметр `-AllowClobber` в команду установки. Таким образом все существующие общие зависимости будут обновлены. Если этот параметр отсутствует, происходит сбой установки модуля.

```powershell
Install-Module Azure -AllowClobber
```

После установки этого модуля вы можете импортировать модуль, выполнив следующую команду:

```powershell
Import-Module Azure
```

## <a name="to-use-the-cmdlets"></a>Использование командлетов

Чтобы начать работу с командлетами управления службами Azure, сначала войдите в свою учетную запись Azure. Чтобы войти в учетную запись, выполните следующую команду:

```powershell
Add-AzureAccount
```

Когда вы войдете в Azure, Azure PowerShell создаст контекст для этого сеанса. Этот контекст содержит среду Azure PowerShell, учетную запись, клиент и подписку, которые будут использоваться для всех командлетов в этом сеансе. Теперь вы готовы использовать следующие модули.

## <a name="azure-service-management-cmdlets"></a>Командлеты для управления службами Azure

Модули Azure PowerShell часто обновляются. Если вы заметили, что онлайн-справка по командлетам содержит командлеты и параметры, которых нет в вашем модуле, скачайте и установите последнюю версию модуля. Чтобы найти версию своего модуля, введите: `(Get-Module Azure).Version`.

Примеры скриптов, с помощью которых можно автоматизировать некоторые распространенные задачи в Azure, см. в [центре скриптов Microsoft Azure](http://www.windowsazure.com/documentation/scripts/).

Общие сведения об установке, обучении, использовании и настройке Windows PowerShell см. в статье, посвященной [работе со скриптами в Windows PowerShell](http://go.microsoft.com/fwlink/p/?linkid=320210).

### <a name="how-to-get-powershellget"></a>Как получить PowerShellGet

|Версия ОС|Инструкции по установке|
|---|---|
|Используется Windows 10 или Windows Server 2016|Встроены в Windows Management Framework (WMF) 5.0, которая входит в состав ОС|
|Необходимо выполнить обновление до версии PowerShell 5|[Установите последнюю версию WMF](https://www.microsoft.com/en-us/download/details.aspx?id=54616)|
|Используется версия Windows с PowerShell 3 или PowerShell 4|[Скачайте модули PackageManagement](http://go.microsoft.com/fwlink/?LinkID=746217)|

<a id="helpmechoose"></a>
### <a name="checking-the-version-of-azure-powershell"></a>Проверка версии Azure PowerShell

Хотя мы советуем выполнить обновление до последней версии как можно раньше, несколько версий Azure PowerShell все еще поддерживаются. Чтобы определить, какая версия Azure PowerShell установлена, выполните в командной строке команду `Get-Module AzureRM`.

```powershell
Get-Module AzureRM -list | Select-Object Name,Version,Path
```
