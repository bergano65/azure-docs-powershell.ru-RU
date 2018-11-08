---
title: Другие способы установки Azure PowerShell
description: Сведения о том, как установить Azure PowerShell без PowerShellGet с помощью пакета MSI.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: 9fa5790e0a2aca4f933b40256634f772c258b189
ms.sourcegitcommit: 06f9206e025afa7207d4657c8f57c94ddb74817a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2018
ms.locfileid: "51213097"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a><span data-ttu-id="20127-103">Установка Azure PowerShell в ОС Windows с помощью пакета MSI</span><span class="sxs-lookup"><span data-stu-id="20127-103">Install Azure PowerShell on Windows with MSI</span></span>

<span data-ttu-id="20127-104">В этой статье объясняется, как установить Azure PowerShell в ОС Windows с помощью установщика MSI.</span><span class="sxs-lookup"><span data-stu-id="20127-104">This article explains how to install Azure PowerShell on Windows using an MSI installer.</span></span>  
<span data-ttu-id="20127-105">Используйте эти способы установки только в том случае, если это необходимо для вашей системы.</span><span class="sxs-lookup"><span data-stu-id="20127-105">Use these installation methods only if they're necessary for your system.</span></span> <span data-ttu-id="20127-106">Мы рекомендуем устанавливать Azure PowerShell в ОС Windows с помощью PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="20127-106">The recommended way to install Azure PowerShell on Windows is with PowerShellGet.</span></span> <span data-ttu-id="20127-107">Инструкции по установке Azure PowerShell с помощью PowerShellGet см. в [этой статье](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="20127-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-azurerm-ps.md).</span></span>

> [!NOTE]
> <span data-ttu-id="20127-108">Для Azure PowerShell 6.x и более новых версий установка с помощью установщика веб-платформы больше не доступна.</span><span class="sxs-lookup"><span data-stu-id="20127-108">The Web Platform Installer method of installation is no longer available for versions of Azure PowerShell 6.x and higher.</span></span> <span data-ttu-id="20127-109">Если вам нужно использовать установщик веб-платформы, попробуйте вместо него использовать пакет MSI или установите более раннюю версию Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="20127-109">If you require use of the Web Platform Installer please consider using the MSI instead, or you can install an earlier version of Azure PowerShell.</span></span>

<span data-ttu-id="20127-110">Сведения об установке в средах Linux или macOS см. в [этом разделе](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="20127-110">To install on Linux or macOS environments, see [Install Azure PowerShell on macOS or Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="20127-111">Установка или обновление в Windows с помощью пакета MSI</span><span class="sxs-lookup"><span data-stu-id="20127-111">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="20127-112">Azure PowerShell можно установить с помощью MSI-файла из [GitHub](https://github.com/Azure/azure-powershell/releases/latest).</span><span class="sxs-lookup"><span data-stu-id="20127-112">Azure PowerShell can be installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/latest).</span></span> <span data-ttu-id="20127-113">Если вы установили предыдущие версии модулей Azure с помощью пакета MSI, установщик удалит их автоматически.</span><span class="sxs-lookup"><span data-stu-id="20127-113">If you have installed previous versions of Azure modules as an MSI, the installer automatically removes them.</span></span> <span data-ttu-id="20127-114">Пакет MSI устанавливает модули в `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="20127-114">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="20127-115">Устанавливаются оба модуля: `AzureRM` и `Azure`.</span><span class="sxs-lookup"><span data-stu-id="20127-115">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="20127-116">Используйте модуль `Azure`, только если вы работаете с классической моделью развертывания Azure.</span><span class="sxs-lookup"><span data-stu-id="20127-116">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="20127-117">Чтобы приступить к работе с Azure PowerShell, вам нужно загрузить `AzureRM` в текущий сеанс PowerShell. Для этого воспользуйтесь командлетом [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), после чего войдите в систему с помощью своих учетных данных Azure.</span><span class="sxs-lookup"><span data-stu-id="20127-117">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="20127-118">Эти действия нужно повторять для каждого нового сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="20127-118">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="20127-119">Чтобы автоматически импортировать модуль `AzureRM`, необходимо настроить профиль PowerShell. Подробнее об этом рассказывается [здесь](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="20127-119">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="20127-120">Чтобы узнать, как повторно использовать свои данные для входа в Azure в разных сеансах, см. статью [Использование учетных данных пользователя в разных сеансах PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="20127-120">To learn how to persist your Azure sign-in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>
