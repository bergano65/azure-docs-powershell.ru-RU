---
title: Заметки о выпуске Azure PowerShell
description: Узнайте обо всех последних обновлениях модулей Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: 2280b594ee9f525b2fa3175c917f6365cea354ba
ms.sourcegitcommit: 45e1823aa1a792840aa4829831b5f67a9d5d24a0
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "74537119"
---
## <a name="310---november-2019"></a><span data-ttu-id="8d767-103">Версия 3.1.0 от ноября 2019 г.</span><span class="sxs-lookup"><span data-stu-id="8d767-103">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8d767-104">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="8d767-104">Highlights since the last major release</span></span>
* <span data-ttu-id="8d767-105">Выпуск Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="8d767-105">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="8d767-106">Выпуск Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="8d767-106">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d767-107">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d767-107">Az.Compute</span></span>
* <span data-ttu-id="8d767-108">Функция повторного применения виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="8d767-108">VM Reapply feature</span></span>
    - <span data-ttu-id="8d767-109">Добавлен параметр повторного применения в командлет Set-AzVM.</span><span class="sxs-lookup"><span data-stu-id="8d767-109">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="8d767-110">Функция AutomaticRepairs масштабируемого набора виртуальных машин:</span><span class="sxs-lookup"><span data-stu-id="8d767-110">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="8d767-111">Добавлены параметры EnableAutomaticRepair, AutomaticRepairGracePeriod и AutomaticRepairMaxInstanceRepairsPercent в следующие командлеты:   New-AzVmssConfig Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8d767-111">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="8d767-112">Включена поддержка образа из коллекции разных клиентов для New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="8d767-112">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="8d767-113">Добавлен фрагмент Spot в средство заполнения аргументов параметра Priority в командлетах New-AzVM, New-AzVMConfig и New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="8d767-113">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="8d767-114">Добавлены параметры DiskIOPSReadWrite и DiskMBpsReadWrite в командлет Add-AzVmssDataDisk.</span><span class="sxs-lookup"><span data-stu-id="8d767-114">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="8d767-115">Изменен параметр SourceImageId командлета New-AzGalleryImageVersion на необязательный.</span><span class="sxs-lookup"><span data-stu-id="8d767-115">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="8d767-116">Добавлены параметры OSDiskImage и DataDiskImage в командлет New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="8d767-116">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="8d767-117">Добавлен параметр HyperVGeneration в командлет New-AzGalleryImageDefinition.</span><span class="sxs-lookup"><span data-stu-id="8d767-117">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="8d767-118">Добавлены параметры SkipExtensionsOnOverprovisionedVMs в командлеты New-AzVmss, New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="8d767-118">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="8d767-119">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="8d767-119">Az.DataBoxEdge</span></span>
