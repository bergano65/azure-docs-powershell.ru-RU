---
title: Общие сведения об Azure PowerShell
description: Общие сведения об установке и начале работы с модулем Az для Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 01/10/2019
ms.openlocfilehash: 45ab083dd133c8c7b8dbe902484c92564bc216b9
ms.sourcegitcommit: ae4540a90508db73335a54408dfd6cdf3712a1e9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/17/2019
ms.locfileid: "59364254"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="585f1-103">Общие сведения об Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="585f1-103">Overview of Azure PowerShell</span></span>

<span data-ttu-id="585f1-104">В Azure PowerShell доступен набор командлетов, которые используют модель [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) для управления ресурсами Azure.</span><span class="sxs-lookup"><span data-stu-id="585f1-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="585f1-105">Azure PowerShell использует .NET Standard, делая его доступным для Windows, macOS и Linux.</span><span class="sxs-lookup"><span data-stu-id="585f1-105">Azure PowerShell uses .NET Standard, making it available for Windows, macOS, and Linux.</span></span>
<span data-ttu-id="585f1-106">Среда Azure PowerShell также доступна в Azure Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="585f1-106">Azure PowerShell is also available on Azure Cloud Shell.</span></span>

## <a name="about-the-new-az-module"></a><span data-ttu-id="585f1-107">Сведения о новом модуле Az</span><span class="sxs-lookup"><span data-stu-id="585f1-107">About the new Az module</span></span>

<span data-ttu-id="585f1-108">В этой документации описывается новый модуль Az для Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="585f1-108">This documentation describes the new Az module for Azure PowerShell.</span></span> <span data-ttu-id="585f1-109">Этот новый модуль создан с нуля на платформе .NET Standard.</span><span class="sxs-lookup"><span data-stu-id="585f1-109">This new module is written from the ground up in .NET Standard.</span></span> <span data-ttu-id="585f1-110">Использование .NET Standard позволяет Azure PowerShell запускаться в PowerShell 5 на Windows или в PowerShell 6 на любой другой платформе.</span><span class="sxs-lookup"><span data-stu-id="585f1-110">Using .NET Standard allows Azure PowerShell to run under PowerShell 5 on Windows or PowerShell 6 on any platform.</span></span> <span data-ttu-id="585f1-111">Модуль Az теперь является предполагаемым способом для работы с Azure с помощью PowerShell.</span><span class="sxs-lookup"><span data-stu-id="585f1-111">The Az module is now the intended way to interact with Azure through PowerShell.</span></span>
<span data-ttu-id="585f1-112">На AzureRM будут и дальше приходить исправления ошибок, но новые функции не будут доступны.</span><span class="sxs-lookup"><span data-stu-id="585f1-112">AzureRM will continue to get bug fixes, but no longer receive new features.</span></span>

