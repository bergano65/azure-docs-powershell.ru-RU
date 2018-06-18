---
title: Другие способы установки Azure PowerShell
description: Как установить Azure PowerShell с помощью пакета MSI или установщика веб-платформы.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 0919583d9cb05a75fae3b812eed84109be8b28aa
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323277"
---
# <a name="other-installation-methods"></a>Другие методы установки

В этой статье описывается, как установить Azure PowerShell с использованием MSI или установщика веб-платформы (WebPI). Вы также можете запустить Azure PowerShell в контейнере Docker. Используйте эти способы установки только в том случае, если это необходимо для вашей системы. Стандартный вариант — установка Azure PowerShell через PowerShellGet. Инструкции по установке Azure PowerShell с помощью PowerShellGet см. в [этой статье](install-azurerm-ps.md).

Сведения об установке в средах Linux или macOS см. в [этом разделе](install-azurermps-maclinux.md).

## <a name="install-or-update-on-windows-using-the-web-platform-installer"></a>Установка или обновление в Windows с помощью установщика веб-платформы

Установка последней версии Azure PowerShell из WebPI выполняется также, как и установка предыдущих версий.
Скачайте [пакет Azure PowerShell WebPI](http://aka.ms/webpi-azps) и запустите установку.

> [!NOTE]
> Если вы ранее установили модули Azure из коллекции PowerShell, то установщик автоматически удаляет их. Это облегчает использование среды за счет установки только одной версии Azure PowerShell. Но в некоторых сценариях может потребоваться установить несколько версий одновременно.
>
> Модули из коллекции PowerShell устанавливают модули в папку `$env:ProgramFiles\WindowsPowerShell\Modules`. А установщик WebPI устанавливает модули Azure в другую папку: `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.
>
> Если во время установки возникла ошибка, вы можете вручную удалить папки `Azure*` в папке `$env:ProgramFiles\WindowsPowerShell\Modules` и повторить попытку установки.

По завершении установки ваш параметр `$env:PSModulePath` должен включать каталоги, содержащие командлеты Azure PowerShell. Используйте следующую команду, чтобы проверить, правильно ли установлена среда Azure PowerShell.

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

Эту ошибку можно исправить при перезагрузке компьютера или импорте модуля, используя полный путь.

```powershell
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-or-update-on-windows-using-the-msi-package"></a>Установка или обновление в Windows с помощью пакета MSI

Azure PowerShell можно установить с помощью MSI-файла из [GitHub](https://aka.ms/azps-release). Если вы устанавливали предыдущие версии модулей Azure, то установщик автоматически удаляет их. Пакет MSI устанавливает модули в папку `$env:ProgramFiles\WindowsPowerShell\Modules`, но не создает папки для определенных версий.

## <a name="run-in-a-docker-container"></a>Запуск в контейнере Docker

Мы поддерживаем набор образов Docker, предварительно настроенный с помощью Azure PowerShell. Доступны контейнеры двух типов: в одних используется стандартная версия PowerShell в среде Windows, а в других — версия PowerShell Core в среде Windows или Linux.

| Среда | Образ Docker |
|-------------|--------------|
| PowerShell в среде Windows | [azuresdk/azure-powershell](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| PowerShell Core в среде Windows | [azuresdk/azure-powershell-core:nanoserver](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| PowerShell Core в среде Linux | [azuresdk/azure-powershell-core:latest](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

Для запуска любого из этих контейнеров используйте `docker run -it $ImageName`, чтобы получить интерактивный терминал. Например, чтобы запустить контейнер с PowerShell Core в среде Linux, используйте следующую команду:

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> Чтобы запустить контейнер Windows в Docker, в качестве ОС узла должна использоваться ОС Windows, а Docker необходимо настроить для запуска контейнеров Windows. Дополнительные сведения о переключении между средами Windows и Linux в Docker см. в документации по Docker [о переключении между контейнерами Windows и Linux](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).