* <span data-ttu-id="8d767-120">Добавлен командлет `Get-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="8d767-120">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="8d767-121">Получение заказа.</span><span class="sxs-lookup"><span data-stu-id="8d767-121">Get the Order</span></span>
* <span data-ttu-id="8d767-122">Добавлен командлет `New-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="8d767-122">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="8d767-123">Создание заказа.</span><span class="sxs-lookup"><span data-stu-id="8d767-123">Create new Order</span></span>
* <span data-ttu-id="8d767-124">Добавлен командлет `Remove-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="8d767-124">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="8d767-125">Удаление заказа.</span><span class="sxs-lookup"><span data-stu-id="8d767-125">Remove the Order</span></span>
* <span data-ttu-id="8d767-126">Изменен командлет `New-AzDataBoxEdgeShare`.</span><span class="sxs-lookup"><span data-stu-id="8d767-126">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="8d767-127">Создание локальной общей папки.</span><span class="sxs-lookup"><span data-stu-id="8d767-127">Now creates Local Share</span></span>
* <span data-ttu-id="8d767-128">Добавлен командлет `Set-AzDataBoxEdgeRole`.</span><span class="sxs-lookup"><span data-stu-id="8d767-128">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="8d767-129">Сопоставление IotRole с общей папкой.</span><span class="sxs-lookup"><span data-stu-id="8d767-129">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="8d767-130">Добавлен командлет `Invoke-AzDataBoxEdgeDevice`.</span><span class="sxs-lookup"><span data-stu-id="8d767-130">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="8d767-131">Вызов проверки обновлений, скачивание обновления, установка обновления на устройстве.</span><span class="sxs-lookup"><span data-stu-id="8d767-131">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="8d767-132">Добавлен командлет `Get-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="8d767-132">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="8d767-133">Получение сведений о триггерах.</span><span class="sxs-lookup"><span data-stu-id="8d767-133">Gets the information about Triggers</span></span>
* <span data-ttu-id="8d767-134">Добавлен командлет `New-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="8d767-134">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="8d767-135">Создание триггеров.</span><span class="sxs-lookup"><span data-stu-id="8d767-135">Create new Triggers</span></span>
* <span data-ttu-id="8d767-136">Добавлен командлет `Remove-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="8d767-136">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="8d767-137">Удаление триггеров.</span><span class="sxs-lookup"><span data-stu-id="8d767-137">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8d767-138">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8d767-138">Az.DataFactory</span></span>
* <span data-ttu-id="8d767-139">Обновление пакета SDK Фабрики данных для .NET до версии 4.4.0.</span><span class="sxs-lookup"><span data-stu-id="8d767-139">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="8d767-140">Добавлен параметр ExpressCustomSetup в командлет Set-AzureRmDataFactoryV2IntegrationRuntime для включения конфигураций установки и сторонних компонентов без использования настраиваемого скрипта установки.</span><span class="sxs-lookup"><span data-stu-id="8d767-140">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8d767-141">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8d767-141">Az.DataLakeStore</span></span>
* <span data-ttu-id="8d767-142">Обновлена документация по Get-AzDataLakeStoreDeletedItem и Restore-AzDataLakeStoreDeletedItem.</span><span class="sxs-lookup"><span data-stu-id="8d767-142">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8d767-143">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8d767-143">Az.EventHub</span></span>
* <span data-ttu-id="8d767-144">Исправлена проблема № 10301. Исправлен формат даты маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="8d767-144">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8d767-145">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8d767-145">Az.FrontDoor</span></span>
* <span data-ttu-id="8d767-146">Добавлен параметр MinimumTlsVersion в Enable-AzFrontDoorCustomDomainHttps и New-AzFrontDoorFrontendEndpointObject.</span><span class="sxs-lookup"><span data-stu-id="8d767-146">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="8d767-147">Добавлены параметры HealthProbeMethod и EnabledState в New-AzFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="8d767-147">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="8d767-148">Добавлен новый командлет для создания объекта BackendPoolsSettings для передачи при создании и обновлении Front Door.</span><span class="sxs-lookup"><span data-stu-id="8d767-148">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="8d767-149">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="8d767-149">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d767-150">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d767-150">Az.Network</span></span>
* <span data-ttu-id="8d767-151">Изменены примеры параметра FilterData Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="8d767-151">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="8d767-152">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="8d767-152">Az.PrivateDns</span></span>
* <span data-ttu-id="8d767-153">Пакет SDK PrivateDns для .NET обновлен до версии 1.0.0</span><span class="sxs-lookup"><span data-stu-id="8d767-153">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8d767-154">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d767-154">Az.RecoveryServices</span></span>
* <span data-ttu-id="8d767-155">Включена поддержка Azure Site Recovery для выбора типа диска при включении защиты.</span><span class="sxs-lookup"><span data-stu-id="8d767-155">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="8d767-156">Внесено исправление Azure Site Recovery для изменения действия плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="8d767-156">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="8d767-157">Включена поддержка восстановления SQL Azure Backup для принятия баз данных файлового потока.</span><span class="sxs-lookup"><span data-stu-id="8d767-157">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="8d767-158">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8d767-158">Az.RedisCache</span></span>
* <span data-ttu-id="8d767-159">Добавлен параметр MinimumTlsVersion в командлеты New-AzRedisCache и Set-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="8d767-159">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="8d767-160">Кроме того, добавлен параметр MinimumTlsVersion в выходные данные командлета Get-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="8d767-160">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="8d767-161">Добавлена проверка параметра -Size для командлетов Set-AzRedisCache и New-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="8d767-161">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d767-162">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d767-162">Az.Resources</span></span>
- <span data-ttu-id="8d767-163">Обновлены командлеты политики для использования новой версии API 2019-06-01 с новым свойством EnforcementMode в назначении политики.</span><span class="sxs-lookup"><span data-stu-id="8d767-163">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="8d767-164">Обновлен пример справки по созданию определения политики</span><span class="sxs-lookup"><span data-stu-id="8d767-164">Updated create policy definition help example</span></span>
- <span data-ttu-id="8d767-165">Исправлена ошибка с параметром -ServicePrincipalName командлета Remove-AZADServicePrincipal с возвратом пустой ссылки, если имя субъекта службы не найдено.</span><span class="sxs-lookup"><span data-stu-id="8d767-165">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="8d767-166">Исправлена ошибка с New-AZADServicePrincipal с возвратом пустой ссылки, если у клиента нет подписки.</span><span class="sxs-lookup"><span data-stu-id="8d767-166">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="8d767-167">Изменен командлет New-AzAdServicePrincipal для добавления учетных данных только для связанного приложения.</span><span class="sxs-lookup"><span data-stu-id="8d767-167">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d767-168">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d767-168">Az.Sql</span></span>
* <span data-ttu-id="8d767-169">Добавлена поддержка ReadReplicaCount для базы данных.</span><span class="sxs-lookup"><span data-stu-id="8d767-169">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="8d767-170">Исправлена ошибка с Set-AzSqlDatabase, если избыточность в пределах зоны не настроена.</span><span class="sxs-lookup"><span data-stu-id="8d767-170">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="8d767-171">Версия 3.0.0 от ноября 2019 г.</span><span class="sxs-lookup"><span data-stu-id="8d767-171">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="8d767-172">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="8d767-172">General</span></span>
* <span data-ttu-id="8d767-173">Выпущена версия Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="8d767-173">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8d767-174">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d767-174">Az.Accounts</span></span>
* <span data-ttu-id="8d767-175">Добавлено сообщение об устаревании для псевдонима "Resolve-Error".</span><span class="sxs-lookup"><span data-stu-id="8d767-175">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="8d767-176">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="8d767-176">Az.Advisor</span></span>
* <span data-ttu-id="8d767-177">Добавлена новая категория Operational Excellence (Эффективность работы) в командлет Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="8d767-177">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="8d767-178">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8d767-178">Az.Batch</span></span>
* <span data-ttu-id="8d767-179">`CoreQuota` в `BatchAccountContext` переименован в `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="8d767-179">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="8d767-180">Также появился новый `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="8d767-180">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="8d767-181">Это влияет на **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="8d767-181">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="8d767-182">Параметр **New-AzBatchTask** `-ResourceFile` теперь принимает коллекцию объектов `PSResourceFile`, которые можно создать с помощью нового командлета **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="8d767-182">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="8d767-183">Новый командлет **New-AzBatchResourceFile**, который помогает создавать объекты `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="8d767-183">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="8d767-184">Их можно передавать в **New-AzBatchTask** в параметре `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="8d767-184">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="8d767-185">Это позволяет поддерживать два новых типа файлов ресурсов, которые дополняют существующий метод `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="8d767-185">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="8d767-186">Файлы ресурсов на основе `AutoStorageContainerName` скачивают весь контейнер автоматического хранения в узел пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="8d767-186">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="8d767-187">Файлы ресурсов на основе `StorageContainerUrl` скачивают указанный в URL-адресе контейнер в узел пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="8d767-187">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="8d767-188">Удалено свойство `ApplicationPackages` в `PSApplication`, который возвращается из **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="8d767-188">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="8d767-189">Отдельные пакеты в приложении теперь можно извлечь с помощью **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="8d767-189">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="8d767-190">Например, `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="8d767-190">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="8d767-191">`ApplicationId` переименован в `ApplicationName` для **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** и **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="8d767-191">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="8d767-192">Теперь `ApplicationId` является псевдонимом для `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="8d767-192">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="8d767-193">Добавлено новое свойство `PSWindowsUserConfiguration` в `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="8d767-193">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="8d767-194">`Version` переименован в `Name` для `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="8d767-194">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="8d767-195">`BlobSource` переименован в `HttpUrl` для `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="8d767-195">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="8d767-196">Удалено свойство `OSDisk` из `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="8d767-196">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="8d767-197">Удалена операция **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="8d767-197">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="8d767-198">Больше она не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8d767-198">This operation is no longer supported.</span></span>
* <span data-ttu-id="8d767-199">Удалено `TargetOSVersion` из `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="8d767-199">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="8d767-200">`CurrentOSVersion` переименован в `OSVersion` для `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="8d767-200">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="8d767-201">Удалено `DataEgressGiB` и `DataIngressGiB` из `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="8d767-201">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="8d767-202">Операция **Get-AzBatchNodeAgentSku** удалена и заменена на **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="8d767-202">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="8d767-203">**Get-AzBatchSupportedImage** возвращает те же данные, что и **Get-AzBatchNodeAgentSku**, но в более удобном формате.</span><span class="sxs-lookup"><span data-stu-id="8d767-203">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="8d767-204">Также возвращаются новые непроверенные образы.</span><span class="sxs-lookup"><span data-stu-id="8d767-204">New non-verified images are also now returned.</span></span> <span data-ttu-id="8d767-205">Включается и дополнительная информация о `Capabilities` и `BatchSupportEndOfLife` для каждого образа.</span><span class="sxs-lookup"><span data-stu-id="8d767-205">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="8d767-206">Добавлена возможность монтировать файловые системы на каждом узле пула с помощью нового параметра `MountConfiguration` в **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="8d767-206">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="8d767-207">Теперь поддерживаются правила безопасности сети, которые блокируют сетевой доступ к пулу по исходящему порту трафика.</span><span class="sxs-lookup"><span data-stu-id="8d767-207">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="8d767-208">Это выполняется с помощью свойства `SourcePortRanges` для `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="8d767-208">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="8d767-209">Что касается выполнения контейнеров, пакетная служба теперь поддерживает выполнение задачи в рабочей папке контейнера или рабочей папке задачи пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="8d767-209">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="8d767-210">Выбор зависит от параметра `WorkingDirectory` в `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="8d767-210">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="8d767-211">Добавлена возможность указать коллекцию общедоступных IP-адресов для `PSNetworkConfiguration` с помощью нового свойства `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="8d767-211">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="8d767-212">Это гарантирует, что узлы в пуле будут иметь IP-адреса из списка, предоставленного пользователем.</span><span class="sxs-lookup"><span data-stu-id="8d767-212">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="8d767-213">Если значение не задано, по умолчанию для `WaitForSuccess` в `PSSTartTask` используется значение `$True` (ранее `$False`).</span><span class="sxs-lookup"><span data-stu-id="8d767-213">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="8d767-214">Если значение не задано, по умолчанию для `Scope` в `PSAutoUserSpecification` используется значение `Pool` (ранее `Task` для Windows или `Pool` для Linux).</span><span class="sxs-lookup"><span data-stu-id="8d767-214">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8d767-215">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8d767-215">Az.Cdn</span></span>
* <span data-ttu-id="8d767-216">Добавлены UrlRewriteAction и CacheKeyQueryStringAction в RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="8d767-216">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="8d767-217">Исправлено несколько ошибок, таких как отсутствующий входной параметр Selector в командлете New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="8d767-217">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d767-218">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d767-218">Az.Compute</span></span>
* <span data-ttu-id="8d767-219">Функция набора шифрования диска</span><span class="sxs-lookup"><span data-stu-id="8d767-219">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="8d767-220">Новые командлеты:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="8d767-220">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="8d767-221">Добавлен параметр ProximityPlacementGroupId в следующие командлеты: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="8d767-221">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="8d767-222">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="8d767-222">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="8d767-223">Параметры DiskEncryptionSetId и EncryptionType добавлены в следующие командлеты:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="8d767-223">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="8d767-224">Добавлен параметр PublicIPAddressVersion в New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="8d767-224">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="8d767-225">FileUris для расширения пользовательских скриптов теперь будет защищенным, а не общедоступным параметром</span><span class="sxs-lookup"><span data-stu-id="8d767-225">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="8d767-226">Добавлено ScaleInPolicy в командлеты New-AzVmss, New-AzVmssConfig и Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8d767-226">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="8d767-227">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="8d767-227">Breaking changes</span></span>
    - <span data-ttu-id="8d767-228">Параметр UploadSizeInBytes применяется теперь вместо DiskSizeGB для New-AzDiskConfig, если CreateOption имеет значение Upload</span><span class="sxs-lookup"><span data-stu-id="8d767-228">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="8d767-229">PublishingProfile.Source.ManagedImage.Id заменяется на StorageProfile.Source.Id в объекте GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="8d767-229">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8d767-230">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8d767-230">Az.DataFactory</span></span>
* <span data-ttu-id="8d767-231">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.3.0.</span><span class="sxs-lookup"><span data-stu-id="8d767-231">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8d767-232">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8d767-232">Az.DataLakeStore</span></span>
* <span data-ttu-id="8d767-233">Обновлен пакет SDK для ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), включает следующие исправления</span><span class="sxs-lookup"><span data-stu-id="8d767-233">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="8d767-234">Не создается исключение при невозможности десериализовать значение времени создания для записи в корзине или каталоге.</span><span class="sxs-lookup"><span data-stu-id="8d767-234">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="8d767-235">Предоставляется параметр для времени ожидания запроса в adlsclient</span><span class="sxs-lookup"><span data-stu-id="8d767-235">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="8d767-236">Исправлена передача исходного значения syncflag для восстановления badoffset</span><span class="sxs-lookup"><span data-stu-id="8d767-236">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="8d767-237">Исправлена операция EnumerateDirectory, чтобы она извлекала токен продолжения после проверки ответа</span><span class="sxs-lookup"><span data-stu-id="8d767-237">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="8d767-238">Исправлена ошибка объединения</span><span class="sxs-lookup"><span data-stu-id="8d767-238">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8d767-239">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8d767-239">Az.FrontDoor</span></span>
* <span data-ttu-id="8d767-240">Исправлены разные опечатки в разных частях модуля</span><span class="sxs-lookup"><span data-stu-id="8d767-240">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8d767-241">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8d767-241">Az.HDInsight</span></span>
* <span data-ttu-id="8d767-242">Исправлена ошибка, из-за которой клиент получал сообщение об ошибке 'Not a valid Base-64 string' (Не является допустимой строкой Base64) при выполнении Get-AzHDInsightCluster для получения кластера с хранилищем ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="8d767-242">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="8d767-243">Добавлен параметр с именем ApplicationId в три командлета Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig и New-AzHDInsightCluster, чтобы клиент мог предоставить идентификатор приложения субъекта-службы для доступа к Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="8d767-243">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="8d767-244">Для Microsoft.Azure.Management.HDInsight изменена версия с 2.1.0 на 5.1.0</span><span class="sxs-lookup"><span data-stu-id="8d767-244">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="8d767-245">Удалены пять командлетов:</span><span class="sxs-lookup"><span data-stu-id="8d767-245">Removed five cmdlets:</span></span>
    - <span data-ttu-id="8d767-246">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="8d767-246">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="8d767-247">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="8d767-247">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="8d767-248">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="8d767-248">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="8d767-249">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="8d767-249">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="8d767-250">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="8d767-250">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="8d767-251">Добавлены три командлета:</span><span class="sxs-lookup"><span data-stu-id="8d767-251">Added three cmdlets:</span></span>
    - <span data-ttu-id="8d767-252">Get-AzHDInsightMonitoring заменяет собой Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="8d767-252">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="8d767-253">Enable-AzHDInsightMonitoring заменяет собой Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="8d767-253">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="8d767-254">Disable-AzHDInsightMonitoring заменяет собой Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="8d767-254">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="8d767-255">Исправлен командлет Get-AzHDInsightProperties, чтобы он поддерживал получение сведений о возможностях из определенного расположения.</span><span class="sxs-lookup"><span data-stu-id="8d767-255">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="8d767-256">Удалены наборы параметров ("Spark1", "Spark2") из Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="8d767-256">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="8d767-257">Добавлены примеры в справочные документы по командлету Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="8d767-257">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="8d767-258">Изменен тип выходных данных для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="8d767-258">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="8d767-259">Для Get-AzHDInsightProperties тип выходных данных изменен с CapabilitiesResponse на AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="8d767-259">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="8d767-260">Для Remove-AzHDInsightCluster тип выходных данных изменен с ClusterGetResponse на bool.</span><span class="sxs-lookup"><span data-stu-id="8d767-260">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="8d767-261">Для Set-AzHDInsightGatewaySettings тип выходных данных изменен с HttpConnectivitySettings на GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="8d767-261">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="8d767-262">Добавлены несколько условий для проверки сценариев.</span><span class="sxs-lookup"><span data-stu-id="8d767-262">Added some scenario test cases.</span></span>
* <span data-ttu-id="8d767-263">Удалены несколько псевдонимов: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="8d767-263">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8d767-264">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8d767-264">Az.IotHub</span></span>
* <span data-ttu-id="8d767-265">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="8d767-265">Breaking changes:</span></span>
    - <span data-ttu-id="8d767-266">Командлет Add-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="8d767-266">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="8d767-267">Удален набор параметров __AllParameterSets для командлета Add-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="8d767-267">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="8d767-268">Командлет Get-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="8d767-268">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="8d767-269">Удален набор параметров __AllParameterSets для командлета Get-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="8d767-269">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="8d767-270">Удалено свойство OperationsMonitoringProperties для типа Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties.</span><span class="sxs-lookup"><span data-stu-id="8d767-270">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="8d767-271">Удалено свойство OperationsMonitoringProperties для типа Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties.</span><span class="sxs-lookup"><span data-stu-id="8d767-271">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="8d767-272">Командлет New-AzIotHubExportDevice больше не поддерживает псевдоним New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="8d767-272">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="8d767-273">Командлет New-AzIotHubImportDevice больше не поддерживает псевдоним New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="8d767-273">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="8d767-274">Командлет Remove-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="8d767-274">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="8d767-275">Удален набор параметров __AllParameterSets для командлета Remove-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="8d767-275">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="8d767-276">Командлет Set-AzIotHub теперь не поддерживает параметр OperationsMonitoringProperties и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="8d767-276">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="8d767-277">Удален набор параметров UpdateOperationsMonitoringProperties для командлета Set-AzIotHub.</span><span class="sxs-lookup"><span data-stu-id="8d767-277">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8d767-278">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d767-278">Az.RecoveryServices</span></span>
* <span data-ttu-id="8d767-279">Azure Site Recovery поддерживает настройку сетевых ресурсов, например групп безопасности сети, общедоступных IP-адресов и внутренних подсистем балансировки нагрузки из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="8d767-279">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="8d767-280">Azure Site Recovery поддерживает запись на управляемый диск из vMWare в Azure.</span><span class="sxs-lookup"><span data-stu-id="8d767-280">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="8d767-281">Azure Site Recovery поддерживает сокращение NIC из vMWare в Azure.</span><span class="sxs-lookup"><span data-stu-id="8d767-281">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="8d767-282">Azure Site Recovery поддерживает ускорение сети NIC из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="8d767-282">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="8d767-283">Azure Site Recovery поддерживает автоматическое обновление агента из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="8d767-283">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="8d767-284">Azure Site Recovery поддерживает стандартный SSD-накопитель из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="8d767-284">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="8d767-285">Azure Site Recovery поддерживает двухпроходное шифрование диска Azure из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="8d767-285">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="8d767-286">Azure Site Recovery поддерживает новый добавленный диск из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="8d767-286">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="8d767-287">Добавлена функция SoftDelete для виртуальных машин и соответствующие тесты</span><span class="sxs-lookup"><span data-stu-id="8d767-287">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d767-288">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d767-288">Az.Resources</span></span>
* <span data-ttu-id="8d767-289">Обновлена сборка зависимостей Microsoft.Extensions.Caching.Memory с версии 1.1.1 до 2.2</span><span class="sxs-lookup"><span data-stu-id="8d767-289">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d767-290">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d767-290">Az.Network</span></span>
* <span data-ttu-id="8d767-291">Изменены все командлеты для PrivateEndpointConnection, чтобы они поддерживали универсальный поставщик служб.</span><span class="sxs-lookup"><span data-stu-id="8d767-291">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="8d767-292">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="8d767-292">Updated cmdlet:</span></span>
        - <span data-ttu-id="8d767-293">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="8d767-293">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8d767-294">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="8d767-294">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8d767-295">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="8d767-295">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8d767-296">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="8d767-296">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8d767-297">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8d767-297">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="8d767-298">Добавлен новый командлет для PrivateLinkResource, который поддерживает универсальный поставщик служб.</span><span class="sxs-lookup"><span data-stu-id="8d767-298">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="8d767-299">Новый командлет</span><span class="sxs-lookup"><span data-stu-id="8d767-299">New cmdlet:</span></span>
        - <span data-ttu-id="8d767-300">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="8d767-300">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="8d767-301">Добавлены новые поля и параметр для протокола прокси версии 2.</span><span class="sxs-lookup"><span data-stu-id="8d767-301">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="8d767-302">Добавлено свойство EnableProxyProtocol в PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8d767-302">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="8d767-303">Добавлено свойство LinkIdentifier в PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8d767-303">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="8d767-304">Обновлен New-AzPrivateLinkService для поддержки нового необязательного параметра EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="8d767-304">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="8d767-305">Исправлено описание параметра в справочной документации по командлету New-AzApplicationGatewaySku.</span><span class="sxs-lookup"><span data-stu-id="8d767-305">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="8d767-306">Новые командлеты для поддержки политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="8d767-306">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="8d767-307">Добавлена поддержка дочерних ресурсов RouteTables для VirtualHub</span><span class="sxs-lookup"><span data-stu-id="8d767-307">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="8d767-308">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="8d767-308">New cmdlets added:</span></span>
        - <span data-ttu-id="8d767-309">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="8d767-309">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="8d767-310">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="8d767-310">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="8d767-311">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="8d767-311">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="8d767-312">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="8d767-312">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="8d767-313">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="8d767-313">Set-AzVirtualHub</span></span>
* <span data-ttu-id="8d767-314">Добавлена поддержка новых свойств SKU для VirtualHub и VirtualWANType в VirtualWan</span><span class="sxs-lookup"><span data-stu-id="8d767-314">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="8d767-315">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="8d767-315">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="8d767-316">New-AzVirtualHub: добавлен параметр Sku</span><span class="sxs-lookup"><span data-stu-id="8d767-316">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="8d767-317">Update-AzVirtualHub: добавлен параметр Sku</span><span class="sxs-lookup"><span data-stu-id="8d767-317">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="8d767-318">New-AzVirtualWan: добавлен параметр VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="8d767-318">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="8d767-319">Update-AzVirtualWan: добавлен параметр VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="8d767-319">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="8d767-320">Добавлена поддержка свойства EnableInternetSecurity для HubVnetConnection, VpnConnection и ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="8d767-320">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="8d767-321">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="8d767-321">New cmdlets added:</span></span>
        - <span data-ttu-id="8d767-322">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="8d767-322">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="8d767-323">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="8d767-323">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="8d767-324">New-AzureRmVirtualHubVnetConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="8d767-324">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="8d767-325">New-AzureRmVpnConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="8d767-325">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="8d767-326">Update-AzureRmVpnConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="8d767-326">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="8d767-327">New-AzureRmExpressRouteConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="8d767-327">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="8d767-328">Set-AzureRmExpressRouteConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="8d767-328">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="8d767-329">Добавлена поддержка настройки политики верхнего уровня WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="8d767-329">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="8d767-330">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="8d767-330">New cmdlets added:</span></span>
        - <span data-ttu-id="8d767-331">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="8d767-331">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="8d767-332">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="8d767-332">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="8d767-333">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="8d767-333">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="8d767-334">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="8d767-334">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="8d767-335">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="8d767-335">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="8d767-336">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="8d767-336">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="8d767-337">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="8d767-337">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="8d767-338">New-AzApplicationGatewayFirewallPolicy: добавлены параметры PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="8d767-338">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="8d767-339">Добавлена поддержка оператора Geo-Match для CustomRule</span><span class="sxs-lookup"><span data-stu-id="8d767-339">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="8d767-340">Добавлен параметр GeoMatch в оператор для FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="8d767-340">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="8d767-341">Добавлена поддержка политики брандмауэра perListener и perSite</span><span class="sxs-lookup"><span data-stu-id="8d767-341">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="8d767-342">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="8d767-342">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="8d767-343">New-AzApplicationGatewayHttpListener: добавлены параметры FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="8d767-343">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="8d767-344">New-AzApplicationGatewayPathRuleConfig: добавлены параметры FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="8d767-344">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="8d767-345">Исправлен учет регистра для требуемой подсети с именем AzureBastionSubnet в PSBastion</span><span class="sxs-lookup"><span data-stu-id="8d767-345">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="8d767-346">Поддержка полного доменного имени назначения в правилах сети и преобразованного полного доменного имени в правилах NAT для брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="8d767-346">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="8d767-347">Добавлена поддержка ресурсов верхнего уровня RouteTables для IpGroup</span><span class="sxs-lookup"><span data-stu-id="8d767-347">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="8d767-348">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="8d767-348">New cmdlets added:</span></span>
        - <span data-ttu-id="8d767-349">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="8d767-349">New-AzIpGroup</span></span>
        - <span data-ttu-id="8d767-350">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="8d767-350">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="8d767-351">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="8d767-351">Get-AzIpGroup</span></span>
        - <span data-ttu-id="8d767-352">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="8d767-352">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8d767-353">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8d767-353">Az.ServiceFabric</span></span>
* <span data-ttu-id="8d767-354">Удален командлет Add-AzServiceFabricApplicationCertificate, так как соответствующий сценарий выполняется командлетом Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="8d767-354">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d767-355">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d767-355">Az.Sql</span></span>
* <span data-ttu-id="8d767-356">Добавлена поддержка восстановления удаленных баз данных в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="8d767-356">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="8d767-357">Из кода удалены старые командлеты аудита.</span><span class="sxs-lookup"><span data-stu-id="8d767-357">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="8d767-358">Удалены нерекомендуемые псевдонимы:</span><span class="sxs-lookup"><span data-stu-id="8d767-358">Removed deprecated aliases:</span></span>
* <span data-ttu-id="8d767-359">Get-AzSqlDatabaseIndexRecommendations (вместо него используйте Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="8d767-359">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="8d767-360">Get-AzSqlDatabaseRestorePoints (вместо него используйте Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="8d767-360">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="8d767-361">Удален командлет Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8d767-361">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="8d767-362">Удалены псевдонимы для нерекомендуемых командлетов параметров оценки уязвимостей</span><span class="sxs-lookup"><span data-stu-id="8d767-362">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="8d767-363">Командлеты расширенного обнаружения угроз объявлены устаревшими</span><span class="sxs-lookup"><span data-stu-id="8d767-363">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="8d767-364">Добавлены командлеты для отключения и включения рекомендаций о конфиденциальности для столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="8d767-364">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d767-365">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d767-365">Az.Storage</span></span>
* <span data-ttu-id="8d767-366">Поддержка включения большой общей папки при создании или обновлении учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="8d767-366">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="8d767-367">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8d767-367">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="8d767-368">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8d767-368">Set-AzStorageAccount</span></span>
* <span data-ttu-id="8d767-369">При закрытии или получении маркера файла пропускается проверка того, является ли входной путь файлом или каталогом, чтобы избежать сбоев при получении объектов в состоянии DeletePending.</span><span class="sxs-lookup"><span data-stu-id="8d767-369">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="8d767-370">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="8d767-370">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="8d767-371">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="8d767-371">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="8d767-372">2.8.0 — октябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="8d767-372">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="8d767-373">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="8d767-373">General</span></span>
* <span data-ttu-id="8d767-374">Выпуск Az.HealthcareApis 1.0.0</span><span class="sxs-lookup"><span data-stu-id="8d767-374">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8d767-375">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d767-375">Az.Accounts</span></span>
* <span data-ttu-id="8d767-376">Обновление телеметрии и перезаписи URL-адресов для созданных модулей, исправление для модульных тестов Windows.</span><span class="sxs-lookup"><span data-stu-id="8d767-376">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="8d767-377">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8d767-377">Az.ApiManagement</span></span>
* <span data-ttu-id="8d767-378">**Set-AzApiManagementApi** — в ApiVersionSet добавлена поддержка обновления API.</span><span class="sxs-lookup"><span data-stu-id="8d767-378">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="8d767-379">исправлена проблема https://github.com/Azure/azure-powershell/issues/10068.</span><span class="sxs-lookup"><span data-stu-id="8d767-379">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8d767-380">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8d767-380">Az.Automation</span></span>
* <span data-ttu-id="8d767-381">Исправлен командлет New-AzureAutomationSoftwareUpdateConfiguration для параметра перезагрузки Linux.</span><span class="sxs-lookup"><span data-stu-id="8d767-381">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="8d767-382">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8d767-382">Az.Batch</span></span>
* <span data-ttu-id="8d767-383">Командлет **Get-AzBatchNodeAgentSku** объявлен устаревшим и будет заменен на **Get-AzBatchSupportImage** в версии 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="8d767-383">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d767-384">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d767-384">Az.Compute</span></span>
* <span data-ttu-id="8d767-385">В командлеты New-AzVM и New-AzVmss добавлены параметры Priority, EvictionPolicy и MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="8d767-385">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="8d767-386">Исправлены предупреждающее сообщение для командлетов Add-AzVMAdditionalUnattendContent и Add-AzVMSshPublicKey и справочная документация по ним.</span><span class="sxs-lookup"><span data-stu-id="8d767-386">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="8d767-387">Для Set-AzVMDiskEncryptionExtension исправлено исключение -skipVmBackup для виртуальных машин Linux с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="8d767-387">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="8d767-388">Исправлена ошибка при изменении параметров шифрования в Set-AzVMDiskEncryptionExtension, реализован двухэтапный сценарий.</span><span class="sxs-lookup"><span data-stu-id="8d767-388">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8d767-389">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8d767-389">Az.DataFactory</span></span>
* <span data-ttu-id="8d767-390">Добавлены команды CRUD для потока данных Фабрики данных Azure версии 2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow и Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="8d767-390">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="8d767-391">Добавлены команды действий для сеанса отладки потока данных Фабрики данных Azure версии 2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand и Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="8d767-391">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="8d767-392">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.2.0.</span><span class="sxs-lookup"><span data-stu-id="8d767-392">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8d767-393">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8d767-393">Az.DataLakeStore</span></span>
* <span data-ttu-id="8d767-394">Проверка учетной записи исправлена так, чтобы учетные записи, содержащие знак "-", можно было передавать без домена.</span><span class="sxs-lookup"><span data-stu-id="8d767-394">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="8d767-395">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="8d767-395">Az.HealthcareApis</span></span>
* <span data-ttu-id="8d767-396">Версия PowerShell обновлена до 1.0.0.</span><span class="sxs-lookup"><span data-stu-id="8d767-396">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="8d767-397">Версия пакета SDK обновлена до 1.0.2.</span><span class="sxs-lookup"><span data-stu-id="8d767-397">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="8d767-398">В тестах обновлены ссылки на новую версию пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="8d767-398">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="8d767-399">Вложенная выходная структура заменена на плоскую.</span><span class="sxs-lookup"><span data-stu-id="8d767-399">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8d767-400">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8d767-400">Az.IotHub</span></span>
* <span data-ttu-id="8d767-401">Добавлен новый источник маршрутизации DigitalTwinChangeEvents.</span><span class="sxs-lookup"><span data-stu-id="8d767-401">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="8d767-402">Исправлены незначительные ошибки: Get-AzIothub не возвращает subscriptionId.</span><span class="sxs-lookup"><span data-stu-id="8d767-402">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="8d767-403">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8d767-403">Az.Monitor</span></span>
* <span data-ttu-id="8d767-404">Добавлены новые получатели групп действий: -ItsmReceiver, -VoiceReceiver, -ArmRoleReceiver, -AzureFunctionReceiver, -LogicAppReceiver, -AutomationRunbookReceiver, -AzureAppPushReceiver.</span><span class="sxs-lookup"><span data-stu-id="8d767-404">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="8d767-405">Для получателей включите общую схему оповещений.</span><span class="sxs-lookup"><span data-stu-id="8d767-405">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="8d767-406">Это не касается получателей SMS, push-уведомлений приложения Azure, ITSM и голосовых сообщений.</span><span class="sxs-lookup"><span data-stu-id="8d767-406">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="8d767-407">Веб-перехватчики теперь поддерживают аутентификацию Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8d767-407">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d767-408">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d767-408">Az.Network</span></span>
* <span data-ttu-id="8d767-409">Добавлен новый командлет Get-AzAvailableServiceAlias, позволяющий получить псевдонимы для политик конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="8d767-409">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="8d767-410">В подключениях шлюза виртуальной сети появилась возможность добавлять селекторы трафика.</span><span class="sxs-lookup"><span data-stu-id="8d767-410">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="8d767-411">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="8d767-411">New cmdlets added:</span></span>
        - <span data-ttu-id="8d767-412">New-AzureRmTrafficSelectorPolicy.</span><span class="sxs-lookup"><span data-stu-id="8d767-412">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="8d767-413">В командлеты добавлены необязательные параметры -TrafficSelectorPolicies, -New-AzureRmVirtualNetworkGatewayConnection, -Set-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="8d767-413">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="8d767-414">В конфигурациях правил сетевой безопасности добавлена поддержка протоколов ESP и AH.</span><span class="sxs-lookup"><span data-stu-id="8d767-414">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="8d767-415">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="8d767-415">Updated cmdlets:</span></span>
        - <span data-ttu-id="8d767-416">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="8d767-416">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="8d767-417">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="8d767-417">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="8d767-418">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="8d767-418">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="8d767-419">Улучшена обработка исключений в командлетах Cortex.</span><span class="sxs-lookup"><span data-stu-id="8d767-419">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="8d767-420">Выпущены новые поколения и номера SKU VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="8d767-420">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="8d767-421">Представлены новые поколения VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="8d767-421">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="8d767-422">Представлены новые номера SKU VirtualNetworkGateways с высокой пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="8d767-422">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="8d767-423">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8d767-423">Az.RedisCache</span></span>
* <span data-ttu-id="8d767-424">В справочную документацию по Set-AzRedisCache добавлены недостающие значения для параметра -Size.</span><span class="sxs-lookup"><span data-stu-id="8d767-424">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d767-425">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d767-425">Az.Sql</span></span>
* <span data-ttu-id="8d767-426">Добавлена возможность назначать администратора Active Directory в Управляемом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="8d767-426">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d767-427">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d767-427">Az.Storage</span></span>
* <span data-ttu-id="8d767-428">Клиентская библиотека службы хранилища Azure обновлена до версии 11.1.0.</span><span class="sxs-lookup"><span data-stu-id="8d767-428">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="8d767-429">NextPageLink теперь позволяет получить список контейнеров с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="8d767-429">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="8d767-430">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="8d767-430">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="8d767-431">NextPageLink теперь позволяет получить список учетных записей хранения из подписки.</span><span class="sxs-lookup"><span data-stu-id="8d767-431">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="8d767-432">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8d767-432">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="8d767-433">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="8d767-433">Az.StorageSync</span></span>
* <span data-ttu-id="8d767-434">Исправлена проблема 9810 с Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="8d767-434">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8d767-435">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d767-435">Az.Websites</span></span>
* <span data-ttu-id="8d767-436">Обновление плана службы приложений с помощью Set-AzWebApp приводило к сбою приложения.</span><span class="sxs-lookup"><span data-stu-id="8d767-436">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="8d767-437">2.7.0 — сентябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="8d767-437">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="8d767-438">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8d767-438">Az.ApiManagement</span></span>
* <span data-ttu-id="8d767-439">В справочной документации по командлету Set-AzApiManagementPolicy обновлено описание параметра -Format.</span><span class="sxs-lookup"><span data-stu-id="8d767-439">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="8d767-440">Из справочной документации удалены ссылки на нерекомендуемый командлет Update-AzApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="8d767-440">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="8d767-441">Вместо него следует использовать командлет Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="8d767-441">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8d767-442">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8d767-442">Az.Automation</span></span>
* <span data-ttu-id="8d767-443">В справочной документации по командлету Register-AzAutomationDscNode исправлена опечатка в примере.</span><span class="sxs-lookup"><span data-stu-id="8d767-443">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="8d767-444">Добавлено уточнение об ограничениях ОС для командлета Register-AzAutomationDSCNode.</span><span class="sxs-lookup"><span data-stu-id="8d767-444">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="8d767-445">Исправлено исключение пустой ссылки для параметра -Wait в командлете Start-AzAutomationRunbook.</span><span class="sxs-lookup"><span data-stu-id="8d767-445">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d767-446">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d767-446">Az.Compute</span></span>
* <span data-ttu-id="8d767-447">Добавлен параметр UploadSizeInBytes для командлета New-AzDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="8d767-447">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="8d767-448">Добавлен добавочный параметр для командлета New-AzSnapshotConfig.</span><span class="sxs-lookup"><span data-stu-id="8d767-448">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="8d767-449">Для виртуальной машины добавлены такие функции с низким приоритетом:</span><span class="sxs-lookup"><span data-stu-id="8d767-449">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="8d767-450">Для командлета New-AzVMConfig добавлены параметры MaxPrice, EvictionPolicy и Priority.</span><span class="sxs-lookup"><span data-stu-id="8d767-450">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="8d767-451">Для командлетов New-AzVmssConfig, Update-AzVM и Update-AzVmss добавлен параметр MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="8d767-451">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="8d767-452">Для командлета Get-AzAvailabilitySet устранена проблема со ссылкой на виртуальную машину, когда в нем перечисляются все группы доступности в подписке.</span><span class="sxs-lookup"><span data-stu-id="8d767-452">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="8d767-453">Исправлено исключение NULL для командлета Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="8d767-453">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="8d767-454">Исправлен метод поиска VHD для относительной конечной позиции.</span><span class="sxs-lookup"><span data-stu-id="8d767-454">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="8d767-455">Устранена проблема с UltraSSD для командлетов New-AzVM и Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="8d767-455">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8d767-456">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8d767-456">Az.DataFactory</span></span>
* <span data-ttu-id="8d767-457">Добавлены 3 новые команды для ADF версии 2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription и Get-AzDataFactoryV2TriggerSubscriptionStatus.</span><span class="sxs-lookup"><span data-stu-id="8d767-457">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="8d767-458">Пакет SDK ADF для .NET обновлен до версии 4.1.3.</span><span class="sxs-lookup"><span data-stu-id="8d767-458">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8d767-459">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8d767-459">Az.HDInsight</span></span>
* <span data-ttu-id="8d767-460">Укажите критические изменения.</span><span class="sxs-lookup"><span data-stu-id="8d767-460">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8d767-461">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8d767-461">Az.IotHub</span></span>
* <span data-ttu-id="8d767-462">Добавлена поддержка для вызова отработки отказа для IotHub в георегион аварийного восстановления.</span><span class="sxs-lookup"><span data-stu-id="8d767-462">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="8d767-463">Добавлена поддержка для управления обогащением сообщений для IotHub.</span><span class="sxs-lookup"><span data-stu-id="8d767-463">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="8d767-464">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="8d767-464">New cmdlets are:</span></span>
    - <span data-ttu-id="8d767-465">Add-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="8d767-465">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="8d767-466">Get-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="8d767-466">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="8d767-467">Remove-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="8d767-467">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="8d767-468">Set-AzIotHubMessageEnrichment.</span><span class="sxs-lookup"><span data-stu-id="8d767-468">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8d767-469">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8d767-469">Az.Monitor</span></span>
* <span data-ttu-id="8d767-470">Указание на самую последнюю версию пакета SDK для монитора, т. е. 0.24.1-preview:</span><span class="sxs-lookup"><span data-stu-id="8d767-470">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="8d767-471">В командлеты метрик добавлены некритические изменения, т. е. перечисление единиц поддерживает несколько новых значений.</span><span class="sxs-lookup"><span data-stu-id="8d767-471">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="8d767-472">Эти командлеты доступны только для чтения, поэтому входные данные командлетов не будут изменены.</span><span class="sxs-lookup"><span data-stu-id="8d767-472">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="8d767-473">Актуальная версия API запросов **ActionGroups** — **2019-06-01**. До этого была версия **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="8d767-473">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="8d767-474">Тесты сценария обновлены в соответствии с этим изменением.</span><span class="sxs-lookup"><span data-stu-id="8d767-474">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="8d767-475">В конструкторы классов **EmailReceiver** и **WebhookReceiver** добавлен один новый обязательный аргумент — логическое значение с именем **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="8d767-475">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="8d767-476">Сейчас для него установлено значение **false**, чтобы скрыть это критическое изменение от командлетов.</span><span class="sxs-lookup"><span data-stu-id="8d767-476">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="8d767-477">**Примечание**. Это временное изменение, которое должно быть подтверждено командой оповещения.</span><span class="sxs-lookup"><span data-stu-id="8d767-477">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="8d767-478">Порядок аргументов для конструктора класса **Source** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="8d767-478">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="8d767-479">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="8d767-479">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="8d767-480">Порядок аргументов для конструктора класса **AlertingAction** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="8d767-480">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="8d767-481">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="8d767-481">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="8d767-482">Добавлена поддержка критериев динамического порога для оповещения метрики версии 2:</span><span class="sxs-lookup"><span data-stu-id="8d767-482">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="8d767-483">New-AzMetricAlertRuleV2Criteria: теперь также позволяет создавать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="8d767-483">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="8d767-484">Add-AzMetricAlertRuleV2: теперь также позволяет принимать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="8d767-484">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="8d767-485">Добавлены усовершенствования в командлетах запланированных правил запросов (SQR).</span><span class="sxs-lookup"><span data-stu-id="8d767-485">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="8d767-486">Командлеты будут принимать параметр Location в обоих форматах: расположение (например, eastus) или отображаемое имя расположения (например, "восточная часть США").</span><span class="sxs-lookup"><span data-stu-id="8d767-486">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="8d767-487">Параметр Enabled проиллюстрирован в файлах справки надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="8d767-487">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="8d767-488">Добавлены примеры для необязательного параметра ActionGroup.</span><span class="sxs-lookup"><span data-stu-id="8d767-488">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="8d767-489">Все файлы справки улучшены.</span><span class="sxs-lookup"><span data-stu-id="8d767-489">Overall improved help files</span></span>
* <span data-ttu-id="8d767-490">Исправлена ошибка в определении типа области для командлета Set-AzActionRule.</span><span class="sxs-lookup"><span data-stu-id="8d767-490">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d767-491">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d767-491">Az.Network</span></span>
* <span data-ttu-id="8d767-492">Исправлен неправильный пример в справочной документации по командлету New-AzApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="8d767-492">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="8d767-493">В справочную документацию по командлету Get-AzNetworkWatcherPacketCapture добавлено примечание, посвященное извлечению всех свойств для записи пакетов.</span><span class="sxs-lookup"><span data-stu-id="8d767-493">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="8d767-494">В справочной документации по командлету Test-AzNetworkWatcherIPFlow исправлен пример: теперь он правильно перечисляет сетевые карты.</span><span class="sxs-lookup"><span data-stu-id="8d767-494">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="8d767-495">Улучшен анализ облачных исключений для отображения дополнительных сведений (при их наличии).</span><span class="sxs-lookup"><span data-stu-id="8d767-495">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="8d767-496">Улучшен анализ облачных исключений для обработки дополнительного типа исключения SDK.</span><span class="sxs-lookup"><span data-stu-id="8d767-496">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="8d767-497">Исправлено неправильное сопоставление моделей правил безопасности.</span><span class="sxs-lookup"><span data-stu-id="8d767-497">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="8d767-498">Добавлены свойства сетевого интерфейса для компонента частного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="8d767-498">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="8d767-499">Для интерфейса PSNetworkInterface добавлено свойство PrivateEndpoint с типом PSResourceId.</span><span class="sxs-lookup"><span data-stu-id="8d767-499">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="8d767-500">В PSNetworkInterfaceIPConfiguration добавлено свойство PrivateLinkConnectionProperties с типом PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="8d767-500">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="8d767-501">Добавлен новый класс модели: PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="8d767-501">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="8d767-502">Добавлен новый тип ApplicationRuleProtocolType "mssql" для ресурса Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="8d767-502">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="8d767-503">Поддержка многоканального подключения в Виртуальной глобальной сети:</span><span class="sxs-lookup"><span data-stu-id="8d767-503">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="8d767-504">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="8d767-504">New cmdlets</span></span>
        - <span data-ttu-id="8d767-505">New-AzVpnSiteLink;</span><span class="sxs-lookup"><span data-stu-id="8d767-505">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="8d767-506">New-AzVpnSiteLinkConnection;</span><span class="sxs-lookup"><span data-stu-id="8d767-506">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="8d767-507">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="8d767-507">Updated cmdlet:</span></span>
        - <span data-ttu-id="8d767-508">New-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="8d767-508">New-VpnSite</span></span>
        - <span data-ttu-id="8d767-509">Update-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="8d767-509">Update-VpnSite</span></span>
        - <span data-ttu-id="8d767-510">New-VpnConnection;</span><span class="sxs-lookup"><span data-stu-id="8d767-510">New-VpnConnection</span></span>
        - <span data-ttu-id="8d767-511">Update-VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="8d767-511">Update-VpnConnection</span></span>
* <span data-ttu-id="8d767-512">Исправлены документы с некоторыми примерами PowerShell для использования командлетов AZ вместо командлетов AzureRM.</span><span class="sxs-lookup"><span data-stu-id="8d767-512">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8d767-513">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d767-513">Az.RecoveryServices</span></span>
* <span data-ttu-id="8d767-514">Для объекта AzureVMpolicy добавлен новый атрибут — ProtectedItemsCount.</span><span class="sxs-lookup"><span data-stu-id="8d767-514">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="8d767-515">Добавлены тесты для политики виртуальной машины и восстановления исходной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="8d767-515">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d767-516">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d767-516">Az.Resources</span></span>
* <span data-ttu-id="8d767-517">Исправлена ошибка, при которой не удавалось вызвать командлет New-AzRoleAssignment без параметра Scope.</span><span class="sxs-lookup"><span data-stu-id="8d767-517">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8d767-518">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8d767-518">Az.ServiceFabric</span></span>
* <span data-ttu-id="8d767-519">Исправлена опечатка в примере в справочной документации по командлету Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="8d767-519">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="8d767-520">Добавлены новые командлеты для управления приложениями и службами:</span><span class="sxs-lookup"><span data-stu-id="8d767-520">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="8d767-521">New-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="8d767-521">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="8d767-522">New-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="8d767-522">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="8d767-523">New-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="8d767-523">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="8d767-524">New-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="8d767-524">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="8d767-525">Update-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="8d767-525">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="8d767-526">Get-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="8d767-526">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="8d767-527">Get-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="8d767-527">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="8d767-528">Get-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="8d767-528">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="8d767-529">Get-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="8d767-529">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="8d767-530">Remove-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="8d767-530">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="8d767-531">Remove-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="8d767-531">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="8d767-532">Remove-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="8d767-532">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="8d767-533">Remove-AzServiceFabricServic.</span><span class="sxs-lookup"><span data-stu-id="8d767-533">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="8d767-534">Пакет SDK для Service Fabric обновлен до версии 1.2.0, в которой используется версия API 2019-03-01 поставщика ресурсов Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="8d767-534">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="8d767-535">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="8d767-535">Az.SignalR</span></span>
* <span data-ttu-id="8d767-536">Добавлены командлеты Update, Restart, CheckNameAvailability и GetUsage.</span><span class="sxs-lookup"><span data-stu-id="8d767-536">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d767-537">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d767-537">Az.Sql</span></span>
* <span data-ttu-id="8d767-538">Обновлен пример в справочной документации по командлету Get-AzSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="8d767-538">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="8d767-539">Добавлен пример виртуального ядра для командлета создания эластичного пула (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="8d767-539">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="8d767-540">Удалена проверка свойства EmailAddresses и того, что свойство EmailAdmins правильное в случае, если свойство EmailAddresses пустое в командлетах Set-AzSqlServerAdvancedThreatProtectionPolicy и Set-AzSqlDatabaseAdvancedThreatProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="8d767-540">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="8d767-541">Теперь, если существует несколько параметров диагностики, включающих категорию аудита, параметры аудита сервера и базы данных удаляются.</span><span class="sxs-lookup"><span data-stu-id="8d767-541">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="8d767-542">Исправлена проверка адресов электронной почты в нескольких командлетах оценки уязвимостей SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting и Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="8d767-542">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d767-543">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d767-543">Az.Storage</span></span>
* <span data-ttu-id="8d767-544">Обновлен пример в справочной документации по командлету Get-AzStorageAccountKey.</span><span class="sxs-lookup"><span data-stu-id="8d767-544">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="8d767-545">Теперь при отправке и загрузке файла Azure в конечном файле сохраняются свойства SMB исходного файла (атрибуты файла, время создания файла, время последней записи файла).</span><span class="sxs-lookup"><span data-stu-id="8d767-545">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="8d767-546">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8d767-546">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="8d767-547">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8d767-547">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="8d767-548">Исправлена операция отправки блочного BLOB-объекта, в которой происходили сбои свойств и метаданных в контейнере с включенной ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="8d767-548">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="8d767-549">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8d767-549">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="8d767-550">Добавлена поддержка управления общими папками Azure в API плоскости управления с помощью таких командлетов:</span><span class="sxs-lookup"><span data-stu-id="8d767-550">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="8d767-551">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="8d767-551">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="8d767-552">Get-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="8d767-552">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="8d767-553">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="8d767-553">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="8d767-554">Remove-AzRmStorageShare.</span><span class="sxs-lookup"><span data-stu-id="8d767-554">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8d767-555">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d767-555">Az.Websites</span></span>
* <span data-ttu-id="8d767-556">Устранена проблема, из-за которой теги webapp удалялись при переносе приложения в новый ASP.</span><span class="sxs-lookup"><span data-stu-id="8d767-556">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="8d767-557">Теперь командлет Publish-AzureWebapp работает в Linux и Windows.</span><span class="sxs-lookup"><span data-stu-id="8d767-557">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="8d767-558">Обновлен пример в справочной документации по командлету Get-AzWebAppPublishingProfile.</span><span class="sxs-lookup"><span data-stu-id="8d767-558">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="8d767-559">2.6.0 — август 2019 г.</span><span class="sxs-lookup"><span data-stu-id="8d767-559">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="8d767-560">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="8d767-560">General</span></span>
* <span data-ttu-id="8d767-561">Исправлены опечатки в модулях.</span><span class="sxs-lookup"><span data-stu-id="8d767-561">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8d767-562">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d767-562">Az.Accounts</span></span>
* <span data-ttu-id="8d767-563">Добавлена поддержка назначаемого пользователем удостоверения MSI при проверке подлинности в Функциях Azure (№ 9479).</span><span class="sxs-lookup"><span data-stu-id="8d767-563">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="8d767-564">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="8d767-564">Az.Aks</span></span>
* <span data-ttu-id="8d767-565">Устранена проблема с выходными данными для Get-AzAks.</span><span class="sxs-lookup"><span data-stu-id="8d767-565">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="8d767-566">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9847.</span><span class="sxs-lookup"><span data-stu-id="8d767-566">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="8d767-567">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8d767-567">Az.ApiManagement</span></span>
* <span data-ttu-id="8d767-568">исправлена проблема https://github.com/Azure/azure-powershell/issues/9351.</span><span class="sxs-lookup"><span data-stu-id="8d767-568">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="8d767-569">Обновлена версия NuGet для .NET, которая не накладывает ограничений на productId, apiId, groupId и userId.</span><span class="sxs-lookup"><span data-stu-id="8d767-569">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="8d767-570">**Get-AzApiManagementProduct**. Добавлена поддержка запросов к продуктам с помощью API.</span><span class="sxs-lookup"><span data-stu-id="8d767-570">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="8d767-571">**New-AzApiManagementApiRevision**. Устранена проблема, из-за которой не задавался параметр ApiRevisionDescription при создании новой редакции API https://github.com/Azure/azure-powershell/issues/9752.</span><span class="sxs-lookup"><span data-stu-id="8d767-571">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="8d767-572">Исправлено написание имени модели c PsApiManagementOAuth2AuthrozationServer на PsApiManagementOAuth2AuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="8d767-572">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="8d767-573">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8d767-573">Az.Batch</span></span>
* <span data-ttu-id="8d767-574">Исправлена опечатка в написании Windows со строчной буквы в справочных сообщениях и документации.</span><span class="sxs-lookup"><span data-stu-id="8d767-574">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8d767-575">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8d767-575">Az.Cdn</span></span>
* <span data-ttu-id="8d767-576">Исправлена опечатка во вспомогательном приложении модуля CDN.</span><span class="sxs-lookup"><span data-stu-id="8d767-576">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d767-577">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d767-577">Az.Compute</span></span>
* <span data-ttu-id="8d767-578">Добавлен параметр VmssId в новый командлет Add New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="8d767-578">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="8d767-579">Добавлены параметры TerminateScheduledEvents и TerminateScheduledEventNotBeforeTimeoutInMinutes в New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="8d767-579">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="8d767-580">Добавлено свойство HyperVGeneration в объект образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8d767-580">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="8d767-581">Добавлены компоненты Host и HostGroup.</span><span class="sxs-lookup"><span data-stu-id="8d767-581">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="8d767-582">Новые командлеты:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="8d767-582">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="8d767-583">Параметр HostId добавлен в New-AzVMConfig и New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="8d767-583">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="8d767-584">Исправлен пример в документации по Invoke-AzVMRunCommand, в котором теперь используется правильное имя параметра.</span><span class="sxs-lookup"><span data-stu-id="8d767-584">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="8d767-585">Исправлено описание VolumeType в справочной документации по Set-AzVMDiskEncryptionExtension и Set-AzVmssDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="8d767-585">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8d767-586">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8d767-586">Az.DataFactory</span></span>
* <span data-ttu-id="8d767-587">Исправлена опечатка в написании Windows со строчной буквы в документации по New-AzDataFactoryEncryptValue.</span><span class="sxs-lookup"><span data-stu-id="8d767-587">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="8d767-588">Пакет SDK ADF для .NET обновлен до версии 4.1.2.</span><span class="sxs-lookup"><span data-stu-id="8d767-588">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="8d767-589">Добавлены параметры DataProxyIntegrationRuntimeName, DataProxyStagingLinkedServiceName и DataProxyStagingPath в командлет Set-AzureRmDataFactoryV2IntegrationRuntime, что позволяет настраивать локальную среду выполнения интеграции в качестве прокси-сервера для Azure-SSIS Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="8d767-589">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="8d767-590">Обновлены PSTriggerRun для отображения активированных конвейеров, сообщений и свойств и PSActivityRun для отображения типа действия.</span><span class="sxs-lookup"><span data-stu-id="8d767-590">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8d767-591">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8d767-591">Az.DataLakeStore</span></span>
* <span data-ttu-id="8d767-592">Устранена проблема, при которой Get-DataLakeStoreDeletedItem переставал отвечать на запросы при возникновении ошибок или удаленных исключений.</span><span class="sxs-lookup"><span data-stu-id="8d767-592">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8d767-593">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8d767-593">Az.EventHub</span></span>
* <span data-ttu-id="8d767-594">Исправлена проблема № 9658: опечатка в написании параметра VirtualNteworkRule у Set-AzEventHubNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="8d767-594">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="8d767-595">Исправлена проблема № 9558: в Set-AzEventHubNamespace используется PATCH вместо PUT.</span><span class="sxs-lookup"><span data-stu-id="8d767-595">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="8d767-596">В командлет Set-AzEventHubNamespace добавлен параметр EnableKafka.</span><span class="sxs-lookup"><span data-stu-id="8d767-596">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="8d767-597">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="8d767-597">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="8d767-598">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="8d767-598">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="8d767-599">Исправлено написание Azure со строчной буквы.</span><span class="sxs-lookup"><span data-stu-id="8d767-599">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8d767-600">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8d767-600">Az.Monitor</span></span>
* <span data-ttu-id="8d767-601">Исправлены неправильные имена параметров в справочной документации.</span><span class="sxs-lookup"><span data-stu-id="8d767-601">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d767-602">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d767-602">Az.Network</span></span>
* <span data-ttu-id="8d767-603">Обновлен New-AzPrivateLinkServiceIpConfig.</span><span class="sxs-lookup"><span data-stu-id="8d767-603">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="8d767-604">Параметр PublicIpAddress объявлен нерекомендуемым, так как он не используется на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="8d767-604">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="8d767-605">Добавлен необязательный параметр Primary, указывающий, является ли текущая IP-конфигурация основной.</span><span class="sxs-lookup"><span data-stu-id="8d767-605">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="8d767-606">Улучшена обработка исключений из-за ошибок запроса от пакета SDK. Устранена проблема, при которой исключения пакета SDK не обрабатывались правильно, из-за чего не отображались основные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="8d767-606">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="8d767-607">Настроена логика проверки для префикса IPv6 IP-адреса для проверки правильности длины префикса IPv6.</span><span class="sxs-lookup"><span data-stu-id="8d767-607">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="8d767-608">Обновлен Get-AzVirtualNetworkSubnetConfig: добавлен набор параметров для получения по идентификатору ресурса подсети.</span><span class="sxs-lookup"><span data-stu-id="8d767-608">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="8d767-609">Обновлено описание параметра Location для AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="8d767-609">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8d767-610">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8d767-610">Az.OperationalInsights</span></span>
* <span data-ttu-id="8d767-611">Обновлена документация по New-AzOperationalInsightsLinuxSyslogDataSource.</span><span class="sxs-lookup"><span data-stu-id="8d767-611">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="8d767-612">Добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="8d767-612">Added example</span></span>
    - <span data-ttu-id="8d767-613">Обновлено описание параметра -Name.</span><span class="sxs-lookup"><span data-stu-id="8d767-613">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="8d767-614">Добавлен пример для New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="8d767-614">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="8d767-615">Изменено описание параметра -Name для New-AzOperationalInsightsWindowsEventDataSource.</span><span class="sxs-lookup"><span data-stu-id="8d767-615">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8d767-616">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d767-616">Az.RecoveryServices</span></span>
* <span data-ttu-id="8d767-617">Обновлен Get-AzRecoveryServicesBackupJobDetail.md.</span><span class="sxs-lookup"><span data-stu-id="8d767-617">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d767-618">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d767-618">Az.Resources</span></span>
* <span data-ttu-id="8d767-619">Добавлена поддержка новой версии API 2019-05-10 для Microsoft.Resource.</span><span class="sxs-lookup"><span data-stu-id="8d767-619">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="8d767-620">Добавлена поддержка copy.count = 0 для переменных, ресурсов и свойств.</span><span class="sxs-lookup"><span data-stu-id="8d767-620">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="8d767-621">Ресурсы, у которых condition = false или copy.count = 0, будут удаляться в полном режиме.</span><span class="sxs-lookup"><span data-stu-id="8d767-621">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="8d767-622">В справочную документацию добавлен пример назначения политики на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="8d767-622">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8d767-623">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8d767-623">Az.ServiceBus</span></span>
* <span data-ttu-id="8d767-624">Исправлена проблема № 9658: опечатка в написании параметра VirtualNetworkRule В Set-AzServiceBusNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="8d767-624">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="8d767-625">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="8d767-625">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="8d767-626">Добавлена новая команда Test-AzServiceBusNameAvailability для проверки доступности имени для очереди и раздела.</span><span class="sxs-lookup"><span data-stu-id="8d767-626">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="8d767-627">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8d767-627">Az.ServiceFabric</span></span>
* <span data-ttu-id="8d767-628">Устранены ошибки командлета для добавления типа узла:</span><span class="sxs-lookup"><span data-stu-id="8d767-628">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="8d767-629">ошибка NullReferenceException, возникавшая, если у группы ресурсов были другие VMSS, не связанные с кластером Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="8d767-629">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="8d767-630">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8681.</span><span class="sxs-lookup"><span data-stu-id="8d767-630">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="8d767-631">Исправлена ошибка, из-за которой командлет завершился сбоем, если virtualNetwork находилась не в той группе ресурсов, к которой относится кластер.</span><span class="sxs-lookup"><span data-stu-id="8d767-631">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="8d767-632">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8407.</span><span class="sxs-lookup"><span data-stu-id="8d767-632">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="8d767-633">Командлет Add-AzServiceFabricApplicationCertificate объявлен нерекомендуемым.</span><span class="sxs-lookup"><span data-stu-id="8d767-633">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d767-634">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d767-634">Az.Sql</span></span>
* <span data-ttu-id="8d767-635">Обновление документации по старым командлетам аудита.</span><span class="sxs-lookup"><span data-stu-id="8d767-635">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d767-636">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d767-636">Az.Storage</span></span>
* <span data-ttu-id="8d767-637">Обновлена справка по Get/Close-AzStorageFileHandle: в примеры добавлены сценарии использования командлетов и обновлено описание параметров.</span><span class="sxs-lookup"><span data-stu-id="8d767-637">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="8d767-638">Добавлена поддержка StandardBlobTier в операции отправки BLOB-объекта и копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="8d767-638">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="8d767-639">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8d767-639">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="8d767-640">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="8d767-640">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="8d767-641">Добавлена поддержка приоритета восстановления в операцию копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="8d767-641">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="8d767-642">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="8d767-642">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8d767-643">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d767-643">Az.Websites</span></span>
* <span data-ttu-id="8d767-644">Добавлены уточнение для параметра -AppSettings в Set-AzWebApp и Set-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="8d767-644">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="8d767-645">2.5.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="8d767-645">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8d767-646">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d767-646">Az.Accounts</span></span>
* <span data-ttu-id="8d767-647">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8d767-647">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="8d767-648">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="8d767-648">Az.ApplicationInsights</span></span>
* <span data-ttu-id="8d767-649">Исправлена опечатка в примере в документации по Remove-AzApplicationInsightsApiKey.</span><span class="sxs-lookup"><span data-stu-id="8d767-649">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="8d767-650">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8d767-650">Az.Automation</span></span>
* <span data-ttu-id="8d767-651">Исправлена опечатка в строке ресурса.</span><span class="sxs-lookup"><span data-stu-id="8d767-651">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="8d767-652">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8d767-652">Az.CognitiveServices</span></span>
* <span data-ttu-id="8d767-653">Добавлена поддержка NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="8d767-653">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d767-654">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d767-654">Az.Compute</span></span>
* <span data-ttu-id="8d767-655">Добавлены недостающие свойства (ComputerName, OsName, OsVersion и HyperVGeneration) для объекта представления экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8d767-655">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="8d767-656">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8d767-656">Az.ContainerRegistry</span></span>
* <span data-ttu-id="8d767-657">Исправлена опечатка в Remove-AzContainerRegistryReplication для параметра репликации.</span><span class="sxs-lookup"><span data-stu-id="8d767-657">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="8d767-658">См. подробнее: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="8d767-658">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8d767-659">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8d767-659">Az.DataFactory</span></span>
* <span data-ttu-id="8d767-660">Пакет SDK для ADF .NET обновлен до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="8d767-660">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="8d767-661">Исправлена опечатка в документации по Get-AzDataFactoryV2PipelineRun.</span><span class="sxs-lookup"><span data-stu-id="8d767-661">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8d767-662">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8d767-662">Az.EventHub</span></span>
* <span data-ttu-id="8d767-663">Добавлен новый командлет для создания маркера SAS: New-AzEventHubAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="8d767-663">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="8d767-664">Добавлена проверка и сообщение об ошибке для случаев, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="8d767-664">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8d767-665">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8d767-665">Az.KeyVault</span></span>
* <span data-ttu-id="8d767-666">Добавлена поддержка для настройки параметра KeySize в политиках сертификатов.</span><span class="sxs-lookup"><span data-stu-id="8d767-666">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8d767-667">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8d767-667">Az.LogicApp</span></span>
* <span data-ttu-id="8d767-668">Get-AzIntegrationAccountMap теперь надлежащим образом выводит все типы сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="8d767-668">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="8d767-669">Добавлен новый параметр MapType для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="8d767-669">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="8d767-670">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="8d767-670">Az.ManagedServices</span></span>
* <span data-ttu-id="8d767-671">Добавлена поддержка API версии 2019-06-01 (общедоступная).</span><span class="sxs-lookup"><span data-stu-id="8d767-671">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d767-672">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d767-672">Az.Network</span></span>
* <span data-ttu-id="8d767-673">Добавлена поддержка частной конечной точки и службы приватного канала.</span><span class="sxs-lookup"><span data-stu-id="8d767-673">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="8d767-674">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="8d767-674">New cmdlets</span></span>
        - <span data-ttu-id="8d767-675">Set-AzPrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="8d767-675">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="8d767-676">Set-AzPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="8d767-676">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="8d767-677">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="8d767-677">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8d767-678">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="8d767-678">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8d767-679">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="8d767-679">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8d767-680">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="8d767-680">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8d767-681">Test-AzPrivateLinkServiceVisibility.</span><span class="sxs-lookup"><span data-stu-id="8d767-681">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="8d767-682">Get-AzAutoApprovedPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="8d767-682">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="8d767-683">Обновлены следующие команды для функции: Флаг PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies в подсети в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="8d767-683">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="8d767-684">Обновлены командлеты New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig.</span><span class="sxs-lookup"><span data-stu-id="8d767-684">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="8d767-685">Добавлен необязательный параметр -PrivateEndpointNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к частной конечной точке в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="8d767-685">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="8d767-686">Добавлен необязательный параметр -PrivateLinkServiceNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к службе приватного канала в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="8d767-686">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="8d767-687">Параметр ServiceName командлета AzPrivateLinkService был переименован на Name с псевдонимом ServiceName для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="8d767-687">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="8d767-688">Включен протокол ICMP для настройки правил безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="8d767-688">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="8d767-689">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="8d767-689">Updated cmdlets</span></span>
        - <span data-ttu-id="8d767-690">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="8d767-690">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="8d767-691">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="8d767-691">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="8d767-692">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="8d767-692">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="8d767-693">Добавлен ConnectionProtocolType (Ikev1/Ikev2) в качестве настраиваемого параметра для командлета New-AzVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="8d767-693">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="8d767-694">Добавлен PrivateIpAddressVersion в LoadBalancerFrontendIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="8d767-694">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="8d767-695">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="8d767-695">Updated cmdlet:</span></span>
        - <span data-ttu-id="8d767-696">New-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="8d767-696">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="8d767-697">Add-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="8d767-697">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="8d767-698">Set-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="8d767-698">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="8d767-699">Команда New-AzApplicationGatewayProbeConfig Шлюза приложений обновлена для поддержки настраиваемого порта в зонде.</span><span class="sxs-lookup"><span data-stu-id="8d767-699">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="8d767-700">Обновлен командлет New-AzApplicationGatewayProbeConfig: добавлен необязательный параметр Port, который используется при проверке внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="8d767-700">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="8d767-701">Этот параметр применяется к номерам SKU Standard_V2 и WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="8d767-701">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8d767-702">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8d767-702">Az.OperationalInsights</span></span>
* <span data-ttu-id="8d767-703">Обновленная версия по умолчанию для сохраненных операций поиска имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="8d767-703">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="8d767-704">Исправлены ошибки при обработке регулярных выражений со значениями NULL в журналах.</span><span class="sxs-lookup"><span data-stu-id="8d767-704">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8d767-705">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d767-705">Az.RecoveryServices</span></span>
* <span data-ttu-id="8d767-706">Обновлен файл Get-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="8d767-706">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="8d767-707">Обновлен файл Get-AzRecoveryServicesBackupContainer.md.</span><span class="sxs-lookup"><span data-stu-id="8d767-707">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="8d767-708">Обновлен файл Get-AzRecoveryServicesVault.md.</span><span class="sxs-lookup"><span data-stu-id="8d767-708">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="8d767-709">Обновлен файл Wait-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="8d767-709">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="8d767-710">Обновлен файл Set-AzRecoveryServicesVaultContext.md.</span><span class="sxs-lookup"><span data-stu-id="8d767-710">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="8d767-711">Обновлен файл Get-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="8d767-711">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="8d767-712">Обновлен файл Get-AzRecoveryServicesBackupRecoveryPoint.md.</span><span class="sxs-lookup"><span data-stu-id="8d767-712">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="8d767-713">Обновлен файл Restore-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="8d767-713">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="8d767-714">Обновлен вызов службы для отмены регистрации контейнера в общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="8d767-714">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="8d767-715">Обновлен файл Set-AzRecoveryServicesAsrAlertSetting.md.</span><span class="sxs-lookup"><span data-stu-id="8d767-715">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d767-716">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d767-716">Az.Resources</span></span>
- <span data-ttu-id="8d767-717">Удален отсутствующий командлет, который упоминается в документации по New-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="8d767-717">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="8d767-718">Обновлены командлеты политик для использования новой версии API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="8d767-718">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8d767-719">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8d767-719">Az.ServiceBus</span></span>
* <span data-ttu-id="8d767-720">Добавлен новый командлет для создания маркера SAS: New-AzServiceBusAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="8d767-720">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="8d767-721">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="8d767-721">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d767-722">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d767-722">Az.Sql</span></span>
* <span data-ttu-id="8d767-723">Исправлены отсутствующие примеры для командлета Set-AzSqlDatabaseSecondary.</span><span class="sxs-lookup"><span data-stu-id="8d767-723">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="8d767-724">Исправлены заданные повторяющиеся проверки для оценки наличия уязвимостей без указания адресов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="8d767-724">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="8d767-725">Исправлена незначительная опечатка в сообщении предупреждения.</span><span class="sxs-lookup"><span data-stu-id="8d767-725">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d767-726">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d767-726">Az.Storage</span></span>
* <span data-ttu-id="8d767-727">Обновлен пример в справочной документации для использования командлетом Get-AzStorageAccount правильного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="8d767-727">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="8d767-728">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="8d767-728">Az.StorageSync</span></span>
* <span data-ttu-id="8d767-729">Добавлен командлет Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="8d767-729">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="8d767-730">Исправлена проблема № 9551, связанная с TierFilesOlderThanDays.</span><span class="sxs-lookup"><span data-stu-id="8d767-730">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8d767-731">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d767-731">Az.Websites</span></span>
* <span data-ttu-id="8d767-732">Исправлена ошибка, при которой некоторые свойства SiteConfig не возвращались Get-AzWebApp и Set-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="8d767-732">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="8d767-733">Добавлен новый параметр Location в Get-AzDeletedWebApp и Restore-AzDeletedWebApp.</span><span class="sxs-lookup"><span data-stu-id="8d767-733">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="8d767-734">Исправлена ошибка, которая возникала при клонировании слотов веб-приложений с помощью командлета New-AzWebApp-IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="8d767-734">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="8d767-735">2.4.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="8d767-735">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8d767-736">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d767-736">Az.Accounts</span></span>
* <span data-ttu-id="8d767-737">Добавлена поддержка командлетов профиля.</span><span class="sxs-lookup"><span data-stu-id="8d767-737">Add support for profile cmdlets</span></span>
* <span data-ttu-id="8d767-738">Добавлена поддержка сред и плоскостей данных в созданных командлетах.</span><span class="sxs-lookup"><span data-stu-id="8d767-738">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="8d767-739">Исправлена ошибка, когда в командлетах плоскости данных в Windows PowerShell в некоторых случаях использовалась неправильная конечная точка.</span><span class="sxs-lookup"><span data-stu-id="8d767-739">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="8d767-740">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="8d767-740">Az.Advisor</span></span>
* <span data-ttu-id="8d767-741">Выпущена общедоступная версия Az.Advisor.</span><span class="sxs-lookup"><span data-stu-id="8d767-741">GA release of Az.Advisor</span></span>
* <span data-ttu-id="8d767-742">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="8d767-742">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="8d767-743">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8d767-743">Az.ApiManagement</span></span>
* <span data-ttu-id="8d767-744">исправлена проблема https://github.com/Azure/azure-powershell/issues/8671.</span><span class="sxs-lookup"><span data-stu-id="8d767-744">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="8d767-745">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="8d767-745">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="8d767-746">Добавлена поддержка запрашивания подписок по пользователю и продукту.</span><span class="sxs-lookup"><span data-stu-id="8d767-746">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="8d767-747">Добавлена поддержка создания запросов с использованием области "/", "/apis", "/apis/echo-api".</span><span class="sxs-lookup"><span data-stu-id="8d767-747">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="8d767-748">Исправлены проблемы https://github.com/Azure/azure-powershell/issues/9307 и https://github.com/Azure/azure-powershell/issues/8432.</span><span class="sxs-lookup"><span data-stu-id="8d767-748">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="8d767-749">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="8d767-749">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="8d767-750">Добавлена поддержка указания ApiVersion и ApiVersionSetId при импорте API-интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="8d767-750">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8d767-751">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8d767-751">Az.Automation</span></span>
* <span data-ttu-id="8d767-752">Исправлена ошибка командлета Set-AzAutomationConnectionFieldValue при обработке строкового значения.</span><span class="sxs-lookup"><span data-stu-id="8d767-752">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d767-753">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d767-753">Az.Compute</span></span>
* <span data-ttu-id="8d767-754">В New AzImageConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="8d767-754">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8d767-755">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8d767-755">Az.DataFactory</span></span>
* <span data-ttu-id="8d767-756">Обновление выходных данных командлетов ADF, предназначенных для получения числа выполнений действий, конвейеров и триггеров, для поддержки канала Select-Object.</span><span class="sxs-lookup"><span data-stu-id="8d767-756">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8d767-757">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8d767-757">Az.EventGrid</span></span>
* <span data-ttu-id="8d767-758">Исправлена опечатка в документации по командлету New-AzEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="8d767-758">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8d767-759">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8d767-759">Az.IotHub</span></span>
* <span data-ttu-id="8d767-760">Добавлена поддержка повторного создания ключей политики авторизации.</span><span class="sxs-lookup"><span data-stu-id="8d767-760">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d767-761">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d767-761">Az.Network</span></span>
* <span data-ttu-id="8d767-762">К тегам общедоступного IP-адреса добавлен тег RoutingPreference.</span><span class="sxs-lookup"><span data-stu-id="8d767-762">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="8d767-763">Улучшены примеры для справочной документации по командлету Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="8d767-763">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8d767-764">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8d767-764">Az.PolicyInsights</span></span>
* <span data-ttu-id="8d767-765">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="8d767-765">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="8d767-766">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9446.</span><span class="sxs-lookup"><span data-stu-id="8d767-766">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8d767-767">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8d767-767">Az.OperationalInsights</span></span>
* <span data-ttu-id="8d767-768">Исправленная модель источника данных CustomLog возвращена в командлет Get-AzOperationalInsightsDataSource.</span><span class="sxs-lookup"><span data-stu-id="8d767-768">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8d767-769">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d767-769">Az.RecoveryServices</span></span>
* <span data-ttu-id="8d767-770">Выпущено исправление для команды get-policy для виртуальных машин IaaS.</span><span class="sxs-lookup"><span data-stu-id="8d767-770">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d767-771">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d767-771">Az.Resources</span></span>
    - <span data-ttu-id="8d767-772">Исправлен текст справки по параметру Get-AzPolicyState -Top.</span><span class="sxs-lookup"><span data-stu-id="8d767-772">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="8d767-773">Добавлена поддержка разбиения по страницам на стороне клиента для Get-AzPolicyAlias.</span><span class="sxs-lookup"><span data-stu-id="8d767-773">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="8d767-774">Добавлены новые параметры для Set-AzPolicyAssignment, -PolicyParameters и -PolicyParametersObject.</span><span class="sxs-lookup"><span data-stu-id="8d767-774">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="8d767-775">Добавлен ряд обновлений документов и примеров для командлетов политик.</span><span class="sxs-lookup"><span data-stu-id="8d767-775">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8d767-776">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8d767-776">Az.ServiceBus</span></span>
* <span data-ttu-id="8d767-777">Исправление ошибки № 4938: командлет New-AzureRmServiceBusQueue возвращает ответ BadRequest (Недопустимый запрос) при задании значения MaxSizeInMegabytes.</span><span class="sxs-lookup"><span data-stu-id="8d767-777">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d767-778">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d767-778">Az.Sql</span></span>
* <span data-ttu-id="8d767-779">Из выпуска предварительной версии в выпуск общедоступной версии добавлены командлеты группы отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="8d767-779">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="8d767-780">Поддержка аудита Azure SQL Server и баз данных с помощью новых командлетов:</span><span class="sxs-lookup"><span data-stu-id="8d767-780">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="8d767-781">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="8d767-781">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="8d767-782">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="8d767-782">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="8d767-783">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="8d767-783">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="8d767-784">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="8d767-784">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="8d767-785">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="8d767-785">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="8d767-786">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="8d767-786">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="8d767-787">Из параметров оценки уязвимостей удалены ограничения, касающиеся электронной почты.</span><span class="sxs-lookup"><span data-stu-id="8d767-787">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d767-788">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d767-788">Az.Storage</span></span>
* <span data-ttu-id="8d767-789">Два параметра в указанном ниже командлете — -IndexDocument и -ErrorDocument404Path, — которые ранее были обязательными, стали необязательными:</span><span class="sxs-lookup"><span data-stu-id="8d767-789">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="8d767-790">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="8d767-790">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="8d767-791">Обновлена справка по командлету Get-AzStorageBlobContent: добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="8d767-791">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="8d767-792">При сбое выполнения командлета с ошибкой StorageException отображаются дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="8d767-792">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="8d767-793">Добавлена поддержка создания или обновления учетной записи хранения с использованием проверки подлинности AAD DS для службы "Файлы Azure".</span><span class="sxs-lookup"><span data-stu-id="8d767-793">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="8d767-794">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8d767-794">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="8d767-795">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8d767-795">Set-AzStorageAccount</span></span>
* <span data-ttu-id="8d767-796">Добавлена поддержка перечисления или закрытия дескрипторов файлов для общей папки, каталога файлов или файла:</span><span class="sxs-lookup"><span data-stu-id="8d767-796">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="8d767-797">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="8d767-797">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="8d767-798">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="8d767-798">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="8d767-799">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="8d767-799">Az.StorageSync</span></span>
* <span data-ttu-id="8d767-800">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="8d767-800">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="8d767-801">2.3.2 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="8d767-801">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8d767-802">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d767-802">Az.Accounts</span></span>
* <span data-ttu-id="8d767-803">Исправлена ошибка, связанная с использованием неправильного URL-адреса для вызовов функций.</span><span class="sxs-lookup"><span data-stu-id="8d767-803">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="8d767-804">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8983.</span><span class="sxs-lookup"><span data-stu-id="8d767-804">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="8d767-805">Устранена проблема с псевдонимами из AzureRM для командлетов Az.</span><span class="sxs-lookup"><span data-stu-id="8d767-805">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="8d767-806">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="8d767-806">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="8d767-807">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest.</span><span class="sxs-lookup"><span data-stu-id="8d767-807">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d767-808">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d767-808">Az.Compute</span></span>
* <span data-ttu-id="8d767-809">Простые наборы параметров New-AzVm и New-AzVmss теперь принимают параметр ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="8d767-809">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="8d767-810">Исправлена опечатка в справочной документации по New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="8d767-810">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="8d767-811">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="8d767-811">Az.Dns</span></span>
* <span data-ttu-id="8d767-812">Исправлена опечатка в справочных примерах по использованию Set-AzDnsZone.</span><span class="sxs-lookup"><span data-stu-id="8d767-812">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8d767-813">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8d767-813">Az.EventGrid</span></span>
* <span data-ttu-id="8d767-814">Обновлен для использования API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="8d767-814">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="8d767-815">Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="8d767-815">New cmdlets:</span></span>
    - <span data-ttu-id="8d767-816">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="8d767-816">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="8d767-817">Создает домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="8d767-817">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="8d767-818">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="8d767-818">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="8d767-819">Возвращает сведения о домене Сетки событий или список всех доменов Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="8d767-819">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="8d767-820">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="8d767-820">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="8d767-821">Удаляет домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="8d767-821">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="8d767-822">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="8d767-822">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="8d767-823">Повторно создает ключ общего доступа для домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="8d767-823">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="8d767-824">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="8d767-824">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="8d767-825">Возвращает ключи общего доступа, используемые для публикации событий в домене Сетки событий.</span><span class="sxs-lookup"><span data-stu-id="8d767-825">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="8d767-826">New-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="8d767-826">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="8d767-827">Создает раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="8d767-827">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="8d767-828">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="8d767-828">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="8d767-829">Возвращает сведения о разделе домена Сетки событий или список всех разделов определенного домена Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="8d767-829">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="8d767-830">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="8d767-830">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="8d767-831">Удаляет раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="8d767-831">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="8d767-832">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="8d767-832">Updated cmdlets:</span></span>
    - <span data-ttu-id="8d767-833">New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="8d767-833">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="8d767-834">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для нового домена Сетки событий и раздела домена Сетки событий и позволяющие создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="8d767-834">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="8d767-835">Добавляют новые обязательные параметры для указания имени нового домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="8d767-835">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="8d767-836">Добавляют новые наборы параметров для доменов и разделов домена и позволяют повторно использовать существующие параметры (например, EndPointType, SubjectBeginsWith и т. д.).</span><span class="sxs-lookup"><span data-stu-id="8d767-836">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="8d767-837">Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="8d767-837">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="8d767-838">срока действия подписки на событие;</span><span class="sxs-lookup"><span data-stu-id="8d767-838">Event subscription expiration date,</span></span>
            - <span data-ttu-id="8d767-839">параметров расширенной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="8d767-839">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="8d767-840">Добавляют новое перечисление для ServiceBusQueue в качестве места назначения.</span><span class="sxs-lookup"><span data-stu-id="8d767-840">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="8d767-841">Запрещают использование значение All в параметре -IncludedEventType и заменяют его следующим:</span><span class="sxs-lookup"><span data-stu-id="8d767-841">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="8d767-842">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="8d767-842">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="8d767-843">Добавляют новые необязательные параметры (Top, ODataQuery и NextLink) для поддержки разбиения на страницы и фильтрации результатов.</span><span class="sxs-lookup"><span data-stu-id="8d767-843">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="8d767-844">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="8d767-844">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="8d767-845">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для домена Сетки событий и раздела домена Сетки событий и позволяющие удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="8d767-845">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="8d767-846">Добавляют новые обязательные параметры для указания имени домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="8d767-846">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8d767-847">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8d767-847">Az.FrontDoor</span></span>
* <span data-ttu-id="8d767-848">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="8d767-848">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="8d767-849">Добавляет поддержку преобразований и новое значение оператора автозавершения (RegEx).</span><span class="sxs-lookup"><span data-stu-id="8d767-849">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="8d767-850">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="8d767-850">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="8d767-851">Добавляет новые значения автозавершения.</span><span class="sxs-lookup"><span data-stu-id="8d767-851">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d767-852">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d767-852">Az.Network</span></span>
* <span data-ttu-id="8d767-853">Добавляет поддержку ресурса шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="8d767-853">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="8d767-854">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="8d767-854">New cmdlets</span></span>
        - <span data-ttu-id="8d767-855">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="8d767-855">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="8d767-856">Добавляет AvailablePrivateEndpointType.</span><span class="sxs-lookup"><span data-stu-id="8d767-856">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="8d767-857">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="8d767-857">New cmdlets</span></span> 
        - <span data-ttu-id="8d767-858">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="8d767-858">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="8d767-859">Добавляет PrivatePrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="8d767-859">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="8d767-860">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="8d767-860">New cmdlets</span></span> 
        - <span data-ttu-id="8d767-861">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8d767-861">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="8d767-862">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8d767-862">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="8d767-863">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8d767-863">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="8d767-864">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="8d767-864">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="8d767-865">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8d767-865">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="8d767-866">Добавляет PrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="8d767-866">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="8d767-867">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="8d767-867">New cmdlets</span></span>
        - <span data-ttu-id="8d767-868">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8d767-868">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="8d767-869">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8d767-869">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="8d767-870">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8d767-870">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="8d767-871">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="8d767-871">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="8d767-872">Обновлены следующие команды для функции: флаг UseLocalAzureIpAddress для VPN-подключения.</span><span class="sxs-lookup"><span data-stu-id="8d767-872">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="8d767-873">Обновлен командлет New-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="8d767-873">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="8d767-874">Обновлен командлет Set-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="8d767-874">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="8d767-875">В пиринг ExpressRoute добавлено поле только для чтения PeeredConnections.</span><span class="sxs-lookup"><span data-stu-id="8d767-875">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="8d767-876">В ExpressRoute добавлено поле только для чтения GlobalReachEnabled.</span><span class="sxs-lookup"><span data-stu-id="8d767-876">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="8d767-877">Добавлен атрибут в рамках критического изменения, отменяющего статус устаревшего поля AllowGlobalReach в модели ExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="8d767-877">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="8d767-878">Исправлена проблема, связанная с ошибкой 8756, при использовании TargetListenerID с командлетами AzApplicationGatewayRedirectConfiguration.</span><span class="sxs-lookup"><span data-stu-id="8d767-878">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="8d767-879">Исправлена ошибка в New-AzApplicationGatewayPathRuleConfig, не позволявшая задавать набор правил повторного создания.</span><span class="sxs-lookup"><span data-stu-id="8d767-879">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="8d767-880">Исправлено отображение VirtualNetworkTaps в NetworkInterfaceIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="8d767-880">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="8d767-881">Исправлены командлеты Cortex Get для отображения всех частей.</span><span class="sxs-lookup"><span data-stu-id="8d767-881">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="8d767-882">Исправлено создание ссылок VirtualHub для ExpressRouteGateways и VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="8d767-882">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="8d767-883">В AzureFirewall и NatGateway добавлена поддержка Зон доступности.</span><span class="sxs-lookup"><span data-stu-id="8d767-883">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="8d767-884">Добавлен командлет Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="8d767-884">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="8d767-885">Добавлена поддержка нескольких общедоступных IP-адресов для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="8d767-885">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="8d767-886">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="8d767-886">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="8d767-887">Добавлен параметр -PublicIpAddress, который принимает один или несколько объектов общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="8d767-887">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="8d767-888">Добавлен параметр -VirtualNetwork, который принимает объект виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="8d767-888">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="8d767-889">Добавлены методы AddPublicIpAddress и RemovePublicIpAddress для объекта брандмауэра. Они принимают объект общедоступного IP-адреса в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="8d767-889">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="8d767-890">Не рекомендуется использовать параметры -PublicIpName и -VirtualNetworkName.</span><span class="sxs-lookup"><span data-stu-id="8d767-890">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="8d767-891">Обновлены следующие команды для функции: В параметрах проверки подлинности AAD VPN-клиента задан ресурс шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="8d767-891">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="8d767-892">Обновлен командлет New-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="8d767-892">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="8d767-893">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="8d767-893">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="8d767-894">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр-переключатель RemoveAadAuthentication для удаления в шлюзе параметров проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="8d767-894">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8d767-895">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8d767-895">Az.OperationalInsights</span></span>
* <span data-ttu-id="8d767-896">Добавлена поддержка SKU **pergb2018** в команде New-AzureRmOperationalInsightsWorkspace.</span><span class="sxs-lookup"><span data-stu-id="8d767-896">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d767-897">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d767-897">Az.Resources</span></span>
* <span data-ttu-id="8d767-898">Поддержка дополнительных вариантов экспорта шаблона.</span><span class="sxs-lookup"><span data-stu-id="8d767-898">Support for additional Template Export options</span></span>
    - <span data-ttu-id="8d767-899">В Export-AzResourceGroup добавлен параметр -SkipResourceNameParameterization.</span><span class="sxs-lookup"><span data-stu-id="8d767-899">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="8d767-900">В Export-AzResourceGroup добавлен параметр -SkipAllParameterization.</span><span class="sxs-lookup"><span data-stu-id="8d767-900">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="8d767-901">В Export-AzResourceGroup добавлен параметр -Resource для фильтрации экспортированных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8d767-901">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8d767-902">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8d767-902">Az.ServiceFabric</span></span>
* <span data-ttu-id="8d767-903">Исправлена ошибка, связанная с получением иногда неправильных отпечатков при добавлении сертификата ByExistingKeyVault.</span><span class="sxs-lookup"><span data-stu-id="8d767-903">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d767-904">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d767-904">Az.Sql</span></span>
* <span data-ttu-id="8d767-905">Исправлен суффикс конечной точки хранилища службы "Расширенная защита от угроз Azure".</span><span class="sxs-lookup"><span data-stu-id="8d767-905">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="8d767-906">Исправлена ошибка, связанная с возможностью пакета "Расширенная защита данных" переопределять политику службы "Расширенная защита от угроз".</span><span class="sxs-lookup"><span data-stu-id="8d767-906">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="8d767-907">Новые командлеты для Management.Sql позволяют клиентам добавлять ключи TDE и задавать средство защиты TDE для управляемых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="8d767-907">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="8d767-908">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8d767-908">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="8d767-909">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8d767-909">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="8d767-910">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8d767-910">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="8d767-911">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="8d767-911">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="8d767-912">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="8d767-912">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d767-913">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d767-913">Az.Storage</span></span>
* <span data-ttu-id="8d767-914">Поддержка класса Kind в FileStorage и значения Premium_ZRS в SkuName при создании учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="8d767-914">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="8d767-915">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8d767-915">New-AzStorageAccount</span></span>
* <span data-ttu-id="8d767-916">Уточнено описание командлета неизменности BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="8d767-916">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="8d767-917">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="8d767-917">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8d767-918">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d767-918">Az.Websites</span></span>
* <span data-ttu-id="8d767-919">Оптимизирует Get-AzWebAppCertificate для фильтрации по группе ресурсов на сервере, а не в клиенте.</span><span class="sxs-lookup"><span data-stu-id="8d767-919">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="8d767-920">Добавляет параметр-переключатель - UseDisasterRecovery в Get AzWebAppSnapshot.</span><span class="sxs-lookup"><span data-stu-id="8d767-920">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="8d767-921">2.2.0 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="8d767-921">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="8d767-922">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8d767-922">Az.Cdn</span></span>
* <span data-ttu-id="8d767-923">Обновлены командлеты для поддержки функции rulesEngine на основе API версии 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="8d767-923">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d767-924">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d767-924">Az.Compute</span></span>
* <span data-ttu-id="8d767-925">Добавлен параметр `NoWait`, который запускает операцию и немедленно возвращает значение еще до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="8d767-925">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="8d767-926">Обновлены командлеты:   Export-AzLogAnalyticRequestRateByInterval; Export-AzLogAnalyticThrottledRequest; Remove-AzVM; Remove-AzVMAccessExtension; Remove-AzVMAEMExtension; Remove-AzVMChefExtension; Remove-AzVMCustomScriptExtension; Remove-AzVMDiagnosticsExtension; Remove-AzVMDiskEncryptionExtension; Remove-AzVMDscExtension; Remove-AzVMSqlServerExtension; Restart-AzVM; Set-AzVM; Set-AzVMAccessExtension; Set-AzVMADDomainExtension; Set-AzVMAEMExtension; Set-AzVMBginfoExtension; Set-AzVMChefExtension; Set-AzVMCustomScriptExtension; Set-AzVMDiagnosticsExtension; Set-AzVMDscExtension; Set-AzVMExtension; Start-AzVM; Stop-AzVM; Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="8d767-926">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8d767-927">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8d767-927">Az.EventHub</span></span>
* <span data-ttu-id="8d767-928">Исправлена ошибка № 9231. Командлет Get-AzEventHubNamespace не возвращал теги.</span><span class="sxs-lookup"><span data-stu-id="8d767-928">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="8d767-929">Исправлена ошибка № 9230. Командлет Get-AzEventHubNamespace возвращал значение ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="8d767-929">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d767-930">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d767-930">Az.Network</span></span>
* <span data-ttu-id="8d767-931">Обновлены параметры ResourceId и InputObject для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="8d767-931">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="8d767-932">Добавлены псевдонимы для параметров ResourceId и InputObject.</span><span class="sxs-lookup"><span data-stu-id="8d767-932">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8d767-933">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8d767-933">Az.PolicyInsights</span></span>
* <span data-ttu-id="8d767-934">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyEvent.</span><span class="sxs-lookup"><span data-stu-id="8d767-934">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8d767-935">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d767-935">Az.RecoveryServices</span></span>
* <span data-ttu-id="8d767-936">Минимальный срок хранения политики IaaSVM изменился с 1 до 7 дней.</span><span class="sxs-lookup"><span data-stu-id="8d767-936">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8d767-937">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8d767-937">Az.ServiceBus</span></span>
* <span data-ttu-id="8d767-938">Исправлена ошибка № 9182. Командлет Get-AzServiceBusNamespace возвращал ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="8d767-938">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8d767-939">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8d767-939">Az.ServiceFabric</span></span>
* <span data-ttu-id="8d767-940">Исправлена опечатка в сообщении об ошибке для командлета Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="8d767-940">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="8d767-941">Исправлен отсутствующей символ в командных строках Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="8d767-941">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d767-942">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d767-942">Az.Sql</span></span>
* <span data-ttu-id="8d767-943">Для командлета New-AzureSqlInstance добавлен параметр DnsZonePartner, обеспечивающий поддержку AutoDr для Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="8d767-943">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="8d767-944">Командлет Get-AzSqlDatabaseSecureConnectionPolicy объявлен неподдерживаемым.</span><span class="sxs-lookup"><span data-stu-id="8d767-944">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="8d767-945">Командлеты обнаружения угроз переименованы в командлеты Расширенной защиты от угроз.</span><span class="sxs-lookup"><span data-stu-id="8d767-945">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="8d767-946">Параметры -StorageSizeInGB и -LicenseType командлета New-AzSqlInstance теперь необязательны.</span><span class="sxs-lookup"><span data-stu-id="8d767-946">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8d767-947">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d767-947">Az.Websites</span></span>
* <span data-ttu-id="8d767-948">Исправлены проблемы, когда удалялись теги при использовании Set-AzWebApp и Set-AzWebAppSlot со свойством -WebApp.</span><span class="sxs-lookup"><span data-stu-id="8d767-948">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="8d767-949">2.1.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="8d767-949">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="8d767-950">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8d767-950">Az.ApiManagement</span></span>
* <span data-ttu-id="8d767-951">Созданы командлеты для управления диагностикой в глобальной области и в области API.</span><span class="sxs-lookup"><span data-stu-id="8d767-951">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="8d767-952">**Get-AzApiManagementDiagnostic** — получение диагностики, заданной глобально или на уровне области API.</span><span class="sxs-lookup"><span data-stu-id="8d767-952">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="8d767-953">**New-AzApiManagementDiagnostic** — создание диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="8d767-953">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="8d767-954">**New-AzApiManagementHttpMessageDiagnostic** — создание параметра диагностики, для которого регистрируются заголовки и размер байтов тела.</span><span class="sxs-lookup"><span data-stu-id="8d767-954">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="8d767-955">**New-AzApiManagementPipelineDiagnosticSetting** — создание параметров диагностики для сообщений HTTP, поступающих в шлюз или исходящих из него.</span><span class="sxs-lookup"><span data-stu-id="8d767-955">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="8d767-956">**New-AzApiManagementSamplingSetting** — создание параметра выборки для запросов и ответов касательно диагностики.</span><span class="sxs-lookup"><span data-stu-id="8d767-956">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="8d767-957">**Remove-AzApiManagementDiagnostic** — удаление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="8d767-957">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="8d767-958">**Set-AzApiManagementDiagnostic** — обновление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="8d767-958">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="8d767-959">Созданы командлеты для управления кэшем в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="8d767-959">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="8d767-960">**Get-AzApiManagementCache** — получение сведений о кэше, указанном идентификатором, или обо всех кэшах.</span><span class="sxs-lookup"><span data-stu-id="8d767-960">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="8d767-961">**New-AzApiManagementCache** — создание кэша по умолчанию или кэша в определенном регионе Azure.</span><span class="sxs-lookup"><span data-stu-id="8d767-961">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="8d767-962">**Remove-AzApiManagementCache** — удаление кэша.</span><span class="sxs-lookup"><span data-stu-id="8d767-962">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="8d767-963">**Update-AzApiManagementCache** — обновление кэша.</span><span class="sxs-lookup"><span data-stu-id="8d767-963">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="8d767-964">Созданы командлеты для управления схемой API.</span><span class="sxs-lookup"><span data-stu-id="8d767-964">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="8d767-965">**New-AzApiManagementSchema** — создание схемы для API.</span><span class="sxs-lookup"><span data-stu-id="8d767-965">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="8d767-966">**Get-AzApiManagementSchema** — получение схем, настроенных в API.</span><span class="sxs-lookup"><span data-stu-id="8d767-966">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="8d767-967">**Remove-AzApiManagementSchema** — удаление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="8d767-967">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="8d767-968">**Set-AzApiManagementSchema** — обновление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="8d767-968">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="8d767-969">Создан командлет для создания токена пользователя.</span><span class="sxs-lookup"><span data-stu-id="8d767-969">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="8d767-970">**New-AzApiManagementUserToken** — создание токена пользователя, по умолчанию действительного в течение 8 часов. С помощью этого командлета можно создавать токен для пользователя GIT.</span><span class="sxs-lookup"><span data-stu-id="8d767-970">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="8d767-971">Создан командлет для получения состояния сети.</span><span class="sxs-lookup"><span data-stu-id="8d767-971">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="8d767-972">**Get-AzApiManagementNetworkStatus** — получение состояния сети ресурсов, от которых зависит служба "Управление API".</span><span class="sxs-lookup"><span data-stu-id="8d767-972">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="8d767-973">Это полезно при развертывании службы ApiManagement в виртуальной сети и проверке того, не нарушена ли какая-либо из зависимостей.</span><span class="sxs-lookup"><span data-stu-id="8d767-973">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="8d767-974">Обновлен командлет **New-AzApiManagement** для управления службой ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="8d767-974">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="8d767-975">Добавлена поддержка нового SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="8d767-975">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="8d767-976">Добавлена поддержка для включения флага EnableClientCertificate в SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="8d767-976">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="8d767-977">Новый командлет **New-AzApiManagementSslSetting** позволяет настраивать параметр TLS/SSL для сервера (Backend) и внешнего интерфейса (Frontend).</span><span class="sxs-lookup"><span data-stu-id="8d767-977">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="8d767-978">Его также можно использовать для настройки Ciphers как 3DES, в ServerProtocols как Http2 для внешнего интерфейса (Frontend) службы ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="8d767-978">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="8d767-979">Добавлена поддержка настройки имени узла DeveloperPortal в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="8d767-979">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="8d767-980">Обновлен командлет **Get-AzApiManagementSsoToken** для извлечения объекта PsApiManagement в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="8d767-980">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="8d767-981">Обновлен командлет для отображения встроенных сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="8d767-981">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="8d767-982">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Код ошибки: ValidationError. Сообщение об ошибке: "Некоторые поля содержат неправильные значения". Сведения об ошибке: [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="8d767-982">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="8d767-983">Обновлен командлет **Export-AzApiManagementApi** для экспортирования программных интерфейсов в формате OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="8d767-983">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="8d767-984">Обновлен командлет **Import-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="8d767-984">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="8d767-985">Для импортирования API из спецификации документа OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="8d767-985">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="8d767-986">Для переопределения свойства PsApiManagementSchema, указанного в любом документе (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="8d767-986">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="8d767-987">Для переопределения свойства ServiceUrl, указанного в любом документе.</span><span class="sxs-lookup"><span data-stu-id="8d767-987">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="8d767-988">Обновлен командлет **Get-AzApiManagementPolicy** для возврата политики в формате, экранированном не для XML, с использованием rawxml.</span><span class="sxs-lookup"><span data-stu-id="8d767-988">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="8d767-989">Обновлен командлет **Set-AzApiManagementPolicy**. Он принимает политику в формате, экранированном не для XML, с использованием rawxml и в формате, экранированном для XML, с использованием XML.</span><span class="sxs-lookup"><span data-stu-id="8d767-989">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="8d767-990">Обновлен командлет **New-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="8d767-990">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="8d767-991">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="8d767-991">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="8d767-992">Для создания API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="8d767-992">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="8d767-993">Для клонирования API с использованием значений SourceApiId и SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="8d767-993">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="8d767-994">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="8d767-994">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="8d767-995">Обновлен командлет **Set-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="8d767-995">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="8d767-996">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="8d767-996">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="8d767-997">Для обновления API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="8d767-997">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="8d767-998">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="8d767-998">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="8d767-999">Обновлен командлет **New-AzApiManagementRevision**:</span><span class="sxs-lookup"><span data-stu-id="8d767-999">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="8d767-1000">Для клонирования (копирования тегов, продуктов, операций и политик) существующей редакции с использованием SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="8d767-1000">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="8d767-1001">Новая редакция предполагает родительский идентификатор ApiId.</span><span class="sxs-lookup"><span data-stu-id="8d767-1001">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="8d767-1002">Для предоставления ApiRevisionDescription.</span><span class="sxs-lookup"><span data-stu-id="8d767-1002">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="8d767-1003">Для переопределения значения ServiceUrl при клонировании API.</span><span class="sxs-lookup"><span data-stu-id="8d767-1003">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="8d767-1004">Обновлен командлет **New-AzApiManagementIdentityProvider**:</span><span class="sxs-lookup"><span data-stu-id="8d767-1004">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="8d767-1005">Для настройки AAD или AADB2C с Authority.</span><span class="sxs-lookup"><span data-stu-id="8d767-1005">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="8d767-1006">Для установки политик SignupPolicy, SigninPolicy, ProfileEditingPolicy и PasswordResetPolicy.</span><span class="sxs-lookup"><span data-stu-id="8d767-1006">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="8d767-1007">Обновлен командлет **New-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="8d767-1007">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="8d767-1008">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="8d767-1008">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="8d767-1009">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="8d767-1009">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="8d767-1010">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="8d767-1010">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="8d767-1011">Обновлен командлет **Set-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="8d767-1011">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="8d767-1012">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="8d767-1012">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="8d767-1013">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="8d767-1013">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="8d767-1014">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="8d767-1014">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="8d767-1015">Следующие командлеты обновлены, чтобы принимать значение ResourceId в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="8d767-1015">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="8d767-1016">New-AzApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="8d767-1016">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="8d767-1017">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="8d767-1017">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="8d767-1018">Get-AzApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="8d767-1018">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="8d767-1019">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="8d767-1019">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="8d767-1020">Get-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="8d767-1020">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="8d767-1021">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="8d767-1021">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="8d767-1022">Get-AzApiManagementAuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="8d767-1022">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="8d767-1023">Get-AzApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="8d767-1023">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="8d767-1024">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="8d767-1024">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="8d767-1025">Get-AzApiManagementCertificate.</span><span class="sxs-lookup"><span data-stu-id="8d767-1025">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="8d767-1026">Remove-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="8d767-1026">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="8d767-1027">Remove-AzApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="8d767-1027">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8d767-1028">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8d767-1028">Az.Automation</span></span>
* <span data-ttu-id="8d767-1029">Обновлен командлет Get-AzAutomationJobOutputRecord для обработки значений в формате JSON и в виде текстовой записи.</span><span class="sxs-lookup"><span data-stu-id="8d767-1029">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="8d767-1030">исправлена проблема https://github.com/Azure/azure-powershell/issues/7977.</span><span class="sxs-lookup"><span data-stu-id="8d767-1030">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="8d767-1031">исправлена проблема https://github.com/Azure/azure-powershell/issues/8600.</span><span class="sxs-lookup"><span data-stu-id="8d767-1031">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="8d767-1032">Поведение командлета Start-AzAutomationDscCompilationJob изменено так, чтобы сразу же запустить задание, а не ждать его завершения.</span><span class="sxs-lookup"><span data-stu-id="8d767-1032">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="8d767-1033">исправлена проблема https://github.com/Azure/azure-powershell/issues/8347.</span><span class="sxs-lookup"><span data-stu-id="8d767-1033">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="8d767-1034">Исправлен командлет Get-AzAutomationDscNode, возвращающий все узлы при использовании -Name.</span><span class="sxs-lookup"><span data-stu-id="8d767-1034">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="8d767-1035">Теперь он возвращает только соответствующий узел.</span><span class="sxs-lookup"><span data-stu-id="8d767-1035">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d767-1036">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d767-1036">Az.Compute</span></span>
* <span data-ttu-id="8d767-1037">Добавлены параметры ProtectFromScaleIn и ProtectFromScaleSetAction для командлета Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="8d767-1037">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="8d767-1038">Командлет New-AzVM с простым набором параметров теперь по умолчанию использует доступное расположение, если регион "восточная часть США" не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8d767-1038">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8d767-1039">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8d767-1039">Az.DataLakeStore</span></span>
* <span data-ttu-id="8d767-1040">Обновлен пакет SDK ADLS для использования httpclient. В инфраструктуру Azure интегрирована проверка плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="8d767-1040">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8d767-1041">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8d767-1041">Az.Monitor</span></span>
* <span data-ttu-id="8d767-1042">Исправлены неправильные имена параметров в справочных примерах.</span><span class="sxs-lookup"><span data-stu-id="8d767-1042">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d767-1043">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d767-1043">Az.Network</span></span>
* <span data-ttu-id="8d767-1044">Добавлен флаг DisableBgpRoutePropagation для выходных данных действующей таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="8d767-1044">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="8d767-1045">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="8d767-1045">Updated cmdlet:</span></span>
        - <span data-ttu-id="8d767-1046">Get-AzEffectiveRouteTable.</span><span class="sxs-lookup"><span data-stu-id="8d767-1046">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="8d767-1047">Исправлен двойной дефис в документации New-AzApplicationGatewayTrustedRootCertificate.</span><span class="sxs-lookup"><span data-stu-id="8d767-1047">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d767-1048">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d767-1048">Az.Resources</span></span>
* <span data-ttu-id="8d767-1049">Добавлен новый командлет Get-AzureRmDenyAssignment для получения запрещающих назначений.</span><span class="sxs-lookup"><span data-stu-id="8d767-1049">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d767-1050">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d767-1050">Az.Sql</span></span>
* <span data-ttu-id="8d767-1051">Командлеты Расширенной защиты от угроз переименованы на командлеты Расширенной защиты данных, и оценка уязвимости включена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8d767-1051">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="8d767-1052">2.0.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="8d767-1052">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8d767-1053">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d767-1053">Az.Accounts</span></span>
* <span data-ttu-id="8d767-1054">Обновлена библиотека аутентификации для устранения проблем с ADFS при использовании аутентификации на основе имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="8d767-1054">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8d767-1055">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8d767-1055">Az.CognitiveServices</span></span>
* <span data-ttu-id="8d767-1056">Отображается только заявление об отказе Bing для служб Поиска Bing.</span><span class="sxs-lookup"><span data-stu-id="8d767-1056">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="8d767-1057">Исправлена проблема с созданием учетной записи.</span><span class="sxs-lookup"><span data-stu-id="8d767-1057">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d767-1058">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d767-1058">Az.Compute</span></span>
* <span data-ttu-id="8d767-1059">Функция группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="8d767-1059">Proximity placement group feature.</span></span>
    - <span data-ttu-id="8d767-1060">Добавлены следующие новые командлеты:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="8d767-1060">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="8d767-1061">Новый параметр ProximityPlacementGroupId будет добавлен в следующие командлеты:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="8d767-1061">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="8d767-1062">В командлет New-AzGalleryImageVersion добавлен параметр StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="8d767-1062">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="8d767-1063">TargetRegion в командлете New-AzGalleryImageVersion может содержать StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="8d767-1063">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="8d767-1064">Параметр-переключатель SkipShutdown добавлен в командлеты Stop-AzVM и Stop-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="8d767-1064">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="8d767-1065">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="8d767-1065">Breaking changes</span></span>
    - <span data-ttu-id="8d767-1066">Командлет SET-AzVMBootDiagnostics изменен на Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="8d767-1066">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="8d767-1067">Командлет Export-AzLogAnalyticThrottledRequests изменен на Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="8d767-1067">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="8d767-1068">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="8d767-1068">Az.DeploymentManager</span></span>
* <span data-ttu-id="8d767-1069">Первая общедоступная версия командлетов диспетчера развертывания Azure</span><span class="sxs-lookup"><span data-stu-id="8d767-1069">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="8d767-1070">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="8d767-1070">Az.Dns</span></span>
* <span data-ttu-id="8d767-1071">Автоматическое делегирование DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="8d767-1071">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="8d767-1072">Командлет для создания зоны DNS принимает имя родительской зоны в качестве дополнительного необязательного параметра.</span><span class="sxs-lookup"><span data-stu-id="8d767-1072">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="8d767-1073">Он добавляет записи NS в родительской зоне для созданной дочерней зоны.</span><span class="sxs-lookup"><span data-stu-id="8d767-1073">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8d767-1074">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8d767-1074">Az.FrontDoor</span></span>
* <span data-ttu-id="8d767-1075">Первая общедоступная версия командлетов Azure FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="8d767-1075">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="8d767-1076">Переименованы командлеты WAF для включения Waf.</span><span class="sxs-lookup"><span data-stu-id="8d767-1076">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="8d767-1077">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8d767-1077">Az.HDInsight</span></span>
* <span data-ttu-id="8d767-1078">Удалены два командлета:</span><span class="sxs-lookup"><span data-stu-id="8d767-1078">Removed two cmdlets:</span></span>
    - <span data-ttu-id="8d767-1079">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="8d767-1079">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="8d767-1080">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="8d767-1080">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="8d767-1081">Добавлен новый командлет Set-AzHDInsightGatewayCredential для замены Grant-AzHDInsightHttpServicesAccess.</span><span class="sxs-lookup"><span data-stu-id="8d767-1081">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="8d767-1082">Обновлен командлет Get-AzHDInsightJobOutput для различения ролей читателя и оператора HDInsight:</span><span class="sxs-lookup"><span data-stu-id="8d767-1082">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="8d767-1083">Пользователям с ролью читателя не нужно указывать параметр DefaultStorageAccountKey явным образом, иначе возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="8d767-1083">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="8d767-1084">На пользователей с ролью оператора HDInsight это не повлияет.</span><span class="sxs-lookup"><span data-stu-id="8d767-1084">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8d767-1085">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8d767-1085">Az.Monitor</span></span>
* <span data-ttu-id="8d767-1086">Новые командлеты для API SQR (запланированное правило запросов)</span><span class="sxs-lookup"><span data-stu-id="8d767-1086">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="8d767-1087">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="8d767-1087">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="8d767-1088">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="8d767-1088">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="8d767-1089">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="8d767-1089">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="8d767-1090">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="8d767-1090">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="8d767-1091">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="8d767-1091">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="8d767-1092">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="8d767-1092">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="8d767-1093">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8d767-1093">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8d767-1094">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8d767-1094">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8d767-1095">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8d767-1095">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8d767-1096">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8d767-1096">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8d767-1097">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8d767-1097">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8d767-1098">См. подробнее об [API SQR](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules).</span><span class="sxs-lookup"><span data-stu-id="8d767-1098">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="8d767-1099">Обновлен файл Az.Monitor.md для включения командлетов для правила генерации оповещений на основе метрик GenV2(не классическая версия).</span><span class="sxs-lookup"><span data-stu-id="8d767-1099">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d767-1100">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d767-1100">Az.Network</span></span>
* <span data-ttu-id="8d767-1101">Добавлена поддержка для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="8d767-1101">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="8d767-1102">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="8d767-1102">New cmdlets</span></span>
        - <span data-ttu-id="8d767-1103">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="8d767-1103">New-AzNatGateway</span></span>
        - <span data-ttu-id="8d767-1104">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="8d767-1104">Get-AzNatGateway</span></span>
        - <span data-ttu-id="8d767-1105">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="8d767-1105">Set-AzNatGateway</span></span>
        - <span data-ttu-id="8d767-1106">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="8d767-1106">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="8d767-1107">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="8d767-1107">Updated cmdlets</span></span>
        - <span data-ttu-id="8d767-1108">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="8d767-1108">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="8d767-1109">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="8d767-1109">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="8d767-1110">Обновлены следующие команды для функции: Настройка и удаление пользовательских маршрутов через шлюз в Бруклине.</span><span class="sxs-lookup"><span data-stu-id="8d767-1110">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="8d767-1111">Обновлен командлет New-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="8d767-1111">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="8d767-1112">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="8d767-1112">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8d767-1113">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8d767-1113">Az.PolicyInsights</span></span>
* <span data-ttu-id="8d767-1114">Добавлена поддержка сведений об оценке политики запросов.</span><span class="sxs-lookup"><span data-stu-id="8d767-1114">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="8d767-1115">Добавлен параметр -Expand в командлет Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="8d767-1115">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="8d767-1116">Добавлена поддержка -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="8d767-1116">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8d767-1117">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d767-1117">Az.RecoveryServices</span></span>
* <span data-ttu-id="8d767-1118">Добавлена поддержка перекрестной подписки на Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="8d767-1118">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="8d767-1119">Добавлена возможность отмечать предстоящие критически важные изменения для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="8d767-1119">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="8d767-1120">Исправлены план восстановления и план действий для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="8d767-1120">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="8d767-1121">Исправлено сетевое сопоставление обновления Azure Site Recovery (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="8d767-1121">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="8d767-1122">Исправлено направление защиты обновления Azure Site Recovery для управляемых дисков (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="8d767-1122">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="8d767-1123">Добавлены другие незначительные исправления.</span><span class="sxs-lookup"><span data-stu-id="8d767-1123">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="8d767-1124">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="8d767-1124">Az.Relay</span></span>
* <span data-ttu-id="8d767-1125">Исправлены опечатки в сообщениях для клиентов.</span><span class="sxs-lookup"><span data-stu-id="8d767-1125">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8d767-1126">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8d767-1126">Az.ServiceBus</span></span>
* <span data-ttu-id="8d767-1127">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="8d767-1127">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d767-1128">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d767-1128">Az.Storage</span></span>
* <span data-ttu-id="8d767-1129">Выполнено обновление клиентской библиотеки хранилища до версии 10.0.1 (пространство имен всех объектов из этого пакета SDK изменено с Microsoft.WindowsAzure.Storage. *на Microsoft.Azure.Storage*).</span><span class="sxs-lookup"><span data-stu-id="8d767-1129">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="8d767-1130">Выполнено обновление до Microsoft.Azure.Management.Storage версии 11.0.0 для включения поддержки нового API версии 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="8d767-1130">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="8d767-1131">Значение свойства Kind по умолчанию в учетной записи хранения изменено со Storage на StorageV2.</span><span class="sxs-lookup"><span data-stu-id="8d767-1131">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="8d767-1132">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8d767-1132">New-AzStorageAccount</span></span>
* <span data-ttu-id="8d767-1133">Изменено значение Sku.Name в выходных данных командлета учетной записи хранения в соответствии со значением Sku.Name во входных данных путем добавления _ (например, StandardLRS изменено на Standard_LRS).</span><span class="sxs-lookup"><span data-stu-id="8d767-1133">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="8d767-1134">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8d767-1134">New-AzStorageAccount</span></span>
    - <span data-ttu-id="8d767-1135">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8d767-1135">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="8d767-1136">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8d767-1136">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8d767-1137">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d767-1137">Az.Websites</span></span>
* <span data-ttu-id="8d767-1138">Свойство Kind теперь будет задаваться объектам PSSite, возвращаемым командлетом Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="8d767-1138">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="8d767-1139">Get-AzWebApp\*Metrics и Get-AzAppServicePlanMetrics считаются нерекомендуемыми.</span><span class="sxs-lookup"><span data-stu-id="8d767-1139">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="8d767-1140">1.8.0 — апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="8d767-1140">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8d767-1141">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="8d767-1141">Highlights since the last major release</span></span>
* <span data-ttu-id="8d767-1142">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="8d767-1142">General availability of `Az` module</span></span>
* <span data-ttu-id="8d767-1143">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="8d767-1143">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="8d767-1144">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="8d767-1144">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="8d767-1145">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="8d767-1145">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="8d767-1146">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="8d767-1146">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8d767-1147">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="8d767-1147">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="8d767-1148">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="8d767-1148">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8d767-1149">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d767-1149">Az.Accounts</span></span>
* <span data-ttu-id="8d767-1150">Обновлен командлет Uninstall-AzureRm для правильного удаления модулей в Mac.</span><span class="sxs-lookup"><span data-stu-id="8d767-1150">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="8d767-1151">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8d767-1151">Az.Batch</span></span>
* <span data-ttu-id="8d767-1152">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="8d767-1152">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8d767-1153">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8d767-1153">Az.Cdn</span></span>
* <span data-ttu-id="8d767-1154">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="8d767-1154">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8d767-1155">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8d767-1155">Az.CognitiveServices</span></span>
* <span data-ttu-id="8d767-1156">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="8d767-1156">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d767-1157">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d767-1157">Az.Compute</span></span>
* <span data-ttu-id="8d767-1158">Устранена проблема с установкой AEM, если в идентификаторах ресурсов дисков группа ресурсов указана в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="8d767-1158">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="8d767-1159">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="8d767-1159">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8d767-1160">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="8d767-1160">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8d767-1161">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8d767-1161">Az.DataFactory</span></span>
* <span data-ttu-id="8d767-1162">Добавлены свойства SsisProperties, если NodeCount не имеет значения NULL для управляемой среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="8d767-1162">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8d767-1163">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8d767-1163">Az.DataLakeStore</span></span>
* <span data-ttu-id="8d767-1164">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="8d767-1164">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8d767-1165">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8d767-1165">Az.EventGrid</span></span>
* <span data-ttu-id="8d767-1166">Обновлен текст справки для конечной точки, указывающий, что необходимо создать ресурсы, прежде чем использовать командлеты для создания или обновления подписки на события.</span><span class="sxs-lookup"><span data-stu-id="8d767-1166">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8d767-1167">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8d767-1167">Az.EventHub</span></span>
* <span data-ttu-id="8d767-1168">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="8d767-1168">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="8d767-1169">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8d767-1169">Az.HDInsight</span></span>
* <span data-ttu-id="8d767-1170">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="8d767-1170">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8d767-1171">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8d767-1171">Az.IotHub</span></span>
* <span data-ttu-id="8d767-1172">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="8d767-1172">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8d767-1173">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8d767-1173">Az.KeyVault</span></span>
* <span data-ttu-id="8d767-1174">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="8d767-1174">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8d767-1175">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="8d767-1175">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="8d767-1176">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="8d767-1176">Az.MachineLearning</span></span>
* <span data-ttu-id="8d767-1177">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="8d767-1177">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="8d767-1178">Az.Media</span><span class="sxs-lookup"><span data-stu-id="8d767-1178">Az.Media</span></span>
* <span data-ttu-id="8d767-1179">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="8d767-1179">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8d767-1180">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8d767-1180">Az.Monitor</span></span>
  * <span data-ttu-id="8d767-1181">Добавлены новые командлеты для правила генерации оповещений на основе метрик GenV2 (не классических).</span><span class="sxs-lookup"><span data-stu-id="8d767-1181">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="8d767-1182">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="8d767-1182">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="8d767-1183">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="8d767-1183">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="8d767-1184">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="8d767-1184">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="8d767-1185">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="8d767-1185">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="8d767-1186">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="8d767-1186">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="8d767-1187">Обновлен пакет SDK Monitor до предварительной версии 0.22.0.</span><span class="sxs-lookup"><span data-stu-id="8d767-1187">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d767-1188">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d767-1188">Az.Network</span></span>
* <span data-ttu-id="8d767-1189">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="8d767-1189">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8d767-1190">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="8d767-1190">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="8d767-1191">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="8d767-1191">Az.NotificationHubs</span></span>
* <span data-ttu-id="8d767-1192">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="8d767-1192">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8d767-1193">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8d767-1193">Az.OperationalInsights</span></span>
* <span data-ttu-id="8d767-1194">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="8d767-1194">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="8d767-1195">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="8d767-1195">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="8d767-1196">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="8d767-1196">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8d767-1197">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d767-1197">Az.RecoveryServices</span></span>
* <span data-ttu-id="8d767-1198">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="8d767-1198">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8d767-1199">Обновлен табличный формат для SQL на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="8d767-1199">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="8d767-1200">Добавлен альтернативный метод для получения расположения в Общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="8d767-1200">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="8d767-1201">Обновлено значение ScheduleRunDays в объекте SchedulePolicy в соответствии с часовым поясом.</span><span class="sxs-lookup"><span data-stu-id="8d767-1201">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="8d767-1202">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8d767-1202">Az.RedisCache</span></span>
* <span data-ttu-id="8d767-1203">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="8d767-1203">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d767-1204">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d767-1204">Az.Resources</span></span>
* <span data-ttu-id="8d767-1205">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="8d767-1205">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d767-1206">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d767-1206">Az.Sql</span></span>
* <span data-ttu-id="8d767-1207">Заменена зависимость от пакета SDK монитора на обычный код.</span><span class="sxs-lookup"><span data-stu-id="8d767-1207">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="8d767-1208">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="8d767-1208">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8d767-1209">Улучшен процесс классификации нескольких столбцов.</span><span class="sxs-lookup"><span data-stu-id="8d767-1209">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="8d767-1210">Добавлены свойства SKU (имя, семейство, производительность SKU) в отклике Get-AzSqlServerServiceObjective, а также по умолчанию задан табличный формат.</span><span class="sxs-lookup"><span data-stu-id="8d767-1210">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="8d767-1211">C помощью Get-AzSqlServerServiceObjective теперь можно получать список доступных целевых служб по расположению без необходимости заранее размещать сервер в регионе.</span><span class="sxs-lookup"><span data-stu-id="8d767-1211">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="8d767-1212">Поддерживается параметр часового пояса при создании Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="8d767-1212">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="8d767-1213">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="8d767-1213">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8d767-1214">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d767-1214">Az.Websites</span></span>
* <span data-ttu-id="8d767-1215">Исправлены командлеты Set-AzWebApp и Set-AzWebAppSlot, которые теперь не удаляют теги при выполнении.</span><span class="sxs-lookup"><span data-stu-id="8d767-1215">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="8d767-1216">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="8d767-1216">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8d767-1217">Обновлен пакет SDK веб-узлов.</span><span class="sxs-lookup"><span data-stu-id="8d767-1217">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="8d767-1218">Удалено свойство AdminSiteName из PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="8d767-1218">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="8d767-1219">1.7.0 —апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="8d767-1219">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8d767-1220">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="8d767-1220">Highlights since the last major release</span></span>
* <span data-ttu-id="8d767-1221">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="8d767-1221">General availability of `Az` module</span></span>
* <span data-ttu-id="8d767-1222">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="8d767-1222">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="8d767-1223">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="8d767-1223">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="8d767-1224">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="8d767-1224">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="8d767-1225">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="8d767-1225">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8d767-1226">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="8d767-1226">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="8d767-1227">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="8d767-1227">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8d767-1228">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d767-1228">Az.Accounts</span></span>
* <span data-ttu-id="8d767-1229">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметр AzureAnalysisServicesEndpointResourceId.</span><span class="sxs-lookup"><span data-stu-id="8d767-1229">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="8d767-1230">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8d767-1230">Az.AnalysisServices</span></span>
* <span data-ttu-id="8d767-1231">Использование ServiceClient в командлетах плоскости данных и удаление исходной логики проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="8d767-1231">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="8d767-1232">Add-AzureASAccount используется как оболочка для Connect-AzAccount во избежание критических изменений.</span><span class="sxs-lookup"><span data-stu-id="8d767-1232">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8d767-1233">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8d767-1233">Az.Automation</span></span>
* <span data-ttu-id="8d767-1234">Исправлена ошибка командлета New-AzAutomationSoftwareUpdateConfiguration, связанная с включением.</span><span class="sxs-lookup"><span data-stu-id="8d767-1234">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="8d767-1235">Теперь параметры IncludedKbNumber и IncludedPackageNameMask должны работать нормально.</span><span class="sxs-lookup"><span data-stu-id="8d767-1235">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="8d767-1236">Исправлена ошибка динамической группы управления обновлениями службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="8d767-1236">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d767-1237">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d767-1237">Az.Compute</span></span>
* <span data-ttu-id="8d767-1238">В командлеты New-AzDiskConfig и New-AzSnapshotConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="8d767-1238">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="8d767-1239">Теперь можно создавать виртуальные машину на основе образов из коллекции от других клиентов.</span><span class="sxs-lookup"><span data-stu-id="8d767-1239">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="8d767-1240">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8d767-1240">Az.ContainerInstance</span></span>
* <span data-ttu-id="8d767-1241">Исправлена проблема в параметре -Command командлета New-AzContainerGroup, из-за которой в конце добавлялся пустой аргумент.</span><span class="sxs-lookup"><span data-stu-id="8d767-1241">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8d767-1242">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8d767-1242">Az.DataFactory</span></span>
* <span data-ttu-id="8d767-1243">Пакет SDK для ADF .NET обновлен до версии 3.0.2.</span><span class="sxs-lookup"><span data-stu-id="8d767-1243">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="8d767-1244">Командлет Set-AzDataFactoryV2 обновлен с помощью дополнительных параметров для настроек, связанных с RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="8d767-1244">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d767-1245">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d767-1245">Az.Resources</span></span>
* <span data-ttu-id="8d767-1246">Улучшена обработка поставщиков Get-AzResource при предоставлении параметров -ResourceId или -ResourceGroupName, -Name и -ResourceType.</span><span class="sxs-lookup"><span data-stu-id="8d767-1246">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="8d767-1247">Улучшена обработка ошибок в командлетах Test-AzDeployment и Test-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="8d767-1247">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="8d767-1248">Теперь ошибки, возникающие за пределами проверки развертывания, обрабатываются и включаются в выходные данные команды.</span><span class="sxs-lookup"><span data-stu-id="8d767-1248">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="8d767-1249">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="8d767-1249">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="8d767-1250">Добавлен параметр-переключатель -IgnoreDynamicParameters, с помощью которого можно настроить командлеты развертывания так, чтобы они пропускали запросы в сценариях скриптов и заданий.</span><span class="sxs-lookup"><span data-stu-id="8d767-1250">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="8d767-1251">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="8d767-1251">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d767-1252">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d767-1252">Az.Sql</span></span>
* <span data-ttu-id="8d767-1253">Поддержка классификации данных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="8d767-1253">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d767-1254">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d767-1254">Az.Storage</span></span>
* <span data-ttu-id="8d767-1255">Подробные сообщения об ошибке передаются при создании контекста хранилища с помощью параметра -UseConnectedAccount, но без входа в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="8d767-1255">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="8d767-1256">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="8d767-1256">New-AzStorageContext</span></span>
* <span data-ttu-id="8d767-1257">Поддержка свойств службы управления BLOB-объектов в указанной учетной записи хранения с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="8d767-1257">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="8d767-1258">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="8d767-1258">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="8d767-1259">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="8d767-1259">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="8d767-1260">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8d767-1260">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="8d767-1261">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8d767-1261">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="8d767-1262">Поддержка параметра -AsJob в командлетах для отправки и скачивания больших двоичных объектов и файлов.</span><span class="sxs-lookup"><span data-stu-id="8d767-1262">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="8d767-1263">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8d767-1263">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="8d767-1264">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8d767-1264">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="8d767-1265">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8d767-1265">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="8d767-1266">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8d767-1266">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="8d767-1267">1.6.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="8d767-1267">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8d767-1268">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="8d767-1268">Highlights since the last major release</span></span>
* <span data-ttu-id="8d767-1269">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="8d767-1269">General availability of `Az` module</span></span>
* <span data-ttu-id="8d767-1270">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="8d767-1270">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="8d767-1271">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="8d767-1271">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="8d767-1272">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="8d767-1272">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="8d767-1273">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="8d767-1273">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8d767-1274">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="8d767-1274">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="8d767-1275">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="8d767-1275">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8d767-1276">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8d767-1276">Az.Automation</span></span>
* <span data-ttu-id="8d767-1277">В управление обновлениями службы автоматизации Azure внесены изменения для поддержки следующих новых функций:</span><span class="sxs-lookup"><span data-stu-id="8d767-1277">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="8d767-1278">динамическое группирование;</span><span class="sxs-lookup"><span data-stu-id="8d767-1278">Dynamic grouping</span></span>
    * <span data-ttu-id="8d767-1279">скрипты предварительного или последующего выполнения;</span><span class="sxs-lookup"><span data-stu-id="8d767-1279">Pre-Post script</span></span>
    * <span data-ttu-id="8d767-1280">параметр перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="8d767-1280">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d767-1281">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d767-1281">Az.Compute</span></span>
* <span data-ttu-id="8d767-1282">Устранена проблема, связанная с разрешением пути в Get-AzVmBootDiagnosticsData.</span><span class="sxs-lookup"><span data-stu-id="8d767-1282">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="8d767-1283">Обновление клиентской библиотеки вычислений до версии 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="8d767-1283">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8d767-1284">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8d767-1284">Az.KeyVault</span></span>
* <span data-ttu-id="8d767-1285">Добавлена поддержка подстановочных знаков в командлетах KeyVault.</span><span class="sxs-lookup"><span data-stu-id="8d767-1285">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d767-1286">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d767-1286">Az.Network</span></span>
* <span data-ttu-id="8d767-1287">Добавлена поддержка анализа угроз для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="8d767-1287">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="8d767-1288">Добавлены настраиваемые правила и ресурс верхнего уровня для политики брандмауэра Шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="8d767-1288">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8d767-1289">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d767-1289">Az.RecoveryServices</span></span>
* <span data-ttu-id="8d767-1290">В политику виртуальной машины Azure добавлен объект SnapshotRetentionInDays для поддержки мгновенного восстановления.</span><span class="sxs-lookup"><span data-stu-id="8d767-1290">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="8d767-1291">Добавлена поддержка канала для отмены регистрации контейнера.</span><span class="sxs-lookup"><span data-stu-id="8d767-1291">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d767-1292">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d767-1292">Az.Resources</span></span>
* <span data-ttu-id="8d767-1293">Обновлена поддержка подстановочных знаков для Get-AzResource и Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8d767-1293">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="8d767-1294">Обновлены учетные данные, используемые при общих вызовах к ARM.</span><span class="sxs-lookup"><span data-stu-id="8d767-1294">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d767-1295">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d767-1295">Az.Sql</span></span>
* <span data-ttu-id="8d767-1296">Изменен тип параметра (ExcludeDetectionType) командлетов для обнаружения угроз с DetectionTypes на string[] для поддержки актуального состояния при добавлении новых типов обнаружения и для поддержки автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="8d767-1296">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d767-1297">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d767-1297">Az.Storage</span></span>
* <span data-ttu-id="8d767-1298">Поддержка получения, настройки и удаления политики управления в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="8d767-1298">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="8d767-1299">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="8d767-1299">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="8d767-1300">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="8d767-1300">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="8d767-1301">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="8d767-1301">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="8d767-1302">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="8d767-1302">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="8d767-1303">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="8d767-1303">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="8d767-1304">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="8d767-1304">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8d767-1305">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d767-1305">Az.Websites</span></span>
* <span data-ttu-id="8d767-1306">Исправлена ошибка с шаблоном ARM, из-за которой прерывалось клонирование все слотов при использовании New-AzWebApp -IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="8d767-1306">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="8d767-1307">1.5.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="8d767-1307">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8d767-1308">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d767-1308">Az.Accounts</span></span>
* <span data-ttu-id="8d767-1309">Добавлена команда Register-AzModule для поддержки созданных командлетов AutoRest.</span><span class="sxs-lookup"><span data-stu-id="8d767-1309">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="8d767-1310">Обновлены примеры для Connect AzAccount.</span><span class="sxs-lookup"><span data-stu-id="8d767-1310">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8d767-1311">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8d767-1311">Az.Automation</span></span>
* <span data-ttu-id="8d767-1312">Исправлена проблема с получением некоторых ежемесячных расписаний в нескольких командлетах службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="8d767-1312">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="8d767-1313">Исправлен командлет Get-AzAutomationDscNode, возвращающий только первые 20 узлов.</span><span class="sxs-lookup"><span data-stu-id="8d767-1313">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="8d767-1314">Теперь он возвращает все узлы.</span><span class="sxs-lookup"><span data-stu-id="8d767-1314">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8d767-1315">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8d767-1315">Az.Cdn</span></span>
* <span data-ttu-id="8d767-1316">Добавлены новые командлеты PowerShell для включения и отключения HTTPS для личного домена и отключены устаревшие командлеты.</span><span class="sxs-lookup"><span data-stu-id="8d767-1316">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d767-1317">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d767-1317">Az.Compute</span></span>
* <span data-ttu-id="8d767-1318">Добавлена поддержка подстановочных знаков в командлетах Get.</span><span class="sxs-lookup"><span data-stu-id="8d767-1318">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8d767-1319">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8d767-1319">Az.DataFactory</span></span>
* <span data-ttu-id="8d767-1320">Обновлен пакет SDK для ADF .NET до версии 3.0.1.</span><span class="sxs-lookup"><span data-stu-id="8d767-1320">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8d767-1321">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8d767-1321">Az.LogicApp</span></span>
* <span data-ttu-id="8d767-1322">Исправлена проблема с получением только первой страницы результатов при выполнении команды ListWorkflows.</span><span class="sxs-lookup"><span data-stu-id="8d767-1322">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d767-1323">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d767-1323">Az.Network</span></span>
* <span data-ttu-id="8d767-1324">Добавлена поддержка подстановочных знаков в командлетах Network.</span><span class="sxs-lookup"><span data-stu-id="8d767-1324">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8d767-1325">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d767-1325">Az.RecoveryServices</span></span>
* <span data-ttu-id="8d767-1326">Добавлена поддержка SQL Server на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="8d767-1326">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="8d767-1327">Обновление пакета SDK</span><span class="sxs-lookup"><span data-stu-id="8d767-1327">SDK Update</span></span>
* <span data-ttu-id="8d767-1328">Удалена проверка VMappContainer в Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="8d767-1328">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="8d767-1329">Добавлены параметры Name и ServerName для Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="8d767-1329">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d767-1330">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d767-1330">Az.Resources</span></span>
* <span data-ttu-id="8d767-1331">Добавлен параметр `-TemplateObject` в командлеты для развертывания.</span><span class="sxs-lookup"><span data-stu-id="8d767-1331">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="8d767-1332">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2933.</span><span class="sxs-lookup"><span data-stu-id="8d767-1332">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="8d767-1333">Устранена проблема с передачей в конвейер результата `Get-AzResource` для `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="8d767-1333">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="8d767-1334">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8240.</span><span class="sxs-lookup"><span data-stu-id="8d767-1334">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="8d767-1335">Устранена проблема с изменением типа данных JSON при выполнении `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="8d767-1335">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="8d767-1336">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7930.</span><span class="sxs-lookup"><span data-stu-id="8d767-1336">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d767-1337">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d767-1337">Az.Sql</span></span>
* <span data-ttu-id="8d767-1338">Обновление AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="8d767-1338">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="8d767-1339">Исправлено поведение для пограничного случая при создании параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="8d767-1339">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d767-1340">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d767-1340">Az.Storage</span></span>
* <span data-ttu-id="8d767-1341">Включена поддержка Kind BlockBlobStorage при создании учетной записи хранения для New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="8d767-1341">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="8d767-1342">1.4.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="8d767-1342">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="8d767-1343">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8d767-1343">Az.AnalysisServices</span></span>
* <span data-ttu-id="8d767-1344">Командлет AddAzureASAccount устарел.</span><span class="sxs-lookup"><span data-stu-id="8d767-1344">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8d767-1345">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8d767-1345">Az.Automation</span></span>
* <span data-ttu-id="8d767-1346">Обновлена справка для командлета Import-AzAutomationDscNodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="8d767-1346">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="8d767-1347">Добавлена проверка имени конфигурации для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="8d767-1347">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="8d767-1348">Улучшена обработка ошибок для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="8d767-1348">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8d767-1349">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8d767-1349">Az.CognitiveServices</span></span>
* <span data-ttu-id="8d767-1350">Добавлен параметр CustomSubdomainName — новый необязательный параметр для командлета New-AzCognitiveServicesAccount, который указывает поддомен для ресурса.</span><span class="sxs-lookup"><span data-stu-id="8d767-1350">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d767-1351">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d767-1351">Az.Compute</span></span>
* <span data-ttu-id="8d767-1352">Устранена проблема с идентификаторами наборов параметров.</span><span class="sxs-lookup"><span data-stu-id="8d767-1352">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="8d767-1353">Обновлен командлет Get-AzVMExtension для отображения списка всех установленных расширений, если не указан параметр Name.</span><span class="sxs-lookup"><span data-stu-id="8d767-1353">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="8d767-1354">Для командлета Update-AzImage добавлены параметры Tag и ResourceId.</span><span class="sxs-lookup"><span data-stu-id="8d767-1354">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="8d767-1355">Командлет Get-AzVmssVM, который выполняется без указания идентификатора экземпляра и с параметром InstanceView, может выводить виртуальные машины из VMSS с представлением экземпляра.</span><span class="sxs-lookup"><span data-stu-id="8d767-1355">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8d767-1356">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8d767-1356">Az.DataLakeStore</span></span>
* <span data-ttu-id="8d767-1357">Добавлены командлеты для перечисления и восстановления удаленного элемента ADL.</span><span class="sxs-lookup"><span data-stu-id="8d767-1357">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8d767-1358">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8d767-1358">Az.EventHub</span></span>
* <span data-ttu-id="8d767-1359">Добавлено новое логическое свойство SkipEmptyArchives для пропуска пустых архивов в классе CaptureDescription Eventhub.</span><span class="sxs-lookup"><span data-stu-id="8d767-1359">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="8d767-1360">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8d767-1360">Az.KeyVault</span></span>
* <span data-ttu-id="8d767-1361">Исправлена расстановка тегов для командлета Set-AzKeyVaultSecret.</span><span class="sxs-lookup"><span data-stu-id="8d767-1361">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8d767-1362">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8d767-1362">Az.LogicApp</span></span>
* <span data-ttu-id="8d767-1363">Добавлен SKU "Базовый" для учетных записей интеграции.</span><span class="sxs-lookup"><span data-stu-id="8d767-1363">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="8d767-1364">Добавлены типы сопоставлений Liquid, а также XSLT 2.0 и XSLT 3.0.</span><span class="sxs-lookup"><span data-stu-id="8d767-1364">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="8d767-1365">Новые командлеты для сборок учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="8d767-1365">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="8d767-1366">Get-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="8d767-1366">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="8d767-1367">New-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="8d767-1367">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="8d767-1368">Remove-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="8d767-1368">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="8d767-1369">Set-AzIntegrationAccountAssembly.</span><span class="sxs-lookup"><span data-stu-id="8d767-1369">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="8d767-1370">Новые командлеты для конфигурации пакета учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="8d767-1370">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="8d767-1371">Get-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="8d767-1371">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="8d767-1372">New-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="8d767-1372">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="8d767-1373">Remove-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="8d767-1373">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="8d767-1374">Set-AzIntegrationAccountBatchConfiguration.</span><span class="sxs-lookup"><span data-stu-id="8d767-1374">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="8d767-1375">Обновлен пакет SDK Logic Apps до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="8d767-1375">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8d767-1376">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8d767-1376">Az.Monitor</span></span>
* <span data-ttu-id="8d767-1377">Обновлена справка для командлета Get-AzMetric.</span><span class="sxs-lookup"><span data-stu-id="8d767-1377">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d767-1378">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d767-1378">Az.Network</span></span>
* <span data-ttu-id="8d767-1379">Обновлен пример справки для командлета Add-AzApplicationGatewayCustomError.</span><span class="sxs-lookup"><span data-stu-id="8d767-1379">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8d767-1380">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8d767-1380">Az.OperationalInsights</span></span>
* <span data-ttu-id="8d767-1381">Дополнительная поддержка создания и получения источников данных ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="8d767-1381">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="8d767-1382">Добавлен новый тип ApplicationInsights для получения определенных или всех источников данных ApplicationInsights для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="8d767-1382">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="8d767-1383">Добавлен командлет New-AzOperationalInsightsApplicationInsightsDataSource для создания источника данных с использованием параметров указанного ресурса Application-Insightss: subscription Id, resourceGroupName и name.</span><span class="sxs-lookup"><span data-stu-id="8d767-1383">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="8d767-1384">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d767-1384">Az.Resources</span></span>
* <span data-ttu-id="8d767-1385">исправлена проблема https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="8d767-1385">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="8d767-1386">исправлена проблема https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="8d767-1386">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="8d767-1387">исправлена проблема https://github.com/Azure/azure-powershell/issues/6219.</span><span class="sxs-lookup"><span data-stu-id="8d767-1387">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="8d767-1388">Исправлена ошибка, препятствующая повторному созданию KeyCredentials.</span><span class="sxs-lookup"><span data-stu-id="8d767-1388">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d767-1389">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d767-1389">Az.Sql</span></span>
* <span data-ttu-id="8d767-1390">Добавлена поддержка уровня гипермасштабирования в базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="8d767-1390">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="8d767-1391">Исправлена ошибка, из-за которой восстановление могло завершиться со сбоем при указании ненужных свойств в запросе на восстановление.</span><span class="sxs-lookup"><span data-stu-id="8d767-1391">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8d767-1392">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d767-1392">Az.Websites</span></span>
* <span data-ttu-id="8d767-1393">Исправлен пример для командлета Get-AzWebAppSlotMetrics.</span><span class="sxs-lookup"><span data-stu-id="8d767-1393">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="8d767-1394">1.3.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="8d767-1394">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8d767-1395">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d767-1395">Az.Accounts</span></span>
* <span data-ttu-id="8d767-1396">Обновление до последней версии ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="8d767-1396">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="8d767-1397">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8d767-1397">Az.AnalysisServices</span></span>
<span data-ttu-id="8d767-1398">Общедоступная версия модуля Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="8d767-1398">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d767-1399">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d767-1399">Az.Compute</span></span>
* <span data-ttu-id="8d767-1400">Расширение AEM: добавлена поддержка дисков UltraSSD, P60, P70 и P80.</span><span class="sxs-lookup"><span data-stu-id="8d767-1400">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="8d767-1401">Обновлено описание справки для командлета Set-AzVMBootDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="8d767-1401">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="8d767-1402">Обновлено описание справки и пример для командлета Update-AzImage.</span><span class="sxs-lookup"><span data-stu-id="8d767-1402">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8d767-1403">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d767-1403">Az.RecoveryServices</span></span>
<span data-ttu-id="8d767-1404">Общедоступная версия модуля Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="8d767-1404">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d767-1405">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d767-1405">Az.Resources</span></span>
* <span data-ttu-id="8d767-1406">Исправлена расстановка тегов для групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8d767-1406">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="8d767-1407">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="8d767-1407">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="8d767-1408">Исправлена проблема с игнорированием командлетом `Get-AzureRmRoleAssignment` параметра -ErrorAction.</span><span class="sxs-lookup"><span data-stu-id="8d767-1408">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="8d767-1409">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="8d767-1409">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d767-1410">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d767-1410">Az.Sql</span></span>
* <span data-ttu-id="8d767-1411">Добавлен командлет Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="8d767-1411">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="8d767-1412">Исправлена проблема с появлением исключения NullRef при выполнении командлетов SQL, если не выполнен вход в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="8d767-1412">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="8d767-1413">Исправлено исключение NullRef в командлете Get-AzSqlCapability.</span><span class="sxs-lookup"><span data-stu-id="8d767-1413">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="8d767-1414">1.2.1 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="8d767-1414">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8d767-1415">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d767-1415">Az.Accounts</span></span>
* <span data-ttu-id="8d767-1416">Выпуск с правильной версией службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="8d767-1416">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="8d767-1417">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8d767-1417">Az.AnalysisServices</span></span>
* <span data-ttu-id="8d767-1418">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="8d767-1418">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8d767-1419">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d767-1419">Az.RecoveryServices</span></span>
* <span data-ttu-id="8d767-1420">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="8d767-1420">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="8d767-1421">1.2.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="8d767-1421">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8d767-1422">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d767-1422">Az.Accounts</span></span>
* <span data-ttu-id="8d767-1423">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="8d767-1423">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8d767-1424">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="8d767-1424">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8d767-1425">Добавлено предупреждающее сообщение в PS Core для модуля Uninstall-AzureRm.</span><span class="sxs-lookup"><span data-stu-id="8d767-1425">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="8d767-1426">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="8d767-1426">Az.Aks</span></span>
* <span data-ttu-id="8d767-1427">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="8d767-1427">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8d767-1428">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8d767-1428">Az.Automation</span></span>
* <span data-ttu-id="8d767-1429">Добавлена поддержка для модулей runbook Python 2.</span><span class="sxs-lookup"><span data-stu-id="8d767-1429">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="8d767-1430">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="8d767-1430">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8d767-1431">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8d767-1431">Az.Cdn</span></span>
* <span data-ttu-id="8d767-1432">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="8d767-1432">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d767-1433">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d767-1433">Az.Compute</span></span>
* <span data-ttu-id="8d767-1434">Добавлен командлет Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="8d767-1434">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="8d767-1435">Добавлен параметр TempDisk к командлету Set-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="8d767-1435">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="8d767-1436">Исправлено предупреждающее сообщение командлета New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="8d767-1436">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="8d767-1437">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8d767-1437">Az.ContainerRegistry</span></span>
* <span data-ttu-id="8d767-1438">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="8d767-1438">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8d767-1439">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8d767-1439">Az.DataFactory</span></span>
* <span data-ttu-id="8d767-1440">Пакет SDK ADF .Net обновлен до версии 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="8d767-1440">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8d767-1441">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8d767-1441">Az.DataLakeStore</span></span>
* <span data-ttu-id="8d767-1442">Исправлена проблема с конечной точкой ADLS при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="8d767-1442">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="8d767-1443">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7462.</span><span class="sxs-lookup"><span data-stu-id="8d767-1443">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="8d767-1444">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="8d767-1444">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8d767-1445">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8d767-1445">Az.IotHub</span></span>
* <span data-ttu-id="8d767-1446">Добавлен формат кодирования для командлета Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="8d767-1446">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8d767-1447">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8d767-1447">Az.KeyVault</span></span>
* <span data-ttu-id="8d767-1448">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="8d767-1448">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d767-1449">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d767-1449">Az.Network</span></span>
* <span data-ttu-id="8d767-1450">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="8d767-1450">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d767-1451">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d767-1451">Az.Resources</span></span>
* <span data-ttu-id="8d767-1452">Исправлены неправильные примеры в справочной документации по командлетам New-AzADAppCredential и New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="8d767-1452">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="8d767-1453">Исправлена проблема, при которой путь для параметра -TemplateFile не удавалось разрешить до выполнения командлетов развертывания групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8d767-1453">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="8d767-1454">Az.Resources: исправлена документация для значения по умолчанию -Mode командлета New-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="8d767-1454">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="8d767-1455">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/7522.</span><span class="sxs-lookup"><span data-stu-id="8d767-1455">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="8d767-1456">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/5747.</span><span class="sxs-lookup"><span data-stu-id="8d767-1456">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="8d767-1457">Исправлена проблема с форматированием объекта PSResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="8d767-1457">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="8d767-1458">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2123.</span><span class="sxs-lookup"><span data-stu-id="8d767-1458">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8d767-1459">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8d767-1459">Az.ServiceFabric</span></span>
* <span data-ttu-id="8d767-1460">Исправлена проблема с появлением исключения в процессе отката при добавлении сертификата к модели VMSS: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="8d767-1460">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="8d767-1461">Исправлены некоторые сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="8d767-1461">Fix some error messages.</span></span>
* <span data-ttu-id="8d767-1462">Исправлена проблема с созданием кластера с шаблоном ARM по умолчанию для командлета New-AzServiceFabriCluster, который не работал с операцией миграции в Az.</span><span class="sxs-lookup"><span data-stu-id="8d767-1462">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="8d767-1463">Исправлена проблема с добавлением сертификата кластера или приложения: теперь они добавляются только в Масштабируемые наборы виртуальных машин, которые сопоставлены с кластером, путем проверки идентификатора кластера в расширении.</span><span class="sxs-lookup"><span data-stu-id="8d767-1463">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="8d767-1464">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="8d767-1464">Az.SignalR</span></span>
* <span data-ttu-id="8d767-1465">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="8d767-1465">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d767-1466">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d767-1466">Az.Sql</span></span>
* <span data-ttu-id="8d767-1467">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="8d767-1467">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8d767-1468">Обновлено описание параметра LicenseType с добавлением возможных значений.</span><span class="sxs-lookup"><span data-stu-id="8d767-1468">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="8d767-1469">Исправлена проблема с неправильным обновлением удостоверения управляемого экземпляра, если оно было единственным обновляемым свойством.</span><span class="sxs-lookup"><span data-stu-id="8d767-1469">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="8d767-1470">Поддержка пользовательских параметров сортировки в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="8d767-1470">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d767-1471">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d767-1471">Az.Storage</span></span>
* <span data-ttu-id="8d767-1472">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="8d767-1472">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8d767-1473">Добавлен вывод подробных сообщений об ошибке при получении или установке классических свойств ведения журнала или метрик в учетной записи хранилища класса Premium, так как учетная запись хранилища класса Premium не поддерживает классические функции ведения журнала и метрик.</span><span class="sxs-lookup"><span data-stu-id="8d767-1473">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="8d767-1474">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="8d767-1474">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="8d767-1475">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="8d767-1475">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="8d767-1476">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="8d767-1476">Az.TrafficManager</span></span>
* <span data-ttu-id="8d767-1477">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="8d767-1477">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8d767-1478">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d767-1478">Az.Websites</span></span>
* <span data-ttu-id="8d767-1479">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="8d767-1479">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8d767-1480">Исправлена работа командлета New-AzWebAppSSLBinding: сертификат отправляется в правильную группу ресурсов и правильное расположение, если приложение размещено в ASE.</span><span class="sxs-lookup"><span data-stu-id="8d767-1480">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="8d767-1481">Исправлена работа командлета New-AzWebAppSSLBinding: теги не перезаписываются при привязке SSL-сертификата к приложению.</span><span class="sxs-lookup"><span data-stu-id="8d767-1481">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="8d767-1482">1.1.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="8d767-1482">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8d767-1483">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d767-1483">Az.Accounts</span></span>
* <span data-ttu-id="8d767-1484">Добавление области "Local" в Enable-AzureRmAlias.</span><span class="sxs-lookup"><span data-stu-id="8d767-1484">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d767-1485">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d767-1485">Az.Compute</span></span>
* <span data-ttu-id="8d767-1486">Теперь имя не является обязательным в идентификаторе набора параметров для Restart/Start/Stop/Remove/Set-AzVM и Save-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="8d767-1486">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="8d767-1487">Обновлено описание идентификатора в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="8d767-1487">Updated the description of ID in help files</span></span>
* <span data-ttu-id="8d767-1488">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="8d767-1488">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8d767-1489">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8d767-1489">Az.DataLakeStore</span></span>
* <span data-ttu-id="8d767-1490">Обновление версии пакета SDK для плоскости данных до 1.1.14 для устранения найденных проблем.</span><span class="sxs-lookup"><span data-stu-id="8d767-1490">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="8d767-1491">Исправлена обработка отрицательного времени доступа и времени изменения для getfilestatus и liststatus, исправлен токен отмены для асинхронных методов.</span><span class="sxs-lookup"><span data-stu-id="8d767-1491">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8d767-1492">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8d767-1492">Az.EventGrid</span></span>
* <span data-ttu-id="8d767-1493">Обновление для использования API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="8d767-1493">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="8d767-1494">Обновлены указанные ниже командлеты для поддержки нового сценария в API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="8d767-1494">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="8d767-1495">New-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="8d767-1495">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="8d767-1496">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="8d767-1496">Event Time-To-Live,</span></span>
        - <span data-ttu-id="8d767-1497">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="8d767-1497">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="8d767-1498">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="8d767-1498">Dead letter endpoint.</span></span>
    - <span data-ttu-id="8d767-1499">Update-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="8d767-1499">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="8d767-1500">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="8d767-1500">Event Time-To-Live,</span></span>
        - <span data-ttu-id="8d767-1501">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="8d767-1501">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="8d767-1502">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="8d767-1502">Dead letter endpoint.</span></span>
* <span data-ttu-id="8d767-1503">Для параметра EndpointType добавлены новые значения перечисления (storageQueue и hybridConnection) в командлеты New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="8d767-1503">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="8d767-1504">Если ожидается, что создание или обновление подписки на событие повлечет за собой действия со стороны пользователя, выполняемые вручную, отображается предупреждение при создании или обновлении подписки события.</span><span class="sxs-lookup"><span data-stu-id="8d767-1504">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8d767-1505">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8d767-1505">Az.IotHub</span></span>
* <span data-ttu-id="8d767-1506">Пакет SDK Центра Интернета вещей обновлен до последней версии.</span><span class="sxs-lookup"><span data-stu-id="8d767-1506">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8d767-1507">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8d767-1507">Az.LogicApp</span></span>
* <span data-ttu-id="8d767-1508">Get-AzLogicApp позволяет перечислить все параметры без указанного имени.</span><span class="sxs-lookup"><span data-stu-id="8d767-1508">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d767-1509">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d767-1509">Az.Resources</span></span>
* <span data-ttu-id="8d767-1510">Исправлена проблема с набором параметров при предоставлении параметров "-ODataQuery" и "-ResourceId" для "Get-AzResource".</span><span class="sxs-lookup"><span data-stu-id="8d767-1510">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="8d767-1511">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7875.</span><span class="sxs-lookup"><span data-stu-id="8d767-1511">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="8d767-1512">Исправлена обработка параметра -Custom в New/Set-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="8d767-1512">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="8d767-1513">Исправлена опечатка в документации по New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="8d767-1513">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="8d767-1514">Параметр "-MailNickname" стал обязательным для "New-AzADUser".</span><span class="sxs-lookup"><span data-stu-id="8d767-1514">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="8d767-1515">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8220.</span><span class="sxs-lookup"><span data-stu-id="8d767-1515">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="8d767-1516">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="8d767-1516">Az.SignalR</span></span>
* <span data-ttu-id="8d767-1517">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="8d767-1517">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d767-1518">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d767-1518">Az.Sql</span></span>
* <span data-ttu-id="8d767-1519">Зависимость клиента управления хранением преобразована для общей реализации в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="8d767-1519">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8d767-1520">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d767-1520">Az.Storage</span></span>
* <span data-ttu-id="8d767-1521">Установка параметра StorageAccountName для контекста хранилища в качестве реального имени учетной записи хранения, если она была создана с использованием токена Sas, OAuth или анонимного доступа.</span><span class="sxs-lookup"><span data-stu-id="8d767-1521">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="8d767-1522">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="8d767-1522">New-AzStorageContext</span></span>
* <span data-ttu-id="8d767-1523">Создание токена Sas большого двоичного объекта моментального снимка с параметром "-FullUri". Возвращаемый URI исправлен на URI моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="8d767-1523">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="8d767-1524">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="8d767-1524">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8d767-1525">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d767-1525">Az.Websites</span></span>
* <span data-ttu-id="8d767-1526">Исправлена ошибка синтаксического анализа даты в "Get-AzDeletedWebApp".</span><span class="sxs-lookup"><span data-stu-id="8d767-1526">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="8d767-1527">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="8d767-1527">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="8d767-1528">1.0.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="8d767-1528">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="8d767-1529">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="8d767-1529">General</span></span>

- <span data-ttu-id="8d767-1530">Общедоступная версия модуля Az.</span><span class="sxs-lookup"><span data-stu-id="8d767-1530">General Availability of Az Module</span></span>
- <span data-ttu-id="8d767-1531">Справка в Интернете для каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="8d767-1531">Online help for each module</span></span>
- <span data-ttu-id="8d767-1532">Дополнительные сведения и стратегию развития см. в статье [Announcing New Module 'Az'](https://aka.ms/azps-announce) (Объявление о новом модуле Az)</span><span class="sxs-lookup"><span data-stu-id="8d767-1532">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="8d767-1533">Сведения о миграции с AzureRM см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="8d767-1533">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="8d767-1534">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8d767-1534">Az.Accounts</span></span>
- <span data-ttu-id="8d767-1535">Изменено с Az.Profile.</span><span class="sxs-lookup"><span data-stu-id="8d767-1535">Changed from Az.Profile</span></span>
- <span data-ttu-id="8d767-1536">Исправлены форматы таблиц для типов профиля и контекста.</span><span class="sxs-lookup"><span data-stu-id="8d767-1536">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="8d767-1537">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8d767-1537">Az.ApiManagement</span></span>
- <span data-ttu-id="8d767-1538">Исправления для #7002.</span><span class="sxs-lookup"><span data-stu-id="8d767-1538">Fixes for #7002</span></span>
- <span data-ttu-id="8d767-1539">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="8d767-1539">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="8d767-1540">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8d767-1540">Az.Batch</span></span>
- <span data-ttu-id="8d767-1541">Добавлена возможность видеть, какая версия агента узла пакетной службы Azure работает в пуле на каждой виртуальной машине, с помощью нового свойства `NodeAgentInformation` в `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="8d767-1541">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="8d767-1542">Значение `Caching` по умолчанию для `PSDataDisk` теперь `ReadWrite` вместо `None`.</span><span class="sxs-lookup"><span data-stu-id="8d767-1542">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="8d767-1543">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="8d767-1543">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="8d767-1544">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="8d767-1544">Az.Billing</span></span>
- <span data-ttu-id="8d767-1545">Объединены командлеты Billing, Consumption и UsageAggregates. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0).</span><span class="sxs-lookup"><span data-stu-id="8d767-1545">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="8d767-1546">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="8d767-1546">Az.CognitivServices</span></span>
- <span data-ttu-id="8d767-1547">Добавлены средства заполнения для SkuName и Typem, доступные в операции New-AzureRmCognitiveServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="8d767-1547">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="8d767-1548">Удален набор параметров GetSkusWithAccountParamSetName из Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="8d767-1548">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="8d767-1549">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8d767-1549">Az.ContainerInstance</span></span>
- <span data-ttu-id="8d767-1550">Добавлена поддержка ManagedIdentity.</span><span class="sxs-lookup"><span data-stu-id="8d767-1550">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="8d767-1551">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="8d767-1551">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="8d767-1552">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="8d767-1552">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="8d767-1553">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8d767-1553">Az.DataLakeStore</span></span>
- <span data-ttu-id="8d767-1554">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="8d767-1554">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="8d767-1555">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8d767-1555">Az.Monitor</span></span>
- <span data-ttu-id="8d767-1556">"Az.Insights" переименован в "Az.Monitor" и внесены другие незначительные критические изменения. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="8d767-1556">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="8d767-1557">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8d767-1557">Az.KeyVault</span></span>
- <span data-ttu-id="8d767-1558">Из типов вывода удалено устаревшее свойство PurgeDisabled</span><span class="sxs-lookup"><span data-stu-id="8d767-1558">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="8d767-1559">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="8d767-1559">Az.MachineLearning</span></span>
- <span data-ttu-id="8d767-1560">Включены командлеты из модуля Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="8d767-1560">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="8d767-1561">Az.Media</span><span class="sxs-lookup"><span data-stu-id="8d767-1561">Az.Media</span></span>
- <span data-ttu-id="8d767-1562">Удаляет устаревший псевдоним Tags из New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="8d767-1562">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="8d767-1563">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d767-1563">Az.Network</span></span>
<span data-ttu-id="8d767-1564">В шлюз приложений добавлена поддержка настройки RewriteRuleSets</span><span class="sxs-lookup"><span data-stu-id="8d767-1564">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="8d767-1565">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="8d767-1565">New cmdlets added:</span></span>
        - <span data-ttu-id="8d767-1566">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8d767-1566">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8d767-1567">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8d767-1567">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8d767-1568">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8d767-1568">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8d767-1569">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8d767-1569">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8d767-1570">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8d767-1570">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8d767-1571">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="8d767-1571">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="8d767-1572">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="8d767-1572">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="8d767-1573">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="8d767-1573">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="8d767-1574">В следующие командлеты добавлен необязательный параметр -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8d767-1574">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="8d767-1575">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8d767-1575">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="8d767-1576">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8d767-1576">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="8d767-1577">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8d767-1577">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="8d767-1578">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8d767-1578">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="8d767-1579">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="8d767-1579">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="8d767-1580">New-AzureRmApplicationGatewayUrlPathMapConfig добавил с помощью идентификатора поддержку KeyVault для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="8d767-1580">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="8d767-1581">В следующие командлеты добавлен необязательный параметр -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="8d767-1581">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="8d767-1582">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8d767-1582">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="8d767-1583">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8d767-1583">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="8d767-1584">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8d767-1584">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="8d767-1585">В командлет New-AzApplicationGateway добавлен необязательный параметр -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="8d767-1585">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="8d767-1586">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="8d767-1586">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="8d767-1587">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8d767-1587">Az.OperationalInsights</span></span>
