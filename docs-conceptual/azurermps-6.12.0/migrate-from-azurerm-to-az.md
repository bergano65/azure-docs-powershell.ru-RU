---
title: Перенос скриптов Azure PowerShell с AzureRM на Az
description: Сведения о действиях и инструментах для переноса скриптов с модуля AzureRM на новый модуль Az.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/07/2018
ms.openlocfilehash: 0c73e7ac1d47a2a97b6136fa481d0adce8de33db
ms.sourcegitcommit: 4afdba3cd7e1d348876ce59f3503fdcd258f79ab
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/15/2018
ms.locfileid: "51574419"
---
# <a name="migrate-from-azurerm-to-azure-powershell-az"></a><span data-ttu-id="8db38-103">Миграция с AzureRM на Az для Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="8db38-103">Migrate from AzureRM to Azure PowerShell Az</span></span>

<span data-ttu-id="8db38-104">Модуль Az имеет равенство функций с AzureRM, но использует более короткие и единообразные имена командлетов.</span><span class="sxs-lookup"><span data-stu-id="8db38-104">The Az module has feature parity with AzureRM, but uses shorter and more consistent cmdlet names.</span></span>
<span data-ttu-id="8db38-105">Скрипты, написанные для командлетов AzureRM, не смогут автоматически работать с новым модулем.</span><span class="sxs-lookup"><span data-stu-id="8db38-105">Scripts written for the AzureRM cmdlets won't automatically work with the new module.</span></span> <span data-ttu-id="8db38-106">Для упрощения перехода модуль Az предлагает средства, позволяющие запускать существующие скрипты, которые используют AzureRM.</span><span class="sxs-lookup"><span data-stu-id="8db38-106">To make the transition easier, Az offers tools to allow you to run your existing scripts using AzureRM.</span></span> <span data-ttu-id="8db38-107">Миграция всегда сопряжена со сложностями, но эта статья поможет вам начать переход на новый модуль с новым набором команд.</span><span class="sxs-lookup"><span data-stu-id="8db38-107">No migration to a new command set is ever convenient, but this article will help you get started on transitioning to the new module.</span></span>

## <a name="ensure-your-existing-scripts-work-with-the-latest-azurerm-release"></a><span data-ttu-id="8db38-108">Убедитесь, что существующие скрипты работают с последним выпуском AzureRM</span><span class="sxs-lookup"><span data-stu-id="8db38-108">Ensure your existing scripts work with the latest AzureRM release</span></span>

<span data-ttu-id="8db38-109">Это самый важный шаг.</span><span class="sxs-lookup"><span data-stu-id="8db38-109">This is the most important step!</span></span> <span data-ttu-id="8db38-110">Запустите существующие скрипты и убедитесь, что они работают с _последним_ выпуском AzureRM (__6.12.0__).</span><span class="sxs-lookup"><span data-stu-id="8db38-110">Run your existing scripts, and make sure that they work with the _latest_ release of AzureRM (__6.12.0__).</span></span> <span data-ttu-id="8db38-111">Если скрипты не работают, ознакомьтесь с [руководством по миграции AzureRM](migration-guide.6.0.0.md).</span><span class="sxs-lookup"><span data-stu-id="8db38-111">If your scripts don't work, make sure to read the [AzureRM migration guide](migration-guide.6.0.0.md).</span></span>

## <a name="install-the-azure-powershell-az-module"></a><span data-ttu-id="8db38-112">Установка модуля Az для Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="8db38-112">Install the Azure PowerShell Az module</span></span>

<span data-ttu-id="8db38-113">Первый шаг — это установка модуля Az на вашей платформе.</span><span class="sxs-lookup"><span data-stu-id="8db38-113">The first step is to install the Az module on your platform.</span></span> <span data-ttu-id="8db38-114">Чтобы установить Az, нужно сначала удалить AzureRM.</span><span class="sxs-lookup"><span data-stu-id="8db38-114">To install Az, you need to uninstall AzureRM.</span></span>
<span data-ttu-id="8db38-115">В последующих разделах вы узнаете, как продолжить использовать существующие скрипты и активировать режим совместимости со старыми именами командлетов.</span><span class="sxs-lookup"><span data-stu-id="8db38-115">In the following steps, you'll learn how to keep running your existing scripts and enable compatibility for old cmdlet names.</span></span>

