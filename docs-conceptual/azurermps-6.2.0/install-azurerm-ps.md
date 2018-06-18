---
title: Установка Azure PowerShell с помощью PowerShellGet
description: Инструкции по установке Azure PowerShell с помощью PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/31/2018
ms.openlocfilehash: 9b7046157e32a5c8473210e9840f9ae1b2f45902
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323107"
---
# <a name="install-azure-powershell-with-powershellget"></a>Установка Azure PowerShell с помощью PowerShellGet

В этой статье содержатся инструкции по установке модулей Azure PowerShell в среде Windows с помощью PowerShellGet.  Это предпочтительный способ установки Azure PowerShell, но если вы хотите использовать для установки пакет MSI или установщик веб-платформы, см. раздел [Другие способы установки](other-install.md).

Если вы хотите использовать Azure PowerShell в macOS или Linux, ознакомьтесь со следующей статьей: [Установка и настройка Azure PowerShell в macOS и Linux](install-azurermps-maclinux.md).

## <a name="system-requirements"></a>Требования к системе

Для работы с Azure PowerShell версии 6.1.0 требуется PowerShell версии 5.0 (или выше). Сведения об обновлении до версии PowerShell 5.0 см. в разделе [Обновление существующей версии Windows PowerShell](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).

PowerShellGet автоматически входит в состав PowerShell 5.0.

## <a name="install-or-update-the-azure-powershell-module"></a>Установка или обновление модуля Azure PowerShell

Для установки Azure PowerShell из коллекции PowerShell требуются повышенные права. Выполните следующую команду PowerShell с повышенными правами:

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

> [!IMPORTANT]
> В результате использования этой команды любая существующая в вашей системе версия модуля Azure PowerShell будет обновлена. Если необходимо установить несколько версий, перейдите в раздел часто задаваемых вопросов и найдите ответ на вопрос [Можно ли установить несколько версий Azure PowerShell?](#multiple-versions).

По умолчанию коллекция PowerShell не настроена как доверенный репозиторий для PowerShellGet. При первом использовании PSGallery отображается следующее сообщение:

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Ответьте "Да" или "Да для всех", чтобы продолжить установку.

> [!NOTE]
> Если установленная версия NuGet предшествует версии 2.8.5.201, вам будет предложено скачать и установить последнюю версию NuGet.

Модуль AzureRM — это набор командлетов для работы с Azure Resource Manager.  При установке модуля AzureRM любой модуль Azure PowerShell, который ранее не был установлен, скачивается из коллекции PowerShell.

## <a name="load-the-azure-powershell-module"></a>Загрузка модуля Azure PowerShell

После установки модуля его необходимо загрузить в сеанс PowerShell. Это необходимо сделать в обычном (без повышенных привилегий) сеансе PowerShell. Модули можно загрузить с помощью командлета `Import-Module` следующим образом:

```powershell
Import-Module -Name AzureRM
```

## <a name="reporting-issues-and-feedback"></a>Создание отчетов о проблемах и обратная связь

При возникновении каких-либо ошибок в работе средства [сообщите о проблеме на сайте GitHub](https://github.com/Azure/azure-powershell/issues). Чтобы отправить отзыв из командной строки, используйте командлет `Send-Feedback`.

## <a name="next-steps"></a>Дальнейшие действия

Дополнительные сведения об использовании Azure PowerShell см. в следующей статье:

* [Getting started with Azure PowerShell](get-started-azureps.md) (Приступая к работе с Azure PowerShell)

## <a name="frequently-asked-questions"></a>Часто задаваемые вопросы

### <a id="helpmechoose"></a>Как проверить версию Azure PowerShell?

Хотя мы советуем выполнить обновление до последней версии как можно скорее, поддерживается несколько версий Azure PowerShell. Чтобы определить, какая версия Azure PowerShell установлена, выполните в командной строке команду `Get-Module AzureRM`.

```powershell
Get-Module AzureRM -ListAvailable | Select-Object -Property Name,Version,Path
```

### <a name="can-i-use-azure-powershell-for-azure-classic-deployments"></a>Можно ли использовать Azure PowerShell для классических развертываний Azure?

При наличии экземпляров, развернутых с помощью классической модели, вы можете установить Azure PowerShell для управления службами. Дополнительные сведения см. в статье об [установке модуля управления службами Azure PowerShell](/powershell/azure/servicemanagement/install-azure-ps). Модули Azure и AzureRM имеют общие зависимости. При использовании обоих модулей (Azure и AzureRM) необходимо установить одинаковую версию каждого пакета.

### <a name="a-namemultiple-versionscan-i-install-multiple-versions-of-azure-powershell"></a><a name="multiple-versions"/>Можно ли установить несколько версий Azure PowerShell?

Установка с помощью PowerShellGet — единственный способ, поддерживающий установку нескольких версий. Для установки нескольких версий необходимо добавить параметр `-RequiredVersion` в командлет `Install-Module`. Ниже показан пример для установки версий 6.1.0 и 1.2.9:

```powershell
Install-Module -Name AzureRM -RequiredVersion 6.1.0
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

В сеанс PowerShell можно загрузить только одну версию модуля. Необходимо открыть новое окно PowerShell и с помощью команды `Import-Module` импортировать определенную версию модуля Azure PowerShell.

```powershell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

> [!NOTE]
> Версии 2.1.0 и 1.2.6 — это первые версии модуля, предназначенные для установки и использования без удаления предыдущей версии. Если загрузить более раннюю версию модуля Azure PowerShell, то загрузится несовместимая версия модуля **AzureRM.Profile**. Это приведет к тому, что командлеты будут запрашивать выполнить вход при каждом выполнении командлета.
