---
title: Общие сведения об Azure PowerShell | Документация Майкрософт
description: Общие сведения об Azure PowerShell со ссылками на установку и настройку.
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 08/31/2017
ms.openlocfilehash: cd6b57ff6234895ec4f7a4200f9df0852b2280c2
ms.sourcegitcommit: 5f0013981fcea1d689649b9a2b2ffe84ae842e56
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2018
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="5b580-103">Общие сведения об Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="5b580-103">Overview of Azure PowerShell</span></span>

<span data-ttu-id="5b580-104">В Azure PowerShell доступен набор командлетов, которые используют модель [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) для управления ресурсами Azure.</span><span class="sxs-lookup"><span data-stu-id="5b580-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="5b580-105">Его можно использовать в браузере с [Azure Cloud Shell](/azure/cloud-shell/overview), а также установить на локальном компьютере и использовать в любом сеансе PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5b580-105">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can install it on your local machine and use it in any PowerShell session.</span></span>

<span data-ttu-id="5b580-106">Запускайте Azure PowerShell в браузере с помощью [Cloud Shell](/azure/cloud-shell/overview) либо [установите](install-azurerm-ps.md) его на компьютере.</span><span class="sxs-lookup"><span data-stu-id="5b580-106">Use the [Cloud Shell](/azure/cloud-shell/overview) to run the Azure PowerShell in your browser, or [install](install-azurerm-ps.md) it on own computer.</span></span> <span data-ttu-id="5b580-107">Прежде чем начать использовать эту среду, прочтите статью о [начале работы](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="5b580-107">Then read the [Get Started](get-started-azureps.md) article to begin using it.</span></span> <span data-ttu-id="5b580-108">Сведения о последнем выпуске см. в [заметках о выпуске](release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="5b580-108">For information about the latest release, see the [release notes](release-notes-azureps.md).</span></span>

<span data-ttu-id="5b580-109">Приведенные ниже примеры помогут вам понять, как реализовать типичные сценарии с помощью Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="5b580-109">The following samples can help you learn how to perform common scenarios with Azure PowerShell:</span></span>

* [<span data-ttu-id="5b580-110">Виртуальные машины Linux</span><span class="sxs-lookup"><span data-stu-id="5b580-110">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="5b580-111">Виртуальные машины Windows</span><span class="sxs-lookup"><span data-stu-id="5b580-111">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="5b580-112">Веб-приложения</span><span class="sxs-lookup"><span data-stu-id="5b580-112">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="5b580-113">Базы данных SQL</span><span class="sxs-lookup"><span data-stu-id="5b580-113">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

> [!NOTE]
> <span data-ttu-id="5b580-114">При наличии экземпляров, развернутых с помощью классической модели, которая не может быть преобразована, вы можете установить Azure PowerShell для управления службами.</span><span class="sxs-lookup"><span data-stu-id="5b580-114">If you have deployments that use the classic deployment model that cannot be converted, you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="5b580-115">Дополнительные сведения см. в статье об [установке модуля управления службами Azure PowerShell](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="5b580-115">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>


### <a name="need-help-with-powershell"></a><span data-ttu-id="5b580-116">Нужна помощь с PowerShell?</span><span class="sxs-lookup"><span data-stu-id="5b580-116">Need help with PowerShell?</span></span>

<span data-ttu-id="5b580-117">Если вы не знакомы с PowerShell, ознакомьтесь с вводными сведениями о PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5b580-117">If you are unfamiliar with PowerShell, you may find an introduction to PowerShell helpful.</span></span>

* <span data-ttu-id="5b580-118">[Installing Windows PowerShell](/powershell/scripting/installing-windows-powershell) (Установка Windows PowerShell)</span><span class="sxs-lookup"><span data-stu-id="5b580-118">[Installing PowerShell](/powershell/scripting/installing-windows-powershell)</span></span>
* <span data-ttu-id="5b580-119">[Scripting with Windows PowerShell](/powershell/scripting/scripting-with-windows-powershell) (Написание скриптов с помощью Windows PowerShell)</span><span class="sxs-lookup"><span data-stu-id="5b580-119">[Scripting with PowerShell](/powershell/scripting/scripting-with-windows-powershell)</span></span>

<span data-ttu-id="5b580-120">Вы также можете посмотреть этот видеоролик: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1) (Основы PowerShell (часть 1). Начало работы с PowerShell).</span><span class="sxs-lookup"><span data-stu-id="5b580-120">You can also watch this video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span></span>

<span data-ttu-id="5b580-121">Или пройдите [краткий курс по началу работы с PowerShell](https://mva.microsoft.com/liveevents/powershell-jumpstart) на сайте Microsoft Virtual Academy.</span><span class="sxs-lookup"><span data-stu-id="5b580-121">Or attend the Microsoft Virtual Academy's [Getting Started with PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart).</span></span>

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="5b580-122">Другие модули Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="5b580-122">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="5b580-123">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="5b580-123">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="5b580-124">Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="5b580-124">Azure Information Protection</span></span>](/powershell/azure/aip/)
* [<span data-ttu-id="5b580-125">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="5b580-125">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="5b580-126">Azure ElasticDB</span><span class="sxs-lookup"><span data-stu-id="5b580-126">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
