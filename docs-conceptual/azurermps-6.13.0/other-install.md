---
title: Другие способы установки Azure PowerShell
description: Сведения о том, как установить Azure PowerShell без PowerShellGet с помощью пакета MSI.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/16/2018
ms.openlocfilehash: b442da364a01cd6022c14cbb32a9b633676ca8c7
ms.sourcegitcommit: 93f93b90ef88c2659be95f3acaba514fe9639169
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2018
ms.locfileid: "52828864"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a><span data-ttu-id="4a9d7-103">Установка Azure PowerShell в ОС Windows с помощью пакета MSI</span><span class="sxs-lookup"><span data-stu-id="4a9d7-103">Install Azure PowerShell on Windows with MSI</span></span>

<span data-ttu-id="4a9d7-104">В этой статье объясняется, как установить Azure PowerShell в ОС Windows с помощью установщика MSI.</span><span class="sxs-lookup"><span data-stu-id="4a9d7-104">This article explains how to install Azure PowerShell on Windows using an MSI installer.</span></span>  
<span data-ttu-id="4a9d7-105">Используйте эти способы установки только в том случае, если это необходимо для вашей системы.</span><span class="sxs-lookup"><span data-stu-id="4a9d7-105">Use these installation methods only if they're necessary for your system.</span></span> <span data-ttu-id="4a9d7-106">Мы рекомендуем устанавливать Azure PowerShell в ОС Windows с помощью PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="4a9d7-106">The recommended way to install Azure PowerShell on Windows is with PowerShellGet.</span></span> <span data-ttu-id="4a9d7-107">Инструкции по установке Azure PowerShell с помощью PowerShellGet см. в [этой статье](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="4a9d7-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-azurerm-ps.md).</span></span>

> [!NOTE]
> <span data-ttu-id="4a9d7-108">Для Azure PowerShell 6.x и более новых версий установка с помощью установщика веб-платформы больше не доступна.</span><span class="sxs-lookup"><span data-stu-id="4a9d7-108">The Web Platform Installer method of installation is no longer available for versions of Azure PowerShell 6.x and higher.</span></span> <span data-ttu-id="4a9d7-109">Если вам нужно использовать установщик веб-платформы, попробуйте вместо него использовать пакет MSI или установите более раннюю версию Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4a9d7-109">If you require use of the Web Platform Installer please consider using the MSI instead, or you can install an earlier version of Azure PowerShell.</span></span>

<span data-ttu-id="4a9d7-110">Сведения об установке в средах Linux или macOS см. в [этом разделе](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="4a9d7-110">To install on Linux or macOS environments, see [Install Azure PowerShell on macOS or Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="4a9d7-111">Установка или обновление в Windows с помощью пакета MSI</span><span class="sxs-lookup"><span data-stu-id="4a9d7-111">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="4a9d7-112">Azure PowerShell можно установить с помощью MSI-файла из [GitHub](https://github.com/Azure/azure-powershell/releases/latest).</span><span class="sxs-lookup"><span data-stu-id="4a9d7-112">Azure PowerShell can be installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/latest).</span></span> <span data-ttu-id="4a9d7-113">Если вы установили предыдущие версии модулей Azure с помощью пакета MSI, установщик удалит их автоматически.</span><span class="sxs-lookup"><span data-stu-id="4a9d7-113">If you have installed previous versions of Azure modules as an MSI, the installer automatically removes them.</span></span> <span data-ttu-id="4a9d7-114">Пакет MSI устанавливает модули в `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="4a9d7-114">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="4a9d7-115">Устанавливаются оба модуля: `AzureRM` и `Azure`.</span><span class="sxs-lookup"><span data-stu-id="4a9d7-115">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="4a9d7-116">Используйте модуль `Azure`, только если вы работаете с классической моделью развертывания Azure.</span><span class="sxs-lookup"><span data-stu-id="4a9d7-116">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="4a9d7-117">Чтобы начать работу с Azure PowerShell, выполните вход, используя данные своей учетной записи в Azure.</span><span class="sxs-lookup"><span data-stu-id="4a9d7-117">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

> [!NOTE]
>
> <span data-ttu-id="4a9d7-118">Если вы отключили автоматическую загрузку модулей, вам нужно вручную импортировать модуль с помощью `Import-Module AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="4a9d7-118">If you've disabled module autoloading, you need to manually import the module with `Import-Module AzureRM`.</span></span> <span data-ttu-id="4a9d7-119">Из-за структуры модуля эта операция может занять несколько секунд.</span><span class="sxs-lookup"><span data-stu-id="4a9d7-119">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="4a9d7-120">Это действие нужно будет повторить для каждого нового сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4a9d7-120">You'll need to repeat this step for every new PowerShell session you start.</span></span> <span data-ttu-id="4a9d7-121">Чтобы узнать, как повторно использовать свои данные для входа в Azure в разных сеансах PowerShell, см. статью [Использование учетных данных пользователя в разных сеансах PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="4a9d7-121">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>
