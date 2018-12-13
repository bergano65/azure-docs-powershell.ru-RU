---
title: Знакомство с модулем Az для Azure PowerShell
description: Знакомством с новым модулем Az для Azure PowerShell, который заменяет модуль AzureRM.
ms.date: 11/07/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: b0f31341d4344bdac5b4d657a1f66acfd9984dda
ms.sourcegitcommit: 087c588169786c005a3c177624fb3ac6c8870125
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/13/2018
ms.locfileid: "53217547"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a><span data-ttu-id="9f716-103">Знакомство с новым модулем Az для Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="9f716-103">Introducing the new Azure PowerShell Az module</span></span>

<span data-ttu-id="9f716-104">Модуль `Az` для Azure PowerShell выпущен в виде общедоступной предварительной версии в ноябре 2018 г.</span><span class="sxs-lookup"><span data-stu-id="9f716-104">Starting in November 2018, the Azure PowerShell `Az` module is available for full public preview.</span></span>
<span data-ttu-id="9f716-105">Модуль Az позволяет использовать более короткие имена команд, обеспечивает улучшенную стабильность, а также поддержку Windows, macOS и Linux.</span><span class="sxs-lookup"><span data-stu-id="9f716-105">Az offers shorter commands, improved stability, and supports Windows, macOS, and Linux.</span></span> <span data-ttu-id="9f716-106">Az также обеспечивает равенство функций с модулем AzureRM и предлагает простой метод миграции со старого модуля.</span><span class="sxs-lookup"><span data-stu-id="9f716-106">Az also offers feature parity and an easy migration path from AzureRM.</span></span>

<span data-ttu-id="9f716-107">Модуль Az использует библиотеку .NET Standard, благодаря чему он может работать в PowerShell 5.x и PowerShell 6.x.</span><span class="sxs-lookup"><span data-stu-id="9f716-107">Az uses the .NET Standard library, which means it runs on PowerShell 5.x and PowerShell 6.x.</span></span>
<span data-ttu-id="9f716-108">PowerShell 6.x может запускаться в Linux, macOS и Windows, а это значит, что модуль Az доступен для всех платформ.</span><span class="sxs-lookup"><span data-stu-id="9f716-108">Since PowerShell 6.x can run on Linux, macOS, and Windows, that means Az is available for all platforms.</span></span>
<span data-ttu-id="9f716-109">Использование .NET Standard позволяет унифицировать кодовую базу Azure PowerShell с минимальными последствиями для пользователей.</span><span class="sxs-lookup"><span data-stu-id="9f716-109">Using .NET Standard allows us to unify the code base of Azure PowerShell with minimal impact on users.</span></span>

<span data-ttu-id="9f716-110">Az — это новый модуль, поэтому нумерация версий начата с начала.</span><span class="sxs-lookup"><span data-stu-id="9f716-110">Az is a new module, so the version has been reset.</span></span> <span data-ttu-id="9f716-111">Первому стабильному выпуску будет присвоен номер 1.0, но модуль будет иметь равенство функций с AzureRM по состоянию на ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="9f716-111">The first stable release will be 1.0, but the module has feature parity with AzureRm as of November 2018.</span></span>

## <a name="upgrade-to-az"></a><span data-ttu-id="9f716-112">Обновление до Az</span><span class="sxs-lookup"><span data-stu-id="9f716-112">Upgrade to Az</span></span>

<span data-ttu-id="9f716-113">Пользователям рекомендуется выполнить обновление до нового модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="9f716-113">It's recommended that users upgrade to the new `Az` module.</span></span> <span data-ttu-id="9f716-114">Для этого выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="9f716-114">To do so:</span></span>

