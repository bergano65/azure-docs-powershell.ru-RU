# <a name="azure-stack-module-140"></a><span data-ttu-id="5d0f6-101">Модуль Azure Stack 1.4.0</span><span class="sxs-lookup"><span data-stu-id="5d0f6-101">Azure Stack Module 1.4.0</span></span>

## <a name="requirements"></a><span data-ttu-id="5d0f6-102">Требования:</span><span class="sxs-lookup"><span data-stu-id="5d0f6-102">Requirements:</span></span>
<span data-ttu-id="5d0f6-103">Минимальная поддерживаемая версия Azure Stack — 1804.</span><span class="sxs-lookup"><span data-stu-id="5d0f6-103">Minimum supported Azure Stack version is 1804.</span></span>

<span data-ttu-id="5d0f6-104">Примечание. Если вы используете более раннюю версию, установите версию 1.2.11.</span><span class="sxs-lookup"><span data-stu-id="5d0f6-104">Note: If you are using an earlier version install version 1.2.11</span></span>

## <a name="known-issues"></a><span data-ttu-id="5d0f6-105">Известные проблемы:</span><span class="sxs-lookup"><span data-stu-id="5d0f6-105">Known issues:</span></span>

- <span data-ttu-id="5d0f6-106">Для закрытия оповещения требуется Azure Stack версии 1803.</span><span class="sxs-lookup"><span data-stu-id="5d0f6-106">Close Alert requires Azure Stack version 1803</span></span>
- <span data-ttu-id="5d0f6-107">New-AzsOffer не позволяет создать общедоступное предложение.</span><span class="sxs-lookup"><span data-stu-id="5d0f6-107">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="5d0f6-108">После него нужно вызвать командлет Set-AzsOffer, чтобы изменить состояние.</span><span class="sxs-lookup"><span data-stu-id="5d0f6-108">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="5d0f6-109">Нельзя удалить пул IP-адресов без повторного развертывания.</span><span class="sxs-lookup"><span data-stu-id="5d0f6-109">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="breaking-changes"></a><span data-ttu-id="5d0f6-110">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="5d0f6-110">Breaking Changes</span></span>
<span data-ttu-id="5d0f6-111">Критических изменений по сравнению с версией 1.3.0 нет.</span><span class="sxs-lookup"><span data-stu-id="5d0f6-111">There are no breaking changes from the version 1.3.0.</span></span> <span data-ttu-id="5d0f6-112">Все критические изменения при миграции с 1.2.11 описаны по адресу https://aka.ms/azspowershellmigration</span><span class="sxs-lookup"><span data-stu-id="5d0f6-112">All breaking changes migrating from 1.2.11 are documented here https://aka.ms/azspowershellmigration</span></span>

