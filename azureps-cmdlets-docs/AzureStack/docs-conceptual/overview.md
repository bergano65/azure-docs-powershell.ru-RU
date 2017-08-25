---
title: "Общие сведения о PowerShell для Azure Stack | Документация Майкрософт"
description: "Обзор установки и настройки модуля PowerShell для Azure Stack"
author: SnehaGunda
manager: Byronr
ms.product: azure-stack
ms.service: powershell
ms.devlang: powershell
ms.topic: reference
ms.author: sngun
ms.manager: byronr
ms.openlocfilehash: 2a03697e0f3e80d63c48f2dc5615f6c99b9ef716
ms.sourcegitcommit: 226527be7cb647acfe2ea9ab151185053ab3c6db
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/29/2017
---
# <a name="azure-stack-powershell"></a><span data-ttu-id="e93c5-103">PowerShell для Azure Stack</span><span class="sxs-lookup"><span data-stu-id="e93c5-103">Azure Stack PowerShell</span></span> 

<span data-ttu-id="e93c5-104">Azure Stack необходимы следующие два модуля PowerShell:</span><span class="sxs-lookup"><span data-stu-id="e93c5-104">Azure Stack requires the following two PowerShell modules:</span></span>  

1. <span data-ttu-id="e93c5-105">Совместимый с Azure Stack модуль **AzureRM**, который доступен в комплекте установки профиля API версии **2017-03-09-profile**.</span><span class="sxs-lookup"><span data-stu-id="e93c5-105">The Azure Stack compatible **AzureRM** module which is available by installing the **2017-03-09-profile** API Version Profile.</span></span> <span data-ttu-id="e93c5-106">Командлеты, установленные с помощью этого профиля, могут использовать администраторы и клиенты облака Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="e93c5-106">The cmdlets installed by using this profile can be used by the Azure Stack cloud administrators and the tenants.</span></span> <span data-ttu-id="e93c5-107">Чтобы узнать о командлетах PowerShell, доступных в этом профиле, ознакомьтесь со справочными материалами по PowerShell для модуля [AzureRM версии 1.2.9](https://docs.microsoft.com/en-us/powershell/azure/overview?view=azurermps-1.2.9).</span><span class="sxs-lookup"><span data-stu-id="e93c5-107">To learn about the PowerShell cmdlets that are available in this profile, see the PowerShell reference content for the [1.2.9 version of AzureRM](https://docs.microsoft.com/en-us/powershell/azure/overview?view=azurermps-1.2.9) module.</span></span>  

2. <span data-ttu-id="e93c5-108">Модуль **AzureStack** версии **1.2.9**.</span><span class="sxs-lookup"><span data-stu-id="e93c5-108">The **1.2.9** version of the **AzureStack** module.</span></span> <span data-ttu-id="e93c5-109">Командлеты, установленные с помощью этого модуля, могут использовать только администраторы облака Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="e93c5-109">The cmdlets installed by using this module can be used by Azure Stack cloud administrators only.</span></span> <span data-ttu-id="e93c5-110">С помощью командлетов PowerShell, предоставляемых этим модулем, администратор может выполнять такие операции, как управление предложениями, планами, службами, квотами и т. д.</span><span class="sxs-lookup"><span data-stu-id="e93c5-110">Administrator can perform operations such as manage offers, plans, services, quotas, etc. by using the PowerShell cmdlets provided by this module.</span></span> <span data-ttu-id="e93c5-111">Чтобы узнать о командлетах PowerShell, доступных в этом модуле, ознакомьтесь со справочными материалами по [AzureStackAdmin](https://docs.microsoft.com/en-us/powershell/module/azurerm.azurestackadmin/?view=azurestackps-1.2.9#azurerm.azurestackadmin) и [AzureStackStorage](https://docs.microsoft.com/en-us/powershell/module/azurerm.azurestackstorage/?view=azurestackps-1.2.9#azurerm.azurestackstorage).</span><span class="sxs-lookup"><span data-stu-id="e93c5-111">To learn about the PowerShell cmdlets available in this module, see the [AzureStackAdmin](https://docs.microsoft.com/en-us/powershell/module/azurerm.azurestackadmin/?view=azurestackps-1.2.9#azurerm.azurestackadmin) and [AzureStackStorage](https://docs.microsoft.com/en-us/powershell/module/azurerm.azurestackstorage/?view=azurestackps-1.2.9#azurerm.azurestackstorage) Reference content.</span></span>

## <a name="next-steps"></a><span data-ttu-id="e93c5-112">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="e93c5-112">Next Steps</span></span>

* [<span data-ttu-id="e93c5-113">Install PowerShell for Azure Stack</span><span class="sxs-lookup"><span data-stu-id="e93c5-113">Install PowerShell for Azure Stack</span></span>](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9) (Установка PowerShell для Azure Stack)
* [<span data-ttu-id="e93c5-114">Configure PowerShell for use with Azure Stack</span><span class="sxs-lookup"><span data-stu-id="e93c5-114">Configure PowerShell for use with Azure Stack</span></span>](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-configure?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9) (Настройка PowerShell для использования с Azure Stack)


