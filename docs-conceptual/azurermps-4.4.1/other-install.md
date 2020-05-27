---
title: Другие методы установки Azure PowerShell | Документация Майкрософт
description: Как установить Azure PowerShell с помощью пакета MSI или установщика веб-платформы.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/06/2017
ms.openlocfilehash: 3f8963c98b26f971c1259dc89d5da1f35ce3015a
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "83386703"
---
# <a name="other-installation-methods"></a>Другие методы установки

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

Azure PowerShell можно установить разными способами. Предпочтительным является использование PowerShellGet с коллекцией PowerShell. Azure PowerShell можно установить в Windows с помощью установщика веб-платформы (WebPI) или с помощью MSI-файла из GitHub.

## <a name="install-on-windows-using-the-web-platform-installer"></a>Установка в Windows с помощью установщика веб-платформы

Установка последней версии Azure PowerShell из WebPI выполняется также, как и установка предыдущих версий.
Скачайте [пакет Azure PowerShell WebPI](https://aka.ms/webpi-azps) и запустите установку.

> [!NOTE]
> Если вы ранее установили модули Azure из коллекции PowerShell, то установщик автоматически удаляет их. Это облегчает использование среды за счет установки только одной версии Azure PowerShell. Но в некоторых сценариях может потребоваться установить несколько версий одновременно.
>
> Модули из коллекции PowerShell устанавливают модули в папку `$env:ProgramFiles\WindowsPowerShell\Modules`. А установщик WebPI устанавливает модули Azure в другую папку: `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.
>
> Если во время установки возникла ошибка, вы можете можно вручную удалить папки Azure\* в папке `$env:ProgramFiles\WindowsPowerShell\Modules` и повторить попытку установки.

По завершении установки ваш параметр `$env:PSModulePath` должен включать каталоги, содержащие командлеты Azure PowerShell. Используйте следующую команду, чтобы убедиться, что среда Azure PowerShell установлена правильно.

```powershell-interactive
# To make sure the Azure PowerShell module is available after you install
Get-InstalledModule -Name AzureRM -AllVersions | Select-Object Name, Version, Path
```

> [!NOTE]
> При установке с помощью WebPI может возникать известная проблема. Если из-за установки обновлений системы или других компонентов потребуется перезагрузка компьютера, это может привести к исключению из `$env:PSModulePath` пути установки Azure PowerShell.

При попытке загрузки или выполнения командлетов после установки может появиться следующее сообщение об ошибке:

```output
PS C:\> Login-AzureRmAccount
Login-AzureRmAccount : The term 'Login-AzureRmAccount' is not recognized as the name of a cmdlet,
function, script file, or operable program. Check the spelling of the name, or if a path was
included, verify that the path is correct and try again.
At line:1 char:1
+ Login-AzureRmAccount
+ ~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (Login-AzureRmAccount:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
```

Эту ошибку можно исправить при перезагрузке компьютера или импорте модуля, используя полный путь. Пример:

```powershell-interactive
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-on-windows-using-the-msi-package"></a>Установка в Windows с помощью пакета MSI

Azure PowerShell можно установить с помощью MSI-файла из [GitHub](https://github.com/Azure/azure-powershell/releases/latest). Если вы устанавливали предыдущие версии модулей Azure, то установщик автоматически удаляет их. Пакет MSI устанавливает модули в папку `$env:ProgramFiles\WindowsPowerShell\Modules`, но не создает папки для определенных версий.