## <a name="install"></a><span data-ttu-id="5d0f6-113">Install</span><span class="sxs-lookup"><span data-stu-id="5d0f6-113">Install</span></span>
```
# 1.4.0 can be installed side by side with 1.3.0
# Remove previous version 1.2.11
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Uninstall-Module -Name AzureStack -Force 


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2017-03-09-profile -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.4.0
```
## <a name="release-notes"></a><span data-ttu-id="5d0f6-114">Заметки о выпуске</span><span class="sxs-lookup"><span data-stu-id="5d0f6-114">Release Notes</span></span>
    * <span data-ttu-id="5d0f6-115">В версии Azurestack 1.4.0 нет критических изменений по сравнению с предыдущим выпуском 1.3.0.</span><span class="sxs-lookup"><span data-stu-id="5d0f6-115">Azurestack 1.4.0 version has no breaking changes from the previous release 1.3.0</span></span>
    * <span data-ttu-id="5d0f6-116">Azs.AzureBridge.Admin</span><span class="sxs-lookup"><span data-stu-id="5d0f6-116">Azs.AzureBridge.Admin</span></span>
        - <span data-ttu-id="5d0f6-117">Исправлена ошибка, из-за которой в результатах с разбивкой на страницы возвращалась всего одна страница.</span><span class="sxs-lookup"><span data-stu-id="5d0f6-117">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="5d0f6-118">Azs.Backup.Admin</span><span class="sxs-lookup"><span data-stu-id="5d0f6-118">Azs.Backup.Admin</span></span>
        - <span data-ttu-id="5d0f6-119">Добавлены новые параметры BackupFrequencyInHours, IsBackupSchedulerEnabled, BackupRetentionPeriodInDays для командлета Set-AzsBackupShare.</span><span class="sxs-lookup"><span data-stu-id="5d0f6-119">Added new parameters BackupFrequencyInHours, IsBackupSchedulerEnabled, BackupRetentionPeriodInDays in cmdlet Set-AzsBackupShare</span></span>
        - <span data-ttu-id="5d0f6-120">Добавлен командлет New-EncyptionKeyBase64, упрощающий создание ключа шифрования.</span><span class="sxs-lookup"><span data-stu-id="5d0f6-120">Added a cmdlet New-EncyptionKeyBase64 to facilitate creating encryption key</span></span>
        - <span data-ttu-id="5d0f6-121">Исправлена ошибка, из-за которой в результатах с разбивкой на страницы возвращалась всего одна страница.</span><span class="sxs-lookup"><span data-stu-id="5d0f6-121">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="5d0f6-122">Azs.Commerce.Admin</span><span class="sxs-lookup"><span data-stu-id="5d0f6-122">Azs.Commerce.Admin</span></span>
        - <span data-ttu-id="5d0f6-123">Исправлена ошибка, из-за которой в результатах с разбивкой на страницы возвращалась всего одна страница.</span><span class="sxs-lookup"><span data-stu-id="5d0f6-123">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="5d0f6-124">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="5d0f6-124">Azs.Fabric.Admin</span></span>
        - <span data-ttu-id="5d0f6-125">Исправлена ошибка, из-за которой в результатах с разбивкой на страницы возвращалась всего одна страница.</span><span class="sxs-lookup"><span data-stu-id="5d0f6-125">Fix for the bug that returned only a single page in paginated results</span></span>
        - <span data-ttu-id="5d0f6-126">Добавлен командлет Add-AzsScaleUnitNode, позволяющий администратору добавлять к метке azurestack новые узлы единиц масштабирования.</span><span class="sxs-lookup"><span data-stu-id="5d0f6-126">Added a cmdlet Add-AzsScaleUnitNode to enable admin to add new scale unit nodes to the azurestack stamp</span></span>
        - <span data-ttu-id="5d0f6-127">Добавлен командлет New-AzsScaleUnitNodeObject, упрощающий создание объектов параметров единиц масштабирования.</span><span class="sxs-lookup"><span data-stu-id="5d0f6-127">Added cmdlet and New-AzsScaleUnitNodeObject to facilitate the creation scale unit parameter objects</span></span>
    * <span data-ttu-id="5d0f6-128">Azs.Gallery.Admin</span><span class="sxs-lookup"><span data-stu-id="5d0f6-128">Azs.Gallery.Admin</span></span>
        - <span data-ttu-id="5d0f6-129">Исправлена ошибка, из-за которой в результатах с разбивкой на страницы возвращалась всего одна страница.</span><span class="sxs-lookup"><span data-stu-id="5d0f6-129">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="5d0f6-130">Azs.InfrastructureInsights.Admin</span><span class="sxs-lookup"><span data-stu-id="5d0f6-130">Azs.InfrastructureInsights.Admin</span></span>
        - <span data-ttu-id="5d0f6-131">Исправлена ошибка, из-за которой в результатах с разбивкой на страницы возвращалась всего одна страница.</span><span class="sxs-lookup"><span data-stu-id="5d0f6-131">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="5d0f6-132">Azs.Network.Admin</span><span class="sxs-lookup"><span data-stu-id="5d0f6-132">Azs.Network.Admin</span></span>
        - <span data-ttu-id="5d0f6-133">Исправлена ошибка, из-за которой в результатах с разбивкой на страницы возвращалась всего одна страница.</span><span class="sxs-lookup"><span data-stu-id="5d0f6-133">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="5d0f6-134">Azs.Update.Admin</span><span class="sxs-lookup"><span data-stu-id="5d0f6-134">Azs.Update.Admin</span></span>
        - <span data-ttu-id="5d0f6-135">Исправлена ошибка, из-за которой в результатах с разбивкой на страницы возвращалась всего одна страница.</span><span class="sxs-lookup"><span data-stu-id="5d0f6-135">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="5d0f6-136">Azs.Subscriptions</span><span class="sxs-lookup"><span data-stu-id="5d0f6-136">Azs.Subscriptions</span></span>
        - <span data-ttu-id="5d0f6-137">Исправлена ошибка, из-за которой в результатах с разбивкой на страницы возвращалась всего одна страница.</span><span class="sxs-lookup"><span data-stu-id="5d0f6-137">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="5d0f6-138">Azs.Subscriptions.Admin</span><span class="sxs-lookup"><span data-stu-id="5d0f6-138">Azs.Subscriptions.Admin</span></span>
        - <span data-ttu-id="5d0f6-139">Добавлен командлет Move-AzsSubscription, позволяющий перемещать подписки между предложениями делегированных поставщиков.</span><span class="sxs-lookup"><span data-stu-id="5d0f6-139">Added a cmdlet Move-AzsSubscription to move subscriptions between delegated provider offers</span></span>
        - <span data-ttu-id="5d0f6-140">Добавлен командлет Test-AzsMoveSubscription, позволяющий проверить, можно ли перемещать подписки пользователей между предложениями делегированных поставщиков.</span><span class="sxs-lookup"><span data-stu-id="5d0f6-140">Added a cmdlet Test-AzsMoveSubscription to validate that user subscriptions can be moved between delegated provider offers</span></span>
        - <span data-ttu-id="5d0f6-141">Исправлена ошибка, из-за которой в результатах с разбивкой на страницы возвращалась всего одна страница.</span><span class="sxs-lookup"><span data-stu-id="5d0f6-141">Fix for the bug that returned only a single page in paginated results'</span></span>

