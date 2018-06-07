---
title: Общие сведения о PowerShell для Azure Stack | Документация Майкрософт
description: Обзор установки и настройки модуля PowerShell для Azure Stack
author: SnehaGunda
manager: Byronr
ms.product: azure-stack
ms.devlang: powershell
ms.topic: reference
ms.author: sngun
ms.manager: byronr
ms.openlocfilehash: 3f55ff613004f0726e20255126b29bf7f64662b8
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/06/2018
ms.locfileid: "34820207"
---
# <a name="azure-stack-powershell"></a><span data-ttu-id="debef-103">PowerShell для Azure Stack</span><span class="sxs-lookup"><span data-stu-id="debef-103">Azure Stack PowerShell</span></span>

<span data-ttu-id="debef-104">Azure Stack необходимы следующие два модуля PowerShell:</span><span class="sxs-lookup"><span data-stu-id="debef-104">Azure Stack requires the following two PowerShell modules:</span></span>  

1. <span data-ttu-id="debef-105">Совместимый с Azure Stack модуль **AzureRM**, который доступен в комплекте установки профиля API версии **2017-03-09-profile**.</span><span class="sxs-lookup"><span data-stu-id="debef-105">The Azure Stack compatible **AzureRM** module which is available by installing the **2017-03-09-profile** API Version Profile.</span></span> <span data-ttu-id="debef-106">Командлеты, установленные с помощью этого профиля, могут использовать операторы и пользователи Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="debef-106">The cmdlets installed by using this profile can be used by Azure Stack operators and users.</span></span>

2. <span data-ttu-id="debef-107">Последняя версия модуля **AzureStack** — **1.2.11**.</span><span class="sxs-lookup"><span data-stu-id="debef-107">The most current version is the **1.2.11** install of the **AzureStack** module.</span></span> <span data-ttu-id="debef-108">Командлеты, установленные с помощью этого модуля, могут использовать только операторы Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="debef-108">The cmdlets installed by using this module can be used by Azure Stack operators only.</span></span> <span data-ttu-id="debef-109">С помощью командлетов PowerShell, предоставляемых этим модулем, операторы могут выполнять такие задачи, как управление предложениями, планами, службами, квотами и т. д.</span><span class="sxs-lookup"><span data-stu-id="debef-109">Operators can perform operations such as manage offers, plans, services, quotas, etc. by using the PowerShell cmdlets provided by this module.</span></span> <span data-ttu-id="debef-110">Чтобы узнать о командлетах PowerShell, доступных в этом модуле, ознакомьтесь со справочными материалами по [AzureStackAdmin](https://docs.microsoft.com/powershell/module/azurerm.azurestackadmin/?view=azurestackps-1.2.11#azurerm.azurestackadmin) и [AzureStackStorage](https://docs.microsoft.com/powershell/module/azurerm.azurestackstorage/?view=azurestackps-1.2.11#azurerm.azurestackstorage).</span><span class="sxs-lookup"><span data-stu-id="debef-110">To learn about the PowerShell cmdlets available in this module, see the [AzureStackAdmin](https://docs.microsoft.com/powershell/module/azurerm.azurestackadmin/?view=azurestackps-1.2.11#azurerm.azurestackadmin) and [AzureStackStorage](https://docs.microsoft.com/powershell/module/azurerm.azurestackstorage/?view=azurestackps-1.2.11#azurerm.azurestackstorage) Reference content.</span></span>

## <a name="next-steps"></a><span data-ttu-id="debef-111">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="debef-111">Next Steps</span></span>

* <span data-ttu-id="debef-112">[Install PowerShell for Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9) (Установка PowerShell для Azure Stack)</span><span class="sxs-lookup"><span data-stu-id="debef-112">[Install PowerShell for Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9)</span></span>
* <span data-ttu-id="debef-113">[Configure PowerShell for use with Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-configure?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9) (Настройка PowerShell для использования с Azure Stack)</span><span class="sxs-lookup"><span data-stu-id="debef-113">[Configure PowerShell for use with Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-configure?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9)</span></span>