- <span data-ttu-id="8d767-1588">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="8d767-1588">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="8d767-1589">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8d767-1589">Az.Profile</span></span>
- <span data-ttu-id="8d767-1590">Имя модуля изменено на Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="8d767-1590">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="8d767-1591">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d767-1591">Az.RecoveryServices</span></span>
- <span data-ttu-id="8d767-1592">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="8d767-1592">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="8d767-1593">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d767-1593">Az.Resources</span></span>
- <span data-ttu-id="8d767-1594">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="8d767-1594">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="8d767-1595">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8d767-1595">Az.ServiceFabric</span></span>
- <span data-ttu-id="8d767-1596">Поддержка спецификации сертификата по общему имени и отпечатку</span><span class="sxs-lookup"><span data-stu-id="8d767-1596">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="8d767-1597">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="8d767-1597">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="8d767-1598">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="8d767-1598">Az.SIgnalR</span></span>
- <span data-ttu-id="8d767-1599">Общедоступная версия командлетов PowerShell для SIgnalR</span><span class="sxs-lookup"><span data-stu-id="8d767-1599">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="8d767-1600">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d767-1600">Az.Sql</span></span>
- <span data-ttu-id="8d767-1601">Добавлены новые типы обнаружения Data_Exfiltration и Unsafe_Action в командлеты обнаружения угроз</span><span class="sxs-lookup"><span data-stu-id="8d767-1601">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="8d767-1602">Примеры обновленной документации для командлетов аудита Sql</span><span class="sxs-lookup"><span data-stu-id="8d767-1602">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="8d767-1603">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="8d767-1603">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="8d767-1604">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d767-1604">Az.Storage</span></span>
- <span data-ttu-id="8d767-1605">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="8d767-1605">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="8d767-1606">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d767-1606">Az.Websites</span></span>
- <span data-ttu-id="8d767-1607">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="8d767-1607">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="8d767-1608">0.7.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="8d767-1608">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="8d767-1609">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="8d767-1609">General</span></span>

