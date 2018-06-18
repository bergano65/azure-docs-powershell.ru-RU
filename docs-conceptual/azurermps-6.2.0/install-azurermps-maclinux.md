---
title: Установка Azure PowerShell в ОС macOS или Linux
description: Инструкции по установке Azure PowerShell в ОС macOS или Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 17912c155255b6fdfd3cfb9242163b67d405dc03
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323175"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a>Установка Azure PowerShell в ОС macOS или Linux

Теперь Azure PowerShell можно запускать на основе PowerShell Core версии 6 на платформах, отличных от Windows. В отличие от стандартной версии Azure PowerShell, созданной на основе .NET Framework для Windows, эта версия создана специально для .NET Core и запустить ее можно на любой платформе, поддерживающей среду выполнения .NET Core.

> [!NOTE]
> Сейчас PowerShell Core версии 6 и Azure PowerShell для .NET Core реализованы в бета-версии.
> Поддержка этих продуктов ограничена. Если у вас возникнут проблемы или вы обнаружите ошибки, сообщите об этом через сайт GitHub.
>
> * [Проблемы, связанные с PowerShell Core версии 6](https://github.com/PowerShell/PowerShell/issues)
> * [Проблемы, связанные с Azure PowerShell](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core-v6"></a>Установка PowerShell Core версии 6

Процедура установки PowerShell Core версии 6 в ОС Linux или macOS зависит от дистрибутива Linux и версии ОС.
Подробные инструкции можно найти в следующих статьях:

- [Установка PowerShell Core в macOS](/powershell/scripting/setup/installing-powershell-core-on-macos)
- [Установка PowerShell Core в Linux](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a>Установка Azure PowerShell для .NET Core

PowerShell Core версии 6 поставляется с установленным модулем PowerShellGet. Это позволяет легко установить любой модуль, опубликованный в коллекции PowerShell. Чтобы установить Azure PowerShell, откройте новый сеанс PowerShell и выполните следующую команду.

```powershell
Install-Module AzureRM.NetCore
```

## <a name="load-the-azurermnetcore-module"></a>Загрузка модуля AzureRM.Netcore

После установки модуля его необходимо загрузить в сеанс PowerShell. Модули можно загрузить с помощью командлета `Import-Module` следующим образом:

```powershell
Import-Module AzureRM.Netcore
Import-Module AzureRM.Profile.Netcore
```

После завершения импорта можно проверить только что установленный модуль, попытавшись войти в Azure с помощью следующей команды.

```powershell
Connect-AzureRmAccount
```

Приведенная выше команда должна предложить перейти по адресу `https://aka.ms/devicelogin` и ввести предоставленный код.

## <a name="available-cmdlets"></a>Доступные командлеты

Модули Azure PowerShell для .NET Standard еще находятся в разработке. Эти модули не обеспечивают полный набор командлетов, которые доступны в версии модулей для Windows. В модулях AzureRM.Netcore реализованы следующие функции.

* Управление учетными записями
  - Вход с помощью учетной записи Майкрософт, рабочей или учебной учетной записи или субъекта-службы с помощью Microsoft Azure Active Directory.
  - Сохранение учетных данных на диск с помощью командлета Save-AzureRmContext и загрузка сохраненных учетных данных с помощью командлета Import-AzureRmContext.
* Среда
  - Получение различных стандартных сред Microsoft Azure.
  - Добавление, настройка и удаление настроенных сред (например, сред Azure Stack или Windows Azure Pack).
* Командлеты плоскости управления для служб Azure, использующих интерфейсы Resource Manager и интерфейсы управления службами.
  - Виртуальная машина
  - Служба приложений (веб-сайты)
  - База данных SQL
  - Служба хранилища
  - Сеть

## <a name="next-steps"></a>Дальнейшие действия

Дополнительные сведения об использовании Azure PowerShell см. в статье [Начало работы с Azure PowerShell](get-started-azureps.md).
