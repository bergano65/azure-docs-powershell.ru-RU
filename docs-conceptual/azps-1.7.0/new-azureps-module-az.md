---
title: Знакомство с модулем Az для Azure PowerShell
description: Знакомством с новым модулем Az для Azure PowerShell, который заменяет модуль AzureRM.
ms.date: 12/13/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 10665a72bc7dcae8ecf36b5ef4e2ab285a0e78b7
ms.sourcegitcommit: 89066b7c4b527357bb2024e1ad708df84c131804
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2019
ms.locfileid: "59364221"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a><span data-ttu-id="64051-103">Знакомство с новым модулем Az для Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="64051-103">Introducing the new Azure PowerShell Az module</span></span>

<span data-ttu-id="64051-104">Начиная с декабря 2018 года модуль Az для Azure PowerShell есть в общедоступном выпуске и теперь является предполагаемым модулем PowerShell для работы с Azure.</span><span class="sxs-lookup"><span data-stu-id="64051-104">Starting in December 2018, the Azure PowerShell Az module is in general release and now the intended PowerShell module for interacting with Azure.</span></span> <span data-ttu-id="64051-105">Модуль Az предлагает более короткие имена команд, улучшенную стабильность, а также кроссплатформенную поддержку.</span><span class="sxs-lookup"><span data-stu-id="64051-105">Az offers shorter commands, improved stability, and cross-platform support.</span></span> <span data-ttu-id="64051-106">Az также обеспечивает равенство функций с модулем AzureRM и предлагает простой метод миграции со старого модуля.</span><span class="sxs-lookup"><span data-stu-id="64051-106">Az also offers feature parity and an easy migration path from AzureRM.</span></span>

<span data-ttu-id="64051-107">Модуль Az использует библиотеку .NET Standard, то есть он работает в PowerShell 5 и PowerShell 6.</span><span class="sxs-lookup"><span data-stu-id="64051-107">Az uses the .NET Standard library, which means it runs on PowerShell 5 and PowerShell 6.</span></span>
<span data-ttu-id="64051-108">PowerShell 6 может запускаться на Linux, macOS и Windows, то есть модуль Azure PowerShell теперь доступен на всех платформах.</span><span class="sxs-lookup"><span data-stu-id="64051-108">Since PowerShell 6 can run on Linux, macOS, and Windows, Azure PowerShell is now available for all platforms.</span></span>
<span data-ttu-id="64051-109">Использование .NET Standard позволяет унифицировать кодовую базу Azure PowerShell с минимальными последствиями для пользователей.</span><span class="sxs-lookup"><span data-stu-id="64051-109">Using .NET Standard allows us to unify the code base of Azure PowerShell with minimal impact on users.</span></span>

<span data-ttu-id="64051-110">Az — это новый модуль, поэтому нумерация версий начинается с 1.0.0.</span><span class="sxs-lookup"><span data-stu-id="64051-110">Az is a new module, so the version has been reset to 1.0.0.</span></span>

## <a name="upgrade-to-az"></a><span data-ttu-id="64051-111">Обновление до Az</span><span class="sxs-lookup"><span data-stu-id="64051-111">Upgrade to Az</span></span>

<span data-ttu-id="64051-112">Мы рекомендуем всем пользователям перейти на новый модуль Az.</span><span class="sxs-lookup"><span data-stu-id="64051-112">It's recommended that all users upgrade to the new Az module.</span></span> <span data-ttu-id="64051-113">Для этого выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="64051-113">To do so:</span></span>

