# <a name="azure-stack-module-130"></a><span data-ttu-id="10986-101">Модуль Azure Stack 1.3.0</span><span class="sxs-lookup"><span data-stu-id="10986-101">Azure Stack Module 1.3.0</span></span>

## <a name="requirements"></a><span data-ttu-id="10986-102">Требования:</span><span class="sxs-lookup"><span data-stu-id="10986-102">Requirements:</span></span>
<span data-ttu-id="10986-103">Минимальная поддерживаемая версия Azure Stack — 1804.</span><span class="sxs-lookup"><span data-stu-id="10986-103">Minimum supported Azure Stack version is 1804.</span></span>

<span data-ttu-id="10986-104">Примечание. Если вы используете более раннюю версию, установите версию 1.2.11.</span><span class="sxs-lookup"><span data-stu-id="10986-104">Note: If you are using an earlier version install version 1.2.11</span></span>

## <a name="known-issues"></a><span data-ttu-id="10986-105">Известные проблемы:</span><span class="sxs-lookup"><span data-stu-id="10986-105">Known issues:</span></span>

- <span data-ttu-id="10986-106">Для закрытия оповещения требуется Azure Stack версии 1803.</span><span class="sxs-lookup"><span data-stu-id="10986-106">Close Alert requires Azure Stack version 1803</span></span>
- <span data-ttu-id="10986-107">Для некоторых командлетов хранилища требуется версия Azure Stack 1804.</span><span class="sxs-lookup"><span data-stu-id="10986-107">Some Storage cmdlets do require Azure Stack version 1804</span></span>
- <span data-ttu-id="10986-108">New-AzsOffer не позволяет создать общедоступное предложение.</span><span class="sxs-lookup"><span data-stu-id="10986-108">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="10986-109">После него нужно вызвать командлет Set-AzsOffer, чтобы изменить состояние.</span><span class="sxs-lookup"><span data-stu-id="10986-109">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="10986-110">Нельзя удалить пул IP-адресов без повторного развертывания.</span><span class="sxs-lookup"><span data-stu-id="10986-110">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="breaking-changes"></a><span data-ttu-id="10986-111">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="10986-111">Breaking Changes</span></span>
<span data-ttu-id="10986-112">Все критические изменения при миграции с 1.2.11 описаны по адресу https://aka.ms/azspowershellmigration</span><span class="sxs-lookup"><span data-stu-id="10986-112">All breaking changes migrating from 1.2.11 are documented here https://aka.ms/azspowershellmigration</span></span>

