---
title: "Установка и настройка Azure PowerShell | Документация Майкрософт"
description: "Как установить и настроить Azure PowerShell для первого использования."
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/31/2017
ms.openlocfilehash: 7b7177609ef9104525f173f468d44610b4ad1fe9
ms.sourcegitcommit: db7f0ad39036bf60985ab7bf991b2d41fb34019f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/27/2017
---
# <a name="install-and-configure-azure-powershell"></a>Установка и настройка Azure PowerShell

В этой статье описывается порядок установки модулей Azure PowerShell в среде Windows.
Если вы хотите использовать Azure PowerShell в macOS или Linux, ознакомьтесь со следующей статьей: [Установка и настройка Azure PowerShell в macOS и Linux](install-azurermps-maclinux.md).

Предпочтительный способ установки Azure PowerShell— из коллекции PowerShell.

## <a name="step-1-install-powershellget"></a>Шаг 1. Установка PowerShellGet

Чтобы установить элементы из коллекции PowerShell, требуется модуль PowerShellGet. Убедитесь, что в системе установлена соответствующая версия PowerShellGet и что выполнены другие требования к системе. Выполните следующую команду, чтобы определить наличие PowerShellGet в вашей системе:

```powershell
Get-Module PowerShellGet -list | Select-Object Name,Version,Path
```

Должен отобразиться результат, аналогичный следующему:

```Output
Name          Version Path
----          ------- ----
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

Если у вас не установлен PowerShellGet, перейдите к разделу [Как получить PowerShellGet](#how-to-get-powershellget) этой статьи.

> [!NOTE]
> Чтобы использовать PowerShellGet, необходимо иметь политику выполнения, которая позволяет запускать сценарии. Дополнительные сведения о политике выполнения PowerShell см. в [этой статье](/powershell/module/microsoft.powershell.core/about/about_execution_policies).

## <a name="step-2-install-azure-powershell"></a>Шаг 2. Установка Azure PowerShell

Для установки Azure PowerShell из коллекции PowerShell требуются повышенные привилегии. Выполните следующую команду в сеансе PowerShell с повышенными правами:

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module AzureRM -AllowClobber
```

