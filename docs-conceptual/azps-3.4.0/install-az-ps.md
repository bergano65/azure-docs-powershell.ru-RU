---
title: Установка Azure PowerShell с помощью PowerShellGet
description: Инструкции по установке Azure PowerShell с помощью PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/22/2019
ms.openlocfilehash: 88861b63846db04e901d2a216657307c456c48fe
ms.sourcegitcommit: 9181f20c2c5eaa271150de9e25b9cb30ba5e6cb0
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2020
ms.locfileid: "77002934"
---
# <a name="install-the-azure-powershell-module"></a>Установка модуля Azure PowerShell

В этой статье рассказывается, как установить модули Azure PowerShell с помощью PowerShellGet. Эти инструкции применимы для платформ Windows, macOS и Linux. В данный момент другие методы установки не поддерживаются для модуля Az.

## <a name="requirements"></a>Требования

Azure PowerShell работает с PowerShell 5.1 или более поздней версии на платформе Windows или с PowerShell Core 6.x или более поздней версии на любых платформах. Если вы не уверены, установлена ли среда PowerShell, либо используете macOS или Linux, [установите последнюю версию PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core).

Чтобы узнать вашу версию PowerShell, выполните приведенную ниже команду:

```powershell-interactive
$PSVersionTable.PSVersion
```

Чтобы запустить Azure PowerShell в PowerShell 5.1 на платформе Windows, сделайте следующее:

1. При необходимости выполните обновление до [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell). Если вы используете Windows 10, среда PowerShell 5.1 уже установлена.
2. [Установите платформу .NET Framework версии 4.7.2 или более поздней](/dotnet/framework/install).

При использовании PowerShell Core для Azure PowerShell нет дополнительных требований.

## <a name="install-the-azure-powershell-module"></a>Установка модуля Azure PowerShell

> [!WARNING]
> Для PowerShell 5.1 в Windows __не могут__ одновременно быть установлены модули AzureRM и Az. Если в системе нужно оставить модуль AzureRM, установите модуль Az для PowerShell Core версии 6.x или более поздней. Чтобы сделать это, [установите PowerShell Core версии 6.x или более поздней](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows), а затем следуйте инструкциям в окне терминала PowerShell Core.

Рекомендуемый метод — установка только для активного пользователя:

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

Если вам нужно выполнить установку для всех пользователей в системе, потребуются права администратора. В сеансе PowerShell с повышенными привилегиями выполните запуск от имени администратора или используйте команду `sudo` в macOS либо Linux:

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope AllUsers
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

## <a name="install-offline"></a>Установка в автономном режиме

В некоторых средах невозможно подключиться к коллекции PowerShell. В таких случаях все же можно выполнить установку в автономном режиме, используя один из следующих методов:

* Скачайте модули в другое расположение и используйте его в качестве источника установки в сети. Возможно, этот процесс будет сложным, но так вы сможете поместить в кэш модули PowerShell на отдельном сервере или в общей папке, чтобы развернуть их с помощью PowerShellGet на любой системе без подключения к сети. Сведения о том, как настроить локальный репозиторий и установить его в системах без подключения к сети, см. в статье [Работа с локальными хранилищами PowerShellGet](/powershell/scripting/gallery/how-to/working-with-local-psrepositories).
* [Скачайте MSI для Azure PowerShell](install-az-ps-msi.md) на компьютер, подключенный к сети, а затем скопируйте установщик в системы без доступа к коллекции PowerShell. Помните, что установщик MSI работает только с PowerShell 5.1 в Windows.
* С помощью команды [Save-Module](/powershell/module/PowershellGet/Save-Module) сохраните модуль в общую папку или в другом источнике и вручную скопируйте на другие компьютеры.
  
  ```powershell-interactive
  Save-Module -Name Az -Path '\\someshare\PowerShell\modules' -Force
  ```

## <a name="troubleshooting"></a>Устранение неполадок

Ниже описаны некоторые распространенные проблемы с установкой модуля Azure PowerShell. Если у вас возникла проблема, не описанная здесь, [сообщите о ней на сайте GitHub](https://github.com/azure/azure-powershell/issues).

### <a name="proxy-blocks-connection"></a>Прокси-сервер блокирует подключения

Если командлет `Install-Module` возвращает ошибки о том, что коллекция PowerShell недоступна, возможно, ваша система находится за прокси-сервером. Требования к настройке прокси-сервера на уровне системы в разных операционных системах могут отличаться. Эти требования не рассматриваются здесь. Обратитесь к системному администратору, чтобы узнать о параметрах своего прокси-сервера и о том, как настроить их для своей операционной системы.

Возможно, среду PowerShell нельзя настроить для автоматического использования этого прокси-сервера. В PowerShell версии 5.1 и более поздних настройте использование прокси-сервера для сеанса PowerShell с помощью следующей команды:

```powershell
(New-Object System.Net.WebClient).Proxy.Credentials = `
  [System.Net.CredentialCache]::DefaultNetworkCredentials
```

Если учетные данные операционной системы настроены правильно, в результате выполнения приведенной выше команды запросы PowerShell будут направляться через прокси-сервер.
Чтобы эта настройка сохранялась между сеансами, добавьте команду в [профиль PowerShell](/powershell/module/microsoft.powershell.core/about/about_profiles).

Чтобы установить пакет, ваш прокси-сервер должен разрешать HTTPS-подключения по следующему адресу:

* `https://www.powershellgallery.com`

## <a name="sign-in"></a>Вход

Чтобы начать работу с Azure PowerShell, выполните вход, используя данные своей учетной записи в Azure.

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> Если вы отключили автоматическую загрузку модулей, вручную импортируйте модуль с помощью `Import-Module Az`. Из-за структуры модуля эта операция может занять несколько секунд.

Эти действия нужно повторять для каждого нового сеанса PowerShell. Чтобы узнать, как повторно использовать свои данные для входа в Azure в разных сеансах PowerShell, см. статью [Использование учетных данных пользователя в разных сеансах PowerShell](context-persistence.md).

## <a name="update-the-azure-powershell-module"></a>Обновление модуля Azure PowerShell

Если вы изначально использовали командлет Install-Module, то для получения последней версии следует использовать командлет [Update-Module](/powershell/module/powershellget/update-module). Если вы изначально использовали пакет MSI, необходимо скачать и установить новый MSI для обновления. Если у вас возникли проблемы с обновлением с использованием пакета, полученного с помощью модуля PowerShellGet, необходимо будет выполнить __переустановку__, а не просто __обновление__. Эта процедура ничем не отличается от установки, но может потребоваться добавить аргумент `-Force`:

```powershell
Install-Module -Name Az -AllowClobber -Force
```

Хотя это может перезаписать установленные модули, в системе по-прежнему могут остаться более старые версии.
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

## <a name="next-steps"></a>Next Steps

Дополнительные сведения о модулях Azure PowerShell и их функциях см. в статье [Get Started with Azure PowerShell](get-started-azureps.md) (Начало работы с Azure PowerShell).
Если вы знакомы с Azure PowerShell и вам необходимо мигрировать из AzureRM, см. статью [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md) (Миграция с AzureRM на Az).
