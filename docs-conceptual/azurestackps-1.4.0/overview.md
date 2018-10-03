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
ms.openlocfilehash: 72d147f5bc9c882083dda6b33b1c89663fd2eb34
ms.sourcegitcommit: 19dffee617477001f98d43e39a50ce1fad087b74
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2018
ms.locfileid: "47178805"
---
# <a name="azure-stack-module-140"></a><span data-ttu-id="55809-103">Модуль Azure Stack 1.4.0</span><span class="sxs-lookup"><span data-stu-id="55809-103">Azure Stack Module 1.4.0</span></span>

## <a name="requirements"></a><span data-ttu-id="55809-104">Требования:</span><span class="sxs-lookup"><span data-stu-id="55809-104">Requirements:</span></span>
<span data-ttu-id="55809-105">Минимальная поддерживаемая версия Azure Stack — 1804.</span><span class="sxs-lookup"><span data-stu-id="55809-105">Minimum supported Azure Stack version is 1804.</span></span>

<span data-ttu-id="55809-106">Примечание. Если вы используете более раннюю версию, установите версию 1.2.11.</span><span class="sxs-lookup"><span data-stu-id="55809-106">Note: If you are using an earlier version install version 1.2.11</span></span>

## <a name="known-issues"></a><span data-ttu-id="55809-107">Известные проблемы:</span><span class="sxs-lookup"><span data-stu-id="55809-107">Known issues:</span></span>

- <span data-ttu-id="55809-108">Для закрытия оповещения требуется Azure Stack версии 1803.</span><span class="sxs-lookup"><span data-stu-id="55809-108">Close Alert requires Azure Stack version 1803</span></span>
- <span data-ttu-id="55809-109">New-AzsOffer не позволяет создать общедоступное предложение.</span><span class="sxs-lookup"><span data-stu-id="55809-109">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="55809-110">После него нужно вызвать командлет Set-AzsOffer, чтобы изменить состояние.</span><span class="sxs-lookup"><span data-stu-id="55809-110">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="55809-111">Нельзя удалить пул IP-адресов без повторного развертывания.</span><span class="sxs-lookup"><span data-stu-id="55809-111">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="breaking-changes"></a><span data-ttu-id="55809-112">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="55809-112">Breaking Changes</span></span>
<span data-ttu-id="55809-113">Критических изменений по сравнению с версией 1.3.0 нет.</span><span class="sxs-lookup"><span data-stu-id="55809-113">There are no breaking changes from the version 1.3.0.</span></span> <span data-ttu-id="55809-114">Все критические изменения при миграции с 1.2.11 описаны по адресу https://aka.ms/azspowershellmigration</span><span class="sxs-lookup"><span data-stu-id="55809-114">All breaking changes migrating from 1.2.11 are documented here https://aka.ms/azspowershellmigration</span></span>

