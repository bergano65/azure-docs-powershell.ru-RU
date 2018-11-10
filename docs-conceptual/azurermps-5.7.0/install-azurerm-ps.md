---
title: Установка Azure PowerShell в ОС Windows с помощью PowerShellGet
description: Инструкции по установке Azure PowerShell с помощью PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/15/2018
ms.openlocfilehash: a868a62bd7bb2f39775a3b7878e2c8484c50438d
ms.sourcegitcommit: 06f9206e025afa7207d4657c8f57c94ddb74817a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2018
ms.locfileid: "51211100"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a>Установка Azure PowerShell в ОС Windows с помощью PowerShellGet

В этой статье содержатся инструкции по установке модулей Azure PowerShell в среде Windows с помощью PowerShellGet. PowerShellGet и управление модулями — это предпочтительный способ установки Azure PowerShell, но если вы хотите использовать для установки пакет MSI или установщик веб-платформы, см. статью о [других способах установки](other-install.md).

Инструкции по установке Azure PowerShell на других платформах см. в статье [Установка Azure PowerShell в macOS или Linux](install-azurermps-maclinux.md).

Эта версия Azure PowerShell не поддерживает классическую модель развертывания Azure. Если вам нужна поддержка классического развертывания, см. статью [Установка модуля управления службами Azure PowerShell](/powershell/azure/servicemanagement/install-azure-ps).

## <a name="requirements"></a>Требования

Чтобы установить Azure PowerShell, требуется PowerShellGet начиная с версии 1.1.2.0. Чтобы проверить свою систему на наличие этого компонента, выполните следующую команду:

```powershell-interactive
Get-Module -Name PowerShellGet -ListAvailable | Select-Object -Property Name,Version,Path
```

Должен отобразиться результат, аналогичный следующему:

```output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

Чтобы обновить свою версию PowerShellGet, выполните следующую команду:

```powershell-interactive
Install-Module PowerShellGet -Force
```

Если компонент PowerShellGet не установлен, следуйте инструкциям для своей системы из таблицы ниже.

|Сценарий|Инструкции по установке|
|---|---|
|Windows 10<br/>Windows Server 2016|Встроен в пакет Windows Management Framework (WMF) 5.0, который входит в состав ОС|
|Обновление до PowerShell 5| <ol><li>[Установите последнюю версию WMF](https://www.microsoft.com/en-us/download/details.aspx?id=54616)</li><li>Выполните следующую команду:<br/>```Install-Module PowerShellGet -Force```</li></ol>|
|Windows с PowerShell 3 или PowerShell 4|<ol><il>[Получите модули PackageManagement:](http://go.microsoft.com/fwlink/?LinkID=746217)</il><li>Выполните следующую команду:<br/>```Install-Module PowerShellGet -Force```</li></ol>|

> [!NOTE]
> Чтобы использовать PowerShellGet, необходимо иметь политику выполнения, которая позволяет запускать сценарии. Дополнительные сведения о политике выполнения PowerShell см. в [этой статье](/powershell/module/microsoft.powershell.core/about/about_execution_policies).
>
> [!IMPORTANT]
> Для модуля AzureRM, описанном в этом документе, используется .NET Framework. Из-за этого модуль несовместимым с PowerShell версии 6.0, для которой используется .NET Core. Если вы используете PowerShell 6.0, изучите [инструкции по установке для macOS и Linux](install-azurermps-maclinux.md).

## <a name="install-the-azure-powershell-module"></a>Установка модуля Azure PowerShell

Для установки модулей из коллекции PowerShell требуется более высокий уровень привилегий. Чтобы установить Azure PowerShell, в сеансе с более высоким уровнем привилегий выполните следующую команду:

```powershell-interactive
Install-Module -Name AzureRM
```

> [!NOTE]
> Если установленная версия NuGet предшествует версии 2.8.5.201, вам будет предложено скачать и установить последнюю версию NuGet.

По умолчанию коллекция PowerShell не используется как доверенный репозиторий для PowerShellGet. При первом использовании PSGallery отображается следующее сообщение:

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Ответьте `Yes` или `Yes to All`, чтобы продолжить установку.

Модуль `AzureRM` — это общий модуль для командлетов Azure PowerShell. Во время его установки скачиваются все доступные модули Azure Resource Manager и устанавливаются все соответствующие командлеты.

## <a name="sign-in"></a>Вход

Чтобы приступить к работе с Azure PowerShell, вам нужно загрузить `AzureRM` в текущий сеанс PowerShell. Для этого воспользуйтесь командлетом [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), после чего войдите в систему с помощью своих учетных данных Azure.

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

Эти действия нужно повторять для каждого нового сеанса PowerShell. Чтобы автоматически импортировать модуль `AzureRM`, необходимо настроить профиль PowerShell. Подробнее об этом рассказывается [здесь](/powershell/module/microsoft.powershell.core/about/about_profiles).
Чтобы узнать, как повторно использовать свои данные для входа в Azure в разных сеансах, см. статью [Использование учетных данных пользователя в разных сеансах PowerShell](context-persistence.md).

## <a name="update-the-azure-powershell-module"></a>Обновление модуля Azure PowerShell

Чтобы обновить версию Azure PowerShell, выполните команду [Update-Module](/powershell/module/powershellget/update-module). Эта команда __не__ удаляет предыдущие версии.

```powershell-interactive
Update-Module -Name AzureRM
```

Сведения о том, как удалить из системы предыдущие версии Azure PowerShell, см. в статье [Удаление модуля Azure PowerShell](uninstall-azurerm-ps.md).

## <a name="use-multiple-versions-of-azure-powershell"></a>Использование нескольких версий Azure PowerShell

Вы можете установить несколько версий Azure PowerShell. Несколько версий могут понадобиться, если вы работаете с локальными ресурсами Azure Stack, пользуетесь версиями Windows, в которых невозможно обновить PowerShell до версии 5.0, или используете классическую модель развертывания Azure. Чтобы установить более раннюю версию, при установке укажите аргумент `-RequiredVersion`.

```powershell-interactive
# Install version 1.2.9 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

По умолчанию всегда загружается модуль Azure PowerShell последней версии. Чтобы загрузить другую версию, укажите аргумент `-RequiredVersion`.

```powershell-interactive
# Load version 1.2.9 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

## <a name="provide-feedback"></a>Отзывы

Если вы нашли ошибку при работе с Azure Powershell, [сообщите о ней на сайте GitHub](https://github.com/Azure/azure-powershell/issues).
Чтобы отправить отзыв из командной строки, используйте командлет [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).

## <a name="next-steps"></a>Дальнейшие действия

Сведения о начале работы с Azure PowerShell см. в [этой статье](get-started-azureps.md). Она содержит более подробную информацию о модуле и его компонентах.