## <a name="content"></a><span data-ttu-id="5d0f6-142">Содержимое:</span><span class="sxs-lookup"><span data-stu-id="5d0f6-142">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="5d0f6-143">Мост Azure</span><span class="sxs-lookup"><span data-stu-id="5d0f6-143">Azure Bridge</span></span>
<span data-ttu-id="5d0f6-144">Предварительная версия модуля для администраторов компонента Azure Stack "Мост Azure", которая позволяет объединять образы из Azure.</span><span class="sxs-lookup"><span data-stu-id="5d0f6-144">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="5d0f6-145">Azure Backup</span><span class="sxs-lookup"><span data-stu-id="5d0f6-145">Backup</span></span>
<span data-ttu-id="5d0f6-146">Предварительная версия модуля для администраторов службы Backup, которая позволяет администраторам:</span><span class="sxs-lookup"><span data-stu-id="5d0f6-146">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="5d0f6-147">настраивать расположение для хранения резервных копий;</span><span class="sxs-lookup"><span data-stu-id="5d0f6-147">Configure where backups are stored</span></span>
- <span data-ttu-id="5d0f6-148">выполнять резервное копирование;</span><span class="sxs-lookup"><span data-stu-id="5d0f6-148">Perform backups</span></span>
- <span data-ttu-id="5d0f6-149">выводить список созданных резервных копий и выполнять на их основе восстановление.</span><span class="sxs-lookup"><span data-stu-id="5d0f6-149">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="5d0f6-150">Приложения для коммерции</span><span class="sxs-lookup"><span data-stu-id="5d0f6-150">Commerce</span></span>
<span data-ttu-id="5d0f6-151">Предварительная версия модуля для администраторов средства коммерции в Azure Stack, которая позволяет просматривать статистические сведения об использовании данных для всей системы Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="5d0f6-151">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="5d0f6-152">Службы вычислений</span><span class="sxs-lookup"><span data-stu-id="5d0f6-152">Compute</span></span>
<span data-ttu-id="5d0f6-153">Предварительная версия модуля для администраторов вычислительных ресурсов в Azure Stack, которая предоставляет функции управления квотами вычислительных ресурсов, образами платформ и расширениями виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="5d0f6-153">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="5d0f6-154">Fabric</span><span class="sxs-lookup"><span data-stu-id="5d0f6-154">Fabric</span></span>
<span data-ttu-id="5d0f6-155">Предварительная версия модуля для администраторов Fabric в Azure Stack, которая позволяет администраторам просматривать компоненты инфраструктуры и управлять ими, выполняя следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="5d0f6-155">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="5d0f6-156">остановка, запуск и завершение работы для узлов единиц масштабирования;</span><span class="sxs-lookup"><span data-stu-id="5d0f6-156">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="5d0f6-157">очистка и возобновление работы узлов единиц масштабирования для связанных действий FRU;</span><span class="sxs-lookup"><span data-stu-id="5d0f6-157">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="5d0f6-158">исправление узлов единиц масштабирования;</span><span class="sxs-lookup"><span data-stu-id="5d0f6-158">Repair of scale unit nodes</span></span>
- <span data-ttu-id="5d0f6-159">перезапуск роли инфраструктуры;</span><span class="sxs-lookup"><span data-stu-id="5d0f6-159">Restart of Infrastructure role</span></span>
- <span data-ttu-id="5d0f6-160">остановка, запуск и завершение работы экземпляров роли инфраструктуры;</span><span class="sxs-lookup"><span data-stu-id="5d0f6-160">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="5d0f6-161">создание пулов IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="5d0f6-161">Create new IP Pools</span></span>