## <a name="install"></a><span data-ttu-id="55809-115">Install</span><span class="sxs-lookup"><span data-stu-id="55809-115">Install</span></span>
```
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2017-03-09-profile -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.4.0
```
## <a name="release-notes"></a><span data-ttu-id="55809-116">Заметки о выпуске</span><span class="sxs-lookup"><span data-stu-id="55809-116">Release Notes</span></span>
    * <span data-ttu-id="55809-117">В версии Azurestack 1.4.0 нет критических изменений по сравнению с предыдущим выпуском 1.3.0.</span><span class="sxs-lookup"><span data-stu-id="55809-117">Azurestack 1.4.0 version has no breaking changes from the previous release 1.3.0</span></span>
    * <span data-ttu-id="55809-118">Azs.AzureBridge.Admin</span><span class="sxs-lookup"><span data-stu-id="55809-118">Azs.AzureBridge.Admin</span></span>
        - <span data-ttu-id="55809-119">Исправлена ошибка, из-за которой в результатах с разбивкой на страницы возвращалась всего одна страница.</span><span class="sxs-lookup"><span data-stu-id="55809-119">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="55809-120">Azs.Backup.Admin</span><span class="sxs-lookup"><span data-stu-id="55809-120">Azs.Backup.Admin</span></span>
        - <span data-ttu-id="55809-121">Добавлены новые параметры BackupFrequencyInHours, IsBackupSchedulerEnabled, BackupRetentionPeriodInDays для командлета Set-AzsBackupShare.</span><span class="sxs-lookup"><span data-stu-id="55809-121">Added new parameters BackupFrequencyInHours, IsBackupSchedulerEnabled, BackupRetentionPeriodInDays in cmdlet Set-AzsBackupShare</span></span>
        - <span data-ttu-id="55809-122">Добавлен командлет New-EncyptionKeyBase64, упрощающий создание ключа шифрования.</span><span class="sxs-lookup"><span data-stu-id="55809-122">Added a cmdlet New-EncyptionKeyBase64 to facilitate creating encryption key</span></span>
        - <span data-ttu-id="55809-123">Исправлена ошибка, из-за которой в результатах с разбивкой на страницы возвращалась всего одна страница.</span><span class="sxs-lookup"><span data-stu-id="55809-123">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="55809-124">Azs.Commerce.Admin</span><span class="sxs-lookup"><span data-stu-id="55809-124">Azs.Commerce.Admin</span></span>
        - <span data-ttu-id="55809-125">Исправлена ошибка, из-за которой в результатах с разбивкой на страницы возвращалась всего одна страница.</span><span class="sxs-lookup"><span data-stu-id="55809-125">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="55809-126">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="55809-126">Azs.Fabric.Admin</span></span>
        - <span data-ttu-id="55809-127">Исправлена ошибка, из-за которой в результатах с разбивкой на страницы возвращалась всего одна страница.</span><span class="sxs-lookup"><span data-stu-id="55809-127">Fix for the bug that returned only a single page in paginated results</span></span>
        - <span data-ttu-id="55809-128">Добавлен командлет Add-AzsScaleUnitNode, позволяющий администратору добавлять к метке azurestack новые узлы единиц масштабирования.</span><span class="sxs-lookup"><span data-stu-id="55809-128">Added a cmdlet Add-AzsScaleUnitNode to enable admin to add new scale unit nodes to the azurestack stamp</span></span>
        - <span data-ttu-id="55809-129">Добавлен командлет New-AzsScaleUnitNodeObject, упрощающий создание объектов параметров единиц масштабирования.</span><span class="sxs-lookup"><span data-stu-id="55809-129">Added cmdlet and New-AzsScaleUnitNodeObject to facilitate the creation scale unit parameter objects</span></span>
    * <span data-ttu-id="55809-130">Azs.Gallery.Admin</span><span class="sxs-lookup"><span data-stu-id="55809-130">Azs.Gallery.Admin</span></span>
        - <span data-ttu-id="55809-131">Исправлена ошибка, из-за которой в результатах с разбивкой на страницы возвращалась всего одна страница.</span><span class="sxs-lookup"><span data-stu-id="55809-131">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="55809-132">Azs.InfrastructureInsights.Admin</span><span class="sxs-lookup"><span data-stu-id="55809-132">Azs.InfrastructureInsights.Admin</span></span>
        - <span data-ttu-id="55809-133">Исправлена ошибка, из-за которой в результатах с разбивкой на страницы возвращалась всего одна страница.</span><span class="sxs-lookup"><span data-stu-id="55809-133">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="55809-134">Azs.Network.Admin</span><span class="sxs-lookup"><span data-stu-id="55809-134">Azs.Network.Admin</span></span>
        - <span data-ttu-id="55809-135">Исправлена ошибка, из-за которой в результатах с разбивкой на страницы возвращалась всего одна страница.</span><span class="sxs-lookup"><span data-stu-id="55809-135">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="55809-136">Azs.Update.Admin</span><span class="sxs-lookup"><span data-stu-id="55809-136">Azs.Update.Admin</span></span>
        - <span data-ttu-id="55809-137">Исправлена ошибка, из-за которой в результатах с разбивкой на страницы возвращалась всего одна страница.</span><span class="sxs-lookup"><span data-stu-id="55809-137">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="55809-138">Azs.Subscriptions</span><span class="sxs-lookup"><span data-stu-id="55809-138">Azs.Subscriptions</span></span>
        - <span data-ttu-id="55809-139">Исправлена ошибка, из-за которой в результатах с разбивкой на страницы возвращалась всего одна страница.</span><span class="sxs-lookup"><span data-stu-id="55809-139">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="55809-140">Azs.Subscriptions.Admin</span><span class="sxs-lookup"><span data-stu-id="55809-140">Azs.Subscriptions.Admin</span></span>
        - <span data-ttu-id="55809-141">Добавлен командлет Move-AzsSubscription, позволяющий перемещать подписки между предложениями делегированных поставщиков.</span><span class="sxs-lookup"><span data-stu-id="55809-141">Added a cmdlet Move-AzsSubscription to move subscriptions between delegated provider offers</span></span>
        - <span data-ttu-id="55809-142">Добавлен командлет Test-AzsMoveSubscription, позволяющий проверить, можно ли перемещать подписки пользователей между предложениями делегированных поставщиков.</span><span class="sxs-lookup"><span data-stu-id="55809-142">Added a cmdlet Test-AzsMoveSubscription to validate that user subscriptions can be moved between delegated provider offers</span></span>
        - <span data-ttu-id="55809-143">Исправлена ошибка, из-за которой в результатах с разбивкой на страницы возвращалась всего одна страница.</span><span class="sxs-lookup"><span data-stu-id="55809-143">Fix for the bug that returned only a single page in paginated results'</span></span>

