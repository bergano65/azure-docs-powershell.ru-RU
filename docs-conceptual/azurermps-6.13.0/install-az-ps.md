---
title: Установка модуля Az для Azure PowerShell с помощью PowerShellGet
description: Сведения об установке Azure PowerShell с помощью PowerShellGet в Windows, macOS и Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/26/2018
ms.openlocfilehash: 3d52b18750341f220dc8e10d6bf89796457c5a10
ms.sourcegitcommit: 558436c824d9b59731aa9b963cdc8df4dea932e7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/29/2018
ms.locfileid: "52588185"
---
# <a name="install-the-azure-powershell-az-module"></a>Установка модуля Az для Azure PowerShell

В этой статье рассказывается, как установить модули Azure PowerShell с помощью PowerShellGet. Эти инструкции применимы для платформ Windows, macOS и Linux. В предварительной версии модуля Az другие методы установки не поддерживаются. 

## <a name="requirements"></a>Требования

Azure PowerShell работает с PowerShell 5.x в Windows, или PowerShell 6.x на любой платформе. Чтобы проверить установленную на своем компьютере версию PowerShell, выполните следующую команду:

```powershell-interactive
$PSVersionTable.PSVersion
```

Если вы используете старую версию или вам нужно установить PowerShell, см. статью [Установка разных версий PowerShell](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-powershell?view=powershell-6). На этой странице вы найдете ссылки на сведения по установке для своей платформы.

## <a name="install-the-azure-powershell-module"></a>Установка модуля Azure PowerShell

> [!IMPORTANT]
>
> Модули `AzureRM` и `Az` могут быть установлены одновременно. Если у вас установлены оба модуля, __не включайте псевдонимы__.
> Включение псевдонимов приведет к конфликтам между командлетами `AzureRM` и псевдонимами команд `Az` с непредсказуемыми результатами.
> Рекомендуется перед установкой модуля `Az` удалить `AzureRM`. Вы можете удалить `AzureRM` или включить псевдонимы в любое время. Инструкции по удалению см. в статье [Удаление модуля Azure PowerShell (AzureRM)](uninstall-azurerm-ps.md). 

Чтобы установить модули в глобальной области видимости, необходим более высокий уровень привилегий для установки модулей из коллекции PowerShell. Чтобы установить Azure PowerShell, выполните следующую команду в сеансе с более высоким уровнем привилегий ("Запуск от имени администратора" в Windows или с правами суперпользователя в macOS или Linux):

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

Если у вас нет доступа к привилегиям администратора, можно выполнить установку для текущего пользователя, добавив аргумент `-Scope`.

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

По умолчанию коллекция PowerShell не используется как доверенный репозиторий для PowerShellGet. При первом использовании PSGallery отображается следующее сообщение:

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Ответьте `Yes` или `Yes to All`, чтобы продолжить установку.

Модуль `Az` — это общий модуль для командлетов Azure PowerShell. Во время его установки скачиваются все доступные модули Azure Resource Manager и устанавливаются все соответствующие командлеты.

## <a name="sign-in"></a>Вход

Чтобы начать работу с Azure PowerShell, выполните вход, используя данные своей учетной записи в Azure.

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> Если вы отключили автоматическую загрузку модулей, вам нужно вручную импортировать модуль с помощью `Import-Module Az`. Из-за структуры модуля эта операция может занять несколько секунд.

Эти действия нужно повторять для каждого нового сеанса PowerShell. Чтобы узнать, как повторно использовать свои данные для входа в Azure в разных сеансах PowerShell, см. статью [Использование учетных данных пользователя в разных сеансах PowerShell](context-persistence.md).

## <a name="update-the-azure-powershell-module"></a>Обновление модуля Azure PowerShell

Чтобы обновить версию Azure PowerShell, выполните команду [Update-Module](/powershell/module/powershellget/update-module). Эта команда __не__ удаляет предыдущие версии.

```powershell-interactive
Update-Module -Name Az
```

Сведения о том, как удалить из системы предыдущие версии Azure PowerShell, см. в статье [Удаление модуля Azure PowerShell](uninstall-azurerm-ps.md).

## <a name="use-multiple-versions-of-azure-powershell"></a>Использование нескольких версий Azure PowerShell

Вы можете установить несколько версий Azure PowerShell. Чтобы проверить наличие нескольких установленных версий Azure PowerShell, используйте следующую команду:

```powershell-interactive
Get-Module -Name Az -List | select Name,Version
```

Сведения о том, как удалить версию Azure PowerShell, см. в статье [Удаление модуля Azure PowerShell](uninstall-azurerm-ps.md).

Вы можете загрузить определенную версию модуля `Az`, используя аргумент `-RequiredVersion` с командами `Install-Module` или `Import-Module`:

```powershell-interactive
Install-Module -Name Az -RequiredVersion 0.4.0
Import-Module -Name Az -RequiredVersion 0.4.0
```

Если у вас установлено несколько версий модуля, по умолчанию загружается последняя версия.

## <a name="provide-feedback"></a>Отзывы

Если вы нашли ошибку при работе с Azure Powershell, [сообщите о ней на сайте GitHub](https://github.com/Azure/azure-powershell/issues).
Чтобы отправить отзыв из командной строки, используйте командлет [Send-Feedback](/powershell/module/az.profile/send-feedback).

## <a name="next-steps"></a>Дальнейшие действия

Сведения о начале работы с Azure PowerShell см. в [этой статье](get-started-azureps.md). Она содержит более подробную информацию о модуле и его компонентах.
