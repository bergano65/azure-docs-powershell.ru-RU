---
title: Другие способы установки Azure PowerShell
description: Сведения о том, как установить Azure PowerShell без PowerShellGet с помощью пакета MSI.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/16/2018
ms.openlocfilehash: 82375cc4267f468f562d138c4cdec6131e34ae32
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/05/2020
ms.locfileid: "65534515"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a>Установка Azure PowerShell в ОС Windows с помощью пакета MSI

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

В этой статье объясняется, как установить Azure PowerShell в ОС Windows с помощью установщика MSI.  
Используйте эти способы установки только в том случае, если это необходимо для вашей системы. Мы рекомендуем устанавливать Azure PowerShell в ОС Windows с помощью PowerShellGet. Инструкции по установке Azure PowerShell с помощью PowerShellGet см. в [этой статье](install-azurerm-ps.md).

> [!NOTE]
> Для Azure PowerShell 6.x и более новых версий установка с помощью установщика веб-платформы больше не доступна. Если вам нужно использовать установщик веб-платформы, попробуйте вместо него использовать пакет MSI или установите более раннюю версию Azure PowerShell.

## <a name="install-or-update-on-windows-using-the-msi-package"></a>Установка или обновление в Windows с помощью пакета MSI

Azure PowerShell для Windows PowerShell 5.x можно установить с помощью MSI-файла из [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018). Если вы установили предыдущие версии модулей Azure с помощью пакета MSI, установщик удалит их автоматически. Пакет MSI устанавливает модули в `${env:ProgramFiles}\WindowsPowerShell\Modules`. Устанавливаются оба модуля: `AzureRM` и `Azure`.

> [!NOTE]
> Используйте модуль `Azure`, только если вы работаете с классической моделью развертывания Azure.

Чтобы начать работу с Azure PowerShell, выполните вход, используя данные своей учетной записи в Azure.

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

> [!NOTE]
>
> Если вы отключили автоматическую загрузку модулей, вам нужно вручную импортировать модуль с помощью `Import-Module AzureRM`. Из-за структуры модуля эта операция может занять несколько секунд.

Это действие нужно будет повторить для каждого нового сеанса PowerShell. Чтобы узнать, как повторно использовать свои данные для входа в Azure в разных сеансах PowerShell, см. статью [Использование учетных данных пользователя в разных сеансах PowerShell](context-persistence.md).
