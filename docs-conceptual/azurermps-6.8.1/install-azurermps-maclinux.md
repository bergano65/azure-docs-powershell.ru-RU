---
title: Установка Azure PowerShell в ОС macOS или Linux
description: Инструкции по установке Azure PowerShell в ОС macOS или Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: 8347502df3c9cd6237a44293cfa3e5c051066940
ms.sourcegitcommit: bc88e64c494337821274d6a66c1edad656c119c5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/20/2018
ms.locfileid: "46300669"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a>Установка Azure PowerShell в ОС macOS или Linux

Для платформ, отличных от Windows, доступна альтернатива Azure PowerShell — PowerShell Core версии 6. Эта версия PowerShell предназначена для всех платформ, поддерживающих .NET Core. Для работы с этими платформами доступна особая версия Azure PowerShell — для .NET Core.

> [!NOTE]
> Сейчас PowerShell Core версии 6 и Azure PowerShell для .NET Core реализованы в бета-версии.
> Поддержка этих продуктов ограничена. Если у вас возникнут проблемы или вы обнаружите ошибки, сообщите об этом через сайт GitHub.
>
> * [Проблемы, связанные с PowerShell Core версии 6](https://github.com/PowerShell/PowerShell/issues)
> * [Проблемы, связанные с Azure PowerShell](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a>Установка PowerShell Core

Инструкции по установке PowerShell Core отличаются для macOS и большинства дистрибутивов Linux.
Подробные инструкции можно найти в следующих статьях:

* [Установка PowerShell Core в macOS](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [Установка PowerShell Core в Linux](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a>Установка Azure PowerShell для .NET Core

В PowerShell Core уже входит модуль PowerShellGet. Для установки модулей в PowerShell требуется более высокий уровень привилегий, поэтому вы должны запустить сеанс как суперпользователь.

```bash
sudo pwsh
```

Чтобы установить Azure PowerShell, выполните следующую команду:

```powershell
Install-Module AzureRM.NetCore
```

> [!IMPORTANT]
> Модуль `AzureRM`, описанный в других статьях, не предназначен для .NET Core и не будет работать с PowerShell Core. В обоих модулях, `AzureRM` и `AzureRM.NetCore`, используются одинаковые имена командлетов. Единственное отличие заключается в общем модуле и версии .NET, для которой они предназначены.

По умолчанию коллекция PowerShell не используется как доверенный репозиторий для PowerShellGet. При первом использовании PSGallery отображается следующее сообщение:

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Ответьте `Yes` или `Yes to All`, чтобы продолжить установку.

## <a name="sign-in"></a>Вход

Чтобы приступить к работе с Azure PowerShell, вам нужно загрузить `AzureRM.Netcore` в текущий сеанс PowerShell. Для этого воспользуйтесь командлетом [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), после чего войдите в систему с помощью своих учетных данных Azure. Для импорта модуля более высокий уровень привилегий __не__ требуется.

```powershell
# Import the module into the PowerShell session
Import-Module AzureRM.Netcore
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

Эти действия нужно повторять для каждого нового сеанса PowerShell. Чтобы автоматически импортировать модуль `AzureRM`, необходимо настроить профиль PowerShell. Подробнее об этом рассказывается [здесь](/powershell/module/microsoft.powershell.core/about/about_profiles).
В macOS и Linux работа с профилем выполняется с использованием переменной среды `$Profile`. Чтобы узнать, как повторно использовать свои данные для входа в Azure в разных сеансах, см. статью [Использование учетных данных пользователя в разных сеансах PowerShell](context-persistence.md).

## <a name="available-cmdlets"></a>Доступные командлеты

Модули Azure PowerShell для .NET Core еще находятся в разработке. Эти модули не обеспечивают полный набор командлетов, которые доступны в версии модулей для Windows. В модулях AzureRM.Netcore реализованы следующие функции.

* Управление учетными записями
  * Вход с помощью учетной записи Майкрософт, рабочей или учебной учетной записи или субъекта-службы с помощью Microsoft Azure Active Directory.
  * Сохранение учетных данных на диск с помощью командлета Save-AzureRmContext и загрузка сохраненных учетных данных с помощью командлета Import-AzureRmContext.
* Среда
  * Получение различных стандартных сред Microsoft Azure.
  * Добавление, настройка и удаление настроенных сред (например, сред Azure Stack или Windows Azure Pack).
* Командлеты плоскости управления для служб Azure, использующих интерфейсы классической модели развертывания и развертывания с помощью Resource Manager.
  * Виртуальная машина
  * Служба приложений (веб-сайты)
  * База данных SQL
  * служба хранилища.
  * Сеть

## <a name="next-steps"></a>Дальнейшие действия

Дополнительные сведения об использовании Azure PowerShell см. в статье [Начало работы с Azure PowerShell](get-started-azureps.md).