По умолчанию коллекция PowerShell не настроена как доверенное хранилище для PowerShellGet. При первом использовании PSGallery отображается следующее сообщение:

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): Y
```

Ответьте "Да" или "Да для всех", чтобы продолжить установку.

> [!NOTE]
> Если установленная версия NuGet предшествует версии 2.8.5.201, то вам будет предложено скачать и установить последнюю версию NuGet.

Модуль AzureRM — это модуль свертки для командлетов Azure Resource Manager. При установке модуля AzureRM любой модуль Azure PowerShell, который ранее не был установлен, скачивается из коллекции PowerShell.

Если у вас установлена предыдущая версия Azure PowerShell, то может появляться сообщение об ошибке. Для устранения этой проблемы см. раздел [Обновление Azure PowerShell до новой версии](#update-azps) далее в этой статье.

## <a name="step-3-load-the-azurerm-module"></a>Шаг 3. Загрузка модуля AzureRM
После установки модуля его необходимо загрузить в сеанс PowerShell. Это необходимо сделать в обычном (без повышенных привилегий) сеансе PowerShell. Модули можно загрузить с помощью командлета `Import-Module` следующим образом:

```powershell
Import-Module AzureRM
```

## <a name="next-steps"></a>Дальнейшие действия

Дополнительные сведения об использовании Azure PowerShell см. в следующей статье:

* [Getting started with Azure PowerShell](get-started-azureps.md) (Приступая к работе с Azure PowerShell)

## <a name="reporting-issues-and-feedback"></a>Создание отчетов о проблемах и обратная связь

При появлении ошибок в средстве сообщите о проблеме в разделе [Проблемы](https://github.com/Azure/azure-powershell/issues) репозитория GitHub. Чтобы отправить отзыв из командной строки, используйте командлет `Send-Feedback`.

## <a name="frequently-asked-questions"></a>Часто задаваемые вопросы

### <a name="how-to-get-powershellget"></a>Как получить PowerShellGet

|Версия ОС|Инструкции по установке|
|---|---|
|Используется Windows 10 или Windows Server 2016|Встроены в Windows Management Framework (WMF) 5.0, которая входит в состав ОС|
|Необходимо выполнить обновление до версии PowerShell 5|[Установите последнюю версию WMF](https://www.microsoft.com/en-us/download/details.aspx?id=54616)|
|Используется версия Windows с PowerShell 3 или PowerShell 4|[Скачайте модули PackageManagement](http://go.microsoft.com/fwlink/?LinkID=746217)|

<a id="helpmechoose"></a>
### <a name="checking-the-version-of-azure-powershell"></a>Проверка версии Azure PowerShell

Хотя мы советуем выполнить обновление до последней версии как можно скорее, поддерживается несколько версий Azure PowerShell. Чтобы определить, какая версия Azure PowerShell установлена, выполните в командной строке команду `Get-Module AzureRM`.

```powershell
Get-Module AzureRM -list | Select-Object Name,Version,Path
```

### <a name="support-for-classic-deployment-methods"></a>Поддержка классических методов развертывания

При наличии экземпляров, развернутых с помощью классической модели, вы можете установить Azure PowerShell для управления службами. Дополнительные сведения см. в статье об [установке модуля управления службами Azure PowerShell](/powershell/azure/servicemanagement/install-azure-ps). Модули Azure и AzureRM имеют общие зависимости. При использовании обоих модулей (Azure и AzureRM) необходимо установить одинаковую версию каждого пакета.

<a id="update-azps"></a>
### <a name="updating-to-a-new-version-of-azure-powershell"></a>Обновление Azure PowerShell до новой версии

Если у вас установлена предыдущая версия Azure PowerShell, включающая модуль управления службами, то может появляться следующее сообщение об ошибке:

```Output
PackageManagement\Install-Package : A command with name 'Get-AzureStorageContainerAcl' is already
available on this system. This module 'Azure.Storage' may override the existing commands. If you
still want to install this module 'Azure.Storage', use -AllowClobber parameter.

At C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PSModule.psm1:1772 char:21
+ ...          $null = PackageManagement\Install-Package @PSBoundParameters
+                      ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : InvalidOperation: (Microsoft.Power....InstallPackage:InstallPackage) [Install-Package], Exception
    + FullyQualifiedErrorId : CommandAlreadyAvailable,Validate-ModuleCommandAlreadyAvailable,Microsoft.PowerShell.PackageManagement.Cmdlets.InstallPackage
```

Как указано в сообщении об ошибке, для установки модуля необходимо использовать параметр -AllowClobber. Используйте следующую команду:

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module AzureRM -AllowClobber
```

Дополнительные сведения см. в статье, посвященной командлету [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).

### <a name="installing-module-versions-side-by-side"></a>Установка версий модуля без замены

Метод установки PowerShellGet — это единственный метод, поддерживающий установку нескольких версий. Например, вы можете использовать скрипты, написанные с помощью предыдущих версий Azure PowerShell, которые вы не можете обновить из-за отсутствия времени или ресурсов. Чтобы установить несколько версий Azure PowerShell, выполните следующие команды:

```powershell
Install-Module -Name AzureRM -RequiredVersion 3.7.0
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

В сеанс PowerShell можно загрузить только одну версию модуля. Необходимо открыть новое окно PowerShell и с помощью команды `Import-Module` импортировать определенную версию командлетов AzureRM:

```powershell
Import-Module AzureRM -RequiredVersion 1.2.9
```

> [!NOTE]
> Версии 2.1.0 и 1.2.6 — это первые версии модуля, предназначенные для установки и использования без удаления предыдущей версии. Если загрузить более раннюю версию модуля Azure PowerShell, то загрузится несовместимая версия модуля **AzureRM.Profile**. Это приведет к тому, что командлеты будут запрашивать выполнить вход при каждом выполнении командлета.

### <a name="other-installation-methods"></a>Другие методы установки

Сведения об установке с помощью установщика веб-платформы или пакета MSI см. статье [Other installation methods](other-install.md) (Другие методы установки).