<span data-ttu-id="585f1-113">В статье [Знакомство с новым модулем Az для Azure PowerShell](new-azureps-module-az.md) узнайте все сведения о новом модуле, включая переименование команд и планы обслуживания AzureRM.</span><span class="sxs-lookup"><span data-stu-id="585f1-113">Learn the full details about the new module, including how commands have been renamed and the maintenance plans for AzureRM, in the [Introducing the Azure PowerShell Az module](new-azureps-module-az.md).</span></span> <span data-ttu-id="585f1-114">Если вы хотите начать работу с использованием нового модуля прямо сейчас, см. раздел [Миграция с AzureRM на Az для Azure PowerShell](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="585f1-114">If you want to get started with using the new module right away, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

<span data-ttu-id="585f1-115">Доступны также [Общие сведения об Azure PowerShell](/powershell/azure/azurerm).</span><span class="sxs-lookup"><span data-stu-id="585f1-115">The [AzureRM documentation](/powershell/azure/azurerm) is also available.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="585f1-116">Если общие сведения об Azure PowerShell обновляются с учетом имен командлетов нового модуля, то статьи все еще используют команды AzureRM.</span><span class="sxs-lookup"><span data-stu-id="585f1-116">While the Azure documentation is being updated to reflect the new module cmdlet names, articles may still use the AzureRM commands.</span></span> <span data-ttu-id="585f1-117">После установки модуля Az рекомендуется включить псевдонимы командлетов AzureRM с помощью `Enable-AzureRmAlias`.</span><span class="sxs-lookup"><span data-stu-id="585f1-117">After installing the Az module, it's recommended that you enable the AzureRM cmdlet aliases with `Enable-AzureRmAlias`.</span></span> <span data-ttu-id="585f1-118">Дополнительные сведения см. в статье [Миграция с AzureRM на Az для Azure PowerShell](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="585f1-118">See the [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md) article for more details.</span></span>

## <a name="run-or-install"></a><span data-ttu-id="585f1-119">Запуск или установка</span><span class="sxs-lookup"><span data-stu-id="585f1-119">Run or install</span></span>

<span data-ttu-id="585f1-120">Вы можете установить Azure PowerShell на PowerShell 5.1 или более поздней версии на платформе Windows, PowerShell 6 — на любой платформе, а также запустить среду в Azure Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="585f1-120">You can install Azure PowerShell on PowerShell 5.1 or higher on Windows, PowerShell 6 on any platform, or run in Azure Cloud Shell.</span></span>

* <span data-ttu-id="585f1-121">Чтобы запустить Azure PowerShell в браузере с Azure Cloud Shell, ознакомьтесь со статьей [Краткое руководство по использованию PowerShell в Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span><span class="sxs-lookup"><span data-stu-id="585f1-121">To run in your browser with Azure Cloud Shell, see [Quickstart for PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span></span>
* <span data-ttu-id="585f1-122">Чтобы установить Azure PowerShell в своей системе, воспользуйтесь [этими инструкциями](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="585f1-122">To install Azure PowerShell on your system, see [Install Azure PowerShell](install-az-ps.md).</span></span>

<span data-ttu-id="585f1-123">Сведения о последнем выпуске Azure PowerShell см. в [заметках о выпуске](release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="585f1-123">For information about the latest Azure PowerShell release, see the [release notes](release-notes-azureps.md).</span></span>

## <a name="get-started"></a><span data-ttu-id="585f1-124">Начало работы</span><span class="sxs-lookup"><span data-stu-id="585f1-124">Get Started</span></span>

<span data-ttu-id="585f1-125">Ознакомьтесь со статьей [Get started with Azure PowerShell](get-started-azureps.md) (Начало работы с Azure PowerShell), чтобы изучить основы Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="585f1-125">Read the [Get Started with Azure PowerShell](get-started-azureps.md) article to learn the Azure PowerShell basics.</span></span> <span data-ttu-id="585f1-126">Если вы еще не работали с PowerShell, ознакомьтесь с вводными сведениями об этой среде:</span><span class="sxs-lookup"><span data-stu-id="585f1-126">If you're not familiar with PowerShell, an introduction might be helpful:</span></span>

* [<span data-ttu-id="585f1-127">Установка PowerShell</span><span class="sxs-lookup"><span data-stu-id="585f1-127">Install PowerShell</span></span>](/powershell/scripting/install/installing-powershell)
* <span data-ttu-id="585f1-128">[Scripting with Windows PowerShell](/powershell/scripting/powershell-scripting) (Написание скриптов с помощью Windows PowerShell)</span><span class="sxs-lookup"><span data-stu-id="585f1-128">[Scripting with PowerShell](/powershell/scripting/powershell-scripting)</span></span>
* <span data-ttu-id="585f1-129">[Основы PowerShell. (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1) (Основы PowerShell. Часть 1. Начало работы с PowerShell)</span><span class="sxs-lookup"><span data-stu-id="585f1-129">[PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1)</span></span>
* <span data-ttu-id="585f1-130">[Краткий курс по началу работы с PowerShell](https://mva.microsoft.com/liveevents/powershell-jumpstart) на сайте Microsoft Virtual Academy</span><span class="sxs-lookup"><span data-stu-id="585f1-130">Microsoft Virtual Academy's [Getting Started with PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart)</span></span>

<span data-ttu-id="585f1-131">Приведенные ниже примеры помогут вам разобраться в некоторых вариантах использования Azure:</span><span class="sxs-lookup"><span data-stu-id="585f1-131">The following samples can help you with some common uses of Azure:</span></span>

* [<span data-ttu-id="585f1-132">Виртуальные машины Linux</span><span class="sxs-lookup"><span data-stu-id="585f1-132">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="585f1-133">Виртуальные машины Windows</span><span class="sxs-lookup"><span data-stu-id="585f1-133">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="585f1-134">Веб-приложения</span><span class="sxs-lookup"><span data-stu-id="585f1-134">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="585f1-135">Базы данных SQL</span><span class="sxs-lookup"><span data-stu-id="585f1-135">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="build-your-skills-with-microsoft-learn"></a><span data-ttu-id="585f1-136">Развитие навыков с помощью Microsoft Learn</span><span class="sxs-lookup"><span data-stu-id="585f1-136">Build your skills with Microsoft Learn</span></span>

- [<span data-ttu-id="585f1-137">Автоматизация задач Azure с помощью скриптов в PowerShell</span><span class="sxs-lookup"><span data-stu-id="585f1-137">Automate Azure tasks using scripts with PowerShell</span></span>](/learn/modules/automate-azure-tasks-with-powershell/)
- [<span data-ttu-id="585f1-138">Другие интерактивные руководства</span><span class="sxs-lookup"><span data-stu-id="585f1-138">More interactive learning...</span></span>](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="585f1-139">Другие модули Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="585f1-139">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="585f1-140">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="585f1-140">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="585f1-141">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="585f1-141">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="585f1-142">Azure ElasticDB</span><span class="sxs-lookup"><span data-stu-id="585f1-142">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
