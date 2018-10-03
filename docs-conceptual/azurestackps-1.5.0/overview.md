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
ms.openlocfilehash: 18861f0e5232e0b505767aa9609099afe88f9477
ms.sourcegitcommit: 19dffee617477001f98d43e39a50ce1fad087b74
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2018
ms.locfileid: "47178635"
---
# <a name="azure-stack-module-150"></a><span data-ttu-id="797a4-103">Модуль Azure Stack версии 1.5.0</span><span class="sxs-lookup"><span data-stu-id="797a4-103">Azure Stack Module 1.5.0</span></span>

## <a name="requirements"></a><span data-ttu-id="797a4-104">Требования:</span><span class="sxs-lookup"><span data-stu-id="797a4-104">Requirements:</span></span>
<span data-ttu-id="797a4-105">Минимальная поддерживаемая версия Azure Stack — 1808.</span><span class="sxs-lookup"><span data-stu-id="797a4-105">Minimum supported Azure Stack version is 1808.</span></span>

<span data-ttu-id="797a4-106">Примечание. Если вы используете более раннюю версию, установите версию 1.4.0.</span><span class="sxs-lookup"><span data-stu-id="797a4-106">Note: If you are using an earlier version install version 1.4.0</span></span>

## <a name="known-issues"></a><span data-ttu-id="797a4-107">Известные проблемы:</span><span class="sxs-lookup"><span data-stu-id="797a4-107">Known issues:</span></span>

- <span data-ttu-id="797a4-108">New-AzsOffer не позволяет создать общедоступное предложение.</span><span class="sxs-lookup"><span data-stu-id="797a4-108">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="797a4-109">После него нужно вызвать командлет Set-AzsOffer, чтобы изменить состояние.</span><span class="sxs-lookup"><span data-stu-id="797a4-109">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="797a4-110">Нельзя удалить пул IP-адресов без повторного развертывания.</span><span class="sxs-lookup"><span data-stu-id="797a4-110">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="install"></a><span data-ttu-id="797a4-111">Install</span><span class="sxs-lookup"><span data-stu-id="797a4-111">Install</span></span>
```
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.5.0
```

##<a name="release-notes"></a><span data-ttu-id="797a4-112">Заметки о выпуске</span><span class="sxs-lookup"><span data-stu-id="797a4-112">Release Notes</span></span>
* <span data-ttu-id="797a4-113">Все модули администрирования Azure Stack обновлены и зависят от модуля AzureRm.Profile такой же или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="797a4-113">All the Azure Stack Admin modules are updated for greater than or equal to dependency on the AzureRm.Profile module</span></span>
* <span data-ttu-id="797a4-114">Добавлена поддержка обработки имен вложенных ресурсов во всех модулях.</span><span class="sxs-lookup"><span data-stu-id="797a4-114">Support for handling nested resource names in all the modules</span></span>
* <span data-ttu-id="797a4-115">Исправление ошибки во всех модулях, когда параметру ErrorActionPreference принудительно присваивалось значение Stop.</span><span class="sxs-lookup"><span data-stu-id="797a4-115">Bug fix in all the modules where ErrorActionPreference is being overridden to be Stop</span></span>
* <span data-ttu-id="797a4-116">Модуль Azs.Compute.Admin</span><span class="sxs-lookup"><span data-stu-id="797a4-116">Azs.Compute.Admin Module</span></span>
    * <span data-ttu-id="797a4-117">Добавлены новые свойства квот для поддержки управляемых дисков.</span><span class="sxs-lookup"><span data-stu-id="797a4-117">New quota properties added for the support of manged disk</span></span>
    * <span data-ttu-id="797a4-118">Добавлены командлеты для переноса дисков.</span><span class="sxs-lookup"><span data-stu-id="797a4-118">Addition of disk migration related cmdlets</span></span>
    * <span data-ttu-id="797a4-119">Дополнительные свойства для объектов образа платформы и расширений виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="797a4-119">Additional properties in the Platform Image and VM extesnion objects</span></span>