## <a name="content"></a><span data-ttu-id="55809-144">Содержимое:</span><span class="sxs-lookup"><span data-stu-id="55809-144">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="55809-145">Мост Azure</span><span class="sxs-lookup"><span data-stu-id="55809-145">Azure Bridge</span></span>
<span data-ttu-id="55809-146">Предварительная версия модуля для администраторов компонента Azure Stack "Мост Azure", которая позволяет объединять образы из Azure.</span><span class="sxs-lookup"><span data-stu-id="55809-146">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="55809-147">Azure Backup</span><span class="sxs-lookup"><span data-stu-id="55809-147">Backup</span></span>
<span data-ttu-id="55809-148">Предварительная версия модуля для администраторов службы Backup, которая позволяет администраторам:</span><span class="sxs-lookup"><span data-stu-id="55809-148">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="55809-149">настраивать расположение для хранения резервных копий;</span><span class="sxs-lookup"><span data-stu-id="55809-149">Configure where backups are stored</span></span>
- <span data-ttu-id="55809-150">выполнять резервное копирование;</span><span class="sxs-lookup"><span data-stu-id="55809-150">Perform backups</span></span>
- <span data-ttu-id="55809-151">выводить список созданных резервных копий и выполнять на их основе восстановление.</span><span class="sxs-lookup"><span data-stu-id="55809-151">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="55809-152">Приложения для коммерции</span><span class="sxs-lookup"><span data-stu-id="55809-152">Commerce</span></span>
<span data-ttu-id="55809-153">Предварительная версия модуля для администраторов средства коммерции в Azure Stack, которая позволяет просматривать статистические сведения об использовании данных для всей системы Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="55809-153">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="55809-154">Службы вычислений</span><span class="sxs-lookup"><span data-stu-id="55809-154">Compute</span></span>
<span data-ttu-id="55809-155">Предварительная версия модуля для администраторов вычислительных ресурсов в Azure Stack, которая предоставляет функции управления квотами вычислительных ресурсов, образами платформ и расширениями виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="55809-155">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="55809-156">Fabric</span><span class="sxs-lookup"><span data-stu-id="55809-156">Fabric</span></span>
<span data-ttu-id="55809-157">Предварительная версия модуля для администраторов Fabric в Azure Stack, которая позволяет администраторам просматривать компоненты инфраструктуры и управлять ими, выполняя следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="55809-157">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="55809-158">остановка, запуск и завершение работы для узлов единиц масштабирования;</span><span class="sxs-lookup"><span data-stu-id="55809-158">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="55809-159">очистка и возобновление работы узлов единиц масштабирования для связанных действий FRU;</span><span class="sxs-lookup"><span data-stu-id="55809-159">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="55809-160">исправление узлов единиц масштабирования;</span><span class="sxs-lookup"><span data-stu-id="55809-160">Repair of scale unit nodes</span></span>
- <span data-ttu-id="55809-161">перезапуск роли инфраструктуры;</span><span class="sxs-lookup"><span data-stu-id="55809-161">Restart of Infrastructure role</span></span>
- <span data-ttu-id="55809-162">остановка, запуск и завершение работы экземпляров роли инфраструктуры;</span><span class="sxs-lookup"><span data-stu-id="55809-162">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="55809-163">создание пулов IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="55809-163">Create new IP Pools</span></span>

