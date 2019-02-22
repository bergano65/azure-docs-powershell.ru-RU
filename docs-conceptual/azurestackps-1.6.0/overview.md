---
title: Обзор модуля администрирования PowerShell для Azure Stack | Документация Майкрософт
description: Обзор модуля администрирования PowerShell для Azure Stack с инструкциями по установке и конфигурации.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: b0e85bec82b9b7c876b2bbf337b603c8d68cf6a3
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2019
ms.locfileid: "56153914"
---
# <a name="azure-stack-module-160"></a><span data-ttu-id="49365-103">Модуль Azure Stack 1.6.0</span><span class="sxs-lookup"><span data-stu-id="49365-103">Azure Stack Module 1.6.0</span></span>

## <a name="requirements"></a><span data-ttu-id="49365-104">Требования:</span><span class="sxs-lookup"><span data-stu-id="49365-104">Requirements:</span></span>
<span data-ttu-id="49365-105">Минимальная поддерживаемая версия Azure Stack — 1811.</span><span class="sxs-lookup"><span data-stu-id="49365-105">Minimum supported Azure Stack version is 1811.</span></span>

<span data-ttu-id="49365-106">Примечание. Если вы используете более раннюю версию, установите версию 1.6.0.</span><span class="sxs-lookup"><span data-stu-id="49365-106">Note: If you are using an earlier version install version 1.6.0</span></span>

## <a name="install"></a><span data-ttu-id="49365-107">Install</span><span class="sxs-lookup"><span data-stu-id="49365-107">Install</span></span>
```
# Remove previous versions of AzureStack and AzureRM modules
Uninstall-Module -Name AzureRM -Force
Uninstall-Module -Name Azure.Storage -Force
Uninstall-Module -Name AzureStack -Force
Get-Module -Name "Azs*" -ListAvailable | Uninstall-Module  -Force 
Get-Module -Name "AzureRm*" -ListAvailable | Uninstall-Module  -Force

# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.6.0
```

## <a name="release-notes"></a><span data-ttu-id="49365-108">Заметки о выпуске</span><span class="sxs-lookup"><span data-stu-id="49365-108">Release Notes</span></span>
* <span data-ttu-id="49365-109">Поддержка в обновлении 1811.</span><span class="sxs-lookup"><span data-stu-id="49365-109">Supported with 1811 update</span></span>
* <span data-ttu-id="49365-110">Модуль Azs.Compute.Admin</span><span class="sxs-lookup"><span data-stu-id="49365-110">Azs.Compute.Admin Module</span></span>
    * <span data-ttu-id="49365-111">Исправлен отсутствующий префикс Azs для объекта New-DataDiskObject, добавлен псевдоним с предупреждением о том, что в дальнейшем командлет будет отмечен как нерекомендуемый.</span><span class="sxs-lookup"><span data-stu-id="49365-111">Fixed missing Azs prefix for New-DataDiskObject and added alias with warning of future deprecation.</span></span>
* <span data-ttu-id="49365-112">Модуль Azs.Update.Admin:</span><span class="sxs-lookup"><span data-stu-id="49365-112">Azs.Update.Admin Module</span></span>
    * <span data-ttu-id="49365-113">Добавлено предупреждение с рекомендацией запускать Test-AzureStack перед установкой AzsUpdate.</span><span class="sxs-lookup"><span data-stu-id="49365-113">Added a warning to recommend running Test-AzureStack before Install-AzsUpdate</span></span>
* <span data-ttu-id="49365-114">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="49365-114">Azs.Fabric.Admin</span></span>
    * <span data-ttu-id="49365-115">Новый командлет (функции, поддерживаемые в Azure Stack 1811+):</span><span class="sxs-lookup"><span data-stu-id="49365-115">New cmdlet (The features are supported by Azure Stack 1811+)</span></span>
        * <span data-ttu-id="49365-116">Get-AzsDrive;</span><span class="sxs-lookup"><span data-stu-id="49365-116">Get-AzsDrive</span></span>
        * <span data-ttu-id="49365-117">Get-AzsVolume;</span><span class="sxs-lookup"><span data-stu-id="49365-117">Get-AzsVolume</span></span>
        * <span data-ttu-id="49365-118">Get-AzsStorageSubSystem.</span><span class="sxs-lookup"><span data-stu-id="49365-118">Get-AzsStorageSubSystem</span></span>
    * <span data-ttu-id="49365-119">Устаревшее</span><span class="sxs-lookup"><span data-stu-id="49365-119">Deprecation</span></span>
        * <span data-ttu-id="49365-120">Get-AzsInfrastructureVolume — это псевдоним для командлета Get-AzsVolume.</span><span class="sxs-lookup"><span data-stu-id="49365-120">Get-AzsInfrastructureVolume is an alias now to the cmdlet Get-AzsVolume</span></span>
* <span data-ttu-id="49365-121">Azs.InfrastructureInsights.Admin</span><span class="sxs-lookup"><span data-stu-id="49365-121">Azs.InfrastructureInsights.Admin</span></span>
    *  <span data-ttu-id="49365-122">Добавлен новый командлет Repair-AzsAlert.</span><span class="sxs-lookup"><span data-stu-id="49365-122">Added a new cmdlet Repair-AzsAlert</span></span>
* <span data-ttu-id="49365-123">Azs.Storage.Admin:</span><span class="sxs-lookup"><span data-stu-id="49365-123">Azs.Storage.Admin</span></span>
    * <span data-ttu-id="49365-124">Исправлена ошибка, возникающая, если значения квоты по умолчанию не используются.</span><span class="sxs-lookup"><span data-stu-id="49365-124">Bug fix where default quota values are not being used</span></span>
* <span data-ttu-id="49365-125">Модуль Azs.Subscriptions.Admin:</span><span class="sxs-lookup"><span data-stu-id="49365-125">Azs.Subscriptions.Admin Module</span></span>
    * <span data-ttu-id="49365-126">Исправлен отсутствующий префикс Azs для объекта New-AddonPlanDefinitionObject, добавлен псевдоним с предупреждением о том, что в дальнейшем командлет будет отмечен как нерекомендуемый.</span><span class="sxs-lookup"><span data-stu-id="49365-126">Fixed missing Azs prefix for New-AddonPlanDefinitionObject and added alias with warning of future deprecation.</span></span>
