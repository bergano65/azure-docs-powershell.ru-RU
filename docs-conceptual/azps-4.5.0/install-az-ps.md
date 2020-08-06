---
title: Установка Azure PowerShell с помощью PowerShellGet
description: Инструкции по установке Azure PowerShell с помощью PowerShellGet
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/14/2020
ms.openlocfilehash: caa0c2fbba8b8b7e07424481360a60f3da163e66
ms.sourcegitcommit: edfe63c6949cd59127028ac8a13bb4a8827d555c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/04/2020
ms.locfileid: "87566548"
---
# <a name="install-azure-powershell"></a>Установите Azure PowerShell

В этой статье показано, как установить модули Azure PowerShell с помощью [PowerShellGet](/powershell/scripting/gallery/installing-psget). Эти инструкции применимы для платформ Windows, macOS и Linux.

Azure PowerShell также предоставляется в Azure [Cloud Shell](/azure/cloud-shell/overview) и предустанавливается в [образах Docker](azureps-in-docker.md).

## <a name="requirements"></a>Требования

> [!NOTE]
> Для работы в Azure PowerShell на всех платформах мы рекомендуем использовать PowerShell версии 7.x и выше.

Azure PowerShell работает с PowerShell версии 6.2.4 и выше на любой платформе. Кроме того, в Windows также поддерживается использование в PowerShell 5.1. Установите [последнюю версию PowerShell](/powershell/scripting/install/installing-powershell) для своей операционной системы. Дополнительных требований для использования Azure PowerShell в PowerShell версии 6.2.4 и выше нет.

Чтобы узнать вашу версию PowerShell, выполните приведенную ниже команду:

```azurepowershell-interactive
$PSVersionTable.PSVersion
```

Чтобы использовать Azure PowerShell в PowerShell 5.1 в Windows, сделайте следующее:

1. Выполните обновление до [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell).
   Если вы используете Windows 10 версии 1607 и выше, у вас уже есть PowerShell версии 5.1.
2. [Установите платформу .NET Framework версии 4.7.2 или более поздней](/dotnet/framework/install).
3. Убедитесь, что у вас установлена последняя версия PowerShellGet. Выполните `Install-Module -Name PowerShellGet -Force`.

## <a name="install-the-azure-powershell-module"></a>Установка модуля Azure PowerShell

> [!WARNING]
> В Windows нельзя одновременно установить модули AzureRM и Az для PowerShell 5.1 Если в системе нужно оставить модуль AzureRM, установите модуль Az для PowerShell версии 6.2.4 и выше.

Использование командлетов PowerShellGet — предпочтительный метод установки. Установите модуль Az только для текущего пользователя. Это рекомендуемая область установки. Этот метод работает одинаково на платформах Windows, macOS и Linux. Выполните следующую команду из сеанса PowerShell:

```powershell-interactive
if ($PSVersionTable.PSEdition -eq 'Desktop' -and (Get-Module -Name AzureRM -ListAvailable)) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Scope CurrentUser
}
```

По умолчанию коллекция PowerShell не используется как доверенный репозиторий для PowerShellGet. При первом использовании PSGallery отображается следующее сообщение:

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the `Set-PSRepository` cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Ответьте `Yes` или `Yes to All`, чтобы продолжить установку.

Для установки модуля для всех пользователей системы требуются повышенные права. Запустите сеанс PowerShell **от имени администратора** в Windows либо выполните команду `sudo` в macOS или Linux:

```powershell-interactive
if ($PSVersionTable.PSEdition -eq 'Desktop' -and (Get-Module -Name AzureRM -ListAvailable)) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Scope AllUsers
}
```

Модуль Az — это общий модуль для командлетов Azure PowerShell. Во время его установки скачиваются все общедоступные модули Az PowerShell, а после этого становятся доступными все соответствующие командлеты.

## <a name="install-offline"></a>Установка в автономном режиме

В некоторых средах невозможно подключиться к коллекции PowerShell. В таких случаях все же можно выполнить установку в автономном режиме, используя один из следующих методов:

* Скачайте модули в другое сетевое расположение и используйте его в качестве источника установки.
  Так вы сможете кэшировать модули PowerShell на отдельном сервере или в общей папке, чтобы развернуть их с помощью PowerShellGet в любой системе в автономном режиме. Сведения о том, как настроить локальный репозиторий и установить его в системах без подключения к сети, см. в статье [Работа с локальными хранилищами PowerShellGet](/powershell/scripting/gallery/how-to/working-with-local-psrepositories).
* [Скачайте MSI для Azure PowerShell](install-az-ps-msi.md) на компьютер, подключенный к сети, а затем скопируйте установщик в системы без доступа к коллекции PowerShell. Помните, что установщик MSI работает только с PowerShell 5.1 в Windows.
* С помощью команды [Save-Module](/powershell/module/PowershellGet/Save-Module) сохраните модуль в общую папку или в другом источнике и вручную скопируйте на другие компьютеры.

  ```powershell-interactive
  Save-Module -Name Az -Path '\\server\share\PowerShell\modules' -Force
  ```

## <a name="troubleshooting"></a>Устранение неполадок