<span data-ttu-id="8db38-116">Чтобы установить модуль Az для Azure PowerShell, выполните следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="8db38-116">To install the Azure PowerShell Az module, follow these steps:</span></span>

* <span data-ttu-id="8db38-117">[Удалите модуль AzureRM](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="8db38-117">[Uninstall the AzureRM module](uninstall-azurerm-ps.md).</span></span> <span data-ttu-id="8db38-118">Убедитесь, что вы удалили _все_ установленные версии AzureRM, а не только самую последнюю.</span><span class="sxs-lookup"><span data-stu-id="8db38-118">Make sure that you remove _all_ installed versions of AzureRM, not just the most recent version.</span></span>
* <span data-ttu-id="8db38-119">[Установите модуль Az](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="8db38-119">[Install the Az module](install-az-ps.md)</span></span>

## <a name="a-namealiasesenable-azurerm-alias-mode"></a><span data-ttu-id="8db38-120"><a name="aliases"/>Активация режима псевдонимов AzureRM</span><span class="sxs-lookup"><span data-stu-id="8db38-120"><a name="aliases"/>Enable AzureRM alias mode</span></span>

<span data-ttu-id="8db38-121">После того как вы убедились, что ваши скрипты работают с последней версией AzureRM, и удалили AzureRM, можно активировать режим совместимости для модуля Az.</span><span class="sxs-lookup"><span data-stu-id="8db38-121">With AzureRM uninstalled and your scripts working with the latest AzureRM version, now is the time to enable the compatibility mode for the Az module.</span></span> <span data-ttu-id="8db38-122">Режим совместимости активируется следующей командой:</span><span class="sxs-lookup"><span data-stu-id="8db38-122">Compatibility is enabled with the command:</span></span>

```powershell-interactive
Enable-AzureRmAlias -Scope CurrentUser
```

<span data-ttu-id="8db38-123">Псевдонимы позволяют использовать старые имена командлетов с установленным модулем `Az`.</span><span class="sxs-lookup"><span data-stu-id="8db38-123">Aliases enable the ability to use old cmdlet names with the `Az` module installed.</span></span> <span data-ttu-id="8db38-124">Эти псевдонимы записываются в профиль пользователя для выбранной области видимости.</span><span class="sxs-lookup"><span data-stu-id="8db38-124">These aliases are written to the user profile for the selected scope.</span></span> <span data-ttu-id="8db38-125">Если профиль пользователя отсутствует, он будет создан.</span><span class="sxs-lookup"><span data-stu-id="8db38-125">If no user profile exists, one is created.</span></span>

> [!WARNING]
>
> <span data-ttu-id="8db38-126">Можно использовать другое значение параметра `-Scope` для этой команды, но делать это не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="8db38-126">You can use a different `-Scope` for this command, but it's not recommended!</span></span> <span data-ttu-id="8db38-127">Псевдонимы записываются в профиль пользователя для выбранной области видимости, поэтому используйте их для как можно более узкой области.</span><span class="sxs-lookup"><span data-stu-id="8db38-127">Aliases are written to the user profile for the selected scope, so keep enabling them to as limited a scope as possible.</span></span> <span data-ttu-id="8db38-128">Активация псевдонимов для всей системы может также вызвать проблемы у других пользователей, которые установили `AzureRM` в свою локальную область видимости.</span><span class="sxs-lookup"><span data-stu-id="8db38-128">Enabling aliases system-wide could also cause issues for other users which have `AzureRM` installed in their local scope.</span></span>

<span data-ttu-id="8db38-129">После активации режима псевдонимов запустите скрипты снова, чтобы убедиться, что они по-прежнему работают правильно.</span><span class="sxs-lookup"><span data-stu-id="8db38-129">Once the alias mode is enabled, run your scripts again to confirm that they still function as expected.</span></span> 

## <a name="change-module-imports-and-cmdlet-names"></a><span data-ttu-id="8db38-130">Изменение импорта модулей и имен командлетов</span><span class="sxs-lookup"><span data-stu-id="8db38-130">Change module imports and cmdlet names</span></span>

<span data-ttu-id="8db38-131">В общем случае имена модулей были изменены таким образом, чтобы заменить `AzureRM` и `Azure` на `Az`. То же относится и к командлетам.</span><span class="sxs-lookup"><span data-stu-id="8db38-131">In general, the module names have been changed so that `AzureRM` and `Azure` become `Az`, and the same for cmdlets.</span></span>
<span data-ttu-id="8db38-132">Например, модуль `AzureRM.Compute` был переименован в `Az.Compute`.</span><span class="sxs-lookup"><span data-stu-id="8db38-132">For example, the `AzureRM.Compute` module has been renamed to `Az.Compute`.</span></span> <span data-ttu-id="8db38-133">`New-AzureRmVM` теперь называется `New-AzVM`, а `Get-AzureStorageBlob` — `Get-AzStorageBlob`.</span><span class="sxs-lookup"><span data-stu-id="8db38-133">`New-AzureRmVM` has become `New-AzVM`, and `Get-AzureStorageBlob` is now `Get-AzStorageBlob`.</span></span>

<span data-ttu-id="8db38-134">Существует несколько исключений из этой схемы именования, о которых следует знать, прежде чем менять какие-либо имена:</span><span class="sxs-lookup"><span data-stu-id="8db38-134">There are exceptions to this naming change that you should be aware of before doing any renaming:</span></span>

| <span data-ttu-id="8db38-135">Модуль AzureRM</span><span class="sxs-lookup"><span data-stu-id="8db38-135">AzureRM module</span></span> | <span data-ttu-id="8db38-136">Модуль Az</span><span class="sxs-lookup"><span data-stu-id="8db38-136">Az module</span></span> |
|----------------|-----------|
| <span data-ttu-id="8db38-137">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="8db38-137">AzureRM.DataFactories</span></span> | <span data-ttu-id="8db38-138">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8db38-138">Az.DataFactory</span></span> |
| <span data-ttu-id="8db38-139">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="8db38-139">AzureRM.DataFactoryV2</span></span> | <span data-ttu-id="8db38-140">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8db38-140">Az.DataFactory</span></span> |
| <span data-ttu-id="8db38-141">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="8db38-141">AzureRM.RecoveryServices.Backup</span></span> | <span data-ttu-id="8db38-142">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8db38-142">Az.RecoveryServices</span></span> |
| <span data-ttu-id="8db38-143">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="8db38-143">AzureRM.RecoveryServices.SiteRecovery</span></span> | <span data-ttu-id="8db38-144">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8db38-144">Az.RecoveryServices</span></span> |

## <a name="summary"></a><span data-ttu-id="8db38-145">Сводка</span><span class="sxs-lookup"><span data-stu-id="8db38-145">Summary</span></span>

<span data-ttu-id="8db38-146">Выполнив эти шаги, можно обновить все существующие скрипты для использования с новым модулем.</span><span class="sxs-lookup"><span data-stu-id="8db38-146">By following these steps, you can update all of your existing scripts to use the new module.</span></span> <span data-ttu-id="8db38-147">Если у вас возникли вопросы по описанным действиям или же проблемы, которые затруднили миграцию, оставьте комментарии к этой статье, чтобы мы могли улучшить инструкции.</span><span class="sxs-lookup"><span data-stu-id="8db38-147">If you have any questions or problems with these steps that made your migration difficult, please comment on this article so that we can improve the instructions.</span></span>