---
title: Общие сведения об Azure PowerShell
description: Общие сведения об установке и начале работы с модулем Az для Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 10/29/2018
ms.openlocfilehash: 7982e122d49db4d558648231d1ab8bfeed80be2d
ms.sourcegitcommit: 4acddc7026522c4fe39de2c4424917d88ee01b7e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/21/2018
ms.locfileid: "53736466"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="fc278-103">Общие сведения об Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="fc278-103">Overview of Azure PowerShell</span></span>

<span data-ttu-id="fc278-104">В Azure PowerShell доступен набор командлетов, которые используют модель [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) для управления ресурсами Azure.</span><span class="sxs-lookup"><span data-stu-id="fc278-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="fc278-105">Azure PowerShell использует .NET Standard, делая его доступным для Windows, macOS и Linux.</span><span class="sxs-lookup"><span data-stu-id="fc278-105">Azure PowerShell uses .NET Standard, making it available for Windows, macOS, and Linux.</span></span>
<span data-ttu-id="fc278-106">Azure PowerShell также доступен на Azure Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="fc278-106">Azure PowerShell is also available from Azure Cloud Shell.</span></span>

<span data-ttu-id="fc278-107">С помощью [Azure Cloud Shell](/azure/cloud-shell/overview) запускайте Azure PowerShell в браузере или [устанавливайте локально](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="fc278-107">Use [Azure Cloud Shell](/azure/cloud-shell/overview) to run Azure PowerShell in your browser, or [install locally](install-az-ps.md).</span></span> <span data-ttu-id="fc278-108">Ознакомьтесь со статьей [Начало работы с Azure PowerShell](get-started-azureps.md), чтобы изучить основы Azure PowerShell и приступить к работе с Azure.</span><span class="sxs-lookup"><span data-stu-id="fc278-108">Check out the [Get Started](get-started-azureps.md) article to learn the Azure PowerShell basics and get started with Azure.</span></span>

<span data-ttu-id="fc278-109">Сведения о последнем выпуске Azure PowerShell см. в [заметках о выпуске](release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="fc278-109">For information about the latest Azure PowerShell release, see the [release notes](release-notes-azureps.md).</span></span>

## <a name="about-the-new-az-module"></a><span data-ttu-id="fc278-110">Сведения о новом модуле Az</span><span class="sxs-lookup"><span data-stu-id="fc278-110">About the new Az module</span></span>

<span data-ttu-id="fc278-111">В этой документации описывается новый модуль Az для Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fc278-111">This documentation describes the new Az module for Azure PowerShell.</span></span> <span data-ttu-id="fc278-112">Этот новый модуль создан с нуля на платформе .NET Standard.</span><span class="sxs-lookup"><span data-stu-id="fc278-112">This new module is written from the ground up in .NET Standard.</span></span> <span data-ttu-id="fc278-113">Использование .NET Standard позволяет Azure PowerShell запускаться в PowerShell 5.x на Windows или в PowerShell 6 на любой другой платформе.</span><span class="sxs-lookup"><span data-stu-id="fc278-113">Using .NET Standard allows Azure PowerShell to run under PowerShell 5.x on Windows or PowerShell 6 on any platform.</span></span> <span data-ttu-id="fc278-114">Модуль Az теперь является предполагаемым способом для работы с Azure с помощью PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fc278-114">The Az module is now the intended way to interact with Azure through PowerShell.</span></span>
<span data-ttu-id="fc278-115">На AzureRM будут и дальше приходить исправления ошибок, но новые функции не будут доступны.</span><span class="sxs-lookup"><span data-stu-id="fc278-115">AzureRM will continue to get bug fixes, but no longer receive new features.</span></span>

<span data-ttu-id="fc278-116">В статье [Знакомство с новым модулем Az для Azure PowerShell](new-azureps-module-az.md) узнайте все сведения о новом модуле, включая переименование команд и планы обслуживания AzureRM.</span><span class="sxs-lookup"><span data-stu-id="fc278-116">Learn the full details about the new module, including how commands have been renamed and the maintenance plans for AzureRM, in the [Introducing the Azure PowerShell Az module](new-azureps-module-az.md).</span></span> <span data-ttu-id="fc278-117">Если вы хотите начать работу с использованием нового модуля прямо сейчас, см. раздел [Миграция с AzureRM на Az для Azure PowerShell](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="fc278-117">If you want to get started with using the new module right away, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

<span data-ttu-id="fc278-118">Доступны также [Общие сведения об Azure PowerShell](/powershell/azure/azurerm).</span><span class="sxs-lookup"><span data-stu-id="fc278-118">The [AzureRM documentation](/powershell/azure/azurerm) is also available.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="fc278-119">Если общие сведения об Azure PowerShell обновляются с учетом имен командлетов нового модуля, то статьи все еще используют команды AzureRM.</span><span class="sxs-lookup"><span data-stu-id="fc278-119">While the Azure documentation is being updated to reflect the new module cmdlet names, articles may still use the AzureRM commands.</span></span> <span data-ttu-id="fc278-120">После установки модуля Az рекомендуется включить псевдонимы командлетов AzureRM с помощью `Enable-AzureRmAlias`.</span><span class="sxs-lookup"><span data-stu-id="fc278-120">After installing the Az module, it's recommended that you enable the AzureRM cmdlet aliases with `Enable-AzureRmAlias`.</span></span> <span data-ttu-id="fc278-121">Дополнительные сведения см. в статье [Миграция с AzureRM на Az для Azure PowerShell](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="fc278-121">See the [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md) article for more details.</span></span>

## <a name="common-scenarios"></a><span data-ttu-id="fc278-122">Распространенные сценарии</span><span class="sxs-lookup"><span data-stu-id="fc278-122">Common scenarios</span></span>

<span data-ttu-id="fc278-123">Приведенные ниже примеры помогут вам понять, как реализовать типичные сценарии с помощью Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="fc278-123">The following samples can help you learn how to perform common scenarios with Azure PowerShell:</span></span>

* [<span data-ttu-id="fc278-124">Виртуальные машины Linux</span><span class="sxs-lookup"><span data-stu-id="fc278-124">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="fc278-125">Виртуальные машины Windows</span><span class="sxs-lookup"><span data-stu-id="fc278-125">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="fc278-126">Веб-приложения</span><span class="sxs-lookup"><span data-stu-id="fc278-126">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="fc278-127">Базы данных SQL</span><span class="sxs-lookup"><span data-stu-id="fc278-127">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="learn-powershell-basics"></a><span data-ttu-id="fc278-128">Изучение основ PowerShell</span><span class="sxs-lookup"><span data-stu-id="fc278-128">Learn PowerShell basics</span></span>

<span data-ttu-id="fc278-129">Если вы незнакомы с PowerShell, ознакомьтесь с вводными сведениями о PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fc278-129">If you're unfamiliar with PowerShell, an introduction may be helpful.</span></span>

* <span data-ttu-id="fc278-130">[Installing Windows PowerShell](/powershell/scripting/setup/installing-windows-powershell) (Установка Windows PowerShell)</span><span class="sxs-lookup"><span data-stu-id="fc278-130">[Installing PowerShell](/powershell/scripting/setup/installing-windows-powershell)</span></span>
* <span data-ttu-id="fc278-131">[Scripting with Windows PowerShell](/powershell/scripting/powershell-scripting) (Написание скриптов с помощью Windows PowerShell)</span><span class="sxs-lookup"><span data-stu-id="fc278-131">[Scripting with PowerShell](/powershell/scripting/powershell-scripting)</span></span>

<span data-ttu-id="fc278-132">Вы также можете посмотреть этот видеоролик: [Основы PowerShell. Часть 1. Начало работы с PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span><span class="sxs-lookup"><span data-stu-id="fc278-132">You can also watch this video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span></span>

<span data-ttu-id="fc278-133">Или пройдите [краткий курс по началу работы с PowerShell](https://mva.microsoft.com/liveevents/powershell-jumpstart) на сайте Microsoft Virtual Academy.</span><span class="sxs-lookup"><span data-stu-id="fc278-133">Or attend the Microsoft Virtual Academy's [Getting Started with PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart).</span></span>

## <a name="build-your-skills-with-microsoft-learn"></a><span data-ttu-id="fc278-134">Развитие навыков с помощью Microsoft Learn</span><span class="sxs-lookup"><span data-stu-id="fc278-134">Build your skills with Microsoft Learn</span></span>

- [<span data-ttu-id="fc278-135">Автоматизация задач Azure с помощью скриптов в PowerShell</span><span class="sxs-lookup"><span data-stu-id="fc278-135">Automate Azure tasks using scripts with PowerShell</span></span>](/learn/modules/automate-azure-tasks-with-powershell/)
- [<span data-ttu-id="fc278-136">Другие интерактивные руководства</span><span class="sxs-lookup"><span data-stu-id="fc278-136">More interactive learning...</span></span>](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="fc278-137">Другие модули Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="fc278-137">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="fc278-138">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="fc278-138">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="fc278-139">Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="fc278-139">Azure Information Protection</span></span>](/powershell/azure/aip/)
* [<span data-ttu-id="fc278-140">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="fc278-140">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="fc278-141">Azure ElasticDB</span><span class="sxs-lookup"><span data-stu-id="fc278-141">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
