---
title: Установка Azure PowerShell с помощью MSI
description: Сведения о том, как установить Azure PowerShell без PowerShellGet с помощью пакета MSI.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/22/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 88419c14755ff4dbcf5f8527282d9698b1259799
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2020
ms.locfileid: "93409641"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a>Установка Azure PowerShell в ОС Windows с помощью пакета MSI

В этой статье объясняется, как установить Azure PowerShell в ОС Windows с помощью установщика MSI. Установщик MSI предоставляется для сред, в которых коллекция PowerShell может блокироваться брандмауэром или требуется автономный установщик. Мы рекомендуем устанавливать Azure PowerShell с помощью PowerShellGet. Инструкции по установке Azure PowerShell с помощью PowerShellGet см. в [этой статье](install-az-ps.md).

## <a name="requirements"></a>Требования

Установщик MSI в Windows предназначен для только установки Azure PowerShell 5.1. Для установки на платформах, отличающихся от Windows, или более поздних версий PowerShell [выполните установку PowerShellGet](install-az-ps.md). Чтобы узнать вашу версию PowerShell, выполните приведенную ниже команду:

```powershell-interactive
$PSVersionTable.PSVersion
```

Чтобы использовать Azure PowerShell в PowerShell 5.1, сделайте следующее:

1. При необходимости выполните обновление до [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell). Если вы используете Windows 10, среда PowerShell 5.1 уже установлена.
2. [Установите платформу .NET Framework версии 4.7.2 или более поздней](/dotnet/framework/install).

## <a name="install-or-update-on-windows-using-the-msi-package"></a>Установка или обновление в Windows с помощью пакета MSI

Пакет MSI для Azure PowerShell доступен на [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v2.8.0-October2019). Если вы установили более ранние версии модулей Azure PowerShell с помощью пакета MSI, установщик удалит их автоматически. Пакет MSI устанавливает модули в `${env:ProgramFiles}\WindowsPowerShell\Modules`.

Чтобы начать работу с Azure PowerShell, выполните вход, используя данные своей учетной записи в Azure.

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzAccount
```

> [!NOTE]
> Если вы отключили автоматическую загрузку модулей, вам нужно вручную импортировать модуль с помощью `Import-Module Az`. Из-за структуры модуля эта операция может занять около минуты.

Это действие нужно будет повторить для каждого нового сеанса PowerShell. Чтобы узнать, как повторно использовать свои данные для входа в Azure в разных сеансах PowerShell, см. статью [Использование учетных данных пользователя в разных сеансах PowerShell](context-persistence.md).

## <a name="provide-feedback"></a>Отзывы

Если вы нашли ошибку при работе с Azure PowerShell, [сообщите о проблеме на GitHub](https://github.com/Azure/azure-powershell/issues). Чтобы отправить отзыв из командной строки, используйте командлет [Send-Feedback](/powershell/module/az.accounts/send-feedback).

## <a name="next-steps"></a>Next Steps

Дополнительные сведения о модулях Azure PowerShell и их функциях см. в статье [Get Started with Azure PowerShell](get-started-azureps.md) (Начало работы с Azure PowerShell). Если вы знакомы с Azure PowerShell и вам необходимо мигрировать из AzureRM, см. статью [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md) (Миграция с AzureRM на Az).