* <span data-ttu-id="8d767-1610">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="8d767-1610">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="8d767-1611">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d767-1611">Az.Compute</span></span>

* <span data-ttu-id="8d767-1612">Добавлена поддержка UltraSSD и образов коллекции в простых наборах параметров для командлетов `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="8d767-1612">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="8d767-1613">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8d767-1613">Az.DataLakeStore</span></span>

* <span data-ttu-id="8d767-1614">Исправлено косую черту в конце домена учетной записи ADLS</span><span class="sxs-lookup"><span data-stu-id="8d767-1614">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="8d767-1615">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8d767-1615">Az.FrontDoor</span></span>

* <span data-ttu-id="8d767-1616">Исправлены некоторые неработающие ссылки</span><span class="sxs-lookup"><span data-stu-id="8d767-1616">Fixed some broken links</span></span>
    - <span data-ttu-id="8d767-1617">В статьях New-AzureRmFrontDoor и Set-AzureRmFrontDoor исправлена ссылка на статью командлета New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="8d767-1617">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="8d767-1618">В статье New-AzureRmFrontDoorManagedRuleObject исправлена ссылка на статью командлета New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="8d767-1618">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="8d767-1619">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8d767-1619">Az.RecoveryServices</span></span>

* <span data-ttu-id="8d767-1620">Добавлены проверки на стороне клиента для операций восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="8d767-1620">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="8d767-1621">StorageAccountName и storageAccountResourceGroupName являются необязательными для восстановления afs.</span><span class="sxs-lookup"><span data-stu-id="8d767-1621">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="8d767-1622">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d767-1622">Az.Resources</span></span>

* <span data-ttu-id="8d767-1623">Исправление для https://github.com/Azure/azure-powershell/issues/7679.</span><span class="sxs-lookup"><span data-stu-id="8d767-1623">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="8d767-1624">Обновите Get-AzureRmRoleAssignment, чтобы использовать область подписки, если она указана при запросе классических администраторов.</span><span class="sxs-lookup"><span data-stu-id="8d767-1624">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="8d767-1625">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d767-1625">Az.Sql</span></span>

* <span data-ttu-id="8d767-1626">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="8d767-1626">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="8d767-1627">Устранена проблема с использованием Get-AzureRmSqlDatabaseVulnerabilityAssessment с .NET Core.</span><span class="sxs-lookup"><span data-stu-id="8d767-1627">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="8d767-1628">Изменена документация справочных сообщений, связанных с командлетами аудита SQL.</span><span class="sxs-lookup"><span data-stu-id="8d767-1628">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="8d767-1629">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8d767-1629">Az.Storage</span></span>

* <span data-ttu-id="8d767-1630">Добавлено -EnableHierarchicalNamespace к New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8d767-1630">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="8d767-1631">Устранена проблема, из-за которой командлет Copy File не может повторно использовать исходный контекст в пункте назначения, если не введен -DestContext</span><span class="sxs-lookup"><span data-stu-id="8d767-1631">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="8d767-1632">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="8d767-1632">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="8d767-1633">Поддержка статической конфигурации сайта</span><span class="sxs-lookup"><span data-stu-id="8d767-1633">Support Static Website configuration</span></span>
    - <span data-ttu-id="8d767-1634">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="8d767-1634">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="8d767-1635">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="8d767-1635">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="8d767-1636">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d767-1636">Az.Websites</span></span>

* <span data-ttu-id="8d767-1637">Set-AzureRmWebApp и Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8d767-1637">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="8d767-1638">Добавлен новый параметр (-AzureStoragePath), который указывает путь службы хранилища Azure для подключения в приложениях-контейнерах Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="8d767-1638">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="8d767-1639">Используйте выходные данные нового командлета New-AzureRmWebAppAzureStoragePath в качестве параметра, чтобы задать пути к службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="8d767-1639">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="8d767-1640">0.6.1 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="8d767-1640">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="8d767-1641">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8d767-1641">Az.ApiManagement</span></span>
* <span data-ttu-id="8d767-1642">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="8d767-1642">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="8d767-1643">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8d767-1643">Az.Automation</span></span>
* <span data-ttu-id="8d767-1644">Командлеты службы автоматизации Azure на базе Swagger.</span><span class="sxs-lookup"><span data-stu-id="8d767-1644">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="8d767-1645">Добавлены командлеты для Управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="8d767-1645">Added Update Management cmdlets</span></span>
* <span data-ttu-id="8d767-1646">Добавлены командлеты для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="8d767-1646">Added Source Control cmdlets</span></span>
* <span data-ttu-id="8d767-1647">Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="8d767-1647">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="8d767-1648">Исправлена команда DSC для регистрации узла.</span><span class="sxs-lookup"><span data-stu-id="8d767-1648">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="8d767-1649">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d767-1649">Az.Compute</span></span>
* <span data-ttu-id="8d767-1650">Исправлена проблема с удостоверением, назначаемым системой.</span><span class="sxs-lookup"><span data-stu-id="8d767-1650">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="8d767-1651">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="8d767-1651">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="8d767-1652">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8d767-1652">Az.ContainerInstance</span></span>
* <span data-ttu-id="8d767-1653">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="8d767-1653">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="8d767-1654">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="8d767-1654">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="8d767-1655">Обновлено описание в примерах командлетов для Marketplace.</span><span class="sxs-lookup"><span data-stu-id="8d767-1655">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="8d767-1656">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d767-1656">Az.Network</span></span>
* <span data-ttu-id="8d767-1657">Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="8d767-1657">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="8d767-1658">Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="8d767-1658">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="8d767-1659">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="8d767-1659">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="8d767-1660">Исправлены проблемы с использованием памяти в карте виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="8d767-1660">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="8d767-1661">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="8d767-1661">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="8d767-1662">Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="8d767-1662">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="8d767-1663">Параметры часового пояса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="8d767-1663">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="8d767-1664">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="8d767-1664">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="8d767-1665">Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="8d767-1665">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="8d767-1666">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="8d767-1666">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="8d767-1667">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="8d767-1667">Az.Relay</span></span>
* <span data-ttu-id="8d767-1668">Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.</span><span class="sxs-lookup"><span data-stu-id="8d767-1668">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="8d767-1669">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d767-1669">Az.Resources</span></span>
* <span data-ttu-id="8d767-1670">Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.</span><span class="sxs-lookup"><span data-stu-id="8d767-1670">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="8d767-1671">Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.</span><span class="sxs-lookup"><span data-stu-id="8d767-1671">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="8d767-1672">Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.</span><span class="sxs-lookup"><span data-stu-id="8d767-1672">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="8d767-1673">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8d767-1673">Az.ServiceFabric</span></span>
* <span data-ttu-id="8d767-1674">Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.</span><span class="sxs-lookup"><span data-stu-id="8d767-1674">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="8d767-1675">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d767-1675">Az.Sql</span></span>
* <span data-ttu-id="8d767-1676">Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="8d767-1676">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="8d767-1677">Get-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="8d767-1677">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8d767-1678">New-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="8d767-1678">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8d767-1679">Set-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="8d767-1679">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8d767-1680">Remove-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="8d767-1680">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8d767-1681">Get-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="8d767-1681">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="8d767-1682">New-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="8d767-1682">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="8d767-1683">Restore-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="8d767-1683">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="8d767-1684">Remove-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="8d767-1684">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="8d767-1685">Добавлено расширенное управление политиками аудита для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="8d767-1685">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="8d767-1686">Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="8d767-1686">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="8d767-1687">Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.</span><span class="sxs-lookup"><span data-stu-id="8d767-1687">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="8d767-1688">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="8d767-1688">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="8d767-1689">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="8d767-1689">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="8d767-1690">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="8d767-1690">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="8d767-1691">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="8d767-1691">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="8d767-1692">Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="8d767-1692">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="8d767-1693">0.5.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="8d767-1693">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="8d767-1694">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="8d767-1694">General</span></span>
* <span data-ttu-id="8d767-1695">Добавлены средства заполнения ресурсов для многих основных командлетов — они позволяют вам переключать существующие имена ресурсов при вызове командлетов в интерактивном режиме</span><span class="sxs-lookup"><span data-stu-id="8d767-1695">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="8d767-1696">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8d767-1696">Az.Profile</span></span>
* <span data-ttu-id="8d767-1697">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8d767-1697">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="8d767-1698">В командлете Connect-AzAccount параметр TenantId переименован в Tenant и добавлен псевдоним для TenantId</span><span class="sxs-lookup"><span data-stu-id="8d767-1698">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="8d767-1699">Обновлено описание TenantId для командлета Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="8d767-1699">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="8d767-1700">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="8d767-1700">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="8d767-1701">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="8d767-1701">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="8d767-1702">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="8d767-1702">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="8d767-1703">Устранена проблема, при которой командлет Disconnect-AzAccount вызывал сбой при отсутствии подключения</span><span class="sxs-lookup"><span data-stu-id="8d767-1703">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="8d767-1704">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8d767-1704">Az.CognitiveServices</span></span>
* <span data-ttu-id="8d767-1705">Добавлена операция Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="8d767-1705">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d767-1706">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d767-1706">Az.Compute</span></span>
* <span data-ttu-id="8d767-1707">Добавлены командлеты Add-AzVmssVMDataDisk и Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="8d767-1707">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="8d767-1708">Get-AzVMImage отображает AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="8d767-1708">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="8d767-1709">Устранена проблема, при которой значения параметров SetAzVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="8d767-1709">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8d767-1710">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8d767-1710">Az.DataLakeStore</span></span>
* <span data-ttu-id="8d767-1711">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="8d767-1711">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="8d767-1712">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="8d767-1712">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="8d767-1713">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="8d767-1713">Az.Insights</span></span>
* <span data-ttu-id="8d767-1714">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="8d767-1714">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="8d767-1715">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="8d767-1715">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="8d767-1716">Исправлена проблема № 7513 [Insights], при которой для командлета Set-AzDiagnosticSetting требовалось явное указание категорий во время создания параметра</span><span class="sxs-lookup"><span data-stu-id="8d767-1716">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="8d767-1717">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="8d767-1717">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d767-1718">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d767-1718">Az.Network</span></span>
* <span data-ttu-id="8d767-1719">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="8d767-1719">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="8d767-1720">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="8d767-1720">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="8d767-1721">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="8d767-1721">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="8d767-1722">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="8d767-1722">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="8d767-1723">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="8d767-1723">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="8d767-1724">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="8d767-1724">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="8d767-1725">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="8d767-1725">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8d767-1726">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8d767-1726">Az.PolicyInsights</span></span>
* <span data-ttu-id="8d767-1727">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="8d767-1727">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d767-1728">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d767-1728">Az.Resources</span></span>
* <span data-ttu-id="8d767-1729">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="8d767-1729">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="8d767-1730">Разрешено перечисление ресурсов с помощью параметра -ResourceId для командлета Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="8d767-1730">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8d767-1731">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8d767-1731">Az.ServiceBus</span></span>
* <span data-ttu-id="8d767-1732">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="8d767-1732">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8d767-1733">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8d767-1733">Az.ServiceFabric</span></span>
* <span data-ttu-id="8d767-1734">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="8d767-1734">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="8d767-1735">Исправлен командлет Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="8d767-1735">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="8d767-1736">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="8d767-1736">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="8d767-1737">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="8d767-1737">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="8d767-1738">Исправлен командлет Update-AzServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="8d767-1738">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="8d767-1739">0.4.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="8d767-1739">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="8d767-1740">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8d767-1740">Az.Profile</span></span>
* <span data-ttu-id="8d767-1741">Устранена проблема с Get-AzSubscription в CloudShell</span><span class="sxs-lookup"><span data-stu-id="8d767-1741">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="8d767-1742">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8d767-1742">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d767-1743">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d767-1743">Az.Compute</span></span>
* <span data-ttu-id="8d767-1744">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzVm</span><span class="sxs-lookup"><span data-stu-id="8d767-1744">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="8d767-1745">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="8d767-1745">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8d767-1746">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8d767-1746">Az.DataLakeStore</span></span>
* <span data-ttu-id="8d767-1747">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="8d767-1747">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="8d767-1748">Get-AzDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8d767-1748">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="8d767-1749">Add-AzDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8d767-1749">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="8d767-1750">Set-AzDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8d767-1750">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="8d767-1751">Remove-AzDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8d767-1751">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d767-1752">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d767-1752">Az.Network</span></span>
* <span data-ttu-id="8d767-1753">Обновлен командлет Test-AzNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="8d767-1753">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="8d767-1754">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="8d767-1754">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d767-1755">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d767-1755">Az.Resources</span></span>
* <span data-ttu-id="8d767-1756">Устранена проблема, из-за которой командлет Get-AzRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), благодаря добавлению понятного исключения в сценарий.</span><span class="sxs-lookup"><span data-stu-id="8d767-1756">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="8d767-1757">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="8d767-1757">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="8d767-1758">0.3.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="8d767-1758">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="8d767-1759">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="8d767-1759">Azure.Storage</span></span>
* <span data-ttu-id="8d767-1760">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="8d767-1760">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="8d767-1761">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="8d767-1761">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="8d767-1762">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="8d767-1762">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="8d767-1763">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="8d767-1763">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="8d767-1764">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="8d767-1764">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="8d767-1765">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8d767-1765">Az.CognitiveServices</span></span>
* <span data-ttu-id="8d767-1766">Поддержка Get-AzCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="8d767-1766">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8d767-1767">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8d767-1767">Az.Compute</span></span>
* <span data-ttu-id="8d767-1768">Исправлена команда Get-AzVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов</span><span class="sxs-lookup"><span data-stu-id="8d767-1768">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="8d767-1769">Добавлен пример использования SimpleParameterSet в справку командлета New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="8d767-1769">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="8d767-1770">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="8d767-1770">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="8d767-1771">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="8d767-1771">Az.DataFactoryV2</span></span>
* <span data-ttu-id="8d767-1772">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="8d767-1772">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8d767-1773">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8d767-1773">Az.Network</span></span>
* <span data-ttu-id="8d767-1774">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="8d767-1774">Added NetworkProfile functionality.</span></span> <span data-ttu-id="8d767-1775">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="8d767-1775">new cmdlets added</span></span>
    - <span data-ttu-id="8d767-1776">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8d767-1776">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="8d767-1777">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8d767-1777">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="8d767-1778">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8d767-1778">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="8d767-1779">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8d767-1779">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="8d767-1780">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="8d767-1780">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="8d767-1781">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="8d767-1781">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="8d767-1782">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="8d767-1782">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="8d767-1783">Добавлены командлеты: New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="8d767-1783">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="8d767-1784">Добавлены командлеты: Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="8d767-1784">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="8d767-1785">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8d767-1785">Az.RedisCache</span></span>
* <span data-ttu-id="8d767-1786">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="8d767-1786">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="8d767-1787">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="8d767-1787">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="8d767-1788">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8d767-1788">Az.Resources</span></span>
* <span data-ttu-id="8d767-1789">Добавлен отсутствующий параметр -Mode в командлет Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8d767-1789">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="8d767-1790">Исправлена ошибка командлета Get-AzProviderOperation для операций, когда Origin содержит User</span><span class="sxs-lookup"><span data-stu-id="8d767-1790">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="8d767-1791">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8d767-1791">Az.Sql</span></span>
* <span data-ttu-id="8d767-1792">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="8d767-1792">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8d767-1793">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8d767-1793">Az.Websites</span></span>
* <span data-ttu-id="8d767-1794">Новый командлет Get-AzWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="8d767-1794">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="8d767-1795">Новые командлеты New-AzWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows</span><span class="sxs-lookup"><span data-stu-id="8d767-1795">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="8d767-1796">0.2.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="8d767-1796">0.2.0 - September 2018</span></span>
 <span data-ttu-id="8d767-1797">Первый выпуск</span><span class="sxs-lookup"><span data-stu-id="8d767-1797">Initial Release</span></span>