Ниже описаны некоторые распространенные проблемы с установкой модуля Azure PowerShell. Если у вас возникла проблема, не описанная здесь, [сообщите о ней на сайте GitHub](https://github.com/azure/azure-powershell/issues).

### <a name="proxy-blocks-connection"></a>Прокси-сервер блокирует подключения

Если командлет `Install-Module` возвращает ошибки о том, что коллекция PowerShell недоступна, возможно, ваша система находится за прокси-сервером. Разные операционные системы и сетевые среды имеют разные требования для настройки прокси-сервера на уровне системы. Обратитесь к системному администратору, чтобы узнать о параметрах своего прокси-сервера и о том, как настроить их для своей среды.

Возможно, среду PowerShell нельзя настроить для автоматического использования этого прокси-сервера. В PowerShell 5.1 и более поздних версий настройте сеанс PowerShell для использования прокси-сервера с помощью следующих команд:

```powershell
$webClient = New-Object System.Net.WebClient
$webClient.Proxy.Credentials = [System.Net.CredentialCache]::DefaultNetworkCredentials
```

Если учетные данные операционной системы настроены правильно, конфигурация будет направлять запросы PowerShell через прокси-сервер. Чтобы такое поведение сохранялось между сеансами, добавьте команду в [профиль PowerShell](/powershell/module/microsoft.powershell.core/about/about_profiles).

Для установки пакета ваш прокси-сервер должен разрешать HTTPS-подключения по следующему адресу:

* `https://www.powershellgallery.com`

## <a name="sign-in"></a>Вход

Чтобы начать работу с Azure PowerShell, выполните вход, используя данные своей учетной записи в Azure.

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
> Если вы отключили автоматическую загрузку модулей, вручную импортируйте модуль с помощью `Import-Module -Name Az`.
> Из-за структуры модуля эта операция может занять несколько секунд.

Эти действия нужно повторять для каждого нового сеанса PowerShell. См. сведения в статье [Использование учетных данных пользователя в разных сеансах PowerShell](context-persistence.md).

## <a name="update-the-azure-powershell-module"></a>Обновление модуля Azure PowerShell

Для обновления любого модуля PowerShell следует использовать тот же метод, который использовался для установки модуля. Например, если вы изначально использовали `Install-Module`, для получения последней версии следует использовать командлет [Update-Module](/powershell/module/powershellget/update-module). Если вы изначально использовали пакет MSI, необходимо скачать и установить новый пакет MSI.

Командлеты PowerShellGet не могут обновлять модули, установленные из пакета MSI. Пакеты MSI не обновляют модули, установленные с помощью PowerShellGet. Если у вас возникли проблемы с обновлением с помощью модуля PowerShellGet, необходимо выполнить **повторную установку**, а не просто **обновление**. Повторная установка выполняется так же, как и первоначальная, но необходимо добавить параметр `-Force`:

```powershell
if ($PSVersionTable.PSEdition -eq 'Desktop' -and (Get-Module -Name AzureRM -ListAvailable)) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Force
}
```

В отличие от установки с помощью MSI, при установке или обновлении с помощью PowerShellGet не удаляются более старые версии, которые могут существовать в вашей системе. См. сведения об [удалении из системы предыдущих версий модуля Azure PowerShell](uninstall-az-ps.md). См. сведения об [установке Azure PowerShell с помощью MSI](install-az-ps-msi.md).

## <a name="use-multiple-versions-of-azure-powershell"></a>Использование нескольких версий Azure PowerShell

Вы можете установить несколько версий Azure PowerShell. Чтобы проверить наличие нескольких установленных версий Azure PowerShell, используйте следующую команду:

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | Select-Object -Property Name, Version
```

Сведения о том, как удалить версию Azure PowerShell, см. в статье [Удаление модуля Azure PowerShell](uninstall-az-ps.md).

Если у вас установлено несколько версий модуля, модуль автозагрузки и `Import-Module` загрузит последнюю версию по умолчанию.

Определенную версию модуля `Az` можно установить или загрузить с помощью параметра `-RequiredVersion`.

```powershell-interactive
# Install Az version 3.6.1
Install-Module -Name Az -RequiredVersion 3.6.1
# Load Az version 3.6.1
Import-Module -Name Az -RequiredVersion 3.6.1
```

## <a name="use-multiple-repositories-with-powershellget"></a>Использование нескольких репозиториев с PowerShellGet

Параметр **Repository** является обязательным, если вы добавили дополнительные репозитории в PowerShellGet в системе и модуль Az можно найти более чем в одном из них.

```powershell-interactive
if ($PSVersionTable.PSEdition -eq 'Desktop' -and (Get-Module -Name AzureRM -ListAvailable)) {
    Write-Warning -Message 'Az module not installed. Having both the AzureRM and Az modules installed at the same time is not supported.'
} else {
    Install-Module -Name Az -Repository PSGallery -AllowClobber -Force
}
```

## <a name="provide-feedback"></a>Отзывы

Если вы нашли ошибку при работе с Azure PowerShell, [сообщите о проблеме на GitHub](https://github.com/Azure/azure-powershell/issues). Чтобы отправить отзыв из командной строки, используйте командлет [Send-Feedback](/powershell/module/az.accounts/send-feedback).

## <a name="next-steps"></a>Next Steps

Дополнительные сведения о модулях Azure PowerShell и их функциях см. в статье [Get Started with Azure PowerShell](get-started-azureps.md) (Начало работы с Azure PowerShell). Если вы знакомы с Azure PowerShell и вам необходимо мигрировать из AzureRM, см. статью [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md) (Миграция с AzureRM на Az).