### <a name="gallery"></a><span data-ttu-id="5d0f6-162">Коллекция</span><span class="sxs-lookup"><span data-stu-id="5d0f6-162">Gallery</span></span>
<span data-ttu-id="5d0f6-163">Предварительная версия модуля для администраторов коллекций Azure Stack, которая предоставляет функции для управления элементами коллекции в Azure Stack Marketplace.</span><span class="sxs-lookup"><span data-stu-id="5d0f6-163">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="5d0f6-164">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="5d0f6-164">Infrastructure Insights</span></span>
<span data-ttu-id="5d0f6-165">Предварительная версия модуля для администраторов Infrastructure Insights, которая позволяет администраторам:</span><span class="sxs-lookup"><span data-stu-id="5d0f6-165">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="5d0f6-166">просматривать сведения о работоспособности ресурсов отметок в Azure Stack;</span><span class="sxs-lookup"><span data-stu-id="5d0f6-166">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="5d0f6-167">просматривать оповещения и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="5d0f6-167">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="5d0f6-168">Хранилище ключей</span><span class="sxs-lookup"><span data-stu-id="5d0f6-168">KeyVault</span></span>
<span data-ttu-id="5d0f6-169">Предварительная версия модуля для администраторов Key Vault в Azure Stack, которая позволяет администратору просматривать квоты Key Vault.</span><span class="sxs-lookup"><span data-stu-id="5d0f6-169">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="5d0f6-170">Сеть</span><span class="sxs-lookup"><span data-stu-id="5d0f6-170">Network</span></span>
<span data-ttu-id="5d0f6-171">Предварительная версия модуля для администраторов сетей, которая позволяет:</span><span class="sxs-lookup"><span data-stu-id="5d0f6-171">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="5d0f6-172">управлять квотами сети;</span><span class="sxs-lookup"><span data-stu-id="5d0f6-172">Management of network quotas</span></span>
- <span data-ttu-id="5d0f6-173">просматривать выделенные сетевые ресурсы, например общедоступные IP-адреса, виртуальные сети, подсистемы балансировки нагрузки;</span><span class="sxs-lookup"><span data-stu-id="5d0f6-173">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="5d0f6-174">использовать командлет для отображения общих сведений об администраторе.</span><span class="sxs-lookup"><span data-stu-id="5d0f6-174">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="5d0f6-175">Хранилище</span><span class="sxs-lookup"><span data-stu-id="5d0f6-175">Storage</span></span>
<span data-ttu-id="5d0f6-176">Предварительная версия модуля для администраторов хранилища Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="5d0f6-176">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="5d0f6-177">В этом выпуске мы предоставляем следующие функции:</span><span class="sxs-lookup"><span data-stu-id="5d0f6-177">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="5d0f6-178">управление квотами хранилища;</span><span class="sxs-lookup"><span data-stu-id="5d0f6-178">Manage storage quotas</span></span>
- <span data-ttu-id="5d0f6-179">сборка мусора для удаленных ресурсов хранилища;</span><span class="sxs-lookup"><span data-stu-id="5d0f6-179">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="5d0f6-180">восстановление удаленных учетных записей хранения;</span><span class="sxs-lookup"><span data-stu-id="5d0f6-180">Restore deleted storage accounts</span></span>
- <span data-ttu-id="5d0f6-181">перенос контейнеров из одной общей папки в другую;</span><span class="sxs-lookup"><span data-stu-id="5d0f6-181">Migrate containers from one share to another</span></span>
- <span data-ttu-id="5d0f6-182">просмотр сведений об отдельных компонентах хранилища;</span><span class="sxs-lookup"><span data-stu-id="5d0f6-182">View information about the individual storage components</span></span>
- <span data-ttu-id="5d0f6-183">просмотр сведений об использовании и производительности.</span><span class="sxs-lookup"><span data-stu-id="5d0f6-183">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="5d0f6-184">Администратор подписки</span><span class="sxs-lookup"><span data-stu-id="5d0f6-184">Subscription Admin</span></span>
<span data-ttu-id="5d0f6-185">Предварительная версия модуля для администраторов подписки Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="5d0f6-185">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="5d0f6-186">Этот модуль предоставляет следующие функции для администраторов:</span><span class="sxs-lookup"><span data-stu-id="5d0f6-186">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="5d0f6-187">управление планами и предложениями;</span><span class="sxs-lookup"><span data-stu-id="5d0f6-187">Manage plans and offers</span></span>
- <span data-ttu-id="5d0f6-188">просмотр сведений об использовании и производительности.</span><span class="sxs-lookup"><span data-stu-id="5d0f6-188">View usage and performance information</span></span>
- <span data-ttu-id="5d0f6-189">Управление RBAC</span><span class="sxs-lookup"><span data-stu-id="5d0f6-189">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="5d0f6-190">Подписка</span><span class="sxs-lookup"><span data-stu-id="5d0f6-190">Subscription</span></span>
<span data-ttu-id="5d0f6-191">Предварительная версия модуля подписки Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="5d0f6-191">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="5d0f6-192">Этот модуль предоставляет следующие функции для пользователей:</span><span class="sxs-lookup"><span data-stu-id="5d0f6-192">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="5d0f6-193">создание, удаление и изменение подписок.</span><span class="sxs-lookup"><span data-stu-id="5d0f6-193">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="5d0f6-194">Блокировка изменений</span><span class="sxs-lookup"><span data-stu-id="5d0f6-194">Update</span></span>
<span data-ttu-id="5d0f6-195">Предварительная версия модуля для администраторов обновлений Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="5d0f6-195">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="5d0f6-196">В этом модуле администраторы могут:</span><span class="sxs-lookup"><span data-stu-id="5d0f6-196">In this module administrators can:</span></span>
- <span data-ttu-id="5d0f6-197">выводить список и устанавливать доступные обновления;</span><span class="sxs-lookup"><span data-stu-id="5d0f6-197">List and install available updates</span></span>
- <span data-ttu-id="5d0f6-198">возобновлять прерванную установку обновлений;</span><span class="sxs-lookup"><span data-stu-id="5d0f6-198">Resume interrupted updates</span></span>
- <span data-ttu-id="5d0f6-199">просматривать установленные обновления.</span><span class="sxs-lookup"><span data-stu-id="5d0f6-199">View installed updates</span></span>