### <a name="gallery"></a><span data-ttu-id="55809-164">Коллекция</span><span class="sxs-lookup"><span data-stu-id="55809-164">Gallery</span></span>
<span data-ttu-id="55809-165">Предварительная версия модуля для администраторов коллекций Azure Stack, которая предоставляет функции для управления элементами коллекции в Azure Stack Marketplace.</span><span class="sxs-lookup"><span data-stu-id="55809-165">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="55809-166">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="55809-166">Infrastructure Insights</span></span>
<span data-ttu-id="55809-167">Предварительная версия модуля для администраторов Infrastructure Insights, которая позволяет администраторам:</span><span class="sxs-lookup"><span data-stu-id="55809-167">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="55809-168">просматривать сведения о работоспособности ресурсов отметок в Azure Stack;</span><span class="sxs-lookup"><span data-stu-id="55809-168">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="55809-169">просматривать оповещения и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="55809-169">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="55809-170">Хранилище ключей</span><span class="sxs-lookup"><span data-stu-id="55809-170">KeyVault</span></span>
<span data-ttu-id="55809-171">Предварительная версия модуля для администраторов Key Vault в Azure Stack, которая позволяет администратору просматривать квоты Key Vault.</span><span class="sxs-lookup"><span data-stu-id="55809-171">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="55809-172">Сеть</span><span class="sxs-lookup"><span data-stu-id="55809-172">Network</span></span>
<span data-ttu-id="55809-173">Предварительная версия модуля для администраторов сетей, которая позволяет:</span><span class="sxs-lookup"><span data-stu-id="55809-173">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="55809-174">управлять квотами сети;</span><span class="sxs-lookup"><span data-stu-id="55809-174">Management of network quotas</span></span>
- <span data-ttu-id="55809-175">просматривать выделенные сетевые ресурсы, например общедоступные IP-адреса, виртуальные сети, подсистемы балансировки нагрузки;</span><span class="sxs-lookup"><span data-stu-id="55809-175">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="55809-176">использовать командлет для отображения общих сведений об администраторе.</span><span class="sxs-lookup"><span data-stu-id="55809-176">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="55809-177">служба хранилища.</span><span class="sxs-lookup"><span data-stu-id="55809-177">Storage</span></span>
<span data-ttu-id="55809-178">Предварительная версия модуля для администраторов хранилища Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="55809-178">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="55809-179">В этом выпуске мы предоставляем следующие функции:</span><span class="sxs-lookup"><span data-stu-id="55809-179">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="55809-180">управление квотами хранилища;</span><span class="sxs-lookup"><span data-stu-id="55809-180">Manage storage quotas</span></span>
- <span data-ttu-id="55809-181">сборка мусора для удаленных ресурсов хранилища;</span><span class="sxs-lookup"><span data-stu-id="55809-181">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="55809-182">восстановление удаленных учетных записей хранения;</span><span class="sxs-lookup"><span data-stu-id="55809-182">Restore deleted storage accounts</span></span>
- <span data-ttu-id="55809-183">перенос контейнеров из одной общей папки в другую;</span><span class="sxs-lookup"><span data-stu-id="55809-183">Migrate containers from one share to another</span></span>
- <span data-ttu-id="55809-184">просмотр сведений об отдельных компонентах хранилища;</span><span class="sxs-lookup"><span data-stu-id="55809-184">View information about the individual storage components</span></span>
- <span data-ttu-id="55809-185">просмотр сведений об использовании и производительности.</span><span class="sxs-lookup"><span data-stu-id="55809-185">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="55809-186">Администратор подписки</span><span class="sxs-lookup"><span data-stu-id="55809-186">Subscription Admin</span></span>
<span data-ttu-id="55809-187">Предварительная версия модуля для администраторов подписки Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="55809-187">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="55809-188">Этот модуль предоставляет следующие функции для администраторов:</span><span class="sxs-lookup"><span data-stu-id="55809-188">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="55809-189">управление планами и предложениями;</span><span class="sxs-lookup"><span data-stu-id="55809-189">Manage plans and offers</span></span>
- <span data-ttu-id="55809-190">просмотр сведений об использовании и производительности.</span><span class="sxs-lookup"><span data-stu-id="55809-190">View usage and performance information</span></span>
- <span data-ttu-id="55809-191">Управление RBAC</span><span class="sxs-lookup"><span data-stu-id="55809-191">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="55809-192">Подписка</span><span class="sxs-lookup"><span data-stu-id="55809-192">Subscription</span></span>
<span data-ttu-id="55809-193">Предварительная версия модуля подписки Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="55809-193">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="55809-194">Этот модуль предоставляет следующие функции для пользователей:</span><span class="sxs-lookup"><span data-stu-id="55809-194">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="55809-195">создание, удаление и изменение подписок.</span><span class="sxs-lookup"><span data-stu-id="55809-195">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="55809-196">Блокировка изменений</span><span class="sxs-lookup"><span data-stu-id="55809-196">Update</span></span>
<span data-ttu-id="55809-197">Предварительная версия модуля для администраторов обновлений Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="55809-197">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="55809-198">В этом модуле администраторы могут:</span><span class="sxs-lookup"><span data-stu-id="55809-198">In this module administrators can:</span></span>
- <span data-ttu-id="55809-199">выводить список и устанавливать доступные обновления;</span><span class="sxs-lookup"><span data-stu-id="55809-199">List and install available updates</span></span>
- <span data-ttu-id="55809-200">возобновлять прерванную установку обновлений;</span><span class="sxs-lookup"><span data-stu-id="55809-200">Resume interrupted updates</span></span>
- <span data-ttu-id="55809-201">просматривать установленные обновления.</span><span class="sxs-lookup"><span data-stu-id="55809-201">View installed updates</span></span>