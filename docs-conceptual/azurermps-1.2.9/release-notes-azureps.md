---
title: Журнал изменений Azure PowerShell | Документация Майкрософт
description: Это руководство содержит историю изменений Azure PowerShell, внесенных в новом выпуске.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: 91d97260568a36e1135196899503fb0c8e1c6731
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2018
ms.locfileid: "34853021"
---
# <a name="release-notes"></a><span data-ttu-id="f7af2-103">Заметки о выпуске</span><span class="sxs-lookup"><span data-stu-id="f7af2-103">Release notes</span></span>

<span data-ttu-id="f7af2-104">Здесь приведен список изменений, внесенных в Azure PowerShell в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="f7af2-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-129"></a><span data-ttu-id="f7af2-105">Версия 1.2.9</span><span class="sxs-lookup"><span data-stu-id="f7af2-105">Version 1.2.9</span></span>

<span data-ttu-id="f7af2-106">Изменения в этом выпуске</span><span class="sxs-lookup"><span data-stu-id="f7af2-106">Changes This Release</span></span>

* <span data-ttu-id="f7af2-107">Модуль AzureRm.AzureStackAdmin</span><span class="sxs-lookup"><span data-stu-id="f7af2-107">AzureRm.AzureStackAdmin Module</span></span>
    + <span data-ttu-id="f7af2-108">Изменения в командлете Add-AzureRmResourceProviderRegistration для поддержки разделения Azure Resource Manager для администратора и для клиента.</span><span class="sxs-lookup"><span data-stu-id="f7af2-108">Changes in the Add-AzureRmResourceProviderRegistration cmdlet for the support of Admin Azure resource manager and tenant azure resource manager split.</span></span> <span data-ttu-id="f7af2-109">Добавлен новый параметр -ResourceManagerType.</span><span class="sxs-lookup"><span data-stu-id="f7af2-109">A new parameter -ResourceManagerType has been added.</span></span>
    + <span data-ttu-id="f7af2-110">Удалены параметры -AdminUri, -ApiVersion, -SubscriptionId и -Token из каждого командлета.</span><span class="sxs-lookup"><span data-stu-id="f7af2-110">Removal of the parameters -AdminUri, -ApiVersion, -SubscriptionId and -Token from each cmdlets.</span></span> <span data-ttu-id="f7af2-111">Мы предупреждали о том, что поддержка этих параметров будет прекращена, и теперь они удалены.</span><span class="sxs-lookup"><span data-stu-id="f7af2-111">We have been printing warnings that these parameters will be deprecated and now they got removed.</span></span>
* <span data-ttu-id="f7af2-112">Модуль AzureStackStorage</span><span class="sxs-lookup"><span data-stu-id="f7af2-112">AzureStackStorage module</span></span>
    + <span data-ttu-id="f7af2-113">Добавлены новые командлеты для поддержки сценариев миграции контейнера.</span><span class="sxs-lookup"><span data-stu-id="f7af2-113">Added new cmdlets to support container migration scenarios.</span></span>
    + <span data-ttu-id="f7af2-114">Удалены командлеты, ссылающиеся на внутренние компоненты и базовые функции.</span><span class="sxs-lookup"><span data-stu-id="f7af2-114">Removed cmdlets referring to internal components and underlying features.</span></span>
* <span data-ttu-id="f7af2-115">AzureRM.BootStrapper</span><span class="sxs-lookup"><span data-stu-id="f7af2-115">AzureRM.BootStrapper</span></span>
    + <span data-ttu-id="f7af2-116">Создан модуль для управления версиями командлетов Azure PowerShell с помощью профилей версии.</span><span class="sxs-lookup"><span data-stu-id="f7af2-116">Created new module to manage versions of Azure PowerShell cmdlets through the use of version profiles</span></span>