## <a name="install"></a><span data-ttu-id="10986-113">Install</span><span class="sxs-lookup"><span data-stu-id="10986-113">Install</span></span>
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
## <a name="content"></a><span data-ttu-id="10986-114">Содержимое:</span><span class="sxs-lookup"><span data-stu-id="10986-114">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="10986-115">Мост Azure</span><span class="sxs-lookup"><span data-stu-id="10986-115">Azure Bridge</span></span>
<span data-ttu-id="10986-116">Предварительная версия модуля для администраторов компонента Azure Stack "Мост Azure", которая позволяет объединять образы из Azure.</span><span class="sxs-lookup"><span data-stu-id="10986-116">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="10986-117">Azure Backup</span><span class="sxs-lookup"><span data-stu-id="10986-117">Backup</span></span>
<span data-ttu-id="10986-118">Предварительная версия модуля для администраторов службы Backup, которая позволяет администраторам:</span><span class="sxs-lookup"><span data-stu-id="10986-118">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="10986-119">настраивать расположение для хранения резервных копий;</span><span class="sxs-lookup"><span data-stu-id="10986-119">Configure where backups are stored</span></span>
- <span data-ttu-id="10986-120">выполнять резервное копирование;</span><span class="sxs-lookup"><span data-stu-id="10986-120">Perform backups</span></span>
- <span data-ttu-id="10986-121">выводить список созданных резервных копий и выполнять на их основе восстановление.</span><span class="sxs-lookup"><span data-stu-id="10986-121">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="10986-122">Приложения для коммерции</span><span class="sxs-lookup"><span data-stu-id="10986-122">Commerce</span></span>
<span data-ttu-id="10986-123">Предварительная версия модуля для администраторов средства коммерции в Azure Stack, которая позволяет просматривать статистические сведения об использовании данных для всей системы Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="10986-123">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="10986-124">Службы вычислений</span><span class="sxs-lookup"><span data-stu-id="10986-124">Compute</span></span>
<span data-ttu-id="10986-125">Предварительная версия модуля для администраторов вычислительных ресурсов в Azure Stack, которая предоставляет функции управления квотами вычислительных ресурсов, образами платформ и расширениями виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="10986-125">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="10986-126">Fabric</span><span class="sxs-lookup"><span data-stu-id="10986-126">Fabric</span></span>
<span data-ttu-id="10986-127">Предварительная версия модуля для администраторов Fabric в Azure Stack, которая позволяет администраторам просматривать компоненты инфраструктуры и управлять ими, выполняя следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="10986-127">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="10986-128">остановка, запуск и завершение работы для узлов единиц масштабирования;</span><span class="sxs-lookup"><span data-stu-id="10986-128">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="10986-129">очистка и возобновление работы узлов единиц масштабирования для связанных действий FRU;</span><span class="sxs-lookup"><span data-stu-id="10986-129">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="10986-130">исправление узлов единиц масштабирования;</span><span class="sxs-lookup"><span data-stu-id="10986-130">Repair of scale unit nodes</span></span>
- <span data-ttu-id="10986-131">перезапуск роли инфраструктуры;</span><span class="sxs-lookup"><span data-stu-id="10986-131">Restart of Infrastructure role</span></span>
- <span data-ttu-id="10986-132">остановка, запуск и завершение работы экземпляров роли инфраструктуры;</span><span class="sxs-lookup"><span data-stu-id="10986-132">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="10986-133">создание пулов IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="10986-133">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="10986-134">Коллекция</span><span class="sxs-lookup"><span data-stu-id="10986-134">Gallery</span></span>
<span data-ttu-id="10986-135">Предварительная версия модуля для администраторов коллекций Azure Stack, которая предоставляет функции для управления элементами коллекции в Azure Stack Marketplace.</span><span class="sxs-lookup"><span data-stu-id="10986-135">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="10986-136">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="10986-136">Infrastructure Insights</span></span>
<span data-ttu-id="10986-137">Предварительная версия модуля для администраторов Infrastructure Insights, которая позволяет администраторам:</span><span class="sxs-lookup"><span data-stu-id="10986-137">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="10986-138">просматривать сведения о работоспособности ресурсов отметок в Azure Stack;</span><span class="sxs-lookup"><span data-stu-id="10986-138">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="10986-139">просматривать оповещения и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="10986-139">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="10986-140">Хранилище ключей</span><span class="sxs-lookup"><span data-stu-id="10986-140">KeyVault</span></span>
<span data-ttu-id="10986-141">Предварительная версия модуля для администраторов Key Vault в Azure Stack, которая позволяет администратору просматривать квоты Key Vault.</span><span class="sxs-lookup"><span data-stu-id="10986-141">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="10986-142">Сеть</span><span class="sxs-lookup"><span data-stu-id="10986-142">Network</span></span>
<span data-ttu-id="10986-143">Предварительная версия модуля для администраторов сетей, которая позволяет:</span><span class="sxs-lookup"><span data-stu-id="10986-143">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="10986-144">управлять квотами сети;</span><span class="sxs-lookup"><span data-stu-id="10986-144">Management of network quotas</span></span>
- <span data-ttu-id="10986-145">просматривать выделенные сетевые ресурсы, например общедоступные IP-адреса, виртуальные сети, подсистемы балансировки нагрузки;</span><span class="sxs-lookup"><span data-stu-id="10986-145">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="10986-146">использовать командлет для отображения общих сведений об администраторе.</span><span class="sxs-lookup"><span data-stu-id="10986-146">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="10986-147">Служба хранилища</span><span class="sxs-lookup"><span data-stu-id="10986-147">Storage</span></span>
<span data-ttu-id="10986-148">Предварительная версия модуля для администраторов хранилища Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="10986-148">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="10986-149">В этом выпуске мы предоставляем следующие функции:</span><span class="sxs-lookup"><span data-stu-id="10986-149">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="10986-150">управление квотами хранилища;</span><span class="sxs-lookup"><span data-stu-id="10986-150">Manage storage quotas</span></span>
- <span data-ttu-id="10986-151">сборка мусора для удаленных ресурсов хранилища;</span><span class="sxs-lookup"><span data-stu-id="10986-151">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="10986-152">восстановление удаленных учетных записей хранения;</span><span class="sxs-lookup"><span data-stu-id="10986-152">Restore deleted storage accounts</span></span>
- <span data-ttu-id="10986-153">перенос контейнеров из одной общей папки в другую;</span><span class="sxs-lookup"><span data-stu-id="10986-153">Migrate containers from one share to another</span></span>
- <span data-ttu-id="10986-154">просмотр сведений об отдельных компонентах хранилища;</span><span class="sxs-lookup"><span data-stu-id="10986-154">View information about the individual storage components</span></span>
- <span data-ttu-id="10986-155">просмотр сведений об использовании и производительности.</span><span class="sxs-lookup"><span data-stu-id="10986-155">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="10986-156">Администратор подписки</span><span class="sxs-lookup"><span data-stu-id="10986-156">Subscription Admin</span></span>
<span data-ttu-id="10986-157">Предварительная версия модуля для администраторов подписки Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="10986-157">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="10986-158">Этот модуль предоставляет следующие функции для администраторов:</span><span class="sxs-lookup"><span data-stu-id="10986-158">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="10986-159">управление планами и предложениями;</span><span class="sxs-lookup"><span data-stu-id="10986-159">Manage plans and offers</span></span>
- <span data-ttu-id="10986-160">просмотр сведений об использовании и производительности.</span><span class="sxs-lookup"><span data-stu-id="10986-160">View usage and performance information</span></span>
- <span data-ttu-id="10986-161">Управление RBAC</span><span class="sxs-lookup"><span data-stu-id="10986-161">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="10986-162">Подписка</span><span class="sxs-lookup"><span data-stu-id="10986-162">Subscription</span></span>
<span data-ttu-id="10986-163">Предварительная версия модуля подписки Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="10986-163">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="10986-164">Этот модуль предоставляет следующие функции для пользователей:</span><span class="sxs-lookup"><span data-stu-id="10986-164">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="10986-165">создание, удаление и изменение подписок.</span><span class="sxs-lookup"><span data-stu-id="10986-165">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="10986-166">Блокировка изменений</span><span class="sxs-lookup"><span data-stu-id="10986-166">Update</span></span>
<span data-ttu-id="10986-167">Предварительная версия модуля для администраторов обновлений Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="10986-167">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="10986-168">В этом модуле администраторы могут:</span><span class="sxs-lookup"><span data-stu-id="10986-168">In this module administrators can:</span></span>
- <span data-ttu-id="10986-169">выводить список и устанавливать доступные обновления;</span><span class="sxs-lookup"><span data-stu-id="10986-169">List and install available updates</span></span>
- <span data-ttu-id="10986-170">возобновлять прерванную установку обновлений;</span><span class="sxs-lookup"><span data-stu-id="10986-170">Resume interrupted updates</span></span>
- <span data-ttu-id="10986-171">просматривать установленные обновления.</span><span class="sxs-lookup"><span data-stu-id="10986-171">View installed updates</span></span>
