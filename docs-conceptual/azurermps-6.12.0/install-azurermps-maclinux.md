---
title: Установка Azure PowerShell в ОС macOS или Linux
description: Инструкции по установке Azure PowerShell в ОС macOS или Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/05/2018
ms.openlocfilehash: f60ea1c608be4b1c8319d53303713ba039276abc
ms.sourcegitcommit: 06f9206e025afa7207d4657c8f57c94ddb74817a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2018
ms.locfileid: "51213113"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a>Установка Azure PowerShell в ОС macOS или Linux

Для платформ, отличных от Windows, доступна альтернатива Azure PowerShell — PowerShell Core версии 6. Эта версия PowerShell предназначена для всех платформ, поддерживающих .NET Core. Для работы с этими платформами доступна версия Azure PowerShell для .NET Standard.

> [!NOTE]
> В настоящее время Azure PowerShell для .NET Standard предлагается в режиме бета-версии.
> Если у вас возникнут проблемы или вы обнаружите ошибки, сообщите об этом через сайт GitHub.
>
> * [Проблемы, связанные с Azure PowerShell](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a>Установка PowerShell Core

Инструкции по установке PowerShell Core отличаются для macOS и большинства дистрибутивов Linux.
Подробные инструкции можно найти в следующих статьях:

* [Установка PowerShell Core в macOS](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [Установка PowerShell Core в Linux](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-standard"></a>Установка Azure PowerShell для .NET Standard

> [!IMPORTANT]
> Модуль `AzureRM`, описанный в других статьях, не работает с PowerShell Core.
> Чтобы получить функциональность Azure PowerShell в PowerShell Core, необходимо установить модуль `Az`.

В PowerShell Core уже входит модуль PowerShellGet. Запустите PowerShell с помощью команды:

```bash
pwsh
```

Чтобы установить Azure PowerShell, выполните следующую команду:

```powershell-interactive
Install-Module Az
```

> [!NOTE]
> Если при попытке установить модуль возникает ошибка, связанная с разрешениями, возможно, для установки модулей вам нужно запустить PowerShell в режиме суперпользователя.
>
> ```bash
> sudo pwsh
> ```

По умолчанию коллекция PowerShell не используется как доверенный репозиторий для PowerShellGet. При первом использовании PSGallery отображается следующее сообщение:

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Ответьте `Yes` или `Yes to All`, чтобы продолжить установку.

## <a name="enable-aliases"></a>Включение псевдонимов

Для совместимости с существующим модулем `AzureRM` новый модуль `Az` получил возможность создавать обратно совместимые псевдонимы для командлетов `AzureRM`. Перед первым использованием модуля настройте эти псевдонимы с помощью следующей команды:

```powershell-interactive
# Import the module into the PowerShell session
Import-Module Az
# Enable AzureRM aliases for the user
Enable-AzureRmAlias -Scope CurrentUser
```

Псевдонимы будут настроены только для текущего пользователя. Сведения о других значениях, которые можно указать в параметре `-Scope` при настройке псевдонимов, см. в справке командлета.

> [!NOTE]
> Если возникла ошибка, связанная с расположением пути, убедитесь, что этот путь существует в локальной файловой системе. В области `CurrentUser` это ошибку можно устранить, выполнив следующую команду в `bash`:
>
> ```bash
> mkdir -p $HOME/.config/powershell
> ```

## <a name="sign-in"></a>Вход

Чтобы приступить к работе с Azure PowerShell, вам нужно загрузить `Az` в текущий сеанс PowerShell. Для этого воспользуйтесь командлетом [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), после чего войдите в систему с помощью своих учетных данных Azure. Для импорта модуля более высокий уровень привилегий __не__ требуется.

```powershell-interactive
# Import the module into the PowerShell session
Import-Module Az
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

Эти действия нужно повторять для каждого нового сеанса PowerShell. Чтобы автоматически импортировать модуль `Az`, необходимо настроить профиль PowerShell. Подробнее об этом рассказывается [здесь](/powershell/module/microsoft.powershell.core/about/about_profiles).
В macOS и Linux работа с профилем выполняется с использованием переменной среды `$Profile`. Чтобы узнать, как повторно использовать свои данные для входа в Azure в разных сеансах, см. статью [Использование учетных данных пользователя в разных сеансах PowerShell](context-persistence.md).

## <a name="next-steps"></a>Дальнейшие действия

Дополнительные сведения об использовании Azure PowerShell см. в статье [Начало работы с Azure PowerShell](get-started-azureps.md).
