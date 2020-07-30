---
title: Установка и настройка Azure PowerShell | Документация Майкрософт
description: Как установить и настроить Azure PowerShell для первого использования.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/27/2018
ms.openlocfilehash: 653284edc093943972516dfd4253af6297754a6a
ms.sourcegitcommit: c19bf5a96a82a56e2b1fa9ab5e106690f850cedf
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/27/2020
ms.locfileid: "87177515"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a>Установка Azure PowerShell в ОС Windows с помощью PowerShellGet

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

В этой статье содержатся инструкции по установке модулей Azure PowerShell для PowerShell 5.x для Windows с помощью PowerShellGet. PowerShellGet и управление модулями — это предпочтительный способ установки Azure PowerShell, но если вы хотите использовать для установки пакет MSI или установщик веб-платформы, см. статью о [других способах установки](other-install.md).

Эта версия Azure PowerShell не поддерживает классическую модель развертывания Azure. Если вам нужна поддержка классического развертывания, см. статью [Установка модуля управления службами Azure PowerShell](/powershell/azure/servicemanagement/install-azure-ps).

> [!IMPORTANT]
> Модуль AzureRM не поддерживается в macOS и Linux. Чтобы использовать командлеты Azure PowerShell на этих платформах, [установите модуль Az](/powershell/azure/install-az-ps).

## <a name="step-1-install-powershellget"></a>Шаг 1. Установка PowerShellGet

Чтобы установить элементы из коллекции PowerShell, требуется модуль PowerShellGet. Убедитесь, что в системе установлена необходимая версия PowerShellGet и что выполнены другие требования к системе. Выполните следующую команду, чтобы определить наличие PowerShellGet в вашей системе:


```powershell-interactive
Get-InstalledModule -Name PowerShellGet -ListAvailable | Select-Object -Property Name,Version,Path
```

Должен отобразиться результат, аналогичный следующему:

```Output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

Необходимо установить версию PowerShellGet 1.1.2.0 или более позднюю. Для обновления PowerShellGet используйте следующую команду:

```powershell-interactive
Install-Module PowerShellGet -Force
```

Если у вас не установлен PowerShellGet, перейдите к разделу [Как установить PowerShellGet](#how-to-get-powershellget) этой статьи.

> [!NOTE]
> Чтобы использовать PowerShellGet, необходимо иметь политику выполнения, которая позволяет запускать сценарии. Дополнительные сведения о политике выполнения PowerShell см. в [этой статье](/powershell/module/microsoft.powershell.core/about/about_execution_policies).
>
> [!IMPORTANT]
> Для модуля AzureRM, описанном в этом документе, используется .NET Framework. Из-за этого модуль несовместимым с PowerShell версии 6.0, для которой используется .NET Core. Если вы используете PowerShell 6.0, изучите [инструкции по установке для macOS и Linux](/powershell/azure/install-az-ps).

## <a name="step-2-install-azure-powershell"></a>Шаг 2. Установите Azure PowerShell

Для установки Azure PowerShell из коллекции PowerShell требуются повышенные права. Выполните следующую команду PowerShell с повышенными правами:

```powershell-interactive
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