* <span data-ttu-id="797a4-120">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="797a4-120">Azs.Fabric.Admin</span></span> 
    * <span data-ttu-id="797a4-121">Новый командлет для добавления узла единицы масштабирования.</span><span class="sxs-lookup"><span data-stu-id="797a4-121">New cmdlet for adding scale unit node</span></span>
* <span data-ttu-id="797a4-122">Azs.Backup.Admin</span><span class="sxs-lookup"><span data-stu-id="797a4-122">Azs.Backup.Admin</span></span>
    * <span data-ttu-id="797a4-123">Set-AzsBackupShare — это псевдоним командлета Set-AzsBackupConfiguration.</span><span class="sxs-lookup"><span data-stu-id="797a4-123">Set-AzsBackupShare is an alias now to the cmdlet Set-AzsBackupConfiguration</span></span>
    * <span data-ttu-id="797a4-124">Get-AzsBackupLocation — это псевдоним командлета Get-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="797a4-124">Get-AzsBackupLocation is an alias now to the cmdlet Get-AzsBackupConfiguration</span></span>
    * <span data-ttu-id="797a4-125">В Set-AzsBackupConfiguration параметр BackupShare — это псевдоним для параметра path.</span><span class="sxs-lookup"><span data-stu-id="797a4-125">Set-AzsBackupConfiguration, the parameter BackupShare is an alias now for the parameter path</span></span>
* <span data-ttu-id="797a4-126">Azs.Subscriptions</span><span class="sxs-lookup"><span data-stu-id="797a4-126">Azs.Subscriptions</span></span>
    * <span data-ttu-id="797a4-127">В Get-AzsDelegatedProviderOffer параметр OfferName — это псевдоним для Offer.</span><span class="sxs-lookup"><span data-stu-id="797a4-127">Get-AzsDelegatedProviderOffer, the parameter OfferName is now an alias for Offer</span></span>
* <span data-ttu-id="797a4-128">Azs.Subscriptions.Admin</span><span class="sxs-lookup"><span data-stu-id="797a4-128">Azs.Subscriptions.Admin</span></span>
    * <span data-ttu-id="797a4-129">В Get-AzsDelegatedProviderOffer параметр OfferName — это псевдоним для Offer.</span><span class="sxs-lookup"><span data-stu-id="797a4-129">Get-AzsDelegatedProviderOffer, the parameter OfferName is now an alias for Offer</span></span>