* <span data-ttu-id="9f716-115">[Удалите модуль AzureRM для Azure PowerShell](/powershell/azure/uninstall-azurerm-ps).</span><span class="sxs-lookup"><span data-stu-id="9f716-115">[Uninstall the Azure PowerShell AzureRM module](/powershell/azure/uninstall-azurerm-ps)</span></span>
* <span data-ttu-id="9f716-116">[Установите модуль Az для Azure PowerShell](/powershell/azure/install-az-ps).</span><span class="sxs-lookup"><span data-stu-id="9f716-116">[Install the Azure PowerShell Az module](/powershell/azure/install-az-ps)</span></span>
* <span data-ttu-id="9f716-117">Активируйте режим совместимости с AzureRM с помощью команды `Enable-AzureRMAlias`, пока вы не ознакомитесь с новым набором команд.</span><span class="sxs-lookup"><span data-stu-id="9f716-117">Enable compatibility mode for AzureRM with `Enable-AzureRMAlias` while you become familiar with the new command set.</span></span>

## <a name="migrate-existing-scripts-to-az"></a><span data-ttu-id="9f716-118">Миграция существующих скриптов на Az</span><span class="sxs-lookup"><span data-stu-id="9f716-118">Migrate existing scripts to Az</span></span>

<span data-ttu-id="9f716-119">Значительные обновления могут быть сопряжены со сложностями.</span><span class="sxs-lookup"><span data-stu-id="9f716-119">Major updates can be inconvenient.</span></span> <span data-ttu-id="9f716-120">В модуле `Az` предусмотрен режим совместимости, который позволяет использовать существующие скрипты, пока вы выполняете обновление для поддержки нового синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="9f716-120">However, the `Az` module has a compatibility mode to help you use existing scripts while you work on updates to the new syntax.</span></span> <span data-ttu-id="9f716-121">Используйте командлет `Enable-AzureRmAlias` для активации режима совместимости `AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="9f716-121">Use the `Enable-AzureRmAlias` cmdlet to enable the `AzureRM` compatibility mode.</span></span> <span data-ttu-id="9f716-122">Этот командлет определяет имена командлетов `AzureRM` как псевдонимы для новых имен командлетов `Az`.</span><span class="sxs-lookup"><span data-stu-id="9f716-122">This cmdlet defines `AzureRM` cmdlet names as aliases for the new `Az` cmdlet names.</span></span>

<span data-ttu-id="9f716-123">Новые имена командлетов выбраны таким образом, чтобы их было легко запомнить.</span><span class="sxs-lookup"><span data-stu-id="9f716-123">The new cmdlet names have been designed to be easy to learn.</span></span> <span data-ttu-id="9f716-124">Вместо имен командлетов `AzureRm` или `Azure` используйте `Az`.</span><span class="sxs-lookup"><span data-stu-id="9f716-124">Instead of using `AzureRm` or `Azure` in cmdlet names, use `Az`.</span></span> <span data-ttu-id="9f716-125">Например, вместо старой команды `New-AzureRmVm` используется `New-AzVm`.</span><span class="sxs-lookup"><span data-stu-id="9f716-125">For example, the old command `New-AzureRmVm` has become `New-AzVm`.</span></span>

<span data-ttu-id="9f716-126">Полное описание процесса миграции см. в статье [Миграция с AzureRM на Az для Azure PowerShell](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="9f716-126">For a full description of the migration process, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

## <a name="the-future-of-support-for-azurerm"></a><span data-ttu-id="9f716-127">Поддержка AzureRM в будущем</span><span class="sxs-lookup"><span data-stu-id="9f716-127">The future of support for AzureRM</span></span>

<span data-ttu-id="9f716-128">После выпуска версии 1.0 `Az` в декабре 2018 г. в существующий модуль `AzureRM` больше не будут добавляться новые командлеты или возможности.</span><span class="sxs-lookup"><span data-stu-id="9f716-128">The existing `AzureRM` module will no longer receive new cmdlets or features when `Az` version 1.0 is released in December 2018.</span></span> <span data-ttu-id="9f716-129">Но `AzureRM` по-прежнему официально поддерживается и будет получать исправления ошибок.</span><span class="sxs-lookup"><span data-stu-id="9f716-129">However, `AzureRM` is still officially maintained and will get bug fixes.</span></span> <span data-ttu-id="9f716-130">Для поддержки новых служб и возможностей Azure рекомендуем перейти на использование модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="9f716-130">To keep up with the latest Azure services and features, you should switch to the `Az` module.</span></span>