* <span data-ttu-id="64051-114">__РЕКОМЕНДУЕТСЯ__: [Удалите модуль AzureRM для Azure PowerShell](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module).</span><span class="sxs-lookup"><span data-stu-id="64051-114">__RECOMMENDED__: [Uninstall the Azure PowerShell AzureRM module](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)</span></span>
* [<span data-ttu-id="64051-115">Установка модуля Az для Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="64051-115">Install the Azure PowerShell Az module</span></span>](/powershell/azure/install-az-ps)
* <span data-ttu-id="64051-116">Активируйте режим совместимости, чтобы добавить псевдонимы для командлетов AzureRM с помощью `Enable-AzureRMAlias`, пока вы не ознакомитесь с новым набором команд.</span><span class="sxs-lookup"><span data-stu-id="64051-116">Enable compatibility mode to add aliases for AzureRM cmdlets with `Enable-AzureRMAlias` while you become familiar with the new command set.</span></span> <span data-ttu-id="64051-117">Включайте псевдонимы __только__ в том случае, если у вас не установлено AzureRM.</span><span class="sxs-lookup"><span data-stu-id="64051-117">__Only__ enable aliases if you do not have AzureRM installed.</span></span>

## <a name="migrate-existing-scripts-to-az"></a><span data-ttu-id="64051-118">Миграция существующих скриптов на Az</span><span class="sxs-lookup"><span data-stu-id="64051-118">Migrate existing scripts to Az</span></span>

<span data-ttu-id="64051-119">Значительные обновления могут быть сопряжены со сложностями.</span><span class="sxs-lookup"><span data-stu-id="64051-119">Major updates can be inconvenient.</span></span> <span data-ttu-id="64051-120">Однако в модуле Az предусмотрен режим совместимости, который позволяет использовать существующие скрипты, пока вы выполняете обновление для нового синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="64051-120">However, the Az module has a compatibility mode to help you use existing scripts while you work on updates to the new syntax.</span></span> <span data-ttu-id="64051-121">Используйте командлет `Enable-AzureRmAlias` для активации режима совместимости AzureRM.</span><span class="sxs-lookup"><span data-stu-id="64051-121">Use the `Enable-AzureRmAlias` cmdlet to enable the AzureRM compatibility mode.</span></span> <span data-ttu-id="64051-122">Этот командлет определяет имена командлета AzureRM как псевдонимы для новых имен командлета Az.</span><span class="sxs-lookup"><span data-stu-id="64051-122">This cmdlet defines AzureRM cmdlet names as aliases for the new Az cmdlet names.</span></span>

<span data-ttu-id="64051-123">Новые имена командлетов выбраны таким образом, чтобы их было легко запомнить.</span><span class="sxs-lookup"><span data-stu-id="64051-123">The new cmdlet names have been designed to be easy to learn.</span></span> <span data-ttu-id="64051-124">Вместо имен командлетов `AzureRm` или `Azure` используйте `Az`.</span><span class="sxs-lookup"><span data-stu-id="64051-124">Instead of using `AzureRm` or `Azure` in cmdlet names, use `Az`.</span></span> <span data-ttu-id="64051-125">Например, вместо старой команды `New-AzureRMVm` используется `New-AzVm`.</span><span class="sxs-lookup"><span data-stu-id="64051-125">For example, the old command `New-AzureRMVm` has become `New-AzVm`.</span></span>

<span data-ttu-id="64051-126">Полное описание процесса миграции см. в статье [Миграция с AzureRM на Az для Azure PowerShell](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="64051-126">For a full description of the migration process, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

## <a name="the-future-of-support-for-azurerm"></a><span data-ttu-id="64051-127">Поддержка AzureRM в будущем</span><span class="sxs-lookup"><span data-stu-id="64051-127">The future of support for AzureRM</span></span>

<span data-ttu-id="64051-128">Существующий модуль AzureRM больше не будет получать новые командлеты или функции.</span><span class="sxs-lookup"><span data-stu-id="64051-128">The existing AzureRM module will no longer receive new cmdlets or features.</span></span> <span data-ttu-id="64051-129">Но AzureRM по-прежнему официально поддерживается и будет получать исправления ошибок до декабря 2020 г.</span><span class="sxs-lookup"><span data-stu-id="64051-129">However, AzureRM is still officially maintained and will get bug fixes up through December 2020.</span></span> <span data-ttu-id="64051-130">Для поддержки новых служб и функций Azure перейдите на модуль Az.</span><span class="sxs-lookup"><span data-stu-id="64051-130">To keep up with the latest Azure services and features, switch to the Az module.</span></span>