По умолчанию коллекция PowerShell не настроена как доверенное хранилище для PowerShellGet. При первом использовании PSGallery отображается следующее сообщение:

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): Y
```

Ответьте Yes (Да) или Yes to All (Да для всех), чтобы продолжить установку.

> [!NOTE]
> Если установленная версия NuGet предшествует версии 2.8.5.201, вам будет предложено скачать и установить последнюю версию NuGet.

Модуль AzureRM — это набор командлетов для работы с Azure Resource Manager. При установке модуля AzureRM любой модуль Azure PowerShell, который ранее не был установлен, скачивается из коллекции PowerShell.

Если у вас установлена предыдущая версия Azure PowerShell, то может появиться сообщение об ошибке. Для устранения этой проблемы см. раздел [Обновление Azure PowerShell до новой версии](#update-azps) далее в этой статье.

## <a name="step-3-load-the-azurerm-module"></a>Шаг 3. Загрузка модуля AzureRM

После установки модуля его необходимо загрузить в сеанс PowerShell. Это необходимо сделать в обычном (без повышенных привилегий) сеансе PowerShell. Модули можно загрузить с помощью командлета `Import-Module` следующим образом:

```powershell-interactive
Import-Module -Name AzureRM
```

## <a name="next-steps"></a>Next Steps

Дополнительные сведения об использовании Azure PowerShell см. в следующей статье:

* [Getting started with Azure PowerShell](get-started-azureps.md) (Приступая к работе с Azure PowerShell)

## <a name="reporting-issues-and-feedback"></a>Создание отчетов о проблемах и обратная связь

При появлении ошибок в средстве сообщите о проблеме в разделе [Проблемы](https://github.com/Azure/azure-powershell/issues) репозитория GitHub. Чтобы отправить отзыв из командной строки, используйте командлет `Send-Feedback`.

## <a name="frequently-asked-questions"></a>Часто задаваемые вопросы

### <a name="how-to-get-powershellget"></a>Как установить PowerShellGet

|Сценарий|Инструкции по установке|
|---|---|
|Используется Windows 10 или Windows Server 2016|Встроен в пакет Windows Management Framework (WMF) 5.0, который входит в состав ОС|
|Обновление до PowerShell 5.0|[Установите последнюю версию WMF](https://www.microsoft.com/download/details.aspx?id=54616)|
|Используется версия Windows с PowerShell 3 или PowerShell 4|[Скачайте модули PackageManagement](https://go.microsoft.com/fwlink/?LinkID=746217)|

### <a name="div-idhelpmechoosechecking-the-version-of-azure-powershell"></a><div id="helpmechoose"/>Проверка версии Azure PowerShell

Хотя мы советуем выполнить обновление до последней версии как можно скорее, поддерживается несколько версий Azure PowerShell. Чтобы определить, какая версия Azure PowerShell установлена, выполните в командной строке команду `Get-InstalledModule AzureRM`.

```powershell-interactive
Get-InstalledModule AzureRM -AllVersions | Select-Object -Property Name,Version,Path
```

### <a name="support-for-classic-deployment-methods"></a>Поддержка классических методов развертывания

При наличии экземпляров, развернутых с помощью классической модели, вы можете установить Azure PowerShell для управления службами. Дополнительные сведения см. в статье об [установке модуля управления службами Azure PowerShell](/powershell/azure/servicemanagement/install-azure-ps). Модули Azure и AzureRM имеют общие зависимости. При использовании обоих модулей (Azure и AzureRM) необходимо установить одинаковую версию каждого пакета.

### <a name="div-idupdate-azpsupdating-to-a-new-version-of-azure-powershell"></a><div id="update-azps"/>Обновление Azure PowerShell до новой версии

Если у вас установлена предыдущая версия Azure PowerShell, включающая модуль управления службами, то может появиться следующее сообщение об ошибке:

```Output
PackageManagement\Install-Package : A command with name 'Get-AzureStorageContainerAcl' is already
available on this system. This module 'Azure.Storage' may override the existing commands. If you
still want to install this module 'Azure.Storage', use -AllowClobber parameter.

At C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PSModule.psm1:1772 char:21
+ ...          $null = PackageManagement\Install-Package @PSBoundParameters
+                      ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : InvalidOperation: (Microsoft.Power....InstallPackage:InstallPackage) [Install-Package], Exception
    + FullyQualifiedErrorId : CommandAlreadyAvailable,Validate-ModuleCommandAlreadyAvailable,Microsoft.PowerShell.PackageManagement.Cmdlets.InstallPackage
```

Как указано в сообщении об ошибке, для установки модуля предлагается использовать параметр -AllowClobber Используйте следующую команду:

```powershell-interactive
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

Дополнительные сведения см. в статье, посвященной командлету [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).

### <a name="installing-module-versions-side-by-side"></a>Установка версий модуля без замены

Метод установки PowerShellGet — это единственный метод, поддерживающий установку нескольких версий. Например, вы можете использовать скрипты, написанные с помощью предыдущих версий Azure PowerShell, которые вы не можете обновить из-за отсутствия времени или ресурсов. Чтобы установить несколько версий Azure PowerShell, выполните следующие команды:

```powershell-interactive
Install-Module -Name AzureRM -RequiredVersion 3.7.0
Install-Module -Name AzureRM -RequiredVersion 2.3.0
```

В сеанс PowerShell можно загрузить только одну версию модуля. Необходимо открыть новое окно PowerShell и с помощью команды `Import-Module` импортировать определенную версию командлетов AzureRM:

```powershell-interactive
Import-Module -Name AzureRM -RequiredVersion 2.3.0
```

> [!NOTE]
> Версии 2.1.0 и 1.2.6 — это первые версии модуля, предназначенные для установки и использования без удаления предыдущей версии. Если загрузить более раннюю версию модуля Azure PowerShell, то загрузится несовместимая версия модуля **AzureRM.Profile**. Это приведет к тому, что при каждом выполнении командлета будет отображаться запрос на вход.

### <a name="other-installation-methods"></a>Другие методы установки

Сведения об установке с помощью установщика веб-платформы или пакета MSI см. статье [Other installation methods](other-install.md) (Другие методы установки).