## <a name="content"></a><span data-ttu-id="797a4-130">Содержимое:</span><span class="sxs-lookup"><span data-stu-id="797a4-130">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="797a4-131">Мост Azure</span><span class="sxs-lookup"><span data-stu-id="797a4-131">Azure Bridge</span></span>
<span data-ttu-id="797a4-132">Предварительная версия модуля для администраторов компонента Azure Stack "Мост Azure", которая позволяет объединять образы из Azure.</span><span class="sxs-lookup"><span data-stu-id="797a4-132">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="797a4-133">Azure Backup</span><span class="sxs-lookup"><span data-stu-id="797a4-133">Backup</span></span>
<span data-ttu-id="797a4-134">Предварительная версия модуля для администраторов службы Backup, которая позволяет администраторам:</span><span class="sxs-lookup"><span data-stu-id="797a4-134">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="797a4-135">настраивать расположение для хранения резервных копий;</span><span class="sxs-lookup"><span data-stu-id="797a4-135">Configure where backups are stored</span></span>
- <span data-ttu-id="797a4-136">выполнять резервное копирование;</span><span class="sxs-lookup"><span data-stu-id="797a4-136">Perform backups</span></span>
- <span data-ttu-id="797a4-137">выводить список созданных резервных копий и выполнять на их основе восстановление.</span><span class="sxs-lookup"><span data-stu-id="797a4-137">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="797a4-138">Приложения для коммерции</span><span class="sxs-lookup"><span data-stu-id="797a4-138">Commerce</span></span>
<span data-ttu-id="797a4-139">Предварительная версия модуля для администраторов средства коммерции в Azure Stack, которая позволяет просматривать статистические сведения об использовании данных для всей системы Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="797a4-139">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="797a4-140">Службы вычислений</span><span class="sxs-lookup"><span data-stu-id="797a4-140">Compute</span></span>
<span data-ttu-id="797a4-141">Предварительная версия модуля для администраторов вычислительных ресурсов в Azure Stack, которая предоставляет функции управления квотами вычислительных ресурсов, образами платформ, управляемыми дисками и расширениями виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="797a4-141">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, managed disks and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="797a4-142">Fabric</span><span class="sxs-lookup"><span data-stu-id="797a4-142">Fabric</span></span>
<span data-ttu-id="797a4-143">Предварительная версия модуля для администраторов Fabric в Azure Stack, которая позволяет администраторам просматривать компоненты инфраструктуры и управлять ими, выполняя следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="797a4-143">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="797a4-144">остановка, запуск и завершение работы для узлов единиц масштабирования;</span><span class="sxs-lookup"><span data-stu-id="797a4-144">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="797a4-145">очистка и возобновление работы узлов единиц масштабирования для связанных действий FRU;</span><span class="sxs-lookup"><span data-stu-id="797a4-145">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="797a4-146">исправление узлов единиц масштабирования;</span><span class="sxs-lookup"><span data-stu-id="797a4-146">Repair of scale unit nodes</span></span>
- <span data-ttu-id="797a4-147">перезапуск роли инфраструктуры;</span><span class="sxs-lookup"><span data-stu-id="797a4-147">Restart of Infrastructure role</span></span>
- <span data-ttu-id="797a4-148">остановка, запуск и завершение работы экземпляров роли инфраструктуры;</span><span class="sxs-lookup"><span data-stu-id="797a4-148">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="797a4-149">создание пулов IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="797a4-149">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="797a4-150">Коллекция</span><span class="sxs-lookup"><span data-stu-id="797a4-150">Gallery</span></span>
<span data-ttu-id="797a4-151">Предварительная версия модуля для администраторов коллекций Azure Stack, которая предоставляет функции для управления элементами коллекции в Azure Stack Marketplace.</span><span class="sxs-lookup"><span data-stu-id="797a4-151">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="797a4-152">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="797a4-152">Infrastructure Insights</span></span>
<span data-ttu-id="797a4-153">Предварительная версия модуля для администраторов Infrastructure Insights, которая позволяет администраторам:</span><span class="sxs-lookup"><span data-stu-id="797a4-153">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="797a4-154">просматривать сведения о работоспособности ресурсов отметок в Azure Stack;</span><span class="sxs-lookup"><span data-stu-id="797a4-154">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="797a4-155">просматривать оповещения и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="797a4-155">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="797a4-156">Хранилище ключей</span><span class="sxs-lookup"><span data-stu-id="797a4-156">KeyVault</span></span>
<span data-ttu-id="797a4-157">Предварительная версия модуля для администраторов Key Vault в Azure Stack, которая позволяет администратору просматривать квоты Key Vault.</span><span class="sxs-lookup"><span data-stu-id="797a4-157">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="797a4-158">Сеть</span><span class="sxs-lookup"><span data-stu-id="797a4-158">Network</span></span>
<span data-ttu-id="797a4-159">Предварительная версия модуля для администраторов сетей, которая позволяет:</span><span class="sxs-lookup"><span data-stu-id="797a4-159">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="797a4-160">управлять квотами сети;</span><span class="sxs-lookup"><span data-stu-id="797a4-160">Management of network quotas</span></span>
- <span data-ttu-id="797a4-161">просматривать выделенные сетевые ресурсы, например общедоступные IP-адреса, виртуальные сети, подсистемы балансировки нагрузки;</span><span class="sxs-lookup"><span data-stu-id="797a4-161">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="797a4-162">использовать командлет для отображения общих сведений об администраторе.</span><span class="sxs-lookup"><span data-stu-id="797a4-162">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="797a4-163">служба хранилища.</span><span class="sxs-lookup"><span data-stu-id="797a4-163">Storage</span></span>
<span data-ttu-id="797a4-164">Предварительная версия модуля для администраторов хранилища Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="797a4-164">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="797a4-165">В этом выпуске мы предоставляем следующие функции:</span><span class="sxs-lookup"><span data-stu-id="797a4-165">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="797a4-166">управление квотами хранилища;</span><span class="sxs-lookup"><span data-stu-id="797a4-166">Manage storage quotas</span></span>
- <span data-ttu-id="797a4-167">сборка мусора для удаленных ресурсов хранилища;</span><span class="sxs-lookup"><span data-stu-id="797a4-167">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="797a4-168">восстановление удаленных учетных записей хранения;</span><span class="sxs-lookup"><span data-stu-id="797a4-168">Restore deleted storage accounts</span></span>
- <span data-ttu-id="797a4-169">перенос контейнеров из одной общей папки в другую;</span><span class="sxs-lookup"><span data-stu-id="797a4-169">Migrate containers from one share to another</span></span>
- <span data-ttu-id="797a4-170">просмотр сведений об отдельных компонентах хранилища;</span><span class="sxs-lookup"><span data-stu-id="797a4-170">View information about the individual storage components</span></span>
- <span data-ttu-id="797a4-171">просмотр сведений об использовании и производительности.</span><span class="sxs-lookup"><span data-stu-id="797a4-171">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="797a4-172">Администратор подписки</span><span class="sxs-lookup"><span data-stu-id="797a4-172">Subscription Admin</span></span>
<span data-ttu-id="797a4-173">Предварительная версия модуля для администраторов подписки Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="797a4-173">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="797a4-174">Этот модуль предоставляет следующие функции для администраторов:</span><span class="sxs-lookup"><span data-stu-id="797a4-174">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="797a4-175">управление планами и предложениями;</span><span class="sxs-lookup"><span data-stu-id="797a4-175">Manage plans and offers</span></span>
- <span data-ttu-id="797a4-176">просмотр сведений об использовании и производительности.</span><span class="sxs-lookup"><span data-stu-id="797a4-176">View usage and performance information</span></span>
- <span data-ttu-id="797a4-177">Управление RBAC</span><span class="sxs-lookup"><span data-stu-id="797a4-177">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="797a4-178">Подписка</span><span class="sxs-lookup"><span data-stu-id="797a4-178">Subscription</span></span>
<span data-ttu-id="797a4-179">Предварительная версия модуля подписки Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="797a4-179">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="797a4-180">Этот модуль предоставляет следующие функции для пользователей:</span><span class="sxs-lookup"><span data-stu-id="797a4-180">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="797a4-181">создание, удаление и изменение подписок.</span><span class="sxs-lookup"><span data-stu-id="797a4-181">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="797a4-182">Блокировка изменений</span><span class="sxs-lookup"><span data-stu-id="797a4-182">Update</span></span>
<span data-ttu-id="797a4-183">Предварительная версия модуля для администраторов обновлений Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="797a4-183">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="797a4-184">В этом модуле администраторы могут:</span><span class="sxs-lookup"><span data-stu-id="797a4-184">In this module administrators can:</span></span>
- <span data-ttu-id="797a4-185">выводить список и устанавливать доступные обновления;</span><span class="sxs-lookup"><span data-stu-id="797a4-185">List and install available updates</span></span>
- <span data-ttu-id="797a4-186">возобновлять прерванную установку обновлений;</span><span class="sxs-lookup"><span data-stu-id="797a4-186">Resume interrupted updates</span></span>
- <span data-ttu-id="797a4-187">просматривать установленные обновления.</span><span class="sxs-lookup"><span data-stu-id="797a4-187">View installed updates</span></span>
