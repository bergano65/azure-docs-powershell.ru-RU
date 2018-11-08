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
ms.openlocfilehash: fb892daeafb1365ea62324392ac806cf9f3d39cf
ms.sourcegitcommit: 06f9206e025afa7207d4657c8f57c94ddb74817a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2018
ms.locfileid: "51211984"
---
# <a name="azure-stack-module-130"></a><span data-ttu-id="aa903-103">Модуль Azure Stack 1.3.0</span><span class="sxs-lookup"><span data-stu-id="aa903-103">Azure Stack Module 1.3.0</span></span>

## <a name="requirements"></a><span data-ttu-id="aa903-104">Требования:</span><span class="sxs-lookup"><span data-stu-id="aa903-104">Requirements:</span></span>
<span data-ttu-id="aa903-105">Минимальная поддерживаемая версия Azure Stack — 1804.</span><span class="sxs-lookup"><span data-stu-id="aa903-105">Minimum supported Azure Stack version is 1804.</span></span>

<span data-ttu-id="aa903-106">Примечание. Если вы используете более раннюю версию, установите версию 1.2.11.</span><span class="sxs-lookup"><span data-stu-id="aa903-106">Note: If you are using an earlier version install version 1.2.11</span></span>

## <a name="known-issues"></a><span data-ttu-id="aa903-107">Известные проблемы:</span><span class="sxs-lookup"><span data-stu-id="aa903-107">Known issues:</span></span>

- <span data-ttu-id="aa903-108">Для закрытия оповещения требуется Azure Stack версии 1803.</span><span class="sxs-lookup"><span data-stu-id="aa903-108">Close Alert requires Azure Stack version 1803</span></span>
- <span data-ttu-id="aa903-109">Для некоторых командлетов хранилища требуется версия Azure Stack 1804.</span><span class="sxs-lookup"><span data-stu-id="aa903-109">Some Storage cmdlets do require Azure Stack version 1804</span></span>
- <span data-ttu-id="aa903-110">New-AzsOffer не позволяет создать общедоступное предложение.</span><span class="sxs-lookup"><span data-stu-id="aa903-110">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="aa903-111">После него нужно вызвать командлет Set-AzsOffer, чтобы изменить состояние.</span><span class="sxs-lookup"><span data-stu-id="aa903-111">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="aa903-112">Нельзя удалить пул IP-адресов без повторного развертывания.</span><span class="sxs-lookup"><span data-stu-id="aa903-112">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="breaking-changes"></a><span data-ttu-id="aa903-113">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="aa903-113">Breaking Changes</span></span>
<span data-ttu-id="aa903-114">Все критические изменения при миграции с 1.2.11 описаны по адресу https://aka.ms/azspowershellmigration</span><span class="sxs-lookup"><span data-stu-id="aa903-114">All breaking changes migrating from 1.2.11 are documented here https://aka.ms/azspowershellmigration</span></span>

