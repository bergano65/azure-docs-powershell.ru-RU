---
title: Другие способы установки Azure PowerShell
description: Сведения о том, как установить Azure PowerShell без PowerShellGet.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.openlocfilehash: f9293d2715b36161c3e6d0d9469b6f18ab35d6c8
ms.sourcegitcommit: 93f93b90ef88c2659be95f3acaba514fe9639169
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2018
ms.locfileid: "52828218"
---
# <a name="install-azure-powershell-on-windows-with-msi-or-web-platform-installer"></a><span data-ttu-id="b026c-103">Установка Azure PowerShell в ОС Windows с помощью пакета MSI или установщика веб-платформы</span><span class="sxs-lookup"><span data-stu-id="b026c-103">Install Azure PowerShell on Windows with MSI or Web Platform Installer</span></span>

<span data-ttu-id="b026c-104">В этой статье описывается, как установить Azure PowerShell в ОС Windows с помощью пакета MSI или установщика веб-платформы.</span><span class="sxs-lookup"><span data-stu-id="b026c-104">This article explains how to install Azure PowerShell on Windows using an MSI or Web Platform Installer (WebPI).</span></span>  
<span data-ttu-id="b026c-105">Используйте эти способы установки только в том случае, если это необходимо для вашей системы.</span><span class="sxs-lookup"><span data-stu-id="b026c-105">Use these installation methods only if they're necessary for your system.</span></span> <span data-ttu-id="b026c-106">Мы рекомендуем устанавливать Azure PowerShell в ОС Windows с помощью PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="b026c-106">The recommended way to install Azure PowerShell on Windows is with PowerShellGet.</span></span> <span data-ttu-id="b026c-107">Инструкции по установке Azure PowerShell с помощью PowerShellGet см. в [этой статье](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="b026c-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-azurerm-ps.md).</span></span>

<span data-ttu-id="b026c-108">Сведения об установке в средах Linux или macOS см. в [этом разделе](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="b026c-108">To install on Linux or macOS environments, see [Install Azure PowerShell on macOS or Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="b026c-109">Установка или обновление в Windows с помощью пакета MSI</span><span class="sxs-lookup"><span data-stu-id="b026c-109">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="b026c-110">Azure PowerShell можно установить с помощью MSI-файла из [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v5.7.0-April2018).</span><span class="sxs-lookup"><span data-stu-id="b026c-110">Azure PowerShell can be installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v5.7.0-April2018).</span></span> <span data-ttu-id="b026c-111">Если вы установили предыдущие версии модулей Azure с помощью пакета MSI, установщик удалит их автоматически.</span><span class="sxs-lookup"><span data-stu-id="b026c-111">If you have installed previous versions of Azure modules as an MSI, the installer automatically removes them.</span></span> <span data-ttu-id="b026c-112">Пакет MSI устанавливает модули в `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="b026c-112">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="b026c-113">Устанавливаются оба модуля: `AzureRM` и `Azure`.</span><span class="sxs-lookup"><span data-stu-id="b026c-113">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="b026c-114">Используйте модуль `Azure`, только если вы работаете с классической моделью развертывания Azure.</span><span class="sxs-lookup"><span data-stu-id="b026c-114">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="b026c-115">Чтобы приступить к работе с Azure PowerShell, вам нужно загрузить `AzureRM` в текущий сеанс PowerShell. Для этого воспользуйтесь командлетом [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), после чего войдите в систему с помощью своих учетных данных Azure.</span><span class="sxs-lookup"><span data-stu-id="b026c-115">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="b026c-116">Эти действия нужно повторять для каждого нового сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b026c-116">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="b026c-117">Чтобы автоматически импортировать модуль `AzureRM`, необходимо настроить профиль PowerShell. Подробнее об этом рассказывается [здесь](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="b026c-117">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="b026c-118">Чтобы узнать, как повторно использовать свои данные для входа в Azure в разных сеансах, см. статью [Использование учетных данных пользователя в разных сеансах PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="b026c-118">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="install-or-update-on-windows-using-the-web-platform-installer"></a><span data-ttu-id="b026c-119">Установка или обновление в Windows с помощью установщика веб-платформы</span><span class="sxs-lookup"><span data-stu-id="b026c-119">Install or update on Windows using the Web Platform Installer</span></span>

<span data-ttu-id="b026c-120">Скачайте [пакет Azure PowerShell WebPI](http://aka.ms/webpi-azps) и запустите установку.</span><span class="sxs-lookup"><span data-stu-id="b026c-120">Download the [Azure PowerShell WebPI package](http://aka.ms/webpi-azps) and start the install.</span></span> <span data-ttu-id="b026c-121">Если вы установили предыдущие версии модулей Azure с помощью пакета MSI или установщика веб-платформы, установщик удалит их автоматически.</span><span class="sxs-lookup"><span data-stu-id="b026c-121">If you have installed previous versions of Azure modules from an MSI or with WebPI, the installer automatically removes them.</span></span> <span data-ttu-id="b026c-122">Модули устанавливаются в `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="b026c-122">Modules are installed into `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="b026c-123">Устанавливаются оба модуля: `AzureRM` и `Azure`.</span><span class="sxs-lookup"><span data-stu-id="b026c-123">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="b026c-124">Используйте модуль `Azure`, только если вы работаете с классической моделью развертывания Azure.</span><span class="sxs-lookup"><span data-stu-id="b026c-124">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="b026c-125">Чтобы приступить к работе с Azure PowerShell, вам нужно загрузить `AzureRM` в текущий сеанс PowerShell. Для этого воспользуйтесь командлетом [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), после чего войдите в систему с помощью своих учетных данных Azure.</span><span class="sxs-lookup"><span data-stu-id="b026c-125">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="b026c-126">Эти действия нужно повторять для каждого нового сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b026c-126">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="b026c-127">Чтобы автоматически импортировать модуль `AzureRM`, необходимо настроить профиль PowerShell. Подробнее об этом рассказывается [здесь](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="b026c-127">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="b026c-128">Чтобы узнать, как повторно использовать свои данные для входа в Azure в разных сеансах, см. статью [Использование учетных данных пользователя в разных сеансах PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="b026c-128">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>
