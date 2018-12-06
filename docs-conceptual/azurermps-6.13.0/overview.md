---
title: Общие сведения об Azure PowerShell | Документация Майкрософт
description: Общие сведения об Azure PowerShell со ссылками на установку и настройку.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 09/11/2018
ms.openlocfilehash: bdd8e69a2ea9df8b4fff100e1f3cc4c82d2d9d9d
ms.sourcegitcommit: 93f93b90ef88c2659be95f3acaba514fe9639169
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2018
ms.locfileid: "52827349"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="51263-103">Общие сведения об Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="51263-103">Overview of Azure PowerShell</span></span>

<span data-ttu-id="51263-104">В Azure PowerShell доступен набор командлетов, которые используют модель [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) для управления ресурсами Azure.</span><span class="sxs-lookup"><span data-stu-id="51263-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="51263-105">Его можно использовать в браузере с [Azure Cloud Shell](/azure/cloud-shell/overview), а также установить на локальном компьютере и использовать в любом сеансе PowerShell.</span><span class="sxs-lookup"><span data-stu-id="51263-105">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can install it on your local machine and use it in any PowerShell session.</span></span>

<span data-ttu-id="51263-106">Запускайте Azure PowerShell в браузере с помощью [Cloud Shell](/azure/cloud-shell/overview) либо [установите](install-azurerm-ps.md) его на компьютере.</span><span class="sxs-lookup"><span data-stu-id="51263-106">Use the [Cloud Shell](/azure/cloud-shell/overview) to run the Azure PowerShell in your browser, or [install](install-azurerm-ps.md) it on own computer.</span></span> <span data-ttu-id="51263-107">Прежде чем начать использовать эту среду, прочтите статью о [начале работы](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="51263-107">Then read the [Get Started](get-started-azureps.md) article to begin using it.</span></span> <span data-ttu-id="51263-108">Сведения о последнем выпуске см. в [заметках о выпуске](release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="51263-108">For information about the latest release, see the [release notes](release-notes-azureps.md).</span></span>

<span data-ttu-id="51263-109">Приведенные ниже примеры помогут вам понять, как реализовать типичные сценарии с помощью Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="51263-109">The following samples can help you learn how to perform common scenarios with Azure PowerShell:</span></span>

* [<span data-ttu-id="51263-110">Виртуальные машины Linux</span><span class="sxs-lookup"><span data-stu-id="51263-110">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="51263-111">Виртуальные машины Windows</span><span class="sxs-lookup"><span data-stu-id="51263-111">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="51263-112">Веб-приложения</span><span class="sxs-lookup"><span data-stu-id="51263-112">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="51263-113">Базы данных SQL</span><span class="sxs-lookup"><span data-stu-id="51263-113">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

[!INCLUDE[az-replacing-azurerm](../includes/az-replacing-azurerm.md)]

## <a name="learn-powershell-basics"></a><span data-ttu-id="51263-114">Изучение основ PowerShell</span><span class="sxs-lookup"><span data-stu-id="51263-114">Learn PowerShell basics</span></span>

<span data-ttu-id="51263-115">Если вы не знакомы с PowerShell, ознакомьтесь с вводными сведениями о PowerShell.</span><span class="sxs-lookup"><span data-stu-id="51263-115">If you're unfamiliar with PowerShell, an introduction to PowerShell may be helpful.</span></span>

* <span data-ttu-id="51263-116">[Installing Windows PowerShell](/powershell/scripting/setup/installing-windows-powershell) (Установка Windows PowerShell)</span><span class="sxs-lookup"><span data-stu-id="51263-116">[Installing PowerShell](/powershell/scripting/setup/installing-windows-powershell)</span></span>
* <span data-ttu-id="51263-117">[Scripting with Windows PowerShell](/powershell/scripting/powershell-scripting) (Написание скриптов с помощью Windows PowerShell)</span><span class="sxs-lookup"><span data-stu-id="51263-117">[Scripting with PowerShell](/powershell/scripting/powershell-scripting)</span></span>

<span data-ttu-id="51263-118">Вы также можете посмотреть этот видеоролик: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1) (Основы PowerShell (часть 1). Начало работы с PowerShell).</span><span class="sxs-lookup"><span data-stu-id="51263-118">You can also watch this video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span></span>

<span data-ttu-id="51263-119">Или пройдите [краткий курс по началу работы с PowerShell](https://mva.microsoft.com/liveevents/powershell-jumpstart) на сайте Microsoft Virtual Academy.</span><span class="sxs-lookup"><span data-stu-id="51263-119">Or attend the Microsoft Virtual Academy's [Getting Started with PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart).</span></span>

## <a name="build-your-skills-with-microsoft-learn"></a><span data-ttu-id="51263-120">Развитие навыков с помощью Microsoft Learn</span><span class="sxs-lookup"><span data-stu-id="51263-120">Build your skills with Microsoft Learn</span></span>

- [<span data-ttu-id="51263-121">Автоматизация задач Azure с помощью скриптов в PowerShell</span><span class="sxs-lookup"><span data-stu-id="51263-121">Automate Azure tasks using scripts with PowerShell</span></span>](/learn/modules/automate-azure-tasks-with-powershell/)
- [<span data-ttu-id="51263-122">Другие интерактивные руководства</span><span class="sxs-lookup"><span data-stu-id="51263-122">More interactive learning...</span></span>](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="51263-123">Другие модули Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="51263-123">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="51263-124">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="51263-124">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="51263-125">Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="51263-125">Azure Information Protection</span></span>](/powershell/azure/aip/)
* [<span data-ttu-id="51263-126">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="51263-126">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="51263-127">Azure ElasticDB</span><span class="sxs-lookup"><span data-stu-id="51263-127">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