## <a name="install"></a><span data-ttu-id="aa903-115">Install</span><span class="sxs-lookup"><span data-stu-id="aa903-115">Install</span></span>
```
# Remove previous Versions
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Uninstall-Module -Name AzureStack -Force 


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2017-03-09-profile -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.3.0
```
## <a name="content"></a><span data-ttu-id="aa903-116">Содержимое:</span><span class="sxs-lookup"><span data-stu-id="aa903-116">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="aa903-117">Мост Azure</span><span class="sxs-lookup"><span data-stu-id="aa903-117">Azure Bridge</span></span>
<span data-ttu-id="aa903-118">Предварительная версия модуля для администраторов компонента Azure Stack "Мост Azure", которая позволяет объединять образы из Azure.</span><span class="sxs-lookup"><span data-stu-id="aa903-118">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="aa903-119">Azure Backup</span><span class="sxs-lookup"><span data-stu-id="aa903-119">Backup</span></span>
<span data-ttu-id="aa903-120">Предварительная версия модуля для администраторов службы Backup, которая позволяет администраторам:</span><span class="sxs-lookup"><span data-stu-id="aa903-120">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="aa903-121">настраивать расположение для хранения резервных копий;</span><span class="sxs-lookup"><span data-stu-id="aa903-121">Configure where backups are stored</span></span>
- <span data-ttu-id="aa903-122">выполнять резервное копирование;</span><span class="sxs-lookup"><span data-stu-id="aa903-122">Perform backups</span></span>
- <span data-ttu-id="aa903-123">выводить список созданных резервных копий и выполнять на их основе восстановление.</span><span class="sxs-lookup"><span data-stu-id="aa903-123">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="aa903-124">Приложения для коммерции</span><span class="sxs-lookup"><span data-stu-id="aa903-124">Commerce</span></span>
<span data-ttu-id="aa903-125">Предварительная версия модуля для администраторов средства коммерции в Azure Stack, которая позволяет просматривать статистические сведения об использовании данных для всей системы Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="aa903-125">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="aa903-126">Службы вычислений</span><span class="sxs-lookup"><span data-stu-id="aa903-126">Compute</span></span>
<span data-ttu-id="aa903-127">Предварительная версия модуля для администраторов вычислительных ресурсов в Azure Stack, которая предоставляет функции управления квотами вычислительных ресурсов, образами платформ и расширениями виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="aa903-127">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="aa903-128">Fabric</span><span class="sxs-lookup"><span data-stu-id="aa903-128">Fabric</span></span>
<span data-ttu-id="aa903-129">Предварительная версия модуля для администраторов Fabric в Azure Stack, которая позволяет администраторам просматривать компоненты инфраструктуры и управлять ими, выполняя следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="aa903-129">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="aa903-130">остановка, запуск и завершение работы для узлов единиц масштабирования;</span><span class="sxs-lookup"><span data-stu-id="aa903-130">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="aa903-131">очистка и возобновление работы узлов единиц масштабирования для связанных действий FRU;</span><span class="sxs-lookup"><span data-stu-id="aa903-131">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="aa903-132">исправление узлов единиц масштабирования;</span><span class="sxs-lookup"><span data-stu-id="aa903-132">Repair of scale unit nodes</span></span>
- <span data-ttu-id="aa903-133">перезапуск роли инфраструктуры;</span><span class="sxs-lookup"><span data-stu-id="aa903-133">Restart of Infrastructure role</span></span>
- <span data-ttu-id="aa903-134">остановка, запуск и завершение работы экземпляров роли инфраструктуры;</span><span class="sxs-lookup"><span data-stu-id="aa903-134">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="aa903-135">создание пулов IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="aa903-135">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="aa903-136">Коллекция</span><span class="sxs-lookup"><span data-stu-id="aa903-136">Gallery</span></span>
<span data-ttu-id="aa903-137">Предварительная версия модуля для администраторов коллекций Azure Stack, которая предоставляет функции для управления элементами коллекции в Azure Stack Marketplace.</span><span class="sxs-lookup"><span data-stu-id="aa903-137">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="aa903-138">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="aa903-138">Infrastructure Insights</span></span>
<span data-ttu-id="aa903-139">Предварительная версия модуля для администраторов Infrastructure Insights, которая позволяет администраторам:</span><span class="sxs-lookup"><span data-stu-id="aa903-139">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="aa903-140">просматривать сведения о работоспособности ресурсов отметок в Azure Stack;</span><span class="sxs-lookup"><span data-stu-id="aa903-140">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="aa903-141">просматривать оповещения и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="aa903-141">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="aa903-142">Хранилище ключей</span><span class="sxs-lookup"><span data-stu-id="aa903-142">KeyVault</span></span>
<span data-ttu-id="aa903-143">Предварительная версия модуля для администраторов Key Vault в Azure Stack, которая позволяет администратору просматривать квоты Key Vault.</span><span class="sxs-lookup"><span data-stu-id="aa903-143">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="aa903-144">Сеть</span><span class="sxs-lookup"><span data-stu-id="aa903-144">Network</span></span>
<span data-ttu-id="aa903-145">Предварительная версия модуля для администраторов сетей, которая позволяет:</span><span class="sxs-lookup"><span data-stu-id="aa903-145">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="aa903-146">управлять квотами сети;</span><span class="sxs-lookup"><span data-stu-id="aa903-146">Management of network quotas</span></span>
- <span data-ttu-id="aa903-147">просматривать выделенные сетевые ресурсы, например общедоступные IP-адреса, виртуальные сети, подсистемы балансировки нагрузки;</span><span class="sxs-lookup"><span data-stu-id="aa903-147">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="aa903-148">использовать командлет для отображения общих сведений об администраторе.</span><span class="sxs-lookup"><span data-stu-id="aa903-148">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="aa903-149">Хранилище</span><span class="sxs-lookup"><span data-stu-id="aa903-149">Storage</span></span>
<span data-ttu-id="aa903-150">Предварительная версия модуля для администраторов хранилища Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="aa903-150">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="aa903-151">В этом выпуске мы предоставляем следующие функции:</span><span class="sxs-lookup"><span data-stu-id="aa903-151">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="aa903-152">управление квотами хранилища;</span><span class="sxs-lookup"><span data-stu-id="aa903-152">Manage storage quotas</span></span>
- <span data-ttu-id="aa903-153">сборка мусора для удаленных ресурсов хранилища;</span><span class="sxs-lookup"><span data-stu-id="aa903-153">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="aa903-154">восстановление удаленных учетных записей хранения;</span><span class="sxs-lookup"><span data-stu-id="aa903-154">Restore deleted storage accounts</span></span>
- <span data-ttu-id="aa903-155">перенос контейнеров из одной общей папки в другую;</span><span class="sxs-lookup"><span data-stu-id="aa903-155">Migrate containers from one share to another</span></span>
- <span data-ttu-id="aa903-156">просмотр сведений об отдельных компонентах хранилища;</span><span class="sxs-lookup"><span data-stu-id="aa903-156">View information about the individual storage components</span></span>
- <span data-ttu-id="aa903-157">просмотр сведений об использовании и производительности.</span><span class="sxs-lookup"><span data-stu-id="aa903-157">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="aa903-158">Администратор подписки</span><span class="sxs-lookup"><span data-stu-id="aa903-158">Subscription Admin</span></span>
<span data-ttu-id="aa903-159">Предварительная версия модуля для администраторов подписки Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="aa903-159">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="aa903-160">Этот модуль предоставляет следующие функции для администраторов:</span><span class="sxs-lookup"><span data-stu-id="aa903-160">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="aa903-161">управление планами и предложениями;</span><span class="sxs-lookup"><span data-stu-id="aa903-161">Manage plans and offers</span></span>
- <span data-ttu-id="aa903-162">просмотр сведений об использовании и производительности.</span><span class="sxs-lookup"><span data-stu-id="aa903-162">View usage and performance information</span></span>
- <span data-ttu-id="aa903-163">Управление RBAC</span><span class="sxs-lookup"><span data-stu-id="aa903-163">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="aa903-164">Подписка</span><span class="sxs-lookup"><span data-stu-id="aa903-164">Subscription</span></span>
<span data-ttu-id="aa903-165">Предварительная версия модуля подписки Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="aa903-165">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="aa903-166">Этот модуль предоставляет следующие функции для пользователей:</span><span class="sxs-lookup"><span data-stu-id="aa903-166">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="aa903-167">создание, удаление и изменение подписок.</span><span class="sxs-lookup"><span data-stu-id="aa903-167">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="aa903-168">Блокировка изменений</span><span class="sxs-lookup"><span data-stu-id="aa903-168">Update</span></span>
<span data-ttu-id="aa903-169">Предварительная версия модуля для администраторов обновлений Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="aa903-169">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="aa903-170">В этом модуле администраторы могут:</span><span class="sxs-lookup"><span data-stu-id="aa903-170">In this module administrators can:</span></span>
- <span data-ttu-id="aa903-171">выводить список и устанавливать доступные обновления;</span><span class="sxs-lookup"><span data-stu-id="aa903-171">List and install available updates</span></span>
- <span data-ttu-id="aa903-172">возобновлять прерванную установку обновлений;</span><span class="sxs-lookup"><span data-stu-id="aa903-172">Resume interrupted updates</span></span>
- <span data-ttu-id="aa903-173">просматривать установленные обновления.</span><span class="sxs-lookup"><span data-stu-id="aa903-173">View installed updates</span></span>
