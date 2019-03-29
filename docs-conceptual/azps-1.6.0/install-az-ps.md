---
title: Установка Azure PowerShell с помощью PowerShellGet
description: Инструкции по установке Azure PowerShell с помощью PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 269119333b2197a15ed7bb50e3e5d90588456174
ms.sourcegitcommit: 8f59e11e5c991543964154d63648aa1e6ae22512
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/26/2019
ms.locfileid: "58475531"
---
# <a name="install-the-azure-powershell-module"></a>Установка модуля Azure PowerShell

В этой статье рассказывается, как установить модули Azure PowerShell с помощью PowerShellGet. Эти инструкции применимы для платформ Windows, macOS и Linux. В данный момент другие методы установки не поддерживаются для модуля Az.

## <a name="requirements"></a>Требования

Azure PowerShell работает с PowerShell 5.1 или более высокой версии на платформе Windows или с PowerShell 6 на любой платформе.
Чтобы узнать вашу версию PowerShell, выполните приведенную ниже команду:

```powershell-interactive
$PSVersionTable.PSVersion
```

Если вы используете старую версию или вам нужно установить PowerShell, см. статью [Установка разных версий PowerShell](/powershell/scripting/setup/installing-powershell). На этой странице вы найдете ссылки на сведения по установке для своей платформы.

Если вы используете PowerShell 5 на Windows, необходимо также установить .NET Framework 4.7.2. Инструкции по обновлению или установке новой версии платформы .NET Framework см. в разделе [Руководство по установке](/dotnet/framework/install).

## <a name="install-the-azure-powershell-module"></a>Установка модуля Azure PowerShell

> [!IMPORTANT]
>
> Модули AzureRM и Az могут быть установлены одновременно. Если у вас установлены оба модуля, __не включайте псевдонимы__.
> Включение псевдонимов приведет к конфликтам между командлетами AzureRM и псевдонимами команд Az с непредсказуемыми результатами.
> Перед установкой модуля Az рекомендуется удалить AzureRM. Удалить AzureRM или включить псевдонимы можно в любое время. Дополнительные сведения о псевдонимах команд AzureRM см. в статье [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md) (Миграция с AzureRM на Az для Azure PowerShell).
> Инструкции по удалению см. в разделе [Uninstall the AzureRM module](uninstall-az-ps.md#uninstall-the-azurerm-module) (Удаление модуля AzureRM). 

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

Модуль Az — это общий модуль для командлетов Azure PowerShell. Во время его установки скачиваются все доступные модули Azure Resource Manager и устанавливаются все соответствующие командлеты.

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

Сведения о том, как удалить из системы предыдущие версии Azure PowerShell, см. в статье [Uninstall the Azure PowerShell module](uninstall-az-ps.md) (Удаление модуля Azure PowerShell).

## <a name="use-multiple-versions-of-azure-powershell"></a>Использование нескольких версий Azure PowerShell

Вы можете установить несколько версий Azure PowerShell. Чтобы проверить наличие нескольких установленных версий Azure PowerShell, используйте следующую команду:

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

Сведения о том, как удалить версию Azure PowerShell, см. в статье [Удаление модуля Azure PowerShell](uninstall-az-ps.md).

Определенную версию модуля `Az` можно установить или загрузить с помощью аргумента `-RequiredVersion`.

```powershell-interactive
# Install Az version 0.7.0
Install-Module -Name Az -RequiredVersion 0.7.0 
# Load Az version 0.7.0
Import-Module -Name Az -RequiredVersion 0.7.0
```

Если у вас установлено несколько версий модуля, модуль автозагрузки и `Import-Module` загрузит последнюю версию по умолчанию.

## <a name="provide-feedback"></a>Отзывы

Если вы нашли ошибку при работе с Azure Powershell, сообщите о ней [на сайте GitHub](https://github.com/Azure/azure-powershell/issues).
Чтобы отправить отзыв из командной строки, используйте командлет [Send-Feedback](/powershell/module/az.accounts/send-feedback).

## <a name="next-steps"></a>Дальнейшие действия

Дополнительные сведения о модулях Azure PowerShell и их функциях см. в статье [Get Started with Azure PowerShell](get-started-azureps.md) (Начало работы с Azure PowerShell).
Если вы знакомы с Azure PowerShell и вам необходимо мигрировать из AzureRM, см. статью [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md) (Миграция с AzureRM на Az).
