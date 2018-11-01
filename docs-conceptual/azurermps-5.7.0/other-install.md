---
title: Другие способы установки Azure PowerShell
description: Сведения о том, как установить Azure PowerShell без PowerShellGet.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.openlocfilehash: 2fcd2307667d1f810fbcb3fe4d14e3b0def537ed
ms.sourcegitcommit: ff44dec6418a449757bded3c6ebe0a7d4c05ee6e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/01/2018
ms.locfileid: "50737498"
---
# <a name="install-azure-powershell-on-windows-with-msi-or-web-platform-installer"></a>Установка Azure PowerShell в ОС Windows с помощью пакета MSI или установщика веб-платформы

В этой статье описывается, как установить Azure PowerShell в ОС Windows с помощью пакета MSI или установщика веб-платформы.  
Используйте эти способы установки только в том случае, если это необходимо для вашей системы. Мы рекомендуем устанавливать Azure PowerShell в ОС Windows с помощью PowerShellGet. Инструкции по установке Azure PowerShell с помощью PowerShellGet см. в [этой статье](install-azurerm-ps.md).

Сведения об установке в средах Linux или macOS см. в [этом разделе](install-azurermps-maclinux.md).

## <a name="install-or-update-on-windows-using-the-msi-package"></a>Установка или обновление в Windows с помощью пакета MSI

Azure PowerShell можно установить с помощью MSI-файла из [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v5.7.0-April2018). Если вы установили предыдущие версии модулей Azure с помощью пакета MSI, установщик удалит их автоматически. Пакет MSI устанавливает модули в `${env:ProgramFiles}\WindowsPowerShell\Modules`. Устанавливаются оба модуля: `AzureRM` и `Azure`.

> [!NOTE]
> Используйте модуль `Azure`, только если вы работаете с классической моделью развертывания Azure.

Чтобы приступить к работе с Azure PowerShell, вам нужно загрузить `AzureRM` в текущий сеанс PowerShell. Для этого воспользуйтесь командлетом [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), после чего войдите в систему с помощью своих учетных данных Azure.

```powershell
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

Эти действия нужно повторять для каждого нового сеанса PowerShell. Чтобы автоматически импортировать модуль `AzureRM`, необходимо настроить профиль PowerShell. Подробнее об этом рассказывается [здесь](/powershell/module/microsoft.powershell.core/about/about_profiles).
Чтобы узнать, как повторно использовать свои данные для входа в Azure в разных сеансах, см. статью [Использование учетных данных пользователя в разных сеансах PowerShell](context-persistence.md).

## <a name="install-or-update-on-windows-using-the-web-platform-installer"></a>Установка или обновление в Windows с помощью установщика веб-платформы

Скачайте [пакет Azure PowerShell WebPI](http://aka.ms/webpi-azps) и запустите установку. Если вы установили предыдущие версии модулей Azure с помощью пакета MSI или установщика веб-платформы, установщик удалит их автоматически. Модули устанавливаются в `${env:ProgramFiles}\WindowsPowerShell\Modules`. Устанавливаются оба модуля: `AzureRM` и `Azure`.

> [!NOTE]
> Используйте модуль `Azure`, только если вы работаете с классической моделью развертывания Azure.

Чтобы приступить к работе с Azure PowerShell, вам нужно загрузить `AzureRM` в текущий сеанс PowerShell. Для этого воспользуйтесь командлетом [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), после чего войдите в систему с помощью своих учетных данных Azure.

```powershell
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

Эти действия нужно повторять для каждого нового сеанса PowerShell. Чтобы автоматически импортировать модуль `AzureRM`, необходимо настроить профиль PowerShell. Подробнее об этом рассказывается [здесь](/powershell/module/microsoft.powershell.core/about/about_profiles).
Чтобы узнать, как повторно использовать свои данные для входа в Azure в разных сеансах, см. статью [Использование учетных данных пользователя в разных сеансах PowerShell](context-persistence.md).
