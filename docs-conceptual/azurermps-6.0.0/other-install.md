---
title: Другие методы установки Azure PowerShell | Документация Майкрософт
description: Как установить Azure PowerShell с помощью пакета MSI или установщика веб-платформы.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/06/2017
ms.openlocfilehash: fd5263a327fa8e4b70418bf6fa7702d8c5383733
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/08/2018
ms.locfileid: "33911958"
---
# <a name="other-installation-methods"></a>Другие методы установки

Azure PowerShell можно установить разными способами. Предпочтительным является использование PowerShellGet с коллекцией PowerShell. Azure PowerShell можно установить в Windows с помощью установщика веб-платформы (WebPI) или с помощью MSI-файла из GitHub. Также можно установить Azure PowerShell в контейнер Docker.

## <a name="install-on-windows-using-the-web-platform-installer"></a>Установка в Windows с помощью установщика веб-платформы

Установка последней версии Azure PowerShell из WebPI выполняется также, как и установка предыдущих версий.
Скачайте [пакет Azure PowerShell WebPI](http://aka.ms/webpi-azps) и запустите установку.

> [!NOTE]
> Если вы ранее установили модули Azure из коллекции PowerShell, то установщик автоматически удаляет их. Это облегчает использование среды за счет установки только одной версии Azure PowerShell. Но в некоторых сценариях может потребоваться установить несколько версий одновременно.
>
> Модули из коллекции PowerShell устанавливают модули в папку `$env:ProgramFiles\WindowsPowerShell\Modules`. А установщик WebPI устанавливает модули Azure в другую папку: `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.
>
> Если во время установки возникла ошибка, вы можете можно вручную удалить папки Azure* в каталоге `$env:ProgramFiles\WindowsPowerShell\Modules` и повторить попытку установки.

По завершении установки ваш параметр `$env:PSModulePath` должен включать каталоги, содержащие командлеты Azure PowerShell. Используйте следующую команду, чтобы убедиться, что среда Azure PowerShell установлена правильно.

```powershell
# To make sure the Azure PowerShell module is available after you install
Get-Module -ListAvailable Azure* | Select-Object Name, Version, Path
```

> [!NOTE]
> При установке с помощью WebPI может возникать известная проблема. Если из-за установки обновлений системы или других компонентов потребуется перезагрузка компьютера, это может привести к исключению из `$env:PSModulePath` пути установки Azure PowerShell.

При попытке загрузки или выполнения командлетов после установки может появиться следующее сообщение об ошибке:

```
PS C:\> Connect-AzureRmAccount
Connect-AzureRmAccount : The term 'Connect-AzureRmAccount' is not recognized as the name of a cmdlet,
function, script file, or operable program. Check the spelling of the name, or if a path was
included, verify that the path is correct and try again.
At line:1 char:1
+ Connect-AzureRmAccount
+ ~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (Connect-AzureRmAccount:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
```

Эту ошибку можно исправить при перезагрузке компьютера или импорте модуля, используя полный путь. Например: 

```powershell
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-on-windows-using-the-msi-package"></a>Установка в Windows с помощью пакета MSI

Azure PowerShell можно установить с помощью MSI-файла из [GitHub](https://aka.ms/azps-release). Если вы устанавливали предыдущие версии модулей Azure, то установщик автоматически удаляет их. Пакет MSI устанавливает модули в папку `$env:ProgramFiles\WindowsPowerShell\Modules`, но не создает папки для определенных версий.

## <a name="install-in-a-docker-container"></a>Установка в контейнер Docker

Мы поддерживаем образ Docker, предварительно настроенный с помощью Azure PowerShell.

Запустите контейнер с помощью команды `docker run`.

```powershell
docker run azuresdk/azure-powershell
```

Кроме того, мы поддерживаем подмножество командлетов в виде контейнера PowerShell Core.

Для платформ Mac и Linux используйте образ `latest`.

```bash
docker run azuresdk/azure-powershell-core:latest
```

Для платформы Windows используйте образ `nanoserver`.

```powershell
docker run azuresdk/azure-powershell-core:nanoserver
```

Azure PowerShell устанавливается в образ с помощью `Install-Module` из [коллекции PowerShell](https://www.powershellgallery.com/).
