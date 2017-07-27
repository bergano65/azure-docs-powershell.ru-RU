---
title: "Общие сведения об Azure PowerShell | Документация Майкрософт"
description: "Общие сведения об Azure PowerShell со ссылками на установку и настройку."
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 07/26/2017
ms.openlocfilehash: 3772b68949dc9dba110e6015c8d2a8b944b26528
ms.sourcegitcommit: 20bcef86db4e4869125bb63085fcffd009c19280
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/27/2017
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="fb276-103">Общие сведения об Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="fb276-103">Overview of Azure PowerShell</span></span>

<span data-ttu-id="fb276-104">В Azure PowerShell доступен набор командлетов, которые используют модель [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) для управления ресурсами Azure.</span><span class="sxs-lookup"><span data-stu-id="fb276-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span>

<span data-ttu-id="fb276-105">См. статью об [установке](install-azurerm-ps.md), чтобы установить и запустить Azure PowerShell на компьютере.</span><span class="sxs-lookup"><span data-stu-id="fb276-105">Review the [Install](install-azurerm-ps.md) article to get Azure PowerShell up and running on your system.</span></span> <span data-ttu-id="fb276-106">Прежде чем начать использовать эту среду, прочтите статью о [начале работы](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="fb276-106">Then read the [Get Started](get-started-azureps.md) article to begin using it.</span></span> <span data-ttu-id="fb276-107">Сведения о последнем выпуске см. в [заметках о выпуске](release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="fb276-107">For information about the latest release, see the [release notes](release-notes-azureps.md).</span></span>

<span data-ttu-id="fb276-108">Приведенные ниже примеры помогут вам понять, как реализовать типичные сценарии с помощью Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="fb276-108">The following samples can help you learn how to perform common scenarios with Azure PowerShell:</span></span>

* [<span data-ttu-id="fb276-109">Виртуальные машины Linux</span><span class="sxs-lookup"><span data-stu-id="fb276-109">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="fb276-110">Виртуальные машины Windows</span><span class="sxs-lookup"><span data-stu-id="fb276-110">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="fb276-111">Веб-приложения</span><span class="sxs-lookup"><span data-stu-id="fb276-111">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="fb276-112">Базы данных SQL</span><span class="sxs-lookup"><span data-stu-id="fb276-112">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)


> [!NOTE]<span data-ttu-id="fb276-113"> При наличии экземпляров, развернутых с помощью классической модели, которая не может быть преобразована, вы можете установить Azure PowerShell для управления службами.</span><span class="sxs-lookup"><span data-stu-id="fb276-113"> > If you have deployments that use the classic deployment model that cannot be converted, you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="fb276-114">Дополнительные сведения см. в статье об [установке модуля управления службами Azure PowerShell](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="fb276-114">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>


### <a name="need-help-with-powershell"></a><span data-ttu-id="fb276-115">Нужна помощь с PowerShell?</span><span class="sxs-lookup"><span data-stu-id="fb276-115">Need help with PowerShell?</span></span>

<span data-ttu-id="fb276-116">Если вы не знакомы с PowerShell, ознакомьтесь с вводными сведениями о PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fb276-116">If you are unfamiliar with PowerShell, you may find an introduction to PowerShell helpful.</span></span> <span data-ttu-id="fb276-117">Чтобы начать работу с PowerShell, см. статью, посвященную [работе со сценариями в Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx).</span><span class="sxs-lookup"><span data-stu-id="fb276-117">To get started with PowerShell, see [Scripting with PowerShell](https://technet.microsoft.com/library/bb978526.aspx).</span></span>

<span data-ttu-id="fb276-118">Вы также можете посмотреть этот видеоролик: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1) (Основы PowerShell (часть 1). Начало работы с PowerShell).</span><span class="sxs-lookup"><span data-stu-id="fb276-118">You can also watch this video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span></span>

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="fb276-119">Другие модули Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="fb276-119">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="fb276-120">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="fb276-120">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="fb276-121">Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="fb276-121">Azure Information Protection</span></span>](/powershell/azure/aip/)
* [<span data-ttu-id="fb276-122">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="fb276-122">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="fb276-123">Azure ElasticDB</span><span class="sxs-lookup"><span data-stu-id="fb276-123">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
