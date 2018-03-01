---
title: "Установка и настройка Azure PowerShell в macOS и Linux | Документация Майкрософт"
description: "Как установить и настроить Azure PowerShell для первого использования в macOS и Linux."
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/12/2018
ms.openlocfilehash: 64a86dfd4af7f3f0a91501e9a096ff190f7100cb
ms.sourcegitcommit: 5fe9a579d2e0d1cb5a05aadaeba5db784f1b18fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/28/2018
---
# <a name="install-and-configure-azure-powershell-on-macos-and-linux"></a>Установка и настройка Azure PowerShell в macOS и Linux

Теперь можно установить PowerShell Core версии 6 и Azure PowerShell на платформах, отличных от Windows.
Процесс установки Azure PowerShell в macOS и Linux не отличается от процесса установки в Windows, но сначала нужно установить PowerShell Core версии 6.

> [!NOTE]

> Сейчас PowerShell Core версии 6 и Azure PowerShell для .NET Core реализованы в бета-версии.
> Поддержка этих продуктов ограничена. Если у вас возникнут проблемы или вы обнаружите ошибки, отправьте сведения об этих проблемах на сайт GitHub.
>
> * [Проблемы, связанные с PowerShell Core версии 6](https://github.com/PowerShell/PowerShell/issues)
> * [Проблемы, связанные с Azure PowerShell](https://github.com/azure/azure-docs-powershell/issues)

## <a name="step-1-install-powershell-core-v6"></a>Шаг 1. Установка PowerShell Core версии 6

Процесс установки PowerShell Core версии 6 зависит от целевой операционной системы.
PowerShell Core версии 6 можно установить и в Windows, но эта статья посвящена macOS и Linux. Если вы хотите использовать Azure PowerShell в Windows, ознакомьтесь с разделом [Установка](./install-azurerm-ps.md) статьи для Windows.

Установка **PowerShell Core версии 6** в Linux или macOS зависит от дистрибутива Linux и версии ОС.
Подробные инструкции можно найти в следующей статье:

- [Установка PowerShell Core в macOS и Linux](/powershell/scripting/setup/installing-powershell-core-on-macos-and-linux)

## <a name="step-2-install-azure-powershell-for-net-core"></a>Шаг 2. Установка Azure PowerShell для .NET Core

PowerShell Core версии 6 поставляется с установленным модулем PowerShellGet. Это позволяет легко установить любой модуль, опубликованный в коллекции PowerShell. Чтобы установить Azure PowerShell, откройте новый сеанс PowerShell и выполните следующую команду.

```powershell
Install-Module AzureRM.NetCore
```

## <a name="step-3-load-the-azurermnetcore-module"></a>Шаг 3. Загрузка модуля AzureRM.Netcore

После установки модуля его необходимо загрузить в сеанс PowerShell. Модули можно загрузить с помощью командлета `Import-Module` следующим образом:

```powershell
Import-Module AzureRM.Netcore
Import-Module AzureRM.Profile.Netcore
```

После завершения импорта можно проверить только что установленный модуль, попытавшись войти в Azure с помощью следующей команды.

```powershell
Login-AzureRMAccount
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
  - Хранилище
  - Сеть

## <a name="next-steps"></a>Дальнейшие действия

Дополнительные сведения об использовании Azure PowerShell см. в статье [Начало работы с Azure PowerShell](get-started-azureps.md).
